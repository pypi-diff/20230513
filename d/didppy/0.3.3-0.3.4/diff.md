# Comparing `tmp/didppy-0.3.3.tar.gz` & `tmp/didppy-0.3.4.tar.gz`

## Comparing `didppy-0.3.3.tar` & `didppy-0.3.4.tar`

### file list

```diff
@@ -1,154 +1,154 @@
--rw-r--r--   0        0        0      405 1970-01-01 00:00:00.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/Cargo.toml
--rw-r--r--   0      501       20     1685 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/README.md
--rw-r--r--   0      501       20     3915 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/caasdy.rs
--rw-r--r--   0      501       20     3922 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_acps.rs
--rw-r--r--   0      501       20     3867 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_apps.rs
--rw-r--r--   0      501       20     3559 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_breadth_first_search.rs
--rw-r--r--   0      501       20     4414 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_cabs.rs
--rw-r--r--   0      501       20     3645 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_cbfs.rs
--rw-r--r--   0      501       20     3773 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_dbdfs.rs
--rw-r--r--   0      501       20     3984 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_dfbb.rs
--rw-r--r--   0      501       20     3425 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_weighted_astar.rs
--rw-r--r--   0      501       20     8062 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/expression_beam_search.rs
--rw-r--r--   0      501       20     1711 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/f_evaluator_type.rs
--rw-r--r--   0      501       20     1192 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/lib.rs
--rw-r--r--   0      501       20    10895 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/acps.rs
--rw-r--r--   0      501       20    12016 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/apps.rs
--rw-r--r--   0      501       20     9941 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/beam_search.rs
--rw-r--r--   0      501       20    10115 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/best_first_search.rs
--rw-r--r--   0      501       20     9967 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/breadth_first_search.rs
--rw-r--r--   0      501       20    10642 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cabs.rs
--rw-r--r--   0      501       20    10414 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cbfs.rs
--rw-r--r--   0      501       20    19258 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam.rs
--rw-r--r--   0      501       20     8068 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_node.rs
--rw-r--r--   0      501       20      930 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_problem_instance.rs
--rw-r--r--   0      501       20     2153 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/bfs_node.rs
--rw-r--r--   0      501       20    37845 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/f_node.rs
--rw-r--r--   0      501       20    47180 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/hashable_state.rs
--rw-r--r--   0      501       20     3549 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/lazy_search_node.rs
--rw-r--r--   0      501       20      222 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/prioritized_node.rs
--rw-r--r--   0      501       20    20071 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/search_node.rs
--rw-r--r--   0      501       20    49429 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/state_registry.rs
--rw-r--r--   0      501       20    17046 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/successor_generator.rs
--rw-r--r--   0      501       20     3608 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_chain.rs
--rw-r--r--   0      501       20    28031 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_with_custom_cost.rs
--rw-r--r--   0      501       20     1971 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/util.rs
--rw-r--r--   0      501       20     1016 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure.rs
--rw-r--r--   0      501       20    10386 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dbdfs.rs
--rw-r--r--   0      501       20     8338 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbb.rs
--rw-r--r--   0      501       20     8947 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbbbfs.rs
--rw-r--r--   0      501       20    14198 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dijkstra.rs
--rw-r--r--   0      501       20     7077 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/forward_recursion.rs
--rw-r--r--   0      501       20    16651 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/rollout.rs
--rw-r--r--   0      501       20     3780 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/search.rs
--rw-r--r--   0      501       20     3707 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/util.rs
--rw-r--r--   0      501       20      918 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm.rs
--rw-r--r--   0        0        0      377 1970-01-01 00:00:00.000000 didppy-0.3.3/local_dependencies/dypdl/Cargo.toml
--rw-r--r--   0      501       20     5194 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/README.md
--rw-r--r--   0      501       20     3301 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/base_case.rs
--rw-r--r--   0      501       20     1344 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/effect.rs
--rw-r--r--   0      501       20    16931 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/argument_expression.rs
--rw-r--r--   0      501       20    59188 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/condition.rs
--rw-r--r--   0      501       20   290240 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/continuous_expression.rs
--rw-r--r--   0      501       20    36620 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/continuous_vector_expression.rs
--rw-r--r--   0      501       20    88634 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/element_expression.rs
--rw-r--r--   0      501       20   134795 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/integer_expression.rs
--rw-r--r--   0      501       20    25379 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/integer_vector_expression.rs
--rw-r--r--   0      501       20    18114 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/numeric_operator.rs
--rw-r--r--   0      501       20    62551 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/numeric_table_expression.rs
--rw-r--r--   0      501       20     4969 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/reference_expression.rs
--rw-r--r--   0      501       20    48744 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/set_condition.rs
--rw-r--r--   0      501       20   114732 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/set_expression.rs
--rw-r--r--   0      501       20   135581 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/set_reduce_expression.rs
--rw-r--r--   0      501       20    15550 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/table_expression.rs
--rw-r--r--   0      501       20    56292 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/table_vector_expression.rs
--rw-r--r--   0      501       20     1787 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/util.rs
--rw-r--r--   0      501       20    19963 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression/vector_expression.rs
--rw-r--r--   0      501       20     1500 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/expression.rs
--rw-r--r--   0      501       20    26414 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/grounded_condition.rs
--rw-r--r--   0      501       20   650168 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/lib.rs
--rw-r--r--   0      501       20   131318 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/state.rs
--rw-r--r--   0      501       20    18956 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/table.rs
--rw-r--r--   0      501       20    46003 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/table_data.rs
--rw-r--r--   0      501       20    84395 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/table_registry.rs
--rw-r--r--   0      501       20    55902 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/transition.rs
--rw-r--r--   0      501       20      438 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/util.rs
--rw-r--r--   0      501       20     3450 2023-03-21 15:58:35.000000 didppy-0.3.3/local_dependencies/dypdl/src/variable_type.rs
--rw-r--r--   0        0        0      748 1970-01-01 00:00:00.000000 didppy-0.3.3/Cargo.toml
--rw-r--r--   0      501       20      705 2023-03-21 15:58:35.000000 didppy-0.3.3/.gitignore
--rw-r--r--   0      501       20     1872 2023-03-21 15:58:35.000000 didppy-0.3.3/README.md
--rw-r--r--   0      501       20       71 2023-03-21 15:58:35.000000 didppy-0.3.3/build.rs
--rw-r--r--   0      501       20      634 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/Makefile
--rw-r--r--   0      501       20    29958 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/_static/images/TSPTW.png
--rw-r--r--   0      501       20      645 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/_templates/autosummary/class.rst
--rw-r--r--   0      501       20     8470 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/advanced-tutorials/forced-transitions.rst
--rw-r--r--   0      501       20     6060 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/advanced-tutorials/general-cost.rst
--rw-r--r--   0      501       20      250 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/advanced-tutorials.rst
--rw-r--r--   0      501       20     1931 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/api-reference.rst
--rw-r--r--   0      501       20     2218 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/conf.py
--rw-r--r--   0      501       20     4189 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/debugging/common-mistakes.rst
--rw-r--r--   0      501       20     5687 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/debugging/state.rst
--rw-r--r--   0      501       20     2881 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/debugging/validate.rst
--rw-r--r--   0      501       20      255 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/debugging.rst
--rw-r--r--   0      501       20     2237 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/examples.rst
--rw-r--r--   0      501       20     1086 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/index.rst
--rw-r--r--   0      501       20      800 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/make.bat
--rw-r--r--   0      501       20     1494 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/papers.rst
--rw-r--r--   0      501       20     4205 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/quickstart.rst
--rw-r--r--   0      501       20     7668 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/ref.bib
--rw-r--r--   0      501       20       67 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/references.rst
--rw-r--r--   0      501       20       45 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/requirements.txt
--rw-r--r--   0      501       20     4859 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/solver-selection.rst
--rw-r--r--   0      501       20    28129 2023-03-21 15:58:35.000000 didppy-0.3.3/docs/tutorial.rst
--rw-r--r--   0      501       20     2617 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/README.md
--rw-r--r--   0      501       20    10326 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/bin-packing.ipynb
--rw-r--r--   0      501       20     9176 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/cvrp.ipynb
--rw-r--r--   0      501       20     5949 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/graph-clear.ipynb
--rw-r--r--   0      501       20     4906 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/knapsack.ipynb
--rw-r--r--   0      501       20     9295 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/m-pdtsp.ipynb
--rw-r--r--   0      501       20     6910 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/mosp.ipynb
--rw-r--r--   0      501       20     9923 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/salbp-1.ipynb
--rw-r--r--   0      501       20     5293 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/single-machine.ipynb
--rw-r--r--   0      501       20     7666 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/talent-scheduling.ipynb
--rw-r--r--   0      501       20     8093 2023-03-21 15:58:35.000000 didppy-0.3.3/examples/tsptw.ipynb
--rw-r--r--   0      501       20      584 2023-03-21 15:58:35.000000 didppy-0.3.3/pyproject.toml
--rw-r--r--   0      501       20     9027 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/acps.rs
--rw-r--r--   0      501       20     9135 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/apps.rs
--rw-r--r--   0      501       20     8285 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/breadth_first_search.rs
--rw-r--r--   0      501       20     8500 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/caasdy.rs
--rw-r--r--   0      501       20     8418 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/cabs.rs
--rw-r--r--   0      501       20     8193 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/cbfs.rs
--rw-r--r--   0      501       20     8461 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/dbdfs.rs
--rw-r--r--   0      501       20     8253 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/dfbb.rs
--rw-r--r--   0      501       20     5103 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/dijkstra.rs
--rw-r--r--   0      501       20    13229 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/expression_beam_search.rs
--rw-r--r--   0      501       20     1675 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/f_operator.rs
--rw-r--r--   0      501       20     3616 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/forward_recursion.rs
--rw-r--r--   0      501       20     8124 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/weighted_astar.rs
--rw-r--r--   0      501       20     6297 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver/wrapped_solver.rs
--rw-r--r--   0      501       20      728 2023-03-21 15:58:35.000000 didppy-0.3.3/src/heuristic_search_solver.rs
--rw-r--r--   0      501       20     2919 2023-03-21 15:58:35.000000 didppy-0.3.3/src/lib.rs
--rw-r--r--   0      501       20   376402 2023-03-21 15:58:35.000000 didppy-0.3.3/src/model/expression.rs
--rw-r--r--   0      501       20     4897 2023-03-21 15:58:35.000000 didppy-0.3.3/src/model/state.rs
--rw-r--r--   0      501       20   172084 2023-03-21 15:58:35.000000 didppy-0.3.3/src/model/table.rs
--rw-r--r--   0      501       20    44254 2023-03-21 15:58:35.000000 didppy-0.3.3/src/model/transition.rs
--rw-r--r--   0      501       20   543965 2023-03-21 15:58:35.000000 didppy-0.3.3/src/model.rs
--rw-r--r--   0      501       20     2741 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_acps.py
--rw-r--r--   0      501       20     2741 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_apps.py
--rw-r--r--   0      501       20     2687 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_bradth_first_search.py
--rw-r--r--   0      501       20     2627 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_caasdy.py
--rw-r--r--   0      501       20     2561 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_cabs.py
--rw-r--r--   0      501       20     2617 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_cbfs.py
--rw-r--r--   0      501       20     2658 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_dbdfs.py
--rw-r--r--   0      501       20     2617 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_dfbb.py
--rw-r--r--   0      501       20     1565 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_dijkstra.py
--rw-r--r--   0      501       20     1613 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_expression_beam_search.py
--rw-r--r--   0      501       20     1589 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_forward_recursion.py
--rw-r--r--   0      501       20     2727 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/heuristic_search_solver/test_weighted_astar.py
--rw-r--r--   0      501       20    85219 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/model/test_expression.py
--rw-r--r--   0      501       20     6576 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/model/test_state.py
--rw-r--r--   0      501       20    66254 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/model/test_table.py
--rw-r--r--   0      501       20    16456 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/model/test_transition.py
--rw-r--r--   0      501       20    54164 2023-03-21 15:58:35.000000 didppy-0.3.3/tests/test_model.py
--rw-r--r--   0      501       20    12339 2023-03-21 15:58:34.000000 didppy-0.3.3/Cargo.lock
--rw-r--r--   0        0        0     2322 1970-01-01 00:00:00.000000 didppy-0.3.3/PKG-INFO
+-rw-r--r--   0        0        0      377 1970-01-01 00:00:00.000000 didppy-0.3.4/local_dependencies/dypdl/Cargo.toml
+-rw-r--r--   0      501       20     5194 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/README.md
+-rw-r--r--   0      501       20     3301 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/base_case.rs
+-rw-r--r--   0      501       20     1344 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/effect.rs
+-rw-r--r--   0      501       20    16931 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/argument_expression.rs
+-rw-r--r--   0      501       20    59188 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/condition.rs
+-rw-r--r--   0      501       20   290240 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/continuous_expression.rs
+-rw-r--r--   0      501       20    36620 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/continuous_vector_expression.rs
+-rw-r--r--   0      501       20    88634 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/element_expression.rs
+-rw-r--r--   0      501       20   134795 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/integer_expression.rs
+-rw-r--r--   0      501       20    25379 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/integer_vector_expression.rs
+-rw-r--r--   0      501       20    18114 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/numeric_operator.rs
+-rw-r--r--   0      501       20    62551 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/numeric_table_expression.rs
+-rw-r--r--   0      501       20     4969 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/reference_expression.rs
+-rw-r--r--   0      501       20    48744 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/set_condition.rs
+-rw-r--r--   0      501       20   114732 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/set_expression.rs
+-rw-r--r--   0      501       20   135581 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/set_reduce_expression.rs
+-rw-r--r--   0      501       20    15550 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/table_expression.rs
+-rw-r--r--   0      501       20    56292 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/table_vector_expression.rs
+-rw-r--r--   0      501       20     1787 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/util.rs
+-rw-r--r--   0      501       20    19963 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression/vector_expression.rs
+-rw-r--r--   0      501       20     1500 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/expression.rs
+-rw-r--r--   0      501       20    26414 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/grounded_condition.rs
+-rw-r--r--   0      501       20   650168 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/lib.rs
+-rw-r--r--   0      501       20   131318 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/state.rs
+-rw-r--r--   0      501       20    18956 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/table.rs
+-rw-r--r--   0      501       20    46003 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/table_data.rs
+-rw-r--r--   0      501       20    84395 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/table_registry.rs
+-rw-r--r--   0      501       20    55902 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/transition.rs
+-rw-r--r--   0      501       20      438 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/util.rs
+-rw-r--r--   0      501       20     3450 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl/src/variable_type.rs
+-rw-r--r--   0        0        0      405 1970-01-01 00:00:00.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/Cargo.toml
+-rw-r--r--   0      501       20     1685 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/README.md
+-rw-r--r--   0      501       20     3915 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/caasdy.rs
+-rw-r--r--   0      501       20     3922 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_acps.rs
+-rw-r--r--   0      501       20     3867 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_apps.rs
+-rw-r--r--   0      501       20     3559 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_breadth_first_search.rs
+-rw-r--r--   0      501       20     4414 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_cabs.rs
+-rw-r--r--   0      501       20     3645 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_cbfs.rs
+-rw-r--r--   0      501       20     3773 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_dbdfs.rs
+-rw-r--r--   0      501       20     3984 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_dfbb.rs
+-rw-r--r--   0      501       20     3425 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_weighted_astar.rs
+-rw-r--r--   0      501       20     8062 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/expression_beam_search.rs
+-rw-r--r--   0      501       20     1711 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/f_evaluator_type.rs
+-rw-r--r--   0      501       20     1192 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/lib.rs
+-rw-r--r--   0      501       20    10895 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/acps.rs
+-rw-r--r--   0      501       20    12016 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/apps.rs
+-rw-r--r--   0      501       20     9941 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/beam_search.rs
+-rw-r--r--   0      501       20    10115 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/best_first_search.rs
+-rw-r--r--   0      501       20     9967 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/breadth_first_search.rs
+-rw-r--r--   0      501       20    10642 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cabs.rs
+-rw-r--r--   0      501       20    10414 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cbfs.rs
+-rw-r--r--   0      501       20    19258 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam.rs
+-rw-r--r--   0      501       20     8068 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_node.rs
+-rw-r--r--   0      501       20      930 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_problem_instance.rs
+-rw-r--r--   0      501       20     2153 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/bfs_node.rs
+-rw-r--r--   0      501       20    37845 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/f_node.rs
+-rw-r--r--   0      501       20    47180 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/hashable_state.rs
+-rw-r--r--   0      501       20     3549 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/lazy_search_node.rs
+-rw-r--r--   0      501       20      222 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/prioritized_node.rs
+-rw-r--r--   0      501       20    20071 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/search_node.rs
+-rw-r--r--   0      501       20    49429 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/state_registry.rs
+-rw-r--r--   0      501       20    17046 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/successor_generator.rs
+-rw-r--r--   0      501       20     3608 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_chain.rs
+-rw-r--r--   0      501       20    28031 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_with_custom_cost.rs
+-rw-r--r--   0      501       20     1971 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/util.rs
+-rw-r--r--   0      501       20     1016 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure.rs
+-rw-r--r--   0      501       20    10386 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dbdfs.rs
+-rw-r--r--   0      501       20     8338 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbb.rs
+-rw-r--r--   0      501       20     8947 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbbbfs.rs
+-rw-r--r--   0      501       20    14198 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dijkstra.rs
+-rw-r--r--   0      501       20     7077 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/forward_recursion.rs
+-rw-r--r--   0      501       20    16651 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/rollout.rs
+-rw-r--r--   0      501       20     3780 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/search.rs
+-rw-r--r--   0      501       20     3707 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/util.rs
+-rw-r--r--   0      501       20      918 2023-05-13 01:44:59.000000 didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm.rs
+-rw-r--r--   0        0        0      748 1970-01-01 00:00:00.000000 didppy-0.3.4/Cargo.toml
+-rw-r--r--   0      501       20      705 2023-05-13 01:44:59.000000 didppy-0.3.4/.gitignore
+-rw-r--r--   0      501       20     1872 2023-05-13 01:44:59.000000 didppy-0.3.4/README.md
+-rw-r--r--   0      501       20       71 2023-05-13 01:44:59.000000 didppy-0.3.4/build.rs
+-rw-r--r--   0      501       20      634 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/Makefile
+-rw-r--r--   0      501       20    29958 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/_static/images/TSPTW.png
+-rw-r--r--   0      501       20      645 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/_templates/autosummary/class.rst
+-rw-r--r--   0      501       20     8470 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/advanced-tutorials/forced-transitions.rst
+-rw-r--r--   0      501       20     6060 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/advanced-tutorials/general-cost.rst
+-rw-r--r--   0      501       20      250 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/advanced-tutorials.rst
+-rw-r--r--   0      501       20     1931 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/api-reference.rst
+-rw-r--r--   0      501       20     2246 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/conf.py
+-rw-r--r--   0      501       20     4189 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/debugging/common-mistakes.rst
+-rw-r--r--   0      501       20     5687 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/debugging/state.rst
+-rw-r--r--   0      501       20     2881 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/debugging/validate.rst
+-rw-r--r--   0      501       20      255 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/debugging.rst
+-rw-r--r--   0      501       20     2237 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/examples.rst
+-rw-r--r--   0      501       20     1086 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/index.rst
+-rw-r--r--   0      501       20      800 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/make.bat
+-rw-r--r--   0      501       20     1494 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/papers.rst
+-rw-r--r--   0      501       20     4205 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/quickstart.rst
+-rw-r--r--   0      501       20     7668 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/ref.bib
+-rw-r--r--   0      501       20       67 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/references.rst
+-rw-r--r--   0      501       20       45 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/requirements.txt
+-rw-r--r--   0      501       20     4859 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/solver-selection.rst
+-rw-r--r--   0      501       20    28129 2023-05-13 01:44:59.000000 didppy-0.3.4/docs/tutorial.rst
+-rw-r--r--   0      501       20     2617 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/README.md
+-rw-r--r--   0      501       20    10326 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/bin-packing.ipynb
+-rw-r--r--   0      501       20     9176 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/cvrp.ipynb
+-rw-r--r--   0      501       20     5949 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/graph-clear.ipynb
+-rw-r--r--   0      501       20     4906 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/knapsack.ipynb
+-rw-r--r--   0      501       20     9295 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/m-pdtsp.ipynb
+-rw-r--r--   0      501       20     6910 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/mosp.ipynb
+-rw-r--r--   0      501       20     9923 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/salbp-1.ipynb
+-rw-r--r--   0      501       20     5293 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/single-machine.ipynb
+-rw-r--r--   0      501       20     7666 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/talent-scheduling.ipynb
+-rw-r--r--   0      501       20     8093 2023-05-13 01:44:59.000000 didppy-0.3.4/examples/tsptw.ipynb
+-rw-r--r--   0      501       20      584 2023-05-13 01:44:59.000000 didppy-0.3.4/pyproject.toml
+-rw-r--r--   0      501       20     9027 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/acps.rs
+-rw-r--r--   0      501       20     9135 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/apps.rs
+-rw-r--r--   0      501       20     8285 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/breadth_first_search.rs
+-rw-r--r--   0      501       20     8500 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/caasdy.rs
+-rw-r--r--   0      501       20     8418 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/cabs.rs
+-rw-r--r--   0      501       20     8193 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/cbfs.rs
+-rw-r--r--   0      501       20     8461 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/dbdfs.rs
+-rw-r--r--   0      501       20     8253 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/dfbb.rs
+-rw-r--r--   0      501       20     5103 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/dijkstra.rs
+-rw-r--r--   0      501       20    13229 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/expression_beam_search.rs
+-rw-r--r--   0      501       20     1675 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/f_operator.rs
+-rw-r--r--   0      501       20     3616 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/forward_recursion.rs
+-rw-r--r--   0      501       20     8124 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/weighted_astar.rs
+-rw-r--r--   0      501       20     6297 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver/wrapped_solver.rs
+-rw-r--r--   0      501       20      728 2023-05-13 01:44:59.000000 didppy-0.3.4/src/heuristic_search_solver.rs
+-rw-r--r--   0      501       20     2919 2023-05-13 01:44:59.000000 didppy-0.3.4/src/lib.rs
+-rw-r--r--   0      501       20   376402 2023-05-13 01:44:59.000000 didppy-0.3.4/src/model/expression.rs
+-rw-r--r--   0      501       20     4897 2023-05-13 01:44:59.000000 didppy-0.3.4/src/model/state.rs
+-rw-r--r--   0      501       20   172084 2023-05-13 01:44:59.000000 didppy-0.3.4/src/model/table.rs
+-rw-r--r--   0      501       20    44254 2023-05-13 01:44:59.000000 didppy-0.3.4/src/model/transition.rs
+-rw-r--r--   0      501       20   543965 2023-05-13 01:44:59.000000 didppy-0.3.4/src/model.rs
+-rw-r--r--   0      501       20     2741 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_acps.py
+-rw-r--r--   0      501       20     2741 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_apps.py
+-rw-r--r--   0      501       20     2687 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_bradth_first_search.py
+-rw-r--r--   0      501       20     2627 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_caasdy.py
+-rw-r--r--   0      501       20     2561 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_cabs.py
+-rw-r--r--   0      501       20     2617 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_cbfs.py
+-rw-r--r--   0      501       20     2658 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_dbdfs.py
+-rw-r--r--   0      501       20     2617 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_dfbb.py
+-rw-r--r--   0      501       20     1565 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_dijkstra.py
+-rw-r--r--   0      501       20     1613 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_expression_beam_search.py
+-rw-r--r--   0      501       20     1589 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_forward_recursion.py
+-rw-r--r--   0      501       20     2727 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/heuristic_search_solver/test_weighted_astar.py
+-rw-r--r--   0      501       20    85219 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/model/test_expression.py
+-rw-r--r--   0      501       20     6576 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/model/test_state.py
+-rw-r--r--   0      501       20    66254 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/model/test_table.py
+-rw-r--r--   0      501       20    16456 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/model/test_transition.py
+-rw-r--r--   0      501       20    54164 2023-05-13 01:44:59.000000 didppy-0.3.4/tests/test_model.py
+-rw-r--r--   0      501       20    12339 2023-05-13 01:44:59.000000 didppy-0.3.4/Cargo.lock
+-rw-r--r--   0        0        0     2322 1970-01-01 00:00:00.000000 didppy-0.3.4/PKG-INFO
```

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/README.md` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/README.md`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/caasdy.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/caasdy.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_acps.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_acps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_apps.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_apps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_breadth_first_search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_breadth_first_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_cabs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_cabs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_cbfs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_cbfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_dbdfs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_dbdfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_dfbb.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_dfbb.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/dual_bound_weighted_astar.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/dual_bound_weighted_astar.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/expression_beam_search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/expression_beam_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/f_evaluator_type.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/f_evaluator_type.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/lib.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/lib.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/acps.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/acps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/apps.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/apps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/beam_search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/beam_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/best_first_search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/best_first_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/breadth_first_search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/breadth_first_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cabs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cabs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cbfs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/cbfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_node.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_node.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_problem_instance.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/beam_search_problem_instance.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/bfs_node.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/bfs_node.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/f_node.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/f_node.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/hashable_state.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/hashable_state.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/lazy_search_node.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/lazy_search_node.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/search_node.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/search_node.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/state_registry.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/state_registry.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/successor_generator.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/successor_generator.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_chain.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_chain.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_with_custom_cost.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/transition_with_custom_cost.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/util.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure/util.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/data_structure.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dbdfs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dbdfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbb.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbb.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbbbfs.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dfbbbfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dijkstra.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/dijkstra.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/forward_recursion.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/forward_recursion.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/rollout.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/rollout.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/search.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm/util.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm/util.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl-heuristic-search/src/search_algorithm.rs` & `didppy-0.3.4/local_dependencies/dypdl-heuristic-search/src/search_algorithm.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/README.md` & `didppy-0.3.4/local_dependencies/dypdl/README.md`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/base_case.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/base_case.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/effect.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/effect.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/argument_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/argument_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/condition.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/condition.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/continuous_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/continuous_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/continuous_vector_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/continuous_vector_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/element_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/element_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/integer_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/integer_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/integer_vector_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/integer_vector_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/numeric_operator.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/numeric_operator.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/numeric_table_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/numeric_table_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/reference_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/reference_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/set_condition.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/set_condition.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/set_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/set_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/set_reduce_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/set_reduce_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/table_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/table_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/table_vector_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/table_vector_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/util.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/util.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression/vector_expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression/vector_expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/expression.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/grounded_condition.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/grounded_condition.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/lib.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/lib.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/state.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/state.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/table.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/table.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/table_data.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/table_data.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/table_registry.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/table_registry.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/transition.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/transition.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/local_dependencies/dypdl/src/variable_type.rs` & `didppy-0.3.4/local_dependencies/dypdl/src/variable_type.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/Cargo.toml` & `didppy-0.3.4/Cargo.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [package]
 name = "didppy"
-version = "0.3.3"
+version = "0.3.4"
 edition = "2021"
 description = "Python interface for Dynamic Programming Description Language (DyPDL) and DyPDL solvers."
 license = "MIT OR Apache-2.0"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 [lib]
 name = "didppy"
 crate-type = ["cdylib"]
 
 [dependencies]
-dypdl = { path = "local_dependencies/dypdl", version = "0.3.3" }
-dypdl-heuristic-search = { path = "local_dependencies/dypdl-heuristic-search", version = "0.3.3" }
+dypdl = { path = "local_dependencies/dypdl", version = "0.3.4" }
+dypdl-heuristic-search = { path = "local_dependencies/dypdl-heuristic-search", version = "0.3.4" }
 rustc-hash = "1.1"
 
 [dependencies.pyo3]
 version = "0.18"
 
 [features]
 extension-module = ["pyo3/extension-module"]
```

### Comparing `didppy-0.3.3/.gitignore` & `didppy-0.3.4/.gitignore`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/README.md` & `didppy-0.3.4/README.md`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/Makefile` & `didppy-0.3.4/docs/Makefile`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/_static/images/TSPTW.png` & `didppy-0.3.4/docs/_static/images/TSPTW.png`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/_templates/autosummary/class.rst` & `didppy-0.3.4/docs/_templates/autosummary/class.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/advanced-tutorials/forced-transitions.rst` & `didppy-0.3.4/docs/advanced-tutorials/forced-transitions.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/advanced-tutorials/general-cost.rst` & `didppy-0.3.4/docs/advanced-tutorials/general-cost.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/api-reference.rst` & `didppy-0.3.4/docs/api-reference.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/conf.py` & `didppy-0.3.4/docs/conf.py`

 * *Files 8% similar despite different names*

```diff
@@ -29,14 +29,15 @@
 # ones.
 extensions = [
     "sphinx.ext.autodoc",
     "sphinx.ext.napoleon",
     "sphinx.ext.autosummary",
     "sphinx.ext.autosectionlabel",
     "sphinxcontrib.bibtex",
+    "sphinxcontrib.jquery",
 ]
 
 autosectionlabel_prefix_document = True
 
 # Add any paths that contain templates here, relative to this directory.
 templates_path = ["_templates"]
```

### Comparing `didppy-0.3.3/docs/debugging/common-mistakes.rst` & `didppy-0.3.4/docs/debugging/common-mistakes.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/debugging/state.rst` & `didppy-0.3.4/docs/debugging/state.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/debugging/validate.rst` & `didppy-0.3.4/docs/debugging/validate.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/examples.rst` & `didppy-0.3.4/docs/examples.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/index.rst` & `didppy-0.3.4/docs/index.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/make.bat` & `didppy-0.3.4/docs/make.bat`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/papers.rst` & `didppy-0.3.4/docs/papers.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/quickstart.rst` & `didppy-0.3.4/docs/quickstart.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/ref.bib` & `didppy-0.3.4/docs/ref.bib`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/solver-selection.rst` & `didppy-0.3.4/docs/solver-selection.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/docs/tutorial.rst` & `didppy-0.3.4/docs/tutorial.rst`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/README.md` & `didppy-0.3.4/examples/README.md`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/bin-packing.ipynb` & `didppy-0.3.4/examples/bin-packing.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/cvrp.ipynb` & `didppy-0.3.4/examples/cvrp.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/graph-clear.ipynb` & `didppy-0.3.4/examples/graph-clear.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/knapsack.ipynb` & `didppy-0.3.4/examples/knapsack.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/m-pdtsp.ipynb` & `didppy-0.3.4/examples/m-pdtsp.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/mosp.ipynb` & `didppy-0.3.4/examples/mosp.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/salbp-1.ipynb` & `didppy-0.3.4/examples/salbp-1.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/single-machine.ipynb` & `didppy-0.3.4/examples/single-machine.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/talent-scheduling.ipynb` & `didppy-0.3.4/examples/talent-scheduling.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/examples/tsptw.ipynb` & `didppy-0.3.4/examples/tsptw.ipynb`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/pyproject.toml` & `didppy-0.3.4/pyproject.toml`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/acps.rs` & `didppy-0.3.4/src/heuristic_search_solver/acps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/apps.rs` & `didppy-0.3.4/src/heuristic_search_solver/apps.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/breadth_first_search.rs` & `didppy-0.3.4/src/heuristic_search_solver/breadth_first_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/caasdy.rs` & `didppy-0.3.4/src/heuristic_search_solver/caasdy.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/cabs.rs` & `didppy-0.3.4/src/heuristic_search_solver/cabs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/cbfs.rs` & `didppy-0.3.4/src/heuristic_search_solver/cbfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/dbdfs.rs` & `didppy-0.3.4/src/heuristic_search_solver/dbdfs.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/dfbb.rs` & `didppy-0.3.4/src/heuristic_search_solver/dfbb.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/dijkstra.rs` & `didppy-0.3.4/src/heuristic_search_solver/dijkstra.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/expression_beam_search.rs` & `didppy-0.3.4/src/heuristic_search_solver/expression_beam_search.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/f_operator.rs` & `didppy-0.3.4/src/heuristic_search_solver/f_operator.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/forward_recursion.rs` & `didppy-0.3.4/src/heuristic_search_solver/forward_recursion.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/weighted_astar.rs` & `didppy-0.3.4/src/heuristic_search_solver/weighted_astar.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver/wrapped_solver.rs` & `didppy-0.3.4/src/heuristic_search_solver/wrapped_solver.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/heuristic_search_solver.rs` & `didppy-0.3.4/src/heuristic_search_solver.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/lib.rs` & `didppy-0.3.4/src/lib.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/model/expression.rs` & `didppy-0.3.4/src/model/expression.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/model/state.rs` & `didppy-0.3.4/src/model/state.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/model/table.rs` & `didppy-0.3.4/src/model/table.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/model/transition.rs` & `didppy-0.3.4/src/model/transition.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/src/model.rs` & `didppy-0.3.4/src/model.rs`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_acps.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_acps.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_apps.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_apps.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_bradth_first_search.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_bradth_first_search.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_caasdy.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_caasdy.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_cabs.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_cabs.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_cbfs.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_cbfs.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_dbdfs.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_dbdfs.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_dfbb.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_dfbb.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_dijkstra.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_dijkstra.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_expression_beam_search.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_expression_beam_search.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_forward_recursion.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_forward_recursion.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/heuristic_search_solver/test_weighted_astar.py` & `didppy-0.3.4/tests/heuristic_search_solver/test_weighted_astar.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/model/test_expression.py` & `didppy-0.3.4/tests/model/test_expression.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/model/test_state.py` & `didppy-0.3.4/tests/model/test_state.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/model/test_table.py` & `didppy-0.3.4/tests/model/test_table.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/model/test_transition.py` & `didppy-0.3.4/tests/model/test_transition.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/tests/test_model.py` & `didppy-0.3.4/tests/test_model.py`

 * *Files identical despite different names*

### Comparing `didppy-0.3.3/Cargo.lock` & `didppy-0.3.4/Cargo.lock`

 * *Files 1% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 name = "cfg-if"
 version = "1.0.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "baf1de4339761588bc0619e3cbc0120ee582ebb74b53b4efbf79117bd2da40fd"
 
 [[package]]
 name = "didp-yaml"
-version = "0.3.3"
+version = "0.3.4"
 dependencies = [
  "approx",
  "dypdl",
  "dypdl-heuristic-search",
  "lazy_static",
  "linked-hash-map",
  "num-traits",
@@ -50,37 +50,37 @@
  "serde_yaml",
  "tikv-jemallocator",
  "yaml-rust",
 ]
 
 [[package]]
 name = "didppy"
-version = "0.3.3"
+version = "0.3.4"
 dependencies = [
  "dypdl",
  "dypdl-heuristic-search",
  "pyo3",
  "pyo3-build-config",
  "rustc-hash",
 ]
 
 [[package]]
 name = "dypdl"
-version = "0.3.3"
+version = "0.3.4"
 dependencies = [
  "approx",
  "fixedbitset",
  "num-traits",
  "ordered-float",
  "rustc-hash",
 ]
 
 [[package]]
 name = "dypdl-heuristic-search"
-version = "0.3.3"
+version = "0.3.4"
 dependencies = [
  "dypdl",
  "ordered-float",
  "rustc-hash",
 ]
 
 [[package]]
```

### Comparing `didppy-0.3.3/PKG-INFO` & `didppy-0.3.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: didppy
-Version: 0.3.3
+Version: 0.3.4
 Classifier: Programming Language :: Rust
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Summary: Python interface for Dynamic Programming Description Language (DyPDL) and DyPDL solvers.
 License: MIT OR Apache-2.0
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
```

