# Comparing `tmp/genbank-0.75.tar.gz` & `tmp/genbank-0.81.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "genbank-0.75.tar", last modified: Tue Apr 11 20:59:56 2023, max compression
+gzip compressed data, was "genbank-0.81.tar", last modified: Fri May 12 23:04:20 2023, max compression
```

## Comparing `genbank-0.75.tar` & `genbank-0.81.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-04-11 20:59:56.130232 genbank-0.75/
--rw-r--r--   0 katelyn    (501) staff       (20)    35149 2022-02-15 23:16:16.000000 genbank-0.75/LICENSE
--rw-r--r--   0 katelyn    (501) staff       (20)       51 2022-12-13 21:12:02.000000 genbank-0.75/MANIFEST.in
--rw-r--r--   0 katelyn    (501) staff       (20)     3209 2023-04-11 20:59:56.130005 genbank-0.75/PKG-INFO
--rw-r--r--   0 katelyn    (501) staff       (20)     2744 2022-12-13 21:12:02.000000 genbank-0.75/README.md
--rw-r--r--   0 katelyn    (501) staff       (20)        5 2023-04-11 20:58:36.000000 genbank-0.75/VERSION
-drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-04-11 20:59:56.128481 genbank-0.75/genbank/
--rw-r--r--   0 katelyn    (501) staff       (20)        0 2022-02-15 23:20:41.000000 genbank-0.75/genbank/__init__.py
--rw-r--r--   0 katelyn    (501) staff       (20)     3235 2022-03-01 21:08:53.000000 genbank-0.75/genbank/codons.py
--rw-r--r--   0 katelyn    (501) staff       (20)     6602 2023-02-15 02:40:07.000000 genbank-0.75/genbank/feature.py
--rw-r--r--   0 katelyn    (501) staff       (20)     2918 2023-02-07 21:33:49.000000 genbank-0.75/genbank/file.py
--rw-r--r--   0 katelyn    (501) staff       (20)    11229 2023-03-20 20:20:53.000000 genbank-0.75/genbank/locus.py
--rw-r--r--   0 katelyn    (501) staff       (20)      371 2023-04-11 20:58:21.000000 genbank-0.75/genbank/sequence.py
--rw-r--r--   0 katelyn    (501) staff       (20)     2726 2022-03-08 22:07:42.000000 genbank-0.75/genbank/translate.py
-drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-04-11 20:59:56.129486 genbank-0.75/genbank.egg-info/
--rw-r--r--   0 katelyn    (501) staff       (20)     3209 2023-04-11 20:59:56.000000 genbank-0.75/genbank.egg-info/PKG-INFO
--rw-r--r--   0 katelyn    (501) staff       (20)      330 2023-04-11 20:59:56.000000 genbank-0.75/genbank.egg-info/SOURCES.txt
--rw-r--r--   0 katelyn    (501) staff       (20)        1 2023-04-11 20:59:56.000000 genbank-0.75/genbank.egg-info/dependency_links.txt
--rw-r--r--   0 katelyn    (501) staff       (20)        8 2023-04-11 20:59:56.000000 genbank-0.75/genbank.egg-info/top_level.txt
--rw-r--r--   0 katelyn    (501) staff       (20)     5972 2023-02-27 22:07:26.000000 genbank-0.75/genbank.py
--rw-r--r--   0 katelyn    (501) staff       (20)       38 2023-04-11 20:59:56.130301 genbank-0.75/setup.cfg
--rw-r--r--   0 katelyn    (501) staff       (20)     1397 2022-03-30 22:21:48.000000 genbank-0.75/setup.py
-drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-04-11 20:59:56.129729 genbank-0.75/tests/
--rw-r--r--   0 katelyn    (501) staff       (20)      126 2022-04-07 22:19:14.000000 genbank-0.75/tests/small.fasta
+drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-05-12 23:04:20.889831 genbank-0.81/
+-rw-r--r--   0 katelyn    (501) staff       (20)    35149 2022-02-15 23:16:16.000000 genbank-0.81/LICENSE
+-rw-r--r--   0 katelyn    (501) staff       (20)       51 2022-12-13 21:12:02.000000 genbank-0.81/MANIFEST.in
+-rw-r--r--   0 katelyn    (501) staff       (20)     3209 2023-05-12 23:04:20.889557 genbank-0.81/PKG-INFO
+-rw-r--r--   0 katelyn    (501) staff       (20)     2744 2022-12-13 21:12:02.000000 genbank-0.81/README.md
+-rw-r--r--   0 katelyn    (501) staff       (20)        5 2023-05-12 22:17:30.000000 genbank-0.81/VERSION
+drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-05-12 23:04:20.886922 genbank-0.81/genbank/
+-rw-r--r--   0 katelyn    (501) staff       (20)        0 2022-02-15 23:20:41.000000 genbank-0.81/genbank/__init__.py
+-rw-r--r--   0 katelyn    (501) staff       (20)     3235 2022-03-01 21:08:53.000000 genbank-0.81/genbank/codons.py
+-rw-r--r--   0 katelyn    (501) staff       (20)     6086 2023-05-12 22:39:31.000000 genbank-0.81/genbank/feature.py
+-rw-r--r--   0 katelyn    (501) staff       (20)     2918 2023-02-07 21:33:49.000000 genbank-0.81/genbank/file.py
+-rw-r--r--   0 katelyn    (501) staff       (20)    13299 2023-05-12 22:26:53.000000 genbank-0.81/genbank/locus.py
+-rw-r--r--   0 katelyn    (501) staff       (20)      371 2023-04-11 20:58:21.000000 genbank-0.81/genbank/sequence.py
+-rw-r--r--   0 katelyn    (501) staff       (20)     2726 2022-03-08 22:07:42.000000 genbank-0.81/genbank/translate.py
+drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-05-12 23:04:20.888557 genbank-0.81/genbank.egg-info/
+-rw-r--r--   0 katelyn    (501) staff       (20)     3209 2023-05-12 23:04:20.000000 genbank-0.81/genbank.egg-info/PKG-INFO
+-rw-r--r--   0 katelyn    (501) staff       (20)      330 2023-05-12 23:04:20.000000 genbank-0.81/genbank.egg-info/SOURCES.txt
+-rw-r--r--   0 katelyn    (501) staff       (20)        1 2023-05-12 23:04:20.000000 genbank-0.81/genbank.egg-info/dependency_links.txt
+-rw-r--r--   0 katelyn    (501) staff       (20)        8 2023-05-12 23:04:20.000000 genbank-0.81/genbank.egg-info/top_level.txt
+-rw-r--r--   0 katelyn    (501) staff       (20)     8793 2023-05-05 23:42:46.000000 genbank-0.81/genbank.py
+-rw-r--r--   0 katelyn    (501) staff       (20)       38 2023-05-12 23:04:20.889903 genbank-0.81/setup.cfg
+-rw-r--r--   0 katelyn    (501) staff       (20)     1397 2023-04-12 22:59:11.000000 genbank-0.81/setup.py
+drwxr-xr-x   0 katelyn    (501) staff       (20)        0 2023-05-12 23:04:20.888842 genbank-0.81/tests/
+-rw-r--r--   0 katelyn    (501) staff       (20)      126 2022-04-07 22:19:14.000000 genbank-0.81/tests/small.fasta
```

### Comparing `genbank-0.75/LICENSE` & `genbank-0.81/LICENSE`

 * *Files identical despite different names*

### Comparing `genbank-0.75/PKG-INFO` & `genbank-0.81/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: genbank
-Version: 0.75
+Version: 0.81
 Summary: Code to work with Genbank files
 Home-page: https://github.com/deprekate/genbank
 Author: Katelyn McNair
 Author-email: deprekate@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
```

### Comparing `genbank-0.75/README.md` & `genbank-0.81/README.md`

 * *Files identical despite different names*

### Comparing `genbank-0.75/genbank/codons.py` & `genbank-0.81/genbank/codons.py`

 * *Files identical despite different names*

### Comparing `genbank-0.75/genbank/feature.py` & `genbank-0.81/genbank/feature.py`

 * *Files 12% similar despite different names*

```diff
@@ -47,49 +47,42 @@
 		# convert genbank 1-based indexing to standard 0-based
 		return nint(self.pairs[-1][-1]) - 3
 	
 	def length(self):
 		return len(self.seq())
 
 	def seq(self):
-		seq = ''
-		for n in self.base_locations():
-			seq += self.locus.seq(n,n+1, self.strand)
+		seq = list()
+		for pair in self.pairs:
+			left,right = map(nint, pair)
+			seq.append(self.locus.seq(left-1,right, self.strand))
 		if self.strand > 0:
-			return seq
+			return ''.join(seq)
 		else:
-			return seq[::-1]
-
-	def base_locations(self, full=True):
-		#if full and self.partial() == 'left': 
-		if self.partial() == 'left': 
-			for i in range(-(self.frame()%3),0,1): #range(-((3 - self.frame() % 3) % 3), 0, 1):
-				yield i
-		for left,right in self:
-			#left,right = map(int, [ item.replace('<','').replace('>','') for item in self.pair ] )
-			for i in range(left,right+1):
-				if i < self.locus.length():
-					yield i
-
-	def codon_locations(self, full=True):
-		assert self.type == 'CDS'
-		for triplet in grouper(self.base_locations(full=True), 3):
-			#if triplet[0] >= 0:
-			yield triplet
+			return ''.join(seq[::-1])
 
 	def codons(self):
 		assert self.type == 'CDS'
-		if self.strand > 0:
-			for locations in self.codon_locations():
-				#yield ''.join([self.locus.dna[loc] if loc else '' for loc in locations])
-				yield self.locus.seq()[locations[0]:locations[2]+1]
-		else:
-			for locations in self.codon_locations():
-				#yield rev_comp(''.join([self.locus.dna[loc] if loc else '' for loc in locations]))
-				yield rev_comp(self.locus.seq()[ locations[0] : locations[2]+1 ])
+		dna = self.seq()
+		# should I return partial codons?
+		if self.partial() == 'left':
+			remainder = len(dna) % 3
+			if self.strand > 0:
+				dna = dna[remainder:]
+			else:
+				dna = dna[:-remainder]
+		if self.partial() == 'right':
+			remainder = len(dna) % 3
+			if self.strand > 0:
+				dna = dna[:-remainder]
+			else:
+				dna = dna[remainder:]
+		for triplet in grouper(dna, 3):
+			yield ''.join(triplet)
+		return
 
 	def fna(self):
 		return self.header() + self.seq() + "\n"
 
 	def faa(self):
 		return self.header() + self.translation() + "\n"
```

### Comparing `genbank-0.75/genbank/file.py` & `genbank-0.81/genbank/file.py`

 * *Files identical despite different names*

### Comparing `genbank-0.75/genbank/translate.py` & `genbank-0.81/genbank/translate.py`

 * *Files identical despite different names*

### Comparing `genbank-0.75/genbank.egg-info/PKG-INFO` & `genbank-0.81/genbank.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: genbank
-Version: 0.75
+Version: 0.81
 Summary: Code to work with Genbank files
 Home-page: https://github.com/deprekate/genbank
 Author: Katelyn McNair
 Author-email: deprekate@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
```

### Comparing `genbank-0.75/genbank.py` & `genbank-0.81/genbank.py`

 * *Files 25% similar despite different names*

```diff
@@ -26,42 +26,110 @@
 	if not os.path.exists(x):
 		raise argparse.ArgumentTypeError("{0} does not exist".format(x))
 	return x
 
 def nint(x):
     return int(x.replace('<','').replace('>',''))
 
+def _print(self, item):
+    if isinstance(item, str):
+        self.write(item)
+    else:
+        self.write(str(item))
 
 if __name__ == "__main__":
-	choices = 	['tabular','genbank','fasta', 'fna','faa', 'coverage','rarity','bases','gc','taxonomy','part', 'gff', 'gff3']
-
+	choices = 	['tabular','genbank','fasta', 'fna','faa', 'coverage','rarity','bases','gc','gcfp', 'taxonomy','part', 'gff', 'gff3', 'testcode']
 	usage = '%s [-opt1, [-opt2, ...]] infile' % __file__
 	parser = argparse.ArgumentParser(description='', formatter_class=RawTextHelpFormatter, usage=usage)
 	parser.add_argument('infile', type=is_valid_file, help='input file in genbank format')
 	parser.add_argument('-o', '--outfile', action="store", default=sys.stdout, type=argparse.FileType('w'), help='where to write output [stdout]')
 	parser.add_argument('-f', '--format', help='Output the features in the specified format', type=str, default='genbank', choices=choices)
 	parser.add_argument('-s', '--slice', help='This slices the infile at the specified coordinates. \nThe range can be in one of three different formats:\n    -s 0-99      (zero based string indexing)\n    -s 1..100    (one based GenBank indexing)\n    -s 50:+10    (an index and size of slice)', type=str, default=None)
 	parser.add_argument('-g', '--get', action="store_true")
 	parser.add_argument('-r', '--revcomp', action="store_true")
+	parser.add_argument('-a', '--add', help='This adds features the shell input via < features.txt', type=str, default=None)
 	parser.add_argument('-e', '--edit', help='This edits the given feature key with the value from the shell input via < new_keys.txt', type=str, default=None)
 	parser.add_argument('-k', '--key', help='Print the given keys [and qualifiers]', type=str, default=None)
+	parser.add_argument('-c', '--compare', help='Compares the CDS of two genbank files', type=str, default=None)
 	args = parser.parse_args()
+	args.outfile.print = _print.__get__(args.outfile)
 
 	if not args.get:
 		genbank = File(args.infile)
 	else:
 		#raise Exception("not implemented yet")
 		# not ready yet
 		accession,rettype = args.infile.split('.')
-		with urllib.request.urlopen('http://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nuccore&id=' + accession + '&rettype=' + rettype + '&retmode=text') as response:
+		url = 'http://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=nuccore&id=' + accession + '&rettype=' + rettype + '&retmode=text'
+		with urllib.request.urlopen(url) as response:
 			with tempfile.NamedTemporaryFile() as tmp:
 				shutil.copyfileobj(response, tmp)
 				genbank = File(tmp.name)
 		
-	if args.edit:
+	if args.compare:
+		perfect = partial = total = 0
+		compare = File(args.compare)
+		for (name,locus),( _ ,other) in zip(genbank.items(),compare.items()):
+			pairs = dict()
+			for feature in locus.features(include='CDS'):
+				if feature.strand > 0:
+					pairs[feature.pairs[-1][-1]] = feature.pairs[ 0][ 0]
+				else:
+					pairs[feature.pairs[ 0][ 0]] = feature.pairs[-1][-1]
+			total += len(pairs)
+			for feature in other.features(include='CDS'):
+				if feature.strand > 0:
+					if feature.pairs[-1][-1] in pairs:
+						partial += 1
+						if feature.pairs[ 0][ 0] == pairs[feature.pairs[-1][-1]]:
+							perfect += 1
+				else:
+					if feature.pairs[ 0][ 0] in pairs:
+						partial += 1
+						if feature.pairs[-1][-1] == pairs[feature.pairs[ 0][ 0]]:
+							perfect += 1
+		args.outfile.print(partial)
+		args.outfile.print('\t')
+		args.outfile.print('(')
+		args.outfile.print(partial/total)
+		args.outfile.print(')')
+		args.outfile.print('\t')
+		args.outfile.print(perfect)
+		args.outfile.print('\t')
+		args.outfile.print('(')
+		args.outfile.print(perfect/total)
+		args.outfile.print(')')
+		args.outfile.print('\t')
+		args.outfile.print(total)
+		args.outfile.print('\n')
+		exit()
+	if args.add:
+		# this only works for single sequence files
+		if not sys.stdin.isatty():
+			stdin = sys.stdin.readlines()
+		for locus in genbank:
+			for line in stdin:
+				if args.add == 'genbank':
+					pass
+				elif args.add == 'genemark':
+					if line.startswith(' ') and 'Gene' not in line and '#' not in line:
+						key = 'CDS'
+						n,strand,left,right,*_ = line.split()
+						locus.add_feature(key,strand,[[left,right]],{'note':['genemarkS']})
+				elif args.add == 'glimmer':
+					if not line.startswith('>'):
+						key = 'CDS'
+						n,left,right,(strand,*_),*_ = line.split()
+						locus.add_feature(key,strand,[[left,right]],{'note':['glimmer3']})
+				elif args.add == 'gff':
+					if not line.startswith('#'):
+						name,other,key,left,right,_,strand,_,tags = line.rstrip('\n').split('\t')
+						tags = dict((key,value) for tag in tags.split(';') for key,*value in [tag.split('=')])
+						locus.add_feature(key,strand,[[left,right]],tags)
+	elif args.edit:
 		if not sys.stdin.isatty():
 			stdin = sys.stdin.readlines()
 			#sys.stdin = open('/dev/tty')
 		key,qualifier = args.edit.replace('/',':').split(':')
 		for feature,values in zip(genbank.features(include=[key]), stdin):
 			feature.tags[qualifier] = list()
 			for value in values.rstrip().split('\t'):
@@ -88,76 +156,84 @@
 			left = int(args.slice)
 			right = left+1
 		for name,locus in genbank.items():
 			locus = locus.slice(left,right)
 	if args.key:
 		key,qualifier = args.key.replace('/',':').split(':')
 		for feature in genbank.features(include=key):
-			args.outfile.write('\t'.join(feature.tags[qualifier]))
-			args.outfile.write("\n")
+			args.outfile.print('\t'.join(feature.tags[qualifier]))
+			args.outfile.print("\n")
 	elif args.format == 'genbank':
 		genbank.write(args.outfile)	
 	elif args.format == 'tabular':
 		for feature in genbank.features(include=['CDS']):
-			args.outfile.write(str(feature))
-			args.outfile.write("\t")
-			args.outfile.write(feature.seq())
-			args.outfile.write("\n")
+			args.outfile.print(feature)
+			args.outfile.print("\t")
+			args.outfile.print(feature.seq())
+			args.outfile.print("\n")
 	elif args.format in ['gff', 'gff3']:
 		for locus in genbank:
 			locus.write(args.outfile, args)
-
 	elif args.format in ['fna','faa']:
 		for name,locus in genbank.items():
 			for feature in locus.features(include=['CDS']):
-				args.outfile.write( getattr(feature, args.format)() )
+				args.outfile.print( getattr(feature, args.format)() )
 	elif args.format in ['fasta']:
 		for name,locus in genbank.items():
 			if args.revcomp:
 				locus.dna = locus.seq(strand=-1)
-			args.outfile.write( getattr(locus, args.format)() )
+			args.outfile.print( getattr(locus, args.format)() )
 	elif args.format == 'coverage':
 		cbases = tbases = 0
 		for name,locus in genbank.items():
 			c,t = locus.gene_coverage()
 			cbases += c
 			tbases += t
-		#args.outfile.write( name )
-		#args.outfile.write( '\t' )
-		args.outfile.write( str( cbases / tbases ) )
-		args.outfile.write( '\n' )
+		#args.outfile.print( name )
+		#args.outfile.print( '\t' )
+		args.outfile.print( cbases / tbases )
+		args.outfile.print( '\n' )
 	elif args.format == 'rarity':
 		rarity = dict()
 		for name,locus in genbank.items():
 			for codon,freq in sorted(locus.codon_rarity().items(), key=lambda item: item[1]):
-				args.outfile.write(codon)
-				args.outfile.write('\t')
-				args.outfile.write(str(round(freq,5)))
-				args.outfile.write('\n')
+				args.outfile.print(codon)
+				args.outfile.print('\t')
+				args.outfile.print(round(freq,5))
+				args.outfile.print('\n')
 	elif args.format == 'bases':
 		strand = -1 if args.revcomp else +1
 		for name,locus in genbank.items():
-			args.outfile.write(locus.seq(strand=strand))
-			args.outfile.write('\n')
-	elif args.format == 'gc':
-		for name,locus in genbank.items():
-			args.outfile.write(locus.name())
-			args.outfile.write('\t')
-			args.outfile.write(str(locus.gc_content()))
-			args.outfile.write('\n')
+			args.outfile.print(locus.seq(strand=strand))
+			args.outfile.print('\n')
+	elif args.format in ['gc','gcfp']:
+		for name,locus in genbank.items():
+			args.outfile.print(locus.name())
+			args.outfile.print('\t')
+			if args.format == 'gc':
+				args.outfile.print(locus.gc_content())
+			else:
+				args.outfile.print(locus.gc_fp())
+			args.outfile.print('\n')
 	elif args.format == 'taxonomy':
 		for name,locus in genbank.items():
-			args.outfile.write(locus.groups['SOURCE'][0].replace('\n','\t').replace('            ','').replace(';\t','; ') )
-			args.outfile.write('\n')
+			args.outfile.print(locus.groups['SOURCE'][0].replace('\n','\t').replace('            ','').replace(';\t','; ') )
+			args.outfile.print('\n')
 	elif args.format in ['part']:
 		folder = args.outfile.name if args.outfile.name != '<stdout>' else ''
 		for name,locus in genbank.items():
 			with open(os.path.join(folder,name + '.fna'), 'w') as f:
 				f.write('>')
 				f.write(name)
 				f.write('\n')
 				f.write(locus.seq())
 				f.write('\n')
+	elif args.format == 'testcode':
+		for name,locus in genbank.items():
+			args.outfile.print(locus.name())
+			args.outfile.print('\t')
+			args.outfile.print(locus.testcode())
+			args.outfile.print('\n')
```

### Comparing `genbank-0.75/setup.py` & `genbank-0.81/setup.py`

 * *Files identical despite different names*

