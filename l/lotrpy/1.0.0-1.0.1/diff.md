# Comparing `tmp/lotrpy-1.0.0.tar.gz` & `tmp/lotrpy-1.0.1.tar.gz`

## Comparing `lotrpy-1.0.0.tar` & `lotrpy-1.0.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0     1571 2020-02-02 00:00:00.000000 lotrpy-1.0.0/DESIGN.md
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lotrpy-1.0.0/lotrpy/__init__.py
--rw-r--r--   0        0        0     4228 2020-02-02 00:00:00.000000 lotrpy-1.0.0/lotrpy/lotr.py
--rw-r--r--   0        0        0      826 2020-02-02 00:00:00.000000 lotrpy-1.0.0/lotrpy/models.py
--rw-r--r--   0        0        0     2689 2020-02-02 00:00:00.000000 lotrpy-1.0.0/lotrpy/serializers.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lotrpy-1.0.0/tests/__init__.py
--rw-r--r--   0        0        0     2855 2020-02-02 00:00:00.000000 lotrpy-1.0.0/tests/conftest.py
--rw-r--r--   0        0        0     2091 2020-02-02 00:00:00.000000 lotrpy-1.0.0/tests/integration/test_apis.py
--rw-r--r--   0        0        0     2109 2020-02-02 00:00:00.000000 lotrpy-1.0.0/tests/unit/test_lotr.py
--rw-r--r--   0        0        0     3077 2020-02-02 00:00:00.000000 lotrpy-1.0.0/.gitignore
--rw-r--r--   0        0        0     1063 2020-02-02 00:00:00.000000 lotrpy-1.0.0/LICENSE
--rw-r--r--   0        0        0     1511 2020-02-02 00:00:00.000000 lotrpy-1.0.0/README.md
--rw-r--r--   0        0        0      452 2020-02-02 00:00:00.000000 lotrpy-1.0.0/pyproject.toml
--rw-r--r--   0        0        0     1918 2020-02-02 00:00:00.000000 lotrpy-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0     1571 2020-02-02 00:00:00.000000 lotrpy-1.0.1/DESIGN.md
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lotrpy-1.0.1/lotrpy/__init__.py
+-rw-r--r--   0        0        0     4238 2020-02-02 00:00:00.000000 lotrpy-1.0.1/lotrpy/lotr.py
+-rw-r--r--   0        0        0      826 2020-02-02 00:00:00.000000 lotrpy-1.0.1/lotrpy/models.py
+-rw-r--r--   0        0        0     2699 2020-02-02 00:00:00.000000 lotrpy-1.0.1/lotrpy/serializers.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 lotrpy-1.0.1/tests/__init__.py
+-rw-r--r--   0        0        0     2855 2020-02-02 00:00:00.000000 lotrpy-1.0.1/tests/conftest.py
+-rw-r--r--   0        0        0     3099 2020-02-02 00:00:00.000000 lotrpy-1.0.1/tests/integration/test_apis.py
+-rw-r--r--   0        0        0     2114 2020-02-02 00:00:00.000000 lotrpy-1.0.1/tests/unit/test_lotr.py
+-rw-r--r--   0        0        0     3077 2020-02-02 00:00:00.000000 lotrpy-1.0.1/.gitignore
+-rw-r--r--   0        0        0     1063 2020-02-02 00:00:00.000000 lotrpy-1.0.1/LICENSE
+-rw-r--r--   0        0        0     1511 2020-02-02 00:00:00.000000 lotrpy-1.0.1/README.md
+-rw-r--r--   0        0        0      451 2020-02-02 00:00:00.000000 lotrpy-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     1918 2020-02-02 00:00:00.000000 lotrpy-1.0.1/PKG-INFO
```

### Comparing `lotrpy-1.0.0/DESIGN.md` & `lotrpy-1.0.1/DESIGN.md`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/lotrpy/lotr.py` & `lotrpy-1.0.1/lotrpy/lotr.py`

 * *Files 0% similar despite different names*

```diff
@@ -83,15 +83,15 @@
             kwargs:
                 limit: restrict the number of movies returned to this
                 page: the page number to fetch
         
         Returns:
             ```QuoteListResponse``` object
         """
-        response = make_request(self.token, self.server_url, f"movie/{movie_id}/quote")
+        response = make_request(self.token, self.server_url, f"movie/{movie_id}/quote", **kwargs)
         return deserialize_quotes(response)
 
     def get_quote(self, quote_id: str) -> Union[Quote, None]:
         """
         Fetch a specific quote based on quote_id.
 
         Arguments:
```

### Comparing `lotrpy-1.0.0/lotrpy/models.py` & `lotrpy-1.0.1/lotrpy/models.py`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/lotrpy/serializers.py` & `lotrpy-1.0.1/lotrpy/serializers.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
     Quote,
     QuoteListResponse
 )
 
 def deserialize_movies(movies: dict) -> MovieListResponse:
     resp = MovieListResponse(
         limit = movies['limit'],
-        offset = movies['offset'] if "offset" in movies else "",
+        offset = str(movies['offset']) if "offset" in movies else "",
         page = movies['page'],
         pages = movies['pages'],
         total = movies['total'],
     )
     resp.movies = []
     for movie in movies['docs']:
         item = Movie(
@@ -64,15 +64,15 @@
         dialog = quote["dialog"],
         character = quote["character"]
     )
 
 def deserialize_quotes(quotes: dict) -> QuoteListResponse:
     resp = QuoteListResponse(
         limit = quotes['limit'],
-        offset = quotes['offset'] if "offset" in quotes else "",
+        offset = str(quotes['offset']) if "offset" in quotes else "",
         page = quotes['page'],
         pages = quotes['pages'],
         total = quotes['total'],
     )
     resp.quotes = []
     for quote in quotes['docs']:
         item = Quote(
```

### Comparing `lotrpy-1.0.0/tests/conftest.py` & `lotrpy-1.0.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/tests/integration/test_apis.py` & `lotrpy-1.0.1/tests/integration/test_apis.py`

 * *Files 18% similar despite different names*

```diff
@@ -4,14 +4,19 @@
   Movie,
   MovieListResponse,
   Quote,
   QuoteListResponse
 ) 
 from requests.exceptions import HTTPError
 
+# NOTE: The tests here are less than ideal as we are checking for specific data
+# from a third party API, which we have no control over and hence can change. 
+# What we should actually be checking is that the API contract and endpoints are 
+# valid from this external server. For data checks we should set up our own mock services.
+
 def test_get_movies(lotr_object):
     resp = lotr_object.get_movies()
     assert len(resp.movies) > 0
 
 def test_get_movies_with_paging_and_limit(lotr_object):
     # we should received on page with 2 results with several pending
     # pages
@@ -23,38 +28,46 @@
     next_page = lotr_object.get_movies(limit = 2, page = 2)
     assert len(next_page.movies) == 2
     assert next_page.page == resp.page + 1
 
 
 def test_get_movie(lotr_object):
     resp = lotr_object.get_movie("5cd95395de30eff6ebccde5d")
-    # import pdb;pdb.set_trace()
     assert isinstance(resp, Movie)
     assert resp.name
 
     # negative test
     with pytest.raises(HTTPError):
         resp = lotr_object.get_movie("bad_id")
 
 def test_get_quote(lotr_object):
     resp = lotr_object.get_quote("5cd96e05de30eff6ebccebcf")
-    # import pdb;pdb.set_trace()
     assert isinstance(resp, Quote)
     assert resp.dialog
 
     # negative test
     with pytest.raises(HTTPError):
         resp = lotr_object.get_quote("bad_id")
 
 
 def test_get_quotes_from_movie(lotr_object):
     resp = lotr_object.get_quotes_from_movie("5cd95395de30eff6ebccde5b")
     assert len(resp.quotes) > 0
     assert isinstance(resp, QuoteListResponse)
 
+def test_get_quotes_from_movie_with_paging(lotr_object):
+    resp = lotr_object.get_quotes_from_movie("5cd95395de30eff6ebccde5b")
+    assert len(resp.quotes) > 0
+    assert len(resp.quotes) == resp.limit
+    assert resp.page < resp.pages
+
+    next_page = lotr_object.get_quotes_from_movie("5cd95395de30eff6ebccde5b", page=2)
+    assert len(resp.quotes) > 0
+    assert next_page.limit == resp.limit
+
 def test_get_quotes(lotr_object):
     resp = lotr_object.get_quotes()
     assert len(resp.quotes) > 1
     assert isinstance(resp, QuoteListResponse)
 
 
 def test_get_quotes_with_paging_and_limit(lotr_object):
@@ -65,8 +78,19 @@
     assert resp.page < resp.pages
 
     # testing paging by fetching the next page
     next_page = lotr_object.get_quotes(limit = 2, page = 2)
     assert len(next_page.quotes) == 2
     assert next_page.page == resp.page + 1
 
+def test_get_quotes_with_paging(lotr_object):
+    resp = lotr_object.get_quotes()
+    assert len(resp.quotes) > 0
+    assert resp.limit == len(resp.quotes)
+    assert resp.page < resp.pages
+
+    next_page = lotr_object.get_quotes(page=2)
+    assert len(next_page.quotes) > 0
+    assert next_page.limit == resp.limit # we didn't change this
+
+
```

### Comparing `lotrpy-1.0.0/tests/unit/test_lotr.py` & `lotrpy-1.0.1/tests/unit/test_lotr.py`

 * *Files 4% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 def test_deserialize_movies(movies):
     resp = deserialize_movies(movies)
     assert isinstance(resp, MovieListResponse)
     assert resp.limit == 2
     assert resp.page == 1
     assert resp.total == 8
     assert resp.pages == 4
-    assert resp.offset == 0
+    assert int(resp.offset) == 0
     assert len(resp.movies) == 2
     assert resp.movies[0].name == "The Lord of the Rings Series"
     assert resp.movies[1].name == "The Hobbit Series"
 
 def test_deserialize_quote(quote):
     resp = deserialize_quote(quote)
     assert isinstance(resp, Quote)
```

### Comparing `lotrpy-1.0.0/.gitignore` & `lotrpy-1.0.1/.gitignore`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/LICENSE` & `lotrpy-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/README.md` & `lotrpy-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `lotrpy-1.0.0/PKG-INFO` & `lotrpy-1.0.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lotrpy
-Version: 1.0.0
+Version: 1.0.1
 Summary: Lord Of the Rings Python SDK
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.10.6
 Requires-Dist: requests
```

