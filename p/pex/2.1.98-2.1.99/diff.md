# Comparing `tmp/pex-2.1.98.tar.gz` & `tmp/pex-2.1.99.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pex-2.1.98.tar", last modified: Wed Jul 13 22:54:52 2022, max compression
+gzip compressed data, was "pex-2.1.99.tar", last modified: Thu Jul 14 16:31:32 2022, max compression
```

## Comparing `pex-2.1.98.tar` & `pex-2.1.99.tar`

### file list

```diff
@@ -1,915 +1,915 @@
--rw-r--r--   0        0        0     8997 2022-07-13 22:54:40.516411 pex-2.1.98/.github/workflows/ci.yml
--rw-r--r--   0        0        0     3330 2022-07-13 22:54:40.516411 pex-2.1.98/.github/workflows/release.yml
--rw-r--r--   0        0        0      148 2022-07-13 22:54:40.516411 pex-2.1.98/.gitignore
--rw-r--r--   0        0        0      262 2022-07-13 22:54:40.516411 pex-2.1.98/.readthedocs.yml
--rw-r--r--   0        0        0   109824 2022-07-13 22:54:40.520411 pex-2.1.98/CHANGES.rst
--rw-r--r--   0        0        0    11323 2022-07-13 22:54:40.520411 pex-2.1.98/LICENSE
--rw-r--r--   0        0        0      194 2022-07-13 22:54:40.520411 pex-2.1.98/MANIFEST.in
--rw-r--r--   0        0        0     5534 2022-07-13 22:54:40.520411 pex-2.1.98/README.rst
--rw-r--r--   0        0        0     2675 2022-07-13 22:54:40.520411 pex-2.1.98/RELEASE.rst
--rw-r--r--   0        0        0      896 2022-07-13 22:54:40.520411 pex-2.1.98/docker/base/Dockerfile
--rw-r--r--   0        0        0      483 2022-07-13 22:54:40.520411 pex-2.1.98/docker/user/Dockerfile
--rwxr-xr-x   0        0        0      371 2022-07-13 22:54:40.520411 pex-2.1.98/docker/user/create_docker_image_user.sh
--rw-r--r--   0        0        0     6750 2022-07-13 22:54:40.520411 pex-2.1.98/docs/Makefile
--rw-r--r--   0        0        0     1299 2022-07-13 22:54:40.520411 pex-2.1.98/docs/_ext/vars.py
--rw-r--r--   0        0        0       79 2022-07-13 22:54:40.520411 pex-2.1.98/docs/api/vars.rst
--rw-r--r--   0        0        0    18814 2022-07-13 22:54:40.520411 pex-2.1.98/docs/buildingpex.rst
--rw-r--r--   0        0        0     8585 2022-07-13 22:54:40.520411 pex-2.1.98/docs/conf.py
--rw-r--r--   0        0        0     1441 2022-07-13 22:54:40.520411 pex-2.1.98/docs/index.rst
--rw-r--r--   0        0        0     5516 2022-07-13 22:54:40.520411 pex-2.1.98/docs/recipes.rst
--rw-r--r--   0        0        0      196 2022-07-13 22:54:40.520411 pex-2.1.98/docs/rtd/requirements.txt
--rw-r--r--   0        0        0     1888 2022-07-13 22:54:40.520411 pex-2.1.98/docs/whatispex.rst
--rwxr-xr-x   0        0        0     1101 2022-07-13 22:54:40.520411 pex-2.1.98/dtox.sh
--rw-r--r--   0        0        0      990 2022-07-13 22:54:40.520411 pex-2.1.98/mypy.ini
--rw-r--r--   0        0        0      401 2022-07-13 22:54:40.520411 pex-2.1.98/pex/__init__.py
--rw-r--r--   0        0        0      235 2022-07-13 22:54:40.520411 pex-2.1.98/pex/__main__.py
--rw-r--r--   0        0        0      601 2022-07-13 22:54:40.520411 pex-2.1.98/pex/argparse.py
--rw-r--r--   0        0        0      483 2022-07-13 22:54:40.520411 pex-2.1.98/pex/attrs.py
--rw-r--r--   0        0        0     5898 2022-07-13 22:54:40.520411 pex-2.1.98/pex/auth.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/bin/__init__.py
--rwxr-xr-x   0        0        0    34811 2022-07-13 22:54:40.520411 pex-2.1.98/pex/bin/pex.py
--rw-r--r--   0        0        0     9760 2022-07-13 22:54:40.520411 pex-2.1.98/pex/bin/sh_boot.py
--rw-r--r--   0        0        0     3084 2022-07-13 22:54:40.520411 pex-2.1.98/pex/bootstrap.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/build_system/__init__.py
--rw-r--r--   0        0        0     4077 2022-07-13 22:54:40.520411 pex-2.1.98/pex/build_system/pep_517.py
--rw-r--r--   0        0        0     3907 2022-07-13 22:54:40.520411 pex-2.1.98/pex/build_system/pep_518.py
--rw-r--r--   0        0        0     1598 2022-07-13 22:54:40.520411 pex-2.1.98/pex/build_system/testing.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/__init__.py
--rw-r--r--   0        0        0      230 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/__main__.py
--rw-r--r--   0        0        0     2971 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/command.py
--rw-r--r--   0        0        0      465 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/commands/__init__.py
--rw-r--r--   0        0        0     6689 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/commands/interpreter.py
--rw-r--r--   0        0        0    28819 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/commands/lock.py
--rw-r--r--   0        0        0     1102 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/pex.py
--rw-r--r--   0        0        0      771 2022-07-13 22:54:40.520411 pex-2.1.98/pex/cli/testing.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/commands/__init__.py
--rw-r--r--   0        0        0    13469 2022-07-13 22:54:40.520411 pex-2.1.98/pex/commands/command.py
--rw-r--r--   0        0        0    27541 2022-07-13 22:54:40.520411 pex-2.1.98/pex/common.py
--rw-r--r--   0        0        0     6175 2022-07-13 22:54:40.520411 pex-2.1.98/pex/compatibility.py
--rw-r--r--   0        0        0     3592 2022-07-13 22:54:40.520411 pex-2.1.98/pex/compiler.py
--rw-r--r--   0        0        0    28300 2022-07-13 22:54:40.520411 pex-2.1.98/pex/dist_metadata.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/distutils/__init__.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.520411 pex-2.1.98/pex/distutils/commands/__init__.py
--rw-r--r--   0        0        0     5082 2022-07-13 22:54:40.520411 pex-2.1.98/pex/distutils/commands/bdist_pex.py
--rw-r--r--   0        0        0     3896 2022-07-13 22:54:40.520411 pex-2.1.98/pex/enum.py
--rw-r--r--   0        0        0    30226 2022-07-13 22:54:40.520411 pex-2.1.98/pex/environment.py
--rw-r--r--   0        0        0     4151 2022-07-13 22:54:40.520411 pex-2.1.98/pex/executor.py
--rw-r--r--   0        0        0     5192 2022-07-13 22:54:40.520411 pex-2.1.98/pex/fetcher.py
--rw-r--r--   0        0        0     3457 2022-07-13 22:54:40.520411 pex-2.1.98/pex/finders.py
--rw-r--r--   0        0        0      776 2022-07-13 22:54:40.520411 pex-2.1.98/pex/fingerprinted_distribution.py
--rw-r--r--   0        0        0     7375 2022-07-13 22:54:40.520411 pex-2.1.98/pex/hashing.py
--rw-r--r--   0        0        0     1007 2022-07-13 22:54:40.520411 pex-2.1.98/pex/inherit_path.py
--rw-r--r--   0        0        0    50414 2022-07-13 22:54:40.520411 pex-2.1.98/pex/interpreter.py
--rw-r--r--   0        0        0     8072 2022-07-13 22:54:40.520411 pex-2.1.98/pex/interpreter_constraints.py
--rw-r--r--   0        0        0    18654 2022-07-13 22:54:40.520411 pex-2.1.98/pex/jobs.py
--rw-r--r--   0        0        0     9606 2022-07-13 22:54:40.520411 pex-2.1.98/pex/layout.py
--rw-r--r--   0        0        0     1710 2022-07-13 22:54:40.520411 pex-2.1.98/pex/network_configuration.py
--rw-r--r--   0        0        0     3747 2022-07-13 22:54:40.520411 pex-2.1.98/pex/orderedset.py
--rw-r--r--   0        0        0    24137 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pep_376.py
--rw-r--r--   0        0        0     5719 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pep_425.py
--rw-r--r--   0        0        0     2329 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pep_440.py
--rw-r--r--   0        0        0     1120 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pep_503.py
--rw-r--r--   0        0        0     5515 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pep_508.py
--rw-r--r--   0        0        0    31790 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pex.py
--rw-r--r--   0        0        0    28193 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pex_bootstrapper.py
--rw-r--r--   0        0        0    32126 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pex_builder.py
--rw-r--r--   0        0        0    16993 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pex_info.py
--rw-r--r--   0        0        0     1137 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pex_warnings.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/__init__.py
--rw-r--r--   0        0        0     1147 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/download_observer.py
--rw-r--r--   0        0        0     5298 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/foreign_platform.py
--rw-r--r--   0        0        0     1463 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/foreign_platform_patches.py
--rw-r--r--   0        0        0     2123 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/local_project.py
--rw-r--r--   0        0        0     3632 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/log_analyzer.py
--rw-r--r--   0        0        0     4469 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/tailer.py
--rw-r--r--   0        0        0    31906 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/tool.py
--rw-r--r--   0        0        0     2810 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pip/vcs.py
--rw-r--r--   0        0        0    13464 2022-07-13 22:54:40.524411 pex-2.1.98/pex/platforms.py
--rw-r--r--   0        0        0     8432 2022-07-13 22:54:40.524411 pex-2.1.98/pex/pyenv.py
--rw-r--r--   0        0        0     3925 2022-07-13 22:54:40.524411 pex-2.1.98/pex/rank.py
--rw-r--r--   0        0        0    24615 2022-07-13 22:54:40.524411 pex-2.1.98/pex/requirements.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/__init__.py
--rw-r--r--   0        0        0     3376 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/configured_resolver.py
--rw-r--r--   0        0        0     6354 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/downloads.py
--rw-r--r--   0        0        0    17110 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lock_resolver.py
--rw-r--r--   0        0        0    29188 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/locked_resolve.py
--rw-r--r--   0        0        0    16114 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/locker.py
--rw-r--r--   0        0        0    10040 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/locker_patches.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/__init__.py
--rw-r--r--   0        0        0    14511 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/create.py
--rw-r--r--   0        0        0     7981 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/download_manager.py
--rw-r--r--   0        0        0    14188 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/json_codec.py
--rw-r--r--   0        0        0     5034 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/model.py
--rw-r--r--   0        0        0     5037 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/subset.py
--rw-r--r--   0        0        0    13964 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/lockfile/updater.py
--rw-r--r--   0        0        0     2097 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/path_mappings.py
--rw-r--r--   0        0        0     4420 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/pex_repository_resolver.py
--rw-r--r--   0        0        0     2532 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/requirement_configuration.py
--rw-r--r--   0        0        0     1652 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/requirement_options.py
--rw-r--r--   0        0        0     2737 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/resolved_requirement.py
--rw-r--r--   0        0        0     3037 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/resolver_configuration.py
--rw-r--r--   0        0        0    20711 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/resolver_options.py
--rw-r--r--   0        0        0     3038 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/resolvers.py
--rw-r--r--   0        0        0     7630 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/target_configuration.py
--rw-r--r--   0        0        0    11496 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/target_options.py
--rw-r--r--   0        0        0     2218 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolve/testing.py
--rw-r--r--   0        0        0    51072 2022-07-13 22:54:40.524411 pex-2.1.98/pex/resolver.py
--rw-r--r--   0        0        0     2945 2022-07-13 22:54:40.524411 pex-2.1.98/pex/result.py
--rw-r--r--   0        0        0     2091 2022-07-13 22:54:40.524411 pex-2.1.98/pex/sorted_tuple.py
--rw-r--r--   0        0        0    12123 2022-07-13 22:54:40.524411 pex-2.1.98/pex/targets.py
--rw-r--r--   0        0        0    22595 2022-07-13 22:54:40.528411 pex-2.1.98/pex/testing.py
--rw-r--r--   0        0        0    22685 2022-07-13 22:54:40.528411 pex-2.1.98/pex/third_party/__init__.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/__init__.py
--rw-r--r--   0        0        0      244 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/__main__.py
--rw-r--r--   0        0        0      440 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/command.py
--rw-r--r--   0        0        0      621 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/__init__.py
--rw-r--r--   0        0        0     3781 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/digraph.py
--rw-r--r--   0        0        0     5936 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/graph.py
--rw-r--r--   0        0        0      961 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/info.py
--rw-r--r--   0        0        0     4528 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/interpreter.py
--rw-r--r--   0        0        0    16196 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/repository.py
--rw-r--r--   0        0        0     7525 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/commands/venv.py
--rw-r--r--   0        0        0     3435 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tools/main.py
--rw-r--r--   0        0        0     4614 2022-07-13 22:54:40.528411 pex-2.1.98/pex/tracer.py
--rw-r--r--   0        0        0     2538 2022-07-13 22:54:40.528411 pex-2.1.98/pex/typing.py
--rw-r--r--   0        0        0     9347 2022-07-13 22:54:40.528411 pex-2.1.98/pex/util.py
--rw-r--r--   0        0        0    29372 2022-07-13 22:54:40.528411 pex-2.1.98/pex/variables.py
--rw-r--r--   0        0        0     2364 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/README.md
--rw-r--r--   0        0        0    12539 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/__init__.py
--rw-r--r--   0        0        0    16893 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/__main__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/__init__.py
--rw-r--r--   0        0        0       80 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/.layout.json
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/__init__.py
--rw-r--r--   0        0        0     1672 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/__init__.py
--rw-r--r--   0        0        0    15100 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/__init__.pyi
--rw-r--r--   0        0        0     4165 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_cmp.py
--rw-r--r--   0        0        0      317 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_cmp.pyi
--rw-r--r--   0        0        0     8396 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_compat.py
--rw-r--r--   0        0        0      892 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_config.py
--rw-r--r--   0        0        0    14753 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_funcs.py
--rw-r--r--   0        0        0   102691 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_make.py
--rw-r--r--   0        0        0     5728 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_next_gen.py
--rw-r--r--   0        0        0     2194 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_version_info.py
--rw-r--r--   0        0        0      209 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/_version_info.pyi
--rw-r--r--   0        0        0     4078 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/converters.py
--rw-r--r--   0        0        0      416 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/converters.pyi
--rw-r--r--   0        0        0     1981 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/exceptions.py
--rw-r--r--   0        0        0      539 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/exceptions.pyi
--rw-r--r--   0        0        0     1124 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/filters.py
--rw-r--r--   0        0        0      215 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/filters.pyi
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/py.typed
--rw-r--r--   0        0        0     1466 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/setters.py
--rw-r--r--   0        0        0      573 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/setters.pyi
--rw-r--r--   0        0        0    15966 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/validators.py
--rw-r--r--   0        0        0     2268 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attr/validators.pyi
--rw-r--r--   0        0        0      752 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/AUTHORS.rst
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/INSTALLER
--rw-r--r--   0        0        0     1082 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/LICENSE
--rw-r--r--   0        0        0     9838 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/WHEEL
--rw-r--r--   0        0        0      199 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/direct_url.json
--rw-r--r--   0        0        0       11 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/top_level.txt
--rw-r--r--   0        0        0     1745 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/__init__.py
--rw-r--r--   0        0        0     1982 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/__init__.pyi
--rw-r--r--   0        0        0      197 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/converters.py
--rw-r--r--   0        0        0      197 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/exceptions.py
--rw-r--r--   0        0        0      191 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/filters.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/py.typed
--rw-r--r--   0        0        0      191 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/setters.py
--rw-r--r--   0        0        0      197 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/attrs/attrs/validators.py
--rw-r--r--   0        0        0       77 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/.layout.json
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/__init__.py
--rw-r--r--   0        0        0       33 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/constraints.txt
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/INSTALLER
--rw-r--r--   0        0        0      197 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE
--rw-r--r--   0        0        0    10174 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.APACHE
--rw-r--r--   0        0        0     1344 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.BSD
--rw-r--r--   0        0        0    13299 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/WHEEL
--rw-r--r--   0        0        0       10 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/top_level.txt
--rw-r--r--   0        0        0      726 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/__about__.py
--rw-r--r--   0        0        0      562 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/__init__.py
--rw-r--r--   0        0        0     1128 2022-07-13 22:54:40.528411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_compat.py
--rw-r--r--   0        0        0     2022 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_structures.py
--rw-r--r--   0        0        0     1812 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_typing.py
--rw-r--r--   0        0        0     9741 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/markers.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/py.typed
--rw-r--r--   0        0        0     5388 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/requirements.py
--rw-r--r--   0        0        0    32208 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/specifiers.py
--rw-r--r--   0        0        0    29561 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/tags.py
--rw-r--r--   0        0        0     4385 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/utils.py
--rw-r--r--   0        0        0    15974 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/packaging/version.py
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/INSTALLER
--rw-r--r--   0        0        0     1023 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/LICENSE
--rw-r--r--   0        0        0     3636 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/METADATA
--rw-r--r--   0        0        0      564 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/RECORD
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/WHEEL
--rw-r--r--   0        0        0       10 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/top_level.txt
--rw-r--r--   0        0        0   273365 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing.py
--rw-r--r--   0        0        0       73 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/.layout.json
--rwxr-xr-x   0        0        0      211 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/.prefix/bin/pip
--rwxr-xr-x   0        0        0      211 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/.prefix/bin/pip3
--rwxr-xr-x   0        0        0      211 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/.prefix/bin/pip3.8
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/INSTALLER
--rw-r--r--   0        0        0     1090 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/LICENSE.txt
--rw-r--r--   0        0        0     4310 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/WHEEL
--rw-r--r--   0        0        0      195 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/direct_url.json
--rw-r--r--   0        0        0      124 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/entry_points.txt
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/top_level.txt
--rw-r--r--   0        0        0      455 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/__init__.py
--rw-r--r--   0        0        0      911 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/__main__.py
--rw-r--r--   0        0        0      495 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/__init__.py
--rw-r--r--   0        0        0     8089 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/build_env.py
--rw-r--r--   0        0        0    12249 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cache.py
--rw-r--r--   0        0        0      132 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/__init__.py
--rw-r--r--   0        0        0     6547 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/autocompletion.py
--rw-r--r--   0        0        0     9337 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/base_command.py
--rw-r--r--   0        0        0    28618 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/cmdoptions.py
--rw-r--r--   0        0        0      975 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/command_context.py
--rw-r--r--   0        0        0     2616 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/main.py
--rw-r--r--   0        0        0     2830 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/main_parser.py
--rw-r--r--   0        0        0    10388 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/parser.py
--rw-r--r--   0        0        0     9121 2022-07-13 22:54:40.532411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/progress_bars.py
--rw-r--r--   0        0        0    16455 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/req_command.py
--rw-r--r--   0        0        0     5509 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/spinners.py
--rw-r--r--   0        0        0      156 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/status_codes.py
--rw-r--r--   0        0        0     4101 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/__init__.py
--rw-r--r--   0        0        0     7555 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/cache.py
--rw-r--r--   0        0        0     1677 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/check.py
--rw-r--r--   0        0        0     3081 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/completion.py
--rw-r--r--   0        0        0     9327 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/configuration.py
--rw-r--r--   0        0        0     7315 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/debug.py
--rw-r--r--   0        0        0     4932 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/download.py
--rw-r--r--   0        0        0     3871 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/freeze.py
--rw-r--r--   0        0        0     1843 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/hash.py
--rw-r--r--   0        0        0     1294 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/help.py
--rw-r--r--   0        0        0    27410 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/install.py
--rw-r--r--   0        0        0    11519 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/list.py
--rw-r--r--   0        0        0     6033 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/search.py
--rw-r--r--   0        0        0     6996 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/show.py
--rw-r--r--   0        0        0     3311 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/uninstall.py
--rw-r--r--   0        0        0     6802 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/wheel.py
--rw-r--r--   0        0        0    13904 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/configuration.py
--rw-r--r--   0        0        0      959 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/__init__.py
--rw-r--r--   0        0        0     1426 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/base.py
--rw-r--r--   0        0        0      761 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/installed.py
--rw-r--r--   0        0        0     4087 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/sdist.py
--rw-r--r--   0        0        0     1295 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/wheel.py
--rw-r--r--   0        0        0    13003 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/exceptions.py
--rw-r--r--   0        0        0       30 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/index/__init__.py
--rw-r--r--   0        0        0    22070 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/index/collector.py
--rw-r--r--   0        0        0    37454 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/index/package_finder.py
--rw-r--r--   0        0        0     6731 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/locations.py
--rw-r--r--   0        0        0      437 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/main.py
--rw-r--r--   0        0        0       63 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/__init__.py
--rw-r--r--   0        0        0     1196 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/candidate.py
--rw-r--r--   0        0        0     6884 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/direct_url.py
--rw-r--r--   0        0        0     2823 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/format_control.py
--rw-r--r--   0        0        0     1161 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/index.py
--rw-r--r--   0        0        0     7471 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/link.py
--rw-r--r--   0        0        0      778 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/scheme.py
--rw-r--r--   0        0        0     4751 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/search_scope.py
--rw-r--r--   0        0        0     2045 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/selection_prefs.py
--rw-r--r--   0        0        0     4070 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/target_python.py
--rw-r--r--   0        0        0     2772 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/wheel.py
--rw-r--r--   0        0        0       50 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/__init__.py
--rw-r--r--   0        0        0    11652 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/auth.py
--rw-r--r--   0        0        0     2329 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/cache.py
--rw-r--r--   0        0        0     6401 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/download.py
--rw-r--r--   0        0        0     8121 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/lazy_wheel.py
--rw-r--r--   0        0        0    15449 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/session.py
--rw-r--r--   0        0        0     4172 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/utils.py
--rw-r--r--   0        0        0     1883 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/xmlrpc.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/__init__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/__init__.py
--rw-r--r--   0        0        0     1255 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata.py
--rw-r--r--   0        0        0     2011 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata_legacy.py
--rw-r--r--   0        0        0     1466 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel.py
--rw-r--r--   0        0        0     3347 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel_legacy.py
--rw-r--r--   0        0        0     5216 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/check.py
--rw-r--r--   0        0        0    10411 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/freeze.py
--rw-r--r--   0        0        0       51 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/__init__.py
--rw-r--r--   0        0        0     1488 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/editable_legacy.py
--rw-r--r--   0        0        0     4281 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/legacy.py
--rw-r--r--   0        0        0    31247 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/wheel.py
--rw-r--r--   0        0        0    22460 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/prepare.py
--rw-r--r--   0        0        0     7400 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/pyproject.py
--rw-r--r--   0        0        0     3133 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/__init__.py
--rw-r--r--   0        0        0    16135 2022-07-13 22:54:40.536411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/constructors.py
--rw-r--r--   0        0        0    18594 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_file.py
--rw-r--r--   0        0        0    33420 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_install.py
--rw-r--r--   0        0        0     7887 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_set.py
--rw-r--r--   0        0        0     4691 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_tracker.py
--rw-r--r--   0        0        0    23771 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_uninstall.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/__init__.py
--rw-r--r--   0        0        0      683 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/base.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/__init__.py
--rw-r--r--   0        0        0    18234 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/resolver.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/__init__.py
--rw-r--r--   0        0        0     5061 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/base.py
--rw-r--r--   0        0        0    20035 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/candidates.py
--rw-r--r--   0        0        0    18946 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/factory.py
--rw-r--r--   0        0        0     3773 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/found_candidates.py
--rw-r--r--   0        0        0     7339 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/provider.py
--rw-r--r--   0        0        0     2857 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/reporter.py
--rw-r--r--   0        0        0     5969 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/requirements.py
--rw-r--r--   0        0        0    11634 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/resolver.py
--rw-r--r--   0        0        0     6745 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/self_outdated_check.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/__init__.py
--rw-r--r--   0        0        0     1349 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/appdirs.py
--rw-r--r--   0        0        0     9489 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/compat.py
--rw-r--r--   0        0        0     5690 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/compatibility_tags.py
--rw-r--r--   0        0        0      295 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/datetime.py
--rw-r--r--   0        0        0     3318 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/deprecation.py
--rw-r--r--   0        0        0     4146 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/direct_url_helpers.py
--rw-r--r--   0        0        0     1350 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/distutils_args.py
--rw-r--r--   0        0        0     1284 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/encoding.py
--rw-r--r--   0        0        0     1152 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/entrypoints.py
--rw-r--r--   0        0        0     6943 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/filesystem.py
--rw-r--r--   0        0        0      847 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/filetypes.py
--rw-r--r--   0        0        0     3297 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/glibc.py
--rw-r--r--   0        0        0     5297 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/hashes.py
--rw-r--r--   0        0        0      810 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/inject_securetransport.py
--rw-r--r--   0        0        0    13093 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/logging.py
--rw-r--r--   0        0        0    28047 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/misc.py
--rw-r--r--   0        0        0     1201 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/models.py
--rw-r--r--   0        0        0     3036 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/packaging.py
--rw-r--r--   0        0        0     3404 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/parallel.py
--rw-r--r--   0        0        0     1254 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/pkg_resources.py
--rw-r--r--   0        0        0     5058 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/setuptools_build.py
--rw-r--r--   0        0        0    10866 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/subprocess.py
--rw-r--r--   0        0        0     8845 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/temp_dir.py
--rw-r--r--   0        0        0     1401 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/typing.py
--rw-r--r--   0        0        0     9488 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/unpacking.py
--rw-r--r--   0        0        0     1527 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/urls.py
--rw-r--r--   0        0        0     3706 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/virtualenv.py
--rw-r--r--   0        0        0     7303 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/wheel.py
--rw-r--r--   0        0        0      617 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/__init__.py
--rw-r--r--   0        0        0     4016 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/bazaar.py
--rw-r--r--   0        0        0    15599 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/git.py
--rw-r--r--   0        0        0     5564 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/mercurial.py
--rw-r--r--   0        0        0    12558 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/subversion.py
--rw-r--r--   0        0        0    23767 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/versioncontrol.py
--rw-r--r--   0        0        0    11816 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/wheel_builder.py
--rw-r--r--   0        0        0     4788 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/__init__.py
--rw-r--r--   0        0        0    25907 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/appdirs.py
--rw-r--r--   0        0        0      302 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/__init__.py
--rw-r--r--   0        0        0     1295 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/_cmd.py
--rw-r--r--   0        0        0     4882 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/adapter.py
--rw-r--r--   0        0        0      805 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/cache.py
--rw-r--r--   0        0        0       86 2022-07-13 22:54:40.540411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/__init__.py
--rw-r--r--   0        0        0     4153 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/file_cache.py
--rw-r--r--   0        0        0      856 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/redis_cache.py
--rw-r--r--   0        0        0      695 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/compat.py
--rw-r--r--   0        0        0    14149 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/controller.py
--rw-r--r--   0        0        0     2533 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/filewrapper.py
--rw-r--r--   0        0        0     4070 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/heuristics.py
--rw-r--r--   0        0        0     7091 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/serialize.py
--rw-r--r--   0        0        0      690 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/wrapper.py
--rw-r--r--   0        0        0       62 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/__init__.py
--rw-r--r--   0        0        0      255 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/__main__.py
--rw-r--r--   0        0        0   281608 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/cacert.pem
--rw-r--r--   0        0        0     2315 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/core.py
--rw-r--r--   0        0        0     1559 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/__init__.py
--rw-r--r--   0        0        0    31254 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5freq.py
--rw-r--r--   0        0        0     1757 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5prober.py
--rw-r--r--   0        0        0     9411 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/chardistribution.py
--rw-r--r--   0        0        0     3787 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetgroupprober.py
--rw-r--r--   0        0        0     5110 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetprober.py
--rw-r--r--   0        0        0        1 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/__init__.py
--rw-r--r--   0        0        0     2774 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/chardetect.py
--rw-r--r--   0        0        0     3590 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/codingstatemachine.py
--rw-r--r--   0        0        0     1134 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/compat.py
--rw-r--r--   0        0        0     1855 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/cp949prober.py
--rw-r--r--   0        0        0     1661 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/enums.py
--rw-r--r--   0        0        0     3950 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/escprober.py
--rw-r--r--   0        0        0    10510 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/escsm.py
--rw-r--r--   0        0        0     3749 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/eucjpprober.py
--rw-r--r--   0        0        0    13546 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrfreq.py
--rw-r--r--   0        0        0     1748 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrprober.py
--rw-r--r--   0        0        0    31621 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwfreq.py
--rw-r--r--   0        0        0     1747 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwprober.py
--rw-r--r--   0        0        0    20715 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312freq.py
--rw-r--r--   0        0        0     1754 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312prober.py
--rw-r--r--   0        0        0    13838 2022-07-13 22:54:40.544411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/hebrewprober.py
--rw-r--r--   0        0        0    25777 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/jisfreq.py
--rw-r--r--   0        0        0    19643 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/jpcntx.py
--rw-r--r--   0        0        0    12839 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langbulgarianmodel.py
--rw-r--r--   0        0        0    17948 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langcyrillicmodel.py
--rw-r--r--   0        0        0    12688 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langgreekmodel.py
--rw-r--r--   0        0        0    11345 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhebrewmodel.py
--rw-r--r--   0        0        0    12592 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhungarianmodel.py
--rw-r--r--   0        0        0    11290 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langthaimodel.py
--rw-r--r--   0        0        0    11102 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langturkishmodel.py
--rw-r--r--   0        0        0     5370 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/latin1prober.py
--rw-r--r--   0        0        0     3413 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcharsetprober.py
--rw-r--r--   0        0        0     2012 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcsgroupprober.py
--rw-r--r--   0        0        0    25481 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcssm.py
--rw-r--r--   0        0        0     5657 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcharsetprober.py
--rw-r--r--   0        0        0     3546 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcsgroupprober.py
--rw-r--r--   0        0        0     3774 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sjisprober.py
--rw-r--r--   0        0        0    12485 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/universaldetector.py
--rw-r--r--   0        0        0     2766 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/utf8prober.py
--rw-r--r--   0        0        0      242 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/version.py
--rw-r--r--   0        0        0      239 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/__init__.py
--rw-r--r--   0        0        0     2522 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansi.py
--rw-r--r--   0        0        0    10517 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansitowin32.py
--rw-r--r--   0        0        0     1915 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/initialise.py
--rw-r--r--   0        0        0     5404 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/win32.py
--rw-r--r--   0        0        0     6438 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/winterm.py
--rw-r--r--   0        0        0    16915 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/contextlib2.py
--rw-r--r--   0        0        0      581 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/__init__.py
--rw-r--r--   0        0        0      274 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/__init__.py
--rw-r--r--   0        0        0      971 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/misc.py
--rw-r--r--   0        0        0    25707 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/shutil.py
--rw-r--r--   0        0        0     2617 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.cfg
--rw-r--r--   0        0        0    26854 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.py
--rw-r--r--   0        0        0    92628 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/tarfile.py
--rw-r--r--   0        0        0    41408 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/compat.py
--rw-r--r--   0        0        0    51059 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/database.py
--rw-r--r--   0        0        0    21066 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/index.py
--rw-r--r--   0        0        0    52100 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/locators.py
--rw-r--r--   0        0        0    14811 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/manifest.py
--rw-r--r--   0        0        0     4387 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/markers.py
--rw-r--r--   0        0        0    38962 2022-07-13 22:54:40.548411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/metadata.py
--rw-r--r--   0        0        0    10766 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/resources.py
--rw-r--r--   0        0        0    17180 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py
--rw-r--r--   0        0        0    96768 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/t32.exe
--rw-r--r--   0        0        0   105984 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/t64.exe
--rw-r--r--   0        0        0    59845 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/util.py
--rw-r--r--   0        0        0    23391 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/version.py
--rw-r--r--   0        0        0    90112 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/w32.exe
--rw-r--r--   0        0        0    99840 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/w64.exe
--rw-r--r--   0        0        0    41144 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/wheel.py
--rw-r--r--   0        0        0    43628 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distro.py
--rw-r--r--   0        0        0     1160 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/__init__.py
--rw-r--r--   0        0        0    16728 2022-07-13 22:54:40.552411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_ihatexml.py
--rw-r--r--   0        0        0    32353 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_inputstream.py
--rw-r--r--   0        0        0    77040 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_tokenizer.py
--rw-r--r--   0        0        0      109 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/__init__.py
--rw-r--r--   0        0        0     1013 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/_base.py
--rw-r--r--   0        0        0     1775 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/py.py
--rw-r--r--   0        0        0     4931 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_utils.py
--rw-r--r--   0        0        0    83464 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/constants.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/__init__.py
--rw-r--r--   0        0        0      919 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/alphabeticalattributes.py
--rw-r--r--   0        0        0      286 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/base.py
--rw-r--r--   0        0        0     2945 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/inject_meta_charset.py
--rw-r--r--   0        0        0     3643 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/lint.py
--rw-r--r--   0        0        0    10588 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/optionaltags.py
--rw-r--r--   0        0        0    26897 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/sanitizer.py
--rw-r--r--   0        0        0     1214 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/whitespace.py
--rw-r--r--   0        0        0   117186 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/html5parser.py
--rw-r--r--   0        0        0    15759 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/serializer.py
--rw-r--r--   0        0        0      679 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/__init__.py
--rw-r--r--   0        0        0     1715 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/genshi.py
--rw-r--r--   0        0        0     1776 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/sax.py
--rw-r--r--   0        0        0     3592 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/__init__.py
--rw-r--r--   0        0        0    14565 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/base.py
--rw-r--r--   0        0        0     8925 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/dom.py
--rw-r--r--   0        0        0    12836 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree.py
--rw-r--r--   0        0        0    14766 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree_lxml.py
--rw-r--r--   0        0        0     5719 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/__init__.py
--rw-r--r--   0        0        0     7476 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/base.py
--rw-r--r--   0        0        0     1413 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/dom.py
--rw-r--r--   0        0        0     4551 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree.py
--rw-r--r--   0        0        0     6357 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree_lxml.py
--rw-r--r--   0        0        0     2309 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/genshi.py
--rw-r--r--   0        0        0       58 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/__init__.py
--rw-r--r--   0        0        0     3299 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/codec.py
--rw-r--r--   0        0        0      232 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/compat.py
--rw-r--r--   0        0        0    11951 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/core.py
--rw-r--r--   0        0        0    42350 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/idnadata.py
--rw-r--r--   0        0        0     1749 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/intranges.py
--rw-r--r--   0        0        0       22 2022-07-13 22:54:40.556411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/package_data.py
--rw-r--r--   0        0        0   202084 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/uts46data.py
--rw-r--r--   0        0        0    79875 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/ipaddress.py
--rw-r--r--   0        0        0     1118 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/__init__.py
--rw-r--r--   0        0        0       20 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/_version.py
--rw-r--r--   0        0        0     1081 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/exceptions.py
--rw-r--r--   0        0        0     6034 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/ext.py
--rw-r--r--   0        0        0    37133 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/fallback.py
--rw-r--r--   0        0        0      726 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/__about__.py
--rw-r--r--   0        0        0      562 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/__init__.py
--rw-r--r--   0        0        0     1128 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_compat.py
--rw-r--r--   0        0        0     2022 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_structures.py
--rw-r--r--   0        0        0     1824 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_typing.py
--rw-r--r--   0        0        0     9472 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/markers.py
--rw-r--r--   0        0        0     5110 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/requirements.py
--rw-r--r--   0        0        0    32208 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/specifiers.py
--rw-r--r--   0        0        0    29561 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/tags.py
--rw-r--r--   0        0        0     4385 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/utils.py
--rw-r--r--   0        0        0    15974 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/version.py
--rw-r--r--   0        0        0      129 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/__init__.py
--rw-r--r--   0        0        0     8438 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/_in_process.py
--rw-r--r--   0        0        0     3335 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/build.py
--rw-r--r--   0        0        0     5961 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/check.py
--rw-r--r--   0        0        0     4098 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/colorlog.py
--rw-r--r--   0        0        0      780 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/compat.py
--rw-r--r--   0        0        0     1129 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/dirtools.py
--rw-r--r--   0        0        0     6041 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/envbuild.py
--rw-r--r--   0        0        0     2463 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/meta.py
--rw-r--r--   0        0        0    11290 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/wrappers.py
--rw-r--r--   0        0        0   108277 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/__init__.py
--rw-r--r--   0        0        0      562 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/py31compat.py
--rw-r--r--   0        0        0     4857 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/__init__.py
--rw-r--r--   0        0        0     2854 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/bar.py
--rw-r--r--   0        0        0     1372 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/counter.py
--rw-r--r--   0        0        0     1380 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/spinner.py
--rw-r--r--   0        0        0   273394 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pyparsing.py
--rw-r--r--   0        0        0     4465 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/__init__.py
--rw-r--r--   0        0        0      441 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/__version__.py
--rw-r--r--   0        0        0     1096 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/_internal_utils.py
--rw-r--r--   0        0        0    21548 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/adapters.py
--rw-r--r--   0        0        0     6496 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/api.py
--rw-r--r--   0        0        0    10207 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/auth.py
--rw-r--r--   0        0        0      465 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/certs.py
--rw-r--r--   0        0        0     2045 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/compat.py
--rw-r--r--   0        0        0    18430 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/cookies.py
--rw-r--r--   0        0        0     3173 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/exceptions.py
--rw-r--r--   0        0        0     3578 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/help.py
--rw-r--r--   0        0        0      757 2022-07-13 22:54:40.560411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/hooks.py
--rw-r--r--   0        0        0    34373 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/models.py
--rw-r--r--   0        0        0      695 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/packages.py
--rw-r--r--   0        0        0    30135 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/sessions.py
--rw-r--r--   0        0        0     4188 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/status_codes.py
--rw-r--r--   0        0        0     3005 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/structures.py
--rw-r--r--   0        0        0    30355 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/utils.py
--rw-r--r--   0        0        0      537 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/__init__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/compat/__init__.py
--rw-r--r--   0        0        0      127 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/compat/collections_abc.py
--rw-r--r--   0        0        0     5091 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/providers.py
--rw-r--r--   0        0        0     1364 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/reporters.py
--rw-r--r--   0        0        0    16538 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/resolvers.py
--rw-r--r--   0        0        0     4408 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/structs.py
--rw-r--r--   0        0        0     9972 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/retrying.py
--rw-r--r--   0        0        0    34159 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/six.py
--rw-r--r--   0        0        0      747 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/__init__.py
--rw-r--r--   0        0        0    38954 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/decoder.py
--rw-r--r--   0        0        0     9964 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/encoder.py
--rw-r--r--   0        0        0      378 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/ordered.py
--rw-r--r--   0        0        0      701 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/tz.py
--rw-r--r--   0        0        0     2763 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/__init__.py
--rw-r--r--   0        0        0    10811 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_collections.py
--rw-r--r--   0        0        0       63 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_version.py
--rw-r--r--   0        0        0    18489 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connection.py
--rw-r--r--   0        0        0    37133 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connectionpool.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/__init__.py
--rw-r--r--   0        0        0      957 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_appengine_environ.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/__init__.py
--rw-r--r--   0        0        0    17649 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/bindings.py
--rw-r--r--   0        0        0    13908 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/low_level.py
--rw-r--r--   0        0        0    11034 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/appengine.py
--rw-r--r--   0        0        0     4160 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/ntlmpool.py
--rw-r--r--   0        0        0    16795 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/pyopenssl.py
--rw-r--r--   0        0        0    34303 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/securetransport.py
--rw-r--r--   0        0        0     7097 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/socks.py
--rw-r--r--   0        0        0     7810 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/exceptions.py
--rw-r--r--   0        0        0     8579 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/fields.py
--rw-r--r--   0        0        0     2440 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/filepost.py
--rw-r--r--   0        0        0      108 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/__init__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/__init__.py
--rw-r--r--   0        0        0     1417 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/makefile.py
--rw-r--r--   0        0        0    32536 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/six.py
--rw-r--r--   0        0        0      757 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/__init__.py
--rw-r--r--   0        0        0     5696 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/_implementation.py
--rw-r--r--   0        0        0    19763 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/poolmanager.py
--rw-r--r--   0        0        0     5985 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/request.py
--rw-r--r--   0        0        0    28203 2022-07-13 22:54:40.564411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/response.py
--rw-r--r--   0        0        0     1155 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/__init__.py
--rw-r--r--   0        0        0     4922 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/connection.py
--rw-r--r--   0        0        0     1604 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/proxy.py
--rw-r--r--   0        0        0      498 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/queue.py
--rw-r--r--   0        0        0     4123 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/request.py
--rw-r--r--   0        0        0     3510 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/response.py
--rw-r--r--   0        0        0    21366 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/retry.py
--rw-r--r--   0        0        0    16281 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssl_.py
--rw-r--r--   0        0        0     6932 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssltransport.py
--rw-r--r--   0        0        0    10003 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/timeout.py
--rw-r--r--   0        0        0    13981 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/url.py
--rw-r--r--   0        0        0     5404 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/wait.py
--rw-r--r--   0        0        0      437 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/vendor.txt
--rw-r--r--   0        0        0    10579 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/__init__.py
--rw-r--r--   0        0        0     8979 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/labels.py
--rw-r--r--   0        0        0     1305 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/mklabels.py
--rw-r--r--   0        0        0     6563 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/tests.py
--rw-r--r--   0        0        0     4307 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/x_user_defined.py
--rw-r--r--   0        0        0      121 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/.layout.json
--rwxr-xr-x   0        0        0      220 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/.prefix/bin/easy_install
--rwxr-xr-x   0        0        0      220 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/.prefix/bin/easy_install-3.8
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/__init__.py
--rw-r--r--   0        0        0      282 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/easy_install.py
--rw-r--r--   0        0        0   109513 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/__init__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/__init__.py
--rw-r--r--   0        0        0    24701 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/appdirs.py
--rw-r--r--   0        0        0      720 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__about__.py
--rw-r--r--   0        0        0      513 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__init__.py
--rw-r--r--   0        0        0      860 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_compat.py
--rw-r--r--   0        0        0     1416 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_structures.py
--rw-r--r--   0        0        0     8769 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/markers.py
--rw-r--r--   0        0        0     5044 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/requirements.py
--rw-r--r--   0        0        0    28025 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/specifiers.py
--rw-r--r--   0        0        0      421 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/utils.py
--rw-r--r--   0        0        0    11556 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/version.py
--rw-r--r--   0        0        0   232055 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/pyparsing.py
--rw-r--r--   0        0        0    30098 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/six.py
--rw-r--r--   0        0        0     2498 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/extern/__init__.py
--rw-r--r--   0        0        0      558 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/py31compat.py
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/INSTALLER
--rw-r--r--   0        0        0     1078 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/LICENSE
--rw-r--r--   0        0        0     3745 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/WHEEL
--rw-r--r--   0        0        0      239 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/dependency_links.txt
--rw-r--r--   0        0        0     3206 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/entry_points.txt
--rw-r--r--   0        0        0       38 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/top_level.txt
--rw-r--r--   0        0        0        1 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/zip-safe
--rw-r--r--   0        0        0     8157 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/__init__.py
--rw-r--r--   0        0        0      218 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_deprecation_warning.py
--rw-r--r--   0        0        0     2223 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_imp.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/__init__.py
--rw-r--r--   0        0        0    15130 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/ordered_set.py
--rw-r--r--   0        0        0      744 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__about__.py
--rw-r--r--   0        0        0      562 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__init__.py
--rw-r--r--   0        0        0      865 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_compat.py
--rw-r--r--   0        0        0     1416 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_structures.py
--rw-r--r--   0        0        0     8780 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/markers.py
--rw-r--r--   0        0        0     5419 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/requirements.py
--rw-r--r--   0        0        0    27778 2022-07-13 22:54:40.568411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/specifiers.py
--rw-r--r--   0        0        0    12933 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/tags.py
--rw-r--r--   0        0        0     1520 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/utils.py
--rw-r--r--   0        0        0    11978 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/version.py
--rw-r--r--   0        0        0   232055 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/pyparsing.py
--rw-r--r--   0        0        0    30098 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/six.py
--rw-r--r--   0        0        0     6730 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/archive_util.py
--rw-r--r--   0        0        0    10153 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/build_meta.py
--rw-r--r--   0        0        0    65536 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli-32.exe
--rw-r--r--   0        0        0    74752 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli-64.exe
--rw-r--r--   0        0        0    65536 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli.exe
--rw-r--r--   0        0        0      710 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/__init__.py
--rw-r--r--   0        0        0     2736 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/alias.py
--rw-r--r--   0        0        0    18880 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_egg.py
--rw-r--r--   0        0        0     1508 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_rpm.py
--rw-r--r--   0        0        0      637 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_wininst.py
--rw-r--r--   0        0        0     4632 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_clib.py
--rw-r--r--   0        0        0    13284 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_ext.py
--rw-r--r--   0        0        0    10036 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_py.py
--rw-r--r--   0        0        0     8854 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/develop.py
--rw-r--r--   0        0        0      960 2022-07-13 22:54:40.572411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/dist_info.py
--rw-r--r--   0        0        0    90093 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/easy_install.py
--rw-r--r--   0        0        0    27330 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/egg_info.py
--rw-r--r--   0        0        0     4832 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install.py
--rw-r--r--   0        0        0     2737 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_egg_info.py
--rw-r--r--   0        0        0     4034 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_lib.py
--rw-r--r--   0        0        0     3105 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_scripts.py
--rw-r--r--   0        0        0      628 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/launcher manifest.xml
--rw-r--r--   0        0        0     5128 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/py36compat.py
--rw-r--r--   0        0        0      613 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/register.py
--rw-r--r--   0        0        0     2419 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/rotate.py
--rw-r--r--   0        0        0      816 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/saveopts.py
--rw-r--r--   0        0        0     8363 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/sdist.py
--rw-r--r--   0        0        0     5359 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/setopt.py
--rw-r--r--   0        0        0    10328 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/test.py
--rw-r--r--   0        0        0      607 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/upload.py
--rw-r--r--   0        0        0     7734 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/upload_docs.py
--rw-r--r--   0        0        0    21571 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/config.py
--rw-r--r--   0        0        0      935 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/dep_util.py
--rw-r--r--   0        0        0     5517 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/depends.py
--rw-r--r--   0        0        0    51749 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/dist.py
--rw-r--r--   0        0        0      524 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/errors.py
--rw-r--r--   0        0        0     1868 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/extension.py
--rw-r--r--   0        0        0     2514 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/extern/__init__.py
--rw-r--r--   0        0        0     5084 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/glob.py
--rw-r--r--   0        0        0    65536 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui-32.exe
--rw-r--r--   0        0        0    75264 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui-64.exe
--rw-r--r--   0        0        0    65536 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui.exe
--rw-r--r--   0        0        0     5881 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/installer.py
--rw-r--r--   0        0        0      787 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/launch.py
--rw-r--r--   0        0        0     2140 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/lib2to3_ex.py
--rw-r--r--   0        0        0     5520 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/monkey.py
--rw-r--r--   0        0        0    47209 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/msvc.py
--rw-r--r--   0        0        0     3338 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/namespaces.py
--rw-r--r--   0        0        0    42090 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/package_index.py
--rw-r--r--   0        0        0     1625 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py27compat.py
--rw-r--r--   0        0        0      838 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py31compat.py
--rw-r--r--   0        0        0     1606 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py33compat.py
--rw-r--r--   0        0        0      245 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py34compat.py
--rw-r--r--   0        0        0    15424 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/sandbox.py
--rw-r--r--   0        0        0      218 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/script (dev).tmpl
--rw-r--r--   0        0        0      138 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/script.tmpl
--rw-r--r--   0        0        0     2302 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/site-patch.py
--rw-r--r--   0        0        0     8815 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/ssl_support.py
--rw-r--r--   0        0        0     1125 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/unicode_utils.py
--rw-r--r--   0        0        0      277 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/version.py
--rw-r--r--   0        0        0     9445 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/wheel.py
--rw-r--r--   0        0        0      714 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/windows_support.py
--rw-r--r--   0        0        0       74 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/.layout.json
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/__init__.py
--rw-r--r--   0        0        0       13 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/constraints.txt
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/INSTALLER
--rw-r--r--   0        0        0     1252 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/LICENSE
--rw-r--r--   0        0        0     7142 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/WHEEL
--rw-r--r--   0        0        0        5 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/top_level.txt
--rw-r--r--   0        0        0      963 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml/__init__.py
--rw-r--r--   0        0        0    39064 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml/decoder.py
--rw-r--r--   0        0        0    10233 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml/encoder.py
--rw-r--r--   0        0        0      602 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml/ordered.py
--rw-r--r--   0        0        0      701 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/toml/toml/tz.py
--rw-r--r--   0        0        0       75 2022-07-13 22:54:40.576411 pex-2.1.98/pex/vendor/_vendored/wheel/.layout.json
--rwxr-xr-x   0        0        0      198 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/.prefix/bin/wheel
--rw-r--r--   0        0        0       14 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/constraints.txt
--rw-r--r--   0        0        0        4 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/INSTALLER
--rw-r--r--   0        0        0     1125 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/LICENSE.txt
--rw-r--r--   0        0        0     2328 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/METADATA
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/REQUESTED
--rw-r--r--   0        0        0      110 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/WHEEL
--rw-r--r--   0        0        0      108 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/entry_points.txt
--rw-r--r--   0        0        0        6 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/top_level.txt
--rw-r--r--   0        0        0       23 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/__init__.py
--rw-r--r--   0        0        0      417 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/__main__.py
--rw-r--r--   0        0        0    19075 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/bdist_wheel.py
--rw-r--r--   0        0        0     2572 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/__init__.py
--rw-r--r--   0        0        0     9498 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/convert.py
--rw-r--r--   0        0        0     3364 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/pack.py
--rw-r--r--   0        0        0      673 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/unpack.py
--rw-r--r--   0        0        0    15930 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/macosx_libfile.py
--rw-r--r--   0        0        0     4344 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/metadata.py
--rw-r--r--   0        0        0     1257 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/pkginfo.py
--rw-r--r--   0        0        0      938 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/util.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/__init__.py
--rw-r--r--   0        0        0        0 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/packaging/__init__.py
--rw-r--r--   0        0        0     1812 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/packaging/_typing.py
--rw-r--r--   0        0        0    29560 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/packaging/tags.py
--rw-r--r--   0        0        0     7574 2022-07-13 22:54:40.580411 pex-2.1.98/pex/vendor/_vendored/wheel/wheel/wheelfile.py
--rw-r--r--   0        0        0      430 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/README.md
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/__init__.py
--rw-r--r--   0        0        0      368 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/bin_path.py
--rw-r--r--   0        0        0      376 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/install_scope.py
--rw-r--r--   0        0        0    25905 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/pex.py
--rw-r--r--   0        0        0    12529 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/virtualenv.py
--rw-r--r--   0        0        0   106996 2022-07-13 22:54:40.580411 pex-2.1.98/pex/venv/virtualenv_16.7.12_py
--rw-r--r--   0        0        0      155 2022-07-13 22:54:40.580411 pex-2.1.98/pex/version.py
--rw-r--r--   0        0        0     2405 2022-07-13 22:54:40.580411 pex-2.1.98/pyproject.toml
--rwxr-xr-x   0        0        0      286 2022-07-13 22:54:40.580411 pex-2.1.98/scripts/embed_virtualenv.sh
--rwxr-xr-x   0        0        0      368 2022-07-13 22:54:40.580411 pex-2.1.98/scripts/format.sh
--rwxr-xr-x   0        0        0     5429 2022-07-13 22:54:40.580411 pex-2.1.98/scripts/package.py
--rwxr-xr-x   0        0        0      657 2022-07-13 22:54:40.580411 pex-2.1.98/scripts/typecheck.sh
--rw-r--r--   0        0        0     5261 2022-07-13 22:54:40.580411 pex-2.1.98/tests/bin/test_sh_boot.py
--rw-r--r--   0        0        0     1822 2022-07-13 22:54:40.580411 pex-2.1.98/tests/build_system/test_pep_517.py
--rw-r--r--   0        0        0     2234 2022-07-13 22:54:40.580411 pex-2.1.98/tests/build_system/test_pep_518.py
--rw-r--r--   0        0        0     2302 2022-07-13 22:54:40.580411 pex-2.1.98/tests/commands/test_command.py
--rw-r--r--   0        0        0     1161 2022-07-13 22:54:40.580411 pex-2.1.98/tests/conftest.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.580411 pex-2.1.98/tests/data/__init__.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.580411 pex-2.1.98/tests/data/platforms/__init__.py
--rw-r--r--   0        0        0    27259 2022-07-13 22:54:40.580411 pex-2.1.98/tests/data/platforms/macosx_10_13_x86_64-cp-36-m.tags.txt
--rw-r--r--   0        0        0    25660 2022-07-13 22:54:40.580411 pex-2.1.98/tests/example_packages/MarkupSafe-1.0-cp27-cp27mu-linux_x86_64.whl
--rw-r--r--   0        0        0    32074 2022-07-13 22:54:40.580411 pex-2.1.98/tests/example_packages/PyAthena-1.11.5-py2.py3-none-any.whl
--rw-r--r--   0        0        0    37477 2022-07-13 22:54:40.580411 pex-2.1.98/tests/example_packages/PyAthena-1.9.0-py2.py3-none-any.whl
--rw-r--r--   0        0        0   983623 2022-07-13 22:54:40.588411 pex-2.1.98/tests/example_packages/aws_cfn_bootstrap-1.4-py2-none-any.whl
--rw-r--r--   0        0        0    56975 2022-07-13 22:54:40.588411 pex-2.1.98/tests/example_packages/pyparsing-2.1.10-py2.py3-none-any.whl
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/__init__.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/build_system/__init__.py
--rw-r--r--   0        0        0     1350 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/build_system/test_pep_517.py
--rw-r--r--   0        0        0     1756 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/build_system/test_pep_518.py
--rw-r--r--   0        0        0     5654 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_export.py
--rw-r--r--   0        0        0     3343 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_interpreter_inspect.py
--rw-r--r--   0        0        0     5373 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1413.py
--rw-r--r--   0        0        0     1288 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1665.py
--rw-r--r--   0        0        0     2616 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1667.py
--rw-r--r--   0        0        0     2204 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1688.py
--rw-r--r--   0        0        0     4665 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1711.py
--rw-r--r--   0        0        0     3200 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1734.py
--rw-r--r--   0        0        0     2691 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1741.py
--rw-r--r--   0        0        0     2417 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1801.py
--rw-r--r--   0        0        0     8278 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_issue_1821.py
--rw-r--r--   0        0        0     4016 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_local_project_lock.py
--rw-r--r--   0        0        0    75069 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_lock.py
--rw-r--r--   0        0        0    11683 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_lock_resolve_auth.py
--rw-r--r--   0        0        0     7407 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/cli/commands/test_vcs_lock.py
--rw-r--r--   0        0        0     5876 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/conftest.py
--rw-r--r--   0        0        0     2537 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_downloads.py
--rw-r--r--   0        0        0     2011 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_executuon_mode_venv.py
--rw-r--r--   0        0        0    62420 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_integration.py
--rw-r--r--   0        0        0    17225 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_interpreter_selection.py
--rw-r--r--   0        0        0      649 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1017.py
--rw-r--r--   0        0        0     2554 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1018.py
--rw-r--r--   0        0        0     2132 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1025.py
--rw-r--r--   0        0        0     3090 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1031.py
--rw-r--r--   0        0        0      886 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1179.py
--rw-r--r--   0        0        0      607 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1201.py
--rw-r--r--   0        0        0     2291 2022-07-13 22:54:40.588411 pex-2.1.98/tests/integration/test_issue_1202.py
--rw-r--r--   0        0        0     2200 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1218.py
--rw-r--r--   0        0        0     2922 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1225.py
--rw-r--r--   0        0        0     6909 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1232.py
--rw-r--r--   0        0        0     1608 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1302.py
--rw-r--r--   0        0        0      561 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1316.py
--rw-r--r--   0        0        0      647 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1336.py
--rw-r--r--   0        0        0     3974 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1422.py
--rw-r--r--   0        0        0     1151 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1447.py
--rw-r--r--   0        0        0     1404 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1479.py
--rw-r--r--   0        0        0     3219 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1520.py
--rw-r--r--   0        0        0     1148 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1537.py
--rw-r--r--   0        0        0     1252 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1550.py
--rw-r--r--   0        0        0     2683 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1560.py
--rw-r--r--   0        0        0     4902 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1597.py
--rw-r--r--   0        0        0     1216 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1598.py
--rw-r--r--   0        0        0     5884 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1656.py
--rw-r--r--   0        0        0     1640 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1683.py
--rw-r--r--   0        0        0     2133 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1726.py
--rw-r--r--   0        0        0     1441 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1730.py
--rw-r--r--   0        0        0     3130 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1802.py
--rw-r--r--   0        0        0     3405 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1809.py
--rw-r--r--   0        0        0     1561 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1817.py
--rw-r--r--   0        0        0     4234 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_1825.py
--rw-r--r--   0        0        0      988 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_434.py
--rw-r--r--   0        0        0     2162 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_539.py
--rw-r--r--   0        0        0      715 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_598.py
--rw-r--r--   0        0        0     1319 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_661.py
--rw-r--r--   0        0        0     2950 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_729.py
--rw-r--r--   0        0        0     1341 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_736.py
--rw-r--r--   0        0        0     2314 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_745.py
--rw-r--r--   0        0        0     1849 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_749.py
--rw-r--r--   0        0        0     1750 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_898.py
--rw-r--r--   0        0        0     1772 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_899.py
--rw-r--r--   0        0        0      921 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_940.py
--rw-r--r--   0        0        0     2046 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_issue_996.py
--rw-r--r--   0        0        0     1862 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_layout.py
--rw-r--r--   0        0        0    16860 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_lock_resolver.py
--rw-r--r--   0        0        0     5778 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_locked_resolve.py
--rw-r--r--   0        0        0    15297 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_pex_bootstrapper.py
--rw-r--r--   0        0        0     3876 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_pex_entry_points.py
--rw-r--r--   0        0        0     4637 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_pex_import.py
--rw-r--r--   0        0        0     7478 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_reexec.py
--rw-r--r--   0        0        0     6086 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_reproducible.py
--rw-r--r--   0        0        0     4772 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_setproctitle.py
--rw-r--r--   0        0        0     6306 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_sh_boot.py
--rw-r--r--   0        0        0     9535 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_shebang_length_limit.py
--rw-r--r--   0        0        0     1576 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/test_variables.py
--rw-r--r--   0        0        0     8716 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/tools/commands/test_venv.py
--rw-r--r--   0        0        0     2545 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_issue_1630.py
--rw-r--r--   0        0        0     5866 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_issue_1637.py
--rw-r--r--   0        0        0     2331 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_issue_1641.py
--rw-r--r--   0        0        0     2222 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_issue_1668.py
--rw-r--r--   0        0        0     4550 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_issue_1745.py
--rw-r--r--   0        0        0     3432 2022-07-13 22:54:40.592411 pex-2.1.98/tests/integration/venv_ITs/test_virtualenv.py
--rw-r--r--   0        0        0     3525 2022-07-13 22:54:40.592411 pex-2.1.98/tests/pip/test_tailer.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/__init__.py
--rw-r--r--   0        0        0      276 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/conftest.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/lockfile/__init__.py
--rw-r--r--   0        0        0     5981 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/lockfile/test_download_manager.py
--rw-r--r--   0        0        0    18787 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/lockfile/test_json_codec.py
--rw-r--r--   0        0        0     3714 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/lockfile/test_lockfile.py
--rw-r--r--   0        0        0    31051 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/test_locked_resolve.py
--rw-r--r--   0        0        0     2636 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/test_path_mappings.py
--rw-r--r--   0        0        0    10589 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/test_pex_repository_resolver.py
--rw-r--r--   0        0        0     5087 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/test_resolver_options.py
--rw-r--r--   0        0        0    14237 2022-07-13 22:54:40.592411 pex-2.1.98/tests/resolve/test_target_options.py
--rw-r--r--   0        0        0     7030 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_bdist_pex.py
--rw-r--r--   0        0        0    13563 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_common.py
--rw-r--r--   0        0        0     1683 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_compatibility.py
--rw-r--r--   0        0        0     3007 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_compiler.py
--rw-r--r--   0        0        0    11640 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_dist_metadata.py
--rw-r--r--   0        0        0     4000 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_enum.py
--rw-r--r--   0        0        0    17201 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_environment.py
--rw-r--r--   0        0        0     3708 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_execution_mode.py
--rw-r--r--   0        0        0     3575 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_executor.py
--rw-r--r--   0        0        0     1680 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_fetcher.py
--rw-r--r--   0        0        0     3429 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_finders.py
--rw-r--r--   0        0        0     2049 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_hashing.py
--rw-r--r--   0        0        0     2199 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_inherits_path_option.py
--rw-r--r--   0        0        0    19052 2022-07-13 22:54:40.592411 pex-2.1.98/tests/test_interpreter.py
--rw-r--r--   0        0        0     3500 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_interpreter_constraints.py
--rw-r--r--   0        0        0     3433 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_jobs.py
--rw-r--r--   0        0        0     1898 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_packaging.py
--rw-r--r--   0        0        0     3123 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pep_376.py
--rw-r--r--   0        0        0     1933 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pep_425.py
--rw-r--r--   0        0        0     3472 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pep_508.py
--rw-r--r--   0        0        0    31154 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex.py
--rw-r--r--   0        0        0     8003 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex_binary.py
--rw-r--r--   0        0        0    10749 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex_bootstrapper.py
--rw-r--r--   0        0        0    17103 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex_builder.py
--rw-r--r--   0        0        0     5344 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex_info.py
--rw-r--r--   0        0        0     2732 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pex_warnings.py
--rw-r--r--   0        0        0     9165 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_pip.py
--rw-r--r--   0        0        0     4916 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_platform.py
--rw-r--r--   0        0        0    19681 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_requirements.py
--rw-r--r--   0        0        0    22891 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_resolver.py
--rw-r--r--   0        0        0      572 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_sorted_tuple.py
--rw-r--r--   0        0        0     8209 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_targets.py
--rw-r--r--   0        0        0     2347 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_third_party.py
--rw-r--r--   0        0        0     7059 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_util.py
--rw-r--r--   0        0        0     8139 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_variables.py
--rw-r--r--   0        0        0     2243 2022-07-13 22:54:40.596411 pex-2.1.98/tests/test_vendor.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.596411 pex-2.1.98/tests/tools/__init__.py
--rw-r--r--   0        0        0      131 2022-07-13 22:54:40.596411 pex-2.1.98/tests/tools/commands/__init__.py
--rw-r--r--   0        0        0     5641 2022-07-13 22:54:40.596411 pex-2.1.98/tests/tools/commands/test_interpreter_command.py
--rw-r--r--   0        0        0     9136 2022-07-13 22:54:40.596411 pex-2.1.98/tests/tools/commands/test_repository.py
--rw-r--r--   0        0        0    27025 2022-07-13 22:54:40.596411 pex-2.1.98/tests/tools/commands/test_venv.py
--rw-r--r--   0        0        0     6260 2022-07-13 22:54:40.596411 pex-2.1.98/tox.ini
--rw-r--r--   0        0        0     7266 1970-01-01 00:00:00.000000 pex-2.1.98/PKG-INFO
+-rw-r--r--   0        0        0     8997 2022-07-14 16:31:21.806360 pex-2.1.99/.github/workflows/ci.yml
+-rw-r--r--   0        0        0     3330 2022-07-14 16:31:21.806360 pex-2.1.99/.github/workflows/release.yml
+-rw-r--r--   0        0        0      148 2022-07-14 16:31:21.806360 pex-2.1.99/.gitignore
+-rw-r--r--   0        0        0      262 2022-07-14 16:31:21.806360 pex-2.1.99/.readthedocs.yml
+-rw-r--r--   0        0        0   110081 2022-07-14 16:31:21.806360 pex-2.1.99/CHANGES.rst
+-rw-r--r--   0        0        0    11323 2022-07-14 16:31:21.806360 pex-2.1.99/LICENSE
+-rw-r--r--   0        0        0      194 2022-07-14 16:31:21.806360 pex-2.1.99/MANIFEST.in
+-rw-r--r--   0        0        0     5534 2022-07-14 16:31:21.806360 pex-2.1.99/README.rst
+-rw-r--r--   0        0        0     2675 2022-07-14 16:31:21.806360 pex-2.1.99/RELEASE.rst
+-rw-r--r--   0        0        0      896 2022-07-14 16:31:21.806360 pex-2.1.99/docker/base/Dockerfile
+-rw-r--r--   0        0        0      483 2022-07-14 16:31:21.806360 pex-2.1.99/docker/user/Dockerfile
+-rwxr-xr-x   0        0        0      371 2022-07-14 16:31:21.806360 pex-2.1.99/docker/user/create_docker_image_user.sh
+-rw-r--r--   0        0        0     6750 2022-07-14 16:31:21.806360 pex-2.1.99/docs/Makefile
+-rw-r--r--   0        0        0     1299 2022-07-14 16:31:21.806360 pex-2.1.99/docs/_ext/vars.py
+-rw-r--r--   0        0        0       79 2022-07-14 16:31:21.806360 pex-2.1.99/docs/api/vars.rst
+-rw-r--r--   0        0        0    18814 2022-07-14 16:31:21.806360 pex-2.1.99/docs/buildingpex.rst
+-rw-r--r--   0        0        0     8585 2022-07-14 16:31:21.806360 pex-2.1.99/docs/conf.py
+-rw-r--r--   0        0        0     1441 2022-07-14 16:31:21.806360 pex-2.1.99/docs/index.rst
+-rw-r--r--   0        0        0     5516 2022-07-14 16:31:21.806360 pex-2.1.99/docs/recipes.rst
+-rw-r--r--   0        0        0      196 2022-07-14 16:31:21.806360 pex-2.1.99/docs/rtd/requirements.txt
+-rw-r--r--   0        0        0     1888 2022-07-14 16:31:21.806360 pex-2.1.99/docs/whatispex.rst
+-rwxr-xr-x   0        0        0     1101 2022-07-14 16:31:21.806360 pex-2.1.99/dtox.sh
+-rw-r--r--   0        0        0      990 2022-07-14 16:31:21.806360 pex-2.1.99/mypy.ini
+-rw-r--r--   0        0        0      401 2022-07-14 16:31:21.806360 pex-2.1.99/pex/__init__.py
+-rw-r--r--   0        0        0      235 2022-07-14 16:31:21.806360 pex-2.1.99/pex/__main__.py
+-rw-r--r--   0        0        0      601 2022-07-14 16:31:21.806360 pex-2.1.99/pex/argparse.py
+-rw-r--r--   0        0        0      483 2022-07-14 16:31:21.806360 pex-2.1.99/pex/attrs.py
+-rw-r--r--   0        0        0     5898 2022-07-14 16:31:21.806360 pex-2.1.99/pex/auth.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.806360 pex-2.1.99/pex/bin/__init__.py
+-rwxr-xr-x   0        0        0    34811 2022-07-14 16:31:21.806360 pex-2.1.99/pex/bin/pex.py
+-rw-r--r--   0        0        0     9760 2022-07-14 16:31:21.806360 pex-2.1.99/pex/bin/sh_boot.py
+-rw-r--r--   0        0        0     3084 2022-07-14 16:31:21.806360 pex-2.1.99/pex/bootstrap.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.806360 pex-2.1.99/pex/build_system/__init__.py
+-rw-r--r--   0        0        0     4077 2022-07-14 16:31:21.810360 pex-2.1.99/pex/build_system/pep_517.py
+-rw-r--r--   0        0        0     3907 2022-07-14 16:31:21.810360 pex-2.1.99/pex/build_system/pep_518.py
+-rw-r--r--   0        0        0     1598 2022-07-14 16:31:21.810360 pex-2.1.99/pex/build_system/testing.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/__init__.py
+-rw-r--r--   0        0        0      230 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/__main__.py
+-rw-r--r--   0        0        0     2971 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/command.py
+-rw-r--r--   0        0        0      465 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/commands/__init__.py
+-rw-r--r--   0        0        0     6689 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/commands/interpreter.py
+-rw-r--r--   0        0        0    28819 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/commands/lock.py
+-rw-r--r--   0        0        0     1102 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/pex.py
+-rw-r--r--   0        0        0      771 2022-07-14 16:31:21.810360 pex-2.1.99/pex/cli/testing.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/commands/__init__.py
+-rw-r--r--   0        0        0    13469 2022-07-14 16:31:21.810360 pex-2.1.99/pex/commands/command.py
+-rw-r--r--   0        0        0    27541 2022-07-14 16:31:21.810360 pex-2.1.99/pex/common.py
+-rw-r--r--   0        0        0     6175 2022-07-14 16:31:21.810360 pex-2.1.99/pex/compatibility.py
+-rw-r--r--   0        0        0     3592 2022-07-14 16:31:21.810360 pex-2.1.99/pex/compiler.py
+-rw-r--r--   0        0        0    28300 2022-07-14 16:31:21.810360 pex-2.1.99/pex/dist_metadata.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/distutils/__init__.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/distutils/commands/__init__.py
+-rw-r--r--   0        0        0     5082 2022-07-14 16:31:21.810360 pex-2.1.99/pex/distutils/commands/bdist_pex.py
+-rw-r--r--   0        0        0     3896 2022-07-14 16:31:21.810360 pex-2.1.99/pex/enum.py
+-rw-r--r--   0        0        0    30226 2022-07-14 16:31:21.810360 pex-2.1.99/pex/environment.py
+-rw-r--r--   0        0        0     4151 2022-07-14 16:31:21.810360 pex-2.1.99/pex/executor.py
+-rw-r--r--   0        0        0     5192 2022-07-14 16:31:21.810360 pex-2.1.99/pex/fetcher.py
+-rw-r--r--   0        0        0     3457 2022-07-14 16:31:21.810360 pex-2.1.99/pex/finders.py
+-rw-r--r--   0        0        0      776 2022-07-14 16:31:21.810360 pex-2.1.99/pex/fingerprinted_distribution.py
+-rw-r--r--   0        0        0     7375 2022-07-14 16:31:21.810360 pex-2.1.99/pex/hashing.py
+-rw-r--r--   0        0        0     1007 2022-07-14 16:31:21.810360 pex-2.1.99/pex/inherit_path.py
+-rw-r--r--   0        0        0    50414 2022-07-14 16:31:21.810360 pex-2.1.99/pex/interpreter.py
+-rw-r--r--   0        0        0     8072 2022-07-14 16:31:21.810360 pex-2.1.99/pex/interpreter_constraints.py
+-rw-r--r--   0        0        0    18654 2022-07-14 16:31:21.810360 pex-2.1.99/pex/jobs.py
+-rw-r--r--   0        0        0     9606 2022-07-14 16:31:21.810360 pex-2.1.99/pex/layout.py
+-rw-r--r--   0        0        0     1710 2022-07-14 16:31:21.810360 pex-2.1.99/pex/network_configuration.py
+-rw-r--r--   0        0        0     3747 2022-07-14 16:31:21.810360 pex-2.1.99/pex/orderedset.py
+-rw-r--r--   0        0        0    24114 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pep_376.py
+-rw-r--r--   0        0        0     5719 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pep_425.py
+-rw-r--r--   0        0        0     2329 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pep_440.py
+-rw-r--r--   0        0        0     1120 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pep_503.py
+-rw-r--r--   0        0        0     5515 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pep_508.py
+-rw-r--r--   0        0        0    31790 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pex.py
+-rw-r--r--   0        0        0    28193 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pex_bootstrapper.py
+-rw-r--r--   0        0        0    32126 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pex_builder.py
+-rw-r--r--   0        0        0    16993 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pex_info.py
+-rw-r--r--   0        0        0     1137 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pex_warnings.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/__init__.py
+-rw-r--r--   0        0        0     1147 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/download_observer.py
+-rw-r--r--   0        0        0     5298 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/foreign_platform.py
+-rw-r--r--   0        0        0     1463 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/foreign_platform_patches.py
+-rw-r--r--   0        0        0     2123 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/local_project.py
+-rw-r--r--   0        0        0     3632 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/log_analyzer.py
+-rw-r--r--   0        0        0     4469 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/tailer.py
+-rw-r--r--   0        0        0    31906 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/tool.py
+-rw-r--r--   0        0        0     2810 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pip/vcs.py
+-rw-r--r--   0        0        0    13464 2022-07-14 16:31:21.810360 pex-2.1.99/pex/platforms.py
+-rw-r--r--   0        0        0     8432 2022-07-14 16:31:21.810360 pex-2.1.99/pex/pyenv.py
+-rw-r--r--   0        0        0     3925 2022-07-14 16:31:21.810360 pex-2.1.99/pex/rank.py
+-rw-r--r--   0        0        0    24615 2022-07-14 16:31:21.810360 pex-2.1.99/pex/requirements.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.810360 pex-2.1.99/pex/resolve/__init__.py
+-rw-r--r--   0        0        0     3376 2022-07-14 16:31:21.810360 pex-2.1.99/pex/resolve/configured_resolver.py
+-rw-r--r--   0        0        0     6406 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/downloads.py
+-rw-r--r--   0        0        0    16537 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lock_resolver.py
+-rw-r--r--   0        0        0    29188 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/locked_resolve.py
+-rw-r--r--   0        0        0    16114 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/locker.py
+-rw-r--r--   0        0        0    10040 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/locker_patches.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/__init__.py
+-rw-r--r--   0        0        0    14511 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/create.py
+-rw-r--r--   0        0        0     7981 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/download_manager.py
+-rw-r--r--   0        0        0    14188 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/json_codec.py
+-rw-r--r--   0        0        0     5034 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/model.py
+-rw-r--r--   0        0        0     5037 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/subset.py
+-rw-r--r--   0        0        0    13964 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/lockfile/updater.py
+-rw-r--r--   0        0        0     2097 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/path_mappings.py
+-rw-r--r--   0        0        0     4420 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/pex_repository_resolver.py
+-rw-r--r--   0        0        0     2532 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/requirement_configuration.py
+-rw-r--r--   0        0        0     1652 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/requirement_options.py
+-rw-r--r--   0        0        0     2737 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/resolved_requirement.py
+-rw-r--r--   0        0        0     3037 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/resolver_configuration.py
+-rw-r--r--   0        0        0    20711 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/resolver_options.py
+-rw-r--r--   0        0        0     3038 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/resolvers.py
+-rw-r--r--   0        0        0     7630 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/target_configuration.py
+-rw-r--r--   0        0        0    11496 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/target_options.py
+-rw-r--r--   0        0        0     2218 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolve/testing.py
+-rw-r--r--   0        0        0    51072 2022-07-14 16:31:21.814360 pex-2.1.99/pex/resolver.py
+-rw-r--r--   0        0        0     2945 2022-07-14 16:31:21.814360 pex-2.1.99/pex/result.py
+-rw-r--r--   0        0        0     2091 2022-07-14 16:31:21.814360 pex-2.1.99/pex/sorted_tuple.py
+-rw-r--r--   0        0        0    12123 2022-07-14 16:31:21.814360 pex-2.1.99/pex/targets.py
+-rw-r--r--   0        0        0    22595 2022-07-14 16:31:21.814360 pex-2.1.99/pex/testing.py
+-rw-r--r--   0        0        0    22685 2022-07-14 16:31:21.814360 pex-2.1.99/pex/third_party/__init__.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/__init__.py
+-rw-r--r--   0        0        0      244 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/__main__.py
+-rw-r--r--   0        0        0      440 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/command.py
+-rw-r--r--   0        0        0      621 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/__init__.py
+-rw-r--r--   0        0        0     3781 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/digraph.py
+-rw-r--r--   0        0        0     5936 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/graph.py
+-rw-r--r--   0        0        0      961 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/info.py
+-rw-r--r--   0        0        0     4528 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/interpreter.py
+-rw-r--r--   0        0        0    16196 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/repository.py
+-rw-r--r--   0        0        0     7525 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/commands/venv.py
+-rw-r--r--   0        0        0     3435 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tools/main.py
+-rw-r--r--   0        0        0     4614 2022-07-14 16:31:21.814360 pex-2.1.99/pex/tracer.py
+-rw-r--r--   0        0        0     2538 2022-07-14 16:31:21.814360 pex-2.1.99/pex/typing.py
+-rw-r--r--   0        0        0     9347 2022-07-14 16:31:21.814360 pex-2.1.99/pex/util.py
+-rw-r--r--   0        0        0    29372 2022-07-14 16:31:21.814360 pex-2.1.99/pex/variables.py
+-rw-r--r--   0        0        0     2364 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/README.md
+-rw-r--r--   0        0        0    12539 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/__init__.py
+-rw-r--r--   0        0        0    16893 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/__main__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/__init__.py
+-rw-r--r--   0        0        0       80 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/.layout.json
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/__init__.py
+-rw-r--r--   0        0        0     1672 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/__init__.py
+-rw-r--r--   0        0        0    15100 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/__init__.pyi
+-rw-r--r--   0        0        0     4165 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_cmp.py
+-rw-r--r--   0        0        0      317 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_cmp.pyi
+-rw-r--r--   0        0        0     8396 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_compat.py
+-rw-r--r--   0        0        0      892 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_config.py
+-rw-r--r--   0        0        0    14753 2022-07-14 16:31:21.814360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_funcs.py
+-rw-r--r--   0        0        0   102691 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_make.py
+-rw-r--r--   0        0        0     5728 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_next_gen.py
+-rw-r--r--   0        0        0     2194 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_version_info.py
+-rw-r--r--   0        0        0      209 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/_version_info.pyi
+-rw-r--r--   0        0        0     4078 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/converters.py
+-rw-r--r--   0        0        0      416 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/converters.pyi
+-rw-r--r--   0        0        0     1981 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/exceptions.py
+-rw-r--r--   0        0        0      539 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/exceptions.pyi
+-rw-r--r--   0        0        0     1124 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/filters.py
+-rw-r--r--   0        0        0      215 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/filters.pyi
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/py.typed
+-rw-r--r--   0        0        0     1466 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/setters.py
+-rw-r--r--   0        0        0      573 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/setters.pyi
+-rw-r--r--   0        0        0    15966 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/validators.py
+-rw-r--r--   0        0        0     2268 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attr/validators.pyi
+-rw-r--r--   0        0        0      752 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/AUTHORS.rst
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1082 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/LICENSE
+-rw-r--r--   0        0        0     9838 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/WHEEL
+-rw-r--r--   0        0        0      199 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/direct_url.json
+-rw-r--r--   0        0        0       11 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/top_level.txt
+-rw-r--r--   0        0        0     1745 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/__init__.py
+-rw-r--r--   0        0        0     1982 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/__init__.pyi
+-rw-r--r--   0        0        0      197 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/converters.py
+-rw-r--r--   0        0        0      197 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/exceptions.py
+-rw-r--r--   0        0        0      191 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/filters.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/py.typed
+-rw-r--r--   0        0        0      191 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/setters.py
+-rw-r--r--   0        0        0      197 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/attrs/attrs/validators.py
+-rw-r--r--   0        0        0       77 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/.layout.json
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/__init__.py
+-rw-r--r--   0        0        0       33 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/constraints.txt
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/INSTALLER
+-rw-r--r--   0        0        0      197 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE
+-rw-r--r--   0        0        0    10174 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.APACHE
+-rw-r--r--   0        0        0     1344 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.BSD
+-rw-r--r--   0        0        0    13299 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/WHEEL
+-rw-r--r--   0        0        0       10 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/top_level.txt
+-rw-r--r--   0        0        0      726 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/__about__.py
+-rw-r--r--   0        0        0      562 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/__init__.py
+-rw-r--r--   0        0        0     1128 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_compat.py
+-rw-r--r--   0        0        0     2022 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_structures.py
+-rw-r--r--   0        0        0     1812 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_typing.py
+-rw-r--r--   0        0        0     9741 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/markers.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/py.typed
+-rw-r--r--   0        0        0     5388 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/requirements.py
+-rw-r--r--   0        0        0    32208 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/specifiers.py
+-rw-r--r--   0        0        0    29561 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/tags.py
+-rw-r--r--   0        0        0     4385 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/utils.py
+-rw-r--r--   0        0        0    15974 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/packaging/version.py
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1023 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/LICENSE
+-rw-r--r--   0        0        0     3636 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/METADATA
+-rw-r--r--   0        0        0      564 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/RECORD
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/WHEEL
+-rw-r--r--   0        0        0       10 2022-07-14 16:31:21.818360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/top_level.txt
+-rw-r--r--   0        0        0   273365 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing.py
+-rw-r--r--   0        0        0       73 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/.layout.json
+-rwxr-xr-x   0        0        0      211 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/.prefix/bin/pip
+-rwxr-xr-x   0        0        0      211 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/.prefix/bin/pip3
+-rwxr-xr-x   0        0        0      211 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/.prefix/bin/pip3.8
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1090 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/LICENSE.txt
+-rw-r--r--   0        0        0     4310 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/WHEEL
+-rw-r--r--   0        0        0      195 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/direct_url.json
+-rw-r--r--   0        0        0      124 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/entry_points.txt
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/top_level.txt
+-rw-r--r--   0        0        0      455 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/__init__.py
+-rw-r--r--   0        0        0      911 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/__main__.py
+-rw-r--r--   0        0        0      495 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/__init__.py
+-rw-r--r--   0        0        0     8089 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/build_env.py
+-rw-r--r--   0        0        0    12249 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cache.py
+-rw-r--r--   0        0        0      132 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/__init__.py
+-rw-r--r--   0        0        0     6547 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/autocompletion.py
+-rw-r--r--   0        0        0     9337 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/base_command.py
+-rw-r--r--   0        0        0    28618 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/cmdoptions.py
+-rw-r--r--   0        0        0      975 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/command_context.py
+-rw-r--r--   0        0        0     2616 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/main.py
+-rw-r--r--   0        0        0     2830 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/main_parser.py
+-rw-r--r--   0        0        0    10388 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/parser.py
+-rw-r--r--   0        0        0     9121 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/progress_bars.py
+-rw-r--r--   0        0        0    16455 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/req_command.py
+-rw-r--r--   0        0        0     5509 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/spinners.py
+-rw-r--r--   0        0        0      156 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/status_codes.py
+-rw-r--r--   0        0        0     4101 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/__init__.py
+-rw-r--r--   0        0        0     7555 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/cache.py
+-rw-r--r--   0        0        0     1677 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/check.py
+-rw-r--r--   0        0        0     3081 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/completion.py
+-rw-r--r--   0        0        0     9327 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/configuration.py
+-rw-r--r--   0        0        0     7315 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/debug.py
+-rw-r--r--   0        0        0     4932 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/download.py
+-rw-r--r--   0        0        0     3871 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/freeze.py
+-rw-r--r--   0        0        0     1843 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/hash.py
+-rw-r--r--   0        0        0     1294 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/help.py
+-rw-r--r--   0        0        0    27410 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/install.py
+-rw-r--r--   0        0        0    11519 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/list.py
+-rw-r--r--   0        0        0     6033 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/search.py
+-rw-r--r--   0        0        0     6996 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/show.py
+-rw-r--r--   0        0        0     3311 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/uninstall.py
+-rw-r--r--   0        0        0     6802 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/wheel.py
+-rw-r--r--   0        0        0    13904 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/configuration.py
+-rw-r--r--   0        0        0      959 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/__init__.py
+-rw-r--r--   0        0        0     1426 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/base.py
+-rw-r--r--   0        0        0      761 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/installed.py
+-rw-r--r--   0        0        0     4087 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/sdist.py
+-rw-r--r--   0        0        0     1295 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/wheel.py
+-rw-r--r--   0        0        0    13003 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/exceptions.py
+-rw-r--r--   0        0        0       30 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/index/__init__.py
+-rw-r--r--   0        0        0    22070 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/index/collector.py
+-rw-r--r--   0        0        0    37454 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/index/package_finder.py
+-rw-r--r--   0        0        0     6731 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/locations.py
+-rw-r--r--   0        0        0      437 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/main.py
+-rw-r--r--   0        0        0       63 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/__init__.py
+-rw-r--r--   0        0        0     1196 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/candidate.py
+-rw-r--r--   0        0        0     6884 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/direct_url.py
+-rw-r--r--   0        0        0     2823 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/format_control.py
+-rw-r--r--   0        0        0     1161 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/index.py
+-rw-r--r--   0        0        0     7471 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/link.py
+-rw-r--r--   0        0        0      778 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/scheme.py
+-rw-r--r--   0        0        0     4751 2022-07-14 16:31:21.822360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/search_scope.py
+-rw-r--r--   0        0        0     2045 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/selection_prefs.py
+-rw-r--r--   0        0        0     4070 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/target_python.py
+-rw-r--r--   0        0        0     2772 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/wheel.py
+-rw-r--r--   0        0        0       50 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/__init__.py
+-rw-r--r--   0        0        0    11652 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/auth.py
+-rw-r--r--   0        0        0     2329 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/cache.py
+-rw-r--r--   0        0        0     6401 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/download.py
+-rw-r--r--   0        0        0     8121 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/lazy_wheel.py
+-rw-r--r--   0        0        0    15449 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/session.py
+-rw-r--r--   0        0        0     4172 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/utils.py
+-rw-r--r--   0        0        0     1883 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/xmlrpc.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/__init__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/__init__.py
+-rw-r--r--   0        0        0     1255 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata.py
+-rw-r--r--   0        0        0     2011 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata_legacy.py
+-rw-r--r--   0        0        0     1466 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel.py
+-rw-r--r--   0        0        0     3347 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel_legacy.py
+-rw-r--r--   0        0        0     5216 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/check.py
+-rw-r--r--   0        0        0    10411 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/freeze.py
+-rw-r--r--   0        0        0       51 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/__init__.py
+-rw-r--r--   0        0        0     1488 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/editable_legacy.py
+-rw-r--r--   0        0        0     4281 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/legacy.py
+-rw-r--r--   0        0        0    31247 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/wheel.py
+-rw-r--r--   0        0        0    22460 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/prepare.py
+-rw-r--r--   0        0        0     7400 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/pyproject.py
+-rw-r--r--   0        0        0     3133 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/__init__.py
+-rw-r--r--   0        0        0    16135 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/constructors.py
+-rw-r--r--   0        0        0    18594 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_file.py
+-rw-r--r--   0        0        0    33420 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_install.py
+-rw-r--r--   0        0        0     7887 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_set.py
+-rw-r--r--   0        0        0     4691 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_tracker.py
+-rw-r--r--   0        0        0    23771 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_uninstall.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/__init__.py
+-rw-r--r--   0        0        0      683 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/base.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/__init__.py
+-rw-r--r--   0        0        0    18234 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/resolver.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/__init__.py
+-rw-r--r--   0        0        0     5061 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/base.py
+-rw-r--r--   0        0        0    20035 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/candidates.py
+-rw-r--r--   0        0        0    18946 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/factory.py
+-rw-r--r--   0        0        0     3773 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/found_candidates.py
+-rw-r--r--   0        0        0     7339 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/provider.py
+-rw-r--r--   0        0        0     2857 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/reporter.py
+-rw-r--r--   0        0        0     5969 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/requirements.py
+-rw-r--r--   0        0        0    11634 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/resolver.py
+-rw-r--r--   0        0        0     6745 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/self_outdated_check.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/__init__.py
+-rw-r--r--   0        0        0     1349 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/appdirs.py
+-rw-r--r--   0        0        0     9489 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/compat.py
+-rw-r--r--   0        0        0     5690 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/compatibility_tags.py
+-rw-r--r--   0        0        0      295 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/datetime.py
+-rw-r--r--   0        0        0     3318 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/deprecation.py
+-rw-r--r--   0        0        0     4146 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/direct_url_helpers.py
+-rw-r--r--   0        0        0     1350 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/distutils_args.py
+-rw-r--r--   0        0        0     1284 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/encoding.py
+-rw-r--r--   0        0        0     1152 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/entrypoints.py
+-rw-r--r--   0        0        0     6943 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/filesystem.py
+-rw-r--r--   0        0        0      847 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/filetypes.py
+-rw-r--r--   0        0        0     3297 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/glibc.py
+-rw-r--r--   0        0        0     5297 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/hashes.py
+-rw-r--r--   0        0        0      810 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/inject_securetransport.py
+-rw-r--r--   0        0        0    13093 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/logging.py
+-rw-r--r--   0        0        0    28047 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/misc.py
+-rw-r--r--   0        0        0     1201 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/models.py
+-rw-r--r--   0        0        0     3036 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/packaging.py
+-rw-r--r--   0        0        0     3404 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/parallel.py
+-rw-r--r--   0        0        0     1254 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/pkg_resources.py
+-rw-r--r--   0        0        0     5058 2022-07-14 16:31:21.826360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/setuptools_build.py
+-rw-r--r--   0        0        0    10866 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/subprocess.py
+-rw-r--r--   0        0        0     8845 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/temp_dir.py
+-rw-r--r--   0        0        0     1401 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/typing.py
+-rw-r--r--   0        0        0     9488 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/unpacking.py
+-rw-r--r--   0        0        0     1527 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/urls.py
+-rw-r--r--   0        0        0     3706 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/virtualenv.py
+-rw-r--r--   0        0        0     7303 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/wheel.py
+-rw-r--r--   0        0        0      617 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/__init__.py
+-rw-r--r--   0        0        0     4016 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/bazaar.py
+-rw-r--r--   0        0        0    15599 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/git.py
+-rw-r--r--   0        0        0     5564 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/mercurial.py
+-rw-r--r--   0        0        0    12558 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/subversion.py
+-rw-r--r--   0        0        0    23767 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/versioncontrol.py
+-rw-r--r--   0        0        0    11816 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/wheel_builder.py
+-rw-r--r--   0        0        0     4788 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/__init__.py
+-rw-r--r--   0        0        0    25907 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/appdirs.py
+-rw-r--r--   0        0        0      302 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/__init__.py
+-rw-r--r--   0        0        0     1295 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/_cmd.py
+-rw-r--r--   0        0        0     4882 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/adapter.py
+-rw-r--r--   0        0        0      805 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/cache.py
+-rw-r--r--   0        0        0       86 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/__init__.py
+-rw-r--r--   0        0        0     4153 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/file_cache.py
+-rw-r--r--   0        0        0      856 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/redis_cache.py
+-rw-r--r--   0        0        0      695 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/compat.py
+-rw-r--r--   0        0        0    14149 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/controller.py
+-rw-r--r--   0        0        0     2533 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/filewrapper.py
+-rw-r--r--   0        0        0     4070 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/heuristics.py
+-rw-r--r--   0        0        0     7091 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/serialize.py
+-rw-r--r--   0        0        0      690 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/wrapper.py
+-rw-r--r--   0        0        0       62 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/__init__.py
+-rw-r--r--   0        0        0      255 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/__main__.py
+-rw-r--r--   0        0        0   281608 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/cacert.pem
+-rw-r--r--   0        0        0     2315 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/core.py
+-rw-r--r--   0        0        0     1559 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/__init__.py
+-rw-r--r--   0        0        0    31254 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5freq.py
+-rw-r--r--   0        0        0     1757 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5prober.py
+-rw-r--r--   0        0        0     9411 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/chardistribution.py
+-rw-r--r--   0        0        0     3787 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetgroupprober.py
+-rw-r--r--   0        0        0     5110 2022-07-14 16:31:21.830360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetprober.py
+-rw-r--r--   0        0        0        1 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/__init__.py
+-rw-r--r--   0        0        0     2774 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/chardetect.py
+-rw-r--r--   0        0        0     3590 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/codingstatemachine.py
+-rw-r--r--   0        0        0     1134 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/compat.py
+-rw-r--r--   0        0        0     1855 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/cp949prober.py
+-rw-r--r--   0        0        0     1661 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/enums.py
+-rw-r--r--   0        0        0     3950 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/escprober.py
+-rw-r--r--   0        0        0    10510 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/escsm.py
+-rw-r--r--   0        0        0     3749 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/eucjpprober.py
+-rw-r--r--   0        0        0    13546 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrfreq.py
+-rw-r--r--   0        0        0     1748 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrprober.py
+-rw-r--r--   0        0        0    31621 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwfreq.py
+-rw-r--r--   0        0        0     1747 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwprober.py
+-rw-r--r--   0        0        0    20715 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312freq.py
+-rw-r--r--   0        0        0     1754 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312prober.py
+-rw-r--r--   0        0        0    13838 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/hebrewprober.py
+-rw-r--r--   0        0        0    25777 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/jisfreq.py
+-rw-r--r--   0        0        0    19643 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/jpcntx.py
+-rw-r--r--   0        0        0    12839 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langbulgarianmodel.py
+-rw-r--r--   0        0        0    17948 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langcyrillicmodel.py
+-rw-r--r--   0        0        0    12688 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langgreekmodel.py
+-rw-r--r--   0        0        0    11345 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhebrewmodel.py
+-rw-r--r--   0        0        0    12592 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhungarianmodel.py
+-rw-r--r--   0        0        0    11290 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langthaimodel.py
+-rw-r--r--   0        0        0    11102 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langturkishmodel.py
+-rw-r--r--   0        0        0     5370 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/latin1prober.py
+-rw-r--r--   0        0        0     3413 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcharsetprober.py
+-rw-r--r--   0        0        0     2012 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcsgroupprober.py
+-rw-r--r--   0        0        0    25481 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcssm.py
+-rw-r--r--   0        0        0     5657 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcharsetprober.py
+-rw-r--r--   0        0        0     3546 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcsgroupprober.py
+-rw-r--r--   0        0        0     3774 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sjisprober.py
+-rw-r--r--   0        0        0    12485 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/universaldetector.py
+-rw-r--r--   0        0        0     2766 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/utf8prober.py
+-rw-r--r--   0        0        0      242 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/version.py
+-rw-r--r--   0        0        0      239 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/__init__.py
+-rw-r--r--   0        0        0     2522 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansi.py
+-rw-r--r--   0        0        0    10517 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansitowin32.py
+-rw-r--r--   0        0        0     1915 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/initialise.py
+-rw-r--r--   0        0        0     5404 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/win32.py
+-rw-r--r--   0        0        0     6438 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/winterm.py
+-rw-r--r--   0        0        0    16915 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/contextlib2.py
+-rw-r--r--   0        0        0      581 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/__init__.py
+-rw-r--r--   0        0        0      274 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/__init__.py
+-rw-r--r--   0        0        0      971 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/misc.py
+-rw-r--r--   0        0        0    25707 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/shutil.py
+-rw-r--r--   0        0        0     2617 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.cfg
+-rw-r--r--   0        0        0    26854 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.py
+-rw-r--r--   0        0        0    92628 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/tarfile.py
+-rw-r--r--   0        0        0    41408 2022-07-14 16:31:21.834360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/compat.py
+-rw-r--r--   0        0        0    51059 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/database.py
+-rw-r--r--   0        0        0    21066 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/index.py
+-rw-r--r--   0        0        0    52100 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/locators.py
+-rw-r--r--   0        0        0    14811 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/manifest.py
+-rw-r--r--   0        0        0     4387 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/markers.py
+-rw-r--r--   0        0        0    38962 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/metadata.py
+-rw-r--r--   0        0        0    10766 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/resources.py
+-rw-r--r--   0        0        0    17180 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py
+-rw-r--r--   0        0        0    96768 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/t32.exe
+-rw-r--r--   0        0        0   105984 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/t64.exe
+-rw-r--r--   0        0        0    59845 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/util.py
+-rw-r--r--   0        0        0    23391 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/version.py
+-rw-r--r--   0        0        0    90112 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/w32.exe
+-rw-r--r--   0        0        0    99840 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/w64.exe
+-rw-r--r--   0        0        0    41144 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/wheel.py
+-rw-r--r--   0        0        0    43628 2022-07-14 16:31:21.838360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distro.py
+-rw-r--r--   0        0        0     1160 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/__init__.py
+-rw-r--r--   0        0        0    16728 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_ihatexml.py
+-rw-r--r--   0        0        0    32353 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_inputstream.py
+-rw-r--r--   0        0        0    77040 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_tokenizer.py
+-rw-r--r--   0        0        0      109 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/__init__.py
+-rw-r--r--   0        0        0     1013 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/_base.py
+-rw-r--r--   0        0        0     1775 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/py.py
+-rw-r--r--   0        0        0     4931 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_utils.py
+-rw-r--r--   0        0        0    83464 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/constants.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/__init__.py
+-rw-r--r--   0        0        0      919 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/alphabeticalattributes.py
+-rw-r--r--   0        0        0      286 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/base.py
+-rw-r--r--   0        0        0     2945 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/inject_meta_charset.py
+-rw-r--r--   0        0        0     3643 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/lint.py
+-rw-r--r--   0        0        0    10588 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/optionaltags.py
+-rw-r--r--   0        0        0    26897 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/sanitizer.py
+-rw-r--r--   0        0        0     1214 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/whitespace.py
+-rw-r--r--   0        0        0   117186 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/html5parser.py
+-rw-r--r--   0        0        0    15759 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/serializer.py
+-rw-r--r--   0        0        0      679 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/__init__.py
+-rw-r--r--   0        0        0     1715 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/genshi.py
+-rw-r--r--   0        0        0     1776 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/sax.py
+-rw-r--r--   0        0        0     3592 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/__init__.py
+-rw-r--r--   0        0        0    14565 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/base.py
+-rw-r--r--   0        0        0     8925 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/dom.py
+-rw-r--r--   0        0        0    12836 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree.py
+-rw-r--r--   0        0        0    14766 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree_lxml.py
+-rw-r--r--   0        0        0     5719 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/__init__.py
+-rw-r--r--   0        0        0     7476 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/base.py
+-rw-r--r--   0        0        0     1413 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/dom.py
+-rw-r--r--   0        0        0     4551 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree.py
+-rw-r--r--   0        0        0     6357 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree_lxml.py
+-rw-r--r--   0        0        0     2309 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/genshi.py
+-rw-r--r--   0        0        0       58 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/__init__.py
+-rw-r--r--   0        0        0     3299 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/codec.py
+-rw-r--r--   0        0        0      232 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/compat.py
+-rw-r--r--   0        0        0    11951 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/core.py
+-rw-r--r--   0        0        0    42350 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/idnadata.py
+-rw-r--r--   0        0        0     1749 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/intranges.py
+-rw-r--r--   0        0        0       22 2022-07-14 16:31:21.842360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/package_data.py
+-rw-r--r--   0        0        0   202084 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/uts46data.py
+-rw-r--r--   0        0        0    79875 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/ipaddress.py
+-rw-r--r--   0        0        0     1118 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/__init__.py
+-rw-r--r--   0        0        0       20 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/_version.py
+-rw-r--r--   0        0        0     1081 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/exceptions.py
+-rw-r--r--   0        0        0     6034 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/ext.py
+-rw-r--r--   0        0        0    37133 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/fallback.py
+-rw-r--r--   0        0        0      726 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/__about__.py
+-rw-r--r--   0        0        0      562 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/__init__.py
+-rw-r--r--   0        0        0     1128 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_compat.py
+-rw-r--r--   0        0        0     2022 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_structures.py
+-rw-r--r--   0        0        0     1824 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_typing.py
+-rw-r--r--   0        0        0     9472 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/markers.py
+-rw-r--r--   0        0        0     5110 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/requirements.py
+-rw-r--r--   0        0        0    32208 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/specifiers.py
+-rw-r--r--   0        0        0    29561 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/tags.py
+-rw-r--r--   0        0        0     4385 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/utils.py
+-rw-r--r--   0        0        0    15974 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/version.py
+-rw-r--r--   0        0        0      129 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/__init__.py
+-rw-r--r--   0        0        0     8438 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/_in_process.py
+-rw-r--r--   0        0        0     3335 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/build.py
+-rw-r--r--   0        0        0     5961 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/check.py
+-rw-r--r--   0        0        0     4098 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/colorlog.py
+-rw-r--r--   0        0        0      780 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/compat.py
+-rw-r--r--   0        0        0     1129 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/dirtools.py
+-rw-r--r--   0        0        0     6041 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/envbuild.py
+-rw-r--r--   0        0        0     2463 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/meta.py
+-rw-r--r--   0        0        0    11290 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/wrappers.py
+-rw-r--r--   0        0        0   108277 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/__init__.py
+-rw-r--r--   0        0        0      562 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/py31compat.py
+-rw-r--r--   0        0        0     4857 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/__init__.py
+-rw-r--r--   0        0        0     2854 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/bar.py
+-rw-r--r--   0        0        0     1372 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/counter.py
+-rw-r--r--   0        0        0     1380 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/spinner.py
+-rw-r--r--   0        0        0   273394 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pyparsing.py
+-rw-r--r--   0        0        0     4465 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/__init__.py
+-rw-r--r--   0        0        0      441 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/__version__.py
+-rw-r--r--   0        0        0     1096 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/_internal_utils.py
+-rw-r--r--   0        0        0    21548 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/adapters.py
+-rw-r--r--   0        0        0     6496 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/api.py
+-rw-r--r--   0        0        0    10207 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/auth.py
+-rw-r--r--   0        0        0      465 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/certs.py
+-rw-r--r--   0        0        0     2045 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/compat.py
+-rw-r--r--   0        0        0    18430 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/cookies.py
+-rw-r--r--   0        0        0     3173 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/exceptions.py
+-rw-r--r--   0        0        0     3578 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/help.py
+-rw-r--r--   0        0        0      757 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/hooks.py
+-rw-r--r--   0        0        0    34373 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/models.py
+-rw-r--r--   0        0        0      695 2022-07-14 16:31:21.846360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/packages.py
+-rw-r--r--   0        0        0    30135 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/sessions.py
+-rw-r--r--   0        0        0     4188 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/status_codes.py
+-rw-r--r--   0        0        0     3005 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/structures.py
+-rw-r--r--   0        0        0    30355 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/utils.py
+-rw-r--r--   0        0        0      537 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/__init__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/compat/__init__.py
+-rw-r--r--   0        0        0      127 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/compat/collections_abc.py
+-rw-r--r--   0        0        0     5091 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/providers.py
+-rw-r--r--   0        0        0     1364 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/reporters.py
+-rw-r--r--   0        0        0    16538 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/resolvers.py
+-rw-r--r--   0        0        0     4408 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/structs.py
+-rw-r--r--   0        0        0     9972 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/retrying.py
+-rw-r--r--   0        0        0    34159 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/six.py
+-rw-r--r--   0        0        0      747 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/__init__.py
+-rw-r--r--   0        0        0    38954 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/decoder.py
+-rw-r--r--   0        0        0     9964 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/encoder.py
+-rw-r--r--   0        0        0      378 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/ordered.py
+-rw-r--r--   0        0        0      701 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/tz.py
+-rw-r--r--   0        0        0     2763 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/__init__.py
+-rw-r--r--   0        0        0    10811 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_collections.py
+-rw-r--r--   0        0        0       63 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_version.py
+-rw-r--r--   0        0        0    18489 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connection.py
+-rw-r--r--   0        0        0    37133 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connectionpool.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/__init__.py
+-rw-r--r--   0        0        0      957 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_appengine_environ.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/__init__.py
+-rw-r--r--   0        0        0    17649 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/bindings.py
+-rw-r--r--   0        0        0    13908 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/low_level.py
+-rw-r--r--   0        0        0    11034 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/appengine.py
+-rw-r--r--   0        0        0     4160 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/ntlmpool.py
+-rw-r--r--   0        0        0    16795 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/pyopenssl.py
+-rw-r--r--   0        0        0    34303 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/securetransport.py
+-rw-r--r--   0        0        0     7097 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/socks.py
+-rw-r--r--   0        0        0     7810 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/exceptions.py
+-rw-r--r--   0        0        0     8579 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/fields.py
+-rw-r--r--   0        0        0     2440 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/filepost.py
+-rw-r--r--   0        0        0      108 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/__init__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/__init__.py
+-rw-r--r--   0        0        0     1417 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/makefile.py
+-rw-r--r--   0        0        0    32536 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/six.py
+-rw-r--r--   0        0        0      757 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/__init__.py
+-rw-r--r--   0        0        0     5696 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/_implementation.py
+-rw-r--r--   0        0        0    19763 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/poolmanager.py
+-rw-r--r--   0        0        0     5985 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/request.py
+-rw-r--r--   0        0        0    28203 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/response.py
+-rw-r--r--   0        0        0     1155 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/__init__.py
+-rw-r--r--   0        0        0     4922 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/connection.py
+-rw-r--r--   0        0        0     1604 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/proxy.py
+-rw-r--r--   0        0        0      498 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/queue.py
+-rw-r--r--   0        0        0     4123 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/request.py
+-rw-r--r--   0        0        0     3510 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/response.py
+-rw-r--r--   0        0        0    21366 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/retry.py
+-rw-r--r--   0        0        0    16281 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssl_.py
+-rw-r--r--   0        0        0     6932 2022-07-14 16:31:21.850360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssltransport.py
+-rw-r--r--   0        0        0    10003 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/timeout.py
+-rw-r--r--   0        0        0    13981 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/url.py
+-rw-r--r--   0        0        0     5404 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/wait.py
+-rw-r--r--   0        0        0      437 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/vendor.txt
+-rw-r--r--   0        0        0    10579 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/__init__.py
+-rw-r--r--   0        0        0     8979 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/labels.py
+-rw-r--r--   0        0        0     1305 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/mklabels.py
+-rw-r--r--   0        0        0     6563 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/tests.py
+-rw-r--r--   0        0        0     4307 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/x_user_defined.py
+-rw-r--r--   0        0        0      121 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/.layout.json
+-rwxr-xr-x   0        0        0      220 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/.prefix/bin/easy_install
+-rwxr-xr-x   0        0        0      220 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/.prefix/bin/easy_install-3.8
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/__init__.py
+-rw-r--r--   0        0        0      282 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/easy_install.py
+-rw-r--r--   0        0        0   109513 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/__init__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/__init__.py
+-rw-r--r--   0        0        0    24701 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/appdirs.py
+-rw-r--r--   0        0        0      720 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__about__.py
+-rw-r--r--   0        0        0      513 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__init__.py
+-rw-r--r--   0        0        0      860 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_compat.py
+-rw-r--r--   0        0        0     1416 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_structures.py
+-rw-r--r--   0        0        0     8769 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/markers.py
+-rw-r--r--   0        0        0     5044 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/requirements.py
+-rw-r--r--   0        0        0    28025 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/specifiers.py
+-rw-r--r--   0        0        0      421 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/utils.py
+-rw-r--r--   0        0        0    11556 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/version.py
+-rw-r--r--   0        0        0   232055 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/pyparsing.py
+-rw-r--r--   0        0        0    30098 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/six.py
+-rw-r--r--   0        0        0     2498 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/extern/__init__.py
+-rw-r--r--   0        0        0      558 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/py31compat.py
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1078 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/LICENSE
+-rw-r--r--   0        0        0     3745 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/WHEEL
+-rw-r--r--   0        0        0      239 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/dependency_links.txt
+-rw-r--r--   0        0        0     3206 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/entry_points.txt
+-rw-r--r--   0        0        0       38 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/top_level.txt
+-rw-r--r--   0        0        0        1 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/zip-safe
+-rw-r--r--   0        0        0     8157 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/__init__.py
+-rw-r--r--   0        0        0      218 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_deprecation_warning.py
+-rw-r--r--   0        0        0     2223 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_imp.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/__init__.py
+-rw-r--r--   0        0        0    15130 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/ordered_set.py
+-rw-r--r--   0        0        0      744 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__about__.py
+-rw-r--r--   0        0        0      562 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__init__.py
+-rw-r--r--   0        0        0      865 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_compat.py
+-rw-r--r--   0        0        0     1416 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_structures.py
+-rw-r--r--   0        0        0     8780 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/markers.py
+-rw-r--r--   0        0        0     5419 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/requirements.py
+-rw-r--r--   0        0        0    27778 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/specifiers.py
+-rw-r--r--   0        0        0    12933 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/tags.py
+-rw-r--r--   0        0        0     1520 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/utils.py
+-rw-r--r--   0        0        0    11978 2022-07-14 16:31:21.854360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/version.py
+-rw-r--r--   0        0        0   232055 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/pyparsing.py
+-rw-r--r--   0        0        0    30098 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/six.py
+-rw-r--r--   0        0        0     6730 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/archive_util.py
+-rw-r--r--   0        0        0    10153 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/build_meta.py
+-rw-r--r--   0        0        0    65536 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli-32.exe
+-rw-r--r--   0        0        0    74752 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli-64.exe
+-rw-r--r--   0        0        0    65536 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli.exe
+-rw-r--r--   0        0        0      710 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/__init__.py
+-rw-r--r--   0        0        0     2736 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/alias.py
+-rw-r--r--   0        0        0    18880 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_egg.py
+-rw-r--r--   0        0        0     1508 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_rpm.py
+-rw-r--r--   0        0        0      637 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_wininst.py
+-rw-r--r--   0        0        0     4632 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_clib.py
+-rw-r--r--   0        0        0    13284 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_ext.py
+-rw-r--r--   0        0        0    10036 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_py.py
+-rw-r--r--   0        0        0     8854 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/develop.py
+-rw-r--r--   0        0        0      960 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/dist_info.py
+-rw-r--r--   0        0        0    90093 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/easy_install.py
+-rw-r--r--   0        0        0    27330 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/egg_info.py
+-rw-r--r--   0        0        0     4832 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install.py
+-rw-r--r--   0        0        0     2737 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_egg_info.py
+-rw-r--r--   0        0        0     4034 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_lib.py
+-rw-r--r--   0        0        0     3105 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_scripts.py
+-rw-r--r--   0        0        0      628 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/launcher manifest.xml
+-rw-r--r--   0        0        0     5128 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/py36compat.py
+-rw-r--r--   0        0        0      613 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/register.py
+-rw-r--r--   0        0        0     2419 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/rotate.py
+-rw-r--r--   0        0        0      816 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/saveopts.py
+-rw-r--r--   0        0        0     8363 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/sdist.py
+-rw-r--r--   0        0        0     5359 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/setopt.py
+-rw-r--r--   0        0        0    10328 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/test.py
+-rw-r--r--   0        0        0      607 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/upload.py
+-rw-r--r--   0        0        0     7734 2022-07-14 16:31:21.858360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/upload_docs.py
+-rw-r--r--   0        0        0    21571 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/config.py
+-rw-r--r--   0        0        0      935 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/dep_util.py
+-rw-r--r--   0        0        0     5517 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/depends.py
+-rw-r--r--   0        0        0    51749 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/dist.py
+-rw-r--r--   0        0        0      524 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/errors.py
+-rw-r--r--   0        0        0     1868 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/extension.py
+-rw-r--r--   0        0        0     2514 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/extern/__init__.py
+-rw-r--r--   0        0        0     5084 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/glob.py
+-rw-r--r--   0        0        0    65536 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui-32.exe
+-rw-r--r--   0        0        0    75264 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui-64.exe
+-rw-r--r--   0        0        0    65536 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui.exe
+-rw-r--r--   0        0        0     5881 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/installer.py
+-rw-r--r--   0        0        0      787 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/launch.py
+-rw-r--r--   0        0        0     2140 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/lib2to3_ex.py
+-rw-r--r--   0        0        0     5520 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/monkey.py
+-rw-r--r--   0        0        0    47209 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/msvc.py
+-rw-r--r--   0        0        0     3338 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/namespaces.py
+-rw-r--r--   0        0        0    42090 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/package_index.py
+-rw-r--r--   0        0        0     1625 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py27compat.py
+-rw-r--r--   0        0        0      838 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py31compat.py
+-rw-r--r--   0        0        0     1606 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py33compat.py
+-rw-r--r--   0        0        0      245 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py34compat.py
+-rw-r--r--   0        0        0    15424 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/sandbox.py
+-rw-r--r--   0        0        0      218 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/script (dev).tmpl
+-rw-r--r--   0        0        0      138 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/script.tmpl
+-rw-r--r--   0        0        0     2302 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/site-patch.py
+-rw-r--r--   0        0        0     8815 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/ssl_support.py
+-rw-r--r--   0        0        0     1125 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/unicode_utils.py
+-rw-r--r--   0        0        0      277 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/version.py
+-rw-r--r--   0        0        0     9445 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/wheel.py
+-rw-r--r--   0        0        0      714 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/windows_support.py
+-rw-r--r--   0        0        0       74 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/.layout.json
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/__init__.py
+-rw-r--r--   0        0        0       13 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/constraints.txt
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1252 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/LICENSE
+-rw-r--r--   0        0        0     7142 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/WHEEL
+-rw-r--r--   0        0        0        5 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/top_level.txt
+-rw-r--r--   0        0        0      963 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml/__init__.py
+-rw-r--r--   0        0        0    39064 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml/decoder.py
+-rw-r--r--   0        0        0    10233 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml/encoder.py
+-rw-r--r--   0        0        0      602 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml/ordered.py
+-rw-r--r--   0        0        0      701 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/toml/toml/tz.py
+-rw-r--r--   0        0        0       75 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/.layout.json
+-rwxr-xr-x   0        0        0      198 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/.prefix/bin/wheel
+-rw-r--r--   0        0        0       14 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/constraints.txt
+-rw-r--r--   0        0        0        4 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/INSTALLER
+-rw-r--r--   0        0        0     1125 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/LICENSE.txt
+-rw-r--r--   0        0        0     2328 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/METADATA
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/REQUESTED
+-rw-r--r--   0        0        0      110 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/WHEEL
+-rw-r--r--   0        0        0      108 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/entry_points.txt
+-rw-r--r--   0        0        0        6 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/top_level.txt
+-rw-r--r--   0        0        0       23 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/__init__.py
+-rw-r--r--   0        0        0      417 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/__main__.py
+-rw-r--r--   0        0        0    19075 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/bdist_wheel.py
+-rw-r--r--   0        0        0     2572 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/__init__.py
+-rw-r--r--   0        0        0     9498 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/convert.py
+-rw-r--r--   0        0        0     3364 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/pack.py
+-rw-r--r--   0        0        0      673 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/unpack.py
+-rw-r--r--   0        0        0    15930 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/macosx_libfile.py
+-rw-r--r--   0        0        0     4344 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/metadata.py
+-rw-r--r--   0        0        0     1257 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/pkginfo.py
+-rw-r--r--   0        0        0      938 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/util.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/__init__.py
+-rw-r--r--   0        0        0        0 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/packaging/__init__.py
+-rw-r--r--   0        0        0     1812 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/packaging/_typing.py
+-rw-r--r--   0        0        0    29560 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/packaging/tags.py
+-rw-r--r--   0        0        0     7574 2022-07-14 16:31:21.862360 pex-2.1.99/pex/vendor/_vendored/wheel/wheel/wheelfile.py
+-rw-r--r--   0        0        0      430 2022-07-14 16:31:21.862360 pex-2.1.99/pex/venv/README.md
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.862360 pex-2.1.99/pex/venv/__init__.py
+-rw-r--r--   0        0        0      368 2022-07-14 16:31:21.862360 pex-2.1.99/pex/venv/bin_path.py
+-rw-r--r--   0        0        0      376 2022-07-14 16:31:21.862360 pex-2.1.99/pex/venv/install_scope.py
+-rw-r--r--   0        0        0    25905 2022-07-14 16:31:21.866360 pex-2.1.99/pex/venv/pex.py
+-rw-r--r--   0        0        0    12533 2022-07-14 16:31:21.866360 pex-2.1.99/pex/venv/virtualenv.py
+-rw-r--r--   0        0        0   106996 2022-07-14 16:31:21.866360 pex-2.1.99/pex/venv/virtualenv_16.7.12_py
+-rw-r--r--   0        0        0      155 2022-07-14 16:31:21.866360 pex-2.1.99/pex/version.py
+-rw-r--r--   0        0        0     2405 2022-07-14 16:31:21.866360 pex-2.1.99/pyproject.toml
+-rwxr-xr-x   0        0        0      286 2022-07-14 16:31:21.866360 pex-2.1.99/scripts/embed_virtualenv.sh
+-rwxr-xr-x   0        0        0      368 2022-07-14 16:31:21.866360 pex-2.1.99/scripts/format.sh
+-rwxr-xr-x   0        0        0     5429 2022-07-14 16:31:21.866360 pex-2.1.99/scripts/package.py
+-rwxr-xr-x   0        0        0      657 2022-07-14 16:31:21.866360 pex-2.1.99/scripts/typecheck.sh
+-rw-r--r--   0        0        0     5261 2022-07-14 16:31:21.866360 pex-2.1.99/tests/bin/test_sh_boot.py
+-rw-r--r--   0        0        0     1822 2022-07-14 16:31:21.866360 pex-2.1.99/tests/build_system/test_pep_517.py
+-rw-r--r--   0        0        0     2234 2022-07-14 16:31:21.866360 pex-2.1.99/tests/build_system/test_pep_518.py
+-rw-r--r--   0        0        0     2302 2022-07-14 16:31:21.866360 pex-2.1.99/tests/commands/test_command.py
+-rw-r--r--   0        0        0     1161 2022-07-14 16:31:21.866360 pex-2.1.99/tests/conftest.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.866360 pex-2.1.99/tests/data/__init__.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.866360 pex-2.1.99/tests/data/platforms/__init__.py
+-rw-r--r--   0        0        0    27259 2022-07-14 16:31:21.866360 pex-2.1.99/tests/data/platforms/macosx_10_13_x86_64-cp-36-m.tags.txt
+-rw-r--r--   0        0        0    25660 2022-07-14 16:31:21.866360 pex-2.1.99/tests/example_packages/MarkupSafe-1.0-cp27-cp27mu-linux_x86_64.whl
+-rw-r--r--   0        0        0    32074 2022-07-14 16:31:21.866360 pex-2.1.99/tests/example_packages/PyAthena-1.11.5-py2.py3-none-any.whl
+-rw-r--r--   0        0        0    37477 2022-07-14 16:31:21.866360 pex-2.1.99/tests/example_packages/PyAthena-1.9.0-py2.py3-none-any.whl
+-rw-r--r--   0        0        0   983623 2022-07-14 16:31:21.870360 pex-2.1.99/tests/example_packages/aws_cfn_bootstrap-1.4-py2-none-any.whl
+-rw-r--r--   0        0        0    56975 2022-07-14 16:31:21.870360 pex-2.1.99/tests/example_packages/pyparsing-2.1.10-py2.py3-none-any.whl
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/__init__.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/build_system/__init__.py
+-rw-r--r--   0        0        0     1350 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/build_system/test_pep_517.py
+-rw-r--r--   0        0        0     1756 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/build_system/test_pep_518.py
+-rw-r--r--   0        0        0     5654 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_export.py
+-rw-r--r--   0        0        0     3343 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_interpreter_inspect.py
+-rw-r--r--   0        0        0     5373 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1413.py
+-rw-r--r--   0        0        0     1288 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1665.py
+-rw-r--r--   0        0        0     2616 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1667.py
+-rw-r--r--   0        0        0     2204 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1688.py
+-rw-r--r--   0        0        0     4665 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1711.py
+-rw-r--r--   0        0        0     3200 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1734.py
+-rw-r--r--   0        0        0     2691 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1741.py
+-rw-r--r--   0        0        0     2417 2022-07-14 16:31:21.870360 pex-2.1.99/tests/integration/cli/commands/test_issue_1801.py
+-rw-r--r--   0        0        0     8278 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/cli/commands/test_issue_1821.py
+-rw-r--r--   0        0        0     4016 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/cli/commands/test_local_project_lock.py
+-rw-r--r--   0        0        0    75069 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/cli/commands/test_lock.py
+-rw-r--r--   0        0        0    11683 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/cli/commands/test_lock_resolve_auth.py
+-rw-r--r--   0        0        0     7407 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/cli/commands/test_vcs_lock.py
+-rw-r--r--   0        0        0     5876 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/conftest.py
+-rw-r--r--   0        0        0     2537 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_downloads.py
+-rw-r--r--   0        0        0     2011 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_executuon_mode_venv.py
+-rw-r--r--   0        0        0    62420 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_integration.py
+-rw-r--r--   0        0        0    17225 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_interpreter_selection.py
+-rw-r--r--   0        0        0      649 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1017.py
+-rw-r--r--   0        0        0     2554 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1018.py
+-rw-r--r--   0        0        0     2132 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1025.py
+-rw-r--r--   0        0        0     3090 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1031.py
+-rw-r--r--   0        0        0      886 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1179.py
+-rw-r--r--   0        0        0      607 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1201.py
+-rw-r--r--   0        0        0     2291 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1202.py
+-rw-r--r--   0        0        0     2200 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1218.py
+-rw-r--r--   0        0        0     2922 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1225.py
+-rw-r--r--   0        0        0     6909 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1232.py
+-rw-r--r--   0        0        0     1608 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1302.py
+-rw-r--r--   0        0        0      561 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1316.py
+-rw-r--r--   0        0        0      647 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1336.py
+-rw-r--r--   0        0        0     3974 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1422.py
+-rw-r--r--   0        0        0     1151 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1447.py
+-rw-r--r--   0        0        0     1404 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1479.py
+-rw-r--r--   0        0        0     3219 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1520.py
+-rw-r--r--   0        0        0     1148 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1537.py
+-rw-r--r--   0        0        0     1252 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1550.py
+-rw-r--r--   0        0        0     2683 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1560.py
+-rw-r--r--   0        0        0     4902 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1597.py
+-rw-r--r--   0        0        0     1216 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1598.py
+-rw-r--r--   0        0        0     5884 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1656.py
+-rw-r--r--   0        0        0     1640 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1683.py
+-rw-r--r--   0        0        0     2133 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1726.py
+-rw-r--r--   0        0        0     1441 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1730.py
+-rw-r--r--   0        0        0     3130 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1802.py
+-rw-r--r--   0        0        0     3405 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1809.py
+-rw-r--r--   0        0        0     1561 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1817.py
+-rw-r--r--   0        0        0     4234 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_1825.py
+-rw-r--r--   0        0        0      988 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_434.py
+-rw-r--r--   0        0        0     2162 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_539.py
+-rw-r--r--   0        0        0      715 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_598.py
+-rw-r--r--   0        0        0     1319 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_661.py
+-rw-r--r--   0        0        0     2950 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_729.py
+-rw-r--r--   0        0        0     1341 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_736.py
+-rw-r--r--   0        0        0     2314 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_745.py
+-rw-r--r--   0        0        0     1849 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_749.py
+-rw-r--r--   0        0        0     1750 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_898.py
+-rw-r--r--   0        0        0     1772 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_899.py
+-rw-r--r--   0        0        0      921 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_940.py
+-rw-r--r--   0        0        0     2046 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_issue_996.py
+-rw-r--r--   0        0        0     1862 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_layout.py
+-rw-r--r--   0        0        0    16860 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_lock_resolver.py
+-rw-r--r--   0        0        0     5778 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_locked_resolve.py
+-rw-r--r--   0        0        0    15297 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_pex_bootstrapper.py
+-rw-r--r--   0        0        0     3876 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_pex_entry_points.py
+-rw-r--r--   0        0        0     4637 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_pex_import.py
+-rw-r--r--   0        0        0     7478 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_reexec.py
+-rw-r--r--   0        0        0     6086 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_reproducible.py
+-rw-r--r--   0        0        0     4772 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_setproctitle.py
+-rw-r--r--   0        0        0     6306 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_sh_boot.py
+-rw-r--r--   0        0        0     9535 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_shebang_length_limit.py
+-rw-r--r--   0        0        0     1576 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/test_variables.py
+-rw-r--r--   0        0        0     8716 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/tools/commands/test_venv.py
+-rw-r--r--   0        0        0     2545 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_issue_1630.py
+-rw-r--r--   0        0        0     5866 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_issue_1637.py
+-rw-r--r--   0        0        0     2331 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_issue_1641.py
+-rw-r--r--   0        0        0     2222 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_issue_1668.py
+-rw-r--r--   0        0        0     4550 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_issue_1745.py
+-rw-r--r--   0        0        0     3432 2022-07-14 16:31:21.874360 pex-2.1.99/tests/integration/venv_ITs/test_virtualenv.py
+-rw-r--r--   0        0        0     3525 2022-07-14 16:31:21.874360 pex-2.1.99/tests/pip/test_tailer.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.874360 pex-2.1.99/tests/resolve/__init__.py
+-rw-r--r--   0        0        0      276 2022-07-14 16:31:21.874360 pex-2.1.99/tests/resolve/conftest.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.874360 pex-2.1.99/tests/resolve/lockfile/__init__.py
+-rw-r--r--   0        0        0     5981 2022-07-14 16:31:21.874360 pex-2.1.99/tests/resolve/lockfile/test_download_manager.py
+-rw-r--r--   0        0        0    18787 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/lockfile/test_json_codec.py
+-rw-r--r--   0        0        0     3714 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/lockfile/test_lockfile.py
+-rw-r--r--   0        0        0    31051 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/test_locked_resolve.py
+-rw-r--r--   0        0        0     2636 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/test_path_mappings.py
+-rw-r--r--   0        0        0    10589 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/test_pex_repository_resolver.py
+-rw-r--r--   0        0        0     5087 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/test_resolver_options.py
+-rw-r--r--   0        0        0    14237 2022-07-14 16:31:21.878360 pex-2.1.99/tests/resolve/test_target_options.py
+-rw-r--r--   0        0        0     7030 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_bdist_pex.py
+-rw-r--r--   0        0        0    13563 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_common.py
+-rw-r--r--   0        0        0     1683 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_compatibility.py
+-rw-r--r--   0        0        0     3007 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_compiler.py
+-rw-r--r--   0        0        0    11640 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_dist_metadata.py
+-rw-r--r--   0        0        0     4000 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_enum.py
+-rw-r--r--   0        0        0    17201 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_environment.py
+-rw-r--r--   0        0        0     3708 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_execution_mode.py
+-rw-r--r--   0        0        0     3575 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_executor.py
+-rw-r--r--   0        0        0     1680 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_fetcher.py
+-rw-r--r--   0        0        0     3429 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_finders.py
+-rw-r--r--   0        0        0     2049 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_hashing.py
+-rw-r--r--   0        0        0     2199 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_inherits_path_option.py
+-rw-r--r--   0        0        0    19052 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_interpreter.py
+-rw-r--r--   0        0        0     3500 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_interpreter_constraints.py
+-rw-r--r--   0        0        0     3433 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_jobs.py
+-rw-r--r--   0        0        0     1898 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_packaging.py
+-rw-r--r--   0        0        0     3123 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pep_376.py
+-rw-r--r--   0        0        0     1933 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pep_425.py
+-rw-r--r--   0        0        0     3472 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pep_508.py
+-rw-r--r--   0        0        0    31154 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex.py
+-rw-r--r--   0        0        0     8003 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex_binary.py
+-rw-r--r--   0        0        0    10749 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex_bootstrapper.py
+-rw-r--r--   0        0        0    17103 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex_builder.py
+-rw-r--r--   0        0        0     5344 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex_info.py
+-rw-r--r--   0        0        0     2732 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pex_warnings.py
+-rw-r--r--   0        0        0     9165 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_pip.py
+-rw-r--r--   0        0        0     4916 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_platform.py
+-rw-r--r--   0        0        0    19681 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_requirements.py
+-rw-r--r--   0        0        0    22891 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_resolver.py
+-rw-r--r--   0        0        0      572 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_sorted_tuple.py
+-rw-r--r--   0        0        0     8209 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_targets.py
+-rw-r--r--   0        0        0     2347 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_third_party.py
+-rw-r--r--   0        0        0     7059 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_util.py
+-rw-r--r--   0        0        0     8139 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_variables.py
+-rw-r--r--   0        0        0     2243 2022-07-14 16:31:21.878360 pex-2.1.99/tests/test_vendor.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.878360 pex-2.1.99/tests/tools/__init__.py
+-rw-r--r--   0        0        0      131 2022-07-14 16:31:21.878360 pex-2.1.99/tests/tools/commands/__init__.py
+-rw-r--r--   0        0        0     5641 2022-07-14 16:31:21.878360 pex-2.1.99/tests/tools/commands/test_interpreter_command.py
+-rw-r--r--   0        0        0     9136 2022-07-14 16:31:21.878360 pex-2.1.99/tests/tools/commands/test_repository.py
+-rw-r--r--   0        0        0    27025 2022-07-14 16:31:21.878360 pex-2.1.99/tests/tools/commands/test_venv.py
+-rw-r--r--   0        0        0     6260 2022-07-14 16:31:21.878360 pex-2.1.99/tox.ini
+-rw-r--r--   0        0        0     7266 1970-01-01 00:00:00.000000 pex-2.1.99/PKG-INFO
```

### Comparing `pex-2.1.98/.github/workflows/ci.yml` & `pex-2.1.99/.github/workflows/ci.yml`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/.github/workflows/release.yml` & `pex-2.1.99/.github/workflows/release.yml`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/CHANGES.rst` & `pex-2.1.99/CHANGES.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,22 +1,32 @@
 Release Notes
 =============
 
-2.1.98
+2.1.99
 ------
 
-This releases fixes regressions in foreign `--platform` handling and
-artifact downloading introduced by #1787 in Pex 2.1.91.
+This release fixes a concurrency bug in the ``pex --lock ...`` artifact
+downloading.
+
+* Fix ``pex --lock ...`` concurrent download errors. (#1854)
+  `PR #1854 <https://github.com/pantsbuild/pex/pull/1854>`_
+
+2.1.98
+------
 
-In addition, PEXes can now be used as `sys.path` entries. Once on the 
-`sys.path`, via `PYTHONPATH` or other means, the code in the PEX can be
-made importable by first importing `__pex__` either as its own
-stand-alone import statement; e.g.: `import __pex__; import psutil` or
+This releases fixes regressions in foreign ``--platform`` handling and
+artifact downloading introduced by #1787 in Pex 2.1.91 and #1811 in
+2.1.93.
+
+In addition, PEXes can now be used as ``sys.path`` entries. Once on the 
+``sys.path``, via ``PYTHONPATH`` or other means, the code in the PEX can
+be made importable by first importing ``__pex__`` either as its own
+stand-alone import statement; e.g.: ``import __pex__; import psutil`` or
 as a prefix of the code to import from the PEX; e.g.:
-`from __pex__ import psutil`.
+``from __pex__ import psutil``.
 
 * Tags should be patched for --platform. (#1846)
   `PR #1846 <https://github.com/pantsbuild/pex/pull/1846>`_
 
 * Add support for importing from PEXes. (#1845) 
   `PR #1845 <https://github.com/pantsbuild/pex/pull/1845>`_
```

### Comparing `pex-2.1.98/LICENSE` & `pex-2.1.99/LICENSE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/README.rst` & `pex-2.1.99/README.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/RELEASE.rst` & `pex-2.1.99/RELEASE.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docker/base/Dockerfile` & `pex-2.1.99/docker/base/Dockerfile`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/Makefile` & `pex-2.1.99/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/_ext/vars.py` & `pex-2.1.99/docs/_ext/vars.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/buildingpex.rst` & `pex-2.1.99/docs/buildingpex.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/conf.py` & `pex-2.1.99/docs/conf.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/index.rst` & `pex-2.1.99/docs/index.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/recipes.rst` & `pex-2.1.99/docs/recipes.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/docs/whatispex.rst` & `pex-2.1.99/docs/whatispex.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/dtox.sh` & `pex-2.1.99/dtox.sh`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/mypy.ini` & `pex-2.1.99/mypy.ini`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/argparse.py` & `pex-2.1.99/pex/argparse.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/auth.py` & `pex-2.1.99/pex/auth.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/bin/pex.py` & `pex-2.1.99/pex/bin/pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/bin/sh_boot.py` & `pex-2.1.99/pex/bin/sh_boot.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/bootstrap.py` & `pex-2.1.99/pex/bootstrap.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/build_system/pep_517.py` & `pex-2.1.99/pex/build_system/pep_517.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/build_system/pep_518.py` & `pex-2.1.99/pex/build_system/pep_518.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/build_system/testing.py` & `pex-2.1.99/pex/build_system/testing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/cli/command.py` & `pex-2.1.99/pex/cli/command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/cli/commands/interpreter.py` & `pex-2.1.99/pex/cli/commands/interpreter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/cli/commands/lock.py` & `pex-2.1.99/pex/cli/commands/lock.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/cli/pex.py` & `pex-2.1.99/pex/cli/pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/cli/testing.py` & `pex-2.1.99/pex/cli/testing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/commands/command.py` & `pex-2.1.99/pex/commands/command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/common.py` & `pex-2.1.99/pex/common.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/compatibility.py` & `pex-2.1.99/pex/compatibility.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/compiler.py` & `pex-2.1.99/pex/compiler.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/dist_metadata.py` & `pex-2.1.99/pex/dist_metadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/distutils/commands/bdist_pex.py` & `pex-2.1.99/pex/distutils/commands/bdist_pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/enum.py` & `pex-2.1.99/pex/enum.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/environment.py` & `pex-2.1.99/pex/environment.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/executor.py` & `pex-2.1.99/pex/executor.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/fetcher.py` & `pex-2.1.99/pex/fetcher.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/finders.py` & `pex-2.1.99/pex/finders.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/fingerprinted_distribution.py` & `pex-2.1.99/pex/fingerprinted_distribution.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/hashing.py` & `pex-2.1.99/pex/hashing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/inherit_path.py` & `pex-2.1.99/pex/inherit_path.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/interpreter.py` & `pex-2.1.99/pex/interpreter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/interpreter_constraints.py` & `pex-2.1.99/pex/interpreter_constraints.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/jobs.py` & `pex-2.1.99/pex/jobs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/layout.py` & `pex-2.1.99/pex/layout.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/network_configuration.py` & `pex-2.1.99/pex/network_configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/orderedset.py` & `pex-2.1.99/pex/orderedset.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pep_376.py` & `pex-2.1.99/pex/pep_376.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # Licensed under the Apache License, Version 2.0 (see LICENSE).
 
 from __future__ import absolute_import
 
 import base64
 import csv
 import errno
-import fileinput
 import hashlib
 import itertools
 import json
 import os
 import shutil
 from contextlib import closing
 from fileinput import FileInput
@@ -595,15 +594,15 @@
                 # line of console_script shim ~code defined in
                 # pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py on line 41:
                 # https://github.com/pantsbuild/pex/blob/196b4cd5b8dd4b4af2586460530e9a777262be7d/pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py#L41
                 scripts[script_path] = b"# -*- coding: utf-8 -*-"
         if not scripts:
             return
 
-        with closing(fileinput.input(files=scripts.keys(), inplace=True, mode="rb")) as script_fi:
+        with closing(FileInput(files=scripts.keys(), inplace=True, mode="rb")) as script_fi:
             first_non_shebang_line = None  # type: Optional[bytes]
             for line in script_fi:
                 buffer = get_stdout_bytes_buffer()
                 if script_fi.isfirstline():
                     first_non_shebang_line = scripts[script_fi.filename()]
                     # Ensure python shebangs are reproducible. The only place these can be used is
                     # in venv mode PEXes where the `#!python` placeholder shebang will be re-written
```

### Comparing `pex-2.1.98/pex/pep_425.py` & `pex-2.1.99/pex/pep_425.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pep_440.py` & `pex-2.1.99/pex/pep_440.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pep_503.py` & `pex-2.1.99/pex/pep_503.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pep_508.py` & `pex-2.1.99/pex/pep_508.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pex.py` & `pex-2.1.99/pex/pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pex_bootstrapper.py` & `pex-2.1.99/pex/pex_bootstrapper.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pex_builder.py` & `pex-2.1.99/pex/pex_builder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pex_info.py` & `pex-2.1.99/pex/pex_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pex_warnings.py` & `pex-2.1.99/pex/pex_warnings.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/download_observer.py` & `pex-2.1.99/pex/pip/download_observer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/foreign_platform.py` & `pex-2.1.99/pex/pip/foreign_platform.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/foreign_platform_patches.py` & `pex-2.1.99/pex/pip/foreign_platform_patches.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/local_project.py` & `pex-2.1.99/pex/pip/local_project.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/log_analyzer.py` & `pex-2.1.99/pex/pip/log_analyzer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/tailer.py` & `pex-2.1.99/pex/pip/tailer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/tool.py` & `pex-2.1.99/pex/pip/tool.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pip/vcs.py` & `pex-2.1.99/pex/pip/vcs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/platforms.py` & `pex-2.1.99/pex/platforms.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/pyenv.py` & `pex-2.1.99/pex/pyenv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/rank.py` & `pex-2.1.99/pex/rank.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/requirements.py` & `pex-2.1.99/pex/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/configured_resolver.py` & `pex-2.1.99/pex/resolve/configured_resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/downloads.py` & `pex-2.1.99/pex/resolve/downloads.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 import shutil
 
 from pex import hashing
 from pex.common import atomic_directory, safe_mkdir, safe_mkdtemp
 from pex.compatibility import unquote, urlparse
 from pex.hashing import Sha256
 from pex.jobs import Job, Raise, SpawnedJob, execute_parallel
-from pex.pip.tool import PackageIndexConfiguration, get_pip
+from pex.pip.tool import PackageIndexConfiguration, Pip, get_pip
 from pex.resolve import locker
 from pex.resolve.locked_resolve import Artifact, FileArtifact, LockConfiguration, LockStyle
 from pex.resolve.resolved_requirement import Fingerprint, PartialArtifact
 from pex.resolve.resolvers import Resolver
 from pex.result import Error
 from pex.typing import TYPE_CHECKING
 from pex.variables import ENV
@@ -40,14 +40,15 @@
         _DOWNLOADS_DIRS[root_dir] = downloads_dir
     return downloads_dir
 
 
 @attr.s(frozen=True)
 class ArtifactDownloader(object):
     resolver = attr.ib()  # type: Resolver
+    pip = attr.ib(factory=get_pip)  # type: Pip
     package_index_configuration = attr.ib(
         default=PackageIndexConfiguration.create()
     )  # type: PackageIndexConfiguration
 
     @staticmethod
     def _fingerprint_and_move(path):
         # type: (str) -> Fingerprint
@@ -94,15 +95,15 @@
         # observer does just this for universal locks with no target system or requires python
         # restrictions.
         download_observer = locker.patch(
             resolver=self.resolver,
             lock_configuration=LockConfiguration(style=LockStyle.UNIVERSAL),
             download_dir=download_dir,
         )
-        return get_pip().spawn_download_distributions(
+        return self.pip.spawn_download_distributions(
             download_dir=download_dir,
             requirements=[url],
             transitive=False,
             package_index_configuration=self.package_index_configuration,
             observer=download_observer,
         )
```

### Comparing `pex-2.1.98/pex/resolve/lock_resolver.py` & `pex-2.1.99/pex/resolve/lock_resolver.py`

 * *Files 10% similar despite different names*

```diff
@@ -10,17 +10,18 @@
 from multiprocessing.pool import ThreadPool
 
 from pex import resolver
 from pex.auth import PasswordDatabase, PasswordEntry
 from pex.common import FileLockStyle, pluralize
 from pex.compatibility import cpu_count
 from pex.network_configuration import NetworkConfiguration
+from pex.orderedset import OrderedSet
 from pex.pep_503 import ProjectName
 from pex.pip.local_project import digest_local_project
-from pex.pip.tool import PackageIndexConfiguration
+from pex.pip.tool import PackageIndexConfiguration, get_pip
 from pex.pip.vcs import digest_vcs_archive
 from pex.resolve.downloads import ArtifactDownloader
 from pex.resolve.locked_resolve import (
     DownloadableArtifact,
     FileArtifact,
     LocalProjectArtifact,
     VCSArtifact,
@@ -29,20 +30,20 @@
 from pex.resolve.lockfile.model import Lockfile
 from pex.resolve.lockfile.subset import subset
 from pex.resolve.requirement_configuration import RequirementConfiguration
 from pex.resolve.resolver_configuration import ResolverVersion
 from pex.resolve.resolvers import Installed, Resolver
 from pex.resolver import BuildAndInstallRequest, BuildRequest, InstallRequest
 from pex.result import Error, catch, try_
-from pex.targets import Target, Targets
+from pex.targets import Targets
 from pex.tracer import TRACER
 from pex.typing import TYPE_CHECKING
 
 if TYPE_CHECKING:
-    from typing import Dict, Iterable, Mapping, Optional, Sequence, Tuple, Union
+    from typing import Dict, Iterable, Optional, Sequence, Union
 
     from pex.hashing import HintedDigest
 
 
 class FileArtifactDownloadManager(DownloadManager[FileArtifact]):
     def __init__(
         self,
@@ -171,32 +172,29 @@
         )
         if isinstance(source_dir_or_error, Error):
             return source_dir_or_error
         return os.path.basename(source_dir_or_error)
 
 
 def download_artifact(
-    downloadable_artifact_and_target,  # type: Tuple[DownloadableArtifact, Target]
-    file_download_managers_by_target,  # type: Mapping[Target, FileArtifactDownloadManager]
+    downloadable_artifact,  # type: DownloadableArtifact
+    file_download_manager,  # type: FileArtifactDownloadManager
     vcs_download_manager,  # type: VCSArtifactDownloadManager
     local_project_download_manager,  # type: LocalProjectDownloadManager
 ):
     # type: (...) -> Union[DownloadedArtifact, Error]
 
-    downloadable_artifact, target = downloadable_artifact_and_target
-
     if isinstance(downloadable_artifact.artifact, VCSArtifact):
         return catch(
             vcs_download_manager.store,
             downloadable_artifact.artifact,
             downloadable_artifact.pin.project_name,
         )
 
     if isinstance(downloadable_artifact.artifact, FileArtifact):
-        file_download_manager = file_download_managers_by_target[target]
         return catch(
             file_download_manager.store,
             downloadable_artifact.artifact,
             downloadable_artifact.pin.project_name,
         )
 
     return catch(
@@ -247,46 +245,45 @@
             network_configuration=network_configuration,
             build=build,
             use_wheel=use_wheel,
             prefer_older_binary=prefer_older_binary,
             transitive=transitive,
         )
     )
-    target_by_downloadable_artifact = OrderedDict(
-        (downloadable_artifact, resolved_subset.target)
+    downloadable_artifacts = OrderedSet(
+        downloadable_artifact
         for resolved_subset in subset_result.subsets
         for downloadable_artifact in resolved_subset.resolved.downloadable_artifacts
     )
 
     # Since the download managers are stored to via a thread pool, we need to use BSD style locks.
     # These locks are not as portable as POSIX style locks but work with threading unlike POSIX
     # locks which are subject to threading-unaware deadlock detection per the standard. Linux, in
     # fact, implements deadlock detection for POSIX locks; so we can run afoul of false EDEADLCK
     # errors under the right interleaving of processes and threads and download artifact targets.
     file_lock_style = FileLockStyle.BSD
 
-    file_download_managers_by_target = {}
-    package_index_configuration = None  # type: Optional[PackageIndexConfiguration]
-    for downloadable_artifact, target in target_by_downloadable_artifact.items():
-        if target not in file_download_managers_by_target:
-            if package_index_configuration is None:
-                package_index_configuration = PackageIndexConfiguration.create(
-                    resolver_version=resolver_version,
-                    indexes=indexes,
-                    find_links=find_links,
-                    network_configuration=network_configuration,
-                    password_entries=PasswordDatabase.from_netrc().append(password_entries).entries,
-                )
-            file_download_managers_by_target[target] = FileArtifactDownloadManager(
-                file_lock_style=file_lock_style,
-                downloader=ArtifactDownloader(
-                    resolver=resolver,
-                    package_index_configuration=package_index_configuration,
-                ),
-            )
+    # We eagerly initialize a Pip tool for reasons alluded to above, creation of the Pip tool venv
+    # is not thread-safe and this can lead to errors.
+    pip = get_pip()
+
+    file_download_manager = FileArtifactDownloadManager(
+        file_lock_style=file_lock_style,
+        downloader=ArtifactDownloader(
+            resolver=resolver,
+            pip=pip,
+            package_index_configuration=PackageIndexConfiguration.create(
+                resolver_version=resolver_version,
+                indexes=indexes,
+                find_links=find_links,
+                network_configuration=network_configuration,
+                password_entries=PasswordDatabase.from_netrc().append(password_entries).entries,
+            ),
+        ),
+    )
 
     vcs_download_manager = VCSArtifactDownloadManager(
         file_lock_style=file_lock_style,
         indexes=indexes,
         find_links=find_links,
         resolver_version=resolver_version,
         network_configuration=network_configuration,
@@ -297,36 +294,36 @@
 
     local_project_download_manager = LocalProjectDownloadManager(
         file_lock_style=file_lock_style,
         build_requires_resolver=resolver,
     )
 
     max_threads = min(
-        len(target_by_downloadable_artifact) or 1,
+        len(downloadable_artifacts) or 1,
         min(MAX_PARALLEL_DOWNLOADS, 4 * (max_parallel_jobs or cpu_count() or 1)),
     )
     with TRACER.timed(
         "Downloading {url_count} distributions to satisfy {requirement_count} requirements".format(
-            url_count=len(target_by_downloadable_artifact),
+            url_count=len(downloadable_artifacts),
             requirement_count=len(subset_result.requirements),
         )
     ):
         pool = ThreadPool(processes=max_threads)
         try:
             download_results = tuple(
                 zip(
-                    target_by_downloadable_artifact,
+                    downloadable_artifacts,
                     pool.map(
                         functools.partial(
                             download_artifact,
-                            file_download_managers_by_target=file_download_managers_by_target,
+                            file_download_manager=file_download_manager,
                             vcs_download_manager=vcs_download_manager,
                             local_project_download_manager=local_project_download_manager,
                         ),
-                        target_by_downloadable_artifact.items(),
+                        downloadable_artifacts,
                     ),
                 )
             )
         finally:
             pool.close()
             pool.join()
```

### Comparing `pex-2.1.98/pex/resolve/locked_resolve.py` & `pex-2.1.99/pex/resolve/locked_resolve.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/locker.py` & `pex-2.1.99/pex/resolve/locker.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/locker_patches.py` & `pex-2.1.99/pex/resolve/locker_patches.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/create.py` & `pex-2.1.99/pex/resolve/lockfile/create.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/download_manager.py` & `pex-2.1.99/pex/resolve/lockfile/download_manager.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/json_codec.py` & `pex-2.1.99/pex/resolve/lockfile/json_codec.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/model.py` & `pex-2.1.99/pex/resolve/lockfile/model.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/subset.py` & `pex-2.1.99/pex/resolve/lockfile/subset.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/lockfile/updater.py` & `pex-2.1.99/pex/resolve/lockfile/updater.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/path_mappings.py` & `pex-2.1.99/pex/resolve/path_mappings.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/pex_repository_resolver.py` & `pex-2.1.99/pex/resolve/pex_repository_resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/requirement_configuration.py` & `pex-2.1.99/pex/resolve/requirement_configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/requirement_options.py` & `pex-2.1.99/pex/resolve/requirement_options.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/resolved_requirement.py` & `pex-2.1.99/pex/resolve/resolved_requirement.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/resolver_configuration.py` & `pex-2.1.99/pex/resolve/resolver_configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/resolver_options.py` & `pex-2.1.99/pex/resolve/resolver_options.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/resolvers.py` & `pex-2.1.99/pex/resolve/resolvers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/target_configuration.py` & `pex-2.1.99/pex/resolve/target_configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/target_options.py` & `pex-2.1.99/pex/resolve/target_options.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolve/testing.py` & `pex-2.1.99/pex/resolve/testing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/resolver.py` & `pex-2.1.99/pex/resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/result.py` & `pex-2.1.99/pex/result.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/sorted_tuple.py` & `pex-2.1.99/pex/sorted_tuple.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/targets.py` & `pex-2.1.99/pex/targets.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/testing.py` & `pex-2.1.99/pex/testing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/third_party/__init__.py` & `pex-2.1.99/pex/third_party/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/__init__.py` & `pex-2.1.99/pex/tools/commands/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/digraph.py` & `pex-2.1.99/pex/tools/commands/digraph.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/graph.py` & `pex-2.1.99/pex/tools/commands/graph.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/info.py` & `pex-2.1.99/pex/tools/commands/info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/interpreter.py` & `pex-2.1.99/pex/tools/commands/interpreter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/repository.py` & `pex-2.1.99/pex/tools/commands/repository.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/commands/venv.py` & `pex-2.1.99/pex/tools/commands/venv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tools/main.py` & `pex-2.1.99/pex/tools/main.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/tracer.py` & `pex-2.1.99/pex/tracer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/typing.py` & `pex-2.1.99/pex/typing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/util.py` & `pex-2.1.99/pex/util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/variables.py` & `pex-2.1.99/pex/variables.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/README.md` & `pex-2.1.99/pex/vendor/README.md`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/__init__.py` & `pex-2.1.99/pex/vendor/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/__main__.py` & `pex-2.1.99/pex/vendor/__main__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/__init__.pyi` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/__init__.pyi`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_cmp.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_cmp.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_compat.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_config.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_config.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_funcs.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_funcs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_make.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_make.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_next_gen.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_next_gen.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/_version_info.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/_version_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/converters.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/converters.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/exceptions.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/exceptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/exceptions.pyi` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/exceptions.pyi`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/filters.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/filters.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/setters.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/setters.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/setters.pyi` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/setters.pyi`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/validators.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/validators.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attr/validators.pyi` & `pex-2.1.99/pex/vendor/_vendored/attrs/attr/validators.pyi`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/AUTHORS.rst` & `pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/AUTHORS.rst`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/LICENSE` & `pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/LICENSE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/attrs/attrs-21.5.0.dev0.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attrs/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/attrs/attrs/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/attrs/attrs/__init__.pyi` & `pex-2.1.99/pex/vendor/_vendored/attrs/attrs/__init__.pyi`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.APACHE` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.APACHE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.BSD` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/LICENSE.BSD`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging-20.9.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/__about__.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_compat.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_structures.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/_typing.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/_typing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/markers.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/requirements.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/specifiers.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/tags.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/utils.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/packaging/version.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/packaging/version.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/LICENSE` & `pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/LICENSE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/RECORD` & `pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing-2.4.7.dist-info/RECORD`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/packaging/pyparsing.py` & `pex-2.1.99/pex/vendor/_vendored/packaging/pyparsing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/LICENSE.txt` & `pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/pip/pip-20.3.4.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/__main__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/__main__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/build_env.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/build_env.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/autocompletion.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/autocompletion.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/base_command.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/base_command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/cmdoptions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/cmdoptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/command_context.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/command_context.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/main.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/main.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/main_parser.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/main_parser.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/parser.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/parser.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/progress_bars.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/progress_bars.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/req_command.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/req_command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/cli/spinners.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/cli/spinners.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/check.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/check.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/completion.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/completion.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/configuration.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/debug.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/debug.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/download.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/download.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/freeze.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/freeze.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/hash.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/hash.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/help.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/help.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/install.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/install.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/list.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/list.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/search.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/search.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/show.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/show.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/uninstall.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/uninstall.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/commands/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/commands/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/configuration.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/configuration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/installed.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/installed.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/sdist.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/sdist.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/distributions/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/distributions/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/exceptions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/exceptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/index/collector.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/index/collector.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/index/package_finder.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/index/package_finder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/locations.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/locations.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/candidate.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/candidate.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/direct_url.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/direct_url.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/format_control.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/format_control.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/index.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/index.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/link.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/link.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/scheme.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/scheme.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/search_scope.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/search_scope.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/selection_prefs.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/selection_prefs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/target_python.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/target_python.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/models/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/models/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/auth.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/auth.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/download.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/download.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/lazy_wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/lazy_wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/session.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/session.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/utils.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/network/xmlrpc.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/network/xmlrpc.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata_legacy.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/metadata_legacy.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel_legacy.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/build/wheel_legacy.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/check.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/check.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/freeze.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/freeze.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/editable_legacy.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/editable_legacy.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/legacy.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/legacy.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/install/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/install/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/operations/prepare.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/operations/prepare.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/pyproject.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/pyproject.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/constructors.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/constructors.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_file.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_file.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_install.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_install.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_set.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_set.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_tracker.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_tracker.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/req/req_uninstall.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/req/req_uninstall.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/resolver.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/legacy/resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/candidates.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/candidates.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/factory.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/factory.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/found_candidates.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/found_candidates.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/provider.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/provider.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/reporter.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/reporter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/requirements.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/resolver.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/resolution/resolvelib/resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/self_outdated_check.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/self_outdated_check.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/appdirs.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/appdirs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/compatibility_tags.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/compatibility_tags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/deprecation.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/deprecation.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/direct_url_helpers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/direct_url_helpers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/distutils_args.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/distutils_args.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/encoding.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/encoding.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/entrypoints.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/entrypoints.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/filesystem.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/filesystem.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/filetypes.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/filetypes.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/glibc.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/glibc.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/hashes.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/hashes.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/inject_securetransport.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/inject_securetransport.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/logging.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/logging.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/misc.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/models.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/models.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/packaging.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/packaging.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/parallel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/parallel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/pkg_resources.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/pkg_resources.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/setuptools_build.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/setuptools_build.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/subprocess.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/subprocess.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/temp_dir.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/temp_dir.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/typing.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/typing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/unpacking.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/unpacking.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/urls.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/urls.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/virtualenv.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/virtualenv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/utils/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/utils/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/bazaar.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/bazaar.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/git.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/git.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/mercurial.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/mercurial.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/subversion.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/subversion.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/vcs/versioncontrol.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/vcs/versioncontrol.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_internal/wheel_builder.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_internal/wheel_builder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/appdirs.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/appdirs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/_cmd.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/_cmd.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/adapter.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/adapter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/file_cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/file_cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/redis_cache.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/caches/redis_cache.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/controller.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/controller.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/filewrapper.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/filewrapper.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/heuristics.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/heuristics.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/serialize.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/serialize.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/wrapper.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/cachecontrol/wrapper.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/cacert.pem` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/cacert.pem`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/certifi/core.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/certifi/core.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5freq.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5freq.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5prober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/big5prober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/chardistribution.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/chardistribution.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetgroupprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetgroupprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/charsetprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/chardetect.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/cli/chardetect.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/codingstatemachine.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/codingstatemachine.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/cp949prober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/cp949prober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/enums.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/enums.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/escprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/escprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/escsm.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/escsm.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/eucjpprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/eucjpprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrfreq.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrfreq.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euckrprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwfreq.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwfreq.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/euctwprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312freq.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312freq.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312prober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/gb2312prober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/hebrewprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/hebrewprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/jisfreq.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/jisfreq.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/jpcntx.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/jpcntx.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langbulgarianmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langbulgarianmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langcyrillicmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langcyrillicmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langgreekmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langgreekmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhebrewmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhebrewmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhungarianmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langhungarianmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langthaimodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langthaimodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/langturkishmodel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/langturkishmodel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/latin1prober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/latin1prober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcharsetprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcharsetprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcsgroupprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcsgroupprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcssm.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/mbcssm.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcharsetprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcharsetprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcsgroupprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sbcsgroupprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/sjisprober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/sjisprober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/universaldetector.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/universaldetector.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/chardet/utf8prober.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/chardet/utf8prober.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansi.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansi.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansitowin32.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/ansitowin32.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/initialise.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/initialise.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/win32.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/win32.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/colorama/winterm.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/colorama/winterm.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/contextlib2.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/contextlib2.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/misc.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/misc.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/shutil.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/shutil.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.cfg` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.cfg`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/sysconfig.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/tarfile.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/_backport/tarfile.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/database.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/database.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/index.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/index.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/locators.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/locators.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/manifest.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/manifest.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/markers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/markers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/metadata.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/metadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/resources.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/resources.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/scripts.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/t32.exe` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/t32.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/t64.exe` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/t64.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/util.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/version.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/version.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/w32.exe` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/w32.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/w64.exe` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/w64.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distlib/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distlib/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/distro.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/distro.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_ihatexml.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_ihatexml.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_inputstream.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_inputstream.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_tokenizer.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_tokenizer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/_base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/_base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/py.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_trie/py.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_utils.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/_utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/constants.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/constants.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/alphabeticalattributes.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/alphabeticalattributes.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/inject_meta_charset.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/inject_meta_charset.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/lint.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/lint.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/optionaltags.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/optionaltags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/sanitizer.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/sanitizer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/whitespace.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/filters/whitespace.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/html5parser.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/html5parser.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/serializer.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/serializer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/genshi.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/genshi.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/sax.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treeadapters/sax.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/dom.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/dom.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree_lxml.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treebuilders/etree_lxml.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/base.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/base.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/dom.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/dom.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree_lxml.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/etree_lxml.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/genshi.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/html5lib/treewalkers/genshi.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/codec.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/codec.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/core.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/core.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/idnadata.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/idnadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/intranges.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/intranges.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/idna/uts46data.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/idna/uts46data.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/ipaddress.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/ipaddress.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/exceptions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/exceptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/ext.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/ext.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/msgpack/fallback.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/msgpack/fallback.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/__about__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_structures.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/_typing.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/_typing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/markers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/requirements.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/specifiers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/tags.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/utils.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/packaging/version.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/_in_process.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/_in_process.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/build.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/build.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/check.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/check.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/colorlog.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/colorlog.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/dirtools.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/dirtools.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/envbuild.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/envbuild.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/meta.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/meta.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pep517/wrappers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pep517/wrappers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/py31compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pkg_resources/py31compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/bar.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/bar.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/counter.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/counter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/progress/spinner.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/progress/spinner.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/pyparsing.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/pyparsing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/_internal_utils.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/_internal_utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/adapters.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/adapters.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/api.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/api.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/auth.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/auth.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/compat.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/cookies.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/cookies.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/exceptions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/exceptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/help.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/help.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/hooks.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/hooks.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/models.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/models.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/packages.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/packages.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/sessions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/sessions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/status_codes.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/status_codes.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/structures.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/structures.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/requests/utils.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/requests/utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/providers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/providers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/reporters.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/reporters.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/resolvers.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/resolvers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/structs.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/resolvelib/structs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/retrying.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/retrying.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/six.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/decoder.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/decoder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/encoder.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/encoder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/toml/tz.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/toml/tz.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_collections.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/_collections.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connection.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connection.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connectionpool.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/connectionpool.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_appengine_environ.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_appengine_environ.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/bindings.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/bindings.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/low_level.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/_securetransport/low_level.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/appengine.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/appengine.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/ntlmpool.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/ntlmpool.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/pyopenssl.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/pyopenssl.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/securetransport.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/securetransport.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/socks.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/contrib/socks.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/exceptions.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/exceptions.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/fields.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/fields.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/filepost.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/filepost.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/makefile.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/backports/makefile.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/six.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/six.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/_implementation.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/packages/ssl_match_hostname/_implementation.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/poolmanager.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/poolmanager.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/request.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/request.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/response.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/response.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/connection.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/connection.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/proxy.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/proxy.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/request.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/request.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/response.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/response.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/retry.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/retry.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssl_.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssl_.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssltransport.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/ssltransport.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/timeout.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/timeout.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/url.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/url.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/wait.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/urllib3/util/wait.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/labels.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/labels.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/mklabels.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/mklabels.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/tests.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/tests.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/pip/pip/_vendor/webencodings/x_user_defined.py` & `pex-2.1.99/pex/vendor/_vendored/pip/pip/_vendor/webencodings/x_user_defined.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/appdirs.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/appdirs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__about__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_structures.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/markers.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/requirements.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/specifiers.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/version.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/pyparsing.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/pyparsing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/six.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/extern/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/extern/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/pkg_resources/py31compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/pkg_resources/py31compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/LICENSE` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/LICENSE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/entry_points.txt` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools-44.0.0+3acb925dd708430aeaf197ea53ac8a752f7c1863.dist-info/entry_points.txt`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_imp.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_imp.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/ordered_set.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/ordered_set.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__about__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__about__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_structures.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/_structures.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/markers.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/markers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/requirements.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/specifiers.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/specifiers.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/tags.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/utils.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/version.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/packaging/version.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/pyparsing.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/pyparsing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/_vendor/six.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/_vendor/six.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/archive_util.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/archive_util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/build_meta.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/build_meta.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli-32.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli-32.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli-64.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli-64.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/cli.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/cli.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/alias.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/alias.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_egg.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_egg.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_rpm.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_rpm.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/bdist_wininst.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/bdist_wininst.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_clib.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_clib.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_ext.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_ext.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/build_py.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/build_py.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/develop.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/develop.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/dist_info.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/dist_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/easy_install.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/easy_install.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/egg_info.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/egg_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_egg_info.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_egg_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_lib.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_lib.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/install_scripts.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/install_scripts.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/launcher manifest.xml` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/launcher manifest.xml`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/py36compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/py36compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/register.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/register.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/rotate.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/rotate.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/saveopts.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/saveopts.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/sdist.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/sdist.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/setopt.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/setopt.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/test.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/test.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/upload.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/upload.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/command/upload_docs.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/command/upload_docs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/config.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/config.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/dep_util.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/dep_util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/depends.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/depends.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/dist.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/dist.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/errors.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/errors.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/extension.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/extension.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/extern/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/extern/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/glob.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/glob.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui-32.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui-32.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui-64.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui-64.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/gui.exe` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/gui.exe`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/installer.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/installer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/launch.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/launch.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/lib2to3_ex.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/lib2to3_ex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/monkey.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/monkey.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/msvc.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/msvc.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/namespaces.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/namespaces.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/package_index.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/package_index.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py27compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py27compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py31compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py31compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/py33compat.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/py33compat.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/sandbox.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/sandbox.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/site-patch.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/site-patch.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/ssl_support.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/ssl_support.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/unicode_utils.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/unicode_utils.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/wheel.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/setuptools/setuptools/windows_support.py` & `pex-2.1.99/pex/vendor/_vendored/setuptools/setuptools/windows_support.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/LICENSE` & `pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/LICENSE`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/toml/toml-0.10.2.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/toml/toml/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml/decoder.py` & `pex-2.1.99/pex/vendor/_vendored/toml/toml/decoder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml/encoder.py` & `pex-2.1.99/pex/vendor/_vendored/toml/toml/encoder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml/ordered.py` & `pex-2.1.99/pex/vendor/_vendored/toml/toml/ordered.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/toml/toml/tz.py` & `pex-2.1.99/pex/vendor/_vendored/toml/toml/tz.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/LICENSE.txt` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/METADATA` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel-0.37.1.dist-info/METADATA`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/bdist_wheel.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/bdist_wheel.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/__init__.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/convert.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/convert.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/pack.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/pack.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/cli/unpack.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/cli/unpack.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/macosx_libfile.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/macosx_libfile.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/metadata.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/metadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/pkginfo.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/pkginfo.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/util.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/packaging/_typing.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/packaging/_typing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/vendored/packaging/tags.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/vendored/packaging/tags.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/vendor/_vendored/wheel/wheel/wheelfile.py` & `pex-2.1.99/pex/vendor/_vendored/wheel/wheel/wheelfile.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/venv/pex.py` & `pex-2.1.99/pex/venv/pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pex/venv/virtualenv.py` & `pex-2.1.99/pex/venv/virtualenv.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 # Copyright 2020 Pants project contributors (see CONTRIBUTORS.md).
 # Licensed under the Apache License, Version 2.0 (see LICENSE).
 
 from __future__ import absolute_import
 
-import fileinput
 import logging
 import os
 import pkgutil
 import re
+from fileinput import FileInput
+
 import sys
 from contextlib import closing
 from pex.common import AtomicDirectory, is_exe, safe_mkdir
 from pex.compatibility import get_stdout_bytes_buffer
 from pex.dist_metadata import find_distributions, Distribution
 from pex.interpreter import PythonInterpreter
 from pex.tracer import TRACER
@@ -282,15 +283,15 @@
         scripts = [
             path
             for path in self._base_bin
             if _is_python_script(path) or re.search(r"^[Aa]ctivate", os.path.basename(path))
         ]
         if scripts:
             rewritten_files = set()
-            with closing(fileinput.input(files=sorted(scripts), inplace=True)) as fi:
+            with closing(FileInput(files=sorted(scripts), inplace=True)) as fi:
                 for line in fi:
                     rewritten_line = line.replace(self._venv_dir, real_venv_dir)
                     if rewritten_line != line:
                         filename = fi.filename()
                         if filename not in rewritten_files:
                             rewritten_files.add(filename)
                             yield filename
@@ -303,17 +304,17 @@
     ):
         # type: (...) -> Iterator[str]
         python_scripts = [
             executable for executable in self.iter_executables() if _is_python_script(executable)
         ]
         if python_scripts:
             with closing(
-                fileinput.input(files=sorted(python_scripts), inplace=True, mode="rb")
+                FileInput(files=sorted(python_scripts), inplace=True, mode="rb")
             ) as fi:
-                # N.B.: `fileinput` is strange, but useful: the context manager above monkey-patches
+                # N.B.: `FileInput` is strange, but useful: the context manager above monkey-patches
                 # sys.stdout to print to the corresponding original input file, which is has moved
                 # aside.
                 for line in fi:
                     buffer = get_stdout_bytes_buffer()
                     if fi.isfirstline():
                         shebang = [python or self._interpreter.binary]
                         if python_args:
```

### Comparing `pex-2.1.98/pex/venv/virtualenv_16.7.12_py` & `pex-2.1.99/pex/venv/virtualenv_16.7.12_py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/pyproject.toml` & `pex-2.1.99/pyproject.toml`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/scripts/package.py` & `pex-2.1.99/scripts/package.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/scripts/typecheck.sh` & `pex-2.1.99/scripts/typecheck.sh`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/bin/test_sh_boot.py` & `pex-2.1.99/tests/bin/test_sh_boot.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/build_system/test_pep_517.py` & `pex-2.1.99/tests/build_system/test_pep_517.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/build_system/test_pep_518.py` & `pex-2.1.99/tests/build_system/test_pep_518.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/commands/test_command.py` & `pex-2.1.99/tests/commands/test_command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/conftest.py` & `pex-2.1.99/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/data/platforms/macosx_10_13_x86_64-cp-36-m.tags.txt` & `pex-2.1.99/tests/data/platforms/macosx_10_13_x86_64-cp-36-m.tags.txt`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/example_packages/MarkupSafe-1.0-cp27-cp27mu-linux_x86_64.whl` & `pex-2.1.99/tests/example_packages/MarkupSafe-1.0-cp27-cp27mu-linux_x86_64.whl`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/example_packages/PyAthena-1.11.5-py2.py3-none-any.whl` & `pex-2.1.99/tests/example_packages/PyAthena-1.11.5-py2.py3-none-any.whl`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/example_packages/PyAthena-1.9.0-py2.py3-none-any.whl` & `pex-2.1.99/tests/example_packages/PyAthena-1.9.0-py2.py3-none-any.whl`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/example_packages/aws_cfn_bootstrap-1.4-py2-none-any.whl` & `pex-2.1.99/tests/example_packages/aws_cfn_bootstrap-1.4-py2-none-any.whl`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/example_packages/pyparsing-2.1.10-py2.py3-none-any.whl` & `pex-2.1.99/tests/example_packages/pyparsing-2.1.10-py2.py3-none-any.whl`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/build_system/test_pep_517.py` & `pex-2.1.99/tests/integration/build_system/test_pep_517.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/build_system/test_pep_518.py` & `pex-2.1.99/tests/integration/build_system/test_pep_518.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_export.py` & `pex-2.1.99/tests/integration/cli/commands/test_export.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_interpreter_inspect.py` & `pex-2.1.99/tests/integration/cli/commands/test_interpreter_inspect.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1413.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1413.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1665.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1665.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1667.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1667.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1688.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1688.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1711.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1711.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1734.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1734.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1741.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1741.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1801.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1801.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_issue_1821.py` & `pex-2.1.99/tests/integration/cli/commands/test_issue_1821.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_local_project_lock.py` & `pex-2.1.99/tests/integration/cli/commands/test_local_project_lock.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_lock.py` & `pex-2.1.99/tests/integration/cli/commands/test_lock.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_lock_resolve_auth.py` & `pex-2.1.99/tests/integration/cli/commands/test_lock_resolve_auth.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/cli/commands/test_vcs_lock.py` & `pex-2.1.99/tests/integration/cli/commands/test_vcs_lock.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/conftest.py` & `pex-2.1.99/tests/integration/conftest.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_downloads.py` & `pex-2.1.99/tests/integration/test_downloads.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_executuon_mode_venv.py` & `pex-2.1.99/tests/integration/test_executuon_mode_venv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_integration.py` & `pex-2.1.99/tests/integration/test_integration.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_interpreter_selection.py` & `pex-2.1.99/tests/integration/test_interpreter_selection.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1017.py` & `pex-2.1.99/tests/integration/test_issue_1017.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1018.py` & `pex-2.1.99/tests/integration/test_issue_1018.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1025.py` & `pex-2.1.99/tests/integration/test_issue_1025.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1031.py` & `pex-2.1.99/tests/integration/test_issue_1031.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1179.py` & `pex-2.1.99/tests/integration/test_issue_1179.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1201.py` & `pex-2.1.99/tests/integration/test_issue_1201.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1202.py` & `pex-2.1.99/tests/integration/test_issue_1202.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1218.py` & `pex-2.1.99/tests/integration/test_issue_1218.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1225.py` & `pex-2.1.99/tests/integration/test_issue_1225.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1232.py` & `pex-2.1.99/tests/integration/test_issue_1232.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1302.py` & `pex-2.1.99/tests/integration/test_issue_1302.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1316.py` & `pex-2.1.99/tests/integration/test_issue_1316.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1336.py` & `pex-2.1.99/tests/integration/test_issue_1336.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1422.py` & `pex-2.1.99/tests/integration/test_issue_1422.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1447.py` & `pex-2.1.99/tests/integration/test_issue_1447.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1479.py` & `pex-2.1.99/tests/integration/test_issue_1479.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1520.py` & `pex-2.1.99/tests/integration/test_issue_1520.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1537.py` & `pex-2.1.99/tests/integration/test_issue_1537.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1550.py` & `pex-2.1.99/tests/integration/test_issue_1550.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1560.py` & `pex-2.1.99/tests/integration/test_issue_1560.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1597.py` & `pex-2.1.99/tests/integration/test_issue_1597.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1598.py` & `pex-2.1.99/tests/integration/test_issue_1598.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1656.py` & `pex-2.1.99/tests/integration/test_issue_1656.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1683.py` & `pex-2.1.99/tests/integration/test_issue_1683.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1726.py` & `pex-2.1.99/tests/integration/test_issue_1726.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1730.py` & `pex-2.1.99/tests/integration/test_issue_1730.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1802.py` & `pex-2.1.99/tests/integration/test_issue_1802.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1809.py` & `pex-2.1.99/tests/integration/test_issue_1809.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1817.py` & `pex-2.1.99/tests/integration/test_issue_1817.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_1825.py` & `pex-2.1.99/tests/integration/test_issue_1825.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_434.py` & `pex-2.1.99/tests/integration/test_issue_434.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_539.py` & `pex-2.1.99/tests/integration/test_issue_539.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_598.py` & `pex-2.1.99/tests/integration/test_issue_598.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_661.py` & `pex-2.1.99/tests/integration/test_issue_661.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_729.py` & `pex-2.1.99/tests/integration/test_issue_729.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_736.py` & `pex-2.1.99/tests/integration/test_issue_736.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_745.py` & `pex-2.1.99/tests/integration/test_issue_745.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_749.py` & `pex-2.1.99/tests/integration/test_issue_749.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_898.py` & `pex-2.1.99/tests/integration/test_issue_898.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_899.py` & `pex-2.1.99/tests/integration/test_issue_899.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_940.py` & `pex-2.1.99/tests/integration/test_issue_940.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_issue_996.py` & `pex-2.1.99/tests/integration/test_issue_996.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_layout.py` & `pex-2.1.99/tests/integration/test_layout.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_lock_resolver.py` & `pex-2.1.99/tests/integration/test_lock_resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_locked_resolve.py` & `pex-2.1.99/tests/integration/test_locked_resolve.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_pex_bootstrapper.py` & `pex-2.1.99/tests/integration/test_pex_bootstrapper.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_pex_entry_points.py` & `pex-2.1.99/tests/integration/test_pex_entry_points.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_pex_import.py` & `pex-2.1.99/tests/integration/test_pex_import.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_reexec.py` & `pex-2.1.99/tests/integration/test_reexec.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_reproducible.py` & `pex-2.1.99/tests/integration/test_reproducible.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_setproctitle.py` & `pex-2.1.99/tests/integration/test_setproctitle.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_sh_boot.py` & `pex-2.1.99/tests/integration/test_sh_boot.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_shebang_length_limit.py` & `pex-2.1.99/tests/integration/test_shebang_length_limit.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/test_variables.py` & `pex-2.1.99/tests/integration/test_variables.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/tools/commands/test_venv.py` & `pex-2.1.99/tests/integration/tools/commands/test_venv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_issue_1630.py` & `pex-2.1.99/tests/integration/venv_ITs/test_issue_1630.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_issue_1637.py` & `pex-2.1.99/tests/integration/venv_ITs/test_issue_1637.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_issue_1641.py` & `pex-2.1.99/tests/integration/venv_ITs/test_issue_1641.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_issue_1668.py` & `pex-2.1.99/tests/integration/venv_ITs/test_issue_1668.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_issue_1745.py` & `pex-2.1.99/tests/integration/venv_ITs/test_issue_1745.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/integration/venv_ITs/test_virtualenv.py` & `pex-2.1.99/tests/integration/venv_ITs/test_virtualenv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/pip/test_tailer.py` & `pex-2.1.99/tests/pip/test_tailer.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/lockfile/test_download_manager.py` & `pex-2.1.99/tests/resolve/lockfile/test_download_manager.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/lockfile/test_json_codec.py` & `pex-2.1.99/tests/resolve/lockfile/test_json_codec.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/lockfile/test_lockfile.py` & `pex-2.1.99/tests/resolve/lockfile/test_lockfile.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/test_locked_resolve.py` & `pex-2.1.99/tests/resolve/test_locked_resolve.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/test_path_mappings.py` & `pex-2.1.99/tests/resolve/test_path_mappings.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/test_pex_repository_resolver.py` & `pex-2.1.99/tests/resolve/test_pex_repository_resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/test_resolver_options.py` & `pex-2.1.99/tests/resolve/test_resolver_options.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/resolve/test_target_options.py` & `pex-2.1.99/tests/resolve/test_target_options.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_bdist_pex.py` & `pex-2.1.99/tests/test_bdist_pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_common.py` & `pex-2.1.99/tests/test_common.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_compatibility.py` & `pex-2.1.99/tests/test_compatibility.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_compiler.py` & `pex-2.1.99/tests/test_compiler.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_dist_metadata.py` & `pex-2.1.99/tests/test_dist_metadata.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_enum.py` & `pex-2.1.99/tests/test_enum.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_environment.py` & `pex-2.1.99/tests/test_environment.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_execution_mode.py` & `pex-2.1.99/tests/test_execution_mode.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_executor.py` & `pex-2.1.99/tests/test_executor.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_fetcher.py` & `pex-2.1.99/tests/test_fetcher.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_finders.py` & `pex-2.1.99/tests/test_finders.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_hashing.py` & `pex-2.1.99/tests/test_hashing.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_inherits_path_option.py` & `pex-2.1.99/tests/test_inherits_path_option.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_interpreter.py` & `pex-2.1.99/tests/test_interpreter.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_interpreter_constraints.py` & `pex-2.1.99/tests/test_interpreter_constraints.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_jobs.py` & `pex-2.1.99/tests/test_jobs.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_packaging.py` & `pex-2.1.99/tests/test_packaging.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pep_376.py` & `pex-2.1.99/tests/test_pep_376.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pep_425.py` & `pex-2.1.99/tests/test_pep_425.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pep_508.py` & `pex-2.1.99/tests/test_pep_508.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex.py` & `pex-2.1.99/tests/test_pex.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex_binary.py` & `pex-2.1.99/tests/test_pex_binary.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex_bootstrapper.py` & `pex-2.1.99/tests/test_pex_bootstrapper.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex_builder.py` & `pex-2.1.99/tests/test_pex_builder.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex_info.py` & `pex-2.1.99/tests/test_pex_info.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pex_warnings.py` & `pex-2.1.99/tests/test_pex_warnings.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_pip.py` & `pex-2.1.99/tests/test_pip.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_platform.py` & `pex-2.1.99/tests/test_platform.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_requirements.py` & `pex-2.1.99/tests/test_requirements.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_resolver.py` & `pex-2.1.99/tests/test_resolver.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_sorted_tuple.py` & `pex-2.1.99/tests/test_sorted_tuple.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_targets.py` & `pex-2.1.99/tests/test_targets.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_third_party.py` & `pex-2.1.99/tests/test_third_party.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_util.py` & `pex-2.1.99/tests/test_util.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_variables.py` & `pex-2.1.99/tests/test_variables.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/test_vendor.py` & `pex-2.1.99/tests/test_vendor.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/tools/commands/test_interpreter_command.py` & `pex-2.1.99/tests/tools/commands/test_interpreter_command.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/tools/commands/test_repository.py` & `pex-2.1.99/tests/tools/commands/test_repository.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tests/tools/commands/test_venv.py` & `pex-2.1.99/tests/tools/commands/test_venv.py`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/tox.ini` & `pex-2.1.99/tox.ini`

 * *Files identical despite different names*

### Comparing `pex-2.1.98/PKG-INFO` & `pex-2.1.99/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pex
-Version: 2.1.98
+Version: 2.1.99
 Summary: The PEX packaging toolchain.
 Home-page: https://github.com/pantsbuild/pex
 Author: The PEX developers
 Author-email: pantsbuild@gmail.com
 Requires-Python: >=2.7,<3.12,!=3.0.*,!=3.1.*,!=3.2.*,!=3.3.*,!=3.4.*
 Description-Content-Type: text/x-rst
 Classifier: Development Status :: 5 - Production/Stable
```

