# Comparing `tmp/mttf-0.9.202209080905-py3-none-any.whl.zip` & `tmp/mttf-0.9.202209080909-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,25 +1,25 @@
-Zip file size: 45769 bytes, number of entries: 23
+Zip file size: 45689 bytes, number of entries: 23
 -rw-r--r--  2.0 unx      338 b- defN 22-Aug-30 02:57 mt/tf/__init__.py
 -rw-r--r--  2.0 unx     2662 b- defN 22-Sep-08 05:24 mt/tf/init.py
--rw-r--r--  2.0 unx      396 b- defN 22-Sep-08 09:05 mt/tf/mttf_version.py
+-rw-r--r--  2.0 unx      396 b- defN 22-Sep-08 09:09 mt/tf/mttf_version.py
 -rw-r--r--  2.0 unx      562 b- defN 22-Aug-30 02:57 mt/tf/utils.py
 -rw-r--r--  2.0 unx        0 b- defN 21-Dec-14 12:16 mt/tf/keras_applications/__init__.py
 -rw-r--r--  2.0 unx    39204 b- defN 22-Mar-08 16:37 mt/tf/keras_applications/efficientnet_v2.py
 -rw-r--r--  2.0 unx    22568 b- defN 21-Dec-14 12:16 mt/tf/keras_applications/mobilenet_v3.py
--rw-r--r--  2.0 unx    18226 b- defN 22-Sep-07 03:06 mt/tf/keras_applications/mobilenet_v3_split.py
+-rw-r--r--  2.0 unx    17950 b- defN 22-Sep-08 09:09 mt/tf/keras_applications/mobilenet_v3_split.py
 -rw-r--r--  2.0 unx     9823 b- defN 22-Sep-07 02:49 mt/tf/keras_applications/mobilevit.py
 -rw-r--r--  2.0 unx        0 b- defN 21-Dec-14 12:16 mt/tf/keras_engine/__init__.py
 -rw-r--r--  2.0 unx    33446 b- defN 21-Dec-14 12:16 mt/tf/keras_engine/hdf5_format.py
 -rw-r--r--  2.0 unx       26 b- defN 22-Sep-08 03:53 mt/tf/keras_layers/__init__.py
 -rw-r--r--  2.0 unx    19996 b- defN 22-Sep-08 09:04 mt/tf/keras_layers/simple_mha.py
 -rw-r--r--  2.0 unx     3804 b- defN 21-Dec-14 12:16 mt/tf/keras_optimizers/lr_extra.py
 -rw-r--r--  2.0 unx     2403 b- defN 22-Sep-07 02:46 mt/tfc/__init__.py
 -rw-r--r--  2.0 unx      304 b- defN 22-Feb-19 07:18 mt/tfg/__init__.py
 -rw-r--r--  2.0 unx      383 b- defN 22-Jul-07 08:16 mt/tfp/__init__.py
 -rw-r--r--  2.0 unx     4440 b- defN 22-Jul-11 05:36 mt/tfp/real_nvp.py
--rw-r--r--  2.0 unx     1070 b- defN 22-Sep-08 09:06 mttf-0.9.202209080905.dist-info/LICENSE
--rw-r--r--  2.0 unx      371 b- defN 22-Sep-08 09:06 mttf-0.9.202209080905.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 22-Sep-08 09:06 mttf-0.9.202209080905.dist-info/WHEEL
--rw-r--r--  2.0 unx        3 b- defN 22-Sep-08 09:06 mttf-0.9.202209080905.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1940 b- defN 22-Sep-08 09:06 mttf-0.9.202209080905.dist-info/RECORD
-23 files, 162057 bytes uncompressed, 42605 bytes compressed:  73.7%
+-rw-r--r--  2.0 unx     1070 b- defN 22-Sep-08 09:44 mttf-0.9.202209080909.dist-info/LICENSE
+-rw-r--r--  2.0 unx      371 b- defN 22-Sep-08 09:44 mttf-0.9.202209080909.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 22-Sep-08 09:44 mttf-0.9.202209080909.dist-info/WHEEL
+-rw-r--r--  2.0 unx        3 b- defN 22-Sep-08 09:44 mttf-0.9.202209080909.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1940 b- defN 22-Sep-08 09:44 mttf-0.9.202209080909.dist-info/RECORD
+23 files, 161781 bytes uncompressed, 42525 bytes compressed:  73.7%
```

## zipnote {}

```diff
@@ -48,23 +48,23 @@
 
 Filename: mt/tfp/__init__.py
 Comment: 
 
 Filename: mt/tfp/real_nvp.py
 Comment: 
 
-Filename: mttf-0.9.202209080905.dist-info/LICENSE
+Filename: mttf-0.9.202209080909.dist-info/LICENSE
 Comment: 
 
-Filename: mttf-0.9.202209080905.dist-info/METADATA
+Filename: mttf-0.9.202209080909.dist-info/METADATA
 Comment: 
 
-Filename: mttf-0.9.202209080905.dist-info/WHEEL
+Filename: mttf-0.9.202209080909.dist-info/WHEEL
 Comment: 
 
-Filename: mttf-0.9.202209080905.dist-info/top_level.txt
+Filename: mttf-0.9.202209080909.dist-info/top_level.txt
 Comment: 
 
-Filename: mttf-0.9.202209080905.dist-info/RECORD
+Filename: mttf-0.9.202209080909.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## mt/tf/mttf_version.py

```diff
@@ -1,11 +1,11 @@
 VERSION_YEAR = 2022
 VERSION_MONTH = int('09')
 VERSION_DAY = int('08')
 VERSION_HOUR = int('09')
-VERSION_MINUTE = int('05')
+VERSION_MINUTE = int('09')
 MAJOR_VERSION = 0
 MINOR_VERSION = 9
-PATCH_VERSION = 202209080905
-version_date = '2022/09/08 09:05'
+PATCH_VERSION = 202209080909
+version_date = '2022/09/08 09:09'
 version = '{}.{}.{}'.format(MAJOR_VERSION, MINOR_VERSION, PATCH_VERSION)
 __all__  = ['MAJOR_VERSION', 'MINOR_VERSION', 'PATCH_VERSION', 'version_date', 'version']
```

## mt/tf/keras_applications/mobilenet_v3_split.py

```diff
@@ -279,38 +279,32 @@
         x = layers.GlobalMaxPool2D(x)
     elif mixer_type == "mha":
         if backend.image_data_format() == "channels_first":
             raise tfc.ModelSyntaxError(
                 "Mixer type MHA requires channels_last image data format."
             )
 
+        from ..keras_layers import SimpleMHA
+
         n_heads = mha_params.n_heads
         input_dim = x.shape[-1]
         if mha_params.key_dim is None:
             if input_dim % n_heads != 0:
                 raise tfc.ModelSyntaxError(
                     "The last dimension ({}) is not divisible by {}.".format(
                         input_dim, n_heads
                     )
                 )
             key_dim = input_dim // n_heads
         else:
             key_dim = mha_params.key_dim
-        fake_input = tf.eye(1, num_columns=input_dim)[
-            tf.newaxis, tf.newaxis, ...
-        ]  # (B=1, H=1, W=1, D=input_dim)
-        fake_input = tf.repeat(fake_input, tf.shape(x)[0:1], axis=0)
-        layer = kl.MultiHeadAttention(
-            n_heads,
-            key_dim,
-            value_dim=mha_params.value_dim,
-            output_shape=mha_params.output_shape,
-            attention_axes=(1, 2),
+        layer = SimpleMHA(
+            num_heads=n_heads, key_dim=key_dim, value_dim=mha_params.value_dim
         )
-        x = layer(fake_input, x)
+        x = layer(x)
     else:
         raise tfc.ModelSyntaxError("Unknown mixer type: '{}'.".format(mixer_type))
 
     # Create model.
     model = models.Model(input_tensor, x, name="MobilenetV3{}Mixer".format(model_type))
 
     return model
```

## Comparing `mttf-0.9.202209080905.dist-info/LICENSE` & `mttf-0.9.202209080909.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `mttf-0.9.202209080905.dist-info/RECORD` & `mttf-0.9.202209080909.dist-info/RECORD`

 * *Files 12% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 mt/tf/__init__.py,sha256=M8xiJNdrAUJZgiZTOQOdfkehjO-CYzGpoxh5HVGBkms,338
 mt/tf/init.py,sha256=0bqpe-23-2P2YTsor3oYIa1ZAJ2ZYvjVGCOmkmvdYvo,2662
-mt/tf/mttf_version.py,sha256=ZVQl_8gq3bhzNFN_B_X5mQwWY0QMyXKpAbhW-ooKT88,396
+mt/tf/mttf_version.py,sha256=pSS22J-3YP7KV7D5OVg-AdqfpsRa2YekWYsv6JeDmRg,396
 mt/tf/utils.py,sha256=R_YG31mn6bU5XjiLJCzadR0tbymy4YM8te2Q_DtURiQ,562
 mt/tf/keras_applications/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 mt/tf/keras_applications/efficientnet_v2.py,sha256=DYXP567HNUp2SO0_pXUfzO9-WqlTiGmXApAawkKaetc,39204
 mt/tf/keras_applications/mobilenet_v3.py,sha256=wwAKizlhWm2YNzIk0DyH2UwYDE6Xk0DUuEU8KWNr08M,22568
-mt/tf/keras_applications/mobilenet_v3_split.py,sha256=YNROjCi-MtqSyV8PKq0kXtdrrK99KsVdSEuFWdvfQe4,18226
+mt/tf/keras_applications/mobilenet_v3_split.py,sha256=-ODfQ-kjz9CkCcDhTa2QGBPoYT5_ZsLJOMzDNPkRVcg,17950
 mt/tf/keras_applications/mobilevit.py,sha256=o9Rfzf1CKU0R3rZoaS7y_MCuppthJu7P6bP4QPsVjQw,9823
 mt/tf/keras_engine/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
 mt/tf/keras_engine/hdf5_format.py,sha256=f3DK63dAzif2szAPbHVtcohiUB3tC_JVgd3lu4cUhPQ,33446
 mt/tf/keras_layers/__init__.py,sha256=Y4u3qUt9UZMB01SkGYZP1RHAhrbLcTGs0i4Ct04nJLk,26
 mt/tf/keras_layers/simple_mha.py,sha256=cGJLGZtVKgv7Gpntb46OU6qdRBRAm53Gisx6md0mdYo,19996
 mt/tf/keras_optimizers/lr_extra.py,sha256=We0k3Uj2kBb18_V1Cw0wuAofLZoSuSekdpCBCQ6WoEM,3804
 mt/tfc/__init__.py,sha256=HOiYPW-NrIBKSonR0HStN6_27lTShBmtUu23xUw3zcY,2403
 mt/tfg/__init__.py,sha256=6Ly2QImAyQTsg_ZszuAuK_L2n56v89Cix9yYmMVk0CM,304
 mt/tfp/__init__.py,sha256=AQkGCkmDRwswEt3qoOSpxe-fZekx78sHHBs2ZVz33gc,383
 mt/tfp/real_nvp.py,sha256=U9EmkXGqFcvtS2yeh5_RgbKlVKKlGFGklAb7Voyazz4,4440
-mttf-0.9.202209080905.dist-info/LICENSE,sha256=e_JtcszdGZ2ZGfjcymTGrcxFj_9XPicZOVtnsrPvruk,1070
-mttf-0.9.202209080905.dist-info/METADATA,sha256=Nnxp3-ab68npYc7HNQDsXsyNBZ5DUF95R5Oy2gRSA5M,371
-mttf-0.9.202209080905.dist-info/WHEEL,sha256=G16H4A3IeoQmnOrYV4ueZGKSjhipXx8zc8nu9FGlvMA,92
-mttf-0.9.202209080905.dist-info/top_level.txt,sha256=WcqGFu9cV7iMZg09iam8eNxUvGpLSKKF2Iubf6SJVOo,3
-mttf-0.9.202209080905.dist-info/RECORD,,
+mttf-0.9.202209080909.dist-info/LICENSE,sha256=e_JtcszdGZ2ZGfjcymTGrcxFj_9XPicZOVtnsrPvruk,1070
+mttf-0.9.202209080909.dist-info/METADATA,sha256=d3dsNyW86W01WWVo8dnpku0nyRl13twWaL87qSh2a7U,371
+mttf-0.9.202209080909.dist-info/WHEEL,sha256=G16H4A3IeoQmnOrYV4ueZGKSjhipXx8zc8nu9FGlvMA,92
+mttf-0.9.202209080909.dist-info/top_level.txt,sha256=WcqGFu9cV7iMZg09iam8eNxUvGpLSKKF2Iubf6SJVOo,3
+mttf-0.9.202209080909.dist-info/RECORD,,
```

