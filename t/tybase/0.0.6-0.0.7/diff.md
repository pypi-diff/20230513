# Comparing `tmp/tybase-0.0.6.tar.gz` & `tmp/tybase-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tybase-0.0.6.tar", last modified: Mon May  8 10:39:26 2023, max compression
+gzip compressed data, was "tybase-0.0.7.tar", last modified: Sat May 13 04:52:31 2023, max compression
```

## Comparing `tybase-0.0.6.tar` & `tybase-0.0.7.tar`

### file list

```diff
@@ -1,22 +1,26 @@
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-08 10:39:26.002058 tybase-0.0.6/
--rw-rw-rw-   0 zhangte    (501) staff       (20)       28 2023-05-04 00:02:42.000000 tybase-0.0.6/MANIFEST.in
--rw-r--r--   0 zhangte    (501) staff       (20)      609 2023-05-08 10:39:26.001777 tybase-0.0.6/PKG-INFO
--rw-rw-rw-   0 zhangte    (501) staff       (20)      156 2023-05-08 08:46:36.000000 tybase-0.0.6/README.md
--rw-r--r--   0 zhangte    (501) staff       (20)       38 2023-05-08 10:39:26.002177 tybase-0.0.6/setup.cfg
--rw-rw-rw-   0 zhangte    (501) staff       (20)      778 2023-05-08 10:38:38.000000 tybase-0.0.6/setup.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-08 10:39:25.948550 tybase-0.0.6/tybase/
--rw-rw-rw-   0 zhangte    (501) staff       (20)        0 2023-05-03 23:43:39.000000 tybase-0.0.6/tybase/__init__.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-08 10:39:25.952005 tybase-0.0.6/tybase/baidu/
--rw-rw-rw-   0 zhangte    (501) staff       (20)        0 2023-05-04 01:26:22.000000 tybase-0.0.6/tybase/baidu/__init__.py
--rw-rw-rw-   0 zhangte    (501) staff       (20)     4126 2023-05-05 10:37:20.000000 tybase-0.0.6/tybase/baidu/kw_tool.py
--rw-rw-rw-   0 zhangte    (501) staff       (20)        6 2023-05-03 23:45:43.000000 tybase-0.0.6/tybase/datatest.txt
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-08 10:39:25.968680 tybase-0.0.6/tybase/lc/
--rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-08 08:41:12.000000 tybase-0.0.6/tybase/lc/__init__.py
--rw-r--r--   0 zhangte    (501) staff       (20)     2995 2023-05-08 10:37:41.000000 tybase-0.0.6/tybase/lc/eg1.py
--rw-rw-rw-   0 zhangte    (501) staff       (20)      205 2023-05-03 23:46:43.000000 tybase-0.0.6/tybase/tytest.py
-drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-08 10:39:25.951270 tybase-0.0.6/tybase.egg-info/
--rw-rw-rw-   0 zhangte    (501) staff       (20)      609 2023-05-08 10:39:25.000000 tybase-0.0.6/tybase.egg-info/PKG-INFO
--rw-rw-rw-   0 zhangte    (501) staff       (20)      323 2023-05-08 10:39:25.000000 tybase-0.0.6/tybase.egg-info/SOURCES.txt
--rw-rw-rw-   0 zhangte    (501) staff       (20)        1 2023-05-08 10:39:25.000000 tybase-0.0.6/tybase.egg-info/dependency_links.txt
--rw-rw-rw-   0 zhangte    (501) staff       (20)       20 2023-05-08 10:39:25.000000 tybase-0.0.6/tybase.egg-info/requires.txt
--rw-rw-rw-   0 zhangte    (501) staff       (20)        7 2023-05-08 10:39:25.000000 tybase-0.0.6/tybase.egg-info/top_level.txt
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.028733 tybase-0.0.7/
+-rw-r--r--   0 zhangte    (501) staff       (20)       28 2023-05-04 00:02:42.000000 tybase-0.0.7/MANIFEST.in
+-rw-r--r--   0 zhangte    (501) staff       (20)      611 2023-05-13 04:52:31.028486 tybase-0.0.7/PKG-INFO
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      156 2023-05-08 08:46:36.000000 tybase-0.0.7/README.md
+-rw-r--r--   0 zhangte    (501) staff       (20)       38 2023-05-13 04:52:31.028851 tybase-0.0.7/setup.cfg
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      947 2023-05-13 04:52:18.000000 tybase-0.0.7/setup.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.021388 tybase-0.0.7/tybase/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-03 23:43:39.000000 tybase-0.0.7/tybase/__init__.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.024586 tybase-0.0.7/tybase/baidu/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-04 01:26:22.000000 tybase-0.0.7/tybase/baidu/__init__.py
+-rw-rw-rw-   0 zhangte    (501) staff       (20)     4364 2023-05-09 03:46:53.000000 tybase-0.0.7/tybase/baidu/kw_tool.py
+-rw-r--r--   0 zhangte    (501) staff       (20)        6 2023-05-03 23:45:43.000000 tybase-0.0.7/tybase/datatest.txt
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.026893 tybase-0.0.7/tybase/dbtool/
+-rw-r--r--   0 zhangte    (501) staff       (20)        0 2023-05-13 02:41:28.000000 tybase-0.0.7/tybase/dbtool/__init__.py
+-rw-r--r--   0 zhangte    (501) staff       (20)     4364 2023-05-13 04:50:10.000000 tybase-0.0.7/tybase/dbtool/data_import.py
+-rw-r--r--   0 zhangte    (501) staff       (20)     2206 2023-05-13 03:56:34.000000 tybase-0.0.7/tybase/dbtool/mysql.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.027805 tybase-0.0.7/tybase/lc/
+-rw-rw-rw-   0 zhangte    (501) staff       (20)        0 2023-05-08 08:41:12.000000 tybase-0.0.7/tybase/lc/__init__.py
+-rw-rw-rw-   0 zhangte    (501) staff       (20)     2995 2023-05-08 10:37:41.000000 tybase-0.0.7/tybase/lc/eg1.py
+-rw-r--r--   0 zhangte    (501) staff       (20)      205 2023-05-03 23:46:43.000000 tybase-0.0.7/tybase/tytest.py
+drwxr-xr-x   0 zhangte    (501) staff       (20)        0 2023-05-13 04:52:31.023942 tybase-0.0.7/tybase.egg-info/
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      611 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/PKG-INFO
+-rw-rw-rw-   0 zhangte    (501) staff       (20)      401 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/SOURCES.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)        1 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/dependency_links.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)       86 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/requires.txt
+-rw-r--r--   0 zhangte    (501) staff       (20)        7 2023-05-13 04:52:30.000000 tybase-0.0.7/tybase.egg-info/top_level.txt
```

### Comparing `tybase-0.0.6/tybase/baidu/kw_tool.py` & `tybase-0.0.7/tybase/baidu/kw_tool.py`

 * *Files 7% similar despite different names*

```diff
@@ -24,24 +24,26 @@
     def summarize(self, target_column, summary_columns):
         """
         :param target_column: 目标名,比如搜索词汇总一般就是"搜索词"
         :param summary_columns: 需要汇总的列名
         :return: 汇总后的DataFrame
 
         # 使用示例
+        from tybase.baidu.kw_tool import KeywordSummary
         custom_words = ["手机版","写作猫","国内版","中国版","生成器","创作猫"]   #定义不分词列表
         filter_words = [" ","的"]  # 定义过滤词
         ks = KeywordSummary(df, custom_words, filter_words)
         # 传入需要计算的字段
         summary_df = ks.summarize("搜索词", ["展现", "点击", "消费", "激活数", "注册数", "付费金额"])
         # 返回
+        ```txt
         关键词	频次	展现	点击	消费	激活数	注册数	付费金额
     0	手机版	223.0	40223.0	8912.0	11858.01	2867.0	2385.0	12712.0
     1	下载	1362.0	88378.0	20140.0	24303.06	6330.0	5162.0	25668.0
-
+        ```
         """
         self.df["分词"] = self.df[target_column].apply(self._split_keywords)
 
         summary_data = defaultdict(lambda: defaultdict(float))
 
         for _, row in self.df.iterrows():
             for word in row["分词"]:
@@ -53,26 +55,28 @@
         summary_df.reset_index(level=0, inplace=True)
         summary_df.rename(columns={'index': '关键词'}, inplace=True)
 
         return summary_df
 
 
 class KeywordAggregator:
+    """对竞价的关键词,根据条件过滤包含的关键词,分组汇总好对应的数据"""
     def __init__(self, dataframe):
         self.df = dataframe
 
     def aggregate(self, keyword_dict, summary_columns, roi_formula=None) -> pd.DataFrame:
         """
 
         :param keyword_dict: 关键词分组字典,比如 {"chatgpt": "chat|gpt", "作文": "作文"}
         :param summary_columns: 需要汇总的列名,比如 ["展现", "点击", "消费", "激活数", "注册数", "付费金额"]
         :param roi_formula: ROI计算公式,比如 "付费金额 / 消费"
         :return: 汇总后的DataFrame
 
         # 使用示例
+        from tybase.baidu.kw_tool import KeywordSummary
         # 创建 KeywordAggregator 实例
         ka = KeywordAggregator(df)
 
 
         # 传入分类规则,以及ROI的计算公式
 
         keyword_dict = {"chatgpt": "chat|gpt",
```

### Comparing `tybase-0.0.6/tybase/lc/eg1.py` & `tybase-0.0.7/tybase/lc/eg1.py`

 * *Files identical despite different names*

