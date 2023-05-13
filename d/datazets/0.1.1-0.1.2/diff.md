# Comparing `tmp/datazets-0.1.1.tar.gz` & `tmp/datazets-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datazets-0.1.1.tar", last modified: Sat May 13 19:00:39 2023, max compression
+gzip compressed data, was "datazets-0.1.2.tar", last modified: Sat May 13 19:15:35 2023, max compression
```

## Comparing `datazets-0.1.1.tar` & `datazets-0.1.2.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-05-13 19:00:39.532568 datazets-0.1.1/
--rw-rw-rw-   0        0        0     1121 2022-03-22 18:16:18.000000 datazets-0.1.1/LICENSE
--rw-rw-rw-   0        0        0       56 2023-05-12 07:39:26.000000 datazets-0.1.1/MANIFEST.in
--rw-rw-rw-   0        0        0     4888 2023-05-13 19:00:39.531083 datazets-0.1.1/PKG-INFO
--rw-rw-rw-   0        0        0     4294 2023-05-13 19:00:10.000000 datazets-0.1.1/README.md
-drwxrwxrwx   0        0        0        0 2023-05-13 19:00:39.520101 datazets-0.1.1/datazets/
--rw-rw-rw-   0        0        0      700 2023-05-13 19:00:26.000000 datazets-0.1.1/datazets/__init__.py
--rw-rw-rw-   0        0        0    12353 2023-05-13 18:51:22.000000 datazets-0.1.1/datazets/datazets.py
--rw-rw-rw-   0        0        0      721 2023-05-13 18:30:32.000000 datazets-0.1.1/datazets/examples.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:00:39.531083 datazets-0.1.1/datazets/utils/
--rw-rw-rw-   0        0        0        0 2020-01-01 22:53:45.000000 datazets-0.1.1/datazets/utils/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-13 19:00:39.530106 datazets-0.1.1/datazets.egg-info/
--rw-rw-rw-   0        0        0     4888 2023-05-13 19:00:39.000000 datazets-0.1.1/datazets.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      287 2023-05-13 19:00:39.000000 datazets-0.1.1/datazets.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-13 19:00:39.000000 datazets-0.1.1/datazets.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       22 2023-05-13 19:00:39.000000 datazets-0.1.1/datazets.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-05-13 19:00:39.000000 datazets-0.1.1/datazets.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-13 19:00:39.532568 datazets-0.1.1/setup.cfg
--rw-rw-rw-   0        0        0     1382 2023-05-13 18:52:09.000000 datazets-0.1.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:15:35.940380 datazets-0.1.2/
+-rw-rw-rw-   0        0        0     1121 2022-03-22 18:16:18.000000 datazets-0.1.2/LICENSE
+-rw-rw-rw-   0        0        0       56 2023-05-12 07:39:26.000000 datazets-0.1.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     4654 2023-05-13 19:15:35.938967 datazets-0.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     4060 2023-05-13 19:04:51.000000 datazets-0.1.2/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 19:15:35.921440 datazets-0.1.2/datazets/
+-rw-rw-rw-   0        0        0      700 2023-05-13 19:13:14.000000 datazets-0.1.2/datazets/__init__.py
+-rw-rw-rw-   0        0        0    12367 2023-05-13 19:10:27.000000 datazets-0.1.2/datazets/datazets.py
+-rw-rw-rw-   0        0        0      749 2023-05-13 19:11:03.000000 datazets-0.1.2/datazets/examples.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:15:35.937387 datazets-0.1.2/datazets/utils/
+-rw-rw-rw-   0        0        0        0 2020-01-01 22:53:45.000000 datazets-0.1.2/datazets/utils/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 19:15:35.936416 datazets-0.1.2/datazets.egg-info/
+-rw-rw-rw-   0        0        0     4654 2023-05-13 19:15:35.000000 datazets-0.1.2/datazets.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      287 2023-05-13 19:15:35.000000 datazets-0.1.2/datazets.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 19:15:35.000000 datazets-0.1.2/datazets.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       22 2023-05-13 19:15:35.000000 datazets-0.1.2/datazets.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-05-13 19:15:35.000000 datazets-0.1.2/datazets.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 19:15:35.940380 datazets-0.1.2/setup.cfg
+-rw-rw-rw-   0        0        0     1382 2023-05-13 18:52:09.000000 datazets-0.1.2/setup.py
```

### Comparing `datazets-0.1.1/LICENSE` & `datazets-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `datazets-0.1.1/PKG-INFO` & `datazets-0.1.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: datazets
-Version: 0.1.1
+Version: 0.1.2
 Summary: Datazets is a python package to import well known example data sets.
 Home-page: https://github.com/erdogant/datazets
 Author: Erdogan Taskesen
 Author-email: erdogant@gmail.com
 License: UNKNOWN
-Download-URL: https://github.com/erdogant/datazets/archive/0.1.1.tar.gz
+Download-URL: https://github.com/erdogant/datazets/archive/0.1.2.tar.gz
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -23,15 +23,14 @@
 [![LOC](https://sloc.xyz/github/erdogant/datazets/?category=code)](https://github.com/erdogant/datazets/)
 [![Downloads](https://static.pepy.tech/personalized-badge/datazets?period=month&units=international_system&left_color=grey&right_color=brightgreen&left_text=PyPI%20downloads/month)](https://pepy.tech/project/datazets)
 [![Downloads](https://static.pepy.tech/personalized-badge/datazets?period=total&units=international_system&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/datazets)
 [![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/erdogant/datazets/blob/master/LICENSE)
 [![Forks](https://img.shields.io/github/forks/erdogant/datazets.svg)](https://github.com/erdogant/datazets/network)
 [![Issues](https://img.shields.io/github/issues/erdogant/datazets.svg)](https://github.com/erdogant/datazets/issues)
 [![Project Status](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
-[![Colab](https://colab.research.google.com/assets/colab-badge.svg?logo=github%20sponsors)](https://erdogant.github.io/datazets/pages/html/Documentation.html#colab-notebook)
 ![GitHub Repo stars](https://img.shields.io/github/stars/erdogant/datazets)
 ![GitHub repo size](https://img.shields.io/github/repo-size/erdogant/datazets)
 [![Donate](https://img.shields.io/badge/Support%20this%20project-grey.svg?logo=github%20sponsors)](https://erdogant.github.io/datazets/pages/html/Documentation.html#)
 <!---[![BuyMeCoffee](https://img.shields.io/badge/buymea-coffee-yellow.svg)](https://www.buymeacoffee.com/erdogant)-->
 <!---[![Coffee](https://img.shields.io/badge/coffee-black-grey.svg)](https://erdogant.github.io/donate/?currency=USD&amount=5)-->
 
 
@@ -99,17 +98,14 @@
 ```
 <p align="center">
   <img src="https://github.com/erdogant/datazets/blob/master/docs/figs/fig1.png" width="600" />
   
 </p>
 
 
-#### References
-* https://github.com/erdogant/datazets
-
 #### Citation
 Please cite in your publications if this is useful for your research (see citation).
    
 ### Maintainers
 * Erdogan Taskesen, github: [erdogant](https://github.com/erdogant)
 
 ### Contribute
```

### Comparing `datazets-0.1.1/README.md` & `datazets-0.1.2/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -75,195 +75,180 @@
 000004a0: 7461 7a65 7473 2f69 7373 7565 7329 0d0a  tazets/issues)..
 000004b0: 5b21 5b50 726f 6a65 6374 2053 7461 7475  [![Project Statu
 000004c0: 735d 2868 7474 703a 2f2f 7777 772e 7265  s](http://www.re
 000004d0: 706f 7374 6174 7573 2e6f 7267 2f62 6164  postatus.org/bad
 000004e0: 6765 732f 6c61 7465 7374 2f61 6374 6976  ges/latest/activ
 000004f0: 652e 7376 6729 5d28 6874 7470 3a2f 2f77  e.svg)](http://w
 00000500: 7777 2e72 6570 6f73 7461 7475 732e 6f72  ww.repostatus.or
-00000510: 672f 2361 6374 6976 6529 0d0a 5b21 5b43  g/#active)..[![C
-00000520: 6f6c 6162 5d28 6874 7470 733a 2f2f 636f  olab](https://co
-00000530: 6c61 622e 7265 7365 6172 6368 2e67 6f6f  lab.research.goo
-00000540: 676c 652e 636f 6d2f 6173 7365 7473 2f63  gle.com/assets/c
-00000550: 6f6c 6162 2d62 6164 6765 2e73 7667 3f6c  olab-badge.svg?l
-00000560: 6f67 6f3d 6769 7468 7562 2532 3073 706f  ogo=github%20spo
-00000570: 6e73 6f72 7329 5d28 6874 7470 733a 2f2f  nsors)](https://
-00000580: 6572 646f 6761 6e74 2e67 6974 6875 622e  erdogant.github.
-00000590: 696f 2f64 6174 617a 6574 732f 7061 6765  io/datazets/page
-000005a0: 732f 6874 6d6c 2f44 6f63 756d 656e 7461  s/html/Documenta
-000005b0: 7469 6f6e 2e68 746d 6c23 636f 6c61 622d  tion.html#colab-
-000005c0: 6e6f 7465 626f 6f6b 290d 0a21 5b47 6974  notebook)..![Git
-000005d0: 4875 6220 5265 706f 2073 7461 7273 5d28  Hub Repo stars](
-000005e0: 6874 7470 733a 2f2f 696d 672e 7368 6965  https://img.shie
-000005f0: 6c64 732e 696f 2f67 6974 6875 622f 7374  lds.io/github/st
-00000600: 6172 732f 6572 646f 6761 6e74 2f64 6174  ars/erdogant/dat
-00000610: 617a 6574 7329 0d0a 215b 4769 7448 7562  azets)..![GitHub
-00000620: 2072 6570 6f20 7369 7a65 5d28 6874 7470   repo size](http
-00000630: 733a 2f2f 696d 672e 7368 6965 6c64 732e  s://img.shields.
-00000640: 696f 2f67 6974 6875 622f 7265 706f 2d73  io/github/repo-s
-00000650: 697a 652f 6572 646f 6761 6e74 2f64 6174  ize/erdogant/dat
-00000660: 617a 6574 7329 0d0a 5b21 5b44 6f6e 6174  azets)..[![Donat
-00000670: 655d 2868 7474 7073 3a2f 2f69 6d67 2e73  e](https://img.s
-00000680: 6869 656c 6473 2e69 6f2f 6261 6467 652f  hields.io/badge/
-00000690: 5375 7070 6f72 7425 3230 7468 6973 2532  Support%20this%2
-000006a0: 3070 726f 6a65 6374 2d67 7265 792e 7376  0project-grey.sv
-000006b0: 673f 6c6f 676f 3d67 6974 6875 6225 3230  g?logo=github%20
-000006c0: 7370 6f6e 736f 7273 295d 2868 7474 7073  sponsors)](https
-000006d0: 3a2f 2f65 7264 6f67 616e 742e 6769 7468  ://erdogant.gith
-000006e0: 7562 2e69 6f2f 6461 7461 7a65 7473 2f70  ub.io/datazets/p
-000006f0: 6167 6573 2f68 746d 6c2f 446f 6375 6d65  ages/html/Docume
-00000700: 6e74 6174 696f 6e2e 6874 6d6c 2329 0d0a  ntation.html#)..
-00000710: 3c21 2d2d 2d5b 215b 4275 794d 6543 6f66  <!---[![BuyMeCof
-00000720: 6665 655d 2868 7474 7073 3a2f 2f69 6d67  fee](https://img
-00000730: 2e73 6869 656c 6473 2e69 6f2f 6261 6467  .shields.io/badg
-00000740: 652f 6275 796d 6561 2d63 6f66 6665 652d  e/buymea-coffee-
-00000750: 7965 6c6c 6f77 2e73 7667 295d 2868 7474  yellow.svg)](htt
-00000760: 7073 3a2f 2f77 7777 2e62 7579 6d65 6163  ps://www.buymeac
-00000770: 6f66 6665 652e 636f 6d2f 6572 646f 6761  offee.com/erdoga
-00000780: 6e74 292d 2d3e 0d0a 3c21 2d2d 2d5b 215b  nt)-->..<!---[![
-00000790: 436f 6666 6565 5d28 6874 7470 733a 2f2f  Coffee](https://
-000007a0: 696d 672e 7368 6965 6c64 732e 696f 2f62  img.shields.io/b
-000007b0: 6164 6765 2f63 6f66 6665 652d 626c 6163  adge/coffee-blac
-000007c0: 6b2d 6772 6579 2e73 7667 295d 2868 7474  k-grey.svg)](htt
-000007d0: 7073 3a2f 2f65 7264 6f67 616e 742e 6769  ps://erdogant.gi
-000007e0: 7468 7562 2e69 6f2f 646f 6e61 7465 2f3f  thub.io/donate/?
-000007f0: 6375 7272 656e 6379 3d55 5344 2661 6d6f  currency=USD&amo
-00000800: 756e 743d 3529 2d2d 3e0d 0a0d 0a0d 0a0d  unt=5)-->.......
-00000810: 0a0d 0a0d 0a3c 212d 2d2d 5b21 5b42 7579  .....<!---[![Buy
-00000820: 4d65 436f 6666 6565 5d28 6874 7470 733a  MeCoffee](https:
-00000830: 2f2f 696d 672e 7368 6965 6c64 732e 696f  //img.shields.io
-00000840: 2f62 6164 6765 2f62 7579 6d65 612d 636f  /badge/buymea-co
-00000850: 6666 6565 2d79 656c 6c6f 772e 7376 6729  ffee-yellow.svg)
-00000860: 5d28 6874 7470 733a 2f2f 7777 772e 6275  ](https://www.bu
-00000870: 796d 6561 636f 6666 6565 2e63 6f6d 2f65  ymeacoffee.com/e
-00000880: 7264 6f67 616e 7429 2d2d 3e0d 0a3c 212d  rdogant)-->..<!-
-00000890: 2d2d 5b21 5b43 6f66 6665 655d 2868 7474  --[![Coffee](htt
-000008a0: 7073 3a2f 2f69 6d67 2e73 6869 656c 6473  ps://img.shields
-000008b0: 2e69 6f2f 6261 6467 652f 636f 6666 6565  .io/badge/coffee
-000008c0: 2d62 6c61 636b 2d67 7265 792e 7376 6729  -black-grey.svg)
-000008d0: 5d28 6874 7470 733a 2f2f 6572 646f 6761  ](https://erdoga
-000008e0: 6e74 2e67 6974 6875 622e 696f 2f64 6f6e  nt.github.io/don
-000008f0: 6174 652f 3f63 7572 7265 6e63 793d 5553  ate/?currency=US
-00000900: 4426 616d 6f75 6e74 3d35 292d 2d3e 0d0a  D&amount=5)-->..
-00000910: 0d0a 2a20 6060 6461 7461 7a65 7473 6060  ..* ``datazets``
-00000920: 2069 7320 5079 7468 6f6e 2070 6163 6b61   is Python packa
-00000930: 6765 0d0a 0d0a 2320 0d0a 2a2a 5374 6172  ge....# ..**Star
-00000940: 2074 6869 7320 7265 706f 2069 6620 796f   this repo if yo
-00000950: 7520 6c69 6b65 2069 7421 20e2 ad90 efb8  u like it! .....
-00000960: 8f2a 2a0d 0a23 0d0a 0d0a 2323 2320 436f  .**..#....### Co
-00000970: 6e74 656e 7473 0d0a 2d20 5b49 6e73 7461  ntents..- [Insta
-00000980: 6c6c 6174 696f 6e5d 2823 2d69 6e73 7461  llation](#-insta
-00000990: 6c6c 6174 696f 6e29 0d0a 2d20 5b43 6f6e  llation)..- [Con
-000009a0: 7472 6962 7574 655d 2823 2d63 6f6e 7472  tribute](#-contr
-000009b0: 6962 7574 6529 0d0a 2d20 5b43 6974 6174  ibute)..- [Citat
-000009c0: 696f 6e5d 2823 2d63 6974 6174 696f 6e29  ion](#-citation)
-000009d0: 0d0a 2d20 5b4d 6169 6e74 6169 6e65 7273  ..- [Maintainers
-000009e0: 5d28 232d 6d61 696e 7461 696e 6572 7329  ](#-maintainers)
-000009f0: 0d0a 2d20 5b4c 6963 656e 7365 5d28 232d  ..- [License](#-
-00000a00: 636f 7079 7269 6768 7429 0d0a 0d0a 2323  copyright)....##
-00000a10: 2320 496e 7374 616c 6c61 7469 6f6e 0d0a  # Installation..
-00000a20: 2a20 496e 7374 616c 6c20 6461 7461 7a65  * Install dataze
-00000a30: 7473 2066 726f 6d20 5079 5049 2028 7265  ts from PyPI (re
-00000a40: 636f 6d6d 656e 6465 6429 2e20 6461 7461  commended). data
-00000a50: 7a65 7473 2069 7320 636f 6d70 6174 6962  zets is compatib
-00000a60: 6c65 2077 6974 6820 5079 7468 6f6e 2033  le with Python 3
-00000a70: 2e36 2b20 616e 6420 7275 6e73 206f 6e20  .6+ and runs on 
-00000a80: 4c69 6e75 782c 204d 6163 4f53 2058 2061  Linux, MacOS X a
-00000a90: 6e64 2057 696e 646f 7773 2e20 0d0a 2a20  nd Windows. ..* 
-00000aa0: 4120 6e65 7720 656e 7669 726f 6e6d 656e  A new environmen
-00000ab0: 7420 6361 6e20 6265 2063 7265 6174 6564  t can be created
-00000ac0: 2061 7320 666f 6c6c 6f77 696e 673a 0d0a   as following:..
-00000ad0: 0d0a 6060 6062 6173 680d 0a63 6f6e 6461  ..```bash..conda
-00000ae0: 2063 7265 6174 6520 2d6e 2065 6e76 5f64   create -n env_d
-00000af0: 6174 617a 6574 7320 7079 7468 6f6e 3d33  atazets python=3
-00000b00: 2e38 0d0a 636f 6e64 6120 6163 7469 7661  .8..conda activa
-00000b10: 7465 2065 6e76 5f64 6174 617a 6574 730d  te env_datazets.
-00000b20: 0a60 6060 0d0a 0d0a 6060 6062 6173 680d  .```....```bash.
-00000b30: 0a70 6970 2069 6e73 7461 6c6c 2064 6174  .pip install dat
-00000b40: 617a 6574 7320 2020 2020 2020 2020 2020  azets           
-00000b50: 2023 206e 6f72 6d61 6c20 696e 7374 616c   # normal instal
-00000b60: 6c0d 0a70 6970 2069 6e73 7461 6c6c 202d  l..pip install -
-00000b70: 2d75 7067 7261 6465 2064 6174 617a 6574  -upgrade datazet
-00000b80: 7320 2320 6f72 2075 7064 6174 6520 6966  s # or update if
-00000b90: 206e 6565 6465 640d 0a60 6060 0d0a 0d0a   needed..```....
-00000ba0: 2a20 416c 7465 726e 6174 6976 656c 792c  * Alternatively,
-00000bb0: 2079 6f75 2063 616e 2069 6e73 7461 6c6c   you can install
-00000bc0: 2066 726f 6d20 7468 6520 4769 7448 7562   from the GitHub
-00000bd0: 2073 6f75 7263 653a 0d0a 6060 6062 6173   source:..```bas
-00000be0: 680d 0a23 2044 6972 6563 746c 7920 696e  h..# Directly in
-00000bf0: 7374 616c 6c20 6672 6f6d 2067 6974 6875  stall from githu
-00000c00: 6220 736f 7572 6365 0d0a 7069 7020 696e  b source..pip in
-00000c10: 7374 616c 6c20 2d65 2067 6974 3a2f 2f67  stall -e git://g
-00000c20: 6974 6875 622e 636f 6d2f 6572 646f 6761  ithub.com/erdoga
-00000c30: 6e74 2f64 6174 617a 6574 732e 6769 7440  nt/datazets.git@
-00000c40: 302e 312e 3023 6567 673d 6d61 7374 6572  0.1.0#egg=master
-00000c50: 0d0a 7069 7020 696e 7374 616c 6c20 6769  ..pip install gi
-00000c60: 742b 6874 7470 733a 2f2f 6769 7468 7562  t+https://github
-00000c70: 2e63 6f6d 2f65 7264 6f67 616e 742f 6461  .com/erdogant/da
-00000c80: 7461 7a65 7473 2365 6767 3d6d 6173 7465  tazets#egg=maste
-00000c90: 720d 0a70 6970 2069 6e73 7461 6c6c 2067  r..pip install g
-00000ca0: 6974 2b68 7474 7073 3a2f 2f67 6974 6875  it+https://githu
-00000cb0: 622e 636f 6d2f 6572 646f 6761 6e74 2f64  b.com/erdogant/d
-00000cc0: 6174 617a 6574 730d 0a0d 0a23 2042 7920  atazets....# By 
-00000cd0: 636c 6f6e 696e 670d 0a67 6974 2063 6c6f  cloning..git clo
-00000ce0: 6e65 2068 7474 7073 3a2f 2f67 6974 6875  ne https://githu
-00000cf0: 622e 636f 6d2f 6572 646f 6761 6e74 2f64  b.com/erdogant/d
-00000d00: 6174 617a 6574 732e 6769 740d 0a63 6420  atazets.git..cd 
-00000d10: 6461 7461 7a65 7473 0d0a 7069 7020 696e  datazets..pip in
-00000d20: 7374 616c 6c20 2d55 202e 0d0a 6060 6020  stall -U ...``` 
-00000d30: 200d 0a0d 0a23 2323 2320 496d 706f 7274   ....#### Import
-00000d40: 2064 6174 617a 6574 730d 0a60 6060 7079   datazets..```py
-00000d50: 7468 6f6e 0d0a 2320 496d 706f 7274 206c  thon..# Import l
-00000d60: 6962 7261 7279 0d0a 696d 706f 7274 2064  ibrary..import d
-00000d70: 6174 617a 6574 7320 6173 2064 7a0d 0a23  atazets as dz..#
-00000d80: 2049 6d70 6f72 7420 6461 7461 2073 6574   Import data set
-00000d90: 0d0a 6466 203d 2064 7a2e 6765 7428 2774  ..df = dz.get('t
-00000da0: 6974 616e 6963 2729 0d0a 0d0a 6060 600d  itanic')....```.
-00000db0: 0a0d 0a23 2323 2320 4578 616d 706c 653a  ...#### Example:
-00000dc0: 0d0a 6060 6070 7974 686f 6e0d 0a0d 0a23  ..```python....#
-00000dd0: 2049 6d70 6f72 7420 6672 6f6d 2075 726c   Import from url
-00000de0: 0d0a 7572 6c3d 2768 7474 7073 3a2f 2f61  ..url='https://a
-00000df0: 7263 6869 7665 2e69 6373 2e75 6369 2e65  rchive.ics.uci.e
-00000e00: 6475 2f6d 6c2f 6d61 6368 696e 652d 6c65  du/ml/machine-le
-00000e10: 6172 6e69 6e67 2d64 6174 6162 6173 6573  arning-databases
-00000e20: 2f61 6475 6c74 2f61 6475 6c74 2e64 6174  /adult/adult.dat
-00000e30: 6127 0d0a 6466 203d 2064 7a2e 6765 7428  a'..df = dz.get(
-00000e40: 7572 6c3d 7572 6c2c 2073 6570 3d27 2c27  url=url, sep=','
-00000e50: 290d 0a60 6060 0d0a 3c70 2061 6c69 676e  )..```..<p align
-00000e60: 3d22 6365 6e74 6572 223e 0d0a 2020 3c69  ="center">..  <i
-00000e70: 6d67 2073 7263 3d22 6874 7470 733a 2f2f  mg src="https://
-00000e80: 6769 7468 7562 2e63 6f6d 2f65 7264 6f67  github.com/erdog
-00000e90: 616e 742f 6461 7461 7a65 7473 2f62 6c6f  ant/datazets/blo
-00000ea0: 622f 6d61 7374 6572 2f64 6f63 732f 6669  b/master/docs/fi
-00000eb0: 6773 2f66 6967 312e 706e 6722 2077 6964  gs/fig1.png" wid
-00000ec0: 7468 3d22 3630 3022 202f 3e0d 0a20 200d  th="600" />..  .
-00000ed0: 0a3c 2f70 3e0d 0a0d 0a0d 0a23 2323 2320  .</p>......#### 
-00000ee0: 5265 6665 7265 6e63 6573 0d0a 2a20 6874  References..* ht
-00000ef0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
-00000f00: 2f65 7264 6f67 616e 742f 6461 7461 7a65  /erdogant/dataze
-00000f10: 7473 0d0a 0d0a 2323 2323 2043 6974 6174  ts....#### Citat
-00000f20: 696f 6e0d 0a50 6c65 6173 6520 6369 7465  ion..Please cite
-00000f30: 2069 6e20 796f 7572 2070 7562 6c69 6361   in your publica
-00000f40: 7469 6f6e 7320 6966 2074 6869 7320 6973  tions if this is
-00000f50: 2075 7365 6675 6c20 666f 7220 796f 7572   useful for your
-00000f60: 2072 6573 6561 7263 6820 2873 6565 2063   research (see c
-00000f70: 6974 6174 696f 6e29 2e0d 0a20 2020 0d0a  itation)...   ..
-00000f80: 2323 2320 4d61 696e 7461 696e 6572 730d  ### Maintainers.
-00000f90: 0a2a 2045 7264 6f67 616e 2054 6173 6b65  .* Erdogan Taske
-00000fa0: 7365 6e2c 2067 6974 6875 623a 205b 6572  sen, github: [er
-00000fb0: 646f 6761 6e74 5d28 6874 7470 733a 2f2f  dogant](https://
-00000fc0: 6769 7468 7562 2e63 6f6d 2f65 7264 6f67  github.com/erdog
-00000fd0: 616e 7429 0d0a 0d0a 2323 2320 436f 6e74  ant)....### Cont
-00000fe0: 7269 6275 7465 0d0a 2a20 416c 6c20 6b69  ribute..* All ki
-00000ff0: 6e64 7320 6f66 2063 6f6e 7472 6962 7574  nds of contribut
-00001000: 696f 6e73 2061 7265 2077 656c 636f 6d65  ions are welcome
-00001010: 210d 0a2a 2049 6620 796f 7520 7769 7368  !..* If you wish
-00001020: 2074 6f20 6275 7920 6d65 2061 203c 6120   to buy me a <a 
-00001030: 6872 6566 3d22 6874 7470 733a 2f2f 7777  href="https://ww
-00001040: 772e 6275 796d 6561 636f 6666 6565 2e63  w.buymeacoffee.c
-00001050: 6f6d 2f65 7264 6f67 616e 7422 3e43 6f66  om/erdogant">Cof
-00001060: 6665 653c 2f61 3e20 666f 7220 7468 6973  fee</a> for this
-00001070: 2077 6f72 6b2c 2069 7420 6973 2076 6572   work, it is ver
-00001080: 7920 6170 7072 6563 6961 7465 6420 3a29  y appreciated :)
-00001090: 0d0a 0d0a 2323 2320 4c69 6365 6e63 650d  ....### Licence.
-000010a0: 0a53 6565 205b 4c49 4345 4e53 455d 284c  .See [LICENSE](L
-000010b0: 4943 454e 5345 2920 666f 7220 6465 7461  ICENSE) for deta
-000010c0: 696c 732e 0d0a                           ils...
+00000510: 672f 2361 6374 6976 6529 0d0a 215b 4769  g/#active)..![Gi
+00000520: 7448 7562 2052 6570 6f20 7374 6172 735d  tHub Repo stars]
+00000530: 2868 7474 7073 3a2f 2f69 6d67 2e73 6869  (https://img.shi
+00000540: 656c 6473 2e69 6f2f 6769 7468 7562 2f73  elds.io/github/s
+00000550: 7461 7273 2f65 7264 6f67 616e 742f 6461  tars/erdogant/da
+00000560: 7461 7a65 7473 290d 0a21 5b47 6974 4875  tazets)..![GitHu
+00000570: 6220 7265 706f 2073 697a 655d 2868 7474  b repo size](htt
+00000580: 7073 3a2f 2f69 6d67 2e73 6869 656c 6473  ps://img.shields
+00000590: 2e69 6f2f 6769 7468 7562 2f72 6570 6f2d  .io/github/repo-
+000005a0: 7369 7a65 2f65 7264 6f67 616e 742f 6461  size/erdogant/da
+000005b0: 7461 7a65 7473 290d 0a5b 215b 446f 6e61  tazets)..[![Dona
+000005c0: 7465 5d28 6874 7470 733a 2f2f 696d 672e  te](https://img.
+000005d0: 7368 6965 6c64 732e 696f 2f62 6164 6765  shields.io/badge
+000005e0: 2f53 7570 706f 7274 2532 3074 6869 7325  /Support%20this%
+000005f0: 3230 7072 6f6a 6563 742d 6772 6579 2e73  20project-grey.s
+00000600: 7667 3f6c 6f67 6f3d 6769 7468 7562 2532  vg?logo=github%2
+00000610: 3073 706f 6e73 6f72 7329 5d28 6874 7470  0sponsors)](http
+00000620: 733a 2f2f 6572 646f 6761 6e74 2e67 6974  s://erdogant.git
+00000630: 6875 622e 696f 2f64 6174 617a 6574 732f  hub.io/datazets/
+00000640: 7061 6765 732f 6874 6d6c 2f44 6f63 756d  pages/html/Docum
+00000650: 656e 7461 7469 6f6e 2e68 746d 6c23 290d  entation.html#).
+00000660: 0a3c 212d 2d2d 5b21 5b42 7579 4d65 436f  .<!---[![BuyMeCo
+00000670: 6666 6565 5d28 6874 7470 733a 2f2f 696d  ffee](https://im
+00000680: 672e 7368 6965 6c64 732e 696f 2f62 6164  g.shields.io/bad
+00000690: 6765 2f62 7579 6d65 612d 636f 6666 6565  ge/buymea-coffee
+000006a0: 2d79 656c 6c6f 772e 7376 6729 5d28 6874  -yellow.svg)](ht
+000006b0: 7470 733a 2f2f 7777 772e 6275 796d 6561  tps://www.buymea
+000006c0: 636f 6666 6565 2e63 6f6d 2f65 7264 6f67  coffee.com/erdog
+000006d0: 616e 7429 2d2d 3e0d 0a3c 212d 2d2d 5b21  ant)-->..<!---[!
+000006e0: 5b43 6f66 6665 655d 2868 7474 7073 3a2f  [Coffee](https:/
+000006f0: 2f69 6d67 2e73 6869 656c 6473 2e69 6f2f  /img.shields.io/
+00000700: 6261 6467 652f 636f 6666 6565 2d62 6c61  badge/coffee-bla
+00000710: 636b 2d67 7265 792e 7376 6729 5d28 6874  ck-grey.svg)](ht
+00000720: 7470 733a 2f2f 6572 646f 6761 6e74 2e67  tps://erdogant.g
+00000730: 6974 6875 622e 696f 2f64 6f6e 6174 652f  ithub.io/donate/
+00000740: 3f63 7572 7265 6e63 793d 5553 4426 616d  ?currency=USD&am
+00000750: 6f75 6e74 3d35 292d 2d3e 0d0a 0d0a 0d0a  ount=5)-->......
+00000760: 0d0a 0d0a 0d0a 3c21 2d2d 2d5b 215b 4275  ......<!---[![Bu
+00000770: 794d 6543 6f66 6665 655d 2868 7474 7073  yMeCoffee](https
+00000780: 3a2f 2f69 6d67 2e73 6869 656c 6473 2e69  ://img.shields.i
+00000790: 6f2f 6261 6467 652f 6275 796d 6561 2d63  o/badge/buymea-c
+000007a0: 6f66 6665 652d 7965 6c6c 6f77 2e73 7667  offee-yellow.svg
+000007b0: 295d 2868 7474 7073 3a2f 2f77 7777 2e62  )](https://www.b
+000007c0: 7579 6d65 6163 6f66 6665 652e 636f 6d2f  uymeacoffee.com/
+000007d0: 6572 646f 6761 6e74 292d 2d3e 0d0a 3c21  erdogant)-->..<!
+000007e0: 2d2d 2d5b 215b 436f 6666 6565 5d28 6874  ---[![Coffee](ht
+000007f0: 7470 733a 2f2f 696d 672e 7368 6965 6c64  tps://img.shield
+00000800: 732e 696f 2f62 6164 6765 2f63 6f66 6665  s.io/badge/coffe
+00000810: 652d 626c 6163 6b2d 6772 6579 2e73 7667  e-black-grey.svg
+00000820: 295d 2868 7474 7073 3a2f 2f65 7264 6f67  )](https://erdog
+00000830: 616e 742e 6769 7468 7562 2e69 6f2f 646f  ant.github.io/do
+00000840: 6e61 7465 2f3f 6375 7272 656e 6379 3d55  nate/?currency=U
+00000850: 5344 2661 6d6f 756e 743d 3529 2d2d 3e0d  SD&amount=5)-->.
+00000860: 0a0d 0a2a 2060 6064 6174 617a 6574 7360  ...* ``datazets`
+00000870: 6020 6973 2050 7974 686f 6e20 7061 636b  ` is Python pack
+00000880: 6167 650d 0a0d 0a23 200d 0a2a 2a53 7461  age....# ..**Sta
+00000890: 7220 7468 6973 2072 6570 6f20 6966 2079  r this repo if y
+000008a0: 6f75 206c 696b 6520 6974 2120 e2ad 90ef  ou like it! ....
+000008b0: b88f 2a2a 0d0a 230d 0a0d 0a23 2323 2043  ..**..#....### C
+000008c0: 6f6e 7465 6e74 730d 0a2d 205b 496e 7374  ontents..- [Inst
+000008d0: 616c 6c61 7469 6f6e 5d28 232d 696e 7374  allation](#-inst
+000008e0: 616c 6c61 7469 6f6e 290d 0a2d 205b 436f  allation)..- [Co
+000008f0: 6e74 7269 6275 7465 5d28 232d 636f 6e74  ntribute](#-cont
+00000900: 7269 6275 7465 290d 0a2d 205b 4369 7461  ribute)..- [Cita
+00000910: 7469 6f6e 5d28 232d 6369 7461 7469 6f6e  tion](#-citation
+00000920: 290d 0a2d 205b 4d61 696e 7461 696e 6572  )..- [Maintainer
+00000930: 735d 2823 2d6d 6169 6e74 6169 6e65 7273  s](#-maintainers
+00000940: 290d 0a2d 205b 4c69 6365 6e73 655d 2823  )..- [License](#
+00000950: 2d63 6f70 7972 6967 6874 290d 0a0d 0a23  -copyright)....#
+00000960: 2323 2049 6e73 7461 6c6c 6174 696f 6e0d  ## Installation.
+00000970: 0a2a 2049 6e73 7461 6c6c 2064 6174 617a  .* Install dataz
+00000980: 6574 7320 6672 6f6d 2050 7950 4920 2872  ets from PyPI (r
+00000990: 6563 6f6d 6d65 6e64 6564 292e 2064 6174  ecommended). dat
+000009a0: 617a 6574 7320 6973 2063 6f6d 7061 7469  azets is compati
+000009b0: 626c 6520 7769 7468 2050 7974 686f 6e20  ble with Python 
+000009c0: 332e 362b 2061 6e64 2072 756e 7320 6f6e  3.6+ and runs on
+000009d0: 204c 696e 7578 2c20 4d61 634f 5320 5820   Linux, MacOS X 
+000009e0: 616e 6420 5769 6e64 6f77 732e 200d 0a2a  and Windows. ..*
+000009f0: 2041 206e 6577 2065 6e76 6972 6f6e 6d65   A new environme
+00000a00: 6e74 2063 616e 2062 6520 6372 6561 7465  nt can be create
+00000a10: 6420 6173 2066 6f6c 6c6f 7769 6e67 3a0d  d as following:.
+00000a20: 0a0d 0a60 6060 6261 7368 0d0a 636f 6e64  ...```bash..cond
+00000a30: 6120 6372 6561 7465 202d 6e20 656e 765f  a create -n env_
+00000a40: 6461 7461 7a65 7473 2070 7974 686f 6e3d  datazets python=
+00000a50: 332e 380d 0a63 6f6e 6461 2061 6374 6976  3.8..conda activ
+00000a60: 6174 6520 656e 765f 6461 7461 7a65 7473  ate env_datazets
+00000a70: 0d0a 6060 600d 0a0d 0a60 6060 6261 7368  ..```....```bash
+00000a80: 0d0a 7069 7020 696e 7374 616c 6c20 6461  ..pip install da
+00000a90: 7461 7a65 7473 2020 2020 2020 2020 2020  tazets          
+00000aa0: 2020 2320 6e6f 726d 616c 2069 6e73 7461    # normal insta
+00000ab0: 6c6c 0d0a 7069 7020 696e 7374 616c 6c20  ll..pip install 
+00000ac0: 2d2d 7570 6772 6164 6520 6461 7461 7a65  --upgrade dataze
+00000ad0: 7473 2023 206f 7220 7570 6461 7465 2069  ts # or update i
+00000ae0: 6620 6e65 6564 6564 0d0a 6060 600d 0a0d  f needed..```...
+00000af0: 0a2a 2041 6c74 6572 6e61 7469 7665 6c79  .* Alternatively
+00000b00: 2c20 796f 7520 6361 6e20 696e 7374 616c  , you can instal
+00000b10: 6c20 6672 6f6d 2074 6865 2047 6974 4875  l from the GitHu
+00000b20: 6220 736f 7572 6365 3a0d 0a60 6060 6261  b source:..```ba
+00000b30: 7368 0d0a 2320 4469 7265 6374 6c79 2069  sh..# Directly i
+00000b40: 6e73 7461 6c6c 2066 726f 6d20 6769 7468  nstall from gith
+00000b50: 7562 2073 6f75 7263 650d 0a70 6970 2069  ub source..pip i
+00000b60: 6e73 7461 6c6c 202d 6520 6769 743a 2f2f  nstall -e git://
+00000b70: 6769 7468 7562 2e63 6f6d 2f65 7264 6f67  github.com/erdog
+00000b80: 616e 742f 6461 7461 7a65 7473 2e67 6974  ant/datazets.git
+00000b90: 4030 2e31 2e30 2365 6767 3d6d 6173 7465  @0.1.0#egg=maste
+00000ba0: 720d 0a70 6970 2069 6e73 7461 6c6c 2067  r..pip install g
+00000bb0: 6974 2b68 7474 7073 3a2f 2f67 6974 6875  it+https://githu
+00000bc0: 622e 636f 6d2f 6572 646f 6761 6e74 2f64  b.com/erdogant/d
+00000bd0: 6174 617a 6574 7323 6567 673d 6d61 7374  atazets#egg=mast
+00000be0: 6572 0d0a 7069 7020 696e 7374 616c 6c20  er..pip install 
+00000bf0: 6769 742b 6874 7470 733a 2f2f 6769 7468  git+https://gith
+00000c00: 7562 2e63 6f6d 2f65 7264 6f67 616e 742f  ub.com/erdogant/
+00000c10: 6461 7461 7a65 7473 0d0a 0d0a 2320 4279  datazets....# By
+00000c20: 2063 6c6f 6e69 6e67 0d0a 6769 7420 636c   cloning..git cl
+00000c30: 6f6e 6520 6874 7470 733a 2f2f 6769 7468  one https://gith
+00000c40: 7562 2e63 6f6d 2f65 7264 6f67 616e 742f  ub.com/erdogant/
+00000c50: 6461 7461 7a65 7473 2e67 6974 0d0a 6364  datazets.git..cd
+00000c60: 2064 6174 617a 6574 730d 0a70 6970 2069   datazets..pip i
+00000c70: 6e73 7461 6c6c 202d 5520 2e0d 0a60 6060  nstall -U ...```
+00000c80: 2020 0d0a 0d0a 2323 2323 2049 6d70 6f72    ....#### Impor
+00000c90: 7420 6461 7461 7a65 7473 0d0a 6060 6070  t datazets..```p
+00000ca0: 7974 686f 6e0d 0a23 2049 6d70 6f72 7420  ython..# Import 
+00000cb0: 6c69 6272 6172 790d 0a69 6d70 6f72 7420  library..import 
+00000cc0: 6461 7461 7a65 7473 2061 7320 647a 0d0a  datazets as dz..
+00000cd0: 2320 496d 706f 7274 2064 6174 6120 7365  # Import data se
+00000ce0: 740d 0a64 6620 3d20 647a 2e67 6574 2827  t..df = dz.get('
+00000cf0: 7469 7461 6e69 6327 290d 0a0d 0a60 6060  titanic')....```
+00000d00: 0d0a 0d0a 2323 2323 2045 7861 6d70 6c65  ....#### Example
+00000d10: 3a0d 0a60 6060 7079 7468 6f6e 0d0a 0d0a  :..```python....
+00000d20: 2320 496d 706f 7274 2066 726f 6d20 7572  # Import from ur
+00000d30: 6c0d 0a75 726c 3d27 6874 7470 733a 2f2f  l..url='https://
+00000d40: 6172 6368 6976 652e 6963 732e 7563 692e  archive.ics.uci.
+00000d50: 6564 752f 6d6c 2f6d 6163 6869 6e65 2d6c  edu/ml/machine-l
+00000d60: 6561 726e 696e 672d 6461 7461 6261 7365  earning-database
+00000d70: 732f 6164 756c 742f 6164 756c 742e 6461  s/adult/adult.da
+00000d80: 7461 270d 0a64 6620 3d20 647a 2e67 6574  ta'..df = dz.get
+00000d90: 2875 726c 3d75 726c 2c20 7365 703d 272c  (url=url, sep=',
+00000da0: 2729 0d0a 6060 600d 0a3c 7020 616c 6967  ')..```..<p alig
+00000db0: 6e3d 2263 656e 7465 7222 3e0d 0a20 203c  n="center">..  <
+00000dc0: 696d 6720 7372 633d 2268 7474 7073 3a2f  img src="https:/
+00000dd0: 2f67 6974 6875 622e 636f 6d2f 6572 646f  /github.com/erdo
+00000de0: 6761 6e74 2f64 6174 617a 6574 732f 626c  gant/datazets/bl
+00000df0: 6f62 2f6d 6173 7465 722f 646f 6373 2f66  ob/master/docs/f
+00000e00: 6967 732f 6669 6731 2e70 6e67 2220 7769  igs/fig1.png" wi
+00000e10: 6474 683d 2236 3030 2220 2f3e 0d0a 2020  dth="600" />..  
+00000e20: 0d0a 3c2f 703e 0d0a 0d0a 0d0a 2323 2323  ..</p>......####
+00000e30: 2043 6974 6174 696f 6e0d 0a50 6c65 6173   Citation..Pleas
+00000e40: 6520 6369 7465 2069 6e20 796f 7572 2070  e cite in your p
+00000e50: 7562 6c69 6361 7469 6f6e 7320 6966 2074  ublications if t
+00000e60: 6869 7320 6973 2075 7365 6675 6c20 666f  his is useful fo
+00000e70: 7220 796f 7572 2072 6573 6561 7263 6820  r your research 
+00000e80: 2873 6565 2063 6974 6174 696f 6e29 2e0d  (see citation)..
+00000e90: 0a20 2020 0d0a 2323 2320 4d61 696e 7461  .   ..### Mainta
+00000ea0: 696e 6572 730d 0a2a 2045 7264 6f67 616e  iners..* Erdogan
+00000eb0: 2054 6173 6b65 7365 6e2c 2067 6974 6875   Taskesen, githu
+00000ec0: 623a 205b 6572 646f 6761 6e74 5d28 6874  b: [erdogant](ht
+00000ed0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
+00000ee0: 2f65 7264 6f67 616e 7429 0d0a 0d0a 2323  /erdogant)....##
+00000ef0: 2320 436f 6e74 7269 6275 7465 0d0a 2a20  # Contribute..* 
+00000f00: 416c 6c20 6b69 6e64 7320 6f66 2063 6f6e  All kinds of con
+00000f10: 7472 6962 7574 696f 6e73 2061 7265 2077  tributions are w
+00000f20: 656c 636f 6d65 210d 0a2a 2049 6620 796f  elcome!..* If yo
+00000f30: 7520 7769 7368 2074 6f20 6275 7920 6d65  u wish to buy me
+00000f40: 2061 203c 6120 6872 6566 3d22 6874 7470   a <a href="http
+00000f50: 733a 2f2f 7777 772e 6275 796d 6561 636f  s://www.buymeaco
+00000f60: 6666 6565 2e63 6f6d 2f65 7264 6f67 616e  ffee.com/erdogan
+00000f70: 7422 3e43 6f66 6665 653c 2f61 3e20 666f  t">Coffee</a> fo
+00000f80: 7220 7468 6973 2077 6f72 6b2c 2069 7420  r this work, it 
+00000f90: 6973 2076 6572 7920 6170 7072 6563 6961  is very apprecia
+00000fa0: 7465 6420 3a29 0d0a 0d0a 2323 2320 4c69  ted :)....### Li
+00000fb0: 6365 6e63 650d 0a53 6565 205b 4c49 4345  cence..See [LICE
+00000fc0: 4e53 455d 284c 4943 454e 5345 2920 666f  NSE](LICENSE) fo
+00000fd0: 7220 6465 7461 696c 732e 0d0a            r details...
```

### Comparing `datazets-0.1.1/datazets/__init__.py` & `datazets-0.1.2/datazets/__init__.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from datazets.datazets import get
 
 
 __author__ = 'Erdogan Tasksen'
 __email__ = 'erdogant@gmail.com'
-__version__ = '0.1.1'
+__version__ = '0.1.2'
 
 # module level doc-string
 __doc__ = """
 datazets
 =====================================================================
 
 Description
```

### Comparing `datazets-0.1.1/datazets/datazets.py` & `datazets-0.1.2/datazets/datazets.py`

 * *Files 2% similar despite different names*

```diff
@@ -99,15 +99,15 @@
     """
     set_logger(verbose=verbose)
     if data is None and url is None:
         logger.error('Input parameter <data> or <url> should be used.')
         return None
 
     # Get and Set data information
-    file_data, url, datatype, sep = _set_names_and_url(data, url)
+    file_data, url, datatype, sep = _set_names_and_url(data, url, sep)
     logger.info('Import dataset [%s]' %(file_data))
 
     if url is None:
         logger.info('Nothing to download.')
         return None
 
     # Import dataset
@@ -172,20 +172,20 @@
     # Import local dataset
     image_files = listdir(dirpath)
     # Return
     return image_files
 
 
 # %%
-def _set_names_and_url(data, url):
-    sep=';'
+def _set_names_and_url(data, url, sep):
     datatype=None
 
     # Set names
     if data is not None:
+        sep=';'
         # Set datatype for imges
         if data=='flowers' or data=='faces' or data=='mnist' or data=='scenes':
             datatype='image'
         elif data=='random_discrete':
             datatype='synthetic'
         else:
             datatype='various'
```

### Comparing `datazets-0.1.1/datazets.egg-info/PKG-INFO` & `datazets-0.1.2/datazets.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: datazets
-Version: 0.1.1
+Version: 0.1.2
 Summary: Datazets is a python package to import well known example data sets.
 Home-page: https://github.com/erdogant/datazets
 Author: Erdogan Taskesen
 Author-email: erdogant@gmail.com
 License: UNKNOWN
-Download-URL: https://github.com/erdogant/datazets/archive/0.1.1.tar.gz
+Download-URL: https://github.com/erdogant/datazets/archive/0.1.2.tar.gz
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -23,15 +23,14 @@
 [![LOC](https://sloc.xyz/github/erdogant/datazets/?category=code)](https://github.com/erdogant/datazets/)
 [![Downloads](https://static.pepy.tech/personalized-badge/datazets?period=month&units=international_system&left_color=grey&right_color=brightgreen&left_text=PyPI%20downloads/month)](https://pepy.tech/project/datazets)
 [![Downloads](https://static.pepy.tech/personalized-badge/datazets?period=total&units=international_system&left_color=grey&right_color=brightgreen&left_text=Downloads)](https://pepy.tech/project/datazets)
 [![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/erdogant/datazets/blob/master/LICENSE)
 [![Forks](https://img.shields.io/github/forks/erdogant/datazets.svg)](https://github.com/erdogant/datazets/network)
 [![Issues](https://img.shields.io/github/issues/erdogant/datazets.svg)](https://github.com/erdogant/datazets/issues)
 [![Project Status](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
-[![Colab](https://colab.research.google.com/assets/colab-badge.svg?logo=github%20sponsors)](https://erdogant.github.io/datazets/pages/html/Documentation.html#colab-notebook)
 ![GitHub Repo stars](https://img.shields.io/github/stars/erdogant/datazets)
 ![GitHub repo size](https://img.shields.io/github/repo-size/erdogant/datazets)
 [![Donate](https://img.shields.io/badge/Support%20this%20project-grey.svg?logo=github%20sponsors)](https://erdogant.github.io/datazets/pages/html/Documentation.html#)
 <!---[![BuyMeCoffee](https://img.shields.io/badge/buymea-coffee-yellow.svg)](https://www.buymeacoffee.com/erdogant)-->
 <!---[![Coffee](https://img.shields.io/badge/coffee-black-grey.svg)](https://erdogant.github.io/donate/?currency=USD&amount=5)-->
 
 
@@ -99,17 +98,14 @@
 ```
 <p align="center">
   <img src="https://github.com/erdogant/datazets/blob/master/docs/figs/fig1.png" width="600" />
   
 </p>
 
 
-#### References
-* https://github.com/erdogant/datazets
-
 #### Citation
 Please cite in your publications if this is useful for your research (see citation).
    
 ### Maintainers
 * Erdogan Taskesen, github: [erdogant](https://github.com/erdogant)
 
 ### Contribute
```

### Comparing `datazets-0.1.1/setup.py` & `datazets-0.1.2/setup.py`

 * *Files identical despite different names*

