# Comparing `tmp/nonebot_plugin_spark_gpt-0.1.5.tar.gz` & `tmp/nonebot_plugin_spark_gpt-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_spark_gpt-0.1.5.tar", max compression
+gzip compressed data, was "nonebot_plugin_spark_gpt-0.1.6.tar", max compression
```

## Comparing `nonebot_plugin_spark_gpt-0.1.5.tar` & `nonebot_plugin_spark_gpt-0.1.6.tar`

### file list

```diff
@@ -1,48 +1,98 @@
--rw-r--r--   0        0        0     2191 2023-05-12 11:48:33.428381 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/__init__.py
--rw-r--r--   0        0        0     3177 2023-05-12 05:45:21.846684 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/bard_api.py
--rw-r--r--   0        0        0     3267 2023-05-12 11:44:42.841389 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/bard_func.py
--rw-r--r--   0        0        0     5709 2023-05-12 06:28:47.719071 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/config.py
--rw-r--r--   0        0        0     5252 2023-05-12 12:33:26.769754 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/main.py
--rw-r--r--   0        0        0       16 2023-05-10 17:23:53.939876 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/__init__.py
--rw-r--r--   0        0        0     3919 2023-05-12 11:44:35.835300 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/chatgpt_web_func.py
--rw-r--r--   0        0        0     8228 2023-05-10 17:23:58.319737 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/config.py
--rw-r--r--   0        0        0    27566 2023-05-12 08:19:34.784059 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/main.py
--rw-r--r--   0        0        0     6131 2023-05-10 17:24:01.276809 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/web_api.py
--rw-r--r--   0        0        0       16 2023-05-10 17:24:06.325142 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/__init__.py
--rw-r--r--   0        0        0     3036 2023-05-12 11:43:53.053398 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/claude_func.py
--rw-r--r--   0        0        0     8094 2023-05-10 17:24:09.084792 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/config.py
--rw-r--r--   0        0        0    26120 2023-05-12 08:59:36.615279 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/main.py
--rw-r--r--   0        0        0     4309 2023-05-10 17:24:12.141727 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/slack_api.py
--rw-r--r--   0        0        0       16 2023-05-10 17:24:16.477844 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/__init__.py
--rw-r--r--   0        0        0     2633 2023-05-10 17:24:17.515144 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/common_func.py
--rw-r--r--   0        0        0     6158 2023-05-10 16:32:44.366675 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/config.py
--rw-r--r--   0        0        0     6053 2023-05-11 11:40:42.573933 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/main.py
--rw-r--r--   0        0        0     4066 2023-05-09 11:11:11.036002 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/render.py
--rw-r--r--   0        0        0    18464 2023-05-09 08:51:42.987873 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/github-markdown-light.css
--rw-r--r--   0        0        0  1458204 2023-04-22 14:17:13.496635 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.b64_fonts.css
--rw-r--r--   0        0        0   270288 2023-04-22 14:17:13.497555 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.js
--rw-r--r--   0        0        0     1290 2023-04-22 14:17:13.498611 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/mathtex-script-type.min.js
--rw-r--r--   0        0        0      670 2023-05-09 08:51:13.189256 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/markdown.html
--rw-r--r--   0        0        0     1253 2023-05-09 05:07:59.973080 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/markdown_.html
--rw-r--r--   0        0        0     4625 2023-05-09 09:23:49.857905 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/pygments-default.css
--rw-r--r--   0        0        0    86342 2023-04-22 05:34:37.774678 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/background.png
--rw-r--r--   0        0        0     1137 2023-04-22 05:34:37.774678 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/banner.png
--rw-r--r--   0        0        0    86342 2023-04-22 05:34:37.775678 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/mi_background.png
--rw-r--r--   0        0        0      125 2023-04-22 14:17:13.500554 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/text.css
--rw-r--r--   0        0        0      233 2023-04-22 14:17:13.500554 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/text.html
--rw-r--r--   0        0        0     4381 2023-05-12 12:11:17.703314 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/config.py
--rw-r--r--   0        0        0    18816 2023-05-12 12:12:48.443343 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/main.py
--rw-r--r--   0        0        0     3068 2023-05-12 11:44:56.693243 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/newbing_func.py
--rw-r--r--   0        0        0       16 2023-05-08 03:59:58.447201 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/__init__.py
--rw-r--r--   0        0        0     9719 2023-05-10 14:13:15.440356 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/config.py
--rw-r--r--   0        0        0    30054 2023-05-12 08:22:28.915839 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/main.py
--rw-r--r--   0        0        0    10706 2023-05-08 03:59:52.713874 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/poe_api.py
--rw-r--r--   0        0        0     6332 2023-05-12 11:45:14.325433 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/poe_func.py
--rw-r--r--   0        0        0     2147 2023-05-08 03:59:48.875662 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/pwframework.py
--rw-r--r--   0        0        0     7940 2023-05-11 09:56:25.548175 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/config.py
--rw-r--r--   0        0        0    26574 2023-05-12 09:18:52.703887 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/main.py
--rw-r--r--   0        0        0     4762 2023-05-11 09:15:30.854977 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/spark_api.py
--rw-r--r--   0        0        0     3905 2023-05-12 11:45:35.923235 nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/spark_desk_func.py
--rw-r--r--   0        0        0      920 2023-05-11 13:38:24.229938 nonebot_plugin_spark_gpt-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     3339 2023-05-12 12:21:29.536622 nonebot_plugin_spark_gpt-0.1.5/README.md
--rw-r--r--   0        0        0     4465 1970-01-01 00:00:00.000000 nonebot_plugin_spark_gpt-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     2356 2023-05-12 14:11:45.179341 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/__init__.py
+-rw-r--r--   0        0        0     2817 2023-05-12 07:38:45.037083 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/__pycache__/bard_api.cpython-310.pyc
+-rw-r--r--   0        0        0     2297 2023-05-12 11:49:16.151764 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/__pycache__/bard_func.cpython-310.pyc
+-rw-r--r--   0        0        0     6203 2023-05-12 07:38:45.031063 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0     3980 2023-05-12 08:19:04.601931 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     3177 2023-05-12 05:45:21.846684 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/bard_api.py
+-rw-r--r--   0        0        0     3267 2023-05-12 11:44:42.841389 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/bard_func.py
+-rw-r--r--   0        0        0     5709 2023-05-12 06:28:47.719071 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/config.py
+-rw-r--r--   0        0        0     5351 2023-05-12 08:18:49.873558 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/main.py
+-rw-r--r--   0        0        0       16 2023-05-10 17:23:53.939876 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__init__.py
+-rw-r--r--   0        0        0      217 2023-05-12 12:33:41.114051 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     2850 2023-05-12 12:33:42.376051 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__pycache__/chatgpt_web_func.cpython-310.pyc
+-rw-r--r--   0        0        0     7978 2023-05-12 12:33:41.117052 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    15682 2023-05-12 14:11:55.079018 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     4689 2023-05-12 12:33:42.379058 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/__pycache__/web_api.cpython-310.pyc
+-rw-r--r--   0        0        0     3919 2023-05-12 11:44:35.835300 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/chatgpt_web_func.py
+-rw-r--r--   0        0        0     8228 2023-05-10 17:23:58.319737 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/config.py
+-rw-r--r--   0        0        0    27569 2023-05-12 13:22:10.805761 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/main.py
+-rw-r--r--   0        0        0     6131 2023-05-10 17:24:01.276809 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/web_api.py
+-rw-r--r--   0        0        0       16 2023-05-10 17:24:06.325142 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__init__.py
+-rw-r--r--   0        0        0      218 2023-05-12 12:33:42.688616 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     2155 2023-05-12 12:33:42.910715 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__pycache__/claude_func.cpython-310.pyc
+-rw-r--r--   0        0        0     7737 2023-05-12 12:33:42.690616 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    15270 2023-05-13 06:31:33.550204 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     3162 2023-05-12 12:33:42.913715 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/__pycache__/slack_api.cpython-310.pyc
+-rw-r--r--   0        0        0     3036 2023-05-12 11:43:53.053398 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/claude_func.py
+-rw-r--r--   0        0        0     8094 2023-05-10 17:24:09.084792 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/config.py
+-rw-r--r--   0        0        0    26134 2023-05-13 06:31:13.147392 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/main.py
+-rw-r--r--   0        0        0     4309 2023-05-10 17:24:12.141727 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/slack_api.py
+-rw-r--r--   0        0        0       16 2023-05-10 17:24:16.477844 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/__init__.py
+-rw-r--r--   0        0        0      212 2023-05-12 12:33:40.562416 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     2408 2023-05-12 14:11:54.728124 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/__pycache__/common_func.cpython-310.pyc
+-rw-r--r--   0        0        0     6937 2023-05-12 14:11:54.313051 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0     5005 2023-05-12 14:11:55.391701 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     2636 2023-05-12 13:22:10.807761 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/common_func.py
+-rw-r--r--   0        0        0     6299 2023-05-12 14:09:56.253829 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/config.py
+-rw-r--r--   0        0        0     6056 2023-05-12 13:22:10.808762 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/main.py
+-rw-r--r--   0        0        0     3970 2023-05-13 06:17:37.884666 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/__pycache__/render.cpython-310.pyc
+-rw-r--r--   0        0        0     4118 2023-05-13 06:17:21.388185 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/render.py
+-rw-r--r--   0        0        0    18464 2023-05-09 08:51:42.987873 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/github-markdown-light.css
+-rw-r--r--   0        0        0  1458204 2023-04-22 14:17:13.496635 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.b64_fonts.css
+-rw-r--r--   0        0        0   270288 2023-04-22 14:17:13.497555 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.js
+-rw-r--r--   0        0        0     1290 2023-04-22 14:17:13.498611 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/mathtex-script-type.min.js
+-rw-r--r--   0        0        0      670 2023-05-09 08:51:13.189256 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/markdown.html
+-rw-r--r--   0        0        0     1253 2023-05-09 05:07:59.973080 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/markdown_.html
+-rw-r--r--   0        0        0     4625 2023-05-09 09:23:49.857905 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/pygments-default.css
+-rw-r--r--   0        0        0    86342 2023-04-22 05:34:37.774678 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/background.png
+-rw-r--r--   0        0        0     1137 2023-04-22 05:34:37.774678 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/banner.png
+-rw-r--r--   0        0        0    86342 2023-04-22 05:34:37.775678 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/mi_background.png
+-rw-r--r--   0        0        0      125 2023-04-22 14:17:13.500554 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/text.css
+-rw-r--r--   0        0        0      233 2023-04-22 14:17:13.500554 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/text.html
+-rw-r--r--   0        0        0     5101 2023-05-12 12:33:41.513051 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    11884 2023-05-13 06:17:37.422608 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     2236 2023-05-12 12:33:41.510052 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/__pycache__/newbing_func.cpython-310.pyc
+-rw-r--r--   0        0        0     4381 2023-05-12 12:11:17.703314 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/config.py
+-rw-r--r--   0        0        0    18888 2023-05-13 06:16:25.243685 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/main.py
+-rw-r--r--   0        0        0     3068 2023-05-12 11:44:56.693243 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/newbing_func.py
+-rw-r--r--   0        0        0       16 2023-05-08 03:59:58.447201 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/__init__.py
+-rw-r--r--   0        0        0     9719 2023-05-10 14:13:15.440356 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/config.py
+-rw-r--r--   0        0        0    30054 2023-05-12 08:22:28.915839 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/main.py
+-rw-r--r--   0        0        0    10706 2023-05-08 03:59:52.713874 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/poe_api.py
+-rw-r--r--   0        0        0     6332 2023-05-12 11:45:14.325433 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/poe_func.py
+-rw-r--r--   0        0        0     2147 2023-05-08 03:59:48.875662 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/pwframework.py
+-rw-r--r--   0        0        0       16 2023-05-08 03:59:58.447201 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__init__.py
+-rw-r--r--   0        0        0      209 2023-05-12 12:33:40.538417 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     8409 2023-05-13 03:43:07.824443 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    17634 2023-05-13 04:17:09.906260 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     1498 2023-05-13 03:20:10.311812 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/poe_api.cpython-310.pyc
+-rw-r--r--   0        0        0     3842 2023-05-12 14:17:14.955455 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/poe_func.cpython-310.pyc
+-rw-r--r--   0        0        0     2246 2023-05-12 12:33:40.699419 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/__pycache__/pwframework.cpython-310.pyc
+-rw-r--r--   0        0        0     9735 2023-05-13 03:43:00.875513 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/config.py
+-rw-r--r--   0        0        0    29816 2023-05-13 04:16:52.625972 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/main.py
+-rw-r--r--   0        0        0     1324 2023-05-13 03:20:05.948500 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/poe_api.py
+-rw-r--r--   0        0        0     4664 2023-05-12 14:16:58.307681 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/poe_func.py
+-rw-r--r--   0        0        0     2147 2023-05-08 03:59:48.875662 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_http/pwframework.py
+-rw-r--r--   0        0        0       16 2023-05-08 03:59:58.447201 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__init__.py
+-rw-r--r--   0        0        0      209 2023-05-12 12:33:40.538417 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     8386 2023-05-12 12:33:40.547409 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    17531 2023-05-12 12:33:40.543409 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     6350 2023-05-12 12:33:41.126052 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/poe_api.cpython-310.pyc
+-rw-r--r--   0        0        0     5078 2023-05-12 12:33:40.577417 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/poe_func.cpython-310.pyc
+-rw-r--r--   0        0        0     2246 2023-05-12 12:33:40.699419 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/__pycache__/pwframework.cpython-310.pyc
+-rw-r--r--   0        0        0     9719 2023-05-10 14:13:15.440356 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/config.py
+-rw-r--r--   0        0        0    30054 2023-05-12 08:22:28.915839 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/main.py
+-rw-r--r--   0        0        0    10706 2023-05-08 03:59:52.713874 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/poe_api.py
+-rw-r--r--   0        0        0     6332 2023-05-12 11:45:14.325433 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/poe_func.py
+-rw-r--r--   0        0        0     2147 2023-05-08 03:59:48.875662 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe_pw/pwframework.py
+-rw-r--r--   0        0        0     7685 2023-05-12 12:33:42.698615 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0    15429 2023-05-12 14:14:22.795930 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/__pycache__/main.cpython-310.pyc
+-rw-r--r--   0        0        0     4381 2023-05-12 12:33:43.326776 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/__pycache__/spark_api.cpython-310.pyc
+-rw-r--r--   0        0        0     2716 2023-05-12 12:33:43.324777 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/__pycache__/spark_desk_func.cpython-310.pyc
+-rw-r--r--   0        0        0     7940 2023-05-11 09:56:25.548175 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/config.py
+-rw-r--r--   0        0        0    26577 2023-05-12 13:22:10.805761 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/main.py
+-rw-r--r--   0        0        0     4762 2023-05-11 09:15:30.854977 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/spark_api.py
+-rw-r--r--   0        0        0     3905 2023-05-12 11:45:35.923235 nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/spark_desk_func.py
+-rw-r--r--   0        0        0      940 2023-05-13 06:44:33.373393 nonebot_plugin_spark_gpt-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0     3339 2023-05-12 12:21:29.536622 nonebot_plugin_spark_gpt-0.1.6/README.md
+-rw-r--r--   0        0        0     4505 1970-01-01 00:00:00.000000 nonebot_plugin_spark_gpt-0.1.6/PKG-INFO
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/__init__.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/__init__.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,18 @@
 import nonebot
 
-from .poe import main
 from .newbing import main
 from .chatgpt_web import main
 from .common import main
+from .common.config import spark_persistor
+if spark_persistor.poe_api_mode == 0:
+    from .poe_http import main
+elif spark_persistor.poe_api_mode == 1:
+    from .poe_pw import main
+
 from .claude_slack import main
 from .Spark_desk import main
 from .bard import main
 from nonebot.matcher import Matcher
 from nonebot.plugin import PluginMetadata
 from nonebot.adapters.onebot.v11 import (
     Event,
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/bard_api.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/bard_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/bard_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/bard_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/bard/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/bard/main.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 import json
 from pathlib import Path
 import re
 from nonebot import logger
 from nonebot.plugin import on_command, on_message
+from nonebot.params import ArgStr, CommandArg
+from nonebot.typing import T_State
 from nonebot.matcher import Matcher
 from nonebot.adapters.onebot.v11 import (
     Message,
     Event,
     Bot,
     MessageEvent,
     MessageSegment,
 )
 from .bard_func import is_useable, sendmsg
-from .config import BotInfo, BardTemper, set_userdata
+from .config import BotInfo, bard_persistor, BardTemper, set_userdata
 from ..common.render.render import md_to_pic
 from ..common.common_func import reply_out
 from .bard_api import bardchat
 
 logger.info("开始加载Bard")
 bardtemper = BardTemper()
 user_data_dict = bardtemper.user_data_dict
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/chatgpt_web_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/chatgpt_web_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/main.py`

 * *Files 0% similar despite different names*

```diff
@@ -20,15 +20,15 @@
     get_user_info_and_data,
     set_userdata,
 )
 from .chatgpt_web_func import sendmsg
 from .web_api import gptweb_api
 from ..common.config import spark_persistor
 from ..common.common_func import delete_messages, reply_out
-from ..poe.config import poe_persistor
+from ..poe_pw.config import poe_persistor
 from nonebot import logger
 
 # 初始化两个需要使用的实例
 temp_data = GPT_webTemper()
 user_data_dict = temp_data.user_data_dict
 msg_bot_bidict = temp_data.msg_bot_bidict
 prompts_dict = spark_persistor.prompts_dict
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/chatgpt_web/web_api.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/chatgpt_web/web_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/claude_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/claude_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/main.py`

 * *Files 1% similar despite different names*

```diff
@@ -20,15 +20,15 @@
     get_user_info_and_data,
     set_userdata,
 )
 from .claude_func import reply_out, sendmsg
 from .slack_api import claude_chat
 from ..common.config import spark_persistor
 from ..common.common_func import delete_messages
-from ..poe.config import poe_persistor
+from ..poe_pw.config import poe_persistor
 from nonebot import logger
 
 # 初始化两个需要使用的实例
 temp_data = Claude_slack_Temper()
 user_data_dict = temp_data.user_data_dict
 msg_bot_bidict = temp_data.msg_bot_bidict
 prompts_dict = spark_persistor.prompts_dict
@@ -345,21 +345,22 @@
     if temp == "none":
         current_userinfo, current_userdata = set_userdata(event, user_data_dict)
         if current_userdata.is_waiting:
             await matcher.finish(reply_out(event, "你已经有一个请求进行中了，请等结束后再发送"))
         nickname = "cdefault"
         prompt_nickname = claude_slack_persistor.auto_prompt
         prompt = prompts_dict[prompt_nickname]
-        raw_message = (
+        raw_message =  (
             str(event.message)
             .replace("/ctalk ", "")
             .replace("/ctalk", "")
             .replace("/ct ", "")
             .replace("/ct", "")
         )
+        
         botinfo = BotInfo(
             nickname=nickname,
             time_stamp="",
             thread_ts="",
             source="claude_slack",
             prompt_nickname=prompt_nickname,
             prompt=prompt,
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/claude_slack/slack_api.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/claude_slack/slack_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/common_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/common_func.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import asyncio
 from typing import Union
 
 import aiohttp
-from ..poe.config import poe_persistor
+from ..poe_pw.config import poe_persistor
 from ..chatgpt_web.config import gptweb_persistor
 from nonebot_plugin_guild_patch import GuildMessageEvent
 from nonebot.adapters.onebot.v11 import Message, MessageEvent, MessageSegment
 
 
 def is_auto_prompt(prompt_nickname):
     if prompt_nickname in [gptweb_persistor.auto_prompt, poe_persistor.auto_prompt]:
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/config.py`

 * *Files 2% similar despite different names*

```diff
@@ -132,14 +132,16 @@
 # 储存spark的持久数据,提供一键保存和加载功能
 class SparkPersistor(BaseModel):
     path_: str = str(Path()) + "/data/spark_gpt/spark_data.json"
     pic_able: str = None
     url_able: str = "True"
     suggest_able: str = "True"
     num_limit: int = 350
+    #0为http版，1为playwright版本
+    poe_api_mode: int = 0
     superusers: List[str] = []
     blacklist: List[str] = []
     whitelist: List[str] = []
     mode: str = "black"
     prompts_dict: Dict[str, str] = {
         "猫娘": "现在你将模仿一只猫娘，与我对话每一句话后面都要加上“喵”，如果你能明白我的意思，请回复“喵~你好主人”",
         "默认": "你是一个ai语言模型",
@@ -170,14 +172,15 @@
         )
         self.mode = (
             get_config.spark_mode
             if hasattr(get_config, "spark_mode")
             and get_config.spark_mode in ["white", "black"]
             else self.mode
         )
+        self.poe_api_mode = int(getattr(get_config, "poe_api_mode", 0))
         self.pic_able = getattr(get_config, "spark_picable", None)
         self.url_able = getattr(get_config, "spark_urlable", "True")
         self.suggest_able = getattr(get_config, "spark_suggestable", "True")
         self.num_limit = int(getattr(get_config, "spark_limit", 350))
         self.save()
 
     def save(self):
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/main.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from nonebot.adapters.onebot.v11 import Event, Message,MessageSegment
 from nonebot.params import ArgStr, CommandArg
 from .render.render import md_to_pic
 from .common_func import reply_out
 from .config import spark_persistor, get_user_info_and_data
 from .common_func import is_auto_prompt
 from ..chatgpt_web.config import gptweb_persistor
-from ..poe.config import poe_persistor
+from ..poe_pw.config import poe_persistor
 from ..claude_slack.config import claude_slack_persistor
 from ..Spark_desk.config import spark_desk_persistor
 spark_addprompt = on_command("添加预设", aliases={"ap"}, priority=4, block=False)
 
 
 @spark_addprompt.handle()
 async def __spark_addprompt__(matcher: Matcher, event: Event):
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/render.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/render.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from typing import Union, Literal
 from pathlib import Path
 import jinja2
 import aiofiles
 import markdown
 import pymdownx
 from nonebot.log import logger
-from ...poe.pwframework import pwfw
+from ...poe_pw.pwframework import pwfw
 
 TEMPLATES_PATH = str(Path(__file__).parent / "templates")
 
 env = jinja2.Environment(
     extensions=["jinja2.ext.loopcontrols"],
     loader=jinja2.FileSystemLoader(TEMPLATES_PATH),
     enable_async=True,
@@ -37,14 +37,16 @@
     """
     template = env.get_template("markdown.html")
     if not md:
         if md_path:
             md = await read_file(md_path)
         else:
             raise Exception("必须输入 md 或 md_path")
+    else:
+        md = md.replace("\n","  \n")
     # logger.debug(md)
     md = markdown.markdown(
         md,
         extensions=[
             "pymdownx.tasklist",
             "tables",
             "fenced_code",
```

#### html2text {}

```diff
@@ -1,28 +1,28 @@
 from os import getcwd import re from typing import Union, Literal from pathlib
 import Path import jinja2 import aiofiles import markdown import pymdownx from
-nonebot.log import logger from ...poe.pwframework import pwfw TEMPLATES_PATH =
-str(Path(__file__).parent / "templates") env = jinja2.Environment( extensions=
-["jinja2.ext.loopcontrols"], loader=jinja2.FileSystemLoader(TEMPLATES_PATH),
-enable_async=True, ) async def md_to_pic( md: str = "", md_path: str = "",
-css_path: str = "", type: Literal["jpeg", "png"] = "png", quality: Union[int,
-None] = None, ) -> bytes: """markdown è½¬ å¾ç Args: md (str, optional):
-markdown æ ¼å¼ææ¬ md_path (str, optional): markdown æä»¶è·¯å¾ css_path
-(str, optional): cssæä»¶è·¯å¾. Defaults to None. type (Literal["jpeg",
-"png"]): å¾çç±»å, é»è®¤ png quality (int, optional): å¾çè´¨é 0-100
-å½ä¸º`png`æ¶æ æ Returns: bytes: å¾ç, å¯ç´æ¥åé """ template =
-env.get_template("markdown.html") if not md: if md_path: md = await read_file
-(md_path) else: raise Exception("å¿é¡»è¾å¥ md æ md_path") # logger.debug
-(md) md = markdown.markdown( md, extensions=[ "pymdownx.tasklist", "tables",
-"fenced_code", "codehilite", "mdx_math", "pymdownx.tilde", ],
-extension_configs={"mdx_math": {"enable_dollar_delimiter": True}}, ) #
-logger.debug(md) extra = "" if "math/tex" in md: katex_css = await read_tpl
-("katex/katex.min.b64_fonts.css") katex_js = await read_tpl("katex/
-katex.min.js") mathtex_js = await read_tpl("katex/mathtex-script-type.min.js")
-extra = ( f'
+nonebot.log import logger from ...poe_pw.pwframework import pwfw TEMPLATES_PATH
+= str(Path(__file__).parent / "templates") env = jinja2.Environment
+( extensions=["jinja2.ext.loopcontrols"], loader=jinja2.FileSystemLoader
+(TEMPLATES_PATH), enable_async=True, ) async def md_to_pic( md: str = "",
+md_path: str = "", css_path: str = "", type: Literal["jpeg", "png"] = "png",
+quality: Union[int, None] = None, ) -> bytes: """markdown è½¬ å¾ç Args: md
+(str, optional): markdown æ ¼å¼ææ¬ md_path (str, optional): markdown
+æä»¶è·¯å¾ css_path (str, optional): cssæä»¶è·¯å¾. Defaults to None. type
+(Literal["jpeg", "png"]): å¾çç±»å, é»è®¤ png quality (int, optional):
+å¾çè´¨é 0-100 å½ä¸º`png`æ¶æ æ Returns: bytes: å¾ç, å¯ç´æ¥åé
+""" template = env.get_template("markdown.html") if not md: if md_path: md =
+await read_file(md_path) else: raise Exception("å¿é¡»è¾å¥ md æ md_path")
+else: md = md.replace("\n"," \n") # logger.debug(md) md = markdown.markdown
+( md, extensions=[ "pymdownx.tasklist", "tables", "fenced_code", "codehilite",
+"mdx_math", "pymdownx.tilde", ], extension_configs={"mdx_math":
+{"enable_dollar_delimiter": True}}, ) # logger.debug(md) extra = "" if "math/
+tex" in md: katex_css = await read_tpl("katex/katex.min.b64_fonts.css")
+katex_js = await read_tpl("katex/katex.min.js") mathtex_js = await read_tpl
+("katex/mathtex-script-type.min.js") extra = ( f'
 ' f"
 " f"
 " ) if css_path: css = await read_file(css_path) else: css = await read_tpl
 ("github-markdown-light.css") + await read_tpl( "pygments-default.css" ) return
 await html_to_pic( template_path=f"file://{css_path if css_path else
 TEMPLATES_PATH}", html=await template.render_async(md=md, css=css,
 extra=extra), type=type, quality=quality, ) async def html_to_pic( html: str,
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/github-markdown-light.css` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/github-markdown-light.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.b64_fonts.css` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.b64_fonts.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.js` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/katex.min.js`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/katex/mathtex-script-type.min.js` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/katex/mathtex-script-type.min.js`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/markdown.html` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/markdown.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/markdown_.html` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/markdown_.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/pygments-default.css` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/pygments-default.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/background.png` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/background.png`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/banner.png` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/banner.png`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/common/render/templates/source/mi_background.png` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/common/render/templates/source/mi_background.png`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/main.py`

 * *Files 1% similar despite different names*

```diff
@@ -189,17 +189,16 @@
     try:
         max_num = raw_json["item"]["throttling"]["maxNumUserMessagesInConversation"]
         now_num = raw_json["item"]["throttling"]["numUserMessagesInConversation"]
         reply = raw_json["item"]["messages"][1]["text"]
         reply = reply.replace("&#91;","[").replace("&#93;","]").replace("[^","[").replace("^]","]")
     except:
         await matcher.finish(reply_out(event, "出错喽，多次重试都出错的话，联系机器人主人"))
-    reply = reply.replace("\n","\n  ")
     ##纯文本正文部分
-    msg_text = reply + "  \n"
+    msg_text = reply + "\n"
     
     #尝试解析图片或其他资源
     try:
         forward_msg = None
         html_resource = ""
         image_sources = [
             a["seeMoreUrl"]
@@ -216,30 +215,30 @@
             for a in raw_json["item"]["messages"][1]["sourceAttributions"]
             if "imageLink" in a
         ]
         for i in range(len(image_sources)):
             source_link = image_sources[i]
             display_name = image_names[i]
             each_msg = MessageSegment.text(f"[{i+1}] {display_name}:\n{source_link}\n")
-            html_each_msg = f"[{i+1}]:<a href=\"{source_link}\">{display_name}</a>  \n"
+            html_each_msg = f"[{i+1}]:<a href=\"{source_link}\">{display_name}</a>\n"
             if len(image_links) - i>0:
                 image_link = image_links[i]
                 each_msg += MessageSegment.image(image_link)
-                html_each_msg += f"<img src={image_link} alt={i+1}>  \n"
+                html_each_msg += f"<img src={image_link} alt={i+1}>\n"
             forward_msg += MessageSegment.node_custom(
                 user_id=current_userdata.sender.user_id,
                 nickname=current_userdata.sender.user_name,
                 content=each_msg,
             )
             html_resource += html_each_msg
     except:
         pass
     
     ##处理建议回复
-    suggest_str = "  \n建议回复:  \n"
+    suggest_str = "\n建议回复:\n"
     if newbing_persistor.suggest_able == "True":
         try:
             suggests = [
                 raw_json["item"]["messages"][1]["suggestedResponses"][i]["text"]
                 for i in range(
                     len(raw_json["item"]["messages"][1]["suggestedResponses"])
                 )
@@ -390,23 +389,25 @@
             else:
                 logger.warning("newbing的cookie内容有误,无法使用，跳过")
                 await matcher.finish()
     except FileNotFoundError:
         logger.warning("newbing cookie未配置,无法使用，跳过")
         await matcher.finish()
     current_userdata.is_waiting = True
+    from pathlib import Path
+
     try:
         async with ImageGenAsync(auth_cookie) as image_generator:
             image_links = await image_generator.get_images(prompt)
             max_retry = 3  # 最大重试次数
             retry_count = 0  # 当前重试次数
             while retry_count < max_retry:
                 try:
-                    temp_path = "./data/spark_gpt/temp/"
-                    jpeg_files = list(Path(temp_path).glob("*.jpeg"))
+                    temp_path = Path("./data/spark_gpt/temp/")
+                    jpeg_files = list(temp_path.glob("*.jpeg"))
                     # 删除所有JPEG格式的文件
                     for file_path in jpeg_files:
                         file_path.unlink()
 
                     await image_generator.save_images(image_links, temp_path)
                     break  # 如果保存成功，则跳出循环
                 except Exception as e:
@@ -425,21 +426,22 @@
         forward_msg = MessageSegment.node_custom(
             user_id=current_userdata.sender.user_id,
             nickname=current_userdata.sender.user_name,
             content=MessageSegment.text("绘图结果如下:\n"),
         )
         image_msg = MessageSegment.text("绘图结果如下:\n")
         for i in range(4):
-            image_msg += MessageSegment.image(Path(temp_path + f"{i}.jpeg"))
+            image_msg += MessageSegment.image(temp_path / f"{i}.jpeg")
             forward_msg += MessageSegment.node_custom(
                 user_id=current_userdata.sender.user_id,
                 nickname=current_userdata.sender.user_name,
-                content=MessageSegment.image(Path(temp_path + f"{i}.jpeg")),
+                content=MessageSegment.image(temp_path / f"{i}.jpeg"),
             )
-
+    except Exception as e:
+        await matcher.finish(reply_out(event, f"发送图片出错: {e}"))
     except:
         await matcher.finish(reply_out(event, "发送失败，多次失败请联系机器人主人"))
     try:
         # 尝试合并转发
         if forward_msg and event.message_type == "group":
             await bot.send_group_forward_msg(
                 group_id=event.group_id, messages=forward_msg
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/newbing/newbing_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/newbing/newbing_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/main.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/poe_api.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/poe_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/poe_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/poe_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/poe/pwframework.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/poe/pwframework.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/config.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/main.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/main.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
     spark_desk_persistor,
     get_user_info_and_data,
     set_userdata,
 )
 from .spark_api import sparkchat
 from ..common.config import spark_persistor
 from ..common.common_func import delete_messages, reply_out
-from ..poe.config import poe_persistor
+from ..poe_pw.config import poe_persistor
 from nonebot import logger
 
 # 初始化两个需要使用的实例
 temp_data = Spark_DeskTemper()
 user_data_dict = temp_data.user_data_dict
 msg_bot_bidict = temp_data.msg_bot_bidict
 prompts_dict = spark_persistor.prompts_dict
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/spark_api.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/spark_api.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/nonebot_plugin_spark_gpt/Spark_desk/spark_desk_func.py` & `nonebot_plugin_spark_gpt-0.1.6/nonebot_plugin_spark_gpt/Spark_desk/spark_desk_func.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/pyproject.toml` & `nonebot_plugin_spark_gpt-0.1.6/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot_plugin_spark_gpt"
-version = "0.1.5"
+version = "0.1.6"
 description = "Spark-GPT,将多来源的gpt接入qq及更多平台,使用便捷,管理完善,功能强大"
 authors = ["canxin121 <1969730106@qq.com>"]
 readme = "README.md"
 packages = [{include = "nonebot_plugin_spark_gpt"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
@@ -20,14 +20,15 @@
 nonebot-plugin-guild-patch = "*"
 playwright = "^1.33.0"
 pydantic = "^1.10.7"
 nonebot-adapter-onebot = { version = "^2.0.0-beta.1", optional = true }
 pymdown-extensions = "^9.11"
 python-markdown-math = "^0.8"
 slack-sdk = "^3.21.3"
+poe-api = "^0.3.1"
 
 [tool.poetry.extras]
 onebot = ["nonebot-adapter-onebot"]
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `nonebot_plugin_spark_gpt-0.1.5/README.md` & `nonebot_plugin_spark_gpt-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-0.1.5/PKG-INFO` & `nonebot_plugin_spark_gpt-0.1.6/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-spark-gpt
-Version: 0.1.5
+Version: 0.1.6
 Summary: Spark-GPT,将多来源的gpt接入qq及更多平台,使用便捷,管理完善,功能强大
 Author: canxin121
 Author-email: 1969730106@qq.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
@@ -17,14 +17,15 @@
 Requires-Dist: imagegen (>=0.2,<0.3)
 Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
 Requires-Dist: markdown (>=3.4.3,<4.0.0)
 Requires-Dist: nonebot-adapter-onebot (>=2.0.0-beta.1,<3.0.0) ; extra == "onebot"
 Requires-Dist: nonebot-plugin-guild-patch
 Requires-Dist: nonebot2 (>=2.0.0-beta.1,<3.0.0)
 Requires-Dist: playwright (>=1.33.0,<2.0.0)
+Requires-Dist: poe-api (>=0.3.1,<0.4.0)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
 Requires-Dist: pymdown-extensions (>=9.11,<10.0)
 Requires-Dist: python-markdown-math (>=0.8,<0.9)
 Requires-Dist: slack-sdk (>=3.21.3,<4.0.0)
 Description-Content-Type: text/markdown
 
 <div align="center">
```

#### html2text {}

```diff
@@ -1,24 +1,24 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-spark-gpt Version: 0.1.5 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-spark-gpt Version: 0.1.6 Summary:
 Spark-
 GPT,å°å¤æ¥æºçgptæ¥å¥qqåæ´å¤å¹³å°,ä½¿ç¨ä¾¿æ·,ç®¡çå®å,åè½å¼ºå¤§
 Author: canxin121 Author-email: 1969730106@qq.com Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3 Classifier: Programming
 Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: onebot Requires-Dist: aiofiles (>=23.1.0,<24.0.0) Requires-
 Dist: aiohttp (>=3.8.4,<4.0.0) Requires-Dist: bidict (>=0.22.1,<0.23.0)
 Requires-Dist: edgegpt (>=0.3.6,<0.4.0) Requires-Dist: httpx (>=0.24.0,<0.25.0)
 Requires-Dist: imagegen (>=0.2,<0.3) Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
 Requires-Dist: markdown (>=3.4.3,<4.0.0) Requires-Dist: nonebot-adapter-onebot
 (>=2.0.0-beta.1,<3.0.0) ; extra == "onebot" Requires-Dist: nonebot-plugin-
 guild-patch Requires-Dist: nonebot2 (>=2.0.0-beta.1,<3.0.0) Requires-Dist:
-playwright (>=1.33.0,<2.0.0) Requires-Dist: pydantic (>=1.10.7,<2.0.0)
-Requires-Dist: pymdown-extensions (>=9.11,<10.0) Requires-Dist: python-
-markdown-math (>=0.8,<0.9) Requires-Dist: slack-sdk (>=3.21.3,<4.0.0)
-Description-Content-Type: text/markdown
+playwright (>=1.33.0,<2.0.0) Requires-Dist: poe-api (>=0.3.1,<0.4.0) Requires-
+Dist: pydantic (>=1.10.7,<2.0.0) Requires-Dist: pymdown-extensions
+(>=9.11,<10.0) Requires-Dist: python-markdown-math (>=0.8,<0.9) Requires-Dist:
+slack-sdk (>=3.21.3,<4.0.0) Description-Content-Type: text/markdown
                 [https://socialify.git.ci/canxin121/Spark-GPT/
 image?font=Raleway&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcanxin121.github.io%2Fdocs%2Flogo.png&name=1&owner=1&pattern=Charlie%20Brown&pulls=1&stargazers=1&theme=Auto]
                             ****** Spark-GPT ******
                                    Spark-GPT
                             [pypi] [python] [pypi]
                                [onebot]_[github]
 --- [![æ®å¿å°ç«-ææ¡£åº](https://github.com/canxin121/Spark-GPT/blob/
```

