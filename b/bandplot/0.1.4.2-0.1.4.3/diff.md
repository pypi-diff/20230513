# Comparing `tmp/bandplot-0.1.4.2-py3-none-any.whl.zip` & `tmp/bandplot-0.1.4.3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 9614 bytes, number of entries: 9
--rw-rw-r--  2.0 unx       26 b- defN 23-May-08 02:39 bandplot/__init__.py
--rw-rw-r--  2.0 unx    28110 b- defN 23-May-08 02:39 bandplot/plots.py
--rw-rw-r--  2.0 unx     6111 b- defN 23-May-08 02:39 bandplot/readdata.py
--rw-rw-r--  2.0 unx    15638 b- defN 23-May-08 02:39 bandplot/wrapper.py
--rw-rw-r--  2.0 unx     2901 b- defN 23-May-08 02:39 bandplot-0.1.4.2.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-May-08 02:39 bandplot-0.1.4.2.dist-info/WHEEL
--rw-rw-r--  2.0 unx       86 b- defN 23-May-08 02:39 bandplot-0.1.4.2.dist-info/entry_points.txt
--rw-rw-r--  2.0 unx        9 b- defN 23-May-08 02:39 bandplot-0.1.4.2.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      711 b- defN 23-May-08 02:39 bandplot-0.1.4.2.dist-info/RECORD
-9 files, 53684 bytes uncompressed, 8390 bytes compressed:  84.4%
+Zip file size: 10214 bytes, number of entries: 9
+-rw-rw-r--  2.0 unx       26 b- defN 23-May-12 23:05 bandplot/__init__.py
+-rw-rw-r--  2.0 unx    32523 b- defN 23-May-12 23:05 bandplot/plots.py
+-rw-rw-r--  2.0 unx     6111 b- defN 23-May-12 23:05 bandplot/readdata.py
+-rw-rw-r--  2.0 unx    16829 b- defN 23-May-12 23:05 bandplot/wrapper.py
+-rw-rw-r--  2.0 unx     2954 b- defN 23-May-12 23:05 bandplot-0.1.4.3.dist-info/METADATA
+-rw-rw-r--  2.0 unx       92 b- defN 23-May-12 23:05 bandplot-0.1.4.3.dist-info/WHEEL
+-rw-rw-r--  2.0 unx       86 b- defN 23-May-12 23:05 bandplot-0.1.4.3.dist-info/entry_points.txt
+-rw-rw-r--  2.0 unx        9 b- defN 23-May-12 23:05 bandplot-0.1.4.3.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      711 b- defN 23-May-12 23:05 bandplot-0.1.4.3.dist-info/RECORD
+9 files, 59341 bytes uncompressed, 8990 bytes compressed:  84.9%
```

## zipnote {}

```diff
@@ -6,23 +6,23 @@
 
 Filename: bandplot/readdata.py
 Comment: 
 
 Filename: bandplot/wrapper.py
 Comment: 
 
-Filename: bandplot-0.1.4.2.dist-info/METADATA
+Filename: bandplot-0.1.4.3.dist-info/METADATA
 Comment: 
 
-Filename: bandplot-0.1.4.2.dist-info/WHEEL
+Filename: bandplot-0.1.4.3.dist-info/WHEEL
 Comment: 
 
-Filename: bandplot-0.1.4.2.dist-info/entry_points.txt
+Filename: bandplot-0.1.4.3.dist-info/entry_points.txt
 Comment: 
 
-Filename: bandplot-0.1.4.2.dist-info/top_level.txt
+Filename: bandplot-0.1.4.3.dist-info/top_level.txt
 Comment: 
 
-Filename: bandplot-0.1.4.2.dist-info/RECORD
+Filename: bandplot-0.1.4.3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## bandplot/__init__.py

```diff
@@ -1,3 +1,3 @@
 
-__version__ = "0.1.4.2"
+__version__ = "0.1.4.3"
```

## bandplot/plots.py

```diff
@@ -17,28 +17,58 @@
     plt.xticks(ticks,labels)
     plt.legend(legend, frameon=False, prop={'size':'medium'}, loc=fig_p.location)
     plt.xlim(arr[0], arr[-1])
     plt.ylim(fig_p.vertical)
     plt.ylabel('Energy (eV)')
     plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
 
+def Noneispin2(arr, bands, ticks, labels, legend, fig_p):
+    fig = plt.figure(figsize=fig_p.size)
+    color = fig_p.color or ['r', 'k']
+    linestyle = fig_p.linestyle or ['-', '-.']
+    linewidth = fig_p.linewidth or [0.8, 0.8]
+    if len(color) == 1:
+        color = [color[0], 'k']
+    if len(linestyle) == 1:
+        linestyle = [linestyle[0], '-.']
+    if len(linewidth) == 1:
+        linewidth = [linewidth[0], 0.8]
+    f = plt.plot(arr[0], bands[0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0])
+    plt.tick_params(axis='y', which='minor', color='gray')
+    plt.axhline(linewidth=0.4, linestyle='-.', c='gray')
+    if len(ticks) > 2:
+        ticks[0],ticks[-1] = arr[0][0],arr[0][-1]
+        for i in ticks[1:-1]:
+            plt.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
+    plt.xticks(ticks,labels)
+    plt.xlim(arr[0][0], arr[0][-1])
+    plt.ylim(fig_p.vertical)
+    plt.ylabel('Energy (eV)')
+    ax = plt.axes()
+    g = ax.plot(arr[1], bands[1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1])
+    ax.set_xlim(arr[1][0], arr[1][-1])
+    ax.set_ylim(fig_p.vertical)
+    ax.axis('off')
+    plt.legend([f[0], g[0]], [legend[1], legend[2]], frameon=False, prop={'size':'medium'}, loc=fig_p.location, alignment='left', title=legend[0], title_fontproperties={'size':'medium'})
+    plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
+
 def Ispin(arr, bands, ticks, labels, legend, fig_p):
     plt.figure(figsize=fig_p.size)
     color = fig_p.color or ['r', 'k']
     linestyle = fig_p.linestyle or ['-', '-.']
     linewidth = fig_p.linewidth or [0.8, 0.8]
     if len(color) == 1:
         color = [color[0], 'k']
     if len(linestyle) == 1:
         linestyle = [linestyle[0], '-.']
     if len(linewidth) == 1:
         linewidth = [linewidth[0], 0.8]
     p_up = plt.plot(arr, bands[0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0])
     p_do = plt.plot(arr, bands[1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1])
-    plt.legend([p_up[0], p_do[0]], ['up', 'down'], frameon=False, prop={'style':'italic', 'size':'medium'}, alignment='left', loc=fig_p.location, title=legend[0], title_fontproperties={'size':'medium'})
+    plt.legend([p_up[0], p_do[0]], ['up', 'down'], frameon=False, prop={'style':'italic', 'size':'medium'}, loc=fig_p.location, alignment='left', title=legend[0], title_fontproperties={'size':'medium'})
     plt.tick_params(axis='y', which='minor', color='gray')
     plt.axhline(linewidth=0.4, linestyle='-.', c='gray')
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
             plt.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
 
@@ -58,16 +88,18 @@
         color = [color[0], 'k']
     if len(linestyle) == 1:
         linestyle = [linestyle[0], '-.']
     if len(linewidth) == 1:
         linewidth = [linewidth[0], 0.8]
     ax1.plot(arr, bands[0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0])
     ax2.plot(arr, bands[1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1])
-    ax1.legend(['up'], frameon=False, prop={'style':'italic', 'size':'medium'}, alignment='left', loc=fig_p.location, title=legend[0], title_fontproperties={'size':'medium'})
-    ax2.legend(['down'], frameon=False, prop={'style':'italic', 'size':'medium'}, alignment='left', loc=fig_p.location)
+    L = ax1.legend([], frameon=False, loc='lower left', title=legend[0], title_fontproperties={'size':'medium'})
+    ax1.add_artist(L)
+    ax1.legend(['up'], frameon=False, prop={'style':'italic', 'size':'medium'}, loc=fig_p.location)
+    ax2.legend(['down'], frameon=False, prop={'style':'italic', 'size':'medium'}, loc=fig_p.location)
     ax1.tick_params(axis='y', which='minor', color='gray')
     ax2.tick_params(axis='y', which='minor', color='gray')
 
     ax1.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.set_yticklabels([])
     if len(ticks) > 2:
@@ -76,19 +108,74 @@
             ax1.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
             ax2.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
 
     ax1.set_xlim(arr[0], arr[-1])
     ax1.set_ylim(fig_p.vertical)
     ax2.set_xlim(arr[0], arr[-1])
     ax2.set_ylim(fig_p.vertical)
-    ax1.set_xticks(ticks,labels[:-1]+[''])
+    if len(labels) > 0:
+        ax1.set_xticks(ticks,labels[:-1]+[''])
+    else:
+        ax1.set_xticks(ticks,labels)
     ax2.set_xticks(ticks,labels)
     ax1.set_ylabel('Energy (eV)')
     plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
 
+def Dispin2(arr, bands, ticks, labels, legend, fig_p):
+    fig, (ax1, ax2) = plt.subplots(1, 2, figsize=fig_p.size)
+    fig.subplots_adjust(wspace=0.0)
+    color = fig_p.color or ['r', 'r', 'k', 'k']
+    linestyle = fig_p.linestyle or ['-', '-', '-.', '-.']
+    linewidth = fig_p.linewidth or [0.8, 0.8, 0.8, 0.8]
+    if len(color) < 4:
+        color = color + [''] * (4 - len(color))
+    if len(linestyle) < 4:
+        linestyle = linestyle + ['-'] * (4 - len(linestyle))
+    if len(linewidth) < 4:
+        linewidth = linewidth + [0.8] * (4 - len(linewidth))
+    f1 = ax1.plot(arr[0], bands[0][0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0], label='1')
+    f2 = ax2.plot(arr[0], bands[0][1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1], label='1')
+    L = ax1.legend([], frameon=False, loc='lower left', title=legend[0], title_fontproperties={'size':'medium'})
+    ax1.add_artist(L)
+    ax1.tick_params(axis='y', which='minor', color='gray')
+    ax2.tick_params(axis='y', which='minor', color='gray')
+
+    ax1.axhline(linewidth=0.4, linestyle='-.', c='gray')
+    ax2.axhline(linewidth=0.4, linestyle='-.', c='gray')
+    ax2.set_yticklabels([])
+    if len(ticks) > 2:
+        ticks[0],ticks[-1] = arr[0][0],arr[0][-1]
+        for i in ticks[1:-1]:
+            ax1.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
+            ax2.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
+
+    ax1.set_xlim(arr[0][0], arr[0][-1])
+    ax1.set_ylim(fig_p.vertical)
+    ax2.set_xlim(arr[0][0], arr[0][-1])
+    ax2.set_ylim(fig_p.vertical)
+    if len(labels) > 0:
+        ax1.set_xticks(ticks,labels[:-1]+[''])
+    else:
+        ax1.set_xticks(ticks,labels)
+    ax2.set_xticks(ticks,labels)
+    ax1.set_ylabel('Energy (eV)')
+    ax1_f = fig.add_subplot(1,2,1)
+    g1 = ax1_f.plot(arr[1], bands[1][0].T, color=color[2], linewidth=linewidth[2], linestyle=linestyle[2])
+    ax1_f.set_xlim(arr[1][0], arr[1][-1])
+    ax1_f.set_ylim(fig_p.vertical)
+    ax1_f.axis('off')
+    ax2_f = fig.add_subplot(1,2,2)
+    g2 = ax2_f.plot(arr[1], bands[1][1].T, color=color[3], linewidth=linewidth[3], linestyle=linestyle[3], label='2')
+    ax2_f.set_xlim(arr[1][0], arr[1][-1])
+    ax2_f.set_ylim(fig_p.vertical)
+    ax2_f.axis('off')
+    ax1.legend([f1[0], g1[0]], [legend[1], legend[2]], frameon=False, prop={'size':'medium'}, loc=fig_p.location, alignment='left', title='up', title_fontproperties={'style':'italic', 'size':'medium'})
+    ax2.legend([f2[0], g2[0]], [legend[1], legend[2]], frameon=False, prop={'size':'medium'}, loc=fig_p.location, alignment='left', title='down', title_fontproperties={'style':'italic', 'size':'medium'})
+    plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
+
 def NoneispinWd(arr, bands, ticks, labels, darr, dele, fill, index_f, elements, width_ratios, legend, fig_p):
     fig, (ax1, ax2) = plt.subplots(1, 2, width_ratios=[1-width_ratios, width_ratios], figsize=fig_p.size)
     fig.subplots_adjust(wspace=0.0)
     color = fig_p.color or ['r']
     linestyle = fig_p.linestyle or ['-']
     linewidth = fig_p.linewidth or [0.8]
 
@@ -115,15 +202,15 @@
                 plt.fill_between(dele[index_f[i][0]].T[index_f[i][1]], darr[index_f[i][0]], 0, alpha=0.2)
 
     ax1.legend(legend, frameon=False, prop={'size':'small'}, loc=fig_p.location)
     ax1.tick_params(axis='y', which='minor', color='gray')
     ax2.minorticks_on()
     ax2.tick_params(axis='both', which='minor', color='gray')
     ax2.set_yticklabels([])
-    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, alignment='left', loc=fig_p.location, title="Density of states", title_fontproperties={'size':'small'})
+    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, loc=fig_p.location, alignment='left', title="Density of states", title_fontproperties={'size':'small'})
     ax1.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.axvline(linewidth=0.4, linestyle='-.', c='gray')
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
             ax1.axvline(i,linewidth=0.4,linestyle='-.',c='gray')
@@ -147,15 +234,15 @@
         color = [color[0], 'k']
     if len(linestyle) == 1:
         linestyle = [linestyle[0], '-.']
     if len(linewidth) == 1:
         linewidth = [linewidth[0], 0.8]
     p_up = ax1.plot(arr, bands[0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0])
     p_do = ax1.plot(arr, bands[1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1])
-    ax1.legend([p_up[0], p_do[0]], ['up', 'down'], frameon=False, prop={'style':'italic', 'size':'small'}, alignment='left', loc=fig_p.location, title=legend[0], title_fontproperties={'size':'small'})
+    ax1.legend([p_up[0], p_do[0]], ['up', 'down'], frameon=False, prop={'style':'italic', 'size':'small'}, loc=fig_p.location, alignment='left', title=legend[0], title_fontproperties={'size':'small'})
     num = len(index_f)
     p_dos = []
     if num + 2 > len(color):
         color = color + [''] * (num + 2 - len(color))
 
     if num + 2 > len(linestyle):
         linestyle = linestyle + ['-'] * (num + 2 - len(linestyle))
@@ -174,15 +261,15 @@
                 plt.fill_between(dele[index_f[i][0]].T[index_f[i][1]], darr[index_f[i][0]], 0, alpha=0.2)
 
     ax1.tick_params(axis='y', which='minor', color='gray')
     ax2.minorticks_on()
     ax2.tick_params(axis='both', which='minor', color='gray')
     ax2.axvline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.set_yticklabels([])
-    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, alignment='left', loc=fig_p.location, title="Density of states", title_fontproperties={'size':'small'})
+    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, loc=fig_p.location, alignment='left', title="Density of states", title_fontproperties={'size':'small'})
     ax1.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.axhline(linewidth=0.4, linestyle='-.', c='gray')
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
             ax1.axvline(i,linewidth=0.4, linestyle='-.', c='gray')
 
@@ -205,16 +292,18 @@
         color = [color[0], 'k']
     if len(linestyle) == 1:
         linestyle = [linestyle[0], '-.']
     if len(linewidth) == 1:
         linewidth = [linewidth[0], 0.8]
     ax1.plot(arr, bands[0].T, color=color[0], linewidth=linewidth[0], linestyle=linestyle[0])
     ax2.plot(arr, bands[1].T, color=color[1], linewidth=linewidth[1], linestyle=linestyle[1])
-    ax1.legend(['up'], frameon=False, prop={'style':'italic', 'size':'small'}, alignment='left', loc=fig_p.location, title=legend[0], title_fontproperties={'size':'small'})
-    ax2.legend(['down'], frameon=False, prop={'style':'italic', 'size':'small'}, alignment='left', loc=fig_p.location)
+    L = ax1.legend([], frameon=False, loc='lower left', title=legend[0], title_fontproperties={'size':'small'})
+    ax1.add_artist(L)
+    ax1.legend(['up'], frameon=False, prop={'style':'italic', 'size':'small'}, loc=fig_p.location)
+    ax2.legend(['down'], frameon=False, prop={'style':'italic', 'size':'small'}, loc=fig_p.location)
     ax1.tick_params(axis='y', which='minor', color='gray')
     ax2.tick_params(axis='y', which='minor', color='gray')
     ax3.minorticks_on()
     ax3.tick_params(axis='both', which='minor', color='gray')
     num = len(index_f)
     p_dos = []
     if num + 2 > len(color):
@@ -235,15 +324,15 @@
             p_dos = p_dos + ax3.plot(dele[index_f[i][0]].T[index_f[i][1]], darr[index_f[i][0]], linewidth=linewidth[i+2], linestyle=linestyle[i+2])
             if fill:
                 plt.fill_between(dele[index_f[i][0]].T[index_f[i][1]], darr[index_f[i][0]], 0, alpha=0.2)
 
     ax3.axvline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.set_yticklabels([])
     ax3.set_yticklabels([])
-    ax3.legend(p_dos, elements, frameon=False, prop={'size':'small'}, alignment='left', loc=fig_p.location, title="Density of states", title_fontproperties={'size':'small'})
+    ax3.legend(p_dos, elements, frameon=False, prop={'size':'small'}, loc=fig_p.location, alignment='left', title="Density of states", title_fontproperties={'size':'small'})
 
     ax1.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax2.axhline(linewidth=0.4, linestyle='-.', c='gray')
     ax3.axhline(linewidth=0.4, linestyle='-.', c='gray')
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
@@ -252,15 +341,18 @@
 
     ax1.set_xlim(arr[0], arr[-1])
     ax1.set_ylim(fig_p.vertical)
     ax2.set_xlim(arr[0], arr[-1])
     ax2.set_ylim(fig_p.vertical)
     ax3.set_xlim(fig_p.horizontal)
     ax3.set_ylim(fig_p.vertical)
-    ax1.set_xticks(ticks,labels[:-1]+[''])
+    if len(labels) > 0:
+        ax1.set_xticks(ticks,labels[:-1]+[''])
+    else:
+        ax1.set_xticks(ticks,labels)
     ax2.set_xticks(ticks,labels)
     ax3.tick_params(axis='x', labelsize='x-small', labelcolor='dimgray', labelrotation=-90, pad=1.5)
     ax1.set_ylabel('Energy (eV)')
     plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
 
 def pdosfiles(darr, dele, fill, index_f, elements, legend, exchange, fig_p):
     plt.figure(figsize=fig_p.size)
@@ -311,15 +403,15 @@
         plt.ylim(fig_p.vertical)
         plt.xlim(fig_p.horizontal)
         plt.ylabel('Energy (eV)')
         plt.xlabel('Density of states, electrons/eV')
 
     plt.axvline(linewidth=0.4, linestyle='-.', c='gray')
     plt.axhline(linewidth=0.4, linestyle='-.', c='gray')
-    plt.legend(p_dos, elements, frameon=False, prop={'size':'medium'}, loc=fig_p.location, title=legend[0], title_fontproperties={'size':'medium'})
+    plt.legend(p_dos, elements, frameon=False, prop={'size':'medium'}, loc=fig_p.location, alignment='left', title=legend[0], title_fontproperties={'size':'medium'})
     plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
 
 # pbandplot
 
 def Broken(arr, fre, ticks, labels, broken, height_ratio, legend, fig_p):
     fig, (ax1, ax2) = plt.subplots(2, 1, sharex=True, height_ratios=[height_ratio, 1-height_ratio], figsize=fig_p.size)
     fig.subplots_adjust(hspace=0.0)
@@ -441,15 +533,15 @@
     elif num < len(elements):
         if num == 1:
             elements = ['$tdos$']
         else:
             elements = elements[:num]
 
     ax3.legend(legend, frameon=False, prop={'size':'small'}, loc=fig_p.location)
-    ax4.legend(p_dos, elements, frameon=False, prop={'size':'small'}, alignment='left', loc=fig_p.location, title="Phonon DOS", title_fontproperties={'size':'small'})
+    ax4.legend(p_dos, elements, frameon=False, prop={'size':'small'}, loc=fig_p.location, alignment='left', title="Phonon DOS", title_fontproperties={'size':'small'})
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
             ax1.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
             ax3.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
 
     ax3.set_xticks(ticks,labels)
@@ -509,15 +601,15 @@
         if num == 1:
             elements = ['$tdos$']
         else:
             elements = elements[:num]
 
     ax1.legend(legend, frameon=False, prop={'size':'small'}, loc=fig_p.location)
     ax2.axvline(linewidth=0.4,linestyle='-.',c='dimgray')
-    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, alignment='left', loc=fig_p.location, title="Phonon DOS", title_fontproperties={'size':'small'})
+    ax2.legend(p_dos, elements, frameon=False, prop={'size':'small'}, loc=fig_p.location, alignment='left', title="Phonon DOS", title_fontproperties={'size':'small'})
     if len(ticks) > 2:
         ticks[0],ticks[-1] = arr[0],arr[-1]
         for i in ticks[1:-1]:
             ax1.axvline(i, linewidth=0.4, linestyle='-.', c='gray')
 
     ax1.set_xticks(ticks,labels)
     ax1.set_ylabel('Frequency (THz)')
@@ -580,10 +672,10 @@
         elements = elements + [''] * (num - len(elements))
     elif num < len(elements):
         if num == 1:
             elements = ['$tdos$']
         else:
             elements = elements[:num]
 
-    plt.legend(p_dos, elements, frameon=False, prop={'size':'medium'}, alignment='left', loc=fig_p.location, title=legend[0], title_fontproperties={'size':'medium'})
+    plt.legend(p_dos, elements, frameon=False, prop={'size':'medium'}, loc=fig_p.location, alignment='left', title=legend[0], title_fontproperties={'size':'medium'})
     plt.savefig(fig_p.output, dpi=fig_p.dpi, transparent=True, bbox_inches='tight')
```

## bandplot/wrapper.py

```diff
@@ -16,31 +16,31 @@
             else:
                 exec('self.%s = %s' %(key, value))
 
 def main():
     parser = argparse.ArgumentParser(description='Plot the band structure or DOS from vaspkit result.',
                                      epilog='''
 Example:
-bandplot -i band.dat -o pband.png -l g m k g -d PDOS* -z
+bandplot -i BAND.dat -o BAND.png -l g m k g -d PDOS* -z
 ''',
                                      formatter_class=argparse.RawDescriptionHelpFormatter)
     parser.add_argument('-v', "--version",    action="version",     version="bandplot "+__version__+" from "+os.path.dirname(__file__)+' (python'+platform.python_version()+')')
     parser.add_argument('-s', "--size",       type=int,   nargs=2,  help='figure size: width, height')
     parser.add_argument('-b', "--divided",    action='store_true',  help="plot the up and down spin in divided subplot")
     parser.add_argument('-y', "--vertical",   type=float, nargs=2,  help="energy (eV) range, default: [-5.0, 5.0]")
-    parser.add_argument('-g', "--legend",     type=str,   nargs=1,  help="legend labels")
+    parser.add_argument('-g', "--legend",     type=str,             nargs='+', help="legend labels", default=[])
     parser.add_argument('-a', "--location",   type=str.lower,       choices=['best', 'upper right', 'upper left', 'lower left', 'lower right', 'right',
                                                                              'center left', 'center right', 'lower center', 'upper center', 'center'],
                                                                     help="arrange the legend location, default: best", default='best')
     parser.add_argument('-c', "--color",      type=str,             nargs='+', help="line color: b, blue; g, green; r, red; c, cyan; m, magenta; y, yellow;"+
                                                                                     "k, black; w, white", default=[])
     parser.add_argument('-k', "--linestyle",  type=str,             nargs='+', help="linestyle: solid, dashed, dashdot, dotted or tuple; default: solid",
                                                                                     default=[])
     parser.add_argument('-w', "--linewidth",  type=str,             nargs='+', help="linewidth, default: 0.8", default=[])
-    parser.add_argument('-i', "--input",      type=str,             help="plot figure from .dat file, default: BAND.dat", default="BAND.dat")
+    parser.add_argument('-i', "--input",      type=str,             nargs='+', help="plot figure from .dat file, default: BAND.dat", default=["BAND.dat"])
     parser.add_argument('-o', "--output",     type=str,             help="plot figure filename, default: BAND.png", default="BAND.png")
     parser.add_argument('-q', "--dpi",        type=int,             help="dpi of the figure, default: 500", default=500)
     parser.add_argument('-j', "--klabels",    type=str,             help="filename of KLABELS, default: KLABELS", default="KLABELS")
     parser.add_argument('-l', "--labels",     type=str.upper,       nargs='+', default=[], help='labels for high-symmetry points, such as X S Y K M')
     parser.add_argument('-d', "--dos",        type=str,             nargs='+', default=[], help="plot DOS from .dat file, or file list")
     parser.add_argument('-x', "--horizontal", type=float, nargs=2,  help="Density of states, electrons/eV range")
     parser.add_argument('-n', "--exchange",   action='store_true',  help="exchange the x and y axes of DOS")
@@ -96,18 +96,19 @@
             else:
                 formula = formula + symbol[i]
 
     legend = args.legend or [formula] or [pltname]
 
     fig_p = cla_fig(output=args.output, size=args.size, vertical=args.vertical, horizontal=args.horizontal,
                     color=color, linestyle=linestyle, linewidth=linewidth, location=args.location, dpi=args.dpi)
-    if os.path.exists(args.input):
+    bandfile = [f for i in args.input for f in glob.glob(i)]
+    if len(bandfile) == 1:
         if not fig_p.vertical:
             fig_p.vertical = [-5.0, 5.0]
-        arr, bands, ispin = readdata.bands(args.input)
+        arr, bands, ispin = readdata.bands(bandfile[0])
         ticks   = []
         klabels = []
         if os.path.exists(args.klabels):
             ticks, klabels = readdata.klabels(args.klabels)
 
         if len(labels) == 0:
             labels=[re.sub('GAMMA|Gamma|G', 'Γ', re.sub('Undefined|Un|[0-9]', '', i)) for i in klabels]
@@ -140,32 +141,61 @@
             if ispin == "Noneispin":
                 plots.NoneispinWd(arr, bands, ticks, labels, darr, dele, args.fill, index_f, elements, width_ratios, legend, fig_p)
             elif ispin == "Ispin" and not args.divided:
                 plots.IspinWd(arr, bands, ticks, labels, darr, dele, args.fill, index_f, elements, width_ratios, legend, fig_p)
             elif ispin == "Ispin" and args.divided:
                 plots.DispinWd(arr, bands, ticks, labels, darr, dele, args.fill, index_f, elements, width_ratios, legend, fig_p)
 
-    else:
+    elif len(bandfile) == 0:
         if dosfiles:
             if fig_p.output == "BAND.png":
                 fig_p.output = "DOS.png"
             darr, dele, s_elements = readdata.dos(dosfiles)
             index_f, labels_elements = readdata.select(s_elements, args.partial)
             if not elements:
                 elements = labels_elements
 
             plots.pdosfiles(darr, dele, args.fill, index_f, elements, legend, args.exchange, fig_p)
         else:
             print('No .dat file!')
 
+    if len(bandfile) == 2:
+        if not fig_p.vertical:
+            fig_p.vertical = [-5.0, 5.0]
+        arr = [''] * 2
+        bands = [''] * 2
+        ispin = [''] * 2
+        arr[0], bands[0], ispin[0] = readdata.bands(bandfile[0])
+        arr[1], bands[1], ispin[1] = readdata.bands(bandfile[1])
+        ticks   = []
+        klabels = []
+        if os.path.exists(args.klabels):
+            ticks, klabels = readdata.klabels(args.klabels)
+
+        if len(labels) == 0:
+            labels=[re.sub('GAMMA|Gamma|G', 'Γ', re.sub('Undefined|Un|[0-9]', '', i)) for i in klabels]
+
+        if len(ticks) > len(labels):
+            labels = labels + [''] * (len(ticks) - len(labels))
+        elif len(ticks) < len(labels):
+            labels = labels[:len(ticks)]
+
+        if len(legend) < 3:
+            legend = legend + [''] * (3 - len(legend))
+
+        if all(x == "Noneispin" for x in ispin):
+            plots.Noneispin2(arr, bands, ticks, labels, legend, fig_p)
+        elif all(x == "Ispin" for x in ispin):
+            plots.Dispin2(arr, bands, ticks, labels, legend, fig_p)
+
 def pmain():
     parser = argparse.ArgumentParser(description='Plot the phonon band structure or DOS from phonopy results.',
                                      epilog='''
 Example:
-pbandplot -i band.dat -o pband.png -l g m k g -d projected_dos.dat -g "$\pi^2_4$" -e Si C O
+pbandplot -i BAND.dat -o BAND.png -l g m k g -d projected_dos.dat -g \$\\pi^2_4\$ -e Si C O
 ''',
                                      formatter_class=argparse.RawDescriptionHelpFormatter)
     parser.add_argument('-v', "--version",    action="version",     version="bandplot "+__version__+" from "+os.path.dirname(__file__)+' (python'+platform.python_version()+')')
     parser.add_argument('-s', "--size",       type=float, nargs=2,  help='figure size: width, height')
     parser.add_argument('-b', "--broken",     type=float, nargs=2,  help='broken axis: start, end')
     parser.add_argument('-r', "--hratios",    type=float,           help='height ratio for broken axis, default: 0.2', default=0.2)
     parser.add_argument('-y', "--vertical",   type=float, nargs=2,  help="frequency (THz) range")
```

## Comparing `bandplot-0.1.4.2.dist-info/METADATA` & `bandplot-0.1.4.3.dist-info/METADATA`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bandplot
-Version: 0.1.4.2
+Version: 0.1.4.3
 Summary: Band structure, DOS or phonon band structure plot from vaspkit or phonopy result.
 Home-page: https://github.com/lkccrr/bandplot
 Author: kan
 Author-email: luokan@hrbeu.edu.cn
 License: MIT
 Keywords: DFT VASP DOS band plot Phonon
 Platform: Unix
@@ -37,15 +37,16 @@
 The <b style="color:green;"><i>bandplot</b></i> is used for electron band structure, DOS or phonon band structure, DOS plotting from ***vaspkit*** or ***phonopy*** results. The code will provide two scripts, <b style="color:blue;"><i>bandplot</b></i> for band structure or DOS plotting from ***vaspkit*** <b style="color:darkred;"><i>\*.dat</b></i> files, and <b style="color:blue;"><i>pbandplot</b></i> for phonon band structure or DOS plotting from ***phonopy*** <b style="color:darkred;"><i>\*.dat</b></i> files.
 ***
 <b style="color:blue;"><i>bandplot</b></i>
 * To execute <b style="color:blue;"><i>bandplot</b></i> <b style="color:red;"><i>\-h</b></i> for the parameters to use.
 * Example:
 ```bash
 bandplot -h
-bandplot -i band.dat -o band.png -l g m k g -d PDOS* -z
+bandplot -i BAND.dat -o band.png -l g m k g -d PDOS* -z
+bandplot -i BAND1.dat BAND2.dat -g TiO\$_2\$ PBE HSE
 bandplot -b -l g m k g -y -3 3
 ```
 ***
 <b style="color:blue;"><i>pbandplot</b></i>
 * To execute <b style="color:blue;"><i>pbandplot</b></i> <b style="color:red;"><i>\-h</b></i> for the parameters to use.
 * Example:
 ```bash
```

