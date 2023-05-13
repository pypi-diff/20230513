# Comparing `tmp/urllib3_ext_hface-0.2.0.tar.gz` & `tmp/urllib3_ext_hface-0.2.2.tar.gz`

## Comparing `urllib3_ext_hface-0.2.0.tar` & `urllib3_ext_hface-0.2.2.tar`

### file list

```diff
@@ -1,50 +1,50 @@
--rw-r--r--   0        0        0      346 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/CHANGELOG.rst
--rw-r--r--   0        0        0      100 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/dev-requirements.txt
--rw-r--r--   0        0        0       52 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/changelog.rst
--rw-r--r--   0        0        0     2869 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/cli.rst
--rw-r--r--   0        0        0     1971 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/common.rst
--rw-r--r--   0        0        0     1614 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/conf.py
--rw-r--r--   0        0        0     7367 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/connections.rst
--rw-r--r--   0        0        0     4257 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/facade.rst
--rw-r--r--   0        0        0     1021 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/index.rst
--rw-r--r--   0        0        0     1008 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/install.rst
--rw-r--r--   0        0        0     2993 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/intro.rst
--rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/license.rst
--rw-r--r--   0        0        0     5453 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/protocols.rst
--rw-r--r--   0        0        0       26 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/requirements.txt
--rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/_static/custom.css
--rw-r--r--   0        0        0    33109 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/docs/_static/hface.png
--rw-r--r--   0        0        0     1616 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/__init__.py
--rw-r--r--   0        0        0     1267 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_configuration.py
--rw-r--r--   0        0        0     1207 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_error_codes.py
--rw-r--r--   0        0        0      801 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_typing.py
--rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_version.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/py.typed
--rw-r--r--   0        0        0     1035 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/events/__init__.py
--rw-r--r--   0        0        0     4214 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/events/_events.py
--rw-r--r--   0        0        0     1648 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/__init__.py
--rw-r--r--   0        0        0     4719 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_factories.py
--rw-r--r--   0        0        0     9029 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_protocols.py
--rw-r--r--   0        0        0     1513 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_registry.py
--rw-r--r--   0        0        0      703 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/__init__.py
--rw-r--r--   0        0        0     1439 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_factories.py
--rw-r--r--   0        0        0     2221 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_helpers.py
--rw-r--r--   0        0        0    13753 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_protocol.py
--rw-r--r--   0        0        0      703 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/__init__.py
--rw-r--r--   0        0        0     2888 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/_factories.py
--rw-r--r--   0        0        0     4763 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/_protocol.py
--rw-r--r--   0        0        0      808 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/__init__.py
--rw-r--r--   0        0        0     2574 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/_factories.py
--rw-r--r--   0        0        0     9382 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/_protocol.py
--rw-r--r--   0        0        0     1682 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/_quic.py
--rw-r--r--   0        0        0     1274 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/tests/helpers.py
--rw-r--r--   0        0        0    19814 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/tests/test_http1.py
--rw-r--r--   0        0        0    16257 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/tests/test_http2.py
--rw-r--r--   0        0        0     2274 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/tests/test_integration.py
--rw-r--r--   0        0        0       88 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/.gitignore
--rw-r--r--   0        0        0      247 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/AUTHORS
--rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/LICENSE
--rw-r--r--   0        0        0      565 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/NOTICE
--rw-r--r--   0        0        0     1347 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/README.rst
--rw-r--r--   0        0        0     2860 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/pyproject.toml
--rw-r--r--   0        0        0     3165 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0      577 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/CHANGELOG.rst
+-rw-r--r--   0        0        0      100 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/dev-requirements.txt
+-rw-r--r--   0        0        0       52 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/changelog.rst
+-rw-r--r--   0        0        0     2869 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/cli.rst
+-rw-r--r--   0        0        0     1971 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/common.rst
+-rw-r--r--   0        0        0     1614 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/conf.py
+-rw-r--r--   0        0        0     7367 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/connections.rst
+-rw-r--r--   0        0        0     4257 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/facade.rst
+-rw-r--r--   0        0        0     1021 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/index.rst
+-rw-r--r--   0        0        0     1008 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/install.rst
+-rw-r--r--   0        0        0     2993 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/intro.rst
+-rw-r--r--   0        0        0       68 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/license.rst
+-rw-r--r--   0        0        0     5453 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/protocols.rst
+-rw-r--r--   0        0        0       26 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/requirements.txt
+-rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/_static/custom.css
+-rw-r--r--   0        0        0    33109 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/docs/_static/hface.png
+-rw-r--r--   0        0        0     1616 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/__init__.py
+-rw-r--r--   0        0        0     1547 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_configuration.py
+-rw-r--r--   0        0        0     1207 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_error_codes.py
+-rw-r--r--   0        0        0      801 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_typing.py
+-rw-r--r--   0        0        0       58 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_version.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/py.typed
+-rw-r--r--   0        0        0     1131 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/events/__init__.py
+-rw-r--r--   0        0        0     4875 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/events/_events.py
+-rw-r--r--   0        0        0     1648 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/__init__.py
+-rw-r--r--   0        0        0     4719 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_factories.py
+-rw-r--r--   0        0        0     8977 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_protocols.py
+-rw-r--r--   0        0        0     1513 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_registry.py
+-rw-r--r--   0        0        0      703 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/__init__.py
+-rw-r--r--   0        0        0     1439 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_factories.py
+-rw-r--r--   0        0        0     2221 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_helpers.py
+-rw-r--r--   0        0        0    13753 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_protocol.py
+-rw-r--r--   0        0        0      703 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/__init__.py
+-rw-r--r--   0        0        0     2888 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/_factories.py
+-rw-r--r--   0        0        0     4917 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/_protocol.py
+-rw-r--r--   0        0        0      778 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/__init__.py
+-rw-r--r--   0        0        0     2256 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/_factories.py
+-rw-r--r--   0        0        0     6652 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/_protocol.py
+-rw-r--r--   0        0        0     1102 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/_quic.py
+-rw-r--r--   0        0        0     1274 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/tests/helpers.py
+-rw-r--r--   0        0        0    19814 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/tests/test_http1.py
+-rw-r--r--   0        0        0    16257 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/tests/test_http2.py
+-rw-r--r--   0        0        0     2274 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/tests/test_integration.py
+-rw-r--r--   0        0        0       88 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/.gitignore
+-rw-r--r--   0        0        0      247 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/AUTHORS
+-rw-r--r--   0        0        0    11357 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/LICENSE
+-rw-r--r--   0        0        0      565 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/NOTICE
+-rw-r--r--   0        0        0     1370 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/README.rst
+-rw-r--r--   0        0        0     2860 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/pyproject.toml
+-rw-r--r--   0        0        0     3188 2020-02-02 00:00:00.000000 urllib3_ext_hface-0.2.2/PKG-INFO
```

### Comparing `urllib3_ext_hface-0.2.0/docs/cli.rst` & `urllib3_ext_hface-0.2.2/docs/cli.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/common.rst` & `urllib3_ext_hface-0.2.2/docs/common.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/conf.py` & `urllib3_ext_hface-0.2.2/docs/conf.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/connections.rst` & `urllib3_ext_hface-0.2.2/docs/connections.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/facade.rst` & `urllib3_ext_hface-0.2.2/docs/facade.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/index.rst` & `urllib3_ext_hface-0.2.2/docs/index.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/install.rst` & `urllib3_ext_hface-0.2.2/docs/install.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/intro.rst` & `urllib3_ext_hface-0.2.2/docs/intro.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/protocols.rst` & `urllib3_ext_hface-0.2.2/docs/protocols.rst`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/docs/_static/hface.png` & `urllib3_ext_hface-0.2.2/docs/_static/hface.png`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/__init__.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_configuration.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_configuration.py`

 * *Files 21% similar despite different names*

```diff
@@ -12,14 +12,16 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
 import dataclasses
 
+from aioquic.tls import CipherSuite, SessionTicket
+
 
 @dataclasses.dataclass
 class ClientTLSConfig:
     """
     Client TLS configuration.
     """
 
@@ -31,12 +33,18 @@
 
     #: Directory with CA certificates to trust for server verification
     capath: str | None = None
 
     #: Blob with CA certificates to trust for server verification
     cadata: bytes | None = None
 
+    #: Manually set ciphers to be used in your DTLS
+    cipher_suites: list[CipherSuite] | None = None
+
+    #: The DTLS session ticket which should be used for session resumption
+    session_ticket: SessionTicket | None = None
+
     def clone(self) -> ClientTLSConfig:
         """
         Clone this instance.
         """
         return dataclasses.replace(self)
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_error_codes.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_error_codes.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/_typing.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/_typing.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/events/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/events/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -15,25 +15,29 @@
 from __future__ import annotations
 
 from ._events import (
     ConnectionTerminated,
     DataReceived,
     Event,
     GoawayReceived,
+    HandshakeCompleted,
     HeadersReceived,
     StreamEvent,
     StreamReset,
     StreamResetReceived,
     StreamResetSent,
+    UnclassifiedData,
 )
 
 __all__ = (
     "Event",
     "ConnectionTerminated",
     "GoawayReceived",
     "StreamEvent",
     "StreamReset",
     "StreamResetReceived",
     "StreamResetSent",
     "HeadersReceived",
     "DataReceived",
+    "HandshakeCompleted",
+    "UnclassifiedData",
 )
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/events/_events.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/events/_events.py`

 * *Files 11% similar despite different names*

```diff
@@ -135,14 +135,44 @@
     implementation can send the reset when a peer misbehaves.
 
     Extends :class:`.StreamReset`.
     """
 
 
 @dataclass
+class HandshakeCompleted(Event):
+    alpn_protocol: str | None
+
+    def __repr__(self) -> str:
+        cls = type(self).__name__
+        return f"{cls}(alpn={self.alpn_protocol})"
+
+
+@dataclass
+class UnclassifiedData(StreamEvent):
+    """
+    A frame containing unclassified data was received.
+    This is only useful for debug purposes.
+
+    Extends :class:`.StreamEvent`.
+    """
+
+    data: bytes
+
+    end_stream: bool = False
+
+    def __repr__(self) -> str:
+        cls = type(self).__name__
+        return (
+            f"{cls}(stream_id={self.stream_id!r}, "
+            f"len(data)={len(self.data)}, end_stream={self.end_stream!r})"
+        )
+
+
+@dataclass
 class HeadersReceived(StreamEvent):
     """
     A frame with HTTP headers was received.
 
     Extends :class:`.StreamEvent`.
     """
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/__init__.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_factories.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_factories.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_protocols.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_protocols.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 
 from __future__ import annotations
 
 from abc import ABCMeta, abstractmethod
 from typing import Sequence
 
 from .._error_codes import HTTPErrorCodes
-from .._typing import DatagramType, HeadersType
+from .._typing import HeadersType
 from ..events import Event
 
 
 class OverTCPProtocol(metaclass=ABCMeta):
     """
     Interface for sans-IO protocols on top TCP.
     """
@@ -97,30 +97,30 @@
     def connection_lost(self) -> None:
         """
         Called when the connection is lost or closed.
         """
         raise NotImplementedError
 
     @abstractmethod
-    def datagram_received(self, datagram: DatagramType) -> None:
+    def bytes_received(self, data: bytes) -> None:
         """
         Called when some data is received.
 
-        :param datagram: the received datagram.
+        :param data: the received UDP frame.
         """
         raise NotImplementedError
 
     # Sending direction
 
     @abstractmethod
-    def datagrams_to_send(self) -> Sequence[DatagramType]:
+    def bytes_to_send(self) -> bytes:
         """
         Returns data for sending out of the internal data buffer.
 
-        :return: datagrams to send
+        :return: UDP frame to send
         """
         raise NotImplementedError
 
 
 class OverQUICProtocol(OverUDPProtocol):
     @property
     @abstractmethod
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/_registry.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/_registry.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/__init__.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_factories.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_factories.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_helpers.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_helpers.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http1/_protocol.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http1/_protocol.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/__init__.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/_factories.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/_factories.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http2/_protocol.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http2/_protocol.py`

 * *Files 3% similar despite different names*

```diff
@@ -76,15 +76,22 @@
     def next_event(self) -> Event | None:
         if not self._events:
             return None
         return self._events.popleft()
 
     def _map_events(self, h2_events: list[h2.events.Event]) -> Iterator[Event]:
         for e in h2_events:
-            if isinstance(e, (h2.events.RequestReceived, h2.events.ResponseReceived)):
+            if isinstance(
+                e,
+                (
+                    h2.events.RequestReceived,
+                    h2.events.ResponseReceived,
+                    h2.events.TrailersReceived,
+                ),
+            ):
                 end_stream = e.stream_ended is not None
                 yield HeadersReceived(e.stream_id, e.headers, end_stream=end_stream)
             elif isinstance(e, h2.events.DataReceived):
                 end_stream = e.stream_ended is not None
                 self._connection.acknowledge_received_data(
                     e.flow_controlled_length, e.stream_id
                 )
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/__init__.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -11,10 +11,10 @@
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
 from ._factories import HTTP3ClientFactory
-from ._quic import InvalidPacket, PacketInfo, sniff_packet
+from ._quic import InvalidPacket, PacketInfo
 
-__all__ = ("HTTP3ClientFactory", "InvalidPacket", "PacketInfo", "sniff_packet")
+__all__ = ("HTTP3ClientFactory", "InvalidPacket", "PacketInfo")
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/_factories.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/_factories.py`

 * *Files 13% similar despite different names*

```diff
@@ -10,15 +10,14 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
-import os
 import ssl
 
 import aioquic.h3.connection
 import aioquic.quic.configuration
 import aioquic.quic.connection
 
 from ..._configuration import ClientTLSConfig
@@ -44,27 +43,23 @@
         *,
         remote_address: AddressType,
         server_name: str,
         tls_config: ClientTLSConfig,
     ) -> HTTP3Protocol:
         configuration = self._build_configuration(tls_config=tls_config)
         configuration.server_name = server_name
+        configuration.load_verify_locations(tls_config.cafile)
         return HTTP3ProtocolImpl(configuration, remote_address=remote_address)
 
     def _build_configuration(
         self, *, tls_config: ClientTLSConfig
     ) -> aioquic.quic.configuration.QuicConfiguration:
-        # OpenSSL (so Python builtin ssl.SSLContext) trusts to SSL_CERT_FILE by default.
-        # We set it here explicitly, so that TLS implementations not using OpenSSL
-        # (namely aioquic and our default HTTP/3 implementation) use this variable too.
-        #
-        # We could (and probably should) be more sophisticated in unifying
-        # TLS configuration, but just this one hack helps a lot.
-        tls_cafile = tls_config.cafile or os.environ.get("SSL_CERT_FILE")
         return aioquic.quic.configuration.QuicConfiguration(
             is_client=True,
             verify_mode=ssl.CERT_NONE if tls_config.insecure else ssl.CERT_REQUIRED,
-            cafile=tls_cafile,
+            cafile=tls_config.cafile,
             capath=tls_config.capath,
             cadata=tls_config.cadata,
             alpn_protocols=["h3"],
+            cipher_suites=tls_config.cipher_suites,
+            session_ticket=tls_config.session_ticket,
         )
```

### Comparing `urllib3_ext_hface-0.2.0/src/urllib3_ext_hface/protocols/http3/_quic.py` & `urllib3_ext_hface-0.2.2/src/urllib3_ext_hface/protocols/http3/_quic.py`

 * *Files 26% similar despite different names*

```diff
@@ -34,24 +34,7 @@
     length: int
 
     @property
     def is_initial_packet(self) -> bool:
         if self.length < 1200:
             return False
         return self.packet_type == aioquic.quic.packet.PACKET_TYPE_INITIAL
-
-
-def sniff_packet(data: bytes, *, connection_id_length: int) -> PacketInfo:
-    buf = aioquic.buffer.Buffer(data=data)  # type: ignore[attr-defined]
-    try:
-        header = aioquic.quic.packet.pull_quic_header(
-            buf, host_cid_length=connection_id_length
-        )
-    except ValueError:
-        raise InvalidPacket("Invalid header")
-    return PacketInfo(
-        version=header.version,
-        packet_type=header.packet_type,
-        destination_connection_id=header.destination_cid,
-        source_connection_id=header.source_cid,
-        length=len(data),
-    )
```

### Comparing `urllib3_ext_hface-0.2.0/tests/helpers.py` & `urllib3_ext_hface-0.2.2/tests/helpers.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/tests/test_http1.py` & `urllib3_ext_hface-0.2.2/tests/test_http1.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/tests/test_http2.py` & `urllib3_ext_hface-0.2.2/tests/test_http2.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/tests/test_integration.py` & `urllib3_ext_hface-0.2.2/tests/test_integration.py`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/LICENSE` & `urllib3_ext_hface-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/NOTICE` & `urllib3_ext_hface-0.2.2/NOTICE`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/README.rst` & `urllib3_ext_hface-0.2.2/README.rst`

 * *Files 15% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 
 This project is a fork of the akamai/hface project but highly slimmed.
 The purpose of that project is to enable basic support for HTTP/1.1, HTTP/2 and HTTP/3 in urllib3.
 
 * HTTP/1.1, HTTP/2, and HTTP/3 support
 * Sans-IO_ core with pluggable protocol implementations
 * Layered design with well-defined APIs
+* Client-oriented only
 
 See online documentation_ for more info.
 
 .. _Documentation: https://urllib3.readthedocs.io/
 .. _GitHub: https://github.com/Ousret/urllib3-ext-hface
 .. _PyPI: https://pypi.org/project/urllib3-ext-hface
```

### Comparing `urllib3_ext_hface-0.2.0/pyproject.toml` & `urllib3_ext_hface-0.2.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `urllib3_ext_hface-0.2.0/PKG-INFO` & `urllib3_ext_hface-0.2.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: urllib3-ext-hface
-Version: 0.2.0
+Version: 0.2.2
 Summary: urllib3 extension to support HTTP/1.1, HTTP/2 and HTTP/3 independently of Python httplib
 Project-URL: Changelog, https://github.com/Ousret/urllib3-ext-hface/blob/main/CHANGELOG.rst
 Project-URL: Documentation, https://urllib3.readthedocs.io
 Project-URL: Code, https://github.com/Ousret/urllib3-ext-hface
 Project-URL: Issue tracker, https://github.com/Ousret/urllib3-ext-hface/issues
 Author-email: Miloslav Pojman <mpojman@akamai.com>
 Maintainer-email: "Ahmed R. TAHRI" <ahmed.tahri@cloudnursery.dev>
@@ -47,14 +47,15 @@
 
 This project is a fork of the akamai/hface project but highly slimmed.
 The purpose of that project is to enable basic support for HTTP/1.1, HTTP/2 and HTTP/3 in urllib3.
 
 * HTTP/1.1, HTTP/2, and HTTP/3 support
 * Sans-IO_ core with pluggable protocol implementations
 * Layered design with well-defined APIs
+* Client-oriented only
 
 See online documentation_ for more info.
 
 .. _Documentation: https://urllib3.readthedocs.io/
 .. _GitHub: https://github.com/Ousret/urllib3-ext-hface
 .. _PyPI: https://pypi.org/project/urllib3-ext-hface
```

