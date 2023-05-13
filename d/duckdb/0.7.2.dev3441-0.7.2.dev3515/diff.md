# Comparing `tmp/duckdb-0.7.2.dev3441.tar.gz` & `tmp/duckdb-0.7.2.dev3515-cp38-cp38-win_amd64.whl.zip`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/duckdb-0.7.2.dev3441.tar", last modified: Fri May 12 04:13:44 2023, max compression
+Zip archive data, at least v2.0 to extract, compression method=deflate
```

## filetype from diffoscope

```diff
@@ -1 +1 @@
-GzipFile
+ZipFile
```

