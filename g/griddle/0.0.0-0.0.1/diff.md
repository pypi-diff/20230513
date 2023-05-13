# Comparing `tmp/griddle-0.0.0.tar.gz` & `tmp/griddle-0.0.1.tar.gz`

## Comparing `griddle-0.0.0.tar` & `griddle-0.0.1.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0    59547 2020-02-02 00:00:00.000000 griddle-0.0.0/docs/griddle.html
--rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 griddle-0.0.0/docs/index.html
--rw-r--r--   0        0        0    22856 2020-02-02 00:00:00.000000 griddle-0.0.0/docs/search.js
--rw-r--r--   0        0        0     2890 2020-02-02 00:00:00.000000 griddle-0.0.0/src/griddle/__init__.py
--rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 griddle-0.0.0/.gitignore
--rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 griddle-0.0.0/LICENSE.txt
--rw-r--r--   0        0        0     1493 2020-02-02 00:00:00.000000 griddle-0.0.0/README.md
--rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 griddle-0.0.0/pyproject.toml
--rw-r--r--   0        0        0     2203 2020-02-02 00:00:00.000000 griddle-0.0.0/PKG-INFO
+-rw-r--r--   0        0        0    59523 2020-02-02 00:00:00.000000 griddle-0.0.1/docs/griddle.html
+-rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 griddle-0.0.1/docs/index.html
+-rw-r--r--   0        0        0    22848 2020-02-02 00:00:00.000000 griddle-0.0.1/docs/search.js
+-rw-r--r--   0        0        0     2882 2020-02-02 00:00:00.000000 griddle-0.0.1/src/griddle/__init__.py
+-rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 griddle-0.0.1/.gitignore
+-rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 griddle-0.0.1/LICENSE.txt
+-rw-r--r--   0        0        0     1493 2020-02-02 00:00:00.000000 griddle-0.0.1/README.md
+-rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 griddle-0.0.1/pyproject.toml
+-rw-r--r--   0        0        0     2203 2020-02-02 00:00:00.000000 griddle-0.0.1/PKG-INFO
```

### Comparing `griddle-0.0.0/docs/griddle.html` & `griddle-0.0.1/docs/griddle.html`

 * *Files 0% similar despite different names*

```diff
@@ -54,15 +54,15 @@
 </span><span id="L-5"><a href="#L-5"><span class="linenos"> 5</span></a>
 </span><span id="L-6"><a href="#L-6"><span class="linenos"> 6</span></a>
 </span><span id="L-7"><a href="#L-7"><span class="linenos"> 7</span></a><span class="k">def</span> <span class="nf">griddy</span><span class="p">(</span>
 </span><span id="L-8"><a href="#L-8"><span class="linenos"> 8</span></a>    <span class="n">data</span><span class="p">:</span> <span class="n">Mapping</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]]</span> <span class="o">|</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span>
 </span><span id="L-9"><a href="#L-9"><span class="linenos"> 9</span></a>    <span class="n">headers</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="n">Sequence</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">(),</span>
 </span><span id="L-10"><a href="#L-10"><span class="linenos">10</span></a>    <span class="n">shrink_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
 </span><span id="L-11"><a href="#L-11"><span class="linenos">11</span></a>    <span class="n">margin</span><span class="p">:</span> <span class="nb">int</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
-</span><span id="L-12"><a href="#L-12"><span class="linenos">12</span></a>    <span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;rounded_grid&quot;</span><span class="p">,</span>
+</span><span id="L-12"><a href="#L-12"><span class="linenos">12</span></a>    <span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;grid&quot;</span><span class="p">,</span>
 </span><span id="L-13"><a href="#L-13"><span class="linenos">13</span></a>    <span class="n">disable_numparse</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
 </span><span id="L-14"><a href="#L-14"><span class="linenos">14</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
 </span><span id="L-15"><a href="#L-15"><span class="linenos">15</span></a>    <span class="sd">&quot;&quot;&quot;Convert `data` into a formatted string grid representation.</span>
 </span><span id="L-16"><a href="#L-16"><span class="linenos">16</span></a>
 </span><span id="L-17"><a href="#L-17"><span class="linenos">17</span></a><span class="sd">    #### :params:</span>
 </span><span id="L-18"><a href="#L-18"><span class="linenos">18</span></a>
 </span><span id="L-19"><a href="#L-19"><span class="linenos">19</span></a><span class="sd">    * `headers`: Can either be an explicit list of column names, `&quot;keys&quot;`, or `&quot;firstrow&quot;`.</span>
@@ -127,26 +127,26 @@
 
             </section>
                 <section id="griddy">
                             <input id="griddy-view-source" class="view-source-toggle-state" type="checkbox" aria-hidden="true" tabindex="-1">
 <div class="attr function">
             
         <span class="def">def</span>
-        <span class="name">griddy</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="n">data</span><span class="p">:</span> <span class="n">Union</span><span class="p">[</span><span class="n">Mapping</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]]]</span>,</span><span class="param">	<span class="n">headers</span><span class="p">:</span> <span class="n">Union</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">dict</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">str</span><span class="p">],</span> <span class="n">Sequence</span><span class="p">[</span><span class="nb">str</span><span class="p">]]</span> <span class="o">=</span> <span class="p">()</span>,</span><span class="param">	<span class="n">shrink_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>,</span><span class="param">	<span class="n">margin</span><span class="p">:</span> <span class="nb">int</span> <span class="o">=</span> <span class="mi">10</span>,</span><span class="param">	<span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s1">&#39;rounded_grid&#39;</span>,</span><span class="param">	<span class="n">disable_numparse</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">str</span>:</span></span>
+        <span class="name">griddy</span><span class="signature pdoc-code multiline">(<span class="param">	<span class="n">data</span><span class="p">:</span> <span class="n">Union</span><span class="p">[</span><span class="n">Mapping</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]]]</span>,</span><span class="param">	<span class="n">headers</span><span class="p">:</span> <span class="n">Union</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">dict</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">str</span><span class="p">],</span> <span class="n">Sequence</span><span class="p">[</span><span class="nb">str</span><span class="p">]]</span> <span class="o">=</span> <span class="p">()</span>,</span><span class="param">	<span class="n">shrink_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span>,</span><span class="param">	<span class="n">margin</span><span class="p">:</span> <span class="nb">int</span> <span class="o">=</span> <span class="mi">10</span>,</span><span class="param">	<span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s1">&#39;grid&#39;</span>,</span><span class="param">	<span class="n">disable_numparse</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span></span><span class="return-annotation">) -> <span class="nb">str</span>:</span></span>
 
                 <label class="view-source-button" for="griddy-view-source"><span>View Source</span></label>
 
     </div>
     <a class="headerlink" href="#griddy"></a>
             <div class="pdoc-code codehilite"><pre><span></span><span id="griddy-8"><a href="#griddy-8"><span class="linenos"> 8</span></a><span class="k">def</span> <span class="nf">griddy</span><span class="p">(</span>
 </span><span id="griddy-9"><a href="#griddy-9"><span class="linenos"> 9</span></a>    <span class="n">data</span><span class="p">:</span> <span class="n">Mapping</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]]</span> <span class="o">|</span> <span class="n">Iterable</span><span class="p">[</span><span class="n">Iterable</span><span class="p">[</span><span class="n">Any</span><span class="p">]],</span>
 </span><span id="griddy-10"><a href="#griddy-10"><span class="linenos">10</span></a>    <span class="n">headers</span><span class="p">:</span> <span class="nb">str</span> <span class="o">|</span> <span class="nb">dict</span><span class="p">[</span><span class="nb">str</span><span class="p">,</span> <span class="nb">str</span><span class="p">]</span> <span class="o">|</span> <span class="n">Sequence</span><span class="p">[</span><span class="nb">str</span><span class="p">]</span> <span class="o">=</span> <span class="p">(),</span>
 </span><span id="griddy-11"><a href="#griddy-11"><span class="linenos">11</span></a>    <span class="n">shrink_to_terminal</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
 </span><span id="griddy-12"><a href="#griddy-12"><span class="linenos">12</span></a>    <span class="n">margin</span><span class="p">:</span> <span class="nb">int</span> <span class="o">=</span> <span class="mi">10</span><span class="p">,</span>
-</span><span id="griddy-13"><a href="#griddy-13"><span class="linenos">13</span></a>    <span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;rounded_grid&quot;</span><span class="p">,</span>
+</span><span id="griddy-13"><a href="#griddy-13"><span class="linenos">13</span></a>    <span class="n">table_format</span><span class="p">:</span> <span class="nb">str</span> <span class="o">=</span> <span class="s2">&quot;grid&quot;</span><span class="p">,</span>
 </span><span id="griddy-14"><a href="#griddy-14"><span class="linenos">14</span></a>    <span class="n">disable_numparse</span><span class="p">:</span> <span class="nb">bool</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span>
 </span><span id="griddy-15"><a href="#griddy-15"><span class="linenos">15</span></a><span class="p">)</span> <span class="o">-&gt;</span> <span class="nb">str</span><span class="p">:</span>
 </span><span id="griddy-16"><a href="#griddy-16"><span class="linenos">16</span></a>    <span class="sd">&quot;&quot;&quot;Convert `data` into a formatted string grid representation.</span>
 </span><span id="griddy-17"><a href="#griddy-17"><span class="linenos">17</span></a>
 </span><span id="griddy-18"><a href="#griddy-18"><span class="linenos">18</span></a><span class="sd">    #### :params:</span>
 </span><span id="griddy-19"><a href="#griddy-19"><span class="linenos">19</span></a>
 </span><span id="griddy-20"><a href="#griddy-20"><span class="linenos">20</span></a><span class="sd">    * `headers`: Can either be an explicit list of column names, `&quot;keys&quot;`, or `&quot;firstrow&quot;`.</span>
```

#### html2text {}

```diff
@@ -14,15 +14,15 @@
 _5
 _6
 _7def griddy(
 _8    data: Mapping[str, Iterable[Any]] | Iterable[Iterable[Any]],
 _9    headers: str | dict[str, str] | Sequence[str] = (),
 10    shrink_to_terminal: bool = True,
 11    margin: int = 10,
-12    table_format: str = "rounded_grid",
+12    table_format: str = "grid",
 13    disable_numparse: bool = True,
 14) -> str:
 15    """Convert `data` into a formatted string grid representation.
 16
 17    #### :params:
 18
 19    * `headers`: Can either be an explicit list of column names, `"keys"`, or
@@ -94,22 +94,22 @@
 /.")
   ⁰
 def griddy(
 data: Union[Mapping[str, Iterable[Any]], Iterable[Iterable[Any]]],
 headers: Union[str, dict[str, str], Sequence[str]] = (),
 shrink_to_terminal: bool = True,
 margin: int = 10,
-table_format: str = 'rounded_grid',
+table_format: str = 'grid',
 disable_numparse: bool = True) -> str: View Source
 _8def griddy(
 _9    data: Mapping[str, Iterable[Any]] | Iterable[Iterable[Any]],
 10    headers: str | dict[str, str] | Sequence[str] = (),
 11    shrink_to_terminal: bool = True,
 12    margin: int = 10,
-13    table_format: str = "rounded_grid",
+13    table_format: str = "grid",
 14    disable_numparse: bool = True,
 15) -> str:
 16    """Convert `data` into a formatted string grid representation.
 17
 18    #### :params:
 19
 20    * `headers`: Can either be an explicit list of column names, `"keys"`, or
```

### Comparing `griddle-0.0.0/docs/search.js` & `griddle-0.0.1/docs/search.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -689,15 +689,15 @@
         "doc": "<p></p>\n"
     }, {
         "fullname": "griddle.griddy",
         "modulename": "griddle",
         "qualname": "griddy",
         "kind": "function",
         "doc": "<p>Convert <code>data</code> into a formatted string grid representation.</p>\n\n<h4 id=\"params\">:params:</h4>\n\n<ul>\n<li><p><code>headers</code>: Can either be an explicit list of column names, <code>\"keys\"</code>, or <code>\"firstrow\"</code>.\nIf not given, the grid will have no headers.</p></li>\n<li><p><code>shrink_to_terminal</code>: When <code>True</code>, <code>griddy</code> will limit column widths so that the total width of the output will fit within the terminal.</p></li>\n<li><p><code>margin</code>: When shrinking to the terminal, <code>griddy</code> will try to maximize the output width such that <code>terminal_width - margin &lt; output_width &lt; terminal_width</code>.\nThe larger this value, the larger the acceptable output width and, likely, the faster this function will return.\nNote: <code>griddy</code> will, internally, increase the margin when necessary to avoid getting stuck in an infinite loop.</p></li>\n<li><p><code>table_format</code>: The grid asthetic. See the <code>tabulate</code> package for a full list of options.</p></li>\n<li><p><code>disable_numparse</code>: Turn off treating and aligning numbers differently from non-numbers.</p></li>\n</ul>\n",
-        "signature": "<span class=\"signature pdoc-code multiline\">(<span class=\"param\">\t<span class=\"n\">data</span><span class=\"p\">:</span> <span class=\"n\">Union</span><span class=\"p\">[</span><span class=\"n\">Mapping</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Any</span><span class=\"p\">]],</span> <span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Any</span><span class=\"p\">]]]</span>,</span><span class=\"param\">\t<span class=\"n\">headers</span><span class=\"p\">:</span> <span class=\"n\">Union</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"nb\">dict</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"nb\">str</span><span class=\"p\">],</span> <span class=\"n\">Sequence</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">]]</span> <span class=\"o\">=</span> <span class=\"p\">()</span>,</span><span class=\"param\">\t<span class=\"n\">shrink_to_terminal</span><span class=\"p\">:</span> <span class=\"nb\">bool</span> <span class=\"o\">=</span> <span class=\"kc\">True</span>,</span><span class=\"param\">\t<span class=\"n\">margin</span><span class=\"p\">:</span> <span class=\"nb\">int</span> <span class=\"o\">=</span> <span class=\"mi\">10</span>,</span><span class=\"param\">\t<span class=\"n\">table_format</span><span class=\"p\">:</span> <span class=\"nb\">str</span> <span class=\"o\">=</span> <span class=\"s1\">&#39;rounded_grid&#39;</span>,</span><span class=\"param\">\t<span class=\"n\">disable_numparse</span><span class=\"p\">:</span> <span class=\"nb\">bool</span> <span class=\"o\">=</span> <span class=\"kc\">True</span></span><span class=\"return-annotation\">) -> <span class=\"nb\">str</span>:</span></span>",
+        "signature": "<span class=\"signature pdoc-code multiline\">(<span class=\"param\">\t<span class=\"n\">data</span><span class=\"p\">:</span> <span class=\"n\">Union</span><span class=\"p\">[</span><span class=\"n\">Mapping</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Any</span><span class=\"p\">]],</span> <span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Iterable</span><span class=\"p\">[</span><span class=\"n\">Any</span><span class=\"p\">]]]</span>,</span><span class=\"param\">\t<span class=\"n\">headers</span><span class=\"p\">:</span> <span class=\"n\">Union</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"nb\">dict</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">,</span> <span class=\"nb\">str</span><span class=\"p\">],</span> <span class=\"n\">Sequence</span><span class=\"p\">[</span><span class=\"nb\">str</span><span class=\"p\">]]</span> <span class=\"o\">=</span> <span class=\"p\">()</span>,</span><span class=\"param\">\t<span class=\"n\">shrink_to_terminal</span><span class=\"p\">:</span> <span class=\"nb\">bool</span> <span class=\"o\">=</span> <span class=\"kc\">True</span>,</span><span class=\"param\">\t<span class=\"n\">margin</span><span class=\"p\">:</span> <span class=\"nb\">int</span> <span class=\"o\">=</span> <span class=\"mi\">10</span>,</span><span class=\"param\">\t<span class=\"n\">table_format</span><span class=\"p\">:</span> <span class=\"nb\">str</span> <span class=\"o\">=</span> <span class=\"s1\">&#39;grid&#39;</span>,</span><span class=\"param\">\t<span class=\"n\">disable_numparse</span><span class=\"p\">:</span> <span class=\"nb\">bool</span> <span class=\"o\">=</span> <span class=\"kc\">True</span></span><span class=\"return-annotation\">) -> <span class=\"nb\">str</span>:</span></span>",
         "funcdef": "def"
     }];
 
     // mirrored in build-search-index.js (part 1)
     // Also split on html tags. this is a cheap heuristic, but good enough.
     elasticlunr.tokenizer.setSeperator(/[\s\-.;&_'"=,()]+|<[^>]*>/);
```

### Comparing `griddle-0.0.0/src/griddle/__init__.py` & `griddle-0.0.1/src/griddle/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 
 
 def griddy(
     data: Mapping[str, Iterable[Any]] | Iterable[Iterable[Any]],
     headers: str | dict[str, str] | Sequence[str] = (),
     shrink_to_terminal: bool = True,
     margin: int = 10,
-    table_format: str = "rounded_grid",
+    table_format: str = "grid",
     disable_numparse: bool = True,
 ) -> str:
     """Convert `data` into a formatted string grid representation.
 
     #### :params:
 
     * `headers`: Can either be an explicit list of column names, `"keys"`, or `"firstrow"`.
```

### Comparing `griddle-0.0.0/LICENSE.txt` & `griddle-0.0.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `griddle-0.0.0/README.md` & `griddle-0.0.1/README.md`

 * *Files identical despite different names*

### Comparing `griddle-0.0.0/pyproject.toml` & `griddle-0.0.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 00000090: 6f20 6120 7072 696e 7461 626c 6520 6772  o a printable gr
 000000a0: 6964 2077 6974 6820 6479 6e61 6d69 6361  id with dynamica
 000000b0: 6c6c 7920 636f 6e74 726f 6c6c 6564 2063  lly controlled c
 000000c0: 6f6c 756d 6e20 7369 7a65 7320 746f 2073  olumn sizes to s
 000000d0: 6872 696e 6b20 6772 6964 2077 6964 7468  hrink grid width
 000000e0: 2074 6f20 796f 7572 2074 6572 6d69 6e61   to your termina
 000000f0: 6c20 7369 7a65 2e22 0d0a 7665 7273 696f  l size."..versio
-00000100: 6e20 3d20 2230 2e30 2e30 220d 0a72 6571  n = "0.0.0"..req
+00000100: 6e20 3d20 2230 2e30 2e31 220d 0a72 6571  n = "0.0.1"..req
 00000110: 7569 7265 732d 7079 7468 6f6e 203d 2022  uires-python = "
 00000120: 3e3d 332e 3130 220d 0a64 6570 656e 6465  >=3.10"..depende
 00000130: 6e63 6965 7320 3d20 5b22 7461 6275 6c61  ncies = ["tabula
 00000140: 7465 225d 0d0a 7265 6164 6d65 203d 2022  te"]..readme = "
 00000150: 5245 4144 4d45 2e6d 6422 0d0a 6b65 7977  README.md"..keyw
 00000160: 6f72 6473 203d 205b 2274 6162 756c 6174  ords = ["tabulat
 00000170: 6522 2c20 2267 7269 6422 2c20 2270 7269  e", "grid", "pri
```

### Comparing `griddle-0.0.0/PKG-INFO` & `griddle-0.0.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: griddle
-Version: 0.0.0
+Version: 0.0.1
 Summary: Turn an interable into a printable grid with dynamically controlled column sizes to shrink grid width to your terminal size.
 Project-URL: Homepage, https://github.com/matt-manes/griddle
 Project-URL: Documentation, https://github.com/matt-manes/griddle/tree/main/docs
 Project-URL: Source code, https://github.com/matt-manes/griddle/tree/main/src/griddle
 Author-email: Matt Manes <mattmanes@pm.me>
 License-File: LICENSE.txt
 Keywords: grid,print,tabulate,terminal
```

