# Comparing `tmp/twitter_api_py-0.5.1.tar.gz` & `tmp/twitter_api_py-0.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "twitter_api_py-0.5.1.tar", max compression
+gzip compressed data, was "twitter_api_py-0.6.0.tar", max compression
```

## Comparing `twitter_api_py-0.5.1.tar` & `twitter_api_py-0.6.0.tar`

### file list

```diff
@@ -1,271 +1,271 @@
--rw-r--r--   0        0        0     1497 2023-05-03 13:16:42.851501 twitter_api_py-0.5.1/LICENSE
--rw-r--r--   0        0        0     2126 2023-05-03 13:16:42.851501 twitter_api_py-0.5.1/README.md
--rw-r--r--   0        0        0     1552 2023-05-13 06:11:03.950904 twitter_api_py-0.5.1/pyproject.toml
--rw-r--r--   0        0        0      480 2023-05-05 00:14:01.094855 twitter_api_py-0.5.1/twitter_api/__init__.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/__init__.py
--rw-r--r--   0        0        0        0 2023-04-22 10:21:01.811509 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/__init__.py
--rw-r--r--   0        0        0     1041 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_access_token_client.py
--rw-r--r--   0        0        0      311 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_access_token_mock_client.py
--rw-r--r--   0        0        0     1388 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_authorization_client.py
--rw-r--r--   0        0        0      306 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_authorization_mock_client.py
--rw-r--r--   0        0        0      808 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_request_token_client.py
--rw-r--r--   0        0        0      315 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_request_token_mock_client.py
--rw-r--r--   0        0        0     1211 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_access_token_client.py
--rw-r--r--   0        0        0      311 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_access_token_mock_client.py
--rw-r--r--   0        0        0      831 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_authorization_client.py
--rw-r--r--   0        0        0      306 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_authorization_mock_client.py
--rw-r--r--   0        0        0        0 2023-04-09 09:46:11.283030 twitter_api_py-0.5.1/twitter_api/client/oauth_session/__init__.py
--rw-r--r--   0        0        0        0 2023-04-22 10:21:01.811509 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/__init__.py
--rw-r--r--   0        0        0      365 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_access_token/__init__.py
--rw-r--r--   0        0        0     1140 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_access_token/post_oauth1_access_token.py
--rw-r--r--   0        0        0      451 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authenticate/__init__.py
--rw-r--r--   0        0        0      793 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authenticate/generate_authorization_url_oauth1_authenticate.py
--rw-r--r--   0        0        0      433 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authorize/__init__.py
--rw-r--r--   0        0        0      722 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authorize/generate_authorization_url_oauth1_authorize.py
--rw-r--r--   0        0        0      392 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_request_token/__init__.py
--rw-r--r--   0        0        0      798 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_request_token/post_oauth1_request_token.py
--rw-r--r--   0        0        0      501 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth2_authorize/__init__.py
--rw-r--r--   0        0        0      751 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth2_authorize/generate_authorization_url_oauth2_authorize.py
--rw-r--r--   0        0        0      648 2023-05-03 13:16:42.861501 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/session_resources.py
--rw-r--r--   0        0        0      376 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/v2_oauth2_token/__init__.py
--rw-r--r--   0        0        0     1596 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/v2_oauth2_token/post_v2_oauth2_token.py
--rw-r--r--   0        0        0     1793 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_mock_session.py
--rw-r--r--   0        0        0     3885 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_real_session.py
--rw-r--r--   0        0        0     1103 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_session.py
--rw-r--r--   0        0        0     1561 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_mock_session.py
--rw-r--r--   0        0        0     3397 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_real_session.py
--rw-r--r--   0        0        0      823 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_session.py
--rw-r--r--   0        0        0        0 2023-04-01 17:37:10.337565 twitter_api_py-0.5.1/twitter_api/client/request/__init__.py
--rw-r--r--   0        0        0     1577 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/request/request_async_client.py
--rw-r--r--   0        0        0      236 2023-05-12 07:40:28.123664 twitter_api_py-0.5.1/twitter_api/client/request/request_async_mock_client.py
--rw-r--r--   0        0        0     5182 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/request/request_async_real_client.py
--rw-r--r--   0        0        0     1967 2023-05-07 06:32:00.442839 twitter_api_py-0.5.1/twitter_api/client/request/request_client.py
--rw-r--r--   0        0        0     3368 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/request/request_mock_client.py
--rw-r--r--   0        0        0     7235 2023-05-07 06:32:00.442839 twitter_api_py-0.5.1/twitter_api/client/request/request_real_client.py
--rw-r--r--   0        0        0    32304 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_client.py
--rw-r--r--   0        0        0    14518 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_mock_client.py
--rw-r--r--   0        0        0    14743 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_real_client.py
--rw-r--r--   0        0        0    32063 2023-05-11 13:04:23.720798 twitter_api_py-0.5.1/twitter_api/client/twitter_api_client.py
--rw-r--r--   0        0        0    26895 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/twitter_api_mock_client.py
--rw-r--r--   0        0        0    13583 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/client/twitter_api_real_client.py
--rw-r--r--   0        0        0    10636 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/error.py
--rw-r--r--   0        0        0        0 2023-05-12 15:03:06.661543 twitter_api_py-0.5.1/twitter_api/rate_limit/__init__.py
--rw-r--r--   0        0        0      603 2023-05-12 15:04:47.555425 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/__init__.py
--rw-r--r--   0        0        0      677 2023-05-11 12:26:55.616192 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/dict_rate_limit_manager.py
--rw-r--r--   0        0        0     1233 2023-05-12 15:12:49.904443 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/dict_sleep_rate_limit_manager.py
--rw-r--r--   0        0        0        0 2023-05-10 13:38:39.016734 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/__init__.py
--rw-r--r--   0        0        0     2197 2023-05-11 11:06:16.299266 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/dict_rate_limit_checker_mixin.py
--rw-r--r--   0        0        0      618 2023-05-12 08:30:09.376371 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/raise_rate_limit_handler_mixin.py
--rw-r--r--   0        0        0     3219 2023-05-13 06:08:12.650886 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/sleep_rate_limit_handler_mixin.py
--rw-r--r--   0        0        0      840 2023-05-12 08:30:09.256372 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/no_operation_rate_limit_manager.py
--rw-r--r--   0        0        0     1358 2023-05-13 06:08:12.650886 twitter_api_py-0.5.1/twitter_api/rate_limit/manager/rate_limit_manager.py
--rw-r--r--   0        0        0     3751 2023-05-13 06:08:12.650886 twitter_api_py-0.5.1/twitter_api/rate_limit/rate_limit.py
--rw-r--r--   0        0        0      291 2023-05-02 14:52:07.203654 twitter_api_py-0.5.1/twitter_api/rate_limit/rate_limit_info.py
--rw-r--r--   0        0        0       91 2023-05-02 14:52:07.203654 twitter_api_py-0.5.1/twitter_api/rate_limit/rate_limit_target.py
--rw-r--r--   0        0        0      281 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/api_resources.py
--rw-r--r--   0        0        0      437 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/oauth2_invalidate_token/__init__.py
--rw-r--r--   0        0        0     2295 2023-05-07 06:32:00.452839 twitter_api_py-0.5.1/twitter_api/resources/oauth2_invalidate_token/post_oauth2_invalidate_token.py
--rw-r--r--   0        0        0      332 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/oauth2_token/__init__.py
--rw-r--r--   0        0        0     2187 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/oauth2_token/post_oauth2_token.py
--rw-r--r--   0        0        0      541 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversation_messages/__init__.py
--rw-r--r--   0        0        0     2316 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversation_messages/post_v2_dm_conversations_messages.py
--rw-r--r--   0        0        0      441 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations/__init__.py
--rw-r--r--   0        0        0     2164 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations/post_v2_dm_conversations.py
--rw-r--r--   0        0        0      673 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/__init__.py
--rw-r--r--   0        0        0     8867 2023-05-12 08:33:05.386154 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/get_v2_dm_conversations_with_participant_dm_events.py
--rw-r--r--   0        0        0      676 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_messages/__init__.py
--rw-r--r--   0        0        0     2390 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_messages/post_v2_dm_conversations_with_participant_messages.py
--rw-r--r--   0        0        0      429 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweet/__init__.py
--rw-r--r--   0        0        0     1438 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweet/delete_v2_tweet.py
--rw-r--r--   0        0        0     3088 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweet/get_v2_tweet.py
--rw-r--r--   0        0        0      458 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweet_retweeted_by/__init__.py
--rw-r--r--   0        0        0     6521 2023-05-12 08:33:05.676154 twitter_api_py-0.5.1/twitter_api/resources/v2_tweet_retweeted_by/get_v2_tweet_retweeted_by.py
--rw-r--r--   0        0        0      428 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets/__init__.py
--rw-r--r--   0        0        0     2977 2023-05-07 06:32:00.452839 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets/get_v2_tweets.py
--rw-r--r--   0        0        0     2926 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets/post_v2_tweets.py
--rw-r--r--   0        0        0      438 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_all/__init__.py
--rw-r--r--   0        0        0     5970 2023-05-12 08:33:05.616154 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_all/get_v2_tweets_search_all.py
--rw-r--r--   0        0        0      471 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_recent/__init__.py
--rw-r--r--   0        0        0     6069 2023-05-12 08:33:05.826154 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_recent/get_v2_tweets_search_recent.py
--rw-r--r--   0        0        0      471 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream/__init__.py
--rw-r--r--   0        0        0     3615 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream/get_v2_tweets_search_stream.py
--rw-r--r--   0        0        0      770 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/__init__.py
--rw-r--r--   0        0        0     2111 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/get_v2_tweets_search_stream_rules.py
--rw-r--r--   0        0        0     3096 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/post_v2_tweets_search_stream_rules.py
--rw-r--r--   0        0        0      275 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user/__init__.py
--rw-r--r--   0        0        0     2780 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user/get_v2_user.py
--rw-r--r--   0        0        0      371 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_followers/__init__.py
--rw-r--r--   0        0        0     6470 2023-05-12 08:33:05.506154 twitter_api_py-0.5.1/twitter_api/resources/v2_user_followers/get_v2_user_followers.py
--rw-r--r--   0        0        0      376 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_following/__init__.py
--rw-r--r--   0        0        0     1909 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_following/post_v2_user_following.py
--rw-r--r--   0        0        0      391 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_liked_tweets/__init__.py
--rw-r--r--   0        0        0     7891 2023-05-12 08:33:05.586154 twitter_api_py-0.5.1/twitter_api/resources/v2_user_liked_tweets/get_v2_user_liked_tweets.py
--rw-r--r--   0        0        0      367 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_retweets/__init__.py
--rw-r--r--   0        0        0     1911 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_retweets/post_v2_user_retweets.py
--rw-r--r--   0        0        0      331 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_user_tweets/__init__.py
--rw-r--r--   0        0        0     8304 2023-05-12 08:33:05.436154 twitter_api_py-0.5.1/twitter_api/resources/v2_user_tweets/get_v2_user_tweets.py
--rw-r--r--   0        0        0      279 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users/__init__.py
--rw-r--r--   0        0        0     2680 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users/get_v2_users.py
--rw-r--r--   0        0        0      299 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users_by/__init__.py
--rw-r--r--   0        0        0     2755 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users_by/get_v2_users_by.py
--rw-r--r--   0        0        0      396 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users_by_username/__init__.py
--rw-r--r--   0        0        0     3025 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/resources/v2_users_by_username/get_v2_users_by_username.py
--rw-r--r--   0        0        0        0 2023-04-01 17:37:01.267513 twitter_api_py-0.5.1/twitter_api/types/__init__.py
--rw-r--r--   0        0        0      386 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/_chainable.py
--rw-r--r--   0        0        0      570 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/_generic_client.py
--rw-r--r--   0        0        0     2362 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/_model.py
--rw-r--r--   0        0        0     3428 2023-05-12 08:33:05.826154 twitter_api_py-0.5.1/twitter_api/types/_paging.py
--rw-r--r--   0        0        0      697 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/comma_separatable.py
--rw-r--r--   0        0        0      234 2023-04-02 10:01:26.462016 twitter_api_py-0.5.1/twitter_api/types/endpoint.py
--rw-r--r--   0        0        0     1581 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/extra_permissive_model.py
--rw-r--r--   0        0        0      616 2023-05-07 06:17:38.693572 twitter_api_py-0.5.1/twitter_api/types/http.py
--rw-r--r--   0        0        0      734 2023-05-07 06:32:00.452839 twitter_api_py-0.5.1/twitter_api/types/httpx.py
--rw-r--r--   0        0        0     1942 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth1/__init__.py
--rw-r--r--   0        0        0     2037 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth1/oauth1_access_token.py
--rw-r--r--   0        0        0     3474 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth1/oauth1_authorization.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth2/__init__.py
--rw-r--r--   0        0        0     1975 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth2/oauth2_access_token.py
--rw-r--r--   0        0        0     3593 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/oauth2/oauth2_authorization.py
--rw-r--r--   0        0        0       63 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/pagination_token.py
--rw-r--r--   0        0        0       55 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_cashtag.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/__init__.py
--rw-r--r--   0        0        0      337 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/dm_conversation.py
--rw-r--r--   0        0        0      201 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/dm_conversation_attachment.py
--rw-r--r--   0        0        0       64 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/dm_conversation_id.py
--rw-r--r--   0        0        0      594 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/dm_conversation_message.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_event/__init__.py
--rw-r--r--   0        0        0      331 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_event/dm_event_expansion.py
--rw-r--r--   0        0        0      437 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_event/dm_event_field.py
--rw-r--r--   0        0        0       57 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_event/dm_event_id.py
--rw-r--r--   0        0        0      238 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_dm_event/dm_event_type.py
--rw-r--r--   0        0        0      338 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_domain.py
--rw-r--r--   0        0        0        0 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_entity/__init__.py
--rw-r--r--   0        0        0      286 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_entity/entity.py
--rw-r--r--   0        0        0       56 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_entity/entity_id.py
--rw-r--r--   0        0        0       58 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_entity/entity_name.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_geo/__init__.py
--rw-r--r--   0        0        0      209 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_geo/geo.py
--rw-r--r--   0        0        0       55 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_hashtag.py
--rw-r--r--   0        0        0      762 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_language.py
--rw-r--r--   0        0        0        0 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_list/__init__.py
--rw-r--r--   0        0        0       54 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_list/list_id.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/__init__.py
--rw-r--r--   0        0        0     1356 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media.py
--rw-r--r--   0        0        0      570 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_field.py
--rw-r--r--   0        0        0      100 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_id.py
--rw-r--r--   0        0        0       56 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_key.py
--rw-r--r--   0        0        0      376 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_non_public_metrics.py
--rw-r--r--   0        0        0      411 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_organic_metrics.py
--rw-r--r--   0        0        0      412 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_promoted_metrics.py
--rw-r--r--   0        0        0      190 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_public_metrics.py
--rw-r--r--   0        0        0      211 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_media/media_variants.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_place/__init__.py
--rw-r--r--   0        0        0      933 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_place/place.py
--rw-r--r--   0        0        0     2712 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_place/place_country_code.py
--rw-r--r--   0        0        0      348 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_place/place_field.py
--rw-r--r--   0        0        0       61 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_place/place_full_name.py
--rw-r--r--   0        0        0       94 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_place/place_id.py
--rw-r--r--   0        0        0       57 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_place/place_name.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_poll/__init__.py
--rw-r--r--   0        0        0      593 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_poll/poll.py
--rw-r--r--   0        0        0      272 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_poll/poll_field.py
--rw-r--r--   0        0        0       54 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_poll/poll_id.py
--rw-r--r--   0        0        0      164 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_poll/poll_option.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/__init__.py
--rw-r--r--   0        0        0     1163 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet.py
--rw-r--r--   0        0        0      392 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities.py
--rw-r--r--   0        0        0      913 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description.py
--rw-r--r--   0        0        0      237 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description_cashtag.py
--rw-r--r--   0        0        0      237 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description_hashtag.py
--rw-r--r--   0        0        0      246 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description_mention.py
--rw-r--r--   0        0        0      258 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description_url.py
--rw-r--r--   0        0        0      338 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_url.py
--rw-r--r--   0        0        0      254 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_includes.py
--rw-r--r--   0        0        0      219 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_public_metrics.py
--rw-r--r--   0        0        0      352 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_withheld.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_rule/__init__.py
--rw-r--r--   0        0        0      311 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_rule/rule.py
--rw-r--r--   0        0        0       54 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_rule/rule_id.py
--rw-r--r--   0        0        0       55 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_rule/rule_tag.py
--rw-r--r--   0        0        0     1411 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_scope.py
--rw-r--r--   0        0        0        0 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/__init__.py
--rw-r--r--   0        0        0        0 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/__init__.py
--rw-r--r--   0        0        0      873 2023-05-07 21:39:44.447272 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_and_operator.py
--rw-r--r--   0        0        0      305 2023-05-04 12:42:31.224094 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_markable_operator.py
--rw-r--r--   0        0        0      521 2023-05-07 21:38:09.546737 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_not_operator.py
--rw-r--r--   0        0        0      662 2023-05-07 21:39:53.267324 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_or_operator.py
--rw-r--r--   0        0        0      700 2023-05-07 16:28:48.589302 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/bounding_box_operator.py
--rw-r--r--   0        0        0      339 2023-05-05 14:00:53.910897 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/cashtag_operator.py
--rw-r--r--   0        0        0     1331 2023-05-05 14:00:57.340927 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/context_operator.py
--rw-r--r--   0        0        0      380 2023-05-05 14:01:01.570963 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/conversation_id_operator.py
--rw-r--r--   0        0        0      341 2023-05-05 14:01:05.470996 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/entity_operator.py
--rw-r--r--   0        0        0      424 2023-05-05 14:01:09.381029 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/from_user_operator.py
--rw-r--r--   0        0        0     1547 2023-05-08 15:42:34.966124 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/group_operator.py
--rw-r--r--   0        0        0      219 2023-05-05 13:28:23.574470 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_cashtags_operator.py
--rw-r--r--   0        0        0      209 2023-05-05 13:28:20.014444 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_geo_operator.py
--rw-r--r--   0        0        0      219 2023-05-05 13:27:22.214012 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_hashtags_operator.py
--rw-r--r--   0        0        0      215 2023-05-05 13:28:16.594433 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_images_operator.py
--rw-r--r--   0        0        0      213 2023-05-05 13:28:36.294611 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_links_operator.py
--rw-r--r--   0        0        0      213 2023-05-05 13:27:47.934228 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_media_operator.py
--rw-r--r--   0        0        0      219 2023-05-05 13:27:43.424190 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_mentions_operator.py
--rw-r--r--   0        0        0      222 2023-05-05 13:28:12.874411 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/has_video_link_operator.py
--rw-r--r--   0        0        0      339 2023-05-05 14:01:12.611056 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/hashtag_operator.py
--rw-r--r--   0        0        0      349 2023-05-05 14:01:16.081086 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/in_reply_to_tweet_id_operator.py
--rw-r--r--   0        0        0      442 2023-05-05 00:14:01.104855 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/is_nullcast_operator.py
--rw-r--r--   0        0        0      211 2023-05-05 13:27:39.924161 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/is_quote_operator.py
--rw-r--r--   0        0        0      211 2023-05-05 13:28:08.404378 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/is_reply_operator.py
--rw-r--r--   0        0        0      215 2023-05-05 13:27:35.034120 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/is_retweet_operator.py
--rw-r--r--   0        0        0      217 2023-05-05 13:28:03.544340 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/is_verified_operator.py
--rw-r--r--   0        0        0      416 2023-05-05 14:00:42.330799 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/keyword_operator.py
--rw-r--r--   0        0        0      339 2023-05-05 13:27:31.434090 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/lang_operator.py
--rw-r--r--   0        0        0      317 2023-05-05 14:01:22.251139 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/list_operator.py
--rw-r--r--   0        0        0      349 2023-05-05 14:00:34.930737 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/mention_operator.py
--rw-r--r--   0        0        0     2648 2023-05-07 21:39:35.247220 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/operator.py
--rw-r--r--   0        0        0      370 2023-05-05 14:01:25.541167 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/place_country_operator.py
--rw-r--r--   0        0        0      544 2023-05-05 14:01:31.431217 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/place_operator.py
--rw-r--r--   0        0        0     1298 2023-05-07 16:29:28.619549 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/point_radius_operator.py
--rw-r--r--   0        0        0      354 2023-05-05 14:01:45.811339 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/quotes_of_tweet_id_operator.py
--rw-r--r--   0        0        0      433 2023-05-08 03:59:00.708178 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/retweets_of_operator.py
--rw-r--r--   0        0        0      350 2023-05-05 14:01:57.361437 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/retweets_of_tweet_id_operator.py
--rw-r--r--   0        0        0      420 2023-05-05 14:02:00.741466 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/to_user_operator.py
--rw-r--r--   0        0        0      262 2023-05-05 14:02:03.911493 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/url_operator.py
--rw-r--r--   0        0        0     2494 2023-05-08 15:45:30.406136 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/search_query.py
--rw-r--r--   0        0        0    14352 2023-05-08 15:47:57.376115 twitter_api_py-0.5.1/twitter_api/types/v2_search_query/serch_query_builder.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/__init__.py
--rw-r--r--   0        0        0     7856 2023-05-04 12:42:31.234094 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet.py
--rw-r--r--   0        0        0      309 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_attachments.py
--rw-r--r--   0        0        0      267 2023-05-04 12:42:31.234094 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_context_annotation.py
--rw-r--r--   0        0        0      314 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_edit_controls.py
--rw-r--r--   0        0        0      720 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities.py
--rw-r--r--   0        0        0      333 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities_annotation.py
--rw-r--r--   0        0        0      247 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities_cashtag.py
--rw-r--r--   0        0        0      247 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities_hashtag.py
--rw-r--r--   0        0        0      313 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities_mention.py
--rw-r--r--   0        0        0      415 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities_url.py
--rw-r--r--   0        0        0      632 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_expansion.py
--rw-r--r--   0        0        0     1910 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_field.py
--rw-r--r--   0        0        0      288 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_geo.py
--rw-r--r--   0        0        0      231 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_geo_coordinates.py
--rw-r--r--   0        0        0      100 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_id.py
--rw-r--r--   0        0        0      287 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_non_public_metrics.py
--rw-r--r--   0        0        0      285 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_organic_metrics.py
--rw-r--r--   0        0        0      286 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_promoted_metrics.py
--rw-r--r--   0        0        0      437 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_public_metrics.py
--rw-r--r--   0        0        0      256 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_referenced_tweet.py
--rw-r--r--   0        0        0     7050 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_response_body.py
--rw-r--r--   0        0        0      387 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_withheld.py
--rw-r--r--   0        0        0        0 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/__init__.py
--rw-r--r--   0        0        0      969 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/user.py
--rw-r--r--   0        0        0      157 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/user_expantion.py
--rw-r--r--   0        0        0      608 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/user_field.py
--rw-r--r--   0        0        0       54 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/user_id.py
--rw-r--r--   0        0        0       97 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/user_verified_type.py
--rw-r--r--   0        0        0      128 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/types/v2_user/username.py
--rw-r--r--   0        0        0        0 2023-04-01 09:17:10.085603 twitter_api_py-0.5.1/twitter_api/utils/__init__.py
--rw-r--r--   0        0        0      123 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/utils/_datetime.py
--rw-r--r--   0        0        0      716 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/utils/_functional.py
--rw-r--r--   0        0        0      904 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/utils/_oauth.py
--rw-r--r--   0        0        0      790 2023-05-05 00:14:01.104855 twitter_api_py-0.5.1/twitter_api/utils/json.py
--rw-r--r--   0        0        0      630 2023-05-03 13:16:42.871502 twitter_api_py-0.5.1/twitter_api/warning.py
--rw-r--r--   0        0        0     3073 1970-01-01 00:00:00.000000 twitter_api_py-0.5.1/PKG-INFO
+-rw-r--r--   0        0        0     1497 2023-05-13 19:29:28.558751 twitter_api_py-0.6.0/LICENSE
+-rw-r--r--   0        0        0     2126 2023-05-13 19:29:28.558751 twitter_api_py-0.6.0/README.md
+-rw-r--r--   0        0        0     1724 2023-05-13 19:29:28.598751 twitter_api_py-0.6.0/pyproject.toml
+-rw-r--r--   0        0        0      480 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/__init__.py
+-rw-r--r--   0        0        0     1041 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_access_token_client.py
+-rw-r--r--   0        0        0      311 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_access_token_mock_client.py
+-rw-r--r--   0        0        0     1388 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_authorization_client.py
+-rw-r--r--   0        0        0      306 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_authorization_mock_client.py
+-rw-r--r--   0        0        0      808 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_request_token_client.py
+-rw-r--r--   0        0        0      315 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_request_token_mock_client.py
+-rw-r--r--   0        0        0     1211 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_access_token_client.py
+-rw-r--r--   0        0        0      311 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_access_token_mock_client.py
+-rw-r--r--   0        0        0      831 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_authorization_client.py
+-rw-r--r--   0        0        0      306 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_authorization_mock_client.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/__init__.py
+-rw-r--r--   0        0        0      365 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_access_token/__init__.py
+-rw-r--r--   0        0        0     1140 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_access_token/post_oauth1_access_token.py
+-rw-r--r--   0        0        0      451 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authenticate/__init__.py
+-rw-r--r--   0        0        0      793 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authenticate/generate_authorization_url_oauth1_authenticate.py
+-rw-r--r--   0        0        0      433 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authorize/__init__.py
+-rw-r--r--   0        0        0      722 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authorize/generate_authorization_url_oauth1_authorize.py
+-rw-r--r--   0        0        0      392 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_request_token/__init__.py
+-rw-r--r--   0        0        0      798 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_request_token/post_oauth1_request_token.py
+-rw-r--r--   0        0        0      501 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth2_authorize/__init__.py
+-rw-r--r--   0        0        0      751 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth2_authorize/generate_authorization_url_oauth2_authorize.py
+-rw-r--r--   0        0        0      648 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/session_resources.py
+-rw-r--r--   0        0        0      357 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/v2_oauth2_token/__init__.py
+-rw-r--r--   0        0        0     1596 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/v2_oauth2_token/post_v2_oauth2_token.py
+-rw-r--r--   0        0        0     1875 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_mock_session.py
+-rw-r--r--   0        0        0     3966 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_real_session.py
+-rw-r--r--   0        0        0     1103 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_session.py
+-rw-r--r--   0        0        0     1629 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_mock_session.py
+-rw-r--r--   0        0        0     3464 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_real_session.py
+-rw-r--r--   0        0        0      823 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_session.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/__init__.py
+-rw-r--r--   0        0        0     1375 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_async_client.py
+-rw-r--r--   0        0        0      458 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_async_mock_client.py
+-rw-r--r--   0        0        0     5306 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_async_real_client.py
+-rw-r--r--   0        0        0     1786 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_client.py
+-rw-r--r--   0        0        0     3673 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_mock_client.py
+-rw-r--r--   0        0        0     7358 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/request/request_real_client.py
+-rw-r--r--   0        0        0    32334 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_client.py
+-rw-r--r--   0        0        0    14712 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_mock_client.py
+-rw-r--r--   0        0        0    14927 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_real_client.py
+-rw-r--r--   0        0        0    32093 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_client.py
+-rw-r--r--   0        0        0    27089 2023-05-13 19:29:28.622751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_mock_client.py
+-rw-r--r--   0        0        0    13734 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/client/twitter_api_real_client.py
+-rw-r--r--   0        0        0    10801 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/error.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/__init__.py
+-rw-r--r--   0        0        0      603 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/__init__.py
+-rw-r--r--   0        0        0      677 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/dict_rate_limit_manager.py
+-rw-r--r--   0        0        0     1301 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/dict_sleep_rate_limit_manager.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/__init__.py
+-rw-r--r--   0        0        0     2251 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/dict_rate_limit_checker_mixin.py
+-rw-r--r--   0        0        0      672 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/raise_rate_limit_handler_mixin.py
+-rw-r--r--   0        0        0     3287 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/sleep_rate_limit_handler_mixin.py
+-rw-r--r--   0        0        0      908 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/no_operation_rate_limit_manager.py
+-rw-r--r--   0        0        0     1358 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/manager/rate_limit_manager.py
+-rw-r--r--   0        0        0     3751 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/rate_limit.py
+-rw-r--r--   0        0        0      291 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/rate_limit_info.py
+-rw-r--r--   0        0        0      102 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/rate_limit/rate_limit_target.py
+-rw-r--r--   0        0        0      281 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/api_resources.py
+-rw-r--r--   0        0        0      437 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/oauth2_invalidate_token/__init__.py
+-rw-r--r--   0        0        0     2331 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/oauth2_invalidate_token/post_oauth2_invalidate_token.py
+-rw-r--r--   0        0        0      332 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/oauth2_token/__init__.py
+-rw-r--r--   0        0        0     2223 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/oauth2_token/post_oauth2_token.py
+-rw-r--r--   0        0        0      522 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversation_messages/__init__.py
+-rw-r--r--   0        0        0     2370 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversation_messages/post_v2_dm_conversations_messages.py
+-rw-r--r--   0        0        0      422 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations/__init__.py
+-rw-r--r--   0        0        0     2199 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations/post_v2_dm_conversations.py
+-rw-r--r--   0        0        0      654 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/__init__.py
+-rw-r--r--   0        0        0     8948 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/get_v2_dm_conversations_with_participant_dm_events.py
+-rw-r--r--   0        0        0      657 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_messages/__init__.py
+-rw-r--r--   0        0        0     2444 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_messages/post_v2_dm_conversations_with_participant_messages.py
+-rw-r--r--   0        0        0      429 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweet/__init__.py
+-rw-r--r--   0        0        0     1492 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweet/delete_v2_tweet.py
+-rw-r--r--   0        0        0     3142 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweet/get_v2_tweet.py
+-rw-r--r--   0        0        0      439 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweet_retweeted_by/__init__.py
+-rw-r--r--   0        0        0     6602 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweet_retweeted_by/get_v2_tweet_retweeted_by.py
+-rw-r--r--   0        0        0      428 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets/__init__.py
+-rw-r--r--   0        0        0     3007 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets/get_v2_tweets.py
+-rw-r--r--   0        0        0     2956 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets/post_v2_tweets.py
+-rw-r--r--   0        0        0      419 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_all/__init__.py
+-rw-r--r--   0        0        0     6019 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_all/get_v2_tweets_search_all.py
+-rw-r--r--   0        0        0      452 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_recent/__init__.py
+-rw-r--r--   0        0        0     6118 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_recent/get_v2_tweets_search_recent.py
+-rw-r--r--   0        0        0      452 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream/__init__.py
+-rw-r--r--   0        0        0     3669 2023-05-13 19:29:28.626751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream/get_v2_tweets_search_stream.py
+-rw-r--r--   0        0        0      751 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/__init__.py
+-rw-r--r--   0        0        0     2164 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/get_v2_tweets_search_stream_rules.py
+-rw-r--r--   0        0        0     3149 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/post_v2_tweets_search_stream_rules.py
+-rw-r--r--   0        0        0      275 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user/__init__.py
+-rw-r--r--   0        0        0     2833 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user/get_v2_user.py
+-rw-r--r--   0        0        0      371 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_followers/__init__.py
+-rw-r--r--   0        0        0     6551 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_followers/get_v2_user_followers.py
+-rw-r--r--   0        0        0      376 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_following/__init__.py
+-rw-r--r--   0        0        0     1944 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_following/post_v2_user_following.py
+-rw-r--r--   0        0        0      391 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_liked_tweets/__init__.py
+-rw-r--r--   0        0        0     7972 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_liked_tweets/get_v2_user_liked_tweets.py
+-rw-r--r--   0        0        0      367 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_retweets/__init__.py
+-rw-r--r--   0        0        0     1946 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_retweets/post_v2_user_retweets.py
+-rw-r--r--   0        0        0      331 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_tweets/__init__.py
+-rw-r--r--   0        0        0     8381 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_user_tweets/get_v2_user_tweets.py
+-rw-r--r--   0        0        0      279 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users/__init__.py
+-rw-r--r--   0        0        0     2733 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users/get_v2_users.py
+-rw-r--r--   0        0        0      299 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users_by/__init__.py
+-rw-r--r--   0        0        0     2808 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users_by/get_v2_users_by.py
+-rw-r--r--   0        0        0      396 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users_by_username/__init__.py
+-rw-r--r--   0        0        0     3078 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/resources/v2_users_by_username/get_v2_users_by_username.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/__init__.py
+-rw-r--r--   0        0        0      397 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/_chainable.py
+-rw-r--r--   0        0        0      570 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/_generic_client.py
+-rw-r--r--   0        0        0     2362 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/_model.py
+-rw-r--r--   0        0        0     3413 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/_paging.py
+-rw-r--r--   0        0        0      727 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/comma_separatable.py
+-rw-r--r--   0        0        0      234 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/endpoint.py
+-rw-r--r--   0        0        0     1581 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/extra_permissive_model.py
+-rw-r--r--   0        0        0      645 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/http.py
+-rw-r--r--   0        0        0      744 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/httpx.py
+-rw-r--r--   0        0        0     1971 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth1/__init__.py
+-rw-r--r--   0        0        0     2037 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth1/oauth1_access_token.py
+-rw-r--r--   0        0        0     3474 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth1/oauth1_authorization.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth2/__init__.py
+-rw-r--r--   0        0        0     1975 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth2/oauth2_access_token.py
+-rw-r--r--   0        0        0     3593 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/oauth2/oauth2_authorization.py
+-rw-r--r--   0        0        0       74 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/pagination_token.py
+-rw-r--r--   0        0        0       66 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_cashtag.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/__init__.py
+-rw-r--r--   0        0        0      337 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/dm_conversation.py
+-rw-r--r--   0        0        0      212 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/dm_conversation_attachment.py
+-rw-r--r--   0        0        0       75 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/dm_conversation_id.py
+-rw-r--r--   0        0        0      624 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/dm_conversation_message.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_event/__init__.py
+-rw-r--r--   0        0        0      342 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_event/dm_event_expansion.py
+-rw-r--r--   0        0        0      437 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_event/dm_event_field.py
+-rw-r--r--   0        0        0       68 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_event/dm_event_id.py
+-rw-r--r--   0        0        0      238 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_dm_event/dm_event_type.py
+-rw-r--r--   0        0        0      368 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_domain.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_entity/__init__.py
+-rw-r--r--   0        0        0      286 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_entity/entity.py
+-rw-r--r--   0        0        0       67 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_entity/entity_id.py
+-rw-r--r--   0        0        0       69 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_entity/entity_name.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_geo/__init__.py
+-rw-r--r--   0        0        0      209 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_geo/geo.py
+-rw-r--r--   0        0        0       66 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_hashtag.py
+-rw-r--r--   0        0        0      762 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_language.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_list/__init__.py
+-rw-r--r--   0        0        0       65 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_list/list_id.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/__init__.py
+-rw-r--r--   0        0        0     1356 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media.py
+-rw-r--r--   0        0        0      570 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_field.py
+-rw-r--r--   0        0        0      111 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_id.py
+-rw-r--r--   0        0        0       67 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_key.py
+-rw-r--r--   0        0        0      376 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_non_public_metrics.py
+-rw-r--r--   0        0        0      411 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_organic_metrics.py
+-rw-r--r--   0        0        0      412 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_promoted_metrics.py
+-rw-r--r--   0        0        0      190 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_public_metrics.py
+-rw-r--r--   0        0        0      211 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_media/media_variants.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/__init__.py
+-rw-r--r--   0        0        0      933 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place.py
+-rw-r--r--   0        0        0     2712 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place_country_code.py
+-rw-r--r--   0        0        0      348 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place_field.py
+-rw-r--r--   0        0        0       72 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place_full_name.py
+-rw-r--r--   0        0        0      105 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place_id.py
+-rw-r--r--   0        0        0       68 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_place/place_name.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_poll/__init__.py
+-rw-r--r--   0        0        0      593 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_poll/poll.py
+-rw-r--r--   0        0        0      272 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_poll/poll_field.py
+-rw-r--r--   0        0        0       65 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_poll/poll_id.py
+-rw-r--r--   0        0        0      164 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_poll/poll_option.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/__init__.py
+-rw-r--r--   0        0        0     1163 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet.py
+-rw-r--r--   0        0        0      392 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities.py
+-rw-r--r--   0        0        0      913 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description.py
+-rw-r--r--   0        0        0      237 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description_cashtag.py
+-rw-r--r--   0        0        0      237 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description_hashtag.py
+-rw-r--r--   0        0        0      246 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description_mention.py
+-rw-r--r--   0        0        0      258 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description_url.py
+-rw-r--r--   0        0        0      338 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_url.py
+-rw-r--r--   0        0        0      254 2023-05-13 19:29:28.630751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_includes.py
+-rw-r--r--   0        0        0      219 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_public_metrics.py
+-rw-r--r--   0        0        0      352 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_withheld.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_rule/__init__.py
+-rw-r--r--   0        0        0      311 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_rule/rule.py
+-rw-r--r--   0        0        0       65 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_rule/rule_id.py
+-rw-r--r--   0        0        0       66 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_rule/rule_tag.py
+-rw-r--r--   0        0        0     1411 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_scope.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/__init__.py
+-rw-r--r--   0        0        0      873 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_and_operator.py
+-rw-r--r--   0        0        0      305 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_markable_operator.py
+-rw-r--r--   0        0        0      521 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_not_operator.py
+-rw-r--r--   0        0        0      662 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_or_operator.py
+-rw-r--r--   0        0        0      700 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/bounding_box_operator.py
+-rw-r--r--   0        0        0      339 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/cashtag_operator.py
+-rw-r--r--   0        0        0     1331 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/context_operator.py
+-rw-r--r--   0        0        0      380 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/conversation_id_operator.py
+-rw-r--r--   0        0        0      341 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/entity_operator.py
+-rw-r--r--   0        0        0      424 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/from_user_operator.py
+-rw-r--r--   0        0        0     1547 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/group_operator.py
+-rw-r--r--   0        0        0      219 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_cashtags_operator.py
+-rw-r--r--   0        0        0      209 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_geo_operator.py
+-rw-r--r--   0        0        0      219 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_hashtags_operator.py
+-rw-r--r--   0        0        0      215 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_images_operator.py
+-rw-r--r--   0        0        0      213 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_links_operator.py
+-rw-r--r--   0        0        0      213 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_media_operator.py
+-rw-r--r--   0        0        0      219 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_mentions_operator.py
+-rw-r--r--   0        0        0      222 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/has_video_link_operator.py
+-rw-r--r--   0        0        0      339 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/hashtag_operator.py
+-rw-r--r--   0        0        0      349 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/in_reply_to_tweet_id_operator.py
+-rw-r--r--   0        0        0      442 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/is_nullcast_operator.py
+-rw-r--r--   0        0        0      211 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/is_quote_operator.py
+-rw-r--r--   0        0        0      211 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/is_reply_operator.py
+-rw-r--r--   0        0        0      215 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/is_retweet_operator.py
+-rw-r--r--   0        0        0      217 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/is_verified_operator.py
+-rw-r--r--   0        0        0      416 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/keyword_operator.py
+-rw-r--r--   0        0        0      339 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/lang_operator.py
+-rw-r--r--   0        0        0      317 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/list_operator.py
+-rw-r--r--   0        0        0      349 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/mention_operator.py
+-rw-r--r--   0        0        0     2648 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/operator.py
+-rw-r--r--   0        0        0      370 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/place_country_operator.py
+-rw-r--r--   0        0        0      544 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/place_operator.py
+-rw-r--r--   0        0        0     1298 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/point_radius_operator.py
+-rw-r--r--   0        0        0      354 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/quotes_of_tweet_id_operator.py
+-rw-r--r--   0        0        0      433 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/retweets_of_operator.py
+-rw-r--r--   0        0        0      350 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/retweets_of_tweet_id_operator.py
+-rw-r--r--   0        0        0      420 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/to_user_operator.py
+-rw-r--r--   0        0        0      262 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/url_operator.py
+-rw-r--r--   0        0        0     2494 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/search_query.py
+-rw-r--r--   0        0        0    14382 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_search_query/serch_query_builder.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/__init__.py
+-rw-r--r--   0        0        0     7856 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet.py
+-rw-r--r--   0        0        0      309 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_attachments.py
+-rw-r--r--   0        0        0      267 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_context_annotation.py
+-rw-r--r--   0        0        0      314 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_edit_controls.py
+-rw-r--r--   0        0        0      720 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities.py
+-rw-r--r--   0        0        0      333 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities_annotation.py
+-rw-r--r--   0        0        0      247 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities_cashtag.py
+-rw-r--r--   0        0        0      247 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities_hashtag.py
+-rw-r--r--   0        0        0      313 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities_mention.py
+-rw-r--r--   0        0        0      415 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities_url.py
+-rw-r--r--   0        0        0      643 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_expansion.py
+-rw-r--r--   0        0        0     1910 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_field.py
+-rw-r--r--   0        0        0      288 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_geo.py
+-rw-r--r--   0        0        0      231 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_geo_coordinates.py
+-rw-r--r--   0        0        0      111 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_id.py
+-rw-r--r--   0        0        0      287 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_non_public_metrics.py
+-rw-r--r--   0        0        0      285 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_organic_metrics.py
+-rw-r--r--   0        0        0      286 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_promoted_metrics.py
+-rw-r--r--   0        0        0      437 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_public_metrics.py
+-rw-r--r--   0        0        0      256 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_referenced_tweet.py
+-rw-r--r--   0        0        0     7079 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_response_body.py
+-rw-r--r--   0        0        0      387 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_withheld.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/__init__.py
+-rw-r--r--   0        0        0      969 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/user.py
+-rw-r--r--   0        0        0      168 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/user_expantion.py
+-rw-r--r--   0        0        0      608 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/user_field.py
+-rw-r--r--   0        0        0       65 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/user_id.py
+-rw-r--r--   0        0        0       97 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/user_verified_type.py
+-rw-r--r--   0        0        0      139 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/types/v2_user/username.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/utils/__init__.py
+-rw-r--r--   0        0        0      123 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/utils/_datetime.py
+-rw-r--r--   0        0        0      716 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/utils/_functional.py
+-rw-r--r--   0        0        0      904 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/utils/_oauth.py
+-rw-r--r--   0        0        0      790 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/utils/json.py
+-rw-r--r--   0        0        0      630 2023-05-13 19:29:28.634751 twitter_api_py-0.6.0/twitter_api/warning.py
+-rw-r--r--   0        0        0     3376 1970-01-01 00:00:00.000000 twitter_api_py-0.6.0/PKG-INFO
```

### Comparing `twitter_api_py-0.5.1/LICENSE` & `twitter_api_py-0.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/README.md` & `twitter_api_py-0.6.0/README.md`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/pyproject.toml` & `twitter_api_py-0.6.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,36 +1,40 @@
 [tool.poetry]
 authors = ["yassun4dev <yassun4dev@outlook.com>"]
 description = "Twitter API Client by Typed Python."
 name = "twitter-api-py"
 packages = [{include = "twitter_api"}]
 readme = "README.md"
-version = "0.5.1"
+version = "0.6.0"
 license = "BSD-3-Clause"
 repository = "https://github.com/yassun4dev/twitter-api-py"
 classifiers = [
     "Development Status :: 4 - Beta",
     "Topic :: Software Development :: Libraries",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: BSD License",
     "Programming Language :: Python :: 3",
+    "Programming Language :: Python :: 3.8",
+    "Programming Language :: Python :: 3.9",
+    "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11",
     "Programming Language :: Python :: 3 :: Only",
 ]
 
 [tool.taskipy.tasks]
 test = "pytest"
 format = "black --target-version py310 ."
 lint = "PYRIGHT_PYTHON_FORCE_VERSION=latest pyright twitter_api/** tests/** examples/**"
 
 [tool.poetry.dependencies]
-python = "^3.11"
+python = ">=3.8.1,<4.0"
 pydantic = "^1.10.7"
 authlib = "^1.2.0"
 httpx = "^0.24.0"
+typing-extensions = "^4.5.0"
 
 [tool.poetry.group.dev.dependencies]
 flake8 = "^6.0.0"
 black = "^23.1.0"
 isort = "^5.12.0"
 pytest = "^7.2.2"
 pyright = "^1.1.300"
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_access_token_client.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_access_token_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_authorization_client.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_authorization_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth1_request_token_client.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth1_request_token_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_access_token_client.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_access_token_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_flow/twitter_oauth2_authorization_client.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_flow/twitter_oauth2_authorization_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_access_token/post_oauth1_access_token.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_access_token/post_oauth1_access_token.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authenticate/generate_authorization_url_oauth1_authenticate.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authenticate/generate_authorization_url_oauth1_authenticate.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_authorize/generate_authorization_url_oauth1_authorize.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_authorize/generate_authorization_url_oauth1_authorize.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth1_request_token/post_oauth1_request_token.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth1_request_token/post_oauth1_request_token.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/oauth2_authorize/generate_authorization_url_oauth2_authorize.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/oauth2_authorize/generate_authorization_url_oauth2_authorize.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/session_resources.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/session_resources.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/resources/v2_oauth2_token/post_v2_oauth2_token.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/resources/v2_oauth2_token/post_v2_oauth2_token.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_mock_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_mock_session.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 from typing import Callable, Union
 
+from typing_extensions import override
+
 from twitter_api.client.oauth_flow.twitter_oauth1_authorization_client import (
     TwitterOAuth1AuthorizeClient,
 )
 from twitter_api.client.oauth_session.resources.oauth1_authenticate import (
     OauthAuth1enticateUrl,
 )
 from twitter_api.client.oauth_session.resources.oauth1_authorize import (
@@ -19,28 +21,31 @@
         self,
         client_generator: Callable[
             [AccessToken, AccessSecret], TwitterApiGenericMockClient
         ],
     ) -> None:
         self._client_generator = client_generator
 
+    @override
     def request_token(self) -> TwitterOAuth1AuthorizeClient:
         return TwitterOAuth1AuthorizeClient(session=self)
 
+    @override
     def generate_authorization_url(
         self,
         url: Union[OauthAuth1enticateUrl, Oauth1AuthorizeUrl],
     ):
         from twitter_api.types.oauth1.oauth1_authorization import OAuth1Authorization
 
         return OAuth1Authorization(
             authorization_url="https://authorization.url.com",
             session=self,
         )
 
+    @override
     def fetch_token(
         self,
         authorization_response_url: CallbackUrl,
     ):
         from twitter_api.types.oauth1.oauth1_access_token import OAuth1AccessToken
 
         return OAuth1AccessToken(
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_real_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_real_session.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from typing import Callable, Mapping, Optional, Union
 
 from authlib.integrations.httpx_client.oauth1_client import OAuth1Client
+from typing_extensions import override
 
 from twitter_api.client.oauth_flow.twitter_oauth1_authorization_client import (
     TwitterOAuth1AuthorizeClient,
 )
 from twitter_api.client.oauth_session.resources.oauth1_access_token import (
     Oauth1AccessTokenUrl,
 )
@@ -68,30 +69,33 @@
         self._limits = limits
         self._mounts = mounts
         self._proxies = proxies
         self._timeout = timeout
         self._transport = transport
         self._verify = verify
 
+    @override
     def request_token(self) -> TwitterOAuth1AuthorizeClient[TwitterApiGenericClient]:
         url: Oauth1RequestTokenUrl = "https://api.twitter.com/oauth/request_token"
 
         self._session.fetch_request_token(url)
 
         return TwitterOAuth1AuthorizeClient(session=self)
 
+    @override
     def generate_authorization_url(
         self,
         url: Union[OauthAuth1enticateUrl, Oauth1AuthorizeUrl],
     ) -> OAuth1Authorization[TwitterApiGenericClient]:
         return OAuth1Authorization(
             authorization_url=self._session.create_authorization_url(url),
             session=self,
         )
 
+    @override
     def fetch_token(
         self,
         authorization_response_url: CallbackUrl,
     ) -> OAuth1AccessToken[TwitterApiGenericClient]:
         url: Oauth1AccessTokenUrl = "https://api.twitter.com/oauth/access_token"
 
         self._session.parse_authorization_response(authorization_response_url)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth1_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth1_session.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_mock_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_mock_session.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 from datetime import datetime
 from typing import Callable
 
+from typing_extensions import override
+
 from twitter_api.client.oauth_session.twitter_oauth2_session import TwitterOAuth2Session
 from twitter_api.types._generic_client import TwitterApiGenericMockClient
 from twitter_api.types.oauth import AccessToken, CallbackUrl
 from twitter_api.types.oauth2.oauth2_access_token import OAuth2AccessToken
 from twitter_api.types.v2_scope import Scope
 
 
@@ -14,24 +16,26 @@
         client_generator: Callable[[AccessToken], TwitterApiGenericMockClient],
         *,
         scope: list[Scope],
     ) -> None:
         self._client_generator = client_generator
         self._scope = scope
 
+    @override
     def generate_authorization_url(self):
         from twitter_api.types.oauth2.oauth2_authorization import OAuth2Authorization
 
         return OAuth2Authorization(
             authorization_url="https://authorization.url.com",
             state="state",
             code_verifier="code_verifier",
             session=self,
         )
 
+    @override
     def fetch_token(
         self,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
     ) -> OAuth2AccessToken:
         expires_in = 7200
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_real_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_real_session.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import Any, Callable, Generic, Mapping, Optional
+from typing import Callable, Generic, Mapping, Optional
 
 from authlib.integrations.httpx_client.oauth2_client import OAuth2Client
+from typing_extensions import Any, override
 
 from twitter_api.client.oauth_session.resources.oauth2_authorize import (
     Oauth2AuthorizeUrl,
 )
 from twitter_api.client.oauth_session.resources.v2_oauth2_token import V2Oauth2TokenUrl
 from twitter_api.client.oauth_session.twitter_oauth2_session import TwitterOAuth2Session
 from twitter_api.types import httpx
@@ -45,14 +46,15 @@
             mounts=mounts,
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
+    @override
     def generate_authorization_url(
         self,
     ) -> OAuth2Authorization[TwitterApiGenericClient]:
         url: Oauth2AuthorizeUrl = "https://twitter.com/i/oauth2/authorize"
         code_verifier = generate_code_verifier()
 
         authorization_url, state = self._session.create_authorization_url(
@@ -62,14 +64,15 @@
         return OAuth2Authorization(
             authorization_url=authorization_url,
             state=state,
             code_verifier=code_verifier,
             session=self,
         )
 
+    @override
     def fetch_token(
         self,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
     ) -> OAuth2AccessToken[TwitterApiGenericClient]:
         url: V2Oauth2TokenUrl = "https://api.twitter.com/2/oauth2/token"
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/oauth_session/twitter_oauth2_session.py` & `twitter_api_py-0.6.0/twitter_api/client/oauth_session/twitter_oauth2_session.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/client/request/request_async_client.py` & `twitter_api_py-0.6.0/twitter_api/client/request/request_async_client.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from abc import abstractmethod
-from typing import Optional, Self, Type
+from typing import Optional, Type
 
 from twitter_api.client.request.request_client import RequestClient
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.http import (
     Headers,
     QuryParameters,
     RequestJsonBody,
@@ -47,16 +47,7 @@
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
         headers: Optional[Headers] = None,
         query: Optional[QuryParameters] = None,
     ) -> ResponseModelBody:
         ...
-
-    async def aclose(self) -> None:
-        pass
-
-    async def __aenter__(self) -> Self:
-        return self
-
-    async def __aexit__(self, exc_type, exc_value, traceback) -> None:
-        pass
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/request/request_async_real_client.py` & `twitter_api_py-0.6.0/twitter_api/client/request/request_async_real_client.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Mapping, Optional, Self, Type
+from typing import Mapping, Optional
+
+from typing_extensions import Self, Type, override
 
 from twitter_api.client.request.request_async_client import RequestAsyncClient
 from twitter_api.client.request.request_real_client import (
     _parse_response,
     _remove_none_field,
 )
 from twitter_api.rate_limit.manager.no_operation_rate_limit_manager import (
@@ -53,25 +55,29 @@
 
         if rate_limit_manager is None:
             rate_limit_manager = NoOperationRateLimitManager()
 
         self._rate_limit_manager = rate_limit_manager
 
     @property
+    @override
     def oauth_version(self) -> OAuthVersion:
         return self._oauth_version
 
     @property
+    @override
     def rate_limit_target(self) -> RateLimitTarget:
         return self._rate_limit_target
 
     @property
+    @override
     def rate_limit_manager(self) -> RateLimitManager:
         return self._rate_limit_manager
 
+    @override
     async def get(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
@@ -94,14 +100,15 @@
             response_body_type,
             url,
             headers,
             query,
             body,
         )
 
+    @override
     async def post(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
@@ -126,14 +133,15 @@
             response_body_type,
             url,
             headers,
             query,
             body,
         )
 
+    @override
     async def delete(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/request/request_mock_client.py` & `twitter_api_py-0.6.0/twitter_api/client/request/request_mock_client.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Generic, Optional, Type, Union
+from typing import Generic, Optional, Union
+
+from typing_extensions import Self, Type, override
 
 from twitter_api.error import (
     MockInjectionResponseWrong,
     MockResponseNotFound,
     TwitterApiError,
 )
 from twitter_api.rate_limit.manager.no_operation_rate_limit_manager import (
@@ -39,22 +41,25 @@
 
         if rate_limit_manager is None:
             rate_limit_manager = NoOperationRateLimitManager()
 
         self._rate_limit_manager = rate_limit_manager
 
     @property
+    @override
     def oauth_version(self) -> OAuthVersion:
         return self._oauth_version
 
     @property
+    @override
     def rate_limit_target(self) -> RateLimitTarget:
         return self._rate_limit_target
 
     @property
+    @override
     def rate_limit_manager(self) -> RateLimitManager:
         return self._rate_limit_manager
 
     def inject_response_body(
         self,
         endpoint: Endpoint,
         response_body: Union[ResponseModelBody, TwitterApiError],
@@ -71,42 +76,54 @@
             raise MockInjectionResponseWrong(endpoint, expected_endpoint)
 
         if isinstance(response_body, TwitterApiError):
             raise response_body
 
         return response_body
 
+    @override
     def get(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
         query: Optional[QuryParameters] = None,
     ) -> ResponseModelBody:
         return self._extract_response_body(endpoint)
 
+    @override
     def post(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
         headers: Optional[Headers] = None,
         query: Optional[QuryParameters] = None,
         body: Optional[RequestJsonBody] = None,
     ) -> ResponseModelBody:
         return self._extract_response_body(endpoint)
 
+    @override
     def delete(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
         headers: Optional[Headers] = None,
         query: Optional[QuryParameters] = None,
     ) -> ResponseModelBody:
         return self._extract_response_body(endpoint)
+
+    def close(self) -> None:
+        pass
+
+    def __enter__(self) -> Self:
+        return self
+
+    def __exit__(self, exc_type, exc_value, traceback) -> None:
+        pass
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/request/request_real_client.py` & `twitter_api_py-0.6.0/twitter_api/client/request/request_real_client.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import Mapping, Optional, Self, Type
+from typing import Mapping, Optional
 
 import pydantic
+from typing_extensions import Self, Type, override
 
 from twitter_api.error import (
     TwitterApiOAuthTokenV1NotFound,
     TwitterApiResponseError,
     TwitterApiResponseFailed,
     TwitterApiResponseModelBodyDecodeError,
     TwitterApiResponseValidationError,
@@ -63,25 +64,29 @@
 
         if rate_limit_manager is None:
             rate_limit_manager = NoOperationRateLimitManager()
 
         self._rate_limit_manager = rate_limit_manager
 
     @property
+    @override
     def oauth_version(self) -> OAuthVersion:
         return self._oauth_version
 
     @property
+    @override
     def rate_limit_target(self) -> RateLimitTarget:
         return self._rate_limit_target
 
     @property
+    @override
     def rate_limit_manager(self) -> RateLimitManager:
         return self._rate_limit_manager
 
+    @override
     def get(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
@@ -104,14 +109,15 @@
             response_body_type,
             url,
             headers,
             query,
             body,
         )
 
+    @override
     def post(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
@@ -136,14 +142,15 @@
             response_body_type,
             url,
             headers,
             query,
             body,
         )
 
+    @override
     def delete(
         self,
         *,
         endpoint: Endpoint,
         response_body_type: Type[ResponseModelBody],
         url: Optional[Url] = None,
         auth: bool = True,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 import os
 from abc import ABCMeta, abstractmethod
-from typing import Mapping, Optional, Self, Union, overload
+from typing import Mapping, Optional, Union
+
+from typing_extensions import Self, overload
 
 from twitter_api.client.request.request_async_client import RequestAsyncClient
 from twitter_api.error import NeverError
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.resources.oauth2_invalidate_token import (
     AsyncOauth2InvalidateTokenResources,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_mock_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_mock_client.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Mapping, Optional, Self
+from typing import Mapping, Optional
+
+from typing_extensions import Self, override
 
 from twitter_api.client.twitter_api_async_client import TwitterApiAsyncClient
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.types import httpx
 from twitter_api.types.oauth import (
     AccessSecret,
@@ -17,14 +19,15 @@
 from twitter_api.types.v2_scope import Scope
 
 from .twitter_api_mock_client import _BaseTwitterApiMockClient
 
 
 class TwitterApiAsyncMockClient(_BaseTwitterApiMockClient, TwitterApiAsyncClient):
     @classmethod
+    @override
     def from_oauth2_bearer_token(
         cls,
         bearer_token: str,
         *,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
         limits: httpx.Limits = httpx.DEFAULT_LIMITS,
@@ -37,14 +40,15 @@
         return TwitterApiAsyncMockClient(
             oauth_version="2.0",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth2_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
@@ -58,14 +62,15 @@
         return TwitterApiAsyncMockClient(
             oauth_version="2.0",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_flow(
         cls,
         *,
         client_id: ClientId,
         client_secret: ClientSecret,
         callback_url: CallbackUrl,
         scope: list[Scope],
@@ -91,14 +96,15 @@
             ),
             scope=scope,
         )
 
         return TwitterOAuth2AuthorizeMockClient(session=session)
 
     @classmethod
+    @override
     def from_oauth2_user_flow_env(
         cls,
         *,
         scope: list[Scope],
         client_id_env: Env[ClientId] = "CLIENT_ID",
         client_secret_env: Env[ClientSecret] = "CLIENT_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
@@ -126,14 +132,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id: ClientId,
@@ -166,14 +173,15 @@
             authorization_response_url=authorization_response_url,
             state=state,
             code_verifier=code_verifier,
             session=session,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url_env(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id_env: Env[ClientId],
@@ -207,14 +215,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth1_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         access_token: AccessToken,
         access_secret: AccessSecret,
@@ -230,14 +239,15 @@
         return TwitterApiAsyncMockClient(
             oauth_version="1.0a",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_flow(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
@@ -264,14 +274,15 @@
                 access_secret=access_secret,
             ),
         )
 
         return TwitterOAuth1RequestTokenMockClient(session=session)
 
     @classmethod
+    @override
     def from_oauth1_user_flow_env(
         cls,
         *,
         api_key_env: Env[ApiKey] = "API_KEY",
         api_secret_env: Env[ApiSecret] = "API_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
         callback_url: Optional[CallbackUrl] = None,
@@ -297,14 +308,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
@@ -335,14 +347,15 @@
 
         return TwitterOAuth1AccessTokenMockClient(
             authorization_response_url=authorization_response_url,
             session=session,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url_env(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key_env: Env[ApiKey] = "API_KEY",
         api_secret_env: Env[ApiSecret] = "API_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_async_real_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_async_real_client.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,14 @@
-from typing import Mapping, Optional, Self
+from typing import Mapping, Optional
 
 from authlib.integrations.httpx_client.oauth1_client import OAuth1Auth
 from authlib.integrations.httpx_client.oauth2_client import OAuth2Auth
+from typing_extensions import Self, override
 
+from twitter_api.client.request.request_async_client import RequestAsyncClient
 from twitter_api.client.request.request_async_real_client import RequestAsyncRealClient
 from twitter_api.client.request.request_real_client import RequestRealClient
 from twitter_api.client.twitter_api_async_client import TwitterApiAsyncClient
 from twitter_api.client.twitter_api_real_client import TwitterApiRealClient
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.types import httpx
@@ -17,16 +19,14 @@
     ApiSecret,
     CallbackUrl,
     ClientId,
     ClientSecret,
 )
 from twitter_api.types.v2_scope import Scope
 
-from .request.request_client import RequestClient
-
 
 class TwitterApiAsyncRealClient(TwitterApiAsyncClient):
     """
     Twitter API V2 を操作するためのクライアント
 
     TwitterApiClient から生成されるクラスは、このクラスを継承する。
     """
@@ -34,18 +34,20 @@
     def __init__(
         self,
         request_client: RequestAsyncRealClient,
     ) -> None:
         self._real_request_client = request_client
 
     @property
-    def _request_client(self) -> RequestClient:
+    @override
+    def _request_client(self) -> RequestAsyncClient:
         return self._real_request_client
 
     @classmethod
+    @override
     def from_oauth2_bearer_token(
         cls,
         bearer_token: str,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
         limits: httpx.Limits = httpx.DEFAULT_LIMITS,
         mounts: Optional[Mapping[str, httpx.AsyncBaseTransport]] = None,
@@ -72,14 +74,15 @@
                 timeout=timeout,
                 transport=transport,
                 verify=verify,
             ),
         )
 
     @classmethod
+    @override
     def from_oauth2_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
@@ -124,14 +127,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_flow(
         cls,
         *,
         client_id: ClientId,
         client_secret: ClientSecret,
         callback_url: CallbackUrl,
         scope: list[Scope],
@@ -181,14 +185,15 @@
         client: TwitterOAuth2AuthorizeClient[
             TwitterApiAsyncRealClient
         ] = TwitterOAuth2AuthorizeClient(session)
 
         return client
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id: ClientId,
@@ -247,14 +252,15 @@
             code_verifier=code_verifier,
             session=session,
         )
 
         return client
 
     @classmethod
+    @override
     def from_oauth1_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         access_token: AccessToken,
         access_secret: AccessSecret,
@@ -286,14 +292,15 @@
                 timeout=timeout,
                 transport=transport,
                 verify=verify,
             ),
         )
 
     @classmethod
+    @override
     def from_oauth1_user_flow(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
@@ -338,14 +345,15 @@
             transport=None,
             verify=verify,
         )
 
         return TwitterOAuth1RequestTokenClient(session)
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 import os
 from abc import ABCMeta, abstractmethod
-from typing import Mapping, Optional, Self, Union, overload
+from typing import Mapping, Optional, Union
+
+from typing_extensions import Self, overload
 
 from twitter_api.error import NeverError
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.resources.oauth2_invalidate_token import (
     Oauth2InvalidateTokenResources,
     Oauth2InvalidateTokenUrl,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_mock_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_mock_client.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Mapping, Optional, Self, Union, overload
+from typing import Mapping, Optional, Union
+
+from typing_extensions import Self, overload, override
 
 from twitter_api.error import TwitterApiError
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.rate_limit.rate_limit_target import RateLimitTarget
 from twitter_api.resources.oauth2_invalidate_token import Oauth2InvalidateTokenUrl
 from twitter_api.resources.oauth2_invalidate_token.post_oauth2_invalidate_token import (
@@ -430,14 +432,15 @@
         return ""
 
 
 class TwitterApiMockClient(_BaseTwitterApiMockClient, TwitterApiClient):
     """Twitter API V2 をモックするためのクライアント"""
 
     @classmethod
+    @override
     def from_oauth2_bearer_token(
         cls,
         bearer_token: str,
         *,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
         limits: httpx.Limits = httpx.DEFAULT_LIMITS,
@@ -450,14 +453,15 @@
         return TwitterApiMockClient(
             oauth_version="2.0",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth2_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
@@ -471,14 +475,15 @@
         return TwitterApiMockClient(
             oauth_version="2.0",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_flow(
         cls,
         *,
         client_id: ClientId,
         client_secret: ClientSecret,
         callback_url: CallbackUrl,
         scope: list[Scope],
@@ -504,14 +509,15 @@
             ),
             scope=scope,
         )
 
         return TwitterOAuth2AuthorizeMockClient(session=session)
 
     @classmethod
+    @override
     def from_oauth2_user_flow_env(
         cls,
         *,
         scope: list[Scope],
         client_id_env: Env[ClientId] = "CLIENT_ID",
         client_secret_env: Env[ClientSecret] = "CLIENT_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
@@ -541,14 +547,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id: ClientId,
@@ -581,14 +588,15 @@
             authorization_response_url=authorization_response_url,
             state=state,
             code_verifier=code_verifier,
             session=session,
         )
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url_env(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id_env: Env[ClientId] = "CLIENT_ID",
@@ -622,14 +630,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth1_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         access_token: AccessToken,
         access_secret: AccessSecret,
@@ -645,14 +654,15 @@
         return TwitterApiMockClient(
             oauth_version="1.0a",
             rate_limit_target="app",
             rate_limit_manager=rate_limit_manager,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_flow(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
@@ -679,14 +689,15 @@
                 access_secret=access_secret,
             ),
         )
 
         return TwitterOAuth1RequestTokenMockClient(session=session)
 
     @classmethod
+    @override
     def from_oauth1_user_flow_env(
         cls,
         *,
         api_key_env: Env[ApiKey] = "API_KEY",
         api_secret_env: Env[ApiSecret] = "API_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
         callback_url: Optional[CallbackUrl] = None,
@@ -714,14 +725,15 @@
             proxies=proxies,
             timeout=timeout,
             transport=transport,
             verify=verify,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
@@ -754,14 +766,15 @@
 
         return TwitterOAuth1AccessTokenMockClient(
             authorization_response_url=authorization_response_url,
             session=session,
         )
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url_env(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key_env: Env[ApiKey] = "API_KEY",
         api_secret_env: Env[ApiSecret] = "API_SECRET",
         callback_url_env: Env[CallbackUrl] = "CALLBACK_URL",
```

### Comparing `twitter_api_py-0.5.1/twitter_api/client/twitter_api_real_client.py` & `twitter_api_py-0.6.0/twitter_api/client/twitter_api_real_client.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,12 @@
-from typing import Mapping, Optional, Self
+from typing import Mapping, Optional
 
 from authlib.integrations.httpx_client.oauth1_client import OAuth1Auth
 from authlib.integrations.httpx_client.oauth2_client import OAuth2Auth
+from typing_extensions import Self, override
 
 from twitter_api.client.oauth_flow.twitter_oauth1_request_token_client import (
     TwitterOAuth1RequestTokenClient,
 )
 from twitter_api.rate_limit.manager import DEFAULT_RATE_LIMIT_MANAGER
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.types import httpx
@@ -33,18 +34,20 @@
     def __init__(
         self,
         request_client: RequestRealClient,
     ) -> None:
         self._real_request_client = request_client
 
     @property
+    @override
     def _request_client(self) -> RequestClient:
         return self._real_request_client
 
     @classmethod
+    @override
     def from_oauth2_bearer_token(
         cls,
         bearer_token: str,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
         limits: httpx.Limits = httpx.DEFAULT_LIMITS,
         mounts: Optional[Mapping[str, httpx.BaseTransport]] = None,
@@ -71,14 +74,15 @@
                 timeout=timeout,
                 transport=transport,
                 verify=verify,
             ),
         )
 
     @classmethod
+    @override
     def from_oauth2_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
         event_hooks: Optional[Mapping[str, list[httpx.EventHook]]] = None,
@@ -113,14 +117,15 @@
                 )
                 .access_token
             )
 
         return TwitterApiRealClient.from_oauth2_bearer_token(access_token)
 
     @classmethod
+    @override
     def from_oauth2_user_flow(
         cls,
         *,
         client_id: ClientId,
         client_secret: ClientSecret,
         callback_url: CallbackUrl,
         scope: list[Scope],
@@ -160,14 +165,15 @@
         client: TwitterOAuth2AuthorizeClient[
             TwitterApiRealClient
         ] = TwitterOAuth2AuthorizeClient(session)
 
         return client
 
     @classmethod
+    @override
     def from_oauth2_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         state: str,
         code_verifier: str,
         client_id: ClientId,
@@ -224,14 +230,15 @@
             code_verifier=code_verifier,
             session=session,
         )
 
         return client
 
     @classmethod
+    @override
     def from_oauth1_app(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         access_token: AccessToken,
         access_secret: AccessSecret,
@@ -263,14 +270,15 @@
                 timeout=timeout,
                 transport=transport,
                 verify=verify,
             ),
         )
 
     @classmethod
+    @override
     def from_oauth1_user_flow(
         cls,
         *,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
         rate_limit_manager: RateLimitManager = DEFAULT_RATE_LIMIT_MANAGER,
@@ -312,14 +320,15 @@
             transport=transport,
             verify=verify,
         )
 
         return TwitterOAuth1RequestTokenClient(session)
 
     @classmethod
+    @override
     def from_oauth1_user_authorization_response_url(
         cls,
         *,
         authorization_response_url: CallbackUrl,
         api_key: ApiKey,
         api_secret: ApiSecret,
         callback_url: CallbackUrl,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/error.py` & `twitter_api_py-0.6.0/twitter_api/error.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 import json
 from abc import abstractmethod
 from collections import OrderedDict
 from enum import Enum
 from textwrap import dedent
-from typing import Any, Never, Optional, Union
+from typing import Optional, Union
 
 import pydantic
+from typing_extensions import Any, Never
 
 from twitter_api.rate_limit.rate_limit_info import RateLimitInfo
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 
 from .types.endpoint import Endpoint
 from .types.http import Headers, QuryParameters, RequestJsonBody, ResponseJsonBody
 from .types.oauth import OAuthVersion
@@ -148,47 +149,46 @@
         self.query = query
         self.request_body = request_body
         self.status_code = status_code
         self.response_body = response_body
 
     @property
     def message(self) -> str:
-        match self.status_code:
-            case TwitterApiErrorCode.OK.value:
-                return "API が成功しています。"
-            case TwitterApiErrorCode.NotModified.value:
-                return "返却する新しいデータがありません。"
-            case TwitterApiErrorCode.BadRequest.value:
-                return "リクエストの形式が間違っています。"
-            case TwitterApiErrorCode.Unauthorized.value:
-                return "このリクエストは証認されていません。"
-            case TwitterApiErrorCode.Forbidden.value:
-                return "このリクエストは許可されていません。"
-            case TwitterApiErrorCode.NotFound.value:
-                return "データが見つかりません。"
-            case TwitterApiErrorCode.NotAcceptable.value:
-                return "アクセスできません。"
-            case TwitterApiErrorCode.ConnectionException.value:
-                return "接続に失敗しました。"
-            case TwitterApiErrorCode.Gone.value:
-                return "このリソースは利用できなくなりました。"
-            case TwitterApiErrorCode.UnprocessableEntity.value:
-                return "処理できないエンティティです。"
-            case TwitterApiErrorCode.TooManyRequests.value:
-                return "レートリミットか Tweet Cap が制限を超えました。"
-            case TwitterApiErrorCode.InternalServerError.value:
-                return "Twitter API の内部でエラーが発生しました。"
-            case TwitterApiErrorCode.BadGateway.value:
-                return "Twitter API がダウンしているか、アップグレード中です。"
-            case TwitterApiErrorCode.ServiceUnavailable.value:
-                return "リクエスト数が多く処理できません。後でもう一度お試しください。"
-            case TwitterApiErrorCode.GatewayTimeout.value:
-                return "Twitter API が内部的にダウンしています。後でもう一度お試しください。"
-            case _:
-                return "Twitter API の応答が 200 ではありません。"
+        if self.status_code == TwitterApiErrorCode.OK.value:
+            return "API が成功しています。"
+        elif self.status_code == TwitterApiErrorCode.NotModified.value:
+            return "返却する新しいデータがありません。"
+        elif self.status_code == TwitterApiErrorCode.BadRequest.value:
+            return "リクエストの形式が間違っています。"
+        elif self.status_code == TwitterApiErrorCode.Unauthorized.value:
+            return "このリクエストは証認されていません。"
+        elif self.status_code == TwitterApiErrorCode.Forbidden.value:
+            return "このリクエストは許可されていません。"
+        elif self.status_code == TwitterApiErrorCode.NotFound.value:
+            return "データが見つかりません。"
+        elif self.status_code == TwitterApiErrorCode.NotAcceptable.value:
+            return "アクセスできません。"
+        elif self.status_code == TwitterApiErrorCode.ConnectionException.value:
+            return "接続に失敗しました。"
+        elif self.status_code == TwitterApiErrorCode.Gone.value:
+            return "このリソースは利用できなくなりました。"
+        elif self.status_code == TwitterApiErrorCode.UnprocessableEntity.value:
+            return "処理できないエンティティです。"
+        elif self.status_code == TwitterApiErrorCode.TooManyRequests.value:
+            return "レートリミットか Tweet Cap が制限を超えました。"
+        elif self.status_code == TwitterApiErrorCode.InternalServerError.value:
+            return "Twitter API の内部でエラーが発生しました。"
+        elif self.status_code == TwitterApiErrorCode.BadGateway.value:
+            return "Twitter API がダウンしているか、アップグレード中です。"
+        elif self.status_code == TwitterApiErrorCode.ServiceUnavailable.value:
+            return "リクエスト数が多く処理できません。後でもう一度お試しください。"
+        elif self.status_code == TwitterApiErrorCode.GatewayTimeout.value:
+            return "Twitter API が内部的にダウンしています。後でもう一度お試しください。"
+        else:
+            return "Twitter API の応答が 200 ではありません。"
 
     @property
     def info(self) -> TwitterApiExceptionInfo:
         return TwitterApiExceptionInfo(
             type=self.__class__.__name__,
             message=self.message,
             **OrderedDict(
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/__init__.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/__init__.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/dict_rate_limit_manager.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/dict_rate_limit_manager.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/dict_sleep_rate_limit_manager.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/dict_sleep_rate_limit_manager.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+from typing_extensions import override
+
 from twitter_api.rate_limit.manager.mixins.dict_rate_limit_checker_mixin import (
     DictRateLimitCheckerMixin,
 )
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 
 from .mixins.sleep_rate_limit_handler_mixin import (
     DEFAULT_MAX_RANDOM_SLEEP_SECONDS,
@@ -25,13 +27,15 @@
         max_random_sleep_seconds: int = DEFAULT_MAX_RANDOM_SLEEP_SECONDS,
     ):
         self._min_random_sleep_seconds = min_random_sleep_seconds
         self._max_random_sleep_seconds = max_random_sleep_seconds
         super().__init__()
 
     @property
+    @override
     def min_random_sleep_seconds(self) -> int:
         return self._min_random_sleep_seconds
 
     @property
+    @override
     def max_random_sleep_seconds(self) -> int:
         return self._max_random_sleep_seconds
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/dict_rate_limit_checker_mixin.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/dict_rate_limit_checker_mixin.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 from bisect import bisect_left
 from dataclasses import dataclass
 from datetime import datetime, timedelta
 from typing import Optional
 
+from typing_extensions import override
+
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.rate_limit.rate_limit_info import RateLimitInfo
 
 
 @dataclass
 class RateLimitStatus:
     start_datetime: datetime
@@ -20,14 +22,15 @@
     Redis, RDS などで管理したい場合は、
     このクラスを参考に RateLimitManager を実装すればよい。
     """
 
     def __init__(self) -> None:
         self._store: dict[RateLimitInfo, RateLimitStatus] = {}
 
+    @override
     def check_limit_over(
         self,
         rate_limit_info: RateLimitInfo,
         now: Optional[datetime] = None,
     ) -> Optional[float]:
         if now is None:
             now = datetime.now()
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/raise_rate_limit_handler_mixin.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/raise_rate_limit_handler_mixin.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,17 +1,20 @@
 from typing import Generator
 
+from typing_extensions import override
+
 from twitter_api.error import RateLimitOverError
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.rate_limit.rate_limit_info import RateLimitInfo
 
 
 class RaiseRateLimitHandlerMixin(RateLimitManager):
     """
     レートリミットオーバーが発生した場合、例外を投げる単純な操作を行う。
     """
 
+    @override
     def handle(self, rate_limit_info: RateLimitInfo) -> Generator[None, None, None]:
         if self.check_limit_over(rate_limit_info) is not None:
             raise RateLimitOverError(rate_limit_info)
 
         yield
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/mixins/sleep_rate_limit_handler_mixin.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/mixins/sleep_rate_limit_handler_mixin.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 import asyncio
 import time
 from logging import getLogger
 from random import randint
-from typing import AsyncGenerator, Generator
+from typing import Generator
+
+from typing_extensions import AsyncGenerator, override
 
 from twitter_api.error import TwitterApiErrorCode, TwitterApiResponseFailed
 from twitter_api.rate_limit.manager.rate_limit_manager import (
     RateLimitManager,
     RetryRateLimitHandling,
 )
 from twitter_api.rate_limit.rate_limit_info import RateLimitInfo
@@ -34,14 +36,15 @@
     def generate_random_sleep_seconds(self) -> int:
         """
         予期しないレートリミットに遭遇した場合にランダムに休む時間[秒]。
         """
 
         return randint(self.min_random_sleep_seconds, self.max_random_sleep_seconds)
 
+    @override
     def handle(self, rate_limit_info: RateLimitInfo) -> Generator[None, None, None]:
         # レートリミットを超えてしまっていたら、必要な待ち時間分だけ待つ。
         if wait_time_seconds := self.check_limit_over(rate_limit_info):
             logger.warning(RateLimitOverWarning(rate_limit_info))
             time.sleep(wait_time_seconds)
 
             raise RetryRateLimitHandling()
@@ -56,14 +59,15 @@
 
             # 予期しないレートリミットに遭遇した場合、投機的な待機を行う。
             logger.warning(UnmanagedRateLimitOverWarning())
             time.sleep(self.generate_random_sleep_seconds())
 
             raise RetryRateLimitHandling()
 
+    @override
     async def ahandle(
         self, rate_limit_info: RateLimitInfo
     ) -> AsyncGenerator[None, None]:
         # レートリミットを超えてしまっていたら、必要な待ち時間分だけ待つ。
         if wait_time_seconds := self.check_limit_over(rate_limit_info):
             logger.warning(RateLimitOverWarning(rate_limit_info))
             await asyncio.sleep(wait_time_seconds)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/no_operation_rate_limit_manager.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/no_operation_rate_limit_manager.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,25 +1,29 @@
 from contextlib import contextmanager
 from datetime import datetime
 from typing import Generator, Optional
 
+from typing_extensions import override
+
 from twitter_api.rate_limit.manager.rate_limit_manager import RateLimitManager
 from twitter_api.rate_limit.rate_limit_info import RateLimitInfo
 
 
 class NoOperationRateLimitManager(RateLimitManager):
     """
     レートリミットに関して、クライアント側で何も制御しないマネージャ。
 
     Twitter API が返すレートリミットエラーをそのまま例外として投げることを想定している。
     """
 
+    @override
     def check_limit_over(
         self,
         rate_limit_info: RateLimitInfo,
         now: Optional[datetime] = None,
     ) -> Optional[float]:
         return None
 
+    @override
     @contextmanager
     def handle(self, rate_limit_info: RateLimitInfo) -> Generator[None, None, None]:
         yield
```

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/manager/rate_limit_manager.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/manager/rate_limit_manager.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/rate_limit/rate_limit.py` & `twitter_api_py-0.6.0/twitter_api/rate_limit/rate_limit.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/oauth2_invalidate_token/post_oauth2_invalidate_token.py` & `twitter_api_py-0.6.0/twitter_api/resources/oauth2_invalidate_token/post_oauth2_invalidate_token.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import base64
-from typing import TypedDict
+
+from typing_extensions import TypedDict, override
 
 from twitter_api.error import TwitterApiOAuthVersionWrong
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.oauth import AccessToken, ApiKey, ApiSecret
@@ -53,14 +54,15 @@
                 "Content-Type": "application/x-www-form-urlencoded",
             },
             query=downcast_dict(query),
         )
 
 
 class AsyncPostOauth2InvalidateTokenResources(PostOauth2InvalidateTokenResources):
+    @override
     async def post(
         self,
         api_key: ApiKey,
         api_secret: ApiSecret,
         query: PostOauth2InvalidateTokenQueryParameters,
     ) -> PostOauth2InvalidateTokenResponseBody:
         return super().post(
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/oauth2_token/post_oauth2_token.py` & `twitter_api_py-0.6.0/twitter_api/resources/oauth2_token/post_oauth2_token.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import base64
-from typing import Literal, TypedDict
+
+from typing_extensions import Literal, TypedDict, override
 
 from twitter_api.error import TwitterApiOAuthVersionWrong
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.oauth import AccessToken, ApiKey, ApiSecret
@@ -51,14 +52,15 @@
                 "Content-Type": "application/x-www-form-urlencoded;charset=UTF-8",
             },
             query=downcast_dict(query),
         )
 
 
 class AsyncPostOauth2TokenResources(PostOauth2TokenResources):
+    @override
     async def post(
         self,
         api_key: ApiKey,
         api_secret: ApiSecret,
         query: PostOauth2TokenQueryParameters,
     ) -> PostOauth2TokenResponseBody:
         return super().post(
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversation_messages/__init__.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversation_messages/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import TypeAlias
-
-from typing_extensions import Literal
+from typing_extensions import Literal, TypeAlias
 
 from .post_v2_dm_conversations_messages import (
     AsyncPostV2DmConversationMessagesResources,
     PostV2DmConversationMessagesResources,
 )
 
 V2DmConversationsMessagesUrl: TypeAlias = Literal[
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversation_messages/post_v2_dm_conversations_messages.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversation_messages/post_v2_dm_conversations_messages.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+from typing_extensions import override
+
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_dm_conversation.dm_conversation import DmConversation
 from twitter_api.types.v2_dm_conversation.dm_conversation_id import DmConversationId
@@ -47,14 +49,15 @@
             url=ENDPOINT.url.replace(":dm_conversation_id", dm_conversation_id),
             body=downcast_dict(request_body),
             response_body_type=PostV2DmConversationMessagesResponseBody,
         )
 
 
 class AsyncPostV2DmConversationMessagesResources(PostV2DmConversationMessagesResources):
+    @override
     async def post(
         self,
         dm_conversation_id: DmConversationId,
         request_body: PostV2DmConversationMessagesRequestBody,
     ) -> PostV2DmConversationMessagesResponseBody:
         return super().post(
             dm_conversation_id,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations/post_v2_dm_conversations.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations/post_v2_dm_conversations.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import Literal, TypedDict
+from typing_extensions import Literal, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_dm_conversation.dm_conversation import DmConversation
@@ -52,14 +52,15 @@
             endpoint=ENDPOINT,
             body=downcast_dict(request_body),
             response_body_type=PostV2DmConversationsResponseBody,
         )
 
 
 class AsyncPostV2DmConversationsResources(PostV2DmConversationsResources):
+    @override
     async def post(
         self,
         request_body: PostV2DmConversationsRequestBody,
     ) -> PostV2DmConversationsResponseBody:
         return super().post(
             request_body,
         )
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/__init__.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/__init__.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import TypeAlias
-
-from typing_extensions import Literal
+from typing_extensions import Literal, TypeAlias
 
 from .get_v2_dm_conversations_with_participant_dm_events import (
     AsyncGetV2DmConversationsWithParticipantDmEventsResources,
     GetV2DmConversationsWithParticipantDmEventsResources,
 )
 
 V2DmConversationsWithParticipantDmEventsUrl: TypeAlias = Literal[
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/get_v2_dm_conversations_with_participant_dm_events.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_dm_events/get_v2_dm_conversations_with_participant_dm_events.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from datetime import datetime
 from functools import partial
-from typing import AsyncGenerator, Generator, NotRequired, Optional, Self, TypedDict
+from typing import Generator, Optional
 
 from pydantic import Field
+from typing_extensions import AsyncGenerator, NotRequired, Self, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     PageResponseBody,
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
@@ -197,37 +198,40 @@
             partial(self.get, participant_id), query, "pagination_token"
         )
 
 
 class AsyncGetV2DmConversationsWithParticipantDmEventsResources(
     GetV2DmConversationsWithParticipantDmEventsResources
 ):
+    @override
     async def get(
         self,
         participant_id: UserId,
         query: Optional[
             GetV2DmConversationsWithParticipantDmEventsQueryParameters
         ] = None,
     ) -> GetV2DmConversationsWithParticipantDmEventsResponseBody:
         return super().get(
             participant_id,
             query,
         )
 
+    @override
     async def get_paging_response_body_iter(
         self,
         participant_id: UserId,
         query: Optional[
             GetV2DmConversationsWithParticipantDmEventsQueryParameters
         ] = None,
     ) -> AsyncGenerator[GetV2DmConversationsWithParticipantDmEventsResponseBody, None]:
         return aget_paging_response_body_iter(
             partial(self.get, participant_id), query, "pagination_token"
         )
 
+    @override
     async def get_collected_paging_response_body(
         self,
         participant_id: UserId,
         query: Optional[
             GetV2DmConversationsWithParticipantDmEventsQueryParameters
         ] = None,
     ) -> GetV2DmConversationsWithParticipantDmEventsResponseBody:
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_messages/__init__.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_messages/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import TypeAlias
-
-from typing_extensions import Literal
+from typing_extensions import Literal, TypeAlias
 
 from .post_v2_dm_conversations_with_participant_messages import (
     AsyncPostV2DmConversationsWithParticipantMessagesResources,
     PostV2DmConversationsWithParticipantMessagesResources,
 )
 
 V2DmConversationsWithParticipantMessagesUrl: TypeAlias = Literal[
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_dm_conversations_with_participant_messages/post_v2_dm_conversations_with_participant_messages.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_dm_conversations_with_participant_messages/post_v2_dm_conversations_with_participant_messages.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+from typing_extensions import override
+
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_dm_conversation.dm_conversation import DmConversation
 from twitter_api.types.v2_dm_conversation.dm_conversation_message import (
@@ -49,14 +51,15 @@
             response_body_type=PostV2DmConversationsWithParticipantMessagesResponseBody,
         )
 
 
 class AsyncPostV2DmConversationsWithParticipantMessagesResources(
     PostV2DmConversationsWithParticipantMessagesResources
 ):
+    @override
     async def post(
         self,
         participant_id: UserId,
         request_body: PostV2DmConversationsWithParticipantMessagesRequestBody,
     ) -> PostV2DmConversationsWithParticipantMessagesResponseBody:
         return super().post(
             participant_id,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweet/delete_v2_tweet.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweet/delete_v2_tweet.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+from typing_extensions import override
+
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.v2_scope import oauth2_scopes
 from twitter_api.types.v2_tweet.tweet_id import TweetId
 
@@ -36,12 +38,13 @@
             endpoint=ENDPOINT,
             response_body_type=DeleteV2TweetResponseBody,
             url=ENDPOINT.url.replace(":id", id),
         )
 
 
 class AsyncDeleteV2TweetResources(DeleteV2TweetResources):
+    @override
     async def delete(
         self,
         id: TweetId,
     ) -> DeleteV2TweetResponseBody:
         return super().delete(id)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweet/get_v2_tweet.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweet/get_v2_tweet.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
+
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.v2_media.media_field import MediaField
 from twitter_api.types.v2_place.place_field import PlaceField
@@ -71,13 +73,14 @@
             response_body_type=GetV2TweetResponseBody,
             url=ENDPOINT.url.replace(":id", id),
             query=_make_query(query),
         )
 
 
 class AsyncGetV2TweetResources(GetV2TweetResources):
+    @override
     async def get(
         self,
         id: TweetId,
         query: Optional[GetV2TweetQueryParameters] = None,
     ):
         return super().get(id, query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweet_retweeted_by/get_v2_tweet_retweeted_by.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweet_retweeted_by/get_v2_tweet_retweeted_by.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from functools import partial
-from typing import AsyncGenerator, Generator, NotRequired, Optional, Self, TypedDict
+from typing import Generator, Optional
 
 from pydantic import Field
+from typing_extensions import AsyncGenerator, NotRequired, Self, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     PageResponseBody,
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
@@ -138,28 +139,31 @@
         """
         return get_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
         )
 
 
 class AsyncGetV2TweetRetweetedByResources(GetV2TweetRetweetedByResources):
+    @override
     async def get(
         self, id: TweetId, query: Optional[GetV2TweetRetweetedByQueryParameters] = None
     ) -> GetV2TweetRetweetedByResponseBody:
         return super().get(
             id,
             query,
         )
 
+    @override
     async def get_paging_response_body_iter(
         self, id: TweetId, query: Optional[GetV2TweetRetweetedByQueryParameters] = None
     ) -> AsyncGenerator[GetV2TweetRetweetedByResponseBody, None]:
         return aget_paging_response_body_iter(
             partial(self.get, id), query, "pagination_token"
         )
 
+    @override
     async def get_collected_paging_response_body(
         self, id: TweetId, query: Optional[GetV2TweetRetweetedByQueryParameters] = None
     ) -> GetV2TweetRetweetedByResponseBody:
         return await aget_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
         )
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets/get_v2_tweets.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets/get_v2_tweets.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
+
+from typing_extensions import NotRequired, TypedDict
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.v2_media.media_field import MediaField
 from twitter_api.types.v2_place.place_field import PlaceField
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets/post_v2_tweets.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets/post_v2_tweets.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Literal, NotRequired, Optional, TypedDict, Union
+from typing import Optional, Union
+
+from typing_extensions import Literal, NotRequired, TypedDict
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import Url, downcast_dict
 from twitter_api.types.v2_media.media_id import MediaId
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_all/get_v2_tweets_search_all.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_all/get_v2_tweets_search_all.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,19 +1,13 @@
 from datetime import datetime
-from typing import (
-    AsyncGenerator,
-    Generator,
-    Literal,
-    NotRequired,
-    Optional,
-    TypedDict,
-    Union,
-)
+from typing import Generator, Optional, Union
 from urllib import parse
 
+from typing_extensions import AsyncGenerator, Literal, NotRequired, TypedDict, override
+
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
     get_collected_paging_response_body,
     get_paging_response_body_iter,
@@ -123,21 +117,24 @@
 
         refer: https://developer.twitter.com/en/docs/twitter-api/tweets/search/api-reference/get-tweets-search-all
         """
         return get_collected_paging_response_body(self.get, query, "next_token")
 
 
 class AsyncGetV2TweetsSearchAllResources(GetV2TweetsSearchAllResources):
+    @override
     async def get(
         self, query: GetV2TweetsSearchAllQueryParameters
     ) -> GetV2TweetsSearchAllResponseBody:
         return super().get(query)
 
+    @override
     async def get_paging_response_body_iter(
         self, query: GetV2TweetsSearchAllQueryParameters
     ) -> AsyncGenerator[GetV2TweetsSearchAllResponseBody, None]:
         return aget_paging_response_body_iter(self.get, query, "next_token")
 
+    @override
     async def get_collected_paging_response_body(
         self, query: GetV2TweetsSearchAllQueryParameters
     ) -> GetV2TweetsSearchAllResponseBody:
         return await aget_collected_paging_response_body(self.get, query, "next_token")
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_recent/get_v2_tweets_search_recent.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_recent/get_v2_tweets_search_recent.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,11 @@
 from datetime import datetime
-from typing import (
-    AsyncGenerator,
-    Generator,
-    Literal,
-    NotRequired,
-    Optional,
-    TypedDict,
-    Union,
-)
+from typing import Generator, Optional, Union
+
+from typing_extensions import AsyncGenerator, Literal, NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
     get_collected_paging_response_body,
@@ -122,21 +116,24 @@
 
         refer: https://developer.twitter.com/en/docs/twitter-api/tweets/search/api-reference/get-tweets-search-recent
         """
         return get_collected_paging_response_body(self.get, query, "next_token")
 
 
 class AsyncGetV2TweetsSearchRecentResources(GetV2TweetsSearchRecentResources):
+    @override
     async def get(
         self, query: GetV2TweetsSearchRecentQueryParameters
     ) -> GetV2TweetsSearchRecentResponseBody:
         return super().get(query)
 
+    @override
     async def get_paging_response_body_iter(
         self, query: GetV2TweetsSearchRecentQueryParameters
     ) -> AsyncGenerator[GetV2TweetsSearchRecentResponseBody, None]:
         return aget_paging_response_body_iter(self.get, query, "next_token")
 
+    @override
     async def get_collected_paging_response_body(
         self, query: GetV2TweetsSearchRecentQueryParameters
     ) -> GetV2TweetsSearchRecentResponseBody:
         return await aget_collected_paging_response_body(self.get, query, "next_token")
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream/get_v2_tweets_search_stream.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream/get_v2_tweets_search_stream.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 from datetime import datetime
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
+
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.v2_media.media_field import MediaField
 from twitter_api.types.v2_place.place_field import PlaceField
@@ -71,11 +73,12 @@
             endpoint=ENDPOINT,
             response_body_type=GetV2TweetsSearchStreamResponseBody,
             query=_make_query(query) if query is not None else None,
         )
 
 
 class AsyncGetV2TweetsSearchStreamResources(GetV2TweetsSearchStreamResources):
+    @override
     async def get(
         self, query: Optional[GetV2TweetsSearchStreamQueryParameters] = None
     ) -> GetV2TweetsSearchStreamResponseBody:
         return super().get(query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/__init__.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/__init__.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import TypeAlias
-
-from typing_extensions import Literal
+from typing_extensions import Literal, TypeAlias
 
 from .get_v2_tweets_search_stream_rules import (
     AsyncGetV2TweetsSearchStreamRulesResources,
     GetV2TweetsSearchStreamRulesResources,
 )
 from .post_v2_tweets_search_stream_rules import (
     AsyncPostV2TweetsSearchStreamRulesResources,
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/get_v2_tweets_search_stream_rules.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/get_v2_tweets_search_stream_rules.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from datetime import datetime
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_rule.rule import Rule
@@ -47,12 +48,13 @@
             endpoint=ENDPOINT,
             response_body_type=GetV2TweetsSearchStreamRulesResponseBody,
             query=downcast_dict(query),
         )
 
 
 class AsyncGetV2TweetsSearchStreamRulesResources(GetV2TweetsSearchStreamRulesResources):
+    @override
     async def get(
         self,
         query: Optional[GetV2TweetsSearchStreamRulesQueryParameters] = None,
     ) -> GetV2TweetsSearchStreamRulesResponseBody:
         return super().get(query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_tweets_search_stream_rules/post_v2_tweets_search_stream_rules.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_tweets_search_stream_rules/post_v2_tweets_search_stream_rules.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from datetime import datetime
-from typing import NotRequired, Optional, TypedDict, Union
+from typing import Optional, Union
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_rule.rule import Rule
@@ -82,13 +83,14 @@
             body=downcast_dict(request_body),
         )
 
 
 class AsyncPostV2TweetsSearchStreamRulesResources(
     PostV2TweetsSearchStreamRulesResources
 ):
+    @override
     async def post(
         self,
         request_body: PostV2TweetsSearchStreamRulesRequestBody,
         query: Optional[PostV2TweetsSearchStreamRulesQueryParameters] = None,
     ) -> PostV2TweetsSearchStreamRulesResponseBody:
         return super().post(request_body, query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user/get_v2_user.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user/get_v2_user.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -67,13 +68,14 @@
             url=ENDPOINT.url.replace(":id", id),
             query=_make_query(query) if query is not None else None,
             response_body_type=GetV2UserResponseBody,
         )
 
 
 class AsyncGetV2UserResources(GetV2UserResources):
+    @override
     async def get(
         self,
         id: UserId,
         query: Optional[GetV2UserQueryParameters] = None,
     ) -> GetV2UserResponseBody:
         return super().get(id, query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user_followers/get_v2_user_followers.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user_followers/get_v2_user_followers.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from functools import partial
-from typing import AsyncGenerator, Generator, NotRequired, Optional, Self, TypedDict
+from typing import Generator, Optional
 
 from pydantic import Field
+from typing_extensions import AsyncGenerator, NotRequired, Self, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     PageResponseBody,
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
@@ -145,30 +146,33 @@
         """
         return get_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
         )
 
 
 class AsyncGetV2UserFollowersResources(GetV2UserFollowersResources):
+    @override
     async def get(
         self,
         id: UserId,
         query: Optional[GetV2UserFollowersQueryParameters] = None,
     ) -> GetV2UserFollowersResponseBody:
         return super().get(id, query)
 
+    @override
     async def get_paging_response_body_iter(
         self,
         id: UserId,
         query: Optional[GetV2UserFollowersQueryParameters] = None,
     ) -> AsyncGenerator[GetV2UserFollowersResponseBody, None]:
         return aget_paging_response_body_iter(
             partial(self.get, id), query, "pagination_token"
         )
 
+    @override
     async def get_collected_paging_response_body(
         self,
         id: UserId,
         query: Optional[GetV2UserFollowersQueryParameters] = None,
     ) -> GetV2UserFollowersResponseBody:
         return await aget_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user_following/post_v2_user_following.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user_following/post_v2_user_following.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import TypedDict
+from typing_extensions import TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -49,13 +49,14 @@
             url=ENDPOINT.url.replace(":id", id),
             body=downcast_dict(request_body),
             response_body_type=PostV2UserFollowingResponseBody,
         )
 
 
 class AsyncPostV2UserFollowingResources(PostV2UserFollowingResources):
+    @override
     async def post(
         self,
         id: UserId,
         request_body: PostV2UserFollowingRequestBody,
     ) -> PostV2UserFollowingResponseBody:
         return super().post(id, request_body)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user_liked_tweets/get_v2_user_liked_tweets.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user_liked_tweets/get_v2_user_liked_tweets.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from functools import partial
-from typing import AsyncGenerator, Generator, NotRequired, Optional, Self, TypedDict
+from typing import Generator, Optional
 
 from pydantic import Field
+from typing_extensions import AsyncGenerator, NotRequired, Self, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     PageResponseBody,
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
@@ -170,30 +171,33 @@
         """
         return get_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
         )
 
 
 class AsyncGetV2UserLikedTweetsResources(GetV2UserLikedTweetsResources):
+    @override
     async def get(
         self,
         id: UserId,
         query: Optional[GetV2UserLikedTweetsQueryParameters] = None,
     ) -> GetV2UserLikedTweetsResponseBody:
         return super().get(id, query)
 
+    @override
     async def get_paging_response_body_iter(
         self,
         id: UserId,
         query: Optional[GetV2UserLikedTweetsQueryParameters] = None,
     ) -> AsyncGenerator[GetV2UserLikedTweetsResponseBody, None]:
         return aget_paging_response_body_iter(
             partial(self.get, id), query, "pagination_token"
         )
 
+    @override
     async def get_collected_paging_response_body(
         self,
         id: UserId,
         query: Optional[GetV2UserLikedTweetsQueryParameters] = None,
     ) -> GetV2UserLikedTweetsResponseBody:
         return await aget_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user_retweets/post_v2_user_retweets.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user_retweets/post_v2_user_retweets.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import TypedDict
+from typing_extensions import TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.http import downcast_dict
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -49,13 +49,14 @@
             url=ENDPOINT.url.replace(":id", id),
             body=downcast_dict(request_body),
             response_body_type=PostV2UserRetweetsResponseBody,
         )
 
 
 class AsyncPostV2UserRetweetsResources(PostV2UserRetweetsResources):
+    @override
     async def post(
         self,
         id: UserId,
         request_body: PostV2UserRetweetsRequestBody,
     ) -> PostV2UserRetweetsResponseBody:
         return super().post(id, request_body)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_user_tweets/get_v2_user_tweets.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_user_tweets/get_v2_user_tweets.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 from datetime import datetime
 from functools import partial
-from typing import (
+from typing import Generator, Optional
+
+from pydantic import Field
+from typing_extensions import (
     AsyncGenerator,
-    Generator,
     Literal,
     NotRequired,
-    Optional,
     Self,
     TypedDict,
+    override,
 )
 
-from pydantic import Field
-
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types._paging import (
     PageResponseBody,
     aget_collected_paging_response_body,
     aget_paging_response_body_iter,
     get_collected_paging_response_body,
@@ -188,30 +188,33 @@
         """
         return get_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
         )
 
 
 class AsyncGetV2UserTweetsResources(GetV2UserTweetsResources):
+    @override
     async def get(
         self,
         id: UserId,
         query: Optional[GetV2UserTweetsQueryParameters] = None,
     ) -> GetV2UserTweetsResponseBody:
         return super().get(id, query)
 
+    @override
     async def get_paging_response_body_iter(
         self,
         id: UserId,
         query: Optional[GetV2UserTweetsQueryParameters] = None,
     ) -> AsyncGenerator[GetV2UserTweetsResponseBody, None]:
         return aget_paging_response_body_iter(
             partial(self.get, id), query, "pagination_token"
         )
 
+    @override
     async def get_collected_paging_response_body(
         self,
         id: UserId,
         query: Optional[GetV2UserTweetsQueryParameters] = None,
     ) -> GetV2UserTweetsResponseBody:
         return await aget_collected_paging_response_body(
             partial(self.get, id), query, "pagination_token"
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_users/get_v2_users.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_users/get_v2_users.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -64,9 +65,10 @@
             endpoint=ENDPOINT,
             query=_make_query(query),
             response_body_type=GetV2UsersResponseBody,
         )
 
 
 class AsyncGetV2UsersResources(GetV2UsersResources):
+    @override
     async def get(self, query: GetV2UsersQueryParameters) -> GetV2UsersResponseBody:
         return super().get(query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_users_by/get_v2_users_by.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_users_by/get_v2_users_by.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -64,9 +65,10 @@
             endpoint=ENDPOINT,
             query=_make_query(query),
             response_body_type=GetV2UsersByResponseBody,
         )
 
 
 class AsyncGetV2UsersByResources(GetV2UsersByResources):
+    @override
     async def get(self, query: GetV2UsersByQueryParameters) -> GetV2UsersByResponseBody:
         return super().get(query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/resources/v2_users_by_username/get_v2_users_by_username.py` & `twitter_api_py-0.6.0/twitter_api/resources/v2_users_by_username/get_v2_users_by_username.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import NotRequired, Optional, TypedDict
+from typing import Optional
 
 from pydantic import Field
+from typing_extensions import NotRequired, TypedDict, override
 
 from twitter_api.rate_limit.rate_limit import rate_limit
 from twitter_api.resources.api_resources import ApiResources
 from twitter_api.types.comma_separatable import CommaSeparatable, comma_separated_str
 from twitter_api.types.endpoint import Endpoint
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.v2_scope import oauth2_scopes
@@ -67,13 +68,14 @@
             url=ENDPOINT.url.replace(":username", username),
             query=_make_query(query) if query is not None else None,
             response_body_type=GetV2UsersByUsernameResponseBody,
         )
 
 
 class AsyncGetV2UsersByUsernameResources(GetV2UsersByUsernameResources):
+    @override
     async def get(
         self,
         username: Username,
         query: Optional[GetV2UsersByUsernameQueryParameters] = None,
     ) -> GetV2UsersByUsernameResponseBody:
         return super().get(username, query)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/_generic_client.py` & `twitter_api_py-0.6.0/twitter_api/types/_generic_client.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/_model.py` & `twitter_api_py-0.6.0/twitter_api/types/_model.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/_paging.py` & `twitter_api_py-0.6.0/twitter_api/types/_paging.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,20 +1,11 @@
 from abc import ABCMeta, abstractmethod
-from typing import (
-    Any,
-    AsyncGenerator,
-    Callable,
-    Coroutine,
-    Generator,
-    Optional,
-    Self,
-    TypedDict,
-    TypeVar,
-    cast,
-)
+from typing import Callable, Generator, Optional, cast
+
+from typing_extensions import Any, AsyncGenerator, Coroutine, Self, TypedDict, TypeVar
 
 from twitter_api.types.pagination_token import PaginationToken
 
 
 class PageResponseBody(metaclass=ABCMeta):
     @property
     @abstractmethod
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/comma_separatable.py` & `twitter_api_py-0.6.0/twitter_api/types/comma_separatable.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Optional, TypeAlias, TypeVar, Union
+from typing import Optional, Union
+
+from typing_extensions import TypeAlias, TypeVar
 
 T = TypeVar("T", bound=str)
 
 CommaSeparatedStr: TypeAlias = str
 """
 要素がカンマ区切りで結合された文字列。
 """
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/extra_permissive_model.py` & `twitter_api_py-0.6.0/twitter_api/types/extra_permissive_model.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/http.py` & `twitter_api_py-0.6.0/twitter_api/types/http.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import Optional, TypeAlias, TypedDict, TypeVar, overload
+from typing import Optional
 
 from pydantic import BaseModel
+from typing_extensions import TypeAlias, TypedDict, TypeVar, overload
 
 Url: TypeAlias = str
 Headers = TypeVar("Headers", bound=dict)
 QuryParameters = TypeVar("QuryParameters", bound=dict)
 RequestJsonBody = TypeVar("RequestJsonBody", bound=dict)
 ResponseJsonBody = TypeVar("ResponseJsonBody", bound=dict)
 ResponseModelBody = TypeVar("ResponseModelBody", bound=BaseModel)
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/httpx.py` & `twitter_api_py-0.6.0/twitter_api/types/httpx.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,9 @@
-from typing import TypeAlias
-
 import httpx
+from typing_extensions import TypeAlias
 
 Client: TypeAlias = httpx.Client
 AsyncClient: TypeAlias = httpx.AsyncClient
 
 Response: TypeAlias = httpx.Response
 
 URL: TypeAlias = httpx.URL
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/oauth.py` & `twitter_api_py-0.6.0/twitter_api/types/oauth.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,18 +3,19 @@
 
 型を作るほどなのか難しい所であるが、同じことを指す用語がたくさん存在するため、
 あえて型を作ることで説明文を用意している。
 
 refer: https://developer.twitter.com/en/docs/authentication/oauth-1-0a/obtaining-user-access-tokens
 """
 
-from typing import Annotated, Literal, TypeAlias, TypeVar, Union
+from typing import Union
 
 from authlib.integrations.httpx_client.oauth1_client import OAuth1Auth
 from authlib.integrations.httpx_client.oauth2_client import OAuth2Auth
+from typing_extensions import Annotated, Literal, TypeAlias, TypeVar
 
 T = TypeVar("T", bound=str)
 
 OAuthVersion = Literal["1.0a", "2.0"]
 OAuth: TypeAlias = Union[OAuth2Auth, OAuth1Auth]
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/oauth1/oauth1_access_token.py` & `twitter_api_py-0.6.0/twitter_api/types/oauth1/oauth1_access_token.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/oauth1/oauth1_authorization.py` & `twitter_api_py-0.6.0/twitter_api/types/oauth1/oauth1_authorization.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/oauth2/oauth2_access_token.py` & `twitter_api_py-0.6.0/twitter_api/types/oauth2/oauth2_access_token.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/oauth2/oauth2_authorization.py` & `twitter_api_py-0.6.0/twitter_api/types/oauth2/oauth2_authorization.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_dm_conversation/dm_conversation_message.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_dm_conversation/dm_conversation_message.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import NotRequired, Optional, TypedDict, Union
+from typing import Optional, Union
+
+from typing_extensions import NotRequired, TypedDict
 
 from twitter_api.types.v2_dm_conversation.dm_conversation_attachment import (
     DmConversationAttachment,
 )
 
 DmConversationAttachmentOnly = TypedDict(
     "DmConversationMessage",
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_language.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_language.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_media/media.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_media/media.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_media/media_field.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_media/media_field.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_place/place.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_place/place.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_place/place_country_code.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_place/place_country_code.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_poll/poll.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_poll/poll.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_retweet/retweet_entities_description.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_retweet/retweet_entities_description.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_scope.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_scope.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_and_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_and_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_not_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_not_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/_or_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/_or_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/bounding_box_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/bounding_box_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/context_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/context_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/group_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/group_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/operator.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -67,25 +67,25 @@
 
     def __invert__(self):
         from ._not_operator import NotOperator
 
         return NotOperator(self)
 
 
-class ConjunctionRequiredOperator(IncompleteOperator):
+class StandaloneOperator(CompleteOperator):
     """
-    Twitter が定義した、それ自身だけではクエリとして成立しない Operator。
+    Twitter が定義した、それ自身がクエリとして成立する Operator。
 
     refer: https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/build-a-query#list
     """
 
     pass
 
 
-class StandaloneOperator(CompleteOperator):
+class ConjunctionRequiredOperator(IncompleteOperator):
     """
-    Twitter が定義した、それ自身がクエリとして成立する Operator。
+    Twitter が定義した、それ自身だけではクエリとして成立しない Operator。
 
     refer: https://developer.twitter.com/en/docs/twitter-api/tweets/search/integrate/build-a-query#list
     """
 
     pass
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/place_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/place_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/operators/point_radius_operator.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/operators/point_radius_operator.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/search_query.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/search_query.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_search_query/serch_query_builder.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_search_query/serch_query_builder.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,10 @@
-from typing import Any, Literal, Union, overload
+from typing import Union
+
+from typing_extensions import Any, Literal, overload
 
 from twitter_api.types.v2_cashtag import Cashtag
 from twitter_api.types.v2_dm_conversation.dm_conversation_id import DmConversationId
 from twitter_api.types.v2_domain import DomainId
 from twitter_api.types.v2_entity.entity_id import EntityId
 from twitter_api.types.v2_entity.entity_name import EntityName
 from twitter_api.types.v2_hashtag import Hashtag
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_entities.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_entities.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_expansion.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_expansion.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from typing import Literal, TypeAlias
+from typing_extensions import Literal, TypeAlias
 
 TweetExpansion: TypeAlias = Literal[
     "attachments.poll_ids",
     "attachments.media_keys",
     "author_id",
     "edit_history_tweet_ids",
     "entities.mentions.username",
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_field.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_field.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_tweet/tweet_response_body.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_tweet/tweet_response_body.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from abc import ABCMeta, abstractmethod
-from typing import Optional, Self, Union
+from typing import Optional, Union
 
 from pydantic import Field
+from typing_extensions import Self
 
 from twitter_api.types._paging import PageResponseBody
 from twitter_api.types.extra_permissive_model import ExtraPermissiveModel
 from twitter_api.types.pagination_token import PaginationToken
 from twitter_api.types.v2_media.media import Media
 from twitter_api.types.v2_place.place import Place
 from twitter_api.types.v2_poll.poll import Poll
```

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_user/user.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_user/user.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/types/v2_user/user_field.py` & `twitter_api_py-0.6.0/twitter_api/types/v2_user/user_field.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/utils/_functional.py` & `twitter_api_py-0.6.0/twitter_api/utils/_functional.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/utils/_oauth.py` & `twitter_api_py-0.6.0/twitter_api/utils/_oauth.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/utils/json.py` & `twitter_api_py-0.6.0/twitter_api/utils/json.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/twitter_api/warning.py` & `twitter_api_py-0.6.0/twitter_api/warning.py`

 * *Files identical despite different names*

### Comparing `twitter_api_py-0.5.1/PKG-INFO` & `twitter_api_py-0.6.0/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,28 +1,34 @@
 Metadata-Version: 2.1
 Name: twitter-api-py
-Version: 0.5.1
+Version: 0.6.0
 Summary: Twitter API Client by Typed Python.
 Home-page: https://github.com/yassun4dev/twitter-api-py
 License: BSD-3-Clause
 Author: yassun4dev
 Author-email: yassun4dev@outlook.com
-Requires-Python: >=3.11,<4.0
+Requires-Python: >=3.8.1,<4.0
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
+Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries
 Requires-Dist: authlib (>=1.2.0,<2.0.0)
 Requires-Dist: httpx (>=0.24.0,<0.25.0)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
+Requires-Dist: typing-extensions (>=4.5.0,<5.0.0)
 Project-URL: Repository, https://github.com/yassun4dev/twitter-api-py
 Description-Content-Type: text/markdown
 
 # <p align="center">✨✨ Twitter API Client by Typed Python ✨✨</p>
 
 <p align="center">
     <a href="https://github.com/yassun4dev/twitter-api-py/actions">
```

