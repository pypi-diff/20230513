# Comparing `tmp/pyThorlabsPM100x-0.8.tar.gz` & `tmp/pyThorlabsPM100x-0.9-py3-none-any.whl.zip`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyThorlabsPM100x-0.8.tar", last modified: Thu Mar  3 04:14:54 2022, max compression
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

