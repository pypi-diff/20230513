# Comparing `tmp/pyvrp-0.1.0.tar.gz` & `tmp/pyvrp-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvrp-0.1.0.tar", max compression
+gzip compressed data, was "pyvrp-0.2.1.tar", max compression
```

## Comparing `pyvrp-0.1.0.tar` & `pyvrp-0.2.1.tar`

### file list

```diff
@@ -1,160 +1,162 @@
--rw-r--r--   0        0        0     1071 2023-03-01 19:49:38.347854 pyvrp-0.1.0/LICENSE
--rw-r--r--   0        0        0     2110 2023-03-01 19:49:38.347854 pyvrp-0.1.0/README.md
--rw-r--r--   0        0        0     3248 2023-03-01 19:49:38.347854 pyvrp-0.1.0/build_extensions.py
--rw-r--r--   0        0        0     4825 2023-03-01 19:49:38.371853 pyvrp-0.1.0/meson.build
--rw-r--r--   0        0        0      150 2023-03-01 19:49:38.371853 pyvrp-0.1.0/meson_options.txt
--rw-r--r--   0        0        0     3506 2023-03-01 19:49:38.371853 pyvrp-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     5848 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/GeneticAlgorithm.py
--rw-r--r--   0        0        0      189 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/OptimisationTarget.py
--rw-r--r--   0        0        0     4793 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/Population.py
--rw-r--r--   0        0        0     2659 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/Result.py
--rw-r--r--   0        0        0     5899 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/Statistics.py
--rw-r--r--   0        0        0     4242 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_Individual.pyi
--rw-r--r--   0        0        0      906 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_Matrix.pyi
--rw-r--r--   0        0        0     5379 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_PenaltyManager.pyi
--rw-r--r--   0        0        0     4505 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_ProblemData.pyi
--rw-r--r--   0        0        0     3007 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_SubPopulation.pyi
--rw-r--r--   0        0        0     1900 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_TimeWindowSegment.pyi
--rw-r--r--   0        0        0      267 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/_XorShift128.pyi
--rw-r--r--   0        0        0      436 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/__init__.py
--rw-r--r--   0        0        0     8842 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cli.py
--rw-r--r--   0        0        0     6460 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/Individual.cpp
--rw-r--r--   0        0        0     4006 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/Individual.h
--rw-r--r--   0        0        0     2206 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/Individual_bindings.cpp
--rw-r--r--   0        0        0     2484 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/Matrix.h
--rw-r--r--   0        0        0     1715 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/Matrix_bindings.cpp
--rw-r--r--   0        0        0     1997 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/PenaltyManager.cpp
--rw-r--r--   0        0        0     4875 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/PenaltyManager.h
--rw-r--r--   0        0        0     2722 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/PenaltyManager_bindings.cpp
--rw-r--r--   0        0        0     1452 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/ProblemData.cpp
--rw-r--r--   0        0        0     3029 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/ProblemData.h
--rw-r--r--   0        0        0     1902 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/ProblemData_bindings.cpp
--rw-r--r--   0        0        0      574 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/README.md
--rw-r--r--   0        0        0     4651 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/SubPopulation.cpp
--rw-r--r--   0        0        0     2744 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/SubPopulation.h
--rw-r--r--   0        0        0     2560 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/SubPopulation_bindings.cpp
--rw-r--r--   0        0        0     3166 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/TimeWindowSegment.h
--rw-r--r--   0        0        0      775 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/TimeWindowSegment_bindings.cpp
--rw-r--r--   0        0        0      581 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/XorShift128.cpp
--rw-r--r--   0        0        0     2017 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/XorShift128.h
--rw-r--r--   0        0        0      467 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/XorShift128_bindings.cpp
--rw-r--r--   0        0        0     2781 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/crossover/crossover.cpp
--rw-r--r--   0        0        0     1283 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/crossover/crossover.h
--rw-r--r--   0        0        0     6016 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/crossover/selective_route_exchange.cpp
--rw-r--r--   0        0        0      327 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/crossover/selective_route_exchange_bindings.cpp
--rw-r--r--   0        0        0     1007 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/diversity/broken_pairs_distance.cpp
--rw-r--r--   0        0        0      254 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/diversity/broken_pairs_distance_bindings.cpp
--rw-r--r--   0        0        0      686 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/diversity/diversity.h
--rw-r--r--   0        0        0     3011 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/CircleSector.h
--rw-r--r--   0        0        0     9865 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Exchange.h
--rw-r--r--   0        0        0     3536 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Exchange_bindings.cpp
--rw-r--r--   0        0        0    10457 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch.cpp
--rw-r--r--   0        0        0     3203 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch.h
--rw-r--r--   0        0        0     2592 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearchOperator.h
--rw-r--r--   0        0        0     1453 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch_bindings.cpp
--rw-r--r--   0        0        0     3039 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/MoveTwoClientsReversed.cpp
--rw-r--r--   0        0        0      457 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/MoveTwoClientsReversed.h
--rw-r--r--   0        0        0      633 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/MoveTwoClientsReversed_bindings.cpp
--rw-r--r--   0        0        0      669 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Node.cpp
--rw-r--r--   0        0        0     1666 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Node.h
--rw-r--r--   0        0        0      906 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/RelocateStar.cpp
--rw-r--r--   0        0        0      841 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/RelocateStar.h
--rw-r--r--   0        0        0      587 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/RelocateStar_bindings.cpp
--rw-r--r--   0        0        0     4141 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Route.cpp
--rw-r--r--   0        0        0     4921 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/Route.h
--rw-r--r--   0        0        0     9288 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/SwapStar.cpp
--rw-r--r--   0        0        0     3137 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/SwapStar.h
--rw-r--r--   0        0        0      571 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/SwapStar_bindings.cpp
--rw-r--r--   0        0        0     3533 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/TwoOpt.cpp
--rw-r--r--   0        0        0      719 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/TwoOpt.h
--rw-r--r--   0        0        0      560 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/cpp/educate/TwoOpt_bindings.cpp
--rw-r--r--   0        0        0       64 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/crossover/__init__.py
--rw-r--r--   0        0        0     1423 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/crossover/_selective_route_exchange.pyi
--rw-r--r--   0        0        0     6352 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/crossover/tests/test_selective_route_exchange.py
--rw-r--r--   0        0        0      115 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diagnostics/__init__.py
--rw-r--r--   0        0        0     3814 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diagnostics/get_route_statistics.py
--rw-r--r--   0        0        0        0 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diagnostics/tests/__init__.py
--rw-r--r--   0        0        0        7 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diagnostics/tests/test_get_route_statistics.py
--rw-r--r--   0        0        0       58 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diversity/__init__.py
--rw-r--r--   0        0        0     1462 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diversity/_broken_pairs_distance.pyi
--rw-r--r--   0        0        0     1384 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/diversity/tests/test_broken_pairs_distance.py
--rw-r--r--   0        0        0     6176 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/LocalSearch.py
--rw-r--r--   0        0        0     1335 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_Exchange.pyi
--rw-r--r--   0        0        0      822 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_LocalSearch.pyi
--rw-r--r--   0        0        0      267 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_MoveTwoClientsReversed.pyi
--rw-r--r--   0        0        0      259 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_RelocateStar.pyi
--rw-r--r--   0        0        0      255 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_SwapStar.pyi
--rw-r--r--   0        0        0      251 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/_TwoOpt.pyi
--rw-r--r--   0        0        0      708 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/__init__.py
--rw-r--r--   0        0        0     4121 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/neighbourhood.py
--rw-r--r--   0        0        0        0 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/__init__.py
--rw-r--r--   0        0        0     6913 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_Exchange.py
--rw-r--r--   0        0        0     3873 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_LocalSearch.py
--rw-r--r--   0        0        0     2375 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_MoveTwoClientsReversed.py
--rw-r--r--   0        0        0     2941 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_RelocateStar.py
--rw-r--r--   0        0        0     2727 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_SwapStar.py
--rw-r--r--   0        0        0     1916 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_TwoOpt.py
--rw-r--r--   0        0        0     3717 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/educate/tests/test_neighbourhood.py
--rw-r--r--   0        0        0      206 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/exceptions.py
--rw-r--r--   0        0        0      436 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/__init__.py
--rw-r--r--   0        0        0     1106 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_coordinates.py
--rw-r--r--   0        0        0     1046 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_demands.py
--rw-r--r--   0        0        0     1199 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_diversity.py
--rw-r--r--   0        0        0     1129 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_instance.py
--rw-r--r--   0        0        0     2343 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_objectives.py
--rw-r--r--   0        0        0     1608 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_result.py
--rw-r--r--   0        0        0     4756 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_route_schedule.py
--rw-r--r--   0        0        0     1136 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_runtimes.py
--rw-r--r--   0        0        0     1844 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_solution.py
--rw-r--r--   0        0        0     1226 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/plot_time_windows.py
--rw-r--r--   0        0        0        0 2023-03-01 19:49:38.375853 pyvrp-0.1.0/pyvrp/plotting/tests/__init__.py
--rw-r--r--   0        0        0    47981 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_instance.png
--rw-r--r--   0        0        0   141297 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_result.png
--rw-r--r--   0        0        0    35194 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_route_schedule.png
--rw-r--r--   0        0        0    25609 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution.png
--rw-r--r--   0        0        0    43058 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution_with_customers.png
--rw-r--r--   0        0        0     2968 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/plotting/tests/test_plotting.py
--rw-r--r--   0        0        0     5118 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/read.py
--rw-r--r--   0        0        0     1048 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/show_versions.py
--rw-r--r--   0        0        0      510 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/MaxIterations.py
--rw-r--r--   0        0        0      654 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/MaxRuntime.py
--rw-r--r--   0        0        0      907 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/NoImprovement.py
--rw-r--r--   0        0        0      625 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/StoppingCriterion.py
--rw-r--r--   0        0        0      630 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/TimedNoImprovement.py
--rw-r--r--   0        0        0      217 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/__init__.py
--rw-r--r--   0        0        0        0 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/tests/__init__.py
--rw-r--r--   0        0        0      922 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/tests/test_MaxIterations.py
--rw-r--r--   0        0        0     1083 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/tests/test_MaxRuntime.py
--rw-r--r--   0        0        0     1951 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/tests/test_NoImprovement.py
--rw-r--r--   0        0        0     1357 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/stop/tests/test_TimedNoImprovement.py
--rw-r--r--   0        0        0        0 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/__init__.py
--rw-r--r--   0        0        0      189 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/DepotNotOne.txt
--rw-r--r--   0        0        0      607 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/E-n22-k4.vrp.txt
--rw-r--r--   0        0        0      671 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/EdgeWeightsNoExplicit.txt
--rw-r--r--   0        0        0      668 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/EdgeWeightsNotFullMatrix.txt
--rw-r--r--   0        0        0      389 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/FileWithUnknownSection.txt
--rw-r--r--   0        0        0      191 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/MoreThanOneDepot.txt
--rw-r--r--   0        0        0      371 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/NonZeroDepotDemand.txt
--rw-r--r--   0        0        0      371 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/NonZeroDepotOpenTimeWindow.txt
--rw-r--r--   0        0        0      371 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/NonZeroDepotServiceDuration.txt
--rw-r--r--   0        0        0      675 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/OkSmall.txt
--rw-r--r--   0        0        0      697 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/OkSmallGreedyRepair.txt
--rw-r--r--   0        0        0      347 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/RC208.sol
--rw-r--r--   0        0        0     7524 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/RC208.txt
--rw-r--r--   0        0        0      369 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/TimeWindowOpenLargerThanClose.txt
--rw-r--r--   0        0        0      187 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/UnknownEdgeWeightFmt.txt
--rw-r--r--   0        0        0      154 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/data/UnknownEdgeWeightType.txt
--rw-r--r--   0        0        0     1263 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/helpers.py
--rw-r--r--   0        0        0     3738 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_GeneticAlgorithm.py
--rw-r--r--   0        0        0     8610 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_Individual.py
--rw-r--r--   0        0        0     1214 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_Matrix.py
--rw-r--r--   0        0        0    10199 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_PenaltyManager.py
--rw-r--r--   0        0        0    11320 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_Population.py
--rw-r--r--   0        0        0      499 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_ProblemData.py
--rw-r--r--   0        0        0     2752 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_Result.py
--rw-r--r--   0        0        0     1025 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_Statistics.py
--rw-r--r--   0        0        0     5523 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_SubPopulation.py
--rw-r--r--   0        0        0     1955 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_TimeWindowSegment.py
--rw-r--r--   0        0        0     1101 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_XorShift128.py
--rw-r--r--   0        0        0     6219 2023-03-01 19:49:38.379853 pyvrp-0.1.0/pyvrp/tests/test_read.py
--rw-r--r--   0        0        0     3491 1970-01-01 00:00:00.000000 pyvrp-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1082 2023-05-13 19:41:45.381572 pyvrp-0.2.1/LICENSE
+-rw-r--r--   0        0        0     2102 2023-05-13 19:41:45.381572 pyvrp-0.2.1/README.md
+-rw-r--r--   0        0        0     3248 2023-05-13 19:41:45.381572 pyvrp-0.2.1/build_extensions.py
+-rw-r--r--   0        0        0     4855 2023-05-13 19:41:45.405573 pyvrp-0.2.1/meson.build
+-rw-r--r--   0        0        0      150 2023-05-13 19:41:45.405573 pyvrp-0.2.1/meson_options.txt
+-rw-r--r--   0        0        0     3502 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0     7123 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/GeneticAlgorithm.py
+-rw-r--r--   0        0        0     8810 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/PenaltyManager.py
+-rw-r--r--   0        0        0     6144 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/Population.py
+-rw-r--r--   0        0        0     2872 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/Result.py
+-rw-r--r--   0        0        0     6197 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/Statistics.py
+-rw-r--r--   0        0        0      799 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_CostEvaluator.pyi
+-rw-r--r--   0        0        0     4129 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_Individual.pyi
+-rw-r--r--   0        0        0      465 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_Matrix.pyi
+-rw-r--r--   0        0        0     4877 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_ProblemData.pyi
+-rw-r--r--   0        0        0     4021 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_SubPopulation.pyi
+-rw-r--r--   0        0        0     1885 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_TimeWindowSegment.pyi
+-rw-r--r--   0        0        0      267 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/_XorShift128.pyi
+-rw-r--r--   0        0        0      513 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/__init__.py
+-rw-r--r--   0        0        0     8916 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cli.py
+-rw-r--r--   0        0        0      715 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/CostEvaluator.cpp
+-rw-r--r--   0        0        0     2194 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/CostEvaluator.h
+-rw-r--r--   0        0        0      711 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/CostEvaluator_bindings.cpp
+-rw-r--r--   0        0        0     6093 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/Individual.cpp
+-rw-r--r--   0        0        0     3819 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/Individual.h
+-rw-r--r--   0        0        0     2291 2023-05-13 19:41:45.405573 pyvrp-0.2.1/pyvrp/cpp/Individual_bindings.cpp
+-rw-r--r--   0        0        0     2484 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/Matrix.h
+-rw-r--r--   0        0        0      909 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/Matrix_bindings.cpp
+-rw-r--r--   0        0        0     1565 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/ProblemData.cpp
+-rw-r--r--   0        0        0     3605 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/ProblemData.h
+-rw-r--r--   0        0        0     2246 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/ProblemData_bindings.cpp
+-rw-r--r--   0        0        0      574 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/README.md
+-rw-r--r--   0        0        0     4784 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/SubPopulation.cpp
+-rw-r--r--   0        0        0     3115 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/SubPopulation.h
+-rw-r--r--   0        0        0     2750 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/SubPopulation_bindings.cpp
+-rw-r--r--   0        0        0     3349 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/TimeWindowSegment.h
+-rw-r--r--   0        0        0     1215 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/TimeWindowSegment_bindings.cpp
+-rw-r--r--   0        0        0      581 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/XorShift128.cpp
+-rw-r--r--   0        0        0     2017 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/XorShift128.h
+-rw-r--r--   0        0        0      467 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/XorShift128_bindings.cpp
+-rw-r--r--   0        0        0     2822 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/crossover/crossover.cpp
+-rw-r--r--   0        0        0     1925 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/crossover/crossover.h
+-rw-r--r--   0        0        0     8549 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/crossover/selective_route_exchange.cpp
+-rw-r--r--   0        0        0      375 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/crossover/selective_route_exchange_bindings.cpp
+-rw-r--r--   0        0        0     1007 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/diversity/broken_pairs_distance.cpp
+-rw-r--r--   0        0        0      254 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/diversity/broken_pairs_distance_bindings.cpp
+-rw-r--r--   0        0        0      659 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/diversity/diversity.h
+-rw-r--r--   0        0        0     3011 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/CircleSector.h
+-rw-r--r--   0        0        0    11332 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Exchange.h
+-rw-r--r--   0        0        0     2173 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Exchange_bindings.cpp
+-rw-r--r--   0        0        0    10040 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch.cpp
+-rw-r--r--   0        0        0     3281 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch.h
+-rw-r--r--   0        0        0     2513 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearchOperator.h
+-rw-r--r--   0        0        0     1420 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch_bindings.cpp
+-rw-r--r--   0        0        0     3633 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/MoveTwoClientsReversed.cpp
+-rw-r--r--   0        0        0      481 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/MoveTwoClientsReversed.h
+-rw-r--r--   0        0        0      482 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/MoveTwoClientsReversed_bindings.cpp
+-rw-r--r--   0        0        0      669 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Node.cpp
+-rw-r--r--   0        0        0     1561 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Node.h
+-rw-r--r--   0        0        0     1112 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/RelocateStar.cpp
+-rw-r--r--   0        0        0      735 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/RelocateStar.h
+-rw-r--r--   0        0        0      436 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/RelocateStar_bindings.cpp
+-rw-r--r--   0        0        0     3651 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Route.cpp
+-rw-r--r--   0        0        0     4897 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/Route.h
+-rw-r--r--   0        0        0    10591 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/SwapStar.cpp
+-rw-r--r--   0        0        0     3186 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/SwapStar.h
+-rw-r--r--   0        0        0      420 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/SwapStar_bindings.cpp
+-rw-r--r--   0        0        0     4113 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/TwoOpt.cpp
+-rw-r--r--   0        0        0      895 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/TwoOpt.h
+-rw-r--r--   0        0        0      409 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/cpp/educate/TwoOpt_bindings.cpp
+-rw-r--r--   0        0        0       63 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/crossover/__init__.py
+-rw-r--r--   0        0        0      374 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/crossover/_selective_route_exchange.pyi
+-rw-r--r--   0        0        0     1853 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/crossover/selective_route_exchange.py
+-rw-r--r--   0        0        0     8425 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/crossover/tests/test_selective_route_exchange.py
+-rw-r--r--   0        0        0      115 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diagnostics/__init__.py
+-rw-r--r--   0        0        0     3825 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diagnostics/get_route_statistics.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diagnostics/tests/__init__.py
+-rw-r--r--   0        0        0        7 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diagnostics/tests/test_get_route_statistics.py
+-rw-r--r--   0        0        0       58 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diversity/__init__.py
+-rw-r--r--   0        0        0     1462 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diversity/_broken_pairs_distance.pyi
+-rw-r--r--   0        0        0     1305 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/diversity/tests/test_broken_pairs_distance.py
+-rw-r--r--   0        0        0     6601 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/LocalSearch.py
+-rw-r--r--   0        0        0      896 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_Exchange.pyi
+-rw-r--r--   0        0        0      880 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_LocalSearch.pyi
+-rw-r--r--   0        0        0      204 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_MoveTwoClientsReversed.pyi
+-rw-r--r--   0        0        0      196 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_RelocateStar.pyi
+-rw-r--r--   0        0        0      192 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_SwapStar.pyi
+-rw-r--r--   0        0        0      188 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/_TwoOpt.pyi
+-rw-r--r--   0        0        0      708 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/__init__.py
+-rw-r--r--   0        0        0     5045 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/neighbourhood.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/__init__.py
+-rw-r--r--   0        0        0     9129 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_Exchange.py
+-rw-r--r--   0        0        0     5461 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_LocalSearch.py
+-rw-r--r--   0        0        0     2714 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_MoveTwoClientsReversed.py
+-rw-r--r--   0        0        0     3145 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_RelocateStar.py
+-rw-r--r--   0        0        0     3027 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_SwapStar.py
+-rw-r--r--   0        0        0     2141 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_TwoOpt.py
+-rw-r--r--   0        0        0     5350 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/educate/tests/test_neighbourhood.py
+-rw-r--r--   0        0        0      206 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/exceptions.py
+-rw-r--r--   0        0        0      436 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/__init__.py
+-rw-r--r--   0        0        0     1106 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_coordinates.py
+-rw-r--r--   0        0        0     1046 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_demands.py
+-rw-r--r--   0        0        0     1199 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_diversity.py
+-rw-r--r--   0        0        0     1129 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_instance.py
+-rw-r--r--   0        0        0     2344 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_objectives.py
+-rw-r--r--   0        0        0     1608 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_result.py
+-rw-r--r--   0        0        0     4732 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_route_schedule.py
+-rw-r--r--   0        0        0     1136 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_runtimes.py
+-rw-r--r--   0        0        0     1844 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_solution.py
+-rw-r--r--   0        0        0     1226 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/plot_time_windows.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/tests/__init__.py
+-rw-r--r--   0        0        0    47981 2023-05-13 19:41:45.409572 pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_instance.png
+-rw-r--r--   0        0        0   141297 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_result.png
+-rw-r--r--   0        0        0    35194 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_route_schedule.png
+-rw-r--r--   0        0        0    25609 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution.png
+-rw-r--r--   0        0        0    43058 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution_with_customers.png
+-rw-r--r--   0        0        0     3108 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/plotting/tests/test_plotting.py
+-rw-r--r--   0        0        0     5543 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/read.py
+-rw-r--r--   0        0        0     1048 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/show_versions.py
+-rw-r--r--   0        0        0      444 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/MaxIterations.py
+-rw-r--r--   0        0        0      589 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/MaxRuntime.py
+-rw-r--r--   0        0        0      819 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/NoImprovement.py
+-rw-r--r--   0        0        0      573 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/StoppingCriterion.py
+-rw-r--r--   0        0        0      575 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/TimedNoImprovement.py
+-rw-r--r--   0        0        0      217 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/__init__.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/tests/__init__.py
+-rw-r--r--   0        0        0      839 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/tests/test_MaxIterations.py
+-rw-r--r--   0        0        0     1031 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/tests/test_MaxRuntime.py
+-rw-r--r--   0        0        0     1777 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/tests/test_NoImprovement.py
+-rw-r--r--   0        0        0     1292 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/stop/tests/test_TimedNoImprovement.py
+-rw-r--r--   0        0        0        0 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/__init__.py
+-rw-r--r--   0        0        0      189 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/DepotNotOne.txt
+-rw-r--r--   0        0        0      607 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/E-n22-k4.txt
+-rw-r--r--   0        0        0      671 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/EdgeWeightsNoExplicit.txt
+-rw-r--r--   0        0        0      668 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/EdgeWeightsNotFullMatrix.txt
+-rw-r--r--   0        0        0      389 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/FileWithUnknownSection.txt
+-rw-r--r--   0        0        0      191 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/MoreThanOneDepot.txt
+-rw-r--r--   0        0        0      371 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/NonZeroDepotDemand.txt
+-rw-r--r--   0        0        0      371 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/NonZeroDepotOpenTimeWindow.txt
+-rw-r--r--   0        0        0      371 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/NonZeroDepotServiceDuration.txt
+-rw-r--r--   0        0        0      675 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/OkSmall.txt
+-rw-r--r--   0        0        0      697 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/OkSmallGreedyRepair.txt
+-rw-r--r--   0        0        0      347 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/RC208.sol
+-rw-r--r--   0        0        0     7524 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/RC208.txt
+-rw-r--r--   0        0        0      369 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/TimeWindowOpenLargerThanClose.txt
+-rw-r--r--   0        0        0      187 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/UnknownEdgeWeightFmt.txt
+-rw-r--r--   0        0        0      154 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/data/UnknownEdgeWeightType.txt
+-rw-r--r--   0        0        0     1256 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/helpers.py
+-rw-r--r--   0        0        0     3914 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_CostEvaluator.py
+-rw-r--r--   0        0        0     7641 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_GeneticAlgorithm.py
+-rw-r--r--   0        0        0     8829 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_Individual.py
+-rw-r--r--   0        0        0     1190 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_Matrix.py
+-rw-r--r--   0        0        0     9864 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_PenaltyManager.py
+-rw-r--r--   0        0        0    12487 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_Population.py
+-rw-r--r--   0        0        0     3000 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_ProblemData.py
+-rw-r--r--   0        0        0     2743 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_Result.py
+-rw-r--r--   0        0        0     1148 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_Statistics.py
+-rw-r--r--   0        0        0     5918 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_SubPopulation.py
+-rw-r--r--   0        0        0     1913 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_TimeWindowSegment.py
+-rw-r--r--   0        0        0     1101 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_XorShift128.py
+-rw-r--r--   0        0        0     6306 2023-05-13 19:41:45.413573 pyvrp-0.2.1/pyvrp/tests/test_read.py
+-rw-r--r--   0        0        0     3477 1970-01-01 00:00:00.000000 pyvrp-0.2.1/PKG-INFO
```

### Comparing `pyvrp-0.1.0/LICENSE` & `pyvrp-0.2.1/LICENSE`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2022, Paper authors
+Copyright (c) since 2022, PyVRP contributors
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `pyvrp-0.1.0/README.md` & `pyvrp-0.2.1/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [![PyPI version](https://badge.fury.io/py/pyvrp.svg)](https://badge.fury.io/py/pyvrp)
-[![CI](https://github.com/N-Wouda/pyvrp/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/N-Wouda/pyvrp/actions/workflows/CI.yml)
+[![CI](https://github.com/PyVRP/PyVRP/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/PyVRP/PyVRP/actions/workflows/CI.yml)
 [![Documentation Status](https://readthedocs.org/projects/pyvrp/badge/?version=latest)](https://pyvrp.readthedocs.io/en/latest/?badge=latest)
-[![codecov](https://codecov.io/gh/N-Wouda/pyvrp/branch/main/graph/badge.svg?token=G9JKIVZOHB)](https://codecov.io/gh/N-Wouda/pyvrp)
+[![codecov](https://codecov.io/gh/PyVRP/PyVRP/branch/main/graph/badge.svg?token=G9JKIVZOHB)](https://codecov.io/gh/PyVRP/PyVRP)
 
 # PyVRP
 
 The `pyvrp` package is an open-source, state-of-the-art vehicle routing problem solver.
 
 `pyvrp` may be installed in the usual way as
 ```
```

### Comparing `pyvrp-0.1.0/build_extensions.py` & `pyvrp-0.2.1/build_extensions.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/meson.build` & `pyvrp-0.2.1/meson.build`

 * *Files 6% similar despite different names*

```diff
@@ -43,19 +43,20 @@
 endif
 
 # We first compile a common library that contains all regular, C++ code. This
 # is then linked against by the extension modules. We also define source and
 # installation directories here, as a shorthand.
 INST_DIR = 'pyvrp'
 SRC_DIR = 'pyvrp' / 'cpp'
+INCLUDES = [include_directories(SRC_DIR)]
 
 libcommon = static_library(
     'common',
     [
-        SRC_DIR / 'PenaltyManager.cpp',
+        SRC_DIR / 'CostEvaluator.cpp',
         SRC_DIR / 'ProblemData.cpp',
         SRC_DIR / 'XorShift128.cpp',
         SRC_DIR / 'Individual.cpp',
         SRC_DIR / 'SubPopulation.cpp',
         SRC_DIR / 'crossover' / 'selective_route_exchange.cpp',
         SRC_DIR / 'crossover' / 'crossover.cpp',
         SRC_DIR / 'diversity' / 'broken_pairs_distance.cpp',
@@ -63,15 +64,15 @@
         SRC_DIR / 'educate' / 'Route.cpp',
         SRC_DIR / 'educate' / 'Node.cpp',
         SRC_DIR / 'educate' / 'MoveTwoClientsReversed.cpp',
         SRC_DIR / 'educate' / 'TwoOpt.cpp',
         SRC_DIR / 'educate' / 'RelocateStar.cpp',
         SRC_DIR / 'educate' / 'SwapStar.cpp',
     ],
-    include_directories: [include_directories(SRC_DIR)],
+    include_directories: INCLUDES,
 )
 
 # Next we get the extension dependencies. These are pretty simple: we only
 # depend on Python (duh!) and pybind11.
 py = import('python').find_installation()
 pybind11 = dependency('pybind11', required: false)
 
@@ -84,21 +85,22 @@
     pybind11 = find_program('pybind11-config')
     pybind11 = run_command(pybind11, ['--includes'], check: true)
     pybind11 = pybind11.stdout().split('-I')[-1].strip()
     pybind11 = declare_dependency(include_directories: [pybind11])
 endif
 
 assert(pybind11.found(), 'Could not find pybind11!')
+dependencies = [py.dependency(), pybind11]
 
 # Extension as [extension name, subdirectory]. Here 'extension name' names the
 # eventual module name and the bindings source file, and 'subdirectory' gives 
 # the source and installation directories (relative to SRC_DIR and INST_DIR).
 extensions = [
     ['Matrix', ''],
-    ['PenaltyManager', ''],
+    ['CostEvaluator', ''],
     ['ProblemData', ''],
     ['SubPopulation', ''],
     ['TimeWindowSegment', ''],
     ['XorShift128', ''],
     ['Individual', ''],
     ['selective_route_exchange', 'crossover'],
     ['broken_pairs_distance', 'diversity'],
@@ -113,16 +115,16 @@
 foreach extension : extensions  # extension[0] = name, extension[1] = subdir
     message('Going to build ' + extension[0])
 
     source_dir = '/'.join([SRC_DIR, extension[1]])
     install_dir = '/'.join([INST_DIR, extension[1]])
 
     py.extension_module(
-        '_' + extension[0], # module names are prepended by an underscore
+        '_' + extension[0],  # native extensions are prepended by an underscore
         source_dir / extension[0] + '_bindings.cpp',
-        dependencies: [py.dependency(), pybind11],
+        dependencies: dependencies,
         link_with: libcommon,
         install: true,
         subdir: install_dir,
-        include_directories: [include_directories(SRC_DIR)],
+        include_directories: INCLUDES,
     )
 endforeach
```

### Comparing `pyvrp-0.1.0/pyproject.toml` & `pyvrp-0.2.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 [tool.poetry]
 name = "pyvrp"
-version = "0.1.0"
+version = "0.2.1"
 description = "A state-of-the-art vehicle routing problem solver."
 authors = [
     "Niels Wouda <nielswouda@gmail.com>",
     "Leon Lan <leon.lanyidong@gmail.com>",
     "Wouter Kool <wouter.kool@ortec.com>",
 ]
 license = "MIT"
 readme = "README.md"
-repository = "https://github.com/N-Wouda/PyVRP"
+repository = "https://github.com/PyVRP/PyVRP"
 include = [
     { path = "LICENSE.md" },
     { path = "meson.build", format = "sdist" },
     { path = "meson_options.txt", format = "sdist" },
     { path = "build_extensions.py", format = "sdist" },
     { path = "pyvrp/**/*.so", format = "wheel" },
     { path = "pyvrp/**/*.pyd", format = "wheel" },
@@ -33,15 +33,15 @@
     "Development Status :: 5 - Production/Stable",
     "Topic :: Software Development",
     "Topic :: Scientific/Engineering",
 ]
 
 
 [tool.poetry.urls]
-"Tracker" = "https://github.com/N-Wouda/PyVRP/issues"
+"Tracker" = "https://github.com/PyVRP/PyVRP/issues"
 
 
 [tool.poetry.dependencies]
 python = "^3.8,<4.0"
 numpy = ">=1.15.2"
 matplotlib = ">=2.2.0"
 vrplib = "^1.0.0"
```

### Comparing `pyvrp-0.1.0/pyvrp/GeneticAlgorithm.py` & `pyvrp-0.2.1/pyvrp/GeneticAlgorithm.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 import time
 from dataclasses import dataclass
-from typing import Callable, Tuple
+from typing import Callable, Collection, Tuple
 
 from pyvrp.educate.LocalSearch import LocalSearch
 from pyvrp.stop import StoppingCriterion
 
+from .PenaltyManager import PenaltyManager
 from .Population import Population
 from .Result import Result
 from .Statistics import Statistics
+from ._CostEvaluator import CostEvaluator
 from ._Individual import Individual
-from ._PenaltyManager import PenaltyManager
 from ._ProblemData import ProblemData
 from ._XorShift128 import XorShift128
 
 _Parents = Tuple[Individual, Individual]
 CrossoverOperator = Callable[
-    [_Parents, ProblemData, PenaltyManager, XorShift128], Individual
+    [_Parents, ProblemData, CostEvaluator, XorShift128], Individual
 ]
 
 
 @dataclass
 class GeneticAlgorithmParams:
     repair_probability: float = 0.80
     collect_statistics: bool = False
@@ -35,52 +36,72 @@
             raise ValueError("intensify_probability must be in [0, 1].")
 
         if self.nb_iter_no_improvement < 0:
             raise ValueError("nb_iter_no_improvement < 0 not understood.")
 
 
 class GeneticAlgorithm:
+    """
+    Creates a GeneticAlgorithm instance.
+
+    Parameters
+    ----------
+    data
+        Data object describing the problem to be solved.
+    penalty_manager
+        Penalty manager to use.
+    rng
+        Random number generator.
+    population
+        Population to use.
+    local_search
+        Local search instance to use.
+    crossover_op
+        Crossover operator to use for generating offspring.
+    initial_solutions
+        Initial solutions to use to initialise the population.
+    params
+        Genetic algorithm parameters. If not provided, a default will be used.
+
+    Raises
+    ------
+    ValueError
+        When the population is empty.
+    """
+
     def __init__(
         self,
         data: ProblemData,
         penalty_manager: PenaltyManager,
         rng: XorShift128,
         population: Population,
         local_search: LocalSearch,
         crossover_op: CrossoverOperator,
+        initial_solutions: Collection[Individual],
         params: GeneticAlgorithmParams = GeneticAlgorithmParams(),
     ):
-        """
-        Creates a GeneticAlgorithm instance.
+        if len(initial_solutions) == 0:
+            raise ValueError("Expected at least one initial solution.")
 
-        Parameters
-        ----------
-        data
-            Data object describing the problem to be solved.
-        penalty_manager
-            Penalty manager to use.
-        rng
-            Random number generator.
-        local_search
-            Local search instance to use.
-        crossover_op
-            Crossover operator to use for generating offspring.
-        params, optional
-            Genetic algorithm parameters. If not provided, a default will be
-            used.
-        """
         self._data = data
         self._pm = penalty_manager
         self._rng = rng
         self._pop = population
         self._ls = local_search
         self._op = crossover_op
+        self._initial_solutions = initial_solutions
         self._params = params
 
-        self._best = Individual(data, penalty_manager, rng)
+        # Find best feasible initial solution if any exist, else set a random
+        # infeasible solution (with infinite cost) as the initial best.
+        self._best = min(initial_solutions, key=self._cost_evaluator.cost)
+
+    @property
+    def _cost_evaluator(self) -> CostEvaluator:
+        return self._pm.get_cost_evaluator()
 
     def run(self, stop: StoppingCriterion):
         """
         Runs the genetic algorithm with the provided stopping criterion.
 
         Parameters
         ----------
@@ -94,86 +115,105 @@
             A Result object, containing statistics and the best found solution.
         """
         start = time.perf_counter()
         stats = Statistics()
         iters = 0
         iters_no_improvement = 1
 
-        while not stop(self._best):
+        for individual in self._initial_solutions:
+            self._pop.add(individual, self._cost_evaluator)
+
+        while not stop(self._cost_evaluator.cost(self._best)):
             iters += 1
 
             if iters_no_improvement == self._params.nb_iter_no_improvement:
-                self._pop.restart()
                 iters_no_improvement = 1
+                self._pop.clear()
+
+                for individual in self._initial_solutions:
+                    self._pop.add(individual, self._cost_evaluator)
 
-            curr_best = self._best.cost()
+            curr_best = self._cost_evaluator.cost(self._best)
 
-            parents = self._pop.select()
-            offspring = self._op(parents, self._data, self._pm, self._rng)
+            parents = self._pop.select(self._rng, self._cost_evaluator)
+            offspring = self._op(
+                parents, self._data, self._cost_evaluator, self._rng
+            )
             self._educate(offspring)
 
-            new_best = self._best.cost()
+            new_best = self._cost_evaluator.cost(self._best)
 
             if new_best < curr_best:
                 iters_no_improvement = 1
             else:
                 iters_no_improvement += 1
 
             if self._params.collect_statistics:
-                stats.collect_from(self._pop)
+                stats.collect_from(self._pop, self._cost_evaluator)
 
         end = time.perf_counter() - start
         return Result(self._best, stats, iters, end)
 
     def _educate(self, individual: Individual):
         def is_new_best(indiv):
-            return indiv.is_feasible() and indiv.cost() < self._best.cost()
+            cost = self._cost_evaluator.cost(indiv)
+            best_cost = self._cost_evaluator.cost(self._best)
+            return cost < best_cost
 
         def add_and_register(indiv):
-            self._pop.add(indiv)
-            self._pm.register_load_feasible(not indiv.has_excess_capacity())
+            self._pop.add(indiv, self._cost_evaluator)
+            self._pm.register_load_feasible(not indiv.has_excess_load())
             self._pm.register_time_feasible(not indiv.has_time_warp())
 
         intensify_prob = self._params.intensify_probability
         should_intensify = self._rng.rand() < intensify_prob
 
-        individual = self._ls.run(individual, should_intensify)
+        individual = self._ls.run(
+            individual, self._cost_evaluator, should_intensify
+        )
 
         if is_new_best(individual):
             self._best = individual
 
             # Only intensify feasible, new best solutions. See also the repair
             # step below. TODO Refactor to on_best callback (see issue #111)
             if self._params.intensify_on_best:
                 individual = self._ls.intensify(
-                    individual, overlap_tolerance_degrees=360
+                    individual,
+                    self._cost_evaluator,
+                    overlap_tolerance_degrees=360,
                 )
 
                 if is_new_best(individual):
                     self._best = individual
 
         add_and_register(individual)
 
         # Possibly repair if current solution is infeasible. In that case, we
         # penalise infeasibility more using a penalty booster.
         if (
             not individual.is_feasible()
             and self._rng.rand() < self._params.repair_probability
         ):
-            with self._pm.get_penalty_booster():
-                should_intensify = self._rng.rand() < intensify_prob
-                individual = self._ls.run(individual, should_intensify)
-
-                if is_new_best(individual):
-                    self._best = individual
 
-                    # TODO Refactor to on_best callback (see issue #111)
-                    if self._params.intensify_on_best:
-                        individual = self._ls.intensify(
-                            individual, overlap_tolerance_degrees=360
-                        )
+            should_intensify = self._rng.rand() < intensify_prob
+            individual = self._ls.run(
+                individual,
+                self._pm.get_booster_cost_evaluator(),
+                should_intensify,
+            )
+
+            if is_new_best(individual):
+                self._best = individual
+
+                if self._params.intensify_on_best:
+                    individual = self._ls.intensify(
+                        individual,
+                        self._pm.get_booster_cost_evaluator(),
+                        overlap_tolerance_degrees=360,
+                    )
 
-                        if is_new_best(individual):
-                            self._best = individual
+                    if is_new_best(individual):
+                        self._best = individual
 
-                if individual.is_feasible():
-                    add_and_register(individual)
+            if individual.is_feasible():
+                add_and_register(individual)
```

### Comparing `pyvrp-0.1.0/pyvrp/Result.py` & `pyvrp-0.2.1/pyvrp/Result.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,12 @@
+import math
 from dataclasses import dataclass
 
 from .Statistics import Statistics
+from ._CostEvaluator import CostEvaluator
 from ._Individual import Individual
 
 
 @dataclass
 class Result:
     """
     Stores the outcomes of a single run. An instance of this class is returned
@@ -38,22 +40,25 @@
             raise ValueError("Negative number of iterations not understood.")
 
         if self.runtime < 0:
             raise ValueError("Negative runtime not understood.")
 
     def cost(self) -> float:
         """
-        Returns the cost (objective) value of the best solution.
+        Returns the cost (objective) value of the best solution. Returns inf
+        if the best solution is infeasible.
 
         Returns
         -------
         float
             Objective value.
         """
-        return self.best.cost()
+        if not self.best.is_feasible():
+            return math.inf
+        return CostEvaluator().cost(self.best)
 
     def is_feasible(self) -> bool:
         """
         Returns whether the best solution is feasible.
 
         Returns
         -------
@@ -74,20 +79,20 @@
         """
         return (
             self.num_iterations > 0
             and self.num_iterations == self.stats.num_iterations
         )
 
     def __str__(self) -> str:
+        obj_str = f"{self.cost():.2f}" if self.is_feasible() else "INFEASIBLE"
         summary = [
             "Solution results",
             "================",
             f"    # routes: {self.best.num_routes()}",
-            f"   objective: {self.cost():.2f}",
-            f"    feasible? {self.is_feasible()}",
+            f"   objective: {obj_str}",
             f"# iterations: {self.num_iterations}",
             f"    run-time: {self.runtime:.2f} seconds",
             "",
             "Routes",
             "------",
         ]
```

### Comparing `pyvrp-0.1.0/pyvrp/Statistics.py` & `pyvrp-0.2.1/pyvrp/Statistics.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 from math import nan
 from pathlib import Path
 from statistics import fmean
 from time import perf_counter
 from typing import List, Union
 
 from .Population import Population, SubPopulation
+from ._CostEvaluator import CostEvaluator
 
 _FEAS_CSV_PREFIX = "feas_"
 _INFEAS_CSV_PREFIX = "infeas_"
 
 
 @dataclass
 class _Datum:
@@ -37,52 +38,60 @@
     num_iterations: int = 0
     feas_stats: List[_Datum] = field(default_factory=list)
     infeas_stats: List[_Datum] = field(default_factory=list)
 
     def __post_init__(self):
         self._clock = perf_counter()
 
-    def collect_from(self, population: Population):
+    def collect_from(
+        self, population: Population, cost_evaluator: CostEvaluator
+    ):
         """
         Collects statistics from the given population object.
 
         Parameters
         ----------
         population
             Population instance to collect statistics from.
+        cost_evaluator
+            CostEvaluator used to compute costs for individuals.
         """
         start = self._clock
         self._clock = perf_counter()
 
         self.runtimes.append(self._clock - start)
         self.num_iterations += 1
 
         # The following lines access private members of the population, but in
         # this case that is mostly OK: we really want to have that access to
         # enable detailed statistics logging.
         feas_subpop = population._feas  # noqa
-        feas_datum = self._collect_from_subpop(feas_subpop)
+        feas_datum = self._collect_from_subpop(feas_subpop, cost_evaluator)
         self.feas_stats.append(feas_datum)
 
         infeas_subpop = population._infeas  # noqa
-        infeas_datum = self._collect_from_subpop(infeas_subpop)
+        infeas_datum = self._collect_from_subpop(infeas_subpop, cost_evaluator)
         self.infeas_stats.append(infeas_datum)
 
-    def _collect_from_subpop(self, subpop: SubPopulation) -> _Datum:
+    def _collect_from_subpop(
+        self, subpop: SubPopulation, cost_evaluator: CostEvaluator
+    ) -> _Datum:
         if not subpop:  # empty, so many statistics cannot be collected
             return _Datum(
                 size=0,
                 avg_diversity=nan,
                 best_cost=nan,
                 avg_cost=nan,
                 avg_num_routes=nan,
             )
 
         size = len(subpop)
-        costs = [item.individual.cost() for item in subpop]
+        costs = [
+            cost_evaluator.penalised_cost(item.individual) for item in subpop
+        ]
         num_routes = [item.individual.num_routes() for item in subpop]
         diversities = [item.avg_distance_closest() for item in subpop]
 
         return _Datum(
             size=size,
             avg_diversity=fmean(diversities),
             best_cost=min(costs),
```

### Comparing `pyvrp-0.1.0/pyvrp/_Individual.pyi` & `pyvrp-0.2.1/pyvrp/_Individual.pyi`

 * *Files 18% similar despite different names*

```diff
@@ -1,76 +1,55 @@
-from typing import Any, Dict, List, Tuple, overload
+from typing import Any, Dict, List, Tuple
 
-from ._PenaltyManager import PenaltyManager
 from ._ProblemData import ProblemData
 from ._XorShift128 import XorShift128
 
 class Individual:
     """
     The Individual class encodes VRP solutions.
+
+    Parameters
+    ----------
+    data
+        Data instance.
+    routes
+        Route list to use.
+
+    Raises
+    ------
+    RuntimeError
+        When the number of routes in the ``routes`` argument exceeds
+        :py:attr:`~pyvrp._ProblemData.ProblemData.num_vehicles`.
     """
 
-    @overload
     def __init__(
         self,
         data: ProblemData,
-        penalty_manager: PenaltyManager,
+        routes: List[List[int]],
+    ) -> None: ...
+    @classmethod
+    def make_random(
+        cls,
+        data: ProblemData,
         rng: XorShift128,
-    ) -> None:
+    ) -> Individual:
         """
         Creates a randomly generated Individual.
 
         Parameters
         ----------
         data
             Data instance.
-        penalty_manager
-            Penalty manager instance.
         rng
             Random number generator to use.
-        """
-    @overload
-    def __init__(
-        self,
-        data: ProblemData,
-        penalty_manager: PenaltyManager,
-        routes: List[List[int]],
-    ) -> None:
-        """
-        Creates an Individual with the given route list as its solution.
-
-        Parameters
-        ----------
-        data
-            Data instance.
-        penalty_manager
-            Penalty manager instance.
-        routes
-            Route list to use.
-
-        Raises
-        ------
-        RuntimeError
-            When the number of routes in the ``routes`` argument exceeds
-            :py:attr:`~pyvrp._ProblemData.ProblemData.num_vehicles`.
-        """
-    def cost(self) -> int:
-        """
-        Returns the current cost of the individual's solution.
-
-        .. note::
-
-           These costs depend on the current penalty values maintained by the
-           :class:`~pyvrp._PenaltyManager.PenaltyManager` used to construct the
-           individual.
 
         Returns
         -------
-        int
-            The current cost of this individual.
+        Individual
+            The randomly generated Individual.
         """
     def get_neighbours(self) -> List[Tuple[int, int]]:
         """
         Returns a list of neighbours for each client, by index. Also includes
         the depot at index 0, which only neighbours itself.
 
         Returns
@@ -94,15 +73,15 @@
         Returns
         -------
         list
             A list of routes, where each route is a list of client numbers. The
             routes each start and end at the depot (0), but that is implicit:
             the depot is not part of the returned routes.
         """
-    def has_excess_capacity(self) -> bool:
+    def has_excess_load(self) -> bool:
         """
         Returns whether this individual violates capacity constraints.
 
         Returns
         -------
         bool
             True if the individual is not capacity feasible, False otherwise.
@@ -113,18 +92,45 @@
 
         Returns
         -------
         bool
             True if the individual is not time window feasible, False
             otherwise.
         """
+    def distance(self) -> int:
+        """
+        Returns the total distance over all routes.
+
+        Returns
+        -------
+        int
+            Total distance over all routes.
+        """
+    def excess_load(self) -> int:
+        """
+        Returns the total excess load over all routes.
+
+        Returns
+        -------
+        int
+            Total excess load over all routes.
+        """
+    def time_warp(self) -> int:
+        """
+        Returns the total time warp load over all routes.
+
+        Returns
+        -------
+        int
+            Total time warp over all routes.
+        """
     def is_feasible(self) -> bool:
         """
         Whether this individual is feasible. This is a shorthand for checking
-        :meth:`~has_excess_capacity` and :meth:`~has_time_warp` both return
+        :meth:`~has_excess_load` and :meth:`~has_time_warp` both return
         false.
 
         Returns
         -------
         bool
             Whether the solution of this individual is feasible with respect to
             capacity and time window constraints.
```

### Comparing `pyvrp-0.1.0/pyvrp/_ProblemData.pyi` & `pyvrp-0.2.1/pyvrp/_ProblemData.pyi`

 * *Files 24% similar despite different names*

```diff
@@ -1,82 +1,79 @@
-from typing import Any, List, Tuple
+from typing import List
+
+from pyvrp._Matrix import Matrix
 
 class Client:
     """
-    Simple data object storing all client data as properties.
+    Simple data object storing all client data as (read-only) properties.
 
-    Attributes
+    Parameters
     ----------
-    demand
-        The amount this client's demanding.
-    service_duration
-        This client's service duration, that is, the amount of time we need to
-        visit the client for.
-    tw_early
-        Earliest time at which we can visit this client.
-    tw_late
-        Latest time at which we can visit this client.
     x
         Horizontal coordinate of this client, that is, the 'x' part of the
         client's (x, y) location tuple.
     y
         Vertical coordinate of this client, that is, the 'y' part of the
         client's (x, y) location tuple.
+    demand
+        The amount this client's demanding. Default 0.
+    service_duration
+        This client's service duration, that is, the amount of time we need to
+        visit the client for. Service should start (but not necessarily end)
+        within the [:py:attr:`~tw_early`, :py:attr:`~tw_late`] interval.
+        Default 0.
+    tw_early
+        Earliest time at which we can visit this client. Default 0.
+    tw_late
+        Latest time at which we can visit this client. Default 0.
     """
 
+    x: int
+    y: int
     demand: int
     service_duration: int
     tw_early: int
     tw_late: int
-    x: int
-    y: int
+
+    def __init__(
+        self,
+        x: int,
+        y: int,
+        demand: int = 0,
+        service_duration: int = 0,
+        tw_early: int = 0,
+        tw_late: int = 0,
+    ) -> None: ...
 
 class ProblemData:
     """
     Creates a problem data instance. This instance contains all information
     needed to solve the vehicle routing problem.
 
     Parameters
     ----------
-    coords
-        Array of (x, y) coordinates. The first coordinate at index 0 is assumed
-        to be the depot.
-    demands
-        Array of client demands. The demand at index 0 is assumed to be the
-        depot's demand, and should be zero.
+    clients
+        List of clients. The first client (at index 0) is assumed to be the
+        depot. The time window for the depot is assumed to describe the overall
+        time horizon. The depot should have 0 demand and 0 service duration.
     nb_vehicles
         The number of vehicles in this problem instance.
     vehicle_cap
         Homogenous vehicle capacity for all vehicles in the problem instance.
-    time_windows
-        Array of (early, late) time windows. The time window at index 0 is
-        assumed to be the depot's time window, and describes the overall time
-        horizon.
-    service_durations
-        Array of service durations, that is, the length of time needed to
-        service a customer upon visiting. The service duration at index 0 is
-        assumed to be the depot's service time, and should be zero.
     duration_matrix
         A matrix that gives the travel times between clients (and the depot at
-        index 0). Does not have to be symmetric.
-
-    Notes
-    -----
-    All array data assume that the data at or involving index 0 relates to the
-    depot, and all other indices specify client information.
+        index 0).
     """
 
     def __init__(
         self,
-        coords: List[Tuple[int, int]],
-        demands: List[int],
+        clients: List[Client],
         nb_vehicles: int,
         vehicle_cap: int,
-        time_windows: List[Tuple[int, int]],
-        service_durations: List[int],
+        distance_matrix: List[List[int]],
         duration_matrix: List[List[int]],
     ): ...
     def client(self, client: int) -> Client:
         """
         Returns client data for the given client.
 
         Parameters
@@ -97,14 +94,31 @@
         Returns
         -------
         Client
             A simple data object containing the depot's information.
         """
     def dist(self, first: int, second: int) -> int:
         """
+        Returns the travel distance between the first and second argument,
+        according to this instance's travel distance matrix.
+
+        Parameters
+        ----------
+        first
+            Client or depot number.
+        second
+            Client or depot number.
+
+        Returns
+        -------
+        int
+            Travel distance between the given clients.
+        """
+    def duration(self, first: int, second: int) -> int:
+        """
         Returns the travel duration between the first and second argument,
         according to this instance's travel duration matrix.
 
         Parameters
         ----------
         first
             Client or depot number.
@@ -112,22 +126,30 @@
             Client or depot number.
 
         Returns
         -------
         int
             Travel duration between the given clients.
         """
-    def distance_matrix(self) -> Any:
+    def distance_matrix(self) -> Matrix:
+        """
+        Returns the travel distance matrix used for distance computations.
+
+        Returns
+        -------
+        Matrix
+            Travel distance matrix.
+        """
+    def duration_matrix(self) -> Matrix:
         """
-        Returns the travel duration matrix used for distance/duration
-        computations.
+        Returns the travel duration matrix used for duration computations.
 
         Returns
         -------
-        Any
+        Matrix
             Travel duration matrix.
         """
     @property
     def num_clients(self) -> int:
         """
         Number of clients in this problem instance.
```

### Comparing `pyvrp-0.1.0/pyvrp/_SubPopulation.pyi` & `pyvrp-0.2.1/pyvrp/_SubPopulation.pyi`

 * *Files 20% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from typing import Iterator, List, Tuple
 
+from pyvrp._CostEvaluator import CostEvaluator
 from pyvrp._Individual import Individual
 
 class PopulationParams:
     generation_size: int
     lb_diversity: float
     min_pop_size: int
     nb_close: int
@@ -36,46 +37,80 @@
         Parameters
         ----------
         diversity_op
             Operator to use to determine pairwise diversity between solutions.
         params
             Population parameters.
         """
-    def add(self, individual: Individual) -> None:
+    def add(
+        self, individual: Individual, cost_evaluator: CostEvaluator
+    ) -> None:
         """
         Adds the given individual to the subpopulation. Survivor selection is
         automatically triggered when the population reaches its maximum size.
 
         Parameters
         ----------
         individual
             Individual to add to the subpopulation.
+        cost_evaluator
+            CostEvaluator to use to compute the cost.
         """
-    def purge(self) -> None:
+    def purge(self, cost_evaluator: CostEvaluator) -> None:
         """
         Performs survivor selection: individuals in the subpopulation are
         purged until the population is reduced to the ``min_pop_size``.
         Purging happens to duplicate solutions first, and then to solutions
         with high biased fitness.
+
+        Parameters
+        ----------
+        cost_evaluator
+            CostEvaluator to use to compute the cost.
         """
-    def update_fitness(self) -> None:
+    def update_fitness(self, cost_evaluator: CostEvaluator) -> None:
         """
         Updates the biased fitness scores of individuals in the subpopulation.
         This fitness depends on the quality of the solution (based on its cost)
         and the diversity w.r.t. to other individuals in the subpopulation.
+
+        .. warning::
+            This function must be called before accessing the
+            SubPopulationItem.fitness attribute.
         """
     def __getitem__(self, idx: int) -> SubPopulationItem: ...
     def __iter__(self) -> Iterator[SubPopulationItem]: ...
     def __len__(self) -> int: ...
 
 class SubPopulationItem:
     @property
     def fitness(self) -> float: ...
+    """
+    Fitness value for this SubPopulationItem.
+
+    Returns
+    -------
+    float
+        Fitness value for this SubPopulationItem.
+
+    .. warning::
+        This is a cached property that is not automatically updated. Before
+        accessing the property, `SubPopulation.update_fitness` should be called
+        unless the population has not changed since the last call.
+    """
     @property
     def individual(self) -> Individual: ...
+    """
+    Individual for this SubPopulationItem.
+
+    Returns
+    -------
+    Individual
+        Individual for this SubPopulationItem.
+    """
     def avg_distance_closest(self) -> float:
         """
         Determines the average distance of the individual wrapped by this item
         to a number of individuals that are most similar to it. This provides a
         measure of the relative 'diversity' of the wrapped individual.
 
         Returns
```

### Comparing `pyvrp-0.1.0/pyvrp/_TimeWindowSegment.pyi` & `pyvrp-0.2.1/pyvrp/_TimeWindowSegment.pyi`

 * *Files 20% similar despite different names*

```diff
@@ -1,29 +1,26 @@
-from typing import Union, overload
+from typing import overload
 
-from ._Matrix import DoubleMatrix, IntMatrix
+from ._Matrix import Matrix
 
 class TimeWindowSegment:
     def __init__(
         self,
-        dist: Union[DoubleMatrix, IntMatrix],
         idx_first: int,
         idx_last: int,
         duration: int,
         time_warp: int,
         tw_early: int,
         tw_late: int,
     ) -> None:
         """
         Creates a time window segment.
 
         Parameters
         ----------
-        dist
-            Matrix to use for duration computations.
         idx_first
             Index of the first customer in the route segment.
         idx_last
             Index of the last customer in the route segment.
         duration
             Total duration, including waiting time.
         time_warp
@@ -32,36 +29,40 @@
             Earliest visit moment of the first client.
         tw_late
             Latest visit moment of the last client.
         """
     @overload
     @staticmethod
     def merge(
-        arg0: TimeWindowSegment, arg1: TimeWindowSegment
+        duration_matrix: Matrix,
+        first: TimeWindowSegment,
+        second: TimeWindowSegment,
     ) -> TimeWindowSegment:
         """
         Merges two time window segments, in order.
         """
     @overload
     @staticmethod
     def merge(
-        arg0: TimeWindowSegment,
-        arg1: TimeWindowSegment,
-        arg2: TimeWindowSegment,
+        duration_matrix: Matrix,
+        first: TimeWindowSegment,
+        second: TimeWindowSegment,
+        third: TimeWindowSegment,
     ) -> TimeWindowSegment:
         """
         Merges three time window segments, in order.
         """
     @overload
     @staticmethod
     def merge(
-        arg0: TimeWindowSegment,
-        arg1: TimeWindowSegment,
-        arg2: TimeWindowSegment,
-        arg3: TimeWindowSegment,
+        duration_matrix: Matrix,
+        first: TimeWindowSegment,
+        second: TimeWindowSegment,
+        third: TimeWindowSegment,
+        fourth: TimeWindowSegment,
     ) -> TimeWindowSegment:
         """
         Merges four time window segments, in order.
         """
     def total_time_warp(self) -> int:
         """
         Returns the total time warp on this route segment.
```

### Comparing `pyvrp-0.1.0/pyvrp/cli.py` & `pyvrp-0.2.1/pyvrp/cli.py`

 * *Files 4% similar despite different names*

```diff
@@ -12,14 +12,15 @@
     msg = "Install 'tqdm' and 'tomli' to use the command line program."
     raise ModuleNotFoundError(msg)
 
 import pyvrp.educate
 from pyvrp import (
     GeneticAlgorithm,
     GeneticAlgorithmParams,
+    Individual,
     PenaltyManager,
     PenaltyParams,
     Population,
     PopulationParams,
     Result,
     XorShift128,
 )
@@ -123,34 +124,41 @@
 
     pen_params = PenaltyParams(**config.get("penalty", {}))
     pop_params = PopulationParams(**config.get("population", {}))
     nb_params = NeighbourhoodParams(**config.get("neighbourhood", {}))
 
     data = read(data_loc, instance_format, round_func)
     rng = XorShift128(seed=seed)
-    pen_manager = PenaltyManager(data.vehicle_capacity, pen_params)
-    pop = Population(data, pen_manager, rng, bpd, pop_params)
+    pen_manager = PenaltyManager(pen_params)
+    pop = Population(bpd, params=pop_params)
+
     neighbours = compute_neighbours(data, nb_params)
-    ls = LocalSearch(data, pen_manager, rng, neighbours)
+    ls = LocalSearch(data, rng, neighbours)
 
     node_ops = NODE_OPERATORS
     if "node_ops" in config:
         node_ops = [getattr(pyvrp.educate, op) for op in config["node_ops"]]
 
     for op in node_ops:
-        ls.add_node_operator(op(data, pen_manager))
+        ls.add_node_operator(op(data))
 
     route_ops = ROUTE_OPERATORS
     if "route_ops" in config:
         route_ops = [getattr(pyvrp.educate, op) for op in config["route_ops"]]
 
     for op in route_ops:
-        ls.add_route_operator(op(data, pen_manager))
+        ls.add_route_operator(op(data))
 
-    algo = GeneticAlgorithm(data, pen_manager, rng, pop, ls, srex, gen_params)
+    init = [
+        Individual.make_random(data, rng)
+        for _ in range(pop_params.min_pop_size)
+    ]
+    algo = GeneticAlgorithm(
+        data, pen_manager, rng, pop, ls, srex, init, gen_params
+    )
 
     if max_runtime is not None:
         stop = MaxRuntime(max_runtime)
     else:
         assert max_iterations is not None
         stop = MaxIterations(max_iterations)  # type: ignore
 
@@ -179,15 +187,15 @@
     """
     res = solve(instance, **kwargs)
     instance_name = Path(instance).stem
 
     return (
         instance_name,
         "Y" if res.is_feasible() else "N",
-        int(res.cost()),
+        round(res.cost(), 2),
         res.num_iterations,
         round(res.runtime, 3),
     )
 
 
 def benchmark(instances: List[str], **kwargs):
     """
@@ -212,15 +220,15 @@
 
     tqdm_kwargs = dict(max_workers=kwargs.get("num_procs", 1), unit="instance")
     data = process_map(func, func_args, **tqdm_kwargs)
 
     dtypes = [
         ("inst", "U37"),
         ("ok", "U1"),
-        ("obj", int),
+        ("obj", float),
         ("iters", int),
         ("time", float),
     ]
 
     data = np.asarray(data, dtype=dtypes)
     headers = ["Instance", "OK", "Obj.", "Iters. (#)", "Time (s)"]
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/Individual.cpp` & `pyvrp-0.2.1/pyvrp/cpp/Individual.cpp`

 * *Files 8% similar despite different names*

```diff
@@ -5,137 +5,132 @@
 #include <numeric>
 #include <vector>
 
 using Client = int;
 using Route = std::vector<Client>;
 using Routes = std::vector<Route>;
 
-void Individual::evaluateCompleteCost()
+void Individual::evaluate(ProblemData const &data)
 {
-    // TODO simplify implementation
-    nbRoutes = 0;
-    distance = 0;
-    capacityExcess = 0;
-    timeWarp = 0;
+    numRoutes_ = 0;
+    distance_ = 0;
+    excessLoad_ = 0;
+    timeWarp_ = 0;
 
     for (auto const &route : routes_)
     {
         if (route.empty())  // First empty route. All subsequent routes are
             break;          // empty as well.
 
-        nbRoutes++;
+        numRoutes_++;
 
-        int rDist = data->dist(0, route[0]);
-        int rTimeWarp = 0;
+        int routeDist = data.dist(0, route[0]);
+        int routeTimeWarp = 0;
+        int routeLoad = data.client(route[0]).demand;
 
-        int load = data->client(route[0]).demand;
-        int time = rDist;
+        int time = data.duration(0, route[0]);
 
-        if (time < data->client(route[0]).twEarly)
-            time = data->client(route[0]).twEarly;
+        if (time < data.client(route[0]).twEarly)
+            time = data.client(route[0]).twEarly;
 
-        if (time > data->client(route[0]).twLate)
+        if (time > data.client(route[0]).twLate)
         {
-            rTimeWarp += time - data->client(route[0]).twLate;
-            time = data->client(route[0]).twLate;
+            routeTimeWarp += time - data.client(route[0]).twLate;
+            time = data.client(route[0]).twLate;
         }
 
         for (size_t idx = 1; idx < route.size(); idx++)
         {
-            // Sum the rDist, load, serviceDuration and time associated with the
-            // vehicle traveling from the depot to the next client
-            rDist += data->dist(route[idx - 1], route[idx]);
-            load += data->client(route[idx]).demand;
+            routeDist += data.dist(route[idx - 1], route[idx]);
+            routeLoad += data.client(route[idx]).demand;
 
-            time += data->client(route[idx - 1]).serviceDuration
-                    + data->dist(route[idx - 1], route[idx]);
+            time += data.client(route[idx - 1]).serviceDuration
+                    + data.duration(route[idx - 1], route[idx]);
 
             // Add possible waiting time
-            if (time < data->client(route[idx]).twEarly)
-                time = data->client(route[idx]).twEarly;
+            if (time < data.client(route[idx]).twEarly)
+                time = data.client(route[idx]).twEarly;
 
             // Add possible time warp
-            if (time > data->client(route[idx]).twLate)
+            if (time > data.client(route[idx]).twLate)
             {
-                rTimeWarp += time - data->client(route[idx]).twLate;
-                time = data->client(route[idx]).twLate;
+                routeTimeWarp += time - data.client(route[idx]).twLate;
+                time = data.client(route[idx]).twLate;
             }
         }
 
         // For the last client, the successors is the depot. Also update the
         // rDist and time
-        rDist += data->dist(route.back(), 0);
-        time += data->client(route.back()).serviceDuration
-                + data->dist(route.back(), 0);
+        routeDist += data.dist(route.back(), 0);
+        time += data.client(route.back()).serviceDuration
+                + data.duration(route.back(), 0);
 
         // For the depot, we only need to check the end of the time window
         // (add possible time warp)
-        rTimeWarp += std::max(time - data->depot().twLate, 0);
+        routeTimeWarp += std::max(time - data.depot().twLate, 0);
 
         // Whole solution stats
-        distance += rDist;
-        timeWarp += rTimeWarp;
+        distance_ += routeDist;
+        timeWarp_ += routeTimeWarp;
 
-        if (static_cast<size_t>(load) > data->vehicleCapacity())
-            capacityExcess += load - data->vehicleCapacity();
+        if (static_cast<size_t>(routeLoad) > data.vehicleCapacity())
+            excessLoad_ += routeLoad - data.vehicleCapacity();
     }
 }
 
-size_t Individual::cost() const
-{
-    auto const load = data->vehicleCapacity() + capacityExcess;
-    auto const loadPenalty = penaltyManager->loadPenalty(load);
-    auto const twPenalty = penaltyManager->twPenalty(timeWarp);
-
-    return distance + loadPenalty + twPenalty;
-}
-
-size_t Individual::numRoutes() const { return nbRoutes; }
+size_t Individual::numRoutes() const { return numRoutes_; }
 
 Routes const &Individual::getRoutes() const { return routes_; }
 
 std::vector<std::pair<Client, Client>> const &Individual::getNeighbours() const
 {
     return neighbours;
 }
 
 bool Individual::isFeasible() const
 {
-    return !hasExcessCapacity() && !hasTimeWarp();
+    return !hasExcessLoad() && !hasTimeWarp();
 }
 
-bool Individual::hasExcessCapacity() const { return capacityExcess > 0; }
+bool Individual::hasExcessLoad() const { return excessLoad_ > 0; }
+
+bool Individual::hasTimeWarp() const { return timeWarp_ > 0; }
+
+size_t Individual::distance() const { return distance_; }
+
+size_t Individual::excessLoad() const { return excessLoad_; }
 
-bool Individual::hasTimeWarp() const { return timeWarp > 0; }
+size_t Individual::timeWarp() const { return timeWarp_; }
 
 void Individual::makeNeighbours()
 {
     neighbours[0] = {0, 0};  // note that depot neighbours have no meaning
 
     for (auto const &route : routes_)
         for (size_t idx = 0; idx != route.size(); ++idx)
             neighbours[route[idx]]
                 = {idx == 0 ? 0 : route[idx - 1],                  // pred
                    idx == route.size() - 1 ? 0 : route[idx + 1]};  // succ
 }
 
 bool Individual::operator==(Individual const &other) const
 {
-    // First compare costs, since that's a quick and cheap check. Only when
-    // the costs are the same do we test if the neighbours are all equal.
-    return cost() == other.cost() && neighbours == other.neighbours;
+    // First compare simple attributes, since that's a quick and cheap check.
+    // Only when these are the same we test if the neighbours are all equal.
+    // clang-format off
+    return distance_ == other.distance_
+        && excessLoad_ == other.excessLoad_
+        && timeWarp_ == other.timeWarp_
+        && numRoutes_ == other.numRoutes_
+        && neighbours == other.neighbours;
+    // clang-format on
 }
 
-Individual::Individual(ProblemData const &data,
-                       PenaltyManager const &penaltyManager,
-                       XorShift128 &rng)
-    : data(&data),
-      penaltyManager(&penaltyManager),
-      routes_(data.numVehicles()),
-      neighbours(data.numClients() + 1)
+Individual::Individual(ProblemData const &data, XorShift128 &rng)
+    : routes_(data.numVehicles()), neighbours(data.numClients() + 1)
 {
     // Shuffle clients (to create random routes)
     auto clients = std::vector<int>(data.numClients());
     std::iota(clients.begin(), clients.end(), 1);
     std::shuffle(clients.begin(), clients.end(), rng);
 
     // Distribute clients evenly over the routes: the total number of clients
@@ -145,53 +140,48 @@
     auto const perVehicle = std::max(numClients / numVehicles, size_t(1));
     auto const perRoute = perVehicle + (numClients % numVehicles != 0);
 
     for (size_t idx = 0; idx != numClients; ++idx)
         routes_[idx / perRoute].push_back(clients[idx]);
 
     makeNeighbours();
-    evaluateCompleteCost();
+    evaluate(data);
 }
 
-Individual::Individual(ProblemData const &data,
-                       PenaltyManager const &penaltyManager,
-                       Routes routes)
-    : data(&data),
-      penaltyManager(&penaltyManager),
-      routes_(std::move(routes)),
-      neighbours(data.numClients() + 1)
+Individual::Individual(ProblemData const &data, Routes routes)
+    : routes_(std::move(routes)), neighbours(data.numClients() + 1)
 {
-    if (routes_.size() > static_cast<size_t>(data.numVehicles()))
+    if (routes_.size() > data.numVehicles())
     {
         auto const msg = "Number of routes must not exceed number of vehicles.";
         throw std::runtime_error(msg);
     }
 
     // Expand to at least numVehicles routes, where any newly inserted routes
-    // will be empty. 
-    routes_.resize(static_cast<size_t>(data.numVehicles()));
+    // will be empty.
+    routes_.resize(data.numVehicles());
 
     // a precedes b only when a is not empty and b is. Combined with a stable
     // sort, this ensures we keep the original sorting as much as possible, but
     // also make sure all empty routes are at the end of routes_.
     auto comp = [](auto &a, auto &b) { return !a.empty() && b.empty(); };
     std::stable_sort(routes_.begin(), routes_.end(), comp);
 
     makeNeighbours();
-    evaluateCompleteCost();
+    evaluate(data);
 }
 
 std::ostream &operator<<(std::ostream &out, Individual const &indiv)
 {
     auto const &routes = indiv.getRoutes();
 
     for (size_t rIdx = 0; rIdx != indiv.numRoutes(); ++rIdx)
     {
         out << "Route #" << rIdx + 1 << ":";  // route number
         for (int cIdx : routes[rIdx])
             out << " " << cIdx;  // client index
         out << '\n';
     }
 
-    out << "Cost: " << indiv.cost() << '\n';
+    out << "Distance: " << indiv.distance() << '\n';
     return out;
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/Individual.h` & `pyvrp-0.2.1/pyvrp/cpp/Individual.h`

 * *Files 9% similar despite different names*

```diff
@@ -1,49 +1,40 @@
 #ifndef INDIVIDUAL_H
 #define INDIVIDUAL_H
 
-#include "PenaltyManager.h"
 #include "ProblemData.h"
 #include "XorShift128.h"
 
 #include <string>
 #include <vector>
 
 class Individual
 {
     friend struct std::hash<Individual>;  // friend struct to enable hashing
 
     using Client = int;
     using Route = std::vector<Client>;
     using Routes = std::vector<Route>;
 
-    size_t nbRoutes = 0;        // Number of routes
-    size_t distance = 0;        // Total distance
-    size_t capacityExcess = 0;  // Total excess load over all routes
-    size_t timeWarp = 0;        // All route time warp of late arrivals
+    size_t numRoutes_ = 0;   // Number of routes
+    size_t distance_ = 0;    // Total distance
+    size_t excessLoad_ = 0;  // Total excess load over all routes
+    size_t timeWarp_ = 0;    // Total time warp over all routes
 
-    ProblemData const *data;
-    PenaltyManager const *penaltyManager;
-
-    Routes routes_;  // Routes - only the first nbRoutes are non-empty
+    Routes routes_;  // Routes - only the first numRoutes_ are non-empty
     std::vector<std::pair<Client, Client>> neighbours;  // pairs of [pred, succ]
 
     // Determines the [pred, succ] pairs for each client.
     void makeNeighbours();
 
-    // Evaluates this solution's objective value.
-    void evaluateCompleteCost();
+    // Evaluates this solution's characteristics.
+    void evaluate(ProblemData const &data);
 
 public:
     /**
-     * Returns this individual's objective (penalized cost).
-     */
-    [[nodiscard]] size_t cost() const;
-
-    /**
      * Returns the number of non-empty routes in this individual's solution.
      * Such non-empty routes are guaranteed to be in the lower indices of the
      * routes returned by ``getRoutes``.
      */
     [[nodiscard]] size_t numRoutes() const;
 
     /**
@@ -62,68 +53,77 @@
      * @return True when this solution is feasible; false otherwise.
      */
     [[nodiscard]] bool isFeasible() const;
 
     /**
      * @return True if the solution violates load constraints.
      */
-    [[nodiscard]] bool hasExcessCapacity() const;
+    [[nodiscard]] bool hasExcessLoad() const;
 
     /**
      * @return True if the solution violates time window constraints.
      */
     [[nodiscard]] bool hasTimeWarp() const;
 
+    /**
+     * @return Total distance over all routes.
+     */
+    [[nodiscard]] size_t distance() const;
+
+    /**
+     * @return Total excess load over all routes.
+     */
+    [[nodiscard]] size_t excessLoad() const;
+
+    /**
+     * @return Total time warp over all routes.
+     */
+    [[nodiscard]] size_t timeWarp() const;
+
     bool operator==(Individual const &other) const;
 
     Individual &operator=(Individual const &other) = delete;  // is immutable
     Individual &operator=(Individual &&other) = delete;       // is immutable
 
     Individual(Individual const &other) = default;
     Individual(Individual &&other) = default;
 
     /**
      * Constructs a random individual using the given random number generator.
      *
      * @param data           Data instance describing the problem that's being
      *                       solved.
-     * @param penaltyManager Penalty manager, used to compute the objective.
      * @param rng            Random number generator.
      */
-    Individual(ProblemData const &data,
-               PenaltyManager const &penaltyManager,
-               XorShift128 &rng);
+    Individual(ProblemData const &data, XorShift128 &rng);
 
     /**
      * Constructs an individual having the given routes as its solution.
      *
      * @param data           Data instance describing the problem that's being
      *                       solved.
-     * @param penaltyManager Penalty manager, used to compute the objective.
      * @param routes         Solution's route list.
      */
-    Individual(ProblemData const &data,
-               PenaltyManager const &penaltyManager,
-               Routes routes);
+    Individual(ProblemData const &data, Routes routes);
 };
 
 // Outputs an individual into a given ostream in VRPLIB format
 std::ostream &operator<<(std::ostream &out, Individual const &indiv);
 
 namespace std
 {
 template <> struct hash<Individual>
 {
     std::size_t operator()(Individual const &individual) const
     {
         size_t res = 17;
-        res = res * 31 + std::hash<size_t>()(individual.nbRoutes);
-        res = res * 31 + std::hash<size_t>()(individual.distance);
-        res = res * 31 + std::hash<size_t>()(individual.capacityExcess);
-        res = res * 31 + std::hash<size_t>()(individual.timeWarp);
+        res = res * 31 + std::hash<size_t>()(individual.numRoutes_);
+        res = res * 31 + std::hash<size_t>()(individual.distance_);
+        res = res * 31 + std::hash<size_t>()(individual.excessLoad_);
+        res = res * 31 + std::hash<size_t>()(individual.timeWarp_);
 
         return res;
     }
 };
 }  // namespace std
 
 #endif
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/Individual_bindings.cpp` & `pyvrp-0.2.1/pyvrp/cpp/Individual_bindings.cpp`

 * *Files 27% similar despite different names*

```diff
@@ -7,53 +7,54 @@
 #include <sstream>
 
 namespace py = pybind11;
 
 PYBIND11_MODULE(_Individual, m)
 {
     py::class_<Individual>(m, "Individual")
-        .def(py::init<ProblemData &, PenaltyManager &, XorShift128 &>(),
+        .def(py::init<ProblemData const &, std::vector<std::vector<int>>>(),
              py::arg("data"),
-             py::arg("penalty_manager"),
-             py::arg("rng"),
-             py::keep_alive<1, 2>(),  // keep data and penalty_manager alive
-             py::keep_alive<1, 3>())  // at least until individual is freed
-        .def(py::init<ProblemData &,
-                      PenaltyManager &,
-                      std::vector<std::vector<int>>>(),
-             py::arg("data"),
-             py::arg("penalty_manager"),
-             py::arg("routes"),
-             py::keep_alive<1, 2>(),  // keep data and penalty_manager alive
-             py::keep_alive<1, 3>())  // at least until individual is freed
-        .def("cost", &Individual::cost)
+             py::arg("routes"))
+        .def_property_readonly_static(
+            "make_random",                // this is a bit of a workaround for
+            [](py::object)                // classmethods, because pybind does
+            {                             // not yet support those natively.
+                return py::cpp_function(  // See issue 1693 in the pybind repo.
+                    [](ProblemData const &data, XorShift128 &rng) {
+                        return Individual(data, rng);
+                    },
+                    py::arg("data"),
+                    py::arg("rng"));
+            })
         .def("num_routes", &Individual::numRoutes)
         .def("get_routes",
              &Individual::getRoutes,
              py::return_value_policy::reference_internal)
         .def("get_neighbours",
              &Individual::getNeighbours,
              py::return_value_policy::reference_internal)
         .def("is_feasible", &Individual::isFeasible)
-        .def("has_excess_capacity", &Individual::hasExcessCapacity)
+        .def("has_excess_load", &Individual::hasExcessLoad)
         .def("has_time_warp", &Individual::hasTimeWarp)
+        .def("distance", &Individual::distance)
+        .def("excess_load", &Individual::excessLoad)
+        .def("time_warp", &Individual::timeWarp)
         .def(
             "__copy__",
             [](Individual const &individual) { return Individual(individual); })
         .def(
             "__deepcopy__",
             [](Individual const &individual, py::dict) {
                 return Individual(individual);
             },
             py::arg("memo"))
         .def("__hash__",
-             [](Individual const &individual)
-             { return std::hash<Individual>()(individual); })
+             [](Individual const &individual) {
+                 return std::hash<Individual>()(individual);
+             })
         .def(pybind11::self == pybind11::self)  // this is __eq__
-        .def("__str__",
-             [](Individual const &individual)
-             {
-                 std::stringstream stream;
-                 stream << individual;
-                 return stream.str();
-             });
+        .def("__str__", [](Individual const &individual) {
+            std::stringstream stream;
+            stream << individual;
+            return stream.str();
+        });
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/Matrix.h` & `pyvrp-0.2.1/pyvrp/cpp/Matrix.h`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/Matrix_bindings.cpp` & `pyvrp-0.2.1/pyvrp/cpp/Matrix_bindings.cpp`

 * *Files 22% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 #include <pybind11/pybind11.h>
 #include <pybind11/stl.h>
 
 namespace py = pybind11;
 
 PYBIND11_MODULE(_Matrix, m)
 {
-    py::class_<Matrix<int>>(m, "IntMatrix")
+    py::class_<Matrix<int>>(m, "Matrix")
         .def(py::init<size_t>(), py::arg("dimension"))
         .def(py::init<size_t, size_t>(), py::arg("n_rows"), py::arg("n_cols"))
         .def(py::init<std::vector<std::vector<int>>>(), py::arg("data"))
         .def(
             "__getitem__",
             [](Matrix<int> &m, std::pair<size_t, size_t> idx) -> int {
                 return m(idx.first, idx.second);
@@ -22,28 +22,8 @@
             [](Matrix<int> &m, std::pair<size_t, size_t> idx, int value) {
                 m(idx.first, idx.second) = value;
             },
             py::arg("idx"),
             py::arg("value"))
         .def("max", &Matrix<int>::max)
         .def("size", &Matrix<int>::size);
-
-    py::class_<Matrix<double>>(m, "DoubleMatrix")
-        .def(py::init<size_t>(), py::arg("dimension"))
-        .def(py::init<size_t, size_t>(), py::arg("n_rows"), py::arg("n_cols"))
-        .def(py::init<std::vector<std::vector<double>>>(), py::arg("data"))
-        .def(
-            "__getitem__",
-            [](Matrix<double> &m, std::pair<size_t, size_t> idx) -> double {
-                return m(idx.first, idx.second);
-            },
-            py::arg("idx"))
-        .def(
-            "__setitem__",
-            [](Matrix<double> &m, std::pair<size_t, size_t> idx, double value) {
-                m(idx.first, idx.second) = value;
-            },
-            py::arg("idx"),
-            py::arg("value"))
-        .def("max", &Matrix<double>::max)
-        .def("size", &Matrix<double>::size);
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/ProblemData.h` & `pyvrp-0.2.1/pyvrp/cpp/ProblemData.h`

 * *Files 19% similar despite different names*

```diff
@@ -10,22 +10,30 @@
 class ProblemData
 {
 public:
     struct Client
     {
         int x;                // Coordinate X
         int y;                // Coordinate Y
-        int serviceDuration;  // Service duration
         int demand;           // Demand
+        int serviceDuration;  // Service duration
         int twEarly;          // Earliest arrival (when using time windows)
         int twLate;           // Latest arrival (when using time windows)
+
+        Client(int x,
+               int y,
+               int demand = 0,
+               int serviceDuration = 0,
+               int twEarly = 0,
+               int twLate = 0);
     };
 
 private:
     Matrix<int> const dist_;       // Distance matrix (+depot)
+    Matrix<int> const dur_;        // Duration matrix (+depot)
     std::vector<Client> clients_;  // Client (+depot) information
 
     size_t const numClients_;
     size_t const numVehicles_;
     size_t const vehicleCapacity_;
 
 public:
@@ -39,26 +47,40 @@
      * @return A struct containing the depot's information.
      */
     [[nodiscard]] Client const &depot() const;
 
     /**
      * Returns the distance between the indicated two clients.
      *
-     * @param first First client.
+     * @param first  First client.
      * @param second Second client.
      * @return distance from the first to the second client.
      */
     [[nodiscard]] inline int dist(size_t first, size_t second) const;
 
     /**
-     * @return The full distance matrix.
+     * Returns the travel duration between the indicated two clients.
+     *
+     * @param first  First client.
+     * @param second Second client.
+     * @return Travel duration from the first to the second client.
+     */
+    [[nodiscard]] inline int duration(size_t first, size_t second) const;
+
+    /**
+     * @return The full travel distance matrix.
      */
     [[nodiscard]] Matrix<int> const &distanceMatrix() const;
 
     /**
+     * @return The full travel duration matrix.
+     */
+    [[nodiscard]] Matrix<int> const &durationMatrix() const;
+
+    /**
      * @return Total number of clients in this instance.
      */
     [[nodiscard]] size_t numClients() const;
 
     /**
      * @return Total number of vehicles available in this instance.
      */
@@ -66,39 +88,40 @@
 
     /**
      * @return Capacity of each vehicle in this instance.
      */
     [[nodiscard]] size_t vehicleCapacity() const;
 
     /**
-     * Constructs a ProblemData object with the given data. Assumes the data
-     * contains the depot, such that each vector is one longer than the number
-     * of clients.
+     * Constructs a ProblemData object with the given data. Assumes the list of
+     * clients contains the depot, such that each vector is one longer than the
+     * number of clients.
      *
-     * @param coords       Coordinates as pairs of [x, y].
-     * @param demands      Client demands.
+     * @param clients      List of clients (including depot at index 0).
      * @param numVehicles  Number of vehicles.
      * @param vehicleCap   Vehicle capacity.
-     * @param timeWindows  Time windows as pairs of [early, late].
-     * @param servDurs     Service durations.
      * @param distMat      Distance matrix.
+     * @param durMat       Duration matrix.
      */
-    ProblemData(std::vector<std::pair<int, int>> const &coords,
-                std::vector<int> const &demands,
+    ProblemData(std::vector<Client> const &clients,
                 size_t numVehicles,
                 size_t vehicleCap,
-                std::vector<std::pair<int, int>> const &timeWindows,
-                std::vector<int> const &servDurs,
-                std::vector<std::vector<int>> const &distMat);
+                std::vector<std::vector<int>> const &distMat,
+                std::vector<std::vector<int>> const &durMat);
 };
 
 ProblemData::Client const &ProblemData::client(size_t client) const
 {
     return clients_[client];
 }
 
 int ProblemData::dist(size_t first, size_t second) const
 {
     return dist_(first, second);
 }
 
+int ProblemData::duration(size_t first, size_t second) const
+{
+    return dur_(first, second);
+}
+
 #endif  // HGS_PROBLEMDATA_H
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/ProblemData_bindings.cpp` & `pyvrp-0.2.1/pyvrp/cpp/ProblemData_bindings.cpp`

 * *Files 11% similar despite different names*

```diff
@@ -4,43 +4,53 @@
 #include <pybind11/stl.h>
 
 namespace py = pybind11;
 
 PYBIND11_MODULE(_ProblemData, m)
 {
     py::class_<ProblemData::Client>(m, "Client")
+        .def(py::init<int, int, int, int, int, int>(),
+             py::arg("x"),
+             py::arg("y"),
+             py::arg("demand") = 0,
+             py::arg("service_duration") = 0,
+             py::arg("tw_early") = 0,
+             py::arg("tw_late") = 0)
         .def_readonly("x", &ProblemData::Client::x)
         .def_readonly("y", &ProblemData::Client::y)
         .def_readonly("service_duration", &ProblemData::Client::serviceDuration)
         .def_readonly("demand", &ProblemData::Client::demand)
         .def_readonly("tw_early", &ProblemData::Client::twEarly)
         .def_readonly("tw_late", &ProblemData::Client::twLate);
 
     py::class_<ProblemData>(m, "ProblemData")
-        .def(py::init<std::vector<std::pair<int, int>> const &,
-                      std::vector<int> const &,
+        .def(py::init<std::vector<ProblemData::Client> const &,
                       int,
                       int,
-                      std::vector<std::pair<int, int>> const &,
-                      std::vector<int> const &,
+                      std::vector<std::vector<int>> const &,
                       std::vector<std::vector<int>> const &>(),
-             py::arg("coords"),
-             py::arg("demands"),
+             py::arg("clients"),
              py::arg("nb_vehicles"),
              py::arg("vehicle_cap"),
-             py::arg("time_windows"),
-             py::arg("service_durations"),
+             py::arg("distance_matrix"),
              py::arg("duration_matrix"))
         .def_property_readonly("num_clients", &ProblemData::numClients)
         .def_property_readonly("num_vehicles", &ProblemData::numVehicles)
         .def_property_readonly("vehicle_capacity",
                                &ProblemData::vehicleCapacity)
         .def("client",
              &ProblemData::client,
              py::arg("client"),
              py::return_value_policy::reference)
         .def("depot", &ProblemData::depot, py::return_value_policy::reference)
         .def("dist", &ProblemData::dist, py::arg("first"), py::arg("second"))
+        .def("duration",
+             &ProblemData::duration,
+             py::arg("first"),
+             py::arg("second"))
         .def("distance_matrix",
              &ProblemData::distanceMatrix,
+             py::return_value_policy::reference)
+        .def("duration_matrix",
+             &ProblemData::durationMatrix,
              py::return_value_policy::reference);
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/README.md` & `pyvrp-0.2.1/pyvrp/cpp/README.md`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/SubPopulation.cpp` & `pyvrp-0.2.1/pyvrp/cpp/SubPopulation.cpp`

 * *Files 24% similar despite different names*

```diff
@@ -10,15 +10,16 @@
 
 SubPopulation::~SubPopulation()
 {
     for (auto &item : items)
         delete item.individual;
 }
 
-void SubPopulation::add(Individual const *individual)
+void SubPopulation::add(Individual const *individual,
+                        CostEvaluator const &costEvaluator)
 {
     // Copy the given individual into a new memory location, and use that from
     // now on.
     individual = new Individual(*individual);
     Item item = {&params, individual, 0.0, {}};
 
     for (auto &other : items)  // update distance to other individuals
@@ -31,19 +32,18 @@
         oProx.emplace(place, div, individual);
 
         auto &iProx = item.proximity;
         place = std::lower_bound(iProx.begin(), iProx.end(), div, cmp);
         iProx.emplace(place, div, other.individual);
     }
 
-    items.push_back(item);  // add individual and update fitness scores for the
-    updateFitness();        // entire subpopulation.
+    items.push_back(item);  // add individual
 
     if (size() > params.maxPopSize())
-        purge();
+        purge(costEvaluator);
 }
 
 size_t SubPopulation::size() const { return items.size(); }
 
 SubPopulation::Item const &SubPopulation::operator[](size_t idx) const
 {
     return items[idx];
@@ -56,75 +56,74 @@
 
 std::vector<SubPopulation::Item>::const_iterator SubPopulation::cend() const
 {
     return items.cend();
 }
 
 void SubPopulation::remove(
-    std::vector<SubPopulation::Item>::iterator const &iterator)
+    std::vector<SubPopulation::Item>::iterator const &iterator,
+    CostEvaluator const &costEvaluator)
 {
     for (auto &[params, individual, fitness, proximity] : items)
         // Remove individual from other proximities.
         for (size_t idx = 0; idx != proximity.size(); ++idx)
             if (proximity[idx].second == iterator->individual)
             {
                 proximity.erase(proximity.begin() + idx);
                 break;
             }
 
     delete iterator->individual;  // dispose of manually allocated memory
-    items.erase(iterator);        // before the item is removed. Then update
-    updateFitness();              // the fitness scores.
+    items.erase(iterator);        // before the item is removed.
 }
 
-void SubPopulation::purge()
+void SubPopulation::purge(CostEvaluator const &costEvaluator)
 {
+    // First we remove duplicates. This does not rely on the fitness values.
     while (size() > params.minPopSize)
     {
         // Remove duplicates from the subpopulation (if they exist)
-        auto const pred = [&](auto &iterator)
-        {
+        auto const pred = [&](auto &iterator) {
             return !iterator.proximity.empty()
                    && *iterator.proximity[0].second == *iterator.individual;
         };
 
         auto const duplicate = std::find_if(items.begin(), items.end(), pred);
 
         if (duplicate == items.end())  // there are no more duplicates
             break;
 
-        remove(duplicate);
+        remove(duplicate, costEvaluator);
     }
 
     while (size() > params.minPopSize)
     {
+        // Before using fitness, we must update fitness
+        updateFitness(costEvaluator);
         auto const worstFitness = std::max_element(
-            items.begin(),
-            items.end(),
-            [](auto const &a, auto const &b) { return a.fitness < b.fitness; });
+            items.begin(), items.end(), [](auto const &a, auto const &b) {
+                return a.fitness < b.fitness;
+            });
 
-        remove(worstFitness);
+        remove(worstFitness, costEvaluator);
     }
 }
 
-// TODO this function should also be called after updating the penalties, since
-//  in that case the cost rank likely changes.
-void SubPopulation::updateFitness()
+void SubPopulation::updateFitness(CostEvaluator const &costEvaluator)
 {
     if (items.empty())
         return;
 
     std::vector<size_t> byCost(size());
     std::iota(byCost.begin(), byCost.end(), 0);
 
-    std::stable_sort(
-        byCost.begin(),
-        byCost.end(),
-        [&](size_t a, size_t b)
-        { return items[a].individual->cost() < items[b].individual->cost(); });
+    std::stable_sort(byCost.begin(), byCost.end(), [&](size_t a, size_t b) {
+        return costEvaluator.penalisedCost(*items[a].individual)
+               < costEvaluator.penalisedCost(*items[b].individual);
+    });
 
     std::vector<std::pair<double, size_t>> diversity;
     for (size_t costRank = 0; costRank != size(); costRank++)
     {
         auto const dist = items[byCost[costRank]].avgDistanceClosest();
         diversity.emplace_back(-dist, costRank);  // higher is better
     }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/SubPopulation.h` & `pyvrp-0.2.1/pyvrp/cpp/SubPopulation.h`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 #ifndef SUBPOPULATION_H
 #define SUBPOPULATION_H
 
+#include "CostEvaluator.h"
 #include "Individual.h"
 #include "diversity/diversity.h"
 
 #include <functional>
 #include <iosfwd>
 #include <stdexcept>
 #include <vector>
@@ -46,57 +47,60 @@
 
     size_t maxPopSize() const { return minPopSize + generationSize; }
 };
 
 class SubPopulation
 {
     DiversityMeasure divOp;
-    PopulationParams const &params;
+    PopulationParams const &params;  // owned by Population, on the Python side
 
 public:
     struct Item
     {
         using Proximity = std::vector<std::pair<double, Individual const *>>;
 
         PopulationParams const *params;
 
         // Note that this pointer is not owned by the Item - it is merely a
         // reference to memory owned and allocated by the SubPopulation this
         // item is part of. The SubPopulation remains responsible for managing
         // that memory.
         Individual const *individual;
+        // Fitness should be used carefully: only directly after updateFitness
+        // was called. At any other moment, it will be outdated.
         double fitness;
         Proximity proximity;
 
         double avgDistanceClosest() const;
     };
 
 private:
     std::vector<Item> items;
 
     // Removes the element at the given iterator location from the items.
-    void remove(std::vector<Item>::iterator const &iterator);
-
-    // Recomputes the fitness of all individuals maintained by this population.
-    // This is called whenever an individual is added to, or removed from, the
-    // population.
-    void updateFitness();
+    void remove(std::vector<Item>::iterator const &iterator,
+                CostEvaluator const &costEvaluator);
 
 public:
     SubPopulation(DiversityMeasure divOp, PopulationParams const &params);
 
     ~SubPopulation();
 
-    void add(Individual const *individual);
+    void add(Individual const *individual, CostEvaluator const &costEvaluator);
 
     std::vector<Item>::const_iterator cbegin() const;
 
     std::vector<Item>::const_iterator cend() const;
 
     size_t size() const;
 
     Item const &operator[](size_t idx) const;
 
-    void purge();
+    void purge(CostEvaluator const &costEvaluator);
+
+    // Recomputes the fitness of all individuals maintained by this population.
+    // This is called whenever an individual is added to, or removed from, the
+    // population.
+    void updateFitness(CostEvaluator const &costEvaluator);
 };
 
 #endif  // SUBPOPULATION_H
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/SubPopulation_bindings.cpp` & `pyvrp-0.2.1/pyvrp/cpp/SubPopulation_bindings.cpp`

 * *Files 8% similar despite different names*

```diff
@@ -28,33 +28,38 @@
         .def_readonly("individual",
                       &SubPopulation::Item::individual,
                       py::return_value_policy::reference_internal)
         .def_readonly("fitness", &SubPopulation::Item::fitness)
         .def("avg_distance_closest", &SubPopulation::Item::avgDistanceClosest);
 
     py::class_<SubPopulation>(m, "SubPopulation")
-        .def(py::init<DiversityMeasure,
-                      PopulationParams const &>(),
+        .def(py::init<DiversityMeasure, PopulationParams const &>(),
              py::arg("diversity_op"),
              py::arg("params"),
              py::keep_alive<1, 3>())  // keep params alive
-        .def("add", &SubPopulation::add, py::arg("individual"))
+        .def("add",
+             &SubPopulation::add,
+             py::arg("individual"),
+             py::arg("cost_evaluator"))
         .def("__len__", &SubPopulation::size)
         .def(
             "__getitem__",
-            [](SubPopulation const &subPop, int idx)
-            {
+            [](SubPopulation const &subPop, int idx) {
                 // int so we also support negative offsets from the end.
                 idx = idx < 0 ? subPop.size() + idx : idx;
                 if (idx < 0 || static_cast<size_t>(idx) >= subPop.size())
                     throw py::index_error();
                 return subPop[idx];
             },
             py::arg("idx"),
             py::return_value_policy::reference_internal)
         .def(
             "__iter__",
-            [](SubPopulation const &subPop)
-            { return py::make_iterator(subPop.cbegin(), subPop.cend()); },
+            [](SubPopulation const &subPop) {
+                return py::make_iterator(subPop.cbegin(), subPop.cend());
+            },
             py::return_value_policy::reference_internal)
-        .def("purge", &SubPopulation::purge);
+        .def("purge", &SubPopulation::purge, py::arg("cost_evaluator"))
+        .def("update_fitness",
+             &SubPopulation::updateFitness,
+             py::arg("cost_evaluator"));
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/TimeWindowSegment.h` & `pyvrp-0.2.1/pyvrp/cpp/TimeWindowSegment.h`

 * *Files 12% similar despite different names*

```diff
@@ -3,97 +3,94 @@
 
 #include "Matrix.h"
 
 class TimeWindowSegment
 {
     using TWS = TimeWindowSegment;
 
-    Matrix<int> const *dist = nullptr;  // Distance matrix
     int idxFirst = 0;  // Index of the first client in the segment
     int idxLast = 0;   // Index of the last client in the segment
     int duration = 0;  // Total duration, incl. waiting and servicing
     int timeWarp = 0;  // Cumulative time warp
     int twEarly = 0;   // Earliest visit moment of first client
     int twLate = 0;    // Latest visit moment of last client
 
-    [[nodiscard]] inline TWS merge(TWS const &other) const;
+    [[nodiscard]] inline TWS merge(Matrix<int> const &durationMatrix,
+                                   TWS const &other) const;
 
 public:
     template <typename... Args>
-    [[nodiscard]] inline static TWS
-    merge(TWS const &first, TWS const &second, Args... args);
+    [[nodiscard]] inline static TWS merge(Matrix<int> const &durationMatrix,
+                                          TWS const &first,
+                                          TWS const &second,
+                                          Args... args);
 
     /**
      * Total time warp, that is, the time warp along the the segment, and
      * potential time warp due to too late a release time.
      */
     [[nodiscard]] inline int totalTimeWarp() const;
 
-    TimeWindowSegment() = default;  // TODO get rid of this constructor
+    TimeWindowSegment() = default;
 
-    inline TimeWindowSegment(Matrix<int> const *dist,
-                             int idxFirst,
+    inline TimeWindowSegment(int idxFirst,
                              int idxLast,
                              int duration,
                              int timeWarp,
                              int twEarly,
                              int twLate);
 };
 
-template <typename... Args>
-TimeWindowSegment TimeWindowSegment::merge(TimeWindowSegment const &first,
-                                           TimeWindowSegment const &second,
-                                           Args... args)
+TimeWindowSegment TimeWindowSegment::merge(Matrix<int> const &durationMatrix,
+                                           TimeWindowSegment const &other) const
 {
 #ifdef VRP_NO_TIME_WINDOWS
     return {};
 #else
-    auto const res = first.merge(second);
+    auto const arcDuration = durationMatrix(idxLast, other.idxFirst);
+    auto const delta = duration - timeWarp + arcDuration;
+    auto const deltaWaitTime = std::max(other.twEarly - delta - twLate, 0);
+    auto const deltaTimeWarp = std::max(twEarly + delta - other.twLate, 0);
 
-    if constexpr (sizeof...(args) == 0)
-        return res;
-    else
-        return merge(res, args...);
+    return {idxFirst,
+            other.idxLast,
+            duration + other.duration + arcDuration + deltaWaitTime,
+            timeWarp + other.timeWarp + deltaTimeWarp,
+            std::max(other.twEarly - delta, twEarly) - deltaWaitTime,
+            std::min(other.twLate - delta, twLate) + deltaTimeWarp};
 #endif
 }
 
-TimeWindowSegment TimeWindowSegment::merge(TimeWindowSegment const &other) const
+template <typename... Args>
+TimeWindowSegment TimeWindowSegment::merge(Matrix<int> const &durationMatrix,
+                                           TimeWindowSegment const &first,
+                                           TimeWindowSegment const &second,
+                                           Args... args)
 {
 #ifdef VRP_NO_TIME_WINDOWS
     return {};
 #else
-    int const distance = (*dist)(idxLast, other.idxFirst);
-    int const delta = duration - timeWarp + distance;
-    int const deltaWaitTime = std::max(other.twEarly - delta - twLate, 0);
-    int const deltaTimeWarp = std::max(twEarly + delta - other.twLate, 0);
+    auto const res = first.merge(durationMatrix, second);
 
-    return {dist,
-            idxFirst,
-            other.idxLast,
-            duration + other.duration + distance + deltaWaitTime,
-            timeWarp + other.timeWarp + deltaTimeWarp,
-            std::max(other.twEarly - delta, twEarly) - deltaWaitTime,
-            std::min(other.twLate - delta, twLate) + deltaTimeWarp};
+    if constexpr (sizeof...(args) == 0)
+        return res;
+    else
+        return merge(durationMatrix, res, args...);
 #endif
 }
 
-int TimeWindowSegment::totalTimeWarp() const
-{
-    return timeWarp;
-}
+int TimeWindowSegment::totalTimeWarp() const { return timeWarp; }
 
-TimeWindowSegment::TimeWindowSegment(Matrix<int> const *dist,
-                                     int idxFirst,
+TimeWindowSegment::TimeWindowSegment(int idxFirst,
                                      int idxLast,
                                      int duration,
                                      int timeWarp,
                                      int twEarly,
                                      int twLate)
-    : dist(dist),
-      idxFirst(idxFirst),
+    : idxFirst(idxFirst),
       idxLast(idxLast),
       duration(duration),
       timeWarp(timeWarp),
       twEarly(twEarly),
       twLate(twLate)
 {
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/XorShift128.cpp` & `pyvrp-0.2.1/pyvrp/cpp/XorShift128.cpp`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/XorShift128.h` & `pyvrp-0.2.1/pyvrp/cpp/XorShift128.h`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #ifndef XORSHIFT128_H
 #define XORSHIFT128_H
 
 #include <climits>
-#include <cstdint>
 #include <cstddef>
+#include <cstdint>
 #include <type_traits>
 
 /**
  * This class implements a XOR-shift pseudo-random number generator. It
  * generates the next number of a sequence by repeatedly taking the 'exclusive
  * or' (the ^ operator) of a number with a bit-shifted version of itself. See
  * also here for more details: https://en.wikipedia.org/wiki/Xorshift.
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/crossover/crossover.cpp` & `pyvrp-0.2.1/pyvrp/cpp/crossover/crossover.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -13,34 +13,35 @@
     size_t offset;
 };
 
 // Evaluates the cost change of inserting client between prev and next.
 int deltaCost(Client client, Client prev, Client next, ProblemData const &data)
 {
     int prevEarliestArrival
-        = std::max(data.dist(0, prev), data.client(prev).twEarly);
+        = std::max(data.duration(0, prev), data.client(prev).twEarly);
     int prevEarliestFinish
         = prevEarliestArrival + data.client(prev).serviceDuration;
-    int distPrevClient = data.dist(prev, client);
+    int durPrevClient = data.duration(prev, client);
     int clientLate = data.client(client).twLate;
 
-    if (prevEarliestFinish + distPrevClient >= clientLate)
+    if (prevEarliestFinish + durPrevClient >= clientLate)
         return INT_MAX;
 
     int clientEarliestArrival
-        = std::max(data.dist(0, client), data.client(client).twEarly);
+        = std::max(data.duration(0, client), data.client(client).twEarly);
     int clientEarliestFinish
         = clientEarliestArrival + data.client(client).serviceDuration;
-    int distClientNext = data.dist(client, next);
+    int durClientNext = data.duration(client, next);
     int nextLate = data.client(next).twLate;
 
-    if (clientEarliestFinish + distClientNext >= nextLate)
+    if (clientEarliestFinish + durClientNext >= nextLate)
         return INT_MAX;
 
-    return distPrevClient + distClientNext - data.dist(prev, next);
+    return data.dist(prev, client) + data.dist(client, next)
+           - data.dist(prev, next);
 }
 }  // namespace
 
 void crossover::greedyRepair(Routes &routes,
                              std::vector<Client> const &unplanned,
                              ProblemData const &data)
 {
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/diversity/broken_pairs_distance.cpp` & `pyvrp-0.2.1/pyvrp/cpp/diversity/broken_pairs_distance.cpp`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/diversity/diversity.h` & `pyvrp-0.2.1/pyvrp/cpp/diversity/diversity.h`

 * *Files 2% similar despite different names*

```diff
@@ -15,11 +15,10 @@
  * [0, 1].
  *
  * @param first  First individual.
  * @param second Second individual.
  * @return The (symmetric) broken pairs distance between the two
  *         individuals.
  */
-double brokenPairsDistance(Individual const &first,
-                           Individual const &second);
+double brokenPairsDistance(Individual const &first, Individual const &second);
 
 #endif  // HGS_DIVERSITY_H
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/CircleSector.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/CircleSector.h`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/Exchange.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/SwapStar.cpp`

 * *Files 26% similar despite different names*

```diff
@@ -1,298 +1,290 @@
-#ifndef EXCHANGE_H
-#define EXCHANGE_H
-
-#include "LocalSearchOperator.h"
-#include "Node.h"
-#include "Route.h"
-#include "TimeWindowSegment.h"
-
-#include <cassert>
+#include "SwapStar.h"
 
 using TWS = TimeWindowSegment;
 
-/**
- * Template class that exchanges N consecutive nodes from U's route (starting at
- * U) with M consecutive nodes from V's route (starting at V). As special cases,
- * (1, 0) is pure relocate, and (1, 1) pure swap.
- */
-template <size_t N, size_t M> class Exchange : public LocalSearchOperator<Node>
+void SwapStar::updateRemovalCosts(Route *R1, CostEvaluator const &costEvaluator)
 {
-    using LocalSearchOperator::LocalSearchOperator;
-
-    static_assert(N >= M && N > 0, "N < M or N == 0 does not make sense");
+    auto const currTimeWarp = costEvaluator.twPenalty(R1->timeWarp());
 
-    // Tests if the segment starting at node of given length contains the depot
-    inline bool containsDepot(Node *node, size_t segLength) const;
+    for (Node *U = n(R1->depot); !U->isDepot(); U = n(U))
+    {
+        auto twData
+            = TWS::merge(data.durationMatrix(), p(U)->twBefore, n(U)->twAfter);
+        removalCosts(R1->idx, U->client)
+            = data.dist(p(U)->client, n(U)->client)
+              - data.dist(p(U)->client, U->client)
+              - data.dist(U->client, n(U)->client)
+              + costEvaluator.twPenalty(twData.totalTimeWarp()) - currTimeWarp;
+    }
+}
 
-    // Tests if the segments of U and V overlap in the same route
-    inline bool overlap(Node *U, Node *V) const;
+void SwapStar::updateInsertionCost(Route *R,
+                                   Node *U,
+                                   CostEvaluator const &costEvaluator)
+{
+    auto &insertPositions = cache(R->idx, U->client);
 
-    // Tests if the segments of U and V are adjacent in the same route
-    inline bool adjacent(Node *U, Node *V) const;
+    insertPositions = {};
+    insertPositions.shouldUpdate = false;
 
-    // Special case that's applied when M == 0
-    int evalRelocateMove(Node *U, Node *V) const;
+    // Insert cost of U just after the depot (0 -> U -> ...)
+    auto twData = TWS::merge(
+        data.durationMatrix(), R->depot->twBefore, U->tw, n(R->depot)->twAfter);
+    int cost = data.dist(0, U->client)
+               + data.dist(U->client, n(R->depot)->client)
+               - data.dist(0, n(R->depot)->client)
+               + costEvaluator.twPenalty(twData.totalTimeWarp())
+               - costEvaluator.twPenalty(R->timeWarp());
 
-    // Applied when M != 0
-    int evalSwapMove(Node *U, Node *V) const;
+    insertPositions.maybeAdd(cost, R->depot);
 
-public:
-    int evaluate(Node *U, Node *V) override;
+    for (Node *V = n(R->depot); !V->isDepot(); V = n(V))
+    {
+        // Insert cost of U just after V (V -> U -> ...)
+        twData = TWS::merge(
+            data.durationMatrix(), V->twBefore, U->tw, n(V)->twAfter);
+        int deltaCost = data.dist(V->client, U->client)
+                        + data.dist(U->client, n(V)->client)
+                        - data.dist(V->client, n(V)->client)
+                        + costEvaluator.twPenalty(twData.totalTimeWarp())
+                        - costEvaluator.twPenalty(R->timeWarp());
 
-    void apply(Node *U, Node *V) override;
-};
+        insertPositions.maybeAdd(deltaCost, V);
+    }
+}
 
-template <size_t N, size_t M>
-bool Exchange<N, M>::containsDepot(Node *node, size_t segLength) const
+std::pair<int, Node *> SwapStar::getBestInsertPoint(
+    Node *U, Node *V, CostEvaluator const &costEvaluator)
 {
-    if (node->isDepot())
-        return true;
+    auto &best_ = cache(V->route->idx, U->client);
 
-    // size() is the position of the last node in the route. So the segment
-    // must include the depot if position + move length - 1 (-1 since we're
-    // also moving the node *at* position) is larger than size().
-    return node->position + segLength - 1 > node->route->size();
-}
+    if (best_.shouldUpdate)  // then we first update the insert positions
+        updateInsertionCost(V->route, U, costEvaluator);
 
-template <size_t N, size_t M>
-bool Exchange<N, M>::overlap(Node *U, Node *V) const
-{
-    // clang-format off
-    return U->route == V->route
-        // We need max(M, 1) here because when V is the depot and M == 0, this
-        // would turn negative and wrap around to a large number.
-        && U->position <= V->position + std::max(M, size_t(1)) - 1
-        && V->position <= U->position + N - 1;
-    // clang-format on
+    for (size_t idx = 0; idx != 3; ++idx)  // only OK if V is not adjacent
+        if (best_.locs[idx] && best_.locs[idx] != V && n(best_.locs[idx]) != V)
+            return std::make_pair(best_.costs[idx], best_.locs[idx]);
+
+    // As a fallback option, we consider inserting in the place of V
+    auto const twData = TWS::merge(
+        data.durationMatrix(), p(V)->twBefore, U->tw, n(V)->twAfter);
+    int deltaCost = data.dist(p(V)->client, U->client)
+                    + data.dist(U->client, n(V)->client)
+                    - data.dist(p(V)->client, n(V)->client)
+                    + costEvaluator.twPenalty(twData.totalTimeWarp())
+                    - costEvaluator.twPenalty(V->route->timeWarp());
+
+    return std::make_pair(deltaCost, p(V));
 }
 
-template <size_t N, size_t M>
-bool Exchange<N, M>::adjacent(Node *U, Node *V) const
+void SwapStar::init(Individual const &indiv)
 {
-    if (U->route != V->route)
-        return false;
-
-    return U->position + N == V->position || V->position + M == U->position;
+    LocalSearchOperator<Route>::init(indiv);
+    std::fill(updated.begin(), updated.end(), true);
 }
 
-template <size_t N, size_t M>
-int Exchange<N, M>::evalRelocateMove(Node *U, Node *V) const
+int SwapStar::evaluate(Route *routeU,
+                       Route *routeV,
+                       CostEvaluator const &costEvaluator)
 {
-    auto const posU = U->position;
-    auto const posV = V->position;
-
-    assert(posU > 0);
+    best = {};
 
-    auto *endU = N == 1 ? U : (*U->route)[posU + N - 1];
-
-    int const current = U->route->distBetween(posU - 1, posU + N)
-                        + data.dist(V->client, n(V)->client);
-
-    int const proposed = data.dist(V->client, U->client)
-                         + U->route->distBetween(posU, posU + N - 1)
-                         + data.dist(endU->client, n(V)->client)
-                         + data.dist(p(U)->client, n(endU)->client);
-
-    int deltaCost = proposed - current;
-
-    if (U->route != V->route)
+    if (updated[routeV->idx])
     {
-        if (U->route->isFeasible() && deltaCost >= 0)
-            return deltaCost;
-
-        auto uTWS = TWS::merge(p(U)->twBefore, n(endU)->twAfter);
-
-        deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
-
-        auto const loadDiff = U->route->loadBetween(posU, posU + N - 1);
-
-        deltaCost += penaltyManager.loadPenalty(U->route->load() - loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(U->route->load());
+        updateRemovalCosts(routeV, costEvaluator);
+        updated[routeV->idx] = false;
 
-        if (deltaCost >= 0)    // if delta cost of just U's route is not enough
-            return deltaCost;  // even without V, the move will never be good
-
-        deltaCost += penaltyManager.loadPenalty(V->route->load() + loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(V->route->load());
-
-        auto vTWS = TWS::merge(V->twBefore,
-                               U->route->twBetween(posU, posU + N - 1),
-                               n(V)->twAfter);
-
-        deltaCost += penaltyManager.twPenalty(vTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(V->route->timeWarp());
+        for (size_t idx = 1; idx != data.numClients() + 1; ++idx)
+            cache(routeV->idx, idx).shouldUpdate = true;
     }
-    else  // within same route
-    {
-        auto const *route = U->route;
 
-        if (!route->hasTimeWarp() && deltaCost >= 0)
-            return deltaCost;
+    if (updated[routeU->idx])
+    {
+        updateRemovalCosts(routeU, costEvaluator);
+        updated[routeV->idx] = false;
 
-        if (posU < posV)
-        {
-            auto const tws = TWS::merge(p(U)->twBefore,
-                                        route->twBetween(posU + N, posV),
-                                        route->twBetween(posU, posU + N - 1),
-                                        n(V)->twAfter);
+        for (size_t idx = 1; idx != data.numClients() + 1; ++idx)
+            cache(routeU->idx, idx).shouldUpdate = true;
+    }
 
-            deltaCost += penaltyManager.twPenalty(tws.totalTimeWarp());
-        }
-        else
+    for (Node *U = n(routeU->depot); !U->isDepot(); U = n(U))
+        for (Node *V = n(routeV->depot); !V->isDepot(); V = n(V))
         {
-            auto const tws = TWS::merge(V->twBefore,
-                                        route->twBetween(posU, posU + N - 1),
-                                        route->twBetween(posV + 1, posU - 1),
-                                        n(endU)->twAfter);
+            int deltaCost = 0;
 
-            deltaCost += penaltyManager.twPenalty(tws.totalTimeWarp());
-        }
+            int const uDemand = data.client(U->client).demand;
+            int const vDemand = data.client(V->client).demand;
+            int const loadDiff = uDemand - vDemand;
 
-        deltaCost -= penaltyManager.twPenalty(route->timeWarp());
-    }
-
-    return deltaCost;
-}
+            deltaCost += costEvaluator.loadPenalty(routeU->load() - loadDiff,
+                                                   data.vehicleCapacity());
+            deltaCost -= costEvaluator.loadPenalty(routeU->load(),
+                                                   data.vehicleCapacity());
 
-template <size_t N, size_t M>
-int Exchange<N, M>::evalSwapMove(Node *U, Node *V) const
-{
-    auto const posU = U->position;
-    auto const posV = V->position;
+            deltaCost += costEvaluator.loadPenalty(routeV->load() + loadDiff,
+                                                   data.vehicleCapacity());
+            deltaCost -= costEvaluator.loadPenalty(routeV->load(),
+                                                   data.vehicleCapacity());
 
-    assert(posU > 0 && posV > 0);
+            deltaCost += removalCosts(routeU->idx, U->client);
+            deltaCost += removalCosts(routeV->idx, V->client);
 
-    auto *endU = N == 1 ? U : (*U->route)[posU + N - 1];
-    auto *endV = M == 1 ? V : (*V->route)[posV + M - 1];
+            if (deltaCost >= 0)  // an early filter on many moves, before doing
+                continue;        // costly work determining insertion points
 
-    int const current = U->route->distBetween(posU - 1, posU + N)
-                        + V->route->distBetween(posV - 1, posV + M);
-
-    int const proposed
-        //   p(U) -> V -> ... -> endV -> n(endU)
-        // + p(V) -> U -> ... -> endU -> n(endV)
-        = data.dist(p(U)->client, V->client)
-          + V->route->distBetween(posV, posV + M - 1)
-          + data.dist(endV->client, n(endU)->client)
-          + data.dist(p(V)->client, U->client)
-          + U->route->distBetween(posU, posU + N - 1)
-          + data.dist(endU->client, n(endV)->client);
+            auto [extraV, UAfter] = getBestInsertPoint(U, V, costEvaluator);
+            deltaCost += extraV;
 
-    int deltaCost = proposed - current;
+            if (deltaCost >= 0)  // continuing here avoids evaluating another
+                continue;        // costly insertion point below
 
-    if (U->route != V->route)
-    {
-        if (U->route->isFeasible() && V->route->isFeasible() && deltaCost >= 0)
-            return deltaCost;
+            auto [extraU, VAfter] = getBestInsertPoint(V, U, costEvaluator);
+            deltaCost += extraU;
 
-        auto uTWS = TWS::merge(p(U)->twBefore,
-                               V->route->twBetween(posV, posV + M - 1),
-                               n(endU)->twAfter);
+            if (deltaCost < best.cost)
+            {
+                best.cost = deltaCost;
 
-        deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
+                best.U = U;
+                best.UAfter = UAfter;
 
-        auto vTWS = TWS::merge(p(V)->twBefore,
-                               U->route->twBetween(posU, posU + N - 1),
-                               n(endV)->twAfter);
+                best.V = V;
+                best.VAfter = VAfter;
+            }
+        }
 
-        deltaCost += penaltyManager.twPenalty(vTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(V->route->timeWarp());
+    // It is possible for positive delta costs to turn negative when we do a
+    // complete evaluation. But in practice that almost never happens, and is
+    // not worth spending time on.
+    if (best.cost >= 0)
+        return best.cost;
+
+    // Now do a full evaluation of the proposed swap move. This includes
+    // possible time warp penalties.
+    int const current = data.dist(p(best.U)->client, best.U->client)
+                        + data.dist(best.U->client, n(best.U)->client)
+                        + data.dist(p(best.V)->client, best.V->client)
+                        + data.dist(best.V->client, n(best.V)->client);
 
-        auto const loadU = U->route->loadBetween(posU, posU + N - 1);
-        auto const loadV = V->route->loadBetween(posV, posV + M - 1);
-        auto const loadDiff = loadU - loadV;
+    int const proposed = data.dist(best.VAfter->client, best.V->client)
+                         + data.dist(best.UAfter->client, best.U->client);
 
-        deltaCost += penaltyManager.loadPenalty(U->route->load() - loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(U->route->load());
+    int deltaCost = proposed - current;
 
-        deltaCost += penaltyManager.loadPenalty(V->route->load() + loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(V->route->load());
+    if (best.VAfter == p(best.U))
+    {
+        // Insert in place of U
+        deltaCost += data.dist(best.V->client, n(best.U)->client);
     }
-    else  // within same route
+    else
     {
-        auto const *route = U->route;
-
-        if (!route->hasTimeWarp() && deltaCost >= 0)
-            return deltaCost;
-
-        if (posU < posV)
-        {
-            auto const tws = TWS::merge(p(U)->twBefore,
-                                        route->twBetween(posV, posV + M - 1),
-                                        route->twBetween(posU + N, posV - 1),
-                                        route->twBetween(posU, posU + N - 1),
-                                        n(endV)->twAfter);
-
-            deltaCost += penaltyManager.twPenalty(tws.totalTimeWarp());
-        }
-        else
-        {
-            auto const tws = TWS::merge(p(V)->twBefore,
-                                        route->twBetween(posU, posU + N - 1),
-                                        route->twBetween(posV + M, posU - 1),
-                                        route->twBetween(posV, posV + M - 1),
-                                        n(endU)->twAfter);
+        deltaCost += data.dist(best.V->client, n(best.VAfter)->client)
+                     + data.dist(p(best.U)->client, n(best.U)->client)
+                     - data.dist(best.VAfter->client, n(best.VAfter)->client);
+    }
 
-            deltaCost += penaltyManager.twPenalty(tws.totalTimeWarp());
-        }
+    if (best.UAfter == p(best.V))
+        // Insert in place of V
+        deltaCost += data.dist(best.U->client, n(best.V)->client);
+    else
+        deltaCost += data.dist(best.U->client, n(best.UAfter)->client)
+                     + data.dist(p(best.V)->client, n(best.V)->client)
+                     - data.dist(best.UAfter->client, n(best.UAfter)->client);
+
+    // It is not possible to have UAfter == V or VAfter == U, so the positions
+    // are always strictly different
+    if (best.VAfter->position + 1 == best.U->position)
+    {
+        // Special case
+        auto uTWS = TWS::merge(data.durationMatrix(),
+                               best.VAfter->twBefore,
+                               best.V->tw,
+                               n(best.U)->twAfter);
 
-        deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
+        deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
     }
+    else if (best.VAfter->position < best.U->position)
+    {
+        auto uTWS = TWS::merge(
+            data.durationMatrix(),
+            best.VAfter->twBefore,
+            best.V->tw,
+            routeU->twBetween(best.VAfter->position + 1, best.U->position - 1),
+            n(best.U)->twAfter);
 
-    return deltaCost;
-}
+        deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
+    }
+    else
+    {
+        auto uTWS = TWS::merge(
+            data.durationMatrix(),
+            p(best.U)->twBefore,
+            routeU->twBetween(best.U->position + 1, best.VAfter->position),
+            best.V->tw,
+            n(best.VAfter)->twAfter);
 
-template <size_t N, size_t M> int Exchange<N, M>::evaluate(Node *U, Node *V)
-{
-    if (containsDepot(U, N) || overlap(U, V))
-        return 0;
+        deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
+    }
 
-    if constexpr (M > 0)
-        if (containsDepot(V, M))
-            return 0;
+    if (best.UAfter->position + 1 == best.V->position)
+    {
+        // Special case
+        auto vTWS = TWS::merge(data.durationMatrix(),
+                               best.UAfter->twBefore,
+                               best.U->tw,
+                               n(best.V)->twAfter);
 
-    if constexpr (M == 0)  // special case where nothing in V is moved
+        deltaCost += costEvaluator.twPenalty(vTWS.totalTimeWarp());
+    }
+    else if (best.UAfter->position < best.V->position)
     {
-        if (U == n(V))
-            return 0;
+        auto vTWS = TWS::merge(
+            data.durationMatrix(),
+            best.UAfter->twBefore,
+            best.U->tw,
+            routeV->twBetween(best.UAfter->position + 1, best.V->position - 1),
+            n(best.V)->twAfter);
 
-        return evalRelocateMove(U, V);
+        deltaCost += costEvaluator.twPenalty(vTWS.totalTimeWarp());
     }
     else
     {
-        if constexpr (N == M)  // symmetric, so only have to evaluate this once
-            if (U->client >= V->client)
-                return 0;
-
-        if (adjacent(U, V))
-            return 0;
+        auto vTWS = TWS::merge(
+            data.durationMatrix(),
+            p(best.V)->twBefore,
+            routeV->twBetween(best.V->position + 1, best.UAfter->position),
+            best.U->tw,
+            n(best.UAfter)->twAfter);
 
-        return evalSwapMove(U, V);
+        deltaCost += costEvaluator.twPenalty(vTWS.totalTimeWarp());
     }
-}
 
-template <size_t N, size_t M> void Exchange<N, M>::apply(Node *U, Node *V)
-{
-    auto *uToInsert = N == 1 ? U : (*U->route)[U->position + N - 1];
-    auto *insertUAfter = M == 0 ? V : (*V->route)[V->position + M - 1];
+    deltaCost -= costEvaluator.twPenalty(routeU->timeWarp());
+    deltaCost -= costEvaluator.twPenalty(routeV->timeWarp());
 
-    // Insert these 'extra' nodes of U after the end of V...
-    for (size_t count = 0; count != N - M; ++count)
-    {
-        auto *prev = p(uToInsert);
-        uToInsert->insertAfter(insertUAfter);
-        uToInsert = prev;
-    }
+    auto const uDemand = data.client(best.U->client).demand;
+    auto const vDemand = data.client(best.V->client).demand;
+
+    deltaCost += costEvaluator.loadPenalty(routeU->load() - uDemand + vDemand,
+                                           data.vehicleCapacity());
+    deltaCost
+        -= costEvaluator.loadPenalty(routeU->load(), data.vehicleCapacity());
+
+    deltaCost += costEvaluator.loadPenalty(routeV->load() + uDemand - vDemand,
+                                           data.vehicleCapacity());
+    deltaCost
+        -= costEvaluator.loadPenalty(routeV->load(), data.vehicleCapacity());
 
-    // ...and swap the overlapping nodes!
-    for (size_t count = 0; count != std::min(N, M); ++count)
+    return deltaCost;
+}
+
+void SwapStar::apply(Route *U, Route *V) const
+{
+    if (best.U && best.UAfter && best.V && best.VAfter)
     {
-        U->swapWith(V);
-        U = n(U);
-        V = n(V);
+        best.U->insertAfter(best.UAfter);
+        best.V->insertAfter(best.VAfter);
     }
 }
 
-#endif  // EXCHANGE_H
+void SwapStar::update(Route *U) { updated[U->idx] = true; }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -2,82 +2,84 @@
 
 #include <algorithm>
 #include <numeric>
 #include <set>
 #include <stdexcept>
 #include <vector>
 
-Individual LocalSearch::search(Individual &individual)
+Individual LocalSearch::search(Individual &individual,
+                               CostEvaluator const &costEvaluator)
 {
     loadIndividual(individual);
 
     // Shuffling the order beforehand adds diversity to the search
     std::shuffle(orderNodes.begin(), orderNodes.end(), rng);
     std::shuffle(nodeOps.begin(), nodeOps.end(), rng);
 
     if (nodeOps.empty())
         throw std::runtime_error("No known node operators.");
 
-    // Caches the last time nodes were tested for modification (uses nbMoves to
+    // Caches the last time nodes were tested for modification (uses numMoves to
     // track this). The lastModified field, in contrast, track when a route was
     // last *actually* modified.
     std::vector<int> lastTestedNodes(data.numClients() + 1, -1);
     lastModified = std::vector<int>(data.numVehicles(), 0);
 
     searchCompleted = false;
-    nbMoves = 0;
+    numMoves = 0;
 
     for (int step = 0; !searchCompleted; ++step)
     {
         searchCompleted = true;
 
         // Node operators are evaluated at neighbouring (U, V) pairs.
         for (auto const uClient : orderNodes)
         {
             auto *U = &clients[uClient];
             auto const lastTestedNode = lastTestedNodes[uClient];
-            lastTestedNodes[uClient] = nbMoves;
+            lastTestedNodes[uClient] = numMoves;
 
             // Shuffling the neighbours in this loop should not matter much as
             // we are already randomizing the nodes U.
             for (auto const vClient : neighbours[uClient])
             {
                 auto *V = &clients[vClient];
 
                 if (lastModified[U->route->idx] > lastTestedNode
                     || lastModified[V->route->idx] > lastTestedNode)
                 {
-                    if (applyNodeOps(U, V))
+                    if (applyNodeOps(U, V, costEvaluator))
                         continue;
 
-                    if (p(V)->isDepot() && applyNodeOps(U, p(V)))
+                    if (p(V)->isDepot() && applyNodeOps(U, p(V), costEvaluator))
                         continue;
                 }
             }
 
             // Empty route moves are not tested in the first iteration to avoid
             // increasing the fleet size too much.
             if (step > 0)
             {
                 auto pred = [](auto const &route) { return route.empty(); };
                 auto empty = std::find_if(routes.begin(), routes.end(), pred);
 
                 if (empty == routes.end())
                     continue;
 
-                if (applyNodeOps(U, empty->depot))
+                if (applyNodeOps(U, empty->depot, costEvaluator))
                     continue;
             }
         }
     }
 
     return exportIndividual();
 }
 
 Individual LocalSearch::intensify(Individual &individual,
+                                  CostEvaluator const &costEvaluator,
                                   int overlapToleranceDegrees)
 {
     loadIndividual(individual);
 
     auto const overlapTolerance = overlapToleranceDegrees * 65536;
 
     // Shuffling the order beforehand adds diversity to the search
@@ -87,72 +89,77 @@
     if (routeOps.empty())
         throw std::runtime_error("No known route operators.");
 
     std::vector<int> lastTestedRoutes(data.numVehicles(), -1);
     lastModified = std::vector<int>(data.numVehicles(), 0);
 
     searchCompleted = false;
-    nbMoves = 0;
+    numMoves = 0;
 
     while (!searchCompleted)
     {
         searchCompleted = true;
 
         for (int const rU : orderRoutes)
         {
             auto &U = routes[rU];
 
             if (U.empty())
                 continue;
 
             auto const lastTested = lastTestedRoutes[U.idx];
-            lastTestedRoutes[U.idx] = nbMoves;
+            lastTestedRoutes[U.idx] = numMoves;
 
             // Shuffling in this loop should not matter much as we are
             // already randomizing the routes U.
             for (int rV = 0; rV != U.idx; ++rV)
             {
                 auto &V = routes[rV];
 
                 if (V.empty() || !U.overlapsWith(V, overlapTolerance))
                     continue;
 
                 auto const lastModifiedRoute
                     = std::max(lastModified[U.idx], lastModified[V.idx]);
 
-                if (lastModifiedRoute > lastTested && applyRouteOps(&U, &V))
+                if (lastModifiedRoute > lastTested
+                    && applyRouteOps(&U, &V, costEvaluator))
                     continue;
             }
         }
     }
 
     return exportIndividual();
 }
 
-bool LocalSearch::applyNodeOps(Node *U, Node *V)
+bool LocalSearch::applyNodeOps(Node *U,
+                               Node *V,
+                               CostEvaluator const &costEvaluator)
 {
     for (auto *nodeOp : nodeOps)
-        if (nodeOp->evaluate(U, V) < 0)
+        if (nodeOp->evaluate(U, V, costEvaluator) < 0)
         {
             auto *routeU = U->route;  // copy pointers because the operator can
             auto *routeV = V->route;  // modify the node's route membership
 
             nodeOp->apply(U, V);
             update(routeU, routeV);
 
             return true;
         }
 
     return false;
 }
 
-bool LocalSearch::applyRouteOps(Route *U, Route *V)
+bool LocalSearch::applyRouteOps(Route *U,
+                                Route *V,
+                                CostEvaluator const &costEvaluator)
 {
     for (auto *routeOp : routeOps)
-        if (routeOp->evaluate(U, V) < 0)
+        if (routeOp->evaluate(U, V, costEvaluator) < 0)
         {
             routeOp->apply(U, V);
             update(U, V);
 
             for (auto *op : routeOps)  // this is used by some route operators
             {                          // (particularly SWAP*) to keep caches
                 op->update(U);         // in sync.
@@ -163,32 +170,31 @@
         }
 
     return false;
 }
 
 void LocalSearch::update(Route *U, Route *V)
 {
-    nbMoves++;
+    numMoves++;
     searchCompleted = false;
 
     U->update();
-    lastModified[U->idx] = nbMoves;
+    lastModified[U->idx] = numMoves;
 
     if (U != V)
     {
         V->update();
-        lastModified[V->idx] = nbMoves;
+        lastModified[V->idx] = numMoves;
     }
 }
 
 void LocalSearch::loadIndividual(Individual const &individual)
 {
     for (size_t client = 0; client <= data.numClients(); client++)
-        clients[client].tw = {&data.distanceMatrix(),
-                              static_cast<int>(client),  // TODO cast
+        clients[client].tw = {static_cast<int>(client),  // TODO cast
                               static_cast<int>(client),  // TODO cast
                               data.client(client).serviceDuration,
                               0,
                               data.client(client).twEarly,
                               data.client(client).twLate};
 
     auto const &routesIndiv = individual.getRoutes();
@@ -202,18 +208,16 @@
         startDepot->next = endDepot;
 
         endDepot->prev = startDepot;
         endDepot->next = startDepot;
 
         startDepot->tw = clients[0].tw;
         startDepot->twBefore = clients[0].tw;
-        startDepot->twAfter = clients[0].tw;
 
         endDepot->tw = clients[0].tw;
-        endDepot->twBefore = clients[0].tw;
         endDepot->twAfter = clients[0].tw;
 
         Route *route = &routes[r];
 
         if (!routesIndiv[r].empty())
         {
             Node *client = &clients[routesIndiv[r][0]];
@@ -242,37 +246,28 @@
 
     for (auto *routeOp : routeOps)
         routeOp->init(individual);
 }
 
 Individual LocalSearch::exportIndividual()
 {
-    std::vector<std::pair<double, int>> routePolarAngles;
-    routePolarAngles.reserve(data.numVehicles());
-
-    for (size_t r = 0; r < data.numVehicles(); r++)
-        routePolarAngles.emplace_back(routes[r].angleCenter, r);
-
-    // Empty routes have a large center angle, and thus always sort at the end
-    std::sort(routePolarAngles.begin(), routePolarAngles.end());
-
     std::vector<std::vector<int>> indivRoutes(data.numVehicles());
 
     for (size_t r = 0; r < data.numVehicles(); r++)
     {
-        Node *node = startDepots[routePolarAngles[r].second].next;
+        Node *node = startDepots[r].next;
 
         while (!node->isDepot())
         {
             indivRoutes[r].push_back(node->client);
             node = node->next;
         }
     }
 
-    return {data, penaltyManager, indivRoutes};
+    return {data, indivRoutes};
 }
 
 void LocalSearch::addNodeOperator(NodeOp &op) { nodeOps.emplace_back(&op); }
 
 void LocalSearch::addRouteOperator(RouteOp &op) { routeOps.emplace_back(&op); }
 
 void LocalSearch::setNeighbours(Neighbours neighbours)
@@ -302,49 +297,40 @@
 
     this->neighbours = neighbours;
 }
 
 LocalSearch::Neighbours LocalSearch::getNeighbours() { return neighbours; }
 
 LocalSearch::LocalSearch(ProblemData &data,
-                         PenaltyManager &penaltyManager,
                          XorShift128 &rng,
                          Neighbours neighbours)
     : data(data),
-      penaltyManager(penaltyManager),
       rng(rng),
       neighbours(data.numClients() + 1),
       orderNodes(data.numClients()),
       orderRoutes(data.numVehicles()),
-      lastModified(data.numVehicles(), -1)
+      lastModified(data.numVehicles(), -1),
+      clients(data.numClients() + 1),
+      routes(data.numVehicles(), data),
+      startDepots(data.numVehicles()),
+      endDepots(data.numVehicles())
 {
     setNeighbours(neighbours);
 
     std::iota(orderNodes.begin(), orderNodes.end(), 1);
     std::iota(orderRoutes.begin(), orderRoutes.end(), 0);
 
-    clients = std::vector<Node>(data.numClients() + 1);
-    routes = std::vector<Route>(data.numVehicles());
-    startDepots = std::vector<Node>(data.numVehicles());
-    endDepots = std::vector<Node>(data.numVehicles());
-
     for (size_t i = 0; i <= data.numClients(); i++)
-    {
-        clients[i].data = &data;
         clients[i].client = i;
-    }
 
     for (size_t i = 0; i < data.numVehicles(); i++)
     {
-        routes[i].data = &data;
         routes[i].idx = i;
         routes[i].depot = &startDepots[i];
 
-        startDepots[i].data = &data;
         startDepots[i].client = 0;
         startDepots[i].route = &routes[i];
 
-        startDepots[i].data = &data;
         endDepots[i].client = 0;
         endDepots[i].route = &routes[i];
     }
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch.h`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #ifndef LOCALSEARCH_H
 #define LOCALSEARCH_H
 
+#include "CostEvaluator.h"
 #include "Individual.h"
 #include "LocalSearchOperator.h"
 #include "Node.h"
-#include "PenaltyManager.h"
 #include "ProblemData.h"
 #include "Route.h"
 #include "XorShift128.h"
 
 #include <functional>
 #include <stdexcept>
 #include <vector>
@@ -16,46 +16,47 @@
 class LocalSearch
 {
     using NodeOp = LocalSearchOperator<Node>;
     using RouteOp = LocalSearchOperator<Route>;
     using Neighbours = std::vector<std::vector<int>>;
 
     ProblemData &data;
-    PenaltyManager &penaltyManager;
     XorShift128 &rng;
 
     // Neighborhood restrictions: For each client, list of nearby clients (size
     // nbClients + 1, but nothing stored for the depot!)
     Neighbours neighbours;
 
     std::vector<int> orderNodes;   // random node order used in RI operators
     std::vector<int> orderRoutes;  // random route order used in SWAP* operators
 
     std::vector<int> lastModified;  // tracks when routes were last modified
 
-    std::vector<Node> clients;      // Note that clients[0] is a sentinel value
+    std::vector<Node> clients;  // Note that clients[0] is a sentinel value
+    std::vector<Route> routes;
     std::vector<Node> startDepots;  // These mark the start of routes
     std::vector<Node> endDepots;    // These mark the end of routes
-    std::vector<Route> routes;
 
     std::vector<NodeOp *> nodeOps;
     std::vector<RouteOp *> routeOps;
 
-    int nbMoves = 0;               // Operator counter
+    int numMoves = 0;              // Operator counter
     bool searchCompleted = false;  // No further improving move found?
 
     // Load an initial solution that we will attempt to improve
     void loadIndividual(Individual const &individual);
 
     // Export the LS solution back into an individual
     Individual exportIndividual();
 
-    [[nodiscard]] bool applyNodeOps(Node *U, Node *V);
+    [[nodiscard]] bool
+    applyNodeOps(Node *U, Node *V, CostEvaluator const &costEvaluator);
 
-    [[nodiscard]] bool applyRouteOps(Route *U, Route *V);
+    [[nodiscard]] bool
+    applyRouteOps(Route *U, Route *V, CostEvaluator const &costEvaluator);
 
     // Updates solution state after an improving local search move
     void update(Route *U, Route *V);
 
 public:
     /**
      * Adds a local search operator that works on node/client pairs U and V.
@@ -80,24 +81,23 @@
      */
     Neighbours getNeighbours();
 
     /**
      * Performs regular (node-based) local search around the given individual,
      * and returns a new, hopefully improved individual.
      */
-    Individual search(Individual &individual);
+    Individual search(Individual &individual,
+                      CostEvaluator const &costEvaluator);
 
     /**
      * Performs a more intensive local search around the given individual,
      * using route-based operators and subpath enumeration. Returns a new,
      * hopefully improved individual.
      */
     Individual intensify(Individual &individual,
+                         CostEvaluator const &costEvaluator,
                          int overlapToleranceDegrees = 0);
 
-    LocalSearch(ProblemData &data,
-                PenaltyManager &penaltyManager,
-                XorShift128 &rng,
-                Neighbours neighbours);
+    LocalSearch(ProblemData &data, XorShift128 &rng, Neighbours neighbours);
 };
 
 #endif
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearchOperator.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearchOperator.h`

 * *Files 17% similar despite different names*

```diff
@@ -1,51 +1,50 @@
 #ifndef LOCALSEARCHOPERATOR_H
 #define LOCALSEARCHOPERATOR_H
 
+#include "CostEvaluator.h"
 #include "Individual.h"
-#include "PenaltyManager.h"
+#include "Node.h"
+#include "ProblemData.h"
 #include "Route.h"
 
 template <typename Arg> class LocalSearchOperatorBase
 {
     // Can only be specialised into either a Node or Route operator; there
     // are no other types that are expected to work.
     static_assert(std::is_same<Arg, Node>::value
                   || std::is_same<Arg, Route>::value);
 
 protected:
     ProblemData const &data;
-    PenaltyManager const &penaltyManager;
 
 public:
     /**
      * Determines the cost delta of applying this operator to the arguments.
      * If the cost delta is negative, this is an improving move.
      * <br />
      * The contract is as follows: if the cost delta is negative, that is the
      * true cost delta of this move. As such, improving moves are fully
      * evaluated. The operator, however, is free to return early if it knows
      * the move will never be good: that is, when it determines the cost delta
      * cannot become negative at all. In that case, the returned (non-negative)
      * cost delta does not constitute a full evaluation.
      */
-    virtual int evaluate(Arg *U, Arg *V) { return false; }
+    virtual int evaluate(Arg *U, Arg *V, CostEvaluator const &costEvaluator)
+    {
+        return 0;
+    }
 
     /**
      * Applies this operator to the given arguments. For improvements, should
      * only be called if <code>evaluate()</code> returns a negative delta cost.
      */
-    virtual void apply(Arg *U, Arg *V){};
-
-    explicit LocalSearchOperatorBase(ProblemData const &data,
-                                     PenaltyManager const &penaltyManager)
-        : data(data), penaltyManager(penaltyManager)
-    {
-    }
+    virtual void apply(Arg *U, Arg *V) const {};
 
+    LocalSearchOperatorBase(ProblemData const &data) : data(data){};
     virtual ~LocalSearchOperatorBase() = default;
 };
 
 template <typename Arg>
 class LocalSearchOperator : public LocalSearchOperatorBase<Arg>
 {
 };
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/LocalSearch_bindings.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/LocalSearch_bindings.cpp`

 * *Files 14% similar despite different names*

```diff
@@ -6,37 +6,38 @@
 
 namespace py = pybind11;
 
 PYBIND11_MODULE(_LocalSearch, m)
 {
     py::class_<LocalSearch>(m, "LocalSearch")
         .def(py::init<ProblemData &,
-                      PenaltyManager &,
                       XorShift128 &,
                       std::vector<std::vector<int>>>(),
              py::arg("data"),
-             py::arg("penalty_manager"),
              py::arg("rng"),
              py::arg("neighbours"),
-             py::keep_alive<1, 2>(),  // keep data, penalty_manager and rng
-             py::keep_alive<1, 3>(),  // alive at least until local search
-             py::keep_alive<1, 4>())  // is freed
+             py::keep_alive<1, 2>(),  // keep data and rng alive at least until
+             py::keep_alive<1, 3>())  // local search is freed
         .def("add_node_operator",
              &LocalSearch::addNodeOperator,
              py::arg("op"),
              py::keep_alive<1, 2>())
         .def("add_route_operator",
              &LocalSearch::addRouteOperator,
              py::arg("op"),
              py::keep_alive<1, 2>())
         .def("set_neighbours",
              &LocalSearch::setNeighbours,
              py::arg("neighbours"))
         .def("get_neighbours",
              &LocalSearch::getNeighbours,
              py::return_value_policy::reference_internal)
-        .def("search", &LocalSearch::search, py::arg("individual"))
+        .def("search",
+             &LocalSearch::search,
+             py::arg("individual"),
+             py::arg("cost_evaluator"))
         .def("intensify",
              &LocalSearch::intensify,
              py::arg("individual"),
+             py::arg("cost_evaluator"),
              py::arg("overlap_tolerance_degrees") = 0);
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/MoveTwoClientsReversed.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/MoveTwoClientsReversed.cpp`

 * *Files 27% similar despite different names*

```diff
@@ -1,91 +1,100 @@
 #include "MoveTwoClientsReversed.h"
-
 #include "Route.h"
 #include "TimeWindowSegment.h"
 
 using TWS = TimeWindowSegment;
 
-int MoveTwoClientsReversed::evaluate(Node *U, Node *V)
+int MoveTwoClientsReversed::evaluate(Node *U,
+                                     Node *V,
+                                     CostEvaluator const &costEvaluator)
 {
     if (U == n(V) || n(U) == V || n(U)->isDepot())
         return 0;
 
     auto const posU = U->position;
     auto const posV = V->position;
 
     int const current = U->route->distBetween(posU - 1, posU + 2)
                         + data.dist(V->client, n(V)->client);
-    int const proposed = data.dist(p(U)->client, nn(U)->client)
+    int const proposed = data.dist(p(U)->client, n(n(U))->client)
                          + data.dist(V->client, n(U)->client)
                          + data.dist(n(U)->client, U->client)
                          + data.dist(U->client, n(V)->client);
 
     int deltaCost = proposed - current;
 
     if (U->route != V->route)
     {
         if (U->route->isFeasible() && deltaCost >= 0)
             return deltaCost;
 
-        auto uTWS = TWS::merge(p(U)->twBefore, nn(U)->twAfter);
+        auto uTWS = TWS::merge(
+            data.durationMatrix(), p(U)->twBefore, n(n(U))->twAfter);
 
-        deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
+        deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
+        deltaCost -= costEvaluator.twPenalty(U->route->timeWarp());
 
         auto const loadDiff = U->route->loadBetween(posU, posU + 1);
 
-        deltaCost += penaltyManager.loadPenalty(U->route->load() - loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(U->route->load());
+        deltaCost += costEvaluator.loadPenalty(U->route->load() - loadDiff,
+                                               data.vehicleCapacity());
+        deltaCost -= costEvaluator.loadPenalty(U->route->load(),
+                                               data.vehicleCapacity());
 
         if (deltaCost >= 0)    // if delta cost of just U's route is not enough
             return deltaCost;  // even without V, the move will never be good
 
-        deltaCost += penaltyManager.loadPenalty(V->route->load() + loadDiff);
-        deltaCost -= penaltyManager.loadPenalty(V->route->load());
+        deltaCost += costEvaluator.loadPenalty(V->route->load() + loadDiff,
+                                               data.vehicleCapacity());
+        deltaCost -= costEvaluator.loadPenalty(V->route->load(),
+                                               data.vehicleCapacity());
 
-        auto vTWS = TWS::merge(V->twBefore, n(U)->tw, U->tw, n(V)->twAfter);
+        auto vTWS = TWS::merge(
+            data.durationMatrix(), V->twBefore, n(U)->tw, U->tw, n(V)->twAfter);
 
-        deltaCost += penaltyManager.twPenalty(vTWS.totalTimeWarp());
-        deltaCost -= penaltyManager.twPenalty(V->route->timeWarp());
+        deltaCost += costEvaluator.twPenalty(vTWS.totalTimeWarp());
+        deltaCost -= costEvaluator.twPenalty(V->route->timeWarp());
     }
     else  // within same route
     {
         auto const *route = U->route;
 
         if (!route->hasTimeWarp() && deltaCost >= 0)
             return deltaCost;
 
         if (posU < posV)
         {
-            auto const uTWS = TWS::merge(p(U)->twBefore,
+            auto const uTWS = TWS::merge(data.durationMatrix(),
+                                         p(U)->twBefore,
                                          route->twBetween(posU + 2, posV),
                                          n(U)->tw,
                                          U->tw,
                                          n(V)->twAfter);
 
-            deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
+            deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
         }
         else
         {
-            auto const uTWS = TWS::merge(V->twBefore,
+            auto const uTWS = TWS::merge(data.durationMatrix(),
+                                         V->twBefore,
                                          n(U)->tw,
                                          U->tw,
                                          route->twBetween(posV + 1, posU - 1),
-                                         nn(U)->twAfter);
+                                         n(n(U))->twAfter);
 
-            deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
+            deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
         }
 
-        deltaCost -= penaltyManager.twPenalty(route->timeWarp());
+        deltaCost -= costEvaluator.twPenalty(route->timeWarp());
     }
 
     return deltaCost;
 }
 
-void MoveTwoClientsReversed::apply(Node *U, Node *V)
+void MoveTwoClientsReversed::apply(Node *U, Node *V) const
 {
     auto *X = n(U);  // copy since the insert below changes n(U)
 
     U->insertAfter(V);
     X->insertAfter(V);
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/Node.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/Node.cpp`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/Node.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/Node.h`

 * *Files 8% similar despite different names*

```diff
@@ -4,23 +4,22 @@
 #include "ProblemData.h"
 #include "TimeWindowSegment.h"
 
 class Route;
 
 class Node
 {
-public:  // TODO make fields private
-    ProblemData const *data;
-
+public:               // TODO make fields private
     int client;       // Client represented with this node
     size_t position;  // Position in the route
     Node *next;       // Next node in the route order
     Node *prev;       // Previous node in the route order
     Route *route;     // Pointer towards the associated route
 
+    // TODO can these data fields be moved to Route?
     int cumulatedLoad;              // Load from depot to client (inclusive)
     int cumulatedDistance;          // Distance from depot to client (inclusive)
     int cumulatedReversalDistance;  // Distance if (0 .. client) is reversed
 
     TimeWindowSegment tw;        // TWS for individual node (client)
     TimeWindowSegment twBefore;  // TWS for (0...client) including self
     TimeWindowSegment twAfter;   // TWS for (client...0) including self
@@ -46,13 +45,8 @@
 inline Node *p(Node *node) { return node->prev; }
 
 /**
  * Convenience method accessing the node directly after the argument.
  */
 inline Node *n(Node *node) { return node->next; }
 
-/**
- * Convenience method accessing the node two positions after the argument.
- */
-inline Node *nn(Node *node) { return node->next->next; }
-
 #endif  // NODE_H
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/RelocateStar.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/RelocateStar.h`

 * *Files 22% similar despite different names*

```diff
@@ -1,14 +1,12 @@
 #ifndef RELOCATESTAR_H
 #define RELOCATESTAR_H
 
 #include "Exchange.h"
 #include "LocalSearchOperator.h"
-#include "Node.h"
-#include "Route.h"
 
 /**
  * Performs the best (1, 0)-exchange move between routes U and V. Tests both
  * ways: from U to V, and from V to U.
  */
 class RelocateStar : public LocalSearchOperator<Route>
 {
@@ -19,20 +17,19 @@
         Node *to = nullptr;
     };
 
     Exchange<1, 0> relocate;
     Move move;
 
 public:
-    int evaluate(Route *U, Route *V) override;
+    int
+    evaluate(Route *U, Route *V, CostEvaluator const &costEvaluator) override;
 
-    void apply(Route *U, Route *V) override;
+    void apply(Route *U, Route *V) const override;
 
-    explicit RelocateStar(ProblemData const &data,
-                          PenaltyManager const &penaltyManager)
-        : LocalSearchOperator<Route>(data, penaltyManager),
-          relocate(data, penaltyManager)
+    RelocateStar(ProblemData const &data)
+        : LocalSearchOperator<Route>(data), relocate(data)
     {
     }
 };
 
 #endif  // RELOCATESTAR_H
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/Route.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/Route.cpp`

 * *Files 23% similar despite different names*

```diff
@@ -2,79 +2,67 @@
 // TODO use std::numbers::pi instead of M_PI when C++20 is supported by CIBW
 
 #include "Route.h"
 
 #include <cmath>
 #include <ostream>
 
+using TWS = TimeWindowSegment;
+
+Route::Route(ProblemData const &data) : data(data) {}
+
 void Route::setupNodes()
 {
     nodes.clear();
     auto *node = depot;
 
     do
     {
         node = n(node);
         nodes.push_back(node);
     } while (!node->isDepot());
 }
 
 void Route::setupSector()
 {
-    if (empty())
-    {
-        angleCenter = 1.e30;
+    if (empty())  // Note: sector has no meaning for empty routes, don't use
         return;
-    }
 
-    auto const depotData = data->client(0);
-    auto const clientData = data->client(n(depot)->client);
+    auto const depotData = data.client(0);
+    auto const clientData = data.client(n(depot)->client);
     auto const angle = CircleSector::positive_mod(static_cast<int>(
         32768. * atan2(clientData.y - depotData.y, clientData.x - depotData.x)
         / M_PI));
 
     sector.initialize(angle);
 
-    int cumulatedX = 0;
-    int cumulatedY = 0;
-
     for (auto it = nodes.begin(); it != nodes.end() - 1; ++it)
     {
         auto const *node = *it;
         assert(!node->isDepot());
 
-        cumulatedX += data->client(node->client).x;
-        cumulatedY += data->client(node->client).y;
-
-        auto const clientData = data->client(node->client);
+        auto const clientData = data.client(node->client);
         auto const angle = CircleSector::positive_mod(static_cast<int>(
             32768.
             * atan2(clientData.y - depotData.y, clientData.x - depotData.x)
             / M_PI));
 
         sector.extend(angle);
     }
-
-    // This computes a pseudo-angle that sorts roughly equivalently to the atan2
-    // angle, but is much faster to compute. See the following post for details:
-    // https://stackoverflow.com/a/16561333/4316405.
-    auto const routeSize = static_cast<double>(size());
-    auto const dy = cumulatedY / routeSize - data->depot().y;
-    auto const dx = cumulatedX / routeSize - data->depot().x;
-    angleCenter = std::copysign(1. - dx / (std::fabs(dx) + std::fabs(dy)), dy);
 }
 
 void Route::setupRouteTimeWindows()
 {
     auto *node = nodes.back();
 
     do  // forward time window segments
     {
         auto *prev = p(node);
-        prev->twAfter = TimeWindowSegment::merge(prev->tw, node->twAfter);
+        prev->twAfter
+            = TWS::merge(data.durationMatrix(), prev->tw, node->twAfter);
         node = prev;
     } while (!node->isDepot());
 }
 
 bool Route::overlapsWith(Route const &other, int const tolerance) const
 {
     return CircleSector::overlap(sector, other.sector, tolerance);
@@ -105,32 +93,33 @@
                 reverseDistance = nodes[pos - 1]->cumulatedReversalDistance;
             }
         }
 
         if (!foundChange)
             continue;
 
-        load += data->client(node->client).demand;
-        distance += data->dist(p(node)->client, node->client);
+        load += data.client(node->client).demand;
+        distance += data.dist(p(node)->client, node->client);
 
-        reverseDistance += data->dist(node->client, p(node)->client);
-        reverseDistance -= data->dist(p(node)->client, node->client);
+        reverseDistance += data.dist(node->client, p(node)->client);
+        reverseDistance -= data.dist(p(node)->client, node->client);
 
         node->position = pos + 1;
         node->cumulatedLoad = load;
         node->cumulatedDistance = distance;
         node->cumulatedReversalDistance = reverseDistance;
-        node->twBefore = TimeWindowSegment::merge(p(node)->twBefore, node->tw);
+        node->twBefore
+            = TWS::merge(data.durationMatrix(), p(node)->twBefore, node->tw);
     }
 
     setupSector();
     setupRouteTimeWindows();
 
     load_ = nodes.back()->cumulatedLoad;
-    isLoadFeasible_ = static_cast<size_t>(load_) <= data->vehicleCapacity();
+    isLoadFeasible_ = static_cast<size_t>(load_) <= data.vehicleCapacity();
 
     timeWarp_ = nodes.back()->twBefore.totalTimeWarp();
     isTimeWarpFeasible_ = timeWarp_ == 0;
 }
 
 std::ostream &operator<<(std::ostream &out, Route const &route)
 {
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/Route.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/Route.h`

 * *Files 3% similar despite different names*

```diff
@@ -8,38 +8,37 @@
 #include <array>
 #include <bit>
 #include <cassert>
 #include <iosfwd>
 
 class Route
 {
+    ProblemData const &data;
+
     std::vector<Node *> nodes;  // List of nodes (in order) in this solution.
     CircleSector sector;        // Circle sector of the route's clients
 
     int load_;             // Current route load.
     bool isLoadFeasible_;  // Whether current load is feasible.
 
     int timeWarp_;             // Current route time warp.
     bool isTimeWarpFeasible_;  // Whether current time warp is feasible.
 
     // Populates the nodes vector.
     void setupNodes();
 
-    // Sets the angle and sector data.
+    // Sets the sector data.
     void setupSector();
 
     // Sets forward node time windows.
     void setupRouteTimeWindows();
 
-public:  // TODO make fields private
-    ProblemData const *data;
-
-    int idx;             // Route index
-    Node *depot;         // Pointer to the associated depot
-    double angleCenter;  // Angle of the barycenter of the route
+public:           // TODO make fields private
+    int idx;      // Route index
+    Node *depot;  // Pointer to the associated depot
 
     /**
      * @return The client or depot node at the given position.
      */
     [[nodiscard]] inline Node *operator[](size_t position) const;
 
     /**
@@ -50,15 +49,15 @@
     [[nodiscard]] inline bool isFeasible() const;
 
     /**
      * Determines whether this route is load-feasible.
      *
      * @return true if the route exceeds the vehicle capacity, false otherwise.
      */
-    [[nodiscard]] inline bool hasExcessCapacity() const;
+    [[nodiscard]] inline bool hasExcessLoad() const;
 
     /**
      * Determines whether this route is time-feasible.
      *
      * @return true if the route has time warp, false otherwise.
      */
     [[nodiscard]] inline bool hasTimeWarp() const;
@@ -107,22 +106,21 @@
                                     int const tolerance) const;
 
     /**
      * Updates this route. To be called after swapping nodes/changing the
      * solution.
      */
     void update();
+
+    Route(ProblemData const &data);
 };
 
-bool Route::isFeasible() const
-{
-    return !hasExcessCapacity() && !hasTimeWarp();
-}
+bool Route::isFeasible() const { return !hasExcessLoad() && !hasTimeWarp(); }
 
-bool Route::hasExcessCapacity() const { return !isLoadFeasible_; }
+bool Route::hasExcessLoad() const { return !isLoadFeasible_; }
 
 bool Route::hasTimeWarp() const
 {
 #ifdef VRP_NO_TIME_WINDOWS
     return false;
 #else
     return !isTimeWarpFeasible_;
@@ -149,15 +147,16 @@
 TimeWindowSegment Route::twBetween(size_t start, size_t end) const
 {
     assert(start <= end);
 
     auto tws = nodes[start - 1]->tw;
 
     for (size_t step = start; step != end; ++step)
-        tws = TimeWindowSegment::merge(tws, nodes[step]->tw);
+        tws = TimeWindowSegment::merge(
+            data.durationMatrix(), tws, nodes[step]->tw);
 
     return tws;
 }
 
 int Route::distBetween(size_t start, size_t end) const
 {
     assert(start <= end && end <= nodes.size());
@@ -171,15 +170,15 @@
 }
 
 int Route::loadBetween(size_t start, size_t end) const
 {
     assert(start <= end && end <= nodes.size());
 
     auto const *startNode = start == 0 ? depot : nodes[start - 1];
-    auto const atStart = data->client(startNode->client).demand;
+    auto const atStart = data.client(startNode->client).demand;
     auto const startLoad = startNode->cumulatedLoad;
     auto const endLoad = nodes[end - 1]->cumulatedLoad;
 
     assert(startLoad <= endLoad);
 
     return endLoad - startLoad + atStart;
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/SwapStar.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/SwapStar.h`

 * *Files 8% similar despite different names*

```diff
@@ -1,14 +1,12 @@
 #ifndef SWAPSTAR_H
 #define SWAPSTAR_H
 
 #include "LocalSearchOperator.h"
 #include "Matrix.h"
-#include "Node.h"
-#include "Route.h"
 
 #include <array>
 #include <vector>
 
 /**
  * Explores the SWAP* neighbourhood of [1]. The SWAP* neighbourhood explores
  * free form re-insertions of nodes U and V in the given routes (so the nodes
@@ -65,42 +63,44 @@
         Node *UAfter = nullptr;
 
         Node *V = nullptr;
         Node *VAfter = nullptr;
     };
 
     // Updates the removal costs of clients in the given route
-    void updateRemovalCosts(Route *R1);
+    void updateRemovalCosts(Route *R1, CostEvaluator const &costEvaluator);
 
     // Updates the cache storing the three best positions in the given route for
     // the passed-in node (client).
-    void updateInsertionCost(Route *R, Node *U);
+    void
+    updateInsertionCost(Route *R, Node *U, CostEvaluator const &costEvaluator);
 
     // Gets the delta cost and reinsert point for U in the route of V, assuming
     // V is removed.
-    inline std::pair<int, Node *> getBestInsertPoint(Node *U, Node *V);
+    inline std::pair<int, Node *>
+    getBestInsertPoint(Node *U, Node *V, CostEvaluator const &costEvaluator);
 
     Matrix<ThreeBest> cache;
     Matrix<int> removalCosts;
     std::vector<bool> updated;
 
     BestMove best;
 
 public:
     void init(Individual const &indiv) override;
 
-    int evaluate(Route *U, Route *V) override;
+    int
+    evaluate(Route *U, Route *V, CostEvaluator const &costEvaluator) override;
 
-    void apply(Route *U, Route *V) override;
+    void apply(Route *U, Route *V) const override;
 
     void update(Route *U) override;
 
-    explicit SwapStar(ProblemData const &data,
-                      PenaltyManager const &penaltyManager)
-        : LocalSearchOperator<Route>(data, penaltyManager),
+    explicit SwapStar(ProblemData const &data)
+        : LocalSearchOperator<Route>(data),
           cache(data.numVehicles(), data.numClients() + 1),
           removalCosts(data.numVehicles(), data.numClients() + 1),
           updated(data.numVehicles(), true)
     {
     }
 };
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/TwoOpt.cpp` & `pyvrp-0.2.1/pyvrp/cpp/educate/TwoOpt.cpp`

 * *Files 26% similar despite different names*

```diff
@@ -1,15 +1,17 @@
 #include "TwoOpt.h"
 
 #include "Route.h"
 #include "TimeWindowSegment.h"
 
 using TWS = TimeWindowSegment;
 
-int TwoOpt::evalWithinRoute(Node *U, Node *V)
+int TwoOpt::evalWithinRoute(Node *U,
+                            Node *V,
+                            CostEvaluator const &costEvaluator) const
 {
     if (U->position + 1 >= V->position)
         return 0;
 
     int deltaCost = data.dist(U->client, V->client)
                     + data.dist(n(U)->client, n(V)->client)
                     + V->cumulatedReversalDistance
@@ -20,75 +22,83 @@
     if (!U->route->hasTimeWarp() && deltaCost >= 0)
         return deltaCost;
 
     auto tws = U->twBefore;
     auto *itRoute = V;
     while (itRoute != U)
     {
-        tws = TWS::merge(tws, itRoute->tw);
+        tws = TWS::merge(data.durationMatrix(), tws, itRoute->tw);
         itRoute = p(itRoute);
     }
 
-    tws = TWS::merge(tws, n(V)->twAfter);
+    tws = TWS::merge(data.durationMatrix(), tws, n(V)->twAfter);
 
-    deltaCost += penaltyManager.twPenalty(tws.totalTimeWarp());
-    deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
+    deltaCost += costEvaluator.twPenalty(tws.totalTimeWarp());
+    deltaCost -= costEvaluator.twPenalty(U->route->timeWarp());
 
     return deltaCost;
 }
 
-int TwoOpt::evalBetweenRoutes(Node *U, Node *V)
+int TwoOpt::evalBetweenRoutes(Node *U,
+                              Node *V,
+                              CostEvaluator const &costEvaluator) const
 {
     int const current = data.dist(U->client, n(U)->client)
                         + data.dist(V->client, n(V)->client);
     int const proposed = data.dist(U->client, n(V)->client)
                          + data.dist(V->client, n(U)->client);
 
     int deltaCost = proposed - current;
 
     if (U->route->isFeasible() && V->route->isFeasible() && deltaCost >= 0)
         return deltaCost;
 
-    auto const uTWS = TWS::merge(U->twBefore, n(V)->twAfter);
+    auto const uTWS
+        = TWS::merge(data.durationMatrix(), U->twBefore, n(V)->twAfter);
 
-    deltaCost += penaltyManager.twPenalty(uTWS.totalTimeWarp());
-    deltaCost -= penaltyManager.twPenalty(U->route->timeWarp());
+    deltaCost += costEvaluator.twPenalty(uTWS.totalTimeWarp());
+    deltaCost -= costEvaluator.twPenalty(U->route->timeWarp());
 
-    auto const vTWS = TWS::merge(V->twBefore, n(U)->twAfter);
+    auto const vTWS
+        = TWS::merge(data.durationMatrix(), V->twBefore, n(U)->twAfter);
 
-    deltaCost += penaltyManager.twPenalty(vTWS.totalTimeWarp());
-    deltaCost -= penaltyManager.twPenalty(V->route->timeWarp());
+    deltaCost += costEvaluator.twPenalty(vTWS.totalTimeWarp());
+    deltaCost -= costEvaluator.twPenalty(V->route->timeWarp());
 
     int const deltaLoad = U->cumulatedLoad - V->cumulatedLoad;
 
-    deltaCost += penaltyManager.loadPenalty(U->route->load() - deltaLoad);
-    deltaCost -= penaltyManager.loadPenalty(U->route->load());
-
-    deltaCost += penaltyManager.loadPenalty(V->route->load() + deltaLoad);
-    deltaCost -= penaltyManager.loadPenalty(V->route->load());
+    deltaCost += costEvaluator.loadPenalty(U->route->load() - deltaLoad,
+                                           data.vehicleCapacity());
+    deltaCost
+        -= costEvaluator.loadPenalty(U->route->load(), data.vehicleCapacity());
+
+    deltaCost += costEvaluator.loadPenalty(V->route->load() + deltaLoad,
+                                           data.vehicleCapacity());
+    deltaCost
+        -= costEvaluator.loadPenalty(V->route->load(), data.vehicleCapacity());
 
     return deltaCost;
 }
 
-void TwoOpt::applyWithinRoute(Node *U, Node *V)
+void TwoOpt::applyWithinRoute(Node *U, Node *V) const
 {
     auto *itRoute = V;
     auto *insertionPoint = U;
     auto *currNext = n(U);
 
     while (itRoute != currNext)  // No need to move x, we pivot around it
     {
         auto *current = itRoute;
         itRoute = p(itRoute);
         current->insertAfter(insertionPoint);
         insertionPoint = current;
     }
 }
 
-void TwoOpt::applyBetweenRoutes(Node *U, Node *V)
+void TwoOpt::applyBetweenRoutes(Node *U, Node *V) const
 {
     auto *itRouteU = n(U);
     auto *itRouteV = n(V);
 
     auto *insertLocation = U;
     while (!itRouteV->isDepot())
     {
@@ -104,23 +114,23 @@
         auto *node = itRouteU;
         itRouteU = n(itRouteU);
         node->insertAfter(insertLocation);
         insertLocation = node;
     }
 }
 
-int TwoOpt::evaluate(Node *U, Node *V)
+int TwoOpt::evaluate(Node *U, Node *V, CostEvaluator const &costEvaluator)
 {
     if (U->route->idx > V->route->idx)  // will be tackled in a later iteration
         return 0;                       // - no need to process here already
 
-    return U->route == V->route ? evalWithinRoute(U, V)
-                                : evalBetweenRoutes(U, V);
+    return U->route == V->route ? evalWithinRoute(U, V, costEvaluator)
+                                : evalBetweenRoutes(U, V, costEvaluator);
 }
 
-void TwoOpt::apply(Node *U, Node *V)
+void TwoOpt::apply(Node *U, Node *V) const
 {
     if (U->route == V->route)
         applyWithinRoute(U, V);
     else
         applyBetweenRoutes(U, V);
 }
```

### Comparing `pyvrp-0.1.0/pyvrp/cpp/educate/TwoOpt.h` & `pyvrp-0.2.1/pyvrp/cpp/educate/TwoOpt.h`

 * *Files 16% similar despite different names*

```diff
@@ -1,32 +1,34 @@
 #ifndef TWOOPT_H
 #define TWOOPT_H
 
 #include "LocalSearchOperator.h"
-#include "Node.h"
 
 /**
  * 2-OPT moves.
  *
  * Between routes: replaces U -> X and V -> Y by U -> Y and V -> X, if that is
  * an improving move. Within route: replaces U -> X and V -> Y by U -> V and
  * X -> Y, if that is an improving move.
  */
 class TwoOpt : public LocalSearchOperator<Node>
 {
     using LocalSearchOperator::LocalSearchOperator;
 
-    int evalWithinRoute(Node *U, Node *V);
+    int
+    evalWithinRoute(Node *U, Node *V, CostEvaluator const &costEvaluator) const;
 
-    int evalBetweenRoutes(Node *U, Node *V);
+    int evalBetweenRoutes(Node *U,
+                          Node *V,
+                          CostEvaluator const &costEvaluator) const;
 
-    void applyWithinRoute(Node *U, Node *V);
+    void applyWithinRoute(Node *U, Node *V) const;
 
-    void applyBetweenRoutes(Node *U, Node *V);
+    void applyBetweenRoutes(Node *U, Node *V) const;
 
 public:
-    int evaluate(Node *U, Node *V) override;
+    int evaluate(Node *U, Node *V, CostEvaluator const &costEvaluator) override;
 
-    void apply(Node *U, Node *V) override;
+    void apply(Node *U, Node *V) const override;
 };
 
 #endif  // TWOOPT_H
```

### Comparing `pyvrp-0.1.0/pyvrp/crossover/_selective_route_exchange.pyi` & `pyvrp-0.2.1/pyvrp/crossover/selective_route_exchange.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,18 +1,21 @@
 from typing import Tuple
 
+from pyvrp._CostEvaluator import CostEvaluator
 from pyvrp._Individual import Individual
-from pyvrp._PenaltyManager import PenaltyManager
 from pyvrp._ProblemData import ProblemData
 from pyvrp._XorShift128 import XorShift128
 
+from ._selective_route_exchange import selective_route_exchange as _srex
+
+
 def selective_route_exchange(
     parents: Tuple[Individual, Individual],
     data: ProblemData,
-    penalty_manager: PenaltyManager,
+    cost_evaluator: CostEvaluator,
     rng: XorShift128,
 ) -> Individual:
     """
     This crossover operator due to Nagata and Kobayashi (2010) combines routes
     from both parents to generate a new offspring solution. It does this by
     carefully selecting routes from the second parent that could be exchanged
     with routes from the first parent. After exchanging these routes, the
@@ -20,16 +23,16 @@
 
     Parameters
     ----------
     parents
         The two parent solutions to create an offspring from.
     data
         The problem instance.
-    penalty_manager
-        The penalty manager instance to be used during the greedy repair step.
+    cost_evaluator
+        The cost evaluator to be used during the greedy repair step.
     rng
         The random number generator to use.
 
     Returns
     -------
     Individual
         A new offspring.
@@ -37,7 +40,18 @@
     References
     ----------
     .. [1] Nagata, Y., & Kobayashi, S. (2010). A Memetic Algorithm for the
            Pickup and Delivery Problem with Time Windows Using Selective Route
            Exchange Crossover. *Parallel Problem Solving from Nature*, PPSN XI,
            536 - 545.
     """
+    first, second = parents
+
+    idx1 = rng.randint(first.num_routes())
+    idx2 = idx1 if idx1 < second.num_routes() else 0
+
+    max_routes_to_move = min(first.num_routes(), second.num_routes())
+    num_routes_to_move = rng.randint(max_routes_to_move) + 1  # at least one
+
+    return _srex(
+        parents, data, cost_evaluator, (idx1, idx2), num_routes_to_move
+    )
```

### Comparing `pyvrp-0.1.0/pyvrp/diagnostics/get_route_statistics.py` & `pyvrp-0.2.1/pyvrp/diagnostics/get_route_statistics.py`

 * *Files 3% similar despite different names*

```diff
@@ -80,41 +80,40 @@
     wait_time = 0
     time_warp = 0
     distance = 0
 
     prev_idx = 0  # depot
     for idx in list(route) + [0]:
         stop = data.client(idx)
-        delta = data.dist(prev_idx, idx)
-        current_time += delta
-        distance += delta
+        current_time += data.duration(prev_idx, idx)
+        distance += data.dist(prev_idx, idx)
 
         if current_time < stop.tw_early:
             wait_time += stop.tw_early - current_time
             current_time = stop.tw_early
 
         if current_time > stop.tw_late:
             time_warp += current_time - stop.tw_late
             current_time = stop.tw_late
 
         if idx != 0:  # Don't count final depot
             current_time += stop.service_duration
         prev_idx = idx
 
     demand = sum([data.client(idx).demand for idx in route])
-    serv_dur = sum([data.client(idx).service_duration for idx in route])
+    serv_duration = sum([data.client(idx).service_duration for idx in route])
 
     return RouteStatistics(
         distance=distance,
         start_time=start_time,
         end_time=current_time,
         duration=current_time - start_time,
         timewarp=time_warp,
         wait_time=wait_time,
-        service_time=serv_dur,
+        service_time=serv_duration,
         num_stops=len(route),
         total_demand=demand,
         fillrate=demand / data.vehicle_capacity,
         is_feasible=time_warp == 0 and demand <= data.vehicle_capacity,
         is_empty=len(route) == 0,
     )
```

### Comparing `pyvrp-0.1.0/pyvrp/diversity/_broken_pairs_distance.pyi` & `pyvrp-0.2.1/pyvrp/diversity/_broken_pairs_distance.pyi`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/diversity/tests/test_broken_pairs_distance.py` & `pyvrp-0.2.1/pyvrp/diversity/tests/test_broken_pairs_distance.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 from numpy.testing import assert_allclose
 
-from pyvrp import Individual, PenaltyManager
+from pyvrp import Individual
 from pyvrp.diversity import broken_pairs_distance as bpd
 from pyvrp.tests.helpers import read
 
 
 def test_broken_pairs_distance():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv1 = Individual(data, pm, [[1, 2, 3, 4], [], []])
-    indiv2 = Individual(data, pm, [[1, 2], [3], [4]])
-    indiv3 = Individual(data, pm, [[3], [4, 1, 2], []])
-    indiv4 = Individual(data, pm, [[4, 3, 2, 1], [], []])
+    indiv1 = Individual(data, [[1, 2, 3, 4], [], []])
+    indiv2 = Individual(data, [[1, 2], [3], [4]])
+    indiv3 = Individual(data, [[3], [4, 1, 2], []])
+    indiv4 = Individual(data, [[4, 3, 2, 1], [], []])
 
     # BPD of an individual and itself should be zero.
     for indiv in [indiv1, indiv2, indiv3, indiv4]:
         assert_allclose(bpd(indiv, indiv), 0.0)
 
     # BPD of indiv1 and indiv2. The two broken pairs are (2, 3) and (3, 4).
     assert_allclose(bpd(indiv1, indiv2), 0.5)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/LocalSearch.py` & `pyvrp-0.2.1/pyvrp/educate/LocalSearch.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from typing import List
 
+from pyvrp._CostEvaluator import CostEvaluator
 from pyvrp._Individual import Individual
-from pyvrp._PenaltyManager import PenaltyManager
 from pyvrp._ProblemData import ProblemData
 from pyvrp._XorShift128 import XorShift128
 
 from ._LocalSearch import LocalSearch as _LocalSearch
 
 Neighbours = List[List[int]]
 
@@ -16,30 +16,27 @@
     neighbourhood in a very efficient manner using user-provided node and route
     operators. This quickly results in much improved ('educated') solutions.
 
     Parameters
     ----------
     data
         Data object describing the problem to be solved.
-    penalty_manager
-        Penalty manager to use.
     rng
         Random number generator.
     neighbours
         List of lists that defines the local search neighbourhood.
     """
 
     def __init__(
         self,
         data: ProblemData,
-        penalty_manager: PenaltyManager,
         rng: XorShift128,
         neighbours: Neighbours,
     ):
-        self._ls = _LocalSearch(data, penalty_manager, rng, neighbours)
+        self._ls = _LocalSearch(data, rng, neighbours)
 
     def add_node_operator(self, op):
         """
         Adds a node operator to this local search object. The node operator
         will be used by :meth:`~search` to improve an individual.
 
         Parameters
@@ -82,27 +79,32 @@
         -------
         list
             The current granular neighbourhood.
         """
         return self._ls.get_neighbours()
 
     def run(
-        self, individual: Individual, should_intensify: bool
+        self,
+        individual: Individual,
+        cost_evaluator: CostEvaluator,
+        should_intensify: bool,
     ) -> Individual:
         """
         This method uses the :meth:`~search` and :meth:`~intensify` methods to
         iteratively improve the given individual. First, :meth:`~search` is
         applied. Thereafter, if ``should_intensify`` is true,
         :meth:`~intensify` is applied. This process repeats until no further
         improvements are found. Finally, the improved solution is returned.
 
         Parameters
         ----------
         individual
             The individual to improve through local search.
+        cost_evaluator
+            Cost evaluator to use.
         should_intensify
             Whether to apply :meth:`~intensify`. Intensification can provide
             much better solutions, but is computationally demanding. By default
             intensification is applied.
 
         Returns
         -------
@@ -111,40 +113,47 @@
             individual that was passed in.
         """
         # HACK We keep searching and intensifying to mimic the local search
         # implementation of HGS-CVRP and HGS-VRPTW
         # TODO separate load/export individual from c++ implementation
         # so we only need to do it once
         while True:
-            individual = self.search(individual)
+            individual = self.search(individual, cost_evaluator)
 
             if not should_intensify:
                 return individual
 
-            new_individual = self.intensify(individual)
+            new_individual = self.intensify(individual, cost_evaluator)
 
-            if new_individual.cost() < individual.cost():
+            current_cost = cost_evaluator.penalised_cost(individual)
+            new_cost = cost_evaluator.penalised_cost(new_individual)
+            if new_cost < current_cost:
                 individual = new_individual
                 continue
 
             return individual
 
     def intensify(
-        self, individual: Individual, overlap_tolerance_degrees: int = 0
+        self,
+        individual: Individual,
+        cost_evaluator: CostEvaluator,
+        overlap_tolerance_degrees: int = 0,
     ) -> Individual:
         """
         This method uses the intensifying route operators on this local search
         object to improve the given individual. To limit the computation
         demands of intensification, the  ``overlap_tolerance_degrees`` argument
         can be used to limit the number of route pairs that are evaluated.
 
         Parameters
         ----------
         individual
             The individual to improve.
+        cost_evaluator
+            Cost evaluator to use.
         overlap_tolerance_degrees
             This method evaluates improving moves between route pairs. To limit
             computational efforts, by default not all route pairs are
             considered: only those route pairs that share some overlap when
             considering their center's angle from the depot are evaluted.
             This parameter controls the amount of overlap needed before two
             routes are evaluated.
@@ -157,32 +166,38 @@
 
         Returns
         -------
         Individual
             The improved individual. This is not the same object as the
             individual that was passed in.
         """
-        return self._ls.intensify(individual, overlap_tolerance_degrees)
+        return self._ls.intensify(
+            individual, cost_evaluator, overlap_tolerance_degrees
+        )
 
-    def search(self, individual: Individual) -> Individual:
+    def search(
+        self, individual: Individual, cost_evaluator: CostEvaluator
+    ) -> Individual:
         """
         This method uses the node operators on this local search object to
         improve the given individual.
 
         Parameters
         ----------
         individual
             The individual to improve.
+        cost_evaluator
+            Cost evaluator to use.
 
         Raises
         ------
         RuntimeError
             When this method is called before registering node operators.
             Operators can be registered using :meth:`~add_node_operator`.
 
         Returns
         -------
         Individual
             The improved individual. This is not the same object as the
             individual that was passed in.
         """
-        return self._ls.search(individual)
+        return self._ls.search(individual, cost_evaluator)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/_LocalSearch.pyi` & `pyvrp-0.2.1/pyvrp/educate/_LocalSearch.pyi`

 * *Files 26% similar despite different names*

```diff
@@ -1,25 +1,29 @@
 from typing import List
 
+from pyvrp._CostEvaluator import CostEvaluator
 from pyvrp._Individual import Individual
-from pyvrp._PenaltyManager import PenaltyManager
 from pyvrp._ProblemData import ProblemData
 from pyvrp._XorShift128 import XorShift128
 
 Neighbours = List[List[int]]
 
 class LocalSearch:
     def __init__(
         self,
         data: ProblemData,
-        penalty_manager: PenaltyManager,
         rng: XorShift128,
         neighbours: Neighbours,
     ) -> None: ...
     def add_node_operator(self, op) -> None: ...
     def add_route_operator(self, op) -> None: ...
     def set_neighbours(self, neighbours: Neighbours) -> None: ...
     def get_neighbours(self) -> Neighbours: ...
     def intensify(
-        self, individual: Individual, overlap_tolerance_degrees: int = 0
+        self,
+        individual: Individual,
+        cost_evaluator: CostEvaluator,
+        overlap_tolerance_degrees: int = 0,
+    ) -> Individual: ...
+    def search(
+        self, individual: Individual, cost_evaluator: CostEvaluator
     ) -> Individual: ...
-    def search(self, individual: Individual) -> Individual: ...
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/__init__.py` & `pyvrp-0.2.1/pyvrp/educate/__init__.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/educate/neighbourhood.py` & `pyvrp-0.2.1/pyvrp/educate/neighbourhood.py`

 * *Files 22% similar despite different names*

```diff
@@ -14,25 +14,32 @@
 class NeighbourhoodParams:
     """
     Configuration for calculating a granular neighbourhood.
 
     Attributes
     ----------
     weight_wait_time
-        TODO
+        Weight given to the minimum wait time aspect of the proximity
+        calculation. A large wait time indicates the clients are far apart
+        in duration/time.
     weight_time_warp
-        TODO
+        Weight given to the minimum time warp aspect of the proximity
+        calculation. A large time warp indicates the clients are far apart in
+        duration/time.
     nb_granular
         Number of other clients that are in each client's granular
         neighbourhood. This parameter determines the size of the overall
         neighbourhood.
     symmetric_proximity
-        TODO
+        Whether to calculate a symmetric proximity matrix. This ensures edge
+        :math:`(i, j)` is given the same weight as :math:`(j, i)`.
     symmetric_neighbours
-        TODO
+        Whether to symmetrise the neighbourhood structure. This ensures that
+        when edge :math:`(i, j)` is in, then so is :math:`(j, i)`. Note that
+        this is *not* the same as ``symmetric_proximity``.
 
     Raises
     ------
     ValueError
         When ``nb_granular`` is non-positive.
     """
 
@@ -62,84 +69,95 @@
 
     Returns
     -------
     Neighbours
         A list of list of integers representing the neighbours for each client.
         The first element represents the depot and is an empty list.
     """
+    proximity = _compute_proximity(
+        data,
+        params.weight_wait_time,
+        params.weight_time_warp,
+    )
 
-    proximity = _compute_proximity(data, params)
+    if params.symmetric_proximity:
+        proximity = np.minimum(proximity, proximity.T)
 
-    # Mask self from proximities by adding a large constant
-    # and add the index with a very small weight as tie-breaker (to mimic
-    # original c++ version)
     n = len(proximity)
-    k = min(params.nb_granular, n - 1)
-    idcs = np.arange(n)
-    jitter = 1e-6 * idcs  # add a bit of jitter to break ties
-    proximity = proximity + jitter[None, :]
-    np.fill_diagonal(proximity, np.inf)  # exclude self from neighbourhood
-    idx_topk = np.argpartition(proximity, k, axis=-1)[:, :k]
-
-    if params.symmetric_neighbours:
-        # Convert into adjacency matrix that can be symmetrized
-        adj = np.zeros_like(proximity, dtype=bool)
-        adj[idcs[:, None], idx_topk] = True
-
-        # Add correlated vertex if correlated in one of two directions
-        adj = adj | adj.transpose()
-
-        # Append empty neighbours for depot and add 1 to offset depot indexing
-        return [[]] + [(np.flatnonzero(row) + 1).tolist() for row in adj]
-    else:
-        return [[]] + (np.sort(idx_topk, -1) + 1).tolist()
+    k = min(params.nb_granular, n - 2)  # excl. depot and self
+
+    np.fill_diagonal(proximity, np.inf)  # cannot be in own neighbourhood
+    proximity[0, :] = np.inf  # depot has no neighbours
+    proximity[:, 0] = np.inf  # clients do not neighbour depot
+
+    top_k = np.argsort(proximity, axis=1, kind="stable")[1:, :k]  # excl. depot
+
+    if not params.symmetric_neighbours:
+        return [[]] + top_k.tolist()
+
+    # Construct a symmetric adjacency matrix and return the adjacent clients
+    # as the neighbourhood structure.
+    adj = np.zeros_like(proximity, dtype=bool)
+    rows = np.expand_dims(np.arange(1, n), axis=1)
+    adj[rows, top_k] = True
+    adj = adj | adj.transpose()
+
+    return [np.flatnonzero(row).tolist() for row in adj]
 
 
 def _compute_proximity(
-    data: ProblemData, params: NeighbourhoodParams = NeighbourhoodParams()
+    data: ProblemData, weight_wait_time: float, weight_time_warp: float
 ) -> np.ndarray[float]:
     """
-    Computes proximity for neighborhood.
+    Computes proximity for neighborhood. Proximity is based on Vidal et al.
+    (2013).
 
     Parameters
     ----------
     data
         ProblemData for which to compute proximity.
     params
         NeighbourhoodParams that define how proximity is computed.
 
     Returns
     -------
     np.ndarray[float]
         A numpy array of size n x n where n = data.num_clients containing
         the proximities values between all clients (depot excluded).
-    """
 
+    References
+    ----------
+    .. [1] Vidal, T., Crainic, T. G., Gendreau, M., and Prins, C. (2013). A
+           hybrid genetic algorithm with adaptive diversity management for a
+           large class of vehicle routing problems with time-windows.
+           *Computers & Operations Research*, 40(1), 475 - 489.
+    """
     dim = data.num_clients + 1
-
     clients = [data.client(idx) for idx in range(dim)]
 
     earliest = np.array([cli.tw_early for cli in clients])
     latest = np.array([cli.tw_late for cli in clients])
     service = np.array([cli.service_duration for cli in clients])
     durations = np.array(
-        [[data.dist(i, j) for j in range(dim)] for i in range(dim)],
+        [[data.duration(i, j) for j in range(dim)] for i in range(dim)],
         dtype=float,
     )
 
     min_wait_time = np.maximum(
         earliest[None, :] - durations - service[:, None] - latest[:, None], 0
     )
+
     min_time_warp = np.maximum(
         earliest[:, None] + service[:, None] + durations - latest[None, :],
         0,
     )
 
-    prox = (
-        durations
-        + params.weight_wait_time * min_wait_time
-        + params.weight_time_warp * min_time_warp
+    distances = np.array(
+        [[data.dist(i, j) for j in range(dim)] for i in range(dim)],
+        dtype=float,
     )
 
-    if params.symmetric_proximity:
-        prox = np.minimum(prox, prox.T)
-    return prox[1:, 1:]  # Skip depot
+    return (
+        distances
+        + weight_wait_time * min_wait_time
+        + weight_time_warp * min_time_warp
+    )
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/tests/test_Exchange.py` & `pyvrp-0.2.1/pyvrp/educate/tests/test_Exchange.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from numpy.testing import assert_, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import Client, CostEvaluator, Individual, ProblemData, XorShift128
 from pyvrp.educate import LocalSearch, NeighbourhoodParams, compute_neighbours
 from pyvrp.educate._Exchange import (
     Exchange10,
     Exchange11,
     Exchange20,
     Exchange21,
     Exchange22,
@@ -31,28 +31,30 @@
 def test_swap_single_route_stays_single_route(operator):
     """
     Swap operators ((N, M)-exchange operators with M > 0) on a single route can
     only move within the same route, so they can never find a solution that has
     more than one route.
     """
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(operator(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(operator(data))
 
     single_route = list(range(1, data.num_clients + 1))
-    individual = Individual(data, pm, [single_route])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [single_route])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution.
     assert_equal(improved_individual.num_routes(), 1)
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
 
 
 @mark.parametrize(
     "operator",
     [
         Exchange10,
         Exchange20,
@@ -61,29 +63,31 @@
 )
 def test_relocate_uses_empty_routes(operator):
     """
     Unlike the swapping exchange operators, relocate should be able to relocate
     clients to empty routes if that is an improvement.
     """
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(operator(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(operator(data))
 
     single_route = list(range(1, data.num_clients + 1))
-    individual = Individual(data, pm, [single_route])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [single_route])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution, and
     # should use more routes.
     assert_(improved_individual.num_routes() > 1)
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
 
 
 @mark.parametrize(
     "operator",
     [
         Exchange22,
         Exchange30,
@@ -96,107 +100,156 @@
     """
     (N, M)-exchange works by exchanging N nodes starting at some node U with
     M nodes starting at some node V. But when there is no sequence of N or M
     nodes that does not contain the depot (because the routes are very short),
     then no exchange is possible.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(operator(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(operator(data))
 
-    individual = Individual(data, pm, [[1, 2], [3], [4]])
-    new_individual = ls.search(individual)
+    individual = Individual(data, [[1, 2], [3], [4]])
+    new_individual = ls.search(individual, cost_evaluator)
 
     assert_equal(new_individual, individual)
 
 
 @mark.parametrize("operator", [Exchange32, Exchange33])
 def test_cannot_exchange_when_segments_overlap(operator):
     """
     (3, 2)- and (3, 3)-exchange cannot exchange anything on a length-four
     single route solution: there's always overlap between the segments.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(operator(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(operator(data))
 
-    individual = Individual(data, pm, [[1, 2, 3, 4]])
-    new_individual = ls.search(individual)
+    individual = Individual(data, [[1, 2, 3, 4]])
+    new_individual = ls.search(individual, cost_evaluator)
 
     assert_equal(new_individual, individual)
 
 
 def test_cannot_swap_adjacent_segments():
     """
     (2, 2)-exchange on a single route cannot swap adjacent segments, since
     that's already covered by (2, 0)-exchange.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(Exchange22(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(Exchange22(data))
 
     # An adjacent swap by (2, 2)-exchange could have created the single-route
     # solution [3, 4, 1, 2], which has a much lower cost. But that's not
     # allowed because adjacent swaps are not allowed.
-    individual = Individual(data, pm, [[1, 2, 3, 4]])
-    new_individual = ls.search(individual)
+    individual = Individual(data, [[1, 2, 3, 4]])
+    new_individual = ls.search(individual, cost_evaluator)
 
     assert_equal(new_individual, individual)
 
 
 def test_swap_between_routes_OkSmall():
     """
     On the OkSmall example, (2, 1)-exchange should be able to swap parts of a
     two route solution, resulting in something better.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(Exchange21(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(Exchange21(data))
 
-    individual = Individual(data, pm, [[1, 2], [3, 4]])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [[1, 2], [3, 4]])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     assert_equal(improved_individual.get_routes(), [[3, 4, 2], [1], []])
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
 
 
 def test_relocate_after_depot_should_work():
     """
     This test exercises the bug identified in issue #142, involving a relocate
     action that should insert directly after the depot.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     # This is a non-empty neighbourhood (so LS does not complain), but the only
     # client moves allowed by it will not improve the initial solution created
     # below. So the only improvements (1, 0)-exchange can make must come from
     # moving clients behind the depot of a route.
     neighbours = [[] for _ in range(data.num_clients + 1)]
     neighbours[2].append(1)
 
-    ls = LocalSearch(data, pm, rng, neighbours)
-    ls.add_node_operator(Exchange10(data, pm))
+    ls = LocalSearch(data, rng, neighbours)
+    ls.add_node_operator(Exchange10(data))
 
     # This individual can be improved by moving 3 into its own route, that is,
     # inserting it after the depot of an empty route. Before the bug was fixed,
     # (1, 0)-exchange never performed this move.
-    individual = Individual(data, pm, [[1, 2, 3], [4]])
-    expected = Individual(data, pm, [[1, 2], [3], [4]])
-    assert_equal(ls.search(individual), expected)
+    individual = Individual(data, [[1, 2, 3], [4]])
+    expected = Individual(data, [[1, 2], [3], [4]])
+    assert_equal(ls.search(individual, cost_evaluator), expected)
+
+
+def test_relocate_only_happens_when_distance_and_duration_allow_it():
+    """
+    Tests that (1, 0)-exchange checks the duration matrix for time-window
+    feasibility before applying a move that improves the traveled distance.
+    """
+    clients = [
+        Client(x=0, y=0, demand=0, service_duration=0, tw_early=0, tw_late=10),
+        Client(x=1, y=0, demand=0, service_duration=0, tw_early=0, tw_late=5),
+        Client(x=2, y=0, demand=0, service_duration=0, tw_early=0, tw_late=5),
+    ]
+
+    data = ProblemData(
+        clients=clients,
+        nb_vehicles=1,
+        vehicle_cap=0,
+        distance_matrix=[  # distance-wise, the best route is 0 -> 1 -> 2 -> 0.
+            [0, 1, 5],
+            [5, 0, 1],
+            [1, 5, 0],
+        ],
+        duration_matrix=[  # duration-wise, the best route is 0 -> 2 -> 1 -> 0.
+            [0, 100, 2],
+            [1, 0, 100],
+            [100, 2, 0],
+        ],
+    )
+
+    # We consider two solutions. The first is duration optimal, and overall the
+    # only feasible solution. This solution can thus not be improved further.
+    # We also consider a distance-optimal solution that is not feasible. Since
+    # we have non-zero time warp penalty, this solution should be improved into
+    # the duration optimal solution.
+    duration_optimal = Individual(data, [[2, 1]])
+    distance_optimal = Individual(data, [[1, 2]])
+
+    assert_(distance_optimal.distance() < duration_optimal.distance())
+    assert_(duration_optimal.time_warp() < distance_optimal.time_warp())
+
+    cost_evaluator = CostEvaluator(1, 1)
+    rng = XorShift128(seed=42)
+    ls = LocalSearch(data, rng, compute_neighbours(data))
+    ls.add_node_operator(Exchange10(data))
+
+    assert_equal(ls.search(duration_optimal, cost_evaluator), duration_optimal)
+    assert_equal(ls.search(distance_optimal, cost_evaluator), duration_optimal)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/tests/test_MoveTwoClientsReversed.py` & `pyvrp-0.2.1/pyvrp/educate/tests/test_MoveTwoClientsReversed.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from numpy.testing import assert_, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import CostEvaluator, Individual, XorShift128
 from pyvrp.educate import (
     LocalSearch,
     MoveTwoClientsReversed,
     NeighbourhoodParams,
     compute_neighbours,
 )
 from pyvrp.tests.helpers import read
@@ -13,49 +13,55 @@
 
 def test_single_route_OkSmall():
     """
     This test checks that MoveTwoClientsReversed properly solves the small
     instance where we know what is going on.
     """
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(MoveTwoClientsReversed(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(MoveTwoClientsReversed(data))
 
-    individual = Individual(data, pm, [[1, 4, 2, 3]])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [[1, 4, 2, 3]])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution.
     assert_equal(improved_individual.num_routes(), 1)
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
 
     # (2, 3) was inserted after 1 as 1 -> 3 -> 2 -> 4. Then (1, 3) got inserted
-    # after 2 as 2 -> 3 -> 1 -> 4.
-    assert_equal(improved_individual.get_routes(), [[2, 3, 1, 4], [], []])
+    # after 4 as 2 -> 4 -> 3 -> 1.
+    assert_equal(improved_individual.get_routes(), [[2, 4, 3, 1], [], []])
 
     # These two-route solutions can all be created by MoveTwoClientsReversed
     # from the returned solution. So they must have a cost that's at best equal
     # to the returned solution's cost.
-    for routes in ([[3, 2], [1, 4]], [[2, 3], [4, 1]], [[2, 4], [1, 3]]):
-        other = Individual(data, pm, routes)
-        assert_(improved_individual.cost() <= other.cost())
+    for routes in ([[3, 1], [4, 2]], [[2, 1], [3, 4]], [[2, 4], [1, 3]]):
+        other = Individual(data, routes)
+        improved_cost = cost_evaluator.penalised_cost(improved_individual)
+        other_cost = cost_evaluator.penalised_cost(other)
+        assert_(improved_cost <= other_cost)
 
 
 @mark.parametrize("seed", [2643, 2742, 2941, 3457, 4299, 4497, 6178, 6434])
 def test_RC208_instance(seed: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=seed)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(MoveTwoClientsReversed(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(MoveTwoClientsReversed(data))
 
     single_route = list(range(1, data.num_clients + 1))
-    individual = Individual(data, pm, [single_route])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [single_route])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution.
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/tests/test_RelocateStar.py` & `pyvrp-0.2.1/pyvrp/educate/tests/test_RelocateStar.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from numpy.testing import assert_, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import CostEvaluator, Individual, XorShift128
 from pyvrp.educate import (
     Exchange10,
     LocalSearch,
     NeighbourhoodParams,
     RelocateStar,
     compute_neighbours,
 )
@@ -15,28 +15,28 @@
 def test_exchange10_and_relocate_star_are_same_large_neighbourhoods():
     """
     With sufficiently large granular neighbourhoods, (1, 0)-Exchange and
     RELOCATE* find the exact same solutions. Only when the granular
     neighbourhood is restricted do these solutions start to differ.
     """
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
 
-    ls.add_node_operator(Exchange10(data, pm))
-    ls.add_route_operator(RelocateStar(data, pm))
+    ls.add_node_operator(Exchange10(data))
+    ls.add_route_operator(RelocateStar(data))
 
     for _ in range(10):  # repeat a few times to really make sure
-        individual = Individual(data, pm, rng)
-        exchange_individual = ls.search(individual)
+        individual = Individual.make_random(data, rng)
+        exchange_individual = ls.search(individual, cost_evaluator)
         relocate_individual = ls.intensify(
-            exchange_individual, overlap_tolerance_degrees=360
+            exchange_individual, cost_evaluator, overlap_tolerance_degrees=360
         )
 
         # RELOCATE* applies the best (1, 0)-exchange moves between routes. But
         # when the granular neighbourhood covers the entire client space, that
         # best move has already been evaluated and applied by regular (1,0)
         # exchange. Thus, at this point the individual cannot be improved
         # further by RELOCATE*.
@@ -46,29 +46,32 @@
 @mark.parametrize("size", [2, 5, 10])
 def test_exchange10_and_relocate_star_differ_small_neighbourhoods(size: int):
     """
     This test restricts the sizes of the granular neighbourhoods, so now
     (1, 0)-Exchange and RELOCATE* should start to differ.
     """
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=size)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
 
-    ls.add_node_operator(Exchange10(data, pm))
-    ls.add_route_operator(RelocateStar(data, pm))
+    ls.add_node_operator(Exchange10(data))
+    ls.add_route_operator(RelocateStar(data))
 
-    individual = Individual(data, pm, rng)
-    exchange_individual = ls.search(individual)
+    individual = Individual.make_random(data, rng)
+    exchange_individual = ls.search(individual, cost_evaluator)
     relocate_individual = ls.intensify(
-        exchange_individual, overlap_tolerance_degrees=360
+        exchange_individual, cost_evaluator, overlap_tolerance_degrees=360
     )
 
     # The original individual was not that great, so after (1, 0)-Exchange it
     # should have improved. But that operator is restricted by the size of the
     # granular neighbourhood, which limits the number of operators. RELOCATE*
     # overcomes some of that, and as a result, should be able to improve the
     # solution further.
-    assert_(individual.cost() > exchange_individual.cost())
-    assert_(exchange_individual.cost() > relocate_individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    exchange_cost = cost_evaluator.penalised_cost(exchange_individual)
+    relocate_cost = cost_evaluator.penalised_cost(relocate_individual)
+    assert_(current_cost > exchange_cost)
+    assert_(exchange_cost > relocate_cost)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/tests/test_SwapStar.py` & `pyvrp-0.2.1/pyvrp/educate/tests/test_SwapStar.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from numpy.testing import assert_, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import CostEvaluator, Individual, XorShift128
 from pyvrp.educate import (
     Exchange11,
     LocalSearch,
     NeighbourhoodParams,
     SwapStar,
     compute_neighbours,
 )
@@ -16,55 +16,60 @@
     """
     SWAP* can move two clients to any position in the routes, whereas regular
     swap ((1, 1)-exchange) must reinsert each client in the other's position.
     Thus, SWAP* should still be able to identify additional improving moves
     after (1, 1)-exchange gets stuck.
     """
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     # For a fair comparison we should not hamper the node operator with
     # granularity restrictions.
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
 
-    ls.add_node_operator(Exchange11(data, pm))
-    ls.add_route_operator(SwapStar(data, pm))
+    ls.add_node_operator(Exchange11(data))
+    ls.add_route_operator(SwapStar(data))
 
     for _ in range(10):  # repeat a few times to really make sure
-        individual = Individual(data, pm, rng)
+        individual = Individual.make_random(data, rng)
 
-        swap_individual = ls.search(individual)
+        swap_individual = ls.search(individual, cost_evaluator)
         swap_star_individual = ls.intensify(
-            swap_individual, overlap_tolerance_degrees=360
+            swap_individual, cost_evaluator, overlap_tolerance_degrees=360
         )
 
         # The regular swap operator should have been able to improve the random
         # individual. After swap gets stuck, SWAP* should still be able to
         # further improve the individual.
-        assert_(swap_individual.cost() < individual.cost())
-        assert_(swap_star_individual.cost() < swap_individual.cost())
+        current_cost = cost_evaluator.penalised_cost(individual)
+        swap_cost = cost_evaluator.penalised_cost(swap_individual)
+        swap_star_cost = cost_evaluator.penalised_cost(swap_star_individual)
+        assert_(swap_cost < current_cost)
+        assert_(swap_star_cost < swap_cost)
 
 
 @mark.parametrize("seed", [2643, 2742, 2941, 3457, 4299, 4497, 6178, 6434])
 def test_swap_star_on_RC208_instance(seed: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=seed)
 
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data))
-    ls.add_route_operator(SwapStar(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data))
+    ls.add_route_operator(SwapStar(data))
 
     # Make an initial solution that consists of two routes, by randomly
     # splitting the single-route solution.
     route = list(range(1, data.num_clients + 1))
     split = rng.randint(data.num_clients)
-    individual = Individual(data, pm, [route[:split], route[split:]])
+    individual = Individual(data, [route[:split], route[split:]])
     improved_individual = ls.intensify(
-        individual, overlap_tolerance_degrees=360
+        individual, cost_evaluator, overlap_tolerance_degrees=360
     )
 
     # The new solution should strictly improve on our original solution, but
     # cannot use more routes since SWAP* does not create routes.
     assert_equal(improved_individual.num_routes(), 2)
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
```

### Comparing `pyvrp-0.1.0/pyvrp/educate/tests/test_TwoOpt.py` & `pyvrp-0.2.1/pyvrp/educate/tests/test_TwoOpt.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,51 +1,55 @@
 from numpy.testing import assert_, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import CostEvaluator, Individual, XorShift128
 from pyvrp.educate import (
     LocalSearch,
     NeighbourhoodParams,
     TwoOpt,
     compute_neighbours,
 )
 from pyvrp.tests.helpers import read
 
 
 def test_OkSmall_instance():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(TwoOpt(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(TwoOpt(data))
 
-    individual = Individual(data, pm, [[1, 2, 3, 4]])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [[1, 2, 3, 4]])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution.
     assert_equal(improved_individual.num_routes(), 2)
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
 
     # First improving (U, V) node pair is (1, 3), which results in the route
     # [1, 3, 2, 4]. The second improving node pair involves the depot of an
-    # empty route: (1, 0). This results in routes [3, 2, 4] and [1].
-    assert_equal(improved_individual.get_routes(), [[3, 2, 4], [1], []])
+    # empty route: (1, 0). This results in routes [1] and [3, 2, 4].
+    assert_equal(improved_individual.get_routes(), [[1], [3, 2, 4], []])
 
 
 @mark.parametrize("seed", [2643, 2742, 2941, 3457, 4299, 4497, 6178, 6434])
 def test_RC208_instance(seed: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=seed)
 
     nb_params = NeighbourhoodParams(nb_granular=data.num_clients)
-    ls = LocalSearch(data, pm, rng, compute_neighbours(data, nb_params))
-    ls.add_node_operator(TwoOpt(data, pm))
+    ls = LocalSearch(data, rng, compute_neighbours(data, nb_params))
+    ls.add_node_operator(TwoOpt(data))
 
     single_route = list(range(1, data.num_clients + 1))
-    individual = Individual(data, pm, [single_route])
-    improved_individual = ls.search(individual)
+    individual = Individual(data, [single_route])
+    improved_individual = ls.search(individual, cost_evaluator)
 
     # The new solution should strictly improve on our original solution.
-    assert_(improved_individual.cost() < individual.cost())
+    current_cost = cost_evaluator.penalised_cost(individual)
+    improved_cost = cost_evaluator.penalised_cost(improved_individual)
+    assert_(improved_cost < current_cost)
```

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_coordinates.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_coordinates.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_demands.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_demands.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_diversity.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_diversity.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_instance.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_instance.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_objectives.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_objectives.py`

 * *Files 12% similar despite different names*

```diff
@@ -16,23 +16,24 @@
     """
     Plots each subpopulation's objective values.
 
     Parameters
     ----------
     result
         Result for which to plot objectives.
-    num_to_skip, optional
+    num_to_skip
         Number of initial iterations to skip when plotting. Early iterations
         often have very high objective values, and obscure what's going on
         later in the search. The default skips the first 5% of iterations.
-    ax, optional
+    ax
         Axes object to draw the plot on. One will be created if not provided.
     ylim_adjust
-        Adjusts the y-limits to ``(best*ylim_adjust[0], best*ylim_adjust[1])``,
-        where ``best`` denotes the best found feasible objective value.
+        Bounds the y-axis to ``(best * ylim_adjust[0], best * ylim_adjust[1])``
+        where ``best`` denotes the best found feasible objective value. Default
+        (0.95, 1.15).
 
     Raises
     ------
     StatisticsNotCollectedError
         Raised when statistics have not been collected.
     """
     if not result.has_statistics():
@@ -62,12 +63,12 @@
     y = [d.avg_cost for d in result.stats.feas_stats]
     _plot(x, y, label="Feas. avg.", c="tab:green", alpha=0.3, ls="--")
 
     # Use best objectives to set reasonable y-limits
     best = np.nanmin([d.best_cost for d in result.stats.feas_stats])
     ax.set_ylim(best * ylim_adjust[0], best * ylim_adjust[1])
 
-    ax.set_title("Feasible objectives")
+    ax.set_title("Objectives")
     ax.set_xlabel("Iteration (#)")
     ax.set_ylabel("Objective")
 
     ax.legend(frameon=False)
```

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_result.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_result.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_route_schedule.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_route_schedule.py`

 * *Files 2% similar despite different names*

```diff
@@ -41,15 +41,15 @@
     """
     if not ax:
         _, ax = plt.subplots()
 
     depot = data.client(0)  # For readability, define variable
     horizon = depot.tw_late - depot.tw_early
 
-    # Initialize tracking variables
+    # Initialise tracking variables
     t = 0
     wait_time = 0
     time_warp = 0
     drive_time = 0
     serv_time = 0
     dist = 0
     load = sum([data.client(idx).demand for idx in route])
@@ -75,16 +75,16 @@
     serv_time += depot.service_duration
 
     add_traces(dist, t, drive_time, serv_time, load)
 
     prev_idx = 0  # depot
     for idx in list(route) + [0]:
         stop = data.client(idx)
-        # Currently time = distance (i.e. assume speed of 1)
-        delta_time = delta_dist = data.dist(prev_idx, idx)
+        delta_time = data.duration(prev_idx, idx)
+        delta_dist = data.dist(prev_idx, idx)
         t += delta_time
         drive_time += delta_time
         dist += delta_dist
 
         add_traces(dist, t, drive_time, serv_time, load)
 
         if t < stop.tw_early:
```

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_runtimes.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_runtimes.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_solution.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_solution.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/plot_time_windows.py` & `pyvrp-0.2.1/pyvrp/plotting/plot_time_windows.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_instance.png` & `pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_instance.png`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_result.png` & `pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_result.png`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_route_schedule.png` & `pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_route_schedule.png`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution.png` & `pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution.png`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution_with_customers.png` & `pyvrp-0.2.1/pyvrp/plotting/tests/baseline_images/test_plotting/plot_solution_with_customers.png`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/plotting/tests/test_plotting.py` & `pyvrp-0.2.1/pyvrp/plotting/tests/test_plotting.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,24 +1,30 @@
 from matplotlib.testing.decorators import image_comparison as img_comp
 from numpy.testing import assert_, assert_raises
 
-from pyvrp import Individual, PenaltyManager, Population, XorShift128, plotting
+from pyvrp import (
+    CostEvaluator,
+    Individual,
+    Population,
+    PopulationParams,
+    XorShift128,
+    plotting,
+)
 from pyvrp.Result import Result
 from pyvrp.Statistics import Statistics
 from pyvrp.diversity import broken_pairs_distance
 from pyvrp.exceptions import StatisticsNotCollectedError
-from pyvrp.tests.helpers import read, read_solution
+from pyvrp.tests.helpers import make_random_solutions, read, read_solution
 
 IMG_KWARGS = dict(remove_text=True, tol=2, extensions=["png"], style="mpl20")
 
 
 def test_plotting_methods_raise_when_no_stats_available():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
-    individual = Individual(data, pm, [[1, 2, 3, 4]])
+    individual = Individual(data, [[1, 2, 3, 4]])
     res = Result(individual, Statistics(), 0, 0.0)
 
     assert_(not res.has_statistics())
 
     with assert_raises(StatisticsNotCollectedError):
         plotting.plot_diversity(res)
 
@@ -34,47 +40,52 @@
     plotting.plot_result(res, data)
 
 
 @img_comp(["plot_solution", "plot_solution_with_customers"], **IMG_KWARGS)
 def test_plot_solution():
     data = read("data/RC208.txt", "solomon", round_func="trunc")
     bks = read_solution("data/RC208.sol")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    individual = Individual(data, pm, bks)
+    individual = Individual(data, bks)
 
     plotting.plot_solution(individual, data)
     plotting.plot_solution(individual, data, plot_customers=True)
 
 
 @img_comp(["plot_result"], **IMG_KWARGS)
 def test_plot_result():
     num_iterations = 100
 
     data = read("data/RC208.txt", "solomon", round_func="trunc")
     bks = read_solution("data/RC208.sol")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
-    pop = Population(data, pm, rng, broken_pairs_distance)
+
+    params = PopulationParams()
+    pop = Population(broken_pairs_distance, params=params)
+
+    for indiv in make_random_solutions(params.min_pop_size, data, rng):
+        pop.add(indiv, cost_evaluator)
+
     stats = Statistics()
 
     for i in range(num_iterations):
         if i == num_iterations // 2:
             # Make sure we insert a feasible solution
-            individual = Individual(data, pm, bks)
+            individual = Individual(data, bks)
         else:
-            individual = Individual(data, pm, rng)
+            individual = Individual.make_random(data, rng)
 
-        pop.add(individual)
-        stats.collect_from(pop)
+        pop.add(individual, cost_evaluator)
+        stats.collect_from(pop, cost_evaluator)
 
         # Hacky to produce deterministic result
         stats.runtimes[-1] = i % 3
 
-    res = Result(Individual(data, pm, bks), stats, num_iterations, 0.0)
+    res = Result(Individual(data, bks), stats, num_iterations, 0.0)
     plotting.plot_result(res, data)
 
 
 @img_comp(["plot_instance"], **IMG_KWARGS)
 def test_plot_instance():
     data = read("data/RC208.txt", "solomon", round_func="trunc")
     plotting.plot_instance(data)
```

### Comparing `pyvrp-0.1.0/pyvrp/read.py` & `pyvrp-0.2.1/pyvrp/read.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import functools
 import pathlib
 from typing import Callable, Dict, List, Union
 
 import numpy as np
 import vrplib
 
-from ._ProblemData import ProblemData
+from ._ProblemData import Client, ProblemData
 
 _Routes = List[List[int]]
 _RoundingFunc = Callable[[np.ndarray], np.ndarray]
 
 _INT_MAX = np.iinfo(np.int32).max
 
 
@@ -67,61 +67,65 @@
             * ``'none'`` does no rounding. This is the default.
 
     Returns
     -------
     ProblemData
         Data instance constructed from the read data.
     """
-    if isinstance(round_func, str) and round_func in ROUND_FUNCS:
-        round_func = ROUND_FUNCS[round_func]
-    elif not callable(round_func):
+    if (key := str(round_func)) in ROUND_FUNCS:
+        round_func = ROUND_FUNCS[key]
+
+    if not callable(round_func):
         raise ValueError(
             f"round_func = {round_func} is not understood. Can be a function,"
             f" or one of {ROUND_FUNCS.keys()}."
         )
 
     instance = vrplib.read_instance(where, instance_format=instance_format)
 
     # A priori checks
     if "dimension" in instance:
-        num_clients = instance["dimension"]
+        dimension: int = instance["dimension"]
     else:
         if "demand" not in instance:
             raise ValueError("File should either contain dimension or demands")
-        num_clients = len(instance["demand"])
+        dimension = len(instance["demand"])
+
+    depots: np.ndarray = instance.get("depot", np.array([0]))
+    num_vehicles: int = instance.get("vehicles", dimension - 1)
+    capacity: int = instance.get("capacity", _INT_MAX)
 
-    depots = instance.get("depot", np.array([0]))
-    num_vehicles = instance.get("vehicles", num_clients - 1)
-    capacity = instance.get("capacity", _INT_MAX)
-    edge_weight = round_func(instance["edge_weight"])
+    distances: np.ndarray = round_func(instance["edge_weight"])
 
     if "demand" in instance:
-        demands = instance["demand"]
+        demands: np.ndarray = instance["demand"]
     else:
-        demands = np.zeros(num_clients, dtype=int)
+        demands = np.zeros(dimension, dtype=int)
 
     if "node_coord" in instance:
-        coords = round_func(instance["node_coord"])
+        coords: np.ndarray = round_func(instance["node_coord"])
     else:
-        coords = np.zeros((num_clients, 2), dtype=int)
+        coords = np.zeros((dimension, 2), dtype=int)
 
     if "service_time" in instance:
-        service_times = round_func(instance["service_time"])
+        service_times: np.ndarray = round_func(instance["service_time"])
     else:
-        service_times = np.zeros(num_clients, dtype=int)
+        service_times = np.zeros(dimension, dtype=int)
 
     if "time_window" in instance:
-        time_windows = round_func(instance["time_window"])
+        # VRPLIB instances typically do not have a duration data field, so we
+        # assume duration == distance if the instance has time windows.
+        durations = distances
+        time_windows: np.ndarray = round_func(instance["time_window"])
     else:
-        # The default value for the latest time window based on the maximum
-        # route duration. This ensures that the time window constraints are
-        # always satisfied.
-        bound = num_clients * (edge_weight.max() + service_times.max())
-        bound = min(bound, _INT_MAX)
-        time_windows = np.repeat([[0, bound]], num_clients, axis=0)
+        # No time window data. So the time window component is not relevant,
+        # and we set all time-related fields to zero.
+        durations = np.zeros_like(distances)
+        service_times = np.zeros(dimension, dtype=int)
+        time_windows = np.zeros((dimension, 2), dtype=int)
 
     # Checks
     if len(depots) != 1 or depots[0] != 0:
         raise ValueError(
             "Source file should contain single depot with index 1 "
             + "(depot index should be 0 after subtracting offset 1)"
         )
@@ -134,22 +138,32 @@
 
     if service_times[0] != 0:
         raise ValueError("Depot service duration must be 0")
 
     if (time_windows[:, 0] > time_windows[:, 1]).any():
         raise ValueError("Time window cannot start after end")
 
+    clients = [
+        Client(
+            coords[idx][0],  # x
+            coords[idx][1],  # y
+            demands[idx],
+            service_times[idx],
+            time_windows[idx][0],  # TW early
+            time_windows[idx][1],  # TW late
+        )
+        for idx in range(dimension)
+    ]
+
     return ProblemData(
-        coords,
-        demands,
+        clients,
         num_vehicles,
         capacity,
-        time_windows,
-        service_times,
-        edge_weight,
+        distances,
+        durations,
     )
 
 
 def read_solution(where: Union[str, pathlib.Path]) -> _Routes:
     """
     Reads a solution in VRPLIB format from file at the given location, and
     returns the routes contained in it.
```

### Comparing `pyvrp-0.1.0/pyvrp/show_versions.py` & `pyvrp-0.2.1/pyvrp/show_versions.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/stop/NoImprovement.py` & `pyvrp-0.2.1/pyvrp/stop/NoImprovement.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,8 @@
-from typing import Optional, Union
-
-from pyvrp.OptimisationTarget import OptimisationTarget
+from typing import Optional
 
 
 class NoImprovement:
     """
     Criterion that stops if the best solution has not been improved for a fixed
     number of iterations.
 
@@ -15,18 +13,18 @@
     """
 
     def __init__(self, max_iterations: int):
         if max_iterations < 0:
             raise ValueError("max_iterations < 0 not understood.")
 
         self._max_iterations = max_iterations
-        self._target: Optional[Union[int, float]] = None
+        self._target: Optional[float] = None
         self._counter = 0
 
-    def __call__(self, best: OptimisationTarget) -> bool:
-        if self._target is None or best.cost() < self._target:
-            self._target = best.cost()
+    def __call__(self, best_cost: float) -> bool:
+        if self._target is None or best_cost < self._target:
+            self._target = best_cost
             self._counter = 0
         else:
             self._counter += 1
 
         return self._counter >= self._max_iterations
```

### Comparing `pyvrp-0.1.0/pyvrp/stop/StoppingCriterion.py` & `pyvrp-0.2.1/pyvrp/stop/StoppingCriterion.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,26 +1,24 @@
 from typing import Protocol
 
-from pyvrp.OptimisationTarget import OptimisationTarget
-
 
 class StoppingCriterion(Protocol):  # pragma: no cover
     """
     Protocol that stopping criteria must implement.
     """
 
-    def __call__(self, best: OptimisationTarget) -> bool:
+    def __call__(self, best_cost: float) -> bool:
         """
         When called, this stopping criterion should return True if the
         algorithm should stop, and False otherwise.
 
         Parameters
         ----------
-        best
-            Current best solution.
+        best_cost
+            Cost of current best solution.
 
         Returns
         -------
         bool
             True if the algorithm should stop, False otherwise.
         """
         ...
```

### Comparing `pyvrp-0.1.0/pyvrp/stop/tests/test_MaxIterations.py` & `pyvrp-0.2.1/pyvrp/stop/tests/test_MaxIterations.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from numpy.testing import assert_, assert_raises
 from pytest import mark
 
 from pyvrp.stop import MaxIterations
-from pyvrp.tests.helpers import DummyTarget
 
 
 @mark.parametrize("max_iterations", [-1, -42, -10000])
 def test_raise_negative_parameters(max_iterations: int):
     """
     Maximum iterations cannot be negative.
     """
@@ -22,18 +21,18 @@
     MaxIterations(max_iterations)
 
 
 def test_before_max_iterations():
     stop = MaxIterations(100)
 
     for _ in range(100):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
 
 def test_after_max_iterations():
     stop = MaxIterations(100)
 
     for _ in range(100):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
     for _ in range(100):
-        assert_(stop(DummyTarget(1)))
+        assert_(stop(1))
```

### Comparing `pyvrp-0.1.0/pyvrp/stop/tests/test_MaxRuntime.py` & `pyvrp-0.2.1/pyvrp/stop/tests/test_MaxRuntime.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from numpy.testing import assert_, assert_raises
 from pytest import mark
 
 from pyvrp.stop import MaxRuntime
-from pyvrp.tests.helpers import DummyTarget, sleep
+from pyvrp.tests.helpers import sleep
 
 
 @mark.parametrize("max_runtime", [-0.001, -1, -10.1])
 def test_raise_negative_parameters(max_runtime: float):
     """
     Maximum runtime may not be negative.
     """
@@ -23,19 +23,19 @@
 
 
 @mark.parametrize("max_runtime", [0.01, 0.05, 0.10])
 def test_before_max_runtime(max_runtime):
     stop = MaxRuntime(max_runtime)
 
     for _ in range(100):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
 
 @mark.parametrize("max_runtime", [0.01, 0.05, 0.10])
 def test_after_max_runtime(max_runtime):
     stop = MaxRuntime(max_runtime)
-    assert_(not stop(DummyTarget(1)))  # trigger the first time measurement
+    assert_(not stop(1))  # trigger the first time measurement
 
     sleep(max_runtime)
 
     for _ in range(100):
-        assert_(stop(DummyTarget(1)))
+        assert_(stop(1))
```

### Comparing `pyvrp-0.1.0/pyvrp/stop/tests/test_NoImprovement.py` & `pyvrp-0.2.1/pyvrp/stop/tests/test_NoImprovement.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 from numpy.testing import assert_, assert_raises
 from pytest import mark
 
 from pyvrp.stop import NoImprovement
-from pyvrp.tests.helpers import DummyTarget
 
 
 @mark.parametrize("max_iterations", [-10, -100, -1000])
 def test_raise_negative_parameters(max_iterations: int):
     """
     max_iterations cannot be negative.
     """
@@ -16,57 +15,57 @@
 
 def test_zero_max_iterations():
     """
     Test if setting max_iterations to zero always stops.
     """
     stop = NoImprovement(0)
 
-    assert_(stop(DummyTarget(1)))
-    assert_(stop(DummyTarget(1)))
+    assert_(stop(1))
+    assert_(stop(1))
 
 
 def test_one_max_iterations():
     """
     Test if setting max_iterations to one only stops when a non-improving
     solution has been found.
     """
     stop = NoImprovement(1)
 
-    assert_(not stop(DummyTarget(2)))
-    assert_(not stop(DummyTarget(1)))
-    assert_(stop(DummyTarget(1)))
+    assert_(not stop(2))
+    assert_(not stop(1))
+    assert_(stop(1))
 
 
 @mark.parametrize("n", [10, 100, 1000])
 def test_n_max_iterations_non_improving(n):
     """
     Test if setting max_iterations to n correctly stops with non-improving
     solutions. The first n iterations should not stop, but after that, the
     criterion should stop.
     """
     stop = NoImprovement(n)
 
     for _ in range(n):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
     for _ in range(n):
-        assert_(stop(DummyTarget(1)))
+        assert_(stop(1))
 
 
 @mark.parametrize("n, k", [(10, 2), (100, 20), (1000, 200)])
 def test_n_max_iterations_with_single_improvement(n, k):
     """
     Test if setting max_iterations to n correctly stops with a sequence of
     solutions, when the k-th solution is improving and the other solutions
     are non-improving. The first n + k - 1 iterations should not stop. After
     that, the criterion should stop.
     """
     stop = NoImprovement(n)
 
     for _ in range(k):
-        assert_(not stop(DummyTarget(2)))
+        assert_(not stop(2))
 
     for _ in range(n):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
     for _ in range(n):
-        assert_(stop(DummyTarget(1)))
+        assert_(stop(1))
```

### Comparing `pyvrp-0.1.0/pyvrp/stop/tests/test_TimedNoImprovement.py` & `pyvrp-0.2.1/pyvrp/stop/tests/test_TimedNoImprovement.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from numpy.testing import assert_, assert_raises
 from pytest import mark
 
 from pyvrp.stop import TimedNoImprovement
-from pyvrp.tests.helpers import DummyTarget, sleep
+from pyvrp.tests.helpers import sleep
 
 
 @mark.parametrize(
     "max_iterations, max_runtime",
     [(-1, 0), (-42, 0), (-10_000, 0), (0, -1), (0, -42), (0, -10_000)],
 )
 def test_raise_negative_parameters(max_iterations, max_runtime):
@@ -22,27 +22,27 @@
     Does not raise for non-negative parameters.
     """
     TimedNoImprovement(max_iterations, max_runtime)
 
 
 def test_stops_if_zero_max_iterations():
     stop = TimedNoImprovement(0, 0.100)
-    assert_(stop(DummyTarget(1)))
+    assert_(stop(1))
 
 
 @mark.parametrize("max_runtime", [0.01, 0.05, 0.10])
 def test_before_max_runtime(max_runtime):
     stop = TimedNoImprovement(101, max_runtime)
 
     for _ in range(100):
-        assert_(not stop(DummyTarget(1)))
+        assert_(not stop(1))
 
 
 @mark.parametrize("max_runtime", [0.01, 0.05, 0.10])
 def test_after_max_runtime(max_runtime):
     stop = TimedNoImprovement(101, max_runtime)
-    assert_(not stop(DummyTarget(1)))  # trigger the first time measurement
+    assert_(not stop(1))  # trigger the first time measurement
 
     sleep(max_runtime)
 
     for _ in range(100):
-        assert_(stop(DummyTarget(1)))
+        assert_(stop(1))
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/E-n22-k4.vrp.txt` & `pyvrp-0.2.1/pyvrp/tests/data/E-n22-k4.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/EdgeWeightsNoExplicit.txt` & `pyvrp-0.2.1/pyvrp/tests/data/EdgeWeightsNoExplicit.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/EdgeWeightsNotFullMatrix.txt` & `pyvrp-0.2.1/pyvrp/tests/data/EdgeWeightsNotFullMatrix.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/OkSmall.txt` & `pyvrp-0.2.1/pyvrp/tests/data/OkSmall.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/OkSmallGreedyRepair.txt` & `pyvrp-0.2.1/pyvrp/tests/data/OkSmallGreedyRepair.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/data/RC208.txt` & `pyvrp-0.2.1/pyvrp/tests/data/RC208.txt`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/helpers.py` & `pyvrp-0.2.1/pyvrp/tests/helpers.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import pathlib
 import time
 from functools import lru_cache
 
+from pyvrp import Individual
 from pyvrp.read import read as _read
 from pyvrp.read import read_solution as _read_solution
 
 
 @lru_cache
 def read(where: str, *args, **kwargs):
     """
@@ -33,17 +34,12 @@
     """
     now = get_now()
     end = now + duration
     while now < end:
         now = get_now()
 
 
-class DummyTarget:
+def make_random_solutions(num_sols, data, rng):
     """
-    Dummy optimisation target that implements the OptimisationTarget protocol.
+    Returns a list of ``num_sols`` random solutions.
     """
-
-    def __init__(self, cost: float):
-        self._cost = cost
-
-    def cost(self):
-        return self._cost
+    return [Individual.make_random(data, rng) for _ in range(num_sols)]
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_Individual.py` & `pyvrp-0.2.1/pyvrp/tests/test_Individual.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 from copy import copy, deepcopy
 
+import numpy as np
 from numpy.testing import assert_, assert_equal, assert_raises
+from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import Client, Individual, ProblemData, XorShift128
 from pyvrp.tests.helpers import read
 
 
 def test_route_constructor_sorts_by_empty():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[3, 4], [], [1, 2]])
+    indiv = Individual(data, [[3, 4], [], [1, 2]])
     routes = indiv.get_routes()
 
     # num_routes() should show two non-empty routes. However, we passed in
     # three routes, so len(routes) should not have changed.
     assert_equal(indiv.num_routes(), 2)
     assert_equal(len(routes), 3)
 
@@ -23,36 +24,34 @@
     assert_equal(len(routes[0]), 2)
     assert_equal(len(routes[1]), 2)
     assert_equal(len(routes[2]), 0)
 
 
 def test_route_constructor_raises():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
     assert_equal(data.num_vehicles, 3)
 
     # Only two routes should not raise. But we should always get num_vehicles
     # routes back.
-    individual = Individual(data, pm, [[1, 2], [4, 2]])
+    individual = Individual(data, [[1, 2], [4, 2]])
     assert_equal(len(individual.get_routes()), data.num_vehicles)
 
     # Empty third route should not raise.
-    Individual(data, pm, [[1, 2], [4, 2], []])
+    Individual(data, [[1, 2], [4, 2], []])
 
     # More than three routes should raise, since we only have three vehicles.
     with assert_raises(RuntimeError):
-        Individual(data, pm, [[1], [2], [3], [4]])
+        Individual(data, [[1], [2], [3], [4]])
 
 
 def test_get_neighbours():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[3, 4], [], [1, 2]])
+    indiv = Individual(data, [[3, 4], [], [1, 2]])
     neighbours = indiv.get_neighbours()
 
     expected = [
         (0, 0),  # 0: is depot
         (0, 2),  # 1: between depot (0) to 2
         (1, 0),  # 2: between 1 and depot (0)
         (0, 4),  # 3: between depot (0) and 4
@@ -63,204 +62,216 @@
 
     for client in range(data.num_clients + 1):  # incl. depot
         assert_equal(neighbours[client], expected[client])
 
 
 def test_feasibility():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
     # This solution is infeasible due to both load and time window violations.
-    indiv = Individual(data, pm, [[1, 2, 3, 4]])
+    indiv = Individual(data, [[1, 2, 3, 4]])
     assert_(not indiv.is_feasible())
 
     # First route has total load 18, but vehicle capacity is only 10.
-    assert_(indiv.has_excess_capacity())
+    assert_(indiv.has_excess_load())
 
     # Client 4 has TW [8400, 15300], but client 2 cannot be visited before
     # 15600, so there must be time warp on the single-route solution.
     assert_(indiv.has_time_warp())
 
     # Let's try another solution that's actually feasible.
-    indiv = Individual(data, pm, [[1, 2], [3], [4]])
+    indiv = Individual(data, [[1, 2], [3], [4]])
     assert_(indiv.is_feasible())
-    assert_(not indiv.has_excess_capacity())
+    assert_(not indiv.has_excess_load())
     assert_(not indiv.has_time_warp())
 
 
-def test_distance_cost_calculation():
+def test_distance_calculation():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[1, 2], [3], [4]])
+    indiv = Individual(data, [[1, 2], [3], [4]])
     assert_(indiv.is_feasible())
 
     # Feasible individual, so cost should equal total distance travelled.
     dist = (
         data.dist(0, 1)
         + data.dist(1, 2)
         + data.dist(2, 0)
         + data.dist(0, 3)
         + data.dist(3, 0)
         + data.dist(0, 4)
         + data.dist(4, 0)
     )
+    assert_equal(indiv.distance(), dist)
 
-    assert_equal(indiv.cost(), dist)
 
-
-def test_capacity_cost_calculation():
+def test_excess_load_calculation():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[4, 3, 1, 2]])
-    assert_(indiv.has_excess_capacity())
+    indiv = Individual(data, [[4, 3, 1, 2]])
+    assert_(indiv.has_excess_load())
     assert_(not indiv.has_time_warp())
 
     # All clients are visited on the same route/by the same vehicle. The total
     # demand is 18, but the vehicle capacity is only 10. This has a non-zero
     # load penalty
-    load_penalty = pm.load_penalty(18)
-    assert_(load_penalty > 0)
-
-    # The total costs are now load_penalty + dist
-    dist = (
-        data.dist(0, 4)
-        + data.dist(4, 3)
-        + data.dist(3, 1)
-        + data.dist(1, 2)
-        + data.dist(2, 0)
-    )
+    assert_equal(indiv.excess_load(), 18 - data.vehicle_capacity)
 
-    assert_equal(indiv.cost(), dist + load_penalty)
 
-
-def test_time_warp_cost_calculation():
+def test_time_warp_calculation():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[1, 3], [2, 4]])
-    assert_(not indiv.has_excess_capacity())
+    indiv = Individual(data, [[1, 3], [2, 4]])
+    assert_(not indiv.has_excess_load())
     assert_(indiv.has_time_warp())
 
-    # There's only time warp on the first route: dist(0, 1) = 1'544, so we
+    # There's only time warp on the first route: duration(0, 1) = 1'544, so we
     # arrive at 1 before its opening window of 15'600. Service (360) thus
-    # starts at 15'600, and completes at 15'600 + 360. Then we drive dist(1, 3)
-    # = 1'427, where we arrive after 15'300 (its closing time window). This is
-    # where we incur time warp: we need to 'warp back' to 15'300.
+    # starts at 15'600, and completes at 15'600 + 360. Then we drive for
+    # duration(1, 3) = 1'427, where we arrive after 15'300 (its closing time
+    # window). This is where we incur time warp: we need to 'warp' to 15'300.
     tw_first_route = 15_600 + 360 + 1_427 - 15_300
     tw_second_route = 0
-    tw_penalty = pm.tw_penalty(tw_first_route + tw_second_route)
+    assert_equal(indiv.time_warp(), tw_first_route + tw_second_route)
 
-    # The total costs are now tw_penalty + dist
-    dist = (
-        data.dist(0, 1)
-        + data.dist(1, 3)
-        + data.dist(3, 0)
-        + data.dist(0, 2)
-        + data.dist(2, 4)
-        + data.dist(4, 0)
+
+@mark.parametrize(
+    "dist_mat",
+    [
+        np.full((3, 3), fill_value=100, dtype=int),
+        np.full((3, 3), fill_value=1, dtype=int),
+        np.full((3, 3), fill_value=1000, dtype=int),
+    ],
+)
+def test_time_warp_for_a_very_constrained_problem(dist_mat):
+    """
+    This tests an artificial instance where the second client cannot be reached
+    directly from the depot in a feasible solution, but only after the first
+    client.
+    """
+    dur_mat = [
+        [0, 1, 10],  # cannot get to 2 from depot within 2's time window
+        [1, 0, 1],
+        [1, 1, 0],
+    ]
+
+    data = ProblemData(
+        clients=[
+            Client(x=0, y=0, tw_late=10),
+            Client(x=1, y=0, tw_late=5),
+            Client(x=2, y=0, tw_late=5),
+        ],
+        nb_vehicles=2,
+        vehicle_cap=0,
+        distance_matrix=dist_mat,
+        duration_matrix=dur_mat,
     )
 
-    assert_equal(indiv.cost(), dist + tw_penalty)
+    # This solution directly visits the second client from the depot, which is
+    # not time window feasible.
+    infeasible = Individual(data, [[1], [2]])
+    assert_(infeasible.has_time_warp())
+    assert_(not infeasible.has_excess_load())
+    assert_(not infeasible.is_feasible())
+
+    # But visiting the second client after the first is feasible.
+    feasible = Individual(data, [[1, 2]])
+    assert_(not feasible.has_time_warp())
+    assert_(not feasible.has_excess_load())
+    assert_(feasible.is_feasible())
+
+    assert_equal(
+        feasible.distance(),
+        dist_mat[0, 1] + dist_mat[1, 2] + dist_mat[2, 0],
+    )
 
 
 # TODO test all time warp cases
 
 
 def test_copy():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv = Individual(data, pm, [[1, 2, 3, 4]])
+    indiv = Individual(data, [[1, 2, 3, 4]])
     copy_indiv = copy(indiv)
     deepcopy_indiv = deepcopy(indiv)
 
     # Copied individuals are equal to the original individual
     assert_(indiv == copy_indiv)
     assert_(indiv == deepcopy_indiv)
 
     # But they are not the same object
     assert_(indiv is not copy_indiv)
     assert_(indiv is not deepcopy_indiv)
 
 
 def test_eq():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
 
-    indiv1 = Individual(data, pm, [[1, 2, 3, 4]])
-    indiv2 = Individual(data, pm, [[1, 2], [3], [4]])
-    indiv3 = Individual(data, pm, [[1, 2, 3, 4]])
+    indiv1 = Individual(data, [[1, 2, 3, 4]])
+    indiv2 = Individual(data, [[1, 2], [3], [4]])
+    indiv3 = Individual(data, [[1, 2, 3, 4]])
 
     assert_(indiv1 == indiv1)  # individuals should be equal to themselves
     assert_(indiv2 == indiv2)
     assert_(indiv1 != indiv2)  # different routes, so should not be equal
     assert_(indiv1 == indiv3)  # same solution, different individual
 
-    indiv4 = Individual(data, pm, [[1, 2, 3], [], [4]])
-    indiv5 = Individual(data, pm, [[4], [1, 2, 3], []])
+    indiv4 = Individual(data, [[1, 2, 3], [], [4]])
+    indiv5 = Individual(data, [[4], [1, 2, 3], []])
 
     assert_(indiv4 == indiv5)  # routes are the same, but in different order
 
     # And a few tests against things that are not Individuals, just to be sure
     # there's also a type check in there somewhere.
     assert_(indiv4 != 1)
     assert_(indiv4 != "abc")
     assert_(indiv5 != 5)
     assert_(indiv5 != "cd")
 
 
 def test_str_contains_essential_information():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
     rng = XorShift128(seed=2)
 
     for _ in range(5):  # let's do this a few times to really make sure
-        individual = Individual(data, pm, rng)
+        individual = Individual.make_random(data, rng)
         str_representation = str(individual).splitlines()
 
         routes = individual.get_routes()
         num_routes = individual.num_routes()
 
         # There should be no more than num_routes lines (each detailing a
-        # single route), and a final line containing the cost.
+        # single route), and a final line containing the distance.
         assert_equal(len(str_representation), num_routes + 1)
 
         # The first num_routes lines should each contain a route, where each
         # route should contain every client that is in the route as returned
         # by get_routes().
         for route, str_route in zip(routes[:num_routes], str_representation):
             for client in route:
                 assert_(str(client) in str_route)
 
-        # Last line should contain the cost
-        assert_(str(individual.cost()) in str_representation[-1])
+        # Last line should contain the distance (cost).
+        assert_(str(individual.distance()) in str_representation[-1])
 
 
 def test_hash():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
     rng = XorShift128(seed=2)
 
-    indiv1 = Individual(data, pm, rng)
-    indiv2 = Individual(data, pm, rng)
+    indiv1 = Individual.make_random(data, rng)
+    indiv2 = Individual.make_random(data, rng)
 
     hash1 = hash(indiv1)
     hash2 = hash(indiv2)
 
     # Two random solutions. They're not the same, so the hashes should not be
     # the same either.
     assert_(indiv1 != indiv2)
     assert_(hash1 != hash2)
 
     indiv3 = deepcopy(indiv2)  # is a direct copy
 
     # These two are the same solution, so their hashes should be the same too.
     assert_equal(indiv2, indiv3)
     assert_equal(hash(indiv2), hash(indiv3))
-
-    with pm.get_penalty_booster():
-        # This tests the hash does not depend on obviously changing values,
-        # like the Individual's cost (through the penalty manager).
-        assert_equal(hash(indiv1), hash1)
-        assert_equal(hash(indiv2), hash2)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_Matrix.py` & `pyvrp-0.2.1/pyvrp/tests/test_Matrix.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,41 +1,41 @@
 from numpy.testing import assert_equal, assert_raises
 
-from pyvrp._Matrix import IntMatrix
+from pyvrp._Matrix import Matrix
 
 
 def test_dimension_constructor():
-    square = IntMatrix(10)
+    square = Matrix(10)
     assert_equal(square.size(), 10 * 10)
     assert_equal(square.max(), 0)  # matrix initialises all zero
 
-    rectangle = IntMatrix(10, 20)
+    rectangle = Matrix(10, 20)
     assert_equal(rectangle.size(), 10 * 20)
     assert_equal(rectangle.max(), 0)  # matrix initialises all zero
 
 
 def test_data_constructor():
-    empty = IntMatrix([[], []])
+    empty = Matrix([[], []])
     assert_equal(empty.size(), 0)
 
-    non_empty = IntMatrix([[1, 2], [1, 3]])
+    non_empty = Matrix([[1, 2], [1, 3]])
     assert_equal(non_empty.size(), 4)  # matrix has four elements
     assert_equal(non_empty.max(), 3)
 
 
 def test_data_constructor_throws():
     with assert_raises(ValueError):
-        IntMatrix([[1, 2], []])  # second row shorter than first
+        Matrix([[1, 2], []])  # second row shorter than first
 
     with assert_raises(ValueError):
-        IntMatrix([[1, 2], [1, 2, 3]])  # second row longer than first
+        Matrix([[1, 2], [1, 2, 3]])  # second row longer than first
 
 
 def test_element_access():
-    mat = IntMatrix(10)
+    mat = Matrix(10)
 
     for i in range(10):
         for j in range(10):
             mat[i, j] = i + j
 
     assert_equal(mat.max(), 9 + 9)  # maximum value
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_PenaltyManager.py` & `pyvrp-0.2.1/pyvrp/tests/test_PenaltyManager.py`

 * *Files 14% similar despite different names*

```diff
@@ -39,244 +39,209 @@
             num_iters_between_penalty_updates,
             penalty_increase,
             penalty_decrease,
             target_feasible,
         )
 
 
-def test_load_penalty():
-    params = PenaltyParams(2, 1, 1, 1, 1, 1, 1)
-    pm = PenaltyManager(1, params)
-
-    assert_equal(pm.load_penalty(0), 0)  # below capacity
-    assert_equal(pm.load_penalty(1), 0)  # at capacity
-
-    # Penalty per unit excess capacity is 2
-    assert_equal(pm.load_penalty(2), 2)  # 1 unit above capacity
-    assert_equal(pm.load_penalty(3), 4)  # 2 units above capacity
-
-    # Penalty per unit excess capacity is 4
-    params = PenaltyParams(4, 1, 1, 1, 1, 1, 1)
-    pm = PenaltyManager(1, params)
-
-    assert_equal(pm.load_penalty(2), 4)  # 1 unit above capacity
-    assert_equal(pm.load_penalty(3), 8)  # 2 units above capacity
-
-
-def test_tw_penalty():
-    params = PenaltyParams(1, 2, 1, 1, 1, 1, 1)
-    pm = PenaltyManager(1, params)
-
-    # Penalty per unit time warp is 2
-    assert_equal(pm.tw_penalty(0), 0)
-    assert_equal(pm.tw_penalty(1), 2)
-    assert_equal(pm.tw_penalty(2), 4)
-
-    params = PenaltyParams(1, 4, 1, 1, 1, 1, 1)
-    pm = PenaltyManager(1, params)
-
-    # Penalty per unit excess capacity is now 4
-    assert_equal(pm.tw_penalty(0), 0)
-    assert_equal(pm.tw_penalty(1), 4)
-    assert_equal(pm.tw_penalty(2), 8)
-
-
 def test_repair_booster():
     params = PenaltyParams(1, 1, 5, 1, 1, 1, 1)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
+
+    cost_evaluator = pm.get_cost_evaluator()
 
-    assert_equal(pm.tw_penalty(1), 1)
-    assert_equal(pm.load_penalty(2), 1)  # 1 unit above capacity
+    assert_equal(cost_evaluator.tw_penalty(1), 1)
+    assert_equal(cost_evaluator.load_penalty(2, 1), 1)  # 1 unit above capacity
 
-    # While the booster lives, the penalty values are multiplied by the
+    # With the booster, the penalty values are multiplied by the
     # repairBooster term (x5 in this case).
-    with pm.get_penalty_booster():
-        assert_equal(pm.tw_penalty(1), 5)
-        assert_equal(pm.tw_penalty(2), 10)
-
-        assert_equal(pm.load_penalty(2), 5)  # 1 unit above capacity
-        assert_equal(pm.load_penalty(3), 10)  # 2 units above capacity
-
-    # Booster no longer in scope, so penalties should return to normal.
-    assert_equal(pm.tw_penalty(1), 1)
-    assert_equal(pm.load_penalty(2), 1)  # 1 unit above capacity
+    booster = pm.get_booster_cost_evaluator()
+    assert_equal(booster.tw_penalty(1), 5)
+    assert_equal(booster.tw_penalty(2), 10)
+
+    assert_equal(booster.load_penalty(2, 1), 5)  # 1 unit above capacity
+    assert_equal(booster.load_penalty(3, 1), 10)  # 2 units above capacity
+
+    # Test that using booster did not affect normal cost_evaluator.
+    assert_equal(cost_evaluator.tw_penalty(1), 1)
+    assert_equal(cost_evaluator.load_penalty(2, 1), 1)  # 1 unit above capacity
 
 
 def test_capacity_penalty_update_increase():
     num_registerations = 4
     params = PenaltyParams(1, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
     # Within bandwidth, so penalty should not change.
-    assert_equal(pm.load_penalty(2), 1)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1)
     for feas in [True, False, True, False]:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 1)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1)
 
     # Below targetFeasible, so should increase the capacityPenalty by +1
     # (normally to 1.1 due to penaltyIncrease, but we should not end up at the
     # same int).
     for feas in [False] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 2)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 2)
 
     # Now we start from a much bigger initial capacityPenalty. Here we want the
     # penalty to increase by 10% due to penaltyIncrease = 1.1, and +1 due to
     # double -> int.
     params = PenaltyParams(100, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.load_penalty(2), 100)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 100)
     for feas in [False] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 111)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 111)
 
     # Test that the penalty cannot increase beyond 1000, its maximum value.
     params = PenaltyParams(1000, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.load_penalty(2), 1000)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1000)
     for feas in [False] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 1000)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1000)
 
 
 def test_capacity_penalty_update_decrease():
     num_registerations = 4
     params = PenaltyParams(4, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
     # Within bandwidth, so penalty should not change.
-    assert_equal(pm.load_penalty(2), 4)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 4)
     for feas in [True, False, True, False]:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 4)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 4)
 
     # Above targetFeasible, so should decrease the capacityPenalty to 90%, and
     # -1 from the bounds check. So 0.9 * 4 = 3.6, 3.6 - 1 = 2.6, (int) 2.6 = 2
     for feas in [True] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 2)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 2)
 
     # Now we start from a much bigger initial capacityPenalty. Here we want the
     # penalty to decrease by 10% due to penaltyDecrease = 0.9, and -1 due to
     # double -> int.
     params = PenaltyParams(100, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.load_penalty(2), 100)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 100)
     for feas in [True] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 89)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 89)
 
     # Test that the penalty cannot decrease beyond 1, its minimum value.
     params = PenaltyParams(1, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.load_penalty(2), 1)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1)
     for feas in [True] * num_registerations:
         pm.register_load_feasible(feas)
-    assert_equal(pm.load_penalty(2), 1)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 1)
 
 
 def test_time_warp_penalty_update_increase():
     num_registerations = 4
     params = PenaltyParams(1, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
     # Within bandwidth, so penalty should not change.
-    assert_equal(pm.tw_penalty(1), 1)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1)
     for feas in [True, False, True, False]:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 1)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1)
 
     # Below targetFeasible, so should increase the tw penalty by +1
     # (normally to 1.1 due to penaltyIncrease, but we should not end up at the
     # same int).
     for feas in [False] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 2)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 2)
 
     # Now we start from a much bigger initial tw penalty. Here we want
     # the penalty to increase by 10% due to penaltyIncrease = 1.1, and +1 due
     # to double -> int.
     params = PenaltyParams(1, 100, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.tw_penalty(1), 100)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 100)
     for feas in [False] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 111)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 111)
 
     # Test that the penalty cannot increase beyond 1000, its maximum value.
     params = PenaltyParams(1, 1000, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.tw_penalty(1), 1000)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1000)
     for feas in [False] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 1000)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1000)
 
 
 def test_time_warp_penalty_update_decrease():
     num_registerations = 4
     params = PenaltyParams(1, 4, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
     # Within bandwidth, so penalty should not change.
-    assert_equal(pm.tw_penalty(1), 4)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 4)
     for feas in [True, False, True, False]:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 4)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 4)
 
     # Above targetFeasible, so should decrease the timeWarPenalty to 90%, and
     # -1 from the bounds check. So 0.9 * 4 = 3.6, 3.6 - 1 = 2.6, (int) 2.6 = 2
     for feas in [True] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 2)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 2)
 
     # Now we start from a much bigger initial timeWarpCapacity. Here we want
     # the penalty to decrease by 10% due to penaltyDecrease = 0.9, and -1 due
     # to double -> int.
     params = PenaltyParams(1, 100, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.tw_penalty(1), 100)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 100)
     for feas in [True] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 89)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 89)
 
     # Test that the penalty cannot decrease beyond 1, its minimum value.
     params = PenaltyParams(1, 1, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
-    assert_equal(pm.tw_penalty(1), 1)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1)
     for feas in [True] * num_registerations:
         pm.register_time_feasible(feas)
-    assert_equal(pm.tw_penalty(1), 1)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 1)
 
 
 def test_does_not_update_penalties_before_sufficient_registrations():
     num_registerations = 4
     params = PenaltyParams(4, 4, 1, num_registerations, 1.1, 0.9, 0.5)
-    pm = PenaltyManager(1, params)
+    pm = PenaltyManager(params)
 
     # Both have four initial penalty, and vehicle capacity is one.
-    assert_equal(pm.tw_penalty(1), 4)
-    assert_equal(pm.load_penalty(2), 4)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 4)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 4)
 
     # Register three times. We need at least four registrations before the
     # penalties are updated, so this should not change anything.
     for feas in [True, False, True]:
         pm.register_time_feasible(feas)
-        assert_equal(pm.tw_penalty(1), 4)
+        assert_equal(pm.get_cost_evaluator().tw_penalty(1), 4)
 
         pm.register_load_feasible(feas)
-        assert_equal(pm.load_penalty(2), 4)
+        assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 4)
 
     # Register a fourth time. Now the penalties should change. Since there are
     # more feasible registrations than desired, the penalties should decrease.
     pm.register_load_feasible(True)
-    assert_equal(pm.load_penalty(2), 2)
+    assert_equal(pm.get_cost_evaluator().load_penalty(2, 1), 2)
 
     pm.register_time_feasible(True)
-    assert_equal(pm.tw_penalty(1), 2)
+    assert_equal(pm.get_cost_evaluator().tw_penalty(1), 2)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_Population.py` & `pyvrp-0.2.1/pyvrp/tests/test_Population.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 import numpy as np
 from numpy.testing import assert_, assert_allclose, assert_equal, assert_raises
 from pytest import mark
 
 from pyvrp import (
+    CostEvaluator,
     Individual,
-    PenaltyManager,
     Population,
     PopulationParams,
     XorShift128,
 )
-from pyvrp.diversity import broken_pairs_distance
-from pyvrp.tests.helpers import read
+from pyvrp.diversity import broken_pairs_distance as bpd
+from pyvrp.tests.helpers import make_random_solutions, read
 
 
 @mark.parametrize(
     "min_pop_size,"
     "generation_size,"
     "nb_elite,"
     "nb_close,"
@@ -94,236 +94,264 @@
     assert_allclose(params.lb_diversity, lb_diversity)
     assert_allclose(params.ub_diversity, ub_diversity)
     assert_equal(params.max_pop_size, min_pop_size + generation_size)
 
 
 def test_add_triggers_purge():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
 
     params = PopulationParams()
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
+    pop = Population(bpd, params=params)
+
+    for indiv in make_random_solutions(params.min_pop_size, data, rng):
+        pop.add(indiv, cost_evaluator)
 
     # Population should initialise at least min_pop_size individuals
     assert_(len(pop) >= params.min_pop_size)
     assert_equal(len(pop), pop.num_feasible() + pop.num_infeasible())
 
     num_feas = pop.num_feasible()
     num_infeas = pop.num_infeasible()
 
     while True:  # keep adding feasible individuals until we are about to purge
-        individual = Individual(data, pm, rng)
+        individual = Individual.make_random(data, rng)
 
         if individual.is_feasible():
-            pop.add(individual)
+            pop.add(individual, cost_evaluator)
             num_feas += 1
 
             assert_equal(len(pop), num_feas + num_infeas)
             assert_equal(pop.num_feasible(), num_feas)
 
         if num_feas == params.max_pop_size:  # next add() triggers purge
             break
 
     # RNG is fixed, and this next individual is feasible. Since we now have a
     # feasible population that is of maximal size, adding this individual
     # should trigger survivor selection (purge). Survivor selection reduces the
     # feasible subpopulation to min_pop_size, so the overal population is then
     # just num_infeas + min_pop_size.
-    individual = Individual(data, pm, rng)
+    individual = Individual.make_random(data, rng)
     assert_(individual.is_feasible())
 
-    pop.add(individual)
+    pop.add(individual, cost_evaluator)
     assert_equal(pop.num_feasible(), params.min_pop_size)
     assert_equal(len(pop), num_infeas + params.min_pop_size)
 
 
 def test_select_returns_same_parents_if_no_other_option():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=2_147_483_647)
 
     params = PopulationParams(min_pop_size=0)
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
+    pop = Population(bpd, params=params)
 
     assert_equal(len(pop), 0)
 
-    pop.add(Individual(data, pm, [[3, 2], [1, 4], []]))
+    pop.add(Individual(data, [[3, 2], [1, 4]]), cost_evaluator)
     assert_equal(len(pop), 1)
 
     # We added a single individual, so we should now get the same parent twice.
-    parents = pop.select()
+    parents = pop.select(rng, cost_evaluator)
     assert_(parents[0] == parents[1])
 
     # Now we add another, different individual.
-    pop.add(Individual(data, pm, [[3, 2], [1], [4]]))
+    pop.add(Individual(data, [[3, 2], [1], [4]]), cost_evaluator)
     assert_equal(len(pop), 2)
 
     # We should now get two different individuals as parents, at least most of
     # the time. The actual probability of getting the same parents is very
     # small, but not zero. So let's do an experiment where we do 1000 selects,
     # and collect the number of times the parents are different.
     different_parents = 0
     for _ in range(1_000):
-        parents = pop.select()
+        parents = pop.select(rng, cost_evaluator)
         different_parents += parents[0] != parents[1]
 
     # The probability of selecting different parents is very close to 100%, so
     # we would expect to observe different parents much more than 90% of the
     # time. At the same time, it is very unlikely each one of the 1000 selects
     # returns a different parent pair.
     assert_(900 < different_parents < 1_000)
 
 
 # // TODO test more select() - diversity, feas/infeas pairs
 
 
-def test_restart_generates_min_pop_size_new_individuals():
-    """
-    Tests if restarting the population will generate ``min_pop_size`` new
-    individuals.
-    """
-    data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.vehicle_capacity)
-    rng = XorShift128(seed=12)
-
-    params = PopulationParams()
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
-
-    old = {individual for individual in pop}
-    pop.restart()
-    new = {individual for individual in pop}
-
-    assert_equal(len(pop), params.min_pop_size)
-    assert_equal(len(old & new), 0)  # no old pops survived the restart
-
-
 def test_population_is_empty_with_zero_min_pop_size_and_generation_size():
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=12)
 
     params = PopulationParams(min_pop_size=0, generation_size=0)
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
+    pop = Population(bpd, params=params)
 
     assert_equal(len(pop), 0)
 
     for _ in range(10):
         # With zero min_pop_size and zero generation_size, every additional
         # individual triggers a purge. So the population size can never grow
         # beyond zero.
-        pop.add(Individual(data, pm, rng))
+        pop.add(Individual.make_random(data, rng), cost_evaluator)
         assert_equal(len(pop), 0)
 
 
 @mark.parametrize("nb_elite", [5, 25])
 def test_elite_individuals_are_not_purged(nb_elite: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     params = PopulationParams(nb_elite=nb_elite)
     rng = XorShift128(seed=42)
 
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
+    pop = Population(bpd, params=params)
 
     # Keep adding individuals until the infeasible subpopulation is of maximum
     # size.
     while pop.num_infeasible() != params.max_pop_size:
-        pop.add(Individual(data, pm, rng))
+        pop.add(Individual.make_random(data, rng), cost_evaluator)
 
     assert_equal(pop.num_infeasible(), params.max_pop_size)
 
     # These are the nb_elite best solutions in the current solution pool. These
     # should never be purged.
     curr_individuals = [
         individual for individual in pop if not individual.is_feasible()
     ]
 
-    best_individuals = sorted(curr_individuals, key=lambda indiv: indiv.cost())
+    best_individuals = sorted(
+        curr_individuals, key=cost_evaluator.penalised_cost
+    )
     elite_individuals = best_individuals[:nb_elite]
 
     # Add a solution that is certainly not feasible, thus causing a purge.
     single_route = [client for client in range(1, data.num_clients + 1)]
-    pop.add(Individual(data, pm, [single_route]))
+    pop.add(Individual(data, [single_route]), cost_evaluator)
 
     # After the purge, there should remain min_pop_size infeasible solutions.
     assert_equal(pop.num_infeasible(), params.min_pop_size)
 
     # In the infeasible subpopulation, nb_elite solutions from before the purge
     # should also still be present. We test that by selecting the nb_elite best
     # individuals from before the purge. We test by id/memory location because
     # these individuals should still be present, unmodified.
     new_individuals = [id(individual) for individual in pop]
     for elite_individual in elite_individuals:
         assert_(id(elite_individual) in new_individuals)
 
 
-def test_binary_tournament_ranks_by_fitness():
+@mark.parametrize("k", [2, 3])
+def test_tournament_ranks_by_fitness(k: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
-    params = PopulationParams()
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
+    pop = Population(bpd)
 
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
-
-    for _ in range(50):
-        pop.add(Individual(data, pm, rng))
+    for individual in make_random_solutions(50, data, rng):
+        if not individual.is_feasible():
+            pop.add(individual, cost_evaluator)
 
     assert_equal(pop.num_feasible(), 0)
 
     # Since this test requires the fitness values of the individuals, we have
     # to access the underlying infeasible subpopulation directly.
-    infeas = [item for item in pop._infeas]
-    infeas = sorted(infeas, key=lambda item: item.fitness)
-    infeas = {item.individual: idx for idx, item in enumerate(infeas)}
-    infeas_count = np.zeros(len(infeas))
+    infeas_pop = pop._infeas
+    infeas_pop.update_fitness(cost_evaluator)
 
-    for _ in range(10_000):
-        indiv = pop.get_binary_tournament()
-        infeas_count[infeas[indiv]] += 1
+    items = [item for item in pop._infeas]
+    by_fitness = sorted(items, key=lambda item: item.fitness)
+    indiv2idx = {item.individual: idx for idx, item in enumerate(by_fitness)}
+    infeas_count = np.zeros(len(infeas_pop))
 
-    # Now we compare the observed ranking from the binary tournament selection
-    # against what we would expect from the actual fitness ranking. We compute
-    # the percentage of times we're incorrect, and test that that number is not
-    # too high.
-    actual_rank = np.argsort(-infeas_count)  # higher is better
-    expected_rank = np.arange(len(infeas))
-    pct_off = np.abs((actual_rank - expected_rank) / len(infeas)).mean()
+    for _ in range(10_000):
+        indiv = pop.get_tournament(rng, cost_evaluator, k=k)
+        infeas_count[indiv2idx[indiv]] += 1
 
+    # Now we compare the observed ranking from the tournament selection with
+    # what we expect from the actual fitness ranking. We compute the percentage
+    # of times we're incorrect, and test that that number is not too high.
+    actual_rank = 1 + np.argsort(-infeas_count)  # higher is better
+    expected_rank = 1 + np.arange(len(infeas_pop))
+    pct_off = np.abs((actual_rank - expected_rank) / len(infeas_pop)).mean()
     assert_(pct_off < 0.05)
 
+    # Previous test compared just rank. Now we compare expected frequency. An
+    # item at rank i wins only when the other k - 1 items have a rank lower
+    # than i. That happens with probability roughly proportional to
+    #   (1 - i / #pop) ** (k - 1)
+    actual_freq = infeas_count / infeas_count.sum()
+    expected_freq = (1 - expected_rank / len(infeas_pop)) ** (k - 1)
+    expected_freq /= expected_freq.sum()
+    assert_allclose(actual_freq, expected_freq, atol=0.01)  # 1% tolerance
+
+
+@mark.parametrize("k", [-100, -1, 0])  # k must be strictly positive
+def test_tournament_raises_for_invalid_k(k: int):
+    data = read("data/RC208.txt", "solomon", "dimacs")
+    cost_evaluator = CostEvaluator(20, 6)
+    rng = XorShift128(seed=42)
+    pop = Population(bpd)
+
+    for individual in make_random_solutions(5, data, rng):
+        pop.add(individual, cost_evaluator)
+
+    with assert_raises(ValueError):
+        pop.get_tournament(rng, cost_evaluator, k=k)
+
 
 def test_purge_removes_duplicates():
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     params = PopulationParams(min_pop_size=20, generation_size=5)
     rng = XorShift128(seed=42)
 
-    pop = Population(data, pm, rng, broken_pairs_distance, params)
+    pop = Population(bpd, params=params)
+
+    for indiv in make_random_solutions(params.min_pop_size, data, rng):
+        pop.add(indiv, cost_evaluator)
+
     assert_equal(len(pop), params.min_pop_size)
 
     # This is the individual we are going to add a few times. That should make
     # sure the relevant subpopulation definitely contains duplicates.
-    individual = Individual(data, pm, rng)
+    individual = Individual.make_random(data, rng)
     assert_(not individual.is_feasible())
 
     for _ in range(params.generation_size):
-        pop.add(individual)
+        pop.add(individual, cost_evaluator)
 
     # Make sure we have not yet purged, and increase the minimum population
     # size by one to make sure we're definitely not removing *all* of the
     # duplicate individuals.
     assert_(pop.num_infeasible() != params.min_pop_size)
     params.min_pop_size += 1
 
     # Keep adding individuals until we have had a purge, and returned to the
     # minimum population size.
     while pop.num_infeasible() != params.min_pop_size:
-        pop.add(Individual(data, pm, rng))
+        pop.add(Individual.make_random(data, rng), cost_evaluator)
 
     # Since duplicates are purged first, there should now be only one of them
     # in the subpopulation. There cannot be zero, because we made sure of that.
     duplicates = 0
     for other in pop:
         if other == individual:
             duplicates += 1
 
     assert_equal(duplicates, 1)
+
+
+def test_clear():
+    data = read("data/RC208.txt", "solomon", "dimacs")
+    cost_evaluator = CostEvaluator(20, 6)
+    rng = XorShift128(seed=42)
+    pop = Population(bpd)
+
+    for individual in make_random_solutions(10, data, rng):
+        pop.add(individual, cost_evaluator)
+
+    assert_equal(len(pop), 10)
+
+    pop.clear()
+    assert_equal(len(pop), 0)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_Result.py` & `pyvrp-0.2.1/pyvrp/tests/test_Result.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,79 +1,87 @@
+import math
+
 from numpy.testing import assert_, assert_allclose, assert_equal, assert_raises
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, Population, XorShift128
+from pyvrp import CostEvaluator, Individual, Population, XorShift128
 from pyvrp.Result import Result
 from pyvrp.Statistics import Statistics
 from pyvrp.diversity import broken_pairs_distance
 from pyvrp.tests.helpers import read
 
 
 @mark.parametrize(
     "routes, num_iterations, runtime",
     [([[1, 2], [3], [4]], 1, 1.5), ([[1, 2, 3, 4]], 100, 54.2)],
 )
 def test_fields_are_correctly_set(routes, num_iterations, runtime):
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
-    indiv = Individual(data, pm, routes)
+    indiv = Individual(data, routes)
 
     res = Result(indiv, Statistics(), num_iterations, runtime)
 
     assert_equal(res.is_feasible(), indiv.is_feasible())
     assert_equal(res.num_iterations, num_iterations)
-    assert_allclose(res.cost(), indiv.cost())
+    if indiv.is_feasible():
+        assert_allclose(res.cost(), CostEvaluator().cost(indiv))
+    else:
+        assert_equal(res.cost(), math.inf)
     assert_allclose(res.runtime, runtime)
 
 
 @mark.parametrize(
     "num_iterations, runtime",
     [
         (-1, 0.0),  # num_iterations < 0
         (0, -1.0),  # runtime < 0
     ],
 )
 def test_init_raises_invalid_arguments(num_iterations, runtime):
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
-    indiv = Individual(data, pm, [[1, 2, 3, 4], [], []])
+    indiv = Individual(data, [[1, 2, 3, 4], [], []])
 
     with assert_raises(ValueError):
         Result(indiv, Statistics(), num_iterations, runtime)
 
 
 @mark.parametrize(
     "num_iterations, has_statistics", [(0, False), (1, True), (10, True)]
 )
 def test_has_statistics(num_iterations: int, has_statistics: bool):
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
-    pop = Population(data, pm, rng, broken_pairs_distance)
+    pop = Population(broken_pairs_distance)
     stats = Statistics()
 
     for _ in range(num_iterations):
-        stats.collect_from(pop)
+        stats.collect_from(pop, cost_evaluator)
 
-    res = Result(Individual(data, pm, rng), stats, num_iterations, 0.0)
+    best = Individual.make_random(data, rng)
+    res = Result(best, stats, num_iterations, 0.0)
     assert_equal(res.has_statistics(), has_statistics)
     assert_equal(res.num_iterations, num_iterations)
 
 
-def test_str_contains_essential_information():
+@mark.parametrize(
+    "routes",
+    [[[1, 2], [3], [4]], [[1, 2, 3, 4]]],
+)
+def test_str_contains_essential_information(routes):
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
-    rng = XorShift128(seed=42)
 
-    for _ in range(5):  # let's do this a few times to really make sure
-        individual = Individual(data, pm, rng)
-        res = Result(individual, Statistics(), 0, 0.0)
-        str_representation = str(res)
-
-        # Test that feasibility status and solution cost are presented.
-        assert_(str(individual.cost()) in str_representation)
-        assert_(str(individual.is_feasible()) in str_representation)
-
-        # And make sure that all non-empty routes are printed as well.
-        for route in individual.get_routes():
-            if route:
-                assert_(str(route) in str_representation)
+    individual = Individual(data, routes)
+    res = Result(individual, Statistics(), 0, 0.0)
+    str_representation = str(res)
+
+    # Test that feasibility status and solution cost are presented.
+    if individual.is_feasible():
+        cost = CostEvaluator().cost(individual)
+        assert_(str(cost) in str_representation)
+    else:
+        assert_("INFEASIBLE" in str_representation)
+
+    # And make sure that all non-empty routes are printed as well.
+    for route in individual.get_routes():
+        if route:
+            assert_(str(route) in str_representation)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_Statistics.py` & `pyvrp-0.2.1/pyvrp/tests/test_Statistics.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,24 +1,27 @@
 from numpy.testing import assert_, assert_equal
 
-from pyvrp import PenaltyManager, Population, Statistics, XorShift128
+from pyvrp import CostEvaluator, Population, Statistics, XorShift128
 from pyvrp.diversity import broken_pairs_distance
-from pyvrp.tests.helpers import read
+from pyvrp.tests.helpers import make_random_solutions, read
 
 
 def test_csv_serialises_correctly(tmp_path):
     data = read("data/OkSmall.txt")
-    pm = PenaltyManager(data.vehicle_capacity)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=42)
-    pop = Population(data, pm, rng, broken_pairs_distance)
+    pop = Population(broken_pairs_distance)
+
+    for individual in make_random_solutions(10, data, rng):
+        pop.add(individual, cost_evaluator)
 
     collected_stats = Statistics()
 
     for _ in range(10):  # populate the statistics object
-        collected_stats.collect_from(pop)
+        collected_stats.collect_from(pop, cost_evaluator)
 
     csv_path = tmp_path / "test.csv"
     assert_(not csv_path.exists())
 
     # Write the collected statistcs to the CSV file location, and check that
     # the file now does exist.
     collected_stats.to_csv(csv_path)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_SubPopulation.py` & `pyvrp-0.2.1/pyvrp/tests/test_SubPopulation.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,98 +1,102 @@
 import numpy as np
 from numpy.testing import assert_, assert_allclose, assert_equal
 from pytest import mark
 
-from pyvrp import Individual, PenaltyManager, XorShift128
+from pyvrp import CostEvaluator, Individual, XorShift128
 from pyvrp._SubPopulation import PopulationParams, SubPopulation
 from pyvrp.diversity import broken_pairs_distance as bpd
 from pyvrp.tests.helpers import read
 
 
 @mark.parametrize("nb_close", [5, 10, 25])
 def test_avg_distance_closest_is_same_up_to_nb_close(nb_close: int):
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=5)
 
     params = PopulationParams(
         min_pop_size=0, generation_size=250, nb_close=nb_close
     )
 
     subpop = SubPopulation(bpd, params)
     assert_equal(len(subpop), 0)
 
     for _ in range(nb_close):
-        subpop.add(Individual(data, pm, rng))
+        subpop.add(Individual.make_random(data, rng), cost_evaluator)
 
     # The first nb_close individuals all have each other in their "closest"
     # list. The averages only differ because each individual is themselves not
     # in their own list. So we would expect these values to all be pretty
     # similar.
     distances = np.array([item.avg_distance_closest() for item in subpop])
     assert_allclose(distances, distances.mean(), rtol=1 / len(subpop))
     assert_equal(len(subpop), nb_close)
 
     # Let's add a significantly larger set of individuals.
     for _ in range(250 - nb_close):
-        subpop.add(Individual(data, pm, rng))
+        subpop.add(Individual.make_random(data, rng), cost_evaluator)
 
     # Now the "closest" lists should differ quite a bit between individuals,
     # and the average distances should thus not all be the same any more.
     distances = np.array([item.avg_distance_closest() for item in subpop])
     assert_equal(len(subpop), params.max_pop_size)
     assert_(not np.allclose(distances, distances.mean(), rtol=1 / len(subpop)))
 
 
 def test_avg_distance_closest_for_single_route_solutions():
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     params = PopulationParams(min_pop_size=0, nb_close=10)
 
     subpop = SubPopulation(bpd, params)
     assert_equal(len(subpop), 0)
 
     single_route = [client for client in range(1, data.num_clients + 1)]
 
     for offset in range(params.max_pop_size):
         # This is a single-route solution, but the route is continually shifted
         # (or rotated) around the depot.
         shifted_route = single_route[-offset:] + single_route[:-offset]
-        shifted = Individual(data, pm, [shifted_route])
+        shifted = Individual(data, [shifted_route])
 
         for item in subpop:
             # Every individual already in the subpopulation has exactly two
             # broken links with this new shifted individual, both around the
             # depot. So the average broken pairs distance is 2 / num_clients
             # for all of them.
             assert_equal(bpd(item.individual, shifted), 2 / data.num_clients)
 
-        subpop.add(shifted)
+        subpop.add(shifted, cost_evaluator)
         assert_equal(len(subpop), offset + 1)
 
         # Since the broken pairs distance is the same for all individuals, the
         # average distance amongst the closest individuals should also be the
         # same for all of them.
         distances = np.array([item.avg_distance_closest() for item in subpop])
         assert_allclose(distances, distances.mean())
 
 
 def test_fitness_is_purely_based_on_cost_when_only_elites():
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=51)
     params = PopulationParams(nb_elite=25, min_pop_size=25)
     subpop = SubPopulation(bpd, params)
 
     for _ in range(params.min_pop_size):
-        subpop.add(Individual(data, pm, rng))
+        subpop.add(Individual.make_random(data, rng), cost_evaluator)
+    # We need to call update_fitness before accessing the fitness
+    subpop.update_fitness(cost_evaluator)
 
     # When all individuals are elite the diversity weight term drops out, and
     # fitness rankings are purely based on the cost ranking.
-    cost = np.array([item.individual.cost() for item in subpop])
+    cost = np.array(
+        [cost_evaluator.penalised_cost(item.individual) for item in subpop]
+    )
     by_cost = np.argsort(cost, kind="stable")
 
     rank = np.empty(len(subpop))
     rank[by_cost] = np.arange(len(subpop))
 
     expected_fitness = rank / (2 * len(subpop))
     actual_fitness = np.array([item.fitness for item in subpop])
@@ -101,25 +105,29 @@
     # agree with what we've computed above.
     assert_(((0 <= actual_fitness) & (actual_fitness <= 1)).all())
     assert_allclose(actual_fitness, expected_fitness)
 
 
 def test_fitness_is_average_of_cost_and_diversity_when_no_elites():
     data = read("data/RC208.txt", "solomon", "dimacs")
-    pm = PenaltyManager(data.num_vehicles)
+    cost_evaluator = CostEvaluator(20, 6)
     rng = XorShift128(seed=52)
     params = PopulationParams(nb_elite=0, min_pop_size=25)
     subpop = SubPopulation(bpd, params)
 
     for _ in range(params.min_pop_size):
-        subpop.add(Individual(data, pm, rng))
+        subpop.add(Individual.make_random(data, rng), cost_evaluator)
+    # We need to call update_fitness before accessing the fitness
+    subpop.update_fitness(cost_evaluator)
 
     # When no individuals are elite, the fitness ranking is based on the mean
     # of the cost and diversity ranks.
-    cost = np.array([item.individual.cost() for item in subpop])
+    cost = np.array(
+        [cost_evaluator.penalised_cost(item.individual) for item in subpop]
+    )
     cost_rank = np.argsort(cost, kind="stable")
 
     diversity = np.array([item.avg_distance_closest() for item in subpop])
     div_rank = np.argsort(-diversity[cost_rank], kind="stable")
 
     ranks = np.empty((len(subpop), 2))
     ranks[cost_rank, 0] = np.arange(len(subpop))
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_TimeWindowSegment.py` & `pyvrp-0.2.1/pyvrp/tests/test_TimeWindowSegment.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,46 +1,45 @@
 from numpy.testing import assert_equal
 from pytest import mark
 
-from pyvrp._Matrix import IntMatrix
+from pyvrp._Matrix import Matrix
 from pyvrp._TimeWindowSegment import TimeWindowSegment
 
 
 @mark.parametrize("existing_time_warp", [2, 5, 10])
 def test_total_time_warp(existing_time_warp):
-    mat = IntMatrix(0)
-    tws1 = TimeWindowSegment(mat, 0, 0, 0, existing_time_warp, 0, 0)
+    tws1 = TimeWindowSegment(0, 0, 0, existing_time_warp, 0, 0)
     assert_equal(tws1.total_time_warp(), existing_time_warp)
 
 
 def test_merge_two():
-    mat = IntMatrix([[1, 4], [1, 2]])
-    tws1 = TimeWindowSegment(mat, 0, 0, 5, 0, 0, 5)
-    tws2 = TimeWindowSegment(mat, 1, 1, 0, 5, 3, 6)
+    tws1 = TimeWindowSegment(0, 0, 5, 0, 0, 5)
+    tws2 = TimeWindowSegment(1, 1, 0, 5, 3, 6)
 
-    merged = TimeWindowSegment.merge(tws1, tws2)
+    mat = Matrix([[1, 4], [1, 2]])
+    merged = TimeWindowSegment.merge(mat, tws1, tws2)
 
     # There is no release time, so segment time warp and total time warp should
     # be equal. The first stop (tws1) takes already has five duration, and
     # starts at time 0. Then, we have to drive for 4 units (mat(0, 1) = 4) to
     # get to the second stop (tws2). This second segment has 5 time warp, and
     # we arrive there at time 5 + 4 = 9, which is 9 - 6 = 3 after its closing
     # time window. So we get a final time warp of 5 + 3 = 8.
     assert_equal(merged.total_time_warp(), 8)
 
 
 def test_merge_multiple():
-    mat = IntMatrix([[1, 4, 1], [1, 2, 4], [1, 1, 1]])
-    tws1 = TimeWindowSegment(mat, 0, 0, 5, 0, 0, 5)
-    tws2 = TimeWindowSegment(mat, 1, 1, 0, 0, 3, 6)
-    tws3 = TimeWindowSegment(mat, 2, 2, 0, 0, 2, 3)
-
-    merged1 = TimeWindowSegment.merge(tws1, tws2)
-    merged2 = TimeWindowSegment.merge(merged1, tws3)
-    merged3 = TimeWindowSegment.merge(tws1, tws2, tws3)
+    tws1 = TimeWindowSegment(0, 0, 5, 0, 0, 5)
+    tws2 = TimeWindowSegment(1, 1, 0, 0, 3, 6)
+    tws3 = TimeWindowSegment(2, 2, 0, 0, 2, 3)
+
+    mat = Matrix([[1, 4, 1], [1, 2, 4], [1, 1, 1]])
+    merged1 = TimeWindowSegment.merge(mat, tws1, tws2)
+    merged2 = TimeWindowSegment.merge(mat, merged1, tws3)
+    merged3 = TimeWindowSegment.merge(mat, tws1, tws2, tws3)
 
     # Merge all together should be the same as merging in several steps.
     assert_equal(merged3.total_time_warp(), merged2.total_time_warp())
 
     # After also merging in tws3, we should have 3 time warp from 0 -> 1, and 7
     # time warp from 1 -> 2, for 10 total time warp.
     assert_equal(merged3.total_time_warp(), 10)
```

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_XorShift128.py` & `pyvrp-0.2.1/pyvrp/tests/test_XorShift128.py`

 * *Files identical despite different names*

### Comparing `pyvrp-0.1.0/pyvrp/tests/test_read.py` & `pyvrp-0.2.1/pyvrp/tests/test_read.py`

 * *Files 8% similar despite different names*

```diff
@@ -61,21 +61,27 @@
         [0, 1544, 1944, 1931, 1476],
         [1726, 0, 1992, 1427, 1593],
         [1965, 1975, 0, 621, 1090],
         [2063, 1433, 647, 0, 818],
         [1475, 1594, 1090, 828, 0],
     ]
 
+    # For instances read through VRPLIB/read(), distance is duration. So these
+    # matrices should be the same as the expected edge weights above.
     dist_mat = data.distance_matrix()
+    dur_mat = data.duration_matrix()
 
     for frm in range(data.num_clients + 1):  # incl. depot
         for to in range(data.num_clients + 1):  # incl. depot
             assert_equal(data.dist(frm, to), expected[frm][to])
             assert_equal(dist_mat[frm, to], expected[frm][to])
 
+            assert_equal(data.duration(frm, to), expected[frm][to])
+            assert_equal(dur_mat[frm, to], expected[frm][to])
+
     # From the DEMAND_SECTION in the file
     expected = [0, 5, 5, 3, 5]
 
     for client in range(data.num_clients + 1):  # incl. depot
         assert_equal(data.client(client).demand, expected[client])
 
     # From the TIME_WINDOW_SECTION in the file
@@ -95,15 +101,15 @@
     expected = [0, 360, 360, 420, 360]
 
     for client in range(data.num_clients + 1):  # incl. depot
         assert_equal(data.client(client).service_duration, expected[client])
 
 
 def test_reading_En22k4_instance():  # instance from CVRPLIB
-    data = read("data/E-n22-k4.vrp.txt", round_func="trunc1")
+    data = read("data/E-n22-k4.txt", round_func="trunc1")
 
     assert_equal(data.num_clients, 21)
     assert_equal(data.vehicle_capacity, 6_000)
 
     # Coordinates are scaled by 10 to align with 1 decimal distance precision
     assert_equal(data.depot().x, 1450)  # depot [x, y] location
     assert_equal(data.depot().y, 2150)
@@ -118,27 +124,19 @@
     #      dX = 151 - 145 = 6
     #      dY = 264 - 215 = 49
     #      dist = sqrt(dX^2 + dY^2) = 49.37
     #      int(10 * dist) = 493
     assert_equal(data.dist(0, 1), 493)
     assert_equal(data.dist(1, 0), 493)
 
-    # These fields are not present in the data file, and should thus retain
-    # their default values.
-    max_distance = max(
-        data.dist(i, j)
-        for i in range(data.num_clients + 1)
-        for j in range(data.num_clients + 1)
-    )
-    bound = (data.num_clients + 1) * max_distance
-
+    # This is a CVRP instance, so time window data should all be zeroed out.
     for client in range(data.num_clients + 1):  # incl. depot
         assert_equal(data.client(client).service_duration, 0)
         assert_equal(data.client(client).tw_early, 0)
-        assert_equal(data.client(client).tw_late, bound)
+        assert_equal(data.client(client).tw_late, 0)
 
 
 def test_reading_RC208_instance():  # Solomon style instance
     data = read(
         "data/RC208.txt", instance_format="solomon", round_func="trunc1"
     )
```

### Comparing `pyvrp-0.1.0/PKG-INFO` & `pyvrp-0.2.1/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: pyvrp
-Version: 0.1.0
+Version: 0.2.1
 Summary: A state-of-the-art vehicle routing problem solver.
-Home-page: https://github.com/N-Wouda/PyVRP
+Home-page: https://github.com/PyVRP/PyVRP
 License: MIT
 Author: Niels Wouda
 Author-email: nielswouda@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
@@ -24,22 +24,22 @@
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Dist: matplotlib (>=2.2.0)
 Requires-Dist: numpy (>=1.15.2)
 Requires-Dist: tomli (>=2.0.1,<3.0.0)
 Requires-Dist: tqdm (>=4.64.1,<5.0.0)
 Requires-Dist: vrplib (>=1.0.0,<2.0.0)
-Project-URL: Repository, https://github.com/N-Wouda/PyVRP
-Project-URL: Tracker, https://github.com/N-Wouda/PyVRP/issues
+Project-URL: Repository, https://github.com/PyVRP/PyVRP
+Project-URL: Tracker, https://github.com/PyVRP/PyVRP/issues
 Description-Content-Type: text/markdown
 
 [![PyPI version](https://badge.fury.io/py/pyvrp.svg)](https://badge.fury.io/py/pyvrp)
-[![CI](https://github.com/N-Wouda/pyvrp/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/N-Wouda/pyvrp/actions/workflows/CI.yml)
+[![CI](https://github.com/PyVRP/PyVRP/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/PyVRP/PyVRP/actions/workflows/CI.yml)
 [![Documentation Status](https://readthedocs.org/projects/pyvrp/badge/?version=latest)](https://pyvrp.readthedocs.io/en/latest/?badge=latest)
-[![codecov](https://codecov.io/gh/N-Wouda/pyvrp/branch/main/graph/badge.svg?token=G9JKIVZOHB)](https://codecov.io/gh/N-Wouda/pyvrp)
+[![codecov](https://codecov.io/gh/PyVRP/PyVRP/branch/main/graph/badge.svg?token=G9JKIVZOHB)](https://codecov.io/gh/PyVRP/PyVRP)
 
 # PyVRP
 
 The `pyvrp` package is an open-source, state-of-the-art vehicle routing problem solver.
 
 `pyvrp` may be installed in the usual way as
 ```
```

