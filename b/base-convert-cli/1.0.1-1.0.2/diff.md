# Comparing `tmp/base-convert-cli-1.0.1.tar.gz` & `tmp/base-convert-cli-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/home/kg/proyectos/bs/dist/tmpwf5rvbj_/base-convert-cli-1.0.1.tar", last modified: Mon May  8 15:15:29 2023, max compression
+gzip compressed data, was "/home/kg/proyectos/bs/dist/tmpc8wdv3bf/base-convert-cli-1.0.2.tar", last modified: Fri May 12 19:58:59 2023, max compression
```

## Comparing `base-convert-cli-1.0.1.tar` & `base-convert-cli-1.0.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/
--rw-rw-r--   0 kg        (1000) kg        (1000)     2199 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/PKG-INFO
--rw-rw-r--   0 kg        (1000) kg        (1000)      709 2023-05-08 15:14:19.000000 base-convert-cli-1.0.1/setup.py
--rw-r--r--   0 kg        (1000) kg        (1000)     1055 2020-07-26 18:15:45.000000 base-convert-cli-1.0.1/LICENSE.txt
-drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/scripts/
--rw-rw-r--   0 kg        (1000) kg        (1000)       68 2021-12-10 14:15:41.000000 base-convert-cli-1.0.1/scripts/bs
--rw-rw-r--   0 kg        (1000) kg        (1000)       38 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/setup.cfg
--rw-rw-r--   0 kg        (1000) kg        (1000)     1769 2023-05-08 13:35:09.000000 base-convert-cli-1.0.1/README.md
-drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/
-drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/base_convert_cli.egg-info/
--rw-rw-r--   0 kg        (1000) kg        (1000)     2199 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/base_convert_cli.egg-info/PKG-INFO
--rw-rw-r--   0 kg        (1000) kg        (1000)        1 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/base_convert_cli.egg-info/dependency_links.txt
--rw-rw-r--   0 kg        (1000) kg        (1000)       15 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/base_convert_cli.egg-info/top_level.txt
--rw-rw-r--   0 kg        (1000) kg        (1000)      248 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/base_convert_cli.egg-info/SOURCES.txt
-drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-08 15:15:29.000000 base-convert-cli-1.0.1/src/baseconvertcli/
--rwxrwxr-x   0 kg        (1000) kg        (1000)     6972 2023-05-08 15:11:15.000000 base-convert-cli-1.0.1/src/baseconvertcli/__init__.py
+drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/
+-rw-rw-r--   0 kg        (1000) kg        (1000)     2330 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/PKG-INFO
+-rw-rw-r--   0 kg        (1000) kg        (1000)      709 2023-05-12 19:57:03.000000 base-convert-cli-1.0.2/setup.py
+-rw-r--r--   0 kg        (1000) kg        (1000)     1055 2020-07-26 18:15:45.000000 base-convert-cli-1.0.2/LICENSE.txt
+drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/scripts/
+-rw-rw-r--   0 kg        (1000) kg        (1000)       68 2021-12-10 14:15:41.000000 base-convert-cli-1.0.2/scripts/bs
+-rw-rw-r--   0 kg        (1000) kg        (1000)       38 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/setup.cfg
+-rw-rw-r--   0 kg        (1000) kg        (1000)     1900 2023-05-12 19:55:03.000000 base-convert-cli-1.0.2/README.md
+drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/
+drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/base_convert_cli.egg-info/
+-rw-rw-r--   0 kg        (1000) kg        (1000)     2330 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/base_convert_cli.egg-info/PKG-INFO
+-rw-rw-r--   0 kg        (1000) kg        (1000)        1 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/base_convert_cli.egg-info/dependency_links.txt
+-rw-rw-r--   0 kg        (1000) kg        (1000)       15 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/base_convert_cli.egg-info/top_level.txt
+-rw-rw-r--   0 kg        (1000) kg        (1000)      248 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/base_convert_cli.egg-info/SOURCES.txt
+drwxrwxr-x   0 kg        (1000) kg        (1000)        0 2023-05-12 19:58:59.000000 base-convert-cli-1.0.2/src/baseconvertcli/
+-rwxrwxr-x   0 kg        (1000) kg        (1000)     8351 2023-05-12 19:56:45.000000 base-convert-cli-1.0.2/src/baseconvertcli/__init__.py
```

### Comparing `base-convert-cli-1.0.1/PKG-INFO` & `base-convert-cli-1.0.2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: base-convert-cli
-Version: 1.0.1
+Version: 1.0.2
 Summary: A CLI tool that converts numbers between bases.
 Home-page: https://github.com/Kevinpgalligan/bs
 Author: Kevin Galligan
 Author-email: galligankevinp@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
@@ -109,14 +109,22 @@
 15
 ```
 
 Padding with zeroes.
 
 ```
 $ bs --from decimal --to binary --pad 8 14
+00001110
+```
+
+Setting precision for converting fractional numbers.
+
+```
+$ bs --precision 10 --from 3 --to decimal 0.1
+0.3333333333
 ```
 
 Aaaaand input through a pipe.
 
 ```
 $ echo '5+10' | bc | bs -t h
 [from decimal]
```

### Comparing `base-convert-cli-1.0.1/setup.py` & `base-convert-cli-1.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
     long_description = f.read()
 
 setup(
     name="base-convert-cli",
     description="A CLI tool that converts numbers between bases.",
     long_description=long_description,
     long_description_content_type="text/markdown",
-    version="1.0.1",
+    version="1.0.2",
     url="https://github.com/Kevinpgalligan/bs",
     author="Kevin Galligan",
     author_email="galligankevinp@gmail.com",
     scripts=["scripts/bs"],
     packages=find_packages("src"),
     package_dir={'': 'src'},
     classifiers=[
```

### Comparing `base-convert-cli-1.0.1/LICENSE.txt` & `base-convert-cli-1.0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `base-convert-cli-1.0.1/README.md` & `base-convert-cli-1.0.2/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -95,14 +95,22 @@
 15
 ```
 
 Padding with zeroes.
 
 ```
 $ bs --from decimal --to binary --pad 8 14
+00001110
+```
+
+Setting precision for converting fractional numbers.
+
+```
+$ bs --precision 10 --from 3 --to decimal 0.1
+0.3333333333
 ```
 
 Aaaaand input through a pipe.
 
 ```
 $ echo '5+10' | bc | bs -t h
 [from decimal]
```

### Comparing `base-convert-cli-1.0.1/src/base_convert_cli.egg-info/PKG-INFO` & `base-convert-cli-1.0.2/src/base_convert_cli.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: base-convert-cli
-Version: 1.0.1
+Version: 1.0.2
 Summary: A CLI tool that converts numbers between bases.
 Home-page: https://github.com/Kevinpgalligan/bs
 Author: Kevin Galligan
 Author-email: galligankevinp@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
@@ -109,14 +109,22 @@
 15
 ```
 
 Padding with zeroes.
 
 ```
 $ bs --from decimal --to binary --pad 8 14
+00001110
+```
+
+Setting precision for converting fractional numbers.
+
+```
+$ bs --precision 10 --from 3 --to decimal 0.1
+0.3333333333
 ```
 
 Aaaaand input through a pipe.
 
 ```
 $ echo '5+10' | bc | bs -t h
 [from decimal]
```

### Comparing `base-convert-cli-1.0.1/src/baseconvertcli/__init__.py` & `base-convert-cli-1.0.2/src/baseconvertcli/__init__.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 #!/usr/bin/env python3
 
 import sys
 import re
 import argparse
+import decimal
 
 DIGITS = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ"
 
 class InvalidCliArgsError(Exception):
     def __init__(self, message):
         self.message = message
         super().__init__(message)
@@ -32,26 +33,51 @@
             raise RuntimeError("Failed to parse: {}".format(s))
         if self.prefix:
             digits = match.group(2)
             fractional_digits = match.group(3)
         else:
             digits = match.group(1)
             fractional_digits = match.group(2)
-        return (string_to_number(digits, self.size),
-                string_to_number(fractional_digits[1:], self.size) if fractional_digits else None)
+        if fractional_digits:
+            fractional_digits = fractional_digits[1:] # trim the dot
+            fraction = decimal.Decimal("0.0")
+            i = 0
+            exp = 1
+            while i < len(fractional_digits):
+                fraction += decimal.Decimal(DIGITS.index(fractional_digits[i])) / decimal.Decimal(self.size**exp)
+                i += 1
+                exp += 1
+            # Skip the leading 0 and the decimal point.
+            fraction_as_str = str(fraction%1)[2:]
+            fractional_n = int(fraction_as_str)
+            magnitude = len(fraction_as_str)
+        else:
+            fractional_n = None
+        return (string_to_number(digits, self.size), fractional_n, magnitude if fractional_n else None)
 
-    def format(self, n):
+    def format_integral(self, n):
         if n == 0:
             return "0"
         digits = []
         while n > 0:
             digits.append(DIGITS[n % self.size])
             n = n // self.size
         return "".join(reversed(digits))
 
+    def format_fraction(self, n, magnitude):
+        # Source: https://www.geeksforgeeks.org/convert-decimal-fraction-binary-number/
+        # I'm unsure exactly how it works...
+        q = 10**magnitude
+        digits = []
+        while n > 0:
+            n *= self.size
+            digits.append(DIGITS[n // q])
+            n %= q
+        return "".join(digits)
+
     def __eq__(self, other):
         return isinstance(other, Base) and other.size == self.size
 
 def string_to_number(s, base_size):
     return sum((base_size**i)*DIGITS.index(d)
                for i, d in enumerate(reversed(s))) 
 
@@ -115,19 +141,21 @@
   bs 0                     # many -> many
   bs --from 6 5            # base-6 -> many
   bs --from hexadecimal 5  # hex -> many
   bs 5 --pad 8             # left-pad with zeros so there are at least 8 digits
   bs --from hex --to dec F # hex -> dec
   bs -f h -t d F           # short version
   bs 0xf                   # specify base through prefix
-  bs 1.f                   # fractions""")
+  bs --precision 10 1.f    # fractions, setting precision""")
     parser.add_argument("n", nargs="?", help="The number to convert. Can also be passed in ASCII/text format through standard input.")
     parser.add_argument("--from", "-f", required=False, dest="fr", help="The input base. Number or name.")
     parser.add_argument("--to", "-t", required=False, help="The output base. Number or name.")
     parser.add_argument("--pad", default=0, type=int, required=False, help="Whether to add zero padding.")
+    parser.add_argument("--precision", default=8, type=int,
+                        required=False, help="Precision for converting fractions, default is 8.")
     return parser
 
 def parse_base(s):
     for base in BASES:
         if s in base.names:
             return base
     try:
@@ -140,14 +168,17 @@
         raise InvalidCliArgsError("Only support up to base-36, but given: {}".format(n))
     for base in BASES:
         if n == base.size:
             return base
     return Base([], "base-{}".format(n), n, "")
 
 def do_conversion(args):
+    if not args.precision > 0:
+        raise InvalidCliArgsError("Precision must be at least 1.")
+    decimal.getcontext().prec = args.precision
     if args.n:
         s = args.n
     else:
         s = sys.stdin.read()
     s = s.upper()
     if args.fr:
         base = parse_base(args.fr)
@@ -159,38 +190,38 @@
         if not input_bases:
             raise InvalidCliArgsError("Non-standard input base, specify base with --from.")
     if args.to:
         output_bases = [parse_base(args.to)]
     else:
         output_bases = BASES
     if len(input_bases) == 1 and len(output_bases) == 1:
-        n, fractional_n = input_bases[0].parse(s)
-        show(output_bases[0].format(n).zfill(args.pad), newline=False)
+        n, fractional_n, magnitude = input_bases[0].parse(s)
+        show(output_bases[0].format_integral(n).zfill(args.pad), newline=False)
         if fractional_n:
-            show("." + output_bases[0].format(fractional_n), newline=False)
+            show("." + output_bases[0].format_fraction(fractional_n, magnitude), newline=False)
         show_newline()
     else:
         for i, base in enumerate(input_bases):
-            n, fractional_n = base.parse(s)
+            n, fractional_n, magnitude = base.parse(s)
             if all(obase == base for obase in output_bases):
                 # Don't print anything if there's only a pointless
                 # conversion (from a base to itself).
                 continue
 
             show("[from {}]", base.full_name, bold=True)
             max_name_length = max(len(base.full_name) for base in output_bases)
             for output_base in output_bases:
                 if output_base != base:
                     show(
                         "  {:<" + str(max_name_length+1) + "}{}",
                         output_base.full_name,
-                        output_base.format(n).zfill(args.pad),
+                        output_base.format_integral(n).zfill(args.pad),
                         newline=False)
                     if fractional_n:
-                        show("." + output_base.format(fractional_n), newline=False)
+                        show("." + output_base.format_fraction(fractional_n, magnitude), newline=False)
                     show_newline()
             if i != len(input_bases) - 1:
                 show_newline()
 
 def main():
     parser = get_parser()
     args = parser.parse_args()
```

