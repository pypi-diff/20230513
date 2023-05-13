# Comparing `tmp/ScriptCollection-3.3.81-py3-none-any.whl.zip` & `tmp/ScriptCollection-3.3.9-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,16 +1,17 @@
-Zip file size: 57063 bytes, number of entries: 14
--rw-rw-rw-  2.0 fat    18064 b- defN 23-Mar-05 15:39 ScriptCollection/Executables.py
--rw-rw-rw-  2.0 fat    33985 b- defN 23-Mar-05 15:39 ScriptCollection/GeneralUtilities.py
+Zip file size: 47520 bytes, number of entries: 15
+-rw-rw-rw-  2.0 fat    15739 b- defN 22-Nov-14 12:37 ScriptCollection/Executables.py
+-rw-rw-rw-  2.0 fat    31649 b- defN 22-Oct-16 16:59 ScriptCollection/GeneralUtilities.py
+-rw-rw-rw-  2.0 fat     3421 b- defN 22-Aug-29 05:45 ScriptCollection/Hardening.py
 -rw-rw-rw-  2.0 fat     1937 b- defN 22-Aug-30 21:59 ScriptCollection/ProgramRunnerBase.py
 -rw-rw-rw-  2.0 fat     6273 b- defN 22-Oct-16 19:55 ScriptCollection/ProgramRunnerEpew.py
 -rw-rw-rw-  2.0 fat     3023 b- defN 22-Aug-30 21:59 ScriptCollection/ProgramRunnerPopen.py
--rw-rw-rw-  2.0 fat    86232 b- defN 23-May-13 14:35 ScriptCollection/ScriptCollectionCore.py
--rw-rw-rw-  2.0 fat   127118 b- defN 23-May-13 14:35 ScriptCollection/TasksForCommonProjectStructure.py
+-rw-rw-rw-  2.0 fat    75969 b- defN 22-Nov-18 12:58 ScriptCollection/ScriptCollectionCore.py
+-rw-rw-rw-  2.0 fat    74893 b- defN 22-Nov-18 12:58 ScriptCollection/TasksForCommonProjectStructure.py
 -rw-rw-rw-  2.0 fat     7918 b- defN 22-Aug-30 21:59 ScriptCollection/UpdateCertificates.py
 -rw-rw-rw-  2.0 fat        0 b- defN 22-Aug-29 05:45 ScriptCollection/__init__.py
--rw-rw-rw-  2.0 fat     7878 b- defN 23-May-13 14:35 ScriptCollection-3.3.81.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-May-13 14:35 ScriptCollection-3.3.81.dist-info/WHEEL
--rw-rw-rw-  2.0 fat     1968 b- defN 23-May-13 14:35 ScriptCollection-3.3.81.dist-info/entry_points.txt
--rw-rw-rw-  2.0 fat       17 b- defN 23-May-13 14:35 ScriptCollection-3.3.81.dist-info/top_level.txt
--rw-rw-r--  2.0 fat     1295 b- defN 23-May-13 14:35 ScriptCollection-3.3.81.dist-info/RECORD
-14 files, 295800 bytes uncompressed, 54871 bytes compressed:  81.4%
+-rw-rw-rw-  2.0 fat     7146 b- defN 22-Nov-18 12:58 ScriptCollection-3.3.9.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 22-Nov-18 12:58 ScriptCollection-3.3.9.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat     1697 b- defN 22-Nov-18 12:58 ScriptCollection-3.3.9.dist-info/entry_points.txt
+-rw-rw-rw-  2.0 fat       17 b- defN 22-Nov-18 12:58 ScriptCollection-3.3.9.dist-info/top_level.txt
+?rw-rw-r--  2.0 fat     1375 b- defN 22-Nov-18 12:58 ScriptCollection-3.3.9.dist-info/RECORD
+15 files, 231149 bytes uncompressed, 45204 bytes compressed:  80.4%
```

## zipnote {}

```diff
@@ -1,13 +1,16 @@
 Filename: ScriptCollection/Executables.py
 Comment: 
 
 Filename: ScriptCollection/GeneralUtilities.py
 Comment: 
 
+Filename: ScriptCollection/Hardening.py
+Comment: 
+
 Filename: ScriptCollection/ProgramRunnerBase.py
 Comment: 
 
 Filename: ScriptCollection/ProgramRunnerEpew.py
 Comment: 
 
 Filename: ScriptCollection/ProgramRunnerPopen.py
@@ -21,23 +24,23 @@
 
 Filename: ScriptCollection/UpdateCertificates.py
 Comment: 
 
 Filename: ScriptCollection/__init__.py
 Comment: 
 
-Filename: ScriptCollection-3.3.81.dist-info/METADATA
+Filename: ScriptCollection-3.3.9.dist-info/METADATA
 Comment: 
 
-Filename: ScriptCollection-3.3.81.dist-info/WHEEL
+Filename: ScriptCollection-3.3.9.dist-info/WHEEL
 Comment: 
 
-Filename: ScriptCollection-3.3.81.dist-info/entry_points.txt
+Filename: ScriptCollection-3.3.9.dist-info/entry_points.txt
 Comment: 
 
-Filename: ScriptCollection-3.3.81.dist-info/top_level.txt
+Filename: ScriptCollection-3.3.9.dist-info/top_level.txt
 Comment: 
 
-Filename: ScriptCollection-3.3.81.dist-info/RECORD
+Filename: ScriptCollection-3.3.9.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ScriptCollection/Executables.py

```diff
@@ -1,15 +1,16 @@
-import os
 import argparse
 import time
 import traceback
 import keyboard
+
 from .TasksForCommonProjectStructure import TasksForCommonProjectStructure
 from .ScriptCollectionCore import ScriptCollectionCore
 from .GeneralUtilities import GeneralUtilities
+from .Hardening import HardeningScript
 
 
 def DotNetsign() -> int:
     parser = argparse.ArgumentParser(description='Signs a dll- or exe-file with a snk-file. Requires ilasm and ildasm as available commandline-commands.')
     parser.add_argument("dllOrExefile")
     parser.add_argument("snkfile")
     parser.add_argument("verbose", action='store_true')
@@ -249,14 +250,23 @@
     parser.add_argument('--inputfolder', help='Specifies the folder where the files are stored whose names should be obfuscated', required=True)
 
     args = parser.parse_args()
     ScriptCollectionCore().SCObfuscateFilesFolder(args.inputfolder, args.printtableheadline, args.namemappingfile, args.extensions)
     return 0
 
 
+def Hardening() -> int:
+    parser = argparse.ArgumentParser()
+    parser.add_argument('--applicationstokeep', required=True)
+    parser.add_argument('--additionalfolderstoremove', required=True)
+    args = parser.parse_args()
+    HardeningScript(args.applicationstokeep, args.additionalfolderstoremove).run()
+    return 0
+
+
 def HealthCheck() -> int:
     parser = argparse.ArgumentParser()
     parser.add_argument('--file', required=True)
     args = parser.parse_args()
     return ScriptCollectionCore().SCHealthcheck(args.file)
 
 
@@ -276,61 +286,7 @@
     parser.add_argument('--repositoryfolder', required=False, default=".")
     parser.add_argument('--verbosity', required=False, default=1)
     parser.add_argument('--buildenvironment', required=False, default="QualityCheck")
     parser.add_argument('--additionalargumentsfile', required=False, default=None)
     args = parser.parse_args()
     TasksForCommonProjectStructure().build_codeunits(args.repositoryfolder, int(args.verbosity), args.buildenvironment, args.additionalargumentsfile)
     return 0
-
-
-def GenerateCertificateAuthority() -> int:
-    parser = argparse.ArgumentParser()
-    parser.add_argument('--name', required=True)
-    parser.add_argument('--subj_c', required=True)
-    parser.add_argument('--subj_st', required=True)
-    parser.add_argument('--subj_l', required=True)
-    parser.add_argument('--subj_o', required=True)
-    parser.add_argument('--subj_ou', required=True)
-    parser.add_argument('--days_until_expire', required=False, default=None, type=int)
-    parser.add_argument('--password', required=False, default=None)
-    args = parser.parse_args()
-    ScriptCollectionCore().generate_certificate_authority(os.getcwd(), args.name, args.subj_c, args.subj_st, args.subj_l, args.subj_o, args.subj_ou, args.days_until_expire, args.password)
-    return 0
-
-
-def GenerateCertificate() -> int:
-    parser = argparse.ArgumentParser()
-    parser.add_argument('--domain', required=True)
-    parser.add_argument('--subj_c', required=True)
-    parser.add_argument('--subj_st', required=True)
-    parser.add_argument('--subj_l', required=True)
-    parser.add_argument('--subj_o', required=True)
-    parser.add_argument('--subj_ou', required=True)
-    parser.add_argument('--days_until_expire', required=False, default=None, type=int)
-    parser.add_argument('--password', required=False, default=None)
-    args = parser.parse_args()
-    ScriptCollectionCore().generate_certificate(os.getcwd(), args.domain, args.subj_c, args.subj_st, args.subj_l, args.subj_o, args.subj_ou, args.days_until_expire, args.password)
-    return 0
-
-
-def GenerateCertificateSignRequest() -> int:
-    parser = argparse.ArgumentParser()
-    parser.add_argument('--domain', required=True)
-    parser.add_argument('--subj_c', required=True)
-    parser.add_argument('--subj_st', required=True)
-    parser.add_argument('--subj_l', required=True)
-    parser.add_argument('--subj_o', required=True)
-    parser.add_argument('--subj_ou', required=True)
-    args = parser.parse_args()
-    ScriptCollectionCore().generate_certificate_sign_request(os.getcwd(), args.domain, args.subj_c, args.subj_st, args.subj_l, args.subj_o, args.sub_ou)
-    return 0
-
-
-def SignCertificate() -> int:
-    parser = argparse.ArgumentParser()
-    parser.add_argument('--cafolder', required=True)
-    parser.add_argument('--caname', required=True)
-    parser.add_argument('--targetcertificate', required=True)
-    parser.add_argument('--days_until_expire', required=False, default=None, type=int)
-    args = parser.parse_args()
-    ScriptCollectionCore().sign_certificate(os.getcwd(), args.cafolder, args.caname, args.targetcertificate, args.args.days_until_expire)
-    return 0
```

## ScriptCollection/GeneralUtilities.py

```diff
@@ -1,28 +1,24 @@
 import codecs
 import inspect
 import ctypes
 import hashlib
 import re
 import os
 import shutil
-import urllib
 import stat
-import secrets
-import string as strin
 import sys
 import traceback
 from datetime import datetime, timedelta
 from os import listdir
 from os.path import isfile, join, isdir
 from pathlib import Path
 from shutil import copyfile
 import typing
 from defusedxml.minidom import parse
-from OpenSSL import crypto
 
 
 class GeneralUtilities:
 
     __date_format: str = "%Y-%m-%dT%H:%M:%S"
 
     @staticmethod
@@ -67,17 +63,17 @@
                 result.append(argument)
         return result
 
     @staticmethod
     @check_arguments
     def string_to_lines(string: str, add_empty_lines: bool = True, adapt_lines: bool = True) -> list[str]:
         result = list()
-        if (string is not None):
+        if(string is not None):
             lines = list()
-            if ("\n" in string):
+            if("\n" in string):
                 lines = string.split("\n")
             else:
                 lines.append(string)
         for rawline in lines:
             if adapt_lines:
                 line = rawline.replace("\r", "").strip()
             else:
@@ -97,49 +93,35 @@
     @staticmethod
     @check_arguments
     def string_to_datetime(value: str) -> datetime:
         return datetime.strptime(value, GeneralUtilities.__date_format)  # value ="2022-10-06T19:26:01" for example
 
     @staticmethod
     @check_arguments
-    def copy_content_of_folder(source_directory: str, target_directory: str, overwrite_existing_files=False) -> None:
-        GeneralUtilities.__copy_or_move_content_of_folder(source_directory, target_directory, overwrite_existing_files, False)
-
-    @staticmethod
-    @check_arguments
-    def move_content_of_folder(source_directory: str, target_directory: str, overwrite_existing_files=False) -> None:
-        GeneralUtilities.__copy_or_move_content_of_folder(source_directory, target_directory, overwrite_existing_files, True)
-
-    @staticmethod
-    @check_arguments
-    def __copy_or_move_content_of_folder(source_directory: str, target_directory: str, overwrite_existing_files, remove_source: bool) -> None:
-        srcDirFull = GeneralUtilities.resolve_relative_path_from_current_working_directory(source_directory)
-        dstDirFull = GeneralUtilities.resolve_relative_path_from_current_working_directory(target_directory)
-        if (os.path.isdir(source_directory)):
-            GeneralUtilities.ensure_directory_exists(target_directory)
+    def move_content_of_folder(srcDir, dstDir, overwrite_existing_files=False) -> None:
+        srcDirFull = GeneralUtilities.resolve_relative_path_from_current_working_directory(srcDir)
+        dstDirFull = GeneralUtilities.resolve_relative_path_from_current_working_directory(dstDir)
+        if(os.path.isdir(srcDir)):
+            GeneralUtilities.ensure_directory_exists(dstDir)
             for file in GeneralUtilities.get_direct_files_of_folder(srcDirFull):
                 filename = os.path.basename(file)
                 targetfile = os.path.join(dstDirFull, filename)
-                if (os.path.isfile(targetfile)):
+                if(os.path.isfile(targetfile)):
                     if overwrite_existing_files:
                         GeneralUtilities.ensure_file_does_not_exist(targetfile)
                     else:
                         raise ValueError(f"Targetfile {targetfile} does already exist")
-                if remove_source:
-                    shutil.move(file, dstDirFull)
-                else:
-                    shutil.copy(file, dstDirFull)
+                shutil.move(file, dstDirFull)
             for sub_folder in GeneralUtilities.get_direct_folders_of_folder(srcDirFull):
                 foldername = os.path.basename(sub_folder)
                 sub_target = os.path.join(dstDirFull, foldername)
-                GeneralUtilities.__copy_or_move_content_of_folder(sub_folder, sub_target, overwrite_existing_files, remove_source)
-                if remove_source:
-                    GeneralUtilities.ensure_directory_does_not_exist(sub_folder)
+                GeneralUtilities.move_content_of_folder(sub_folder, sub_target, overwrite_existing_files)
+                GeneralUtilities.ensure_directory_does_not_exist(sub_folder)
         else:
-            raise ValueError(f"Folder '{source_directory}' does not exist")
+            raise ValueError(f"Folder '{srcDir}' does not exist")
 
     @staticmethod
     @check_arguments
     def replace_regex_each_line_of_file(file: str, replace_from_regex: str, replace_to_regex: str, encoding="utf-8", verbose: bool = False) -> None:
         """This function iterates over each line in the file and replaces it by the line which applied regex.
         Note: The lines will be taken from open(...).readlines(). So the lines may contain '\\n' or '\\r\\n' for example."""
         if verbose:
@@ -179,15 +161,15 @@
     def replace_underscores_in_text(text: str, replacements: dict) -> str:
         changed = True
         while changed:
             changed = False
             for key, value in replacements.items():
                 previousValue = text
                 text = text.replace(f"__{key}__", value)
-                if (not text == previousValue):
+                if(not text == previousValue):
                     changed = True
         return text
 
     @staticmethod
     @check_arguments
     def replace_underscores_in_file(file: str, replacements: dict, encoding: str = "utf-8"):
         text = GeneralUtilities.read_text_from_file(file, encoding)
@@ -340,15 +322,15 @@
     def ensure_directory_exists(path: str) -> None:
         if not os.path.isdir(path):
             os.makedirs(path)
 
     @staticmethod
     @check_arguments
     def ensure_file_exists(path: str) -> None:
-        if (not os.path.isfile(path)):
+        if(not os.path.isfile(path)):
             with open(path, "a+", encoding="utf-8"):
                 pass
 
     @staticmethod
     @check_arguments
     def __remove_readonly(func, path, _):
         os.chmod(path, stat.S_IWRITE)
@@ -358,15 +340,15 @@
     @check_arguments
     def rmtree(directory: str) -> None:
         shutil.rmtree(directory, onerror=GeneralUtilities.__remove_readonly)
 
     @staticmethod
     @check_arguments
     def ensure_directory_does_not_exist(path: str) -> None:
-        if (os.path.isdir(path)):
+        if(os.path.isdir(path)):
             for root, dirs, files in os.walk(path, topdown=False):
                 for name in files:
                     filename = os.path.join(root, name)
                     os.chmod(filename, stat.S_IWUSR)
                     os.remove(filename)
                 for name in dirs:
                     GeneralUtilities.rmtree(os.path.join(root, name))
@@ -384,15 +366,15 @@
                 os.unlink(file_path)
             elif os.path.isdir(file_path):
                 shutil.rmtree(file_path)
 
     @staticmethod
     @check_arguments
     def ensure_file_does_not_exist(path: str) -> None:
-        if (os.path.isfile(path)):
+        if(os.path.isfile(path)):
             os.remove(path)
 
     @staticmethod
     @check_arguments
     def format_xml_file(filepath: str) -> None:
         GeneralUtilities.format_xml_file_with_encoding(filepath, "utf-8")
 
@@ -479,15 +461,15 @@
     @check_arguments
     def resolve_relative_path_from_current_working_directory(path: str) -> str:
         return GeneralUtilities.resolve_relative_path(path, os.getcwd())
 
     @staticmethod
     @check_arguments
     def resolve_relative_path(path: str, base_path: str):
-        if (os.path.isabs(path)):
+        if(os.path.isabs(path)):
             return path
         else:
             return str(Path(os.path.join(base_path, path)).resolve())
 
     @staticmethod
     @check_arguments
     def get_metadata_for_file_for_clone_folder_structure(file: str) -> str:
@@ -565,23 +547,23 @@
     def get_all_objects_of_folder(folder: str) -> list[str]:
         return GeneralUtilities.get_all_files_of_folder(folder) + GeneralUtilities.get_all_folders_of_folder(folder)
 
     @staticmethod
     @check_arguments
     def replace_in_filename(file: str, replace_from: str, replace_to: str, replace_only_full_match=False):
         filename = Path(file).name
-        if (GeneralUtilities.__should_get_replaced(filename, replace_from, replace_only_full_match)):
+        if(GeneralUtilities.__should_get_replaced(filename, replace_from, replace_only_full_match)):
             folder_of_file = os.path.dirname(file)
             os.rename(file, os.path.join(folder_of_file, filename.replace(replace_from, replace_to)))
 
     @staticmethod
     @check_arguments
     def replace_in_foldername(folder: str, replace_from: str, replace_to: str, replace_only_full_match=False):
         foldername = Path(folder).name
-        if (GeneralUtilities.__should_get_replaced(foldername, replace_from, replace_only_full_match)):
+        if(GeneralUtilities.__should_get_replaced(foldername, replace_from, replace_only_full_match)):
             folder_of_folder = os.path.dirname(folder)
             os.rename(folder, os.path.join(folder_of_folder, foldername.replace(replace_from, replace_to)))
 
     @staticmethod
     @check_arguments
     def __should_get_replaced(input_text, search_text, replace_only_full_match) -> bool:
         if replace_only_full_match:
@@ -638,17 +620,17 @@
         for line in traceback.format_stack():
             GeneralUtilities.write_message_to_stdout(line.strip())
 
     @staticmethod
     @check_arguments
     def string_to_boolean(value: str) -> bool:
         value = value.strip().lower()
-        if value in ('yes', 'y', 'true', 't', '1'):
+        if value in ('yes', 'true', 't', 'y', '1'):
             return True
-        elif value in ('no', 'n', 'false', 'f', '0'):
+        elif value in ('no', 'false', 'f', 'n', '0'):
             return False
         else:
             raise Exception(f"Can not convert '{value}' to a boolean value")
 
     @staticmethod
     @check_arguments
     def file_is_empty(file: str) -> bool:
@@ -663,15 +645,15 @@
     @check_arguments
     def get_time_based_logfile_by_folder(folder: str, name: str = "Log", in_utc: bool = False) -> str:
         return os.path.join(GeneralUtilities.resolve_relative_path_from_current_working_directory(folder), f"{GeneralUtilities.get_time_based_logfilename(name, in_utc)}.log")
 
     @staticmethod
     @check_arguments
     def get_time_based_logfilename(name: str = "Log", in_utc: bool = False) -> str:
-        if (in_utc):
+        if(in_utc):
             d = datetime.utcnow()
         else:
             d = datetime.now()
         return f"{name}_{GeneralUtilities.datetime_to_string_for_logfile_name(d)}"
 
     @staticmethod
     @check_arguments
@@ -683,15 +665,15 @@
     def string_to_bytes(payload: str, encoding: str = 'utf-8') -> bytes:
         return payload.encode(encoding, errors="ignore")
 
     @staticmethod
     @check_arguments
     def contains_line(lines, regex: str) -> bool:
         for line in lines:
-            if (re.match(regex, line)):
+            if(re.match(regex, line)):
                 return True
         return False
 
     @staticmethod
     @check_arguments
     def read_csv_file(file: str, ignore_first_line: bool = False, treat_number_sign_at_begin_of_line_as_comment: bool = True, trim_values: bool = True,
                       encoding="utf-8", ignore_empty_lines: bool = True, separator_character: str = ";", values_are_surrounded_by_quotes: bool = False) -> list[str]:
@@ -779,43 +761,10 @@
         while square < number:
             root = root+1
             square = root*root
         return root*root
 
     @staticmethod
     @check_arguments
-    def generate_password(length: int = 16, alphabet: str = None) -> None:
-        if alphabet is None:
-            alphabet = strin.ascii_letters + strin.digits+"_"
-        return ''.join(secrets.choice(alphabet) for i in range(length))
-
-    @staticmethod
-    @check_arguments
     def assert_condition(condition: bool, information: str) -> None:
-        if (not condition):
+        if(not condition):
             raise ValueError("Condition failed. "+information)
-
-    @staticmethod
-    @check_arguments
-    def get_certificate_expiry_date(certificate_file: str) -> datetime:
-        with open(certificate_file, encoding="utf-8") as certificate_file_content:
-            cert = crypto.load_certificate(crypto.FILETYPE_PEM, certificate_file_content.read())
-            date_as_bytes = cert.get_notAfter()
-            date_as_string = date_as_bytes.decode("utf-8")
-            result = datetime.strptime(date_as_string, '%Y%m%d%H%M%SZ')
-            return result
-
-    @staticmethod
-    @check_arguments
-    def certificate_is_expired(certificate_file: str) -> bool:
-        return GeneralUtilities.get_certificate_expiry_date(certificate_file) < datetime.now()
-
-    @staticmethod
-    @check_arguments
-    def internet_connection_is_available() -> bool:
-        # TODO add more hosts to check to return true if at least one is available
-        try:
-            with urllib.request.urlopen("https://google.com") as url_result:
-                return (url_result.code // 100) == 2
-        except:
-            pass
-        return False
```

## ScriptCollection/ScriptCollectionCore.py

```diff
@@ -1,35 +1,35 @@
 from datetime import timedelta, datetime
 import binascii
 import filecmp
+import sys
 import hashlib
 from io import BytesIO
 import itertools
 import math
 import os
 from pathlib import Path
 from random import randrange
 from subprocess import Popen
 import re
 import shutil
 import traceback
 import uuid
-import io
 import ntplib
-import qrcode
+from lxml import etree
 import pycdlib
 import send2trash
 from PyPDF2 import PdfFileMerger
 from .GeneralUtilities import GeneralUtilities
 from .ProgramRunnerBase import ProgramRunnerBase
 from .ProgramRunnerPopen import ProgramRunnerPopen
 from .ProgramRunnerEpew import ProgramRunnerEpew, CustomEpewArgument
 
 
-version = "3.3.81"
+version = "3.3.9"
 __version__ = version
 
 
 class ScriptCollectionCore:
 
     # The purpose of this property is to use it when testing your code which uses scriptcollection for external program-calls.
     # Do not change this value for productive environments.
@@ -69,49 +69,56 @@
 
     @GeneralUtilities.check_arguments
     def replace_version_in_dockerfile_file(self, dockerfile: str, new_version_value: str) -> None:
         GeneralUtilities.write_text_to_file(dockerfile, re.sub("ARG Version=\"\\d+\\.\\d+\\.\\d+\"", f"ARG Version=\"{new_version_value}\"",
                                                                GeneralUtilities.read_text_from_file(dockerfile)))
 
     @GeneralUtilities.check_arguments
+    def check_testcoverage(self, testcoverage_file_in_cobertura_format: str, threshold_in_percent: float):
+        root: etree._ElementTree = etree.parse(testcoverage_file_in_cobertura_format)
+        coverage_in_percent = round(float(str(root.xpath('//coverage/@line-rate')[0]))*100, 2)
+        minimalrequiredtestcoverageinpercent = threshold_in_percent
+        if (coverage_in_percent < minimalrequiredtestcoverageinpercent):
+            raise ValueError(f"The testcoverage must be {minimalrequiredtestcoverageinpercent}% or more but is {coverage_in_percent}%.")
+
+    @GeneralUtilities.check_arguments
     def replace_version_in_python_file(self, file: str, new_version_value: str):
         GeneralUtilities.write_text_to_file(file, re.sub("version = \"\\d+\\.\\d+\\.\\d+\"", f"version = \"{new_version_value}\"",
                                                          GeneralUtilities.read_text_from_file(file)))
 
     @GeneralUtilities.check_arguments
-    def replace_version_in_ini_file(self, file: str, new_version_value: str):
-        GeneralUtilities.write_text_to_file(file, re.sub("version = \\d+\\.\\d+\\.\\d+", f"version = {new_version_value}",
+    def replace_version_in_pyproject_file(self, file: str, new_version_value: str):
+        GeneralUtilities.write_text_to_file(file, re.sub("version = \"\\d+\\.\\d+\\.\\d+\"", f"version = \"{new_version_value}\"",
                                                          GeneralUtilities.read_text_from_file(file)))
 
     @GeneralUtilities.check_arguments
-    def replace_version_in_nuspec_file(self, nuspec_file: str, new_version: str) -> None:
-        # TODO use XSLT instead
+    def replace_version_in_nuspec_file(self, nuspec_file: str, current_version: str):
         versionregex = "\\d+\\.\\d+\\.\\d+"
         versiononlyregex = f"^{versionregex}$"
         pattern = re.compile(versiononlyregex)
-        if pattern.match(new_version):
+        if pattern.match(current_version):
             GeneralUtilities.write_text_to_file(nuspec_file, re.sub(f"<version>{versionregex}<\\/version>",
-                                                                    f"<version>{new_version}</version>", GeneralUtilities.read_text_from_file(nuspec_file)))
+                                                                    f"<version>{current_version}</version>", GeneralUtilities.read_text_from_file(nuspec_file)))
         else:
-            raise ValueError(f"Version '{new_version}' does not match version-regex '{versiononlyregex}'")
+            raise ValueError(f"Version '{current_version}' does not match version-regex '{versiononlyregex}'")
 
     @GeneralUtilities.check_arguments
     def replace_version_in_csproj_file(self, csproj_file: str, current_version: str):
         versionregex = "\\d+\\.\\d+\\.\\d+"
         versiononlyregex = f"^{versionregex}$"
         pattern = re.compile(versiononlyregex)
         if pattern.match(current_version):
             for tag in ["Version", "AssemblyVersion", "FileVersion"]:
                 GeneralUtilities.write_text_to_file(csproj_file, re.sub(f"<{tag}>{versionregex}(.\\d+)?<\\/{tag}>",
                                                                         f"<{tag}>{current_version}</{tag}>", GeneralUtilities.read_text_from_file(csproj_file)))
         else:
             raise ValueError(f"Version '{current_version}' does not match version-regex '{versiononlyregex}'")
 
     @GeneralUtilities.check_arguments
-    def push_nuget_build_artifact(self, nupkg_file: str, registry_address: str, api_key: str, verbosity: int = 1):
+    def push_nuget_build_artifact_of_repository_in_common_file_structure(self, nupkg_file: str, registry_address: str, api_key: str, verbosity: int = 1):
         nupkg_file_name = os.path.basename(nupkg_file)
         nupkg_file_folder = os.path.dirname(nupkg_file)
         self.run_program("dotnet", f"nuget push {nupkg_file_name} --force-english-output --source {registry_address} --api-key {api_key}",
                          nupkg_file_folder, verbosity)
 
     @GeneralUtilities.check_arguments
     def dotnet_build(self, repository_folder: str, projectname: str, configuration: str):
@@ -184,33 +191,14 @@
 
     @GeneralUtilities.check_arguments
     def get_parent_commit_ids_of_commit(self, repository_folder: str, commit_id: str) -> str:
         return self.run_program("git", f'log --pretty=%P -n 1 "{commit_id}"',
                                        repository_folder, throw_exception_if_exitcode_is_not_zero=True)[1].replace("\r", "").replace("\n", "").split(" ")
 
     @GeneralUtilities.check_arguments
-    def get_all_authors_and_committers_of_repository(self, repository_folder: str, subfolder: str = None, verbosity: int = 1) -> list[tuple[str, str]]:
-        space_character = "_"
-        if subfolder is None:
-            subfolder_argument = ""
-        else:
-            subfolder_argument = f" -- {subfolder}"
-        log_result = self.run_program("git", f'log --pretty=%aN{space_character}%aE%n%cN{space_character}%cE HEAD{subfolder_argument}',
-                                      repository_folder, verbosity=0)
-        plain_content: list[str] = list(set([line for line in log_result[1].split("\n") if len(line) > 0]))
-        result: list[tuple[str, str]] = []
-        for item in plain_content:
-            if len(re.findall(space_character, item)) == 1:
-                splitted = item.split(space_character)
-                result.append((splitted[0], splitted[1]))
-            else:
-                raise ValueError(f'Unexpected author: "{item}"')
-        return result
-
-    @GeneralUtilities.check_arguments
     def get_commit_ids_between_dates(self, repository_folder: str, since: datetime, until: datetime, ignore_commits_which_are_not_in_history_of_head: bool = True) -> None:
         since_as_string = self.__datetime_to_string_for_git(since)
         until_as_string = self.__datetime_to_string_for_git(until)
         result = filter(lambda line: not GeneralUtilities.string_is_none_or_whitespace(line),
                         self.run_program("git", f'log --since "{since_as_string}" --until "{until_as_string}" --pretty=format:"%H" --no-patch',
                                          repository_folder, throw_exception_if_exitcode_is_not_zero=True)[1].split("\n").replace("\r", ""))
         if ignore_commits_which_are_not_in_history_of_head:
@@ -219,22 +207,15 @@
 
     @GeneralUtilities.check_arguments
     def __datetime_to_string_for_git(self, datetime_object: datetime) -> str:
         return datetime_object.strftime('%Y-%m-%d %H:%M:%S')
 
     @GeneralUtilities.check_arguments
     def git_commit_is_ancestor(self, repository_folder: str,  ancestor: str, descendant: str = "HEAD") -> bool:
-        exit_code = self.run_program_argsasarray("git", ["merge-base", "--is-ancestor", ancestor, descendant],
-                                                 repository_folder, throw_exception_if_exitcode_is_not_zero=False)[0]
-        if exit_code == 0:
-            return True
-        elif exit_code == 1:
-            return False
-        else:
-            raise ValueError(f"Can not calculate if {ancestor} is an ancestor of {descendant} in repository {repository_folder}.")
+        return self.run_program_argsasarray("git", ["merge-base", "--is-ancestor", ancestor, descendant], repository_folder, throw_exception_if_exitcode_is_not_zero=False)[0] == 0
 
     @GeneralUtilities.check_arguments
     def __git_changes_helper(self, repository_folder: str, arguments_as_array: list[str]) -> bool:
         lines = GeneralUtilities.string_to_lines(self.run_program_argsasarray("git", arguments_as_array, repository_folder,
                                                  throw_exception_if_exitcode_is_not_zero=True, verbosity=0)[1], False)
         for line in lines:
             if GeneralUtilities.string_has_content(line):
@@ -266,28 +247,20 @@
         if (self.git_repository_has_unstaged_changes_of_tracked_files(repository_folder)):
             return True
         if (self.git_repository_has_new_untracked_files(repository_folder)):
             return True
         return False
 
     @GeneralUtilities.check_arguments
-    def git_get_commit_id(self, repository_folder: str, commit: str = "HEAD") -> str:
+    def git_get_current_commit_id(self, repository_folder: str, commit: str = "HEAD") -> str:
         result: tuple[int, str, str, int] = self.run_program_argsasarray("git", ["rev-parse", "--verify", commit],
                                                                          repository_folder, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
         return result[1].replace('\n', '')
 
     @GeneralUtilities.check_arguments
-    def git_get_commit_date(self, repository_folder: str, commit: str = "HEAD") -> datetime:
-        result: tuple[int, str, str, int] = self.run_program_argsasarray("git", ["show", "-s", "--format=%ci", commit],
-                                                                         repository_folder, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
-        date_as_string = result[1].replace('\n', '')
-        result = datetime.strptime(date_as_string, '%Y-%m-%d %H:%M:%S %z')
-        return result
-
-    @GeneralUtilities.check_arguments
     def git_fetch(self, folder: str, remotename: str = "--all") -> None:
         self.run_program_argsasarray("git", ["fetch", remotename, "--tags", "--prune"], folder, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
     @GeneralUtilities.check_arguments
     def git_fetch_in_bare_repository(self, folder: str, remotename, localbranch: str, remotebranch: str) -> None:
         self.run_program_argsasarray("git", ["fetch", remotename, f"{remotebranch}:{localbranch}"], folder, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
@@ -390,33 +363,28 @@
             if no_changes_behavior == 2:
                 raise RuntimeError(f"There are no changes to commit in repository '{directory}'. Commit '{message}' will not be done.")
 
         if do_commit:
             GeneralUtilities.write_message_to_stdout(f"Commit changes in '{directory}'")
             self.run_program_argsasarray("git", argument, directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
-        return self.git_get_commit_id(directory)
+        return self.git_get_current_commit_id(directory)
 
     @GeneralUtilities.check_arguments
     def git_create_tag(self, directory: str, target_for_tag: str, tag: str, sign: bool = False, message: str = None) -> None:
         argument = ["tag", tag, target_for_tag]
         if sign:
             if message is None:
                 message = f"Created {target_for_tag}"
             argument.extend(["-s", '-m', message])
         self.run_program_argsasarray("git", argument, directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
     @GeneralUtilities.check_arguments
-    def git_delete_tag(self, directory: str, tag: str) -> None:
-        self.run_program_argsasarray("git", ["tag", "--delete", tag], directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
-
-    @GeneralUtilities.check_arguments
     def git_checkout(self, directory: str, branch: str) -> None:
         self.run_program_argsasarray("git", ["checkout", branch], directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
-        self.run_program_argsasarray("git", ["submodule", "update", "--recursive"], directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
     @GeneralUtilities.check_arguments
     def git_merge_abort(self, directory: str) -> None:
         self.run_program_argsasarray("git", ["merge", "--abort"], directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
 
     @GeneralUtilities.check_arguments
     def git_merge(self, directory: str, sourcebranch: str, targetbranch: str, fastforward: bool = True, commit: bool = True, commit_message: str = None) -> str:
@@ -427,15 +395,15 @@
         if not fastforward:
             args.append("--no-ff")
         if commit_message is not None:
             args.append("-m")
             args.append(commit_message)
         args.append(sourcebranch)
         self.run_program_argsasarray("git", args, directory, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
-        return self.git_get_commit_id(directory)
+        return self.git_get_current_commit_id(directory)
 
     @GeneralUtilities.check_arguments
     def git_undo_all_changes(self, directory: str) -> None:
         """Caution: This function executes 'git clean -df'. This can delete files which maybe should not be deleted. Be aware of that."""
         self.git_unstage_all_changes(directory)
         self.git_discard_all_unstaged_changes(directory)
 
@@ -475,58 +443,14 @@
 
     @GeneralUtilities.check_arguments
     def git_get_current_branch_name(self, repository: str) -> str:
         result = self.run_program_argsasarray("git", ["rev-parse", "--abbrev-ref", "HEAD"], repository, throw_exception_if_exitcode_is_not_zero=True, verbosity=0)
         return result[1].replace("\r", "").replace("\n", "")
 
     @GeneralUtilities.check_arguments
-    def git_get_commitid_of_tag(self, repository: str, tag: str) -> str:
-        stdout = self.run_program_argsasarray("git", ["rev-list", "-n", "1", tag], repository, verbosity=0)
-        result = stdout[1].replace("\r", "").replace("\n", "")
-        return result
-
-    @GeneralUtilities.check_arguments
-    def git_get_tags(self, repository: str) -> list[str]:
-        tags = [line for line in self.run_program_argsasarray("git", ["tag"], repository)[1].split("\n") if len(line) > 0]
-        return tags
-
-    @GeneralUtilities.check_arguments
-    def git_move_tags_to_another_branch(self, repository: str, tag_source_branch: str, tag_target_branch: str,
-                                        sign: bool = False, message: str = None) -> None:
-        tags = self.git_get_tags(repository)
-        tags_count = len(tags)
-        counter = 0
-        for tag in tags:
-            counter = counter+1
-            GeneralUtilities.write_message_to_stdout(f"Process tag {counter}/{tags_count}.")
-            if self.git_commit_is_ancestor(repository, tag, tag_source_branch):  # tag is on source-branch
-                commit_id_old = self.git_get_commitid_of_tag(repository, tag)
-                commit_date: datetime = self.git_get_commit_date(repository, commit_id_old)
-                date_as_string = self.__datetime_to_string_for_git(commit_date)
-                search_commit_result = self.run_program_argsasarray("git", ["log", f'--after="{date_as_string}"', f'--before="{date_as_string}"',
-                                                                            "--pretty=format:%H", tag_target_branch], repository,
-                                                                    throw_exception_if_exitcode_is_not_zero=False)
-                if search_commit_result[0] != 0 or not GeneralUtilities.string_has_nonwhitespace_content(search_commit_result[1]):
-                    raise ValueError(f"Can not calculate corresponding commit for tag '{tag}'.")
-                commit_id_new = search_commit_result[1]
-                self.git_delete_tag(repository, tag)
-                self.git_create_tag(repository, commit_id_new, tag, sign, message)
-
-    @GeneralUtilities.check_arguments
-    def get_current_branch_has_tag(self, repository_folder: str) -> str:
-        result = self.run_program_argsasarray("git", ["describe", "--tags", "--abbrev=0"], repository_folder, verbosity=0)
-        return result[0] == 0
-
-    @GeneralUtilities.check_arguments
-    def get_latest_tag(self, repository_folder: str) -> str:
-        result = self.run_program_argsasarray("git", ["describe", "--tags", "--abbrev=0"], repository_folder, verbosity=0)
-        result = result[1].replace("\r", "").replace("\n", "")
-        return result
-
-    @GeneralUtilities.check_arguments
     def export_filemetadata(self, folder: str, target_file: str, encoding: str = "utf-8", filter_function=None) -> None:
         folder = GeneralUtilities.resolve_relative_path_from_current_working_directory(folder)
         lines = list()
         path_prefix = len(folder)+1
         items = dict()
         for item in GeneralUtilities.get_all_folders_of_folder(folder):
             items[item] = "d"
@@ -835,27 +759,20 @@
             self.__check_file(file, searchstring)
 
     @GeneralUtilities.check_arguments
     def __print_qr_code_by_csv_line(self, displayname: str, website: str, emailaddress: str, key: str, period: str) -> None:
         qrcode_content = f"otpauth://totp/{website}:{emailaddress}?secret={key}&issuer={displayname}&period={period}"
         GeneralUtilities.write_message_to_stdout(f"{displayname} ({emailaddress}):")
         GeneralUtilities.write_message_to_stdout(qrcode_content)
-        qr = qrcode.QRCode()
-        qr.add_data(qrcode_content)
-        f = io.StringIO()
-        qr.print_ascii(out=f)
-        f.seek(0)
-        GeneralUtilities.write_message_to_stdout(f.read())
+        self.run_program("qr", qrcode_content)
 
     @GeneralUtilities.check_arguments
     def SCShow2FAAsQRCode(self, csvfile: str) -> None:
         separator_line = "--------------------------------------------------------"
-        lines = GeneralUtilities.read_csv_file(csvfile, True)
-        lines.sort(key=lambda items: ''.join(items).lower())
-        for line in lines:
+        for line in GeneralUtilities.read_csv_file(csvfile, True):
             GeneralUtilities.write_message_to_stdout(separator_line)
             self.__print_qr_code_by_csv_line(line[0], line[1], line[2], line[3], line[4])
         GeneralUtilities.write_message_to_stdout(separator_line)
 
     @GeneralUtilities.check_arguments
     def SCUpdateNugetpackagesInCsharpProject(self, csprojfile: str) -> int:
         outdated_packages = self.get_nuget_packages_of_csproj_file(csprojfile, True)
@@ -1186,18 +1103,19 @@
         cmd = f'{working_directory}>{program} {arguments_for_log}'
 
         if GeneralUtilities.string_is_none_or_whitespace(title):
             info_for_log = cmd
         else:
             info_for_log = title
 
-        if verbosity >= 3:
+        if verbosity == 3:
             GeneralUtilities.write_message_to_stdout(f"Run '{info_for_log}'.")
 
         if isinstance(self.program_runner, ProgramRunnerEpew):
+            GeneralUtilities.write_message_to_stdout("Using epew.")
             custom_argument = CustomEpewArgument(print_errors_as_information, log_file, timeoutInSeconds, addLogOverhead, title, log_namespace, verbosity, arguments_for_log)
         popen: Popen = self.program_runner.run_program_argsasarray_async_helper(program, arguments_as_array, working_directory, custom_argument)
         return popen
 
     # Return-values program_runner: Exitcode, StdOut, StdErr, Pid
 
     @GeneralUtilities.check_arguments
@@ -1205,59 +1123,50 @@
                                 print_errors_as_information: bool = False, log_file: str = None, timeoutInSeconds: int = 600, addLogOverhead: bool = False,
                                 title: str = None, log_namespace: str = "", arguments_for_log:  list[str] = None,
                                 throw_exception_if_exitcode_is_not_zero: bool = True, custom_argument: object = None) -> tuple[int, str, str, int]:
         mock_loader_result = self.__try_load_mock(program, ' '.join(arguments_as_array), working_directory)
         if mock_loader_result[0]:
             return mock_loader_result[1]
 
-        if arguments_for_log is None:
-            arguments_for_log = arguments_as_array
+        start_datetime = datetime.utcnow()
 
-        arguments_for_log_as_string = ' '.join(arguments_for_log)
-        cmd = f'{working_directory}>{program} {arguments_for_log_as_string}'
+        cmd = f'{working_directory}>{program} {arguments_for_log}'
         if GeneralUtilities.string_is_none_or_whitespace(title):
             info_for_log = cmd
         else:
             info_for_log = title
+        if verbosity == 3:
+            GeneralUtilities.write_message_to_stdout(f"Run '{info_for_log}'.")
 
         epew_will_be_used = isinstance(self.program_runner, ProgramRunnerEpew)
-        program_manages_output_itself = epew_will_be_used and False  # TODO fix stdout-/stderr-reading-block below
         program_manages_logging_itself = epew_will_be_used
+        program_manages_output_itself = epew_will_be_used
 
         process = self.__run_program_argsasarray_async_helper(program, arguments_as_array, working_directory, verbosity, print_errors_as_information, log_file,
                                                               timeoutInSeconds, addLogOverhead, title, log_namespace, arguments_for_log, custom_argument)
         pid = process.pid
 
         if program_manages_output_itself:
-            stdout_readable = process.stdout.readable()
-            stderr_readable = process.stderr.readable()
-            while stdout_readable or stderr_readable:
-
-                if stdout_readable:
-                    stdout_line = GeneralUtilities.bytes_to_string(process.stdout.readline()).strip()
-                    if (len(stdout_line)) > 0:
-                        GeneralUtilities.write_message_to_stdout(stdout_line)
-
-                if stderr_readable:
-                    stderr_line = GeneralUtilities.bytes_to_string(process.stderr.readline()).strip()
-                    if (len(stderr_line)) > 0:
-                        GeneralUtilities.write_message_to_stderr(stderr_line)
-
-                stdout_readable = process.stdout.readable()
-                stderr_readable = process.stderr.readable()
+            for c in iter(lambda: process.stdout.read(1), b""):
+                sys.stdout.buffer.write(c)
+            for c in iter(lambda: process.stderr.read(1), b""):
+                sys.stderr.buffer.write(c)
 
         stdout, stderr = process.communicate()
         exit_code = process.wait()
         stdout = GeneralUtilities.bytes_to_string(stdout).replace('\r', '')
         stderr = GeneralUtilities.bytes_to_string(stderr).replace('\r', '')
+        end_datetime = datetime.utcnow()
 
-        if arguments_for_log_as_string is None:
-            arguments_for_log_as_string = ' '.join(arguments_as_array)
+        if arguments_for_log is None:
+            arguments_for_log = ' '.join(arguments_as_array)
         else:
-            arguments_for_log_as_string = ' '.join(arguments_for_log)
+            arguments_for_log = ' '.join(arguments_for_log)
+
+        duration: timedelta = end_datetime-start_datetime
 
         if GeneralUtilities.string_is_none_or_whitespace(title):
             info_for_log = cmd
         else:
             info_for_log = title
 
         if not program_manages_logging_itself and log_file is not None:
@@ -1270,21 +1179,20 @@
                 self.__write_error_output(print_errors_as_information, stderr)
             if verbosity == 2:
                 GeneralUtilities.write_message_to_stdout(stdout)
                 self.__write_error_output(print_errors_as_information, stderr)
             if verbosity == 3:
                 GeneralUtilities.write_message_to_stdout(stdout)
                 self.__write_error_output(print_errors_as_information, stderr)
-                formatted = self.__format_program_execution_information(title=info_for_log, program=program,
-                                                                        argument=arguments_for_log_as_string, workingdirectory=working_directory)
+                formatted = self.__format_program_execution_information(title=info_for_log, program=program, argument=arguments_for_log, workingdirectory=working_directory)
                 GeneralUtilities.write_message_to_stdout(f"Finished '{info_for_log}'. Details: '{formatted}")
 
         if throw_exception_if_exitcode_is_not_zero and exit_code != 0:
-            arguments_for_log_as_string = ' '.join(arguments_for_log)
-            raise ValueError(f"Program '{working_directory}>{program} {arguments_for_log_as_string}' resulted in exitcode {exit_code}. (StdOut: '{stdout}', StdErr: '{stderr}')")
+            formatted = self.__format_program_execution_information(exit_code, stdout, stderr, program, arguments_for_log, working_directory, info_for_log, pid, duration)
+            raise ValueError(f"Finished '{info_for_log}'. Details: '{formatted}")
 
         result = (exit_code, stdout, stderr, pid)
         return result
 
     # Return-values program_runner: Exitcode, StdOut, StdErr, Pid
     @GeneralUtilities.check_arguments
     def run_program(self, program: str, arguments:  str = "", working_directory: str = None, verbosity: int = 1,
@@ -1447,106 +1355,16 @@
         self.check_system_time(self.__get_default_tolerance_for_system_time_equals_internet_time())
 
     @GeneralUtilities.check_arguments
     def __get_default_tolerance_for_system_time_equals_internet_time(self) -> timedelta:
         return timedelta(hours=0, minutes=0, seconds=3)
 
     @GeneralUtilities.check_arguments
-    def increment_version(self, input_version: str, increment_major: bool, increment_minor: bool, increment_patch: bool) -> str:
-        splitted = input_version.split(".")
-        GeneralUtilities.assert_condition(len(splitted) == 3, f"Version '{input_version}' does not have the 'major.minor.patch'-pattern.")
-        major = int(splitted[0])
-        minor = int(splitted[1])
-        patch = int(splitted[2])
-        if increment_major:
-            major = major+1
-        if increment_minor:
-            minor = minor+1
-        if increment_patch:
-            patch = patch+1
-        return f"{major}.{minor}.{patch}"
-
-    @GeneralUtilities.check_arguments
-    def get_semver_version_from_gitversion(self, repository_folder: str) -> str:
-        result = self.get_version_from_gitversion(repository_folder, "MajorMinorPatch")
-
-        try:
-            if self.git_repository_has_uncommitted_changes(repository_folder):
-                if self.get_current_branch_has_tag(repository_folder):
-                    tag_of_latest_tag = self.git_get_commitid_of_tag(repository_folder, self.get_latest_tag(repository_folder))
-                    current_commit = self.git_get_commit_id(repository_folder)
-                    current_commit_is_on_latest_tag = tag_of_latest_tag == current_commit
-                    if current_commit_is_on_latest_tag:
-                        result = self.increment_version(result, False, False, True)
-        except:#Exceptions are thrown for example when no tags are available. but these cases should be ignored.
-            pass
-
-        return result
+    def get_semver_version_from_gitversion(self, folder: str) -> str:
+        return self.get_version_from_gitversion(folder, "MajorMinorPatch")
 
     @GeneralUtilities.check_arguments
     def get_version_from_gitversion(self, folder: str, variable: str) -> str:
         # called twice as workaround for issue 1877 in gitversion ( https://github.com/GitTools/GitVersion/issues/1877 )
         result = self.run_program_argsasarray("gitversion", ["/showVariable", variable], folder)
         result = self.run_program_argsasarray("gitversion", ["/showVariable", variable], folder)
-        result = GeneralUtilities.strip_new_line_character(result[1])
-
-        return result
-
-    @GeneralUtilities.check_arguments
-    def generate_certificate_authority(self, folder: str, name: str, subj_c: str, subj_st: str, subj_l: str, subj_o: str, subj_ou: str,
-                                       days_until_expire: int = None, password: str = None) -> None:
-        if days_until_expire is None:
-            days_until_expire = 1825
-        if password is None:
-            password = GeneralUtilities.generate_password()
-        self.run_program("openssl", f'req -new -newkey ec -pkeyopt ec_paramgen_curve:prime256v1 -days {days_until_expire} -nodes -x509 -subj ' +
-                         f'/C={subj_c}/ST={subj_st}/L={subj_l}/O={subj_o}/CN={name}/OU={subj_ou} -passout pass:{password} ' +
-                         f'-keyout {name}.key -out {name}.crt', folder)
-
-    @GeneralUtilities.check_arguments
-    def generate_certificate(self, folder: str, domain: str, subj_c: str, subj_st: str, subj_l: str, subj_o: str, subj_ou: str,
-                             days_until_expire: int = None, password: str = None) -> None:
-        if days_until_expire is None:
-            days_until_expire = 397
-        if password is None:
-            password = GeneralUtilities.generate_password()
-        rsa_key_length = 4096
-        self.run_program("openssl", f'genrsa -out {domain}.key {rsa_key_length}', folder)
-        self.run_program("openssl", f'req -new -subj /C={subj_c}/ST={subj_st}/L={subj_l}/O={subj_o}/CN={domain}/OU={subj_ou} -x509 ' +
-                         f'-key {domain}.key -out {domain}.unsigned.crt -days {days_until_expire}', folder)
-        self.run_program("openssl", f'pkcs12 -export -out {domain}.pfx -password pass:{password} -inkey {domain}.key -in {domain}.unsigned.crt', folder)
-        GeneralUtilities.write_text_to_file(os.path.join(folder, f"{domain}.password"), password)
-        GeneralUtilities.write_text_to_file(os.path.join(folder, f"{domain}.san.conf"), f"""[ req ]
-default_bits        = {rsa_key_length}
-distinguished_name  = req_distinguished_name
-req_extensions      = v3_req
-default_md          = sha256
-dirstring_type      = nombstr
-prompt              = no
-
-[ req_distinguished_name ]
-countryName         = {subj_c}
-stateOrProvinceName = {subj_st}
-localityName        = {subj_l}
-organizationName    = {subj_o}
-organizationUnit    = {subj_ou}
-commonName          = {domain}
-
-[v3_req]
-subjectAltName      = @subject_alt_name
-
-[ subject_alt_name ]
-DNS                 = {domain}
-""")
-
-    @GeneralUtilities.check_arguments
-    def generate_certificate_sign_request(self, folder: str, domain: str, subj_c: str, subj_st: str, subj_l: str, subj_o: str, subj_ou: str) -> None:
-        self.run_program("openssl", f'req -new -subj /C={subj_c}/ST={subj_st}/L={subj_l}/O={subj_o}/CN={domain}/OU={subj_ou} ' +
-                         f'-key {domain}.key -out {domain}.csr -config {domain}.san.conf', folder)
-
-    @GeneralUtilities.check_arguments
-    def sign_certificate(self, folder: str, ca_folder: str, ca_name: str, domain: str, days_until_expire: int = None) -> None:
-        if days_until_expire is None:
-            days_until_expire = 397
-        ca = os.path.join(ca_folder, ca_name)
-        self.run_program("openssl", f'x509 -req -in {domain}.csr -CA {ca}.crt -CAkey {ca}.key -CAserial {ca}.srl ' +
-                         f'-out {domain}.crt -days {days_until_expire} -sha256 -extensions v3_req -extfile {domain}.san.conf', folder)
+        return GeneralUtilities.strip_new_line_character(result[1])
```

## ScriptCollection/TasksForCommonProjectStructure.py

```diff
@@ -1,183 +1,153 @@
 from datetime import datetime
-from graphlib import TopologicalSorter
 import os
 from pathlib import Path
 import shutil
 import re
-import urllib.request
-import zipfile
 import json
 import configparser
 import xmlschema
-from OpenSSL import crypto
 from lxml import etree
 from .GeneralUtilities import GeneralUtilities
 from .ScriptCollectionCore import ScriptCollectionCore
 from .ProgramRunnerEpew import ProgramRunnerEpew
 
 
+class CodeUnitConfiguration():
+    name: str
+    push_to_registry_script: str
+    additional_arguments_file: str
+
+    def __init__(self, name: str, push_to_registry_script: str, additional_arguments_file: str):
+
+        self.name = name
+        self.push_to_registry_script = push_to_registry_script
+        self.additional_arguments_file = additional_arguments_file
+
+
 class CreateReleaseConfiguration():
     projectname: str
     remotename: str
     artifacts_folder: str
-    push_artifacts_scripts_folder: str
+    codeunits: dict[str, CodeUnitConfiguration]
     verbosity: int
     reference_repository_remote_name: str = None
     reference_repository_branch_name: str = "main"
     build_repository_branch: str = "main"
     public_repository_url: str
-    additional_arguments_file: str = None
-    artifacts_which_have_artifacts_to_push: list[str] = None
-    repository_folder_name: str = None
-
-    def __init__(self, projectname: str, remotename: str, build_artifacts_target_folder: str, push_artifacts_scripts_folder: str,
-                 verbosity: int, public_repository_url: str, additional_arguments_file: str, artifacts_which_have_artifacts_to_push: list[str],
-                 repository_folder_name: str):
+
+    def __init__(self, projectname: str, remotename: str, build_artifacts_target_folder: str, codeunits: dict[str, CodeUnitConfiguration],
+                 verbosity: int, public_repository_url: str):
 
         self.projectname = projectname
         self.remotename = remotename
         self.artifacts_folder = build_artifacts_target_folder
-        self.push_artifacts_scripts_folder = push_artifacts_scripts_folder
+        self.codeunits = codeunits
         self.verbosity = verbosity
         self.public_repository_url = public_repository_url
         self.reference_repository_remote_name = self.remotename
-        self.additional_arguments_file = additional_arguments_file
-        self.artifacts_which_have_artifacts_to_push = artifacts_which_have_artifacts_to_push
-        self.repository_folder_name = repository_folder_name
 
 
 class CreateReleaseInformationForProjectInCommonProjectFormat:
     projectname: str
     repository: str
     artifacts_folder: str
     verbosity: int = 1
     reference_repository: str = None
     public_repository_url: str = None
     target_branch_name: str = None
-    push_artifacts_scripts_folder: str = None
-    target_environmenttype_for_qualitycheck: str = "QualityCheck"
-    target_environmenttype_for_productive: str = "Productive"
-    additional_arguments_file: str = None
-    export_target: str = None
-    artifacts_which_have_artifacts_to_push: list[str] = None
+    codeunits: dict[str, CodeUnitConfiguration]
+    build_environment_for_qualitycheck: str = "QualityCheck"
+    build_environment_for_productive: str = "Productive"
 
-    def __init__(self, repository: str, artifacts_folder: str, projectname: str, public_repository_url: str, target_branch_name: str,
-                 additional_arguments_file: str, export_target: str, push_artifacts_scripts_folder: str, artifacts_which_have_artifacts_to_push: list[str]):
+    def __init__(self, repository: str, artifacts_folder: str, projectname: str, public_repository_url: str, target_branch_name: str):
         self.repository = repository
         self.public_repository_url = public_repository_url
         self.target_branch_name = target_branch_name
         self.artifacts_folder = artifacts_folder
-        self.additional_arguments_file = additional_arguments_file
-        self.export_target = export_target
-        self.push_artifacts_scripts_folder = push_artifacts_scripts_folder
         if projectname is None:
             projectname = os.path.basename(self.repository)
         else:
             self.projectname = projectname
-        self.reference_repository = f"{repository}Reference"
-        self.artifacts_which_have_artifacts_to_push = artifacts_which_have_artifacts_to_push
+        self.reference_repository = GeneralUtilities.resolve_relative_path(f"../{projectname}Reference", repository)
 
 
 class MergeToStableBranchInformationForProjectInCommonProjectFormat:
     repository: str
     sourcebranch: str = "main"
     targetbranch: str = "stable"
     sign_git_tags: bool = True
-    target_environmenttype_for_qualitycheck: str = "QualityCheck"
-    target_environmenttype_for_productive: str = "Productive"
-    additional_arguments_file: str = None
-    export_target: str = None
+    codeunits: dict[str, CodeUnitConfiguration]
+    build_environment_for_qualitycheck: str = "QualityCheck"
+    build_environment_for_productive: str = "Productive"
 
     push_source_branch: bool = False
     push_source_branch_remote_name: str = None
     push_target_branch: bool = False
     push_target_branch_remote_name: str = None
 
     verbosity: int = 1
 
-    def __init__(self, repository: str, additional_arguments_file: str, export_target: str):
+    def __init__(self, repository: str):
         self.repository = repository
-        self.additional_arguments_file = additional_arguments_file
-        self.export_target = export_target
 
 
 class TasksForCommonProjectStructure:
     __sc: ScriptCollectionCore = None
-    reference_latest_version_of_xsd_when_generating_xml: bool = True
-    validate_developers_of_repository: bool = True
-    dotnet_runsettings_file = "runsettings.xml"
-
-    @staticmethod
-    @GeneralUtilities.check_arguments
-    def get_development_environment_name() -> str:
-        return "Development"
-
-    @staticmethod
-    @GeneralUtilities.check_arguments
-    def get_qualitycheck_environment_name() -> str:
-        return "QualityCheck"
-
-    @staticmethod
-    @GeneralUtilities.check_arguments
-    def get_productive_environment_name() -> str:
-        return "Productive"
 
     def __init__(self, sc: ScriptCollectionCore = None):
         if sc is None:
             sc = ScriptCollectionCore()
         self.__sc = sc
 
     @GeneralUtilities.check_arguments
-    def get_build_folder(self, repository_folder: str, codeunit_name: str) -> str:
+    def get_build_folder_in_repository_in_common_repository_format(self, repository_folder: str, codeunit_name: str) -> str:
         return os.path.join(repository_folder, codeunit_name, "Other", "Build")
 
     @GeneralUtilities.check_arguments
-    def get_artifacts_folder(self, repository_folder: str, codeunit_name: str) -> str:
+    def get_artifacts_folder_in_repository_in_common_repository_format(self, repository_folder: str, codeunit_name: str) -> str:
         return os.path.join(repository_folder, codeunit_name, "Other", "Artifacts")
 
     @GeneralUtilities.check_arguments
-    def get_wheel_file(self, repository_folder: str, codeunit_name: str) -> str:
-        return self.__sc.find_file_by_extension(os.path.join(self.get_artifacts_folder(repository_folder, codeunit_name),
+    def get_wheel_file_in_repository_in_common_repository_format(self, repository_folder: str, codeunit_name: str) -> str:
+        return self.__sc.find_file_by_extension(os.path.join(self.get_artifacts_folder_in_repository_in_common_repository_format(repository_folder, codeunit_name),
                                                              "BuildResult_Wheel"), "whl")
 
     @GeneralUtilities.check_arguments
-    def get_testcoverage_threshold_from_codeunit_file(self, codeunit_file):
+    def __get_testcoverage_threshold_from_codeunit_file(self, codeunit_file):
         root: etree._ElementTree = etree.parse(codeunit_file)
-        return float(str(root.xpath('//cps:minimalcodecoverageinpercent/text()', namespaces={
-            'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure'
-        })[0]))
+        return float(str(root.xpath('//codeunit:minimalcodecoverageinpercent/text()', namespaces={'codeunit': 'https://github.com/anionDev/ProjectTemplates'})[0]))
 
     @GeneralUtilities.check_arguments
-    def codeunit_hast_testable_sourcecode(self, codeunit_file) -> bool:
-        root: etree._ElementTree = etree.parse(codeunit_file)
-        return GeneralUtilities.string_to_boolean(str(root.xpath('//cps:properties/@codeunithastestablesourcecode', namespaces={
-            'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure'
-        })[0]))
-
-    @GeneralUtilities.check_arguments
-    def check_testcoverage(self, testcoverage_file_in_cobertura_format: str, repository_folder: str, codeunitname: str):
+    def check_testcoverage_for_project_in_common_project_structure(self, testcoverage_file_in_cobertura_format: str, repository_folder: str, codeunitname: str):
         root: etree._ElementTree = etree.parse(testcoverage_file_in_cobertura_format)
-        # TODO check if there is at least one package in testcoverage_file_in_cobertura_format
         coverage_in_percent = round(float(str(root.xpath('//coverage/@line-rate')[0]))*100, 2)
         codeunit_file = os.path.join(repository_folder, codeunitname, f"{codeunitname}.codeunit.xml")
-        minimalrequiredtestcoverageinpercent = self.get_testcoverage_threshold_from_codeunit_file(codeunit_file)
-        minimalrecommendedcoverage = 80
-        if minimalrequiredtestcoverageinpercent < minimalrecommendedcoverage:
-            GeneralUtilities.write_message_to_stderr(f"Warning: The minimal required testcoverage is {minimalrequiredtestcoverageinpercent}% " +
-                                                     f"but should be at least {minimalrecommendedcoverage}%.")
-        # TODO check that testcoverage_file_in_cobertura_format contains at least one package with at least one line of code
-        if (coverage_in_percent < minimalrequiredtestcoverageinpercent):
-            raise ValueError(f"The testcoverage for codeunit {codeunitname} must be {minimalrequiredtestcoverageinpercent}% or more but is {coverage_in_percent}%.")
+        threshold_in_percent = self.__get_testcoverage_threshold_from_codeunit_file(codeunit_file)
+        minimalrequiredtestcoverageinpercent = threshold_in_percent
+        if(coverage_in_percent < minimalrequiredtestcoverageinpercent):
+            raise ValueError(f"The testcoverage must be {minimalrequiredtestcoverageinpercent}% or more but is {coverage_in_percent}%.")
 
     @GeneralUtilities.check_arguments
     def replace_version_in_python_file(self, file: str, new_version_value: str):
         GeneralUtilities.write_text_to_file(file, re.sub("version = \"\\d+\\.\\d+\\.\\d+\"", f"version = \"{new_version_value}\"",
                                                          GeneralUtilities.read_text_from_file(file)))
 
+    @GeneralUtilities.check_arguments
+    def __standardized_tasks_run_testcases_for_python_codeunit(self, repository_folder: str, codeunitname: str, verbosity: int):
+        codeunit_folder = os.path.join(repository_folder, codeunitname)
+        self.__sc.run_program("coverage", "run -m pytest", codeunit_folder,  verbosity=verbosity)
+        self.__sc.run_program("coverage", "xml", codeunit_folder, verbosity=verbosity)
+        coveragefolder = os.path.join(repository_folder, codeunitname, "Other/Artifacts/TestCoverage")
+        GeneralUtilities.ensure_directory_exists(coveragefolder)
+        coveragefile = os.path.join(coveragefolder, "TestCoverage.xml")
+        GeneralUtilities.ensure_file_does_not_exist(coveragefile)
+        os.rename(os.path.join(repository_folder, codeunitname, "coverage.xml"), coveragefile)
+        self.check_testcoverage_for_project_in_common_project_structure(coveragefile, repository_folder, codeunitname)
+
     @staticmethod
     @GeneralUtilities.check_arguments
     def __adjust_source_in_testcoverage_file(testcoverage_file: str, codeunitname: str) -> None:
         GeneralUtilities.write_text_to_file(testcoverage_file, re.sub("<source>.+<\\/source>", f"<source>{codeunitname}</source>",
                                                                       GeneralUtilities.read_text_from_file(testcoverage_file)))
 
     @staticmethod
@@ -185,65 +155,35 @@
     def update_path_of_source(repository_folder: str, codeunitname: str) -> None:
         folder = f"{repository_folder}/{codeunitname}/Other/Artifacts/TestCoverage"
         filename = "TestCoverage.xml"
         full_file = os.path.join(folder, filename)
         TasksForCommonProjectStructure.__adjust_source_in_testcoverage_file(full_file, codeunitname)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_run_testcases_for_python_codeunit(self, run_testcases_file: str, generate_badges: bool, verbosity: int,
-                                                             targetenvironmenttype: str, commandline_arguments: list[str]):
+    def standardized_tasks_run_testcases_for_python_codeunit_in_common_project_structure(self, run_testcases_file: str, generate_badges: bool, verbosity: int, buildenvironment: str,
+                                                                                         commandline_arguments: list[str]):
         codeunitname: str = Path(os.path.dirname(run_testcases_file)).parent.parent.name
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         repository_folder: str = str(Path(os.path.dirname(run_testcases_file)).parent.parent.parent.absolute())
-        codeunit_folder = os.path.join(repository_folder, codeunitname)
-        self.__sc.run_program("coverage", f"run -m pytest ./{codeunitname}Tests", codeunit_folder,  verbosity=verbosity)
-        self.__sc.run_program("coverage", "xml", codeunit_folder, verbosity=verbosity)
-        coveragefolder = os.path.join(repository_folder, codeunitname, "Other/Artifacts/TestCoverage")
-        GeneralUtilities.ensure_directory_exists(coveragefolder)
-        coveragefile = os.path.join(coveragefolder, "TestCoverage.xml")
-        GeneralUtilities.ensure_file_does_not_exist(coveragefile)
-        os.rename(os.path.join(repository_folder, codeunitname, "coverage.xml"), coveragefile)
+        self.__standardized_tasks_run_testcases_for_python_codeunit(repository_folder, codeunitname, verbosity)
+        self.standardized_tasks_generate_coverage_report(repository_folder, codeunitname, verbosity, generate_badges, buildenvironment, commandline_arguments)
         self.update_path_of_source(repository_folder, codeunitname)
-        self.standardized_tasks_generate_coverage_report(repository_folder, codeunitname, verbosity, generate_badges, targetenvironmenttype, commandline_arguments)
-        self.run_testcases_common_post_task(repository_folder, codeunitname, verbosity, True, targetenvironmenttype, commandline_arguments)
-
-    def copy_source_files_to_output_directory(self, buildscript_file: str):
-        sc = ScriptCollectionCore()
-        folder = os.path.dirname(os.path.realpath(buildscript_file))
-        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", folder)
-        result = sc.run_program_argsasarray("git", ["ls-tree", "-r", "HEAD", "--name-only"], codeunit_folder)
-        files = [f for f in result[1].split('\n') if len(f) > 0]
-        for file in files:
-            full_source_file = os.path.join(codeunit_folder, file)
-            target_file = os.path.join(codeunit_folder, "Other", "Artifacts", "SourceCode", file)
-            target_folder = os.path.dirname(target_file)
-            GeneralUtilities.ensure_directory_exists(target_folder)
-            shutil.copyfile(full_source_file, target_file)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_build_for_python_codeunit(self, buildscript_file: str, verbosity: int, targetenvironmenttype: str, commandline_arguments: list[str]):
-        self.copy_source_files_to_output_directory(buildscript_file)
+    def standardized_tasks_build_for_python_codeunit_in_common_project_structure(self, buildscript_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]):
         codeunitname: str = Path(os.path.dirname(buildscript_file)).parent.parent.name
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         codeunit_folder = str(Path(os.path.dirname(buildscript_file)).parent.parent.absolute())
         repository_folder: str = str(Path(os.path.dirname(buildscript_file)).parent.parent.parent.absolute())
         target_directory = GeneralUtilities.resolve_relative_path(
-            "../Artifacts/BuildResult_Wheel", os.path.join(self.get_artifacts_folder(repository_folder, codeunitname)))
+            "../Artifacts/BuildResult_Wheel", os.path.join(self.get_artifacts_folder_in_repository_in_common_repository_format(repository_folder, codeunitname)))
         GeneralUtilities.ensure_directory_exists(target_directory)
+        # Copy ReadMe-file to subfolder as workaround because it seems that pyproject.toml or setuptools can not handle paths to a ReadMe-file in the parent-folder
+        shutil.copy(os.path.join(repository_folder, "ReadMe.md"), os.path.join(codeunit_folder, "ReadMe.md"))
         self.__sc.run_program("python", f"-m build --wheel --outdir {target_directory}", codeunit_folder, verbosity=verbosity)
-        self.generate_bom_for_python_project(verbosity, codeunit_folder, codeunitname, commandline_arguments)
-
-    @GeneralUtilities.check_arguments
-    def generate_bom_for_python_project(self, verbosity: int, codeunit_folder: str, codeunitname: str, commandline_arguments: list[str]):
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
-        codeunitversion = self.get_version_of_codeunit_folder(codeunit_folder)
-        bom_folder = "Other/Artifacts/BOM"
-        bom_folder_full = os.path.join(codeunit_folder, bom_folder)
-        GeneralUtilities.ensure_directory_exists(bom_folder_full)
-        self.__sc.run_program("cyclonedx-py", f"-o ./{bom_folder}/{codeunitname}.{codeunitversion}.sbom.xml -r -i requirements.txt", codeunit_folder, verbosity=verbosity)
 
     @GeneralUtilities.check_arguments
     def standardized_tasks_push_wheel_file_to_registry(self, wheel_file: str, api_key: str, repository: str, gpg_identity: str, verbosity: int) -> None:
         # repository-value when PyPi should be used: "pypi"
         # gpg_identity-value when wheel-file should not be signed: None
         folder = os.path.dirname(wheel_file)
         filename = os.path.basename(wheel_file)
@@ -259,78 +199,65 @@
             verbose_argument = ""
 
         twine_argument = f"upload{gpg_identity_argument} --repository {repository} --non-interactive {filename} --disable-progress-bar"
         twine_argument = f"{twine_argument} --username __token__ --password {api_key}{verbose_argument}"
         self.__sc.run_program("twine", twine_argument, folder, verbosity=verbosity, throw_exception_if_exitcode_is_not_zero=True)
 
     @GeneralUtilities.check_arguments
-    def push_wheel_build_artifact(self, push_build_artifacts_file, product_name, codeunitname, repository: str,
-                                  apikey: str, gpg_identity: str, verbosity: int, commandline_arguments: list[str], repository_folder_name: str) -> None:
+    def push_wheel_build_artifact_of_repository_in_common_file_structure(self, push_build_artifacts_file, product_name, codeunitname, repository: str,
+                                                                         apikey: str, gpg_identity: str, verbosity: int, commandline_arguments: list[str]) -> None:
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         folder_of_this_file = os.path.dirname(push_build_artifacts_file)
-        repository_folder = GeneralUtilities.resolve_relative_path(f"..{os.path.sep}../Submodules{os.path.sep}{repository_folder_name}", folder_of_this_file)
-        wheel_file = self.get_wheel_file(repository_folder, codeunitname)
+        repository_folder = GeneralUtilities.resolve_relative_path(f"..{os.path.sep}../Submodules{os.path.sep}{product_name}", folder_of_this_file)
+        wheel_file = self.get_wheel_file_in_repository_in_common_repository_format(repository_folder, codeunitname)
         self.standardized_tasks_push_wheel_file_to_registry(wheel_file, apikey, repository, gpg_identity, verbosity)
 
     @GeneralUtilities.check_arguments
-    def get_version_of_codeunit_file_content(self, codeunit_file_content: str) -> str:
-        root: etree._ElementTree = etree.fromstring(codeunit_file_content.encode("utf-8"))
-        result = str(root.xpath('//cps:version/text()',
-                     namespaces={'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure'})[0])
-        return result
-
-    @GeneralUtilities.check_arguments
     def get_version_of_codeunit(self, codeunit_file: str) -> None:
-        return self.get_version_of_codeunit_file_content(GeneralUtilities.read_text_from_file(codeunit_file))
+        root: etree._ElementTree = etree.parse(codeunit_file)
+        result = str(root.xpath('//codeunit:version/text()', namespaces={'codeunit': 'https://github.com/anionDev/ProjectTemplates'})[0])
+        return result
 
+    @staticmethod
     @GeneralUtilities.check_arguments
-    def get_version_of_codeunit_folder(self, codeunit_folder: str) -> None:
-        codeunit_file = os.path.join(codeunit_folder, f"{os.path.basename(codeunit_folder)}.codeunit.xml")
-        return self.get_version_of_codeunit(codeunit_file)
+    def get_buildconfigurationdevelopment_from_commandline_arguments(commandline_arguments: list[str], default_value: str) -> str:
+        return TasksForCommonProjectStructure.get_string_value_from_commandline_arguments(commandline_arguments, "buildconfigurationdevelopment",  default_value)
 
     @staticmethod
     @GeneralUtilities.check_arguments
-    def get_string_value_from_commandline_arguments(commandline_arguments: list[str], property_name: str, default_value: str) -> str:
-        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, property_name)
-        if result is None:
-            return default_value
-        else:
-            return result
+    def get_buildconfigurationqualitycheck_from_commandline_arguments(commandline_arguments: list[str], default_value: str) -> str:
+        return TasksForCommonProjectStructure.get_string_value_from_commandline_arguments(commandline_arguments, "buildconfigurationqualitycheck",  default_value)
 
     @staticmethod
     @GeneralUtilities.check_arguments
-    def get_is_pre_merge_value_from_commandline_arguments(commandline_arguments: list[str],  default_value: bool) -> bool:
-        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, "is_pre_merge")
-        if result is None:
-            return default_value
-        else:
-            return GeneralUtilities.string_to_boolean(result)
+    def get_buildconfigurationproductive_from_commandline_arguments(commandline_arguments: list[str],  default_value: str) -> str:
+        return TasksForCommonProjectStructure.get_string_value_from_commandline_arguments(commandline_arguments, "buildconfigurationproductive",  default_value)
 
     @staticmethod
     @GeneralUtilities.check_arguments
-    def get_assume_dependent_codeunits_are_already_built_from_commandline_arguments(commandline_arguments: list[str],  default_value: bool) -> bool:
-        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, "assume_dependent_codeunits_are_already_built")
+    def get_string_value_from_commandline_arguments(commandline_arguments: list[str], property_name: str, default_value: str) -> str:
+        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, property_name)
         if result is None:
             return default_value
         else:
-            return GeneralUtilities.string_to_boolean(result)
+            return result
 
     @staticmethod
     @GeneralUtilities.check_arguments
     def get_verbosity_from_commandline_arguments(commandline_arguments: list[str],  default_value: int) -> int:
         result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, "verbosity")
         if result is None:
             return default_value
         else:
             return int(result)
 
     @staticmethod
     @GeneralUtilities.check_arguments
-    def get_targetenvironmenttype_from_commandline_arguments(commandline_arguments: list[str],  default_value: str) -> str:
-        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, "targetenvironmenttype")
+    def get_buildenvironment_from_commandline_arguments(commandline_arguments: list[str],  default_value: str) -> str:
+        result = TasksForCommonProjectStructure.get_property_from_commandline_arguments(commandline_arguments, "buildenvironment")
         if result is None:
             return default_value
         else:
             return result
 
     @staticmethod
     @GeneralUtilities.check_arguments
@@ -363,322 +290,133 @@
             prefix = f"--overwrite_{property_name}"
             if commandline_argument.startswith(prefix):
                 if m := re.match(f"^{re.escape(prefix)}=(.+)$", commandline_argument):
                     result = m.group(1)
         return result
 
     @GeneralUtilities.check_arguments
-    def update_version_of_codeunit(self, common_tasks_file: str, current_version: str) -> None:
+    def update_version_of_codeunit_to_project_version(self, common_tasks_file: str, current_version: str) -> None:
         codeunit_name: str = os.path.basename(GeneralUtilities.resolve_relative_path("..", os.path.dirname(common_tasks_file)))
         codeunit_file: str = os.path.join(GeneralUtilities.resolve_relative_path("..", os.path.dirname(common_tasks_file)), f"{codeunit_name}.codeunit.xml")
         self.write_version_to_codeunit_file(codeunit_file, current_version)
 
     @GeneralUtilities.check_arguments
-    def t4_transform(self, commontasks_script_file_of_current_file: str, verbosity: int):
-        sc = ScriptCollectionCore()
-        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", commontasks_script_file_of_current_file)
-        repository_folder: str = os.path.dirname(codeunit_folder)
-        codeunitname: str = os.path.basename(codeunit_folder)
-        codeunit_folder = os.path.join(repository_folder, codeunitname)
-        for search_result in Path(codeunit_folder).glob('**/*.tt'):
-            tt_file = str(search_result)
-            relative_path_to_tt_file = str(Path(tt_file).relative_to(codeunit_folder))
-            argument = f"--parameter=repositoryFolder={repository_folder} --parameter=codeUnitName={codeunitname} {relative_path_to_tt_file}"
-            sc.run_program("t4", argument, codeunit_folder, verbosity=verbosity)
-
-    @GeneralUtilities.check_arguments
-    def standardized_tasks_generate_reference_by_docfx(self, generate_reference_script_file: str, verbosity: int, targetenvironmenttype: str, commandline_arguments: list[str]) -> None:
+    def standardized_tasks_generate_reference_by_docfx(self, generate_reference_script_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]) -> None:
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         folder_of_current_file = os.path.dirname(generate_reference_script_file)
         generated_reference_folder = GeneralUtilities.resolve_relative_path("../Artifacts/Reference", folder_of_current_file)
         GeneralUtilities.ensure_directory_does_not_exist(generated_reference_folder)
         GeneralUtilities.ensure_directory_exists(generated_reference_folder)
         obj_folder = os.path.join(folder_of_current_file, "obj")
         GeneralUtilities.ensure_directory_does_not_exist(obj_folder)
         GeneralUtilities.ensure_directory_exists(obj_folder)
-        self.__sc.run_program("docfx", "docfx.json", folder_of_current_file, verbosity=verbosity)
+        self.__sc.run_program("docfx", "docfx.json", folder_of_current_file, verbosity)
         GeneralUtilities.ensure_directory_does_not_exist(obj_folder)
 
-    def standardized_task_verify_standard_format_csproj_files(self, codeunit_folder: str) -> bool:
-        repository_folder = os.path.dirname(codeunit_folder)
-        codeunit_name = os.path.basename(codeunit_folder)
-        codeunit_folder = os.path.join(repository_folder, codeunit_name)
-        codeunit_version = self.get_version_of_codeunit_folder(codeunit_folder)
-        message = " does not match the standardized .csproj-file-format."
-
-        project_name = codeunit_name
-        csproj_file = os.path.join(codeunit_folder, project_name, project_name+".csproj")
-        if not self.__standardized_task_verify_standard_format_for_project_csproj_file(csproj_file, codeunit_name, codeunit_version):
-            raise ValueError(csproj_file+message)
-
-        testproject_name = project_name+"Tests"
-        test_csproj_file = os.path.join(codeunit_folder, testproject_name, testproject_name+".csproj")
-        if not self.__standardized_task_verify_standard_format_for_test_csproj_file(test_csproj_file, codeunit_name, codeunit_version):
-            raise ValueError(test_csproj_file+message)
-
-    def __standardized_task_verify_standard_format_for_project_csproj_file(self, csproj_file: str, codeunit_name: str, codeunit_version: str) -> bool:
-        codeunit_name_regex = re.escape(codeunit_name)
-        codeunit_version_regex = re.escape(codeunit_version)
-        regex = f"""^<Project Sdk=\\"Microsoft\\.NET\\.Sdk\\">
-    <PropertyGroup>
-        <TargetFramework>([^<]+)<\\/TargetFramework>
-        <Authors>([^<]+)<\\/Authors>
-        <Version>{codeunit_version_regex}<\\/Version>
-        <AssemblyVersion>{codeunit_version_regex}<\\/AssemblyVersion>
-        <FileVersion>{codeunit_version_regex}<\\/FileVersion>
-        <SelfContained>false<\\/SelfContained>
-        <IsPackable>false<\\/IsPackable>
-        <PreserveCompilationContext>false<\\/PreserveCompilationContext>
-        <GenerateRuntimeConfigurationFiles>true<\\/GenerateRuntimeConfigurationFiles>
-        <Copyright>([^<]+)<\\/Copyright>
-        <Description>([^<]+)<\\/Description>
-        <PackageProjectUrl>https:\\/\\/([^<]+)<\\/PackageProjectUrl>
-        <RepositoryUrl>https:\\/\\/([^<]+)\\.git<\\/RepositoryUrl>
-        <RootNamespace>([^<]+)\\.Core<\\/RootNamespace>
-        <ProduceReferenceAssembly>false<\\/ProduceReferenceAssembly>
-        <Nullable>disable<\\/Nullable>
-        <Configurations>Development;QualityCheck;Productive<\\/Configurations>
-        <IsTestProject>false<\\/IsTestProject>
-        <LangVersion>([^<]+)<\\/LangVersion>
-        <PackageRequireLicenseAcceptance>true<\\/PackageRequireLicenseAcceptance>
-        <GenerateSerializationAssemblies>Off<\\/GenerateSerializationAssemblies>
-        <AppendTargetFrameworkToOutputPath>false<\\/AppendTargetFrameworkToOutputPath>
-        <OutputPath>\\.\\.\\\\Other\\\\Artifacts\\\\BuildResult_DotNet_win-x64<\\/OutputPath>
-        <PlatformTarget>([^<]+)<\\/PlatformTarget>
-        <WarningLevel>\\d<\\/WarningLevel>
-        <Prefer32Bit>false<\\/Prefer32Bit>
-        <NoWarn>([^<]+)<\\/NoWarn>
-        <WarningsAsErrors>([^<]+)<\\/WarningsAsErrors>
-        <ErrorLog>\\.\\.\\\\Other\\\\Resources\\\\{codeunit_name_regex}\\.sarif<\\/ErrorLog>
-        <OutputType>([^<]+)<\\/OutputType>
-        <DocumentationFile>\\.\\.\\\\Other\\\\Artifacts\\\\MetaInformation\\\\{codeunit_name_regex}\\.xml<\\/DocumentationFile>(\\n|.)*
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='Development'\\\">
-        <DebugType>full<\\/DebugType>
-        <DebugSymbols>true<\\/DebugSymbols>
-        <Optimize>false<\\/Optimize>
-        <DefineConstants>TRACE;DEBUG;Development<\\/DefineConstants>
-        <ErrorReport>prompt<\\/ErrorReport>
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='QualityCheck'\\\">
-        <DebugType>portable<\\/DebugType>
-        <DebugSymbols>true<\\/DebugSymbols>
-        <Optimize>false<\\/Optimize>
-        <DefineConstants>TRACE;QualityCheck<\\/DefineConstants>
-        <ErrorReport>none<\\/ErrorReport>
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='Productive'\\\">
-        <DebugType>none<\\/DebugType>
-        <DebugSymbols>false<\\/DebugSymbols>
-        <Optimize>true<\\/Optimize>
-        <DefineConstants>Productive<\\/DefineConstants>
-        <ErrorReport>none<\\/ErrorReport>
-    <\\/PropertyGroup>(\\n|.)*
-<\\/Project>$"""
-        return self.__standardized_task_verify_standard_format_for_csproj_files(regex, csproj_file)
-
-    def __standardized_task_verify_standard_format_for_test_csproj_file(self, csproj_file: str, codeunit_name: str, codeunit_version: str) -> bool:
-        codeunit_name_regex = re.escape(codeunit_name)
-        codeunit_version_regex = re.escape(codeunit_version)
-        regex = f"""^<Project Sdk=\\"Microsoft\\.NET\\.Sdk\\">
-    <PropertyGroup>
-        <TargetFramework>([^<]+)<\\/TargetFramework>
-        <Authors>([^<]+)<\\/Authors>
-        <Version>{codeunit_version_regex}<\\/Version>
-        <AssemblyVersion>{codeunit_version_regex}<\\/AssemblyVersion>
-        <FileVersion>{codeunit_version_regex}<\\/FileVersion>
-        <SelfContained>false<\\/SelfContained>
-        <IsPackable>false<\\/IsPackable>
-        <PreserveCompilationContext>false<\\/PreserveCompilationContext>
-        <GenerateRuntimeConfigurationFiles>true<\\/GenerateRuntimeConfigurationFiles>
-        <Copyright>([^<]+)<\\/Copyright>
-        <Description>{codeunit_name_regex}Tests is the test-project for {codeunit_name_regex}\\.<\\/Description>
-        <PackageProjectUrl>https:\\/\\/([^<]+)<\\/PackageProjectUrl>
-        <RepositoryUrl>https:\\/\\/([^<]+)\\.git</RepositoryUrl>
-        <RootNamespace>([^<]+)\\.Tests<\\/RootNamespace>
-        <ProduceReferenceAssembly>false<\\/ProduceReferenceAssembly>
-        <Nullable>disable<\\/Nullable>
-        <Configurations>Development;QualityCheck;Productive<\\/Configurations>
-        <IsTestProject>true<\\/IsTestProject>
-        <LangVersion>([^<]+)<\\/LangVersion>
-        <PackageRequireLicenseAcceptance>true<\\/PackageRequireLicenseAcceptance>
-        <GenerateSerializationAssemblies>Off<\\/GenerateSerializationAssemblies>
-        <AppendTargetFrameworkToOutputPath>false<\\/AppendTargetFrameworkToOutputPath>
-        <OutputPath>\\.\\.\\\\Other\\\\Artifacts\\\\BuildResultTests_DotNet_win-x64<\\/OutputPath>
-        <PlatformTarget>([^<]+)<\\/PlatformTarget>
-        <WarningLevel>\\d<\\/WarningLevel>
-        <Prefer32Bit>false<\\/Prefer32Bit>
-        <NoWarn>([^<]+)<\\/NoWarn>
-        <WarningsAsErrors>([^<]+)<\\/WarningsAsErrors>
-        <ErrorLog>\\.\\.\\\\Other\\\\Resources\\\\{codeunit_name_regex}Tests\\.sarif<\\/ErrorLog>
-        <OutputType>Library<\\/OutputType>(\\n|.)*
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='Development'\\\">
-        <DebugType>full<\\/DebugType>
-        <DebugSymbols>true<\\/DebugSymbols>
-        <Optimize>false<\\/Optimize>
-        <DefineConstants>TRACE;DEBUG;Development<\\/DefineConstants>
-        <ErrorReport>prompt<\\/ErrorReport>
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='QualityCheck'\\\">
-        <DebugType>portable<\\/DebugType>
-        <DebugSymbols>true<\\/DebugSymbols>
-        <Optimize>false<\\/Optimize>
-        <DefineConstants>TRACE;QualityCheck<\\/DefineConstants>
-        <ErrorReport>none<\\/ErrorReport>
-    <\\/PropertyGroup>
-    <PropertyGroup Condition=\\\"'\\$\\(Configuration\\)'=='Productive'\\\">
-        <DebugType>none<\\/DebugType>
-        <DebugSymbols>false<\\/DebugSymbols>
-        <Optimize>true<\\/Optimize>
-        <DefineConstants>Productive<\\/DefineConstants>
-        <ErrorReport>none<\\/ErrorReport>
-    <\\/PropertyGroup>(\\n|.)*
-<\\/Project>$"""
-        return self.__standardized_task_verify_standard_format_for_csproj_files(regex, csproj_file)
-
-    def __standardized_task_verify_standard_format_for_csproj_files(self, regex: str, csproj_file: str) -> bool:
-        filename = os.path.basename(csproj_file)
-        GeneralUtilities.write_message_to_stdout(f"Check {filename}...")
-        file_content = GeneralUtilities.read_text_from_file(csproj_file)
-        regex = regex.replace("\r", "").replace("\n", "\\n")
-        file_content = file_content.replace("\r", "")
-        match = re.match(regex, file_content)
-        return match is not None
-
-    @GeneralUtilities.check_arguments
-    def __standardized_tasks_build_for_dotnet_build(self, csproj_file: str, originaloutputfolder: str, files_to_sign: dict[str, str], commitid: str,
-                                                    verbosity: int, runtimes: list[str], target_environmenttype: str, target_environmenttype_mapping:  dict[str, str],
-                                                    copy_license_file_to_target_folder: bool, repository_folder: str, codeunit_name: str, commandline_arguments: list[str]):
-        dotnet_build_configuration: str = target_environmenttype_mapping[target_environmenttype]
-        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        codeunit_folder = os.path.join(repository_folder, codeunit_name)
-        csproj_file_folder = os.path.dirname(csproj_file)
-        csproj_file_name = os.path.basename(csproj_file)
-        csproj_file_name_without_extension = csproj_file_name.split(".")[0]
+    @GeneralUtilities.check_arguments
+    def __standardized_tasks_build_for_dotnet_build(self, csproj_file: str, buildconfiguration: str, originaloutputfolder: str, files_to_sign: dict[str, str], commitid: str,
+                                                    verbosity: int, runtimes: list[str]):
         for runtime in runtimes:
             outputfolder = originaloutputfolder+runtime
+            csproj_file_folder = os.path.dirname(csproj_file)
+            csproj_file_name = os.path.basename(csproj_file)
             self.__sc.run_program("dotnet", "clean", csproj_file_folder, verbosity=verbosity)
-            GeneralUtilities.ensure_directory_does_not_exist(os.path.join(csproj_file_folder, "obj"))
             GeneralUtilities.ensure_directory_does_not_exist(outputfolder)
             GeneralUtilities.ensure_directory_exists(outputfolder)
-            self.__sc.run_program("dotnet", "restore", codeunit_folder, verbosity=verbosity)
-            self.__sc.run_program("dotnet", f"build {csproj_file_name} -c {dotnet_build_configuration} -o {outputfolder} --runtime {runtime}",
-                                  csproj_file_folder, verbosity=verbosity)
-            if copy_license_file_to_target_folder:
-                license_file = os.path.join(repository_folder, "License.txt")
-                target = os.path.join(outputfolder, f"{codeunit_name}.License.txt")
-                shutil.copyfile(license_file, target)
+            # TODO pass commitid, timestamp and if desired something like keypair, certificate to the src-code
+            self.__sc.run_program("dotnet", f"build {csproj_file_name} -c {buildconfiguration} -o {outputfolder} --runtime {runtime}", csproj_file_folder, verbosity=verbosity)
             for file, keyfile in files_to_sign.items():
                 self.__sc.dotnet_sign_file(os.path.join(outputfolder, file), keyfile, verbosity)
 
-            sarif_filename = f"{csproj_file_name_without_extension}.sarif"
-            sarif_source_file = os.path.join(codeunit_folder, "Other", "Resources", sarif_filename)
-            if os.path.exists(sarif_source_file):
-                sarif_folder = os.path.join(codeunit_folder, "Other", "Artifacts", "CodeAnalysisResult")
-                GeneralUtilities.ensure_directory_exists(sarif_folder)
-                sarif_target_file = os.path.join(sarif_folder, sarif_filename)
-                GeneralUtilities.ensure_file_does_not_exist(sarif_target_file)
-                shutil.copyfile(sarif_source_file, sarif_target_file)
-                GeneralUtilities.ensure_file_does_not_exist(sarif_source_file)
-
     @GeneralUtilities.check_arguments
-    def standardized_tasks_build_for_dotnet_project(self, buildscript_file: str, default_target_environmenttype: str,
-                                                    target_environmenttype_mapping:  dict[str, str], runtimes: list[str], verbosity: int, commandline_arguments: list[str]):
+    def standardized_tasks_build_for_dotnet_project_in_common_project_structure(self, buildscript_file: str, default_build_environment: str,
+                                                                                build_environment_mapping:  dict[str, str], runtimes: list[str], verbosity: int, commandline_arguments: list[str]):
         # hint: arguments can be overwritten by commandline_arguments
         # this function builds an exe or dll
-        target_environmenttype = self.get_targetenvironmenttype_from_commandline_arguments(commandline_arguments, default_target_environmenttype)
-        self.__standardized_tasks_build_for_dotnet_project(
-            buildscript_file, target_environmenttype_mapping, default_target_environmenttype, verbosity, target_environmenttype,
-            runtimes, True, commandline_arguments)
+        build_environment = self.get_buildenvironment_from_commandline_arguments(commandline_arguments, default_build_environment)
+        self.__standardized_tasks_build_for_dotnet_project_in_common_project_structure(
+            buildscript_file, build_environment_mapping, default_build_environment, verbosity, build_environment, runtimes, commandline_arguments)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_build_for_dotnet_library_project(self, buildscript_file: str, default_target_environmenttype: str,
-                                                            target_environmenttype_mapping:  dict[str, str], runtimes: list[str],
-                                                            verbosity: int, commandline_arguments: list[str]):
+    def standardized_tasks_build_for_dotnet_library_project_in_common_project_structure(self, buildscript_file: str, default_build_environment: str,
+                                                                                        build_environment_mapping:  dict[str, str], runtimes: list[str],
+                                                                                        verbosity: int, commandline_arguments: list[str]):
         # hint: arguments can be overwritten by commandline_arguments
         # this function builds an exe or dll and converts it to a nupkg-file
-
-        target_environmenttype = self.get_targetenvironmenttype_from_commandline_arguments(commandline_arguments, default_target_environmenttype)
-        self.__standardized_tasks_build_for_dotnet_project(buildscript_file, target_environmenttype_mapping, default_target_environmenttype,
-                                                           verbosity, target_environmenttype, runtimes, True, commandline_arguments)
-        self.__standardized_tasks_build_nupkg_for_dotnet_create_package(buildscript_file, verbosity,
-                                                                        commandline_arguments)
+        build_environment = self.get_buildenvironment_from_commandline_arguments(commandline_arguments, default_build_environment)
+        self.__standardized_tasks_build_for_dotnet_project_in_common_project_structure(
+            buildscript_file, build_environment_mapping, default_build_environment, verbosity, build_environment, runtimes, commandline_arguments)
+        self.__standardized_tasks_build_nupkg_for_dotnet_create_package(buildscript_file, verbosity, commandline_arguments)
+
+    @GeneralUtilities.check_arguments
+    def __get_dotnet_buildconfiguration_by_build_environment(self, buildenvironment: str, default_value: str, commandline_arguments: list[str]):
+        if buildenvironment == "Development":
+            return self.get_buildconfigurationdevelopment_from_commandline_arguments(commandline_arguments, default_value)
+        if buildenvironment == "QualityCheck":
+            return self.get_buildconfigurationqualitycheck_from_commandline_arguments(commandline_arguments, default_value)
+        if buildenvironment == "Productive":
+            return self.get_buildconfigurationproductive_from_commandline_arguments(commandline_arguments,  "Release")
+        raise ValueError(f"Unknown build-environment: {buildenvironment}")
 
     @GeneralUtilities.check_arguments
-    def get_default_target_environmenttype_mapping(self) -> dict[str, str]:
+    def get_default_build_environment_mapping(self) -> dict[str, str]:
         return {
-            TasksForCommonProjectStructure.get_development_environment_name(): TasksForCommonProjectStructure.get_development_environment_name(),
-            TasksForCommonProjectStructure.get_qualitycheck_environment_name(): TasksForCommonProjectStructure.get_qualitycheck_environment_name(),
-            TasksForCommonProjectStructure.get_productive_environment_name(): TasksForCommonProjectStructure.get_productive_environment_name()
+            "Development": "Development",
+            "QualityCheck": "QualityCheck",
+            "Productive": "Productive"
         }
 
     @GeneralUtilities.check_arguments
-    def __standardized_tasks_build_for_dotnet_project(self, buildscript_file: str, target_environmenttype_mapping:  dict[str, str],
-                                                      target_environment_type: str,  verbosity: int, target_environmenttype: str,
-                                                      runtimes: list[str], copy_license_file_to_target_folder: bool, commandline_arguments: list[str]) -> None:
-        self.copy_source_files_to_output_directory(buildscript_file)
+    def __standardized_tasks_build_for_dotnet_project_in_common_project_structure(self, buildscript_file: str, build_environment_mapping:  dict[str, str],
+                                                                                  default_build_configuration: str,  verbosity: int, build_environment: str,
+                                                                                  runtimes: list[str], commandline_arguments: list[str]):
+        dotnet_build_configuration: str = build_environment_mapping[build_environment]
         codeunitname: str = os.path.basename(str(Path(os.path.dirname(buildscript_file)).parent.parent.absolute()))
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         files_to_sign: dict[str, str] = TasksForCommonProjectStructure.get_filestosign_from_commandline_arguments(commandline_arguments,  dict())
         repository_folder: str = str(Path(os.path.dirname(buildscript_file)).parent.parent.parent.absolute())
-        commitid = self.__sc.git_get_commit_id(repository_folder)
+        commitid = self.__sc.git_get_current_commit_id(repository_folder)
         outputfolder = GeneralUtilities.resolve_relative_path("../Artifacts", os.path.dirname(buildscript_file))
         codeunit_folder = os.path.join(repository_folder, codeunitname)
-        csproj_file = os.path.join(codeunit_folder, codeunitname, codeunitname + ".csproj")
+        csproj_file = os.path.join(codeunit_folder, codeunitname, codeunitname+".csproj")
         csproj_test_file = os.path.join(codeunit_folder, codeunitname+"Tests", codeunitname+"Tests.csproj")
-        self.__standardized_tasks_build_for_dotnet_build(csproj_file,  os.path.join(outputfolder, "BuildResult_DotNet_"), files_to_sign, commitid,
-                                                         verbosity, runtimes, target_environment_type, target_environmenttype_mapping,
-                                                         copy_license_file_to_target_folder, repository_folder, codeunitname, commandline_arguments)
-        self.__standardized_tasks_build_for_dotnet_build(csproj_test_file,  os.path.join(outputfolder, "BuildResultTests_DotNet_"), files_to_sign, commitid,
-                                                         verbosity, runtimes, target_environment_type, target_environmenttype_mapping,
-                                                         copy_license_file_to_target_folder, repository_folder, codeunitname, commandline_arguments)
+        buildconfiguration = self.__get_dotnet_buildconfiguration_by_build_environment(dotnet_build_configuration, default_build_configuration, commandline_arguments)
 
-        self.generate_sbom_for_dotnet_project(codeunit_folder, verbosity, commandline_arguments)
+        self.__sc.run_program("dotnet", "restore", codeunit_folder, verbosity=verbosity)
+        self.__standardized_tasks_build_for_dotnet_build(csproj_file, buildconfiguration,
+                                                         os.path.join(outputfolder, "BuildResult_DotNet_"), files_to_sign, commitid, verbosity, runtimes)
+        self.__standardized_tasks_build_for_dotnet_build(csproj_test_file, buildconfiguration,
+                                                         os.path.join(outputfolder, "BuildResult_DotNetTests_"), files_to_sign, commitid, verbosity, runtimes)
 
     @GeneralUtilities.check_arguments
     def __standardized_tasks_build_nupkg_for_dotnet_create_package(self, buildscript_file: str, verbosity: int, commandline_arguments: list[str]):
         codeunitname: str = os.path.basename(str(Path(os.path.dirname(buildscript_file)).parent.parent.absolute()))
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         repository_folder: str = str(Path(os.path.dirname(buildscript_file)).parent.parent.parent.absolute())
         build_folder = os.path.join(repository_folder, codeunitname, "Other", "Build")
         outputfolder = GeneralUtilities.resolve_relative_path("../Artifacts/BuildResult_NuGet", os.path.dirname(buildscript_file))
         root: etree._ElementTree = etree.parse(os.path.join(build_folder, f"{codeunitname}.nuspec"))
         current_version = root.xpath("//*[name() = 'package']/*[name() = 'metadata']/*[name() = 'version']/text()")[0]
         nupkg_filename = f"{codeunitname}.{current_version}.nupkg"
         nupkg_file = f"{build_folder}/{nupkg_filename}"
         GeneralUtilities.ensure_file_does_not_exist(nupkg_file)
-        commit_id = self.__sc.git_get_commit_id(repository_folder)
-        self.__sc.run_program("nuget", f"pack {codeunitname}.nuspec -Properties \"commitid={commit_id}\"", build_folder, verbosity=verbosity)
+        self.__sc.run_program("nuget", f"pack {codeunitname}.nuspec", build_folder, verbosity=verbosity)
         GeneralUtilities.ensure_directory_does_not_exist(outputfolder)
         GeneralUtilities.ensure_directory_exists(outputfolder)
         os.rename(nupkg_file, f"{outputfolder}/{nupkg_filename}")
 
     @GeneralUtilities.check_arguments
-    def generate_sbom_for_dotnet_project(self, codeunit_folder: str, verbosity: int, commandline_arguments: list[str]) -> None:
-        codeunit_name = os.path.basename(codeunit_folder)
-        sc = ScriptCollectionCore()
-        bomfile_folder = "Other\\Artifacts\\BOM"
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        sc.run_program("dotnet", f"CycloneDX {codeunit_name}\\{codeunit_name}.csproj -o {bomfile_folder} --disable-github-licenses", codeunit_folder, verbosity=verbosity)
-        codeunitversion = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunit_name}.codeunit.xml"))
-        target = f"{codeunit_folder}\\{bomfile_folder}\\{codeunit_name}.{codeunitversion}.sbom.xml"
-        GeneralUtilities.ensure_file_does_not_exist(target)
-        os.rename(f"{codeunit_folder}\\{bomfile_folder}\\bom.xml", target)
-
-    @GeneralUtilities.check_arguments
-    def standardized_tasks_linting_for_python_codeunit(self, linting_script_file: str, verbosity: int, targetenvironmenttype: str, commandline_arguments: list[str]):
+    def standardized_tasks_linting_for_python_codeunit_in_common_project_structure(self, linting_script_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]):
         codeunitname: str = Path(os.path.dirname(linting_script_file)).parent.parent.name
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         repository_folder: str = str(Path(os.path.dirname(linting_script_file)).parent.parent.parent.absolute())
         errors_found = False
         GeneralUtilities.write_message_to_stdout(f"Check for linting-issues in codeunit {codeunitname}.")
         src_folder = os.path.join(repository_folder, codeunitname, codeunitname)
         tests_folder = src_folder+"Tests"
-        # TODO check if there are errors in sarif-file
         for file in GeneralUtilities.get_all_files_of_folder(src_folder)+GeneralUtilities.get_all_files_of_folder(tests_folder):
             relative_file_path_in_repository = os.path.relpath(file, repository_folder)
             if file.endswith(".py") and os.path.getsize(file) > 0 and not self.__sc.file_is_git_ignored(relative_file_path_in_repository, repository_folder):
                 GeneralUtilities.write_message_to_stdout(f"Check for linting-issues in {os.path.relpath(file,os.path.join(repository_folder,codeunitname))}.")
                 linting_result = self.__sc.python_file_has_errors(file, repository_folder)
                 if (linting_result[0]):
                     errors_found = True
@@ -686,391 +424,318 @@
                         GeneralUtilities.write_message_to_stderr(error)
         if errors_found:
             raise Exception("Linting-issues occurred.")
         else:
             GeneralUtilities.write_message_to_stdout("No linting-issues found.")
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_generate_coverage_report(self, repository_folder: str, codeunitname: str, verbosity: int, generate_badges: bool, targetenvironmenttype: str,
-                                                    commandline_arguments: list[str], add_testcoverage_history_entry: bool = None):
+    def standardized_tasks_generate_coverage_report(self, repository_folder: str, codeunitname: str, verbosity: int, generate_badges: bool, buildenvironment: str, commandline_arguments: list[str]):
         """This script expects that the file '<repositorybasefolder>/<codeunitname>/Other/Artifacts/TestCoverage/TestCoverage.xml'
         which contains a test-coverage-report in the cobertura-format exists.
         This script expectes that the testcoverage-reportfolder is '<repositorybasefolder>/<codeunitname>/Other/Artifacts/TestCoverageReport'.
         This script expectes that a test-coverage-badges should be added to '<repositorybasefolder>/<codeunitname>/Other/Resources/Badges'."""
-        codeunit_version = self.get_version_of_codeunit(os.path.join(repository_folder, codeunitname, f"{codeunitname}.codeunit.xml"))
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         if verbosity == 0:
             verbose_argument_for_reportgenerator = "Off"
         if verbosity == 1:
             verbose_argument_for_reportgenerator = "Error"
         if verbosity == 2:
             verbose_argument_for_reportgenerator = "Info"
         if verbosity == 3:
             verbose_argument_for_reportgenerator = "Verbose"
 
         # Generating report
         GeneralUtilities.ensure_directory_does_not_exist(os.path.join(repository_folder, codeunitname, f"{codeunitname}/Other/Artifacts/TestCoverageReport"))
-        GeneralUtilities.ensure_directory_exists(os.path.join(repository_folder, codeunitname, "Other/Artifacts/TestCoverageReport"))
-
-        if add_testcoverage_history_entry is None:
-            add_testcoverage_history_entry = self.get_is_pre_merge_value_from_commandline_arguments(commandline_arguments, add_testcoverage_history_entry)
-
-        history_folder = f"{codeunitname}/Other/Resources/TestCoverageHistory"
-        history_folder_full = os.path.join(repository_folder, history_folder)
-        GeneralUtilities.ensure_directory_exists(history_folder_full)
-        history_argument = f" -historydir:{history_folder}"
+        GeneralUtilities.ensure_directory_exists(os.path.join(repository_folder, codeunitname, f"{codeunitname}/Other/Artifacts/TestCoverageReport"))
         self.__sc.run_program("reportgenerator", f"-reports:{codeunitname}/Other/Artifacts/TestCoverage/TestCoverage.xml " +
-                              f"-targetdir:{codeunitname}/Other/Artifacts/TestCoverageReport --verbosity:{verbose_argument_for_reportgenerator}{history_argument} " +
-                              f"-title:{codeunitname} -tag:v{codeunit_version}",
-                              repository_folder, verbosity=verbosity)
-        if not add_testcoverage_history_entry:
-            os.remove(GeneralUtilities.get_direct_files_of_folder(history_folder_full)[-1])
+                              f"-targetdir:{codeunitname}/Other/Artifacts/TestCoverageReport --verbosity={verbose_argument_for_reportgenerator}", repository_folder)
 
-        # Generating badges
         if generate_badges:
-            testcoverageubfolger = "Other/Resources/TestCoverageBadges"
+            # Generating badges
+            testcoverageubfolger = f"{codeunitname}/Other/Resources/TestCoverageBadges"
             fulltestcoverageubfolger = os.path.join(repository_folder, codeunitname, testcoverageubfolger)
             GeneralUtilities.ensure_directory_does_not_exist(fulltestcoverageubfolger)
             GeneralUtilities.ensure_directory_exists(fulltestcoverageubfolger)
-            self.__sc.run_program("reportgenerator", "-reports:Other/Artifacts/TestCoverage/TestCoverage.xml " +
-                                  f"-targetdir:{testcoverageubfolger} -reporttypes:Badges " +
-                                  f"--verbosity:{verbose_argument_for_reportgenerator}", os.path.join(repository_folder, codeunitname),
-                                  verbosity=verbosity)
+            self.__sc.run_program("reportgenerator", f"-reports:{codeunitname}/Other/Artifacts/TestCoverage/TestCoverage.xml -targetdir:{testcoverageubfolger} " +
+                                  f"-reporttypes:Badges --verbosity={verbose_argument_for_reportgenerator}",  repository_folder, verbosity=verbosity)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_run_testcases_for_dotnet_project(self, runtestcases_file: str, targetenvironmenttype: str, verbosity: int, generate_badges: bool,
-                                                            target_environmenttype_mapping:  dict[str, str], commandline_arguments: list[str]):
-        dotnet_build_configuration: str = target_environmenttype_mapping[targetenvironmenttype]
+    def standardized_tasks_run_testcases_for_dotnet_project_in_common_project_structure(self, runtestcases_file: str, buildenvironment: str, verbosity: int, generate_badges: bool,
+                                                                                        commandline_arguments: list[str]):
         codeunit_name: str = os.path.basename(str(Path(os.path.dirname(runtestcases_file)).parent.parent.absolute()))
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
         repository_folder: str = str(Path(os.path.dirname(runtestcases_file)).parent.parent.parent.absolute())
-        coverage_file_folder = os.path.join(repository_folder, codeunit_name, "Other/Artifacts/TestCoverage")
-        working_directory = os.path.join(repository_folder, codeunit_name)
-        runsettings_argument = ""
-        runsettings_file = self.dotnet_runsettings_file
-        if os.path.isfile(os.path.join(working_directory, runsettings_file)):
-            runsettings_argument = f"--settings {runsettings_file} "
-        arg = f"collect dotnet test {runsettings_argument}-c {dotnet_build_configuration} --output-format cobertura --output Other\\Artifacts\\TestCoverage\\Testcoverage"
-        self.__sc.run_program("dotnet-coverage", arg, working_directory, verbosity=verbosity)
-        os.rename(os.path.join(coverage_file_folder,  "Testcoverage.cobertura.xml"), os.path.join(coverage_file_folder,  "TestCoverage.xml"))
-        self.run_testcases_common_post_task(repository_folder, codeunit_name, verbosity, generate_badges, targetenvironmenttype, commandline_arguments)
-
-    def run_testcases_common_post_task(self, repository_folder: str, codeunit_name: str, verbosity: int, generate_badges: bool,
-                                       targetenvironmenttype: str, commandline_arguments: list[str]):
+        testprojectname = codeunit_name+"Tests"
+        coveragefilesource = os.path.join(repository_folder, codeunit_name, testprojectname, "TestCoverage.xml")
         coverage_file_folder = os.path.join(repository_folder, codeunit_name, "Other/Artifacts/TestCoverage")
         coveragefiletarget = os.path.join(coverage_file_folder,  "TestCoverage.xml")
+        GeneralUtilities.ensure_file_does_not_exist(coveragefilesource)
+        buildconfiguration = self.__get_dotnet_buildconfiguration_by_build_environment(buildenvironment, codeunit_name, commandline_arguments)
+        self.__sc.run_program("dotnet", f"test {testprojectname}/{testprojectname}.csproj -c {buildconfiguration}"
+                              f" --verbosity normal /p:CollectCoverage=true /p:CoverletOutput=TestCoverage.xml"
+                              f" /p:CoverletOutputFormat=cobertura", os.path.join(repository_folder, codeunit_name), verbosity=verbosity)
+        GeneralUtilities.ensure_file_does_not_exist(coveragefiletarget)
+        GeneralUtilities.ensure_directory_exists(coverage_file_folder)
+        os.rename(coveragefilesource, coveragefiletarget)
+        self.standardized_tasks_generate_coverage_report(repository_folder, codeunit_name, verbosity, generate_badges, buildenvironment, commandline_arguments)
+        self.check_testcoverage_for_project_in_common_project_structure(coveragefiletarget, repository_folder, codeunit_name)
         self.update_path_of_source(repository_folder, codeunit_name)
-        self.standardized_tasks_generate_coverage_report(repository_folder, codeunit_name, verbosity, generate_badges, targetenvironmenttype, commandline_arguments)
-        self.check_testcoverage(coveragefiletarget, repository_folder, codeunit_name)
 
     @GeneralUtilities.check_arguments
     def write_version_to_codeunit_file(self, codeunit_file: str, current_version: str) -> None:
         versionregex = "\\d+\\.\\d+\\.\\d+"
         versiononlyregex = f"^{versionregex}$"
         pattern = re.compile(versiononlyregex)
         if pattern.match(current_version):
-            GeneralUtilities.write_text_to_file(codeunit_file, re.sub(f"<cps:version>{versionregex}<\\/cps:version>",
-                                                                      f"<cps:version>{current_version}</cps:version>", GeneralUtilities.read_text_from_file(codeunit_file)))
+            GeneralUtilities.write_text_to_file(codeunit_file, re.sub(f"<codeunit:version>{versionregex}<\\/codeunit:version>",
+                                                                      f"<codeunit:version>{current_version}</codeunit:version>", GeneralUtilities.read_text_from_file(codeunit_file)))
         else:
             raise ValueError(f"Version '{current_version}' does not match version-regex '{versiononlyregex}'.")
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_linting_for_dotnet_project(self, linting_script_file: str, verbosity: int, targetenvironmenttype: str, commandline_arguments: list[str]):
+    def standardized_tasks_linting_for_dotnet_project_in_common_project_structure(self, linting_script_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]):
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
-        # TODO check if there are errors in sarif-file
+        # TODO implement function
 
     @GeneralUtilities.check_arguments
-    def __export_codeunit_reference_content_to_reference_repository(self, project_version_identifier: str, replace_existing_content: bool,
-                                                                    target_folder_for_reference_repository: str, repository: str, codeunitname, projectname: str,
-                                                                    codeunit_version: str, public_repository_url: str, branch: str) -> None:
-        codeunit_folder = os.path.join(repository, codeunitname)
-        codeunit_file = os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml")
-        codeunit_has_testcases = self.codeunit_hast_testable_sourcecode(codeunit_file)
+    def __export_codeunit_reference_content_to_reference_repository(self, project_version_identifier: str, replace_existing_content: bool, target_folder_for_reference_repository: str,
+                                                                    repository: str, codeunitname, projectname: str, codeunit_version: str, public_repository_url: str, branch: str) -> None:
         target_folder = os.path.join(target_folder_for_reference_repository, project_version_identifier, codeunitname)
         if os.path.isdir(target_folder) and not replace_existing_content:
             raise ValueError(f"Folder '{target_folder}' already exists.")
         GeneralUtilities.ensure_directory_does_not_exist(target_folder)
         GeneralUtilities.ensure_directory_exists(target_folder)
-        codeunit_version_identifier = "Latest" if project_version_identifier == "Latest" else "v"+codeunit_version
-        title = f"Reference of codeunit {codeunitname} <i>{codeunit_version_identifier}</i> (contained in project {projectname} <i>{project_version_identifier}</i>)"
+        title = f"{codeunitname}-reference (codeunit v{codeunit_version}, conained in project {projectname} ({project_version_identifier}))"
         if public_repository_url is None:
             repo_url_html = ""
         else:
-            repo_url_html = f'<a href="{public_repository_url}/tree/{branch}/{codeunitname}">Source-code</a>'
-        if codeunit_has_testcases:
-            coverage_report_link = '<a href=""./TestCoverageReport/index.html"">TestCoverageReport</a><br>'
-        else:
-            coverage_report_link = ""
+            repo_url_html = f'<a href="{public_repository_url}/tree/{branch}/{codeunitname}">Source-code</a><br>'
         index_file_for_reference = os.path.join(target_folder, "index.html")
-
-        design_file = None
-        design = "ModestDark"
-        if design == "ModestDark":
-            design_file = "https://raw.githubusercontent.com/anionDev/ScriptCollection/other/next-release/Other/Resources/Designs/ModestDark/Style.css"
-        # TODO make designs from customizable sources be available by a customizable name and outsource this to a class-property because this is duplicated code.
-        if design_file is None:
-            design_html = f'<link rel="stylesheet" href="{design_file}">'
-        else:
-            design_html = f"{design_file}"
-
         index_file_content = f"""<!DOCTYPE html>
 <html lang="en">
-
   <head>
     <meta charset="UTF-8">
     <title>{title}</title>
-    {design_html}
+    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
   </head>
-
   <body>
-    <h1>{title}</h1>
+    <h1 class="display-1">{title}</h1>
     <hr/>
     Available reference-content for {codeunitname}:<br>
-    {repo_url_html}<br>
+    {repo_url_html}
     <a href="./Reference/index.html">Reference</a><br>
-    {coverage_report_link}
+    <a href="./TestCoverageReport/index.html">TestCoverageReport</a><br>
   </body>
-
 </html>
-"""
-
+"""  # see https://getbootstrap.com/docs/5.1/getting-started/introduction/
         GeneralUtilities.ensure_file_exists(index_file_for_reference)
         GeneralUtilities.write_text_to_file(index_file_for_reference, index_file_content)
         other_folder_in_repository = os.path.join(repository, codeunitname, "Other")
         source_generatedreference = os.path.join(other_folder_in_repository, "Artifacts", "Reference")
         target_generatedreference = os.path.join(target_folder, "Reference")
         shutil.copytree(source_generatedreference, target_generatedreference)
-
-        if codeunit_has_testcases:
-            source_testcoveragereport = os.path.join(other_folder_in_repository, "Artifacts", "TestCoverageReport")
-            target_testcoveragereport = os.path.join(target_folder, "TestCoverageReport")
-            shutil.copytree(source_testcoveragereport, target_testcoveragereport)
+        source_testcoveragereport = os.path.join(other_folder_in_repository, "Artifacts", "TestCoverageReport")
+        target_testcoveragereport = os.path.join(target_folder, "TestCoverageReport")
+        shutil.copytree(source_testcoveragereport, target_testcoveragereport)
 
     @GeneralUtilities.check_arguments
-    def __standardized_tasks_release_buildartifact(self, information: CreateReleaseInformationForProjectInCommonProjectFormat) -> None:
+    def __standardized_tasks_release_buildartifact_for_project_in_common_project_format(self, information: CreateReleaseInformationForProjectInCommonProjectFormat) -> None:
+        # This function is intended to be called directly after standardized_tasks_merge_to_stable_branch_for_project_in_common_project_format
         project_version = self.__sc.get_semver_version_from_gitversion(information.repository)
         target_folder_base = os.path.join(information.artifacts_folder, information.projectname, project_version)
+        if os.path.isdir(target_folder_base):
+            raise ValueError(f"The folder '{target_folder_base}' already exists.")
         GeneralUtilities.ensure_directory_exists(target_folder_base)
 
-        self.build_codeunits(information.repository, information.verbosity, information.target_environmenttype_for_productive,
-                             information.additional_arguments_file, False, information.export_target)
-
-        reference_folder = os.path.join(information.reference_repository, "ReferenceContent")
-
-        for codeunitname in self.get_codeunits(information.repository):
-            # Push artifacts to registry
-            if codeunitname in information.artifacts_which_have_artifacts_to_push:
-                scriptfilename = f"PushArtifacts.{codeunitname}.py"
-                push_artifact_to_registry_script = os.path.join(information.push_artifacts_scripts_folder, scriptfilename)
-                if not os.path.isfile(push_artifact_to_registry_script):
-                    raise ValueError(f"Script '{push_artifact_to_registry_script}' does not exist.")
-                GeneralUtilities.write_message_to_stdout(f"Push artifacts of codeunit {codeunitname}.")
-                self.__sc.run_program("python", push_artifact_to_registry_script, information.push_artifacts_scripts_folder,
-                                      verbosity=information.verbosity, throw_exception_if_exitcode_is_not_zero=True)
+        for codeunitname, codeunit_configuration in information.codeunits.items():
+            codeunit_folder = os.path.join(information.repository, codeunitname)
+            codeunit_version = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
+            self.build_codeunit(os.path.join(information.repository, codeunitname), information.verbosity, information.build_environment_for_productive,
+                                codeunit_configuration.additional_arguments_file)
+
+        reference_repository_target_for_project = os.path.join(information.reference_repository, "ReferenceContent")
+
+        for codeunitname, codeunit_configuration in information.codeunits.items():
+            codeunit_folder = os.path.join(information.repository, codeunitname)
+            codeunit_version = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
+
+            target_folder_for_codeunit = os.path.join(target_folder_base, codeunitname)
+            GeneralUtilities.ensure_directory_exists(target_folder_for_codeunit)
+            shutil.copytree(os.path.join(codeunit_folder, "Other", "Artifacts"), os.path.join(target_folder_for_codeunit, "Artifacts"))
+
+        for codeunitname, codeunit_configuration in information.codeunits.items():
+            push_artifact_to_registry_script = codeunit_configuration.push_to_registry_script
+            folder = os.path.dirname(push_artifact_to_registry_script)
+            file = os.path.basename(push_artifact_to_registry_script)
+            GeneralUtilities.write_message_to_stdout(f"Push buildartifact of codeunit {codeunitname}.")
+            self.__sc.run_program("python", file, folder, verbosity=information.verbosity, throw_exception_if_exitcode_is_not_zero=True)
 
             # Copy reference of codeunit to reference-repository
-            codeunit_version = self.get_version_of_codeunit_folder(os.path.join(information.repository, codeunitname))
-            self.__export_codeunit_reference_content_to_reference_repository(f"v{project_version}", False, reference_folder, information.repository,
+            self.__export_codeunit_reference_content_to_reference_repository(f"v{project_version}", False, reference_repository_target_for_project, information.repository,
                                                                              codeunitname, information.projectname, codeunit_version, information.public_repository_url,
                                                                              f"v{project_version}")
-            self.__export_codeunit_reference_content_to_reference_repository("Latest", True, reference_folder, information.repository,
+            self.__export_codeunit_reference_content_to_reference_repository("Latest", True, reference_repository_target_for_project, information.repository,
                                                                              codeunitname, information.projectname, codeunit_version, information.public_repository_url,
                                                                              information.target_branch_name)
 
-            # Generate reference
-            self.__generate_entire_reference(information.projectname, project_version, reference_folder)
-
-    @GeneralUtilities.check_arguments
-    def __generate_entire_reference(self, projectname: str, project_version: str, reference_folder: str) -> None:
-        all_available_version_identifier_folders_of_reference = list(
-            folder for folder in GeneralUtilities.get_direct_folders_of_folder(reference_folder))
-        all_available_version_identifier_folders_of_reference.reverse()  # move newer versions above
-        all_available_version_identifier_folders_of_reference.insert(0, all_available_version_identifier_folders_of_reference.pop())  # move latest version to the top
-        reference_versions_html_lines = []
-        for all_available_version_identifier_folder_of_reference in all_available_version_identifier_folders_of_reference:
-            version_identifier_of_project = os.path.basename(all_available_version_identifier_folder_of_reference)
-            if version_identifier_of_project == "Latest":
-                latest_version_hint = f" (v {project_version})"
-            else:
-                latest_version_hint = ""
-            reference_versions_html_lines.append('    <hr/>')
-            reference_versions_html_lines.append(f'    <h2 class="display-2">{version_identifier_of_project}{latest_version_hint}</h2>')
-            reference_versions_html_lines.append("    Contained codeunits:<br/>")
-            reference_versions_html_lines.append("    <ul>")
-            for codeunit_reference_folder in list(folder for folder in GeneralUtilities.get_direct_folders_of_folder(all_available_version_identifier_folder_of_reference)):
-                reference_versions_html_lines.append(f'      <li><a href="./{version_identifier_of_project}/{os.path.basename(codeunit_reference_folder)}/index.html">' +
-                                                     f'{os.path.basename(codeunit_reference_folder)} {version_identifier_of_project}</a></li>')
-            reference_versions_html_lines.append("    </ul>")
-
-        design_file = None
-        design = "ModestDark"
-        if design == "ModestDark":
-            design_file = "https://raw.githubusercontent.com/anionDev/ScriptCollection/other/next-release/Other/Resources/Designs/ModestDark/Style.css"
-        # TODO make designs from customizable sources be available by a customizable name and outsource this to a class-property because this is duplicated code.
-        if design_file is None:
-            design_html = f'<link rel="stylesheet" href="{design_file}">'
-        else:
-            design_html = f"{design_file}"
-
-        reference_versions_links_file_content = "    \n".join(reference_versions_html_lines)
-        title = f"{projectname}-reference"
-        reference_index_file = os.path.join(reference_folder, "index.html")
-        reference_index_file_content = f"""<!DOCTYPE html>
+            GeneralUtilities.write_message_to_stdout("Create entire reference")
+            all_available_version_identifier_folders_of_reference = list(
+                folder for folder in GeneralUtilities.get_direct_folders_of_folder(reference_repository_target_for_project))
+            all_available_version_identifier_folders_of_reference.reverse()  # move newer versions above
+            all_available_version_identifier_folders_of_reference.insert(0, all_available_version_identifier_folders_of_reference.pop())  # move latest version to the top
+            reference_versions_html_lines = []
+            for all_available_version_identifier_folder_of_reference in all_available_version_identifier_folders_of_reference:
+                version_identifier_of_project = os.path.basename(all_available_version_identifier_folder_of_reference)
+                if version_identifier_of_project == "Latest":
+                    latest_version_hint = f" (v {project_version})"
+                else:
+                    latest_version_hint = ""
+                reference_versions_html_lines.append('<hr>')
+                reference_versions_html_lines.append(f'<h2 class="display-2">{version_identifier_of_project}{latest_version_hint}</h2>')
+                reference_versions_html_lines.append("Contained codeunits:<br>")
+                reference_versions_html_lines.append("<ul>")
+                for codeunit_reference_folder in list(folder for folder in GeneralUtilities.get_direct_folders_of_folder(all_available_version_identifier_folder_of_reference)):
+                    codeunit_folder = os.path.join(information.repository, codeunitname)
+                    codeunit_version = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
+                    reference_versions_html_lines.append(f'<li><a href="./{version_identifier_of_project}/{os.path.basename(codeunit_reference_folder)}/index.html">' +
+                                                         f'{os.path.basename(codeunit_reference_folder)} {version_identifier_of_project}</a></li>')
+                reference_versions_html_lines.append("</ul>")
+
+            reference_versions_links_file_content = "    \n".join(reference_versions_html_lines)
+            title = f"{information.projectname}-reference"
+            reference_index_file = os.path.join(reference_repository_target_for_project, "index.html")
+            reference_index_file_content = f"""<!DOCTYPE html>
 <html lang="en">
 
   <head>
     <meta charset="UTF-8">
     <title>{title}</title>
-    {design_html}
+    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
   </head>
 
   <body>
-    <h1>{title}</h1>
+    <h1 class="display-1">{title}</h1>
     <hr/>
-{reference_versions_links_file_content}
+    {reference_versions_links_file_content}
   </body>
 
 </html>
 """  # see https://getbootstrap.com/docs/5.1/getting-started/introduction/
-        GeneralUtilities.write_text_to_file(reference_index_file, reference_index_file_content)
+            GeneralUtilities.write_text_to_file(reference_index_file, reference_index_file_content)
 
     @GeneralUtilities.check_arguments
-    def push_nuget_build_artifact(self, push_script_file: str, codeunitname: str, registry_address: str, api_key: str, repository_folder_name: str):
+    def push_nuget_build_artifact_for_project_in_standardized_project_structure(self, push_script_file: str, codeunitname: str,
+                                                                                registry_address: str, api_key: str):
         # when pusing to "default public" nuget-server then use registry_address: "nuget.org"
         build_artifact_folder = GeneralUtilities.resolve_relative_path(
-            f"../../Submodules/{repository_folder_name}/{codeunitname}/Other/Artifacts/BuildResult_NuGet", os.path.dirname(push_script_file))
-        self.__sc.push_nuget_build_artifact(self.__sc.find_file_by_extension(build_artifact_folder, "nupkg"),
-                                            registry_address, api_key)
+            f"../../Submodules/{codeunitname}/{codeunitname}/Other/Artifacts/BuildResult_NuGet", os.path.dirname(push_script_file))
+        self.__sc.push_nuget_build_artifact_of_repository_in_common_file_structure(self.__sc.find_file_by_extension(build_artifact_folder, "nupkg"),
+                                                                                   registry_address, api_key)
 
     @GeneralUtilities.check_arguments
     def assert_no_uncommitted_changes(self, repository_folder: str):
         if self.__sc.git_repository_has_uncommitted_changes(repository_folder):
             raise ValueError(f"Repository '{repository_folder}' has uncommitted changes.")
 
     @GeneralUtilities.check_arguments
-    def generate_certificate_for_nonproductive_purposes(self, codeunit_folder: str, domain: str,
-                                                        subj_c: str, subj_st: str, subj_l: str, subj_o: str, subj_ou: str,
-                                                        resource_name: str = "NonProductiveCertificate"):
-        target_folder = os.path.join(codeunit_folder, "Other", "Resources", resource_name)
-        certificate_file = os.path.join(target_folder, f"{domain}.unsigned.crt")
-        certificate_exists = os.path.exists(certificate_file)
-        if certificate_exists:
-            certificate_expired = GeneralUtilities.certificate_is_expired(certificate_file)
-            generate_new_certificate = certificate_expired
-        else:
-            generate_new_certificate = True
-        if generate_new_certificate:
-            GeneralUtilities.ensure_directory_does_not_exist(target_folder)
-            GeneralUtilities.ensure_directory_exists(target_folder)
-            GeneralUtilities.write_message_to_stdout("Generate TLS-certificate for non-productive purposes.")
-            self.__sc.generate_certificate(target_folder, domain, subj_c, subj_st, subj_l, subj_o, subj_ou)
-
-    @GeneralUtilities.check_arguments
     def get_codeunits(self, repository_folder: str) -> list[str]:
         result: list[str] = []
         for direct_subfolder in GeneralUtilities.get_direct_folders_of_folder(repository_folder):
             subfoldername = os.path.basename(direct_subfolder)
             if os.path.isfile(os.path.join(direct_subfolder, f"{subfoldername}.codeunit.xml")):
                 result.append(subfoldername)
         return result
 
     @GeneralUtilities.check_arguments
-    def merge_to_main_branch(self, repository_folder: str, source_branch: str = "other/next-release",
-                             target_branch: str = "main", verbosity: int = 1, additional_arguments_file: str = None, fast_forward_source_branch: bool = False) -> None:
-        # This is an automatization for automatic merges. Usual this merge would be done by a pull request in a sourcecode-version-control-platform
-        # (like GitHub, GitLab or Azure DevOps)
+    def prepare_release_by_building_code_units_and_committing_changes(self, repository_folder: str, build_repository_folder: str, codeunits: dict[str, CodeUnitConfiguration],
+                                                                      new_version_branch_name: str = "other/next-release", main_branch_name: str = "main", verbosity: int = 1) -> None:
         self.assert_no_uncommitted_changes(repository_folder)
-
-        src_branch_commit_id = self.__sc.git_get_commit_id(repository_folder,  source_branch)
-        if (src_branch_commit_id == self.__sc.git_get_commit_id(repository_folder,  target_branch)):
-            GeneralUtilities.write_message_to_stderr(
-                f"Can not merge because the source-branch and the target-branch are on the same commit (commit-id: {src_branch_commit_id})")
-
-        self.__sc.git_checkout(repository_folder, source_branch)
-        self.build_codeunits(repository_folder, verbosity, "QualityCheck", additional_arguments_file, True, None)
-        self.__sc.git_merge(repository_folder, source_branch, target_branch, False, False, None)
-        self.__sc.git_commit(repository_folder, f'Merge branch {source_branch} into {target_branch}', stage_all_changes=True, no_changes_behavior=1)
-        self.__sc.git_checkout(repository_folder, target_branch)
-        if fast_forward_source_branch:
-            self.__sc.git_merge(repository_folder, target_branch, source_branch, True, True)
+        repository_name = os.path.basename(repository_folder)
+        self.__sc.git_checkout(repository_folder, new_version_branch_name)
+        for codeunitname, codeunit_confoguration in codeunits.items():
+            self.build_codeunit(os.path.join(repository_folder, codeunitname), verbosity, "QualityCheck", codeunit_confoguration.additional_arguments_file)
+        self.__sc.git_commit(repository_folder, "Updates due to building code-units.")
+        self.__sc.git_merge(repository_folder, new_version_branch_name, main_branch_name, False, True, f'Merge branch {new_version_branch_name} into {main_branch_name}')
+        self.__sc.git_checkout(repository_folder, main_branch_name)
+        self.__sc.git_commit(build_repository_folder, f"Updated submodule {repository_name}")
 
     @GeneralUtilities.check_arguments
-    def merge_to_stable_branch(self, create_release_file: str, createRelease_configuration: CreateReleaseConfiguration):
+    def create_release_for_project_in_standardized_release_repository_format(self, create_release_file: str, createReleaseConfiguration: CreateReleaseConfiguration):
 
-        GeneralUtilities.write_message_to_stdout(f"Create release for project {createRelease_configuration.projectname}.")
+        GeneralUtilities.write_message_to_stdout(f"Create release for project {createReleaseConfiguration.projectname}.")
         folder_of_create_release_file_file = os.path.abspath(os.path.dirname(create_release_file))
 
         build_repository_folder = GeneralUtilities.resolve_relative_path(f"..{os.path.sep}..", folder_of_create_release_file_file)
         self.assert_no_uncommitted_changes(build_repository_folder)
 
-        self.__sc.git_checkout(build_repository_folder, createRelease_configuration.build_repository_branch)
-
-        repository_folder = GeneralUtilities.resolve_relative_path(f"Submodules{os.path.sep}{createRelease_configuration.repository_folder_name}", build_repository_folder)
-        mergeInformation = MergeToStableBranchInformationForProjectInCommonProjectFormat(repository_folder,
-                                                                                         createRelease_configuration.additional_arguments_file,
-                                                                                         createRelease_configuration.artifacts_folder)
+        self.__sc.git_checkout(build_repository_folder, createReleaseConfiguration.build_repository_branch)
 
-        # TODO check if repository_folder-merge-source-branch and repository_folder-merge-target-branch have different commits
-        self.assert_no_uncommitted_changes(repository_folder)
-        mergeInformation.verbosity = createRelease_configuration.verbosity
-        mergeInformation.push_target_branch = createRelease_configuration.remotename is not None
-        mergeInformation.push_target_branch_remote_name = createRelease_configuration.remotename
-        mergeInformation.push_source_branch = createRelease_configuration.remotename is not None
-        mergeInformation.push_source_branch_remote_name = createRelease_configuration.remotename
-        new_project_version = self.__standardized_tasks_merge_to_stable_branch(mergeInformation)
-
-        createReleaseInformation = CreateReleaseInformationForProjectInCommonProjectFormat(repository_folder,
-                                                                                           createRelease_configuration.artifacts_folder,
-                                                                                           createRelease_configuration.projectname,
-                                                                                           createRelease_configuration.public_repository_url,
-                                                                                           mergeInformation.targetbranch,
-                                                                                           mergeInformation.additional_arguments_file,
-                                                                                           mergeInformation.export_target,
-                                                                                           createRelease_configuration.push_artifacts_scripts_folder,
-                                                                                           createRelease_configuration.artifacts_which_have_artifacts_to_push)
-        createReleaseInformation.verbosity = createRelease_configuration.verbosity
-        self.__standardized_tasks_release_buildartifact(createReleaseInformation)
-
-        self.__sc.git_commit(createReleaseInformation.reference_repository, f"Added reference of {createRelease_configuration.projectname} v{new_project_version}")
-        if createRelease_configuration.reference_repository_remote_name is not None:
-            self.__sc.git_push(createReleaseInformation.reference_repository, createRelease_configuration.reference_repository_remote_name,
-                               createRelease_configuration.reference_repository_branch_name, createRelease_configuration.reference_repository_branch_name,
-                               verbosity=createRelease_configuration.verbosity)
-        self.__sc.git_commit(build_repository_folder, f"Added {createRelease_configuration.projectname} release v{new_project_version}")
-        GeneralUtilities.write_message_to_stdout(f"Finished release for project {createRelease_configuration.projectname} successfully.")
+        repository_folder = GeneralUtilities.resolve_relative_path(f"Submodules{os.path.sep}{createReleaseConfiguration.projectname}", build_repository_folder)
+        mergeToStableBranchInformation = MergeToStableBranchInformationForProjectInCommonProjectFormat(repository_folder)
+        mergeToStableBranchInformation.verbosity = createReleaseConfiguration.verbosity
+        mergeToStableBranchInformation.push_target_branch = createReleaseConfiguration.remotename is not None
+        mergeToStableBranchInformation.push_target_branch_remote_name = createReleaseConfiguration.remotename
+        mergeToStableBranchInformation.push_source_branch = createReleaseConfiguration.remotename is not None
+        mergeToStableBranchInformation.push_source_branch_remote_name = createReleaseConfiguration.remotename
+        mergeToStableBranchInformation.codeunits = createReleaseConfiguration.codeunits
+        new_project_version = self.__standardized_tasks_merge_to_stable_branch_for_project_in_common_project_format(mergeToStableBranchInformation)
+
+        createReleaseInformation = CreateReleaseInformationForProjectInCommonProjectFormat(repository_folder, createReleaseConfiguration.artifacts_folder,
+                                                                                           createReleaseConfiguration.projectname, createReleaseConfiguration.public_repository_url,
+                                                                                           mergeToStableBranchInformation.targetbranch)
+        createReleaseInformation.verbosity = createReleaseConfiguration.verbosity
+        createReleaseInformation.codeunits = createReleaseConfiguration.codeunits
+        self.__standardized_tasks_release_buildartifact_for_project_in_common_project_format(createReleaseInformation)
+
+        self.__sc.git_commit(createReleaseInformation.reference_repository, f"Added reference of {createReleaseConfiguration.projectname} v{new_project_version}")
+        if createReleaseConfiguration.reference_repository_remote_name is not None:
+            self.__sc.git_push(createReleaseInformation.reference_repository, createReleaseConfiguration.reference_repository_remote_name, createReleaseConfiguration.reference_repository_branch_name,
+                               createReleaseConfiguration.reference_repository_branch_name,  verbosity=createReleaseConfiguration.verbosity)
+        self.__sc.git_commit(build_repository_folder, f"Added {createReleaseConfiguration.projectname} release v{new_project_version}")
+        GeneralUtilities.write_message_to_stdout(f"Finished release for project {createReleaseConfiguration.projectname} successfully.")
         return new_project_version
 
     @GeneralUtilities.check_arguments
     def create_release_starter_for_repository_in_standardized_format(self, create_release_file: str, logfile: str, verbosity: int, addLogOverhead: bool,
                                                                      commandline_arguments: list[str]):
         # hint: arguments can be overwritten by commandline_arguments
         folder_of_this_file = os.path.dirname(create_release_file)
         verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         self.__sc.run_program("python", f"CreateRelease.py --overwrite_verbosity={str(verbosity)}",
                               folder_of_this_file,  verbosity=verbosity, log_file=logfile, addLogOverhead=addLogOverhead)
 
     @GeneralUtilities.check_arguments
-    def __standardized_tasks_merge_to_stable_branch(self, information: MergeToStableBranchInformationForProjectInCommonProjectFormat) -> str:
+    def __standardized_tasks_merge_to_stable_branch_for_project_in_common_project_format(self, information: MergeToStableBranchInformationForProjectInCommonProjectFormat) -> str:
 
-        src_branch_commit_id = self.__sc.git_get_commit_id(information.repository,  information.sourcebranch)
-        if (src_branch_commit_id == self.__sc.git_get_commit_id(information.repository,  information.targetbranch)):
+        src_branch_commit_id = self.__sc.git_get_current_commit_id(information.repository,  information.sourcebranch)
+        if(src_branch_commit_id == self.__sc.git_get_current_commit_id(information.repository,  information.targetbranch)):
             GeneralUtilities.write_message_to_stderr(
                 f"Can not merge because the source-branch and the target-branch are on the same commit (commit-id: {src_branch_commit_id})")
 
         self.assert_no_uncommitted_changes(information.repository)
         self.__sc.git_checkout(information.repository, information.sourcebranch)
         self.__sc.run_program("git", "clean -dfx", information.repository,  verbosity=information.verbosity, throw_exception_if_exitcode_is_not_zero=True)
         project_version = self.__sc.get_semver_version_from_gitversion(information.repository)
+        success = False
+        try:
+            for _, codeunit in information.codeunits.items():
+                GeneralUtilities.write_message_to_stdout(f"Start processing codeunit {codeunit.name}.")
+                self.build_codeunit(os.path.join(information.repository, codeunit.name), information.verbosity,
+                                    information.build_environment_for_qualitycheck, codeunit.additional_arguments_file)
+                GeneralUtilities.write_message_to_stdout(f"Finished processing codeunit {codeunit.name}.")
+
+            self.assert_no_uncommitted_changes(information.repository)
+            success = True
+        except Exception as exception:
+            GeneralUtilities.write_exception_to_stderr(exception, "Error while doing merge-tasks. Merge will be aborted.")
 
-        self.build_codeunits(information.repository, information.verbosity, information.target_environmenttype_for_qualitycheck,
-                             information.additional_arguments_file, False, information.export_target)
-
-        self.assert_no_uncommitted_changes(information.repository)
+        if not success:
+            raise Exception("Release was not successful.")
 
-        commit_id = self.__sc.git_merge(information.repository, information.sourcebranch, information.targetbranch, True, True)
+        commit_id = self.__sc.git_merge(information.repository, information.sourcebranch, information.targetbranch, True)
         self.__sc.git_create_tag(information.repository, commit_id, f"v{project_version}", information.sign_git_tags)
 
         if information.push_source_branch:
             GeneralUtilities.write_message_to_stdout("Push source-branch...")
             self.__sc.git_push(information.repository, information.push_source_branch_remote_name,
                                information.sourcebranch, information.sourcebranch, pushalltags=True, verbosity=information.verbosity)
 
@@ -1078,731 +743,294 @@
             GeneralUtilities.write_message_to_stdout("Push target-branch...")
             self.__sc.git_push(information.repository, information.push_target_branch_remote_name,
                                information.targetbranch, information.targetbranch, pushalltags=True, verbosity=information.verbosity)
 
         return project_version
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_build_for_docker_project(self, build_script_file: str, target_environment_type: str,
-                                                    verbosity: int, commandline_arguments: list[str]):
-        self.copy_source_files_to_output_directory(build_script_file)
-        use_cache: bool = target_environment_type != "Productive"
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+    def standardized_tasks_build_for_docker_library_project_in_common_project_structure(self, build_script_file: str, build_configuration: str, verbosity: int, commandline_arguments: list[str]):
+        use_cache: bool = build_configuration == "QualityCheck"
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         sc: ScriptCollectionCore = ScriptCollectionCore()
         codeunitname: str = Path(os.path.dirname(build_script_file)).parent.parent.name
         codeunit_folder = GeneralUtilities.resolve_relative_path("../..", str(os.path.dirname(build_script_file)))
+
         codeunitname_lower = codeunitname.lower()
-        codeunitversion = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
-        args = ["image", "build", "--pull", "--force-rm", "--progress=plain", "--build-arg", f"TargetEnvironmentType={target_environment_type}",
-                "--tag", f"{codeunitname_lower}:latest", "--tag", f"{codeunitname_lower}:{codeunitversion}", "--file", f"{codeunitname}/Dockerfile"]
+        version = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
+        args = ["image", "build", "--pull", "--force-rm", "--progress=plain", "--build-arg", f"EnvironmentStage={build_configuration}",
+                "--tag", f"{codeunitname_lower}:latest", "--tag", f"{codeunitname_lower}:{version}", "--file", "Dockerfile"]
         if not use_cache:
             args.append("--no-cache")
         args.append(".")
-        codeunit_content_folder = os.path.join(codeunit_folder)
+        codeunit_content_folder = os.path.join(codeunit_folder, codeunitname)
         sc.run_program_argsasarray("docker", args, codeunit_content_folder, verbosity=verbosity, print_errors_as_information=True)
         artifacts_folder = GeneralUtilities.resolve_relative_path("Other/Artifacts", codeunit_folder)
-        app_artifacts_folder = os.path.join(artifacts_folder, "BuildResult_OCIImage")
+        app_artifacts_folder = os.path.join(artifacts_folder, "ApplicationImage")
         GeneralUtilities.ensure_directory_does_not_exist(app_artifacts_folder)
         GeneralUtilities.ensure_directory_exists(app_artifacts_folder)
-        self.__sc.run_program_argsasarray("docker", ["save", "--output", f"{codeunitname}_v{codeunitversion}.tar",
-                                                     f"{codeunitname_lower}:{codeunitversion}"], app_artifacts_folder,
-                                          verbosity=verbosity, print_errors_as_information=True)
+        sc.run_program_argsasarray("docker", ["save", "--output", f"{codeunitname}_v{version}.tar",
+                                   f"{codeunitname_lower}:{version}"], app_artifacts_folder, verbosity=verbosity, print_errors_as_information=True)
 
     @GeneralUtilities.check_arguments
-    def generate_sbom_for_docker_image(self, build_script_file: str, verbosity: int, commandline_arguments: list[str]) -> None:
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        codeunitname: str = Path(os.path.dirname(build_script_file)).parent.parent.name
-        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", str(os.path.dirname(build_script_file)))
-        artifacts_folder = GeneralUtilities.resolve_relative_path("Other/Artifacts", codeunit_folder)
-        codeunitname_lower = codeunitname.lower()
-        sbom_folder = os.path.join(artifacts_folder, "BOM")
-        codeunitversion = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
-        GeneralUtilities.ensure_directory_exists(sbom_folder)
-        self.__sc.run_program_argsasarray("docker", ["sbom", "--format", "cyclonedx", f"{codeunitname_lower}:{codeunitversion}",
-                                                     "--output", f"{codeunitname}.{codeunitversion}.sbom.xml"], sbom_folder, verbosity=verbosity, print_errors_as_information=True)
-
-    @GeneralUtilities.check_arguments
-    def push_docker_build_artifact(self, push_artifacts_file: str, registry: str, product_name: str, codeunitname: str,
-                                   verbosity: int, push_readme: bool, commandline_arguments: list[str], repository_folder_name: str):
+    def push_docker_build_artifact_of_repository_in_common_file_structure(self, push_artifacts_file: str, registry: str, product_name: str, codeunitname: str,
+                                                                          verbosity: int, commandline_arguments: list[str]):
         folder_of_this_file = os.path.dirname(push_artifacts_file)
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        repository_folder = GeneralUtilities.resolve_relative_path(f"..{os.path.sep}..{os.path.sep}Submodules{os.path.sep}{repository_folder_name}", folder_of_this_file)
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        repository_folder = GeneralUtilities.resolve_relative_path(f"..{os.path.sep}..{os.path.sep}Submodules{os.path.sep}{product_name}", folder_of_this_file)
         codeunit_folder = os.path.join(repository_folder, codeunitname)
-        artifacts_folder = self.get_artifacts_folder(repository_folder, codeunitname)
-        applicationimage_folder = os.path.join(artifacts_folder, "BuildResult_OCIImage")
+        artifacts_folder = self.get_artifacts_folder_in_repository_in_common_repository_format(repository_folder, codeunitname)
+        applicationimage_folder = os.path.join(artifacts_folder, "ApplicationImage")
         sc = ScriptCollectionCore()
         image_file = sc.find_file_by_extension(applicationimage_folder, "tar")
         image_filename = os.path.basename(image_file)
         version = self.get_version_of_codeunit(os.path.join(codeunit_folder, f"{codeunitname}.codeunit.xml"))
         image_tag_name = codeunitname.lower()
-        repo = f"{registry}/{image_tag_name}"
-        image_latest = f"{repo}:latest"
-        image_version = f"{repo}:{version}"
+        image_latest = f"{registry}/{image_tag_name}:latest"
+        image_version = f"{registry}/{image_tag_name}:{version}"
         GeneralUtilities.write_message_to_stdout("Load image...")
         sc.run_program("docker", f"load --input {image_filename}", applicationimage_folder, verbosity=verbosity)
         GeneralUtilities.write_message_to_stdout("Tag image...")
         sc.run_program("docker", f"tag {image_tag_name}:{version} {image_latest}", verbosity=verbosity)
         sc.run_program("docker", f"tag {image_tag_name}:{version} {image_version}", verbosity=verbosity)
         GeneralUtilities.write_message_to_stdout("Push image...")
         sc.run_program("docker", f"push {image_latest}", verbosity=verbosity)
         sc.run_program("docker", f"push {image_version}", verbosity=verbosity)
-        if push_readme:
-            sc.run_program("docker", f"pushrm {repo}", codeunit_folder, verbosity=verbosity)
 
     @GeneralUtilities.check_arguments
-    def get_dependent_code_units(self, codeunit_file: str) -> set[str]:
+    def get_dependent_code_units(self, codeunit_file: str) -> list[str]:
         root: etree._ElementTree = etree.parse(codeunit_file)
-        return set(root.xpath('//cps:dependentcodeunit/text()', namespaces={
-            'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure'
-        }))
+        return root.xpath('//codeunit:dependentcodeunit/text()', namespaces={'codeunit': 'https://github.com/anionDev/ProjectTemplates'})
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_linting_for_docker_project(self, linting_script_file: str, verbosity: int, targetenvironmenttype: str, commandline_arguments: list[str]) -> None:
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
-        # TODO check if there are errors in sarif-file
-
-    def copy_licence_file(self, common_tasks_scripts_file: str):
-        folder_of_current_file = os.path.dirname(common_tasks_scripts_file)
-        license_file = GeneralUtilities.resolve_relative_path("../../License.txt", folder_of_current_file)
-        target_folder = GeneralUtilities.resolve_relative_path("Artifacts/License", folder_of_current_file)
-        GeneralUtilities.ensure_directory_exists(target_folder)
-        shutil.copy(license_file, target_folder)
+    def standardized_tasks_run_testcases_for_docker_project_in_common_project_structure(self, run_testcases_script_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]):
+        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", str(os.path.dirname(run_testcases_script_file)))
+        repository_folder: str = str(Path(os.path.dirname(run_testcases_script_file)).parent.parent.parent.absolute())
+        codeunitname: str = Path(os.path.dirname(run_testcases_script_file)).parent.parent.name
+        date = int(round(datetime.now().timestamp()))
+        # TODO generate real coverage report
+        dummy_test_coverage_file = f"""<?xml version="1.0" ?>
+        <coverage version="6.3.2" timestamp="{date}" lines-valid="0" lines-covered="0" line-rate="0" branches-covered="0" branches-valid="0" branch-rate="0" complexity="0">
+            <sources>
+                <source>{codeunitname}</source>
+            </sources>
+            <packages>
+                <package name="{codeunitname}" line-rate="0" branch-rate="0" complexity="0">
+                </package>
+            </packages>
+        </coverage>"""
+        artifacts_folder = GeneralUtilities.resolve_relative_path("Other/Artifacts", codeunit_folder)
+        testcoverage_artifacts_folder = os.path.join(artifacts_folder, "TestCoverage")
+        GeneralUtilities.ensure_directory_exists(testcoverage_artifacts_folder)
+        testcoverage_file = os.path.join(testcoverage_artifacts_folder, "TestCoverage.xml")
+        GeneralUtilities.ensure_file_exists(testcoverage_file)
+        GeneralUtilities.write_text_to_file(testcoverage_file, dummy_test_coverage_file)
+        self.standardized_tasks_generate_coverage_report(repository_folder, codeunitname, verbosity, True, buildenvironment, commandline_arguments)
+        self.update_path_of_source(repository_folder, codeunitname)
 
-    def take_readmefile_from_main_readmefile_of_repository(self, common_tasks_scripts_file: str):
-        folder_of_current_file = os.path.dirname(common_tasks_scripts_file)
-        source_file = GeneralUtilities.resolve_relative_path("../../ReadMe.md", folder_of_current_file)
-        target_file = GeneralUtilities.resolve_relative_path("../ReadMe.md", folder_of_current_file)
-        GeneralUtilities.ensure_file_does_not_exist(target_file)
-        shutil.copyfile(source_file, target_file)
+    @GeneralUtilities.check_arguments
+    def standardized_tasks_linting_for_docker_project_in_common_project_structure(self, linting_script_file: str, verbosity: int, buildenvironment: str, commandline_arguments: list[str]) -> None:
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments,  verbosity)
+        # TODO
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_do_common_tasks(self, common_tasks_scripts_file: str, version: str, verbosity: int,  targetenvironmenttype: str,  clear_artifacts_folder: bool,
-                                           additional_arguments_file: str, assume_dependent_codeunits_are_already_built: bool, commandline_arguments: list[str]) -> None:
-        additional_arguments_file = self.get_additionalargumentsfile_from_commandline_arguments(commandline_arguments, additional_arguments_file)
-        target_environmenttype = self.get_targetenvironmenttype_from_commandline_arguments(commandline_arguments, targetenvironmenttype)
-        assume_dependent_codeunits_are_already_built = self.get_assume_dependent_codeunits_are_already_built_from_commandline_arguments(commandline_arguments,
-                                                                                                                                        assume_dependent_codeunits_are_already_built)
+    def standardized_tasks_do_common_tasks(self, common_tasks_scripts_file: str, verbosity: int,  buildenvironment: str,  clear_artifacts_folder: bool,
+                                           commandline_arguments: list[str]) -> None:
+        build_environment = self.get_string_value_from_commandline_arguments(commandline_arguments, "buildenvironment",  buildenvironment)
         if commandline_arguments is None:
             raise ValueError('The "commandline_arguments"-parameter is not defined.')
         if len(commandline_arguments) == 0:
             raise ValueError('An empty array as argument for the "commandline_arguments"-parameter is not valid.')
         commandline_arguments = commandline_arguments[1:]
+        sc = ScriptCollectionCore()
         repository_folder: str = str(Path(os.path.dirname(common_tasks_scripts_file)).parent.parent.absolute())
-        codeunit_name: str = str(os.path.basename(Path(os.path.dirname(common_tasks_scripts_file)).parent.absolute()))
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        project_version = self.get_version_of_project(repository_folder)
-        codeunit_folder = os.path.join(repository_folder, codeunit_name)
+        codeunitname: str = str(os.path.basename(Path(os.path.dirname(common_tasks_scripts_file)).parent.absolute()))
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        GeneralUtilities.write_message_to_stdout(f"Build-environment: {buildenvironment}")
+
+        # Clear previously builded artifacts if desired:
+        if clear_artifacts_folder:
+            artifacts_folder = os.path.join(repository_folder, codeunitname, "Other", "Artifacts")
+            GeneralUtilities.ensure_directory_does_not_exist(artifacts_folder)
 
         # Check codeunit-conformity
-        # TODO check if foldername=="<codeunitname>[.codeunit.xml]" == <codeunitname> in file
-        codeunitfile = os.path.join(codeunit_folder, f"{codeunit_name}.codeunit.xml")
+        codeunitfile = os.path.join(repository_folder, codeunitname, f"{codeunitname}.codeunit.xml")
         if not os.path.isfile(codeunitfile):
             raise Exception(f'Codeunitfile "{codeunitfile}" does not exist.')
-        # TODO implement usage of self.reference_latest_version_of_xsd_when_generating_xml
-        namespaces = {'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure',
-                      'xsi': 'http://www.w3.org/2001/XMLSchema-instance'}
+        namespaces = {'codeunit': 'https://github.com/anionDev/ProjectTemplates', 'xsi': 'http://www.w3.org/2001/XMLSchema-instance'}
         root: etree._ElementTree = etree.parse(codeunitfile)
-
-        # Check codeunit-spcecification-version
-        codeunit_file_version = root.xpath('//cps:codeunit/@codeunitspecificationversion', namespaces=namespaces)[0]
-        supported_codeunitspecificationversion = "1.4.0"
+        codeunit_file_version = root.xpath('//codeunit:codeunit/@codeunitspecificationversion',  namespaces=namespaces)[0]
+        supported_codeunitspecificationversion = "1.1.0"
         if codeunit_file_version != supported_codeunitspecificationversion:
             raise ValueError(f"ScriptCollection only supports processing codeunits with codeunit-specification-version={supported_codeunitspecificationversion}.")
-        schemaLocation = root.xpath('//cps:codeunit/@xsi:schemaLocation', namespaces=namespaces)[0]
+        schemaLocation = root.xpath('//codeunit:codeunit/@xsi:schemaLocation',  namespaces=namespaces)[0]
         xmlschema.validate(codeunitfile, schemaLocation)
 
-        # Check codeunit-name
-        codeunit_name_in_codeunit_file = root.xpath('//cps:codeunit/cps:name/text()', namespaces=namespaces)[0]
-        if codeunit_name != codeunit_name_in_codeunit_file:
-            raise ValueError(f"The folder-name ('{codeunit_name}') is not equal to the codeunit-name ('{codeunit_name_in_codeunit_file}').")
-
-        # Check developer
-        if self.validate_developers_of_repository:
-            expected_authors: list[tuple[str, str]] = []
-            expected_authors_in_xml = root.xpath('//cps:codeunit/cps:developerteam/cps:developer', namespaces=namespaces)
-            for expected_author in expected_authors_in_xml:
-                author_name = expected_author.xpath('./cps:developername/text()', namespaces=namespaces)[0]
-                author_emailaddress = expected_author.xpath('./cps:developeremailaddress/text()', namespaces=namespaces)[0]
-                expected_authors.append((author_name, author_emailaddress))
-            actual_authors: list[tuple[str, str]] = self.__sc.get_all_authors_and_committers_of_repository(repository_folder, codeunit_name, verbosity)
-            for actual_author in actual_authors:
-                if not (actual_author) in expected_authors:
-                    actual_author_formatted = f"{actual_author[0]} <{actual_author[1]}>"
-                    raise ValueError(f'Author/Comitter "{actual_author_formatted}" is not in the codeunit-developer-team. If {actual_author} is a '
-                                     + 'authorized developer for this codeunit you should consider defining this in the codeunit-file or adapting the name using a '
-                                     + '.mailmap-file (see https://git-scm.com/docs/gitmailmap). The developer-team-check can also be disabled using '
-                                     + 'the property validate_developers_of_repository.')
-
-        # TODO implement cycle-check for dependent codeunits
-
-        # Clear previously builded artifacts if desired:
-        if clear_artifacts_folder:
-            artifacts_folder = os.path.join(codeunit_folder, "Other", "Artifacts")
-            GeneralUtilities.ensure_directory_does_not_exist(artifacts_folder)
-
-        # Get artifacts from dependent codeunits
-        if assume_dependent_codeunits_are_already_built:
-            pass  # TODO do basic checks to verify dependent codeunits are really there and raise exception if not
-        else:
-            self.build_dependent_code_units(repository_folder, codeunit_name, verbosity, target_environmenttype, additional_arguments_file)
-        self.copy_artifacts_from_dependent_code_units(repository_folder, codeunit_name)
+        # Update version
+        version = sc.get_semver_version_from_gitversion(GeneralUtilities.resolve_relative_path("../..", os.path.dirname(common_tasks_scripts_file)))
+        self.update_version_of_codeunit_to_project_version(common_tasks_scripts_file, version)
 
-        # Update codeunit-version
-        self.update_version_of_codeunit(common_tasks_scripts_file, version)
-
-        # set default constants
-        self.set_default_constants(os.path.join(codeunit_folder))
-
-        # Copy changelog-file
-        changelog_folder = os.path.join(repository_folder, "Other", "Resources", "Changelog")
-        changelog_file = os.path.join(changelog_folder, f"v{project_version}.md")
-        target_folder = os.path.join(codeunit_folder, "Other", "Artifacts", "Changelog")
-        GeneralUtilities.ensure_directory_exists(target_folder)
-        shutil.copy(changelog_file, target_folder)
-
-        # Hints-file
-        hints_file = os.path.join(codeunit_folder, "Other", "Hints.md")
-        if not os.path.isfile(hints_file):
-            raise ValueError(f"Hints-file '{hints_file}' does not exist.")
-
-        # Copy license-file
-        self.copy_licence_file(common_tasks_scripts_file)
-
-    @GeneralUtilities.check_arguments
-    def get_version_of_project(self, repository_folder: str):
-        return ScriptCollectionCore().get_semver_version_from_gitversion(repository_folder)
+        # Build dependent code units
+        additional_arguments_file = self.get_string_value_from_commandline_arguments(commandline_arguments, "additionalargumentsfile",  None)
+        self.build_dependent_code_units(repository_folder, codeunitname, verbosity, build_environment, additional_arguments_file)
 
     @GeneralUtilities.check_arguments
-    def replace_common_variables_in_nuspec_file(self, codeunit_folder: str):
-        codeunit_name = os.path.basename(codeunit_folder)
-        version = self.get_version_of_codeunit_folder(codeunit_folder)
-        nuspec_file = os.path.join(codeunit_folder, "Other", "Build", f"{codeunit_name}.nuspec")
-        self.__sc.replace_version_in_nuspec_file(nuspec_file, version)
-
-    @GeneralUtilities.check_arguments
-    def standardized_tasks_build_for_node_project(self, build_script_file: str, build_environment_target_type: str,
-                                                  verbosity: int, commandline_arguments: list[str]):
+    def standardized_tasks_build_for_node_project_in_common_project_structure(self, build_script_file: str,
+                                                                              build_configuration: str, verbosity: int, commandline_arguments: list[str]):
         # TODO use unused parameter
-        self.copy_source_files_to_output_directory(build_script_file)
         sc = ScriptCollectionCore()
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         sc.program_runner = ProgramRunnerEpew()
         build_script_folder = os.path.dirname(build_script_file)
         codeunit_folder = GeneralUtilities.resolve_relative_path("../..", build_script_folder)
-        sc.run_program("npm", "run build", codeunit_folder, verbosity=verbosity)
-        self.standardized_tasks_build_bom_for_node_project(codeunit_folder, verbosity, commandline_arguments)
-
-    @GeneralUtilities.check_arguments
-    def standardized_tasks_build_bom_for_node_project(self, codeunit_folder: str, verbosity: int, commandline_arguments: list[str]):
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        # TODO
+        sc.run_program("npm", "run build", codeunit_folder)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_linting_for_node_project(self, linting_script_file: str, verbosity: int,
-                                                    target_environmenttype: str, commandline_arguments: list[str]):
+    def standardized_tasks_linting_for_node_project_in_common_project_structure(self, linting_script_file: str, verbosity: int,
+                                                                                build_environment: str, commandline_arguments: list[str]):
         # TODO use unused parameter
         sc = ScriptCollectionCore()
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         sc.program_runner = ProgramRunnerEpew()
         build_script_folder = os.path.dirname(linting_script_file)
         codeunit_folder = GeneralUtilities.resolve_relative_path("../..", build_script_folder)
-        sc.run_program("npm", "run lint", codeunit_folder, verbosity=verbosity)
-        # TODO check if there are errors in sarif-file
+        sc.run_program("npm", "run lint", codeunit_folder)
 
     @GeneralUtilities.check_arguments
-    def standardized_tasks_run_testcases_for_node_project(self, runtestcases_script_file: str,
-                                                          targetenvironmenttype: str, generate_badges: bool, verbosity: int,
-                                                          commandline_arguments: list[str]):
-        # TODO use targetenvironmenttype etc.
+    def standardized_tasks_run_testcases_for_node_project_in_common_project_structure(self, runtestcases_script_file: str,
+                                                                                      buildenvironment: str, generate_badges: bool, verbosity: int,
+                                                                                      commandline_arguments: list[str]):
+        # TODO really use buildenvironment etc.
         sc = ScriptCollectionCore()
-        codeunit_name: str = os.path.basename(str(Path(os.path.dirname(runtestcases_script_file)).parent.parent.absolute()))
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
+        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
         sc.program_runner = ProgramRunnerEpew()
-        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", os.path.dirname(runtestcases_script_file))
-        sc.run_program("npm", "run test", codeunit_folder, verbosity=verbosity)
+        build_script_folder = os.path.dirname(runtestcases_script_file)
+        codeunit_folder = GeneralUtilities.resolve_relative_path("../..", build_script_folder)
+        sc.run_program("npm", "run test", codeunit_folder)
         coverage_folder = os.path.join(codeunit_folder, "Other", "Artifacts", "TestCoverage")
         target_file = os.path.join(coverage_folder, "TestCoverage.xml")
         GeneralUtilities.ensure_file_does_not_exist(target_file)
         os.rename(os.path.join(coverage_folder, "cobertura-coverage.xml"), target_file)
         repository_folder = GeneralUtilities.resolve_relative_path("..", codeunit_folder)
-        self.run_testcases_common_post_task(repository_folder, codeunit_name, verbosity, generate_badges, targetenvironmenttype, commandline_arguments)
+        codeunitname = os.path.basename(codeunit_folder)
+        self.check_testcoverage_for_project_in_common_project_structure(target_file, repository_folder, codeunitname)
+        self.standardized_tasks_generate_coverage_report(repository_folder, codeunitname, verbosity, generate_badges, buildenvironment, commandline_arguments)
+        self.update_path_of_source(repository_folder, codeunitname)
 
     @GeneralUtilities.check_arguments
     def do_npm_install(self, package_json_folder: str, verbosity: int):
         sc = ScriptCollectionCore()
         sc.program_runner = ProgramRunnerEpew()
-        sc.run_program("npm", "install", package_json_folder, verbosity=verbosity)
+        sc.run_program("npm", "install", package_json_folder, verbosity=int)
 
     @GeneralUtilities.check_arguments
-    def set_default_constants(self, codeunit_folder: str):
-        self.set_constant_for_commitid(codeunit_folder)
-        self.set_constant_for_commitdate(codeunit_folder)
-        self.set_constant_for_commitname(codeunit_folder)
-        self.set_constant_for_commitversion(codeunit_folder)
-
-    @GeneralUtilities.check_arguments
-    def set_constant_for_commitid(self, codeunit_folder: str):
-        commit_id = self.__sc.git_get_commit_id(codeunit_folder)
-        self.set_constant(codeunit_folder, "CommitId", commit_id)
-
-    @GeneralUtilities.check_arguments
-    def set_constant_for_commitdate(self, codeunit_folder: str):
-        commit_date: datetime = self.__sc.git_get_commit_date(codeunit_folder)
-        self.set_constant(codeunit_folder, "CommitDate", GeneralUtilities.datetime_to_string(commit_date))
-
-    @GeneralUtilities.check_arguments
-    def set_constant_for_commitname(self, codeunit_folder: str):
-        codeunit_name: str = os.path.basename(codeunit_folder)
-        self.set_constant(codeunit_folder, "CodeUnitName", codeunit_name)
-
-    @GeneralUtilities.check_arguments
-    def set_constant_for_commitversion(self, codeunit_folder: str):
-        codeunit_version: str = self.get_version_of_codeunit_folder(codeunit_folder)
-        self.set_constant(codeunit_folder, "CodeUnitVersion", codeunit_version)
-
-    @GeneralUtilities.check_arguments
-    def set_constant(self, codeunit_folder: str, constantname: str, constant_value: str, documentationsummary: str = None, constants_valuefile: str = None):
-        if documentationsummary is None:
-            documentationsummary = ""
-        constants_folder = os.path.join(codeunit_folder, "Other", "Resources", "Constants")
-        GeneralUtilities.ensure_directory_exists(constants_folder)
-        constants_metafile = os.path.join(constants_folder, f"{constantname}.constant.xml")
-        if constants_valuefile is None:
-            constants_valuefile_folder = constants_folder
-            constants_valuefile_name = f"{constantname}.value.txt"
-            constants_valuefiler_reference = f"./{constants_valuefile_name}"
-        else:
-            constants_valuefile_folder = os.path.dirname(constants_valuefile)
-            constants_valuefile_name = os.path.basename(constants_valuefile)
-            constants_valuefiler_reference = os.path.join(constants_valuefile_folder, constants_valuefile_name)
-
-        # TODO implement usage of self.reference_latest_version_of_xsd_when_generating_xml
-        GeneralUtilities.write_text_to_file(constants_metafile, f"""<?xml version="1.0" encoding="UTF-8" ?>
-<cps:constant xmlns:cps="https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure" constantspecificationversion="1.1.0"
-    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/raw/main/Conventions/RepositoryStructure/CommonProjectStructure/constant.xsd">
-    <cps:name>{constantname}</cps:name>
-    <cps:documentationsummary>{documentationsummary}</cps:documentationsummary>
-    <cps:path>{constants_valuefiler_reference}</cps:path>
-</cps:constant>""")
-        # TODO validate generated xml against xsd
-        GeneralUtilities.write_text_to_file(os.path.join(constants_valuefile_folder, constants_valuefile_name), constant_value)
-
-    @GeneralUtilities.check_arguments
-    def get_constant_value(self, source_codeunit_folder: str, constant_name: str) -> str:
-        value_file_relative = self.__get_constant_helper(source_codeunit_folder, constant_name, "path")
-        value_file = GeneralUtilities.resolve_relative_path(value_file_relative, os.path.join(source_codeunit_folder, "Other", "Resources", "Constants"))
-        return GeneralUtilities.read_text_from_file(value_file)
-
-    @GeneralUtilities.check_arguments
-    def get_constant_documentation(self, source_codeunit_folder: str, constant_name: str) -> str:
-        return self.__get_constant_helper(source_codeunit_folder, constant_name, "documentationsummary")
-
-    @GeneralUtilities.check_arguments
-    def __get_constant_helper(self, source_codeunit_folder: str, constant_name: str, propertyname: str) -> str:
-        root: etree._ElementTree = etree.parse(os.path.join(source_codeunit_folder, "Other", "Resources", "Constants", f"{constant_name}.constant.xml"))
-        results = root.xpath(f'//cps:{propertyname}/text()', namespaces={
-            'cps': 'https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure'
-        })
-        length = len(results)
-        if (length == 0):
-            return ""
-        elif length == 1:
-            return results[0]
-        else:
-            raise ValueError("Too many results found.")
-
-    @GeneralUtilities.check_arguments
-    def set_constants_for_certificate_public_information(self, codeunit_folder: str, domain: str, source_constant_name: str = "NonProductiveCertificate"):
-        """Expects a certificate-resource and generates a constant for its public information"""
-        certificate_file = os.path.join(codeunit_folder, "Other", "Resources", source_constant_name, f"{domain}.unsigned.crt")
-        with open(certificate_file, encoding="utf-8") as text_wrapper:
-            certificate = crypto.load_certificate(crypto.FILETYPE_PEM, text_wrapper.read())
-        certificate_publickey = crypto.dump_publickey(crypto.FILETYPE_PEM, certificate.get_pubkey()).decode("utf-8")
-        self.set_constant(codeunit_folder, source_constant_name+"PublicKey", certificate_publickey)
-
-    @GeneralUtilities.check_arguments
-    def set_constants_for_certificate_private_information(self, codeunit_folder: str, certificate_resource_name: str = "NonProductiveCertificate"):
-        """Expects a certificate-resource and generates a constant for its sensitive information in hex-format"""
-        self.__generate_constant_from_resource(codeunit_folder, certificate_resource_name, "password", "Password")
-        self.__generate_constant_from_resource(codeunit_folder, certificate_resource_name, "pfx", "PFX")
-
-    @GeneralUtilities.check_arguments
-    def __generate_constant_from_resource(self, codeunit_folder: str, resource_name: str, extension: str, constant_name: str):
-        certificate_resource_folder = GeneralUtilities.resolve_relative_path(f"Other/Resources/{resource_name}", codeunit_folder)
-        resource_file = self.__sc.find_file_by_extension(certificate_resource_folder, extension)
-        resource_file_content = GeneralUtilities.read_binary_from_file(resource_file)
-        resource_file_as_hex = resource_file_content.hex()
-        self.set_constant(codeunit_folder, f"{resource_name}{constant_name}Hex", resource_file_as_hex)
-
-    @GeneralUtilities.check_arguments
-    def copy_constant_from_dependent_codeunit(self, codeunit_folder: str, constant_name: str, source_codeunit_name: str):
-        source_codeunit_folder: str = GeneralUtilities.resolve_relative_path(f"../{source_codeunit_name}", codeunit_folder)
-        value = self.get_constant_value(source_codeunit_folder, constant_name)
-        documentation = self.get_constant_documentation(source_codeunit_folder, constant_name)
-        self.set_constant(codeunit_folder, constant_name, value, documentation)
-
-    @GeneralUtilities.check_arguments
-    def copy_resources_from_dependent_codeunit(self, codeunit_folder: str, resource_name: str, source_codeunit_name: str):
-        source_folder: str = GeneralUtilities.resolve_relative_path(f"../{source_codeunit_name}/Other/Resources/{resource_name}", codeunit_folder)
-        target_folder: str = GeneralUtilities.resolve_relative_path(f"Other/Resources/{resource_name}", codeunit_folder)
-        GeneralUtilities.ensure_directory_does_not_exist(target_folder)
-        shutil.copytree(source_folder, target_folder)
-
-    @GeneralUtilities.check_arguments
-    def generate_openapi_file(self, buildscript_file: str, runtime: str, verbosity: int, commandline_arguments: list[str],
-                              swagger_document_name: str = "APISpecification") -> None:
-        codeunitname = os.path.basename(str(Path(os.path.dirname(buildscript_file)).parent.parent.absolute()))
-        repository_folder = str(Path(os.path.dirname(buildscript_file)).parent.parent.parent.absolute())
-        artifacts_folder = os.path.join(repository_folder, codeunitname, "Other", "Artifacts")
-        GeneralUtilities.ensure_directory_exists(os.path.join(artifacts_folder, "APISpecification"))
-        verbosity = self.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        version = self.get_version_of_codeunit_folder(os.path.join(repository_folder, codeunitname))
-        self.__sc.run_program("swagger", f"tofile --output APISpecification\\{codeunitname}.v{version}.api.json" +
-                              f" BuildResult_DotNet_{runtime}\\{codeunitname}.dll {swagger_document_name}",
-                              artifacts_folder, verbosity=verbosity)
-
-    @GeneralUtilities.check_arguments
-    def replace_version_in_packagejson_file(self, packagejson_file: str, version: str):
-        encoding = "utf-8"
-        with open(packagejson_file, encoding=encoding) as f:
+    def replace_version_in_package_file(self: ScriptCollectionCore, package_json_file: str, version: str):
+        filename = package_json_file
+        with open(filename, 'r', encoding="utf-8") as f:
             data = json.load(f)
-        data['version'] = version
-        with open(packagejson_file, 'w', encoding=encoding) as f:
+            data['version'] = version
+        os.remove(filename)
+        with open(filename, 'w', encoding="utf-8") as f:
             json.dump(data, f, indent=2)
 
     @GeneralUtilities.check_arguments
-    def build_dependent_code_units(self, repo_folder: str, codeunit_name: str, verbosity: int, target_environmenttype: str,
-                                   additional_arguments_file: str) -> None:
-        codeunit_file = os.path.join(repo_folder, codeunit_name, codeunit_name + ".codeunit.xml")
-        dependent_codeunits = self.get_dependent_code_units(codeunit_file)
-        dependent_codeunits_folder = os.path.join(repo_folder, codeunit_name, "Other", "Resources", "DependentCodeUnits")
-        GeneralUtilities.ensure_directory_does_not_exist(dependent_codeunits_folder)
-        if 0 < len(dependent_codeunits):
-            GeneralUtilities.write_message_to_stdout(f"Start building dependent codeunits for codeunit {codeunit_name}.")
-        for dependent_codeunit in dependent_codeunits:
-            self.__build_codeunit(os.path.join(repo_folder, dependent_codeunit), verbosity, target_environmenttype, additional_arguments_file)
-        if 0 < len(dependent_codeunits):
-            GeneralUtilities.write_message_to_stdout(f"Finished building dependent codeunits for codeunit {codeunit_name}.")
-
-    @GeneralUtilities.check_arguments
-    def copy_artifacts_from_dependent_code_units(self, repo_folder: str, codeunit_name: str) -> None:
-        GeneralUtilities.write_message_to_stdout(f"Get dependent artifacts for codeunit {codeunit_name}.")
+    def build_dependent_code_units(self, repo_folder: str, codeunit_name: str, verbosity: int, build_environment: str, additional_arguments_file: str) -> None:
         codeunit_file = os.path.join(repo_folder, codeunit_name, codeunit_name + ".codeunit.xml")
         dependent_codeunits = self.get_dependent_code_units(codeunit_file)
         dependent_codeunits_folder = os.path.join(repo_folder, codeunit_name, "Other", "Resources", "DependentCodeUnits")
         GeneralUtilities.ensure_directory_does_not_exist(dependent_codeunits_folder)
         for dependent_codeunit in dependent_codeunits:
+            other_folder = os.path.join(repo_folder, codeunit_name, "Other")
+            artifacts_folder = os.path.join(other_folder, "Artifacts")
+            self.build_codeunit(os.path.join(repo_folder, dependent_codeunit), verbosity, build_environment, additional_arguments_file)
             target_folder = os.path.join(dependent_codeunits_folder, dependent_codeunit)
             GeneralUtilities.ensure_directory_does_not_exist(target_folder)
-            other_folder = os.path.join(repo_folder, dependent_codeunit, "Other")
-            artifacts_folder = os.path.join(other_folder, "Artifacts")
             shutil.copytree(artifacts_folder, target_folder)
 
     @GeneralUtilities.check_arguments
-    def add_github_release(self, productname: str, projectversion: str, build_artifacts_folder: str, github_username: str, repository_folder: str,
-                           verbosity: int, commandline_arguments: list[str]):
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        github_repo = f"{github_username}/{productname}"
-        artifact_files = []
-        codeunits = self.get_codeunits(repository_folder)
-        for codeunit in codeunits:
-            artifact_files.append(self.__sc.find_file_by_extension(f"{build_artifacts_folder}\\{productname}\\{projectversion}\\{codeunit}", "Productive.Artifacts.zip"))
-        changelog_file = os.path.join(repository_folder, "Other", "Resources", "Changelog", f"v{projectversion}.md")
-        self.__sc.run_program_argsasarray("gh", ["release", "create", f"v{projectversion}", "--repo",  github_repo,  "--notes-file", changelog_file,
-                                                 "--title", f"Release v{projectversion}"]+artifact_files, verbosity=verbosity)
-
-    @GeneralUtilities.check_arguments
-    def standardized_tasks_update_version_in_docker_examples(self, file, codeunit_version):
-        folder_of_current_file = os.path.dirname(file)
-        codeunit_folder = GeneralUtilities.resolve_relative_path("..", folder_of_current_file)
-        codeunit_name = os.path.basename(codeunit_folder)
-        codeunit_name_lower = codeunit_name.lower()
-        examples_folder = GeneralUtilities.resolve_relative_path("Other/Reference/ReferenceContent/Examples", codeunit_folder)
-        for example_folder in GeneralUtilities.get_direct_folders_of_folder(examples_folder):
-            docker_compose_file = os.path.join(example_folder, "docker-compose.yml")
-            if os.path.isfile(docker_compose_file):
-                filecontent = GeneralUtilities.read_text_from_file(docker_compose_file)
-                replaced = re.sub(f'image:\\s+{codeunit_name_lower}:\\d+\\.\\d+\\.\\d+', f"image: {codeunit_name_lower}:{codeunit_version}", filecontent)
-                GeneralUtilities.write_text_to_file(docker_compose_file, replaced)
-
-    @GeneralUtilities.check_arguments
-    def run_dockerfile_example(self, current_file: str, verbosity: int, remove_old_container: bool, remove_volumes_folder: bool, commandline_arguments: list[str]):
-        verbosity = TasksForCommonProjectStructure.get_verbosity_from_commandline_arguments(commandline_arguments, verbosity)
-        folder = os.path.dirname(current_file)
-        example_name = os.path.basename(folder)
-        GeneralUtilities.write_message_to_stdout(f'Run "{example_name}"-example')
-        sc = ScriptCollectionCore()
-        oci_image_artifacts_folder = GeneralUtilities.resolve_relative_path("../../../../Artifacts/BuildResult_OCIImage", folder)
-        image_filename = os.path.basename(sc.find_file_by_extension(oci_image_artifacts_folder, "tar"))
-        codeunit_name = os.path.basename(GeneralUtilities.resolve_relative_path("../../../../..", folder))
-        codeunit_name_lower = codeunit_name.lower()
-        if remove_old_container:
-            GeneralUtilities.write_message_to_stdout(f"Ensure container {codeunit_name_lower} does not exist...")
-            sc.run_program("docker", f"container rm -f {codeunit_name_lower}", oci_image_artifacts_folder, verbosity=verbosity)
-        if remove_volumes_folder:
-            volumes_folder = os.path.join(folder, "Volumes")
-            GeneralUtilities.write_message_to_stdout(f"Ensure volumes-folder '{volumes_folder}' does not exist...")
-            GeneralUtilities.ensure_directory_does_not_exist(volumes_folder)
-            GeneralUtilities.ensure_directory_exists(volumes_folder)
-        GeneralUtilities.write_message_to_stdout("Load docker-image...")
-        sc.run_program("docker", f"load -i {image_filename}", oci_image_artifacts_folder, verbosity=verbosity)
-        project_name = f"{codeunit_name}_{example_name}".lower()
-        sc_epew = ScriptCollectionCore()
-        sc_epew.program_runner = ProgramRunnerEpew()
-        GeneralUtilities.write_message_to_stdout("Start docker-container...")
-        sc_epew.run_program("docker-compose", f"--project-name {project_name} up", folder, verbosity=verbosity)
-
-    @GeneralUtilities.check_arguments
-    def _internal_sort_codenits(self, codeunits=dict[str, set[str]]) -> list[str]:
-        result: list[str] = list[str]()
-        ts = TopologicalSorter(codeunits)
-        result = list(ts.static_order())
-        return result
-
-    @GeneralUtilities.check_arguments
-    def build_codeunit(self, codeunit_folder: str, verbosity: int = 1, target_environmenttype: str = "QualityCheck", additional_arguments_file: str = None,
-                       is_pre_merge: bool = False, export_target_directory: str = None) -> None:
-        codeunit_folder = GeneralUtilities.resolve_relative_path_from_current_working_directory(codeunit_folder)
-        codeunit_name = os.path.basename(codeunit_folder)
-        repository_folder = os.path.dirname(codeunit_folder)
-        self.build_specific_codeunits(repository_folder, [codeunit_name], verbosity, target_environmenttype, additional_arguments_file, is_pre_merge, export_target_directory)
-
-    @GeneralUtilities.check_arguments
-    def build_codeunits(self, repository_folder: str, verbosity: int = 1, target_environmenttype: str = "QualityCheck", additional_arguments_file: str = None,
-                        is_pre_merge: bool = False, export_target_directory: str = None) -> None:
-        repository_folder = GeneralUtilities.resolve_relative_path_from_current_working_directory(repository_folder)
-        codeunits = self.get_codeunits(repository_folder)
-        self.build_specific_codeunits(repository_folder, codeunits, verbosity, target_environmenttype, additional_arguments_file, is_pre_merge, export_target_directory)
-
-    @GeneralUtilities.check_arguments
-    def build_specific_codeunits(self, repository_folder: str, codeunits: list[str], verbosity: int = 1, target_environmenttype: str = "QualityCheck",
-                                 additional_arguments_file: str = None, is_pre_merge: bool = False, export_target_directory: str = None) -> None:
-        repository_folder = GeneralUtilities.resolve_relative_path_from_current_working_directory(repository_folder)
-        contains_uncommitted_changes = self.__sc.git_repository_has_uncommitted_changes(repository_folder)
-        if is_pre_merge and contains_uncommitted_changes:
-            raise ValueError(f'Repository "{repository_folder}" has uncommitted changes.')
-        subfolders = [os.path.join(repository_folder, codeunit) for codeunit in codeunits]
-        codeunits_with_dependent_codeunits: dict[str, set[str]] = dict[str, set[str]]()
+    def build_codeunits(self, repository_folder: str, verbosity: int = 1, build_environment: str = "QualityCheck", additional_arguments_file: str = None) -> None:
+        codeunits = []
+        subfolders = GeneralUtilities.get_direct_folders_of_folder(repository_folder)
         for subfolder in subfolders:
-            codeunit_name: str = os.path.basename(subfolder)
+            codeunit_name = os.path.basename(subfolder)
             codeunit_file = os.path.join(subfolder, f"{codeunit_name}.codeunit.xml")
             if os.path.exists(codeunit_file):
-                codeunits_with_dependent_codeunits[codeunit_name] = self.get_dependent_code_units(codeunit_file)
-            else:
-                raise ValueError(f"{repository_folder} does not have a codeunit with name {codeunit_name}.")
-        sorted_codeunits = self._internal_sort_codenits(codeunits_with_dependent_codeunits)
-        project_version = self.get_version_of_project(repository_folder)
-        if len(sorted_codeunits) == 0:
-            raise ValueError(f'No codeunit found in subfolders of "{repository_folder}".')
-        else:
-            if verbosity > 1:
-                GeneralUtilities.write_message_to_stdout("Attempt to build codeunits in the following order:")
-                i = 0
-                for codeunit in sorted_codeunits:
-                    i = i+1
-                    GeneralUtilities.write_message_to_stdout(f"{i}.: {codeunit}")
-            self.__do_repository_checks(repository_folder, project_version)
-            line = "----------"
-            for codeunit in sorted_codeunits:
-                GeneralUtilities.write_message_to_stdout(line)
-                self.__build_codeunit(os.path.join(repository_folder, codeunit), verbosity, target_environmenttype, additional_arguments_file, is_pre_merge, True)
-            GeneralUtilities.write_message_to_stdout(line)
-        if not contains_uncommitted_changes and self.__sc.git_repository_has_uncommitted_changes(repository_folder) and not is_pre_merge:
-            message = f'Due to the build-process the repository "{repository_folder}" has new uncommitted changes.'
-            if target_environmenttype == "Development":
-                GeneralUtilities.write_message_to_stdout(message)
-            else:
-                raise ValueError(message)
-        if export_target_directory is not None:
-            project_name = os.path.basename(repository_folder)
-            for codeunit in sorted_codeunits:
-                codeunit_version = self.get_version_of_codeunit_folder(os.path.join(repository_folder,  codeunit))
-                artifacts_folder = os.path.join(repository_folder,  codeunit, "Other", "Artifacts")
-                target_folder = os.path.join(export_target_directory, project_name, project_version, codeunit)
-                GeneralUtilities.ensure_directory_does_not_exist(target_folder)
-                GeneralUtilities.ensure_directory_exists(target_folder)
-                filename_without_extension = f"{codeunit}.v{codeunit_version}.{target_environmenttype}.Artifacts"
-                shutil.make_archive(filename_without_extension, 'zip', artifacts_folder)
-                archive_file = os.path.join(os.getcwd(), f"{filename_without_extension}.zip")
-                shutil.move(archive_file, target_folder)
-
-    @GeneralUtilities.check_arguments
-    def __do_repository_checks(self, repository_folder: str, project_version: str):
-        self.__check_if_changelog_exists(repository_folder, project_version)
-        self.__check_whether_security_txt_exists(repository_folder)
-
-    @GeneralUtilities.check_arguments
-    def __check_whether_security_txt_exists(self, repository_folder: str):
-        security_txt_file_relative = ".well-known/security.txt"
-        security_txt_file = GeneralUtilities.resolve_relative_path(security_txt_file_relative, repository_folder)
-        if not os.path.isfile(security_txt_file):
-            raise ValueError(f"The repository does not contain a '{security_txt_file_relative}'-file. See https://securitytxt.org/ for more information.")
-
-    @GeneralUtilities.check_arguments
-    def __check_if_changelog_exists(self, repository_folder: str, project_version: str):
-        changelog_folder = os.path.join(repository_folder, "Other", "Resources", "Changelog")
-        changelog_file = os.path.join(changelog_folder, f"v{project_version}.md")
-        if not os.path.isfile(changelog_file):
-            raise ValueError(f"Changelog-file '{changelog_file}' does not exist.")
-
-    @GeneralUtilities.check_arguments
-    def ensure_grylibrary_is_available(self, codeunit_folder: str):
-        grylibrary_folder = os.path.join(codeunit_folder, "Other", "Resources", "GRYLibrary")
-        grylibrary_dll_file = os.path.join(grylibrary_folder, "BuildResult_DotNet_win-x64", "GRYLibrary.dll")
-        internet_connection_is_available = GeneralUtilities.internet_connection_is_available()
-        grylibrary_dll_file_exists = os.path.isfile(grylibrary_dll_file)
-        if internet_connection_is_available:  # Load/Update GRYLibrary
-            grylibrary_latest_codeunit_file = "https://raw.githubusercontent.com/anionDev/GRYLibrary/stable/GRYLibrary/GRYLibrary.codeunit.xml"
-            with urllib.request.urlopen(grylibrary_latest_codeunit_file) as url_result:
-                grylibrary_latest_version = self.get_version_of_codeunit_file_content(url_result.read().decode("utf-8"))
-            if grylibrary_dll_file_exists:
-                grylibrary_existing_codeunit_file = os.path.join(grylibrary_folder, "SourceCode", "GRYLibrary.codeunit.xml")
-                grylibrary_existing_codeunit_version = self.get_version_of_codeunit(grylibrary_existing_codeunit_file)
-                if grylibrary_existing_codeunit_version != grylibrary_latest_version:
-                    GeneralUtilities.ensure_directory_does_not_exist(grylibrary_folder)
-            if not os.path.isfile(grylibrary_dll_file):
-                GeneralUtilities.ensure_directory_does_not_exist(grylibrary_folder)
-                GeneralUtilities.ensure_directory_exists(grylibrary_folder)
-                archive_name = f"GRYLibrary.v{grylibrary_latest_version}.Productive.Artifacts.zip"
-                archive_download_link = f"https://github.com/anionDev/GRYLibrary/releases/download/v{grylibrary_latest_version}/{archive_name}"
-                archive_file = os.path.join(grylibrary_folder, archive_name)
-                urllib.request.urlretrieve(archive_download_link, archive_file)
-                with zipfile.ZipFile(archive_file, 'r') as zip_ref:
-                    zip_ref.extractall(grylibrary_folder)
-                GeneralUtilities.ensure_file_does_not_exist(archive_file)
-        else:
-            if grylibrary_dll_file_exists:
-                GeneralUtilities.write_message_to_stdout("Warning: Can not check for updates of GRYLibrary due to missing internet-connection.")
-            else:
-                raise ValueError("Can not download GRYLibrary.")
-
-    @GeneralUtilities.check_arguments
-    def verify_artifact_exists(self, codeunit_folder: str, artifact_name_regexes: dict[str, bool]) -> None:
-        codeunit_name: str = os.path.basename(codeunit_folder)
-        artifacts_folder = os.path.join(codeunit_folder, "Other/Artifacts")
-        existing_artifacts = [os.path.basename(x) for x in GeneralUtilities.get_direct_folders_of_folder(artifacts_folder)]
-        for artifact_name_regex, required in artifact_name_regexes.items():
-            artifact_exists = False
-            for existing_artifact in existing_artifacts:
-                pattern = re.compile(artifact_name_regex)
-                if pattern.match(existing_artifact):
-                    artifact_exists = True
-            if not artifact_exists:
-                message = f"Codeunit {codeunit_name} does not contain an artifact which matches the name '{artifact_name_regex}'."
-                if required:
-                    raise ValueError(message)
-                else:
-                    GeneralUtilities.write_message_to_stderr(f"Warning: {message}")
+                codeunits.append(codeunit_name)
+        # TODO set order (the "last" should be first to not overwrite its artifacts)
+        for codeunit in codeunits:
+            self.build_codeunit(os.path.join(repository_folder, codeunit), verbosity, build_environment, additional_arguments_file)
 
     @GeneralUtilities.check_arguments
-    def __build_codeunit(self, codeunit_folder: str, verbosity: int = 1, target_environmenttype: str = "QualityCheck", additional_arguments_file: str = None,
-                         is_pre_merge: bool = False, assume_dependent_codeunits_are_already_built: bool = False) -> None:
+    def build_codeunit(self, codeunit_folder: str, verbosity: int = 1, build_environment: str = "QualityCheck", additional_arguments_file: str = None) -> None:
         now = datetime.now()
         codeunit_folder = GeneralUtilities.resolve_relative_path_from_current_working_directory(codeunit_folder)
         codeunit_name: str = os.path.basename(codeunit_folder)
         codeunit_file = os.path.join(codeunit_folder, f"{codeunit_name}.codeunit.xml")
-        if (not os.path.isfile(codeunit_file)):
+        if(not os.path.isfile(codeunit_file)):
             raise ValueError(f'"{codeunit_folder}" is no codeunit-folder.')
         artifacts_folder = os.path.join(codeunit_folder, "Other", "Artifacts")
         GeneralUtilities.write_message_to_stdout(f"Start building codeunit {codeunit_name}.")
-        GeneralUtilities.write_message_to_stdout(f"Build-environmenttype: {target_environmenttype}")
+        GeneralUtilities.write_message_to_stdout(f"Build-environment: {build_environment}")
         GeneralUtilities.ensure_directory_does_not_exist(artifacts_folder)
 
-        verbosity_for_executed_programs = min(2, verbosity)
-
         other_folder = os.path.join(codeunit_folder, "Other")
         build_folder = os.path.join(other_folder, "Build")
         quality_folder = os.path.join(other_folder, "QualityCheck")
         reference_folder = os.path.join(other_folder, "Reference")
+        sc = ScriptCollectionCore()
         additional_arguments_c: str = ""
         additional_arguments_b: str = ""
         additional_arguments_r: str = ""
         additional_arguments_l: str = ""
         additional_arguments_g: str = ""
-        general_argument = f' --overwrite_verbosity={str(verbosity)} --overwrite_targetenvironmenttype={target_environmenttype}'
-
-        c_additionalargumentsfile_argument = ""
-
-        if is_pre_merge:
-            general_argument = general_argument+" --overwrite_is_pre_merge=true"
-            GeneralUtilities.write_message_to_stdout("This is a pre-merge-build")
-
-        if assume_dependent_codeunits_are_already_built:
-            c_additionalargumentsfile_argument = c_additionalargumentsfile_argument+" --overwrite_assume_dependent_codeunits_are_already_built=true"
-            GeneralUtilities.write_message_to_stdout("Assume dependent codeunits are already built")
-
-        if additional_arguments_file is not None:
+        general_argument = f'--overwrite_verbosity={str(verbosity)} --overwrite_buildenvironment={build_environment}'
+        if additional_arguments_file:
+            c_additional_argument = ""
+        else:
             config = configparser.ConfigParser()
             config.read(additional_arguments_file)
             section_name = f"{codeunit_name}_Configuration"
             if config.has_option(section_name, "ArgumentsForCommonTasks"):
-                additional_arguments_c = " "+config.get(section_name, "ArgumentsForCommonTasks")
+                additional_arguments_c = config.get(section_name, "ArgumentsForCommonTasks")
             if config.has_option(section_name, "ArgumentsForBuild"):
-                additional_arguments_b = " "+config.get(section_name, "ArgumentsForBuild")
+                additional_arguments_b = config.get(section_name, "ArgumentsForBuild")
             if config.has_option(section_name, "ArgumentsForRunTestcases"):
-                additional_arguments_r = " "+config.get(section_name, "ArgumentsForRunTestcases")
+                additional_arguments_r = config.get(section_name, "ArgumentsForRunTestcases")
             if config.has_option(section_name, "ArgumentsForLinting"):
-                additional_arguments_l = " "+config.get(section_name, "ArgumentsForLinting")
+                additional_arguments_l = config.get(section_name, "ArgumentsForLinting")
             if config.has_option(section_name, "ArgumentsForGenerateReference"):
-                additional_arguments_g = " "+config.get(section_name, "ArgumentsForGenerateReference")
-            c_additionalargumentsfile_argument = f' --overwrite_additionalargumentsfile="{additional_arguments_file}"'
+                additional_arguments_g = config.get(section_name, "ArgumentsForGenerateReference")
+            c_additional_argument = f'--overwrite_additionalargumentsfile="{additional_arguments_file}"'
 
         GeneralUtilities.write_message_to_stdout('Run "CommonTasks.py"...')
-        execution_result = self.__sc.run_program("python", f"CommonTasks.py{additional_arguments_c}{general_argument}{c_additionalargumentsfile_argument}",
-                                                 other_folder, verbosity=verbosity_for_executed_programs, throw_exception_if_exitcode_is_not_zero=False)
-        if execution_result[0] != 0:
-            raise ValueError(f"CommonTasks.py resulted in exitcode {execution_result[0]}. StdOut: '{execution_result[1]}' StdOut: '{execution_result[2]}'")
-        self.verify_artifact_exists(codeunit_folder, dict[str, bool]({"Changelog": False, "License": True}))
-
+        sc.run_program("python", f"CommonTasks.py {additional_arguments_c} {general_argument} {c_additional_argument}", other_folder, verbosity=verbosity)
         GeneralUtilities.write_message_to_stdout('Run "Build.py"...')
-        execution_result = self.__sc.run_program("python", f"Build.py{additional_arguments_b}{general_argument}",
-                                                 build_folder, verbosity=verbosity_for_executed_programs, throw_exception_if_exitcode_is_not_zero=False)
-        if execution_result[0] != 0:
-            raise ValueError(f"Build.py resulted in exitcode {execution_result[0]}. StdOut: '{execution_result[1]}' StdOut: '{execution_result[2]}'")
-        self.verify_artifact_exists(codeunit_folder, dict[str, bool]({"BuildResult_.+": True, "BOM": False, "CodeAnalysisResult": False, "SourceCode": True}))
-
-        codeunit_hast_testable_sourcecode = self.codeunit_hast_testable_sourcecode(codeunit_file)
-        if codeunit_hast_testable_sourcecode:
-            GeneralUtilities.write_message_to_stdout('Run "RunTestcases.py"...')
-            execution_result = self.__sc.run_program("python", f"RunTestcases.py{additional_arguments_r}{general_argument}",
-                                                     quality_folder, verbosity=verbosity_for_executed_programs, throw_exception_if_exitcode_is_not_zero=False)
-            if execution_result[0] != 0:
-                raise ValueError(f"RunTestcases.py resulted in exitcode {execution_result[0]}. StdOut: '{execution_result[1]}' StdOut: '{execution_result[2]}'")
-            self.verify_artifact_exists(codeunit_folder, dict[str, bool]({"TestCoverage": True, "TestCoverageReport": False}))
-
+        sc.run_program("python", f"Build.py {additional_arguments_b} {general_argument}",  build_folder, verbosity=verbosity)
+        GeneralUtilities.write_message_to_stdout('Run "RunTestcases.py"...')
+        sc.run_program("python", f"RunTestcases.py {additional_arguments_r} {general_argument}", quality_folder, verbosity=verbosity)
         GeneralUtilities.write_message_to_stdout('Run "Linting.py"...')
-        execution_result = self.__sc.run_program("python", f"Linting.py{additional_arguments_l}{general_argument}",
-                                                 quality_folder, verbosity=verbosity_for_executed_programs, throw_exception_if_exitcode_is_not_zero=False)
-        if execution_result[0] != 0:
-            raise ValueError(f"Linting.py resulted in exitcode {execution_result[0]}. StdOut: '{execution_result[1]}' StdOut: '{execution_result[2]}'")
-        self.verify_artifact_exists(codeunit_folder, dict[str, bool]())
-
+        sc.run_program("python", f"Linting.py {additional_arguments_l} {general_argument}", quality_folder, verbosity=verbosity)
         GeneralUtilities.write_message_to_stdout('Run "GenerateReference.py"...')
-        execution_result = self.__sc.run_program(
-            "python", f"GenerateReference.py{additional_arguments_g}{general_argument}", reference_folder, verbosity=verbosity_for_executed_programs, throw_exception_if_exitcode_is_not_zero=False)
-        if execution_result[0] != 0:
-            raise ValueError(f"GenerateReference.py resulted in exitcode {execution_result[0]}. StdOut: '{execution_result[1]}' StdOut: '{execution_result[2]}'")
-        self.verify_artifact_exists(codeunit_folder, dict[str, bool]({"Reference": True}))
+        sc.run_program("python", f"GenerateReference.py {additional_arguments_g} {general_argument}", reference_folder, verbosity=verbosity)
 
-        artifactsinformation_file = os.path.join(artifacts_folder, f"{codeunit_name}.artifactsinformation.xml")
+        build_codeunit_info_file = os.path.join(artifacts_folder, f"{codeunit_name}.artifactsinformation.xml")
         version = self.get_version_of_codeunit(codeunit_file)
-        GeneralUtilities.ensure_file_exists(artifactsinformation_file)
+        GeneralUtilities.ensure_file_exists(build_codeunit_info_file)
         artifacts_list = []
         for artifact_folder in GeneralUtilities.get_direct_folders_of_folder(artifacts_folder):
             artifact_name = os.path.basename(artifact_folder)
-            artifacts_list.append(f"        <cps:artifact>{artifact_name}<cps:artifact>")
+            artifacts_list.append(f"        <codeunit:artifact>{artifact_name}<codeunit:artifact>")
         artifacts = '\n'.join(artifacts_list)
         moment = GeneralUtilities.datetime_to_string(now)
-        # TODO implement usage of self.reference_latest_version_of_xsd_when_generating_xml
-        GeneralUtilities.write_text_to_file(artifactsinformation_file, f"""<?xml version="1.0" encoding="UTF-8" ?>
-<cps:artifactsinformation xmlns:cps="https://projects.aniondev.de/PublicProjects/Common/ProjectTemplates/-/tree/main/Conventions/RepositoryStructure/CommonProjectStructure" artifactsinformationspecificationversion="1.0.0"
+        GeneralUtilities.write_text_to_file(build_codeunit_info_file, f"""<?xml version="1.0" encoding="UTF-8" ?>
+<codeunit:artifactsinformation xmlns:codeunit="https://github.com/anionDev/ProjectTemplates" artifactsinformationspecificationversion="1.0.0"
     xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="https://raw.githubusercontent.com/anionDev/ProjectTemplates/main/Templates/Conventions/RepositoryStructure/CommonProjectStructure/artifactsinformation.xsd">
-    <cps:name>{codeunit_name}</cps:name>
-    <cps:version>{version}</cps:version>
-    <cps:timestamp>{moment}</cps:timestamp>
-    <cps:targetenvironmenttype>{target_environmenttype}</cps:targetenvironmenttype>
-    <cps:artifacts>
+    <codeunit:name>{codeunit_name}</codeunit:name>
+    <codeunit:version>{version}</codeunit:version>
+    <codeunit:timestamp>{moment}</codeunit:timestamp>
+    <codeunit:targetenvironment>{build_environment}</codeunit:targetenvironment>
+    <codeunit:artifacts>
 {artifacts}
-    </cps:artifacts>
-</cps:artifactsinformation>""")
-        # TODO validate artifactsinformation_file against xsd
-        GeneralUtilities.write_message_to_stdout(f"Finished building codeunit {codeunit_name} without errors.")
+    </codeunit:artifacts>
+</codeunit:artifactsinformation>""")
+        shutil.copyfile(codeunit_file,
+                        os.path.join(artifacts_folder, f"{codeunit_name}.codeunit.xml"))
+        GeneralUtilities.write_message_to_stdout(f"Finished building codeunit {codeunit_name}.")
```

## Comparing `ScriptCollection-3.3.81.dist-info/METADATA` & `ScriptCollection-3.3.9.dist-info/METADATA`

 * *Files 6% similar despite different names*

```diff
@@ -1,60 +1,45 @@
 Metadata-Version: 2.1
 Name: ScriptCollection
-Version: 3.3.81
+Version: 3.3.9
 Summary: The ScriptCollection is the place for reusable scripts.
-Home-page: https://github.com/anionDev/ScriptCollection
-Author: Marius Göcke
-Author-email: marius.goecke@gmail.com
-Project-URL: Documentation, https://github.com/anionDev/ScriptCollection/blob/main/ScriptCollection/Other/Reference/ReferenceContent/index.md
-Project-URL: Changelog, https://github.com/anionDev/ScriptCollection/tree/main/Other/Resources/Changelog
-Keywords: package release build management
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Author-email: Marius Göcke <marius.goecke@gmail.com>
+Project-URL: Homepage, https://github.com/anionDev/ScriptCollection
+Project-URL: Bug Tracker, https://github.com/anionDev/ScriptCollection/issues
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: POSIX :: Linux
 Classifier: Operating System :: Microsoft :: Windows :: Windows 10
 Classifier: Topic :: System :: Logging
 Classifier: Topic :: System :: Monitoring
-Classifier: Topic :: System :: Archiving :: Packaging
-Classifier: Topic :: System :: Systems Administration
 Classifier: Topic :: Terminals
-Classifier: Topic :: Utilities
 Requires-Python: >=3.10
-Description-Content-Type: text/markdown
-Requires-Dist: autopep8 (>=2.0.1)
-Requires-Dist: build (>=0.10.0)
-Requires-Dist: coverage (>=7.0.5)
-Requires-Dist: cyclonedx-bom (>=3.11.0)
+Description-Content-Type: text/x-rst
+Requires-Dist: build (>=0.9.0)
 Requires-Dist: defusedxml (>=0.7.1)
 Requires-Dist: keyboard (>=0.13.5)
-Requires-Dist: lxml (>=4.0.0)
+Requires-Dist: lxml (>=4.9.1)
 Requires-Dist: ntplib (>=0.4.0)
 Requires-Dist: pycdlib (>=1.13.0)
-Requires-Dist: pylint (>=2.15.10)
-Requires-Dist: pyOpenSSL (>=23.0.0)
-Requires-Dist: PyPDF2 (>=3.0.1)
-Requires-Dist: pytest (>=7.2.1)
+Requires-Dist: pylint (>=2.15.5)
+Requires-Dist: PyPDF2 (>=2.11.1)
+Requires-Dist: pytest (>=7.2.0)
 Requires-Dist: qrcode (>=7.3.1)
 Requires-Dist: send2trash (>=1.8.0)
-Requires-Dist: twine (>=4.0.2)
 Requires-Dist: xmlschema (>=2.1.1)
 
 # ScriptCollection
 
-## General
-
 [![Supported Python versions](https://img.shields.io/pypi/pyversions/ScriptCollection.svg)](https://pypi.org/project/ScriptCollection/)
 ![PyPI](https://img.shields.io/pypi/v/ScriptCollection)
 ![Dependencies](https://img.shields.io/librariesio/github/anionDev/ScriptCollection)
 
 [![CodeFactor](https://www.codefactor.io/repository/github/aniondev/scriptcollection/badge/main)](https://www.codefactor.io/repository/github/aniondev/scriptcollection/overview/main)
 [![Downloads](https://pepy.tech/badge/scriptcollection)](https://pepy.tech/project/scriptcollection)
-![Coverage](https://raw.githubusercontent.com/anionDev/ScriptCollection/main/ScriptCollection/Other/Resources/TestCoverageBadges/badge_shieldsio_linecoverage_blue.svg)
+![Coverage](./ScriptCollection/Other/Resources/TestCoverageBadges/badge_shieldsio_linecoverage_blue.svg)
 
 ![License](https://img.shields.io/badge/license-MIT-blue)
 ![GitHub last commit](https://img.shields.io/github/last-commit/anionDev/ScriptCollection)
 ![GitHub issues](https://img.shields.io/github/issues-raw/anionDev/ScriptCollection)
 
 The ScriptCollection is the place for reusable scripts.
```

## Comparing `ScriptCollection-3.3.81.dist-info/entry_points.txt` & `ScriptCollection-3.3.9.dist-info/entry_points.txt`

 * *Files 16% similar despite different names*

```diff
@@ -4,24 +4,21 @@
 SCCalculateBitcoinBlockHash = ScriptCollection.Executables:CalculateBitcoinBlockHash
 SCChangeHashOfProgram = ScriptCollection.Executables:ChangeHashOfProgram
 SCCreateEmptyFileWithSpecificSize = ScriptCollection.Executables:CreateEmptyFileWithSpecificSize
 SCCreateHashOfAllFiles = ScriptCollection.Executables:CreateHashOfAllFiles
 SCCreateISOFileWithObfuscatedFiles = ScriptCollection.Executables:CreateISOFileWithObfuscatedFiles
 SCCreateSimpleMergeWithoutRelease = ScriptCollection.Executables:CreateSimpleMergeWithoutRelease
 SCFilenameObfuscator = ScriptCollection.Executables:FilenameObfuscator
-SCGenerateCertificate = ScriptCollection.Executables:GenerateCertificate
-SCGenerateCertificateAuthority = ScriptCollection.Executables:GenerateCertificateAuthority
-SCGenerateCertificateSignRequest = ScriptCollection.Executables:GenerateCertificateSignRequest
 SCGenerateSnkFiles = ScriptCollection.Executables:GenerateSnkFiles
 SCGenerateThumbnail = ScriptCollection.Executables:GenerateThumbnail
+SCHardening = ScriptCollection.Executables:Hardening
 SCHealthcheck = ScriptCollection.Executables:Healthcheck
 SCKeyboardDiagnosis = ScriptCollection.Executables:KeyboardDiagnosis
 SCMergePDFs = ScriptCollection.Executables:MergePDFs
 SCObfuscateFilesFolder = ScriptCollection.Executables:ObfuscateFilesFolder
 SCOrganizeLinesInFile = ScriptCollection.Executables:OrganizeLinesInFile
 SCReplaceSubstringsInFilenames = ScriptCollection.Executables:ReplaceSubstringsInFilenames
 SCSearchInFiles = ScriptCollection.Executables:SearchInFiles
 SCShow2FAAsQRCode = ScriptCollection.Executables:Show2FAAsQRCode
 SCShowMissingFiles = ScriptCollection.Executables:ShowMissingFiles
-SCSignCertificate = ScriptCollection.Executables:SignCertificate
 SCUpdateNugetpackagesInCsharpProject = ScriptCollection.Executables:UpdateNugetpackagesInCsharpProject
 SCUploadFile = ScriptCollection.Executables:UploadFile
```

## Comparing `ScriptCollection-3.3.81.dist-info/RECORD` & `ScriptCollection-3.3.9.dist-info/RECORD`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,15 @@
-ScriptCollection/Executables.py,sha256=kXTIX92KLeFuxnYOlsyFs5lkznsxkuoBMVrV3OU7FZU,18064
-ScriptCollection/GeneralUtilities.py,sha256=Blo0Iq-G4zuUL5oUxBTeGFtQ23ndK7dpZPOjCwVDMnE,33985
+ScriptCollection/Executables.py,sha256=jUbHFxCj2DLIxnwc2jRZI4DyfN6qIoS_QOhOvSefPXQ,15739
+ScriptCollection/GeneralUtilities.py,sha256=HVQ80reebBZryk9NOhstxvD5gP9di0KO_-AI5G36WLc,31649
+ScriptCollection/Hardening.py,sha256=XRbyd3f2MEp0EDucPrKbXjvC9qqa6fYTAFWX59HYJx8,3421
 ScriptCollection/ProgramRunnerBase.py,sha256=2kyOuoM3oFjBfLc9Q5t5RTz7Ya2CjUxFtB1rBBDmnjU,1937
 ScriptCollection/ProgramRunnerEpew.py,sha256=ZiBZVMcsphmo49z2BwUwQYXo2uTKXPu33QW3IxCT46E,6273
 ScriptCollection/ProgramRunnerPopen.py,sha256=HOs1QVnXiQtwXy1_xvH79bWBdd0i-2tUyyLloQBvMto,3023
-ScriptCollection/ScriptCollectionCore.py,sha256=8nqQ6PalJ7vWOm2YjRqyzhHXBpDEdlq2xqNh9tPhXeY,86232
-ScriptCollection/TasksForCommonProjectStructure.py,sha256=xCGUpcWwlgjG8_jHd9zV4SahR95AmkarMj2moI8BQjo,127118
+ScriptCollection/ScriptCollectionCore.py,sha256=3aH8OdFUwxBO-Z7oPDElDhMXKqJ4rmQTVX2uUAsYkI8,75969
+ScriptCollection/TasksForCommonProjectStructure.py,sha256=MwBwyyyO-eaEIppYHs9JrOtqbMVP_Uh7gv0xj6vcyTY,74893
 ScriptCollection/UpdateCertificates.py,sha256=Go-JJK-YTi7aBB1phlLxypa8GHkmFHBEPB0_TT9G-bw,7918
 ScriptCollection/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-ScriptCollection-3.3.81.dist-info/METADATA,sha256=oWXnWRXJke8HBUEgEK5562T5o_e3YBlv2K7aol3rG2Q,7878
-ScriptCollection-3.3.81.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-ScriptCollection-3.3.81.dist-info/entry_points.txt,sha256=VIuxVCOpX38lSJUwRRENBNgcGKTIBxQyrCfbJVRHP8g,1968
-ScriptCollection-3.3.81.dist-info/top_level.txt,sha256=hY2hOVH0V0Ce51WB76zKkIWTUNwMUdHo4XDkR2vYVwg,17
-ScriptCollection-3.3.81.dist-info/RECORD,,
+ScriptCollection-3.3.9.dist-info/METADATA,sha256=F-wsv1fW6XJ-KMXLHsO1yM_0swTn7lOHEhpz1y3AYnI,7146
+ScriptCollection-3.3.9.dist-info/WHEEL,sha256=2wepM1nk4DS4eFpYrW1TTqPcoGNfHhhO_i5m4cOimbo,92
+ScriptCollection-3.3.9.dist-info/entry_points.txt,sha256=eppw-Ajd-LdXe2-4X6pgBmcqXg3TGchaiPcjRwY4R8w,1697
+ScriptCollection-3.3.9.dist-info/top_level.txt,sha256=hY2hOVH0V0Ce51WB76zKkIWTUNwMUdHo4XDkR2vYVwg,17
+ScriptCollection-3.3.9.dist-info/RECORD,,
```

