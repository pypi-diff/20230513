# Comparing `tmp/espnet_onnx-0.1.8.tar.gz` & `tmp/espnet_onnx-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "espnet_onnx-0.1.8.tar", last modified: Thu Jun  9 18:31:06 2022, max compression
+gzip compressed data, was "espnet_onnx-0.1.9.tar", last modified: Mon Jun 13 15:27:42 2022, max compression
```

## Comparing `espnet_onnx-0.1.8.tar` & `espnet_onnx-0.1.9.tar`

### file list

```diff
@@ -1,138 +1,142 @@
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/
--rw-rw-r--   0 masao     (1000) masao     (1000)     1069 2022-03-04 10:57:47.000000 espnet_onnx-0.1.8/LICENSE
--rw-rw-r--   0 masao     (1000) masao     (1000)     7125 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/PKG-INFO
--rw-rw-r--   0 masao     (1000) masao     (1000)     6295 2022-06-09 18:30:38.000000 espnet_onnx-0.1.8/README.md
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.448327 espnet_onnx-0.1.8/espnet_onnx/
--rw-rw-r--   0 masao     (1000) masao     (1000)      185 2022-06-09 18:30:29.000000 espnet_onnx-0.1.8/espnet_onnx/__init__.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.448327 espnet_onnx-0.1.8/espnet_onnx/asr/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3120 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/abs_asr_model.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3360 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/asr_model.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     6454 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/asr/asr_streaming.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.448327 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    12061 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/batch_beam_search.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     4930 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/batch_beam_search_online_sim.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    16639 2022-05-14 05:43:09.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/beam_search.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    27032 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/beam_search_transducer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1715 2022-05-14 05:43:20.000000 espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/hyps.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1199 2022-05-05 04:38:52.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/frontend.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2400 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/global_mvn.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2226 2022-04-30 03:46:17.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/logmel.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2225 2022-05-05 04:38:52.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/stft.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2133 2022-05-05 04:38:52.000000 espnet_onnx-0.1.8/espnet_onnx/asr/frontend/utterance_mvn.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/model/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      640 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoder.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     7129 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/rnn.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     7233 2022-05-21 09:39:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/transducer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3516 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/xformer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      470 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/encoder.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-30 03:51:48.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3221 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/encoder.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     5732 2022-05-21 09:39:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/streaming.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      732 2022-05-21 09:39:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/joint_network.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      565 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/lm.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-02 05:08:40.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     4693 2022-05-21 09:39:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/seqrnn_lm.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3890 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/transformer_lm.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2239 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/build_tokenizer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2100 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/token_id_converter.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2175 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/char_tokenizer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    16574 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/phoneme_tokenizer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1228 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/sentencepiece_tokenizer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2033 2022-03-13 10:13:38.000000 espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/word_tokenizer.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    19178 2022-05-21 09:39:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/ctc_prefix_scorer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     5833 2022-04-02 14:23:34.000000 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/interface.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1722 2022-03-12 13:34:32.000000 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/length_bonus.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3043 2022-03-05 08:52:26.000000 espnet_onnx-0.1.8/espnet_onnx/asr/scorer/ngram.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/
--rw-rw-r--   0 masao     (1000) masao     (1000)       86 2022-05-28 13:48:46.000000 espnet_onnx-0.1.8/espnet_onnx/export/__init__.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/asr/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     9445 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/export_asr.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2552 2022-05-05 04:38:52.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/get_config.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/
--rw-rw-r--   0 masao     (1000) masao     (1000)     2324 2022-05-31 11:16:50.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      872 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/ctc.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     8199 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/rnn.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2679 2022-06-09 17:57:26.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/transducer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2814 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/xformer.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     8666 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/contextual_block_xformer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     8565 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/rnn.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     4914 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/xformer.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1321 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/joint_network.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-14 03:33:52.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    11869 2022-06-09 18:03:50.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/embed.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2828 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/seq_rnn.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2915 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/transformer.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/tts/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     7071 2022-06-09 18:18:25.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/export_tts.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2014 2022-06-09 18:22:41.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/get_config.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/
--rw-rw-r--   0 masao     (1000) masao     (1000)     2882 2022-06-09 18:14:08.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/__init__.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     8712 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/fastspeech2.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    13781 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/tacotron2.py
--rw-rw-r--   0 masao     (1000) masao     (1000)    11263 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/vits.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.452327 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1434 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/hifigan.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1090 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/melgan.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1827 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/parallel_wavegan.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2044 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/style_melgan.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/tts/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     4400 2022-06-09 18:23:22.000000 espnet_onnx-0.1.8/espnet_onnx/tts/abs_tts_model.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/tts/model/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2375 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/duration_calculator.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      773 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/common_processor.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2025 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/korean_cleaner.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1520 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/text_cleaner.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      481 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_model.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2342 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/fast_speech2.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     6872 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/tacotron2.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2255 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/vits.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     5387 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/griffin_lim.py
--rw-rw-r--   0 masao     (1000) masao     (1000)      813 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/vocoder.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     3723 2022-06-09 18:25:38.000000 espnet_onnx-0.1.8/espnet_onnx/tts/tts_model.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/espnet_onnx/utils/
--rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.8/espnet_onnx/utils/__init__.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2882 2022-06-09 17:57:27.000000 espnet_onnx-0.1.8/espnet_onnx/utils/abs_model.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     2958 2022-04-10 10:21:03.000000 espnet_onnx-0.1.8/espnet_onnx/utils/config.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     9556 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/utils/function.py
--rw-rw-r--   0 masao     (1000) masao     (1000)     1291 2022-05-31 11:16:58.000000 espnet_onnx-0.1.8/espnet_onnx/utils/torch_function.py
-drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-09 18:31:06.448327 espnet_onnx-0.1.8/espnet_onnx.egg-info/
--rw-rw-r--   0 masao     (1000) masao     (1000)     7125 2022-06-09 18:31:06.000000 espnet_onnx-0.1.8/espnet_onnx.egg-info/PKG-INFO
--rw-rw-r--   0 masao     (1000) masao     (1000)     4458 2022-06-09 18:31:06.000000 espnet_onnx-0.1.8/espnet_onnx.egg-info/SOURCES.txt
--rw-rw-r--   0 masao     (1000) masao     (1000)        1 2022-06-09 18:31:06.000000 espnet_onnx-0.1.8/espnet_onnx.egg-info/dependency_links.txt
--rw-rw-r--   0 masao     (1000) masao     (1000)      168 2022-06-09 18:31:06.000000 espnet_onnx-0.1.8/espnet_onnx.egg-info/requires.txt
--rw-rw-r--   0 masao     (1000) masao     (1000)       12 2022-06-09 18:31:06.000000 espnet_onnx-0.1.8/espnet_onnx.egg-info/top_level.txt
--rw-rw-r--   0 masao     (1000) masao     (1000)       38 2022-06-09 18:31:06.456327 espnet_onnx-0.1.8/setup.cfg
--rw-rw-r--   0 masao     (1000) masao     (1000)     1570 2022-06-09 18:30:17.000000 espnet_onnx-0.1.8/setup.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1069 2022-03-04 10:57:47.000000 espnet_onnx-0.1.9/LICENSE
+-rw-rw-r--   0 masao     (1000) masao     (1000)     7125 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/PKG-INFO
+-rw-rw-r--   0 masao     (1000) masao     (1000)     6295 2022-06-13 15:26:18.000000 espnet_onnx-0.1.9/README.md
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/
+-rw-rw-r--   0 masao     (1000) masao     (1000)      186 2022-06-13 15:26:35.000000 espnet_onnx-0.1.9/espnet_onnx/__init__.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3120 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/abs_asr_model.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3360 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/asr_model.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     6454 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/asr/asr_streaming.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    12061 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/batch_beam_search.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     4930 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/batch_beam_search_online_sim.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    16639 2022-05-14 05:43:09.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/beam_search.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    27032 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/beam_search_transducer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1715 2022-05-14 05:43:20.000000 espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/hyps.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1199 2022-05-05 04:38:52.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/frontend.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2400 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/global_mvn.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2226 2022-04-30 03:46:17.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/logmel.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2225 2022-05-05 04:38:52.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/stft.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2133 2022-05-05 04:38:52.000000 espnet_onnx-0.1.9/espnet_onnx/asr/frontend/utterance_mvn.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/model/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      640 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoder.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     7129 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/rnn.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     7233 2022-05-21 09:39:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/transducer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3516 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/xformer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      470 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/encoder.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-30 03:51:48.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3221 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/encoder.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     5732 2022-05-21 09:39:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/streaming.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      732 2022-05-21 09:39:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/joint_network.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      565 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/lm.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-02 05:08:40.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     4693 2022-05-21 09:39:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/seqrnn_lm.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3890 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/transformer_lm.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2239 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/build_tokenizer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2100 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/token_id_converter.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2175 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/char_tokenizer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    16574 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/phoneme_tokenizer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1228 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/sentencepiece_tokenizer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2033 2022-03-13 10:13:38.000000 espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/word_tokenizer.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    19178 2022-05-21 09:39:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/ctc_prefix_scorer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     5833 2022-04-02 14:23:34.000000 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/interface.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1722 2022-03-12 13:34:32.000000 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/length_bonus.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3043 2022-03-05 08:52:26.000000 espnet_onnx-0.1.9/espnet_onnx/asr/scorer/ngram.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/export/
+-rw-rw-r--   0 masao     (1000) masao     (1000)       86 2022-05-28 13:48:46.000000 espnet_onnx-0.1.9/espnet_onnx/export/__init__.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/export/asr/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     9445 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/export_asr.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2552 2022-05-05 04:38:52.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/get_config.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2324 2022-05-31 11:16:50.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      872 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/ctc.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     8199 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/rnn.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2679 2022-06-09 17:57:26.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/transducer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2814 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/xformer.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     8666 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/contextual_block_xformer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     8565 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/rnn.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     4914 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/xformer.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1321 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/joint_network.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-14 03:33:52.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    11869 2022-06-09 18:03:50.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/embed.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2828 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/seq_rnn.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2915 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/transformer.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/layers/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-06-13 15:18:32.000000 espnet_onnx-0.1.9/espnet_onnx/export/layers/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    15775 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/layers/attention.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1367 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/layers/predecoder.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/tts/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     7071 2022-06-09 18:18:25.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/export_tts.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2014 2022-06-09 18:22:41.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/get_config.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2882 2022-06-09 18:14:08.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/__init__.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     8712 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/fastspeech2.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    13781 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/tacotron2.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)    11263 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/vits.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1434 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/hifigan.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1090 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/melgan.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1827 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/parallel_wavegan.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2044 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/style_melgan.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/tts/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     4400 2022-06-09 18:23:22.000000 espnet_onnx-0.1.9/espnet_onnx/tts/abs_tts_model.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/tts/model/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2375 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/duration_calculator.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      773 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/common_processor.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2025 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/korean_cleaner.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1520 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/text_cleaner.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      481 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_model.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-05-21 09:16:57.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2342 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/fast_speech2.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     6872 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/tacotron2.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2255 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/vits.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     5387 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/griffin_lim.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)      813 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/vocoder.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     3723 2022-06-09 18:25:38.000000 espnet_onnx-0.1.9/espnet_onnx/tts/tts_model.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/espnet_onnx/utils/
+-rw-rw-r--   0 masao     (1000) masao     (1000)        0 2022-04-02 14:31:58.000000 espnet_onnx-0.1.9/espnet_onnx/utils/__init__.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2882 2022-06-09 17:57:27.000000 espnet_onnx-0.1.9/espnet_onnx/utils/abs_model.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     2958 2022-04-10 10:21:03.000000 espnet_onnx-0.1.9/espnet_onnx/utils/config.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     9556 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/utils/function.py
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1291 2022-05-31 11:16:58.000000 espnet_onnx-0.1.9/espnet_onnx/utils/torch_function.py
+drwxrwxr-x   0 masao     (1000) masao     (1000)        0 2022-06-13 15:27:42.001035 espnet_onnx-0.1.9/espnet_onnx.egg-info/
+-rw-rw-r--   0 masao     (1000) masao     (1000)     7125 2022-06-13 15:27:41.000000 espnet_onnx-0.1.9/espnet_onnx.egg-info/PKG-INFO
+-rw-rw-r--   0 masao     (1000) masao     (1000)     4575 2022-06-13 15:27:41.000000 espnet_onnx-0.1.9/espnet_onnx.egg-info/SOURCES.txt
+-rw-rw-r--   0 masao     (1000) masao     (1000)        1 2022-06-13 15:27:41.000000 espnet_onnx-0.1.9/espnet_onnx.egg-info/dependency_links.txt
+-rw-rw-r--   0 masao     (1000) masao     (1000)      168 2022-06-13 15:27:41.000000 espnet_onnx-0.1.9/espnet_onnx.egg-info/requires.txt
+-rw-rw-r--   0 masao     (1000) masao     (1000)       12 2022-06-13 15:27:41.000000 espnet_onnx-0.1.9/espnet_onnx.egg-info/top_level.txt
+-rw-rw-r--   0 masao     (1000) masao     (1000)       38 2022-06-13 15:27:42.005035 espnet_onnx-0.1.9/setup.cfg
+-rw-rw-r--   0 masao     (1000) masao     (1000)     1570 2022-06-13 15:26:23.000000 espnet_onnx-0.1.9/setup.py
```

### Comparing `espnet_onnx-0.1.8/LICENSE` & `espnet_onnx-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/PKG-INFO` & `espnet_onnx-0.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: espnet_onnx
-Version: 0.1.8
+Version: 0.1.9
 Summary: ONNX Wrapper for ESPnet
 Home-page: https://github.com/Masao-Someki/espnet_onnx
 Author: Masao Someki
 Author-email: masao.someki@gmail.com
 License: MIT
 Keywords: espnet onnxruntime
 Classifier: Programming Language :: Python
@@ -21,15 +21,15 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # espnet_onnx
 
 ![](https://circleci.com/gh/Masao-Someki/espnet_onnx.svg?style=shield)
 ![](https://img.shields.io/badge/licence-MIT-blue)
-[![](https://img.shields.io/badge/pypi-0.1.8-brightgreen)](https://pypi.org/project/espnet-onnx/)
+[![](https://img.shields.io/badge/pypi-0.1.9-brightgreen)](https://pypi.org/project/espnet-onnx/)
 
 **ESPNet without PyTorch!**
 
 Utility library to easily export espnet models to onnx format.
 There is no need to install PyTorch or ESPNet on your machine if you already have exported files!
 
 ## Install
```

### Comparing `espnet_onnx-0.1.8/README.md` & `espnet_onnx-0.1.9/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # espnet_onnx
 
 ![](https://circleci.com/gh/Masao-Someki/espnet_onnx.svg?style=shield)
 ![](https://img.shields.io/badge/licence-MIT-blue)
-[![](https://img.shields.io/badge/pypi-0.1.8-brightgreen)](https://pypi.org/project/espnet-onnx/)
+[![](https://img.shields.io/badge/pypi-0.1.9-brightgreen)](https://pypi.org/project/espnet-onnx/)
 
 **ESPNet without PyTorch!**
 
 Utility library to easily export espnet models to onnx format.
 There is no need to install PyTorch or ESPNet on your machine if you already have exported files!
 
 ## Install
```

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/abs_asr_model.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/abs_asr_model.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/asr_model.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/asr_model.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/asr_streaming.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/asr_streaming.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/batch_beam_search.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/batch_beam_search.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/batch_beam_search_online_sim.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/batch_beam_search_online_sim.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/beam_search.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/beam_search.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/beam_search_transducer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/beam_search_transducer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/beam_search/hyps.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/beam_search/hyps.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/frontend/frontend.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/frontend/frontend.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/frontend/global_mvn.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/frontend/global_mvn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/frontend/logmel.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/frontend/logmel.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/frontend/stft.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/frontend/stft.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/frontend/utterance_mvn.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/frontend/utterance_mvn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/decoder.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/decoder.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/rnn.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/rnn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/transducer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/transducer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/decoders/xformer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/decoders/xformer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/encoder.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/encoder.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/encoders/streaming.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/encoders/streaming.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/joint_network.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/joint_network.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/lm.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/lm.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/seqrnn_lm.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/seqrnn_lm.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/model/lms/transformer_lm.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/model/lms/transformer_lm.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/build_tokenizer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/build_tokenizer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/token_id_converter.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/token_id_converter.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/char_tokenizer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/char_tokenizer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/phoneme_tokenizer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/phoneme_tokenizer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/sentencepiece_tokenizer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/sentencepiece_tokenizer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/postprocess/tokenizers/word_tokenizer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/postprocess/tokenizers/word_tokenizer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/scorer/ctc_prefix_scorer.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/scorer/ctc_prefix_scorer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/scorer/interface.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/scorer/interface.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/scorer/length_bonus.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/scorer/length_bonus.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/asr/scorer/ngram.py` & `espnet_onnx-0.1.9/espnet_onnx/asr/scorer/ngram.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/export_asr.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/export_asr.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/get_config.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/get_config.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/__init__.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/__init__.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/ctc.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/ctc.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/rnn.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/rnn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/transducer.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/transducer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/decoders/xformer.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/decoders/xformer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/contextual_block_xformer.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/contextual_block_xformer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/rnn.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/rnn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/encoders/xformer.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/encoders/xformer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/joint_network.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/joint_network.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/embed.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/embed.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/seq_rnn.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/seq_rnn.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/asr/models/language_models/transformer.py` & `espnet_onnx-0.1.9/espnet_onnx/export/asr/models/language_models/transformer.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/export_tts.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/export_tts.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/get_config.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/get_config.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/__init__.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/__init__.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/fastspeech2.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/fastspeech2.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/tacotron2.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/tacotron2.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/tts_models/vits.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/tts_models/vits.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/hifigan.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/hifigan.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/melgan.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/melgan.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/parallel_wavegan.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/parallel_wavegan.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/export/tts/models/vocoders/style_melgan.py` & `espnet_onnx-0.1.9/espnet_onnx/export/tts/models/vocoders/style_melgan.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/abs_tts_model.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/abs_tts_model.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/duration_calculator.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/duration_calculator.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/common_processor.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/common_processor.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/korean_cleaner.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/korean_cleaner.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/preprocess/text_cleaner.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/preprocess/text_cleaner.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/fast_speech2.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/fast_speech2.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/tacotron2.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/tacotron2.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/tts_models/vits.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/tts_models/vits.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/griffin_lim.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/griffin_lim.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/model/vocoders/vocoder.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/model/vocoders/vocoder.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/tts/tts_model.py` & `espnet_onnx-0.1.9/espnet_onnx/tts/tts_model.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/utils/abs_model.py` & `espnet_onnx-0.1.9/espnet_onnx/utils/abs_model.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/utils/config.py` & `espnet_onnx-0.1.9/espnet_onnx/utils/config.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/utils/function.py` & `espnet_onnx-0.1.9/espnet_onnx/utils/function.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx/utils/torch_function.py` & `espnet_onnx-0.1.9/espnet_onnx/utils/torch_function.py`

 * *Files identical despite different names*

### Comparing `espnet_onnx-0.1.8/espnet_onnx.egg-info/PKG-INFO` & `espnet_onnx-0.1.9/espnet_onnx.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: espnet-onnx
-Version: 0.1.8
+Version: 0.1.9
 Summary: ONNX Wrapper for ESPnet
 Home-page: https://github.com/Masao-Someki/espnet_onnx
 Author: Masao Someki
 Author-email: masao.someki@gmail.com
 License: MIT
 Keywords: espnet onnxruntime
 Classifier: Programming Language :: Python
@@ -21,15 +21,15 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # espnet_onnx
 
 ![](https://circleci.com/gh/Masao-Someki/espnet_onnx.svg?style=shield)
 ![](https://img.shields.io/badge/licence-MIT-blue)
-[![](https://img.shields.io/badge/pypi-0.1.8-brightgreen)](https://pypi.org/project/espnet-onnx/)
+[![](https://img.shields.io/badge/pypi-0.1.9-brightgreen)](https://pypi.org/project/espnet-onnx/)
 
 **ESPNet without PyTorch!**
 
 Utility library to easily export espnet models to onnx format.
 There is no need to install PyTorch or ESPNet on your machine if you already have exported files!
 
 ## Install
```

### Comparing `espnet_onnx-0.1.8/espnet_onnx.egg-info/SOURCES.txt` & `espnet_onnx-0.1.9/espnet_onnx.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -66,14 +66,17 @@
 espnet_onnx/export/asr/models/encoders/contextual_block_xformer.py
 espnet_onnx/export/asr/models/encoders/rnn.py
 espnet_onnx/export/asr/models/encoders/xformer.py
 espnet_onnx/export/asr/models/language_models/__init__.py
 espnet_onnx/export/asr/models/language_models/embed.py
 espnet_onnx/export/asr/models/language_models/seq_rnn.py
 espnet_onnx/export/asr/models/language_models/transformer.py
+espnet_onnx/export/layers/__init__.py
+espnet_onnx/export/layers/attention.py
+espnet_onnx/export/layers/predecoder.py
 espnet_onnx/export/tts/__init__.py
 espnet_onnx/export/tts/export_tts.py
 espnet_onnx/export/tts/get_config.py
 espnet_onnx/export/tts/models/__init__.py
 espnet_onnx/export/tts/models/tts_models/__init__.py
 espnet_onnx/export/tts/models/tts_models/fastspeech2.py
 espnet_onnx/export/tts/models/tts_models/tacotron2.py
```

### Comparing `espnet_onnx-0.1.8/setup.py` & `espnet_onnx-0.1.9/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -19,15 +19,15 @@
         "espnet",
         "pytest"
     ]
 }
 
 setup(
     name="espnet_onnx",
-    version="0.1.8",
+    version="0.1.9",
     url="https://github.com/Masao-Someki/espnet_onnx",
     author="Masao Someki",
     author_email="masao.someki@gmail.com",
     description="ONNX Wrapper for ESPnet",
     long_description=open("README.md", "r", encoding="utf-8").read(),
     long_description_content_type="text/markdown",
     keywords="espnet onnxruntime",
```

