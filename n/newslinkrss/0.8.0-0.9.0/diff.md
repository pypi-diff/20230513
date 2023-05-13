# Comparing `tmp/newslinkrss-0.8.0.tar.gz` & `tmp/newslinkrss-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "newslinkrss-0.8.0.tar", last modified: Sat Feb  4 19:35:44 2023, max compression
+gzip compressed data, was "dist/newslinkrss-0.9.0.tar", last modified: Sun Apr 16 22:46:26 2023, max compression
```

## Comparing `newslinkrss-0.8.0.tar` & `newslinkrss-0.9.0.tar`

### file list

```diff
@@ -1,14 +1,13 @@
-drwxrwxr-x   0 ittner    (1001) ittner    (1000)        0 2023-02-04 19:35:44.057726 newslinkrss-0.8.0/
--rw-rw-r--   0 ittner    (1001) ittner    (1000)    36685 2023-02-04 19:35:44.057726 newslinkrss-0.8.0/PKG-INFO
--rw-r--r--   0 ittner    (1001) ittner    (1000)    30552 2023-02-04 19:26:16.000000 newslinkrss-0.8.0/README.md
--rwxr-xr-x   0 ittner    (1001) ittner    (1000)    51147 2023-02-04 19:19:00.000000 newslinkrss-0.8.0/newslinkrss
-drwxrwxr-x   0 ittner    (1001) ittner    (1000)        0 2023-02-04 19:35:44.057726 newslinkrss-0.8.0/newslinkrss.egg-info/
--rw-rw-r--   0 ittner    (1001) ittner    (1000)    36685 2023-02-04 19:35:43.000000 newslinkrss-0.8.0/newslinkrss.egg-info/PKG-INFO
--rw-rw-r--   0 ittner    (1001) ittner    (1000)      259 2023-02-04 19:35:43.000000 newslinkrss-0.8.0/newslinkrss.egg-info/SOURCES.txt
--rw-rw-r--   0 ittner    (1001) ittner    (1000)        1 2023-02-04 19:35:43.000000 newslinkrss-0.8.0/newslinkrss.egg-info/dependency_links.txt
--rw-rw-r--   0 ittner    (1001) ittner    (1000)       86 2023-02-04 19:35:43.000000 newslinkrss-0.8.0/newslinkrss.egg-info/requires.txt
--rw-rw-r--   0 ittner    (1001) ittner    (1000)        1 2023-02-04 19:35:43.000000 newslinkrss-0.8.0/newslinkrss.egg-info/top_level.txt
--rw-rw-r--   0 ittner    (1001) ittner    (1000)        1 2023-02-04 19:35:36.000000 newslinkrss-0.8.0/newslinkrss.egg-info/zip-safe
--rw-r--r--   0 ittner    (1001) ittner    (1000)      108 2021-12-28 23:03:01.000000 newslinkrss-0.8.0/pyproject.toml
--rw-rw-r--   0 ittner    (1001) ittner    (1000)      951 2023-02-04 19:35:44.057726 newslinkrss-0.8.0/setup.cfg
--rwxr-xr-x   0 ittner    (1001) ittner    (1000)       62 2021-08-25 21:30:57.000000 newslinkrss-0.8.0/setup.py
+drwxrwxr-x   0 ittner    (1000) ittner    (1000)        0 2023-04-16 22:46:26.206005 newslinkrss-0.9.0/
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)    42254 2023-04-16 22:46:26.206005 newslinkrss-0.9.0/PKG-INFO
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)    35441 2023-04-16 22:44:12.000000 newslinkrss-0.9.0/README.md
+-rwxrwxr-x   0 ittner    (1000) ittner    (1000)    62599 2023-04-16 22:44:12.000000 newslinkrss-0.9.0/newslinkrss
+drwxrwxr-x   0 ittner    (1000) ittner    (1000)        0 2023-04-16 22:46:26.206005 newslinkrss-0.9.0/newslinkrss.egg-info/
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)    42254 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/PKG-INFO
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)      244 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/SOURCES.txt
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)        1 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/dependency_links.txt
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)       86 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/requires.txt
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)        1 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/top_level.txt
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)        1 2023-04-16 22:46:26.000000 newslinkrss-0.9.0/newslinkrss.egg-info/zip-safe
+-rw-rw-r--   0 ittner    (1000) ittner    (1000)      951 2023-04-16 22:46:26.206005 newslinkrss-0.9.0/setup.cfg
+-rwxrwxr-x   0 ittner    (1000) ittner    (1000)       62 2023-04-16 22:44:12.000000 newslinkrss-0.9.0/setup.py
```

### Comparing `newslinkrss-0.8.0/PKG-INFO` & `newslinkrss-0.9.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: newslinkrss
-Version: 0.8.0
+Version: 0.9.0
 Summary: Generate RSS feeds from generic sites
 Home-page: https://sr.ht/~ittner/newslinkrss/
 Author: Alexandre Erwin Ittner
 Author-email: alexandre@ittner.com.br
 License: GPLv3
 Description: # About
         
         newslinkrss generates RSS feeds from websites that do not provide their own.
-        This is done by loading a given URL and collecting links that matches a
-        pattern, given as a regular expression, to gather the relevant information,
-        optionally visiting them to get more details and even processing the target
-        pages with XPath and CSS Selectors if required. It basically works as a
-        purpose specific crawler or scraper.
+        This is done by loading URLs and collecting links that matches patterns,
+        given as a regular expression, to gather the relevant information, optionally
+        visiting them to get more details and even processing the target pages with
+        XPath and CSS Selectors if required. It basically works as a purpose specific
+        crawler or scraper.
         
         The results are printed as a RSS feed to stdout or, optionally, to a file. The
         simplest way to use it is just configure your **local** feed reader, like
         [Liferea](https://lzone.de/liferea/) or [Newsboat](https://newsboat.org/), to
         use a "command" source and pass the correct command line arguments to generate
         a suitable feed -- this allows you to centralize the configuration in the
         reader itself and let it handle update times, etc.
@@ -77,25 +77,27 @@
         other user-level or system-wide components and make experimentation with
         development versions easier. In this case, just do:
         
             python3 -m venv my-venv
             . my-venv/bin/activate
             pip install -U .
         
-        
         newslinkrss depends on a few libraries, this will ensure all them are also
         installed correctly.
         
         
         
         # Usage examples
         
         newslinkrss is lacking a lot of documentation, but the following examples
-        can show a bit of what it can and can not do. A complete list of options
-        can be read by typing `newslinkrss --help`.
+        can show a bit of what it can and can not do. To make understanding easier,
+        examples uses mostly the long, verbose, form of some options even when
+        abbreviations are available. A complete list of options, abbreviations,
+        default values, etc. can be read by typing `newslinkrss --help`.
+        
         
         
         ### Simplest case
         
         The simplest use case is just load a website, select all links matching a
         pattern and expose a feed using the text of that link as description and
         setting the publish date to the date and time that the command was run. For
@@ -116,15 +118,15 @@
         get information that it not is available from the URL or anchor text.
         Option `--follow` (shortcut `-f`) will make newslinkrss load the candidate
         target page and look for more data there. By default, it automatically
         captures the title of the page as the title of the feed entry, keeps the
         summary from anchor text, and loads author information and the page
         publishing and update dates and times from the page metadata (**if** this
         information is available in some common format, like
-        [Open Graph](https://ogp.me/) or Twitter cards.
+        [Open Graph](https://ogp.me/ ) or Twitter cards.
         
         Reuters [killed](https://news.ycombinator.com/item?id=23576022) its RSS feeds
         in mid 2020, so let's take them as an example and use newslinkrss to bring
         the feed back to life and right into our news readers. Our criteria will be:
         
         - First we must find every link that appears as plain HTML on the front page:
           https://www.reuters.com/ There is an infinite scroll and more links are
@@ -138,28 +140,28 @@
           https://www.reuters.com/world/europe/eu-proposes-create-solidarity-fund-ukraines-basic-needs-2022-03-18/
           Notice they all are in domain "https://www.reuters.com/", have at least one
           section ("/world/europe/") that is followed by part of the title and the
           publish date. This format is really great, as it allows us to ignore
           anything that does not look like a news article on the spot. So, a good
           pattern will be `'https://www.reuters.com/.+/.+\d{4}-\d{2}-\d{2}.+'`;
         
-        - newslinkrss deduplicates URLs automatically, so we don't need to worry if we
-          end up capturing the same link twice;
+        - newslinkrss deduplicates URLs automatically, so we don't need to worry if
+          we end up capturing the same link twice;
         
         - Target pages have Open Graph meta tags, so by just following them we can
           get accurate publish dates and times with no extra effort. Better yet, as
           we know that **all** news pages that we want have them, we can also instruct
           newslinkrss to ignore any page without a valid date, preventing any non-news
           article, captured by accident, from appearing in our feed. This is done
           with option `--require-dates`;
         
         - All page titles are something like "The actual headline | Reuters". This
           format is nice for a website but not so for feed items: the "| Reuters"
           part is not only redundant (the feed title already tells us about the
-          source of the article) but also noise, as it makes scanning through the
+          source of the article) but also noisy, as it makes scanning through the
           headlines harder. newslinkrss has an option `--title-regex` for exactly
           this use case of cleaning up redundant text from titles. It accepts a
           regular expression with a single capture group; if the expression matches,
           the text from the group will be used as the title, otherwise the original
           text will be used (so we don't loose titles if something changes at the
           source, for example). For this case, a good choice would be
           `--title-regex '(.+)\s+\|'` .
@@ -196,19 +198,19 @@
         
         Complete feeds are the ones which include the full text of the article with
         it, instead of just a summary and a link. They are really nice as we can
         read everything in the news aggregator itself. A good item body should be
         mostly static and clean HTML (so no scripts, interactive content, aggressive
         formatting, etc.) leaving everything else to the aggregator to handle.
         
-        Let's extend the previous example from Reuters website: as we are already
-        following and downloading the links, there is no much extra work to
-        generate the full feed from it. Option `--with-body` will copy the entire
-        contents of the "body" element from the page into the feed, just removing a
-        few obviously unwanted tags (scripts, forms, etc.).
+        So let's extend the previous example from Reuters website: as we are already
+        following and downloading the links, there is no much extra work to generate
+        the full feed from it. Option `--with-body` will copy the entire contents of
+        the "body" element from the page into the feed, just removing a few obviously
+        unwanted tags (scripts, forms, etc.).
         
         Including the entire body works for every case, but for this site we can
         filter a bit more and pick only actual text of the news article, ignoring
         unwanted noise like menus, sidebars, links to other news, etc. Running a
         quick "inspect element" in Firefox shows us that there is a single "article"
         element in the pages and that it has the text we want. newslinkrss allows
         using both XPath expressions and CSS Selectors to pick particular elements
@@ -314,32 +316,45 @@
           `--follow` every candidate link, downloading the target page and looking
           for  the title there.
         
         - As we are already following, there is no much extra effort to also
           generate a complete feed. The full text of the article is in an "article"
           element, so we can use `--body-xpath "//article"` here too.
         
+        - The target page has no author information in its metadata so newslinkrss
+          will not be able to find their names automatically. However, it has a link
+          to the list of articles from the same author in format
+          `<a href="/autor/xxxxxxxx">Author Name</a>` and we can use the prefix
+          from attribute `href` to pick it with XPath (using option
+          `--author-from-xpath`) or CSS Selectors (with `--author-from-csss`). The
+          CSS approach is simpler for this particular case, so let's use an
+          `--author-from-csss 'a[href^="/autor/"]'`. While not required for this
+          site (name is the only child element of "a"), some sites may prefix the
+          author name with a "by "; For these cases, we could also use options
+          `--csss-author-regex` and `--xpath-author-regex` to select only the name
+          with a regular expression. Also notice that author is an optional element
+          in both RSS and Atom, but it is nice to have it appearing in the correct
+          fields in the news reader so we can use this information for filtering
+          reading lists, for example.
+        
         The resulting command line is:
         
-            newslinkrss -p '.+/\d{4}/\d{2}/\d{2}/.+' \
+            newslinkrss \
+                -p 'https://revistaquestaodeciencia.com.br/.*\d{4}/\d{2}/\d{2}/.+' \
                 --date-from-url '.*/(\d{4}/\d{2}/\d{2})/.*' \
                 --url-date-fmt '%Y/%m/%d' \
                 --follow \
                 --with-body \
                 --body-xpath "//article" \
-                --max-links 50 \
+                --author-from-csss 'a[href^="/autor/"]' \
                 --max-page-length 512 \
                 --http-timeout 4 \
+                --title-regex '(.+)\s+\|' \
                 'https://revistaquestaodeciencia.com.br/'
         
-        To make understanding easier, this example uses the long, verbose, form of
-        some options even when abbreviations are available. For the same reason, some
-        of the options are set to the default values and are not strictly required
-        but they are listed anyway. See `newslinkrss --help` for details.
-        
         
         ### Using complex XPath expressions
         
         Sometimes we need to fight really hard to get the date that a particular item
         was last updated. Taking GitHub issues as an example: while GH provides Atom
         feeds for releases and commits (but always to specific branches), there is
         no equivalent for issues and pull requests. Of course, there is an API for
@@ -378,56 +393,60 @@
         helper function to get what the expression will return, for example:
         `$x('(//h3/a/relative-time)[last()]/@datetime')`.
         
         
         
         ### The first example, revisited
         
-        Now that we have a few extra tricks on our sleeves we can check back that
+        Now that we have a few extra tricks in our sleeves we can check back that
         very first example and fix some of its limitations:
         
         - First, we need the correct publish dates; they are neither in the URL nor
-          in the anchor text, so we need to `--follow` the pages and get them from
-          there. The pages also have no metadata for that, but there is a publish
-          date intended for human readers there in this slice of HTML:
-          `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`
-          The important part if that we can use a XPath expression to select that
-          date and then parse it; a good (not optimal! It does not follow CSS rules)
-          would be `--date-from-xpath '//small[@class="text-muted"]/b/text()'` and
-          it will capture the "23/12/2022" from the text node of the inner "b"
-          element, no need to filter it through `--xpath-date-regex` to remove
-          unwanted text, so we can then parse it with `--xpath-date-fmt '%d/%m/%Y'`;
-        
-        - Let's be extra careful with the URL patterns, so we don't follow a
-          random link going to another domain;
+          in the anchor text, so we need to `--follow` the pages and get the dates
+          from there. The pages also have no metadata for that, but they have a
+          publish date intended for human readers in a slice of HTML like this:
+          `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`.
+          We can use a XPath expression to select the date from element "b", a good
+          one (but technically incorrect as it does not follow CSS rules for attribute
+          "class") is `--date-from-xpath '//small[@class="text-muted"]/b/text()'` .
+          It is a bit convoluted but we can replace it with a CSS Selector (and also
+          fix the class attribute issue): `--date-from-csss 'small.text-muted > b'`.
+          It will capture the "23/12/2022" from the text node of inner element "b",
+          no need to filter through `--csss-date-regex` to remove unwanted text, but
+          as the date format is still ambiguous, we need to give an explicit format
+          with option `--csss-date-fmt '%d/%m/%Y'`;
+        
+        - Let's be extra careful with the URL pattern and never capture (or follow!)
+          links pointing to other domains. We can replace it with a more restricted
+          `-p 'https://www.jaraguadosul.sc.gov.br/news/.+'`;
         
         - As we are already following the pages, let's also generate a full feed.
           The relevant part of the articles are inside a "div" element with
           attribute "id" set to "area_impressao" (that's Portuguese for
           "printing_area" and one may imagine it is being used to format the page
           for printing, however there is neither an alternate style sheet nor a
           @media selector for it ... anyway, at least it helps us to select the
           correct text). We can isolate this element with a XPath expression
           `'//div[@id="area_impressao"]'` but this is slightly more complex than
           the equivalent CSS Selector `div#area_impressao` and, as we already used
-          XPath in several examples, let's use a CSSS this time;
+          XPath in several other examples, let's stick with CSSS;
         
         - That site can be a bit slow sometimes, so let's be extra tolerant and
           increase the HTTP timeout to 10 s;
         
         And then we have our fixed command line:
         
             newslinkrss \
                 -p 'https://www.jaraguadosul.sc.gov.br/news/.+' \
                 --http-timeout 10 \
                 --follow \
                 --with-body \
                 --body-csss 'div#area_impressao' \
-                --date-from-xpath '//small[@class="text-muted"]/b/text()' \
-                --xpath-date-fmt '%d/%m/%Y' \
+                --date-from-csss 'small.text-muted > b' \
+                --csss-date-fmt '%d/%m/%Y' \
                 https://www.jaraguadosul.sc.gov.br/noticias.php
         
         ... not perfect, but it gives us a very practical and usable feed!
         
         
         
         ## More useful notes
@@ -442,25 +461,25 @@
         Related options are the following:
         
         - If explicitly used, options `--date-from-xpath`, `--xpath-date-regex`, and
           `--xpath-date-fmt` will allow reading dates from any element in the target
           page which can be found with a XPath expression. Naturally, the target page
           which must be downloaded with `--follow`; The XPath expression must return
           a string (from the inner text or the attributes of an element), the second
-          must optionally provide a regular expression with a single capture group
-          with the date, and the third should give the date format. If no regex is
-          given, all the string will be used and if no date format is given, the code
-          will try some common date formats;
+          is optional, but if given it must provide a regular expression with a single
+          capture group with the date, and the third should give the date format. If
+          no regex is given, all the string will be used and if no date format is
+          given, the code will try some common date formats;
         
         - If explicitly used, options `--date-from-csss`, `--csss-date-regex`, and
           `--csss-date-fmt` work in a similar way as the previous ones, but using
           CSS Selectors instead. They are not as powerful or flexible as XPath, but
           simpler, cleaner, and more suitable for HTML;
         
-        - If explicitly used,  options `--date-from-text` and `--text-date-fmt` allow
+        - If explicitly used, options `--date-from-text` and `--text-date-fmt` allow
           reading the date from the anchor text (i.e., the text inside tag `<a>`)
           associated to a particular entry in the index page; no `--follow` is
           necessary. The first option must provide a regular expression with a single
           capture group for the date (which allows removing non-date parts of the
           string) and the second option should give the date format. If the format is
           not given, the code will try some common date formats;
         
@@ -484,40 +503,54 @@
         These options are tried in this order with the first valid date being picked.
         This way, options explicitly included in command line have priority, with
         higher precendence being given to the ones which may return a "good" date.
         If no date options are listed, or if could not grab a date from the document,
         standard metadata and HTTP headers will be used (in this order).
         
         
+        #### Locale-dependent dates
+        
+        Some date formats depend on the system locale, most common cases being month
+        names (tokens `%b` and `%B`), and the date parsing options will also depend
+        on it to interpret these dates correctly. By default, newslinkrss will use
+        the locale set for the current user, read from environment variables, and
+        ignore any failure if it is not available or is invalid. Option `--locale`
+        allows setting an explicit locale name, so newslinkrss will use it or abort
+        in the event of a failure. If you want to keep the default best-effort
+        approach for a non-default locale, set environment variable LC_ALL when
+        caling newslinkrss (i.e. call with
+        `"LC_ALL=pt_BR.UTF-8 newslinkrss <options>"`).
+        
+        
         
         ### Ignoring URLs
         
         The link pattern (-p) has a counterpart `--ignore-pattern` (shortcut `-i`)
         which also accepts a regular expression and makes `newslinkrss` ignore any
         matching URL. Depending on the amount of information that the website puts on
         the URLs, this can be used for excluding native advertisement, uninteresting
         sections, or other unwanted content from the feed, without support from the
         feed reader and without counting to the total URL limit (`-n`). While it is
         possible to add this ignore rule to the link pattern itself, using `-i`
         prevents that regular expression from becoming excessively complex and makes
-        debugging easier.
+        debugging easier. This option can be used multiple times, a URL that match
+        any of them will be ignored.
         
         
         ### Cleaning URL query strings
         
         Sometimes the source page has URLs with unwanted query string parameters,
         like the [UTM trackers](https://en.wikipedia.org/wiki/UTM_parameters), or
         multiple URLs differing only by irrelevant query string parameters and
         pointing to the same destination page (and therefore confusing the duplicate
         link detection). Option `--qs-remove-param` (shortcut `-Q`) may be used to
         fix this. If the name of a parameter matches the regular expression given in
         this option, that name/value pair will be removed from the URL query string.
         This option may be repeated many times if necessary. Example: `-Q '^utm.+'`
-        (notice the anchor to only match a prefix).
-        
+        (notice the anchor to only match prefixes).
         
         
         ### Excluding body elements
         
         When generating a complete feed we may sometimes end up including some
         unwanted elements from the source page into the item body, usually ads,
         "related news" boxes, section headers, random images, distracting formatting,
@@ -527,15 +560,15 @@
         fragile solution, we can just remove the unwanted elements explicitly.
         
         newslinkrss has tree command line options for this:
         
         - Option `--body-remove-tag` (shortcut `-R`) will remove all occurrences of
           the given tag from the feed body and move their child elements to their
           parents. This can be used to remove formatting while preserving the inner
-          text (e.g. `-R strong`) or to remove images from the body (with `-R  img`,
+          text (e.g. `-R strong`) or to remove images from the body (with `-R img`,
           as "img" elements have no children);
         
         - Option `--body-remove-xpath` (shortcut `-X`) will remove the elements
           given by a XPath expression **and** their children. This is a good way
           to remove banners, divs, etc. from the generated feed;
         
         - Option `--body-remove-csss` (shortcut `-C`) will remove the elements given
@@ -543,14 +576,66 @@
           banners, divs, etc. from the generated and more practical when selecting
           element by their CSS classes.
         
         All three options can be repeated in the command line how many times as
         necessary to express all required rules.
         
         
+        ### Handling request language options
+        
+        Some sites change their rendering, response language, **date formats**, etc.
+        according to the preferred language information sent by the user's browser.
+        By default, newslinkrss uses the "LANG" environment variable to set this
+        language information (it is a bit of an optimization for the most common
+        case where the system language is the same as the one of the browser used for
+        debugging the options for a particular feed). To set a different one, you may
+        overwrite the LANG variable or use option `--lang`. The later option is more
+        flexible as it may be repeated to set several languages in order of preference
+        (e.g. `"--lang pt-BR --lang en-US --lang de-DE"`).
+        
+        To not send any preferred language information to the server, independently
+        of one currently set for the system, clear the LANG variable for the
+        newslinkrss process invocation (e.g. `"LANG='' newslinkrss <other options>"`).
+        
+        
+        ### Managing cookies
+        
+        newslinkrss persists cookies among requests from the same program invocation
+        and forgets them once the program finishes; this is usually the most practical
+        choice for typical use cases, but there is an option `--no-cookies` to disable
+        all cookies if it becomes a problem for a particular source.
+        
+        Conversely, sites may expect a particular cookies to be set to a specific
+        values, for example, to show news from a particular geographic region.
+        Command line option `--cookie` allows the user to define customized cookies
+        to handle these cases. This option supports the complete syntax defined by
+        [RFC 2965](https://www.rfc-editor.org/rfc/rfc2965.html), but a simple
+        `name=value` will work for the majority of use cases. Example:
+        `--cookie 'cookie-banner-consent-accepted=false'`. This option can be
+        repeated as many times as necessary.
+        
+        If user-defined cookies are used together with option `--no-cookies`, the
+        target site will have access to them, but will not be able to change or
+        delete them (by overwriting or redefining the expiry date) or set new ones.
+        This results in a read-only set of cookie jar that can be very useful for
+        sites that require cookies but use them to change behavior in unwanted ways
+        after some number of pages are read.
+        
+        
+        ### Setting arbitrary HTTP headers
+        
+        Some sites my require unusual request options to work correctly. newslinkrss
+        has an option `--header` (shortcut: `-H`) to set any HTTP header for the
+        requests it sends. To use it, just pass the header in format `"NAME: VALUE"`
+        (e.g. `--header 'X-Clacks-Overhead: GNU Terry Pratchett'`). This should not
+        be a common requirement, however. It is also not recommended to use this
+        option for handling language preferences and cookies, as the dedicated
+        options `--lang` and `--cookie` will take care of the specific behavior of
+        these headers.
+        
         
         ### Testing links
         
         newslinkrss has an option `--test` that will skip the feed generation step
         and just print the links and titles that were captured for a particular set
         of options to stdout. That's a simple way to check if a pattern is working
         as intended.
```

### Comparing `newslinkrss-0.8.0/README.md` & `newslinkrss-0.9.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # About
 
 newslinkrss generates RSS feeds from websites that do not provide their own.
-This is done by loading a given URL and collecting links that matches a
-pattern, given as a regular expression, to gather the relevant information,
-optionally visiting them to get more details and even processing the target
-pages with XPath and CSS Selectors if required. It basically works as a
-purpose specific crawler or scraper.
+This is done by loading URLs and collecting links that matches patterns,
+given as a regular expression, to gather the relevant information, optionally
+visiting them to get more details and even processing the target pages with
+XPath and CSS Selectors if required. It basically works as a purpose specific
+crawler or scraper.
 
 The results are printed as a RSS feed to stdout or, optionally, to a file. The
 simplest way to use it is just configure your **local** feed reader, like
 [Liferea](https://lzone.de/liferea/) or [Newsboat](https://newsboat.org/), to
 use a "command" source and pass the correct command line arguments to generate
 a suitable feed -- this allows you to centralize the configuration in the
 reader itself and let it handle update times, etc.
@@ -69,25 +69,27 @@
 other user-level or system-wide components and make experimentation with
 development versions easier. In this case, just do:
 
     python3 -m venv my-venv
     . my-venv/bin/activate
     pip install -U .
 
-
 newslinkrss depends on a few libraries, this will ensure all them are also
 installed correctly.
 
 
 
 # Usage examples
 
 newslinkrss is lacking a lot of documentation, but the following examples
-can show a bit of what it can and can not do. A complete list of options
-can be read by typing `newslinkrss --help`.
+can show a bit of what it can and can not do. To make understanding easier,
+examples uses mostly the long, verbose, form of some options even when
+abbreviations are available. A complete list of options, abbreviations,
+default values, etc. can be read by typing `newslinkrss --help`.
+
 
 
 ### Simplest case
 
 The simplest use case is just load a website, select all links matching a
 pattern and expose a feed using the text of that link as description and
 setting the publish date to the date and time that the command was run. For
@@ -108,15 +110,15 @@
 get information that it not is available from the URL or anchor text.
 Option `--follow` (shortcut `-f`) will make newslinkrss load the candidate
 target page and look for more data there. By default, it automatically
 captures the title of the page as the title of the feed entry, keeps the
 summary from anchor text, and loads author information and the page
 publishing and update dates and times from the page metadata (**if** this
 information is available in some common format, like
-[Open Graph](https://ogp.me/) or Twitter cards.
+[Open Graph](https://ogp.me/ ) or Twitter cards.
 
 Reuters [killed](https://news.ycombinator.com/item?id=23576022) its RSS feeds
 in mid 2020, so let's take them as an example and use newslinkrss to bring
 the feed back to life and right into our news readers. Our criteria will be:
 
 - First we must find every link that appears as plain HTML on the front page:
   https://www.reuters.com/ There is an infinite scroll and more links are
@@ -130,28 +132,28 @@
   https://www.reuters.com/world/europe/eu-proposes-create-solidarity-fund-ukraines-basic-needs-2022-03-18/
   Notice they all are in domain "https://www.reuters.com/", have at least one
   section ("/world/europe/") that is followed by part of the title and the
   publish date. This format is really great, as it allows us to ignore
   anything that does not look like a news article on the spot. So, a good
   pattern will be `'https://www.reuters.com/.+/.+\d{4}-\d{2}-\d{2}.+'`;
 
-- newslinkrss deduplicates URLs automatically, so we don't need to worry if we
-  end up capturing the same link twice;
+- newslinkrss deduplicates URLs automatically, so we don't need to worry if
+  we end up capturing the same link twice;
 
 - Target pages have Open Graph meta tags, so by just following them we can
   get accurate publish dates and times with no extra effort. Better yet, as
   we know that **all** news pages that we want have them, we can also instruct
   newslinkrss to ignore any page without a valid date, preventing any non-news
   article, captured by accident, from appearing in our feed. This is done
   with option `--require-dates`;
 
 - All page titles are something like "The actual headline | Reuters". This
   format is nice for a website but not so for feed items: the "| Reuters"
   part is not only redundant (the feed title already tells us about the
-  source of the article) but also noise, as it makes scanning through the
+  source of the article) but also noisy, as it makes scanning through the
   headlines harder. newslinkrss has an option `--title-regex` for exactly
   this use case of cleaning up redundant text from titles. It accepts a
   regular expression with a single capture group; if the expression matches,
   the text from the group will be used as the title, otherwise the original
   text will be used (so we don't loose titles if something changes at the
   source, for example). For this case, a good choice would be
   `--title-regex '(.+)\s+\|'` .
@@ -188,19 +190,19 @@
 
 Complete feeds are the ones which include the full text of the article with
 it, instead of just a summary and a link. They are really nice as we can
 read everything in the news aggregator itself. A good item body should be
 mostly static and clean HTML (so no scripts, interactive content, aggressive
 formatting, etc.) leaving everything else to the aggregator to handle.
 
-Let's extend the previous example from Reuters website: as we are already
-following and downloading the links, there is no much extra work to
-generate the full feed from it. Option `--with-body` will copy the entire
-contents of the "body" element from the page into the feed, just removing a
-few obviously unwanted tags (scripts, forms, etc.).
+So let's extend the previous example from Reuters website: as we are already
+following and downloading the links, there is no much extra work to generate
+the full feed from it. Option `--with-body` will copy the entire contents of
+the "body" element from the page into the feed, just removing a few obviously
+unwanted tags (scripts, forms, etc.).
 
 Including the entire body works for every case, but for this site we can
 filter a bit more and pick only actual text of the news article, ignoring
 unwanted noise like menus, sidebars, links to other news, etc. Running a
 quick "inspect element" in Firefox shows us that there is a single "article"
 element in the pages and that it has the text we want. newslinkrss allows
 using both XPath expressions and CSS Selectors to pick particular elements
@@ -306,32 +308,45 @@
   `--follow` every candidate link, downloading the target page and looking
   for  the title there.
 
 - As we are already following, there is no much extra effort to also
   generate a complete feed. The full text of the article is in an "article"
   element, so we can use `--body-xpath "//article"` here too.
 
+- The target page has no author information in its metadata so newslinkrss
+  will not be able to find their names automatically. However, it has a link
+  to the list of articles from the same author in format
+  `<a href="/autor/xxxxxxxx">Author Name</a>` and we can use the prefix
+  from attribute `href` to pick it with XPath (using option
+  `--author-from-xpath`) or CSS Selectors (with `--author-from-csss`). The
+  CSS approach is simpler for this particular case, so let's use an
+  `--author-from-csss 'a[href^="/autor/"]'`. While not required for this
+  site (name is the only child element of "a"), some sites may prefix the
+  author name with a "by "; For these cases, we could also use options
+  `--csss-author-regex` and `--xpath-author-regex` to select only the name
+  with a regular expression. Also notice that author is an optional element
+  in both RSS and Atom, but it is nice to have it appearing in the correct
+  fields in the news reader so we can use this information for filtering
+  reading lists, for example.
+
 The resulting command line is:
 
-    newslinkrss -p '.+/\d{4}/\d{2}/\d{2}/.+' \
+    newslinkrss \
+        -p 'https://revistaquestaodeciencia.com.br/.*\d{4}/\d{2}/\d{2}/.+' \
         --date-from-url '.*/(\d{4}/\d{2}/\d{2})/.*' \
         --url-date-fmt '%Y/%m/%d' \
         --follow \
         --with-body \
         --body-xpath "//article" \
-        --max-links 50 \
+        --author-from-csss 'a[href^="/autor/"]' \
         --max-page-length 512 \
         --http-timeout 4 \
+        --title-regex '(.+)\s+\|' \
         'https://revistaquestaodeciencia.com.br/'
 
-To make understanding easier, this example uses the long, verbose, form of
-some options even when abbreviations are available. For the same reason, some
-of the options are set to the default values and are not strictly required
-but they are listed anyway. See `newslinkrss --help` for details.
-
 
 ### Using complex XPath expressions
 
 Sometimes we need to fight really hard to get the date that a particular item
 was last updated. Taking GitHub issues as an example: while GH provides Atom
 feeds for releases and commits (but always to specific branches), there is
 no equivalent for issues and pull requests. Of course, there is an API for
@@ -370,56 +385,60 @@
 helper function to get what the expression will return, for example:
 `$x('(//h3/a/relative-time)[last()]/@datetime')`.
 
 
 
 ### The first example, revisited
 
-Now that we have a few extra tricks on our sleeves we can check back that
+Now that we have a few extra tricks in our sleeves we can check back that
 very first example and fix some of its limitations:
 
 - First, we need the correct publish dates; they are neither in the URL nor
-  in the anchor text, so we need to `--follow` the pages and get them from
-  there. The pages also have no metadata for that, but there is a publish
-  date intended for human readers there in this slice of HTML:
-  `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`
-  The important part if that we can use a XPath expression to select that
-  date and then parse it; a good (not optimal! It does not follow CSS rules)
-  would be `--date-from-xpath '//small[@class="text-muted"]/b/text()'` and
-  it will capture the "23/12/2022" from the text node of the inner "b"
-  element, no need to filter it through `--xpath-date-regex` to remove
-  unwanted text, so we can then parse it with `--xpath-date-fmt '%d/%m/%Y'`;
-
-- Let's be extra careful with the URL patterns, so we don't follow a
-  random link going to another domain;
+  in the anchor text, so we need to `--follow` the pages and get the dates
+  from there. The pages also have no metadata for that, but they have a
+  publish date intended for human readers in a slice of HTML like this:
+  `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`.
+  We can use a XPath expression to select the date from element "b", a good
+  one (but technically incorrect as it does not follow CSS rules for attribute
+  "class") is `--date-from-xpath '//small[@class="text-muted"]/b/text()'` .
+  It is a bit convoluted but we can replace it with a CSS Selector (and also
+  fix the class attribute issue): `--date-from-csss 'small.text-muted > b'`.
+  It will capture the "23/12/2022" from the text node of inner element "b",
+  no need to filter through `--csss-date-regex` to remove unwanted text, but
+  as the date format is still ambiguous, we need to give an explicit format
+  with option `--csss-date-fmt '%d/%m/%Y'`;
+
+- Let's be extra careful with the URL pattern and never capture (or follow!)
+  links pointing to other domains. We can replace it with a more restricted
+  `-p 'https://www.jaraguadosul.sc.gov.br/news/.+'`;
 
 - As we are already following the pages, let's also generate a full feed.
   The relevant part of the articles are inside a "div" element with
   attribute "id" set to "area_impressao" (that's Portuguese for
   "printing_area" and one may imagine it is being used to format the page
   for printing, however there is neither an alternate style sheet nor a
   @media selector for it ... anyway, at least it helps us to select the
   correct text). We can isolate this element with a XPath expression
   `'//div[@id="area_impressao"]'` but this is slightly more complex than
   the equivalent CSS Selector `div#area_impressao` and, as we already used
-  XPath in several examples, let's use a CSSS this time;
+  XPath in several other examples, let's stick with CSSS;
 
 - That site can be a bit slow sometimes, so let's be extra tolerant and
   increase the HTTP timeout to 10 s;
 
 And then we have our fixed command line:
 
     newslinkrss \
         -p 'https://www.jaraguadosul.sc.gov.br/news/.+' \
         --http-timeout 10 \
         --follow \
         --with-body \
         --body-csss 'div#area_impressao' \
-        --date-from-xpath '//small[@class="text-muted"]/b/text()' \
-        --xpath-date-fmt '%d/%m/%Y' \
+        --date-from-csss 'small.text-muted > b' \
+        --csss-date-fmt '%d/%m/%Y' \
         https://www.jaraguadosul.sc.gov.br/noticias.php
 
 ... not perfect, but it gives us a very practical and usable feed!
 
 
 
 ## More useful notes
@@ -434,25 +453,25 @@
 Related options are the following:
 
 - If explicitly used, options `--date-from-xpath`, `--xpath-date-regex`, and
   `--xpath-date-fmt` will allow reading dates from any element in the target
   page which can be found with a XPath expression. Naturally, the target page
   which must be downloaded with `--follow`; The XPath expression must return
   a string (from the inner text or the attributes of an element), the second
-  must optionally provide a regular expression with a single capture group
-  with the date, and the third should give the date format. If no regex is
-  given, all the string will be used and if no date format is given, the code
-  will try some common date formats;
+  is optional, but if given it must provide a regular expression with a single
+  capture group with the date, and the third should give the date format. If
+  no regex is given, all the string will be used and if no date format is
+  given, the code will try some common date formats;
 
 - If explicitly used, options `--date-from-csss`, `--csss-date-regex`, and
   `--csss-date-fmt` work in a similar way as the previous ones, but using
   CSS Selectors instead. They are not as powerful or flexible as XPath, but
   simpler, cleaner, and more suitable for HTML;
 
-- If explicitly used,  options `--date-from-text` and `--text-date-fmt` allow
+- If explicitly used, options `--date-from-text` and `--text-date-fmt` allow
   reading the date from the anchor text (i.e., the text inside tag `<a>`)
   associated to a particular entry in the index page; no `--follow` is
   necessary. The first option must provide a regular expression with a single
   capture group for the date (which allows removing non-date parts of the
   string) and the second option should give the date format. If the format is
   not given, the code will try some common date formats;
 
@@ -476,40 +495,54 @@
 These options are tried in this order with the first valid date being picked.
 This way, options explicitly included in command line have priority, with
 higher precendence being given to the ones which may return a "good" date.
 If no date options are listed, or if could not grab a date from the document,
 standard metadata and HTTP headers will be used (in this order).
 
 
+#### Locale-dependent dates
+
+Some date formats depend on the system locale, most common cases being month
+names (tokens `%b` and `%B`), and the date parsing options will also depend
+on it to interpret these dates correctly. By default, newslinkrss will use
+the locale set for the current user, read from environment variables, and
+ignore any failure if it is not available or is invalid. Option `--locale`
+allows setting an explicit locale name, so newslinkrss will use it or abort
+in the event of a failure. If you want to keep the default best-effort
+approach for a non-default locale, set environment variable LC_ALL when
+caling newslinkrss (i.e. call with
+`"LC_ALL=pt_BR.UTF-8 newslinkrss <options>"`).
+
+
 
 ### Ignoring URLs
 
 The link pattern (-p) has a counterpart `--ignore-pattern` (shortcut `-i`)
 which also accepts a regular expression and makes `newslinkrss` ignore any
 matching URL. Depending on the amount of information that the website puts on
 the URLs, this can be used for excluding native advertisement, uninteresting
 sections, or other unwanted content from the feed, without support from the
 feed reader and without counting to the total URL limit (`-n`). While it is
 possible to add this ignore rule to the link pattern itself, using `-i`
 prevents that regular expression from becoming excessively complex and makes
-debugging easier.
+debugging easier. This option can be used multiple times, a URL that match
+any of them will be ignored.
 
 
 ### Cleaning URL query strings
 
 Sometimes the source page has URLs with unwanted query string parameters,
 like the [UTM trackers](https://en.wikipedia.org/wiki/UTM_parameters), or
 multiple URLs differing only by irrelevant query string parameters and
 pointing to the same destination page (and therefore confusing the duplicate
 link detection). Option `--qs-remove-param` (shortcut `-Q`) may be used to
 fix this. If the name of a parameter matches the regular expression given in
 this option, that name/value pair will be removed from the URL query string.
 This option may be repeated many times if necessary. Example: `-Q '^utm.+'`
-(notice the anchor to only match a prefix).
-
+(notice the anchor to only match prefixes).
 
 
 ### Excluding body elements
 
 When generating a complete feed we may sometimes end up including some
 unwanted elements from the source page into the item body, usually ads,
 "related news" boxes, section headers, random images, distracting formatting,
@@ -519,15 +552,15 @@
 fragile solution, we can just remove the unwanted elements explicitly.
 
 newslinkrss has tree command line options for this:
 
 - Option `--body-remove-tag` (shortcut `-R`) will remove all occurrences of
   the given tag from the feed body and move their child elements to their
   parents. This can be used to remove formatting while preserving the inner
-  text (e.g. `-R strong`) or to remove images from the body (with `-R  img`,
+  text (e.g. `-R strong`) or to remove images from the body (with `-R img`,
   as "img" elements have no children);
 
 - Option `--body-remove-xpath` (shortcut `-X`) will remove the elements
   given by a XPath expression **and** their children. This is a good way
   to remove banners, divs, etc. from the generated feed;
 
 - Option `--body-remove-csss` (shortcut `-C`) will remove the elements given
@@ -535,14 +568,66 @@
   banners, divs, etc. from the generated and more practical when selecting
   element by their CSS classes.
 
 All three options can be repeated in the command line how many times as
 necessary to express all required rules.
 
 
+### Handling request language options
+
+Some sites change their rendering, response language, **date formats**, etc.
+according to the preferred language information sent by the user's browser.
+By default, newslinkrss uses the "LANG" environment variable to set this
+language information (it is a bit of an optimization for the most common
+case where the system language is the same as the one of the browser used for
+debugging the options for a particular feed). To set a different one, you may
+overwrite the LANG variable or use option `--lang`. The later option is more
+flexible as it may be repeated to set several languages in order of preference
+(e.g. `"--lang pt-BR --lang en-US --lang de-DE"`).
+
+To not send any preferred language information to the server, independently
+of one currently set for the system, clear the LANG variable for the
+newslinkrss process invocation (e.g. `"LANG='' newslinkrss <other options>"`).
+
+
+### Managing cookies
+
+newslinkrss persists cookies among requests from the same program invocation
+and forgets them once the program finishes; this is usually the most practical
+choice for typical use cases, but there is an option `--no-cookies` to disable
+all cookies if it becomes a problem for a particular source.
+
+Conversely, sites may expect a particular cookies to be set to a specific
+values, for example, to show news from a particular geographic region.
+Command line option `--cookie` allows the user to define customized cookies
+to handle these cases. This option supports the complete syntax defined by
+[RFC 2965](https://www.rfc-editor.org/rfc/rfc2965.html), but a simple
+`name=value` will work for the majority of use cases. Example:
+`--cookie 'cookie-banner-consent-accepted=false'`. This option can be
+repeated as many times as necessary.
+
+If user-defined cookies are used together with option `--no-cookies`, the
+target site will have access to them, but will not be able to change or
+delete them (by overwriting or redefining the expiry date) or set new ones.
+This results in a read-only set of cookie jar that can be very useful for
+sites that require cookies but use them to change behavior in unwanted ways
+after some number of pages are read.
+
+
+### Setting arbitrary HTTP headers
+
+Some sites my require unusual request options to work correctly. newslinkrss
+has an option `--header` (shortcut: `-H`) to set any HTTP header for the
+requests it sends. To use it, just pass the header in format `"NAME: VALUE"`
+(e.g. `--header 'X-Clacks-Overhead: GNU Terry Pratchett'`). This should not
+be a common requirement, however. It is also not recommended to use this
+option for handling language preferences and cookies, as the dedicated
+options `--lang` and `--cookie` will take care of the specific behavior of
+these headers.
+
 
 ### Testing links
 
 newslinkrss has an option `--test` that will skip the feed generation step
 and just print the links and titles that were captured for a particular set
 of options to stdout. That's a simple way to check if a pattern is working
 as intended.
```

### Comparing `newslinkrss-0.8.0/newslinkrss` & `newslinkrss-0.9.0/newslinkrss`

 * *Files 9% similar despite different names*

```diff
@@ -16,20 +16,24 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <https://www.gnu.org/licenses/>.
 #
 
 import sys
 import re
+import os
 import datetime
+import copy
 import argparse
+import locale
 import logging
 import traceback
 from html.parser import HTMLParser
 import http.cookiejar
+import http.cookies
 import urllib
 import urllib3
 
 import dateutil.parser
 import PyRSS2Gen
 import requests
 
@@ -37,15 +41,15 @@
 import lxml.html.clean
 import lxml.etree
 import lxml.cssselect
 import cssselect
 
 
 DEFAULT_USER_AGENT = (
-    "Mozilla/5.0 (X11; Linux x86_64; rv:108.0) Gecko/20100101 Firefox/108.0"
+    "Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/111.0"
 )
 
 USER_LOG_LEVELS = ["DEBUG", "INFO", "WARNING", "ERROR", "CRITICAL", "FATAL"]
 logging.basicConfig(level=logging.WARNING)
 logger = logging.getLogger(__name__)
 
 
@@ -72,16 +76,16 @@
             return itm[1]
     return None
 
 
 def clean_url_query_string(rx_list, url):
     """Remove unwanted parameters from the URL query string.
 
-    If the URL has a query string, remove all name/value pairs which
-    names matches any of the regular expressions given in list 'rx_list'.
+    If the URL has a query string, remove all name/value pairs with names
+    matching any of the regular expressions given in list 'rx_list'.
     Return the URL, possibly modified.
     """
 
     if not rx_list:
         return url
 
     u = urllib.parse.urlparse(url)
@@ -141,23 +145,28 @@
             href = href.split("#", 2)[0]  # Strip URL fragment.
             if self.base_url:
                 href = requests.compat.urljoin(self.base_url, href)
             href = clean_url_query_string(self.qs_cleanup_rx_list, href)
 
             # Try to noe follow the same link more than once. We need to
             # repeat this check later due to redirects.
-            if (
-                href not in self._found_links
-                and (not self.url_patt or re.match(self.url_patt, href))
-                and (not self.ignore_patt or not re.match(self.ignore_patt, href))
-            ):
+            if href not in self._found_links and self.test_url_patterns(href):
                 self._last_link_text = []
                 self._grab_link_text = True
                 self._last_link = href
 
+    def test_url_patterns(self, url):
+        """Return True if url is valid for visiting (i.e. matches at least one
+        accept pattern and do not match any ignore pattern.
+        """
+
+        if self.ignore_patt and any(re.match(patt, url) for patt in self.ignore_patt):
+            return False
+        return not self.url_patt or any(re.match(patt, url) for patt in self.url_patt)
+
     def handle_data(self, data):
         if self._grab_link_text:
             text = data.strip()
             if text != "":
                 self._last_link_text.append(text)
 
     def handle_endtag(self, tag):
@@ -171,16 +180,16 @@
                 self.links.append((self._last_link, link_text))
                 logger.info("New link added: %s %s", self._last_link, link_text)
             self._last_link = False
 
 
 def normalize_rfc1766_lang_tag(loc):
     """RSS2 and HTML use RFC 1766 language codes (with an "-"), while Open
-    Graph uses a "_". This function fixes this mess and normalizes cases,
-    spaces, etc.
+    Graph and "LANG" environment variable use a "_". This function fixes
+    this difference and normalizes cases, spaces, etc.
 
     Notice that RFC 1766 is not case-sensitive, capitalization is just a
     convention. This function capitalizes country codes for easy reading.
 
     Returns None for (some) nonsensical values.
     """
     loc = loc.strip().lower().replace("_", "-")
@@ -263,27 +272,26 @@
             name = _first_valid_attr_in_list(attrs, "name")
             prop = _first_valid_attr_in_list(attrs, "property")
             content = _first_valid_attr_in_list(attrs, "content")
             if name:
                 name = name.lower()
             if prop:
                 prop = prop.lower()
+            # Many sites just mix "name" and "property".
+            name_or_prop = name or prop
 
             # Attributes defined by the Open Graph Protocol: A lot of sites
             # which refuse to provide feeds have this nice attributes so their
             # contents appear nicely when linked on Facebook, Twitter and so.
             # These can provide a lot of useful information.
 
-            if (
-                prop == "article:published_time"
-                or prop == "article:modified_time"
-                or prop == "og:updated_time"
-                or name == "article:published_time"
-                or name == "article:modified_time"
-                or name == "og:updated_time"
+            if name_or_prop in (
+                "article:published_time",
+                "article:modified_time",
+                "og:updated_time",
             ):
                 # Content is a date in ISO format.
                 # <meta property="article:published_time" content="2020-09-13T20:00:00+00:00" />
                 # <meta property="article:modified_time" content="2020-09-13T20:01:42+00:00" />
                 try:
                     dt = dateutil.parser.parse(content)
                     if (not self.changed) or (self.changed < dt):
@@ -292,33 +300,35 @@
                 except:
                     logger.exception("When parsing changed date")
 
             if prop == "og:url" and not self.canonical:
                 # <meta property="og:url" content="xxxxx">
                 self.canonical = content
 
-            if prop in ("og:description", "twitter:description") or (
-                name == "description"
-            ):
-                if len(content) > 8 and (
-                    (not self.description) or (len(content) > len(self.description))
+            if name_or_prop in ("og:description", "twitter:description", "description"):
+                if (
+                    content
+                    and len(content) > 8
+                    and (
+                        (not self.description) or (len(content) > len(self.description))
+                    )
                 ):
                     self.description = content
 
-            if not self.author and (name == "author" or prop == "article:author"):
+            if not self.author and name_or_prop in ("author", "article:author"):
                 self.author = content
 
-            if name == "article:tag" or prop == "article:tag":
+            if name_or_prop == "article:tag":
                 if content and content not in self.tags:
                     self.tags.append(content)
 
-            if (name == "article:section" or prop == "article:section") and content:
+            if (name_or_prop == "article:section") and content:
                 self.section = content
 
-            if (name == "og:locale" or prop == "og:locale") and content:
+            if (name_or_prop == "og:locale") and content:
                 lang = normalize_rfc1766_lang_tag(content)
                 if self._html_locale and self.language:
                     self.language = lang
                     self._html_locale = False
                 elif not self.language:
                     self.language = lang
 
@@ -354,23 +364,35 @@
         logger.exception(
             "when parsing date with src=%s, fmt=%s, rx=%s", src, date_fmt, date_rx
         )
 
     return rdate
 
 
-def make_clean_title(args, title):
-    if args.title_regex:
-        m = re.match(args.title_regex, title)
+def get_regex_first_group(regex, srcstr):
+    """If a regex with one capture group is given and it matches the source
+    string, returns this group. Otherwise, returns None. This is used for a
+    few "clean up" filters through the code.
+
+    regex: regular expression string or None
+    srcstr: source string or None
+    """
+    if regex and srcstr:
+        m = re.match(regex, srcstr)
         if m:
             try:
-                title = m[1]
+                return m[1]
             except IndexError:
                 pass
-    return title[: args.max_title_length]
+    return None
+
+
+def make_clean_title(args, title):
+    clean_title = get_regex_first_group(args.title_regex, title) or title
+    return clean_title[: args.max_title_length]
 
 
 def remove_unwanted_body_elements(args, body):
     if args.body_remove_tag:
         lxml.etree.strip_tags(body, *args.body_remove_tag)
     if args.body_remove_xpath:
         for expr in args.body_remove_xpath:
@@ -404,14 +426,15 @@
             lst = tree.xpath("/html/body/*")
         if lst:
             if len(lst) > 1:
                 body = lxml.html.Element("div")
                 body.extend(lst)
             else:
                 body = lst[0]
+            body = copy.deepcopy(body)
             remove_unwanted_body_elements(args, body)
             cleaner = lxml.html.clean.Cleaner()
             body = cleaner.clean_html(body)
             if isinstance(body, str):
                 bodyhtml = body
             else:
                 bodyhtml = lxml.html.tostring(
@@ -445,14 +468,16 @@
                     break
         except lxml.etree.XPathEvalError:
             pass
     if not date and args.date_from_csss and tree is not None:
         try:
             for res in tree.cssselect(args.date_from_csss):
                 etext = res.text
+                if etext is None:
+                    continue
                 logger.debug("date-from-csss found candidate text: '%s'", etext)
                 date = try_date_from_str(
                     etext, args.csss_date_regex, args.csss_date_fmt
                 )
                 if date:
                     logger.debug("Found date from CSS Selector %s", date)
                     break
@@ -475,81 +500,136 @@
                 date,
             )
         except dateutil.parser.ParserError:
             logger.exception('Invalid date in HTTP header "Last-modified"')
     return date
 
 
-def make_feed_item_follow(session, url, used_urls, args, link_text, base_attrs):
-    attr_parser = CollectAttributesParser()
-    description = ""
+def find_item_author(args, attr_parser, tree):
+    """Try to get the author of an item.
+
+    Finds the author from explicitly requested elements and falls back to
+    metadata if these are not available.
+    """
+    author = None
+    if not author and args.author_from_xpath and tree is not None:
+        try:
+            for res in tree.xpath(args.author_from_xpath):
+                if res:
+                    author = get_regex_first_group(args.xpath_author_regex, str(res))
+                    break
+        except lxml.etree.XPathEvalError:
+            logger.exception("When trying to find author from XPath")
+
+    if not author and args.author_from_csss and tree is not None:
+        try:
+            for res in tree.cssselect(args.author_from_csss):
+                if res.text is not None:
+                    author = get_regex_first_group(
+                        args.csss_author_regex, str(res.text)
+                    )
+                    break
+        except (cssselect.parser.SelectorSyntaxError, lxml.etree.XPathEvalError):
+            logger.exception("When trying to find author from a CSS selector")
+    return author or attr_parser.author
+
+
+def do_session_http_get(session, url, timeout=2, max_len_kb=0, encoding=None):
+    """Do a HTTP(S) GET request for the URL in the context of session,
+    subjected to the limits imposed for timeout (in seconds), max_len_kb
+    (in kilobytes) and using the given encoding to return the resulting page
+    as a *text* string.
+
+    Returns the text and the request object. For exceptions, the text will be
+    None and more error information must be inferred from the request object.
+    """
+    page_text = None
     req = None
-    page_text = ""
-    tree = None
     try:
         logger.info("Following URL %s", url)
-        req = session.get(url, timeout=args.http_timeout, stream=True)
-        if req.url in used_urls:
-            return None
-        if args.encoding:
-            req.encoding = args.encoding
-        used_urls.add(req.url)
-        chunk_size = 1024 * min(100, args.max_page_length)
+        req = session.get(url, timeout=timeout, stream=True)
+        logger.debug("Request returned status code: %d", req.status_code)
+        logger.debug("Request headers: %s", req.request.headers)
+        logger.debug("Response headers: %s", req.headers)
+        logger.debug("Cookies: %s", session.cookies)
+        if encoding:
+            req.encoding = encoding
+        chunk_size = 1024 * min(100, max_len_kb)
         if req.status_code == 200:
+            page_text = ""
             consumed_size = 0
             for chunk in req.iter_content(chunk_size=chunk_size, decode_unicode=True):
-                if consumed_size >= 1024 * args.max_page_length:
+                if consumed_size >= 1024 * max_len_kb:
                     break
                 consumed_size += len(chunk)
-                attr_parser.feed(chunk)
+                if type(chunk) == bytes:
+                    logger.warning("Unexpected binary return, trying to fix.")
+                    chunk = chunk.decode("utf-8")
                 page_text += chunk
-        else:
-            description += "Page returned status code %d<br/>" % req.status_code
     except (
         urllib3.exceptions.ReadTimeoutError,
         requests.exceptions.Timeout,
     ):
         logger.exception("When downloading %s", url)
         # We should handle this somehow.
-        return None
+        page_text = None
     finally:
         if req:
             req.close()
+    return page_text, req
+
+
+def make_feed_item_follow(session, url, used_urls, args, link_text, base_attrs):
+    page_text, req = do_session_http_get(
+        session, url, args.http_timeout, args.max_page_length, args.encoding
+    )
+    if not page_text:
+        return None
+    if req.url in used_urls:
+        return None
 
+    used_urls.add(req.url)
+    attr_parser = CollectAttributesParser()
+    description = ""
+    if req.status_code == 200:
+        attr_parser.feed(page_text)
+    else:
+        description += "Page returned status code %d<br/>" % req.status_code
     if attr_parser.description:
         description = attr_parser.description
+    else:
+        description = link_text
 
     # Give a meaningful title for this entry.
     orig_title = attr_parser.title or link_text or attr_parser.canonical or req.url
     clean_title = make_clean_title(args, orig_title)
     if clean_title == base_attrs.title:
         # The title is the same as the one from base url, a typical thing
         # from horribly-designed news pages (and also happens on a
         # government site I need to consult from time to time), so
         # replace it with the contents of the link text, which should
         # give a bit more useful information for the reader.
         description += "Original title: %s<br/>" % orig_title
         clean_title = link_text[: args.max_title_length]
 
-    description += "Link text: %s" % link_text
     item_url = attr_parser.canonical or req.url
-
     tree = None
     try:
         tree = lxml.html.document_fromstring(page_text)
     except lxml.etree.ParserError:
         logger.exception(
             "Failed to parse document, some information won't be available"
         )
 
     date = find_item_date(args, attr_parser, req, tree, link_text, item_url)
     if args.require_dates and not date:
         # We need a date but the page have none. Skip this entry.
         logger.info("Ignoring feed entry without date %s", url)
         return None
+    author = find_item_author(args, attr_parser, tree)
     if args.with_body and tree is not None:
         bodyhtml = make_item_body(args, page_text, tree)
         if bodyhtml:
             description = bodyhtml
     if attr_parser.tags:
         categories = attr_parser.tags
     elif attr_parser.section:
@@ -558,15 +638,15 @@
         categories = None
     if date:
         # PyRSS2Gen ignores tzinfos and requires the date to be explicitly in UTC.
         date = datetime.datetime.fromtimestamp(date.timestamp(), datetime.timezone.utc)
     return PyRSS2Gen.RSSItem(
         title=clean_title,
         link=item_url,
-        author=attr_parser.author,
+        author=author,
         description=description,
         guid=PyRSS2Gen.Guid(req.url),
         categories=categories,
         pubDate=date,
     )
 
 
@@ -592,15 +672,15 @@
         pubDate=date,
     )
 
 
 def write_feed(rss, args):
     if args.output:
         logger.debug("Writing feed to %s", args.output)
-        with open(args.output, "w") as fp:
+        with open(args.output, "w", encoding="utf-8") as fp:
             rss.write_xml(fp, encoding="utf-8")
     else:
         logger.debug("Writing feed to stdout")
         rss.write_xml(sys.stdout, encoding="utf-8")
 
 
 def make_exception_feed(exc, args=None):
@@ -654,73 +734,138 @@
         if itm[1] and args.date_from_text:
             date = try_date_from_str(itm[1], args.date_from_text, args.text_date_fmt)
             if date:
                 print("    text-date: " + str(date))
         print("")
 
 
-class EmptyCookieJar(http.cookiejar.CookieJar):
-    """A cookie jar that ignores all cookies."""
-
-    def set_cookie(self, cookie, *args, **kwargs):
-        """Method to "set" a cookie.  Actually ignores it."""
-        return
-
-
 def get_start_page(args, session, base_attrs, link_grabber, base_url):
     logger.info("Downloading start URL %s", base_url)
-    page_content = ""
-    req = None
-    try:
-        req = session.get(base_url, timeout=args.http_timeout, stream=True)
-        if args.encoding:
-            req.encoding = args.encoding
-        chunk_size = 1024 * min(100, args.max_first_page_length)
-        consumed_size = 0
-        for chunk in req.iter_content(chunk_size=chunk_size, decode_unicode=True):
-            if consumed_size >= 1024 * args.max_first_page_length:
-                break
-            consumed_size += len(chunk)
-            page_content += chunk
-    finally:
-        if req:
-            req.close()
+    page_content, req = do_session_http_get(
+        session, base_url, args.http_timeout, args.max_first_page_length, args.encoding
+    )
 
     base_attrs.reset_parser()
     base_attrs.feed(page_content)
 
     link_grabber.reset_parser()
     link_grabber.base_url = base_attrs.base or req.url
     link_grabber.feed(page_content)
 
     return req
 
 
-def make_feed(args):
-    session = requests.Session()
-    session.headers = {
+def make_accept_language_header(args):
+    """Build a acceptable Accept-Language HTTP header."""
+    langs = []
+    if args.lang:
+        for lang in args.lang:
+            normalized = normalize_rfc1766_lang_tag(lang)
+            langs.append(normalized if normalized else lang)
+
+    if not langs:
+        locale = os.getenv("LANG")
+        if locale:
+            locale = locale.split(".")[0]
+            normalized = normalize_rfc1766_lang_tag(locale)
+            if normalized:
+                langs.append(normalized)
+
+    q = 0.8
+    qualified = []
+    for lang in langs:
+        qualified.append("%s;q=%.01f" % (lang, q))
+        if q > 0.3:
+            q -= 0.2
+
+    if qualified:
+        return ",".join(qualified)
+    else:
+        return None
+
+
+def make_default_http_headers(args):
+    headers = {
         "User-Agent": args.user_agent,
+        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8",
+        "Accept-Encoding": "gzip, deflate",
+        "Upgrade-Insecure-Requests": "1",
+        "Sec-Fetch-Dest": "document",
+        "Sec-Fetch-Mode": "navigate",
+        "Sec-Fetch-Site": "none",
+        "Sec-Fetch-User": "?1",
+        "TE": "trailers",
     }
 
-    if args.no_cookies:
-        session.cookies = EmptyCookieJar()
+    accept_language = make_accept_language_header(args)
+    if accept_language:
+        headers["Accept-Language"] = accept_language
+
+    if args.header:
+        for header_value in args.header:
+            pair = header_value.split(":", 1)
+            value = pair[1].lstrip() if len(pair) == 2 else ""
+            headers[pair[0].strip()] = value
+
+    return headers
+
+
+class ControlledCookiePolicy(http.cookiejar.DefaultCookiePolicy):
+    """A cookie policy with a simple read-only/read-write switch."""
+
+    def __init__(self):
+        self.read_only = False
+        http.cookiejar.DefaultCookiePolicy.__init__(self)
+
+    def set_ok(self, cookie, request):
+        if self.read_only:
+            return False
+        return http.cookiejar.DefaultCookiePolicy.set_ok(self, cookie, request)
+
+
+def set_cookie_options_for_session(session, args):
+    """Set the cookie options for the session."""
+
+    policy = ControlledCookiePolicy()
+    session.cookies = requests.cookies.RequestsCookieJar(policy=policy)
+
+    if args.cookie:
+        policy.read_only = False
+        for cookie_spec in args.cookie:
+            c = http.cookies.SimpleCookie(cookie_spec)
+            logger.debug("New custom cookie parsed as %s", repr(c))
+            for key, value in c.items():
+                session.cookies[key] = value
+
+    policy.read_only = bool(args.no_cookies)
+
+
+def make_feed(args):
+    session = requests.Session()
+    session.headers = make_default_http_headers(args)
+    set_cookie_options_for_session(session, args)
 
     base_attrs = CollectAttributesParser()
     link_grabber = CollectLinksParser(
         args.link_pattern, args.ignore_pattern, args.max_links, None
     )
     link_grabber.qs_cleanup_rx_list = args.qs_remove_param
 
     for curr_url in args.urls:
         req = get_start_page(args, session, base_attrs, link_grabber, curr_url)
         if link_grabber.limit_reached:
             break
         if not "Referer" in session.headers:
             session.headers["Referer"] = req.url
 
+    # Handle fetch metadata headers according to
+    # https://w3c.github.io/webappsec-fetch-metadata/
+    if "Sec-Fetch-Site" in session.headers:
+        session.headers["Sec-Fetch-Site"] = "same-origin"
+
     if args.test:
         test_links(link_grabber, args)
         return
 
     # URLs that where already processed (considering redirects).
     used_urls = set()
     base_links = link_grabber.links
@@ -752,14 +897,36 @@
         lastBuildDate=datetime.datetime.now(datetime.timezone.utc),
         language=base_attrs.language,
         items=rss_items,
     )
     write_feed(rss, args)
 
 
+def set_locale(args):
+    """Set locale for this application, using both the default "best effort"
+    approach and the explicit locale from command line.
+    """
+
+    if args.locale:
+        locale.setlocale(locale.LC_TIME, args.locale)
+        return
+
+    loc = None
+    candidates = ["LC_ALL", "LC_TIME", "LANG"]
+    for cand in candidates:
+        loc = os.getenv(cand)
+        if loc:
+            break
+    if loc:
+        try:
+            locale.setlocale(locale.LC_TIME, loc)
+        except locale.Error:
+            logger.warning("Ignoring wrong/unknown locale %s", loc)
+
+
 def main():
     parser = argparse.ArgumentParser(
         description=(
             "newslinkrss generates RSS feeds from websites that do not "
             "provide their own. This is done by loading a given URL and "
             "collecting links that matches a pattern, given as a regular "
             "expression, to gather the relevant information, optionally "
@@ -789,35 +956,39 @@
         type=int,
         help="Maximum length of a feed title, in characters.",
     )
 
     parser.add_argument(
         "-p",
         "--link-pattern",
-        action="store",
-        default=".+",
+        action="append",
+        default=None,
         metavar="REGEX",
         help=(
             "A regular expression to filter the URLs of links that the "
-            "script will follow or capture to generate every feed item."
+            "script will follow or capture to generate every feed item. "
+            "This option can be used multiple times, a URL matching any "
+            "expression will be accepted."
         ),
     )
 
     parser.add_argument(
         "-i",
         "--ignore-pattern",
-        action="store",
+        action="append",
         default=None,
         metavar="REGEX",
         help=(
             "A regular expression used to ignore URLs even if they match "
             "--link-pattern. This may be used to prevent unwanted items "
             "from appearing in the feed while keeping the link pattern "
             "simpler (i.e. no need to make that regex excessively complex "
-            "by embedding the ignored patterns in it)."
+            "by embedding the ignored patterns in it). This option can be "
+            "used multiple times, a URL matching any expression will be "
+            "ignored."
         ),
     )
 
     parser.add_argument(
         "-T",
         "--title",
         action="store",
@@ -1055,14 +1226,74 @@
             "a substring from it, and then parsing it as date and time. If "
             "this format is not given or empty, the code will try to "
             "interpret it as some common date/time formats."
         ),
     )
 
     parser.add_argument(
+        "--author-from-xpath",
+        action="store",
+        default=None,
+        metavar="XPATH_EXPRESSION",
+        help=(
+            "Use a XPath expression to get the author of an item, allowing to "
+            "find authors from any element in the page, which is particularly "
+            "useful for sites that do not cite them in the standard metadata. "
+            "Notice that options --author-from-xpath and --xpath-author-regex "
+            "work together as a pipeline, first getting the author name "
+            "from the page and the second filtering optionally selecting a "
+            "substring from it."
+        ),
+    )
+
+    parser.add_argument(
+        "--xpath-author-regex",
+        action="store",
+        default="(.+)",
+        metavar="REGEX",
+        help=(
+            "A regular expression containing a single capture group that "
+            "will be used to select the part of the text returned by "
+            "--author-from-xpath and use it as the author name. Example: "
+            "'by\\s+(.+)' will remove the 'by ' prefix from a byline, "
+            "returning only the name."
+        ),
+    )
+
+    parser.add_argument(
+        "--author-from-csss",
+        action="store",
+        default=None,
+        metavar="CSS_SELECTOR",
+        help=(
+            "Use a CSS Selector to get the author of an item, allowing to "
+            "find authors from any element in the page, which is particularly "
+            "useful for sites that do not cite them in the standard metadata. "
+            "Notice that options --author-from-csss and --csss-author-regex "
+            "work together as a pipeline, first getting the author name "
+            "from the page and the second filtering optionally selecting a "
+            "substring from it."
+        ),
+    )
+
+    parser.add_argument(
+        "--csss-author-regex",
+        action="store",
+        default="(.+)",
+        metavar="REGEX",
+        help=(
+            "A regular expression containing a single capture group that "
+            "will be used to select the part of the text returned by "
+            "--author-from-csss and use it as the author name. Example: "
+            "'by\\s+(.+)' will remove the 'by ' prefix from a byline, "
+            "returning only the name."
+        ),
+    )
+
+    parser.add_argument(
         "--log",
         action="store",
         type=str,
         default="WARNING",
         metavar="LOG_LEVEL",
         help=("Define a log level. Valid values are " + ", ".join(USER_LOG_LEVELS)),
     )
@@ -1293,14 +1524,70 @@
         help="Use this explicit character encoding instead of detecting it "
         "automatically. Usually only required for pages with incorrect "
         "charset information which cause the feed to also be presented "
         'in the wrong encoding (aka "mojibake").',
     )
 
     parser.add_argument(
+        "--lang",
+        action="append",
+        type=str,
+        default=None,
+        metavar="LANGUAGE_CODE",
+        help=(
+            "Ask the site to return the content in this particular language, "
+            "if available. Languages must be specified in ISO 639 or RFC 1766 "
+            "codes (e.g. en, en-US, pt-BR, de-DE). This option may be used "
+            "several times if required and the order in which the options "
+            "are given will be the preference order of the languages. If no "
+            "option is given and environment variable LANG is set, "
+            "newslinkrss will try to get a language code from it. Internally, "
+            "this sets the HTTP Accept-Language header to the prescribed "
+            "value(s)."
+        ),
+    )
+
+    parser.add_argument(
+        "--cookie",
+        action="append",
+        type=str,
+        default=None,
+        metavar="COOKIE_DEFINITION",
+        help=(
+            "Add an arbitrary HTTP cookie to all requests sent to the server. "
+            "These cookies may be overwritten by cookies set by the server "
+            "and then the new ones will be sent in subsequent requests (if "
+            "--follow is used). These explicitly requested cookies are sent "
+            "even if option --no-cookies is used but, in this case, the "
+            "server will not be able to change or replace them. "
+            "The cookie definition is the same used for the Set-Cookie HTTP "
+            "header as defined in RFC 2965 and can be pretty complex. The "
+            "simplest form (NAME=VALUE) can be used ofr the majority of "
+            "cases, however. "
+            "This option may be repeated as many times as necessary."
+        ),
+    )
+
+    parser.add_argument(
+        "-H",
+        "--header",
+        action="append",
+        type=str,
+        default=None,
+        metavar="HTTP_HEADER",
+        help=(
+            "Add an arbitrary HTTP header to all requests send to the "
+            "destination server. Headers must be specified in format "
+            '"Name: Value" and will be passed to destination almost verbatim, '
+            "with only basic whitespace stripping. This option may be "
+            "repeated as many times as necessary."
+        ),
+    )
+
+    parser.add_argument(
         "-t",
         "--http-timeout",
         action="store",
         default=2.0,
         type=float,
         metavar="SECONDS",
         help="Timeout for HTTP(S) requests, in seconds",
@@ -1315,14 +1602,30 @@
             "persisted across invocations of this command, this will only "
             "have any effect when using --follow, typically for sites that "
             "use cookies to detect too many requests in a row."
         ),
     )
 
     parser.add_argument(
+        "--locale",
+        action="store",
+        type=str,
+        default=None,
+        help=(
+            "Use this locale for parsing dates and times. By default, "
+            "newslinkrss will use the locale from environment variables and "
+            "ignore any failure. If this option is used, it will use the "
+            "given locale and abort in the event of a failure (e.g. locale "
+            "not available). If you want to keep the default best-effort "
+            "strategy for a non-default locale, set LC_ALL for newslinkrss "
+            "(i.e. call with 'LC_ALL=pt_BR.UTF-8 newslinkrss <options>')."
+        ),
+    )
+
+    parser.add_argument(
         "-E",
         "--no-exception-feed",
         action="store_true",
         default=False,
         help=(
             "Do not generate feed entries for runtime errors. "
             "The default behavior is to have the information about any "
@@ -1350,14 +1653,18 @@
         nargs="+",
         metavar="URL",
         help="URL of the website to generate the feed.",
     )
 
     args = parser.parse_args()
     set_log_level(args)
+    set_locale(args)
+
+    logger.debug("URL accept pattern: %s", args.link_pattern)
+    logger.debug("URL ignore pattern: %s", args.ignore_pattern)
 
     try:
         make_feed(args)
     except Exception as exc:
         logger.exception("Unhandled exception")
         if args.no_exception_feed:
             raise exc
```

### Comparing `newslinkrss-0.8.0/newslinkrss.egg-info/PKG-INFO` & `newslinkrss-0.9.0/newslinkrss.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 Metadata-Version: 2.1
 Name: newslinkrss
-Version: 0.8.0
+Version: 0.9.0
 Summary: Generate RSS feeds from generic sites
 Home-page: https://sr.ht/~ittner/newslinkrss/
 Author: Alexandre Erwin Ittner
 Author-email: alexandre@ittner.com.br
 License: GPLv3
 Description: # About
         
         newslinkrss generates RSS feeds from websites that do not provide their own.
-        This is done by loading a given URL and collecting links that matches a
-        pattern, given as a regular expression, to gather the relevant information,
-        optionally visiting them to get more details and even processing the target
-        pages with XPath and CSS Selectors if required. It basically works as a
-        purpose specific crawler or scraper.
+        This is done by loading URLs and collecting links that matches patterns,
+        given as a regular expression, to gather the relevant information, optionally
+        visiting them to get more details and even processing the target pages with
+        XPath and CSS Selectors if required. It basically works as a purpose specific
+        crawler or scraper.
         
         The results are printed as a RSS feed to stdout or, optionally, to a file. The
         simplest way to use it is just configure your **local** feed reader, like
         [Liferea](https://lzone.de/liferea/) or [Newsboat](https://newsboat.org/), to
         use a "command" source and pass the correct command line arguments to generate
         a suitable feed -- this allows you to centralize the configuration in the
         reader itself and let it handle update times, etc.
@@ -77,25 +77,27 @@
         other user-level or system-wide components and make experimentation with
         development versions easier. In this case, just do:
         
             python3 -m venv my-venv
             . my-venv/bin/activate
             pip install -U .
         
-        
         newslinkrss depends on a few libraries, this will ensure all them are also
         installed correctly.
         
         
         
         # Usage examples
         
         newslinkrss is lacking a lot of documentation, but the following examples
-        can show a bit of what it can and can not do. A complete list of options
-        can be read by typing `newslinkrss --help`.
+        can show a bit of what it can and can not do. To make understanding easier,
+        examples uses mostly the long, verbose, form of some options even when
+        abbreviations are available. A complete list of options, abbreviations,
+        default values, etc. can be read by typing `newslinkrss --help`.
+        
         
         
         ### Simplest case
         
         The simplest use case is just load a website, select all links matching a
         pattern and expose a feed using the text of that link as description and
         setting the publish date to the date and time that the command was run. For
@@ -116,15 +118,15 @@
         get information that it not is available from the URL or anchor text.
         Option `--follow` (shortcut `-f`) will make newslinkrss load the candidate
         target page and look for more data there. By default, it automatically
         captures the title of the page as the title of the feed entry, keeps the
         summary from anchor text, and loads author information and the page
         publishing and update dates and times from the page metadata (**if** this
         information is available in some common format, like
-        [Open Graph](https://ogp.me/) or Twitter cards.
+        [Open Graph](https://ogp.me/ ) or Twitter cards.
         
         Reuters [killed](https://news.ycombinator.com/item?id=23576022) its RSS feeds
         in mid 2020, so let's take them as an example and use newslinkrss to bring
         the feed back to life and right into our news readers. Our criteria will be:
         
         - First we must find every link that appears as plain HTML on the front page:
           https://www.reuters.com/ There is an infinite scroll and more links are
@@ -138,28 +140,28 @@
           https://www.reuters.com/world/europe/eu-proposes-create-solidarity-fund-ukraines-basic-needs-2022-03-18/
           Notice they all are in domain "https://www.reuters.com/", have at least one
           section ("/world/europe/") that is followed by part of the title and the
           publish date. This format is really great, as it allows us to ignore
           anything that does not look like a news article on the spot. So, a good
           pattern will be `'https://www.reuters.com/.+/.+\d{4}-\d{2}-\d{2}.+'`;
         
-        - newslinkrss deduplicates URLs automatically, so we don't need to worry if we
-          end up capturing the same link twice;
+        - newslinkrss deduplicates URLs automatically, so we don't need to worry if
+          we end up capturing the same link twice;
         
         - Target pages have Open Graph meta tags, so by just following them we can
           get accurate publish dates and times with no extra effort. Better yet, as
           we know that **all** news pages that we want have them, we can also instruct
           newslinkrss to ignore any page without a valid date, preventing any non-news
           article, captured by accident, from appearing in our feed. This is done
           with option `--require-dates`;
         
         - All page titles are something like "The actual headline | Reuters". This
           format is nice for a website but not so for feed items: the "| Reuters"
           part is not only redundant (the feed title already tells us about the
-          source of the article) but also noise, as it makes scanning through the
+          source of the article) but also noisy, as it makes scanning through the
           headlines harder. newslinkrss has an option `--title-regex` for exactly
           this use case of cleaning up redundant text from titles. It accepts a
           regular expression with a single capture group; if the expression matches,
           the text from the group will be used as the title, otherwise the original
           text will be used (so we don't loose titles if something changes at the
           source, for example). For this case, a good choice would be
           `--title-regex '(.+)\s+\|'` .
@@ -196,19 +198,19 @@
         
         Complete feeds are the ones which include the full text of the article with
         it, instead of just a summary and a link. They are really nice as we can
         read everything in the news aggregator itself. A good item body should be
         mostly static and clean HTML (so no scripts, interactive content, aggressive
         formatting, etc.) leaving everything else to the aggregator to handle.
         
-        Let's extend the previous example from Reuters website: as we are already
-        following and downloading the links, there is no much extra work to
-        generate the full feed from it. Option `--with-body` will copy the entire
-        contents of the "body" element from the page into the feed, just removing a
-        few obviously unwanted tags (scripts, forms, etc.).
+        So let's extend the previous example from Reuters website: as we are already
+        following and downloading the links, there is no much extra work to generate
+        the full feed from it. Option `--with-body` will copy the entire contents of
+        the "body" element from the page into the feed, just removing a few obviously
+        unwanted tags (scripts, forms, etc.).
         
         Including the entire body works for every case, but for this site we can
         filter a bit more and pick only actual text of the news article, ignoring
         unwanted noise like menus, sidebars, links to other news, etc. Running a
         quick "inspect element" in Firefox shows us that there is a single "article"
         element in the pages and that it has the text we want. newslinkrss allows
         using both XPath expressions and CSS Selectors to pick particular elements
@@ -314,32 +316,45 @@
           `--follow` every candidate link, downloading the target page and looking
           for  the title there.
         
         - As we are already following, there is no much extra effort to also
           generate a complete feed. The full text of the article is in an "article"
           element, so we can use `--body-xpath "//article"` here too.
         
+        - The target page has no author information in its metadata so newslinkrss
+          will not be able to find their names automatically. However, it has a link
+          to the list of articles from the same author in format
+          `<a href="/autor/xxxxxxxx">Author Name</a>` and we can use the prefix
+          from attribute `href` to pick it with XPath (using option
+          `--author-from-xpath`) or CSS Selectors (with `--author-from-csss`). The
+          CSS approach is simpler for this particular case, so let's use an
+          `--author-from-csss 'a[href^="/autor/"]'`. While not required for this
+          site (name is the only child element of "a"), some sites may prefix the
+          author name with a "by "; For these cases, we could also use options
+          `--csss-author-regex` and `--xpath-author-regex` to select only the name
+          with a regular expression. Also notice that author is an optional element
+          in both RSS and Atom, but it is nice to have it appearing in the correct
+          fields in the news reader so we can use this information for filtering
+          reading lists, for example.
+        
         The resulting command line is:
         
-            newslinkrss -p '.+/\d{4}/\d{2}/\d{2}/.+' \
+            newslinkrss \
+                -p 'https://revistaquestaodeciencia.com.br/.*\d{4}/\d{2}/\d{2}/.+' \
                 --date-from-url '.*/(\d{4}/\d{2}/\d{2})/.*' \
                 --url-date-fmt '%Y/%m/%d' \
                 --follow \
                 --with-body \
                 --body-xpath "//article" \
-                --max-links 50 \
+                --author-from-csss 'a[href^="/autor/"]' \
                 --max-page-length 512 \
                 --http-timeout 4 \
+                --title-regex '(.+)\s+\|' \
                 'https://revistaquestaodeciencia.com.br/'
         
-        To make understanding easier, this example uses the long, verbose, form of
-        some options even when abbreviations are available. For the same reason, some
-        of the options are set to the default values and are not strictly required
-        but they are listed anyway. See `newslinkrss --help` for details.
-        
         
         ### Using complex XPath expressions
         
         Sometimes we need to fight really hard to get the date that a particular item
         was last updated. Taking GitHub issues as an example: while GH provides Atom
         feeds for releases and commits (but always to specific branches), there is
         no equivalent for issues and pull requests. Of course, there is an API for
@@ -378,56 +393,60 @@
         helper function to get what the expression will return, for example:
         `$x('(//h3/a/relative-time)[last()]/@datetime')`.
         
         
         
         ### The first example, revisited
         
-        Now that we have a few extra tricks on our sleeves we can check back that
+        Now that we have a few extra tricks in our sleeves we can check back that
         very first example and fix some of its limitations:
         
         - First, we need the correct publish dates; they are neither in the URL nor
-          in the anchor text, so we need to `--follow` the pages and get them from
-          there. The pages also have no metadata for that, but there is a publish
-          date intended for human readers there in this slice of HTML:
-          `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`
-          The important part if that we can use a XPath expression to select that
-          date and then parse it; a good (not optimal! It does not follow CSS rules)
-          would be `--date-from-xpath '//small[@class="text-muted"]/b/text()'` and
-          it will capture the "23/12/2022" from the text node of the inner "b"
-          element, no need to filter it through `--xpath-date-regex` to remove
-          unwanted text, so we can then parse it with `--xpath-date-fmt '%d/%m/%Y'`;
-        
-        - Let's be extra careful with the URL patterns, so we don't follow a
-          random link going to another domain;
+          in the anchor text, so we need to `--follow` the pages and get the dates
+          from there. The pages also have no metadata for that, but they have a
+          publish date intended for human readers in a slice of HTML like this:
+          `<small class="text-muted"><b>23/12/2022</b> - some random text</small>`.
+          We can use a XPath expression to select the date from element "b", a good
+          one (but technically incorrect as it does not follow CSS rules for attribute
+          "class") is `--date-from-xpath '//small[@class="text-muted"]/b/text()'` .
+          It is a bit convoluted but we can replace it with a CSS Selector (and also
+          fix the class attribute issue): `--date-from-csss 'small.text-muted > b'`.
+          It will capture the "23/12/2022" from the text node of inner element "b",
+          no need to filter through `--csss-date-regex` to remove unwanted text, but
+          as the date format is still ambiguous, we need to give an explicit format
+          with option `--csss-date-fmt '%d/%m/%Y'`;
+        
+        - Let's be extra careful with the URL pattern and never capture (or follow!)
+          links pointing to other domains. We can replace it with a more restricted
+          `-p 'https://www.jaraguadosul.sc.gov.br/news/.+'`;
         
         - As we are already following the pages, let's also generate a full feed.
           The relevant part of the articles are inside a "div" element with
           attribute "id" set to "area_impressao" (that's Portuguese for
           "printing_area" and one may imagine it is being used to format the page
           for printing, however there is neither an alternate style sheet nor a
           @media selector for it ... anyway, at least it helps us to select the
           correct text). We can isolate this element with a XPath expression
           `'//div[@id="area_impressao"]'` but this is slightly more complex than
           the equivalent CSS Selector `div#area_impressao` and, as we already used
-          XPath in several examples, let's use a CSSS this time;
+          XPath in several other examples, let's stick with CSSS;
         
         - That site can be a bit slow sometimes, so let's be extra tolerant and
           increase the HTTP timeout to 10 s;
         
         And then we have our fixed command line:
         
             newslinkrss \
                 -p 'https://www.jaraguadosul.sc.gov.br/news/.+' \
                 --http-timeout 10 \
                 --follow \
                 --with-body \
                 --body-csss 'div#area_impressao' \
-                --date-from-xpath '//small[@class="text-muted"]/b/text()' \
-                --xpath-date-fmt '%d/%m/%Y' \
+                --date-from-csss 'small.text-muted > b' \
+                --csss-date-fmt '%d/%m/%Y' \
                 https://www.jaraguadosul.sc.gov.br/noticias.php
         
         ... not perfect, but it gives us a very practical and usable feed!
         
         
         
         ## More useful notes
@@ -442,25 +461,25 @@
         Related options are the following:
         
         - If explicitly used, options `--date-from-xpath`, `--xpath-date-regex`, and
           `--xpath-date-fmt` will allow reading dates from any element in the target
           page which can be found with a XPath expression. Naturally, the target page
           which must be downloaded with `--follow`; The XPath expression must return
           a string (from the inner text or the attributes of an element), the second
-          must optionally provide a regular expression with a single capture group
-          with the date, and the third should give the date format. If no regex is
-          given, all the string will be used and if no date format is given, the code
-          will try some common date formats;
+          is optional, but if given it must provide a regular expression with a single
+          capture group with the date, and the third should give the date format. If
+          no regex is given, all the string will be used and if no date format is
+          given, the code will try some common date formats;
         
         - If explicitly used, options `--date-from-csss`, `--csss-date-regex`, and
           `--csss-date-fmt` work in a similar way as the previous ones, but using
           CSS Selectors instead. They are not as powerful or flexible as XPath, but
           simpler, cleaner, and more suitable for HTML;
         
-        - If explicitly used,  options `--date-from-text` and `--text-date-fmt` allow
+        - If explicitly used, options `--date-from-text` and `--text-date-fmt` allow
           reading the date from the anchor text (i.e., the text inside tag `<a>`)
           associated to a particular entry in the index page; no `--follow` is
           necessary. The first option must provide a regular expression with a single
           capture group for the date (which allows removing non-date parts of the
           string) and the second option should give the date format. If the format is
           not given, the code will try some common date formats;
         
@@ -484,40 +503,54 @@
         These options are tried in this order with the first valid date being picked.
         This way, options explicitly included in command line have priority, with
         higher precendence being given to the ones which may return a "good" date.
         If no date options are listed, or if could not grab a date from the document,
         standard metadata and HTTP headers will be used (in this order).
         
         
+        #### Locale-dependent dates
+        
+        Some date formats depend on the system locale, most common cases being month
+        names (tokens `%b` and `%B`), and the date parsing options will also depend
+        on it to interpret these dates correctly. By default, newslinkrss will use
+        the locale set for the current user, read from environment variables, and
+        ignore any failure if it is not available or is invalid. Option `--locale`
+        allows setting an explicit locale name, so newslinkrss will use it or abort
+        in the event of a failure. If you want to keep the default best-effort
+        approach for a non-default locale, set environment variable LC_ALL when
+        caling newslinkrss (i.e. call with
+        `"LC_ALL=pt_BR.UTF-8 newslinkrss <options>"`).
+        
+        
         
         ### Ignoring URLs
         
         The link pattern (-p) has a counterpart `--ignore-pattern` (shortcut `-i`)
         which also accepts a regular expression and makes `newslinkrss` ignore any
         matching URL. Depending on the amount of information that the website puts on
         the URLs, this can be used for excluding native advertisement, uninteresting
         sections, or other unwanted content from the feed, without support from the
         feed reader and without counting to the total URL limit (`-n`). While it is
         possible to add this ignore rule to the link pattern itself, using `-i`
         prevents that regular expression from becoming excessively complex and makes
-        debugging easier.
+        debugging easier. This option can be used multiple times, a URL that match
+        any of them will be ignored.
         
         
         ### Cleaning URL query strings
         
         Sometimes the source page has URLs with unwanted query string parameters,
         like the [UTM trackers](https://en.wikipedia.org/wiki/UTM_parameters), or
         multiple URLs differing only by irrelevant query string parameters and
         pointing to the same destination page (and therefore confusing the duplicate
         link detection). Option `--qs-remove-param` (shortcut `-Q`) may be used to
         fix this. If the name of a parameter matches the regular expression given in
         this option, that name/value pair will be removed from the URL query string.
         This option may be repeated many times if necessary. Example: `-Q '^utm.+'`
-        (notice the anchor to only match a prefix).
-        
+        (notice the anchor to only match prefixes).
         
         
         ### Excluding body elements
         
         When generating a complete feed we may sometimes end up including some
         unwanted elements from the source page into the item body, usually ads,
         "related news" boxes, section headers, random images, distracting formatting,
@@ -527,15 +560,15 @@
         fragile solution, we can just remove the unwanted elements explicitly.
         
         newslinkrss has tree command line options for this:
         
         - Option `--body-remove-tag` (shortcut `-R`) will remove all occurrences of
           the given tag from the feed body and move their child elements to their
           parents. This can be used to remove formatting while preserving the inner
-          text (e.g. `-R strong`) or to remove images from the body (with `-R  img`,
+          text (e.g. `-R strong`) or to remove images from the body (with `-R img`,
           as "img" elements have no children);
         
         - Option `--body-remove-xpath` (shortcut `-X`) will remove the elements
           given by a XPath expression **and** their children. This is a good way
           to remove banners, divs, etc. from the generated feed;
         
         - Option `--body-remove-csss` (shortcut `-C`) will remove the elements given
@@ -543,14 +576,66 @@
           banners, divs, etc. from the generated and more practical when selecting
           element by their CSS classes.
         
         All three options can be repeated in the command line how many times as
         necessary to express all required rules.
         
         
+        ### Handling request language options
+        
+        Some sites change their rendering, response language, **date formats**, etc.
+        according to the preferred language information sent by the user's browser.
+        By default, newslinkrss uses the "LANG" environment variable to set this
+        language information (it is a bit of an optimization for the most common
+        case where the system language is the same as the one of the browser used for
+        debugging the options for a particular feed). To set a different one, you may
+        overwrite the LANG variable or use option `--lang`. The later option is more
+        flexible as it may be repeated to set several languages in order of preference
+        (e.g. `"--lang pt-BR --lang en-US --lang de-DE"`).
+        
+        To not send any preferred language information to the server, independently
+        of one currently set for the system, clear the LANG variable for the
+        newslinkrss process invocation (e.g. `"LANG='' newslinkrss <other options>"`).
+        
+        
+        ### Managing cookies
+        
+        newslinkrss persists cookies among requests from the same program invocation
+        and forgets them once the program finishes; this is usually the most practical
+        choice for typical use cases, but there is an option `--no-cookies` to disable
+        all cookies if it becomes a problem for a particular source.
+        
+        Conversely, sites may expect a particular cookies to be set to a specific
+        values, for example, to show news from a particular geographic region.
+        Command line option `--cookie` allows the user to define customized cookies
+        to handle these cases. This option supports the complete syntax defined by
+        [RFC 2965](https://www.rfc-editor.org/rfc/rfc2965.html), but a simple
+        `name=value` will work for the majority of use cases. Example:
+        `--cookie 'cookie-banner-consent-accepted=false'`. This option can be
+        repeated as many times as necessary.
+        
+        If user-defined cookies are used together with option `--no-cookies`, the
+        target site will have access to them, but will not be able to change or
+        delete them (by overwriting or redefining the expiry date) or set new ones.
+        This results in a read-only set of cookie jar that can be very useful for
+        sites that require cookies but use them to change behavior in unwanted ways
+        after some number of pages are read.
+        
+        
+        ### Setting arbitrary HTTP headers
+        
+        Some sites my require unusual request options to work correctly. newslinkrss
+        has an option `--header` (shortcut: `-H`) to set any HTTP header for the
+        requests it sends. To use it, just pass the header in format `"NAME: VALUE"`
+        (e.g. `--header 'X-Clacks-Overhead: GNU Terry Pratchett'`). This should not
+        be a common requirement, however. It is also not recommended to use this
+        option for handling language preferences and cookies, as the dedicated
+        options `--lang` and `--cookie` will take care of the specific behavior of
+        these headers.
+        
         
         ### Testing links
         
         newslinkrss has an option `--test` that will skip the feed generation step
         and just print the links and titles that were captured for a particular set
         of options to stdout. That's a simple way to check if a pattern is working
         as intended.
```

### Comparing `newslinkrss-0.8.0/setup.cfg` & `newslinkrss-0.9.0/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = newslinkrss
-version = 0.8.0
+version = 0.9.0
 url = https://sr.ht/~ittner/newslinkrss/
 license = GPLv3
 author = Alexandre Erwin Ittner
 author_email = alexandre@ittner.com.br
 description = Generate RSS feeds from generic sites
 long_description = file: README.md
 long_description_content_type = text/markdown
```

