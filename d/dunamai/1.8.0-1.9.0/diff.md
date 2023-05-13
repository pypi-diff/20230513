# Comparing `tmp/dunamai-1.8.0.tar.gz` & `tmp/dunamai-1.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dunamai-1.8.0.tar", max compression
+gzip compressed data, was "dunamai-1.9.0.tar", max compression
```

## Comparing `dunamai-1.8.0.tar` & `dunamai-1.9.0.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0    40764 2022-01-27 16:20:47.690237 dunamai-1.8.0/dunamai/__init__.py
--rw-r--r--   0        0        0     8649 2022-01-27 05:43:42.204544 dunamai-1.8.0/dunamai/__main__.py
--rw-r--r--   0        0        0       27 2021-12-24 01:49:29.833352 dunamai-1.8.0/dunamai/py.typed
--rw-r--r--   0        0        0     1089 2021-12-24 01:49:29.831351 dunamai-1.8.0/LICENSE
--rw-r--r--   0        0        0     1215 2022-01-27 16:33:55.742498 dunamai-1.8.0/pyproject.toml
--rw-r--r--   0        0        0     6563 2021-12-24 01:49:29.832351 dunamai-1.8.0/README.md
--rw-r--r--   0        0        0     7633 2022-01-27 16:37:18.915742 dunamai-1.8.0/setup.py
--rw-r--r--   0        0        0     7637 2022-01-27 16:37:18.916742 dunamai-1.8.0/PKG-INFO
+-rw-r--r--   0        0        0    46252 2022-02-17 22:36:20.699381 dunamai-1.9.0/dunamai/__init__.py
+-rw-r--r--   0        0        0     8649 2022-01-27 05:43:42.204544 dunamai-1.9.0/dunamai/__main__.py
+-rw-r--r--   0        0        0       27 2021-12-24 01:49:29.833352 dunamai-1.9.0/dunamai/py.typed
+-rw-r--r--   0        0        0     1089 2021-12-24 01:49:29.831351 dunamai-1.9.0/LICENSE
+-rw-r--r--   0        0        0     1215 2022-02-20 17:55:15.163217 dunamai-1.9.0/pyproject.toml
+-rw-r--r--   0        0        0     6563 2021-12-24 01:49:29.832351 dunamai-1.9.0/README.md
+-rw-r--r--   0        0        0     7633 2022-02-20 17:55:26.476212 dunamai-1.9.0/setup.py
+-rw-r--r--   0        0        0     7637 2022-02-20 17:55:26.476212 dunamai-1.9.0/PKG-INFO
```

### Comparing `dunamai-1.8.0/dunamai/__init__.py` & `dunamai-1.9.0/dunamai/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -6,14 +6,15 @@
     "serialize_pvp",
     "serialize_semver",
     "Style",
     "Vcs",
     "Version",
 ]
 
+import copy
 import datetime as dt
 import re
 import shlex
 import shutil
 import subprocess
 from collections import OrderedDict
 from enum import Enum
@@ -166,14 +167,20 @@
     )
 
 
 def _blank(value: Optional[_T], default: _T) -> _T:
     return value if value is not None else default
 
 
+def _equal_if_set(x: _T, y: Optional[_T], unset: Sequence[Any] = (None,)) -> bool:
+    if y in unset:
+        return True
+    return x == y
+
+
 def _detect_vcs(expected_vcs: Vcs = None) -> Vcs:
     checks = OrderedDict(
         [
             (Vcs.Git, "git status"),
             (Vcs.Mercurial, "hg status"),
             (Vcs.Darcs, "darcs log"),
             (Vcs.Subversion, "svn log"),
@@ -370,14 +377,33 @@
             and self.distance == other.distance
             and self.commit == other.commit
             and self.dirty == other.dirty
             and self.tagged_metadata == other.tagged_metadata
             and self.epoch == other.epoch
         )
 
+    def _matches_partial(self, other: "Version") -> bool:
+        """
+        Compare this version to another version, but ignore None values in the other version.
+        Distance is also ignored when `other.distance == 0`.
+
+        :param other: The version to compare to.
+        :return: True if this version equals the other version.
+        """
+        return (
+            _equal_if_set(self.base, other.base)
+            and _equal_if_set(self.stage, other.stage)
+            and _equal_if_set(self.revision, other.revision)
+            and _equal_if_set(self.distance, other.distance, unset=[None, 0])
+            and _equal_if_set(self.commit, other.commit)
+            and _equal_if_set(self.dirty, other.dirty)
+            and _equal_if_set(self.tagged_metadata, other.tagged_metadata)
+            and _equal_if_set(self.epoch, other.epoch)
+        )
+
     def __lt__(self, other: Any) -> bool:
         if not isinstance(other, Version):
             raise TypeError(
                 "Cannot compare Version with type {}".format(other.__class__.__qualname__)
             )
 
         import packaging.version as pv
@@ -393,15 +419,15 @@
             and _blank(self.epoch, 0) < _blank(other.epoch, 0)
         )
 
     def serialize(
         self,
         metadata: bool = None,
         dirty: bool = False,
-        format: str = None,
+        format: Union[str, Callable[["Version"], str]] = None,
         style: Style = None,
         bump: bool = False,
         tagged_metadata: bool = False,
     ) -> str:
         """
         Create a string from the version info.
 
@@ -409,16 +435,17 @@
             in the metadata/local version part only if the distance is nonzero.
             Set this to True to always include metadata even with no distance,
             or set it to False to always exclude it.
             This is ignored when `format` is used.
         :param dirty: Set this to True to include a dirty flag in the
             metadata if applicable. Inert when metadata=False.
             This is ignored when `format` is used.
-        :param format: Custom output format. You can use substitutions, such as
-            "v{base}" to get "v0.1.0". Available substitutions:
+        :param format: Custom output format. It is either a formatted string or a
+            callback. In the string you can use substitutions, such as "v{base}"
+            to get "v0.1.0". Available substitutions:
 
             * {base}
             * {stage}
             * {revision}
             * {distance}
             * {commit}
             * {dirty} which expands to either "dirty" or "clean"
@@ -434,33 +461,35 @@
         :param tagged_metadata: If true, insert the `tagged_metadata` in the
             version as the first part of the metadata segment.
             This is ignored when `format` is used.
         """
         base = self.base
         revision = self.revision
         if bump:
-            if self.stage is None:
-                base = bump_version(self.base)
-            else:
-                if self.revision is None:
-                    revision = 2
-                else:
-                    revision = self.revision + 1
+            bumped = self.bump()
+            base = bumped.base
+            revision = bumped.revision
 
         if format is not None:
-            out = format.format(
-                base=base,
-                stage=_blank(self.stage, ""),
-                revision=_blank(revision, ""),
-                distance=_blank(self.distance, ""),
-                commit=_blank(self.commit, ""),
-                tagged_metadata=_blank(self.tagged_metadata, ""),
-                dirty="dirty" if self.dirty else "clean",
-                epoch=_blank(self.epoch, ""),
-            )
+            if callable(format):
+                new_version = copy.deepcopy(self)
+                new_version.base = base
+                new_version.revision = revision
+                out = format(new_version)
+            else:
+                out = format.format(
+                    base=base,
+                    stage=_blank(self.stage, ""),
+                    revision=_blank(revision, ""),
+                    distance=_blank(self.distance, ""),
+                    commit=_blank(self.commit, ""),
+                    tagged_metadata=_blank(self.tagged_metadata, ""),
+                    dirty="dirty" if self.dirty else "clean",
+                    epoch=_blank(self.epoch, ""),
+                )
             if style is not None:
                 check_version(out, style)
             return out
 
         if style is None:
             style = Style.Pep440
         out = ""
@@ -522,14 +551,111 @@
         elif style == Style.Pvp:
             out = serialize_pvp(base, metadata=[*pre_parts, *meta_parts])
 
         check_version(out, style)
         return out
 
     @classmethod
+    def parse(cls, version: str, pattern: str = _VERSION_PATTERN) -> "Version":
+        """
+        Attempt to parse a string into a Version instance.
+
+        This uses inexact heuristics, so its output may vary slightly between
+        releases. Consider this a "best effort" conversion.
+
+        :param version: Full version, such as 0.3.0a3+d7.gb6a9020.dirty.
+        :param pattern: Regular expression matched against the version.
+            Refer to `from_any_vcs` for more info.
+        """
+        try:
+            prefixed = version if version.startswith("v") else "v{}".format(version)
+            matched_pattern = _match_version_pattern(pattern, [prefixed], True)
+        except ValueError:
+            return cls(version)
+
+        base = matched_pattern.base
+        stage = matched_pattern.stage_revision
+        distance = None
+        commit = None
+        dirty = None
+        tagged_metadata = matched_pattern.tagged_metadata
+        epoch = matched_pattern.epoch
+
+        if tagged_metadata:
+            pop = []  # type: list
+            parts = tagged_metadata.split(".")
+
+            for i, value in enumerate(parts):
+                if dirty is None:
+                    if value == "dirty":
+                        dirty = True
+                        pop.append(i)
+                        continue
+                    elif value == "clean":
+                        dirty = False
+                        pop.append(i)
+                        continue
+                if distance is None:
+                    match = re.match(r"d?(\d+)", value)
+                    if match:
+                        distance = int(match.group(1))
+                        pop.append(i)
+                        continue
+                if commit is None:
+                    match = re.match(r"g?([\da-z]+)", value)
+                    if match:
+                        commit = match.group(1)
+                        pop.append(i)
+                        continue
+
+            for i in reversed(sorted(pop)):
+                parts.pop(i)
+
+            tagged_metadata = ".".join(parts)
+
+        if distance is None:
+            distance = 0
+        if tagged_metadata is not None and tagged_metadata.strip() == "":
+            tagged_metadata = None
+
+        return cls(
+            base,
+            stage=stage,
+            distance=distance,
+            commit=commit,
+            dirty=dirty,
+            tagged_metadata=tagged_metadata,
+            epoch=epoch,
+        )
+
+    def bump(self, index: int = -1) -> "Version":
+        """
+        Increment the version.
+
+        The base is bumped unless there is a stage defined, in which case,
+        the revision is bumped instead.
+
+        :param index: Numerical position to increment in the base. Default: -1.
+            This follows Python indexing rules, so positive numbers start from
+            the left side and count up from 0, while negative numbers start from
+            the right side and count down from -1.
+            Only has an effect when the base is bumped.
+        :return: Bumped version.
+        """
+        bumped = copy.deepcopy(self)
+        if bumped.stage is None:
+            bumped.base = bump_version(bumped.base, index)
+        else:
+            if bumped.revision is None:
+                bumped.revision = 2
+            else:
+                bumped.revision = bumped.revision + 1
+        return bumped
+
+    @classmethod
     def from_git(cls, pattern: str = _VERSION_PATTERN, latest_tag: bool = False) -> "Version":
         r"""
         Determine a version based on Git tags.
 
         :param pattern: Regular expression matched against the version source.
             Refer to `from_any_vcs` for more info.
         :param latest_tag: If true, only inspect the latest tag on the latest
@@ -989,44 +1115,58 @@
 
 
 def get_version(
     name: str,
     first_choice: Callable[[], Optional[Version]] = None,
     third_choice: Callable[[], Optional[Version]] = None,
     fallback: Version = Version("0.0.0"),
+    ignore: Sequence[Version] = None,
+    parser: Callable[[str], Version] = Version,
 ) -> Version:
     """
     Check pkg_resources info or a fallback function to determine the version.
     This is intended as a convenient default for setting your `__version__` if
     you do not want to include a generated version statically during packaging.
 
     :param name: Installed package name.
     :param first_choice: Callback to determine a version before checking
         to see if the named package is installed.
     :param third_choice: Callback to determine a version if the installed
         package cannot be found by name.
     :param fallback: If no other matches found, use this version.
+    :param ignore: Ignore a found version if it is part of this list. When
+        comparing the found version to an ignored one, fields with None in the ignored
+        version are not taken into account. If the ignored version has distance=0,
+        then that field is also ignored.
+    :param parser: Callback to convert a string into a Version instance.
+        This will be used for the second choice.
+        For example, you can pass `Version.parse` here.
     """
+    if ignore is None:
+        ignore = []
+
     if first_choice:
         first_ver = first_choice()
-        if first_ver:
+        if first_ver and not any(first_ver._matches_partial(v) for v in ignore):
             return first_ver
 
     try:
         import importlib.metadata as ilm
     except ImportError:
         import importlib_metadata as ilm  # type: ignore
     try:
-        return Version(ilm.version(name))
+        ilm_version = parser(ilm.version(name))
+        if not any(ilm_version._matches_partial(v) for v in ignore):
+            return ilm_version
     except ilm.PackageNotFoundError:
         pass
 
     if third_choice:
         third_ver = third_choice()
-        if third_ver:
+        if third_ver and not any(third_ver._matches_partial(v) for v in ignore):
             return third_ver
 
     return fallback
 
 
 def serialize_pep440(
     base: str,
```

### Comparing `dunamai-1.8.0/dunamai/__main__.py` & `dunamai-1.9.0/dunamai/__main__.py`

 * *Files identical despite different names*

### Comparing `dunamai-1.8.0/LICENSE` & `dunamai-1.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `dunamai-1.8.0/pyproject.toml` & `dunamai-1.9.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dunamai"
-version = "1.8.0"
+version = "1.9.0"
 description = "Dynamic version generation"
 license = "MIT"
 authors = ["Matthew T. Kennerly <mtkennerly@gmail.com>"]
 readme = "README.md"
 repository = "https://github.com/mtkennerly/dunamai"
 keywords = ["version", "versioning", "dynamic"]
 classifiers = [
```

### Comparing `dunamai-1.8.0/README.md` & `dunamai-1.9.0/README.md`

 * *Files identical despite different names*

### Comparing `dunamai-1.8.0/setup.py` & `dunamai-1.9.0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 {':python_version < "3.8"': ['importlib-metadata>=1.6.0']}
 
 entry_points = \
 {'console_scripts': ['dunamai = dunamai.__main__:main']}
 
 setup_kwargs = {
     'name': 'dunamai',
-    'version': '1.8.0',
+    'version': '1.9.0',
     'description': 'Dynamic version generation',
     'long_description': '\n# Dunamai\n[![Version](https://img.shields.io/pypi/v/dunamai)](https://pypi.org/project/dunamai)\n[![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](https://opensource.org/licenses/MIT)\n\nDunamai is a Python 3.5+ library and command line tool for producing dynamic,\nstandards-compliant version strings, derived from tags in your version\ncontrol system. This facilitates uniquely identifying nightly or per-commit\nbuilds in continuous integration and releasing new versions of your software\nsimply by creating a tag.\n\nDunamai is also available as a [GitHub Action](https://github.com/marketplace/actions/run-dunamai).\n\n## Features\n* Version control system support:\n  * [Git](https://git-scm.com) (minimum version: 2.7.0)\n  * [Mercurial](https://www.mercurial-scm.org)\n  * [Darcs](http://darcs.net)\n  * [Subversion](https://subversion.apache.org)\n  * [Bazaar](https://bazaar.canonical.com/en)\n  * [Fossil](https://www.fossil-scm.org/home/doc/trunk/www/index.wiki)\n* Version styles:\n  * [PEP 440](https://www.python.org/dev/peps/pep-0440)\n  * [Semantic Versioning](https://semver.org)\n  * [Haskell Package Versioning Policy](https://pvp.haskell.org)\n  * Custom output formats\n* Can be used for projects written in any programming language.\n  For Python, this means you do not need a setup.py.\n\n## Usage\nInstall with `pip install dunamai`, and then use as either a CLI:\n\n```console\n# Suppose you are on commit g29045e8, 7 commits after the v0.2.0 tag.\n# Note that the "v" prefix on the tag is required, unless you specify\n# a different tag style using "--pattern".\n\n# Auto-detect the version control system and generate a version:\n$ dunamai from any\n0.2.0.post7.dev0+g29045e8\n\n# Or use an explicit VCS and style:\n$ dunamai from git --no-metadata --style semver\n0.2.0-post.7\n\n# Custom formats:\n$ dunamai from any --format "v{base}+{distance}.{commit}"\nv0.2.0+7.g29045e8\n\n# If you\'d prefer to frame the version in terms of progress toward the next\n# release rather than distance from the latest one, you can bump it:\n$ dunamai from any --bump\n0.2.1.dev7+g29045e8\n\n# Validation of custom formats:\n$ dunamai from any --format "v{base}" --style pep440\nVersion \'v0.2.0\' does not conform to the PEP 440 style\n\n# Validate your own freeform versions:\n$ dunamai check 0.01.0 --style semver\nVersion \'0.01.0\' does not conform to the Semantic Versioning style\n\n# More info:\n$ dunamai --help\n$ dunamai from --help\n$ dunamai from git --help\n```\n\nOr as a library:\n\n```python\nfrom dunamai import Version, Style\n\n# Let\'s say you\'re on commit g644252b, which is tagged as v0.1.0.\nversion = Version.from_git()\nassert version.serialize() == "0.1.0"\n\n# Let\'s say there was a v0.1.0rc5 tag 44 commits ago\n# and you have some uncommitted changes.\nversion = Version.from_any_vcs()\nassert version.serialize() == "0.1.0rc5.post44.dev0+g644252b"\nassert version.serialize(metadata=False) == "0.1.0rc5.post44.dev0"\nassert version.serialize(dirty=True) == "0.1.0rc5.post44.dev0+g644252b.dirty"\nassert version.serialize(style=Style.SemVer) == "0.1.0-rc.5.post.44+g644252b"\n```\n\nThe `serialize()` method gives you an opinionated, PEP 440-compliant default\nthat ensures that versions for untagged commits are compatible with Pip\'s\n`--pre` flag. The individual parts of the version are also available for you\nto use and inspect as you please:\n\n```python\nassert version.base == "0.1.0"\nassert version.stage == "rc"\nassert version.revision == 5\nassert version.distance == 44\nassert version.commit == "g644252b"\nassert version.dirty is True\n\n# Available if the latest tag includes metadata, like v0.1.0+linux:\nassert version.tagged_metadata == "linux"\n```\n\n## Comparison to Versioneer\n[Versioneer](https://github.com/warner/python-versioneer) is another great\nlibrary for dynamic versions, but there are some design decisions that\nprompted the creation of Dunamai as an alternative:\n\n* Versioneer requires a setup.py file to exist, or else `versioneer install`\n  will fail, rendering it incompatible with non-setuptools-based projects\n  such as those using Poetry or Flit. Dunamai can be used regardless of the\n  project\'s build system.\n* Versioneer has a CLI that generates Python code which needs to be committed\n  into your repository, whereas Dunamai is just a normal importable library\n  with an optional CLI to help statically include your version string.\n* Versioneer produces the version as an opaque string, whereas Dunamai provides\n  a Version class with discrete parts that can then be inspected and serialized\n  separately.\n* Versioneer provides customizability through a config file, whereas Dunamai\n  aims to offer customizability through its library API and CLI for both\n  scripting support and use in other libraries.\n\n## Integration\n* Setting a `__version__` statically:\n\n  ```console\n  $ echo "__version__ = \'$(dunamai from any)\'" > your_library/_version.py\n  ```\n  ```python\n  # your_library/__init__.py\n  from your_library._version import __version__\n  ```\n\n  Or dynamically (but Dunamai becomes a runtime dependency):\n\n  ```python\n  # your_library/__init__.py\n  import dunamai as _dunamai\n  __version__ = _dunamai.get_version("your-library", third_choice=_dunamai.Version.from_any_vcs).serialize()\n  ```\n\n* setup.py (no install-time dependency on Dunamai as long as you use wheels):\n\n  ```python\n  from setuptools import setup\n  from dunamai import Version\n\n  setup(\n      name="your-library",\n      version=Version.from_any_vcs().serialize(),\n  )\n  ```\n\n  Or you could use a static inclusion approach as in the prior example.\n\n* [Poetry](https://poetry.eustace.io):\n\n  ```console\n  $ poetry version $(dunamai from any)\n  ```\n\n  Or you can use the [poetry-dynamic-versioning](https://github.com/mtkennerly/poetry-dynamic-versioning) plugin.\n\n## Other notes\n* When using Git, the initial commit must **not** be both tagged and empty\n  (i.e., created with `--allow-empty`). This is related to a reporting issue\n  in Git. For more info, [click here](https://github.com/mtkennerly/dunamai/issues/14).\n\n## Development\nThis project is managed using [Poetry](https://poetry.eustace.io).\nDevelopment requires Python 3.6+ because of [Black](https://github.com/ambv/black).\n\n* If you want to take advantage of the default VSCode integration, then first\n  configure Poetry to make its virtual environment in the repository:\n  ```\n  poetry config settings.virtualenvs.in-project true\n  ```\n* After cloning the repository, activate the tooling:\n  ```\n  poetry install\n  poetry run pre-commit install\n  ```\n* Run unit tests:\n  ```\n  poetry run pytest --cov\n  poetry run tox\n  ```\n',
     'author': 'Matthew T. Kennerly',
     'author_email': 'mtkennerly@gmail.com',
     'maintainer': None,
     'maintainer_email': None,
     'url': 'https://github.com/mtkennerly/dunamai',
```

### Comparing `dunamai-1.8.0/PKG-INFO` & `dunamai-1.9.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dunamai
-Version: 1.8.0
+Version: 1.9.0
 Summary: Dynamic version generation
 Home-page: https://github.com/mtkennerly/dunamai
 License: MIT
 Keywords: version,versioning,dynamic
 Author: Matthew T. Kennerly
 Author-email: mtkennerly@gmail.com
 Requires-Python: >=3.5,<4.0
```

