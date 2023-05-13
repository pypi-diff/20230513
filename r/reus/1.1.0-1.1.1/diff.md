# Comparing `tmp/reus-1.1.0.tar.gz` & `tmp/reus-1.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reus-1.1.0.tar", last modified: Sun Oct  9 14:17:29 2022, max compression
+gzip compressed data, was "reus-1.1.1.tar", last modified: Sat May 13 14:51:18 2023, max compression
```

## Comparing `reus-1.1.0.tar` & `reus-1.1.1.tar`

### file list

```diff
@@ -1,61 +1,74 @@
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.854931 reus-1.1.0/
--rw-rw-rw-   0        0        0     1090 2022-05-11 22:07:30.000000 reus-1.1.0/LICENSE
--rw-rw-rw-   0        0        0      616 2022-10-09 14:17:29.853931 reus-1.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1812 2022-10-09 14:06:17.000000 reus-1.1.0/README.md
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.795930 reus-1.1.0/reus/
--rw-rw-rw-   0        0        0      100 2022-09-09 22:23:01.000000 reus-1.1.0/reus/__init__.py
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.838930 reus-1.1.0/reus/fbref/
--rw-rw-rw-   0        0        0     1866 2022-09-09 22:14:32.000000 reus-1.1.0/reus/fbref/__init__.py
--rw-rw-rw-   0        0        0     2602 2022-09-09 21:50:09.000000 reus-1.1.0/reus/fbref/fb_league_table.py
--rw-rw-rw-   0        0        0     3492 2022-09-09 22:07:16.000000 reus-1.1.0/reus/fbref/fb_match_data.py
--rw-rw-rw-   0        0        0     4747 2022-09-09 22:06:42.000000 reus-1.1.0/reus/fbref/fb_match_defensive_actions_stats.py
--rw-rw-rw-   0        0        0     5430 2022-09-09 22:06:57.000000 reus-1.1.0/reus/fbref/fb_match_keeper_stats.py
--rw-rw-rw-   0        0        0     2199 2022-09-09 21:50:36.000000 reus-1.1.0/reus/fbref/fb_match_lineups.py
--rw-rw-rw-   0        0        0     5659 2022-09-09 22:03:15.000000 reus-1.1.0/reus/fbref/fb_match_metadata.py
--rw-rw-rw-   0        0        0     3731 2022-09-09 22:06:31.000000 reus-1.1.0/reus/fbref/fb_match_misc_stats.py
--rw-rw-rw-   0        0        0     4450 2022-09-09 22:06:23.000000 reus-1.1.0/reus/fbref/fb_match_passing_stats.py
--rw-rw-rw-   0        0        0     4862 2022-09-09 22:06:15.000000 reus-1.1.0/reus/fbref/fb_match_passing_type_stats.py
--rw-rw-rw-   0        0        0     5410 2022-09-09 22:06:05.000000 reus-1.1.0/reus/fbref/fb_match_possession_stats.py
--rw-rw-rw-   0        0        0     3007 2022-09-09 21:56:15.000000 reus-1.1.0/reus/fbref/fb_match_shots.py
--rw-rw-rw-   0        0        0     3228 2022-09-09 21:56:05.000000 reus-1.1.0/reus/fbref/fb_match_summary.py
--rw-rw-rw-   0        0        0     5989 2022-09-09 22:05:38.000000 reus-1.1.0/reus/fbref/fb_match_summary_stats.py
--rw-rw-rw-   0        0        0     7467 2022-09-09 21:55:58.000000 reus-1.1.0/reus/fbref/fb_match_team_stats.py
--rw-rw-rw-   0        0        0      869 2022-09-09 21:55:47.000000 reus-1.1.0/reus/fbref/fb_match_urls.py
--rw-rw-rw-   0        0        0     3193 2022-09-09 21:55:39.000000 reus-1.1.0/reus/fbref/fb_season_fixture_urls.py
--rw-rw-rw-   0        0        0     3178 2022-09-09 21:55:29.000000 reus-1.1.0/reus/fbref/fb_season_urls.py
--rw-rw-rw-   0        0        0     5502 2022-09-09 21:54:38.000000 reus-1.1.0/reus/fbref/fb_team_player_advanced_keeper_stats.py
--rw-rw-rw-   0        0        0     2915 2022-09-09 21:54:33.000000 reus-1.1.0/reus/fbref/fb_team_player_data.py
--rw-rw-rw-   0        0        0     4593 2022-09-09 21:54:26.000000 reus-1.1.0/reus/fbref/fb_team_player_defensive_actions_stats.py
--rw-rw-rw-   0        0        0     3966 2022-09-09 21:54:23.000000 reus-1.1.0/reus/fbref/fb_team_player_goal_sca_stats.py
--rw-rw-rw-   0        0        0     3908 2022-09-09 21:54:18.000000 reus-1.1.0/reus/fbref/fb_team_player_keeper_stats.py
--rw-rw-rw-   0        0        0     3653 2022-09-09 21:54:13.000000 reus-1.1.0/reus/fbref/fb_team_player_misc_stats.py
--rw-rw-rw-   0        0        0     4445 2022-09-09 21:54:08.000000 reus-1.1.0/reus/fbref/fb_team_player_passing_stats.py
--rw-rw-rw-   0        0        0     4663 2022-09-09 21:54:03.000000 reus-1.1.0/reus/fbref/fb_team_player_passing_type_stats.py
--rw-rw-rw-   0        0        0     4525 2022-09-09 21:53:59.000000 reus-1.1.0/reus/fbref/fb_team_player_playing_time_stats.py
--rw-rw-rw-   0        0        0     5264 2022-09-09 21:53:55.000000 reus-1.1.0/reus/fbref/fb_team_player_possession_stats.py
--rw-rw-rw-   0        0        0     4063 2022-09-09 21:53:46.000000 reus-1.1.0/reus/fbref/fb_team_player_shooting_stats.py
--rw-rw-rw-   0        0        0     4312 2022-09-09 21:53:37.000000 reus-1.1.0/reus/fbref/fb_team_player_summary_stats.py
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.845934 reus-1.1.0/reus/fotmob/
--rw-rw-rw-   0        0        0      143 2022-09-09 22:16:07.000000 reus-1.1.0/reus/fotmob/__init__.py
--rw-rw-rw-   0        0        0     1450 2022-10-09 13:50:26.000000 reus-1.1.0/reus/fotmob/fm_leagues.py
--rw-rw-rw-   0        0        0    15435 2022-10-09 14:01:33.000000 reus-1.1.0/reus/fotmob/fm_match_data.py
--rw-rw-rw-   0        0        0     1333 2022-10-09 13:56:10.000000 reus-1.1.0/reus/fotmob/fm_match_ids.py
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.853931 reus-1.1.0/reus/transfermarkt/
--rw-rw-rw-   0        0        0      387 2022-09-09 22:14:39.000000 reus-1.1.0/reus/transfermarkt/__init__.py
--rw-rw-rw-   0        0        0     1410 2022-09-09 21:56:44.000000 reus-1.1.0/reus/transfermarkt/tm_player_data.py
--rw-rw-rw-   0        0        0     1340 2022-09-09 21:59:29.000000 reus-1.1.0/reus/transfermarkt/tm_player_injury.py
--rw-rw-rw-   0        0        0     1479 2022-09-09 21:57:23.000000 reus-1.1.0/reus/transfermarkt/tm_player_market_value.py
--rw-rw-rw-   0        0        0     7096 2022-09-09 21:57:34.000000 reus-1.1.0/reus/transfermarkt/tm_player_metadata.py
--rw-rw-rw-   0        0        0     3094 2022-09-09 21:57:39.000000 reus-1.1.0/reus/transfermarkt/tm_player_transfers.py
--rw-rw-rw-   0        0        0     6075 2022-09-09 21:57:54.000000 reus-1.1.0/reus/transfermarkt/tm_team_player_urls.py
--rw-rw-rw-   0        0        0     9259 2022-09-09 21:58:26.000000 reus-1.1.0/reus/transfermarkt/tm_team_transfers.py
--rw-rw-rw-   0        0        0     2085 2022-09-09 21:58:51.000000 reus-1.1.0/reus/transfermarkt/util.py
--rw-rw-rw-   0        0        0      848 2022-09-09 21:59:55.000000 reus-1.1.0/reus/util.py
-drwxrwxrwx   0        0        0        0 2022-10-09 14:17:29.810932 reus-1.1.0/reus.egg-info/
--rw-rw-rw-   0        0        0      616 2022-10-09 14:17:29.000000 reus-1.1.0/reus.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1787 2022-10-09 14:17:29.000000 reus-1.1.0/reus.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-10-09 14:17:29.000000 reus-1.1.0/reus.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       45 2022-10-09 14:17:29.000000 reus-1.1.0/reus.egg-info/requires.txt
--rw-rw-rw-   0        0        0        5 2022-10-09 14:17:29.000000 reus-1.1.0/reus.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-10-09 14:17:29.854931 reus-1.1.0/setup.cfg
--rw-rw-rw-   0        0        0      883 2022-09-09 22:23:52.000000 reus-1.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.872095 reus-1.1.1/
+-rw-rw-rw-   0        0        0     1090 2022-05-11 22:07:30.000000 reus-1.1.1/LICENSE
+-rw-rw-rw-   0        0        0      616 2023-05-13 14:51:18.872095 reus-1.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     1978 2023-05-13 14:44:11.000000 reus-1.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.804095 reus-1.1.1/reus/
+-rw-rw-rw-   0        0        0      100 2022-10-09 22:38:33.000000 reus-1.1.1/reus/__init__.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.855096 reus-1.1.1/reus/fbref/
+-rw-rw-rw-   0        0        0     1866 2022-10-09 22:38:44.000000 reus-1.1.1/reus/fbref/__init__.py
+-rw-rw-rw-   0        0        0     3075 2023-05-10 20:47:21.000000 reus-1.1.1/reus/fbref/fb_league_table.py
+-rw-rw-rw-   0        0        0     4728 2023-05-12 15:42:41.000000 reus-1.1.1/reus/fbref/fb_match_data.py
+-rw-rw-rw-   0        0        0     5262 2023-05-11 14:36:50.000000 reus-1.1.1/reus/fbref/fb_match_defensive_actions_stats.py
+-rw-rw-rw-   0        0        0     6747 2023-05-11 14:36:55.000000 reus-1.1.1/reus/fbref/fb_match_keeper_stats.py
+-rw-rw-rw-   0        0        0     2215 2023-05-11 14:38:13.000000 reus-1.1.1/reus/fbref/fb_match_lineups.py
+-rw-rw-rw-   0        0        0     8210 2023-05-10 17:45:31.000000 reus-1.1.1/reus/fbref/fb_match_metadata.py
+-rw-rw-rw-   0        0        0     4753 2023-05-11 14:41:39.000000 reus-1.1.1/reus/fbref/fb_match_misc_stats.py
+-rw-rw-rw-   0        0        0     6569 2023-05-11 14:43:26.000000 reus-1.1.1/reus/fbref/fb_match_passing_stats.py
+-rw-rw-rw-   0        0        0     4564 2023-05-11 14:43:49.000000 reus-1.1.1/reus/fbref/fb_match_passing_type_stats.py
+-rw-rw-rw-   0        0        0     6370 2023-05-11 14:44:03.000000 reus-1.1.1/reus/fbref/fb_match_possession_stats.py
+-rw-rw-rw-   0        0        0     3793 2023-05-10 17:59:04.000000 reus-1.1.1/reus/fbref/fb_match_shots.py
+-rw-rw-rw-   0        0        0     3262 2023-05-06 14:21:55.000000 reus-1.1.1/reus/fbref/fb_match_summary.py
+-rw-rw-rw-   0        0        0     6007 2023-05-11 14:46:36.000000 reus-1.1.1/reus/fbref/fb_match_summary_stats.py
+-rw-rw-rw-   0        0        0     9203 2023-05-10 18:01:05.000000 reus-1.1.1/reus/fbref/fb_match_team_stats.py
+-rw-rw-rw-   0        0        0      869 2022-09-09 21:55:47.000000 reus-1.1.1/reus/fbref/fb_match_urls.py
+-rw-rw-rw-   0        0        0     3176 2023-05-10 18:19:13.000000 reus-1.1.1/reus/fbref/fb_season_fixture_urls.py
+-rw-rw-rw-   0        0        0     3161 2023-05-10 18:16:40.000000 reus-1.1.1/reus/fbref/fb_season_urls.py
+-rw-rw-rw-   0        0        0     6142 2023-05-11 14:56:35.000000 reus-1.1.1/reus/fbref/fb_team_advanced_keeper_stats.py
+-rw-rw-rw-   0        0        0     4206 2023-05-11 15:22:22.000000 reus-1.1.1/reus/fbref/fb_team_data.py
+-rw-rw-rw-   0        0        0     4591 2023-05-11 14:56:06.000000 reus-1.1.1/reus/fbref/fb_team_defensive_actions_stats.py
+-rw-rw-rw-   0        0        0     4227 2023-05-11 15:11:09.000000 reus-1.1.1/reus/fbref/fb_team_goal_sca_stats.py
+-rw-rw-rw-   0        0        0     4272 2023-05-11 15:11:12.000000 reus-1.1.1/reus/fbref/fb_team_keeper_stats.py
+-rw-rw-rw-   0        0        0     4048 2023-05-11 15:11:14.000000 reus-1.1.1/reus/fbref/fb_team_misc_stats.py
+-rw-rw-rw-   0        0        0     6112 2023-05-11 15:11:17.000000 reus-1.1.1/reus/fbref/fb_team_passing_stats.py
+-rw-rw-rw-   0        0        0     3870 2023-05-11 15:11:20.000000 reus-1.1.1/reus/fbref/fb_team_passing_type_stats.py
+-rw-rw-rw-   0        0        0     5794 2023-05-10 20:37:39.000000 reus-1.1.1/reus/fbref/fb_team_player_advanced_keeper_stats.py
+-rw-rw-rw-   0        0        0     3149 2023-05-11 15:22:18.000000 reus-1.1.1/reus/fbref/fb_team_player_data.py
+-rw-rw-rw-   0        0        0     4366 2023-05-10 19:09:34.000000 reus-1.1.1/reus/fbref/fb_team_player_defensive_actions_stats.py
+-rw-rw-rw-   0        0        0     4156 2023-05-10 19:15:49.000000 reus-1.1.1/reus/fbref/fb_team_player_goal_sca_stats.py
+-rw-rw-rw-   0        0        0     4123 2023-05-10 19:26:43.000000 reus-1.1.1/reus/fbref/fb_team_player_keeper_stats.py
+-rw-rw-rw-   0        0        0     3930 2023-05-10 19:41:13.000000 reus-1.1.1/reus/fbref/fb_team_player_misc_stats.py
+-rw-rw-rw-   0        0        0     5823 2023-05-10 19:53:16.000000 reus-1.1.1/reus/fbref/fb_team_player_passing_stats.py
+-rw-rw-rw-   0        0        0     3807 2023-05-10 19:57:40.000000 reus-1.1.1/reus/fbref/fb_team_player_passing_type_stats.py
+-rw-rw-rw-   0        0        0     4870 2023-05-10 20:06:02.000000 reus-1.1.1/reus/fbref/fb_team_player_playing_time_stats.py
+-rw-rw-rw-   0        0        0     5548 2023-05-10 20:08:44.000000 reus-1.1.1/reus/fbref/fb_team_player_possession_stats.py
+-rw-rw-rw-   0        0        0     4208 2023-05-10 20:14:01.000000 reus-1.1.1/reus/fbref/fb_team_player_shooting_stats.py
+-rw-rw-rw-   0        0        0     5299 2023-05-10 20:28:25.000000 reus-1.1.1/reus/fbref/fb_team_player_summary_stats.py
+-rw-rw-rw-   0        0        0     4221 2023-05-10 22:30:19.000000 reus-1.1.1/reus/fbref/fb_team_playing_time_stats.py
+-rw-rw-rw-   0        0        0     5696 2023-05-11 15:11:25.000000 reus-1.1.1/reus/fbref/fb_team_possession_stats.py
+-rw-rw-rw-   0        0        0     4397 2023-05-11 15:11:27.000000 reus-1.1.1/reus/fbref/fb_team_shooting_stats.py
+-rw-rw-rw-   0        0        0     5217 2023-05-11 15:11:28.000000 reus-1.1.1/reus/fbref/fb_team_summary_stats.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.861096 reus-1.1.1/reus/fotmob/
+-rw-rw-rw-   0        0        0      143 2022-10-09 22:38:39.000000 reus-1.1.1/reus/fotmob/__init__.py
+-rw-rw-rw-   0        0        0     1466 2023-05-11 15:29:50.000000 reus-1.1.1/reus/fotmob/fm_leagues.py
+-rw-rw-rw-   0        0        0    14744 2023-05-12 15:42:45.000000 reus-1.1.1/reus/fotmob/fm_match_data.py
+-rw-rw-rw-   0        0        0     1340 2022-10-16 18:56:44.000000 reus-1.1.1/reus/fotmob/fm_match_ids.py
+-rw-rw-rw-   0        0        0     3768 2023-04-22 23:43:18.000000 reus-1.1.1/reus/fotmob/util.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.871095 reus-1.1.1/reus/transfermarkt/
+-rw-rw-rw-   0        0        0      387 2023-05-11 17:36:53.000000 reus-1.1.1/reus/transfermarkt/__init__.py
+-rw-rw-rw-   0        0        0     1522 2023-05-12 15:42:49.000000 reus-1.1.1/reus/transfermarkt/tm_player_data.py
+-rw-rw-rw-   0        0        0     1660 2023-05-12 16:18:21.000000 reus-1.1.1/reus/transfermarkt/tm_player_injury.py
+-rw-rw-rw-   0        0        0     1843 2023-05-12 16:09:28.000000 reus-1.1.1/reus/transfermarkt/tm_player_market_value.py
+-rw-rw-rw-   0        0        0     8087 2023-05-12 16:18:15.000000 reus-1.1.1/reus/transfermarkt/tm_player_metadata.py
+-rw-rw-rw-   0        0        0     3460 2023-05-12 16:18:09.000000 reus-1.1.1/reus/transfermarkt/tm_player_transfers.py
+-rw-rw-rw-   0        0        0     5796 2023-05-12 16:06:28.000000 reus-1.1.1/reus/transfermarkt/tm_team_player_data.py
+-rw-rw-rw-   0        0        0     9782 2023-05-12 16:04:59.000000 reus-1.1.1/reus/transfermarkt/tm_team_transfers.py
+-rw-rw-rw-   0        0        0     2092 2023-05-12 16:07:09.000000 reus-1.1.1/reus/transfermarkt/util.py
+-rw-rw-rw-   0        0        0     1052 2023-04-30 18:07:32.000000 reus-1.1.1/reus/util.py
+drwxrwxrwx   0        0        0        0 2023-05-13 14:51:18.812095 reus-1.1.1/reus.egg-info/
+-rw-rw-rw-   0        0        0      616 2023-05-13 14:51:18.000000 reus-1.1.1/reus.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2259 2023-05-13 14:51:18.000000 reus-1.1.1/reus.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-05-13 14:51:18.000000 reus-1.1.1/reus.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       45 2023-05-13 14:51:18.000000 reus-1.1.1/reus.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        5 2023-05-13 14:51:18.000000 reus-1.1.1/reus.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-05-13 14:51:18.873096 reus-1.1.1/setup.cfg
+-rw-rw-rw-   0        0        0      883 2022-10-09 22:40:20.000000 reus-1.1.1/setup.py
```

### Comparing `reus-1.1.0/LICENSE` & `reus-1.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `reus-1.1.0/PKG-INFO` & `reus-1.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reus
-Version: 1.1.0
+Version: 1.1.1
 Summary: A package that allows you to soccer information
 Home-page: https://github.com/ian-shepherd/reus
 Author: Ian Shepherd
 License: UNKNOWN
 Keywords: python,fbref,fotmob,transfermarkt,soccer,football
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `reus-1.1.0/README.md` & `reus-1.1.1/README.md`

 * *Files 22% similar despite different names*

```diff
@@ -29,20 +29,21 @@
 ```
 
 It is a minor inconvenience to you but lets us all keep accessing the data.
 
 Additional documentation is provided [here](https://ian-shepherd.github.io/reus/)
 
 ## Roadmap
-
+  - add fotmob league table and statistics functionality
+  - translation function for players and teams
+  - change outputs of fbref functions from lists and tuples to dictionaries
   - fbref player scouting reports
   - transfermarkt team staff
   - transfermarkt staff history
   - understat data
-  - fifa data
 
 
 ## Resources
   - [FBref](https://fbref.com/)
   - [Fotmob](https://www.fotmob.com/)
   - [Transfermarkt](http://transfermarkt.com/)
   - [FC Python](https://fcpython.com/)
```

### Comparing `reus-1.1.0/reus/fbref/__init__.py` & `reus-1.1.1/reus/fbref/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "1.1.0"
+__version__ = "1.1.1"
 
 from .fb_season_fixture_urls import fb_season_fixture_urls
 from .fb_season_urls import fb_season_urls
 from .fb_league_table import fb_league_table
 from .fb_match_urls import fb_match_urls
 from .fb_match_data import fb_match_data
 from .fb_match_metadata import fb_match_metadata
```

### Comparing `reus-1.1.0/reus/fbref/fb_league_table.py` & `reus-1.1.1/reus/fbref/fb_league_table.py`

 * *Files 16% similar despite different names*

```diff
@@ -20,52 +20,64 @@
 
     # Generate empty list
     mylist = []
 
     # iterate through each team and store attributes
     for row in rows:
         rank = row.find("th", {"data-stat": "rank"}).text
-        team = row.find("td", {"data-stat": "squad"}).text.strip()
+        team = row.find("td", {"data-stat": "team"}).text.strip()
+        team_id = (
+            row.find("td", {"data-stat": "team"})
+            .find("a", href=True)["href"]
+            .split("/")[3]
+        )
         matches = row.find("td", {"data-stat": "games"}).text
         wins = row.find("td", {"data-stat": "wins"}).text
-        draws = row.find("td", {"data-stat": "draws"}).text
+        draws = row.find("td", {"data-stat": "ties"}).text
         losses = row.find("td", {"data-stat": "losses"}).text
         goals = row.find("td", {"data-stat": "goals_for"}).text
         goals_allowed = row.find("td", {"data-stat": "goals_against"}).text
-        goal_differential = float(row.find("td", {"data-stat": "goal_diff"}).text)
+        goal_differential = row.find("td", {"data-stat": "goal_diff"}).text
         points = row.find("td", {"data-stat": "points"}).text
+        ppg = row.find("td", {"data-stat": "points_avg"}).text
         try:
             xG = row.find("td", {"data-stat": "xg_for"}).text
             xGA = row.find("td", {"data-stat": "xg_against"}).text
             xGD = float(row.find("td", {"data-stat": "xg_diff"}).text)
             xGDp90 = float(row.find("td", {"data-stat": "xg_diff_per90"}).text)
         except AttributeError:
             xG = xGA = xGD = xGDp90 = None
-
+        last_5_ = row.find("td", {"data-stat": "last_5"})
+        last_5 = ""
+        for t in last_5_.find_all("div", {"class": "poptip"}):
+            last_5 += t.text
         avg_attendance = row.find("td", {"data-stat": "attendance_per_g"}).text
         top_scorer = row.find("td", {"data-stat": "top_team_scorers"}).text
         goalkeeper = row.find("td", {"data-stat": "top_keeper"}).text
         notes = row.find("td", {"data-stat": "notes"}).text
 
         # generate dictionary for each player
         mydict = {
             "rank": rank,
             "team": team,
+            "team_id": team_id,
             "matches": matches,
             "wins": wins,
             "draws": draws,
             "losses": losses,
             "G": goals,
             "GA": goals_allowed,
             "GD": goal_differential,
             "Points": points,
+            "Pts/MP": ppg,
             "xG": xG,
             "xGA": xGA,
             "xGD": xGD,
             "xGD/90": xGDp90,
+            "last_5": last_5,
             "avg_attendance": avg_attendance,
             "top_scorer": top_scorer,
             "goalkeeper": goalkeeper,
             "notes": notes,
         }
 
         # append dictionary to list
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_defensive_actions_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_defensive_actions_stats.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,107 +1,115 @@
-from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_match_defensive_actions_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts defensive stats for each player in a given match that includes StatsBomb data
+def fb_team_player_defensive_actions_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts defensive action stats for each player in a given team
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
-        url (str, optional): path of fbref match page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
+        url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        tuple: defensive stats for home and away team players
-            list: defensive stats for home team players
-            list: defensive stats for away team players
+        list: defensive stats for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
-    id_x = metadata.get("id_x")
-    id_y = metadata.get("id_y")
-
-    # Loop through both teams
-    for team_id in [id_x, id_y]:
-        # generate empty list for each team
-        mylist = []
-        # generate html id
-        id_ = "stats_" + team_id + "_defense"
-
-        # find defensive actions object
-        stats_players = pageSoup.find("table", {"id": id_})
-        stats_players = stats_players.find_all("tr")
-
-        # iterate through each player and store metrics
-        for row in stats_players[2:-1]:
-            th = row.find("th")
-            player_id = th.find("a", href=True)["href"].split("/")[3]
-
-            tkl = row.find("td", {"data-stat": "tackles"}).text
-            tklW = row.find("td", {"data-stat": "tackles_won"}).text
-            tkl_def = row.find("td", {"data-stat": "tackles_def_3rd"}).text
-            tkl_mid = row.find("td", {"data-stat": "tackles_mid_3rd"}).text
-            tkl_att = row.find("td", {"data-stat": "tackles_att_3rd"}).text
-            drb_tkl = row.find("td", {"data-stat": "dribble_tackles"}).text
-            drb_att = row.find("td", {"data-stat": "dribbles_vs"}).text
-            drb_pct = row.find("td", {"data-stat": "dribble_tackles_pct"}).text
-            drb_past = row.find("td", {"data-stat": "dribbled_past"}).text
-            press = row.find("td", {"data-stat": "pressures"}).text
-            press_succ = row.find("td", {"data-stat": "pressure_regains"}).text
-            press_pct = row.find("td", {"data-stat": "pressure_regain_pct"}).text
-            press_def = row.find("td", {"data-stat": "pressures_def_3rd"}).text
-            press_mid = row.find("td", {"data-stat": "pressures_mid_3rd"}).text
-            press_att = row.find("td", {"data-stat": "pressures_att_3rd"}).text
-            blk = row.find("td", {"data-stat": "blocks"}).text
-            blk_shots = row.find("td", {"data-stat": "blocked_shots"}).text
-            blk_sv = row.find("td", {"data-stat": "blocked_shots_saves"}).text
-            blk_pass = row.find("td", {"data-stat": "blocked_passes"}).text
-            interceptions = row.find("td", {"data-stat": "interceptions"}).text
-            tkl_int = row.find("td", {"data-stat": "tackles_interceptions"}).text
-            clr = row.find("td", {"data-stat": "clearances"}).text
-            err = row.find("td", {"data-stat": "errors"}).text
-
-            # generate dictionary for team
-            mydict = {
-                "player_id": player_id,
-                "tackles": tkl,
-                "tackles_won": tklW,
-                "tackles_defensive_third": tkl_def,
-                "tackles_middle_third": tkl_mid,
-                "tackles_attacking_third": tkl_att,
-                "dribble_tackles": drb_tkl,
-                "dribble_tackles_attempted": drb_att,
-                "dribble_pct": drb_pct,
-                "dribbled_past": drb_past,
-                "pressures": press,
-                "pressures_successful": press_succ,
-                "pressure_pct": press_pct,
-                "pressures_defensive_third": press_def,
-                "pressures_middle_third": press_mid,
-                "pressures_attacking_third": press_att,
-                "blocks": blk,
-                "blocked_shots": blk_shots,
-                "blocked_shots_on_target": blk_sv,
-                "blocked_passes": blk_pass,
-                "interceptions": interceptions,
-                "tkl_int": tkl_int,
-                "clearances": clr,
-                "errors": err,
-            }
-
-            # add to empty list
-            mylist.append(mydict)
-
-        # assign list to appropriate team
-        if team_id == id_x:
-            defensive_stats_x = mylist.copy()
-        else:
-            defensive_stats_y = mylist.copy()
+    # Find table object
+    div = pageSoup.find("div", {"id": "all_stats_defense"})
+    if div is None:
+        return None
+
+    table = div.find("table")
+    tbody = table.find("tbody")
+    rows = tbody.find_all("tr")
+
+    # Generate empty list
+    mylist = []
+
+    # iterate through each player and store attributes
+    for row in rows:
+        # general
+        th = row.find("th")
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
+        player_id = th.find("a", href=True)["href"].split("/")[3]
+        nation = row.find("td", {"data-stat": "nationality"}).text
+        position = row.find("td", {"data-stat": "position"}).text
+        age = row.find("td", {"data-stat": "age"}).text.split("-")
+        try:
+            age = int(age[0]) + int(age[1]) / 365
+        except ValueError:
+            age = None
+        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+
+        # tackles
+        tackles_attempted = row.find("td", {"data-stat": "tackles"}).text
+        tackles_successful = row.find("td", {"data-stat": "tackles_won"}).text
+        tackles_defensive_third = row.find("td", {"data-stat": "tackles_def_3rd"}).text
+        tackles_middle_third = row.find("td", {"data-stat": "tackles_mid_3rd"}).text
+        tackles_attacking_third = row.find("td", {"data-stat": "tackles_att_3rd"}).text
+
+        # challenges
+        challenges_successful = row.find("td", {"data-stat": "challenge_tackles"}).text
+        challenges_attempted = row.find("td", {"data-stat": "challenges"}).text
+        challenge_success_rate = row.find(
+            "td", {"data-stat": "challenge_tackles_pct"}
+        ).text
+        if challenge_success_rate == "":
+            challenge_success_rate = None
+        challenges_lost = row.find("td", {"data-stat": "challenges_lost"}).text
+
+        # blocks
+        blocks = row.find("td", {"data-stat": "blocks"}).text
+        blocked_shots = row.find("td", {"data-stat": "blocked_shots"}).text
+        blocked_passes = row.find("td", {"data-stat": "blocked_passes"}).text
+
+        # other
+        interceptions = row.find("td", {"data-stat": "interceptions"}).text
+        tkl_int = row.find("td", {"data-stat": "tackles_interceptions"}).text
+        clearances = row.find("td", {"data-stat": "clearances"}).text
+        errors = row.find("td", {"data-stat": "errors"}).text
+
+        # match logs
+        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
+            "href"
+        ]
+
+        # generate dictionary for player
+        mydict = {
+            "player_id": player_id,
+            "name": name,
+            "nation": nation,
+            "position": position,
+            "age": age,
+            "90s": minutes_90,
+            "tackles_attempted": tackles_attempted,
+            "tackles_successful": tackles_successful,
+            "tackles_defensive_third": tackles_defensive_third,
+            "tackles_middle_third": tackles_middle_third,
+            "tackles_attacking_third": tackles_attacking_third,
+            "challenges_successful": challenges_successful,
+            "challenges_attempted": challenges_attempted,
+            "challenge_success_rate": challenge_success_rate,
+            "challenges_lost": challenges_lost,
+            "blocks": blocks,
+            "blocked_shots": blocked_shots,
+            "blocked_passes": blocked_passes,
+            "interceptions": interceptions,
+            "tkl_int": tkl_int,
+            "clearances": clearances,
+            "errors": errors,
+            "match_logs": match_logs,
+        }
 
-    return defensive_stats_x, defensive_stats_y
+        # add to empty list
+        mylist.append(mydict)
+
+    return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_keeper_stats.py` & `reus-1.1.1/reus/fbref/fb_match_keeper_stats.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
 def fb_match_keeper_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts goalkeeping stats for each keeper in a given match that includes StatsBomb data
+    """Extracts goalkeeping stats for each keeper in a given match that includes advanced data
 
     Args:
         pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
         url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
         tuple: goalkeeping stats for home and away team
@@ -19,15 +19,15 @@
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
+    metadata = fb_match_metadata(pageSoup)[0]
     id_x = metadata.get("id_x")
     id_y = metadata.get("id_y")
 
     # Loop through both teams
     for team_id in [id_x, id_y]:
         # generate empty list for each team
         mylist = []
@@ -37,53 +37,99 @@
         # find goalkeeping object
         stats_keeper = pageSoup.find("table", {"id": id_})
         stats_keeper = stats_keeper.find_all("tr")
 
         # iterate through each keeper and store metrics
         for row in stats_keeper[2:]:
             th = row.find("th")
-            name = th["csk"]
-            player_id = th.find("a", href=True)["href"].split("/")[3]
 
+            # general
+            try:
+                name = th.text
+            except AttributeError:
+                name = th["csk"]
+
+            player_id = th.find("a", href=True)["href"].split("/")[3]
             nation = row.find("td", {"data-stat": "nationality"}).text
             age = row.find("td", {"data-stat": "age"}).text.split("-")
-            age = int(age[0]) + int(age[1]) / 365
+            try:
+                age = int(age[0]) + int(age[1]) / 365
+            except ValueError:
+                age = None
             minutes = row.find("td", {"data-stat": "minutes"}).text
+
+            # shot stopping
             shots_against = row.find(
                 "td", {"data-stat": "gk_shots_on_target_against"}
             ).text
             goals_allowed = row.find("td", {"data-stat": "gk_goals_against"}).text
             saves = row.find("td", {"data-stat": "gk_saves"}).text
             save_pct = row.find("td", {"data-stat": "gk_save_pct"}).text
+            if save_pct == "":
+                save_pct = None
             psxg = row.find("td", {"data-stat": "gk_psxg"}).text
+
+            # launched
             launched_completed = row.find(
                 "td", {"data-stat": "gk_passes_completed_launched"}
             ).text
             launched_attempted = row.find(
                 "td", {"data-stat": "gk_passes_launched"}
             ).text
-            launched_acc = row.find("td", {"data-stat": "gk_passes_pct_launched"}).text
+            launched_accuracy = row.find(
+                "td", {"data-stat": "gk_passes_pct_launched"}
+            ).text
+            if launched_accuracy == "":
+                launched_accuracy = None
+
+            # passes
             passes_attempted = row.find("td", {"data-stat": "gk_passes"}).text
+            if passes_attempted == "":
+                passes_attempted = None
             throws_attempted = row.find("td", {"data-stat": "gk_passes_throws"}).text
-            pct_lauched = row.find("td", {"data-stat": "gk_pct_passes_launched"}).text
+            if throws_attempted == "":
+                throws_attempted = None
+            pct_launched = row.find("td", {"data-stat": "gk_pct_passes_launched"}).text
+            if pct_launched == "":
+                pct_launched = None
             passes_avg_length = row.find(
                 "td", {"data-stat": "gk_passes_length_avg"}
             ).text
+            if passes_avg_length == "":
+                passes_avg_length = None
+
+            # goal kicks
             gk_attempted = row.find("td", {"data-stat": "gk_goal_kicks"}).text
+            if gk_attempted == "":
+                gk_attempted = None
             gk_pct_launched = row.find(
                 "td", {"data-stat": "gk_pct_goal_kicks_launched"}
             ).text
+            if gk_pct_launched == "":
+                gk_pct_launched = None
             gk_avg_length = row.find(
                 "td", {"data-stat": "gk_goal_kick_length_avg"}
             ).text
+            if gk_avg_length == "":
+                gk_avg_length = None
+
+            # crosses
             crosses_faced = row.find("td", {"data-stat": "gk_crosses"}).text
+            if crosses_faced == "":
+                crosses_faced = None
             crosses_stopped = row.find("td", {"data-stat": "gk_crosses_stopped"}).text
+            if crosses_stopped == "":
+                crosses_stopped = None
             crosses_stopped_pct = row.find(
                 "td", {"data-stat": "gk_crosses_stopped_pct"}
             ).text
+            if crosses_stopped_pct == "":
+                crosses_stopped_pct = None
+
+            # sweeper
             defensive_actions = row.find(
                 "td", {"data-stat": "gk_def_actions_outside_pen_area"}
             ).text
             defensive_actions_avg_distance = row.find(
                 "td", {"data-stat": "gk_avg_distance_def_actions"}
             ).text
 
@@ -93,22 +139,22 @@
                 "name": name,
                 "nation": nation,
                 "age": age,
                 "minutes": minutes,
                 "shots_against": shots_against,
                 "goals_allowed": goals_allowed,
                 "saves": saves,
-                "saves_pct": save_pct,
+                "save_pct": save_pct,
                 "psxg": psxg,
                 "launched_completed": launched_completed,
                 "launched_attempted": launched_attempted,
-                "launched_accuracy": launched_acc,
+                "launched_accuracy": launched_accuracy,
                 "passes_attempted": passes_attempted,
                 "throws_attempted": throws_attempted,
-                "pct_launched": pct_lauched,
+                "pct_launched": pct_launched,
                 "passes_avg_length": passes_avg_length,
                 "gk_attempted": gk_attempted,
                 "gk_pct_launched": gk_pct_launched,
                 "gk_avg_length": gk_avg_length,
                 "crosses_faced": crosses_faced,
                 "crosses_stopped": crosses_stopped,
                 "crosses_stopped_pct": crosses_stopped_pct,
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_lineups.py` & `reus-1.1.1/reus/fbref/fb_match_lineups.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,55 +23,55 @@
     # Find lineup object
     lineup = pageSoup.find_all("div", {"class": "lineup"})
 
     # Home team
     lineup_x = lineup[0].find("table").find_all("tr")
     formation_x = lineup_x[0].text
     # generate empty lists
-    squad_x = []
+    starter_x = []
     bench_x = []
     role = "starter"
 
     # iterate through each player and store status and id
     for row in lineup_x[1:]:
         if row == lineup_x[12]:
             role = "bench"
             continue
 
         if role == "starter":
-            squad_x.append(row.find("a", href=True)["href"])
+            starter_x.append(row.find("a", href=True)["href"])
         elif role == "bench":
             bench_x.append(row.find("a", href=True)["href"])
 
     # Away team
     lineup_y = lineup[1].find("table").find_all("tr")
     formation_y = lineup_y[0].text
     # generate empty lists
-    squad_y = []
+    starter_y = []
     bench_y = []
     role = "starter"
 
     # iterate through each player and store status and id
     for row in lineup_y[1:]:
         if row == lineup_y[12]:
             role = "bench"
             continue
 
         if role == "starter":
-            squad_y.append(row.find("a", href=True)["href"])
+            starter_y.append(row.find("a", href=True)["href"])
         elif role == "bench":
             bench_y.append(row.find("a", href=True)["href"])
 
     # pattern to extract formation
     pattern = r"\(([^)]+)\)"
 
     # generate dictionary
     mydict = {
         "formation_x": re.search(pattern, formation_x).group(1),
         "formation_y": re.search(pattern, formation_y).group(1),
-        "squad_x": squad_x,
+        "starter_x": starter_x,
         "bench_x": bench_x,
-        "squad_y": squad_y,
+        "starter_y": starter_y,
         "bench_y": bench_y,
     }
 
     return mydict
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_misc_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_misc_stats.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,93 +1,108 @@
-from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_match_misc_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts miscellaneous stats for each player in a given match that includes StatsBomb data
+def fb_team_player_misc_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts miscellaneous stats for rach player in a given team
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
-        url (str, optional): path of fbref match page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
+        url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        tuple: miscellaneous stats for home and away team players
-            list: miscellaneous stats of home team players
-            list: miscellaneous stats of away team players
+        list: miscellaneous stats for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
-    id_x = metadata.get("id_x")
-    id_y = metadata.get("id_y")
-
-    # Loop through both teams
-    for team_id in [id_x, id_y]:
-        # generate empty list for each team
-        mylist = []
-        # generate html id
-        id_ = "stats_" + team_id + "_misc"
-
-        # find miscellaneous stats object
-        stats_players = pageSoup.find("table", {"id": id_})
-        stats_players = stats_players.find_all("tr")
-
-        # iterate through each player and store metrics
-        for row in stats_players[2:-1]:
-            th = row.find("th")
-            player_id = th.find("a", href=True)["href"].split("/")[3]
-
-            crdY = row.find("td", {"data-stat": "cards_yellow"}).text
-            crdR = row.find("td", {"data-stat": "cards_red"}).text
-            crdY2 = row.find("td", {"data-stat": "cards_yellow_red"}).text
-            fls = row.find("td", {"data-stat": "fouls"}).text
-            fld = row.find("td", {"data-stat": "fouled"}).text
-            off = row.find("td", {"data-stat": "offsides"}).text
-            crs = row.find("td", {"data-stat": "crosses"}).text
-            interceptions = row.find("td", {"data-stat": "interceptions"}).text
-            tklW = row.find("td", {"data-stat": "tackles_won"}).text
-            pk_won = row.find("td", {"data-stat": "pens_won"}).text
-            pk_con = row.find("td", {"data-stat": "pens_conceded"}).text
-            og = row.find("td", {"data-stat": "own_goals"}).text
-            recov = row.find("td", {"data-stat": "ball_recoveries"}).text
-            aerial_won = row.find("td", {"data-stat": "aerials_won"}).text
-            aerial_lost = row.find("td", {"data-stat": "aerials_lost"}).text
-            aerial_pct = row.find("td", {"data-stat": "aerials_won_pct"}).text
-
-            # generate dictionary for team
-            mydict = {
-                "player_id": player_id,
-                "cards_yellow": crdY,
-                "cards_red": crdR,
-                "cards_second_yellow": crdY2,
-                "fouls": fls,
-                "fouled": fld,
-                "offsides": off,
-                "crosses": crs,
-                "interceptions": interceptions,
-                "tackles_won": tklW,
-                "pk_won": pk_won,
-                "pk_con": pk_con,
-                "own_goals": og,
-                "recoveries": recov,
-                "aerials_won": aerial_won,
-                "aerials_lost": aerial_lost,
-                "aerials_pct": aerial_pct,
-            }
-
-            # add to empty list
-            mylist.append(mydict)
-
-        # assign list to appropriate team
-        if team_id == id_x:
-            players_misc_stats_x = mylist.copy()
-        else:
-            players_misc_stats_y = mylist.copy()
+    # Find table object
+    div = pageSoup.find("div", {"id": "all_stats_misc"})
+    if div is None:
+        return None
+
+    table = div.find("table")
+    table = div.find("table")
+    tbody = table.find("tbody")
+    rows = tbody.find_all("tr")
+
+    # Generate empty list
+    mylist = []
+
+    # iterate through each player and store attributes
+    for row in rows:
+        # general
+        th = row.find("th")
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
+        player_id = th.find("a", href=True)["href"].split("/")[3]
+        nation = row.find("td", {"data-stat": "nationality"}).text
+        position = row.find("td", {"data-stat": "position"}).text
+        age = row.find("td", {"data-stat": "age"}).text.split("-")
+        try:
+            age = int(age[0]) + int(age[1]) / 365
+        except ValueError:
+            age = None
+
+        # performance
+        cards_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
+        cards_red = row.find("td", {"data-stat": "cards_red"}).text
+        cards_yellow_red = row.find("td", {"data-stat": "cards_yellow_red"}).text
+        fouls = row.find("td", {"data-stat": "fouls"}).text
+        fouled = row.find("td", {"data-stat": "fouled"}).text
+        offsides = row.find("td", {"data-stat": "offsides"}).text
+        crosses = row.find("td", {"data-stat": "crosses"}).text
+        interceptions = row.find("td", {"data-stat": "interceptions"}).text
+        tackles_won = row.find("td", {"data-stat": "tackles_won"}).text
+        penalties_won = row.find("td", {"data-stat": "pens_won"}).text
+        penalties_conceded = row.find("td", {"data-stat": "pens_conceded"}).text
+        own_goals = row.find("td", {"data-stat": "own_goals"}).text
+        recoveries = row.find("td", {"data-stat": "ball_recoveries"}).text
+
+        # aerial duels
+        aerials_won = row.find("td", {"data-stat": "aerials_won"}).text
+        aerials_lost = row.find("td", {"data-stat": "aerials_lost"}).text
+        aerials_won_pct = row.find("td", {"data-stat": "aerials_won_pct"}).text
+        if aerials_won_pct == "":
+            aerials_won_pct = None
+
+        # match logs
+        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
+            "href"
+        ]
+
+        # generate dictionary for player
+        mydict = {
+            "player_id": player_id,
+            "name": name,
+            "nation": nation,
+            "position": position,
+            "age": age,
+            "cards_yellow": cards_yellow,
+            "cards_red": cards_red,
+            "cards_yellow_red": cards_yellow_red,
+            "fouls": fouls,
+            "fouled": fouled,
+            "offsides": offsides,
+            "crosses": crosses,
+            "interceptions": interceptions,
+            "tackles_won": tackles_won,
+            "pk_won": penalties_won,
+            "pk_con": penalties_conceded,
+            "own_goals": own_goals,
+            "recoveries": recoveries,
+            "aerials_won": aerials_won,
+            "aerials_lost": aerials_lost,
+            "aerials_won_pct": aerials_won_pct,
+            "match_logs": match_logs,
+        }
 
-    return players_misc_stats_x, players_misc_stats_y
+        # add to empty list
+        mylist.append(mydict)
+
+    return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_passing_stats.py` & `reus-1.1.1/reus/fbref/fb_team_passing_type_stats.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,102 +1,96 @@
-from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_match_passing_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts passing stats for each player in a given match that includes StatsBomb data
+def fb_team_passing_type_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts passing type stats for each team in a given league
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
-        url (str, optional): path of fbref match page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
+        url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        tuple: passing stats for home and away team players
-            list: passing stats of home team players
-            list: passing stats of away team players
+        tuple: passing type stats for home and away team players
+            list: passing type stats for each team
+            list: passing type stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
-    id_x = metadata.get("id_x")
-    id_y = metadata.get("id_y")
-
-    # Loop through both teams
-    for team_id in [id_x, id_y]:
+    for side in ["for", "against"]:
         # generate empty list for each team
         mylist = []
         # generate html id
-        id_ = "stats_" + team_id + "_passing"
+        id_ = "stats_squads_passing_types_" + side
 
-        # find passing object
-        stats_players = pageSoup.find("table", {"id": id_})
-        stats_players = stats_players.find_all("tr")
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
 
-        # iterate through each player and store metrics
-        for row in stats_players[2:-1]:
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
             th = row.find("th")
-            player_id = th.find("a", href=True)["href"].split("/")[3]
-
-            cmp = row.find("td", {"data-stat": "passes_completed"}).text
-            att = row.find("td", {"data-stat": "passes"}).text
-            acc = row.find("td", {"data-stat": "passes_pct"}).text
-            totdist = row.find("td", {"data-stat": "passes_total_distance"}).text
-            prgdist = row.find("td", {"data-stat": "passes_progressive_distance"}).text
-            short_cmp = row.find("td", {"data-stat": "passes_completed_short"}).text
-            short_att = row.find("td", {"data-stat": "passes_short"}).text
-            short_acc = row.find("td", {"data-stat": "passes_pct_short"}).text
-            med_cmp = row.find("td", {"data-stat": "passes_completed_medium"}).text
-            med_att = row.find("td", {"data-stat": "passes_medium"}).text
-            med_acc = row.find("td", {"data-stat": "passes_pct_medium"}).text
-            long_cmp = row.find("td", {"data-stat": "passes_completed_long"}).text
-            long_att = row.find("td", {"data-stat": "passes_long"}).text
-            long_acc = row.find("td", {"data-stat": "passes_pct_long"}).text
-            ast = row.find("td", {"data-stat": "assists"}).text
-            xA = row.find("td", {"data-stat": "xa"}).text
-            key_passes = row.find("td", {"data-stat": "assisted_shots"}).text
-            final_third = row.find("td", {"data-stat": "passes_into_final_third"}).text
-            ppa = row.find("td", {"data-stat": "passes_into_penalty_area"}).text
-            crs_ppa = row.find("td", {"data-stat": "crosses_into_penalty_area"}).text
-            prog = row.find("td", {"data-stat": "progressive_passes"}).text
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+            matches = row.find("td", {"data-stat": "minutes_90s"}).text
+            passes_attempted = row.find("td", {"data-stat": "passes"}).text
+
+            # pass types
+            live = row.find("td", {"data-stat": "passes_live"}).text
+            dead = row.find("td", {"data-stat": "passes_dead"}).text
+            free_kicks = row.find("td", {"data-stat": "passes_free_kicks"}).text
+            through_balls = row.find("td", {"data-stat": "through_balls"}).text
+            switches = row.find("td", {"data-stat": "passes_switches"}).text
+            crosses = row.find("td", {"data-stat": "crosses"}).text
+            throw_ins = row.find("td", {"data-stat": "throw_ins"}).text
+            corner_kicks = row.find("td", {"data-stat": "corner_kicks"}).text
+
+            # corner kicks
+            ck_in = row.find("td", {"data-stat": "corner_kicks_in"}).text
+            ck_out = row.find("td", {"data-stat": "corner_kicks_out"}).text
+            ck_straight = row.find("td", {"data-stat": "corner_kicks_straight"}).text
+
+            # outcomes
+            completed = row.find("td", {"data-stat": "passes_completed"}).text
+            offsides = row.find("td", {"data-stat": "passes_offsides"}).text
+            blocked = row.find("td", {"data-stat": "passes_blocked"}).text
 
+            # generate dictionary for team
             mydict = {
-                "player_id": player_id,
-                "completed": cmp,
-                "attempted": att,
-                "accuracy": acc,
-                "total_distance": totdist,
-                "progressive_distance": prgdist,
-                "short_completed": short_cmp,
-                "short_attempted": short_att,
-                "short_accuracy": short_acc,
-                "medium_completed": med_cmp,
-                "medium_attempted": med_att,
-                "medium_accuracy": med_acc,
-                "long_completed": long_cmp,
-                "long_attempted": long_att,
-                "long_accuracy": long_acc,
-                "assists": ast,
-                "xA": xA,
-                "key_passes": key_passes,
-                "into_final_third": final_third,
-                "into_penalty_area": ppa,
-                "crosses_into_penalty_area": crs_ppa,
-                "progressive_passes": prog,
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
+                "passes_attempted": passes_attempted,
+                "live": live,
+                "dead": dead,
+                "free_kicks": free_kicks,
+                "through_balls": through_balls,
+                "switches": switches,
+                "crosses": crosses,
+                "throw_ins": throw_ins,
+                "corner_kicks": corner_kicks,
+                "ck_in": ck_in,
+                "ck_out": ck_out,
+                "ck_straight": ck_straight,
+                "completed": completed,
+                "offsides": offsides,
+                "blocked": blocked,
             }
 
             # add to empty list
             mylist.append(mydict)
 
         # assign list to appropriate team
-        if team_id == id_x:
-            players_passing_stats_x = mylist.copy()
+        if side == "for":
+            passing_type_stats_for = mylist.copy()
         else:
-            players_passing_stats_y = mylist.copy()
+            passing_type_stats_against = mylist.copy()
 
-    return players_passing_stats_x, players_passing_stats_y
+    return passing_type_stats_for, passing_type_stats_against
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_passing_type_stats.py` & `reus-1.1.1/reus/fbref/fb_match_passing_type_stats.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,111 +1,116 @@
 from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_match_passing_type_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts passing type statistics for each player in a given match that includes StatsBomb data
+def fb_match_passing_type_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts passing type stats for each player in a given match that includes advanced data
 
     Args:
         pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
         url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
-        tuple: passing stats for home and away team players
+        tuple: passing type stats for home and away team players
             list: passing type stats of home team players
             list: passing type stats of away team players
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
+    metadata = fb_match_metadata(pageSoup)[0]
     id_x = metadata.get("id_x")
     id_y = metadata.get("id_y")
 
     # Loop through both teams
     for team_id in [id_x, id_y]:
         # generate empty list for each team
         mylist = []
         # generate html id
         id_ = "stats_" + team_id + "_passing_types"
 
-        # find passing types object
+        # find passing type object
         stats_players = pageSoup.find("table", {"id": id_})
         stats_players = stats_players.find_all("tr")
 
         # iterate through each player and store metrics
         for row in stats_players[2:-1]:
             th = row.find("th")
+
+            # general
+            try:
+                name = th.text
+            except AttributeError:
+                name = th["csk"]
             player_id = th.find("a", href=True)["href"].split("/")[3]
 
-            att = row.find("td", {"data-stat": "passes"}).text
+            nation = row.find("td", {"data-stat": "nationality"}).text
+            position = row.find("td", {"data-stat": "position"}).text
+            age = row.find("td", {"data-stat": "age"}).text.split("-")
+            try:
+                age = int(age[0]) + int(age[1]) / 365
+            except ValueError:
+                age = None
+            minutes = row.find("td", {"data-stat": "minutes"}).text
+            passes_attempted = row.find("td", {"data-stat": "passes"}).text
+
+            # pass types
             live = row.find("td", {"data-stat": "passes_live"}).text
             dead = row.find("td", {"data-stat": "passes_dead"}).text
-            fk = row.find("td", {"data-stat": "passes_free_kicks"}).text
-            tb = row.find("td", {"data-stat": "through_balls"}).text
-            press = row.find("td", {"data-stat": "passes_pressure"}).text
-            sw = row.find("td", {"data-stat": "passes_switches"}).text
-            crs = row.find("td", {"data-stat": "crosses"}).text
-            ck = row.find("td", {"data-stat": "corner_kicks"}).text
+            free_kicks = row.find("td", {"data-stat": "passes_free_kicks"}).text
+            through_balls = row.find("td", {"data-stat": "through_balls"}).text
+            switches = row.find("td", {"data-stat": "passes_switches"}).text
+            crosses = row.find("td", {"data-stat": "crosses"}).text
+            throw_ins = row.find("td", {"data-stat": "throw_ins"}).text
+            corner_kicks = row.find("td", {"data-stat": "corner_kicks"}).text
+
+            # corner kicks
             ck_in = row.find("td", {"data-stat": "corner_kicks_in"}).text
             ck_out = row.find("td", {"data-stat": "corner_kicks_out"}).text
             ck_straight = row.find("td", {"data-stat": "corner_kicks_straight"}).text
-            height_ground = row.find("td", {"data-stat": "passes_ground"}).text
-            height_low = row.find("td", {"data-stat": "passes_low"}).text
-            height_high = row.find("td", {"data-stat": "passes_high"}).text
-            body_left = row.find("td", {"data-stat": "passes_left_foot"}).text
-            body_right = row.find("td", {"data-stat": "passes_right_foot"}).text
-            body_head = row.find("td", {"data-stat": "passes_head"}).text
-            body_ti = row.find("td", {"data-stat": "throw_ins"}).text
-            body_other = row.find("td", {"data-stat": "passes_other_body"}).text
-            out_cmp = row.find("td", {"data-stat": "passes_completed"}).text
-            out_off = row.find("td", {"data-stat": "passes_offsides"}).text
-            out_out = row.find("td", {"data-stat": "passes_oob"}).text
-            out_int = row.find("td", {"data-stat": "passes_intercepted"}).text
-            out_blk = row.find("td", {"data-stat": "passes_blocked"}).text
 
-            # generate dictionary for team
+            # outcomes
+            completed = row.find("td", {"data-stat": "passes_completed"}).text
+            offsides = row.find("td", {"data-stat": "passes_offsides"}).text
+            blocked = row.find("td", {"data-stat": "passes_blocked"}).text
+
+            # generate dictionary for player
             mydict = {
                 "player_id": player_id,
-                "attempted": att,
+                "name": name,
+                "nation": nation,
+                "position": position,
+                "age": age,
+                "minutes": minutes,
+                "passes_attempted": passes_attempted,
                 "live": live,
                 "dead": dead,
-                "free_kick": fk,
-                "through_balls": tb,
-                "under_pressure": press,
-                "switches": sw,
-                "crosses": crs,
-                "corner_kicks": ck,
-                "corner_inswing": ck_in,
-                "corner_outswing": ck_out,
-                "corner_straight": ck_straight,
-                "height_ground": height_ground,
-                "height_low": height_low,
-                "height_high": height_high,
-                "body_left": body_left,
-                "body_right": body_right,
-                "body_head": body_head,
-                "body_throw_in": body_ti,
-                "body_other": body_other,
-                "completed": out_cmp,
-                "offsides": out_off,
-                "out_of_bounds": out_out,
-                "intercepted": out_int,
-                "blocked": out_blk,
+                "free_kicks": free_kicks,
+                "through_balls": through_balls,
+                "switches": switches,
+                "crosses": crosses,
+                "throw_ins": throw_ins,
+                "corner_kicks": corner_kicks,
+                "ck_in": ck_in,
+                "ck_out": ck_out,
+                "ck_straight": ck_straight,
+                "completed": completed,
+                "offsides": offsides,
+                "blocked": blocked,
             }
 
-            # add to empty list
+            # add to team list
             mylist.append(mydict)
 
         # assign list to appropriate team
         if team_id == id_x:
-            players_passing_stats_x = mylist.copy()
+            player_passing_type_stats_x = mylist.copy()
         else:
-            players_passing_stats_y = mylist.copy()
+            player_passing_type_stats_y = mylist.copy()
 
-    return players_passing_stats_x, players_passing_stats_y
+    return player_passing_type_stats_x, player_passing_type_stats_y
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_possession_stats.py` & `reus-1.1.1/reus/fbref/fb_team_possession_stats.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,117 +1,132 @@
-from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_match_possession_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts possession statistics for each player in a given match that includes StatsBomb data
+def fb_team_possession_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts possession stats for each team in a given league
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
-        url (str, optional): path of fbref match page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
+        url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
         tuple: possession stats for home and away team players
-            list: possession stats of home team players
-            list: possession stats of away team players
+            list: possession stats for each team
+            list: possession stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
-    id_x = metadata.get("id_x")
-    id_y = metadata.get("id_y")
-
-    # Loop through both teams
-    for team_id in [id_x, id_y]:
+    for side in ["for", "against"]:
         # generate empty list for each team
         mylist = []
         # generate html id
-        id_ = "stats_" + team_id + "_possession"
+        id_ = "stats_squads_possession_" + side
 
-        # find possession object
-        stats_players = pageSoup.find("table", {"id": id_})
-        stats_players = stats_players.find_all("tr")
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
 
-        # iterate through each player and store metrics
-        for row in stats_players[2:-1]:
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
             th = row.find("th")
-            player_id = th.find("a", href=True)["href"].split("/")[3]
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+            matches = row.find("td", {"data-stat": "minutes_90s"}).text
 
+            # touches
             touches = row.find("td", {"data-stat": "touches"}).text
-            touches_def_pen = row.find("td", {"data-stat": "touches_def_pen_area"}).text
-            touches_def = row.find("td", {"data-stat": "touches_def_3rd"}).text
-            touches_mid = row.find("td", {"data-stat": "touches_mid_3rd"}).text
-            touches_att = row.find("td", {"data-stat": "touches_att_3rd"}).text
-            touches_att_pen = row.find("td", {"data-stat": "touches_att_pen_area"}).text
+            touches_def_pen_area = row.find(
+                "td", {"data-stat": "touches_def_pen_area"}
+            ).text
+            touches_def_3rd = row.find("td", {"data-stat": "touches_def_3rd"}).text
+            touches_mid_3rd = row.find("td", {"data-stat": "touches_mid_3rd"}).text
+            touches_att_3rd = row.find("td", {"data-stat": "touches_att_3rd"}).text
+            touches_att_pen_area = row.find(
+                "td", {"data-stat": "touches_att_pen_area"}
+            ).text
             touches_live = row.find("td", {"data-stat": "touches_live_ball"}).text
-            dribble_success = row.find("td", {"data-stat": "dribbles_completed"}).text
-            dribble_attempted = row.find("td", {"data-stat": "dribbles"}).text
-            dribble_pct = row.find("td", {"data-stat": "dribbles_completed_pct"}).text
-            dribble_past = row.find("td", {"data-stat": "players_dribbled_past"}).text
-            dribble_meg = row.find("td", {"data-stat": "nutmegs"}).text
+
+            # take ons
+            dribble_attempt = row.find("td", {"data-stat": "take_ons"}).text
+            dribble_success = row.find("td", {"data-stat": "take_ons_won"}).text
+            dribble_success_pct = row.find("td", {"data-stat": "take_ons_won_pct"}).text
+            if dribble_success_pct == "":
+                dribble_success_pct = None
+            dribble_tackled = row.find("td", {"data-stat": "take_ons_tackled"}).text
+            dribble_tackled_pct = row.find(
+                "td", {"data-stat": "take_ons_tackled_pct"}
+            ).text
+
+            # carries
             carries = row.find("td", {"data-stat": "carries"}).text
-            carries_dist = row.find("td", {"data-stat": "carry_distance"}).text
-            carries_prg_dist = row.find(
-                "td", {"data-stat": "carry_progressive_distance"}
+            carries_total_distance = row.find(
+                "td", {"data-stat": "carries_distance"}
             ).text
-            carries_prg = row.find("td", {"data-stat": "progressive_carries"}).text
-            carries_final_third = row.find(
+            carries_progressive_distance = row.find(
+                "td", {"data-stat": "carries_progressive_distance"}
+            ).text
+            progressive_carries = row.find(
+                "td", {"data-stat": "progressive_carries"}
+            ).text
+            carries_into_final_third = row.find(
                 "td", {"data-stat": "carries_into_final_third"}
             ).text
-            carries_pa = row.find("td", {"data-stat": "carries_into_penalty_area"}).text
-            miscon = row.find("td", {"data-stat": "miscontrols"}).text
-            dispos = row.find("td", {"data-stat": "dispossessed"}).text
-            passes_targeted = row.find("td", {"data-stat": "pass_targets"}).text
-            passes_received = row.find("td", {"data-stat": "passes_received"}).text
-            passes_received_pct = row.find(
-                "td", {"data-stat": "passes_received_pct"}
+            carries_into_penalty_area = row.find(
+                "td", {"data-stat": "carries_into_penalty_area"}
             ).text
-            passes_received_prg = row.find(
+            miscontrols = row.find("td", {"data-stat": "miscontrols"}).text
+            dispossessed = row.find("td", {"data-stat": "dispossessed"}).text
+
+            # receiving
+            passes_received = row.find("td", {"data-stat": "passes_received"}).text
+            progressive_passes_received = row.find(
                 "td", {"data-stat": "progressive_passes_received"}
             ).text
 
             # generate dictionary for team
             mydict = {
-                "player_id": player_id,
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
                 "touches": touches,
-                "touches_defensive_pen": touches_def_pen,
-                "touches_defensive_third": touches_def,
-                "touches_middle_third": touches_mid,
-                "touches_attacking_third": touches_att,
-                "touches_attacking_pen": touches_att_pen,
+                "touches_def_pen_area": touches_def_pen_area,
+                "touches_def_3rd": touches_def_3rd,
+                "touches_mid_3rd": touches_mid_3rd,
+                "touches_att_3rd": touches_att_3rd,
+                "touches_att_pen_area": touches_att_pen_area,
                 "touches_live": touches_live,
-                "dribbles_successful": dribble_success,
-                "dribbles_attempted": dribble_attempted,
-                "dribble_pct": dribble_pct,
-                "dribbled_past": dribble_past,
-                "dribble_megs": dribble_meg,
+                "dribble_attempt": dribble_attempt,
+                "dribble_success": dribble_success,
+                "dribble_success_pct": dribble_success_pct,
+                "dribble_tackled": dribble_tackled,
+                "dribble_tackled_pct": dribble_tackled_pct,
                 "carries": carries,
-                "carry_distance": carries_dist,
-                "carry_progressive_distance": carries_prg_dist,
-                "carries_progressive": carries_prg,
-                "carries_into_final_third": carries_final_third,
-                "carries_into_penalty_area": carries_pa,
-                "miscontrols": miscon,
-                "dispossessed": dispos,
-                "passes_targeted": passes_targeted,
+                "carry_total_distance": carries_total_distance,
+                "carry_progressive_distance": carries_progressive_distance,
+                "progressive_carries": progressive_carries,
+                "carries_into_final_third": carries_into_final_third,
+                "carries_into_penalty_area": carries_into_penalty_area,
+                "miscontrols": miscontrols,
+                "dispossessed": dispossessed,
                 "passes_received": passes_received,
-                "passes_received_pct": passes_received_pct,
-                "passes_received_progressive": passes_received_prg,
+                "progressive_passes_received": progressive_passes_received,
             }
 
             # add to empty list
             mylist.append(mydict)
 
         # assign list to appropriate team
-        if team_id == id_x:
-            players_possession_stats_x = mylist.copy()
+        if side == "for":
+            possession_stats_for = mylist.copy()
         else:
-            players_possession_stats_y = mylist.copy()
+            possession_stats_against = mylist.copy()
 
-    return players_possession_stats_x, players_possession_stats_y
+    return possession_stats_for, possession_stats_against
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_shots.py` & `reus-1.1.1/reus/fbref/fb_match_shots.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from ..util import get_page_soup
 
 
 def fb_match_shots(pageSoup=None, url: str = None) -> list:
-    """Extracts shots for a given match that includes StatsBomb data
+    """Extracts shots for a given match that includes Opta data
 
     Args:
         pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
         url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
         list: shots for the match
@@ -17,76 +17,99 @@
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find shots object
     table = pageSoup.find("table", {"id": "shots_all"})
-    shots = table.find("tbody")
+    try:
+        shots = table.find("tbody")
+    except AttributeError:
+        return None
     shots = shots.find_all("tr")
 
     # generate empty list
     shotList = []
 
     # iterate through each shot and store attributes
     for row in shots:
+        # skip spacers
+        if row["class"][0] == "spacer":
+            continue
 
         # generate empty dictionary
         mydict = {}
 
-        # error handling for empty minutes
-        mins = row.find("th", {"data-stat": "minute"}).text
-        if mins == "":
-            continue
-
+        # general
+        minute = row.find("th", {"data-stat": "minute"}).text
+        if minute == "":
+            minute = None
         player_id = row.find("a", href=True)["href"].split("/")[3]
+        name = row.find("a", href=True).text
         team_id = (
             row.find("td", {"data-stat": "team"})
             .find("a", href=True)["href"]
             .split("/")[3]
         )
+        team_name = row.find("td", {"data-stat": "team"}).find("a", href=True).text
+        xG = row.find("td", {"data-stat": "xg_shot"}).text
+        if xG == "":
+            xG = None
+        psxg = row.find("td", {"data-stat": "psxg_shot"}).text
+        if psxg == "":
+            psxg = None
         outcome = row.find("td", {"data-stat": "outcome"}).text
         distance = row.find("td", {"data-stat": "distance"}).text
         body_part = row.find("td", {"data-stat": "body_part"}).text
         notes = row.find("td", {"data-stat": "notes"}).text
 
-        # error handling for no sca_player1
+        # sca 1
         try:
             sca_player1 = (
                 row.find("td", {"data-stat": "sca_1_player"})
                 .find("a", href=True)["href"]
                 .split("/")[3]
             )
+            sca_player1_name = row.find("td", {"data-stat": "sca_1_player"}).text
             sca_player1_event = row.find("td", {"data-stat": "sca_1_type"}).text
         except TypeError:
             sca_player1 = None
+            sca_player1_name = None
             sca_player1_event = None
 
-        # error handling for no sca_player2
+        # sca 2
         try:
             sca_player2 = (
                 row.find("td", {"data-stat": "sca_2_player"})
                 .find("a", href=True)["href"]
                 .split("/")[3]
             )
+            sca_player2_name = row.find("td", {"data-stat": "sca_2_player"}).text
             sca_player2_event = row.find("td", {"data-stat": "sca_2_type"}).text
         except TypeError:
             sca_player2 = None
+            sca_player2_name = None
             sca_player2_event = None
 
-        # generate dictionary for each shot
-        mydict["minute"] = mins
-        mydict["player"] = player_id
-        mydict["team_id"] = team_id
-        mydict["outcome"] = outcome
-        mydict["distance"] = distance
-        mydict["body_part"] = body_part
-        mydict["notes"] = notes
-        mydict["sca_player1"] = sca_player1
-        mydict["sca_player1_event"] = sca_player1_event
-        mydict["sca_player2"] = sca_player2
-        mydict["sca_player2_event"] = sca_player2_event
+        mydict = {
+            "minute": minute,
+            "player_id": player_id,
+            "name": name,
+            "team_id": team_id,
+            "team_name": team_name,
+            "xG": xG,
+            "psxg": psxg,
+            "outcome": outcome,
+            "distance": distance,
+            "body_part": body_part,
+            "notes": notes,
+            "sca_player1": sca_player1,
+            "sca_player1_name": sca_player1_name,
+            "sca_player1_event": sca_player1_event,
+            "sca_player2": sca_player2,
+            "sca_player2_name": sca_player2_name,
+            "sca_player2_event": sca_player2_event,
+        }
 
-        # append dictionary to list
         shotList.append(mydict)
 
     return shotList
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_summary.py` & `reus-1.1.1/reus/fbref/fb_match_summary.py`

 * *Files 10% similar despite different names*

```diff
@@ -68,32 +68,35 @@
                 score_y = int(score_y) - 1
                 score_pre = score_x + ":" + str(score_y)
         else:
             score_pre = score
 
         score_post = score
 
-        # extra primary and secondary (if applicable)
-        event_player1 = divs[3].find("a", href=True)["href"]
+        # extract primary and secondary (if applicable)
+        try:
+            event_player1 = divs[3].find("a", href=True)["href"]
+        except (AttributeError, TypeError):
+            continue
         if event in ["Goal (penalty)", "Own Goal", "Goal (shootout)"]:
             event_player2 = None
         else:
             try:
                 event_player2 = divs[3].find("small").find("a", href=True)["href"]
-            except AttributeError:
-                event_player2 = None
-            except TypeError:
+            except (AttributeError, TypeError):
                 event_player2 = None
 
         # generate dictionary for each event
-        mydict["team"] = team
-        mydict["minute"] = mins
-        mydict["event"] = event
-        mydict["score_pre"] = score_pre
-        mydict["score_post"] = score_post
-        mydict["player1"] = event_player1
-        mydict["player2"] = event_player2
+        mydict = {
+            "team": team,
+            "minute": mins,
+            "event": event,
+            "score_pre": score_pre,
+            "score_post": score_post,
+            "player1": event_player1,
+            "player2": event_player2,
+        }
 
         # append event dictionary to list
         eventList.append(mydict)
 
     return eventList
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_summary_stats.py` & `reus-1.1.1/reus/fbref/fb_match_summary_stats.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
 def fb_match_summary_stats(pageSoup=None, url: str = None) -> tuple:
-    """Extracts summary statistics for each player in a given match that includes StatsBomb data
+    """Extracts summary statistics for each player in a given match that includes advanced data
 
     Args:
         pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
         url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
         tuple: summary stats for home and away team players
@@ -19,15 +19,15 @@
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Get team ids
-    metadata = fb_match_metadata(pageSoup, verbose=False)[0]
+    metadata = fb_match_metadata(pageSoup)[0]
     id_x = metadata.get("id_x")
     id_y = metadata.get("id_y")
 
     # Loop through both teams
     for team_id in [id_x, id_y]:
         # generate empty list for each team
         mylist = []
@@ -37,61 +37,74 @@
         # find summary object
         stats_players = pageSoup.find("table", {"id": id_})
         stats_players = stats_players.find_all("tr")
 
         # iterate through each player and store metrics
         for row in stats_players[2:-1]:
             th = row.find("th")
+
+            # general
             try:
+                name = th.text.replace("\xa0", "")
+            except AttributeError:
                 name = th["csk"]
-            except KeyError:
-                name = th.text
             player_id = th.find("a", href=True)["href"].split("/")[3]
 
             shirtnumber = row.find("td", {"data-stat": "shirtnumber"}).text
             nation = row.find("td", {"data-stat": "nationality"}).text
             position = row.find("td", {"data-stat": "position"}).text
             age = row.find("td", {"data-stat": "age"}).text.split("-")
             try:
                 age = int(age[0]) + int(age[1]) / 365
             except ValueError:
                 age = None
             minutes = row.find("td", {"data-stat": "minutes"}).text
+
+            # performance
             goals = row.find("td", {"data-stat": "goals"}).text
             assists = row.find("td", {"data-stat": "assists"}).text
             pk = row.find("td", {"data-stat": "pens_made"}).text
             pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
-            shots = row.find("td", {"data-stat": "shots_total"}).text
+            shots = row.find("td", {"data-stat": "shots"}).text
             shots_on_target = row.find("td", {"data-stat": "shots_on_target"}).text
             card_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
             card_red = row.find("td", {"data-stat": "cards_red"}).text
             touches = row.find("td", {"data-stat": "touches"}).text
-            pressures = row.find("td", {"data-stat": "pressures"}).text
             tackles = row.find("td", {"data-stat": "tackles"}).text
             interceptions = row.find("td", {"data-stat": "interceptions"}).text
             blocks = row.find("td", {"data-stat": "blocks"}).text
+
+            # expected
             xG = row.find("td", {"data-stat": "xg"}).text
             npxG = row.find("td", {"data-stat": "npxg"}).text
-            xA = row.find("td", {"data-stat": "xa"}).text
+            xA = row.find("td", {"data-stat": "xg_assist"}).text
+
+            # sca
             shot_creating_actions = row.find("td", {"data-stat": "sca"}).text
             goal_creating_actions = row.find("td", {"data-stat": "gca"}).text
+
+            # passes
             passes_completed = row.find("td", {"data-stat": "passes_completed"}).text
             passes_attempted = row.find("td", {"data-stat": "passes"}).text
             pass_accuracy = row.find("td", {"data-stat": "passes_pct"}).text
-            pass_progressive_distance = row.find(
+            progressive_passes = row.find(
                 "td", {"data-stat": "progressive_passes"}
             ).text
+
+            # carries
             carries = row.find("td", {"data-stat": "carries"}).text
-            dribble_progressive_distance = row.find(
+            progressive_carries = row.find(
                 "td", {"data-stat": "progressive_carries"}
             ).text
-            dribble_success = row.find("td", {"data-stat": "dribbles_completed"}).text
-            dribble_attempt = row.find("td", {"data-stat": "dribbles"}).text
 
-            # generate dictionary for team
+            # take ons
+            dribble_success = row.find("td", {"data-stat": "take_ons_won"}).text
+            dribble_attempt = row.find("td", {"data-stat": "take_ons"}).text
+
+            # generate dictionary for player
             mydict = {
                 "player_id": player_id,
                 "name": name,
                 "shirtnumber": shirtnumber,
                 "nation": nation,
                 "position": position,
                 "age": age,
@@ -101,34 +114,33 @@
                 "pk": pk,
                 "pk_attempted": pk_attempted,
                 "shots": shots,
                 "shots_on_target": shots_on_target,
                 "card_yellow": card_yellow,
                 "card_red": card_red,
                 "touches": touches,
-                "pressures": pressures,
                 "tackles": tackles,
                 "interceptions": interceptions,
                 "blocks": blocks,
                 "xG": xG,
                 "npxG": npxG,
                 "xA": xA,
                 "shot_creating_actions": shot_creating_actions,
                 "goal_creating_actions": goal_creating_actions,
                 "passes_completed": passes_completed,
                 "passes_attempted": passes_attempted,
-                "passes_accuracy": pass_accuracy,
-                "pass_progressive_distance": pass_progressive_distance,
+                "pass_accuracy": pass_accuracy,
+                "progressive_passes": progressive_passes,
                 "carries": carries,
-                "dribble_progressive_distance": dribble_progressive_distance,
+                "progressive_carries": progressive_carries,
                 "dribble_success": dribble_success,
                 "dribble_attempt": dribble_attempt,
             }
 
-            # add to empty list
+            # add to team list
             mylist.append(mydict)
 
         # assign list to appropriate team
         if team_id == id_x:
             players_summary_stats_x = mylist.copy()
         else:
             players_summary_stats_y = mylist.copy()
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_team_stats.py` & `reus-1.1.1/reus/fbref/fb_match_team_stats.py`

 * *Files 19% similar despite different names*

```diff
@@ -19,79 +19,125 @@
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find team stats object
     stats = pageSoup.find("div", {"id": "team_stats"})
     statsTable = stats.find("table").find_all("tr")
 
-    # Error handling for missing metrics
-    try:
-        possession = statsTable[2].find_all("strong")
-        possession_x = int(possession[0].text.replace("%", "")) / 100
-        possession_y = int(possession[1].text.replace("%", "")) / 100
-    except IndexError:
-        possession_x = possession_y = None
-
-    try:
-        passing = statsTable[4].find_all("div")
-        passing_x = passing[0].find_all("div")[0].text.split()
-        passing_completed_x = passing_x[0]
-        passing_attempted_x = passing_x[2]
-        passing_accuracy_x = int(passing_x[4].replace("%", "")) / 100
-        passing_y = passing[5].find_all("div")[0].text.split()
-        passing_accuracy_y = int(passing_y[0].replace("%", "")) / 100
-        passing_completed_y = passing_y[2]
-        passing_attempted_y = passing_y[4]
-    except IndexError:
-        passing_completed_x = passing_completed_y = None
-        passing_attempted_x = passing_attempted_y = None
-        passing_accuracy_x = passing_accuracy_y = None
-
-    try:
-        shots = statsTable[6].find_all("div")
-        shots_x = shots[0].find_all("div")[0].text.split()
-        shots_target_x = shots_x[0]
-        shots_taken_x = shots_x[2]
-        shots_accuracy_x = (
-            int(shots_x[4].replace("%", "")) / 100 if shots_x[4] != "%" else None
-        )
-        shots_y = shots[5].find_all("div")[0].text.split()
-        shots_accuracy_y = (
-            int(shots_y[0].replace("%", "")) / 100 if shots_y[0] != "%" else None
-        )
-        shots_target_y = shots_y[2]
-        shots_taken_y = shots_y[4]
-    except IndexError:
-        shots_target_x = shots_target_y = None
-        shots_taken_x = shots_taken_y = None
-        shots_accuracy_x = shots_accuracy_y = None
-
-    try:
-        saves = statsTable[8].find_all("div")
-        saves_x = saves[0].find_all("div")[0].text.split()
-        saves_completed_x = saves_x[0]
-        saves_attempted_x = saves_x[2]
-        saves_rate_x = (
-            int(saves_x[4].replace("%", "")) / 100 if saves_x[4] != "%" else None
-        )
-        saves_y = saves[5].find_all("div")[0].text.split()
-        saves_rate_y = (
-            int(saves_y[0].replace("%", "")) / 100 if saves_y[0] != "%" else None
-        )
-        saves_completed_y = saves_y[2]
-        saves_attempted_y = saves_y[4]
-    except IndexError:
-        saves_completed_x = saves_completed_y = None
-        saves_attempted_x = saves_attempted_y = None
-        saves_rate_x = saves_rate_y = None
+    # Baseline stats
+    possession_x = None
+    possession_y = None
+    passes_completed_x = None
+    passes_attempted_x = None
+    passing_accuracy_x = None
+    passes_completed_y = None
+    passes_attempted_y = None
+    passing_accuracy_y = None
+    shots_target_x = None
+    shots_taken_x = None
+    shot_accuracy_x = None
+    shots_target_y = None
+    shots_taken_y = None
+    shot_accuracy_y = None
+    saves_x = None
+    saves_attempted_x = None
+    save_rate_x = None
+    saves_y = None
+    saves_attempted_y = None
+    save_rate_y = None
+    yellow_cards_x = None
+    red_cards_x = None
+    yellow_cards_y = None
+    red_cards_y = None
+
+    currentStat = None
+    for i in statsTable[1:]:
+        if i.text == "Possession":
+            currentStat = "possession"
+            continue
+        elif i.text == "Passing Accuracy":
+            currentStat = "passing"
+            continue
+        elif i.text == "Shots on Target":
+            currentStat = "shooting"
+            continue
+        elif i.text == "Saves":
+            currentStat = "saves"
+            continue
+        elif i.text == "Cards":
+            currentStat = "cards"
+            continue
+
+        if currentStat == "possession":
+            possession = i.find_all("strong")
+            possession_x = possession[0].text.replace("%", "")
+            possession_y = possession[1].text.replace("%", "")
+            currentStat = None
+            continue
+        elif currentStat == "passing":
+            passing = i.find_all("div")
+            passing_x = passing[0].find_all("div")[0].text.split()
+            passes_completed_x = passing_x[0]
+            passes_attempted_x = passing_x[2]
+            passing_accuracy_x = passing_x[4].replace("%", "")
+            passing_y = passing[5].find_all("div")[0].text.split()
+            passing_accuracy_y = passing_y[0].replace("%", "")
+            passes_completed_y = passing_y[2]
+            passes_attempted_y = passing_y[4]
+            currentStat = None
+            continue
+        elif currentStat == "shooting":
+            shooting = i.find_all("div")
+            shooting_x = shooting[0].find_all("div")[0].text.split()
+            shots_target_x = shooting_x[0]
+            shots_taken_x = shooting_x[2]
+            shot_accuracy_x = shooting_x[4].replace("%", "")
+            shooting_y = shooting[5].find_all("div")[0].text.split()
+            shot_accuracy_y = shooting_y[0].replace("%", "")
+            shots_target_y = shooting_y[2]
+            shots_taken_y = shooting_y[4]
+            currentStat = None
+            continue
+        elif currentStat == "saves":
+            goalkeeping = i.find_all("div")
+            goalkeeping_x = goalkeeping[0].find_all("div")[0].text.split()
+            if goalkeeping_x[0] == "of":
+                saves_x = "0"
+                saves_attempted_x = goalkeeping_x[1]
+                save_rate_x = "0"
+            else:
+                saves_x = goalkeeping_x[0]
+                saves_attempted_x = goalkeeping_x[2]
+                save_rate_x = goalkeeping_x[4].replace("%", "")
+            goalkeeping_y = goalkeeping[5].find_all("div")[0].text.split()
+            if goalkeeping_y[2] == "of":
+                saves_y = "0"
+                saves_attempted_y = goalkeeping_y[3]
+                save_rate_y = "0"
+            else:
+                saves_y = goalkeeping_y[2]
+                saves_attempted_y = goalkeeping_y[4]
+                save_rate_y = goalkeeping_y[0].replace("%", "")
+            currentStat = None
+            continue
+        elif currentStat == "cards":
+            cards = i.find_all("div")
+            cards_x = cards[0]
+            yellow_cards_x = len(cards_x.find_all("span", {"class": "yellow_card"}))
+            red_cards_x = len(cards_x.find_all("span", {"class": "red_card"}))
+            cards_y = cards[5]
+            yellow_cards_y = len(cards_y.find_all("span", {"class": "yellow_card"}))
+            red_cards_y = len(cards_y.find_all("span", {"class": "red_card"}))
+            currentStat = None
+            continue
 
+    # Extra stats
     extra = pageSoup.find("div", {"id": "team_stats_extra"})
     extraTable = extra.find_all("div")
 
-    # Error handling for missing statistics
     fouls_x = fouls_y = None
     corners_x = corners_y = None
     crosses_x = crosses_y = None
     touches_x = touches_y = None
     tackles_x = tackles_y = None
     interceptions_x = interceptions_y = None
     aerials_won_x = aerials_won_y = None
@@ -139,32 +185,36 @@
             long_balls_x = div.findPrevious("div").text
             long_balls_y = div.findNext("div").text
 
     # generate dictionary
     mydict = {
         "possession_x": possession_x,
         "possession_y": possession_y,
-        "passes_completed_x": passing_completed_x,
-        "passes_attempted_x": passing_attempted_x,
+        "passes_completed_x": passes_completed_x,
+        "passes_attempted_x": passes_attempted_x,
         "passing_accuracy_x": passing_accuracy_x,
-        "passes_completed_y": passing_completed_y,
-        "passes_attempted_y": passing_attempted_y,
+        "passes_completed_y": passes_completed_y,
+        "passes_attempted_y": passes_attempted_y,
         "passing_accuracy_y": passing_accuracy_y,
         "shots_on_target_x": shots_target_x,
         "shots_taken_x": shots_taken_x,
-        "shot_accuracy_x": shots_accuracy_x,
+        "shot_accuracy_x": shot_accuracy_x,
         "shots_on_target_y": shots_target_y,
         "shots_taken_y": shots_taken_y,
-        "shot_accuracy_y": shots_accuracy_y,
-        "saves_x": saves_completed_x,
+        "shot_accuracy_y": shot_accuracy_y,
+        "saves_x": saves_x,
         "shots_faced_x": saves_attempted_x,
-        "save_rate_x": saves_rate_x,
-        "saves_y": saves_completed_y,
+        "save_rate_x": save_rate_x,
+        "saves_y": saves_y,
         "shots_faced_y": saves_attempted_y,
-        "save_rate_y": saves_rate_y,
+        "save_rate_y": save_rate_y,
+        "yellow_cards_x": yellow_cards_x,
+        "red_cards_x": red_cards_x,
+        "yellow_cards_y": yellow_cards_y,
+        "red_cards_y": red_cards_y,
         "fouls_x": fouls_x,
         "fouls_y": fouls_y,
         "corners_x": corners_x,
         "corners_y": corners_y,
         "crosses_x": crosses_x,
         "crosses_y": crosses_y,
         "touches_x": touches_x,
```

### Comparing `reus-1.1.0/reus/fbref/fb_match_urls.py` & `reus-1.1.1/reus/fbref/fb_match_urls.py`

 * *Files identical despite different names*

### Comparing `reus-1.1.0/reus/fbref/fb_season_fixture_urls.py` & `reus-1.1.1/reus/fbref/fb_season_urls.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,34 +1,34 @@
 import pandas as pd
 
 
-def fb_season_fixture_urls(
+def fb_season_urls(
     competition_type: str = None,
     competition_name: str = None,
     country: str = None,
     gender: str = None,
     governing_body: str = None,
     tier: str = None,
     season_end_year: int = None,
-    stats_bomb: str = None,
+    advanced: str = None,
 ) -> pd.Series:
-    """Returns a series of urls for fixture section of a season
+    """Returns a series of urls for overview section of a season
 
     Args:
         competition_type (str or list, optional): type of competition. Defaults to None.
         competition_name (str or list, optional): name of competition. Defaults to None.
         country (str or list, optional): country of competition. Defaults to None.
         gender (str or list, optional): gender of competition. Defaults to None.
         governing_body (str or list, optional): governing body of competition. Defaults to None.
         tier (str or list, optional): tier of competition. Defaults to None.
         season_end_year (int or list, optional): year at end of competition. Defaults to None.
-        stats_bomb (str or list, optional): flag for if statsbomb data is available. Defaults to None.
+        advanced (str or list, optional): flag for if advanced data is available. Defaults to None.
 
     Returns:
-        series: season fixture urls
+        series: season urls
     """
 
     df = pd.read_csv(
         "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/all_competitions.csv",
         keep_default_na=False,
     )
 
@@ -84,16 +84,16 @@
     if season_end_year is None:
         season_end_year = df.season_end_year.unique()
     elif not isinstance(season_end_year, list):
         season_end_year = [season_end_year]
 
     df = df[df.season_end_year.isin(season_end_year)]
 
-    # Stats bomb
-    if stats_bomb is None:
-        stats_bomb = df.stats_bomb.unique()
-    elif not isinstance(stats_bomb, list):
-        stats_bomb = [stats_bomb]
+    # Advanced stats
+    if advanced is None:
+        advanced = df.advanced.unique()
+    elif not isinstance(advanced, list):
+        advanced = [advanced]
 
-    df = df[df.stats_bomb.isin(stats_bomb)]
+    df = df[df.advanced.isin(advanced)]
 
-    return df["fixtures_url"]
+    return df["seasons_urls"]
```

### Comparing `reus-1.1.0/reus/fbref/fb_season_urls.py` & `reus-1.1.1/reus/fbref/fb_season_fixture_urls.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,34 +1,34 @@
 import pandas as pd
 
 
-def fb_season_urls(
+def fb_season_fixture_urls(
     competition_type: str = None,
     competition_name: str = None,
     country: str = None,
     gender: str = None,
     governing_body: str = None,
     tier: str = None,
-    season_end_year: str = None,
-    stats_bomb: str = None,
+    season_end_year: int = None,
+    advanced: str = None,
 ) -> pd.Series:
-    """Returns a series of urls for overview section of a season
+    """Returns a series of urls for fixture section of a season
 
     Args:
         competition_type (str or list, optional): type of competition. Defaults to None.
         competition_name (str or list, optional): name of competition. Defaults to None.
         country (str or list, optional): country of competition. Defaults to None.
         gender (str or list, optional): gender of competition. Defaults to None.
         governing_body (str or list, optional): governing body of competition. Defaults to None.
         tier (str or list, optional): tier of competition. Defaults to None.
-        season_end_year (str or list, optional): year at end of competition. Defaults to None.
-        stats_bomb (str or list, optional): flag for if statsbomb data is available. Defaults to None.
+        season_end_year (int or list, optional): year at end of competition. Defaults to None.
+        advanced (str or list, optional): flag for if advanced data is available. Defaults to None.
 
     Returns:
-        series: season urls
+        series: season fixture urls
     """
 
     df = pd.read_csv(
         "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/all_competitions.csv",
         keep_default_na=False,
     )
 
@@ -84,16 +84,16 @@
     if season_end_year is None:
         season_end_year = df.season_end_year.unique()
     elif not isinstance(season_end_year, list):
         season_end_year = [season_end_year]
 
     df = df[df.season_end_year.isin(season_end_year)]
 
-    # Stats bomb
-    if stats_bomb is None:
-        stats_bomb = df.stats_bomb.unique()
-    elif not isinstance(stats_bomb, list):
-        stats_bomb = [stats_bomb]
+    # Advanced stats
+    if advanced is None:
+        advanced = df.advanced.unique()
+    elif not isinstance(advanced, list):
+        advanced = [advanced]
 
-    df = df[df.stats_bomb.isin(stats_bomb)]
+    df = df[df.advanced.isin(advanced)]
 
-    return df["seasons_urls"]
+    return df["fixtures_url"]
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_advanced_keeper_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_summary_stats.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,137 +1,140 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_advanced_keeper_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts advanced keeper stats for each player in a given team
+def fb_team_player_summary_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts summary stats for each player in a given team
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: goalkeeper stats for each player
+        list: summary stats for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_keeper_adv"})
-    if div is None:
-        return None
-
-    table = div.find("table")
+    table = pageSoup.find("table")
     tbody = table.find("tbody")
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
+        except ValueError:
+            age = None
+        minutes = row.find("td", {"data-stat": "minutes"}).text
         minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
 
-        goals_allowed = row.find("td", {"data-stat": "goals_against_gk"}).text
-        pk_allowed = row.find("td", {"data-stat": "pens_allowed"}).text
-        fk_allowed = row.find("td", {"data-stat": "free_kick_goals_against_gk"}).text
-        corner_allowed = row.find(
-            "td", {"data-stat": "corner_kick_goals_against_gk"}
-        ).text
-        own_goals = row.find("td", {"data-stat": "own_goals_against_gk"}).text
-
-        psxg = row.find("td", {"data-stat": "psxg_gk"}).text
-        psxg_per_sot = row.find(
-            "td", {"data-stat": "psnpxg_per_shot_on_target_against"}
-        ).text
-        psxg_g = row.find("td", {"data-stat": "psxg_net_gk"}).text
-        psxg_g_p90 = row.find("td", {"data-stat": "psxg_net_per90_gk"}).text
-
-        launched_completed = row.find(
-            "td", {"data-stat": "passes_completed_launched_gk"}
-        ).text
-        launched_attempted = row.find("td", {"data-stat": "passes_launched_gk"}).text
-        launched_acc = row.find("td", {"data-stat": "passes_pct_launched_gk"}).text
-
-        passes_attempted = row.find("td", {"data-stat": "passes_gk"}).text
-        throws_attempted = row.find("td", {"data-stat": "passes_throws_gk"}).text
-        pct_lauched = row.find("td", {"data-stat": "pct_passes_launched_gk"}).text
-        passes_avg_length = row.find("td", {"data-stat": "passes_length_avg_gk"}).text
-
-        gk_attempted = row.find("td", {"data-stat": "goal_kicks"}).text
-        gk_pct_launched = row.find("td", {"data-stat": "pct_goal_kicks_launched"}).text
-        gk_avg_length = row.find("td", {"data-stat": "goal_kick_length_avg"}).text
-
-        crosses_faced = row.find("td", {"data-stat": "crosses_gk"}).text
-        crosses_stopped = row.find("td", {"data-stat": "crosses_stopped_gk"}).text
-        crosses_stopped_pct = row.find(
-            "td", {"data-stat": "crosses_stopped_pct_gk"}
-        ).text
-
-        defensive_actions = row.find(
-            "td", {"data-stat": "def_actions_outside_pen_area_gk"}
-        ).text
-        defensive_actions_p90 = row.find(
-            "td", {"data-stat": "def_actions_outside_pen_area_per90_gk"}
-        ).text
-        defensive_actions_avg_distance = row.find(
-            "td", {"data-stat": "avg_distance_def_actions_gk"}
-        ).text
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
+        # performance
+        goals = row.find("td", {"data-stat": "goals"}).text
+        assists = row.find("td", {"data-stat": "assists"}).text
+        g_a = row.find("td", {"data-stat": "goals_assists"}).text
+        npg = row.find("td", {"data-stat": "goals_pens"}).text
+        pk = row.find("td", {"data-stat": "pens_made"}).text
+        pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
+        card_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
+        card_red = row.find("td", {"data-stat": "cards_red"}).text
+
+        # expected
+        try:
+            xG = row.find("td", {"data-stat": "xg"}).text
+            npxG = row.find("td", {"data-stat": "npxg"}).text
+            xAG = row.find("td", {"data-stat": "xg_assist"}).text
+            npxg_xga = row.find("td", {"data-stat": "npxg_xg_assist"}).text
+        except AttributeError:
+            xG = npxG = xAG = npxg_xga
+
+        # progression
+        progressive_carries = row.find("td", {"data-stat": "progressive_carries"}).text
+        progressive_passes = row.find("td", {"data-stat": "progressive_passes"}).text
+        progressive_passes_received = row.find(
+            "td", {"data-stat": "progressive_passes_received"}
+        ).text
+
+        # performance per 90 minutes
+        goalp90 = row.find("td", {"data-stat": "goals_per90"}).text
+        assistsp90 = row.find("td", {"data-stat": "assists_per90"}).text
+        g_ap90 = row.find("td", {"data-stat": "goals_assists_per90"}).text
+        npgp90 = row.find("td", {"data-stat": "goals_pens_per90"}).text
+        npg_ap90 = row.find("td", {"data-stat": "goals_assists_pens_per90"}).text
+
+        # expected per 90 minutes
+        try:
+            xGp90 = row.find("td", {"data-stat": "xg_per90"}).text
+            xAGp90 = row.find("td", {"data-stat": "xg_assist_per90"}).text
+            xG_xAGp90 = row.find("td", {"data-stat": "xg_xg_assist_per90"}).text
+            npxGp90 = row.find("td", {"data-stat": "npxg_per90"}).text
+            npxG_xAGp90 = row.find("td", {"data-stat": "npxg_xg_assist_per90"}).text
+        except AttributeError:
+            xGp90 = xAGp90 = xG_xAGp90 = npxGp90 = npxG_xAGp90 = None
+
+        # match logs
+        try:
+            match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
+                "href"
+            ]
+        except TypeError:
+            match_logs = None
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
+            "minutes": minutes,
             "90s": minutes_90,
-            "goals_allowed": goals_allowed,
-            "pk_allowed": pk_allowed,
-            "fk_allowed": fk_allowed,
-            "corner_allowed": corner_allowed,
-            "own_goals": own_goals,
-            "psxg": psxg,
-            "psxg_per_shot_on_target": psxg_per_sot,
-            "psxg_minus_ga": psxg_g,
-            "psxg_minus_ga_p90": psxg_g_p90,
-            "launched_completed": launched_completed,
-            "launched_attempted": launched_attempted,
-            "launched_accuracy": launched_acc,
-            "passes_attempted": passes_attempted,
-            "throws_attempted": throws_attempted,
-            "pct_launched": pct_lauched,
-            "passes_avg_length": passes_avg_length,
-            "gk_attempted": gk_attempted,
-            "gk_pct_launched": gk_pct_launched,
-            "gk_avg_length": gk_avg_length,
-            "crosses_faced": crosses_faced,
-            "crosses_stopped": crosses_stopped,
-            "crosses_stopped_pct": crosses_stopped_pct,
-            "defensive_actions": defensive_actions,
-            "defensive_actions_p90": defensive_actions_p90,
-            "defensive_actions_avg_distance": defensive_actions_avg_distance,
+            "goals": goals,
+            "assists": assists,
+            "goals+assists": g_a,
+            "npg": npg,
+            "pk": pk,
+            "pk_attempted": pk_attempted,
+            "card_yellow": card_yellow,
+            "card_red": card_red,
+            "xG": xG,
+            "npxG": npxG,
+            "xAG": xAG,
+            "npxG+xA": npxg_xga,
+            "progressive_carries": progressive_carries,
+            "progressive_passes": progressive_passes,
+            "progressive_passes_received": progressive_passes_received,
+            "goals_p90": goalp90,
+            "assists_p90": assistsp90,
+            "goals+assists_p90": g_ap90,
+            "npg_p90": npgp90,
+            "npg+assists_p90": npg_ap90,
+            "xG_p90": xGp90,
+            "xAG_p90": xAGp90,
+            "xG+xAGp90": xG_xAGp90,
+            "npxG_p90": npxGp90,
+            "npxG+xAG_p90": npxG_xAGp90,
             "match_logs": match_logs,
         }
 
         # add to empty list
         mylist.append(mydict)
 
     return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_data.py` & `reus-1.1.1/reus/fbref/fb_team_player_data.py`

 * *Files 15% similar despite different names*

```diff
@@ -9,22 +9,24 @@
 from .fb_team_player_goal_sca_stats import fb_team_player_goal_sca_stats
 from .fb_team_player_defensive_actions_stats import (
     fb_team_player_defensive_actions_stats,
 )
 from .fb_team_player_possession_stats import fb_team_player_possession_stats
 from .fb_team_player_playing_time_stats import fb_team_player_playing_time_stats
 from .fb_team_player_misc_stats import fb_team_player_misc_stats
+from bs4 import BeautifulSoup
 
 
-def fb_team_player_data(url: str) -> tuple:
-    """Extracts statistics of each player for a given team. This includes summary, passing,
+def fb_team_player_data(url: str, html_file: BeautifulSoup = None) -> tuple:
+    """Extracts statistics of each player for a given team. This includes summary, shooting, passing,
     defensive, possession, possession, playing time, and goalkeeping stats
 
     Args:
         url (str): path of fbref team page
+        html_file (BeautifulSoup, optional): pageSoup html file. Defaults to None.
 
     Returns:
         tuple: player stats
             list: summary stats of players
             list: goalkeeping stats of players
             list: advanced goalkeeping stats of players
             list: shooting stats of players
@@ -34,16 +36,19 @@
             list: defensive stats of players
             list: possession stats of players
             list: playing time stats of players
             list: miscellaneous stats of players
 
     """
 
-    page = "https://fbref.com" + url
-    pageSoup = get_page_soup(page)
+    if html_file is None:
+        page = "https://fbref.com" + url
+        pageSoup = get_page_soup(page)
+    else:
+        pageSoup = html_file
 
     summary_stats = fb_team_player_summary_stats(pageSoup)
     keeper_stats = fb_team_player_keeper_stats(pageSoup)
     advanced_keeper_stats = fb_team_player_advanced_keeper_stats(pageSoup)
     shooting_stats = fb_team_player_shooting_stats(pageSoup)
     passing_stats = fb_team_player_passing_stats(pageSoup)
     passing_type_stats = fb_team_player_passing_type_stats(pageSoup)
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_defensive_actions_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_shooting_stats.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,117 +1,114 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_defensive_actions_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts defensive action stats for each player in a given team
+def fb_team_player_shooting_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts shooting stats for each player in a given team
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
-        url (str, optional): path of fbref team page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
+        url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
-        list: defensive stats for each player
+        list: shooting stats for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_defense"})
-    if div is None:
-        return None
-
+    div = pageSoup.find("div", {"id": "all_stats_shooting"})
     table = div.find("table")
     tbody = table.find("tbody")
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
+        except ValueError:
+            age = None
         minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
 
-        tkl = row.find("td", {"data-stat": "tackles"}).text
-        tklW = row.find("td", {"data-stat": "tackles_won"}).text
-        tkl_def = row.find("td", {"data-stat": "tackles_def_3rd"}).text
-        tkl_mid = row.find("td", {"data-stat": "tackles_mid_3rd"}).text
-        tkl_att = row.find("td", {"data-stat": "tackles_att_3rd"}).text
-
-        drb_tkl = row.find("td", {"data-stat": "dribble_tackles"}).text
-        drb_att = row.find("td", {"data-stat": "dribbles_vs"}).text
-        drb_pct = row.find("td", {"data-stat": "dribble_tackles_pct"}).text
-        drb_past = row.find("td", {"data-stat": "dribbled_past"}).text
-
-        press = row.find("td", {"data-stat": "pressures"}).text
-        press_succ = row.find("td", {"data-stat": "pressure_regains"}).text
-        press_pct = row.find("td", {"data-stat": "pressure_regain_pct"}).text
-        press_def = row.find("td", {"data-stat": "pressures_def_3rd"}).text
-        press_mid = row.find("td", {"data-stat": "pressures_mid_3rd"}).text
-        press_att = row.find("td", {"data-stat": "pressures_att_3rd"}).text
-
-        blk = row.find("td", {"data-stat": "blocks"}).text
-        blk_shots = row.find("td", {"data-stat": "blocked_shots"}).text
-        blk_sv = row.find("td", {"data-stat": "blocked_shots_saves"}).text
-        blk_pass = row.find("td", {"data-stat": "blocked_passes"}).text
-
-        interceptions = row.find("td", {"data-stat": "interceptions"}).text
-        tkl_int = row.find("td", {"data-stat": "tackles_interceptions"}).text
-        clr = row.find("td", {"data-stat": "clearances"}).text
-        err = row.find("td", {"data-stat": "errors"}).text
+        # standard
+        goals = row.find("td", {"data-stat": "goals"}).text
+        shots = row.find("td", {"data-stat": "shots"}).text
+        shots_on_target = row.find("td", {"data-stat": "shots_on_target"}).text
+        shots_on_target_per = row.find("td", {"data-stat": "shots_on_target_pct"}).text
+        shots_p90 = row.find("td", {"data-stat": "shots_per90"}).text
+        shots_on_target_p90 = row.find(
+            "td", {"data-stat": "shots_on_target_per90"}
+        ).text
+        goals_per_shot = row.find("td", {"data-stat": "goals_per_shot"}).text
+        goals_per_sot = row.find("td", {"data-stat": "goals_per_shot_on_target"}).text
+        try:
+            dist = row.find("td", {"data-stat": "average_shot_distance"}).text
+            fk = row.find("td", {"data-stat": "shots_free_kicks"}).text
+        except AttributeError:
+            dist = fk = None
+        pk = row.find("td", {"data-stat": "pens_made"}).text
+        pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
+
+        # expected
+        try:
+            xG = row.find("td", {"data-stat": "xg"}).text
+            npxG = row.find("td", {"data-stat": "npxg"}).text
+            npxG_per_shot = row.find("td", {"data-stat": "npxg_per_shot"}).text
+            goals_xG = row.find("td", {"data-stat": "xg_net"}).text
+            npg_xG = row.find("td", {"data-stat": "npxg_net"}).text
+        except AttributeError:
+            xG = npxG = npxG_per_shot = goals_xG = npg_xG = None
 
+        # match logs
         match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
             "href"
         ]
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
             "90s": minutes_90,
-            "tackles": tkl,
-            "tackles_won": tklW,
-            "tackles_defensive_third": tkl_def,
-            "tackles_middle_third": tkl_mid,
-            "tackles_attacking_third": tkl_att,
-            "dribble_tackles": drb_tkl,
-            "dribble_tackles_attempted": drb_att,
-            "dribble_pct": drb_pct,
-            "dribbled_past": drb_past,
-            "pressures": press,
-            "pressures_successful": press_succ,
-            "pressure_pct": press_pct,
-            "pressures_defensive_third": press_def,
-            "pressures_middle_third": press_mid,
-            "pressures_attacking_third": press_att,
-            "blocks": blk,
-            "blocked_shots": blk_shots,
-            "blocked_shots_on_target": blk_sv,
-            "blocked_passes": blk_pass,
-            "interceptions": interceptions,
-            "tkl_int": tkl_int,
-            "clearances": clr,
-            "errors": err,
+            "goals": goals,
+            "shots": shots,
+            "shots_on_target": shots_on_target,
+            "shots_on_target%": shots_on_target_per,
+            "shots_p90": shots_p90,
+            "shots_on_target_p90": shots_on_target_p90,
+            "goals_per_shot": goals_per_shot,
+            "goals_per_shot_on_target": goals_per_sot,
+            "avg_distance": dist,
+            "free_kicks": fk,
+            "pk": pk,
+            "pk_attempted": pk_attempted,
+            "xG": xG,
+            "npxG": npxG,
+            "npxG_per_shot": npxG_per_shot,
+            "goals_minus_xG": goals_xG,
+            "npg_minus_xG": npg_xG,
             "match_logs": match_logs,
         }
 
         # add to empty list
         mylist.append(mydict)
 
     return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_goal_sca_stats.py` & `reus-1.1.1/reus/fbref/fb_team_goal_sca_stats.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,102 +1,100 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_goal_sca_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts shot and goal creating actions for each player in a given team
+def fb_team_goal_sca_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts shot and goal creating actions stats for each team in a given league
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: shot and goal creating actions for each player
+        tuple: possession stats for home and away team players
+            list: shot and goal creating stats for each team
+            list: shot and goal creating stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_gca"})
-    if div is None:
-        return None
-
-    table = div.find("table")
-    tbody = table.find("tbody")
-    rows = tbody.find_all("tr")
-
-    # Generate empty list
-    mylist = []
-
-    # iterate through each player and store attributes
-    for row in rows:
-        th = row.find("th")
-        name = th["csk"]
-        player_id = th.find("a", href=True)["href"].split("/")[3]
-        nation = row.find("td", {"data-stat": "nationality"}).text
-        position = row.find("td", {"data-stat": "position"}).text
-        age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
-            age = int(age[0]) + int(age[1]) / 365
+    for side in ["for", "against"]:
+        # generate empty list for each team
+        mylist = []
+        # generate html id
+        id_ = "stats_squads_gca_" + side
+
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
+
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
+            th = row.find("th")
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+            matches = row.find("td", {"data-stat": "minutes_90s"}).text
+
+            # sca
+            shot_creating_actions = row.find("td", {"data-stat": "sca"}).text
+            shot_creating_actions_p90 = row.find("td", {"data-stat": "sca_per90"}).text
+
+            # sca types
+            sca_pass_live = row.find("td", {"data-stat": "sca_passes_live"}).text
+            sca_pass_dead = row.find("td", {"data-stat": "sca_passes_dead"}).text
+            sca_take_on = row.find("td", {"data-stat": "sca_take_ons"}).text
+            sca_shot = row.find("td", {"data-stat": "sca_shots"}).text
+            sca_foul = row.find("td", {"data-stat": "sca_fouled"}).text
+            sca_defense = row.find("td", {"data-stat": "sca_defense"}).text
+
+            # gca
+            goal_creating_actions = row.find("td", {"data-stat": "gca"}).text
+            goal_creating_actions_p90 = row.find("td", {"data-stat": "gca_per90"}).text
+
+            # gca types
+            gca_pass_live = row.find("td", {"data-stat": "gca_passes_live"}).text
+            gca_pass_dead = row.find("td", {"data-stat": "gca_passes_dead"}).text
+            gca_take_on = row.find("td", {"data-stat": "gca_take_ons"}).text
+            gca_shot = row.find("td", {"data-stat": "gca_shots"}).text
+            gca_foul = row.find("td", {"data-stat": "gca_fouled"}).text
+            gca_defense = row.find("td", {"data-stat": "gca_defense"}).text
+
+            # generate dictionary for team
+            mydict = {
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
+                "shot_creating_actions": shot_creating_actions,
+                "shot_creating_actions_p90": shot_creating_actions_p90,
+                "sca_pass_live": sca_pass_live,
+                "sca_pass_dead": sca_pass_dead,
+                "sca_take_on": sca_take_on,
+                "sca_shot": sca_shot,
+                "sca_foul": sca_foul,
+                "sca_defensive_action": sca_defense,
+                "goal_creating_actions": goal_creating_actions,
+                "goal_creating_actions_p90": goal_creating_actions_p90,
+                "gca_pass_live": gca_pass_live,
+                "gca_pass_dead": gca_pass_dead,
+                "gca_take_on": gca_take_on,
+                "gca_shot": gca_shot,
+                "gca_foul": gca_foul,
+                "gca_defensive_action": gca_defense,
+            }
+
+            # add to empty list
+            mylist.append(mydict)
+
+        # assign list to appropriate team
+        if side == "for":
+            goal_sca_stats_for = mylist.copy()
         else:
-            age = age[0]
-        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+            goal_sca_stats_against = mylist.copy()
 
-        shot_creating_actions = row.find("td", {"data-stat": "sca"}).text
-        shot_creating_actions_p90 = row.find("td", {"data-stat": "sca_per90"}).text
-
-        sca_pass_live = row.find("td", {"data-stat": "sca_passes_live"}).text
-        sca_pass_dead = row.find("td", {"data-stat": "sca_passes_dead"}).text
-        sca_dribble = row.find("td", {"data-stat": "sca_dribbles"}).text
-        sca_shot = row.find("td", {"data-stat": "sca_shots"}).text
-        sca_foul = row.find("td", {"data-stat": "sca_fouled"}).text
-        sca_defense = row.find("td", {"data-stat": "sca_defense"}).text
-
-        goal_creating_actions = row.find("td", {"data-stat": "gca"}).text
-        goal_creating_actions_p90 = row.find("td", {"data-stat": "gca_per90"}).text
-
-        gca_pass_live = row.find("td", {"data-stat": "gca_passes_live"}).text
-        gca_pass_dead = row.find("td", {"data-stat": "gca_passes_dead"}).text
-        gca_dribble = row.find("td", {"data-stat": "gca_dribbles"}).text
-        gca_shot = row.find("td", {"data-stat": "gca_shots"}).text
-        gca_foul = row.find("td", {"data-stat": "gca_fouled"}).text
-        gca_defense = row.find("td", {"data-stat": "gca_defense"}).text
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
-
-        # generate dictionary for player
-        mydict = {
-            "player_id": player_id,
-            "name": name,
-            "nation": nation,
-            "position": position,
-            "age": age,
-            "90s": minutes_90,
-            "shot_creating_actions": shot_creating_actions,
-            "shot_creating_actions_p90": shot_creating_actions_p90,
-            "sca_pass_live": sca_pass_live,
-            "sca_pass_dead": sca_pass_dead,
-            "sca_dribble": sca_dribble,
-            "sca_shot": sca_shot,
-            "sca_foul": sca_foul,
-            "sca_defensive_action": sca_defense,
-            "goal_creating_actions": goal_creating_actions,
-            "goal_creating_actions_p90": goal_creating_actions_p90,
-            "gca_pass_live": gca_pass_live,
-            "gca_pass_dead": gca_pass_dead,
-            "gca_dribble": gca_dribble,
-            "gca_shot": gca_shot,
-            "gca_foul": gca_foul,
-            "gca_defensive_action": gca_defense,
-            "match_logs": match_logs,
-        }
-
-        # add to empty list
-        mylist.append(mydict)
-
-    return mylist
+    return goal_sca_stats_for, goal_sca_stats_against
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_keeper_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_goal_sca_stats.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,102 +1,111 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_keeper_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts basic keeper stats for each player in a given team
+def fb_team_player_goal_sca_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts shot and goal creating actions for each player in a given team
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: goalkeeper stats for each player
+        list: shot and goal creating actions for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_keeper"})
+    div = pageSoup.find("div", {"id": "all_stats_gca"})
+    if div is None:
+        return None
 
     table = div.find("table")
     tbody = table.find("tbody")
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
-        matches = row.find("td", {"data-stat": "games_gk"}).text
-        starts = row.find("td", {"data-stat": "games_starts_gk"}).text
-        minutes = row.find("td", {"data-stat": "minutes_gk"}).text
+        except ValueError:
+            age = None
         minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
 
-        goals_allowed = row.find("td", {"data-stat": "goals_against_gk"}).text
-        goals_allowed_p90 = row.find("td", {"data-stat": "goals_against_per90_gk"}).text
-        shots_against = row.find("td", {"data-stat": "shots_on_target_against"}).text
-        saves = row.find("td", {"data-stat": "saves"}).text
-        save_pct = row.find("td", {"data-stat": "save_pct"}).text
-        wins = row.find("td", {"data-stat": "wins_gk"}).text
-        draws = row.find("td", {"data-stat": "draws_gk"}).text
-        losses = row.find("td", {"data-stat": "losses_gk"}).text
-        clean_sheets = row.find("td", {"data-stat": "clean_sheets"}).text
-        cleen_sheet_pct = row.find("td", {"data-stat": "clean_sheets_pct"}).text
-
-        pk_against = row.find("td", {"data-stat": "pens_att_gk"}).text
-        pk_allowed = row.find("td", {"data-stat": "pens_allowed"}).text
-        pk_saves = row.find("td", {"data-stat": "pens_saved"}).text
-        pk_missed = row.find("td", {"data-stat": "pens_missed_gk"}).text
-        pk_save_pct = row.find("td", {"data-stat": "pens_save_pct"}).text
+        # sca
+        shot_creating_actions = row.find("td", {"data-stat": "sca"}).text
+        shot_creating_actions_p90 = row.find("td", {"data-stat": "sca_per90"}).text
+
+        # sca types
+        sca_pass_live = row.find("td", {"data-stat": "sca_passes_live"}).text
+        sca_pass_dead = row.find("td", {"data-stat": "sca_passes_dead"}).text
+        sca_take_on = row.find("td", {"data-stat": "sca_take_ons"}).text
+        sca_shot = row.find("td", {"data-stat": "sca_shots"}).text
+        sca_foul = row.find("td", {"data-stat": "sca_fouled"}).text
+        sca_defense = row.find("td", {"data-stat": "sca_defense"}).text
+
+        # gca
+        goal_creating_actions = row.find("td", {"data-stat": "gca"}).text
+        goal_creating_actions_p90 = row.find("td", {"data-stat": "gca_per90"}).text
+
+        # gca types
+        gca_pass_live = row.find("td", {"data-stat": "gca_passes_live"}).text
+        gca_pass_dead = row.find("td", {"data-stat": "gca_passes_dead"}).text
+        gca_take_on = row.find("td", {"data-stat": "gca_take_ons"}).text
+        gca_shot = row.find("td", {"data-stat": "gca_shots"}).text
+        gca_foul = row.find("td", {"data-stat": "gca_fouled"}).text
+        gca_defense = row.find("td", {"data-stat": "gca_defense"}).text
 
+        # match logs
         match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
             "href"
         ]
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
-            "matches": matches,
-            "starts": starts,
-            "minutes": minutes,
             "90s": minutes_90,
-            "goals_allowed": goals_allowed,
-            "goals_allowed_p90": goals_allowed_p90,
-            "shots_against": shots_against,
-            "saves": saves,
-            "saves_pct": save_pct,
-            "wins": wins,
-            "draws": draws,
-            "losses": losses,
-            "clean_sheets": clean_sheets,
-            "clean_sheets_pct": cleen_sheet_pct,
-            "pk_against": pk_against,
-            "pk_allowed": pk_allowed,
-            "pk_saves": pk_saves,
-            "pk_missed": pk_missed,
-            "pk_save_pct": pk_save_pct,
+            "shot_creating_actions": shot_creating_actions,
+            "shot_creating_actions_p90": shot_creating_actions_p90,
+            "sca_pass_live": sca_pass_live,
+            "sca_pass_dead": sca_pass_dead,
+            "sca_take_on": sca_take_on,
+            "sca_shot": sca_shot,
+            "sca_foul": sca_foul,
+            "sca_defensive_action": sca_defense,
+            "goal_creating_actions": goal_creating_actions,
+            "goal_creating_actions_p90": goal_creating_actions_p90,
+            "gca_pass_live": gca_pass_live,
+            "gca_pass_dead": gca_pass_dead,
+            "gca_take_on": gca_take_on,
+            "gca_shot": gca_shot,
+            "gca_foul": gca_foul,
+            "gca_defensive_action": gca_defense,
             "match_logs": match_logs,
         }
 
         # add to empty list
         mylist.append(mydict)
 
     return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_misc_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_keeper_stats.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,101 +1,111 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_misc_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts miscellaneous stats for rach player in a given team
+def fb_team_player_keeper_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts basic keeper stats for each player in a given team
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: miscellaneous stats for each player
+        list: goalkeeper stats for each player
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
     # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_misc"})
-    if div is None:
-        return None
+    div = pageSoup.find("div", {"id": "all_stats_keeper"})
 
     table = div.find("table")
-    table = div.find("table")
     tbody = table.find("tbody")
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
+        except ValueError:
+            age = None
 
-        crdY = row.find("td", {"data-stat": "cards_yellow"}).text
-        crdR = row.find("td", {"data-stat": "cards_red"}).text
-        crdY2 = row.find("td", {"data-stat": "cards_yellow_red"}).text
-        fls = row.find("td", {"data-stat": "fouls"}).text
-        fld = row.find("td", {"data-stat": "fouled"}).text
-        off = row.find("td", {"data-stat": "offsides"}).text
-        crs = row.find("td", {"data-stat": "crosses"}).text
-        interceptions = row.find("td", {"data-stat": "interceptions"}).text
-        tklW = row.find("td", {"data-stat": "tackles_won"}).text
-        pk_won = row.find("td", {"data-stat": "pens_won"}).text
-        pk_con = row.find("td", {"data-stat": "pens_conceded"}).text
-        og = row.find("td", {"data-stat": "own_goals"}).text
-        try:
-            recov = row.find("td", {"data-stat": "ball_recoveries"}).text
-            aerial_won = row.find("td", {"data-stat": "aerials_won"}).text
-            aerial_lost = row.find("td", {"data-stat": "aerials_lost"}).text
-            aerial_pct = row.find("td", {"data-stat": "aerials_won_pct"}).text
-        except AttributeError:
-            recov = aerial_won = aerial_lost = aerial_pct = None
+        # playing time
+        matches = row.find("td", {"data-stat": "gk_games"}).text
+        starts = row.find("td", {"data-stat": "gk_games_starts"}).text
+        minutes = row.find("td", {"data-stat": "gk_minutes"}).text
+        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+
+        # performance
+        goals_allowed = row.find("td", {"data-stat": "gk_goals_against"}).text
+        goals_allowed_p90 = row.find("td", {"data-stat": "gk_goals_against_per90"}).text
+        shots_against = row.find("td", {"data-stat": "gk_shots_on_target_against"}).text
+        saves = row.find("td", {"data-stat": "gk_saves"}).text
+        save_pct = row.find("td", {"data-stat": "gk_save_pct"}).text
+        wins = row.find("td", {"data-stat": "gk_wins"}).text
+        draws = row.find("td", {"data-stat": "gk_ties"}).text
+        losses = row.find("td", {"data-stat": "gk_losses"}).text
+        clean_sheets = row.find("td", {"data-stat": "gk_clean_sheets"}).text
+        cleen_sheet_pct = row.find("td", {"data-stat": "gk_clean_sheets_pct"}).text
+
+        # penalty kicks
+        pk_against = row.find("td", {"data-stat": "gk_pens_att"}).text
+        pk_allowed = row.find("td", {"data-stat": "gk_pens_allowed"}).text
+        pk_saves = row.find("td", {"data-stat": "gk_pens_saved"}).text
+        pk_missed = row.find("td", {"data-stat": "gk_pens_missed"}).text
+        pk_save_pct = row.find("td", {"data-stat": "gk_pens_save_pct"}).text
 
+        # match logs
         match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
             "href"
         ]
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
-            "cards_yellow": crdY,
-            "cards_red": crdR,
-            "cards_second_yellow": crdY2,
-            "fouls": fls,
-            "fouled": fld,
-            "offsides": off,
-            "crosses": crs,
-            "interceptions": interceptions,
-            "tackles_won": tklW,
-            "pk_won": pk_won,
-            "pk_con": pk_con,
-            "own_goals": og,
-            "recoveries": recov,
-            "aerials_won": aerial_won,
-            "aerials_lost": aerial_lost,
-            "aerials_pct": aerial_pct,
+            "matches": matches,
+            "starts": starts,
+            "minutes": minutes,
+            "90s": minutes_90,
+            "goals_allowed": goals_allowed,
+            "goals_allowed_p90": goals_allowed_p90,
+            "shots_against": shots_against,
+            "saves": saves,
+            "saves_pct": save_pct,
+            "wins": wins,
+            "draws": draws,
+            "losses": losses,
+            "clean_sheets": clean_sheets,
+            "clean_sheets_pct": cleen_sheet_pct,
+            "pk_against": pk_against,
+            "pk_allowed": pk_allowed,
+            "pk_saves": pk_saves,
+            "pk_missed": pk_missed,
+            "pk_save_pct": pk_save_pct,
             "match_logs": match_logs,
         }
 
         # add to empty list
         mylist.append(mydict)
 
     return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_passing_stats.py` & `reus-1.1.1/reus/fbref/fb_team_shooting_stats.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,115 +1,110 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_passing_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts passing stats for each player in a given team
+def fb_team_shooting_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts shooting stats for each team in a given league
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: passing stats for each player
+        tuple: shooting stats for home and away team players
+            list: shooting stats for each team
+            list: shooting stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_passing"})
-    if div is None:
-        return None
-
-    table = div.find("table")
-    tbody = table.find("tbody")
-    rows = tbody.find_all("tr")
-
-    # Generate empty list
-    mylist = []
-
-    # iterate through each player and store attributes
-    for row in rows:
-        th = row.find("th")
-        name = th["csk"]
-        player_id = th.find("a", href=True)["href"].split("/")[3]
-        nation = row.find("td", {"data-stat": "nationality"}).text
-        position = row.find("td", {"data-stat": "position"}).text
-        age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
-            age = int(age[0]) + int(age[1]) / 365
+    for side in ["for", "against"]:
+        # generate empty list for each team
+        mylist = []
+        # generate html id
+        id_ = "stats_squads_shooting_" + side
+
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
+
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
+            th = row.find("th")
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+            matches = row.find("td", {"data-stat": "minutes_90s"}).text
+
+            # standard
+            goals = row.find("td", {"data-stat": "goals"}).text
+            shots = row.find("td", {"data-stat": "shots"}).text
+            shots_on_target = row.find("td", {"data-stat": "shots_on_target"}).text
+            shots_on_target_per = row.find(
+                "td", {"data-stat": "shots_on_target_pct"}
+            ).text
+            shots_p90 = row.find("td", {"data-stat": "shots_per90"}).text
+            shots_on_target_p90 = row.find(
+                "td", {"data-stat": "shots_on_target_per90"}
+            ).text
+            goals_per_shot = row.find("td", {"data-stat": "goals_per_shot"}).text
+            goals_per_sot = row.find(
+                "td", {"data-stat": "goals_per_shot_on_target"}
+            ).text
+            try:
+                dist = row.find("td", {"data-stat": "average_shot_distance"}).text
+                fk = row.find("td", {"data-stat": "shots_free_kicks"}).text
+            except AttributeError:
+                dist = fk = None
+            pk = row.find("td", {"data-stat": "pens_made"}).text
+            pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
+
+            # expected
+            try:
+                xG = row.find("td", {"data-stat": "xg"}).text
+                npxG = row.find("td", {"data-stat": "npxg"}).text
+                npxG_per_shot = row.find("td", {"data-stat": "npxg_per_shot"}).text
+                goals_xG = row.find("td", {"data-stat": "xg_net"}).text
+                npg_xG = row.find("td", {"data-stat": "npxg_net"}).text
+            except AttributeError:
+                xG = npxG = npxG_per_shot = goals_xG = npg_xG = None
+
+            # generate dictionary for team
+            mydict = {
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
+                "goals": goals,
+                "shots": shots,
+                "shots_on_target": shots_on_target,
+                "shots_on_target%": shots_on_target_per,
+                "shots_p90": shots_p90,
+                "shots_on_target_p90": shots_on_target_p90,
+                "goals_per_shot": goals_per_shot,
+                "goals_per_shot_on_target": goals_per_sot,
+                "avg_distance": dist,
+                "free_kicks": fk,
+                "pk": pk,
+                "pk_attempted": pk_attempted,
+                "xG": xG,
+                "npxG": npxG,
+                "npxG_per_shot": npxG_per_shot,
+                "goals_minus_xG": goals_xG,
+                "npg_minus_xG": npg_xG,
+            }
+
+            # add to empty list
+            mylist.append(mydict)
+
+        # assign list to appropriate team
+        if side == "for":
+            shooting_stats_for = mylist.copy()
         else:
-            age = age[0]
-        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+            shooting_stats_against = mylist.copy()
 
-        cmp = row.find("td", {"data-stat": "passes_completed"}).text
-        att = row.find("td", {"data-stat": "passes"}).text
-        acc = row.find("td", {"data-stat": "passes_pct"}).text
-        totdist = row.find("td", {"data-stat": "passes_total_distance"}).text
-        prgdist = row.find("td", {"data-stat": "passes_progressive_distance"}).text
-
-        short_cmp = row.find("td", {"data-stat": "passes_completed_short"}).text
-        short_att = row.find("td", {"data-stat": "passes_short"}).text
-        short_acc = row.find("td", {"data-stat": "passes_pct_short"}).text
-
-        med_cmp = row.find("td", {"data-stat": "passes_completed_medium"}).text
-        med_att = row.find("td", {"data-stat": "passes_medium"}).text
-        med_acc = row.find("td", {"data-stat": "passes_pct_medium"}).text
-
-        long_cmp = row.find("td", {"data-stat": "passes_completed_long"}).text
-        long_att = row.find("td", {"data-stat": "passes_long"}).text
-        long_acc = row.find("td", {"data-stat": "passes_pct_long"}).text
-
-        ast = row.find("td", {"data-stat": "assists"}).text
-        xA = row.find("td", {"data-stat": "xa"}).text
-        ast_xA = row.find("td", {"data-stat": "xa_net"}).text
-        key_passes = row.find("td", {"data-stat": "assisted_shots"}).text
-        final_third = row.find("td", {"data-stat": "passes_into_final_third"}).text
-        ppa = row.find("td", {"data-stat": "passes_into_penalty_area"}).text
-        crs_ppa = row.find("td", {"data-stat": "crosses_into_penalty_area"}).text
-        prog = row.find("td", {"data-stat": "progressive_passes"}).text
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
-
-        # generate dictionary for player
-        mydict = {
-            "player_id": player_id,
-            "name": name,
-            "nation": nation,
-            "position": position,
-            "age": age,
-            "90s": minutes_90,
-            "completed": cmp,
-            "attempted": att,
-            "accuracy": acc,
-            "total_distance": totdist,
-            "progressive_distance": prgdist,
-            "short_completed": short_cmp,
-            "short_attempted": short_att,
-            "short_accuracy": short_acc,
-            "medium_completed": med_cmp,
-            "medium_attempted": med_att,
-            "medium_accuracy": med_acc,
-            "long_completed": long_cmp,
-            "long_attempted": long_att,
-            "long_accuracy": long_acc,
-            "assists": ast,
-            "xA": xA,
-            "assists_minus_xA": ast_xA,
-            "key_passes": key_passes,
-            "into_final_third": final_third,
-            "into_penalty_area": ppa,
-            "crosses_into_penalty_area": crs_ppa,
-            "progressive_passes": prog,
-            "match_logs": match_logs,
-        }
-
-        # add to empty list
-        mylist.append(mydict)
-
-    return mylist
+    return shooting_stats_for, shooting_stats_against
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_passing_type_stats.py` & `reus-1.1.1/reus/fbref/fb_match_misc_stats.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,122 +1,118 @@
+from .fb_match_metadata import fb_match_metadata
 from ..util import get_page_soup
 
 
-def fb_team_player_passing_type_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts passing type stats for each player in a given team
+def fb_match_misc_stats(pageSoup=None, url: str = None) -> tuple:
+    """Extracts miscellaneous stats for each player in a given match that includes advanced data
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
-        url (str, optional): path of fbref team page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
+        url (str, optional): path of fbref match page. Defaults to None.
 
     Returns:
-        list: passing type stats for each player
+        tuple: miscellaneous stats for home and away team players
+            list: miscellaneous stats of home team players
+            list: miscellaneous stats of away team players
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_passing_types"})
-    if div is None:
-        return None
-
-    table = div.find("table")
-    tbody = table.find("tbody")
-    rows = tbody.find_all("tr")
-
-    # Generate empty list
-    mylist = []
-
-    # iterate through each player and store attributes
-    for row in rows:
-        th = row.find("th")
-        name = th["csk"]
-        player_id = th.find("a", href=True)["href"].split("/")[3]
-        nation = row.find("td", {"data-stat": "nationality"}).text
-        position = row.find("td", {"data-stat": "position"}).text
-        age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
-            age = int(age[0]) + int(age[1]) / 365
+    # Get team ids
+    metadata = fb_match_metadata(pageSoup)[0]
+    id_x = metadata.get("id_x")
+    id_y = metadata.get("id_y")
+
+    # Loop through both teams
+    for team_id in [id_x, id_y]:
+        # generate empty list for each team
+        mylist = []
+        # generate html id
+        id_ = "stats_" + team_id + "_misc"
+
+        # find miscellaneous stats object
+        stats_players = pageSoup.find("table", {"id": id_})
+        stats_players = stats_players.find_all("tr")
+
+        # iterate through each player and store metrics
+        for row in stats_players[2:-1]:
+            th = row.find("th")
+
+            # general
+            try:
+                name = th.text
+            except AttributeError:
+                name = th["csk"]
+            player_id = th.find("a", href=True)["href"].split("/")[3]
+
+            nation = row.find("td", {"data-stat": "nationality"}).text
+            position = row.find("td", {"data-stat": "position"}).text
+            age = row.find("td", {"data-stat": "age"}).text.split("-")
+            try:
+                age = int(age[0]) + int(age[1]) / 365
+            except ValueError:
+                age = None
+            minutes = row.find("td", {"data-stat": "minutes"}).text
+
+            # performance
+            cards_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
+            cards_red = row.find("td", {"data-stat": "cards_red"}).text
+            cards_yellow_red = row.find("td", {"data-stat": "cards_yellow_red"}).text
+            fouls = row.find("td", {"data-stat": "fouls"}).text
+            fouled = row.find("td", {"data-stat": "fouled"}).text
+            offsides = row.find("td", {"data-stat": "offsides"}).text
+            crosses = row.find("td", {"data-stat": "crosses"}).text
+            interceptions = row.find("td", {"data-stat": "interceptions"}).text
+            tackles_won = row.find("td", {"data-stat": "tackles_won"}).text
+            penalties_won = row.find("td", {"data-stat": "pens_won"}).text
+            penalties_conceded = row.find("td", {"data-stat": "pens_conceded"}).text
+            own_goals = row.find("td", {"data-stat": "own_goals"}).text
+            recoveries = row.find("td", {"data-stat": "ball_recoveries"}).text
+
+            # aerial duels
+            aerials_won = row.find("td", {"data-stat": "aerials_won"}).text
+            aerials_lost = row.find("td", {"data-stat": "aerials_lost"}).text
+            aerials_won_pct = row.find("td", {"data-stat": "aerials_won_pct"}).text
+            if aerials_won_pct == "":
+                aerials_won_pct = None
+
+            # generate dictionary for team
+            mydict = {
+                "player_id": player_id,
+                "name": name,
+                "nation": nation,
+                "position": position,
+                "age": age,
+                "minutes": minutes,
+                "cards_yellow": cards_yellow,
+                "cards_red": cards_red,
+                "cards_yellow_red": cards_yellow_red,
+                "fouls": fouls,
+                "fouled": fouled,
+                "offsides": offsides,
+                "crosses": crosses,
+                "interceptions": interceptions,
+                "tackles_won": tackles_won,
+                "pk_won": penalties_won,
+                "pk_con": penalties_conceded,
+                "own_goals": own_goals,
+                "recoveries": recoveries,
+                "aerials_won": aerials_won,
+                "aerials_lost": aerials_lost,
+                "aerials_won_pct": aerials_won_pct,
+            }
+
+            # add to empty list
+            mylist.append(mydict)
+
+        # assign list to appropriate team
+        if team_id == id_x:
+            players_misc_stats_x = mylist.copy()
         else:
-            age = age[0]
-        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+            players_misc_stats_y = mylist.copy()
 
-        att = row.find("td", {"data-stat": "passes"}).text
-
-        live = row.find("td", {"data-stat": "passes_live"}).text
-        dead = row.find("td", {"data-stat": "passes_dead"}).text
-        fk = row.find("td", {"data-stat": "passes_free_kicks"}).text
-        tb = row.find("td", {"data-stat": "through_balls"}).text
-        press = row.find("td", {"data-stat": "passes_pressure"}).text
-        sw = row.find("td", {"data-stat": "passes_switches"}).text
-        crs = row.find("td", {"data-stat": "crosses"}).text
-        ck = row.find("td", {"data-stat": "corner_kicks"}).text
-
-        ck_in = row.find("td", {"data-stat": "corner_kicks_in"}).text
-        ck_out = row.find("td", {"data-stat": "corner_kicks_out"}).text
-        ck_straight = row.find("td", {"data-stat": "corner_kicks_straight"}).text
-
-        height_ground = row.find("td", {"data-stat": "passes_ground"}).text
-        height_low = row.find("td", {"data-stat": "passes_low"}).text
-        height_high = row.find("td", {"data-stat": "passes_high"}).text
-
-        body_left = row.find("td", {"data-stat": "passes_left_foot"}).text
-        body_right = row.find("td", {"data-stat": "passes_right_foot"}).text
-        body_head = row.find("td", {"data-stat": "passes_head"}).text
-        body_ti = row.find("td", {"data-stat": "throw_ins"}).text
-        body_other = row.find("td", {"data-stat": "passes_other_body"}).text
-
-        out_cmp = row.find("td", {"data-stat": "passes_completed"}).text
-        out_off = row.find("td", {"data-stat": "passes_offsides"}).text
-        out_out = row.find("td", {"data-stat": "passes_oob"}).text
-        out_int = row.find("td", {"data-stat": "passes_intercepted"}).text
-        out_blk = row.find("td", {"data-stat": "passes_blocked"}).text
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
-
-        # generate dictionary for player
-        mydict = {
-            "player_id": player_id,
-            "name": name,
-            "nation": nation,
-            "position": position,
-            "age": age,
-            "90s": minutes_90,
-            "attempted": att,
-            "live": live,
-            "dead": dead,
-            "free_kick": fk,
-            "through_balls": tb,
-            "under_pressure": press,
-            "switches": sw,
-            "crosses": crs,
-            "corner_kicks": ck,
-            "corner_inswing": ck_in,
-            "corner_outswing": ck_out,
-            "corner_straight": ck_straight,
-            "height_ground": height_ground,
-            "height_low": height_low,
-            "height_high": height_high,
-            "body_left": body_left,
-            "body_right": body_right,
-            "body_head": body_head,
-            "body_throw_in": body_ti,
-            "body_other": body_other,
-            "completed": out_cmp,
-            "offsides": out_off,
-            "out_of_bounds": out_out,
-            "intercepted": out_int,
-            "blocked": out_blk,
-            "match_logs": match_logs,
-        }
-
-        # add to empty list
-        mylist.append(mydict)
-
-    return mylist
+    return players_misc_stats_x, players_misc_stats_y
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_playing_time_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_playing_time_stats.py`

 * *Files 10% similar despite different names*

```diff
@@ -26,70 +26,84 @@
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
+        except ValueError:
+            age = None
 
+        # playing time
         matches = row.find("td", {"data-stat": "games"}).text
         minutes = row.find("td", {"data-stat": "minutes"}).text
         minutes_per_match = row.find("td", {"data-stat": "minutes_per_game"}).text
         minutes_pct = row.find("td", {"data-stat": "minutes_pct"}).text
         minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
 
+        # starts
         starts = row.find("td", {"data-stat": "games_starts"}).text
         minutes_per_start = row.find("td", {"data-stat": "minutes_per_start"}).text
         full_90 = row.find("td", {"data-stat": "games_complete"}).text
 
+        # subs
         subs = row.find("td", {"data-stat": "games_subs"}).text
         minutes_per_sub = row.find("td", {"data-stat": "minutes_per_sub"}).text
         unused_sub = row.find("td", {"data-stat": "unused_subs"}).text
 
-        ppm = row.find("td", {"data-stat": "points_per_match"}).text
+        # Team Success
+        ppm = row.find("td", {"data-stat": "points_per_game"}).text
         goals = row.find("td", {"data-stat": "on_goals_for"}).text
         goals_allowed = row.find("td", {"data-stat": "on_goals_against"}).text
         plus_minus = row.find("td", {"data-stat": "plus_minus"}).text
         plus_minus_p90 = row.find("td", {"data-stat": "plus_minus_per90"}).text
         plus_minus_on_off = row.find("td", {"data-stat": "plus_minus_wowy"}).text
 
+        # Team Success (xG)
         try:
             xG = row.find("td", {"data-stat": "on_xg_for"}).text
             xGA = row.find("td", {"data-stat": "on_xg_against"}).text
             xG_plus_minus = row.find("td", {"data-stat": "xg_plus_minus"}).text
             xG_plus_minus_p90 = row.find(
                 "td", {"data-stat": "xg_plus_minus_per90"}
             ).text
             xG_plus_minus_on_off = row.find(
                 "td", {"data-stat": "xg_plus_minus_wowy"}
             ).text
         except AttributeError:
             xG = xGA = xG_plus_minus = xG_plus_minus_p90 = xG_plus_minus_on_off = None
 
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
+        # match logs
+        try:
+            match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
+                "href"
+            ]
+        except TypeError:
+            match_logs = None
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
+            "matches": matches,
             "minutes": minutes,
             "minutes_per_match": minutes_per_match,
             "minutes_pct": minutes_pct,
             "90s": minutes_90,
             "starts": starts,
             "minutes_per_start": minutes_per_start,
             "full_90": full_90,
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_possession_stats.py` & `reus-1.1.1/reus/fbref/fb_team_player_possession_stats.py`

 * *Files 19% similar despite different names*

```diff
@@ -33,96 +33,109 @@
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each player and store attributes
     for row in rows:
+        # general
         th = row.find("th")
-        name = th["csk"]
+        try:
+            name = th.text
+        except AttributeError:
+            name = th["csk"]
         player_id = th.find("a", href=True)["href"].split("/")[3]
         nation = row.find("td", {"data-stat": "nationality"}).text
         position = row.find("td", {"data-stat": "position"}).text
         age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
+        try:
             age = int(age[0]) + int(age[1]) / 365
-        else:
-            age = age[0]
+        except ValueError:
+            age = None
         minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
 
+        # touches
         touches = row.find("td", {"data-stat": "touches"}).text
-        touches_def_pen = row.find("td", {"data-stat": "touches_def_pen_area"}).text
-        touches_def = row.find("td", {"data-stat": "touches_def_3rd"}).text
-        touches_mid = row.find("td", {"data-stat": "touches_mid_3rd"}).text
-        touches_att = row.find("td", {"data-stat": "touches_att_3rd"}).text
-        touches_att_pen = row.find("td", {"data-stat": "touches_att_pen_area"}).text
+        touches_def_pen_area = row.find(
+            "td", {"data-stat": "touches_def_pen_area"}
+        ).text
+        touches_def_3rd = row.find("td", {"data-stat": "touches_def_3rd"}).text
+        touches_mid_3rd = row.find("td", {"data-stat": "touches_mid_3rd"}).text
+        touches_att_3rd = row.find("td", {"data-stat": "touches_att_3rd"}).text
+        touches_att_pen_area = row.find(
+            "td", {"data-stat": "touches_att_pen_area"}
+        ).text
         touches_live = row.find("td", {"data-stat": "touches_live_ball"}).text
 
-        dribble_success = row.find("td", {"data-stat": "dribbles_completed"}).text
-        dribble_attempted = row.find("td", {"data-stat": "dribbles"}).text
-        dribble_pct = row.find("td", {"data-stat": "dribbles_completed_pct"}).text
-        dribble_past = row.find("td", {"data-stat": "players_dribbled_past"}).text
-        dribble_meg = row.find("td", {"data-stat": "nutmegs"}).text
+        # take ons
+        dribble_attempt = row.find("td", {"data-stat": "take_ons"}).text
+        dribble_success = row.find("td", {"data-stat": "take_ons_won"}).text
+        dribble_success_pct = row.find("td", {"data-stat": "take_ons_won_pct"}).text
+        if dribble_success_pct == "":
+            dribble_success_pct = None
+        dribble_tackled = row.find("td", {"data-stat": "take_ons_tackled"}).text
+        dribble_tackled_pct = row.find("td", {"data-stat": "take_ons_tackled_pct"}).text
 
+        # carries
         carries = row.find("td", {"data-stat": "carries"}).text
-        carries_dist = row.find("td", {"data-stat": "carry_distance"}).text
-        carries_prg_dist = row.find(
-            "td", {"data-stat": "carry_progressive_distance"}
+        carries_total_distance = row.find("td", {"data-stat": "carries_distance"}).text
+        carries_progressive_distance = row.find(
+            "td", {"data-stat": "carries_progressive_distance"}
         ).text
-        carries_prg = row.find("td", {"data-stat": "progressive_carries"}).text
-        carries_final_third = row.find(
+        progressive_carries = row.find("td", {"data-stat": "progressive_carries"}).text
+        carries_into_final_third = row.find(
             "td", {"data-stat": "carries_into_final_third"}
         ).text
-        carries_pa = row.find("td", {"data-stat": "carries_into_penalty_area"}).text
-        miscon = row.find("td", {"data-stat": "miscontrols"}).text
-        dispos = row.find("td", {"data-stat": "dispossessed"}).text
+        carries_into_penalty_area = row.find(
+            "td", {"data-stat": "carries_into_penalty_area"}
+        ).text
+        miscontrols = row.find("td", {"data-stat": "miscontrols"}).text
+        dispossessed = row.find("td", {"data-stat": "dispossessed"}).text
 
-        passes_targeted = row.find("td", {"data-stat": "pass_targets"}).text
+        # receiving
         passes_received = row.find("td", {"data-stat": "passes_received"}).text
-        passes_received_pct = row.find("td", {"data-stat": "passes_received_pct"}).text
-        passes_received_prg = row.find(
+        progressive_passes_received = row.find(
             "td", {"data-stat": "progressive_passes_received"}
         ).text
 
+        # match logs
         match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
             "href"
         ]
 
         # generate dictionary for player
         mydict = {
             "player_id": player_id,
             "name": name,
             "nation": nation,
             "position": position,
             "age": age,
             "90s": minutes_90,
             "touches": touches,
-            "touches_defensive_pen": touches_def_pen,
-            "touches_defensive_third": touches_def,
-            "touches_middle_third": touches_mid,
-            "touches_attacking_third": touches_att,
-            "touches_attacking_pen": touches_att_pen,
+            "touches_def_pen_area": touches_def_pen_area,
+            "touches_def_3rd": touches_def_3rd,
+            "touches_mid_3rd": touches_mid_3rd,
+            "touches_att_3rd": touches_att_3rd,
+            "touches_att_pen_area": touches_att_pen_area,
             "touches_live": touches_live,
-            "dribbles_successful": dribble_success,
-            "dribbles_attempted": dribble_attempted,
-            "dribble_pct": dribble_pct,
-            "dribbled_past": dribble_past,
-            "dribble_megs": dribble_meg,
+            "dribble_attempt": dribble_attempt,
+            "dribble_success": dribble_success,
+            "dribble_success_pct": dribble_success_pct,
+            "dribble_tackled": dribble_tackled,
+            "dribble_tackled_pct": dribble_tackled_pct,
             "carries": carries,
-            "carry_distance": carries_dist,
-            "carry_progressive_distance": carries_prg_dist,
-            "carries_progressive": carries_prg,
-            "carries_into_final_third": carries_final_third,
-            "carries_into_penalty_area": carries_pa,
-            "miscontrols": miscon,
-            "dispossessed": dispos,
-            "passes_targeted": passes_targeted,
+            "carry_total_distance": carries_total_distance,
+            "carry_progressive_distance": carries_progressive_distance,
+            "progressive_carries": progressive_carries,
+            "carries_into_final_third": carries_into_final_third,
+            "carries_into_penalty_area": carries_into_penalty_area,
+            "miscontrols": miscontrols,
+            "dispossessed": dispossessed,
             "passes_received": passes_received,
-            "passes_received_pct": passes_received_pct,
-            "passes_received_progressive": passes_received_prg,
+            "progressive_passes_received": progressive_passes_received,
             "match_logs": match_logs,
         }
 
         # add to empty list
         mylist.append(mydict)
 
     return mylist
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_shooting_stats.py` & `reus-1.1.1/reus/fbref/fb_team_playing_time_stats.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,107 +1,107 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_shooting_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts shooting stats for each player in a given team
+def fb_team_playing_time_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts playing time stats for each team
 
     Args:
-        pageSoup (bs4, optional): bs4 object of a match. Defaults to None.
-        url (str, optional): path of fbref match page. Defaults to None.
+        pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
+        url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: shooting stats for each player
+        tuple: playing time stats for home and away team players
+            list: playing time stats for each team
+            list: playing time stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Find table object
-    div = pageSoup.find("div", {"id": "all_stats_shooting"})
-    table = div.find("table")
-    tbody = table.find("tbody")
-    rows = tbody.find_all("tr")
-
-    # Generate empty list
-    mylist = []
-
-    # iterate through each player and store attributes
-    for row in rows:
-        th = row.find("th")
-        name = th["csk"]
-        player_id = th.find("a", href=True)["href"].split("/")[3]
-        nation = row.find("td", {"data-stat": "nationality"}).text
-        position = row.find("td", {"data-stat": "position"}).text
-        age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
-            age = int(age[0]) + int(age[1]) / 365
+    for side in ["for", "against"]:
+        # generate empty list for each team
+        mylist = []
+        # generate html id
+        id_ = "stats_squads_playing_time_" + side
+
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
+
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
+            th = row.find("th")
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+
+            # playing time
+            matches = row.find("td", {"data-stat": "games"}).text
+            minutes = row.find("td", {"data-stat": "minutes"}).text
+
+            # starts
+            starts = row.find("td", {"data-stat": "games_starts"}).text
+            minutes_per_start = row.find("td", {"data-stat": "minutes_per_start"}).text
+            full_90 = row.find("td", {"data-stat": "games_complete"}).text
+
+            # subs
+            subs = row.find("td", {"data-stat": "games_subs"}).text
+            minutes_per_sub = row.find("td", {"data-stat": "minutes_per_sub"}).text
+            unused_sub = row.find("td", {"data-stat": "unused_subs"}).text
+
+            # Team Success
+            ppm = row.find("td", {"data-stat": "points_per_game"}).text
+            goals = row.find("td", {"data-stat": "on_goals_for"}).text
+            goals_allowed = row.find("td", {"data-stat": "on_goals_against"}).text
+            plus_minus = row.find("td", {"data-stat": "plus_minus"}).text
+            plus_minus_p90 = row.find("td", {"data-stat": "plus_minus_per90"}).text
+
+            # Team Success (xG)
+            try:
+                xG = row.find("td", {"data-stat": "on_xg_for"}).text
+                xGA = row.find("td", {"data-stat": "on_xg_against"}).text
+                xG_plus_minus = row.find("td", {"data-stat": "xg_plus_minus"}).text
+                xG_plus_minus_p90 = row.find(
+                    "td", {"data-stat": "xg_plus_minus_per90"}
+                ).text
+            except AttributeError:
+                xG = xGA = xG_plus_minus = xG_plus_minus_p90 = None
+
+            # generate dictionary for team
+            mydict = {
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
+                "minutes": minutes,
+                "starts": starts,
+                "minutes_per_start": minutes_per_start,
+                "full_90": full_90,
+                "subs": subs,
+                "minutes_per_sub": minutes_per_sub,
+                "unused_sub": unused_sub,
+                "ppm": ppm,
+                "goals": goals,
+                "goals_allowed": goals_allowed,
+                "plus_minus": plus_minus,
+                "plus_minus_p90": plus_minus_p90,
+                "xG": xG,
+                "xGA": xGA,
+                "xG_plus_minus": xG_plus_minus,
+                "xG_plus_minus_p90": xG_plus_minus_p90,
+            }
+
+            # add to empty list
+            mylist.append(mydict)
+
+        # assign list to appropriate team
+        if side == "for":
+            playing_time_stats_for = mylist.copy()
         else:
-            age = age[0]
-        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
+            playing_time_stats_against = mylist.copy()
 
-        goals = row.find("td", {"data-stat": "goals"}).text
-        shots = row.find("td", {"data-stat": "shots_total"}).text
-        shots_on_target = row.find("td", {"data-stat": "shots_on_target"}).text
-        shots_on_target_per = row.find("td", {"data-stat": "shots_on_target_pct"}).text
-        shots_p90 = row.find("td", {"data-stat": "shots_total_per90"}).text
-        shots_on_target_p90 = row.find(
-            "td", {"data-stat": "shots_on_target_per90"}
-        ).text
-        goals_per_shot = row.find("td", {"data-stat": "goals_per_shot"}).text
-        goals_per_sot = row.find("td", {"data-stat": "goals_per_shot_on_target"}).text
-        try:
-            dist = row.find("td", {"data-stat": "average_shot_distance"}).text
-            fk = row.find("td", {"data-stat": "shots_free_kicks"}).text
-        except AttributeError:
-            diist = fk = None
-        pk = row.find("td", {"data-stat": "pens_made"}).text
-        pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
-
-        try:
-            xG = row.find("td", {"data-stat": "xg"}).text
-            npxG = row.find("td", {"data-stat": "npxg"}).text
-            npxG_per_shot = row.find("td", {"data-stat": "npxg_per_shot"}).text
-            goals_xG = row.find("td", {"data-stat": "xg_net"}).text
-            npg_xG = row.find("td", {"data-stat": "npxg_net"}).text
-        except AttributeError:
-            xG = npxG = npxG_per_shot = goals_xG = npg_xG = None
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
-
-        # generate dictionary for player
-        mydict = {
-            "player_id": player_id,
-            "name": name,
-            "nation": nation,
-            "position": position,
-            "age": age,
-            "90s": minutes_90,
-            "goals": goals,
-            "shots": shots,
-            "shots_on_target": shots_on_target,
-            "shots_on_target%": shots_on_target_per,
-            "shots_p90": shots_p90,
-            "shots_on_target_p90": shots_on_target_p90,
-            "goals_per_shot": goals_per_shot,
-            "goals_per_shot_on_target": goals_per_sot,
-            "avg_distance": dist,
-            "free_kicks": fk,
-            "pk": pk,
-            "pk_attempted": pk_attempted,
-            "xG": xG,
-            "npxG": npxG,
-            "npxG_per_shot": npxG_per_shot,
-            "goals_minus_xG": goals_xG,
-            "npg_minus_xG": npg_xG,
-            "match_logs": match_logs,
-        }
-
-        # add to empty list
-        mylist.append(mydict)
-
-    return mylist
+    return playing_time_stats_for, playing_time_stats_against
```

### Comparing `reus-1.1.0/reus/fbref/fb_team_player_summary_stats.py` & `reus-1.1.1/reus/fbref/fb_team_misc_stats.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,115 +1,98 @@
 from ..util import get_page_soup
 
 
-def fb_team_player_summary_stats(pageSoup=None, url: str = None) -> list:
-    """Extracts summary stats for each player in a given team
+def fb_team_misc_stats(pageSoup=None, url: str = None) -> list:
+    """Extracts miscellaneous stats for each team in a given league
 
     Args:
         pageSoup (bs4, optional): bs4 object of a team. Defaults to None.
         url (str, optional): path of fbref team page. Defaults to None.
 
     Returns:
-        list: summary stats for each player
+        tuple: miscellaneous stats for home and away team players
+            list: miscellaneous stats for each team
+            list: miscellaneous stats against each team
     """
 
     assert (
         pageSoup is not None or url is not None
     ), "Either pageSoup or url must be provided"
 
     if pageSoup is None:
         pageSoup = get_page_soup(url)
 
-    # Find table object
-    table = pageSoup.find("table")
-    tbody = table.find("tbody")
-    rows = tbody.find_all("tr")
-
-    # Generate empty list
-    mylist = []
-
-    # iterate through each player and store attributes
-    for row in rows:
-        th = row.find("th")
-        name = th["csk"]
-        player_id = th.find("a", href=True)["href"].split("/")[3]
-        nation = row.find("td", {"data-stat": "nationality"}).text
-        position = row.find("td", {"data-stat": "position"}).text
-        age = row.find("td", {"data-stat": "age"}).text.split("-")
-        if len(age) > 1:
-            age = int(age[0]) + int(age[1]) / 365
+    for side in ["for", "against"]:
+        # generate empty list for each team
+        mylist = []
+        # generate html id
+        id_ = "stats_squads_misc_" + side
+
+        # find goalkeeping object
+        stats = pageSoup.find("table", {"id": id_})
+        stats = stats.find_all("tr")
+
+        # iteratre through each team and store metrics
+        for row in stats[2:]:
+            th = row.find("th")
+            # general
+            team = th.find("a", {"href": True}).text.strip()
+            team_id = th.find("a", {"href": True})["href"].split("/")[3]
+            num_players = row.find("td", {"data-stat": "players_used"}).text
+            matches = row.find("td", {"data-stat": "minutes_90s"}).text
+
+            # performance
+            cards_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
+            cards_red = row.find("td", {"data-stat": "cards_red"}).text
+            cards_yellow_red = row.find("td", {"data-stat": "cards_yellow_red"}).text
+            fouls = row.find("td", {"data-stat": "fouls"}).text
+            fouled = row.find("td", {"data-stat": "fouled"}).text
+            offsides = row.find("td", {"data-stat": "offsides"}).text
+            crosses = row.find("td", {"data-stat": "crosses"}).text
+            interceptions = row.find("td", {"data-stat": "interceptions"}).text
+            tackles_won = row.find("td", {"data-stat": "tackles_won"}).text
+            penalties_won = row.find("td", {"data-stat": "pens_won"}).text
+            penalties_conceded = row.find("td", {"data-stat": "pens_conceded"}).text
+            own_goals = row.find("td", {"data-stat": "own_goals"}).text
+            recoveries = row.find("td", {"data-stat": "ball_recoveries"}).text
+
+            # aerial duels
+            aerials_won = row.find("td", {"data-stat": "aerials_won"}).text
+            aerials_lost = row.find("td", {"data-stat": "aerials_lost"}).text
+            aerials_won_pct = row.find("td", {"data-stat": "aerials_won_pct"}).text
+            if aerials_won_pct == "":
+                aerials_won_pct = None
+
+            # generate dictionary for team
+            mydict = {
+                "team_id": team_id,
+                "team": team,
+                "num_players": num_players,
+                "matches": matches,
+                "cards_yellow": cards_yellow,
+                "cards_red": cards_red,
+                "cards_yellow_red": cards_yellow_red,
+                "fouls": fouls,
+                "fouled": fouled,
+                "offsides": offsides,
+                "crosses": crosses,
+                "interceptions": interceptions,
+                "tackles_won": tackles_won,
+                "pk_won": penalties_won,
+                "pk_con": penalties_conceded,
+                "own_goals": own_goals,
+                "recoveries": recoveries,
+                "aerials_won": aerials_won,
+                "aerials_lost": aerials_lost,
+                "aerials_won_pct": aerials_won_pct,
+            }
+
+            # add to empty list
+            mylist.append(mydict)
+
+        # assign list to appropriate team
+        if side == "for":
+            misc_stats_for = mylist.copy()
         else:
-            age = age[0]
-        minutes = row.find("td", {"data-stat": "minutes"}).text
-        minutes_90 = row.find("td", {"data-stat": "minutes_90s"}).text
-
-        goals = row.find("td", {"data-stat": "goals"}).text
-        assists = row.find("td", {"data-stat": "assists"}).text
-        npg = row.find("td", {"data-stat": "goals_pens"}).text
-        pk = row.find("td", {"data-stat": "pens_made"}).text
-        pk_attempted = row.find("td", {"data-stat": "pens_att"}).text
-        card_yellow = row.find("td", {"data-stat": "cards_yellow"}).text
-        card_red = row.find("td", {"data-stat": "cards_red"}).text
-
-        goalp90 = row.find("td", {"data-stat": "goals_per90"}).text
-        assistsp90 = row.find("td", {"data-stat": "assists_per90"}).text
-        g_ap90 = row.find("td", {"data-stat": "goals_assists_per90"}).text
-        npgp90 = row.find("td", {"data-stat": "goals_pens_per90"}).text
-        npg_ap90 = row.find("td", {"data-stat": "goals_assists_pens_per90"}).text
-
-        try:
-            xG = row.find("td", {"data-stat": "xg"}).text
-            npxG = row.find("td", {"data-stat": "npxg"}).text
-            xA = row.find("td", {"data-stat": "xa"}).text
-            npxG_a = row.find("td", {"data-stat": "npxg_xa"}).text
-            xGp90 = row.find("td", {"data-stat": "xg_per90"}).text
-            xAp90 = row.find("td", {"data-stat": "xa_per90"}).text
-            xG_xAp90 = row.find("td", {"data-stat": "xg_xa_per90"}).text
-            npxGp90 = row.find("td", {"data-stat": "npxg_per90"}).text
-            npxG_ap90 = row.find("td", {"data-stat": "npxg_xa_per90"}).text
-        except AttributeError:
-            xG = (
-                npxG
-            ) = xA = npxG_a = xGp90 = xAp90 = xG_xAp90 = npxGp90 = npxG_ap90 = None
-
-        match_logs = row.find("td", {"data-stat": "matches"}).find("a", href=True)[
-            "href"
-        ]
-
-        # generate dictionary for player
-        mydict = {
-            "player_id": player_id,
-            "name": name,
-            "nation": nation,
-            "position": position,
-            "age": age,
-            "minutes": minutes,
-            "90s": minutes_90,
-            "goals": goals,
-            "assists": assists,
-            "npg": npg,
-            "pk": pk,
-            "pk_attempted": pk_attempted,
-            "card_yellow": card_yellow,
-            "card_red": card_red,
-            "goals_p90": goalp90,
-            "assists_p90": assistsp90,
-            "goals+assists_p90": g_ap90,
-            "npg_p90": npgp90,
-            "npg+assists_p90": npg_ap90,
-            "xG": xG,
-            "npxG": npxG,
-            "xA": xA,
-            "npxG+xA": npxG_a,
-            "xG_p90": xGp90,
-            "xA_p90": xAp90,
-            "xG+xA_p90": xG_xAp90,
-            "npxG_p90": npxGp90,
-            "npxG+xA_p90": npxG_ap90,
-            "npxG+xA": npxG_a,
-            "match_logs": match_logs,
-        }
+            misc_stats_against = mylist.copy()
 
-        # add to empty list
-        mylist.append(mydict)
-
-    return mylist
+    return misc_stats_for, misc_stats_against
```

### Comparing `reus-1.1.0/reus/fotmob/fm_leagues.py` & `reus-1.1.1/reus/fotmob/fm_leagues.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import pandas as pd
 
 
 def fm_leagues(
     ccode: str = None, country: str = None, league_id: str = None, name: str = None
-):
+) -> pd.DataFrame:
     """Returns a dataframe of league information
 
     Args:
         ccode (str): country code of a league. Defaults to None.
         country (str): country of a league. Defaults to None.
         league_id (str): league id of a league. Defaults to None.
         name (str): name of a league. Defaults to None.
```

### Comparing `reus-1.1.0/reus/fotmob/fm_match_data.py` & `reus-1.1.1/reus/fotmob/fm_match_data.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,61 +1,81 @@
 import json
 from urllib.request import urlopen
 import re
+import datetime as dt
+from .util import extract_player_stats
 
 
-def fm_match_data(match_id: str) -> tuple:
+def fm_match_data(
+    match_id: str, save_json: bool = False, json_file: json = None
+) -> tuple:
     """Returns metadata and match data for a given match id
 
     Args:
         match_id (str): id of a match
 
     Returns:
         tuple: match data
             dict: metadata information
             list: events
             list: shots
             list: bench players
             list starters
             list: players not available
             list: shootout
+            json: json file (if save_json=True)
     """
 
     assert isinstance(match_id, str), "match_id must be a string"
 
-    url = f"https://www.fotmob.com/api/matchDetails?matchId={match_id}"
+    if json_file is None:
+        url = f"https://www.fotmob.com/api/matchDetails?matchId={match_id}"
 
-    response = urlopen(url)
-    data = json.loads(response.read())
+        response = urlopen(url)
+        data = json.loads(response.read())
+    else:
+        data = json_file
 
     general = data.get("general")
     header = data.get("header")
     content = data.get("content")
     matchFacts = content.get("matchFacts")
     matchStats = content.get("stats").get("stats")
     shotmap = content.get("shotmap").get("shots")
     lineup = content.get("lineup")
 
     metadata = {}
     metadata["id"] = general.get("matchId")
-    metadata["date"] = header.get("status").get("startDateStr")
-    metadata["time"] = matchFacts.get("infoBox").get("Match Date").get("timeFormatted")
+    metadata["url"] = (
+        "/match/" + metadata["id"] + "/matchfacts/" + data.get("seo").get("path")
+    )
+    # metadata["date"] = header.get("status").get("startDateStr")
+    utcTime = dt.datetime.fromisoformat(
+        header.get("status").get("utcTime")[:-1] + "+00:00"
+    )
+    metadata["date"] = str(utcTime.date())
+    # metadata["time"] = matchFacts.get("infoBox").get("Match Date").get("timeFormatted")
+    metadata["time"] = str(utcTime.time())
     metadata["league_id"] = general.get("leagueId")
     metadata["league"] = general.get("leagueName")
     metadata["perent_league_id"] = general.get("parentLeagueId")
     metadata["parent_league"] = general.get("parentLeagueName")
-    metadata["country"] = general.get("countryCode")
+    metadata["parent_country"] = general.get("countryCode")
     metadata["season"] = general.get("parentLeagueSeason")
     metadata["matchweek"] = general.get("matchRound")
     metadata["team_x"] = general.get("homeTeam").get("name")
     metadata["team_y"] = general.get("awayTeam").get("name")
     metadata["id_x"] = general.get("homeTeam").get("id")
     metadata["id_y"] = general.get("awayTeam").get("id")
-    metadata["color_x"] = general.get("teamColors").get("home")
-    metadata["color_y"] = general.get("teamColors").get("away")
+    try:
+        metadata["color_x"] = general.get("teamColors").get("home")
+        metadata["color_y"] = general.get("teamColors").get("away")
+    except AttributeError:
+        metadata["color_x"] = general.get("teamColors")[0].get("color")
+        metadata["color_y"] = general.get("teamColors")[1].get("color")
     metadata["score_x"] = header.get("teams")[0].get("score")
     metadata["score_y"] = header.get("teams")[1].get("score")
     metadata["reason"] = header.get("status").get("reason").get("long")
     try:
         metadata["highlights"] = matchFacts.get("highlights").get("url")
     except AttributeError:
         metadata["highlights"] = None
@@ -63,42 +83,47 @@
     metadata["venue"] = stadium.get("name")
     metadata["city"] = stadium.get("city")
     metadata["country"] = stadium.get("country")
     metadata["lat"] = stadium.get("lat")
     metadata["long"] = stadium.get("long")
     metadata["referee"] = matchFacts.get("infoBox").get("Referee").get("text")
     metadata["attendance"] = matchFacts.get("infoBox").get("Attendance")
-    metadata["player_of_match"] = " ".join(
-        matchFacts.get("playerOfTheMatch").get("name").values()
-    )
-    metadata["player_of_match_id"] = matchFacts.get("playerOfTheMatch").get("id")
+    try:
+        metadata["player_of_match"] = " ".join(
+            matchFacts.get("playerOfTheMatch").get("name").values()
+        )
+        metadata["player_of_match_id"] = matchFacts.get("playerOfTheMatch").get("id")
+    except AttributeError:
+        metadata["player_of_match"] = None
+        metadata["player_of_match_id"] = None
 
     eventList = []
     events = matchFacts.get("events")["events"]
     score = "0:0"
     for e in events:
         mydict = {}
         mydict["minute"] = e.get("time")
         mydict["minute_stoppage"] = e.get("overloadTime")
         mydict["event"] = e.get("type")
-
+        if e.get("isHome"):
+            mydict["team_id"] = metadata["id_x"]
+        else:
+            mydict["team_id"] = metadata["id_y"]
         mydict["score_pre"] = score
 
         if mydict["event"] == "Goal":
             mydict["player1"] = e.get("player").get("name")
             mydict["player1_id"] = e.get("player").get("id")
             mydict["player1_url"] = e.get("player").get("profileUrl")
-            mydict["player2"] = None
-
             try:
-                mydict["player2_name"] = re.findall(
+                mydict["player2"] = re.findall(
                     "(?<=assist by ).*$", e.get("assistStr")
                 )[0]
             except TypeError:
-                mydict["player2_name"] = None
+                mydict["player2"] = None
             mydict["player2_id"] = e.get("assistPlayerId")
             mydict["player2_url"] = e.get("assistProfileUrl")
             newScore = e.get("newScore")
             mydict["score_post"] = str(newScore[0]) + ":" + str(newScore[1])
             score = mydict["score_post"]
             mydict["own_goal"] = False if e.get("ownGoal") is None else True
             mydict["is_penalty"] = (
@@ -134,14 +159,18 @@
 
     try:
         shootoutList = []
         penalty_events = matchFacts.get("events")["penaltyShootoutEvents"]
         shootout_score = "0:0"
         for p in penalty_events:
             mydict = {}
+            if p.get("isHome"):
+                mydict["team_id"] = metadata["id_x"]
+            else:
+                mydict["team_id"] = metadata["id_y"]
             mydict["event"] = p.get("type")
             mydict["shooter"] = p.get("nameStr")
             mydict["shooter_id"] = p.get("player").get("id")
             mydict["shooter_url"] = p.get("profileUrl")
             mydict["score_pre"] = shootout_score
             try:
                 newScore = p.get("penShootoutScore")
@@ -154,15 +183,14 @@
     except TypeError:
         shootoutList = None
 
     stats = {}
     for s in matchStats[1:]:
         for i in s.get("stats"):
             if i.get("stats") != [None, None]:
-
                 if "xG" in i.get("title"):
                     val_x = float(i.get("stats")[0])
                     val_y = float(i.get("stats")[1])
                 else:
                     val_x = i.get("stats")[0]
                     val_y = i.get("stats")[1]
 
@@ -190,53 +218,68 @@
         mydict["blocked_x"] = shot.get("blockedX")
         mydict["blocked_y"] = shot.get("blockedY")
         mydict["goal_crossed_y"] = shot.get("goalCrossedY")
         mydict["goal_crossed_z"] = shot.get("goalCrossedZ")
         mydict["xG"] = shot.get("expectedGoals")
         mydict["xGOT"] = shot.get("expectedGoalsOnTarget")
         on_goal = shot.get("onGoalShot")
-        mydict["on_goal_x"] = on_goal.get("x")
-        mydict["on_goal_y"] = on_goal.get("y")
-        mydict["on_goal_zoom_ratio"] = on_goal.get("zoomRatio")
+        try:
+            mydict["on_goal_x"] = on_goal.get("x")
+            mydict["on_goal_y"] = on_goal.get("y")
+            mydict["on_goal_zoom_ratio"] = on_goal.get("zoomRatio")
+        except AttributeError:
+            mydict["on_goal_x"] = None
+            mydict["on_goal_y"] = None
+            mydict["on_goal_zoom_ratio"] = None
 
         shotList.append(mydict)
 
     benchPlayerList = []
     startPlayerList = []
 
     for i in lineup.get("lineup"):
         idx = lineup.get("lineup").index(i)
         team_id = i.get("teamId")
         for b in i.get("bench"):
             mydict = {}
             mydict["team_id"] = team_id
             mydict["opta_id"] = b.get("usingOptaId")
             mydict["player_id"] = b.get("id")
-            mydict["player_name"] = " ".join(b.get("name").values())
+            # mydict["player_name"] = " ".join(b.get("name").values())
+            mydict["player_name"] = b.get("name").get("fullName")
             mydict["player_url"] = b.get("pageUrl")
             mydict["shirt_number"] = b.get("shirt")
             mydict["time_subbed_on"] = b.get("timeSubbedOn")
             mydict["time_subbed_off"] = b.get("timeSubbedOff")
             mydict["minutes_played"] = b.get("minutesPlayed")
             mydict["usual_position"] = b.get("usualPosition")
             mydict["role"] = b.get("role")
             mydict["is_captain"] = b.get("isCaptain")
-            mydict["rating"] = b.get("rating").get("num")
-            mydict["fantasy_points"] = b.get("fantasyScore").get("num")
+            try:
+                statsDict = extract_player_stats(b.get("stats"))
+                mydict.update(statsDict)
+            except TypeError:
+                pass
+
             benchPlayerList.append(mydict)
 
-        mgr = i.get("coach")[0]
-        if idx == 0:
-            metadata["manager_x"] = " ".join(mgr.get("name").values())
-            metadata["manager_id_x"] = mgr.get("id")
-            metadata["manager_url_x"] = mgr.get("pageUrl")
-        else:
-            metadata["manager_y"] = " ".join(mgr.get("name").values())
-            metadata["manager_id_y"] = mgr.get("id")
-            metadata["manager_url_y"] = mgr.get("pageUrl")
+        try:
+            mgr = i.get("coach")[0]
+            if idx == 0:
+                # metadata["manager_x"] = " ".join(mgr.get("name").values())
+                metadata["manager_x"] = mgr.get("name").get("fullName")
+                metadata["manager_id_x"] = mgr.get("id")
+                metadata["manager_url_x"] = mgr.get("pageUrl")
+            else:
+                # metadata["manager_y"] = " ".join(mgr.get("name").values())
+                metadata["manager_y"] = mgr.get("name").get("fullName")
+                metadata["manager_id_y"] = mgr.get("id")
+                metadata["manager_url_y"] = mgr.get("pageUrl")
+        except TypeError:
+            pass
 
         for j in i.get("players"):
             for k in j:
                 mydict = {}
                 mydict["team_id"] = team_id
                 mydict["opta_id"] = k.get("usingOptaId")
                 mydict["player_id"] = k.get("id")
@@ -246,72 +289,22 @@
                 mydict["time_subbed_on"] = k.get("timeSubbedOn")
                 mydict["time_subbed_off"] = k.get("timeSubbedOff")
                 mydict["minutes_played"] = k.get("minutesPlayed")
                 mydict["position"] = k.get("positionStringShort")
                 mydict["usual_position"] = k.get("usualPosition")
                 mydict["role"] = k.get("role")
                 mydict["is_captain"] = k.get("isCaptain")
-                mydict["fantasy_points"] = k.get("fantasyScore").get("num")
-                mydict["minutes"] = k.get("minutesPlayed")
-
-                playerStats = k.get("stats")[0].get("stats")
-                mydict["rating"] = playerStats.get("FotMob rating")
-                mydict["goals"] = playerStats.get("Goals")
-                mydict["assists"] = playerStats.get("Assists")
-                mydict["total_shots"] = playerStats.get("Total shots")
-                mydict["accurate_passes"] = playerStats.get("Accurate passes")
-                mydict["chances_created"] = playerStats.get("Chances created")
-                mydict["conceded_penalty"] = playerStats.get("Conceded penalty")
-                mydict["xA"] = playerStats.get("Expected assists (xA)")
-
                 try:
-                    playerStatsAttack = k.get("stats")[1].get("stats")
-                    mydict["touches"] = playerStatsAttack.get("Touches")
-                    mydict["successful_dribbles"] = playerStatsAttack.get(
-                        "Successful dribbles"
-                    )
-                    mydict["accurate_crosses"] = playerStatsAttack.get(
-                        "Accurate crosses"
-                    )
-                    mydict["accurate_long_balls"] = playerStatsAttack.get(
-                        "Accurate long balls"
-                    )
-                    mydict["dispossessed"] = playerStatsAttack.get("Dispossessed")
-
-                    playerStatsDefense = k.get("stats")[2].get("stats")
-                    mydict["tackles_won"] = playerStatsDefense.get("Tackles won")
-                    mydict["clearances"] = playerStatsDefense.get("Clearances")
-                    mydict["interceptions"] = playerStatsDefense.get("Interceptions")
-                    mydict["recoveries"] = playerStatsDefense.get("Recoveries")
-
-                    playerStatsDuels = k.get("stats")[3].get("stats")
-                    mydict["ground_duels_won"] = playerStatsDuels.get(
-                        "Ground duels won"
-                    )
-                    mydict["aerial_duels_won"] = playerStatsDuels.get(
-                        "Aerial duels won"
-                    )
-                    mydict["was_fouled"] = playerStatsDuels.get("Was fouled")
-                    mydict["fouls_committed"] = playerStatsDuels.get("Fouls committed")
-                except IndexError:
-                    mydict["accurate_long_balls"] = playerStats.get(
-                        "Accurate long balls"
-                    )
-                    mydict["touches"] = playerStats.get("Touches")
-
-                mydict["saves"] = playerStats.get("Saves")
-                mydict["goals_conceded"] = playerStats.get("Goals conceded")
-                mydict["xGOT_faced"] = playerStats.get("xGOT faced")
-                mydict["diving_save"] = playerStats.get("Diving save")
-                mydict["saves_inside_box"] = playerStats.get("Saves inside box")
-                mydict["acted_as_sweeper"] = playerStats.get("Acted as sweeper")
-                mydict["punches"] = playerStats.get("Punches")
-                mydict["throws"] = playerStats.get("Throws")
-                mydict["high_claims"] = playerStats.get("High claim")
-                mydict["recoveries"] = playerStats.get("Recoveries")
+                    mydict["fantasy_points"] = k.get("fantasyScore").get("num")
+                    statsDict = extract_player_stats(k.get("stats"))
+                    mydict.update(statsDict)
+                except AttributeError:
+                    # mydict["fantasy_points"] = None
+                    # mydict = {}
+                    pass
 
                 startPlayerList.append(mydict)
 
     if lineup.get("usingOptaLineup"):
         metadata["lineup_source"] = "Opta"
     elif lineup.get("usingEnetpulseLineup"):
         metadata["lineup_source"] = "Enetpulse"
@@ -322,31 +315,50 @@
     metadata["formation_y"] = lineup.get("lineup")[1].get("lineup")
     metadata["team_x_rating"] = lineup.get("teamRatings").get("home").get("num")
     metadata["team_y_rating"] = lineup.get("teamRatings").get("away").get("num")
 
     try:
         matchNaPlayers = lineup.get("naPlayers").get("naPlayersArr")
         naPlayerList = []
-        side = "team_x"
+        team_id = metadata["id_x"]
         for j in matchNaPlayers:
             for k in j:
                 mydict = {}
-                mydict["side"] = side
+                mydict["team_id"] = team_id
                 mydict["player_id"] = k.get("id")
                 mydict["player_name"] = k.get("naInfo").get("name")
                 mydict["player_url"] = k.get("pageUrl")
                 mydict["reason"] = k.get("naInfo").get("naReason")
-                mydict["expected_return"] = k.get("naInfo").get("expectedReturn")
+                try:
+                    mydict["expected_return"] = (
+                        k.get("naInfo")
+                        .get("expectedReturn")
+                        .get("expectedReturnFallback")
+                    )
+                except AttributeError:
+                    mydict["expected_return"] = None
                 naPlayerList.append(mydict)
-            side = "team_y"
+            team_id = metadata["id_y"]
     except AttributeError:
         naPlayerList = None
 
-    return (
-        metadata,
-        eventList,
-        shotList,
-        benchPlayerList,
-        startPlayerList,
-        naPlayerList,
-        shootoutList,
-    )
+    if save_json:
+        return (
+            metadata,
+            eventList,
+            shotList,
+            benchPlayerList,
+            startPlayerList,
+            naPlayerList,
+            shootoutList,
+            data,
+        )
+    else:
+        return (
+            metadata,
+            eventList,
+            shotList,
+            benchPlayerList,
+            startPlayerList,
+            naPlayerList,
+            shootoutList,
+        )
```

### Comparing `reus-1.1.0/reus/fotmob/fm_match_ids.py` & `reus-1.1.1/reus/fotmob/fm_match_ids.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,14 +38,14 @@
     for league in data.get("leagues"):
         if ccode != [None] and not league.get("ccode") in ccode:
             continue
 
         if name != [None] and not league.get("name") in name:
             continue
 
-        if league_id != [None] and not league.get("id") in league_id:
+        if league_id != [None] and not league.get("primaryId") in league_id:
             continue
 
         for match in league.get("matches"):
             myList.append(match.get("id"))
 
     return myList
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_player_injury.py` & `reus-1.1.1/reus/transfermarkt/tm_player_injury.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,37 +1,43 @@
 from .util import tm_player_injury_scraper
 from ..util import get_page_soup_headers
 
 
-def tm_player_injury(pageSoup) -> list:
-
+def tm_player_injury(pageSoup=None, url: str = None) -> list:
     """Extracts player injury history and equipped to handle players with multiple pages of injuries
 
     Args:
-        pageSoup (bs4): bs4 object of injury page for player referenced in url
+        pageSoup (bs4, optional): bs4 object of injury page for player referenced in url. Defaults to None.
+        url (str, optional): path of transfermarkt player page. Defaults to None.
 
     Returns:
         list: player injuries
     """
 
+    assert (
+        pageSoup is not None or url is not None
+    ), "Either pageSoup or url must be provided"
+
+    if pageSoup is None:
+        pageSoup = get_page_soup_headers(url)
+
     # Determine if multiple pages present
     injuryPages = len(pageSoup.find_all("li", {"class": "tm-pagination__list-item"}))
 
     # Execute one time using helper function
     if injuryPages == 0:
         injuries = tm_player_injury_scraper(pageSoup)
 
     # Multiple pages of injuries
     else:
         # execute 1st page
         injuries = tm_player_injury_scraper(pageSoup)
 
         # iterate over each subsequent page
         for p in range(1, injuryPages - 2):
-
             # generate url for next page
             page = pageSoup.find("meta", {"property": "og:url"})["content"]
             page = "/".join((page, "page", str(p + 1)))
 
             # return page soup for next page
             pageSoup = get_page_soup_headers(page)
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_player_market_value.py` & `reus-1.1.1/reus/transfermarkt/tm_player_market_value.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,20 +1,29 @@
 import re
+from ..util import get_page_soup_headers
 
 
-def tm_player_market_value(pageSoup) -> list:
+def tm_player_market_value(pageSoup=None, url: str = None) -> list:
     """Extracts date, team, and market value from highchart
 
     Args:
-        pageSoup (bs4): bs4 object of player page referenced in url
+        pageSoup (bs4, optional): bs4 object of player page referenced in url. Defaults to None.
+        url (str, optional): path of transfermarkt player page. Defaults to None.
 
     Returns:
         list: market value of player by date
     """
 
+    assert (
+        pageSoup is not None or url is not None
+    ), "Either pageSoup or url must be provided"
+
+    if pageSoup is None:
+        pageSoup = get_page_soup_headers(url)
+
     # Extract currency
     value = pageSoup.find("div", {"class": "data-header__box--small"}).find("a").text
     value = value.split("Last update: ")[0]
     currency = value[0]
 
     # Find hicharts script object
     script = pageSoup.find("script", text=re.compile("Highcharts.Chart")).string
@@ -28,15 +37,14 @@
     value = re.findall(pattern, script)
 
     # generate empty list
     mylist = []
 
     # iterate through each data point and store attributes
     for i in range(len(date)):
-
         # generate dictionary for each point
         mydict = {
             "date": date[i].replace("\\x20", " ").replace("'", ""),
             "team": team[i]
             .replace("\\x20", " ")
             .replace("\\u00E9", "\u00E9")
             .replace("'", ""),
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_player_metadata.py` & `reus-1.1.1/reus/transfermarkt/tm_player_metadata.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,21 +1,30 @@
 import re
+from ..util import get_page_soup_headers
 
 
-def tm_player_metadata(pageSoup) -> dict:
+def tm_player_metadata(pageSoup=None, url: str = None) -> dict:
     #
     """Extracts general player information (biographical, club, contract, market value, and miscellaneous)
 
     Args:
-        pageSoup (bs4): bs4 object of player page referenced in url
+        pageSoup (bs4, optional): bs4 object of player page referenced in url. Defaults to None.
+        url (str, optional): path of transfermarkt player page. Defaults to None.
 
     Returns:
         dict: player metadata
     """
 
+    assert (
+        pageSoup is not None or url is not None
+    ), "Either pageSoup or url must be provided"
+
+    if pageSoup is None:
+        pageSoup = get_page_soup_headers(url)
+
     # Extract url
     url = pageSoup.find("meta", {"property": "og:url"})["content"]
 
     # Find data object
     player_data = pageSoup.find("div", {"data-viewport": "Steckbrief"})
     headshot_url = pageSoup.find("div", {"class": "modal-trigger"}).find("img")["src"]
 
@@ -54,14 +63,24 @@
             player_data.find("span", text="Place of birth:")
             .find_next("span")
             .text.strip()
         )
     except AttributeError:
         birth_place = None
 
+    # birth country
+    try:
+        birth_country = (
+            player_data.find("span", text="Place of birth:")
+            .find_next("span")
+            .find("img")["title"]
+        )
+    except AttributeError:
+        birth_country = None
+
     # age
     try:
         age = player_data.find("span", text="Age:").find_next("span").text.strip()
     except AttributeError:
         age = None
 
     # height
@@ -171,25 +190,35 @@
 
     # club
     club = pageSoup.find("div", {"class": "data-header__box--big"})
     club = club.find("img", alt=True)["alt"]
 
     try:
         joined = pageSoup.find("span", text="Joined:")
-        joined = joined.find_next("span").text
+        joined = joined.find_next("span").text.strip()
     except AttributeError:
         joined = None
 
     # contract expiration
     try:
         contracted = pageSoup.find("span", text="Contract expires:")
-        contracted = contracted.find_next("span").text
+        contracted = contracted.find_next("span").text.strip()
     except AttributeError:
         contracted = None
 
+    # date of last contract extension
+    try:
+        extension = (
+            player_data.find("span", text="Date of last contract extension:")
+            .find_next("span")
+            .text.strip()
+        )
+    except AttributeError:
+        extension = None
+
     # market value
     try:
         # value = pageSoup.find("div", {"class": "dataMarktwert"}).text
         # updated = re.search("(?<=update: ).*$", value).group()
         # value = value.split(" ")[0].strip()
         value = (
             pageSoup.find("div", {"class": "data-header__box--small"}).find("a").text
@@ -215,14 +244,15 @@
         "id": id_,
         "name": name,
         "url": "/" + url.split("/")[-4] + "/profil/spieler/" + url.split("/")[-1],
         "headshot_url": headshot_url,
         "full_name": full_name,
         "born": birth_date,
         "birth_place": birth_place,
+        "birth_country": birth_country,
         "age": age,
         "height": height,
         "nationality": nationality[0],
         "position": position,
         "position_main": position_main,
         "position_alt1": pos_alt1,
         "position_alt2": pos_alt2,
@@ -231,13 +261,14 @@
         "outfitter": outfitter,
         "social_twitter": socialTwitter,
         "social_facebook": socialFacebook,
         "social_instagram": socialInstagram,
         "club": club,
         "joined": joined,
         "contracted": contracted,
+        "extension": extension,
         "currency": currency,
         "mv": value,
         "update": updated,
     }
 
     return mydict
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_player_transfers.py` & `reus-1.1.1/reus/transfermarkt/tm_player_transfers.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,29 +1,38 @@
-def tm_player_transfers(pageSoup) -> list:
+from ..util import get_page_soup_headers
 
+
+def tm_player_transfers(pageSoup=None, url: str = None) -> list:
     """Extracts player transfer information
 
     Args:
-        pageSoup (bs4): bs4 object of player page referenced in url
+        pageSoup (bs4, optional): bs4 object of player page referenced in url. Defaults to None.
+        url (str, optional): path of transfermarkt player page. Defaults to None.
 
     Returns:
         list: player transfers
     """
 
+    assert (
+        pageSoup is not None or url is not None
+    ), "Either pageSoup or url must be provided"
+
+    if pageSoup is None:
+        pageSoup = get_page_soup_headers(url)
+
     # Find transfer object
     transfer_data = pageSoup.find("div", {"data-viewport": "Transferhistorie"})
     table = transfer_data.find_all("div", {"class": "tm-player-transfer-history-grid"})
 
     # Generate empty list
     mylist = []
 
     # iterate through each transfer and store attributes
     # for row in rows:
     for row in table[1:-1]:
-
         # extract teams
         left = row.find(
             "div", {"class": "tm-player-transfer-history-grid__old-club"}
         ).text.strip()
         joined = row.find(
             "div", {"class": "tm-player-transfer-history-grid__new-club"}
         ).text.strip()
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_team_player_urls.py` & `reus-1.1.1/reus/transfermarkt/tm_team_player_data.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,72 +1,52 @@
 from ..util import get_page_soup_headers
 from .util import tm_format_currency
 import pandas as pd
 
 
-def tm_team_player_urls(club: str, season: str, currency="EUR") -> list:
-
+def tm_team_player_data(
+    club: str,
+    season: str,
+    domain: str = "us",
+    team_id: int = None,
+    transfermarkt_name: bool = False,
+) -> list:
     """Extracts basic player information for each player in a squad including basic player information,
     market value, and contract expiration
 
     Args:
         club (str): club name
         season (str): year at start of season
-        currency (str): desired currency to return for values. Defaults to EUR.
+        domain (str, optional): domain to use for transfermarkt. Defaults to "us".
+        team_id (int, optional): transfermarkt team id. Defaults to None.
+        transfermarkt_name (bool, optional): if True, club is a transfermarkt name. Defaults to False.
 
     Returns:
         list: squad players
     """
 
-    assert currency in [
-        "EUR",
-        "GBP",
-        "USD",
-    ], "Select a valid currency of EUR, GBP, or USD"
-
-    # Lookup team name
-    df = pd.read_csv(
-        "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/team_translations.csv",
-        keep_default_na=False,
-    )
-    df = df[
-        (df.fbref_name == club)
-        | (df.transfermarkt_name == club)
-        | (df.transfermarkt_link == club)
-        | (df.fcpython == club)
-        | (df.fivethirtyeight == club)
-    ]
-
-    season = str(season)
-
-    # Determine domain
-    match currency:
-        case "EUR":
-            domain = "https://www.transfermarkt.com"
-            signed_currency = "€"
-        case "GBP":
-            domain = "https://www.transfermarkt.co.uk"
-            signed_currency = "£"
-        case "USD":
-            domain = "https://www.transfermarkt.us"
-            signed_currency = "$"
+    if team_id is None and transfermarkt_name is False:
+        # Lookup team name
+        df = pd.read_csv(
+            "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/team_translations.csv",
+            keep_default_na=False,
+        )
+        df = df[
+            (df.fbref_name == club)
+            | (df.transfermarkt_name == club)
+            | (df.transfermarkt_link == club)
+            | (df.fcpython == club)
+            | (df.fivethirtyeight == club)
+        ]
+        club = df.transfermarkt_link.iloc[0]
+        team_id = int(df.transfermarkt.iloc[0])
 
     # Generate url
     try:
-        page = "/".join(
-            (
-                domain,
-                df.transfermarkt_link.iloc[0],
-                "kader/verein",
-                str(df.transfermarkt.iloc[0]),
-                "saison_id",
-                season,
-                "plus/1",
-            )
-        )
+        page = f"https://www.transfermarkt.{domain}/{club}/kader/verein/{str(team_id)}/saison_id/{season}/plus/1"
     except IndexError:
         print("This team does not exist, please confirm spelling")
         exit()
 
     pageSoup = get_page_soup_headers(page)
 
     # Find table object
@@ -77,15 +57,14 @@
     rows = tbody.find_all("tr")
 
     # Generate empty list
     mylist = []
 
     # iterate through each transfer and store attributes
     for row in rows:
-
         # check if valid row
         try:
             num = row.find("div", {"class": "rn_nummer"}).text
         except AttributeError:
             continue
 
         # extract basic info
@@ -141,28 +120,26 @@
         except TypeError:
             joined = None
 
         # extract signing information
         try:
             signed_from = data[-2].find("img")["alt"]
             signed_from_url = data[-2].find("a", href=True)["href"]
-            signed_value = data[-2].find("img")["title"].split()[-1]
-            signed_value = (
-                signed_value.replace(signed_currency, "")
-                .replace("-", "0")
-                .replace("transfer", "0")
-            )
+            signed_value = data[-2].find("a")["title"].split()[-1]
+            signed_currency = signed_value[0]
+            signed_value = signed_value.replace("-", "0").replace("transfer", "0")
             if signed_value == "?":
                 signed_value = "unknown"
             else:
                 signed_value = tm_format_currency(signed_value)
         except TypeError:
             signed_from = None
             signed_from_url = None
             signed_value = None
+            signed_currency = None
 
         # extract contracted
         try:
             contracted = data[-1].text.strip()
         except TypeError:
             contracted = None
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `reus-1.1.0/reus/transfermarkt/tm_team_transfers.py` & `reus-1.1.1/reus/transfermarkt/tm_team_transfers.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 from ..util import get_page_soup_headers
 from .util import tm_format_currency
 import pandas as pd
 
 
 def tm_team_transfers(
     club: str,
-    season,
+    season: str,
+    domain: str = "us",
     position_group="All",
     main_position="All",
     window="All",
-    currency="EUR",
+    team_id: int = None,
+    transfermarkt_name: bool = False,
 ) -> list:
-
     """Extracts player transfer information
 
     Args:
         club (str): club name
         season (str): year at start of season
+        domain (str, optional): domain to use for transfermarkt. Defaults to "us".
         position_group (str): position group to filter by. Defaults to All.
         main_position (str): main position to filter by. Defaults to All.
         window (str): transfer window to filter by. Defaults to All.
-        currency (str): desired currency to return for values. Defaults to EUR.
+        team_id (int, optional): transfermarkt team id. Defaults to None.
+        transfermarkt_name (bool, optional): if True, club is a transfermarkt name. Defaults to False.
 
     Returns:
         list: team transfers
     """
 
     # Validate variables
     assert position_group in [
@@ -49,40 +52,29 @@
         "Left Winger",
         "Right Winger",
         "Second Striker",
         "Centre-Forward",
     ], "Select a valid main position"
     assert window in ["All", "Summer", "Winter"], "Select a valid transfer window"
 
-    # Lookup team name
-    df = pd.read_csv(
-        "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/team_translations.csv",
-        keep_default_na=False,
-    )
-    df = df[
-        (df.fbref_name == club)
-        | (df.transfermarkt_name == club)
-        | (df.transfermarkt_link == club)
-        | (df.fcpython == club)
-        | (df.fivethirtyeight == club)
-    ]
-
-    season = str(season)
-
-    # Determine domain
-    match currency:
-        case "EUR":
-            domain = "https://www.transfermarkt.com"
-            signed_currency = "€"
-        case "GBP":
-            domain = "https://www.transfermarkt.co.uk"
-            signed_currency = "£"
-        case "USD":
-            domain = "https://www.transfermarkt.us"
-            signed_currency = "$"
+    if team_id is None and transfermarkt_name is False:
+        # Lookup team name
+        df = pd.read_csv(
+            "https://raw.githubusercontent.com/ian-shepherd/reus_data/main/raw-data/team_translations.csv",
+            keep_default_na=False,
+        )
+        df = df[
+            (df.fbref_name == club)
+            | (df.transfermarkt_name == club)
+            | (df.transfermarkt_link == club)
+            | (df.fcpython == club)
+            | (df.fivethirtyeight == club)
+        ]
+        club = df.transfermarkt_link.iloc[0]
+        team_id = int(df.transfermarkt.iloc[0])
 
     # Determine position group subdirectory
     match position_group:
         case "All":
             pos_group_subdir = ""
         case "Goalkeepers":
             pos_group_subdir = "Torwart"
@@ -133,40 +125,47 @@
         case "Summer":
             window_subdir = "s"
         case "Winter":
             window_subdir = "w"
 
     # Generate url
     try:
-        subdir = "/".join(
-            (
-                "saison_id",
-                season,
-                "pos",
-                pos_group_subdir,
-                "detailpos",
-                pos_subdir,
-                "w_s",
-                window_subdir,
-                "plus/1#zugaenge",
-            )
-        )
-        page = "/".join(
-            (
-                domain,
-                df.transfermarkt_link.iloc[0],
-                "transfers/verein",
-                str(df.transfermarkt.iloc[0]),
-                subdir,
-            )
-        )
+        subdir = f"saison_id/{season}/pos/{pos_group_subdir}/detailpos/{pos_subdir}/w_s/{window_subdir}/plus/1#zugaenge"
+        page = f"https://www.transfermarkt.{domain}/{club}/transfers/verein/{str(team_id)}/{subdir}"
     except IndexError:
         print("This team does not exist, please confirm spelling")
         exit()
 
+    # try:
+    #     subdir = "/".join(
+    #         (
+    #             "saison_id",
+    #             season,
+    #             "pos",
+    #             pos_group_subdir,
+    #             "detailpos",
+    #             pos_subdir,
+    #             "w_s",
+    #             window_subdir,
+    #             "plus/1#zugaenge",
+    #         )
+    #     )
+    #     page = "/".join(
+    #         (
+    #             domain,
+    #             df.transfermarkt_link.iloc[0],
+    #             "transfers/verein",
+    #             str(df.transfermarkt.iloc[0]),
+    #             subdir,
+    #         )
+    #     )
+    # except IndexError:
+    #     print("This team does not exist, please confirm spelling")
+    #     exit()
+
     pageSoup = get_page_soup_headers(page)
 
     # Find table objects
     tables = pageSoup.find_all("table", {"class": "items"})
 
     # Error handling for no transfers or non-conducive position combinations
     assert (
@@ -190,15 +189,14 @@
             table_departures = None
 
     # Generate empty list
     mylist = []
 
     # iterate over arrivals and departures
     for table in [table_arrivals, table_departures]:
-
         # error handling for no transfers
         try:
             tbody = table.find("tbody")
         except AttributeError:
             continue
 
         # determine transfer direction
@@ -208,15 +206,14 @@
             direction = "departure"
 
         # find rows
         rows = tbody.find_all("tr")
 
         # iterate through each transfer and store attributes
         for row in rows:
-
             # check if valid row
             try:
                 row_ = row["class"] not in ["odd", "even"]
             except KeyError:
                 continue
 
             # row classes
@@ -228,23 +225,25 @@
             name = row.find("img")["alt"]
             pos = row.find("td", {"class": "hauptlink"}).find_next("td").text.strip()
             age = row.find("td", {"class": "zentriert"}).text.strip()
             nation = row.find_all("td", {"class": "zentriert"})[1].find("img")["alt"]
 
             # transfer info
             mv = row.find("td", {"class": "rechts"}).text.strip()
+            mv = mv.replace("-", "0")
             transfer_club = hauptlink_class[1].text.strip()
             try:
                 transfer_club_url = hauptlink_class[1].find("a", href=True)["href"]
             except TypeError:
                 transfer_club_url = None
             transfer_league = signing_class.find_next("a", href=True).text
             transfer_league_url = signing_class.find_next("a", href=True)["href"]
             transfer_country = signing_class["alt"]
             signed_value = hauptlink_class[-1].text
+            signed_currency = signed_value[0]
 
             # value cleaning
             if "End of loan" in signed_value:
                 transfer_type = "End of loan"
                 signed_value = "0"
             elif "Loan" in signed_value:
                 transfer_type = "Loan"
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `reus-1.1.0/reus/transfermarkt/util.py` & `reus-1.1.1/reus/transfermarkt/util.py`

 * *Files 1% similar despite different names*

```diff
@@ -49,15 +49,15 @@
 
         # append dictionary to list
         mylist.append(mydict)
 
     return mylist
 
 
-def tm_format_currency(value: str):
+def tm_format_currency(value: str) -> float:
     """Helper function to convert values from string to float values
 
     Args:
         value (str): raw value of fee or market value
 
     Returns:
         float: converted value
@@ -68,10 +68,10 @@
     for c in currencies:
         value = value.replace(c, "")
 
     # Determine multiplier
     mult = 1000000 if value[-1] == "m" else 1000
 
     # Convert to float
-    value = float(value.replace("Th.", "").replace("m", "").strip()) * mult
+    value = float(value.replace("k", "").replace("m", "").strip()) * mult
 
     return value
```

### Comparing `reus-1.1.0/reus.egg-info/PKG-INFO` & `reus-1.1.1/reus.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reus
-Version: 1.1.0
+Version: 1.1.1
 Summary: A package that allows you to soccer information
 Home-page: https://github.com/ian-shepherd/reus
 Author: Ian Shepherd
 License: UNKNOWN
 Keywords: python,fbref,fotmob,transfermarkt,soccer,football
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

### Comparing `reus-1.1.0/setup.py` & `reus-1.1.1/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import setuptools
 
-VERSION = "1.1.0"
+VERSION = "1.1.1"
 DESCRIPTION = "A package that allows you to soccer information"
 LONG_DESCRIPTION = """
     A package that allows you to pull soccer statistics, player market values, and
      transfer information, primarily from FBref, Fotmob, and Transfermarkt"""
 
 setuptools.setup(
     name="reus",
```

