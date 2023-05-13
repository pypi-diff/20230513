# Comparing `tmp/bibx-0.0.1a4.tar.gz` & `tmp/bibx-0.0.1a5.tar.gz`

## Comparing `bibx-0.0.1a4.tar` & `bibx-0.0.1a5.tar`

### file list

```diff
@@ -1,34 +1,35 @@
--rw-r--r--   0        0        0      576 2020-02-02 00:00:00.000000 bibx-0.0.1a4/.pre-commit-config.yaml
--rw-r--r--   0        0        0      163 2020-02-02 00:00:00.000000 bibx-0.0.1a4/Makefile
--rw-r--r--   0        0        0      744 2020-02-02 00:00:00.000000 bibx-0.0.1a4/.github/workflows/cd.yml
--rw-r--r--   0        0        0      814 2020-02-02 00:00:00.000000 bibx-0.0.1a4/.github/workflows/ci.yml
--rw-r--r--   0        0        0  2221838 2020-02-02 00:00:00.000000 bibx-0.0.1a4/docs/examples/bit-pattern-savedrecs.txt
--rw-r--r--   0        0        0  5022778 2020-02-02 00:00:00.000000 bibx-0.0.1a4/docs/examples/scopus.bib
--rw-r--r--   0        0        0  2955913 2020-02-02 00:00:00.000000 bibx-0.0.1a4/docs/examples/scopus.ris
--rw-r--r--   0        0        0     4911 2020-02-02 00:00:00.000000 bibx-0.0.1a4/docs/examples/single-article.txt
--rw-r--r--   0        0        0     1694 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/__init__.py
--rw-r--r--   0        0        0     1079 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/__main__.py
--rw-r--r--   0        0        0     1047 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/exceptions.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/__init__.py
--rw-r--r--   0        0        0     1263 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/article.py
--rw-r--r--   0        0        0     1732 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/__init__.py
--rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/base.py
--rw-r--r--   0        0        0      436 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/cross_ref.py
--rw-r--r--   0        0        0      328 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/generic.py
--rw-r--r--   0        0        0     2571 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/scopus_bib.py
--rw-r--r--   0        0        0     6202 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/scopus_ris.py
--rw-r--r--   0        0        0      401 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/simple.py
--rw-r--r--   0        0        0    13156 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/_entities/collection_builders/wos.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/algorithms/__init__.py
--rw-r--r--   0        0        0    11115 2020-02-02 00:00:00.000000 bibx-0.0.1a4/src/bibx/algorithms/sap.py
--rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 bibx-0.0.1a4/tests/test_works.py
--rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 bibx-0.0.1a4/tests/algorithms/test_sap.py
--rw-r--r--   0        0        0     6876 2020-02-02 00:00:00.000000 bibx-0.0.1a4/tests/entities/collection_builders/test_scopus_bib.py
--rw-r--r--   0        0        0     1882 2020-02-02 00:00:00.000000 bibx-0.0.1a4/tests/entities/collection_builders/test_scopus_ris.py
--rw-r--r--   0        0        0     6580 2020-02-02 00:00:00.000000 bibx-0.0.1a4/tests/entities/collection_builders/test_wos.py
--rw-r--r--   0        0        0     3077 2020-02-02 00:00:00.000000 bibx-0.0.1a4/.gitignore
--rw-r--r--   0        0        0     1073 2020-02-02 00:00:00.000000 bibx-0.0.1a4/LICENSE
--rw-r--r--   0        0        0     1869 2020-02-02 00:00:00.000000 bibx-0.0.1a4/README.md
--rw-r--r--   0        0        0     1067 2020-02-02 00:00:00.000000 bibx-0.0.1a4/pyproject.toml
--rw-r--r--   0        0        0     2467 2020-02-02 00:00:00.000000 bibx-0.0.1a4/PKG-INFO
+-rw-r--r--   0        0        0      576 2020-02-02 00:00:00.000000 bibx-0.0.1a5/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      163 2020-02-02 00:00:00.000000 bibx-0.0.1a5/Makefile
+-rw-r--r--   0        0        0      744 2020-02-02 00:00:00.000000 bibx-0.0.1a5/.github/workflows/cd.yml
+-rw-r--r--   0        0        0      814 2020-02-02 00:00:00.000000 bibx-0.0.1a5/.github/workflows/ci.yml
+-rw-r--r--   0        0        0  2221838 2020-02-02 00:00:00.000000 bibx-0.0.1a5/docs/examples/bit-pattern-savedrecs.txt
+-rw-r--r--   0        0        0  5022778 2020-02-02 00:00:00.000000 bibx-0.0.1a5/docs/examples/scopus.bib
+-rw-r--r--   0        0        0  2955913 2020-02-02 00:00:00.000000 bibx-0.0.1a5/docs/examples/scopus.ris
+-rw-r--r--   0        0        0     4911 2020-02-02 00:00:00.000000 bibx-0.0.1a5/docs/examples/single-article.txt
+-rw-r--r--   0        0        0     1694 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/__init__.py
+-rw-r--r--   0        0        0       63 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/__main__.py
+-rw-r--r--   0        0        0     1670 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/cli.py
+-rw-r--r--   0        0        0     1047 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/exceptions.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/__init__.py
+-rw-r--r--   0        0        0     1468 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/article.py
+-rw-r--r--   0        0        0     1732 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/__init__.py
+-rw-r--r--   0        0        0      162 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/base.py
+-rw-r--r--   0        0        0      436 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/cross_ref.py
+-rw-r--r--   0        0        0      328 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/generic.py
+-rw-r--r--   0        0        0     2571 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/scopus_bib.py
+-rw-r--r--   0        0        0     6133 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/scopus_ris.py
+-rw-r--r--   0        0        0      401 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/simple.py
+-rw-r--r--   0        0        0    13050 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/_entities/collection_builders/wos.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/algorithms/__init__.py
+-rw-r--r--   0        0        0    11180 2020-02-02 00:00:00.000000 bibx-0.0.1a5/src/bibx/algorithms/sap.py
+-rw-r--r--   0        0        0       34 2020-02-02 00:00:00.000000 bibx-0.0.1a5/tests/test_works.py
+-rw-r--r--   0        0        0     1065 2020-02-02 00:00:00.000000 bibx-0.0.1a5/tests/algorithms/test_sap.py
+-rw-r--r--   0        0        0     6876 2020-02-02 00:00:00.000000 bibx-0.0.1a5/tests/entities/collection_builders/test_scopus_bib.py
+-rw-r--r--   0        0        0     1882 2020-02-02 00:00:00.000000 bibx-0.0.1a5/tests/entities/collection_builders/test_scopus_ris.py
+-rw-r--r--   0        0        0     6580 2020-02-02 00:00:00.000000 bibx-0.0.1a5/tests/entities/collection_builders/test_wos.py
+-rw-r--r--   0        0        0     3077 2020-02-02 00:00:00.000000 bibx-0.0.1a5/.gitignore
+-rw-r--r--   0        0        0     1073 2020-02-02 00:00:00.000000 bibx-0.0.1a5/LICENSE
+-rw-r--r--   0        0        0     1869 2020-02-02 00:00:00.000000 bibx-0.0.1a5/README.md
+-rw-r--r--   0        0        0     1092 2020-02-02 00:00:00.000000 bibx-0.0.1a5/pyproject.toml
+-rw-r--r--   0        0        0     2500 2020-02-02 00:00:00.000000 bibx-0.0.1a5/PKG-INFO
```

### Comparing `bibx-0.0.1a4/.pre-commit-config.yaml` & `bibx-0.0.1a5/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/.github/workflows/cd.yml` & `bibx-0.0.1a5/.github/workflows/cd.yml`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/.github/workflows/ci.yml` & `bibx-0.0.1a5/.github/workflows/ci.yml`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/docs/examples/bit-pattern-savedrecs.txt` & `bibx-0.0.1a5/docs/examples/bit-pattern-savedrecs.txt`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/docs/examples/scopus.bib` & `bibx-0.0.1a5/docs/examples/scopus.bib`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/docs/examples/scopus.ris` & `bibx-0.0.1a5/docs/examples/scopus.ris`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/docs/examples/single-article.txt` & `bibx-0.0.1a5/docs/examples/single-article.txt`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/src/bibx/__init__.py` & `bibx-0.0.1a5/src/bibx/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
     "Sap",
     "read_scopus_bib",
     "read_scopus_ris",
     "read_wos",
     "read_any",
 ]
 
-__version__ = "0.0.1a4"
+__version__ = "0.0.1a5"
 
 
 def read_scopus_bib(*files: TextIO) -> Collection:
     """
     Takes any number of bibtex files from scopus and generates a collection.
 
     :param files: Scopus bib files open.
```

### Comparing `bibx-0.0.1a4/src/bibx/exceptions.py` & `bibx-0.0.1a5/src/bibx/exceptions.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/src/bibx/_entities/article.py` & `bibx-0.0.1a5/src/bibx/_entities/article.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,39 +1,42 @@
 from dataclasses import dataclass, field
 from typing import List, Mapping, Optional, Set
 
 
 @dataclass
 class Article:
-    authors: List[str]
-    year: int
+    authors: List[str] = field(default_factory=list)
+    year: Optional[int] = None
     title: Optional[str] = None
     journal: Optional[str] = None
     volume: Optional[str] = None
     issue: Optional[str] = None
     page: Optional[str] = None
     doi: Optional[str] = None
     _label: Optional[str] = None
     references: List["Article"] = field(default_factory=list)
     keywords: List[str] = field(default_factory=list)
     sources: Set[str] = field(default_factory=set)
     extra: Mapping = field(default_factory=dict)
 
     @property
     def key(self):
-        author = self.authors[0].split(" ")[0].replace(",", "")
+        if self.authors:
+            author = self.authors[0].split(" ")[0].replace(",", "")
+        else:
+            author = "anonymous"
         year = self.year
         return f"{author}{year}".lower()
 
     @property
     def label(self):
         if self._label is not None:
             return self._label
         pieces = {
-            "AU": self.authors[0].replace(",", ""),
-            "PY": str(self.year),
-            "J9": str(self.journal),
+            "AU": self.authors[0].replace(",", "") if self.authors else "anonymous",
+            "PY": str(self.year) if self.year else None,
+            "J9": str(self.journal) if self.journal else None,
             "VL": f"V{self.volume}" if self.volume else None,
             "BP": f"P{self.page}" if self.page else None,
             "DI": f"DOI {self.doi}" if self.doi else None,
         }
         return ", ".join(value for value in pieces.values() if value)
```

### Comparing `bibx-0.0.1a4/src/bibx/_entities/collection.py` & `bibx-0.0.1a5/src/bibx/_entities/collection.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/src/bibx/_entities/collection_builders/scopus_bib.py` & `bibx-0.0.1a5/src/bibx/_entities/collection_builders/scopus_bib.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/src/bibx/_entities/collection_builders/scopus_ris.py` & `bibx-0.0.1a5/src/bibx/_entities/collection_builders/scopus_ris.py`

 * *Files 2% similar despite different names*

```diff
@@ -147,20 +147,18 @@
                 else:
                     current = data["key"]
             if value and current:
                 parsed[current].append(data.get("value", ""))
         return dict(parsed)
 
     @classmethod
-    def _parse_record(cls, record: str) -> Article:
+    def _article_from_record(cls, record: str) -> Article:
         data = cls._ris_to_dict(record)
         year = _int_or_nothing(data.get("PY", []))
         authors = data.get("AU", [])
-        if not authors or not year:
-            raise MissingCriticalInformation()
         return Article(
             title=_joined(data.get("TI")),
             authors=authors,
             year=year,
             journal=_joined(data.get("J2")),
             volume=_joined(data.get("VL")),
             issue=_joined(data.get("IS")),
@@ -176,11 +174,11 @@
     def _parse_file(cls, file: TextIO) -> Iterable[Article]:
         if not _size(file):
             return []
         for item in file.read().split("\n\n"):
             if item.isspace():
                 continue
             try:
-                article = cls._parse_record(item.strip())
+                article = cls._article_from_record(item.strip())
                 yield article
             except MissingCriticalInformation:
                 logger.info("Missing critical information for record %s", item)
```

### Comparing `bibx-0.0.1a4/src/bibx/_entities/collection_builders/wos.py` & `bibx-0.0.1a5/src/bibx/_entities/collection_builders/wos.py`

 * *Files 0% similar despite different names*

```diff
@@ -292,20 +292,17 @@
             field = parsed.get("field") or field
             if not field or "value" not in parsed or parsed["value"] is None:
                 continue
             article_data[field].append(parsed["value"])
 
         processed = cls._parse_all(dict(article_data))
 
-        if not processed.get("year") or not processed.get("authors"):
-            raise MissingCriticalInformation()
-
         return Article(
-            authors=processed["authors"],
-            year=processed["year"],
+            authors=processed.get("authors", []),
+            year=processed.get("year"),
             title=processed.get("title"),
             journal=processed.get("source_abbreviation"),
             volume=processed.get("volume"),
             issue=processed.get("issue"),
             page=processed.get("beginning_page"),
             doi=processed.get("DOI"),
             references=list(
```

### Comparing `bibx-0.0.1a4/src/bibx/algorithms/sap.py` & `bibx-0.0.1a5/src/bibx/algorithms/sap.py`

 * *Files 2% similar despite different names*

```diff
@@ -181,15 +181,17 @@
         if self.min_leaf_connections is not None:
             potential_leaves = [
                 (n, c) for n, c in potential_leaves if c >= self.min_leaf_connections
             ]
 
         if self.max_leaf_age is not None:
             potential_leaves = [
-                (n, c) for n, c in potential_leaves if YEAR in g.nodes[n]
+                (n, c)
+                for n, c in potential_leaves
+                if YEAR in g.nodes[n] and g.nodes[n][YEAR] is not None
             ]
             newest_year = max(
                 g.nodes[n][YEAR] for n, _ in potential_leaves if g.nodes[n][YEAR]
             )
             earliest_publication_year = newest_year - self.max_leaf_age
             potential_leaves = [
                 (n, c)
```

### Comparing `bibx-0.0.1a4/tests/algorithms/test_sap.py` & `bibx-0.0.1a5/tests/algorithms/test_sap.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/tests/entities/collection_builders/test_scopus_bib.py` & `bibx-0.0.1a5/tests/entities/collection_builders/test_scopus_bib.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/tests/entities/collection_builders/test_scopus_ris.py` & `bibx-0.0.1a5/tests/entities/collection_builders/test_scopus_ris.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/tests/entities/collection_builders/test_wos.py` & `bibx-0.0.1a5/tests/entities/collection_builders/test_wos.py`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/.gitignore` & `bibx-0.0.1a5/.gitignore`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/LICENSE` & `bibx-0.0.1a5/LICENSE`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/README.md` & `bibx-0.0.1a5/README.md`

 * *Files identical despite different names*

### Comparing `bibx-0.0.1a4/pyproject.toml` & `bibx-0.0.1a5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -12,14 +12,15 @@
     "text mining",
 ]
 dynamic = ["version"]
 
 dependencies = [
     "bibtexparser~=1.4.0",
     "networkx~=3.0",
+    "typer[all]~=0.9.0",
 ]
 
 [project.optional-dependencies]
 dev = [
     "black~=22.10.0",
     "pytest~=7.2.0",
     "isort~=5.12.0",
```

### Comparing `bibx-0.0.1a4/PKG-INFO` & `bibx-0.0.1a5/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 Metadata-Version: 2.1
 Name: bibx
-Version: 0.0.1a4
+Version: 0.0.1a5
 Summary: Python bibliometric tools.
 Author-email: Core of Science Team <technology@coreofscience.org>
 License-Expression: MIT
 License-File: LICENSE
 Keywords: bibliometrics,science,text mining
 Requires-Dist: bibtexparser~=1.4.0
 Requires-Dist: networkx~=3.0
+Requires-Dist: typer[all]~=0.9.0
 Provides-Extra: dev
 Requires-Dist: black~=22.10.0; extra == 'dev'
 Requires-Dist: isort~=5.12.0; extra == 'dev'
 Requires-Dist: pre-commit~=2.20.0; extra == 'dev'
 Requires-Dist: pytest~=7.2.0; extra == 'dev'
 Requires-Dist: ruff~=0.0.254; extra == 'dev'
 Description-Content-Type: text/markdown
```

