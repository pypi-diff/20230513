# Comparing `tmp/pyinstaller-5.8.0.tar.gz` & `tmp/pyinstaller-5.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyinstaller-5.8.0.tar", last modified: Sat Feb 11 15:00:28 2023, max compression
+gzip compressed data, was "pyinstaller-5.9.0.tar", last modified: Mon Mar 13 20:35:17 2023, max compression
```

## Comparing `pyinstaller-5.8.0.tar` & `pyinstaller-5.9.0.tar`

### file list

```diff
@@ -1,687 +1,1760 @@
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.664231 pyinstaller-5.8.0/
--rwxrwxrwx   0 root         (0) root         (0)    32138 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/COPYING.txt
--rwxrwxrwx   0 root         (0) root         (0)      846 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/MANIFEST.in
--rwxrwxrwx   0 root         (0) root         (0)     7872 2023-02-11 15:00:28.664440 pyinstaller-5.8.0/PKG-INFO
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.473219 pyinstaller-5.8.0/PyInstaller/
--rwxrwxrwx   0 root         (0) root         (0)     2997 2023-02-11 14:47:41.000000 pyinstaller-5.8.0/PyInstaller/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     7103 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/__main__.py
--rwxrwxrwx   0 root         (0) root         (0)     1821 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/_recursion_too_deep_message.py
--rwxrwxrwx   0 root         (0) root         (0)     3911 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/_shared_with_waf.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.474264 pyinstaller-5.8.0/PyInstaller/archive/
--rwxrwxrwx   0 root         (0) root         (0)       23 2022-12-03 11:32:23.000000 pyinstaller-5.8.0/PyInstaller/archive/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     1730 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/archive/pyz_crypto.py
--rwxrwxrwx   0 root         (0) root         (0)     8186 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/archive/readers.py
--rwxrwxrwx   0 root         (0) root         (0)    23757 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/archive/writers.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.467507 pyinstaller-5.8.0/PyInstaller/bootloader/
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.477872 pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/
--rwxrwxrwx   0 root         (0) root         (0)   189104 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/run
--rwxrwxrwx   0 root         (0) root         (0)   189096 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/run_d
--rwxrwxrwx   0 root         (0) root         (0)   191896 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/runw
--rwxrwxrwx   0 root         (0) root         (0)   241192 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/runw_d
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.482620 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/
--rwxrwxrwx   0 root         (0) root         (0)   219648 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/run.exe
--rwxrwxrwx   0 root         (0) root         (0)   224256 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/run_d.exe
--rwxrwxrwx   0 root         (0) root         (0)   220672 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/runw.exe
--rwxrwxrwx   0 root         (0) root         (0)   225280 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/runw_d.exe
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.487592 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/
--rwxrwxrwx   0 root         (0) root         (0)   258048 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/run.exe
--rwxrwxrwx   0 root         (0) root         (0)   263168 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/run_d.exe
--rwxrwxrwx   0 root         (0) root         (0)   258560 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/runw.exe
--rwxrwxrwx   0 root         (0) root         (0)   264192 2023-02-11 14:56:01.000000 pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/runw_d.exe
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.490708 pyinstaller-5.8.0/PyInstaller/bootloader/images/
--rwxrwxrwx   0 root         (0) root         (0)   106001 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-console.icns
--rwxrwxrwx   0 root         (0) root         (0)    59521 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-console.ico
--rwxrwxrwx   0 root         (0) root         (0)   110199 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-windowed.icns
--rwxrwxrwx   0 root         (0) root         (0)    60690 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-windowed.ico
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.494703 pyinstaller-5.8.0/PyInstaller/building/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:23.000000 pyinstaller-5.8.0/PyInstaller/building/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)    54255 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/api.py
--rwxrwxrwx   0 root         (0) root         (0)    43404 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/build_main.py
--rwxrwxrwx   0 root         (0) root         (0)    10868 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/datastruct.py
--rwxrwxrwx   0 root         (0) root         (0)     3574 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/icon.py
--rwxrwxrwx   0 root         (0) root         (0)    32485 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/makespec.py
--rwxrwxrwx   0 root         (0) root         (0)    13060 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/osx.py
--rwxrwxrwx   0 root         (0) root         (0)    22976 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/splash.py
--rwxrwxrwx   0 root         (0) root         (0)     7453 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/splash_templates.py
--rwxrwxrwx   0 root         (0) root         (0)     3642 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/templates.py
--rwxrwxrwx   0 root         (0) root         (0)     6493 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/toc_conversion.py
--rwxrwxrwx   0 root         (0) root         (0)    32929 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/building/utils.py
--rwxrwxrwx   0 root         (0) root         (0)    32104 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/compat.py
--rwxrwxrwx   0 root         (0) root         (0)     1727 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/config.py
--rwxrwxrwx   0 root         (0) root         (0)     3343 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/configure.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.497510 pyinstaller-5.8.0/PyInstaller/depend/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:23.000000 pyinstaller-5.8.0/PyInstaller/depend/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)    43344 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/analysis.py
--rwxrwxrwx   0 root         (0) root         (0)    44289 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/bindepend.py
--rwxrwxrwx   0 root         (0) root         (0)    12576 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/bytecode.py
--rwxrwxrwx   0 root         (0) root         (0)    15844 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/dylib.py
--rwxrwxrwx   0 root         (0) root         (0)    25659 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/imphook.py
--rwxrwxrwx   0 root         (0) root         (0)    20149 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/imphookapi.py
--rwxrwxrwx   0 root         (0) root         (0)    17332 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/depend/utils.py
--rwxrwxrwx   0 root         (0) root         (0)     1101 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/exceptions.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.497851 pyinstaller-5.8.0/PyInstaller/fake-modules/
--rwxrwxrwx   0 root         (0) root         (0)     8555 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/fake-modules/pyi_splash.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.584957 pyinstaller-5.8.0/PyInstaller/hooks/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:24.000000 pyinstaller-5.8.0/PyInstaller/hooks/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      845 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.Image.py
--rwxrwxrwx   0 root         (0) root         (0)      589 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.ImageFilter.py
--rwxrwxrwx   0 root         (0) root         (0)      773 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.SpiderImagePlugin.py
--rwxrwxrwx   0 root         (0) root         (0)     1100 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QAxContainer.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qsci.py
--rwxrwxrwx   0 root         (0) root         (0)     1274 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DAnimation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DInput.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DLogic.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DRender.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtBluetooth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtChart.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDBus.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDataVisualization.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDesigner.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtGui.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtHelp.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtLocation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMacExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMultimedia.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMultimediaWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNetwork.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNetworkAuth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNfc.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtOpenGL.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPositioning.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPrintSupport.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPurchasing.py
--rwxrwxrwx   0 root         (0) root         (0)      764 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuick3D.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuickWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtRemoteObjects.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtScript.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSensors.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSerialPort.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSql.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSvg.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtTest.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtTextToSpeech.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebChannel.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngine.py
--rwxrwxrwx   0 root         (0) root         (0)      995 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebKit.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebKitWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebSockets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWinExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtX11Extras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtXml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtXmlPatterns.py
--rwxrwxrwx   0 root         (0) root         (0)     1027 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.py
--rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.uic.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QAxContainer.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qsci.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DAnimation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DInput.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DLogic.py
--rwxrwxrwx   0 root         (0) root         (0)      670 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DRender.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtBluetooth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtCharts.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDBus.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDataVisualization.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDesigner.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtGui.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtHelp.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtMultimedia.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtMultimediaWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNetwork.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNetworkAuth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNfc.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtOpenGL.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtOpenGLWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPdf.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPdfWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPositioning.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPrintSupport.py
--rwxrwxrwx   0 root         (0) root         (0)      764 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuick3D.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuickWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtRemoteObjects.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSensors.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSerialPort.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSql.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSvg.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSvgWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtTest.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebChannel.py
--rwxrwxrwx   0 root         (0) root         (0)     1351 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebSockets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtXml.py
--rwxrwxrwx   0 root         (0) root         (0)      870 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.py
--rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.uic.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DAnimation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DInput.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DLogic.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DRender.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtAxContainer.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtCharts.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtConcurrent.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtDataVisualization.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtGui.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtHelp.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtLocation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMacExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMultimedia.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMultimediaWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      714 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtNetwork.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtOpenGL.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtOpenGLFunctions.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtPositioning.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtPrintSupport.py
--rwxrwxrwx   0 root         (0) root         (0)      804 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuickControls2.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuickWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtRemoteObjects.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScript.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScriptTools.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScxml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSensors.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSerialPort.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSql.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSvg.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtTest.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtTextToSpeech.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtUiTools.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebChannel.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngine.py
--rwxrwxrwx   0 root         (0) root         (0)     1003 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngineCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngineWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebKit.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebKitWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebSockets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWinExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtX11Extras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtXml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtXmlPatterns.py
--rwxrwxrwx   0 root         (0) root         (0)      972 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qwt5.py
--rwxrwxrwx   0 root         (0) root         (0)      984 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DAnimation.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DExtras.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DInput.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DLogic.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DRender.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtAxContainer.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtBluetooth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtCharts.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtConcurrent.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDBus.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDataVisualization.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDesigner.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtGui.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtHelp.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtHttpServer.py
--rwxrwxrwx   0 root         (0) root         (0)      981 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtMultimedia.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtMultimediaWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      714 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNetwork.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNetworkAuth.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNfc.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtOpenGL.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtOpenGLWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPdf.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPdfWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPositioning.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPrintSupport.py
--rwxrwxrwx   0 root         (0) root         (0)      768 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuick3D.py
--rwxrwxrwx   0 root         (0) root         (0)      671 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuickControls2.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuickWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtRemoteObjects.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtScxml.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSensors.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSerialPort.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSpatialAudio.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSql.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtStateMachine.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSvg.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSvgWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtTest.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtUiTools.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebChannel.py
--rwxrwxrwx   0 root         (0) root         (0)     1410 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineCore.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineQuick.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebSockets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWidgets.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtXml.py
--rwxrwxrwx   0 root         (0) root         (0)     1126 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.py
--rwxrwxrwx   0 root         (0) root         (0)     1327 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-_tkinter.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-babel.py
--rwxrwxrwx   0 root         (0) root         (0)      577 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-difflib.py
--rwxrwxrwx   0 root         (0) root         (0)     1863 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-distutils.py
--rwxrwxrwx   0 root         (0) root         (0)      661 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-distutils.util.py
--rwxrwxrwx   0 root         (0) root         (0)      635 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.contrib.sessions.py
--rwxrwxrwx   0 root         (0) root         (0)      629 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.cache.py
--rwxrwxrwx   0 root         (0) root         (0)     1069 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.mail.py
--rwxrwxrwx   0 root         (0) root         (0)      942 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.management.py
--rwxrwxrwx   0 root         (0) root         (0)      611 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.mysql.base.py
--rwxrwxrwx   0 root         (0) root         (0)      563 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.oracle.base.py
--rwxrwxrwx   0 root         (0) root         (0)      983 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.py
--rwxrwxrwx   0 root         (0) root         (0)     3922 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.py
--rwxrwxrwx   0 root         (0) root         (0)      626 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-django.template.loaders.py
--rwxrwxrwx   0 root         (0) root         (0)      612 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-encodings.py
--rwxrwxrwx   0 root         (0) root         (0)     1011 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gevent.py
--rwxrwxrwx   0 root         (0) root         (0)      552 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.py
--rwxrwxrwx   0 root         (0) root         (0)      698 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Adw.py
--rwxrwxrwx   0 root         (0) root         (0)     1084 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Atk.py
--rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Champlain.py
--rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Clutter.py
--rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GIRepository.py
--rwxrwxrwx   0 root         (0) root         (0)     1490 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GLib.py
--rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GModule.py
--rwxrwxrwx   0 root         (0) root         (0)      909 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GObject.py
--rwxrwxrwx   0 root         (0) root         (0)     1393 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gdk.py
--rwxrwxrwx   0 root         (0) root         (0)     5846 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GdkPixbuf.py
--rwxrwxrwx   0 root         (0) root         (0)     2605 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gio.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Graphene.py
--rwxrwxrwx   0 root         (0) root         (0)      700 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gsk.py
--rwxrwxrwx   0 root         (0) root         (0)     3461 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gst.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstAllocators.py
--rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstApp.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstAudio.py
--rwxrwxrwx   0 root         (0) root         (0)      708 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstBadAudio.py
--rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstBase.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstCheck.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstCodecs.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstController.py
--rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGL.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLEGL.py
--rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLWayland.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLX11.py
--rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstInsertBin.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstMpegts.py
--rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstNet.py
--rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPbutils.py
--rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPlay.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPlayer.py
--rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtp.py
--rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtsp.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtspServer.py
--rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstSdp.py
--rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstTag.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstTranscoder.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVideo.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkan.py
--rwxrwxrwx   0 root         (0) root         (0)      713 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkanWayland.py
--rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkanXCB.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstWebRTC.py
--rwxrwxrwx   0 root         (0) root         (0)     2150 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gtk.py
--rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkChamplain.py
--rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkClutter.py
--rwxrwxrwx   0 root         (0) root         (0)     1297 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkSource.py
--rwxrwxrwx   0 root         (0) root         (0)      781 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkosxApplication.py
--rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.HarfBuzz.py
--rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Pango.py
--rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.PangoCairo.py
--rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.cairo.py
--rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.freetype2.py
--rwxrwxrwx   0 root         (0) root         (0)      701 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.xlib.py
--rwxrwxrwx   0 root         (0) root         (0)      578 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-heapq.py
--rwxrwxrwx   0 root         (0) root         (0)      602 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-idlelib.py
--rwxrwxrwx   0 root         (0) root         (0)     1350 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-importlib_metadata.py
--rwxrwxrwx   0 root         (0) root         (0)     1021 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-importlib_resources.py
--rwxrwxrwx   0 root         (0) root         (0)      888 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-keyring.py
--rwxrwxrwx   0 root         (0) root         (0)     1130 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-kivy.py
--rwxrwxrwx   0 root         (0) root         (0)      653 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-lib2to3.py
--rwxrwxrwx   0 root         (0) root         (0)     9232 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.backends.py
--rwxrwxrwx   0 root         (0) root         (0)      683 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.numerix.py
--rwxrwxrwx   0 root         (0) root         (0)      701 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.py
--rwxrwxrwx   0 root         (0) root         (0)      791 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-multiprocessing.util.py
--rwxrwxrwx   0 root         (0) root         (0)      799 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-numpy._pytesttester.py
--rwxrwxrwx   0 root         (0) root         (0)     2335 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-numpy.py
--rwxrwxrwx   0 root         (0) root         (0)      577 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-packaging.py
--rwxrwxrwx   0 root         (0) root         (0)      751 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.io.formats.style.py
--rwxrwxrwx   0 root         (0) root         (0)      944 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.plotting.py
--rwxrwxrwx   0 root         (0) root         (0)      959 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.py
--rwxrwxrwx   0 root         (0) root         (0)      589 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pickle.py
--rwxrwxrwx   0 root         (0) root         (0)     2960 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pkg_resources.py
--rwxrwxrwx   0 root         (0) root         (0)      713 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-platform.py
--rwxrwxrwx   0 root         (0) root         (0)     1184 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pygments.py
--rwxrwxrwx   0 root         (0) root         (0)      734 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pytz.py
--rwxrwxrwx   0 root         (0) root         (0)      603 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-pytzdata.py
--rwxrwxrwx   0 root         (0) root         (0)      792 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-qtawesome.py
--rwxrwxrwx   0 root         (0) root         (0)      930 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scapy.layers.all.py
--rwxrwxrwx   0 root         (0) root         (0)      655 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.io.matlab.py
--rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.linalg.py
--rwxrwxrwx   0 root         (0) root         (0)     1608 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.py
--rwxrwxrwx   0 root         (0) root         (0)      611 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.sparse.csgraph.py
--rwxrwxrwx   0 root         (0) root         (0)      797 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.spatial.transform.rotation.py
--rwxrwxrwx   0 root         (0) root         (0)     1317 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.special._ellip_harm_2.py
--rwxrwxrwx   0 root         (0) root         (0)      696 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.special._ufuncs.py
--rwxrwxrwx   0 root         (0) root         (0)      660 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.stats._stats.py
--rwxrwxrwx   0 root         (0) root         (0)      819 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-scrapy.py
--rwxrwxrwx   0 root         (0) root         (0)      599 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-setuptools.msvc.py
--rwxrwxrwx   0 root         (0) root         (0)     2153 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-setuptools.py
--rwxrwxrwx   0 root         (0) root         (0)      603 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-shelve.py
--rwxrwxrwx   0 root         (0) root         (0)     1998 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-sphinx.py
--rwxrwxrwx   0 root         (0) root         (0)     3165 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-sqlalchemy.py
--rwxrwxrwx   0 root         (0) root         (0)      813 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-sqlite3.py
--rwxrwxrwx   0 root         (0) root         (0)     1558 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-sysconfig.py
--rwxrwxrwx   0 root         (0) root         (0)      602 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-wcwidth.py
--rwxrwxrwx   0 root         (0) root         (0)      993 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-win32ctypes.core.py
--rwxrwxrwx   0 root         (0) root         (0)      569 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.dom.domreg.py
--rwxrwxrwx   0 root         (0) root         (0)      615 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.etree.cElementTree.py
--rwxrwxrwx   0 root         (0) root         (0)      569 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.py
--rwxrwxrwx   0 root         (0) root         (0)      539 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/hook-zope.interface.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.585947 pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:24.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      696 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-PyQt5.uic.port_v2.py
--rwxrwxrwx   0 root         (0) root         (0)     2347 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-distutils.py
--rwxrwxrwx   0 root         (0) root         (0)     1412 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-pyi_splash.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.601476 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:24.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     1955 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Adw.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Atk.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Champlain.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Clutter.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GIRepository.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GLib.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GModule.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GObject.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gdk.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GdkPixbuf.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gio.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Graphene.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gsk.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gst.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAllocators.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstApp.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAudio.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBadAudio.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBase.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCheck.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCodecs.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstController.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGL.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLEGL.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLWayland.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLX11.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstInsertBin.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstMpegts.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstNet.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPbutils.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlay.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlayer.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtp.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtsp.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtspServer.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstSdp.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTag.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTranscoder.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVideo.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkan.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanWayland.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanXCB.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstWebRTC.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gtk.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkChamplain.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkClutter.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkSource.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkosxApplication.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.HarfBuzz.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Pango.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.PangoCairo.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.cairo.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.freetype2.py
--rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.xlib.py
--rwxrwxrwx   0 root         (0) root         (0)     1477 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-setuptools.extern.six.moves.py
--rwxrwxrwx   0 root         (0) root         (0)     3731 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-six.moves.py
--rwxrwxrwx   0 root         (0) root         (0)     1240 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-urllib3.packages.six.moves.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.608655 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:24.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     1136 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth__tkinter.py
--rwxrwxrwx   0 root         (0) root         (0)     1013 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_django.py
--rwxrwxrwx   0 root         (0) root         (0)     1309 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gdkpixbuf.py
--rwxrwxrwx   0 root         (0) root         (0)      568 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gi.py
--rwxrwxrwx   0 root         (0) root         (0)      567 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gio.py
--rwxrwxrwx   0 root         (0) root         (0)     1324 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_glib.py
--rwxrwxrwx   0 root         (0) root         (0)     1079 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gstreamer.py
--rwxrwxrwx   0 root         (0) root         (0)      802 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gtk.py
--rwxrwxrwx   0 root         (0) root         (0)     1904 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_inspect.py
--rwxrwxrwx   0 root         (0) root         (0)      665 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_kivy.py
--rwxrwxrwx   0 root         (0) root         (0)     1486 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_mplconfig.py
--rwxrwxrwx   0 root         (0) root         (0)     3991 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_multiprocessing.py
--rwxrwxrwx   0 root         (0) root         (0)     8550 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pkgres.py
--rwxrwxrwx   0 root         (0) root         (0)     4278 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pkgutil.py
--rwxrwxrwx   0 root         (0) root         (0)     1238 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5.py
--rwxrwxrwx   0 root         (0) root         (0)     1380 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5webengine.py
--rwxrwxrwx   0 root         (0) root         (0)     1317 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6.py
--rwxrwxrwx   0 root         (0) root         (0)     1697 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6webengine.py
--rwxrwxrwx   0 root         (0) root         (0)     1293 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2.py
--rwxrwxrwx   0 root         (0) root         (0)     1093 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2webengine.py
--rwxrwxrwx   0 root         (0) root         (0)     1293 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6.py
--rwxrwxrwx   0 root         (0) root         (0)     1484 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6webengine.py
--rwxrwxrwx   0 root         (0) root         (0)     1365 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_setuptools.py
--rwxrwxrwx   0 root         (0) root         (0)     2204 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_win32comgenpy.py
--rwxrwxrwx   0 root         (0) root         (0)     1252 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/hooks/rthooks.dat
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.609388 pyinstaller-5.8.0/PyInstaller/isolated/
--rwxrwxrwx   0 root         (0) root         (0)     1505 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/isolated/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     3696 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/isolated/_child.py
--rwxrwxrwx   0 root         (0) root         (0)    16904 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/isolated/_parent.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.609955 pyinstaller-5.8.0/PyInstaller/lib/
--rwxrwxrwx   0 root         (0) root         (0)     1382 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/README.rst
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/__init__.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.612328 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/
--rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     2742 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/__main__.py
--rwxrwxrwx   0 root         (0) root         (0)      519 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/_compat.py
--rwxrwxrwx   0 root         (0) root         (0)    10651 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/find_modules.py
--rwxrwxrwx   0 root         (0) root         (0)   139611 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/modulegraph.py
--rwxrwxrwx   0 root         (0) root         (0)     4350 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/util.py
--rwxrwxrwx   0 root         (0) root         (0)    10335 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/PyInstaller/lib/modulegraph/zipio.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.614064 pyinstaller-5.8.0/PyInstaller/loader/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:24.000000 pyinstaller-5.8.0/PyInstaller/loader/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     3450 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/loader/pyiboot01_bootstrap.py
--rwxrwxrwx   0 root         (0) root         (0)    10822 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/loader/pyimod01_archive.py
--rwxrwxrwx   0 root         (0) root         (0)    22141 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/loader/pyimod02_importers.py
--rwxrwxrwx   0 root         (0) root         (0)     4915 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/loader/pyimod03_ctypes.py
--rwxrwxrwx   0 root         (0) root         (0)     2440 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/loader/pyimod04_pywin32.py
--rwxrwxrwx   0 root         (0) root         (0)     2058 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/log.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.616251 pyinstaller-5.8.0/PyInstaller/utils/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:25.000000 pyinstaller-5.8.0/PyInstaller/utils/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      451 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/PyInstaller/utils/_gitrevision.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.617825 pyinstaller-5.8.0/PyInstaller/utils/cliutils/
--rwxrwxrwx   0 root         (0) root         (0)        3 2022-12-03 11:32:25.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     7771 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/archive_viewer.py
--rwxrwxrwx   0 root         (0) root         (0)     1742 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/bindepend.py
--rwxrwxrwx   0 root         (0) root         (0)     1714 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/grab_version.py
--rwxrwxrwx   0 root         (0) root         (0)     1502 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/makespec.py
--rwxrwxrwx   0 root         (0) root         (0)     1360 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/cliutils/set_version.py
--rwxrwxrwx   0 root         (0) root         (0)    23530 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/conftest.py
--rwxrwxrwx   0 root         (0) root         (0)     2014 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/git.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.619730 pyinstaller-5.8.0/PyInstaller/utils/hooks/
--rwxrwxrwx   0 root         (0) root         (0)    54533 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)    14787 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/conda.py
--rwxrwxrwx   0 root         (0) root         (0)     6095 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/django.py
--rwxrwxrwx   0 root         (0) root         (0)    17070 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/gi.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.620445 pyinstaller-5.8.0/PyInstaller/utils/hooks/qt/
--rwxrwxrwx   0 root         (0) root         (0)    45378 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/qt/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)    24612 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/qt/_modules_info.py
--rwxrwxrwx   0 root         (0) root         (0)    10947 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/tcl_tk.py
--rwxrwxrwx   0 root         (0) root         (0)     1569 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/hooks/win32.py
--rwxrwxrwx   0 root         (0) root         (0)     7195 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/misc.py
--rwxrwxrwx   0 root         (0) root         (0)    14989 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/osx.py
--rwxrwxrwx   0 root         (0) root         (0)     2839 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/run_tests.py
--rwxrwxrwx   0 root         (0) root         (0)     5766 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/tests.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.622367 pyinstaller-5.8.0/PyInstaller/utils/win32/
--rwxrwxrwx   0 root         (0) root         (0)       23 2022-12-03 11:32:25.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     9151 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/icon.py
--rwxrwxrwx   0 root         (0) root         (0)    20598 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/versioninfo.py
--rwxrwxrwx   0 root         (0) root         (0)    44149 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/winmanifest.py
--rwxrwxrwx   0 root         (0) root         (0)     9621 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/winresource.py
--rwxrwxrwx   0 root         (0) root         (0)    12688 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/PyInstaller/utils/win32/winutils.py
--rwxrwxrwx   0 root         (0) root         (0)     5554 2023-02-11 14:47:41.000000 pyinstaller-5.8.0/README.rst
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.622948 pyinstaller-5.8.0/bootloader/
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.631827 pyinstaller-5.8.0/bootloader/src/
--rwxrwxrwx   0 root         (0) root         (0)     2619 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/main.c
--rwxrwxrwx   0 root         (0) root         (0)      875 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/mkdtemp.h
--rwxrwxrwx   0 root         (0) root         (0)    29474 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_apple_events.c
--rwxrwxrwx   0 root         (0) root         (0)     1825 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_apple_events.h
--rwxrwxrwx   0 root         (0) root         (0)    17949 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_archive.c
--rwxrwxrwx   0 root         (0) root         (0)     5542 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_archive.h
--rwxrwxrwx   0 root         (0) root         (0)    13273 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_exception_dialog.c
--rwxrwxrwx   0 root         (0) root         (0)      822 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_exception_dialog.h
--rwxrwxrwx   0 root         (0) root         (0)     7347 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_global.c
--rwxrwxrwx   0 root         (0) root         (0)     8378 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_global.h
--rwxrwxrwx   0 root         (0) root         (0)    23942 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_launch.c
--rwxrwxrwx   0 root         (0) root         (0)     2316 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_launch.h
--rwxrwxrwx   0 root         (0) root         (0)    15596 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_main.c
--rwxrwxrwx   0 root         (0) root         (0)      564 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_main.h
--rwxrwxrwx   0 root         (0) root         (0)    11094 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_path.c
--rwxrwxrwx   0 root         (0) root         (0)     1465 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_path.h
--rwxrwxrwx   0 root         (0) root         (0)     4850 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_python.c
--rwxrwxrwx   0 root         (0) root         (0)     6457 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_python.h
--rwxrwxrwx   0 root         (0) root         (0)    23303 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_pythonlib.c
--rwxrwxrwx   0 root         (0) root         (0)     1125 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_pythonlib.h
--rwxrwxrwx   0 root         (0) root         (0)    38074 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_splash.c
--rwxrwxrwx   0 root         (0) root         (0)     6003 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_splash.h
--rwxrwxrwx   0 root         (0) root         (0)     3386 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_splashlib.c
--rwxrwxrwx   0 root         (0) root         (0)     4517 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_splashlib.h
--rwxrwxrwx   0 root         (0) root         (0)    44952 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_utils.c
--rwxrwxrwx   0 root         (0) root         (0)     2442 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_utils.h
--rwxrwxrwx   0 root         (0) root         (0)    16726 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_win32_utils.c
--rwxrwxrwx   0 root         (0) root         (0)     1226 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/src/pyi_win32_utils.h
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.632573 pyinstaller-5.8.0/bootloader/tests/
--rwxrwxrwx   0 root         (0) root         (0)     3854 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/tests/test_launch.c
--rwxrwxrwx   0 root         (0) root         (0)     7906 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/tests/test_path.c
--rwxrwxrwx   0 root         (0) root         (0)     1770 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/tests/wscript
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.632816 pyinstaller-5.8.0/bootloader/tools/
--rwxrwxrwx   0 root         (0) root         (0)     1818 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/tools/strip.py
--rwxrwxrwx   0 root         (0) root         (0)     1581 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waf
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.637743 pyinstaller-5.8.0/bootloader/waflib/
--rwxrwxrwx   0 root         (0) root         (0)    30209 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Build.py
--rwxrwxrwx   0 root         (0) root         (0)     5179 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/ConfigSet.py
--rwxrwxrwx   0 root         (0) root         (0)    14831 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Configure.py
--rwxrwxrwx   0 root         (0) root         (0)    14805 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Context.py
--rwxrwxrwx   0 root         (0) root         (0)     1248 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Errors.py
--rwxrwxrwx   0 root         (0) root         (0)     7207 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Logs.py
--rwxrwxrwx   0 root         (0) root         (0)    15286 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Node.py
--rwxrwxrwx   0 root         (0) root         (0)    11367 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Options.py
--rwxrwxrwx   0 root         (0) root         (0)    13041 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Runner.py
--rwxrwxrwx   0 root         (0) root         (0)    15382 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Scripting.py
--rwxrwxrwx   0 root         (0) root         (0)    28095 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Task.py
--rwxrwxrwx   0 root         (0) root         (0)    17611 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/TaskGen.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.654165 pyinstaller-5.8.0/bootloader/waflib/Tools/
--rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)      360 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/ar.py
--rwxrwxrwx   0 root         (0) root         (0)     2090 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/asm.py
--rwxrwxrwx   0 root         (0) root         (0)      933 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/bison.py
--rwxrwxrwx   0 root         (0) root         (0)     1220 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c.py
--rwxrwxrwx   0 root         (0) root         (0)     1893 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c_aliases.py
--rwxrwxrwx   0 root         (0) root         (0)    31501 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c_config.py
--rwxrwxrwx   0 root         (0) root         (0)     5203 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c_osx.py
--rwxrwxrwx   0 root         (0) root         (0)    25054 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c_preproc.py
--rwxrwxrwx   0 root         (0) root         (0)     5042 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/c_tests.py
--rwxrwxrwx   0 root         (0) root         (0)    19729 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/ccroot.py
--rwxrwxrwx   0 root         (0) root         (0)      594 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/clang.py
--rwxrwxrwx   0 root         (0) root         (0)      606 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/clangxx.py
--rwxrwxrwx   0 root         (0) root         (0)     2165 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_c.py
--rwxrwxrwx   0 root         (0) root         (0)     2178 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_cxx.py
--rwxrwxrwx   0 root         (0) root         (0)     1689 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_d.py
--rwxrwxrwx   0 root         (0) root         (0)     2006 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_fc.py
--rwxrwxrwx   0 root         (0) root         (0)     4439 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/cs.py
--rwxrwxrwx   0 root         (0) root         (0)     1295 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/cxx.py
--rwxrwxrwx   0 root         (0) root         (0)     2297 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/d.py
--rwxrwxrwx   0 root         (0) root         (0)     1306 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/d_config.py
--rwxrwxrwx   0 root         (0) root         (0)     4337 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/d_scan.py
--rwxrwxrwx   0 root         (0) root         (0)     1227 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/dbus.py
--rwxrwxrwx   0 root         (0) root         (0)     1643 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/dmd.py
--rwxrwxrwx   0 root         (0) root         (0)     8302 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/errcheck.py
--rwxrwxrwx   0 root         (0) root         (0)     5373 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/fc.py
--rwxrwxrwx   0 root         (0) root         (0)    11313 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/fc_config.py
--rwxrwxrwx   0 root         (0) root         (0)     2414 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/fc_scan.py
--rwxrwxrwx   0 root         (0) root         (0)     1377 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/flex.py
--rwxrwxrwx   0 root         (0) root         (0)     1599 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/g95.py
--rwxrwxrwx   0 root         (0) root         (0)      385 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gas.py
--rwxrwxrwx   0 root         (0) root         (0)     2985 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gcc.py
--rwxrwxrwx   0 root         (0) root         (0)      998 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gdc.py
--rwxrwxrwx   0 root         (0) root         (0)     2225 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gfortran.py
--rwxrwxrwx   0 root         (0) root         (0)    12984 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/glib2.py
--rwxrwxrwx   0 root         (0) root         (0)     3104 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gnu_dirs.py
--rwxrwxrwx   0 root         (0) root         (0)     3054 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/gxx.py
--rwxrwxrwx   0 root         (0) root         (0)      553 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/icc.py
--rwxrwxrwx   0 root         (0) root         (0)      553 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/icpc.py
--rwxrwxrwx   0 root         (0) root         (0)    11869 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/ifort.py
--rwxrwxrwx   0 root         (0) root         (0)     4385 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/intltool.py
--rwxrwxrwx   0 root         (0) root         (0)     1096 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/irixcc.py
--rwxrwxrwx   0 root         (0) root         (0)    13193 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/javaw.py
--rwxrwxrwx   0 root         (0) root         (0)     1068 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/ldc2.py
--rwxrwxrwx   0 root         (0) root         (0)      641 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/lua.py
--rwxrwxrwx   0 root         (0) root         (0)      801 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/md5_tstamp.py
--rwxrwxrwx   0 root         (0) root         (0)    33374 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/msvc.py
--rwxrwxrwx   0 root         (0) root         (0)      686 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/nasm.py
--rwxrwxrwx   0 root         (0) root         (0)      305 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/nobuild.py
--rwxrwxrwx   0 root         (0) root         (0)     3446 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/perl.py
--rwxrwxrwx   0 root         (0) root         (0)    21797 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/python.py
--rwxrwxrwx   0 root         (0) root         (0)    20211 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/qt5.py
--rwxrwxrwx   0 root         (0) root         (0)     4384 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/ruby.py
--rwxrwxrwx   0 root         (0) root         (0)     1324 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/suncc.py
--rwxrwxrwx   0 root         (0) root         (0)     1358 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/suncxx.py
--rwxrwxrwx   0 root         (0) root         (0)    13995 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/tex.py
--rwxrwxrwx   0 root         (0) root         (0)    10164 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/vala.py
--rwxrwxrwx   0 root         (0) root         (0)     7884 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/waf_unit_test.py
--rwxrwxrwx   0 root         (0) root         (0)     2097 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/winres.py
--rwxrwxrwx   0 root         (0) root         (0)     1204 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/xlc.py
--rwxrwxrwx   0 root         (0) root         (0)     1247 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Tools/xlcxx.py
--rwxrwxrwx   0 root         (0) root         (0)    19314 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/Utils.py
--rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)    12079 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/ansiterm.py
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.654413 pyinstaller-5.8.0/bootloader/waflib/extras/
--rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/extras/__init__.py
--rwxrwxrwx   0 root         (0) root         (0)     1509 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/fixpy2.py
--rwxrwxrwx   0 root         (0) root         (0)     1764 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/waflib/processor.py
--rwxrwxrwx   0 root         (0) root         (0)    39431 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/wscript
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.661809 pyinstaller-5.8.0/bootloader/zlib/
--rwxrwxrwx   0 root         (0) root         (0)     5390 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/bootloader/zlib/adler32.c
--rwxrwxrwx   0 root         (0) root         (0)    32250 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/crc32.c
--rwxrwxrwx   0 root         (0) root         (0)   591749 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/zlib/crc32.h
--rwxrwxrwx   0 root         (0) root         (0)     6843 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/zlib/gzguts.h
--rwxrwxrwx   0 root         (0) root         (0)    12998 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/zlib/inffast.c
--rwxrwxrwx   0 root         (0) root         (0)      438 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/bootloader/zlib/inffast.h
--rwxrwxrwx   0 root         (0) root         (0)     6426 2022-11-30 18:58:46.000000 pyinstaller-5.8.0/bootloader/zlib/inffixed.h
--rwxrwxrwx   0 root         (0) root         (0)    56089 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/inflate.c
--rwxrwxrwx   0 root         (0) root         (0)     6683 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/zlib/inflate.h
--rwxrwxrwx   0 root         (0) root         (0)    12999 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/inftrees.c
--rwxrwxrwx   0 root         (0) root         (0)     2927 2023-01-08 13:33:19.000000 pyinstaller-5.8.0/bootloader/zlib/inftrees.h
--rwxrwxrwx   0 root         (0) root         (0)    16625 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/zconf.h
--rwxrwxrwx   0 root         (0) root         (0)    97323 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/zlib.h
--rwxrwxrwx   0 root         (0) root         (0)     7340 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/zutil.c
--rwxrwxrwx   0 root         (0) root         (0)     7297 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/bootloader/zlib/zutil.h
-drwxrwxrwx   0 root         (0) root         (0)        0 2023-02-11 15:00:28.664009 pyinstaller-5.8.0/pyinstaller.egg-info/
--rwxrwxrwx   0 root         (0) root         (0)     7872 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/PKG-INFO
--rwxrwxrwx   0 root         (0) root         (0)    27687 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/SOURCES.txt
--rwxrwxrwx   0 root         (0) root         (0)        1 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/dependency_links.txt
--rwxrwxrwx   0 root         (0) root         (0)      376 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/entry_points.txt
--rwxrwxrwx   0 root         (0) root         (0)        1 2023-02-11 15:00:15.000000 pyinstaller-5.8.0/pyinstaller.egg-info/not-zip-safe
--rwxrwxrwx   0 root         (0) root         (0)      305 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/requires.txt
--rwxrwxrwx   0 root         (0) root         (0)       12 2023-02-11 15:00:28.000000 pyinstaller-5.8.0/pyinstaller.egg-info/top_level.txt
--rwxrwxrwx   0 root         (0) root         (0)     1910 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/pyproject.toml
--rwxrwxrwx   0 root         (0) root         (0)     4021 2023-02-11 15:00:28.665392 pyinstaller-5.8.0/setup.cfg
--rwxrwxrwx   0 root         (0) root         (0)    10914 2023-02-11 14:47:39.000000 pyinstaller-5.8.0/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.777016 pyinstaller-5.9.0/
+-rwxrwxrwx   0 root         (0) root         (0)      339 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.dockerignore
+-rwxrwxrwx   0 root         (0) root         (0)      230 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.editorconfig
+-rwxrwxrwx   0 root         (0) root         (0)      853 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/.gitattributes
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.285061 pyinstaller-5.9.0/.github/
+-rwxrwxrwx   0 root         (0) root         (0)      102 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/.github/CONTRIBUTING.md
+-rwxrwxrwx   0 root         (0) root         (0)       17 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.github/FUNDING.yml
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.286994 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/
+-rwxrwxrwx   0 root         (0) root         (0)     5689 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/antivirus.md
+-rwxrwxrwx   0 root         (0) root         (0)      286 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/blank.md
+-rwxrwxrwx   0 root         (0) root         (0)     2763 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/bug_report.md
+-rwxrwxrwx   0 root         (0) root         (0)      404 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/config.yml
+-rwxrwxrwx   0 root         (0) root         (0)     1016 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/ISSUE_TEMPLATE/feature_request.md
+-rwxrwxrwx   0 root         (0) root         (0)      198 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/.github/SECURITY.md
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.289684 pyinstaller-5.9.0/.github/workflows/
+-rwxrwxrwx   0 root         (0) root         (0)      387 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/workflows/cancel.yml
+-rwxrwxrwx   0 root         (0) root         (0)     7080 2023-02-23 22:17:16.000000 pyinstaller-5.9.0/.github/workflows/ci.yml
+-rwxrwxrwx   0 root         (0) root         (0)      978 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/workflows/lint.yml
+-rwxrwxrwx   0 root         (0) root         (0)      391 2023-02-19 13:09:11.000000 pyinstaller-5.9.0/.github/workflows/lock-threads.yml
+-rwxrwxrwx   0 root         (0) root         (0)      463 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/workflows/validate-new-news.yml
+-rwxrwxrwx   0 root         (0) root         (0)      679 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.github/workflows/wheel-builder.yml
+-rwxrwxrwx   0 root         (0) root         (0)     2077 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/.gitignore
+-rwxrwxrwx   0 root         (0) root         (0)     1125 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/.pylintrc
+-rwxrwxrwx   0 root         (0) root         (0)      426 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/.pyup.yml
+-rwxrwxrwx   0 root         (0) root         (0)      237 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.readthedocs.yml
+-rwxrwxrwx   0 root         (0) root         (0)      438 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/.yapfignore
+-rwxrwxrwx   0 root         (0) root         (0)    32138 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/COPYING.txt
+-rwxrwxrwx   0 root         (0) root         (0)      846 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/MANIFEST.in
+-rwxrwxrwx   0 root         (0) root         (0)     7872 2023-03-13 20:35:17.777223 pyinstaller-5.9.0/PKG-INFO
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.292441 pyinstaller-5.9.0/PyInstaller/
+-rwxrwxrwx   0 root         (0) root         (0)     2997 2023-03-13 20:05:20.000000 pyinstaller-5.9.0/PyInstaller/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     7103 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/__main__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1821 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/_recursion_too_deep_message.py
+-rwxrwxrwx   0 root         (0) root         (0)     3911 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/_shared_with_waf.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.293379 pyinstaller-5.9.0/PyInstaller/archive/
+-rwxrwxrwx   0 root         (0) root         (0)       23 2023-02-23 22:46:11.000000 pyinstaller-5.9.0/PyInstaller/archive/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1730 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/archive/pyz_crypto.py
+-rwxrwxrwx   0 root         (0) root         (0)     8186 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/archive/readers.py
+-rwxrwxrwx   0 root         (0) root         (0)    23757 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/archive/writers.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.260102 pyinstaller-5.9.0/PyInstaller/bootloader/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.296741 pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/
+-rwxrwxrwx   0 root         (0) root         (0)   189104 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/run
+-rwxrwxrwx   0 root         (0) root         (0)   189096 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/run_d
+-rwxrwxrwx   0 root         (0) root         (0)   191896 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/runw
+-rwxrwxrwx   0 root         (0) root         (0)   241192 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/runw_d
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.301354 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/
+-rwxrwxrwx   0 root         (0) root         (0)   219648 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/run.exe
+-rwxrwxrwx   0 root         (0) root         (0)   224256 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/run_d.exe
+-rwxrwxrwx   0 root         (0) root         (0)   220672 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/runw.exe
+-rwxrwxrwx   0 root         (0) root         (0)   225280 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/runw_d.exe
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.306313 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/
+-rwxrwxrwx   0 root         (0) root         (0)   258048 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/run.exe
+-rwxrwxrwx   0 root         (0) root         (0)   263168 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/run_d.exe
+-rwxrwxrwx   0 root         (0) root         (0)   258560 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/runw.exe
+-rwxrwxrwx   0 root         (0) root         (0)   264192 2023-02-11 14:56:01.000000 pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/runw_d.exe
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.309405 pyinstaller-5.9.0/PyInstaller/bootloader/images/
+-rwxrwxrwx   0 root         (0) root         (0)   106001 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-console.icns
+-rwxrwxrwx   0 root         (0) root         (0)    59521 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-console.ico
+-rwxrwxrwx   0 root         (0) root         (0)   110199 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-windowed.icns
+-rwxrwxrwx   0 root         (0) root         (0)    60690 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-windowed.ico
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.313182 pyinstaller-5.9.0/PyInstaller/building/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:11.000000 pyinstaller-5.9.0/PyInstaller/building/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)    54255 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/api.py
+-rwxrwxrwx   0 root         (0) root         (0)    43629 2023-02-23 22:17:16.000000 pyinstaller-5.9.0/PyInstaller/building/build_main.py
+-rwxrwxrwx   0 root         (0) root         (0)    10868 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/datastruct.py
+-rwxrwxrwx   0 root         (0) root         (0)     3574 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/icon.py
+-rwxrwxrwx   0 root         (0) root         (0)    32485 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/makespec.py
+-rwxrwxrwx   0 root         (0) root         (0)    13060 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/osx.py
+-rwxrwxrwx   0 root         (0) root         (0)    22976 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/splash.py
+-rwxrwxrwx   0 root         (0) root         (0)     7453 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/splash_templates.py
+-rwxrwxrwx   0 root         (0) root         (0)     3642 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/templates.py
+-rwxrwxrwx   0 root         (0) root         (0)     6493 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/toc_conversion.py
+-rwxrwxrwx   0 root         (0) root         (0)    32929 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/building/utils.py
+-rwxrwxrwx   0 root         (0) root         (0)    32104 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/compat.py
+-rwxrwxrwx   0 root         (0) root         (0)     1727 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/config.py
+-rwxrwxrwx   0 root         (0) root         (0)     3343 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/configure.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.315824 pyinstaller-5.9.0/PyInstaller/depend/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:11.000000 pyinstaller-5.9.0/PyInstaller/depend/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)    43344 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/depend/analysis.py
+-rwxrwxrwx   0 root         (0) root         (0)    44289 2023-03-12 23:23:33.000000 pyinstaller-5.9.0/PyInstaller/depend/bindepend.py
+-rwxrwxrwx   0 root         (0) root         (0)    12576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/depend/bytecode.py
+-rwxrwxrwx   0 root         (0) root         (0)    15844 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/depend/dylib.py
+-rwxrwxrwx   0 root         (0) root         (0)    25446 2023-03-11 20:25:03.000000 pyinstaller-5.9.0/PyInstaller/depend/imphook.py
+-rwxrwxrwx   0 root         (0) root         (0)    20149 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/depend/imphookapi.py
+-rwxrwxrwx   0 root         (0) root         (0)    17332 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/depend/utils.py
+-rwxrwxrwx   0 root         (0) root         (0)     1101 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/exceptions.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.316132 pyinstaller-5.9.0/PyInstaller/fake-modules/
+-rwxrwxrwx   0 root         (0) root         (0)     8555 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/fake-modules/pyi_splash.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.400560 pyinstaller-5.9.0/PyInstaller/hooks/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/hooks/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      845 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.Image.py
+-rwxrwxrwx   0 root         (0) root         (0)      589 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.ImageFilter.py
+-rwxrwxrwx   0 root         (0) root         (0)      773 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.SpiderImagePlugin.py
+-rwxrwxrwx   0 root         (0) root         (0)     1100 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QAxContainer.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qsci.py
+-rwxrwxrwx   0 root         (0) root         (0)     1274 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DAnimation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DInput.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DLogic.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DRender.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtBluetooth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtChart.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDBus.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDataVisualization.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDesigner.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtGui.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtHelp.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtLocation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMacExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMultimedia.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMultimediaWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNetwork.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNetworkAuth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNfc.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtOpenGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPositioning.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPrintSupport.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPurchasing.py
+-rwxrwxrwx   0 root         (0) root         (0)      764 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuick3D.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuickWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtRemoteObjects.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtScript.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSensors.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSerialPort.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSql.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSvg.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtTest.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtTextToSpeech.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebChannel.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngine.py
+-rwxrwxrwx   0 root         (0) root         (0)      995 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebKit.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebKitWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebSockets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWinExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtX11Extras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtXml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtXmlPatterns.py
+-rwxrwxrwx   0 root         (0) root         (0)     1027 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.py
+-rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.uic.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QAxContainer.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qsci.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DAnimation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DInput.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DLogic.py
+-rwxrwxrwx   0 root         (0) root         (0)      670 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DRender.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtBluetooth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtCharts.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDBus.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDataVisualization.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDesigner.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtGui.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtHelp.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtMultimedia.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtMultimediaWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNetwork.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNetworkAuth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNfc.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtOpenGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtOpenGLWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPdf.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPdfWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPositioning.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPrintSupport.py
+-rwxrwxrwx   0 root         (0) root         (0)      764 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuick3D.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuickWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtRemoteObjects.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSensors.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSerialPort.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSql.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSvg.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSvgWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtTest.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebChannel.py
+-rwxrwxrwx   0 root         (0) root         (0)     1351 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebSockets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtXml.py
+-rwxrwxrwx   0 root         (0) root         (0)      870 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.py
+-rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.uic.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DAnimation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DInput.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DLogic.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DRender.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtAxContainer.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtCharts.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtConcurrent.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtDataVisualization.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtGui.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtHelp.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtLocation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMacExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      979 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMultimedia.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMultimediaWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      714 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtNetwork.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtOpenGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtOpenGLFunctions.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtPositioning.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtPrintSupport.py
+-rwxrwxrwx   0 root         (0) root         (0)      804 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuickControls2.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuickWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtRemoteObjects.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScript.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScriptTools.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScxml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSensors.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSerialPort.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSql.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSvg.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtTest.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtTextToSpeech.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtUiTools.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebChannel.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngine.py
+-rwxrwxrwx   0 root         (0) root         (0)     1003 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngineCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngineWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebKit.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebKitWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebSockets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWinExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtX11Extras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtXml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtXmlPatterns.py
+-rwxrwxrwx   0 root         (0) root         (0)      972 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qwt5.py
+-rwxrwxrwx   0 root         (0) root         (0)      984 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DAnimation.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DExtras.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DInput.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DLogic.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DRender.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtAxContainer.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtBluetooth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtCharts.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtConcurrent.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDBus.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDataVisualization.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDesigner.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtGui.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtHelp.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtHttpServer.py
+-rwxrwxrwx   0 root         (0) root         (0)      981 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtMultimedia.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtMultimediaWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      714 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNetwork.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNetworkAuth.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNfc.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtOpenGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtOpenGLWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPdf.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPdfWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPositioning.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPrintSupport.py
+-rwxrwxrwx   0 root         (0) root         (0)      768 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuick3D.py
+-rwxrwxrwx   0 root         (0) root         (0)      671 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuickControls2.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuickWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtRemoteObjects.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtScxml.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSensors.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSerialPort.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSpatialAudio.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSql.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtStateMachine.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSvg.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSvgWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtTest.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtUiTools.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebChannel.py
+-rwxrwxrwx   0 root         (0) root         (0)     1410 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineCore.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineQuick.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebSockets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWidgets.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtXml.py
+-rwxrwxrwx   0 root         (0) root         (0)     1126 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.py
+-rwxrwxrwx   0 root         (0) root         (0)     1327 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-_tkinter.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-babel.py
+-rwxrwxrwx   0 root         (0) root         (0)      577 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-difflib.py
+-rwxrwxrwx   0 root         (0) root         (0)     1863 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-distutils.py
+-rwxrwxrwx   0 root         (0) root         (0)      661 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-distutils.util.py
+-rwxrwxrwx   0 root         (0) root         (0)      635 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.contrib.sessions.py
+-rwxrwxrwx   0 root         (0) root         (0)      629 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.cache.py
+-rwxrwxrwx   0 root         (0) root         (0)     1069 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.mail.py
+-rwxrwxrwx   0 root         (0) root         (0)      942 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.management.py
+-rwxrwxrwx   0 root         (0) root         (0)      611 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.mysql.base.py
+-rwxrwxrwx   0 root         (0) root         (0)      563 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.oracle.base.py
+-rwxrwxrwx   0 root         (0) root         (0)      983 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.py
+-rwxrwxrwx   0 root         (0) root         (0)     3922 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.py
+-rwxrwxrwx   0 root         (0) root         (0)      626 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-django.template.loaders.py
+-rwxrwxrwx   0 root         (0) root         (0)      612 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-encodings.py
+-rwxrwxrwx   0 root         (0) root         (0)     1011 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gevent.py
+-rwxrwxrwx   0 root         (0) root         (0)      552 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.py
+-rwxrwxrwx   0 root         (0) root         (0)      698 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Adw.py
+-rwxrwxrwx   0 root         (0) root         (0)     1084 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Atk.py
+-rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Champlain.py
+-rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Clutter.py
+-rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GIRepository.py
+-rwxrwxrwx   0 root         (0) root         (0)     1490 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GLib.py
+-rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GModule.py
+-rwxrwxrwx   0 root         (0) root         (0)      909 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GObject.py
+-rwxrwxrwx   0 root         (0) root         (0)     1393 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gdk.py
+-rwxrwxrwx   0 root         (0) root         (0)     5846 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GdkPixbuf.py
+-rwxrwxrwx   0 root         (0) root         (0)     2605 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gio.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Graphene.py
+-rwxrwxrwx   0 root         (0) root         (0)      700 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gsk.py
+-rwxrwxrwx   0 root         (0) root         (0)     3461 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gst.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstAllocators.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstApp.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstAudio.py
+-rwxrwxrwx   0 root         (0) root         (0)      708 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstBadAudio.py
+-rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstBase.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstCheck.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstCodecs.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstController.py
+-rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLEGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLWayland.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLX11.py
+-rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstInsertBin.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstMpegts.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstNet.py
+-rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPbutils.py
+-rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPlay.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPlayer.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtp.py
+-rwxrwxrwx   0 root         (0) root         (0)      704 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtsp.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtspServer.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstSdp.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstTag.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstTranscoder.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVideo.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkan.py
+-rwxrwxrwx   0 root         (0) root         (0)      713 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkanWayland.py
+-rwxrwxrwx   0 root         (0) root         (0)      709 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkanXCB.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstWebRTC.py
+-rwxrwxrwx   0 root         (0) root         (0)     2150 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gtk.py
+-rwxrwxrwx   0 root         (0) root         (0)      710 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkChamplain.py
+-rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkClutter.py
+-rwxrwxrwx   0 root         (0) root         (0)     1297 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkSource.py
+-rwxrwxrwx   0 root         (0) root         (0)      781 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkosxApplication.py
+-rwxrwxrwx   0 root         (0) root         (0)      705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.HarfBuzz.py
+-rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Pango.py
+-rwxrwxrwx   0 root         (0) root         (0)      707 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.PangoCairo.py
+-rwxrwxrwx   0 root         (0) root         (0)      702 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.cairo.py
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.freetype2.py
+-rwxrwxrwx   0 root         (0) root         (0)      701 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.xlib.py
+-rwxrwxrwx   0 root         (0) root         (0)      578 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-heapq.py
+-rwxrwxrwx   0 root         (0) root         (0)      602 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-idlelib.py
+-rwxrwxrwx   0 root         (0) root         (0)     1350 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-importlib_metadata.py
+-rwxrwxrwx   0 root         (0) root         (0)     1021 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-importlib_resources.py
+-rwxrwxrwx   0 root         (0) root         (0)      888 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-keyring.py
+-rwxrwxrwx   0 root         (0) root         (0)     1130 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-kivy.py
+-rwxrwxrwx   0 root         (0) root         (0)      653 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-lib2to3.py
+-rwxrwxrwx   0 root         (0) root         (0)     9232 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.backends.py
+-rwxrwxrwx   0 root         (0) root         (0)      683 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.numerix.py
+-rwxrwxrwx   0 root         (0) root         (0)      701 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.py
+-rwxrwxrwx   0 root         (0) root         (0)      791 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-multiprocessing.util.py
+-rwxrwxrwx   0 root         (0) root         (0)     2335 2023-03-08 20:43:10.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-numpy.py
+-rwxrwxrwx   0 root         (0) root         (0)      577 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-packaging.py
+-rwxrwxrwx   0 root         (0) root         (0)      751 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.io.formats.style.py
+-rwxrwxrwx   0 root         (0) root         (0)      944 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.plotting.py
+-rwxrwxrwx   0 root         (0) root         (0)      959 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.py
+-rwxrwxrwx   0 root         (0) root         (0)      589 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pickle.py
+-rwxrwxrwx   0 root         (0) root         (0)     2960 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pkg_resources.py
+-rwxrwxrwx   0 root         (0) root         (0)      713 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-platform.py
+-rwxrwxrwx   0 root         (0) root         (0)     1184 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pygments.py
+-rwxrwxrwx   0 root         (0) root         (0)      734 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pytz.py
+-rwxrwxrwx   0 root         (0) root         (0)      603 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-pytzdata.py
+-rwxrwxrwx   0 root         (0) root         (0)      792 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-qtawesome.py
+-rwxrwxrwx   0 root         (0) root         (0)      930 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scapy.layers.all.py
+-rwxrwxrwx   0 root         (0) root         (0)      655 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.io.matlab.py
+-rwxrwxrwx   0 root         (0) root         (0)      633 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.linalg.py
+-rwxrwxrwx   0 root         (0) root         (0)     1608 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.py
+-rwxrwxrwx   0 root         (0) root         (0)      611 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.sparse.csgraph.py
+-rwxrwxrwx   0 root         (0) root         (0)      797 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.spatial.transform.rotation.py
+-rwxrwxrwx   0 root         (0) root         (0)     1317 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.special._ellip_harm_2.py
+-rwxrwxrwx   0 root         (0) root         (0)      696 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.special._ufuncs.py
+-rwxrwxrwx   0 root         (0) root         (0)      660 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.stats._stats.py
+-rwxrwxrwx   0 root         (0) root         (0)      819 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-scrapy.py
+-rwxrwxrwx   0 root         (0) root         (0)      599 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-setuptools.msvc.py
+-rwxrwxrwx   0 root         (0) root         (0)     2153 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-setuptools.py
+-rwxrwxrwx   0 root         (0) root         (0)      603 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-shelve.py
+-rwxrwxrwx   0 root         (0) root         (0)     1998 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-sphinx.py
+-rwxrwxrwx   0 root         (0) root         (0)     3165 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-sqlalchemy.py
+-rwxrwxrwx   0 root         (0) root         (0)      813 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-sqlite3.py
+-rwxrwxrwx   0 root         (0) root         (0)     1558 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-sysconfig.py
+-rwxrwxrwx   0 root         (0) root         (0)      602 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-wcwidth.py
+-rwxrwxrwx   0 root         (0) root         (0)      993 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-win32ctypes.core.py
+-rwxrwxrwx   0 root         (0) root         (0)      569 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.dom.domreg.py
+-rwxrwxrwx   0 root         (0) root         (0)      615 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.etree.cElementTree.py
+-rwxrwxrwx   0 root         (0) root         (0)      569 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.py
+-rwxrwxrwx   0 root         (0) root         (0)      539 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/hook-zope.interface.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.401570 pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      696 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-PyQt5.uic.port_v2.py
+-rwxrwxrwx   0 root         (0) root         (0)     2347 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-distutils.py
+-rwxrwxrwx   0 root         (0) root         (0)     1412 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-pyi_splash.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.416773 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1955 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Adw.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Atk.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Champlain.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Clutter.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GIRepository.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GLib.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GModule.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GObject.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gdk.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GdkPixbuf.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gio.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Graphene.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gsk.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gst.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAllocators.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstApp.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAudio.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBadAudio.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBase.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCheck.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCodecs.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstController.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLEGL.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLWayland.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLX11.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstInsertBin.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstMpegts.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstNet.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPbutils.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlay.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlayer.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtp.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtsp.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtspServer.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstSdp.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTag.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTranscoder.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVideo.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkan.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanWayland.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanXCB.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstWebRTC.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gtk.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkChamplain.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkClutter.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkSource.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkosxApplication.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.HarfBuzz.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Pango.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.PangoCairo.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.cairo.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.freetype2.py
+-rwxrwxrwx   0 root         (0) root         (0)      783 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.xlib.py
+-rwxrwxrwx   0 root         (0) root         (0)     1477 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-setuptools.extern.six.moves.py
+-rwxrwxrwx   0 root         (0) root         (0)     3731 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-six.moves.py
+-rwxrwxrwx   0 root         (0) root         (0)     1240 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-urllib3.packages.six.moves.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.423245 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1136 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth__tkinter.py
+-rwxrwxrwx   0 root         (0) root         (0)     1013 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_django.py
+-rwxrwxrwx   0 root         (0) root         (0)     1309 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gdkpixbuf.py
+-rwxrwxrwx   0 root         (0) root         (0)      568 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gi.py
+-rwxrwxrwx   0 root         (0) root         (0)      567 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gio.py
+-rwxrwxrwx   0 root         (0) root         (0)     1324 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_glib.py
+-rwxrwxrwx   0 root         (0) root         (0)     1079 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gstreamer.py
+-rwxrwxrwx   0 root         (0) root         (0)      802 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gtk.py
+-rwxrwxrwx   0 root         (0) root         (0)     1904 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_inspect.py
+-rwxrwxrwx   0 root         (0) root         (0)      665 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_kivy.py
+-rwxrwxrwx   0 root         (0) root         (0)     1486 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_mplconfig.py
+-rwxrwxrwx   0 root         (0) root         (0)     3991 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_multiprocessing.py
+-rwxrwxrwx   0 root         (0) root         (0)     8550 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pkgres.py
+-rwxrwxrwx   0 root         (0) root         (0)     4278 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pkgutil.py
+-rwxrwxrwx   0 root         (0) root         (0)     1238 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5.py
+-rwxrwxrwx   0 root         (0) root         (0)     1380 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5webengine.py
+-rwxrwxrwx   0 root         (0) root         (0)     1317 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6.py
+-rwxrwxrwx   0 root         (0) root         (0)     1697 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6webengine.py
+-rwxrwxrwx   0 root         (0) root         (0)     1293 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2.py
+-rwxrwxrwx   0 root         (0) root         (0)     1093 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2webengine.py
+-rwxrwxrwx   0 root         (0) root         (0)     1293 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6.py
+-rwxrwxrwx   0 root         (0) root         (0)     1484 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6webengine.py
+-rwxrwxrwx   0 root         (0) root         (0)     1365 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_setuptools.py
+-rwxrwxrwx   0 root         (0) root         (0)     2204 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_win32comgenpy.py
+-rwxrwxrwx   0 root         (0) root         (0)     1252 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/hooks/rthooks.dat
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.423987 pyinstaller-5.9.0/PyInstaller/isolated/
+-rwxrwxrwx   0 root         (0) root         (0)     1505 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/isolated/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     3757 2023-02-25 00:58:06.000000 pyinstaller-5.9.0/PyInstaller/isolated/_child.py
+-rwxrwxrwx   0 root         (0) root         (0)    16717 2023-02-25 00:58:06.000000 pyinstaller-5.9.0/PyInstaller/isolated/_parent.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.424555 pyinstaller-5.9.0/PyInstaller/lib/
+-rwxrwxrwx   0 root         (0) root         (0)     1382 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/README.rst
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.426908 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     2742 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/__main__.py
+-rwxrwxrwx   0 root         (0) root         (0)      519 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/_compat.py
+-rwxrwxrwx   0 root         (0) root         (0)    10651 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/find_modules.py
+-rwxrwxrwx   0 root         (0) root         (0)   139611 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/modulegraph.py
+-rwxrwxrwx   0 root         (0) root         (0)     4350 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/util.py
+-rwxrwxrwx   0 root         (0) root         (0)     9962 2023-03-12 23:23:33.000000 pyinstaller-5.9.0/PyInstaller/lib/modulegraph/zipio.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.428564 pyinstaller-5.9.0/PyInstaller/loader/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/loader/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     3450 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/loader/pyiboot01_bootstrap.py
+-rwxrwxrwx   0 root         (0) root         (0)    10822 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/loader/pyimod01_archive.py
+-rwxrwxrwx   0 root         (0) root         (0)    22141 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/loader/pyimod02_importers.py
+-rwxrwxrwx   0 root         (0) root         (0)     4915 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/loader/pyimod03_ctypes.py
+-rwxrwxrwx   0 root         (0) root         (0)     2440 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/loader/pyimod04_pywin32.py
+-rwxrwxrwx   0 root         (0) root         (0)     2058 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/log.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.430981 pyinstaller-5.9.0/PyInstaller/utils/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/utils/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      451 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/PyInstaller/utils/_gitrevision.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.432550 pyinstaller-5.9.0/PyInstaller/utils/cliutils/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     7771 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/archive_viewer.py
+-rwxrwxrwx   0 root         (0) root         (0)     1742 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/bindepend.py
+-rwxrwxrwx   0 root         (0) root         (0)     1714 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/grab_version.py
+-rwxrwxrwx   0 root         (0) root         (0)     1502 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/makespec.py
+-rwxrwxrwx   0 root         (0) root         (0)     1360 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/cliutils/set_version.py
+-rwxrwxrwx   0 root         (0) root         (0)    23530 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/conftest.py
+-rwxrwxrwx   0 root         (0) root         (0)     2014 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/git.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.434444 pyinstaller-5.9.0/PyInstaller/utils/hooks/
+-rwxrwxrwx   0 root         (0) root         (0)    54533 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)    14787 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/conda.py
+-rwxrwxrwx   0 root         (0) root         (0)     6095 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/django.py
+-rwxrwxrwx   0 root         (0) root         (0)    17070 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/gi.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.435114 pyinstaller-5.9.0/PyInstaller/utils/hooks/qt/
+-rwxrwxrwx   0 root         (0) root         (0)    45378 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/qt/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)    24612 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/qt/_modules_info.py
+-rwxrwxrwx   0 root         (0) root         (0)    10947 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/tcl_tk.py
+-rwxrwxrwx   0 root         (0) root         (0)     1569 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/hooks/win32.py
+-rwxrwxrwx   0 root         (0) root         (0)     7195 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/misc.py
+-rwxrwxrwx   0 root         (0) root         (0)    14989 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/osx.py
+-rwxrwxrwx   0 root         (0) root         (0)       87 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/PyInstaller/utils/pytest.ini
+-rwxrwxrwx   0 root         (0) root         (0)     2839 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/run_tests.py
+-rwxrwxrwx   0 root         (0) root         (0)     5766 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/tests.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.437021 pyinstaller-5.9.0/PyInstaller/utils/win32/
+-rwxrwxrwx   0 root         (0) root         (0)       23 2023-02-23 22:46:12.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     9151 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/icon.py
+-rwxrwxrwx   0 root         (0) root         (0)    20598 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/versioninfo.py
+-rwxrwxrwx   0 root         (0) root         (0)    44149 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/winmanifest.py
+-rwxrwxrwx   0 root         (0) root         (0)     9621 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/winresource.py
+-rwxrwxrwx   0 root         (0) root         (0)    12688 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/PyInstaller/utils/win32/winutils.py
+-rwxrwxrwx   0 root         (0) root         (0)     5554 2023-03-13 20:05:26.000000 pyinstaller-5.9.0/README.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2013 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/alpine.dockerfile
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.443221 pyinstaller-5.9.0/bootloader/
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/bootloader/.gitattributes
+-rwxrwxrwx   0 root         (0) root         (0)     2053 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/Dockerfile
+-rwxrwxrwx   0 root         (0) root         (0)     3924 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/Dockerfile.osxcross
+-rwxrwxrwx   0 root         (0) root         (0)     1038 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/README.txt
+-rwxrwxrwx   0 root         (0) root         (0)    15148 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/Vagrantfile
+-rwxrwxrwx   0 root         (0) root         (0)     1489 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/build.sh
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.451804 pyinstaller-5.9.0/bootloader/src/
+-rwxrwxrwx   0 root         (0) root         (0)     2619 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/main.c
+-rwxrwxrwx   0 root         (0) root         (0)      875 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/mkdtemp.h
+-rwxrwxrwx   0 root         (0) root         (0)    29474 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_apple_events.c
+-rwxrwxrwx   0 root         (0) root         (0)     1825 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_apple_events.h
+-rwxrwxrwx   0 root         (0) root         (0)    17949 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_archive.c
+-rwxrwxrwx   0 root         (0) root         (0)     5542 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_archive.h
+-rwxrwxrwx   0 root         (0) root         (0)    13273 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_exception_dialog.c
+-rwxrwxrwx   0 root         (0) root         (0)      822 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_exception_dialog.h
+-rwxrwxrwx   0 root         (0) root         (0)     7347 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_global.c
+-rwxrwxrwx   0 root         (0) root         (0)     8378 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_global.h
+-rwxrwxrwx   0 root         (0) root         (0)    23942 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_launch.c
+-rwxrwxrwx   0 root         (0) root         (0)     2316 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_launch.h
+-rwxrwxrwx   0 root         (0) root         (0)    15596 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_main.c
+-rwxrwxrwx   0 root         (0) root         (0)      564 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_main.h
+-rwxrwxrwx   0 root         (0) root         (0)    11094 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_path.c
+-rwxrwxrwx   0 root         (0) root         (0)     1465 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_path.h
+-rwxrwxrwx   0 root         (0) root         (0)     4850 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_python.c
+-rwxrwxrwx   0 root         (0) root         (0)     6457 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_python.h
+-rwxrwxrwx   0 root         (0) root         (0)    23303 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_pythonlib.c
+-rwxrwxrwx   0 root         (0) root         (0)     1125 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_pythonlib.h
+-rwxrwxrwx   0 root         (0) root         (0)    38074 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_splash.c
+-rwxrwxrwx   0 root         (0) root         (0)     6003 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_splash.h
+-rwxrwxrwx   0 root         (0) root         (0)     3386 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_splashlib.c
+-rwxrwxrwx   0 root         (0) root         (0)     4517 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_splashlib.h
+-rwxrwxrwx   0 root         (0) root         (0)    44952 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_utils.c
+-rwxrwxrwx   0 root         (0) root         (0)     2442 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_utils.h
+-rwxrwxrwx   0 root         (0) root         (0)    16726 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_win32_utils.c
+-rwxrwxrwx   0 root         (0) root         (0)     1226 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/src/pyi_win32_utils.h
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.452991 pyinstaller-5.9.0/bootloader/tests/
+-rwxrwxrwx   0 root         (0) root         (0)     3854 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/tests/test_launch.c
+-rwxrwxrwx   0 root         (0) root         (0)     7906 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/tests/test_path.c
+-rwxrwxrwx   0 root         (0) root         (0)     1770 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/tests/wscript
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.453271 pyinstaller-5.9.0/bootloader/tools/
+-rwxrwxrwx   0 root         (0) root         (0)     1818 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/tools/strip.py
+-rwxrwxrwx   0 root         (0) root         (0)    82527 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/bootloader/uncrustify.cfg
+-rwxrwxrwx   0 root         (0) root         (0)     1820 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/update-waf.sh
+-rwxrwxrwx   0 root         (0) root         (0)     1581 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waf
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.460565 pyinstaller-5.9.0/bootloader/waflib/
+-rwxrwxrwx   0 root         (0) root         (0)    30209 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Build.py
+-rwxrwxrwx   0 root         (0) root         (0)     5179 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/ConfigSet.py
+-rwxrwxrwx   0 root         (0) root         (0)    14831 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Configure.py
+-rwxrwxrwx   0 root         (0) root         (0)    14805 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Context.py
+-rwxrwxrwx   0 root         (0) root         (0)     1248 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Errors.py
+-rwxrwxrwx   0 root         (0) root         (0)     7207 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Logs.py
+-rwxrwxrwx   0 root         (0) root         (0)    15286 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Node.py
+-rwxrwxrwx   0 root         (0) root         (0)    11367 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Options.py
+-rwxrwxrwx   0 root         (0) root         (0)    13041 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Runner.py
+-rwxrwxrwx   0 root         (0) root         (0)    15382 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Scripting.py
+-rwxrwxrwx   0 root         (0) root         (0)    28095 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Task.py
+-rwxrwxrwx   0 root         (0) root         (0)    17611 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/TaskGen.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.488638 pyinstaller-5.9.0/bootloader/waflib/Tools/
+-rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      360 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/ar.py
+-rwxrwxrwx   0 root         (0) root         (0)     2090 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/asm.py
+-rwxrwxrwx   0 root         (0) root         (0)      933 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/bison.py
+-rwxrwxrwx   0 root         (0) root         (0)     1220 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c.py
+-rwxrwxrwx   0 root         (0) root         (0)     1893 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c_aliases.py
+-rwxrwxrwx   0 root         (0) root         (0)    31501 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c_config.py
+-rwxrwxrwx   0 root         (0) root         (0)     5203 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c_osx.py
+-rwxrwxrwx   0 root         (0) root         (0)    25054 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c_preproc.py
+-rwxrwxrwx   0 root         (0) root         (0)     5042 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/c_tests.py
+-rwxrwxrwx   0 root         (0) root         (0)    19729 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/ccroot.py
+-rwxrwxrwx   0 root         (0) root         (0)      594 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/clang.py
+-rwxrwxrwx   0 root         (0) root         (0)      606 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/clangxx.py
+-rwxrwxrwx   0 root         (0) root         (0)     2165 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_c.py
+-rwxrwxrwx   0 root         (0) root         (0)     2178 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_cxx.py
+-rwxrwxrwx   0 root         (0) root         (0)     1689 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_d.py
+-rwxrwxrwx   0 root         (0) root         (0)     2006 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_fc.py
+-rwxrwxrwx   0 root         (0) root         (0)     4439 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/cs.py
+-rwxrwxrwx   0 root         (0) root         (0)     1295 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/cxx.py
+-rwxrwxrwx   0 root         (0) root         (0)     2297 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/d.py
+-rwxrwxrwx   0 root         (0) root         (0)     1306 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/d_config.py
+-rwxrwxrwx   0 root         (0) root         (0)     4337 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/d_scan.py
+-rwxrwxrwx   0 root         (0) root         (0)     1227 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/dbus.py
+-rwxrwxrwx   0 root         (0) root         (0)     1643 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/dmd.py
+-rwxrwxrwx   0 root         (0) root         (0)     8302 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/errcheck.py
+-rwxrwxrwx   0 root         (0) root         (0)     5373 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/fc.py
+-rwxrwxrwx   0 root         (0) root         (0)    11313 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/fc_config.py
+-rwxrwxrwx   0 root         (0) root         (0)     2414 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/fc_scan.py
+-rwxrwxrwx   0 root         (0) root         (0)     1377 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/flex.py
+-rwxrwxrwx   0 root         (0) root         (0)     1599 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/g95.py
+-rwxrwxrwx   0 root         (0) root         (0)      385 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gas.py
+-rwxrwxrwx   0 root         (0) root         (0)     2985 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gcc.py
+-rwxrwxrwx   0 root         (0) root         (0)      998 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gdc.py
+-rwxrwxrwx   0 root         (0) root         (0)     2225 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gfortran.py
+-rwxrwxrwx   0 root         (0) root         (0)    12984 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/glib2.py
+-rwxrwxrwx   0 root         (0) root         (0)     3104 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gnu_dirs.py
+-rwxrwxrwx   0 root         (0) root         (0)     3054 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/gxx.py
+-rwxrwxrwx   0 root         (0) root         (0)      553 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/icc.py
+-rwxrwxrwx   0 root         (0) root         (0)      553 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/icpc.py
+-rwxrwxrwx   0 root         (0) root         (0)    11869 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/ifort.py
+-rwxrwxrwx   0 root         (0) root         (0)     4385 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/intltool.py
+-rwxrwxrwx   0 root         (0) root         (0)     1096 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/irixcc.py
+-rwxrwxrwx   0 root         (0) root         (0)    13193 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/javaw.py
+-rwxrwxrwx   0 root         (0) root         (0)     1068 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/ldc2.py
+-rwxrwxrwx   0 root         (0) root         (0)      641 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/lua.py
+-rwxrwxrwx   0 root         (0) root         (0)      801 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/md5_tstamp.py
+-rwxrwxrwx   0 root         (0) root         (0)    33374 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/msvc.py
+-rwxrwxrwx   0 root         (0) root         (0)      686 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/nasm.py
+-rwxrwxrwx   0 root         (0) root         (0)      305 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/nobuild.py
+-rwxrwxrwx   0 root         (0) root         (0)     3446 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/perl.py
+-rwxrwxrwx   0 root         (0) root         (0)    21797 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/python.py
+-rwxrwxrwx   0 root         (0) root         (0)    20211 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/qt5.py
+-rwxrwxrwx   0 root         (0) root         (0)     4384 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/ruby.py
+-rwxrwxrwx   0 root         (0) root         (0)     1324 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/suncc.py
+-rwxrwxrwx   0 root         (0) root         (0)     1358 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/suncxx.py
+-rwxrwxrwx   0 root         (0) root         (0)    13995 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/tex.py
+-rwxrwxrwx   0 root         (0) root         (0)    10164 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/vala.py
+-rwxrwxrwx   0 root         (0) root         (0)     7884 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/waf_unit_test.py
+-rwxrwxrwx   0 root         (0) root         (0)     2097 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/winres.py
+-rwxrwxrwx   0 root         (0) root         (0)     1204 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/xlc.py
+-rwxrwxrwx   0 root         (0) root         (0)     1247 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Tools/xlcxx.py
+-rwxrwxrwx   0 root         (0) root         (0)    19314 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/Utils.py
+-rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)    12079 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/ansiterm.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.489181 pyinstaller-5.9.0/bootloader/waflib/extras/
+-rwxrwxrwx   0 root         (0) root         (0)      120 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/extras/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1509 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/fixpy2.py
+-rwxrwxrwx   0 root         (0) root         (0)     1764 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/waflib/processor.py
+-rwxrwxrwx   0 root         (0) root         (0)    39431 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/wscript
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.501091 pyinstaller-5.9.0/bootloader/zlib/
+-rwxrwxrwx   0 root         (0) root         (0)      279 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/README
+-rwxrwxrwx   0 root         (0) root         (0)     5390 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/bootloader/zlib/adler32.c
+-rwxrwxrwx   0 root         (0) root         (0)    32250 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/crc32.c
+-rwxrwxrwx   0 root         (0) root         (0)   591749 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/zlib/crc32.h
+-rwxrwxrwx   0 root         (0) root         (0)     6843 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/zlib/gzguts.h
+-rwxrwxrwx   0 root         (0) root         (0)    12998 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/zlib/inffast.c
+-rwxrwxrwx   0 root         (0) root         (0)      438 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/bootloader/zlib/inffast.h
+-rwxrwxrwx   0 root         (0) root         (0)     6426 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/bootloader/zlib/inffixed.h
+-rwxrwxrwx   0 root         (0) root         (0)    56089 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/inflate.c
+-rwxrwxrwx   0 root         (0) root         (0)     6683 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/zlib/inflate.h
+-rwxrwxrwx   0 root         (0) root         (0)    12999 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/inftrees.c
+-rwxrwxrwx   0 root         (0) root         (0)     2927 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/bootloader/zlib/inftrees.h
+-rwxrwxrwx   0 root         (0) root         (0)    16625 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/zconf.h
+-rwxrwxrwx   0 root         (0) root         (0)    97323 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/zlib.h
+-rwxrwxrwx   0 root         (0) root         (0)     7340 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/zutil.c
+-rwxrwxrwx   0 root         (0) root         (0)     7297 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/bootloader/zlib/zutil.h
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.518725 pyinstaller-5.9.0/doc/
+-rwxrwxrwx   0 root         (0) root         (0)    10650 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/CHANGES-1.rst
+-rwxrwxrwx   0 root         (0) root         (0)     6193 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/CHANGES-2.rst
+-rwxrwxrwx   0 root         (0) root         (0)    51520 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/CHANGES-3.rst
+-rwxrwxrwx   0 root         (0) root         (0)    92231 2023-03-13 20:06:05.000000 pyinstaller-5.9.0/doc/CHANGES.rst
+-rwxrwxrwx   0 root         (0) root         (0)    18941 2023-03-13 20:05:26.000000 pyinstaller-5.9.0/doc/CREDITS.rst
+-rwxrwxrwx   0 root         (0) root         (0)     7447 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/Makefile
+-rwxrwxrwx   0 root         (0) root         (0)     4333 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/_common_definitions.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.521498 pyinstaller-5.9.0/doc/_static/
+-rwxrwxrwx   0 root         (0) root         (0)     3986 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/_static/CArchive.png
+-rwxrwxrwx   0 root         (0) root         (0)     3058 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/_static/SE_exe.png
+-rwxrwxrwx   0 root         (0) root         (0)     3521 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/_static/ZlibArchive.png
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.523572 pyinstaller-5.9.0/doc/_static/css/
+-rwxrwxrwx   0 root         (0) root         (0)      963 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/_static/css/pyinstaller.css
+-rwxrwxrwx   0 root         (0) root         (0)    16059 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/_static/pyinstaller-draft1a-100_trans.png
+-rwxrwxrwx   0 root         (0) root         (0)   217780 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/_static/pyinstaller-draft1a.ico
+-rwxrwxrwx   0 root         (0) root         (0)    22833 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/advanced-topics.rst
+-rwxrwxrwx   0 root         (0) root         (0)    19455 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/bootloader-building.rst
+-rwxrwxrwx   0 root         (0) root         (0)    14909 2023-02-23 22:17:10.000000 pyinstaller-5.9.0/doc/conf.py
+-rwxrwxrwx   0 root         (0) root         (0)     3322 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/contributing.rst
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.528646 pyinstaller-5.9.0/doc/development/
+-rwxrwxrwx   0 root         (0) root         (0)     1749 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/branch-model.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2755 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/development/changelog-entries.rst
+-rwxrwxrwx   0 root         (0) root         (0)     1091 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/development/coding-conventions.rst
+-rwxrwxrwx   0 root         (0) root         (0)     9608 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/commit-messages.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2681 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/documentation.rst
+-rwxrwxrwx   0 root         (0) root         (0)      843 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/development/git.rst
+-rwxrwxrwx   0 root         (0) root         (0)      415 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/index.rst
+-rwxrwxrwx   0 root         (0) root         (0)     3473 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/pull-requests.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2221 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/development/quickstart.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2100 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/development/testing.rst
+-rwxrwxrwx   0 root         (0) root         (0)     1253 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/development/venv.rst
+-rwxrwxrwx   0 root         (0) root         (0)    66741 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/feature-notes.rst
+-rwxrwxrwx   0 root         (0) root         (0)     4432 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/help2rst.py
+-rwxrwxrwx   0 root         (0) root         (0)    14701 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/hooks-config.rst
+-rwxrwxrwx   0 root         (0) root         (0)    24936 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/hooks.rst
+-rwxrwxrwx   0 root         (0) root         (0)     2250 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/index.rst
+-rwxrwxrwx   0 root         (0) root         (0)     4402 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/installation.rst
+-rwxrwxrwx   0 root         (0) root         (0)     1024 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/license.rst
+-rwxrwxrwx   0 root         (0) root         (0)     6994 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/make.bat
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.529597 pyinstaller-5.9.0/doc/man/
+-rwxrwxrwx   0 root         (0) root         (0)     1495 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/man/pyi-makespec.rst
+-rwxrwxrwx   0 root         (0) root         (0)     1663 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/man/pyinstaller.rst
+-rwxrwxrwx   0 root         (0) root         (0)      105 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/doc/man-pages.rst
+-rwxrwxrwx   0 root         (0) root         (0)    11898 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/operating-mode.rst
+-rwxrwxrwx   0 root         (0) root         (0)    12702 2023-03-13 20:05:25.000000 pyinstaller-5.9.0/doc/pyi-makespec.1
+-rwxrwxrwx   0 root         (0) root         (0)    13690 2023-03-13 20:05:25.000000 pyinstaller-5.9.0/doc/pyinstaller.1
+-rwxrwxrwx   0 root         (0) root         (0)     2004 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/requirements.rst
+-rwxrwxrwx   0 root         (0) root         (0)      696 2023-02-23 22:17:10.000000 pyinstaller-5.9.0/doc/requirements.txt
+-rwxrwxrwx   0 root         (0) root         (0)     9138 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/doc/runtime-information.rst
+-rwxrwxrwx   0 root         (0) root         (0)    25733 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/spec-files.rst
+-rwxrwxrwx   0 root         (0) root         (0)    28823 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/doc/usage.rst
+-rwxrwxrwx   0 root         (0) root         (0)    14242 2023-02-23 22:17:10.000000 pyinstaller-5.9.0/doc/when-things-go-wrong.rst
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.535089 pyinstaller-5.9.0/icons/
+-rwxrwxrwx   0 root         (0) root         (0)   266950 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/icons/github_logo.png
+-rwxrwxrwx   0 root         (0) root         (0)   339276 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/icons/icon-console.svg
+-rwxrwxrwx   0 root         (0) root         (0)   339293 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/icons/icon-windowed.svg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.538264 pyinstaller-5.9.0/news/
+-rwxrwxrwx   0 root         (0) root         (0)       13 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/news/.gitignore
+-rwxrwxrwx   0 root         (0) root         (0)     2755 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/news/README.txt
+-rwxrwxrwx   0 root         (0) root         (0)     1065 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/news/_template.rst
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.540535 pyinstaller-5.9.0/pyinstaller.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)     7872 2023-03-13 20:35:16.000000 pyinstaller-5.9.0/pyinstaller.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)    76379 2023-03-13 20:35:17.000000 pyinstaller-5.9.0/pyinstaller.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        1 2023-03-13 20:35:16.000000 pyinstaller-5.9.0/pyinstaller.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)      376 2023-03-13 20:35:16.000000 pyinstaller-5.9.0/pyinstaller.egg-info/entry_points.txt
+-rwxrwxrwx   0 root         (0) root         (0)        1 2023-03-13 20:35:00.000000 pyinstaller-5.9.0/pyinstaller.egg-info/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)      305 2023-03-13 20:35:16.000000 pyinstaller-5.9.0/pyinstaller.egg-info/requires.txt
+-rwxrwxrwx   0 root         (0) root         (0)       12 2023-03-13 20:35:16.000000 pyinstaller-5.9.0/pyinstaller.egg-info/top_level.txt
+-rwxrwxrwx   0 root         (0) root         (0)     1910 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/pyproject.toml
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.541414 pyinstaller-5.9.0/release/
+-rwxrwxrwx   0 root         (0) root         (0)     2036 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/release/README.rst
+-rwxrwxrwx   0 root         (0) root         (0)      529 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/release/build-manylinux
+-rwxrwxrwx   0 root         (0) root         (0)     3928 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/release/release.fish
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.543698 pyinstaller-5.9.0/scripts/
+-rwxrwxrwx   0 root         (0) root         (0)      166 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/scripts/clean
+-rwxrwxrwx   0 root         (0) root         (0)       68 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/scripts/clean.bat
+-rwxrwxrwx   0 root         (0) root         (0)     1876 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/scripts/find-empty-hooks.py
+-rwxrwxrwx   0 root         (0) root         (0)     6327 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/scripts/update-copyright
+-rwxrwxrwx   0 root         (0) root         (0)      362 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/scripts/update-readme-versions.sh
+-rwxrwxrwx   0 root         (0) root         (0)     2048 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/scripts/verify-news-fragments.py
+-rwxrwxrwx   0 root         (0) root         (0)     4211 2023-03-13 20:35:17.778476 pyinstaller-5.9.0/setup.cfg
+-rwxrwxrwx   0 root         (0) root         (0)    10515 2023-02-23 22:17:16.000000 pyinstaller-5.9.0/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.545812 pyinstaller-5.9.0/tests/
+-rwxrwxrwx   0 root         (0) root         (0)     4442 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/README.md
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.560076 pyinstaller-5.9.0/tests/functional/
+-rwxrwxrwx   0 root         (0) root         (0)      214 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/README
+-rwxrwxrwx   0 root         (0) root         (0)       98 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/conftest.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.264051 pyinstaller-5.9.0/tests/functional/data/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.560511 pyinstaller-5.9.0/tests/functional/data/PIL_images/
+-rwxrwxrwx   0 root         (0) root         (0)     5758 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/PIL_images/tinysample.tiff
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.561032 pyinstaller-5.9.0/tests/functional/data/Qt_Ui_file/
+-rwxrwxrwx   0 root         (0) root         (0)      862 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/Qt_Ui_file/gui.ui
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.561557 pyinstaller-5.9.0/tests/functional/data/app_with_plugin/
+-rwxrwxrwx   0 root         (0) root         (0)      624 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/app_with_plugin/static_plugin.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.565162 pyinstaller-5.9.0/tests/functional/data/appimage/
+-rwxrwxrwx   0 root         (0) root         (0)   339293 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/appimage/AppIcon.svg
+-rwxrwxrwx   0 root         (0) root         (0)    20448 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/appimage/DirIcon.png
+-rwxrwxrwx   0 root         (0) root         (0)     1019 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/appimage/create.sh
+-rwxrwxrwx   0 root         (0) root         (0)      794 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/appimage/org.pyinstaller.appimage.test.appdata.xml
+-rwxrwxrwx   0 root         (0) root         (0)      253 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/appimage/org.pyinstaller.appimage.test.desktop
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.565444 pyinstaller-5.9.0/tests/functional/data/ctypes_dylib/
+-rwxrwxrwx   0 root         (0) root         (0)      695 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/ctypes_dylib/ctypes_dylib.c
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.567401 pyinstaller-5.9.0/tests/functional/data/django/
+-rwxrwxrwx   0 root         (0) root         (0)   131072 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/db.sqlite3
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.569157 pyinstaller-5.9.0/tests/functional/data/django/django_site/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/data/django/django_site/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      399 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/django_site/asgi.py
+-rwxrwxrwx   0 root         (0) root         (0)     3230 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/django_site/settings.py
+-rwxrwxrwx   0 root         (0) root         (0)      753 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/django_site/urls.py
+-rwxrwxrwx   0 root         (0) root         (0)      399 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/django_site/wsgi.py
+-rwxrwxrwx   0 root         (0) root         (0)      667 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/data/django/manage.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.569442 pyinstaller-5.9.0/tests/functional/data/invalid_icon/
+-rwxrwxrwx   0 root         (0) root         (0)      587 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/invalid_icon/pyi_icon.png
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.569720 pyinstaller-5.9.0/tests/functional/data/name_clash_with_entry_point/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.570265 pyinstaller-5.9.0/tests/functional/data/name_clash_with_entry_point/matching_name/
+-rwxrwxrwx   0 root         (0) root         (0)       56 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/name_clash_with_entry_point/matching_name/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       57 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/name_clash_with_entry_point/matching_name/submodule.py
+-rwxrwxrwx   0 root         (0) root         (0)       83 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/name_clash_with_entry_point/matching_name.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.570763 pyinstaller-5.9.0/tests/functional/data/requests/
+-rwxrwxrwx   0 root         (0) root         (0)      304 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/requests/openssl.conf
+-rwxrwxrwx   0 root         (0) root         (0)     5623 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/requests/server.pem
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.573095 pyinstaller-5.9.0/tests/functional/data/set_icon/
+-rwxrwxrwx   0 root         (0) root         (0)   108027 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/set_icon/pyi_icon.icns
+-rwxrwxrwx   0 root         (0) root         (0)    56493 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/set_icon/pyi_icon.ico
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.575867 pyinstaller-5.9.0/tests/functional/data/sphinx/
+-rwxrwxrwx   0 root         (0) root         (0)     9765 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/sphinx/conf.py
+-rwxrwxrwx   0 root         (0) root         (0)      511 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/data/sphinx/index.rst
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.576116 pyinstaller-5.9.0/tests/functional/data/splash/
+-rwxrwxrwx   0 root         (0) root         (0)    20448 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/data/splash/image.png
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.583259 pyinstaller-5.9.0/tests/functional/logs/
+-rwxrwxrwx   0 root         (0) root         (0)       72 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage1_B.toc
+-rwxrwxrwx   0 root         (0) root         (0)       45 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage2_B.toc
+-rwxrwxrwx   0 root         (0) root         (0)       84 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage3_B.toc
+-rwxrwxrwx   0 root         (0) root         (0)       45 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage4_B.toc
+-rwxrwxrwx   0 root         (0) root         (0)       45 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage5_B.toc
+-rwxrwxrwx   0 root         (0) root         (0)      152 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/multipackage5_C.toc
+-rwxrwxrwx   0 root         (0) root         (0)      389 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/pyi_import_relative.toc
+-rwxrwxrwx   0 root         (0) root         (0)       58 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_hiddenimport.toc
+-rwxrwxrwx   0 root         (0) root         (0)       78 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_keyring.toc
+-rwxrwxrwx   0 root         (0) root         (0)      123 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_multipackage1.toc
+-rwxrwxrwx   0 root         (0) root         (0)      155 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_multipackage2.toc
+-rwxrwxrwx   0 root         (0) root         (0)      123 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_multipackage3.toc
+-rwxrwxrwx   0 root         (0) root         (0)      155 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_multipackage4.toc
+-rwxrwxrwx   0 root         (0) root         (0)      155 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_multipackage5.toc
+-rwxrwxrwx   0 root         (0) root         (0)       86 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg1.toc
+-rwxrwxrwx   0 root         (0) root         (0)       54 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg1_bbb_zzz.toc
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg1_empty.toc
+-rwxrwxrwx   0 root         (0) root         (0)       86 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg2.toc
+-rwxrwxrwx   0 root         (0) root         (0)       81 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg3.toc
+-rwxrwxrwx   0 root         (0) root         (0)       34 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg3_aaa.toc
+-rwxrwxrwx   0 root         (0) root         (0)       54 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg3_bbb_zzz.toc
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg3_empty.toc
+-rwxrwxrwx   0 root         (0) root         (0)      149 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_nspkg_pep420.toc
+-rwxrwxrwx   0 root         (0) root         (0)      229 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_option_verbose.toc
+-rwxrwxrwx   0 root         (0) root         (0)       17 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_pil_FixTk.toc
+-rwxrwxrwx   0 root         (0) root         (0)       36 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_pil_PyQt5.toc
+-rwxrwxrwx   0 root         (0) root         (0)       47 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_pkg_without_hook_for_pkg.toc
+-rwxrwxrwx   0 root         (0) root         (0)       17 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_tkinter_FixTk.toc
+-rwxrwxrwx   0 root         (0) root         (0)       39 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/logs/test_zope_interface.toc
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.587046 pyinstaller-5.9.0/tests/functional/modules/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.587773 pyinstaller-5.9.0/tests/functional/modules/a_hidden_import/
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/a_hidden_import/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/a_hidden_import/submodule.py
+-rwxrwxrwx   0 root         (0) root         (0)      523 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/error_during_import2.py
+-rwxrwxrwx   0 root         (0) root         (0)      547 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/module_with_coding_utf8.py
+-rwxrwxrwx   0 root         (0) root         (0)      615 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/module_with_utf8_emoji.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.264463 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.264385 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path1/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.588048 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path1/package/
+-rwxrwxrwx   0 root         (0) root         (0)       21 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path1/package/sub2.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.264496 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.588320 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.588584 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/nspkg/
+-rwxrwxrwx   0 root         (0) root         (0)       26 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/nspkg/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       21 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/sub1.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.589110 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/subpackage/
+-rwxrwxrwx   0 root         (0) root         (0)       27 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/subpackage/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       31 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg-pep420/path2/package/subpackage/sub.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.589819 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.264864 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.591706 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/
+-rwxrwxrwx   0 root         (0) root         (0)      215 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      270 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/EGG-INFO/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.591949 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/nspkg1/
+-rwxrwxrwx   0 root         (0) root         (0)       64 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/nspkg1/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.592188 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/nspkg1/aaa/
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_aaa.egg/nspkg1/aaa/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1545 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_bbb.egg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.265099 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.593625 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/
+-rwxrwxrwx   0 root         (0) root         (0)      215 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      261 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/EGG-INFO/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.594110 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/nspkg1/
+-rwxrwxrwx   0 root         (0) root         (0)       64 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/nspkg1/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_ccc.egg/nspkg1/ccc.py
+-rwxrwxrwx   0 root         (0) root         (0)     1193 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg1-pkg/nspkg1_empty.egg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.595223 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.595471 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.595721 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/aaa/
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/aaa/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.265393 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/bbb/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.595976 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/bbb/zzz/
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/bbb/zzz/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2/ccc.py
+-rwxrwxrwx   0 root         (0) root         (0)      308 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2_aaa-nspkg.pth
+-rwxrwxrwx   0 root         (0) root         (0)      678 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2_bbb-nspkg.pth
+-rwxrwxrwx   0 root         (0) root         (0)      308 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2_ccc-nspkg.pth
+-rwxrwxrwx   0 root         (0) root         (0)      306 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg2-pkg/nspkg2_empty-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.596685 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.265642 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.598282 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/
+-rwxrwxrwx   0 root         (0) root         (0)      215 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      270 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/EGG-INFO/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.598527 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/nspkg3/
+-rwxrwxrwx   0 root         (0) root         (0)       76 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/nspkg3/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.598766 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/nspkg3/aaa/
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_aaa.egg/nspkg3/aaa/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1560 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_bbb.egg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.265876 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.600223 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/
+-rwxrwxrwx   0 root         (0) root         (0)      215 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      261 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)        8 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/EGG-INFO/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.600710 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/nspkg3/
+-rwxrwxrwx   0 root         (0) root         (0)       76 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/nspkg3/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       38 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_ccc.egg/nspkg3/ccc.py
+-rwxrwxrwx   0 root         (0) root         (0)     1202 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/nspkg3-pkg/nspkg3_empty.egg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.601208 pyinstaller-5.9.0/tests/functional/modules/pkg3/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pkg3/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       58 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pkg3/sample-data.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.601451 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.601693 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/sub1/
+-rwxrwxrwx   0 root         (0) root         (0)      281 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/sub1/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.601937 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/sub1/sub11/
+-rwxrwxrwx   0 root         (0) root         (0)       33 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pkg_without_hook_for_pkg/sub1/sub11/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      577 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_collect_submodules_mod.py
+-rwxrwxrwx   0 root         (0) root         (0)      230 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_dummy_module.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.266319 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.603145 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/
+-rwxrwxrwx   0 root         (0) root         (0)      225 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      239 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)       14 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/EGG-INFO/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.603400 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/unzipped_egg/
+-rwxrwxrwx   0 root         (0) root         (0)      678 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/unzipped_egg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.603799 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/unzipped_egg/data/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_unzipped.egg/unzipped_egg/data/datafile.txt
+-rwxrwxrwx   0 root         (0) root         (0)     1399 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_egg_zipped.egg
+-rwxrwxrwx   0 root         (0) root         (0)     1277 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_get_datadir.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.266534 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.604286 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/
+-rwxrwxrwx   0 root         (0) root         (0)      371 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/QtCore.py
+-rwxrwxrwx   0 root         (0) root         (0)       90 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.604565 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/
+-rwxrwxrwx   0 root         (0) root         (0)      120 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.605077 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v2/
+-rwxrwxrwx   0 root         (0) root         (0)      148 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      154 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v2/test.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.605591 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v3/
+-rwxrwxrwx   0 root         (0) root         (0)      148 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v3/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      155 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_import_pyqt_uic_port/PyQt5/uic/port_v3/test.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.266850 pyinstaller-5.9.0/tests/functional/modules/pyi_inspect_getmodule_from_stackframes/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.606090 pyinstaller-5.9.0/tests/functional/modules/pyi_inspect_getmodule_from_stackframes/helper_package/
+-rwxrwxrwx   0 root         (0) root         (0)      138 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_inspect_getmodule_from_stackframes/helper_package/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      290 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_inspect_getmodule_from_stackframes/helper_package/helper_module.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.266965 pyinstaller-5.9.0/tests/functional/modules/pyi_issue_4141/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.606332 pyinstaller-5.9.0/tests/functional/modules/pyi_issue_4141/app/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_issue_4141/app/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.267158 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.607326 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/hooks/
+-rwxrwxrwx   0 root         (0) root         (0)       65 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/hooks/hook-mymodule_feature1.py
+-rwxrwxrwx   0 root         (0) root         (0)      387 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/hooks/hook-mymodule_feature2.py
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/hooks/hook-mymodule_feature3.py
+-rwxrwxrwx   0 root         (0) root         (0)      155 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/hooks/hook-mymodule_main.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.267319 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.607575 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_feature1/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_feature1/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.607822 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_feature2/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_feature2/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.608299 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_main/
+-rwxrwxrwx   0 root         (0) root         (0)      619 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_main/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      210 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_module_exclusion/modules/mymodule_main/submodule_feature3.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.267495 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.608542 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/hooks/
+-rwxrwxrwx   0 root         (0) root         (0)      642 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/hooks/hook-pyi_pkgres_testpkg.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.608979 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.610032 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       89 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/a.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/b.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.610902 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/
+-rwxrwxrwx   0 root         (0) root         (0)       34 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/c.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/d.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.611687 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/
+-rwxrwxrwx   0 root         (0) root         (0)       32 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/entry1.txt
+-rwxrwxrwx   0 root         (0) root         (0)       34 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/entry2.md
+-rwxrwxrwx   0 root         (0) root         (0)       36 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/entry3.rst
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.611936 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/extra/
+-rwxrwxrwx   0 root         (0) root         (0)       66 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg1/data/extra/extra_entry1.json
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.612439 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/
+-rwxrwxrwx   0 root         (0) root         (0)       74 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/mod.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.612929 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/subsubpkg21/
+-rwxrwxrwx   0 root         (0) root         (0)       33 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/subsubpkg21/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg2/subsubpkg21/mod.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.613409 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg3/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg3/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       45 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/pyi_pkgres_testpkg/subpkg3/_datafile.json
+-rwxrwxrwx   0 root         (0) root         (0)     1128 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_pkg_resources_provider/package/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.613883 pyinstaller-5.9.0/tests/functional/modules/pyi_single_file_metadata/
+-rwxrwxrwx   0 root         (0) root         (0)      196 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_single_file_metadata/README
+-rwxrwxrwx   0 root         (0) root         (0)      290 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_single_file_metadata/my_test_package-1.0.egg-info
+-rwxrwxrwx   0 root         (0) root         (0)     1139 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_dynamic.py
+-rwxrwxrwx   0 root         (0) root         (0)     1311 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_gettemp.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.614124 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/
+-rwxrwxrwx   0 root         (0) root         (0)     1654 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.615114 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      558 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/aaa.py
+-rwxrwxrwx   0 root         (0) root         (0)      558 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/bbb.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.615640 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      817 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/ddd.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.616374 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/eee/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/eee/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      555 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/_vendor/ccc/eee/fff.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.616630 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/extern/
+-rwxrwxrwx   0 root         (0) root         (0)     4176 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_metapath1/extern/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.617085 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_missing_submod/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_missing_submod/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.617343 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_missing_submod/aaa/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_missing_submod/aaa/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.617893 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_nameclash/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_nameclash/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       59 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_nameclash/nameclash.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.618583 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_path/
+-rwxrwxrwx   0 root         (0) root         (0)      697 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_path/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.618840 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_path/a/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_path/a/b.py
+-rwxrwxrwx   0 root         (0) root         (0)      525 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_path/b.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.620047 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.621016 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/B/
+-rwxrwxrwx   0 root         (0) root         (0)     1030 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/B/C.py
+-rwxrwxrwx   0 root         (0) root         (0)      589 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/B/D.py
+-rwxrwxrwx   0 root         (0) root         (0)      538 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/B/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      538 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/E.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.621590 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/F/
+-rwxrwxrwx   0 root         (0) root         (0)      540 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/F/G.py
+-rwxrwxrwx   0 root         (0) root         (0)      585 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/F/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      536 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.622530 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/pyi_testmod_relimp/
+-rwxrwxrwx   0 root         (0) root         (0)      555 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/pyi_testmod_relimp/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1251 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/pyi_testmod_relimp/relimp2.py
+-rwxrwxrwx   0 root         (0) root         (0)      563 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/pyi_testmod_relimp/relimp3.py
+-rwxrwxrwx   0 root         (0) root         (0)      945 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/relimp1.py
+-rwxrwxrwx   0 root         (0) root         (0)      544 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp/relimp2.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.622778 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.623276 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/bar/
+-rwxrwxrwx   0 root         (0) root         (0)      556 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/bar/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.623528 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/bar/bar2/
+-rwxrwxrwx   0 root         (0) root         (0)      557 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/bar/bar2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      559 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp2/bar/baz.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.624030 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.624921 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/aa/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/aa/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      853 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/aa/a1.py
+-rwxrwxrwx   0 root         (0) root         (0)      547 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/aa/pyi_testmod_relimp3c.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.625402 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/pyi_testmod_relimp3b/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/pyi_testmod_relimp3b/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      540 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/pyi_testmod_relimp3b/b1.py
+-rwxrwxrwx   0 root         (0) root         (0)      525 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3a/pyi_testmod_relimp3c.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.625879 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3b/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3b/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      525 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3b/b1.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.626124 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3c/
+-rwxrwxrwx   0 root         (0) root         (0)      527 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_relimp3c/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.626617 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_from_aliased_pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_from_aliased_pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_from_aliased_pkg/submodule.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.627274 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_shadowed/
+-rwxrwxrwx   0 root         (0) root         (0)      963 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_shadowed/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      750 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_shadowed/submodule.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.628246 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_unshadowed/
+-rwxrwxrwx   0 root         (0) root         (0)     1605 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_unshadowed/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      756 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_submodule_global_unshadowed/submodule.py
+-rwxrwxrwx   0 root         (0) root         (0)      611 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/pyi_testmod_threading.py
+-rwxrwxrwx   0 root         (0) root         (0)      703 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/modules/resources_testmod.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.649436 pyinstaller-5.9.0/tests/functional/scripts/
+-rwxrwxrwx   0 root         (0) root         (0)      706 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/list_pytest11_entry_point.py
+-rwxrwxrwx   0 root         (0) root         (0)     1155 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pkg_resource_res_string.py
+-rwxrwxrwx   0 root         (0) root         (0)      914 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pkgutil_get_data.py
+-rwxrwxrwx   0 root         (0) root         (0)      896 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pkgutil_get_data__main__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1490 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_absolute_ld_library_path.py
+-rwxrwxrwx   0 root         (0) root         (0)     1221 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_absolute_python_path.py
+-rwxrwxrwx   0 root         (0) root         (0)     1948 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_app_with_plugin.py
+-rwxrwxrwx   0 root         (0) root         (0)      182 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_arbitrary_ext.foo
+-rwxrwxrwx   0 root         (0) root         (0)     1559 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_c_extension.py
+-rwxrwxrwx   0 root         (0) root         (0)      870 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_codecs.py
+-rwxrwxrwx   0 root         (0) root         (0)      634 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_filename.py
+-rwxrwxrwx   0 root         (0) root         (0)     3636 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_future.py
+-rwxrwxrwx   0 root         (0) root         (0)     1325 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_get_meipass_value.py
+-rwxrwxrwx   0 root         (0) root         (0)     1138 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_getfilesystemencoding.py
+-rwxrwxrwx   0 root         (0) root         (0)      531 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_helloworld.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.652786 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/
+-rwxrwxrwx   0 root         (0) root         (0)      890 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/hook-pkg_without_hook_for_pkg.sub1.py
+-rwxrwxrwx   0 root         (0) root         (0)      621 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/hook-pyi_collect_submodules_mod.py
+-rwxrwxrwx   0 root         (0) root         (0)      770 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/hook-pyi_testmod_metapath1.py
+-rwxrwxrwx   0 root         (0) root         (0)      821 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/hook-pyi_testmod_path.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.653285 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/pre_safe_import_module/
+-rwxrwxrwx   0 root         (0) root         (0)      524 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/pre_safe_import_module/hook-alias_name.py
+-rwxrwxrwx   0 root         (0) root         (0)     3310 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/wx_lib_pubsub.py
+-rwxrwxrwx   0 root         (0) root         (0)      984 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/wx_lib_pubsub_setuparg1.py
+-rwxrwxrwx   0 root         (0) root         (0)      978 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_hooks/wx_lib_pubsub_setupkwargs.py
+-rwxrwxrwx   0 root         (0) root         (0)     1266 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_import_pyqt5_uic_port.py
+-rwxrwxrwx   0 root         (0) root         (0)    14399 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_importlib_resources.py
+-rwxrwxrwx   0 root         (0) root         (0)     1191 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_interact_pyi_splash.py
+-rwxrwxrwx   0 root         (0) root         (0)     1329 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_issue_4141.py
+-rwxrwxrwx   0 root         (0) root         (0)      774 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_lib_PIL_img_conversion.py
+-rwxrwxrwx   0 root         (0) root         (0)     1031 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_lib_PyQt5-uic.py
+-rwxrwxrwx   0 root         (0) root         (0)     2840 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_lib_requests.py
+-rwxrwxrwx   0 root         (0) root         (0)     1401 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_lib_sphinx.py
+-rwxrwxrwx   0 root         (0) root         (0)     2161 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_lib_tkinter.py
+-rwxrwxrwx   0 root         (0) root         (0)     1058 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_load_dll_using_ctypes.py
+-rwxrwxrwx   0 root         (0) root         (0)     1334 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_module__file__attribute.py
+-rwxrwxrwx   0 root         (0) root         (0)     2556 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_module_attributes.py
+-rwxrwxrwx   0 root         (0) root         (0)     1383 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_module_reload.py
+-rwxrwxrwx   0 root         (0) root         (0)     1133 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_multiprocess.py
+-rwxrwxrwx   0 root         (0) root         (0)     1030 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_multiprocess_forking.py
+-rwxrwxrwx   0 root         (0) root         (0)     1055 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_multiprocess_pool.py
+-rwxrwxrwx   0 root         (0) root         (0)    11714 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_osx_aevent_logger_carbon.py
+-rwxrwxrwx   0 root         (0) root         (0)     1058 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_path_encoding.py
+-rwxrwxrwx   0 root         (0) root         (0)    14974 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_pkg_resources_provider.py
+-rwxrwxrwx   0 root         (0) root         (0)     1658 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_pkgutil_iter_modules.py
+-rwxrwxrwx   0 root         (0) root         (0)      933 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_python_home.py
+-rwxrwxrwx   0 root         (0) root         (0)     1868 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_site_module_disabled.py
+-rwxrwxrwx   0 root         (0) root         (0)     1131 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_stderr_encoding.py
+-rwxrwxrwx   0 root         (0) root         (0)     1130 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_stdout_encoding.py
+-rwxrwxrwx   0 root         (0) root         (0)     1462 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_symlink_basename_is_kept.py
+-rwxrwxrwx   0 root         (0) root         (0)     2283 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_threading_module2.py
+-rwxrwxrwx   0 root         (0) root         (0)     2232 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_unbuffered_output.py
+-rwxrwxrwx   0 root         (0) root         (0)     1697 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/scripts/pyi_win_py3_no_shortpathname.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.660220 pyinstaller-5.9.0/tests/functional/specs/
+-rwxrwxrwx   0 root         (0) root         (0)     1190 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/list_pytest11_entry_point.spec
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.663378 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.663622 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/extra-hooks/
+-rwxrwxrwx   0 root         (0) root         (0)      616 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/extra-hooks/hook-multipackage_test_pkg.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage1_B.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage2_B.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage3_B.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage4_B.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage5_B.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage5_C.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.664079 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage_test_pkg/
+-rwxrwxrwx   0 root         (0) root         (0)     1413 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage_test_pkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.664531 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage_test_pkg/data/
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/multipackage_test_pkg/data/secret.txt
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/test_multipackage1.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/test_multipackage2.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/test_multipackage3.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/test_multipackage4.py
+-rwxrwxrwx   0 root         (0) root         (0)      576 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/multipackage-scripts/test_multipackage5.py
+-rwxrwxrwx   0 root         (0) root         (0)     2415 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/pyi_osx_aevent_handling_carbon.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1611 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/pyi_osx_override_info_plist.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1170 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/pyi_unbuffered_output.spec
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.665677 pyinstaller-5.9.0/tests/functional/specs/several-scripts/
+-rwxrwxrwx   0 root         (0) root         (0)       94 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts/basemod.py
+-rwxrwxrwx   0 root         (0) root         (0)      366 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts/main-script1.py
+-rwxrwxrwx   0 root         (0) root         (0)      136 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts/main-script2.py
+-rwxrwxrwx   0 root         (0) root         (0)      198 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts/rt-hook-script.py
+-rwxrwxrwx   0 root         (0) root         (0)     1025 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts1.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1003 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/several-scripts2.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1029 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/spec-with-utf8.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1780 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/spec_with_splash.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1583 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/symlink_basename_is_kept.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1699 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/test_multipackage1.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1936 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/test_multipackage2.spec
+-rwxrwxrwx   0 root         (0) root         (0)     1962 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/test_multipackage3.spec
+-rwxrwxrwx   0 root         (0) root         (0)     2170 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/test_multipackage4.spec
+-rwxrwxrwx   0 root         (0) root         (0)     2734 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/specs/test_multipackage5.spec
+-rwxrwxrwx   0 root         (0) root         (0)    15751 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_apple_events.py
+-rwxrwxrwx   0 root         (0) root         (0)    27639 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_basic.py
+-rwxrwxrwx   0 root         (0) root         (0)     1480 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_cliutils.py
+-rwxrwxrwx   0 root         (0) root         (0)     1759 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_django.py
+-rwxrwxrwx   0 root         (0) root         (0)     1410 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hook_utilities.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.668498 pyinstaller-5.9.0/tests/functional/test_hooks/
+-rwxrwxrwx   0 root         (0) root         (0)     2423 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_gi.py
+-rwxrwxrwx   0 root         (0) root         (0)     4752 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_matplotlib.py
+-rwxrwxrwx   0 root         (0) root         (0)     4032 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_pil.py
+-rwxrwxrwx   0 root         (0) root         (0)      837 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_pkg_resources.py
+-rwxrwxrwx   0 root         (0) root         (0)     1805 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_scipy.py
+-rwxrwxrwx   0 root         (0) root         (0)     1037 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_six.py
+-rwxrwxrwx   0 root         (0) root         (0)     2495 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_hooks/test_wx_lib_pubsub.py
+-rwxrwxrwx   0 root         (0) root         (0)    24086 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_import.py
+-rwxrwxrwx   0 root         (0) root         (0)     3321 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_import_pep302.py
+-rwxrwxrwx   0 root         (0) root         (0)     4503 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_importlib_resources.py
+-rwxrwxrwx   0 root         (0) root         (0)     1784 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_interactive.py
+-rwxrwxrwx   0 root         (0) root         (0)    13513 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_libraries.py
+-rwxrwxrwx   0 root         (0) root         (0)     1937 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_linux_appimage.py
+-rwxrwxrwx   0 root         (0) root         (0)     3231 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_macos_bundle_signing.py
+-rwxrwxrwx   0 root         (0) root         (0)     6032 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_misc.py
+-rwxrwxrwx   0 root         (0) root         (0)     2015 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_module_exclusion.py
+-rwxrwxrwx   0 root         (0) root         (0)      672 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/functional/test_multipackage.py
+-rwxrwxrwx   0 root         (0) root         (0)     5992 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_multiprocess.py
+-rwxrwxrwx   0 root         (0) root         (0)     5519 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_path_encodings.py
+-rwxrwxrwx   0 root         (0) root         (0)     4594 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_pkg_resources_provider.py
+-rwxrwxrwx   0 root         (0) root         (0)     4603 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_pkgutil.py
+-rwxrwxrwx   0 root         (0) root         (0)     3160 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_pywin32.py
+-rwxrwxrwx   0 root         (0) root         (0)    21385 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_qt.py
+-rwxrwxrwx   0 root         (0) root         (0)     5764 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_regression.py
+-rwxrwxrwx   0 root         (0) root         (0)      918 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_runtime.py
+-rwxrwxrwx   0 root         (0) root         (0)     3428 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_signals.py
+-rwxrwxrwx   0 root         (0) root         (0)     3000 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_unbuffered_stdio.py
+-rwxrwxrwx   0 root         (0) root         (0)     2803 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/functional/test_updating_manifest.py
+-rwxrwxrwx   0 root         (0) root         (0)      895 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/requirements-developer.txt
+-rwxrwxrwx   0 root         (0) root         (0)     2058 2023-03-12 16:25:45.000000 pyinstaller-5.9.0/tests/requirements-libraries.txt
+-rwxrwxrwx   0 root         (0) root         (0)     1020 2023-02-19 13:09:11.000000 pyinstaller-5.9.0/tests/requirements-tools.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.671071 pyinstaller-5.9.0/tests/scripts/
+-rwxrwxrwx   0 root         (0) root         (0)      980 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/Dockerfile
+-rwxrwxrwx   0 root         (0) root         (0)       67 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/README
+-rwxrwxrwx   0 root         (0) root         (0)     2573 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/check-pefile-arch.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.673606 pyinstaller-5.9.0/tests/scripts/eggs4testing/
+-rwxrwxrwx   0 root         (0) root         (0)      128 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/.gitignore
+-rwxrwxrwx   0 root         (0) root         (0)      240 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/README.txt
+-rwxrwxrwx   0 root         (0) root         (0)     4204 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/build-nspkg-tests.py
+-rwxrwxrwx   0 root         (0) root         (0)     3258 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/make.sh
+-rwxrwxrwx   0 root         (0) root         (0)      829 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/setup-unzipped.py
+-rwxrwxrwx   0 root         (0) root         (0)      801 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/setup-zipped.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.674039 pyinstaller-5.9.0/tests/scripts/eggs4testing/unzipped_egg/
+-rwxrwxrwx   0 root         (0) root         (0)      678 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/unzipped_egg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.674482 pyinstaller-5.9.0/tests/scripts/eggs4testing/unzipped_egg/data/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/unzipped_egg/data/datafile.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.674772 pyinstaller-5.9.0/tests/scripts/eggs4testing/zipped_egg/
+-rwxrwxrwx   0 root         (0) root         (0)      678 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/zipped_egg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.675212 pyinstaller-5.9.0/tests/scripts/eggs4testing/zipped_egg/data/
+-rwxrwxrwx   0 root         (0) root         (0)       33 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/eggs4testing/zipped_egg/data/datafile.txt
+-rwxrwxrwx   0 root         (0) root         (0)       81 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/scripts/printShortLongCWD.cmd
+-rwxrwxrwx   0 root         (0) root         (0)     1190 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/test-cliutils.sh
+-rwxrwxrwx   0 root         (0) root         (0)     1300 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/scripts/test-docker.sh
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.675486 pyinstaller-5.9.0/tests/speed/
+-rwxrwxrwx   0 root         (0) root         (0)     1705 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/speed/speed_pefile.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.689319 pyinstaller-5.9.0/tests/unit/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.691513 pyinstaller-5.9.0/tests/unit/Tree_files/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/dynamiclib.dll
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/dynamiclib.dylib
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/nine.dat
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.692019 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.692257 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/data/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/data/eleven.dat
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/one.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.692734 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/sub_pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/sub_pkg/init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/sub_pkg/three.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/py_files_not_in_package/ten.dat
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/pyextension.pyd
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/pyextension.so
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.693440 pyinstaller-5.9.0/tests/unit/Tree_files/subpkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/subpkg/init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/Tree_files/subpkg/thirteen.txt
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/subpkg/twelve.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/Tree_files/two.py
+-rwxrwxrwx   0 root         (0) root         (0)      791 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/conftest.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.694122 pyinstaller-5.9.0/tests/unit/hook_order_hooks/
+-rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/MANIFEST.in
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.694853 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/
+-rwxrwxrwx   0 root         (0) root         (0)       94 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       46 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/hook-pyi_example_package.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.695094 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/rthooks/
+-rwxrwxrwx   0 root         (0) root         (0)       47 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/rthooks/pyi_rth_naughty.py
+-rwxrwxrwx   0 root         (0) root         (0)       55 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/pyi_example_package/rthooks.dat
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.695337 pyinstaller-5.9.0/tests/unit/hook_order_hooks/rthooks/
+-rwxrwxrwx   0 root         (0) root         (0)      507 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/rthooks/pyi_rth_good.py
+-rwxrwxrwx   0 root         (0) root         (0)       52 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/rthooks.dat
+-rwxrwxrwx   0 root         (0) root         (0)      286 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hook_order_hooks/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.695581 pyinstaller-5.9.0/tests/unit/hookutils_files/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.697609 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/dynamiclib.dll
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/dynamiclib.dylib
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/nine.dat
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.698143 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.698389 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/data/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/data/eleven.dat
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/one.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.699100 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/sub_pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/sub_pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/sub_pkg/three.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/py_files_not_in_package/ten.dat
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/pyextension.pyd
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/pyextension.so
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.699589 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_1/
+-rwxrwxrwx   0 root         (0) root         (0)       34 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_1/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        0 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_1/foo.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.700034 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_2/
+-rwxrwxrwx   0 root         (0) root         (0)       34 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        0 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/raises_error_on_import_2/foo.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.700704 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/subpkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/subpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/subpkg/thirteen.txt
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/subpkg/twelve.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/hookutils_package/two.py
+-rwxrwxrwx   0 root         (0) root         (0)      939 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/hookutils_files/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.272016 pyinstaller-5.9.0/tests/unit/hookutils_files2/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.700953 pyinstaller-5.9.0/tests/unit/hookutils_files2/foo/
+-rwxrwxrwx   0 root         (0) root         (0)        0 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/hookutils_files2/foo/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.701160 pyinstaller-5.9.0/tests/unit/hookutils_files2/foo/bar/
+-rwxrwxrwx   0 root         (0) root         (0)       52 2023-02-23 22:46:13.000000 pyinstaller-5.9.0/tests/unit/hookutils_files2/foo/bar/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     9389 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_TOC.py
+-rwxrwxrwx   0 root         (0) root         (0)     2664 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_Tree.py
+-rwxrwxrwx   0 root         (0) root         (0)     1115 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_additionalfilescache.py
+-rwxrwxrwx   0 root         (0) root         (0)      991 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_bindepend.py
+-rwxrwxrwx   0 root         (0) root         (0)     5305 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_building_utils.py
+-rwxrwxrwx   0 root         (0) root         (0)     6647 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_bytecode.py
+-rwxrwxrwx   0 root         (0) root         (0)     2142 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_compat.py
+-rwxrwxrwx   0 root         (0) root         (0)     4153 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_depend_utils.py
+-rwxrwxrwx   0 root         (0) root         (0)     1189 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_hook_order.py
+-rwxrwxrwx   0 root         (0) root         (0)    16330 2023-02-25 00:58:06.000000 pyinstaller-5.9.0/tests/unit/test_hookutils.py
+-rwxrwxrwx   0 root         (0) root         (0)      772 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_hookutils_gi.py
+-rwxrwxrwx   0 root         (0) root         (0)    10520 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_isolation.py
+-rwxrwxrwx   0 root         (0) root         (0)     2077 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_loader.py
+-rwxrwxrwx   0 root         (0) root         (0)     1746 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_makespec.py
+-rwxrwxrwx   0 root         (0) root         (0)     7060 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_miscutils.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.708747 pyinstaller-5.9.0/tests/unit/test_modulegraph/
+-rwxrwxrwx   0 root         (0) root         (0)       27 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     1355 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_basic.py
+-rwxrwxrwx   0 root         (0) root         (0)     2330 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_compiled_modules.py
+-rwxrwxrwx   0 root         (0) root         (0)    23743 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_edge_data.py
+-rwxrwxrwx   0 root         (0) root         (0)     1689 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_explicit_packages.py
+-rwxrwxrwx   0 root         (0) root         (0)     2892 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_implies.py
+-rwxrwxrwx   0 root         (0) root         (0)     4488 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_import_from_init.py
+-rwxrwxrwx   0 root         (0) root         (0)    22218 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_imports.py
+-rwxrwxrwx   0 root         (0) root         (0)    39070 2023-01-08 13:33:19.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_modulegraph.py
+-rwxrwxrwx   0 root         (0) root         (0)     8010 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_pep420_nspkg.py
+-rwxrwxrwx   0 root         (0) root         (0)     1894 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_pycompat_pkg.py
+-rwxrwxrwx   0 root         (0) root         (0)     1396 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_relimport2.py
+-rwxrwxrwx   0 root         (0) root         (0)     3843 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_setuptools_nspkg.py
+-rwxrwxrwx   0 root         (0) root         (0)     1654 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_swig.py
+-rwxrwxrwx   0 root         (0) root         (0)     2193 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_util.py
+-rwxrwxrwx   0 root         (0) root         (0)    11977 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/test_zipio.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.711315 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.275871 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.272562 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.711796 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.712091 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      314 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.713454 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/child/nameduser-1.5-py2.6.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.713702 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.713945 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      314 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.715181 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.10/parent/namedpkg-1.0-py2.6.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.272994 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.715431 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.715676 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      306 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.716900 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/child/nameduser-1.5-py2.5.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.717154 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.717402 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      306 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.718652 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/distribute-0.6.12/parent/namedpkg-1.0-py2.5.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.273424 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.718907 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.719149 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      306 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.720375 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/child/nameduser-1.5-py2.5.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.720622 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.720874 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      306 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.722104 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-0.6c9/parent/namedpkg-1.0-py2.5.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.273855 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.722358 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.722607 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      312 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.723842 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/child/nameduser-1.5-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.724095 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.724342 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      312 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.725566 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.1.0/parent/namedpkg-1.0-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.274303 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.725818 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.726062 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      362 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.727291 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/child/nameduser-1.5-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.727540 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.727807 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      362 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.729041 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-28.7.0/parent/namedpkg-1.0-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.274780 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.729318 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.729566 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      566 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.730796 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/child/nameduser-1.5-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.731054 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.731304 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      566 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.732524 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-31.0.0/parent/namedpkg-1.0-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.275225 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.732777 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.733022 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      550 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.734264 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/child/nameduser-1.5-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.734521 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.734761 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      550 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.735982 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-34.3.0/parent/namedpkg-1.0-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.275665 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.736238 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.736483 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/namedpkg/slave.py
+-rwxrwxrwx   0 root         (0) root         (0)      550 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.737748 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/child/nameduser-1.5-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.738003 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.738254 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg/parent.py
+-rwxrwxrwx   0 root         (0) root         (0)      550 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7-nspkg.pth
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.739487 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/setuptools-40.4.3/parent/namedpkg-1.0-py2.7.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.739735 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.740101 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.740648 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       57 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/namedpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       35 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/namedpkg/slave.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.742083 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      191 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      228 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/nameduser.egg-info/top_level.txt
+-rwxrwxrwx   0 root         (0) root         (0)      168 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/child/setup.py
+-rwxrwxrwx   0 root         (0) root         (0)     1706 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/install.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.742356 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.742914 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       57 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg/parent.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.744173 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      190 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      224 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)       10 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/namedpkg.egg-info/top_level.txt
+-rwxrwxrwx   0 root         (0) root         (0)      167 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/nspkg/src/parent/setup.py
+-rwxrwxrwx   0 root         (0) root         (0)       58 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/script
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.744672 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/subdir/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/subdir/file1.txt
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/subdir/file2.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.745891 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/
+-rwxrwxrwx   0 root         (0) root         (0)       24 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/myext.pyd
+-rwxrwxrwx   0 root         (0) root         (0)       24 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/myext.so
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/mymodule.py
+-rwxrwxrwx   0 root         (0) root         (0)       21 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/mymodule2.pyc
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/mymodule3.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.746133 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/mypkg/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath/mypkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)     2065 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath.egg
+-rwxrwxrwx   0 root         (0) root         (0)     1825 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/syspath.zip
+-rwxrwxrwx   0 root         (0) root         (0)      760 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/test.egg
+-rwxrwxrwx   0 root         (0) root         (0)       17 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/test.txt
+-rwxrwxrwx   0 root         (0) root         (0)     1627 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testdata/zipped.egg
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.276570 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.747084 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       13 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      122 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/pkg/api.py
+-rwxrwxrwx   0 root         (0) root         (0)      160 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/pkg/api2.py
+-rwxrwxrwx   0 root         (0) root         (0)      182 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compatmodule/pkg/api3.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.276741 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.747328 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/compiled/
+-rwxrwxrwx   0 root         (0) root         (0)       19 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/compiled/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.748288 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/source/
+-rwxrwxrwx   0 root         (0) root         (0)       37 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/source/mod1.py
+-rwxrwxrwx   0 root         (0) root         (0)       72 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/source/mod2.py
+-rwxrwxrwx   0 root         (0) root         (0)       33 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/source/mod3.py
+-rwxrwxrwx   0 root         (0) root         (0)       43 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-compiled/source/mod4.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.752900 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_class_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_conditional_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_conditional_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_conditional_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/function_import_existing.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.756571 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_class_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_conditional_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_conditional_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_conditional_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/function_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_class_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_conditional_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_conditional_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_conditional_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/pkg/toplevel_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)     1435 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/script.py
+-rwxrwxrwx   0 root         (0) root         (0)     1597 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/script_from_import.py
+-rwxrwxrwx   0 root         (0) root         (0)      291 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/script_multi_import.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_class_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_conditional_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_conditional_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_conditional_import_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_import2_existing.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-edgedata/toplevel_import_existing.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.756821 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.757067 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       13 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.757836 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/subpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       80 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/subpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       52 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/subpkg/_collections.py
+-rwxrwxrwx   0 root         (0) root         (0)       42 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg/subpkg/compat.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.758077 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.758793 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/subpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       83 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/subpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       53 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/subpkg/_collections.py
+-rwxrwxrwx   0 root         (0) root         (0)       43 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/pkg2/subpkg/compat.py
+-rwxrwxrwx   0 root         (0) root         (0)       39 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-import-from-init/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.759036 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/main_script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.759522 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.760002 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub1/
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub1/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub1/modA.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.760486 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub2/
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub2/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-packages/pkg/sub3.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.277717 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.277635 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path1/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.760742 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path1/package/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path1/package/sub2.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.277752 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.760987 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.761239 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/nspkg/
+-rwxrwxrwx   0 root         (0) root         (0)       27 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/nspkg/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/sub1.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.761734 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/subpackage/
+-rwxrwxrwx   0 root         (0) root         (0)       28 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/subpackage/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       32 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-pep420-namespace/path2/package/subpackage/sub.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.761980 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/
+-rwxrwxrwx   0 root         (0) root         (0)       19 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/main_script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.762711 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       17 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/pkg/a.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr1/pkg/b.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.762960 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/main_script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.763707 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)      162 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/pkg/base.py
+-rwxrwxrwx   0 root         (0) root         (0)       16 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr2/pkg/pkg.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.763957 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.764206 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/mypkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/mypkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.764727 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/mypkg/json/
+-rwxrwxrwx   0 root         (0) root         (0)        2 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/mypkg/json/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       68 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/mypkg/json/encoder.py
+-rwxrwxrwx   0 root         (0) root         (0)       31 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr3/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.764989 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.765236 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/__init__.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.766229 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/core/
+-rwxrwxrwx   0 root         (0) root         (0)       27 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/core/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      102 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/core/callables.py
+-rwxrwxrwx   0 root         (0) root         (0)      166 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/core/listener.py
+-rwxrwxrwx   0 root         (0) root         (0)       90 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/pkg/core/listenerimpl.py
+-rwxrwxrwx   0 root         (0) root         (0)       50 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr4/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.766726 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr5/
+-rwxrwxrwx   0 root         (0) root         (0)       31 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr5/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      111 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr5/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.766977 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr7/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.767471 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr7/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       17 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr7/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       68 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr7/pkg/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       21 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr7/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.767996 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr8/
+-rwxrwxrwx   0 root         (0) root         (0)       33 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr8/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-regr8/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.768497 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/
+-rwxrwxrwx   0 root         (0) root         (0)       25 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/mod.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.770018 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       19 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       26 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/mod.py
+-rwxrwxrwx   0 root         (0) root         (0)       12 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/oldstyle.py
+-rwxrwxrwx   0 root         (0) root         (0)       59 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/relative.py
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/relimport.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.770524 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/sub2/
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/sub2/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/sub2/mod.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.771634 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/subpkg/
+-rwxrwxrwx   0 root         (0) root         (0)       20 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/subpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)      121 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/subpkg/mod2.py
+-rwxrwxrwx   0 root         (0) root         (0)       89 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/subpkg/relative.py
+-rwxrwxrwx   0 root         (0) root         (0)      109 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/subpkg/relative2.py
+-rwxrwxrwx   0 root         (0) root         (0)       52 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/pkg/toplevel.py
+-rwxrwxrwx   0 root         (0) root         (0)      184 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport/script.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.771884 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.772870 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)       41 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       14 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/mod1.py
+-rwxrwxrwx   0 root         (0) root         (0)       14 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/mod2.py
+-rwxrwxrwx   0 root         (0) root         (0)       14 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/mod3.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.773120 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/sub/
+-rwxrwxrwx   0 root         (0) root         (0)       68 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/pkg/sub/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       18 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-relimport2/toplevel.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.773374 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/
+-rwxrwxrwx   0 root         (0) root         (0)      231 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/setup.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.279536 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.773895 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/
+-rwxrwxrwx   0 root         (0) root         (0)      207 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       22 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/module.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.775873 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/nssubpkg/
+-rwxrwxrwx   0 root         (0) root         (0)      207 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/nssubpkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)       27 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg/nssubpkg/sub.py
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.775389 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/
+-rwxrwxrwx   0 root         (0) root         (0)      187 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/PKG-INFO
+-rwxrwxrwx   0 root         (0) root         (0)      323 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/SOURCES.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/dependency_links.txt
+-rwxrwxrwx   0 root         (0) root         (0)       23 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/namespace_packages.txt
+-rwxrwxrwx   0 root         (0) root         (0)        2 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/not-zip-safe
+-rwxrwxrwx   0 root         (0) root         (0)        7 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-setuptools-namespace/src/nspkg.egg-info/top_level.txt
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.279722 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-swig/
+drwxrwxrwx   0 root         (0) root         (0)        0 2023-03-13 20:35:17.776591 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-swig/pkg/
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-swig/pkg/__init__.py
+-rwxrwxrwx   0 root         (0) root         (0)        3 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-swig/pkg/_sample.py
+-rwxrwxrwx   0 root         (0) root         (0)     2146 2022-11-30 18:58:46.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph/testpkg-swig/pkg/sample.py
+-rwxrwxrwx   0 root         (0) root         (0)    25961 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_modulegraph_more.py
+-rwxrwxrwx   0 root         (0) root         (0)     3034 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_normalize_icon_type.py
+-rwxrwxrwx   0 root         (0) root         (0)     8891 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_pyimodulegraph.py
+-rwxrwxrwx   0 root         (0) root         (0)     3087 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_recursion_limit.py
+-rwxrwxrwx   0 root         (0) root         (0)     1278 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_systemexit.py
+-rwxrwxrwx   0 root         (0) root         (0)     1650 2023-02-11 14:47:39.000000 pyinstaller-5.9.0/tests/unit/test_winmanifest.py
```

### Comparing `pyinstaller-5.8.0/COPYING.txt` & `pyinstaller-5.9.0/COPYING.txt`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/MANIFEST.in` & `pyinstaller-5.9.0/MANIFEST.in`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PKG-INFO` & `pyinstaller-5.9.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyinstaller
-Version: 5.8.0
+Version: 5.9.0
 Summary: PyInstaller bundles a Python application and all its dependencies into a single package.
 Home-page: https://www.pyinstaller.org/
 Author: Hartmut Goebel, Giovanni Bajo, David Vierra, David Cortesi, Martin Zibricky
 License: GPLv2-or-later with a special exception which allows to use PyInstaller to build and distribute non-free programs (including commercial ones)
 Project-URL: Source, https://github.com/pyinstaller/pyinstaller
 Keywords: packaging, app, apps, bundle, convert, standalone, executable,pyinstaller, cxfreeze, freeze, py2exe, py2app, bbfreeze
 Classifier: Development Status :: 6 - Mature
@@ -179,21 +179,21 @@
 pyinstaller`` provided that you have an appropriate C compiler (typically
 either ``gcc`` or ``clang``) and zlib's development headers already installed.
 
 
 Support
 -------
 
-- Official debugging guide: https://pyinstaller.org/en/v5.8.0/when-things-go-wrong.html
+- Official debugging guide: https://pyinstaller.org/en/v5.9.0/when-things-go-wrong.html
 - Assorted user contributed help topics: https://github.com/pyinstaller/pyinstaller/wiki
 - Web based Q&A forums: https://github.com/pyinstaller/pyinstaller/discussions
 - Email based Q&A forums: https://groups.google.com/g/pyinstaller
 
 
 Changes in this Release
 -----------------------
 
 You can find a detailed list of changes in this release
 in the `Changelog`_ section of the manual.
 
-.. _`manual`: https://pyinstaller.org/en/v5.8.0/
-.. _`Changelog`: https://pyinstaller.org/en/v5.8.0/CHANGES.html
+.. _`manual`: https://pyinstaller.org/en/v5.9.0/
+.. _`Changelog`: https://pyinstaller.org/en/v5.9.0/CHANGES.html
```

### Comparing `pyinstaller-5.8.0/PyInstaller/__init__.py` & `pyinstaller-5.9.0/PyInstaller/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 import os
 import sys
 
 from PyInstaller import compat
 from PyInstaller.utils.git import get_repo_revision
 
 # Note: Keep this variable as plain string so it could be updated automatically when doing a release.
-__version__ = '5.8.0'
+__version__ = '5.9.0'
 
 # Absolute path of this package's directory. Save this early so all submodules can use the absolute path. This is
 # required for example if the current directory changes prior to loading the hooks.
 PACKAGEPATH = os.path.abspath(os.path.dirname(__file__))
 
 HOMEPATH = os.path.dirname(PACKAGEPATH)
```

### Comparing `pyinstaller-5.8.0/PyInstaller/__main__.py` & `pyinstaller-5.9.0/PyInstaller/__main__.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/_recursion_too_deep_message.py` & `pyinstaller-5.9.0/PyInstaller/_recursion_too_deep_message.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/_shared_with_waf.py` & `pyinstaller-5.9.0/PyInstaller/_shared_with_waf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/archive/pyz_crypto.py` & `pyinstaller-5.9.0/PyInstaller/archive/pyz_crypto.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/archive/readers.py` & `pyinstaller-5.9.0/PyInstaller/archive/readers.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/archive/writers.py` & `pyinstaller-5.9.0/PyInstaller/archive/writers.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/run` & `pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/run`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/run_d` & `pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/run_d`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/runw` & `pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/runw`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Darwin-64bit/runw_d` & `pyinstaller-5.9.0/PyInstaller/bootloader/Darwin-64bit/runw_d`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/run.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/run.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/run_d.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/run_d.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/runw.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/runw.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-32bit-intel/runw_d.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-32bit-intel/runw_d.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/run.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/run.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/run_d.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/run_d.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/runw.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/runw.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/Windows-64bit-intel/runw_d.exe` & `pyinstaller-5.9.0/PyInstaller/bootloader/Windows-64bit-intel/runw_d.exe`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-console.icns` & `pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-console.icns`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-console.ico` & `pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-console.ico`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-windowed.icns` & `pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-windowed.icns`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/bootloader/images/icon-windowed.ico` & `pyinstaller-5.9.0/PyInstaller/bootloader/images/icon-windowed.ico`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/api.py` & `pyinstaller-5.9.0/PyInstaller/building/api.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/build_main.py` & `pyinstaller-5.9.0/PyInstaller/building/build_main.py`

 * *Files 1% similar despite different names*

```diff
@@ -104,14 +104,16 @@
 
     import sys  # noqa: F401
     from traceback import format_exception_only
     import pkg_resources
     from PyInstaller.log import logger
 
     entry_points = pkg_resources.iter_entry_points('pyinstaller40', 'hook-dirs')
+    # Ensure that pyinstaller_hooks_contrib comes last so that hooks from packages providing their own take priority.
+    entry_points = sorted(entry_points, key=lambda x: x.module_name == "_pyinstaller_hooks_contrib.hooks")
 
     hook_directories = []
     for entry_point in entry_points:
         try:
             hook_directories.extend(entry_point.load()())
         except Exception as e:
             msg = "".join(format_exception_only(type(e), e)).strip()
```

### Comparing `pyinstaller-5.8.0/PyInstaller/building/datastruct.py` & `pyinstaller-5.9.0/PyInstaller/building/datastruct.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/icon.py` & `pyinstaller-5.9.0/PyInstaller/building/icon.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/makespec.py` & `pyinstaller-5.9.0/PyInstaller/building/makespec.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/osx.py` & `pyinstaller-5.9.0/PyInstaller/building/osx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/splash.py` & `pyinstaller-5.9.0/PyInstaller/building/splash.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/splash_templates.py` & `pyinstaller-5.9.0/PyInstaller/building/splash_templates.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/templates.py` & `pyinstaller-5.9.0/PyInstaller/building/templates.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/toc_conversion.py` & `pyinstaller-5.9.0/PyInstaller/building/toc_conversion.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/building/utils.py` & `pyinstaller-5.9.0/PyInstaller/building/utils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/compat.py` & `pyinstaller-5.9.0/PyInstaller/compat.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/config.py` & `pyinstaller-5.9.0/PyInstaller/config.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/configure.py` & `pyinstaller-5.9.0/PyInstaller/configure.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/analysis.py` & `pyinstaller-5.9.0/PyInstaller/depend/analysis.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/bindepend.py` & `pyinstaller-5.9.0/PyInstaller/depend/bindepend.py`

 * *Files 0% similar despite different names*

```diff
@@ -362,15 +362,15 @@
     for i, name in enumerate(components):
         if name.lower().endswith(".egg"):
             eggpth = os.path.sep.join(components[:i + 1])
             if os.path.isfile(eggpth):
                 # eggs can also be directories!
                 try:
                     egg = zipfile.ZipFile(eggpth)
-                except zipfile.BadZipfile as e:
+                except zipfile.BadZipFile as e:
                     raise SystemExit("Error: %s %s" % (eggpth, e))
                 if todir is None:
                     # Use the same directory as setuptools/pkg_resources. So, if the specific egg was accessed before
                     # (not necessarily by pyinstaller), the extracted contents already exist (pkg_resources puts them
                     # there) and can be used.
                     todir = os.path.join(pkg_resources_get_default_cache(), name + "-tmp")
                 if components[i + 1:]:
```

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/bytecode.py` & `pyinstaller-5.9.0/PyInstaller/depend/bytecode.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/dylib.py` & `pyinstaller-5.9.0/PyInstaller/depend/dylib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/imphook.py` & `pyinstaller-5.9.0/PyInstaller/depend/imphook.py`

 * *Files 0% similar despite different names*

```diff
@@ -110,18 +110,14 @@
 
             # For each hook script in this directory...
             hook_filenames = glob.glob(os.path.join(hook_dir, 'hook-*.py'))
             for hook_filename in hook_filenames:
                 # Fully-qualified name of this hook's corresponding module, constructed by removing the "hook-" prefix
                 # and ".py" suffix.
                 module_name = os.path.basename(hook_filename)[5:-3]
-                if module_name in self:
-                    logger.warning(
-                        "Several hooks defined for module %r. Please take care they do not conflict.", module_name
-                    )
 
                 # Lazily loadable hook object.
                 module_hook = ModuleHook(
                     module_graph=self.module_graph,
                     module_name=module_name,
                     hook_filename=hook_filename,
                     hook_module_name_prefix=self._hook_module_name_prefix,
```

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/imphookapi.py` & `pyinstaller-5.9.0/PyInstaller/depend/imphookapi.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/depend/utils.py` & `pyinstaller-5.9.0/PyInstaller/depend/utils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/exceptions.py` & `pyinstaller-5.9.0/PyInstaller/exceptions.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/fake-modules/pyi_splash.py` & `pyinstaller-5.9.0/PyInstaller/fake-modules/pyi_splash.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.Image.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.Image.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.ImageFilter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.ImageFilter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.SpiderImagePlugin.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.SpiderImagePlugin.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PIL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PIL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QAxContainer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QAxContainer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qsci.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qsci.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DAnimation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DAnimation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DInput.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DInput.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DLogic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DLogic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.Qt3DRender.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.Qt3DRender.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtBluetooth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtBluetooth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtChart.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtChart.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDBus.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDBus.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDataVisualization.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDataVisualization.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtDesigner.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtDesigner.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtGui.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtGui.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtHelp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtHelp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtLocation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtLocation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMacExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMacExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMultimedia.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMultimedia.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtMultimediaWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtMultimediaWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNetwork.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNetwork.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNetworkAuth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNetworkAuth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtNfc.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtNfc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtOpenGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtOpenGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPositioning.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPositioning.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPrintSupport.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPrintSupport.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtPurchasing.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtPurchasing.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuick3D.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuick3D.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtQuickWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtQuickWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtRemoteObjects.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtRemoteObjects.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtScript.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtScript.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSensors.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSensors.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSerialPort.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSerialPort.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSql.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSql.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtSvg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtSvg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtTest.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtTest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtTextToSpeech.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtTextToSpeech.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebChannel.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebChannel.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebEngineWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebKit.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebKit.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebKitWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebKitWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWebSockets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWebSockets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtWinExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtWinExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtX11Extras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtX11Extras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtXml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtXml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.QtXmlPatterns.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.QtXmlPatterns.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt5.uic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt5.uic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QAxContainer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QAxContainer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qsci.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qsci.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DAnimation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DAnimation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DInput.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DInput.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DLogic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DLogic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.Qt3DRender.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.Qt3DRender.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtBluetooth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtBluetooth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtCharts.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtCharts.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDBus.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDBus.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDataVisualization.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDataVisualization.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtDesigner.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtDesigner.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtGui.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtGui.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtHelp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtHelp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtMultimedia.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtMultimedia.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtMultimediaWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtMultimediaWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNetwork.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNetwork.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNetworkAuth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNetworkAuth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtNfc.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtNfc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtOpenGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtOpenGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtOpenGLWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtOpenGLWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPdf.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPdf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPdfWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPdfWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPositioning.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPositioning.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtPrintSupport.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtPrintSupport.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuick3D.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuick3D.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtQuickWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtQuickWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtRemoteObjects.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtRemoteObjects.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSensors.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSensors.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSerialPort.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSerialPort.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSql.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSql.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSvg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSvg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtSvgWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtSvgWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtTest.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtTest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebChannel.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebChannel.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebEngineWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWebSockets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWebSockets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.QtXml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.QtXml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PyQt6.uic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PyQt6.uic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DAnimation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DAnimation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DInput.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DInput.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DLogic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DLogic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qt3DRender.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qt3DRender.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtAxContainer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtAxContainer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtCharts.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtCharts.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtConcurrent.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtConcurrent.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtDataVisualization.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtDataVisualization.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtGui.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtGui.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtHelp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtHelp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtLocation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtLocation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMacExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMacExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMultimedia.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMultimedia.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtMultimediaWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtMultimediaWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtNetwork.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtNetwork.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtOpenGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtOpenGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtOpenGLFunctions.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtOpenGLFunctions.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtPositioning.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtPositioning.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtPrintSupport.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtPrintSupport.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuickControls2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuickControls2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtQuickWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtQuickWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtRemoteObjects.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtRemoteObjects.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScript.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScript.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScriptTools.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScriptTools.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtScxml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtScxml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSensors.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSensors.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSerialPort.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSerialPort.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSql.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSql.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtSvg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtSvg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtTest.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtTest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtTextToSpeech.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtTextToSpeech.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtUiTools.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtUiTools.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebChannel.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebChannel.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngineCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngineCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebEngineWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebEngineWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebKit.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebKit.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebKitWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebKitWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWebSockets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWebSockets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtWinExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtWinExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtX11Extras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtX11Extras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtXml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtXml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.QtXmlPatterns.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.QtXmlPatterns.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.Qwt5.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.Qwt5.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DAnimation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DAnimation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DExtras.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DExtras.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DInput.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DInput.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DLogic.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DLogic.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.Qt3DRender.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.Qt3DRender.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtAxContainer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtAxContainer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtBluetooth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtBluetooth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtCharts.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtCharts.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtConcurrent.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtConcurrent.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDBus.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDBus.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDataVisualization.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDataVisualization.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtDesigner.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtDesigner.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtGui.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtGui.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtHelp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtHelp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtHttpServer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtHttpServer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtMultimedia.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtMultimedia.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtMultimediaWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtMultimediaWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNetwork.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNetwork.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNetworkAuth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNetworkAuth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtNfc.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtNfc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtOpenGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtOpenGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtOpenGLWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtOpenGLWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPdf.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPdf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPdfWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPdfWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPositioning.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPositioning.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtPrintSupport.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtPrintSupport.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuick3D.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuick3D.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuickControls2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuickControls2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtQuickWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtQuickWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtRemoteObjects.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtRemoteObjects.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtScxml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtScxml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSensors.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSensors.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSerialPort.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSerialPort.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSpatialAudio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSpatialAudio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSql.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSql.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtStateMachine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtStateMachine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSvg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSvg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtSvgWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtSvgWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtTest.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtTest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtUiTools.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtUiTools.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebChannel.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebChannel.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineCore.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineCore.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineQuick.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineQuick.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebEngineWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebEngineWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWebSockets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWebSockets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtWidgets.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtWidgets.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.QtXml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.QtXml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-PySide6.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-PySide6.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-_tkinter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-_tkinter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-babel.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-babel.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-difflib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-difflib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-distutils.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-distutils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-distutils.util.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-distutils.util.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.contrib.sessions.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.contrib.sessions.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.cache.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.cache.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.mail.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.mail.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.core.management.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.core.management.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.mysql.base.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.mysql.base.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.oracle.base.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.oracle.base.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.db.backends.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.db.backends.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-django.template.loaders.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-django.template.loaders.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-encodings.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-encodings.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gevent.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gevent.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Adw.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Adw.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Atk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Atk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Champlain.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Champlain.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Clutter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Clutter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GIRepository.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GIRepository.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GLib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GLib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GModule.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GModule.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GObject.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GObject.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gdk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gdk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GdkPixbuf.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GdkPixbuf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Graphene.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Graphene.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gsk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gsk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gst.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gst.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstAllocators.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstAllocators.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstApp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstApp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstAudio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstAudio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstBadAudio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstBadAudio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstBase.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstBase.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstCheck.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstCheck.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstCodecs.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstCodecs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstController.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstController.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLEGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLEGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLWayland.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLWayland.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstGLX11.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstGLX11.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstInsertBin.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstInsertBin.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstMpegts.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstMpegts.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstNet.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstNet.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPbutils.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPbutils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPlay.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPlay.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstPlayer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstPlayer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtsp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtsp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstRtspServer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstRtspServer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstSdp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstSdp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstTag.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstTag.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstTranscoder.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstTranscoder.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVideo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVideo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkan.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkan.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkanWayland.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkanWayland.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstVulkanXCB.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstVulkanXCB.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GstWebRTC.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GstWebRTC.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Gtk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Gtk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkChamplain.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkChamplain.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkClutter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkClutter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkSource.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkSource.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.GtkosxApplication.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.GtkosxApplication.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.HarfBuzz.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.HarfBuzz.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.Pango.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.Pango.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.PangoCairo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.PangoCairo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.cairo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.cairo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.freetype2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.freetype2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-gi.repository.xlib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-gi.repository.xlib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-heapq.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-heapq.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-idlelib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-idlelib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-importlib_metadata.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-importlib_metadata.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-importlib_resources.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-importlib_resources.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-keyring.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-keyring.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-kivy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-kivy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-lib2to3.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-lib2to3.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.backends.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.backends.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.numerix.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.numerix.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-matplotlib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-matplotlib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-multiprocessing.util.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-multiprocessing.util.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-numpy._pytesttester.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pickle.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,16 +1,13 @@
-# -----------------------------------------------------------------------------
-# Copyright (c) 2013-2023, PyInstaller Development Team.
+#-----------------------------------------------------------------------------
+# Copyright (c) 2015-2023, PyInstaller Development Team.
 #
 # Distributed under the terms of the GNU General Public License (version 2
 # or later) with exception for distributing the bootloader.
 #
 # The full license is in the file COPYING.txt, distributed with this software.
 #
 # SPDX-License-Identifier: (GPL-2.0-or-later WITH Bootloader-exception)
-# -----------------------------------------------------------------------------
+#-----------------------------------------------------------------------------
 
-# numpy._pytesttester is unconditionally imported by numpy.core, thus we can not exclude _pytesttester (which would be
-# preferred). Anyway, we can avoid importing pytest, which pulls in anotehr 150+ modules. See
-# https://github.com/numpy/numpy/issues/17183
-
-excludedimports = ["pytest"]
+# Only required when run as `__main__`
+excludedimports = ["argparse", "doctest"]
```

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-numpy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-numpy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-packaging.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-packaging.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.io.formats.style.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.io.formats.style.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.plotting.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.plotting.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pandas.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pandas.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pickle.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-zope.interface.py`

 * *Files 13% similar despite different names*

```diff
@@ -5,9 +5,8 @@
 # or later) with exception for distributing the bootloader.
 #
 # The full license is in the file COPYING.txt, distributed with this software.
 #
 # SPDX-License-Identifier: (GPL-2.0-or-later WITH Bootloader-exception)
 #-----------------------------------------------------------------------------
 
-# Only required when run as `__main__`
-excludedimports = ["argparse", "doctest"]
+excludedimports = ["unittest"]
```

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pkg_resources.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pkg_resources.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-platform.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-platform.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pygments.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pygments.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pytz.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pytz.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-pytzdata.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-pytzdata.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-qtawesome.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-qtawesome.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scapy.layers.all.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scapy.layers.all.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.io.matlab.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.io.matlab.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.linalg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.linalg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.sparse.csgraph.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.sparse.csgraph.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.spatial.transform.rotation.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.spatial.transform.rotation.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.special._ellip_harm_2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.special._ellip_harm_2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.special._ufuncs.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.special._ufuncs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scipy.stats._stats.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scipy.stats._stats.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-scrapy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-scrapy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-setuptools.msvc.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-setuptools.msvc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-setuptools.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-setuptools.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-shelve.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-shelve.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-sphinx.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-sphinx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-sqlalchemy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-sqlalchemy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-sqlite3.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-sqlite3.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-sysconfig.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-sysconfig.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-wcwidth.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-wcwidth.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-win32ctypes.core.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-win32ctypes.core.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.dom.domreg.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.dom.domreg.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.etree.cElementTree.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.etree.cElementTree.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-xml.py` & `pyinstaller-5.9.0/PyInstaller/hooks/hook-xml.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/hook-zope.interface.py` & `pyinstaller-5.9.0/tests/functional/modules/error_during_import2.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #-----------------------------------------------------------------------------
-# Copyright (c) 2015-2023, PyInstaller Development Team.
+# Copyright (c) 2013-2023, PyInstaller Development Team.
 #
 # Distributed under the terms of the GNU General Public License (version 2
 # or later) with exception for distributing the bootloader.
 #
 # The full license is in the file COPYING.txt, distributed with this software.
 #
 # SPDX-License-Identifier: (GPL-2.0-or-later WITH Bootloader-exception)
 #-----------------------------------------------------------------------------
 
-excludedimports = ["unittest"]
+raise KeyError
```

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-PyQt5.uic.port_v2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-PyQt5.uic.port_v2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-distutils.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-distutils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_find_module_path/hook-pyi_splash.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_find_module_path/hook-pyi_splash.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Adw.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Adw.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Atk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Atk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Champlain.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Champlain.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Clutter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Clutter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GIRepository.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GIRepository.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GLib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GLib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GModule.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GModule.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GObject.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GObject.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gdk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gdk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GdkPixbuf.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GdkPixbuf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Graphene.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Graphene.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gsk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gsk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gst.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gst.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAllocators.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAllocators.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstApp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstApp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAudio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstAudio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBadAudio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBadAudio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBase.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstBase.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCheck.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCheck.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCodecs.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstCodecs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstController.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstController.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLEGL.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLEGL.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLWayland.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLWayland.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLX11.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstGLX11.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstInsertBin.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstInsertBin.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstMpegts.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstMpegts.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstNet.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstNet.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPbutils.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPbutils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlay.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlay.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlayer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstPlayer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtsp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtsp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtspServer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstRtspServer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstSdp.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstSdp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTag.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTag.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTranscoder.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstTranscoder.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVideo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVideo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkan.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkan.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanWayland.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanWayland.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanXCB.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstVulkanXCB.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstWebRTC.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GstWebRTC.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gtk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Gtk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkChamplain.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkChamplain.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkClutter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkClutter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkSource.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkSource.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkosxApplication.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.GtkosxApplication.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.HarfBuzz.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.HarfBuzz.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Pango.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.Pango.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.PangoCairo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.PangoCairo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.cairo.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.cairo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.freetype2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.freetype2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.xlib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-gi.repository.xlib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-setuptools.extern.six.moves.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-setuptools.extern.six.moves.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-six.moves.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-six.moves.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/pre_safe_import_module/hook-urllib3.packages.six.moves.py` & `pyinstaller-5.9.0/PyInstaller/hooks/pre_safe_import_module/hook-urllib3.packages.six.moves.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth__tkinter.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth__tkinter.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_django.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_django.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gdkpixbuf.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gdkpixbuf.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gi.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gi.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gio.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gio.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_glib.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_glib.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gstreamer.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gstreamer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_gtk.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_gtk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_inspect.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_inspect.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_kivy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_kivy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_mplconfig.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_mplconfig.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_multiprocessing.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_multiprocessing.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pkgres.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pkgres.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pkgutil.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pkgutil.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5webengine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt5webengine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6webengine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyqt6webengine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2webengine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside2webengine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6webengine.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_pyside6webengine.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_setuptools.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_setuptools.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks/pyi_rth_win32comgenpy.py` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks/pyi_rth_win32comgenpy.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/hooks/rthooks.dat` & `pyinstaller-5.9.0/PyInstaller/hooks/rthooks.dat`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/isolated/__init__.py` & `pyinstaller-5.9.0/PyInstaller/isolated/__init__.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/isolated/_child.py` & `pyinstaller-5.9.0/PyInstaller/isolated/_child.py`

 * *Files 3% similar despite different names*

```diff
@@ -86,10 +86,12 @@
 
 
 if __name__ == '__main__':
     read_from_parent, write_to_parent = map(int, sys.argv[1:])
 
     with _open(read_from_parent, "rb") as read_fh:
         with _open(write_to_parent, "wb") as write_fh:
+            sys.path = loads(b64decode(read_fh.readline()))
+
             # Keep receiving and running instructions until the parent sends the signal to stop.
             while run_next_command(read_fh, write_fh):
                 pass
```

### Comparing `pyinstaller-5.8.0/PyInstaller/isolated/_parent.py` & `pyinstaller-5.9.0/PyInstaller/isolated/_parent.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,14 +11,15 @@
 
 import os
 from pathlib import Path
 from marshal import loads, dumps
 from base64 import b64encode, b64decode
 import functools
 import subprocess
+import sys
 
 from PyInstaller import compat
 from PyInstaller import log as logging
 
 logger = logging.getLogger(__name__)
 
 # WinAPI bindings for Windows-specific codepath
@@ -232,14 +233,16 @@
             # is closed).
             self._write_handle = os.fdopen(msvcrt.open_osfhandle(write_to_child, 0), "wb")
             self._read_handle = os.fdopen(msvcrt.open_osfhandle(read_from_child, 0), "rb")
         else:
             self._write_handle = os.fdopen(write_to_child, "wb")
             self._read_handle = os.fdopen(read_from_child, "rb")
 
+        self._send(sys.path)
+
         return self
 
     def __exit__(self, exc_type, exc_val, exc_tb):
         # Send the signal (a blank line) to the child to tell it that it's time to stop.
         self._write_handle.write(b"\n")
         self._write_handle.flush()
 
@@ -279,41 +282,37 @@
         """
         Call a function in the child Python. Retrieve its return value. Usage of this method is identical to that
         of the :func:`call` function.
         """
         if self._child is None:
             raise RuntimeError("An isolated.Python object must be used in a 'with' clause.")
 
-        # Send 5 lines to the child process: The function's code attribute, its default args and kwargs, and its actual
-        # args and kwargs, all serialised.
-        self._write_handle.writelines([
-            b64encode(dumps(function.__code__)), b"\n",
-            b64encode(dumps(function.__defaults__)), b"\n",
-            b64encode(dumps(function.__kwdefaults__)), b"\n",
-            b64encode(dumps(args)), b"\n",
-            b64encode(dumps(kwargs)), b"\n",
-        ])  # yapf: disable
-
-        # Flushing is very important. Without it, the data is not sent but forever sits in a buffer so that the child is
-        # forever waiting for its data and the parent in turn is forever waiting for the child's response.
-        self._write_handle.flush()
+        self._send(function.__code__, function.__defaults__, function.__kwdefaults__, args, kwargs)
 
         # Read a single line of output back from the child. This contains if the function worked and either its return
         # value or a traceback. This will block indefinitely until it receives a '\n' byte.
         ok, output = loads(b64decode(self._read_handle.readline()))
 
         # If all went well, then ``output`` is the return value.
         if ok:
             return output
 
         # Otherwise an error happened and ``output`` is a string-ified stacktrace. Raise an error appending the
         # stacktrace. Having the output in this order gives a nice fluent transition from parent to child in the stack
         # trace.
         raise RuntimeError(f"Child process call to {function.__name__}() failed with:\n" + output)
 
+    def _send(self, *objects):
+        for object in objects:
+            self._write_handle.write(b64encode(dumps(object)))
+            self._write_handle.write(b"\n")
+        # Flushing is very important. Without it, the data is not sent but forever sits in a buffer so that the child is
+        # forever waiting for its data and the parent in turn is forever waiting for the child's response.
+        self._write_handle.flush()
+
 
 def call(function, *args, **kwargs):
     r"""
     Call a function with arguments in a separate child Python. Retrieve its return value.
 
     Args:
         function:
```

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/README.rst` & `pyinstaller-5.9.0/PyInstaller/lib/README.rst`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/__main__.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/__main__.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/_compat.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/_compat.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/find_modules.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/find_modules.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/modulegraph.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/modulegraph.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/util.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/util.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/lib/modulegraph/zipio.py` & `pyinstaller-5.9.0/PyInstaller/lib/modulegraph/zipio.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,418 +1,418 @@
-"""
-A helper module that can work with paths
-that can refer to data inside a zipfile
-
-XXX: Need to determine if isdir("zipfile.zip")
-should return True or False. Currently returns
-True, but that might do the wrong thing with
-data-files that are zipfiles.
-"""
-import os as _os
-import zipfile as _zipfile
-import errno as _errno
-import time as _time
-import sys as _sys
-import stat as _stat
-
-_DFLT_DIR_MODE = (
-    _stat.S_IXOTH
-    | _stat.S_IXGRP
-    | _stat.S_IXUSR
-    | _stat.S_IROTH
-    | _stat.S_IRGRP
-    | _stat.S_IRUSR)
-
-_DFLT_FILE_MODE = (
-    _stat.S_IROTH
-    | _stat.S_IRGRP
-    | _stat.S_IRUSR)
-
-
-if _sys.version_info[0] == 2:
-    from StringIO import StringIO as _BaseStringIO
-    from StringIO import StringIO as _BaseBytesIO
-
-    class _StringIO (_BaseStringIO):
-        def __enter__(self):
-            return self
-
-        def __exit__(self, exc_type, exc_value, traceback):
-            self.close()
-            return False
-
-    class _BytesIO (_BaseBytesIO):
-        def __enter__(self):
-            return self
-
-        def __exit__(self, exc_type, exc_value, traceback):
-            self.close()
-            return False
-
-else:
-    from io import StringIO as _StringIO
-    from io import BytesIO as _BytesIO
-
-
-def _locate(path):
-    full_path = path
-    if _os.path.exists(path):
-        return path, None
-
-    else:
-        rest = []
-        root = _os.path.splitdrive(path)
-        while path and path != root:
-            path, bn = _os.path.split(path)
-            rest.append(bn)
-            if _os.path.exists(path):
-                break
-
-        if path == root:
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        if not _os.path.isfile(path):
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        rest.reverse()
-        return path, '/'.join(rest).strip('/')
-
-
-_open = open
-
-
-def open(path, mode='r'):
-    if 'w' in mode or 'a' in mode:
-        raise IOError(
-            _errno.EINVAL, path, "Write access not supported")
-    elif 'r+' in mode:
-        raise IOError(
-            _errno.EINVAL, path, "Write access not supported")
-
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        return _open(path, mode)
-
-    else:
-        try:
-            zf = _zipfile.ZipFile(path, 'r')
-
-        except _zipfile.error:
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        try:
-            data = zf.read(rest)
-        except (_zipfile.error, KeyError):
-            zf.close()
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-        zf.close()
-
-        if mode == 'rb':
-            return _BytesIO(data)
-
-        else:
-            if _sys.version_info[0] == 3:
-                data = data.decode('ascii')
-
-            return _StringIO(data)
-
-
-def listdir(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest and not _os.path.isfile(path):
-        return _os.listdir(path)
-
-    else:
-        try:
-            zf = _zipfile.ZipFile(path, 'r')
-
-        except _zipfile.error:
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        result = set()
-        seen = False
-        try:
-            for nm in zf.namelist():
-                if rest is None:
-                    seen = True
-                    value = nm.split('/')[0]
-                    if value:
-                        result.add(value)
-
-                elif nm.startswith(rest):
-                    if nm == rest:
-                        seen = True
-                        value = ''
-                        pass
-                    elif nm[len(rest)] == '/':
-                        seen = True
-                        value = nm[len(rest)+1:].split('/')[0]
-                    else:
-                        value = None
-
-                    if value:
-                        result.add(value)
-        except _zipfile.error:
-            zf.close()
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        zf.close()
-
-        if not seen:
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        return list(result)
-
-
-def isfile(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        ok = _os.path.isfile(path)
-        if ok:
-            try:
-                zf = _zipfile.ZipFile(path, 'r')
-                return False
-            except (_zipfile.error, IOError):
-                return True
-        return False
-
-    zf = None
-    try:
-        zf = _zipfile.ZipFile(path, 'r')
-        zf.getinfo(rest)
-        zf.close()
-        return True
-    except (KeyError, _zipfile.error):
-        if zf is not None:
-            zf.close()
-
-        # Check if this is a directory
-        try:
-            zf.getinfo(rest + '/')
-        except KeyError:
-            pass
-        else:
-            return False
-
-        rest = rest + '/'
-        for nm in zf.namelist():
-            if nm.startswith(rest):
-                # Directory
-                return False
-
-        # No trace in zipfile
-        raise IOError(
-            _errno.ENOENT, full_path,
-            "No such file or directory")
-
-
-def isdir(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        ok = _os.path.isdir(path)
-        if not ok:
-            try:
-                zf = _zipfile.ZipFile(path, 'r')
-            except (_zipfile.error, IOError):
-                return False
-            return True
-        return True
-
-    zf = None
-    try:
-        try:
-            zf = _zipfile.ZipFile(path)
-        except _zipfile.error:
-            raise IOError(
-                _errno.ENOENT, full_path,
-                "No such file or directory")
-
-        try:
-            zf.getinfo(rest)
-        except KeyError:
-            pass
-        else:
-            # File found
-            return False
-
-        rest = rest + '/'
-        try:
-            zf.getinfo(rest)
-        except KeyError:
-            pass
-        else:
-            # Directory entry found
-            return True
-
-        for nm in zf.namelist():
-            if nm.startswith(rest):
-                return True
-
-        raise IOError(
-            _errno.ENOENT, full_path,
-            "No such file or directory")
-    finally:
-        if zf is not None:
-            zf.close()
-
-
-def islink(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        return _os.path.islink(path)
-
-    try:
-        zf = _zipfile.ZipFile(path)
-    except _zipfile.error:
-        raise IOError(
-            _errno.ENOENT, full_path,
-            "No such file or directory")
-    try:
-        try:
-            zf.getinfo(rest)
-        except KeyError:
-            pass
-        else:
-            # File
-            return False
-
-        rest += '/'
-        try:
-            zf.getinfo(rest)
-        except KeyError:
-            pass
-        else:
-            # Directory
-            return False
-
-        for nm in zf.namelist():
-            if nm.startswith(rest):
-                # Directory without listing
-                return False
-
-        raise IOError(
-            _errno.ENOENT, full_path,
-            "No such file or directory")
-
-    finally:
-        zf.close()
-
-
-def readlink(path):
-    full_path = path
-    path, rest = _locate(path)
-    if rest:
-        # No symlinks inside zipfiles
-        raise OSError(
-            _errno.ENOENT, full_path,
-            "No such file or directory")
-
-    return _os.readlink(path)
-
-
-def getmode(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        return _stat.S_IMODE(_os.stat(path).st_mode)
-
-    zf = None
-    try:
-        zf = _zipfile.ZipFile(path)
-        info = None
-
-        try:
-            info = zf.getinfo(rest)
-        except KeyError:
-            pass
-
-        if info is None:
-            try:
-                info = zf.getinfo(rest + '/')
-            except KeyError:
-                pass
-
-        if info is None:
-            rest = rest + '/'
-            for nm in zf.namelist():
-                if nm.startswith(rest):
-                    break
-            else:
-                raise IOError(
-                    _errno.ENOENT, full_path,
-                    "No such file or directory")
-
-            # Directory exists, but has no entry of its own.
-            return _DFLT_DIR_MODE
-
-        # The mode is stored without file-type in external_attr.
-        if (info.external_attr >> 16) != 0:
-            return _stat.S_IMODE(info.external_attr >> 16)
-        else:
-            return _DFLT_FILE_MODE
-
-    finally:
-        if zf is not None:
-            zf.close()
-
-
-def getmtime(path):
-    full_path = path
-    path, rest = _locate(path)
-    if not rest:
-        return _os.path.getmtime(path)
-
-    zf = None
-    try:
-        zf = _zipfile.ZipFile(path)
-        info = None
-
-        try:
-            info = zf.getinfo(rest)
-        except KeyError:
-            pass
-
-        if info is None:
-            try:
-                info = zf.getinfo(rest + '/')
-            except KeyError:
-                pass
-
-        if info is None:
-            rest = rest + '/'
-            for nm in zf.namelist():
-                if nm.startswith(rest):
-                    break
-            else:
-                raise IOError(
-                    _errno.ENOENT, full_path,
-                    "No such file or directory")
-
-            # Directory exists, but has no entry of its
-            # own, fake mtime by using the timestamp of
-            # the zipfile itself.
-            return _os.path.getmtime(path)
-
-        return _time.mktime(info.date_time + (0, 0, -1))
-
-    finally:
-        if zf is not None:
-            zf.close()
+"""
+A helper module that can work with paths
+that can refer to data inside a zipfile
+
+XXX: Need to determine if isdir("zipfile.zip")
+should return True or False. Currently returns
+True, but that might do the wrong thing with
+data-files that are zipfiles.
+"""
+import os as _os
+import zipfile as _zipfile
+import errno as _errno
+import time as _time
+import sys as _sys
+import stat as _stat
+
+_DFLT_DIR_MODE = (
+    _stat.S_IXOTH
+    | _stat.S_IXGRP
+    | _stat.S_IXUSR
+    | _stat.S_IROTH
+    | _stat.S_IRGRP
+    | _stat.S_IRUSR)
+
+_DFLT_FILE_MODE = (
+    _stat.S_IROTH
+    | _stat.S_IRGRP
+    | _stat.S_IRUSR)
+
+
+if _sys.version_info[0] == 2:
+    from StringIO import StringIO as _BaseStringIO
+    from StringIO import StringIO as _BaseBytesIO
+
+    class _StringIO (_BaseStringIO):
+        def __enter__(self):
+            return self
+
+        def __exit__(self, exc_type, exc_value, traceback):
+            self.close()
+            return False
+
+    class _BytesIO (_BaseBytesIO):
+        def __enter__(self):
+            return self
+
+        def __exit__(self, exc_type, exc_value, traceback):
+            self.close()
+            return False
+
+else:
+    from io import StringIO as _StringIO
+    from io import BytesIO as _BytesIO
+
+
+def _locate(path):
+    full_path = path
+    if _os.path.exists(path):
+        return path, None
+
+    else:
+        rest = []
+        root = _os.path.splitdrive(path)
+        while path and path != root:
+            path, bn = _os.path.split(path)
+            rest.append(bn)
+            if _os.path.exists(path):
+                break
+
+        if path == root:
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        if not _os.path.isfile(path):
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        rest.reverse()
+        return path, '/'.join(rest).strip('/')
+
+
+_open = open
+
+
+def open(path, mode='r'):
+    if 'w' in mode or 'a' in mode:
+        raise IOError(
+            _errno.EINVAL, path, "Write access not supported")
+    elif 'r+' in mode:
+        raise IOError(
+            _errno.EINVAL, path, "Write access not supported")
+
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        return _open(path, mode)
+
+    else:
+        try:
+            zf = _zipfile.ZipFile(path, 'r')
+
+        except _zipfile.BadZipFile:
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        try:
+            data = zf.read(rest)
+        except (_zipfile.BadZipFile, KeyError):
+            zf.close()
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+        zf.close()
+
+        if mode == 'rb':
+            return _BytesIO(data)
+
+        else:
+            if _sys.version_info[0] == 3:
+                data = data.decode('ascii')
+
+            return _StringIO(data)
+
+
+def listdir(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest and not _os.path.isfile(path):
+        return _os.listdir(path)
+
+    else:
+        try:
+            zf = _zipfile.ZipFile(path, 'r')
+
+        except _zipfile.BadZipFile:
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        result = set()
+        seen = False
+        try:
+            for nm in zf.namelist():
+                if rest is None:
+                    seen = True
+                    value = nm.split('/')[0]
+                    if value:
+                        result.add(value)
+
+                elif nm.startswith(rest):
+                    if nm == rest:
+                        seen = True
+                        value = ''
+                        pass
+                    elif nm[len(rest)] == '/':
+                        seen = True
+                        value = nm[len(rest)+1:].split('/')[0]
+                    else:
+                        value = None
+
+                    if value:
+                        result.add(value)
+        except _zipfile.BadZipFile:
+            zf.close()
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        zf.close()
+
+        if not seen:
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        return list(result)
+
+
+def isfile(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        ok = _os.path.isfile(path)
+        if ok:
+            try:
+                zf = _zipfile.ZipFile(path, 'r')
+                return False
+            except (_zipfile.BadZipFile, IOError):
+                return True
+        return False
+
+    zf = None
+    try:
+        zf = _zipfile.ZipFile(path, 'r')
+        zf.getinfo(rest)
+        zf.close()
+        return True
+    except (KeyError, _zipfile.BadZipFile):
+        if zf is not None:
+            zf.close()
+
+        # Check if this is a directory
+        try:
+            zf.getinfo(rest + '/')
+        except KeyError:
+            pass
+        else:
+            return False
+
+        rest = rest + '/'
+        for nm in zf.namelist():
+            if nm.startswith(rest):
+                # Directory
+                return False
+
+        # No trace in zipfile
+        raise IOError(
+            _errno.ENOENT, full_path,
+            "No such file or directory")
+
+
+def isdir(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        ok = _os.path.isdir(path)
+        if not ok:
+            try:
+                zf = _zipfile.ZipFile(path, 'r')
+            except (_zipfile.BadZipFile, IOError):
+                return False
+            return True
+        return True
+
+    zf = None
+    try:
+        try:
+            zf = _zipfile.ZipFile(path)
+        except _zipfile.BadZipFile:
+            raise IOError(
+                _errno.ENOENT, full_path,
+                "No such file or directory")
+
+        try:
+            zf.getinfo(rest)
+        except KeyError:
+            pass
+        else:
+            # File found
+            return False
+
+        rest = rest + '/'
+        try:
+            zf.getinfo(rest)
+        except KeyError:
+            pass
+        else:
+            # Directory entry found
+            return True
+
+        for nm in zf.namelist():
+            if nm.startswith(rest):
+                return True
+
+        raise IOError(
+            _errno.ENOENT, full_path,
+            "No such file or directory")
+    finally:
+        if zf is not None:
+            zf.close()
+
+
+def islink(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        return _os.path.islink(path)
+
+    try:
+        zf = _zipfile.ZipFile(path)
+    except _zipfile.BadZipFile:
+        raise IOError(
+            _errno.ENOENT, full_path,
+            "No such file or directory")
+    try:
+        try:
+            zf.getinfo(rest)
+        except KeyError:
+            pass
+        else:
+            # File
+            return False
+
+        rest += '/'
+        try:
+            zf.getinfo(rest)
+        except KeyError:
+            pass
+        else:
+            # Directory
+            return False
+
+        for nm in zf.namelist():
+            if nm.startswith(rest):
+                # Directory without listing
+                return False
+
+        raise IOError(
+            _errno.ENOENT, full_path,
+            "No such file or directory")
+
+    finally:
+        zf.close()
+
+
+def readlink(path):
+    full_path = path
+    path, rest = _locate(path)
+    if rest:
+        # No symlinks inside zipfiles
+        raise OSError(
+            _errno.ENOENT, full_path,
+            "No such file or directory")
+
+    return _os.readlink(path)
+
+
+def getmode(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        return _stat.S_IMODE(_os.stat(path).st_mode)
+
+    zf = None
+    try:
+        zf = _zipfile.ZipFile(path)
+        info = None
+
+        try:
+            info = zf.getinfo(rest)
+        except KeyError:
+            pass
+
+        if info is None:
+            try:
+                info = zf.getinfo(rest + '/')
+            except KeyError:
+                pass
+
+        if info is None:
+            rest = rest + '/'
+            for nm in zf.namelist():
+                if nm.startswith(rest):
+                    break
+            else:
+                raise IOError(
+                    _errno.ENOENT, full_path,
+                    "No such file or directory")
+
+            # Directory exists, but has no entry of its own.
+            return _DFLT_DIR_MODE
+
+        # The mode is stored without file-type in external_attr.
+        if (info.external_attr >> 16) != 0:
+            return _stat.S_IMODE(info.external_attr >> 16)
+        else:
+            return _DFLT_FILE_MODE
+
+    finally:
+        if zf is not None:
+            zf.close()
+
+
+def getmtime(path):
+    full_path = path
+    path, rest = _locate(path)
+    if not rest:
+        return _os.path.getmtime(path)
+
+    zf = None
+    try:
+        zf = _zipfile.ZipFile(path)
+        info = None
+
+        try:
+            info = zf.getinfo(rest)
+        except KeyError:
+            pass
+
+        if info is None:
+            try:
+                info = zf.getinfo(rest + '/')
+            except KeyError:
+                pass
+
+        if info is None:
+            rest = rest + '/'
+            for nm in zf.namelist():
+                if nm.startswith(rest):
+                    break
+            else:
+                raise IOError(
+                    _errno.ENOENT, full_path,
+                    "No such file or directory")
+
+            # Directory exists, but has no entry of its
+            # own, fake mtime by using the timestamp of
+            # the zipfile itself.
+            return _os.path.getmtime(path)
+
+        return _time.mktime(info.date_time + (0, 0, -1))
+
+    finally:
+        if zf is not None:
+            zf.close()
```

### Comparing `pyinstaller-5.8.0/PyInstaller/loader/pyiboot01_bootstrap.py` & `pyinstaller-5.9.0/PyInstaller/loader/pyiboot01_bootstrap.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/loader/pyimod01_archive.py` & `pyinstaller-5.9.0/PyInstaller/loader/pyimod01_archive.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/loader/pyimod02_importers.py` & `pyinstaller-5.9.0/PyInstaller/loader/pyimod02_importers.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/loader/pyimod03_ctypes.py` & `pyinstaller-5.9.0/PyInstaller/loader/pyimod03_ctypes.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/loader/pyimod04_pywin32.py` & `pyinstaller-5.9.0/PyInstaller/loader/pyimod04_pywin32.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/log.py` & `pyinstaller-5.9.0/PyInstaller/log.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/cliutils/archive_viewer.py` & `pyinstaller-5.9.0/PyInstaller/utils/cliutils/archive_viewer.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/cliutils/bindepend.py` & `pyinstaller-5.9.0/PyInstaller/utils/cliutils/bindepend.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/cliutils/grab_version.py` & `pyinstaller-5.9.0/PyInstaller/utils/cliutils/grab_version.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/cliutils/makespec.py` & `pyinstaller-5.9.0/PyInstaller/utils/cliutils/makespec.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/cliutils/set_version.py` & `pyinstaller-5.9.0/PyInstaller/utils/cliutils/set_version.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/conftest.py` & `pyinstaller-5.9.0/PyInstaller/utils/conftest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/git.py` & `pyinstaller-5.9.0/PyInstaller/utils/git.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/__init__.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/__init__.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/conda.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/conda.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/django.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/django.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/gi.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/gi.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/qt/__init__.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/qt/__init__.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/qt/_modules_info.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/qt/_modules_info.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/tcl_tk.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/tcl_tk.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/hooks/win32.py` & `pyinstaller-5.9.0/PyInstaller/utils/hooks/win32.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/misc.py` & `pyinstaller-5.9.0/PyInstaller/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/osx.py` & `pyinstaller-5.9.0/PyInstaller/utils/osx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/run_tests.py` & `pyinstaller-5.9.0/PyInstaller/utils/run_tests.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/tests.py` & `pyinstaller-5.9.0/PyInstaller/utils/tests.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/win32/icon.py` & `pyinstaller-5.9.0/PyInstaller/utils/win32/icon.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/win32/versioninfo.py` & `pyinstaller-5.9.0/PyInstaller/utils/win32/versioninfo.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/win32/winmanifest.py` & `pyinstaller-5.9.0/PyInstaller/utils/win32/winmanifest.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/win32/winresource.py` & `pyinstaller-5.9.0/PyInstaller/utils/win32/winresource.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/PyInstaller/utils/win32/winutils.py` & `pyinstaller-5.9.0/PyInstaller/utils/win32/winutils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/README.rst` & `pyinstaller-5.9.0/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -133,21 +133,21 @@
 pyinstaller`` provided that you have an appropriate C compiler (typically
 either ``gcc`` or ``clang``) and zlib's development headers already installed.
 
 
 Support
 -------
 
-- Official debugging guide: https://pyinstaller.org/en/v5.8.0/when-things-go-wrong.html
+- Official debugging guide: https://pyinstaller.org/en/v5.9.0/when-things-go-wrong.html
 - Assorted user contributed help topics: https://github.com/pyinstaller/pyinstaller/wiki
 - Web based Q&A forums: https://github.com/pyinstaller/pyinstaller/discussions
 - Email based Q&A forums: https://groups.google.com/g/pyinstaller
 
 
 Changes in this Release
 -----------------------
 
 You can find a detailed list of changes in this release
 in the `Changelog`_ section of the manual.
 
-.. _`manual`: https://pyinstaller.org/en/v5.8.0/
-.. _`Changelog`: https://pyinstaller.org/en/v5.8.0/CHANGES.html
+.. _`manual`: https://pyinstaller.org/en/v5.9.0/
+.. _`Changelog`: https://pyinstaller.org/en/v5.9.0/CHANGES.html
```

### Comparing `pyinstaller-5.8.0/bootloader/src/main.c` & `pyinstaller-5.9.0/bootloader/src/main.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/mkdtemp.h` & `pyinstaller-5.9.0/bootloader/src/mkdtemp.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_apple_events.c` & `pyinstaller-5.9.0/bootloader/src/pyi_apple_events.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_apple_events.h` & `pyinstaller-5.9.0/bootloader/src/pyi_apple_events.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_archive.c` & `pyinstaller-5.9.0/bootloader/src/pyi_archive.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_archive.h` & `pyinstaller-5.9.0/bootloader/src/pyi_archive.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_exception_dialog.c` & `pyinstaller-5.9.0/bootloader/src/pyi_exception_dialog.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_exception_dialog.h` & `pyinstaller-5.9.0/bootloader/src/pyi_exception_dialog.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_global.c` & `pyinstaller-5.9.0/bootloader/src/pyi_global.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_global.h` & `pyinstaller-5.9.0/bootloader/src/pyi_global.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_launch.c` & `pyinstaller-5.9.0/bootloader/src/pyi_launch.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_launch.h` & `pyinstaller-5.9.0/bootloader/src/pyi_launch.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_main.c` & `pyinstaller-5.9.0/bootloader/src/pyi_main.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_main.h` & `pyinstaller-5.9.0/bootloader/src/pyi_main.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_path.c` & `pyinstaller-5.9.0/bootloader/src/pyi_path.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_path.h` & `pyinstaller-5.9.0/bootloader/src/pyi_path.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_python.c` & `pyinstaller-5.9.0/bootloader/src/pyi_python.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_python.h` & `pyinstaller-5.9.0/bootloader/src/pyi_python.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_pythonlib.c` & `pyinstaller-5.9.0/bootloader/src/pyi_pythonlib.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_pythonlib.h` & `pyinstaller-5.9.0/bootloader/src/pyi_pythonlib.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_splash.c` & `pyinstaller-5.9.0/bootloader/src/pyi_splash.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_splash.h` & `pyinstaller-5.9.0/bootloader/src/pyi_splash.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_splashlib.c` & `pyinstaller-5.9.0/bootloader/src/pyi_splashlib.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_splashlib.h` & `pyinstaller-5.9.0/bootloader/src/pyi_splashlib.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_utils.c` & `pyinstaller-5.9.0/bootloader/src/pyi_utils.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_utils.h` & `pyinstaller-5.9.0/bootloader/src/pyi_utils.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_win32_utils.c` & `pyinstaller-5.9.0/bootloader/src/pyi_win32_utils.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/src/pyi_win32_utils.h` & `pyinstaller-5.9.0/bootloader/src/pyi_win32_utils.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/tests/test_launch.c` & `pyinstaller-5.9.0/bootloader/tests/test_launch.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/tests/test_path.c` & `pyinstaller-5.9.0/bootloader/tests/test_path.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/tests/wscript` & `pyinstaller-5.9.0/bootloader/tests/wscript`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/tools/strip.py` & `pyinstaller-5.9.0/bootloader/tools/strip.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waf` & `pyinstaller-5.9.0/bootloader/waf`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Build.py` & `pyinstaller-5.9.0/bootloader/waflib/Build.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/ConfigSet.py` & `pyinstaller-5.9.0/bootloader/waflib/ConfigSet.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Configure.py` & `pyinstaller-5.9.0/bootloader/waflib/Configure.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Context.py` & `pyinstaller-5.9.0/bootloader/waflib/Context.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Errors.py` & `pyinstaller-5.9.0/bootloader/waflib/Errors.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Logs.py` & `pyinstaller-5.9.0/bootloader/waflib/Logs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Node.py` & `pyinstaller-5.9.0/bootloader/waflib/Node.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Options.py` & `pyinstaller-5.9.0/bootloader/waflib/Options.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Runner.py` & `pyinstaller-5.9.0/bootloader/waflib/Runner.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Scripting.py` & `pyinstaller-5.9.0/bootloader/waflib/Scripting.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Task.py` & `pyinstaller-5.9.0/bootloader/waflib/Task.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/TaskGen.py` & `pyinstaller-5.9.0/bootloader/waflib/TaskGen.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/asm.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/asm.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/bison.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/bison.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c_aliases.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c_aliases.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c_config.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c_config.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c_osx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c_osx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c_preproc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c_preproc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/c_tests.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/c_tests.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/ccroot.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/ccroot.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/clang.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/clang.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/clangxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/clangxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_c.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_c.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_cxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_cxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_d.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_d.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/compiler_fc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/compiler_fc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/cs.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/cs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/cxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/cxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/d.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/d.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/d_config.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/d_config.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/d_scan.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/d_scan.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/dbus.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/dbus.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/dmd.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/dmd.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/errcheck.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/errcheck.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/fc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/fc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/fc_config.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/fc_config.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/fc_scan.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/fc_scan.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/flex.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/flex.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/g95.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/g95.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/gcc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/gcc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/gdc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/gdc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/gfortran.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/gfortran.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/glib2.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/glib2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/gnu_dirs.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/gnu_dirs.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/gxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/gxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/icc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/icc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/icpc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/icpc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/ifort.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/ifort.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/intltool.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/intltool.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/irixcc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/irixcc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/javaw.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/javaw.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/ldc2.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/ldc2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/lua.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/lua.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/md5_tstamp.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/md5_tstamp.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/msvc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/msvc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/nasm.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/nasm.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/perl.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/perl.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/python.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/python.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/qt5.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/qt5.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/ruby.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/ruby.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/suncc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/suncc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/suncxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/suncxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/tex.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/tex.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/vala.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/vala.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/waf_unit_test.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/waf_unit_test.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/winres.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/winres.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/xlc.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/xlc.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Tools/xlcxx.py` & `pyinstaller-5.9.0/bootloader/waflib/Tools/xlcxx.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/Utils.py` & `pyinstaller-5.9.0/bootloader/waflib/Utils.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/ansiterm.py` & `pyinstaller-5.9.0/bootloader/waflib/ansiterm.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/fixpy2.py` & `pyinstaller-5.9.0/bootloader/waflib/fixpy2.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/waflib/processor.py` & `pyinstaller-5.9.0/bootloader/waflib/processor.py`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/wscript` & `pyinstaller-5.9.0/bootloader/wscript`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/adler32.c` & `pyinstaller-5.9.0/bootloader/zlib/adler32.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/crc32.c` & `pyinstaller-5.9.0/bootloader/zlib/crc32.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/crc32.h` & `pyinstaller-5.9.0/bootloader/zlib/crc32.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/gzguts.h` & `pyinstaller-5.9.0/bootloader/zlib/gzguts.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inffast.c` & `pyinstaller-5.9.0/bootloader/zlib/inffast.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inffixed.h` & `pyinstaller-5.9.0/bootloader/zlib/inffixed.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inflate.c` & `pyinstaller-5.9.0/bootloader/zlib/inflate.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inflate.h` & `pyinstaller-5.9.0/bootloader/zlib/inflate.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inftrees.c` & `pyinstaller-5.9.0/bootloader/zlib/inftrees.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/inftrees.h` & `pyinstaller-5.9.0/bootloader/zlib/inftrees.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/zconf.h` & `pyinstaller-5.9.0/bootloader/zlib/zconf.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/zlib.h` & `pyinstaller-5.9.0/bootloader/zlib/zlib.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/zutil.c` & `pyinstaller-5.9.0/bootloader/zlib/zutil.c`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/bootloader/zlib/zutil.h` & `pyinstaller-5.9.0/bootloader/zlib/zutil.h`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/pyinstaller.egg-info/PKG-INFO` & `pyinstaller-5.9.0/pyinstaller.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyinstaller
-Version: 5.8.0
+Version: 5.9.0
 Summary: PyInstaller bundles a Python application and all its dependencies into a single package.
 Home-page: https://www.pyinstaller.org/
 Author: Hartmut Goebel, Giovanni Bajo, David Vierra, David Cortesi, Martin Zibricky
 License: GPLv2-or-later with a special exception which allows to use PyInstaller to build and distribute non-free programs (including commercial ones)
 Project-URL: Source, https://github.com/pyinstaller/pyinstaller
 Keywords: packaging, app, apps, bundle, convert, standalone, executable,pyinstaller, cxfreeze, freeze, py2exe, py2app, bbfreeze
 Classifier: Development Status :: 6 - Mature
@@ -179,21 +179,21 @@
 pyinstaller`` provided that you have an appropriate C compiler (typically
 either ``gcc`` or ``clang``) and zlib's development headers already installed.
 
 
 Support
 -------
 
-- Official debugging guide: https://pyinstaller.org/en/v5.8.0/when-things-go-wrong.html
+- Official debugging guide: https://pyinstaller.org/en/v5.9.0/when-things-go-wrong.html
 - Assorted user contributed help topics: https://github.com/pyinstaller/pyinstaller/wiki
 - Web based Q&A forums: https://github.com/pyinstaller/pyinstaller/discussions
 - Email based Q&A forums: https://groups.google.com/g/pyinstaller
 
 
 Changes in this Release
 -----------------------
 
 You can find a detailed list of changes in this release
 in the `Changelog`_ section of the manual.
 
-.. _`manual`: https://pyinstaller.org/en/v5.8.0/
-.. _`Changelog`: https://pyinstaller.org/en/v5.8.0/CHANGES.html
+.. _`manual`: https://pyinstaller.org/en/v5.9.0/
+.. _`Changelog`: https://pyinstaller.org/en/v5.9.0/CHANGES.html
```

### Comparing `pyinstaller-5.8.0/pyproject.toml` & `pyinstaller-5.9.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `pyinstaller-5.8.0/setup.cfg` & `pyinstaller-5.9.0/setup.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -43,26 +43,39 @@
 	Topic :: Software Development :: Interpreters
 	Topic :: Software Development :: Libraries :: Python Modules
 	Topic :: System :: Installation/Setup
 	Topic :: System :: Software Distribution
 	Topic :: Utilities
 
 [options]
+packages = find:
 zip_safe = False
 include_package_data = False
 python_requires = >=3.7, <3.12
 install_requires = 
 	setuptools >= 42.0.0
 	altgraph
 	pefile >= 2022.5.30 ; sys_platform == 'win32'
 	pywin32-ctypes >= 0.2.0 ; sys_platform == 'win32'
 	macholib >= 1.8 ; sys_platform == 'darwin'
 	pyinstaller-hooks-contrib >= 2021.4
 	importlib-metadata >= 1.4 ; python_version < '3.8'
 
+[options.packages.find]
+include = 
+	PyInstaller
+	PyInstaller.*
+
+[options.package_data]
+PyInstaller = 
+	bootloader/*/*
+	fake-modules/*.py
+	hooks/rthooks.dat
+	lib/README.rst
+
 [options.extras_require]
 hook_testing = 
 	pytest >= 2.7.3
 	execnet >= 1.5.0
 	psutil
 encryption = 
 	tinyaes>=1.0.0
```

### Comparing `pyinstaller-5.8.0/setup.py` & `pyinstaller-5.9.0/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 #-----------------------------------------------------------------------------
 
 import sys
 import os
 import subprocess
 from typing import Type
 
-from setuptools import setup, find_packages
+from setuptools import setup
 
 #-- plug-in building the bootloader
 
 from distutils.core import Command
 from distutils.command.build import build
 
 # Hack required to allow compat to not fail when pypiwin32 isn't found
@@ -279,19 +279,8 @@
     cmdclass={
         'build_bootloader': build_bootloader,
         'build': MyBuild,
         **wheel_commands,
         'bdist_wheels': bdist_wheels,
         **bdist_egg_override,
     },
-    packages=find_packages(include=["PyInstaller", "PyInstaller.*"]),
-    package_data={
-        "PyInstaller": [
-            # Include all bootloaders in wheels by default.
-            "bootloader/*/*",
-            # These files need to be explicitly included as well.
-            "fake-modules/*.py",
-            "hooks/rthooks.dat",
-            "lib/README.rst",
-        ],
-    },
 )
```

