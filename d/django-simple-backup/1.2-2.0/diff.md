# Comparing `tmp/django-simple-backup-1.2.tar.gz` & `tmp/django-simple-backup-2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/django-simple-backup-1.2.tar", last modified: Sat May 13 18:25:37 2023, max compression
+gzip compressed data, was "django-simple-backup-2.0.tar", last modified: Sat May 13 19:55:53 2023, max compression
```

## Comparing `django-simple-backup-1.2.tar` & `django-simple-backup-2.0.tar`

### file list

```diff
@@ -1,21 +1,22 @@
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/
--rw-r--r--   0 evgeny     (501) staff       (20)     2093 2023-05-13 18:25:37.000000 django-simple-backup-1.2/PKG-INFO
--rw-r--r--   0 evgeny     (501) staff       (20)       89 2023-05-13 16:03:45.000000 django-simple-backup-1.2/MANIFEST.in
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/docs/
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/docs/Makefile
--rw-r--r--   0 evgeny     (501) staff       (20)      542 2023-05-13 18:24:56.000000 django-simple-backup-1.2/setup.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/
--rw-r--r--   0 evgeny     (501) staff       (20)     2093 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/PKG-INFO
--rw-r--r--   0 evgeny     (501) staff       (20)      399 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/SOURCES.txt
--rw-r--r--   0 evgeny     (501) staff       (20)       14 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/top_level.txt
--rw-r--r--   0 evgeny     (501) staff       (20)        1 2023-05-13 18:25:37.000000 django-simple-backup-1.2/django_simple_backup.egg-info/dependency_links.txt
--rw-r--r--   0 evgeny     (501) staff       (20)       38 2023-05-13 18:25:37.000000 django-simple-backup-1.2/setup.cfg
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/
--rw-r--r--   0 evgeny     (501) staff       (20)       88 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/signals.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/management/
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/management/__init__.py
-drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 18:25:37.000000 django-simple-backup-1.2/simple_backup/management/commands/
--rw-r--r--   0 evgeny     (501) staff       (20)     7761 2023-05-13 16:07:11.000000 django-simple-backup-1.2/simple_backup/management/commands/backup.py
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/management/commands/__init__.py
--rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-1.2/simple_backup/__init__.py
--rw-r--r--   0 evgeny     (501) staff       (20)     1527 2023-05-13 16:03:45.000000 django-simple-backup-1.2/README.rst
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.661681 django-simple-backup-2.0/
+-rw-r--r--   0 evgeny     (501) staff       (20)       54 2023-05-13 16:03:45.000000 django-simple-backup-2.0/AUTHORS
+-rw-r--r--   0 evgeny     (501) staff       (20)       89 2023-05-13 16:03:45.000000 django-simple-backup-2.0/MANIFEST.in
+-rw-r--r--   0 evgeny     (501) staff       (20)     1752 2023-05-13 19:55:53.661410 django-simple-backup-2.0/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)     1527 2023-05-13 16:03:45.000000 django-simple-backup-2.0/README.rst
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.659483 django-simple-backup-2.0/django_simple_backup.egg-info/
+-rw-r--r--   0 evgeny     (501) staff       (20)     1752 2023-05-13 19:55:53.000000 django-simple-backup-2.0/django_simple_backup.egg-info/PKG-INFO
+-rw-r--r--   0 evgeny     (501) staff       (20)      407 2023-05-13 19:55:53.000000 django-simple-backup-2.0/django_simple_backup.egg-info/SOURCES.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)        1 2023-05-13 19:55:53.000000 django-simple-backup-2.0/django_simple_backup.egg-info/dependency_links.txt
+-rw-r--r--   0 evgeny     (501) staff       (20)       14 2023-05-13 19:55:53.000000 django-simple-backup-2.0/django_simple_backup.egg-info/top_level.txt
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.659776 django-simple-backup-2.0/docs/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-2.0/docs/Makefile
+-rw-r--r--   0 evgeny     (501) staff       (20)       38 2023-05-13 19:55:53.661770 django-simple-backup-2.0/setup.cfg
+-rw-r--r--   0 evgeny     (501) staff       (20)      576 2023-05-13 19:55:44.000000 django-simple-backup-2.0/setup.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.660192 django-simple-backup-2.0/simple_backup/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-2.0/simple_backup/__init__.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.660474 django-simple-backup-2.0/simple_backup/management/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-2.0/simple_backup/management/__init__.py
+drwxr-xr-x   0 evgeny     (501) staff       (20)        0 2023-05-13 19:55:53.660928 django-simple-backup-2.0/simple_backup/management/commands/
+-rw-r--r--   0 evgeny     (501) staff       (20)        0 2023-05-13 16:03:45.000000 django-simple-backup-2.0/simple_backup/management/commands/__init__.py
+-rw-r--r--   0 evgeny     (501) staff       (20)     8640 2023-05-13 19:38:49.000000 django-simple-backup-2.0/simple_backup/management/commands/backup.py
+-rw-r--r--   0 evgeny     (501) staff       (20)      221 2023-05-13 18:33:31.000000 django-simple-backup-2.0/simple_backup/signals.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `django-simple-backup-1.2/PKG-INFO` & `django-simple-backup-2.0/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,50 +1,49 @@
-Metadata-Version: 1.2
+Metadata-Version: 2.1
 Name: django-simple-backup
-Version: 1.2
+Version: 2.0
 Summary: A simple backup command for Django
-Home-page: UNKNOWN
+Home-page: 
 Author: Evgeny Fadeev
 Author-email: evgeny.fadeev@gmail.com
-License: UNKNOWN
-Description: This is a fork of the `django-backup app <https://github.com/chriscohoat/django-backup>`_
-        
-        This app backs up database and the media directory on the local disk
-        in a plain directory, without subdirectories.
-        
-        It does not set a goal of syncing files offsite.
-        To sync the files or do other post-processing,
-        please use a signal `backup_ready`
-        or an independent script.
-        
-        To list and download the backup files via the web, 
-        try application `django-directory <https://pypi.python.org/pypi/django-directory/>`_
-        
-        Installation
-        ============
-        Add to the `INSTALLED_APPS` entry `'simple_backup',`.
-        
-        Settings
-        ========
-        `SIMPLE_BACKUP_DIRECTORY` - directory where the backups will be stored. Default value
-        is `'backups'`, relative to the current working directory. This setting can be over-ridden
-        with the option `--output-directory` (or shorter version `-o`)
-        
-        `SIMPLE_BACKUP_DAYS` - number of days to keep the backup files. Default value is `None`.
-        If set, older files will be deleted automatically each time the new backup is made.
-        This walue can be over-ridden with a `--days` option to the command.
-        
-        .. warning:: 
-            To avoid accidental deletion of valuable files when the above setting/option is used,
-            make sure that the backup directory contains only backups.
-        
-        Commands
-        ========
-        `backup` - backs up the site. See output of `python manage.py backup --help` for more information.
-        
-        Signals
-        =======
-        The command `backup` sends a signal `simple_backups.signals.backup_ready` when
-        the backup is prepared and copied to the backups directory.
-        
-Platform: UNKNOWN
-Requires-Python: <3
+Requires-Python: >2, <4
+License-File: AUTHORS
+
+This is a fork of the `django-backup app <https://github.com/chriscohoat/django-backup>`_
+
+This app backs up database and the media directory on the local disk
+in a plain directory, without subdirectories.
+
+It does not set a goal of syncing files offsite.
+To sync the files or do other post-processing,
+please use a signal `backup_ready`
+or an independent script.
+
+To list and download the backup files via the web, 
+try application `django-directory <https://pypi.python.org/pypi/django-directory/>`_
+
+Installation
+============
+Add to the `INSTALLED_APPS` entry `'simple_backup',`.
+
+Settings
+========
+`SIMPLE_BACKUP_DIRECTORY` - directory where the backups will be stored. Default value
+is `'backups'`, relative to the current working directory. This setting can be over-ridden
+with the option `--output-directory` (or shorter version `-o`)
+
+`SIMPLE_BACKUP_DAYS` - number of days to keep the backup files. Default value is `None`.
+If set, older files will be deleted automatically each time the new backup is made.
+This walue can be over-ridden with a `--days` option to the command.
+
+.. warning:: 
+    To avoid accidental deletion of valuable files when the above setting/option is used,
+    make sure that the backup directory contains only backups.
+
+Commands
+========
+`backup` - backs up the site. See output of `python manage.py backup --help` for more information.
+
+Signals
+=======
+The command `backup` sends a signal `simple_backups.signals.backup_ready` when
+the backup is prepared and copied to the backups directory.
```

### Comparing `django-simple-backup-1.2/django_simple_backup.egg-info/PKG-INFO` & `django-simple-backup-2.0/django_simple_backup.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,50 +1,49 @@
-Metadata-Version: 1.2
+Metadata-Version: 2.1
 Name: django-simple-backup
-Version: 1.2
+Version: 2.0
 Summary: A simple backup command for Django
-Home-page: UNKNOWN
+Home-page: 
 Author: Evgeny Fadeev
 Author-email: evgeny.fadeev@gmail.com
-License: UNKNOWN
-Description: This is a fork of the `django-backup app <https://github.com/chriscohoat/django-backup>`_
-        
-        This app backs up database and the media directory on the local disk
-        in a plain directory, without subdirectories.
-        
-        It does not set a goal of syncing files offsite.
-        To sync the files or do other post-processing,
-        please use a signal `backup_ready`
-        or an independent script.
-        
-        To list and download the backup files via the web, 
-        try application `django-directory <https://pypi.python.org/pypi/django-directory/>`_
-        
-        Installation
-        ============
-        Add to the `INSTALLED_APPS` entry `'simple_backup',`.
-        
-        Settings
-        ========
-        `SIMPLE_BACKUP_DIRECTORY` - directory where the backups will be stored. Default value
-        is `'backups'`, relative to the current working directory. This setting can be over-ridden
-        with the option `--output-directory` (or shorter version `-o`)
-        
-        `SIMPLE_BACKUP_DAYS` - number of days to keep the backup files. Default value is `None`.
-        If set, older files will be deleted automatically each time the new backup is made.
-        This walue can be over-ridden with a `--days` option to the command.
-        
-        .. warning:: 
-            To avoid accidental deletion of valuable files when the above setting/option is used,
-            make sure that the backup directory contains only backups.
-        
-        Commands
-        ========
-        `backup` - backs up the site. See output of `python manage.py backup --help` for more information.
-        
-        Signals
-        =======
-        The command `backup` sends a signal `simple_backups.signals.backup_ready` when
-        the backup is prepared and copied to the backups directory.
-        
-Platform: UNKNOWN
-Requires-Python: <3
+Requires-Python: >2, <4
+License-File: AUTHORS
+
+This is a fork of the `django-backup app <https://github.com/chriscohoat/django-backup>`_
+
+This app backs up database and the media directory on the local disk
+in a plain directory, without subdirectories.
+
+It does not set a goal of syncing files offsite.
+To sync the files or do other post-processing,
+please use a signal `backup_ready`
+or an independent script.
+
+To list and download the backup files via the web, 
+try application `django-directory <https://pypi.python.org/pypi/django-directory/>`_
+
+Installation
+============
+Add to the `INSTALLED_APPS` entry `'simple_backup',`.
+
+Settings
+========
+`SIMPLE_BACKUP_DIRECTORY` - directory where the backups will be stored. Default value
+is `'backups'`, relative to the current working directory. This setting can be over-ridden
+with the option `--output-directory` (or shorter version `-o`)
+
+`SIMPLE_BACKUP_DAYS` - number of days to keep the backup files. Default value is `None`.
+If set, older files will be deleted automatically each time the new backup is made.
+This walue can be over-ridden with a `--days` option to the command.
+
+.. warning:: 
+    To avoid accidental deletion of valuable files when the above setting/option is used,
+    make sure that the backup directory contains only backups.
+
+Commands
+========
+`backup` - backs up the site. See output of `python manage.py backup --help` for more information.
+
+Signals
+=======
+The command `backup` sends a signal `simple_backups.signals.backup_ready` when
+the backup is prepared and copied to the backups directory.
```

### Comparing `django-simple-backup-1.2/simple_backup/management/commands/backup.py` & `django-simple-backup-2.0/simple_backup/management/commands/backup.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,202 +1,227 @@
+"""`backup` management command.
+Backs up the database and media files.
+"""
 import os
 import shutil
 import time
 import tempfile
 from datetime import datetime
-from optparse import make_option
 
 from django.core.exceptions import ImproperlyConfigured
-from django.core.management.base import BaseCommand, CommandError
-from django.core.mail import EmailMessage
+from django.core.management.base import BaseCommand, CommandError, CommandParser
 from django.conf import settings
+from django.contrib.sites.models import Site
 from simple_backup.signals import backup_ready
 
 def maybe_print(text, verbosity):
+    """Prints to stdout if verbosity is True"""
     if verbosity:
-        print text
+        print(text)
 
 def delete_old_backup_files(directory, days):
+    """Deletes files in the directory older than `days` days"""
     file_names = os.listdir(directory)
     today = datetime.now()
     for name in file_names:
         file_path = os.path.join(directory, name)
         #won't delete a directory or non- .tar.gz files
         if name.endswith('.tar.gz') and os.path.isfile(file_path):
             stat = os.stat(os.path.join(directory, name))
             delta = today - datetime.fromtimestamp(stat.st_ctime)
             if delta.days > days:
                 os.remove(file_path)
 
 def get_backup_name():
+    """Returns a name for the backup file
+    using the current site name and the current date and time.
+    Defaults to 'django_YYYYMMDD-HHMMSS'
+    """
     if 'sites' in settings.INSTALLED_APPS:
-        from django.contrib.sites.models import Site
         site_name = Site.objects.get_current().name
     else:
         site_name = 'django'
     return site_name + '_' + time.strftime('%Y%m%d-%H%M%S')
 
 def get_safe_dirname(sourcedir):
+    """Returns a safe name for the directory to be backed up.
+    Works for Unix and hopefully Windows.
+    """
     if not os.path.isabs(sourcedir):
         sourcedir = os.path.abspath(sourcedir)
     drive, dirname = os.path.splitdrive(sourcedir)
     dirname = dirname.replace(os.path.sep, '_')
     if drive:
         dirname = drive.strip(':') + '_' + dirname
     return dirname
 
 def get_database_parameters():
-    if hasattr(settings, 'DATABASES'):
-        params = list()
-        for name in settings.DATABASES.keys():
-            params_for_name = {
-                'engine': settings.DATABASES[name]['ENGINE'],
-                'name': settings.DATABASES[name]['NAME'],
-                'user': settings.DATABASES[name]['USER'],
-                'password': settings.DATABASES[name]['PASSWORD'],
-                'host': settings.DATABASES[name]['HOST'],
-                'port': settings.DATABASES[name]['PORT']
-            }
-            params.append((name, params_for_name))
-        return params
-    else:
-        return ('default', {
-            'engine': settings.DATABASE_ENGINE,
-            'name': settings.DATABASE_NAME,
-            'user': settings.DATABASE_USER,
-            'password': settings.DATABASE_PASSWORD,
-            'host': settings.DATABASE_HOST,
-            'port': settings.DATABASE_PORT
-        })
+    """Returns a list of tuples (name, params) with the parameters
+    for each database in the settings."""
+    params = []
+    for name in settings.DATABASES.keys():
+        params_for_name = {
+            'engine': settings.DATABASES[name]['ENGINE'],
+            'name': settings.DATABASES[name]['NAME'],
+            'user': settings.DATABASES[name]['USER'],
+            'password': settings.DATABASES[name]['PASSWORD'],
+            'host': settings.DATABASES[name]['HOST'],
+            'port': settings.DATABASES[name]['PORT']
+        }
+        params.append((name, params_for_name))
+    return params
 
 def backup_sqlite(params, outfile):
-    os.system('cp %s %s' % (params['name'], outfile))
+    """Backs up a sqlite database by copying the file"""
+    os.system(f'cp {params["name"]} {outfile}')
 
 def backup_mysql(params, outfile):
+    """Backs up a mysql database using mysqldump"""
     args = ''
     user = params['user']
     password = params['password']
     host = params['host']
     port = params['port']
     if user:
-        args += "--user=%s " % user
+        args += f"--user={user} "
     if password:
-        args += "--password=%s " % password
+        args += f"--password={password} "
     if host:
-        args += "--host=%s " % host
+        args += f"--host={host} "
     if port:
-        args += "--port=%s " % port
+        args += f"--port={port} "
     args += params['name']
-    os.system('mysqldump %s > %s' % (args, outfile))
+    os.system(f'mysqldump {args} > {outfile}')
 
 def backup_postgresql(params, outfile):
+    """Backs up a postgresql database using pg_dump"""
     args = ''
     user = params['user']
     password = params['password']
     host = params['host']
     port = params['port']
     if user:
-        args += "--username=%s " % user
+        args += f"--username={user} "
     if host:
-        args += "--host=%s " % host
+        args += f"--host={user} "
     if port:
-        args += "--port=%s " % port
+        args += f"--port={port} "
     args += params['name']
 
     if password:
-        command = 'PGPASSWORD=%s pg_dump %s > %s' % (password, args, outfile)
+        command = f'PGPASSWORD={password} pg_dump {args} > {outfile}'
     else:
-        command = 'pg_dump %s -w > %s' % (args, outfile)
+        command = f'pg_dump {args} -w > {outfile}'
     os.system(command)
 
 def backup_database(params, outfile, verbosity):
+    """Backs up a database of any supported engine"""
     engine = params['engine']
     name = params['name']
     if 'mysql' in engine:
-        maybe_print('Backing up Mysql database %s' % name, verbosity)
+        maybe_print(f'Backing up Mysql database {name}', verbosity)
         backup_mysql(params, outfile)
     elif engine in ('postgresql_psycopg2', 'postgresql') or 'postgresql' in engine:
-        maybe_print('Backing up Postgresql database %s' % name, verbosity)
+        maybe_print(f'Backing up Postgresql database {name}', verbosity)
         backup_postgresql(params, outfile)
     elif 'sqlite3' in engine:
-        maybe_print('Backing up Postgresql database %s' % name, verbosity)
+        maybe_print(f'Backing up Postgresql database {name}', verbosity)
         backup_sqlite(params, outfile)
     else:
-        raise CommandError('Backup for the database %s engine not implemented' % engine)
+        raise CommandError(f'Backup for the database {engine} engine not implemented')
+
+def backup_databases(collect_dir, verbosity):
+    """Backs up all the databases in the settings"""
+    database_params = get_database_parameters()
+    for name, params in database_params:
+        outfile = os.path.join(collect_dir, name + '.sql')
+        backup_database(params, outfile, verbosity)
+
+def backup_media(collect_dir, verbosity):
+    """Backs up the uploaded media files"""
+    maybe_print(f"Backing up uploaded files from {settings.MEDIA_ROOT}", verbosity)
+    #copy the uploaded media to the temp directory
+    dest_dir = os.path.join(collect_dir, os.path.basename(settings.MEDIA_ROOT))
+    shutil.copytree(settings.MEDIA_ROOT, dest_dir)
+
+def backup_directories(collect_dir, directories, verbosity):
+    """Backs up extra directories specified in `settings.SIMPLE_BACKUP_DIRECTORIES`"""
+    comments = []
+    for directory in directories:
+        maybe_print(f"Backing up directory {directory}", verbosity)
+        destdir = get_safe_dirname(directory)
+        shutil.copytree(directory, os.path.join(collect_dir, destdir))
+        comments.append(f'Directory {directory} copied to {destdir}')
+    #write comments if there are any
+    if comments:
+        comments_file_path = os.path.join(collect_dir, 'README.txt')
+        with open(comments_file_path, 'w', encoding='utf-8') as readme_file:
+            readme_file.write('\n'.join(comments))
+
+def clean_days_option(days):
+    """Returns the number of days to keep backups"""
+    try:
+        return int(days)
+    except ValueError as exc:
+        if days:
+            raise CommandError('value of --days must be an integer') from exc
+        error_msg = 'value of SIMPLE_BACKUP_DAYS must be an Integer'
+        raise ImproperlyConfigured(error_msg) from exc
 
 # Based on: http://code.google.com/p/django-backup/
 # Based on: http://www.djangosnippets.org/snippets/823/
 # Based on: http://www.yashh.com/blog/2008/sep/05/django-database-backup-view/
 class Command(BaseCommand):
-    option_list = BaseCommand.option_list + (
-        make_option('--directory', '-d', action='append', default=[], dest='directories',
-            help='Extra directories to back up'),
-        make_option('--without-media', '-u', action='store_true', default=False,
-            dest='without_media', help='Do not backup the media directory'),
-        make_option('--without-db', '-b', action='store_true', default=False,
-            dest='without_db', help='Do not back up database'),
-    )
+    """`backup` management command"""
     help = "Backup database. Mysql, Postgresql and Sqlite engines are supported"
 
+    def add_arguments(self, parser: CommandParser) -> None:
+        """Adds arguments to the command
+        * --directory
+        * --without-media
+        * --without-db
+        """
+        parser.add_argument('--directory', '-d', action='append', default=[], dest='directories',
+            help='Extra directories to back up')
+        parser.add_argument('--without-media', '-u', action='store_true', default=False,
+            dest='without_media', help='Do not backup the media directory')
+        parser.add_argument('--without-db', '-b', action='store_true', default=False,
+            dest='without_db', help='Do not back up database')
+
     def handle(self, *args, **options):
         temp_dir = tempfile.mkdtemp()
         backup_name = get_backup_name()
         #collect all files into this directory
         collect_dir = os.path.join(temp_dir, backup_name)
         os.makedirs(collect_dir)
 
         #Backup documents?
         if not options['without_media']:
-            maybe_print("Backing up uploaded files from %s" % settings.MEDIA_ROOT, options['verbosity'])
-            #copy the uploaded media to the temp directory
-            dest_dir = os.path.join(collect_dir, os.path.basename(settings.MEDIA_ROOT))
-            shutil.copytree(settings.MEDIA_ROOT, dest_dir)
+            backup_media(collect_dir, options['verbosity'])
 
         # Doing backup
         if not options['without_db']:
-            database_params = get_database_parameters()
-            #todo: allow to select databases to back up
-            for name, params in database_params:
-                outfile = os.path.join(collect_dir, name + '.sql')
-                backup_database(params, outfile, options['verbosity'])
+            backup_databases(collect_dir, options['verbosity'])
 
         #backing up extra directoris
-        comments = list()
-        for directory in options['directories']:
-            maybe_print("Backing up directory %s" % directory, options['verbosity'])
-            destdir = get_safe_dirname(directory)
-            shutil.copytree(directory, os.path.join(collect_dir, destdir))
-            comments.append('Directory %s copied to %s' % (directory, destdir))
-
-        #write comments if there are any
-        if comments:
-            readme_file = open(os.path.join(collect_dir, 'README.txt'), 'w')
-            readme_file.write('\n'.join(comments))
-            readme_file.close()
+        backup_directories(collect_dir, options['directories'], options['verbosity'])
 
         #compress backup
         maybe_print('Compressing backup file', options['verbosity'])
         outfile = os.path.join(temp_dir, backup_name + '.tar.gz')
-        os.system('cd %s && tar -czf %s %s' % (temp_dir, outfile, backup_name))
+        os.system(f'cd {temp_dir} && tar -czf {outfile} {backup_name}')
 
         #move file to the final location
         backups_dir = getattr(settings, 'SIMPLE_BACKUP_DIRECTORY', 'backups')
         if not os.path.exists(backups_dir):
             os.makedirs(backups_dir)
 
         shutil.move(outfile, backups_dir)
         shutil.rmtree(temp_dir)
 
         days = options.get('days', getattr(settings, 'SIMPLE_BACKUP_DAYS', None))
         if days:
-            try:
-                days = int(days)
-            except ValueError:
-                if options['days']:
-                    raise CommandError('value of --days must be an integer')
-                else:
-                    raise ImproperlyConfigured('value of SIMPLE_BACKUP_DAYS must be an Integer')
-            else:
-                delete_old_backup_files(backups_dir, days)
+            days = clean_days_option(days)
+            delete_old_backup_files(backups_dir, days)
 
         backup_file = os.path.join(backups_dir, os.path.basename(outfile))
         backup_ready.send(None, path=backup_file)
```

### Comparing `django-simple-backup-1.2/README.rst` & `django-simple-backup-2.0/README.rst`

 * *Files identical despite different names*

