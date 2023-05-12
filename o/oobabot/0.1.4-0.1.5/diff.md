# Comparing `tmp/oobabot-0.1.4.tar.gz` & `tmp/oobabot-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "oobabot-0.1.4.tar", max compression
+gzip compressed data, was "oobabot-0.1.5.tar", max compression
```

## Comparing `oobabot-0.1.4.tar` & `oobabot-0.1.5.tar`

### file list

```diff
@@ -1,14 +1,21 @@
--rw-r--r--   0        0        0     1067 2023-05-04 00:39:46.200078 oobabot-0.1.4/LICENSE
--rw-r--r--   0        0        0    11382 2023-05-10 23:17:09.014151 oobabot-0.1.4/README.md
--rw-r--r--   0        0        0      967 2023-05-10 23:13:03.004218 oobabot-0.1.4/pyproject.toml
--rw-r--r--   0        0        0       80 2023-05-10 23:21:59.614073 oobabot-0.1.4/src/oobabot/__init__.py
--rw-r--r--   0        0        0       69 2023-05-09 03:46:59.468832 oobabot-0.1.4/src/oobabot/__main__.py
--rw-r--r--   0        0        0    27234 2023-05-10 02:23:25.013734 oobabot-0.1.4/src/oobabot/discord_bot.py
--rw-r--r--   0        0        0     1572 2023-05-09 03:46:59.468832 oobabot-0.1.4/src/oobabot/fancy_logging.py
--rw-r--r--   0        0        0     4989 2023-05-10 00:01:52.945718 oobabot-0.1.4/src/oobabot/ooba_client.py
--rwxr-xr-x   0        0        0     2645 2023-05-10 01:43:04.854299 oobabot-0.1.4/src/oobabot/oobabot.py
--rw-r--r--   0        0        0     6586 2023-05-09 03:46:59.468832 oobabot-0.1.4/src/oobabot/response_stats.py
--rw-r--r--   0        0        0    10818 2023-05-10 00:01:52.945718 oobabot-0.1.4/src/oobabot/sd_client.py
--rw-r--r--   0        0        0     2695 2023-05-09 03:46:59.468832 oobabot-0.1.4/src/oobabot/sentence_splitter.py
--rw-r--r--   0        0        0     6656 2023-05-10 01:39:31.894349 oobabot-0.1.4/src/oobabot/settings.py
--rw-r--r--   0        0        0    12218 1970-01-01 00:00:00.000000 oobabot-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-05-03 00:11:59.534663 oobabot-0.1.5/LICENSE
+-rw-r--r--   0        0        0    12401 2023-05-12 21:59:07.554398 oobabot-0.1.5/README.md
+-rw-r--r--   0        0        0      967 2023-05-12 21:59:53.189975 oobabot-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0       80 2023-05-12 22:00:00.522861 oobabot-0.1.5/src/oobabot/__init__.py
+-rw-r--r--   0        0        0       69 2023-05-05 00:57:20.206747 oobabot-0.1.5/src/oobabot/__main__.py
+-rw-r--r--   0        0        0     6356 2023-05-12 21:31:34.953554 oobabot-0.1.5/src/oobabot/decide_to_respond.py
+-rw-r--r--   0        0        0     8499 2023-05-12 21:41:24.362388 oobabot-0.1.5/src/oobabot/discord_bot.py
+-rw-r--r--   0        0        0     1572 2023-05-12 09:20:17.327499 oobabot-0.1.5/src/oobabot/fancy_logging.py
+-rw-r--r--   0        0        0     1099 2023-05-12 09:21:18.606212 oobabot-0.1.5/src/oobabot/http_client.py
+-rw-r--r--   0        0        0     8134 2023-05-12 20:40:24.610786 oobabot-0.1.5/src/oobabot/image_generator.py
+-rw-r--r--   0        0        0     4092 2023-05-12 13:22:04.074586 oobabot-0.1.5/src/oobabot/ooba_client.py
+-rwxr-xr-x   0        0        0     5815 2023-05-12 21:26:10.891395 oobabot-0.1.5/src/oobabot/oobabot.py
+-rw-r--r--   0        0        0     7520 2023-05-12 10:30:14.671081 oobabot-0.1.5/src/oobabot/prompt_generator.py
+-rw-r--r--   0        0        0     2334 2023-05-12 21:49:59.613778 oobabot-0.1.5/src/oobabot/repetition_tracker.py
+-rw-r--r--   0        0        0     6605 2023-05-12 09:53:03.857841 oobabot-0.1.5/src/oobabot/response_stats.py
+-rw-r--r--   0        0        0    10177 2023-05-12 21:02:06.616260 oobabot-0.1.5/src/oobabot/sd_client.py
+-rw-r--r--   0        0        0     2695 2023-05-12 09:19:49.870308 oobabot-0.1.5/src/oobabot/sentence_splitter.py
+-rw-r--r--   0        0        0    11050 2023-05-12 22:01:40.925524 oobabot-0.1.5/src/oobabot/settings.py
+-rw-r--r--   0        0        0     5512 2023-05-12 21:38:15.155746 oobabot-0.1.5/src/oobabot/templates.py
+-rw-r--r--   0        0        0     1572 2023-05-12 10:48:40.662797 oobabot-0.1.5/src/oobabot/types.py
+-rw-r--r--   0        0        0    13237 1970-01-01 00:00:00.000000 oobabot-0.1.5/PKG-INFO
```

### Comparing `oobabot-0.1.4/LICENSE` & `oobabot-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `oobabot-0.1.4/README.md` & `oobabot-0.1.5/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -68,62 +68,83 @@
 
 ~: oobabot --base-url ws://oobabooga-hostname:5005/ --ai-name YourBotsName --persona "You are a cat named YourBotsName"
 ```
 
 You should now be able to run oobabot from wherever pip installed it.
 
 ```none
-usage: oobabot [-h] [--ai-name AI_NAME] [--wakewords [WAKEWORDS ...]] [--ignore-dms]
-               [--base-url BASE_URL] [--persona PERSONA] [--log-all-the-things]
-               [--stable-diffusion-url STABLE_DIFFUSION_URL]
+usage: oobabot [-h] [--history-lines HISTORY_LINES] [--ignore-dms]
+               [--wakewords [WAKEWORDS ...]] [--ai-name AI_NAME] [--base-url BASE_URL]
+               [--log-all-the-things] [--persona PERSONA]
+               [--diffusion-steps DIFFUSION_STEPS] [--image-height IMAGE_HEIGHT]
+               [--image-width IMAGE_WIDTH] [--image-words [IMAGE_WORDS ...]]
                [--stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER]
-               [--stable-diffusion-negative-prompt STABLE_DIFFUSION_NEGATIVE_PROMPT]
-               [--stable-diffusion-negative-prompt-nsfw STABLE_DIFFUSION_NEGATIVE_PROMPT_NSFW]
+               [--stable-diffusion-url STABLE_DIFFUSION_URL]
+               [--sd-negative-prompt SD_NEGATIVE_PROMPT]
+               [--sd-negative-prompt-nsfw SD_NEGATIVE_PROMPT_NSFW]
 
 Discord bot for oobabooga's text-generation-webui
 
 options:
   -h, --help            show this help message and exit
 
 Discord Settings:
-  --ai-name AI_NAME     Name of the AI to use for requests. This can be whatever you want, but
-                        might make sense to be the name of the bot in Discord.
-  --wakewords [WAKEWORDS ...]
-                        One or more words that the bot will listen for. The bot will listen in all
-                        discord channels can access for one of these words to be mentioned, then
-                        reply to any messages it sees with a matching word. The bot will always
-                        reply to @-mentions and direct messages, even if no wakewords are supplied.
+  --history-lines HISTORY_LINES
+                        Number of lines of history to supply to the AI. This is the number
+                        of lines of history that the AI will see when generating a response.
+                        The default is 20.
   --ignore-dms          If set, the bot will ignore direct messages.
+  --wakewords [WAKEWORDS ...]
+                        One or more words that the bot will listen for. The bot will listen
+                        in all discord channels can access for one of these words to be
+                        mentioned, then reply to any messages it sees with a matching word.
+                        The bot will always reply to @-mentions and direct messages, even if
+                        no wakewords are supplied.
 
 Oobabooga Seetings:
-  --base-url BASE_URL   Base URL for the oobabooga instance. This should be ws://hostname[:port]
-                        for plain websocket connections, or wss://hostname[:port] for websocket
-                        connections over TLS.
-  --persona PERSONA     This prefix will be added in front of every user-supplied request. This is
-                        useful for setting up a 'character' for the bot to play. Alternatively,
-                        this can be set with the OOBABOT_PERSONA environment variable.
-  --log-all-the-things  Prints all oobabooga requests and responses in their entirety to STDOUT
+  --ai-name AI_NAME     Name of the AI to use for requests. This can be whatever you want,
+                        but might make sense to be the name of the bot in Discord.
+  --base-url BASE_URL   Base URL for the oobabooga instance. This should be
+                        ws://hostname[:port] for plain websocket connections, or
+                        wss://hostname[:port] for websocket connections over TLS.
+  --log-all-the-things  Prints all oobabooga requests and responses in their entirety to
+                        STDOUT
+  --persona PERSONA     This prefix will be added in front of every user-supplied request.
+                        This is useful for setting up a 'character' for the bot to play.
+                        Alternatively, this can be set with the OOBABOT_PERSONA environment
+                        variable.
 
 Stable Diffusion Settings:
-  --stable-diffusion-url STABLE_DIFFUSION_URL
+  --diffusion-steps DIFFUSION_STEPS
+                        Number of diffusion steps to take when generating an image. The
+                        default is 30.
+  --image-height IMAGE_HEIGHT
+                        Size of images to generate. This is the height of the image in
+                        pixels. The default is 512.
+  --image-width IMAGE_WIDTH
+                        Size of images to generate. This is the width of the image in
+                        pixels. The default is 512.
+  --image-words [IMAGE_WORDS ...]
+                        One or more words that will indicate the user is requeting an image
+                        to be generated.
+  --stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER, --sd-sampler STABLE_DIFFUSION_SAMPLER
+                        Sampler to use when generating images. If not specified, the one set
+                        on the AUTOMATIC1111 server will be used.
+  --stable-diffusion-url STABLE_DIFFUSION_URL, --sd-url STABLE_DIFFUSION_URL
                         URL for an AUTOMATIC1111 Stable Diffusion server
-  --stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER
-                        Sampler to use when generating images. If not specified, the one set on the
-                        AUTOMATIC1111 server will be used.
-  --stable-diffusion-negative-prompt STABLE_DIFFUSION_NEGATIVE_PROMPT
-                        Negative prompt to use when generating images. This will discourage Stable
-                        Diffusion from generating images with the specified content. By default,
-                        this is set to follow Discord's TOS.
-  --stable-diffusion-negative-prompt-nsfw STABLE_DIFFUSION_NEGATIVE_PROMPT_NSFW
-                        Negative prompt to use when generating images in a channel marked as'Age-
-                        Restricted'. By default, this follows the Discord TOS by allowing some
-                        sexual content forbidden in non-age-restricted channels.
+  --sd-negative-prompt SD_NEGATIVE_PROMPT
+                        Negative prompt to use when generating images. This will discourage
+                        Stable Diffusion from generating images with the specified content.
+                        By default, this is set to follow Discord's TOS.
+  --sd-negative-prompt-nsfw SD_NEGATIVE_PROMPT_NSFW
+                        Negative prompt to use when generating images in a channel marked
+                        as'Age-Restricted'.
 
-Also, to authenticate to Discord, you must set the environment variable: DISCORD_TOKEN = <your
-bot's discord token>
+Also, to authenticate to Discord, you must set the environment variable: DISCORD_TOKEN =
+<your bot's discord token>
 ```
 
 ## Required settings
 
 - **`DISCORD_TOKEN`** environment variable
 
    Set your shell environment's **`DISCORD_TOKEN`** to token Discord provided when you set up the bot account.  It should be something like a 72-character-long random-looking string.
```

### Comparing `oobabot-0.1.4/pyproject.toml` & `oobabot-0.1.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "oobabot"
-version = "0.1.4"
+version = "0.1.5"
 description = "A Discord bot which talks to Large Language Model AIs running on oobabooga's text-generation-webui"
 authors = ["Christopher Rude <chris@rudesoftware.net>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/chrisrude/oobabot"
 
 [tool.poetry.dependencies]
```

### Comparing `oobabot-0.1.4/src/oobabot/fancy_logging.py` & `oobabot-0.1.5/src/oobabot/fancy_logging.py`

 * *Files identical despite different names*

### Comparing `oobabot-0.1.4/src/oobabot/ooba_client.py` & `oobabot-0.1.5/src/oobabot/ooba_client.py`

 * *Files 15% similar despite different names*

```diff
@@ -5,68 +5,44 @@
 from asyncio.exceptions import TimeoutError
 from socket import gaierror
 import typing
 
 import aiohttp
 
 from oobabot.fancy_logging import get_logger
+from oobabot.http_client import OobaClientError
+from oobabot.http_client import SerializedHttpClient
 from oobabot.sentence_splitter import SentenceSplitter
+from oobabot.settings import Settings
 
 
-class OobaClientError(Exception):
-    pass
-
-
-class OobaClient:
+class OobaClient(SerializedHttpClient):
     # Purpose: Streaming client for the Ooba API.
     # Can provide the response by token or by sentence.
 
+    OOBABOOGA_STREAMING_URI_PATH: str = "/api/v1/stream"
+
     END_OF_INPUT = ""
 
     def __init__(self, base_url: str):
-        self.base_url = base_url
+        super().__init__(base_url)
         self.total_response_tokens = 0
-        self._session = None
-
-    DEFAULT_REQUEST_PARAMS = {
-        "max_new_tokens": 250,
-        "do_sample": True,
-        "temperature": 1.3,
-        "top_p": 0.1,
-        "typical_p": 1,
-        "repetition_penalty": 1.18,
-        "top_k": 40,
-        "min_length": 0,
-        "no_repeat_ngram_size": 0,
-        "num_beams": 1,
-        "penalty_alpha": 0,
-        "length_penalty": 1,
-        "early_stopping": False,
-        "seed": -1,
-        "add_bos_token": True,
-        "truncation_length": 2048,
-        "ban_eos_token": False,
-        "skip_special_tokens": True,
-        "stopping_strings": [],
-    }
-
-    STREAMING_URI_PATH = "/api/v1/stream"
 
     async def setup(self):
         """
         Attempt to connect to the oobabooga server.
 
         Returns:
             nothing, if the connection test was successful
 
         Raises:
             OobaClientError, if the connection fails
         """
         try:
-            async with self.get_session().ws_connect(self.STREAMING_URI_PATH):
+            async with self.get_session().ws_connect(self.OOBABOOGA_STREAMING_URI_PATH):
                 return
         except (
             ConnectionRefusedError,
             gaierror,
             TimeoutError,
         ) as e:
             raise OobaClientError(f"Failed to connect to {self.base_url}: {e}", e)
@@ -82,20 +58,22 @@
                 yield sentence
 
     async def request_by_token(self, prompt: str) -> typing.AsyncIterator[str]:
         """
         Yields each token of the response as it arrives.
         """
 
-        request = {
+        request: dict[str, bool | float | int | str | typing.List[typing.Any]] = {
             "prompt": prompt,
         }
-        request.update(self.DEFAULT_REQUEST_PARAMS)
+        request.update(Settings.OOBABOOGA_DEFAULT_REQUEST_PARAMS)
 
-        async with self.get_session().ws_connect(self.STREAMING_URI_PATH) as websocket:
+        async with self.get_session().ws_connect(
+            self.OOBABOOGA_STREAMING_URI_PATH
+        ) as websocket:
             await websocket.send_json(request)
 
             async for msg in websocket:
                 # we expect a series of text messages in JSON encoding,
                 # like this:
                 #
                 # {"event": "text_stream", "message_num": 0, "text": ""}
@@ -126,24 +104,7 @@
                     get_logger().error(f"WebSocket connection closed with error: {msg}")
                     raise OobaClientError(
                         f"WebSocket connection closed with error {msg}"
                     )
                 elif msg.type == aiohttp.WSMsgType.CLOSED:
                     get_logger().info(f"WebSocket connection closed normally: {msg}")
                     return
-
-    def get_session(self) -> aiohttp.ClientSession:
-        if not self._session:
-            raise OobaClientError("Session not initialized")
-        return self._session
-
-    async def __aenter__(self):
-        connector = aiohttp.TCPConnector(limit_per_host=1)
-        self._session = aiohttp.ClientSession(
-            base_url=self.base_url, connector=connector
-        )
-        return self
-
-    async def __aexit__(self, *_err):
-        if self._session:
-            await self._session.close()
-        self._session = None
```

### Comparing `oobabot-0.1.4/src/oobabot/response_stats.py` & `oobabot-0.1.5/src/oobabot/response_stats.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,37 +1,37 @@
 import time
+from typing import Callable
 
 from oobabot.fancy_logging import get_logger
-from oobabot.ooba_client import OobaClient
 
 
 class ResponseStats:
     """
     Purpose: collects timing and rate statistics for a single response
     """
 
-    def __init__(self, ooba_client: OobaClient, prompt: str):
-        self.ooba_client = ooba_client
+    def __init__(self, fn_get_total_tokens: Callable[[], int], prompt: str):
+        self.fn_get_total_tokens = fn_get_total_tokens
         self.start_time = time.time()
-        self.start_tokens = ooba_client.total_response_tokens
+        self.start_tokens = fn_get_total_tokens()
         self.duration = 0
         self.latency = 0
         self.tokens = 0
         self.prompt_len = len(prompt)
 
     def log_response_part(self) -> None:
         """
         Call this each time the response is updated by the AI.
         """
 
         now = time.time()
         if not self.latency:
             self.latency = now - self.start_time
         self.duration = now - self.start_time
-        self.tokens = self.ooba_client.total_response_tokens - self.start_tokens
+        self.tokens = self.fn_get_total_tokens() - self.start_tokens
 
     def tokens_per_second(self) -> float:
         """
         Returns the rate at which tokens were generated, in tokens per second.
         """
         if not self.duration:
             return 0
@@ -52,33 +52,33 @@
 
 
 class AggregateResponseStats:
     """
     Purpose: collects timing and rate statistics for all AggregateResponseStats
     """
 
-    def __init__(self, ooba_client: OobaClient):
-        self.ooba_client = ooba_client
+    def __init__(self, fn_get_total_tokens: Callable[[], int]):
         self.total_requests_received = 0
         self.total_successful_responses = 0
         self.total_failed_responses = 0
         self.total_response_time_seconds = 0
         self.total_response_latency_seconds = 0
         self.prompt_max_chars = 0
         self.prompt_min_chars = 0
         self.prompt_total_chars = 0
+        self.fn_get_total_tokens = fn_get_total_tokens
 
     def log_request_arrived(self, prompt) -> ResponseStats:
         """
         Call this when a request has arrived.
         This must be followed by zero or more calls
         to log_response_part(), and then exactly one call to
         either log_response_failure() or log_response_success().
         """
-        result = ResponseStats(self.ooba_client, prompt)
+        result = ResponseStats(self.fn_get_total_tokens, prompt)
 
         self.total_requests_received += 1
         # update the prompt stats now
         if self.prompt_max_chars < result.prompt_len:
             self.prompt_max_chars = result.prompt_len
         if self.prompt_min_chars > result.prompt_len:
             self.prompt_min_chars = result.prompt_len
@@ -132,15 +132,15 @@
     def average_tokens_per_second(self) -> float:
         """
         Returns the average rate at which tokens were generated,
         in tokens per second.
         """
         if 0 == self.total_successful_responses:
             return 0.0
-        return self.ooba_client.total_response_tokens / self.total_response_time_seconds
+        return self.fn_get_total_tokens() / self.total_response_time_seconds
 
     def average_prompt_length(self) -> float:
         """
         Returns the average prompt length in characters.
         """
         if 0 == self.total_requests_received:
             return 0.0
```

### Comparing `oobabot-0.1.4/src/oobabot/sd_client.py` & `oobabot-0.1.5/src/oobabot/sd_client.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,76 +6,73 @@
 import base64
 import time
 from typing import Dict
 
 import aiohttp
 
 from oobabot.fancy_logging import get_logger
+from oobabot.http_client import SerializedHttpClient
 
 
 class StableDiffusionClientError(Exception):
     pass
 
 
 # todo: response stats for SD client
-# todo: refactor to share code with ooba_client
 
 
-class StableDiffusionClient:
-    # Purpose: Client for a Stable Diffusion API.
-
-    DEFAULT_IMG_WIDTH = 512
-    DEFAULT_IMG_HEIGHT = DEFAULT_IMG_WIDTH
-    DEFAULT_STEPS = 30
-
-    API_URI_PATH = "/sdapi/v1/"
+class StableDiffusionClient(SerializedHttpClient):
+    """
+    Purpose: Client for generating images using the AUTOMATIC1111
+    API.  Takes a prompt and returns image binary data in PNG format.
+    """
 
     LOG_PREFIX = "Stable Diffusion: "
+    STABLE_DIFFUSION_API_URI_PATH: str = "/sdapi/v1/"
 
     API_COMMAND_URLS = {
-        "get_samplers": API_URI_PATH + "samplers",
+        "get_samplers": STABLE_DIFFUSION_API_URI_PATH + "samplers",
         # get_samplers: GET only
         #   returns a list of samplers which we can use
         #   in text2img
-        "options": API_URI_PATH + "options",
+        "options": STABLE_DIFFUSION_API_URI_PATH + "options",
         # options: GET and POST
         #   retrieves (GET) and sets (POST) global options
         #   for the server.  This is how we set the checkpoint
         #   and also a few privacy-related fields.
-        "progress": API_URI_PATH + "progress",
+        "progress": STABLE_DIFFUSION_API_URI_PATH + "progress",
         # progress: GET only
         #   returns the progress of the current image generation
-        "txt2img": API_URI_PATH + "txt2img",
+        "txt2img": STABLE_DIFFUSION_API_URI_PATH + "txt2img",
         # txt2img: POST only
         #   takes a prompt, generates an image and returns it
     }
 
     def __init__(
         self,
         base_url: str,
         negative_prompt: str,
         negative_prompt_nsfw: str,
+        image_width: int,
+        image_height: int,
+        steps: int,
         desired_sampler: str | None = None,
-        img_width: int = DEFAULT_IMG_WIDTH,
-        img_height: int = DEFAULT_IMG_HEIGHT,
-        steps: int = DEFAULT_STEPS,
     ):
-        self._base_url = base_url
+        super().__init__(base_url)
 
         self.negative_prompt = negative_prompt
         self.negative_prompt_nsfw = negative_prompt_nsfw
 
         self._sampler = None
         self.desired_sampler = desired_sampler
 
-        self._img_width = img_width
-        self._img_height = img_height
+        self.image_width = image_width
+        self.image_height = image_height
 
         self._steps = steps
-        self._session = None
 
     # set default negative prompts to make it more difficult
     # to create content against the discord TOS
     # https://discord.com/guidelines
 
     DEFAULT_REQUEST_PARAMS: Dict[str, bool | int | str] = {
         # default values are commented out
@@ -129,15 +126,15 @@
         # reasons;
         #  - show the user exactly what we changed, if anything
         #  - some versions of the API don't support the
         #    "do_not_add_watermark" option, so we need to
         #    check if it's there before we try to set it
         #
         current_options = None
-        async with (await self._get_session()).get(url) as response:
+        async with self.get_session().get(url) as response:
             if response.status != 200:
                 raise StableDiffusionClientError(response)
             current_options = await response.json()
 
         # now, set the options
         options_to_set = {}
         for k, v in self.DEFAULT_OPTIONS.items():
@@ -154,37 +151,32 @@
 
         if not options_to_set:
             get_logger().debug(
                 self.LOG_PREFIX + "Options are already set correctly, no changes made."
             )
             return
 
-        async with (await self._get_session()).post(
-            url, json=options_to_set
-        ) as response:
+        async with self.get_session().post(url, json=options_to_set) as response:
             if response.status != 200:
                 raise StableDiffusionClientError(response)
             await response.json()
 
     async def get_samplers(self) -> list[str]:
         url = self.API_COMMAND_URLS["get_samplers"]
-        async with (await self._get_session()).get(url) as response:
+        async with self.get_session().get(url) as response:
             if response.status != 200:
                 raise StableDiffusionClientError(response)
             response = await response.json()
             samplers = [str(sampler["name"]) for sampler in response]
             return samplers
 
     def generate_image(
         self,
         prompt: str,
         is_channel_nsfw: bool = False,
-        steps: int = DEFAULT_STEPS,
-        width: int = DEFAULT_IMG_WIDTH,
-        height: int = DEFAULT_IMG_HEIGHT,
     ) -> asyncio.Task[bytes]:
         # Purpose: Generate an image from a prompt.
         # Args:
         #     prompt: The prompt to generate an image from.
         #     negative_prompt: The negative prompt to use.
         #     sampler_name: The sampler to use.
         #     steps: The number of steps to use.
@@ -198,30 +190,30 @@
         negative_prompt = self.negative_prompt
         if is_channel_nsfw:
             negative_prompt = self.negative_prompt_nsfw
         request.update(
             {
                 "prompt": prompt,
                 "negative_prompt": negative_prompt,
-                "steps": steps,
-                "width": width,
-                "height": height,
+                "steps": self._steps,
+                "width": self.image_width,
+                "height": self.image_height,
             }
         )
         if self._sampler is not None:
             request["sampler_name"] = self._sampler
 
         async def do_post() -> bytes:
             get_logger().debug(
                 self.LOG_PREFIX
                 + f"Image request (nsfw: {is_channel_nsfw}): {request['prompt']}"
             )
             start_time = time.time()
 
-            async with (await self._get_session()).post(
+            async with self.get_session().post(
                 self.API_COMMAND_URLS["txt2img"],
                 json=request,
             ) as response:
                 if response.status != 200:
                     raise StableDiffusionClientError(response)
                 duration = time.time() - start_time
                 json_body = await response.json()
@@ -250,31 +242,14 @@
                         + f"Connection reset error: {e}, retrying in 1 second"
                     )
                     await asyncio.sleep(1)
                     tries += 1
 
         return asyncio.create_task(do_post_with_retry())
 
-    async def _get_session(self) -> aiohttp.ClientSession:
-        if self._session is None:
-            raise RuntimeError("session not initialized")
-        return self._session
-
-    async def __aenter__(self):
-        connector = aiohttp.TCPConnector(limit_per_host=1)
-        self._session = aiohttp.ClientSession(
-            base_url=self._base_url, connector=connector
-        )
-        return self
-
-    async def __aexit__(self, *_err):
-        if self._session:
-            await self._session.close()
-        self._session = None
-
     async def set_sampler(self):
         """Sets the sampler to use, if it is available."""
         samplers = await self.get_samplers()
         if self.desired_sampler is not None:
             if self.desired_sampler in samplers:
                 get_logger().debug(
                     self.LOG_PREFIX + "Using desired sampler '%s'", self.desired_sampler
```

### Comparing `oobabot-0.1.4/src/oobabot/sentence_splitter.py` & `oobabot-0.1.5/src/oobabot/sentence_splitter.py`

 * *Files identical despite different names*

### Comparing `oobabot-0.1.4/PKG-INFO` & `oobabot-0.1.5/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: oobabot
-Version: 0.1.4
+Version: 0.1.5
 Summary: A Discord bot which talks to Large Language Model AIs running on oobabooga's text-generation-webui
 Home-page: https://github.com/chrisrude/oobabot
 License: MIT
 Author: Christopher Rude
 Author-email: chris@rudesoftware.net
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
@@ -89,62 +89,83 @@
 
 ~: oobabot --base-url ws://oobabooga-hostname:5005/ --ai-name YourBotsName --persona "You are a cat named YourBotsName"
 ```
 
 You should now be able to run oobabot from wherever pip installed it.
 
 ```none
-usage: oobabot [-h] [--ai-name AI_NAME] [--wakewords [WAKEWORDS ...]] [--ignore-dms]
-               [--base-url BASE_URL] [--persona PERSONA] [--log-all-the-things]
-               [--stable-diffusion-url STABLE_DIFFUSION_URL]
+usage: oobabot [-h] [--history-lines HISTORY_LINES] [--ignore-dms]
+               [--wakewords [WAKEWORDS ...]] [--ai-name AI_NAME] [--base-url BASE_URL]
+               [--log-all-the-things] [--persona PERSONA]
+               [--diffusion-steps DIFFUSION_STEPS] [--image-height IMAGE_HEIGHT]
+               [--image-width IMAGE_WIDTH] [--image-words [IMAGE_WORDS ...]]
                [--stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER]
-               [--stable-diffusion-negative-prompt STABLE_DIFFUSION_NEGATIVE_PROMPT]
-               [--stable-diffusion-negative-prompt-nsfw STABLE_DIFFUSION_NEGATIVE_PROMPT_NSFW]
+               [--stable-diffusion-url STABLE_DIFFUSION_URL]
+               [--sd-negative-prompt SD_NEGATIVE_PROMPT]
+               [--sd-negative-prompt-nsfw SD_NEGATIVE_PROMPT_NSFW]
 
 Discord bot for oobabooga's text-generation-webui
 
 options:
   -h, --help            show this help message and exit
 
 Discord Settings:
-  --ai-name AI_NAME     Name of the AI to use for requests. This can be whatever you want, but
-                        might make sense to be the name of the bot in Discord.
-  --wakewords [WAKEWORDS ...]
-                        One or more words that the bot will listen for. The bot will listen in all
-                        discord channels can access for one of these words to be mentioned, then
-                        reply to any messages it sees with a matching word. The bot will always
-                        reply to @-mentions and direct messages, even if no wakewords are supplied.
+  --history-lines HISTORY_LINES
+                        Number of lines of history to supply to the AI. This is the number
+                        of lines of history that the AI will see when generating a response.
+                        The default is 20.
   --ignore-dms          If set, the bot will ignore direct messages.
+  --wakewords [WAKEWORDS ...]
+                        One or more words that the bot will listen for. The bot will listen
+                        in all discord channels can access for one of these words to be
+                        mentioned, then reply to any messages it sees with a matching word.
+                        The bot will always reply to @-mentions and direct messages, even if
+                        no wakewords are supplied.
 
 Oobabooga Seetings:
-  --base-url BASE_URL   Base URL for the oobabooga instance. This should be ws://hostname[:port]
-                        for plain websocket connections, or wss://hostname[:port] for websocket
-                        connections over TLS.
-  --persona PERSONA     This prefix will be added in front of every user-supplied request. This is
-                        useful for setting up a 'character' for the bot to play. Alternatively,
-                        this can be set with the OOBABOT_PERSONA environment variable.
-  --log-all-the-things  Prints all oobabooga requests and responses in their entirety to STDOUT
+  --ai-name AI_NAME     Name of the AI to use for requests. This can be whatever you want,
+                        but might make sense to be the name of the bot in Discord.
+  --base-url BASE_URL   Base URL for the oobabooga instance. This should be
+                        ws://hostname[:port] for plain websocket connections, or
+                        wss://hostname[:port] for websocket connections over TLS.
+  --log-all-the-things  Prints all oobabooga requests and responses in their entirety to
+                        STDOUT
+  --persona PERSONA     This prefix will be added in front of every user-supplied request.
+                        This is useful for setting up a 'character' for the bot to play.
+                        Alternatively, this can be set with the OOBABOT_PERSONA environment
+                        variable.
 
 Stable Diffusion Settings:
-  --stable-diffusion-url STABLE_DIFFUSION_URL
+  --diffusion-steps DIFFUSION_STEPS
+                        Number of diffusion steps to take when generating an image. The
+                        default is 30.
+  --image-height IMAGE_HEIGHT
+                        Size of images to generate. This is the height of the image in
+                        pixels. The default is 512.
+  --image-width IMAGE_WIDTH
+                        Size of images to generate. This is the width of the image in
+                        pixels. The default is 512.
+  --image-words [IMAGE_WORDS ...]
+                        One or more words that will indicate the user is requeting an image
+                        to be generated.
+  --stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER, --sd-sampler STABLE_DIFFUSION_SAMPLER
+                        Sampler to use when generating images. If not specified, the one set
+                        on the AUTOMATIC1111 server will be used.
+  --stable-diffusion-url STABLE_DIFFUSION_URL, --sd-url STABLE_DIFFUSION_URL
                         URL for an AUTOMATIC1111 Stable Diffusion server
-  --stable-diffusion-sampler STABLE_DIFFUSION_SAMPLER
-                        Sampler to use when generating images. If not specified, the one set on the
-                        AUTOMATIC1111 server will be used.
-  --stable-diffusion-negative-prompt STABLE_DIFFUSION_NEGATIVE_PROMPT
-                        Negative prompt to use when generating images. This will discourage Stable
-                        Diffusion from generating images with the specified content. By default,
-                        this is set to follow Discord's TOS.
-  --stable-diffusion-negative-prompt-nsfw STABLE_DIFFUSION_NEGATIVE_PROMPT_NSFW
-                        Negative prompt to use when generating images in a channel marked as'Age-
-                        Restricted'. By default, this follows the Discord TOS by allowing some
-                        sexual content forbidden in non-age-restricted channels.
+  --sd-negative-prompt SD_NEGATIVE_PROMPT
+                        Negative prompt to use when generating images. This will discourage
+                        Stable Diffusion from generating images with the specified content.
+                        By default, this is set to follow Discord's TOS.
+  --sd-negative-prompt-nsfw SD_NEGATIVE_PROMPT_NSFW
+                        Negative prompt to use when generating images in a channel marked
+                        as'Age-Restricted'.
 
-Also, to authenticate to Discord, you must set the environment variable: DISCORD_TOKEN = <your
-bot's discord token>
+Also, to authenticate to Discord, you must set the environment variable: DISCORD_TOKEN =
+<your bot's discord token>
 ```
 
 ## Required settings
 
 - **`DISCORD_TOKEN`** environment variable
 
    Set your shell environment's **`DISCORD_TOKEN`** to token Discord provided when you set up the bot account.  It should be something like a 72-character-long random-looking string.
```

