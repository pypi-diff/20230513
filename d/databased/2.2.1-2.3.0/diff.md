# Comparing `tmp/databased-2.2.1.tar.gz` & `tmp/databased-2.3.0.tar.gz`

## Comparing `databased-2.2.1.tar` & `databased-2.3.0.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0     6395 2020-02-02 00:00:00.000000 databased-2.2.1/CHANGELOG.md
--rw-r--r--   0        0        0    34933 2020-02-02 00:00:00.000000 databased-2.2.1/docs/databased.html
--rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 databased-2.2.1/docs/index.html
--rw-r--r--   0        0        0    67193 2020-02-02 00:00:00.000000 databased-2.2.1/docs/search.js
--rw-r--r--   0        0        0    44745 2020-02-02 00:00:00.000000 databased-2.2.1/docs/databased/customshell.html
--rw-r--r--   0        0        0   445565 2020-02-02 00:00:00.000000 databased-2.2.1/docs/databased/databased.html
--rw-r--r--   0        0        0   127332 2020-02-02 00:00:00.000000 databased-2.2.1/docs/databased/dbparsers.html
--rw-r--r--   0        0        0   315998 2020-02-02 00:00:00.000000 databased-2.2.1/docs/databased/dbshell.html
--rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 databased-2.2.1/src/databased/__init__.py
--rw-r--r--   0        0        0      740 2020-02-02 00:00:00.000000 databased-2.2.1/src/databased/customshell.py
--rw-r--r--   0        0        0    23517 2020-02-02 00:00:00.000000 databased-2.2.1/src/databased/databased.py
--rw-r--r--   0        0        0     7079 2020-02-02 00:00:00.000000 databased-2.2.1/src/databased/dbparsers.py
--rw-r--r--   0        0        0    14140 2020-02-02 00:00:00.000000 databased-2.2.1/src/databased/dbshell.py
--rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 databased-2.2.1/.gitignore
--rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 databased-2.2.1/LICENSE.txt
--rw-r--r--   0        0        0     7480 2020-02-02 00:00:00.000000 databased-2.2.1/README.md
--rw-r--r--   0        0        0     1133 2020-02-02 00:00:00.000000 databased-2.2.1/pyproject.toml
--rw-r--r--   0        0        0     8166 2020-02-02 00:00:00.000000 databased-2.2.1/PKG-INFO
+-rw-r--r--   0        0        0     6540 2020-02-02 00:00:00.000000 databased-2.3.0/CHANGELOG.md
+-rw-r--r--   0        0        0    34933 2020-02-02 00:00:00.000000 databased-2.3.0/docs/databased.html
+-rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 databased-2.3.0/docs/index.html
+-rw-r--r--   0        0        0    67193 2020-02-02 00:00:00.000000 databased-2.3.0/docs/search.js
+-rw-r--r--   0        0        0    44745 2020-02-02 00:00:00.000000 databased-2.3.0/docs/databased/customshell.html
+-rw-r--r--   0        0        0   428406 2020-02-02 00:00:00.000000 databased-2.3.0/docs/databased/databased.html
+-rw-r--r--   0        0        0   127332 2020-02-02 00:00:00.000000 databased-2.3.0/docs/databased/dbparsers.html
+-rw-r--r--   0        0        0   315998 2020-02-02 00:00:00.000000 databased-2.3.0/docs/databased/dbshell.html
+-rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 databased-2.3.0/src/databased/__init__.py
+-rw-r--r--   0        0        0      740 2020-02-02 00:00:00.000000 databased-2.3.0/src/databased/customshell.py
+-rw-r--r--   0        0        0    21943 2020-02-02 00:00:00.000000 databased-2.3.0/src/databased/databased.py
+-rw-r--r--   0        0        0     7079 2020-02-02 00:00:00.000000 databased-2.3.0/src/databased/dbparsers.py
+-rw-r--r--   0        0        0    14140 2020-02-02 00:00:00.000000 databased-2.3.0/src/databased/dbshell.py
+-rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 databased-2.3.0/.gitignore
+-rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 databased-2.3.0/LICENSE.txt
+-rw-r--r--   0        0        0     7480 2020-02-02 00:00:00.000000 databased-2.3.0/README.md
+-rw-r--r--   0        0        0     1144 2020-02-02 00:00:00.000000 databased-2.3.0/pyproject.toml
+-rw-r--r--   0        0        0     8189 2020-02-02 00:00:00.000000 databased-2.3.0/PKG-INFO
```

### Comparing `databased-2.2.1/CHANGELOG.md` & `databased-2.3.0/CHANGELOG.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,26 @@
 # Changelog
 
-## 2.2.0 (2023-05-08)
+## 2.2.1 (2023-05-08)
+
+#### Fixes
+
+* do_vacuum actually calls vacuum function now
+
+
+## v2.2.0 (2023-05-08)
 
 #### New Features
 
 * add timestamp option to dbshell backup command
+#### Others
+
+* build v2.2.0
+* update changelog
+
 
 ## v2.1.0 (2023-05-08)
 
 #### New Features
 
 * add _disconnect decorator
 * add vacuum()
```

### Comparing `databased-2.2.1/docs/databased.html` & `databased-2.3.0/docs/databased.html`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/docs/search.js` & `databased-2.3.0/docs/search.js`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/docs/databased/customshell.html` & `databased-2.3.0/docs/databased/customshell.html`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/docs/databased/databased.html` & `databased-2.3.0/docs/databased/databased.html`

 * *Files 0% similar despite different names*

```diff
@@ -121,644 +121,607 @@
 </span><span id="L-2"><a href="#L-2"><span class="linenos">  2</span></a><span class="kn">import</span> <span class="nn">os</span>
 </span><span id="L-3"><a href="#L-3"><span class="linenos">  3</span></a><span class="kn">import</span> <span class="nn">sqlite3</span>
 </span><span id="L-4"><a href="#L-4"><span class="linenos">  4</span></a><span class="kn">from</span> <span class="nn">datetime</span> <span class="kn">import</span> <span class="n">datetime</span>
 </span><span id="L-5"><a href="#L-5"><span class="linenos">  5</span></a><span class="kn">from</span> <span class="nn">functools</span> <span class="kn">import</span> <span class="n">wraps</span>
 </span><span id="L-6"><a href="#L-6"><span class="linenos">  6</span></a><span class="kn">from</span> <span class="nn">typing</span> <span class="kn">import</span> <span class="n">Any</span>
 </span><span id="L-7"><a href="#L-7"><span class="linenos">  7</span></a>
 </span><span id="L-8"><a href="#L-8"><span class="linenos">  8</span></a><span class="kn">import</span> <span class="nn">pandas</span>
-</span><span id="L-9"><a href="#L-9"><span class="linenos">  9</span></a><span class="kn">from</span> <span class="nn">pathier</span> <span class="kn">import</span> <span class="n">Pathier</span>
-</span><span id="L-10"><a href="#L-10"><span class="linenos"> 10</span></a><span class="kn">from</span> <span class="nn">tabulate</span> <span class="kn">import</span> <span class="n">tabulate</span>
-</span><span id="L-11"><a href="#L-11"><span class="linenos"> 11</span></a>
+</span><span id="L-9"><a href="#L-9"><span class="linenos">  9</span></a><span class="kn">from</span> <span class="nn">griddle</span> <span class="kn">import</span> <span class="n">griddy</span>
+</span><span id="L-10"><a href="#L-10"><span class="linenos"> 10</span></a><span class="kn">from</span> <span class="nn">pathier</span> <span class="kn">import</span> <span class="n">Pathier</span>
+</span><span id="L-11"><a href="#L-11"><span class="linenos"> 11</span></a><span class="kn">from</span> <span class="nn">tabulate</span> <span class="kn">import</span> <span class="n">tabulate</span>
 </span><span id="L-12"><a href="#L-12"><span class="linenos"> 12</span></a>
-</span><span id="L-13"><a href="#L-13"><span class="linenos"> 13</span></a><span class="k">def</span> <span class="nf">_connect</span><span class="p">(</span><span class="n">func</span><span class="p">):</span>
-</span><span id="L-14"><a href="#L-14"><span class="linenos"> 14</span></a>    <span class="sd">&quot;&quot;&quot;Decorator to open db connection if it isn&#39;t already open.&quot;&quot;&quot;</span>
-</span><span id="L-15"><a href="#L-15"><span class="linenos"> 15</span></a>
-</span><span id="L-16"><a href="#L-16"><span class="linenos"> 16</span></a>    <span class="nd">@wraps</span><span class="p">(</span><span class="n">func</span><span class="p">)</span>
-</span><span id="L-17"><a href="#L-17"><span class="linenos"> 17</span></a>    <span class="k">def</span> <span class="nf">inner</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">):</span>
-</span><span id="L-18"><a href="#L-18"><span class="linenos"> 18</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="L-19"><a href="#L-19"><span class="linenos"> 19</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
-</span><span id="L-20"><a href="#L-20"><span class="linenos"> 20</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="n">func</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">)</span>
-</span><span id="L-21"><a href="#L-21"><span class="linenos"> 21</span></a>        <span class="k">return</span> <span class="n">results</span>
-</span><span id="L-22"><a href="#L-22"><span class="linenos"> 22</span></a>
-</span><span id="L-23"><a href="#L-23"><span class="linenos"> 23</span></a>    <span class="k">return</span> <span class="n">inner</span>
-</span><span id="L-24"><a href="#L-24"><span class="linenos"> 24</span></a>
+</span><span id="L-13"><a href="#L-13"><span class="linenos"> 13</span></a>
+</span><span id="L-14"><a href="#L-14"><span class="linenos"> 14</span></a><span class="k">def</span> <span class="nf">_connect</span><span class="p">(</span><span class="n">func</span><span class="p">):</span>
+</span><span id="L-15"><a href="#L-15"><span class="linenos"> 15</span></a>    <span class="sd">&quot;&quot;&quot;Decorator to open db connection if it isn&#39;t already open.&quot;&quot;&quot;</span>
+</span><span id="L-16"><a href="#L-16"><span class="linenos"> 16</span></a>
+</span><span id="L-17"><a href="#L-17"><span class="linenos"> 17</span></a>    <span class="nd">@wraps</span><span class="p">(</span><span class="n">func</span><span class="p">)</span>
+</span><span id="L-18"><a href="#L-18"><span class="linenos"> 18</span></a>    <span class="k">def</span> <span class="nf">inner</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">):</span>
+</span><span id="L-19"><a href="#L-19"><span class="linenos"> 19</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="L-20"><a href="#L-20"><span class="linenos"> 20</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
+</span><span id="L-21"><a href="#L-21"><span class="linenos"> 21</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="n">func</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">)</span>
+</span><span id="L-22"><a href="#L-22"><span class="linenos"> 22</span></a>        <span class="k">return</span> <span class="n">results</span>
+</span><span id="L-23"><a href="#L-23"><span class="linenos"> 23</span></a>
+</span><span id="L-24"><a href="#L-24"><span class="linenos"> 24</span></a>    <span class="k">return</span> <span class="n">inner</span>
 </span><span id="L-25"><a href="#L-25"><span class="linenos"> 25</span></a>
-</span><span id="L-26"><a href="#L-26"><span class="linenos"> 26</span></a><span class="k">def</span> <span class="nf">_disconnect</span><span class="p">(</span><span class="n">func</span><span class="p">):</span>
-</span><span id="L-27"><a href="#L-27"><span class="linenos"> 27</span></a>    <span class="sd">&quot;&quot;&quot;Decorator to commit and close db connection.</span>
-</span><span id="L-28"><a href="#L-28"><span class="linenos"> 28</span></a>
-</span><span id="L-29"><a href="#L-29"><span class="linenos"> 29</span></a><span class="sd">    Primarily intended for when `DataBased` is subclassed and the inhereting class</span>
-</span><span id="L-30"><a href="#L-30"><span class="linenos"> 30</span></a><span class="sd">    has functions that call parent class functions that are decorated with `_connect`.</span>
-</span><span id="L-31"><a href="#L-31"><span class="linenos"> 31</span></a><span class="sd">    Decorating the child class function with `_disconnect` avoids having to manually close</span>
-</span><span id="L-32"><a href="#L-32"><span class="linenos"> 32</span></a><span class="sd">    the connection or use a context manager in an application.&quot;&quot;&quot;</span>
-</span><span id="L-33"><a href="#L-33"><span class="linenos"> 33</span></a>
-</span><span id="L-34"><a href="#L-34"><span class="linenos"> 34</span></a>    <span class="nd">@wraps</span><span class="p">(</span><span class="n">func</span><span class="p">)</span>
-</span><span id="L-35"><a href="#L-35"><span class="linenos"> 35</span></a>    <span class="k">def</span> <span class="nf">inner</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">):</span>
-</span><span id="L-36"><a href="#L-36"><span class="linenos"> 36</span></a>        <span class="n">result</span> <span class="o">=</span> <span class="n">func</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">)</span>
-</span><span id="L-37"><a href="#L-37"><span class="linenos"> 37</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="L-38"><a href="#L-38"><span class="linenos"> 38</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="L-39"><a href="#L-39"><span class="linenos"> 39</span></a>        <span class="k">return</span> <span class="n">result</span>
-</span><span id="L-40"><a href="#L-40"><span class="linenos"> 40</span></a>
-</span><span id="L-41"><a href="#L-41"><span class="linenos"> 41</span></a>    <span class="k">return</span> <span class="n">inner</span>
-</span><span id="L-42"><a href="#L-42"><span class="linenos"> 42</span></a>
+</span><span id="L-26"><a href="#L-26"><span class="linenos"> 26</span></a>
+</span><span id="L-27"><a href="#L-27"><span class="linenos"> 27</span></a><span class="k">def</span> <span class="nf">_disconnect</span><span class="p">(</span><span class="n">func</span><span class="p">):</span>
+</span><span id="L-28"><a href="#L-28"><span class="linenos"> 28</span></a>    <span class="sd">&quot;&quot;&quot;Decorator to commit and close db connection.</span>
+</span><span id="L-29"><a href="#L-29"><span class="linenos"> 29</span></a>
+</span><span id="L-30"><a href="#L-30"><span class="linenos"> 30</span></a><span class="sd">    Primarily intended for when `DataBased` is subclassed and the inhereting class</span>
+</span><span id="L-31"><a href="#L-31"><span class="linenos"> 31</span></a><span class="sd">    has functions that call parent class functions that are decorated with `_connect`.</span>
+</span><span id="L-32"><a href="#L-32"><span class="linenos"> 32</span></a><span class="sd">    Decorating the child class function with `_disconnect` avoids having to manually close</span>
+</span><span id="L-33"><a href="#L-33"><span class="linenos"> 33</span></a><span class="sd">    the connection or use a context manager in an application.&quot;&quot;&quot;</span>
+</span><span id="L-34"><a href="#L-34"><span class="linenos"> 34</span></a>
+</span><span id="L-35"><a href="#L-35"><span class="linenos"> 35</span></a>    <span class="nd">@wraps</span><span class="p">(</span><span class="n">func</span><span class="p">)</span>
+</span><span id="L-36"><a href="#L-36"><span class="linenos"> 36</span></a>    <span class="k">def</span> <span class="nf">inner</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">):</span>
+</span><span id="L-37"><a href="#L-37"><span class="linenos"> 37</span></a>        <span class="n">result</span> <span class="o">=</span> <span class="n">func</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="o">*</span><span class="n">args</span><span class="p">,</span> <span class="o">**</span><span class="n">kwargs</span><span class="p">)</span>
+</span><span id="L-38"><a href="#L-38"><span class="linenos"> 38</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="L-39"><a href="#L-39"><span class="linenos"> 39</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="L-40"><a href="#L-40"><span class="linenos"> 40</span></a>        <span class="k">return</span> <span class="n">result</span>
+</span><span id="L-41"><a href="#L-41"><span class="linenos"> 41</span></a>
+</span><span id="L-42"><a href="#L-42"><span class="linenos"> 42</span></a>    <span class="k">return</span> <span class="n">inner</span>
 </span><span id="L-43"><a href="#L-43"><span class="linenos"> 43</span></a>
-</span><span id="L-44"><a href="#L-44"><span class="linenos"> 44</span></a><span class="k">class</span> <span class="nc">DataBased</span><span class="p">:</span>
-</span><span id="L-45"><a href="#L-45"><span class="linenos"> 45</span></a>    <span class="sd">&quot;&quot;&quot;Sqli wrapper so queries don&#39;t need to be written except table definitions.</span>
-</span><span id="L-46"><a href="#L-46"><span class="linenos"> 46</span></a>
-</span><span id="L-47"><a href="#L-47"><span class="linenos"> 47</span></a><span class="sd">    Supports saving and reading dates as datetime objects.</span>
-</span><span id="L-48"><a href="#L-48"><span class="linenos"> 48</span></a>
-</span><span id="L-49"><a href="#L-49"><span class="linenos"> 49</span></a><span class="sd">    Supports using a context manager.&quot;&quot;&quot;</span>
-</span><span id="L-50"><a href="#L-50"><span class="linenos"> 50</span></a>
-</span><span id="L-51"><a href="#L-51"><span class="linenos"> 51</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
-</span><span id="L-52"><a href="#L-52"><span class="linenos"> 52</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="L-53"><a href="#L-53"><span class="linenos"> 53</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
-</span><span id="L-54"><a href="#L-54"><span class="linenos"> 54</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
-</span><span id="L-55"><a href="#L-55"><span class="linenos"> 55</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
-</span><span id="L-56"><a href="#L-56"><span class="linenos"> 56</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
-</span><span id="L-57"><a href="#L-57"><span class="linenos"> 57</span></a>    <span class="p">):</span>
-</span><span id="L-58"><a href="#L-58"><span class="linenos"> 58</span></a>        <span class="sd">&quot;&quot;&quot;</span>
-</span><span id="L-59"><a href="#L-59"><span class="linenos"> 59</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-60"><a href="#L-60"><span class="linenos"> 60</span></a>
-</span><span id="L-61"><a href="#L-61"><span class="linenos"> 61</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
-</span><span id="L-62"><a href="#L-62"><span class="linenos"> 62</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
-</span><span id="L-63"><a href="#L-63"><span class="linenos"> 63</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
-</span><span id="L-64"><a href="#L-64"><span class="linenos"> 64</span></a><span class="sd">        same directory.</span>
-</span><span id="L-65"><a href="#L-65"><span class="linenos"> 65</span></a>
-</span><span id="L-66"><a href="#L-66"><span class="linenos"> 66</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
-</span><span id="L-67"><a href="#L-67"><span class="linenos"> 67</span></a>
-</span><span id="L-68"><a href="#L-68"><span class="linenos"> 68</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
-</span><span id="L-69"><a href="#L-69"><span class="linenos"> 69</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
-</span><span id="L-70"><a href="#L-70"><span class="linenos"> 70</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
-</span><span id="L-71"><a href="#L-71"><span class="linenos"> 71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
-</span><span id="L-72"><a href="#L-72"><span class="linenos"> 72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
-</span><span id="L-73"><a href="#L-73"><span class="linenos"> 73</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
-</span><span id="L-74"><a href="#L-74"><span class="linenos"> 74</span></a>        <span class="p">)</span>
-</span><span id="L-75"><a href="#L-75"><span class="linenos"> 75</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="L-76"><a href="#L-76"><span class="linenos"> 76</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
-</span><span id="L-77"><a href="#L-77"><span class="linenos"> 77</span></a>
-</span><span id="L-78"><a href="#L-78"><span class="linenos"> 78</span></a>    <span class="k">def</span> <span class="fm">__enter__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="L-79"><a href="#L-79"><span class="linenos"> 79</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
-</span><span id="L-80"><a href="#L-80"><span class="linenos"> 80</span></a>        <span class="k">return</span> <span class="bp">self</span>
-</span><span id="L-81"><a href="#L-81"><span class="linenos"> 81</span></a>
-</span><span id="L-82"><a href="#L-82"><span class="linenos"> 82</span></a>    <span class="k">def</span> <span class="fm">__exit__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">exception_type</span><span class="p">,</span> <span class="n">exception_value</span><span class="p">,</span> <span class="n">exception_traceback</span><span class="p">):</span>
-</span><span id="L-83"><a href="#L-83"><span class="linenos"> 83</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="L-84"><a href="#L-84"><span class="linenos"> 84</span></a>
-</span><span id="L-85"><a href="#L-85"><span class="linenos"> 85</span></a>    <span class="nd">@property</span>
-</span><span id="L-86"><a href="#L-86"><span class="linenos"> 86</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">float</span><span class="p">:</span>
-</span><span id="L-87"><a href="#L-87"><span class="linenos"> 87</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span>
-</span><span id="L-88"><a href="#L-88"><span class="linenos"> 88</span></a>
-</span><span id="L-89"><a href="#L-89"><span class="linenos"> 89</span></a>    <span class="nd">@connection_timeout</span><span class="o">.</span><span class="n">setter</span>
-</span><span id="L-90"><a href="#L-90"><span class="linenos"> 90</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">num_seconds</span><span class="p">:</span> <span class="nb">float</span><span class="p">):</span>
-</span><span id="L-91"><a href="#L-91"><span class="linenos"> 91</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span> <span class="o">=</span> <span class="n">num_seconds</span>
-</span><span id="L-92"><a href="#L-92"><span class="linenos"> 92</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="L-93"><a href="#L-93"><span class="linenos"> 93</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="L-94"><a href="#L-94"><span class="linenos"> 94</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
-</span><span id="L-95"><a href="#L-95"><span class="linenos"> 95</span></a>
-</span><span id="L-96"><a href="#L-96"><span class="linenos"> 96</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="L-97"><a href="#L-97"><span class="linenos"> 97</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
-</span><span id="L-98"><a href="#L-98"><span class="linenos"> 98</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
-</span><span id="L-99"><a href="#L-99"><span class="linenos"> 99</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
-</span><span id="L-100"><a href="#L-100"><span class="linenos">100</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
-</span><span id="L-101"><a href="#L-101"><span class="linenos">101</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
-</span><span id="L-102"><a href="#L-102"><span class="linenos">102</span></a>        <span class="p">)</span>
-</span><span id="L-103"><a href="#L-103"><span class="linenos">103</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
-</span><span id="L-104"><a href="#L-104"><span class="linenos">104</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
-</span><span id="L-105"><a href="#L-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-106"><a href="#L-106"><span class="linenos">106</span></a>
-</span><span id="L-107"><a href="#L-107"><span class="linenos">107</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="L-108"><a href="#L-108"><span class="linenos">108</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
-</span><span id="L-109"><a href="#L-109"><span class="linenos">109</span></a>
-</span><span id="L-110"><a href="#L-110"><span class="linenos">110</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
-</span><span id="L-111"><a href="#L-111"><span class="linenos">111</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
-</span><span id="L-112"><a href="#L-112"><span class="linenos">112</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="L-113"><a href="#L-113"><span class="linenos">113</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
-</span><span id="L-114"><a href="#L-114"><span class="linenos">114</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="L-115"><a href="#L-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="L-116"><a href="#L-116"><span class="linenos">116</span></a>
-</span><span id="L-117"><a href="#L-117"><span class="linenos">117</span></a>    <span class="k">def</span> <span class="nf">_logger_init</span><span class="p">(</span>
-</span><span id="L-118"><a href="#L-118"><span class="linenos">118</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="L-119"><a href="#L-119"><span class="linenos">119</span></a>        <span class="n">message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
-</span><span id="L-120"><a href="#L-120"><span class="linenos">120</span></a>        <span class="n">encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
-</span><span id="L-121"><a href="#L-121"><span class="linenos">121</span></a>    <span class="p">):</span>
-</span><span id="L-122"><a href="#L-122"><span class="linenos">122</span></a>        <span class="sd">&quot;&quot;&quot;:param `message_format`: &#39;{&#39; style format string&quot;&quot;&quot;</span>
-</span><span id="L-123"><a href="#L-123"><span class="linenos">123</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">logger</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">getLogger</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbname</span><span class="p">)</span>
-</span><span id="L-124"><a href="#L-124"><span class="linenos">124</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">hasHandlers</span><span class="p">():</span>
-</span><span id="L-125"><a href="#L-125"><span class="linenos">125</span></a>            <span class="n">handler</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">FileHandler</span><span class="p">(</span>
-</span><span id="L-126"><a href="#L-126"><span class="linenos">126</span></a>                <span class="nb">str</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">,</span> <span class="s2">&quot;&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;.log&quot;</span><span class="p">,</span> <span class="n">encoding</span><span class="o">=</span><span class="n">encoding</span>
-</span><span id="L-127"><a href="#L-127"><span class="linenos">127</span></a>            <span class="p">)</span>
-</span><span id="L-128"><a href="#L-128"><span class="linenos">128</span></a>            <span class="n">handler</span><span class="o">.</span><span class="n">setFormatter</span><span class="p">(</span>
-</span><span id="L-129"><a href="#L-129"><span class="linenos">129</span></a>                <span class="n">logging</span><span class="o">.</span><span class="n">Formatter</span><span class="p">(</span>
-</span><span id="L-130"><a href="#L-130"><span class="linenos">130</span></a>                    <span class="n">message_format</span><span class="p">,</span> <span class="n">style</span><span class="o">=</span><span class="s2">&quot;{&quot;</span><span class="p">,</span> <span class="n">datefmt</span><span class="o">=</span><span class="s2">&quot;%m/</span><span class="si">%d</span><span class="s2">/%Y %I:%M:%S %p&quot;</span>
-</span><span id="L-131"><a href="#L-131"><span class="linenos">131</span></a>                <span class="p">)</span>
-</span><span id="L-132"><a href="#L-132"><span class="linenos">132</span></a>            <span class="p">)</span>
-</span><span id="L-133"><a href="#L-133"><span class="linenos">133</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">addHandler</span><span class="p">(</span><span class="n">handler</span><span class="p">)</span>
-</span><span id="L-134"><a href="#L-134"><span class="linenos">134</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">setLevel</span><span class="p">(</span><span class="n">logging</span><span class="o">.</span><span class="n">INFO</span><span class="p">)</span>
-</span><span id="L-135"><a href="#L-135"><span class="linenos">135</span></a>
-</span><span id="L-136"><a href="#L-136"><span class="linenos">136</span></a>    <span class="k">def</span> <span class="nf">_get_dict</span><span class="p">(</span>
-</span><span id="L-137"><a href="#L-137"><span class="linenos">137</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-138"><a href="#L-138"><span class="linenos">138</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">dict</span><span class="p">:</span>
-</span><span id="L-139"><a href="#L-139"><span class="linenos">139</span></a>        <span class="sd">&quot;&quot;&quot;Converts the values of a row into a dictionary with column names as keys.</span>
-</span><span id="L-140"><a href="#L-140"><span class="linenos">140</span></a>
-</span><span id="L-141"><a href="#L-141"><span class="linenos">141</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-142"><a href="#L-142"><span class="linenos">142</span></a>
-</span><span id="L-143"><a href="#L-143"><span class="linenos">143</span></a><span class="sd">        `table`: The table that values were pulled from.</span>
-</span><span id="L-144"><a href="#L-144"><span class="linenos">144</span></a>
-</span><span id="L-145"><a href="#L-145"><span class="linenos">145</span></a><span class="sd">        `values`: List of values expected to be the same quantity</span>
-</span><span id="L-146"><a href="#L-146"><span class="linenos">146</span></a><span class="sd">        and in the same order as the column names of table.</span>
-</span><span id="L-147"><a href="#L-147"><span class="linenos">147</span></a>
-</span><span id="L-148"><a href="#L-148"><span class="linenos">148</span></a><span class="sd">        `columns_to_return`: An optional list of column names.</span>
-</span><span id="L-149"><a href="#L-149"><span class="linenos">149</span></a><span class="sd">        If given, only these columns will be included in the returned dictionary.</span>
-</span><span id="L-150"><a href="#L-150"><span class="linenos">150</span></a><span class="sd">        Otherwise all columns and values are returned.&quot;&quot;&quot;</span>
-</span><span id="L-151"><a href="#L-151"><span class="linenos">151</span></a>        <span class="k">return</span> <span class="p">{</span>
-</span><span id="L-152"><a href="#L-152"><span class="linenos">152</span></a>            <span class="n">column</span><span class="p">:</span> <span class="n">value</span>
-</span><span id="L-153"><a href="#L-153"><span class="linenos">153</span></a>            <span class="k">for</span> <span class="n">column</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">zip</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">),</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="L-154"><a href="#L-154"><span class="linenos">154</span></a>            <span class="k">if</span> <span class="ow">not</span> <span class="n">columns_to_return</span> <span class="ow">or</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns_to_return</span>
-</span><span id="L-155"><a href="#L-155"><span class="linenos">155</span></a>        <span class="p">}</span>
-</span><span id="L-156"><a href="#L-156"><span class="linenos">156</span></a>
-</span><span id="L-157"><a href="#L-157"><span class="linenos">157</span></a>    <span class="k">def</span> <span class="nf">_get_conditions</span><span class="p">(</span>
-</span><span id="L-158"><a href="#L-158"><span class="linenos">158</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-159"><a href="#L-159"><span class="linenos">159</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="L-160"><a href="#L-160"><span class="linenos">160</span></a>        <span class="sd">&quot;&quot;&quot;Builds and returns the conditional portion of a query.</span>
-</span><span id="L-161"><a href="#L-161"><span class="linenos">161</span></a>
-</span><span id="L-162"><a href="#L-162"><span class="linenos">162</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-163"><a href="#L-163"><span class="linenos">163</span></a>
-</span><span id="L-164"><a href="#L-164"><span class="linenos">164</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="L-165"><a href="#L-165"><span class="linenos">165</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="L-166"><a href="#L-166"><span class="linenos">166</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="L-167"><a href="#L-167"><span class="linenos">167</span></a>
-</span><span id="L-168"><a href="#L-168"><span class="linenos">168</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
-</span><span id="L-169"><a href="#L-169"><span class="linenos">169</span></a><span class="sd">        will be matched as a substring.</span>
-</span><span id="L-170"><a href="#L-170"><span class="linenos">170</span></a>
-</span><span id="L-171"><a href="#L-171"><span class="linenos">171</span></a><span class="sd">        Usage e.g.:</span>
-</span><span id="L-172"><a href="#L-172"><span class="linenos">172</span></a>
-</span><span id="L-173"><a href="#L-173"><span class="linenos">173</span></a><span class="sd">        &gt;&gt;&gt; self.cursor.execute(f&#39;select * from {table} where {conditions};&#39;)&quot;&quot;&quot;</span>
-</span><span id="L-174"><a href="#L-174"><span class="linenos">174</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">)</span> <span class="o">==</span> <span class="nb">dict</span><span class="p">:</span>
-</span><span id="L-175"><a href="#L-175"><span class="linenos">175</span></a>            <span class="n">match_criteria</span> <span class="o">=</span> <span class="p">[(</span><span class="n">k</span><span class="p">,</span> <span class="n">v</span><span class="p">)</span> <span class="k">for</span> <span class="n">k</span><span class="p">,</span> <span class="n">v</span> <span class="ow">in</span> <span class="n">match_criteria</span><span class="o">.</span><span class="n">items</span><span class="p">()]</span>
-</span><span id="L-176"><a href="#L-176"><span class="linenos">176</span></a>        <span class="k">if</span> <span class="n">exact_match</span><span class="p">:</span>
-</span><span id="L-177"><a href="#L-177"><span class="linenos">177</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
-</span><span id="L-178"><a href="#L-178"><span class="linenos">178</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; = &quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot;&#39;</span>
-</span><span id="L-179"><a href="#L-179"><span class="linenos">179</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
-</span><span id="L-180"><a href="#L-180"><span class="linenos">180</span></a>            <span class="p">)</span>
-</span><span id="L-181"><a href="#L-181"><span class="linenos">181</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="L-182"><a href="#L-182"><span class="linenos">182</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
-</span><span id="L-183"><a href="#L-183"><span class="linenos">183</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; like &quot;%</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">%&quot;&#39;</span>
-</span><span id="L-184"><a href="#L-184"><span class="linenos">184</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
-</span><span id="L-185"><a href="#L-185"><span class="linenos">185</span></a>            <span class="p">)</span>
-</span><span id="L-186"><a href="#L-186"><span class="linenos">186</span></a>        <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;(</span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">)&quot;</span>
-</span><span id="L-187"><a href="#L-187"><span class="linenos">187</span></a>
-</span><span id="L-188"><a href="#L-188"><span class="linenos">188</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="L-189"><a href="#L-189"><span class="linenos">189</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
-</span><span id="L-190"><a href="#L-190"><span class="linenos">190</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
-</span><span id="L-191"><a href="#L-191"><span class="linenos">191</span></a>
-</span><span id="L-192"><a href="#L-192"><span class="linenos">192</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-193"><a href="#L-193"><span class="linenos">193</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
-</span><span id="L-194"><a href="#L-194"><span class="linenos">194</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
-</span><span id="L-195"><a href="#L-195"><span class="linenos">195</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
-</span><span id="L-196"><a href="#L-196"><span class="linenos">196</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
-</span><span id="L-197"><a href="#L-197"><span class="linenos">197</span></a>
-</span><span id="L-198"><a href="#L-198"><span class="linenos">198</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-199"><a href="#L-199"><span class="linenos">199</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
-</span><span id="L-200"><a href="#L-200"><span class="linenos">200</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
-</span><span id="L-201"><a href="#L-201"><span class="linenos">201</span></a>
-</span><span id="L-202"><a href="#L-202"><span class="linenos">202</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
-</span><span id="L-203"><a href="#L-203"><span class="linenos">203</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
-</span><span id="L-204"><a href="#L-204"><span class="linenos">204</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
-</span><span id="L-205"><a href="#L-205"><span class="linenos">205</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
-</span><span id="L-206"><a href="#L-206"><span class="linenos">206</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
-</span><span id="L-207"><a href="#L-207"><span class="linenos">207</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="L-208"><a href="#L-208"><span class="linenos">208</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
-</span><span id="L-209"><a href="#L-209"><span class="linenos">209</span></a>
-</span><span id="L-210"><a href="#L-210"><span class="linenos">210</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-211"><a href="#L-211"><span class="linenos">211</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
-</span><span id="L-212"><a href="#L-212"><span class="linenos">212</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
-</span><span id="L-213"><a href="#L-213"><span class="linenos">213</span></a>
-</span><span id="L-214"><a href="#L-214"><span class="linenos">214</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-215"><a href="#L-215"><span class="linenos">215</span></a>
-</span><span id="L-216"><a href="#L-216"><span class="linenos">216</span></a><span class="sd">        `table`: Name of the table to create.</span>
-</span><span id="L-217"><a href="#L-217"><span class="linenos">217</span></a>
-</span><span id="L-218"><a href="#L-218"><span class="linenos">218</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
-</span><span id="L-219"><a href="#L-219"><span class="linenos">219</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
-</span><span id="L-220"><a href="#L-220"><span class="linenos">220</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
-</span><span id="L-221"><a href="#L-221"><span class="linenos">221</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
-</span><span id="L-222"><a href="#L-222"><span class="linenos">222</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="L-223"><a href="#L-223"><span class="linenos">223</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
-</span><span id="L-224"><a href="#L-224"><span class="linenos">224</span></a>
-</span><span id="L-225"><a href="#L-225"><span class="linenos">225</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-226"><a href="#L-226"><span class="linenos">226</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="L-227"><a href="#L-227"><span class="linenos">227</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
-</span><span id="L-228"><a href="#L-228"><span class="linenos">228</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-229"><a href="#L-229"><span class="linenos">229</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
-</span><span id="L-230"><a href="#L-230"><span class="linenos">230</span></a>        <span class="p">)</span>
-</span><span id="L-231"><a href="#L-231"><span class="linenos">231</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
-</span><span id="L-232"><a href="#L-232"><span class="linenos">232</span></a>
-</span><span id="L-233"><a href="#L-233"><span class="linenos">233</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-234"><a href="#L-234"><span class="linenos">234</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="L-235"><a href="#L-235"><span class="linenos">235</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
-</span><span id="L-236"><a href="#L-236"><span class="linenos">236</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
-</span><span id="L-237"><a href="#L-237"><span class="linenos">237</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
-</span><span id="L-238"><a href="#L-238"><span class="linenos">238</span></a>
-</span><span id="L-239"><a href="#L-239"><span class="linenos">239</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-240"><a href="#L-240"><span class="linenos">240</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
-</span><span id="L-241"><a href="#L-241"><span class="linenos">241</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="L-242"><a href="#L-242"><span class="linenos">242</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="L-243"><a href="#L-243"><span class="linenos">243</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-244"><a href="#L-244"><span class="linenos">244</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="L-245"><a href="#L-245"><span class="linenos">245</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="L-246"><a href="#L-246"><span class="linenos">246</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
-</span><span id="L-247"><a href="#L-247"><span class="linenos">247</span></a>
-</span><span id="L-248"><a href="#L-248"><span class="linenos">248</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-249"><a href="#L-249"><span class="linenos">249</span></a>
-</span><span id="L-250"><a href="#L-250"><span class="linenos">250</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="L-251"><a href="#L-251"><span class="linenos">251</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="L-252"><a href="#L-252"><span class="linenos">252</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="L-253"><a href="#L-253"><span class="linenos">253</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
-</span><span id="L-254"><a href="#L-254"><span class="linenos">254</span></a>
-</span><span id="L-255"><a href="#L-255"><span class="linenos">255</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
-</span><span id="L-256"><a href="#L-256"><span class="linenos">256</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
-</span><span id="L-257"><a href="#L-257"><span class="linenos">257</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
-</span><span id="L-258"><a href="#L-258"><span class="linenos">258</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="L-259"><a href="#L-259"><span class="linenos">259</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="L-260"><a href="#L-260"><span class="linenos">260</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-261"><a href="#L-261"><span class="linenos">261</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="L-262"><a href="#L-262"><span class="linenos">262</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-263"><a href="#L-263"><span class="linenos">263</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="L-264"><a href="#L-264"><span class="linenos">264</span></a>                <span class="p">)</span>
-</span><span id="L-265"><a href="#L-265"><span class="linenos">265</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="L-266"><a href="#L-266"><span class="linenos">266</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="L-267"><a href="#L-267"><span class="linenos">267</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
-</span><span id="L-268"><a href="#L-268"><span class="linenos">268</span></a>        <span class="k">except</span><span class="p">:</span>
-</span><span id="L-269"><a href="#L-269"><span class="linenos">269</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="L-270"><a href="#L-270"><span class="linenos">270</span></a>
-</span><span id="L-271"><a href="#L-271"><span class="linenos">271</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-272"><a href="#L-272"><span class="linenos">272</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
-</span><span id="L-273"><a href="#L-273"><span class="linenos">273</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-274"><a href="#L-274"><span class="linenos">274</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="L-275"><a href="#L-275"><span class="linenos">275</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
-</span><span id="L-276"><a href="#L-276"><span class="linenos">276</span></a>
-</span><span id="L-277"><a href="#L-277"><span class="linenos">277</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
-</span><span id="L-278"><a href="#L-278"><span class="linenos">278</span></a>
-</span><span id="L-279"><a href="#L-279"><span class="linenos">279</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-280"><a href="#L-280"><span class="linenos">280</span></a>
-</span><span id="L-281"><a href="#L-281"><span class="linenos">281</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="L-282"><a href="#L-282"><span class="linenos">282</span></a>
-</span><span id="L-283"><a href="#L-283"><span class="linenos">283</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
-</span><span id="L-284"><a href="#L-284"><span class="linenos">284</span></a>
-</span><span id="L-285"><a href="#L-285"><span class="linenos">285</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="L-286"><a href="#L-286"><span class="linenos">286</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="L-287"><a href="#L-287"><span class="linenos">287</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="L-288"><a href="#L-288"><span class="linenos">288</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="L-289"><a href="#L-289"><span class="linenos">289</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-290"><a href="#L-290"><span class="linenos">290</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="L-291"><a href="#L-291"><span class="linenos">291</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
-</span><span id="L-292"><a href="#L-292"><span class="linenos">292</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-293"><a href="#L-293"><span class="linenos">293</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
-</span><span id="L-294"><a href="#L-294"><span class="linenos">294</span></a>                    <span class="n">values</span><span class="p">,</span>
-</span><span id="L-295"><a href="#L-295"><span class="linenos">295</span></a>                <span class="p">)</span>
-</span><span id="L-296"><a href="#L-296"><span class="linenos">296</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="L-297"><a href="#L-297"><span class="linenos">297</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-298"><a href="#L-298"><span class="linenos">298</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
-</span><span id="L-299"><a href="#L-299"><span class="linenos">299</span></a>                <span class="p">)</span>
-</span><span id="L-300"><a href="#L-300"><span class="linenos">300</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
-</span><span id="L-301"><a href="#L-301"><span class="linenos">301</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="L-302"><a href="#L-302"><span class="linenos">302</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="L-303"><a href="#L-303"><span class="linenos">303</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
-</span><span id="L-304"><a href="#L-304"><span class="linenos">304</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
-</span><span id="L-305"><a href="#L-305"><span class="linenos">305</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
-</span><span id="L-306"><a href="#L-306"><span class="linenos">306</span></a>                <span class="p">)</span>
-</span><span id="L-307"><a href="#L-307"><span class="linenos">307</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="L-308"><a href="#L-308"><span class="linenos">308</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
-</span><span id="L-309"><a href="#L-309"><span class="linenos">309</span></a>            <span class="k">return</span> <span class="kc">False</span>
-</span><span id="L-310"><a href="#L-310"><span class="linenos">310</span></a>
-</span><span id="L-311"><a href="#L-311"><span class="linenos">311</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-312"><a href="#L-312"><span class="linenos">312</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
-</span><span id="L-313"><a href="#L-313"><span class="linenos">313</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-314"><a href="#L-314"><span class="linenos">314</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
-</span><span id="L-315"><a href="#L-315"><span class="linenos">315</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
-</span><span id="L-316"><a href="#L-316"><span class="linenos">316</span></a>
-</span><span id="L-317"><a href="#L-317"><span class="linenos">317</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
-</span><span id="L-318"><a href="#L-318"><span class="linenos">318</span></a>
-</span><span id="L-319"><a href="#L-319"><span class="linenos">319</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-320"><a href="#L-320"><span class="linenos">320</span></a>
-</span><span id="L-321"><a href="#L-321"><span class="linenos">321</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="L-322"><a href="#L-322"><span class="linenos">322</span></a>
-</span><span id="L-323"><a href="#L-323"><span class="linenos">323</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
-</span><span id="L-324"><a href="#L-324"><span class="linenos">324</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
-</span><span id="L-325"><a href="#L-325"><span class="linenos">325</span></a>
-</span><span id="L-326"><a href="#L-326"><span class="linenos">326</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="L-327"><a href="#L-327"><span class="linenos">327</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="L-328"><a href="#L-328"><span class="linenos">328</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="L-329"><a href="#L-329"><span class="linenos">329</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="L-330"><a href="#L-330"><span class="linenos">330</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
-</span><span id="L-331"><a href="#L-331"><span class="linenos">331</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
-</span><span id="L-332"><a href="#L-332"><span class="linenos">332</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="L-333"><a href="#L-333"><span class="linenos">333</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="L-334"><a href="#L-334"><span class="linenos">334</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="L-335"><a href="#L-335"><span class="linenos">335</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
-</span><span id="L-336"><a href="#L-336"><span class="linenos">336</span></a>
-</span><span id="L-337"><a href="#L-337"><span class="linenos">337</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-338"><a href="#L-338"><span class="linenos">338</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
-</span><span id="L-339"><a href="#L-339"><span class="linenos">339</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="L-340"><a href="#L-340"><span class="linenos">340</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="L-341"><a href="#L-341"><span class="linenos">341</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-342"><a href="#L-342"><span class="linenos">342</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="L-343"><a href="#L-343"><span class="linenos">343</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-344"><a href="#L-344"><span class="linenos">344</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-345"><a href="#L-345"><span class="linenos">345</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="L-346"><a href="#L-346"><span class="linenos">346</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="L-347"><a href="#L-347"><span class="linenos">347</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-348"><a href="#L-348"><span class="linenos">348</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-349"><a href="#L-349"><span class="linenos">349</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
-</span><span id="L-350"><a href="#L-350"><span class="linenos">350</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
-</span><span id="L-351"><a href="#L-351"><span class="linenos">351</span></a>
-</span><span id="L-352"><a href="#L-352"><span class="linenos">352</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
-</span><span id="L-353"><a href="#L-353"><span class="linenos">353</span></a>
+</span><span id="L-44"><a href="#L-44"><span class="linenos"> 44</span></a>
+</span><span id="L-45"><a href="#L-45"><span class="linenos"> 45</span></a><span class="k">class</span> <span class="nc">DataBased</span><span class="p">:</span>
+</span><span id="L-46"><a href="#L-46"><span class="linenos"> 46</span></a>    <span class="sd">&quot;&quot;&quot;Sqli wrapper so queries don&#39;t need to be written except table definitions.</span>
+</span><span id="L-47"><a href="#L-47"><span class="linenos"> 47</span></a>
+</span><span id="L-48"><a href="#L-48"><span class="linenos"> 48</span></a><span class="sd">    Supports saving and reading dates as datetime objects.</span>
+</span><span id="L-49"><a href="#L-49"><span class="linenos"> 49</span></a>
+</span><span id="L-50"><a href="#L-50"><span class="linenos"> 50</span></a><span class="sd">    Supports using a context manager.&quot;&quot;&quot;</span>
+</span><span id="L-51"><a href="#L-51"><span class="linenos"> 51</span></a>
+</span><span id="L-52"><a href="#L-52"><span class="linenos"> 52</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
+</span><span id="L-53"><a href="#L-53"><span class="linenos"> 53</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="L-54"><a href="#L-54"><span class="linenos"> 54</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
+</span><span id="L-55"><a href="#L-55"><span class="linenos"> 55</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
+</span><span id="L-56"><a href="#L-56"><span class="linenos"> 56</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
+</span><span id="L-57"><a href="#L-57"><span class="linenos"> 57</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
+</span><span id="L-58"><a href="#L-58"><span class="linenos"> 58</span></a>    <span class="p">):</span>
+</span><span id="L-59"><a href="#L-59"><span class="linenos"> 59</span></a>        <span class="sd">&quot;&quot;&quot;</span>
+</span><span id="L-60"><a href="#L-60"><span class="linenos"> 60</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-61"><a href="#L-61"><span class="linenos"> 61</span></a>
+</span><span id="L-62"><a href="#L-62"><span class="linenos"> 62</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
+</span><span id="L-63"><a href="#L-63"><span class="linenos"> 63</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
+</span><span id="L-64"><a href="#L-64"><span class="linenos"> 64</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
+</span><span id="L-65"><a href="#L-65"><span class="linenos"> 65</span></a><span class="sd">        same directory.</span>
+</span><span id="L-66"><a href="#L-66"><span class="linenos"> 66</span></a>
+</span><span id="L-67"><a href="#L-67"><span class="linenos"> 67</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
+</span><span id="L-68"><a href="#L-68"><span class="linenos"> 68</span></a>
+</span><span id="L-69"><a href="#L-69"><span class="linenos"> 69</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
+</span><span id="L-70"><a href="#L-70"><span class="linenos"> 70</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
+</span><span id="L-71"><a href="#L-71"><span class="linenos"> 71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
+</span><span id="L-72"><a href="#L-72"><span class="linenos"> 72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
+</span><span id="L-73"><a href="#L-73"><span class="linenos"> 73</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
+</span><span id="L-74"><a href="#L-74"><span class="linenos"> 74</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
+</span><span id="L-75"><a href="#L-75"><span class="linenos"> 75</span></a>        <span class="p">)</span>
+</span><span id="L-76"><a href="#L-76"><span class="linenos"> 76</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+</span><span id="L-77"><a href="#L-77"><span class="linenos"> 77</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
+</span><span id="L-78"><a href="#L-78"><span class="linenos"> 78</span></a>
+</span><span id="L-79"><a href="#L-79"><span class="linenos"> 79</span></a>    <span class="k">def</span> <span class="fm">__enter__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="L-80"><a href="#L-80"><span class="linenos"> 80</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
+</span><span id="L-81"><a href="#L-81"><span class="linenos"> 81</span></a>        <span class="k">return</span> <span class="bp">self</span>
+</span><span id="L-82"><a href="#L-82"><span class="linenos"> 82</span></a>
+</span><span id="L-83"><a href="#L-83"><span class="linenos"> 83</span></a>    <span class="k">def</span> <span class="fm">__exit__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">exception_type</span><span class="p">,</span> <span class="n">exception_value</span><span class="p">,</span> <span class="n">exception_traceback</span><span class="p">):</span>
+</span><span id="L-84"><a href="#L-84"><span class="linenos"> 84</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="L-85"><a href="#L-85"><span class="linenos"> 85</span></a>
+</span><span id="L-86"><a href="#L-86"><span class="linenos"> 86</span></a>    <span class="nd">@property</span>
+</span><span id="L-87"><a href="#L-87"><span class="linenos"> 87</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">float</span><span class="p">:</span>
+</span><span id="L-88"><a href="#L-88"><span class="linenos"> 88</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span>
+</span><span id="L-89"><a href="#L-89"><span class="linenos"> 89</span></a>
+</span><span id="L-90"><a href="#L-90"><span class="linenos"> 90</span></a>    <span class="nd">@connection_timeout</span><span class="o">.</span><span class="n">setter</span>
+</span><span id="L-91"><a href="#L-91"><span class="linenos"> 91</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">num_seconds</span><span class="p">:</span> <span class="nb">float</span><span class="p">):</span>
+</span><span id="L-92"><a href="#L-92"><span class="linenos"> 92</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span> <span class="o">=</span> <span class="n">num_seconds</span>
+</span><span id="L-93"><a href="#L-93"><span class="linenos"> 93</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="L-94"><a href="#L-94"><span class="linenos"> 94</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="L-95"><a href="#L-95"><span class="linenos"> 95</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
+</span><span id="L-96"><a href="#L-96"><span class="linenos"> 96</span></a>
+</span><span id="L-97"><a href="#L-97"><span class="linenos"> 97</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="L-98"><a href="#L-98"><span class="linenos"> 98</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
+</span><span id="L-99"><a href="#L-99"><span class="linenos"> 99</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
+</span><span id="L-100"><a href="#L-100"><span class="linenos">100</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
+</span><span id="L-101"><a href="#L-101"><span class="linenos">101</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
+</span><span id="L-102"><a href="#L-102"><span class="linenos">102</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
+</span><span id="L-103"><a href="#L-103"><span class="linenos">103</span></a>        <span class="p">)</span>
+</span><span id="L-104"><a href="#L-104"><span class="linenos">104</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
+</span><span id="L-105"><a href="#L-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
+</span><span id="L-106"><a href="#L-106"><span class="linenos">106</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="L-107"><a href="#L-107"><span class="linenos">107</span></a>
+</span><span id="L-108"><a href="#L-108"><span class="linenos">108</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="L-109"><a href="#L-109"><span class="linenos">109</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
+</span><span id="L-110"><a href="#L-110"><span class="linenos">110</span></a>
+</span><span id="L-111"><a href="#L-111"><span class="linenos">111</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
+</span><span id="L-112"><a href="#L-112"><span class="linenos">112</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
+</span><span id="L-113"><a href="#L-113"><span class="linenos">113</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="L-114"><a href="#L-114"><span class="linenos">114</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
+</span><span id="L-115"><a href="#L-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="L-116"><a href="#L-116"><span class="linenos">116</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+</span><span id="L-117"><a href="#L-117"><span class="linenos">117</span></a>
+</span><span id="L-118"><a href="#L-118"><span class="linenos">118</span></a>    <span class="k">def</span> <span class="nf">_logger_init</span><span class="p">(</span>
+</span><span id="L-119"><a href="#L-119"><span class="linenos">119</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="L-120"><a href="#L-120"><span class="linenos">120</span></a>        <span class="n">message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
+</span><span id="L-121"><a href="#L-121"><span class="linenos">121</span></a>        <span class="n">encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
+</span><span id="L-122"><a href="#L-122"><span class="linenos">122</span></a>    <span class="p">):</span>
+</span><span id="L-123"><a href="#L-123"><span class="linenos">123</span></a>        <span class="sd">&quot;&quot;&quot;:param `message_format`: &#39;{&#39; style format string&quot;&quot;&quot;</span>
+</span><span id="L-124"><a href="#L-124"><span class="linenos">124</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">logger</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">getLogger</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbname</span><span class="p">)</span>
+</span><span id="L-125"><a href="#L-125"><span class="linenos">125</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">hasHandlers</span><span class="p">():</span>
+</span><span id="L-126"><a href="#L-126"><span class="linenos">126</span></a>            <span class="n">handler</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">FileHandler</span><span class="p">(</span>
+</span><span id="L-127"><a href="#L-127"><span class="linenos">127</span></a>                <span class="nb">str</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">,</span> <span class="s2">&quot;&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;.log&quot;</span><span class="p">,</span> <span class="n">encoding</span><span class="o">=</span><span class="n">encoding</span>
+</span><span id="L-128"><a href="#L-128"><span class="linenos">128</span></a>            <span class="p">)</span>
+</span><span id="L-129"><a href="#L-129"><span class="linenos">129</span></a>            <span class="n">handler</span><span class="o">.</span><span class="n">setFormatter</span><span class="p">(</span>
+</span><span id="L-130"><a href="#L-130"><span class="linenos">130</span></a>                <span class="n">logging</span><span class="o">.</span><span class="n">Formatter</span><span class="p">(</span>
+</span><span id="L-131"><a href="#L-131"><span class="linenos">131</span></a>                    <span class="n">message_format</span><span class="p">,</span> <span class="n">style</span><span class="o">=</span><span class="s2">&quot;{&quot;</span><span class="p">,</span> <span class="n">datefmt</span><span class="o">=</span><span class="s2">&quot;%m/</span><span class="si">%d</span><span class="s2">/%Y %I:%M:%S %p&quot;</span>
+</span><span id="L-132"><a href="#L-132"><span class="linenos">132</span></a>                <span class="p">)</span>
+</span><span id="L-133"><a href="#L-133"><span class="linenos">133</span></a>            <span class="p">)</span>
+</span><span id="L-134"><a href="#L-134"><span class="linenos">134</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">addHandler</span><span class="p">(</span><span class="n">handler</span><span class="p">)</span>
+</span><span id="L-135"><a href="#L-135"><span class="linenos">135</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">setLevel</span><span class="p">(</span><span class="n">logging</span><span class="o">.</span><span class="n">INFO</span><span class="p">)</span>
+</span><span id="L-136"><a href="#L-136"><span class="linenos">136</span></a>
+</span><span id="L-137"><a href="#L-137"><span class="linenos">137</span></a>    <span class="k">def</span> <span class="nf">_get_dict</span><span class="p">(</span>
+</span><span id="L-138"><a href="#L-138"><span class="linenos">138</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-139"><a href="#L-139"><span class="linenos">139</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">dict</span><span class="p">:</span>
+</span><span id="L-140"><a href="#L-140"><span class="linenos">140</span></a>        <span class="sd">&quot;&quot;&quot;Converts the values of a row into a dictionary with column names as keys.</span>
+</span><span id="L-141"><a href="#L-141"><span class="linenos">141</span></a>
+</span><span id="L-142"><a href="#L-142"><span class="linenos">142</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-143"><a href="#L-143"><span class="linenos">143</span></a>
+</span><span id="L-144"><a href="#L-144"><span class="linenos">144</span></a><span class="sd">        `table`: The table that values were pulled from.</span>
+</span><span id="L-145"><a href="#L-145"><span class="linenos">145</span></a>
+</span><span id="L-146"><a href="#L-146"><span class="linenos">146</span></a><span class="sd">        `values`: List of values expected to be the same quantity</span>
+</span><span id="L-147"><a href="#L-147"><span class="linenos">147</span></a><span class="sd">        and in the same order as the column names of table.</span>
+</span><span id="L-148"><a href="#L-148"><span class="linenos">148</span></a>
+</span><span id="L-149"><a href="#L-149"><span class="linenos">149</span></a><span class="sd">        `columns_to_return`: An optional list of column names.</span>
+</span><span id="L-150"><a href="#L-150"><span class="linenos">150</span></a><span class="sd">        If given, only these columns will be included in the returned dictionary.</span>
+</span><span id="L-151"><a href="#L-151"><span class="linenos">151</span></a><span class="sd">        Otherwise all columns and values are returned.&quot;&quot;&quot;</span>
+</span><span id="L-152"><a href="#L-152"><span class="linenos">152</span></a>        <span class="k">return</span> <span class="p">{</span>
+</span><span id="L-153"><a href="#L-153"><span class="linenos">153</span></a>            <span class="n">column</span><span class="p">:</span> <span class="n">value</span>
+</span><span id="L-154"><a href="#L-154"><span class="linenos">154</span></a>            <span class="k">for</span> <span class="n">column</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">zip</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">),</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="L-155"><a href="#L-155"><span class="linenos">155</span></a>            <span class="k">if</span> <span class="ow">not</span> <span class="n">columns_to_return</span> <span class="ow">or</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns_to_return</span>
+</span><span id="L-156"><a href="#L-156"><span class="linenos">156</span></a>        <span class="p">}</span>
+</span><span id="L-157"><a href="#L-157"><span class="linenos">157</span></a>
+</span><span id="L-158"><a href="#L-158"><span class="linenos">158</span></a>    <span class="k">def</span> <span class="nf">_get_conditions</span><span class="p">(</span>
+</span><span id="L-159"><a href="#L-159"><span class="linenos">159</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="L-160"><a href="#L-160"><span class="linenos">160</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="L-161"><a href="#L-161"><span class="linenos">161</span></a>        <span class="sd">&quot;&quot;&quot;Builds and returns the conditional portion of a query.</span>
+</span><span id="L-162"><a href="#L-162"><span class="linenos">162</span></a>
+</span><span id="L-163"><a href="#L-163"><span class="linenos">163</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-164"><a href="#L-164"><span class="linenos">164</span></a>
+</span><span id="L-165"><a href="#L-165"><span class="linenos">165</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="L-166"><a href="#L-166"><span class="linenos">166</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="L-167"><a href="#L-167"><span class="linenos">167</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="L-168"><a href="#L-168"><span class="linenos">168</span></a>
+</span><span id="L-169"><a href="#L-169"><span class="linenos">169</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
+</span><span id="L-170"><a href="#L-170"><span class="linenos">170</span></a><span class="sd">        will be matched as a substring.</span>
+</span><span id="L-171"><a href="#L-171"><span class="linenos">171</span></a>
+</span><span id="L-172"><a href="#L-172"><span class="linenos">172</span></a><span class="sd">        Usage e.g.:</span>
+</span><span id="L-173"><a href="#L-173"><span class="linenos">173</span></a>
+</span><span id="L-174"><a href="#L-174"><span class="linenos">174</span></a><span class="sd">        &gt;&gt;&gt; self.cursor.execute(f&#39;select * from {table} where {conditions};&#39;)&quot;&quot;&quot;</span>
+</span><span id="L-175"><a href="#L-175"><span class="linenos">175</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">)</span> <span class="o">==</span> <span class="nb">dict</span><span class="p">:</span>
+</span><span id="L-176"><a href="#L-176"><span class="linenos">176</span></a>            <span class="n">match_criteria</span> <span class="o">=</span> <span class="p">[(</span><span class="n">k</span><span class="p">,</span> <span class="n">v</span><span class="p">)</span> <span class="k">for</span> <span class="n">k</span><span class="p">,</span> <span class="n">v</span> <span class="ow">in</span> <span class="n">match_criteria</span><span class="o">.</span><span class="n">items</span><span class="p">()]</span>
+</span><span id="L-177"><a href="#L-177"><span class="linenos">177</span></a>        <span class="k">if</span> <span class="n">exact_match</span><span class="p">:</span>
+</span><span id="L-178"><a href="#L-178"><span class="linenos">178</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
+</span><span id="L-179"><a href="#L-179"><span class="linenos">179</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; = &quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot;&#39;</span>
+</span><span id="L-180"><a href="#L-180"><span class="linenos">180</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
+</span><span id="L-181"><a href="#L-181"><span class="linenos">181</span></a>            <span class="p">)</span>
+</span><span id="L-182"><a href="#L-182"><span class="linenos">182</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="L-183"><a href="#L-183"><span class="linenos">183</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
+</span><span id="L-184"><a href="#L-184"><span class="linenos">184</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; like &quot;%</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">%&quot;&#39;</span>
+</span><span id="L-185"><a href="#L-185"><span class="linenos">185</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
+</span><span id="L-186"><a href="#L-186"><span class="linenos">186</span></a>            <span class="p">)</span>
+</span><span id="L-187"><a href="#L-187"><span class="linenos">187</span></a>        <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;(</span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">)&quot;</span>
+</span><span id="L-188"><a href="#L-188"><span class="linenos">188</span></a>
+</span><span id="L-189"><a href="#L-189"><span class="linenos">189</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="L-190"><a href="#L-190"><span class="linenos">190</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
+</span><span id="L-191"><a href="#L-191"><span class="linenos">191</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
+</span><span id="L-192"><a href="#L-192"><span class="linenos">192</span></a>
+</span><span id="L-193"><a href="#L-193"><span class="linenos">193</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-194"><a href="#L-194"><span class="linenos">194</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
+</span><span id="L-195"><a href="#L-195"><span class="linenos">195</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
+</span><span id="L-196"><a href="#L-196"><span class="linenos">196</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
+</span><span id="L-197"><a href="#L-197"><span class="linenos">197</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+</span><span id="L-198"><a href="#L-198"><span class="linenos">198</span></a>
+</span><span id="L-199"><a href="#L-199"><span class="linenos">199</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-200"><a href="#L-200"><span class="linenos">200</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
+</span><span id="L-201"><a href="#L-201"><span class="linenos">201</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
+</span><span id="L-202"><a href="#L-202"><span class="linenos">202</span></a>
+</span><span id="L-203"><a href="#L-203"><span class="linenos">203</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
+</span><span id="L-204"><a href="#L-204"><span class="linenos">204</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
+</span><span id="L-205"><a href="#L-205"><span class="linenos">205</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
+</span><span id="L-206"><a href="#L-206"><span class="linenos">206</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
+</span><span id="L-207"><a href="#L-207"><span class="linenos">207</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
+</span><span id="L-208"><a href="#L-208"><span class="linenos">208</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="L-209"><a href="#L-209"><span class="linenos">209</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
+</span><span id="L-210"><a href="#L-210"><span class="linenos">210</span></a>
+</span><span id="L-211"><a href="#L-211"><span class="linenos">211</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-212"><a href="#L-212"><span class="linenos">212</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
+</span><span id="L-213"><a href="#L-213"><span class="linenos">213</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
+</span><span id="L-214"><a href="#L-214"><span class="linenos">214</span></a>
+</span><span id="L-215"><a href="#L-215"><span class="linenos">215</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-216"><a href="#L-216"><span class="linenos">216</span></a>
+</span><span id="L-217"><a href="#L-217"><span class="linenos">217</span></a><span class="sd">        `table`: Name of the table to create.</span>
+</span><span id="L-218"><a href="#L-218"><span class="linenos">218</span></a>
+</span><span id="L-219"><a href="#L-219"><span class="linenos">219</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
+</span><span id="L-220"><a href="#L-220"><span class="linenos">220</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
+</span><span id="L-221"><a href="#L-221"><span class="linenos">221</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
+</span><span id="L-222"><a href="#L-222"><span class="linenos">222</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
+</span><span id="L-223"><a href="#L-223"><span class="linenos">223</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="L-224"><a href="#L-224"><span class="linenos">224</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
+</span><span id="L-225"><a href="#L-225"><span class="linenos">225</span></a>
+</span><span id="L-226"><a href="#L-226"><span class="linenos">226</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-227"><a href="#L-227"><span class="linenos">227</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="L-228"><a href="#L-228"><span class="linenos">228</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
+</span><span id="L-229"><a href="#L-229"><span class="linenos">229</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-230"><a href="#L-230"><span class="linenos">230</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
+</span><span id="L-231"><a href="#L-231"><span class="linenos">231</span></a>        <span class="p">)</span>
+</span><span id="L-232"><a href="#L-232"><span class="linenos">232</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
+</span><span id="L-233"><a href="#L-233"><span class="linenos">233</span></a>
+</span><span id="L-234"><a href="#L-234"><span class="linenos">234</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-235"><a href="#L-235"><span class="linenos">235</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="L-236"><a href="#L-236"><span class="linenos">236</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
+</span><span id="L-237"><a href="#L-237"><span class="linenos">237</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
+</span><span id="L-238"><a href="#L-238"><span class="linenos">238</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
+</span><span id="L-239"><a href="#L-239"><span class="linenos">239</span></a>
+</span><span id="L-240"><a href="#L-240"><span class="linenos">240</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-241"><a href="#L-241"><span class="linenos">241</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
+</span><span id="L-242"><a href="#L-242"><span class="linenos">242</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="L-243"><a href="#L-243"><span class="linenos">243</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="L-244"><a href="#L-244"><span class="linenos">244</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-245"><a href="#L-245"><span class="linenos">245</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="L-246"><a href="#L-246"><span class="linenos">246</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="L-247"><a href="#L-247"><span class="linenos">247</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
+</span><span id="L-248"><a href="#L-248"><span class="linenos">248</span></a>
+</span><span id="L-249"><a href="#L-249"><span class="linenos">249</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-250"><a href="#L-250"><span class="linenos">250</span></a>
+</span><span id="L-251"><a href="#L-251"><span class="linenos">251</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="L-252"><a href="#L-252"><span class="linenos">252</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="L-253"><a href="#L-253"><span class="linenos">253</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="L-254"><a href="#L-254"><span class="linenos">254</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
+</span><span id="L-255"><a href="#L-255"><span class="linenos">255</span></a>
+</span><span id="L-256"><a href="#L-256"><span class="linenos">256</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
+</span><span id="L-257"><a href="#L-257"><span class="linenos">257</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
+</span><span id="L-258"><a href="#L-258"><span class="linenos">258</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
+</span><span id="L-259"><a href="#L-259"><span class="linenos">259</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="L-260"><a href="#L-260"><span class="linenos">260</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="L-261"><a href="#L-261"><span class="linenos">261</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-262"><a href="#L-262"><span class="linenos">262</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="L-263"><a href="#L-263"><span class="linenos">263</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-264"><a href="#L-264"><span class="linenos">264</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="L-265"><a href="#L-265"><span class="linenos">265</span></a>                <span class="p">)</span>
+</span><span id="L-266"><a href="#L-266"><span class="linenos">266</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="L-267"><a href="#L-267"><span class="linenos">267</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="L-268"><a href="#L-268"><span class="linenos">268</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
+</span><span id="L-269"><a href="#L-269"><span class="linenos">269</span></a>        <span class="k">except</span><span class="p">:</span>
+</span><span id="L-270"><a href="#L-270"><span class="linenos">270</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="L-271"><a href="#L-271"><span class="linenos">271</span></a>
+</span><span id="L-272"><a href="#L-272"><span class="linenos">272</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-273"><a href="#L-273"><span class="linenos">273</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
+</span><span id="L-274"><a href="#L-274"><span class="linenos">274</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-275"><a href="#L-275"><span class="linenos">275</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="L-276"><a href="#L-276"><span class="linenos">276</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
+</span><span id="L-277"><a href="#L-277"><span class="linenos">277</span></a>
+</span><span id="L-278"><a href="#L-278"><span class="linenos">278</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
+</span><span id="L-279"><a href="#L-279"><span class="linenos">279</span></a>
+</span><span id="L-280"><a href="#L-280"><span class="linenos">280</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-281"><a href="#L-281"><span class="linenos">281</span></a>
+</span><span id="L-282"><a href="#L-282"><span class="linenos">282</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="L-283"><a href="#L-283"><span class="linenos">283</span></a>
+</span><span id="L-284"><a href="#L-284"><span class="linenos">284</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
+</span><span id="L-285"><a href="#L-285"><span class="linenos">285</span></a>
+</span><span id="L-286"><a href="#L-286"><span class="linenos">286</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="L-287"><a href="#L-287"><span class="linenos">287</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="L-288"><a href="#L-288"><span class="linenos">288</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="L-289"><a href="#L-289"><span class="linenos">289</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="L-290"><a href="#L-290"><span class="linenos">290</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-291"><a href="#L-291"><span class="linenos">291</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="L-292"><a href="#L-292"><span class="linenos">292</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
+</span><span id="L-293"><a href="#L-293"><span class="linenos">293</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-294"><a href="#L-294"><span class="linenos">294</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
+</span><span id="L-295"><a href="#L-295"><span class="linenos">295</span></a>                    <span class="n">values</span><span class="p">,</span>
+</span><span id="L-296"><a href="#L-296"><span class="linenos">296</span></a>                <span class="p">)</span>
+</span><span id="L-297"><a href="#L-297"><span class="linenos">297</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="L-298"><a href="#L-298"><span class="linenos">298</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-299"><a href="#L-299"><span class="linenos">299</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
+</span><span id="L-300"><a href="#L-300"><span class="linenos">300</span></a>                <span class="p">)</span>
+</span><span id="L-301"><a href="#L-301"><span class="linenos">301</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
+</span><span id="L-302"><a href="#L-302"><span class="linenos">302</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="L-303"><a href="#L-303"><span class="linenos">303</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-304"><a href="#L-304"><span class="linenos">304</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
+</span><span id="L-305"><a href="#L-305"><span class="linenos">305</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
+</span><span id="L-306"><a href="#L-306"><span class="linenos">306</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
+</span><span id="L-307"><a href="#L-307"><span class="linenos">307</span></a>                <span class="p">)</span>
+</span><span id="L-308"><a href="#L-308"><span class="linenos">308</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="L-309"><a href="#L-309"><span class="linenos">309</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
+</span><span id="L-310"><a href="#L-310"><span class="linenos">310</span></a>            <span class="k">return</span> <span class="kc">False</span>
+</span><span id="L-311"><a href="#L-311"><span class="linenos">311</span></a>
+</span><span id="L-312"><a href="#L-312"><span class="linenos">312</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-313"><a href="#L-313"><span class="linenos">313</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
+</span><span id="L-314"><a href="#L-314"><span class="linenos">314</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-315"><a href="#L-315"><span class="linenos">315</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
+</span><span id="L-316"><a href="#L-316"><span class="linenos">316</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
+</span><span id="L-317"><a href="#L-317"><span class="linenos">317</span></a>
+</span><span id="L-318"><a href="#L-318"><span class="linenos">318</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
+</span><span id="L-319"><a href="#L-319"><span class="linenos">319</span></a>
+</span><span id="L-320"><a href="#L-320"><span class="linenos">320</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-321"><a href="#L-321"><span class="linenos">321</span></a>
+</span><span id="L-322"><a href="#L-322"><span class="linenos">322</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="L-323"><a href="#L-323"><span class="linenos">323</span></a>
+</span><span id="L-324"><a href="#L-324"><span class="linenos">324</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
+</span><span id="L-325"><a href="#L-325"><span class="linenos">325</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
+</span><span id="L-326"><a href="#L-326"><span class="linenos">326</span></a>
+</span><span id="L-327"><a href="#L-327"><span class="linenos">327</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="L-328"><a href="#L-328"><span class="linenos">328</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="L-329"><a href="#L-329"><span class="linenos">329</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="L-330"><a href="#L-330"><span class="linenos">330</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="L-331"><a href="#L-331"><span class="linenos">331</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
+</span><span id="L-332"><a href="#L-332"><span class="linenos">332</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
+</span><span id="L-333"><a href="#L-333"><span class="linenos">333</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="L-334"><a href="#L-334"><span class="linenos">334</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="L-335"><a href="#L-335"><span class="linenos">335</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="L-336"><a href="#L-336"><span class="linenos">336</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
+</span><span id="L-337"><a href="#L-337"><span class="linenos">337</span></a>
+</span><span id="L-338"><a href="#L-338"><span class="linenos">338</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-339"><a href="#L-339"><span class="linenos">339</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
+</span><span id="L-340"><a href="#L-340"><span class="linenos">340</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="L-341"><a href="#L-341"><span class="linenos">341</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="L-342"><a href="#L-342"><span class="linenos">342</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-343"><a href="#L-343"><span class="linenos">343</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="L-344"><a href="#L-344"><span class="linenos">344</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-345"><a href="#L-345"><span class="linenos">345</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-346"><a href="#L-346"><span class="linenos">346</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="L-347"><a href="#L-347"><span class="linenos">347</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="L-348"><a href="#L-348"><span class="linenos">348</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-349"><a href="#L-349"><span class="linenos">349</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-350"><a href="#L-350"><span class="linenos">350</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
+</span><span id="L-351"><a href="#L-351"><span class="linenos">351</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
+</span><span id="L-352"><a href="#L-352"><span class="linenos">352</span></a>
+</span><span id="L-353"><a href="#L-353"><span class="linenos">353</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
 </span><span id="L-354"><a href="#L-354"><span class="linenos">354</span></a>
-</span><span id="L-355"><a href="#L-355"><span class="linenos">355</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-356"><a href="#L-356"><span class="linenos">356</span></a>
-</span><span id="L-357"><a href="#L-357"><span class="linenos">357</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="L-358"><a href="#L-358"><span class="linenos">358</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="L-359"><a href="#L-359"><span class="linenos">359</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="L-360"><a href="#L-360"><span class="linenos">360</span></a>
-</span><span id="L-361"><a href="#L-361"><span class="linenos">361</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
-</span><span id="L-362"><a href="#L-362"><span class="linenos">362</span></a>
-</span><span id="L-363"><a href="#L-363"><span class="linenos">363</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
-</span><span id="L-364"><a href="#L-364"><span class="linenos">364</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
-</span><span id="L-365"><a href="#L-365"><span class="linenos">365</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
-</span><span id="L-366"><a href="#L-366"><span class="linenos">366</span></a>
-</span><span id="L-367"><a href="#L-367"><span class="linenos">367</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
-</span><span id="L-368"><a href="#L-368"><span class="linenos">368</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
-</span><span id="L-369"><a href="#L-369"><span class="linenos">369</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
-</span><span id="L-370"><a href="#L-370"><span class="linenos">370</span></a>
-</span><span id="L-371"><a href="#L-371"><span class="linenos">371</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
-</span><span id="L-372"><a href="#L-372"><span class="linenos">372</span></a>
-</span><span id="L-373"><a href="#L-373"><span class="linenos">373</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
-</span><span id="L-374"><a href="#L-374"><span class="linenos">374</span></a>
-</span><span id="L-375"><a href="#L-375"><span class="linenos">375</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
-</span><span id="L-376"><a href="#L-376"><span class="linenos">376</span></a>
-</span><span id="L-377"><a href="#L-377"><span class="linenos">377</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
-</span><span id="L-378"><a href="#L-378"><span class="linenos">378</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="L-379"><a href="#L-379"><span class="linenos">379</span></a>
-</span><span id="L-380"><a href="#L-380"><span class="linenos">380</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="L-381"><a href="#L-381"><span class="linenos">381</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
-</span><span id="L-382"><a href="#L-382"><span class="linenos">382</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="L-383"><a href="#L-383"><span class="linenos">383</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="L-384"><a href="#L-384"><span class="linenos">384</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="L-385"><a href="#L-385"><span class="linenos">385</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="L-386"><a href="#L-386"><span class="linenos">386</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
-</span><span id="L-387"><a href="#L-387"><span class="linenos">387</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="L-388"><a href="#L-388"><span class="linenos">388</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
-</span><span id="L-389"><a href="#L-389"><span class="linenos">389</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="L-390"><a href="#L-390"><span class="linenos">390</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="L-391"><a href="#L-391"><span class="linenos">391</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="L-392"><a href="#L-392"><span class="linenos">392</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
-</span><span id="L-393"><a href="#L-393"><span class="linenos">393</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
-</span><span id="L-394"><a href="#L-394"><span class="linenos">394</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
-</span><span id="L-395"><a href="#L-395"><span class="linenos">395</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
-</span><span id="L-396"><a href="#L-396"><span class="linenos">396</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
-</span><span id="L-397"><a href="#L-397"><span class="linenos">397</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
-</span><span id="L-398"><a href="#L-398"><span class="linenos">398</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
-</span><span id="L-399"><a href="#L-399"><span class="linenos">399</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
-</span><span id="L-400"><a href="#L-400"><span class="linenos">400</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="L-401"><a href="#L-401"><span class="linenos">401</span></a>            <span class="k">return</span> <span class="n">results</span>
-</span><span id="L-402"><a href="#L-402"><span class="linenos">402</span></a>
-</span><span id="L-403"><a href="#L-403"><span class="linenos">403</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-404"><a href="#L-404"><span class="linenos">404</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
-</span><span id="L-405"><a href="#L-405"><span class="linenos">405</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-406"><a href="#L-406"><span class="linenos">406</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
-</span><span id="L-407"><a href="#L-407"><span class="linenos">407</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
-</span><span id="L-408"><a href="#L-408"><span class="linenos">408</span></a>
-</span><span id="L-409"><a href="#L-409"><span class="linenos">409</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-410"><a href="#L-410"><span class="linenos">410</span></a>
-</span><span id="L-411"><a href="#L-411"><span class="linenos">411</span></a><span class="sd">        `table`: The table to search.</span>
-</span><span id="L-412"><a href="#L-412"><span class="linenos">412</span></a>
-</span><span id="L-413"><a href="#L-413"><span class="linenos">413</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
-</span><span id="L-414"><a href="#L-414"><span class="linenos">414</span></a>
-</span><span id="L-415"><a href="#L-415"><span class="linenos">415</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
-</span><span id="L-416"><a href="#L-416"><span class="linenos">416</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
-</span><span id="L-417"><a href="#L-417"><span class="linenos">417</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="L-418"><a href="#L-418"><span class="linenos">418</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="L-419"><a href="#L-419"><span class="linenos">419</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
-</span><span id="L-420"><a href="#L-420"><span class="linenos">420</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="L-421"><a href="#L-421"><span class="linenos">421</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="L-422"><a href="#L-422"><span class="linenos">422</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
-</span><span id="L-423"><a href="#L-423"><span class="linenos">423</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="L-424"><a href="#L-424"><span class="linenos">424</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
-</span><span id="L-425"><a href="#L-425"><span class="linenos">425</span></a>                <span class="p">[</span>
-</span><span id="L-426"><a href="#L-426"><span class="linenos">426</span></a>                    <span class="n">row</span>
-</span><span id="L-427"><a href="#L-427"><span class="linenos">427</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
-</span><span id="L-428"><a href="#L-428"><span class="linenos">428</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
-</span><span id="L-429"><a href="#L-429"><span class="linenos">429</span></a>                    <span class="p">)</span>
-</span><span id="L-430"><a href="#L-430"><span class="linenos">430</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
-</span><span id="L-431"><a href="#L-431"><span class="linenos">431</span></a>                <span class="p">]</span>
-</span><span id="L-432"><a href="#L-432"><span class="linenos">432</span></a>            <span class="p">)</span>
-</span><span id="L-433"><a href="#L-433"><span class="linenos">433</span></a>        <span class="k">return</span> <span class="n">results</span>
-</span><span id="L-434"><a href="#L-434"><span class="linenos">434</span></a>
-</span><span id="L-435"><a href="#L-435"><span class="linenos">435</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-436"><a href="#L-436"><span class="linenos">436</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
-</span><span id="L-437"><a href="#L-437"><span class="linenos">437</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-438"><a href="#L-438"><span class="linenos">438</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="L-439"><a href="#L-439"><span class="linenos">439</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
-</span><span id="L-440"><a href="#L-440"><span class="linenos">440</span></a>
-</span><span id="L-441"><a href="#L-441"><span class="linenos">441</span></a><span class="sd">        Returns the number of deleted records.</span>
-</span><span id="L-442"><a href="#L-442"><span class="linenos">442</span></a>
-</span><span id="L-443"><a href="#L-443"><span class="linenos">443</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-444"><a href="#L-444"><span class="linenos">444</span></a>
-</span><span id="L-445"><a href="#L-445"><span class="linenos">445</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
-</span><span id="L-446"><a href="#L-446"><span class="linenos">446</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="L-447"><a href="#L-447"><span class="linenos">447</span></a>
-</span><span id="L-448"><a href="#L-448"><span class="linenos">448</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
-</span><span id="L-449"><a href="#L-449"><span class="linenos">449</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="L-450"><a href="#L-450"><span class="linenos">450</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="L-451"><a href="#L-451"><span class="linenos">451</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-452"><a href="#L-452"><span class="linenos">452</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
-</span><span id="L-453"><a href="#L-453"><span class="linenos">453</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="L-454"><a href="#L-454"><span class="linenos">454</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="L-455"><a href="#L-455"><span class="linenos">455</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
-</span><span id="L-456"><a href="#L-456"><span class="linenos">456</span></a>            <span class="p">)</span>
-</span><span id="L-457"><a href="#L-457"><span class="linenos">457</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
-</span><span id="L-458"><a href="#L-458"><span class="linenos">458</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="L-459"><a href="#L-459"><span class="linenos">459</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
-</span><span id="L-460"><a href="#L-460"><span class="linenos">460</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="L-461"><a href="#L-461"><span class="linenos">461</span></a>            <span class="p">)</span>
-</span><span id="L-462"><a href="#L-462"><span class="linenos">462</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="L-463"><a href="#L-463"><span class="linenos">463</span></a>
-</span><span id="L-464"><a href="#L-464"><span class="linenos">464</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-465"><a href="#L-465"><span class="linenos">465</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
-</span><span id="L-466"><a href="#L-466"><span class="linenos">466</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="L-467"><a href="#L-467"><span class="linenos">467</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="L-468"><a href="#L-468"><span class="linenos">468</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="L-469"><a href="#L-469"><span class="linenos">469</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
-</span><span id="L-470"><a href="#L-470"><span class="linenos">470</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="L-471"><a href="#L-471"><span class="linenos">471</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="L-472"><a href="#L-472"><span class="linenos">472</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="L-473"><a href="#L-473"><span class="linenos">473</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
-</span><span id="L-474"><a href="#L-474"><span class="linenos">474</span></a>
-</span><span id="L-475"><a href="#L-475"><span class="linenos">475</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-476"><a href="#L-476"><span class="linenos">476</span></a>
-</span><span id="L-477"><a href="#L-477"><span class="linenos">477</span></a><span class="sd">        `table`: The table to update rows in.</span>
-</span><span id="L-478"><a href="#L-478"><span class="linenos">478</span></a>
-</span><span id="L-479"><a href="#L-479"><span class="linenos">479</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
-</span><span id="L-480"><a href="#L-480"><span class="linenos">480</span></a>
-</span><span id="L-481"><a href="#L-481"><span class="linenos">481</span></a><span class="sd">        `new_value`: The new value to insert.</span>
-</span><span id="L-482"><a href="#L-482"><span class="linenos">482</span></a>
-</span><span id="L-483"><a href="#L-483"><span class="linenos">483</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
-</span><span id="L-484"><a href="#L-484"><span class="linenos">484</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="L-485"><a href="#L-485"><span class="linenos">485</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
-</span><span id="L-486"><a href="#L-486"><span class="linenos">486</span></a>
-</span><span id="L-487"><a href="#L-487"><span class="linenos">487</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
-</span><span id="L-488"><a href="#L-488"><span class="linenos">488</span></a>
-</span><span id="L-489"><a href="#L-489"><span class="linenos">489</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
-</span><span id="L-490"><a href="#L-490"><span class="linenos">490</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
-</span><span id="L-491"><a href="#L-491"><span class="linenos">491</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
-</span><span id="L-492"><a href="#L-492"><span class="linenos">492</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="L-493"><a href="#L-493"><span class="linenos">493</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="L-494"><a href="#L-494"><span class="linenos">494</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="L-495"><a href="#L-495"><span class="linenos">495</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="L-496"><a href="#L-496"><span class="linenos">496</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-497"><a href="#L-497"><span class="linenos">497</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="L-498"><a href="#L-498"><span class="linenos">498</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-499"><a href="#L-499"><span class="linenos">499</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-500"><a href="#L-500"><span class="linenos">500</span></a>                <span class="n">query</span><span class="p">,</span>
-</span><span id="L-501"><a href="#L-501"><span class="linenos">501</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
-</span><span id="L-502"><a href="#L-502"><span class="linenos">502</span></a>            <span class="p">)</span>
-</span><span id="L-503"><a href="#L-503"><span class="linenos">503</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="L-504"><a href="#L-504"><span class="linenos">504</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="L-505"><a href="#L-505"><span class="linenos">505</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="L-506"><a href="#L-506"><span class="linenos">506</span></a>            <span class="p">)</span>
-</span><span id="L-507"><a href="#L-507"><span class="linenos">507</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
-</span><span id="L-508"><a href="#L-508"><span class="linenos">508</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="L-509"><a href="#L-509"><span class="linenos">509</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
-</span><span id="L-510"><a href="#L-510"><span class="linenos">510</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="L-511"><a href="#L-511"><span class="linenos">511</span></a>            <span class="p">)</span>
-</span><span id="L-512"><a href="#L-512"><span class="linenos">512</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="L-513"><a href="#L-513"><span class="linenos">513</span></a>
-</span><span id="L-514"><a href="#L-514"><span class="linenos">514</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-515"><a href="#L-515"><span class="linenos">515</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="L-516"><a href="#L-516"><span class="linenos">516</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
-</span><span id="L-517"><a href="#L-517"><span class="linenos">517</span></a>
-</span><span id="L-518"><a href="#L-518"><span class="linenos">518</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
-</span><span id="L-519"><a href="#L-519"><span class="linenos">519</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-520"><a href="#L-520"><span class="linenos">520</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="L-521"><a href="#L-521"><span class="linenos">521</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="L-522"><a href="#L-522"><span class="linenos">522</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="L-523"><a href="#L-523"><span class="linenos">523</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="L-524"><a href="#L-524"><span class="linenos">524</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
-</span><span id="L-525"><a href="#L-525"><span class="linenos">525</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="L-526"><a href="#L-526"><span class="linenos">526</span></a>            <span class="k">return</span> <span class="kc">False</span>
-</span><span id="L-527"><a href="#L-527"><span class="linenos">527</span></a>
-</span><span id="L-528"><a href="#L-528"><span class="linenos">528</span></a>    <span class="nd">@_connect</span>
-</span><span id="L-529"><a href="#L-529"><span class="linenos">529</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
-</span><span id="L-530"><a href="#L-530"><span class="linenos">530</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="L-531"><a href="#L-531"><span class="linenos">531</span></a>    <span class="p">):</span>
-</span><span id="L-532"><a href="#L-532"><span class="linenos">532</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
-</span><span id="L-533"><a href="#L-533"><span class="linenos">533</span></a>
-</span><span id="L-534"><a href="#L-534"><span class="linenos">534</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-535"><a href="#L-535"><span class="linenos">535</span></a>
-</span><span id="L-536"><a href="#L-536"><span class="linenos">536</span></a><span class="sd">        `column`: Name of the column to add.</span>
-</span><span id="L-537"><a href="#L-537"><span class="linenos">537</span></a>
-</span><span id="L-538"><a href="#L-538"><span class="linenos">538</span></a><span class="sd">        `_type`: The data type of the new column.</span>
-</span><span id="L-539"><a href="#L-539"><span class="linenos">539</span></a>
-</span><span id="L-540"><a href="#L-540"><span class="linenos">540</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
-</span><span id="L-541"><a href="#L-541"><span class="linenos">541</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="L-542"><a href="#L-542"><span class="linenos">542</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
-</span><span id="L-543"><a href="#L-543"><span class="linenos">543</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-544"><a href="#L-544"><span class="linenos">544</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="L-545"><a href="#L-545"><span class="linenos">545</span></a>                <span class="p">)</span>
-</span><span id="L-546"><a href="#L-546"><span class="linenos">546</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
-</span><span id="L-547"><a href="#L-547"><span class="linenos">547</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="L-548"><a href="#L-548"><span class="linenos">548</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="L-549"><a href="#L-549"><span class="linenos">549</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="L-550"><a href="#L-550"><span class="linenos">550</span></a>                <span class="p">)</span>
-</span><span id="L-551"><a href="#L-551"><span class="linenos">551</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
-</span><span id="L-552"><a href="#L-552"><span class="linenos">552</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="L-553"><a href="#L-553"><span class="linenos">553</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
-</span><span id="L-554"><a href="#L-554"><span class="linenos">554</span></a>
-</span><span id="L-555"><a href="#L-555"><span class="linenos">555</span></a>    <span class="nd">@staticmethod</span>
-</span><span id="L-556"><a href="#L-556"><span class="linenos">556</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
-</span><span id="L-557"><a href="#L-557"><span class="linenos">557</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-558"><a href="#L-558"><span class="linenos">558</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="L-559"><a href="#L-559"><span class="linenos">559</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
-</span><span id="L-560"><a href="#L-560"><span class="linenos">560</span></a>
-</span><span id="L-561"><a href="#L-561"><span class="linenos">561</span></a><span class="sd">        #### :params:</span>
-</span><span id="L-562"><a href="#L-562"><span class="linenos">562</span></a>
-</span><span id="L-563"><a href="#L-563"><span class="linenos">563</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
-</span><span id="L-564"><a href="#L-564"><span class="linenos">564</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
-</span><span id="L-565"><a href="#L-565"><span class="linenos">565</span></a>
-</span><span id="L-566"><a href="#L-566"><span class="linenos">566</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
-</span><span id="L-567"><a href="#L-567"><span class="linenos">567</span></a>
-</span><span id="L-568"><a href="#L-568"><span class="linenos">568</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
-</span><span id="L-569"><a href="#L-569"><span class="linenos">569</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
-</span><span id="L-570"><a href="#L-570"><span class="linenos">570</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
-</span><span id="L-571"><a href="#L-571"><span class="linenos">571</span></a>
+</span><span id="L-355"><a href="#L-355"><span class="linenos">355</span></a>
+</span><span id="L-356"><a href="#L-356"><span class="linenos">356</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-357"><a href="#L-357"><span class="linenos">357</span></a>
+</span><span id="L-358"><a href="#L-358"><span class="linenos">358</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="L-359"><a href="#L-359"><span class="linenos">359</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="L-360"><a href="#L-360"><span class="linenos">360</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="L-361"><a href="#L-361"><span class="linenos">361</span></a>
+</span><span id="L-362"><a href="#L-362"><span class="linenos">362</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
+</span><span id="L-363"><a href="#L-363"><span class="linenos">363</span></a>
+</span><span id="L-364"><a href="#L-364"><span class="linenos">364</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
+</span><span id="L-365"><a href="#L-365"><span class="linenos">365</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
+</span><span id="L-366"><a href="#L-366"><span class="linenos">366</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
+</span><span id="L-367"><a href="#L-367"><span class="linenos">367</span></a>
+</span><span id="L-368"><a href="#L-368"><span class="linenos">368</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
+</span><span id="L-369"><a href="#L-369"><span class="linenos">369</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
+</span><span id="L-370"><a href="#L-370"><span class="linenos">370</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
+</span><span id="L-371"><a href="#L-371"><span class="linenos">371</span></a>
+</span><span id="L-372"><a href="#L-372"><span class="linenos">372</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
+</span><span id="L-373"><a href="#L-373"><span class="linenos">373</span></a>
+</span><span id="L-374"><a href="#L-374"><span class="linenos">374</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
+</span><span id="L-375"><a href="#L-375"><span class="linenos">375</span></a>
+</span><span id="L-376"><a href="#L-376"><span class="linenos">376</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
+</span><span id="L-377"><a href="#L-377"><span class="linenos">377</span></a>
+</span><span id="L-378"><a href="#L-378"><span class="linenos">378</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
+</span><span id="L-379"><a href="#L-379"><span class="linenos">379</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="L-380"><a href="#L-380"><span class="linenos">380</span></a>
+</span><span id="L-381"><a href="#L-381"><span class="linenos">381</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="L-382"><a href="#L-382"><span class="linenos">382</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
+</span><span id="L-383"><a href="#L-383"><span class="linenos">383</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="L-384"><a href="#L-384"><span class="linenos">384</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="L-385"><a href="#L-385"><span class="linenos">385</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="L-386"><a href="#L-386"><span class="linenos">386</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="L-387"><a href="#L-387"><span class="linenos">387</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
+</span><span id="L-388"><a href="#L-388"><span class="linenos">388</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="L-389"><a href="#L-389"><span class="linenos">389</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
+</span><span id="L-390"><a href="#L-390"><span class="linenos">390</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="L-391"><a href="#L-391"><span class="linenos">391</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="L-392"><a href="#L-392"><span class="linenos">392</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="L-393"><a href="#L-393"><span class="linenos">393</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+</span><span id="L-394"><a href="#L-394"><span class="linenos">394</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
+</span><span id="L-395"><a href="#L-395"><span class="linenos">395</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
+</span><span id="L-396"><a href="#L-396"><span class="linenos">396</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
+</span><span id="L-397"><a href="#L-397"><span class="linenos">397</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
+</span><span id="L-398"><a href="#L-398"><span class="linenos">398</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
+</span><span id="L-399"><a href="#L-399"><span class="linenos">399</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
+</span><span id="L-400"><a href="#L-400"><span class="linenos">400</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
+</span><span id="L-401"><a href="#L-401"><span class="linenos">401</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="L-402"><a href="#L-402"><span class="linenos">402</span></a>            <span class="k">return</span> <span class="n">results</span>
+</span><span id="L-403"><a href="#L-403"><span class="linenos">403</span></a>
+</span><span id="L-404"><a href="#L-404"><span class="linenos">404</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-405"><a href="#L-405"><span class="linenos">405</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
+</span><span id="L-406"><a href="#L-406"><span class="linenos">406</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-407"><a href="#L-407"><span class="linenos">407</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
+</span><span id="L-408"><a href="#L-408"><span class="linenos">408</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
+</span><span id="L-409"><a href="#L-409"><span class="linenos">409</span></a>
+</span><span id="L-410"><a href="#L-410"><span class="linenos">410</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-411"><a href="#L-411"><span class="linenos">411</span></a>
+</span><span id="L-412"><a href="#L-412"><span class="linenos">412</span></a><span class="sd">        `table`: The table to search.</span>
+</span><span id="L-413"><a href="#L-413"><span class="linenos">413</span></a>
+</span><span id="L-414"><a href="#L-414"><span class="linenos">414</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
+</span><span id="L-415"><a href="#L-415"><span class="linenos">415</span></a>
+</span><span id="L-416"><a href="#L-416"><span class="linenos">416</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
+</span><span id="L-417"><a href="#L-417"><span class="linenos">417</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
+</span><span id="L-418"><a href="#L-418"><span class="linenos">418</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="L-419"><a href="#L-419"><span class="linenos">419</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="L-420"><a href="#L-420"><span class="linenos">420</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
+</span><span id="L-421"><a href="#L-421"><span class="linenos">421</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="L-422"><a href="#L-422"><span class="linenos">422</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="L-423"><a href="#L-423"><span class="linenos">423</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
+</span><span id="L-424"><a href="#L-424"><span class="linenos">424</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="L-425"><a href="#L-425"><span class="linenos">425</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
+</span><span id="L-426"><a href="#L-426"><span class="linenos">426</span></a>                <span class="p">[</span>
+</span><span id="L-427"><a href="#L-427"><span class="linenos">427</span></a>                    <span class="n">row</span>
+</span><span id="L-428"><a href="#L-428"><span class="linenos">428</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
+</span><span id="L-429"><a href="#L-429"><span class="linenos">429</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
+</span><span id="L-430"><a href="#L-430"><span class="linenos">430</span></a>                    <span class="p">)</span>
+</span><span id="L-431"><a href="#L-431"><span class="linenos">431</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
+</span><span id="L-432"><a href="#L-432"><span class="linenos">432</span></a>                <span class="p">]</span>
+</span><span id="L-433"><a href="#L-433"><span class="linenos">433</span></a>            <span class="p">)</span>
+</span><span id="L-434"><a href="#L-434"><span class="linenos">434</span></a>        <span class="k">return</span> <span class="n">results</span>
+</span><span id="L-435"><a href="#L-435"><span class="linenos">435</span></a>
+</span><span id="L-436"><a href="#L-436"><span class="linenos">436</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-437"><a href="#L-437"><span class="linenos">437</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
+</span><span id="L-438"><a href="#L-438"><span class="linenos">438</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="L-439"><a href="#L-439"><span class="linenos">439</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="L-440"><a href="#L-440"><span class="linenos">440</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
+</span><span id="L-441"><a href="#L-441"><span class="linenos">441</span></a>
+</span><span id="L-442"><a href="#L-442"><span class="linenos">442</span></a><span class="sd">        Returns the number of deleted records.</span>
+</span><span id="L-443"><a href="#L-443"><span class="linenos">443</span></a>
+</span><span id="L-444"><a href="#L-444"><span class="linenos">444</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-445"><a href="#L-445"><span class="linenos">445</span></a>
+</span><span id="L-446"><a href="#L-446"><span class="linenos">446</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
+</span><span id="L-447"><a href="#L-447"><span class="linenos">447</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="L-448"><a href="#L-448"><span class="linenos">448</span></a>
+</span><span id="L-449"><a href="#L-449"><span class="linenos">449</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
+</span><span id="L-450"><a href="#L-450"><span class="linenos">450</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="L-451"><a href="#L-451"><span class="linenos">451</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="L-452"><a href="#L-452"><span class="linenos">452</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-453"><a href="#L-453"><span class="linenos">453</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
+</span><span id="L-454"><a href="#L-454"><span class="linenos">454</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="L-455"><a href="#L-455"><span class="linenos">455</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="L-456"><a href="#L-456"><span class="linenos">456</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
+</span><span id="L-457"><a href="#L-457"><span class="linenos">457</span></a>            <span class="p">)</span>
+</span><span id="L-458"><a href="#L-458"><span class="linenos">458</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
+</span><span id="L-459"><a href="#L-459"><span class="linenos">459</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-460"><a href="#L-460"><span class="linenos">460</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
+</span><span id="L-461"><a href="#L-461"><span class="linenos">461</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="L-462"><a href="#L-462"><span class="linenos">462</span></a>            <span class="p">)</span>
+</span><span id="L-463"><a href="#L-463"><span class="linenos">463</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="L-464"><a href="#L-464"><span class="linenos">464</span></a>
+</span><span id="L-465"><a href="#L-465"><span class="linenos">465</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-466"><a href="#L-466"><span class="linenos">466</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
+</span><span id="L-467"><a href="#L-467"><span class="linenos">467</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="L-468"><a href="#L-468"><span class="linenos">468</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="L-469"><a href="#L-469"><span class="linenos">469</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="L-470"><a href="#L-470"><span class="linenos">470</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
+</span><span id="L-471"><a href="#L-471"><span class="linenos">471</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="L-472"><a href="#L-472"><span class="linenos">472</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="L-473"><a href="#L-473"><span class="linenos">473</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="L-474"><a href="#L-474"><span class="linenos">474</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
+</span><span id="L-475"><a href="#L-475"><span class="linenos">475</span></a>
+</span><span id="L-476"><a href="#L-476"><span class="linenos">476</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-477"><a href="#L-477"><span class="linenos">477</span></a>
+</span><span id="L-478"><a href="#L-478"><span class="linenos">478</span></a><span class="sd">        `table`: The table to update rows in.</span>
+</span><span id="L-479"><a href="#L-479"><span class="linenos">479</span></a>
+</span><span id="L-480"><a href="#L-480"><span class="linenos">480</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
+</span><span id="L-481"><a href="#L-481"><span class="linenos">481</span></a>
+</span><span id="L-482"><a href="#L-482"><span class="linenos">482</span></a><span class="sd">        `new_value`: The new value to insert.</span>
+</span><span id="L-483"><a href="#L-483"><span class="linenos">483</span></a>
+</span><span id="L-484"><a href="#L-484"><span class="linenos">484</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
+</span><span id="L-485"><a href="#L-485"><span class="linenos">485</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="L-486"><a href="#L-486"><span class="linenos">486</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
+</span><span id="L-487"><a href="#L-487"><span class="linenos">487</span></a>
+</span><span id="L-488"><a href="#L-488"><span class="linenos">488</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
+</span><span id="L-489"><a href="#L-489"><span class="linenos">489</span></a>
+</span><span id="L-490"><a href="#L-490"><span class="linenos">490</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
+</span><span id="L-491"><a href="#L-491"><span class="linenos">491</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
+</span><span id="L-492"><a href="#L-492"><span class="linenos">492</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
+</span><span id="L-493"><a href="#L-493"><span class="linenos">493</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="L-494"><a href="#L-494"><span class="linenos">494</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="L-495"><a href="#L-495"><span class="linenos">495</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="L-496"><a href="#L-496"><span class="linenos">496</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="L-497"><a href="#L-497"><span class="linenos">497</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-498"><a href="#L-498"><span class="linenos">498</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="L-499"><a href="#L-499"><span class="linenos">499</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-500"><a href="#L-500"><span class="linenos">500</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-501"><a href="#L-501"><span class="linenos">501</span></a>                <span class="n">query</span><span class="p">,</span>
+</span><span id="L-502"><a href="#L-502"><span class="linenos">502</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
+</span><span id="L-503"><a href="#L-503"><span class="linenos">503</span></a>            <span class="p">)</span>
+</span><span id="L-504"><a href="#L-504"><span class="linenos">504</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="L-505"><a href="#L-505"><span class="linenos">505</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="L-506"><a href="#L-506"><span class="linenos">506</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="L-507"><a href="#L-507"><span class="linenos">507</span></a>            <span class="p">)</span>
+</span><span id="L-508"><a href="#L-508"><span class="linenos">508</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
+</span><span id="L-509"><a href="#L-509"><span class="linenos">509</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-510"><a href="#L-510"><span class="linenos">510</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
+</span><span id="L-511"><a href="#L-511"><span class="linenos">511</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="L-512"><a href="#L-512"><span class="linenos">512</span></a>            <span class="p">)</span>
+</span><span id="L-513"><a href="#L-513"><span class="linenos">513</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="L-514"><a href="#L-514"><span class="linenos">514</span></a>
+</span><span id="L-515"><a href="#L-515"><span class="linenos">515</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-516"><a href="#L-516"><span class="linenos">516</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="L-517"><a href="#L-517"><span class="linenos">517</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
+</span><span id="L-518"><a href="#L-518"><span class="linenos">518</span></a>
+</span><span id="L-519"><a href="#L-519"><span class="linenos">519</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
+</span><span id="L-520"><a href="#L-520"><span class="linenos">520</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-521"><a href="#L-521"><span class="linenos">521</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="L-522"><a href="#L-522"><span class="linenos">522</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="L-523"><a href="#L-523"><span class="linenos">523</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="L-524"><a href="#L-524"><span class="linenos">524</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-525"><a href="#L-525"><span class="linenos">525</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
+</span><span id="L-526"><a href="#L-526"><span class="linenos">526</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="L-527"><a href="#L-527"><span class="linenos">527</span></a>            <span class="k">return</span> <span class="kc">False</span>
+</span><span id="L-528"><a href="#L-528"><span class="linenos">528</span></a>
+</span><span id="L-529"><a href="#L-529"><span class="linenos">529</span></a>    <span class="nd">@_connect</span>
+</span><span id="L-530"><a href="#L-530"><span class="linenos">530</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
+</span><span id="L-531"><a href="#L-531"><span class="linenos">531</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="L-532"><a href="#L-532"><span class="linenos">532</span></a>    <span class="p">):</span>
+</span><span id="L-533"><a href="#L-533"><span class="linenos">533</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
+</span><span id="L-534"><a href="#L-534"><span class="linenos">534</span></a>
+</span><span id="L-535"><a href="#L-535"><span class="linenos">535</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-536"><a href="#L-536"><span class="linenos">536</span></a>
+</span><span id="L-537"><a href="#L-537"><span class="linenos">537</span></a><span class="sd">        `column`: Name of the column to add.</span>
+</span><span id="L-538"><a href="#L-538"><span class="linenos">538</span></a>
+</span><span id="L-539"><a href="#L-539"><span class="linenos">539</span></a><span class="sd">        `_type`: The data type of the new column.</span>
+</span><span id="L-540"><a href="#L-540"><span class="linenos">540</span></a>
+</span><span id="L-541"><a href="#L-541"><span class="linenos">541</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
+</span><span id="L-542"><a href="#L-542"><span class="linenos">542</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="L-543"><a href="#L-543"><span class="linenos">543</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
+</span><span id="L-544"><a href="#L-544"><span class="linenos">544</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-545"><a href="#L-545"><span class="linenos">545</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="L-546"><a href="#L-546"><span class="linenos">546</span></a>                <span class="p">)</span>
+</span><span id="L-547"><a href="#L-547"><span class="linenos">547</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
+</span><span id="L-548"><a href="#L-548"><span class="linenos">548</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="L-549"><a href="#L-549"><span class="linenos">549</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="L-550"><a href="#L-550"><span class="linenos">550</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="L-551"><a href="#L-551"><span class="linenos">551</span></a>                <span class="p">)</span>
+</span><span id="L-552"><a href="#L-552"><span class="linenos">552</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+</span><span id="L-553"><a href="#L-553"><span class="linenos">553</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-554"><a href="#L-554"><span class="linenos">554</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+</span><span id="L-555"><a href="#L-555"><span class="linenos">555</span></a>
+</span><span id="L-556"><a href="#L-556"><span class="linenos">556</span></a>    <span class="nd">@staticmethod</span>
+</span><span id="L-557"><a href="#L-557"><span class="linenos">557</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
+</span><span id="L-558"><a href="#L-558"><span class="linenos">558</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="L-559"><a href="#L-559"><span class="linenos">559</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="L-560"><a href="#L-560"><span class="linenos">560</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
+</span><span id="L-561"><a href="#L-561"><span class="linenos">561</span></a>
+</span><span id="L-562"><a href="#L-562"><span class="linenos">562</span></a><span class="sd">        #### :params:</span>
+</span><span id="L-563"><a href="#L-563"><span class="linenos">563</span></a>
+</span><span id="L-564"><a href="#L-564"><span class="linenos">564</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
+</span><span id="L-565"><a href="#L-565"><span class="linenos">565</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
+</span><span id="L-566"><a href="#L-566"><span class="linenos">566</span></a>
+</span><span id="L-567"><a href="#L-567"><span class="linenos">567</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
+</span><span id="L-568"><a href="#L-568"><span class="linenos">568</span></a>
+</span><span id="L-569"><a href="#L-569"><span class="linenos">569</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
+</span><span id="L-570"><a href="#L-570"><span class="linenos">570</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
+</span><span id="L-571"><a href="#L-571"><span class="linenos">571</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
 </span><span id="L-572"><a href="#L-572"><span class="linenos">572</span></a>
-</span><span id="L-573"><a href="#L-573"><span class="linenos">573</span></a><span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
-</span><span id="L-574"><a href="#L-574"><span class="linenos">574</span></a>    <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-575"><a href="#L-575"><span class="linenos">575</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="L-576"><a href="#L-576"><span class="linenos">576</span></a>    <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
-</span><span id="L-577"><a href="#L-577"><span class="linenos">577</span></a>
-</span><span id="L-578"><a href="#L-578"><span class="linenos">578</span></a><span class="sd">    #### :params:</span>
-</span><span id="L-579"><a href="#L-579"><span class="linenos">579</span></a>
-</span><span id="L-580"><a href="#L-580"><span class="linenos">580</span></a><span class="sd">    `data`: The list of dictionaries to create a grid from.</span>
-</span><span id="L-581"><a href="#L-581"><span class="linenos">581</span></a><span class="sd">    Assumes all dictionaries in list have the same set of keys.</span>
-</span><span id="L-582"><a href="#L-582"><span class="linenos">582</span></a>
-</span><span id="L-583"><a href="#L-583"><span class="linenos">583</span></a><span class="sd">    `sort_key`: Optional dictionary key to sort data with.</span>
-</span><span id="L-584"><a href="#L-584"><span class="linenos">584</span></a>
-</span><span id="L-585"><a href="#L-585"><span class="linenos">585</span></a><span class="sd">    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
-</span><span id="L-586"><a href="#L-586"><span class="linenos">586</span></a><span class="sd">    Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
-</span><span id="L-587"><a href="#L-587"><span class="linenos">587</span></a>    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">data</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
-</span><span id="L-588"><a href="#L-588"><span class="linenos">588</span></a>        <span class="k">return</span> <span class="s2">&quot;&quot;</span>
-</span><span id="L-589"><a href="#L-589"><span class="linenos">589</span></a>    <span class="k">if</span> <span class="n">sort_key</span><span class="p">:</span>
-</span><span id="L-590"><a href="#L-590"><span class="linenos">590</span></a>        <span class="n">data</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">d</span><span class="p">:</span> <span class="n">d</span><span class="p">[</span><span class="n">sort_key</span><span class="p">])</span>
-</span><span id="L-591"><a href="#L-591"><span class="linenos">591</span></a>    <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">d</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">data</span><span class="p">):</span>
-</span><span id="L-592"><a href="#L-592"><span class="linenos">592</span></a>        <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">d</span><span class="p">:</span>
-</span><span id="L-593"><a href="#L-593"><span class="linenos">593</span></a>            <span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">])</span>
-</span><span id="L-594"><a href="#L-594"><span class="linenos">594</span></a>
-</span><span id="L-595"><a href="#L-595"><span class="linenos">595</span></a>    <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="L-596"><a href="#L-596"><span class="linenos">596</span></a>    <span class="n">terminal_width</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">get_terminal_size</span><span class="p">()</span><span class="o">.</span><span class="n">columns</span>
-</span><span id="L-597"><a href="#L-597"><span class="linenos">597</span></a>    <span class="n">max_col_widths</span> <span class="o">=</span> <span class="n">terminal_width</span>
-</span><span id="L-598"><a href="#L-598"><span class="linenos">598</span></a>    <span class="c1"># Make an output with effectively unrestricted column widths</span>
-</span><span id="L-599"><a href="#L-599"><span class="linenos">599</span></a>    <span class="c1"># to see if shrinking is necessary</span>
-</span><span id="L-600"><a href="#L-600"><span class="linenos">600</span></a>    <span class="n">output</span> <span class="o">=</span> <span class="n">tabulate</span><span class="p">(</span>
-</span><span id="L-601"><a href="#L-601"><span class="linenos">601</span></a>        <span class="n">data</span><span class="p">,</span>
-</span><span id="L-602"><a href="#L-602"><span class="linenos">602</span></a>        <span class="n">headers</span><span class="o">=</span><span class="s2">&quot;keys&quot;</span><span class="p">,</span>
-</span><span id="L-603"><a href="#L-603"><span class="linenos">603</span></a>        <span class="n">disable_numparse</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
-</span><span id="L-604"><a href="#L-604"><span class="linenos">604</span></a>        <span class="n">tablefmt</span><span class="o">=</span><span class="s2">&quot;grid&quot;</span><span class="p">,</span>
-</span><span id="L-605"><a href="#L-605"><span class="linenos">605</span></a>        <span class="n">maxcolwidths</span><span class="o">=</span><span class="n">max_col_widths</span><span class="p">,</span>
-</span><span id="L-606"><a href="#L-606"><span class="linenos">606</span></a>    <span class="p">)</span>
-</span><span id="L-607"><a href="#L-607"><span class="linenos">607</span></a>    <span class="n">current_width</span> <span class="o">=</span> <span class="n">output</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="L-608"><a href="#L-608"><span class="linenos">608</span></a>    <span class="k">if</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="L-609"><a href="#L-609"><span class="linenos">609</span></a>        <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="L-610"><a href="#L-610"><span class="linenos">610</span></a>    <span class="k">if</span> <span class="n">wrap_to_terminal</span> <span class="ow">and</span> <span class="n">too_wide</span><span class="p">:</span>
-</span><span id="L-611"><a href="#L-611"><span class="linenos">611</span></a>        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Resizing grid to fit within the terminal...</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="L-612"><a href="#L-612"><span class="linenos">612</span></a>        <span class="n">previous_col_widths</span> <span class="o">=</span> <span class="n">max_col_widths</span>
-</span><span id="L-613"><a href="#L-613"><span class="linenos">613</span></a>        <span class="n">acceptable_width</span> <span class="o">=</span> <span class="n">terminal_width</span> <span class="o">-</span> <span class="mi">10</span>
-</span><span id="L-614"><a href="#L-614"><span class="linenos">614</span></a>        <span class="k">while</span> <span class="n">too_wide</span> <span class="ow">and</span> <span class="n">max_col_widths</span> <span class="o">&gt;</span> <span class="mi">1</span><span class="p">:</span>
-</span><span id="L-615"><a href="#L-615"><span class="linenos">615</span></a>            <span class="k">if</span> <span class="n">current_width</span> <span class="o">&gt;=</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="L-616"><a href="#L-616"><span class="linenos">616</span></a>                <span class="n">previous_col_widths</span> <span class="o">=</span> <span class="n">max_col_widths</span>
-</span><span id="L-617"><a href="#L-617"><span class="linenos">617</span></a>                <span class="n">max_col_widths</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">max_col_widths</span> <span class="o">*</span> <span class="mf">0.5</span><span class="p">)</span>
-</span><span id="L-618"><a href="#L-618"><span class="linenos">618</span></a>            <span class="k">elif</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="L-619"><a href="#L-619"><span class="linenos">619</span></a>                <span class="c1"># Without lowering acceptable_width, this condition will cause infinite loop</span>
-</span><span id="L-620"><a href="#L-620"><span class="linenos">620</span></a>                <span class="k">if</span> <span class="n">max_col_widths</span> <span class="o">==</span> <span class="n">previous_col_widths</span> <span class="o">-</span> <span class="mi">1</span><span class="p">:</span>
-</span><span id="L-621"><a href="#L-621"><span class="linenos">621</span></a>                    <span class="n">acceptable_width</span> <span class="o">-=</span> <span class="mi">10</span>
-</span><span id="L-622"><a href="#L-622"><span class="linenos">622</span></a>                <span class="n">max_col_widths</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span>
-</span><span id="L-623"><a href="#L-623"><span class="linenos">623</span></a>                    <span class="n">max_col_widths</span> <span class="o">+</span> <span class="p">(</span><span class="mf">0.5</span> <span class="o">*</span> <span class="p">(</span><span class="n">previous_col_widths</span> <span class="o">-</span> <span class="n">max_col_widths</span><span class="p">))</span>
-</span><span id="L-624"><a href="#L-624"><span class="linenos">624</span></a>                <span class="p">)</span>
-</span><span id="L-625"><a href="#L-625"><span class="linenos">625</span></a>            <span class="n">output</span> <span class="o">=</span> <span class="n">tabulate</span><span class="p">(</span>
-</span><span id="L-626"><a href="#L-626"><span class="linenos">626</span></a>                <span class="n">data</span><span class="p">,</span>
-</span><span id="L-627"><a href="#L-627"><span class="linenos">627</span></a>                <span class="n">headers</span><span class="o">=</span><span class="s2">&quot;keys&quot;</span><span class="p">,</span>
-</span><span id="L-628"><a href="#L-628"><span class="linenos">628</span></a>                <span class="n">disable_numparse</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
-</span><span id="L-629"><a href="#L-629"><span class="linenos">629</span></a>                <span class="n">tablefmt</span><span class="o">=</span><span class="s2">&quot;grid&quot;</span><span class="p">,</span>
-</span><span id="L-630"><a href="#L-630"><span class="linenos">630</span></a>                <span class="n">maxcolwidths</span><span class="o">=</span><span class="n">max_col_widths</span><span class="p">,</span>
-</span><span id="L-631"><a href="#L-631"><span class="linenos">631</span></a>            <span class="p">)</span>
-</span><span id="L-632"><a href="#L-632"><span class="linenos">632</span></a>            <span class="n">current_width</span> <span class="o">=</span> <span class="n">output</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="L-633"><a href="#L-633"><span class="linenos">633</span></a>            <span class="k">if</span> <span class="n">acceptable_width</span> <span class="o">&lt;</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="L-634"><a href="#L-634"><span class="linenos">634</span></a>                <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="L-635"><a href="#L-635"><span class="linenos">635</span></a>        <span class="k">if</span> <span class="n">too_wide</span><span class="p">:</span>
-</span><span id="L-636"><a href="#L-636"><span class="linenos">636</span></a>            <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Couldn&#39;t resize grid to fit within the terminal.&quot;</span><span class="p">)</span>
-</span><span id="L-637"><a href="#L-637"><span class="linenos">637</span></a>            <span class="k">return</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
-</span><span id="L-638"><a href="#L-638"><span class="linenos">638</span></a>    <span class="k">return</span> <span class="n">output</span>
+</span><span id="L-573"><a href="#L-573"><span class="linenos">573</span></a>
+</span><span id="L-574"><a href="#L-574"><span class="linenos">574</span></a><span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
+</span><span id="L-575"><a href="#L-575"><span class="linenos">575</span></a>    <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="L-576"><a href="#L-576"><span class="linenos">576</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="L-577"><a href="#L-577"><span class="linenos">577</span></a>    <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
+</span><span id="L-578"><a href="#L-578"><span class="linenos">578</span></a>
+</span><span id="L-579"><a href="#L-579"><span class="linenos">579</span></a><span class="sd">    #### :params:</span>
+</span><span id="L-580"><a href="#L-580"><span class="linenos">580</span></a>
+</span><span id="L-581"><a href="#L-581"><span class="linenos">581</span></a><span class="sd">    `data`: The list of dictionaries to create a grid from.</span>
+</span><span id="L-582"><a href="#L-582"><span class="linenos">582</span></a><span class="sd">    Assumes all dictionaries in list have the same set of keys.</span>
+</span><span id="L-583"><a href="#L-583"><span class="linenos">583</span></a>
+</span><span id="L-584"><a href="#L-584"><span class="linenos">584</span></a><span class="sd">    `sort_key`: Optional dictionary key to sort data with.</span>
+</span><span id="L-585"><a href="#L-585"><span class="linenos">585</span></a>
+</span><span id="L-586"><a href="#L-586"><span class="linenos">586</span></a><span class="sd">    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
+</span><span id="L-587"><a href="#L-587"><span class="linenos">587</span></a><span class="sd">    Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
+</span><span id="L-588"><a href="#L-588"><span class="linenos">588</span></a>    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">data</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
+</span><span id="L-589"><a href="#L-589"><span class="linenos">589</span></a>        <span class="k">return</span> <span class="s2">&quot;&quot;</span>
+</span><span id="L-590"><a href="#L-590"><span class="linenos">590</span></a>    <span class="k">if</span> <span class="n">sort_key</span><span class="p">:</span>
+</span><span id="L-591"><a href="#L-591"><span class="linenos">591</span></a>        <span class="n">data</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">d</span><span class="p">:</span> <span class="n">d</span><span class="p">[</span><span class="n">sort_key</span><span class="p">])</span>
+</span><span id="L-592"><a href="#L-592"><span class="linenos">592</span></a>    <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">d</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">data</span><span class="p">):</span>
+</span><span id="L-593"><a href="#L-593"><span class="linenos">593</span></a>        <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">d</span><span class="p">:</span>
+</span><span id="L-594"><a href="#L-594"><span class="linenos">594</span></a>            <span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">])</span>
+</span><span id="L-595"><a href="#L-595"><span class="linenos">595</span></a>
+</span><span id="L-596"><a href="#L-596"><span class="linenos">596</span></a>    <span class="k">try</span><span class="p">:</span>
+</span><span id="L-597"><a href="#L-597"><span class="linenos">597</span></a>        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Resizing grid to fit within the terminal...</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="L-598"><a href="#L-598"><span class="linenos">598</span></a>        <span class="k">return</span> <span class="n">griddy</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="s2">&quot;keys&quot;</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
+</span><span id="L-599"><a href="#L-599"><span class="linenos">599</span></a>    <span class="k">except</span> <span class="ne">RuntimeError</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="L-600"><a href="#L-600"><span class="linenos">600</span></a>        <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
+</span><span id="L-601"><a href="#L-601"><span class="linenos">601</span></a>        <span class="k">return</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
 </span></pre></div>
 
 
             </section>
                 <section id="DataBased">
                             <input id="DataBased-view-source" class="view-source-toggle-state" type="checkbox" aria-hidden="true" tabindex="-1">
 <div class="attr class">
@@ -766,541 +729,541 @@
     <span class="def">class</span>
     <span class="name">DataBased</span>:
 
                 <label class="view-source-button" for="DataBased-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased-45"><a href="#DataBased-45"><span class="linenos"> 45</span></a><span class="k">class</span> <span class="nc">DataBased</span><span class="p">:</span>
-</span><span id="DataBased-46"><a href="#DataBased-46"><span class="linenos"> 46</span></a>    <span class="sd">&quot;&quot;&quot;Sqli wrapper so queries don&#39;t need to be written except table definitions.</span>
-</span><span id="DataBased-47"><a href="#DataBased-47"><span class="linenos"> 47</span></a>
-</span><span id="DataBased-48"><a href="#DataBased-48"><span class="linenos"> 48</span></a><span class="sd">    Supports saving and reading dates as datetime objects.</span>
-</span><span id="DataBased-49"><a href="#DataBased-49"><span class="linenos"> 49</span></a>
-</span><span id="DataBased-50"><a href="#DataBased-50"><span class="linenos"> 50</span></a><span class="sd">    Supports using a context manager.&quot;&quot;&quot;</span>
-</span><span id="DataBased-51"><a href="#DataBased-51"><span class="linenos"> 51</span></a>
-</span><span id="DataBased-52"><a href="#DataBased-52"><span class="linenos"> 52</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
-</span><span id="DataBased-53"><a href="#DataBased-53"><span class="linenos"> 53</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased-54"><a href="#DataBased-54"><span class="linenos"> 54</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
-</span><span id="DataBased-55"><a href="#DataBased-55"><span class="linenos"> 55</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
-</span><span id="DataBased-56"><a href="#DataBased-56"><span class="linenos"> 56</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
-</span><span id="DataBased-57"><a href="#DataBased-57"><span class="linenos"> 57</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
-</span><span id="DataBased-58"><a href="#DataBased-58"><span class="linenos"> 58</span></a>    <span class="p">):</span>
-</span><span id="DataBased-59"><a href="#DataBased-59"><span class="linenos"> 59</span></a>        <span class="sd">&quot;&quot;&quot;</span>
-</span><span id="DataBased-60"><a href="#DataBased-60"><span class="linenos"> 60</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-61"><a href="#DataBased-61"><span class="linenos"> 61</span></a>
-</span><span id="DataBased-62"><a href="#DataBased-62"><span class="linenos"> 62</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
-</span><span id="DataBased-63"><a href="#DataBased-63"><span class="linenos"> 63</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
-</span><span id="DataBased-64"><a href="#DataBased-64"><span class="linenos"> 64</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
-</span><span id="DataBased-65"><a href="#DataBased-65"><span class="linenos"> 65</span></a><span class="sd">        same directory.</span>
-</span><span id="DataBased-66"><a href="#DataBased-66"><span class="linenos"> 66</span></a>
-</span><span id="DataBased-67"><a href="#DataBased-67"><span class="linenos"> 67</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
-</span><span id="DataBased-68"><a href="#DataBased-68"><span class="linenos"> 68</span></a>
-</span><span id="DataBased-69"><a href="#DataBased-69"><span class="linenos"> 69</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
-</span><span id="DataBased-70"><a href="#DataBased-70"><span class="linenos"> 70</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
-</span><span id="DataBased-71"><a href="#DataBased-71"><span class="linenos"> 71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
-</span><span id="DataBased-72"><a href="#DataBased-72"><span class="linenos"> 72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
-</span><span id="DataBased-73"><a href="#DataBased-73"><span class="linenos"> 73</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
-</span><span id="DataBased-74"><a href="#DataBased-74"><span class="linenos"> 74</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
-</span><span id="DataBased-75"><a href="#DataBased-75"><span class="linenos"> 75</span></a>        <span class="p">)</span>
-</span><span id="DataBased-76"><a href="#DataBased-76"><span class="linenos"> 76</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="DataBased-77"><a href="#DataBased-77"><span class="linenos"> 77</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
-</span><span id="DataBased-78"><a href="#DataBased-78"><span class="linenos"> 78</span></a>
-</span><span id="DataBased-79"><a href="#DataBased-79"><span class="linenos"> 79</span></a>    <span class="k">def</span> <span class="fm">__enter__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased-80"><a href="#DataBased-80"><span class="linenos"> 80</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
-</span><span id="DataBased-81"><a href="#DataBased-81"><span class="linenos"> 81</span></a>        <span class="k">return</span> <span class="bp">self</span>
-</span><span id="DataBased-82"><a href="#DataBased-82"><span class="linenos"> 82</span></a>
-</span><span id="DataBased-83"><a href="#DataBased-83"><span class="linenos"> 83</span></a>    <span class="k">def</span> <span class="fm">__exit__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">exception_type</span><span class="p">,</span> <span class="n">exception_value</span><span class="p">,</span> <span class="n">exception_traceback</span><span class="p">):</span>
-</span><span id="DataBased-84"><a href="#DataBased-84"><span class="linenos"> 84</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="DataBased-85"><a href="#DataBased-85"><span class="linenos"> 85</span></a>
-</span><span id="DataBased-86"><a href="#DataBased-86"><span class="linenos"> 86</span></a>    <span class="nd">@property</span>
-</span><span id="DataBased-87"><a href="#DataBased-87"><span class="linenos"> 87</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">float</span><span class="p">:</span>
-</span><span id="DataBased-88"><a href="#DataBased-88"><span class="linenos"> 88</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span>
-</span><span id="DataBased-89"><a href="#DataBased-89"><span class="linenos"> 89</span></a>
-</span><span id="DataBased-90"><a href="#DataBased-90"><span class="linenos"> 90</span></a>    <span class="nd">@connection_timeout</span><span class="o">.</span><span class="n">setter</span>
-</span><span id="DataBased-91"><a href="#DataBased-91"><span class="linenos"> 91</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">num_seconds</span><span class="p">:</span> <span class="nb">float</span><span class="p">):</span>
-</span><span id="DataBased-92"><a href="#DataBased-92"><span class="linenos"> 92</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span> <span class="o">=</span> <span class="n">num_seconds</span>
-</span><span id="DataBased-93"><a href="#DataBased-93"><span class="linenos"> 93</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="DataBased-94"><a href="#DataBased-94"><span class="linenos"> 94</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="DataBased-95"><a href="#DataBased-95"><span class="linenos"> 95</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
-</span><span id="DataBased-96"><a href="#DataBased-96"><span class="linenos"> 96</span></a>
-</span><span id="DataBased-97"><a href="#DataBased-97"><span class="linenos"> 97</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased-98"><a href="#DataBased-98"><span class="linenos"> 98</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
-</span><span id="DataBased-99"><a href="#DataBased-99"><span class="linenos"> 99</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
-</span><span id="DataBased-100"><a href="#DataBased-100"><span class="linenos">100</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
-</span><span id="DataBased-101"><a href="#DataBased-101"><span class="linenos">101</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
-</span><span id="DataBased-102"><a href="#DataBased-102"><span class="linenos">102</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
-</span><span id="DataBased-103"><a href="#DataBased-103"><span class="linenos">103</span></a>        <span class="p">)</span>
-</span><span id="DataBased-104"><a href="#DataBased-104"><span class="linenos">104</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
-</span><span id="DataBased-105"><a href="#DataBased-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
-</span><span id="DataBased-106"><a href="#DataBased-106"><span class="linenos">106</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased-107"><a href="#DataBased-107"><span class="linenos">107</span></a>
-</span><span id="DataBased-108"><a href="#DataBased-108"><span class="linenos">108</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased-109"><a href="#DataBased-109"><span class="linenos">109</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
-</span><span id="DataBased-110"><a href="#DataBased-110"><span class="linenos">110</span></a>
-</span><span id="DataBased-111"><a href="#DataBased-111"><span class="linenos">111</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
-</span><span id="DataBased-112"><a href="#DataBased-112"><span class="linenos">112</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
-</span><span id="DataBased-113"><a href="#DataBased-113"><span class="linenos">113</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="DataBased-114"><a href="#DataBased-114"><span class="linenos">114</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
-</span><span id="DataBased-115"><a href="#DataBased-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="DataBased-116"><a href="#DataBased-116"><span class="linenos">116</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="DataBased-117"><a href="#DataBased-117"><span class="linenos">117</span></a>
-</span><span id="DataBased-118"><a href="#DataBased-118"><span class="linenos">118</span></a>    <span class="k">def</span> <span class="nf">_logger_init</span><span class="p">(</span>
-</span><span id="DataBased-119"><a href="#DataBased-119"><span class="linenos">119</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased-120"><a href="#DataBased-120"><span class="linenos">120</span></a>        <span class="n">message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
-</span><span id="DataBased-121"><a href="#DataBased-121"><span class="linenos">121</span></a>        <span class="n">encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
-</span><span id="DataBased-122"><a href="#DataBased-122"><span class="linenos">122</span></a>    <span class="p">):</span>
-</span><span id="DataBased-123"><a href="#DataBased-123"><span class="linenos">123</span></a>        <span class="sd">&quot;&quot;&quot;:param `message_format`: &#39;{&#39; style format string&quot;&quot;&quot;</span>
-</span><span id="DataBased-124"><a href="#DataBased-124"><span class="linenos">124</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">logger</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">getLogger</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbname</span><span class="p">)</span>
-</span><span id="DataBased-125"><a href="#DataBased-125"><span class="linenos">125</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">hasHandlers</span><span class="p">():</span>
-</span><span id="DataBased-126"><a href="#DataBased-126"><span class="linenos">126</span></a>            <span class="n">handler</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">FileHandler</span><span class="p">(</span>
-</span><span id="DataBased-127"><a href="#DataBased-127"><span class="linenos">127</span></a>                <span class="nb">str</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">,</span> <span class="s2">&quot;&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;.log&quot;</span><span class="p">,</span> <span class="n">encoding</span><span class="o">=</span><span class="n">encoding</span>
-</span><span id="DataBased-128"><a href="#DataBased-128"><span class="linenos">128</span></a>            <span class="p">)</span>
-</span><span id="DataBased-129"><a href="#DataBased-129"><span class="linenos">129</span></a>            <span class="n">handler</span><span class="o">.</span><span class="n">setFormatter</span><span class="p">(</span>
-</span><span id="DataBased-130"><a href="#DataBased-130"><span class="linenos">130</span></a>                <span class="n">logging</span><span class="o">.</span><span class="n">Formatter</span><span class="p">(</span>
-</span><span id="DataBased-131"><a href="#DataBased-131"><span class="linenos">131</span></a>                    <span class="n">message_format</span><span class="p">,</span> <span class="n">style</span><span class="o">=</span><span class="s2">&quot;{&quot;</span><span class="p">,</span> <span class="n">datefmt</span><span class="o">=</span><span class="s2">&quot;%m/</span><span class="si">%d</span><span class="s2">/%Y %I:%M:%S %p&quot;</span>
-</span><span id="DataBased-132"><a href="#DataBased-132"><span class="linenos">132</span></a>                <span class="p">)</span>
-</span><span id="DataBased-133"><a href="#DataBased-133"><span class="linenos">133</span></a>            <span class="p">)</span>
-</span><span id="DataBased-134"><a href="#DataBased-134"><span class="linenos">134</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">addHandler</span><span class="p">(</span><span class="n">handler</span><span class="p">)</span>
-</span><span id="DataBased-135"><a href="#DataBased-135"><span class="linenos">135</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">setLevel</span><span class="p">(</span><span class="n">logging</span><span class="o">.</span><span class="n">INFO</span><span class="p">)</span>
-</span><span id="DataBased-136"><a href="#DataBased-136"><span class="linenos">136</span></a>
-</span><span id="DataBased-137"><a href="#DataBased-137"><span class="linenos">137</span></a>    <span class="k">def</span> <span class="nf">_get_dict</span><span class="p">(</span>
-</span><span id="DataBased-138"><a href="#DataBased-138"><span class="linenos">138</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-139"><a href="#DataBased-139"><span class="linenos">139</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">dict</span><span class="p">:</span>
-</span><span id="DataBased-140"><a href="#DataBased-140"><span class="linenos">140</span></a>        <span class="sd">&quot;&quot;&quot;Converts the values of a row into a dictionary with column names as keys.</span>
-</span><span id="DataBased-141"><a href="#DataBased-141"><span class="linenos">141</span></a>
-</span><span id="DataBased-142"><a href="#DataBased-142"><span class="linenos">142</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-143"><a href="#DataBased-143"><span class="linenos">143</span></a>
-</span><span id="DataBased-144"><a href="#DataBased-144"><span class="linenos">144</span></a><span class="sd">        `table`: The table that values were pulled from.</span>
-</span><span id="DataBased-145"><a href="#DataBased-145"><span class="linenos">145</span></a>
-</span><span id="DataBased-146"><a href="#DataBased-146"><span class="linenos">146</span></a><span class="sd">        `values`: List of values expected to be the same quantity</span>
-</span><span id="DataBased-147"><a href="#DataBased-147"><span class="linenos">147</span></a><span class="sd">        and in the same order as the column names of table.</span>
-</span><span id="DataBased-148"><a href="#DataBased-148"><span class="linenos">148</span></a>
-</span><span id="DataBased-149"><a href="#DataBased-149"><span class="linenos">149</span></a><span class="sd">        `columns_to_return`: An optional list of column names.</span>
-</span><span id="DataBased-150"><a href="#DataBased-150"><span class="linenos">150</span></a><span class="sd">        If given, only these columns will be included in the returned dictionary.</span>
-</span><span id="DataBased-151"><a href="#DataBased-151"><span class="linenos">151</span></a><span class="sd">        Otherwise all columns and values are returned.&quot;&quot;&quot;</span>
-</span><span id="DataBased-152"><a href="#DataBased-152"><span class="linenos">152</span></a>        <span class="k">return</span> <span class="p">{</span>
-</span><span id="DataBased-153"><a href="#DataBased-153"><span class="linenos">153</span></a>            <span class="n">column</span><span class="p">:</span> <span class="n">value</span>
-</span><span id="DataBased-154"><a href="#DataBased-154"><span class="linenos">154</span></a>            <span class="k">for</span> <span class="n">column</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">zip</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">),</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="DataBased-155"><a href="#DataBased-155"><span class="linenos">155</span></a>            <span class="k">if</span> <span class="ow">not</span> <span class="n">columns_to_return</span> <span class="ow">or</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns_to_return</span>
-</span><span id="DataBased-156"><a href="#DataBased-156"><span class="linenos">156</span></a>        <span class="p">}</span>
-</span><span id="DataBased-157"><a href="#DataBased-157"><span class="linenos">157</span></a>
-</span><span id="DataBased-158"><a href="#DataBased-158"><span class="linenos">158</span></a>    <span class="k">def</span> <span class="nf">_get_conditions</span><span class="p">(</span>
-</span><span id="DataBased-159"><a href="#DataBased-159"><span class="linenos">159</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased-160"><a href="#DataBased-160"><span class="linenos">160</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased-161"><a href="#DataBased-161"><span class="linenos">161</span></a>        <span class="sd">&quot;&quot;&quot;Builds and returns the conditional portion of a query.</span>
-</span><span id="DataBased-162"><a href="#DataBased-162"><span class="linenos">162</span></a>
-</span><span id="DataBased-163"><a href="#DataBased-163"><span class="linenos">163</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-164"><a href="#DataBased-164"><span class="linenos">164</span></a>
-</span><span id="DataBased-165"><a href="#DataBased-165"><span class="linenos">165</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="DataBased-166"><a href="#DataBased-166"><span class="linenos">166</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="DataBased-167"><a href="#DataBased-167"><span class="linenos">167</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="DataBased-168"><a href="#DataBased-168"><span class="linenos">168</span></a>
-</span><span id="DataBased-169"><a href="#DataBased-169"><span class="linenos">169</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
-</span><span id="DataBased-170"><a href="#DataBased-170"><span class="linenos">170</span></a><span class="sd">        will be matched as a substring.</span>
-</span><span id="DataBased-171"><a href="#DataBased-171"><span class="linenos">171</span></a>
-</span><span id="DataBased-172"><a href="#DataBased-172"><span class="linenos">172</span></a><span class="sd">        Usage e.g.:</span>
-</span><span id="DataBased-173"><a href="#DataBased-173"><span class="linenos">173</span></a>
-</span><span id="DataBased-174"><a href="#DataBased-174"><span class="linenos">174</span></a><span class="sd">        &gt;&gt;&gt; self.cursor.execute(f&#39;select * from {table} where {conditions};&#39;)&quot;&quot;&quot;</span>
-</span><span id="DataBased-175"><a href="#DataBased-175"><span class="linenos">175</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">)</span> <span class="o">==</span> <span class="nb">dict</span><span class="p">:</span>
-</span><span id="DataBased-176"><a href="#DataBased-176"><span class="linenos">176</span></a>            <span class="n">match_criteria</span> <span class="o">=</span> <span class="p">[(</span><span class="n">k</span><span class="p">,</span> <span class="n">v</span><span class="p">)</span> <span class="k">for</span> <span class="n">k</span><span class="p">,</span> <span class="n">v</span> <span class="ow">in</span> <span class="n">match_criteria</span><span class="o">.</span><span class="n">items</span><span class="p">()]</span>
-</span><span id="DataBased-177"><a href="#DataBased-177"><span class="linenos">177</span></a>        <span class="k">if</span> <span class="n">exact_match</span><span class="p">:</span>
-</span><span id="DataBased-178"><a href="#DataBased-178"><span class="linenos">178</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
-</span><span id="DataBased-179"><a href="#DataBased-179"><span class="linenos">179</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; = &quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot;&#39;</span>
-</span><span id="DataBased-180"><a href="#DataBased-180"><span class="linenos">180</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
-</span><span id="DataBased-181"><a href="#DataBased-181"><span class="linenos">181</span></a>            <span class="p">)</span>
-</span><span id="DataBased-182"><a href="#DataBased-182"><span class="linenos">182</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-183"><a href="#DataBased-183"><span class="linenos">183</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
-</span><span id="DataBased-184"><a href="#DataBased-184"><span class="linenos">184</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; like &quot;%</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">%&quot;&#39;</span>
-</span><span id="DataBased-185"><a href="#DataBased-185"><span class="linenos">185</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
-</span><span id="DataBased-186"><a href="#DataBased-186"><span class="linenos">186</span></a>            <span class="p">)</span>
-</span><span id="DataBased-187"><a href="#DataBased-187"><span class="linenos">187</span></a>        <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;(</span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">)&quot;</span>
-</span><span id="DataBased-188"><a href="#DataBased-188"><span class="linenos">188</span></a>
-</span><span id="DataBased-189"><a href="#DataBased-189"><span class="linenos">189</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased-190"><a href="#DataBased-190"><span class="linenos">190</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
-</span><span id="DataBased-191"><a href="#DataBased-191"><span class="linenos">191</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
-</span><span id="DataBased-192"><a href="#DataBased-192"><span class="linenos">192</span></a>
-</span><span id="DataBased-193"><a href="#DataBased-193"><span class="linenos">193</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-194"><a href="#DataBased-194"><span class="linenos">194</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
-</span><span id="DataBased-195"><a href="#DataBased-195"><span class="linenos">195</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
-</span><span id="DataBased-196"><a href="#DataBased-196"><span class="linenos">196</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
-</span><span id="DataBased-197"><a href="#DataBased-197"><span class="linenos">197</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
-</span><span id="DataBased-198"><a href="#DataBased-198"><span class="linenos">198</span></a>
-</span><span id="DataBased-199"><a href="#DataBased-199"><span class="linenos">199</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-200"><a href="#DataBased-200"><span class="linenos">200</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
-</span><span id="DataBased-201"><a href="#DataBased-201"><span class="linenos">201</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
-</span><span id="DataBased-202"><a href="#DataBased-202"><span class="linenos">202</span></a>
-</span><span id="DataBased-203"><a href="#DataBased-203"><span class="linenos">203</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
-</span><span id="DataBased-204"><a href="#DataBased-204"><span class="linenos">204</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
-</span><span id="DataBased-205"><a href="#DataBased-205"><span class="linenos">205</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
-</span><span id="DataBased-206"><a href="#DataBased-206"><span class="linenos">206</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
-</span><span id="DataBased-207"><a href="#DataBased-207"><span class="linenos">207</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
-</span><span id="DataBased-208"><a href="#DataBased-208"><span class="linenos">208</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="DataBased-209"><a href="#DataBased-209"><span class="linenos">209</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
-</span><span id="DataBased-210"><a href="#DataBased-210"><span class="linenos">210</span></a>
-</span><span id="DataBased-211"><a href="#DataBased-211"><span class="linenos">211</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-212"><a href="#DataBased-212"><span class="linenos">212</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
-</span><span id="DataBased-213"><a href="#DataBased-213"><span class="linenos">213</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
-</span><span id="DataBased-214"><a href="#DataBased-214"><span class="linenos">214</span></a>
-</span><span id="DataBased-215"><a href="#DataBased-215"><span class="linenos">215</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-216"><a href="#DataBased-216"><span class="linenos">216</span></a>
-</span><span id="DataBased-217"><a href="#DataBased-217"><span class="linenos">217</span></a><span class="sd">        `table`: Name of the table to create.</span>
-</span><span id="DataBased-218"><a href="#DataBased-218"><span class="linenos">218</span></a>
-</span><span id="DataBased-219"><a href="#DataBased-219"><span class="linenos">219</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
-</span><span id="DataBased-220"><a href="#DataBased-220"><span class="linenos">220</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
-</span><span id="DataBased-221"><a href="#DataBased-221"><span class="linenos">221</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
-</span><span id="DataBased-222"><a href="#DataBased-222"><span class="linenos">222</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
-</span><span id="DataBased-223"><a href="#DataBased-223"><span class="linenos">223</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="DataBased-224"><a href="#DataBased-224"><span class="linenos">224</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
-</span><span id="DataBased-225"><a href="#DataBased-225"><span class="linenos">225</span></a>
-</span><span id="DataBased-226"><a href="#DataBased-226"><span class="linenos">226</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-227"><a href="#DataBased-227"><span class="linenos">227</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="DataBased-228"><a href="#DataBased-228"><span class="linenos">228</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
-</span><span id="DataBased-229"><a href="#DataBased-229"><span class="linenos">229</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-230"><a href="#DataBased-230"><span class="linenos">230</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
-</span><span id="DataBased-231"><a href="#DataBased-231"><span class="linenos">231</span></a>        <span class="p">)</span>
-</span><span id="DataBased-232"><a href="#DataBased-232"><span class="linenos">232</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
-</span><span id="DataBased-233"><a href="#DataBased-233"><span class="linenos">233</span></a>
-</span><span id="DataBased-234"><a href="#DataBased-234"><span class="linenos">234</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-235"><a href="#DataBased-235"><span class="linenos">235</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="DataBased-236"><a href="#DataBased-236"><span class="linenos">236</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
-</span><span id="DataBased-237"><a href="#DataBased-237"><span class="linenos">237</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
-</span><span id="DataBased-238"><a href="#DataBased-238"><span class="linenos">238</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
-</span><span id="DataBased-239"><a href="#DataBased-239"><span class="linenos">239</span></a>
-</span><span id="DataBased-240"><a href="#DataBased-240"><span class="linenos">240</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-241"><a href="#DataBased-241"><span class="linenos">241</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
-</span><span id="DataBased-242"><a href="#DataBased-242"><span class="linenos">242</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased-243"><a href="#DataBased-243"><span class="linenos">243</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased-244"><a href="#DataBased-244"><span class="linenos">244</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-245"><a href="#DataBased-245"><span class="linenos">245</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased-246"><a href="#DataBased-246"><span class="linenos">246</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased-247"><a href="#DataBased-247"><span class="linenos">247</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
-</span><span id="DataBased-248"><a href="#DataBased-248"><span class="linenos">248</span></a>
-</span><span id="DataBased-249"><a href="#DataBased-249"><span class="linenos">249</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-250"><a href="#DataBased-250"><span class="linenos">250</span></a>
-</span><span id="DataBased-251"><a href="#DataBased-251"><span class="linenos">251</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="DataBased-252"><a href="#DataBased-252"><span class="linenos">252</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="DataBased-253"><a href="#DataBased-253"><span class="linenos">253</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="DataBased-254"><a href="#DataBased-254"><span class="linenos">254</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
-</span><span id="DataBased-255"><a href="#DataBased-255"><span class="linenos">255</span></a>
-</span><span id="DataBased-256"><a href="#DataBased-256"><span class="linenos">256</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
-</span><span id="DataBased-257"><a href="#DataBased-257"><span class="linenos">257</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
-</span><span id="DataBased-258"><a href="#DataBased-258"><span class="linenos">258</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
-</span><span id="DataBased-259"><a href="#DataBased-259"><span class="linenos">259</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased-260"><a href="#DataBased-260"><span class="linenos">260</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="DataBased-261"><a href="#DataBased-261"><span class="linenos">261</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-262"><a href="#DataBased-262"><span class="linenos">262</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased-263"><a href="#DataBased-263"><span class="linenos">263</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-264"><a href="#DataBased-264"><span class="linenos">264</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased-265"><a href="#DataBased-265"><span class="linenos">265</span></a>                <span class="p">)</span>
-</span><span id="DataBased-266"><a href="#DataBased-266"><span class="linenos">266</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-267"><a href="#DataBased-267"><span class="linenos">267</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="DataBased-268"><a href="#DataBased-268"><span class="linenos">268</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
-</span><span id="DataBased-269"><a href="#DataBased-269"><span class="linenos">269</span></a>        <span class="k">except</span><span class="p">:</span>
-</span><span id="DataBased-270"><a href="#DataBased-270"><span class="linenos">270</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="DataBased-271"><a href="#DataBased-271"><span class="linenos">271</span></a>
-</span><span id="DataBased-272"><a href="#DataBased-272"><span class="linenos">272</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-273"><a href="#DataBased-273"><span class="linenos">273</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
-</span><span id="DataBased-274"><a href="#DataBased-274"><span class="linenos">274</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-275"><a href="#DataBased-275"><span class="linenos">275</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="DataBased-276"><a href="#DataBased-276"><span class="linenos">276</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
-</span><span id="DataBased-277"><a href="#DataBased-277"><span class="linenos">277</span></a>
-</span><span id="DataBased-278"><a href="#DataBased-278"><span class="linenos">278</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
-</span><span id="DataBased-279"><a href="#DataBased-279"><span class="linenos">279</span></a>
-</span><span id="DataBased-280"><a href="#DataBased-280"><span class="linenos">280</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-281"><a href="#DataBased-281"><span class="linenos">281</span></a>
-</span><span id="DataBased-282"><a href="#DataBased-282"><span class="linenos">282</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="DataBased-283"><a href="#DataBased-283"><span class="linenos">283</span></a>
-</span><span id="DataBased-284"><a href="#DataBased-284"><span class="linenos">284</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
-</span><span id="DataBased-285"><a href="#DataBased-285"><span class="linenos">285</span></a>
-</span><span id="DataBased-286"><a href="#DataBased-286"><span class="linenos">286</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="DataBased-287"><a href="#DataBased-287"><span class="linenos">287</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="DataBased-288"><a href="#DataBased-288"><span class="linenos">288</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="DataBased-289"><a href="#DataBased-289"><span class="linenos">289</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="DataBased-290"><a href="#DataBased-290"><span class="linenos">290</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-291"><a href="#DataBased-291"><span class="linenos">291</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased-292"><a href="#DataBased-292"><span class="linenos">292</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
-</span><span id="DataBased-293"><a href="#DataBased-293"><span class="linenos">293</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-294"><a href="#DataBased-294"><span class="linenos">294</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
-</span><span id="DataBased-295"><a href="#DataBased-295"><span class="linenos">295</span></a>                    <span class="n">values</span><span class="p">,</span>
-</span><span id="DataBased-296"><a href="#DataBased-296"><span class="linenos">296</span></a>                <span class="p">)</span>
-</span><span id="DataBased-297"><a href="#DataBased-297"><span class="linenos">297</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-298"><a href="#DataBased-298"><span class="linenos">298</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-299"><a href="#DataBased-299"><span class="linenos">299</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
-</span><span id="DataBased-300"><a href="#DataBased-300"><span class="linenos">300</span></a>                <span class="p">)</span>
-</span><span id="DataBased-301"><a href="#DataBased-301"><span class="linenos">301</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
-</span><span id="DataBased-302"><a href="#DataBased-302"><span class="linenos">302</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="DataBased-303"><a href="#DataBased-303"><span class="linenos">303</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased-304"><a href="#DataBased-304"><span class="linenos">304</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
-</span><span id="DataBased-305"><a href="#DataBased-305"><span class="linenos">305</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
-</span><span id="DataBased-306"><a href="#DataBased-306"><span class="linenos">306</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
-</span><span id="DataBased-307"><a href="#DataBased-307"><span class="linenos">307</span></a>                <span class="p">)</span>
-</span><span id="DataBased-308"><a href="#DataBased-308"><span class="linenos">308</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-309"><a href="#DataBased-309"><span class="linenos">309</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
-</span><span id="DataBased-310"><a href="#DataBased-310"><span class="linenos">310</span></a>            <span class="k">return</span> <span class="kc">False</span>
-</span><span id="DataBased-311"><a href="#DataBased-311"><span class="linenos">311</span></a>
-</span><span id="DataBased-312"><a href="#DataBased-312"><span class="linenos">312</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-313"><a href="#DataBased-313"><span class="linenos">313</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
-</span><span id="DataBased-314"><a href="#DataBased-314"><span class="linenos">314</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-315"><a href="#DataBased-315"><span class="linenos">315</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
-</span><span id="DataBased-316"><a href="#DataBased-316"><span class="linenos">316</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
-</span><span id="DataBased-317"><a href="#DataBased-317"><span class="linenos">317</span></a>
-</span><span id="DataBased-318"><a href="#DataBased-318"><span class="linenos">318</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
-</span><span id="DataBased-319"><a href="#DataBased-319"><span class="linenos">319</span></a>
-</span><span id="DataBased-320"><a href="#DataBased-320"><span class="linenos">320</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-321"><a href="#DataBased-321"><span class="linenos">321</span></a>
-</span><span id="DataBased-322"><a href="#DataBased-322"><span class="linenos">322</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="DataBased-323"><a href="#DataBased-323"><span class="linenos">323</span></a>
-</span><span id="DataBased-324"><a href="#DataBased-324"><span class="linenos">324</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
-</span><span id="DataBased-325"><a href="#DataBased-325"><span class="linenos">325</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
-</span><span id="DataBased-326"><a href="#DataBased-326"><span class="linenos">326</span></a>
-</span><span id="DataBased-327"><a href="#DataBased-327"><span class="linenos">327</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="DataBased-328"><a href="#DataBased-328"><span class="linenos">328</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="DataBased-329"><a href="#DataBased-329"><span class="linenos">329</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="DataBased-330"><a href="#DataBased-330"><span class="linenos">330</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="DataBased-331"><a href="#DataBased-331"><span class="linenos">331</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
-</span><span id="DataBased-332"><a href="#DataBased-332"><span class="linenos">332</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
-</span><span id="DataBased-333"><a href="#DataBased-333"><span class="linenos">333</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="DataBased-334"><a href="#DataBased-334"><span class="linenos">334</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-335"><a href="#DataBased-335"><span class="linenos">335</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="DataBased-336"><a href="#DataBased-336"><span class="linenos">336</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
-</span><span id="DataBased-337"><a href="#DataBased-337"><span class="linenos">337</span></a>
-</span><span id="DataBased-338"><a href="#DataBased-338"><span class="linenos">338</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-339"><a href="#DataBased-339"><span class="linenos">339</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
-</span><span id="DataBased-340"><a href="#DataBased-340"><span class="linenos">340</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased-341"><a href="#DataBased-341"><span class="linenos">341</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased-342"><a href="#DataBased-342"><span class="linenos">342</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-343"><a href="#DataBased-343"><span class="linenos">343</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased-344"><a href="#DataBased-344"><span class="linenos">344</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-345"><a href="#DataBased-345"><span class="linenos">345</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-346"><a href="#DataBased-346"><span class="linenos">346</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="DataBased-347"><a href="#DataBased-347"><span class="linenos">347</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="DataBased-348"><a href="#DataBased-348"><span class="linenos">348</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-349"><a href="#DataBased-349"><span class="linenos">349</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-350"><a href="#DataBased-350"><span class="linenos">350</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
-</span><span id="DataBased-351"><a href="#DataBased-351"><span class="linenos">351</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
-</span><span id="DataBased-352"><a href="#DataBased-352"><span class="linenos">352</span></a>
-</span><span id="DataBased-353"><a href="#DataBased-353"><span class="linenos">353</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
-</span><span id="DataBased-354"><a href="#DataBased-354"><span class="linenos">354</span></a>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased-46"><a href="#DataBased-46"><span class="linenos"> 46</span></a><span class="k">class</span> <span class="nc">DataBased</span><span class="p">:</span>
+</span><span id="DataBased-47"><a href="#DataBased-47"><span class="linenos"> 47</span></a>    <span class="sd">&quot;&quot;&quot;Sqli wrapper so queries don&#39;t need to be written except table definitions.</span>
+</span><span id="DataBased-48"><a href="#DataBased-48"><span class="linenos"> 48</span></a>
+</span><span id="DataBased-49"><a href="#DataBased-49"><span class="linenos"> 49</span></a><span class="sd">    Supports saving and reading dates as datetime objects.</span>
+</span><span id="DataBased-50"><a href="#DataBased-50"><span class="linenos"> 50</span></a>
+</span><span id="DataBased-51"><a href="#DataBased-51"><span class="linenos"> 51</span></a><span class="sd">    Supports using a context manager.&quot;&quot;&quot;</span>
+</span><span id="DataBased-52"><a href="#DataBased-52"><span class="linenos"> 52</span></a>
+</span><span id="DataBased-53"><a href="#DataBased-53"><span class="linenos"> 53</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
+</span><span id="DataBased-54"><a href="#DataBased-54"><span class="linenos"> 54</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased-55"><a href="#DataBased-55"><span class="linenos"> 55</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
+</span><span id="DataBased-56"><a href="#DataBased-56"><span class="linenos"> 56</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
+</span><span id="DataBased-57"><a href="#DataBased-57"><span class="linenos"> 57</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
+</span><span id="DataBased-58"><a href="#DataBased-58"><span class="linenos"> 58</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
+</span><span id="DataBased-59"><a href="#DataBased-59"><span class="linenos"> 59</span></a>    <span class="p">):</span>
+</span><span id="DataBased-60"><a href="#DataBased-60"><span class="linenos"> 60</span></a>        <span class="sd">&quot;&quot;&quot;</span>
+</span><span id="DataBased-61"><a href="#DataBased-61"><span class="linenos"> 61</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-62"><a href="#DataBased-62"><span class="linenos"> 62</span></a>
+</span><span id="DataBased-63"><a href="#DataBased-63"><span class="linenos"> 63</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
+</span><span id="DataBased-64"><a href="#DataBased-64"><span class="linenos"> 64</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
+</span><span id="DataBased-65"><a href="#DataBased-65"><span class="linenos"> 65</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
+</span><span id="DataBased-66"><a href="#DataBased-66"><span class="linenos"> 66</span></a><span class="sd">        same directory.</span>
+</span><span id="DataBased-67"><a href="#DataBased-67"><span class="linenos"> 67</span></a>
+</span><span id="DataBased-68"><a href="#DataBased-68"><span class="linenos"> 68</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
+</span><span id="DataBased-69"><a href="#DataBased-69"><span class="linenos"> 69</span></a>
+</span><span id="DataBased-70"><a href="#DataBased-70"><span class="linenos"> 70</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
+</span><span id="DataBased-71"><a href="#DataBased-71"><span class="linenos"> 71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
+</span><span id="DataBased-72"><a href="#DataBased-72"><span class="linenos"> 72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
+</span><span id="DataBased-73"><a href="#DataBased-73"><span class="linenos"> 73</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
+</span><span id="DataBased-74"><a href="#DataBased-74"><span class="linenos"> 74</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
+</span><span id="DataBased-75"><a href="#DataBased-75"><span class="linenos"> 75</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
+</span><span id="DataBased-76"><a href="#DataBased-76"><span class="linenos"> 76</span></a>        <span class="p">)</span>
+</span><span id="DataBased-77"><a href="#DataBased-77"><span class="linenos"> 77</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+</span><span id="DataBased-78"><a href="#DataBased-78"><span class="linenos"> 78</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
+</span><span id="DataBased-79"><a href="#DataBased-79"><span class="linenos"> 79</span></a>
+</span><span id="DataBased-80"><a href="#DataBased-80"><span class="linenos"> 80</span></a>    <span class="k">def</span> <span class="fm">__enter__</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased-81"><a href="#DataBased-81"><span class="linenos"> 81</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
+</span><span id="DataBased-82"><a href="#DataBased-82"><span class="linenos"> 82</span></a>        <span class="k">return</span> <span class="bp">self</span>
+</span><span id="DataBased-83"><a href="#DataBased-83"><span class="linenos"> 83</span></a>
+</span><span id="DataBased-84"><a href="#DataBased-84"><span class="linenos"> 84</span></a>    <span class="k">def</span> <span class="fm">__exit__</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">exception_type</span><span class="p">,</span> <span class="n">exception_value</span><span class="p">,</span> <span class="n">exception_traceback</span><span class="p">):</span>
+</span><span id="DataBased-85"><a href="#DataBased-85"><span class="linenos"> 85</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="DataBased-86"><a href="#DataBased-86"><span class="linenos"> 86</span></a>
+</span><span id="DataBased-87"><a href="#DataBased-87"><span class="linenos"> 87</span></a>    <span class="nd">@property</span>
+</span><span id="DataBased-88"><a href="#DataBased-88"><span class="linenos"> 88</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">float</span><span class="p">:</span>
+</span><span id="DataBased-89"><a href="#DataBased-89"><span class="linenos"> 89</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span>
+</span><span id="DataBased-90"><a href="#DataBased-90"><span class="linenos"> 90</span></a>
+</span><span id="DataBased-91"><a href="#DataBased-91"><span class="linenos"> 91</span></a>    <span class="nd">@connection_timeout</span><span class="o">.</span><span class="n">setter</span>
+</span><span id="DataBased-92"><a href="#DataBased-92"><span class="linenos"> 92</span></a>    <span class="k">def</span> <span class="nf">connection_timeout</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">num_seconds</span><span class="p">:</span> <span class="nb">float</span><span class="p">):</span>
+</span><span id="DataBased-93"><a href="#DataBased-93"><span class="linenos"> 93</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_connection_timeout</span> <span class="o">=</span> <span class="n">num_seconds</span>
+</span><span id="DataBased-94"><a href="#DataBased-94"><span class="linenos"> 94</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="DataBased-95"><a href="#DataBased-95"><span class="linenos"> 95</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="DataBased-96"><a href="#DataBased-96"><span class="linenos"> 96</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">open</span><span class="p">()</span>
+</span><span id="DataBased-97"><a href="#DataBased-97"><span class="linenos"> 97</span></a>
+</span><span id="DataBased-98"><a href="#DataBased-98"><span class="linenos"> 98</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased-99"><a href="#DataBased-99"><span class="linenos"> 99</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
+</span><span id="DataBased-100"><a href="#DataBased-100"><span class="linenos">100</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
+</span><span id="DataBased-101"><a href="#DataBased-101"><span class="linenos">101</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
+</span><span id="DataBased-102"><a href="#DataBased-102"><span class="linenos">102</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
+</span><span id="DataBased-103"><a href="#DataBased-103"><span class="linenos">103</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
+</span><span id="DataBased-104"><a href="#DataBased-104"><span class="linenos">104</span></a>        <span class="p">)</span>
+</span><span id="DataBased-105"><a href="#DataBased-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
+</span><span id="DataBased-106"><a href="#DataBased-106"><span class="linenos">106</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
+</span><span id="DataBased-107"><a href="#DataBased-107"><span class="linenos">107</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased-108"><a href="#DataBased-108"><span class="linenos">108</span></a>
+</span><span id="DataBased-109"><a href="#DataBased-109"><span class="linenos">109</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased-110"><a href="#DataBased-110"><span class="linenos">110</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
+</span><span id="DataBased-111"><a href="#DataBased-111"><span class="linenos">111</span></a>
+</span><span id="DataBased-112"><a href="#DataBased-112"><span class="linenos">112</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
+</span><span id="DataBased-113"><a href="#DataBased-113"><span class="linenos">113</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
+</span><span id="DataBased-114"><a href="#DataBased-114"><span class="linenos">114</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="DataBased-115"><a href="#DataBased-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
+</span><span id="DataBased-116"><a href="#DataBased-116"><span class="linenos">116</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="DataBased-117"><a href="#DataBased-117"><span class="linenos">117</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+</span><span id="DataBased-118"><a href="#DataBased-118"><span class="linenos">118</span></a>
+</span><span id="DataBased-119"><a href="#DataBased-119"><span class="linenos">119</span></a>    <span class="k">def</span> <span class="nf">_logger_init</span><span class="p">(</span>
+</span><span id="DataBased-120"><a href="#DataBased-120"><span class="linenos">120</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased-121"><a href="#DataBased-121"><span class="linenos">121</span></a>        <span class="n">message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
+</span><span id="DataBased-122"><a href="#DataBased-122"><span class="linenos">122</span></a>        <span class="n">encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
+</span><span id="DataBased-123"><a href="#DataBased-123"><span class="linenos">123</span></a>    <span class="p">):</span>
+</span><span id="DataBased-124"><a href="#DataBased-124"><span class="linenos">124</span></a>        <span class="sd">&quot;&quot;&quot;:param `message_format`: &#39;{&#39; style format string&quot;&quot;&quot;</span>
+</span><span id="DataBased-125"><a href="#DataBased-125"><span class="linenos">125</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">logger</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">getLogger</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbname</span><span class="p">)</span>
+</span><span id="DataBased-126"><a href="#DataBased-126"><span class="linenos">126</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">hasHandlers</span><span class="p">():</span>
+</span><span id="DataBased-127"><a href="#DataBased-127"><span class="linenos">127</span></a>            <span class="n">handler</span> <span class="o">=</span> <span class="n">logging</span><span class="o">.</span><span class="n">FileHandler</span><span class="p">(</span>
+</span><span id="DataBased-128"><a href="#DataBased-128"><span class="linenos">128</span></a>                <span class="nb">str</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s2">&quot;.&quot;</span><span class="p">,</span> <span class="s2">&quot;&quot;</span><span class="p">)</span> <span class="o">+</span> <span class="s2">&quot;.log&quot;</span><span class="p">,</span> <span class="n">encoding</span><span class="o">=</span><span class="n">encoding</span>
+</span><span id="DataBased-129"><a href="#DataBased-129"><span class="linenos">129</span></a>            <span class="p">)</span>
+</span><span id="DataBased-130"><a href="#DataBased-130"><span class="linenos">130</span></a>            <span class="n">handler</span><span class="o">.</span><span class="n">setFormatter</span><span class="p">(</span>
+</span><span id="DataBased-131"><a href="#DataBased-131"><span class="linenos">131</span></a>                <span class="n">logging</span><span class="o">.</span><span class="n">Formatter</span><span class="p">(</span>
+</span><span id="DataBased-132"><a href="#DataBased-132"><span class="linenos">132</span></a>                    <span class="n">message_format</span><span class="p">,</span> <span class="n">style</span><span class="o">=</span><span class="s2">&quot;{&quot;</span><span class="p">,</span> <span class="n">datefmt</span><span class="o">=</span><span class="s2">&quot;%m/</span><span class="si">%d</span><span class="s2">/%Y %I:%M:%S %p&quot;</span>
+</span><span id="DataBased-133"><a href="#DataBased-133"><span class="linenos">133</span></a>                <span class="p">)</span>
+</span><span id="DataBased-134"><a href="#DataBased-134"><span class="linenos">134</span></a>            <span class="p">)</span>
+</span><span id="DataBased-135"><a href="#DataBased-135"><span class="linenos">135</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">addHandler</span><span class="p">(</span><span class="n">handler</span><span class="p">)</span>
+</span><span id="DataBased-136"><a href="#DataBased-136"><span class="linenos">136</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">setLevel</span><span class="p">(</span><span class="n">logging</span><span class="o">.</span><span class="n">INFO</span><span class="p">)</span>
+</span><span id="DataBased-137"><a href="#DataBased-137"><span class="linenos">137</span></a>
+</span><span id="DataBased-138"><a href="#DataBased-138"><span class="linenos">138</span></a>    <span class="k">def</span> <span class="nf">_get_dict</span><span class="p">(</span>
+</span><span id="DataBased-139"><a href="#DataBased-139"><span class="linenos">139</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-140"><a href="#DataBased-140"><span class="linenos">140</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">dict</span><span class="p">:</span>
+</span><span id="DataBased-141"><a href="#DataBased-141"><span class="linenos">141</span></a>        <span class="sd">&quot;&quot;&quot;Converts the values of a row into a dictionary with column names as keys.</span>
+</span><span id="DataBased-142"><a href="#DataBased-142"><span class="linenos">142</span></a>
+</span><span id="DataBased-143"><a href="#DataBased-143"><span class="linenos">143</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-144"><a href="#DataBased-144"><span class="linenos">144</span></a>
+</span><span id="DataBased-145"><a href="#DataBased-145"><span class="linenos">145</span></a><span class="sd">        `table`: The table that values were pulled from.</span>
+</span><span id="DataBased-146"><a href="#DataBased-146"><span class="linenos">146</span></a>
+</span><span id="DataBased-147"><a href="#DataBased-147"><span class="linenos">147</span></a><span class="sd">        `values`: List of values expected to be the same quantity</span>
+</span><span id="DataBased-148"><a href="#DataBased-148"><span class="linenos">148</span></a><span class="sd">        and in the same order as the column names of table.</span>
+</span><span id="DataBased-149"><a href="#DataBased-149"><span class="linenos">149</span></a>
+</span><span id="DataBased-150"><a href="#DataBased-150"><span class="linenos">150</span></a><span class="sd">        `columns_to_return`: An optional list of column names.</span>
+</span><span id="DataBased-151"><a href="#DataBased-151"><span class="linenos">151</span></a><span class="sd">        If given, only these columns will be included in the returned dictionary.</span>
+</span><span id="DataBased-152"><a href="#DataBased-152"><span class="linenos">152</span></a><span class="sd">        Otherwise all columns and values are returned.&quot;&quot;&quot;</span>
+</span><span id="DataBased-153"><a href="#DataBased-153"><span class="linenos">153</span></a>        <span class="k">return</span> <span class="p">{</span>
+</span><span id="DataBased-154"><a href="#DataBased-154"><span class="linenos">154</span></a>            <span class="n">column</span><span class="p">:</span> <span class="n">value</span>
+</span><span id="DataBased-155"><a href="#DataBased-155"><span class="linenos">155</span></a>            <span class="k">for</span> <span class="n">column</span><span class="p">,</span> <span class="n">value</span> <span class="ow">in</span> <span class="nb">zip</span><span class="p">(</span><span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">),</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="DataBased-156"><a href="#DataBased-156"><span class="linenos">156</span></a>            <span class="k">if</span> <span class="ow">not</span> <span class="n">columns_to_return</span> <span class="ow">or</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns_to_return</span>
+</span><span id="DataBased-157"><a href="#DataBased-157"><span class="linenos">157</span></a>        <span class="p">}</span>
+</span><span id="DataBased-158"><a href="#DataBased-158"><span class="linenos">158</span></a>
+</span><span id="DataBased-159"><a href="#DataBased-159"><span class="linenos">159</span></a>    <span class="k">def</span> <span class="nf">_get_conditions</span><span class="p">(</span>
+</span><span id="DataBased-160"><a href="#DataBased-160"><span class="linenos">160</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased-161"><a href="#DataBased-161"><span class="linenos">161</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased-162"><a href="#DataBased-162"><span class="linenos">162</span></a>        <span class="sd">&quot;&quot;&quot;Builds and returns the conditional portion of a query.</span>
+</span><span id="DataBased-163"><a href="#DataBased-163"><span class="linenos">163</span></a>
+</span><span id="DataBased-164"><a href="#DataBased-164"><span class="linenos">164</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-165"><a href="#DataBased-165"><span class="linenos">165</span></a>
+</span><span id="DataBased-166"><a href="#DataBased-166"><span class="linenos">166</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="DataBased-167"><a href="#DataBased-167"><span class="linenos">167</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="DataBased-168"><a href="#DataBased-168"><span class="linenos">168</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="DataBased-169"><a href="#DataBased-169"><span class="linenos">169</span></a>
+</span><span id="DataBased-170"><a href="#DataBased-170"><span class="linenos">170</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
+</span><span id="DataBased-171"><a href="#DataBased-171"><span class="linenos">171</span></a><span class="sd">        will be matched as a substring.</span>
+</span><span id="DataBased-172"><a href="#DataBased-172"><span class="linenos">172</span></a>
+</span><span id="DataBased-173"><a href="#DataBased-173"><span class="linenos">173</span></a><span class="sd">        Usage e.g.:</span>
+</span><span id="DataBased-174"><a href="#DataBased-174"><span class="linenos">174</span></a>
+</span><span id="DataBased-175"><a href="#DataBased-175"><span class="linenos">175</span></a><span class="sd">        &gt;&gt;&gt; self.cursor.execute(f&#39;select * from {table} where {conditions};&#39;)&quot;&quot;&quot;</span>
+</span><span id="DataBased-176"><a href="#DataBased-176"><span class="linenos">176</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">)</span> <span class="o">==</span> <span class="nb">dict</span><span class="p">:</span>
+</span><span id="DataBased-177"><a href="#DataBased-177"><span class="linenos">177</span></a>            <span class="n">match_criteria</span> <span class="o">=</span> <span class="p">[(</span><span class="n">k</span><span class="p">,</span> <span class="n">v</span><span class="p">)</span> <span class="k">for</span> <span class="n">k</span><span class="p">,</span> <span class="n">v</span> <span class="ow">in</span> <span class="n">match_criteria</span><span class="o">.</span><span class="n">items</span><span class="p">()]</span>
+</span><span id="DataBased-178"><a href="#DataBased-178"><span class="linenos">178</span></a>        <span class="k">if</span> <span class="n">exact_match</span><span class="p">:</span>
+</span><span id="DataBased-179"><a href="#DataBased-179"><span class="linenos">179</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
+</span><span id="DataBased-180"><a href="#DataBased-180"><span class="linenos">180</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; = &quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot;&#39;</span>
+</span><span id="DataBased-181"><a href="#DataBased-181"><span class="linenos">181</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
+</span><span id="DataBased-182"><a href="#DataBased-182"><span class="linenos">182</span></a>            <span class="p">)</span>
+</span><span id="DataBased-183"><a href="#DataBased-183"><span class="linenos">183</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-184"><a href="#DataBased-184"><span class="linenos">184</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot; and &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span>
+</span><span id="DataBased-185"><a href="#DataBased-185"><span class="linenos">185</span></a>                <span class="sa">f</span><span class="s1">&#39;&quot;</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1">&quot; like &quot;%</span><span class="si">{</span><span class="n">column_row</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span><span class="si">}</span><span class="s1">%&quot;&#39;</span>
+</span><span id="DataBased-186"><a href="#DataBased-186"><span class="linenos">186</span></a>                <span class="k">for</span> <span class="n">column_row</span> <span class="ow">in</span> <span class="n">match_criteria</span>
+</span><span id="DataBased-187"><a href="#DataBased-187"><span class="linenos">187</span></a>            <span class="p">)</span>
+</span><span id="DataBased-188"><a href="#DataBased-188"><span class="linenos">188</span></a>        <span class="k">return</span> <span class="sa">f</span><span class="s2">&quot;(</span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">)&quot;</span>
+</span><span id="DataBased-189"><a href="#DataBased-189"><span class="linenos">189</span></a>
+</span><span id="DataBased-190"><a href="#DataBased-190"><span class="linenos">190</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased-191"><a href="#DataBased-191"><span class="linenos">191</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
+</span><span id="DataBased-192"><a href="#DataBased-192"><span class="linenos">192</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
+</span><span id="DataBased-193"><a href="#DataBased-193"><span class="linenos">193</span></a>
+</span><span id="DataBased-194"><a href="#DataBased-194"><span class="linenos">194</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-195"><a href="#DataBased-195"><span class="linenos">195</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
+</span><span id="DataBased-196"><a href="#DataBased-196"><span class="linenos">196</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
+</span><span id="DataBased-197"><a href="#DataBased-197"><span class="linenos">197</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
+</span><span id="DataBased-198"><a href="#DataBased-198"><span class="linenos">198</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+</span><span id="DataBased-199"><a href="#DataBased-199"><span class="linenos">199</span></a>
+</span><span id="DataBased-200"><a href="#DataBased-200"><span class="linenos">200</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-201"><a href="#DataBased-201"><span class="linenos">201</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
+</span><span id="DataBased-202"><a href="#DataBased-202"><span class="linenos">202</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
+</span><span id="DataBased-203"><a href="#DataBased-203"><span class="linenos">203</span></a>
+</span><span id="DataBased-204"><a href="#DataBased-204"><span class="linenos">204</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
+</span><span id="DataBased-205"><a href="#DataBased-205"><span class="linenos">205</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
+</span><span id="DataBased-206"><a href="#DataBased-206"><span class="linenos">206</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
+</span><span id="DataBased-207"><a href="#DataBased-207"><span class="linenos">207</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
+</span><span id="DataBased-208"><a href="#DataBased-208"><span class="linenos">208</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
+</span><span id="DataBased-209"><a href="#DataBased-209"><span class="linenos">209</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="DataBased-210"><a href="#DataBased-210"><span class="linenos">210</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
+</span><span id="DataBased-211"><a href="#DataBased-211"><span class="linenos">211</span></a>
+</span><span id="DataBased-212"><a href="#DataBased-212"><span class="linenos">212</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-213"><a href="#DataBased-213"><span class="linenos">213</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
+</span><span id="DataBased-214"><a href="#DataBased-214"><span class="linenos">214</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
+</span><span id="DataBased-215"><a href="#DataBased-215"><span class="linenos">215</span></a>
+</span><span id="DataBased-216"><a href="#DataBased-216"><span class="linenos">216</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-217"><a href="#DataBased-217"><span class="linenos">217</span></a>
+</span><span id="DataBased-218"><a href="#DataBased-218"><span class="linenos">218</span></a><span class="sd">        `table`: Name of the table to create.</span>
+</span><span id="DataBased-219"><a href="#DataBased-219"><span class="linenos">219</span></a>
+</span><span id="DataBased-220"><a href="#DataBased-220"><span class="linenos">220</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
+</span><span id="DataBased-221"><a href="#DataBased-221"><span class="linenos">221</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
+</span><span id="DataBased-222"><a href="#DataBased-222"><span class="linenos">222</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
+</span><span id="DataBased-223"><a href="#DataBased-223"><span class="linenos">223</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
+</span><span id="DataBased-224"><a href="#DataBased-224"><span class="linenos">224</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="DataBased-225"><a href="#DataBased-225"><span class="linenos">225</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
+</span><span id="DataBased-226"><a href="#DataBased-226"><span class="linenos">226</span></a>
+</span><span id="DataBased-227"><a href="#DataBased-227"><span class="linenos">227</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-228"><a href="#DataBased-228"><span class="linenos">228</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="DataBased-229"><a href="#DataBased-229"><span class="linenos">229</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
+</span><span id="DataBased-230"><a href="#DataBased-230"><span class="linenos">230</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-231"><a href="#DataBased-231"><span class="linenos">231</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
+</span><span id="DataBased-232"><a href="#DataBased-232"><span class="linenos">232</span></a>        <span class="p">)</span>
+</span><span id="DataBased-233"><a href="#DataBased-233"><span class="linenos">233</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
+</span><span id="DataBased-234"><a href="#DataBased-234"><span class="linenos">234</span></a>
+</span><span id="DataBased-235"><a href="#DataBased-235"><span class="linenos">235</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-236"><a href="#DataBased-236"><span class="linenos">236</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="DataBased-237"><a href="#DataBased-237"><span class="linenos">237</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
+</span><span id="DataBased-238"><a href="#DataBased-238"><span class="linenos">238</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
+</span><span id="DataBased-239"><a href="#DataBased-239"><span class="linenos">239</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
+</span><span id="DataBased-240"><a href="#DataBased-240"><span class="linenos">240</span></a>
+</span><span id="DataBased-241"><a href="#DataBased-241"><span class="linenos">241</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-242"><a href="#DataBased-242"><span class="linenos">242</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
+</span><span id="DataBased-243"><a href="#DataBased-243"><span class="linenos">243</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased-244"><a href="#DataBased-244"><span class="linenos">244</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased-245"><a href="#DataBased-245"><span class="linenos">245</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-246"><a href="#DataBased-246"><span class="linenos">246</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased-247"><a href="#DataBased-247"><span class="linenos">247</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased-248"><a href="#DataBased-248"><span class="linenos">248</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
+</span><span id="DataBased-249"><a href="#DataBased-249"><span class="linenos">249</span></a>
+</span><span id="DataBased-250"><a href="#DataBased-250"><span class="linenos">250</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-251"><a href="#DataBased-251"><span class="linenos">251</span></a>
+</span><span id="DataBased-252"><a href="#DataBased-252"><span class="linenos">252</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="DataBased-253"><a href="#DataBased-253"><span class="linenos">253</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="DataBased-254"><a href="#DataBased-254"><span class="linenos">254</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="DataBased-255"><a href="#DataBased-255"><span class="linenos">255</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
+</span><span id="DataBased-256"><a href="#DataBased-256"><span class="linenos">256</span></a>
+</span><span id="DataBased-257"><a href="#DataBased-257"><span class="linenos">257</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
+</span><span id="DataBased-258"><a href="#DataBased-258"><span class="linenos">258</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
+</span><span id="DataBased-259"><a href="#DataBased-259"><span class="linenos">259</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
+</span><span id="DataBased-260"><a href="#DataBased-260"><span class="linenos">260</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased-261"><a href="#DataBased-261"><span class="linenos">261</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="DataBased-262"><a href="#DataBased-262"><span class="linenos">262</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-263"><a href="#DataBased-263"><span class="linenos">263</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased-264"><a href="#DataBased-264"><span class="linenos">264</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-265"><a href="#DataBased-265"><span class="linenos">265</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased-266"><a href="#DataBased-266"><span class="linenos">266</span></a>                <span class="p">)</span>
+</span><span id="DataBased-267"><a href="#DataBased-267"><span class="linenos">267</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-268"><a href="#DataBased-268"><span class="linenos">268</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="DataBased-269"><a href="#DataBased-269"><span class="linenos">269</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
+</span><span id="DataBased-270"><a href="#DataBased-270"><span class="linenos">270</span></a>        <span class="k">except</span><span class="p">:</span>
+</span><span id="DataBased-271"><a href="#DataBased-271"><span class="linenos">271</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="DataBased-272"><a href="#DataBased-272"><span class="linenos">272</span></a>
+</span><span id="DataBased-273"><a href="#DataBased-273"><span class="linenos">273</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-274"><a href="#DataBased-274"><span class="linenos">274</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
+</span><span id="DataBased-275"><a href="#DataBased-275"><span class="linenos">275</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-276"><a href="#DataBased-276"><span class="linenos">276</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="DataBased-277"><a href="#DataBased-277"><span class="linenos">277</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
+</span><span id="DataBased-278"><a href="#DataBased-278"><span class="linenos">278</span></a>
+</span><span id="DataBased-279"><a href="#DataBased-279"><span class="linenos">279</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
+</span><span id="DataBased-280"><a href="#DataBased-280"><span class="linenos">280</span></a>
+</span><span id="DataBased-281"><a href="#DataBased-281"><span class="linenos">281</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-282"><a href="#DataBased-282"><span class="linenos">282</span></a>
+</span><span id="DataBased-283"><a href="#DataBased-283"><span class="linenos">283</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="DataBased-284"><a href="#DataBased-284"><span class="linenos">284</span></a>
+</span><span id="DataBased-285"><a href="#DataBased-285"><span class="linenos">285</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
+</span><span id="DataBased-286"><a href="#DataBased-286"><span class="linenos">286</span></a>
+</span><span id="DataBased-287"><a href="#DataBased-287"><span class="linenos">287</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="DataBased-288"><a href="#DataBased-288"><span class="linenos">288</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="DataBased-289"><a href="#DataBased-289"><span class="linenos">289</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="DataBased-290"><a href="#DataBased-290"><span class="linenos">290</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="DataBased-291"><a href="#DataBased-291"><span class="linenos">291</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-292"><a href="#DataBased-292"><span class="linenos">292</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased-293"><a href="#DataBased-293"><span class="linenos">293</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
+</span><span id="DataBased-294"><a href="#DataBased-294"><span class="linenos">294</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-295"><a href="#DataBased-295"><span class="linenos">295</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
+</span><span id="DataBased-296"><a href="#DataBased-296"><span class="linenos">296</span></a>                    <span class="n">values</span><span class="p">,</span>
+</span><span id="DataBased-297"><a href="#DataBased-297"><span class="linenos">297</span></a>                <span class="p">)</span>
+</span><span id="DataBased-298"><a href="#DataBased-298"><span class="linenos">298</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-299"><a href="#DataBased-299"><span class="linenos">299</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-300"><a href="#DataBased-300"><span class="linenos">300</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
+</span><span id="DataBased-301"><a href="#DataBased-301"><span class="linenos">301</span></a>                <span class="p">)</span>
+</span><span id="DataBased-302"><a href="#DataBased-302"><span class="linenos">302</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
+</span><span id="DataBased-303"><a href="#DataBased-303"><span class="linenos">303</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="DataBased-304"><a href="#DataBased-304"><span class="linenos">304</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased-305"><a href="#DataBased-305"><span class="linenos">305</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
+</span><span id="DataBased-306"><a href="#DataBased-306"><span class="linenos">306</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
+</span><span id="DataBased-307"><a href="#DataBased-307"><span class="linenos">307</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
+</span><span id="DataBased-308"><a href="#DataBased-308"><span class="linenos">308</span></a>                <span class="p">)</span>
+</span><span id="DataBased-309"><a href="#DataBased-309"><span class="linenos">309</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-310"><a href="#DataBased-310"><span class="linenos">310</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
+</span><span id="DataBased-311"><a href="#DataBased-311"><span class="linenos">311</span></a>            <span class="k">return</span> <span class="kc">False</span>
+</span><span id="DataBased-312"><a href="#DataBased-312"><span class="linenos">312</span></a>
+</span><span id="DataBased-313"><a href="#DataBased-313"><span class="linenos">313</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-314"><a href="#DataBased-314"><span class="linenos">314</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
+</span><span id="DataBased-315"><a href="#DataBased-315"><span class="linenos">315</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-316"><a href="#DataBased-316"><span class="linenos">316</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
+</span><span id="DataBased-317"><a href="#DataBased-317"><span class="linenos">317</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
+</span><span id="DataBased-318"><a href="#DataBased-318"><span class="linenos">318</span></a>
+</span><span id="DataBased-319"><a href="#DataBased-319"><span class="linenos">319</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
+</span><span id="DataBased-320"><a href="#DataBased-320"><span class="linenos">320</span></a>
+</span><span id="DataBased-321"><a href="#DataBased-321"><span class="linenos">321</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-322"><a href="#DataBased-322"><span class="linenos">322</span></a>
+</span><span id="DataBased-323"><a href="#DataBased-323"><span class="linenos">323</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="DataBased-324"><a href="#DataBased-324"><span class="linenos">324</span></a>
+</span><span id="DataBased-325"><a href="#DataBased-325"><span class="linenos">325</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
+</span><span id="DataBased-326"><a href="#DataBased-326"><span class="linenos">326</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
+</span><span id="DataBased-327"><a href="#DataBased-327"><span class="linenos">327</span></a>
+</span><span id="DataBased-328"><a href="#DataBased-328"><span class="linenos">328</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="DataBased-329"><a href="#DataBased-329"><span class="linenos">329</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="DataBased-330"><a href="#DataBased-330"><span class="linenos">330</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="DataBased-331"><a href="#DataBased-331"><span class="linenos">331</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="DataBased-332"><a href="#DataBased-332"><span class="linenos">332</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
+</span><span id="DataBased-333"><a href="#DataBased-333"><span class="linenos">333</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
+</span><span id="DataBased-334"><a href="#DataBased-334"><span class="linenos">334</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="DataBased-335"><a href="#DataBased-335"><span class="linenos">335</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-336"><a href="#DataBased-336"><span class="linenos">336</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="DataBased-337"><a href="#DataBased-337"><span class="linenos">337</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
+</span><span id="DataBased-338"><a href="#DataBased-338"><span class="linenos">338</span></a>
+</span><span id="DataBased-339"><a href="#DataBased-339"><span class="linenos">339</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-340"><a href="#DataBased-340"><span class="linenos">340</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
+</span><span id="DataBased-341"><a href="#DataBased-341"><span class="linenos">341</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased-342"><a href="#DataBased-342"><span class="linenos">342</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased-343"><a href="#DataBased-343"><span class="linenos">343</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-344"><a href="#DataBased-344"><span class="linenos">344</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased-345"><a href="#DataBased-345"><span class="linenos">345</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-346"><a href="#DataBased-346"><span class="linenos">346</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-347"><a href="#DataBased-347"><span class="linenos">347</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="DataBased-348"><a href="#DataBased-348"><span class="linenos">348</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="DataBased-349"><a href="#DataBased-349"><span class="linenos">349</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-350"><a href="#DataBased-350"><span class="linenos">350</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-351"><a href="#DataBased-351"><span class="linenos">351</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
+</span><span id="DataBased-352"><a href="#DataBased-352"><span class="linenos">352</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
+</span><span id="DataBased-353"><a href="#DataBased-353"><span class="linenos">353</span></a>
+</span><span id="DataBased-354"><a href="#DataBased-354"><span class="linenos">354</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
 </span><span id="DataBased-355"><a href="#DataBased-355"><span class="linenos">355</span></a>
-</span><span id="DataBased-356"><a href="#DataBased-356"><span class="linenos">356</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-357"><a href="#DataBased-357"><span class="linenos">357</span></a>
-</span><span id="DataBased-358"><a href="#DataBased-358"><span class="linenos">358</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="DataBased-359"><a href="#DataBased-359"><span class="linenos">359</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="DataBased-360"><a href="#DataBased-360"><span class="linenos">360</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="DataBased-361"><a href="#DataBased-361"><span class="linenos">361</span></a>
-</span><span id="DataBased-362"><a href="#DataBased-362"><span class="linenos">362</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
-</span><span id="DataBased-363"><a href="#DataBased-363"><span class="linenos">363</span></a>
-</span><span id="DataBased-364"><a href="#DataBased-364"><span class="linenos">364</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
-</span><span id="DataBased-365"><a href="#DataBased-365"><span class="linenos">365</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
-</span><span id="DataBased-366"><a href="#DataBased-366"><span class="linenos">366</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
-</span><span id="DataBased-367"><a href="#DataBased-367"><span class="linenos">367</span></a>
-</span><span id="DataBased-368"><a href="#DataBased-368"><span class="linenos">368</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
-</span><span id="DataBased-369"><a href="#DataBased-369"><span class="linenos">369</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
-</span><span id="DataBased-370"><a href="#DataBased-370"><span class="linenos">370</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
-</span><span id="DataBased-371"><a href="#DataBased-371"><span class="linenos">371</span></a>
-</span><span id="DataBased-372"><a href="#DataBased-372"><span class="linenos">372</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
-</span><span id="DataBased-373"><a href="#DataBased-373"><span class="linenos">373</span></a>
-</span><span id="DataBased-374"><a href="#DataBased-374"><span class="linenos">374</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
-</span><span id="DataBased-375"><a href="#DataBased-375"><span class="linenos">375</span></a>
-</span><span id="DataBased-376"><a href="#DataBased-376"><span class="linenos">376</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
-</span><span id="DataBased-377"><a href="#DataBased-377"><span class="linenos">377</span></a>
-</span><span id="DataBased-378"><a href="#DataBased-378"><span class="linenos">378</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
-</span><span id="DataBased-379"><a href="#DataBased-379"><span class="linenos">379</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased-380"><a href="#DataBased-380"><span class="linenos">380</span></a>
-</span><span id="DataBased-381"><a href="#DataBased-381"><span class="linenos">381</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased-382"><a href="#DataBased-382"><span class="linenos">382</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
-</span><span id="DataBased-383"><a href="#DataBased-383"><span class="linenos">383</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="DataBased-384"><a href="#DataBased-384"><span class="linenos">384</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="DataBased-385"><a href="#DataBased-385"><span class="linenos">385</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased-386"><a href="#DataBased-386"><span class="linenos">386</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased-387"><a href="#DataBased-387"><span class="linenos">387</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
-</span><span id="DataBased-388"><a href="#DataBased-388"><span class="linenos">388</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased-389"><a href="#DataBased-389"><span class="linenos">389</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
-</span><span id="DataBased-390"><a href="#DataBased-390"><span class="linenos">390</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased-391"><a href="#DataBased-391"><span class="linenos">391</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="DataBased-392"><a href="#DataBased-392"><span class="linenos">392</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="DataBased-393"><a href="#DataBased-393"><span class="linenos">393</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
-</span><span id="DataBased-394"><a href="#DataBased-394"><span class="linenos">394</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
-</span><span id="DataBased-395"><a href="#DataBased-395"><span class="linenos">395</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
-</span><span id="DataBased-396"><a href="#DataBased-396"><span class="linenos">396</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
-</span><span id="DataBased-397"><a href="#DataBased-397"><span class="linenos">397</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
-</span><span id="DataBased-398"><a href="#DataBased-398"><span class="linenos">398</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
-</span><span id="DataBased-399"><a href="#DataBased-399"><span class="linenos">399</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
-</span><span id="DataBased-400"><a href="#DataBased-400"><span class="linenos">400</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
-</span><span id="DataBased-401"><a href="#DataBased-401"><span class="linenos">401</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-402"><a href="#DataBased-402"><span class="linenos">402</span></a>            <span class="k">return</span> <span class="n">results</span>
-</span><span id="DataBased-403"><a href="#DataBased-403"><span class="linenos">403</span></a>
-</span><span id="DataBased-404"><a href="#DataBased-404"><span class="linenos">404</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-405"><a href="#DataBased-405"><span class="linenos">405</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
-</span><span id="DataBased-406"><a href="#DataBased-406"><span class="linenos">406</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-407"><a href="#DataBased-407"><span class="linenos">407</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
-</span><span id="DataBased-408"><a href="#DataBased-408"><span class="linenos">408</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
-</span><span id="DataBased-409"><a href="#DataBased-409"><span class="linenos">409</span></a>
-</span><span id="DataBased-410"><a href="#DataBased-410"><span class="linenos">410</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-411"><a href="#DataBased-411"><span class="linenos">411</span></a>
-</span><span id="DataBased-412"><a href="#DataBased-412"><span class="linenos">412</span></a><span class="sd">        `table`: The table to search.</span>
-</span><span id="DataBased-413"><a href="#DataBased-413"><span class="linenos">413</span></a>
-</span><span id="DataBased-414"><a href="#DataBased-414"><span class="linenos">414</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
-</span><span id="DataBased-415"><a href="#DataBased-415"><span class="linenos">415</span></a>
-</span><span id="DataBased-416"><a href="#DataBased-416"><span class="linenos">416</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
-</span><span id="DataBased-417"><a href="#DataBased-417"><span class="linenos">417</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
-</span><span id="DataBased-418"><a href="#DataBased-418"><span class="linenos">418</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased-419"><a href="#DataBased-419"><span class="linenos">419</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased-420"><a href="#DataBased-420"><span class="linenos">420</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
-</span><span id="DataBased-421"><a href="#DataBased-421"><span class="linenos">421</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="DataBased-422"><a href="#DataBased-422"><span class="linenos">422</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased-423"><a href="#DataBased-423"><span class="linenos">423</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
-</span><span id="DataBased-424"><a href="#DataBased-424"><span class="linenos">424</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased-425"><a href="#DataBased-425"><span class="linenos">425</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
-</span><span id="DataBased-426"><a href="#DataBased-426"><span class="linenos">426</span></a>                <span class="p">[</span>
-</span><span id="DataBased-427"><a href="#DataBased-427"><span class="linenos">427</span></a>                    <span class="n">row</span>
-</span><span id="DataBased-428"><a href="#DataBased-428"><span class="linenos">428</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
-</span><span id="DataBased-429"><a href="#DataBased-429"><span class="linenos">429</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
-</span><span id="DataBased-430"><a href="#DataBased-430"><span class="linenos">430</span></a>                    <span class="p">)</span>
-</span><span id="DataBased-431"><a href="#DataBased-431"><span class="linenos">431</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
-</span><span id="DataBased-432"><a href="#DataBased-432"><span class="linenos">432</span></a>                <span class="p">]</span>
-</span><span id="DataBased-433"><a href="#DataBased-433"><span class="linenos">433</span></a>            <span class="p">)</span>
-</span><span id="DataBased-434"><a href="#DataBased-434"><span class="linenos">434</span></a>        <span class="k">return</span> <span class="n">results</span>
-</span><span id="DataBased-435"><a href="#DataBased-435"><span class="linenos">435</span></a>
-</span><span id="DataBased-436"><a href="#DataBased-436"><span class="linenos">436</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-437"><a href="#DataBased-437"><span class="linenos">437</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
-</span><span id="DataBased-438"><a href="#DataBased-438"><span class="linenos">438</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased-439"><a href="#DataBased-439"><span class="linenos">439</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased-440"><a href="#DataBased-440"><span class="linenos">440</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
-</span><span id="DataBased-441"><a href="#DataBased-441"><span class="linenos">441</span></a>
-</span><span id="DataBased-442"><a href="#DataBased-442"><span class="linenos">442</span></a><span class="sd">        Returns the number of deleted records.</span>
-</span><span id="DataBased-443"><a href="#DataBased-443"><span class="linenos">443</span></a>
-</span><span id="DataBased-444"><a href="#DataBased-444"><span class="linenos">444</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-445"><a href="#DataBased-445"><span class="linenos">445</span></a>
-</span><span id="DataBased-446"><a href="#DataBased-446"><span class="linenos">446</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
-</span><span id="DataBased-447"><a href="#DataBased-447"><span class="linenos">447</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="DataBased-448"><a href="#DataBased-448"><span class="linenos">448</span></a>
-</span><span id="DataBased-449"><a href="#DataBased-449"><span class="linenos">449</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
-</span><span id="DataBased-450"><a href="#DataBased-450"><span class="linenos">450</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased-451"><a href="#DataBased-451"><span class="linenos">451</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="DataBased-452"><a href="#DataBased-452"><span class="linenos">452</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-453"><a href="#DataBased-453"><span class="linenos">453</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
-</span><span id="DataBased-454"><a href="#DataBased-454"><span class="linenos">454</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="DataBased-455"><a href="#DataBased-455"><span class="linenos">455</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="DataBased-456"><a href="#DataBased-456"><span class="linenos">456</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
-</span><span id="DataBased-457"><a href="#DataBased-457"><span class="linenos">457</span></a>            <span class="p">)</span>
-</span><span id="DataBased-458"><a href="#DataBased-458"><span class="linenos">458</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
-</span><span id="DataBased-459"><a href="#DataBased-459"><span class="linenos">459</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased-460"><a href="#DataBased-460"><span class="linenos">460</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
-</span><span id="DataBased-461"><a href="#DataBased-461"><span class="linenos">461</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased-462"><a href="#DataBased-462"><span class="linenos">462</span></a>            <span class="p">)</span>
-</span><span id="DataBased-463"><a href="#DataBased-463"><span class="linenos">463</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="DataBased-464"><a href="#DataBased-464"><span class="linenos">464</span></a>
-</span><span id="DataBased-465"><a href="#DataBased-465"><span class="linenos">465</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-466"><a href="#DataBased-466"><span class="linenos">466</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
-</span><span id="DataBased-467"><a href="#DataBased-467"><span class="linenos">467</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased-468"><a href="#DataBased-468"><span class="linenos">468</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased-469"><a href="#DataBased-469"><span class="linenos">469</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased-470"><a href="#DataBased-470"><span class="linenos">470</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
-</span><span id="DataBased-471"><a href="#DataBased-471"><span class="linenos">471</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased-472"><a href="#DataBased-472"><span class="linenos">472</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased-473"><a href="#DataBased-473"><span class="linenos">473</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased-474"><a href="#DataBased-474"><span class="linenos">474</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
-</span><span id="DataBased-475"><a href="#DataBased-475"><span class="linenos">475</span></a>
-</span><span id="DataBased-476"><a href="#DataBased-476"><span class="linenos">476</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-477"><a href="#DataBased-477"><span class="linenos">477</span></a>
-</span><span id="DataBased-478"><a href="#DataBased-478"><span class="linenos">478</span></a><span class="sd">        `table`: The table to update rows in.</span>
-</span><span id="DataBased-479"><a href="#DataBased-479"><span class="linenos">479</span></a>
-</span><span id="DataBased-480"><a href="#DataBased-480"><span class="linenos">480</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
-</span><span id="DataBased-481"><a href="#DataBased-481"><span class="linenos">481</span></a>
-</span><span id="DataBased-482"><a href="#DataBased-482"><span class="linenos">482</span></a><span class="sd">        `new_value`: The new value to insert.</span>
-</span><span id="DataBased-483"><a href="#DataBased-483"><span class="linenos">483</span></a>
-</span><span id="DataBased-484"><a href="#DataBased-484"><span class="linenos">484</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
-</span><span id="DataBased-485"><a href="#DataBased-485"><span class="linenos">485</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="DataBased-486"><a href="#DataBased-486"><span class="linenos">486</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
-</span><span id="DataBased-487"><a href="#DataBased-487"><span class="linenos">487</span></a>
-</span><span id="DataBased-488"><a href="#DataBased-488"><span class="linenos">488</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
-</span><span id="DataBased-489"><a href="#DataBased-489"><span class="linenos">489</span></a>
-</span><span id="DataBased-490"><a href="#DataBased-490"><span class="linenos">490</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
-</span><span id="DataBased-491"><a href="#DataBased-491"><span class="linenos">491</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
-</span><span id="DataBased-492"><a href="#DataBased-492"><span class="linenos">492</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
-</span><span id="DataBased-493"><a href="#DataBased-493"><span class="linenos">493</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased-494"><a href="#DataBased-494"><span class="linenos">494</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="DataBased-495"><a href="#DataBased-495"><span class="linenos">495</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased-496"><a href="#DataBased-496"><span class="linenos">496</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-497"><a href="#DataBased-497"><span class="linenos">497</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-498"><a href="#DataBased-498"><span class="linenos">498</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="DataBased-499"><a href="#DataBased-499"><span class="linenos">499</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-500"><a href="#DataBased-500"><span class="linenos">500</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-501"><a href="#DataBased-501"><span class="linenos">501</span></a>                <span class="n">query</span><span class="p">,</span>
-</span><span id="DataBased-502"><a href="#DataBased-502"><span class="linenos">502</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
-</span><span id="DataBased-503"><a href="#DataBased-503"><span class="linenos">503</span></a>            <span class="p">)</span>
-</span><span id="DataBased-504"><a href="#DataBased-504"><span class="linenos">504</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="DataBased-505"><a href="#DataBased-505"><span class="linenos">505</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="DataBased-506"><a href="#DataBased-506"><span class="linenos">506</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased-507"><a href="#DataBased-507"><span class="linenos">507</span></a>            <span class="p">)</span>
-</span><span id="DataBased-508"><a href="#DataBased-508"><span class="linenos">508</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
-</span><span id="DataBased-509"><a href="#DataBased-509"><span class="linenos">509</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased-510"><a href="#DataBased-510"><span class="linenos">510</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
-</span><span id="DataBased-511"><a href="#DataBased-511"><span class="linenos">511</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased-512"><a href="#DataBased-512"><span class="linenos">512</span></a>            <span class="p">)</span>
-</span><span id="DataBased-513"><a href="#DataBased-513"><span class="linenos">513</span></a>            <span class="k">return</span> <span class="mi">0</span>
-</span><span id="DataBased-514"><a href="#DataBased-514"><span class="linenos">514</span></a>
-</span><span id="DataBased-515"><a href="#DataBased-515"><span class="linenos">515</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-516"><a href="#DataBased-516"><span class="linenos">516</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="DataBased-517"><a href="#DataBased-517"><span class="linenos">517</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
-</span><span id="DataBased-518"><a href="#DataBased-518"><span class="linenos">518</span></a>
-</span><span id="DataBased-519"><a href="#DataBased-519"><span class="linenos">519</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
-</span><span id="DataBased-520"><a href="#DataBased-520"><span class="linenos">520</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-521"><a href="#DataBased-521"><span class="linenos">521</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="DataBased-522"><a href="#DataBased-522"><span class="linenos">522</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="DataBased-523"><a href="#DataBased-523"><span class="linenos">523</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="DataBased-524"><a href="#DataBased-524"><span class="linenos">524</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased-525"><a href="#DataBased-525"><span class="linenos">525</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
-</span><span id="DataBased-526"><a href="#DataBased-526"><span class="linenos">526</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="DataBased-527"><a href="#DataBased-527"><span class="linenos">527</span></a>            <span class="k">return</span> <span class="kc">False</span>
-</span><span id="DataBased-528"><a href="#DataBased-528"><span class="linenos">528</span></a>
-</span><span id="DataBased-529"><a href="#DataBased-529"><span class="linenos">529</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased-530"><a href="#DataBased-530"><span class="linenos">530</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
-</span><span id="DataBased-531"><a href="#DataBased-531"><span class="linenos">531</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased-532"><a href="#DataBased-532"><span class="linenos">532</span></a>    <span class="p">):</span>
-</span><span id="DataBased-533"><a href="#DataBased-533"><span class="linenos">533</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
-</span><span id="DataBased-534"><a href="#DataBased-534"><span class="linenos">534</span></a>
-</span><span id="DataBased-535"><a href="#DataBased-535"><span class="linenos">535</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-536"><a href="#DataBased-536"><span class="linenos">536</span></a>
-</span><span id="DataBased-537"><a href="#DataBased-537"><span class="linenos">537</span></a><span class="sd">        `column`: Name of the column to add.</span>
-</span><span id="DataBased-538"><a href="#DataBased-538"><span class="linenos">538</span></a>
-</span><span id="DataBased-539"><a href="#DataBased-539"><span class="linenos">539</span></a><span class="sd">        `_type`: The data type of the new column.</span>
-</span><span id="DataBased-540"><a href="#DataBased-540"><span class="linenos">540</span></a>
-</span><span id="DataBased-541"><a href="#DataBased-541"><span class="linenos">541</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
-</span><span id="DataBased-542"><a href="#DataBased-542"><span class="linenos">542</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased-543"><a href="#DataBased-543"><span class="linenos">543</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
-</span><span id="DataBased-544"><a href="#DataBased-544"><span class="linenos">544</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-545"><a href="#DataBased-545"><span class="linenos">545</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased-546"><a href="#DataBased-546"><span class="linenos">546</span></a>                <span class="p">)</span>
-</span><span id="DataBased-547"><a href="#DataBased-547"><span class="linenos">547</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
-</span><span id="DataBased-548"><a href="#DataBased-548"><span class="linenos">548</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased-549"><a href="#DataBased-549"><span class="linenos">549</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased-550"><a href="#DataBased-550"><span class="linenos">550</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased-551"><a href="#DataBased-551"><span class="linenos">551</span></a>                <span class="p">)</span>
-</span><span id="DataBased-552"><a href="#DataBased-552"><span class="linenos">552</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
-</span><span id="DataBased-553"><a href="#DataBased-553"><span class="linenos">553</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased-554"><a href="#DataBased-554"><span class="linenos">554</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
-</span><span id="DataBased-555"><a href="#DataBased-555"><span class="linenos">555</span></a>
-</span><span id="DataBased-556"><a href="#DataBased-556"><span class="linenos">556</span></a>    <span class="nd">@staticmethod</span>
-</span><span id="DataBased-557"><a href="#DataBased-557"><span class="linenos">557</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
-</span><span id="DataBased-558"><a href="#DataBased-558"><span class="linenos">558</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased-559"><a href="#DataBased-559"><span class="linenos">559</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased-560"><a href="#DataBased-560"><span class="linenos">560</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
-</span><span id="DataBased-561"><a href="#DataBased-561"><span class="linenos">561</span></a>
-</span><span id="DataBased-562"><a href="#DataBased-562"><span class="linenos">562</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased-563"><a href="#DataBased-563"><span class="linenos">563</span></a>
-</span><span id="DataBased-564"><a href="#DataBased-564"><span class="linenos">564</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
-</span><span id="DataBased-565"><a href="#DataBased-565"><span class="linenos">565</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
-</span><span id="DataBased-566"><a href="#DataBased-566"><span class="linenos">566</span></a>
-</span><span id="DataBased-567"><a href="#DataBased-567"><span class="linenos">567</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
-</span><span id="DataBased-568"><a href="#DataBased-568"><span class="linenos">568</span></a>
-</span><span id="DataBased-569"><a href="#DataBased-569"><span class="linenos">569</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
-</span><span id="DataBased-570"><a href="#DataBased-570"><span class="linenos">570</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
-</span><span id="DataBased-571"><a href="#DataBased-571"><span class="linenos">571</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
+</span><span id="DataBased-356"><a href="#DataBased-356"><span class="linenos">356</span></a>
+</span><span id="DataBased-357"><a href="#DataBased-357"><span class="linenos">357</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-358"><a href="#DataBased-358"><span class="linenos">358</span></a>
+</span><span id="DataBased-359"><a href="#DataBased-359"><span class="linenos">359</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="DataBased-360"><a href="#DataBased-360"><span class="linenos">360</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="DataBased-361"><a href="#DataBased-361"><span class="linenos">361</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="DataBased-362"><a href="#DataBased-362"><span class="linenos">362</span></a>
+</span><span id="DataBased-363"><a href="#DataBased-363"><span class="linenos">363</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
+</span><span id="DataBased-364"><a href="#DataBased-364"><span class="linenos">364</span></a>
+</span><span id="DataBased-365"><a href="#DataBased-365"><span class="linenos">365</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
+</span><span id="DataBased-366"><a href="#DataBased-366"><span class="linenos">366</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
+</span><span id="DataBased-367"><a href="#DataBased-367"><span class="linenos">367</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
+</span><span id="DataBased-368"><a href="#DataBased-368"><span class="linenos">368</span></a>
+</span><span id="DataBased-369"><a href="#DataBased-369"><span class="linenos">369</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
+</span><span id="DataBased-370"><a href="#DataBased-370"><span class="linenos">370</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
+</span><span id="DataBased-371"><a href="#DataBased-371"><span class="linenos">371</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
+</span><span id="DataBased-372"><a href="#DataBased-372"><span class="linenos">372</span></a>
+</span><span id="DataBased-373"><a href="#DataBased-373"><span class="linenos">373</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
+</span><span id="DataBased-374"><a href="#DataBased-374"><span class="linenos">374</span></a>
+</span><span id="DataBased-375"><a href="#DataBased-375"><span class="linenos">375</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
+</span><span id="DataBased-376"><a href="#DataBased-376"><span class="linenos">376</span></a>
+</span><span id="DataBased-377"><a href="#DataBased-377"><span class="linenos">377</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
+</span><span id="DataBased-378"><a href="#DataBased-378"><span class="linenos">378</span></a>
+</span><span id="DataBased-379"><a href="#DataBased-379"><span class="linenos">379</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
+</span><span id="DataBased-380"><a href="#DataBased-380"><span class="linenos">380</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased-381"><a href="#DataBased-381"><span class="linenos">381</span></a>
+</span><span id="DataBased-382"><a href="#DataBased-382"><span class="linenos">382</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased-383"><a href="#DataBased-383"><span class="linenos">383</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
+</span><span id="DataBased-384"><a href="#DataBased-384"><span class="linenos">384</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="DataBased-385"><a href="#DataBased-385"><span class="linenos">385</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="DataBased-386"><a href="#DataBased-386"><span class="linenos">386</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased-387"><a href="#DataBased-387"><span class="linenos">387</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased-388"><a href="#DataBased-388"><span class="linenos">388</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
+</span><span id="DataBased-389"><a href="#DataBased-389"><span class="linenos">389</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased-390"><a href="#DataBased-390"><span class="linenos">390</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
+</span><span id="DataBased-391"><a href="#DataBased-391"><span class="linenos">391</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased-392"><a href="#DataBased-392"><span class="linenos">392</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="DataBased-393"><a href="#DataBased-393"><span class="linenos">393</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="DataBased-394"><a href="#DataBased-394"><span class="linenos">394</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+</span><span id="DataBased-395"><a href="#DataBased-395"><span class="linenos">395</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
+</span><span id="DataBased-396"><a href="#DataBased-396"><span class="linenos">396</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
+</span><span id="DataBased-397"><a href="#DataBased-397"><span class="linenos">397</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
+</span><span id="DataBased-398"><a href="#DataBased-398"><span class="linenos">398</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
+</span><span id="DataBased-399"><a href="#DataBased-399"><span class="linenos">399</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
+</span><span id="DataBased-400"><a href="#DataBased-400"><span class="linenos">400</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
+</span><span id="DataBased-401"><a href="#DataBased-401"><span class="linenos">401</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
+</span><span id="DataBased-402"><a href="#DataBased-402"><span class="linenos">402</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-403"><a href="#DataBased-403"><span class="linenos">403</span></a>            <span class="k">return</span> <span class="n">results</span>
+</span><span id="DataBased-404"><a href="#DataBased-404"><span class="linenos">404</span></a>
+</span><span id="DataBased-405"><a href="#DataBased-405"><span class="linenos">405</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-406"><a href="#DataBased-406"><span class="linenos">406</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
+</span><span id="DataBased-407"><a href="#DataBased-407"><span class="linenos">407</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-408"><a href="#DataBased-408"><span class="linenos">408</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
+</span><span id="DataBased-409"><a href="#DataBased-409"><span class="linenos">409</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
+</span><span id="DataBased-410"><a href="#DataBased-410"><span class="linenos">410</span></a>
+</span><span id="DataBased-411"><a href="#DataBased-411"><span class="linenos">411</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-412"><a href="#DataBased-412"><span class="linenos">412</span></a>
+</span><span id="DataBased-413"><a href="#DataBased-413"><span class="linenos">413</span></a><span class="sd">        `table`: The table to search.</span>
+</span><span id="DataBased-414"><a href="#DataBased-414"><span class="linenos">414</span></a>
+</span><span id="DataBased-415"><a href="#DataBased-415"><span class="linenos">415</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
+</span><span id="DataBased-416"><a href="#DataBased-416"><span class="linenos">416</span></a>
+</span><span id="DataBased-417"><a href="#DataBased-417"><span class="linenos">417</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
+</span><span id="DataBased-418"><a href="#DataBased-418"><span class="linenos">418</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
+</span><span id="DataBased-419"><a href="#DataBased-419"><span class="linenos">419</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased-420"><a href="#DataBased-420"><span class="linenos">420</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased-421"><a href="#DataBased-421"><span class="linenos">421</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
+</span><span id="DataBased-422"><a href="#DataBased-422"><span class="linenos">422</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="DataBased-423"><a href="#DataBased-423"><span class="linenos">423</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased-424"><a href="#DataBased-424"><span class="linenos">424</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
+</span><span id="DataBased-425"><a href="#DataBased-425"><span class="linenos">425</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased-426"><a href="#DataBased-426"><span class="linenos">426</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
+</span><span id="DataBased-427"><a href="#DataBased-427"><span class="linenos">427</span></a>                <span class="p">[</span>
+</span><span id="DataBased-428"><a href="#DataBased-428"><span class="linenos">428</span></a>                    <span class="n">row</span>
+</span><span id="DataBased-429"><a href="#DataBased-429"><span class="linenos">429</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
+</span><span id="DataBased-430"><a href="#DataBased-430"><span class="linenos">430</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
+</span><span id="DataBased-431"><a href="#DataBased-431"><span class="linenos">431</span></a>                    <span class="p">)</span>
+</span><span id="DataBased-432"><a href="#DataBased-432"><span class="linenos">432</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
+</span><span id="DataBased-433"><a href="#DataBased-433"><span class="linenos">433</span></a>                <span class="p">]</span>
+</span><span id="DataBased-434"><a href="#DataBased-434"><span class="linenos">434</span></a>            <span class="p">)</span>
+</span><span id="DataBased-435"><a href="#DataBased-435"><span class="linenos">435</span></a>        <span class="k">return</span> <span class="n">results</span>
+</span><span id="DataBased-436"><a href="#DataBased-436"><span class="linenos">436</span></a>
+</span><span id="DataBased-437"><a href="#DataBased-437"><span class="linenos">437</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-438"><a href="#DataBased-438"><span class="linenos">438</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
+</span><span id="DataBased-439"><a href="#DataBased-439"><span class="linenos">439</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased-440"><a href="#DataBased-440"><span class="linenos">440</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased-441"><a href="#DataBased-441"><span class="linenos">441</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
+</span><span id="DataBased-442"><a href="#DataBased-442"><span class="linenos">442</span></a>
+</span><span id="DataBased-443"><a href="#DataBased-443"><span class="linenos">443</span></a><span class="sd">        Returns the number of deleted records.</span>
+</span><span id="DataBased-444"><a href="#DataBased-444"><span class="linenos">444</span></a>
+</span><span id="DataBased-445"><a href="#DataBased-445"><span class="linenos">445</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-446"><a href="#DataBased-446"><span class="linenos">446</span></a>
+</span><span id="DataBased-447"><a href="#DataBased-447"><span class="linenos">447</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
+</span><span id="DataBased-448"><a href="#DataBased-448"><span class="linenos">448</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="DataBased-449"><a href="#DataBased-449"><span class="linenos">449</span></a>
+</span><span id="DataBased-450"><a href="#DataBased-450"><span class="linenos">450</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
+</span><span id="DataBased-451"><a href="#DataBased-451"><span class="linenos">451</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased-452"><a href="#DataBased-452"><span class="linenos">452</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="DataBased-453"><a href="#DataBased-453"><span class="linenos">453</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-454"><a href="#DataBased-454"><span class="linenos">454</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
+</span><span id="DataBased-455"><a href="#DataBased-455"><span class="linenos">455</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="DataBased-456"><a href="#DataBased-456"><span class="linenos">456</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="DataBased-457"><a href="#DataBased-457"><span class="linenos">457</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
+</span><span id="DataBased-458"><a href="#DataBased-458"><span class="linenos">458</span></a>            <span class="p">)</span>
+</span><span id="DataBased-459"><a href="#DataBased-459"><span class="linenos">459</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
+</span><span id="DataBased-460"><a href="#DataBased-460"><span class="linenos">460</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased-461"><a href="#DataBased-461"><span class="linenos">461</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
+</span><span id="DataBased-462"><a href="#DataBased-462"><span class="linenos">462</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased-463"><a href="#DataBased-463"><span class="linenos">463</span></a>            <span class="p">)</span>
+</span><span id="DataBased-464"><a href="#DataBased-464"><span class="linenos">464</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="DataBased-465"><a href="#DataBased-465"><span class="linenos">465</span></a>
+</span><span id="DataBased-466"><a href="#DataBased-466"><span class="linenos">466</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-467"><a href="#DataBased-467"><span class="linenos">467</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
+</span><span id="DataBased-468"><a href="#DataBased-468"><span class="linenos">468</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased-469"><a href="#DataBased-469"><span class="linenos">469</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased-470"><a href="#DataBased-470"><span class="linenos">470</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased-471"><a href="#DataBased-471"><span class="linenos">471</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
+</span><span id="DataBased-472"><a href="#DataBased-472"><span class="linenos">472</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased-473"><a href="#DataBased-473"><span class="linenos">473</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased-474"><a href="#DataBased-474"><span class="linenos">474</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased-475"><a href="#DataBased-475"><span class="linenos">475</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
+</span><span id="DataBased-476"><a href="#DataBased-476"><span class="linenos">476</span></a>
+</span><span id="DataBased-477"><a href="#DataBased-477"><span class="linenos">477</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-478"><a href="#DataBased-478"><span class="linenos">478</span></a>
+</span><span id="DataBased-479"><a href="#DataBased-479"><span class="linenos">479</span></a><span class="sd">        `table`: The table to update rows in.</span>
+</span><span id="DataBased-480"><a href="#DataBased-480"><span class="linenos">480</span></a>
+</span><span id="DataBased-481"><a href="#DataBased-481"><span class="linenos">481</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
+</span><span id="DataBased-482"><a href="#DataBased-482"><span class="linenos">482</span></a>
+</span><span id="DataBased-483"><a href="#DataBased-483"><span class="linenos">483</span></a><span class="sd">        `new_value`: The new value to insert.</span>
+</span><span id="DataBased-484"><a href="#DataBased-484"><span class="linenos">484</span></a>
+</span><span id="DataBased-485"><a href="#DataBased-485"><span class="linenos">485</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
+</span><span id="DataBased-486"><a href="#DataBased-486"><span class="linenos">486</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="DataBased-487"><a href="#DataBased-487"><span class="linenos">487</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
+</span><span id="DataBased-488"><a href="#DataBased-488"><span class="linenos">488</span></a>
+</span><span id="DataBased-489"><a href="#DataBased-489"><span class="linenos">489</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
+</span><span id="DataBased-490"><a href="#DataBased-490"><span class="linenos">490</span></a>
+</span><span id="DataBased-491"><a href="#DataBased-491"><span class="linenos">491</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
+</span><span id="DataBased-492"><a href="#DataBased-492"><span class="linenos">492</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
+</span><span id="DataBased-493"><a href="#DataBased-493"><span class="linenos">493</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
+</span><span id="DataBased-494"><a href="#DataBased-494"><span class="linenos">494</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased-495"><a href="#DataBased-495"><span class="linenos">495</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="DataBased-496"><a href="#DataBased-496"><span class="linenos">496</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased-497"><a href="#DataBased-497"><span class="linenos">497</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-498"><a href="#DataBased-498"><span class="linenos">498</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-499"><a href="#DataBased-499"><span class="linenos">499</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="DataBased-500"><a href="#DataBased-500"><span class="linenos">500</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-501"><a href="#DataBased-501"><span class="linenos">501</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-502"><a href="#DataBased-502"><span class="linenos">502</span></a>                <span class="n">query</span><span class="p">,</span>
+</span><span id="DataBased-503"><a href="#DataBased-503"><span class="linenos">503</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
+</span><span id="DataBased-504"><a href="#DataBased-504"><span class="linenos">504</span></a>            <span class="p">)</span>
+</span><span id="DataBased-505"><a href="#DataBased-505"><span class="linenos">505</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="DataBased-506"><a href="#DataBased-506"><span class="linenos">506</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="DataBased-507"><a href="#DataBased-507"><span class="linenos">507</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased-508"><a href="#DataBased-508"><span class="linenos">508</span></a>            <span class="p">)</span>
+</span><span id="DataBased-509"><a href="#DataBased-509"><span class="linenos">509</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
+</span><span id="DataBased-510"><a href="#DataBased-510"><span class="linenos">510</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased-511"><a href="#DataBased-511"><span class="linenos">511</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
+</span><span id="DataBased-512"><a href="#DataBased-512"><span class="linenos">512</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased-513"><a href="#DataBased-513"><span class="linenos">513</span></a>            <span class="p">)</span>
+</span><span id="DataBased-514"><a href="#DataBased-514"><span class="linenos">514</span></a>            <span class="k">return</span> <span class="mi">0</span>
+</span><span id="DataBased-515"><a href="#DataBased-515"><span class="linenos">515</span></a>
+</span><span id="DataBased-516"><a href="#DataBased-516"><span class="linenos">516</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-517"><a href="#DataBased-517"><span class="linenos">517</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="DataBased-518"><a href="#DataBased-518"><span class="linenos">518</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
+</span><span id="DataBased-519"><a href="#DataBased-519"><span class="linenos">519</span></a>
+</span><span id="DataBased-520"><a href="#DataBased-520"><span class="linenos">520</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
+</span><span id="DataBased-521"><a href="#DataBased-521"><span class="linenos">521</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-522"><a href="#DataBased-522"><span class="linenos">522</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="DataBased-523"><a href="#DataBased-523"><span class="linenos">523</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="DataBased-524"><a href="#DataBased-524"><span class="linenos">524</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="DataBased-525"><a href="#DataBased-525"><span class="linenos">525</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased-526"><a href="#DataBased-526"><span class="linenos">526</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
+</span><span id="DataBased-527"><a href="#DataBased-527"><span class="linenos">527</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="DataBased-528"><a href="#DataBased-528"><span class="linenos">528</span></a>            <span class="k">return</span> <span class="kc">False</span>
+</span><span id="DataBased-529"><a href="#DataBased-529"><span class="linenos">529</span></a>
+</span><span id="DataBased-530"><a href="#DataBased-530"><span class="linenos">530</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased-531"><a href="#DataBased-531"><span class="linenos">531</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
+</span><span id="DataBased-532"><a href="#DataBased-532"><span class="linenos">532</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased-533"><a href="#DataBased-533"><span class="linenos">533</span></a>    <span class="p">):</span>
+</span><span id="DataBased-534"><a href="#DataBased-534"><span class="linenos">534</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
+</span><span id="DataBased-535"><a href="#DataBased-535"><span class="linenos">535</span></a>
+</span><span id="DataBased-536"><a href="#DataBased-536"><span class="linenos">536</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-537"><a href="#DataBased-537"><span class="linenos">537</span></a>
+</span><span id="DataBased-538"><a href="#DataBased-538"><span class="linenos">538</span></a><span class="sd">        `column`: Name of the column to add.</span>
+</span><span id="DataBased-539"><a href="#DataBased-539"><span class="linenos">539</span></a>
+</span><span id="DataBased-540"><a href="#DataBased-540"><span class="linenos">540</span></a><span class="sd">        `_type`: The data type of the new column.</span>
+</span><span id="DataBased-541"><a href="#DataBased-541"><span class="linenos">541</span></a>
+</span><span id="DataBased-542"><a href="#DataBased-542"><span class="linenos">542</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
+</span><span id="DataBased-543"><a href="#DataBased-543"><span class="linenos">543</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased-544"><a href="#DataBased-544"><span class="linenos">544</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
+</span><span id="DataBased-545"><a href="#DataBased-545"><span class="linenos">545</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-546"><a href="#DataBased-546"><span class="linenos">546</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased-547"><a href="#DataBased-547"><span class="linenos">547</span></a>                <span class="p">)</span>
+</span><span id="DataBased-548"><a href="#DataBased-548"><span class="linenos">548</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
+</span><span id="DataBased-549"><a href="#DataBased-549"><span class="linenos">549</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased-550"><a href="#DataBased-550"><span class="linenos">550</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased-551"><a href="#DataBased-551"><span class="linenos">551</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased-552"><a href="#DataBased-552"><span class="linenos">552</span></a>                <span class="p">)</span>
+</span><span id="DataBased-553"><a href="#DataBased-553"><span class="linenos">553</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+</span><span id="DataBased-554"><a href="#DataBased-554"><span class="linenos">554</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased-555"><a href="#DataBased-555"><span class="linenos">555</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+</span><span id="DataBased-556"><a href="#DataBased-556"><span class="linenos">556</span></a>
+</span><span id="DataBased-557"><a href="#DataBased-557"><span class="linenos">557</span></a>    <span class="nd">@staticmethod</span>
+</span><span id="DataBased-558"><a href="#DataBased-558"><span class="linenos">558</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
+</span><span id="DataBased-559"><a href="#DataBased-559"><span class="linenos">559</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased-560"><a href="#DataBased-560"><span class="linenos">560</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased-561"><a href="#DataBased-561"><span class="linenos">561</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
+</span><span id="DataBased-562"><a href="#DataBased-562"><span class="linenos">562</span></a>
+</span><span id="DataBased-563"><a href="#DataBased-563"><span class="linenos">563</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased-564"><a href="#DataBased-564"><span class="linenos">564</span></a>
+</span><span id="DataBased-565"><a href="#DataBased-565"><span class="linenos">565</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
+</span><span id="DataBased-566"><a href="#DataBased-566"><span class="linenos">566</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
+</span><span id="DataBased-567"><a href="#DataBased-567"><span class="linenos">567</span></a>
+</span><span id="DataBased-568"><a href="#DataBased-568"><span class="linenos">568</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
+</span><span id="DataBased-569"><a href="#DataBased-569"><span class="linenos">569</span></a>
+</span><span id="DataBased-570"><a href="#DataBased-570"><span class="linenos">570</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
+</span><span id="DataBased-571"><a href="#DataBased-571"><span class="linenos">571</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
+</span><span id="DataBased-572"><a href="#DataBased-572"><span class="linenos">572</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Sqli wrapper so queries don't need to be written except table definitions.</p>
 
 <p>Supports saving and reading dates as datetime objects.</p>
 
@@ -1314,40 +1277,40 @@
             
         <span class="name">DataBased</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">pathier</span><span class="o">.</span><span class="n">pathier</span><span class="o">.</span><span class="n">Pathier</span>,</span><span class="param">	<span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s1">&#39;utf-8&#39;</span>,</span><span class="param">	<span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s1">&#39;</span><span class="si">{levelname}</span><span class="s1">|-|</span><span class="si">{asctime}</span><span class="s1">|-|</span><span class="si">{message}</span><span class="s1">&#39;</span>,</span><span class="param">	<span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span></span>)</span>
 
                 <label class="view-source-button" for="DataBased.__init__-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.__init__"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.__init__-52"><a href="#DataBased.__init__-52"><span class="linenos">52</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
-</span><span id="DataBased.__init__-53"><a href="#DataBased.__init__-53"><span class="linenos">53</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased.__init__-54"><a href="#DataBased.__init__-54"><span class="linenos">54</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
-</span><span id="DataBased.__init__-55"><a href="#DataBased.__init__-55"><span class="linenos">55</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
-</span><span id="DataBased.__init__-56"><a href="#DataBased.__init__-56"><span class="linenos">56</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
-</span><span id="DataBased.__init__-57"><a href="#DataBased.__init__-57"><span class="linenos">57</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
-</span><span id="DataBased.__init__-58"><a href="#DataBased.__init__-58"><span class="linenos">58</span></a>    <span class="p">):</span>
-</span><span id="DataBased.__init__-59"><a href="#DataBased.__init__-59"><span class="linenos">59</span></a>        <span class="sd">&quot;&quot;&quot;</span>
-</span><span id="DataBased.__init__-60"><a href="#DataBased.__init__-60"><span class="linenos">60</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.__init__-61"><a href="#DataBased.__init__-61"><span class="linenos">61</span></a>
-</span><span id="DataBased.__init__-62"><a href="#DataBased.__init__-62"><span class="linenos">62</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
-</span><span id="DataBased.__init__-63"><a href="#DataBased.__init__-63"><span class="linenos">63</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
-</span><span id="DataBased.__init__-64"><a href="#DataBased.__init__-64"><span class="linenos">64</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
-</span><span id="DataBased.__init__-65"><a href="#DataBased.__init__-65"><span class="linenos">65</span></a><span class="sd">        same directory.</span>
-</span><span id="DataBased.__init__-66"><a href="#DataBased.__init__-66"><span class="linenos">66</span></a>
-</span><span id="DataBased.__init__-67"><a href="#DataBased.__init__-67"><span class="linenos">67</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
-</span><span id="DataBased.__init__-68"><a href="#DataBased.__init__-68"><span class="linenos">68</span></a>
-</span><span id="DataBased.__init__-69"><a href="#DataBased.__init__-69"><span class="linenos">69</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
-</span><span id="DataBased.__init__-70"><a href="#DataBased.__init__-70"><span class="linenos">70</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
-</span><span id="DataBased.__init__-71"><a href="#DataBased.__init__-71"><span class="linenos">71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
-</span><span id="DataBased.__init__-72"><a href="#DataBased.__init__-72"><span class="linenos">72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
-</span><span id="DataBased.__init__-73"><a href="#DataBased.__init__-73"><span class="linenos">73</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
-</span><span id="DataBased.__init__-74"><a href="#DataBased.__init__-74"><span class="linenos">74</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
-</span><span id="DataBased.__init__-75"><a href="#DataBased.__init__-75"><span class="linenos">75</span></a>        <span class="p">)</span>
-</span><span id="DataBased.__init__-76"><a href="#DataBased.__init__-76"><span class="linenos">76</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="DataBased.__init__-77"><a href="#DataBased.__init__-77"><span class="linenos">77</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.__init__-53"><a href="#DataBased.__init__-53"><span class="linenos">53</span></a>    <span class="k">def</span> <span class="fm">__init__</span><span class="p">(</span>
+</span><span id="DataBased.__init__-54"><a href="#DataBased.__init__-54"><span class="linenos">54</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased.__init__-55"><a href="#DataBased.__init__-55"><span class="linenos">55</span></a>        <span class="n">dbpath</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="n">Pathier</span><span class="p">,</span>
+</span><span id="DataBased.__init__-56"><a href="#DataBased.__init__-56"><span class="linenos">56</span></a>        <span class="n">logger_encoding</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;utf-8&quot;</span><span class="p">,</span>
+</span><span id="DataBased.__init__-57"><a href="#DataBased.__init__-57"><span class="linenos">57</span></a>        <span class="n">logger_message_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;</span><span class="si">{levelname}</span><span class="s2">|-|</span><span class="si">{asctime}</span><span class="s2">|-|</span><span class="si">{message}</span><span class="s2">&quot;</span><span class="p">,</span>
+</span><span id="DataBased.__init__-58"><a href="#DataBased.__init__-58"><span class="linenos">58</span></a>        <span class="n">connection_timeout</span><span class="p">:</span> <span class="nb">float</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
+</span><span id="DataBased.__init__-59"><a href="#DataBased.__init__-59"><span class="linenos">59</span></a>    <span class="p">):</span>
+</span><span id="DataBased.__init__-60"><a href="#DataBased.__init__-60"><span class="linenos">60</span></a>        <span class="sd">&quot;&quot;&quot;</span>
+</span><span id="DataBased.__init__-61"><a href="#DataBased.__init__-61"><span class="linenos">61</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.__init__-62"><a href="#DataBased.__init__-62"><span class="linenos">62</span></a>
+</span><span id="DataBased.__init__-63"><a href="#DataBased.__init__-63"><span class="linenos">63</span></a><span class="sd">        * `dbpath`: String or Path object to database file.</span>
+</span><span id="DataBased.__init__-64"><a href="#DataBased.__init__-64"><span class="linenos">64</span></a><span class="sd">        If a relative path is given, it will be relative to the</span>
+</span><span id="DataBased.__init__-65"><a href="#DataBased.__init__-65"><span class="linenos">65</span></a><span class="sd">        current working directory. The log file will be saved to the</span>
+</span><span id="DataBased.__init__-66"><a href="#DataBased.__init__-66"><span class="linenos">66</span></a><span class="sd">        same directory.</span>
+</span><span id="DataBased.__init__-67"><a href="#DataBased.__init__-67"><span class="linenos">67</span></a>
+</span><span id="DataBased.__init__-68"><a href="#DataBased.__init__-68"><span class="linenos">68</span></a><span class="sd">        * `logger_message_format`: `{` style format string for the logger object.</span>
+</span><span id="DataBased.__init__-69"><a href="#DataBased.__init__-69"><span class="linenos">69</span></a>
+</span><span id="DataBased.__init__-70"><a href="#DataBased.__init__-70"><span class="linenos">70</span></a><span class="sd">        * `connection_timeout`: The number of seconds to wait when trying to connect to the database before throwing an error.&quot;&quot;&quot;</span>
+</span><span id="DataBased.__init__-71"><a href="#DataBased.__init__-71"><span class="linenos">71</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span>
+</span><span id="DataBased.__init__-72"><a href="#DataBased.__init__-72"><span class="linenos">72</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbname</span> <span class="o">=</span> <span class="n">Pathier</span><span class="p">(</span><span class="n">dbpath</span><span class="p">)</span><span class="o">.</span><span class="n">name</span>
+</span><span id="DataBased.__init__-73"><a href="#DataBased.__init__-73"><span class="linenos">73</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="o">.</span><span class="n">parent</span><span class="o">.</span><span class="n">mkdir</span><span class="p">(</span><span class="n">parents</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">exist_ok</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
+</span><span id="DataBased.__init__-74"><a href="#DataBased.__init__-74"><span class="linenos">74</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">_logger_init</span><span class="p">(</span>
+</span><span id="DataBased.__init__-75"><a href="#DataBased.__init__-75"><span class="linenos">75</span></a>            <span class="n">encoding</span><span class="o">=</span><span class="n">logger_encoding</span><span class="p">,</span> <span class="n">message_format</span><span class="o">=</span><span class="n">logger_message_format</span>
+</span><span id="DataBased.__init__-76"><a href="#DataBased.__init__-76"><span class="linenos">76</span></a>        <span class="p">)</span>
+</span><span id="DataBased.__init__-77"><a href="#DataBased.__init__-77"><span class="linenos">77</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+</span><span id="DataBased.__init__-78"><a href="#DataBased.__init__-78"><span class="linenos">78</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span> <span class="o">=</span> <span class="n">connection_timeout</span>
 </span></pre></div>
 
 
             <div class="docstring"><h4 id="params">:params:</h4>
 
 <ul>
 <li><p><code>dbpath</code>: String or Path object to database file.
@@ -1368,24 +1331,24 @@
         <span class="def">def</span>
         <span class="name">open</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.open-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.open"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.open-97"><a href="#DataBased.open-97"><span class="linenos"> 97</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased.open-98"><a href="#DataBased.open-98"><span class="linenos"> 98</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
-</span><span id="DataBased.open-99"><a href="#DataBased.open-99"><span class="linenos"> 99</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
-</span><span id="DataBased.open-100"><a href="#DataBased.open-100"><span class="linenos">100</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
-</span><span id="DataBased.open-101"><a href="#DataBased.open-101"><span class="linenos">101</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
-</span><span id="DataBased.open-102"><a href="#DataBased.open-102"><span class="linenos">102</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
-</span><span id="DataBased.open-103"><a href="#DataBased.open-103"><span class="linenos">103</span></a>        <span class="p">)</span>
-</span><span id="DataBased.open-104"><a href="#DataBased.open-104"><span class="linenos">104</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
-</span><span id="DataBased.open-105"><a href="#DataBased.open-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
-</span><span id="DataBased.open-106"><a href="#DataBased.open-106"><span class="linenos">106</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.open-98"><a href="#DataBased.open-98"><span class="linenos"> 98</span></a>    <span class="k">def</span> <span class="nf">open</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased.open-99"><a href="#DataBased.open-99"><span class="linenos"> 99</span></a>        <span class="sd">&quot;&quot;&quot;Open connection to db.&quot;&quot;&quot;</span>
+</span><span id="DataBased.open-100"><a href="#DataBased.open-100"><span class="linenos">100</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span> <span class="o">=</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">connect</span><span class="p">(</span>
+</span><span id="DataBased.open-101"><a href="#DataBased.open-101"><span class="linenos">101</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">dbpath</span><span class="p">,</span>
+</span><span id="DataBased.open-102"><a href="#DataBased.open-102"><span class="linenos">102</span></a>            <span class="n">detect_types</span><span class="o">=</span><span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_DECLTYPES</span> <span class="o">|</span> <span class="n">sqlite3</span><span class="o">.</span><span class="n">PARSE_COLNAMES</span><span class="p">,</span>
+</span><span id="DataBased.open-103"><a href="#DataBased.open-103"><span class="linenos">103</span></a>            <span class="n">timeout</span><span class="o">=</span><span class="bp">self</span><span class="o">.</span><span class="n">connection_timeout</span><span class="p">,</span>
+</span><span id="DataBased.open-104"><a href="#DataBased.open-104"><span class="linenos">104</span></a>        <span class="p">)</span>
+</span><span id="DataBased.open-105"><a href="#DataBased.open-105"><span class="linenos">105</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="s2">&quot;pragma foreign_keys = 1;&quot;</span><span class="p">)</span>
+</span><span id="DataBased.open-106"><a href="#DataBased.open-106"><span class="linenos">106</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">cursor</span><span class="p">()</span>
+</span><span id="DataBased.open-107"><a href="#DataBased.open-107"><span class="linenos">107</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">True</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Open connection to db.</p>
 </div>
 
 
@@ -1397,23 +1360,23 @@
         <span class="def">def</span>
         <span class="name">close</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.close-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.close"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.close-108"><a href="#DataBased.close-108"><span class="linenos">108</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased.close-109"><a href="#DataBased.close-109"><span class="linenos">109</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
-</span><span id="DataBased.close-110"><a href="#DataBased.close-110"><span class="linenos">110</span></a>
-</span><span id="DataBased.close-111"><a href="#DataBased.close-111"><span class="linenos">111</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
-</span><span id="DataBased.close-112"><a href="#DataBased.close-112"><span class="linenos">112</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
-</span><span id="DataBased.close-113"><a href="#DataBased.close-113"><span class="linenos">113</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
-</span><span id="DataBased.close-114"><a href="#DataBased.close-114"><span class="linenos">114</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
-</span><span id="DataBased.close-115"><a href="#DataBased.close-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
-</span><span id="DataBased.close-116"><a href="#DataBased.close-116"><span class="linenos">116</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.close-109"><a href="#DataBased.close-109"><span class="linenos">109</span></a>    <span class="k">def</span> <span class="nf">close</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased.close-110"><a href="#DataBased.close-110"><span class="linenos">110</span></a>        <span class="sd">&quot;&quot;&quot;Save and close connection to db.</span>
+</span><span id="DataBased.close-111"><a href="#DataBased.close-111"><span class="linenos">111</span></a>
+</span><span id="DataBased.close-112"><a href="#DataBased.close-112"><span class="linenos">112</span></a><span class="sd">        Call this as soon as you are done using the database if you have</span>
+</span><span id="DataBased.close-113"><a href="#DataBased.close-113"><span class="linenos">113</span></a><span class="sd">        multiple threads or processes using the same database.&quot;&quot;&quot;</span>
+</span><span id="DataBased.close-114"><a href="#DataBased.close-114"><span class="linenos">114</span></a>        <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span><span class="p">:</span>
+</span><span id="DataBased.close-115"><a href="#DataBased.close-115"><span class="linenos">115</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">commit</span><span class="p">()</span>
+</span><span id="DataBased.close-116"><a href="#DataBased.close-116"><span class="linenos">116</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection</span><span class="o">.</span><span class="n">close</span><span class="p">()</span>
+</span><span id="DataBased.close-117"><a href="#DataBased.close-117"><span class="linenos">117</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">connection_open</span> <span class="o">=</span> <span class="kc">False</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Save and close connection to db.</p>
 
 <p>Call this as soon as you are done using the database if you have
 multiple threads or processes using the same database.</p>
@@ -1428,17 +1391,17 @@
         <span class="def">def</span>
         <span class="name">vacuum</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.vacuum-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.vacuum"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.vacuum-189"><a href="#DataBased.vacuum-189"><span class="linenos">189</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
-</span><span id="DataBased.vacuum-190"><a href="#DataBased.vacuum-190"><span class="linenos">190</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
-</span><span id="DataBased.vacuum-191"><a href="#DataBased.vacuum-191"><span class="linenos">191</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.vacuum-190"><a href="#DataBased.vacuum-190"><span class="linenos">190</span></a>    <span class="k">def</span> <span class="nf">vacuum</span><span class="p">(</span><span class="bp">self</span><span class="p">):</span>
+</span><span id="DataBased.vacuum-191"><a href="#DataBased.vacuum-191"><span class="linenos">191</span></a>        <span class="sd">&quot;&quot;&quot;Reduce disk size of the database with a `VACUUM` query.&quot;&quot;&quot;</span>
+</span><span id="DataBased.vacuum-192"><a href="#DataBased.vacuum-192"><span class="linenos">192</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">query</span><span class="p">(</span><span class="s2">&quot;VACUUM;&quot;</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Reduce disk size of the database with a <code>VACUUM</code> query.</p>
 </div>
 
 
@@ -1450,19 +1413,19 @@
         <span class="def">def</span>
         <span class="name">query</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span>, </span><span class="param"><span class="n">query_</span></span><span class="return-annotation">) -> <span class="nb">list</span><span class="p">[</span><span class="n">typing</span><span class="o">.</span><span class="n">Any</span><span class="p">]</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.query-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.query"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.query-193"><a href="#DataBased.query-193"><span class="linenos">193</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.query-194"><a href="#DataBased.query-194"><span class="linenos">194</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
-</span><span id="DataBased.query-195"><a href="#DataBased.query-195"><span class="linenos">195</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
-</span><span id="DataBased.query-196"><a href="#DataBased.query-196"><span class="linenos">196</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
-</span><span id="DataBased.query-197"><a href="#DataBased.query-197"><span class="linenos">197</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.query-194"><a href="#DataBased.query-194"><span class="linenos">194</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.query-195"><a href="#DataBased.query-195"><span class="linenos">195</span></a>    <span class="k">def</span> <span class="nf">query</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">query_</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="n">Any</span><span class="p">]:</span>
+</span><span id="DataBased.query-196"><a href="#DataBased.query-196"><span class="linenos">196</span></a>        <span class="sd">&quot;&quot;&quot;Execute an arbitrary query and return the results.&quot;&quot;&quot;</span>
+</span><span id="DataBased.query-197"><a href="#DataBased.query-197"><span class="linenos">197</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query_</span><span class="p">)</span>
+</span><span id="DataBased.query-198"><a href="#DataBased.query-198"><span class="linenos">198</span></a>        <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Execute an arbitrary query and return the results.</p>
 </div>
 
 
@@ -1474,25 +1437,25 @@
         <span class="def">def</span>
         <span class="name">create_tables</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span>, </span><span class="param"><span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.create_tables-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.create_tables"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.create_tables-199"><a href="#DataBased.create_tables-199"><span class="linenos">199</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.create_tables-200"><a href="#DataBased.create_tables-200"><span class="linenos">200</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
-</span><span id="DataBased.create_tables-201"><a href="#DataBased.create_tables-201"><span class="linenos">201</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
-</span><span id="DataBased.create_tables-202"><a href="#DataBased.create_tables-202"><span class="linenos">202</span></a>
-</span><span id="DataBased.create_tables-203"><a href="#DataBased.create_tables-203"><span class="linenos">203</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
-</span><span id="DataBased.create_tables-204"><a href="#DataBased.create_tables-204"><span class="linenos">204</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
-</span><span id="DataBased.create_tables-205"><a href="#DataBased.create_tables-205"><span class="linenos">205</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
-</span><span id="DataBased.create_tables-206"><a href="#DataBased.create_tables-206"><span class="linenos">206</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
-</span><span id="DataBased.create_tables-207"><a href="#DataBased.create_tables-207"><span class="linenos">207</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
-</span><span id="DataBased.create_tables-208"><a href="#DataBased.create_tables-208"><span class="linenos">208</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="DataBased.create_tables-209"><a href="#DataBased.create_tables-209"><span class="linenos">209</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.create_tables-200"><a href="#DataBased.create_tables-200"><span class="linenos">200</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.create_tables-201"><a href="#DataBased.create_tables-201"><span class="linenos">201</span></a>    <span class="k">def</span> <span class="nf">create_tables</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">[]):</span>
+</span><span id="DataBased.create_tables-202"><a href="#DataBased.create_tables-202"><span class="linenos">202</span></a>        <span class="sd">&quot;&quot;&quot;Create tables if they don&#39;t exist.</span>
+</span><span id="DataBased.create_tables-203"><a href="#DataBased.create_tables-203"><span class="linenos">203</span></a>
+</span><span id="DataBased.create_tables-204"><a href="#DataBased.create_tables-204"><span class="linenos">204</span></a><span class="sd">        :param `table_defs`: Each definition should be in the form `table_name(column_definitions)`&quot;&quot;&quot;</span>
+</span><span id="DataBased.create_tables-205"><a href="#DataBased.create_tables-205"><span class="linenos">205</span></a>        <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">table_defs</span><span class="p">)</span> <span class="o">&gt;</span> <span class="mi">0</span><span class="p">:</span>
+</span><span id="DataBased.create_tables-206"><a href="#DataBased.create_tables-206"><span class="linenos">206</span></a>            <span class="n">table_names</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">()</span>
+</span><span id="DataBased.create_tables-207"><a href="#DataBased.create_tables-207"><span class="linenos">207</span></a>            <span class="k">for</span> <span class="n">table</span> <span class="ow">in</span> <span class="n">table_defs</span><span class="p">:</span>
+</span><span id="DataBased.create_tables-208"><a href="#DataBased.create_tables-208"><span class="linenos">208</span></a>                <span class="k">if</span> <span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="o">.</span><span class="n">strip</span><span class="p">()</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">table_names</span><span class="p">:</span>
+</span><span id="DataBased.create_tables-209"><a href="#DataBased.create_tables-209"><span class="linenos">209</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="DataBased.create_tables-210"><a href="#DataBased.create_tables-210"><span class="linenos">210</span></a>                    <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;</span><span class="si">{</span><span class="n">table</span><span class="o">.</span><span class="n">split</span><span class="p">(</span><span class="s2">&quot;(&quot;</span><span class="p">)[</span><span class="mi">0</span><span class="p">]</span><span class="si">}</span><span class="s1"> table created.&#39;</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Create tables if they don't exist.</p>
 
 <h6 id="parameters">Parameters</h6>
 
@@ -1510,28 +1473,28 @@
         <span class="def">def</span>
         <span class="name">create_table</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span>, </span><span class="param"><span class="n">table</span><span class="p">:</span> <span class="nb">str</span>, </span><span class="param"><span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.create_table-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.create_table"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.create_table-211"><a href="#DataBased.create_table-211"><span class="linenos">211</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.create_table-212"><a href="#DataBased.create_table-212"><span class="linenos">212</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
-</span><span id="DataBased.create_table-213"><a href="#DataBased.create_table-213"><span class="linenos">213</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
-</span><span id="DataBased.create_table-214"><a href="#DataBased.create_table-214"><span class="linenos">214</span></a>
-</span><span id="DataBased.create_table-215"><a href="#DataBased.create_table-215"><span class="linenos">215</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.create_table-216"><a href="#DataBased.create_table-216"><span class="linenos">216</span></a>
-</span><span id="DataBased.create_table-217"><a href="#DataBased.create_table-217"><span class="linenos">217</span></a><span class="sd">        `table`: Name of the table to create.</span>
-</span><span id="DataBased.create_table-218"><a href="#DataBased.create_table-218"><span class="linenos">218</span></a>
-</span><span id="DataBased.create_table-219"><a href="#DataBased.create_table-219"><span class="linenos">219</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
-</span><span id="DataBased.create_table-220"><a href="#DataBased.create_table-220"><span class="linenos">220</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
-</span><span id="DataBased.create_table-221"><a href="#DataBased.create_table-221"><span class="linenos">221</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
-</span><span id="DataBased.create_table-222"><a href="#DataBased.create_table-222"><span class="linenos">222</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
-</span><span id="DataBased.create_table-223"><a href="#DataBased.create_table-223"><span class="linenos">223</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="DataBased.create_table-224"><a href="#DataBased.create_table-224"><span class="linenos">224</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.create_table-212"><a href="#DataBased.create_table-212"><span class="linenos">212</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.create_table-213"><a href="#DataBased.create_table-213"><span class="linenos">213</span></a>    <span class="k">def</span> <span class="nf">create_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column_defs</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]):</span>
+</span><span id="DataBased.create_table-214"><a href="#DataBased.create_table-214"><span class="linenos">214</span></a>        <span class="sd">&quot;&quot;&quot;Create a table if it doesn&#39;t exist.</span>
+</span><span id="DataBased.create_table-215"><a href="#DataBased.create_table-215"><span class="linenos">215</span></a>
+</span><span id="DataBased.create_table-216"><a href="#DataBased.create_table-216"><span class="linenos">216</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.create_table-217"><a href="#DataBased.create_table-217"><span class="linenos">217</span></a>
+</span><span id="DataBased.create_table-218"><a href="#DataBased.create_table-218"><span class="linenos">218</span></a><span class="sd">        `table`: Name of the table to create.</span>
+</span><span id="DataBased.create_table-219"><a href="#DataBased.create_table-219"><span class="linenos">219</span></a>
+</span><span id="DataBased.create_table-220"><a href="#DataBased.create_table-220"><span class="linenos">220</span></a><span class="sd">        `column_defs`: List of column definitions in proper Sqlite3 sytax.</span>
+</span><span id="DataBased.create_table-221"><a href="#DataBased.create_table-221"><span class="linenos">221</span></a><span class="sd">        i.e. `&quot;column_name text unique&quot;` or `&quot;column_name int primary key&quot;` etc.&quot;&quot;&quot;</span>
+</span><span id="DataBased.create_table-222"><a href="#DataBased.create_table-222"><span class="linenos">222</span></a>        <span class="k">if</span> <span class="n">table</span> <span class="ow">not</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_table_names</span><span class="p">():</span>
+</span><span id="DataBased.create_table-223"><a href="#DataBased.create_table-223"><span class="linenos">223</span></a>            <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;create table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">](</span><span class="si">{</span><span class="s1">&#39;, &#39;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column_defs</span><span class="p">)</span><span class="si">}</span><span class="s2">);&quot;</span>
+</span><span id="DataBased.create_table-224"><a href="#DataBased.create_table-224"><span class="linenos">224</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="DataBased.create_table-225"><a href="#DataBased.create_table-225"><span class="linenos">225</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;&#39;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">&#39; table created.&quot;</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Create a table if it doesn't exist.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -1550,21 +1513,21 @@
         <span class="def">def</span>
         <span class="name">get_table_names</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span></span><span class="return-annotation">) -> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.get_table_names-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.get_table_names"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_table_names-226"><a href="#DataBased.get_table_names-226"><span class="linenos">226</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.get_table_names-227"><a href="#DataBased.get_table_names-227"><span class="linenos">227</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="DataBased.get_table_names-228"><a href="#DataBased.get_table_names-228"><span class="linenos">228</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
-</span><span id="DataBased.get_table_names-229"><a href="#DataBased.get_table_names-229"><span class="linenos">229</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.get_table_names-230"><a href="#DataBased.get_table_names-230"><span class="linenos">230</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
-</span><span id="DataBased.get_table_names-231"><a href="#DataBased.get_table_names-231"><span class="linenos">231</span></a>        <span class="p">)</span>
-</span><span id="DataBased.get_table_names-232"><a href="#DataBased.get_table_names-232"><span class="linenos">232</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_table_names-227"><a href="#DataBased.get_table_names-227"><span class="linenos">227</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.get_table_names-228"><a href="#DataBased.get_table_names-228"><span class="linenos">228</span></a>    <span class="k">def</span> <span class="nf">get_table_names</span><span class="p">(</span><span class="bp">self</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="DataBased.get_table_names-229"><a href="#DataBased.get_table_names-229"><span class="linenos">229</span></a>        <span class="sd">&quot;&quot;&quot;Returns a list of table names from the database.&quot;&quot;&quot;</span>
+</span><span id="DataBased.get_table_names-230"><a href="#DataBased.get_table_names-230"><span class="linenos">230</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.get_table_names-231"><a href="#DataBased.get_table_names-231"><span class="linenos">231</span></a>            <span class="s1">&#39;select name from sqlite_Schema where type = &quot;table&quot; and name not like &quot;sqlite_%&quot;;&#39;</span>
+</span><span id="DataBased.get_table_names-232"><a href="#DataBased.get_table_names-232"><span class="linenos">232</span></a>        <span class="p">)</span>
+</span><span id="DataBased.get_table_names-233"><a href="#DataBased.get_table_names-233"><span class="linenos">233</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">result</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">result</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()]</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Returns a list of table names from the database.</p>
 </div>
 
 
@@ -1576,19 +1539,19 @@
         <span class="def">def</span>
         <span class="name">get_column_names</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span>, </span><span class="param"><span class="n">table</span><span class="p">:</span> <span class="nb">str</span></span><span class="return-annotation">) -> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.get_column_names-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.get_column_names"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_column_names-234"><a href="#DataBased.get_column_names-234"><span class="linenos">234</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.get_column_names-235"><a href="#DataBased.get_column_names-235"><span class="linenos">235</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
-</span><span id="DataBased.get_column_names-236"><a href="#DataBased.get_column_names-236"><span class="linenos">236</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
-</span><span id="DataBased.get_column_names-237"><a href="#DataBased.get_column_names-237"><span class="linenos">237</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
-</span><span id="DataBased.get_column_names-238"><a href="#DataBased.get_column_names-238"><span class="linenos">238</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_column_names-235"><a href="#DataBased.get_column_names-235"><span class="linenos">235</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.get_column_names-236"><a href="#DataBased.get_column_names-236"><span class="linenos">236</span></a>    <span class="k">def</span> <span class="nf">get_column_names</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]:</span>
+</span><span id="DataBased.get_column_names-237"><a href="#DataBased.get_column_names-237"><span class="linenos">237</span></a>        <span class="sd">&quot;&quot;&quot;Return a list of column names from a table.&quot;&quot;&quot;</span>
+</span><span id="DataBased.get_column_names-238"><a href="#DataBased.get_column_names-238"><span class="linenos">238</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where 1=0;&quot;</span><span class="p">)</span>
+</span><span id="DataBased.get_column_names-239"><a href="#DataBased.get_column_names-239"><span class="linenos">239</span></a>        <span class="k">return</span> <span class="p">[</span><span class="n">description</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span> <span class="k">for</span> <span class="n">description</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">description</span><span class="p">]</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Return a list of column names from a table.</p>
 </div>
 
 
@@ -1600,45 +1563,45 @@
         <span class="def">def</span>
         <span class="name">count</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">int</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.count-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.count"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.count-240"><a href="#DataBased.count-240"><span class="linenos">240</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.count-241"><a href="#DataBased.count-241"><span class="linenos">241</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
-</span><span id="DataBased.count-242"><a href="#DataBased.count-242"><span class="linenos">242</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased.count-243"><a href="#DataBased.count-243"><span class="linenos">243</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased.count-244"><a href="#DataBased.count-244"><span class="linenos">244</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.count-245"><a href="#DataBased.count-245"><span class="linenos">245</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased.count-246"><a href="#DataBased.count-246"><span class="linenos">246</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased.count-247"><a href="#DataBased.count-247"><span class="linenos">247</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
-</span><span id="DataBased.count-248"><a href="#DataBased.count-248"><span class="linenos">248</span></a>
-</span><span id="DataBased.count-249"><a href="#DataBased.count-249"><span class="linenos">249</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.count-250"><a href="#DataBased.count-250"><span class="linenos">250</span></a>
-</span><span id="DataBased.count-251"><a href="#DataBased.count-251"><span class="linenos">251</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="DataBased.count-252"><a href="#DataBased.count-252"><span class="linenos">252</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="DataBased.count-253"><a href="#DataBased.count-253"><span class="linenos">253</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="DataBased.count-254"><a href="#DataBased.count-254"><span class="linenos">254</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
-</span><span id="DataBased.count-255"><a href="#DataBased.count-255"><span class="linenos">255</span></a>
-</span><span id="DataBased.count-256"><a href="#DataBased.count-256"><span class="linenos">256</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
-</span><span id="DataBased.count-257"><a href="#DataBased.count-257"><span class="linenos">257</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
-</span><span id="DataBased.count-258"><a href="#DataBased.count-258"><span class="linenos">258</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
-</span><span id="DataBased.count-259"><a href="#DataBased.count-259"><span class="linenos">259</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased.count-260"><a href="#DataBased.count-260"><span class="linenos">260</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="DataBased.count-261"><a href="#DataBased.count-261"><span class="linenos">261</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.count-262"><a href="#DataBased.count-262"><span class="linenos">262</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased.count-263"><a href="#DataBased.count-263"><span class="linenos">263</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.count-264"><a href="#DataBased.count-264"><span class="linenos">264</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased.count-265"><a href="#DataBased.count-265"><span class="linenos">265</span></a>                <span class="p">)</span>
-</span><span id="DataBased.count-266"><a href="#DataBased.count-266"><span class="linenos">266</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.count-267"><a href="#DataBased.count-267"><span class="linenos">267</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="DataBased.count-268"><a href="#DataBased.count-268"><span class="linenos">268</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
-</span><span id="DataBased.count-269"><a href="#DataBased.count-269"><span class="linenos">269</span></a>        <span class="k">except</span><span class="p">:</span>
-</span><span id="DataBased.count-270"><a href="#DataBased.count-270"><span class="linenos">270</span></a>            <span class="k">return</span> <span class="mi">0</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.count-241"><a href="#DataBased.count-241"><span class="linenos">241</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.count-242"><a href="#DataBased.count-242"><span class="linenos">242</span></a>    <span class="k">def</span> <span class="nf">count</span><span class="p">(</span>
+</span><span id="DataBased.count-243"><a href="#DataBased.count-243"><span class="linenos">243</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased.count-244"><a href="#DataBased.count-244"><span class="linenos">244</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased.count-245"><a href="#DataBased.count-245"><span class="linenos">245</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.count-246"><a href="#DataBased.count-246"><span class="linenos">246</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased.count-247"><a href="#DataBased.count-247"><span class="linenos">247</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased.count-248"><a href="#DataBased.count-248"><span class="linenos">248</span></a>        <span class="sd">&quot;&quot;&quot;Return number of items in `table`.</span>
+</span><span id="DataBased.count-249"><a href="#DataBased.count-249"><span class="linenos">249</span></a>
+</span><span id="DataBased.count-250"><a href="#DataBased.count-250"><span class="linenos">250</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.count-251"><a href="#DataBased.count-251"><span class="linenos">251</span></a>
+</span><span id="DataBased.count-252"><a href="#DataBased.count-252"><span class="linenos">252</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="DataBased.count-253"><a href="#DataBased.count-253"><span class="linenos">253</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="DataBased.count-254"><a href="#DataBased.count-254"><span class="linenos">254</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="DataBased.count-255"><a href="#DataBased.count-255"><span class="linenos">255</span></a><span class="sd">        If `None`, all rows from the table will be counted.</span>
+</span><span id="DataBased.count-256"><a href="#DataBased.count-256"><span class="linenos">256</span></a>
+</span><span id="DataBased.count-257"><a href="#DataBased.count-257"><span class="linenos">257</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column</span>
+</span><span id="DataBased.count-258"><a href="#DataBased.count-258"><span class="linenos">258</span></a><span class="sd">        in `match_criteria` will be matched as a substring.</span>
+</span><span id="DataBased.count-259"><a href="#DataBased.count-259"><span class="linenos">259</span></a><span class="sd">        Has no effect if `match_criteria` is `None`.</span>
+</span><span id="DataBased.count-260"><a href="#DataBased.count-260"><span class="linenos">260</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased.count-261"><a href="#DataBased.count-261"><span class="linenos">261</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select count(_rowid_) from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="DataBased.count-262"><a href="#DataBased.count-262"><span class="linenos">262</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.count-263"><a href="#DataBased.count-263"><span class="linenos">263</span></a>            <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased.count-264"><a href="#DataBased.count-264"><span class="linenos">264</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.count-265"><a href="#DataBased.count-265"><span class="linenos">265</span></a>                    <span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2"> where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased.count-266"><a href="#DataBased.count-266"><span class="linenos">266</span></a>                <span class="p">)</span>
+</span><span id="DataBased.count-267"><a href="#DataBased.count-267"><span class="linenos">267</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.count-268"><a href="#DataBased.count-268"><span class="linenos">268</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;</span><span class="si">{</span><span class="n">query</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="DataBased.count-269"><a href="#DataBased.count-269"><span class="linenos">269</span></a>            <span class="k">return</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchone</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>
+</span><span id="DataBased.count-270"><a href="#DataBased.count-270"><span class="linenos">270</span></a>        <span class="k">except</span><span class="p">:</span>
+</span><span id="DataBased.count-271"><a href="#DataBased.count-271"><span class="linenos">271</span></a>            <span class="k">return</span> <span class="mi">0</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Return number of items in <code>table</code>.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -1661,53 +1624,53 @@
         <span class="def">def</span>
         <span class="name">add_row</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">typing</span><span class="o">.</span><span class="n">Any</span><span class="p">]</span>,</span><span class="param">	<span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span></span><span class="return-annotation">) -> <span class="nb">bool</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.add_row-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.add_row"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_row-272"><a href="#DataBased.add_row-272"><span class="linenos">272</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.add_row-273"><a href="#DataBased.add_row-273"><span class="linenos">273</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
-</span><span id="DataBased.add_row-274"><a href="#DataBased.add_row-274"><span class="linenos">274</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased.add_row-275"><a href="#DataBased.add_row-275"><span class="linenos">275</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="DataBased.add_row-276"><a href="#DataBased.add_row-276"><span class="linenos">276</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
-</span><span id="DataBased.add_row-277"><a href="#DataBased.add_row-277"><span class="linenos">277</span></a>
-</span><span id="DataBased.add_row-278"><a href="#DataBased.add_row-278"><span class="linenos">278</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
-</span><span id="DataBased.add_row-279"><a href="#DataBased.add_row-279"><span class="linenos">279</span></a>
-</span><span id="DataBased.add_row-280"><a href="#DataBased.add_row-280"><span class="linenos">280</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.add_row-281"><a href="#DataBased.add_row-281"><span class="linenos">281</span></a>
-</span><span id="DataBased.add_row-282"><a href="#DataBased.add_row-282"><span class="linenos">282</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="DataBased.add_row-283"><a href="#DataBased.add_row-283"><span class="linenos">283</span></a>
-</span><span id="DataBased.add_row-284"><a href="#DataBased.add_row-284"><span class="linenos">284</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
-</span><span id="DataBased.add_row-285"><a href="#DataBased.add_row-285"><span class="linenos">285</span></a>
-</span><span id="DataBased.add_row-286"><a href="#DataBased.add_row-286"><span class="linenos">286</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="DataBased.add_row-287"><a href="#DataBased.add_row-287"><span class="linenos">287</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="DataBased.add_row-288"><a href="#DataBased.add_row-288"><span class="linenos">288</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="DataBased.add_row-289"><a href="#DataBased.add_row-289"><span class="linenos">289</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
-</span><span id="DataBased.add_row-290"><a href="#DataBased.add_row-290"><span class="linenos">290</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.add_row-291"><a href="#DataBased.add_row-291"><span class="linenos">291</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased.add_row-292"><a href="#DataBased.add_row-292"><span class="linenos">292</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
-</span><span id="DataBased.add_row-293"><a href="#DataBased.add_row-293"><span class="linenos">293</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.add_row-294"><a href="#DataBased.add_row-294"><span class="linenos">294</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
-</span><span id="DataBased.add_row-295"><a href="#DataBased.add_row-295"><span class="linenos">295</span></a>                    <span class="n">values</span><span class="p">,</span>
-</span><span id="DataBased.add_row-296"><a href="#DataBased.add_row-296"><span class="linenos">296</span></a>                <span class="p">)</span>
-</span><span id="DataBased.add_row-297"><a href="#DataBased.add_row-297"><span class="linenos">297</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.add_row-298"><a href="#DataBased.add_row-298"><span class="linenos">298</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.add_row-299"><a href="#DataBased.add_row-299"><span class="linenos">299</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
-</span><span id="DataBased.add_row-300"><a href="#DataBased.add_row-300"><span class="linenos">300</span></a>                <span class="p">)</span>
-</span><span id="DataBased.add_row-301"><a href="#DataBased.add_row-301"><span class="linenos">301</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
-</span><span id="DataBased.add_row-302"><a href="#DataBased.add_row-302"><span class="linenos">302</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="DataBased.add_row-303"><a href="#DataBased.add_row-303"><span class="linenos">303</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased.add_row-304"><a href="#DataBased.add_row-304"><span class="linenos">304</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
-</span><span id="DataBased.add_row-305"><a href="#DataBased.add_row-305"><span class="linenos">305</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
-</span><span id="DataBased.add_row-306"><a href="#DataBased.add_row-306"><span class="linenos">306</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
-</span><span id="DataBased.add_row-307"><a href="#DataBased.add_row-307"><span class="linenos">307</span></a>                <span class="p">)</span>
-</span><span id="DataBased.add_row-308"><a href="#DataBased.add_row-308"><span class="linenos">308</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.add_row-309"><a href="#DataBased.add_row-309"><span class="linenos">309</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
-</span><span id="DataBased.add_row-310"><a href="#DataBased.add_row-310"><span class="linenos">310</span></a>            <span class="k">return</span> <span class="kc">False</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_row-273"><a href="#DataBased.add_row-273"><span class="linenos">273</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.add_row-274"><a href="#DataBased.add_row-274"><span class="linenos">274</span></a>    <span class="k">def</span> <span class="nf">add_row</span><span class="p">(</span>
+</span><span id="DataBased.add_row-275"><a href="#DataBased.add_row-275"><span class="linenos">275</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased.add_row-276"><a href="#DataBased.add_row-276"><span class="linenos">276</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="DataBased.add_row-277"><a href="#DataBased.add_row-277"><span class="linenos">277</span></a>        <span class="sd">&quot;&quot;&quot;Add a row of values to a table.</span>
+</span><span id="DataBased.add_row-278"><a href="#DataBased.add_row-278"><span class="linenos">278</span></a>
+</span><span id="DataBased.add_row-279"><a href="#DataBased.add_row-279"><span class="linenos">279</span></a><span class="sd">        Returns whether the addition was successful or not.</span>
+</span><span id="DataBased.add_row-280"><a href="#DataBased.add_row-280"><span class="linenos">280</span></a>
+</span><span id="DataBased.add_row-281"><a href="#DataBased.add_row-281"><span class="linenos">281</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.add_row-282"><a href="#DataBased.add_row-282"><span class="linenos">282</span></a>
+</span><span id="DataBased.add_row-283"><a href="#DataBased.add_row-283"><span class="linenos">283</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="DataBased.add_row-284"><a href="#DataBased.add_row-284"><span class="linenos">284</span></a>
+</span><span id="DataBased.add_row-285"><a href="#DataBased.add_row-285"><span class="linenos">285</span></a><span class="sd">        `values`: A tuple of values to be inserted into the table.</span>
+</span><span id="DataBased.add_row-286"><a href="#DataBased.add_row-286"><span class="linenos">286</span></a>
+</span><span id="DataBased.add_row-287"><a href="#DataBased.add_row-287"><span class="linenos">287</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="DataBased.add_row-288"><a href="#DataBased.add_row-288"><span class="linenos">288</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="DataBased.add_row-289"><a href="#DataBased.add_row-289"><span class="linenos">289</span></a>        <span class="n">parameterizer</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="s2">&quot;?&quot;</span> <span class="k">for</span> <span class="n">_</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="DataBased.add_row-290"><a href="#DataBased.add_row-290"><span class="linenos">290</span></a>        <span class="n">logger_values</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">value</span><span class="p">)</span> <span class="k">for</span> <span class="n">value</span> <span class="ow">in</span> <span class="n">values</span><span class="p">)</span>
+</span><span id="DataBased.add_row-291"><a href="#DataBased.add_row-291"><span class="linenos">291</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.add_row-292"><a href="#DataBased.add_row-292"><span class="linenos">292</span></a>            <span class="k">if</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased.add_row-293"><a href="#DataBased.add_row-293"><span class="linenos">293</span></a>                <span class="n">columns_query</span> <span class="o">=</span> <span class="s2">&quot;, &quot;</span><span class="o">.</span><span class="n">join</span><span class="p">(</span><span class="n">column</span> <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">)</span>
+</span><span id="DataBased.add_row-294"><a href="#DataBased.add_row-294"><span class="linenos">294</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.add_row-295"><a href="#DataBased.add_row-295"><span class="linenos">295</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] (</span><span class="si">{</span><span class="n">columns_query</span><span class="si">}</span><span class="s2">) values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span>
+</span><span id="DataBased.add_row-296"><a href="#DataBased.add_row-296"><span class="linenos">296</span></a>                    <span class="n">values</span><span class="p">,</span>
+</span><span id="DataBased.add_row-297"><a href="#DataBased.add_row-297"><span class="linenos">297</span></a>                <span class="p">)</span>
+</span><span id="DataBased.add_row-298"><a href="#DataBased.add_row-298"><span class="linenos">298</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.add_row-299"><a href="#DataBased.add_row-299"><span class="linenos">299</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.add_row-300"><a href="#DataBased.add_row-300"><span class="linenos">300</span></a>                    <span class="sa">f</span><span class="s2">&quot;insert into [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] values(</span><span class="si">{</span><span class="n">parameterizer</span><span class="si">}</span><span class="s2">);&quot;</span><span class="p">,</span> <span class="n">values</span>
+</span><span id="DataBased.add_row-301"><a href="#DataBased.add_row-301"><span class="linenos">301</span></a>                <span class="p">)</span>
+</span><span id="DataBased.add_row-302"><a href="#DataBased.add_row-302"><span class="linenos">302</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span><span class="p">)</span>
+</span><span id="DataBased.add_row-303"><a href="#DataBased.add_row-303"><span class="linenos">303</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="DataBased.add_row-304"><a href="#DataBased.add_row-304"><span class="linenos">304</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased.add_row-305"><a href="#DataBased.add_row-305"><span class="linenos">305</span></a>            <span class="k">if</span> <span class="s2">&quot;constraint&quot;</span> <span class="ow">not</span> <span class="ow">in</span> <span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">)</span><span class="o">.</span><span class="n">lower</span><span class="p">():</span>
+</span><span id="DataBased.add_row-306"><a href="#DataBased.add_row-306"><span class="linenos">306</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">exception</span><span class="p">(</span>
+</span><span id="DataBased.add_row-307"><a href="#DataBased.add_row-307"><span class="linenos">307</span></a>                    <span class="sa">f</span><span class="s1">&#39;Error adding &quot;</span><span class="si">{</span><span class="n">logger_values</span><span class="si">}</span><span class="s1">&quot; to </span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1"> table.&#39;</span>
+</span><span id="DataBased.add_row-308"><a href="#DataBased.add_row-308"><span class="linenos">308</span></a>                <span class="p">)</span>
+</span><span id="DataBased.add_row-309"><a href="#DataBased.add_row-309"><span class="linenos">309</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.add_row-310"><a href="#DataBased.add_row-310"><span class="linenos">310</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span><span class="nb">str</span><span class="p">(</span><span class="n">e</span><span class="p">))</span>
+</span><span id="DataBased.add_row-311"><a href="#DataBased.add_row-311"><span class="linenos">311</span></a>            <span class="k">return</span> <span class="kc">False</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Add a row of values to a table.</p>
 
 <p>Returns whether the addition was successful or not.</p>
 
@@ -1730,39 +1693,39 @@
         <span class="def">def</span>
         <span class="name">add_rows</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">typing</span><span class="o">.</span><span class="n">Any</span><span class="p">]]</span>,</span><span class="param">	<span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span></span><span class="return-annotation">) -> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.add_rows-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.add_rows"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_rows-312"><a href="#DataBased.add_rows-312"><span class="linenos">312</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.add_rows-313"><a href="#DataBased.add_rows-313"><span class="linenos">313</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
-</span><span id="DataBased.add_rows-314"><a href="#DataBased.add_rows-314"><span class="linenos">314</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased.add_rows-315"><a href="#DataBased.add_rows-315"><span class="linenos">315</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
-</span><span id="DataBased.add_rows-316"><a href="#DataBased.add_rows-316"><span class="linenos">316</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
-</span><span id="DataBased.add_rows-317"><a href="#DataBased.add_rows-317"><span class="linenos">317</span></a>
-</span><span id="DataBased.add_rows-318"><a href="#DataBased.add_rows-318"><span class="linenos">318</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
-</span><span id="DataBased.add_rows-319"><a href="#DataBased.add_rows-319"><span class="linenos">319</span></a>
-</span><span id="DataBased.add_rows-320"><a href="#DataBased.add_rows-320"><span class="linenos">320</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.add_rows-321"><a href="#DataBased.add_rows-321"><span class="linenos">321</span></a>
-</span><span id="DataBased.add_rows-322"><a href="#DataBased.add_rows-322"><span class="linenos">322</span></a><span class="sd">        `table`: The table to insert values into.</span>
-</span><span id="DataBased.add_rows-323"><a href="#DataBased.add_rows-323"><span class="linenos">323</span></a>
-</span><span id="DataBased.add_rows-324"><a href="#DataBased.add_rows-324"><span class="linenos">324</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
-</span><span id="DataBased.add_rows-325"><a href="#DataBased.add_rows-325"><span class="linenos">325</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
-</span><span id="DataBased.add_rows-326"><a href="#DataBased.add_rows-326"><span class="linenos">326</span></a>
-</span><span id="DataBased.add_rows-327"><a href="#DataBased.add_rows-327"><span class="linenos">327</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
-</span><span id="DataBased.add_rows-328"><a href="#DataBased.add_rows-328"><span class="linenos">328</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
-</span><span id="DataBased.add_rows-329"><a href="#DataBased.add_rows-329"><span class="linenos">329</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="DataBased.add_rows-330"><a href="#DataBased.add_rows-330"><span class="linenos">330</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
-</span><span id="DataBased.add_rows-331"><a href="#DataBased.add_rows-331"><span class="linenos">331</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
-</span><span id="DataBased.add_rows-332"><a href="#DataBased.add_rows-332"><span class="linenos">332</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
-</span><span id="DataBased.add_rows-333"><a href="#DataBased.add_rows-333"><span class="linenos">333</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="DataBased.add_rows-334"><a href="#DataBased.add_rows-334"><span class="linenos">334</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.add_rows-335"><a href="#DataBased.add_rows-335"><span class="linenos">335</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
-</span><span id="DataBased.add_rows-336"><a href="#DataBased.add_rows-336"><span class="linenos">336</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_rows-313"><a href="#DataBased.add_rows-313"><span class="linenos">313</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.add_rows-314"><a href="#DataBased.add_rows-314"><span class="linenos">314</span></a>    <span class="k">def</span> <span class="nf">add_rows</span><span class="p">(</span>
+</span><span id="DataBased.add_rows-315"><a href="#DataBased.add_rows-315"><span class="linenos">315</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">values</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased.add_rows-316"><a href="#DataBased.add_rows-316"><span class="linenos">316</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">tuple</span><span class="p">[</span><span class="nb">int</span><span class="p">,</span> <span class="nb">int</span><span class="p">]:</span>
+</span><span id="DataBased.add_rows-317"><a href="#DataBased.add_rows-317"><span class="linenos">317</span></a>        <span class="sd">&quot;&quot;&quot;Add multiple rows of values to a table.</span>
+</span><span id="DataBased.add_rows-318"><a href="#DataBased.add_rows-318"><span class="linenos">318</span></a>
+</span><span id="DataBased.add_rows-319"><a href="#DataBased.add_rows-319"><span class="linenos">319</span></a><span class="sd">        Returns a tuple containing the number of successful additions and the number of failed additions.</span>
+</span><span id="DataBased.add_rows-320"><a href="#DataBased.add_rows-320"><span class="linenos">320</span></a>
+</span><span id="DataBased.add_rows-321"><a href="#DataBased.add_rows-321"><span class="linenos">321</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.add_rows-322"><a href="#DataBased.add_rows-322"><span class="linenos">322</span></a>
+</span><span id="DataBased.add_rows-323"><a href="#DataBased.add_rows-323"><span class="linenos">323</span></a><span class="sd">        `table`: The table to insert values into.</span>
+</span><span id="DataBased.add_rows-324"><a href="#DataBased.add_rows-324"><span class="linenos">324</span></a>
+</span><span id="DataBased.add_rows-325"><a href="#DataBased.add_rows-325"><span class="linenos">325</span></a><span class="sd">        `values`: A list of tuples of values to be inserted into the table.</span>
+</span><span id="DataBased.add_rows-326"><a href="#DataBased.add_rows-326"><span class="linenos">326</span></a><span class="sd">        Each tuple constitutes a single row to be inserted</span>
+</span><span id="DataBased.add_rows-327"><a href="#DataBased.add_rows-327"><span class="linenos">327</span></a>
+</span><span id="DataBased.add_rows-328"><a href="#DataBased.add_rows-328"><span class="linenos">328</span></a><span class="sd">        `columns`: If `None`, `values` is expected to supply a value for every column in the table.</span>
+</span><span id="DataBased.add_rows-329"><a href="#DataBased.add_rows-329"><span class="linenos">329</span></a><span class="sd">        If `columns` is provided, it should contain the same number of elements as `values`.&quot;&quot;&quot;</span>
+</span><span id="DataBased.add_rows-330"><a href="#DataBased.add_rows-330"><span class="linenos">330</span></a>        <span class="n">successes</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="DataBased.add_rows-331"><a href="#DataBased.add_rows-331"><span class="linenos">331</span></a>        <span class="n">failures</span> <span class="o">=</span> <span class="mi">0</span>
+</span><span id="DataBased.add_rows-332"><a href="#DataBased.add_rows-332"><span class="linenos">332</span></a>        <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">values</span><span class="p">:</span>
+</span><span id="DataBased.add_rows-333"><a href="#DataBased.add_rows-333"><span class="linenos">333</span></a>            <span class="k">if</span> <span class="bp">self</span><span class="o">.</span><span class="n">add_row</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">row</span><span class="p">,</span> <span class="n">columns</span><span class="p">):</span>
+</span><span id="DataBased.add_rows-334"><a href="#DataBased.add_rows-334"><span class="linenos">334</span></a>                <span class="n">successes</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="DataBased.add_rows-335"><a href="#DataBased.add_rows-335"><span class="linenos">335</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.add_rows-336"><a href="#DataBased.add_rows-336"><span class="linenos">336</span></a>                <span class="n">failures</span> <span class="o">+=</span> <span class="mi">1</span>
+</span><span id="DataBased.add_rows-337"><a href="#DataBased.add_rows-337"><span class="linenos">337</span></a>        <span class="k">return</span> <span class="p">(</span><span class="n">successes</span><span class="p">,</span> <span class="n">failures</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Add multiple rows of values to a table.</p>
 
 <p>Returns a tuple containing the number of successful additions and the number of failed additions.</p>
 
@@ -1786,79 +1749,79 @@
         <span class="def">def</span>
         <span class="name">get_rows</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>,</span><span class="param">	<span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span>,</span><span class="param">	<span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span>,</span><span class="param">	<span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span></span><span class="return-annotation">) -> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">core</span><span class="o">.</span><span class="n">frame</span><span class="o">.</span><span class="n">DataFrame</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.get_rows-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.get_rows"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_rows-338"><a href="#DataBased.get_rows-338"><span class="linenos">338</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.get_rows-339"><a href="#DataBased.get_rows-339"><span class="linenos">339</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
-</span><span id="DataBased.get_rows-340"><a href="#DataBased.get_rows-340"><span class="linenos">340</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-341"><a href="#DataBased.get_rows-341"><span class="linenos">341</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-342"><a href="#DataBased.get_rows-342"><span class="linenos">342</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-343"><a href="#DataBased.get_rows-343"><span class="linenos">343</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-344"><a href="#DataBased.get_rows-344"><span class="linenos">344</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-345"><a href="#DataBased.get_rows-345"><span class="linenos">345</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-346"><a href="#DataBased.get_rows-346"><span class="linenos">346</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-347"><a href="#DataBased.get_rows-347"><span class="linenos">347</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-348"><a href="#DataBased.get_rows-348"><span class="linenos">348</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-349"><a href="#DataBased.get_rows-349"><span class="linenos">349</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.get_rows-350"><a href="#DataBased.get_rows-350"><span class="linenos">350</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-351"><a href="#DataBased.get_rows-351"><span class="linenos">351</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
-</span><span id="DataBased.get_rows-352"><a href="#DataBased.get_rows-352"><span class="linenos">352</span></a>
-</span><span id="DataBased.get_rows-353"><a href="#DataBased.get_rows-353"><span class="linenos">353</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
-</span><span id="DataBased.get_rows-354"><a href="#DataBased.get_rows-354"><span class="linenos">354</span></a>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.get_rows-339"><a href="#DataBased.get_rows-339"><span class="linenos">339</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.get_rows-340"><a href="#DataBased.get_rows-340"><span class="linenos">340</span></a>    <span class="k">def</span> <span class="nf">get_rows</span><span class="p">(</span>
+</span><span id="DataBased.get_rows-341"><a href="#DataBased.get_rows-341"><span class="linenos">341</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-342"><a href="#DataBased.get_rows-342"><span class="linenos">342</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-343"><a href="#DataBased.get_rows-343"><span class="linenos">343</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-344"><a href="#DataBased.get_rows-344"><span class="linenos">344</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-345"><a href="#DataBased.get_rows-345"><span class="linenos">345</span></a>        <span class="n">sort_by_column</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-346"><a href="#DataBased.get_rows-346"><span class="linenos">346</span></a>        <span class="n">columns_to_return</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-347"><a href="#DataBased.get_rows-347"><span class="linenos">347</span></a>        <span class="n">return_as_dataframe</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-348"><a href="#DataBased.get_rows-348"><span class="linenos">348</span></a>        <span class="n">values_only</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">False</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-349"><a href="#DataBased.get_rows-349"><span class="linenos">349</span></a>        <span class="n">order_by</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-350"><a href="#DataBased.get_rows-350"><span class="linenos">350</span></a>        <span class="n">limit</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">int</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.get_rows-351"><a href="#DataBased.get_rows-351"><span class="linenos">351</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span> <span class="o">|</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-352"><a href="#DataBased.get_rows-352"><span class="linenos">352</span></a>        <span class="sd">&quot;&quot;&quot;Return matching rows from `table`.</span>
+</span><span id="DataBased.get_rows-353"><a href="#DataBased.get_rows-353"><span class="linenos">353</span></a>
+</span><span id="DataBased.get_rows-354"><a href="#DataBased.get_rows-354"><span class="linenos">354</span></a><span class="sd">        By default, rows will be returned as a list of dictionaries of the form `[{&quot;column_name&quot;: value, ...}, ...]`</span>
 </span><span id="DataBased.get_rows-355"><a href="#DataBased.get_rows-355"><span class="linenos">355</span></a>
-</span><span id="DataBased.get_rows-356"><a href="#DataBased.get_rows-356"><span class="linenos">356</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.get_rows-357"><a href="#DataBased.get_rows-357"><span class="linenos">357</span></a>
-</span><span id="DataBased.get_rows-358"><a href="#DataBased.get_rows-358"><span class="linenos">358</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
-</span><span id="DataBased.get_rows-359"><a href="#DataBased.get_rows-359"><span class="linenos">359</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
-</span><span id="DataBased.get_rows-360"><a href="#DataBased.get_rows-360"><span class="linenos">360</span></a><span class="sd">        keys are column names and values are row values.</span>
-</span><span id="DataBased.get_rows-361"><a href="#DataBased.get_rows-361"><span class="linenos">361</span></a>
-</span><span id="DataBased.get_rows-362"><a href="#DataBased.get_rows-362"><span class="linenos">362</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
-</span><span id="DataBased.get_rows-363"><a href="#DataBased.get_rows-363"><span class="linenos">363</span></a>
-</span><span id="DataBased.get_rows-364"><a href="#DataBased.get_rows-364"><span class="linenos">364</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
-</span><span id="DataBased.get_rows-365"><a href="#DataBased.get_rows-365"><span class="linenos">365</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
-</span><span id="DataBased.get_rows-366"><a href="#DataBased.get_rows-366"><span class="linenos">366</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
-</span><span id="DataBased.get_rows-367"><a href="#DataBased.get_rows-367"><span class="linenos">367</span></a>
-</span><span id="DataBased.get_rows-368"><a href="#DataBased.get_rows-368"><span class="linenos">368</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
-</span><span id="DataBased.get_rows-369"><a href="#DataBased.get_rows-369"><span class="linenos">369</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
-</span><span id="DataBased.get_rows-370"><a href="#DataBased.get_rows-370"><span class="linenos">370</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
-</span><span id="DataBased.get_rows-371"><a href="#DataBased.get_rows-371"><span class="linenos">371</span></a>
-</span><span id="DataBased.get_rows-372"><a href="#DataBased.get_rows-372"><span class="linenos">372</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
-</span><span id="DataBased.get_rows-373"><a href="#DataBased.get_rows-373"><span class="linenos">373</span></a>
-</span><span id="DataBased.get_rows-374"><a href="#DataBased.get_rows-374"><span class="linenos">374</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
-</span><span id="DataBased.get_rows-375"><a href="#DataBased.get_rows-375"><span class="linenos">375</span></a>
-</span><span id="DataBased.get_rows-376"><a href="#DataBased.get_rows-376"><span class="linenos">376</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
-</span><span id="DataBased.get_rows-377"><a href="#DataBased.get_rows-377"><span class="linenos">377</span></a>
-</span><span id="DataBased.get_rows-378"><a href="#DataBased.get_rows-378"><span class="linenos">378</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
-</span><span id="DataBased.get_rows-379"><a href="#DataBased.get_rows-379"><span class="linenos">379</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased.get_rows-380"><a href="#DataBased.get_rows-380"><span class="linenos">380</span></a>
-</span><span id="DataBased.get_rows-381"><a href="#DataBased.get_rows-381"><span class="linenos">381</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-382"><a href="#DataBased.get_rows-382"><span class="linenos">382</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
-</span><span id="DataBased.get_rows-383"><a href="#DataBased.get_rows-383"><span class="linenos">383</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
-</span><span id="DataBased.get_rows-384"><a href="#DataBased.get_rows-384"><span class="linenos">384</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="DataBased.get_rows-385"><a href="#DataBased.get_rows-385"><span class="linenos">385</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-386"><a href="#DataBased.get_rows-386"><span class="linenos">386</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased.get_rows-387"><a href="#DataBased.get_rows-387"><span class="linenos">387</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-388"><a href="#DataBased.get_rows-388"><span class="linenos">388</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased.get_rows-389"><a href="#DataBased.get_rows-389"><span class="linenos">389</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-390"><a href="#DataBased.get_rows-390"><span class="linenos">390</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased.get_rows-391"><a href="#DataBased.get_rows-391"><span class="linenos">391</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="DataBased.get_rows-392"><a href="#DataBased.get_rows-392"><span class="linenos">392</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
-</span><span id="DataBased.get_rows-393"><a href="#DataBased.get_rows-393"><span class="linenos">393</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
-</span><span id="DataBased.get_rows-394"><a href="#DataBased.get_rows-394"><span class="linenos">394</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
-</span><span id="DataBased.get_rows-395"><a href="#DataBased.get_rows-395"><span class="linenos">395</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-396"><a href="#DataBased.get_rows-396"><span class="linenos">396</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
-</span><span id="DataBased.get_rows-397"><a href="#DataBased.get_rows-397"><span class="linenos">397</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-398"><a href="#DataBased.get_rows-398"><span class="linenos">398</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
-</span><span id="DataBased.get_rows-399"><a href="#DataBased.get_rows-399"><span class="linenos">399</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-400"><a href="#DataBased.get_rows-400"><span class="linenos">400</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
-</span><span id="DataBased.get_rows-401"><a href="#DataBased.get_rows-401"><span class="linenos">401</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.get_rows-402"><a href="#DataBased.get_rows-402"><span class="linenos">402</span></a>            <span class="k">return</span> <span class="n">results</span>
+</span><span id="DataBased.get_rows-356"><a href="#DataBased.get_rows-356"><span class="linenos">356</span></a>
+</span><span id="DataBased.get_rows-357"><a href="#DataBased.get_rows-357"><span class="linenos">357</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.get_rows-358"><a href="#DataBased.get_rows-358"><span class="linenos">358</span></a>
+</span><span id="DataBased.get_rows-359"><a href="#DataBased.get_rows-359"><span class="linenos">359</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each</span>
+</span><span id="DataBased.get_rows-360"><a href="#DataBased.get_rows-360"><span class="linenos">360</span></a><span class="sd">        tuple is `(columnName, rowValue)` or a dictionary where</span>
+</span><span id="DataBased.get_rows-361"><a href="#DataBased.get_rows-361"><span class="linenos">361</span></a><span class="sd">        keys are column names and values are row values.</span>
+</span><span id="DataBased.get_rows-362"><a href="#DataBased.get_rows-362"><span class="linenos">362</span></a>
+</span><span id="DataBased.get_rows-363"><a href="#DataBased.get_rows-363"><span class="linenos">363</span></a><span class="sd">        `exact_match`: If `False`, the row value for a given column will be matched as a substring.</span>
+</span><span id="DataBased.get_rows-364"><a href="#DataBased.get_rows-364"><span class="linenos">364</span></a>
+</span><span id="DataBased.get_rows-365"><a href="#DataBased.get_rows-365"><span class="linenos">365</span></a><span class="sd">        `sort_by_column`: A column name to sort the results by.</span>
+</span><span id="DataBased.get_rows-366"><a href="#DataBased.get_rows-366"><span class="linenos">366</span></a><span class="sd">        This will sort results in Python after retrieving them from the db.</span>
+</span><span id="DataBased.get_rows-367"><a href="#DataBased.get_rows-367"><span class="linenos">367</span></a><span class="sd">        Use the &#39;order_by&#39; param to use SQLite engine for ordering.</span>
+</span><span id="DataBased.get_rows-368"><a href="#DataBased.get_rows-368"><span class="linenos">368</span></a>
+</span><span id="DataBased.get_rows-369"><a href="#DataBased.get_rows-369"><span class="linenos">369</span></a><span class="sd">        `columns_to_return`: Optional list of column names.</span>
+</span><span id="DataBased.get_rows-370"><a href="#DataBased.get_rows-370"><span class="linenos">370</span></a><span class="sd">        If provided, the elements returned by this function will only contain the provided columns.</span>
+</span><span id="DataBased.get_rows-371"><a href="#DataBased.get_rows-371"><span class="linenos">371</span></a><span class="sd">        Otherwise every column in the row is returned.</span>
+</span><span id="DataBased.get_rows-372"><a href="#DataBased.get_rows-372"><span class="linenos">372</span></a>
+</span><span id="DataBased.get_rows-373"><a href="#DataBased.get_rows-373"><span class="linenos">373</span></a><span class="sd">        `return_as_dataframe`: Return the results as a `pandas.DataFrame` object.</span>
+</span><span id="DataBased.get_rows-374"><a href="#DataBased.get_rows-374"><span class="linenos">374</span></a>
+</span><span id="DataBased.get_rows-375"><a href="#DataBased.get_rows-375"><span class="linenos">375</span></a><span class="sd">        `values_only`: Return the results as a list of tuples.</span>
+</span><span id="DataBased.get_rows-376"><a href="#DataBased.get_rows-376"><span class="linenos">376</span></a>
+</span><span id="DataBased.get_rows-377"><a href="#DataBased.get_rows-377"><span class="linenos">377</span></a><span class="sd">        `order_by`: If given, a `order by {order_by}` clause will be added to the select query.</span>
+</span><span id="DataBased.get_rows-378"><a href="#DataBased.get_rows-378"><span class="linenos">378</span></a>
+</span><span id="DataBased.get_rows-379"><a href="#DataBased.get_rows-379"><span class="linenos">379</span></a><span class="sd">        `limit`: If given, a `limit {limit}` clause will be added to the select query.</span>
+</span><span id="DataBased.get_rows-380"><a href="#DataBased.get_rows-380"><span class="linenos">380</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased.get_rows-381"><a href="#DataBased.get_rows-381"><span class="linenos">381</span></a>
+</span><span id="DataBased.get_rows-382"><a href="#DataBased.get_rows-382"><span class="linenos">382</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns_to_return</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-383"><a href="#DataBased.get_rows-383"><span class="linenos">383</span></a>            <span class="n">columns_to_return</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns_to_return</span><span class="p">]</span>
+</span><span id="DataBased.get_rows-384"><a href="#DataBased.get_rows-384"><span class="linenos">384</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;select * from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">]&quot;</span>
+</span><span id="DataBased.get_rows-385"><a href="#DataBased.get_rows-385"><span class="linenos">385</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="DataBased.get_rows-386"><a href="#DataBased.get_rows-386"><span class="linenos">386</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-387"><a href="#DataBased.get_rows-387"><span class="linenos">387</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased.get_rows-388"><a href="#DataBased.get_rows-388"><span class="linenos">388</span></a>        <span class="k">if</span> <span class="n">order_by</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-389"><a href="#DataBased.get_rows-389"><span class="linenos">389</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; order by </span><span class="si">{</span><span class="n">order_by</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased.get_rows-390"><a href="#DataBased.get_rows-390"><span class="linenos">390</span></a>        <span class="k">if</span> <span class="n">limit</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-391"><a href="#DataBased.get_rows-391"><span class="linenos">391</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; limit </span><span class="si">{</span><span class="n">limit</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased.get_rows-392"><a href="#DataBased.get_rows-392"><span class="linenos">392</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="DataBased.get_rows-393"><a href="#DataBased.get_rows-393"><span class="linenos">393</span></a>        <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="n">query</span><span class="p">)</span>
+</span><span id="DataBased.get_rows-394"><a href="#DataBased.get_rows-394"><span class="linenos">394</span></a>        <span class="n">matches</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">fetchall</span><span class="p">()</span>
+</span><span id="DataBased.get_rows-395"><a href="#DataBased.get_rows-395"><span class="linenos">395</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[</span><span class="bp">self</span><span class="o">.</span><span class="n">_get_dict</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">match</span><span class="p">,</span> <span class="n">columns_to_return</span><span class="p">)</span> <span class="k">for</span> <span class="n">match</span> <span class="ow">in</span> <span class="n">matches</span><span class="p">]</span>
+</span><span id="DataBased.get_rows-396"><a href="#DataBased.get_rows-396"><span class="linenos">396</span></a>        <span class="k">if</span> <span class="n">sort_by_column</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-397"><a href="#DataBased.get_rows-397"><span class="linenos">397</span></a>            <span class="n">results</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">results</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="p">[</span><span class="n">sort_by_column</span><span class="p">])</span>
+</span><span id="DataBased.get_rows-398"><a href="#DataBased.get_rows-398"><span class="linenos">398</span></a>        <span class="k">if</span> <span class="n">return_as_dataframe</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-399"><a href="#DataBased.get_rows-399"><span class="linenos">399</span></a>            <span class="k">return</span> <span class="n">pandas</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">results</span><span class="p">)</span>
+</span><span id="DataBased.get_rows-400"><a href="#DataBased.get_rows-400"><span class="linenos">400</span></a>        <span class="k">if</span> <span class="n">values_only</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-401"><a href="#DataBased.get_rows-401"><span class="linenos">401</span></a>            <span class="k">return</span> <span class="p">[</span><span class="nb">tuple</span><span class="p">(</span><span class="n">row</span><span class="o">.</span><span class="n">values</span><span class="p">())</span> <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="n">results</span><span class="p">]</span>
+</span><span id="DataBased.get_rows-402"><a href="#DataBased.get_rows-402"><span class="linenos">402</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.get_rows-403"><a href="#DataBased.get_rows-403"><span class="linenos">403</span></a>            <span class="k">return</span> <span class="n">results</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Return matching rows from <code>table</code>.</p>
 
 <p>By default, rows will be returned as a list of dictionaries of the form <code>[{"column_name": value, ...}, ...]</code></p>
 
@@ -1896,45 +1859,45 @@
         <span class="def">def</span>
         <span class="name">find</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span></span><span class="return-annotation">) -> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.find-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.find"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.find-404"><a href="#DataBased.find-404"><span class="linenos">404</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.find-405"><a href="#DataBased.find-405"><span class="linenos">405</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
-</span><span id="DataBased.find-406"><a href="#DataBased.find-406"><span class="linenos">406</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased.find-407"><a href="#DataBased.find-407"><span class="linenos">407</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
-</span><span id="DataBased.find-408"><a href="#DataBased.find-408"><span class="linenos">408</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
-</span><span id="DataBased.find-409"><a href="#DataBased.find-409"><span class="linenos">409</span></a>
-</span><span id="DataBased.find-410"><a href="#DataBased.find-410"><span class="linenos">410</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.find-411"><a href="#DataBased.find-411"><span class="linenos">411</span></a>
-</span><span id="DataBased.find-412"><a href="#DataBased.find-412"><span class="linenos">412</span></a><span class="sd">        `table`: The table to search.</span>
-</span><span id="DataBased.find-413"><a href="#DataBased.find-413"><span class="linenos">413</span></a>
-</span><span id="DataBased.find-414"><a href="#DataBased.find-414"><span class="linenos">414</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
-</span><span id="DataBased.find-415"><a href="#DataBased.find-415"><span class="linenos">415</span></a>
-</span><span id="DataBased.find-416"><a href="#DataBased.find-416"><span class="linenos">416</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
-</span><span id="DataBased.find-417"><a href="#DataBased.find-417"><span class="linenos">417</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
-</span><span id="DataBased.find-418"><a href="#DataBased.find-418"><span class="linenos">418</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased.find-419"><a href="#DataBased.find-419"><span class="linenos">419</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased.find-420"><a href="#DataBased.find-420"><span class="linenos">420</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
-</span><span id="DataBased.find-421"><a href="#DataBased.find-421"><span class="linenos">421</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
-</span><span id="DataBased.find-422"><a href="#DataBased.find-422"><span class="linenos">422</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased.find-423"><a href="#DataBased.find-423"><span class="linenos">423</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
-</span><span id="DataBased.find-424"><a href="#DataBased.find-424"><span class="linenos">424</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
-</span><span id="DataBased.find-425"><a href="#DataBased.find-425"><span class="linenos">425</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
-</span><span id="DataBased.find-426"><a href="#DataBased.find-426"><span class="linenos">426</span></a>                <span class="p">[</span>
-</span><span id="DataBased.find-427"><a href="#DataBased.find-427"><span class="linenos">427</span></a>                    <span class="n">row</span>
-</span><span id="DataBased.find-428"><a href="#DataBased.find-428"><span class="linenos">428</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
-</span><span id="DataBased.find-429"><a href="#DataBased.find-429"><span class="linenos">429</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
-</span><span id="DataBased.find-430"><a href="#DataBased.find-430"><span class="linenos">430</span></a>                    <span class="p">)</span>
-</span><span id="DataBased.find-431"><a href="#DataBased.find-431"><span class="linenos">431</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
-</span><span id="DataBased.find-432"><a href="#DataBased.find-432"><span class="linenos">432</span></a>                <span class="p">]</span>
-</span><span id="DataBased.find-433"><a href="#DataBased.find-433"><span class="linenos">433</span></a>            <span class="p">)</span>
-</span><span id="DataBased.find-434"><a href="#DataBased.find-434"><span class="linenos">434</span></a>        <span class="k">return</span> <span class="n">results</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.find-405"><a href="#DataBased.find-405"><span class="linenos">405</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.find-406"><a href="#DataBased.find-406"><span class="linenos">406</span></a>    <span class="k">def</span> <span class="nf">find</span><span class="p">(</span>
+</span><span id="DataBased.find-407"><a href="#DataBased.find-407"><span class="linenos">407</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">query_string</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">columns</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased.find-408"><a href="#DataBased.find-408"><span class="linenos">408</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]:</span>
+</span><span id="DataBased.find-409"><a href="#DataBased.find-409"><span class="linenos">409</span></a>        <span class="sd">&quot;&quot;&quot;Search for rows that contain `query_string` as a substring of any column.</span>
+</span><span id="DataBased.find-410"><a href="#DataBased.find-410"><span class="linenos">410</span></a>
+</span><span id="DataBased.find-411"><a href="#DataBased.find-411"><span class="linenos">411</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.find-412"><a href="#DataBased.find-412"><span class="linenos">412</span></a>
+</span><span id="DataBased.find-413"><a href="#DataBased.find-413"><span class="linenos">413</span></a><span class="sd">        `table`: The table to search.</span>
+</span><span id="DataBased.find-414"><a href="#DataBased.find-414"><span class="linenos">414</span></a>
+</span><span id="DataBased.find-415"><a href="#DataBased.find-415"><span class="linenos">415</span></a><span class="sd">        `query_string`: The substring to search for in all columns.</span>
+</span><span id="DataBased.find-416"><a href="#DataBased.find-416"><span class="linenos">416</span></a>
+</span><span id="DataBased.find-417"><a href="#DataBased.find-417"><span class="linenos">417</span></a><span class="sd">        `columns`: A list of columns to search for query_string.</span>
+</span><span id="DataBased.find-418"><a href="#DataBased.find-418"><span class="linenos">418</span></a><span class="sd">        If None, all columns in the table will be searched.</span>
+</span><span id="DataBased.find-419"><a href="#DataBased.find-419"><span class="linenos">419</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased.find-420"><a href="#DataBased.find-420"><span class="linenos">420</span></a>        <span class="k">if</span> <span class="nb">type</span><span class="p">(</span><span class="n">columns</span><span class="p">)</span> <span class="ow">is</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased.find-421"><a href="#DataBased.find-421"><span class="linenos">421</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="p">[</span><span class="n">columns</span><span class="p">]</span>
+</span><span id="DataBased.find-422"><a href="#DataBased.find-422"><span class="linenos">422</span></a>        <span class="n">results</span> <span class="o">=</span> <span class="p">[]</span>
+</span><span id="DataBased.find-423"><a href="#DataBased.find-423"><span class="linenos">423</span></a>        <span class="k">if</span> <span class="ow">not</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased.find-424"><a href="#DataBased.find-424"><span class="linenos">424</span></a>            <span class="n">columns</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_column_names</span><span class="p">(</span><span class="n">table</span><span class="p">)</span>
+</span><span id="DataBased.find-425"><a href="#DataBased.find-425"><span class="linenos">425</span></a>        <span class="k">for</span> <span class="n">column</span> <span class="ow">in</span> <span class="n">columns</span><span class="p">:</span>
+</span><span id="DataBased.find-426"><a href="#DataBased.find-426"><span class="linenos">426</span></a>            <span class="n">results</span><span class="o">.</span><span class="n">extend</span><span class="p">(</span>
+</span><span id="DataBased.find-427"><a href="#DataBased.find-427"><span class="linenos">427</span></a>                <span class="p">[</span>
+</span><span id="DataBased.find-428"><a href="#DataBased.find-428"><span class="linenos">428</span></a>                    <span class="n">row</span>
+</span><span id="DataBased.find-429"><a href="#DataBased.find-429"><span class="linenos">429</span></a>                    <span class="k">for</span> <span class="n">row</span> <span class="ow">in</span> <span class="bp">self</span><span class="o">.</span><span class="n">get_rows</span><span class="p">(</span>
+</span><span id="DataBased.find-430"><a href="#DataBased.find-430"><span class="linenos">430</span></a>                        <span class="n">table</span><span class="p">,</span> <span class="p">[(</span><span class="n">column</span><span class="p">,</span> <span class="n">query_string</span><span class="p">)],</span> <span class="n">exact_match</span><span class="o">=</span><span class="kc">False</span>
+</span><span id="DataBased.find-431"><a href="#DataBased.find-431"><span class="linenos">431</span></a>                    <span class="p">)</span>
+</span><span id="DataBased.find-432"><a href="#DataBased.find-432"><span class="linenos">432</span></a>                    <span class="k">if</span> <span class="n">row</span> <span class="ow">not</span> <span class="ow">in</span> <span class="n">results</span>
+</span><span id="DataBased.find-433"><a href="#DataBased.find-433"><span class="linenos">433</span></a>                <span class="p">]</span>
+</span><span id="DataBased.find-434"><a href="#DataBased.find-434"><span class="linenos">434</span></a>            <span class="p">)</span>
+</span><span id="DataBased.find-435"><a href="#DataBased.find-435"><span class="linenos">435</span></a>        <span class="k">return</span> <span class="n">results</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Search for rows that contain <code>query_string</code> as a substring of any column.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -1955,42 +1918,42 @@
         <span class="def">def</span>
         <span class="name">delete</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span>,</span><span class="param">	<span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">int</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.delete-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.delete"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.delete-436"><a href="#DataBased.delete-436"><span class="linenos">436</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.delete-437"><a href="#DataBased.delete-437"><span class="linenos">437</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
-</span><span id="DataBased.delete-438"><a href="#DataBased.delete-438"><span class="linenos">438</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased.delete-439"><a href="#DataBased.delete-439"><span class="linenos">439</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased.delete-440"><a href="#DataBased.delete-440"><span class="linenos">440</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
-</span><span id="DataBased.delete-441"><a href="#DataBased.delete-441"><span class="linenos">441</span></a>
-</span><span id="DataBased.delete-442"><a href="#DataBased.delete-442"><span class="linenos">442</span></a><span class="sd">        Returns the number of deleted records.</span>
-</span><span id="DataBased.delete-443"><a href="#DataBased.delete-443"><span class="linenos">443</span></a>
-</span><span id="DataBased.delete-444"><a href="#DataBased.delete-444"><span class="linenos">444</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.delete-445"><a href="#DataBased.delete-445"><span class="linenos">445</span></a>
-</span><span id="DataBased.delete-446"><a href="#DataBased.delete-446"><span class="linenos">446</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
-</span><span id="DataBased.delete-447"><a href="#DataBased.delete-447"><span class="linenos">447</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="DataBased.delete-448"><a href="#DataBased.delete-448"><span class="linenos">448</span></a>
-</span><span id="DataBased.delete-449"><a href="#DataBased.delete-449"><span class="linenos">449</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
-</span><span id="DataBased.delete-450"><a href="#DataBased.delete-450"><span class="linenos">450</span></a><span class="sd">        &quot;&quot;&quot;</span>
-</span><span id="DataBased.delete-451"><a href="#DataBased.delete-451"><span class="linenos">451</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="DataBased.delete-452"><a href="#DataBased.delete-452"><span class="linenos">452</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.delete-453"><a href="#DataBased.delete-453"><span class="linenos">453</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
-</span><span id="DataBased.delete-454"><a href="#DataBased.delete-454"><span class="linenos">454</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="DataBased.delete-455"><a href="#DataBased.delete-455"><span class="linenos">455</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="DataBased.delete-456"><a href="#DataBased.delete-456"><span class="linenos">456</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
-</span><span id="DataBased.delete-457"><a href="#DataBased.delete-457"><span class="linenos">457</span></a>            <span class="p">)</span>
-</span><span id="DataBased.delete-458"><a href="#DataBased.delete-458"><span class="linenos">458</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
-</span><span id="DataBased.delete-459"><a href="#DataBased.delete-459"><span class="linenos">459</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased.delete-460"><a href="#DataBased.delete-460"><span class="linenos">460</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
-</span><span id="DataBased.delete-461"><a href="#DataBased.delete-461"><span class="linenos">461</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased.delete-462"><a href="#DataBased.delete-462"><span class="linenos">462</span></a>            <span class="p">)</span>
-</span><span id="DataBased.delete-463"><a href="#DataBased.delete-463"><span class="linenos">463</span></a>            <span class="k">return</span> <span class="mi">0</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.delete-437"><a href="#DataBased.delete-437"><span class="linenos">437</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.delete-438"><a href="#DataBased.delete-438"><span class="linenos">438</span></a>    <span class="k">def</span> <span class="nf">delete</span><span class="p">(</span>
+</span><span id="DataBased.delete-439"><a href="#DataBased.delete-439"><span class="linenos">439</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased.delete-440"><a href="#DataBased.delete-440"><span class="linenos">440</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased.delete-441"><a href="#DataBased.delete-441"><span class="linenos">441</span></a>        <span class="sd">&quot;&quot;&quot;Delete records from `table`.</span>
+</span><span id="DataBased.delete-442"><a href="#DataBased.delete-442"><span class="linenos">442</span></a>
+</span><span id="DataBased.delete-443"><a href="#DataBased.delete-443"><span class="linenos">443</span></a><span class="sd">        Returns the number of deleted records.</span>
+</span><span id="DataBased.delete-444"><a href="#DataBased.delete-444"><span class="linenos">444</span></a>
+</span><span id="DataBased.delete-445"><a href="#DataBased.delete-445"><span class="linenos">445</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.delete-446"><a href="#DataBased.delete-446"><span class="linenos">446</span></a>
+</span><span id="DataBased.delete-447"><a href="#DataBased.delete-447"><span class="linenos">447</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(column_name, value)`</span>
+</span><span id="DataBased.delete-448"><a href="#DataBased.delete-448"><span class="linenos">448</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="DataBased.delete-449"><a href="#DataBased.delete-449"><span class="linenos">449</span></a>
+</span><span id="DataBased.delete-450"><a href="#DataBased.delete-450"><span class="linenos">450</span></a><span class="sd">        `exact_match`: If `False`, the value for a given column will be matched as a substring.</span>
+</span><span id="DataBased.delete-451"><a href="#DataBased.delete-451"><span class="linenos">451</span></a><span class="sd">        &quot;&quot;&quot;</span>
+</span><span id="DataBased.delete-452"><a href="#DataBased.delete-452"><span class="linenos">452</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="DataBased.delete-453"><a href="#DataBased.delete-453"><span class="linenos">453</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.delete-454"><a href="#DataBased.delete-454"><span class="linenos">454</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;delete from [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">;&quot;</span><span class="p">)</span>
+</span><span id="DataBased.delete-455"><a href="#DataBased.delete-455"><span class="linenos">455</span></a>            <span class="n">num_deletions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="DataBased.delete-456"><a href="#DataBased.delete-456"><span class="linenos">456</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="DataBased.delete-457"><a href="#DataBased.delete-457"><span class="linenos">457</span></a>                <span class="sa">f</span><span class="s1">&#39;Deleted </span><span class="si">{</span><span class="n">num_deletions</span><span class="si">}</span><span class="s1"> rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;.&#39;</span>
+</span><span id="DataBased.delete-458"><a href="#DataBased.delete-458"><span class="linenos">458</span></a>            <span class="p">)</span>
+</span><span id="DataBased.delete-459"><a href="#DataBased.delete-459"><span class="linenos">459</span></a>            <span class="k">return</span> <span class="n">num_deletions</span>
+</span><span id="DataBased.delete-460"><a href="#DataBased.delete-460"><span class="linenos">460</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased.delete-461"><a href="#DataBased.delete-461"><span class="linenos">461</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">debug</span><span class="p">(</span>
+</span><span id="DataBased.delete-462"><a href="#DataBased.delete-462"><span class="linenos">462</span></a>                <span class="sa">f</span><span class="s1">&#39;Error deleting rows from &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">.</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased.delete-463"><a href="#DataBased.delete-463"><span class="linenos">463</span></a>            <span class="p">)</span>
+</span><span id="DataBased.delete-464"><a href="#DataBased.delete-464"><span class="linenos">464</span></a>            <span class="k">return</span> <span class="mi">0</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Delete records from <code>table</code>.</p>
 
 <p>Returns the number of deleted records.</p>
 
@@ -2011,63 +1974,63 @@
         <span class="def">def</span>
         <span class="name">update</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span>,</span><span class="param">	<span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">int</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.update-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.update"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.update-465"><a href="#DataBased.update-465"><span class="linenos">465</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.update-466"><a href="#DataBased.update-466"><span class="linenos">466</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
-</span><span id="DataBased.update-467"><a href="#DataBased.update-467"><span class="linenos">467</span></a>        <span class="bp">self</span><span class="p">,</span>
-</span><span id="DataBased.update-468"><a href="#DataBased.update-468"><span class="linenos">468</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased.update-469"><a href="#DataBased.update-469"><span class="linenos">469</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
-</span><span id="DataBased.update-470"><a href="#DataBased.update-470"><span class="linenos">470</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
-</span><span id="DataBased.update-471"><a href="#DataBased.update-471"><span class="linenos">471</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
-</span><span id="DataBased.update-472"><a href="#DataBased.update-472"><span class="linenos">472</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
-</span><span id="DataBased.update-473"><a href="#DataBased.update-473"><span class="linenos">473</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
-</span><span id="DataBased.update-474"><a href="#DataBased.update-474"><span class="linenos">474</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
-</span><span id="DataBased.update-475"><a href="#DataBased.update-475"><span class="linenos">475</span></a>
-</span><span id="DataBased.update-476"><a href="#DataBased.update-476"><span class="linenos">476</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.update-477"><a href="#DataBased.update-477"><span class="linenos">477</span></a>
-</span><span id="DataBased.update-478"><a href="#DataBased.update-478"><span class="linenos">478</span></a><span class="sd">        `table`: The table to update rows in.</span>
-</span><span id="DataBased.update-479"><a href="#DataBased.update-479"><span class="linenos">479</span></a>
-</span><span id="DataBased.update-480"><a href="#DataBased.update-480"><span class="linenos">480</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
-</span><span id="DataBased.update-481"><a href="#DataBased.update-481"><span class="linenos">481</span></a>
-</span><span id="DataBased.update-482"><a href="#DataBased.update-482"><span class="linenos">482</span></a><span class="sd">        `new_value`: The new value to insert.</span>
-</span><span id="DataBased.update-483"><a href="#DataBased.update-483"><span class="linenos">483</span></a>
-</span><span id="DataBased.update-484"><a href="#DataBased.update-484"><span class="linenos">484</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
-</span><span id="DataBased.update-485"><a href="#DataBased.update-485"><span class="linenos">485</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
-</span><span id="DataBased.update-486"><a href="#DataBased.update-486"><span class="linenos">486</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
-</span><span id="DataBased.update-487"><a href="#DataBased.update-487"><span class="linenos">487</span></a>
-</span><span id="DataBased.update-488"><a href="#DataBased.update-488"><span class="linenos">488</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
-</span><span id="DataBased.update-489"><a href="#DataBased.update-489"><span class="linenos">489</span></a>
-</span><span id="DataBased.update-490"><a href="#DataBased.update-490"><span class="linenos">490</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
-</span><span id="DataBased.update-491"><a href="#DataBased.update-491"><span class="linenos">491</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
-</span><span id="DataBased.update-492"><a href="#DataBased.update-492"><span class="linenos">492</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
-</span><span id="DataBased.update-493"><a href="#DataBased.update-493"><span class="linenos">493</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
-</span><span id="DataBased.update-494"><a href="#DataBased.update-494"><span class="linenos">494</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
-</span><span id="DataBased.update-495"><a href="#DataBased.update-495"><span class="linenos">495</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
-</span><span id="DataBased.update-496"><a href="#DataBased.update-496"><span class="linenos">496</span></a>        <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.update-497"><a href="#DataBased.update-497"><span class="linenos">497</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased.update-498"><a href="#DataBased.update-498"><span class="linenos">498</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
-</span><span id="DataBased.update-499"><a href="#DataBased.update-499"><span class="linenos">499</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.update-500"><a href="#DataBased.update-500"><span class="linenos">500</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.update-501"><a href="#DataBased.update-501"><span class="linenos">501</span></a>                <span class="n">query</span><span class="p">,</span>
-</span><span id="DataBased.update-502"><a href="#DataBased.update-502"><span class="linenos">502</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
-</span><span id="DataBased.update-503"><a href="#DataBased.update-503"><span class="linenos">503</span></a>            <span class="p">)</span>
-</span><span id="DataBased.update-504"><a href="#DataBased.update-504"><span class="linenos">504</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
-</span><span id="DataBased.update-505"><a href="#DataBased.update-505"><span class="linenos">505</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
-</span><span id="DataBased.update-506"><a href="#DataBased.update-506"><span class="linenos">506</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased.update-507"><a href="#DataBased.update-507"><span class="linenos">507</span></a>            <span class="p">)</span>
-</span><span id="DataBased.update-508"><a href="#DataBased.update-508"><span class="linenos">508</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
-</span><span id="DataBased.update-509"><a href="#DataBased.update-509"><span class="linenos">509</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased.update-510"><a href="#DataBased.update-510"><span class="linenos">510</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
-</span><span id="DataBased.update-511"><a href="#DataBased.update-511"><span class="linenos">511</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
-</span><span id="DataBased.update-512"><a href="#DataBased.update-512"><span class="linenos">512</span></a>            <span class="p">)</span>
-</span><span id="DataBased.update-513"><a href="#DataBased.update-513"><span class="linenos">513</span></a>            <span class="k">return</span> <span class="mi">0</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.update-466"><a href="#DataBased.update-466"><span class="linenos">466</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.update-467"><a href="#DataBased.update-467"><span class="linenos">467</span></a>    <span class="k">def</span> <span class="nf">update</span><span class="p">(</span>
+</span><span id="DataBased.update-468"><a href="#DataBased.update-468"><span class="linenos">468</span></a>        <span class="bp">self</span><span class="p">,</span>
+</span><span id="DataBased.update-469"><a href="#DataBased.update-469"><span class="linenos">469</span></a>        <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased.update-470"><a href="#DataBased.update-470"><span class="linenos">470</span></a>        <span class="n">column_to_update</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span>
+</span><span id="DataBased.update-471"><a href="#DataBased.update-471"><span class="linenos">471</span></a>        <span class="n">new_value</span><span class="p">:</span> <span class="n">Any</span><span class="p">,</span>
+</span><span id="DataBased.update-472"><a href="#DataBased.update-472"><span class="linenos">472</span></a>        <span class="n">match_criteria</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">tuple</span><span class="p">]</span> <span class="o">|</span> <span class="nb">dict</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span>
+</span><span id="DataBased.update-473"><a href="#DataBased.update-473"><span class="linenos">473</span></a>        <span class="n">exact_match</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
+</span><span id="DataBased.update-474"><a href="#DataBased.update-474"><span class="linenos">474</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">int</span><span class="p">:</span>
+</span><span id="DataBased.update-475"><a href="#DataBased.update-475"><span class="linenos">475</span></a>        <span class="sd">&quot;&quot;&quot;Update the value in `column_to_update` to `new_value` for rows matched with `match_criteria`.</span>
+</span><span id="DataBased.update-476"><a href="#DataBased.update-476"><span class="linenos">476</span></a>
+</span><span id="DataBased.update-477"><a href="#DataBased.update-477"><span class="linenos">477</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.update-478"><a href="#DataBased.update-478"><span class="linenos">478</span></a>
+</span><span id="DataBased.update-479"><a href="#DataBased.update-479"><span class="linenos">479</span></a><span class="sd">        `table`: The table to update rows in.</span>
+</span><span id="DataBased.update-480"><a href="#DataBased.update-480"><span class="linenos">480</span></a>
+</span><span id="DataBased.update-481"><a href="#DataBased.update-481"><span class="linenos">481</span></a><span class="sd">        `column_to_update`: The column to be updated in the matched rows.</span>
+</span><span id="DataBased.update-482"><a href="#DataBased.update-482"><span class="linenos">482</span></a>
+</span><span id="DataBased.update-483"><a href="#DataBased.update-483"><span class="linenos">483</span></a><span class="sd">        `new_value`: The new value to insert.</span>
+</span><span id="DataBased.update-484"><a href="#DataBased.update-484"><span class="linenos">484</span></a>
+</span><span id="DataBased.update-485"><a href="#DataBased.update-485"><span class="linenos">485</span></a><span class="sd">        `match_criteria`: Can be a list of 2-tuples where each tuple is `(columnName, rowValue)`</span>
+</span><span id="DataBased.update-486"><a href="#DataBased.update-486"><span class="linenos">486</span></a><span class="sd">        or a dictionary where keys are column names and values are corresponding values.</span>
+</span><span id="DataBased.update-487"><a href="#DataBased.update-487"><span class="linenos">487</span></a><span class="sd">        If `None`, every row in `table` will be updated.</span>
+</span><span id="DataBased.update-488"><a href="#DataBased.update-488"><span class="linenos">488</span></a>
+</span><span id="DataBased.update-489"><a href="#DataBased.update-489"><span class="linenos">489</span></a><span class="sd">        `exact_match`: If `False`, `match_criteria` values will be treated as substrings.</span>
+</span><span id="DataBased.update-490"><a href="#DataBased.update-490"><span class="linenos">490</span></a>
+</span><span id="DataBased.update-491"><a href="#DataBased.update-491"><span class="linenos">491</span></a><span class="sd">        Returns the number of updated rows.&quot;&quot;&quot;</span>
+</span><span id="DataBased.update-492"><a href="#DataBased.update-492"><span class="linenos">492</span></a>        <span class="n">query</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">&quot;update [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] set </span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s2"> = ?&quot;</span>
+</span><span id="DataBased.update-493"><a href="#DataBased.update-493"><span class="linenos">493</span></a>        <span class="n">conditions</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span>
+</span><span id="DataBased.update-494"><a href="#DataBased.update-494"><span class="linenos">494</span></a>        <span class="k">if</span> <span class="n">match_criteria</span><span class="p">:</span>
+</span><span id="DataBased.update-495"><a href="#DataBased.update-495"><span class="linenos">495</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">_get_conditions</span><span class="p">(</span><span class="n">match_criteria</span><span class="p">,</span> <span class="n">exact_match</span><span class="p">)</span>
+</span><span id="DataBased.update-496"><a href="#DataBased.update-496"><span class="linenos">496</span></a>            <span class="n">query</span> <span class="o">+=</span> <span class="sa">f</span><span class="s2">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s2">&quot;</span>
+</span><span id="DataBased.update-497"><a href="#DataBased.update-497"><span class="linenos">497</span></a>        <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.update-498"><a href="#DataBased.update-498"><span class="linenos">498</span></a>            <span class="n">conditions</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased.update-499"><a href="#DataBased.update-499"><span class="linenos">499</span></a>        <span class="n">query</span> <span class="o">+=</span> <span class="s2">&quot;;&quot;</span>
+</span><span id="DataBased.update-500"><a href="#DataBased.update-500"><span class="linenos">500</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.update-501"><a href="#DataBased.update-501"><span class="linenos">501</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.update-502"><a href="#DataBased.update-502"><span class="linenos">502</span></a>                <span class="n">query</span><span class="p">,</span>
+</span><span id="DataBased.update-503"><a href="#DataBased.update-503"><span class="linenos">503</span></a>                <span class="p">(</span><span class="n">new_value</span><span class="p">,),</span>
+</span><span id="DataBased.update-504"><a href="#DataBased.update-504"><span class="linenos">504</span></a>            <span class="p">)</span>
+</span><span id="DataBased.update-505"><a href="#DataBased.update-505"><span class="linenos">505</span></a>            <span class="n">num_updates</span> <span class="o">=</span> <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">rowcount</span>
+</span><span id="DataBased.update-506"><a href="#DataBased.update-506"><span class="linenos">506</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span>
+</span><span id="DataBased.update-507"><a href="#DataBased.update-507"><span class="linenos">507</span></a>                <span class="sa">f</span><span class="s1">&#39;In </span><span class="si">{</span><span class="n">num_updates</span><span class="si">}</span><span class="s1"> rows, updated &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased.update-508"><a href="#DataBased.update-508"><span class="linenos">508</span></a>            <span class="p">)</span>
+</span><span id="DataBased.update-509"><a href="#DataBased.update-509"><span class="linenos">509</span></a>            <span class="k">return</span> <span class="n">num_updates</span>
+</span><span id="DataBased.update-510"><a href="#DataBased.update-510"><span class="linenos">510</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased.update-511"><a href="#DataBased.update-511"><span class="linenos">511</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span>
+</span><span id="DataBased.update-512"><a href="#DataBased.update-512"><span class="linenos">512</span></a>                <span class="sa">f</span><span class="s1">&#39;Failed to update &quot;</span><span class="si">{</span><span class="n">column_to_update</span><span class="si">}</span><span class="s1">&quot; in &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table to &quot;</span><span class="si">{</span><span class="n">new_value</span><span class="si">}</span><span class="s1">&quot; where </span><span class="si">{</span><span class="n">conditions</span><span class="si">}</span><span class="s1">&quot;</span><span class="se">\n</span><span class="si">{</span><span class="n">e</span><span class="si">}</span><span class="s1">&#39;</span>
+</span><span id="DataBased.update-513"><a href="#DataBased.update-513"><span class="linenos">513</span></a>            <span class="p">)</span>
+</span><span id="DataBased.update-514"><a href="#DataBased.update-514"><span class="linenos">514</span></a>            <span class="k">return</span> <span class="mi">0</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Update the value in <code>column_to_update</code> to <code>new_value</code> for rows matched with <code>match_criteria</code>.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -2095,27 +2058,27 @@
         <span class="def">def</span>
         <span class="name">drop_table</span><span class="signature pdoc-code condensed">(<span class="param"><span class="bp">self</span>, </span><span class="param"><span class="n">table</span><span class="p">:</span> <span class="nb">str</span></span><span class="return-annotation">) -> <span class="nb">bool</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.drop_table-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.drop_table"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.drop_table-515"><a href="#DataBased.drop_table-515"><span class="linenos">515</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.drop_table-516"><a href="#DataBased.drop_table-516"><span class="linenos">516</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
-</span><span id="DataBased.drop_table-517"><a href="#DataBased.drop_table-517"><span class="linenos">517</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
-</span><span id="DataBased.drop_table-518"><a href="#DataBased.drop_table-518"><span class="linenos">518</span></a>
-</span><span id="DataBased.drop_table-519"><a href="#DataBased.drop_table-519"><span class="linenos">519</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
-</span><span id="DataBased.drop_table-520"><a href="#DataBased.drop_table-520"><span class="linenos">520</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.drop_table-521"><a href="#DataBased.drop_table-521"><span class="linenos">521</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
-</span><span id="DataBased.drop_table-522"><a href="#DataBased.drop_table-522"><span class="linenos">522</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="DataBased.drop_table-523"><a href="#DataBased.drop_table-523"><span class="linenos">523</span></a>            <span class="k">return</span> <span class="kc">True</span>
-</span><span id="DataBased.drop_table-524"><a href="#DataBased.drop_table-524"><span class="linenos">524</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased.drop_table-525"><a href="#DataBased.drop_table-525"><span class="linenos">525</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
-</span><span id="DataBased.drop_table-526"><a href="#DataBased.drop_table-526"><span class="linenos">526</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
-</span><span id="DataBased.drop_table-527"><a href="#DataBased.drop_table-527"><span class="linenos">527</span></a>            <span class="k">return</span> <span class="kc">False</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.drop_table-516"><a href="#DataBased.drop_table-516"><span class="linenos">516</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.drop_table-517"><a href="#DataBased.drop_table-517"><span class="linenos">517</span></a>    <span class="k">def</span> <span class="nf">drop_table</span><span class="p">(</span><span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">bool</span><span class="p">:</span>
+</span><span id="DataBased.drop_table-518"><a href="#DataBased.drop_table-518"><span class="linenos">518</span></a>        <span class="sd">&quot;&quot;&quot;Drop `table` from the database.</span>
+</span><span id="DataBased.drop_table-519"><a href="#DataBased.drop_table-519"><span class="linenos">519</span></a>
+</span><span id="DataBased.drop_table-520"><a href="#DataBased.drop_table-520"><span class="linenos">520</span></a><span class="sd">        Returns `True` if successful, `False` if not.&quot;&quot;&quot;</span>
+</span><span id="DataBased.drop_table-521"><a href="#DataBased.drop_table-521"><span class="linenos">521</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.drop_table-522"><a href="#DataBased.drop_table-522"><span class="linenos">522</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;drop Table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">];&quot;</span><span class="p">)</span>
+</span><span id="DataBased.drop_table-523"><a href="#DataBased.drop_table-523"><span class="linenos">523</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Dropped table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="DataBased.drop_table-524"><a href="#DataBased.drop_table-524"><span class="linenos">524</span></a>            <span class="k">return</span> <span class="kc">True</span>
+</span><span id="DataBased.drop_table-525"><a href="#DataBased.drop_table-525"><span class="linenos">525</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased.drop_table-526"><a href="#DataBased.drop_table-526"><span class="linenos">526</span></a>            <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
+</span><span id="DataBased.drop_table-527"><a href="#DataBased.drop_table-527"><span class="linenos">527</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to drop table &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot;&#39;</span><span class="p">)</span>
+</span><span id="DataBased.drop_table-528"><a href="#DataBased.drop_table-528"><span class="linenos">528</span></a>            <span class="k">return</span> <span class="kc">False</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Drop <code>table</code> from the database.</p>
 
 <p>Returns <code>True</code> if successful, <code>False</code> if not.</p>
 </div>
@@ -2129,40 +2092,40 @@
         <span class="def">def</span>
         <span class="name">add_column</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="bp">self</span>,</span><span class="param">	<span class="n">table</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">column</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">_type</span><span class="p">:</span> <span class="nb">str</span>,</span><span class="param">	<span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span></span><span class="return-annotation">):</span></span>
 
                 <label class="view-source-button" for="DataBased.add_column-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.add_column"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_column-529"><a href="#DataBased.add_column-529"><span class="linenos">529</span></a>    <span class="nd">@_connect</span>
-</span><span id="DataBased.add_column-530"><a href="#DataBased.add_column-530"><span class="linenos">530</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
-</span><span id="DataBased.add_column-531"><a href="#DataBased.add_column-531"><span class="linenos">531</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
-</span><span id="DataBased.add_column-532"><a href="#DataBased.add_column-532"><span class="linenos">532</span></a>    <span class="p">):</span>
-</span><span id="DataBased.add_column-533"><a href="#DataBased.add_column-533"><span class="linenos">533</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
-</span><span id="DataBased.add_column-534"><a href="#DataBased.add_column-534"><span class="linenos">534</span></a>
-</span><span id="DataBased.add_column-535"><a href="#DataBased.add_column-535"><span class="linenos">535</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.add_column-536"><a href="#DataBased.add_column-536"><span class="linenos">536</span></a>
-</span><span id="DataBased.add_column-537"><a href="#DataBased.add_column-537"><span class="linenos">537</span></a><span class="sd">        `column`: Name of the column to add.</span>
-</span><span id="DataBased.add_column-538"><a href="#DataBased.add_column-538"><span class="linenos">538</span></a>
-</span><span id="DataBased.add_column-539"><a href="#DataBased.add_column-539"><span class="linenos">539</span></a><span class="sd">        `_type`: The data type of the new column.</span>
-</span><span id="DataBased.add_column-540"><a href="#DataBased.add_column-540"><span class="linenos">540</span></a>
-</span><span id="DataBased.add_column-541"><a href="#DataBased.add_column-541"><span class="linenos">541</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
-</span><span id="DataBased.add_column-542"><a href="#DataBased.add_column-542"><span class="linenos">542</span></a>        <span class="k">try</span><span class="p">:</span>
-</span><span id="DataBased.add_column-543"><a href="#DataBased.add_column-543"><span class="linenos">543</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
-</span><span id="DataBased.add_column-544"><a href="#DataBased.add_column-544"><span class="linenos">544</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.add_column-545"><a href="#DataBased.add_column-545"><span class="linenos">545</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased.add_column-546"><a href="#DataBased.add_column-546"><span class="linenos">546</span></a>                <span class="p">)</span>
-</span><span id="DataBased.add_column-547"><a href="#DataBased.add_column-547"><span class="linenos">547</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
-</span><span id="DataBased.add_column-548"><a href="#DataBased.add_column-548"><span class="linenos">548</span></a>            <span class="k">else</span><span class="p">:</span>
-</span><span id="DataBased.add_column-549"><a href="#DataBased.add_column-549"><span class="linenos">549</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
-</span><span id="DataBased.add_column-550"><a href="#DataBased.add_column-550"><span class="linenos">550</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
-</span><span id="DataBased.add_column-551"><a href="#DataBased.add_column-551"><span class="linenos">551</span></a>                <span class="p">)</span>
-</span><span id="DataBased.add_column-552"><a href="#DataBased.add_column-552"><span class="linenos">552</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
-</span><span id="DataBased.add_column-553"><a href="#DataBased.add_column-553"><span class="linenos">553</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
-</span><span id="DataBased.add_column-554"><a href="#DataBased.add_column-554"><span class="linenos">554</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.add_column-530"><a href="#DataBased.add_column-530"><span class="linenos">530</span></a>    <span class="nd">@_connect</span>
+</span><span id="DataBased.add_column-531"><a href="#DataBased.add_column-531"><span class="linenos">531</span></a>    <span class="k">def</span> <span class="nf">add_column</span><span class="p">(</span>
+</span><span id="DataBased.add_column-532"><a href="#DataBased.add_column-532"><span class="linenos">532</span></a>        <span class="bp">self</span><span class="p">,</span> <span class="n">table</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">column</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">_type</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">default_value</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>
+</span><span id="DataBased.add_column-533"><a href="#DataBased.add_column-533"><span class="linenos">533</span></a>    <span class="p">):</span>
+</span><span id="DataBased.add_column-534"><a href="#DataBased.add_column-534"><span class="linenos">534</span></a>        <span class="sd">&quot;&quot;&quot;Add a new column to `table`.</span>
+</span><span id="DataBased.add_column-535"><a href="#DataBased.add_column-535"><span class="linenos">535</span></a>
+</span><span id="DataBased.add_column-536"><a href="#DataBased.add_column-536"><span class="linenos">536</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.add_column-537"><a href="#DataBased.add_column-537"><span class="linenos">537</span></a>
+</span><span id="DataBased.add_column-538"><a href="#DataBased.add_column-538"><span class="linenos">538</span></a><span class="sd">        `column`: Name of the column to add.</span>
+</span><span id="DataBased.add_column-539"><a href="#DataBased.add_column-539"><span class="linenos">539</span></a>
+</span><span id="DataBased.add_column-540"><a href="#DataBased.add_column-540"><span class="linenos">540</span></a><span class="sd">        `_type`: The data type of the new column.</span>
+</span><span id="DataBased.add_column-541"><a href="#DataBased.add_column-541"><span class="linenos">541</span></a>
+</span><span id="DataBased.add_column-542"><a href="#DataBased.add_column-542"><span class="linenos">542</span></a><span class="sd">        `default_value`: Optional default value for the column.&quot;&quot;&quot;</span>
+</span><span id="DataBased.add_column-543"><a href="#DataBased.add_column-543"><span class="linenos">543</span></a>        <span class="k">try</span><span class="p">:</span>
+</span><span id="DataBased.add_column-544"><a href="#DataBased.add_column-544"><span class="linenos">544</span></a>            <span class="k">if</span> <span class="n">default_value</span><span class="p">:</span>
+</span><span id="DataBased.add_column-545"><a href="#DataBased.add_column-545"><span class="linenos">545</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.add_column-546"><a href="#DataBased.add_column-546"><span class="linenos">546</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2"> default </span><span class="si">{</span><span class="n">default_value</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased.add_column-547"><a href="#DataBased.add_column-547"><span class="linenos">547</span></a>                <span class="p">)</span>
+</span><span id="DataBased.add_column-548"><a href="#DataBased.add_column-548"><span class="linenos">548</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">update</span><span class="p">(</span><span class="n">table</span><span class="p">,</span> <span class="n">column</span><span class="p">,</span> <span class="n">default_value</span><span class="p">)</span>
+</span><span id="DataBased.add_column-549"><a href="#DataBased.add_column-549"><span class="linenos">549</span></a>            <span class="k">else</span><span class="p">:</span>
+</span><span id="DataBased.add_column-550"><a href="#DataBased.add_column-550"><span class="linenos">550</span></a>                <span class="bp">self</span><span class="o">.</span><span class="n">cursor</span><span class="o">.</span><span class="n">execute</span><span class="p">(</span>
+</span><span id="DataBased.add_column-551"><a href="#DataBased.add_column-551"><span class="linenos">551</span></a>                    <span class="sa">f</span><span class="s2">&quot;alter table [</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s2">] add column </span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s2"> </span><span class="si">{</span><span class="n">_type</span><span class="si">}</span><span class="s2">;&quot;</span>
+</span><span id="DataBased.add_column-552"><a href="#DataBased.add_column-552"><span class="linenos">552</span></a>                <span class="p">)</span>
+</span><span id="DataBased.add_column-553"><a href="#DataBased.add_column-553"><span class="linenos">553</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">info</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Added column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
+</span><span id="DataBased.add_column-554"><a href="#DataBased.add_column-554"><span class="linenos">554</span></a>        <span class="k">except</span> <span class="ne">Exception</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="DataBased.add_column-555"><a href="#DataBased.add_column-555"><span class="linenos">555</span></a>            <span class="bp">self</span><span class="o">.</span><span class="n">logger</span><span class="o">.</span><span class="n">error</span><span class="p">(</span><span class="sa">f</span><span class="s1">&#39;Failed to add column &quot;</span><span class="si">{</span><span class="n">column</span><span class="si">}</span><span class="s1">&quot; to &quot;</span><span class="si">{</span><span class="n">table</span><span class="si">}</span><span class="s1">&quot; table.&#39;</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Add a new column to <code>table</code>.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -2183,30 +2146,30 @@
         <span class="def">def</span>
         <span class="name">data_to_string</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span>,</span><span class="param">	<span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">str</span>:</span></span>
 
                 <label class="view-source-button" for="DataBased.data_to_string-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#DataBased.data_to_string"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.data_to_string-556"><a href="#DataBased.data_to_string-556"><span class="linenos">556</span></a>    <span class="nd">@staticmethod</span>
-</span><span id="DataBased.data_to_string-557"><a href="#DataBased.data_to_string-557"><span class="linenos">557</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
-</span><span id="DataBased.data_to_string-558"><a href="#DataBased.data_to_string-558"><span class="linenos">558</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="DataBased.data_to_string-559"><a href="#DataBased.data_to_string-559"><span class="linenos">559</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="DataBased.data_to_string-560"><a href="#DataBased.data_to_string-560"><span class="linenos">560</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
-</span><span id="DataBased.data_to_string-561"><a href="#DataBased.data_to_string-561"><span class="linenos">561</span></a>
-</span><span id="DataBased.data_to_string-562"><a href="#DataBased.data_to_string-562"><span class="linenos">562</span></a><span class="sd">        #### :params:</span>
-</span><span id="DataBased.data_to_string-563"><a href="#DataBased.data_to_string-563"><span class="linenos">563</span></a>
-</span><span id="DataBased.data_to_string-564"><a href="#DataBased.data_to_string-564"><span class="linenos">564</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
-</span><span id="DataBased.data_to_string-565"><a href="#DataBased.data_to_string-565"><span class="linenos">565</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
-</span><span id="DataBased.data_to_string-566"><a href="#DataBased.data_to_string-566"><span class="linenos">566</span></a>
-</span><span id="DataBased.data_to_string-567"><a href="#DataBased.data_to_string-567"><span class="linenos">567</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
-</span><span id="DataBased.data_to_string-568"><a href="#DataBased.data_to_string-568"><span class="linenos">568</span></a>
-</span><span id="DataBased.data_to_string-569"><a href="#DataBased.data_to_string-569"><span class="linenos">569</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
-</span><span id="DataBased.data_to_string-570"><a href="#DataBased.data_to_string-570"><span class="linenos">570</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
-</span><span id="DataBased.data_to_string-571"><a href="#DataBased.data_to_string-571"><span class="linenos">571</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="DataBased.data_to_string-557"><a href="#DataBased.data_to_string-557"><span class="linenos">557</span></a>    <span class="nd">@staticmethod</span>
+</span><span id="DataBased.data_to_string-558"><a href="#DataBased.data_to_string-558"><span class="linenos">558</span></a>    <span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
+</span><span id="DataBased.data_to_string-559"><a href="#DataBased.data_to_string-559"><span class="linenos">559</span></a>        <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="DataBased.data_to_string-560"><a href="#DataBased.data_to_string-560"><span class="linenos">560</span></a>    <span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="DataBased.data_to_string-561"><a href="#DataBased.data_to_string-561"><span class="linenos">561</span></a>        <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
+</span><span id="DataBased.data_to_string-562"><a href="#DataBased.data_to_string-562"><span class="linenos">562</span></a>
+</span><span id="DataBased.data_to_string-563"><a href="#DataBased.data_to_string-563"><span class="linenos">563</span></a><span class="sd">        #### :params:</span>
+</span><span id="DataBased.data_to_string-564"><a href="#DataBased.data_to_string-564"><span class="linenos">564</span></a>
+</span><span id="DataBased.data_to_string-565"><a href="#DataBased.data_to_string-565"><span class="linenos">565</span></a><span class="sd">        `data`: The list of dictionaries to create a grid from.</span>
+</span><span id="DataBased.data_to_string-566"><a href="#DataBased.data_to_string-566"><span class="linenos">566</span></a><span class="sd">        Assumes all dictionaries in list have the same set of keys.</span>
+</span><span id="DataBased.data_to_string-567"><a href="#DataBased.data_to_string-567"><span class="linenos">567</span></a>
+</span><span id="DataBased.data_to_string-568"><a href="#DataBased.data_to_string-568"><span class="linenos">568</span></a><span class="sd">        `sort_key`: Optional dictionary key to sort data with.</span>
+</span><span id="DataBased.data_to_string-569"><a href="#DataBased.data_to_string-569"><span class="linenos">569</span></a>
+</span><span id="DataBased.data_to_string-570"><a href="#DataBased.data_to_string-570"><span class="linenos">570</span></a><span class="sd">        `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
+</span><span id="DataBased.data_to_string-571"><a href="#DataBased.data_to_string-571"><span class="linenos">571</span></a><span class="sd">        Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
+</span><span id="DataBased.data_to_string-572"><a href="#DataBased.data_to_string-572"><span class="linenos">572</span></a>        <span class="k">return</span> <span class="n">data_to_string</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">sort_key</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Uses tabulate to produce pretty string output from a list of dictionaries.</p>
 
 <h4 id="params">:params:</h4>
 
@@ -2229,80 +2192,42 @@
         <span class="def">def</span>
         <span class="name">data_to_string</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">]</span>,</span><span class="param">	<span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span>,</span><span class="param">	<span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">str</span>:</span></span>
 
                 <label class="view-source-button" for="data_to_string-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#data_to_string"></a>
-            <div class="pdoc-code codehilite"><pre><span></span><span id="data_to_string-574"><a href="#data_to_string-574"><span class="linenos">574</span></a><span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
-</span><span id="data_to_string-575"><a href="#data_to_string-575"><span class="linenos">575</span></a>    <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="data_to_string-576"><a href="#data_to_string-576"><span class="linenos">576</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
-</span><span id="data_to_string-577"><a href="#data_to_string-577"><span class="linenos">577</span></a>    <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
-</span><span id="data_to_string-578"><a href="#data_to_string-578"><span class="linenos">578</span></a>
-</span><span id="data_to_string-579"><a href="#data_to_string-579"><span class="linenos">579</span></a><span class="sd">    #### :params:</span>
-</span><span id="data_to_string-580"><a href="#data_to_string-580"><span class="linenos">580</span></a>
-</span><span id="data_to_string-581"><a href="#data_to_string-581"><span class="linenos">581</span></a><span class="sd">    `data`: The list of dictionaries to create a grid from.</span>
-</span><span id="data_to_string-582"><a href="#data_to_string-582"><span class="linenos">582</span></a><span class="sd">    Assumes all dictionaries in list have the same set of keys.</span>
-</span><span id="data_to_string-583"><a href="#data_to_string-583"><span class="linenos">583</span></a>
-</span><span id="data_to_string-584"><a href="#data_to_string-584"><span class="linenos">584</span></a><span class="sd">    `sort_key`: Optional dictionary key to sort data with.</span>
-</span><span id="data_to_string-585"><a href="#data_to_string-585"><span class="linenos">585</span></a>
-</span><span id="data_to_string-586"><a href="#data_to_string-586"><span class="linenos">586</span></a><span class="sd">    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
-</span><span id="data_to_string-587"><a href="#data_to_string-587"><span class="linenos">587</span></a><span class="sd">    Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
-</span><span id="data_to_string-588"><a href="#data_to_string-588"><span class="linenos">588</span></a>    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">data</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
-</span><span id="data_to_string-589"><a href="#data_to_string-589"><span class="linenos">589</span></a>        <span class="k">return</span> <span class="s2">&quot;&quot;</span>
-</span><span id="data_to_string-590"><a href="#data_to_string-590"><span class="linenos">590</span></a>    <span class="k">if</span> <span class="n">sort_key</span><span class="p">:</span>
-</span><span id="data_to_string-591"><a href="#data_to_string-591"><span class="linenos">591</span></a>        <span class="n">data</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">d</span><span class="p">:</span> <span class="n">d</span><span class="p">[</span><span class="n">sort_key</span><span class="p">])</span>
-</span><span id="data_to_string-592"><a href="#data_to_string-592"><span class="linenos">592</span></a>    <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">d</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">data</span><span class="p">):</span>
-</span><span id="data_to_string-593"><a href="#data_to_string-593"><span class="linenos">593</span></a>        <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">d</span><span class="p">:</span>
-</span><span id="data_to_string-594"><a href="#data_to_string-594"><span class="linenos">594</span></a>            <span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">])</span>
-</span><span id="data_to_string-595"><a href="#data_to_string-595"><span class="linenos">595</span></a>
-</span><span id="data_to_string-596"><a href="#data_to_string-596"><span class="linenos">596</span></a>    <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">True</span>
-</span><span id="data_to_string-597"><a href="#data_to_string-597"><span class="linenos">597</span></a>    <span class="n">terminal_width</span> <span class="o">=</span> <span class="n">os</span><span class="o">.</span><span class="n">get_terminal_size</span><span class="p">()</span><span class="o">.</span><span class="n">columns</span>
-</span><span id="data_to_string-598"><a href="#data_to_string-598"><span class="linenos">598</span></a>    <span class="n">max_col_widths</span> <span class="o">=</span> <span class="n">terminal_width</span>
-</span><span id="data_to_string-599"><a href="#data_to_string-599"><span class="linenos">599</span></a>    <span class="c1"># Make an output with effectively unrestricted column widths</span>
-</span><span id="data_to_string-600"><a href="#data_to_string-600"><span class="linenos">600</span></a>    <span class="c1"># to see if shrinking is necessary</span>
-</span><span id="data_to_string-601"><a href="#data_to_string-601"><span class="linenos">601</span></a>    <span class="n">output</span> <span class="o">=</span> <span class="n">tabulate</span><span class="p">(</span>
-</span><span id="data_to_string-602"><a href="#data_to_string-602"><span class="linenos">602</span></a>        <span class="n">data</span><span class="p">,</span>
-</span><span id="data_to_string-603"><a href="#data_to_string-603"><span class="linenos">603</span></a>        <span class="n">headers</span><span class="o">=</span><span class="s2">&quot;keys&quot;</span><span class="p">,</span>
-</span><span id="data_to_string-604"><a href="#data_to_string-604"><span class="linenos">604</span></a>        <span class="n">disable_numparse</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
-</span><span id="data_to_string-605"><a href="#data_to_string-605"><span class="linenos">605</span></a>        <span class="n">tablefmt</span><span class="o">=</span><span class="s2">&quot;grid&quot;</span><span class="p">,</span>
-</span><span id="data_to_string-606"><a href="#data_to_string-606"><span class="linenos">606</span></a>        <span class="n">maxcolwidths</span><span class="o">=</span><span class="n">max_col_widths</span><span class="p">,</span>
-</span><span id="data_to_string-607"><a href="#data_to_string-607"><span class="linenos">607</span></a>    <span class="p">)</span>
-</span><span id="data_to_string-608"><a href="#data_to_string-608"><span class="linenos">608</span></a>    <span class="n">current_width</span> <span class="o">=</span> <span class="n">output</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="data_to_string-609"><a href="#data_to_string-609"><span class="linenos">609</span></a>    <span class="k">if</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="data_to_string-610"><a href="#data_to_string-610"><span class="linenos">610</span></a>        <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="data_to_string-611"><a href="#data_to_string-611"><span class="linenos">611</span></a>    <span class="k">if</span> <span class="n">wrap_to_terminal</span> <span class="ow">and</span> <span class="n">too_wide</span><span class="p">:</span>
-</span><span id="data_to_string-612"><a href="#data_to_string-612"><span class="linenos">612</span></a>        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Resizing grid to fit within the terminal...</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="data_to_string-613"><a href="#data_to_string-613"><span class="linenos">613</span></a>        <span class="n">previous_col_widths</span> <span class="o">=</span> <span class="n">max_col_widths</span>
-</span><span id="data_to_string-614"><a href="#data_to_string-614"><span class="linenos">614</span></a>        <span class="n">acceptable_width</span> <span class="o">=</span> <span class="n">terminal_width</span> <span class="o">-</span> <span class="mi">10</span>
-</span><span id="data_to_string-615"><a href="#data_to_string-615"><span class="linenos">615</span></a>        <span class="k">while</span> <span class="n">too_wide</span> <span class="ow">and</span> <span class="n">max_col_widths</span> <span class="o">&gt;</span> <span class="mi">1</span><span class="p">:</span>
-</span><span id="data_to_string-616"><a href="#data_to_string-616"><span class="linenos">616</span></a>            <span class="k">if</span> <span class="n">current_width</span> <span class="o">&gt;=</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="data_to_string-617"><a href="#data_to_string-617"><span class="linenos">617</span></a>                <span class="n">previous_col_widths</span> <span class="o">=</span> <span class="n">max_col_widths</span>
-</span><span id="data_to_string-618"><a href="#data_to_string-618"><span class="linenos">618</span></a>                <span class="n">max_col_widths</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span><span class="n">max_col_widths</span> <span class="o">*</span> <span class="mf">0.5</span><span class="p">)</span>
-</span><span id="data_to_string-619"><a href="#data_to_string-619"><span class="linenos">619</span></a>            <span class="k">elif</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="data_to_string-620"><a href="#data_to_string-620"><span class="linenos">620</span></a>                <span class="c1"># Without lowering acceptable_width, this condition will cause infinite loop</span>
-</span><span id="data_to_string-621"><a href="#data_to_string-621"><span class="linenos">621</span></a>                <span class="k">if</span> <span class="n">max_col_widths</span> <span class="o">==</span> <span class="n">previous_col_widths</span> <span class="o">-</span> <span class="mi">1</span><span class="p">:</span>
-</span><span id="data_to_string-622"><a href="#data_to_string-622"><span class="linenos">622</span></a>                    <span class="n">acceptable_width</span> <span class="o">-=</span> <span class="mi">10</span>
-</span><span id="data_to_string-623"><a href="#data_to_string-623"><span class="linenos">623</span></a>                <span class="n">max_col_widths</span> <span class="o">=</span> <span class="nb">int</span><span class="p">(</span>
-</span><span id="data_to_string-624"><a href="#data_to_string-624"><span class="linenos">624</span></a>                    <span class="n">max_col_widths</span> <span class="o">+</span> <span class="p">(</span><span class="mf">0.5</span> <span class="o">*</span> <span class="p">(</span><span class="n">previous_col_widths</span> <span class="o">-</span> <span class="n">max_col_widths</span><span class="p">))</span>
-</span><span id="data_to_string-625"><a href="#data_to_string-625"><span class="linenos">625</span></a>                <span class="p">)</span>
-</span><span id="data_to_string-626"><a href="#data_to_string-626"><span class="linenos">626</span></a>            <span class="n">output</span> <span class="o">=</span> <span class="n">tabulate</span><span class="p">(</span>
-</span><span id="data_to_string-627"><a href="#data_to_string-627"><span class="linenos">627</span></a>                <span class="n">data</span><span class="p">,</span>
-</span><span id="data_to_string-628"><a href="#data_to_string-628"><span class="linenos">628</span></a>                <span class="n">headers</span><span class="o">=</span><span class="s2">&quot;keys&quot;</span><span class="p">,</span>
-</span><span id="data_to_string-629"><a href="#data_to_string-629"><span class="linenos">629</span></a>                <span class="n">disable_numparse</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span>
-</span><span id="data_to_string-630"><a href="#data_to_string-630"><span class="linenos">630</span></a>                <span class="n">tablefmt</span><span class="o">=</span><span class="s2">&quot;grid&quot;</span><span class="p">,</span>
-</span><span id="data_to_string-631"><a href="#data_to_string-631"><span class="linenos">631</span></a>                <span class="n">maxcolwidths</span><span class="o">=</span><span class="n">max_col_widths</span><span class="p">,</span>
-</span><span id="data_to_string-632"><a href="#data_to_string-632"><span class="linenos">632</span></a>            <span class="p">)</span>
-</span><span id="data_to_string-633"><a href="#data_to_string-633"><span class="linenos">633</span></a>            <span class="n">current_width</span> <span class="o">=</span> <span class="n">output</span><span class="o">.</span><span class="n">index</span><span class="p">(</span><span class="s2">&quot;</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
-</span><span id="data_to_string-634"><a href="#data_to_string-634"><span class="linenos">634</span></a>            <span class="k">if</span> <span class="n">acceptable_width</span> <span class="o">&lt;</span> <span class="n">current_width</span> <span class="o">&lt;</span> <span class="n">terminal_width</span><span class="p">:</span>
-</span><span id="data_to_string-635"><a href="#data_to_string-635"><span class="linenos">635</span></a>                <span class="n">too_wide</span> <span class="o">=</span> <span class="kc">False</span>
-</span><span id="data_to_string-636"><a href="#data_to_string-636"><span class="linenos">636</span></a>        <span class="k">if</span> <span class="n">too_wide</span><span class="p">:</span>
-</span><span id="data_to_string-637"><a href="#data_to_string-637"><span class="linenos">637</span></a>            <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Couldn&#39;t resize grid to fit within the terminal.&quot;</span><span class="p">)</span>
-</span><span id="data_to_string-638"><a href="#data_to_string-638"><span class="linenos">638</span></a>            <span class="k">return</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
-</span><span id="data_to_string-639"><a href="#data_to_string-639"><span class="linenos">639</span></a>    <span class="k">return</span> <span class="n">output</span>
+            <div class="pdoc-code codehilite"><pre><span></span><span id="data_to_string-575"><a href="#data_to_string-575"><span class="linenos">575</span></a><span class="k">def</span> <span class="nf">data_to_string</span><span class="p">(</span>
+</span><span id="data_to_string-576"><a href="#data_to_string-576"><span class="linenos">576</span></a>    <span class="n">data</span><span class="p">:</span> <span class="nb">list</span><span class="p">[</span><span class="nb">dict</span><span class="p">],</span> <span class="n">sort_key</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="kc">None</span> <span class="o">=</span> <span class="kc">None</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>
+</span><span id="data_to_string-577"><a href="#data_to_string-577"><span class="linenos">577</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
+</span><span id="data_to_string-578"><a href="#data_to_string-578"><span class="linenos">578</span></a>    <span class="sd">&quot;&quot;&quot;Uses tabulate to produce pretty string output from a list of dictionaries.</span>
+</span><span id="data_to_string-579"><a href="#data_to_string-579"><span class="linenos">579</span></a>
+</span><span id="data_to_string-580"><a href="#data_to_string-580"><span class="linenos">580</span></a><span class="sd">    #### :params:</span>
+</span><span id="data_to_string-581"><a href="#data_to_string-581"><span class="linenos">581</span></a>
+</span><span id="data_to_string-582"><a href="#data_to_string-582"><span class="linenos">582</span></a><span class="sd">    `data`: The list of dictionaries to create a grid from.</span>
+</span><span id="data_to_string-583"><a href="#data_to_string-583"><span class="linenos">583</span></a><span class="sd">    Assumes all dictionaries in list have the same set of keys.</span>
+</span><span id="data_to_string-584"><a href="#data_to_string-584"><span class="linenos">584</span></a>
+</span><span id="data_to_string-585"><a href="#data_to_string-585"><span class="linenos">585</span></a><span class="sd">    `sort_key`: Optional dictionary key to sort data with.</span>
+</span><span id="data_to_string-586"><a href="#data_to_string-586"><span class="linenos">586</span></a>
+</span><span id="data_to_string-587"><a href="#data_to_string-587"><span class="linenos">587</span></a><span class="sd">    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit within the current terminal window.</span>
+</span><span id="data_to_string-588"><a href="#data_to_string-588"><span class="linenos">588</span></a><span class="sd">    Pass as `False` if the output is going into something like a `.txt` file.&quot;&quot;&quot;</span>
+</span><span id="data_to_string-589"><a href="#data_to_string-589"><span class="linenos">589</span></a>    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">data</span><span class="p">)</span> <span class="o">==</span> <span class="mi">0</span><span class="p">:</span>
+</span><span id="data_to_string-590"><a href="#data_to_string-590"><span class="linenos">590</span></a>        <span class="k">return</span> <span class="s2">&quot;&quot;</span>
+</span><span id="data_to_string-591"><a href="#data_to_string-591"><span class="linenos">591</span></a>    <span class="k">if</span> <span class="n">sort_key</span><span class="p">:</span>
+</span><span id="data_to_string-592"><a href="#data_to_string-592"><span class="linenos">592</span></a>        <span class="n">data</span> <span class="o">=</span> <span class="nb">sorted</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="k">lambda</span> <span class="n">d</span><span class="p">:</span> <span class="n">d</span><span class="p">[</span><span class="n">sort_key</span><span class="p">])</span>
+</span><span id="data_to_string-593"><a href="#data_to_string-593"><span class="linenos">593</span></a>    <span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">d</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">data</span><span class="p">):</span>
+</span><span id="data_to_string-594"><a href="#data_to_string-594"><span class="linenos">594</span></a>        <span class="k">for</span> <span class="n">k</span> <span class="ow">in</span> <span class="n">d</span><span class="p">:</span>
+</span><span id="data_to_string-595"><a href="#data_to_string-595"><span class="linenos">595</span></a>            <span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">]</span> <span class="o">=</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">[</span><span class="n">i</span><span class="p">][</span><span class="n">k</span><span class="p">])</span>
+</span><span id="data_to_string-596"><a href="#data_to_string-596"><span class="linenos">596</span></a>
+</span><span id="data_to_string-597"><a href="#data_to_string-597"><span class="linenos">597</span></a>    <span class="k">try</span><span class="p">:</span>
+</span><span id="data_to_string-598"><a href="#data_to_string-598"><span class="linenos">598</span></a>        <span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Resizing grid to fit within the terminal...</span><span class="se">\n</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="data_to_string-599"><a href="#data_to_string-599"><span class="linenos">599</span></a>        <span class="k">return</span> <span class="n">griddy</span><span class="p">(</span><span class="n">data</span><span class="p">,</span> <span class="s2">&quot;keys&quot;</span><span class="p">,</span> <span class="n">wrap_to_terminal</span><span class="p">)</span>
+</span><span id="data_to_string-600"><a href="#data_to_string-600"><span class="linenos">600</span></a>    <span class="k">except</span> <span class="ne">RuntimeError</span> <span class="k">as</span> <span class="n">e</span><span class="p">:</span>
+</span><span id="data_to_string-601"><a href="#data_to_string-601"><span class="linenos">601</span></a>        <span class="nb">print</span><span class="p">(</span><span class="n">e</span><span class="p">)</span>
+</span><span id="data_to_string-602"><a href="#data_to_string-602"><span class="linenos">602</span></a>        <span class="k">return</span> <span class="nb">str</span><span class="p">(</span><span class="n">data</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Uses tabulate to produce pretty string output from a list of dictionaries.</p>
 
 <h4 id="params">:params:</h4>
```

#### html2text {}

```diff
@@ -32,709 +32,53 @@
 __2import os
 __3import sqlite3
 __4from datetime import datetime
 __5from functools import wraps
 __6from typing import Any
 __7
 __8import pandas
-__9from pathier import Pathier
-_10from tabulate import tabulate
-_11
+__9from griddle import griddy
+_10from pathier import Pathier
+_11from tabulate import tabulate
 _12
-_13def _connect(func):
-_14    """Decorator to open db connection if it isn't already open."""
-_15
-_16    @wraps(func)
-_17    def inner(self, *args, **kwargs):
-_18        if not self.connection_open:
-_19            self.open()
-_20        results = func(self, *args, **kwargs)
-_21        return results
-_22
-_23    return inner
-_24
+_13
+_14def _connect(func):
+_15    """Decorator to open db connection if it isn't already open."""
+_16
+_17    @wraps(func)
+_18    def inner(self, *args, **kwargs):
+_19        if not self.connection_open:
+_20            self.open()
+_21        results = func(self, *args, **kwargs)
+_22        return results
+_23
+_24    return inner
 _25
-_26def _disconnect(func):
-_27    """Decorator to commit and close db connection.
-_28
-_29    Primarily intended for when `DataBased` is subclassed and the inhereting
+_26
+_27def _disconnect(func):
+_28    """Decorator to commit and close db connection.
+_29
+_30    Primarily intended for when `DataBased` is subclassed and the inhereting
 class
-_30    has functions that call parent class functions that are decorated with
+_31    has functions that call parent class functions that are decorated with
 `_connect`.
-_31    Decorating the child class function with `_disconnect` avoids having to
+_32    Decorating the child class function with `_disconnect` avoids having to
 manually close
-_32    the connection or use a context manager in an application."""
-_33
-_34    @wraps(func)
-_35    def inner(self, *args, **kwargs):
-_36        result = func(self, *args, **kwargs)
-_37        if self.connection_open:
-_38            self.close()
-_39        return result
-_40
-_41    return inner
-_42
+_33    the connection or use a context manager in an application."""
+_34
+_35    @wraps(func)
+_36    def inner(self, *args, **kwargs):
+_37        result = func(self, *args, **kwargs)
+_38        if self.connection_open:
+_39            self.close()
+_40        return result
+_41
+_42    return inner
 _43
-_44class DataBased:
-_45    """Sqli wrapper so queries don't need to be written except table
-definitions.
-_46
-_47    Supports saving and reading dates as datetime objects.
-_48
-_49    Supports using a context manager."""
-_50
-_51    def __init__(
-_52        self,
-_53        dbpath: str | Pathier,
-_54        logger_encoding: str = "utf-8",
-_55        logger_message_format: str = "{levelname}|-|{asctime}|-|{message}",
-_56        connection_timeout: float = 10,
-_57    ):
-_58        """
-_59        #### :params:
-_60
-_61        * `dbpath`: String or Path object to database file.
-_62        If a relative path is given, it will be relative to the
-_63        current working directory. The log file will be saved to the
-_64        same directory.
-_65
-_66        * `logger_message_format`: `{` style format string for the logger
-object.
-_67
-_68        * `connection_timeout`: The number of seconds to wait when trying to
-connect to the database before throwing an error."""
-_69        self.dbpath = Pathier(dbpath)
-_70        self.dbname = Pathier(dbpath).name
-_71        self.dbpath.parent.mkdir(parents=True, exist_ok=True)
-_72        self._logger_init(
-_73            encoding=logger_encoding, message_format=logger_message_format
-_74        )
-_75        self.connection_open = False
-_76        self.connection_timeout = connection_timeout
-_77
-_78    def __enter__(self):
-_79        self.open()
-_80        return self
-_81
-_82    def __exit__(self, exception_type, exception_value,
-exception_traceback):
-_83        self.close()
-_84
-_85    @property
-_86    def connection_timeout(self) -> float:
-_87        return self._connection_timeout
-_88
-_89    @connection_timeout.setter
-_90    def connection_timeout(self, num_seconds: float):
-_91        self._connection_timeout = num_seconds
-_92        if self.connection_open:
-_93            self.close()
-_94            self.open()
-_95
-_96    def open(self):
-_97        """Open connection to db."""
-_98        self.connection = sqlite3.connect(
-_99            self.dbpath,
-100            detect_types=sqlite3.PARSE_DECLTYPES | sqlite3.PARSE_COLNAMES,
-101            timeout=self.connection_timeout,
-102        )
-103        self.connection.execute("pragma foreign_keys = 1;")
-104        self.cursor = self.connection.cursor()
-105        self.connection_open = True
-106
-107    def close(self):
-108        """Save and close connection to db.
-109
-110        Call this as soon as you are done using the database if you have
-111        multiple threads or processes using the same database."""
-112        if self.connection_open:
-113            self.connection.commit()
-114            self.connection.close()
-115            self.connection_open = False
-116
-117    def _logger_init(
-118        self,
-119        message_format: str = "{levelname}|-|{asctime}|-|{message}",
-120        encoding: str = "utf-8",
-121    ):
-122        """:param `message_format`: '{' style format string"""
-123        self.logger = logging.getLogger(self.dbname)
-124        if not self.logger.hasHandlers():
-125            handler = logging.FileHandler(
-126                str(self.dbpath).replace(".", "") + ".log",
-encoding=encoding
-127            )
-128            handler.setFormatter(
-129                logging.Formatter(
-130                    message_format, style="{", datefmt="%m/%d/%Y %I:%M:%S
-%p"
-131                )
-132            )
-133            self.logger.addHandler(handler)
-134            self.logger.setLevel(logging.INFO)
-135
-136    def _get_dict(
-137        self, table: str, values: list, columns_to_return: list[str] | None
-= None
-138    ) -> dict:
-139        """Converts the values of a row into a dictionary with column names
-as keys.
-140
-141        #### :params:
-142
-143        `table`: The table that values were pulled from.
-144
-145        `values`: List of values expected to be the same quantity
-146        and in the same order as the column names of table.
-147
-148        `columns_to_return`: An optional list of column names.
-149        If given, only these columns will be included in the returned
-dictionary.
-150        Otherwise all columns and values are returned."""
-151        return {
-152            column: value
-153            for column, value in zip(self.get_column_names(table), values)
-154            if not columns_to_return or column in columns_to_return
-155        }
-156
-157    def _get_conditions(
-158        self, match_criteria: list[tuple] | dict, exact_match: bool = True
-159    ) -> str:
-160        """Builds and returns the conditional portion of a query.
-161
-162        #### :params:
-163
-164        `match_criteria`: Can be a list of 2-tuples where each
-165        tuple is `(columnName, rowValue)` or a dictionary where
-166        keys are column names and values are row values.
-167
-168        `exact_match`: If `False`, the row value for a given column
-169        will be matched as a substring.
-170
-171        Usage e.g.:
-172
-173        >>> self.cursor.execute(f'select * from {table} where
-{conditions};')"""
-174        if type(match_criteria) == dict:
-175            match_criteria = [(k, v) for k, v in match_criteria.items()]
-176        if exact_match:
-177            conditions = " and ".join(
-178                f'"{column_row[0]}" = "{column_row[1]}"'
-179                for column_row in match_criteria
-180            )
-181        else:
-182            conditions = " and ".join(
-183                f'"{column_row[0]}" like "%{column_row[1]}%"'
-184                for column_row in match_criteria
-185            )
-186        return f"({conditions})"
-187
-188    def vacuum(self):
-189        """Reduce disk size of the database with a `VACUUM` query."""
-190        self.query("VACUUM;")
-191
-192    @_connect
-193    def query(self, query_) -> list[Any]:
-194        """Execute an arbitrary query and return the results."""
-195        self.cursor.execute(query_)
-196        return self.cursor.fetchall()
-197
-198    @_connect
-199    def create_tables(self, table_defs: list[str] = []):
-200        """Create tables if they don't exist.
-201
-202        :param `table_defs`: Each definition should be in the form
-`table_name(column_definitions)`"""
-203        if len(table_defs) > 0:
-204            table_names = self.get_table_names()
-205            for table in table_defs:
-206                if table.split("(")[0].strip() not in table_names:
-207                    self.cursor.execute(f"create table [{table}];")
-208                    self.logger.info(f'{table.split("(")[0]} table
-created.')
-209
-210    @_connect
-211    def create_table(self, table: str, column_defs: list[str]):
-212        """Create a table if it doesn't exist.
-213
-214        #### :params:
-215
-216        `table`: Name of the table to create.
-217
-218        `column_defs`: List of column definitions in proper Sqlite3 sytax.
-219        i.e. `"column_name text unique"` or `"column_name int primary key"`
-etc."""
-220        if table not in self.get_table_names():
-221            query = f"create table [{table}]({', '.join(column_defs)});"
-222            self.cursor.execute(query)
-223            self.logger.info(f"'{table}' table created.")
-224
-225    @_connect
-226    def get_table_names(self) -> list[str]:
-227        """Returns a list of table names from the database."""
-228        self.cursor.execute(
-229            'select name from sqlite_Schema where type = "table" and name
-not like "sqlite_%";'
-230        )
-231        return [result[0] for result in self.cursor.fetchall()]
-232
-233    @_connect
-234    def get_column_names(self, table: str) -> list[str]:
-235        """Return a list of column names from a table."""
-236        self.cursor.execute(f"select * from [{table}] where 1=0;")
-237        return [description[0] for description in self.cursor.description]
-238
-239    @_connect
-240    def count(
-241        self,
-242        table: str,
-243        match_criteria: list[tuple] | dict | None = None,
-244        exact_match: bool = True,
-245    ) -> int:
-246        """Return number of items in `table`.
-247
-248        #### :params:
-249
-250        `match_criteria`: Can be a list of 2-tuples where each
-251        tuple is `(columnName, rowValue)` or a dictionary where
-252        keys are column names and values are row values.
-253        If `None`, all rows from the table will be counted.
-254
-255        `exact_match`: If `False`, the row value for a given column
-256        in `match_criteria` will be matched as a substring.
-257        Has no effect if `match_criteria` is `None`.
-258        """
-259        query = f"select count(_rowid_) from [{table}]"
-260        try:
-261            if match_criteria:
-262                self.cursor.execute(
-263                    f"{query} where {self._get_conditions(match_criteria,
-exact_match)};"
-264                )
-265            else:
-266                self.cursor.execute(f"{query}")
-267            return self.cursor.fetchone()[0]
-268        except:
-269            return 0
-270
-271    @_connect
-272    def add_row(
-273        self, table: str, values: tuple[Any], columns: tuple[str] | None =
-None
-274    ) -> bool:
-275        """Add a row of values to a table.
-276
-277        Returns whether the addition was successful or not.
-278
-279        #### :params:
-280
-281        `table`: The table to insert values into.
-282
-283        `values`: A tuple of values to be inserted into the table.
-284
-285        `columns`: If `None`, `values` is expected to supply a value for
-every column in the table.
-286        If `columns` is provided, it should contain the same number of
-elements as `values`."""
-287        parameterizer = ", ".join("?" for _ in values)
-288        logger_values = ", ".join(str(value) for value in values)
-289        try:
-290            if columns:
-291                columns_query = ", ".join(column for column in columns)
-292                self.cursor.execute(
-293                    f"insert into [{table}] ({columns_query}) values(
-{parameterizer});",
-294                    values,
-295                )
-296            else:
-297                self.cursor.execute(
-298                    f"insert into [{table}] values({parameterizer});",
-values
-299                )
-300            self.logger.info(f'Added "{logger_values}" to {table} table.')
-301            return True
-302        except Exception as e:
-303            if "constraint" not in str(e).lower():
-304                self.logger.exception(
-305                    f'Error adding "{logger_values}" to {table} table.'
-306                )
-307            else:
-308                self.logger.debug(str(e))
-309            return False
-310
-311    @_connect
-312    def add_rows(
-313        self, table: str, values: list[tuple[Any]], columns: tuple[str] |
-None = None
-314    ) -> tuple[int, int]:
-315        """Add multiple rows of values to a table.
-316
-317        Returns a tuple containing the number of successful additions and
-the number of failed additions.
-318
-319        #### :params:
-320
-321        `table`: The table to insert values into.
-322
-323        `values`: A list of tuples of values to be inserted into the table.
-324        Each tuple constitutes a single row to be inserted
-325
-326        `columns`: If `None`, `values` is expected to supply a value for
-every column in the table.
-327        If `columns` is provided, it should contain the same number of
-elements as `values`."""
-328        successes = 0
-329        failures = 0
-330        for row in values:
-331            if self.add_row(table, row, columns):
-332                successes += 1
-333            else:
-334                failures += 1
-335        return (successes, failures)
-336
-337    @_connect
-338    def get_rows(
-339        self,
-340        table: str,
-341        match_criteria: list[tuple] | dict | None = None,
-342        exact_match: bool = True,
-343        sort_by_column: str | None = None,
-344        columns_to_return: list[str] | None = None,
-345        return_as_dataframe: bool = False,
-346        values_only: bool = False,
-347        order_by: str | None = None,
-348        limit: str | int | None = None,
-349    ) -> list[dict] | list[tuple] | pandas.DataFrame:
-350        """Return matching rows from `table`.
-351
-352        By default, rows will be returned as a list of dictionaries of the
-form `[{"column_name": value, ...}, ...]`
-353
-354
-355        #### :params:
-356
-357        `match_criteria`: Can be a list of 2-tuples where each
-358        tuple is `(columnName, rowValue)` or a dictionary where
-359        keys are column names and values are row values.
-360
-361        `exact_match`: If `False`, the row value for a given column will be
-matched as a substring.
-362
-363        `sort_by_column`: A column name to sort the results by.
-364        This will sort results in Python after retrieving them from the db.
-365        Use the 'order_by' param to use SQLite engine for ordering.
-366
-367        `columns_to_return`: Optional list of column names.
-368        If provided, the elements returned by this function will only
-contain the provided columns.
-369        Otherwise every column in the row is returned.
-370
-371        `return_as_dataframe`: Return the results as a `pandas.DataFrame`
-object.
-372
-373        `values_only`: Return the results as a list of tuples.
-374
-375        `order_by`: If given, a `order by {order_by}` clause will be added
-to the select query.
-376
-377        `limit`: If given, a `limit {limit}` clause will be added to the
-select query.
-378        """
-379
-380        if type(columns_to_return) is str:
-381            columns_to_return = [columns_to_return]
-382        query = f"select * from [{table}]"
-383        matches = []
-384        if match_criteria:
-385            query += f" where {self._get_conditions(match_criteria,
-exact_match)}"
-386        if order_by:
-387            query += f" order by {order_by}"
-388        if limit:
-389            query += f" limit {limit}"
-390        query += ";"
-391        self.cursor.execute(query)
-392        matches = self.cursor.fetchall()
-393        results = [self._get_dict(table, match, columns_to_return) for match
-in matches]
-394        if sort_by_column:
-395            results = sorted(results, key=lambda x: x[sort_by_column])
-396        if return_as_dataframe:
-397            return pandas.DataFrame(results)
-398        if values_only:
-399            return [tuple(row.values()) for row in results]
-400        else:
-401            return results
-402
-403    @_connect
-404    def find(
-405        self, table: str, query_string: str, columns: list[str] | None =
-None
-406    ) -> list[dict]:
-407        """Search for rows that contain `query_string` as a substring of any
-column.
-408
-409        #### :params:
-410
-411        `table`: The table to search.
-412
-413        `query_string`: The substring to search for in all columns.
-414
-415        `columns`: A list of columns to search for query_string.
-416        If None, all columns in the table will be searched.
-417        """
-418        if type(columns) is str:
-419            columns = [columns]
-420        results = []
-421        if not columns:
-422            columns = self.get_column_names(table)
-423        for column in columns:
-424            results.extend(
-425                [
-426                    row
-427                    for row in self.get_rows(
-428                        table, [(column, query_string)], exact_match=False
-429                    )
-430                    if row not in results
-431                ]
-432            )
-433        return results
-434
-435    @_connect
-436    def delete(
-437        self, table: str, match_criteria: list[tuple] | dict, exact_match:
-bool = True
-438    ) -> int:
-439        """Delete records from `table`.
-440
-441        Returns the number of deleted records.
-442
-443        #### :params:
-444
-445        `match_criteria`: Can be a list of 2-tuples where each tuple is `
-(column_name, value)`
-446        or a dictionary where keys are column names and values are
-corresponding values.
-447
-448        `exact_match`: If `False`, the value for a given column will be
-matched as a substring.
-449        """
-450        conditions = self._get_conditions(match_criteria, exact_match)
-451        try:
-452            self.cursor.execute(f"delete from [{table}] where
-{conditions};")
-453            num_deletions = self.cursor.rowcount
-454            self.logger.info(
-455                f'Deleted {num_deletions} rows from "{table}" where
-{conditions}".'
-456            )
-457            return num_deletions
-458        except Exception as e:
-459            self.logger.debug(
-460                f'Error deleting rows from "{table}" where {conditions}.\n
-{e}'
-461            )
-462            return 0
-463
-464    @_connect
-465    def update(
-466        self,
-467        table: str,
-468        column_to_update: str,
-469        new_value: Any,
-470        match_criteria: list[tuple] | dict | None = None,
-471        exact_match: bool = True,
-472    ) -> int:
-473        """Update the value in `column_to_update` to `new_value` for rows
-matched with `match_criteria`.
-474
-475        #### :params:
-476
-477        `table`: The table to update rows in.
-478
-479        `column_to_update`: The column to be updated in the matched rows.
-480
-481        `new_value`: The new value to insert.
-482
-483        `match_criteria`: Can be a list of 2-tuples where each tuple is `
-(columnName, rowValue)`
-484        or a dictionary where keys are column names and values are
-corresponding values.
-485        If `None`, every row in `table` will be updated.
-486
-487        `exact_match`: If `False`, `match_criteria` values will be treated
-as substrings.
-488
-489        Returns the number of updated rows."""
-490        query = f"update [{table}] set {column_to_update} = ?"
-491        conditions = ""
-492        if match_criteria:
-493            conditions = self._get_conditions(match_criteria, exact_match)
-494            query += f" where {conditions}"
-495        else:
-496            conditions = None
-497        query += ";"
-498        try:
-499            self.cursor.execute(
-500                query,
-501                (new_value,),
-502            )
-503            num_updates = self.cursor.rowcount
-504            self.logger.info(
-505                f'In {num_updates} rows, updated "{column_to_update}" in "
-{table}" table to "{new_value}" where {conditions}'
-506            )
-507            return num_updates
-508        except Exception as e:
-509            self.logger.error(
-510                f'Failed to update "{column_to_update}" in "{table}" table
-to "{new_value}" where {conditions}"\n{e}'
-511            )
-512            return 0
-513
-514    @_connect
-515    def drop_table(self, table: str) -> bool:
-516        """Drop `table` from the database.
-517
-518        Returns `True` if successful, `False` if not."""
-519        try:
-520            self.cursor.execute(f"drop Table [{table}];")
-521            self.logger.info(f'Dropped table "{table}"')
-522            return True
-523        except Exception as e:
-524            print(e)
-525            self.logger.error(f'Failed to drop table "{table}"')
-526            return False
-527
-528    @_connect
-529    def add_column(
-530        self, table: str, column: str, _type: str, default_value: str | None
-= None
-531    ):
-532        """Add a new column to `table`.
-533
-534        #### :params:
-535
-536        `column`: Name of the column to add.
-537
-538        `_type`: The data type of the new column.
-539
-540        `default_value`: Optional default value for the column."""
-541        try:
-542            if default_value:
-543                self.cursor.execute(
-544                    f"alter table [{table}] add column {column} {_type}
-default {default_value};"
-545                )
-546                self.update(table, column, default_value)
-547            else:
-548                self.cursor.execute(
-549                    f"alter table [{table}] add column {column} {_type};"
-550                )
-551            self.logger.info(f'Added column "{column}" to "{table}" table.')
-552        except Exception as e:
-553            self.logger.error(f'Failed to add column "{column}" to "{table}"
-table.')
-554
-555    @staticmethod
-556    def data_to_string(
-557        data: list[dict], sort_key: str | None = None, wrap_to_terminal:
-bool = True
-558    ) -> str:
-559        """Uses tabulate to produce pretty string output from a list of
-dictionaries.
-560
-561        #### :params:
-562
-563        `data`: The list of dictionaries to create a grid from.
-564        Assumes all dictionaries in list have the same set of keys.
-565
-566        `sort_key`: Optional dictionary key to sort data with.
-567
-568        `wrap_to_terminal`: If `True`, the table width will be wrapped to
-fit within the current terminal window.
-569        Pass as `False` if the output is going into something like a `.txt`
-file."""
-570        return data_to_string(data, sort_key, wrap_to_terminal)
-571
-572
-573def data_to_string(
-574    data: list[dict], sort_key: str | None = None, wrap_to_terminal: bool =
-True
-575) -> str:
-576    """Uses tabulate to produce pretty string output from a list of
-dictionaries.
-577
-578    #### :params:
-579
-580    `data`: The list of dictionaries to create a grid from.
-581    Assumes all dictionaries in list have the same set of keys.
-582
-583    `sort_key`: Optional dictionary key to sort data with.
-584
-585    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit
-within the current terminal window.
-586    Pass as `False` if the output is going into something like a `.txt`
-file."""
-587    if len(data) == 0:
-588        return ""
-589    if sort_key:
-590        data = sorted(data, key=lambda d: d[sort_key])
-591    for i, d in enumerate(data):
-592        for k in d:
-593            data[i][k] = str(data[i][k])
-594
-595    too_wide = True
-596    terminal_width = os.get_terminal_size().columns
-597    max_col_widths = terminal_width
-598    # Make an output with effectively unrestricted column widths
-599    # to see if shrinking is necessary
-600    output = tabulate(
-601        data,
-602        headers="keys",
-603        disable_numparse=True,
-604        tablefmt="grid",
-605        maxcolwidths=max_col_widths,
-606    )
-607    current_width = output.index("\n")
-608    if current_width < terminal_width:
-609        too_wide = False
-610    if wrap_to_terminal and too_wide:
-611        print("Resizing grid to fit within the terminal...\n")
-612        previous_col_widths = max_col_widths
-613        acceptable_width = terminal_width - 10
-614        while too_wide and max_col_widths > 1:
-615            if current_width >= terminal_width:
-616                previous_col_widths = max_col_widths
-617                max_col_widths = int(max_col_widths * 0.5)
-618            elif current_width < terminal_width:
-619                # Without lowering acceptable_width, this condition will
-cause infinite loop
-620                if max_col_widths == previous_col_widths - 1:
-621                    acceptable_width -= 10
-622                max_col_widths = int(
-623                    max_col_widths + (0.5 * (previous_col_widths -
-max_col_widths))
-624                )
-625            output = tabulate(
-626                data,
-627                headers="keys",
-628                disable_numparse=True,
-629                tablefmt="grid",
-630                maxcolwidths=max_col_widths,
-631            )
-632            current_width = output.index("\n")
-633            if acceptable_width < current_width < terminal_width:
-634                too_wide = False
-635        if too_wide:
-636            print("Couldn't resize grid to fit within the terminal.")
-637            return str(data)
-638    return output
-  ⁰
-class DataBased: View Source
+_44
 _45class DataBased:
 _46    """Sqli wrapper so queries don't need to be written except table
 definitions.
 _47
 _48    Supports saving and reading dates as datetime objects.
 _49
 _50    Supports using a context manager."""
@@ -1308,297 +652,914 @@
 567        `sort_key`: Optional dictionary key to sort data with.
 568
 569        `wrap_to_terminal`: If `True`, the table width will be wrapped to
 fit within the current terminal window.
 570        Pass as `False` if the output is going into something like a `.txt`
 file."""
 571        return data_to_string(data, sort_key, wrap_to_terminal)
+572
+573
+574def data_to_string(
+575    data: list[dict], sort_key: str | None = None, wrap_to_terminal: bool =
+True
+576) -> str:
+577    """Uses tabulate to produce pretty string output from a list of
+dictionaries.
+578
+579    #### :params:
+580
+581    `data`: The list of dictionaries to create a grid from.
+582    Assumes all dictionaries in list have the same set of keys.
+583
+584    `sort_key`: Optional dictionary key to sort data with.
+585
+586    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit
+within the current terminal window.
+587    Pass as `False` if the output is going into something like a `.txt`
+file."""
+588    if len(data) == 0:
+589        return ""
+590    if sort_key:
+591        data = sorted(data, key=lambda d: d[sort_key])
+592    for i, d in enumerate(data):
+593        for k in d:
+594            data[i][k] = str(data[i][k])
+595
+596    try:
+597        print("Resizing grid to fit within the terminal...\n")
+598        return griddy(data, "keys", wrap_to_terminal)
+599    except RuntimeError as e:
+600        print(e)
+601        return str(data)
+  ⁰
+class DataBased: View Source
+_46class DataBased:
+_47    """Sqli wrapper so queries don't need to be written except table
+definitions.
+_48
+_49    Supports saving and reading dates as datetime objects.
+_50
+_51    Supports using a context manager."""
+_52
+_53    def __init__(
+_54        self,
+_55        dbpath: str | Pathier,
+_56        logger_encoding: str = "utf-8",
+_57        logger_message_format: str = "{levelname}|-|{asctime}|-|{message}",
+_58        connection_timeout: float = 10,
+_59    ):
+_60        """
+_61        #### :params:
+_62
+_63        * `dbpath`: String or Path object to database file.
+_64        If a relative path is given, it will be relative to the
+_65        current working directory. The log file will be saved to the
+_66        same directory.
+_67
+_68        * `logger_message_format`: `{` style format string for the logger
+object.
+_69
+_70        * `connection_timeout`: The number of seconds to wait when trying to
+connect to the database before throwing an error."""
+_71        self.dbpath = Pathier(dbpath)
+_72        self.dbname = Pathier(dbpath).name
+_73        self.dbpath.parent.mkdir(parents=True, exist_ok=True)
+_74        self._logger_init(
+_75            encoding=logger_encoding, message_format=logger_message_format
+_76        )
+_77        self.connection_open = False
+_78        self.connection_timeout = connection_timeout
+_79
+_80    def __enter__(self):
+_81        self.open()
+_82        return self
+_83
+_84    def __exit__(self, exception_type, exception_value,
+exception_traceback):
+_85        self.close()
+_86
+_87    @property
+_88    def connection_timeout(self) -> float:
+_89        return self._connection_timeout
+_90
+_91    @connection_timeout.setter
+_92    def connection_timeout(self, num_seconds: float):
+_93        self._connection_timeout = num_seconds
+_94        if self.connection_open:
+_95            self.close()
+_96            self.open()
+_97
+_98    def open(self):
+_99        """Open connection to db."""
+100        self.connection = sqlite3.connect(
+101            self.dbpath,
+102            detect_types=sqlite3.PARSE_DECLTYPES | sqlite3.PARSE_COLNAMES,
+103            timeout=self.connection_timeout,
+104        )
+105        self.connection.execute("pragma foreign_keys = 1;")
+106        self.cursor = self.connection.cursor()
+107        self.connection_open = True
+108
+109    def close(self):
+110        """Save and close connection to db.
+111
+112        Call this as soon as you are done using the database if you have
+113        multiple threads or processes using the same database."""
+114        if self.connection_open:
+115            self.connection.commit()
+116            self.connection.close()
+117            self.connection_open = False
+118
+119    def _logger_init(
+120        self,
+121        message_format: str = "{levelname}|-|{asctime}|-|{message}",
+122        encoding: str = "utf-8",
+123    ):
+124        """:param `message_format`: '{' style format string"""
+125        self.logger = logging.getLogger(self.dbname)
+126        if not self.logger.hasHandlers():
+127            handler = logging.FileHandler(
+128                str(self.dbpath).replace(".", "") + ".log",
+encoding=encoding
+129            )
+130            handler.setFormatter(
+131                logging.Formatter(
+132                    message_format, style="{", datefmt="%m/%d/%Y %I:%M:%S
+%p"
+133                )
+134            )
+135            self.logger.addHandler(handler)
+136            self.logger.setLevel(logging.INFO)
+137
+138    def _get_dict(
+139        self, table: str, values: list, columns_to_return: list[str] | None
+= None
+140    ) -> dict:
+141        """Converts the values of a row into a dictionary with column names
+as keys.
+142
+143        #### :params:
+144
+145        `table`: The table that values were pulled from.
+146
+147        `values`: List of values expected to be the same quantity
+148        and in the same order as the column names of table.
+149
+150        `columns_to_return`: An optional list of column names.
+151        If given, only these columns will be included in the returned
+dictionary.
+152        Otherwise all columns and values are returned."""
+153        return {
+154            column: value
+155            for column, value in zip(self.get_column_names(table), values)
+156            if not columns_to_return or column in columns_to_return
+157        }
+158
+159    def _get_conditions(
+160        self, match_criteria: list[tuple] | dict, exact_match: bool = True
+161    ) -> str:
+162        """Builds and returns the conditional portion of a query.
+163
+164        #### :params:
+165
+166        `match_criteria`: Can be a list of 2-tuples where each
+167        tuple is `(columnName, rowValue)` or a dictionary where
+168        keys are column names and values are row values.
+169
+170        `exact_match`: If `False`, the row value for a given column
+171        will be matched as a substring.
+172
+173        Usage e.g.:
+174
+175        >>> self.cursor.execute(f'select * from {table} where
+{conditions};')"""
+176        if type(match_criteria) == dict:
+177            match_criteria = [(k, v) for k, v in match_criteria.items()]
+178        if exact_match:
+179            conditions = " and ".join(
+180                f'"{column_row[0]}" = "{column_row[1]}"'
+181                for column_row in match_criteria
+182            )
+183        else:
+184            conditions = " and ".join(
+185                f'"{column_row[0]}" like "%{column_row[1]}%"'
+186                for column_row in match_criteria
+187            )
+188        return f"({conditions})"
+189
+190    def vacuum(self):
+191        """Reduce disk size of the database with a `VACUUM` query."""
+192        self.query("VACUUM;")
+193
+194    @_connect
+195    def query(self, query_) -> list[Any]:
+196        """Execute an arbitrary query and return the results."""
+197        self.cursor.execute(query_)
+198        return self.cursor.fetchall()
+199
+200    @_connect
+201    def create_tables(self, table_defs: list[str] = []):
+202        """Create tables if they don't exist.
+203
+204        :param `table_defs`: Each definition should be in the form
+`table_name(column_definitions)`"""
+205        if len(table_defs) > 0:
+206            table_names = self.get_table_names()
+207            for table in table_defs:
+208                if table.split("(")[0].strip() not in table_names:
+209                    self.cursor.execute(f"create table [{table}];")
+210                    self.logger.info(f'{table.split("(")[0]} table
+created.')
+211
+212    @_connect
+213    def create_table(self, table: str, column_defs: list[str]):
+214        """Create a table if it doesn't exist.
+215
+216        #### :params:
+217
+218        `table`: Name of the table to create.
+219
+220        `column_defs`: List of column definitions in proper Sqlite3 sytax.
+221        i.e. `"column_name text unique"` or `"column_name int primary key"`
+etc."""
+222        if table not in self.get_table_names():
+223            query = f"create table [{table}]({', '.join(column_defs)});"
+224            self.cursor.execute(query)
+225            self.logger.info(f"'{table}' table created.")
+226
+227    @_connect
+228    def get_table_names(self) -> list[str]:
+229        """Returns a list of table names from the database."""
+230        self.cursor.execute(
+231            'select name from sqlite_Schema where type = "table" and name
+not like "sqlite_%";'
+232        )
+233        return [result[0] for result in self.cursor.fetchall()]
+234
+235    @_connect
+236    def get_column_names(self, table: str) -> list[str]:
+237        """Return a list of column names from a table."""
+238        self.cursor.execute(f"select * from [{table}] where 1=0;")
+239        return [description[0] for description in self.cursor.description]
+240
+241    @_connect
+242    def count(
+243        self,
+244        table: str,
+245        match_criteria: list[tuple] | dict | None = None,
+246        exact_match: bool = True,
+247    ) -> int:
+248        """Return number of items in `table`.
+249
+250        #### :params:
+251
+252        `match_criteria`: Can be a list of 2-tuples where each
+253        tuple is `(columnName, rowValue)` or a dictionary where
+254        keys are column names and values are row values.
+255        If `None`, all rows from the table will be counted.
+256
+257        `exact_match`: If `False`, the row value for a given column
+258        in `match_criteria` will be matched as a substring.
+259        Has no effect if `match_criteria` is `None`.
+260        """
+261        query = f"select count(_rowid_) from [{table}]"
+262        try:
+263            if match_criteria:
+264                self.cursor.execute(
+265                    f"{query} where {self._get_conditions(match_criteria,
+exact_match)};"
+266                )
+267            else:
+268                self.cursor.execute(f"{query}")
+269            return self.cursor.fetchone()[0]
+270        except:
+271            return 0
+272
+273    @_connect
+274    def add_row(
+275        self, table: str, values: tuple[Any], columns: tuple[str] | None =
+None
+276    ) -> bool:
+277        """Add a row of values to a table.
+278
+279        Returns whether the addition was successful or not.
+280
+281        #### :params:
+282
+283        `table`: The table to insert values into.
+284
+285        `values`: A tuple of values to be inserted into the table.
+286
+287        `columns`: If `None`, `values` is expected to supply a value for
+every column in the table.
+288        If `columns` is provided, it should contain the same number of
+elements as `values`."""
+289        parameterizer = ", ".join("?" for _ in values)
+290        logger_values = ", ".join(str(value) for value in values)
+291        try:
+292            if columns:
+293                columns_query = ", ".join(column for column in columns)
+294                self.cursor.execute(
+295                    f"insert into [{table}] ({columns_query}) values(
+{parameterizer});",
+296                    values,
+297                )
+298            else:
+299                self.cursor.execute(
+300                    f"insert into [{table}] values({parameterizer});",
+values
+301                )
+302            self.logger.info(f'Added "{logger_values}" to {table} table.')
+303            return True
+304        except Exception as e:
+305            if "constraint" not in str(e).lower():
+306                self.logger.exception(
+307                    f'Error adding "{logger_values}" to {table} table.'
+308                )
+309            else:
+310                self.logger.debug(str(e))
+311            return False
+312
+313    @_connect
+314    def add_rows(
+315        self, table: str, values: list[tuple[Any]], columns: tuple[str] |
+None = None
+316    ) -> tuple[int, int]:
+317        """Add multiple rows of values to a table.
+318
+319        Returns a tuple containing the number of successful additions and
+the number of failed additions.
+320
+321        #### :params:
+322
+323        `table`: The table to insert values into.
+324
+325        `values`: A list of tuples of values to be inserted into the table.
+326        Each tuple constitutes a single row to be inserted
+327
+328        `columns`: If `None`, `values` is expected to supply a value for
+every column in the table.
+329        If `columns` is provided, it should contain the same number of
+elements as `values`."""
+330        successes = 0
+331        failures = 0
+332        for row in values:
+333            if self.add_row(table, row, columns):
+334                successes += 1
+335            else:
+336                failures += 1
+337        return (successes, failures)
+338
+339    @_connect
+340    def get_rows(
+341        self,
+342        table: str,
+343        match_criteria: list[tuple] | dict | None = None,
+344        exact_match: bool = True,
+345        sort_by_column: str | None = None,
+346        columns_to_return: list[str] | None = None,
+347        return_as_dataframe: bool = False,
+348        values_only: bool = False,
+349        order_by: str | None = None,
+350        limit: str | int | None = None,
+351    ) -> list[dict] | list[tuple] | pandas.DataFrame:
+352        """Return matching rows from `table`.
+353
+354        By default, rows will be returned as a list of dictionaries of the
+form `[{"column_name": value, ...}, ...]`
+355
+356
+357        #### :params:
+358
+359        `match_criteria`: Can be a list of 2-tuples where each
+360        tuple is `(columnName, rowValue)` or a dictionary where
+361        keys are column names and values are row values.
+362
+363        `exact_match`: If `False`, the row value for a given column will be
+matched as a substring.
+364
+365        `sort_by_column`: A column name to sort the results by.
+366        This will sort results in Python after retrieving them from the db.
+367        Use the 'order_by' param to use SQLite engine for ordering.
+368
+369        `columns_to_return`: Optional list of column names.
+370        If provided, the elements returned by this function will only
+contain the provided columns.
+371        Otherwise every column in the row is returned.
+372
+373        `return_as_dataframe`: Return the results as a `pandas.DataFrame`
+object.
+374
+375        `values_only`: Return the results as a list of tuples.
+376
+377        `order_by`: If given, a `order by {order_by}` clause will be added
+to the select query.
+378
+379        `limit`: If given, a `limit {limit}` clause will be added to the
+select query.
+380        """
+381
+382        if type(columns_to_return) is str:
+383            columns_to_return = [columns_to_return]
+384        query = f"select * from [{table}]"
+385        matches = []
+386        if match_criteria:
+387            query += f" where {self._get_conditions(match_criteria,
+exact_match)}"
+388        if order_by:
+389            query += f" order by {order_by}"
+390        if limit:
+391            query += f" limit {limit}"
+392        query += ";"
+393        self.cursor.execute(query)
+394        matches = self.cursor.fetchall()
+395        results = [self._get_dict(table, match, columns_to_return) for match
+in matches]
+396        if sort_by_column:
+397            results = sorted(results, key=lambda x: x[sort_by_column])
+398        if return_as_dataframe:
+399            return pandas.DataFrame(results)
+400        if values_only:
+401            return [tuple(row.values()) for row in results]
+402        else:
+403            return results
+404
+405    @_connect
+406    def find(
+407        self, table: str, query_string: str, columns: list[str] | None =
+None
+408    ) -> list[dict]:
+409        """Search for rows that contain `query_string` as a substring of any
+column.
+410
+411        #### :params:
+412
+413        `table`: The table to search.
+414
+415        `query_string`: The substring to search for in all columns.
+416
+417        `columns`: A list of columns to search for query_string.
+418        If None, all columns in the table will be searched.
+419        """
+420        if type(columns) is str:
+421            columns = [columns]
+422        results = []
+423        if not columns:
+424            columns = self.get_column_names(table)
+425        for column in columns:
+426            results.extend(
+427                [
+428                    row
+429                    for row in self.get_rows(
+430                        table, [(column, query_string)], exact_match=False
+431                    )
+432                    if row not in results
+433                ]
+434            )
+435        return results
+436
+437    @_connect
+438    def delete(
+439        self, table: str, match_criteria: list[tuple] | dict, exact_match:
+bool = True
+440    ) -> int:
+441        """Delete records from `table`.
+442
+443        Returns the number of deleted records.
+444
+445        #### :params:
+446
+447        `match_criteria`: Can be a list of 2-tuples where each tuple is `
+(column_name, value)`
+448        or a dictionary where keys are column names and values are
+corresponding values.
+449
+450        `exact_match`: If `False`, the value for a given column will be
+matched as a substring.
+451        """
+452        conditions = self._get_conditions(match_criteria, exact_match)
+453        try:
+454            self.cursor.execute(f"delete from [{table}] where
+{conditions};")
+455            num_deletions = self.cursor.rowcount
+456            self.logger.info(
+457                f'Deleted {num_deletions} rows from "{table}" where
+{conditions}".'
+458            )
+459            return num_deletions
+460        except Exception as e:
+461            self.logger.debug(
+462                f'Error deleting rows from "{table}" where {conditions}.\n
+{e}'
+463            )
+464            return 0
+465
+466    @_connect
+467    def update(
+468        self,
+469        table: str,
+470        column_to_update: str,
+471        new_value: Any,
+472        match_criteria: list[tuple] | dict | None = None,
+473        exact_match: bool = True,
+474    ) -> int:
+475        """Update the value in `column_to_update` to `new_value` for rows
+matched with `match_criteria`.
+476
+477        #### :params:
+478
+479        `table`: The table to update rows in.
+480
+481        `column_to_update`: The column to be updated in the matched rows.
+482
+483        `new_value`: The new value to insert.
+484
+485        `match_criteria`: Can be a list of 2-tuples where each tuple is `
+(columnName, rowValue)`
+486        or a dictionary where keys are column names and values are
+corresponding values.
+487        If `None`, every row in `table` will be updated.
+488
+489        `exact_match`: If `False`, `match_criteria` values will be treated
+as substrings.
+490
+491        Returns the number of updated rows."""
+492        query = f"update [{table}] set {column_to_update} = ?"
+493        conditions = ""
+494        if match_criteria:
+495            conditions = self._get_conditions(match_criteria, exact_match)
+496            query += f" where {conditions}"
+497        else:
+498            conditions = None
+499        query += ";"
+500        try:
+501            self.cursor.execute(
+502                query,
+503                (new_value,),
+504            )
+505            num_updates = self.cursor.rowcount
+506            self.logger.info(
+507                f'In {num_updates} rows, updated "{column_to_update}" in "
+{table}" table to "{new_value}" where {conditions}'
+508            )
+509            return num_updates
+510        except Exception as e:
+511            self.logger.error(
+512                f'Failed to update "{column_to_update}" in "{table}" table
+to "{new_value}" where {conditions}"\n{e}'
+513            )
+514            return 0
+515
+516    @_connect
+517    def drop_table(self, table: str) -> bool:
+518        """Drop `table` from the database.
+519
+520        Returns `True` if successful, `False` if not."""
+521        try:
+522            self.cursor.execute(f"drop Table [{table}];")
+523            self.logger.info(f'Dropped table "{table}"')
+524            return True
+525        except Exception as e:
+526            print(e)
+527            self.logger.error(f'Failed to drop table "{table}"')
+528            return False
+529
+530    @_connect
+531    def add_column(
+532        self, table: str, column: str, _type: str, default_value: str | None
+= None
+533    ):
+534        """Add a new column to `table`.
+535
+536        #### :params:
+537
+538        `column`: Name of the column to add.
+539
+540        `_type`: The data type of the new column.
+541
+542        `default_value`: Optional default value for the column."""
+543        try:
+544            if default_value:
+545                self.cursor.execute(
+546                    f"alter table [{table}] add column {column} {_type}
+default {default_value};"
+547                )
+548                self.update(table, column, default_value)
+549            else:
+550                self.cursor.execute(
+551                    f"alter table [{table}] add column {column} {_type};"
+552                )
+553            self.logger.info(f'Added column "{column}" to "{table}" table.')
+554        except Exception as e:
+555            self.logger.error(f'Failed to add column "{column}" to "{table}"
+table.')
+556
+557    @staticmethod
+558    def data_to_string(
+559        data: list[dict], sort_key: str | None = None, wrap_to_terminal:
+bool = True
+560    ) -> str:
+561        """Uses tabulate to produce pretty string output from a list of
+dictionaries.
+562
+563        #### :params:
+564
+565        `data`: The list of dictionaries to create a grid from.
+566        Assumes all dictionaries in list have the same set of keys.
+567
+568        `sort_key`: Optional dictionary key to sort data with.
+569
+570        `wrap_to_terminal`: If `True`, the table width will be wrapped to
+fit within the current terminal window.
+571        Pass as `False` if the output is going into something like a `.txt`
+file."""
+572        return data_to_string(data, sort_key, wrap_to_terminal)
 Sqli wrapper so queries don't need to be written except table definitions.
 Supports saving and reading dates as datetime objects.
 Supports using a context manager.
 ⁰
 DataBased(
 dbpath: str | pathier.pathier.Pathier,
 logger_encoding: str = 'utf-8',
 logger_message_format: str = '{levelname}|-|{asctime}|-|{message}',
 connection_timeout: float = 10) View Source
-52    def __init__(
-53        self,
-54        dbpath: str | Pathier,
-55        logger_encoding: str = "utf-8",
-56        logger_message_format: str = "{levelname}|-|{asctime}|-|{message}",
-57        connection_timeout: float = 10,
-58    ):
-59        """
-60        #### :params:
-61
-62        * `dbpath`: String or Path object to database file.
-63        If a relative path is given, it will be relative to the
-64        current working directory. The log file will be saved to the
-65        same directory.
-66
-67        * `logger_message_format`: `{` style format string for the logger
+53    def __init__(
+54        self,
+55        dbpath: str | Pathier,
+56        logger_encoding: str = "utf-8",
+57        logger_message_format: str = "{levelname}|-|{asctime}|-|{message}",
+58        connection_timeout: float = 10,
+59    ):
+60        """
+61        #### :params:
+62
+63        * `dbpath`: String or Path object to database file.
+64        If a relative path is given, it will be relative to the
+65        current working directory. The log file will be saved to the
+66        same directory.
+67
+68        * `logger_message_format`: `{` style format string for the logger
 object.
-68
-69        * `connection_timeout`: The number of seconds to wait when trying to
+69
+70        * `connection_timeout`: The number of seconds to wait when trying to
 connect to the database before throwing an error."""
-70        self.dbpath = Pathier(dbpath)
-71        self.dbname = Pathier(dbpath).name
-72        self.dbpath.parent.mkdir(parents=True, exist_ok=True)
-73        self._logger_init(
-74            encoding=logger_encoding, message_format=logger_message_format
-75        )
-76        self.connection_open = False
-77        self.connection_timeout = connection_timeout
+71        self.dbpath = Pathier(dbpath)
+72        self.dbname = Pathier(dbpath).name
+73        self.dbpath.parent.mkdir(parents=True, exist_ok=True)
+74        self._logger_init(
+75            encoding=logger_encoding, message_format=logger_message_format
+76        )
+77        self.connection_open = False
+78        self.connection_timeout = connection_timeout
 *** :params: ***
     * dbpath: String or Path object to database file. If a relative path is
       given, it will be relative to the current working directory. The log file
       will be saved to the same directory.
     * logger_message_format: { style format string for the logger object.
     * connection_timeout: The number of seconds to wait when trying to connect
       to the database before throwing an error.
 ⁰
 def open(self): View Source
-_97    def open(self):
-_98        """Open connection to db."""
-_99        self.connection = sqlite3.connect(
-100            self.dbpath,
-101            detect_types=sqlite3.PARSE_DECLTYPES | sqlite3.PARSE_COLNAMES,
-102            timeout=self.connection_timeout,
-103        )
-104        self.connection.execute("pragma foreign_keys = 1;")
-105        self.cursor = self.connection.cursor()
-106        self.connection_open = True
+_98    def open(self):
+_99        """Open connection to db."""
+100        self.connection = sqlite3.connect(
+101            self.dbpath,
+102            detect_types=sqlite3.PARSE_DECLTYPES | sqlite3.PARSE_COLNAMES,
+103            timeout=self.connection_timeout,
+104        )
+105        self.connection.execute("pragma foreign_keys = 1;")
+106        self.cursor = self.connection.cursor()
+107        self.connection_open = True
 Open connection to db.
 ⁰
 def close(self): View Source
-108    def close(self):
-109        """Save and close connection to db.
-110
-111        Call this as soon as you are done using the database if you have
-112        multiple threads or processes using the same database."""
-113        if self.connection_open:
-114            self.connection.commit()
-115            self.connection.close()
-116            self.connection_open = False
+109    def close(self):
+110        """Save and close connection to db.
+111
+112        Call this as soon as you are done using the database if you have
+113        multiple threads or processes using the same database."""
+114        if self.connection_open:
+115            self.connection.commit()
+116            self.connection.close()
+117            self.connection_open = False
 Save and close connection to db.
 Call this as soon as you are done using the database if you have multiple
 threads or processes using the same database.
 ⁰
 def vacuum(self): View Source
-189    def vacuum(self):
-190        """Reduce disk size of the database with a `VACUUM` query."""
-191        self.query("VACUUM;")
+190    def vacuum(self):
+191        """Reduce disk size of the database with a `VACUUM` query."""
+192        self.query("VACUUM;")
 Reduce disk size of the database with a VACUUM query.
 ⁰
 def query(self, query_) -> list[typing.Any]: View Source
-193    @_connect
-194    def query(self, query_) -> list[Any]:
-195        """Execute an arbitrary query and return the results."""
-196        self.cursor.execute(query_)
-197        return self.cursor.fetchall()
+194    @_connect
+195    def query(self, query_) -> list[Any]:
+196        """Execute an arbitrary query and return the results."""
+197        self.cursor.execute(query_)
+198        return self.cursor.fetchall()
 Execute an arbitrary query and return the results.
 ⁰
 def create_tables(self, table_defs: list[str] = []): View Source
-199    @_connect
-200    def create_tables(self, table_defs: list[str] = []):
-201        """Create tables if they don't exist.
-202
-203        :param `table_defs`: Each definition should be in the form
+200    @_connect
+201    def create_tables(self, table_defs: list[str] = []):
+202        """Create tables if they don't exist.
+203
+204        :param `table_defs`: Each definition should be in the form
 `table_name(column_definitions)`"""
-204        if len(table_defs) > 0:
-205            table_names = self.get_table_names()
-206            for table in table_defs:
-207                if table.split("(")[0].strip() not in table_names:
-208                    self.cursor.execute(f"create table [{table}];")
-209                    self.logger.info(f'{table.split("(")[0]} table
+205        if len(table_defs) > 0:
+206            table_names = self.get_table_names()
+207            for table in table_defs:
+208                if table.split("(")[0].strip() not in table_names:
+209                    self.cursor.execute(f"create table [{table}];")
+210                    self.logger.info(f'{table.split("(")[0]} table
 created.')
 Create tables if they don't exist.
 * Parameters *
     * table_defs: Each definition should be in the form table_name
       (column_definitions)
 ⁰
 def create_table(self, table: str, column_defs: list[str]): View Source
-211    @_connect
-212    def create_table(self, table: str, column_defs: list[str]):
-213        """Create a table if it doesn't exist.
-214
-215        #### :params:
-216
-217        `table`: Name of the table to create.
-218
-219        `column_defs`: List of column definitions in proper Sqlite3 sytax.
-220        i.e. `"column_name text unique"` or `"column_name int primary key"`
+212    @_connect
+213    def create_table(self, table: str, column_defs: list[str]):
+214        """Create a table if it doesn't exist.
+215
+216        #### :params:
+217
+218        `table`: Name of the table to create.
+219
+220        `column_defs`: List of column definitions in proper Sqlite3 sytax.
+221        i.e. `"column_name text unique"` or `"column_name int primary key"`
 etc."""
-221        if table not in self.get_table_names():
-222            query = f"create table [{table}]({', '.join(column_defs)});"
-223            self.cursor.execute(query)
-224            self.logger.info(f"'{table}' table created.")
+222        if table not in self.get_table_names():
+223            query = f"create table [{table}]({', '.join(column_defs)});"
+224            self.cursor.execute(query)
+225            self.logger.info(f"'{table}' table created.")
 Create a table if it doesn't exist.
 *** :params: ***
 table: Name of the table to create.
 column_defs: List of column definitions in proper Sqlite3 sytax. i.e.
 "column_name text unique" or "column_name int primary key" etc.
 ⁰
 def get_table_names(self) -> list[str]: View Source
-226    @_connect
-227    def get_table_names(self) -> list[str]:
-228        """Returns a list of table names from the database."""
-229        self.cursor.execute(
-230            'select name from sqlite_Schema where type = "table" and name
+227    @_connect
+228    def get_table_names(self) -> list[str]:
+229        """Returns a list of table names from the database."""
+230        self.cursor.execute(
+231            'select name from sqlite_Schema where type = "table" and name
 not like "sqlite_%";'
-231        )
-232        return [result[0] for result in self.cursor.fetchall()]
+232        )
+233        return [result[0] for result in self.cursor.fetchall()]
 Returns a list of table names from the database.
 ⁰
 def get_column_names(self, table: str) -> list[str]: View Source
-234    @_connect
-235    def get_column_names(self, table: str) -> list[str]:
-236        """Return a list of column names from a table."""
-237        self.cursor.execute(f"select * from [{table}] where 1=0;")
-238        return [description[0] for description in self.cursor.description]
+235    @_connect
+236    def get_column_names(self, table: str) -> list[str]:
+237        """Return a list of column names from a table."""
+238        self.cursor.execute(f"select * from [{table}] where 1=0;")
+239        return [description[0] for description in self.cursor.description]
 Return a list of column names from a table.
 ⁰
 def count(
 self,
 table: str,
 match_criteria: list[tuple] | dict | None = None,
 exact_match: bool = True) -> int: View Source
-240    @_connect
-241    def count(
-242        self,
-243        table: str,
-244        match_criteria: list[tuple] | dict | None = None,
-245        exact_match: bool = True,
-246    ) -> int:
-247        """Return number of items in `table`.
-248
-249        #### :params:
-250
-251        `match_criteria`: Can be a list of 2-tuples where each
-252        tuple is `(columnName, rowValue)` or a dictionary where
-253        keys are column names and values are row values.
-254        If `None`, all rows from the table will be counted.
-255
-256        `exact_match`: If `False`, the row value for a given column
-257        in `match_criteria` will be matched as a substring.
-258        Has no effect if `match_criteria` is `None`.
-259        """
-260        query = f"select count(_rowid_) from [{table}]"
-261        try:
-262            if match_criteria:
-263                self.cursor.execute(
-264                    f"{query} where {self._get_conditions(match_criteria,
+241    @_connect
+242    def count(
+243        self,
+244        table: str,
+245        match_criteria: list[tuple] | dict | None = None,
+246        exact_match: bool = True,
+247    ) -> int:
+248        """Return number of items in `table`.
+249
+250        #### :params:
+251
+252        `match_criteria`: Can be a list of 2-tuples where each
+253        tuple is `(columnName, rowValue)` or a dictionary where
+254        keys are column names and values are row values.
+255        If `None`, all rows from the table will be counted.
+256
+257        `exact_match`: If `False`, the row value for a given column
+258        in `match_criteria` will be matched as a substring.
+259        Has no effect if `match_criteria` is `None`.
+260        """
+261        query = f"select count(_rowid_) from [{table}]"
+262        try:
+263            if match_criteria:
+264                self.cursor.execute(
+265                    f"{query} where {self._get_conditions(match_criteria,
 exact_match)};"
-265                )
-266            else:
-267                self.cursor.execute(f"{query}")
-268            return self.cursor.fetchone()[0]
-269        except:
-270            return 0
+266                )
+267            else:
+268                self.cursor.execute(f"{query}")
+269            return self.cursor.fetchone()[0]
+270        except:
+271            return 0
 Return number of items in table.
 *** :params: ***
 match_criteria: Can be a list of 2-tuples where each tuple is (columnName,
 rowValue) or a dictionary where keys are column names and values are row
 values. If None, all rows from the table will be counted.
 exact_match: If False, the row value for a given column in match_criteria will
 be matched as a substring. Has no effect if match_criteria is None.
 ⁰
 def add_row(
 self,
 table: str,
 values: tuple[typing.Any],
 columns: tuple[str] | None = None) -> bool: View Source
-272    @_connect
-273    def add_row(
-274        self, table: str, values: tuple[Any], columns: tuple[str] | None =
+273    @_connect
+274    def add_row(
+275        self, table: str, values: tuple[Any], columns: tuple[str] | None =
 None
-275    ) -> bool:
-276        """Add a row of values to a table.
-277
-278        Returns whether the addition was successful or not.
-279
-280        #### :params:
-281
-282        `table`: The table to insert values into.
-283
-284        `values`: A tuple of values to be inserted into the table.
-285
-286        `columns`: If `None`, `values` is expected to supply a value for
+276    ) -> bool:
+277        """Add a row of values to a table.
+278
+279        Returns whether the addition was successful or not.
+280
+281        #### :params:
+282
+283        `table`: The table to insert values into.
+284
+285        `values`: A tuple of values to be inserted into the table.
+286
+287        `columns`: If `None`, `values` is expected to supply a value for
 every column in the table.
-287        If `columns` is provided, it should contain the same number of
+288        If `columns` is provided, it should contain the same number of
 elements as `values`."""
-288        parameterizer = ", ".join("?" for _ in values)
-289        logger_values = ", ".join(str(value) for value in values)
-290        try:
-291            if columns:
-292                columns_query = ", ".join(column for column in columns)
-293                self.cursor.execute(
-294                    f"insert into [{table}] ({columns_query}) values(
+289        parameterizer = ", ".join("?" for _ in values)
+290        logger_values = ", ".join(str(value) for value in values)
+291        try:
+292            if columns:
+293                columns_query = ", ".join(column for column in columns)
+294                self.cursor.execute(
+295                    f"insert into [{table}] ({columns_query}) values(
 {parameterizer});",
-295                    values,
-296                )
-297            else:
-298                self.cursor.execute(
-299                    f"insert into [{table}] values({parameterizer});",
+296                    values,
+297                )
+298            else:
+299                self.cursor.execute(
+300                    f"insert into [{table}] values({parameterizer});",
 values
-300                )
-301            self.logger.info(f'Added "{logger_values}" to {table} table.')
-302            return True
-303        except Exception as e:
-304            if "constraint" not in str(e).lower():
-305                self.logger.exception(
-306                    f'Error adding "{logger_values}" to {table} table.'
-307                )
-308            else:
-309                self.logger.debug(str(e))
-310            return False
+301                )
+302            self.logger.info(f'Added "{logger_values}" to {table} table.')
+303            return True
+304        except Exception as e:
+305            if "constraint" not in str(e).lower():
+306                self.logger.exception(
+307                    f'Error adding "{logger_values}" to {table} table.'
+308                )
+309            else:
+310                self.logger.debug(str(e))
+311            return False
 Add a row of values to a table.
 Returns whether the addition was successful or not.
 *** :params: ***
 table: The table to insert values into.
 values: A tuple of values to be inserted into the table.
 columns: If None, values is expected to supply a value for every column in the
 table. If columns is provided, it should contain the same number of elements as
 values.
 ⁰
 def add_rows(
 self,
 table: str,
 values: list[tuple[typing.Any]],
 columns: tuple[str] | None = None) -> tuple[int, int]: View Source
-312    @_connect
-313    def add_rows(
-314        self, table: str, values: list[tuple[Any]], columns: tuple[str] |
+313    @_connect
+314    def add_rows(
+315        self, table: str, values: list[tuple[Any]], columns: tuple[str] |
 None = None
-315    ) -> tuple[int, int]:
-316        """Add multiple rows of values to a table.
-317
-318        Returns a tuple containing the number of successful additions and
+316    ) -> tuple[int, int]:
+317        """Add multiple rows of values to a table.
+318
+319        Returns a tuple containing the number of successful additions and
 the number of failed additions.
-319
-320        #### :params:
-321
-322        `table`: The table to insert values into.
-323
-324        `values`: A list of tuples of values to be inserted into the table.
-325        Each tuple constitutes a single row to be inserted
-326
-327        `columns`: If `None`, `values` is expected to supply a value for
+320
+321        #### :params:
+322
+323        `table`: The table to insert values into.
+324
+325        `values`: A list of tuples of values to be inserted into the table.
+326        Each tuple constitutes a single row to be inserted
+327
+328        `columns`: If `None`, `values` is expected to supply a value for
 every column in the table.
-328        If `columns` is provided, it should contain the same number of
+329        If `columns` is provided, it should contain the same number of
 elements as `values`."""
-329        successes = 0
-330        failures = 0
-331        for row in values:
-332            if self.add_row(table, row, columns):
-333                successes += 1
-334            else:
-335                failures += 1
-336        return (successes, failures)
+330        successes = 0
+331        failures = 0
+332        for row in values:
+333            if self.add_row(table, row, columns):
+334                successes += 1
+335            else:
+336                failures += 1
+337        return (successes, failures)
 Add multiple rows of values to a table.
 Returns a tuple containing the number of successful additions and the number of
 failed additions.
 *** :params: ***
 table: The table to insert values into.
 values: A list of tuples of values to be inserted into the table. Each tuple
 constitutes a single row to be inserted
@@ -1614,87 +1575,87 @@
 sort_by_column: str | None = None,
 columns_to_return: list[str] | None = None,
 return_as_dataframe: bool = False,
 values_only: bool = False,
 order_by: str | None = None,
 limit: str | int | None = None) -> list[dict] | list[tuple] |
 pandas.core.frame.DataFrame: View Source
-338    @_connect
-339    def get_rows(
-340        self,
-341        table: str,
-342        match_criteria: list[tuple] | dict | None = None,
-343        exact_match: bool = True,
-344        sort_by_column: str | None = None,
-345        columns_to_return: list[str] | None = None,
-346        return_as_dataframe: bool = False,
-347        values_only: bool = False,
-348        order_by: str | None = None,
-349        limit: str | int | None = None,
-350    ) -> list[dict] | list[tuple] | pandas.DataFrame:
-351        """Return matching rows from `table`.
-352
-353        By default, rows will be returned as a list of dictionaries of the
+339    @_connect
+340    def get_rows(
+341        self,
+342        table: str,
+343        match_criteria: list[tuple] | dict | None = None,
+344        exact_match: bool = True,
+345        sort_by_column: str | None = None,
+346        columns_to_return: list[str] | None = None,
+347        return_as_dataframe: bool = False,
+348        values_only: bool = False,
+349        order_by: str | None = None,
+350        limit: str | int | None = None,
+351    ) -> list[dict] | list[tuple] | pandas.DataFrame:
+352        """Return matching rows from `table`.
+353
+354        By default, rows will be returned as a list of dictionaries of the
 form `[{"column_name": value, ...}, ...]`
-354
 355
-356        #### :params:
-357
-358        `match_criteria`: Can be a list of 2-tuples where each
-359        tuple is `(columnName, rowValue)` or a dictionary where
-360        keys are column names and values are row values.
-361
-362        `exact_match`: If `False`, the row value for a given column will be
+356
+357        #### :params:
+358
+359        `match_criteria`: Can be a list of 2-tuples where each
+360        tuple is `(columnName, rowValue)` or a dictionary where
+361        keys are column names and values are row values.
+362
+363        `exact_match`: If `False`, the row value for a given column will be
 matched as a substring.
-363
-364        `sort_by_column`: A column name to sort the results by.
-365        This will sort results in Python after retrieving them from the db.
-366        Use the 'order_by' param to use SQLite engine for ordering.
-367
-368        `columns_to_return`: Optional list of column names.
-369        If provided, the elements returned by this function will only
+364
+365        `sort_by_column`: A column name to sort the results by.
+366        This will sort results in Python after retrieving them from the db.
+367        Use the 'order_by' param to use SQLite engine for ordering.
+368
+369        `columns_to_return`: Optional list of column names.
+370        If provided, the elements returned by this function will only
 contain the provided columns.
-370        Otherwise every column in the row is returned.
-371
-372        `return_as_dataframe`: Return the results as a `pandas.DataFrame`
+371        Otherwise every column in the row is returned.
+372
+373        `return_as_dataframe`: Return the results as a `pandas.DataFrame`
 object.
-373
-374        `values_only`: Return the results as a list of tuples.
-375
-376        `order_by`: If given, a `order by {order_by}` clause will be added
+374
+375        `values_only`: Return the results as a list of tuples.
+376
+377        `order_by`: If given, a `order by {order_by}` clause will be added
 to the select query.
-377
-378        `limit`: If given, a `limit {limit}` clause will be added to the
+378
+379        `limit`: If given, a `limit {limit}` clause will be added to the
 select query.
-379        """
-380
-381        if type(columns_to_return) is str:
-382            columns_to_return = [columns_to_return]
-383        query = f"select * from [{table}]"
-384        matches = []
-385        if match_criteria:
-386            query += f" where {self._get_conditions(match_criteria,
+380        """
+381
+382        if type(columns_to_return) is str:
+383            columns_to_return = [columns_to_return]
+384        query = f"select * from [{table}]"
+385        matches = []
+386        if match_criteria:
+387            query += f" where {self._get_conditions(match_criteria,
 exact_match)}"
-387        if order_by:
-388            query += f" order by {order_by}"
-389        if limit:
-390            query += f" limit {limit}"
-391        query += ";"
-392        self.cursor.execute(query)
-393        matches = self.cursor.fetchall()
-394        results = [self._get_dict(table, match, columns_to_return) for match
+388        if order_by:
+389            query += f" order by {order_by}"
+390        if limit:
+391            query += f" limit {limit}"
+392        query += ";"
+393        self.cursor.execute(query)
+394        matches = self.cursor.fetchall()
+395        results = [self._get_dict(table, match, columns_to_return) for match
 in matches]
-395        if sort_by_column:
-396            results = sorted(results, key=lambda x: x[sort_by_column])
-397        if return_as_dataframe:
-398            return pandas.DataFrame(results)
-399        if values_only:
-400            return [tuple(row.values()) for row in results]
-401        else:
-402            return results
+396        if sort_by_column:
+397            results = sorted(results, key=lambda x: x[sort_by_column])
+398        if return_as_dataframe:
+399            return pandas.DataFrame(results)
+400        if values_only:
+401            return [tuple(row.values()) for row in results]
+402        else:
+403            return results
 Return matching rows from table.
 By default, rows will be returned as a list of dictionaries of the form [
 {"column_name": value, ...}, ...]
 *** :params: ***
 match_criteria: Can be a list of 2-tuples where each tuple is (columnName,
 rowValue) or a dictionary where keys are column names and values are row
 values.
@@ -1713,94 +1674,94 @@
 limit: If given, a limit {limit} clause will be added to the select query.
 ⁰
 def find(
 self,
 table: str,
 query_string: str,
 columns: list[str] | None = None) -> list[dict]: View Source
-404    @_connect
-405    def find(
-406        self, table: str, query_string: str, columns: list[str] | None =
+405    @_connect
+406    def find(
+407        self, table: str, query_string: str, columns: list[str] | None =
 None
-407    ) -> list[dict]:
-408        """Search for rows that contain `query_string` as a substring of any
+408    ) -> list[dict]:
+409        """Search for rows that contain `query_string` as a substring of any
 column.
-409
-410        #### :params:
-411
-412        `table`: The table to search.
-413
-414        `query_string`: The substring to search for in all columns.
-415
-416        `columns`: A list of columns to search for query_string.
-417        If None, all columns in the table will be searched.
-418        """
-419        if type(columns) is str:
-420            columns = [columns]
-421        results = []
-422        if not columns:
-423            columns = self.get_column_names(table)
-424        for column in columns:
-425            results.extend(
-426                [
-427                    row
-428                    for row in self.get_rows(
-429                        table, [(column, query_string)], exact_match=False
-430                    )
-431                    if row not in results
-432                ]
-433            )
-434        return results
+410
+411        #### :params:
+412
+413        `table`: The table to search.
+414
+415        `query_string`: The substring to search for in all columns.
+416
+417        `columns`: A list of columns to search for query_string.
+418        If None, all columns in the table will be searched.
+419        """
+420        if type(columns) is str:
+421            columns = [columns]
+422        results = []
+423        if not columns:
+424            columns = self.get_column_names(table)
+425        for column in columns:
+426            results.extend(
+427                [
+428                    row
+429                    for row in self.get_rows(
+430                        table, [(column, query_string)], exact_match=False
+431                    )
+432                    if row not in results
+433                ]
+434            )
+435        return results
 Search for rows that contain query_string as a substring of any column.
 *** :params: ***
 table: The table to search.
 query_string: The substring to search for in all columns.
 columns: A list of columns to search for query_string. If None, all columns in
 the table will be searched.
 ⁰
 def delete(
 self,
 table: str,
 match_criteria: list[tuple] | dict,
 exact_match: bool = True) -> int: View Source
-436    @_connect
-437    def delete(
-438        self, table: str, match_criteria: list[tuple] | dict, exact_match:
+437    @_connect
+438    def delete(
+439        self, table: str, match_criteria: list[tuple] | dict, exact_match:
 bool = True
-439    ) -> int:
-440        """Delete records from `table`.
-441
-442        Returns the number of deleted records.
-443
-444        #### :params:
-445
-446        `match_criteria`: Can be a list of 2-tuples where each tuple is `
+440    ) -> int:
+441        """Delete records from `table`.
+442
+443        Returns the number of deleted records.
+444
+445        #### :params:
+446
+447        `match_criteria`: Can be a list of 2-tuples where each tuple is `
 (column_name, value)`
-447        or a dictionary where keys are column names and values are
+448        or a dictionary where keys are column names and values are
 corresponding values.
-448
-449        `exact_match`: If `False`, the value for a given column will be
+449
+450        `exact_match`: If `False`, the value for a given column will be
 matched as a substring.
-450        """
-451        conditions = self._get_conditions(match_criteria, exact_match)
-452        try:
-453            self.cursor.execute(f"delete from [{table}] where
+451        """
+452        conditions = self._get_conditions(match_criteria, exact_match)
+453        try:
+454            self.cursor.execute(f"delete from [{table}] where
 {conditions};")
-454            num_deletions = self.cursor.rowcount
-455            self.logger.info(
-456                f'Deleted {num_deletions} rows from "{table}" where
+455            num_deletions = self.cursor.rowcount
+456            self.logger.info(
+457                f'Deleted {num_deletions} rows from "{table}" where
 {conditions}".'
-457            )
-458            return num_deletions
-459        except Exception as e:
-460            self.logger.debug(
-461                f'Error deleting rows from "{table}" where {conditions}.\n
+458            )
+459            return num_deletions
+460        except Exception as e:
+461            self.logger.debug(
+462                f'Error deleting rows from "{table}" where {conditions}.\n
 {e}'
-462            )
-463            return 0
+463            )
+464            return 0
 Delete records from table.
 Returns the number of deleted records.
 *** :params: ***
 match_criteria: Can be a list of 2-tuples where each tuple is (column_name,
 value) or a dictionary where keys are column names and values are corresponding
 values.
 exact_match: If False, the value for a given column will be matched as a
@@ -1809,249 +1770,209 @@
 def update(
 self,
 table: str,
 column_to_update: str,
 new_value: Any,
 match_criteria: list[tuple] | dict | None = None,
 exact_match: bool = True) -> int: View Source
-465    @_connect
-466    def update(
-467        self,
-468        table: str,
-469        column_to_update: str,
-470        new_value: Any,
-471        match_criteria: list[tuple] | dict | None = None,
-472        exact_match: bool = True,
-473    ) -> int:
-474        """Update the value in `column_to_update` to `new_value` for rows
+466    @_connect
+467    def update(
+468        self,
+469        table: str,
+470        column_to_update: str,
+471        new_value: Any,
+472        match_criteria: list[tuple] | dict | None = None,
+473        exact_match: bool = True,
+474    ) -> int:
+475        """Update the value in `column_to_update` to `new_value` for rows
 matched with `match_criteria`.
-475
-476        #### :params:
-477
-478        `table`: The table to update rows in.
-479
-480        `column_to_update`: The column to be updated in the matched rows.
-481
-482        `new_value`: The new value to insert.
-483
-484        `match_criteria`: Can be a list of 2-tuples where each tuple is `
+476
+477        #### :params:
+478
+479        `table`: The table to update rows in.
+480
+481        `column_to_update`: The column to be updated in the matched rows.
+482
+483        `new_value`: The new value to insert.
+484
+485        `match_criteria`: Can be a list of 2-tuples where each tuple is `
 (columnName, rowValue)`
-485        or a dictionary where keys are column names and values are
+486        or a dictionary where keys are column names and values are
 corresponding values.
-486        If `None`, every row in `table` will be updated.
-487
-488        `exact_match`: If `False`, `match_criteria` values will be treated
+487        If `None`, every row in `table` will be updated.
+488
+489        `exact_match`: If `False`, `match_criteria` values will be treated
 as substrings.
-489
-490        Returns the number of updated rows."""
-491        query = f"update [{table}] set {column_to_update} = ?"
-492        conditions = ""
-493        if match_criteria:
-494            conditions = self._get_conditions(match_criteria, exact_match)
-495            query += f" where {conditions}"
-496        else:
-497            conditions = None
-498        query += ";"
-499        try:
-500            self.cursor.execute(
-501                query,
-502                (new_value,),
-503            )
-504            num_updates = self.cursor.rowcount
-505            self.logger.info(
-506                f'In {num_updates} rows, updated "{column_to_update}" in "
+490
+491        Returns the number of updated rows."""
+492        query = f"update [{table}] set {column_to_update} = ?"
+493        conditions = ""
+494        if match_criteria:
+495            conditions = self._get_conditions(match_criteria, exact_match)
+496            query += f" where {conditions}"
+497        else:
+498            conditions = None
+499        query += ";"
+500        try:
+501            self.cursor.execute(
+502                query,
+503                (new_value,),
+504            )
+505            num_updates = self.cursor.rowcount
+506            self.logger.info(
+507                f'In {num_updates} rows, updated "{column_to_update}" in "
 {table}" table to "{new_value}" where {conditions}'
-507            )
-508            return num_updates
-509        except Exception as e:
-510            self.logger.error(
-511                f'Failed to update "{column_to_update}" in "{table}" table
+508            )
+509            return num_updates
+510        except Exception as e:
+511            self.logger.error(
+512                f'Failed to update "{column_to_update}" in "{table}" table
 to "{new_value}" where {conditions}"\n{e}'
-512            )
-513            return 0
+513            )
+514            return 0
 Update the value in column_to_update to new_value for rows matched with
 match_criteria.
 *** :params: ***
 table: The table to update rows in.
 column_to_update: The column to be updated in the matched rows.
 new_value: The new value to insert.
 match_criteria: Can be a list of 2-tuples where each tuple is (columnName,
 rowValue) or a dictionary where keys are column names and values are
 corresponding values. If None, every row in table will be updated.
 exact_match: If False, match_criteria values will be treated as substrings.
 Returns the number of updated rows.
 ⁰
 def drop_table(self, table: str) -> bool: View Source
-515    @_connect
-516    def drop_table(self, table: str) -> bool:
-517        """Drop `table` from the database.
-518
-519        Returns `True` if successful, `False` if not."""
-520        try:
-521            self.cursor.execute(f"drop Table [{table}];")
-522            self.logger.info(f'Dropped table "{table}"')
-523            return True
-524        except Exception as e:
-525            print(e)
-526            self.logger.error(f'Failed to drop table "{table}"')
-527            return False
+516    @_connect
+517    def drop_table(self, table: str) -> bool:
+518        """Drop `table` from the database.
+519
+520        Returns `True` if successful, `False` if not."""
+521        try:
+522            self.cursor.execute(f"drop Table [{table}];")
+523            self.logger.info(f'Dropped table "{table}"')
+524            return True
+525        except Exception as e:
+526            print(e)
+527            self.logger.error(f'Failed to drop table "{table}"')
+528            return False
 Drop table from the database.
 Returns True if successful, False if not.
 ⁰
 def add_column(
 self,
 table: str,
 column: str,
 _type: str,
 default_value: str | None = None): View Source
-529    @_connect
-530    def add_column(
-531        self, table: str, column: str, _type: str, default_value: str | None
+530    @_connect
+531    def add_column(
+532        self, table: str, column: str, _type: str, default_value: str | None
 = None
-532    ):
-533        """Add a new column to `table`.
-534
-535        #### :params:
-536
-537        `column`: Name of the column to add.
-538
-539        `_type`: The data type of the new column.
-540
-541        `default_value`: Optional default value for the column."""
-542        try:
-543            if default_value:
-544                self.cursor.execute(
-545                    f"alter table [{table}] add column {column} {_type}
+533    ):
+534        """Add a new column to `table`.
+535
+536        #### :params:
+537
+538        `column`: Name of the column to add.
+539
+540        `_type`: The data type of the new column.
+541
+542        `default_value`: Optional default value for the column."""
+543        try:
+544            if default_value:
+545                self.cursor.execute(
+546                    f"alter table [{table}] add column {column} {_type}
 default {default_value};"
-546                )
-547                self.update(table, column, default_value)
-548            else:
-549                self.cursor.execute(
-550                    f"alter table [{table}] add column {column} {_type};"
-551                )
-552            self.logger.info(f'Added column "{column}" to "{table}" table.')
-553        except Exception as e:
-554            self.logger.error(f'Failed to add column "{column}" to "{table}"
+547                )
+548                self.update(table, column, default_value)
+549            else:
+550                self.cursor.execute(
+551                    f"alter table [{table}] add column {column} {_type};"
+552                )
+553            self.logger.info(f'Added column "{column}" to "{table}" table.')
+554        except Exception as e:
+555            self.logger.error(f'Failed to add column "{column}" to "{table}"
 table.')
 Add a new column to table.
 *** :params: ***
 column: Name of the column to add.
 _type: The data type of the new column.
 default_value: Optional default value for the column.
 ⁰
 @staticmethod
 def data_to_string(
 data: list[dict],
 sort_key: str | None = None,
 wrap_to_terminal: bool = True) -> str: View Source
-556    @staticmethod
-557    def data_to_string(
-558        data: list[dict], sort_key: str | None = None, wrap_to_terminal:
+557    @staticmethod
+558    def data_to_string(
+559        data: list[dict], sort_key: str | None = None, wrap_to_terminal:
 bool = True
-559    ) -> str:
-560        """Uses tabulate to produce pretty string output from a list of
+560    ) -> str:
+561        """Uses tabulate to produce pretty string output from a list of
 dictionaries.
-561
-562        #### :params:
-563
-564        `data`: The list of dictionaries to create a grid from.
-565        Assumes all dictionaries in list have the same set of keys.
-566
-567        `sort_key`: Optional dictionary key to sort data with.
-568
-569        `wrap_to_terminal`: If `True`, the table width will be wrapped to
+562
+563        #### :params:
+564
+565        `data`: The list of dictionaries to create a grid from.
+566        Assumes all dictionaries in list have the same set of keys.
+567
+568        `sort_key`: Optional dictionary key to sort data with.
+569
+570        `wrap_to_terminal`: If `True`, the table width will be wrapped to
 fit within the current terminal window.
-570        Pass as `False` if the output is going into something like a `.txt`
+571        Pass as `False` if the output is going into something like a `.txt`
 file."""
-571        return data_to_string(data, sort_key, wrap_to_terminal)
+572        return data_to_string(data, sort_key, wrap_to_terminal)
 Uses tabulate to produce pretty string output from a list of dictionaries.
 *** :params: ***
 data: The list of dictionaries to create a grid from. Assumes all dictionaries
 in list have the same set of keys.
 sort_key: Optional dictionary key to sort data with.
 wrap_to_terminal: If True, the table width will be wrapped to fit within the
 current terminal window. Pass as False if the output is going into something
 like a .txt file.
   ⁰
 def data_to_string(
 data: list[dict],
 sort_key: str | None = None,
 wrap_to_terminal: bool = True) -> str: View Source
-574def data_to_string(
-575    data: list[dict], sort_key: str | None = None, wrap_to_terminal: bool =
+575def data_to_string(
+576    data: list[dict], sort_key: str | None = None, wrap_to_terminal: bool =
 True
-576) -> str:
-577    """Uses tabulate to produce pretty string output from a list of
+577) -> str:
+578    """Uses tabulate to produce pretty string output from a list of
 dictionaries.
-578
-579    #### :params:
-580
-581    `data`: The list of dictionaries to create a grid from.
-582    Assumes all dictionaries in list have the same set of keys.
-583
-584    `sort_key`: Optional dictionary key to sort data with.
-585
-586    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit
+579
+580    #### :params:
+581
+582    `data`: The list of dictionaries to create a grid from.
+583    Assumes all dictionaries in list have the same set of keys.
+584
+585    `sort_key`: Optional dictionary key to sort data with.
+586
+587    `wrap_to_terminal`: If `True`, the table width will be wrapped to fit
 within the current terminal window.
-587    Pass as `False` if the output is going into something like a `.txt`
+588    Pass as `False` if the output is going into something like a `.txt`
 file."""
-588    if len(data) == 0:
-589        return ""
-590    if sort_key:
-591        data = sorted(data, key=lambda d: d[sort_key])
-592    for i, d in enumerate(data):
-593        for k in d:
-594            data[i][k] = str(data[i][k])
-595
-596    too_wide = True
-597    terminal_width = os.get_terminal_size().columns
-598    max_col_widths = terminal_width
-599    # Make an output with effectively unrestricted column widths
-600    # to see if shrinking is necessary
-601    output = tabulate(
-602        data,
-603        headers="keys",
-604        disable_numparse=True,
-605        tablefmt="grid",
-606        maxcolwidths=max_col_widths,
-607    )
-608    current_width = output.index("\n")
-609    if current_width < terminal_width:
-610        too_wide = False
-611    if wrap_to_terminal and too_wide:
-612        print("Resizing grid to fit within the terminal...\n")
-613        previous_col_widths = max_col_widths
-614        acceptable_width = terminal_width - 10
-615        while too_wide and max_col_widths > 1:
-616            if current_width >= terminal_width:
-617                previous_col_widths = max_col_widths
-618                max_col_widths = int(max_col_widths * 0.5)
-619            elif current_width < terminal_width:
-620                # Without lowering acceptable_width, this condition will
-cause infinite loop
-621                if max_col_widths == previous_col_widths - 1:
-622                    acceptable_width -= 10
-623                max_col_widths = int(
-624                    max_col_widths + (0.5 * (previous_col_widths -
-max_col_widths))
-625                )
-626            output = tabulate(
-627                data,
-628                headers="keys",
-629                disable_numparse=True,
-630                tablefmt="grid",
-631                maxcolwidths=max_col_widths,
-632            )
-633            current_width = output.index("\n")
-634            if acceptable_width < current_width < terminal_width:
-635                too_wide = False
-636        if too_wide:
-637            print("Couldn't resize grid to fit within the terminal.")
-638            return str(data)
-639    return output
+589    if len(data) == 0:
+590        return ""
+591    if sort_key:
+592        data = sorted(data, key=lambda d: d[sort_key])
+593    for i, d in enumerate(data):
+594        for k in d:
+595            data[i][k] = str(data[i][k])
+596
+597    try:
+598        print("Resizing grid to fit within the terminal...\n")
+599        return griddy(data, "keys", wrap_to_terminal)
+600    except RuntimeError as e:
+601        print(e)
+602        return str(data)
 Uses tabulate to produce pretty string output from a list of dictionaries.
 *** :params: ***
 data: The list of dictionaries to create a grid from. Assumes all dictionaries
 in list have the same set of keys.
 sort_key: Optional dictionary key to sort data with.
 wrap_to_terminal: If True, the table width will be wrapped to fit within the
 current terminal window. Pass as False if the output is going into something
```

### Comparing `databased-2.2.1/docs/databased/dbparsers.html` & `databased-2.3.0/docs/databased/dbparsers.html`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/docs/databased/dbshell.html` & `databased-2.3.0/docs/databased/dbshell.html`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/src/databased/customshell.py` & `databased-2.3.0/src/databased/customshell.py`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/src/databased/databased.py` & `databased-2.3.0/src/databased/databased.py`

 * *Files 5% similar despite different names*

```diff
@@ -2,14 +2,15 @@
 import os
 import sqlite3
 from datetime import datetime
 from functools import wraps
 from typing import Any
 
 import pandas
+from griddle import griddy
 from pathier import Pathier
 from tabulate import tabulate
 
 
 def _connect(func):
     """Decorator to open db connection if it isn't already open."""
 
@@ -588,51 +589,13 @@
         return ""
     if sort_key:
         data = sorted(data, key=lambda d: d[sort_key])
     for i, d in enumerate(data):
         for k in d:
             data[i][k] = str(data[i][k])
 
-    too_wide = True
-    terminal_width = os.get_terminal_size().columns
-    max_col_widths = terminal_width
-    # Make an output with effectively unrestricted column widths
-    # to see if shrinking is necessary
-    output = tabulate(
-        data,
-        headers="keys",
-        disable_numparse=True,
-        tablefmt="grid",
-        maxcolwidths=max_col_widths,
-    )
-    current_width = output.index("\n")
-    if current_width < terminal_width:
-        too_wide = False
-    if wrap_to_terminal and too_wide:
+    try:
         print("Resizing grid to fit within the terminal...\n")
-        previous_col_widths = max_col_widths
-        acceptable_width = terminal_width - 10
-        while too_wide and max_col_widths > 1:
-            if current_width >= terminal_width:
-                previous_col_widths = max_col_widths
-                max_col_widths = int(max_col_widths * 0.5)
-            elif current_width < terminal_width:
-                # Without lowering acceptable_width, this condition will cause infinite loop
-                if max_col_widths == previous_col_widths - 1:
-                    acceptable_width -= 10
-                max_col_widths = int(
-                    max_col_widths + (0.5 * (previous_col_widths - max_col_widths))
-                )
-            output = tabulate(
-                data,
-                headers="keys",
-                disable_numparse=True,
-                tablefmt="grid",
-                maxcolwidths=max_col_widths,
-            )
-            current_width = output.index("\n")
-            if acceptable_width < current_width < terminal_width:
-                too_wide = False
-        if too_wide:
-            print("Couldn't resize grid to fit within the terminal.")
-            return str(data)
-    return output
+        return griddy(data, "keys", wrap_to_terminal)
+    except RuntimeError as e:
+        print(e)
+        return str(data)
```

### Comparing `databased-2.2.1/src/databased/dbparsers.py` & `databased-2.3.0/src/databased/dbparsers.py`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/src/databased/dbshell.py` & `databased-2.3.0/src/databased/dbshell.py`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/LICENSE.txt` & `databased-2.3.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/README.md` & `databased-2.3.0/README.md`

 * *Files identical despite different names*

### Comparing `databased-2.2.1/pyproject.toml` & `databased-2.3.0/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "databased"
 authors = [{name="Matt Manes"}]
 description = "Wrapper for the standard library Sqlite3 module to make setting up and using a database quicker and easier."
-version = "2.2.1"
+version = "2.3.0"
 requires-python = ">=3.10"
-dependencies = ["pandas", "tabulate", "pytest", "argshell", "pathier"]
+dependencies = ["pandas", "tabulate", "pytest", "argshell", "pathier", "griddle"]
 readme = "README.md"
 keywords = [
     "database",
     "sqlite",
     "sqlite3"
 ]
 classifiers = [
```

### Comparing `databased-2.2.1/PKG-INFO` & `databased-2.3.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 Metadata-Version: 2.1
 Name: databased
-Version: 2.2.1
+Version: 2.3.0
 Summary: Wrapper for the standard library Sqlite3 module to make setting up and using a database quicker and easier.
 Project-URL: Homepage, https://github.com/matt-manes/databased
 Project-URL: Documentation, https://github.com/matt-manes/databased/tree/main/docs
 Project-URL: Source code, https://github.com/matt-manes/databased/tree/main/src/databased
 Author: Matt Manes
 License-File: LICENSE.txt
 Keywords: database,sqlite,sqlite3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.10
 Requires-Dist: argshell
+Requires-Dist: griddle
 Requires-Dist: pandas
 Requires-Dist: pathier
 Requires-Dist: pytest
 Requires-Dist: tabulate
 Description-Content-Type: text/markdown
 
 # Databased
```

