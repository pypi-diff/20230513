# Comparing `tmp/aioconnectors-1.6.1.tar.gz` & `tmp/aioconnectors-1.6.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aioconnectors-1.6.1.tar", last modified: Sun Mar  5 21:49:09 2023, max compression
+gzip compressed data, was "aioconnectors-1.6.2.tar", last modified: Sat May 13 06:05:42 2023, max compression
```

## Comparing `aioconnectors-1.6.1.tar` & `aioconnectors-1.6.2.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-03-05 21:49:09.326033 aioconnectors-1.6.1/
--rw-r--r--   0 mm        (1000) mm        (1000)    11357 2020-06-11 21:16:01.000000 aioconnectors-1.6.1/LICENSE
--rw-rw-r--   0 mm        (1000) mm        (1000)    66939 2023-03-05 21:49:09.326033 aioconnectors-1.6.1/PKG-INFO
--rw-rw-r--   0 mm        (1000) mm        (1000)    66287 2023-03-05 21:45:10.000000 aioconnectors-1.6.1/README.md
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-03-05 21:49:09.326033 aioconnectors-1.6.1/aioconnectors/
--rw-rw-r--   0 mm        (1000) mm        (1000)     1950 2023-03-05 21:47:40.000000 aioconnectors-1.6.1/aioconnectors/__init__.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    12863 2023-03-05 21:21:52.000000 aioconnectors-1.6.1/aioconnectors/__main__.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    65655 2022-11-02 04:38:47.000000 aioconnectors-1.6.1/aioconnectors/api.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    53057 2023-03-05 21:23:45.000000 aioconnectors-1.6.1/aioconnectors/applications.py
--rw-rw-r--   0 mm        (1000) mm        (1000)   100549 2022-09-09 15:58:05.000000 aioconnectors-1.6.1/aioconnectors/connection.py
--rw-rw-r--   0 mm        (1000) mm        (1000)   135021 2022-11-02 04:23:50.000000 aioconnectors-1.6.1/aioconnectors/core.py
--rw-rw-r--   0 mm        (1000) mm        (1000)     5059 2022-09-13 03:55:28.000000 aioconnectors-1.6.1/aioconnectors/helpers.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    33740 2023-03-05 21:29:30.000000 aioconnectors-1.6.1/aioconnectors/ssl_helper.py
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-03-05 21:49:09.326033 aioconnectors-1.6.1/aioconnectors.egg-info/
--rw-rw-r--   0 mm        (1000) mm        (1000)    66939 2023-03-05 21:49:09.000000 aioconnectors-1.6.1/aioconnectors.egg-info/PKG-INFO
--rw-rw-r--   0 mm        (1000) mm        (1000)      380 2023-03-05 21:49:09.000000 aioconnectors-1.6.1/aioconnectors.egg-info/SOURCES.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)        1 2023-03-05 21:49:09.000000 aioconnectors-1.6.1/aioconnectors.egg-info/dependency_links.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)       14 2023-03-05 21:49:09.000000 aioconnectors-1.6.1/aioconnectors.egg-info/top_level.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)       38 2023-03-05 21:49:09.326033 aioconnectors-1.6.1/setup.cfg
--rw-rw-r--   0 mm        (1000) mm        (1000)     6788 2023-03-05 21:47:32.000000 aioconnectors-1.6.1/setup.py
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-05-13 06:05:42.596231 aioconnectors-1.6.2/
+-rw-r--r--   0 mm        (1000) mm        (1000)    11357 2020-06-11 21:16:01.000000 aioconnectors-1.6.2/LICENSE
+-rw-rw-r--   0 mm        (1000) mm        (1000)    67137 2023-05-13 06:05:42.596231 aioconnectors-1.6.2/PKG-INFO
+-rw-rw-r--   0 mm        (1000) mm        (1000)    66485 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/README.md
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-05-13 06:05:42.592231 aioconnectors-1.6.2/aioconnectors/
+-rw-rw-r--   0 mm        (1000) mm        (1000)     1950 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/aioconnectors/__init__.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    13030 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/aioconnectors/__main__.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    65878 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/aioconnectors/api.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    53057 2023-03-05 21:23:45.000000 aioconnectors-1.6.2/aioconnectors/applications.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)   100549 2022-09-09 15:58:05.000000 aioconnectors-1.6.2/aioconnectors/connection.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)   135021 2022-11-02 04:23:50.000000 aioconnectors-1.6.2/aioconnectors/core.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)     5078 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/aioconnectors/helpers.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    33740 2023-03-05 21:29:30.000000 aioconnectors-1.6.2/aioconnectors/ssl_helper.py
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-05-13 06:05:42.592231 aioconnectors-1.6.2/aioconnectors.egg-info/
+-rw-rw-r--   0 mm        (1000) mm        (1000)    67137 2023-05-13 06:05:42.000000 aioconnectors-1.6.2/aioconnectors.egg-info/PKG-INFO
+-rw-rw-r--   0 mm        (1000) mm        (1000)      380 2023-05-13 06:05:42.000000 aioconnectors-1.6.2/aioconnectors.egg-info/SOURCES.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)        1 2023-05-13 06:05:42.000000 aioconnectors-1.6.2/aioconnectors.egg-info/dependency_links.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)       14 2023-05-13 06:05:42.000000 aioconnectors-1.6.2/aioconnectors.egg-info/top_level.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)       38 2023-05-13 06:05:42.596231 aioconnectors-1.6.2/setup.cfg
+-rw-rw-r--   0 mm        (1000) mm        (1000)     6788 2023-05-13 06:03:20.000000 aioconnectors-1.6.2/setup.py
```

### Comparing `aioconnectors-1.6.1/LICENSE` & `aioconnectors-1.6.2/LICENSE`

 * *Files identical despite different names*

### Comparing `aioconnectors-1.6.1/PKG-INFO` & `aioconnectors-1.6.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aioconnectors
-Version: 1.6.1
+Version: 1.6.2
 Summary: Simple secure asynchronous message queue
 Home-page: https://github.com/mori-b/aioconnectors
 Author: Mori Benech
 Author-email: moribirom@gmail.com
 License: UNKNOWN
 Keywords: message queue,broker,asyncio,simple,easy
 Platform: UNKNOWN
@@ -585,15 +585,15 @@
 transport\_json will contain a with\_file key if a file has been received, more details in <a href="#send">5-</a>.  
 -**Note** : if you send a message using send\_message(await\_response=True), the response value is the expected response message : so in that case the response message is not received by the start\_waiting\_for\_messages task.
 
 
 <a name="classes"></a>
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 
-    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>
+    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>,default_logger_bk_count=5
 
 config\_file\_path can be the path of a json file like the following, or instead you can load its items as kwargs, as shown in the basic example later on and in aioconnectors\_test.py  
 You can use both kwargs and config\_file\_path : if there are shared items, the ones from config_file_path will override the kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by default).  
 The main use case for providing a config\_file\_path while having config\_file\_overrides\_kwargs=False is when you prefer to configure your connector only with kwargs but you also want to let the connector update its config file content on the fly (for example blacklisted\_clients\_id, whitelisted\_clients\_id, or ignore\_peer\_traffic).  
 
 Here is an example of config\_file\_path, with ConnectorManager class arguments, used to create a connector
 
@@ -605,14 +605,15 @@
         "certificates_directory_path": "/var/tmp/aioconnectors",
         "client_bind_ip": null,
         "client_cafile_verify_server": null,
         "client_name": null,
         "connect_timeout": 10,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
         "debug_msg_counts": true,
+        "default_logger_bk_count":5,
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "disk_persistence_recv": false,
         "disk_persistence_send": false,
         "enable_client_try_reconnect": true,
         "everybody_can_send_messages": true,
@@ -667,14 +668,15 @@
 Here is an example of config\_file\_path, with ConnectorAPI class arguments, used to send/receive messages.  
 These are a subset of ConnectorManager arguments : which means you can use the ConnectorManager config file also for ConnectorAPI.
 
 
     {
         "client_name": null,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
+        "default_logger_bk_count":5,        
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "is_server": true,
         "max_size_chunk_upload": 209715200,
         "pubsub_central_broker": false,
         "receive_from_any_connector_owner": true,
@@ -698,15 +700,16 @@
 -**certificates\_directory\_path** is where your certificates are located, if use\_ssl is True. This is the <optional\_directory\_path> where you generated your certificates by calling "python3 -m aioconnectors create\_certificates <optional\_directory\_path>".  
 -**client\_cafile\_verify\_server** : On client side, if server\_sockaddr is configured with the server hostname, you can set client\_cafile\_verify\_server to be the ca cert path (like /etc/ssl/certs/ca-certificates.crt), to enable CA verification of you server certificate.  
 -**client\_name** is used on client side. It is the name that will be associated with this client on server side. Auto generated if not supplied in ConnectorManager. Mandatory in ConnectorAPI. It should match the regex \^\[0\-9a\-zA\-Z\-\_\:\]\+$  
 -**client_bind_ip** is optional, specifies the interface to bind your client. You can use an interface name or its ip address (string).  
 -**connect\_timeout** : On client side, the socket timeout to connect to Tsoc. Default is 10s, you might need to increase it when using a server hostname in server\_sockaddr, since sometimes name resolution with getaddrinfo is slow.  
 -**connector\_files\_dirpath** is important, it is the path where all internal files are stored. The default is /var/tmp/aioconnectors. unix sockets files, default log files, and persistent files are stored there.  
 -**debug_msg_counts** is a boolean, enables to display every 2 minutes a count of messages in the log file, and in stdout if **silent** is disabled.  
--**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes. There are 5 backups configured, compressed with gzip.  
+-**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes.  
+-**default\_logger\_bk\_count**  an integer telling the maximum number of gzip compressed logs kept when log rotate is enabled. Default is 5.  
 -**disk\_persistence\_recv** : In order to enable persistence between the connector and a message listener (supported on both client and server sides), use disk\_persistence\_recv=True (applies to all message types). disk\_persistence\_recv can also be a list of message types for which to apply persistence. There will be 1 persistence file per message type.  
 -**file\_recv\_config** : In order to be able to receive files, you must define the destination path of files according to their associated dst\_type. This is done in file\_recv\_config, as shown in aioconnectors\_test.py. file\_recv\_config = {"target\_directory":"", "owner":"", "override\_existing":False}. **target\_directory** is later formatted using the transport\_json fields : which means you can use a target\_directory value like "/my_destination_files/{message\_type}/{source\_id}". **owner** is optional, it is the owner of the uploaded file. It must be of the form "user:group". **override\_existing** is optional and false by default : when receiving a file with an already existing destination path, it decides whether to override the existing file or not.  
 -**enable\_client\_try\_reconnect** is a boolean set to True by default. If enabled, it lets the client try to reconnect automatically to the server every 5 seconds in case of failure.  
 -**keep\_alive\_period** is null by default. If an integer then the client periodically sends a ping keep-alive to the server. If **max\_number\_of\_unanswered\_keep\_alive** (default is 2) keep-alive responses are not received by the client, each after **keep\_alive\_timeout** (default is 5s), then the client disconnects and tries to reconnect with the same mechanism used by enable\_client\_try\_reconnect.  
 -**everybody\_can\_send\_messages** if True lets anyone send messages through the connector, otherwise the sender must have write permission to the connector. Setting to True requires the connector to run as root.  
 -**hook\_allow\_certificate\_creation** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client_name and returning a boolean, to let the server accept or block the client_name certificate creation.  
 -**hook\_server\_auth\_client** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client peername and returning a boolean, to let the server accept or block the client connection. An example exists in the chat implementation in applications.py.
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: aioconnectors Version: 1.6.1 Summary: Simple secure
+Metadata-Version: 2.1 Name: aioconnectors Version: 1.6.2 Summary: Simple secure
 asynchronous message queue Home-page: https://github.com/mori-b/aioconnectors
 Author: Mori Benech Author-email: moribirom@gmail.com License: UNKNOWN
 Keywords: message queue,broker,asyncio,simple,easy Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable Classifier: Intended
 Audience :: Developers Classifier: Topic :: Software Development :: Libraries
 Classifier: License :: OSI Approved :: Apache Software License Classifier:
 Programming Language :: Python :: 3 Requires-Python: >=3.6 Description-Content-
@@ -436,37 +436,38 @@
 destination\_id, and response\_id for example if needed, etc). transport\_json
 will contain a with\_file key if a file has been received, more details in 5-.
 -**Note** : if you send a message using send\_message(await\_response=True),
 the response value is the expected response message : so in that case the
 response message is not received by the start\_waiting\_for\_messages task.
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 logger=None, use_default_logger=True, default_logger_log_level='INFO',
-default_logger_rotate=True, config_file_path= config\_file\_path can be the
-path of a json file like the following, or instead you can load its items as
-kwargs, as shown in the basic example later on and in aioconnectors\_test.py
-You can use both kwargs and config\_file\_path : if there are shared items, the
-ones from config_file_path will override the kwargs, unless you specify
-config\_file\_overrides\_kwargs=False (True by default). The main use case for
-providing a config\_file\_path while having
+default_logger_rotate=True, config_file_path=,default_logger_bk_count=5
+config\_file\_path can be the path of a json file like the following, or
+instead you can load its items as kwargs, as shown in the basic example later
+on and in aioconnectors\_test.py You can use both kwargs and config\_file\_path
+: if there are shared items, the ones from config_file_path will override the
+kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by
+default). The main use case for providing a config\_file\_path while having
 config\_file\_overrides\_kwargs=False is when you prefer to configure your
 connector only with kwargs but you also want to let the connector update its
 config file content on the fly (for example blacklisted\_clients\_id,
 whitelisted\_clients\_id, or ignore\_peer\_traffic). Here is an example of
 config\_file\_path, with ConnectorManager class arguments, used to create a
 connector { "alternate_client_default_cert": false, "blacklisted_clients_id":
 null, "blacklisted_clients_ip": null, "blacklisted_clients_subnet": null,
 "certificates_directory_path": "/var/tmp/aioconnectors", "client_bind_ip":
 null, "client_cafile_verify_server": null, "client_name": null,
 "connect_timeout": 10, "connector_files_dirpath": "/var/tmp/aioconnectors",
-"debug_msg_counts": true, "default_logger_dirpath": "/var/tmp/aioconnectors",
-"default_logger_log_level": "INFO", "default_logger_rotate": true,
-"disk_persistence_recv": false, "disk_persistence_send": false,
-"enable_client_try_reconnect": true, "everybody_can_send_messages": true,
-"file_recv_config": {}, "ignore_peer_traffic": false, "is_server": true,
-"keep_alive_period": null, "keep_alive_timeout": 5, "max_certs": 1024,
+"debug_msg_counts": true, "default_logger_bk_count":5,
+"default_logger_dirpath": "/var/tmp/aioconnectors", "default_logger_log_level":
+"INFO", "default_logger_rotate": true, "disk_persistence_recv": false,
+"disk_persistence_send": false, "enable_client_try_reconnect": true,
+"everybody_can_send_messages": true, "file_recv_config": {},
+"ignore_peer_traffic": false, "is_server": true, "keep_alive_period": null,
+"keep_alive_timeout": 5, "max_certs": 1024,
 "max_number_of_unanswered_keep_alive": 2, "max_size_file_upload_recv":
 8589930194, "max_size_file_upload_send": 8589930194,
 "max_size_persistence_path": 1073741824, "proxy": {}, "pubsub_central_broker":
 false, "recv_message_types": [ "any" ], "reuse_server_sockaddr": false,
 "reuse_uds_path_commander_server": false, "reuse_uds_path_send_to_connector":
 false, "send_message_types": [ "any" ], "send_message_types_priorities": {},
 "send_timeout": 50, "server_ca": false, "server_ca_certs_not_stored": true,
@@ -478,24 +479,24 @@
 aioconnectors", "uds_path_receive_preserve_socket": true,
 "uds_path_send_preserve_socket": true, "use_ssl": true, "use_token": false,
 "whitelisted_clients_id": null, "whitelisted_clients_ip": null,
 "whitelisted_clients_subnet": null } Here is an example of config\_file\_path,
 with ConnectorAPI class arguments, used to send/receive messages. These are a
 subset of ConnectorManager arguments : which means you can use the
 ConnectorManager config file also for ConnectorAPI. { "client_name": null,
-"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_dirpath":
-"/var/tmp/aioconnectors", "default_logger_log_level": "INFO",
-"default_logger_rotate": true, "is_server": true, "max_size_chunk_upload":
-209715200, "pubsub_central_broker": false, "receive_from_any_connector_owner":
-true, "recv_message_types": [ "any" ], "send_message_types": [ "any" ],
-"server_sockaddr": [ "127.0.0.1", 10673 ], "uds_path_receive_preserve_socket":
-true, "uds_path_send_preserve_socket": true } -
-**alternate\_client\_default\_cert** is false by default : if true it lets the
-client try to connect alternatively with the default certificate, in case of
-failure with the private certificate. This can save the hassle of having to
+"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_bk_count":
+5, "default_logger_dirpath": "/var/tmp/aioconnectors",
+"default_logger_log_level": "INFO", "default_logger_rotate": true, "is_server":
+true, "max_size_chunk_upload": 209715200, "pubsub_central_broker": false,
+"receive_from_any_connector_owner": true, "recv_message_types": [ "any" ],
+"send_message_types": [ "any" ], "server_sockaddr": [ "127.0.0.1", 10673 ],
+"uds_path_receive_preserve_socket": true, "uds_path_send_preserve_socket": true
+} -**alternate\_client\_default\_cert** is false by default : if true it lets
+the client try to connect alternatively with the default certificate, in case
+of failure with the private certificate. This can save the hassle of having to
 delete manually your client certificate when the certificate was already
 deleted on server side. This affects also the token authentication : the client
 will try to connect alternatively by requesting a new token if its token fails.
 -**blacklisted\_clients\_id|ip|subnet** : a list of blacklisted clients (regex
 for blacklisted\_clients\_id), can be updated on the fly with the api functions
 add|remove\_blacklist\_client or in the cli. -**certificates\_directory\_path**
 is where your certificates are located, if use\_ssl is True. This is the
@@ -515,15 +516,16 @@
 server\_sockaddr, since sometimes name resolution with getaddrinfo is slow. -
 **connector\_files\_dirpath** is important, it is the path where all internal
 files are stored. The default is /var/tmp/aioconnectors. unix sockets files,
 default log files, and persistent files are stored there. -**debug_msg_counts**
 is a boolean, enables to display every 2 minutes a count of messages in the log
 file, and in stdout if **silent** is disabled. -**default\_logger\_rotate**
 (boolean) can also be an integer telling the maximum size of the log file in
-bytes. There are 5 backups configured, compressed with gzip. -
+bytes. -**default\_logger\_bk\_count** an integer telling the maximum number of
+gzip compressed logs kept when log rotate is enabled. Default is 5. -
 **disk\_persistence\_recv** : In order to enable persistence between the
 connector and a message listener (supported on both client and server sides),
 use disk\_persistence\_recv=True (applies to all message types).
 disk\_persistence\_recv can also be a list of message types for which to apply
 persistence. There will be 1 persistence file per message type. -
 **file\_recv\_config** : In order to be able to receive files, you must define
 the destination path of files according to their associated dst\_type. This is
```

### Comparing `aioconnectors-1.6.1/README.md` & `aioconnectors-1.6.2/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -566,15 +566,15 @@
 transport\_json will contain a with\_file key if a file has been received, more details in <a href="#send">5-</a>.  
 -**Note** : if you send a message using send\_message(await\_response=True), the response value is the expected response message : so in that case the response message is not received by the start\_waiting\_for\_messages task.
 
 
 <a name="classes"></a>
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 
-    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>
+    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>,default_logger_bk_count=5
 
 config\_file\_path can be the path of a json file like the following, or instead you can load its items as kwargs, as shown in the basic example later on and in aioconnectors\_test.py  
 You can use both kwargs and config\_file\_path : if there are shared items, the ones from config_file_path will override the kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by default).  
 The main use case for providing a config\_file\_path while having config\_file\_overrides\_kwargs=False is when you prefer to configure your connector only with kwargs but you also want to let the connector update its config file content on the fly (for example blacklisted\_clients\_id, whitelisted\_clients\_id, or ignore\_peer\_traffic).  
 
 Here is an example of config\_file\_path, with ConnectorManager class arguments, used to create a connector
 
@@ -586,14 +586,15 @@
         "certificates_directory_path": "/var/tmp/aioconnectors",
         "client_bind_ip": null,
         "client_cafile_verify_server": null,
         "client_name": null,
         "connect_timeout": 10,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
         "debug_msg_counts": true,
+        "default_logger_bk_count":5,
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "disk_persistence_recv": false,
         "disk_persistence_send": false,
         "enable_client_try_reconnect": true,
         "everybody_can_send_messages": true,
@@ -648,14 +649,15 @@
 Here is an example of config\_file\_path, with ConnectorAPI class arguments, used to send/receive messages.  
 These are a subset of ConnectorManager arguments : which means you can use the ConnectorManager config file also for ConnectorAPI.
 
 
     {
         "client_name": null,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
+        "default_logger_bk_count":5,        
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "is_server": true,
         "max_size_chunk_upload": 209715200,
         "pubsub_central_broker": false,
         "receive_from_any_connector_owner": true,
@@ -679,15 +681,16 @@
 -**certificates\_directory\_path** is where your certificates are located, if use\_ssl is True. This is the <optional\_directory\_path> where you generated your certificates by calling "python3 -m aioconnectors create\_certificates <optional\_directory\_path>".  
 -**client\_cafile\_verify\_server** : On client side, if server\_sockaddr is configured with the server hostname, you can set client\_cafile\_verify\_server to be the ca cert path (like /etc/ssl/certs/ca-certificates.crt), to enable CA verification of you server certificate.  
 -**client\_name** is used on client side. It is the name that will be associated with this client on server side. Auto generated if not supplied in ConnectorManager. Mandatory in ConnectorAPI. It should match the regex \^\[0\-9a\-zA\-Z\-\_\:\]\+$  
 -**client_bind_ip** is optional, specifies the interface to bind your client. You can use an interface name or its ip address (string).  
 -**connect\_timeout** : On client side, the socket timeout to connect to Tsoc. Default is 10s, you might need to increase it when using a server hostname in server\_sockaddr, since sometimes name resolution with getaddrinfo is slow.  
 -**connector\_files\_dirpath** is important, it is the path where all internal files are stored. The default is /var/tmp/aioconnectors. unix sockets files, default log files, and persistent files are stored there.  
 -**debug_msg_counts** is a boolean, enables to display every 2 minutes a count of messages in the log file, and in stdout if **silent** is disabled.  
--**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes. There are 5 backups configured, compressed with gzip.  
+-**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes.  
+-**default\_logger\_bk\_count**  an integer telling the maximum number of gzip compressed logs kept when log rotate is enabled. Default is 5.  
 -**disk\_persistence\_recv** : In order to enable persistence between the connector and a message listener (supported on both client and server sides), use disk\_persistence\_recv=True (applies to all message types). disk\_persistence\_recv can also be a list of message types for which to apply persistence. There will be 1 persistence file per message type.  
 -**file\_recv\_config** : In order to be able to receive files, you must define the destination path of files according to their associated dst\_type. This is done in file\_recv\_config, as shown in aioconnectors\_test.py. file\_recv\_config = {"target\_directory":"", "owner":"", "override\_existing":False}. **target\_directory** is later formatted using the transport\_json fields : which means you can use a target\_directory value like "/my_destination_files/{message\_type}/{source\_id}". **owner** is optional, it is the owner of the uploaded file. It must be of the form "user:group". **override\_existing** is optional and false by default : when receiving a file with an already existing destination path, it decides whether to override the existing file or not.  
 -**enable\_client\_try\_reconnect** is a boolean set to True by default. If enabled, it lets the client try to reconnect automatically to the server every 5 seconds in case of failure.  
 -**keep\_alive\_period** is null by default. If an integer then the client periodically sends a ping keep-alive to the server. If **max\_number\_of\_unanswered\_keep\_alive** (default is 2) keep-alive responses are not received by the client, each after **keep\_alive\_timeout** (default is 5s), then the client disconnects and tries to reconnect with the same mechanism used by enable\_client\_try\_reconnect.  
 -**everybody\_can\_send\_messages** if True lets anyone send messages through the connector, otherwise the sender must have write permission to the connector. Setting to True requires the connector to run as root.  
 -**hook\_allow\_certificate\_creation** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client_name and returning a boolean, to let the server accept or block the client_name certificate creation.  
 -**hook\_server\_auth\_client** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client peername and returning a boolean, to let the server accept or block the client connection. An example exists in the chat implementation in applications.py.
```

#### html2text {}

```diff
@@ -428,37 +428,38 @@
 destination\_id, and response\_id for example if needed, etc). transport\_json
 will contain a with\_file key if a file has been received, more details in 5-.
 -**Note** : if you send a message using send\_message(await\_response=True),
 the response value is the expected response message : so in that case the
 response message is not received by the start\_waiting\_for\_messages task.
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 logger=None, use_default_logger=True, default_logger_log_level='INFO',
-default_logger_rotate=True, config_file_path= config\_file\_path can be the
-path of a json file like the following, or instead you can load its items as
-kwargs, as shown in the basic example later on and in aioconnectors\_test.py
-You can use both kwargs and config\_file\_path : if there are shared items, the
-ones from config_file_path will override the kwargs, unless you specify
-config\_file\_overrides\_kwargs=False (True by default). The main use case for
-providing a config\_file\_path while having
+default_logger_rotate=True, config_file_path=,default_logger_bk_count=5
+config\_file\_path can be the path of a json file like the following, or
+instead you can load its items as kwargs, as shown in the basic example later
+on and in aioconnectors\_test.py You can use both kwargs and config\_file\_path
+: if there are shared items, the ones from config_file_path will override the
+kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by
+default). The main use case for providing a config\_file\_path while having
 config\_file\_overrides\_kwargs=False is when you prefer to configure your
 connector only with kwargs but you also want to let the connector update its
 config file content on the fly (for example blacklisted\_clients\_id,
 whitelisted\_clients\_id, or ignore\_peer\_traffic). Here is an example of
 config\_file\_path, with ConnectorManager class arguments, used to create a
 connector { "alternate_client_default_cert": false, "blacklisted_clients_id":
 null, "blacklisted_clients_ip": null, "blacklisted_clients_subnet": null,
 "certificates_directory_path": "/var/tmp/aioconnectors", "client_bind_ip":
 null, "client_cafile_verify_server": null, "client_name": null,
 "connect_timeout": 10, "connector_files_dirpath": "/var/tmp/aioconnectors",
-"debug_msg_counts": true, "default_logger_dirpath": "/var/tmp/aioconnectors",
-"default_logger_log_level": "INFO", "default_logger_rotate": true,
-"disk_persistence_recv": false, "disk_persistence_send": false,
-"enable_client_try_reconnect": true, "everybody_can_send_messages": true,
-"file_recv_config": {}, "ignore_peer_traffic": false, "is_server": true,
-"keep_alive_period": null, "keep_alive_timeout": 5, "max_certs": 1024,
+"debug_msg_counts": true, "default_logger_bk_count":5,
+"default_logger_dirpath": "/var/tmp/aioconnectors", "default_logger_log_level":
+"INFO", "default_logger_rotate": true, "disk_persistence_recv": false,
+"disk_persistence_send": false, "enable_client_try_reconnect": true,
+"everybody_can_send_messages": true, "file_recv_config": {},
+"ignore_peer_traffic": false, "is_server": true, "keep_alive_period": null,
+"keep_alive_timeout": 5, "max_certs": 1024,
 "max_number_of_unanswered_keep_alive": 2, "max_size_file_upload_recv":
 8589930194, "max_size_file_upload_send": 8589930194,
 "max_size_persistence_path": 1073741824, "proxy": {}, "pubsub_central_broker":
 false, "recv_message_types": [ "any" ], "reuse_server_sockaddr": false,
 "reuse_uds_path_commander_server": false, "reuse_uds_path_send_to_connector":
 false, "send_message_types": [ "any" ], "send_message_types_priorities": {},
 "send_timeout": 50, "server_ca": false, "server_ca_certs_not_stored": true,
@@ -470,24 +471,24 @@
 aioconnectors", "uds_path_receive_preserve_socket": true,
 "uds_path_send_preserve_socket": true, "use_ssl": true, "use_token": false,
 "whitelisted_clients_id": null, "whitelisted_clients_ip": null,
 "whitelisted_clients_subnet": null } Here is an example of config\_file\_path,
 with ConnectorAPI class arguments, used to send/receive messages. These are a
 subset of ConnectorManager arguments : which means you can use the
 ConnectorManager config file also for ConnectorAPI. { "client_name": null,
-"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_dirpath":
-"/var/tmp/aioconnectors", "default_logger_log_level": "INFO",
-"default_logger_rotate": true, "is_server": true, "max_size_chunk_upload":
-209715200, "pubsub_central_broker": false, "receive_from_any_connector_owner":
-true, "recv_message_types": [ "any" ], "send_message_types": [ "any" ],
-"server_sockaddr": [ "127.0.0.1", 10673 ], "uds_path_receive_preserve_socket":
-true, "uds_path_send_preserve_socket": true } -
-**alternate\_client\_default\_cert** is false by default : if true it lets the
-client try to connect alternatively with the default certificate, in case of
-failure with the private certificate. This can save the hassle of having to
+"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_bk_count":
+5, "default_logger_dirpath": "/var/tmp/aioconnectors",
+"default_logger_log_level": "INFO", "default_logger_rotate": true, "is_server":
+true, "max_size_chunk_upload": 209715200, "pubsub_central_broker": false,
+"receive_from_any_connector_owner": true, "recv_message_types": [ "any" ],
+"send_message_types": [ "any" ], "server_sockaddr": [ "127.0.0.1", 10673 ],
+"uds_path_receive_preserve_socket": true, "uds_path_send_preserve_socket": true
+} -**alternate\_client\_default\_cert** is false by default : if true it lets
+the client try to connect alternatively with the default certificate, in case
+of failure with the private certificate. This can save the hassle of having to
 delete manually your client certificate when the certificate was already
 deleted on server side. This affects also the token authentication : the client
 will try to connect alternatively by requesting a new token if its token fails.
 -**blacklisted\_clients\_id|ip|subnet** : a list of blacklisted clients (regex
 for blacklisted\_clients\_id), can be updated on the fly with the api functions
 add|remove\_blacklist\_client or in the cli. -**certificates\_directory\_path**
 is where your certificates are located, if use\_ssl is True. This is the
@@ -507,15 +508,16 @@
 server\_sockaddr, since sometimes name resolution with getaddrinfo is slow. -
 **connector\_files\_dirpath** is important, it is the path where all internal
 files are stored. The default is /var/tmp/aioconnectors. unix sockets files,
 default log files, and persistent files are stored there. -**debug_msg_counts**
 is a boolean, enables to display every 2 minutes a count of messages in the log
 file, and in stdout if **silent** is disabled. -**default\_logger\_rotate**
 (boolean) can also be an integer telling the maximum size of the log file in
-bytes. There are 5 backups configured, compressed with gzip. -
+bytes. -**default\_logger\_bk\_count** an integer telling the maximum number of
+gzip compressed logs kept when log rotate is enabled. Default is 5. -
 **disk\_persistence\_recv** : In order to enable persistence between the
 connector and a message listener (supported on both client and server sides),
 use disk\_persistence\_recv=True (applies to all message types).
 disk\_persistence\_recv can also be a list of message types for which to apply
 persistence. There will be 1 persistence file per message type. -
 **file\_recv\_config** : In order to be able to receive files, you must define
 the destination path of files according to their associated dst\_type. This is
```

### Comparing `aioconnectors-1.6.1/aioconnectors/__init__.py` & `aioconnectors-1.6.2/aioconnectors/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -27,14 +27,14 @@
 - Embeds a command line interface, which can manage the broker through the command line
 - Embeds an encrypted chat/file transfer tool easily callable through the command line
 
 The command line tool can be called by "python3 -m aioconnectors --help"
 Usage examples can be found in applications.py
 '''
 
-__version__ = '1.6.1'
+__version__ = '1.6.2'
 __author__ = 'Mori Benech'
 
 from .api import ConnectorManager, ConnectorAPI, ConnectorRemoteTool
 from .connection import MessageFields
 from .helpers import get_logger, iface_to_ip, get_tmp_dir
 from . import applications
```

### Comparing `aioconnectors-1.6.1/aioconnectors/__main__.py` & `aioconnectors-1.6.2/aioconnectors/__main__.py`

 * *Files 2% similar despite different names*

```diff
@@ -81,14 +81,15 @@
             sys.exit(1)
         
     elif sys.argv[1] == 'print_config_templates':
         Connector = aioconnectors.core.Connector
     
         manager_config_template = dict(default_logger_log_level='INFO', default_logger_rotate=True,
                         default_logger_dirpath=Connector.CONNECTOR_FILES_DIRPATH, 
+                        default_logger_bk_count=aioconnectors.helpers.LOG_BK_COUNT,
                         connector_files_dirpath=Connector.CONNECTOR_FILES_DIRPATH,
                         is_server=True, server_sockaddr=Connector.SERVER_ADDR, reuse_server_sockaddr=False,
                         reuse_uds_path_commander_server=False, reuse_uds_path_send_to_connector=False,
                         use_ssl=Connector.USE_SSL, ssl_allow_all=False, use_token=Connector.USE_TOKEN,
                         server_ca=Connector.SERVER_CA, server_ca_certs_not_stored=True, server_secure_tls=True,
                         certificates_directory_path=Connector.CONNECTOR_FILES_DIRPATH,
                         tokens_directory_path=Connector.CONNECTOR_FILES_DIRPATH,                        
@@ -121,15 +122,16 @@
         print(json.dumps(manager_config_template, indent=4, sort_keys=True))
         file_recv_config = {'any': {'target_directory':'/var/tmp/aioconnectors/{message_type}/{source_id}/',
                                     'owner':'user:user', 'override_existing':False}}
         print('\n- file_recv_config example, used inside MANAGER TEMPLATE')
         print(json.dumps(file_recv_config, indent=4, sort_keys=True))                
         
         api_config_template = dict(default_logger_log_level='INFO', default_logger_rotate=True,
-                        default_logger_dirpath=Connector.CONNECTOR_FILES_DIRPATH, 
+                        default_logger_dirpath=Connector.CONNECTOR_FILES_DIRPATH,
+                        default_logger_bk_count=aioconnectors.helpers.LOG_BK_COUNT,
                         connector_files_dirpath=Connector.CONNECTOR_FILES_DIRPATH, 
                         is_server=True, server_sockaddr=Connector.SERVER_ADDR, client_name=None,
                         uds_path_receive_preserve_socket=Connector.UDS_PATH_RECEIVE_PRESERVE_SOCKET, 
                         uds_path_send_preserve_socket=Connector.UDS_PATH_SEND_PRESERVE_SOCKET,
                         send_message_types=Connector.DEFAULT_MESSAGE_TYPES, 
                         recv_message_types=Connector.DEFAULT_MESSAGE_TYPES,
                         receive_from_any_connector_owner=True, pubsub_central_broker=False,
```

### Comparing `aioconnectors-1.6.1/aioconnectors/api.py` & `aioconnectors-1.6.2/aioconnectors/api.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,22 +5,20 @@
 import uuid
 import ipaddress
 
 from .helpers import get_logger, chown_nobody_permissions, PYTHON_GREATER_37
 from .core import Connector
 from .connection import Structures, MessageFields, Misc
 
-DEFAULT_LOGGER_NAME = 'aioconnectors'
-LOGFILE_DEFAULT_NAME = 'aioconnectors.log'
-DEFAULT_LOGGER_LOG_LEVEL = 'INFO'
-DEFAULT_LOGGER_ROTATE = True
+from .helpers import DEFAULT_LOGGER_NAME, LOGFILE_DEFAULT_NAME, LOG_LEVEL, LOG_ROTATE, LOG_BK_COUNT
 
 class ConnectorManager:
     def __init__(self, config_file_path=None, config_file_overrides_kwargs=True, logger=None, use_default_logger=True, 
-                 default_logger_log_level=DEFAULT_LOGGER_LOG_LEVEL, default_logger_rotate=True,
+                 default_logger_log_level=LOG_LEVEL, default_logger_rotate=LOG_ROTATE,
+                 default_logger_bk_count=LOG_BK_COUNT,
                  default_logger_dirpath=Connector.CONNECTOR_FILES_DIRPATH, use_token=Connector.USE_TOKEN,
                  is_server=True, server_sockaddr=None, use_ssl=Connector.USE_SSL, ssl_allow_all=Connector.SSL_ALLOW_ALL, 
                  server_ca=Connector.SERVER_CA, server_ca_certs_not_stored=True, server_secure_tls=True,
                  client_bind_ip=None, certificates_directory_path=Connector.CONNECTOR_FILES_DIRPATH,
                  tokens_directory_path=Connector.CONNECTOR_FILES_DIRPATH, client_name=None, 
                  send_message_types=None, recv_message_types=None, subscribe_message_types=None,
                  connector_files_dirpath=Connector.CONNECTOR_FILES_DIRPATH,
@@ -47,24 +45,25 @@
                  token_client_verify_server_hostname=Connector.TOKEN_CLIENT_VERIFY_SERVER_HOSTNAME,
                  token_server_allow_authorized_non_default_cert=False, **kwargs):
         
         self.connector_files_dirpath = connector_files_dirpath
         self.default_logger_dirpath = default_logger_dirpath
         self.default_logger_log_level = default_logger_log_level
         self.default_logger_rotate = default_logger_rotate
+        self.default_logger_bk_count = default_logger_bk_count
         if not os.path.isdir(self.connector_files_dirpath):
             os.makedirs(self.connector_files_dirpath)
         if not os.path.isdir(self.default_logger_dirpath):
             os.makedirs(self.default_logger_dirpath)
                 
         if not logger:
             if use_default_logger:
                 self.logger = get_logger(logfile_path=os.path.join(self.default_logger_dirpath, LOGFILE_DEFAULT_NAME), 
                                          logger_name=DEFAULT_LOGGER_NAME, silent=True, level=default_logger_log_level,
-                                         rotate=default_logger_rotate)
+                                         rotate=default_logger_rotate, bk_count=default_logger_bk_count)
             else:
                 self.logger = get_logger(logfile_path=None)  #dummy logger
         else:
             self.logger = logger
             
         self.is_server, self.server_sockaddr, self.use_ssl, self.ssl_allow_all, self.certificates_directory_path, self.server_ca = \
                             is_server, server_sockaddr, use_ssl, ssl_allow_all, certificates_directory_path, server_ca
@@ -127,15 +126,15 @@
                         for key,val in config_json.items():                            
                             setattr(self, key, val)
                     #update logger according to config
                     if not logger and use_default_logger:
                         self.logger = get_logger(logfile_path=os.path.join(self.default_logger_dirpath,
                                                  LOGFILE_DEFAULT_NAME), logger_name=DEFAULT_LOGGER_NAME, 
                                                  silent=self.silent, level=self.default_logger_log_level,
-                                                 rotate=self.default_logger_rotate)                            
+                                                 rotate=self.default_logger_rotate, bk_count=self.default_logger_bk_count)                            
                 except Exception:
                     self.logger.exception('ConnectorManager init config_file_path')
             else:
                 self.logger.warning('ConnectorManager init could not find config file at path '+self.config_file_path)
 
         if self.server_sockaddr:
             self.server_sockaddr = tuple(self.server_sockaddr)
@@ -378,16 +377,16 @@
         return self.connector.show_log_level()
 
     def set_log_level(self, level):
         self.logger.info(f'{self.source_id} set_log_level') 
         return self.connector.set_log_level(level)       
 
 class ConnectorBaseTool:
-    def __init__(self, config_file_path=None, logger=None, use_default_logger=True, default_logger_rotate=DEFAULT_LOGGER_ROTATE,
-                 default_logger_log_level=DEFAULT_LOGGER_LOG_LEVEL,
+    def __init__(self, config_file_path=None, logger=None, use_default_logger=True, default_logger_rotate=LOG_ROTATE,
+                 default_logger_log_level=LOG_LEVEL, default_logger_bk_count=LOG_BK_COUNT,
                  default_logger_dirpath=Connector.CONNECTOR_FILES_DIRPATH, connector_files_dirpath=Connector.CONNECTOR_FILES_DIRPATH, 
                  is_server=False, server_sockaddr=None, client_name=None, 
                  uds_path_receive_preserve_socket=Connector.UDS_PATH_RECEIVE_PRESERVE_SOCKET,
                  uds_path_send_preserve_socket=Connector.UDS_PATH_SEND_PRESERVE_SOCKET,
                  send_message_types=None, recv_message_types=None, pubsub_central_broker=False):
 
         self.connector_files_dirpath = connector_files_dirpath
@@ -395,15 +394,15 @@
         if not os.path.isdir(self.connector_files_dirpath):
             os.makedirs(self.connector_files_dirpath)
     
         if not logger:
             if use_default_logger:
                 self.logger = get_logger(logfile_path=os.path.join(self.default_logger_dirpath, LOGFILE_DEFAULT_NAME), 
                                          logger_name=DEFAULT_LOGGER_NAME, silent=True, level=default_logger_log_level,
-                                         rotate=default_logger_rotate)                
+                                         rotate=default_logger_rotate, bk_count=default_logger_bk_count)                
             else:
                 self.logger = get_logger(logfile_path=None)  #dummy logger
         else:
             self.logger = logger
         self.is_server, self.server_sockaddr, self.client_name = is_server, server_sockaddr, client_name
         self.send_message_types, self.recv_message_types = send_message_types, recv_message_types
         self.pubsub_central_broker = pubsub_central_broker
@@ -421,15 +420,15 @@
                         for key,val in config_json.items():                            
                             setattr(self, key, val)
                     #update logger according to config
                     if not logger and use_default_logger:
                         self.logger = get_logger(logfile_path=os.path.join(self.default_logger_dirpath,
                                                  LOGFILE_DEFAULT_NAME), logger_name=DEFAULT_LOGGER_NAME, 
                                                  silent=self.silent, level=self.default_logger_log_level,
-                                                 rotate=self.default_logger_rotate)                                                        
+                                                 rotate=self.default_logger_rotate, bk_count=self.default_logger_bk_count)                                                        
                 except Exception:
                     self.logger.exception('type(self).__name__ init config_file_path')
             else:
                 self.logger.warning('type(self).__name__ init could not find config file at path '+self.config_file_path)
         else:
             self.config_file_path = config_file_path
```

### Comparing `aioconnectors-1.6.1/aioconnectors/applications.py` & `aioconnectors-1.6.2/aioconnectors/applications.py`

 * *Files identical despite different names*

### Comparing `aioconnectors-1.6.1/aioconnectors/connection.py` & `aioconnectors-1.6.2/aioconnectors/connection.py`

 * *Files identical despite different names*

### Comparing `aioconnectors-1.6.1/aioconnectors/core.py` & `aioconnectors-1.6.2/aioconnectors/core.py`

 * *Files identical despite different names*

### Comparing `aioconnectors-1.6.1/aioconnectors/helpers.py` & `aioconnectors-1.6.2/aioconnectors/helpers.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 PYTHON_VERSION = (sys.version_info.major,sys.version_info.minor)
 if PYTHON_VERSION < (3,6):
     print('aioconnectors minimum requirement : Python 3.6')
     sys.exit(1)
 PYTHON_GREATER_37 = (PYTHON_VERSION >= (3,7))
 
 DEFAULT_LOGGER_NAME = 'aioconnector'
-LOGFILE_DEFAULT_PATH = 'aioconnectors.log'
+LOGFILE_DEFAULT_NAME = 'aioconnectors.log'
 LOG_LEVEL = 'INFO'
 LOG_ROTATE = True
 LOG_FORMAT = '%(asctime)s - %(name)s - %(levelname)s - %(message)s'
 LOG_FORMAT_SHORT = '%(asctime)s - %(levelname)s - %(message)s'
 LOG_BK_COUNT = 5
 LOG_MAX_SIZE = 67108864 # 2**26 = 64 MB
 
@@ -37,16 +37,16 @@
     if os.path.exists('/var/tmp'):
         return '/var/tmp/aioconnectors'
     else:
         candidate1 = full_path('~/aioconnectors_tmp')
         candidate2 = full_path('aioconnectors_tmp')
         return min(candidate1, candidate2, key=lambda x:len(x))
 
-def get_logger(logfile_path=LOGFILE_DEFAULT_PATH, first_run=False, silent=True, logger_name=DEFAULT_LOGGER_NAME, 
-               log_format=LOG_FORMAT, level=LOG_LEVEL, rotate=LOG_ROTATE):
+def get_logger(logfile_path=LOGFILE_DEFAULT_NAME, first_run=False, silent=True, logger_name=DEFAULT_LOGGER_NAME, 
+               log_format=LOG_FORMAT, level=LOG_LEVEL, rotate=LOG_ROTATE, bk_count=LOG_BK_COUNT):
     
     def namer(name):
         return name + '.gz'
     
     def rotator(source, dest):
         with open(source, 'rb') as sf:
             data = sf.read()
@@ -65,15 +65,15 @@
                     rotate = LOG_MAX_SIZE
                 else:
                     #use user defined value                    
                     try:
                         rotate = int(rotate)
                     except Exception:
                         rotate = LOG_MAX_SIZE
-                fh = RotatingFileHandler(logfile_path, maxBytes=rotate, backupCount=LOG_BK_COUNT)
+                fh = RotatingFileHandler(logfile_path, maxBytes=rotate, backupCount=bk_count)
                 fh.rotator = rotator
                 fh.namer = namer                
                 handlers.append(fh)
             else:
                 handlers.append(logging.FileHandler(logfile_path))
         if not silent:
             handlers.append(logging.StreamHandler(sys.stdout))
```

### Comparing `aioconnectors-1.6.1/aioconnectors/ssl_helper.py` & `aioconnectors-1.6.2/aioconnectors/ssl_helper.py`

 * *Files identical despite different names*

### Comparing `aioconnectors-1.6.1/aioconnectors.egg-info/PKG-INFO` & `aioconnectors-1.6.2/aioconnectors.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aioconnectors
-Version: 1.6.1
+Version: 1.6.2
 Summary: Simple secure asynchronous message queue
 Home-page: https://github.com/mori-b/aioconnectors
 Author: Mori Benech
 Author-email: moribirom@gmail.com
 License: UNKNOWN
 Keywords: message queue,broker,asyncio,simple,easy
 Platform: UNKNOWN
@@ -585,15 +585,15 @@
 transport\_json will contain a with\_file key if a file has been received, more details in <a href="#send">5-</a>.  
 -**Note** : if you send a message using send\_message(await\_response=True), the response value is the expected response message : so in that case the response message is not received by the start\_waiting\_for\_messages task.
 
 
 <a name="classes"></a>
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 
-    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>
+    logger=None, use_default_logger=True, default_logger_log_level='INFO', default_logger_rotate=True, config_file_path=<path>,default_logger_bk_count=5
 
 config\_file\_path can be the path of a json file like the following, or instead you can load its items as kwargs, as shown in the basic example later on and in aioconnectors\_test.py  
 You can use both kwargs and config\_file\_path : if there are shared items, the ones from config_file_path will override the kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by default).  
 The main use case for providing a config\_file\_path while having config\_file\_overrides\_kwargs=False is when you prefer to configure your connector only with kwargs but you also want to let the connector update its config file content on the fly (for example blacklisted\_clients\_id, whitelisted\_clients\_id, or ignore\_peer\_traffic).  
 
 Here is an example of config\_file\_path, with ConnectorManager class arguments, used to create a connector
 
@@ -605,14 +605,15 @@
         "certificates_directory_path": "/var/tmp/aioconnectors",
         "client_bind_ip": null,
         "client_cafile_verify_server": null,
         "client_name": null,
         "connect_timeout": 10,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
         "debug_msg_counts": true,
+        "default_logger_bk_count":5,
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "disk_persistence_recv": false,
         "disk_persistence_send": false,
         "enable_client_try_reconnect": true,
         "everybody_can_send_messages": true,
@@ -667,14 +668,15 @@
 Here is an example of config\_file\_path, with ConnectorAPI class arguments, used to send/receive messages.  
 These are a subset of ConnectorManager arguments : which means you can use the ConnectorManager config file also for ConnectorAPI.
 
 
     {
         "client_name": null,
         "connector_files_dirpath": "/var/tmp/aioconnectors",
+        "default_logger_bk_count":5,        
         "default_logger_dirpath": "/var/tmp/aioconnectors",
         "default_logger_log_level": "INFO",
         "default_logger_rotate": true,
         "is_server": true,
         "max_size_chunk_upload": 209715200,
         "pubsub_central_broker": false,
         "receive_from_any_connector_owner": true,
@@ -698,15 +700,16 @@
 -**certificates\_directory\_path** is where your certificates are located, if use\_ssl is True. This is the <optional\_directory\_path> where you generated your certificates by calling "python3 -m aioconnectors create\_certificates <optional\_directory\_path>".  
 -**client\_cafile\_verify\_server** : On client side, if server\_sockaddr is configured with the server hostname, you can set client\_cafile\_verify\_server to be the ca cert path (like /etc/ssl/certs/ca-certificates.crt), to enable CA verification of you server certificate.  
 -**client\_name** is used on client side. It is the name that will be associated with this client on server side. Auto generated if not supplied in ConnectorManager. Mandatory in ConnectorAPI. It should match the regex \^\[0\-9a\-zA\-Z\-\_\:\]\+$  
 -**client_bind_ip** is optional, specifies the interface to bind your client. You can use an interface name or its ip address (string).  
 -**connect\_timeout** : On client side, the socket timeout to connect to Tsoc. Default is 10s, you might need to increase it when using a server hostname in server\_sockaddr, since sometimes name resolution with getaddrinfo is slow.  
 -**connector\_files\_dirpath** is important, it is the path where all internal files are stored. The default is /var/tmp/aioconnectors. unix sockets files, default log files, and persistent files are stored there.  
 -**debug_msg_counts** is a boolean, enables to display every 2 minutes a count of messages in the log file, and in stdout if **silent** is disabled.  
--**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes. There are 5 backups configured, compressed with gzip.  
+-**default\_logger\_rotate** (boolean) can also be an integer telling the maximum size of the log file in bytes.  
+-**default\_logger\_bk\_count**  an integer telling the maximum number of gzip compressed logs kept when log rotate is enabled. Default is 5.  
 -**disk\_persistence\_recv** : In order to enable persistence between the connector and a message listener (supported on both client and server sides), use disk\_persistence\_recv=True (applies to all message types). disk\_persistence\_recv can also be a list of message types for which to apply persistence. There will be 1 persistence file per message type.  
 -**file\_recv\_config** : In order to be able to receive files, you must define the destination path of files according to their associated dst\_type. This is done in file\_recv\_config, as shown in aioconnectors\_test.py. file\_recv\_config = {"target\_directory":"", "owner":"", "override\_existing":False}. **target\_directory** is later formatted using the transport\_json fields : which means you can use a target\_directory value like "/my_destination_files/{message\_type}/{source\_id}". **owner** is optional, it is the owner of the uploaded file. It must be of the form "user:group". **override\_existing** is optional and false by default : when receiving a file with an already existing destination path, it decides whether to override the existing file or not.  
 -**enable\_client\_try\_reconnect** is a boolean set to True by default. If enabled, it lets the client try to reconnect automatically to the server every 5 seconds in case of failure.  
 -**keep\_alive\_period** is null by default. If an integer then the client periodically sends a ping keep-alive to the server. If **max\_number\_of\_unanswered\_keep\_alive** (default is 2) keep-alive responses are not received by the client, each after **keep\_alive\_timeout** (default is 5s), then the client disconnects and tries to reconnect with the same mechanism used by enable\_client\_try\_reconnect.  
 -**everybody\_can\_send\_messages** if True lets anyone send messages through the connector, otherwise the sender must have write permission to the connector. Setting to True requires the connector to run as root.  
 -**hook\_allow\_certificate\_creation** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client_name and returning a boolean, to let the server accept or block the client_name certificate creation.  
 -**hook\_server\_auth\_client** : does not appear in the config file (usable as a kwargs only). Only for server. Can be an async def coroutine receiving a client peername and returning a boolean, to let the server accept or block the client connection. An example exists in the chat implementation in applications.py.
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: aioconnectors Version: 1.6.1 Summary: Simple secure
+Metadata-Version: 2.1 Name: aioconnectors Version: 1.6.2 Summary: Simple secure
 asynchronous message queue Home-page: https://github.com/mori-b/aioconnectors
 Author: Mori Benech Author-email: moribirom@gmail.com License: UNKNOWN
 Keywords: message queue,broker,asyncio,simple,easy Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable Classifier: Intended
 Audience :: Developers Classifier: Topic :: Software Development :: Libraries
 Classifier: License :: OSI Approved :: Apache Software License Classifier:
 Programming Language :: Python :: 3 Requires-Python: >=3.6 Description-Content-
@@ -436,37 +436,38 @@
 destination\_id, and response\_id for example if needed, etc). transport\_json
 will contain a with\_file key if a file has been received, more details in 5-.
 -**Note** : if you send a message using send\_message(await\_response=True),
 the response value is the expected response message : so in that case the
 response message is not received by the start\_waiting\_for\_messages task.
 ### 4.More details about the ConnectorManager and ConnectorAPI arguments.
 logger=None, use_default_logger=True, default_logger_log_level='INFO',
-default_logger_rotate=True, config_file_path= config\_file\_path can be the
-path of a json file like the following, or instead you can load its items as
-kwargs, as shown in the basic example later on and in aioconnectors\_test.py
-You can use both kwargs and config\_file\_path : if there are shared items, the
-ones from config_file_path will override the kwargs, unless you specify
-config\_file\_overrides\_kwargs=False (True by default). The main use case for
-providing a config\_file\_path while having
+default_logger_rotate=True, config_file_path=,default_logger_bk_count=5
+config\_file\_path can be the path of a json file like the following, or
+instead you can load its items as kwargs, as shown in the basic example later
+on and in aioconnectors\_test.py You can use both kwargs and config\_file\_path
+: if there are shared items, the ones from config_file_path will override the
+kwargs, unless you specify config\_file\_overrides\_kwargs=False (True by
+default). The main use case for providing a config\_file\_path while having
 config\_file\_overrides\_kwargs=False is when you prefer to configure your
 connector only with kwargs but you also want to let the connector update its
 config file content on the fly (for example blacklisted\_clients\_id,
 whitelisted\_clients\_id, or ignore\_peer\_traffic). Here is an example of
 config\_file\_path, with ConnectorManager class arguments, used to create a
 connector { "alternate_client_default_cert": false, "blacklisted_clients_id":
 null, "blacklisted_clients_ip": null, "blacklisted_clients_subnet": null,
 "certificates_directory_path": "/var/tmp/aioconnectors", "client_bind_ip":
 null, "client_cafile_verify_server": null, "client_name": null,
 "connect_timeout": 10, "connector_files_dirpath": "/var/tmp/aioconnectors",
-"debug_msg_counts": true, "default_logger_dirpath": "/var/tmp/aioconnectors",
-"default_logger_log_level": "INFO", "default_logger_rotate": true,
-"disk_persistence_recv": false, "disk_persistence_send": false,
-"enable_client_try_reconnect": true, "everybody_can_send_messages": true,
-"file_recv_config": {}, "ignore_peer_traffic": false, "is_server": true,
-"keep_alive_period": null, "keep_alive_timeout": 5, "max_certs": 1024,
+"debug_msg_counts": true, "default_logger_bk_count":5,
+"default_logger_dirpath": "/var/tmp/aioconnectors", "default_logger_log_level":
+"INFO", "default_logger_rotate": true, "disk_persistence_recv": false,
+"disk_persistence_send": false, "enable_client_try_reconnect": true,
+"everybody_can_send_messages": true, "file_recv_config": {},
+"ignore_peer_traffic": false, "is_server": true, "keep_alive_period": null,
+"keep_alive_timeout": 5, "max_certs": 1024,
 "max_number_of_unanswered_keep_alive": 2, "max_size_file_upload_recv":
 8589930194, "max_size_file_upload_send": 8589930194,
 "max_size_persistence_path": 1073741824, "proxy": {}, "pubsub_central_broker":
 false, "recv_message_types": [ "any" ], "reuse_server_sockaddr": false,
 "reuse_uds_path_commander_server": false, "reuse_uds_path_send_to_connector":
 false, "send_message_types": [ "any" ], "send_message_types_priorities": {},
 "send_timeout": 50, "server_ca": false, "server_ca_certs_not_stored": true,
@@ -478,24 +479,24 @@
 aioconnectors", "uds_path_receive_preserve_socket": true,
 "uds_path_send_preserve_socket": true, "use_ssl": true, "use_token": false,
 "whitelisted_clients_id": null, "whitelisted_clients_ip": null,
 "whitelisted_clients_subnet": null } Here is an example of config\_file\_path,
 with ConnectorAPI class arguments, used to send/receive messages. These are a
 subset of ConnectorManager arguments : which means you can use the
 ConnectorManager config file also for ConnectorAPI. { "client_name": null,
-"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_dirpath":
-"/var/tmp/aioconnectors", "default_logger_log_level": "INFO",
-"default_logger_rotate": true, "is_server": true, "max_size_chunk_upload":
-209715200, "pubsub_central_broker": false, "receive_from_any_connector_owner":
-true, "recv_message_types": [ "any" ], "send_message_types": [ "any" ],
-"server_sockaddr": [ "127.0.0.1", 10673 ], "uds_path_receive_preserve_socket":
-true, "uds_path_send_preserve_socket": true } -
-**alternate\_client\_default\_cert** is false by default : if true it lets the
-client try to connect alternatively with the default certificate, in case of
-failure with the private certificate. This can save the hassle of having to
+"connector_files_dirpath": "/var/tmp/aioconnectors", "default_logger_bk_count":
+5, "default_logger_dirpath": "/var/tmp/aioconnectors",
+"default_logger_log_level": "INFO", "default_logger_rotate": true, "is_server":
+true, "max_size_chunk_upload": 209715200, "pubsub_central_broker": false,
+"receive_from_any_connector_owner": true, "recv_message_types": [ "any" ],
+"send_message_types": [ "any" ], "server_sockaddr": [ "127.0.0.1", 10673 ],
+"uds_path_receive_preserve_socket": true, "uds_path_send_preserve_socket": true
+} -**alternate\_client\_default\_cert** is false by default : if true it lets
+the client try to connect alternatively with the default certificate, in case
+of failure with the private certificate. This can save the hassle of having to
 delete manually your client certificate when the certificate was already
 deleted on server side. This affects also the token authentication : the client
 will try to connect alternatively by requesting a new token if its token fails.
 -**blacklisted\_clients\_id|ip|subnet** : a list of blacklisted clients (regex
 for blacklisted\_clients\_id), can be updated on the fly with the api functions
 add|remove\_blacklist\_client or in the cli. -**certificates\_directory\_path**
 is where your certificates are located, if use\_ssl is True. This is the
@@ -515,15 +516,16 @@
 server\_sockaddr, since sometimes name resolution with getaddrinfo is slow. -
 **connector\_files\_dirpath** is important, it is the path where all internal
 files are stored. The default is /var/tmp/aioconnectors. unix sockets files,
 default log files, and persistent files are stored there. -**debug_msg_counts**
 is a boolean, enables to display every 2 minutes a count of messages in the log
 file, and in stdout if **silent** is disabled. -**default\_logger\_rotate**
 (boolean) can also be an integer telling the maximum size of the log file in
-bytes. There are 5 backups configured, compressed with gzip. -
+bytes. -**default\_logger\_bk\_count** an integer telling the maximum number of
+gzip compressed logs kept when log rotate is enabled. Default is 5. -
 **disk\_persistence\_recv** : In order to enable persistence between the
 connector and a message listener (supported on both client and server sides),
 use disk\_persistence\_recv=True (applies to all message types).
 disk\_persistence\_recv can also be a list of message types for which to apply
 persistence. There will be 1 persistence file per message type. -
 **file\_recv\_config** : In order to be able to receive files, you must define
 the destination path of files according to their associated dst\_type. This is
```

### Comparing `aioconnectors-1.6.1/setup.py` & `aioconnectors-1.6.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 
 # Always prefer setuptools over distutils
 from setuptools import setup, find_packages
 # To use a consistent encoding
 from codecs import open
 from os import path
 
-VERSION = '1.6.1'
+VERSION = '1.6.2'
 
 here = path.abspath(path.dirname(__file__))
 # Get the long description from the README file
 with open(path.join(here, 'README.md'), encoding='utf-8') as fd:
     long_description = fd.read()
 
 # Arguments marked as "Required" below must be included for upload to PyPI.
```

