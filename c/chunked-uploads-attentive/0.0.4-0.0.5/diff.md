# Comparing `tmp/chunked-uploads-attentive-0.0.4.tar.gz` & `tmp/chunked-uploads-attentive-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chunked-uploads-attentive-0.0.4.tar", last modified: Thu Apr 13 07:19:05 2023, max compression
+gzip compressed data, was "chunked-uploads-attentive-0.0.5.tar", last modified: Sat May 13 13:39:54 2023, max compression
```

## Comparing `chunked-uploads-attentive-0.0.4.tar` & `chunked-uploads-attentive-0.0.5.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-04-13 07:19:05.641483 chunked-uploads-attentive-0.0.4/
--rw-rw-rw-   0        0        0      478 2023-04-13 07:19:05.640494 chunked-uploads-attentive-0.0.4/PKG-INFO
--rw-rw-rw-   0        0        0       42 2023-04-13 07:19:05.642480 chunked-uploads-attentive-0.0.4/setup.cfg
--rw-rw-rw-   0        0        0      893 2023-04-13 07:18:20.000000 chunked-uploads-attentive-0.0.4/setup.py
-drwxrwxrwx   0        0        0        0 2023-04-13 07:19:05.606107 chunked-uploads-attentive-0.0.4/src/
-drwxrwxrwx   0        0        0        0 2023-04-13 07:19:05.617482 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/
--rw-rw-rw-   0        0        0      478 2023-04-13 07:19:05.000000 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      527 2023-04-13 07:19:05.000000 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-13 07:19:05.000000 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       27 2023-04-13 07:19:05.000000 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-04-13 07:19:05.000000 chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-04-13 07:19:05.638504 chunked-uploads-attentive-0.0.4/src/uploads/
--rw-rw-rw-   0        0        0        0 2023-03-21 15:09:06.000000 chunked-uploads-attentive-0.0.4/src/uploads/__init__.py
--rw-rw-rw-   0        0        0      325 2023-03-21 15:15:16.000000 chunked-uploads-attentive-0.0.4/src/uploads/admin.py
--rw-rw-rw-   0        0        0      152 2023-03-21 15:09:06.000000 chunked-uploads-attentive-0.0.4/src/uploads/apps.py
--rw-rw-rw-   0        0        0      301 2023-02-16 16:23:12.000000 chunked-uploads-attentive-0.0.4/src/uploads/constants.py
--rw-rw-rw-   0        0        0      262 2023-02-13 12:36:18.000000 chunked-uploads-attentive-0.0.4/src/uploads/exceptions.py
--rw-rw-rw-   0        0        0     3879 2023-03-31 07:05:44.000000 chunked-uploads-attentive-0.0.4/src/uploads/models.py
--rw-rw-rw-   0        0        0      376 2023-02-13 12:36:18.000000 chunked-uploads-attentive-0.0.4/src/uploads/response.py
--rw-rw-rw-   0        0        0      570 2023-03-21 15:17:55.000000 chunked-uploads-attentive-0.0.4/src/uploads/serializers.py
--rw-rw-rw-   0        0        0     2334 2023-03-21 15:10:53.000000 chunked-uploads-attentive-0.0.4/src/uploads/settings.py
--rw-rw-rw-   0        0        0       63 2023-03-21 15:09:06.000000 chunked-uploads-attentive-0.0.4/src/uploads/tests.py
--rw-rw-rw-   0        0        0    18287 2023-03-31 07:10:24.000000 chunked-uploads-attentive-0.0.4/src/uploads/views.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:39:54.438647 chunked-uploads-attentive-0.0.5/
+-rw-rw-rw-   0        0        0      478 2023-05-13 13:39:54.437647 chunked-uploads-attentive-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0       42 2023-05-13 13:39:54.438647 chunked-uploads-attentive-0.0.5/setup.cfg
+-rw-rw-rw-   0        0        0      893 2023-05-13 13:38:48.000000 chunked-uploads-attentive-0.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:39:54.400646 chunked-uploads-attentive-0.0.5/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 13:39:54.410646 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/
+-rw-rw-rw-   0        0        0      478 2023-05-13 13:39:54.000000 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      527 2023-05-13 13:39:54.000000 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 13:39:54.000000 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       27 2023-05-13 13:39:54.000000 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-05-13 13:39:54.000000 chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 13:39:54.435650 chunked-uploads-attentive-0.0.5/src/uploads/
+-rw-rw-rw-   0        0        0        0 2023-03-21 15:09:06.000000 chunked-uploads-attentive-0.0.5/src/uploads/__init__.py
+-rw-rw-rw-   0        0        0      325 2023-04-20 11:41:44.000000 chunked-uploads-attentive-0.0.5/src/uploads/admin.py
+-rw-rw-rw-   0        0        0      152 2023-04-20 11:41:44.000000 chunked-uploads-attentive-0.0.5/src/uploads/apps.py
+-rw-rw-rw-   0        0        0      300 2023-04-20 11:41:44.000000 chunked-uploads-attentive-0.0.5/src/uploads/constants.py
+-rw-rw-rw-   0        0        0      262 2023-02-13 12:36:18.000000 chunked-uploads-attentive-0.0.5/src/uploads/exceptions.py
+-rw-rw-rw-   0        0        0     3853 2023-05-07 19:41:00.000000 chunked-uploads-attentive-0.0.5/src/uploads/models.py
+-rw-rw-rw-   0        0        0      384 2023-04-20 11:41:44.000000 chunked-uploads-attentive-0.0.5/src/uploads/response.py
+-rw-rw-rw-   0        0        0      578 2023-04-20 11:41:44.000000 chunked-uploads-attentive-0.0.5/src/uploads/serializers.py
+-rw-rw-rw-   0        0        0     2417 2023-05-07 19:40:59.000000 chunked-uploads-attentive-0.0.5/src/uploads/settings.py
+-rw-rw-rw-   0        0        0       63 2023-03-21 15:09:06.000000 chunked-uploads-attentive-0.0.5/src/uploads/tests.py
+-rw-rw-rw-   0        0        0    12227 2023-05-12 19:57:30.000000 chunked-uploads-attentive-0.0.5/src/uploads/views.py
```

### Comparing `chunked-uploads-attentive-0.0.4/setup.py` & `chunked-uploads-attentive-0.0.5/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 import codecs
 import os
 
-VERSION = '0.0.4'
+VERSION = '0.0.5'
 DESCRIPTION = 'Chunked Upload of files on gcs using Django'
 LONG_DESCRIPTION = 'A package that allows to transfer files and resume in case of data failure'
 
 # Setting up
 setup(
     name="chunked-uploads-attentive",
     version=VERSION,
```

### Comparing `chunked-uploads-attentive-0.0.4/src/chunked_uploads_attentive.egg-info/SOURCES.txt` & `chunked-uploads-attentive-0.0.5/src/chunked_uploads_attentive.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `chunked-uploads-attentive-0.0.4/src/uploads/models.py` & `chunked-uploads-attentive-0.0.5/src/uploads/models.py`

 * *Files 18% similar despite different names*

```diff
@@ -3,107 +3,124 @@
 
 from django.db import models
 from django.conf import settings
 from django.core.files.uploadedfile import UploadedFile
 from django.utils import timezone
 from google.cloud import storage
 
-from .settings import EXPIRATION_DELTA, UPLOAD_TO, STORAGE, DEFAULT_MODEL_USER_FIELD_NULL, DEFAULT_MODEL_USER_FIELD_BLANK
+from .settings import (
+    EXPIRATION_DELTA,
+    UPLOAD_TO,
+    STORAGE,
+    DEFAULT_MODEL_USER_FIELD_NULL,
+    DEFAULT_MODEL_USER_FIELD_BLANK,
+)
 from .constants import CHUNKED_UPLOAD_CHOICES, UPLOADING
 
 
 def generate_upload_id():
     return uuid.uuid4().hex
 
+
 def upload_remote_path(instance, filename):
     parent_folder = "chunked_uploads"
     today = timezone.localtime(timezone.now()).date()
     upload_id = instance.upload_id
     filename = instance.filename
     return f"{parent_folder}/{today}/{upload_id}/{filename}"
 
+
 class AbstractChunkedUpload(models.Model):
     """
     Base chunked upload model. This model is abstract (doesn't create a table
     in the database).
     Inherit from this model to implement your own.
     """
 
-    upload_id = models.CharField(max_length=32, unique=True, editable=False,
-                                 default=generate_upload_id)
-    file = models.FileField(max_length=255, upload_to=upload_remote_path,
-                            storage=STORAGE)
+    upload_id = models.CharField(
+        max_length=32, unique=True, editable=False, default=generate_upload_id
+    )
+    file = models.FileField(max_length=255, upload_to=UPLOAD_TO, storage=STORAGE)
     filename = models.CharField(max_length=255)
     offset = models.BigIntegerField(default=0)
     created_on = models.DateTimeField(auto_now_add=True)
-    status = models.PositiveSmallIntegerField(choices=CHUNKED_UPLOAD_CHOICES,
-                                              default=UPLOADING)
+    status = models.PositiveSmallIntegerField(
+        choices=CHUNKED_UPLOAD_CHOICES, default=UPLOADING
+    )
     completed_on = models.DateTimeField(null=True, blank=True)
     file_md5 = models.CharField(null=True, max_length=128)
 
     @property
     def expires_on(self):
         return self.created_on + EXPIRATION_DELTA
 
     @property
     def expired(self):
         return self.expires_on <= timezone.now()
 
     @property
     def md5(self):
-        if getattr(self, '_md5', None) is None:
+        if getattr(self, "_md5", None) is None:
             md5 = hashlib.md5()
             for chunk in self.file.chunks():
                 md5.update(chunk)
             self._md5 = md5.hexdigest()
         return self._md5
 
     def delete(self, delete_file=True, *args, **kwargs):
         if self.file:
             storage, path = self.file.storage, self.file.path
         super(AbstractChunkedUpload, self).delete(*args, **kwargs)
         if self.file and delete_file:
             storage.delete(path)
 
     def __str__(self):
-        return u'<%s - upload_id: %s - bytes: %s - status: %s>' % (
-            self.filename, self.upload_id, self.offset, self.status)
+        return "<%s - upload_id: %s - bytes: %s - status: %s>" % (
+            self.filename,
+            self.upload_id,
+            self.offset,
+            self.status,
+        )
+
+    def append_chunk(self, chunk, chunk_size=None, save=True, chunk_num=0):
+        self.file.close()
+        with open(
+            self.file.path + str(chunk_num), "wb"
+        ) as file_obj:  # mode = write+binary
+            file_obj.write(chunk.read(-1))
+            # We can use .read() safely because chunk is already in memory
 
-    def append_chunk(self, chunk, chunk_size=None,chunk_number=0, save=True,attrs= None):
-        today = attrs['today']
-        bucket = attrs['bucket']
-        blob = bucket.blob(f"chunked_uploads/{today}/{self.upload_id}/{self.filename}{chunk_number}")
-        blob.upload_from_file(chunk, content_type=chunk.content_type,rewind=True)
         if chunk_size is not None:
             self.offset += chunk_size
-        elif hasattr(chunk, 'size'):
+        elif hasattr(chunk, "size"):
             self.offset += chunk.size
         else:
             self.offset = self.file.size
         self._md5 = None  # Clear cached md5
         if save:
             self.save()
         self.file.close()  # Flush
 
     def get_uploaded_file(self):
         self.file.close()
-        self.file.open(mode='rb')  # mode = read+binary
-        return UploadedFile(file=self.file, name=self.filename,
-                            size=self.offset)
+        self.file.open(mode="rb")  # mode = read+binary
+        return UploadedFile(file=self.file, name=self.filename, size=self.offset)
 
     class Meta:
         abstract = True
 
 
 class ChunkedUpload(AbstractChunkedUpload):
     """
     Default chunked upload model.
     """
+
     user = models.ForeignKey(
         settings.AUTH_USER_MODEL,
         on_delete=models.CASCADE,
-        related_name='chunked_uploads',
+        related_name="chunked_uploads",
         null=DEFAULT_MODEL_USER_FIELD_NULL,
-        blank=DEFAULT_MODEL_USER_FIELD_BLANK
+        blank=DEFAULT_MODEL_USER_FIELD_BLANK,
     )
 
+
 MyChunkedUpload = ChunkedUpload
```

### Comparing `chunked-uploads-attentive-0.0.4/src/uploads/serializers.py` & `chunked-uploads-attentive-0.0.5/src/uploads/serializers.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,16 +4,18 @@
 
 class BaseModelSerializer(serializers.ModelSerializer):
     """Base Serializer class to be inherited by other Serializer classes."""
 
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)  # noqa
 
+
 class ChunkedUploadSerializer(BaseModelSerializer):
     class Meta:
         model = MyChunkedUpload
         fields = "__all__"
-    def md5(self,obj):
+
+    def md5(self, obj):
         return obj.md5
 
-    def get_uploaded_file(self,obj):
-        return obj.get_uploaded_file()
+    def get_uploaded_file(self, obj):
+        return obj.get_uploaded_file()
```

### Comparing `chunked-uploads-attentive-0.0.4/src/uploads/settings.py` & `chunked-uploads-attentive-0.0.5/src/uploads/settings.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,59 +1,67 @@
 import time
 import os.path
 from datetime import timedelta
 from django.utils.module_loading import import_string
 from django.conf import settings
+from django.utils import timezone
 
 try:
     from django.core.serializers.json import DjangoJSONEncoder
 except ImportError:
     try:
         # Deprecated class name (for backwards compatibility purposes)
         from django.core.serializers.json import (
-            DateTimeAwareJSONEncoder as DjangoJSONEncoder
+            DateTimeAwareJSONEncoder as DjangoJSONEncoder,
         )
     except ImportError:
-        raise ImportError('Dude! what version of Django are you using?')
+        raise ImportError("Dude! what version of Django are you using?")
 
 # How long after creation the upload will expire
 DEFAULT_EXPIRATION_DELTA = timedelta(days=1)
-EXPIRATION_DELTA = getattr(settings, 'CHUNKED_UPLOAD_EXPIRATION_DELTA',
-                           DEFAULT_EXPIRATION_DELTA)
+EXPIRATION_DELTA = getattr(
+    settings, "CHUNKED_UPLOAD_EXPIRATION_DELTA", DEFAULT_EXPIRATION_DELTA
+)
 
 # Path where uploading files will be stored until completion
-DEFAULT_UPLOAD_PATH = 'chunked_uploads/%Y/%m/%d'
-UPLOAD_PATH = getattr(settings, 'CHUNKED_UPLOAD_PATH', DEFAULT_UPLOAD_PATH)
+today = timezone.localtime(timezone.now()).date()
+DEFAULT_UPLOAD_PATH = "chunked_uploads"  # here
+UPLOAD_PATH = getattr(settings, "CHUNKED_UPLOAD_PATH", DEFAULT_UPLOAD_PATH)
 
 
 # upload_to function to be used in the FileField
 def default_upload_to(instance, filename):
-    filename = os.path.join(UPLOAD_PATH, instance.upload_id + '.part')
+    filename = os.path.join(UPLOAD_PATH, instance.upload_id, instance.filename)
     return time.strftime(filename)
 
 
-UPLOAD_TO = getattr(settings, 'CHUNKED_UPLOAD_TO', default_upload_to)
+UPLOAD_TO = getattr(settings, "CHUNKED_UPLOAD_TO", default_upload_to)
 
 # Storage system
 
 
 try:
-    STORAGE = getattr(settings, 'CHUNKED_UPLOAD_STORAGE_CLASS', lambda: None)()
+    STORAGE = getattr(settings, "CHUNKED_UPLOAD_STORAGE_CLASS", lambda: None)()
 except TypeError:
-    STORAGE = import_string(getattr(settings, 'CHUNKED_UPLOAD_STORAGE_CLASS', lambda: None))()
+    STORAGE = import_string(
+        getattr(settings, "CHUNKED_UPLOAD_STORAGE_CLASS", lambda: None)
+    )()
 
 # Function used to encode response data. Receives a dict and return a string
 DEFAULT_ENCODER = DjangoJSONEncoder().encode
-ENCODER = getattr(settings, 'CHUNKED_UPLOAD_ENCODER', DEFAULT_ENCODER)
+ENCODER = getattr(settings, "CHUNKED_UPLOAD_ENCODER", DEFAULT_ENCODER)
 
 # Content-Type for the response data
-DEFAULT_CONTENT_TYPE = 'application/json'
-CONTENT_TYPE = getattr(settings, 'CHUNKED_UPLOAD_CONTENT_TYPE',
-                       DEFAULT_CONTENT_TYPE)
+DEFAULT_CONTENT_TYPE = "application/json"
+CONTENT_TYPE = getattr(settings, "CHUNKED_UPLOAD_CONTENT_TYPE", DEFAULT_CONTENT_TYPE)
 
 # Max amount of data (in bytes) that can be uploaded. `None` means no limit
 DEFAULT_MAX_BYTES = None
-MAX_BYTES = getattr(settings, 'CHUNKED_UPLOAD_MAX_BYTES', DEFAULT_MAX_BYTES)
+MAX_BYTES = getattr(settings, "CHUNKED_UPLOAD_MAX_BYTES", DEFAULT_MAX_BYTES)
 
 # determine the "null" and "blank" properties of "user" field in the "ChunkedUpload" model
-DEFAULT_MODEL_USER_FIELD_NULL = getattr(settings, 'CHUNKED_UPLOAD_MODEL_USER_FIELD_NULL', True)
-DEFAULT_MODEL_USER_FIELD_BLANK = getattr(settings, 'CHUNKED_UPLOAD_MODEL_USER_FIELD_BLANK', True)
+DEFAULT_MODEL_USER_FIELD_NULL = getattr(
+    settings, "CHUNKED_UPLOAD_MODEL_USER_FIELD_NULL", True
+)
+DEFAULT_MODEL_USER_FIELD_BLANK = getattr(
+    settings, "CHUNKED_UPLOAD_MODEL_USER_FIELD_BLANK", True
+)
```

### Comparing `chunked-uploads-attentive-0.0.4/src/uploads/views.py` & `chunked-uploads-attentive-0.0.5/src/uploads/views.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 import re
 import os
 from django.views.generic import View
 from django.shortcuts import get_object_or_404
 from django.core.files.base import ContentFile
 from django.utils import timezone
+import datetime
 
 from .settings import MAX_BYTES
 from .models import ChunkedUpload, MyChunkedUpload
 from .response import Response
 from .constants import http_status, COMPLETE
 from .exceptions import ChunkedUploadError
 
@@ -22,93 +23,70 @@
 from django.views import View
 
 import hashlib
 from django.core.files.base import ContentFile
 from django.core.files.uploadedfile import InMemoryUploadedFile
 from google.cloud import storage
 
+
 def is_authenticated(user):
     if callable(user.is_authenticated):
         return user.is_authenticated()  # Django <2.0
     return user.is_authenticated  # Django >=2.0
 
 
-
-
 class ChunkedUploadBaseView(View):
     """
     Base view for the rest of chunked upload views.
     """
 
     # Has to be a ChunkedUpload subclass
-    today = timezone.localtime(timezone.now()).date()
-    client = storage.Client()
-    bucket = client.get_bucket('cos-dev-filestore')
     model = ChunkedUpload
-    user_field_name = 'user'  # the field name that point towards the AUTH_USER in ChunkedUpload class or its subclasses
+    user_field_name = "user"  # the field name that point towards the AUTH_USER in ChunkedUpload class or its subclasses
 
     def get_queryset(self, request):
         """
         Get (and filter) ChunkedUpload queryset.
         By default, users can only continue uploading their own uploads.
         """
         queryset = self.model.objects.all()
-        if hasattr(request, 'user') and is_authenticated(request.user):
+        if hasattr(request, "user") and is_authenticated(request.user):
             queryset = queryset.filter(**{self.user_field_name: request.user})
         return queryset
 
-    def validate(self, request):
-        """
-        Placeholder method to define extra validation.
-        Must raise ChunkedUploadError if validation fails.
-        """
 
     def get_response_data(self, chunked_upload, request):
         """
         Data for the response. Should return a dictionary-like object.
         Called *only* if POST is successful.
         """
         return {}
 
-    def pre_save(self, chunked_upload, request, new=False):
-        """
-        Placeholder method for calling before saving an object.
-        May be used to set attributes on the object that are implicit
-        in either the request, or the url.
-        """
-
     def save(self, chunked_upload, request, new=False):
         """
         Method that calls save(). Overriding may be useful is save() needs
         special args or kwargs.
         """
         chunked_upload.save()
 
-    def post_save(self, chunked_upload, request, new=False):
-        """
-        Placeholder method for calling after saving an object.
-        """
-
     def _save(self, chunked_upload):
         """
         Wraps save() method.
         """
         new = chunked_upload.id is None
-        self.pre_save(chunked_upload, self.request, new=new)
         self.save(chunked_upload, self.request, new=new)
-        self.post_save(chunked_upload, self.request, new=new)
 
     def check_permissions(self, request):
         """
         Grants permission to start/continue an upload based on the request.
         """
-        if hasattr(request, 'user') and not is_authenticated(request.user):
+        if hasattr(request, "user") and not is_authenticated(request.user):
             raise ChunkedUploadError(
                 status=http_status.HTTP_403_FORBIDDEN,
-                detail='Authentication credentials were not provided'
+                detail="Authentication credentials were not provided",
             )
 
     def _post(self, request, *args, **kwargs):
         raise NotImplementedError
 
     def post(self, request, *args, **kwargs):
         """
@@ -123,347 +101,211 @@
 
 class ChunkedUploadView(ChunkedUploadBaseView):
     """
     Uploads large files in multiple chunks. Also, has the ability to resume
     if the upload is interrupted.
     """
 
-    field_name = 'file'
-    content_range_header = 'HTTP_CONTENT_RANGE'
+    field_name = "file"
+    content_range_header = "HTTP_CONTENT_RANGE"
     content_range_pattern = re.compile(
-        r'^bytes (?P<start>\d+)-(?P<end>\d+)/(?P<total>\d+)$'
+        r"^bytes (?P<start>\d+)-(?P<end>\d+)/(?P<total>\d+)$"
     )
     max_bytes = MAX_BYTES  # Max amount of data that can be uploaded
     # If `fail_if_no_header` is True, an exception will be raised if the
     # content-range header is not found. Default is False to match Jquery File
     # Upload behavior (doesn't send header if the file is smaller than chunk)
     fail_if_no_header = False
 
     def get_extra_attrs(self, request):
         """
         Extra attribute values to be passed to the new ChunkedUpload instance.
         Should return a dictionary-like object.
         """
         return {}
 
-    def get_max_bytes(self, request):
-        """
-        Used to limit the max amount of data that can be uploaded. `None` means
-        no limit.
-        You can override this to have a custom `max_bytes`, e.g. based on
-        logged user.
-        """
-
-        return self.max_bytes
-
     def create_chunked_upload(self, save=False, **attrs):
         """
         Creates new chunked upload instance. Called if no 'upload_id' is
         found in the POST data.
         """
         chunked_upload = self.model(**attrs)
         # file starts empty
-        chunked_upload.file.save(name='', content=ContentFile(''), save=save)
+        chunked_upload.file.save(name="", content=ContentFile(""), save=save)
         return chunked_upload
 
     def is_valid_chunked_upload(self, chunked_upload):
         """
         Check if chunked upload has already expired or is already complete.
         """
         if chunked_upload.expired:
-            raise ChunkedUploadError(status=http_status.HTTP_410_GONE,
-                                     detail='Upload has expired')
+            raise ChunkedUploadError(
+                status=http_status.HTTP_410_GONE, detail="Upload has expired"
+            )
         error_msg = 'Upload has already been marked as "%s"'
         if chunked_upload.status == COMPLETE:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail=error_msg % 'complete')
+            raise ChunkedUploadError(
+                status=http_status.HTTP_400_BAD_REQUEST, detail=error_msg % "complete"
+            )
 
     def get_response_data(self, chunked_upload, request):
         """
         Data for the response. Should return a dictionary-like object.
         """
         return {
-            'upload_id': chunked_upload.upload_id,
-            'offset': chunked_upload.offset,
-            'expires': chunked_upload.expires_on
+            "upload_id": chunked_upload.upload_id,
+            "offset": chunked_upload.offset,
+            "expires": chunked_upload.expires_on,
         }
 
     def _post(self, request, *args, **kwargs):
         print(request)
-        chunk = request.data['file']
+        chunk = request.data["file"]
         if chunk is None:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail='No chunk file was submitted')
-        self.validate(request)
-
-        upload_id = request.data['upload_id']
-        if request.data['chunk_number']:
-            chunk_number = request.data['chunk_number'] 
+            raise ChunkedUploadError(
+                status=http_status.HTTP_400_BAD_REQUEST,
+                detail="No chunk file was submitted",
+            )
+
+        upload_id = request.data["upload_id"]
+        chunk_num = request.data['chunk_num']
         if upload_id:
-            chunked_upload = get_object_or_404(self.get_queryset(request),
-                                               upload_id=upload_id)
+            chunked_upload = get_object_or_404(
+                self.get_queryset(request), upload_id=upload_id
+            )
             self.is_valid_chunked_upload(chunked_upload)
         else:
-            attrs = {'filename': chunk.name}
-            if hasattr(request, 'user') and is_authenticated(request.user):
-                attrs['user'] = request.user
+            attrs = {"filename": chunk.name}
+            if hasattr(request, "user") and is_authenticated(request.user):
+                attrs["user"] = request.user
             attrs.update(self.get_extra_attrs(request))
             chunked_upload = self.create_chunked_upload(save=False, **attrs)
+    
+        chunked_upload.append_chunk(chunk, chunk_size=chunk.size, save=False,chunk_num = chunk_num)
 
-        content_range = request.META.get(self.content_range_header, '')
-        match = self.content_range_pattern.match(content_range)
-        print(chunk.size)
-        comments = """if offset:
-            start = int(match.group('start'))
-            end = int(match.group('end'))
-            total = int(match.group('total'))
-        elif self.fail_if_no_header:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail='Error in request headers')
-        else:
-            # Use the whole size when HTTP_CONTENT_RANGE is not provided
-            start = 0
-            end = chunk.size - 1
-            total = chunk.size
-
-        chunk_size = end - start + 1
-        max_bytes = self.get_max_bytes(request)
-
-        if max_bytes is not None and total > max_bytes:
-            raise ChunkedUploadError(
-                status=http_status.HTTP_400_BAD_REQUEST,
-                detail='Size of file exceeds the limit (%s bytes)' % max_bytes
-            )
-        print(chunked_upload.offset)
-        print(start)
-        if chunked_upload.offset != start:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail='Offsets do not match',
-                                     offset=chunked_upload.offset)
-        if chunk.size != chunk_size:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail="File size doesn't match headers")
-        """
-        attrs = {}
-        attrs['today'] = self.today
-        attrs['bucket'] = self.bucket
-        chunked_upload.append_chunk(chunk, chunk_size=chunk.size, chunk_number=chunk_number,save=False,attrs=attrs)
-
-        self._save(chunked_upload)
-
-        return Response(self.get_response_data(chunked_upload, request),
-                        status=http_status.HTTP_200_OK)
-
-
-class ChunkedUploadCompleteView(ChunkedUploadBaseView):
-    """
-    Completes an chunked upload. Method `on_completion` is a placeholder to
-    define what to do when upload is complete.
-    """
-
-    # I wouldn't recommend to turn off the md5 check, unless is really
-    # impacting your performance. Proceed at your own risk.
-    do_md5_check = False
-
-    def on_completion(self, uploaded_file, request):
-        """
-        Placeholder method to define what to do when upload is complete.
-        """
-
-    def is_valid_chunked_upload(self, chunked_upload):
-        """
-        Check if chunked upload is already complete.
-        """
-        if chunked_upload.status == COMPLETE:
-            error_msg = "Upload has already been marked as complete"
-            return ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                      detail=error_msg)
-
-    def md5_check(self, chunked_upload, md5):
-        """
-        Verify if md5 checksum sent by client matches generated md5.
-        """
-        if chunked_upload.md5 != md5:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail='md5 checksum does not match')
-
-    def _post(self, request, *args, **kwargs):
-        upload_id = request.data['upload_id']
-        md5 = request.data['md5']
-
-        error_msg = None
-        if self.do_md5_check:
-            if not upload_id or not md5:
-                error_msg = "Both 'upload_id' and 'md5' are required"
-        elif not upload_id:
-            error_msg = "'upload_id' is required"
-        if error_msg:
-            raise ChunkedUploadError(status=http_status.HTTP_400_BAD_REQUEST,
-                                     detail=error_msg)
-
-        chunked_upload = get_object_or_404(self.get_queryset(request),
-                                           upload_id=upload_id)
-
-        self.validate(request)
-        self.is_valid_chunked_upload(chunked_upload)
-        if self.do_md5_check:
-            self.md5_check(chunked_upload, md5)
-
-        chunked_upload.status = COMPLETE
-        chunked_upload.completed_on = timezone.now()
         self._save(chunked_upload)
-        self.on_completion(chunked_upload.get_uploaded_file(), request)
-
-        return Response(self.get_response_data(chunked_upload, request),
-                        status=http_status.HTTP_200_OK)
 
-class MyChunkedUploadView(ChunkedUploadView):
-
-    model = MyChunkedUpload
-    field_name = 'the_file'
-
-    def check_permissions(self, request):
-        # Allow non authenticated users to make uploads
-        pass
+        return Response(
+            self.get_response_data(chunked_upload, request),
+            status=http_status.HTTP_200_OK,
+        )
 
 class ChunkedUploadApiViewSet(viewsets.ModelViewSet):
 
+    today = timezone.localtime(timezone.now()).date()
+    client = storage.Client()
+    bucket = client.get_bucket("cos-dev-filestore")
     queryset = MyChunkedUpload.objects.all()
     model = MyChunkedUpload
     serializer_class = ChunkedUploadSerializer
-    def get_response_data(self, chunked_upload):
+    CHUNK_SIZE = 262144
+
+    def md5(self, file):
         """
-        Data for the response. Should return a dictionary-like object.
+        Caculates md5 hash value of a give file
         """
-        return {
-            'upload_id': chunked_upload.upload_id,
-            'offset': chunked_upload.offset,
-            'expires': chunked_upload.expires_on
-        }
-    def md5(self,file):
-        CHUNK_SIZE = 10485760
         md5 = hashlib.md5()
-        for chunk in file.chunks(CHUNK_SIZE):
+        for chunk in file.chunks(self.CHUNK_SIZE):
             md5.update(chunk)
         md5 = md5.hexdigest()
         return md5
+
     def create(self, request, pk=None):
-        print(os.environ["GOOGLE_APPLICATION_CREDENTIALS"])
-        file = request.data['file']
-        content_type = file.content_type
-        print(type(file))
-        md5 = self.md5(file)
-        fetch = 0
-        offset = 0
-        if self.queryset.filter(file_md5=md5).exists():
-            fetch = 1
-            resume_upload = self.queryset.get(file_md5=md5)
+        """
+        Takes in various chunks and stores them in a file. Also updates the database.
+        """
+        filename = request.data["filename"] 
+        chunk_num = request.data["chunk_num"]
+        chunk = request.data["chunk"]
+        file_md5 = request.data['file_md5'] 
+        chunk_md5 = request.data['chunk_md5']
+        #file_size = request.data["size"]
+        if(chunk_md5 != self.md5(chunk)):
+            return Response({"chunk_num" : chunk_num,"message" :"File Corrupt","status" : 2})
+
+        if self.queryset.filter(file_md5=file_md5).exists():
+            resume_upload = self.queryset.get(file_md5=file_md5)
             resume_serializer = ChunkedUploadSerializer(resume_upload)
-            upload_id = resume_serializer.data['upload_id']
-            offset = resume_serializer.data['offset']
+            upload_id = resume_serializer.data["upload_id"]
+            if resume_serializer.data['status'] == 2:
+                return Response({"chunk_num" : chunk_num,"message" :"File Already Uploaded","status" : 3,"url" :f"{resume_serializer.data['file']}"})
             print(resume_serializer.data)
-
-        CHUNK_SIZE = 10485760
-        chunk_number = 1
-        cuv = MyChunkedUploadView()
-        today = timezone.localtime(timezone.now()).date()
-        filename = request.data['filename']
-        for chunk in file.chunks(CHUNK_SIZE):
-            print(type(chunk))
-            content = ContentFile(chunk)
-            chunk = InMemoryUploadedFile(content, None, filename, content_type, len(chunk), None)
-            if fetch == 0 and chunk_number == 1:
-                request.data['file_md5'] = md5
-                request.data['file'] = chunk
-                serializer = ChunkedUploadSerializer(data=request.data)
-                serializer.is_valid(raise_exception=True)
-                serializer.save()
-                print(request)
-                upload_id = serializer.data['upload_id']
-                print(serializer.data['offset'])
-                print(upload_id)
-            if fetch == 1 and chunk_number == 1 and offset != 0:
-                offset -= CHUNK_SIZE
-                continue
-            else:
-                cuv.request = request
-                request.data['chunk_number'] = chunk_number
-                request.data['upload_id'] = upload_id
-                request.data['file'] = chunk
-                x = cuv._post(request)
-                print(x)
-            chunk_number += 1
-        today = cuv.today
-        bucket = cuv.bucket
-        outputfile = f"chunked_uploads/{today}/{upload_id}/{filename}"
-        blobs = []
-        for shard in range(1,7):
-            sfile = f'chunked_uploads/{today}/{upload_id}/{filename}{shard}'
-            blob = bucket.blob(sfile)
-            if not blob.exists():
-                # this causes a retry in 60s
-                raise ValueError(f'branch {sfile} not present')
-            blobs.append(blob)
-            bucket.blob(outputfile).compose(blobs)
-        for blob in blobs:
-            blob.delete()
-        chunked_upload = self.queryset.get(upload_id=upload_id)
-        if (md5 == chunked_upload.md5):
-            data = {"status" : 2,"completed_on" : timezone.now()}
-            serializer = ChunkedUploadSerializer(chunked_upload, data=data, partial=True)
-            if serializer.is_valid():
-                serializer.save()
-        else:
-            error_msg = 'Md5 is wrong, byte transfer error'
-            return Response(error_msg, status=400)
-        return Response(serializer.data)
-
-    resume = """def resume(self, request):
-        file = request.data['file']
-        upload_id = request.data['upload_id']
-        cuv = MyChunkedUploadView()
-        chunked_upload = self.queryset.get(upload_id=upload_id)
-        serializer = ChunkedUploadSerializer(chunked_upload)
-        offset = serializer.data['offset']
-        CHUNK_SIZE = 10485760
-        for chunk in file.chunks(CHUNK_SIZE):
-            if offset != 0:
-                offset -= CHUNK_SIZE
-                continue
+            cuv = ChunkedUploadView()
             cuv.request = request
-            request.data['file'] = chunk
+            request.data['upload_id'] = upload_id
+            request.data['file'] = chunk.open()
+            request.data['chunk_num'] = chunk_num
             x = cuv._post(request)
             print(x)
-
-        chunked_upload = self.queryset.get(upload_id=upload_id)
-        if (self.md5(file) == chunked_upload.md5):
-            data = {"status" : 2,"completed_on" : timezone.now()}
-            serializer = ChunkedUploadSerializer(chunked_upload, data=data, partial=True)
-            if serializer.is_valid():
-                serializer.save()
         else:
-            error_msg = 'Md5 is wrong, byte transfer error'
-            return Response(error_msg, status=400)
-        return Response(serializer.get_uploaded_file(chunked_upload))"""
+            request.data["file_md5"] = file_md5
+            request.data["file"] = chunk
+            serializer = ChunkedUploadSerializer(data=request.data)
+            serializer.is_valid(raise_exception=True)
+            serializer.save()
+            print(request)
+            upload_id = serializer.data["upload_id"]
+            print(serializer.data["offset"])
+            print(upload_id)    
+        return Response({"chunk_num" : chunk_num, "message" : "Done","status" : 1})
     
-    combine = '''@action(methods=["POST"], detail=False)
-    def combine(self, request):
-        today = timezone.localtime(timezone.now()).date()
-        client = storage.Client()
-        filename = "trees.mp4"
-        upload_id = "5ebceb9203204fcab712be5422fa2e04"
-        bucket = client.get_bucket('cos-dev-filestore')
-        outputfile = f"chunked_uploads/{today}/{upload_id}/{filename}"
-        blobs = []
-        for shard in range(1,7):
-            sfile = f'chunked_uploads/{today}/{upload_id}/{filename}{shard}'
-            blob = bucket.blob(sfile)
-            if not blob.exists():
-                # this causes a retry in 60s
-                raise ValueError(f'branch {sfile} not present')
-            blobs.append(blob)
-            bucket.blob(outputfile).compose(blobs)
-        for blob in blobs:
-            blob.delete()
 
-        return Response("Done")'''
+    @action(methods=["PATCH"], detail=False)
+    def combine_chunks(self, request):
+        """
+        Checks if all chunks are present and Combines them. Also deletes already combined chunks.
+        """
+        filename = request.data["filename"] 
+        file_md5 = request.data['file_md5'] 
+        file_size = int(request.data["size"])
+        if file_size%self.CHUNK_SIZE == 0:
+            ciel = int(file_size/self.CHUNK_SIZE)
+        else:
+            ciel = int(file_size/self.CHUNK_SIZE) + 1
+        if self.queryset.filter(file_md5=file_md5).exists():
+            fetch = 1
+            resume_upload = self.queryset.get(file_md5=file_md5)
+            resume_serializer = ChunkedUploadSerializer(resume_upload)
+            upload_id = resume_serializer.data["upload_id"]
+            #if resume_serializer.data['status'] == 2:
+                #return Response({"url" : f"{resume_serializer.data['file']}", "message" : "Done" , "status": 1})
+            print(resume_serializer.data['file'])
+            path = f'./chunked_uploads/{upload_id}/{filename}'
+            for i in range(2, ciel + 1):
+                if os.path.isfile(path+str(i)) == False:
+                    return Response({"chunk_num": {i},"message" : f"Chunk Number : {i} not arrived", "status": "failure"})
+
+            with open(path, "ab") as file_obj:  # mode = append+binary
+                for i in range(2,ciel + 1):
+                    with open(path+str(i),'rb') as chunk:
+                        file_obj.write(
+                            chunk.read()
+                        )
+                    os.remove(path+str(i))
+                
+        else:
+            return Response({"message" : "wrong md5", "status": 2})
+        # GCS
+        try:
+            blob = self.bucket.blob(f"chunked_uploads/{self.today}/{upload_id}/{filename}")
+            with open(path,'rb') as file:
+                blob.upload_from_file(file,rewind=True)
+            url = blob.generate_signed_url(
+                    version="v2",
+                    # This URL is valid for 365 days
+                    expiration=datetime.timedelta(days=365),
+                    # Allow GET requests using this URL.
+                    method="GET",
+                )
+            if self.queryset.filter(file_md5=file_md5).exists():
+                resume_upload = self.queryset.get(file_md5=file_md5)
+                resume_upload.file = url
+                resume_upload.completed_on = timezone.datetime.now()
+                resume_upload.status = 2
+                serializer = ChunkedUploadSerializer(resume_upload, data=request.data, partial=True)
+                if serializer.is_valid():
+                    serializer.save()
+            os.remove(path)
+        except:
+            return Response({"status" : 3, "message" : "Error on upload"})
+        return Response({"url" : f"{url}", "message" : "Done", "status": 1})
```

