# Comparing `tmp/snapcast-2.3.2.tar.gz` & `tmp/snapcast-2.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/snapcast-2.3.2.tar", last modified: Mon Mar  6 18:02:03 2023, max compression
+gzip compressed data, was "snapcast-2.3.3.tar", last modified: Sat May 13 12:15:18 2023, max compression
```

## Comparing `snapcast-2.3.2.tar` & `snapcast-2.3.3.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-03-06 18:02:03.000000 snapcast-2.3.2/
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     1701 2022-10-16 21:10:32.000000 snapcast-2.3.2/README.md
-drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/
--rw-rw-r--   0 mzander   (1000) mzander   (1000)        1 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/dependency_links.txt
--rw-rw-r--   0 mzander   (1000) mzander   (1000)       27 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/requires.txt
--rw-rw-r--   0 mzander   (1000) mzander   (1000)      458 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/SOURCES.txt
--rw-rw-r--   0 mzander   (1000) mzander   (1000)      399 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/PKG-INFO
--rw-rw-r--   0 mzander   (1000) mzander   (1000)        9 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast.egg-info/top_level.txt
-drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast/
--rw-rw-r--   0 mzander   (1000) mzander   (1000)        0 2016-12-04 15:23:56.000000 snapcast-2.3.2/snapcast/__init__.py
-drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast/control/
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     5343 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/client.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     2599 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/protocol.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)      303 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/__init__.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)    16687 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/server.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     6490 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/group.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     2012 2023-03-06 18:00:40.000000 snapcast-2.3.2/snapcast/control/stream.py
-drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-03-06 18:02:03.000000 snapcast-2.3.2/snapcast/client/
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     3888 2016-12-04 15:23:56.000000 snapcast-2.3.2/snapcast/client/__init__.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     2034 2016-12-04 15:23:56.000000 snapcast-2.3.2/snapcast/client/gstreamer.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)     3758 2016-12-04 15:23:56.000000 snapcast-2.3.2/snapcast/client/messages.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)      399 2023-03-06 18:02:03.000000 snapcast-2.3.2/PKG-INFO
--rw-rw-r--   0 mzander   (1000) mzander   (1000)      583 2023-03-06 18:01:19.000000 snapcast-2.3.2/setup.py
--rw-rw-r--   0 mzander   (1000) mzander   (1000)       79 2023-03-06 18:02:03.000000 snapcast-2.3.2/setup.cfg
+drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-05-13 12:15:18.306385 snapcast-2.3.3/
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)      399 2023-05-13 12:15:18.306385 snapcast-2.3.3/PKG-INFO
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     1701 2022-10-16 21:10:32.000000 snapcast-2.3.3/README.md
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)       79 2023-05-13 12:15:18.310385 snapcast-2.3.3/setup.cfg
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)      583 2023-05-13 12:12:29.000000 snapcast-2.3.3/setup.py
+drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-05-13 12:15:18.302385 snapcast-2.3.3/snapcast/
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)        0 2016-12-04 15:23:56.000000 snapcast-2.3.3/snapcast/__init__.py
+drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-05-13 12:15:18.302385 snapcast-2.3.3/snapcast/client/
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     3888 2016-12-04 15:23:56.000000 snapcast-2.3.3/snapcast/client/__init__.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     2034 2016-12-04 15:23:56.000000 snapcast-2.3.3/snapcast/client/gstreamer.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     3758 2016-12-04 15:23:56.000000 snapcast-2.3.3/snapcast/client/messages.py
+drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-05-13 12:15:18.306385 snapcast-2.3.3/snapcast/control/
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)      303 2023-03-06 18:00:40.000000 snapcast-2.3.3/snapcast/control/__init__.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     5351 2023-05-13 12:12:21.000000 snapcast-2.3.3/snapcast/control/client.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     6581 2023-05-13 12:12:21.000000 snapcast-2.3.3/snapcast/control/group.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     2599 2023-03-06 18:00:40.000000 snapcast-2.3.3/snapcast/control/protocol.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)    16697 2023-05-13 12:12:21.000000 snapcast-2.3.3/snapcast/control/server.py
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)     2012 2023-03-06 18:00:40.000000 snapcast-2.3.3/snapcast/control/stream.py
+drwxrwxr-x   0 mzander   (1000) mzander   (1000)        0 2023-05-13 12:15:18.302385 snapcast-2.3.3/snapcast.egg-info/
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)      399 2023-05-13 12:15:18.000000 snapcast-2.3.3/snapcast.egg-info/PKG-INFO
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)      458 2023-05-13 12:15:18.000000 snapcast-2.3.3/snapcast.egg-info/SOURCES.txt
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)        1 2023-05-13 12:15:18.000000 snapcast-2.3.3/snapcast.egg-info/dependency_links.txt
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)       27 2023-05-13 12:15:18.000000 snapcast-2.3.3/snapcast.egg-info/requires.txt
+-rw-rw-r--   0 mzander   (1000) mzander   (1000)        9 2023-05-13 12:15:18.000000 snapcast-2.3.3/snapcast.egg-info/top_level.txt
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `snapcast-2.3.2/README.md` & `snapcast-2.3.3/README.md`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/snapcast/control/client.py` & `snapcast-2.3.3/snapcast/control/client.py`

 * *Files 3% similar despite different names*

```diff
@@ -79,15 +79,15 @@
 
     async def set_muted(self, status):
         """Set client mute status."""
         new_volume = self._client['config']['volume']
         new_volume['muted'] = status
         self._client['config']['volume']['muted'] = status
         await self._server.client_volume(self.identifier, new_volume)
-        _LOGGER.info('set muted to %s on %s', status, self.friendly_name)
+        _LOGGER.debug('set muted to %s on %s', status, self.friendly_name)
 
     @property
     def volume(self):
         """Volume percent."""
         return self._client.get('config').get('volume').get('percent')
 
     async def set_volume(self, percent, update_group=True):
@@ -96,65 +96,65 @@
             raise ValueError('Volume percent out of range')
         new_volume = self._client['config']['volume']
         new_volume['percent'] = percent
         self._client['config']['volume']['percent'] = percent
         await self._server.client_volume(self.identifier, new_volume)
         if update_group:
             self._server.group(self.group.identifier).callback()
-        _LOGGER.info('set volume to %s on %s', percent, self.friendly_name)
+        _LOGGER.debug('set volume to %s on %s', percent, self.friendly_name)
 
     def groups_available(self):
         """Get available group objects."""
         return list(self._server.groups)
 
     def update_volume(self, data):
         """Update volume."""
         self._client['config']['volume'] = data['volume']
-        _LOGGER.info('updated volume on %s', self.friendly_name)
+        _LOGGER.debug('updated volume on %s', self.friendly_name)
         self._server.group(self.group.identifier).callback()
         self.callback()
 
     def update_name(self, data):
         """Update name."""
         self._client['config']['name'] = data['name']
-        _LOGGER.info('updated name on %s', self.friendly_name)
+        _LOGGER.debug('updated name on %s', self.friendly_name)
         self.callback()
 
     def update_latency(self, data):
         """Update latency."""
         self._client['config']['latency'] = data['latency']
-        _LOGGER.info('updated latency on %s', self.friendly_name)
+        _LOGGER.debug('updated latency on %s', self.friendly_name)
         self.callback()
 
     def update_connected(self, status):
         """Update connected."""
         self._client['connected'] = status
-        _LOGGER.info('updated connected status to %s on %s', status, self.friendly_name)
+        _LOGGER.debug('updated connected status to %s on %s', status, self.friendly_name)
         self.callback()
 
     def snapshot(self):
         """Snapshot current state."""
         self._snapshot = {
             'name': self.name,
             'volume': self.volume,
             'muted': self.muted,
             'latency': self.latency
         }
-        _LOGGER.info('took snapshot of current state of %s', self.friendly_name)
+        _LOGGER.debug('took snapshot of current state of %s', self.friendly_name)
 
     async def restore(self):
         """Restore snapshotted state."""
         if not self._snapshot:
             return
         await self.set_name(self._snapshot['name'])
         await self.set_volume(self._snapshot['volume'])
         await self.set_muted(self._snapshot['muted'])
         await self.set_latency(self._snapshot['latency'])
         self.callback()
-        _LOGGER.info('restored snapshot of state of %s', self.friendly_name)
+        _LOGGER.debug('restored snapshot of state of %s', self.friendly_name)
 
     def callback(self):
         """Run callback."""
         if self._callback_func and callable(self._callback_func):
             self._callback_func(self)
 
     def set_callback(self, func):
```

### Comparing `snapcast-2.3.2/snapcast/control/protocol.py` & `snapcast-2.3.3/snapcast/control/protocol.py`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/snapcast/control/server.py` & `snapcast-2.3.3/snapcast/control/server.py`

 * *Files 7% similar despite different names*

```diff
@@ -106,24 +106,24 @@
         self._on_disconnect_callback_func = None
         self._new_client_callback_func = None
 
     async def start(self):
         """Initiate server connection."""
         self._is_stopped = False
         await self._do_connect()
-        _LOGGER.info('connected to snapserver on %s:%s', self._host, self._port)
+        _LOGGER.debug('connected to snapserver on %s:%s', self._host, self._port)
         status = await self.status()
         self.synchronize(status)
         self._on_server_connect()
 
     async def stop(self):
         """Stop server."""
         self._is_stopped = True
         self._do_disconnect()
-        _LOGGER.info('disconnected from snapserver on %s:%s', self._host, self._port)
+        _LOGGER.debug('disconnected from snapserver on %s:%s', self._host, self._port)
         self._clients = {}
         self._streams = {}
         self._groups = {}
         self._version = None
         self._protocol = None
         self._transport = None
 
@@ -135,15 +135,15 @@
     async def _do_connect(self):
         """Perform the connection to the server."""
         self._transport, self._protocol = await self._loop.create_connection(
             lambda: SnapcastProtocol(self._callbacks), self._host, self._port)
 
     def _reconnect_cb(self):
         """Callback to reconnect to the server."""
-        _LOGGER.info('try reconnect')
+        _LOGGER.debug('try reconnect')
 
         async def try_reconnect():
             """Actual coroutine ro try to reconnect or reschedule."""
             try:
                 await self._do_connect()
             except OSError:
                 self._loop.call_later(SERVER_RECONNECT_DELAY,
@@ -306,21 +306,21 @@
         result = await self._transact(method, params)
         if isinstance(result, dict) and key in result:
             return result.get(key)
         return result
 
     def _on_server_connect(self):
         """Handle server connection."""
-        _LOGGER.info('Server connected')
+        _LOGGER.debug('Server connected')
         if self._on_connect_callback_func and callable(self._on_connect_callback_func):
             self._on_connect_callback_func()
 
     def _on_server_disconnect(self, exception):
         """Handle server disconnection."""
-        _LOGGER.info('Server disconnected')
+        _LOGGER.debug('Server disconnected')
         if self._on_disconnect_callback_func and callable(self._on_disconnect_callback_func):
             self._on_disconnect_callback_func(exception)
         if not self._is_stopped:
             self._do_disconnect()
             self._protocol = None
             self._transport = None
             if self._reconnect:
@@ -357,20 +357,20 @@
             client = self._clients[data.get('id')]
             client.update_connected(True)
         else:
             client = Snapclient(self, data.get('client'))
             self._clients[data.get('id')] = client
             if self._new_client_callback_func and callable(self._new_client_callback_func):
                 self._new_client_callback_func(client)
-        _LOGGER.info('client %s connected', client.friendly_name)
+        _LOGGER.debug('client %s connected', client.friendly_name)
 
     def _on_client_disconnect(self, data):
         """Handle client disconnect."""
         self._clients[data.get('id')].update_connected(False)
-        _LOGGER.info('client %s disconnected', self._clients[data.get('id')].friendly_name)
+        _LOGGER.debug('client %s disconnected', self._clients[data.get('id')].friendly_name)
 
     def _on_client_volume_changed(self, data):
         """Handle client volume change."""
         self._clients.get(data.get('id')).update_volume(data)
 
     def _on_client_name_changed(self, data):
         """Handle client name changed."""
@@ -380,34 +380,34 @@
         """Handle client latency changed."""
         self._clients.get(data.get('id')).update_latency(data)
 
     def _on_stream_meta(self, data):  # deprecated
         """Handle stream metadata update."""
         stream = self._streams[data.get('id')]
         stream.update_meta(data.get('meta'))
-        _LOGGER.info('stream %s metadata updated', stream.friendly_name)
+        _LOGGER.debug('stream %s metadata updated', stream.friendly_name)
         for group in self._groups.values():
             if group.stream == data.get('id'):
                 group.callback()
 
     def _on_stream_properties(self, data):
         """Handle stream properties update."""
         stream = self._streams[data.get('id')]
         stream.update_properties(data.get('properties'))
-        _LOGGER.info('stream %s properties updated', stream.friendly_name)
+        _LOGGER.debug('stream %s properties updated', stream.friendly_name)
         for group in self._groups.values():
             if group.stream == data.get('id'):
                 group.callback()
                 for clientID in group.clients:
                     self._clients.get(clientID).callback()
 
     def _on_stream_update(self, data):
         """Handle stream update."""
         self._streams[data.get('id')].update(data.get('stream'))
-        _LOGGER.info('stream %s updated', self._streams[data.get('id')].friendly_name)
+        _LOGGER.debug('stream %s updated', self._streams[data.get('id')].friendly_name)
         self._streams[data.get("id")].callback()
         for group in self._groups.values():
             if group.stream == data.get('id'):
                 group.callback()
                 for clientID in group.clients:
                     self._clients.get(clientID).callback()
```

### Comparing `snapcast-2.3.2/snapcast/control/group.py` & `snapcast-2.3.3/snapcast/control/group.py`

 * *Files 6% similar despite different names*

```diff
@@ -42,15 +42,15 @@
         """Get stream identifier."""
         return self._group.get('stream_id')
 
     async def set_stream(self, stream_id):
         """Set group stream."""
         self._group['stream_id'] = stream_id
         await self._server.group_stream(self.identifier, stream_id)
-        _LOGGER.info('set stream to %s on %s', stream_id, self.friendly_name)
+        _LOGGER.debug('set stream to %s on %s', stream_id, self.friendly_name)
 
     @property
     def stream_status(self):
         """Get stream status."""
         return self._server.stream(self.stream).status
 
     @property
@@ -58,15 +58,15 @@
         """Get mute status."""
         return self._group.get('muted')
 
     async def set_muted(self, status):
         """Set group mute status."""
         self._group['muted'] = status
         await self._server.group_mute(self.identifier, status)
-        _LOGGER.info('set muted to %s on %s', status, self.friendly_name)
+        _LOGGER.debug('set muted to %s on %s', status, self.friendly_name)
 
     @property
     def volume(self):
         """Get volume."""
         volume_sum = 0
         for client in self._group.get('clients'):
             volume_sum += self._server.client(client.get('id')).volume
@@ -74,15 +74,15 @@
 
     async def set_volume(self, volume):
         """Set volume."""
         if volume not in range(0, 101):
             raise ValueError('Volume out of range')
         current_volume = self.volume
         if volume == current_volume:
-            _LOGGER.info('left volume at %s on group %s', volume, self.friendly_name)
+            _LOGGER.debug('left volume at %s on group %s', volume, self.friendly_name)
             return
         delta = volume - current_volume
         if delta < 0:
             ratio = (current_volume - volume) / current_volume
         else:
             ratio = (volume - current_volume) / (100 - current_volume)
         for data in self._group.get('clients'):
@@ -96,91 +96,92 @@
             await client.set_volume(client_volume, update_group=False)
             client.update_volume({
                 'volume': {
                     'percent': client_volume,
                     'muted': client.muted
                 }
             })
-        _LOGGER.info('set volume to %s on group %s', volume, self.friendly_name)
+        _LOGGER.debug('set volume to %s on group %s', volume, self.friendly_name)
 
     @property
     def friendly_name(self):
         """Get friendly name."""
-        return self.name if self.name != '' else self.stream
+        return self.name if self.name != '' else "+".join(
+            sorted([self._server.client(c).friendly_name for c in self.clients]))
 
     @property
     def clients(self):
         """Get client identifiers."""
         return [client.get('id') for client in self._group.get('clients')]
 
     async def add_client(self, client_identifier):
         """Add a client."""
         if client_identifier in self.clients:
             _LOGGER.error('%s already in group %s', client_identifier, self.identifier)
             return
         new_clients = self.clients
         new_clients.append(client_identifier)
         await self._server.group_clients(self.identifier, new_clients)
-        _LOGGER.info('added %s to %s', client_identifier, self.identifier)
+        _LOGGER.debug('added %s to %s', client_identifier, self.identifier)
         status = await self._server.status()
         self._server.synchronize(status)
         self._server.client(client_identifier).callback()
         self.callback()
 
     async def remove_client(self, client_identifier):
         """Remove a client."""
         new_clients = self.clients
         new_clients.remove(client_identifier)
         await self._server.group_clients(self.identifier, new_clients)
-        _LOGGER.info('removed %s from %s', client_identifier, self.identifier)
+        _LOGGER.debug('removed %s from %s', client_identifier, self.identifier)
         status = await self._server.status()
         self._server.synchronize(status)
         self._server.client(client_identifier).callback()
         self.callback()
 
     def streams_by_name(self):
         """Get available stream objects by name."""
         return {stream.friendly_name: stream for stream in self._server.streams}
 
     def update_mute(self, data):
         """Update mute."""
         self._group['muted'] = data['mute']
         self.callback()
-        _LOGGER.info('updated mute on %s', self.friendly_name)
+        _LOGGER.debug('updated mute on %s', self.friendly_name)
 
     def update_name(self, data):
         """Update name."""
         self._group['name'] = data['name']
-        _LOGGER.info('updated name on %s', self.name)
+        _LOGGER.debug('updated name on %s', self.name)
         self.callback()
 
     def update_stream(self, data):
         """Update stream."""
         self._group['stream_id'] = data['stream_id']
         self.callback()
-        _LOGGER.info('updated stream to %s on %s', self.stream, self.friendly_name)
+        _LOGGER.debug('updated stream to %s on %s', self.stream, self.friendly_name)
 
     def snapshot(self):
         """Snapshot current state."""
         self._snapshot = {
             'muted': self.muted,
             'volume': self.volume,
             'stream': self.stream
         }
-        _LOGGER.info('took snapshot of current state of %s', self.friendly_name)
+        _LOGGER.debug('took snapshot of current state of %s', self.friendly_name)
 
     async def restore(self):
         """Restore snapshotted state."""
         if not self._snapshot:
             return
         await self.set_muted(self._snapshot['muted'])
         await self.set_volume(self._snapshot['volume'])
         await self.set_stream(self._snapshot['stream'])
         self.callback()
-        _LOGGER.info('restored snapshot of state of %s', self.friendly_name)
+        _LOGGER.debug('restored snapshot of state of %s', self.friendly_name)
 
     def callback(self):
         """Run callback."""
         if self._callback_func and callable(self._callback_func):
             self._callback_func(self)
 
     def set_callback(self, func):
```

### Comparing `snapcast-2.3.2/snapcast/control/stream.py` & `snapcast-2.3.3/snapcast/control/stream.py`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/snapcast/client/__init__.py` & `snapcast-2.3.3/snapcast/client/__init__.py`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/snapcast/client/gstreamer.py` & `snapcast-2.3.3/snapcast/client/gstreamer.py`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/snapcast/client/messages.py` & `snapcast-2.3.3/snapcast/client/messages.py`

 * *Files identical despite different names*

### Comparing `snapcast-2.3.2/setup.py` & `snapcast-2.3.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='snapcast',
-    version='2.3.2',
+    version='2.3.3',
     description='Control Snapcast.',
     url='https://github.com/happyleavesaoc/python-snapcast/',
     license='MIT',
     author='happyleaves',
     author_email='happyleaves.tfr@gmail.com',
     packages=['snapcast', 'snapcast.control', 'snapcast.client'],
     install_requires=[
```

