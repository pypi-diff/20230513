# Comparing `tmp/cxmlinvbot-1.0.5.tar.gz` & `tmp/cxmlinvbot-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cxmlinvbot-1.0.5.tar", last modified: Sat May  6 13:55:47 2023, max compression
+gzip compressed data, was "cxmlinvbot-1.1.0.tar", last modified: Sat May 13 13:34:52 2023, max compression
```

## Comparing `cxmlinvbot-1.0.5.tar` & `cxmlinvbot-1.1.0.tar`

### file list

```diff
@@ -1,47 +1,48 @@
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.861601 cxmlinvbot-1.0.5/
--rw-rw-rw-   0        0        0      166 2023-05-06 13:55:47.860093 cxmlinvbot-1.0.5/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.709973 cxmlinvbot-1.0.5/cxmlinvbot/
--rw-rw-rw-   0        0        0        0 2023-05-06 08:44:56.000000 cxmlinvbot-1.0.5/cxmlinvbot/__init__.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.729960 cxmlinvbot-1.0.5/cxmlinvbot/config/
--rw-rw-rw-   0        0        0        0 2023-04-19 13:14:10.000000 cxmlinvbot-1.0.5/cxmlinvbot/config/__init__.py
--rw-rw-rw-   0        0        0     1483 2023-05-06 13:54:30.000000 cxmlinvbot-1.0.5/cxmlinvbot/config/base.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.740891 cxmlinvbot-1.0.5/cxmlinvbot/errors/
--rw-rw-rw-   0        0        0        0 2023-05-06 10:19:45.000000 cxmlinvbot-1.0.5/cxmlinvbot/errors/__init__.py
--rw-rw-rw-   0        0        0      400 2023-05-05 17:26:49.000000 cxmlinvbot-1.0.5/cxmlinvbot/errors/errors.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.752866 cxmlinvbot-1.0.5/cxmlinvbot/filing/
--rw-rw-rw-   0        0        0        0 2023-05-06 10:19:57.000000 cxmlinvbot-1.0.5/cxmlinvbot/filing/__init__.py
--rw-rw-rw-   0        0        0     2066 2023-05-01 15:06:11.000000 cxmlinvbot-1.0.5/cxmlinvbot/filing/filing.py
--rw-rw-rw-   0        0        0      246 2023-05-06 11:05:58.000000 cxmlinvbot-1.0.5/cxmlinvbot/kill.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.763350 cxmlinvbot-1.0.5/cxmlinvbot/mail/
--rw-rw-rw-   0        0        0        0 2023-05-06 10:20:09.000000 cxmlinvbot-1.0.5/cxmlinvbot/mail/__init__.py
--rw-rw-rw-   0        0        0     2784 2023-05-06 11:03:43.000000 cxmlinvbot-1.0.5/cxmlinvbot/mail/mail.py
--rw-rw-rw-   0        0        0     7361 2023-05-06 13:53:17.000000 cxmlinvbot-1.0.5/cxmlinvbot/main.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.795264 cxmlinvbot-1.0.5/cxmlinvbot/mapping/
--rw-rw-rw-   0        0        0        0 2023-05-06 10:20:19.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/__init__.py
--rw-rw-rw-   0        0        0     1925 2023-05-06 13:49:41.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/action.py
--rw-rw-rw-   0        0        0     4713 2023-05-06 11:04:04.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/headermapping.py
--rw-rw-rw-   0        0        0    12894 2023-05-06 13:38:46.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/invoicedetailrequestmapping.py
--rw-rw-rw-   0        0        0      638 2023-05-06 09:04:46.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/mapping.py
--rw-rw-rw-   0        0        0      464 2023-05-06 09:52:03.000000 cxmlinvbot-1.0.5/cxmlinvbot/mapping/profilerequestmapping.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.815211 cxmlinvbot-1.0.5/cxmlinvbot/objects/
--rw-rw-rw-   0        0        0        0 2023-04-19 11:11:56.000000 cxmlinvbot-1.0.5/cxmlinvbot/objects/__init__.py
--rw-rw-rw-   0        0        0     5144 2023-05-06 09:08:47.000000 cxmlinvbot-1.0.5/cxmlinvbot/objects/cxmlobject.py
--rw-rw-rw-   0        0        0     1359 2023-05-06 09:05:33.000000 cxmlinvbot-1.0.5/cxmlinvbot/objects/profileresponse.py
--rw-rw-rw-   0        0        0      803 2023-05-06 09:05:41.000000 cxmlinvbot-1.0.5/cxmlinvbot/objects/response.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.856104 cxmlinvbot-1.0.5/cxmlinvbot/unittests/
--rw-rw-rw-   0        0        0        0 2023-04-19 11:22:52.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/__init__.py
--rw-rw-rw-   0        0        0     2231 2023-05-06 13:49:56.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_action.py
--rw-rw-rw-   0        0        0     2947 2023-05-06 09:06:03.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_cxmlobject.py
--rw-rw-rw-   0        0        0      932 2023-05-06 09:06:10.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_errors.py
--rw-rw-rw-   0        0        0     3050 2023-05-06 11:05:43.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_filing.py
--rw-rw-rw-   0        0        0     1107 2023-05-06 09:49:37.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_mapping.py
--rw-rw-rw-   0        0        0     2164 2023-05-06 09:46:38.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_profileresponse.py
--rw-rw-rw-   0        0        0     1123 2023-05-06 09:07:06.000000 cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_response.py
-drwxrwxrwx   0        0        0        0 2023-05-06 13:55:47.723935 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/
--rw-rw-rw-   0        0        0      166 2023-05-06 13:55:47.000000 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1116 2023-05-06 13:55:47.000000 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-06 13:55:47.000000 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       29 2023-05-06 13:55:47.000000 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-05-06 13:55:47.000000 cxmlinvbot-1.0.5/cxmlinvbot.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-05-06 13:55:47.861601 cxmlinvbot-1.0.5/setup.cfg
--rw-rw-rw-   0        0        0      639 2023-05-06 09:55:52.000000 cxmlinvbot-1.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:52.284175 cxmlinvbot-1.1.0/
+-rw-rw-rw-   0        0        0      166 2023-05-13 13:34:52.283160 cxmlinvbot-1.1.0/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.942665 cxmlinvbot-1.1.0/cxmlinvbot/
+-rw-rw-rw-   0        0        0        0 2023-05-06 08:44:56.000000 cxmlinvbot-1.1.0/cxmlinvbot/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.962613 cxmlinvbot-1.1.0/cxmlinvbot/config/
+-rw-rw-rw-   0        0        0        0 2023-04-19 13:14:10.000000 cxmlinvbot-1.1.0/cxmlinvbot/config/__init__.py
+-rw-rw-rw-   0        0        0     1641 2023-05-13 13:29:31.000000 cxmlinvbot-1.1.0/cxmlinvbot/config/base.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.970595 cxmlinvbot-1.1.0/cxmlinvbot/errors/
+-rw-rw-rw-   0        0        0        0 2023-05-06 10:19:45.000000 cxmlinvbot-1.1.0/cxmlinvbot/errors/__init__.py
+-rw-rw-rw-   0        0        0      445 2023-05-13 12:28:57.000000 cxmlinvbot-1.1.0/cxmlinvbot/errors/errors.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.979603 cxmlinvbot-1.1.0/cxmlinvbot/filing/
+-rw-rw-rw-   0        0        0        0 2023-05-06 10:19:57.000000 cxmlinvbot-1.1.0/cxmlinvbot/filing/__init__.py
+-rw-rw-rw-   0        0        0     2349 2023-05-13 13:12:19.000000 cxmlinvbot-1.1.0/cxmlinvbot/filing/filing.py
+-rw-rw-rw-   0        0        0      246 2023-05-06 11:05:58.000000 cxmlinvbot-1.1.0/cxmlinvbot/kill.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.988543 cxmlinvbot-1.1.0/cxmlinvbot/mail/
+-rw-rw-rw-   0        0        0        0 2023-05-06 10:20:09.000000 cxmlinvbot-1.1.0/cxmlinvbot/mail/__init__.py
+-rw-rw-rw-   0        0        0     3393 2023-05-10 18:39:23.000000 cxmlinvbot-1.1.0/cxmlinvbot/mail/mail.py
+-rw-rw-rw-   0        0        0     9021 2023-05-13 12:46:13.000000 cxmlinvbot-1.1.0/cxmlinvbot/main.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:52.013478 cxmlinvbot-1.1.0/cxmlinvbot/mapping/
+-rw-rw-rw-   0        0        0        0 2023-05-06 10:20:19.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/__init__.py
+-rw-rw-rw-   0        0        0     1925 2023-05-06 13:49:41.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/action.py
+-rw-rw-rw-   0        0        0     4712 2023-05-10 12:55:16.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/headermapping.py
+-rw-rw-rw-   0        0        0    12894 2023-05-10 12:56:37.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/invoicedetailrequestmapping.py
+-rw-rw-rw-   0        0        0     1046 2023-05-13 12:27:38.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/mapping.py
+-rw-rw-rw-   0        0        0      464 2023-05-06 09:52:03.000000 cxmlinvbot-1.1.0/cxmlinvbot/mapping/profilerequestmapping.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:52.191813 cxmlinvbot-1.1.0/cxmlinvbot/objects/
+-rw-rw-rw-   0        0        0        0 2023-04-19 11:11:56.000000 cxmlinvbot-1.1.0/cxmlinvbot/objects/__init__.py
+-rw-rw-rw-   0        0        0     5144 2023-05-06 09:08:47.000000 cxmlinvbot-1.1.0/cxmlinvbot/objects/cxmlobject.py
+-rw-rw-rw-   0        0        0     1359 2023-05-06 09:05:33.000000 cxmlinvbot-1.1.0/cxmlinvbot/objects/profileresponse.py
+-rw-rw-rw-   0        0        0      803 2023-05-06 09:05:41.000000 cxmlinvbot-1.1.0/cxmlinvbot/objects/response.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:52.279170 cxmlinvbot-1.1.0/cxmlinvbot/unittests/
+-rw-rw-rw-   0        0        0        0 2023-04-19 11:22:52.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/__init__.py
+-rw-rw-rw-   0        0        0     2231 2023-05-06 13:49:56.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_action.py
+-rw-rw-rw-   0        0        0     2947 2023-05-06 09:06:03.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_cxmlobject.py
+-rw-rw-rw-   0        0        0     1218 2023-05-13 12:30:12.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_errors.py
+-rw-rw-rw-   0        0        0     2950 2023-05-13 13:26:20.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_filing.py
+-rw-rw-rw-   0        0        0    24304 2023-05-13 12:46:25.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_main.py
+-rw-rw-rw-   0        0        0     2183 2023-05-13 12:30:54.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_mapping.py
+-rw-rw-rw-   0        0        0     2164 2023-05-06 09:46:38.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_profileresponse.py
+-rw-rw-rw-   0        0        0     1123 2023-05-06 09:07:06.000000 cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_response.py
+drwxrwxrwx   0        0        0        0 2023-05-13 13:34:51.955633 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/
+-rw-rw-rw-   0        0        0      166 2023-05-13 13:34:51.000000 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1150 2023-05-13 13:34:51.000000 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 13:34:51.000000 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 13:34:51.000000 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-05-13 13:34:51.000000 cxmlinvbot-1.1.0/cxmlinvbot.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 13:34:52.284175 cxmlinvbot-1.1.0/setup.cfg
+-rw-rw-rw-   0        0        0      671 2023-05-13 13:33:59.000000 cxmlinvbot-1.1.0/setup.py
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/config/base.py` & `cxmlinvbot-1.1.0/cxmlinvbot/config/base.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,35 @@
 from local.config.env import EnvConfig
 
 
 class BaseConfig(object):
 
+    # XML/cXML config...
     DTD_VERSION             = '1.2.020'
     DTD_ROOT_PATH           = 'http://xml.cxml.org/schemas/cXML/%s/' % DTD_VERSION
     XML_NS                  = 'http://www.w3.org/XML/1998/namespace'
     CXML_DTD_URL            = '%scXML.dtd' % DTD_ROOT_PATH
     INVOICE_DETAIL_DTD_URL  = '%sInvoiceDetail.dtd' % DTD_ROOT_PATH
     
+    # COUPA config...
     PROD_COUPA_END_POINT    = 'https://cbre.coupahost.com/cxml/'
     TEST_COUPA_END_POINT    = 'https://cbre-test.coupahost.com/cxml/'
     PROD_INVOICE_END_POINT  = '%sinvoices/' % PROD_COUPA_END_POINT
     TEST_INVOICE_END_POINT  = '%sinvoices/' % TEST_COUPA_END_POINT
 
+    # Miscellania...
+    MAIL_PREAMBLE           = 'Pro Door Invoice Bot - '
+    VERSION                 = '1.1.0'
+
+    # Testing widgets...
     SAMPLE_PATH             = '%sResources\\cXML\\1.2.057\\Samples\\' % EnvConfig.PROJECT_ROOT
     XML_SAMPLES             = {
         'ProfileResponse'           : '%sprofileresponse.xml' % SAMPLE_PATH,
         'ProfileResponseNoDTD'      : '%sprofileresponsenodtd.xml' % SAMPLE_PATH,
         'ProfileResponseInvalidXML' : '%sprofileresponseinvalidxml.xml' % SAMPLE_PATH,
         'ProfileResponseInvalidDTD' : '%sprofileresponseinvaliddtd.xml' % SAMPLE_PATH,
         'Response'                  : '%sresponse.xml' % SAMPLE_PATH,
         'ResponseWithData'          : '%sresponsewithdata.xml' % SAMPLE_PATH,
     }
     
     CSV_SAMPLE              = '%sCXML Site - Documents\\CSV Invoices\\%s' % (EnvConfig.PROJECT_ROOT, 'CSV 25th to 31st March 2023.csv')
-    VERSION                 = '1.0.5'
+
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/filing/filing.py` & `cxmlinvbot-1.1.0/cxmlinvbot/filing/filing.py`

 * *Files 6% similar despite different names*

```diff
@@ -9,49 +9,57 @@
 
 class ArchiveException(Exception):
     pass
 
 
 class Archive(object):
 
+    FMT = '%Y%m%d%H%M%S'
+    
     def __init__(self, path, ext, period):
         logger.info('Creating Archive @%s for files of type %s for a period of %d days' % (path, ext, period))
         os.makedirs(path, exist_ok=True)
         self._path = path
         self._period = period
         self._ext = ext
-        self._pattern = re.compile('(?P<date>[0-9]{8})\..*\.%s' % ext)
+        self._pattern = re.compile('(?P<datetime>[0-9]{14})\..*\.%s' % ext)
         
     def archive(self, path, name):
-        new = '%s.%s' % (datetime.date.today().strftime('%Y%m%d'), name)
+        new = '%s.%s' % (datetime.datetime.now().strftime(self.FMT), name)
         if self._pattern.fullmatch(new):
             newFP = '%s%s' % (self._path, new)
             os.rename('%s%s' %  (path, name), newFP)
             return newFP
         else:
             raise(ArchiveException('File to be archived (%s) does not match Arhive pattern (%s)' % (new, self._pattern.pattern)))
 
+    def _hasArchiveExt(self, name):
+        return name.split('.')[-1] == self._ext
+    
     def createFile(self, name):
-        new = '%s.%s.%s' % (datetime.date.today().strftime('%Y%m%d'), name, self._ext)
+        if self._hasArchiveExt(name):
+            new = '%s.%s' % (datetime.datetime.now().strftime(self.FMT), name)
+        else:
+            new = '%s.%s.%s' % (datetime.datetime.now().strftime(self.FMT), name, self._ext)
         if self._pattern.fullmatch(new):
             return open('%s%s' % (self._path, new), 'w')
         else:
             raise(ArchiveException('File to be archived (%s) does not match Arhive pattern (%s)' % (new, self._pattern.pattern)))
 
     def exists(self, name):
-        tgt = name if self._ext in name else '%s.%s' % (name, self._ext)
+        tgt = name if self._hasArchiveExt(name) else '%s.%s' % (name, self._ext)
         return len(glob.glob('%s*.%s' % (self._path, tgt))) > 0
                       
     def cleanse(self):
         logger.info('Cleansing archive @%s' % self._path)
         files = glob.glob('*.%s' % self._ext, root_dir=self._path)
         for f in files:
             m = self._pattern.fullmatch(f)
             if m:
-                d = datetime.datetime.strptime(m.group('date'), '%Y%m%d').date()
+                d = datetime.datetime.strptime(m.group('datetime'), self.FMT).date()
                 if (datetime.date.today() - d).days >= self._period:
                     logger.info('Deleting - %s%s' % (self._path, f))
                     os.remove('%s%s' % (self._path, f))
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/mail/mail.py` & `cxmlinvbot-1.1.0/cxmlinvbot/mail/mail.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 import itertools
 import logging
 import sys
 import io
 import smtplib
 from   datetime import datetime, timedelta
+from   encrypta import encrypta
 
+from local.config.env import EnvConfig
 from local.config.mail import MailConfig
 
 logger = logging.getLogger(__name__)
 
 
 class Mail():
     '''
@@ -18,32 +20,40 @@
         '''
         Initialise the Mail class with content; all parameters are optional
         and can be added instead via the Mail interface.
 
         :param subject: the subject line of the email
         :param content: a list of strs or files containing content
         '''
-        self._container = 'MIME-Version: 1.0\nContent-type: text/html\n' \
-                'Subject:{subject}\n\n{body}</body>'
+        self._container = 'MIME-Version: 1.0\nFrom:{sender}\nTo:{to}\n'\
+            'Content-type: text/html\nSubject:{subject}\n\n{body}</body>'
         self._firstTable = True
         self._subject = ''
         self._body = ''
         self._stdRecipients = True
 
         self.addSubject(subject)
         self.addContent(content)
 
         self._sender = MailConfig.FROM
+        self._user = MailConfig.USER
         self._recipients = MailConfig.RECIPIENTS
-        self._server = smtplib.SMTP(MailConfig.SVR, MailConfig.PORT)
+        self._useSSL = MailConfig.USE_SSL
+        if self._useSSL:
+            self._server = smtplib.SMTP_SSL(MailConfig.SVR, MailConfig.PORT)
+        else:
+            self._server = smtplib.SMTP(MailConfig.SVR, MailConfig.PORT)
+        #self._server.set_debuglevel(1)
         if 'localhost' not in MailConfig.SVR:
             self._server.ehlo()
-            self._server.starttls()
-            self._server.ehlo()
-            self._server.login(self._sender, MailConfig.PWD)
+            if not self._useSSL:
+                self._server.starttls()
+                self._server.ehlo()
+            with open('%s\\local\\config\\env.py' % EnvConfig.PROJECT_FULLPATH, 'r') as f:
+                self._server.login(self._user, encrypta.decrypt(bytearray(MailConfig.PWD), f.readline()))
         
     def addSubject(self, subject:str):
         if isinstance(subject, str):
             self._subject = subject
 
     def addContent(self, content):
         if content:
@@ -71,15 +81,16 @@
         self._addTextContent(content.read())
 
     def send(self):
        self._server.sendmail(*self._repr()) 
        logger.info('email sent to: {!s}'.format(self._recipients))
  
     def __str__(self):
-        return self._container.format(subject=self._subject, body=self._body)
+        return self._container.format(sender=self._sender, to=','.join(self._recipients), \
+                                      subject=self._subject, body=self._body)
 
     def __repr__(self):
         return str(self._repr())
     
     def _repr(self):
         return (self._sender, self._recipients, str(self))
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/main.py` & `cxmlinvbot-1.1.0/cxmlinvbot/main.py`

 * *Files 17% similar despite different names*

```diff
@@ -14,30 +14,14 @@
 from   cxmlinvbot.mapping.action import MapActionError
 from   cxmlinvbot.mapping.invoicedetailrequestmapping import InvoiceDetailRequestMapping
 from   cxmlinvbot.objects.cxmlobject import CXMLObject, CXML_DTDError
 from   cxmlinvbot.objects.response import Response
 from   local.config.env import EnvConfig
 from   local.config.mail import MailConfig
 
-'''
-# For debugging HTTP requests
-import http.client as http_client
-http_client.HTTPConnection.debuglevel = 1
-'''
-
-logging.basicConfig(level=logging.INFO,
-                    format='%(asctime)s : %(levelname)s : %(module)s : %(message)s')
-logger = logging.getLogger(__name__)
-
-csvArchive = Archive(EnvConfig.ACRHIVE_CSV_PATH, 'csv', EnvConfig.CLEANSE_PERIOD)
-cxmlArchive = Archive(EnvConfig.ACRHIVE_CXML_PATH, 'cxml', EnvConfig.CLEANSE_PERIOD)
-logArchive = Archive(EnvConfig.LOG_PATH, 'log', EnvConfig.CLEANSE_PERIOD)
-
-mail = Mail()
-
 
 def cleanseAll():
     if EnvConfig.CLEANSE_ARCHIVES:
         csvArchive.cleanse()
         cxmlArchive.cleanse()
     if EnvConfig.CLEANSE_LOGS:
         logArchive.cleanse()
@@ -52,128 +36,186 @@
     # Can raise ConnectionError
     headers = {'Content-Type':'text/xml'}
     r = requests.post(endPoint, headers=headers, data=cxml.asXMLString())
 
     logger.info('Response for cxml from endpoint - %s : %s' % (r.status_code, r.text))
     if r.status_code == 200:
         cxmlResp = Response()
+        # lxml etree doesn't like the encoding to be resent in the xml header
         cxmlResp.fromXMLString(r.text.replace('encoding="UTF-8"', ''))
         if cxmlResp.status.code == 200:
             with cxmlArchive.createFile(invoice) as cxmlFile:
                 cxmlFile.write(cxml.asXMLString(prettyPrint=True))
         else:
             return {invoice : '%s : %s : %s' % (cxmlResp.status.code, cxmlResp.status.text, cxmlResp.status.data)}
     else:
        # Raise as HTTPError
        r.raise_for_status()
     return {}
 
 def processInvoice(row):
-    invoice = row['InvoiceNumber']
-    if not len(invoice):
-        raise MapActionError('Data Error: InvoiceNumber field is missing from CSV can\'t do anything without this')
+    invoice = row.get('InvoiceNumber', '')
+    if not (type(invoice) == str and len(invoice)):
+        return {'UNKNOWN' : 'There are rows in the CSV file without an InvoiceNumber field.'}
     
     logger.info('Processing invoice - %s' % invoice)
     if not cxmlArchive.exists(invoice):
         cxml = CXMLObject()
         req = InvoiceDetailRequestMapping()
         try:
-            cxml.fromPathValueMap(req.perform(row))
+            cxml.fromPathValueMap(req.perform(row, catchAll=True))
             cxml.validate(req.getDTD_URL())
         except MapActionError as e1:
-            logger.error('Data Error: CSV mapping failed, please correct CSV for missing fields below...')
+            logger.error('CSV mapping failed, please correct CSV for missing fields below...')
             logger.error(e1)
             return {invoice : e1}
         except CXML_DTDError as e2:
-            logger.error('Data Error: Invoice failed to validate against the DTD, this will need to be corrected...')
+            logger.error('Invoice failed to validate against the DTD, this will need to be corrected...')
             logger.error(e2)  
             return {invoice : e2}
         return postCXML(invoice, cxml)
     else:
         logger.info('Seen this invoice before, will not process again')
     return {}
 
 def mailBatchComplete(f, badInvoices):
     logger.info(MailConfig.BATCH_MAIL_TEMPLATE % (f, len(badInvoices)))
-    mail.addSubject('Prodoor Invoice Bot - %s' % f)
+    mail = Mail()
+    mail.addSubject(BaseConfig.MAIL_PREAMBLE + f)
     mail.addContent(MailConfig.BATCH_MAIL_TEMPLATE % (f, len(badInvoices)))
     for n, (i, e) in enumerate(badInvoices.items()):
         if n == 0:
             mail.addContent(MailConfig.ERROR_INTRO)
         mail.addContent(MailConfig.INVOICE_ERROR % (i, e))
     mail.send()
 
 def mailFatal(message):
     logger.fatal(message)
-    mail.addSubject('Prodoor Invoice Bot - FATAL error')
+    mail = Mail()
+    mail.addSubject(BaseConfig.MAIL_PREAMBLE + 'FATAL error')
     mail.addContent('ERROR DETAILS\n')
     mail.addContent(message)
     mail.send()
 
-def main():
-    pid = os.getpid()
-    logger.info('Starting ProDoor Invoice Bot...PID (%s)' % pid)
-    logger.info('Running in %s deployment mode' % EnvConfig.DEPLOYMENT_MODE)
+def mailLockedFile(f):
+    mail = Mail()
+    mail.addSubject(BaseConfig.MAIL_PREAMBLE + 'Locked File Warning')
+    mail.addContent('The CSV file "%s" is locked by another user.\n' % f)
+    mail.addContent('Possibly it is still open in Excel?\n')
+    mail.addContent('Please release the file ASAP.\n')
+    mail.addContent('Invoice Bot will continue trying to access it for another %s minutes.\n' % EnvConfig.LOCKED_FILE_RETRIES)
+    mail.addContent('If still locked, the Bot will exit and need to be restarted.')
+    mail.send()
 
-    cleanseAll()
+def starting(pid):
+    title = BaseConfig.MAIL_PREAMBLE + 'Starting'
+    body  = 'Running in %s deployment mode as PID %s.' % (EnvConfig.DEPLOYMENT_MODE, pid)
+    logger.info(title)
+    logger.info(body)
+    mail = Mail()
+    mail.addSubject(title)
+    mail.addContent(body)
+    mail.send()
+
+def stopping(pid):
+    title = BaseConfig.MAIL_PREAMBLE + 'Stopping'
+    body  = 'PID %s exiting gracefully.' % pid
+    logger.info(title)
+    logger.info(body)
+    mail = Mail()
+    mail.addSubject(title)
+    mail.addContent(body)
+    mail.send()
 
+def createGrace(pid):
     # Deleting the grace file will cause the bot to exit gracefully
     graceFile = '%s%s.grace' % (EnvConfig.PROJECT_FULLPATH, pid)
     pathlib.Path(graceFile).touch()
+    return graceFile
+
+def pathExists(f):
+    # Wrapper method to simplify unittesting    
+    return os.path.exists(f)
+
+def openFile(f, newline='', encoding='utf-8-sig', mode='r+'):
+    # Wrapper method to simplify unittesting
+    return open(f, newline=newline, encoding=encoding, mode=mode)
+
+def wait():
+    # Wrapper method to simplify unittesting
+    time.sleep(EnvConfig.HEARTBEAT_TIME)
+
+def main():
+    pid = os.getpid()
+    starting(pid)
+    # cleanseAll must be called before createGrace otherwise the bot will never startup
+    cleanseAll()
+    graceFile = createGrace(pid)
 
     lockedFileCountMap = {}
     try:
-        while(os.path.exists(graceFile)):
+        while(pathExists(graceFile)):
             # List available csv files
             files = glob.glob('*.csv', root_dir=EnvConfig.NEW_CSV_PATH)
             for f in files:
                 logger.info('Processing CSV invoice file - %s' % f)
                 # TODO: may not need to do this locked file handling if the windows scheduling works as anticpiated
                 lockedFileCount = lockedFileCountMap.get(f, 0)
                 try:
-                    csvFile = open(EnvConfig.NEW_CSV_PATH + f, newline='', encoding='utf-8-sig', mode='r+')
+                    with openFile(EnvConfig.NEW_CSV_PATH + f) as csvFile:
+                        badInvoices = {}
+                        reader = csv.DictReader(csvFile, delimiter=',')
+                        for row in reader:
+                            # Don't process empty rows
+                            if ''.join(row.values()).strip():
+                                badInvoices.update(processInvoice(row))
+                    csvArchive.archive(EnvConfig.NEW_CSV_PATH, f)
+                    mailBatchComplete(f, badInvoices)
                 except PermissionError as e:
                     # The file is locked let's go round the loop and see if it becomes unlocked
                     lockedFileCountMap[f] = lockedFileCount + 1
                     if lockedFileCount + 1 > EnvConfig.LOCKED_FILE_RETRIES:
                         raise LockedFileError('CSV file locked for over %d minutes - %s' % (EnvConfig.LOCKED_FILE_RETRIES, f))
+                    elif lockedFileCount == 0:
+                        # Send out mail on the first lock to give users an opportunity to release the file before
+                        # we exit
+                        mailLockedFile(f)
                     logger.warning('CSV is locked by another user, will retry.')
-                    continue
-
-                badInvoices = {}
-                reader = csv.DictReader(csvFile, delimiter=',')
-                for row in reader:
-                    badInvoices.update(processInvoice(row))
-                csvFile.close()
-                csvArchive.archive(EnvConfig.NEW_CSV_PATH, f)
-                
-                mailBatchComplete(f, badInvoices)
-
-            time.sleep(EnvConfig.HEARTBEAT_TIME)
-            logger.info('HEARTBEAT...')
-        logger.info('Exiting...')
+            wait()
+            logger.info('HEARTBEAT...')            
+        stopping(pid)
         return 0
     except LockedFileError as lfe:
-        message = str(lfe)
-        message += traceback.format_exc() + '\n'
-        message += 'Invoice Bot has died and will be automatically restarted shortly\n'
-        message += 'Please close the CSV file ASAP...'
+        message = str(lfe) + '\n'
+        message += 'Please close the CSV file ASAP and restart the Bot.'
         errorCode = 100
     except (ConnectionError, requests.HTTPError):
-        message = 'Connection Error: An error occurred either connecting to or sending data to the Coupa endpoint...\n'
+        message = 'Connection Error: An error occurred either connecting to or sending data to the Coupa endpoint.\n'
         message += traceback.format_exc() + '\n'
-        message += 'Invoice Bot has died and will be automatically restarted shortly\n'
-        message += 'If this error does not clear on restart pleace contact Coupa support...'
+        message += 'If this error does not clear on restart pleace contact IT and/or Coupa support.'
         errorCode = 100
     except BaseException:
         message = 'Fatal Error: An unexpected error condition occured...\n'
         message += traceback.format_exc() + '\n'
-        message += 'Invoice Bot has died and will NOT be automatically restarted\n'
-        message += 'Please address the above error and restart the Bot...'
+        message += 'Please contact IT to address the above error and restart the Bot.'
         errorCode = 999
     mailFatal(message)
 
     return errorCode
 
 
 if __name__ == '__main__':
+    '''
+    # For debugging HTTP requests
+    import http.client as http_client
+    http_client.HTTPConnection.debuglevel = 1
+    '''
+    
+    logging.basicConfig(level=logging.INFO,
+                        format='%(asctime)s : %(levelname)s : %(module)s : %(message)s')
+    logger = logging.getLogger(__name__)
+
+    csvArchive = Archive(EnvConfig.ACRHIVE_CSV_PATH, 'csv', EnvConfig.CLEANSE_PERIOD)
+    cxmlArchive = Archive(EnvConfig.ACRHIVE_CXML_PATH, 'cxml', EnvConfig.CLEANSE_PERIOD)
+    logArchive = Archive(EnvConfig.LOG_PATH, 'log', EnvConfig.CLEANSE_PERIOD)
+
     main()
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/mapping/action.py` & `cxmlinvbot-1.1.0/cxmlinvbot/mapping/action.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/mapping/headermapping.py` & `cxmlinvbot-1.1.0/cxmlinvbot/mapping/headermapping.py`

 * *Files 0% similar despite different names*

```diff
@@ -45,15 +45,15 @@
         SACountry=cxmlinvbot.mapping.action.Default('Header/From/Correspondent/Contact/PostalAddress/Country@isoCountryCode', 'GB'),
         SharedSecret=cxmlinvbot.mapping.action.Default('Header/Sender/Credential/SharedSecret', 'none'),
         SupplierDomain=cxmlinvbot.mapping.action.Default(('Header/From/Credential@domain',
                                                 'Header/Sender/Credential@domain'),
                                                 'DUNS'), 
         SupplierID=cxmlinvbot.mapping.action.Default(('Header/From/Credential/Identity',
                                             'Header/Sender/Credential/Identity'),
-                                            'PRODOORGWS'), # Default to 'PRODOORGWS' as there are so few invoices for the 'PRODOORMA' entity that they can be entered manually
+                                            'PRODOORMA'), # Default to 'PRODOORMA' as there are so few invoices for the 'PRODOORGWS' entity that they can be entered manually
         Version=cxmlinvbot.mapping.action.Default('@version', BaseConfig.DTD_VERSION),
         PayloadID=cxmlinvbot.mapping.action.Lambda('@payloadID', lambda : '%s@prodoor.com'%int(datetime.datetime.now().timestamp()), ()),
         TimeStamp=cxmlinvbot.mapping.action.Lambda('@timestamp', lambda : datetime.datetime.now().isoformat(), ()),
         Language=cxmlinvbot.mapping.action.Default(('Header/From/Correspondent/Contact/Name@xml:lang',
                                          'Header/To/Correspondent/Contact/Name@xml:lang',
                                          '@xml:lang'),
                                          'en'),
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/mapping/invoicedetailrequestmapping.py` & `cxmlinvbot-1.1.0/cxmlinvbot/mapping/invoicedetailrequestmapping.py`

 * *Files 0% similar despite different names*

```diff
@@ -38,15 +38,15 @@
     #'Request/InvoiceDetailRequest/InvoiceDetailSummary/Tax/Extrinsic',
     'Request/InvoiceDetailRequest/InvoiceDetailSummary/GrossAmount/Money',
     'Request/InvoiceDetailRequest/InvoiceDetailSummary/NetAmount/Money',
     'Request/InvoiceDetailRequest/InvoiceDetailSummary/DueAmount/Money',
   ]
 
   FIELD_TO_ACTION_MAPS = HeaderMapping.FIELD_TO_ACTION_MAPS + [dict(
-    BillToAddressID=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact@addressID', '357122'),
+    BillToAddressID=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact@addressID', '357106'),
     ContactName=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact/Name', 'CBRE MANAGED SERVICES LIMITED'),
     POAddressLine1=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact/PostalAddress/Street', '61 SOUTHWARK STREET'),
     POCity=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact/PostalAddress/City', 'London'),
     POPostalCode=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact/PostalAddress/PostalCode', 'SE1 0HL'),
     POCountry=cxmlinvbot.mapping.action.Default('Request/InvoiceDetailRequest/InvoiceDetailRequestHeader/InvoicePartner/Contact/PostalAddress/Country@isoCountryCode', 'GB'),
     # This first set of fields come directly from the CSV and in the same order
     #SAVATRegNO=cxmlinvbot.mapping.action.Default(('Request/InvoiceDetailRequest/InvoiceDetailOrder/InvoiceDetailItem/Tax/Extrinsic',
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/objects/cxmlobject.py` & `cxmlinvbot-1.1.0/cxmlinvbot/objects/cxmlobject.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/objects/profileresponse.py` & `cxmlinvbot-1.1.0/cxmlinvbot/objects/profileresponse.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/objects/response.py` & `cxmlinvbot-1.1.0/cxmlinvbot/objects/response.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_action.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_action.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_cxmlobject.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_cxmlobject.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_errors.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_errors.py`

 * *Files 20% similar despite different names*

```diff
@@ -16,19 +16,27 @@
         e = CXML_DTDError('Bang!')
         self.assertEqual(str(e), 'Document Error: Bang!')
 
     def test_DocumentError(self):
         e = DocumentError('Bang!')
         self.assertEqual(str(e), 'Document Error: Bang!')
 
+    def test_DocumentErrorNoPremable(self):
+        e = DocumentError('Bang!', preamble=False)
+        self.assertEqual(str(e), 'Bang!')
+
     def test_LockedFileError(self):
         e = LockedFileError('Bang!')
         self.assertEqual(str(e), 'Locked File Error: Bang!')
         
     def test_MapActionError(self):
         e = MapActionError('Bang!')
         self.assertEqual(str(e), 'Document Error: Bang!')
 
+    def test_MapActionErrorNoPreamble(self):
+        e = MapActionError('Bang!', preamble=False)
+        self.assertEqual(str(e), 'Bang!')
+
 
 if __name__ == '__main__':
     import unittest
     unittest.main()
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_filing.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_filing.py`

 * *Files 16% similar despite different names*

```diff
@@ -10,15 +10,16 @@
 class TestFiling(TestCase):
     '''Filing tests'''
 
     ARCH_PATH = 'c:\\temp\\test\\archive\\'
     TEST_PATH = 'c:\\temp\\test\\'
     TEST_FILE = 'afile.log'
     TEST_FILE_FP = '%s%s' % (TEST_PATH, TEST_FILE)
-    ARCH_FILE_FP = '%s%s.%s' % (ARCH_PATH, datetime.date.today().strftime('%Y%m%d'), TEST_FILE)
+    ARCH_DATE = '2023051201101211'
+    ARCH_FILE_FP = '%s%s.%s' % (ARCH_PATH, ARCH_DATE, TEST_FILE)
 
     def setUp(self):
         os.makedirs(self.TEST_PATH, exist_ok=True)
         pathlib.Path(self.TEST_FILE_FP).touch()
 
     def tearDown(self):
         if os.path.exists(self.ARCH_FILE_FP):
@@ -33,47 +34,50 @@
         os.makedirs(self.ARCH_PATH)
         a = Archive(self.ARCH_PATH, 'log', 10)
         self.assertTrue(os.path.exists(self.ARCH_PATH))
 
     def testArchiveFile(self):
         a = Archive(self.ARCH_PATH, 'log', 10)
         self.assertTrue(os.path.exists(self.TEST_FILE_FP))
-        archFP = a.archive(self.TEST_PATH, self.TEST_FILE)
+        f = a.archive(self.TEST_PATH, self.TEST_FILE)
         self.assertFalse(os.path.exists(self.TEST_FILE_FP))
-        self.assertTrue(os.path.exists(self.ARCH_FILE_FP))
-        self.assertEqual(self.ARCH_FILE_FP, archFP)
+        self.assertTrue(os.path.exists(f))
+        os.remove(f)
 
     def testArchiveCleanse(self):
         a = Archive(self.ARCH_PATH, 'log', 1)
-        a.archive(self.TEST_PATH, self.TEST_FILE)
-        pathlib.Path(self.ARCH_PATH + '20230430.afile.log').touch()
-        pathlib.Path(self.ARCH_PATH + '20230429.afile.log').touch()
-        self.assertTrue(os.path.exists(self.ARCH_PATH + '20230430.afile.log'))
-        self.assertTrue(os.path.exists(self.ARCH_PATH + '20230429.afile.log'))
+        f = a.archive(self.TEST_PATH, self.TEST_FILE)
+        af1 = '20220430101243.%s' % self.TEST_FILE
+        af2 = '20210429112234.%s' % self.TEST_FILE
+        pathlib.Path(self.ARCH_PATH + af1).touch()
+        pathlib.Path(self.ARCH_PATH + af2).touch()
+        self.assertTrue(os.path.exists(self.ARCH_PATH + af1))
+        self.assertTrue(os.path.exists(self.ARCH_PATH + af2))
         a.cleanse()
-        self.assertTrue(os.path.exists(self.ARCH_FILE_FP))
-        self.assertFalse(os.path.exists(self.ARCH_PATH + '20230430.afile.log'))
-        self.assertFalse(os.path.exists(self.ARCH_PATH + '20230429.afile.log'))
+        self.assertTrue(os.path.exists(f))
+        self.assertFalse(os.path.exists(self.ARCH_PATH + af1))
+        self.assertFalse(os.path.exists(self.ARCH_PATH + af2))
+        os.remove(f)
         
     def testArchiveExtUnknown(self):
         a = Archive(self.ARCH_PATH, 'log', 10)
-        self.assertRaises(ArchiveException, a.archive, self.TEST_PATH, 'afile.csv')
+        self.assertRaises(ArchiveException, a.archive, self.TEST_PATH, 'another_file')
 
     def testArchiveCreateFile(self):
         a = Archive(self.ARCH_PATH, 'log', 10)
-        f = a.createFile('myfile')
+        f = a.createFile(self.TEST_FILE)
         f.close()
-        newFile = '%s%s.myfile.log' % (self.ARCH_PATH, datetime.date.today().strftime('%Y%m%d'))
-        self.assertTrue(os.path.exists(newFile))
-        os.remove(newFile)
+        self.assertTrue(os.path.exists(f.name))
+        os.remove(f.name)
 
     def testArchiveExists(self):
         a = Archive(self.ARCH_PATH, 'log', 10)
-        a.archive(self.TEST_PATH, self.TEST_FILE)
+        f = a.archive(self.TEST_PATH, self.TEST_FILE)
         self.assertTrue(a.exists(self.TEST_FILE))
         self.assertTrue(a.exists(self.TEST_FILE.split('.')[0]))
         self.assertFalse(a.exists('any old file'))
+        os.remove(f)
 
 
 if __name__ == '__main__':
     import unittest
     unittest.main()
```

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_profileresponse.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_profileresponse.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot/unittests/test_response.py` & `cxmlinvbot-1.1.0/cxmlinvbot/unittests/test_response.py`

 * *Files identical despite different names*

### Comparing `cxmlinvbot-1.0.5/cxmlinvbot.egg-info/SOURCES.txt` & `cxmlinvbot-1.1.0/cxmlinvbot.egg-info/SOURCES.txt`

 * *Files 14% similar despite different names*

```diff
@@ -26,10 +26,11 @@
 cxmlinvbot/objects/profileresponse.py
 cxmlinvbot/objects/response.py
 cxmlinvbot/unittests/__init__.py
 cxmlinvbot/unittests/test_action.py
 cxmlinvbot/unittests/test_cxmlobject.py
 cxmlinvbot/unittests/test_errors.py
 cxmlinvbot/unittests/test_filing.py
+cxmlinvbot/unittests/test_main.py
 cxmlinvbot/unittests/test_mapping.py
 cxmlinvbot/unittests/test_profileresponse.py
 cxmlinvbot/unittests/test_response.py
```

### Comparing `cxmlinvbot-1.0.5/setup.py` & `cxmlinvbot-1.1.0/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -12,15 +12,16 @@
 #
 # python setup.py install
 #
 # prerequisite: setuptools
 # http://pypi.python.org/pypi/setuptools
 
 REQUIRES = ['lxml>=4.9.2',
-            'requests>=2.29.0']
+            'requests>=2.29.0',
+            'encrypta>=1.0.0']
 
 setup(
     name=NAME,
     version=VERSION,
     description="Invoice Bot - PO to Invoice in CXML",
     author_email="monkeeferret@gmail.com",
     install_requires=REQUIRES,
```

