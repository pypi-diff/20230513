# Comparing `tmp/dnadb-0.2.9.tar.gz` & `tmp/dnadb-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dnadb-0.2.9.tar", last modified: Wed May  3 02:37:08 2023, max compression
+gzip compressed data, was "dnadb-0.3.0.tar", last modified: Sat May 13 03:03:23 2023, max compression
```

## Comparing `dnadb-0.2.9.tar` & `dnadb-0.3.0.tar`

### file list

```diff
@@ -1,28 +1,29 @@
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.972353 dnadb-0.2.9/
--rw-r--r--   0 dwl2x     (1000) users      (100)     1070 2023-03-27 04:24:58.000000 dnadb-0.2.9/LICENSE
--rw-r--r--   0 dwl2x     (1000) users      (100)     1802 2023-05-03 02:37:08.972353 dnadb-0.2.9/PKG-INFO
--rw-r--r--   0 dwl2x     (1000) users      (100)       43 2023-03-27 04:27:38.000000 dnadb-0.2.9/README.md
--rw-r--r--   0 dwl2x     (1000) users      (100)      712 2023-05-03 02:13:13.000000 dnadb-0.2.9/pyproject.toml
--rw-r--r--   0 dwl2x     (1000) users      (100)       38 2023-05-03 02:37:08.972353 dnadb-0.2.9/setup.cfg
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.968353 dnadb-0.2.9/src/
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.972353 dnadb-0.2.9/src/dnadb/
--rw-r--r--   0 dwl2x     (1000) users      (100)       22 2023-05-03 02:36:07.000000 dnadb-0.2.9/src/dnadb/__init__.py
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.972353 dnadb-0.2.9/src/dnadb/datasets/
--rw-r--r--   0 dwl2x     (1000) users      (100)      255 2023-03-27 05:49:34.000000 dnadb-0.2.9/src/dnadb/datasets/__init__.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     7303 2023-03-29 23:23:08.000000 dnadb-0.2.9/src/dnadb/datasets/dataset.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     1392 2023-04-03 19:22:40.000000 dnadb-0.2.9/src/dnadb/datasets/greengenes.py
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.972353 dnadb-0.2.9/src/dnadb/datasets/silva/
--rw-r--r--   0 dwl2x     (1000) users      (100)     5492 2023-04-14 13:32:31.000000 dnadb-0.2.9/src/dnadb/datasets/silva/__init__.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     6022 2023-03-27 05:43:12.000000 dnadb-0.2.9/src/dnadb/datasets/silva/taxonomy_map.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     1163 2023-04-30 03:41:17.000000 dnadb-0.2.9/src/dnadb/db.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     6027 2023-04-02 01:42:55.000000 dnadb-0.2.9/src/dnadb/dna.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     5443 2023-05-03 02:31:55.000000 dnadb-0.2.9/src/dnadb/fasta.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     7157 2023-05-03 02:31:41.000000 dnadb-0.2.9/src/dnadb/fastq.py
--rw-r--r--   0 dwl2x     (1000) users      (100)    15566 2023-05-03 02:35:14.000000 dnadb-0.2.9/src/dnadb/taxonomy.py
--rw-r--r--   0 dwl2x     (1000) users      (100)     1473 2023-04-01 17:43:32.000000 dnadb-0.2.9/src/dnadb/utils.py
-drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-03 02:37:08.972353 dnadb-0.2.9/src/dnadb.egg-info/
--rw-r--r--   0 dwl2x     (1000) users      (100)     1802 2023-05-03 02:37:08.000000 dnadb-0.2.9/src/dnadb.egg-info/PKG-INFO
--rw-r--r--   0 dwl2x     (1000) users      (100)      502 2023-05-03 02:37:08.000000 dnadb-0.2.9/src/dnadb.egg-info/SOURCES.txt
--rw-r--r--   0 dwl2x     (1000) users      (100)        1 2023-05-03 02:37:08.000000 dnadb-0.2.9/src/dnadb.egg-info/dependency_links.txt
--rw-r--r--   0 dwl2x     (1000) users      (100)       40 2023-05-03 02:37:08.000000 dnadb-0.2.9/src/dnadb.egg-info/requires.txt
--rw-r--r--   0 dwl2x     (1000) users      (100)        6 2023-05-03 02:37:08.000000 dnadb-0.2.9/src/dnadb.egg-info/top_level.txt
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.858793 dnadb-0.3.0/
+-rw-r--r--   0 dwl2x     (1000) users      (100)     1070 2023-03-27 04:24:58.000000 dnadb-0.3.0/LICENSE
+-rw-r--r--   0 dwl2x     (1000) users      (100)     1802 2023-05-13 03:03:23.854793 dnadb-0.3.0/PKG-INFO
+-rw-r--r--   0 dwl2x     (1000) users      (100)       43 2023-03-27 04:27:38.000000 dnadb-0.3.0/README.md
+-rw-r--r--   0 dwl2x     (1000) users      (100)      742 2023-05-12 20:49:48.000000 dnadb-0.3.0/pyproject.toml
+-rw-r--r--   0 dwl2x     (1000) users      (100)       38 2023-05-13 03:03:23.858793 dnadb-0.3.0/setup.cfg
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.854793 dnadb-0.3.0/src/
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.854793 dnadb-0.3.0/src/dnadb/
+-rw-r--r--   0 dwl2x     (1000) users      (100)       22 2023-05-12 20:50:07.000000 dnadb-0.3.0/src/dnadb/__init__.py
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.854793 dnadb-0.3.0/src/dnadb/datasets/
+-rw-r--r--   0 dwl2x     (1000) users      (100)      255 2023-03-27 05:49:34.000000 dnadb-0.3.0/src/dnadb/datasets/__init__.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     7303 2023-03-29 23:23:08.000000 dnadb-0.3.0/src/dnadb/datasets/dataset.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     1392 2023-04-03 19:22:40.000000 dnadb-0.3.0/src/dnadb/datasets/greengenes.py
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.854793 dnadb-0.3.0/src/dnadb/datasets/silva/
+-rw-r--r--   0 dwl2x     (1000) users      (100)     5492 2023-04-14 13:32:31.000000 dnadb-0.3.0/src/dnadb/datasets/silva/__init__.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     6022 2023-03-27 05:43:12.000000 dnadb-0.3.0/src/dnadb/datasets/silva/taxonomy_map.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     2234 2023-05-10 12:52:14.000000 dnadb-0.3.0/src/dnadb/db.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     4815 2023-05-11 20:35:23.000000 dnadb-0.3.0/src/dnadb/dna.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     5208 2023-05-11 01:32:34.000000 dnadb-0.3.0/src/dnadb/fasta.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     5969 2023-05-11 01:44:43.000000 dnadb-0.3.0/src/dnadb/fastq.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)        0 2023-05-09 22:29:41.000000 dnadb-0.3.0/src/dnadb/otu.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)    19471 2023-05-13 03:02:48.000000 dnadb-0.3.0/src/dnadb/taxonomy.py
+-rw-r--r--   0 dwl2x     (1000) users      (100)     1473 2023-04-01 17:43:32.000000 dnadb-0.3.0/src/dnadb/utils.py
+drwxr-xr-x   0 dwl2x     (1000) users      (100)        0 2023-05-13 03:03:23.854793 dnadb-0.3.0/src/dnadb.egg-info/
+-rw-r--r--   0 dwl2x     (1000) users      (100)     1802 2023-05-13 03:03:23.000000 dnadb-0.3.0/src/dnadb.egg-info/PKG-INFO
+-rw-r--r--   0 dwl2x     (1000) users      (100)      519 2023-05-13 03:03:23.000000 dnadb-0.3.0/src/dnadb.egg-info/SOURCES.txt
+-rw-r--r--   0 dwl2x     (1000) users      (100)        1 2023-05-13 03:03:23.000000 dnadb-0.3.0/src/dnadb.egg-info/dependency_links.txt
+-rw-r--r--   0 dwl2x     (1000) users      (100)       64 2023-05-13 03:03:23.000000 dnadb-0.3.0/src/dnadb.egg-info/requires.txt
+-rw-r--r--   0 dwl2x     (1000) users      (100)        6 2023-05-13 03:03:23.000000 dnadb-0.3.0/src/dnadb.egg-info/top_level.txt
```

### Comparing `dnadb-0.2.9/LICENSE` & `dnadb-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/PKG-INFO` & `dnadb-0.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnadb
-Version: 0.2.9
+Version: 0.3.0
 Summary: A library for handling DNA files.
 Author-email: David Ludwig <davidludwigii@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 DLii-Research
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `dnadb-0.2.9/pyproject.toml` & `dnadb-0.3.0/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "dnadb"
-version = "0.2.9"
+version = "0.3.0"
 authors = [
   { name="David Ludwig", email="davidludwigii@gmail.com" },
 ]
 description = "A library for handling DNA files."
 readme = "README.md"
 license = { file="LICENSE" }
 requires-python = ">=3.8"
@@ -16,14 +16,15 @@
   "Programming Language :: Python :: 3",
   "License :: OSI Approved :: MIT License",
   "Operating System :: OS Independent",
 ]
 dependencies = [
   "lmdbm-lockable >= 0.0.5",
   "scikit-bio ~= 0.5.8",
+  "sortedcontainers >= 2.4.0"
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/DLii-Research/dnadb"
 "Bug Tracker" = "https://github.com/DLii-Research/dnadb/issues"
 
 [tool.ruff]
```

### Comparing `dnadb-0.2.9/src/dnadb/datasets/dataset.py` & `dnadb-0.3.0/src/dnadb/datasets/dataset.py`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/src/dnadb/datasets/greengenes.py` & `dnadb-0.3.0/src/dnadb/datasets/greengenes.py`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/src/dnadb/datasets/silva/__init__.py` & `dnadb-0.3.0/src/dnadb/datasets/silva/__init__.py`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/src/dnadb/datasets/silva/taxonomy_map.py` & `dnadb-0.3.0/src/dnadb/datasets/silva/taxonomy_map.py`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/src/dnadb/dna.py` & `dnadb-0.3.0/src/dnadb/dna.py`

 * *Files 24% similar despite different names*

```diff
@@ -34,15 +34,14 @@
     IUPAC_AUGMENT_LOOKUP_TABLE[BASE_LOOKUP_TABLE[ord(__base) - ord('A')]] = __repeated_bases
 
 ENC_AMBIGUOUS_BASE_MAP = {BASE_LOOKUP_TABLE[ord(b) - 65]: tuple(BASE_LOOKUP_TABLE[ord(c) - 65] for c in cs)
     for b, cs in IUPAC_MAP.items()}
 
 # DNA Sequence Encoding/Decoding -------------------------------------------------------------------
 
-
 def encode(ascii_bases: npt.NDArray[np.uint8]) ->  npt.NDArray[np.uint8]:
     """
     Encode the given DNA bases in ASCII form into an integer vector representation.
     """
     return BASE_LOOKUP_TABLE[ascii_bases - 65]
 
 
@@ -129,56 +128,7 @@
 
 
 def to_dna(rna_sequence: str) -> str:
     """
     Convert a DNA sequence to RNA.
     """
     return rna_sequence.replace('U', 'T')
-
-# Containers ---------------------------------------------------------------------------------------
-
-class DnaSequence(abc.ABC):
-    """
-    A container for a DNA sequence.
-    """
-    @property
-    @abc.abstractmethod
-    def encoded(self) -> npt.NDArray[np.uint8]:
-        raise NotImplementedError()
-
-    def __bytes__(self):
-        return self.encoded.tobytes()
-
-    @abc.abstractmethod
-    def __str__(self):
-        raise NotImplementedError()
-
-    def __repr__(self):
-        return str(self)
-
-class DecodedDnaSequence(DnaSequence):
-    """
-    A container class for a raw DNA sequence string.
-    """
-    def __init__(self, sequence: str):
-        self.__sequence = sequence
-
-    @property
-    def encoded(self) -> npt.NDArray[np.uint8]:
-        return encode_sequence(str(self))
-
-    def __str__(self):
-        return self.__sequence
-
-class EncodedDnaSequence(DnaSequence):
-    """
-    A container class for an encoded DNA sequence.
-    """
-    def __init__(self, sequence: npt.NDArray[np.uint8]):
-        self.__sequence = sequence
-
-    @property
-    def encoded(self) -> npt.NDArray[np.uint8]:
-        return self.__sequence
-
-    def __str__(self):
-        return decode_sequence(self.__sequence)
```

### Comparing `dnadb-0.2.9/src/dnadb/fasta.py` & `dnadb-0.3.0/src/dnadb/fasta.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,22 +1,30 @@
+from dataclasses import dataclass
 from functools import singledispatchmethod
 import io
 from lmdbm import Lmdb
 import numpy as np
 from pathlib import Path
 from typing import Generator, Iterable, Tuple, Union
 
-from .db import DbFactory
+from .db import DbFactory, DbWrapper
 from .taxonomy import TaxonomyEntry
 from .utils import open_file
 
+@dataclass(frozen=True, order=True)
 class FastaEntry:
     """
     A container class to represent a FASTA entry
     """
+    __slots__ = ("identifier", "sequence", "extra")
+
+    identifier: str
+    sequence: str
+    extra: str
+
     @classmethod
     def deserialize(cls, entry: bytes) -> "FastaEntry":
         """
         Deserialize a FASTA entry from a byte string
         """
         return cls(*entry.decode().split('\x00'))
 
@@ -28,39 +36,28 @@
         header, *sequence_parts = entry.split('\n')
         header_line = header[1:].rstrip().split(maxsplit=1)
         identifier = header_line[0]
         extra = header_line[1] if len(header_line) > 1 else ""
         sequence = "".join(sequence_parts)
         return cls(identifier, sequence, extra)
 
-    def __init__(self, identifier: str, sequence: str, extra: str = ""):
-        self.identifier = identifier
-        self.sequence = sequence
-        self.extra = extra
-
     def serialize(self) -> bytes:
         return "\x00".join((self.identifier, self.sequence, self.extra)).encode()
 
     def __str__(self):
         header_line = f"{self.identifier} {self.extra}".rstrip()
         return f">{header_line}\n{self.sequence}"
 
-    def __eq__(self, other):
-        return self.identifier == other.identifier \
-            and self.sequence == other.sequence \
-            and self.extra == other.extra
-
-    def __repr__(self):
-        return str(self)
-
 
 class FastaDbFactory(DbFactory):
     """
     A factory for creating LMDB-backed databases of FASTA entries.
     """
+    __slots__ = ("num_entries", "has_ambiguous_bases")
+
     def __init__(self, path: Union[str, Path], chunk_size: int = 10000):
         super().__init__(path, chunk_size)
         self.num_entries = np.int32(0)
         self.has_ambiguous_bases = False
 
     def write_entry(self, entry: FastaEntry):
         """
@@ -75,22 +72,20 @@
             self.write_entry(entry)
 
     def before_close(self):
         self.write("length", self.num_entries.tobytes())
         super().before_close()
 
 
-class FastaDb:
+class FastaDb(DbWrapper):
     """
     An LMDB-backed database of FASTA entries.
     """
     def __init__(self, fasta_db_path: Union[str, Path]):
-        super().__init__()
-        self.path = Path(fasta_db_path).absolute()
-        self.db = Lmdb.open(str(self.path), lock=False)
+        super().__init__(fasta_db_path)
         self.length = np.frombuffer(self.db["length"], dtype=np.int32, count=1)[0]
 
     def __len__(self):
         return self.length
 
     @singledispatchmethod
     def __contains__(self, sequence_index: int) -> bool:
```

### Comparing `dnadb-0.2.9/src/dnadb/fastq.py` & `dnadb-0.3.0/src/dnadb/fastq.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,31 +1,57 @@
+from dataclasses import dataclass
 import io
 from lmdbm import Lmdb
 import numpy as np
 import numpy.typing as npt
 from pathlib import Path
 from typing import Generator, Iterable, Tuple, Union
 
-from .db import DbFactory
+from .db import DbFactory, DbWrapper
 from .utils import open_file
 
 def phred_encode(probabilities: npt.ArrayLike, encoding: int = 33) -> str:
     scores = (-10 * np.log10(np.array(probabilities))).astype(int)
     return ''.join((chr(score + encoding)) for score in scores)
 
 
 def phred_decode(qualities: str, encoding: int = 33) -> npt.NDArray[np.float64]:
     scores = np.array([(ord(token) - encoding) for token in qualities])
     return 10**(scores / -10)
 
 
+@dataclass(frozen=True, order=True)
 class FastqHeader:
     """
-    A class representation of the sequence identifier of a FASTQ entry.
+    A class representation of the header of a FASTQ entry.
     """
+    __slots__ = (
+        "instrument",
+        "run_number",
+        "flowcell_id",
+        "lane",
+        "tile",
+        "pos",
+        "read_type",
+        "is_filtered",
+        "control_number",
+        "sequence_index"
+    )
+
+    instrument: str
+    run_number: int
+    flowcell_id: str
+    lane: int
+    tile: int
+    pos: Tuple[int, int]
+    read_type: int
+    is_filtered: bool
+    control_number: int
+    sequence_index: str
+
     @classmethod
     def deserialize(cls, sequence_id: bytes):
         return cls.from_str(sequence_id.decode())
 
     @classmethod
     def from_str(cls, sequence_id: str) -> "FastqHeader":
         # Split up the sequence ID information
@@ -41,54 +67,18 @@
             pos=tuple(map(int, left[5:])),
             read_type=int(right[0]),
             is_filtered=right[1] == 'Y',
             control_number=int(right[2]),
             sequence_index=right[3]
         )
 
-    def __init__(
-        self,
-        instrument: str,
-        run_number: int,
-        flowcell_id: str,
-        lane: int,
-        tile: int,
-        pos: Tuple[int, int],
-        read_type: int,
-        is_filtered: bool,
-        control_number: int,
-        sequence_index: str
-    ):
-        self.instrument = instrument
-        self.run_number = run_number
-        self.flowcell_id = flowcell_id
-        self.lane = lane
-        self.tile = tile
-        self.pos = pos
-        self.read_type = read_type
-        self.is_filtered = is_filtered
-        self.control_number = control_number
-        self.sequence_index = sequence_index
-
     # Serialize a FastqHeader object to a byte string
     def serialize(self) -> bytes:
         return str(self).encode()
 
-    def __eq__(self, other: "FastqHeader"):
-        return self.instrument == other.instrument \
-            and self.run_number == other.run_number \
-            and self.flowcell_id == other.flowcell_id \
-            and self.lane == other.lane \
-            and self.tile == other.tile \
-            and self.pos == other.pos \
-            and self.read_type == other.read_type \
-            and self.is_filtered == other.is_filtered \
-            and self.control_number == other.control_number \
-            and self.sequence_index == other.sequence_index
-
     def __str__(self):
         sequence_id = '@'
         sequence_id += ':'.join(map(str, [
             self.instrument,
             self.run_number,
             self.flowcell_id,
             self.lane,
@@ -100,59 +90,45 @@
             self.read_type,
             'Y' if self.is_filtered else 'N',
             self.control_number,
             self.sequence_index
         ]))
         return sequence_id
 
-    def __repr__(self):
-        return str(self)
-
 
+@dataclass(frozen=True, order=True)
 class FastqEntry:
     """
     A class representation of a FASTQ entry containing the sequnce identifier, sequence, and quality
     scores.
     """
+    __slots__ = ("header_str", "sequence", "quality_scores")
+
+    header_str: str
+    sequence: str
+    quality_scores: str
+
     @classmethod
     def deserialize(cls, entry: bytes) -> "FastqEntry":
         return cls(*entry.decode().split('\x00'))
 
     @classmethod
     def from_str(cls, entry: str) -> "FastqEntry":
         header, sequence, _, quality_scores= entry.rstrip().split('\n')
-        return FastqEntry(header, sequence, quality_scores)
-
-    def __init__(
-        self,
-        header: str,
-        sequence: str,
-        quality_scores: str,
-    ):
-        self.__header = header
-        self.sequence = sequence.strip()
-        self.quality_scores = quality_scores.strip()
+        return cls(header, sequence, quality_scores)
 
     def serialize(self) -> bytes:
-        return '\x00'.join((self.__header, self.sequence, self.quality_scores)).encode()
+        return '\x00'.join((self.header_str, self.sequence, self.quality_scores)).encode()
 
     @property
     def header(self):
-        return FastqHeader.from_str(self.__header)
-
-    def __eq__(self, other: "FastqEntry"):
-        return self.header == other.header \
-            and self.sequence == other.sequence \
-            and self.quality_scores == other.quality_scores
+        return FastqHeader.from_str(self.header_str)
 
     def __str__(self):
-        return f"{self.header}\n{self.sequence}\n+\n{self.quality_scores}"
-
-    def __repr__(self):
-        return "FastqEntry:\n" + '\n'.join(f"  {s}" for s in str(self).split('\n'))
+        return f"{self.header_str}\n{self.sequence}\n+\n{self.quality_scores}"
 
 
 class FastqDbFactory(DbFactory):
     """
     A factory for creating LMDB-backed databases of FASTA entries.
     """
     def __init__(self, path: Union[str, Path], chunk_size: int = 10000):
@@ -171,18 +147,17 @@
             self.write_entry(entry)
 
     def before_close(self):
         self.write("length", self.num_entries.tobytes())
         super().before_close()
 
 
-class FastqDb:
+class FastqDb(DbWrapper):
     def __init__(self, fastq_db_path: Union[str, Path]):
-        self.path = Path(fastq_db_path).absolute()
-        self.db = Lmdb.open(str(self.path), lock=False)
+        super().__init__(fastq_db_path)
         self.length = np.frombuffer(self.db["length"], dtype=np.int32, count=1)[0]
 
     def __len__(self):
         return self.length
 
     def __contains__(self, sequence_index: int) -> bool:
         return str(sequence_index) in self.db
```

### Comparing `dnadb-0.2.9/src/dnadb/utils.py` & `dnadb-0.3.0/src/dnadb/utils.py`

 * *Files identical despite different names*

### Comparing `dnadb-0.2.9/src/dnadb.egg-info/PKG-INFO` & `dnadb-0.3.0/src/dnadb.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dnadb
-Version: 0.2.9
+Version: 0.3.0
 Summary: A library for handling DNA files.
 Author-email: David Ludwig <davidludwigii@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 DLii-Research
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

