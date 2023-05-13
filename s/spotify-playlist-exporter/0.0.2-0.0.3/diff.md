# Comparing `tmp/spotify-playlist-exporter-0.0.2.tar.gz` & `tmp/spotify-playlist-exporter-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "C:\Users\bebis\Dropbox\Code\spotify_grab_current_playlists\dist\.tmp-8yk96n4f\spotify-playlist-exporter-0.0.2.tar", last modified: Sun May  7 08:56:47 2023, max compression
+gzip compressed data, was "C:\Users\bebis\Dropbox\Code\spotify_grab_current_playlists\dist\.tmp-084a80xo\spotify-playlist-exporter-0.0.3.tar", last modified: Sat May 13 05:51:10 2023, max compression
```

## Comparing `spotify-playlist-exporter-0.0.2.tar` & `spotify-playlist-exporter-0.0.3.tar`

### file list

```diff
@@ -1,15 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/
--rw-rw-rw-   0        0        0     1091 2023-04-25 09:38:20.000000 spotify-playlist-exporter-0.0.2/LICENSE.txt
--rw-rw-rw-   0        0        0     3999 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/PKG-INFO
--rw-rw-rw-   0        0        0     3514 2023-05-07 08:45:23.000000 spotify-playlist-exporter-0.0.2/README.md
--rw-rw-rw-   0        0        0      721 2023-05-07 08:55:56.000000 spotify-playlist-exporter-0.0.2/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/
-drwxrwxrwx   0        0        0        0 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_grab_current_playlists/
--rw-rw-rw-   0        0        0      232 2023-05-01 09:07:24.000000 spotify-playlist-exporter-0.0.2/src/spotify_grab_current_playlists/cred.py
--rw-rw-rw-   0        0        0     8779 2023-05-05 22:25:31.000000 spotify-playlist-exporter-0.0.2/src/spotify_grab_current_playlists/spotify_grab_current_playlists.py
-drwxrwxrwx   0        0        0        0 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/
--rw-rw-rw-   0        0        0     3999 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      360 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       31 2023-05-07 08:56:47.000000 spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/
+-rw-rw-rw-   0        0        0     1091 2023-04-25 09:38:20.000000 spotify-playlist-exporter-0.0.3/LICENSE.txt
+-rw-rw-rw-   0        0        0     3999 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0     3514 2023-05-13 05:18:33.000000 spotify-playlist-exporter-0.0.3/README.md
+-rw-rw-rw-   0        0        0      989 2023-05-13 05:49:10.000000 spotify-playlist-exporter-0.0.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_grab_current_playlists/
+-rw-rw-rw-   0        0        0      221 2023-05-13 05:22:55.000000 spotify-playlist-exporter-0.0.3/src/spotify_grab_current_playlists/cred.py
+-rw-rw-rw-   0        0        0      232 2023-05-01 09:07:24.000000 spotify-playlist-exporter-0.0.3/src/spotify_grab_current_playlists/cred_my.py
+-rw-rw-rw-   0        0        0     8859 2023-05-13 05:37:53.000000 spotify-playlist-exporter-0.0.3/src/spotify_grab_current_playlists/spotify_grab_current_playlists.py
+drwxrwxrwx   0        0        0        0 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/
+-rw-rw-rw-   0        0        0     3999 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      458 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      310 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       31 2023-05-13 05:51:10.000000 spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/top_level.txt
```

### Comparing `spotify-playlist-exporter-0.0.2/LICENSE.txt` & `spotify-playlist-exporter-0.0.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `spotify-playlist-exporter-0.0.2/PKG-INFO` & `spotify-playlist-exporter-0.0.3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotify-playlist-exporter
-Version: 0.0.2
+Version: 0.0.3
 Summary: A small example package
 Author-email: Example Author <bebissig@gmail.com>
 Project-URL: Homepage, https://github.com/bebissig/spotify_grab_current_playlists
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
@@ -21,26 +21,26 @@
 
 - Spotipy
 - pandas
 
 You can install them with the following command:
 
 ```bash
-pip install spotipy pandas
+pip install spotipy pandas openpyxl
 ```
 
 ## Setting up Spotify API credentials
 
 To access the Spotify API, you need to have API credentials in the form of a `client_id`, `client_secret`, and a `redirect_uri`. Here's how you can get your credentials:
 
 1. Go to the Spotify Developer Dashboard: https://developer.spotify.com/dashboard/
 2. Log in with your Spotify account or create a new one if you don't have one yet.
 3. Click on "Create an App" and fill in the required information.
 4. After creating the app, you will see your `client_id` and `client_secret` in the app's Dashboard.
-5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:8080/callback".
+5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:9000".
 
 Now that you have your credentials, you can store them in a `cred.py` file in the same directory as the main script. The `cred.py` file should look like this:
 
 ```python
 client_id = "your_client_id"
 client_secret = "your_client_secret"
 redirect_uri = "your_redirect_uri"
```

### Comparing `spotify-playlist-exporter-0.0.2/README.md` & `spotify-playlist-exporter-0.0.3/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -8,26 +8,26 @@
 
 - Spotipy
 - pandas
 
 You can install them with the following command:
 
 ```bash
-pip install spotipy pandas
+pip install spotipy pandas openpyxl
 ```
 
 ## Setting up Spotify API credentials
 
 To access the Spotify API, you need to have API credentials in the form of a `client_id`, `client_secret`, and a `redirect_uri`. Here's how you can get your credentials:
 
 1. Go to the Spotify Developer Dashboard: https://developer.spotify.com/dashboard/
 2. Log in with your Spotify account or create a new one if you don't have one yet.
 3. Click on "Create an App" and fill in the required information.
 4. After creating the app, you will see your `client_id` and `client_secret` in the app's Dashboard.
-5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:8080/callback".
+5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:9000".
 
 Now that you have your credentials, you can store them in a `cred.py` file in the same directory as the main script. The `cred.py` file should look like this:
 
 ```python
 client_id = "your_client_id"
 client_secret = "your_client_secret"
 redirect_uri = "your_redirect_uri"
```

### Comparing `spotify-playlist-exporter-0.0.2/src/spotify_grab_current_playlists/spotify_grab_current_playlists.py` & `spotify-playlist-exporter-0.0.3/src/spotify_grab_current_playlists/spotify_grab_current_playlists.py`

 * *Files 9% similar despite different names*

```diff
@@ -14,18 +14,29 @@
 
 import spotipy
 from spotipy.oauth2 import SpotifyOAuth
 import pandas as pd
 import datetime
 import time
 import argparse
+import sys
 
-from cred import client_id, client_secret, redirect_uri, username
-
+#from cred import client_id, client_secret, redirect_uri, username
 
+def import_credentials():
+    try:
+        from cred_my import client_id, client_secret, redirect_uri, username
+    except ImportError:
+        try: 
+            from cred import client_id, client_secret, redirect_uri, username
+        except ImportError:
+            print('No credentials file found.')
+            sys.exit(1)
+    return client_id, client_secret, redirect_uri, username
+    
 def get_playlist_tracks(sp,username,playlist_id):
     '''
     sp... spotipy API client instance
     username... spotify username
     playlist_id... playlist id (not name)
     '''
     playlist = sp.user_playlist(user=username,playlist_id=playlist_id) # dict with keys 'tracks'
@@ -44,24 +55,15 @@
     return tracks_list_items
 
 def get_playlist(sp,username,list_name):
     playlists=sp.user_playlists(username)
     for playlist in playlists['items']:
         if playlist['name']=='Mit Star bewertet':
             the_list=playlist
-    return the_list
-
-def test_playlist_tracks():
-    scope = "playlist-read-private"
-    sp = spotipy.Spotify(auth_manager=SpotifyOAuth(client_id=client_id, client_secret=client_secret, redirect_uri=redirect_uri, scope=scope))
-
-    the_list=get_playlist(sp,username=username,list_name='Mit Star bewertet')
-    tracks_list_items=get_playlist_tracks(sp=sp,username=username,playlist_id=the_list['id'])
-
-    return tracks_list_items[-1]    
+    return the_list 
 
 
 def create_api_session(scope,client_id,client_secret, redirect_uri):
     sp = spotipy.Spotify(auth_manager=SpotifyOAuth(client_id=client_id, client_secret=client_secret, redirect_uri=redirect_uri, scope=scope))
     return sp
 
 def export_spotify_playlists(username,sp):
@@ -107,15 +109,15 @@
     
     # Convert the list of rows into a pandas DataFrame
     df = pd.DataFrame(rows)
     
     if to_clipboard == True:
         df.to_clipboard()
     if savefile != None:
-        df.to_excel(savefile, index=False)
+        df.to_excel('./out/'+savefile, index=False)
 
     return df
 
 def recently_played_to_dataframe(all_tracks,to_clipboard = False, savefile="recently_played.xlsx"):
     # Initialize an empty list to store the rows of the DataFrame
     rows = []
     # Iterate over each playlist in the all_playlists dictionary
@@ -127,15 +129,15 @@
     
     # Convert the list of rows into a pandas DataFrame
     df = pd.DataFrame(rows)
     
     if to_clipboard == True:
         df.to_clipboard()
     if savefile != None:
-        df.to_excel(savefile, index=False)
+        df.to_excel('./out/'+savefile, index=False)
 
     return df
 
 def recently_played(sp,timestamp):   
     '''
     Problem: Only tracks that have been played to the end are on this list.
     '''
@@ -169,14 +171,16 @@
     return now.strftime("%y%m%d_%H%M%S")
 
 
 def main(playlists_file='playlists',recently_file='recently_played', date_string='2023-01-1'):
     date_timestamp = datestring_to_timestamp(date_string)
     now_string = now_as_string()
 
+    client_id, client_secret, redirect_uri, username = import_credentials()
+
     # Get and save playlists
     scope = "playlist-read-private"
     sp = create_api_session(scope=scope,client_id=client_id,client_secret=client_secret,redirect_uri=redirect_uri)
     all_playlists = export_spotify_playlists(username,sp)
     df_playlists = playlists_to_dataframe(all_playlists,to_clipboard = False, savefile="{}_{}.xlsx".format(now_string,playlists_file))
 
     # Get and save recently played (since date_string in yyyy-mm-dd)
@@ -185,16 +189,16 @@
     recently_list=recently_played(sp,date_timestamp)
     df_recently = recently_played_to_dataframe(recently_list,to_clipboard = False, savefile="{}_{}.xlsx".format(now_string,recently_file))
 
     return df_playlists, df_recently
 
 if __name__ == '__main__':
     parser = argparse.ArgumentParser(description='Description of your program')
-    parser.add_argument('--playlistsfile', type=str, default='playlists_xx', help='Description of arg1')
-    parser.add_argument('--recentlyfile', type=str, default ='recently_played_xy',help='Description of arg2')
+    parser.add_argument('--playlistsfile', type=str, default='playlists', help='Description of arg1')
+    parser.add_argument('--recentlyfile', type=str, default ='recently_played',help='Description of arg2')
     parser.add_argument('--datestring', type=str, default='2023-01-01',help='Description of arg2')
     args = parser.parse_args()
     print(args)
 
 
     playlist_file=args.playlistsfile
     recently_file=args.recentlyfile
```

### Comparing `spotify-playlist-exporter-0.0.2/src/spotify_playlist_exporter.egg-info/PKG-INFO` & `spotify-playlist-exporter-0.0.3/src/spotify_playlist_exporter.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotify-playlist-exporter
-Version: 0.0.2
+Version: 0.0.3
 Summary: A small example package
 Author-email: Example Author <bebissig@gmail.com>
 Project-URL: Homepage, https://github.com/bebissig/spotify_grab_current_playlists
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
@@ -21,26 +21,26 @@
 
 - Spotipy
 - pandas
 
 You can install them with the following command:
 
 ```bash
-pip install spotipy pandas
+pip install spotipy pandas openpyxl
 ```
 
 ## Setting up Spotify API credentials
 
 To access the Spotify API, you need to have API credentials in the form of a `client_id`, `client_secret`, and a `redirect_uri`. Here's how you can get your credentials:
 
 1. Go to the Spotify Developer Dashboard: https://developer.spotify.com/dashboard/
 2. Log in with your Spotify account or create a new one if you don't have one yet.
 3. Click on "Create an App" and fill in the required information.
 4. After creating the app, you will see your `client_id` and `client_secret` in the app's Dashboard.
-5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:8080/callback".
+5. Set the `redirect_uri` for your app by clicking "Edit Settings" and adding a redirect URI, such as "http://localhost:9000".
 
 Now that you have your credentials, you can store them in a `cred.py` file in the same directory as the main script. The `cred.py` file should look like this:
 
 ```python
 client_id = "your_client_id"
 client_secret = "your_client_secret"
 redirect_uri = "your_redirect_uri"
```

