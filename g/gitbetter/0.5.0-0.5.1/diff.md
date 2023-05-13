# Comparing `tmp/gitbetter-0.5.0.tar.gz` & `tmp/gitbetter-0.5.1.tar.gz`

## Comparing `gitbetter-0.5.0.tar` & `gitbetter-0.5.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0     1262 2020-02-02 00:00:00.000000 gitbetter-0.5.0/CHANGELOG.md
--rw-r--r--   0        0        0    34124 2020-02-02 00:00:00.000000 gitbetter-0.5.0/docs/gitbetter.html
--rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 gitbetter-0.5.0/docs/index.html
--rw-r--r--   0        0        0    57989 2020-02-02 00:00:00.000000 gitbetter-0.5.0/docs/search.js
--rw-r--r--   0        0        0   138209 2020-02-02 00:00:00.000000 gitbetter-0.5.0/docs/gitbetter/git.html
--rw-r--r--   0        0        0   248978 2020-02-02 00:00:00.000000 gitbetter-0.5.0/docs/gitbetter/gitbetter.html
--rw-r--r--   0        0        0       27 2020-02-02 00:00:00.000000 gitbetter-0.5.0/src/gitbetter/__init__.py
--rw-r--r--   0        0        0     5856 2020-02-02 00:00:00.000000 gitbetter-0.5.0/src/gitbetter/git.py
--rw-r--r--   0        0        0    10209 2020-02-02 00:00:00.000000 gitbetter-0.5.0/src/gitbetter/gitbetter.py
--rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 gitbetter-0.5.0/.gitignore
--rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 gitbetter-0.5.0/LICENSE.txt
--rw-r--r--   0        0        0     4173 2020-02-02 00:00:00.000000 gitbetter-0.5.0/README.md
--rw-r--r--   0        0        0     1117 2020-02-02 00:00:00.000000 gitbetter-0.5.0/pyproject.toml
--rw-r--r--   0        0        0     4786 2020-02-02 00:00:00.000000 gitbetter-0.5.0/PKG-INFO
+-rw-r--r--   0        0        0     1631 2020-02-02 00:00:00.000000 gitbetter-0.5.1/CHANGELOG.md
+-rw-r--r--   0        0        0    34124 2020-02-02 00:00:00.000000 gitbetter-0.5.1/docs/gitbetter.html
+-rw-r--r--   0        0        0      140 2020-02-02 00:00:00.000000 gitbetter-0.5.1/docs/index.html
+-rw-r--r--   0        0        0    57989 2020-02-02 00:00:00.000000 gitbetter-0.5.1/docs/search.js
+-rw-r--r--   0        0        0   138245 2020-02-02 00:00:00.000000 gitbetter-0.5.1/docs/gitbetter/git.html
+-rw-r--r--   0        0        0   248978 2020-02-02 00:00:00.000000 gitbetter-0.5.1/docs/gitbetter/gitbetter.html
+-rw-r--r--   0        0        0       27 2020-02-02 00:00:00.000000 gitbetter-0.5.1/src/gitbetter/__init__.py
+-rw-r--r--   0        0        0     5874 2020-02-02 00:00:00.000000 gitbetter-0.5.1/src/gitbetter/git.py
+-rw-r--r--   0        0        0    10209 2020-02-02 00:00:00.000000 gitbetter-0.5.1/src/gitbetter/gitbetter.py
+-rw-r--r--   0        0        0       46 2020-02-02 00:00:00.000000 gitbetter-0.5.1/.gitignore
+-rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 gitbetter-0.5.1/LICENSE.txt
+-rw-r--r--   0        0        0     4173 2020-02-02 00:00:00.000000 gitbetter-0.5.1/README.md
+-rw-r--r--   0        0        0     1117 2020-02-02 00:00:00.000000 gitbetter-0.5.1/pyproject.toml
+-rw-r--r--   0        0        0     4786 2020-02-02 00:00:00.000000 gitbetter-0.5.1/PKG-INFO
```

### Comparing `gitbetter-0.5.0/CHANGELOG.md` & `gitbetter-0.5.1/CHANGELOG.md`

 * *Files 7% similar despite different names*

```diff
@@ -1,14 +1,33 @@
 # Changelog
 
-## 0.4.0 (2023-05-04)
+## 0.5.0 (2023-05-11)
+
+#### New Features
+
+* add create_remote_from_cwd()
+#### Refactorings
+
+* rename do_list_branches() to do_branches()
+* do_new_gh_remote invokes create_remote_from_cwd so url no longer needs to be added manually after creating remote
+#### Docs
+
+* update readme
+* update doc string
+
+
+## v0.4.0 (2023-05-04)
 
 #### New Features
 
 * add status command
+#### Others
+
+* build v0.4.0
+* update changelog
 
 
 ## v0.3.0 (2023-05-02)
 
 #### Refactorings
 
 * remove do_cmd as it's now covered by parent class's do_sys
```

### Comparing `gitbetter-0.5.0/docs/gitbetter.html` & `gitbetter-0.5.1/docs/gitbetter.html`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/docs/search.js` & `gitbetter-0.5.1/docs/search.js`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/docs/gitbetter/git.html` & `gitbetter-0.5.1/docs/gitbetter/git.html`

 * *Files 0% similar despite different names*

```diff
@@ -312,15 +312,15 @@
 </span><span id="L-175"><a href="#L-175"><span class="linenos">175</span></a>    <span class="sd">&quot;&quot;&quot;Use GitHub CLI (must be installed and configured) to create a remote GitHub repo from</span>
 </span><span id="L-176"><a href="#L-176"><span class="linenos">176</span></a><span class="sd">    the current working directory repo and add its url as this repo&#39;s remote origin.</span>
 </span><span id="L-177"><a href="#L-177"><span class="linenos">177</span></a>
 </span><span id="L-178"><a href="#L-178"><span class="linenos">178</span></a><span class="sd">    #### :params:</span>
 </span><span id="L-179"><a href="#L-179"><span class="linenos">179</span></a>
 </span><span id="L-180"><a href="#L-180"><span class="linenos">180</span></a><span class="sd">    `public`: Create the GitHub repo as a public repo, default is to create it as private.&quot;&quot;&quot;</span>
 </span><span id="L-181"><a href="#L-181"><span class="linenos">181</span></a>    <span class="n">visibility</span> <span class="o">=</span> <span class="s2">&quot;public&quot;</span> <span class="k">if</span> <span class="n">public</span> <span class="k">else</span> <span class="s2">&quot;private&quot;</span>
-</span><span id="L-182"><a href="#L-182"><span class="linenos">182</span></a>    <span class="n">os</span><span class="o">.</span><span class="n">system</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;gh repo create --source . --</span><span class="si">{</span><span class="n">visibility</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="L-182"><a href="#L-182"><span class="linenos">182</span></a>    <span class="n">os</span><span class="o">.</span><span class="n">system</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;gh repo create --source=. --remote=upstream --</span><span class="si">{</span><span class="n">visibility</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
 </span><span id="L-183"><a href="#L-183"><span class="linenos">183</span></a>
 </span><span id="L-184"><a href="#L-184"><span class="linenos">184</span></a>
 </span><span id="L-185"><a href="#L-185"><span class="linenos">185</span></a><span class="k">def</span> <span class="nf">make_private</span><span class="p">(</span><span class="n">owner</span><span class="p">:</span> <span class="nb">str</span><span class="p">,</span> <span class="n">name</span><span class="p">:</span> <span class="nb">str</span><span class="p">):</span>
 </span><span id="L-186"><a href="#L-186"><span class="linenos">186</span></a>    <span class="sd">&quot;&quot;&quot;Uses GitHub CLI (must be installed and configured) to set the repo&#39;s visibility to private.</span>
 </span><span id="L-187"><a href="#L-187"><span class="linenos">187</span></a>
 </span><span id="L-188"><a href="#L-188"><span class="linenos">188</span></a><span class="sd">    #### :params:</span>
 </span><span id="L-189"><a href="#L-189"><span class="linenos">189</span></a>
@@ -989,15 +989,15 @@
 </span><span id="create_remote_from_cwd-176"><a href="#create_remote_from_cwd-176"><span class="linenos">176</span></a>    <span class="sd">&quot;&quot;&quot;Use GitHub CLI (must be installed and configured) to create a remote GitHub repo from</span>
 </span><span id="create_remote_from_cwd-177"><a href="#create_remote_from_cwd-177"><span class="linenos">177</span></a><span class="sd">    the current working directory repo and add its url as this repo&#39;s remote origin.</span>
 </span><span id="create_remote_from_cwd-178"><a href="#create_remote_from_cwd-178"><span class="linenos">178</span></a>
 </span><span id="create_remote_from_cwd-179"><a href="#create_remote_from_cwd-179"><span class="linenos">179</span></a><span class="sd">    #### :params:</span>
 </span><span id="create_remote_from_cwd-180"><a href="#create_remote_from_cwd-180"><span class="linenos">180</span></a>
 </span><span id="create_remote_from_cwd-181"><a href="#create_remote_from_cwd-181"><span class="linenos">181</span></a><span class="sd">    `public`: Create the GitHub repo as a public repo, default is to create it as private.&quot;&quot;&quot;</span>
 </span><span id="create_remote_from_cwd-182"><a href="#create_remote_from_cwd-182"><span class="linenos">182</span></a>    <span class="n">visibility</span> <span class="o">=</span> <span class="s2">&quot;public&quot;</span> <span class="k">if</span> <span class="n">public</span> <span class="k">else</span> <span class="s2">&quot;private&quot;</span>
-</span><span id="create_remote_from_cwd-183"><a href="#create_remote_from_cwd-183"><span class="linenos">183</span></a>    <span class="n">os</span><span class="o">.</span><span class="n">system</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;gh repo create --source . --</span><span class="si">{</span><span class="n">visibility</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
+</span><span id="create_remote_from_cwd-183"><a href="#create_remote_from_cwd-183"><span class="linenos">183</span></a>    <span class="n">os</span><span class="o">.</span><span class="n">system</span><span class="p">(</span><span class="sa">f</span><span class="s2">&quot;gh repo create --source=. --remote=upstream --</span><span class="si">{</span><span class="n">visibility</span><span class="si">}</span><span class="s2">&quot;</span><span class="p">)</span>
 </span></pre></div>
 
 
             <div class="docstring"><p>Use GitHub CLI (must be installed and configured) to create a remote GitHub repo from
 the current working directory repo and add its url as this repo's remote origin.</p>
 
 <h4 id="params">:params:</h4>
```

#### html2text {}

```diff
@@ -223,15 +223,15 @@
 origin.
 177
 178    #### :params:
 179
 180    `public`: Create the GitHub repo as a public repo, default is to create
 it as private."""
 181    visibility = "public" if public else "private"
-182    os.system(f"gh repo create --source . --{visibility}")
+182    os.system(f"gh repo create --source=. --remote=upstream --{visibility}")
 183
 184
 185def make_private(owner: str, name: str):
 186    """Uses GitHub CLI (must be installed and configured) to set the repo's
 visibility to private.
 187
 188    #### :params:
@@ -487,15 +487,15 @@
 origin.
 178
 179    #### :params:
 180
 181    `public`: Create the GitHub repo as a public repo, default is to create
 it as private."""
 182    visibility = "public" if public else "private"
-183    os.system(f"gh repo create --source . --{visibility}")
+183    os.system(f"gh repo create --source=. --remote=upstream --{visibility}")
 Use GitHub CLI (must be installed and configured) to create a remote GitHub
 repo from the current working directory repo and add its url as this repo's
 remote origin.
 *** :params: ***
 public: Create the GitHub repo as a public repo, default is to create it as
 private.
   ⁰
```

### Comparing `gitbetter-0.5.0/docs/gitbetter/gitbetter.html` & `gitbetter-0.5.1/docs/gitbetter/gitbetter.html`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/src/gitbetter/git.py` & `gitbetter-0.5.1/src/gitbetter/git.py`

 * *Files 1% similar despite different names*

```diff
@@ -175,15 +175,15 @@
     """Use GitHub CLI (must be installed and configured) to create a remote GitHub repo from
     the current working directory repo and add its url as this repo's remote origin.
 
     #### :params:
 
     `public`: Create the GitHub repo as a public repo, default is to create it as private."""
     visibility = "public" if public else "private"
-    os.system(f"gh repo create --source . --{visibility}")
+    os.system(f"gh repo create --source=. --remote=upstream --{visibility}")
 
 
 def make_private(owner: str, name: str):
     """Uses GitHub CLI (must be installed and configured) to set the repo's visibility to private.
 
     #### :params:
```

### Comparing `gitbetter-0.5.0/src/gitbetter/gitbetter.py` & `gitbetter-0.5.1/src/gitbetter/gitbetter.py`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/LICENSE.txt` & `gitbetter-0.5.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/README.md` & `gitbetter-0.5.1/README.md`

 * *Files identical despite different names*

### Comparing `gitbetter-0.5.0/pyproject.toml` & `gitbetter-0.5.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 00000040: 6c69 6e67 2e62 7569 6c64 220d 0a0d 0a5b  ling.build"....[
 00000050: 7072 6f6a 6563 745d 0d0a 6e61 6d65 203d  project]..name =
 00000060: 2022 6769 7462 6574 7465 7222 0d0a 6465   "gitbetter"..de
 00000070: 7363 7269 7074 696f 6e20 3d20 2243 7573  scription = "Cus
 00000080: 746f 6d20 6769 7420 7368 656c 6c20 746f  tom git shell to
 00000090: 2074 7970 6520 6c65 7373 2061 6e64 2063   type less and c
 000000a0: 6f6d 6d69 7420 6d6f 7265 2e22 0d0a 7665  ommit more."..ve
-000000b0: 7273 696f 6e20 3d20 2230 2e35 2e30 220d  rsion = "0.5.0".
+000000b0: 7273 696f 6e20 3d20 2230 2e35 2e31 220d  rsion = "0.5.1".
 000000c0: 0a72 6571 7569 7265 732d 7079 7468 6f6e  .requires-python
 000000d0: 203d 2022 3e3d 332e 3130 220d 0a64 6570   = ">=3.10"..dep
 000000e0: 656e 6465 6e63 6965 7320 3d20 5b22 6172  endencies = ["ar
 000000f0: 6773 6865 6c6c 222c 2022 7061 7468 6965  gshell", "pathie
 00000100: 7222 2c20 2270 7974 6573 7422 5d0d 0a72  r", "pytest"]..r
 00000110: 6561 646d 6520 3d20 2252 4541 444d 452e  eadme = "README.
 00000120: 6d64 220d 0a6b 6579 776f 7264 7320 3d20  md"..keywords =
```

### Comparing `gitbetter-0.5.0/PKG-INFO` & `gitbetter-0.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gitbetter
-Version: 0.5.0
+Version: 0.5.1
 Summary: Custom git shell to type less and commit more.
 Project-URL: Homepage, https://github.com/matt-manes/gitbetter
 Project-URL: Documentation, https://github.com/matt-manes/gitbetter/tree/main/docs
 Project-URL: Source code, https://github.com/matt-manes/gitbetter/tree/main/src/gitbetter
 Author-email: Matt Manes <mattmanes@pm.me>
 License-File: LICENSE.txt
 Keywords: cli,commit,git,shell,terminal
```

