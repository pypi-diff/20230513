# Comparing `tmp/omemo-dr-0.99.1.tar.gz` & `tmp/omemo-dr-0.99.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "omemo-dr-0.99.1.tar", last modified: Wed May  3 19:56:31 2023, max compression
+gzip compressed data, was "omemo-dr-0.99.2.tar", last modified: Sat May 13 17:04:49 2023, max compression
```

## Comparing `omemo-dr-0.99.1.tar` & `omemo-dr-0.99.2.tar`

### file list

```diff
@@ -1,210 +1,206 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/
--rw-rw-rw-   0 root         (0) root         (0)    35122 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/LICENSE
--rw-rw-rw-   0 root         (0) root         (0)       62 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)    43228 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)     2160 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.171828 omemo-dr-0.99.1/curve25519/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.171828 omemo-dr-0.99.1/curve25519/curve/
--rw-rw-rw-   0 root         (0) root         (0)    31932 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/curve25519-donna.c
--rw-rw-rw-   0 root         (0) root         (0)      137 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/curve25519-donna.h
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.179829 omemo-dr-0.99.1/curve25519/curve/ed25519/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.183829 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/
--rw-rw-rw-   0 root         (0) root         (0)      663 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/compare.c
--rw-rw-rw-   0 root         (0) root         (0)      129 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/compare.h
--rw-rw-rw-   0 root         (0) root         (0)      536 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/convert.c
--rw-rw-rw-   0 root         (0) root         (0)     1624 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/crypto_additions.h
--rw-rw-rw-   0 root         (0) root         (0)      156 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/crypto_hash_sha512.h
--rw-rw-rw-   0 root         (0) root         (0)     3046 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/curve_sigs.c
--rw-rw-rw-   0 root         (0) root         (0)      662 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/curve_sigs.h
--rw-rw-rw-   0 root         (0) root         (0)     1139 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ed_sigs.c
--rw-rw-rw-   0 root         (0) root         (0)      321 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ed_sigs.h
--rw-rw-rw-   0 root         (0) root         (0)     2236 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/elligator.c
--rw-rw-rw-   0 root         (0) root         (0)      333 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_edy_to_montx.c
--rw-rw-rw-   0 root         (0) root         (0)      205 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_isequal.c
--rw-rw-rw-   0 root         (0) root         (0)      242 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_isreduced.c
--rw-rw-rw-   0 root         (0) root         (0)      425 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_mont_rhs.c
--rw-rw-rw-   0 root         (0) root         (0)      319 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_montx_to_edy.c
--rw-rw-rw-   0 root         (0) root         (0)     1355 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_sqrt.c
--rw-rw-rw-   0 root         (0) root         (0)      279 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_isneutral.c
--rw-rw-rw-   0 root         (0) root         (0)     1966 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_montx_to_p3.c
--rw-rw-rw-   0 root         (0) root         (0)      201 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_neg.c
--rw-rw-rw-   0 root         (0) root         (0)      440 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_p3_to_montx.c
--rw-rw-rw-   0 root         (0) root         (0)     3141 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_scalarmult.c
--rw-rw-rw-   0 root         (0) root         (0)      314 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_scalarmult_cofactor.c
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.187829 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/
--rw-rw-rw-   0 root         (0) root         (0)      384 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_constants.h
--rw-rw-rw-   0 root         (0) root         (0)      284 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_crypto_additions.h
--rw-rw-rw-   0 root         (0) root         (0)     2660 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_eddsa.h
--rw-rw-rw-   0 root         (0) root         (0)     1034 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_labelset.h
--rw-rw-rw-   0 root         (0) root         (0)      948 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_veddsa.h
--rw-rw-rw-   0 root         (0) root         (0)     1821 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_x.h
--rw-rw-rw-   0 root         (0) root         (0)      621 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/keygen.c
--rw-rw-rw-   0 root         (0) root         (0)      389 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/keygen.h
--rw-rw-rw-   0 root         (0) root         (0)      951 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/open_modified.c
--rw-rw-rw-   0 root         (0) root         (0)      113 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sc_clamp.c
--rw-rw-rw-   0 root         (0) root         (0)      465 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sc_cmov.c
--rw-rw-rw-   0 root         (0) root         (0)      996 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sc_neg.c
--rw-rw-rw-   0 root         (0) root         (0)     1326 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sign_modified.c
--rw-rw-rw-   0 root         (0) root         (0)      594 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/utility.c
--rw-rw-rw-   0 root         (0) root         (0)      252 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/utility.h
--rw-rw-rw-   0 root         (0) root         (0)     2367 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/xeddsa.c
--rw-rw-rw-   0 root         (0) root         (0)      636 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/xeddsa.h
--rw-rw-rw-   0 root         (0) root         (0)      280 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/zeroize.c
--rw-rw-rw-   0 root         (0) root         (0)      174 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/additions/zeroize.h
--rw-rw-rw-   0 root         (0) root         (0)      121 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/api.h
--rw-rw-rw-   0 root         (0) root         (0)    76457 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/base.h
--rw-rw-rw-   0 root         (0) root         (0)     2388 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/base2.h
--rw-rw-rw-   0 root         (0) root         (0)       91 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/d.h
--rw-rw-rw-   0 root         (0) root         (0)       90 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/d2.h
--rw-rw-rw-   0 root         (0) root         (0)     1939 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe.h
--rw-rw-rw-   0 root         (0) root         (0)      170 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_0.c
--rw-rw-rw-   0 root         (0) root         (0)      170 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_1.c
--rw-rw-rw-   0 root         (0) root         (0)     1255 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_add.c
--rw-rw-rw-   0 root         (0) root         (0)     1283 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_cmov.c
--rw-rw-rw-   0 root         (0) root         (0)      454 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_copy.c
--rw-rw-rw-   0 root         (0) root         (0)     2222 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_frombytes.c
--rw-rw-rw-   0 root         (0) root         (0)      135 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_invert.c
--rw-rw-rw-   0 root         (0) root         (0)      266 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_isnegative.c
--rw-rw-rw-   0 root         (0) root         (0)      453 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_isnonzero.c
--rw-rw-rw-   0 root         (0) root         (0)    10744 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_mul.c
--rw-rw-rw-   0 root         (0) root         (0)      855 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_neg.c
--rw-rw-rw-   0 root         (0) root         (0)      127 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_pow22523.c
--rw-rw-rw-   0 root         (0) root         (0)     5980 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sq.c
--rw-rw-rw-   0 root         (0) root         (0)     6106 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sq2.c
--rw-rw-rw-   0 root         (0) root         (0)     1255 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sub.c
--rw-rw-rw-   0 root         (0) root         (0)     3189 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/fe_tobytes.c
--rw-rw-rw-   0 root         (0) root         (0)     2869 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge.h
--rw-rw-rw-   0 root         (0) root         (0)      125 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_add.c
--rw-rw-rw-   0 root         (0) root         (0)     2080 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_add.h
--rw-rw-rw-   0 root         (0) root         (0)     2371 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_double_scalarmult.c
--rw-rw-rw-   0 root         (0) root         (0)      987 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_frombytes.c
--rw-rw-rw-   0 root         (0) root         (0)      128 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_madd.c
--rw-rw-rw-   0 root         (0) root         (0)     1900 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_madd.h
--rw-rw-rw-   0 root         (0) root         (0)      128 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_msub.c
--rw-rw-rw-   0 root         (0) root         (0)     1900 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_msub.h
--rw-rw-rw-   0 root         (0) root         (0)      165 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p1p1_to_p2.c
--rw-rw-rw-   0 root         (0) root         (0)      191 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p1p1_to_p3.c
--rw-rw-rw-   0 root         (0) root         (0)       86 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p2_0.c
--rw-rw-rw-   0 root         (0) root         (0)      112 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p2_dbl.c
--rw-rw-rw-   0 root         (0) root         (0)     1476 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p2_dbl.h
--rw-rw-rw-   0 root         (0) root         (0)      100 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p3_0.c
--rw-rw-rw-   0 root         (0) root         (0)      131 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p3_dbl.c
--rw-rw-rw-   0 root         (0) root         (0)      246 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p3_to_cached.c
--rw-rw-rw-   0 root         (0) root         (0)      149 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p3_to_p2.c
--rw-rw-rw-   0 root         (0) root         (0)      228 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p3_tobytes.c
--rw-rw-rw-   0 root         (0) root         (0)      110 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_precomp_0.c
--rw-rw-rw-   0 root         (0) root         (0)     2477 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_scalarmult_base.c
--rw-rw-rw-   0 root         (0) root         (0)      125 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_sub.c
--rw-rw-rw-   0 root         (0) root         (0)     2080 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_sub.h
--rw-rw-rw-   0 root         (0) root         (0)      225 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/ge_tobytes.c
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.187829 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/
--rw-rw-rw-   0 root         (0) root         (0)       81 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_int32.h
--rw-rw-rw-   0 root         (0) root         (0)       87 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_int64.h
--rw-rw-rw-   0 root         (0) root         (0)      751 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_sign.h
--rw-rw-rw-   0 root         (0) root         (0)     2034 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_sign_edwards25519sha512batch.h
--rw-rw-rw-   0 root         (0) root         (0)       93 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_uint32.h
--rw-rw-rw-   0 root         (0) root         (0)       99 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_uint64.h
--rw-rw-rw-   0 root         (0) root         (0)      579 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_verify_32.h
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.187829 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_sha512/
--rw-rw-rw-   0 root         (0) root         (0)     6416 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_sha512/blocks.c
--rw-rw-rw-   0 root         (0) root         (0)     1807 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_sha512/hash.c
--rw-rw-rw-   0 root         (0) root         (0)     1036 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/open.c
--rw-rw-rw-   0 root         (0) root         (0)     5518 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/pow22523.h
--rw-rw-rw-   0 root         (0) root         (0)     5527 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/pow225521.h
--rw-rw-rw-   0 root         (0) root         (0)      382 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/sc.h
--rw-rw-rw-   0 root         (0) root         (0)    12494 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/sc_muladd.c
--rw-rw-rw-   0 root         (0) root         (0)     8139 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/sc_reduce.c
--rw-rw-rw-   0 root         (0) root         (0)      817 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/sign.c
--rw-rw-rw-   0 root         (0) root         (0)       87 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/sqrtm1.h
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.187829 omemo-dr-0.99.1/curve25519/curve/ed25519/tests/
--rw-rw-rw-   0 root         (0) root         (0)      563 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/tests/internal_fast_tests.h
--rw-rw-rw-   0 root         (0) root         (0)      540 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/curve25519/curve/ed25519/tests/internal_slow_tests.h
--rw-rw-rw-   0 root         (0) root         (0)     8040 2023-04-09 19:22:07.000000 omemo-dr-0.99.1/curve25519/curve25519module.c
--rw-rw-rw-   0 root         (0) root         (0)     4778 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)      685 2023-03-26 20:37:13.000000 omemo-dr-0.99.1/setup.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.167827 omemo-dr-0.99.1/src/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.187829 omemo-dr-0.99.1/src/omemo_dr/
--rw-rw-rw-   0 root         (0) root         (0)       23 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     2254 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/aes.py
--rw-rw-rw-   0 root         (0) root         (0)      121 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/const.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.191830 omemo-dr-0.99.1/src/omemo_dr/curve/
--rw-rw-rw-   0 root         (0) root         (0)     1216 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/curve/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.191830 omemo-dr-0.99.1/src/omemo_dr/ecc/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/ecc/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     2613 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ecc/curve.py
--rw-rw-rw-   0 root         (0) root         (0)     2259 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ecc/djbec.py
--rw-rw-rw-   0 root         (0) root         (0)      352 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ecc/ec.py
--rw-rw-rw-   0 root         (0) root         (0)      445 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ecc/eckeypair.py
--rw-rw-rw-   0 root         (0) root         (0)     1252 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/exceptions.py
--rw-rw-rw-   0 root         (0) root         (0)     1480 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/identitykey.py
--rw-rw-rw-   0 root         (0) root         (0)     1487 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/identitykeypair.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.191830 omemo-dr-0.99.1/src/omemo_dr/kdf/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/kdf/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      620 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/kdf/derivedmessagesecrets.py
--rw-rw-rw-   0 root         (0) root         (0)      372 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/kdf/derivedrootsecrets.py
--rw-rw-rw-   0 root         (0) root         (0)     1912 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/kdf/hkdf.py
--rw-rw-rw-   0 root         (0) root         (0)      507 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/kdf/messagekeys.py
--rw-rw-rw-   0 root         (0) root         (0)      836 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/observable.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.191830 omemo-dr-0.99.1/src/omemo_dr/protocol/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      498 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/ciphertextmessage.py
--rw-rw-rw-   0 root         (0) root         (0)     4099 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/omemo_keyexchange.py
--rw-rw-rw-   0 root         (0) root         (0)     5043 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/omemo_message.py
--rw-rw-rw-   0 root         (0) root         (0)     8074 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/omemo_pb2.py
--rw-rw-rw-   0 root         (0) root         (0)     5085 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/prekeywhispermessage.py
--rw-rw-rw-   0 root         (0) root         (0)     4939 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/whispermessage.py
--rw-rw-rw-   0 root         (0) root         (0)    15498 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/protocol/whisperprotos_pb2.py
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/py.typed
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.195830 omemo-dr-0.99.1/src/omemo_dr/ratchet/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1388 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/aliceparameters.py
--rw-rw-rw-   0 root         (0) root         (0)     1358 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/bobparameters.py
--rw-rw-rw-   0 root         (0) root         (0)     1654 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/chainkey.py
--rw-rw-rw-   0 root         (0) root         (0)     5537 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/ratchetingsession.py
--rw-rw-rw-   0 root         (0) root         (0)     1398 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/ratchet/rootkey.py
--rw-rw-rw-   0 root         (0) root         (0)    17917 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/session.py
--rw-rw-rw-   0 root         (0) root         (0)     5575 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/sessionbuilder.py
--rw-rw-rw-   0 root         (0) root         (0)    11003 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/sessioncipher.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.195830 omemo-dr-0.99.1/src/omemo_dr/state/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/state/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1946 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/prekeybundle.py
--rw-rw-rw-   0 root         (0) root         (0)     1484 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/prekeyrecord.py
--rw-rw-rw-   0 root         (0) root         (0)     2925 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/sessionrecord.py
--rw-rw-rw-   0 root         (0) root         (0)    15547 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/sessionstate.py
--rw-rw-rw-   0 root         (0) root         (0)     1834 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/signedprekeyrecord.py
--rw-rw-rw-   0 root         (0) root         (0)    43661 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/state/storageprotos_pb2.py
--rw-rw-rw-   0 root         (0) root         (0)     4452 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/state/store.py
--rw-rw-rw-   0 root         (0) root         (0)      675 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/structs.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.195830 omemo-dr-0.99.1/src/omemo_dr/util/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/util/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1330 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/util/byteutil.py
--rw-rw-rw-   0 root         (0) root         (0)     2892 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/src/omemo_dr/util/keyhelper.py
--rw-rw-rw-   0 root         (0) root         (0)       39 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/src/omemo_dr/util/medium.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.191830 omemo-dr-0.99.1/src/omemo_dr.egg-info/
--rw-r--r--   0 root         (0) root         (0)    43228 2023-05-03 19:56:31.000000 omemo-dr-0.99.1/src/omemo_dr.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     6972 2023-05-03 19:56:31.000000 omemo-dr-0.99.1/src/omemo_dr.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-05-03 19:56:31.000000 omemo-dr-0.99.1/src/omemo_dr.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       87 2023-05-03 19:56:31.000000 omemo-dr-0.99.1/src/omemo_dr.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        9 2023-05-03 19:56:31.000000 omemo-dr-0.99.1/src/omemo_dr.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/tests/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/tests/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1207 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/inmemoryidentitykeystore.py
--rw-rw-rw-   0 root         (0) root         (0)      853 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/inmemoryprekeystore.py
--rw-rw-rw-   0 root         (0) root         (0)     1110 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/inmemorysessionstore.py
--rw-rw-rw-   0 root         (0) root         (0)     1272 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/inmemorysignedprekeystore.py
--rw-rw-rw-   0 root         (0) root         (0)     3528 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/inmemorystore.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/tests/kdf/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/tests/kdf/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    12318 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/kdf/test_hkdf.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/tests/ratchet/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/tests/ratchet/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3935 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/ratchet/test_chainkey.py
--rw-rw-rw-   0 root         (0) root         (0)     7780 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/ratchet/test_ratchetingsession.py
--rw-rw-rw-   0 root         (0) root         (0)     5833 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/ratchet/test_rootkey.py
--rw-rw-rw-   0 root         (0) root         (0)    10477 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/test_sessionbuilder.py
--rw-rw-rw-   0 root         (0) root         (0)     4371 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/test_sessioncipher.py
--rw-rw-rw-   0 root         (0) root         (0)     9370 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/test_sigs.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-03 19:56:31.199830 omemo-dr-0.99.1/tests/util/
--rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.1/tests/util/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      497 2023-05-03 19:53:25.000000 omemo-dr-0.99.1/tests/util/test_byteutil.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.074070 omemo-dr-0.99.2/
+-rw-rw-rw-   0 root         (0) root         (0)    35122 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/LICENSE
+-rw-rw-rw-   0 root         (0) root         (0)       62 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)    43030 2023-05-13 17:04:49.074070 omemo-dr-0.99.2/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     1962 2023-05-11 21:04:20.000000 omemo-dr-0.99.2/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.046067 omemo-dr-0.99.2/curve25519/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.046067 omemo-dr-0.99.2/curve25519/curve/
+-rw-rw-rw-   0 root         (0) root         (0)    31932 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/curve25519-donna.c
+-rw-rw-rw-   0 root         (0) root         (0)      137 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/curve25519-donna.h
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.054068 omemo-dr-0.99.2/curve25519/curve/ed25519/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.058068 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/
+-rw-rw-rw-   0 root         (0) root         (0)      663 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/compare.c
+-rw-rw-rw-   0 root         (0) root         (0)      129 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/compare.h
+-rw-rw-rw-   0 root         (0) root         (0)      536 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/convert.c
+-rw-rw-rw-   0 root         (0) root         (0)     1624 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/crypto_additions.h
+-rw-rw-rw-   0 root         (0) root         (0)      156 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/crypto_hash_sha512.h
+-rw-rw-rw-   0 root         (0) root         (0)     3046 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/curve_sigs.c
+-rw-rw-rw-   0 root         (0) root         (0)      662 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/curve_sigs.h
+-rw-rw-rw-   0 root         (0) root         (0)     1139 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ed_sigs.c
+-rw-rw-rw-   0 root         (0) root         (0)      321 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ed_sigs.h
+-rw-rw-rw-   0 root         (0) root         (0)     2236 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/elligator.c
+-rw-rw-rw-   0 root         (0) root         (0)      333 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_edy_to_montx.c
+-rw-rw-rw-   0 root         (0) root         (0)      205 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_isequal.c
+-rw-rw-rw-   0 root         (0) root         (0)      242 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_isreduced.c
+-rw-rw-rw-   0 root         (0) root         (0)      425 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_mont_rhs.c
+-rw-rw-rw-   0 root         (0) root         (0)      319 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_montx_to_edy.c
+-rw-rw-rw-   0 root         (0) root         (0)     1355 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_sqrt.c
+-rw-rw-rw-   0 root         (0) root         (0)      279 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_isneutral.c
+-rw-rw-rw-   0 root         (0) root         (0)     1966 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_montx_to_p3.c
+-rw-rw-rw-   0 root         (0) root         (0)      201 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_neg.c
+-rw-rw-rw-   0 root         (0) root         (0)      440 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_p3_to_montx.c
+-rw-rw-rw-   0 root         (0) root         (0)     3141 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_scalarmult.c
+-rw-rw-rw-   0 root         (0) root         (0)      314 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_scalarmult_cofactor.c
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.062069 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/
+-rw-rw-rw-   0 root         (0) root         (0)      384 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_constants.h
+-rw-rw-rw-   0 root         (0) root         (0)      284 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_crypto_additions.h
+-rw-rw-rw-   0 root         (0) root         (0)     2660 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_eddsa.h
+-rw-rw-rw-   0 root         (0) root         (0)     1034 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_labelset.h
+-rw-rw-rw-   0 root         (0) root         (0)      948 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_veddsa.h
+-rw-rw-rw-   0 root         (0) root         (0)     1821 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_x.h
+-rw-rw-rw-   0 root         (0) root         (0)      621 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/keygen.c
+-rw-rw-rw-   0 root         (0) root         (0)      389 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/keygen.h
+-rw-rw-rw-   0 root         (0) root         (0)      951 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/open_modified.c
+-rw-rw-rw-   0 root         (0) root         (0)      113 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sc_clamp.c
+-rw-rw-rw-   0 root         (0) root         (0)      465 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sc_cmov.c
+-rw-rw-rw-   0 root         (0) root         (0)      996 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sc_neg.c
+-rw-rw-rw-   0 root         (0) root         (0)     1326 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sign_modified.c
+-rw-rw-rw-   0 root         (0) root         (0)      594 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/utility.c
+-rw-rw-rw-   0 root         (0) root         (0)      252 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/utility.h
+-rw-rw-rw-   0 root         (0) root         (0)     2367 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/xeddsa.c
+-rw-rw-rw-   0 root         (0) root         (0)      636 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/xeddsa.h
+-rw-rw-rw-   0 root         (0) root         (0)      280 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/zeroize.c
+-rw-rw-rw-   0 root         (0) root         (0)      174 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/additions/zeroize.h
+-rw-rw-rw-   0 root         (0) root         (0)      121 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/api.h
+-rw-rw-rw-   0 root         (0) root         (0)    76457 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/base.h
+-rw-rw-rw-   0 root         (0) root         (0)     2388 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/base2.h
+-rw-rw-rw-   0 root         (0) root         (0)       91 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/d.h
+-rw-rw-rw-   0 root         (0) root         (0)       90 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/d2.h
+-rw-rw-rw-   0 root         (0) root         (0)     1939 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe.h
+-rw-rw-rw-   0 root         (0) root         (0)      170 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_0.c
+-rw-rw-rw-   0 root         (0) root         (0)      170 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_1.c
+-rw-rw-rw-   0 root         (0) root         (0)     1255 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_add.c
+-rw-rw-rw-   0 root         (0) root         (0)     1283 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_cmov.c
+-rw-rw-rw-   0 root         (0) root         (0)      454 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_copy.c
+-rw-rw-rw-   0 root         (0) root         (0)     2222 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_frombytes.c
+-rw-rw-rw-   0 root         (0) root         (0)      135 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_invert.c
+-rw-rw-rw-   0 root         (0) root         (0)      266 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_isnegative.c
+-rw-rw-rw-   0 root         (0) root         (0)      453 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_isnonzero.c
+-rw-rw-rw-   0 root         (0) root         (0)    10744 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_mul.c
+-rw-rw-rw-   0 root         (0) root         (0)      855 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_neg.c
+-rw-rw-rw-   0 root         (0) root         (0)      127 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_pow22523.c
+-rw-rw-rw-   0 root         (0) root         (0)     5980 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sq.c
+-rw-rw-rw-   0 root         (0) root         (0)     6106 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sq2.c
+-rw-rw-rw-   0 root         (0) root         (0)     1255 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sub.c
+-rw-rw-rw-   0 root         (0) root         (0)     3189 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/fe_tobytes.c
+-rw-rw-rw-   0 root         (0) root         (0)     2869 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge.h
+-rw-rw-rw-   0 root         (0) root         (0)      125 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_add.c
+-rw-rw-rw-   0 root         (0) root         (0)     2080 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_add.h
+-rw-rw-rw-   0 root         (0) root         (0)     2371 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_double_scalarmult.c
+-rw-rw-rw-   0 root         (0) root         (0)      987 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_frombytes.c
+-rw-rw-rw-   0 root         (0) root         (0)      128 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_madd.c
+-rw-rw-rw-   0 root         (0) root         (0)     1900 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_madd.h
+-rw-rw-rw-   0 root         (0) root         (0)      128 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_msub.c
+-rw-rw-rw-   0 root         (0) root         (0)     1900 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_msub.h
+-rw-rw-rw-   0 root         (0) root         (0)      165 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p1p1_to_p2.c
+-rw-rw-rw-   0 root         (0) root         (0)      191 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p1p1_to_p3.c
+-rw-rw-rw-   0 root         (0) root         (0)       86 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p2_0.c
+-rw-rw-rw-   0 root         (0) root         (0)      112 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p2_dbl.c
+-rw-rw-rw-   0 root         (0) root         (0)     1476 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p2_dbl.h
+-rw-rw-rw-   0 root         (0) root         (0)      100 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p3_0.c
+-rw-rw-rw-   0 root         (0) root         (0)      131 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p3_dbl.c
+-rw-rw-rw-   0 root         (0) root         (0)      246 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p3_to_cached.c
+-rw-rw-rw-   0 root         (0) root         (0)      149 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p3_to_p2.c
+-rw-rw-rw-   0 root         (0) root         (0)      228 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p3_tobytes.c
+-rw-rw-rw-   0 root         (0) root         (0)      110 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_precomp_0.c
+-rw-rw-rw-   0 root         (0) root         (0)     2477 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_scalarmult_base.c
+-rw-rw-rw-   0 root         (0) root         (0)      125 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_sub.c
+-rw-rw-rw-   0 root         (0) root         (0)     2080 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_sub.h
+-rw-rw-rw-   0 root         (0) root         (0)      225 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/ge_tobytes.c
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.062069 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/
+-rw-rw-rw-   0 root         (0) root         (0)       81 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_int32.h
+-rw-rw-rw-   0 root         (0) root         (0)       87 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_int64.h
+-rw-rw-rw-   0 root         (0) root         (0)      751 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_sign.h
+-rw-rw-rw-   0 root         (0) root         (0)     2034 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_sign_edwards25519sha512batch.h
+-rw-rw-rw-   0 root         (0) root         (0)       93 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_uint32.h
+-rw-rw-rw-   0 root         (0) root         (0)       99 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_uint64.h
+-rw-rw-rw-   0 root         (0) root         (0)      579 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_verify_32.h
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.062069 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_sha512/
+-rw-rw-rw-   0 root         (0) root         (0)     6416 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_sha512/blocks.c
+-rw-rw-rw-   0 root         (0) root         (0)     1807 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_sha512/hash.c
+-rw-rw-rw-   0 root         (0) root         (0)     1036 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/open.c
+-rw-rw-rw-   0 root         (0) root         (0)     5518 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/pow22523.h
+-rw-rw-rw-   0 root         (0) root         (0)     5527 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/pow225521.h
+-rw-rw-rw-   0 root         (0) root         (0)      382 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/sc.h
+-rw-rw-rw-   0 root         (0) root         (0)    12494 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/sc_muladd.c
+-rw-rw-rw-   0 root         (0) root         (0)     8139 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/sc_reduce.c
+-rw-rw-rw-   0 root         (0) root         (0)      817 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/sign.c
+-rw-rw-rw-   0 root         (0) root         (0)       87 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/sqrtm1.h
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.062069 omemo-dr-0.99.2/curve25519/curve/ed25519/tests/
+-rw-rw-rw-   0 root         (0) root         (0)      563 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/tests/internal_fast_tests.h
+-rw-rw-rw-   0 root         (0) root         (0)      540 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/curve25519/curve/ed25519/tests/internal_slow_tests.h
+-rw-rw-rw-   0 root         (0) root         (0)     8040 2023-04-09 19:22:07.000000 omemo-dr-0.99.2/curve25519/curve25519module.c
+-rw-rw-rw-   0 root         (0) root         (0)     4767 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-05-13 17:04:49.074070 omemo-dr-0.99.2/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)      685 2023-03-26 20:37:13.000000 omemo-dr-0.99.2/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.042067 omemo-dr-0.99.2/src/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.062069 omemo-dr-0.99.2/src/omemo_dr/
+-rw-rw-rw-   0 root         (0) root         (0)      104 2023-05-13 17:02:26.000000 omemo-dr-0.99.2/src/omemo_dr/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     2254 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/aes.py
+-rw-rw-rw-   0 root         (0) root         (0)      258 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/const.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.066069 omemo-dr-0.99.2/src/omemo_dr/curve/
+-rw-rw-rw-   0 root         (0) root         (0)     1216 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/curve/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.066069 omemo-dr-0.99.2/src/omemo_dr/ecc/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/ecc/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     2080 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/ecc/curve.py
+-rw-rw-rw-   0 root         (0) root         (0)     2713 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/ecc/djbec.py
+-rw-rw-rw-   0 root         (0) root         (0)      214 2023-05-08 20:42:25.000000 omemo-dr-0.99.2/src/omemo_dr/ecc/ec.py
+-rw-rw-rw-   0 root         (0) root         (0)      471 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/ecc/eckeypair.py
+-rw-rw-rw-   0 root         (0) root         (0)     1252 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/exceptions.py
+-rw-rw-rw-   0 root         (0) root         (0)     1367 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/identitykey.py
+-rw-rw-rw-   0 root         (0) root         (0)     1556 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/identitykeypair.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.066069 omemo-dr-0.99.2/src/omemo_dr/kdf/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/kdf/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      620 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/kdf/derivedmessagesecrets.py
+-rw-rw-rw-   0 root         (0) root         (0)      372 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/kdf/derivedrootsecrets.py
+-rw-rw-rw-   0 root         (0) root         (0)     1736 2023-05-11 18:26:34.000000 omemo-dr-0.99.2/src/omemo_dr/kdf/hkdf.py
+-rw-rw-rw-   0 root         (0) root         (0)      507 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/kdf/messagekeys.py
+-rw-rw-rw-   0 root         (0) root         (0)      837 2023-05-07 15:19:42.000000 omemo-dr-0.99.2/src/omemo_dr/observable.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.066069 omemo-dr-0.99.2/src/omemo_dr/protocol/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      498 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/ciphertextmessage.py
+-rw-rw-rw-   0 root         (0) root         (0)     4076 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/omemo_keyexchange.py
+-rw-rw-rw-   0 root         (0) root         (0)     5152 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/omemo_message.py
+-rw-rw-rw-   0 root         (0) root         (0)     1530 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/omemo_pb2.py
+-rw-rw-rw-   0 root         (0) root         (0)     5046 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/prekeywhispermessage.py
+-rw-rw-rw-   0 root         (0) root         (0)     1620 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/whisper_pb2.py
+-rw-rw-rw-   0 root         (0) root         (0)     4943 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/protocol/whispermessage.py
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/py.typed
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/src/omemo_dr/ratchet/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1410 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/aliceparameters.py
+-rw-rw-rw-   0 root         (0) root         (0)     1368 2023-05-11 18:26:34.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/bobparameters.py
+-rw-rw-rw-   0 root         (0) root         (0)     1614 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/chainkey.py
+-rw-rw-rw-   0 root         (0) root         (0)     5271 2023-05-11 18:26:34.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/ratchetingsession.py
+-rw-rw-rw-   0 root         (0) root         (0)     1412 2023-05-06 21:36:18.000000 omemo-dr-0.99.2/src/omemo_dr/ratchet/rootkey.py
+-rw-rw-rw-   0 root         (0) root         (0)    19091 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/session_manager.py
+-rw-rw-rw-   0 root         (0) root         (0)     5487 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/sessionbuilder.py
+-rw-rw-rw-   0 root         (0) root         (0)    10889 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/sessioncipher.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/src/omemo_dr/state/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/state/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     2812 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/state/prekeybundle.py
+-rw-rw-rw-   0 root         (0) root         (0)     1564 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/state/prekeyrecord.py
+-rw-rw-rw-   0 root         (0) root         (0)     2991 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/state/sessionrecord.py
+-rw-rw-rw-   0 root         (0) root         (0)    12879 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/state/sessionstate.py
+-rw-rw-rw-   0 root         (0) root         (0)     1822 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/state/signedprekeyrecord.py
+-rw-rw-rw-   0 root         (0) root         (0)     5950 2023-05-11 19:26:44.000000 omemo-dr-0.99.2/src/omemo_dr/state/storage_pb2.py
+-rw-rw-rw-   0 root         (0) root         (0)     4777 2023-05-07 10:04:54.000000 omemo-dr-0.99.2/src/omemo_dr/state/store.py
+-rw-rw-rw-   0 root         (0) root         (0)     1369 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/structs.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/src/omemo_dr/util/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/util/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1333 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/src/omemo_dr/util/byteutil.py
+-rw-rw-rw-   0 root         (0) root         (0)     2530 2023-05-07 18:48:15.000000 omemo-dr-0.99.2/src/omemo_dr/util/keyhelper.py
+-rw-rw-rw-   0 root         (0) root         (0)      445 2023-05-07 18:48:15.000000 omemo-dr-0.99.2/src/omemo_dr/util/logging.py
+-rw-rw-rw-   0 root         (0) root         (0)       39 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/src/omemo_dr/util/medium.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.066069 omemo-dr-0.99.2/src/omemo_dr.egg-info/
+-rw-r--r--   0 root         (0) root         (0)    43030 2023-05-13 17:04:49.000000 omemo-dr-0.99.2/src/omemo_dr.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     6870 2023-05-13 17:04:49.000000 omemo-dr-0.99.2/src/omemo_dr.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-05-13 17:04:49.000000 omemo-dr-0.99.2/src/omemo_dr.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       88 2023-05-13 17:04:49.000000 omemo-dr-0.99.2/src/omemo_dr.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        9 2023-05-13 17:04:49.000000 omemo-dr-0.99.2/src/omemo_dr.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/tests/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/tests/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1177 2023-05-06 21:18:55.000000 omemo-dr-0.99.2/tests/inmemoryidentitykeystore.py
+-rw-rw-rw-   0 root         (0) root         (0)      853 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/tests/inmemoryprekeystore.py
+-rw-rw-rw-   0 root         (0) root         (0)     1110 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/tests/inmemorysessionstore.py
+-rw-rw-rw-   0 root         (0) root         (0)     1272 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/tests/inmemorysignedprekeystore.py
+-rw-rw-rw-   0 root         (0) root         (0)     3512 2023-05-06 21:18:55.000000 omemo-dr-0.99.2/tests/inmemorystore.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/tests/kdf/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/tests/kdf/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     9676 2023-05-11 18:26:34.000000 omemo-dr-0.99.2/tests/kdf/test_hkdf.py
+-rw-rw-rw-   0 root         (0) root         (0)    10416 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/tests/test_sessionbuilder.py
+-rw-rw-rw-   0 root         (0) root         (0)     4564 2023-05-11 18:26:34.000000 omemo-dr-0.99.2/tests/test_sessioncipher.py
+-rw-rw-rw-   0 root         (0) root         (0)     9315 2023-05-10 21:35:36.000000 omemo-dr-0.99.2/tests/test_sigs.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-05-13 17:04:49.070070 omemo-dr-0.99.2/tests/util/
+-rw-rw-rw-   0 root         (0) root         (0)        0 2023-03-26 17:49:30.000000 omemo-dr-0.99.2/tests/util/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      497 2023-05-03 19:53:25.000000 omemo-dr-0.99.2/tests/util/test_byteutil.py
```

### Comparing `omemo-dr-0.99.1/LICENSE` & `omemo-dr-0.99.2/LICENSE`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/PKG-INFO` & `omemo-dr-0.99.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: omemo-dr
-Version: 0.99.1
+Version: 0.99.2
 Summary: OMEMO Double Ratchet
 Author: Philipp Hörist
 Author-email: philipp@hoerist.com
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/>
@@ -686,75 +686,68 @@
 Classifier: Topic :: Security :: Cryptography
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
-Initial codebase was forked from https://github.com/tgalal/python-axolotl
-
-This is a python port of [libsignal-protocol-java](https://github.com/WhisperSystems/libaxolotl-android) originally written by [Moxie Marlinspike](https://github.com/moxie0)
-
+Initial codebase was forked from https://github.com/tgalal/python-axolotl but has since been heavily rewritten.
 
 # Dependencies
 
- - [protobuf 3.0+](https://github.com/google/protobuf/)
- - [cryptography](https://cryptography.io)
+ - [protobuf](https://pypi.org/project/protobuf/) (>=4.21.0)
+ - [cryptography](https://pypi.org/project/cryptography/)
 
 ## Linux
 
 ```
 pip install .
 ```
 
 # Usage
 
-This python port is done in an almost 1:1 mapping to the original java code. Therefore any original documentation for the java code can be easily mapped and used with this python port.
-
-## Install time
-
-At install time, a libaxolotl client needs to generate its identity keys, registration id, and
-prekeys.
-
-```python
-    identity_key_pair = KeyHelper.generate_identity_key_pair()
-    registration_id   = KeyHelper.generate_registration_id()
-    pre_keys          = KeyHelper.generate_pre_keys(start_id, 100)
-    last_resort_key   = KeyHelper.generate_last_resort_key()
-    signed_pre_key    = KeyHelper.generate_signed_pre_key(identity_key_pair, 5)
-
-    #Store identity_key_pair somewhere durable and safe.
-    #Store registration_id somewhere durable and safe.
-
-    #Store pre_keys in PreKeyStore.
-    #Store signed prekey in SignedPreKeyStore.
-```
+This library handles only the crypto part of OMEMO, not the XMPP protocol part. This means you need to take care yourself of things like publishing/downloading bundles, publishing/subscribing to PEP deviceliste updates, sending and receiving messages.
 
 ## Building a session
 
-A libaxolotl client needs to implement the Store interface. This will manage loading and storing of identity, 
-prekeys, signed prekeys, and session state.
+A OMEMO client needs to implement the Store interface (omemo_dr.state.store.Store). This will manage loading and storing of identity, prekeys, signed prekeys, and session state.
 
 Once this is implemented, building a session is fairly straightforward:
 
 ```python
-store      = MyStore()
-
-# Instantiate a SessionBuilder for a remote recipient_id + device_id tuple.
-session_builder = SessionBuilder(store, recipient_id, device_id)
+storage = MyStorage()
 
-# Build a session with a PreKey retrieved from the server.
-sessionBuilder.process(retrieved_pre_key)
-
-session_cipher = SessionCipher(store, recipient_id, device_id)
-message        = session_cipher.encrypt("Hello world!")
-
-deliver(message.serialize())
+config = OMEMOConfig(default_prekey_amount=100,
+                     min_prekey_amount=80,
+                     spk_archive_seconds=86400 * 15,
+                     spk_cycle_seconds=86400,
+                     unacknowledged_count=2000)
+
+manager = OMEMOSessionManager(address, storage, config)
+
+# Get your bundle for publishing
+bundle = manager.get_bundle('eu.siacs.conversations.axolotl')
+my_publish_method(bundle)
+
+# Build a session with a downloaded bundle of a remote contact
+bundle = my_receive_bundle_method()
+manager.build_session(remote_address, bundle)
+
+# Encrypt a message to a remote contact
+message = manager.encrypt(remote_address, plaintext)
+my_send_message_method(message)
+
+# Descrypt a message
+message = my_receive_message_method()
+plaintext, fingerprint, trust = manager.decrypt(message, remote_address)
 ```
 
 # Development
 
 ## Generating protobuf files
 
-Download the protobuf-compiler and execute
+Download the protobuf-compiler > 3.19 and execute
 
-`protoc -I=omemo_dr/protobuf --python_out=omemo_dr/protobuf OMEMO.proto WhisperTextProtocol.proto LocalStorageProtocol.proto`
+```bash
+$ protoc -I=src/omemo_dr/protobuf --python_out=src/omemo_dr/protocol omemo.proto whisper.proto
+$ protoc -I=src/omemo_dr/protobuf --python_out=src/omemo_dr/state storage.proto
+```
```

### Comparing `omemo-dr-0.99.1/curve25519/curve/curve25519-donna.c` & `omemo-dr-0.99.2/curve25519/curve/curve25519-donna.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/compare.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/compare.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/convert.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/convert.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/crypto_additions.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/crypto_additions.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/curve_sigs.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/curve_sigs.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/curve_sigs.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/curve_sigs.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ed_sigs.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ed_sigs.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/elligator.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/elligator.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/fe_sqrt.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/fe_sqrt.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_montx_to_p3.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_montx_to_p3.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/ge_scalarmult.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/ge_scalarmult.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_eddsa.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_eddsa.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_labelset.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_labelset.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_veddsa.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_veddsa.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/generalized/gen_x.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/generalized/gen_x.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/keygen.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/keygen.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/open_modified.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/open_modified.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sc_neg.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sc_neg.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/sign_modified.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/sign_modified.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/utility.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/utility.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/xeddsa.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/xeddsa.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/additions/xeddsa.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/additions/xeddsa.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/base.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/base.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/base2.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/base2.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_add.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_add.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_cmov.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_cmov.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_frombytes.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_frombytes.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_mul.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_mul.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_neg.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_neg.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sq.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sq.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sq2.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sq2.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_sub.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_sub.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/fe_tobytes.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/fe_tobytes.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_add.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_add.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_double_scalarmult.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_double_scalarmult.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_frombytes.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_frombytes.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_madd.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_madd.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_msub.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_msub.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_p2_dbl.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_p2_dbl.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_scalarmult_base.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_scalarmult_base.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/ge_sub.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/ge_sub.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_sign.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_sign.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_sign_edwards25519sha512batch.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_sign_edwards25519sha512batch.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_includes/crypto_verify_32.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_includes/crypto_verify_32.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_sha512/blocks.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_sha512/blocks.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/nacl_sha512/hash.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/nacl_sha512/hash.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/open.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/open.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/pow22523.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/pow22523.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/pow225521.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/pow225521.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/sc_muladd.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/sc_muladd.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/sc_reduce.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/sc_reduce.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/sign.c` & `omemo-dr-0.99.2/curve25519/curve/ed25519/sign.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/tests/internal_fast_tests.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/tests/internal_fast_tests.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve/ed25519/tests/internal_slow_tests.h` & `omemo-dr-0.99.2/curve25519/curve/ed25519/tests/internal_slow_tests.h`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/curve25519/curve25519module.c` & `omemo-dr-0.99.2/curve25519/curve25519module.c`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/pyproject.toml` & `omemo-dr-0.99.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -17,15 +17,15 @@
   "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
   "Programming Language :: Python :: 3",
   "Topic :: Security :: Cryptography",
   "Topic :: Software Development :: Libraries :: Python Modules"
 ]
 dependencies = [
   "cryptography",
-  "protobuf>=3.0.0",
+  "protobuf>=4.21.0",
 ]
 dynamic = ["version"]
 
 [project.optional-dependencies]
 dev = [
   "ruff>=0.0.254",
   "codespell[toml]>=2.2.4",
@@ -56,16 +56,16 @@
 
 exclude = [
   "**/__pycache__",
   ".git",
   "build",
   "node_modules",
   "src/omemo_dr/protocol/omemo_pb2.py",
-  "src/omemo_dr/protocol/whisperprotos_pb2.py",
-  "src/omemo_dr/state/storageprotos_pb2.py",
+  "src/omemo_dr/protocol/whisper_pb2.py",
+  "src/omemo_dr/state/storage_pb2.py",
 ]
 
 [tool.ruff]
 line-length = 88
 
 select = [
   "A",      # flake8-builtins
```

### Comparing `omemo-dr-0.99.1/setup.py` & `omemo-dr-0.99.2/setup.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/src/omemo_dr/aes.py` & `omemo-dr-0.99.2/src/omemo_dr/aes.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/src/omemo_dr/curve/__init__.py` & `omemo-dr-0.99.2/src/omemo_dr/curve/__init__.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ecc/curve.py` & `omemo-dr-0.99.2/src/omemo_dr/ecc/curve.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,27 +1,21 @@
 from __future__ import annotations
 
 from typing import Union
 
 import os
 
 from .. import curve
-from ..exceptions import InvalidKeyException
 from .djbec import CurvePublicKey
 from .djbec import DjbECPrivateKey
 from .djbec import EdPublicKey
 from .eckeypair import ECKeyPair
 
-CURVE25519_KEY_LEN = 33
-ED25519_KEY_LEN = 32
-
 
 class Curve:
-    DJB_TYPE = 5
-
     @staticmethod
     def _generate_private_key() -> bytes:
         rand = os.urandom(32)
         return curve.generate_private_key(rand)
 
     @staticmethod
     def _generate_public_key(private_key: bytes) -> bytes:
@@ -30,34 +24,20 @@
     @staticmethod
     def generate_key_pair() -> ECKeyPair:
         private_key = Curve._generate_private_key()
         public_key = Curve._generate_public_key(private_key)
         return ECKeyPair(CurvePublicKey(public_key), DjbECPrivateKey(private_key))
 
     @staticmethod
-    def decode_point(
-        _bytes: bytearray, offset: int = 0
-    ) -> Union[CurvePublicKey, EdPublicKey]:
-        key_type = _bytes[0]
-        key_len = len(_bytes)
-
-        if key_len == CURVE25519_KEY_LEN and key_type == Curve.DJB_TYPE:
-            return CurvePublicKey(bytes(_bytes[1:]))
-
-        elif key_len == ED25519_KEY_LEN:
-            return EdPublicKey(_bytes)
-
-        else:
-            raise InvalidKeyException(
-                "Unknown key type or length: %s - %s" % (key_type, key_len)
-            )
+    def decode_point(bytes_: bytes) -> CurvePublicKey:
+        return CurvePublicKey.from_bytes(bytes_)
 
     @staticmethod
     def decode_private_point(_bytes: bytes) -> DjbECPrivateKey:
-        return DjbECPrivateKey(bytes(_bytes))
+        return DjbECPrivateKey(_bytes)
 
     @staticmethod
     def calculate_agreement(
         public_key: CurvePublicKey, private_key: DjbECPrivateKey
     ) -> bytes:
         return curve.calculate_agreement(
             private_key.get_private_key(), public_key.get_bytes()
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ecc/djbec.py` & `omemo-dr-0.99.2/src/omemo_dr/ecc/djbec.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,32 +1,28 @@
 from __future__ import annotations
 
 from typing import Any
 
 import binascii
 
 from .. import curve
+from ..const import ENCODED_KEY_LENGTH
+from ..const import LEGACY_ENCODED_KEY_LENGTH
+from ..exceptions import InvalidKeyException
 from ..util.byteutil import ByteUtil
 from .ec import ECPrivateKey
 from .ec import ECPublicKey
 
-CURVE25519_KEY_LEN = 33
-ED25519_KEY_LEN = 32
-DJB_TYPE = 5
+DJB_TYPE = 0x05
 
 
 class DjbECPublicKey(ECPublicKey):
     def __init__(self, _bytes: bytes) -> None:
         self._public_key = _bytes
 
-    def get_type(self) -> int:
-        from .curve import Curve
-
-        return Curve.DJB_TYPE
-
     def get_bytes(self) -> bytes:
         return self._public_key
 
     def get_public_key(self) -> bytes:
         return self._public_key
 
     def __eq__(self, other: Any) -> bool:
@@ -47,41 +43,52 @@
         elif my_val == other_val:
             return 0
         else:
             return 1
 
 
 class CurvePublicKey(DjbECPublicKey):
-    def serialize(self) -> bytes:
-        from .curve import Curve
+    @classmethod
+    def from_bytes(cls, bytes_: bytes) -> CurvePublicKey:
+        key_length = len(bytes_)
+        if key_length == LEGACY_ENCODED_KEY_LENGTH and bytes_[0] == 0x05:
+            return cls(bytes_[1:])
+
+        if key_length == ENCODED_KEY_LENGTH:
+            return cls(bytes_)
+
+        raise InvalidKeyException("Unknown key type or length: %s" % bytes_)
 
-        combined = ByteUtil.combine([Curve.DJB_TYPE], self._public_key)
-        return bytes(combined)
+    def serialize(self) -> bytes:
+        return ByteUtil.combine([DJB_TYPE], self._public_key)
 
     def to_ed(self) -> EdPublicKey:
         return EdPublicKey(curve.convert_curve_to_ed_pubkey(self._public_key))
 
 
 class EdPublicKey(DjbECPublicKey):
+    @classmethod
+    def from_bytes(cls, bytes_: bytes) -> EdPublicKey:
+        key_length = len(bytes_)
+        if key_length == ENCODED_KEY_LENGTH:
+            return cls(bytes_)
+
+        raise InvalidKeyException("Unknown key type or length: %s" % bytes_)
+
     def to_curve(self) -> CurvePublicKey:
         return CurvePublicKey(curve.convert_ed_to_curve_pubkey(self._public_key))
 
     def serialize(self) -> bytes:
         return self._public_key
 
 
 class DjbECPrivateKey(ECPrivateKey):
     def __init__(self, private_key: bytes) -> None:
         self._private_key = private_key
 
-    def get_type(self) -> int:
-        from .curve import Curve
-
-        return Curve.DJB_TYPE
-
     def get_private_key(self) -> bytes:
         return self._private_key
 
     def serialize(self) -> bytes:
         return self._private_key
 
     def __eq__(self, other: Any) -> bool:
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/exceptions.py` & `omemo-dr-0.99.2/src/omemo_dr/exceptions.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/src/omemo_dr/identitykey.py` & `omemo-dr-0.99.2/src/omemo_dr/identitykey.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,36 +1,33 @@
 from __future__ import annotations
 
-from typing import Optional
 from typing import Union
 
 import binascii
 import textwrap
 
 from .ecc.curve import Curve
-from .ecc.ec import ECPublicKey
+from .ecc.djbec import CurvePublicKey
 
 
 class IdentityKey:
     def __init__(
         self,
-        ec_pub_key_or_bytes: Union[ECPublicKey, bytes, bytearray],
-        offset: Optional[int] = None,
+        ec_pub_key_or_bytes: Union[CurvePublicKey, bytes],
     ) -> None:
-        if isinstance(ec_pub_key_or_bytes, ECPublicKey):
-            self.public_key = ec_pub_key_or_bytes
+        if isinstance(ec_pub_key_or_bytes, CurvePublicKey):
+            self._public_key = ec_pub_key_or_bytes
         else:
-            assert offset is not None
-            self.public_key = Curve.decode_point(bytearray(ec_pub_key_or_bytes), offset)
+            self._public_key = Curve.decode_point(ec_pub_key_or_bytes)
 
-    def get_public_key(self) -> ECPublicKey:
-        return self.public_key
+    def get_public_key(self) -> CurvePublicKey:
+        return self._public_key
 
     def serialize(self) -> bytes:
-        return self.public_key.serialize()
+        return self._public_key.serialize()
 
     def get_fingerprint(self, formatted: bool = False) -> str:
         public_key = self.serialize()
         fingerprint = binascii.hexlify(public_key).decode()[2:]
         if not formatted:
             return fingerprint
         fplen = len(fingerprint)
@@ -39,11 +36,11 @@
         for word in range(0, fplen, wordsize):
             buf += f"{fingerprint[word : word + wordsize]} "
         buf = textwrap.fill(buf, width=36)
         return buf.rstrip().upper()
 
     def __eq__(self, other: object) -> bool:
         assert isinstance(other, IdentityKey)
-        return self.public_key == other.get_public_key()
+        return self._public_key == other.get_public_key()
 
     def __hash__(self) -> int:
-        return hash(self.public_key.serialize())
+        return hash(self._public_key.serialize())
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/identitykeypair.py` & `omemo-dr-0.99.2/src/omemo_dr/identitykeypair.py`

 * *Files 24% similar despite different names*

```diff
@@ -3,45 +3,51 @@
 from typing import cast
 
 import google.protobuf.message
 
 from .ecc.curve import Curve
 from .ecc.djbec import DjbECPrivateKey
 from .identitykey import IdentityKey
-from .state.storageprotos_pb2 import IdentityKeyPairStructure
+from .state import storage_pb2
 
 
 class IdentityKeyPair:
     def __init__(self, structure: IdentityKeyPairStructureProto) -> None:
         self._structure = structure
 
     @classmethod
     def new(
         cls,
         identity_key_public_key: IdentityKey,
         ec_private_key: DjbECPrivateKey,
     ) -> IdentityKeyPair:
-        structure = cast(IdentityKeyPairStructureProto, IdentityKeyPairStructure())
+        structure = cast(
+            IdentityKeyPairStructureProto,
+            storage_pb2.IdentityKeyPairStructure(),  # pyright: ignore
+        )
 
         structure.publicKey = identity_key_public_key.serialize()
         structure.privateKey = ec_private_key.serialize()
 
         return cls(structure)
 
     @classmethod
     def from_bytes(cls, serialized: bytes) -> IdentityKeyPair:
-        structure = cast(IdentityKeyPairStructureProto, IdentityKeyPairStructure())
+        structure = cast(
+            IdentityKeyPairStructureProto,
+            storage_pb2.IdentityKeyPairStructure(),  # pyright: ignore
+        )
         structure.ParseFromString(serialized)
         return cls(structure)
 
     def get_public_key(self) -> IdentityKey:
-        return IdentityKey(bytearray(self._structure.publicKey), offset=0)
+        return IdentityKey(self._structure.publicKey)
 
     def get_private_key(self) -> DjbECPrivateKey:
-        return Curve.decode_private_point(bytearray(self._structure.privateKey))
+        return Curve.decode_private_point(self._structure.privateKey)
 
     def serialize(self) -> bytes:
         return self._structure.SerializeToString()
 
 
 class IdentityKeyPairStructureProto(google.protobuf.message.Message):
     publicKey: bytes
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/kdf/derivedmessagesecrets.py` & `omemo-dr-0.99.2/src/omemo_dr/kdf/derivedmessagesecrets.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/src/omemo_dr/kdf/hkdf.py` & `omemo-dr-0.99.2/src/omemo_dr/kdf/hkdf.py`

 * *Files 20% similar despite different names*

```diff
@@ -7,56 +7,51 @@
 import math
 
 
 class HKDF:
     HASH_OUTPUT_SIZE = 32
 
     def __init__(self, session_version: int) -> None:
-        if session_version not in (2, 3, 4):
+        if session_version not in (3, 4):
             raise AssertionError("Unknown version: %s " % session_version)
 
-        self.session_version = session_version
+        self._session_version = session_version
+
+    def get_session_version(self) -> int:
+        return self._session_version
 
     def derive_secrets(
         self,
         input_key_material: bytes,
         info: bytes,
         output_length: int,
         salt: Optional[bytes] = None,
     ) -> bytes:
-        salt = salt or bytearray(self.HASH_OUTPUT_SIZE)
+        salt = salt or bytes(self.HASH_OUTPUT_SIZE)
         prk = self._extract(salt, input_key_material)
         return self._expand(prk, info, output_length)
 
     def _extract(self, salt: bytes, input_key_material: bytes) -> bytes:
         mac = hmac.new(bytes(salt), digestmod=hashlib.sha256)
         mac.update(bytes(input_key_material))
         return mac.digest()
 
     def _expand(self, prk: bytes, info: bytes, output_size: int) -> bytes:
         iterations = int(math.ceil(float(output_size) / float(self.HASH_OUTPUT_SIZE)))
-        mixin = bytearray()
+        mixin = b""
         results = bytearray()
         remaining_bytes = output_size
 
-        for i in range(
-            self._get_iteration_start_offset(),
-            iterations + self._get_iteration_start_offset(),
-        ):
+        for i in range(1, iterations + 1):
             mac = hmac.new(prk, digestmod=hashlib.sha256)
-            mac.update(bytes(mixin))
-            mac.update(bytes(info))
+            mac.update(mixin)
+            mac.update(info)
             updateChr = chr(i % 256)
             mac.update(updateChr.encode())
 
             stepResult = mac.digest()
             stepSize = min(remaining_bytes, len(stepResult))
             results.extend(stepResult[:stepSize])
             mixin = stepResult
             remaining_bytes -= stepSize
 
         return bytes(results)
-
-    def _get_iteration_start_offset(self) -> int:
-        if self.session_version == 2:
-            return 0
-        return 1
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/observable.py` & `omemo-dr-0.99.2/src/omemo_dr/observable.py`

 * *Files 11% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 
 import logging
 from collections import defaultdict
 from collections.abc import Callable
 
 
 class Observable:
-    def __init__(self, log_: logging.Logger) -> None:
-        self._log = log_
+    def __init__(self) -> None:
+        self._log = logging.getLogger(__name__)
         self._callbacks: defaultdict[str, list[Callable[..., Any]]] = defaultdict(list)
 
     def register_signal(self, signal_name: str, func: Callable[..., Any]) -> None:
         self._callbacks[signal_name].append(func)
 
     def _unregister_signals(self) -> None:
         self._callbacks = defaultdict(list)
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/protocol/omemo_keyexchange.py` & `omemo-dr-0.99.2/src/omemo_dr/protocol/omemo_keyexchange.py`

 * *Files 8% similar despite different names*

```diff
@@ -6,52 +6,54 @@
 from google.protobuf.message import DecodeError
 
 from ..ecc.curve import Curve
 from ..ecc.ec import ECPublicKey
 from ..exceptions import InvalidKeyException
 from ..exceptions import InvalidMessageException
 from ..identitykey import IdentityKey
-from . import omemo_pb2 as omemoprotos
+from . import omemo_pb2
 from .ciphertextmessage import CiphertextMessage
 from .omemo_message import OMEMOMessage
 
 
 class OMEMOKeyExchange(CiphertextMessage):
     def __init__(
         self,
         serialized: bytes,
         message_version: int,
-        registration_id: int,
+        device_id: int,
         pre_key_id: int,
         signed_pre_key_id: int,
         ec_public_base_key: ECPublicKey,
         identity_key: IdentityKey,
         omemo_message: OMEMOMessage,
     ):
         self._message_version = message_version
-        self._registration_id = registration_id
+        self._device_id = device_id
         self._pre_key_id = pre_key_id
         self._signed_pre_key_id = signed_pre_key_id
         self._base_key = ec_public_base_key
         self._identity_key = identity_key
         self._message = omemo_message
         self._serialized = serialized
 
     @classmethod
     def new(
         cls,
         message_version: int,
-        registration_id: int,
+        device_id: int,
         pre_key_id: int,
         signed_pre_key_id: int,
         ec_public_base_key: ECPublicKey,
         identity_key: IdentityKey,
         omemo_message: OMEMOMessage,
     ) -> OMEMOKeyExchange:
-        key_exchange = cast(OMEMOKeyExchangeProto, omemoprotos.OMEMOKeyExchange())
+        key_exchange = cast(
+            OMEMOKeyExchangeProto, omemo_pb2.OMEMOKeyExchange()  # pyright: ignore
+        )
         key_exchange.pk_id = pre_key_id
         key_exchange.spk_id = signed_pre_key_id
         key_exchange.ik = identity_key.serialize()
         key_exchange.ek = ec_public_base_key.serialize()
         key_exchange.message = omemo_message.serialize()
 
         serialized = key_exchange.SerializeToString()
@@ -66,31 +68,31 @@
             identity_key,
             omemo_message,
         )
 
     @classmethod
     def from_bytes(cls, serialized: bytes) -> OMEMOKeyExchange:
         try:
-            key_exchange = cast(OMEMOKeyExchangeProto, omemoprotos.OMEMOKeyExchange())
+            key_exchange = cast(
+                OMEMOKeyExchangeProto, omemo_pb2.OMEMOKeyExchange()  # pyright: ignore
+            )
             key_exchange.ParseFromString(serialized)
 
             if (
                 not key_exchange.spk_id
                 or not key_exchange.ek
                 or not key_exchange.ik
                 or not key_exchange.message
             ):
                 raise InvalidMessageException("Incomplete message")
 
             pre_key_id = key_exchange.pk_id
             signed_pre_key_id = key_exchange.spk_id
-            ec_public_base_key = Curve.decode_point(bytearray(key_exchange.ek), 0)
-            identity_key = IdentityKey(
-                Curve.decode_point(bytearray(key_exchange.ik), 0)
-            )
+            ec_public_base_key = Curve.decode_point(key_exchange.ek)
+            identity_key = IdentityKey(Curve.decode_point(key_exchange.ik))
             omemo_message = OMEMOMessage.from_bytes(key_exchange.message)
 
         except (InvalidKeyException, DecodeError) as error:
             raise InvalidMessageException(str(error))
 
         return cls(
             serialized,
@@ -105,16 +107,16 @@
 
     def get_message_version(self) -> int:
         return 4
 
     def get_identity_key(self) -> IdentityKey:
         return self._identity_key
 
-    def get_registration_id(self) -> int:
-        return self._registration_id
+    def get_device_id(self) -> int:
+        return self._device_id
 
     def get_pre_key_id(self) -> int:
         return self._pre_key_id
 
     def get_signed_pre_key_id(self) -> int:
         return self._signed_pre_key_id
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/protocol/omemo_message.py` & `omemo-dr-0.99.2/src/omemo_dr/protocol/omemo_message.py`

 * *Files 4% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 
 from ..ecc.curve import Curve
 from ..ecc.djbec import CurvePublicKey
 from ..exceptions import InvalidKeyException
 from ..exceptions import InvalidMessageException
 from ..identitykey import IdentityKey
 from ..util.byteutil import ByteUtil
-from . import omemo_pb2 as omemoprotos
+from . import omemo_pb2
 from .ciphertextmessage import CiphertextMessage
 
 MAC_LENGTH = 16
 
 
 class OMEMOMessage(CiphertextMessage):
     def __init__(
@@ -42,28 +42,31 @@
         ec_public_key_sender_ratchet_key: CurvePublicKey,
         counter: int,
         previous_counter: int,
         ciphertext: bytes,
         sender_identity_key: IdentityKey,
         receiver_identity_key: IdentityKey,
     ) -> OMEMOMessage:
-        omemo_message = cast(OMEMOMessageProto, omemoprotos.OMEMOMessage())
+        omemo_message = cast(
+            OMEMOMessageProto, omemo_pb2.OMEMOMessage()  # pyright: ignore
+        )
 
         omemo_message.dh_pub = ec_public_key_sender_ratchet_key.serialize()
         omemo_message.n = counter
         omemo_message.pn = previous_counter
         omemo_message.ciphertext = ciphertext
         omemo_message = omemo_message.SerializeToString()
 
         mac = cls.get_mac(
             sender_identity_key, receiver_identity_key, mac_key, omemo_message
         )
 
         authenticated_message = cast(
-            OMEMOAuthenticatedMessageProto, omemoprotos.OMEMOAuthenticatedMessage()
+            OMEMOAuthenticatedMessageProto,
+            omemo_pb2.OMEMOAuthenticatedMessage(),  # pyright: ignore
         )
         authenticated_message.mac = mac
         authenticated_message.message = omemo_message
         authenticated_message = authenticated_message.SerializeToString()
 
         return cls(
             authenticated_message,
@@ -72,30 +75,33 @@
             previous_counter,
             ciphertext,
         )
 
     @classmethod
     def from_bytes(cls, serialized: bytes) -> OMEMOMessage:
         authenticated_message = cast(
-            OMEMOAuthenticatedMessageProto, omemoprotos.OMEMOAuthenticatedMessage()
+            OMEMOAuthenticatedMessageProto,
+            omemo_pb2.OMEMOAuthenticatedMessage(),  # pyright: ignore
         )
         try:
             authenticated_message.ParseFromString(serialized)
         except google.protobuf.message.DecodeError as error:
             raise InvalidMessageException(str(error))
 
-        omemo_message = cast(OMEMOMessageProto, omemoprotos.OMEMOMessage())
+        omemo_message = cast(
+            OMEMOMessageProto, omemo_pb2.OMEMOMessage()  # pyright: ignore
+        )
 
         try:
             omemo_message.ParseFromString(authenticated_message.message)
         except google.protobuf.message.DecodeError as error:
             raise InvalidMessageException(str(error))
 
         try:
-            sender_ratchet_key = Curve.decode_point(bytearray(omemo_message.dh_pub), 0)
+            sender_ratchet_key = Curve.decode_point(omemo_message.dh_pub)
             assert isinstance(sender_ratchet_key, CurvePublicKey)
         except InvalidKeyException as error:
             raise InvalidMessageException(str(error))
 
         return OMEMOMessage(
             serialized,
             sender_ratchet_key,
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/protocol/prekeywhispermessage.py` & `omemo-dr-0.99.2/src/omemo_dr/protocol/prekeywhispermessage.py`

 * *Files 16% similar despite different names*

```diff
@@ -2,76 +2,77 @@
 
 from typing import cast
 
 import google.protobuf.message
 from google.protobuf.message import DecodeError
 
 from ..ecc.curve import Curve
-from ..ecc.ec import ECPublicKey
+from ..ecc.djbec import CurvePublicKey
 from ..exceptions import InvalidKeyException
 from ..exceptions import InvalidMessageException
 from ..exceptions import InvalidVersionException
 from ..identitykey import IdentityKey
 from ..util.byteutil import ByteUtil
-from . import whisperprotos_pb2 as whisperprotos
+from . import whisper_pb2
 from .ciphertextmessage import CiphertextMessage
 from .whispermessage import WhisperMessage
 
 
 class PreKeyWhisperMessage(CiphertextMessage):
     def __init__(
         self,
         serialized: bytes,
         message_version: int,
-        registration_id: int,
+        device_id: int,
         pre_key_id: int,
         signed_pre_key_id: int,
-        ec_public_base_key: ECPublicKey,
+        ec_public_base_key: CurvePublicKey,
         identity_key: IdentityKey,
         whisper_message: WhisperMessage,
     ) -> None:
         self._serialized = serialized
         self._message_version = message_version
-        self._registration_id = registration_id
+        self._device_id = device_id
         self._pre_key_id = pre_key_id
         self._signed_pre_key_id = signed_pre_key_id
         self._ec_public_base_key = ec_public_base_key
         self._identity_key = identity_key
         self._whisper_message = whisper_message
 
     @classmethod
     def new(
         cls,
         message_version: int,
-        registration_id: int,
+        device_id: int,
         pre_key_id: int,
         signed_pre_key_id: int,
-        ec_public_base_key: ECPublicKey,
+        ec_public_base_key: CurvePublicKey,
         identity_key: IdentityKey,
         whisper_message: WhisperMessage,
     ) -> PreKeyWhisperMessage:
         prekey_message = cast(
-            PreKeyWhisperMessageProto, whisperprotos.PreKeyWhisperMessage()
+            PreKeyWhisperMessageProto,
+            whisper_pb2.PreKeyWhisperMessage(),  # pyright: ignore
         )
         prekey_message.signedPreKeyId = signed_pre_key_id
         prekey_message.preKeyId = pre_key_id
         prekey_message.baseKey = ec_public_base_key.serialize()
         prekey_message.identityKey = identity_key.serialize()
         prekey_message.message = whisper_message.serialize()
-        prekey_message.registrationId = registration_id
+        prekey_message.registrationId = device_id
 
         version_bytes = ByteUtil.ints_to_byte_high_and_low(3, 3)
         message_bytes = prekey_message.SerializeToString()
 
-        serialized = bytes(ByteUtil.combine(version_bytes, message_bytes))
+        serialized = ByteUtil.combine(version_bytes, message_bytes)
 
         return cls(
             serialized,
             message_version,
-            registration_id,
+            device_id,
             pre_key_id,
             signed_pre_key_id,
             ec_public_base_key,
             identity_key,
             whisper_message,
         )
 
@@ -79,66 +80,67 @@
     def from_bytes(cls, serialized: bytes) -> PreKeyWhisperMessage:
         try:
             version = ByteUtil.high_bits_to_int(serialized[0])
             if version != 3:
                 raise InvalidVersionException("Unknown version %s" % version)
 
             pre_key_whisper_message = cast(
-                PreKeyWhisperMessageProto, whisperprotos.PreKeyWhisperMessage()
+                PreKeyWhisperMessageProto,
+                whisper_pb2.PreKeyWhisperMessage(),  # pyright: ignore
             )
             pre_key_whisper_message.ParseFromString(serialized[1:])
 
             if (
                 not pre_key_whisper_message.signedPreKeyId
                 or not pre_key_whisper_message.baseKey
                 or not pre_key_whisper_message.identityKey
                 or not pre_key_whisper_message.message
             ):
                 raise InvalidMessageException("Incomplete message")
 
-            registration_id = pre_key_whisper_message.registrationId
+            device_id = pre_key_whisper_message.registrationId
             pre_key_id = pre_key_whisper_message.preKeyId
             signed_pre_key_id = pre_key_whisper_message.signedPreKeyId
 
-            base_key = Curve.decode_point(bytearray(pre_key_whisper_message.baseKey), 0)
+            base_key = Curve.decode_point(pre_key_whisper_message.baseKey)
 
             identity_key = IdentityKey(
-                Curve.decode_point(bytearray(pre_key_whisper_message.identityKey), 0)
+                Curve.decode_point(pre_key_whisper_message.identityKey)
             )
             message = WhisperMessage.from_bytes(pre_key_whisper_message.message)
         except (InvalidKeyException, DecodeError) as error:
             raise InvalidMessageException(str(error))
 
         return cls(
             serialized,
             version,
-            registration_id,
+            device_id,
             pre_key_id,
             signed_pre_key_id,
             base_key,
             identity_key,
             message,
         )
 
     def get_message_version(self) -> int:
         return self._message_version
 
     def get_identity_key(self) -> IdentityKey:
         return self._identity_key
 
-    def get_registration_id(self) -> int:
-        return self._registration_id
+    def get_device_id(self) -> int:
+        return self._device_id
 
     def get_pre_key_id(self) -> int:
         return self._pre_key_id
 
     def get_signed_pre_key_id(self) -> int:
         return self._signed_pre_key_id
 
-    def get_base_key(self) -> ECPublicKey:
+    def get_base_key(self) -> CurvePublicKey:
         return self._ec_public_base_key
 
     def get_whisper_message(self) -> WhisperMessage:
         return self._whisper_message
 
     def serialize(self) -> bytes:
         return self._serialized
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/protocol/whispermessage.py` & `omemo-dr-0.99.2/src/omemo_dr/protocol/whispermessage.py`

 * *Files 6% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 
 from ..ecc.curve import Curve
 from ..ecc.djbec import CurvePublicKey
 from ..exceptions import InvalidKeyException
 from ..exceptions import InvalidMessageException
 from ..identitykey import IdentityKey
 from ..util.byteutil import ByteUtil
-from . import whisperprotos_pb2 as whisperprotos
+from . import whisper_pb2
 from .ciphertextmessage import CiphertextMessage
 
 MAC_LENGTH = 8
 
 
 class WhisperMessage(CiphertextMessage):
     def __init__(
@@ -44,29 +44,31 @@
         previous_counter: int,
         ciphertext: bytes,
         sender_identity_key: IdentityKey,
         receiver_identity_key: IdentityKey,
     ) -> WhisperMessage:
         version = ByteUtil.ints_to_byte_high_and_low(message_version, message_version)
 
-        message = cast(WhisperMessageProto, whisperprotos.WhisperMessage())
+        message = cast(
+            WhisperMessageProto, whisper_pb2.WhisperMessage()  # pyright: ignore
+        )
         message.ratchetKey = ec_public_key_sender_ratchet_key.serialize()
         message.counter = counter
         message.previousCounter = previous_counter
         message.ciphertext = ciphertext
         message = message.SerializeToString()
 
         mac = cls.get_mac(
             sender_identity_key,
             receiver_identity_key,
             mac_key,
             ByteUtil.combine(version, message),
         )
 
-        serialized = bytes(ByteUtil.combine(version, message, mac))
+        serialized = ByteUtil.combine(version, message, mac)
 
         return cls(
             serialized,
             ec_public_key_sender_ratchet_key,
             counter,
             previous_counter,
             ciphertext,
@@ -83,24 +85,24 @@
 
         version = ByteUtil.high_bits_to_int(message_parts[0][0])
         message = message_parts[1]
 
         if version != 3:
             raise InvalidMessageException("Unknown version: %s" % version)
 
-        whisper_message = cast(WhisperMessageProto, whisperprotos.WhisperMessage())
+        whisper_message = cast(
+            WhisperMessageProto, whisper_pb2.WhisperMessage()  # pyright: ignore
+        )
         whisper_message.ParseFromString(message)
 
         if not whisper_message.ciphertext or not whisper_message.ratchetKey:
             raise InvalidMessageException("Incomplete message")
 
         try:
-            sender_ratchet_key = Curve.decode_point(
-                bytearray(whisper_message.ratchetKey), 0
-            )
+            sender_ratchet_key = Curve.decode_point(whisper_message.ratchetKey)
             assert isinstance(sender_ratchet_key, CurvePublicKey)
         except InvalidKeyException as e:
             raise InvalidMessageException(str(e))
 
         return WhisperMessage(
             serialized,
             sender_ratchet_key,
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ratchet/aliceparameters.py` & `omemo-dr-0.99.2/src/omemo_dr/ratchet/aliceparameters.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,42 +1,42 @@
 from __future__ import annotations
 
-from ..ecc.ec import ECPublicKey
+from ..ecc.djbec import CurvePublicKey
 from ..ecc.eckeypair import ECKeyPair
 from ..identitykey import IdentityKey
 from ..identitykeypair import IdentityKeyPair
 
 
 class AliceParameters:
     def __init__(
         self,
         our_identity_key: IdentityKeyPair,
         our_base_key: ECKeyPair,
         their_identity_key: IdentityKey,
-        their_signed_pre_key: ECPublicKey,
-        their_ratchet_key: ECPublicKey,
-        their_one_time_pre_key: ECPublicKey | None,
+        their_signed_pre_key: CurvePublicKey,
+        their_ratchet_key: CurvePublicKey,
+        their_one_time_pre_key: CurvePublicKey,
     ) -> None:
-        self.our_base_key = our_base_key
-        self.our_identity_key = our_identity_key
-        self.their_signed_pre_key = their_signed_pre_key
-        self.their_ratchet_key = their_ratchet_key
-        self.their_identity_key = their_identity_key
-        self.their_one_time_pre_key = their_one_time_pre_key
+        self._our_base_key = our_base_key
+        self._our_identity_key = our_identity_key
+        self._their_signed_pre_key = their_signed_pre_key
+        self._their_ratchet_key = their_ratchet_key
+        self._their_identity_key = their_identity_key
+        self._their_one_time_pre_key = their_one_time_pre_key
 
     def get_our_identity_key(self) -> IdentityKeyPair:
-        return self.our_identity_key
+        return self._our_identity_key
 
     def get_our_base_key(self) -> ECKeyPair:
-        return self.our_base_key
+        return self._our_base_key
 
     def get_their_identity_key(self) -> IdentityKey:
-        return self.their_identity_key
+        return self._their_identity_key
 
-    def get_their_signed_pre_key(self) -> ECPublicKey:
-        return self.their_signed_pre_key
+    def get_their_signed_pre_key(self) -> CurvePublicKey:
+        return self._their_signed_pre_key
 
-    def get_their_one_time_pre_key(self) -> ECPublicKey | None:
-        return self.their_one_time_pre_key
+    def get_their_one_time_pre_key(self) -> CurvePublicKey:
+        return self._their_one_time_pre_key
 
-    def get_their_ratchet_key(self) -> ECPublicKey:
-        return self.their_ratchet_key
+    def get_their_ratchet_key(self) -> CurvePublicKey:
+        return self._their_ratchet_key
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ratchet/bobparameters.py` & `omemo-dr-0.99.2/src/omemo_dr/ratchet/bobparameters.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,42 +1,42 @@
 from __future__ import annotations
 
-from ..ecc.ec import ECPublicKey
+from ..ecc.djbec import CurvePublicKey
 from ..ecc.eckeypair import ECKeyPair
 from ..identitykey import IdentityKey
 from ..identitykeypair import IdentityKeyPair
 
 
 class BobParameters:
     def __init__(
         self,
         our_identity_key: IdentityKeyPair,
         our_signed_pre_key: ECKeyPair,
         our_ratchet_key: ECKeyPair,
-        our_one_time_pre_key: ECKeyPair | None,
+        our_one_time_pre_key: ECKeyPair,
         their_identity_key: IdentityKey,
-        their_base_key: ECPublicKey,
+        their_base_key: CurvePublicKey,
     ) -> None:
-        self.our_identity_key = our_identity_key
-        self.our_signed_pre_key = our_signed_pre_key
-        self.our_ratchet_key = our_ratchet_key
-        self.our_one_time_pre_key = our_one_time_pre_key
-        self.their_identity_key = their_identity_key
-        self.their_base_key = their_base_key
+        self._our_identity_key = our_identity_key
+        self._our_signed_pre_key = our_signed_pre_key
+        self._our_ratchet_key = our_ratchet_key
+        self._our_one_time_pre_key = our_one_time_pre_key
+        self._their_identity_key = their_identity_key
+        self._their_base_key = their_base_key
 
     def get_our_identity_key(self) -> IdentityKeyPair:
-        return self.our_identity_key
+        return self._our_identity_key
 
     def get_our_signed_pre_key(self) -> ECKeyPair:
-        return self.our_signed_pre_key
+        return self._our_signed_pre_key
 
-    def get_our_one_time_pre_key(self) -> ECKeyPair | None:
-        return self.our_one_time_pre_key
+    def get_our_one_time_pre_key(self) -> ECKeyPair:
+        return self._our_one_time_pre_key
 
     def get_their_identity_key(self) -> IdentityKey:
-        return self.their_identity_key
+        return self._their_identity_key
 
-    def get_their_base_key(self) -> ECPublicKey:
-        return self.their_base_key
+    def get_their_base_key(self) -> CurvePublicKey:
+        return self._their_base_key
 
     def get_our_ratchet_key(self) -> ECKeyPair:
-        return self.our_ratchet_key
+        return self._our_ratchet_key
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ratchet/chainkey.py` & `omemo-dr-0.99.2/src/omemo_dr/ratchet/chainkey.py`

 * *Files 19% similar despite different names*

```diff
@@ -3,51 +3,51 @@
 import hashlib
 import hmac
 
 from ..kdf.derivedmessagesecrets import DerivedMessageSecrets
 from ..kdf.hkdf import HKDF
 from ..kdf.messagekeys import MessageKeys
 
+MESSAGE_KEY_SEED = bytes([0x01])
+CHAIN_KEY_SEED = bytes([0x02])
 
-class ChainKey:
-    MESSAGE_KEY_SEED = bytearray([0x01])
-    CHAIN_KEY_SEED = bytearray([0x02])
 
+class ChainKey:
     def __init__(self, kdf: HKDF, key: bytes, index: int) -> None:
-        self.kdf = kdf
-        self.key = key
-        self.index = index
+        self._kdf = kdf
+        self._key = key
+        self._index = index
 
     def get_key(self) -> bytes:
-        return self.key
+        return self._key
 
     def get_index(self) -> int:
-        return self.index
+        return self._index
 
     def get_next_chain_key(self) -> ChainKey:
-        nextKey = self.get_base_material(self.__class__.CHAIN_KEY_SEED)
-        return ChainKey(self.kdf, nextKey, self.index + 1)
+        nextKey = self.get_base_material(CHAIN_KEY_SEED)
+        return ChainKey(self._kdf, nextKey, self._index + 1)
 
     def get_message_keys(self) -> MessageKeys:
-        if self.kdf.session_version <= 3:
+        if self._kdf.get_session_version() <= 3:
             domain_separator = "WhisperMessageKeys"
         else:
             domain_separator = "OMEMO Message Key Material"
 
-        input_key_material = self.get_base_material(self.__class__.MESSAGE_KEY_SEED)
-        key_material_bytes = self.kdf.derive_secrets(
+        input_key_material = self.get_base_material(MESSAGE_KEY_SEED)
+        key_material_bytes = self._kdf.derive_secrets(
             input_key_material,
-            bytearray(domain_separator.encode()),
+            domain_separator.encode(),
             DerivedMessageSecrets.SIZE,
         )
         key_material = DerivedMessageSecrets(key_material_bytes)
         return MessageKeys(
             key_material.get_cipher_key(),
             key_material.get_mac_key(),
             key_material.get_iv(),
-            self.index,
+            self._index,
         )
 
     def get_base_material(self, seedBytes: bytes) -> bytes:
-        mac = hmac.new(bytes(self.key), digestmod=hashlib.sha256)
+        mac = hmac.new(bytes(self._key), digestmod=hashlib.sha256)
         mac.update(bytes(seedBytes))
         return mac.digest()
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ratchet/ratchetingsession.py` & `omemo-dr-0.99.2/src/omemo_dr/ratchet/ratchetingsession.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from __future__ import annotations
 
 from ..ecc.curve import Curve
-from ..ecc.ec import ECPublicKey
+from ..ecc.djbec import CurvePublicKey
 from ..kdf.hkdf import HKDF
 from ..state.sessionstate import SessionState
 from ..util.byteutil import ByteUtil
 from .aliceparameters import AliceParameters
 from .bobparameters import BobParameters
 from .chainkey import ChainKey
 from .rootkey import RootKey
@@ -23,16 +23,15 @@
         session_state.set_local_identity_key(
             parameters.get_our_identity_key().get_public_key()
         )
 
         sending_ratchet_key = Curve.generate_key_pair()
         secrets = bytearray()
 
-        if session_version >= 3:
-            secrets.extend(RatchetingSession.get_discontinuity_bytes())
+        secrets.extend(RatchetingSession.get_discontinuity_bytes())
 
         secrets.extend(
             Curve.calculate_agreement(
                 parameters.get_their_signed_pre_key(),
                 parameters.get_our_identity_key().get_private_key(),
             )
         )
@@ -45,24 +44,23 @@
         secrets.extend(
             Curve.calculate_agreement(
                 parameters.get_their_signed_pre_key(),
                 parameters.get_our_base_key().get_private_key(),
             )
         )
 
-        if session_version >= 3 and parameters.get_their_one_time_pre_key() is not None:
-            secrets.extend(
-                Curve.calculate_agreement(
-                    parameters.get_their_one_time_pre_key(),
-                    parameters.get_our_base_key().get_private_key(),
-                )
+        secrets.extend(
+            Curve.calculate_agreement(
+                parameters.get_their_one_time_pre_key(),
+                parameters.get_our_base_key().get_private_key(),
             )
+        )
 
         derived_keys = RatchetingSession.calculate_derived_keys(
-            session_version, secrets
+            session_version, bytes(secrets)
         )
         sending_chain = derived_keys.get_root_key().create_chain(
             parameters.get_their_ratchet_key(), sending_ratchet_key
         )
 
         session_state.add_receiver_chain(
             parameters.get_their_ratchet_key(), derived_keys.get_chain_key()
@@ -80,16 +78,15 @@
         session_state.set_remote_identity_key(parameters.get_their_identity_key())
         session_state.set_local_identity_key(
             parameters.get_our_identity_key().get_public_key()
         )
 
         secrets = bytearray()
 
-        if session_version >= 3:
-            secrets.extend(RatchetingSession.get_discontinuity_bytes())
+        secrets.extend(RatchetingSession.get_discontinuity_bytes())
 
         secrets.extend(
             Curve.calculate_agreement(
                 parameters.get_their_identity_key().get_public_key(),
                 parameters.get_our_signed_pre_key().get_private_key(),
             )
         )
@@ -104,24 +101,23 @@
             Curve.calculate_agreement(
                 parameters.get_their_base_key(),
                 parameters.get_our_signed_pre_key().get_private_key(),
             )
         )
 
         our_one_time_pre_key = parameters.get_our_one_time_pre_key()
-        if session_version >= 3 and our_one_time_pre_key is not None:
-            secrets.extend(
-                Curve.calculate_agreement(
-                    parameters.get_their_base_key(),
-                    our_one_time_pre_key.get_private_key(),
-                )
+        secrets.extend(
+            Curve.calculate_agreement(
+                parameters.get_their_base_key(),
+                our_one_time_pre_key.get_private_key(),
             )
+        )
 
         derived_keys = RatchetingSession.calculate_derived_keys(
-            session_version, secrets
+            session_version, bytes(secrets)
         )
         session_state.set_sender_chain(
             parameters.get_our_ratchet_key(), derived_keys.get_chain_key()
         )
         session_state.set_root_key(derived_keys.get_root_key())
 
     @staticmethod
@@ -134,23 +130,23 @@
     ) -> DerivedKeys:
         if session_version <= 3:
             domain_separator = "WhisperText"
         else:
             domain_separator = "OMEMO Payload"
         kdf = HKDF(session_version)
         derived_secret_bytes = kdf.derive_secrets(
-            master_secret, bytearray(domain_separator.encode()), 64
+            master_secret, domain_separator.encode(), 64
         )
         derived_secrets = ByteUtil.split(derived_secret_bytes, 32, 32)
         return RatchetingSession.DerivedKeys(
             RootKey(kdf, derived_secrets[0]), ChainKey(kdf, derived_secrets[1], 0)
         )
 
     @staticmethod
-    def is_alice(our_key: ECPublicKey, their_key: ECPublicKey) -> bool:
+    def is_alice(our_key: CurvePublicKey, their_key: CurvePublicKey) -> bool:
         return our_key < their_key
 
     class DerivedKeys:
         def __init__(self, root_key: RootKey, chain_key: ChainKey):
             self._root_key = root_key
             self._chain_key = chain_key
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/ratchet/rootkey.py` & `omemo-dr-0.99.2/src/omemo_dr/ratchet/rootkey.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,39 +6,39 @@
 from ..kdf.derivedrootsecrets import DerivedRootSecrets
 from ..kdf.hkdf import HKDF
 from .chainkey import ChainKey
 
 
 class RootKey:
     def __init__(self, kdf: HKDF, key: bytes) -> None:
-        self.kdf = kdf
-        self.key = key
+        self._kdf = kdf
+        self._key = key
 
     def get_key_bytes(self) -> bytes:
-        return self.key
+        return self._key
 
     def create_chain(
         self,
         ec_public_key_their_ratchet_key: CurvePublicKey,
         ec_key_pair_our_ratchet_key: ECKeyPair,
     ) -> tuple[RootKey, ChainKey]:
-        if self.kdf.session_version <= 3:
+        if self._kdf.get_session_version() <= 3:
             domain_separator = "WhisperRatchet"
         else:
             domain_separator = "OMEMO Root Chain"
 
         shared_secret = Curve.calculate_agreement(
             ec_public_key_their_ratchet_key,
             ec_key_pair_our_ratchet_key.get_private_key(),
         )
 
-        derived_secret_bytes = self.kdf.derive_secrets(
+        derived_secret_bytes = self._kdf.derive_secrets(
             shared_secret,
             domain_separator.encode(),
             DerivedRootSecrets.SIZE,
-            salt=self.key,
+            salt=self._key,
         )
 
         derived_secrets = DerivedRootSecrets(derived_secret_bytes)
-        new_root_key = RootKey(self.kdf, derived_secrets.get_root_key())
-        new_chain_key = ChainKey(self.kdf, derived_secrets.get_chain_key(), 0)
+        new_root_key = RootKey(self._kdf, derived_secrets.get_root_key())
+        new_chain_key = ChainKey(self._kdf, derived_secrets.get_chain_key(), 0)
         return (new_root_key, new_chain_key)
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/session.py` & `omemo-dr-0.99.2/src/omemo_dr/session_manager.py`

 * *Files 11% similar despite different names*

```diff
@@ -8,111 +8,118 @@
 from collections import defaultdict
 
 from . import exceptions
 from .aes import aes_decrypt
 from .aes import aes_encrypt
 from .aes import get_new_iv
 from .aes import get_new_key
+from .const import NS_OMEMO_TMP
 from .const import OMEMOTrust
-from .ecc.djbec import CurvePublicKey
 from .identitykey import IdentityKey
 from .identitykeypair import IdentityKeyPair
 from .observable import Observable
 from .protocol.prekeywhispermessage import PreKeyWhisperMessage
 from .protocol.whispermessage import WhisperMessage
 from .sessionbuilder import SessionBuilder
 from .sessioncipher import SessionCipher
 from .state.prekeybundle import PreKeyBundle
 from .state.store import Store
+from .structs import IdentityInfo
 from .structs import OMEMOBundle
+from .structs import OMEMOBundleProto
 from .structs import OMEMOConfig
 from .structs import OMEMOMessage
+from .structs import OMEMOMessageProto
 from .util.keyhelper import KeyHelper
+from .util.logging import SessionContextAdapter
 
 log = logging.getLogger(__name__)
 
 
-class OMEMOSession(Observable):
-    def __init__(self, own_address: str, storage: Store, config: OMEMOConfig) -> None:
-        Observable.__init__(self, log)
+class OMEMOSessionManager(Observable):
+    def __init__(
+        self,
+        our_address: str,
+        storage: Store,
+        config: OMEMOConfig,
+        log_context: str | None = None,
+    ) -> None:
+        Observable.__init__(self)
+        self._log = SessionContextAdapter(log, {"context": log_context})
+
         self._device_store: dict[str, set[int]] = defaultdict(set)
         self._group_member_store: dict[str, set[str]] = defaultdict(set)
         self._session_ciphers: dict[str, dict[int, SessionCipher]] = defaultdict(dict)
 
-        self._own_address = own_address
+        self._our_address = our_address
         self._storage = storage
         self._config = config
 
         if self._storage.needs_init():
-            logging.info("Generating OMEMO keys")
-            self._own_device_id = self._generate_keys()
+            self._log.info("Generating OMEMO keys")
+            self._our_device_id = self._generate_keys()
         else:
-            self._own_device_id = self._storage.get_local_registration_id()
+            self._our_device_id = self._storage.get_our_device_id()
 
-        self.add_device(self._own_address, self._own_device_id)
-        logging.info("Our device id: %s", self._own_device_id)
+        self.add_device(self._our_address, self._our_device_id)
+        self._log.info("Our device id: %s", self._our_device_id)
 
-        logging.info("%s PreKeys available", self._storage.get_pre_key_count())
+        self._log.info("%s PreKeys available", self._storage.get_pre_key_count())
 
         for address, device in self._storage.get_active_device_tuples():
-            logging.info("Load device from storage: %s - %s", address, device)
+            self._log.info("Load device from storage: %s - %s", address, device)
             self.add_device(address, device)
 
     def _generate_keys(self) -> int:
         identity_key_pair = KeyHelper.generate_identity_key_pair()
-        own_device_id = KeyHelper.get_random_sequence(2147483647)
-        self._storage.store_own_identity(own_device_id, identity_key_pair)
+        our_device_id = KeyHelper.get_random_sequence(2147483647)
+        self._storage.set_our_identity(our_device_id, identity_key_pair)
 
         signed_pre_key = KeyHelper.generate_signed_pre_key(
             identity_key_pair, KeyHelper.get_random_sequence(65536)
         )
         self._storage.store_signed_pre_key(signed_pre_key.get_id(), signed_pre_key)
 
         self._generate_pre_keys(self._config.default_prekey_amount)
 
-        return own_device_id
+        return our_device_id
 
     def _generate_pre_keys(self, count: int) -> None:
         prekey_id = self._storage.get_current_pre_key_id() or 0
         pre_keys = KeyHelper.generate_pre_keys(prekey_id + 1, count)
         for pre_key in pre_keys:
             self._storage.store_pre_key(pre_key.get_id(), pre_key)
 
-    def build_session(self, address: str, device_id: int, bundle: OMEMOBundle) -> None:
-        session = SessionBuilder(self._storage, address, device_id)
+    def build_session(self, address: str, bundle: OMEMOBundleProto) -> None:
+        session = SessionBuilder(self._storage, address, bundle.device_id)
+        prekey_bundle = PreKeyBundle.from_proto(bundle)
 
-        prekey = bundle.pick_prekey()
-        otpk = CurvePublicKey(prekey["key"][1:])
+        session.process_pre_key_bundle(prekey_bundle)
 
-        spk = CurvePublicKey(bundle.spk["key"][1:])
-        ik = IdentityKey(CurvePublicKey(bundle.ik[1:]))
+    def delete_session(
+        self, address: str, device_id: int, *, delete_identity: bool
+    ) -> None:
+        if delete_identity:
+            record = self._storage.load_session(address, device_id)
+            identity_key = record.get_session_state().get_remote_identity_key()
+            self._storage.delete_identity(address, identity_key)
+            self.remove_device(address, device_id)
 
-        prekey_bundle = PreKeyBundle(
-            self._own_device_id,
-            device_id,
-            prekey["id"],
-            otpk,
-            bundle.spk["id"],
-            spk,
-            bundle.spk_signature,
-            ik,
-        )
-
-        session.process_pre_key_bundle(prekey_bundle)
-        self._get_session_cipher(address, device_id)
+        self._storage.delete_session(address, device_id)
 
-    @property
-    def storage(self) -> Any:
-        return self._storage
+    def get_our_identity(self) -> tuple[int, IdentityKey]:
+        our_device_id = self._storage.get_our_device_id()
+        identity_key = self._storage.get_identity_key_pair().get_public_key()
+        return our_device_id, identity_key
 
-    def get_own_fingerprint(self, *, formatted: bool = False) -> str:
+    def get_our_fingerprint(self, *, formatted: bool = False) -> str:
         identity_key = self._storage.get_identity_key_pair().get_public_key()
         return identity_key.get_fingerprint(formatted=formatted)
 
-    def get_bundle(self) -> OMEMOBundle:
+    def get_bundle(self, namespace: str) -> OMEMOBundle:
         self._check_pre_key_count()
 
         bundle: dict[str, Any] = {"otpks": []}
         for k in self._storage.load_pending_pre_keys():
             key = k.get_key_pair().get_public_key().serialize()
             bundle["otpks"].append({"key": key, "id": k.get_id()})
 
@@ -126,114 +133,116 @@
         )
         bundle["spk_signature"] = spk.get_signature()
         bundle["spk"] = {
             "key": spk.get_key_pair().get_public_key().serialize(),
             "id": spk.get_id(),
         }
 
-        return OMEMOBundle(**bundle)
+        device_id = self.get_our_device()
+
+        return OMEMOBundle(**bundle, device_id=device_id, namespace=namespace)
 
     def decrypt_message(
-        self, omemo_message: OMEMOMessage, address: str
+        self, omemo_message: OMEMOMessageProto, address: str
     ) -> tuple[str, str, OMEMOTrust]:
-        if omemo_message.sid == self.get_own_device():
-            logging.info("Received previously sent message by us")
+        if omemo_message.sid == self.get_our_device():
+            self._log.info("Received previously sent message by us")
             raise exceptions.SelfMessage
 
         try:
-            encrypted_key, prekey = omemo_message.keys[self.get_own_device()]
+            encrypted_key, prekey = omemo_message.keys[self.get_our_device()]
         except KeyError:
-            logging.info("Received message not for our device")
+            self._log.info("Received message not for our device")
             raise exceptions.MessageNotForDevice
 
         try:
             if prekey:
                 key, fingerprint, trust = self._process_pre_key_message(
                     address, omemo_message.sid, encrypted_key
                 )
             else:
                 key, fingerprint, trust = self._process_message(
                     address, omemo_message.sid, encrypted_key
                 )
 
         except exceptions.DuplicateMessageException:
-            logging.info("Received duplicated message")
+            self._log.info("Received duplicated message")
             raise exceptions.DuplicateMessage
 
         except Exception as error:
-            logging.warning(error)
+            self._log.warning(error)
             raise exceptions.DecryptionFailed
 
         if omemo_message.payload is None:
-            logging.debug("Decrypted Key Exchange Message")
+            self._log.debug("Decrypted Key Exchange Message")
             raise exceptions.KeyExchangeMessage
 
         try:
             result = aes_decrypt(key, omemo_message.iv, omemo_message.payload)
         except Exception as error:
-            logging.warning(error)
+            self._log.warning(error)
             raise exceptions.DecryptionFailed
 
-        logging.debug("Decrypted Message => %s", result)
+        self._log.debug("Decrypted Message => %s", result)
         return result, fingerprint, trust
 
     def _get_whisper_message(
         self, address: str, device: int, key: bytes
     ) -> tuple[bytes, bool]:
-        cipher = self._get_session_cipher(address, device)
-        cipher_key = cipher.encrypt(key)
+        session_cipher = SessionCipher(self._storage, address, device)
+        cipher_key = session_cipher.encrypt(key)
         prekey = isinstance(cipher_key, PreKeyWhisperMessage)
         return cipher_key.serialize(), prekey
 
     def encrypt(
         self, address: str, plaintext: str, *, groupchat: bool
     ) -> Optional[OMEMOMessage]:
         try:
-            devices_for_encryption = self.get_devices_for_enc(
+            devices_for_encryption = self._get_devices_for_enc(
                 address, groupchat=groupchat
             )
         except exceptions.NoDevicesFound:
-            logging.warning("No devices for encryption found for: %s", address)
+            self._log.warning("No devices for encryption found for: %s", address)
             return
 
         result = aes_encrypt(plaintext)
         whisper_messages: dict[str, dict[int, tuple[bytes, bool]]] = defaultdict(dict)
 
         for address_, device in devices_for_encryption:
             count = self._storage.get_unacknowledged_count(address_, device)
             if count >= self._config.unacknowledged_count:
-                logging.warning(
+                self._log.warning(
                     "Set device inactive %s because of %s unacknowledged messages",
                     device,
                     count,
                 )
                 self.remove_device(address_, device)
 
             try:
                 whisper_messages[address_][device] = self._get_whisper_message(
                     address_, device, result.key
                 )
             except Exception:
-                logging.exception("Failed to encrypt")
+                self._log.exception("Failed to encrypt")
                 continue
 
         recipients = set(whisper_messages.keys())
-        if address != self._own_address:
-            recipients -= {self._own_address}
+        if address != self._our_address:
+            recipients -= {self._our_address}
         if not recipients:
-            logging.error("Encrypted keys empty")
+            self._log.error("Encrypted keys empty")
             return
 
         encrypted_keys: dict[int, tuple[bytes, bool]] = {}
         for address_ in whisper_messages:
             encrypted_keys.update(whisper_messages[address_])
 
-        logging.debug("Finished encrypting message")
+        self._log.debug("Finished encrypting message")
         return OMEMOMessage(
-            sid=self.get_own_device(),
+            sid=self.get_our_device(),
             keys=encrypted_keys,
             iv=result.iv,
             payload=result.payload,
         )
 
     def encrypt_key_transport(
         self, address: str, devices: list[int]
@@ -241,85 +250,100 @@
         whisper_messages: dict[str, dict[int, tuple[bytes, bool]]] = defaultdict(dict)
         for device in devices:
             try:
                 whisper_messages[address][device] = self._get_whisper_message(
                     address, device, get_new_key()
                 )
             except Exception:
-                logging.exception("Failed to encrypt")
+                self._log.exception("Failed to encrypt")
                 continue
 
         if not whisper_messages[address]:
-            logging.error("Encrypted keys empty")
+            self._log.error("Encrypted keys empty")
             return
 
-        logging.debug("Finished Key Transport message")
+        self._log.debug("Finished Key Transport message")
         return OMEMOMessage(
-            sid=self.get_own_device(),
+            sid=self.get_our_device(),
             keys=whisper_messages[address],
             iv=get_new_iv(),
             payload=None,
         )
 
-    def has_trusted_keys(self, address: str) -> bool:
-        inactive = self._storage.get_inactive_sessions_keys(address)
-        trusted = self._storage.get_trusted_fingerprints(address)
-        return bool(set(trusted) - set(inactive))
+    def set_trust(
+        self, address: str, identity_key: IdentityKey, trust: OMEMOTrust
+    ) -> None:
+        self._storage.set_trust(address, identity_key, trust)
+
+    def get_identity_infos(
+        self,
+        address: str,
+        *,
+        only_active: bool = False,
+        trust: list[OMEMOTrust] | OMEMOTrust | None = None,
+    ) -> list[IdentityInfo]:
+        if self._is_group_address(address):
+            members = list(self.get_group_members(address))
+            identity_infos = self._storage.get_identity_infos(members)
+        else:
+            identity_infos = self._storage.get_identity_infos(address)
+
+        if only_active:
+            identity_infos = list(filter(lambda info: info.active, identity_infos))
+
+        if trust is not None:
+            if not isinstance(trust, list):
+                trust = [trust]
+            identity_infos = list(
+                filter(lambda info: info.trust in trust, identity_infos)
+            )
+
+        return identity_infos
 
     def get_devices_without_sessions(self, address: str) -> list[int]:
         known_devices = self.get_devices(address, without_self=True)
         missing_devices = [
             dev
             for dev in known_devices
             if not self._storage.contains_session(address, dev)
         ]
         if missing_devices:
-            logging.info("Missing device sessions for %s: %s", address, missing_devices)
-        return missing_devices
-
-    def _get_session_cipher(self, address: str, device_id: int) -> SessionCipher:
-        try:
-            return self._session_ciphers[address][device_id]
-        except KeyError:
-            cipher = SessionCipher(
-                self._storage,
-                address,
-                device_id,
+            self._log.info(
+                "Missing device sessions for %s: %s", address, missing_devices
             )
-            self._session_ciphers[address][device_id] = cipher
-            return cipher
+        return missing_devices
 
     def _process_pre_key_message(
         self, address: str, device: int, key: bytes
     ) -> tuple[bytes, str, OMEMOTrust]:
-        logging.info("Process pre key message from %s", address)
+        self._log.info("Process pre key message from %s", address)
         pre_key_message = PreKeyWhisperMessage.from_bytes(key)
         if not pre_key_message.get_pre_key_id():
             raise Exception("Received Pre Key Message without PreKey => %s" % address)
 
-        session_cipher = self._get_session_cipher(address, device)
+        session_cipher = SessionCipher(self._storage, address, device)
         key = session_cipher.decrypt_pkmsg(pre_key_message)
 
         identity_key = pre_key_message.get_identity_key()
         trust = self._get_trust_from_identity_key(address, identity_key)
         fingerprint = identity_key.get_fingerprint()
 
         self._storage.set_identity_last_seen(address, identity_key)
 
         self.add_device(address, device)
-        self._notify("republish-bundle", self.get_bundle())
+        self._notify("republish-bundle", self.get_bundle(NS_OMEMO_TMP))
         return key, fingerprint, trust
 
     def _process_message(
         self, address: str, device: int, key: bytes
     ) -> tuple[bytes, str, OMEMOTrust]:
-        logging.info("Process message from %s", address)
+        self._log.info("Process message from %s", address)
         message = WhisperMessage.from_bytes(key)
 
-        session_cipher = self._get_session_cipher(address, device)
+        session_cipher = SessionCipher(self._storage, address, device)
         key = session_cipher.decrypt_msg(message)
 
         identity_key = self._get_identity_key_from_device(address, device)
         assert identity_key is not None
         trust = self._get_trust_from_identity_key(address, identity_key)
         fingerprint = identity_key.get_fingerprint()
 
@@ -343,15 +367,15 @@
 
     def _check_pre_key_count(self) -> None:
         # Check if enough PreKeys are available
         pre_key_count = self._storage.get_pre_key_count()
         if pre_key_count < self._config.min_prekey_amount:
             missing_count = self._config.default_prekey_amount - pre_key_count
             self._generate_pre_keys(missing_count)
-            logging.info("%s PreKeys created", missing_count)
+            self._log.info("%s PreKeys created", missing_count)
 
     def _cycle_signed_pre_key(self, ik_pair: IdentityKeyPair) -> None:
         # Publish every spk_cycle_seconds a new SignedPreKey
         # Delete all existing SignedPreKeys that are older
         # then spk_archive_seconds
 
         # if spk_cycle_seconds is reached, generate a new SignedPreKey
@@ -361,107 +385,110 @@
         )
 
         if int(timestamp) < now - self._config.spk_cycle_seconds:
             spk = KeyHelper.generate_signed_pre_key(
                 ik_pair, self._storage.get_next_signed_pre_key_id()
             )
             self._storage.store_signed_pre_key(spk.get_id(), spk)
-            logging.debug("Cycled SignedPreKey")
+            self._log.debug("Cycled SignedPreKey")
 
         # Delete all SignedPreKeys that are older than spk_archive_seconds
         timestamp = now - self._config.spk_archive_seconds
         self._storage.remove_old_signed_pre_keys(timestamp)
 
     def update_devicelist(self, address: str, devicelist: list[int]) -> None:
         for device in list(devicelist):
-            if device == self.get_own_device():
+            if device == self.get_our_device():
                 continue
             count = self._storage.get_unacknowledged_count(address, device)
             if count > self._config.unacknowledged_count:
-                logging.warning(
+                self._log.warning(
                     "Ignore device because of %s unacknowledged messages: %s %s",
                     count,
                     address,
                     device,
                 )
                 devicelist.remove(device)
 
         self._device_store[address] = set(devicelist)
-        logging.info("Saved devices for %s", address)
+        self._log.info("Saved devices for %s", address)
         self._storage.set_active_state(address, devicelist)
 
+    def _is_group_address(self, address: str) -> bool:
+        return address in self._group_member_store
+
     def add_group_member(self, group_address: str, address: str) -> None:
-        logging.info("Saved group member %s %s", group_address, address)
+        self._log.info("Saved group member %s %s", group_address, address)
         self._group_member_store[group_address].add(address)
 
     def remove_group_member(self, group_address: str, address: str) -> None:
-        logging.info("Removed group member %s %s", group_address, address)
+        self._log.info("Removed group member %s %s", group_address, address)
         self._group_member_store[group_address].discard(address)
 
     def get_group_members(
         self, group_address: str, without_self: bool = True
     ) -> set[str]:
         members = set(self._group_member_store[group_address])
         if without_self:
-            members.discard(self._own_address)
+            members.discard(self._our_address)
         return members
 
     def add_device(self, address: str, device: int) -> None:
         self._device_store[address].add(device)
 
     def remove_device(self, address: str, device: int) -> None:
         self._device_store[address].discard(device)
         self._storage.set_inactive(address, device)
 
     def get_devices(self, address: str, without_self: bool = False) -> set[int]:
         devices = set(self._device_store[address])
         if without_self:
-            devices.discard(self.get_own_device())
+            devices.discard(self.get_our_device())
         return devices
 
-    def get_devices_for_enc(
+    def _get_devices_for_enc(
         self, address: str, *, groupchat: bool
     ) -> set[tuple[str, int]]:
         devices_for_encryption: list[tuple[str, int]] = []
 
         if groupchat:
             devices_for_encryption = self._get_devices_for_group_encryption(address)
         else:
             devices_for_encryption = self._get_devices_for_encryption(address)
 
         if not devices_for_encryption:
             raise exceptions.NoDevicesFound
 
-        devices_for_encryption += self._get_own_devices_for_encryption()
+        devices_for_encryption += self._get_our_devices_for_encryption()
         return set(devices_for_encryption)
 
     def _get_devices_for_group_encryption(self, address: str) -> list[tuple[str, int]]:
         devices_for_encryption: list[tuple[str, int]] = []
         for address_ in self._group_member_store[address]:
             devices_for_encryption += self._get_devices_for_encryption(address_)
         return devices_for_encryption
 
-    def _get_own_devices_for_encryption(self) -> list[tuple[str, int]]:
+    def _get_our_devices_for_encryption(self) -> list[tuple[str, int]]:
         devices_for_encryption: list[tuple[str, int]] = []
-        own_devices = self.get_devices(self._own_address, without_self=True)
-        for device in own_devices:
-            if self._storage.is_trusted(self._own_address, device):
-                devices_for_encryption.append((self._own_address, device))
+        our_devices = self.get_devices(self._our_address, without_self=True)
+        for device in our_devices:
+            if self._storage.is_trusted(self._our_address, device):
+                devices_for_encryption.append((self._our_address, device))
         return devices_for_encryption
 
     def _get_devices_for_encryption(self, address: str) -> list[tuple[str, int]]:
         devices_for_encryption: list[tuple[str, int]] = []
         devices = self.get_devices(address)
 
         for device in devices:
             if self._storage.is_trusted(address, device):
                 devices_for_encryption.append((address, device))
         return devices_for_encryption
 
-    def get_own_device(self) -> int:
-        return self._own_device_id
+    def get_our_device(self) -> int:
+        return self._our_device_id
 
-    def is_own_device_published(self) -> bool:
-        return self.get_own_device() in self.get_devices(self._own_address)
+    def is_our_device_published(self) -> bool:
+        return self.get_our_device() in self.get_devices(self._our_address)
 
     def destroy(self) -> None:
         self._unregister_signals()
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/sessionbuilder.py` & `omemo-dr-0.99.2/src/omemo_dr/sessionbuilder.py`

 * *Files 17% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 from .ratchet.aliceparameters import AliceParameters
 from .ratchet.bobparameters import BobParameters
 from .ratchet.ratchetingsession import RatchetingSession
 from .state.prekeybundle import PreKeyBundle
 from .state.sessionrecord import SessionRecord
 from .state.store import Store
 
-logger = logging.getLogger(__name__)
+log = logging.getLogger(__name__)
 
 
 class SessionBuilder:
     def __init__(
         self,
         store: Store,
         recipient_id: str,
@@ -51,15 +51,15 @@
 
     def process_message(
         self, session_record: SessionRecord, message: PreKeyWhisperMessage
     ) -> Optional[int]:
         if session_record.has_session_state(
             message.get_message_version(), message.get_base_key().serialize()
         ):
-            logger.warn(
+            log.warning(
                 "We've already setupgetMessageVersion a "
                 "session for this V3 message, letting bundled "
                 "message fall through..."
             )
             return None
 
         our_signed_pre_key = self._store.load_signed_pre_key(
@@ -83,74 +83,72 @@
             session_record.archive_current_state()
 
         RatchetingSession.initialize_session_as_bob(
             session_record.get_session_state(),
             message.get_message_version(),
             parameters,
         )
-        session_record.get_session_state().set_local_registration_id(
-            self._store.get_local_registration_id()
-        )
-        session_record.get_session_state().set_remote_registration_id(
-            message.get_registration_id()
+        session_record.get_session_state().set_our_device_id(
+            self._store.get_our_device_id()
         )
+        session_record.get_session_state().set_remote_device_id(message.get_device_id())
         session_record.get_session_state().set_alice_base_key(
             message.get_base_key().serialize()
         )
 
         return message.get_pre_key_id()
 
-    def process_pre_key_bundle(self, pre_key: PreKeyBundle) -> None:
+    def process_pre_key_bundle(self, bundle: PreKeyBundle) -> None:
         if not self._store.is_trusted_identity(
-            self._recipient_id, pre_key.get_identity_key()
+            self._recipient_id, bundle.get_identity_key()
         ):
             raise UntrustedIdentityException(
-                self._recipient_id, pre_key.get_identity_key()
+                self._recipient_id, bundle.get_identity_key()
             )
 
         if not Curve.verify_signature(
-            pre_key.get_identity_key().get_public_key(),
-            pre_key.get_signed_pre_key().serialize(),
-            pre_key.get_signed_pre_key_signature(),
+            bundle.get_identity_key().get_public_key(),
+            bundle.get_signed_pre_key().serialize(),
+            bundle.get_signed_pre_key_signature(),
         ):
             raise InvalidKeyException("Invalid signature on device key!")
 
         session_record = self._store.load_session(self._recipient_id, self._device_id)
         our_base_key = Curve.generate_key_pair()
-        their_signed_pre_key = pre_key.get_signed_pre_key()
-        their_one_time_pre_key = pre_key.get_pre_key()
-        their_one_time_pre_key_id = pre_key.get_pre_key_id()
+        their_signed_pre_key = bundle.get_signed_pre_key()
+        their_one_time_pre_key = bundle.get_pre_key()
+        their_one_time_pre_key_id = bundle.get_pre_key_id()
 
         parameters = AliceParameters(
             self._store.get_identity_key_pair(),
             our_base_key,
-            pre_key.get_identity_key(),
+            bundle.get_identity_key(),
             their_signed_pre_key,
             their_signed_pre_key,
             their_one_time_pre_key,
         )
 
         if not session_record.is_fresh():
             session_record.archive_current_state()
 
         RatchetingSession.initialize_session_as_alice(
             session_record.get_session_state(),
-            pre_key.get_session_version(),
+            bundle.get_session_version(),
             parameters,
         )
 
         session_record.get_session_state().set_unacknowledged_pre_key_message(
             their_one_time_pre_key_id,
-            pre_key.get_signed_pre_key_id(),
+            bundle.get_signed_pre_key_id(),
             our_base_key.get_public_key(),
         )
-        session_record.get_session_state().set_local_registration_id(
-            self._store.get_local_registration_id()
+        session_record.get_session_state().set_our_device_id(
+            self._store.get_our_device_id()
         )
-        session_record.get_session_state().set_remote_registration_id(
-            pre_key.get_registration_id()
+        session_record.get_session_state().set_remote_device_id(
+            bundle.get_remote_device_id()
         )
         session_record.get_session_state().set_alice_base_key(
             our_base_key.get_public_key().serialize()
         )
         self._store.store_session(self._recipient_id, self._device_id, session_record)
-        self._store.save_identity(self._recipient_id, pre_key.get_identity_key())
+        self._store.save_identity(self._recipient_id, bundle.get_identity_key())
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/sessioncipher.py` & `omemo-dr-0.99.2/src/omemo_dr/sessioncipher.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,11 @@
 from __future__ import annotations
 
 from typing import Union
 
-import logging
-
 from cryptography.hazmat.backends import default_backend
 from cryptography.hazmat.primitives.ciphers import algorithms
 from cryptography.hazmat.primitives.ciphers import Cipher
 from cryptography.hazmat.primitives.ciphers import modes
 
 from .ecc.curve import Curve
 from .ecc.djbec import CurvePublicKey
@@ -19,37 +17,33 @@
 from .protocol.whispermessage import WhisperMessage
 from .ratchet.chainkey import ChainKey
 from .sessionbuilder import SessionBuilder
 from .state.sessionrecord import SessionRecord
 from .state.sessionstate import SessionState
 from .state.store import Store
 
-logger = logging.getLogger(__name__)
-
 
 class SessionCipher:
     def __init__(self, store: Store, recipient_id: str, device_id: int) -> None:
         self._store = store
-        self.recipient_id = recipient_id
-        self.device_id = device_id
-        self.session_builder = SessionBuilder(
+        self._recipient_id = recipient_id
+        self._device_id = device_id
+        self._session_builder = SessionBuilder(
             store,
             recipient_id,
             device_id,
         )
 
     def encrypt(
         self, padded_message: Union[bytes, str]
     ) -> Union[WhisperMessage, PreKeyWhisperMessage]:
         if isinstance(padded_message, str):
             padded_message = padded_message.encode()
 
-        padded_message = bytearray(padded_message)
-
-        session_record = self._store.load_session(self.recipient_id, self.device_id)
+        session_record = self._store.load_session(self._recipient_id, self._device_id)
         session_state = session_record.get_session_state()
         chain_key = session_state.get_sender_chain_key()
         message_keys = chain_key.get_message_keys()
         sender_ephemeral = session_state.get_sender_ratchet_key()
         previous_counter = session_state.get_previous_counter()
         session_version = session_state.get_session_version()
 
@@ -66,52 +60,52 @@
             ciphertext_body,
             session_state.get_local_identity_key(),
             session_state.get_remote_identity_key(),
         )
 
         if session_state.has_unacknowledged_pre_key_message():
             items = session_state.get_unacknowledged_pre_key_message_items()
-            local_registrationid = session_state.get_local_registration_id()
+            our_device_id = session_state.get_our_device_id()
 
             ciphertext_message = PreKeyWhisperMessage.new(
                 session_version,
-                local_registrationid,
+                our_device_id,
                 items.get_pre_key_id(),
                 items.get_signed_pre_key_id(),
                 items.get_base_key(),
                 session_state.get_local_identity_key(),
                 ciphertext_message,
             )
 
         session_state.set_sender_chain_key(chain_key.get_next_chain_key())
-        self._store.store_session(self.recipient_id, self.device_id, session_record)
+        self._store.store_session(self._recipient_id, self._device_id, session_record)
 
         return ciphertext_message
 
     def decrypt_msg(self, ciphertext: WhisperMessage) -> bytes:
-        if not self._store.contains_session(self.recipient_id, self.device_id):
+        if not self._store.contains_session(self._recipient_id, self._device_id):
             raise NoSessionException(
-                "No session for: %s, %s" % (self.recipient_id, self.device_id)
+                "No session for: %s, %s" % (self._recipient_id, self._device_id)
             )
 
-        session_record = self._store.load_session(self.recipient_id, self.device_id)
+        session_record = self._store.load_session(self._recipient_id, self._device_id)
         plaintext = self.decrypt_with_session_record(session_record, ciphertext)
 
-        self._store.store_session(self.recipient_id, self.device_id, session_record)
+        self._store.store_session(self._recipient_id, self._device_id, session_record)
 
         return plaintext
 
     def decrypt_pkmsg(self, ciphertext: PreKeyWhisperMessage) -> bytes:
-        session_record = self._store.load_session(self.recipient_id, self.device_id)
-        unsigned_pre_key_id = self.session_builder.process(session_record, ciphertext)
+        session_record = self._store.load_session(self._recipient_id, self._device_id)
+        unsigned_pre_key_id = self._session_builder.process(session_record, ciphertext)
         plaintext = self.decrypt_with_session_record(
             session_record, ciphertext.get_whisper_message()
         )
 
-        self._store.store_session(self.recipient_id, self.device_id, session_record)
+        self._store.store_session(self._recipient_id, self._device_id, session_record)
 
         if unsigned_pre_key_id is not None:
             self._store.remove_pre_key(unsigned_pre_key_id)
 
         return plaintext
 
     def decrypt_with_session_record(
@@ -228,31 +222,31 @@
 
         session_state.set_receiver_chain_key(
             their_ephemeral, chain_key.get_next_chain_key()
         )
         return chain_key.get_message_keys()
 
     def get_ciphertext(
-        self, version: int, message_keys: MessageKeys, plain_text: bytearray
+        self, version: int, message_keys: MessageKeys, plain_text: bytes
     ) -> bytes:
         cipher = AESCipher(message_keys.get_cipher_key(), message_keys.get_iv())
-        return cipher.encrypt(bytes(plain_text))
+        return cipher.encrypt(plain_text)
 
     def get_plaintext(
         self, version: int, message_keys: MessageKeys, cipher_text: bytes
     ) -> bytes:
         cipher = AESCipher(message_keys.get_cipher_key(), message_keys.get_iv())
         return cipher.decrypt(cipher_text)
 
 
 class AESCipher:
     def __init__(self, key: bytes, iv: bytes) -> None:
-        self.key = key
-        self.iv = iv
-        self.cipher = Cipher(
+        self._key = key
+        self._iv = iv
+        self._cipher = Cipher(
             algorithms.AES(key), modes.CBC(iv), backend=default_backend()
         )
 
     def unpad(self, data: bytes) -> bytes:
         unpad_length = data[-1]
         if isinstance(unpad_length, int):  # pyright: ignore
             cmp = bytes([data[-unpad_length]] * unpad_length)
@@ -266,16 +260,16 @@
         return data[0:-unpad_length]
 
     def pad(self, s: bytes) -> bytes:
         return s + ((16 - len(s) % 16) * chr(16 - len(s) % 16)).encode()
 
     def encrypt(self, raw: bytes) -> bytes:
         raw_padded = self.pad(raw)
-        encryptor = self.cipher.encryptor()
+        encryptor = self._cipher.encryptor()
         try:
             return encryptor.update(raw_padded) + encryptor.finalize()
         except ValueError:
             raise
 
     def decrypt(self, enc: bytes) -> bytes:
-        decryptor = self.cipher.decryptor()
+        decryptor = self._cipher.decryptor()
         return self.unpad(decryptor.update(enc) + decryptor.finalize())
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/state/prekeybundle.py` & `omemo-dr-0.99.2/src/omemo_dr/state/prekeybundle.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,64 +1,92 @@
 from __future__ import annotations
 
+from ..const import NS_OMEMO_2
+from ..const import NS_OMEMO_TMP
 from ..ecc.djbec import CurvePublicKey
 from ..ecc.djbec import EdPublicKey
-from ..ecc.ec import ECPublicKey
+from ..exceptions import InvalidKeyException
 from ..identitykey import IdentityKey
+from ..structs import OMEMOBundleProto
 
 
 class PreKeyBundle:
     def __init__(
         self,
-        registration_id: int,
-        device_id: int,
+        remote_device_id: int,
+        namespace: str,
         pre_key_id: int,
-        ec_public_key_pre_key_public: ECPublicKey,
+        ec_public_key_pre_key_public: CurvePublicKey,
         signed_pre_key_id: int,
-        ec_public_key_signed_pre_key_public: ECPublicKey,
+        ec_public_key_signed_pre_key_public: CurvePublicKey,
         signed_pre_key_signature: bytes,
         identity_key: IdentityKey,
     ) -> None:
-        self.registration_id = registration_id
-        self.device_id = device_id
-        self.pre_key_id = pre_key_id
-        self.pre_key_public = ec_public_key_pre_key_public
-        self.signed_pre_key_id = signed_pre_key_id
-        self.signed_pre_key_public = ec_public_key_signed_pre_key_public
-        self.signed_pre_key_signature = signed_pre_key_signature
-        self.identity_key = identity_key
+        self._remote_device_id = remote_device_id
+        self._namespace = namespace
+        self._pre_key_id = pre_key_id
+        self._pre_key_public = ec_public_key_pre_key_public
+        self._signed_pre_key_id = signed_pre_key_id
+        self._signed_pre_key_public = ec_public_key_signed_pre_key_public
+        self._signed_pre_key_signature = signed_pre_key_signature
+        self._identity_key = identity_key
+
+    @classmethod
+    def from_proto(cls, bundle: OMEMOBundleProto) -> PreKeyBundle:
+        prekey = bundle.pick_prekey()
+        otpk = CurvePublicKey.from_bytes(prekey["key"])
+        spk = CurvePublicKey.from_bytes(bundle.spk["key"])
+
+        ns = bundle.namespace
+        if ns == NS_OMEMO_TMP:
+            ik_pub = CurvePublicKey.from_bytes(bundle.ik)
+        elif ns == NS_OMEMO_2:
+            ik_pub = EdPublicKey.from_bytes(bundle.ik).to_curve()
+        else:
+            raise InvalidKeyException("Unknown namespace on bundle: %s", ns)
+
+        ik = IdentityKey(ik_pub)
+
+        return cls(
+            bundle.device_id,
+            bundle.namespace,
+            prekey["id"],
+            otpk,
+            bundle.spk["id"],
+            spk,
+            bundle.spk_signature,
+            ik,
+        )
 
-    def get_device_id(self) -> int:
-        return self.device_id
+    def get_remote_device_id(self) -> int:
+        return self._remote_device_id
+
+    def get_namespace(self) -> str:
+        return self._namespace
 
     def get_pre_key_id(self) -> int:
-        return self.pre_key_id
+        return self._pre_key_id
 
-    def get_pre_key(self) -> ECPublicKey:
-        return self.pre_key_public
+    def get_pre_key(self) -> CurvePublicKey:
+        return self._pre_key_public
 
     def get_signed_pre_key_id(self) -> int:
-        return self.signed_pre_key_id
+        return self._signed_pre_key_id
 
-    def get_signed_pre_key(self) -> ECPublicKey:
-        return self.signed_pre_key_public
+    def get_signed_pre_key(self) -> CurvePublicKey:
+        return self._signed_pre_key_public
 
     def get_signed_pre_key_signature(self) -> bytes:
-        return self.signed_pre_key_signature
+        return self._signed_pre_key_signature
 
     def get_identity_key(self) -> IdentityKey:
-        return self.identity_key
-
-    def get_registration_id(self) -> int:
-        return self.registration_id
+        return self._identity_key
 
     def get_session_version(self) -> int:
-        public_key = self.identity_key.get_public_key()
-        if isinstance(public_key, CurvePublicKey):
+        if self._namespace == NS_OMEMO_TMP:
             return 3
 
-        elif isinstance(public_key, EdPublicKey):
+        elif self._namespace == NS_OMEMO_2:
             return 4
 
         else:
-            breakpoint()
             raise AssertionError("Unknown session version")
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/state/prekeyrecord.py` & `omemo-dr-0.99.2/src/omemo_dr/state/signedprekeyrecord.py`

 * *Files 13% similar despite different names*

```diff
@@ -2,48 +2,59 @@
 
 from typing import cast
 
 import google.protobuf.message
 
 from ..ecc.curve import Curve
 from ..ecc.eckeypair import ECKeyPair
-from .storageprotos_pb2 import PreKeyRecordStructure
+from .storage_pb2 import SignedPreKeyRecordStructure  # pyright: ignore
 
 
-class PreKeyRecord:
-    def __init__(self, structure: PreKeyRecordStructureProto) -> None:
+class SignedPreKeyRecord:
+    def __init__(self, structure: SignedPreKeyRecordStructureProto) -> None:
         self._structure = structure
 
     @classmethod
     def new(
-        cls,
-        _id: int,
-        ec_key_pair: ECKeyPair,
-    ) -> PreKeyRecord:
-        structure = cast(PreKeyRecordStructureProto, PreKeyRecordStructure())
-        structure.id = _id
-        structure.publicKey = ec_key_pair.get_public_key().serialize()
-        structure.privateKey = ec_key_pair.get_private_key().serialize()
-        return cls(structure)
+        cls, _id: int, timestamp: int, ec_key_pair: ECKeyPair, signature: bytes
+    ) -> SignedPreKeyRecord:
+        record = cast(SignedPreKeyRecordStructureProto, SignedPreKeyRecordStructure())
+
+        record.id = _id
+        record.publicKey = ec_key_pair.get_public_key().serialize()
+        record.privateKey = ec_key_pair.get_private_key().serialize()
+        record.signature = signature
+        record.timestamp = timestamp
+
+        return cls(record)
 
     @classmethod
-    def from_bytes(cls, serialized: bytes) -> PreKeyRecord:
-        record = cast(PreKeyRecordStructureProto, PreKeyRecordStructure())
+    def from_bytes(cls, serialized: bytes) -> SignedPreKeyRecord:
+        record = cast(SignedPreKeyRecordStructureProto, SignedPreKeyRecordStructure())
         record.ParseFromString(serialized)
         return cls(record)
 
     def get_id(self) -> int:
         return self._structure.id
 
-    def get_key_pair(self):
-        public_key = Curve.decode_point(bytearray(self._structure.publicKey), 0)
-        private_key = Curve.decode_private_point(bytearray(self._structure.privateKey))
+    def get_timestamp(self) -> int:
+        return self._structure.timestamp
+
+    def get_key_pair(self) -> ECKeyPair:
+        public_key = Curve.decode_point(self._structure.publicKey)
+        private_key = Curve.decode_private_point(self._structure.privateKey)
+
         return ECKeyPair(public_key, private_key)
 
+    def get_signature(self) -> bytes:
+        return self._structure.signature
+
     def serialize(self) -> bytes:
         return self._structure.SerializeToString()
 
 
-class PreKeyRecordStructureProto(google.protobuf.message.Message):
+class SignedPreKeyRecordStructureProto(google.protobuf.message.Message):
     id: int
     publicKey: bytes
     privateKey: bytes
+    signature: bytes
+    timestamp: int
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/state/sessionstate.py` & `omemo-dr-0.99.2/src/omemo_dr/state/sessionstate.py`

 * *Files 22% similar despite different names*

```diff
@@ -4,115 +4,112 @@
 from typing import Optional
 from typing import Union
 
 import google.protobuf.message
 
 from ..ecc.curve import Curve
 from ..ecc.djbec import CurvePublicKey
-from ..ecc.ec import ECPublicKey
 from ..ecc.eckeypair import ECKeyPair
 from ..identitykeypair import IdentityKey
-from ..identitykeypair import IdentityKeyPair
 from ..kdf.hkdf import HKDF
 from ..kdf.messagekeys import MessageKeys
 from ..ratchet.chainkey import ChainKey
 from ..ratchet.rootkey import RootKey
-from . import storageprotos_pb2 as storageprotos
+from . import storage_pb2
 
 
 class SessionState:
     def __init__(
         self, session: Optional[Union[SessionState, SessionStructureProto]] = None
     ) -> None:
         if session is None:
-            self.session_structure = cast(
-                SessionStructureProto, storageprotos.SessionStructure()
+            self._session_structure = cast(
+                SessionStructureProto, storage_pb2.SessionStructure()  # pyright: ignore
             )
 
         elif isinstance(session, SessionState):
-            self.session_structure = cast(
-                SessionStructureProto, storageprotos.SessionStructure()
+            self._session_structure = cast(
+                SessionStructureProto, storage_pb2.SessionStructure()  # pyright: ignore
             )
-            self.session_structure.CopyFrom(session.get_structure())
+            self._session_structure.CopyFrom(session.get_structure())
 
         else:
-            self.session_structure = session
+            self._session_structure = session
 
     def get_structure(self) -> SessionStructureProto:
-        return self.session_structure
+        return self._session_structure
 
     def get_alice_base_key(self) -> bytes:
-        return self.session_structure.aliceBaseKey
+        return self._session_structure.aliceBaseKey
 
     def set_alice_base_key(self, alice_base_key: bytes) -> None:
-        self.session_structure.aliceBaseKey = alice_base_key
+        self._session_structure.aliceBaseKey = alice_base_key
 
     def set_session_version(self, version: int) -> None:
-        self.session_structure.sessionVersion = version
+        self._session_structure.sessionVersion = version
 
     def get_session_version(self) -> int:
-        session_version = self.session_structure.sessionVersion
-        return 2 if session_version == 0 else session_version
+        return self._session_structure.sessionVersion
 
     def set_remote_identity_key(self, identity_key: IdentityKey) -> None:
-        self.session_structure.remoteIdentityPublic = identity_key.serialize()
+        self._session_structure.remoteIdentityPublic = identity_key.serialize()
 
     def set_local_identity_key(self, identity_key: IdentityKey) -> None:
-        self.session_structure.localIdentityPublic = identity_key.serialize()
+        self._session_structure.localIdentityPublic = identity_key.serialize()
 
     def get_remote_identity_key(self) -> IdentityKey:
-        assert self.session_structure.remoteIdentityPublic is not None
-        return IdentityKey(self.session_structure.remoteIdentityPublic, 0)
+        assert self._session_structure.remoteIdentityPublic is not None
+        return IdentityKey(self._session_structure.remoteIdentityPublic)
 
     def get_local_identity_key(self) -> IdentityKey:
-        return IdentityKey(self.session_structure.localIdentityPublic, 0)
+        return IdentityKey(self._session_structure.localIdentityPublic)
 
     def get_previous_counter(self) -> int:
-        return self.session_structure.previousCounter
+        return self._session_structure.previousCounter
 
     def set_previous_counter(self, previous_counter: int) -> None:
-        self.session_structure.previousCounter = previous_counter
+        self._session_structure.previousCounter = previous_counter
 
     def get_root_key(self) -> RootKey:
-        return RootKey(HKDF(self.get_session_version()), self.session_structure.rootKey)
+        return RootKey(
+            HKDF(self.get_session_version()), self._session_structure.rootKey
+        )
 
     def set_root_key(self, root_key: RootKey) -> None:
-        self.session_structure.rootKey = root_key.get_key_bytes()
+        self._session_structure.rootKey = root_key.get_key_bytes()
 
     def get_sender_ratchet_key(self) -> CurvePublicKey:
-        key = Curve.decode_point(
-            bytearray(self.session_structure.senderChain.senderRatchetKey), 0
-        )
+        key = Curve.decode_point(self._session_structure.senderChain.senderRatchetKey)
         assert isinstance(key, CurvePublicKey)
         return key
 
     def get_sender_ratchet_key_pair(self) -> ECKeyPair:
         public_key = self.get_sender_ratchet_key()
         private_key = Curve.decode_private_point(
-            self.session_structure.senderChain.senderRatchetKeyPrivate
+            self._session_structure.senderChain.senderRatchetKeyPrivate
         )
 
         return ECKeyPair(public_key, private_key)
 
     def has_receiver_chain(
         self, ec_publick_key_sender_ephemeral: CurvePublicKey
     ) -> bool:
         return self.get_receiver_chain(ec_publick_key_sender_ephemeral) is not None
 
     def has_sender_chain(self) -> bool:
-        return self.session_structure.HasField("senderChain")
+        return self._session_structure.HasField("senderChain")
 
     def get_receiver_chain(
         self, ec_publick_key_sender_ephemeral: CurvePublicKey
     ) -> Optional[tuple[ChainStructureProto, int]]:
-        receiver_chains = self.session_structure.receiverChains
+        receiver_chains = self._session_structure.receiverChains
         index = 0
         for receiver_chain in receiver_chains:
             chain_sender_ratchet_key = Curve.decode_point(
-                bytearray(receiver_chain.senderRatchetKey), 0
+                receiver_chain.senderRatchetKey
             )
             if chain_sender_ratchet_key == ec_publick_key_sender_ephemeral:
                 return (receiver_chain, index)
 
             index += 1
 
     def get_receiver_chain_key(
@@ -134,52 +131,52 @@
     def add_receiver_chain(
         self, ec_publick_key_sender_ratchet_key: CurvePublicKey, chain_key: ChainKey
     ) -> None:
         sender_ratchet_key = ec_publick_key_sender_ratchet_key
 
         chain = cast(
             ChainStructureProto,
-            storageprotos.SessionStructure.Chain(),  # pyright: ignore
+            storage_pb2.SessionStructure.Chain(),  # pyright: ignore
         )
         chain.senderRatchetKey = sender_ratchet_key.serialize()
         chain.chainKey.key = chain_key.get_key()
         chain.chainKey.index = chain_key.get_index()
 
-        self.session_structure.receiverChains.extend([chain])
+        self._session_structure.receiverChains.extend([chain])
 
-        if len(self.session_structure.receiverChains) > 5:
-            del self.session_structure.receiverChains[0]
+        if len(self._session_structure.receiverChains) > 5:
+            del self._session_structure.receiverChains[0]
 
     def set_sender_chain(
         self, ec_key_pair_sender_ratchet_key_pair: ECKeyPair, chain_key: ChainKey
     ) -> None:
         sender_ratchet_key_pair = ec_key_pair_sender_ratchet_key_pair
 
-        self.session_structure.senderChain.senderRatchetKey = (
+        self._session_structure.senderChain.senderRatchetKey = (
             sender_ratchet_key_pair.get_public_key().serialize()
         )
-        self.session_structure.senderChain.senderRatchetKeyPrivate = (
+        self._session_structure.senderChain.senderRatchetKeyPrivate = (
             sender_ratchet_key_pair.get_private_key().serialize()
         )
-        self.session_structure.senderChain.chainKey.key = chain_key.key
-        self.session_structure.senderChain.chainKey.index = chain_key.index
+        self._session_structure.senderChain.chainKey.key = chain_key.get_key()
+        self._session_structure.senderChain.chainKey.index = chain_key.get_index()
 
     def get_sender_chain_key(self) -> ChainKey:
-        chain_key_structure = self.session_structure.senderChain.chainKey
+        chain_key_structure = self._session_structure.senderChain.chainKey
         return ChainKey(
             HKDF(self.get_session_version()),
             chain_key_structure.key,
             chain_key_structure.index,
         )
 
     def set_sender_chain_key(self, chain_key_next_chain_key: ChainKey) -> None:
         next_chain_key = chain_key_next_chain_key
 
-        self.session_structure.senderChain.chainKey.key = next_chain_key.get_key()
-        self.session_structure.senderChain.chainKey.index = next_chain_key.get_index()
+        self._session_structure.senderChain.chainKey.key = next_chain_key.get_key()
+        self._session_structure.senderChain.chainKey.index = next_chain_key.get_index()
 
     def has_message_keys(
         self, ec_publick_key_sender_ephemeral: CurvePublicKey, counter: int
     ) -> bool:
         sender_ephemeral = ec_publick_key_sender_ephemeral
         chain_and_index = self.get_receiver_chain(sender_ephemeral)
         assert chain_and_index is not None
@@ -214,15 +211,15 @@
                     message_key.index,
                 )
                 del message_key_list[i]
                 break
 
         assert result is not None
 
-        self.session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
+        self._session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
 
         return result
 
     def set_message_keys(
         self, ec_public_key_sender_ephemeral: CurvePublicKey, message_keys: MessageKeys
     ) -> None:
         sender_ephemeral = ec_public_key_sender_ephemeral
@@ -231,145 +228,87 @@
         chain = chain_and_index[0]
         message_key_structure = chain.messageKeys.add()  # pyright: ignore
         message_key_structure.cipherKey = message_keys.get_cipher_key()
         message_key_structure.macKey = message_keys.get_mac_key()
         message_key_structure.index = message_keys.get_counter()
         message_key_structure.iv = message_keys.get_iv()
 
-        self.session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
+        self._session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
 
     def set_receiver_chain_key(
         self, ec_public_key_sender_ephemeral: CurvePublicKey, chain_key: ChainKey
     ) -> None:
         sender_ephemeral = ec_public_key_sender_ephemeral
         chain_and_index = self.get_receiver_chain(sender_ephemeral)
         assert chain_and_index is not None
         chain = chain_and_index[0]
         chain.chainKey.key = chain_key.get_key()
         chain.chainKey.index = chain_key.get_index()
 
-        self.session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
-
-    def set_pending_key_exchange(
-        self,
-        sequence: int,
-        our_base_key: ECKeyPair,
-        our_ratchet_key: ECKeyPair,
-        our_identity_key: IdentityKeyPair,
-    ) -> None:
-        structure = cast(
-            PendingKeyExchangeStructureProto,
-            self.session_structure.pending_key_exchange(),  # pyright: ignore
-        )
-        structure.sequence = sequence
-        structure.localBaseKey = our_base_key.get_public_key().serialize()
-        structure.localBaseKeyPrivate = our_base_key.get_private_key().serialize()
-        structure.localRatchetKey = our_ratchet_key.get_public_key().serialize()
-        structure.localRatchetKeyPrivate = our_ratchet_key.get_private_key().serialize()
-        structure.localIdentityKey = our_identity_key.get_public_key().serialize()
-        structure.localIdentityKeyPrivate = (
-            our_identity_key.get_private_key().serialize()
-        )
-
-        self.session_structure.pendingKeyExchange.MergeFrom(structure)
-
-    def get_pending_key_exchange_sequence(self) -> int:
-        return self.session_structure.pendingKeyExchange.sequence
-
-    def get_pending_key_exchange_base_key(self) -> ECKeyPair:
-        public_key = Curve.decode_point(
-            bytearray(self.session_structure.pendingKeyExchange.localBaseKey), 0
-        )
-        private_key = Curve.decode_private_point(
-            self.session_structure.pendingKeyExchange.localBaseKeyPrivate
-        )
-        return ECKeyPair(public_key, private_key)
-
-    def get_pending_key_exchange_ratchet_key(self) -> ECKeyPair:
-        public_key = Curve.decode_point(
-            bytearray(self.session_structure.pendingKeyExchange.localRatchetKey), 0
-        )
-        private_key = Curve.decode_private_point(
-            self.session_structure.pendingKeyExchange.localRatchetKeyPrivate
-        )
-        return ECKeyPair(public_key, private_key)
-
-    def get_pending_key_exchange_identity_key(self) -> IdentityKeyPair:
-        public_key = IdentityKey(
-            bytearray(self.session_structure.pendingKeyExchange.localIdentityKey), 0
-        )
-
-        private_key = Curve.decode_private_point(
-            self.session_structure.pendingKeyExchange.localIdentityKeyPrivate
-        )
-        return IdentityKeyPair.new(public_key, private_key)
-
-    def has_pending_key_exchange(self) -> bool:
-        return self.session_structure.HasField("pendingKeyExchange")
+        self._session_structure.receiverChains[chain_and_index[1]].CopyFrom(chain)
 
     def set_unacknowledged_pre_key_message(
         self, pre_key_id: int, signed_pre_key_id: int, base_key: CurvePublicKey
     ) -> None:
-        self.session_structure.pendingPreKey.signedPreKeyId = signed_pre_key_id
-        self.session_structure.pendingPreKey.baseKey = base_key.serialize()
-        self.session_structure.pendingPreKey.preKeyId = pre_key_id
+        self._session_structure.pendingPreKey.signedPreKeyId = signed_pre_key_id
+        self._session_structure.pendingPreKey.baseKey = base_key.serialize()
+        self._session_structure.pendingPreKey.preKeyId = pre_key_id
 
     def has_unacknowledged_pre_key_message(self) -> bool:
-        return self.session_structure.HasField("pendingPreKey")
+        return self._session_structure.HasField("pendingPreKey")
 
     def get_unacknowledged_pre_key_message_items(
         self,
     ) -> UnacknowledgedPreKeyMessageItems:
         pre_key_id = None
-        if self.session_structure.pendingPreKey.HasField("preKeyId"):
-            pre_key_id = self.session_structure.pendingPreKey.preKeyId
+        if self._session_structure.pendingPreKey.HasField("preKeyId"):
+            pre_key_id = self._session_structure.pendingPreKey.preKeyId
 
         assert pre_key_id is not None
-        return SessionState.UnacknowledgedPreKeyMessageItems(
+        return UnacknowledgedPreKeyMessageItems(
             pre_key_id,
-            self.session_structure.pendingPreKey.signedPreKeyId,
-            Curve.decode_point(
-                bytearray(self.session_structure.pendingPreKey.baseKey), 0
-            ),
+            self._session_structure.pendingPreKey.signedPreKeyId,
+            Curve.decode_point(self._session_structure.pendingPreKey.baseKey),
         )
 
     def clear_unacknowledged_pre_key_message(self) -> None:
-        self.session_structure.ClearField("pendingPreKey")
+        self._session_structure.ClearField("pendingPreKey")
 
-    def set_remote_registration_id(self, registration_id: int) -> None:
-        self.session_structure.remoteRegistrationId = registration_id
+    def set_remote_device_id(self, device_id: int) -> None:
+        self._session_structure.remoteRegistrationId = device_id
 
-    def get_remote_registration_id(self) -> int:
-        return self.session_structure.remoteRegistrationId
+    def get_remote_device_id(self) -> int:
+        return self._session_structure.remoteRegistrationId
 
-    def set_local_registration_id(self, registration_id: int) -> None:
-        self.session_structure.localRegistrationId = registration_id
+    def set_our_device_id(self, device_id: int) -> None:
+        self._session_structure.localRegistrationId = device_id
 
-    def get_local_registration_id(self) -> int:
-        return self.session_structure.localRegistrationId
+    def get_our_device_id(self) -> int:
+        return self._session_structure.localRegistrationId
 
     def serialize(self) -> bytes:
-        return self.session_structure.SerializeToString()
+        return self._session_structure.SerializeToString()
+
 
-    class UnacknowledgedPreKeyMessageItems:
-        def __init__(
-            self, pre_key_id: int, signed_pre_key_id: int, base_key: ECPublicKey
-        ) -> None:
-            self.pre_key_id = pre_key_id
-            self.signed_pre_key_id = signed_pre_key_id
-            self.base_key = base_key
+class UnacknowledgedPreKeyMessageItems:
+    def __init__(
+        self, pre_key_id: int, signed_pre_key_id: int, base_key: CurvePublicKey
+    ) -> None:
+        self._pre_key_id = pre_key_id
+        self._signed_pre_key_id = signed_pre_key_id
+        self._base_key = base_key
 
-        def get_pre_key_id(self) -> int:
-            return self.pre_key_id
+    def get_pre_key_id(self) -> int:
+        return self._pre_key_id
 
-        def get_signed_pre_key_id(self) -> int:
-            return self.signed_pre_key_id
+    def get_signed_pre_key_id(self) -> int:
+        return self._signed_pre_key_id
 
-        def get_base_key(self) -> ECPublicKey:
-            return self.base_key
+    def get_base_key(self) -> CurvePublicKey:
+        return self._base_key
 
 
 class MessageKeyStructureProto(google.protobuf.message.Message):
     index: int
     cipherKey: bytes
     macKey: bytes
     iv: bytes
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/state/signedprekeyrecord.py` & `omemo-dr-0.99.2/src/omemo_dr/state/prekeyrecord.py`

 * *Files 17% similar despite different names*

```diff
@@ -2,59 +2,54 @@
 
 from typing import cast
 
 import google.protobuf.message
 
 from ..ecc.curve import Curve
 from ..ecc.eckeypair import ECKeyPair
-from .storageprotos_pb2 import SignedPreKeyRecordStructure
+from . import storage_pb2
 
 
-class SignedPreKeyRecord:
-    def __init__(self, structure: SignedPreKeyRecordStructureProto) -> None:
+class PreKeyRecord:
+    def __init__(self, structure: PreKeyRecordStructureProto) -> None:
         self._structure = structure
 
     @classmethod
     def new(
-        cls, _id: int, timestamp: int, ec_key_pair: ECKeyPair, signature: bytes
-    ) -> SignedPreKeyRecord:
-        record = cast(SignedPreKeyRecordStructureProto, SignedPreKeyRecordStructure())
-
-        record.id = _id
-        record.publicKey = ec_key_pair.get_public_key().serialize()
-        record.privateKey = ec_key_pair.get_private_key().serialize()
-        record.signature = signature
-        record.timestamp = timestamp
-
-        return cls(record)
+        cls,
+        _id: int,
+        ec_key_pair: ECKeyPair,
+    ) -> PreKeyRecord:
+        structure = cast(
+            PreKeyRecordStructureProto,
+            storage_pb2.PreKeyRecordStructure(),  # pyright: ignore
+        )
+        structure.id = _id
+        structure.publicKey = ec_key_pair.get_public_key().serialize()
+        structure.privateKey = ec_key_pair.get_private_key().serialize()
+        return cls(structure)
 
     @classmethod
-    def from_bytes(cls, serialized: bytes) -> SignedPreKeyRecord:
-        record = cast(SignedPreKeyRecordStructureProto, SignedPreKeyRecordStructure())
+    def from_bytes(cls, serialized: bytes) -> PreKeyRecord:
+        record = cast(
+            PreKeyRecordStructureProto,
+            storage_pb2.PreKeyRecordStructure(),  # pyright: ignore
+        )
         record.ParseFromString(serialized)
         return cls(record)
 
     def get_id(self) -> int:
         return self._structure.id
 
-    def get_timestamp(self) -> int:
-        return self._structure.timestamp
-
-    def get_key_pair(self) -> ECKeyPair:
-        public_key = Curve.decode_point(bytearray(self._structure.publicKey), 0)
-        private_key = Curve.decode_private_point(bytearray(self._structure.privateKey))
-
+    def get_key_pair(self):
+        public_key = Curve.decode_point(self._structure.publicKey)
+        private_key = Curve.decode_private_point(self._structure.privateKey)
         return ECKeyPair(public_key, private_key)
 
-    def get_signature(self) -> bytes:
-        return self._structure.signature
-
     def serialize(self) -> bytes:
         return self._structure.SerializeToString()
 
 
-class SignedPreKeyRecordStructureProto(google.protobuf.message.Message):
+class PreKeyRecordStructureProto(google.protobuf.message.Message):
     id: int
     publicKey: bytes
     privateKey: bytes
-    signature: bytes
-    timestamp: int
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/state/store.py` & `omemo-dr-0.99.2/src/omemo_dr/state/store.py`

 * *Files 5% similar despite different names*

```diff
@@ -4,51 +4,68 @@
 
 import abc
 
 from ..const import OMEMOTrust
 from ..identitykey import IdentityKey
 from ..identitykeypair import IdentityKeyPair
 from ..state.prekeyrecord import PreKeyRecord
+from ..structs import IdentityInfo
 from .sessionrecord import SessionRecord
 from .signedprekeyrecord import SignedPreKeyRecord
 
 
 class Store:
     __metaclass__ = abc.ABCMeta
 
-    # Identity
+    # Secret
 
     @abc.abstractmethod
-    def store_own_identity(
+    def set_our_identity(
         self, device_id: int, identity_key_pair: IdentityKeyPair
     ) -> None:
         pass
 
     @abc.abstractmethod
     def get_identity_key_pair(self) -> IdentityKeyPair:
         pass
 
     @abc.abstractmethod
-    def get_local_registration_id(self) -> int:
+    def get_our_device_id(self) -> int:
         pass
 
+    # Identity
+
     @abc.abstractmethod
     def save_identity(self, recipient_id: str, identity_key: IdentityKey) -> None:
         pass
 
     @abc.abstractmethod
+    def delete_identity(self, recipient_id: str, identity_key: IdentityKey) -> None:
+        pass
+
+    @abc.abstractmethod
     def is_trusted_identity(self, recipient_id: str, identity_key: IdentityKey) -> bool:
         pass
 
     @abc.abstractmethod
+    def set_trust(
+        self, recipient_id: str, identity_key: IdentityKey, trust: OMEMOTrust
+    ) -> None:
+        pass
+
+    @abc.abstractmethod
     def set_identity_last_seen(
         self, recipient_id: str, identity_key: IdentityKey
     ) -> None:
         pass
 
+    @abc.abstractmethod
+    def get_identity_infos(self, recipient_ids: str | list[str]) -> list[IdentityInfo]:
+        pass
+
     # Pre Keys
 
     @abc.abstractmethod
     def get_pre_key_count(self) -> int:
         pass
 
     @abc.abstractmethod
@@ -152,18 +169,14 @@
     @abc.abstractmethod
     def get_trust_for_identity(
         self, recipient_id: str, identity_key: IdentityKey
     ) -> Optional[OMEMOTrust]:
         pass
 
     @abc.abstractmethod
-    def get_trusted_fingerprints(self, address: str) -> list[IdentityKey]:
-        pass
-
-    @abc.abstractmethod
     def get_unacknowledged_count(self, recipient_id: str, device_id: int) -> int:
         pass
 
     @abc.abstractmethod
     def set_active_state(self, address: str, devicelist: list[int]) -> None:
         pass
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/util/byteutil.py` & `omemo-dr-0.99.2/src/omemo_dr/util/byteutil.py`

 * *Files 8% similar despite different names*

```diff
@@ -2,23 +2,23 @@
 
 from typing import Any
 from typing import Optional
 
 
 class ByteUtil:
     @staticmethod
-    def combine(*args: Any) -> bytearray:
+    def combine(*args: Any) -> bytes:
         baos = bytearray()
         for a in args:
             if isinstance(a, (list, bytearray, str, bytes)):
                 baos.extend(a)  # pyright: ignore
             else:
                 baos.append(a)
 
-        return baos
+        return bytes(baos)
 
     @staticmethod
     def split(
         inp: bytes,
         first_length: int,
         second_length: int,
         third_length: Optional[int] = None,
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr/util/keyhelper.py` & `omemo-dr-0.99.2/src/omemo_dr/util/keyhelper.py`

 * *Files 15% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 
 import binascii
 import math
 import os
 import time
 
 from ..ecc.curve import Curve
-from ..ecc.eckeypair import ECKeyPair
 from ..identitykey import IdentityKey
 from ..identitykeypair import IdentityKeyPair
 from ..state.prekeyrecord import PreKeyRecord
 from ..state.signedprekeyrecord import SignedPreKeyRecord
 from .medium import Medium
 
 
@@ -24,15 +23,15 @@
         """
         key_pair = Curve.generate_key_pair()
         public_key = IdentityKey(key_pair.get_public_key())
         identity_key_pair = IdentityKeyPair.new(public_key, key_pair.get_private_key())
         return identity_key_pair
 
     @staticmethod
-    def generate_registration_id() -> int:
+    def generate_device_id() -> int:
         """
         Generate a registration ID.  Clients should only do this once,
         at install time.
         """
         regId = KeyHelper.get_random_sequence()
         return regId
 
@@ -71,19 +70,7 @@
         )
 
         spk = SignedPreKeyRecord.new(
             signed_pre_key_id, int(round(time.time() * 1000)), key_pair, signature
         )
 
         return spk
-
-    @staticmethod
-    def generate_sender_signing_key() -> ECKeyPair:
-        return Curve.generate_key_pair()
-
-    @staticmethod
-    def generate_sender_key() -> bytes:
-        return os.urandom(32)
-
-    @staticmethod
-    def generate_sender_key_id() -> int:
-        return KeyHelper.get_random_sequence(2147483647)
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr.egg-info/PKG-INFO` & `omemo-dr-0.99.2/src/omemo_dr.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: omemo-dr
-Version: 0.99.1
+Version: 0.99.2
 Summary: OMEMO Double Ratchet
 Author: Philipp Hörist
 Author-email: philipp@hoerist.com
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/>
@@ -686,75 +686,68 @@
 Classifier: Topic :: Security :: Cryptography
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
-Initial codebase was forked from https://github.com/tgalal/python-axolotl
-
-This is a python port of [libsignal-protocol-java](https://github.com/WhisperSystems/libaxolotl-android) originally written by [Moxie Marlinspike](https://github.com/moxie0)
-
+Initial codebase was forked from https://github.com/tgalal/python-axolotl but has since been heavily rewritten.
 
 # Dependencies
 
- - [protobuf 3.0+](https://github.com/google/protobuf/)
- - [cryptography](https://cryptography.io)
+ - [protobuf](https://pypi.org/project/protobuf/) (>=4.21.0)
+ - [cryptography](https://pypi.org/project/cryptography/)
 
 ## Linux
 
 ```
 pip install .
 ```
 
 # Usage
 
-This python port is done in an almost 1:1 mapping to the original java code. Therefore any original documentation for the java code can be easily mapped and used with this python port.
-
-## Install time
-
-At install time, a libaxolotl client needs to generate its identity keys, registration id, and
-prekeys.
-
-```python
-    identity_key_pair = KeyHelper.generate_identity_key_pair()
-    registration_id   = KeyHelper.generate_registration_id()
-    pre_keys          = KeyHelper.generate_pre_keys(start_id, 100)
-    last_resort_key   = KeyHelper.generate_last_resort_key()
-    signed_pre_key    = KeyHelper.generate_signed_pre_key(identity_key_pair, 5)
-
-    #Store identity_key_pair somewhere durable and safe.
-    #Store registration_id somewhere durable and safe.
-
-    #Store pre_keys in PreKeyStore.
-    #Store signed prekey in SignedPreKeyStore.
-```
+This library handles only the crypto part of OMEMO, not the XMPP protocol part. This means you need to take care yourself of things like publishing/downloading bundles, publishing/subscribing to PEP deviceliste updates, sending and receiving messages.
 
 ## Building a session
 
-A libaxolotl client needs to implement the Store interface. This will manage loading and storing of identity, 
-prekeys, signed prekeys, and session state.
+A OMEMO client needs to implement the Store interface (omemo_dr.state.store.Store). This will manage loading and storing of identity, prekeys, signed prekeys, and session state.
 
 Once this is implemented, building a session is fairly straightforward:
 
 ```python
-store      = MyStore()
-
-# Instantiate a SessionBuilder for a remote recipient_id + device_id tuple.
-session_builder = SessionBuilder(store, recipient_id, device_id)
+storage = MyStorage()
 
-# Build a session with a PreKey retrieved from the server.
-sessionBuilder.process(retrieved_pre_key)
-
-session_cipher = SessionCipher(store, recipient_id, device_id)
-message        = session_cipher.encrypt("Hello world!")
-
-deliver(message.serialize())
+config = OMEMOConfig(default_prekey_amount=100,
+                     min_prekey_amount=80,
+                     spk_archive_seconds=86400 * 15,
+                     spk_cycle_seconds=86400,
+                     unacknowledged_count=2000)
+
+manager = OMEMOSessionManager(address, storage, config)
+
+# Get your bundle for publishing
+bundle = manager.get_bundle('eu.siacs.conversations.axolotl')
+my_publish_method(bundle)
+
+# Build a session with a downloaded bundle of a remote contact
+bundle = my_receive_bundle_method()
+manager.build_session(remote_address, bundle)
+
+# Encrypt a message to a remote contact
+message = manager.encrypt(remote_address, plaintext)
+my_send_message_method(message)
+
+# Descrypt a message
+message = my_receive_message_method()
+plaintext, fingerprint, trust = manager.decrypt(message, remote_address)
 ```
 
 # Development
 
 ## Generating protobuf files
 
-Download the protobuf-compiler and execute
+Download the protobuf-compiler > 3.19 and execute
 
-`protoc -I=omemo_dr/protobuf --python_out=omemo_dr/protobuf OMEMO.proto WhisperTextProtocol.proto LocalStorageProtocol.proto`
+```bash
+$ protoc -I=src/omemo_dr/protobuf --python_out=src/omemo_dr/protocol omemo.proto whisper.proto
+$ protoc -I=src/omemo_dr/protobuf --python_out=src/omemo_dr/state storage.proto
+```
```

### Comparing `omemo-dr-0.99.1/src/omemo_dr.egg-info/SOURCES.txt` & `omemo-dr-0.99.2/src/omemo_dr.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -116,15 +116,15 @@
 src/omemo_dr/aes.py
 src/omemo_dr/const.py
 src/omemo_dr/exceptions.py
 src/omemo_dr/identitykey.py
 src/omemo_dr/identitykeypair.py
 src/omemo_dr/observable.py
 src/omemo_dr/py.typed
-src/omemo_dr/session.py
+src/omemo_dr/session_manager.py
 src/omemo_dr/sessionbuilder.py
 src/omemo_dr/sessioncipher.py
 src/omemo_dr/structs.py
 src/omemo_dr.egg-info/PKG-INFO
 src/omemo_dr.egg-info/SOURCES.txt
 src/omemo_dr.egg-info/dependency_links.txt
 src/omemo_dr.egg-info/requires.txt
@@ -142,44 +142,41 @@
 src/omemo_dr/kdf/messagekeys.py
 src/omemo_dr/protocol/__init__.py
 src/omemo_dr/protocol/ciphertextmessage.py
 src/omemo_dr/protocol/omemo_keyexchange.py
 src/omemo_dr/protocol/omemo_message.py
 src/omemo_dr/protocol/omemo_pb2.py
 src/omemo_dr/protocol/prekeywhispermessage.py
+src/omemo_dr/protocol/whisper_pb2.py
 src/omemo_dr/protocol/whispermessage.py
-src/omemo_dr/protocol/whisperprotos_pb2.py
 src/omemo_dr/ratchet/__init__.py
 src/omemo_dr/ratchet/aliceparameters.py
 src/omemo_dr/ratchet/bobparameters.py
 src/omemo_dr/ratchet/chainkey.py
 src/omemo_dr/ratchet/ratchetingsession.py
 src/omemo_dr/ratchet/rootkey.py
 src/omemo_dr/state/__init__.py
 src/omemo_dr/state/prekeybundle.py
 src/omemo_dr/state/prekeyrecord.py
 src/omemo_dr/state/sessionrecord.py
 src/omemo_dr/state/sessionstate.py
 src/omemo_dr/state/signedprekeyrecord.py
-src/omemo_dr/state/storageprotos_pb2.py
+src/omemo_dr/state/storage_pb2.py
 src/omemo_dr/state/store.py
 src/omemo_dr/util/__init__.py
 src/omemo_dr/util/byteutil.py
 src/omemo_dr/util/keyhelper.py
+src/omemo_dr/util/logging.py
 src/omemo_dr/util/medium.py
 tests/__init__.py
 tests/inmemoryidentitykeystore.py
 tests/inmemoryprekeystore.py
 tests/inmemorysessionstore.py
 tests/inmemorysignedprekeystore.py
 tests/inmemorystore.py
 tests/test_sessionbuilder.py
 tests/test_sessioncipher.py
 tests/test_sigs.py
 tests/kdf/__init__.py
 tests/kdf/test_hkdf.py
-tests/ratchet/__init__.py
-tests/ratchet/test_chainkey.py
-tests/ratchet/test_ratchetingsession.py
-tests/ratchet/test_rootkey.py
 tests/util/__init__.py
 tests/util/test_byteutil.py
```

### Comparing `omemo-dr-0.99.1/tests/inmemoryidentitykeystore.py` & `omemo-dr-0.99.2/tests/inmemoryidentitykeystore.py`

 * *Files 18% similar despite different names*

```diff
@@ -10,21 +10,21 @@
     def __init__(self) -> None:
         self.trusted_keys: dict[str, IdentityKey] = {}
         identity_key_pair_keys = Curve.generate_key_pair()
         self.identity_key_pair = IdentityKeyPair.new(
             IdentityKey(identity_key_pair_keys.get_public_key()),
             identity_key_pair_keys.get_private_key(),
         )
-        self.local_registration_id = KeyHelper.generate_registration_id()
+        self.our_device_id = KeyHelper.generate_device_id()
 
     def get_identity_key_pair(self) -> IdentityKeyPair:
         return self.identity_key_pair
 
-    def get_local_registration_id(self) -> int:
-        return self.local_registration_id
+    def get_our_device_id(self) -> int:
+        return self.our_device_id
 
     def save_identity(self, recipient_id: str, identity_key: IdentityKey) -> None:
         self.trusted_keys[recipient_id] = identity_key
 
     def is_trusted_identity(self, recipient_id: str, identity_key: IdentityKey) -> bool:
         if recipient_id not in self.trusted_keys:
             return True
```

### Comparing `omemo-dr-0.99.1/tests/inmemoryprekeystore.py` & `omemo-dr-0.99.2/tests/inmemoryprekeystore.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/tests/inmemorysessionstore.py` & `omemo-dr-0.99.2/tests/inmemorysessionstore.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/tests/inmemorysignedprekeystore.py` & `omemo-dr-0.99.2/tests/inmemorysignedprekeystore.py`

 * *Files identical despite different names*

### Comparing `omemo-dr-0.99.1/tests/inmemorystore.py` & `omemo-dr-0.99.2/tests/inmemorystore.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,16 +19,16 @@
         self.pre_key_store = InMemoryPreKeyStore()
         self.signed_pre_key_store = InMemorySignedPreKeyStore()
         self.session_store = InMemorySessionStore()
 
     def get_identity_key_pair(self) -> IdentityKeyPair:
         return self.identity_key_store.get_identity_key_pair()
 
-    def get_local_registration_id(self) -> int:
-        return self.identity_key_store.get_local_registration_id()
+    def get_our_device_id(self) -> int:
+        return self.identity_key_store.get_our_device_id()
 
     def save_identity(self, recipient_id: str, identity_key: IdentityKey) -> None:
         self.identity_key_store.save_identity(recipient_id, identity_key)
 
     def is_trusted_identity(self, recipient_id: str, identity_key: IdentityKey) -> bool:
         return self.identity_key_store.is_trusted_identity(recipient_id, identity_key)
```

### Comparing `omemo-dr-0.99.1/tests/test_sessionbuilder.py` & `omemo-dr-0.99.2/tests/test_sessionbuilder.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import time
 import unittest
 
+from omemo_dr.const import NS_OMEMO_TMP
 from omemo_dr.ecc.curve import Curve
 from omemo_dr.exceptions import InvalidKeyException
 from omemo_dr.protocol.ciphertextmessage import CiphertextMessage
 from omemo_dr.protocol.prekeywhispermessage import PreKeyWhisperMessage
 from omemo_dr.protocol.whispermessage import WhisperMessage
 from omemo_dr.sessionbuilder import SessionBuilder
 from omemo_dr.sessioncipher import SessionCipher
@@ -28,16 +29,16 @@
         bob_signed_pre_key_pair = Curve.generate_key_pair()
         bob_signed_pre_key_signature = Curve.calculate_signature(
             bob_store.get_identity_key_pair().get_private_key(),
             bob_signed_pre_key_pair.get_public_key().serialize(),
         )
 
         bob_pre_key = PreKeyBundle(
-            bob_store.get_local_registration_id(),
             1,
+            NS_OMEMO_TMP,
             31337,
             bob_pre_key_pair.get_public_key(),
             22,
             bob_signed_pre_key_pair.get_public_key(),
             bob_signed_pre_key_signature,
             bob_store.get_identity_key_pair().get_public_key(),
         )
@@ -132,30 +133,30 @@
         )
 
         for i in range(0, len(bob_signed_pre_key_signature) * 8):
             modified_signature = bytearray(bob_signed_pre_key_signature[:])
             modified_signature[int(i / 8)] ^= 0x01 << (i % 8)
 
             bob_pre_key = PreKeyBundle(
-                bob_identity_key_store.get_local_registration_id(),
                 1,
+                NS_OMEMO_TMP,
                 31337,
                 bob_pre_key_pair.get_public_key(),
                 22,
                 bob_signed_pre_key_pair.get_public_key(),
                 bytes(modified_signature),
                 bob_identity_key_store.get_identity_key_pair().get_public_key(),
             )
 
             with self.assertRaises(InvalidKeyException):
                 alice_session_builder.process_pre_key_bundle(bob_pre_key)
 
         bob_pre_key = PreKeyBundle(
-            bob_identity_key_store.get_local_registration_id(),
             1,
+            NS_OMEMO_TMP,
             31337,
             bob_pre_key_pair.get_public_key(),
             22,
             bob_signed_pre_key_pair.get_public_key(),
             bob_signed_pre_key_signature,
             bob_identity_key_store.get_identity_key_pair().get_public_key(),
         )
```

### Comparing `omemo-dr-0.99.1/tests/test_sessioncipher.py` & `omemo-dr-0.99.2/tests/test_sessioncipher.py`

 * *Files 12% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 from omemo_dr.protocol.whispermessage import WhisperMessage
 from omemo_dr.ratchet.aliceparameters import AliceParameters
 from omemo_dr.ratchet.bobparameters import BobParameters
 from omemo_dr.ratchet.ratchetingsession import RatchetingSession
 from omemo_dr.sessioncipher import SessionCipher
 from omemo_dr.state.sessionrecord import SessionRecord
 from omemo_dr.state.sessionstate import SessionState
+from omemo_dr.util.keyhelper import KeyHelper
 
 from .inmemorystore import InMemoryStore
 
 
 class SessionCipherTest(unittest.TestCase):
     def test_basic_session_v3(self):
         alice_session_record = SessionRecord()
@@ -83,29 +84,30 @@
         bob_identity_key_pair = Curve.generate_key_pair()
         bob_identity_key = IdentityKeyPair.new(
             IdentityKey(bob_identity_key_pair.get_public_key()),
             bob_identity_key_pair.get_private_key(),
         )
         bob_base_key = Curve.generate_key_pair()
         bob_ephemeral_key = bob_base_key
+        bob_one_time_pre_key = KeyHelper.generate_pre_keys(1, 1)[0]
 
         alice_parameters = AliceParameters(
             alice_identity_key,
             alice_base_key,
             bob_identity_key.get_public_key(),
             bob_base_key.get_public_key(),
             bob_ephemeral_key.get_public_key(),
-            None,
+            bob_one_time_pre_key.get_key_pair().get_public_key(),
         )
 
         bob_parameters = BobParameters(
             bob_identity_key,
             bob_base_key,
             bob_ephemeral_key,
-            None,
+            bob_one_time_pre_key.get_key_pair(),
             alice_identity_key.get_public_key(),
             alice_base_key.get_public_key(),
         )
 
         RatchetingSession.initialize_session_as_alice(
             alice_session_state, 3, alice_parameters
         )
```

### Comparing `omemo-dr-0.99.1/tests/test_sigs.py` & `omemo-dr-0.99.2/tests/test_sigs.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from omemo_dr.ecc.curve import Curve
 from omemo_dr.ecc.djbec import CurvePublicKey
 from omemo_dr.util.keyhelper import KeyHelper
 
 
 class Curve25519Test(unittest.TestCase):
     def test_agreement(self):
-        alice_public = bytearray(
+        alice_public = bytes(
             [
                 0x05,
                 0x1B,
                 0xB7,
                 0x59,
                 0x66,
                 0xF2,
@@ -40,15 +40,15 @@
                 0xBF,
                 0xA2,
                 0xE4,
                 0xEE,
                 0x28,
             ]
         )
-        alice_private = bytearray(
+        alice_private = bytes(
             [
                 0xC8,
                 0x06,
                 0x43,
                 0x9D,
                 0xC9,
                 0xD2,
@@ -77,15 +77,15 @@
                 0x6B,
                 0xB4,
                 0xBF,
                 0x59,
             ]
         )
 
-        bob_public = bytearray(
+        bob_public = bytes(
             [
                 0x05,
                 0x65,
                 0x36,
                 0x14,
                 0x99,
                 0x3D,
@@ -115,15 +115,15 @@
                 0x5A,
                 0x27,
                 0xA2,
                 0x2F,
             ]
         )
 
-        bob_private = bytearray(
+        bob_private = bytes(
             [
                 0xB0,
                 0x3B,
                 0x34,
                 0xC3,
                 0x3A,
                 0x1C,
@@ -152,15 +152,15 @@
                 0xB9,
                 0x1B,
                 0x44,
                 0x66,
             ]
         )
 
-        shared = bytearray(
+        shared = bytes(
             [
                 0x32,
                 0x5F,
                 0x23,
                 0x93,
                 0x28,
                 0x94,
@@ -189,20 +189,20 @@
                 0xC4,
                 0x77,
                 0xE6,
                 0x29,
             ]
         )
 
-        alice_public_key = Curve.decode_point(alice_public, 0)
+        alice_public_key = Curve.decode_point(alice_public)
         assert isinstance(alice_public_key, CurvePublicKey)
 
         alice_private_key = Curve.decode_private_point(alice_private)
 
-        bob_public_key = Curve.decode_point(bob_public, 0)
+        bob_public_key = Curve.decode_point(bob_public)
         assert isinstance(bob_public_key, CurvePublicKey)
 
         bob_private_key = Curve.decode_private_point(bob_private)
 
         shared_one = Curve.calculate_agreement(alice_public_key, bob_private_key)
         shared_two = Curve.calculate_agreement(bob_public_key, alice_private_key)
 
@@ -222,19 +222,19 @@
             self.assertEqual(shared_alice, shared_bob)
 
     def test_gensig(self):
         identity_key_pair = KeyHelper.generate_identity_key_pair()
         KeyHelper.generate_signed_pre_key(identity_key_pair, 0)
 
     def test_signature(self):
-        # aliceIdentityPrivate = bytearray([0xc0, 0x97, 0x24, 0x84, 0x12, 0xe5, 0x8b, 0xf0, 0x5d, 0xf4, 0x87, 0x96,
+        # aliceIdentityPrivate = bytes([0xc0, 0x97, 0x24, 0x84, 0x12, 0xe5, 0x8b, 0xf0, 0x5d, 0xf4, 0x87, 0x96,
         #                                   0x82, 0x05, 0x13, 0x27, 0x94, 0x17, 0x8e, 0x36, 0x76, 0x37, 0xf5, 0x81,
         #                                   0x8f, 0x81, 0xe0, 0xe6, 0xce, 0x73, 0xe8, 0x65])
 
-        alice_identity_public = bytearray(
+        alice_identity_public = bytes(
             [
                 0x05,
                 0xAB,
                 0x7E,
                 0x71,
                 0x7D,
                 0x4A,
@@ -264,15 +264,15 @@
                 0x7E,
                 0x32,
                 0x2C,
                 0x64,
             ]
         )
 
-        alice_ephemeral_public = bytearray(
+        alice_ephemeral_public = bytes(
             [
                 0x05,
                 0xED,
                 0xCE,
                 0x9D,
                 0x9C,
                 0x41,
@@ -302,15 +302,15 @@
                 0x2D,
                 0x99,
                 0xFB,
                 0x4A,
             ]
         )
 
-        alice_signature = bytearray(
+        alice_signature = bytes(
             [
                 0x5D,
                 0xE8,
                 0x8C,
                 0xA9,
                 0xA8,
                 0x9B,
@@ -372,17 +372,17 @@
                 0xB8,
                 0x6E,
                 0x88,
             ]
         )
 
         # alice_private_key = Curve.decode_private_point(alice_identity_private)
-        alice_public_key = Curve.decode_point(alice_identity_public, 0)
+        alice_public_key = Curve.decode_point(alice_identity_public)
         assert isinstance(alice_public_key, CurvePublicKey)
 
-        alice_ephemeral = Curve.decode_point(alice_ephemeral_public, 0)
+        alice_ephemeral = Curve.decode_point(alice_ephemeral_public)
         assert isinstance(alice_ephemeral, CurvePublicKey)
 
         res = Curve.verify_signature(
-            alice_public_key, alice_ephemeral.serialize(), bytes(alice_signature)
+            alice_public_key, alice_ephemeral.serialize(), alice_signature
         )
         self.assertTrue(res)
```

