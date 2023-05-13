# Comparing `tmp/nonebot_plugin_tuan_chatgpt-0.3.3rc1.tar.gz` & `tmp/nonebot_plugin_tuan_chatgpt-0.4.0b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_tuan_chatgpt-0.3.3rc1.tar", max compression
+gzip compressed data, was "nonebot_plugin_tuan_chatgpt-0.4.0b1.tar", max compression
```

## Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1.tar` & `nonebot_plugin_tuan_chatgpt-0.4.0b1.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1063 2023-04-06 00:49:24.890049 nonebot_plugin_tuan_chatgpt-0.3.3rc1/LICENSE.md
--rw-r--r--   0        0        0    16275 2023-04-06 00:49:24.890049 nonebot_plugin_tuan_chatgpt-0.3.3rc1/README.md
--rw-r--r--   0        0        0     7099 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/__init__.py
--rw-r--r--   0        0        0     1901 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/config.py
--rw-r--r--   0        0        0      729 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/perf_timer.py
--rw-r--r--   0        0        0    17746 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/text_to_img.py
--rw-r--r--   0        0        0    15282 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/utils.py
--rw-r--r--   0        0        0      577 2023-04-06 00:49:25.206047 nonebot_plugin_tuan_chatgpt-0.3.3rc1/pyproject.toml
--rw-r--r--   0        0        0    17257 1970-01-01 00:00:00.000000 nonebot_plugin_tuan_chatgpt-0.3.3rc1/PKG-INFO
+-rw-r--r--   0        0        0     1063 2023-05-13 01:12:30.653881 nonebot_plugin_tuan_chatgpt-0.4.0b1/LICENSE.md
+-rw-r--r--   0        0        0    16966 2023-05-13 01:12:30.653881 nonebot_plugin_tuan_chatgpt-0.4.0b1/README.md
+-rw-r--r--   0        0        0     8709 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/__init__.py
+-rw-r--r--   0        0        0     2146 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/config.py
+-rw-r--r--   0        0        0      729 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/perf_timer.py
+-rw-r--r--   0        0        0    17746 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/text_to_img.py
+-rw-r--r--   0        0        0    24940 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/utils.py
+-rw-r--r--   0        0        0      580 2023-05-13 01:12:30.937884 nonebot_plugin_tuan_chatgpt-0.4.0b1/pyproject.toml
+-rw-r--r--   0        0        0    17947 1970-01-01 00:00:00.000000 nonebot_plugin_tuan_chatgpt-0.4.0b1/PKG-INFO
```

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/LICENSE.md` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/LICENSE.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/README.md` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -54,44 +54,52 @@
 <!--  ![聊天效果](example2.png)  -->
 ![聊天效果](https://raw.githubusercontent.com/TheLZY/nonebot_plugin_tuan_chatgpt/master/examples/example2.png)
 
 
 ## 🎉 使用
 
 ### 指令表
+注意：指令中的团子根据设置的nickname为准。也可以通过 @团子 代替。
+
+现在没有默认触发词了，如果没有设置nickname，就只能通过 @ 触发了
+
+指令的相同触发词可自行查看代码中 aliases 部分。
+
+
 
 | 指令 | 权限 | 需要@ | 范围 | 说明 |
 |:-----:|:----:|:----:|:----:|:----:|
 | 团子[聊天内容] | 群员 | 否 | 群聊 / 私聊 | 来和团子聊天吧！ |
 | @团子[聊天内容] | 同上 |  是 | 同上 | 同上 |
-| 团子看看位置 | 群员 | 否 | 群聊 / 私聊 | 查看团子赛博地址 |
-| 历史记录 | 主人 | 否 | 群聊 / 私聊 | 查看历史提问（不包括回答） |
+| 团子 看看位置 / 你在哪儿 | 群员 | 否 | 群聊 / 私聊 | 查看团子赛博地址 |
+| 团子 历史记录 / history | 主人 | 否 | 群聊 / 私聊 | 查看历史提问（不包括回答） |
+| 团子 清除记忆 / 清除历史记录 | 主人 | 否 | 群聊 / 私聊 | 清除团子的记忆 |
 
 
 
 ## 💿 安装
 
 
 <details>
 
 <summary>使用 nb-cli 安装</summary>
 
 ```
 nb plugin install nonebot-plugin-tuan-chatgpt
+
+# 升级：
+nb plugin update nonebot-plugin-tuan-chatgpt
 ```
 
 </details>
 
 
 <details>
 
-<summary>使用 git 安装 （ 推荐 ）</summary>
-
-
-推荐此方式，因为能够及时收到更新
+<summary>使用 git 安装 </summary>
 
 安装：在 nonebot2 项目的插件目录下, 打开命令行, 使用 git 安装
 
 ```
 git clone https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git
 ```
 升级：
@@ -111,15 +119,15 @@
 ```
 
 </details>
 
 
 环境配置：
 
-打开nonebot的`.env` 文件，写入您的 `chatgpt_api`
+打开nonebot的`.env` 文件，写入您的 `chatgpt_api` 以及 `nickname`
 
 如果希望启用代理，则需要在`.env` 文件中，写入 `chat_use_proxy = True` 以及 `chat_proxy_address_https = "代理地址"` 或 `chat_proxy_address_http = "代理地址"`  (处理逻辑类似openai，优先使用https。但是https经常会报错（aiohttp和urllib3都可能会造成问题），推荐只使用http)
 
 如果希望启用api转发 (类似 [腾讯云函数搭建 OpenAI 国内代理](https://github.com/Ice-Hazymoon/openai-scf-proxy) 通过云函数等方式实现反代 )，则需要写入写入 `chat_use_api_forward = True` 以及 `chat_api_address = "代理地址"` 
 
 但是不推荐两者同时启用
 
@@ -130,14 +138,15 @@
 图片渲染功能启用后，会自动启用二维码添加以及背景图片添加。可以选择关闭。
 
 具体配置方式参考 **⚙️ 配置** 以及 [配置 | Nonebot](https://v2.nonebot.dev/docs/tutorial/configuration#%E9%85%8D%E7%BD%AE%E6%96%B9%E5%BC%8F)
 
 eg： 
 
     chatgpt_api = "sk-1145141919"
+    nickname = ['团子', '雷姆']
     # 启用代理
     chat_use_proxy=True
     chat_proxy_address_http='http://127.0.0.1:10809'
     chat_proxy_address_https='http://127.0.0.1:10809'
     # 启用api转发
     chat_use_api_forward=True
     chat_api_address="https://api.openai.com/v1" （这个是官方接口 照着写没问题，大概？ 还是得看具体的转发方式）
@@ -158,14 +167,17 @@
 
 在 nonebot2 项目的`.env`文件中支持添加以下配置
 
 必填项：
 | 配置项               | 默认值 | 说明           |
 | :-----------------: | :----: | :------------: |
 | chatgpt_api         |   无   | str格式         |
+| nickname         |   无   | list[str]         |
+
+ps. 这个nickname是bot通用的。即，别的插件也能获取这个参数，不过一般不会有啥影响。
 
 代理相关（可选）：
 | 配置项                   | 默认值 | 说明                 |
 | :---------------------: | :----: | :------------------: |
 | chat_use_proxy           | False | 是否启用代理         |
 | chat_proxy_address       | None  | 代理地址             |
 | chat_use_api_forward     | False | 是否启用api转发       |
@@ -209,37 +221,36 @@
 
  ![历史记录效果](https://raw.githubusercontent.com/TheLZY/nonebot_plugin_tuan_chatgpt/master/examples/example_history.png) 
 
 
 
 ## 💡 TODO
 
+- [x] 分群记忆（每个群以及私聊，记忆不会串）
 - [x] 回答分隔 （通过分段实现。可能会考虑换成图片发送）
 - [x] 支持使用代理
 - [x] 增加代理测试 通过返回的ip地址判断代理是否有效 绝赞赛博旅行中！  <!--  http://icanhazip.com/ --> 
 - [x] 私聊做发言频率限制。
 - [x] 错误处理 <!--（比如代理的检测之类的 以及报错方式 团子被玩坏了！这一定不是团子的错！（繁体） 可以写个函数error message    - 倒是可以照着官方的写 不过还是得先在telegrambot上测试一下 ）-->
 - [x] 异步调用优化  （自动重试 / 返回报错  <!-- - 但是估计得自己造轮子...不知道官方有没有提供 --> ）
 - [x] 随机人设 感觉会很有意思（
 - [x] 通过@触发 
 - [ ] 修改人设 ？ 
 - [ ] markdown 渲染 ？ 
-- [ ] ~~自定义触发方式？ 这个倒是可以和修改触发人设一起联动...不过感觉动态修改有点麻烦。~~ 在nickname里面加吧，也挺好
+- [x] ~~自定义触发方式？ 这个倒是可以和修改触发人设一起联动...不过感觉动态修改有点麻烦。~~ 在nickname里面加吧。还是不造轮子了。
 - [ ] ~~Openai 抽风处理（暂时只输出 3*177 个长度的回答 可以根据相同字数出现次数来 同一个字连续出现6次判定为抽风？）~~ 最近没遇到 鉴定为不瞎改就不会有问题
 - [ ] ~~长回答合并转发~~ 似乎更容易被风控 算了。 [参考](https://github.com/Ailitonia/omega-miya/issues/16#issuecomment-827432967)
 
-<!-- - [ ] 全局变量似乎有数据不一致的问题 是否需要加锁？ 毕竟只是一个小小的列表 就算出现一点顺序错误也无伤大雅 --> 
+<!-- - [ ] 全局变量似乎有数据不一致的问题 是否需要加锁？ 毕竟只是一个小小的字典 就算出现一点顺序错误也无伤大雅 --> 
 
 **角色 ~~调教~~ 定制：**
 
-如果希望更改触发语，可以找到源码安装位置里的 `__init__.py` 文件，修改 `chat_checker`
+如果希望更改触发语，可以进入 nonebot 的`.env` 文件，在 `nickname` 里添加触发语
 
-也可以进入 nonebot 的`.env` 文件，在 `nickname` 里添加触发语
-
-如果希望更改人设，可以修改 `utils.py` 文件中的 `MessageBox`
+如果希望更改人设，可以修改 `utils.py` 文件中的 `MessageBox` 中的 `charactor` 相关部分
 
 （正在思考怎么用聊天来添加人设 不过感觉要涉及的东西比较多
 
 ### 一些碎碎念
 
 <!-- 
 代码重构，符合OOC ？ 但是感觉复杂度并不高，可以，但没必要 -->
@@ -311,14 +322,18 @@
 
 
 </details>
 
 
 ## 📆 History
 
+**2023.5.13**
+
+- 支持分群记忆
+- 增加清除记忆功能
 
 **2023.4.4**
 
 - 增加图片渲染功能
 
 
 **2023.3.23**
```

#### html2text {}

```diff
@@ -18,29 +18,36 @@
 tokenï¼ - è®°å¿éå¶ ï¼å¯ä¿®æ¹ é»è®¤è®°å¿7æ¡å¯¹è¯
 ~~åæ­£ç¾¤åä¹æ¯éé±¼ è¿è½é²æ­¢è¢«ç¾¤åè°ææç«å¨~~ï¼ -
 èªå¨éè¯ éè¯¯å¤ç ï¼æ¯ç«æçæ¢¯å­ä¸ç¨³å®ï¼ - æ¯æä»£çå
 api è½¬å ç±äºæ¬äººè½åç²¾åæéï¼å¯¹äºæ½å¨çé®é¢ &
 è½æåçå°æ¹ï¼æ¬¢è¿æ¥æ issue & pull requestã ä¸¾ä¸ªæ å­ ð°ï¼
 ![èå¤©ææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example2.png) ## ð ä½¿ç¨ ###
-æä»¤è¡¨ | æä»¤ | æé | éè¦@ | èå´ | è¯´æ | |:-----:|:----:|:---
--:|:----:|:----:| | å¢å­[èå¤©åå®¹] | ç¾¤å | å¦ | ç¾¤è / ç§è |
+æä»¤è¡¨
+æ³¨æï¼æä»¤ä¸­çå¢å­æ ¹æ®è®¾ç½®çnicknameä¸ºåãä¹å¯ä»¥éè¿
+@å¢å­ ä»£æ¿ã
+ç°å¨æ²¡æé»è®¤è§¦åè¯äºï¼å¦ææ²¡æè®¾ç½®nicknameï¼å°±åªè½éè¿ @
+è§¦åäº æä»¤çç¸åè§¦åè¯å¯èªè¡æ¥çä»£ç ä¸­ aliases é¨åã |
+æä»¤ | æé | éè¦@ | èå´ | è¯´æ | |:-----:|:----:|:----:|:----:|:--
+--:| | å¢å­[èå¤©åå®¹] | ç¾¤å | å¦ | ç¾¤è / ç§è |
 æ¥åå¢å­èå¤©å§ï¼ | | @å¢å­[èå¤©åå®¹] | åä¸ | æ¯ | åä¸ |
-åä¸ | | å¢å­ççä½ç½® | ç¾¤å | å¦ | ç¾¤è / ç§è |
-æ¥çå¢å­èµåå°å | | åå²è®°å½ | ä¸»äºº | å¦ | ç¾¤è / ç§è |
-æ¥çåå²æé®ï¼ä¸åæ¬åç­ï¼ | ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£
-``` nb plugin install nonebot-plugin-tuan-chatgpt ```   ä½¿ç¨ git å®è£ ï¼
-æ¨è ï¼ æ¨èæ­¤æ¹å¼ï¼å ä¸ºè½å¤åæ¶æ¶å°æ´æ° å®è£ï¼å¨
-nonebot2 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, ä½¿ç¨ git å®è£ ``` git
-clone https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git ``` åçº§ï¼
-``` git pull ```   ä½¿ç¨ pip å®è£ ``` pip install nonebot-plugin-tuan-
-chatgpt ```  ç¯å¢éç½®ï¼ æå¼nonebotç`.env` æä»¶ï¼åå¥æ¨ç
-`chatgpt_api` å¦æå¸æå¯ç¨ä»£çï¼åéè¦å¨`.env` æä»¶ä¸­ï¼åå¥
-`chat_use_proxy = True` ä»¥å `chat_proxy_address_https = "ä»£çå°å"` æ
-`chat_proxy_address_http = "ä»£çå°å"`
+åä¸ | | å¢å­ ççä½ç½® / ä½ å¨åªå¿ | ç¾¤å | å¦ | ç¾¤è / ç§è
+| æ¥çå¢å­èµåå°å | | å¢å­ åå²è®°å½ / history | ä¸»äºº | å¦ |
+ç¾¤è / ç§è | æ¥çåå²æé®ï¼ä¸åæ¬åç­ï¼ | | å¢å­
+æ¸é¤è®°å¿ / æ¸é¤åå²è®°å½ | ä¸»äºº | å¦ | ç¾¤è / ç§è |
+æ¸é¤å¢å­çè®°å¿ | ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£ ``` nb plugin
+install nonebot-plugin-tuan-chatgpt # åçº§ï¼ nb plugin update nonebot-
+plugin-tuan-chatgpt ```   ä½¿ç¨ git å®è£  å®è£ï¼å¨ nonebot2
+é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, ä½¿ç¨ git å®è£ ``` git clone
+https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git ``` åçº§ï¼ ``` git
+pull ```   ä½¿ç¨ pip å®è£ ``` pip install nonebot-plugin-tuan-chatgpt ```
+ç¯å¢éç½®ï¼ æå¼nonebotç`.env` æä»¶ï¼åå¥æ¨ç `chatgpt_api`
+ä»¥å `nickname` å¦æå¸æå¯ç¨ä»£çï¼åéè¦å¨`.env`
+æä»¶ä¸­ï¼åå¥ `chat_use_proxy = True` ä»¥å `chat_proxy_address_https =
+"ä»£çå°å"` æ `chat_proxy_address_http = "ä»£çå°å"`
 (å¤çé»è¾ç±»ä¼¼openaiï¼ä¼åä½¿ç¨httpsãä½æ¯httpsç»å¸¸ä¼æ¥éï¼aiohttpåurllib3é½å¯è½ä¼é æé®é¢ï¼ï¼æ¨èåªä½¿ç¨http)
 å¦æå¸æå¯ç¨apiè½¬å (ç±»ä¼¼ [è¾è®¯äºå½æ°æ­å»º OpenAI å½åä»£ç]
 (https://github.com/Ice-Hazymoon/openai-scf-proxy)
 éè¿äºå½æ°ç­æ¹å¼å®ç°åä»£ )ï¼åéè¦åå¥åå¥
 `chat_use_api_forward = True` ä»¥å `chat_api_address = "ä»£çå°å"`
 ä½æ¯ä¸æ¨èä¸¤èåæ¶å¯ç¨
 å¦æå¸æå¯ç¨å¾çæ¸²æï¼åéè¦åå¥ `chat_use_img2text=True`,
@@ -52,31 +59,34 @@
 ä¹å¯ä»¥ç´æ¥ä¸è½½ Release ç [tuan_chatgpt.zip](https://github.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/files/11163988/tuan_chatgpt.zip) æå° `/data`
 éå»
 å¾çæ¸²æåè½å¯ç¨åï¼ä¼èªå¨å¯ç¨äºç»´ç æ·»å ä»¥åèæ¯å¾çæ·»å ãå¯ä»¥éæ©å³é­ã
 å·ä½éç½®æ¹å¼åè **âï¸ éç½®** ä»¥å [éç½® | Nonebot](https://
 v2.nonebot.dev/docs/tutorial/
 configuration#%E9%85%8D%E7%BD%AE%E6%96%B9%E5%BC%8F) egï¼ chatgpt_api = "sk-
-1145141919" # å¯ç¨ä»£ç chat_use_proxy=True chat_proxy_address_http='http://
-127.0.0.1:10809' chat_proxy_address_https='http://127.0.0.1:10809' #
-å¯ç¨apiè½¬å chat_use_api_forward=True chat_api_address="https://
-api.openai.com/v1" ï¼è¿ä¸ªæ¯å®æ¹æ¥å£ ç§çåæ²¡é®é¢ï¼å¤§æ¦ï¼
+1145141919" nickname = ['å¢å­', 'é·å§'] # å¯ç¨ä»£ç chat_use_proxy=True
+chat_proxy_address_http='http://127.0.0.1:10809'
+chat_proxy_address_https='http://127.0.0.1:10809' # å¯ç¨apiè½¬å
+chat_use_api_forward=True chat_api_address="https://api.openai.com/v1"
+ï¼è¿ä¸ªæ¯å®æ¹æ¥å£ ç§çåæ²¡é®é¢ï¼å¤§æ¦ï¼
 è¿æ¯å¾çå·ä½çè½¬åæ¹å¼ï¼ # å¯ç¨å¾çæ¸²æ
 chat_use_img2text=True å¦ææ²¡æèªå¨å¯¼å¥æä»¶çåè½ï¼éè¦æå¼
 nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `[tool.nonebot]`
 é¨åè¿½å åå¥ plugins = ["nonebot_plugin_tuan_chatgpt"] ## âï¸ éç½®
 å¨ nonebot2 é¡¹ç®ç`.env`æä»¶ä¸­æ¯ææ·»å ä»¥ä¸éç½® å¿å¡«é¡¹ï¼ |
 éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :-----------------: | :----: | :-----------
--: | | chatgpt_api | æ  | stræ ¼å¼ | ä»£çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹
-| é»è®¤å¼ | è¯´æ | | :---------------------: | :----: | :-----------------
--: | | chat_use_proxy | False | æ¯å¦å¯ç¨ä»£ç | | chat_proxy_address |
-None | ä»£çå°å | | chat_use_api_forward | False | æ¯å¦å¯ç¨apiè½¬å |
-| chat_api_address | None | apiè½¬åå°å | æ¸²æå¾çç¸å³ï¼å¯éï¼ï¼
-| éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :------------------: | :------------------
------------: | :----------------------------: | | chat_use_img2text | False |
+-: | | chatgpt_api | æ  | stræ ¼å¼ | | nickname | æ  | list[str] | ps.
+è¿ä¸ªnicknameæ¯botéç¨çãå³ï¼å«çæä»¶ä¹è½è·åè¿ä¸ªåæ°ï¼ä¸è¿ä¸è¬ä¸ä¼æå¥å½±åã
+ä»£çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :-------------
+--------: | :----: | :------------------: | | chat_use_proxy | False |
+æ¯å¦å¯ç¨ä»£ç | | chat_proxy_address | None | ä»£çå°å | |
+chat_use_api_forward | False | æ¯å¦å¯ç¨apiè½¬å | | chat_api_address |
+None | apiè½¬åå°å | æ¸²æå¾çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹ |
+é»è®¤å¼ | è¯´æ | | :------------------: | :-----------------------------: |
+:----------------------------: | | chat_use_img2text | False |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_use_qr | True |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_use_background | True |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_data_path | 'data/tuan_chatgpt' |
 æ°æ®è·¯å¾ãä¿®æ¹è¯·ç¨ç»å¯¹è·¯å¾ | | chat_font_path | 'font' |
 å­ä½è·¯å¾ï¼é»è®¤ä¸ºdata/tuan_chat/font) | | chat_background_path |
 "background" | èæ¯è·¯å¾ï¼é»è®¤ä¸ºdata/tuan_chat/backgroundï¼| |
 chat_font_name | 'sarasa-mono-sc-regular.ttf' | ä½¿ç¨çå­ä½ | |
@@ -89,33 +99,33 @@
 åéåç­é¿åº¦ | | user_freq_lim | 4 | éå¶ç¾¤ååè¨éåº¦ï¼ç§ï¼ |
 | group_freq_lim | 6 | éå¶ç¾¤ååè¨éåº¦ï¼ç§ï¼ | |
 conversation_remember_num | 7 | è½è®°ä½çå¯¹è¯æ°ç® | ## ð ææå¾
 å¾çæ¸²æ ![å¾çæ¸²æææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example_img2text.PNG) åå²è®°å½
 ![åå²è®°å½ææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example_history.png) ## ð¡ TODO -
-[x] åç­åé ï¼éè¿åæ®µå®ç°ãå¯è½ä¼èèæ¢æå¾çåéï¼ -
-[x] æ¯æä½¿ç¨ä»£ç - [x] å¢å ä»£çæµè¯
+[x] åç¾¤è®°å¿ï¼æ¯ä¸ªç¾¤ä»¥åç§èï¼è®°å¿ä¸ä¼ä¸²ï¼ - [x]
+åç­åé ï¼éè¿åæ®µå®ç°ãå¯è½ä¼èèæ¢æå¾çåéï¼ - [x]
+æ¯æä½¿ç¨ä»£ç - [x] å¢å ä»£çæµè¯
 éè¿è¿åçipå°åå¤æ­ä»£çæ¯å¦ææ ç»èµèµåæè¡ä¸­ï¼  - [x]
 ç§èååè¨é¢çéå¶ã - [x] éè¯¯å¤ç  - [x] å¼æ­¥è°ç¨ä¼å
 ï¼èªå¨éè¯ / è¿åæ¥é  ï¼ - [x] éæºäººè®¾ æè§ä¼å¾æææï¼
-- [x] éè¿@è§¦å - [ ] ä¿®æ¹äººè®¾ ï¼ - [ ] markdown æ¸²æ ï¼ - [ ]
+- [x] éè¿@è§¦å - [ ] ä¿®æ¹äººè®¾ ï¼ - [ ] markdown æ¸²æ ï¼ - [x]
 ~~èªå®ä¹è§¦åæ¹å¼ï¼
 è¿ä¸ªåæ¯å¯ä»¥åä¿®æ¹è§¦åäººè®¾ä¸èµ·èå¨...ä¸è¿æè§å¨æä¿®æ¹æç¹éº»ç¦ã~~
-å¨nicknameéé¢å å§ï¼ä¹æºå¥½ - [ ] ~~Openai
+å¨nicknameéé¢å å§ãè¿æ¯ä¸é è½®å­äºã - [ ] ~~Openai
 æ½é£å¤çï¼ææ¶åªè¾åº 3*177 ä¸ªé¿åº¦çåç­
 å¯ä»¥æ ¹æ®ç¸åå­æ°åºç°æ¬¡æ°æ¥
 åä¸ä¸ªå­è¿ç»­åºç°6æ¬¡å¤å®ä¸ºæ½é£ï¼ï¼~~ æè¿æ²¡éå°
 é´å®ä¸ºä¸çæ¹å°±ä¸ä¼æé®é¢ - [ ] ~~é¿åç­åå¹¶è½¬å~~
 ä¼¼ä¹æ´å®¹æè¢«é£æ§ ç®äºã [åè](https://github.com/Ailitonia/omega-
 miya/issues/16#issuecomment-827432967)  **è§è² ~~è°æ~~ å®å¶ï¼**
-å¦æå¸ææ´æ¹è§¦åè¯­ï¼å¯ä»¥æ¾å°æºç å®è£ä½ç½®éç
-`__init__.py` æä»¶ï¼ä¿®æ¹ `chat_checker` ä¹å¯ä»¥è¿å¥ nonebot ç`.env`
-æä»¶ï¼å¨ `nickname` éæ·»å è§¦åè¯­
-å¦æå¸ææ´æ¹äººè®¾ï¼å¯ä»¥ä¿®æ¹ `utils.py` æä»¶ä¸­ç `MessageBox`
+å¦æå¸ææ´æ¹è§¦åè¯­ï¼å¯ä»¥è¿å¥ nonebot ç`.env` æä»¶ï¼å¨
+`nickname` éæ·»å è§¦åè¯­ å¦æå¸ææ´æ¹äººè®¾ï¼å¯ä»¥ä¿®æ¹
+`utils.py` æä»¶ä¸­ç `MessageBox` ä¸­ç `charactor` ç¸å³é¨å
 ï¼æ­£å¨æèæä¹ç¨èå¤©æ¥æ·»å äººè®¾
 ä¸è¿æè§è¦æ¶åçä¸è¥¿æ¯è¾å¤ ### ä¸äºç¢ç¢å¿µ
 conversation_remember_num
 æå¥½ä¸è¦è°å¾å¤ªé«ï¼è®°ä½å¤ªå¤è¯äºå°±ä¼åææ§å·æ·¡æºå¨äºº
 ð¥ åºç°äº wake up
 è¯ä¹ä¼ååå»ï¼ä¸è¿ç°å¨åºè¯¥å¤è¯´ä¸¤å¥è¯å°±å¥½äº
 é¿åç­å¤çï¼
@@ -151,20 +161,20 @@
 'å¶å®è¿ä¸ªé®é¢æ²¡ææ åç­æ¡ï¼æ¯ä¸ªäººçèº«é«é½æ¯ç¬ä¸æ äºçï¼éè¦ç'},
 {'role': 'user', 'content': 'å¢å­å¥½æ£'}, {'role': 'assistant', 'content':
 'è°¢è°¢ä½ ï¼ä½ ä¹å¾æ£å¦~'}, {'role': 'user', 'content':
 'å¢å­ï¼å¦ä½çå¾ä¸­å½çæç«¯å¥³æ³é®é¢'}] response = await
 openai.ChatCompletion.acreate( model = "gpt-3.5-turbo", messages =
 messages_error, frequency_penalty = - 0.8, # å¤ªé«äºå®¹æåºbug timeout = 30
 ) answer = response.choices[0].message.content ```  ## ð History
-**2023.4.4** - å¢å å¾çæ¸²æåè½ **2023.3.23** - å¢å  api è½¬åæ¯æ
-**2023.3.15** - æ·»å éæºäººè®¾ãé¢çäºä¿®æ¹äººè®¾çæ¥å£
-æç©ºåå¡«å - æ¯æéè¿@è§¦å **2023.3.14** - å¢å éè¯¯éè¯
-ï¼å¦æå¤±è´¥ èªå¨éè¯æå¤ä¸æ¬¡
-å¯¹äºæ¢¯å­ä¸ç¨³å®çæ¶åå¸®å©å¾å¤§ï¼ - å¢å æ¥éè¾åº
-ï¼3æ¬¡é½å¤±è´¥çè¯ çæ ~~æè¶£ç~~ æ¥éä¿¡æ¯
+**2023.5.13** - æ¯æåç¾¤è®°å¿ - å¢å æ¸é¤è®°å¿åè½ **2023.4.4** -
+å¢å å¾çæ¸²æåè½ **2023.3.23** - å¢å  api è½¬åæ¯æ **2023.3.15**
+- æ·»å éæºäººè®¾ãé¢çäºä¿®æ¹äººè®¾çæ¥å£ æç©ºåå¡«å -
+æ¯æéè¿@è§¦å **2023.3.14** - å¢å éè¯¯éè¯ ï¼å¦æå¤±è´¥
+èªå¨éè¯æå¤ä¸æ¬¡ å¯¹äºæ¢¯å­ä¸ç¨³å®çæ¶åå¸®å©å¾å¤§ï¼ -
+å¢å æ¥éè¾åº ï¼3æ¬¡é½å¤±è´¥çè¯ çæ ~~æè¶£ç~~ æ¥éä¿¡æ¯
 ä»¥ç¬¬ä¸æ¬¡å¤±è´¥è¿åç error ä¸ºåï¼ - ä¿®æ¹æ¶æ¯è§¦åå¨
 ~~è¯å¾éè¿@èå¤© å¤§å¤±è´¥~~ - å¢å ç§èé¢çéå¶
 é»è®¤ä¸º4ç§ä¸æ¬¡ **2023.3.12** - å¢å èµåå°åæ£æµåè½ -
 å¢å éæ©æ§è®°å½åè½ ï¼å»æä¼è®©å¥¹æ³èµ·æ¥èªå·±æ¯aiçåç­
 é¿åä¸ç´è¯´èªå·±æ¯aiï¼ **2023.3.10** - å¢å ä»£çæ¯æ **2023.3.9** -
 åæ¢æå®æ¹å¼æ­¥è°ç¨æ¥å£ ## â­ Special thanks to
 æ¬é¡¹ç®å¨å¼åè¿ç¨ä¸­ï¼åèäºä¸å°ä»¥ä¸é¡¹ç®ï¼å¯¹åä½è¡¨ç¤ºç±è¡·çæè°¢
```

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/__init__.py` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,23 +1,25 @@
 from nonebot.adapters.onebot.v11 import Bot, MessageEvent, Message, GroupMessageEvent, PrivateMessageEvent
 from nonebot.adapters.onebot.v11 import MessageSegment
 # from nonebot.adapters.telegram import Bot
 # from nonebot.adapters.telegram.event import MessageEvent
-from nonebot import on_command, on_message
+from nonebot import on_command, on_message # ,MatcherGroup
+from nonebot.rule import to_me
 from nonebot.plugin import PluginMetadata
-# from nonebot.params import RawCommand
+from nonebot.params import RawCommand
 from nonebot.permission import SUPERUSER
 from nonebot.log import logger
 
 from .utils import *
-from .config import config
+from .config import config, NICKNAME, init_name
 from .text_to_img import text2img_main
 import openai
 
 import asyncio
+import re
 
 __plugin_meta__ = PluginMetadata(
     name='团子聊天',
     description='团子聊天 QQ bot ver. powered by Chatgpt',
     usage='团子[聊天内容]',
     extra={
         'author': 'TheLZY',
@@ -26,20 +28,22 @@
         'configs': {
             '群冷却': 4,
             '群成员冷却': 6
         }
     }
 )
 
-
-### 初始化设置
+###==============  初始化  =================###
 if config.chatgpt_api:
     openai.api_key = config.chatgpt_api
 else:
-    logger.error("请检查 tuan-chatgpt api")
+    logger.error("未配置 tuan-chatgpt api，无法使用chatgpt")
+
+if not init_name:
+    logger.warning("未配置 nickname，只会响应@消息")
 
 # 使用api转发
 if config.chat_use_api_forward:
     if config.chat_api_address:
         openai.api_base = config.chat_api_address
     else:
         logger.error("请检查 api 转发地址 chat_api_address")
@@ -58,89 +62,73 @@
     openai.proxy = proxy
 
 # 初始化路径
 path_init()
 
 
 
-async def chat_checker(event: MessageEvent) -> bool:
-    # 检查 是否以团子开头 / to_me. 可能会造成一点性能问题
-    res = str(event.get_message())[:2]  == '团子' or event.is_tome()
-    return res
-
-chat_service = on_message(rule = chat_checker , priority = 99, block = False)
-chat_service_history = on_command("历史记录", permission=SUPERUSER)
+###==============  主要处理函数  =================###
 
+chat_service = on_message(rule = to_me() , priority = 99, block = False)
 
-# 这样做，每次重启会重置用户对话数据
-# 可以考虑用json保存
-message_list_user = []
+chat_service_history = on_command("历史记录",rule = to_me() , permission=SUPERUSER, aliases={'history'}, priority=98, block=True)
+chat_service_clean = on_command("清除记忆",rule = to_me() , aliases={'消除记忆','记忆消除','清除历史记录','清空历史记录'}, priority=98, block=True)
+chat_service_position = on_command("看看位置",rule = to_me() , aliases={'你在哪儿'}, priority=98, block=True)
 
 
 @chat_service.handle()
-async def main_chat(bot: Bot, event: MessageEvent):
+async def main_chat(event: MessageEvent):
     global tuan_freq_limiter
     global messagebox
-    global message_list_user
 
     # Check cd
     if not tuan_freq_limiter.check(f'chat-user{event.user_id}'):
         await chat_service.finish(f'你说话太快啦! { tuan_freq_limiter.left(f"chat-user{event.user_id}") }秒之后再理你！')
     if isinstance(event, GroupMessageEvent):
-        if not tuan_freq_limiter.check(f'chat-group{event.group_id}'):
-            await chat_service.finish(f'你们说话太快啦! {tuan_freq_limiter.left(f"chat-group{event.group_id}")}秒之后再理你们！')
+        chat_id = f"chat-group{event.group_id}"
+        if not tuan_freq_limiter.check(chat_id):
+            await chat_service.finish(f'你们说话太快啦! { tuan_freq_limiter.left(chat_id) }秒之后再理你们！')
+    else:
+        chat_id = f'chat-user{event.user_id}'
 
+    conversation = str(event.original_message)
 
-    # 可以不保留前面的团子两个字
-    # conversation = str(event.get_message())[2:]
-    conversation = str(event.get_message())
-
-    # 没必要再写一个on command
-    # 但是之后再来写@触发的时候估计要改
-    if conversation == "团子看看位置":
-        proxy = None
-        try:
-            if config.chat_proxy_address_https:
-                proxy = config.chat_proxy_address_https
-            elif config.chat_proxy_address_http:
-                proxy = config.chat_proxy_address_http
-            else:
-                logger.warning("请检查 tuan-chatgpt 代理地址")
-
-            pos = await get_cyber_pos(config.chat_use_proxy, proxy)
-        except Exception as e:
-            # print(e)
-            await chat_service_history.finish(f'赛博旅游失败！都怪{e}！')
-        # 不能写里面，不然finish也会被try视为报错
-        await chat_service_history.finish(f'团子现在正在{pos}赛博旅游中~ ') 
+    conversation = conversation_preprocessing(conversation)
+    if not conversation or conversation == "":
+        # 空消息直接结束
+        # 似乎不能直接break？
+        await chat_service.finish()
 
     # Length detect for conversation
     conversation = limit_conversation_size(conversation, config.conversation_max_size)
 
-    message_list_user = add_conversation(conversation, message_list_user)
-    message_list_user = check_message_length(message_list = message_list_user, conversation_remember_num = config.conversation_remember_num)
+    # 将这段聊天加入聊天历史中
+    # 聊天历史会和人设信息整合在一起
+    # ps.人设信息会随机抽取
+    messagebox.add(conversation = conversation, id = chat_id)
 
-    # 将保存的用户信息和人设信息整合在一起
-    # 人设信息会随机抽取
-    messages = messagebox.get_messages() + message_list_user
+    messages = messagebox.get_messages(id = chat_id)
     
     # 主要交流函数
     try:
         answer = await chat(message_list = messages)
     except Exception as e:
         # print("调用API失败：", e)
-        message_list_user.pop()  # 调用失败不保存这个会话 但是这一步的时候协程可能会出现问题 就是加锁又太影响性能了 算了 先这样
+        # message_list_user.pop()  # 调用失败不保存这个会话 但是这一步的时候协程可能会出现问题 就是加锁又太影响性能了 算了 先这样
+        messagebox.delete_fail(id=chat_id)
         error_message = generate_error_message(e = e)
         await chat_service.finish(error_message)
         
     # 储存answer
     answer_add = limit_conversation_size(answer, config.answer_max_size)
-    message_list_user = add_conversation(answer_add, message_list_user, 'assistant')
+    # message_list_user = add_conversation(answer_add, message_list_user, 'assistant')
+    messagebox.add(conversation = answer_add, role =  'assistant', id = chat_id)
 
     # 限制聊天频率
+    # 其实可以直接改成 id 的 不过因为分了group和user还是得弄一下
     if isinstance(event, GroupMessageEvent):
         tuan_freq_limiter.start(f'chat-group{event.group_id}', config.group_freq_lim)
     tuan_freq_limiter.start(f'chat-user{event.user_id}', config.user_freq_lim)
 
     # Length division for answer
     # 避免腾讯风控。
     # 现在的处理方式是分隔成几段，慢慢发
@@ -163,21 +151,73 @@
         else:
             answer_segments = [answer[i:i + config.answer_split_size] for i in range(0, len(answer), config.answer_split_size)]
             for i in answer_segments[:3]:
                 # Use sleep to avoid Tencent risk management
                 await asyncio.sleep(1)
                 await chat_service.send(i)
 
+
 # 调试用。输出最近的几个问题
 
 @chat_service_history.handle()
 async def send_messagelist(event: MessageEvent):
     # 太长了容易被腾讯拦截 
-    global message_list_user
-    for conversation in message_list_user:
+    # global message_list_user
+    # for conversation in message_list_user:
+    #     if conversation['role'] == "user":
+    #         print(str(conversation['content']))
+    #         # 有时候部分QQ客户端不显示 （PC / 手机） 可能有风控危险
+    #         # 间隔一段时间发一次，避免发送速度过快引发腾讯风控
+    #         # 但是print是没问题的
+    #         await asyncio.sleep(1)
+    #         await chat_service_history.send(str(conversation['content']))
+    global messagebox
+    if isinstance(event, GroupMessageEvent):
+        chat_id = f"chat-group{event.group_id}"
+    else:
+        chat_id = f'chat-user{event.user_id}'
+
+    history_list = messagebox.get_history(id=chat_id)
+
+    if history_list == []:
+        await chat_service_history.send(f"你还没有和{NICKNAME}聊过天哦~")
+
+    for conversation in history_list:
         if conversation['role'] == "user":
-            print(str(conversation['content']))
+            # print(str(conversation['content']))
             # 有时候部分QQ客户端不显示 （PC / 手机） 可能有风控危险
             # 间隔一段时间发一次，避免发送速度过快引发腾讯风控
             # 但是print是没问题的
             await asyncio.sleep(1)
-            await chat_service_history.send(str(conversation['content']))
+            await chat_service_history.send(str(conversation['content']))
+
+
+@chat_service_clean.handle()
+async def clean_history(event: MessageEvent):
+    global messagebox
+    if isinstance(event, GroupMessageEvent):
+        chat_id = f"chat-group{event.group_id}"
+    else:
+        chat_id = f'chat-user{event.user_id}'
+
+    messagebox.clean(id = chat_id)
+    
+    await clean_history.finish(f'成功清除记忆~ 快来和{NICKNAME}聊天吧~')
+
+@chat_service_position.handle()
+async def check_position(event: MessageEvent):
+    
+    proxy = None
+    try:
+        if config.chat_proxy_address_https:
+            proxy = config.chat_proxy_address_https
+        elif config.chat_proxy_address_http:
+            proxy = config.chat_proxy_address_http
+        else:
+            logger.warning("请检查 tuan-chatgpt 代理地址")
+
+        pos = await get_cyber_pos(config.chat_use_proxy, proxy)
+    except Exception as e:
+        # print(e)
+        await chat_service_history.finish(f'赛博旅游失败！都怪{e}！')
+    # 不能写里面，不然finish也会被try视为报错
+    await chat_service_history.finish(f'{NICKNAME}现在正在{pos}赛博旅游中~ ')
```

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/config.py` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/config.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,31 +1,40 @@
 from nonebot import get_driver
 from pydantic import BaseModel, Extra
+from typing import Union, Set
 
 class Config(BaseModel, extra=Extra.ignore):
     chatgpt_api: str = None
-    conversation_max_size: int =  300 # For each conversation, only use first 77 words
-    answer_max_size: int = 50        # For each answer, only record first 30 words
+    conversation_max_size: int =  300 # For each conversation, only use first 300 words
+    answer_max_size: int = 50        # For each answer, only record first 50 words
     answer_split_size: int = 177     # Length division for answer
     user_freq_lim: int = 4           # Limit the speaking speed of group members. (second)
     group_freq_lim: int = 6          # Limit the speaking speed in a group. 
     conversation_remember_num: int = 7    # The number of conversation that is remembered. 7 means she can remember 4 conversation from user. （太大了会忘记）
+    reply_at_message: bool = False    # To be implemented.
     # 代理有关
     chat_use_proxy: bool = False     # Use proxy or not. In fact it's not needed. Just to remind everyone this function exists.
     chat_proxy_address_http: str = None
     chat_proxy_address_https: str = None
     chat_use_api_forward: bool = False    # Use api forward or not. If it's true, the api address must be specified.
     chat_api_address: str = None
     # 图片转文字有关
     chat_data_path: str = 'data/tuan_chatgpt'    # data path
     chat_use_img2text: bool = False    # Render text and send images
-    chat_font_path: str = 'font'  # path of chat. 未指定时默认使用 data/font
-    chat_font_name: str = 'sarasa-mono-sc-regular.ttf'      # 启用的
-    chat_canvas_width: int = 1000    # 画布大小
-    chat_font_size: int = 30         # 字号
+    chat_font_path: str = 'font'  # Path of Font. 未指定时默认使用 data/font
+    chat_font_name: str = 'sarasa-mono-sc-regular.ttf'      # Font.
+    chat_canvas_width: int = 1000    # Width for Canvas
+    chat_font_size: int = 30         # Font size
     chat_offset_x: int = 50          
     chat_offset_y: int = 50          # 起始绘制点的坐标
     chat_use_qr: bool = True         # Render text and send images
     chat_use_background: bool = True    # Render text and send images
     chat_background_path: str = "background"  # path of background. 未指定时默认使用 data/background
 
 config = Config.parse_obj(get_driver().config)
+
+try:
+    NICKNAME: str = list(get_driver().config.nickname)[-1]
+    init_name = NICKNAME
+except Exception:
+    init_name = None
+    NICKNAME = '团子'
```

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/perf_timer.py` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/perf_timer.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/nonebot_plugin_tuan_chatgpt/text_to_img.py` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/nonebot_plugin_tuan_chatgpt/text_to_img.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/pyproject.toml` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/pyproject.toml`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot_plugin_tuan_chatgpt"
-version = "0.3.3rc1"
+version = "0.4.0-beta1"
 description = "\"Chat with tuanzi ~\""
 authors = ["TheLZY"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt"
 
 [tool.poetry.dependencies]
```

### Comparing `nonebot_plugin_tuan_chatgpt-0.3.3rc1/PKG-INFO` & `nonebot_plugin_tuan_chatgpt-0.4.0b1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-tuan-chatgpt
-Version: 0.3.3rc1
+Version: 0.4.0b1
 Summary: "Chat with tuanzi ~"
 Home-page: https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt
 License: MIT
 Author: TheLZY
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -79,44 +79,52 @@
 <!--  ![聊天效果](example2.png)  -->
 ![聊天效果](https://raw.githubusercontent.com/TheLZY/nonebot_plugin_tuan_chatgpt/master/examples/example2.png)
 
 
 ## 🎉 使用
 
 ### 指令表
+注意：指令中的团子根据设置的nickname为准。也可以通过 @团子 代替。
+
+现在没有默认触发词了，如果没有设置nickname，就只能通过 @ 触发了
+
+指令的相同触发词可自行查看代码中 aliases 部分。
+
+
 
 | 指令 | 权限 | 需要@ | 范围 | 说明 |
 |:-----:|:----:|:----:|:----:|:----:|
 | 团子[聊天内容] | 群员 | 否 | 群聊 / 私聊 | 来和团子聊天吧！ |
 | @团子[聊天内容] | 同上 |  是 | 同上 | 同上 |
-| 团子看看位置 | 群员 | 否 | 群聊 / 私聊 | 查看团子赛博地址 |
-| 历史记录 | 主人 | 否 | 群聊 / 私聊 | 查看历史提问（不包括回答） |
+| 团子 看看位置 / 你在哪儿 | 群员 | 否 | 群聊 / 私聊 | 查看团子赛博地址 |
+| 团子 历史记录 / history | 主人 | 否 | 群聊 / 私聊 | 查看历史提问（不包括回答） |
+| 团子 清除记忆 / 清除历史记录 | 主人 | 否 | 群聊 / 私聊 | 清除团子的记忆 |
 
 
 
 ## 💿 安装
 
 
 <details>
 
 <summary>使用 nb-cli 安装</summary>
 
 ```
 nb plugin install nonebot-plugin-tuan-chatgpt
+
+# 升级：
+nb plugin update nonebot-plugin-tuan-chatgpt
 ```
 
 </details>
 
 
 <details>
 
-<summary>使用 git 安装 （ 推荐 ）</summary>
-
-
-推荐此方式，因为能够及时收到更新
+<summary>使用 git 安装 </summary>
 
 安装：在 nonebot2 项目的插件目录下, 打开命令行, 使用 git 安装
 
 ```
 git clone https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git
 ```
 升级：
@@ -136,15 +144,15 @@
 ```
 
 </details>
 
 
 环境配置：
 
-打开nonebot的`.env` 文件，写入您的 `chatgpt_api`
+打开nonebot的`.env` 文件，写入您的 `chatgpt_api` 以及 `nickname`
 
 如果希望启用代理，则需要在`.env` 文件中，写入 `chat_use_proxy = True` 以及 `chat_proxy_address_https = "代理地址"` 或 `chat_proxy_address_http = "代理地址"`  (处理逻辑类似openai，优先使用https。但是https经常会报错（aiohttp和urllib3都可能会造成问题），推荐只使用http)
 
 如果希望启用api转发 (类似 [腾讯云函数搭建 OpenAI 国内代理](https://github.com/Ice-Hazymoon/openai-scf-proxy) 通过云函数等方式实现反代 )，则需要写入写入 `chat_use_api_forward = True` 以及 `chat_api_address = "代理地址"` 
 
 但是不推荐两者同时启用
 
@@ -155,14 +163,15 @@
 图片渲染功能启用后，会自动启用二维码添加以及背景图片添加。可以选择关闭。
 
 具体配置方式参考 **⚙️ 配置** 以及 [配置 | Nonebot](https://v2.nonebot.dev/docs/tutorial/configuration#%E9%85%8D%E7%BD%AE%E6%96%B9%E5%BC%8F)
 
 eg： 
 
     chatgpt_api = "sk-1145141919"
+    nickname = ['团子', '雷姆']
     # 启用代理
     chat_use_proxy=True
     chat_proxy_address_http='http://127.0.0.1:10809'
     chat_proxy_address_https='http://127.0.0.1:10809'
     # 启用api转发
     chat_use_api_forward=True
     chat_api_address="https://api.openai.com/v1" （这个是官方接口 照着写没问题，大概？ 还是得看具体的转发方式）
@@ -183,14 +192,17 @@
 
 在 nonebot2 项目的`.env`文件中支持添加以下配置
 
 必填项：
 | 配置项               | 默认值 | 说明           |
 | :-----------------: | :----: | :------------: |
 | chatgpt_api         |   无   | str格式         |
+| nickname         |   无   | list[str]         |
+
+ps. 这个nickname是bot通用的。即，别的插件也能获取这个参数，不过一般不会有啥影响。
 
 代理相关（可选）：
 | 配置项                   | 默认值 | 说明                 |
 | :---------------------: | :----: | :------------------: |
 | chat_use_proxy           | False | 是否启用代理         |
 | chat_proxy_address       | None  | 代理地址             |
 | chat_use_api_forward     | False | 是否启用api转发       |
@@ -234,37 +246,36 @@
 
  ![历史记录效果](https://raw.githubusercontent.com/TheLZY/nonebot_plugin_tuan_chatgpt/master/examples/example_history.png) 
 
 
 
 ## 💡 TODO
 
+- [x] 分群记忆（每个群以及私聊，记忆不会串）
 - [x] 回答分隔 （通过分段实现。可能会考虑换成图片发送）
 - [x] 支持使用代理
 - [x] 增加代理测试 通过返回的ip地址判断代理是否有效 绝赞赛博旅行中！  <!--  http://icanhazip.com/ --> 
 - [x] 私聊做发言频率限制。
 - [x] 错误处理 <!--（比如代理的检测之类的 以及报错方式 团子被玩坏了！这一定不是团子的错！（繁体） 可以写个函数error message    - 倒是可以照着官方的写 不过还是得先在telegrambot上测试一下 ）-->
 - [x] 异步调用优化  （自动重试 / 返回报错  <!-- - 但是估计得自己造轮子...不知道官方有没有提供 --> ）
 - [x] 随机人设 感觉会很有意思（
 - [x] 通过@触发 
 - [ ] 修改人设 ？ 
 - [ ] markdown 渲染 ？ 
-- [ ] ~~自定义触发方式？ 这个倒是可以和修改触发人设一起联动...不过感觉动态修改有点麻烦。~~ 在nickname里面加吧，也挺好
+- [x] ~~自定义触发方式？ 这个倒是可以和修改触发人设一起联动...不过感觉动态修改有点麻烦。~~ 在nickname里面加吧。还是不造轮子了。
 - [ ] ~~Openai 抽风处理（暂时只输出 3*177 个长度的回答 可以根据相同字数出现次数来 同一个字连续出现6次判定为抽风？）~~ 最近没遇到 鉴定为不瞎改就不会有问题
 - [ ] ~~长回答合并转发~~ 似乎更容易被风控 算了。 [参考](https://github.com/Ailitonia/omega-miya/issues/16#issuecomment-827432967)
 
-<!-- - [ ] 全局变量似乎有数据不一致的问题 是否需要加锁？ 毕竟只是一个小小的列表 就算出现一点顺序错误也无伤大雅 --> 
+<!-- - [ ] 全局变量似乎有数据不一致的问题 是否需要加锁？ 毕竟只是一个小小的字典 就算出现一点顺序错误也无伤大雅 --> 
 
 **角色 ~~调教~~ 定制：**
 
-如果希望更改触发语，可以找到源码安装位置里的 `__init__.py` 文件，修改 `chat_checker`
+如果希望更改触发语，可以进入 nonebot 的`.env` 文件，在 `nickname` 里添加触发语
 
-也可以进入 nonebot 的`.env` 文件，在 `nickname` 里添加触发语
-
-如果希望更改人设，可以修改 `utils.py` 文件中的 `MessageBox`
+如果希望更改人设，可以修改 `utils.py` 文件中的 `MessageBox` 中的 `charactor` 相关部分
 
 （正在思考怎么用聊天来添加人设 不过感觉要涉及的东西比较多
 
 ### 一些碎碎念
 
 <!-- 
 代码重构，符合OOC ？ 但是感觉复杂度并不高，可以，但没必要 -->
@@ -336,14 +347,18 @@
 
 
 </details>
 
 
 ## 📆 History
 
+**2023.5.13**
+
+- 支持分群记忆
+- 增加清除记忆功能
 
 **2023.4.4**
 
 - 增加图片渲染功能
 
 
 **2023.3.23**
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-tuan-chatgpt Version: 0.3.3rc1
+Metadata-Version: 2.1 Name: nonebot-plugin-tuan-chatgpt Version: 0.4.0b1
 Summary: "Chat with tuanzi ~" Home-page: https://github.com/TheLZY/
 nonebot_plugin_tuan_chatgpt License: MIT Author: TheLZY Requires-Python:
 >=3.8,<4.0 Classifier: License :: OSI Approved :: MIT License Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.8 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Programming Language ::
 Python :: 3.11 Requires-Dist: Pillow (>=9.5.0,<10.0.0) Requires-Dist: aiohttp
@@ -32,29 +32,36 @@
 tokenï¼ - è®°å¿éå¶ ï¼å¯ä¿®æ¹ é»è®¤è®°å¿7æ¡å¯¹è¯
 ~~åæ­£ç¾¤åä¹æ¯éé±¼ è¿è½é²æ­¢è¢«ç¾¤åè°ææç«å¨~~ï¼ -
 èªå¨éè¯ éè¯¯å¤ç ï¼æ¯ç«æçæ¢¯å­ä¸ç¨³å®ï¼ - æ¯æä»£çå
 api è½¬å ç±äºæ¬äººè½åç²¾åæéï¼å¯¹äºæ½å¨çé®é¢ &
 è½æåçå°æ¹ï¼æ¬¢è¿æ¥æ issue & pull requestã ä¸¾ä¸ªæ å­ ð°ï¼
 ![èå¤©ææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example2.png) ## ð ä½¿ç¨ ###
-æä»¤è¡¨ | æä»¤ | æé | éè¦@ | èå´ | è¯´æ | |:-----:|:----:|:---
--:|:----:|:----:| | å¢å­[èå¤©åå®¹] | ç¾¤å | å¦ | ç¾¤è / ç§è |
+æä»¤è¡¨
+æ³¨æï¼æä»¤ä¸­çå¢å­æ ¹æ®è®¾ç½®çnicknameä¸ºåãä¹å¯ä»¥éè¿
+@å¢å­ ä»£æ¿ã
+ç°å¨æ²¡æé»è®¤è§¦åè¯äºï¼å¦ææ²¡æè®¾ç½®nicknameï¼å°±åªè½éè¿ @
+è§¦åäº æä»¤çç¸åè§¦åè¯å¯èªè¡æ¥çä»£ç ä¸­ aliases é¨åã |
+æä»¤ | æé | éè¦@ | èå´ | è¯´æ | |:-----:|:----:|:----:|:----:|:--
+--:| | å¢å­[èå¤©åå®¹] | ç¾¤å | å¦ | ç¾¤è / ç§è |
 æ¥åå¢å­èå¤©å§ï¼ | | @å¢å­[èå¤©åå®¹] | åä¸ | æ¯ | åä¸ |
-åä¸ | | å¢å­ççä½ç½® | ç¾¤å | å¦ | ç¾¤è / ç§è |
-æ¥çå¢å­èµåå°å | | åå²è®°å½ | ä¸»äºº | å¦ | ç¾¤è / ç§è |
-æ¥çåå²æé®ï¼ä¸åæ¬åç­ï¼ | ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£
-``` nb plugin install nonebot-plugin-tuan-chatgpt ```   ä½¿ç¨ git å®è£ ï¼
-æ¨è ï¼ æ¨èæ­¤æ¹å¼ï¼å ä¸ºè½å¤åæ¶æ¶å°æ´æ° å®è£ï¼å¨
-nonebot2 é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, ä½¿ç¨ git å®è£ ``` git
-clone https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git ``` åçº§ï¼
-``` git pull ```   ä½¿ç¨ pip å®è£ ``` pip install nonebot-plugin-tuan-
-chatgpt ```  ç¯å¢éç½®ï¼ æå¼nonebotç`.env` æä»¶ï¼åå¥æ¨ç
-`chatgpt_api` å¦æå¸æå¯ç¨ä»£çï¼åéè¦å¨`.env` æä»¶ä¸­ï¼åå¥
-`chat_use_proxy = True` ä»¥å `chat_proxy_address_https = "ä»£çå°å"` æ
-`chat_proxy_address_http = "ä»£çå°å"`
+åä¸ | | å¢å­ ççä½ç½® / ä½ å¨åªå¿ | ç¾¤å | å¦ | ç¾¤è / ç§è
+| æ¥çå¢å­èµåå°å | | å¢å­ åå²è®°å½ / history | ä¸»äºº | å¦ |
+ç¾¤è / ç§è | æ¥çåå²æé®ï¼ä¸åæ¬åç­ï¼ | | å¢å­
+æ¸é¤è®°å¿ / æ¸é¤åå²è®°å½ | ä¸»äºº | å¦ | ç¾¤è / ç§è |
+æ¸é¤å¢å­çè®°å¿ | ## ð¿ å®è£  ä½¿ç¨ nb-cli å®è£ ``` nb plugin
+install nonebot-plugin-tuan-chatgpt # åçº§ï¼ nb plugin update nonebot-
+plugin-tuan-chatgpt ```   ä½¿ç¨ git å®è£  å®è£ï¼å¨ nonebot2
+é¡¹ç®çæä»¶ç®å½ä¸, æå¼å½ä»¤è¡, ä½¿ç¨ git å®è£ ``` git clone
+https://github.com/TheLZY/nonebot_plugin_tuan_chatgpt.git ``` åçº§ï¼ ``` git
+pull ```   ä½¿ç¨ pip å®è£ ``` pip install nonebot-plugin-tuan-chatgpt ```
+ç¯å¢éç½®ï¼ æå¼nonebotç`.env` æä»¶ï¼åå¥æ¨ç `chatgpt_api`
+ä»¥å `nickname` å¦æå¸æå¯ç¨ä»£çï¼åéè¦å¨`.env`
+æä»¶ä¸­ï¼åå¥ `chat_use_proxy = True` ä»¥å `chat_proxy_address_https =
+"ä»£çå°å"` æ `chat_proxy_address_http = "ä»£çå°å"`
 (å¤çé»è¾ç±»ä¼¼openaiï¼ä¼åä½¿ç¨httpsãä½æ¯httpsç»å¸¸ä¼æ¥éï¼aiohttpåurllib3é½å¯è½ä¼é æé®é¢ï¼ï¼æ¨èåªä½¿ç¨http)
 å¦æå¸æå¯ç¨apiè½¬å (ç±»ä¼¼ [è¾è®¯äºå½æ°æ­å»º OpenAI å½åä»£ç]
 (https://github.com/Ice-Hazymoon/openai-scf-proxy)
 éè¿äºå½æ°ç­æ¹å¼å®ç°åä»£ )ï¼åéè¦åå¥åå¥
 `chat_use_api_forward = True` ä»¥å `chat_api_address = "ä»£çå°å"`
 ä½æ¯ä¸æ¨èä¸¤èåæ¶å¯ç¨
 å¦æå¸æå¯ç¨å¾çæ¸²æï¼åéè¦åå¥ `chat_use_img2text=True`,
@@ -66,31 +73,34 @@
 ä¹å¯ä»¥ç´æ¥ä¸è½½ Release ç [tuan_chatgpt.zip](https://github.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/files/11163988/tuan_chatgpt.zip) æå° `/data`
 éå»
 å¾çæ¸²æåè½å¯ç¨åï¼ä¼èªå¨å¯ç¨äºç»´ç æ·»å ä»¥åèæ¯å¾çæ·»å ãå¯ä»¥éæ©å³é­ã
 å·ä½éç½®æ¹å¼åè **âï¸ éç½®** ä»¥å [éç½® | Nonebot](https://
 v2.nonebot.dev/docs/tutorial/
 configuration#%E9%85%8D%E7%BD%AE%E6%96%B9%E5%BC%8F) egï¼ chatgpt_api = "sk-
-1145141919" # å¯ç¨ä»£ç chat_use_proxy=True chat_proxy_address_http='http://
-127.0.0.1:10809' chat_proxy_address_https='http://127.0.0.1:10809' #
-å¯ç¨apiè½¬å chat_use_api_forward=True chat_api_address="https://
-api.openai.com/v1" ï¼è¿ä¸ªæ¯å®æ¹æ¥å£ ç§çåæ²¡é®é¢ï¼å¤§æ¦ï¼
+1145141919" nickname = ['å¢å­', 'é·å§'] # å¯ç¨ä»£ç chat_use_proxy=True
+chat_proxy_address_http='http://127.0.0.1:10809'
+chat_proxy_address_https='http://127.0.0.1:10809' # å¯ç¨apiè½¬å
+chat_use_api_forward=True chat_api_address="https://api.openai.com/v1"
+ï¼è¿ä¸ªæ¯å®æ¹æ¥å£ ç§çåæ²¡é®é¢ï¼å¤§æ¦ï¼
 è¿æ¯å¾çå·ä½çè½¬åæ¹å¼ï¼ # å¯ç¨å¾çæ¸²æ
 chat_use_img2text=True å¦ææ²¡æèªå¨å¯¼å¥æä»¶çåè½ï¼éè¦æå¼
 nonebot2 é¡¹ç®æ ¹ç®å½ä¸ç `pyproject.toml` æä»¶, å¨ `[tool.nonebot]`
 é¨åè¿½å åå¥ plugins = ["nonebot_plugin_tuan_chatgpt"] ## âï¸ éç½®
 å¨ nonebot2 é¡¹ç®ç`.env`æä»¶ä¸­æ¯ææ·»å ä»¥ä¸éç½® å¿å¡«é¡¹ï¼ |
 éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :-----------------: | :----: | :-----------
--: | | chatgpt_api | æ  | stræ ¼å¼ | ä»£çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹
-| é»è®¤å¼ | è¯´æ | | :---------------------: | :----: | :-----------------
--: | | chat_use_proxy | False | æ¯å¦å¯ç¨ä»£ç | | chat_proxy_address |
-None | ä»£çå°å | | chat_use_api_forward | False | æ¯å¦å¯ç¨apiè½¬å |
-| chat_api_address | None | apiè½¬åå°å | æ¸²æå¾çç¸å³ï¼å¯éï¼ï¼
-| éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :------------------: | :------------------
------------: | :----------------------------: | | chat_use_img2text | False |
+-: | | chatgpt_api | æ  | stræ ¼å¼ | | nickname | æ  | list[str] | ps.
+è¿ä¸ªnicknameæ¯botéç¨çãå³ï¼å«çæä»¶ä¹è½è·åè¿ä¸ªåæ°ï¼ä¸è¿ä¸è¬ä¸ä¼æå¥å½±åã
+ä»£çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹ | é»è®¤å¼ | è¯´æ | | :-------------
+--------: | :----: | :------------------: | | chat_use_proxy | False |
+æ¯å¦å¯ç¨ä»£ç | | chat_proxy_address | None | ä»£çå°å | |
+chat_use_api_forward | False | æ¯å¦å¯ç¨apiè½¬å | | chat_api_address |
+None | apiè½¬åå°å | æ¸²æå¾çç¸å³ï¼å¯éï¼ï¼ | éç½®é¡¹ |
+é»è®¤å¼ | è¯´æ | | :------------------: | :-----------------------------: |
+:----------------------------: | | chat_use_img2text | False |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_use_qr | True |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_use_background | True |
 æ¯å¦æ¸²æææ¬å¹¶åéå¾ç | | chat_data_path | 'data/tuan_chatgpt' |
 æ°æ®è·¯å¾ãä¿®æ¹è¯·ç¨ç»å¯¹è·¯å¾ | | chat_font_path | 'font' |
 å­ä½è·¯å¾ï¼é»è®¤ä¸ºdata/tuan_chat/font) | | chat_background_path |
 "background" | èæ¯è·¯å¾ï¼é»è®¤ä¸ºdata/tuan_chat/backgroundï¼| |
 chat_font_name | 'sarasa-mono-sc-regular.ttf' | ä½¿ç¨çå­ä½ | |
@@ -103,33 +113,33 @@
 åéåç­é¿åº¦ | | user_freq_lim | 4 | éå¶ç¾¤ååè¨éåº¦ï¼ç§ï¼ |
 | group_freq_lim | 6 | éå¶ç¾¤ååè¨éåº¦ï¼ç§ï¼ | |
 conversation_remember_num | 7 | è½è®°ä½çå¯¹è¯æ°ç® | ## ð ææå¾
 å¾çæ¸²æ ![å¾çæ¸²æææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example_img2text.PNG) åå²è®°å½
 ![åå²è®°å½ææ](https://raw.githubusercontent.com/TheLZY/
 nonebot_plugin_tuan_chatgpt/master/examples/example_history.png) ## ð¡ TODO -
-[x] åç­åé ï¼éè¿åæ®µå®ç°ãå¯è½ä¼èèæ¢æå¾çåéï¼ -
-[x] æ¯æä½¿ç¨ä»£ç - [x] å¢å ä»£çæµè¯
+[x] åç¾¤è®°å¿ï¼æ¯ä¸ªç¾¤ä»¥åç§èï¼è®°å¿ä¸ä¼ä¸²ï¼ - [x]
+åç­åé ï¼éè¿åæ®µå®ç°ãå¯è½ä¼èèæ¢æå¾çåéï¼ - [x]
+æ¯æä½¿ç¨ä»£ç - [x] å¢å ä»£çæµè¯
 éè¿è¿åçipå°åå¤æ­ä»£çæ¯å¦ææ ç»èµèµåæè¡ä¸­ï¼  - [x]
 ç§èååè¨é¢çéå¶ã - [x] éè¯¯å¤ç  - [x] å¼æ­¥è°ç¨ä¼å
 ï¼èªå¨éè¯ / è¿åæ¥é  ï¼ - [x] éæºäººè®¾ æè§ä¼å¾æææï¼
-- [x] éè¿@è§¦å - [ ] ä¿®æ¹äººè®¾ ï¼ - [ ] markdown æ¸²æ ï¼ - [ ]
+- [x] éè¿@è§¦å - [ ] ä¿®æ¹äººè®¾ ï¼ - [ ] markdown æ¸²æ ï¼ - [x]
 ~~èªå®ä¹è§¦åæ¹å¼ï¼
 è¿ä¸ªåæ¯å¯ä»¥åä¿®æ¹è§¦åäººè®¾ä¸èµ·èå¨...ä¸è¿æè§å¨æä¿®æ¹æç¹éº»ç¦ã~~
-å¨nicknameéé¢å å§ï¼ä¹æºå¥½ - [ ] ~~Openai
+å¨nicknameéé¢å å§ãè¿æ¯ä¸é è½®å­äºã - [ ] ~~Openai
 æ½é£å¤çï¼ææ¶åªè¾åº 3*177 ä¸ªé¿åº¦çåç­
 å¯ä»¥æ ¹æ®ç¸åå­æ°åºç°æ¬¡æ°æ¥
 åä¸ä¸ªå­è¿ç»­åºç°6æ¬¡å¤å®ä¸ºæ½é£ï¼ï¼~~ æè¿æ²¡éå°
 é´å®ä¸ºä¸çæ¹å°±ä¸ä¼æé®é¢ - [ ] ~~é¿åç­åå¹¶è½¬å~~
 ä¼¼ä¹æ´å®¹æè¢«é£æ§ ç®äºã [åè](https://github.com/Ailitonia/omega-
 miya/issues/16#issuecomment-827432967)  **è§è² ~~è°æ~~ å®å¶ï¼**
-å¦æå¸ææ´æ¹è§¦åè¯­ï¼å¯ä»¥æ¾å°æºç å®è£ä½ç½®éç
-`__init__.py` æä»¶ï¼ä¿®æ¹ `chat_checker` ä¹å¯ä»¥è¿å¥ nonebot ç`.env`
-æä»¶ï¼å¨ `nickname` éæ·»å è§¦åè¯­
-å¦æå¸ææ´æ¹äººè®¾ï¼å¯ä»¥ä¿®æ¹ `utils.py` æä»¶ä¸­ç `MessageBox`
+å¦æå¸ææ´æ¹è§¦åè¯­ï¼å¯ä»¥è¿å¥ nonebot ç`.env` æä»¶ï¼å¨
+`nickname` éæ·»å è§¦åè¯­ å¦æå¸ææ´æ¹äººè®¾ï¼å¯ä»¥ä¿®æ¹
+`utils.py` æä»¶ä¸­ç `MessageBox` ä¸­ç `charactor` ç¸å³é¨å
 ï¼æ­£å¨æèæä¹ç¨èå¤©æ¥æ·»å äººè®¾
 ä¸è¿æè§è¦æ¶åçä¸è¥¿æ¯è¾å¤ ### ä¸äºç¢ç¢å¿µ
 conversation_remember_num
 æå¥½ä¸è¦è°å¾å¤ªé«ï¼è®°ä½å¤ªå¤è¯äºå°±ä¼åææ§å·æ·¡æºå¨äºº
 ð¥ åºç°äº wake up
 è¯ä¹ä¼ååå»ï¼ä¸è¿ç°å¨åºè¯¥å¤è¯´ä¸¤å¥è¯å°±å¥½äº
 é¿åç­å¤çï¼
@@ -165,20 +175,20 @@
 'å¶å®è¿ä¸ªé®é¢æ²¡ææ åç­æ¡ï¼æ¯ä¸ªäººçèº«é«é½æ¯ç¬ä¸æ äºçï¼éè¦ç'},
 {'role': 'user', 'content': 'å¢å­å¥½æ£'}, {'role': 'assistant', 'content':
 'è°¢è°¢ä½ ï¼ä½ ä¹å¾æ£å¦~'}, {'role': 'user', 'content':
 'å¢å­ï¼å¦ä½çå¾ä¸­å½çæç«¯å¥³æ³é®é¢'}] response = await
 openai.ChatCompletion.acreate( model = "gpt-3.5-turbo", messages =
 messages_error, frequency_penalty = - 0.8, # å¤ªé«äºå®¹æåºbug timeout = 30
 ) answer = response.choices[0].message.content ```  ## ð History
-**2023.4.4** - å¢å å¾çæ¸²æåè½ **2023.3.23** - å¢å  api è½¬åæ¯æ
-**2023.3.15** - æ·»å éæºäººè®¾ãé¢çäºä¿®æ¹äººè®¾çæ¥å£
-æç©ºåå¡«å - æ¯æéè¿@è§¦å **2023.3.14** - å¢å éè¯¯éè¯
-ï¼å¦æå¤±è´¥ èªå¨éè¯æå¤ä¸æ¬¡
-å¯¹äºæ¢¯å­ä¸ç¨³å®çæ¶åå¸®å©å¾å¤§ï¼ - å¢å æ¥éè¾åº
-ï¼3æ¬¡é½å¤±è´¥çè¯ çæ ~~æè¶£ç~~ æ¥éä¿¡æ¯
+**2023.5.13** - æ¯æåç¾¤è®°å¿ - å¢å æ¸é¤è®°å¿åè½ **2023.4.4** -
+å¢å å¾çæ¸²æåè½ **2023.3.23** - å¢å  api è½¬åæ¯æ **2023.3.15**
+- æ·»å éæºäººè®¾ãé¢çäºä¿®æ¹äººè®¾çæ¥å£ æç©ºåå¡«å -
+æ¯æéè¿@è§¦å **2023.3.14** - å¢å éè¯¯éè¯ ï¼å¦æå¤±è´¥
+èªå¨éè¯æå¤ä¸æ¬¡ å¯¹äºæ¢¯å­ä¸ç¨³å®çæ¶åå¸®å©å¾å¤§ï¼ -
+å¢å æ¥éè¾åº ï¼3æ¬¡é½å¤±è´¥çè¯ çæ ~~æè¶£ç~~ æ¥éä¿¡æ¯
 ä»¥ç¬¬ä¸æ¬¡å¤±è´¥è¿åç error ä¸ºåï¼ - ä¿®æ¹æ¶æ¯è§¦åå¨
 ~~è¯å¾éè¿@èå¤© å¤§å¤±è´¥~~ - å¢å ç§èé¢çéå¶
 é»è®¤ä¸º4ç§ä¸æ¬¡ **2023.3.12** - å¢å èµåå°åæ£æµåè½ -
 å¢å éæ©æ§è®°å½åè½ ï¼å»æä¼è®©å¥¹æ³èµ·æ¥èªå·±æ¯aiçåç­
 é¿åä¸ç´è¯´èªå·±æ¯aiï¼ **2023.3.10** - å¢å ä»£çæ¯æ **2023.3.9** -
 åæ¢æå®æ¹å¼æ­¥è°ç¨æ¥å£ ## â­ Special thanks to
 æ¬é¡¹ç®å¨å¼åè¿ç¨ä¸­ï¼åèäºä¸å°ä»¥ä¸é¡¹ç®ï¼å¯¹åä½è¡¨ç¤ºç±è¡·çæè°¢
```

