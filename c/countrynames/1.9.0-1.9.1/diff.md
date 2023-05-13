# Comparing `tmp/countrynames-1.9.0.tar.gz` & `tmp/countrynames-1.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "countrynames-1.9.0.tar", last modified: Tue Apr 13 06:19:13 2021, max compression
+gzip compressed data, was "countrynames-1.9.1.tar", last modified: Mon May  3 05:56:18 2021, max compression
```

## Comparing `countrynames-1.9.0.tar` & `countrynames-1.9.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-04-13 06:19:13.249325 countrynames-1.9.0/
--rw-r--r--   0 runner    (1001) docker     (121)       79 2021-04-13 06:18:54.000000 countrynames-1.9.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     3287 2021-04-13 06:19:13.249325 countrynames-1.9.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2206 2021-04-13 06:18:54.000000 countrynames-1.9.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-04-13 06:19:13.249325 countrynames-1.9.0/countrynames/
--rw-r--r--   0 runner    (1001) docker     (121)     3032 2021-04-13 06:18:54.000000 countrynames-1.9.0/countrynames/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)   597653 2021-04-13 06:18:54.000000 countrynames-1.9.0/countrynames/data.yaml
--rw-r--r--   0 runner    (1001) docker     (121)     4391 2021-04-13 06:18:54.000000 countrynames-1.9.0/countrynames/mappings.py
--rw-r--r--   0 runner    (1001) docker     (121)        0 2021-04-13 06:18:54.000000 countrynames-1.9.0/countrynames/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-04-13 06:19:13.249325 countrynames-1.9.0/countrynames.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3287 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      384 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/namespace_packages.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-04-13 06:19:07.000000 countrynames-1.9.0/countrynames.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (121)       65 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       13 2021-04-13 06:19:13.000000 countrynames-1.9.0/countrynames.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2021-04-13 06:19:13.249325 countrynames-1.9.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1319 2021-04-13 06:18:54.000000 countrynames-1.9.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-05-03 05:56:18.486107 countrynames-1.9.1/
+-rw-r--r--   0 runner    (1001) docker     (121)       79 2021-05-03 05:55:59.000000 countrynames-1.9.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)     3287 2021-05-03 05:56:18.486107 countrynames-1.9.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2206 2021-05-03 05:55:59.000000 countrynames-1.9.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-05-03 05:56:18.486107 countrynames-1.9.1/countrynames/
+-rw-r--r--   0 runner    (1001) docker     (121)     3032 2021-05-03 05:55:59.000000 countrynames-1.9.1/countrynames/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)   598871 2021-05-03 05:55:59.000000 countrynames-1.9.1/countrynames/data.yaml
+-rw-r--r--   0 runner    (1001) docker     (121)     4391 2021-05-03 05:55:59.000000 countrynames-1.9.1/countrynames/mappings.py
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2021-05-03 05:55:59.000000 countrynames-1.9.1/countrynames/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-05-03 05:56:18.486107 countrynames-1.9.1/countrynames.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     3287 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      384 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/namespace_packages.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-05-03 05:56:13.000000 countrynames-1.9.1/countrynames.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (121)       65 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       13 2021-05-03 05:56:18.000000 countrynames-1.9.1/countrynames.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2021-05-03 05:56:18.486107 countrynames-1.9.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1319 2021-05-03 05:55:59.000000 countrynames-1.9.1/setup.py
```

### Comparing `countrynames-1.9.0/PKG-INFO` & `countrynames-1.9.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: countrynames
-Version: 1.9.0
+Version: 1.9.1
 Summary: A library to map country names to ISO codes.
 Home-page: http://github.com/occrp/countrynames
 Author: Friedrich Lindenberg
 Author-email: friedrich@pudo.org
 License: MIT
 Description: # countrynames
```

### Comparing `countrynames-1.9.0/README.md` & `countrynames-1.9.1/README.md`

 * *Files identical despite different names*

### Comparing `countrynames-1.9.0/countrynames/__init__.py` & `countrynames-1.9.1/countrynames/__init__.py`

 * *Files identical despite different names*

### Comparing `countrynames-1.9.0/countrynames/data.yaml` & `countrynames-1.9.1/countrynames/data.yaml`

 * *Files 1% similar despite different names*

```diff
@@ -18,41 +18,46 @@
   - Africa
   - central america
   - southern america
   - N/A
   - na
   - n a
   - unknown
+  - unk
   - not applicable
   - overseas
   - not specified other
   - not specified
   - non specified
+  - stateless
 CN-XZ:
   - Tibet
 YUCS:
   - YUGOSLAVIA
   - YUGOSLAVIA (FORMER SOCIALIST FEDERAL REPUBLIC)
+  - Federal Republic of Yugoslavia
+  - Federal Socialist Republic of Yugoslavia
   - YU
   - YUG
 CSXX:
   - SERBIA AND MONTENEGRO
   - SERBIA & MONTENEGRO
-  - Federal Republic of Yugoslavia
   - Сербия и Черногория
   - Srbija i Crna Gora
   - Србија и Црна Гора
 SUHH:
   - Soviet Union
   - USSR
   - UdSSR
+  - SU
   - Union of Soviet Socialist Republics
   - Сове́тский Сою́з
   - Сою́з ССР
   - Сою́з Сове́тских Социалисти́ческих Респу́блик
+  - Russia (USSR)
 ANHH:
   - De Nederlandske Antiller
   - NETHERLAND ANTILLES
   - Netherlands Antilles
   - DUTCH ANTILLES
   - Antilles yr Iseldiroedd
 CSHH:
@@ -222,15 +227,24 @@
   - Down
   - Fermanagh
   - Londonderry
   - Derry
   - Tyrone
   - Irlanda del Norte
 MD-PMR:
+  - Шериф
   - Transnistria
+  - Transdniestria
+  - Stînga Nistrului
+  - Приднестровье
+  - Придністров'я
+  - Pridnestrovian Moldavian Republic
+  - Приднестровская Молдавская Республика
+  - Republica Moldovenească Nistreană
+  - Придністровська Молдавська Республіка
   - MDPMR
 AD:
   - Andɔr
   - អង់ដូរ៉ា
   - ઍંડોરા
   - Orílẹ́ède Ààndórà
   - ཨེན་ཌོ་ར།
@@ -460,14 +474,15 @@
   - Ηνωμένα Αραβικά Εμιράτα
   - 阿拉伯聯合酋長國
   - Leta Zunze Ubumwe z’Abarabu
 AF:
   - Авганистан
   - Afganistaŋ
   - Afgan
+  - Afghan
   - अफगानिस्तान
   - أفغانستان
   - আফগানিস্তান
   - Afgaanistan
   - ඇෆ්ගනිස්ථානය
   - ອາຟການິສຖານ
   - ⴰⴼⵖⴰⵏⵉⵙⵜⴰⵏ
@@ -4238,14 +4253,16 @@
   - Ijamhuri ya Hidemokrasi ya Hukongo
   - Kòŋgo ìkɛŋi
   - Kongo   - Kinisasa
   - Kongo   - Kinshasa
   - Republiche Democratiche dal Congo
   - Democratic Republic Of Congo
   - DEMOCRATIC REPUBLIC OF THE CONGO (FORMERLY ZAIRE)
+  - RÉPUBLIQUE DÉMOCRATIQUE DU CONGO
+  - Congo, Democratic Republic of
   - Kongo Kinshasa nutome
   - Republica Democratica dal Congo
   - Конго  -Киншаса
   - Kongo DV
   - Demokoratika Ripaaburika ya Kongo
   - Repoblikan’i Kongo
   - कोङ्गो  -किन्शासा
@@ -4491,14 +4508,15 @@
   - Kòŋgo
   - CONGO REP.
   - Конго  -Браззавил
   - ਕਾਂਗੋ   - ਬ੍ਰਾਜ਼ਾਵਿਲੇ
   - Kɔŋgɔ
   - Kongo   - Palasavila
   - Emetab Congo   - Brazzaville
+  - Congo, Republic of
   - Hukongo
   - 剛果   - 布拉薩
   - Kongo
   - Kongo – Brazzaville
   - Kongo  -Brazzaville
   - Конго (Бразавил)
   - Kongu
@@ -5328,14 +5346,15 @@
 CN:
   - ਚੀਨ
   - Sinɛ
   - චීනය
   - Siaina
   - Cine
   - Chnese
+  - China/Chine
   - Caina, Sin
   - Cina
   - Chinese
   - Chíina
   - Hytaý
   - Cayina
   - PRC
@@ -5440,14 +5459,15 @@
   - i  -China
   - Кина
   - Cháína
   - Kyaina
   - Қытай
   - Tsáina
   - An tSín
+  - Macao SAR, China
 CO:
   - ਕੋਲੰਬੀਆ
   - Kɔlɔ́mbía
   - ኮሎምቢያ
   - i  -Colombia
   - Colombian
   - Columbian
@@ -7260,14 +7280,15 @@
   - Egjipt
   - Egiptas
   - Мисар
   - ઇજિપ્ત
   - Misr
   - อียิปต์
   - Arab Republic of Egypt
+  - Egypt, Arab Republic of
   - ཨི་ཇིབཊ
   - Mísiri
   - Äjüpte
   - ꕆꔖꕞ
   - Egipteb
   - Мысыр
   - Misli
@@ -7619,14 +7640,15 @@
   - Sepanyol
   - canary islands
 ET:
   - Etiopía
   - എത്യോപ്യ
   - 衣索比亞
   - Ethiopia
+  - Ethiopian
   - Ethiopie
   - Emetab Ethiopia
   - Αιθιοπία
   - Etiopi
   - Äthiopien
   - 에티오피아
   - Federal Democratic Republic of Ethiopia
@@ -8548,14 +8570,15 @@
   - England & Wales
   - England/United Kingdom
   - British English
   - Ukengland
   - United Kindgom
   - United Kindgdom
   - The United Kingdom
+  - United Kingdom of Great Britain
   - Welsh
   - Cardiff
   - Britsh
   - Great British
   - Great Britain
   - Scottish
   - United Kingdon
@@ -9647,14 +9670,15 @@
   - Guinée
   - Emetab Guinea
   - ᎫᏇ
   - گینێ
   - Gínea
   - Guineab
   - Guinea
+  - Guinean
   - An Ghuine
   - Gineea
   - گینه
   - Guinee
   - ጊኒ
   - ഗിനിയ
   - Ginɛ
@@ -11211,14 +11235,15 @@
   - ۋېنگىرىيە
   - ହଙ୍ଗେରୀ
   - හන්ගේරියාව
 ID:
   - インドネシア
   - Indonethia
   - Indonesian
+  - Indonesia
   - ಇಂಡೋನೇಶಿಯಾ
   - Undonesia
   - Indonezi
   - Ênndonezïi
   - İndoneziya
   - Orílɛ́ède Indonesia
   - Индонезија
@@ -11321,14 +11346,16 @@
   - IRELEND
   - Irish
   - THE REPUBLI C OF IRELAND
   - THE REPUBLIC OF IRELAND
   - REPUBLIC OF IRELAND
   - IRISH REPUBLIC
   - Rep Of Ireland
+  - Éire-Ireland
+  - Éire-Irlande
   - REPULBIC OF IRELAND
   - IRELANND
   - Ayalan
   - Ayalandi
   - අයර්ලන්තය
   - İrlandiya
   - ꕉꔓ ꖨꕮꕊ
@@ -11650,14 +11677,15 @@
   - Острво Ман
   - მენის კუნძული
   - IMN
   - Oileán Mhanann
   - 맨 섬
   - Мэн аралы
   - Île de Man
+  - Man, Isle of
   - Wyspa Man
   - i  -Isle of Man
   - Illa de Man
   - Pulau Man
   - Mann
   - Ellan Vannin
   - Mannin
@@ -12964,14 +12992,15 @@
   - ਕਿਰਗਿਜ਼ਸਤਾਨ
   - ⴽⵉⵔⵖⵉⵣⵉⵙⵜⴰⵏ
   - KGZ
   - Kirigizitùaan
   - Kirigizisitaŋ
   - Kirgizië
   - Kirgizistan
+  - Kyrgyz SSR (now Kyrgyzstan)
 KH:
   - ਕੰਬੋਡੀਆ
   - Kambodj
   - Kambodza
   - Kamboodiya
   - ꕪꕹꔵꕩ
   - Cambodia
@@ -14077,14 +14106,15 @@
   - Kazachistani
   - Kazahsztán
   - କାଜାକାସ୍ଥାନ୍
   - ਕਜ਼ਾਖਸਤਾਨ
   - Kazasitaŋ
   - kazaxstan
   - ካዛኪስታን
+  - Kazakh SSR
 LA:
   - Laóosi
   - لائوس
   - Laosz
   - ლაოსი
   - လာအို
   - Լաոս
@@ -15385,14 +15415,16 @@
   - મોલડોવા
   - Moldávia
   - Moldawii
   - Molədaví
   - Moldavië
   - Moldau
   - مولداوی
+  - Moldovian SSR (now Republic of Moldovia)
+  - Moldovian SSR
 ME:
   - Чорногорія
   - ಮೊಂಟೆನೆಗ್ರೋ
   - מאנטענעגרא
   - Монтенегро
   - Mōntenegran
   - Montainéagró
@@ -15757,14 +15789,15 @@
   - Marshalleilande
   - Republic of the Marshall Islands
   - Aolepān Aorōkin Ṃajeḷ
   - Majuro
 MK:
   - North Macedonia
   - The Former Yugoslav Republic of Macedonia
+  - Macedonia, The Former Yugoslav Republic of
   - REPUBLIC OF MACEDONIA (F.Y.R.O.M.)
   - Macedonian
   - F.Y.R.O.M.
   - FYROM
   - ແມຊິໂດເນຍ
   - መቄዶንያ
   - మేసిడోనియా
@@ -15945,24 +15978,26 @@
   - म्यानमार
   - Mjanmar (Búrma)
   - Мʼянма (Бірма)
   - ਮਿਆਂਮਾਰ (ਬਰਮਾ)
   - म्यानमार (बर्मा)
   - Pema
   - Birma
+  - Burmese
   - മ്യാൻമാർ (ബർമ്മ)
   - Miáama
   - Birimaniya
   - ମିୟାମାର୍
   - מיאנמאר (בורמה)‎
   - Mjanmarsko
   - Myama
   - Myanmar (Burma) nutome
   - MYANMAR (FORMERLY BURMA)
   - MYANMAR (MYANMA NAINGNGANDAW )
+  - BIRMANIE/MYANMAR
   - Miyamaha
   - Humyama
   - Myanma
   - Mianmar (Birma)
   - Myanamar
   - myanmár
   - Mjanmar
@@ -16490,14 +16525,15 @@
   - Martiník
   - ມາຕິນີກ
   - مارتىنىكا
   - Մարտինիկա
 MR:
   - Mauritani
   - Mauritian
+  - Mauritanian
   - ماۋرىتانىيە
   - മൗറിറ്റാനിയ
   - ሞሪቴኒያ
   - i  -Mauritania
   - Mauretanie
   - ⵎⵓⵕⵉⵟⴰⵏⵢⴰ
   - מאוריטניה
@@ -17901,14 +17937,15 @@
   - نيجيريا
   - Niijéria
   - نایجیریا
   - An Nigéir
 NI:
   - نىكاراگۇئا
   - Nicearagua
+  - Nicaraguan
   - ניקרגואה
   - Никарагуа
   - níkarágwa
   - نيكاراغوا
   - Nìkàragwà
   - Nikalakua
   - Nicaraagua
@@ -19752,14 +19789,15 @@
   - Kpǒto Leko
 PS:
   - State of Palestine
   - Territorios palestinos
   - పాలస్తీనియన్ ప్రాంతాలు
   - Palesztin Terület
   - Palestina
+  - Palestinian
   - Palestinian territory
   - West Bank
   - PALESTINE
   - OCCUPIED PALESTINIAN TERRITORY
   - zǝ palɛstínǝ
   - فَلَستیٖن
   - Territori Palestinais
@@ -20533,14 +20571,15 @@
   - Rusya
   - Risí
   - روس
   - ꊉꇆꌦ
   - Uburusiya
   - 俄羅斯
   - Russian Federation
+  - Russia Federation
   - Российская Федерация
   - rusya
   - Huulusi
   - Русия
   - Lasa
   - Emetab Russia
   - Rosja
@@ -20726,14 +20765,15 @@
   - ਰਵਾਂਡਾ
   - ⵔⵡⴰⵏⴷⴰ
   - रवांडा
 SA:
   - Għarabja Sawdita
   - Saudi  -Arabia
   - Saudi Arabian
+  - Saudi Arab
   - Saudiarabia
   - Ssaεudiyya Taεrabt
   - Arabie Saudide
   - ဆော်ဒီအာရေးဗီးယား
   - साउदी अरब
   - سەئۇدى ئەرەبىستان
   - ਸਾਊਦੀ ਅਰਬ
@@ -24130,14 +24170,15 @@
   - Trinidad və Tobaqo
   - Тринидад и Тобаго
   - 千里達和多巴哥
   - Tiriníida ya Tobáago
   - Trinite  -ni  -Tobago
   - Тринидад ва Тобаго
   - Tinidadɛ mpé Tobago
+  - TRINIDAD ET TOBAGO
   - Trinidad och Tobago
   - त्रिनिदाद आणि टोबॅगो
   - Trinidāds be Tobagō
   - Trinidad d Ṭubagu
   - ტრინიდადი და ტობაგო
   - Тринидад ба Тобаго
   - トリニダード・トバゴ
@@ -24310,14 +24351,15 @@
   - Taiwan nutome
   - તાઇવાન
   - Orílẹ́ède Taiwani
   - Taiwanese
   - TWN
   - i  -Taiwan
   - Taiwan, Province of China
+  - Taiwan, China
   - Тайван
   - Taayiwan
   - Thayiwani
   - ታይዋን
   - ထိုင်ဝမ်
   - තායිවානය
   - Taiwani
@@ -24577,14 +24619,18 @@
   - යුක්රේනය
   - Okraina
   - Ucrania
   - Ukrêni
   - Ukreni
   - Wcráin
   - Україна
+  - Former USSR (currently Ukraine)
+  - Ukrainian SSR (Ukraine)
+  - Ukrainian SSR
+  - Ukraine SSR
 UG:
   - Ùgandà
   - Yùgandà
   - i  -Uganda
   - ഉഗാണ്ട
   - اوگاندا
   - Ugandan
@@ -25472,14 +25518,15 @@
   - Emetab Venezuela
   - Vǝnǝzuela
   - Venezuelan
   - Uvenezuela
   - Venezuelan
   - Vènèzùelà
   - Bolivarian Republic of Venezuela
+  - Venezuela, Republica Bolivariana de
   - Huvenezuela
   - ベネズエラ
   - وینازوٗلا
   - ווענעזועלע
   - વેનેઝુએલા
   - 委內瑞拉
   - Veneezuyeela
@@ -26280,14 +26327,15 @@
   - یەمەن
   - Yémeni
   - Iemen
   - Jämme
   - Yǝmɛn
   - Емен
   - Republic of Yemen
+  - Yemen, Republic of
   - Emetab Yemen
   - Éimin
   - ꔝꘈꘋ
   - Iémen
   - Yemen
   - 也门
   - เยเมน
```

### Comparing `countrynames-1.9.0/countrynames/mappings.py` & `countrynames-1.9.1/countrynames/mappings.py`

 * *Files identical despite different names*

### Comparing `countrynames-1.9.0/countrynames.egg-info/PKG-INFO` & `countrynames-1.9.1/countrynames.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: countrynames
-Version: 1.9.0
+Version: 1.9.1
 Summary: A library to map country names to ISO codes.
 Home-page: http://github.com/occrp/countrynames
 Author: Friedrich Lindenberg
 Author-email: friedrich@pudo.org
 License: MIT
 Description: # countrynames
```

### Comparing `countrynames-1.9.0/setup.py` & `countrynames-1.9.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 path = os.path.abspath(os.path.dirname(__file__))
 
 with open(os.path.join(path, "README.md"), "r") as f:
     readme = f.read()
 
 setup(
     name="countrynames",
-    version="1.9.0",
+    version="1.9.1",
     description="A library to map country names to ISO codes.",
     long_description=readme,
     long_description_content_type="text/markdown",
     classifiers=[
         "Development Status :: 3 - Alpha",
         "Intended Audience :: Developers",
         "License :: OSI Approved :: MIT License",
```

