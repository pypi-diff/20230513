# Comparing `tmp/lineagex-0.0.1.tar.gz` & `tmp/lineagex-0.0.1a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lineagex-0.0.1.tar", max compression
+gzip compressed data, was "lineagex-0.0.1a1.tar", max compression
```

## Comparing `lineagex-0.0.1.tar` & `lineagex-0.0.1a1.tar`

### file list

```diff
@@ -1,13 +1,14 @@
--rw-r--r--   0        0        0    33791 2023-05-12 01:39:20.444678 lineagex-0.0.1/lineagex/ColumnLineage.py
--rw-r--r--   0        0        0    16904 2023-05-12 01:39:20.444678 lineagex-0.0.1/lineagex/ColumnLineageNoConn.py
--rw-r--r--   0        0        0     2319 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/LineageXNoConn.py
--rw-r--r--   0        0        0     9925 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/LineageXWithConn.py
--rw-r--r--   0        0        0     6422 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/SqlToDict.py
--rw-r--r--   0        0        0       61 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/__init__.py
--rw-r--r--   0        0        0    54175 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/app.js
--rw-r--r--   0        0        0      159 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/main.py
--rw-r--r--   0        0        0     1404 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/stack.py
--rw-r--r--   0        0        0     6568 2023-05-12 01:39:20.448011 lineagex-0.0.1/lineagex/utils.py
--rw-r--r--   0        0        0  3761177 2023-05-12 01:39:20.471345 lineagex-0.0.1/lineagex/vendor.js
--rw-r--r--   0        0        0      370 2023-05-12 01:54:16.550848 lineagex-0.0.1/pyproject.toml
--rw-r--r--   0        0        0      656 1970-01-01 00:00:00.000000 lineagex-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0       55 2023-05-12 01:58:21.769698 lineagex-0.0.1a1/lineagex/__init__.py
+-rw-r--r--   0        0        0    54175 2023-04-22 19:33:20.371862 lineagex-0.0.1a1/lineagex/app.js
+-rw-r--r--   0        0        0    34528 2023-05-12 01:56:56.456690 lineagex-0.0.1a1/lineagex/ColumnLineage.py
+-rw-r--r--   0        0        0    17230 2023-05-11 22:25:23.093987 lineagex-0.0.1a1/lineagex/ColumnLineageNoConn.py
+-rw-r--r--   0        0        0      974 2023-05-12 22:15:42.232574 lineagex-0.0.1a1/lineagex/lineagex.py
+-rw-r--r--   0        0        0     2355 2023-05-12 02:16:08.034372 lineagex-0.0.1a1/lineagex/LineageXNoConn.py
+-rw-r--r--   0        0        0     9896 2023-05-12 22:15:49.236456 lineagex-0.0.1a1/lineagex/LineageXWithConn.py
+-rw-r--r--   0        0        0     6556 2023-05-12 02:16:38.442999 lineagex-0.0.1a1/lineagex/SqlToDict.py
+-rw-r--r--   0        0        0     1460 2023-05-08 20:36:59.378380 lineagex-0.0.1a1/lineagex/stack.py
+-rw-r--r--   0        0        0     6760 2023-05-11 19:49:20.736279 lineagex-0.0.1a1/lineagex/utils.py
+-rw-r--r--   0        0        0  3761177 2023-04-22 19:33:20.645016 lineagex-0.0.1a1/lineagex/vendor.js
+-rw-r--r--   0        0        0      449 2023-05-12 23:00:08.932473 lineagex-0.0.1a1/pyproject.toml
+-rw-r--r--   0        0        0     3492 2023-05-12 22:58:42.152661 lineagex-0.0.1a1/README.md
+-rw-r--r--   0        0        0     4192 1970-01-01 00:00:00.000000 lineagex-0.0.1a1/PKG-INFO
```

### Comparing `lineagex-0.0.1/lineagex/ColumnLineage.py` & `lineagex-0.0.1a1/lineagex/ColumnLineage.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,745 +1,745 @@
-import re
-from sqlglot import parse_one, exp
-from sqlglot.expressions import CTE
-from sqlglot import expressions
-from psycopg2.extensions import connection
-from typing import List, Tuple, Optional
-
-from lineagex.utils import find_column
-
-
-class ColumnLineage:
-    def __init__(
-        self,
-        plan: Optional[dict] = None,
-        sql: Optional[str] = "",
-        table_name: Optional[str] = "",
-        conn: connection = None,
-        part_tables: Optional[str] = None,
-        search_schema: Optional[str] = "",
-    ) -> None:
-        self.split_regex = re.compile(r"[^a-zA-Z0-9._]")
-        self.all_used_col = []
-        self.possible_columns = []
-        self.table_alias = {}
-        self.table_alias_reversed = {}
-        self.cte_name = ""
-        self.agg_flag = False
-        self.cte_dict = {}
-        self.subplan_dict = {}
-        self.function_call_cols = {}
-        self.part_tables = part_tables
-        self.column_prefix_dict = {}
-        self.conn = conn
-        self.search_schema = search_schema
-        self.sql_ast = parse_one(sql=sql, read="postgres")
-        self.cte_column = self._find_cte_col()
-        self.final_output = ""
-        self.final_node_type = ""
-        self.subquery_final_output = ""
-        self.column_dict = {}
-        self.table_list = []
-        self._traverse_plan(plan=plan)
-        self._resolve_column_dict(cols=self._find_final_column())
-        self.table_list = sorted(set(self.table_list))
-        # print(self.final_output)
-        # print(self.subplan_dict)
-        # print(self.table_alias)
-        # print(self.cte_dict)
-        # print(self.all_used_col)
-        # print(self.possible_columns)
-        # print("columns: ", self.column_dict)
-        # print("table: ", self.table_list)
-
-    def _find_final_column(self) -> List[str]:
-        """
-        Find all the column names in the final projection
-        :return: the list of column names in the final projection
-        """
-        # Pop all CTE and Subquery trees
-        for with_sql in self.sql_ast.find_all(exp.With):
-            with_sql.pop()
-        for sub_sql in self.sql_ast.find_all(exp.Subquery):
-            sub_sql.pop()
-        final_column_list = []
-        for projection in self.sql_ast.find(exp.Select).expressions:
-            col_name = projection.alias_or_name
-            # Resolve aggregations with no alias
-            if isinstance(projection, exp.Count):
-                col_name = "count"
-            elif isinstance(projection, exp.Avg):
-                col_name = "avg"
-            elif isinstance(projection, exp.Max):
-                col_name = "max"
-            elif isinstance(projection, exp.Min):
-                col_name = "min"
-            # Resolve * and check if it is from a previous CTE or check database for the table
-            elif (
-                isinstance(projection, exp.Column) and projection.find(exp.Star)
-            ) or col_name == "*":
-                main_table_list = []
-                for table in self.sql_ast.find_all(exp.Table):
-                    table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
-                    main_table_list.append(table_def_split[0])
-                # if the * has a prefix
-                if projection.find(exp.Identifier):
-                    t_name = projection.find(exp.Identifier).text("this")
-                    if table_alias_dict[t_name] in self.cte_column.keys():
-                        col_name = self.cte_column[table_alias_dict[t_name]]
-                    else:
-                        col_name = find_column(
-                            table_name=table_alias_dict[t_name],
-                            engine=self.conn,
-                            search_schema=self.search_schema,
-                        )
-                # if * has no prefix
-                else:
-                    for t_name in main_table_list:
-                        if t_name in self.cte_column.keys():
-                            final_column_list.extend(self.cte_column[t_name])
-                        else:
-                            final_column_list.extend(
-                                find_column(
-                                    table_name=t_name,
-                                    engine=self.conn,
-                                    search_schema=self.search_schema,
-                                )
-                            )
-            if isinstance(col_name, list):
-                final_column_list.extend(col_name)
-            else:
-                if col_name != "*":
-                    final_column_list.append(col_name)
-        return final_column_list
-
-    def _resolve_column_dict(self, cols: Optional[List] = None) -> None:
-        """
-        Insert into column_dict using the column names as keys and its dependencies as child
-        :param cols: the columns for the final output
-        :return: None
-        """
-        if len(self.final_output) > len(cols):
-            self.final_output = self.final_output[: len(cols)]
-        elif len(self.final_output) < len(cols):
-            print(
-                "number of columns from the sql does not match the number in manifest"
-            )
-            return
-        for idx, val in enumerate(self.final_output):
-            # Postgres Aggregate function of count(*) that involves all the columns
-            if self.final_node_type == "Aggregate" and val.strip() == "count(*)":
-                all_cols = self.possible_columns
-            else:
-                table_col = re.split(self.split_regex, val.strip())
-                all_cols = list(
-                    set(set(table_col) & set(self.possible_columns)).union(
-                        self.all_used_col
-                    )
-                )
-            # Subquery in the final projection
-            if val.find("SubPlan ") != -1:
-                subplan_name = re.findall(re.compile(r"SubPlan [0-9]*"), val)[0]
-                all_cols.extend(self.subplan_dict[subplan_name])
-            self.column_dict[cols[idx]] = sorted(
-                self._remove_table_alias(cols=all_cols)
-            )
-
-    def _traverse_plan(self, plan: Optional[dict] = None) -> None:
-        """
-        Traversing the plan using recursion and go into Plans if it is present
-        :param plan: the given execution plan
-        :return: None
-        """
-        if plan["Node Type"] in [
-            "Seq Scan",
-            "Parallel Seq Scan",
-            "Bitmap Heap Scan",
-            "Index Scan",
-            "Index Only Scan",
-        ]:
-            self.table_alias[plan["Alias"]] = self._find_parent_table(
-                table=plan["Schema"] + "." + plan["Relation Name"]
-            )
-            self.table_alias_reversed[
-                plan["Schema"] + "." + plan["Relation Name"]
-            ] = plan["Alias"]
-        if "Plans" in plan.keys():
-            for subplan_data in plan["Plans"]:
-                self._traverse_plan(plan=subplan_data)
-        temp = plan.get("Output")
-        if temp is not None:
-            self.final_output = temp
-            self.final_node_type = plan.get("Node Type")
-        # if scan from tables/views, add to possible columns
-        if plan["Node Type"] in [
-            "Seq Scan",
-            "Parallel Seq Scan",
-            "Bitmap Heap Scan",
-            "Index Scan",
-            "Index Only Scan",
-        ]:
-            # Scan and Filter and CTE in one
-            if "Subplan Name" in plan.keys():
-                self._add_possible_columns(plan)
-                # self.possible_columns.extend(plan["Output"])
-                if "Alias" in plan.keys():
-                    alias = plan["Alias"]
-                else:
-                    alias = plan["Schema"] + "." + plan["Relation Name"]
-                temp_regex = re.compile(r"({}\.[a-zA-Z0-9_]+)".format(alias))
-                # print(plan['Subplan Name'], plan['Output'])
-                for i in plan["Output"]:
-                    self.possible_columns.extend(re.findall(temp_regex, i))
-                if "Filter" in plan.keys():
-                    self.possible_columns.extend(re.findall(temp_regex, plan["Filter"]))
-                cte_name = plan["Subplan Name"].split(" ")[1]
-                self.table_list.append(
-                    self._find_parent_table(
-                        table=(plan["Schema"] + "." + plan["Relation Name"])
-                    )
-                )
-                self.table_alias[cte_name] = cte_name
-                self._add_cte_dict(plan=plan)
-            # Filter and scan in one plan
-            elif "Filter" in plan.keys():
-                self._add_possible_columns(plan)
-                # self.possible_columns.extend(plan["Output"])
-                self._handle_filter_in_scan(plan=plan)
-                # in the filter, there is chance there is also index cond
-                self._handle_index_cond(plan=plan)
-            # Scan only
-            else:
-                # to avoid index cond
-                self._add_possible_columns(plan=plan)
-                self._handle_index_cond(plan=plan)
-        # if scan from cte
-        elif plan["Node Type"] == "CTE Scan":
-            # add to possible column first and add all columns from CTE to prevent filters on top of any
-            if "Alias" in plan.keys():
-                all_cte_cols = [
-                    plan["Alias"] + "." + s
-                    for s in list(self.cte_dict[plan["CTE Name"]].keys())
-                ]
-            else:
-                all_cte_cols = [
-                    plan["CTE Name"] + "." + s
-                    for s in list(self.cte_dict[plan["CTE Name"]].keys())
-                ]
-            self.possible_columns.extend(
-                list(set(all_cte_cols).union(set(plan["Output"])))
-            )
-            # handle filter and scan in the same plan
-            if "Filter" in plan.keys():
-                self._handle_filter_in_scan(plan=plan)
-            # the current scan can also be the creation of another cte
-            if "Subplan Name" in plan.keys():
-                if "CTE Name" in plan.keys():
-                    self.possible_columns.extend(
-                        [
-                            plan["CTE Name"] + "." + s
-                            for s in list(self.cte_dict[plan["CTE Name"]].keys())
-                        ]
-                    )
-                self.table_alias[plan["Alias"]] = plan["CTE Name"]
-                self._add_cte_dict(plan=plan)
-            else:
-                # if just a scan, add to alias
-                self.table_alias[plan["Alias"]] = plan["CTE Name"]
-        # if scan from a subquery
-        elif plan["Node Type"] == "Subquery Scan":
-            org_all_used_cols = self.all_used_col
-            org_possible_cols = self.possible_columns
-            self.all_used_col = []
-            self.possible_columns = []
-            if "Plans" in plan.keys():
-                self.subquery_final_output = plan["Plans"][0]["Output"]
-            else:
-                self.subquery_final_output = plan["Output"]
-            self._resolve_subquery(plan=plan)
-            if "Alias" in plan.keys():
-                self.cte_name = plan["Alias"]
-            temp_dict = {}
-            self._extract_from_cond(plan=plan)
-            if self.cte_name in self.cte_column.keys():
-                for idx, val in enumerate(self.cte_column[self.cte_name]):
-                    cte_col = re.split(
-                        self.split_regex, self.subquery_final_output[idx].strip()
-                    )
-                    all_cols = list(
-                        set(set(cte_col) & set(self.possible_columns)).union(
-                            self.all_used_col
-                        )
-                    )
-                    # Subquery in the final projection
-                    if self.subquery_final_output[idx].find("SubPlan ") != -1:
-                        subplan_name = re.findall(
-                            re.compile(r"SubPlan [0-9]*"),
-                            self.subquery_final_output[idx],
-                        )[0]
-                        all_cols.extend(self.subplan_dict[subplan_name])
-                    temp_dict[val] = self._remove_table_alias(cols=all_cols)
-                self.cte_dict[self.cte_name] = temp_dict
-            self.table_alias[plan["Alias"]] = plan["Alias"]
-            self.all_used_col = org_all_used_cols
-            self.possible_columns = org_possible_cols
-            self.possible_columns.extend(plan["Output"])
-        else:
-            # creation of cte but with an Append node(usually UNION/EXCEPT/INTERSECT)
-            if "Subplan Name" in plan.keys():
-                # Resolve UNION/EXCEPT/INTERSECT since the Node Type will be Appended with no outputs
-                if (
-                    plan["Node Type"] in ["Append", "MergeAppend"]
-                    and "Output" not in plan.keys()
-                    and len(plan["Plans"]) != 0
-                ):
-                    s = plan.get("Subplan Name").split(" ")
-                    if s[0] == "CTE":
-                        self.cte_name = s[1]
-                        temp_dict = {}
-                        self._extract_from_cond(plan=plan)
-                        self._resolve_union(plan=plan)
-                        self.agg_flag = False
-                        for val in self.cte_column[self.cte_name]:
-                            temp_dict[val] = self._remove_table_alias(
-                                cols=self.all_used_col
-                            )
-                        self.cte_dict[self.cte_name] = temp_dict
-                        self.all_used_col = []
-                        self.possible_columns = []
-                else:
-                    # if only creation of a cte, but no scan, just add it to cte_dict
-                    self._add_cte_dict(plan=plan)
-            # UNION/EXCEPT/INTERSECT at the last step with no creation of CTE
-            elif (
-                plan["Node Type"] in ["Append", "MergeAppend"]
-                and "Output" not in plan.keys()
-                and len(plan["Plans"]) != 0
-            ):
-                self._extract_from_cond(plan=plan)
-                self._resolve_union(plan=plan)
-                self.agg_flag = False
-            # every other node aside from cte creations/scans
-            else:
-                self._extract_from_cond(plan=plan)
-
-    def _handle_index_cond(self, plan: Optional[dict] = None) -> None:
-        """
-        When there's an index_cond in the plan, handle it and extract the necessary columns
-        :param plan: the plan with the index_cond
-        """
-        temp = plan.get("Index Cond")
-        if temp is not None:
-            idx_name = plan.get("Index Name")
-            if idx_name is not None:
-                cur = self.conn.cursor()
-                cur.execute("""SET search_path TO {};""".format(self.search_schema))
-                cur.execute(
-                    "SELECT schemaname, tablename, indexname, indexdef FROM pg_indexes WHERE indexname = '{}'".format(
-                        idx_name
-                    )
-                )
-                result = cur.fetchall()[0]
-                cur.close()
-                # the indexdef is at index 3
-                indexdef = result[3]
-                btree_idx = indexdef.find("USING btree")
-                if btree_idx != -1:
-                    close_bracket = indexdef.find(")", btree_idx)
-                    if close_bracket != -1:
-                        idx_cols = indexdef[btree_idx + 13 : close_bracket].split(",")
-                        alias = self.table_alias_reversed[result[0] + "." + result[1]]
-                        for i in idx_cols:
-                            self.possible_columns.append(alias + "." + i)
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-
-    def _handle_filter_in_scan(self, plan: Optional[dict] = None) -> None:
-        """
-        When there is filter in the scan node, handle it and find necessary columns
-        :param plan: the plan with the filter in the scan node
-        """
-        if "Alias" in plan.keys():
-            alias = plan["Alias"]
-        else:
-            alias = plan["Schema"] + "." + plan["Relation Name"]
-        temp_regex = re.compile(r"({}\.[a-zA-Z0-9_]+)".format(alias))
-        self.possible_columns.extend(re.findall(temp_regex, plan["Filter"]))
-        temp = plan.get("Filter")
-        row_col = re.split(self.split_regex, temp.strip())
-        self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        if temp.find("SubPlan ") != -1:
-            subplan_name = re.findall(re.compile(r"SubPlan [0-9]*"), temp)[0]
-            self.all_used_col.extend(self.subplan_dict[subplan_name])
-
-    def _resolve_subquery(self, plan: Optional[dict] = None) -> None:
-        """
-        When there is a node with subquery, go in recursively and find the most inner node
-        :param plan: the node with subquery
-        """
-        if "Plans" in plan.keys():
-            for subplan_data in plan["Plans"]:
-                self._resolve_subquery(plan=subplan_data)
-        if "Output" in plan.keys() and plan["Node Type"] in [
-            "Seq Scan",
-            "Parallel Seq Scan",
-            "Bitmap Heap Scan",
-            "Index Scan",
-            "Index Only Scan",
-            "CTE Scan",
-        ]:
-            self.possible_columns.extend(plan["Output"])
-            self._extract_from_cond(plan=plan)
-        else:
-            self._extract_from_cond(plan=plan)
-
-    def _resolve_union(self, plan: Optional[dict] = None) -> None:
-        """
-        To resolve the UNION, all the columns involved are used since those columns need to be the same
-        :param plan: the execution plan for UNION/EXCEPT/INTERSECT
-        """
-        if "Plans" in plan.keys():
-            # Check if it is an aggregation, since it would scan all the columns
-            if plan["Plans"][0]["Node Type"] == "Aggregate":
-                self.agg_flag = True
-            for subplan_data in plan["Plans"]:
-                self._resolve_union(plan=subplan_data)
-        if (
-            "Output" in plan.keys()
-            and plan["Node Type"]
-            in [
-                "Seq Scan",
-                "Parallel Seq Scan",
-                "Bitmap Heap Scan",
-                "Index Scan",
-                "Index Only Scan",
-            ]
-            and not self.agg_flag
-        ):
-            # check if it is using Append node for partitioned tables
-            if plan["Schema"] + "." + plan["Relation Name"] in list(
-                self.part_tables.keys()
-            ):
-                self.possible_columns.extend(plan["Output"])
-                self._extract_from_cond(plan=plan)
-            else:
-                # if it is using Append node for UNION/EXCEPT/INTERSECT
-                for col in plan["Output"]:
-                    row_col = re.split(self.split_regex, col.strip())
-                    self.all_used_col.extend(
-                        list(set(row_col) & set(self.possible_columns))
-                    )
-        elif (
-            "Output" in plan.keys()
-            and plan["Node Type"] == "CTE Scan"
-            and not self.agg_flag
-        ):
-            # if it is using Append node for UNION/EXCEPT/INTERSECT
-            for col in plan["Output"]:
-                row_col = re.split(self.split_regex, col.strip())
-                self.all_used_col.extend(
-                    list(set(row_col) & set(self.possible_columns))
-                )
-
-    def _add_cte_dict(self, plan: Optional[dict] = None) -> None:
-        """
-        Add to the cte dict given the CTE plan and analyze its column lineage
-        :param plan: the CTE plan
-        :return:
-        """
-        s = plan.get("Subplan Name").split(" ")
-        if s[0] == "CTE":
-            self.cte_name = s[1]
-            temp_dict = {}
-            self._extract_from_cond(plan=plan)
-            for idx, val in enumerate(self.cte_column[self.cte_name]):
-                cte_col = re.split(self.split_regex, plan["Output"][idx].strip())
-                all_cols = list(
-                    set(set(cte_col) & set(self.possible_columns)).union(
-                        self.all_used_col
-                    )
-                )
-                # Subquery in the final projection
-                if plan["Output"][idx].find("SubPlan ") != -1:
-                    subplan_name = re.findall(
-                        re.compile(r"SubPlan [0-9]*"), plan["Output"][idx]
-                    )[0]
-                    all_cols.extend(self.subplan_dict[subplan_name])
-                temp_dict[val] = self._remove_table_alias(cols=all_cols)
-            self.cte_dict[self.cte_name] = temp_dict
-            self.all_used_col = []
-            self.possible_columns = []
-        # temporary subplan name
-        elif s[0] == "SubPlan":
-            subplan_list = []
-            for _, val in enumerate(plan["Output"]):
-                table_col = re.split(self.split_regex, val.strip())
-                all_cols = list(set(set(table_col) & set(self.possible_columns)))
-                subplan_list.extend(self._remove_table_alias(cols=all_cols))
-            self.subplan_dict[plan["Subplan Name"]] = subplan_list
-
-    def _extract_from_cond(self, plan: Optional[dict] = None) -> None:
-        """
-        Extract column from multiple operators, some add to possible_cols and some add to all_used_cols
-        :param plan: the execution plan for the operator
-        :return:
-        """
-        # More conditions
-        if plan["Node Type"] == "WindowAgg":
-            self.possible_columns.extend(plan["Output"])
-        # Handle index cond
-        self._handle_index_cond(plan=plan)
-        temp = plan.get("Hash Cond")
-        if temp is not None:
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        temp = plan.get("Merge Cond")
-        if temp is not None:
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        temp = plan.get("Recheck Cond")
-        if temp is not None:
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        temp = plan.get("Join Filter")
-        if temp is not None:
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        temp = plan.get("Filter")
-        if temp is not None:
-            row_col = re.split(self.split_regex, temp.strip())
-            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
-        temp = plan.get("Sort Key")
-        if temp is not None:
-            self.all_used_col.extend(list(set(temp) & set(self.possible_columns)))
-        temp = plan.get("Group Key")
-        if temp is not None:
-            self.all_used_col.extend(list(set(temp) & set(self.possible_columns)))
-        # Function calls
-        if plan["Node Type"] == "Function Scan":
-            if "Function Name" in plan.keys():
-                if plan["Function Name"] == "unnest":
-                    func_cols = re.split(
-                        self.split_regex, plan["Function Call"].strip()
-                    )
-                    all_cols = list(
-                        set(set(func_cols) & set(self.possible_columns)).union(
-                            self.all_used_col
-                        )
-                    )
-                    self.function_call_cols[plan["Output"][0]] = sorted(
-                        self._remove_table_alias(cols=all_cols)
-                    )
-                    self.possible_columns.append(plan["Output"][0])
-
-    def _add_possible_columns(self, plan: Optional[dict] = None) -> None:
-        """
-        Extract the columns/tables from the plan and add to possible columns and used tables, mainly used for base table
-        :param plan: plan to extract columns and tables
-        :return:
-        """
-        invalid_list = []
-        for i in plan["Output"]:
-            if len(i.split(".")) == 1:
-                self.column_prefix_dict[i] = (
-                    plan["Schema"] + "." + plan["Relation Name"] + "." + i
-                )
-        for i in plan["Output"]:
-            # if a column name contains an invalid char(that is not a-zA-z0-9_)
-            if re.search(r"[^\w.]", i):
-                invalid_list.append(i)
-                continue
-            # if a column name starts with a digit, likely is just a number, but not a column
-            elif i[0].isdigit():
-                continue
-            # no table prefix column outputs, append only the column name and the prefix + column
-            elif len(i.split(".")) == 1:
-                if "Alias" in plan.keys():
-                    prefix = plan["Alias"]
-                else:
-                    prefix = plan["Schema"] + "." + plan["Relation Name"]
-                self.possible_columns.append(prefix + "." + i)
-                self.possible_columns.append(i)
-            else:
-                self.possible_columns.append(i)
-        # if an output has invalid char, its likely it's an expression, have to extract the columns
-        if invalid_list:
-            all_table_cols = find_column(
-                table_name=plan["Schema"] + "." + plan["Relation Name"],
-                engine=self.conn,
-                search_schema=self.search_schema,
-            )
-            for i in invalid_list:
-                # split the output and match columns from all the columns of the table
-                table_col = re.split(self.split_regex, i.strip())
-                resolved_possible_cols = list(set(set(table_col) & set(all_table_cols)))
-                for j in resolved_possible_cols:
-                    self.possible_columns.append(j)
-                    if len(j.split(".")) == 1:
-                        self.column_prefix_dict[j] = (
-                            plan["Schema"] + "." + plan["Relation Name"] + "." + j
-                        )
-        self.table_list.append(
-            self._find_parent_table(table=plan["Schema"] + "." + plan["Relation Name"])
-        )
-        self.table_alias[plan["Alias"]] = self._find_parent_table(
-            table=plan["Schema"] + "." + plan["Relation Name"]
-        )
-        self.table_alias_reversed[plan["Schema"] + "." + plan["Relation Name"]] = plan[
-            "Alias"
-        ]
-
-    def _find_parent_table(self, table: Optional[str] = "") -> str:
-        """
-        Find the parent table from a given table name
-        :param table: table name
-        :return: table: the parent table name(if it is not partitioned table, it is just the input
-        """
-        if self.part_tables is not None:
-            if table in self.part_tables.keys():
-                table = self.part_tables[table]
-        return table
-
-    def _remove_table_alias(self, cols: Optional[List] = None) -> List:
-        """
-        Remove the alias in the name or add intended schema.table to column names
-        :param cols: the list of columns that has aliases that need to be resolved
-        :return: resolved aliases for the columns
-        """
-        current_cte_table = ""
-        ret_cols = []
-        temp_keys_dict = {}
-        for i in cols:
-            temp = i.split(".")
-            # has prefix or no
-            if len(temp) > 1:
-                # prefix yes, is the prefix already in alias or base table name
-                if temp[0] in self.table_alias.keys():
-                    org_name = self.table_alias[temp[0]]
-                    # prefix yes, get the non-alias cte name
-                    if org_name in self.cte_dict.keys():
-                        # to avoid case difference, create a temp dict for lower->original
-                        # if the current cte's temp dict is already created, skip it
-                        if org_name != current_cte_table:
-                            cte_dict_keys = list(self.cte_dict[org_name].keys())
-                            temp_keys_dict = {}
-                            for k in cte_dict_keys:
-                                temp_keys_dict[k.lower()] = k
-                            current_cte_table = org_name
-                        # find the matching column name in the cte_dict
-                        if temp[1] in temp_keys_dict.keys():
-                            ret_cols.extend(
-                                self.cte_dict[org_name][temp_keys_dict[temp[1]]]
-                            )
-                    # prefix yes, get the non-alias base table name
-                    else:
-                        ret_cols.append(org_name + "." + temp[1])
-                # prefix yes, is it from a function call temp col
-                elif i in self.function_call_cols.keys():
-                    ret_cols.extend(self.function_call_cols[i])
-                else:
-                    ret_cols.append(i)
-            else:
-                ret_cols.append(self.column_prefix_dict[i])
-        return list(set(ret_cols))
-
-    def _find_table(self, cte: CTE = None) -> Tuple[dict, List]:
-        """
-        Find aliases for the tables in the cte
-        :param cte: the sql of the sql to be analyzed
-        :return: the dict with table name as key and alias as child
-        """
-        table_alias_dict = {}
-        for table in cte.find_all(exp.Table):
-            table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
-            if len(table_def_split) == 1:
-                table_alias_dict[table_def_split[0]] = table_def_split[0]
-            else:
-                table_alias_dict[table_def_split[1]] = table_def_split[0]
-        # Find tables that's only in the CTE but not in the Subquery
-        temp_cte = cte.copy()
-        for sub_ast in temp_cte.find_all(exp.Subquery):
-            sub_ast.pop()
-        cte_table_list = []
-        for table in temp_cte.find_all(exp.Table):
-            table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
-            cte_table_list.append(table_def_split[0])
-        return table_alias_dict, cte_table_list
-
-    def _find_cte_col(self) -> dict:
-        """
-        Find the column names for each cte since it does not show in the execution plan
-        :param sql: the sql that needs to be analyzed
-        :return: the dict with table name as keys and list of columns as child
-        """
-        cte_col_dict = {}
-        for cte in self.sql_ast.find_all(exp.CTE):
-            cte_col_dict = self._find_cte_col_func(cte=cte, cte_col_dict=cte_col_dict)
-        for cte in self.sql_ast.find_all(exp.Subquery):
-            cte_col_dict = self._find_cte_col_func(cte=cte, cte_col_dict=cte_col_dict)
-        return cte_col_dict
-
-    def _find_cte_col_func(
-        self, cte: expressions = None, cte_col_dict: Optional[dict] = None
-    ) -> dict:
-        """
-        The function to find all the column names for the cte
-        :param cte: the cte ast tree
-        :param cte_col_dict: the dict that stores the column names for the previous cte
-        :return: the dict that contains column names with the current cte
-        """
-        # Find each CTE
-        cte_name = cte.find(exp.TableAlias).alias_or_name
-        cte_col_dict[cte_name] = []
-        # Iterate column for each CTE
-        for projection in cte.find(exp.Select).expressions:
-            col_name = projection.alias_or_name
-            # Resolve aggregations with no alias
-            if isinstance(projection, exp.Count):
-                col_name = "count"
-            elif isinstance(projection, exp.Avg):
-                col_name = "avg"
-            elif isinstance(projection, exp.Max):
-                col_name = "max"
-            elif isinstance(projection, exp.Min):
-                col_name = "min"
-            elif isinstance(projection, exp.Sum):
-                col_name = "sum"
-            # Resolve * and check if it is from a previous CTE or check database for the table
-            elif (
-                isinstance(projection, exp.Column) and projection.find(exp.Star)
-            ) or col_name == "*":
-                table_alias_dict, cte_table_list = self._find_table(cte=cte)
-                # if the * has a prefix
-                if projection.find(exp.Identifier):
-                    t_name = projection.find(exp.Identifier).text("this")
-                    if table_alias_dict[t_name] in cte_col_dict.keys():
-                        col_name = cte_col_dict[table_alias_dict[t_name]]
-                    else:
-                        col_name = find_column(
-                            table_name=table_alias_dict[t_name],
-                            engine=self.conn,
-                            search_schema=self.search_schema,
-                        )
-                # if * has no prefix
-                else:
-                    for t_name in cte_table_list:
-                        if t_name in cte_col_dict.keys():
-                            cte_col_dict[cte_name].extend(cte_col_dict[t_name])
-                        else:
-                            cte_col_dict[cte_name].extend(
-                                find_column(
-                                    table_name=t_name,
-                                    engine=self.conn,
-                                    search_schema=self.search_schema,
-                                )
-                            )
-            if isinstance(col_name, list):
-                cte_col_dict[cte_name].extend(col_name)
-            else:
-                if col_name != "*":
-                    cte_col_dict[cte_name].append(col_name)
-        return cte_col_dict
-
-
-if __name__ == "__main__":
-    pass
+import re
+from sqlglot import parse_one, exp
+from sqlglot.expressions import CTE
+from sqlglot import expressions
+from psycopg2.extensions import connection
+from typing import List, Tuple, Optional
+
+from .utils import find_column
+
+
+class ColumnLineage:
+    def __init__(
+        self,
+        plan: Optional[dict] = None,
+        sql: Optional[str] = "",
+        table_name: Optional[str] = "",
+        conn: connection = None,
+        part_tables: Optional[str] = None,
+        search_schema: Optional[str] = "",
+    ) -> None:
+        self.split_regex = re.compile(r"[^a-zA-Z0-9._]")
+        self.all_used_col = []
+        self.possible_columns = []
+        self.table_alias = {}
+        self.table_alias_reversed = {}
+        self.cte_name = ""
+        self.agg_flag = False
+        self.cte_dict = {}
+        self.subplan_dict = {}
+        self.function_call_cols = {}
+        self.part_tables = part_tables
+        self.column_prefix_dict = {}
+        self.conn = conn
+        self.search_schema = search_schema
+        self.sql_ast = parse_one(sql=sql, read="postgres")
+        self.cte_column = self._find_cte_col()
+        self.final_output = ""
+        self.final_node_type = ""
+        self.subquery_final_output = ""
+        self.column_dict = {}
+        self.table_list = []
+        self._traverse_plan(plan=plan)
+        self._resolve_column_dict(cols=self._find_final_column())
+        self.table_list = sorted(set(self.table_list))
+        # print(self.final_output)
+        # print(self.subplan_dict)
+        # print(self.table_alias)
+        # print(self.cte_dict)
+        # print(self.all_used_col)
+        # print(self.possible_columns)
+        # print("columns: ", self.column_dict)
+        # print("table: ", self.table_list)
+
+    def _find_final_column(self) -> List[str]:
+        """
+        Find all the column names in the final projection
+        :return: the list of column names in the final projection
+        """
+        # Pop all CTE and Subquery trees
+        for with_sql in self.sql_ast.find_all(exp.With):
+            with_sql.pop()
+        for sub_sql in self.sql_ast.find_all(exp.Subquery):
+            sub_sql.pop()
+        final_column_list = []
+        for projection in self.sql_ast.find(exp.Select).expressions:
+            col_name = projection.alias_or_name
+            # Resolve aggregations with no alias
+            if isinstance(projection, exp.Count):
+                col_name = "count"
+            elif isinstance(projection, exp.Avg):
+                col_name = "avg"
+            elif isinstance(projection, exp.Max):
+                col_name = "max"
+            elif isinstance(projection, exp.Min):
+                col_name = "min"
+            # Resolve * and check if it is from a previous CTE or check database for the table
+            elif (
+                isinstance(projection, exp.Column) and projection.find(exp.Star)
+            ) or col_name == "*":
+                main_table_list = []
+                for table in self.sql_ast.find_all(exp.Table):
+                    table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
+                    main_table_list.append(table_def_split[0])
+                # if the * has a prefix
+                if projection.find(exp.Identifier):
+                    t_name = projection.find(exp.Identifier).text("this")
+                    if table_alias_dict[t_name] in self.cte_column.keys():
+                        col_name = self.cte_column[table_alias_dict[t_name]]
+                    else:
+                        col_name = find_column(
+                            table_name=table_alias_dict[t_name],
+                            engine=self.conn,
+                            search_schema=self.search_schema,
+                        )
+                # if * has no prefix
+                else:
+                    for t_name in main_table_list:
+                        if t_name in self.cte_column.keys():
+                            final_column_list.extend(self.cte_column[t_name])
+                        else:
+                            final_column_list.extend(
+                                find_column(
+                                    table_name=t_name,
+                                    engine=self.conn,
+                                    search_schema=self.search_schema,
+                                )
+                            )
+            if isinstance(col_name, list):
+                final_column_list.extend(col_name)
+            else:
+                if col_name != "*":
+                    final_column_list.append(col_name)
+        return final_column_list
+
+    def _resolve_column_dict(self, cols: Optional[List] = None) -> None:
+        """
+        Insert into column_dict using the column names as keys and its dependencies as child
+        :param cols: the columns for the final output
+        :return: None
+        """
+        if len(self.final_output) > len(cols):
+            self.final_output = self.final_output[: len(cols)]
+        elif len(self.final_output) < len(cols):
+            print(
+                "number of columns from the sql does not match the number in manifest"
+            )
+            return
+        for idx, val in enumerate(self.final_output):
+            # Postgres Aggregate function of count(*) that involves all the columns
+            if self.final_node_type == "Aggregate" and val.strip() == "count(*)":
+                all_cols = self.possible_columns
+            else:
+                table_col = re.split(self.split_regex, val.strip())
+                all_cols = list(
+                    set(set(table_col) & set(self.possible_columns)).union(
+                        self.all_used_col
+                    )
+                )
+            # Subquery in the final projection
+            if val.find("SubPlan ") != -1:
+                subplan_name = re.findall(re.compile(r"SubPlan [0-9]*"), val)[0]
+                all_cols.extend(self.subplan_dict[subplan_name])
+            self.column_dict[cols[idx]] = sorted(
+                self._remove_table_alias(cols=all_cols)
+            )
+
+    def _traverse_plan(self, plan: Optional[dict] = None) -> None:
+        """
+        Traversing the plan using recursion and go into Plans if it is present
+        :param plan: the given execution plan
+        :return: None
+        """
+        if plan["Node Type"] in [
+            "Seq Scan",
+            "Parallel Seq Scan",
+            "Bitmap Heap Scan",
+            "Index Scan",
+            "Index Only Scan",
+        ]:
+            self.table_alias[plan["Alias"]] = self._find_parent_table(
+                table=plan["Schema"] + "." + plan["Relation Name"]
+            )
+            self.table_alias_reversed[
+                plan["Schema"] + "." + plan["Relation Name"]
+            ] = plan["Alias"]
+        if "Plans" in plan.keys():
+            for subplan_data in plan["Plans"]:
+                self._traverse_plan(plan=subplan_data)
+        temp = plan.get("Output")
+        if temp is not None:
+            self.final_output = temp
+            self.final_node_type = plan.get("Node Type")
+        # if scan from tables/views, add to possible columns
+        if plan["Node Type"] in [
+            "Seq Scan",
+            "Parallel Seq Scan",
+            "Bitmap Heap Scan",
+            "Index Scan",
+            "Index Only Scan",
+        ]:
+            # Scan and Filter and CTE in one
+            if "Subplan Name" in plan.keys():
+                self._add_possible_columns(plan)
+                # self.possible_columns.extend(plan["Output"])
+                if "Alias" in plan.keys():
+                    alias = plan["Alias"]
+                else:
+                    alias = plan["Schema"] + "." + plan["Relation Name"]
+                temp_regex = re.compile(r"({}\.[a-zA-Z0-9_]+)".format(alias))
+                # print(plan['Subplan Name'], plan['Output'])
+                for i in plan["Output"]:
+                    self.possible_columns.extend(re.findall(temp_regex, i))
+                if "Filter" in plan.keys():
+                    self.possible_columns.extend(re.findall(temp_regex, plan["Filter"]))
+                cte_name = plan["Subplan Name"].split(" ")[1]
+                self.table_list.append(
+                    self._find_parent_table(
+                        table=(plan["Schema"] + "." + plan["Relation Name"])
+                    )
+                )
+                self.table_alias[cte_name] = cte_name
+                self._add_cte_dict(plan=plan)
+            # Filter and scan in one plan
+            elif "Filter" in plan.keys():
+                self._add_possible_columns(plan)
+                # self.possible_columns.extend(plan["Output"])
+                self._handle_filter_in_scan(plan=plan)
+                # in the filter, there is chance there is also index cond
+                self._handle_index_cond(plan=plan)
+            # Scan only
+            else:
+                # to avoid index cond
+                self._add_possible_columns(plan=plan)
+                self._handle_index_cond(plan=plan)
+        # if scan from cte
+        elif plan["Node Type"] == "CTE Scan":
+            # add to possible column first and add all columns from CTE to prevent filters on top of any
+            if "Alias" in plan.keys():
+                all_cte_cols = [
+                    plan["Alias"] + "." + s
+                    for s in list(self.cte_dict[plan["CTE Name"]].keys())
+                ]
+            else:
+                all_cte_cols = [
+                    plan["CTE Name"] + "." + s
+                    for s in list(self.cte_dict[plan["CTE Name"]].keys())
+                ]
+            self.possible_columns.extend(
+                list(set(all_cte_cols).union(set(plan["Output"])))
+            )
+            # handle filter and scan in the same plan
+            if "Filter" in plan.keys():
+                self._handle_filter_in_scan(plan=plan)
+            # the current scan can also be the creation of another cte
+            if "Subplan Name" in plan.keys():
+                if "CTE Name" in plan.keys():
+                    self.possible_columns.extend(
+                        [
+                            plan["CTE Name"] + "." + s
+                            for s in list(self.cte_dict[plan["CTE Name"]].keys())
+                        ]
+                    )
+                self.table_alias[plan["Alias"]] = plan["CTE Name"]
+                self._add_cte_dict(plan=plan)
+            else:
+                # if just a scan, add to alias
+                self.table_alias[plan["Alias"]] = plan["CTE Name"]
+        # if scan from a subquery
+        elif plan["Node Type"] == "Subquery Scan":
+            org_all_used_cols = self.all_used_col
+            org_possible_cols = self.possible_columns
+            self.all_used_col = []
+            self.possible_columns = []
+            if "Plans" in plan.keys():
+                self.subquery_final_output = plan["Plans"][0]["Output"]
+            else:
+                self.subquery_final_output = plan["Output"]
+            self._resolve_subquery(plan=plan)
+            if "Alias" in plan.keys():
+                self.cte_name = plan["Alias"]
+            temp_dict = {}
+            self._extract_from_cond(plan=plan)
+            if self.cte_name in self.cte_column.keys():
+                for idx, val in enumerate(self.cte_column[self.cte_name]):
+                    cte_col = re.split(
+                        self.split_regex, self.subquery_final_output[idx].strip()
+                    )
+                    all_cols = list(
+                        set(set(cte_col) & set(self.possible_columns)).union(
+                            self.all_used_col
+                        )
+                    )
+                    # Subquery in the final projection
+                    if self.subquery_final_output[idx].find("SubPlan ") != -1:
+                        subplan_name = re.findall(
+                            re.compile(r"SubPlan [0-9]*"),
+                            self.subquery_final_output[idx],
+                        )[0]
+                        all_cols.extend(self.subplan_dict[subplan_name])
+                    temp_dict[val] = self._remove_table_alias(cols=all_cols)
+                self.cte_dict[self.cte_name] = temp_dict
+            self.table_alias[plan["Alias"]] = plan["Alias"]
+            self.all_used_col = org_all_used_cols
+            self.possible_columns = org_possible_cols
+            self.possible_columns.extend(plan["Output"])
+        else:
+            # creation of cte but with an Append node(usually UNION/EXCEPT/INTERSECT)
+            if "Subplan Name" in plan.keys():
+                # Resolve UNION/EXCEPT/INTERSECT since the Node Type will be Appended with no outputs
+                if (
+                    plan["Node Type"] in ["Append", "MergeAppend"]
+                    and "Output" not in plan.keys()
+                    and len(plan["Plans"]) != 0
+                ):
+                    s = plan.get("Subplan Name").split(" ")
+                    if s[0] == "CTE":
+                        self.cte_name = s[1]
+                        temp_dict = {}
+                        self._extract_from_cond(plan=plan)
+                        self._resolve_union(plan=plan)
+                        self.agg_flag = False
+                        for val in self.cte_column[self.cte_name]:
+                            temp_dict[val] = self._remove_table_alias(
+                                cols=self.all_used_col
+                            )
+                        self.cte_dict[self.cte_name] = temp_dict
+                        self.all_used_col = []
+                        self.possible_columns = []
+                else:
+                    # if only creation of a cte, but no scan, just add it to cte_dict
+                    self._add_cte_dict(plan=plan)
+            # UNION/EXCEPT/INTERSECT at the last step with no creation of CTE
+            elif (
+                plan["Node Type"] in ["Append", "MergeAppend"]
+                and "Output" not in plan.keys()
+                and len(plan["Plans"]) != 0
+            ):
+                self._extract_from_cond(plan=plan)
+                self._resolve_union(plan=plan)
+                self.agg_flag = False
+            # every other node aside from cte creations/scans
+            else:
+                self._extract_from_cond(plan=plan)
+
+    def _handle_index_cond(self, plan: Optional[dict] = None) -> None:
+        """
+        When there's an index_cond in the plan, handle it and extract the necessary columns
+        :param plan: the plan with the index_cond
+        """
+        temp = plan.get("Index Cond")
+        if temp is not None:
+            idx_name = plan.get("Index Name")
+            if idx_name is not None:
+                cur = self.conn.cursor()
+                cur.execute("""SET search_path TO {};""".format(self.search_schema))
+                cur.execute(
+                    "SELECT schemaname, tablename, indexname, indexdef FROM pg_indexes WHERE indexname = '{}'".format(
+                        idx_name
+                    )
+                )
+                result = cur.fetchall()[0]
+                cur.close()
+                # the indexdef is at index 3
+                indexdef = result[3]
+                btree_idx = indexdef.find("USING btree")
+                if btree_idx != -1:
+                    close_bracket = indexdef.find(")", btree_idx)
+                    if close_bracket != -1:
+                        idx_cols = indexdef[btree_idx + 13 : close_bracket].split(",")
+                        alias = self.table_alias_reversed[result[0] + "." + result[1]]
+                        for i in idx_cols:
+                            self.possible_columns.append(alias + "." + i)
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+
+    def _handle_filter_in_scan(self, plan: Optional[dict] = None) -> None:
+        """
+        When there is filter in the scan node, handle it and find necessary columns
+        :param plan: the plan with the filter in the scan node
+        """
+        if "Alias" in plan.keys():
+            alias = plan["Alias"]
+        else:
+            alias = plan["Schema"] + "." + plan["Relation Name"]
+        temp_regex = re.compile(r"({}\.[a-zA-Z0-9_]+)".format(alias))
+        self.possible_columns.extend(re.findall(temp_regex, plan["Filter"]))
+        temp = plan.get("Filter")
+        row_col = re.split(self.split_regex, temp.strip())
+        self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        if temp.find("SubPlan ") != -1:
+            subplan_name = re.findall(re.compile(r"SubPlan [0-9]*"), temp)[0]
+            self.all_used_col.extend(self.subplan_dict[subplan_name])
+
+    def _resolve_subquery(self, plan: Optional[dict] = None) -> None:
+        """
+        When there is a node with subquery, go in recursively and find the most inner node
+        :param plan: the node with subquery
+        """
+        if "Plans" in plan.keys():
+            for subplan_data in plan["Plans"]:
+                self._resolve_subquery(plan=subplan_data)
+        if "Output" in plan.keys() and plan["Node Type"] in [
+            "Seq Scan",
+            "Parallel Seq Scan",
+            "Bitmap Heap Scan",
+            "Index Scan",
+            "Index Only Scan",
+            "CTE Scan",
+        ]:
+            self.possible_columns.extend(plan["Output"])
+            self._extract_from_cond(plan=plan)
+        else:
+            self._extract_from_cond(plan=plan)
+
+    def _resolve_union(self, plan: Optional[dict] = None) -> None:
+        """
+        To resolve the UNION, all the columns involved are used since those columns need to be the same
+        :param plan: the execution plan for UNION/EXCEPT/INTERSECT
+        """
+        if "Plans" in plan.keys():
+            # Check if it is an aggregation, since it would scan all the columns
+            if plan["Plans"][0]["Node Type"] == "Aggregate":
+                self.agg_flag = True
+            for subplan_data in plan["Plans"]:
+                self._resolve_union(plan=subplan_data)
+        if (
+            "Output" in plan.keys()
+            and plan["Node Type"]
+            in [
+                "Seq Scan",
+                "Parallel Seq Scan",
+                "Bitmap Heap Scan",
+                "Index Scan",
+                "Index Only Scan",
+            ]
+            and not self.agg_flag
+        ):
+            # check if it is using Append node for partitioned tables
+            if plan["Schema"] + "." + plan["Relation Name"] in list(
+                self.part_tables.keys()
+            ):
+                self.possible_columns.extend(plan["Output"])
+                self._extract_from_cond(plan=plan)
+            else:
+                # if it is using Append node for UNION/EXCEPT/INTERSECT
+                for col in plan["Output"]:
+                    row_col = re.split(self.split_regex, col.strip())
+                    self.all_used_col.extend(
+                        list(set(row_col) & set(self.possible_columns))
+                    )
+        elif (
+            "Output" in plan.keys()
+            and plan["Node Type"] == "CTE Scan"
+            and not self.agg_flag
+        ):
+            # if it is using Append node for UNION/EXCEPT/INTERSECT
+            for col in plan["Output"]:
+                row_col = re.split(self.split_regex, col.strip())
+                self.all_used_col.extend(
+                    list(set(row_col) & set(self.possible_columns))
+                )
+
+    def _add_cte_dict(self, plan: Optional[dict] = None) -> None:
+        """
+        Add to the cte dict given the CTE plan and analyze its column lineage
+        :param plan: the CTE plan
+        :return:
+        """
+        s = plan.get("Subplan Name").split(" ")
+        if s[0] == "CTE":
+            self.cte_name = s[1]
+            temp_dict = {}
+            self._extract_from_cond(plan=plan)
+            for idx, val in enumerate(self.cte_column[self.cte_name]):
+                cte_col = re.split(self.split_regex, plan["Output"][idx].strip())
+                all_cols = list(
+                    set(set(cte_col) & set(self.possible_columns)).union(
+                        self.all_used_col
+                    )
+                )
+                # Subquery in the final projection
+                if plan["Output"][idx].find("SubPlan ") != -1:
+                    subplan_name = re.findall(
+                        re.compile(r"SubPlan [0-9]*"), plan["Output"][idx]
+                    )[0]
+                    all_cols.extend(self.subplan_dict[subplan_name])
+                temp_dict[val] = self._remove_table_alias(cols=all_cols)
+            self.cte_dict[self.cte_name] = temp_dict
+            self.all_used_col = []
+            self.possible_columns = []
+        # temporary subplan name
+        elif s[0] == "SubPlan":
+            subplan_list = []
+            for _, val in enumerate(plan["Output"]):
+                table_col = re.split(self.split_regex, val.strip())
+                all_cols = list(set(set(table_col) & set(self.possible_columns)))
+                subplan_list.extend(self._remove_table_alias(cols=all_cols))
+            self.subplan_dict[plan["Subplan Name"]] = subplan_list
+
+    def _extract_from_cond(self, plan: Optional[dict] = None) -> None:
+        """
+        Extract column from multiple operators, some add to possible_cols and some add to all_used_cols
+        :param plan: the execution plan for the operator
+        :return:
+        """
+        # More conditions
+        if plan["Node Type"] == "WindowAgg":
+            self.possible_columns.extend(plan["Output"])
+        # Handle index cond
+        self._handle_index_cond(plan=plan)
+        temp = plan.get("Hash Cond")
+        if temp is not None:
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        temp = plan.get("Merge Cond")
+        if temp is not None:
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        temp = plan.get("Recheck Cond")
+        if temp is not None:
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        temp = plan.get("Join Filter")
+        if temp is not None:
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        temp = plan.get("Filter")
+        if temp is not None:
+            row_col = re.split(self.split_regex, temp.strip())
+            self.all_used_col.extend(list(set(row_col) & set(self.possible_columns)))
+        temp = plan.get("Sort Key")
+        if temp is not None:
+            self.all_used_col.extend(list(set(temp) & set(self.possible_columns)))
+        temp = plan.get("Group Key")
+        if temp is not None:
+            self.all_used_col.extend(list(set(temp) & set(self.possible_columns)))
+        # Function calls
+        if plan["Node Type"] == "Function Scan":
+            if "Function Name" in plan.keys():
+                if plan["Function Name"] == "unnest":
+                    func_cols = re.split(
+                        self.split_regex, plan["Function Call"].strip()
+                    )
+                    all_cols = list(
+                        set(set(func_cols) & set(self.possible_columns)).union(
+                            self.all_used_col
+                        )
+                    )
+                    self.function_call_cols[plan["Output"][0]] = sorted(
+                        self._remove_table_alias(cols=all_cols)
+                    )
+                    self.possible_columns.append(plan["Output"][0])
+
+    def _add_possible_columns(self, plan: Optional[dict] = None) -> None:
+        """
+        Extract the columns/tables from the plan and add to possible columns and used tables, mainly used for base table
+        :param plan: plan to extract columns and tables
+        :return:
+        """
+        invalid_list = []
+        for i in plan["Output"]:
+            if len(i.split(".")) == 1:
+                self.column_prefix_dict[i] = (
+                    plan["Schema"] + "." + plan["Relation Name"] + "." + i
+                )
+        for i in plan["Output"]:
+            # if a column name contains an invalid char(that is not a-zA-z0-9_)
+            if re.search(r"[^\w.]", i):
+                invalid_list.append(i)
+                continue
+            # if a column name starts with a digit, likely is just a number, but not a column
+            elif i[0].isdigit():
+                continue
+            # no table prefix column outputs, append only the column name and the prefix + column
+            elif len(i.split(".")) == 1:
+                if "Alias" in plan.keys():
+                    prefix = plan["Alias"]
+                else:
+                    prefix = plan["Schema"] + "." + plan["Relation Name"]
+                self.possible_columns.append(prefix + "." + i)
+                self.possible_columns.append(i)
+            else:
+                self.possible_columns.append(i)
+        # if an output has invalid char, its likely it's an expression, have to extract the columns
+        if invalid_list:
+            all_table_cols = find_column(
+                table_name=plan["Schema"] + "." + plan["Relation Name"],
+                engine=self.conn,
+                search_schema=self.search_schema,
+            )
+            for i in invalid_list:
+                # split the output and match columns from all the columns of the table
+                table_col = re.split(self.split_regex, i.strip())
+                resolved_possible_cols = list(set(set(table_col) & set(all_table_cols)))
+                for j in resolved_possible_cols:
+                    self.possible_columns.append(j)
+                    if len(j.split(".")) == 1:
+                        self.column_prefix_dict[j] = (
+                            plan["Schema"] + "." + plan["Relation Name"] + "." + j
+                        )
+        self.table_list.append(
+            self._find_parent_table(table=plan["Schema"] + "." + plan["Relation Name"])
+        )
+        self.table_alias[plan["Alias"]] = self._find_parent_table(
+            table=plan["Schema"] + "." + plan["Relation Name"]
+        )
+        self.table_alias_reversed[plan["Schema"] + "." + plan["Relation Name"]] = plan[
+            "Alias"
+        ]
+
+    def _find_parent_table(self, table: Optional[str] = "") -> str:
+        """
+        Find the parent table from a given table name
+        :param table: table name
+        :return: table: the parent table name(if it is not partitioned table, it is just the input
+        """
+        if self.part_tables is not None:
+            if table in self.part_tables.keys():
+                table = self.part_tables[table]
+        return table
+
+    def _remove_table_alias(self, cols: Optional[List] = None) -> List:
+        """
+        Remove the alias in the name or add intended schema.table to column names
+        :param cols: the list of columns that has aliases that need to be resolved
+        :return: resolved aliases for the columns
+        """
+        current_cte_table = ""
+        ret_cols = []
+        temp_keys_dict = {}
+        for i in cols:
+            temp = i.split(".")
+            # has prefix or no
+            if len(temp) > 1:
+                # prefix yes, is the prefix already in alias or base table name
+                if temp[0] in self.table_alias.keys():
+                    org_name = self.table_alias[temp[0]]
+                    # prefix yes, get the non-alias cte name
+                    if org_name in self.cte_dict.keys():
+                        # to avoid case difference, create a temp dict for lower->original
+                        # if the current cte's temp dict is already created, skip it
+                        if org_name != current_cte_table:
+                            cte_dict_keys = list(self.cte_dict[org_name].keys())
+                            temp_keys_dict = {}
+                            for k in cte_dict_keys:
+                                temp_keys_dict[k.lower()] = k
+                            current_cte_table = org_name
+                        # find the matching column name in the cte_dict
+                        if temp[1] in temp_keys_dict.keys():
+                            ret_cols.extend(
+                                self.cte_dict[org_name][temp_keys_dict[temp[1]]]
+                            )
+                    # prefix yes, get the non-alias base table name
+                    else:
+                        ret_cols.append(org_name + "." + temp[1])
+                # prefix yes, is it from a function call temp col
+                elif i in self.function_call_cols.keys():
+                    ret_cols.extend(self.function_call_cols[i])
+                else:
+                    ret_cols.append(i)
+            else:
+                ret_cols.append(self.column_prefix_dict[i])
+        return list(set(ret_cols))
+
+    def _find_table(self, cte: CTE = None) -> Tuple[dict, List]:
+        """
+        Find aliases for the tables in the cte
+        :param cte: the sql of the sql to be analyzed
+        :return: the dict with table name as key and alias as child
+        """
+        table_alias_dict = {}
+        for table in cte.find_all(exp.Table):
+            table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
+            if len(table_def_split) == 1:
+                table_alias_dict[table_def_split[0]] = table_def_split[0]
+            else:
+                table_alias_dict[table_def_split[1]] = table_def_split[0]
+        # Find tables that's only in the CTE but not in the Subquery
+        temp_cte = cte.copy()
+        for sub_ast in temp_cte.find_all(exp.Subquery):
+            sub_ast.pop()
+        cte_table_list = []
+        for table in temp_cte.find_all(exp.Table):
+            table_def_split = re.split(" AS ", table.sql(), flags=re.IGNORECASE)
+            cte_table_list.append(table_def_split[0])
+        return table_alias_dict, cte_table_list
+
+    def _find_cte_col(self) -> dict:
+        """
+        Find the column names for each cte since it does not show in the execution plan
+        :param sql: the sql that needs to be analyzed
+        :return: the dict with table name as keys and list of columns as child
+        """
+        cte_col_dict = {}
+        for cte in self.sql_ast.find_all(exp.CTE):
+            cte_col_dict = self._find_cte_col_func(cte=cte, cte_col_dict=cte_col_dict)
+        for cte in self.sql_ast.find_all(exp.Subquery):
+            cte_col_dict = self._find_cte_col_func(cte=cte, cte_col_dict=cte_col_dict)
+        return cte_col_dict
+
+    def _find_cte_col_func(
+        self, cte: expressions = None, cte_col_dict: Optional[dict] = None
+    ) -> dict:
+        """
+        The function to find all the column names for the cte
+        :param cte: the cte ast tree
+        :param cte_col_dict: the dict that stores the column names for the previous cte
+        :return: the dict that contains column names with the current cte
+        """
+        # Find each CTE
+        cte_name = cte.find(exp.TableAlias).alias_or_name
+        cte_col_dict[cte_name] = []
+        # Iterate column for each CTE
+        for projection in cte.find(exp.Select).expressions:
+            col_name = projection.alias_or_name
+            # Resolve aggregations with no alias
+            if isinstance(projection, exp.Count):
+                col_name = "count"
+            elif isinstance(projection, exp.Avg):
+                col_name = "avg"
+            elif isinstance(projection, exp.Max):
+                col_name = "max"
+            elif isinstance(projection, exp.Min):
+                col_name = "min"
+            elif isinstance(projection, exp.Sum):
+                col_name = "sum"
+            # Resolve * and check if it is from a previous CTE or check database for the table
+            elif (
+                isinstance(projection, exp.Column) and projection.find(exp.Star)
+            ) or col_name == "*":
+                table_alias_dict, cte_table_list = self._find_table(cte=cte)
+                # if the * has a prefix
+                if projection.find(exp.Identifier):
+                    t_name = projection.find(exp.Identifier).text("this")
+                    if table_alias_dict[t_name] in cte_col_dict.keys():
+                        col_name = cte_col_dict[table_alias_dict[t_name]]
+                    else:
+                        col_name = find_column(
+                            table_name=table_alias_dict[t_name],
+                            engine=self.conn,
+                            search_schema=self.search_schema,
+                        )
+                # if * has no prefix
+                else:
+                    for t_name in cte_table_list:
+                        if t_name in cte_col_dict.keys():
+                            cte_col_dict[cte_name].extend(cte_col_dict[t_name])
+                        else:
+                            cte_col_dict[cte_name].extend(
+                                find_column(
+                                    table_name=t_name,
+                                    engine=self.conn,
+                                    search_schema=self.search_schema,
+                                )
+                            )
+            if isinstance(col_name, list):
+                cte_col_dict[cte_name].extend(col_name)
+            else:
+                if col_name != "*":
+                    cte_col_dict[cte_name].append(col_name)
+        return cte_col_dict
+
+
+if __name__ == "__main__":
+    pass
```

### Comparing `lineagex-0.0.1/lineagex/ColumnLineageNoConn.py` & `lineagex-0.0.1a1/lineagex/ColumnLineageNoConn.py`

 * *Ordering differences only*

 * *Files 12% similar despite different names*

```diff
@@ -1,326 +1,326 @@
-from sqlglot import parse_one, exp
-from sqlglot import expressions
-from typing import Optional, List, Tuple
-import os
-
-shared_conditions = [exp.Where, exp.EQ, exp.Group, exp.Having, exp.Order]
-shared_conditions_with_table = [exp.Where, exp.EQ, exp.Group, exp.Having, exp.Order, exp.From, exp.Join]
-
-
-class ColumnLineageNoConn:
-    def __init__(self, sql: Optional[str] = "", input_table_dict: Optional[dict] = None):
-        self.column_dict = {}
-        self.table_alias_dict = {}
-        self.cte_table_dict = {}
-        self.cte_dict = {}
-        self.input_table_dict = input_table_dict
-        self.sql_ast = parse_one(sql, read="postgres")
-        self.all_used_col = []
-        self.table_list = []
-        self.all_subquery_table = []
-        self.sub_tables = []
-        self.sub_cols = []
-        self._run_cte_lineage()
-        # Everything other than CTEs, and pop the CTE tree
-        for with_sql in self.sql_ast.find_all(exp.With):
-            with_sql.pop()
-        self._sub_shared_col_conds(sql_ast=self.sql_ast)
-        self._run_lineage(self.sql_ast, False)
-        #print(self.cte_dict)
-        #print(self.column_dict)
-        #print(self.table_list)
-
-    def _run_lineage(self, sql_ast: expressions = None, subquery_flag: bool = False) -> None:
-        """
-        Run the lineage after all the cte and subquery are resolved
-        :param sql_ast: the ast for the sql
-        :param subquery_flag: check if it is a subquery
-        """
-        #print(sql_ast)
-        if not subquery_flag:
-            main_tables = self._resolve_table(part_ast=sql_ast)
-            self.table_list = self._find_all_tables(temp_table_list=main_tables)
-            self.table_list.extend(self.all_subquery_table)
-            self.all_used_col = []
-            self._shared_col_conds(part_ast=sql_ast, used_tables=main_tables)
-            self.all_used_col.extend(self.sub_cols)
-            if isinstance(sql_ast, exp.Union) or isinstance(sql_ast, exp.Except) or isinstance(sql_ast, exp.Intersect):
-                for col in sql_ast.find_all(exp.Column):
-                    self.all_used_col.extend(self._find_alias_col(col_sql=col.sql(), temp_table=main_tables))
-            self.all_used_col = set(self.all_used_col)
-            if sql_ast.find(exp.Select):
-                for projection in sql_ast.find(exp.Select).expressions:
-                    col_name = projection.alias_or_name
-                    self.column_dict = self._resolve_proj(projection=projection, col_name=col_name, target_dict=self.column_dict, source_table=main_tables)
-        else:
-            temp_sub_cols = []
-            for col in sql_ast.find_all(exp.Column):
-                temp_sub_cols.extend(self._find_alias_col(col_sql=col.sql(), temp_table=self.sub_tables))
-            self.sub_cols.extend(temp_sub_cols)
-            #print(temp_sub_cols)
-
-    def _sub_shared_col_conds(self, sql_ast: expressions = None) -> None:
-        """
-        After the cte are resolved, run the subquery ast that is with the shared conditions(WHERE, GROUP BY, etc)
-        :param sql_ast: the ast without the cte
-        """
-        # add in more conditions, including FROM/JOIN
-        for cond in shared_conditions_with_table:
-            for cond_sql in sql_ast.find_all(cond):
-                for sub_ast in cond_sql.find_all(exp.Subquery):
-                    self.sub_tables = self._resolve_table(part_ast=sub_ast)
-                    self.all_subquery_table.extend(self._find_all_tables(temp_table_list=self.sub_tables))
-                    self._run_lineage(sub_ast, True)
-                    sub_ast.pop()
-
-    def _sub_shared_col_conds_cte(self, sql_ast: expressions = None) -> Tuple[List, List]:
-        """
-        Run the subquery inside the cte first that is with the shared conditions(WHERE, GROUP BY, etc)
-        :param sql_ast: the ast for the cte
-        """
-        all_cte_sub_table = []
-        all_cte_sub_cols = []
-        # add in more conditions, including FROM/JOIN
-        for cond in shared_conditions_with_table:
-            for cond_sql in sql_ast.find_all(cond):
-                for sub_ast in cond_sql.find_all(exp.Select):
-                    temp_sub_table = self._resolve_table(part_ast=sub_ast)
-                    temp_sub_cols = []
-                    for col in sub_ast.find_all(exp.Column):
-                        temp_sub_cols.extend(self._find_alias_col(col_sql=col.sql(), temp_table=temp_sub_table))
-                    all_cte_sub_table.extend(self._find_all_tables(temp_table_list=temp_sub_table))
-                    all_cte_sub_cols.extend(temp_sub_cols)
-                    sub_ast.pop()
-        return all_cte_sub_table, all_cte_sub_cols
-
-    def _run_cte_lineage(self):
-        """
-        Run the lineage information for all the cte
-        """
-        for cte in self.sql_ast.find_all(exp.CTE):
-            all_cte_sub_table, all_cte_sub_cols = self._sub_shared_col_conds_cte(sql_ast=cte)
-            self.all_used_col = []
-            temp_cte_dict = {}
-            temp_cte_table = self._resolve_table(part_ast=cte)
-            cte_name = cte.find(exp.TableAlias).alias_or_name
-            self.cte_table_dict[cte_name] = list(set(self._find_all_tables(temp_table_list=temp_cte_table) + all_cte_sub_table))
-            # Resolving shared conditions
-            self._shared_col_conds(part_ast=cte, used_tables=temp_cte_table)
-            self.all_used_col.extend(all_cte_sub_cols)
-            self.all_used_col = set(self.all_used_col)
-            # Resolving the projection
-            for projection in cte.find(exp.Select).expressions:
-                col_name = projection.alias_or_name
-                temp_cte_dict = self._resolve_proj(projection=projection, col_name=col_name, target_dict=temp_cte_dict, source_table=temp_cte_table)
-            self.cte_dict[cte_name] = temp_cte_dict
-
-    def _resolve_proj(self, projection: expressions = None, col_name: Optional[str] = "", target_dict: Optional[dict] = None, source_table: Optional[List] = None) -> dict:
-        """
-        Resolve the projection given the projection expression
-        :param projection: the given projection
-        :param col_name: the column name
-        :param target_dict: the dict it is outputting to
-        :param source_table: all the source tables that this column might originate from
-        """
-        # Resolve count(*) with no alias, potentially other aggregations, MIN, MAX, SUM
-        if isinstance(projection, exp.Count) or isinstance(projection.unalias(), exp.Count)\
-                or isinstance(projection, exp.Avg) or isinstance(projection.unalias(), exp.Avg)\
-                or isinstance(projection, exp.Max) or isinstance(projection.unalias(), exp.Max)\
-                or isinstance(projection, exp.Min) or isinstance(projection.unalias(), exp.Min)\
-                or isinstance(projection, exp.Sum) or isinstance(projection.unalias(), exp.Sum):
-            if isinstance(projection, exp.Count):
-                col_name = "count"
-                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
-            elif isinstance(projection, exp.Avg):
-                col_name = "avg"
-                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
-            elif isinstance(projection, exp.Max):
-                col_name = "max"
-                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
-            elif isinstance(projection, exp.Min):
-                col_name = "min"
-                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
-            elif isinstance(projection, exp.Sum):
-                col_name = "sum"
-                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
-            else:
-                self._resolve_agg_star(col_name=col_name, projection=projection.unalias(), used_tables=source_table)
-        else:
-            proj_columns = []
-            # Resolve only *
-            if not isinstance(projection, exp.Column) and projection.find(exp.Star):
-                for t_name in source_table:
-                    if t_name in self.input_table_dict.keys():
-                        star_cols = self.input_table_dict[t_name]
-                        # every column from there will be a column with that name
-                        for per_star_col in star_cols:
-                            target_dict[per_star_col] = sorted(
-                                list(set(self._find_alias_col(col_sql=per_star_col, temp_table=source_table)).union(
-                                    self.all_used_col)))
-                    elif t_name in self.cte_dict.keys():
-                        star_cols = list(self.cte_dict[t_name].keys())
-                        for per_star_col in star_cols:
-                            target_dict[per_star_col] = sorted(
-                                list(set(self.cte_dict[t_name][per_star_col]).union(self.all_used_col)))
-            # Resolve projections that have many columns, some of which could be *
-            for p in projection.find_all(exp.Column):
-                # Resolve * with other columns
-                if isinstance(p, exp.Column) and p.find(exp.Star):
-                    t_name = p.find(exp.Identifier).text("this")
-                    # Resolve alias
-                    if t_name in self.table_alias_dict.keys():
-                        t_name = self.table_alias_dict[t_name]
-                    # If from input table, get all columns from there
-                    if t_name in self.input_table_dict.keys():
-                        star_cols = self.input_table_dict[t_name]
-                        # every column from there will be a column with that name
-                        for per_star_col in star_cols:
-                            target_dict[per_star_col] = sorted(
-                                list(set(self._find_alias_col(col_sql=per_star_col, temp_table=source_table)).union(
-                                    self.all_used_col)))
-                    # If from another CTE, get all columns from there
-                    elif t_name in self.cte_dict.keys():
-                        star_cols = list(self.cte_dict[t_name].keys())
-                        for per_star_col in star_cols:
-                            target_dict[per_star_col] = sorted(
-                                list(set(self.cte_dict[t_name][per_star_col]).union(self.all_used_col)))
-                    # If from an unknown table, leave it with a STAR as temporary name
-                    else:
-                        target_dict[p.sql()] = [p.sql()] + (list(self.all_used_col))
-                else:
-                    # one projection can have many columns, append first
-                    proj_columns.extend(self._find_alias_col(col_sql=p.sql(), temp_table=source_table))
-            if proj_columns:
-                target_dict[col_name] = sorted(list(set(proj_columns).union(self.all_used_col)))
-        return target_dict
-
-    def _resolve_table(self, part_ast: expressions = None) -> List:
-        """
-        Find the tables in the given ast
-        :param part_ast: the ast to find the table
-        """
-        temp_table_list = []
-        # Resolve FROM
-        for table_sql in part_ast.find_all(exp.From):
-            for table in table_sql.find_all(exp.Table):
-                temp_table_list = self._find_table(table=table, temp_table_list=temp_table_list)
-        # Resolve JOIN
-        for table_sql in part_ast.find_all(exp.Join):
-            for table in table_sql.find_all(exp.Table):
-                temp_table_list = self._find_table(table=table, temp_table_list=temp_table_list)
-        return temp_table_list
-
-    def _find_table(self, table: expressions = None, temp_table_list: Optional[List] = None) -> List:
-        """
-        Update table alias and find all aliased used table names
-        :param table: the expression with the table
-        :param temp_table_list: temporary list of tables for appending the used tables
-        :return:
-        """
-        if table.alias == "":
-            self.table_alias_dict[table.sql()] = table.sql()
-            temp_table_list.append(table.sql())
-        else:
-            temp = table.sql().split(" ")
-            if temp[1] == "AS" or temp[1] == "as":
-                self.table_alias_dict[temp[2]] = temp[0]
-                temp_table_list.append(temp[0])
-        return temp_table_list
-
-    def _find_all_tables(self, temp_table_list: Optional[List] = None) -> List:
-        """
-        Update the used table names, such as if a CTE, update it with the dependant tables
-        :param temp_table_list: temporary list of tables for appending the used tables
-        :return:
-        """
-        ret_table = []
-        for i in temp_table_list:
-            table_name = i
-            if i in self.table_alias_dict.keys():
-                table_name = self.table_alias_dict[i]
-            if table_name in self.cte_table_dict.keys():
-                ret_table.extend(self.cte_table_dict[table_name])
-            else:
-                ret_table.append(table_name)
-        return ret_table
-
-    def _shared_col_conds(self, part_ast: expressions = None, used_tables: Optional[List] = None):
-        """
-        Extract all the columns in the shared conditions(WHERE, GROUP BY, etc)
-        :param part_ast: the ast of the sql to extract
-        :param used_tables: the tables that this sql uses
-        """
-        # COMBINE THE CONDITIONS
-        for cond in shared_conditions:
-            for cond_sql in part_ast.find_all(cond):
-                for cond_col in cond_sql.find_all(exp.Column):
-                    self.all_used_col.extend(self._find_alias_col(col_sql=cond_col.sql(), temp_table=used_tables))
-
-    def _find_alias_col(self, col_sql: Optional[str] = "", temp_table: Optional[List] = None) -> List:
-        """
-        Find the columns and its alias and dependencies if it is from a cte
-        :param col_sql: the sql to the column
-        :param temp_table: the table that the sql uses
-        :return:
-        """
-        temp = col_sql.split(".")
-        # trying to deduce the table if all possible tables are eliminated
-        elim_table = []
-        if len(temp) < 2:
-            for t in temp_table:
-                if t in self.input_table_dict.keys():
-                    if col_sql in self.input_table_dict[t]:
-                        return [t + "." + col_sql]
-                    else:
-                        elim_table.append(t)
-                elif t in self.cte_dict.keys():
-                    if col_sql in self.cte_dict[t].keys():
-                        return self.cte_dict[t][col_sql]
-                    else:
-                        elim_table.append(t)
-            deduced_table = set(temp_table) - set(elim_table)
-            if len(deduced_table) == 1:
-                return [deduced_table.pop() + "." + col_sql]
-        elif len(temp) == 2:
-            if temp[0] in self.table_alias_dict.keys():
-                t = self.table_alias_dict[temp[0]]
-            else:
-                t = temp[0]
-            if t in self.cte_dict.keys():
-                return self.cte_dict[t][temp[1]]
-            else:
-                return [t + "." + temp[1]]
-        return [col_sql]
-
-    def _resolve_agg_star(self, col_name: Optional[str] = "", projection: expressions = None, used_tables: Optional[List] = None):
-        """
-        Trying to resolve the * and append appropriate columns if the table is able to resolved
-        :param col_name: the name of the column
-        :param projection: the expression of the sql
-        :param used_tables: the tables that are used
-        """
-        if projection.find(exp.Star):
-            # * with a table name
-            if projection.find(exp.Identifier):
-                t_name = projection.find(exp.Identifier).text("this")
-                # Resolve alias
-                if t_name in self.table_alias_dict.keys():
-                    t_name = self.table_alias_dict[t_name]
-                if t_name in self.input_table_dict.keys():
-                    star_cols = []
-                    for s in self.input_table_dict[t_name]:
-                        star_cols.extend(self._find_alias_col(col_sql=s, temp_table=used_tables))
-                elif t_name in self.cte_dict.keys():
-                    star_cols = []
-                    for s in list(self.cte_dict[t_name].keys()):
-                        star_cols.extend(self._find_alias_col(col_sql=s, temp_table=used_tables))
-                else:
-                    star_cols = [t_name + ".*"]
-                self.column_dict[col_name] = sorted(list(set(star_cols).union(self.all_used_col)))
-            # only star, like count(*)
-            else:
-                self.column_dict[col_name] = sorted(list(self.all_used_col))
-
-
-if __name__ == "__main__":
-    pass
+from sqlglot import parse_one, exp
+from sqlglot import expressions
+from typing import Optional, List, Tuple
+import os
+
+shared_conditions = [exp.Where, exp.EQ, exp.Group, exp.Having, exp.Order]
+shared_conditions_with_table = [exp.Where, exp.EQ, exp.Group, exp.Having, exp.Order, exp.From, exp.Join]
+
+
+class ColumnLineageNoConn:
+    def __init__(self, sql: Optional[str] = "", input_table_dict: Optional[dict] = None):
+        self.column_dict = {}
+        self.table_alias_dict = {}
+        self.cte_table_dict = {}
+        self.cte_dict = {}
+        self.input_table_dict = input_table_dict
+        self.sql_ast = parse_one(sql, read="postgres")
+        self.all_used_col = []
+        self.table_list = []
+        self.all_subquery_table = []
+        self.sub_tables = []
+        self.sub_cols = []
+        self._run_cte_lineage()
+        # Everything other than CTEs, and pop the CTE tree
+        for with_sql in self.sql_ast.find_all(exp.With):
+            with_sql.pop()
+        self._sub_shared_col_conds(sql_ast=self.sql_ast)
+        self._run_lineage(self.sql_ast, False)
+        #print(self.cte_dict)
+        #print(self.column_dict)
+        #print(self.table_list)
+
+    def _run_lineage(self, sql_ast: expressions = None, subquery_flag: bool = False) -> None:
+        """
+        Run the lineage after all the cte and subquery are resolved
+        :param sql_ast: the ast for the sql
+        :param subquery_flag: check if it is a subquery
+        """
+        #print(sql_ast)
+        if not subquery_flag:
+            main_tables = self._resolve_table(part_ast=sql_ast)
+            self.table_list = self._find_all_tables(temp_table_list=main_tables)
+            self.table_list.extend(self.all_subquery_table)
+            self.all_used_col = []
+            self._shared_col_conds(part_ast=sql_ast, used_tables=main_tables)
+            self.all_used_col.extend(self.sub_cols)
+            if isinstance(sql_ast, exp.Union) or isinstance(sql_ast, exp.Except) or isinstance(sql_ast, exp.Intersect):
+                for col in sql_ast.find_all(exp.Column):
+                    self.all_used_col.extend(self._find_alias_col(col_sql=col.sql(), temp_table=main_tables))
+            self.all_used_col = set(self.all_used_col)
+            if sql_ast.find(exp.Select):
+                for projection in sql_ast.find(exp.Select).expressions:
+                    col_name = projection.alias_or_name
+                    self.column_dict = self._resolve_proj(projection=projection, col_name=col_name, target_dict=self.column_dict, source_table=main_tables)
+        else:
+            temp_sub_cols = []
+            for col in sql_ast.find_all(exp.Column):
+                temp_sub_cols.extend(self._find_alias_col(col_sql=col.sql(), temp_table=self.sub_tables))
+            self.sub_cols.extend(temp_sub_cols)
+            #print(temp_sub_cols)
+
+    def _sub_shared_col_conds(self, sql_ast: expressions = None) -> None:
+        """
+        After the cte are resolved, run the subquery ast that is with the shared conditions(WHERE, GROUP BY, etc)
+        :param sql_ast: the ast without the cte
+        """
+        # add in more conditions, including FROM/JOIN
+        for cond in shared_conditions_with_table:
+            for cond_sql in sql_ast.find_all(cond):
+                for sub_ast in cond_sql.find_all(exp.Subquery):
+                    self.sub_tables = self._resolve_table(part_ast=sub_ast)
+                    self.all_subquery_table.extend(self._find_all_tables(temp_table_list=self.sub_tables))
+                    self._run_lineage(sub_ast, True)
+                    sub_ast.pop()
+
+    def _sub_shared_col_conds_cte(self, sql_ast: expressions = None) -> Tuple[List, List]:
+        """
+        Run the subquery inside the cte first that is with the shared conditions(WHERE, GROUP BY, etc)
+        :param sql_ast: the ast for the cte
+        """
+        all_cte_sub_table = []
+        all_cte_sub_cols = []
+        # add in more conditions, including FROM/JOIN
+        for cond in shared_conditions_with_table:
+            for cond_sql in sql_ast.find_all(cond):
+                for sub_ast in cond_sql.find_all(exp.Select):
+                    temp_sub_table = self._resolve_table(part_ast=sub_ast)
+                    temp_sub_cols = []
+                    for col in sub_ast.find_all(exp.Column):
+                        temp_sub_cols.extend(self._find_alias_col(col_sql=col.sql(), temp_table=temp_sub_table))
+                    all_cte_sub_table.extend(self._find_all_tables(temp_table_list=temp_sub_table))
+                    all_cte_sub_cols.extend(temp_sub_cols)
+                    sub_ast.pop()
+        return all_cte_sub_table, all_cte_sub_cols
+
+    def _run_cte_lineage(self):
+        """
+        Run the lineage information for all the cte
+        """
+        for cte in self.sql_ast.find_all(exp.CTE):
+            all_cte_sub_table, all_cte_sub_cols = self._sub_shared_col_conds_cte(sql_ast=cte)
+            self.all_used_col = []
+            temp_cte_dict = {}
+            temp_cte_table = self._resolve_table(part_ast=cte)
+            cte_name = cte.find(exp.TableAlias).alias_or_name
+            self.cte_table_dict[cte_name] = list(set(self._find_all_tables(temp_table_list=temp_cte_table) + all_cte_sub_table))
+            # Resolving shared conditions
+            self._shared_col_conds(part_ast=cte, used_tables=temp_cte_table)
+            self.all_used_col.extend(all_cte_sub_cols)
+            self.all_used_col = set(self.all_used_col)
+            # Resolving the projection
+            for projection in cte.find(exp.Select).expressions:
+                col_name = projection.alias_or_name
+                temp_cte_dict = self._resolve_proj(projection=projection, col_name=col_name, target_dict=temp_cte_dict, source_table=temp_cte_table)
+            self.cte_dict[cte_name] = temp_cte_dict
+
+    def _resolve_proj(self, projection: expressions = None, col_name: Optional[str] = "", target_dict: Optional[dict] = None, source_table: Optional[List] = None) -> dict:
+        """
+        Resolve the projection given the projection expression
+        :param projection: the given projection
+        :param col_name: the column name
+        :param target_dict: the dict it is outputting to
+        :param source_table: all the source tables that this column might originate from
+        """
+        # Resolve count(*) with no alias, potentially other aggregations, MIN, MAX, SUM
+        if isinstance(projection, exp.Count) or isinstance(projection.unalias(), exp.Count)\
+                or isinstance(projection, exp.Avg) or isinstance(projection.unalias(), exp.Avg)\
+                or isinstance(projection, exp.Max) or isinstance(projection.unalias(), exp.Max)\
+                or isinstance(projection, exp.Min) or isinstance(projection.unalias(), exp.Min)\
+                or isinstance(projection, exp.Sum) or isinstance(projection.unalias(), exp.Sum):
+            if isinstance(projection, exp.Count):
+                col_name = "count"
+                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
+            elif isinstance(projection, exp.Avg):
+                col_name = "avg"
+                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
+            elif isinstance(projection, exp.Max):
+                col_name = "max"
+                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
+            elif isinstance(projection, exp.Min):
+                col_name = "min"
+                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
+            elif isinstance(projection, exp.Sum):
+                col_name = "sum"
+                self._resolve_agg_star(col_name=col_name, projection=projection, used_tables=source_table)
+            else:
+                self._resolve_agg_star(col_name=col_name, projection=projection.unalias(), used_tables=source_table)
+        else:
+            proj_columns = []
+            # Resolve only *
+            if not isinstance(projection, exp.Column) and projection.find(exp.Star):
+                for t_name in source_table:
+                    if t_name in self.input_table_dict.keys():
+                        star_cols = self.input_table_dict[t_name]
+                        # every column from there will be a column with that name
+                        for per_star_col in star_cols:
+                            target_dict[per_star_col] = sorted(
+                                list(set(self._find_alias_col(col_sql=per_star_col, temp_table=source_table)).union(
+                                    self.all_used_col)))
+                    elif t_name in self.cte_dict.keys():
+                        star_cols = list(self.cte_dict[t_name].keys())
+                        for per_star_col in star_cols:
+                            target_dict[per_star_col] = sorted(
+                                list(set(self.cte_dict[t_name][per_star_col]).union(self.all_used_col)))
+            # Resolve projections that have many columns, some of which could be *
+            for p in projection.find_all(exp.Column):
+                # Resolve * with other columns
+                if isinstance(p, exp.Column) and p.find(exp.Star):
+                    t_name = p.find(exp.Identifier).text("this")
+                    # Resolve alias
+                    if t_name in self.table_alias_dict.keys():
+                        t_name = self.table_alias_dict[t_name]
+                    # If from input table, get all columns from there
+                    if t_name in self.input_table_dict.keys():
+                        star_cols = self.input_table_dict[t_name]
+                        # every column from there will be a column with that name
+                        for per_star_col in star_cols:
+                            target_dict[per_star_col] = sorted(
+                                list(set(self._find_alias_col(col_sql=per_star_col, temp_table=source_table)).union(
+                                    self.all_used_col)))
+                    # If from another CTE, get all columns from there
+                    elif t_name in self.cte_dict.keys():
+                        star_cols = list(self.cte_dict[t_name].keys())
+                        for per_star_col in star_cols:
+                            target_dict[per_star_col] = sorted(
+                                list(set(self.cte_dict[t_name][per_star_col]).union(self.all_used_col)))
+                    # If from an unknown table, leave it with a STAR as temporary name
+                    else:
+                        target_dict[p.sql()] = [p.sql()] + (list(self.all_used_col))
+                else:
+                    # one projection can have many columns, append first
+                    proj_columns.extend(self._find_alias_col(col_sql=p.sql(), temp_table=source_table))
+            if proj_columns:
+                target_dict[col_name] = sorted(list(set(proj_columns).union(self.all_used_col)))
+        return target_dict
+
+    def _resolve_table(self, part_ast: expressions = None) -> List:
+        """
+        Find the tables in the given ast
+        :param part_ast: the ast to find the table
+        """
+        temp_table_list = []
+        # Resolve FROM
+        for table_sql in part_ast.find_all(exp.From):
+            for table in table_sql.find_all(exp.Table):
+                temp_table_list = self._find_table(table=table, temp_table_list=temp_table_list)
+        # Resolve JOIN
+        for table_sql in part_ast.find_all(exp.Join):
+            for table in table_sql.find_all(exp.Table):
+                temp_table_list = self._find_table(table=table, temp_table_list=temp_table_list)
+        return temp_table_list
+
+    def _find_table(self, table: expressions = None, temp_table_list: Optional[List] = None) -> List:
+        """
+        Update table alias and find all aliased used table names
+        :param table: the expression with the table
+        :param temp_table_list: temporary list of tables for appending the used tables
+        :return:
+        """
+        if table.alias == "":
+            self.table_alias_dict[table.sql()] = table.sql()
+            temp_table_list.append(table.sql())
+        else:
+            temp = table.sql().split(" ")
+            if temp[1] == "AS" or temp[1] == "as":
+                self.table_alias_dict[temp[2]] = temp[0]
+                temp_table_list.append(temp[0])
+        return temp_table_list
+
+    def _find_all_tables(self, temp_table_list: Optional[List] = None) -> List:
+        """
+        Update the used table names, such as if a CTE, update it with the dependant tables
+        :param temp_table_list: temporary list of tables for appending the used tables
+        :return:
+        """
+        ret_table = []
+        for i in temp_table_list:
+            table_name = i
+            if i in self.table_alias_dict.keys():
+                table_name = self.table_alias_dict[i]
+            if table_name in self.cte_table_dict.keys():
+                ret_table.extend(self.cte_table_dict[table_name])
+            else:
+                ret_table.append(table_name)
+        return ret_table
+
+    def _shared_col_conds(self, part_ast: expressions = None, used_tables: Optional[List] = None):
+        """
+        Extract all the columns in the shared conditions(WHERE, GROUP BY, etc)
+        :param part_ast: the ast of the sql to extract
+        :param used_tables: the tables that this sql uses
+        """
+        # COMBINE THE CONDITIONS
+        for cond in shared_conditions:
+            for cond_sql in part_ast.find_all(cond):
+                for cond_col in cond_sql.find_all(exp.Column):
+                    self.all_used_col.extend(self._find_alias_col(col_sql=cond_col.sql(), temp_table=used_tables))
+
+    def _find_alias_col(self, col_sql: Optional[str] = "", temp_table: Optional[List] = None) -> List:
+        """
+        Find the columns and its alias and dependencies if it is from a cte
+        :param col_sql: the sql to the column
+        :param temp_table: the table that the sql uses
+        :return:
+        """
+        temp = col_sql.split(".")
+        # trying to deduce the table if all possible tables are eliminated
+        elim_table = []
+        if len(temp) < 2:
+            for t in temp_table:
+                if t in self.input_table_dict.keys():
+                    if col_sql in self.input_table_dict[t]:
+                        return [t + "." + col_sql]
+                    else:
+                        elim_table.append(t)
+                elif t in self.cte_dict.keys():
+                    if col_sql in self.cte_dict[t].keys():
+                        return self.cte_dict[t][col_sql]
+                    else:
+                        elim_table.append(t)
+            deduced_table = set(temp_table) - set(elim_table)
+            if len(deduced_table) == 1:
+                return [deduced_table.pop() + "." + col_sql]
+        elif len(temp) == 2:
+            if temp[0] in self.table_alias_dict.keys():
+                t = self.table_alias_dict[temp[0]]
+            else:
+                t = temp[0]
+            if t in self.cte_dict.keys():
+                return self.cte_dict[t][temp[1]]
+            else:
+                return [t + "." + temp[1]]
+        return [col_sql]
+
+    def _resolve_agg_star(self, col_name: Optional[str] = "", projection: expressions = None, used_tables: Optional[List] = None):
+        """
+        Trying to resolve the * and append appropriate columns if the table is able to resolved
+        :param col_name: the name of the column
+        :param projection: the expression of the sql
+        :param used_tables: the tables that are used
+        """
+        if projection.find(exp.Star):
+            # * with a table name
+            if projection.find(exp.Identifier):
+                t_name = projection.find(exp.Identifier).text("this")
+                # Resolve alias
+                if t_name in self.table_alias_dict.keys():
+                    t_name = self.table_alias_dict[t_name]
+                if t_name in self.input_table_dict.keys():
+                    star_cols = []
+                    for s in self.input_table_dict[t_name]:
+                        star_cols.extend(self._find_alias_col(col_sql=s, temp_table=used_tables))
+                elif t_name in self.cte_dict.keys():
+                    star_cols = []
+                    for s in list(self.cte_dict[t_name].keys()):
+                        star_cols.extend(self._find_alias_col(col_sql=s, temp_table=used_tables))
+                else:
+                    star_cols = [t_name + ".*"]
+                self.column_dict[col_name] = sorted(list(set(star_cols).union(self.all_used_col)))
+            # only star, like count(*)
+            else:
+                self.column_dict[col_name] = sorted(list(self.all_used_col))
+
+
+if __name__ == "__main__":
+    pass
```

### Comparing `lineagex-0.0.1/lineagex/SqlToDict.py` & `lineagex-0.0.1a1/lineagex/SqlToDict.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,140 +1,141 @@
-import re
-import os
-from lineagex.utils import get_files, find_select, remove_comments
-from typing import List, Optional
-
-rem_regex = re.compile(r"[^a-zA-Z0-9_.]")
-
-
-class SqlToDict:
-    def __init__(self, path: Optional[str] = "", schema_list: Optional[List] = None) -> None:
-        self.path = path
-        self.schema_list = schema_list
-        self.sql_files = []
-        self.sql_files_dict = {}
-        self.deletion_dict = {}
-        self.insertion_dict = {}
-        self.curr_name = ""
-        self._sql_to_dict()
-        pass
-
-    def _sql_to_dict(self) -> None:
-        """
-        The driver function to make the input into the dict format, name of sql:sql
-        :return:
-        """
-        if isinstance(self.path, list):
-            for idx, val in enumerate(self.path):
-                self._preprocess_sql(org_sql=val, file=str(idx))
-        else:
-            self.sql_files = get_files(path=self.path)
-            for f in self.sql_files:
-                org_sql = open(f, mode="r", encoding="utf-8-sig").read()
-                org_sql = remove_comments(str1=org_sql)
-                org_sql_split = list(filter(None, org_sql.split(";")))
-                if len(org_sql_split) <= 1:
-                    self._preprocess_sql(org_sql=org_sql_split[0], file=f)
-                else:
-                    for idx, val in enumerate(org_sql_split):
-                        self._preprocess_sql(org_sql=val, file=f + "_" + str(idx))
-
-    def _preprocess_sql(self, org_sql: Optional[str] = "", file: Optional[str] = "") -> None:
-        """
-        Process the sql, remove database name in the clause/datetime_add/datetime_sub adding quotes
-        :param org_sql: the original sql, file: file name for the sql
-        :return: None
-        """
-        ret_sql = remove_comments(str1=org_sql)
-        ret_sql = ret_sql.replace("`", "")
-        # remove any database names in the query
-        if self.schema_list:
-            for i in self.schema_list:
-                ret_sql = re.sub("[^ (,]*(\.{}\.)".format(i), "{}.".format(i), ret_sql)
-        ret_sql = re.sub(
-            r"DATETIME_DIFF\((.+?),\s?(.+?),\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
-            r"DATETIME_DIFF(\1, \2, '\3'::TEXT)",
-            ret_sql,
-        )
-        ret_sql = re.sub("datetime_add", "DATETIME_ADD", ret_sql, flags=re.IGNORECASE)
-        ret_sql = re.sub("datetime_sub", "DATETIME_SUB", ret_sql, flags=re.IGNORECASE)
-        # DATETIME_ADD '' value
-        dateime_groups = re.findall(
-            r"DATETIME_ADD\(\s?(.+?),\s?INTERVAL\s?(.+?)\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
-            ret_sql,
-        )
-        if dateime_groups:
-            for i in dateime_groups:
-                if not i[1].startswith("'") and not i[1].endswith("'"):
-                    ret_sql = ret_sql.replace(
-                        "DATETIME_ADD({},INTERVAL {} {})".format(i[0], i[1], i[2]),
-                        "DATETIME_ADD({},INTERVAL '{}' {})".format(i[0], i[1], i[2]),
-                    )
-                else:
-                    continue
-        # DATETIME_SUB '' value
-        dateime_sub_groups = re.findall(
-            r"DATETIME_SUB\(\s?(.+?),\s?INTERVAL\s?(.+?)\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
-            ret_sql,
-        )
-        if dateime_sub_groups:
-            for i in dateime_sub_groups:
-                if not i[1].startswith("'") and not i[1].endswith("'"):
-                    ret_sql = ret_sql.replace(
-                        "DATETIME_SUB({},INTERVAL {} {})".format(i[0], i[1], i[2]),
-                        "DATETIME_SUB({},INTERVAL '{}' {})".format(i[0], i[1], i[2]),
-                    )
-                else:
-                    continue
-        if re.search(
-            "CREATE VIEW IF NOT EXISTS", ret_sql, flags=re.IGNORECASE
-        ) or re.search("CREATE TABLE IF NOT EXISTS", ret_sql, flags=re.IGNORECASE):
-            temp = ret_sql.split(" ")
-            ret_sql = ret_sql[ret_sql.index(temp[7]) :]
-            if temp[5] in self.sql_files_dict.keys():
-                print("WARNING: duplicate script detected for {}".format(temp[5]))
-            self.sql_files_dict[temp[5]] = ret_sql
-        elif re.search("CREATE VIEW", ret_sql, flags=re.IGNORECASE) or re.search(
-            "CREATE TABLE", ret_sql, flags=re.IGNORECASE
-        ):
-            temp = ret_sql.split(" ")
-            ret_sql = ret_sql[ret_sql.index(temp[4]) :]
-            if temp[2] in self.sql_files_dict.keys():
-                print("WARNING: duplicate script detected for {}".format(temp[2]))
-            self.sql_files_dict[temp[2]] = ret_sql
-        # adjust to INSERT/DELETE/SELECT/
-        elif ret_sql.find("INSERT INTO") != -1:
-            # find the current name in the insertion dict and how many times it has been inserted
-            self.curr_name = re.sub(rem_regex, "", ret_sql.split(" ")[2])
-            if self.curr_name not in self.insertion_dict.keys():
-                self.insertion_dict[self.curr_name] = 1
-            else:
-                self.insertion_dict[self.curr_name] = (
-                    self.insertion_dict[self.curr_name] + 1
-                )
-            insert_counter = self.insertion_dict[self.curr_name]
-            self.curr_name = self.curr_name + "_INSERTION_{}".format(insert_counter)
-            self.sql_files_dict[self.curr_name] = find_select(q=ret_sql)
-        elif ret_sql.find("DELETE FROM") != -1:
-            # find the current name in the insertion dict and how many times it has been deleted
-            self.curr_name = re.sub(rem_regex, "", ret_sql.split(" ")[2])
-            if self.curr_name not in self.deletion_dict.keys():
-                self.deletion_dict[self.curr_name] = 1
-            else:
-                self.deletion_dict[self.curr_name] = (
-                    self.deletion_dict[self.curr_name] + 1
-                )
-            delete_counter = self.deletion_dict[self.curr_name]
-            self.curr_name = self.curr_name + "_DELETION_{}".format(delete_counter)
-            self.sql_files_dict[self.curr_name] = find_select(q=ret_sql)
-        else:
-            if os.path.isfile(file):
-                name = os.path.basename(file)[:-4]
-                if name in self.sql_files_dict.keys():
-                    print("WARNING: duplicate script detected for {}".format(name))
-                self.sql_files_dict[name] = ret_sql
-            else:
-                self.sql_files_dict[file] = ret_sql
-
-
-if __name__ == "__main__":
-    pass
+import re
+import os
+from typing import List, Optional
+
+from .utils import get_files, find_select, remove_comments
+
+rem_regex = re.compile(r"[^a-zA-Z0-9_.]")
+
+
+class SqlToDict:
+    def __init__(self, path: Optional[str] = "", schema_list: Optional[List] = None) -> None:
+        self.path = path
+        self.schema_list = schema_list
+        self.sql_files = []
+        self.sql_files_dict = {}
+        self.deletion_dict = {}
+        self.insertion_dict = {}
+        self.curr_name = ""
+        self._sql_to_dict()
+        pass
+
+    def _sql_to_dict(self) -> None:
+        """
+        The driver function to make the input into the dict format, name of sql:sql
+        :return:
+        """
+        if isinstance(self.path, list):
+            for idx, val in enumerate(self.path):
+                self._preprocess_sql(org_sql=val, file=str(idx))
+        else:
+            self.sql_files = get_files(path=self.path)
+            for f in self.sql_files:
+                org_sql = open(f, mode="r", encoding="utf-8-sig").read()
+                org_sql = remove_comments(str1=org_sql)
+                org_sql_split = list(filter(None, org_sql.split(";")))
+                if len(org_sql_split) <= 1:
+                    self._preprocess_sql(org_sql=org_sql_split[0], file=f)
+                else:
+                    for idx, val in enumerate(org_sql_split):
+                        self._preprocess_sql(org_sql=val, file=f + "_" + str(idx))
+
+    def _preprocess_sql(self, org_sql: Optional[str] = "", file: Optional[str] = "") -> None:
+        """
+        Process the sql, remove database name in the clause/datetime_add/datetime_sub adding quotes
+        :param org_sql: the original sql, file: file name for the sql
+        :return: None
+        """
+        ret_sql = remove_comments(str1=org_sql)
+        ret_sql = ret_sql.replace("`", "")
+        # remove any database names in the query
+        if self.schema_list:
+            for i in self.schema_list:
+                ret_sql = re.sub("[^ (,]*(\.{}\.)".format(i), "{}.".format(i), ret_sql)
+        ret_sql = re.sub(
+            r"DATETIME_DIFF\((.+?),\s?(.+?),\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
+            r"DATETIME_DIFF(\1, \2, '\3'::TEXT)",
+            ret_sql,
+        )
+        ret_sql = re.sub("datetime_add", "DATETIME_ADD", ret_sql, flags=re.IGNORECASE)
+        ret_sql = re.sub("datetime_sub", "DATETIME_SUB", ret_sql, flags=re.IGNORECASE)
+        # DATETIME_ADD '' value
+        dateime_groups = re.findall(
+            r"DATETIME_ADD\(\s?(.+?),\s?INTERVAL\s?(.+?)\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
+            ret_sql,
+        )
+        if dateime_groups:
+            for i in dateime_groups:
+                if not i[1].startswith("'") and not i[1].endswith("'"):
+                    ret_sql = ret_sql.replace(
+                        "DATETIME_ADD({},INTERVAL {} {})".format(i[0], i[1], i[2]),
+                        "DATETIME_ADD({},INTERVAL '{}' {})".format(i[0], i[1], i[2]),
+                    )
+                else:
+                    continue
+        # DATETIME_SUB '' value
+        dateime_sub_groups = re.findall(
+            r"DATETIME_SUB\(\s?(.+?),\s?INTERVAL\s?(.+?)\s?(DAY|MINUTE|SECOND|HOUR|YEAR)\)",
+            ret_sql,
+        )
+        if dateime_sub_groups:
+            for i in dateime_sub_groups:
+                if not i[1].startswith("'") and not i[1].endswith("'"):
+                    ret_sql = ret_sql.replace(
+                        "DATETIME_SUB({},INTERVAL {} {})".format(i[0], i[1], i[2]),
+                        "DATETIME_SUB({},INTERVAL '{}' {})".format(i[0], i[1], i[2]),
+                    )
+                else:
+                    continue
+        if re.search(
+            "CREATE VIEW IF NOT EXISTS", ret_sql, flags=re.IGNORECASE
+        ) or re.search("CREATE TABLE IF NOT EXISTS", ret_sql, flags=re.IGNORECASE):
+            temp = ret_sql.split(" ")
+            ret_sql = ret_sql[ret_sql.index(temp[7]) :]
+            if temp[5] in self.sql_files_dict.keys():
+                print("WARNING: duplicate script detected for {}".format(temp[5]))
+            self.sql_files_dict[temp[5]] = ret_sql
+        elif re.search("CREATE VIEW", ret_sql, flags=re.IGNORECASE) or re.search(
+            "CREATE TABLE", ret_sql, flags=re.IGNORECASE
+        ):
+            temp = ret_sql.split(" ")
+            ret_sql = ret_sql[ret_sql.index(temp[4]) :]
+            if temp[2] in self.sql_files_dict.keys():
+                print("WARNING: duplicate script detected for {}".format(temp[2]))
+            self.sql_files_dict[temp[2]] = ret_sql
+        # adjust to INSERT/DELETE/SELECT/
+        elif ret_sql.find("INSERT INTO") != -1:
+            # find the current name in the insertion dict and how many times it has been inserted
+            self.curr_name = re.sub(rem_regex, "", ret_sql.split(" ")[2])
+            if self.curr_name not in self.insertion_dict.keys():
+                self.insertion_dict[self.curr_name] = 1
+            else:
+                self.insertion_dict[self.curr_name] = (
+                    self.insertion_dict[self.curr_name] + 1
+                )
+            insert_counter = self.insertion_dict[self.curr_name]
+            self.curr_name = self.curr_name + "_INSERTION_{}".format(insert_counter)
+            self.sql_files_dict[self.curr_name] = find_select(q=ret_sql)
+        elif ret_sql.find("DELETE FROM") != -1:
+            # find the current name in the insertion dict and how many times it has been deleted
+            self.curr_name = re.sub(rem_regex, "", ret_sql.split(" ")[2])
+            if self.curr_name not in self.deletion_dict.keys():
+                self.deletion_dict[self.curr_name] = 1
+            else:
+                self.deletion_dict[self.curr_name] = (
+                    self.deletion_dict[self.curr_name] + 1
+                )
+            delete_counter = self.deletion_dict[self.curr_name]
+            self.curr_name = self.curr_name + "_DELETION_{}".format(delete_counter)
+            self.sql_files_dict[self.curr_name] = find_select(q=ret_sql)
+        else:
+            if os.path.isfile(file):
+                name = os.path.basename(file)[:-4]
+                if name in self.sql_files_dict.keys():
+                    print("WARNING: duplicate script detected for {}".format(name))
+                self.sql_files_dict[name] = ret_sql
+            else:
+                self.sql_files_dict[file] = ret_sql
+
+
+if __name__ == "__main__":
+    pass
```

### Comparing `lineagex-0.0.1/lineagex/app.js` & `lineagex-0.0.1a1/lineagex/app.js`

 * *Files identical despite different names*

### Comparing `lineagex-0.0.1/lineagex/stack.py` & `lineagex-0.0.1a1/lineagex/stack.py`

 * *Ordering differences only*

 * *Files 27% similar despite different names*

```diff
@@ -1,56 +1,56 @@
-class Node:
-    def __init__(self, value):
-        self.value = value
-        self.next = None
-
-
-class Stack:
-
-    # Initializing a stack.
-    # Use a dummy node, which is
-    # easier for handling edge cases.
-    def __init__(self):
-        self.head = Node("head")
-        self.size = 0
-
-    # String representation of the stack
-    def __str__(self):
-        cur = self.head.next
-        out = ""
-        while cur:
-            out += str(cur.value) + "->"
-            cur = cur.next
-        return out[:-3]
-
-    # Get the current size of the stack
-    def getSize(self):
-        return self.size
-
-    # Check if the stack is empty
-    def isEmpty(self):
-        return self.size == 0
-
-    # Get the top item of the stack
-    def peek(self):
-
-        # Sanitary check to see if we
-        # are peeking an empty stack.
-        if self.isEmpty():
-            raise Exception("Peeking from an empty stack")
-        return self.head.next.value
-
-    # Push a value into the stack.
-    def push(self, value):
-        node = Node(value)
-        node.next = self.head.next
-        self.head.next = node
-        self.size += 1
-
-    # Remove a value from the stack and return.
-    def pop(self):
-        if self.isEmpty():
-            raise Exception("Popping from an empty stack")
-        remove = self.head.next
-        self.head.next = self.head.next.next
-        self.size -= 1
-        return remove.value
+class Node:
+    def __init__(self, value):
+        self.value = value
+        self.next = None
+
+
+class Stack:
+
+    # Initializing a stack.
+    # Use a dummy node, which is
+    # easier for handling edge cases.
+    def __init__(self):
+        self.head = Node("head")
+        self.size = 0
+
+    # String representation of the stack
+    def __str__(self):
+        cur = self.head.next
+        out = ""
+        while cur:
+            out += str(cur.value) + "->"
+            cur = cur.next
+        return out[:-3]
+
+    # Get the current size of the stack
+    def getSize(self):
+        return self.size
+
+    # Check if the stack is empty
+    def isEmpty(self):
+        return self.size == 0
+
+    # Get the top item of the stack
+    def peek(self):
+
+        # Sanitary check to see if we
+        # are peeking an empty stack.
+        if self.isEmpty():
+            raise Exception("Peeking from an empty stack")
+        return self.head.next.value
+
+    # Push a value into the stack.
+    def push(self, value):
+        node = Node(value)
+        node.next = self.head.next
+        self.head.next = node
+        self.size += 1
+
+    # Remove a value from the stack and return.
+    def pop(self):
+        if self.isEmpty():
+            raise Exception("Popping from an empty stack")
+        remove = self.head.next
+        self.head.next = self.head.next.next
+        self.size -= 1
+        return remove.value
```

### Comparing `lineagex-0.0.1/lineagex/vendor.js` & `lineagex-0.0.1a1/lineagex/vendor.js`

 * *Files identical despite different names*

