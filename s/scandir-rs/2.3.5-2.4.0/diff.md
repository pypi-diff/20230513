# Comparing `tmp/scandir_rs-2.3.5.tar.gz` & `tmp/scandir_rs-2.4.0-cp39-cp39-manylinux_2_34_x86_64.whl.zip`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

