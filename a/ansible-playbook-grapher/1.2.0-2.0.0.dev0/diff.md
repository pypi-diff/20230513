# Comparing `tmp/ansible_playbook_grapher-1.2.0-py2.py3-none-any.whl.zip` & `tmp/ansible_playbook_grapher-2.0.0.dev0-py2.py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,17 +1,19 @@
-Zip file size: 41346 bytes, number of entries: 15
--rw-r--r--  2.0 unx      878 b- defN 22-Aug-21 14:59 ansibleplaybookgrapher/__init__.py
--rw-r--r--  2.0 unx     9996 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/cli.py
--rw-r--r--  2.0 unx    12095 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/graph.py
--rw-r--r--  2.0 unx    17131 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/graphbuilder.py
--rw-r--r--  2.0 unx    19619 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/parser.py
--rw-r--r--  2.0 unx     7391 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/postprocessor.py
--rw-r--r--  2.0 unx     6984 b- defN 22-Aug-20 12:50 ansibleplaybookgrapher/utils.py
--rw-r--r--  2.0 unx      358 b- defN 22-Jun-23 20:59 ansibleplaybookgrapher/data/graph.css
--rw-r--r--  2.0 unx     5458 b- defN 22-Aug-21 14:57 ansibleplaybookgrapher/data/highlight-hover.js
--rw-r--r--  2.0 unx    35148 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/LICENSE
--rw-r--r--  2.0 unx    10799 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/METADATA
--rw-r--r--  2.0 unx      110 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/WHEEL
--rw-r--r--  2.0 unx       78 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       23 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1417 b- defN 22-Aug-21 15:04 ansible_playbook_grapher-1.2.0.dist-info/RECORD
-15 files, 127485 bytes uncompressed, 38948 bytes compressed:  69.4%
+Zip file size: 50233 bytes, number of entries: 17
+-rw-r--r--  2.0 unx     2831 b- defN 23-May-13 12:42 ansibleplaybookgrapher/__init__.py
+-rw-r--r--  2.0 unx    11280 b- defN 23-May-13 12:42 ansibleplaybookgrapher/cli.py
+-rw-r--r--  2.0 unx    13757 b- defN 23-May-13 16:23 ansibleplaybookgrapher/graph_model.py
+-rw-r--r--  2.0 unx    19656 b- defN 23-May-13 12:42 ansibleplaybookgrapher/parser.py
+-rw-r--r--  2.0 unx     7014 b- defN 23-May-11 14:42 ansibleplaybookgrapher/utils.py
+-rw-r--r--  2.0 unx      358 b- defN 23-May-11 14:42 ansibleplaybookgrapher/data/graph.css
+-rw-r--r--  2.0 unx     5458 b- defN 23-May-11 14:42 ansibleplaybookgrapher/data/highlight-hover.js
+-rw-r--r--  2.0 unx     8189 b- defN 23-May-13 12:42 ansibleplaybookgrapher/renderer/__init__.py
+-rw-r--r--  2.0 unx    11247 b- defN 23-May-13 16:22 ansibleplaybookgrapher/renderer/mermaid.py
+-rw-r--r--  2.0 unx    11051 b- defN 23-May-13 12:42 ansibleplaybookgrapher/renderer/graphviz/__init__.py
+-rw-r--r--  2.0 unx     7367 b- defN 23-May-13 12:42 ansibleplaybookgrapher/renderer/graphviz/postprocessor.py
+-rw-r--r--  2.0 unx    35148 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/LICENSE
+-rw-r--r--  2.0 unx    27853 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/METADATA
+-rw-r--r--  2.0 unx      110 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/WHEEL
+-rw-r--r--  2.0 unx       77 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       23 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     1687 b- defN 23-May-13 19:56 ansible_playbook_grapher-2.0.0.dev0.dist-info/RECORD
+17 files, 163106 bytes uncompressed, 47377 bytes compressed:  71.0%
```

## zipnote {}

```diff
@@ -1,46 +1,52 @@
 Filename: ansibleplaybookgrapher/__init__.py
 Comment: 
 
 Filename: ansibleplaybookgrapher/cli.py
 Comment: 
 
-Filename: ansibleplaybookgrapher/graph.py
-Comment: 
-
-Filename: ansibleplaybookgrapher/graphbuilder.py
+Filename: ansibleplaybookgrapher/graph_model.py
 Comment: 
 
 Filename: ansibleplaybookgrapher/parser.py
 Comment: 
 
-Filename: ansibleplaybookgrapher/postprocessor.py
-Comment: 
-
 Filename: ansibleplaybookgrapher/utils.py
 Comment: 
 
 Filename: ansibleplaybookgrapher/data/graph.css
 Comment: 
 
 Filename: ansibleplaybookgrapher/data/highlight-hover.js
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/LICENSE
+Filename: ansibleplaybookgrapher/renderer/__init__.py
+Comment: 
+
+Filename: ansibleplaybookgrapher/renderer/mermaid.py
+Comment: 
+
+Filename: ansibleplaybookgrapher/renderer/graphviz/__init__.py
+Comment: 
+
+Filename: ansibleplaybookgrapher/renderer/graphviz/postprocessor.py
+Comment: 
+
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/LICENSE
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/METADATA
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/METADATA
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/WHEEL
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/WHEEL
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/entry_points.txt
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/entry_points.txt
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/top_level.txt
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/top_level.txt
 Comment: 
 
-Filename: ansible_playbook_grapher-1.2.0.dist-info/RECORD
+Filename: ansible_playbook_grapher-2.0.0.dev0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## ansibleplaybookgrapher/__init__.py

```diff
@@ -1,21 +1,76 @@
-# Copyright (C) 2022 Mohamed El Mouctar HAIDARA
+# Copyright (C) 2023 Mohamed El Mouctar HAIDARA
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
 # but WITHOUT ANY WARRANTY; without even the implied warranty of
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <https://www.gnu.org/licenses/>.
 
+from typing import Dict, List, Set, Tuple
+
+from ansible.utils.display import Display
+
+from ansibleplaybookgrapher.graph_model import (
+    PlaybookNode,
+    RoleNode,
+    PlayNode,
+)
+from ansibleplaybookgrapher.parser import PlaybookParser
+from ansibleplaybookgrapher.utils import merge_dicts
+from .graph_model import PlaybookNode, PlayNode, TaskNode, RoleNode, BlockNode
 from .parser import PlaybookParser
-from .postprocessor import GraphVizPostProcessor
-from .graphbuilder import GraphvizGraphBuilder
 
-__version__ = "1.2.0"
+__version__ = "2.0.0-dev"
 __prog__ = "ansible-playbook-grapher"
+
+display = Display()
+
+
+class Grapher:
+    def __init__(self, playbook_filenames: List[str]):
+        """
+        :param playbook_filenames: List of playbooks to graph
+        """
+        self.playbook_filenames = playbook_filenames
+
+    def parse(
+        self,
+        include_role_tasks: bool = False,
+        tags: List[str] = None,
+        skip_tags: List[str] = None,
+        group_roles_by_name: bool = False,
+    ) -> Tuple[List[PlaybookNode], Dict[RoleNode, Set[PlayNode]]]:
+        """
+        Parses all the provided playbooks
+        :param include_role_tasks: Should we include the role tasks
+        :param tags: Only add plays and tasks tagged with these values
+        :param skip_tags: Only add plays and tasks whose tags do not match these values
+        :param group_roles_by_name: Group roles by name instead of considering them as separate nodes with different IDs
+        :return:
+        """
+        playbook_nodes = []
+        roles_usage: Dict[RoleNode, Set[PlayNode]] = {}
+
+        for playbook_file in self.playbook_filenames:
+            display.display(f"Parsing playbook {playbook_file}")
+            playbook_parser = PlaybookParser(
+                playbook_filename=playbook_file,
+                tags=tags,
+                skip_tags=skip_tags,
+                include_role_tasks=include_role_tasks,
+                group_roles_by_name=group_roles_by_name,
+            )
+            playbook_node = playbook_parser.parse()
+            playbook_nodes.append(playbook_node)
+
+            # Update the usage of the roles
+            roles_usage = merge_dicts(roles_usage, playbook_node.roles_usage())
+
+        return playbook_nodes, roles_usage
```

## ansibleplaybookgrapher/cli.py

```diff
@@ -1,8 +1,8 @@
-# Copyright (C) 2022 Mohamed El Mouctar HAIDARA
+# Copyright (C) 2023 Mohamed El Mouctar HAIDARA
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -12,102 +12,90 @@
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <https://www.gnu.org/licenses/>.
 import json
 import ntpath
 import os
 import sys
-from abc import ABC
 
 from ansible.cli import CLI
 from ansible.cli.arguments import option_helpers
 from ansible.errors import AnsibleOptionsError
 from ansible.release import __version__ as ansible_version
-from ansible.utils.display import Display, initialize_locale
+from ansible.utils.display import Display
 
-from ansibleplaybookgrapher import __prog__, __version__
-from ansibleplaybookgrapher.graphbuilder import (
-    OPEN_PROTOCOL_HANDLERS,
-    Grapher,
+from ansibleplaybookgrapher import __prog__, __version__, Grapher
+from ansibleplaybookgrapher.renderer import OPEN_PROTOCOL_HANDLERS
+from ansibleplaybookgrapher.renderer.graphviz import GraphvizRenderer
+from ansibleplaybookgrapher.renderer.mermaid import (
+    MermaidFlowChartRenderer,
+    DEFAULT_DIRECTIVE as MERMAID_DEFAULT_DIRECTIVE,
+    DEFAULT_ORIENTATION as MERMAID_DEFAULT_ORIENTATION,
 )
-from ansibleplaybookgrapher.postprocessor import GraphVizPostProcessor
 
 # The display is a singleton. This instruction will NOT return a new instance.
 # We explicitly set the verbosity after the init.
-
 display = Display()
 
 
-def get_cli_class():
+class PlaybookGrapherCLI(CLI):
     """
-    Utility function to return the class to use as CLI
-    :return:
+    The dedicated playbook grapher CLI
     """
 
-    return PlaybookGrapherCLI
-
+    name = __prog__
 
-class GrapherCLI(CLI, ABC):
-    """
-    An abstract class to be implemented by the different Grapher CLIs.
-    """
+    def __init__(self, args, callback=None):
+        super().__init__(args=args, callback=callback)
+        # We keep the old options as instance attribute for backward compatibility for the grapher CLI.
+        # From Ansible 2.8, they remove this instance attribute 'options' and use a global context instead.
+        # But this may change in the future:
+        # https://github.com/ansible/ansible/blob/bcb64054edaa7cf636bd38b8ab0259f6fb93f3f9/lib/ansible/context.py#L8
+        self.options = None
 
     def run(self):
         super().run()
 
-        # Required to fix the warning "ansible.utils.display.initialize_locale has not been called..."
-        initialize_locale()
         display.verbosity = self.options.verbosity
         grapher = Grapher(self.options.playbook_filenames)
-        grapher.parse(
+        playbook_nodes, roles_usage = grapher.parse(
             include_role_tasks=self.options.include_role_tasks,
             tags=self.options.tags,
             skip_tags=self.options.skip_tags,
             group_roles_by_name=self.options.group_roles_by_name,
         )
-        digraph = grapher.graph(
-            open_protocol_handler=self.options.open_protocol_handler,
-            open_protocol_custom_formats=self.options.open_protocol_custom_formats,
-        )
-
-        display.display("Rendering the graph...")
-        svg_path = digraph.render(
-            cleanup=not self.options.save_dot_file,
-            format="svg",
-            filename=self.options.output_filename,
-            view=self.options.view,
-        )
-
-        post_processor = GraphVizPostProcessor(svg_path=svg_path)
-        display.v("Post processing the SVG...")
-        post_processor.post_process(grapher.playbook_nodes)
-        post_processor.write()
-
-        display.display(f"The graph has been exported to {svg_path}", color="green")
-        if self.options.save_dot_file:
-            # add .dot extension. The render doesn't add an extension
-            final_name = self.options.output_filename + ".dot"
-            os.rename(self.options.output_filename, final_name)
-            display.display(f"Graphviz dot file has been exported to {final_name}")
 
-        return svg_path
-
-
-class PlaybookGrapherCLI(GrapherCLI):
-    """
-    The dedicated playbook grapher CLI
-    """
+        if self.options.renderer == "graphviz":
+            renderer = GraphvizRenderer(
+                playbook_nodes=playbook_nodes,
+                roles_usage=roles_usage,
+            )
+            output_path = renderer.render(
+                open_protocol_handler=self.options.open_protocol_handler,
+                open_protocol_custom_formats=self.options.open_protocol_custom_formats,
+                output_filename=self.options.output_filename,
+                view=self.options.view,
+                save_dot_file=self.options.save_dot_file,
+            )
 
-    def __init__(self, args, callback=None):
-        super().__init__(args=args, callback=callback)
-        # We keep the old options as instance attribute for backward compatibility for the grapher CLI.
-        # From Ansible 2.8, they remove this instance attribute 'options' and use a global context instead.
-        # But this may change in the future:
-        # https://github.com/ansible/ansible/blob/bcb64054edaa7cf636bd38b8ab0259f6fb93f3f9/lib/ansible/context.py#L8
-        self.options = None
+            return output_path
+        else:
+            renderer = MermaidFlowChartRenderer(
+                playbook_nodes=playbook_nodes,
+                roles_usage=roles_usage,
+            )
+            output_path = renderer.render(
+                open_protocol_handler=self.options.open_protocol_handler,
+                open_protocol_custom_formats=self.options.open_protocol_custom_formats,
+                output_filename=self.options.output_filename,
+                view=self.options.view,
+                directive=self.options.renderer_mermaid_directive,
+                orientation=self.options.renderer_mermaid_orientation,
+            )
+            return output_path
 
     def _add_my_options(self):
         """
         Add some of my options to the parser
         :return:
         """
         self.parser.prog = __prog__
@@ -130,15 +118,15 @@
 
         self.parser.add_argument(
             "-s",
             "--save-dot-file",
             dest="save_dot_file",
             action="store_true",
             default=False,
-            help="Save the dot file used to generate the graph.",
+            help="Save the graphviz dot file used to generate the graph.",
         )
 
         self.parser.add_argument(
             "--view",
             action="store_true",
             default=False,
             help="Automatically open the resulting SVG file with your system’s default viewer application for the file type",
@@ -170,24 +158,48 @@
             "--open-protocol-custom-formats",
             dest="open_protocol_custom_formats",
             default=None,
             help="""The custom formats to use as URLs for the nodes in the graph. Required if
                                  --open-protocol-handler is set to custom.
                                  You should provide a JSON formatted string like: {"file": "", "folder": ""}.
                                  Example: If you want to open folders (roles) inside the browser and files (tasks) in
-                                 vscode, set this to 
-                                 '{"file": "vscode://file/{path}:{line}:{column}", "folder": "{path}"}'
+                                 vscode, set it to: 
+                                 '{"file": "vscode://file/{path}:{line}:{column}", "folder": "{path}"}'.
+                                  path: the absolute path to the file containing the the plays/tasks/roles.
+                                  line/column: the position of the plays/tasks/roles in the file.  
+                                  You can optionally add the attribute "remove_from_path" to remove some parts of the 
+                                  path if you want relative paths. 
                                  """,
         )
 
         self.parser.add_argument(
             "--group-roles-by-name",
             action="store_true",
             default=False,
-            help="When rendering the graph, only a single role will be display for all roles having the same names.",
+            help="When rendering the graph, only a single role will be display for all roles having the same names. Default: %(default)s",
+        )
+
+        self.parser.add_argument(
+            "--renderer",
+            choices=["graphviz", "mermaid-flowchart"],
+            default="graphviz",
+            help="The renderer to use to generate the graph. Default: %(default)s",
+        )
+
+        self.parser.add_argument(
+            "--renderer-mermaid-directive",
+            default=MERMAID_DEFAULT_DIRECTIVE,
+            help="The directive for the mermaid renderer. Can be used to customize the output: fonts, theme, curve etc. More info at https://mermaid.js.org/config/directives.html. Default: '%(default)s'",
+        )
+
+        self.parser.add_argument(
+            "--renderer-mermaid-orientation",
+            default=MERMAID_DEFAULT_ORIENTATION,
+            choices=["TD", "RL", "BT", "RL", "LR"],
+            help="The orientation of the flow chart. Default: '%(default)s'",
         )
 
         self.parser.add_argument(
             "--version",
             action="version",
             version=f"{__prog__} {__version__} (with ansible {ansible_version})",
         )
@@ -216,18 +228,19 @@
     def post_process_args(self, options):
         options = super().post_process_args(options)
 
         # init the options
         self.options = options
 
         if self.options.output_filename is None:
-            # use the first playbook name (without the extension) as output filename
-            self.options.output_filename = os.path.splitext(
-                ntpath.basename(self.options.playbook_filenames[0])
-            )[0]
+            basenames = map(ntpath.basename, self.options.playbook_filenames)
+            basenames_without_ext = "-".join(
+                [os.path.splitext(basename)[0] for basename in basenames]
+            )
+            self.options.output_filename = basenames_without_ext
 
         if self.options.open_protocol_handler == "custom":
             self.validate_open_protocol_custom_formats()
 
         return options
 
     def validate_open_protocol_custom_formats(self):
@@ -260,14 +273,14 @@
 
         # Replace the string with a dict
         self.options.open_protocol_custom_formats = format_dict
 
 
 def main(args=None):
     args = args or sys.argv
-    cli = get_cli_class()(args)
+    cli = PlaybookGrapherCLI(args)
 
     cli.run()
 
 
 if __name__ == "__main__":
     main(sys.argv)
```

## ansibleplaybookgrapher/parser.py

```diff
@@ -1,8 +1,8 @@
-# Copyright (C) 2022 Mohamed El Mouctar HAIDARA
+# Copyright (C) 2023 Mohamed El Mouctar HAIDARA
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -23,15 +23,15 @@
 from ansible.playbook.helpers import load_list_of_blocks
 from ansible.playbook.role_include import IncludeRole
 from ansible.playbook.task import Task
 from ansible.playbook.task_include import TaskInclude
 from ansible.template import Templar
 from ansible.utils.display import Display
 
-from ansibleplaybookgrapher.graph import (
+from ansibleplaybookgrapher.graph_model import (
     TaskNode,
     PlaybookNode,
     RoleNode,
     PlayNode,
     CompositeNode,
     BlockNode,
 )
@@ -171,15 +171,14 @@
             loader=self.data_loader,
             variable_manager=self.variable_manager,
         )
         # the root node
         playbook_root_node = PlaybookNode(self.playbook_filename, raw_object=playbook)
         # loop through the plays
         for play in playbook.get_plays():
-
             # the load basedir is relative to the playbook path
             if play._included_path is not None:
                 self.data_loader.set_basedir(play._included_path)
             else:
                 self.data_loader.set_basedir(playbook._basedir)
             display.vvv(f"Loader basedir set to {self.data_loader.get_basedir()}")
 
@@ -191,15 +190,17 @@
                 )
             ]
             play_name = f"Play: {clean_name(play.get_name())} ({len(play_hosts)})"
             play_name = self.template(play_name, play_vars)
 
             display.v(f"Parsing {play_name}")
 
-            play_node = PlayNode(play_name, hosts=play_hosts, raw_object=play)
+            play_node = PlayNode(
+                play_name, hosts=play_hosts, raw_object=play, parent=playbook_root_node
+            )
             playbook_root_node.add_node("plays", play_node)
 
             # loop through the pre_tasks
             display.v("Parsing pre_tasks...")
             for pre_task_block in play.pre_tasks:
                 self._include_tasks_in_blocks(
                     current_play=play,
@@ -313,19 +314,17 @@
                 parent=parent_nodes[-1],
             )
             parent_nodes[-1].add_node(f"{node_type}s", block_node)
             parent_nodes.append(block_node)
 
         # loop through the tasks
         for task_or_block in block.block:
-
             if hasattr(task_or_block, "loop") and task_or_block.loop:
                 display.warning(
-                    "Looping on tasks or roles are not supported for the moment. "
-                    f"Only the task having the loop argument will be added to the graph."
+                    "Looping on tasks or roles are not supported for the moment. Only the task having the loop argument will be added to the graph."
                 )
 
             if isinstance(task_or_block, Block):
                 self._include_tasks_in_blocks(
                     current_play=current_play,
                     parent_nodes=parent_nodes,
                     block=task_or_block,
```

## ansibleplaybookgrapher/utils.py

```diff
@@ -84,15 +84,15 @@
     return name.strip().replace('"', "&#34;")
 
 
 def get_play_colors(play_id: str) -> Tuple[str, str]:
     """
     Generate two colors (in hex) for a given play: the main color and the color to use as a font color
     :param play_id
-    :return:
+    :return: The main color and the font color
     """
     picked_color = Color(pick_for=play_id, luminance=0.4)
     play_font_color = "#ffffff"
 
     return picked_color.get_hex_l(), play_font_color
 
 
@@ -107,26 +107,26 @@
         if parent._role:
             return True
         parent = parent._parent
 
     return False
 
 
-def merge_dicts(dict_1: Dict[Any, List], dict_2: Dict[Any, List]) -> Dict[Any, List]:
+def merge_dicts(dict_1: Dict[Any, Set], dict_2: Dict[Any, Set]) -> Dict[Any, Set]:
     """
     Merge two dicts by grouping keys and appending values in list
     :param dict_1:
     :param dict_2:
     :return:
     """
-    final = defaultdict(list)
+    final = defaultdict(set)
     # iterate dict items
     all_dict_items = map(methodcaller("items"), [dict_1, dict_2])
     for k, v in chain.from_iterable(all_dict_items):
-        final[k].extend(v)
+        final[k].update(v)
 
     return final
 
 
 def handle_include_path(
     original_task: TaskInclude, loader: DataLoader, templar: Templar
 ) -> str:
```

## Comparing `ansibleplaybookgrapher/graph.py` & `ansibleplaybookgrapher/graph_model.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Copyright (C) 2022 Mohamed El Mouctar HAIDARA
+# Copyright (C) 2023 Mohamed El Mouctar HAIDARA
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -10,61 +10,83 @@
 # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 # GNU General Public License for more details.
 #
 # You should have received a copy of the GNU General Public License
 # along with this program.  If not, see <https://www.gnu.org/licenses/>.
 import os
 from collections import defaultdict
-from typing import Dict, List, ItemsView, Set, Type
+from typing import Dict, List, Set, Type, Tuple, Optional
 
-from ansibleplaybookgrapher.utils import generate_id
+from ansibleplaybookgrapher.utils import generate_id, get_play_colors
+
+
+class LoopMixin:
+    """
+    A mixin class for nodes that support looping
+    """
+
+    def has_loop(self) -> bool:
+        """
+        Return true if the node has a loop (`loop` or `with_`).
+        https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html
+        :return:
+        """
+        if self.raw_object is None:
+            return False
+        return self.raw_object.loop is not None
 
 
 class Node:
     """
-    A node in the graph. Everything of the final graph is a node: playbook, plays, edges, tasks and roles.
+    A node in the graph. Everything of the final graph is a node: playbook, plays, tasks and roles.
     """
 
     def __init__(
         self,
         node_name: str,
         node_id: str,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: Optional[int] = None,
     ):
         """
 
         :param node_name: The name of the node
         :param node_id: An identifier for this node
         :param when: The conditional attached to the node
         :param raw_object: The raw ansible object matching this node in the graph. Will be None if there is no match on
         Ansible side
-        :param parent: The parent of this node
+        :param parent: The parent node of this node
         """
         self.name = node_name
         self.parent = parent
         self.id = node_id
         self.when = when
         self.raw_object = raw_object
-        # Trying to get the object position in the parsed files. Format: (path,line,column)
+
+        # Get the node position in the parsed files. Format: (path,line,column)
         self.path = self.line = self.column = None
-        self.retrieve_position()
+        self.set_position()
+
+        # The index of this node in the parent node if it has one (starting from 1)
+        self.index: Optional[int] = index
 
-    def retrieve_position(self):
+    def set_position(self):
         """
         Set the path of this based on the raw object. Not all objects have path
         :return:
         """
         if self.raw_object and self.raw_object.get_ds():
             self.path, self.line, self.column = self.raw_object.get_ds().ansible_pos
 
-    def get_first_parent_matching_type(self, node_type: Type) -> "Type":
+    def get_first_parent_matching_type(self, node_type: Type) -> Type:
         """
         Get the first parent of this node matching the given type
+        :param node_type: The type of the parent to get
         :return:
         """
         current_parent = self.parent
 
         while current_parent is not None:
             if isinstance(current_parent, node_type):
                 return current_parent
@@ -83,86 +105,95 @@
 
     def __hash__(self):
         return hash(self.id)
 
 
 class CompositeNode(Node):
     """
-    A node that composed of multiple of nodes.
+    A node composed of multiple of nodes:
+     - playbook containing plays
+     - play containing tasks
+     - role containing tasks
+     - block containing tasks
     """
 
     def __init__(
         self,
         node_name: str,
         node_id: str,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
         supported_compositions: List[str] = None,
     ):
         """
 
         :param node_name:
         :param node_id:
         :param raw_object: The raw ansible object matching this node in the graph. Will be None if there is no match on
         Ansible side
-        :param supported_compositions:
+        :param supported_compositions: The list of the supported compositions for this composite node.
         """
-        super().__init__(node_name, node_id, when, raw_object, parent)
+        super().__init__(
+            node_name=node_name,
+            node_id=node_id,
+            when=when,
+            raw_object=raw_object,
+            parent=parent,
+            index=index,
+        )
         self._supported_compositions = supported_compositions or []
         # The dict will contain the different types of composition.
         self._compositions = defaultdict(list)  # type: Dict[str, List]
-
-    def items(self) -> ItemsView[str, List[Node]]:
-        """
-        Return a view object (list of tuples) of all the nodes inside this composite node. The first element of the
-        tuple is the composition name and the second one a list of nodes
-        :return:
-        """
-        return self._compositions.items()
+        # Used to count the number of nodes in this composite node
+        self._node_counter = 0
 
     def add_node(self, target_composition: str, node: Node):
         """
         Add a node in the target composition
         :param target_composition: The name of the target composition
         :param node: The node to add in the given composition
         :return:
         """
         if target_composition not in self._supported_compositions:
             raise Exception(
                 f"The target composition '{target_composition}' is unknown. Supported are: {self._supported_compositions}"
             )
         self._compositions[target_composition].append(node)
+        # The node index is position in the composition regardless of the type of the node
+        node.index = self._node_counter + 1
+        self._node_counter += 1
 
     def get_all_tasks(self) -> List["TaskNode"]:
         """
-        Return all the TaskNode inside a composite node
+        Return all the TaskNode inside this composite node
         :return:
         """
         tasks: List[TaskNode] = []
         self._get_all_tasks_nodes(tasks)
         return tasks
 
     def _get_all_tasks_nodes(self, task_acc: List["Node"]):
         """
         Recursively get all tasks
         :param task_acc:
         :return:
         """
-        items = self.items()
+        items = self._compositions.items()
         for _, nodes in items:
             for node in nodes:
                 if isinstance(node, TaskNode):
                     task_acc.append(node)
                 elif isinstance(node, CompositeNode):
                     node._get_all_tasks_nodes(task_acc)
 
     def links_structure(self) -> Dict[Node, List[Node]]:
         """
-        Return a representation of the composite node where each key of the dictionary is the node id and the
+        Return a representation of the composite node where each key of the dictionary is the node and the
          value is the list of the linked nodes
         :return:
         """
         links: Dict[Node, List[Node]] = defaultdict(list)
         self._get_all_links(links)
         return links
 
@@ -186,17 +217,23 @@
     def __init__(
         self,
         node_name: str,
         node_id: str,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
     ):
         super().__init__(
-            node_name, node_id, when=when, raw_object=raw_object, parent=parent
+            node_name=node_name,
+            node_id=node_id,
+            when=when,
+            raw_object=raw_object,
+            parent=parent,
+            index=index,
         )
         self._supported_compositions = ["tasks"]
 
     def add_node(self, target_composition: str, node: Node):
         """
         Override the add_node because block only contains "tasks" regardless of the context (pre_tasks or post_tasks)
         :param target_composition: This is ignored. It's always "tasks" for block
@@ -216,25 +253,31 @@
 
 class PlaybookNode(CompositeNode):
     """
     A playbook is a list of play
     """
 
     def __init__(
-        self, node_name: str, node_id: str = None, when: str = "", raw_object=None
+        self,
+        node_name: str,
+        node_id: str = None,
+        when: str = "",
+        raw_object=None,
+        index: int = None,
     ):
         super().__init__(
-            node_name,
-            node_id or generate_id("playbook_"),
+            node_name=node_name,
+            node_id=node_id or generate_id("playbook_"),
             when=when,
             raw_object=raw_object,
+            index=index,
             supported_compositions=["plays"],
         )
 
-    def retrieve_position(self):
+    def set_position(self):
         """
         Playbooks only have path as position
         :return:
         """
         # Since the playbook is the whole file, the set the position as the beginning of the file
         self.path = os.path.join(os.getcwd(), self.name)
         self.line = 1
@@ -244,30 +287,30 @@
     def plays(self) -> List["PlayNode"]:
         """
         Return the list of plays
         :return:
         """
         return self._compositions["plays"]
 
-    def roles_usage(self) -> Dict["RoleNode", List[Node]]:
+    def roles_usage(self) -> Dict["RoleNode", Set["PlayNode"]]:
         """
-        For each role in the graph, return the plays that reference the role
-        :return: A dict with key as role node and value the list of plays
+        For each role in the playbook, get the uniq plays that reference the role
+        :return: A dict with key as role node and value the list of uniq plays that use it
         """
 
-        usages = defaultdict(list)
+        usages = defaultdict(set)
         links = self.links_structure()
 
         for node, linked_nodes in links.items():
             for linked_node in linked_nodes:
                 if isinstance(linked_node, RoleNode):
                     if isinstance(node, PlayNode):
-                        usages[linked_node].append(node)
+                        usages[linked_node].add(node)
                     else:
-                        usages[linked_node].append(
+                        usages[linked_node].add(
                             node.get_first_parent_matching_type(PlayNode)
                         )
 
         return usages
 
 
 class PlayNode(CompositeNode):
@@ -282,30 +325,33 @@
     def __init__(
         self,
         node_name: str,
         node_id: str = None,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
         hosts: List[str] = None,
     ):
         """
         :param node_name:
         :param node_id:
         :param hosts: List of hosts attached to the play
         """
         super().__init__(
             node_name,
             node_id or generate_id("play_"),
             when=when,
             raw_object=raw_object,
             parent=parent,
+            index=index,
             supported_compositions=["pre_tasks", "roles", "tasks", "post_tasks"],
         )
         self.hosts = hosts or []
+        self.colors: Tuple[str, str] = get_play_colors(self.id)
 
     @property
     def roles(self) -> List["RoleNode"]:
         return self._compositions["roles"]
 
     @property
     def pre_tasks(self) -> List["Node"]:
@@ -328,64 +374,69 @@
     def __init__(
         self,
         node_name: str,
         node_id: str = None,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
     ):
         super().__init__(
-            node_name,
-            node_id or generate_id("block_"),
+            node_name=node_name,
+            node_id=node_id or generate_id("block_"),
             when=when,
             raw_object=raw_object,
             parent=parent,
+            index=index,
         )
 
 
-class TaskNode(Node):
+class TaskNode(LoopMixin, Node):
     """
     A task node. This matches an Ansible Task.
     """
 
     def __init__(
         self,
         node_name: str,
         node_id: str = None,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
     ):
         """
 
         :param node_name:
         :param node_id:
         :param raw_object:
         """
         super().__init__(
-            node_name,
-            node_id or generate_id("task_"),
+            node_name=node_name,
+            node_id=node_id or generate_id("task_"),
             when=when,
             raw_object=raw_object,
             parent=parent,
+            index=index,
         )
 
 
-class RoleNode(CompositeTasksNode):
+class RoleNode(LoopMixin, CompositeTasksNode):
     """
     A role node. A role is a composition of tasks
     """
 
     def __init__(
         self,
         node_name: str,
         node_id: str = None,
         when: str = "",
         raw_object=None,
         parent: "Node" = None,
+        index: int = None,
         include_role: bool = False,
     ):
         """
 
         :param node_name:
         :param node_id:
         :param raw_object:
@@ -393,20 +444,28 @@
         self.include_role = include_role
         super().__init__(
             node_name,
             node_id or generate_id("role_"),
             when=when,
             raw_object=raw_object,
             parent=parent,
+            index=index,
         )
 
-    def retrieve_position(self):
+    def set_position(self):
         """
         Retrieve the position depending on whether it's an include_role or not
         :return:
         """
         if self.raw_object and not self.include_role:
             # If it's not an include_role, we take the role path which the path to the folder where the role is located
             # on the disk
             self.path = self.raw_object._role_path
         else:
-            super().retrieve_position()
+            super().set_position()
+
+    def has_loop(self) -> bool:
+        if not self.include_role:
+            # Only include_role supports loop
+            return False
+
+        return super().has_loop()
```

## Comparing `ansibleplaybookgrapher/postprocessor.py` & `ansibleplaybookgrapher/renderer/graphviz/postprocessor.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# Copyright (C) 2022 Mohamed El Mouctar HAIDARA
+# Copyright (C) 2023 Mohamed El Mouctar HAIDARA
 #
 # This program is free software: you can redistribute it and/or modify
 # it under the terms of the GNU General Public License as published by
 # the Free Software Foundation, either version 3 of the License, or
 # (at your option) any later version.
 #
 # This program is distributed in the hope that it will be useful,
@@ -15,39 +15,38 @@
 import os
 from typing import Dict, List
 
 from ansible.utils.display import Display
 from lxml import etree
 from svg.path import parse_path
 
-from ansibleplaybookgrapher.graph import PlaybookNode
+from ansibleplaybookgrapher.graph_model import PlaybookNode
 
 display = Display()
-DISPLAY_PREFIX = "postprocessor:"
 
 JQUERY = "https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"
 SVG_NAMESPACE = "http://www.w3.org/2000/svg"
 
 
 def _read_data(filename: str) -> str:
     """
     Read the script and return is as string
     :param filename:
     :return:
     """
     current_dir = os.path.abspath(os.path.dirname(__file__))
-    javascript_path = os.path.join(current_dir, "data", filename)
+    javascript_path = os.path.join(current_dir, "../../data", filename)
 
     with open(javascript_path) as javascript:
         return javascript.read()
 
 
-class GraphVizPostProcessor:
+class GraphvizPostProcessor:
     """
-    Post process the svg by adding some javascript and css
+    Post process the svg by adding some javascript, css and hover effects
     """
 
     def __init__(self, svg_path: str):
         """
         :param svg_path:
         """
         self.svg_path = svg_path
@@ -171,15 +170,15 @@
         # This is relatively slow to compute. Decreasing the "error" will drastically slow down the post-processing
         segment_length = path_segments.length(error=1e-4)
         text_length = len(text)
         # We put the label closer to the target node
         offset_factor = 0.76
 
         start_offset = segment_length * offset_factor - text_length
-        msg = f"{DISPLAY_PREFIX} {len(path_segments)} segment(s) found for the path '{path_element.get('id')}', "
+        msg = f"{len(path_segments)} segment(s) found for the path '{path_element.get('id')}', "
         msg += f"segment_length={segment_length}, start_offset={start_offset}, text_length={text_length}"
         display.vvvvv(msg)
         return str(start_offset)
 
     def _curve_text_on_edges(self):
         """
         Update the text on each edge to curve it based on the edge
```

## Comparing `ansible_playbook_grapher-1.2.0.dist-info/LICENSE` & `ansible_playbook_grapher-2.0.0.dev0.dist-info/LICENSE`

 * *Files identical despite different names*

