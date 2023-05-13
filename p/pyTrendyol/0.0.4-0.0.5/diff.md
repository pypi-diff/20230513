# Comparing `tmp/pyTrendyol-0.0.4.tar.gz` & `tmp/pyTrendyol-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyTrendyol-0.0.4.tar", last modified: Fri Feb 17 08:54:35 2023, max compression
+gzip compressed data, was "pyTrendyol-0.0.5.tar", last modified: Sat May 13 13:26:42 2023, max compression
```

## Comparing `pyTrendyol-0.0.4.tar` & `pyTrendyol-0.0.5.tar`

### file list

```diff
@@ -1,17 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-17 08:54:35.359303 pyTrendyol-0.0.4/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    51431 2023-02-17 08:54:35.359303 pyTrendyol-0.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    50837 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-17 08:54:35.359303 pyTrendyol-0.0.4/pyTrendyol/
--rw-r--r--   0 runner    (1001) docker     (123)     4019 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/pyTrendyol/Kategori.py
--rw-r--r--   0 runner    (1001) docker     (123)     4596 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/pyTrendyol/Urun.py
--rw-r--r--   0 runner    (1001) docker     (123)      155 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/pyTrendyol/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-17 08:54:35.359303 pyTrendyol-0.0.4/pyTrendyol.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    51431 2023-02-17 08:54:35.000000 pyTrendyol-0.0.4/pyTrendyol.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      272 2023-02-17 08:54:35.000000 pyTrendyol-0.0.4/pyTrendyol.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-17 08:54:35.000000 pyTrendyol-0.0.4/pyTrendyol.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       43 2023-02-17 08:54:35.000000 pyTrendyol-0.0.4/pyTrendyol.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-02-17 08:54:35.000000 pyTrendyol-0.0.4/pyTrendyol.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-17 08:54:35.359303 pyTrendyol-0.0.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1234 2023-02-17 08:54:17.000000 pyTrendyol-0.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:26:42.409001 pyTrendyol-0.0.5/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-05-13 13:26:42.409001 pyTrendyol-0.0.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3753 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:26:42.409001 pyTrendyol-0.0.5/pyTrendyol/
+-rw-r--r--   0 runner    (1001) docker     (123)     4135 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/pyTrendyol/Kategori.py
+-rw-r--r--   0 runner    (1001) docker     (123)      685 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/pyTrendyol/Modeller.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4691 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/pyTrendyol/Urun.py
+-rw-r--r--   0 runner    (1001) docker     (123)      155 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/pyTrendyol/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 13:26:42.409001 pyTrendyol-0.0.5/pyTrendyol.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-05-13 13:26:42.000000 pyTrendyol-0.0.5/pyTrendyol.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-05-13 13:26:42.000000 pyTrendyol-0.0.5/pyTrendyol.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 13:26:42.000000 pyTrendyol-0.0.5/pyTrendyol.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 13:26:42.000000 pyTrendyol-0.0.5/pyTrendyol.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-05-13 13:26:42.000000 pyTrendyol-0.0.5/pyTrendyol.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 13:26:42.409001 pyTrendyol-0.0.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1254 2023-05-13 13:26:18.000000 pyTrendyol-0.0.5/setup.py
```

### Comparing `pyTrendyol-0.0.4/LICENSE` & `pyTrendyol-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `pyTrendyol-0.0.4/pyTrendyol/Kategori.py` & `pyTrendyol-0.0.5/pyTrendyol/Kategori.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 # Bu araç @keyiflerolsun tarafından | @KekikAkademi için yazılmıştır.
 
-from Kekik    import slugify
-from requests import get
-from parsel   import Selector
+from Kekik               import slugify
+from requests            import get
+from parsel              import Selector
+from pyTrendyol.Modeller import KategoriUrun
 
 class Kategori:
     """
     Kategori : Trendyol'dan hedef kategori ürünlerini çevirir.
 
     Methodlar
     ----------
@@ -21,15 +22,15 @@
         return f"{__class__.__name__} Sınıfı -- Trendyol'dan hedef kategori ürünlerini çevirmek için kodlanmıştır."
 
     def __init__(self):
         """Trendyol'dan hedef kategori ürünlerini çevirir"""
         self.__kimlik = {"User-Agent": "pyTrendyol"}
         self.kategoriler = self.__kategoriler
 
-    def urunleri_ver(self, kategori_adi:str, sayfa_tara:int=1) -> list[dict] or None:
+    def urunleri_ver(self, kategori_adi:str, sayfa_tara:int=1) -> list[KategoriUrun] or None:
         """ilgili kategori ürünlerini istenilen sayfa sayısı boyunca listeler (her sayfada 24 ürün vardır.)"""
         kategori_adi = self.__ascii_decode(kategori_adi)
         if not self.mevcut_mu(kategori_adi):
             return None
 
         veriler = []
         for say in range(1, sayfa_tara+1):
@@ -42,23 +43,23 @@
                 yildiz_sayisi = 0
                 for i_yildiz in urun.xpath(".//div[@class='ratings']/div"):
                     yildiz = list(i_yildiz.xpath(".//div[@class='full' and @style='width:100%;max-width:100%']"))
 
                     yildiz_sayisi += len(yildiz)
 
                 urun_bilgileri = {
-                    "link"       : "https://www.trendyol.com" + urun.xpath(".//a/@href").get(),
+                    "link"       : "https://www.trendyol.com" + urun.xpath(".//a/@href").get().split("?")[0],
                     "marka"      : urun.xpath(".//span[@class='prdct-desc-cntnr-ttl']/text()").get(),
                     "yildiz"     : yildiz_sayisi,
                     "baslik"     : urun.xpath(".//span[@class='prdct-desc-cntnr-name hasRatings']/text()").get() or urun.xpath(".//span[@class='prdct-desc-cntnr-name']/text()").get(),
                     "indirim"    : urun.xpath("normalize-space(.//div[@class='pr-bx-pr-dsc-pr'])").get() or None,
                     "indirimsiz" : urun.xpath("normalize-space(.//div[@class='prc-box-sllng prc-box-sllng-w-dscntd'])").get() or None,
                     "fiyat"      : urun.xpath("normalize-space(.//div[@class='product-price'])").get() or urun.xpath("normalize-space(.//div[@class='prc-box-dscntd'])").get()
                 }
-                veriler.append(urun_bilgileri)
+                veriler.append(KategoriUrun(**urun_bilgileri))
             if sayfa_tara <= 1:
                 break
 
         return veriler
 
     def mevcut_mu(self, kategori_adi:str) -> bool:
         """mevcut kategorileri trendyol rss'inden ayrıştırıp çevirir"""
```

### Comparing `pyTrendyol-0.0.4/pyTrendyol/Urun.py` & `pyTrendyol-0.0.5/pyTrendyol/Urun.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 # Bu araç @keyiflerolsun tarafından | @KekikAkademi için yazılmıştır.
 
 from requests            import get
 from requests.exceptions import ConnectionError
 from urllib.parse        import unquote
 from re                  import search, search
 from parsel              import Selector
+from pyTrendyol.Modeller import UrunDetay, Yorum
 
 class Urun:
     """
     Urun : Trendyol'dan hedef ürün detaylarını çevirir.
 
     Methodlar
     ----------
@@ -37,52 +38,52 @@
             istek = get(link, headers=self.__kimlik, allow_redirects=True)
         except ConnectionError:
             return None
 
         secici = Selector(istek.text)
 
         try:
-            return {
+            return UrunDetay(**{
                 "link"       : link,
                 "marka"      : secici.xpath("//h1[@class='pr-new-br']/a/text()").get().strip() if secici.xpath("//h1[@class='pr-new-br']/a/text()").get() else secici.xpath("//h1[@class='pr-new-br']/text()").get().strip(),
                 "baslik"     : secici.xpath("//h1[@class='pr-new-br']/span/text()").get().strip(),
                 "resim"      : secici.xpath("//div[@class='gallery-modal-content']//img/@src").get(),
                 "gercek"     : secici.xpath("//span[@class='prc-org']/text()").get(),
                 "indirimli"  : secici.xpath("//span[@class='prc-slg prc-slg-w-dsc']/text()").get() or secici.xpath("//span[@class='prc-slg']/text()").get(),
                 "kampanya"   : secici.xpath("//div[@class='pr-bx-pr-dsc']/text()").get(),
                 "son_fiyat"  : secici.xpath("//span[@class='prc-dsc']/text()").get(),
                 "yorumlar"   : self.yorumlar(link),
-            }
+            })
         except AttributeError:
             return None
 
-    def yorumlar(self, urun_link:str) -> list[dict] or None:
+    def yorumlar(self, urun_link:str) -> list[Yorum] or None:
         """Trendyol'dan hedef ürün yorumlarını çevirir"""
         link = self._link_ayristir(urun_link)
         if not link:
             return None
 
         yorumlar = []
 
         url     = f"https://public-mdc.trendyol.com/discovery-web-socialgw-service/api/review/{link.split('-')[-1]}"
         istek   = get(url, headers=self.__kimlik)
         veriler = istek.json()["result"]["productReviews"]
 
         sayfa = 1
-        while True:
+        while veriler["content"]:
             yorumlar.extend(
-                {
+                Yorum(**{
                     "kullanici" : yorum["userFullName"],
                     "elit"      : yorum["isElite"],
                     "tarih"     : yorum["lastModifiedDate"],
                     "satici"    : yorum["sellerName"],
                     "yildiz"    : yorum["rate"],
                     "yorum"     : yorum["comment"]
-                }
-                    for yorum in veriler["content"]
+                })
+                    for yorum in veriler["content"] if yorum
             )
 
             sayfa += 1
             if sayfa == veriler["totalPages"]:
                 break
 
             istek   = get(f"{url}?page={sayfa}", headers=self.__kimlik)
```

### Comparing `pyTrendyol-0.0.4/setup.py` & `pyTrendyol-0.0.5/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 from setuptools import setup
 from io         import open
 
 setup(
     # ? Genel Bilgiler
     name         = "pyTrendyol",
-    version      = "0.0.4",
+    version      = "0.0.5",
     url          = "https://github.com/keyiflerolsun/pyTrendyol",
     description  = "Trendyol'dan veri almayı kolaylaştırmak için tasarlanan kütüphane.",
     keywords     = ["pyTrendyol", "KekikAkademi", "keyiflerolsun"],
 
     author       = "keyiflerolsun",
     author_email = "keyiflerolsun@gmail.com",
 
@@ -26,15 +26,16 @@
     python_requires  = ">=3.10",
     install_requires = [
         "pip",
         "setuptools",
         "wheel",
         "Kekik",
         "requests",
-        "parsel"
+        "parsel",
+        "pydantic"
     ],
 
     # ? PyPI Bilgileri
     long_description_content_type = "text/markdown",
     long_description              = "".join(open("README.md", encoding="utf-8").readlines()),
     include_package_data          = True
 )
```

