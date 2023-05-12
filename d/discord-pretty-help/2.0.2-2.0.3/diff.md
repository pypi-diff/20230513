# Comparing `tmp/discord_pretty_help-2.0.2.tar.gz` & `tmp/discord_pretty_help-2.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "discord_pretty_help-2.0.2.tar", max compression
+gzip compressed data, was "discord_pretty_help-2.0.3.tar", max compression
```

## Comparing `discord_pretty_help-2.0.2.tar` & `discord_pretty_help-2.0.3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1090 2023-05-01 15:55:28.427405 discord_pretty_help-2.0.2/LICENSE
--rw-r--r--   0        0        0      105 2023-05-01 15:55:28.443661 discord_pretty_help-2.0.2/pretty_help/__init__.py
--rw-r--r--   0        0        0      500 2023-05-01 15:55:28.443661 discord_pretty_help-2.0.2/pretty_help/abc_menu.py
--rw-r--r--   0        0        0     4184 2023-05-01 15:55:28.444660 discord_pretty_help-2.0.2/pretty_help/app_menu.py
--rw-r--r--   0        0        0     5332 2023-05-01 15:55:28.445658 discord_pretty_help-2.0.2/pretty_help/emoji_menu.py
--rw-r--r--   0        0        0    22753 2023-05-01 15:55:28.446687 discord_pretty_help-2.0.2/pretty_help/pretty_help.py
--rw-r--r--   0        0        0      747 2023-05-01 16:27:57.343550 discord_pretty_help-2.0.2/pyproject.toml
--rw-r--r--   0        0        0     3784 2023-05-01 15:55:28.428405 discord_pretty_help-2.0.2/README.md
--rw-r--r--   0        0        0     4460 1970-01-01 00:00:00.000000 discord_pretty_help-2.0.2/PKG-INFO
+-rw-r--r--   0        0        0     1090 2023-05-11 00:54:19.082441 discord_pretty_help-2.0.3/LICENSE
+-rw-r--r--   0        0        0      105 2023-05-12 22:33:28.714632 discord_pretty_help-2.0.3/pretty_help/__init__.py
+-rw-r--r--   0        0        0      500 2023-05-11 00:54:19.096444 discord_pretty_help-2.0.3/pretty_help/abc_menu.py
+-rw-r--r--   0        0        0     4197 2023-05-12 22:24:49.371197 discord_pretty_help-2.0.3/pretty_help/app_menu.py
+-rw-r--r--   0        0        0     5332 2023-05-11 00:54:19.097444 discord_pretty_help-2.0.3/pretty_help/emoji_menu.py
+-rw-r--r--   0        0        0    22753 2023-05-12 22:23:41.300783 discord_pretty_help-2.0.3/pretty_help/pretty_help.py
+-rw-r--r--   0        0        0      748 2023-05-12 22:32:31.632523 discord_pretty_help-2.0.3/pyproject.toml
+-rw-r--r--   0        0        0     3784 2023-05-12 22:34:44.353758 discord_pretty_help-2.0.3/README.md
+-rw-r--r--   0        0        0     4460 1970-01-01 00:00:00.000000 discord_pretty_help-2.0.3/PKG-INFO
```

### Comparing `discord_pretty_help-2.0.2/LICENSE` & `discord_pretty_help-2.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `discord_pretty_help-2.0.2/pretty_help/app_menu.py` & `discord_pretty_help-2.0.3/pretty_help/app_menu.py`

 * *Files 1% similar despite different names*

```diff
@@ -39,15 +39,15 @@
         if ephemeral:
             self.remove_item(self._delete)
 
         if pages and len(pages) > 1:
             for index, page in enumerate(pages):
                 self.select.add_option(
                     label=f"{page.title}",
-                    description=page.description.replace("`", ""),
+                    description=f"{page.description[:96]}...".replace("`", ""),
                     value=index,
                 )
 
     @discord.ui.button(
         label="Previous",
         style=discord.ButtonStyle.success,
         row=1,
```

### Comparing `discord_pretty_help-2.0.2/pretty_help/emoji_menu.py` & `discord_pretty_help-2.0.3/pretty_help/emoji_menu.py`

 * *Files identical despite different names*

### Comparing `discord_pretty_help-2.0.2/pretty_help/pretty_help.py` & `discord_pretty_help-2.0.3/pretty_help/pretty_help.py`

 * *Files identical despite different names*

### Comparing `discord_pretty_help-2.0.2/pyproject.toml` & `discord_pretty_help-2.0.3/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "discord-pretty-help"
-version = "2.0.2"
+version = "2.0.3"
 description = "And nicer looking interactive help menu for discord.py"
 authors = ["CasuallyCalm <29642143+casuallycalm@users.noreply.github.com>"]
 readme = "README.md"
 license = "MIT"
 repository = "https://github.com/casuallycalm/discord-pretty-help"
 keywords=["discord", "discord.py", "discord bot"]
 packages = [
@@ -16,13 +16,13 @@
 
 [tool.poetry.dev-dependencies]
 "discord.py" = "^2"
 black = "^22"
 python-dotenv = "*"
 
 [tool.poetry.scripts]
-run = "tests.test_pretty_help:run"
+test = "tests.test_pretty_help:run"
 emoji = "tests.test_pretty_help:run_emoji"
 
 [build-system]
 requires = ["poetry>=0.12"]
 build-backend = "poetry.masonry.api"
```

### Comparing `discord_pretty_help-2.0.2/README.md` & `discord_pretty_help-2.0.3/README.md`

 * *Files identical despite different names*

### Comparing `discord_pretty_help-2.0.2/PKG-INFO` & `discord_pretty_help-2.0.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: discord-pretty-help
-Version: 2.0.2
+Version: 2.0.3
 Summary: And nicer looking interactive help menu for discord.py
 Home-page: https://github.com/casuallycalm/discord-pretty-help
 License: MIT
 Keywords: discord,discord.py,discord bot
 Author: CasuallyCalm
 Author-email: 29642143+casuallycalm@users.noreply.github.com
 Requires-Python: >=3.8,<4.0
```

