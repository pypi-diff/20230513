# Comparing `tmp/ltchiptool-4.0.1.tar.gz` & `tmp/ltchiptool-4.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ltchiptool-4.0.1.tar", max compression
+gzip compressed data, was "ltchiptool-4.1.0.tar", max compression
```

## Comparing `ltchiptool-4.0.1.tar` & `ltchiptool-4.1.0.tar`

### file list

```diff
@@ -1,99 +1,101 @@
--rw-r--r--   0        0        0     1076 2023-04-28 12:18:48.404186 ltchiptool-4.0.1/LICENSE
--rw-r--r--   0        0        0     2384 2023-04-28 12:18:48.404186 ltchiptool-4.0.1/README.md
--rw-r--r--   0        0        0      376 2023-04-28 12:18:48.404186 ltchiptool-4.0.1/ltchiptool/__init__.py
--rw-r--r--   0        0        0     2339 2023-04-28 12:18:48.404186 ltchiptool-4.0.1/ltchiptool/__main__.py
--rw-r--r--   0        0        0     2517 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/dumptool.py
--rw-r--r--   0        0        0      908 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/elf2bin.py
--rw-r--r--   0        0        0      451 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/flash/__main__.py
--rw-r--r--   0        0        0     1724 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/flash/_utils.py
--rw-r--r--   0        0        0     1610 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/flash/file.py
--rw-r--r--   0        0        0     3157 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/flash/read.py
--rw-r--r--   0        0        0     7153 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/flash/write.py
--rw-r--r--   0        0        0      881 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/link2bin.py
--rw-r--r--   0        0        0     2331 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/list.py
--rw-r--r--   0        0        0      423 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/commands/soc.py
--rw-r--r--   0        0        0     2288 2023-04-28 12:19:10.672486 ltchiptool-4.0.1/ltchiptool/families.json
--rw-r--r--   0        0        0      127 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/__init__.py
--rw-r--r--   0        0        0     1459 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/__main__.py
--rw-r--r--   0        0        0     9477 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/ltchiptool-192x192.png
--rw-r--r--   0        0        0    15406 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.ico
--rw-r--r--   0        0        0    15229 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.wxui
--rw-r--r--   0        0        0    19629 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.xrc
--rw-r--r--   0        0        0     6048 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/main.py
--rw-r--r--   0        0        0       48 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/panels/__init__.py
--rw-r--r--   0        0        0     2017 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/panels/about.py
--rw-r--r--   0        0        0     3977 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/panels/base.py
--rw-r--r--   0        0        0    17080 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/panels/flash.py
--rw-r--r--   0        0        0     6937 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/panels/log.py
--rw-r--r--   0        0        0      789 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/utils.py
--rw-r--r--   0        0        0       47 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/work/__init__.py
--rw-r--r--   0        0        0      950 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/work/base.py
--rw-r--r--   0        0        0     6069 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/work/flash.py
--rw-r--r--   0        0        0     2528 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/gui/work/ports.py
--rw-r--r--   0        0        0      263 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/models/__init__.py
--rw-r--r--   0        0        0     3041 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/models/board.py
--rw-r--r--   0        0        0      155 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/models/enums.py
--rw-r--r--   0        0        0     5966 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/models/family.py
--rw-r--r--   0        0        0     3199 2023-04-28 12:19:10.668485 ltchiptool-4.0.1/ltchiptool/platform.json
--rw-r--r--   0        0        0      185 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/__init__.py
--rw-r--r--   0        0        0      111 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/__init__.py
--rw-r--r--   0        0        0     6198 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/binary.py
--rw-r--r--   0        0        0     6871 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/flash.py
--rw-r--r--   0        0        0      721 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/main.py
--rw-r--r--   0        0        0       48 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/util/__init__.py
--rw-r--r--   0        0        0    18071 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz/util/rtltool.py
--rw-r--r--   0        0        0      114 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz2/__init__.py
--rw-r--r--   0        0        0     2780 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz2/flash.py
--rw-r--r--   0        0        0      595 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz2/main.py
--rw-r--r--   0        0        0       49 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz2/util/__init__.py
--rw-r--r--   0        0        0    13040 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/ambz2/util/ambz2tool.py
--rw-r--r--   0        0        0      111 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/__init__.py
--rw-r--r--   0        0        0     9025 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/binary.py
--rw-r--r--   0        0        0     8305 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/bkpackager.py
--rw-r--r--   0        0        0     6820 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/flash.py
--rw-r--r--   0        0        0      723 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/main.py
--rw-r--r--   0        0        0      317 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/__init__.py
--rw-r--r--   0        0        0     7069 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/binary.py
--rw-r--r--   0        0        0     6175 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/crypto.py
--rw-r--r--   0        0        0      515 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/models.py
--rw-r--r--   0        0        0     2940 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/rbl.py
--rw-r--r--   0        0        0     2827 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/common.py
--rw-r--r--   0        0        0     6478 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/soc/interface.py
--rw-r--r--   0        0        0       48 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/__init__.py
--rw-r--r--   0        0        0     2408 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/bitint.py
--rw-r--r--   0        0        0     2727 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/cli.py
--rw-r--r--   0        0        0     5642 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/crc16.py
--rw-r--r--   0        0        0     2277 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/crypto.py
--rw-r--r--   0        0        0     6631 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/detection.py
--rw-r--r--   0        0        0     1987 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/dict.py
--rw-r--r--   0        0        0      252 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/env.py
--rw-r--r--   0        0        0     2420 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/fileio.py
--rw-r--r--   0        0        0     3591 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/flash.py
--rw-r--r--   0        0        0     3296 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/fwbinary.py
--rw-r--r--   0        0        0     6105 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/intbin.py
--rw-r--r--   0        0        0     4806 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/logging.py
--rw-r--r--   0        0        0     7308 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/lvm.py
--rw-r--r--   0        0        0     1368 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/misc.py
--rw-r--r--   0        0        0     1878 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/obj.py
--rw-r--r--   0        0        0      866 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/slice.py
--rw-r--r--   0        0        0     1612 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/util/toolchain.py
--rw-r--r--   0        0        0      772 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/ltchiptool/version.py
--rw-r--r--   0        0        0     1284 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/pyproject.toml
--rw-r--r--   0        0        0      172 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/__init__.py
--rw-r--r--   0        0        0      251 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/binpatch/__init__.py
--rw-r--r--   0        0        0      471 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/binpatch/apply.py
--rw-r--r--   0        0        0     1027 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/binpatch/bindiff.py
--rw-r--r--   0        0        0     1666 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/binpatch/diff32.py
--rw-r--r--   0        0        0     4306 2023-04-28 12:18:48.408187 ltchiptool-4.0.1/uf2tool/cli.py
--rw-r--r--   0        0        0      360 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/__init__.py
--rw-r--r--   0        0        0     4805 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/block.py
--rw-r--r--   0        0        0     5803 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/context.py
--rw-r--r--   0        0        0     2210 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/enums.py
--rw-r--r--   0        0        0     1256 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/flags.py
--rw-r--r--   0        0        0     3311 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/image.py
--rw-r--r--   0        0        0      778 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/partition.py
--rw-r--r--   0        0        0     4552 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/models/uf2.py
--rw-r--r--   0        0        0      124 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/upload/__init__.py
--rw-r--r--   0        0        0     4846 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/upload/esphome.py
--rw-r--r--   0        0        0     7219 2023-04-28 12:18:48.412186 ltchiptool-4.0.1/uf2tool/writer.py
--rw-r--r--   0        0        0     3733 1970-01-01 00:00:00.000000 ltchiptool-4.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1076 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/LICENSE
+-rw-r--r--   0        0        0     2384 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/README.md
+-rw-r--r--   0        0        0      376 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/__init__.py
+-rw-r--r--   0        0        0     2339 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/__main__.py
+-rw-r--r--   0        0        0     2517 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/dumptool.py
+-rw-r--r--   0        0        0      908 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/elf2bin.py
+-rw-r--r--   0        0        0      451 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/flash/__main__.py
+-rw-r--r--   0        0        0     1724 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/flash/_utils.py
+-rw-r--r--   0        0        0     1610 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/flash/file.py
+-rw-r--r--   0        0        0     3157 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/flash/read.py
+-rw-r--r--   0        0        0     7153 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/flash/write.py
+-rw-r--r--   0        0        0      881 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/link2bin.py
+-rw-r--r--   0        0        0     2331 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/list.py
+-rw-r--r--   0        0        0      423 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/commands/soc.py
+-rw-r--r--   0        0        0     2288 2023-05-13 15:36:04.671286 ltchiptool-4.1.0/ltchiptool/families.json
+-rw-r--r--   0        0        0      127 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/__init__.py
+-rw-r--r--   0        0        0     1459 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/__main__.py
+-rw-r--r--   0        0        0     9477 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/ltchiptool-192x192.png
+-rw-r--r--   0        0        0    15406 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.ico
+-rw-r--r--   0        0        0    26033 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.wxui
+-rw-r--r--   0        0        0    32878 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.xrc
+-rw-r--r--   0        0        0     6613 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/main.py
+-rw-r--r--   0        0        0       48 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/__init__.py
+-rw-r--r--   0        0        0     2017 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/about.py
+-rw-r--r--   0        0        0     4453 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/base.py
+-rw-r--r--   0        0        0    17255 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/flash.py
+-rw-r--r--   0        0        0     6995 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/log.py
+-rw-r--r--   0        0        0    11834 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/panels/upk.py
+-rw-r--r--   0        0        0      789 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/utils.py
+-rw-r--r--   0        0        0       47 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/work/__init__.py
+-rw-r--r--   0        0        0      950 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/work/base.py
+-rw-r--r--   0        0        0     6027 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/work/flash.py
+-rw-r--r--   0        0        0     2528 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/work/ports.py
+-rw-r--r--   0        0        0     4397 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/gui/work/upk.py
+-rw-r--r--   0        0        0      263 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/models/__init__.py
+-rw-r--r--   0        0        0     3041 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/models/board.py
+-rw-r--r--   0        0        0      155 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/models/enums.py
+-rw-r--r--   0        0        0     5966 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/models/family.py
+-rw-r--r--   0        0        0     3199 2023-05-13 15:36:04.671286 ltchiptool-4.1.0/ltchiptool/platform.json
+-rw-r--r--   0        0        0      185 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/__init__.py
+-rw-r--r--   0        0        0      111 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/__init__.py
+-rw-r--r--   0        0        0     6198 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/binary.py
+-rw-r--r--   0        0        0     6871 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/flash.py
+-rw-r--r--   0        0        0      721 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/main.py
+-rw-r--r--   0        0        0       48 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/util/__init__.py
+-rw-r--r--   0        0        0    18071 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz/util/rtltool.py
+-rw-r--r--   0        0        0      114 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz2/__init__.py
+-rw-r--r--   0        0        0     2780 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz2/flash.py
+-rw-r--r--   0        0        0      595 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz2/main.py
+-rw-r--r--   0        0        0       49 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz2/util/__init__.py
+-rw-r--r--   0        0        0    13040 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/ambz2/util/ambz2tool.py
+-rw-r--r--   0        0        0      111 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/__init__.py
+-rw-r--r--   0        0        0     9025 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/binary.py
+-rw-r--r--   0        0        0     8305 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/bkpackager.py
+-rw-r--r--   0        0        0     6820 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/flash.py
+-rw-r--r--   0        0        0      723 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/main.py
+-rw-r--r--   0        0        0      317 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/__init__.py
+-rw-r--r--   0        0        0     7069 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/binary.py
+-rw-r--r--   0        0        0     6175 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/crypto.py
+-rw-r--r--   0        0        0      515 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/models.py
+-rw-r--r--   0        0        0     2940 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/rbl.py
+-rw-r--r--   0        0        0     2827 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/common.py
+-rw-r--r--   0        0        0     6478 2023-05-13 15:35:47.743376 ltchiptool-4.1.0/ltchiptool/soc/interface.py
+-rw-r--r--   0        0        0       48 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/__init__.py
+-rw-r--r--   0        0        0     2408 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/bitint.py
+-rw-r--r--   0        0        0     2727 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/cli.py
+-rw-r--r--   0        0        0     5642 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/crc16.py
+-rw-r--r--   0        0        0     2277 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/crypto.py
+-rw-r--r--   0        0        0     6631 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/detection.py
+-rw-r--r--   0        0        0     1987 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/dict.py
+-rw-r--r--   0        0        0      252 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/env.py
+-rw-r--r--   0        0        0     2420 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/fileio.py
+-rw-r--r--   0        0        0     3591 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/flash.py
+-rw-r--r--   0        0        0     3296 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/fwbinary.py
+-rw-r--r--   0        0        0     6105 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/intbin.py
+-rw-r--r--   0        0        0     4845 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/logging.py
+-rw-r--r--   0        0        0     7308 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/lvm.py
+-rw-r--r--   0        0        0     1401 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/misc.py
+-rw-r--r--   0        0        0     1878 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/obj.py
+-rw-r--r--   0        0        0      866 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/slice.py
+-rw-r--r--   0        0        0     1612 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/util/toolchain.py
+-rw-r--r--   0        0        0      772 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/ltchiptool/version.py
+-rw-r--r--   0        0        0     1322 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/pyproject.toml
+-rw-r--r--   0        0        0      172 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/__init__.py
+-rw-r--r--   0        0        0      251 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/binpatch/__init__.py
+-rw-r--r--   0        0        0      471 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/binpatch/apply.py
+-rw-r--r--   0        0        0     1027 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/binpatch/bindiff.py
+-rw-r--r--   0        0        0     1666 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/binpatch/diff32.py
+-rw-r--r--   0        0        0     4306 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/cli.py
+-rw-r--r--   0        0        0      360 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/__init__.py
+-rw-r--r--   0        0        0     4805 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/block.py
+-rw-r--r--   0        0        0     5803 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/context.py
+-rw-r--r--   0        0        0     2210 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/enums.py
+-rw-r--r--   0        0        0     1256 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/flags.py
+-rw-r--r--   0        0        0     3311 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/image.py
+-rw-r--r--   0        0        0      778 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/partition.py
+-rw-r--r--   0        0        0     4552 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/models/uf2.py
+-rw-r--r--   0        0        0      124 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/upload/__init__.py
+-rw-r--r--   0        0        0     4846 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/upload/esphome.py
+-rw-r--r--   0        0        0     7219 2023-05-13 15:35:47.747376 ltchiptool-4.1.0/uf2tool/writer.py
+-rw-r--r--   0        0        0     3794 1970-01-01 00:00:00.000000 ltchiptool-4.1.0/PKG-INFO
```

### Comparing `ltchiptool-4.0.1/LICENSE` & `ltchiptool-4.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/README.md` & `ltchiptool-4.1.0/README.md`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/__main__.py` & `ltchiptool-4.1.0/ltchiptool/__main__.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/dumptool.py` & `ltchiptool-4.1.0/ltchiptool/commands/dumptool.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/elf2bin.py` & `ltchiptool-4.1.0/ltchiptool/commands/elf2bin.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/flash/_utils.py` & `ltchiptool-4.1.0/ltchiptool/commands/flash/_utils.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/flash/file.py` & `ltchiptool-4.1.0/ltchiptool/commands/flash/file.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/flash/read.py` & `ltchiptool-4.1.0/ltchiptool/commands/flash/read.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/flash/write.py` & `ltchiptool-4.1.0/ltchiptool/commands/flash/write.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/link2bin.py` & `ltchiptool-4.1.0/ltchiptool/commands/link2bin.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/commands/list.py` & `ltchiptool-4.1.0/ltchiptool/commands/list.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/families.json` & `ltchiptool-4.1.0/ltchiptool/families.json`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/__main__.py` & `ltchiptool-4.1.0/ltchiptool/gui/__main__.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/ltchiptool-192x192.png` & `ltchiptool-4.1.0/ltchiptool/gui/ltchiptool-192x192.png`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.ico` & `ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.ico`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.xrc` & `ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.xrc`

 * *Files 19% similar despite different names*

#### Comparing `ltchiptool-4.0.1/ltchiptool/gui/ltchiptool.xrc` & `ltchiptool-4.1.0/ltchiptool/gui/ltchiptool.xrc`

```diff
@@ -131,16 +131,16 @@
       <object class="sizeritem">
         <flag>wxALL|wxEXPAND</flag>
         <border>0</border>
         <option>1</option>
         <object class="wxTextCtrl" name="text_log">
           <style>wxTE_MULTILINE|wxTE_READONLY|wxTE_RICH|wxTE_DONTWRAP</style>
           <font>
-            <size>10</size>
-            <face>Cascadia Code</face>
+            <size>11</size>
+            <face>Consolas</face>
           </font>
           <bg>#0C0C0C</bg>
           <fg>#FFFFFF</fg>
         </object>
       </object>
     </object>
   </object>
@@ -643,15 +643,15 @@
         <border>5</border>
         <object class="wxBoxSizer" name="box_sizer_5">
           <orient>wxVERTICAL</orient>
           <object class="sizeritem">
             <flag>wxALL</flag>
             <border>0</border>
             <object class="wxStaticText" name="m_staticText_3">
-              <label>Discord server of LT community</label>
+              <label>Discord server of LibreTiny community</label>
               <wrap>-1</wrap>
             </object>
           </object>
           <object class="sizeritem">
             <flag>wxALL|wxEXPAND</flag>
             <border>0</border>
             <object class="wxHyperlinkCtrl" name="m_hyperlink">
@@ -659,8 +659,376 @@
               <style>wxHL_ALIGN_LEFT</style>
             </object>
           </object>
         </object>
       </object>
     </object>
   </object>
+  <object class="wxPanel" name="UpkPanel">
+    <style>wxTAB_TRAVERSAL</style>
+    <object class="wxBoxSizer" name="sizer_upk_main">
+      <orient>wxHORIZONTAL</orient>
+      <object class="sizeritem">
+        <flag>wxALL|wxEXPAND</flag>
+        <border>5</border>
+        <option>1</option>
+        <object class="wxNotebook" name="notebook_upk">
+          <object>
+            <label>Start page</label>
+            <style>wxTAB_TRAVERSAL</style>
+            <bg>#F0F0F0</bg>
+            <object class="wxPanel" name="page_start">
+              <style>wxTAB_TRAVERSAL</style>
+              <object class="wxBoxSizer" name="sizer_start">
+                <orient>wxVERTICAL</orient>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_start">
+                    <label>This tool allows to easily generate ESPHome YAML configuration, having either:
+- ESPHome-Kickstart running
+- Cloudcutter device profile
+- full firmware dump
+
+Choose a mode of operation to begin:</label>
+                    <wrap>-1</wrap>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxCommandLinkButton" name="button_kickstart">
+                    <label>Grab from ESPHome-Kickstart</label>
+                    <note>If you have flashed Kickstart to a device</note>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxCommandLinkButton" name="button_cloudcutter">
+                    <label>Build from Cloudcutter device profile</label>
+                    <note>If your device has a matching manufacturer/model profile</note>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxCommandLinkButton" name="button_dump">
+                    <label>Analyze firmware dump</label>
+                    <note>If you read a firmware .BIN with ltchiptool or bk7231tools</note>
+                  </object>
+                </object>
+              </object>
+            </object>
+          </object>
+          <object>
+            <label>Options</label>
+            <style>wxTAB_TRAVERSAL</style>
+            <bg>#F0F0F0</bg>
+            <object class="wxPanel" name="page_opts">
+              <style>wxTAB_TRAVERSAL</style>
+              <object class="wxBoxSizer" name="sizer_opts_main">
+                <orient>wxVERTICAL</orient>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_opts">
+                    <label>You can set various options related to the generated YAML.
+The default choices are usually fine in most cases.</label>
+                    <wrap>-1</wrap>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxBoxSizer" name="sizer_opts_horz">
+                    <orient>wxHORIZONTAL</orient>
+                    <object class="sizeritem">
+                      <flag>wxALL|wxEXPAND</flag>
+                      <border>5</border>
+                      <option>1</option>
+                      <object class="wxBoxSizer" name="sizer_opts_vert1">
+                        <orient>wxVERTICAL</orient>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_esphome_block">
+                            <label>Include esphome: block</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_name_mac">
+                            <label>Add MAC to device name</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_common">
+                            <label>Add common components</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_web_server">
+                            <label>Add Web Server &amp;&amp; Captive Portal</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_restart">
+                            <label>Add restart button &amp;&amp; sensor</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_uptime">
+                            <label>Add uptime sensor</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxCheckBox" name="opts_lt_version">
+                            <label>Add LT version sensor</label>
+                            <checked>1</checked>
+                          </object>
+                        </object>
+                      </object>
+                    </object>
+                    <object class="sizeritem">
+                      <flag>wxALL|wxEXPAND</flag>
+                      <border>5</border>
+                      <option>1</option>
+                      <object class="wxBoxSizer" name="sizer_opts_vert2">
+                        <orient>wxVERTICAL</orient>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxStaticText" name="text_wifi_ssid">
+                            <label>Wi-Fi SSID</label>
+                            <wrap>-1</wrap>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxTextCtrl" name="opts_wifi_ssid">
+                            <value>!secret wifi__ssid</value>
+                            <value>!secret wifi__ssid</value>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxStaticText" name="text_wifi_password">
+                            <label>Wi-Fi password</label>
+                            <wrap>-1</wrap>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxTextCtrl" name="opts_wifi_password">
+                            <value>!secret wifi__password</value>
+                            <value>!secret wifi__password</value>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxStaticText" name="text_ota_password">
+                            <label>OTA password</label>
+                            <wrap>-1</wrap>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxTextCtrl" name="opts_ota_password">
+                            <value>!secret ota__password</value>
+                            <value>!secret ota__password</value>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxStaticText" name="text_api_password">
+                            <label>API password</label>
+                            <wrap>-1</wrap>
+                          </object>
+                        </object>
+                        <object class="sizeritem">
+                          <flag>wxALL|wxEXPAND</flag>
+                          <border>5</border>
+                          <object class="wxTextCtrl" name="opts_api_password">
+                            <value>!secret api__password</value>
+                            <value>!secret api__password</value>
+                          </object>
+                        </object>
+                      </object>
+                    </object>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxALIGN_CENTER_HORIZONTAL</flag>
+                  <border>5</border>
+                  <object class="wxButton" name="button_generate">
+                    <label>Generate</label>
+                  </object>
+                </object>
+              </object>
+            </object>
+          </object>
+          <object>
+            <label>ESPHome YAML</label>
+            <style>wxTAB_TRAVERSAL</style>
+            <bg>#F0F0F0</bg>
+            <object class="wxPanel" name="page_esphome">
+              <style>wxTAB_TRAVERSAL</style>
+              <object class="wxGridBagSizer" name="sizer_esphome">
+                <vgap>0</vgap>
+                <hgap>0</hgap>
+                <growablerows>2</growablerows>
+                <growablecols>0</growablecols>
+                <flexibledirection>wxBOTH</flexibledirection>
+                <nonflexiblegrowmode>wxFLEX_GROWMODE_SPECIFIED</nonflexiblegrowmode>
+                <object class="sizeritem">
+                  <cellpos>0,0</cellpos>
+                  <cellspan>1,1</cellspan>
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_esphome_1">
+                    <label>This page shows a suggested YAML config for your device.</label>
+                    <wrap>500</wrap>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <cellpos>1,0</cellpos>
+                  <cellspan>1,1</cellspan>
+                  <flag>wxALL</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_esphome_2">
+                    <label>We do not take responsibility for using this tool and the generated configs.</label>
+                    <wrap>500</wrap>
+                    <font>
+                      <size>9</size>
+                      <weight>bold</weight>
+                    </font>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <cellpos>0,1</cellpos>
+                  <cellspan>2,1</cellspan>
+                  <flag>wxALL</flag>
+                  <border>5</border>
+                  <object class="wxButton" name="button_esphome_copy">
+                    <label>Copy</label>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <cellpos>2,0</cellpos>
+                  <cellspan>1,2</cellspan>
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <option>1</option>
+                  <object class="wxTextCtrl" name="input_esphome">
+                    <style>wxTE_MULTILINE|wxTE_READONLY</style>
+                    <font>
+                      <size>11</size>
+                      <face>Consolas</face>
+                    </font>
+                  </object>
+                </object>
+              </object>
+            </object>
+          </object>
+          <object>
+            <label>Device configuration</label>
+            <style>wxTAB_TRAVERSAL</style>
+            <bg>#F0F0F0</bg>
+            <object class="wxPanel" name="page_upk">
+              <style>wxTAB_TRAVERSAL</style>
+              <object class="wxBoxSizer" name="sizer_upk">
+                <orient>wxVERTICAL</orient>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_upk">
+                    <label>This page shows the raw user__param__key (UPK) structure.
+
+Based on this, ESPHome config is generated.</label>
+                    <wrap>500</wrap>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <option>1</option>
+                  <object class="wxTextCtrl" name="input_upk">
+                    <style>wxTE_MULTILINE|wxTE_READONLY</style>
+                    <font>
+                      <size>11</size>
+                      <face>Consolas</face>
+                    </font>
+                  </object>
+                </object>
+              </object>
+            </object>
+          </object>
+          <object>
+            <label>Storage data</label>
+            <style>wxTAB_TRAVERSAL</style>
+            <bg>#F0F0F0</bg>
+            <object class="wxPanel" name="page_storage">
+              <style>wxTAB_TRAVERSAL</style>
+              <object class="wxBoxSizer" name="sizer_storage">
+                <orient>wxVERTICAL</orient>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <object class="wxStaticText" name="text_storage_1">
+                    <label>This page shows the extracted Storage Area JSON. It contains a device schema and some other information that are useful for building Cloudcutter profiles.
+
+If Cloudcutter doesn't support your device yet, consider submitting the JSON to the issues page:</label>
+                    <wrap>500</wrap>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL</flag>
+                  <border>5</border>
+                  <object class="wxHyperlinkCtrl" name="link_storage">
+                    <label>https://github.com/tuya-cloudcutter/tuya-cloudcutter/issues</label>
+                    <style>wxHL_DEFAULT_STYLE</style>
+                  </object>
+                </object>
+                <object class="sizeritem">
+                  <flag>wxALL|wxEXPAND</flag>
+                  <border>5</border>
+                  <option>1</option>
+                  <object class="wxTextCtrl" name="input_storage">
+                    <style>wxTE_MULTILINE|wxTE_READONLY</style>
+                    <font>
+                      <size>11</size>
+                      <face>Consolas</face>
+                    </font>
+                  </object>
+                </object>
+              </object>
+            </object>
+          </object>
+        </object>
+      </object>
+    </object>
+  </object>
 </resource>
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/main.py` & `ltchiptool-4.1.0/ltchiptool/gui/main.py`

 * *Files 13% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 from ltchiptool.util.logging import LoggingHandler
 from ltchiptool.util.lvm import LVM
 
 from .panels.about import AboutPanel
 from .panels.base import BasePanel
 from .panels.flash import FlashPanel
 from .panels.log import LogPanel
+from .panels.upk import UpkPanel
 from .utils import with_target
 
 
 # noinspection PyPep8Naming
 class MainFrame(wx.Frame):
     panels: dict[str, BasePanel]
     init_params: dict
@@ -37,15 +38,19 @@
             xrc = join(sys._MEIPASS, "ltchiptool.xrc")
             icon = join(sys._MEIPASS, "ltchiptool.ico")
         else:
             xrc = join(dirname(__file__), "ltchiptool.xrc")
             icon = join(dirname(__file__), "ltchiptool.ico")
 
         try:
-            res = wx.xrc.XmlResource(xrc)
+            with open(xrc, "r") as f:
+                xrc_str = f.read()
+                xrc_str = xrc_str.replace("<object>", '<object class="notebookpage">')
+            res = wx.xrc.XmlResource()
+            res.LoadFromBuffer(xrc_str.encode())
         except SystemError:
             raise FileNotFoundError(f"Couldn't load the layout file '{xrc}'")
 
         try:
             # try to find LT directory or local data snapshot
             LVM.get().require_version()
         except Exception as e:
@@ -71,14 +76,18 @@
         try:
             self.SetMenuBar(res.LoadMenuBar("MainMenuBar"))
 
             self.Flash = FlashPanel(res, self.Notebook)
             self.panels["flash"] = self.Flash
             self.Notebook.AddPage(self.Flash, "Flashing")
 
+            self.Upk = UpkPanel(res, self.Notebook)
+            self.panels["upk"] = self.Upk
+            self.Notebook.AddPage(self.Upk, "UPK2ESPHome")
+
             self.About = AboutPanel(res, self.Notebook)
             self.panels["about"] = self.About
             self.Notebook.AddPage(self.About, "About")
 
             self.loaded = True
         except Exception as e:
             LoggingHandler.get().emit_exception(e)
@@ -105,29 +114,34 @@
         with open(self.config_file, "w") as f:
             json.dump(value, f, indent="\t")
 
     # noinspection PyPropertyAccess
     def GetSettings(self) -> dict:
         pos: wx.Point = self.GetPosition()
         size: wx.Size = self.GetSize()
+        page: int = self.Notebook.GetSelection()
         return dict(
             pos=[pos.x, pos.y],
             size=[size.x, size.y],
+            page=page,
         )
 
     def SetSettings(
         self,
         pos: tuple[int, int] = None,
         size: tuple[int, int] = None,
+        page: int = None,
         **_,
     ):
         if pos:
             self.SetPosition(pos)
         if size:
             self.SetSize(size)
+        if page is not None:
+            self.Notebook.SetSelection(page)
 
     @staticmethod
     def OnException(*args):
         if isinstance(args[0], type):
             LoggingHandler.get().emit_exception(args[1])
         else:
             LoggingHandler.get().emit_exception(args[0].exc_value)
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/panels/about.py` & `ltchiptool-4.1.0/ltchiptool/gui/panels/about.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/panels/base.py` & `ltchiptool-4.1.0/ltchiptool/gui/panels/base.py`

 * *Files 11% similar despite different names*

```diff
@@ -58,14 +58,17 @@
         for t in list(self._threads):
             t.stop()
             t.join()
 
     def OnMenu(self, title: str, label: str, checked: bool):
         pass
 
+    def OnFileDrop(self, *files):
+        pass
+
     def _OnUpdate(self, event: wx.Event | None):
         if self._in_update:
             event.Skip()
             return
         self._in_update = True
         event.Skip()
         self.OnUpdate(event.GetEventObject() if event else None)
@@ -136,7 +139,23 @@
         self.OnUpdate()
 
     def DisableAll(self):
         if self.is_closing:
             return
         for window in self._components:
             window.Disable()
+
+    def EnableFileDrop(self):
+        panel = self
+
+        class FileDropTarget(wx.FileDropTarget):
+            def __init__(self):
+                wx.FileDropTarget.__init__(self)
+
+            def OnDropFiles(self, x, y, filenames) -> bool:
+                panel.OnFileDrop(*filenames)
+                return True
+
+        self.SetDropTarget(FileDropTarget())
+
+    def DisableFileDrop(self):
+        self.SetDropTarget(None)
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/panels/flash.py` & `ltchiptool-4.1.0/ltchiptool/gui/panels/flash.py`

 * *Files 1% similar despite different names*

```diff
@@ -75,14 +75,16 @@
         families = set()
         family_names = SocInterface.get_family_names()
         for family in Family.get_all():
             if family.name in family_names:
                 families.add(family.description)
         self.Family.Set(sorted(families))
 
+        self.EnableFileDrop()
+
     def SetInitParams(self, file: str = None, **kwargs):
         if file and isfile(file):
             self.operation = FlashOp.WRITE
             self.file = realpath(file)
 
     def GetSettings(self) -> dict:
         return dict(
@@ -248,14 +250,20 @@
             self.Start.Enable()
         else:
             self.Start.SetNote("")
             self.Start.Enable()
 
         self.Cancel.Disable()
 
+    def OnFileDrop(self, *files):
+        if not files:
+            return
+        self.operation = FlashOp.WRITE
+        self.file = files[0]
+
     @with_target
     def OnBlur(self, event: wx.FocusEvent, target: wx.Window):
         event.Skip()
         if target == self.File:
             self.file = self.file
 
     @property
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/panels/log.py` & `ltchiptool-4.1.0/ltchiptool/gui/panels/log.py`

 * *Files 1% similar despite different names*

```diff
@@ -179,14 +179,16 @@
                 case "Colors":
                     item.Check(not raw)
                 case _ if item.GetItemLabel() == level_name:
                     item.Check()
 
     def OnShow(self):
         super().OnShow()
+        if self.delayed_lines is None:
+            return
         for log_prefix, message, color in self.delayed_lines:
             self.emit_raw(log_prefix, message, color)
         self.delayed_lines = None
 
     def OnClose(self):
         super().OnClose()
         LoggingHandler.get().clear_emitters()
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/utils.py` & `ltchiptool-4.1.0/ltchiptool/gui/utils.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/work/base.py` & `ltchiptool-4.1.0/ltchiptool/gui/work/base.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/work/flash.py` & `ltchiptool-4.1.0/ltchiptool/gui/work/flash.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,27 +1,24 @@
 #  Copyright (c) Kuba Szczodrzyński 2023-1-15.
 
 from logging import debug
 from os import SEEK_SET, makedirs, stat
 from os.path import dirname
 from typing import Callable
 
-import wx
-
 from ltchiptool import SocInterface
 from ltchiptool.util.flash import (
     ClickProgressCallback,
     FlashConnection,
     FlashOp,
     format_flash_guide,
 )
 from ltchiptool.util.logging import LoggingHandler
 from ltchiptool.util.misc import sizeof
 from uf2tool import UploadContext
-from uf2tool.models import UF2
 
 from .base import BaseThread
 
 
 class FlashThread(BaseThread):
     callback: ClickProgressCallback
```

### Comparing `ltchiptool-4.0.1/ltchiptool/gui/work/ports.py` & `ltchiptool-4.1.0/ltchiptool/gui/work/ports.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/models/board.py` & `ltchiptool-4.1.0/ltchiptool/models/board.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/models/family.py` & `ltchiptool-4.1.0/ltchiptool/models/family.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/platform.json` & `ltchiptool-4.1.0/ltchiptool/platform.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9285714285714286%*

 * *Differences: {"'version'": "'1.0.2'"}*

```diff
@@ -107,9 +107,9 @@
         }
     },
     "repository": {
         "type": "git",
         "url": "https://github.com/kuba2k2/platformio-libretiny"
     },
     "title": "LibreTiny",
-    "version": "1.0.0"
+    "version": "1.0.2"
 }
```

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz/binary.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz/binary.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz/flash.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz/flash.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz/main.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz/main.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz/util/rtltool.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz/util/rtltool.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz2/flash.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz2/flash.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz2/main.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz2/main.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/ambz2/util/ambz2tool.py` & `ltchiptool-4.1.0/ltchiptool/soc/ambz2/util/ambz2tool.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/binary.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/binary.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/bkpackager.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/bkpackager.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/flash.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/flash.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/main.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/main.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/binary.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/binary.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/crypto.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/crypto.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/models.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/models.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/bk72xx/util/rbl.py` & `ltchiptool-4.1.0/ltchiptool/soc/bk72xx/util/rbl.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/common.py` & `ltchiptool-4.1.0/ltchiptool/soc/common.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/soc/interface.py` & `ltchiptool-4.1.0/ltchiptool/soc/interface.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/bitint.py` & `ltchiptool-4.1.0/ltchiptool/util/bitint.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/cli.py` & `ltchiptool-4.1.0/ltchiptool/util/cli.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/crc16.py` & `ltchiptool-4.1.0/ltchiptool/util/crc16.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/crypto.py` & `ltchiptool-4.1.0/ltchiptool/util/crypto.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/detection.py` & `ltchiptool-4.1.0/ltchiptool/util/detection.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/dict.py` & `ltchiptool-4.1.0/ltchiptool/util/dict.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/fileio.py` & `ltchiptool-4.1.0/ltchiptool/util/fileio.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/flash.py` & `ltchiptool-4.1.0/ltchiptool/util/flash.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/fwbinary.py` & `ltchiptool-4.1.0/ltchiptool/util/fwbinary.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/intbin.py` & `ltchiptool-4.1.0/ltchiptool/util/intbin.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/logging.py` & `ltchiptool-4.1.0/ltchiptool/util/logging.py`

 * *Files 2% similar despite different names*

```diff
@@ -116,18 +116,18 @@
     @staticmethod
     def tb_echo(tb):
         filename = tb.tb_frame.f_code.co_filename
         name = tb.tb_frame.f_code.co_name
         line = tb.tb_lineno
         graph(1, f'File "{filename}", line {line}, in {name}', loglevel=ERROR)
 
-    def emit_exception(self, e: Exception):
+    def emit_exception(self, e: Exception, no_hook: bool = False):
         error(f"{type(e).__name__}: {e}")
         tb = e.__traceback__
-        if self.exception_hook:
+        if self.exception_hook and not no_hook:
             self.exception_hook(e)
         if not tb:
             return
         while tb.tb_next:
             if self.full_traceback:
                 self.tb_echo(tb)
             tb = tb.tb_next
```

### Comparing `ltchiptool-4.0.1/ltchiptool/util/lvm.py` & `ltchiptool-4.1.0/ltchiptool/util/lvm.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/misc.py` & `ltchiptool-4.1.0/ltchiptool/util/misc.py`

 * *Files 6% similar despite different names*

```diff
@@ -27,19 +27,19 @@
 
 
 def list_serial_ports() -> List[Tuple[str, bool, str]]:
     from serial.tools.list_ports import comports
 
     ports = []
     for port in comports():
+        port.description = port.description.replace(f"({port.name})", "").strip()
         is_usb = port.hwid.startswith("USB")
         if is_usb:
             description = (
                 f"{port.name} - {port.description} - "
-                f"VID={port.vid:04X} ({port.manufacturer}), "
-                f"PID={port.pid:04X} "
+                f"{port.manufacturer} ({port.vid:04X}/{port.pid:04X})"
             )
         else:
-            description = f"{port.name} - {port.description} - HWID={port.hwid}"
+            description = f"{port.name} - {port.description}"
         ports.append((port.device, is_usb, description))
 
     return sorted(ports, key=lambda x: (not x[1], x[2]))
```

### Comparing `ltchiptool-4.0.1/ltchiptool/util/obj.py` & `ltchiptool-4.1.0/ltchiptool/util/obj.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/slice.py` & `ltchiptool-4.1.0/ltchiptool/util/slice.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/util/toolchain.py` & `ltchiptool-4.1.0/ltchiptool/util/toolchain.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/ltchiptool/version.py` & `ltchiptool-4.1.0/ltchiptool/version.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/pyproject.toml` & `ltchiptool-4.1.0/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "ltchiptool"
-version = "4.0.1"
+version = "4.1.0"
 description = "Universal flashing and binary manipulation tool for IoT chips"
 authors = ["Kuba Szczodrzyński <kuba@szczodrzynski.pl>"]
 license = "MIT"
 packages = [
     { include = "ltchiptool" },
     { include = "uf2tool" },
 ]
@@ -16,31 +16,32 @@
 
 [tool.poetry.dependencies]
 python = "^3.7"
 click = "^8.1.3"
 colorama = "^0.4.5"
 importlib-metadata = "^4.12.0"
 prettytable = "^3.3.0"
-bk7231tools = "^1.3.0"
+bk7231tools = "^1.3.5"
 xmodem = "^0.4.6"
 wxPython = {version = "^4.2.0", optional = true}
 pywin32 = {version = "^305", optional = true, markers = "sys_platform == 'win32'"}
 py-datastruct = "^0.3.0"
 semantic-version = "^2.10.0"
+upk2esphome = "^1.0.0"
 
 [tool.poetry.dependencies.pycryptodomex]
 version = "^3.15.0"
 markers = "platform_machine not in 'armv6l,armv7l,armv8l,armv8b,aarch64'"
 
 [tool.poetry.dependencies.pyaes]
 version = "^1.6.1"
 markers = "platform_machine in 'armv6l,armv7l,armv8l,armv8b,aarch64'"
 
 [tool.poetry.extras]
-gui = ["wxPython", "pywin32"]
+gui = ["wxPython", "pywin32", "upk2esphome"]
 
 [tool.poetry.dev-dependencies]
 black = "^22.6.0"
 isort = "^5.10.1"
 autoflake = "^1.4"
 
 [tool.poetry.scripts]
```

### Comparing `ltchiptool-4.0.1/uf2tool/binpatch/bindiff.py` & `ltchiptool-4.1.0/uf2tool/binpatch/bindiff.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/binpatch/diff32.py` & `ltchiptool-4.1.0/uf2tool/binpatch/diff32.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/cli.py` & `ltchiptool-4.1.0/uf2tool/cli.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/block.py` & `ltchiptool-4.1.0/uf2tool/models/block.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/context.py` & `ltchiptool-4.1.0/uf2tool/models/context.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/enums.py` & `ltchiptool-4.1.0/uf2tool/models/enums.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/flags.py` & `ltchiptool-4.1.0/uf2tool/models/flags.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/image.py` & `ltchiptool-4.1.0/uf2tool/models/image.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/partition.py` & `ltchiptool-4.1.0/uf2tool/models/partition.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/models/uf2.py` & `ltchiptool-4.1.0/uf2tool/models/uf2.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/upload/esphome.py` & `ltchiptool-4.1.0/uf2tool/upload/esphome.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/uf2tool/writer.py` & `ltchiptool-4.1.0/uf2tool/writer.py`

 * *Files identical despite different names*

### Comparing `ltchiptool-4.0.1/PKG-INFO` & `ltchiptool-4.1.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,33 +1,34 @@
 Metadata-Version: 2.1
 Name: ltchiptool
-Version: 4.0.1
+Version: 4.1.0
 Summary: Universal flashing and binary manipulation tool for IoT chips
 License: MIT
 Author: Kuba Szczodrzyński
 Author-email: kuba@szczodrzynski.pl
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: gui
-Requires-Dist: bk7231tools (>=1.3.0,<2.0.0)
+Requires-Dist: bk7231tools (>=1.3.5,<2.0.0)
 Requires-Dist: click (>=8.1.3,<9.0.0)
 Requires-Dist: colorama (>=0.4.5,<0.5.0)
 Requires-Dist: importlib-metadata (>=4.12.0,<5.0.0)
 Requires-Dist: prettytable (>=3.3.0,<4.0.0)
 Requires-Dist: py-datastruct (>=0.3.0,<0.4.0)
 Requires-Dist: pyaes (>=1.6.1,<2.0.0) ; platform_machine in "armv6l,armv7l,armv8l,armv8b,aarch64"
 Requires-Dist: pycryptodomex (>=3.15.0,<4.0.0) ; platform_machine not in "armv6l,armv7l,armv8l,armv8b,aarch64"
 Requires-Dist: pywin32 (>=305,<306) ; (sys_platform == "win32") and (extra == "gui")
 Requires-Dist: semantic-version (>=2.10.0,<3.0.0)
+Requires-Dist: upk2esphome (>=1.0.0,<2.0.0) ; extra == "gui"
 Requires-Dist: wxPython (>=4.2.0,<5.0.0) ; extra == "gui"
 Requires-Dist: xmodem (>=0.4.6,<0.5.0)
 Description-Content-Type: text/markdown
 
 # ltchiptool
 
 Universal, easy-to-use GUI flashing/dumping tool for BK7231, RTL8710B and RTL8720C. Also contains some CLI utilities for binary firmware manipulation.
```

