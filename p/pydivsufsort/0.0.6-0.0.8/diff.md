# Comparing `tmp/pydivsufsort-0.0.6.tar.gz` & `tmp/pydivsufsort-0.0.8-cp39-cp39-win_amd64.whl.zip`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pydivsufsort-0.0.6.tar", last modified: Sun Dec 12 20:45:59 2021, max compression
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

