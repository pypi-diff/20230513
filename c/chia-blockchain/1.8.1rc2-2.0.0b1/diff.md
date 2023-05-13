# Comparing `tmp/chia-blockchain-1.8.1rc2.tar.gz` & `tmp/chia-blockchain-2.0.0b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chia-blockchain-1.8.1rc2.tar", last modified: Sat May 13 03:16:39 2023, max compression
+gzip compressed data, was "chia-blockchain-2.0.0b1.tar", last modified: Tue May  9 02:17:12 2023, max compression
```

## Comparing `chia-blockchain-1.8.1rc2.tar` & `chia-blockchain-2.0.0b1.tar`

### file list

```diff
@@ -1,1066 +1,1070 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.847989 chia-blockchain-1.8.1rc2/
--rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.coveragerc
--rw-r--r--   0 runner    (1001) docker     (123)      293 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.591987 chia-blockchain-1.8.1rc2/.github/
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/CODEOWNERS
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.595987 chia-blockchain-1.8.1rc2/.github/ISSUE_TEMPLATE/
--rw-r--r--   0 runner    (1001) docker     (123)     1406 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/ISSUE_TEMPLATE/bug_report.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/ISSUE_TEMPLATE/config.yml
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/PULL_REQUEST_TEMPLATE.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.575986 chia-blockchain-1.8.1rc2/.github/actions/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.595987 chia-blockchain-1.8.1rc2/.github/actions/install/
--rw-r--r--   0 runner    (1001) docker     (123)     1391 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/actions/install/action.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1006 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/dependabot.yml
--rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/release.yml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.599987 chia-blockchain-1.8.1rc2/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2213 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/benchmarks.yml
--rw-r--r--   0 runner    (1001) docker     (123)    12246 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/build-linux-arm64-installer.yml
--rw-r--r--   0 runner    (1001) docker     (123)    12139 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/build-linux-installer-deb.yml
--rw-r--r--   0 runner    (1001) docker     (123)    12226 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/build-linux-installer-rpm.yml
--rw-r--r--   0 runner    (1001) docker     (123)    13442 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/build-macos-installers.yml
--rw-r--r--   0 runner    (1001) docker     (123)    13299 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/build-windows-installer.yml
--rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/check-commit-signing.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2093 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/check_wheel_availability.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2758 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/codeql-analysis.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1036 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/conflict-check.yml
--rw-r--r--   0 runner    (1001) docker     (123)      335 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/daily-matrix.yml
--rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/dependency-review.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1338 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/mozilla-ca-cert.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2065 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/pre-commit.yml
--rw-r--r--   0 runner    (1001) docker     (123)      699 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/require-labels.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2226 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/snyk-python-scan.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1434 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/stale-issue.yml
--rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/start-release.yml
--rw-r--r--   0 runner    (1001) docker     (123)      899 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/start-sync-test.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2383 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/super-linter.yml
--rw-r--r--   0 runner    (1001) docker     (123)     6612 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/test-install-scripts.yml
--rw-r--r--   0 runner    (1001) docker     (123)     8783 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/test-single.yml
--rw-r--r--   0 runner    (1001) docker     (123)     5446 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/test.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/trigger-docker-dev.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/trigger-docker-main.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2437 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.github/workflows/upload-pypi-source.yml
--rw-r--r--   0 runner    (1001) docker     (123)     5420 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.gitmodules
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.isort.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1009 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.markdown-lint.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2043 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/BUILD_TIMELORD.md
--rw-r--r--   0 runner    (1001) docker     (123)   209772 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     3477 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/CODE_OF_CONDUCT.md
--rw-r--r--   0 runner    (1001) docker     (123)     8356 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/CONTRIBUTING.md
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/INSTALL.md
--rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/Install-gui.ps1
--rw-r--r--   0 runner    (1001) docker     (123)     5155 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/Install-plotter.ps1
--rw-r--r--   0 runner    (1001) docker     (123)     3770 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/Install.ps1
--rw-r--r--   0 runner    (1001) docker     (123)    11342 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-05-13 03:16:39.847989 chia-blockchain-1.8.1rc2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    33099 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/PRETTY_GOOD_PRACTICES.md
--rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      701 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/SECURITY.md
--rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/activated.ps1
--rwxr-xr-x   0 runner    (1001) docker     (123)      630 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/activated.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      155 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/activated.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.603987 chia-blockchain-1.8.1rc2/benchmarks/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/block_ref.py
--rw-r--r--   0 runner    (1001) docker     (123)    14354 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/block_store.py
--rw-r--r--   0 runner    (1001) docker     (123)   121543 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/clvm_generator.bin
--rw-r--r--   0 runner    (1001) docker     (123)     9537 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/jsonify.py
--rw-r--r--   0 runner    (1001) docker     (123)     5062 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/mempool-long-lived.py
--rw-r--r--   0 runner    (1001) docker     (123)    11096 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/mempool.py
--rw-r--r--   0 runner    (1001) docker     (123)    11782 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/streamable.py
--rw-r--r--   0 runner    (1001) docker     (123)   439288 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/transaction_height_delta
--rw-r--r--   0 runner    (1001) docker     (123)     6327 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/benchmarks/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.603987 chia-blockchain-1.8.1rc2/build_scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.603987 chia-blockchain-1.8.1rc2/build_scripts/assets/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.607987 chia-blockchain-1.8.1rc2/build_scripts/assets/deb/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/deb/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      277 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/deb/control.j2
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/deb/postinst.sh
--rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/deb/prerm.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.607987 chia-blockchain-1.8.1rc2/build_scripts/assets/dmg/
--rw-r--r--   0 runner    (1001) docker     (123)      315 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/dmg/README
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/dmg/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   507222 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/dmg/background.tiff
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.607987 chia-blockchain-1.8.1rc2/build_scripts/assets/rpm/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/rpm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/rpm/postinst.sh
--rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/assets/rpm/prerm.sh
--rw-r--r--   0 runner    (1001) docker     (123)     1328 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_linux_deb-1-gui.sh
--rw-r--r--   0 runner    (1001) docker     (123)     4684 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_linux_deb-2-installer.sh
--rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_linux_rpm-1-gui.sh
--rw-r--r--   0 runner    (1001) docker     (123)     3818 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_linux_rpm-2-installer.sh
--rw-r--r--   0 runner    (1001) docker     (123)     1350 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_macos-1-gui.sh
--rw-r--r--   0 runner    (1001) docker     (123)     3416 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_macos-2-installer.sh
--rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_windows-1-gui.ps1
--rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/build_windows-2-installer.ps1
--rw-r--r--   0 runner    (1001) docker     (123)     2218 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/check_dependency_artifacts.py
--rw-r--r--   0 runner    (1001) docker     (123)      907 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/clean-runner.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/installer-version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.607987 chia-blockchain-1.8.1rc2/build_scripts/npm_global/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_global/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      342 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_global/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)      267 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_global/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.607987 chia-blockchain-1.8.1rc2/build_scripts/npm_linux/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_linux/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   539731 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_linux/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)      305 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_linux/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.611987 chia-blockchain-1.8.1rc2/build_scripts/npm_macos/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_macos/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   572329 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_macos/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)      379 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_macos/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.611987 chia-blockchain-1.8.1rc2/build_scripts/npm_windows/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_windows/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   553007 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_windows/package-lock.json
--rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/build_scripts/npm_windows/package.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.611987 chia-blockchain-1.8.1rc2/chia/
--rw-r--r--   0 runner    (1001) docker     (123)      347 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       76 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.615987 chia-blockchain-1.8.1rc2/chia/clvm/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/clvm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/clvm/singleton.py
--rw-r--r--   0 runner    (1001) docker     (123)    18474 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/clvm/spend_sim.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.623987 chia-blockchain-1.8.1rc2/chia/cmds/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7240 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/beta.py
--rw-r--r--   0 runner    (1001) docker     (123)     4705 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/beta_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)    16346 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/check_wallet_db.py
--rw-r--r--   0 runner    (1001) docker     (123)     4576 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/chia.py
--rw-r--r--   0 runner    (1001) docker     (123)    10100 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/cmds_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    10675 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/coin_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     6740 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/coins.py
--rw-r--r--   0 runner    (1001) docker     (123)     1399 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/completion.py
--rw-r--r--   0 runner    (1001) docker     (123)    13241 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/configure.py
--rw-r--r--   0 runner    (1001) docker     (123)    11437 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/data.py
--rw-r--r--   0 runner    (1001) docker     (123)     8324 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/data_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2961 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/db.py
--rw-r--r--   0 runner    (1001) docker     (123)     3341 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/db_backup_func.py
--rw-r--r--   0 runner    (1001) docker     (123)    17725 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/db_upgrade_func.py
--rw-r--r--   0 runner    (1001) docker     (123)     7802 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/db_validate_func.py
--rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/dev.py
--rw-r--r--   0 runner    (1001) docker     (123)     2186 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/farm.py
--rw-r--r--   0 runner    (1001) docker     (123)     8468 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/farm_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2085 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/init.py
--rw-r--r--   0 runner    (1001) docker     (123)    16283 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/init_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)    15066 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/keys.py
--rw-r--r--   0 runner    (1001) docker     (123)    26855 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/keys_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1297 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/netspace.py
--rw-r--r--   0 runner    (1001) docker     (123)     2826 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/netspace_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     4814 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/passphrase.py
--rw-r--r--   0 runner    (1001) docker     (123)    12569 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/passphrase_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1404 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/peer.py
--rw-r--r--   0 runner    (1001) docker     (123)     5475 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/peer_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     8198 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/plotnft.py
--rw-r--r--   0 runner    (1001) docker     (123)    17323 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/plotnft_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     7236 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/plots.py
--rw-r--r--   0 runner    (1001) docker     (123)      405 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/plotters.py
--rw-r--r--   0 runner    (1001) docker     (123)     4736 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     2427 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/show.py
--rw-r--r--   0 runner    (1001) docker     (123)     9863 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/show_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     8013 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/sim.py
--rw-r--r--   0 runner    (1001) docker     (123)    22939 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/sim_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)      788 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/start.py
--rw-r--r--   0 runner    (1001) docker     (123)     3452 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/start_funcs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2031 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/stop.py
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/units.py
--rw-r--r--   0 runner    (1001) docker     (123)    38959 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)    49653 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/cmds/wallet_funcs.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.627987 chia-blockchain-1.8.1rc2/chia/consensus/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    22930 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_body_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)    21437 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_creation.py
--rw-r--r--   0 runner    (1001) docker     (123)    51189 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_header_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4805 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_record.py
--rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_rewards.py
--rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/block_root_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)    42752 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/blockchain.py
--rw-r--r--   0 runner    (1001) docker     (123)     3725 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/blockchain_interface.py
--rw-r--r--   0 runner    (1001) docker     (123)     1201 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/coinbase.py
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/condition_costs.py
--rw-r--r--   0 runner    (1001) docker     (123)     4446 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)      517 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/cost_calculator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3699 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/default_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2183 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/deficit.py
--rw-r--r--   0 runner    (1001) docker     (123)    18266 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/difficulty_adjustment.py
--rw-r--r--   0 runner    (1001) docker     (123)     1253 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/find_fork_point.py
--rw-r--r--   0 runner    (1001) docker     (123)     6609 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/full_block_to_block_record.py
--rw-r--r--   0 runner    (1001) docker     (123)     4823 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/get_block_challenge.py
--rw-r--r--   0 runner    (1001) docker     (123)     7852 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/make_sub_epoch_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)    18835 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/multiprocess_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)      788 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/pos_quality.py
--rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/pot_iterations.py
--rw-r--r--   0 runner    (1001) docker     (123)     6971 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/consensus/vdf_info_computation.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.627987 chia-blockchain-1.8.1rc2/chia/daemon/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7977 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/client.py
--rw-r--r--   0 runner    (1001) docker     (123)    18190 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/keychain_proxy.py
--rw-r--r--   0 runner    (1001) docker     (123)    11125 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/keychain_server.py
--rw-r--r--   0 runner    (1001) docker     (123)    56085 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/server.py
--rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/daemon/windows_signal.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.631987 chia-blockchain-1.8.1rc2/chia/data_layer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    40675 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer.py
--rw-r--r--   0 runner    (1001) docker     (123)      696 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1143 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_errors.py
--rw-r--r--   0 runner    (1001) docker     (123)     4996 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_server.py
--rw-r--r--   0 runner    (1001) docker     (123)    18391 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    62475 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)    62999 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/data_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    13650 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/dl_wallet_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     8556 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/download_data.py
--rw-r--r--   0 runner    (1001) docker     (123)     1136 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/s3_plugin_config.yml
--rw-r--r--   0 runner    (1001) docker     (123)    16377 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/s3_plugin_service.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.631987 chia-blockchain-1.8.1rc2/chia/data_layer/util/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4716 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/data_layer/util/benchmark.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.631987 chia-blockchain-1.8.1rc2/chia/farmer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/farmer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    36468 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/farmer/farmer.py
--rw-r--r--   0 runner    (1001) docker     (123)    28233 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/farmer/farmer_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.639987 chia-blockchain-1.8.1rc2/chia/full_node/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/bitcoin_fee_estimator.py
--rw-r--r--   0 runner    (1001) docker     (123)     9689 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/block_height_map.py
--rw-r--r--   0 runner    (1001) docker     (123)    32512 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/block_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     6305 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/bundle_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)    24796 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimate.py
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimate_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2922 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimation.py
--rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1235 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     1955 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_example.py
--rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_interface.py
--rw-r--r--   0 runner    (1001) docker     (123)      610 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_history.py
--rw-r--r--   0 runner    (1001) docker     (123)    22559 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/fee_tracker.py
--rw-r--r--   0 runner    (1001) docker     (123)   130223 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/full_node.py
--rw-r--r--   0 runner    (1001) docker     (123)    79298 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/full_node_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    36689 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/full_node_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2446 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2731 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/hint_management.py
--rw-r--r--   0 runner    (1001) docker     (123)     2524 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/hint_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2854 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/lock_queue.py
--rw-r--r--   0 runner    (1001) docker     (123)    17497 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/mempool.py
--rw-r--r--   0 runner    (1001) docker     (123)     6167 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/mempool_check_conditions.py
--rw-r--r--   0 runner    (1001) docker     (123)    33485 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/mempool_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3670 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/pending_tx_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)      414 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/signage_point.py
--rw-r--r--   0 runner    (1001) docker     (123)     5619 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/subscriptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/sync_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     3335 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/tx_processing_queue.py
--rw-r--r--   0 runner    (1001) docker     (123)    72530 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/full_node/weight_proof.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.639987 chia-blockchain-1.8.1rc2/chia/harvester/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/harvester/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7862 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/harvester/harvester.py
--rw-r--r--   0 runner    (1001) docker     (123)    15433 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/harvester/harvester_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.639987 chia-blockchain-1.8.1rc2/chia/introducer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/introducer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4173 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/introducer/introducer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2009 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/introducer/introducer_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.643987 chia-blockchain-1.8.1rc2/chia/plot_sync/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/delta.py
--rw-r--r--   0 runner    (1001) docker     (123)     2306 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)    14237 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/receiver.py
--rw-r--r--   0 runner    (1001) docker     (123)    13867 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/sender.py
--rw-r--r--   0 runner    (1001) docker     (123)      825 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plot_sync/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.643987 chia-blockchain-1.8.1rc2/chia/plotters/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11146 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/bladebit.py
--rw-r--r--   0 runner    (1001) docker     (123)     1893 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/chiapos.py
--rw-r--r--   0 runner    (1001) docker     (123)     7591 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/madmax.py
--rw-r--r--   0 runner    (1001) docker     (123)    16640 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/plotters.py
--rw-r--r--   0 runner    (1001) docker     (123)     4050 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotters/plotters_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.647987 chia-blockchain-1.8.1rc2/chia/plotting/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7803 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     9712 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/check_plots.py
--rw-r--r--   0 runner    (1001) docker     (123)    10542 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/create_plots.py
--rw-r--r--   0 runner    (1001) docker     (123)    16154 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     9139 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/plotting/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.647987 chia-blockchain-1.8.1rc2/chia/pools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3893 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pools/pool_config.py
--rw-r--r--   0 runner    (1001) docker     (123)    17113 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pools/pool_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)    44516 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pools/pool_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4535 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pools/pool_wallet_info.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.647987 chia-blockchain-1.8.1rc2/chia/protocols/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1841 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/farmer_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/full_node_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     4283 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/harvester_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)      600 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/introducer_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     4059 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/pool_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/protocol_message_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/protocol_state_machine.py
--rw-r--r--   0 runner    (1001) docker     (123)      235 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/protocol_timing.py
--rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/shared_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     3111 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/timelord_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     5771 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/protocols/wallet_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     5617 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/pyinstaller.spec
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.651987 chia-blockchain-1.8.1rc2/chia/rpc/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2640 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/crawler_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    18476 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     5321 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     2003 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    13582 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/farmer_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     3989 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/farmer_rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)    41327 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/full_node_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    12136 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/full_node_rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     3084 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/harvester_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/harvester_rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     3396 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)    17016 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/rpc_server.py
--rw-r--r--   0 runner    (1001) docker     (123)      863 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/timelord_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/util.py
--rw-r--r--   0 runner    (1001) docker     (123)   160800 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/wallet_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    44813 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/rpc/wallet_rpc_client.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.655987 chia-blockchain-1.8.1rc2/chia/seeder/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14746 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/crawl_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    17272 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/crawler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3913 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/crawler_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    10354 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/dns_server.py
--rw-r--r--   0 runner    (1001) docker     (123)     5420 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/peer_record.py
--rw-r--r--   0 runner    (1001) docker     (123)     2676 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/seeder/start_crawler.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.659987 chia-blockchain-1.8.1rc2/chia/server/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    27079 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/address_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/address_manager_sqlite_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     9764 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/address_manager_store.py
--rw-r--r--   0 runner    (1001) docker     (123)      720 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/capabilities.py
--rw-r--r--   0 runner    (1001) docker     (123)    14558 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/chia_policy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2430 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/introducer_peers.py
--rw-r--r--   0 runner    (1001) docker     (123)    33078 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/node_discovery.py
--rw-r--r--   0 runner    (1001) docker     (123)      820 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/outbound_message.py
--rw-r--r--   0 runner    (1001) docker     (123)     3471 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/peer_store_resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)    12583 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/rate_limit_numbers.py
--rw-r--r--   0 runner    (1001) docker     (123)     5013 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/rate_limits.py
--rw-r--r--   0 runner    (1001) docker     (123)    30966 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/server.py
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/ssl_context.py
--rw-r--r--   0 runner    (1001) docker     (123)     3979 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_data_layer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2978 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_farmer.py
--rw-r--r--   0 runner    (1001) docker     (123)     3863 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_full_node.py
--rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_harvester.py
--rw-r--r--   0 runner    (1001) docker     (123)     2017 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_introducer.py
--rw-r--r--   0 runner    (1001) docker     (123)    12376 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2722 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_timelord.py
--rw-r--r--   0 runner    (1001) docker     (123)     3704 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/start_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/upnp.py
--rw-r--r--   0 runner    (1001) docker     (123)    30397 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/server/ws_connection.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.667987 chia-blockchain-1.8.1rc2/chia/simulator/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    96083 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/block_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)    28844 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/full_node_simulator.py
--rw-r--r--   0 runner    (1001) docker     (123)     5689 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/keyring.py
--rw-r--r--   0 runner    (1001) docker     (123)    17193 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/setup_nodes.py
--rw-r--r--   0 runner    (1001) docker     (123)    15080 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/setup_services.py
--rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/simulator_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     5390 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/simulator_full_node_rpc_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     3062 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/simulator_full_node_rpc_client.py
--rw-r--r--   0 runner    (1001) docker     (123)      628 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/simulator_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     6462 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/simulator_test_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)      610 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/socket.py
--rw-r--r--   0 runner    (1001) docker     (123)     4904 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs.py
--rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_1.py
--rw-r--r--   0 runner    (1001) docker     (123)    39473 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_10.py
--rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_2.py
--rw-r--r--   0 runner    (1001) docker     (123)    39471 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_3.py
--rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_4.py
--rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_5.py
--rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_6.py
--rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_7.py
--rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_8.py
--rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_9.py
--rw-r--r--   0 runner    (1001) docker     (123)     4413 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/start_simulator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2956 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/time_out_assert.py
--rw-r--r--   0 runner    (1001) docker     (123)    10290 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/simulator/wallet_tools.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.667987 chia-blockchain-1.8.1rc2/chia/ssl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/ssl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/ssl/chia_ca.crt
--rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/ssl/chia_ca.key
--rw-r--r--   0 runner    (1001) docker     (123)     8874 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/ssl/create_ssl.py
--rw-r--r--   0 runner    (1001) docker     (123)     1200 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/ssl/dst_root_ca.pem
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.667987 chia-blockchain-1.8.1rc2/chia/timelord/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/iters_from_block.py
--rw-r--r--   0 runner    (1001) docker     (123)    58402 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/timelord.py
--rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/timelord_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     4102 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/timelord_launcher.py
--rw-r--r--   0 runner    (1001) docker     (123)    12052 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/timelord_state.py
--rw-r--r--   0 runner    (1001) docker     (123)      354 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/timelord/types.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.671987 chia-blockchain-1.8.1rc2/chia/types/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      718 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/announcement.py
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/block_protocol.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.675987 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1153 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/classgroup.py
--rw-r--r--   0 runner    (1001) docker     (123)      695 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/coin.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/foliage.py
--rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/pool_target.py
--rw-r--r--   0 runner    (1001) docker     (123)     7612 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/program.py
--rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/proof_of_space.py
--rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/reward_chain_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     4646 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/serialized_program.py
--rw-r--r--   0 runner    (1001) docker     (123)      388 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/sized_bytes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/slots.py
--rw-r--r--   0 runner    (1001) docker     (123)      678 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/sub_epoch_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/tree_hash.py
--rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/blockchain_format/vdf.py
--rw-r--r--   0 runner    (1001) docker     (123)      332 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/clvm_cost.py
--rw-r--r--   0 runner    (1001) docker     (123)     1284 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/coin_record.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/coin_solution.py
--rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/coin_spend.py
--rw-r--r--   0 runner    (1001) docker     (123)     1941 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/condition_opcodes.py
--rw-r--r--   0 runner    (1001) docker     (123)      493 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/condition_with_args.py
--rw-r--r--   0 runner    (1001) docker     (123)      560 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/end_of_slot_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)      854 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/fee_rate.py
--rw-r--r--   0 runner    (1001) docker     (123)     3585 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/full_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/generator_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     2475 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/header_block.py
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/mempool_inclusion_status.py
--rw-r--r--   0 runner    (1001) docker     (123)     2172 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/mempool_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/mempool_submission_status.py
--rw-r--r--   0 runner    (1001) docker     (123)      132 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/mojos.py
--rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/peer_info.py
--rw-r--r--   0 runner    (1001) docker     (123)      889 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/signing_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/spend_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)      173 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/spend_bundle_conditions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/transaction_queue_entry.py
--rw-r--r--   0 runner    (1001) docker     (123)     1972 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/unfinished_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     1527 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/unfinished_header_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3217 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/types/weight_proof.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.687987 chia-blockchain-1.8.1rc2/chia/util/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3046 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/api_decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)     4572 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/bech32m.py
--rw-r--r--   0 runner    (1001) docker     (123)     4249 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/beta_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)     3864 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/block_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     2190 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/byte_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     2899 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/cached_bls.py
--rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/check_fork_next_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     4862 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/chia_logging.py
--rw-r--r--   0 runner    (1001) docker     (123)      264 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/chunks.py
--rw-r--r--   0 runner    (1001) docker     (123)      323 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/collection.py
--rw-r--r--   0 runner    (1001) docker     (123)     4990 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/condition_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)    11508 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3642 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/create_alert_file.py
--rw-r--r--   0 runner    (1001) docker     (123)      575 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/db_synchronous.py
--rw-r--r--   0 runner    (1001) docker     (123)      936 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/db_version.py
--rw-r--r--   0 runner    (1001) docker     (123)    10201 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/db_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/default_root.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2866 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/dump_keyring.py
--rw-r--r--   0 runner    (1001) docker     (123)    13116 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/english.txt
--rw-r--r--   0 runner    (1001) docker     (123)     8871 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)    17393 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/file_keyring.py
--rw-r--r--   0 runner    (1001) docker     (123)     3251 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/files.py
--rw-r--r--   0 runner    (1001) docker     (123)    12119 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/full_block_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2911 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/generator_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/hash.py
--rw-r--r--   0 runner    (1001) docker     (123)    24251 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/initial-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      646 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/inline_executor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/ints.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/json_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    22225 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/keychain.py
--rw-r--r--   0 runner    (1001) docker     (123)    10459 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/keyring_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/limited_semaphore.py
--rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/lock.py
--rw-r--r--   0 runner    (1001) docker     (123)      364 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/log_exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)      918 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)      770 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/lru_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)      326 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/make_test_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/math.py
--rw-r--r--   0 runner    (1001) docker     (123)    10292 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/merkle_set.py
--rw-r--r--   0 runner    (1001) docker     (123)     3583 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/misc.py
--rw-r--r--   0 runner    (1001) docker     (123)     5899 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/network.py
--rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/paginator.py
--rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/partial_func.py
--rw-r--r--   0 runner    (1001) docker     (123)      702 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/path.py
--rw-r--r--   0 runner    (1001) docker     (123)      493 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/permissions.py
--rw-r--r--   0 runner    (1001) docker     (123)      884 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/pprint.py
--rw-r--r--   0 runner    (1001) docker     (123)      712 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/prev_transaction_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     6713 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/profiler.py
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/recursive_replace.py
--rw-r--r--   0 runner    (1001) docker     (123)      381 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/safe_cancel_task.py
--rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/service_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/setproctitle.py
--rw-r--r--   0 runner    (1001) docker     (123)      991 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/significant_bits.py
--rw-r--r--   0 runner    (1001) docker     (123)     8071 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/ssl_check.py
--rw-r--r--   0 runner    (1001) docker     (123)    23962 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/streamable.py
--rw-r--r--   0 runner    (1001) docker     (123)     3409 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/struct_stream.py
--rw-r--r--   0 runner    (1001) docker     (123)    10337 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/task_timing.py
--rw-r--r--   0 runner    (1001) docker     (123)     1775 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/validate_alert.py
--rw-r--r--   0 runner    (1001) docker     (123)     1042 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/vdf_prover.py
--rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/util/ws_message.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.699988 chia-blockchain-1.8.1rc2/chia/wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/block_record.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.711988 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      838 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_constants.py
--rw-r--r--   0 runner    (1001) docker     (123)      946 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     5270 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_outer_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     5496 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    42935 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/lineage_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2038 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/chialisp.py
--rw-r--r--   0 runner    (1001) docker     (123)     8815 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/coin_selection.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.711988 chia-blockchain-1.8.1rc2/chia/wallet/dao_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/dao_wallet/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.711988 chia-blockchain-1.8.1rc2/chia/wallet/db_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/db_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/db_wallet/db_wallet_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)      604 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/derivation_record.py
--rw-r--r--   0 runner    (1001) docker     (123)     4834 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/derive_keys.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.715988 chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1028 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_info.py
--rw-r--r--   0 runner    (1001) docker     (123)    62342 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     6587 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_wallet_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)     1003 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/driver_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     1779 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/key_val_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/lineage_proof.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.719987 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4406 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/metadata_outer_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     3190 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_info.py
--rw-r--r--   0 runner    (1001) docker     (123)    12066 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)    84011 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4556 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/ownership_outer_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     4478 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/singleton_outer_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     3349 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/transfer_program_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     7681 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/uncurry_nft.py
--rw-r--r--   0 runner    (1001) docker     (123)     4720 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/notification_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     6194 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/notification_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     4012 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/outer_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)     1088 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/payment.py
--rw-r--r--   0 runner    (1001) docker     (123)     3646 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzle_drivers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.771988 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      649 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/block_program_zero.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      340 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/block_program_zero.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/calculate_synthetic_public_key.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/calculate_synthetic_public_key.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      229 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_loader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_truths.clib
--rw-r--r--   0 runner    (1001) docker     (123)    16823 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_v2.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     3344 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_v2.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2425 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/chialisp_deserialisation.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      942 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/chialisp_deserialisation.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/condition_codes.clib
--rw-r--r--   0 runner    (1001) docker     (123)      553 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/create-lock-puzzlehash.clib
--rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/create_nft_launcher_from_did.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/create_nft_launcher_from_did.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     4002 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/curry-and-treehash.clib
--rw-r--r--   0 runner    (1001) docker     (123)     5264 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/curry.clib
--rw-r--r--   0 runner    (1001) docker     (123)      253 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_coin_spend_entry.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_coin_spend_entry.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_coin_spend_entry_with_prefix.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_coin_spend_entry_with_prefix.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_puzzle.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/decompress_puzzle.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      632 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/delegated_tail.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      360 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/delegated_tail.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     4042 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/deployed_puzzle_hashes.json
--rw-r--r--   0 runner    (1001) docker     (123)     6442 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/did_innerpuz.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     2024 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/did_innerpuz.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      318 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/everything_with_signature.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       82 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/everything_with_signature.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      527 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_coin_id.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_coin_id.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      587 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     3109 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/graftroot_dl_offers.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     1844 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/graftroot_dl_offers.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      830 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/json.clib
--rw-r--r--   0 runner    (1001) docker     (123)     5981 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/load_clvm.py
--rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/merkle_utils.clib
--rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_intermediate_launcher.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_intermediate_launcher.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      886 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_default.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      482 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_default.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      991 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     3796 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_layer.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     2452 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_layer.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     1374 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2976 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_state_layer.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_state_layer.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/notification.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      118 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/notification.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_conditions.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_conditions.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      757 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_conditions.py
--rw-r--r--   0 runner    (1001) docker     (123)      400 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_conditions.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_conditions.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      538 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_conditions.py
--rw-r--r--   0 runner    (1001) docker     (123)      478 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     3237 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      454 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     6979 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      906 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      645 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.py
--rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_parent.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      484 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_parent.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      434 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_puzzle_hash.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_puzzle_hash.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      853 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_puzzle_hash.py
--rw-r--r--   0 runner    (1001) docker     (123)     1540 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      806 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2463 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      992 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2727 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_member_innerpuz.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_member_innerpuz.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     2758 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      824 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp.hex
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.775988 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/make_prefarm_ph.py
--rw-r--r--   0 runner    (1001) docker     (123)     3687 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/spend_prefarm.py
--rw-r--r--   0 runner    (1001) docker     (123)     1957 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/puzzle_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1747 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/rom_bootstrap_generator.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     1474 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/rom_bootstrap_generator.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      280 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/rom_bootstrap_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1694 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      586 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     1551 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments_old.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments_old.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/sha256tree.clib
--rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/sha256tree_module.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/sha256tree_module.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      476 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_launcher.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      350 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_launcher.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)     7453 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     2336 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)    13022 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.py
--rw-r--r--   0 runner    (1001) docker     (123)     5022 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp
--rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)    12723 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     1371 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_truths.clib
--rw-r--r--   0 runner    (1001) docker     (123)     8082 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/tails.py
--rw-r--r--   0 runner    (1001) docker     (123)       89 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/test_generator_deserialize.clsp
--rw-r--r--   0 runner    (1001) docker     (123)       26 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/test_generator_deserialize.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp
--rw-r--r--   0 runner    (1001) docker     (123)      464 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp.hex
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/puzzles/utility_macros.clib
--rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/secret_key_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2883 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/sign_coin_spends.py
--rw-r--r--   0 runner    (1001) docker     (123)     2493 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/singleton.py
--rw-r--r--   0 runner    (1001) docker     (123)    43570 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trade_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2010 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trade_record.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.775988 chia-blockchain-1.8.1rc2/chia/wallet/trading/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trading/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    32738 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trading/offer.py
--rw-r--r--   0 runner    (1001) docker     (123)      206 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trading/trade_status.py
--rw-r--r--   0 runner    (1001) docker     (123)    20392 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/trading/trade_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     5029 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/transaction_record.py
--rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/transaction_sorting.py
--rw-r--r--   0 runner    (1001) docker     (123)      316 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/uncurried_puzzle.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.779988 chia-blockchain-1.8.1rc2/chia/wallet/util/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2003 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/address_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      821 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/compute_hints.py
--rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/compute_memos.py
--rw-r--r--   0 runner    (1001) docker     (123)     2066 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/curry_and_treehash.py
--rw-r--r--   0 runner    (1001) docker     (123)     7886 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/debug_spend_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)      582 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/json_clvm_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3673 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/merkle_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)     3478 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/merkle_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/new_peak_queue.py
--rw-r--r--   0 runner    (1001) docker     (123)      447 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/notifications.py
--rw-r--r--   0 runner    (1001) docker     (123)     7257 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/peer_request_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     6163 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/puzzle_compression.py
--rw-r--r--   0 runner    (1001) docker     (123)      224 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/transaction_type.py
--rw-r--r--   0 runner    (1001) docker     (123)    17157 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/wallet_sync_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      970 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/util/wallet_types.py
--rw-r--r--   0 runner    (1001) docker     (123)    27732 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_action.py
--rw-r--r--   0 runner    (1001) docker     (123)    10829 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_blockchain.py
--rw-r--r--   0 runner    (1001) docker     (123)      910 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_coin_record.py
--rw-r--r--   0 runner    (1001) docker     (123)     9214 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     4972 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_interested_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    12198 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_nft_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    79677 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_node.py
--rw-r--r--   0 runner    (1001) docker     (123)     8172 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_node_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     4346 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_pool_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)    13735 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_puzzle_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2048 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_retry_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    85577 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_state_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)    15012 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_transaction_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     4146 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_user_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     4932 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/chia/wallet/wallet_weight_proof_handler.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.779988 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    32249 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      771 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 03:10:28.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      926 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-13 03:16:39.000000 chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/top_level.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     6676 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/install-gui.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)     4910 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/install-plotter.sh
--rw-r--r--   0 runner    (1001) docker     (123)     5058 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/install-timelord.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)    12532 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/install.sh
--rw-r--r--   0 runner    (1001) docker     (123)     2033 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/installhelper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.783988 chia-blockchain-1.8.1rc2/mozilla-ca/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:10:03.000000 chia-blockchain-1.8.1rc2/mozilla-ca/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   216583 2023-05-13 03:10:03.000000 chia-blockchain-1.8.1rc2/mozilla-ca/cacert.pem
--rw-r--r--   0 runner    (1001) docker     (123)     7565 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/mypy.ini
--rw-r--r--   0 runner    (1001) docker     (123)    14885 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/pylintrc
--rw-r--r--   0 runner    (1001) docker     (123)      432 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/pytest.ini
--rwxr-xr-x   0 runner    (1001) docker     (123)      157 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/run-py-tests.sh
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 03:16:39.851989 chia-blockchain-1.8.1rc2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     5768 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/setup.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1303 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/start-gui.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.783988 chia-blockchain-1.8.1rc2/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     2318 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.783988 chia-blockchain-1.8.1rc2/tests/blockchain/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/blockchain/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6553 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/blockchain/blockchain_test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/blockchain/config.py
--rw-r--r--   0 runner    (1001) docker     (123)   167932 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/blockchain/test_blockchain.py
--rw-r--r--   0 runner    (1001) docker     (123)    37614 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/blockchain/test_blockchain_transactions.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2431 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/build-init-files.py
--rw-r--r--   0 runner    (1001) docker     (123)     4227 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/build-job-matrix.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      924 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/check_pytest_monitor_output.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2398 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/check_sql_statements.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1750 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/chia-start-sim
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.787988 chia-blockchain-1.8.1rc2/tests/clvm/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      824 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/benchmark_costs.py
--rw-r--r--   0 runner    (1001) docker     (123)     5060 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4523 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_chialisp_deserialization.py
--rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_clvm_step.py
--rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_curry_and_treehash.py
--rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_program.py
--rw-r--r--   0 runner    (1001) docker     (123)     5128 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_puzzle_compression.py
--rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_puzzle_drivers.py
--rw-r--r--   0 runner    (1001) docker     (123)     9715 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_serialized_program.py
--rw-r--r--   0 runner    (1001) docker     (123)    21532 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_singletons.py
--rw-r--r--   0 runner    (1001) docker     (123)     5315 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/clvm/test_spend_sim.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.787988 chia-blockchain-1.8.1rc2/tests/cmds/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/cmds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5570 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/cmds/test_sim.py
--rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/cmds/test_wallet_check.py
--rw-r--r--   0 runner    (1001) docker     (123)    28635 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     3817 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/connection_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.791988 chia-blockchain-1.8.1rc2/tests/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.791988 chia-blockchain-1.8.1rc2/tests/core/cmds/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/cmds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/cmds/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    13587 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/cmds/test_beta.py
--rw-r--r--   0 runner    (1001) docker     (123)    38994 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/cmds/test_keys.py
--rw-r--r--   0 runner    (1001) docker     (123)     4196 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/cmds/test_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.795988 chia-blockchain-1.8.1rc2/tests/core/consensus/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/consensus/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/consensus/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     5061 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/consensus/test_pot_iterations.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.795988 chia-blockchain-1.8.1rc2/tests/core/custom_types/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/custom_types/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/custom_types/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3543 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/custom_types/test_coin.py
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/custom_types/test_proof_of_space.py
--rw-r--r--   0 runner    (1001) docker     (123)     4135 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/custom_types/test_spend_bundle.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.795988 chia-blockchain-1.8.1rc2/tests/core/daemon/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/daemon/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/daemon/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    28618 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/daemon/test_daemon.py
--rw-r--r--   0 runner    (1001) docker     (123)     4037 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/daemon/test_daemon_register.py
--rw-r--r--   0 runner    (1001) docker     (123)     2550 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/daemon/test_keychain_proxy.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.799988 chia-blockchain-1.8.1rc2/tests/core/data_layer/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3865 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     3028 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_layer_util.py
--rw-r--r--   0 runner    (1001) docker     (123)   245364 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)    47306 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    14921 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_store_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     6746 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/data_layer/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.799988 chia-blockchain-1.8.1rc2/tests/core/full_node/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      173 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      591 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.799988 chia-blockchain-1.8.1rc2/tests/core/full_node/dos/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/dos/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/dos/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.799988 chia-blockchain-1.8.1rc2/tests/core/full_node/full_sync/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/full_sync/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/full_sync/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    19025 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/full_sync/test_full_sync.py
--rw-r--r--   0 runner    (1001) docker     (123)      855 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/ram_db.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.803988 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      151 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    13967 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_block_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    21322 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    34130 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_full_node_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     6877 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_hint_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2495 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_sync_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    23835 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_address_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)    16506 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_block_height_map.py
--rw-r--r--   0 runner    (1001) docker     (123)    13828 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_conditions.py
--rw-r--r--   0 runner    (1001) docker     (123)    87563 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_full_node.py
--rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_generator_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)     5513 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_hint_management.py
--rw-r--r--   0 runner    (1001) docker     (123)     1369 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_node_load.py
--rw-r--r--   0 runner    (1001) docker     (123)    10377 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_peer_store_resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)     7767 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_performance.py
--rw-r--r--   0 runner    (1001) docker     (123)    11698 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_subscriptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     7644 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_transactions.py
--rw-r--r--   0 runner    (1001) docker     (123)     5618 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/full_node/test_tx_processing_queue.py
--rw-r--r--   0 runner    (1001) docker     (123)   187863 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/large_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/make_block_generator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.803988 chia-blockchain-1.8.1rc2/tests/core/mempool/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/config.py
--rw-r--r--   0 runner    (1001) docker     (123)   123916 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool.py
--rw-r--r--   0 runner    (1001) docker     (123)     3626 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_fee_estimator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_fee_protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)    51540 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2942 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_performance.py
--rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/node_height.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.807988 chia-blockchain-1.8.1rc2/tests/core/server/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/flood.py
--rw-r--r--   0 runner    (1001) docker     (123)     2227 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/serve.py
--rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_capabilities.py
--rw-r--r--   0 runner    (1001) docker     (123)    11389 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_dos.py
--rw-r--r--   0 runner    (1001) docker     (123)     5612 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_event_loop.py
--rw-r--r--   0 runner    (1001) docker     (123)     9162 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_loop.py
--rw-r--r--   0 runner    (1001) docker     (123)    14687 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_rate_limits.py
--rw-r--r--   0 runner    (1001) docker     (123)     2251 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_server.py
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/server/test_upnp.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.807988 chia-blockchain-1.8.1rc2/tests/core/ssl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/ssl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/ssl/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     9973 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/ssl/test_ssl.py
--rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_coins.py
--rw-r--r--   0 runner    (1001) docker     (123)    11935 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_cost_calculation.py
--rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_crawler_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_daemon_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     5904 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_db_conversion.py
--rw-r--r--   0 runner    (1001) docker     (123)     5858 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_db_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)    23550 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_farmer_harvester_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)    19621 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_full_node_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     9905 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_merkle_set.py
--rw-r--r--   0 runner    (1001) docker     (123)     6312 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_services.py
--rw-r--r--   0 runner    (1001) docker     (123)      311 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/test_setproctitle.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.811988 chia-blockchain-1.8.1rc2/tests/core/util/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     2302 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_cached_bls.py
--rw-r--r--   0 runner    (1001) docker     (123)    13727 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4453 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_file_keyring_synchronization.py
--rw-r--r--   0 runner    (1001) docker     (123)    14641 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_files.py
--rw-r--r--   0 runner    (1001) docker     (123)     3545 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_jsonify.py
--rw-r--r--   0 runner    (1001) docker     (123)    20681 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_keychain.py
--rw-r--r--   0 runner    (1001) docker     (123)    22952 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_keyring_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)    14519 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_lockfile.py
--rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_lru_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_significant_bits.py
--rw-r--r--   0 runner    (1001) docker     (123)    29429 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/core/util/test_streamable.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.811988 chia-blockchain-1.8.1rc2/tests/db/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/db/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15542 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/db/test_db_wrapper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.811988 chia-blockchain-1.8.1rc2/tests/farmer_harvester/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/farmer_harvester/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/farmer_harvester/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     4299 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/farmer_harvester/test_farmer_harvester.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.811988 chia-blockchain-1.8.1rc2/tests/fee_estimation/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/cmdline_test.py
--rw-r--r--   0 runner    (1001) docker     (123)    10631 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)    11499 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     5145 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_unit_tests.py
--rw-r--r--   0 runner    (1001) docker     (123)     5873 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/fee_estimation/test_mempoolitem_height_added.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.815988 chia-blockchain-1.8.1rc2/tests/generator/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    14614 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/test_compression.py
--rw-r--r--   0 runner    (1001) docker     (123)     4207 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/test_generator_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     1060 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/test_list_to_batches.py
--rw-r--r--   0 runner    (1001) docker     (123)     6763 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/test_rom.py
--rw-r--r--   0 runner    (1001) docker     (123)     4142 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/generator/test_scan.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.815988 chia-blockchain-1.8.1rc2/tests/plot_sync/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3216 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/test_delta.py
--rw-r--r--   0 runner    (1001) docker     (123)    29365 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/test_plot_sync.py
--rw-r--r--   0 runner    (1001) docker     (123)    17905 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/test_receiver.py
--rw-r--r--   0 runner    (1001) docker     (123)     4917 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/test_sender.py
--rw-r--r--   0 runner    (1001) docker     (123)    18095 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/test_sync_simulated.py
--rw-r--r--   0 runner    (1001) docker     (123)     2395 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plot_sync/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.815988 chia-blockchain-1.8.1rc2/tests/plotting/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plotting/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plotting/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    32802 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plotting/test_plot_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)      316 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/plotting/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.815988 chia-blockchain-1.8.1rc2/tests/pools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_pool_cmdline.py
--rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_pool_config.py
--rw-r--r--   0 runner    (1001) docker     (123)    14572 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_pool_puzzles_lifecycle.py
--rw-r--r--   0 runner    (1001) docker     (123)    47244 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_pool_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)     7062 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_pool_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4421 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/pools/test_wallet_pool_store.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.823988 chia-blockchain-1.8.1rc2/tests/simulation/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/simulation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/simulation/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    21623 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/simulation/test_simulation.py
--rw-r--r--   0 runner    (1001) docker     (123)    10038 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/simulation/test_simulator.py
--rw-r--r--   0 runner    (1001) docker     (123)     5140 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/simulation/test_start_simulator.py
--rw-r--r--   0 runner    (1001) docker     (123)      433 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/testconfig.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.827988 chia-blockchain-1.8.1rc2/tests/tools/
--rw-r--r--   0 runner    (1001) docker     (123)    20462 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/1315537.json
--rw-r--r--   0 runner    (1001) docker     (123)    20277 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/1315544.json
--rw-r--r--   0 runner    (1001) docker     (123)    19672 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/1315630.json
--rw-r--r--   0 runner    (1001) docker     (123)    10501 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/300000.json
--rw-r--r--   0 runner    (1001) docker     (123)    17387 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/442734.json
--rw-r--r--   0 runner    (1001) docker     (123)   233251 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/466212.json
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/config.py
--rw-r--r--   0 runner    (1001) docker     (123)   405504 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/test-blockchain-db.sqlite
--rw-r--r--   0 runner    (1001) docker     (123)      700 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/test_full_sync.py
--rw-r--r--   0 runner    (1001) docker     (123)     3277 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/test_legacy_keyring.py
--rw-r--r--   0 runner    (1001) docker     (123)     4257 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/tools/test_run_block.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.831988 chia-blockchain-1.8.1rc2/tests/util/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2145 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/alert_server.py
--rw-r--r--   0 runner    (1001) docker     (123)     7104 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/benchmark_cost.py
--rw-r--r--   0 runner    (1001) docker     (123)     8592 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/bip39_test_vectors.json
--rw-r--r--   0 runner    (1001) docker     (123)     4245 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/blockchain.py
--rw-r--r--   0 runner    (1001) docker     (123)     9871 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/build_network_protocol_files.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      691 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/db_connection.py
--rw-r--r--   0 runner    (1001) docker     (123)     4328 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/gen_ssl_certs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/generator_tools_testing.py
--rw-r--r--   0 runner    (1001) docker     (123)     1603 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/key_tool.py
--rw-r--r--   0 runner    (1001) docker     (123)     9155 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/misc.py
--rw-r--r--   0 runner    (1001) docker     (123)    31159 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/network_protocol_data.py
--rw-r--r--   0 runner    (1001) docker     (123)    46740 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/protocol_messages_bytes-v1.0
--rw-r--r--   0 runner    (1001) docker     (123)   170660 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/protocol_messages_json.py
--rw-r--r--   0 runner    (1001) docker     (123)      692 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)      297 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/temp_file.py
--rw-r--r--   0 runner    (1001) docker     (123)      791 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_chunks.py
--rw-r--r--   0 runner    (1001) docker     (123)      353 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_collection.py
--rw-r--r--   0 runner    (1001) docker     (123)    11204 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_full_block_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1995 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_limited_semaphore.py
--rw-r--r--   0 runner    (1001) docker     (123)     2112 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_lock_queue.py
--rw-r--r--   0 runner    (1001) docker     (123)     1262 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_logging_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     3182 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_misc.py
--rw-r--r--   0 runner    (1001) docker     (123)     2993 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_network.py
--rw-r--r--   0 runner    (1001) docker     (123)    22379 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_files.py
--rw-r--r--   0 runner    (1001) docker     (123)    17774 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_json.py
--rw-r--r--   0 runner    (1001) docker     (123)     6811 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_test.py
--rw-r--r--   0 runner    (1001) docker     (123)     2346 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_paginator.py
--rw-r--r--   0 runner    (1001) docker     (123)      653 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_pprint.py
--rw-r--r--   0 runner    (1001) docker     (123)     9817 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_struct_stream.py
--rw-r--r--   0 runner    (1001) docker     (123)     1884 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/util/test_trusted_peer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.835988 chia-blockchain-1.8.1rc2/tests/wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.839989 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    25164 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_lifecycle.py
--rw-r--r--   0 runner    (1001) docker     (123)     2894 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_outer_puzzle.py
--rw-r--r--   0 runner    (1001) docker     (123)    39540 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)    14353 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_offer_lifecycle.py
--rw-r--r--   0 runner    (1001) docker     (123)   162923 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_trades.py
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.839989 chia-blockchain-1.8.1rc2/tests/wallet/dao_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/dao_wallet/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.839989 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     6363 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_db_graftroot.py
--rw-r--r--   0 runner    (1001) docker     (123)   135852 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_dl_offers.py
--rw-r--r--   0 runner    (1001) docker     (123)    26485 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_dl_wallet.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.839989 chia-blockchain-1.8.1rc2/tests/wallet/did_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/did_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/did_wallet/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    65884 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/did_wallet/test_did.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.843989 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/config.py
--rw-r--r--   0 runner    (1001) docker     (123)   374078 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_1_offers.py
--rw-r--r--   0 runner    (1001) docker     (123)    43345 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_bulk_mint.py
--rw-r--r--   0 runner    (1001) docker     (123)    15360 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_lifecycle.py
--rw-r--r--   0 runner    (1001) docker     (123)    66774 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_offers.py
--rw-r--r--   0 runner    (1001) docker     (123)     7544 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_puzzles.py
--rw-r--r--   0 runner    (1001) docker     (123)    76327 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3289 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_ownership_outer_puzzle.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.843989 chia-blockchain-1.8.1rc2/tests/wallet/rpc/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/rpc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/rpc/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    10128 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/rpc/test_dl_wallet_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)    74646 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/rpc/test_wallet_rpc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.843989 chia-blockchain-1.8.1rc2/tests/wallet/simple_sync/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/simple_sync/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/simple_sync/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    32900 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/simple_sync/test_simple_sync_protocol.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.847989 chia-blockchain-1.8.1rc2/tests/wallet/sync/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/sync/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/sync/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    65909 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/sync/test_wallet_sync.py
--rw-r--r--   0 runner    (1001) docker     (123)     7270 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_address_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1373 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_bech32m.py
--rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_chialisp.py
--rw-r--r--   0 runner    (1001) docker     (123)    22800 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_coin_selection.py
--rw-r--r--   0 runner    (1001) docker     (123)     6821 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_nft_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     8130 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_notifications.py
--rw-r--r--   0 runner    (1001) docker     (123)    13649 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_offer_parsing_performance.py
--rw-r--r--   0 runner    (1001) docker     (123)     2989 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_puzzle_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     4993 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_singleton.py
--rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_singleton_lifecycle.py
--rw-r--r--   0 runner    (1001) docker     (123)    30445 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_singleton_lifecycle_fast.py
--rw-r--r--   0 runner    (1001) docker     (123)      796 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_taproot.py
--rw-r--r--   0 runner    (1001) docker     (123)    28752 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_transaction_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    43806 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4257 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_blockchain.py
--rw-r--r--   0 runner    (1001) docker     (123)    14603 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_coin_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_interested_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1617 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_key_val_store.py
--rw-r--r--   0 runner    (1001) docker     (123)    17353 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_node.py
--rw-r--r--   0 runner    (1001) docker     (123)     4254 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_retry.py
--rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_state_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_trade_store.py
--rw-r--r--   0 runner    (1001) docker     (123)     1175 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_user_store.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.847989 chia-blockchain-1.8.1rc2/tests/weight_proof/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/weight_proof/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/weight_proof/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    22920 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tests/weight_proof/test_weight_proof.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 03:16:39.847989 chia-blockchain-1.8.1rc2/tools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/__init__.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     5772 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/analyze-chain.py
--rw-r--r--   0 runner    (1001) docker     (123)     6897 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/analyze_memory_profile.py
--rw-r--r--   0 runner    (1001) docker     (123)     3575 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/cpu_utilization.py
--rw-r--r--   0 runner    (1001) docker     (123)     8837 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/generate_chain.py
--rw-r--r--   0 runner    (1001) docker     (123)     4707 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/legacy_keyring.py
--rw-r--r--   0 runner    (1001) docker     (123)    13826 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/manage_clvm.py
--rw-r--r--   0 runner    (1001) docker     (123)     1024 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/plot-log.gnuplot
--rwxr-xr-x   0 runner    (1001) docker     (123)      791 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/run_benchmark.sh
--rw-r--r--   0 runner    (1001) docker     (123)     8880 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/run_block.py
--rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/test_constants.py
--rwxr-xr-x   0 runner    (1001) docker     (123)    13441 2023-05-13 03:09:54.000000 chia-blockchain-1.8.1rc2/tools/test_full_sync.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.986339 chia-blockchain-2.0.0b1/
+-rw-r--r--   0 runner    (1001) docker     (123)      252 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.coveragerc
+-rw-r--r--   0 runner    (1001) docker     (123)      293 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.842338 chia-blockchain-2.0.0b1/.github/
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/CODEOWNERS
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.842338 chia-blockchain-2.0.0b1/.github/ISSUE_TEMPLATE/
+-rw-r--r--   0 runner    (1001) docker     (123)     1406 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/ISSUE_TEMPLATE/bug_report.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/ISSUE_TEMPLATE/config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/PULL_REQUEST_TEMPLATE.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.834338 chia-blockchain-2.0.0b1/.github/actions/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.842338 chia-blockchain-2.0.0b1/.github/actions/install/
+-rw-r--r--   0 runner    (1001) docker     (123)     1391 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/actions/install/action.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1006 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/dependabot.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      435 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/release.yml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.846338 chia-blockchain-2.0.0b1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2213 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/benchmarks.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    12246 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/build-linux-arm64-installer.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    12139 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/build-linux-installer-deb.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    12226 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/build-linux-installer-rpm.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    13442 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/build-macos-installers.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    13299 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/build-windows-installer.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/check-commit-signing.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2093 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/check_wheel_availability.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2758 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1036 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/conflict-check.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      335 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/daily-matrix.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/dependency-review.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1338 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/mozilla-ca-cert.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2065 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/pre-commit.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      699 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/require-labels.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2226 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/snyk-python-scan.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1434 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/stale-issue.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/start-release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      899 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/start-sync-test.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2383 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/super-linter.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     6612 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/test-install-scripts.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     8783 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/test-single.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     5757 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/test.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/trigger-docker-dev.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1023 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/trigger-docker-main.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.github/workflows/upload-pypi-source.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     5420 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.gitmodules
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.isort.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1009 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.markdown-lint.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2100 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/BUILD_TIMELORD.md
+-rw-r--r--   0 runner    (1001) docker     (123)   209772 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     3477 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/CODE_OF_CONDUCT.md
+-rw-r--r--   0 runner    (1001) docker     (123)     8356 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/CONTRIBUTING.md
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/INSTALL.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1179 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/Install-gui.ps1
+-rw-r--r--   0 runner    (1001) docker     (123)     5155 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/Install-plotter.ps1
+-rw-r--r--   0 runner    (1001) docker     (123)     3770 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/Install.ps1
+-rw-r--r--   0 runner    (1001) docker     (123)    11342 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4952 2023-05-09 02:17:12.982339 chia-blockchain-2.0.0b1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    33099 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/PRETTY_GOOD_PRACTICES.md
+-rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      701 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/SECURITY.md
+-rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/activated.ps1
+-rwxr-xr-x   0 runner    (1001) docker     (123)      630 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/activated.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      155 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/activated.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.846338 chia-blockchain-2.0.0b1/benchmarks/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/block_ref.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14354 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/block_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)   121543 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/clvm_generator.bin
+-rw-r--r--   0 runner    (1001) docker     (123)     9537 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/jsonify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5062 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/mempool-long-lived.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11229 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/mempool.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11782 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/streamable.py
+-rw-r--r--   0 runner    (1001) docker     (123)   439288 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/transaction_height_delta
+-rw-r--r--   0 runner    (1001) docker     (123)     6327 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/benchmarks/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.846338 chia-blockchain-2.0.0b1/build_scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/assets/deb/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/deb/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      277 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/deb/control.j2
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/deb/postinst.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/deb/prerm.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/assets/dmg/
+-rw-r--r--   0 runner    (1001) docker     (123)      315 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/dmg/README
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/dmg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   507222 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/dmg/background.tiff
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/assets/rpm/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/rpm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/rpm/postinst.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      178 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/assets/rpm/prerm.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     1328 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_linux_deb-1-gui.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     4684 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_linux_deb-2-installer.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_linux_rpm-1-gui.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     3818 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_linux_rpm-2-installer.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     1350 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_macos-1-gui.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     3416 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_macos-2-installer.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_windows-1-gui.ps1
+-rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/build_windows-2-installer.ps1
+-rw-r--r--   0 runner    (1001) docker     (123)     2218 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/check_dependency_artifacts.py
+-rw-r--r--   0 runner    (1001) docker     (123)      907 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/clean-runner.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/installer-version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/npm_global/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_global/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      342 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_global/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      267 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_global/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/npm_linux/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_linux/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   539731 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_linux/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      305 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_linux/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.850338 chia-blockchain-2.0.0b1/build_scripts/npm_macos/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_macos/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   572329 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_macos/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      379 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_macos/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.854338 chia-blockchain-2.0.0b1/build_scripts/npm_windows/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_windows/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   553007 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_windows/package-lock.json
+-rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/build_scripts/npm_windows/package.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.854338 chia-blockchain-2.0.0b1/chia/
+-rw-r--r--   0 runner    (1001) docker     (123)      347 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       76 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/__main__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.854338 chia-blockchain-2.0.0b1/chia/clvm/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/clvm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/clvm/singleton.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18471 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/clvm/spend_sim.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.858338 chia-blockchain-2.0.0b1/chia/cmds/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7240 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/beta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4705 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/beta_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16346 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/check_wallet_db.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4564 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/chia.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9461 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/cmds_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10675 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/coin_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6716 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/coins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1387 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/completion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13235 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/configure.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11323 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8267 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/data_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2937 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/db.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3341 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/db_backup_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17725 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/db_upgrade_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7802 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/db_validate_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)      244 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/dev.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2168 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/farm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8240 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/farm_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2079 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/init.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16283 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/init_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14964 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/keys.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26855 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/keys_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1291 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/netspace.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2737 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/netspace_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4784 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/passphrase.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12569 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/passphrase_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/peer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5306 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/peer_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8138 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/plotnft.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17241 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/plotnft_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7200 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/plots.py
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/plotters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4730 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2413 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/show.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9793 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/show_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7797 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/sim.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22264 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/sim_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      782 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/start.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3452 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/start_funcs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2025 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/stop.py
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/units.py
+-rw-r--r--   0 runner    (1001) docker     (123)    45984 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    53117 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/cmds/wallet_funcs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.862338 chia-blockchain-2.0.0b1/chia/consensus/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22930 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_body_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21437 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_creation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    51189 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_header_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4805 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_rewards.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/block_root_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42752 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/blockchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3725 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/blockchain_interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1201 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/coinbase.py
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/condition_costs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4446 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)      517 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/cost_calculator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3699 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/default_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2183 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/deficit.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18266 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/difficulty_adjustment.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1253 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/find_fork_point.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6609 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/full_block_to_block_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4823 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/get_block_challenge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7852 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/make_sub_epoch_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18835 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/multiprocess_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)      788 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/pos_quality.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/pot_iterations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6971 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/consensus/vdf_info_computation.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.862338 chia-blockchain-2.0.0b1/chia/daemon/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7977 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18190 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/keychain_proxy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11125 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/keychain_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)    55454 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/server.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/daemon/windows_signal.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.862338 chia-blockchain-2.0.0b1/chia/data_layer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40675 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      696 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1143 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer_errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4996 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18391 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    61922 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_layer_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    62999 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/data_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13650 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/dl_wallet_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8556 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/download_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1136 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/s3_plugin_config.yml
+-rw-r--r--   0 runner    (1001) docker     (123)    16377 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/s3_plugin_service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.862338 chia-blockchain-2.0.0b1/chia/data_layer/util/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4716 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/data_layer/util/benchmark.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.862338 chia-blockchain-2.0.0b1/chia/farmer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/farmer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    36468 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/farmer/farmer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28233 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/farmer/farmer_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.866338 chia-blockchain-2.0.0b1/chia/full_node/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/bitcoin_fee_estimator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9689 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/block_height_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32512 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/block_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6305 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/bundle_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24796 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimate.py
+-rw-r--r--   0 runner    (1001) docker     (123)      526 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimate_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2922 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1235 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1955 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_example.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1606 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_interface.py
+-rw-r--r--   0 runner    (1001) docker     (123)      610 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_history.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22559 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/fee_tracker.py
+-rw-r--r--   0 runner    (1001) docker     (123)   130083 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/full_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)    79298 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/full_node_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    36689 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/full_node_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2446 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2731 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/hint_management.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2524 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/hint_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2854 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/lock_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18041 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/mempool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6167 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/mempool_check_conditions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33511 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/mempool_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3670 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/pending_tx_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)      414 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/signage_point.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5619 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/subscriptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/sync_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3335 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/tx_processing_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)    72530 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/full_node/weight_proof.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.866338 chia-blockchain-2.0.0b1/chia/harvester/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/harvester/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7862 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/harvester/harvester.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15433 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/harvester/harvester_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.866338 chia-blockchain-2.0.0b1/chia/introducer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/introducer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4173 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/introducer/introducer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2009 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/introducer/introducer_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.866338 chia-blockchain-2.0.0b1/chia/plot_sync/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/delta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2306 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14237 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/receiver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13867 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/sender.py
+-rw-r--r--   0 runner    (1001) docker     (123)      825 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plot_sync/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.870338 chia-blockchain-2.0.0b1/chia/plotters/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11146 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/bladebit.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1893 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/chiapos.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7591 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/madmax.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16640 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/plotters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4050 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotters/plotters_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.870338 chia-blockchain-2.0.0b1/chia/plotting/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7803 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9712 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/check_plots.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10542 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/create_plots.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16154 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9139 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/plotting/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.870338 chia-blockchain-2.0.0b1/chia/pools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3893 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pools/pool_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17113 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pools/pool_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44558 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pools/pool_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4535 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pools/pool_wallet_info.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.870338 chia-blockchain-2.0.0b1/chia/protocols/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1841 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/farmer_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4276 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/full_node_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4283 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/harvester_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)      600 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/introducer_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4059 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/pool_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/protocol_message_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/protocol_state_machine.py
+-rw-r--r--   0 runner    (1001) docker     (123)      235 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/protocol_timing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/shared_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3111 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/timelord_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5768 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/protocols/wallet_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     5617 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/pyinstaller.spec
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.874338 chia-blockchain-2.0.0b1/chia/rpc/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2640 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/crawler_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18476 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5321 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2003 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13582 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/farmer_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3989 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/farmer_rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41325 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/full_node_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12300 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/full_node_rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3084 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/harvester_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/harvester_rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3396 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17016 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/rpc_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)      863 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/timelord_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/util.py
+-rw-r--r--   0 runner    (1001) docker     (123)   161377 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/wallet_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46122 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/rpc/wallet_rpc_client.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.874338 chia-blockchain-2.0.0b1/chia/seeder/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14746 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/crawl_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17272 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/crawler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3913 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/crawler_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10354 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/dns_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5420 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/peer_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2676 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/seeder/start_crawler.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.878338 chia-blockchain-2.0.0b1/chia/server/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27079 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/address_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/address_manager_sqlite_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9764 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/address_manager_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)      720 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/capabilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14558 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/chia_policy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2430 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/introducer_peers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33078 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/node_discovery.py
+-rw-r--r--   0 runner    (1001) docker     (123)      820 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/outbound_message.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3471 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/peer_store_resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12583 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/rate_limit_numbers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5013 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/rate_limits.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30966 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/server.py
+-rw-r--r--   0 runner    (1001) docker     (123)      867 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/ssl_context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3979 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_data_layer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2978 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_farmer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3949 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_full_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_harvester.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2017 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_introducer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12376 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2722 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_timelord.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3704 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/start_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/upnp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30397 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/server/ws_connection.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.878338 chia-blockchain-2.0.0b1/chia/simulator/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    96083 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/block_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28763 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/full_node_simulator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5689 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/keyring.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17193 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/setup_nodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15080 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/setup_services.py
+-rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/simulator_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5390 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/simulator_full_node_rpc_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3062 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/simulator_full_node_rpc_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      628 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/simulator_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6462 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/simulator_test_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)      610 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/socket.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4904 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39473 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_10.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_2.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39471 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_3.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_4.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_5.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39483 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_6.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_7.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_8.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39479 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_9.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4413 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/start_simulator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2956 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/time_out_assert.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10290 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/simulator/wallet_tools.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.878338 chia-blockchain-2.0.0b1/chia/ssl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/ssl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/ssl/chia_ca.crt
+-rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/ssl/chia_ca.key
+-rw-r--r--   0 runner    (1001) docker     (123)     8874 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/ssl/create_ssl.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1200 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/ssl/dst_root_ca.pem
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.882338 chia-blockchain-2.0.0b1/chia/timelord/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/iters_from_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)    58402 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/timelord.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/timelord_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4102 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/timelord_launcher.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12052 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/timelord_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)      354 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/timelord/types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.882338 chia-blockchain-2.0.0b1/chia/types/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      718 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/announcement.py
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/block_protocol.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.886338 chia-blockchain-2.0.0b1/chia/types/blockchain_format/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1153 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/classgroup.py
+-rw-r--r--   0 runner    (1001) docker     (123)      695 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/coin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/foliage.py
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/pool_target.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7612 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/program.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/proof_of_space.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1962 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/reward_chain_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4646 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/serialized_program.py
+-rw-r--r--   0 runner    (1001) docker     (123)      388 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/sized_bytes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/slots.py
+-rw-r--r--   0 runner    (1001) docker     (123)      678 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/sub_epoch_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2006 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/tree_hash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/blockchain_format/vdf.py
+-rw-r--r--   0 runner    (1001) docker     (123)      332 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/clvm_cost.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1284 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/coin_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/coin_solution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/coin_spend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1941 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/condition_opcodes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/condition_with_args.py
+-rw-r--r--   0 runner    (1001) docker     (123)      560 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/end_of_slot_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)      854 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/fee_rate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3585 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/full_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/generator_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2475 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/header_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/mempool_inclusion_status.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/mempool_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1055 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/mempool_submission_status.py
+-rw-r--r--   0 runner    (1001) docker     (123)      132 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/mojos.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/peer_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)      889 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/signing_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/spend_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)      173 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/spend_bundle_conditions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/transaction_queue_entry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1972 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/unfinished_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1527 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/unfinished_header_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3217 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/types/weight_proof.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.890338 chia-blockchain-2.0.0b1/chia/util/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3046 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/api_decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4572 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/bech32m.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4249 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/beta_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3864 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/block_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2190 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/byte_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2899 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/cached_bls.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1408 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/check_fork_next_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4862 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/chia_logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)      264 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/chunks.py
+-rw-r--r--   0 runner    (1001) docker     (123)      323 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/collection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4990 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/condition_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11508 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3642 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/create_alert_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)      575 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/db_synchronous.py
+-rw-r--r--   0 runner    (1001) docker     (123)      936 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/db_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10201 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/db_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/default_root.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2866 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/dump_keyring.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13116 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/english.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     8871 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17393 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/file_keyring.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3251 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/files.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12119 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/full_block_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2911 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/generator_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/hash.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24263 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/initial-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      646 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/inline_executor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/ints.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/json_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22225 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/keychain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10459 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/keyring_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1013 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/limited_semaphore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/lock.py
+-rw-r--r--   0 runner    (1001) docker     (123)      722 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/log_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      918 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)      770 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/lru_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)      326 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/make_test_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)      463 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/math.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10292 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/merkle_set.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3933 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5899 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/network.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1593 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/paginator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      622 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/partial_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)      702 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/path.py
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/permissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      884 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/pprint.py
+-rw-r--r--   0 runner    (1001) docker     (123)      712 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/prev_transaction_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6713 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/profiler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/recursive_replace.py
+-rw-r--r--   0 runner    (1001) docker     (123)      381 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/safe_cancel_task.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1501 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/service_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/setproctitle.py
+-rw-r--r--   0 runner    (1001) docker     (123)      991 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/significant_bits.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8071 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/ssl_check.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23962 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/streamable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3409 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/struct_stream.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10459 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/task_timing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1775 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/validate_alert.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1042 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/vdf_prover.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/util/ws_message.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.894338 chia-blockchain-2.0.0b1/chia/wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/block_record.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.894338 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      838 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)      946 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5270 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_outer_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5496 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42795 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/lineage_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2038 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/chialisp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8624 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/coin_selection.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.898338 chia-blockchain-2.0.0b1/chia/wallet/dao_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/dao_wallet/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.898338 chia-blockchain-2.0.0b1/chia/wallet/db_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/db_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/db_wallet/db_wallet_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)      604 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/derivation_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4834 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/derive_keys.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.898338 chia-blockchain-2.0.0b1/chia/wallet/did_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/did_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1028 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)    61765 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6587 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_wallet_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1003 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/driver_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1779 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/key_val_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/lineage_proof.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.898338 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4406 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/metadata_outer_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3190 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12066 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)    82710 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4556 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/ownership_outer_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4478 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/singleton_outer_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3349 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/transfer_program_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7681 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/uncurry_nft.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4720 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/notification_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6194 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/notification_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4012 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/outer_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1125 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/payment.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3646 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzle_drivers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.910338 chia-blockchain-2.0.0b1/chia/wallet/puzzles/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      649 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/block_program_zero.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      340 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/block_program_zero.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/calculate_synthetic_public_key.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       34 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/calculate_synthetic_public_key.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_loader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_truths.clib
+-rw-r--r--   0 runner    (1001) docker     (123)    16823 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_v2.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     3344 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_v2.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2425 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/chialisp_deserialisation.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      942 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/chialisp_deserialisation.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/condition_codes.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      553 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/create-lock-puzzlehash.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/create_nft_launcher_from_did.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/create_nft_launcher_from_did.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     4002 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/curry-and-treehash.clib
+-rw-r--r--   0 runner    (1001) docker     (123)     5264 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/curry.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      253 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_coin_spend_entry.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_coin_spend_entry.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_coin_spend_entry_with_prefix.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_coin_spend_entry_with_prefix.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_puzzle.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       42 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/decompress_puzzle.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      632 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/delegated_tail.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      360 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/delegated_tail.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     4142 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/deployed_puzzle_hashes.json
+-rw-r--r--   0 runner    (1001) docker     (123)     6442 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/did_innerpuz.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     2024 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/did_innerpuz.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      318 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/everything_with_signature.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       82 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/everything_with_signature.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      527 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_coin_id.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       90 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_coin_id.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      587 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     3109 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/graftroot_dl_offers.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     1844 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/graftroot_dl_offers.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      830 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/json.clib
+-rw-r--r--   0 runner    (1001) docker     (123)     5981 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/load_clvm.py
+-rw-r--r--   0 runner    (1001) docker     (123)      547 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/merkle_utils.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      190 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_intermediate_launcher.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_intermediate_launcher.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      886 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_default.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      482 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_default.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      991 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      406 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     3796 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_layer.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     2452 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_layer.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     1374 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2976 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_state_layer.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_state_layer.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/notification.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      118 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/notification.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)       56 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_conditions.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_conditions.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      757 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_conditions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      400 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_conditions.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      274 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_conditions.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      538 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_conditions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      478 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3237 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      454 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     6979 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      906 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      645 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.py
+-rw-r--r--   0 runner    (1001) docker     (123)      384 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_parent.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      484 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_parent.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      434 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_puzzle_hash.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      286 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_puzzle_hash.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      853 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_puzzle_hash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1540 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      806 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2463 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      992 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2727 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_member_innerpuz.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      752 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_member_innerpuz.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     2758 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      824 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp.hex
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.910338 chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/make_prefarm_ph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3687 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/spend_prefarm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1919 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/puzzle_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1747 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     1474 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      386 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1116 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator2.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator2.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator2.clsp.hex.sha256tree
+-rw-r--r--   0 runner    (1001) docker     (123)     1694 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      586 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     1551 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments_old.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      534 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments_old.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      262 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/sha256tree.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      307 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/sha256tree_module.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/sha256tree_module.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      476 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_launcher.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      350 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_launcher.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)     7453 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     2336 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)    13022 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5022 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)    12723 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1371 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_truths.clib
+-rw-r--r--   0 runner    (1001) docker     (123)     8074 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/tails.py
+-rw-r--r--   0 runner    (1001) docker     (123)       89 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/test_generator_deserialize.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)       26 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/test_generator_deserialize.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      794 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp
+-rw-r--r--   0 runner    (1001) docker     (123)      464 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp.hex
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/puzzles/utility_macros.clib
+-rw-r--r--   0 runner    (1001) docker     (123)      595 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/secret_key_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2883 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/sign_coin_spends.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2493 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/singleton.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43782 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trade_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2010 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trade_record.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.910338 chia-blockchain-2.0.0b1/chia/wallet/trading/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trading/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32734 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trading/offer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      206 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trading/trade_status.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20392 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/trading/trade_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5029 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/transaction_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/transaction_sorting.py
+-rw-r--r--   0 runner    (1001) docker     (123)      316 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/uncurried_puzzle.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.910338 chia-blockchain-2.0.0b1/chia/wallet/util/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2003 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/address_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      821 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/compute_hints.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/compute_memos.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2066 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/curry_and_treehash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7886 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/debug_spend_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)      582 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/json_clvm_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3673 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/merkle_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3478 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/merkle_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/new_peak_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)      447 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/notifications.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7257 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/peer_request_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6163 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/puzzle_compression.py
+-rw-r--r--   0 runner    (1001) docker     (123)      224 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/transaction_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17158 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/wallet_sync_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1058 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/util/wallet_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26906 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_action.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10829 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_blockchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2826 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_coin_record.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16488 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4972 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_interested_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12463 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_nft_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    79568 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8172 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_node_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4346 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_pool_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13735 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_puzzle_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2048 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_retry_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    86445 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_state_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15012 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_transaction_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4146 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_user_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4932 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/chia/wallet/wallet_weight_proof_handler.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.914338 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4952 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    32457 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      771 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 02:15:21.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      935 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-05-09 02:17:12.000000 chia-blockchain-2.0.0b1/chia_blockchain.egg-info/top_level.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     6676 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/install-gui.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4910 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/install-plotter.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     5058 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/install-timelord.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)    12532 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/install.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     2033 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/installhelper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.914338 chia-blockchain-2.0.0b1/mozilla-ca/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:56.000000 chia-blockchain-2.0.0b1/mozilla-ca/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   216583 2023-05-09 02:14:56.000000 chia-blockchain-2.0.0b1/mozilla-ca/cacert.pem
+-rw-r--r--   0 runner    (1001) docker     (123)     7464 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/mypy.ini
+-rw-r--r--   0 runner    (1001) docker     (123)    14885 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/pylintrc
+-rw-r--r--   0 runner    (1001) docker     (123)      432 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1739 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/pytest.ini
+-rwxr-xr-x   0 runner    (1001) docker     (123)      157 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/run-py-tests.sh
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-09 02:17:12.986339 chia-blockchain-2.0.0b1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     5844 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/setup.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1303 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/start-gui.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.914338 chia-blockchain-2.0.0b1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2318 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.914338 chia-blockchain-2.0.0b1/tests/blockchain/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/blockchain/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6553 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/blockchain/blockchain_test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/blockchain/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)   167932 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/blockchain/test_blockchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39815 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/blockchain/test_blockchain_transactions.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2786 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/build-init-files.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4227 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/build-job-matrix.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      924 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/check_pytest_monitor_output.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2398 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/check_sql_statements.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1750 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/chia-start-sim
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.914338 chia-blockchain-2.0.0b1/tests/clvm/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      824 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/benchmark_costs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5060 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4523 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_chialisp_deserialization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_clvm_step.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_curry_and_treehash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3588 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_program.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5128 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_puzzle_compression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_puzzle_drivers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9713 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_serialized_program.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21532 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_singletons.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5315 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/clvm/test_spend_sim.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.918338 chia-blockchain-2.0.0b1/tests/cmds/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/cmds/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5570 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/cmds/test_sim.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3424 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/cmds/test_wallet_check.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28635 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3817 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/connection_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.918338 chia-blockchain-2.0.0b1/tests/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.918338 chia-blockchain-2.0.0b1/tests/core/cmds/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/cmds/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/cmds/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13587 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/cmds/test_beta.py
+-rw-r--r--   0 runner    (1001) docker     (123)    38994 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/cmds/test_keys.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4196 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/cmds/test_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.918338 chia-blockchain-2.0.0b1/tests/core/consensus/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/consensus/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/consensus/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5061 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/consensus/test_pot_iterations.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.918338 chia-blockchain-2.0.0b1/tests/core/custom_types/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/custom_types/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/custom_types/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3543 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/custom_types/test_coin.py
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/custom_types/test_proof_of_space.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4135 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/custom_types/test_spend_bundle.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.922339 chia-blockchain-2.0.0b1/tests/core/daemon/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/daemon/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/daemon/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28618 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/daemon/test_daemon.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4037 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/daemon/test_daemon_register.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2550 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/daemon/test_keychain_proxy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.922339 chia-blockchain-2.0.0b1/tests/core/data_layer/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3865 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3028 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_layer_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)   245364 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    47306 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14921 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_store_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6746 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/data_layer/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.922339 chia-blockchain-2.0.0b1/tests/core/full_node/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      173 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      591 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.922339 chia-blockchain-2.0.0b1/tests/core/full_node/dos/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/dos/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/dos/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.922339 chia-blockchain-2.0.0b1/tests/core/full_node/full_sync/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/full_sync/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/full_sync/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19025 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/full_sync/test_full_sync.py
+-rw-r--r--   0 runner    (1001) docker     (123)      855 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/ram_db.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.926339 chia-blockchain-2.0.0b1/tests/core/full_node/stores/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      151 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13967 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_block_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21322 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    34130 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_full_node_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6877 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_hint_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2495 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_sync_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23835 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_address_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16506 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_block_height_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13828 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_conditions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    87563 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_full_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_generator_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5513 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_hint_management.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1369 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_node_load.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10377 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_peer_store_resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7767 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_performance.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11698 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_subscriptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7644 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_transactions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5618 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/full_node/test_tx_processing_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)   187863 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/large_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/make_block_generator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.926339 chia-blockchain-2.0.0b1/tests/core/mempool/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)   125253 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3626 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_fee_estimator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_fee_protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)    51535 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2942 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_performance.py
+-rw-r--r--   0 runner    (1001) docker     (123)      594 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/node_height.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.926339 chia-blockchain-2.0.0b1/tests/core/server/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      934 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/flood.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2227 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/serve.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_capabilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11389 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_dos.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5612 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_event_loop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9162 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_loop.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14687 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_rate_limits.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2251 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)      186 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/server/test_upnp.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.926339 chia-blockchain-2.0.0b1/tests/core/ssl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/ssl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/ssl/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9973 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/ssl/test_ssl.py
+-rw-r--r--   0 runner    (1001) docker     (123)      890 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_coins.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11935 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_cost_calculation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_crawler_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)      711 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_daemon_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5904 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_db_conversion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5858 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_db_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23550 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_farmer_harvester_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1191 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19621 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_full_node_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9905 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_merkle_set.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6312 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_services.py
+-rw-r--r--   0 runner    (1001) docker     (123)      311 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/test_setproctitle.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.930338 chia-blockchain-2.0.0b1/tests/core/util/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2302 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_cached_bls.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13727 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4453 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_file_keyring_synchronization.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14641 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_files.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3545 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_jsonify.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20681 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_keychain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22952 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_keyring_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14519 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_lockfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6370 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_log_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1682 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_lru_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_significant_bits.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29429 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/core/util/test_streamable.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.930338 chia-blockchain-2.0.0b1/tests/db/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/db/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15542 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/db/test_db_wrapper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.930338 chia-blockchain-2.0.0b1/tests/farmer_harvester/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/farmer_harvester/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/farmer_harvester/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4299 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/farmer_harvester/test_farmer_harvester.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.934339 chia-blockchain-2.0.0b1/tests/fee_estimation/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      977 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/cmdline_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10631 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11499 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5145 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_unit_tests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5873 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/fee_estimation/test_mempoolitem_height_added.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.938339 chia-blockchain-2.0.0b1/tests/generator/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14614 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/test_compression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4207 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/test_generator_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1060 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/test_list_to_batches.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6763 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/test_rom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4142 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/generator/test_scan.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.938339 chia-blockchain-2.0.0b1/tests/plot_sync/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3216 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/test_delta.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29365 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/test_plot_sync.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17905 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/test_receiver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4917 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/test_sender.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18095 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/test_sync_simulated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2395 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plot_sync/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.942339 chia-blockchain-2.0.0b1/tests/plotting/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plotting/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plotting/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32802 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plotting/test_plot_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)      316 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/plotting/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.942339 chia-blockchain-2.0.0b1/tests/pools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       99 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_pool_cmdline.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1786 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_pool_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14572 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_pool_puzzles_lifecycle.py
+-rw-r--r--   0 runner    (1001) docker     (123)    47252 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_pool_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7062 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_pool_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4421 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/pools/test_wallet_pool_store.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.946339 chia-blockchain-2.0.0b1/tests/simulation/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/simulation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/simulation/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21623 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/simulation/test_simulation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10038 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/simulation/test_simulator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5129 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/simulation/test_start_simulator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      433 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/testconfig.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.950339 chia-blockchain-2.0.0b1/tests/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)    20462 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/1315537.json
+-rw-r--r--   0 runner    (1001) docker     (123)    20277 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/1315544.json
+-rw-r--r--   0 runner    (1001) docker     (123)    19672 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/1315630.json
+-rw-r--r--   0 runner    (1001) docker     (123)    10501 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/300000.json
+-rw-r--r--   0 runner    (1001) docker     (123)    17387 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/442734.json
+-rw-r--r--   0 runner    (1001) docker     (123)   233251 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/466212.json
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)   405504 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/test-blockchain-db.sqlite
+-rw-r--r--   0 runner    (1001) docker     (123)      700 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/test_full_sync.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3277 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/test_legacy_keyring.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4257 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/tools/test_run_block.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.958339 chia-blockchain-2.0.0b1/tests/util/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2145 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/alert_server.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7104 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/benchmark_cost.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8592 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/bip39_test_vectors.json
+-rw-r--r--   0 runner    (1001) docker     (123)     4346 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/blockchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9871 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/build_network_protocol_files.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      691 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/db_connection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4328 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/gen_ssl_certs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1326 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/generator_tools_testing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1603 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/key_tool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9155 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31159 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/network_protocol_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46740 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/protocol_messages_bytes-v1.0
+-rw-r--r--   0 runner    (1001) docker     (123)   170660 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/protocol_messages_json.py
+-rw-r--r--   0 runner    (1001) docker     (123)      692 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)      297 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/temp_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)      791 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_chunks.py
+-rw-r--r--   0 runner    (1001) docker     (123)      353 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_collection.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11204 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_full_block_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1995 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_limited_semaphore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2112 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_lock_queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1262 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_logging_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3182 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2993 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_network.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22379 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_network_protocol_files.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17774 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_network_protocol_json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6824 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_network_protocol_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2346 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_paginator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      653 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_pprint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9817 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_struct_stream.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1884 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/util/test_trusted_peer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.966339 chia-blockchain-2.0.0b1/tests/wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.970339 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25164 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_lifecycle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2894 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_outer_puzzle.py
+-rw-r--r--   0 runner    (1001) docker     (123)    47568 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14345 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_offer_lifecycle.py
+-rw-r--r--   0 runner    (1001) docker     (123)   162923 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_trades.py
+-rw-r--r--   0 runner    (1001) docker     (123)      123 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.970339 chia-blockchain-2.0.0b1/tests/wallet/dao_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/dao_wallet/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.970339 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6363 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_db_graftroot.py
+-rw-r--r--   0 runner    (1001) docker     (123)   135852 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_dl_offers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26485 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_dl_wallet.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.974339 chia-blockchain-2.0.0b1/tests/wallet/did_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/did_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/did_wallet/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    66004 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/did_wallet/test_did.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.974339 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)   374078 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_1_offers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43345 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_bulk_mint.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15360 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_lifecycle.py
+-rw-r--r--   0 runner    (1001) docker     (123)    66774 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_offers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7544 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_puzzles.py
+-rw-r--r--   0 runner    (1001) docker     (123)    76327 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3289 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_ownership_outer_puzzle.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.978339 chia-blockchain-2.0.0b1/tests/wallet/rpc/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/rpc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/rpc/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10128 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/rpc/test_dl_wallet_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    74646 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/rpc/test_wallet_rpc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.978339 chia-blockchain-2.0.0b1/tests/wallet/simple_sync/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/simple_sync/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/simple_sync/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32900 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/simple_sync/test_simple_sync_protocol.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.978339 chia-blockchain-2.0.0b1/tests/wallet/sync/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/sync/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/sync/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    65362 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/sync/test_wallet_sync.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7270 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_address_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1373 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_bech32m.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2148 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_chialisp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22800 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_coin_selection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8513 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_nft_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8130 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_notifications.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13782 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_offer_parsing_performance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2989 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_puzzle_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4993 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_singleton.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6038 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_singleton_lifecycle.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30445 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_singleton_lifecycle_fast.py
+-rw-r--r--   0 runner    (1001) docker     (123)      796 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_taproot.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28752 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_transaction_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43681 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4257 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_blockchain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40542 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_coin_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_interested_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1617 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_key_val_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17353 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4253 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_retry.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_state_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4398 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_trade_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1175 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/wallet/test_wallet_user_store.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.982339 chia-blockchain-2.0.0b1/tests/weight_proof/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/weight_proof/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/weight_proof/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22920 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tests/weight_proof/test_weight_proof.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 02:17:12.982339 chia-blockchain-2.0.0b1/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/__init__.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     5772 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/analyze-chain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6897 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/analyze_memory_profile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3575 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/cpu_utilization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8959 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/generate_chain.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4707 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/legacy_keyring.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13848 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/manage_clvm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1024 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/plot-log.gnuplot
+-rwxr-xr-x   0 runner    (1001) docker     (123)      791 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/run_benchmark.sh
+-rw-r--r--   0 runner    (1001) docker     (123)     8880 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/run_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)      776 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/test_constants.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    13714 2023-05-09 02:14:48.000000 chia-blockchain-2.0.0b1/tools/test_full_sync.py
```

### Comparing `chia-blockchain-1.8.1rc2/.github/ISSUE_TEMPLATE/bug_report.yaml` & `chia-blockchain-2.0.0b1/.github/ISSUE_TEMPLATE/bug_report.yaml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/ISSUE_TEMPLATE/config.yml` & `chia-blockchain-2.0.0b1/.github/ISSUE_TEMPLATE/config.yml`

 * *Ordering differences only*

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-contact_links:
-  - about: Ask a question or request support here
-    name: Ask for Support
-    url: >-
-      https://github.com/Chia-Network/chia-blockchain/discussions/new?category=support
-  - about: Request a new feature or idea here
-    name: Make a Request
-    url: >-
-      https://github.com/Chia-Network/chia-blockchain/discussions/new?category=ideas
-  - about: Get support on the Chia Keybase chat channels.
-    name: Join the Keybase.io support chat
-    url: 'https://keybase.io/team/chia_network.public'
+contact_links:
+  - about: Ask a question or request support here
+    name: Ask for Support
+    url: >-
+      https://github.com/Chia-Network/chia-blockchain/discussions/new?category=support
+  - about: Request a new feature or idea here
+    name: Make a Request
+    url: >-
+      https://github.com/Chia-Network/chia-blockchain/discussions/new?category=ideas
+  - about: Get support on the Chia Keybase chat channels.
+    name: Join the Keybase.io support chat
+    url: 'https://keybase.io/team/chia_network.public'
```

### Comparing `chia-blockchain-1.8.1rc2/.github/PULL_REQUEST_TEMPLATE.md` & `chia-blockchain-2.0.0b1/.github/PULL_REQUEST_TEMPLATE.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/actions/install/action.yml` & `chia-blockchain-2.0.0b1/.github/actions/install/action.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/dependabot.yml` & `chia-blockchain-2.0.0b1/.github/dependabot.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/benchmarks.yml` & `chia-blockchain-2.0.0b1/.github/workflows/benchmarks.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/build-linux-arm64-installer.yml` & `chia-blockchain-2.0.0b1/.github/workflows/build-linux-arm64-installer.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/build-linux-installer-deb.yml` & `chia-blockchain-2.0.0b1/.github/workflows/build-linux-installer-deb.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/build-linux-installer-rpm.yml` & `chia-blockchain-2.0.0b1/.github/workflows/build-linux-installer-rpm.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/build-macos-installers.yml` & `chia-blockchain-2.0.0b1/.github/workflows/build-macos-installers.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/build-windows-installer.yml` & `chia-blockchain-2.0.0b1/.github/workflows/build-windows-installer.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/check-commit-signing.yml` & `chia-blockchain-2.0.0b1/.github/workflows/check-commit-signing.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/check_wheel_availability.yaml` & `chia-blockchain-2.0.0b1/.github/workflows/check_wheel_availability.yaml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/codeql-analysis.yml` & `chia-blockchain-2.0.0b1/.github/workflows/codeql-analysis.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/conflict-check.yml` & `chia-blockchain-2.0.0b1/.github/workflows/conflict-check.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/dependency-review.yml` & `chia-blockchain-2.0.0b1/.github/workflows/dependency-review.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/mozilla-ca-cert.yml` & `chia-blockchain-2.0.0b1/.github/workflows/mozilla-ca-cert.yml`

 * *Files 0% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 
       - name: "Add changes to new branch"
         run: |
           cd ./mozilla-ca
           git pull origin main
 
       - name: "Create Pull Request"
-        uses: peter-evans/create-pull-request@v4
+        uses: peter-evans/create-pull-request@v5
         with:
           base: main
           body: "Newest Mozilla CA cert"
           branch: mozilla-ca-updates
           commit-message: "adding ca updates"
           delete-branch: true
           reviewers: "wjblanke,emlowe"
```

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/pre-commit.yml` & `chia-blockchain-2.0.0b1/.github/workflows/pre-commit.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/require-labels.yml` & `chia-blockchain-2.0.0b1/.github/workflows/require-labels.yml`

 * *Files 2% similar despite different names*

```diff
@@ -9,15 +9,15 @@
       checks: write
       pull-requests: read
       statuses: write
     outputs:
       status: ${{ steps.check-labels.outputs.status }}
     steps:
       - id: check-labels
-        uses: mheap/github-action-required-labels@v3
+        uses: mheap/github-action-required-labels@v4
         with:
           mode: exactly
           count: 1
           labels: "Added, Changed, Fixed"
           exit_type: success
       - run: echo SUCCESS
         if: steps.check-labels.outputs.status == 'success'
```

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/snyk-python-scan.yml` & `chia-blockchain-2.0.0b1/.github/workflows/snyk-python-scan.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/stale-issue.yml` & `chia-blockchain-2.0.0b1/.github/workflows/stale-issue.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/start-release.yml` & `chia-blockchain-2.0.0b1/.github/workflows/start-release.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/start-sync-test.yml` & `chia-blockchain-2.0.0b1/.github/workflows/start-sync-test.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/super-linter.yml` & `chia-blockchain-2.0.0b1/.github/workflows/super-linter.yml`

 * *Files 0% similar despite different names*

```diff
@@ -53,15 +53,15 @@
       - name: Checkout Code
         uses: actions/checkout@v3
 
       ################################
       # Run Linter against code base #
       ################################
       - name: Lint Code Base
-        uses: github/super-linter@v4
+        uses: github/super-linter@v5
 #        uses: docker://github/super-linter:v3.10.2
         env:
           VALIDATE_ALL_CODEBASE: true
           DEFAULT_BRANCH: main
           LINTER_RULES_PATH: .
           MARKDOWN_CONFIG_FILE: .markdown-lint.yml
           VALIDATE_BASH: true
```

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/test-install-scripts.yml` & `chia-blockchain-2.0.0b1/.github/workflows/test-install-scripts.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/test-single.yml` & `chia-blockchain-2.0.0b1/.github/workflows/test-single.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/test.yml` & `chia-blockchain-2.0.0b1/.github/workflows/test.yml`

 * *Files 5% similar despite different names*

```diff
@@ -127,31 +127,42 @@
           python-version: ${{ matrix.python.action }}
           development: true
 
       - uses: chia-network/actions/activate-venv@main
 
       - name: Coverage Processing
         run: |
-          coverage combine --rcfile=.coveragerc --data-file coverage-reports/.coverage coverage-data/
-          coverage xml --rcfile=.coveragerc --data-file coverage-reports/.coverage -o coverage-reports/coverage.xml
-          coverage html --rcfile=.coveragerc --data-file coverage-reports/.coverage --directory coverage-reports/html/
+          coverage combine --rcfile=.coveragerc --data-file=coverage-reports/.coverage coverage-data/
+          coverage xml --rcfile=.coveragerc --data-file=coverage-reports/.coverage -o coverage-reports/coverage.xml
+          coverage html --rcfile=.coveragerc --data-file=coverage-reports/.coverage --directory coverage-reports/html/
+
+      - uses: coverallsapp/github-action@v2
+        if: always()
+        env:
+          COVERALLS_REPO_TOKEN: ${{ secrets.COVERALLS_REPO_TOKEN }}
 
       - name: Coverage report (chia/)
+        if: always()
         run: |
-          coverage report --rcfile=.coveragerc --data-file coverage-reports/.coverage --include='chia/*' --show-missing | tee coverage-reports/coverage-chia-stdout
+          set -o pipefail
+          coverage report --rcfile=.coveragerc --data-file=coverage-reports/.coverage --include='chia/**/*' --show-missing | tee coverage-reports/coverage-chia-stdout
 
       - name: Coverage report (tests/)
+        if: always()
         run: |
-          coverage report --rcfile=.coveragerc --data-file coverage-reports/.coverage --include='tests/*' --show-missing | tee coverage-reports/coverage-tests-stdout
+          set -o pipefail
+          coverage report --rcfile=.coveragerc --data-file=coverage-reports/.coverage --include='tests/**/*' --show-missing | tee coverage-reports/coverage-tests-stdout
 
       - name: Coverage report (diff)
+        if: always()
         env:
           compare-branch: ${{ github.base_ref == '' && github.event.before || format('origin/{0}', github.base_ref) }}
         run: |
-          diff-cover --compare-branch=${{ env.compare-branch }} --html-report coverage-reports/diff-cover.html --markdown-report coverage-reports/diff-cover.md coverage-reports/coverage.xml | tee coverage-reports/diff-cover-stdout
+          set -o pipefail
+          diff-cover --compare-branch=${{ env.compare-branch }} --fail-under=100 --html-report=coverage-reports/diff-cover.html --markdown-report=coverage-reports/diff-cover.md coverage-reports/coverage.xml | tee coverage-reports/diff-cover-stdout
           cat coverage-reports/diff-cover.md >> $GITHUB_STEP_SUMMARY
 
       - name: Publish coverage reports
         if: always()
         uses: actions/upload-artifact@v3
         with:
           name: coverage-reports
```

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/trigger-docker-dev.yml` & `chia-blockchain-2.0.0b1/.github/workflows/trigger-docker-dev.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.github/workflows/trigger-docker-main.yml` & `chia-blockchain-2.0.0b1/.github/workflows/trigger-docker-main.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.gitignore` & `chia-blockchain-2.0.0b1/.gitignore`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.markdown-lint.yml` & `chia-blockchain-2.0.0b1/.markdown-lint.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/.pre-commit-config.yaml` & `chia-blockchain-2.0.0b1/.pre-commit-config.yaml`

 * *Files 7% similar despite different names*

```diff
@@ -18,14 +18,16 @@
     rev: 23.3.0
     hooks:
     -   id: black
 -   repo: https://github.com/pre-commit/pre-commit-hooks
     rev: v4.3.0
     hooks:
     -   id: check-yaml
+    -   id: mixed-line-ending
+        args: ["--fix=lf"]
     -   id: end-of-file-fixer
         exclude: ".*?(.hex|.clsp|.clvm|.clib)"
     -   id: trailing-whitespace
     -   id: check-merge-conflict
     -   id: check-ast
     -   id: debug-statements
 -   repo: local
```

### Comparing `chia-blockchain-1.8.1rc2/BUILD_TIMELORD.md` & `chia-blockchain-2.0.0b1/BUILD_TIMELORD.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/CHANGELOG.md` & `chia-blockchain-2.0.0b1/CHANGELOG.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/CODE_OF_CONDUCT.md` & `chia-blockchain-2.0.0b1/CODE_OF_CONDUCT.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/CONTRIBUTING.md` & `chia-blockchain-2.0.0b1/CONTRIBUTING.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/Install-gui.ps1` & `chia-blockchain-2.0.0b1/Install-gui.ps1`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/Install-plotter.ps1` & `chia-blockchain-2.0.0b1/Install-plotter.ps1`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/Install.ps1` & `chia-blockchain-2.0.0b1/Install.ps1`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/LICENSE` & `chia-blockchain-2.0.0b1/LICENSE`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/PKG-INFO` & `chia-blockchain-2.0.0b1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chia-blockchain
-Version: 1.8.1rc2
+Version: 2.0.0b1
 Summary: Chia blockchain full node, farmer, timelord, and wallet.
 Home-page: https://chia.net/
 Author: Mariano Sorgente
 Author-email: mariano@chia.net
 License: Apache License
 Project-URL: Source, https://github.com/Chia-Network/chia-blockchain/
 Project-URL: Changelog, https://github.com/Chia-Network/chia-blockchain/blob/main/CHANGELOG.md
```

### Comparing `chia-blockchain-1.8.1rc2/PRETTY_GOOD_PRACTICES.md` & `chia-blockchain-2.0.0b1/PRETTY_GOOD_PRACTICES.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/README.md` & `chia-blockchain-2.0.0b1/README.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/SECURITY.md` & `chia-blockchain-2.0.0b1/SECURITY.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/activated.py` & `chia-blockchain-2.0.0b1/activated.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/block_ref.py` & `chia-blockchain-2.0.0b1/benchmarks/block_ref.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/block_store.py` & `chia-blockchain-2.0.0b1/benchmarks/block_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/clvm_generator.bin` & `chia-blockchain-2.0.0b1/benchmarks/clvm_generator.bin`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/coin_store.py` & `chia-blockchain-2.0.0b1/benchmarks/coin_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/jsonify.py` & `chia-blockchain-2.0.0b1/benchmarks/jsonify.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/mempool-long-lived.py` & `chia-blockchain-2.0.0b1/benchmarks/mempool-long-lived.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/mempool.py` & `chia-blockchain-2.0.0b1/benchmarks/mempool.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from __future__ import annotations
 
 import asyncio
 import cProfile
+import sys
 from contextlib import contextmanager
 from dataclasses import dataclass
 from subprocess import check_call
 from time import monotonic
 from typing import Dict, Iterator, List, Optional, Tuple
 
 from chia.consensus.coinbase import create_farmer_coin, create_pool_coin
@@ -24,14 +25,17 @@
 
 NUM_ITERS = 200
 NUM_PEERS = 5
 
 
 @contextmanager
 def enable_profiler(profile: bool, name: str) -> Iterator[None]:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     if not profile:
         yield
         return
 
     with cProfile.Profile() as pr:
         yield
```

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/streamable.py` & `chia-blockchain-2.0.0b1/benchmarks/streamable.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/transaction_height_delta` & `chia-blockchain-2.0.0b1/benchmarks/transaction_height_delta`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/benchmarks/utils.py` & `chia-blockchain-2.0.0b1/benchmarks/utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/assets/dmg/background.tiff` & `chia-blockchain-2.0.0b1/build_scripts/assets/dmg/background.tiff`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_linux_deb-1-gui.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_linux_deb-1-gui.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_linux_deb-2-installer.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_linux_deb-2-installer.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_linux_rpm-1-gui.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_linux_rpm-1-gui.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_linux_rpm-2-installer.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_linux_rpm-2-installer.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_macos-1-gui.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_macos-1-gui.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_macos-2-installer.sh` & `chia-blockchain-2.0.0b1/build_scripts/build_macos-2-installer.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_windows-1-gui.ps1` & `chia-blockchain-2.0.0b1/build_scripts/build_windows-1-gui.ps1`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/build_windows-2-installer.ps1` & `chia-blockchain-2.0.0b1/build_scripts/build_windows-2-installer.ps1`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/check_dependency_artifacts.py` & `chia-blockchain-2.0.0b1/build_scripts/check_dependency_artifacts.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/clean-runner.sh` & `chia-blockchain-2.0.0b1/build_scripts/clean-runner.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/installer-version.py` & `chia-blockchain-2.0.0b1/build_scripts/installer-version.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/npm_linux/package-lock.json` & `chia-blockchain-2.0.0b1/build_scripts/npm_linux/package-lock.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/npm_macos/package-lock.json` & `chia-blockchain-2.0.0b1/build_scripts/npm_macos/package-lock.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/build_scripts/npm_windows/package-lock.json` & `chia-blockchain-2.0.0b1/build_scripts/npm_windows/package-lock.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/clvm/spend_sim.py` & `chia-blockchain-2.0.0b1/chia/clvm/spend_sim.py`

 * *Files 1% similar despite different names*

```diff
@@ -219,15 +219,15 @@
     async def farm_block(
         self,
         puzzle_hash: bytes32 = bytes32(b"0" * 32),
         item_inclusion_filter: Optional[Callable[[bytes32], bool]] = None,
     ) -> Tuple[List[Coin], List[Coin]]:
         # Fees get calculated
         fees = uint64(0)
-        for item in self.mempool_manager.mempool.all_spends():
+        for item in self.mempool_manager.mempool.all_items():
             fees = uint64(fees + item.fee)
 
         # Rewards get created
         next_block_height: uint32 = uint32(self.block_height + 1) if len(self.block_records) > 0 else self.block_height
         pool_coin: Coin = create_pool_coin(
             next_block_height,
             puzzle_hash,
@@ -423,19 +423,19 @@
             return None
         else:
             assert puzzle is not None
             assert solution is not None
             return CoinSpend(coin_record.coin, puzzle, solution)
 
     async def get_all_mempool_tx_ids(self) -> List[bytes32]:
-        return self.service.mempool_manager.mempool.all_spend_ids()
+        return self.service.mempool_manager.mempool.all_item_ids()
 
     async def get_all_mempool_items(self) -> Dict[bytes32, MempoolItem]:
         spends = {}
-        for item in self.service.mempool_manager.mempool.all_spends():
+        for item in self.service.mempool_manager.mempool.all_items():
             spends[item.name] = item
         return spends
 
     async def get_mempool_item_by_tx_id(self, tx_id: bytes32) -> Optional[Dict[str, Any]]:
         item = self.service.mempool_manager.get_mempool_item(tx_id)
         if item is None:
             return None
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/beta.py` & `chia-blockchain-2.0.0b1/chia/cmds/beta.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/beta_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/beta_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/check_wallet_db.py` & `chia-blockchain-2.0.0b1/chia/cmds/check_wallet_db.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/chia.py` & `chia-blockchain-2.0.0b1/chia/cmds/chia.py`

 * *Files 1% similar despite different names*

```diff
@@ -80,20 +80,20 @@
             exit(1)
         except Exception as e:
             print(f"Failed to read passphrase: {e}")
 
     check_ssl(Path(root_path))
 
 
-@cli.command("version", short_help="Show chia version")
+@cli.command("version", help="Show chia version")
 def version_cmd() -> None:
     print(__version__)
 
 
-@cli.command("run_daemon", short_help="Runs chia daemon")
+@cli.command("run_daemon", help="Runs chia daemon")
 @click.option(
     "--wait-for-unlock",
     help="If the keyring is passphrase-protected, the daemon will wait for an unlock command before accessing keys",
     default=False,
     is_flag=True,
     hidden=True,  # --wait-for-unlock is only set when launched by chia start <service>
 )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/cmds_util.py` & `chia-blockchain-2.0.0b1/chia/cmds/cmds_util.py`

 * *Files 5% similar despite different names*

```diff
@@ -55,44 +55,35 @@
     return f"Run 'chia wallet get_transaction -f {fingerprint} -tx 0x{tx_id}' to get status"
 
 
 async def validate_client_connection(
     rpc_client: RpcClient,
     node_type: str,
     rpc_port: int,
-    root_path: Path,
-    fingerprint: Optional[int],
-    login_to_wallet: bool,
     consume_errors: bool = True,
-) -> Tuple[Optional[int], bool]:
+) -> bool:
     connected: bool = True
     try:
         await rpc_client.healthz()
-        if type(rpc_client) == WalletRpcClient and login_to_wallet:
-            fingerprint = await get_wallet(root_path, rpc_client, fingerprint)
-            if fingerprint is None:
-                connected = False
     except ClientConnectorError:
         if not consume_errors:
             raise
         connected = False
         print(f"Connection error. Check if {node_type.replace('_', ' ')} rpc is running at {rpc_port}")
         print(f"This is normal if {node_type.replace('_', ' ')} is still starting up")
-    return fingerprint, connected
+    return connected
 
 
 @asynccontextmanager
 async def get_any_service_client(
     client_type: Type[_T_RpcClient],
     rpc_port: Optional[int] = None,
     root_path: Path = DEFAULT_ROOT_PATH,
-    fingerprint: Optional[int] = None,
-    login_to_wallet: bool = True,
     consume_errors: bool = True,
-) -> AsyncIterator[Tuple[Optional[_T_RpcClient], Dict[str, Any], Optional[int]]]:
+) -> AsyncIterator[Tuple[Optional[_T_RpcClient], Dict[str, Any]]]:
     """
     Yields a tuple with a RpcClient for the applicable node type a dictionary of the node's configuration,
     and a fingerprint if applicable. However, if connecting to the node fails then we will return None for
     the RpcClient.
     """
 
     node_type = node_config_section_names.get(client_type)
@@ -103,23 +94,20 @@
     config = load_config(root_path, "config.yaml", fill_missing_services=issubclass(client_type, DataLayerRpcClient))
     self_hostname = config["self_hostname"]
     if rpc_port is None:
         rpc_port = config[node_type]["rpc_port"]
     # select node client type based on string
     node_client = await client_type.create(self_hostname, uint16(rpc_port), root_path, config)
     try:
-        # check if we can connect to node, and if we can then validate
-        # fingerprint access (if wallet), otherwise return fingerprint and set connected to False
-        fingerprint, connected = await validate_client_connection(
-            node_client, node_type, rpc_port, root_path, fingerprint, login_to_wallet, consume_errors
-        )
+        # check if we can connect to node
+        connected = await validate_client_connection(node_client, node_type, rpc_port, consume_errors)
         if connected:
-            yield node_client, config, fingerprint
+            yield node_client, config
         else:
-            yield None, config, fingerprint
+            yield None, config
     except Exception as e:  # this is only here to make the errors more user-friendly.
         if not consume_errors:
             raise
         print(f"Exception from '{node_type}' {e}:\n{traceback.format_exc()}")
 
     finally:
         node_client.close()  # this can run even if already closed, will just do nothing.
@@ -221,15 +209,16 @@
 
 async def execute_with_wallet(
     wallet_rpc_port: Optional[int],
     fingerprint: int,
     extra_params: Dict[str, Any],
     function: Callable[[Dict[str, Any], WalletRpcClient, int], Awaitable[None]],
 ) -> None:
-    async with get_any_service_client(WalletRpcClient, wallet_rpc_port, fingerprint=fingerprint) as (
-        wallet_client,
-        _,
-        new_fp,
-    ):
-        if wallet_client is not None:
-            assert new_fp is not None  # wallet only sanity check
-            await function(extra_params, wallet_client, new_fp)
+    async with get_any_service_client(WalletRpcClient, wallet_rpc_port) as (wallet_client, _):
+        if wallet_client is None:
+            return
+
+        new_fp = await get_wallet(DEFAULT_ROOT_PATH, wallet_client, fingerprint)
+        if new_fp is None:
+            return
+
+        await function(extra_params, wallet_client, new_fp)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/coin_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/coin_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/coins.py` & `chia-blockchain-2.0.0b1/chia/cmds/coins.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,21 +5,21 @@
 
 import click
 
 from chia.cmds.cmds_util import execute_with_wallet
 from chia.util.config import load_config, selected_network_address_prefix
 
 
-@click.group("coins", short_help="Manage your wallets coins")
+@click.group("coins", help="Manage your wallets coins")
 @click.pass_context
 def coins_cmd(ctx: click.Context) -> None:
     pass
 
 
-@coins_cmd.command("list", short_help="List all coins")
+@coins_cmd.command("list", help="List all coins")
 @click.option(
     "-p",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -81,15 +81,15 @@
         "paginate": paginate,
     }
     from .coin_funcs import async_list
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, async_list))
 
 
-@coins_cmd.command("combine", short_help="Combine dust coins")
+@coins_cmd.command("combine", help="Combine dust coins")
 @click.option(
     "-p",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -175,15 +175,15 @@
         "largest": largest_first,
     }
     from .coin_funcs import async_combine
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, async_combine))
 
 
-@coins_cmd.command("split", short_help="Split up larger coins")
+@coins_cmd.command("split", help="Split up larger coins")
 @click.option(
     "-p",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/completion.py` & `chia-blockchain-2.0.0b1/chia/cmds/completion.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,21 +12,21 @@
 if shell is not None:
     shell = Path(shell).name
     if shell not in SHELLS:
         shell = None
 
 
 @click.group(
-    short_help="Generate shell completion",
+    help="Generate shell completion",
 )
 def completion() -> None:
     pass
 
 
-@completion.command(short_help="Generate shell completion code")
+@completion.command(help="Generate shell completion code")
 @click.option(
     "-s",
     "--shell",
     type=click.Choice(SHELLS),
     default=shell,
     show_default=True,
     required=shell is None,
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/configure.py` & `chia-blockchain-2.0.0b1/chia/cmds/configure.py`

 * *Files 0% similar despite different names*

```diff
@@ -203,15 +203,15 @@
             change_made = True
 
         if change_made:
             print("Restart any running chia services for changes to take effect")
             save_config(root_path, "config.yaml", config)
 
 
-@click.command("configure", short_help="Modify configuration", no_args_is_help=True)
+@click.command("configure", help="Modify configuration", no_args_is_help=True)
 @click.option(
     "--testnet",
     "-t",
     help="configures for connection to testnet",
     type=click.Choice(["true", "t", "false", "f"]),
 )
 @click.option("--set-node-introducer", help="Set the introducer for node - IP:Port", type=str)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/data.py` & `chia-blockchain-2.0.0b1/chia/cmds/data.py`

 * *Files 2% similar despite different names*

```diff
@@ -24,15 +24,15 @@
     success = response is not None and response.get("success", False)
     logger.info(f"data layer cli call response:{success}")
     # todo make sure all cli methods follow this pattern, uncomment
     # if not success:
     # raise click.ClickException(message=f"query unsuccessful, response: {response}")
 
 
-@click.group("data", short_help="Manage your data")
+@click.group("data", help="Manage your data")
 def data_cmd() -> None:
     pass
 
 
 # TODO: maybe use more helpful `type=`s to get click to handle error reporting of
 #       malformed inputs.
 
@@ -99,27 +99,27 @@
         type=str,
         default=None,
         show_default=True,
         required=False,
     )
 
 
-@data_cmd.command("create_data_store", short_help="Create a new data store")
+@data_cmd.command("create_data_store", help="Create a new data store")
 @create_rpc_port_option()
 @create_fee_option()
 def create_data_store(
     data_rpc_port: int,
     fee: Optional[str],
 ) -> None:
     from chia.cmds.data_funcs import create_data_store_cmd
 
     run(create_data_store_cmd(data_rpc_port, fee))
 
 
-@data_cmd.command("get_value", short_help="Get the value for a given key and store")
+@data_cmd.command("get_value", help="Get the value for a given key and store")
 @create_data_store_id_option()
 @create_key_option()
 @click.option("-r", "--root_hash", help="The hexadecimal root hash", type=str, required=False)
 @create_rpc_port_option()
 def get_value(
     id: str,
     key_string: str,
@@ -127,15 +127,15 @@
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_value_cmd
 
     run(get_value_cmd(data_rpc_port, id, key_string, root_hash))
 
 
-@data_cmd.command("update_data_store", short_help="Update a store by providing the changelist operations")
+@data_cmd.command("update_data_store", help="Update a store by providing the changelist operations")
 @create_data_store_id_option()
 @create_changelist_option()
 @create_rpc_port_option()
 @create_fee_option()
 def update_data_store(
     id: str,
     changelist_string: str,
@@ -143,55 +143,55 @@
     fee: str,
 ) -> None:
     from chia.cmds.data_funcs import update_data_store_cmd
 
     run(update_data_store_cmd(rpc_port=data_rpc_port, store_id=id, changelist=json.loads(changelist_string), fee=fee))
 
 
-@data_cmd.command("get_keys", short_help="Get all keys for a given store")
+@data_cmd.command("get_keys", help="Get all keys for a given store")
 @create_data_store_id_option()
 @click.option("-r", "--root_hash", help="The hexadecimal root hash", type=str, required=False)
 @create_rpc_port_option()
 def get_keys(
     id: str,
     root_hash: Optional[str],
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_keys_cmd
 
     run(get_keys_cmd(data_rpc_port, id, root_hash))
 
 
-@data_cmd.command("get_keys_values", short_help="Get all keys and values for a given store")
+@data_cmd.command("get_keys_values", help="Get all keys and values for a given store")
 @create_data_store_id_option()
 @click.option("-r", "--root_hash", help="The hexadecimal root hash", type=str, required=False)
 @create_rpc_port_option()
 def get_keys_values(
     id: str,
     root_hash: Optional[str],
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_keys_values_cmd
 
     run(get_keys_values_cmd(data_rpc_port, id, root_hash))
 
 
-@data_cmd.command("get_root", short_help="Get the published root hash value for a given store")
+@data_cmd.command("get_root", help="Get the published root hash value for a given store")
 @create_data_store_id_option()
 @create_rpc_port_option()
 def get_root(
     id: str,
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_root_cmd
 
     run(get_root_cmd(rpc_port=data_rpc_port, store_id=id))
 
 
-@data_cmd.command("subscribe", short_help="Subscribe to a store")
+@data_cmd.command("subscribe", help="Subscribe to a store")
 @create_data_store_id_option()
 @click.option(
     "-u",
     "--url",
     "urls",
     help="Manually provide a list of servers urls for downloading the data",
     type=str,
@@ -204,42 +204,42 @@
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import subscribe_cmd
 
     run(subscribe_cmd(rpc_port=data_rpc_port, store_id=id, urls=urls))
 
 
-@data_cmd.command("remove_subscription", short_help="Remove server urls that are added via subscribing to urls")
+@data_cmd.command("remove_subscription", help="Remove server urls that are added via subscribing to urls")
 @create_data_store_id_option()
 @click.option("-u", "--url", "urls", help="Server urls to remove", type=str, multiple=True)
 @create_rpc_port_option()
 def remove_subscription(
     id: str,
     urls: List[str],
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import remove_subscriptions_cmd
 
     run(remove_subscriptions_cmd(rpc_port=data_rpc_port, store_id=id, urls=urls))
 
 
-@data_cmd.command("unsubscribe", short_help="Completely untrack a store")
+@data_cmd.command("unsubscribe", help="Completely untrack a store")
 @create_data_store_id_option()
 @create_rpc_port_option()
 def unsubscribe(
     id: str,
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import unsubscribe_cmd
 
     run(unsubscribe_cmd(rpc_port=data_rpc_port, store_id=id))
 
 
 @data_cmd.command(
-    "get_kv_diff", short_help="Get the inserted and deleted keys and values between an initial and a final hash"
+    "get_kv_diff", help="Get the inserted and deleted keys and values between an initial and a final hash"
 )
 @create_data_store_id_option()
 @click.option("-hash_1", "--hash_1", help="Initial hash", type=str)
 @click.option("-hash_2", "--hash_2", help="Final hash", type=str)
 @create_rpc_port_option()
 def get_kv_diff(
     id: str,
@@ -248,27 +248,27 @@
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_kv_diff_cmd
 
     run(get_kv_diff_cmd(rpc_port=data_rpc_port, store_id=id, hash_1=hash_1, hash_2=hash_2))
 
 
-@data_cmd.command("get_root_history", short_help="Get all changes of a singleton")
+@data_cmd.command("get_root_history", help="Get all changes of a singleton")
 @create_data_store_id_option()
 @create_rpc_port_option()
 def get_root_history(
     id: str,
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_root_history_cmd
 
     run(get_root_history_cmd(rpc_port=data_rpc_port, store_id=id))
 
 
-@data_cmd.command("add_missing_files", short_help="Manually reconstruct server files from the data layer database")
+@data_cmd.command("add_missing_files", help="Manually reconstruct server files from the data layer database")
 @click.option(
     "-i",
     "--ids",
     help="List of stores to reconstruct. If not specified, all stores will be reconstructed",
     type=str,
     required=False,
 )
@@ -290,15 +290,15 @@
             ids=None if ids is None else json.loads(ids),
             overwrite=overwrite,
             foldername=None if foldername is None else Path(foldername),
         )
     )
 
 
-@data_cmd.command("add_mirror", short_help="Publish mirror urls on chain")
+@data_cmd.command("add_mirror", help="Publish mirror urls on chain")
 @click.option("-i", "--id", help="Store id", type=str, required=True)
 @click.option(
     "-a", "--amount", help="Amount to spend for this mirror, in mojos", type=int, default=0, show_default=True
 )
 @click.option(
     "-u",
     "--url",
@@ -319,15 +319,15 @@
             urls=urls,
             amount=amount,
             fee=fee,
         )
     )
 
 
-@data_cmd.command("delete_mirror", short_help="Delete an owned mirror by its coin id")
+@data_cmd.command("delete_mirror", help="Delete an owned mirror by its coin id")
 @click.option("-c", "--coin_id", help="Coin id", type=str, required=True)
 @create_fee_option()
 @create_rpc_port_option()
 def delete_mirror(coin_id: str, fee: Optional[str], data_rpc_port: int) -> None:
     from chia.cmds.data_funcs import delete_mirror_cmd
 
     run(
@@ -335,53 +335,53 @@
             rpc_port=data_rpc_port,
             coin_id=coin_id,
             fee=fee,
         )
     )
 
 
-@data_cmd.command("get_mirrors", short_help="Get a list of all mirrors for a given store")
+@data_cmd.command("get_mirrors", help="Get a list of all mirrors for a given store")
 @click.option("-i", "--id", help="Store id", type=str, required=True)
 @create_rpc_port_option()
 def get_mirrors(id: str, data_rpc_port: int) -> None:
     from chia.cmds.data_funcs import get_mirrors_cmd
 
     run(
         get_mirrors_cmd(
             rpc_port=data_rpc_port,
             store_id=id,
         )
     )
 
 
-@data_cmd.command("get_subscriptions", short_help="Get subscribed stores, including the owned stores")
+@data_cmd.command("get_subscriptions", help="Get subscribed stores, including the owned stores")
 @create_rpc_port_option()
 def get_subscriptions(data_rpc_port: int) -> None:
     from chia.cmds.data_funcs import get_subscriptions_cmd
 
     run(
         get_subscriptions_cmd(
             rpc_port=data_rpc_port,
         )
     )
 
 
-@data_cmd.command("get_owned_stores", short_help="Get owned stores")
+@data_cmd.command("get_owned_stores", help="Get owned stores")
 @create_rpc_port_option()
 def get_owned_stores(data_rpc_port: int) -> None:
     from chia.cmds.data_funcs import get_owned_stores_cmd
 
     run(
         get_owned_stores_cmd(
             rpc_port=data_rpc_port,
         )
     )
 
 
-@data_cmd.command("get_sync_status", short_help="Get locally stored root compared to the root of the singleton")
+@data_cmd.command("get_sync_status", help="Get locally stored root compared to the root of the singleton")
 @create_data_store_id_option()
 @create_rpc_port_option()
 def get_sync_status(
     id: str,
     data_rpc_port: int,
 ) -> None:
     from chia.cmds.data_funcs import get_sync_status_cmd
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/data_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/data_funcs.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,214 +11,214 @@
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.util.byte_types import hexstr_to_bytes
 from chia.util.ints import uint64
 
 
 async def create_data_store_cmd(rpc_port: Optional[int], fee: Optional[str]) -> None:
     final_fee = None if fee is None else uint64(int(Decimal(fee) * units["chia"]))
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.create_data_store(fee=final_fee)
             print(res)
 
 
 async def get_value_cmd(rpc_port: Optional[int], store_id: str, key: str, root_hash: Optional[str]) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     key_bytes = hexstr_to_bytes(key)
     root_hash_bytes = None if root_hash is None else bytes32.from_hexstr(root_hash)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_value(store_id=store_id_bytes, key=key_bytes, root_hash=root_hash_bytes)
             print(res)
 
 
 async def update_data_store_cmd(
     rpc_port: Optional[int],
     store_id: str,
     changelist: List[Dict[str, str]],
     fee: Optional[str],
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     final_fee = None if fee is None else uint64(int(Decimal(fee) * units["chia"]))
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.update_data_store(store_id=store_id_bytes, changelist=changelist, fee=final_fee)
             print(res)
 
 
 async def get_keys_cmd(
     rpc_port: Optional[int],
     store_id: str,
     root_hash: Optional[str],
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     root_hash_bytes = None if root_hash is None else bytes32.from_hexstr(root_hash)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_keys(store_id=store_id_bytes, root_hash=root_hash_bytes)
             print(res)
 
 
 async def get_keys_values_cmd(
     rpc_port: Optional[int],
     store_id: str,
     root_hash: Optional[str],
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     root_hash_bytes = None if root_hash is None else bytes32.from_hexstr(root_hash)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_keys_values(store_id=store_id_bytes, root_hash=root_hash_bytes)
             print(res)
 
 
 async def get_root_cmd(
     rpc_port: Optional[int],
     store_id: str,
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_root(store_id=store_id_bytes)
             print(res)
 
 
 async def subscribe_cmd(
     rpc_port: Optional[int],
     store_id: str,
     urls: List[str],
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.subscribe(store_id=store_id_bytes, urls=urls)
             print(res)
 
 
 async def unsubscribe_cmd(
     rpc_port: Optional[int],
     store_id: str,
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.unsubscribe(store_id=store_id_bytes)
             print(res)
 
 
 async def remove_subscriptions_cmd(
     rpc_port: Optional[int],
     store_id: str,
     urls: List[str],
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.remove_subscriptions(store_id=store_id_bytes, urls=urls)
             print(res)
 
 
 async def get_kv_diff_cmd(
     rpc_port: Optional[int],
     store_id: str,
     hash_1: str,
     hash_2: str,
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     hash_1_bytes = bytes32.from_hexstr(hash_1)
     hash_2_bytes = bytes32.from_hexstr(hash_2)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_kv_diff(store_id=store_id_bytes, hash_1=hash_1_bytes, hash_2=hash_2_bytes)
             print(res)
 
 
 async def get_root_history_cmd(
     rpc_port: Optional[int],
     store_id: str,
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_root_history(store_id=store_id_bytes)
             print(res)
 
 
 async def add_missing_files_cmd(
     rpc_port: Optional[int], ids: Optional[List[str]], overwrite: bool, foldername: Optional[Path]
 ) -> None:
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.add_missing_files(
                 store_ids=(None if ids is None else [bytes32.from_hexstr(id) for id in ids]),
                 overwrite=overwrite,
                 foldername=foldername,
             )
             print(res)
 
 
 async def add_mirror_cmd(
     rpc_port: Optional[int], store_id: str, urls: List[str], amount: int, fee: Optional[str]
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
     final_fee = None if fee is None else uint64(int(Decimal(fee) * units["chia"]))
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.add_mirror(
                 store_id=store_id_bytes,
                 urls=urls,
                 amount=amount,
                 fee=final_fee,
             )
             print(res)
 
 
 async def delete_mirror_cmd(rpc_port: Optional[int], coin_id: str, fee: Optional[str]) -> None:
     coin_id_bytes = bytes32.from_hexstr(coin_id)
     final_fee = None if fee is None else uint64(int(Decimal(fee) * units["chia"]))
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.delete_mirror(
                 coin_id=coin_id_bytes,
                 fee=final_fee,
             )
             print(res)
 
 
 async def get_mirrors_cmd(rpc_port: Optional[int], store_id: str) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_mirrors(store_id=store_id_bytes)
             print(res)
 
 
 async def get_subscriptions_cmd(rpc_port: Optional[int]) -> None:
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_subscriptions()
             print(res)
 
 
 async def get_owned_stores_cmd(rpc_port: Optional[int]) -> None:
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_owned_stores()
             print(res)
 
 
 async def get_sync_status_cmd(
     rpc_port: Optional[int],
     store_id: str,
 ) -> None:
     store_id_bytes = bytes32.from_hexstr(store_id)
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.get_sync_status(store_id=store_id_bytes)
             print(res)
 
 
 async def check_plugins_cmd(rpc_port: Optional[int]) -> None:
-    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _, _):
+    async with get_any_service_client(DataLayerRpcClient, rpc_port) as (client, _):
         if client is not None:
             res = await client.check_plugins()
             print(json.dumps(res, indent=4, sort_keys=True))
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/db.py` & `chia-blockchain-2.0.0b1/chia/cmds/db.py`

 * *Files 6% similar despite different names*

```diff
@@ -6,20 +6,20 @@
 import click
 
 from chia.cmds.db_backup_func import db_backup_func
 from chia.cmds.db_upgrade_func import db_upgrade_func
 from chia.cmds.db_validate_func import db_validate_func
 
 
-@click.group("db", short_help="Manage the blockchain database")
+@click.group("db", help="Manage the blockchain database")
 def db_cmd() -> None:
     pass
 
 
-@db_cmd.command("upgrade", short_help="upgrade a v1 database to v2")
+@db_cmd.command("upgrade", help="upgrade a v1 database to v2")
 @click.option("--input", "in_db_path", default=None, type=click.Path(), help="specify input database file")
 @click.option("--output", "out_db_path", default=None, type=click.Path(), help="specify output database file")
 @click.option(
     "--no-update-config",
     default=False,
     is_flag=True,
     help="don't update config file to point to new database. When specifying a "
@@ -47,15 +47,15 @@
             no_update_config=no_update_config,
             force=force,
         )
     except RuntimeError as e:
         print(f"FAILED: {e}")
 
 
-@db_cmd.command("validate", short_help="validate the (v2) blockchain database. Does not verify proofs")
+@db_cmd.command("validate", help="validate the (v2) blockchain database. Does not verify proofs")
 @click.option("--db", "in_db_path", default=None, type=click.Path(), help="Specifies which database file to validate")
 @click.option(
     "--validate-blocks",
     default=False,
     is_flag=True,
     help="validate consistency of properties of the encoded blocks and block records",
 )
@@ -67,15 +67,15 @@
             None if in_db_path is None else Path(in_db_path),
             validate_blocks=validate_blocks,
         )
     except RuntimeError as e:
         print(f"FAILED: {e}")
 
 
-@db_cmd.command("backup", short_help="backup the blockchain database using VACUUM INTO command")
+@db_cmd.command("backup", help="backup the blockchain database using VACUUM INTO command")
 @click.option("--backup_file", "db_backup_file", default=None, type=click.Path(), help="Specifies the backup file")
 @click.option("--no_indexes", default=False, is_flag=True, help="Create backup without indexes")
 @click.pass_context
 def db_backup_cmd(ctx: click.Context, db_backup_file: Optional[str], no_indexes: bool) -> None:
     try:
         db_backup_func(
             Path(ctx.obj["root_path"]),
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/db_backup_func.py` & `chia-blockchain-2.0.0b1/chia/cmds/db_backup_func.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/db_upgrade_func.py` & `chia-blockchain-2.0.0b1/chia/cmds/db_upgrade_func.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/db_validate_func.py` & `chia-blockchain-2.0.0b1/chia/cmds/db_validate_func.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/farm.py` & `chia-blockchain-2.0.0b1/chia/cmds/farm.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 from __future__ import annotations
 
 from typing import Optional
 
 import click
 
 
-@click.group("farm", short_help="Manage your farm")
+@click.group("farm", help="Manage your farm")
 def farm_cmd() -> None:
     pass
 
 
-@farm_cmd.command("summary", short_help="Summary of farming information")
+@farm_cmd.command("summary", help="Summary of farming information")
 @click.option(
     "-p",
     "--rpc-port",
     help=(
         "Set the port where the Full Node is hosting the RPC interface. "
         "See the rpc_port under full_node in config.yaml"
     ),
@@ -58,15 +58,15 @@
     import asyncio
 
     from .farm_funcs import summary
 
     asyncio.run(summary(rpc_port, wallet_rpc_port, harvester_rpc_port, farmer_rpc_port))
 
 
-@farm_cmd.command("challenges", short_help="Show the latest challenges")
+@farm_cmd.command("challenges", help="Show the latest challenges")
 @click.option(
     "-fp",
     "--farmer-rpc-port",
     help="Set the port where the Farmer is hosting the RPC interface. See the rpc_port under farmer in config.yaml",
     type=int,
     default=None,
     show_default=True,
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/farm_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/farm_funcs.py`

 * *Files 10% similar despite different names*

```diff
@@ -11,32 +11,29 @@
 from chia.util.misc import format_bytes, format_minutes
 from chia.util.network import is_localhost
 
 SECONDS_PER_BLOCK = (24 * 3600) / 4608
 
 
 async def get_harvesters_summary(farmer_rpc_port: Optional[int]) -> Optional[Dict[str, Any]]:
-    async with get_any_service_client(FarmerRpcClient, farmer_rpc_port) as node_config_fp:
-        farmer_client, _, _ = node_config_fp
+    async with get_any_service_client(FarmerRpcClient, farmer_rpc_port) as (farmer_client, _):
         if farmer_client is not None:
             return await farmer_client.get_harvesters_summary()
     return None
 
 
 async def get_blockchain_state(rpc_port: Optional[int]) -> Optional[Dict[str, Any]]:
-    async with get_any_service_client(FullNodeRpcClient, rpc_port) as node_config_fp:
-        client, _, _ = node_config_fp
+    async with get_any_service_client(FullNodeRpcClient, rpc_port) as (client, _):
         if client is not None:
             return await client.get_blockchain_state()
     return None
 
 
 async def get_average_block_time(rpc_port: Optional[int]) -> float:
-    async with get_any_service_client(FullNodeRpcClient, rpc_port) as node_config_fp:
-        client, _, _ = node_config_fp
+    async with get_any_service_client(FullNodeRpcClient, rpc_port) as (client, _):
         if client is not None:
             blocks_to_compare = 500
             blockchain_state = await client.get_blockchain_state()
             curr: Optional[BlockRecord] = blockchain_state["peak"]
             if curr is None or curr.height < (blocks_to_compare + 100):
                 return SECONDS_PER_BLOCK
             while curr is not None and curr.height > 0 and not curr.is_transaction_block:
@@ -51,24 +48,22 @@
                 # stupid mypy
                 return SECONDS_PER_BLOCK
             return (curr.timestamp - past_curr.timestamp) / (curr.height - past_curr.height)
     return SECONDS_PER_BLOCK
 
 
 async def get_wallets_stats(wallet_rpc_port: Optional[int]) -> Optional[Dict[str, Any]]:
-    async with get_any_service_client(WalletRpcClient, wallet_rpc_port, login_to_wallet=False) as node_config_fp:
-        wallet_client, _, _ = node_config_fp
+    async with get_any_service_client(WalletRpcClient, wallet_rpc_port) as (wallet_client, _):
         if wallet_client is not None:
             return await wallet_client.get_farmed_amount()
     return None
 
 
 async def get_challenges(farmer_rpc_port: Optional[int]) -> Optional[List[Dict[str, Any]]]:
-    async with get_any_service_client(FarmerRpcClient, farmer_rpc_port) as node_config_fp:
-        farmer_client, _, _ = node_config_fp
+    async with get_any_service_client(FarmerRpcClient, farmer_rpc_port) as (farmer_client, _):
         if farmer_client is not None:
             return await farmer_client.get_signage_points()
     return None
 
 
 async def challenges(farmer_rpc_port: Optional[int], limit: int) -> None:
     signage_points = await get_challenges(farmer_rpc_port)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/init.py` & `chia-blockchain-2.0.0b1/chia/cmds/init.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from __future__ import annotations
 
 import click
 
 
-@click.command("init", short_help="Create or migrate the configuration")
+@click.command("init", help="Create or migrate the configuration")
 @click.option(
     "--create-certs",
     "-c",
     default=None,
     help="Create new SSL certificates based on CA in [directory]",
     type=click.Path(),
 )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/init_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/init_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/keys.py` & `chia-blockchain-2.0.0b1/chia/cmds/keys.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 from __future__ import annotations
 
 from typing import Optional, Tuple
 
 import click
 
 
-@click.group("keys", short_help="Manage your keys")
+@click.group("keys", help="Manage your keys")
 @click.pass_context
 def keys_cmd(ctx: click.Context) -> None:
     """Create, delete, view and use your key pairs"""
     from pathlib import Path
 
     root_path: Path = ctx.obj["root_path"]
     if not root_path.is_dir():
         raise RuntimeError("Please initialize (or migrate) your config directory with chia init")
 
 
-@keys_cmd.command("generate", short_help="Generates and adds a key to keychain")
+@keys_cmd.command("generate", help="Generates and adds a key to keychain")
 @click.option(
     "--label",
     "-l",
     default=None,
     help="Enter the label for the key",
     type=str,
     required=False,
@@ -30,15 +30,15 @@
     from .init_funcs import check_keys
     from .keys_funcs import generate_and_add
 
     generate_and_add(label)
     check_keys(ctx.obj["root_path"])
 
 
-@keys_cmd.command("show", short_help="Displays all the keys in keychain or the key with the given fingerprint")
+@keys_cmd.command("show", help="Displays all the keys in keychain or the key with the given fingerprint")
 @click.option(
     "--show-mnemonic-seed", help="Show the mnemonic seed of the keys", default=False, show_default=True, is_flag=True
 )
 @click.option(
     "--non-observer-derivation",
     "-d",
     help=(
@@ -74,15 +74,15 @@
     fingerprint: Optional[int],
 ) -> None:
     from .keys_funcs import show_keys
 
     show_keys(ctx.obj["root_path"], show_mnemonic_seed, non_observer_derivation, json, fingerprint)
 
 
-@keys_cmd.command("add", short_help="Add a private key by mnemonic")
+@keys_cmd.command("add", help="Add a private key by mnemonic")
 @click.option(
     "--filename",
     "-f",
     default=None,
     help="The filename containing the secret key mnemonic to add",
     type=str,
     required=False,
@@ -106,27 +106,27 @@
 
         mnemonic = Path(filename).read_text().rstrip()
 
     query_and_add_private_key_seed(mnemonic, label)
     check_keys(ctx.obj["root_path"])
 
 
-@keys_cmd.group("label", short_help="Manage your key labels")
+@keys_cmd.group("label", help="Manage your key labels")
 def label_cmd() -> None:
     pass
 
 
-@label_cmd.command("show", short_help="Show the labels of all available keys")
+@label_cmd.command("show", help="Show the labels of all available keys")
 def show_label_cmd() -> None:
     from .keys_funcs import show_all_key_labels
 
     show_all_key_labels()
 
 
-@label_cmd.command("set", short_help="Set the label of a key")
+@label_cmd.command("set", help="Set the label of a key")
 @click.option(
     "--fingerprint",
     "-f",
     help="Enter the fingerprint of the key you want to use",
     type=int,
     required=True,
 )
@@ -139,29 +139,29 @@
 )
 def set_label_cmd(fingerprint: int, label: str) -> None:
     from .keys_funcs import set_key_label
 
     set_key_label(fingerprint, label)
 
 
-@label_cmd.command("delete", short_help="Delete the label of a key")
+@label_cmd.command("delete", help="Delete the label of a key")
 @click.option(
     "--fingerprint",
     "-f",
     help="Enter the fingerprint of the key you want to use",
     type=int,
     required=True,
 )
 def delete_label_cmd(fingerprint: int) -> None:
     from .keys_funcs import delete_key_label
 
     delete_key_label(fingerprint)
 
 
-@keys_cmd.command("delete", short_help="Delete a key by its pk fingerprint in hex form")
+@keys_cmd.command("delete", help="Delete a key by its pk fingerprint in hex form")
 @click.option(
     "--fingerprint",
     "-f",
     default=None,
     help="Enter the fingerprint of the key you want to use",
     type=int,
     required=True,
@@ -171,29 +171,29 @@
     from .init_funcs import check_keys
     from .keys_funcs import delete
 
     delete(fingerprint)
     check_keys(ctx.obj["root_path"])
 
 
-@keys_cmd.command("delete_all", short_help="Delete all private keys in keychain")
+@keys_cmd.command("delete_all", help="Delete all private keys in keychain")
 def delete_all_cmd() -> None:
     from chia.util.keychain import Keychain
 
     Keychain().delete_all_keys()
 
 
-@keys_cmd.command("generate_and_print", short_help="Generates but does NOT add to keychain")
+@keys_cmd.command("generate_and_print", help="Generates but does NOT add to keychain")
 def generate_and_print_cmd() -> None:
     from .keys_funcs import generate_and_print
 
     generate_and_print()
 
 
-@keys_cmd.command("sign", short_help="Sign a message with a private key")
+@keys_cmd.command("sign", help="Sign a message with a private key")
 @click.option("--message", "-d", default=None, help="Enter the message to sign in UTF-8", type=str, required=True)
 @click.option(
     "--fingerprint",
     "-f",
     default=None,
     help="Enter the fingerprint of the key you want to use",
     type=int,
@@ -248,15 +248,15 @@
         raise click.BadParameter("Missing 'signature' field")
     if "signing_mode" not in data:
         raise click.BadParameter("Missing 'signing_mode' field")
 
     return data["message"], data["pubkey"], data["signature"], data["signing_mode"]
 
 
-@keys_cmd.command("verify", short_help="Verify a signature with a pk")
+@keys_cmd.command("verify", help="Verify a signature with a pk")
 @click.option("--message", "-d", default=None, help="Enter the signed message in UTF-8", type=str)
 @click.option("--public_key", "-p", default=None, help="Enter the pk in hex", type=str)
 @click.option("--signature", "-s", default=None, help="Enter the signature in hex", type=str)
 @click.option(
     "--as-bytes",
     "-b",
     help="Verify the signed message as sequence of bytes rather than UTF-8 string. Ignored if --json is used.",
@@ -278,15 +278,15 @@
         parsed_message, parsed_pubkey, parsed_sig, parsed_signing_mode_str = parse_signature_json(json)
 
         verify(parsed_message, parsed_pubkey, parsed_sig, as_bytes_from_signing_mode(parsed_signing_mode_str))
     else:
         verify(message, public_key, signature, as_bytes)
 
 
-@keys_cmd.group("derive", short_help="Derive child keys or wallet addresses")
+@keys_cmd.group("derive", help="Derive child keys or wallet addresses")
 @click.option(
     "--fingerprint",
     "-f",
     default=None,
     help="Enter the fingerprint of the key you want to use.",
     type=int,
     required=False,
@@ -301,15 +301,15 @@
 )
 @click.pass_context
 def derive_cmd(ctx: click.Context, fingerprint: Optional[int], filename: Optional[str]) -> None:
     ctx.obj["fingerprint"] = fingerprint
     ctx.obj["filename"] = filename
 
 
-@derive_cmd.command("search", short_help="Search the keyring for one or more matching derived keys or wallet addresses")
+@derive_cmd.command("search", help="Search the keyring for one or more matching derived keys or wallet addresses")
 @click.argument("search-terms", type=str, nargs=-1)
 @click.option(
     "--limit", "-l", default=100, show_default=True, help="Limit the number of derivations to search against", type=int
 )
 @click.option(
     "--non-observer-derivation",
     "-d",
@@ -379,15 +379,15 @@
         derive_from_hd_path,
         prefix,
     )
 
     sys.exit(0 if found else 1)
 
 
-@derive_cmd.command("wallet-address", short_help="Derive wallet receive addresses")
+@derive_cmd.command("wallet-address", help="Derive wallet receive addresses")
 @click.option(
     "--index", "-i", help="Index of the first wallet address to derive. Index 0 is the first wallet address.", default=0
 )
 @click.option("--count", "-n", help="Number of wallet addresses to derive, starting at index.", default=1)
 @click.option("--prefix", "-x", help="Address prefix (xch for mainnet, txch for testnet)", default=None, type=str)
 @click.option(
     "--non-observer-derivation",
@@ -416,15 +416,15 @@
     private_key = resolve_derivation_master_key(filename if filename is not None else fingerprint)
 
     derive_wallet_address(
         ctx.obj["root_path"], private_key, index, count, prefix, non_observer_derivation, show_hd_path
     )
 
 
-@derive_cmd.command("child-key", short_help="Derive child keys")
+@derive_cmd.command("child-key", help="Derive child keys")
 @click.option(
     "--type",
     "-t",
     "key_type",  # Rename the target argument
     help="Type of child key to derive",
     required=False,
     type=click.Choice(["farmer", "pool", "wallet", "local", "backup", "singleton", "pool_auth"]),
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/keys_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/keys_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/netspace.py` & `chia-blockchain-2.0.0b1/chia/cmds/netspace.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
 from typing import Optional
 
 import click
 
 
-@click.command("netspace", short_help="Estimate total farmed space on the network")
+@click.command("netspace", help="Estimate total farmed space on the network")
 @click.option(
     "-p",
     "--rpc-port",
     help=(
         "Set the port where the Full Node is hosting the RPC interface. "
         "See the rpc_port under full_node in config.yaml. "
         "[default: 8555]"
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/netspace_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/netspace_funcs.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,49 +1,47 @@
 from __future__ import annotations
 
 from typing import Optional
 
 from chia.cmds.cmds_util import get_any_service_client
 from chia.rpc.full_node_rpc_client import FullNodeRpcClient
-from chia.util.byte_types import hexstr_to_bytes
+from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.util.misc import format_bytes
 
 
 async def netstorge_async(rpc_port: Optional[int], delta_block_height: str, start: str) -> None:
     """
     Calculates the estimated space on the network given two block header hashes.
     """
-    async with get_any_service_client(FullNodeRpcClient, rpc_port) as node_config_fp:
-        client, _, _ = node_config_fp
+    async with get_any_service_client(FullNodeRpcClient, rpc_port) as (client, _):
         if client is not None:
             if delta_block_height:
                 if start == "":
                     blockchain_state = await client.get_blockchain_state()
                     if blockchain_state["peak"] is None:
                         print("No blocks in blockchain")
                         return None
 
                     newer_block_height = blockchain_state["peak"].height
                 else:
-                    newer_block = await client.get_block_record(hexstr_to_bytes(start))
+                    newer_block = await client.get_block_record(bytes32.from_hexstr(start))
                     if newer_block is None:
                         print("Block header hash", start, "not found.")
                         return None
                     else:
                         print("newer_height", newer_block.height)
                         newer_block_height = newer_block.height
 
                 newer_block_header = await client.get_block_record_by_height(newer_block_height)
                 older_block_height = max(0, newer_block_height - int(delta_block_height))
                 older_block_header = await client.get_block_record_by_height(older_block_height)
                 assert newer_block_header is not None and older_block_header is not None
                 network_space_bytes_estimate = await client.get_network_space(
                     newer_block_header.header_hash, older_block_header.header_hash
                 )
-                assert network_space_bytes_estimate is not None
                 print(
                     "Older Block\n"
                     f"Block Height: {older_block_header.height}\n"
                     f"Weight:           {older_block_header.weight}\n"
                     f"VDF Iterations:   {older_block_header.total_iters}\n"
                     f"Header Hash:      0x{older_block_header.header_hash}\n"
                 )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/passphrase.py` & `chia-blockchain-2.0.0b1/chia/cmds/passphrase.py`

 * *Files 6% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 from typing import Optional
 
 import click
 
 from chia.util.config import load_config
 
 
-@click.group("passphrase", short_help="Manage your keyring passphrase")
+@click.group("passphrase", help="Manage your keyring passphrase")
 def passphrase_cmd() -> None:
     pass
 
 
 @passphrase_cmd.command(
     "set",
     help="""Sets or updates the keyring passphrase. If --passphrase-file and/or --current-passphrase-file options are
@@ -99,32 +99,32 @@
     if remove_passphrase(current_passphrase):
         # Attempt to update the daemon's passphrase cache
         root_path = ctx.obj["root_path"]
         config = load_config(root_path, "config.yaml")
         sys.exit(asyncio.run(async_update_daemon_passphrase_cache_if_running(root_path, config)))
 
 
-@passphrase_cmd.group("hint", short_help="Manage the optional keyring passphrase hint")
+@passphrase_cmd.group("hint", help="Manage the optional keyring passphrase hint")
 def hint_cmd() -> None:
     pass
 
 
-@hint_cmd.command("display", short_help="Display the keyring passphrase hint")
+@hint_cmd.command("display", help="Display the keyring passphrase hint")
 def display_hint() -> None:
     from .passphrase_funcs import display_passphrase_hint
 
     display_passphrase_hint()
 
 
-@hint_cmd.command("set", short_help="Set or update the keyring passphrase hint")
+@hint_cmd.command("set", help="Set or update the keyring passphrase hint")
 @click.argument("hint", nargs=1)
 def set_hint(hint: str) -> None:
     from .passphrase_funcs import set_passphrase_hint
 
     set_passphrase_hint(hint)
 
 
-@hint_cmd.command("remove", short_help="Remove the keyring passphrase hint")
+@hint_cmd.command("remove", help="Remove the keyring passphrase hint")
 def remove_hint() -> None:
     from .passphrase_funcs import remove_passphrase_hint
 
     remove_passphrase_hint()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/passphrase_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/passphrase_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/peer.py` & `chia-blockchain-2.0.0b1/chia/cmds/peer.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 
 import click
 
 from chia.cmds.cmds_util import NODE_TYPES
 from chia.cmds.peer_funcs import peer_async
 
 
-@click.command("peer", short_help="Show, or modify peering connections", no_args_is_help=True)
+@click.command("peer", help="Show, or modify peering connections", no_args_is_help=True)
 @click.option(
     "-p",
     "--rpc-port",
     help=(
         "Set the port where the farmer, wallet, full node or harvester "
         "is hosting the RPC interface. See the rpc_port in config.yaml"
     ),
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/peer_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/peer_funcs.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,128 +1,127 @@
-from __future__ import annotations
-
-from pathlib import Path
-from typing import Any, Dict, Optional
-
-from chia.cmds.cmds_util import NODE_TYPES, get_any_service_client
-from chia.rpc.rpc_client import RpcClient
-
-
-async def add_node_connection(rpc_client: RpcClient, add_connection: str) -> None:
-    if ":" not in add_connection:
-        print("Enter a valid IP and port in the following format: 10.5.4.3:8000")
-    else:
-        ip, port = (
-            ":".join(add_connection.split(":")[:-1]),
-            add_connection.split(":")[-1],
-        )
-        print(f"Connecting to {ip}, {port}")
-        try:
-            result = await rpc_client.open_connection(ip, int(port))
-            err = result.get("error")
-            if result["success"] is False or err is not None:
-                print(err)
-        except Exception:
-            print(f"Failed to connect to {ip}:{port}")
-
-
-async def remove_node_connection(rpc_client: RpcClient, remove_connection: str) -> None:
-    from chia.server.outbound_message import NodeType
-
-    result_txt = ""
-    if len(remove_connection) != 8:
-        result_txt = "Invalid NodeID. Do not include '.'"
-    else:
-        connections = await rpc_client.get_connections()
-        for con in connections:
-            if remove_connection == con["node_id"].hex()[:8]:
-                print("Attempting to disconnect", "NodeID", remove_connection)
-                try:
-                    await rpc_client.close_connection(con["node_id"])
-                except Exception:
-                    result_txt = f"Failed to disconnect NodeID {remove_connection}"
-                else:
-                    result_txt = (
-                        f"NodeID {remove_connection}... {NodeType(con['type']).name} {con['peer_host']} disconnected"
-                    )
-            elif result_txt == "":
-                result_txt = f"NodeID {remove_connection}... not found"
-    print(result_txt)
-
-
-async def print_connections(rpc_client: RpcClient, trusted_peers: Dict[str, Any]) -> None:
-    import time
-
-    from chia.server.outbound_message import NodeType
-    from chia.util.network import is_trusted_peer
-
-    connections = await rpc_client.get_connections()
-    print("Connections:")
-    print("Type      IP                                      Ports       NodeID      Last Connect" + "      MiB Up|Dwn")
-    for con in connections:
-        last_connect_tuple = time.struct_time(time.localtime(con["last_message_time"]))
-        last_connect = time.strftime("%b %d %T", last_connect_tuple)
-        mb_down = con["bytes_read"] / (1024 * 1024)
-        mb_up = con["bytes_written"] / (1024 * 1024)
-
-        host = con["peer_host"]
-        # Strip IPv6 brackets
-        host = host.strip("[]")
-
-        trusted: bool = is_trusted_peer(host, con["node_id"], trusted_peers, False)
-        # Nodetype length is 9 because INTRODUCER will be deprecated
-        if NodeType(con["type"]) is NodeType.FULL_NODE:
-            peak_height = con.get("peak_height", None)
-            connection_peak_hash = con.get("peak_hash", None)
-            if connection_peak_hash is None:
-                connection_peak_hash = "No Info"
-            else:
-                if connection_peak_hash.startswith(("0x", "0X")):
-                    connection_peak_hash = connection_peak_hash[2:]
-                connection_peak_hash = f"{connection_peak_hash[:8]}..."
-            con_str = (
-                f"{NodeType(con['type']).name:9} {host:39} "
-                f"{con['peer_port']:5}/{con['peer_server_port']:<5}"
-                f" {con['node_id'].hex()[:8]}... "
-                f"{last_connect}  "
-                f"{mb_up:7.1f}|{mb_down:<7.1f}"
-                f"\n                                                  "
-            )
-            if peak_height is not None:
-                con_str += f"-Height: {peak_height:8.0f}    -Hash: {connection_peak_hash}"
-            else:
-                con_str += f"-Height: No Info    -Hash: {connection_peak_hash}"
-            # Only show when Trusted is True
-            if trusted:
-                con_str += f"    -Trusted: {trusted}"
-        else:
-            con_str = (
-                f"{NodeType(con['type']).name:9} {host:39} "
-                f"{con['peer_port']:5}/{con['peer_server_port']:<5}"
-                f" {con['node_id'].hex()[:8]}... "
-                f"{last_connect}  "
-                f"{mb_up:7.1f}|{mb_down:<7.1f}"
-            )
-        print(con_str)
-
-
-async def peer_async(
-    node_type: str,
-    rpc_port: Optional[int],
-    root_path: Path,
-    show_connections: bool,
-    add_connection: str,
-    remove_connection: str,
-) -> None:
-    client_type = NODE_TYPES[node_type]
-    async with get_any_service_client(client_type, rpc_port, root_path) as node_config_fp:
-        rpc_client, config, _ = node_config_fp
-        if rpc_client is not None:
-            # Check or edit node connections
-            if show_connections:
-                trusted_peers: Dict[str, Any] = config["full_node"].get("trusted_peers", {})
-                await print_connections(rpc_client, trusted_peers)
-                # if called together with state, leave a blank line
-            if add_connection:
-                await add_node_connection(rpc_client, add_connection)
-            if remove_connection:
-                await remove_node_connection(rpc_client, remove_connection)
+from __future__ import annotations
+
+from pathlib import Path
+from typing import Any, Dict, Optional
+
+from chia.cmds.cmds_util import NODE_TYPES, get_any_service_client
+from chia.rpc.rpc_client import RpcClient
+
+
+async def add_node_connection(rpc_client: RpcClient, add_connection: str) -> None:
+    if ":" not in add_connection:
+        print("Enter a valid IP and port in the following format: 10.5.4.3:8000")
+    else:
+        ip, port = (
+            ":".join(add_connection.split(":")[:-1]),
+            add_connection.split(":")[-1],
+        )
+        print(f"Connecting to {ip}, {port}")
+        try:
+            result = await rpc_client.open_connection(ip, int(port))
+            err = result.get("error")
+            if result["success"] is False or err is not None:
+                print(err)
+        except Exception:
+            print(f"Failed to connect to {ip}:{port}")
+
+
+async def remove_node_connection(rpc_client: RpcClient, remove_connection: str) -> None:
+    from chia.server.outbound_message import NodeType
+
+    result_txt = ""
+    if len(remove_connection) != 8:
+        result_txt = "Invalid NodeID. Do not include '.'"
+    else:
+        connections = await rpc_client.get_connections()
+        for con in connections:
+            if remove_connection == con["node_id"].hex()[:8]:
+                print("Attempting to disconnect", "NodeID", remove_connection)
+                try:
+                    await rpc_client.close_connection(con["node_id"])
+                except Exception:
+                    result_txt = f"Failed to disconnect NodeID {remove_connection}"
+                else:
+                    result_txt = (
+                        f"NodeID {remove_connection}... {NodeType(con['type']).name} {con['peer_host']} disconnected"
+                    )
+            elif result_txt == "":
+                result_txt = f"NodeID {remove_connection}... not found"
+    print(result_txt)
+
+
+async def print_connections(rpc_client: RpcClient, trusted_peers: Dict[str, Any]) -> None:
+    import time
+
+    from chia.server.outbound_message import NodeType
+    from chia.util.network import is_trusted_peer
+
+    connections = await rpc_client.get_connections()
+    print("Connections:")
+    print("Type      IP                                      Ports       NodeID      Last Connect" + "      MiB Up|Dwn")
+    for con in connections:
+        last_connect_tuple = time.struct_time(time.localtime(con["last_message_time"]))
+        last_connect = time.strftime("%b %d %T", last_connect_tuple)
+        mb_down = con["bytes_read"] / (1024 * 1024)
+        mb_up = con["bytes_written"] / (1024 * 1024)
+
+        host = con["peer_host"]
+        # Strip IPv6 brackets
+        host = host.strip("[]")
+
+        trusted: bool = is_trusted_peer(host, con["node_id"], trusted_peers, False)
+        # Nodetype length is 9 because INTRODUCER will be deprecated
+        if NodeType(con["type"]) is NodeType.FULL_NODE:
+            peak_height = con.get("peak_height", None)
+            connection_peak_hash = con.get("peak_hash", None)
+            if connection_peak_hash is None:
+                connection_peak_hash = "No Info"
+            else:
+                if connection_peak_hash.startswith(("0x", "0X")):
+                    connection_peak_hash = connection_peak_hash[2:]
+                connection_peak_hash = f"{connection_peak_hash[:8]}..."
+            con_str = (
+                f"{NodeType(con['type']).name:9} {host:39} "
+                f"{con['peer_port']:5}/{con['peer_server_port']:<5}"
+                f" {con['node_id'].hex()[:8]}... "
+                f"{last_connect}  "
+                f"{mb_up:7.1f}|{mb_down:<7.1f}"
+                f"\n                                                  "
+            )
+            if peak_height is not None:
+                con_str += f"-Height: {peak_height:8.0f}    -Hash: {connection_peak_hash}"
+            else:
+                con_str += f"-Height: No Info    -Hash: {connection_peak_hash}"
+            # Only show when Trusted is True
+            if trusted:
+                con_str += f"    -Trusted: {trusted}"
+        else:
+            con_str = (
+                f"{NodeType(con['type']).name:9} {host:39} "
+                f"{con['peer_port']:5}/{con['peer_server_port']:<5}"
+                f" {con['node_id'].hex()[:8]}... "
+                f"{last_connect}  "
+                f"{mb_up:7.1f}|{mb_down:<7.1f}"
+            )
+        print(con_str)
+
+
+async def peer_async(
+    node_type: str,
+    rpc_port: Optional[int],
+    root_path: Path,
+    show_connections: bool,
+    add_connection: str,
+    remove_connection: str,
+) -> None:
+    client_type = NODE_TYPES[node_type]
+    async with get_any_service_client(client_type, rpc_port, root_path) as (rpc_client, config):
+        if rpc_client is not None:
+            # Check or edit node connections
+            if show_connections:
+                trusted_peers: Dict[str, Any] = config["full_node"].get("trusted_peers", {})
+                await print_connections(rpc_client, trusted_peers)
+                # if called together with state, leave a blank line
+            if add_connection:
+                await add_node_connection(rpc_client, add_connection)
+            if remove_connection:
+                await remove_node_connection(rpc_client, remove_connection)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/plotnft.py` & `chia-blockchain-2.0.0b1/chia/cmds/plotnft.py`

 * *Files 2% similar despite different names*

```diff
@@ -16,20 +16,20 @@
     except ValueError:
         raise click.BadParameter("Fee must be decimal dotted value in XCH (e.g. 0.00005)")
     if fee < 0 or fee > MAX_CMDLINE_FEE:
         raise click.BadParameter(f"Fee must be in the range 0 to {MAX_CMDLINE_FEE}")
     return value
 
 
-@click.group("plotnft", short_help="Manage your plot NFTs")
+@click.group("plotnft", help="Manage your plot NFTs")
 def plotnft_cmd() -> None:
     pass
 
 
-@plotnft_cmd.command("show", short_help="Show plotnft information")
+@plotnft_cmd.command("show", help="Show plotnft information")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -39,27 +39,25 @@
     import asyncio
 
     from .plotnft_funcs import show
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, {"id": id}, show))
 
 
-@plotnft_cmd.command(
-    "get_login_link", short_help="Create a login link for a pool. To get the launcher id, use plotnft show."
-)
+@plotnft_cmd.command("get_login_link", help="Create a login link for a pool. To get the launcher id, use plotnft show.")
 @click.option("-l", "--launcher_id", help="Launcher ID of the plotnft", type=str, required=True)
 def get_login_link_cmd(launcher_id: str) -> None:
     import asyncio
 
     from .plotnft_funcs import get_login_link
 
     asyncio.run(get_login_link(launcher_id))
 
 
-@plotnft_cmd.command("create", short_help="Create a plot NFT")
+@plotnft_cmd.command("create", help="Create a plot NFT")
 @click.option("-y", "--yes", help="No prompts", is_flag=True)
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option("-u", "--pool_url", help="HTTPS host:port of the pool to join", type=str, required=False)
 @click.option("-s", "--state", help="Initial state of Plot NFT: local or pool", type=str, required=True)
 @click.option(
     "-m",
     "--fee",
@@ -101,15 +99,15 @@
         "state": valid_initial_states[state],
         "fee": fee,
         "yes": yes,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, create))
 
 
-@plotnft_cmd.command("join", short_help="Join a plot NFT to a Pool")
+@plotnft_cmd.command("join", help="Join a plot NFT to a Pool")
 @click.option("-y", "--yes", help="No prompts", is_flag=True)
 @click.option("-i", "--id", help="ID of the wallet to use", type=int, default=None, show_default=True, required=True)
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option("-u", "--pool_url", help="HTTPS host:port of the pool to join", type=str, required=True)
 @click.option(
     "-m",
     "--fee",
@@ -132,15 +130,15 @@
 
     from .plotnft_funcs import join_pool
 
     extra_params = {"pool_url": pool_url, "id": id, "fee": fee, "yes": yes}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, join_pool))
 
 
-@plotnft_cmd.command("leave", short_help="Leave a pool and return to self-farming")
+@plotnft_cmd.command("leave", help="Leave a pool and return to self-farming")
 @click.option("-y", "--yes", help="No prompts", is_flag=True)
 @click.option("-i", "--id", help="ID of the wallet to use", type=int, default=None, show_default=True, required=True)
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option(
     "-m",
     "--fee",
     help="Set the fees per transaction, in XCH. Fee is charged TWICE.",
@@ -162,15 +160,15 @@
 
     from .plotnft_funcs import self_pool
 
     extra_params = {"id": id, "fee": fee, "yes": yes}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, self_pool))
 
 
-@plotnft_cmd.command("inspect", short_help="Get Detailed plotnft information as JSON")
+@plotnft_cmd.command("inspect", help="Get Detailed plotnft information as JSON")
 @click.option("-i", "--id", help="ID of the wallet to use", type=int, default=None, show_default=True, required=True)
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
@@ -181,15 +179,15 @@
 
     from .plotnft_funcs import inspect_cmd
 
     extra_params = {"id": id}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, inspect_cmd))
 
 
-@plotnft_cmd.command("claim", short_help="Claim rewards from a plot NFT")
+@plotnft_cmd.command("claim", help="Claim rewards from a plot NFT")
 @click.option("-i", "--id", help="ID of the wallet to use", type=int, default=None, show_default=True, required=True)
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option(
     "-m",
     "--fee",
     help="Set the fees per transaction, in XCH.",
     type=str,
@@ -212,15 +210,15 @@
 
     extra_params = {"id": id, "fee": fee}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, claim_cmd))
 
 
 @plotnft_cmd.command(
     "change_payout_instructions",
-    short_help="Change the payout instructions for a pool. To get the launcher id, use plotnft show.",
+    help="Change the payout instructions for a pool. To get the launcher id, use plotnft show.",
 )
 @click.option("-l", "--launcher_id", help="Launcher ID of the plotnft", type=str, required=True)
 @click.option("-a", "--address", help="New address for payout instructions", type=str, required=True)
 def change_payout_instructions_cmd(launcher_id: str, address: str) -> None:
     import asyncio
 
     from .plotnft_funcs import change_payout_instructions
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/plotnft_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/plotnft_funcs.py`

 * *Files 1% similar despite different names*

```diff
@@ -169,16 +169,15 @@
     if pool_wallet_info.current.state == PoolSingletonState.LEAVING_POOL.value:
         expected_leave_height = pool_wallet_info.singleton_block_height + pool_wallet_info.current.relative_lock_height
         if pool_wallet_info.target is not None:
             print(f"Expected to leave after block height: {expected_leave_height}")
 
 
 async def show(args: Dict[str, Any], wallet_client: WalletRpcClient, fingerprint: int) -> None:
-    async with get_any_service_client(FarmerRpcClient) as node_config_fp:
-        farmer_client, config, _ = node_config_fp
+    async with get_any_service_client(FarmerRpcClient) as (farmer_client, config):
         if farmer_client is not None:
             address_prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
             summaries_response = await wallet_client.get_wallets()
             wallet_id_passed_in = args.get("id", None)
             pool_state_list = (await farmer_client.get_pool_state())["pool_state"]
             pool_state_dict: Dict[bytes32, Dict[str, Any]] = {
                 bytes32.from_hexstr(pool_state_item["pool_config"]["launcher_id"]): pool_state_item
@@ -218,16 +217,15 @@
                             pool_state_dict.get(pool_wallet_info.launcher_id),
                         )
                         print("")
 
 
 async def get_login_link(launcher_id_str: str) -> None:
     launcher_id: bytes32 = bytes32.from_hexstr(launcher_id_str)
-    async with get_any_service_client(FarmerRpcClient) as node_config_fp:
-        farmer_client, _, _ = node_config_fp
+    async with get_any_service_client(FarmerRpcClient) as (farmer_client, _):
         if farmer_client is not None:
             login_link: Optional[str] = await farmer_client.get_pool_login_link(launcher_id)
             if login_link is None:
                 print("Was not able to get login link.")
             else:
                 print(login_link)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/plots.py` & `chia-blockchain-2.0.0b1/chia/cmds/plots.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,27 +23,27 @@
         + " Scan and check plots with 'chia plots check'"
     )
     print()
     for str_path in get_plot_directories(root_path):
         print(f"{str_path}")
 
 
-@click.group("plots", short_help="Manage your plots")
+@click.group("plots", help="Manage your plots")
 @click.pass_context
 def plots_cmd(ctx: click.Context):
     """Create, add, remove and check your plots"""
     from chia.util.chia_logging import initialize_logging
 
     root_path: Path = ctx.obj["root_path"]
     if not root_path.is_dir():
         raise RuntimeError("Please initialize (or migrate) your config directory with 'chia init'")
     initialize_logging("", {"log_level": "INFO", "log_stdout": True}, root_path)
 
 
-@plots_cmd.command("create", short_help="Create plots")
+@plots_cmd.command("create", help="Create plots")
 @click.option("-k", "--size", help="Plot size", type=int, default=32, show_default=True)
 @click.option("--override-k", help="Force size smaller than 32", default=False, show_default=True, is_flag=True)
 @click.option("-n", "--num", help="Number of plots or challenges", type=int, default=1, show_default=True)
 @click.option("-b", "--buffer", help="Megabytes for sort/plot buffer", type=int, default=3389, show_default=True)
 @click.option("-r", "--num_threads", help="Number of threads to use", type=int, default=2, show_default=True)
 @click.option("-u", "--buckets", help="Number of buckets", type=int, default=128, show_default=True)
 @click.option(
@@ -155,15 +155,15 @@
     if not exclude_final_dir:
         try:
             add_plot_directory(root_path, final_dir)
         except ValueError as e:
             print(e)
 
 
-@plots_cmd.command("check", short_help="Checks plots")
+@plots_cmd.command("check", help="Checks plots")
 @click.option("-n", "--num", help="Number of plots or challenges", type=int, default=None)
 @click.option(
     "-g",
     "--grep_string",
     help="Shows only plots that contain the string in the filename or directory name",
     type=str,
     default=None,
@@ -176,15 +176,15 @@
     ctx: click.Context, num: int, grep_string: str, list_duplicates: bool, debug_show_memo: bool, challenge_start: int
 ):
     from chia.plotting.check_plots import check_plots
 
     check_plots(ctx.obj["root_path"], num, challenge_start, grep_string, list_duplicates, debug_show_memo)
 
 
-@plots_cmd.command("add", short_help="Adds a directory of plots")
+@plots_cmd.command("add", help="Adds a directory of plots")
 @click.option(
     "-d",
     "--final_dir",
     help="Final directory for plots (relative or absolute)",
     type=click.Path(),
     default=".",
     show_default=True,
@@ -196,15 +196,15 @@
     try:
         add_plot_directory(ctx.obj["root_path"], final_dir)
         print(f"Successfully added: {final_dir}")
     except ValueError as e:
         print(e)
 
 
-@plots_cmd.command("remove", short_help="Removes a directory of plots from config.yaml")
+@plots_cmd.command("remove", help="Removes a directory of plots from config.yaml")
 @click.option(
     "-d",
     "--final_dir",
     help="Final directory for plots (relative or absolute)",
     type=click.Path(),
     default=".",
     show_default=True,
@@ -212,11 +212,11 @@
 @click.pass_context
 def remove_cmd(ctx: click.Context, final_dir: str):
     from chia.plotting.util import remove_plot_directory
 
     remove_plot_directory(ctx.obj["root_path"], final_dir)
 
 
-@plots_cmd.command("show", short_help="Shows the directory of current plots")
+@plots_cmd.command("show", help="Shows the directory of current plots")
 @click.pass_context
 def show_cmd(ctx: click.Context):
     show_plots(ctx.obj["root_path"])
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/rpc.py` & `chia-blockchain-2.0.0b1/chia/cmds/rpc.py`

 * *Files 0% similar despite different names*

```diff
@@ -48,15 +48,15 @@
     print(json.dumps(json_dict, indent=4, sort_keys=True))
 
 
 def get_routes(service: str, config: Dict[str, Any]) -> Dict[str, Any]:
     return asyncio.run(call_endpoint(service, "get_routes", {}, config))
 
 
-@click.group("rpc", short_help="RPC Client")
+@click.group("rpc", help="RPC Client")
 def rpc_cmd() -> None:
     pass
 
 
 @rpc_cmd.command("endpoints", help="Print all endpoints of a service")
 @click.argument("service", type=click.Choice(services))
 def endpoints_cmd(service: str) -> None:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/show.py` & `chia-blockchain-2.0.0b1/chia/cmds/show.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from typing import Optional
 
 import click
 
 from chia.cmds.show_funcs import show_async
 
 
-@click.command("show", short_help="Show node information", no_args_is_help=True)
+@click.command("show", help="Show node information", no_args_is_help=True)
 @click.option(
     "-p",
     "--rpc-port",
     help=(
         "Set the port where the Full Node is hosting the RPC interface. "
         "See the rpc_port under full_node in config.yaml"
     ),
@@ -30,29 +30,27 @@
 @click.option(
     "-c", "--connections", help="List nodes connected to this Full Node", is_flag=True, type=bool, default=False
 )
 @click.option("-a", "--add-connection", help="Connect to another Full Node by ip:port", type=str, default="")
 @click.option(
     "-r", "--remove-connection", help="Remove a Node by the first 8 characters of NodeID", type=str, default=""
 )
-@click.option(
-    "-bh", "--block-header-hash-by-height", help="Look up a block header hash by block height", type=str, default=""
-)
+@click.option("-bh", "--block-header-hash-by-height", help="Look up a block header hash by block height", type=int)
 @click.option("-b", "--block-by-header-hash", help="Look up a block by block header hash", type=str, default="")
 @click.pass_context
 def show_cmd(
     ctx: click.Context,
     rpc_port: Optional[int],
     wallet_rpc_port: Optional[int],
     fee: bool,
     state: bool,
     connections: bool,
     add_connection: str,
     remove_connection: str,
-    block_header_hash_by_height: str,
+    block_header_hash_by_height: Optional[int],
     block_by_header_hash: str,
 ) -> None:
     import asyncio
 
     if connections:
         print("'chia show -c' has been renamed to 'chia peer -c' ")
     if add_connection != "":
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/show_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/show_funcs.py`

 * *Files 2% similar despite different names*

```diff
@@ -95,18 +95,17 @@
 ) -> None:
     import time
 
     from chia.consensus.block_record import BlockRecord
     from chia.types.blockchain_format.sized_bytes import bytes32
     from chia.types.full_block import FullBlock
     from chia.util.bech32m import encode_puzzle_hash
-    from chia.util.byte_types import hexstr_to_bytes
 
-    block: Optional[BlockRecord] = await node_client.get_block_record(hexstr_to_bytes(block_by_header_hash))
-    full_block: Optional[FullBlock] = await node_client.get_block(hexstr_to_bytes(block_by_header_hash))
+    block: Optional[BlockRecord] = await node_client.get_block_record(bytes32.from_hexstr(block_by_header_hash))
+    full_block: Optional[FullBlock] = await node_client.get_block(bytes32.from_hexstr(block_by_header_hash))
     # Would like to have a verbose flag for this
     if block is not None:
         assert full_block is not None
         prev_b = await node_client.get_block_record(block.prev_hash)
         if prev_b is not None:
             difficulty = block.weight - prev_b.weight
         else:
@@ -187,30 +186,29 @@
 
 
 async def show_async(
     rpc_port: Optional[int],
     root_path: Path,
     print_fee_info_flag: bool,
     print_state: bool,
-    block_header_hash_by_height: str,
+    block_header_hash_by_height: Optional[int],
     block_by_header_hash: str,
 ) -> None:
     from chia.cmds.cmds_util import get_any_service_client
 
-    async with get_any_service_client(FullNodeRpcClient, rpc_port, root_path) as node_config_fp:
-        node_client, config, _ = node_config_fp
+    async with get_any_service_client(FullNodeRpcClient, rpc_port, root_path) as (node_client, config):
         if node_client is not None:
             # Check State
             if print_state:
                 if await print_blockchain_state(node_client, config) is True:
                     return None  # if no blockchain is found
             if print_fee_info_flag:
                 await print_fee_info(node_client)
             # Get Block Information
-            if block_header_hash_by_height != "":
+            if block_header_hash_by_height is not None:
                 block_header = await node_client.get_block_record_by_height(block_header_hash_by_height)
                 if block_header is not None:
                     print(f"Header hash of block {block_header_hash_by_height}: {block_header.header_hash.hex()}")
                 else:
                     print("Block height", block_header_hash_by_height, "not found")
             if block_by_header_hash != "":
                 await print_block_from_hash(node_client, config, block_by_header_hash)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/sim.py` & `chia-blockchain-2.0.0b1/chia/cmds/sim.py`

 * *Ordering differences only*

 * *Files 22% similar despite different names*

```diff
@@ -1,216 +1,216 @@
-from __future__ import annotations
-
-import asyncio
-from pathlib import Path
-from typing import Any, Optional
-
-import click
-
-from chia.cmds.sim_funcs import async_config_wizard, farm_blocks, print_status, revert_block_height, set_auto_farm
-from chia.util.default_root import SIMULATOR_ROOT_PATH
-
-
-@click.group("sim", help="Configure and make requests to a Chia Simulator Full Node")
-@click.option(
-    "-p",
-    "--rpc-port",
-    help=(
-        "Set the port where the Simulator is hosting the RPC interface. "
-        "See the rpc_port under full_node in config.yaml"
-    ),
-    type=int,
-    default=None,
-)
-@click.option(
-    "--root-path", default=SIMULATOR_ROOT_PATH, help="Simulator root folder.", type=click.Path(), show_default=True
-)
-@click.option(
-    "-n",
-    "--simulator-name",
-    help="This name is used to determine the sub folder to use in the simulator root folder.",
-    type=str,
-    default="main",
-)
-@click.pass_context
-def sim_cmd(ctx: click.Context, rpc_port: Optional[int], root_path: str, simulator_name: str) -> None:
-    ctx.ensure_object(dict)
-    ctx.obj["root_path"] = Path(root_path) / simulator_name
-    ctx.obj["sim_name"] = simulator_name
-    ctx.obj["rpc_port"] = rpc_port
-
-
-@sim_cmd.command("create", help="Guides you through the process of setting up a Chia Simulator")
-@click.option("-f", "--fingerprint", type=int, required=False, help="Use your fingerprint to skip the key prompt")
-@click.option(
-    "-r",
-    "--reward-address",
-    type=str,
-    required=False,
-    help="Use this address instead of the default farming address.",
-)
-@click.option(
-    "-p", "--plot-directory", type=str, required=False, help="Use a different directory then 'simulator/plots'."
-)
-@click.option("-m", "--mnemonic", type=str, required=False, help="Add to keychain and use a specific mnemonic.")
-@click.option("-a", "--auto-farm", type=bool, default=None, help="Enable or Disable auto farming")
-@click.option(
-    "-d",
-    "--docker-mode",
-    is_flag=True,
-    hidden=True,
-    help="Run non-interactively in Docker Mode, & generate a new key if keychain is empty.",
-)
-@click.option("-b", "--no-bitfield", type=bool, is_flag=True, help="Do not use bitfield when generating plots")
-@click.pass_context
-def create_simulator_config(
-    ctx: click.Context,
-    fingerprint: Optional[int],
-    reward_address: Optional[str],
-    plot_directory: Optional[str],
-    mnemonic: Optional[str],
-    auto_farm: Optional[bool],
-    docker_mode: bool,
-    no_bitfield: bool,
-) -> None:
-    print(f"Using this Directory: {ctx.obj['root_path']}\n")
-    if fingerprint and mnemonic:
-        print("You can't use both a fingerprint and a mnemonic. Please choose one.")
-        return None
-    asyncio.run(
-        async_config_wizard(
-            ctx.obj["root_path"],
-            fingerprint,
-            reward_address,
-            plot_directory,
-            mnemonic,
-            auto_farm,
-            docker_mode,
-            not no_bitfield,
-        )
-    )
-
-
-@sim_cmd.command("start", help="Start service groups while automatically using the right chia_root.")
-@click.option("-r", "--restart", is_flag=True, help="Restart running services")
-@click.option("-w", "--wallet", is_flag=True, help="Start wallet")
-@click.pass_context
-def sim_start_cmd(ctx: click.Context, restart: bool, wallet: bool) -> None:
-    from chia.cmds.start import start_cmd
-
-    group: tuple[str, ...] = ("simulator",)
-    if wallet:
-        group += ("wallet",)
-    ctx.invoke(start_cmd, restart=restart, group=group)
-
-
-@sim_cmd.command("stop", help="Stop running services while automatically using the right chia_root.")
-@click.option("-d", "--daemon", is_flag=True, help="Stop daemon")
-@click.option("-w", "--wallet", is_flag=True, help="Stop wallet")
-@click.pass_context
-def sim_stop_cmd(ctx: click.Context, daemon: bool, wallet: bool) -> None:
-    from chia.cmds.stop import stop_cmd
-
-    group: Any = ("simulator",)
-    if wallet:
-        group += ("wallet",)
-    ctx.invoke(stop_cmd, daemon=daemon, group=group)
-
-
-@sim_cmd.command("status", help="Get information about the state of the simulator.")
-@click.option("-f", "--fingerprint", type=int, help="Get detailed information on this fingerprint.")
-@click.option("--show-key/--no-show-key", help="Show detailed key information.")
-@click.option("-c", "--show-coins", is_flag=True, help="Show all unspent coins.")
-@click.option("-i", "--include-rewards", is_flag=True, help="Include reward coins when showing coins.")
-@click.option("-a", "--show-addresses", is_flag=True, help="Show the balances of all addresses.")
-@click.pass_context
-def status_cmd(
-    ctx: click.Context,
-    fingerprint: Optional[int],
-    show_key: bool,
-    show_coins: bool,
-    include_rewards: bool,
-    show_addresses: bool,
-) -> None:
-    asyncio.run(
-        print_status(
-            ctx.obj["rpc_port"],
-            ctx.obj["root_path"],
-            fingerprint,
-            show_key,
-            show_coins,
-            include_rewards,
-            show_addresses,
-        )
-    )
-
-
-@sim_cmd.command("revert", help="Reset chain to a previous block height.")
-@click.option("-b", "--blocks", type=int, default=1, help="Number of blocks to go back.")
-@click.option("-n", "--new-blocks", type=int, default=1, help="Number of new blocks to add during a reorg.")
-@click.option("-r", "--reset", is_flag=True, help="Reset the chain to the genesis block")
-@click.option(
-    "-f",
-    "--force",
-    is_flag=True,
-    help="Forcefully delete blocks, this is not a reorg but might be needed in very special circumstances."
-    "  Note: Use with caution, this will break all wallets.",
-)
-@click.option("-d", "--disable-prompt", is_flag=True, help="Disable confirmation prompt when force reverting.")
-@click.pass_context
-def revert_cmd(
-    ctx: click.Context, blocks: int, new_blocks: int, reset: bool, force: bool, disable_prompt: bool
-) -> None:
-    if force and not disable_prompt:
-        input_str = (
-            "Are you sure you want to force delete blocks? This should only ever be used in special circumstances,"
-            " and will break all wallets. \nPress 'y' to continue, or any other button to exit: "
-        )
-        if input(input_str) != "y":
-            return
-    if reset and not force:
-        print("\n The force flag (-f) is required to reset the chain to the genesis block. \n")
-        return
-    if reset and blocks != 1:
-        print("\nBlocks, '-b' must not be set if all blocks are selected by reset, '-r'. Exiting.\n")
-        return
-    asyncio.run(
-        revert_block_height(
-            ctx.obj["rpc_port"],
-            ctx.obj["root_path"],
-            blocks,
-            new_blocks,
-            reset,
-            force,
-        )
-    )
-
-
-@sim_cmd.command("farm", help="Farm blocks")
-@click.option("-b", "--blocks", type=int, default=1, help="Amount of blocks to create")
-@click.option("-n", "--non-transaction", is_flag=True, help="Allow non-transaction blocks")
-@click.option("-a", "--target-address", type=str, default="", help="Block reward address")
-@click.pass_context
-def farm_cmd(ctx: click.Context, blocks: int, non_transaction: bool, target_address: str) -> None:
-    asyncio.run(
-        farm_blocks(
-            ctx.obj["rpc_port"],
-            ctx.obj["root_path"],
-            blocks,
-            not non_transaction,
-            target_address,
-        )
-    )
-
-
-@sim_cmd.command("autofarm", help="Enable or disable auto farming on transaction submission")
-@click.argument("set-autofarm", type=click.Choice(["on", "off"]), nargs=1, required=True)
-@click.pass_context
-def autofarm_cmd(ctx: click.Context, set_autofarm: str) -> None:
-    autofarm = bool(set_autofarm == "on")
-    asyncio.run(
-        set_auto_farm(
-            ctx.obj["rpc_port"],
-            ctx.obj["root_path"],
-            autofarm,
-        )
-    )
+from __future__ import annotations
+
+import asyncio
+from pathlib import Path
+from typing import Any, Optional
+
+import click
+
+from chia.cmds.sim_funcs import async_config_wizard, farm_blocks, print_status, revert_block_height, set_auto_farm
+from chia.util.default_root import SIMULATOR_ROOT_PATH
+
+
+@click.group("sim", help="Configure and make requests to a Chia Simulator Full Node")
+@click.option(
+    "-p",
+    "--rpc-port",
+    help=(
+        "Set the port where the Simulator is hosting the RPC interface. "
+        "See the rpc_port under full_node in config.yaml"
+    ),
+    type=int,
+    default=None,
+)
+@click.option(
+    "--root-path", default=SIMULATOR_ROOT_PATH, help="Simulator root folder.", type=click.Path(), show_default=True
+)
+@click.option(
+    "-n",
+    "--simulator-name",
+    help="This name is used to determine the sub folder to use in the simulator root folder.",
+    type=str,
+    default="main",
+)
+@click.pass_context
+def sim_cmd(ctx: click.Context, rpc_port: Optional[int], root_path: str, simulator_name: str) -> None:
+    ctx.ensure_object(dict)
+    ctx.obj["root_path"] = Path(root_path) / simulator_name
+    ctx.obj["sim_name"] = simulator_name
+    ctx.obj["rpc_port"] = rpc_port
+
+
+@sim_cmd.command("create", help="Guides you through the process of setting up a Chia Simulator")
+@click.option("-f", "--fingerprint", type=int, required=False, help="Use your fingerprint to skip the key prompt")
+@click.option(
+    "-r",
+    "--reward-address",
+    type=str,
+    required=False,
+    help="Use this address instead of the default farming address.",
+)
+@click.option(
+    "-p", "--plot-directory", type=str, required=False, help="Use a different directory then 'simulator/plots'."
+)
+@click.option("-m", "--mnemonic", type=str, required=False, help="Add to keychain and use a specific mnemonic.")
+@click.option("-a", "--auto-farm", type=bool, default=None, help="Enable or Disable auto farming")
+@click.option(
+    "-d",
+    "--docker-mode",
+    is_flag=True,
+    hidden=True,
+    help="Run non-interactively in Docker Mode, & generate a new key if keychain is empty.",
+)
+@click.option("-b", "--no-bitfield", type=bool, is_flag=True, help="Do not use bitfield when generating plots")
+@click.pass_context
+def create_simulator_config(
+    ctx: click.Context,
+    fingerprint: Optional[int],
+    reward_address: Optional[str],
+    plot_directory: Optional[str],
+    mnemonic: Optional[str],
+    auto_farm: Optional[bool],
+    docker_mode: bool,
+    no_bitfield: bool,
+) -> None:
+    print(f"Using this Directory: {ctx.obj['root_path']}\n")
+    if fingerprint and mnemonic:
+        print("You can't use both a fingerprint and a mnemonic. Please choose one.")
+        return None
+    asyncio.run(
+        async_config_wizard(
+            ctx.obj["root_path"],
+            fingerprint,
+            reward_address,
+            plot_directory,
+            mnemonic,
+            auto_farm,
+            docker_mode,
+            not no_bitfield,
+        )
+    )
+
+
+@sim_cmd.command("start", help="Start service groups while automatically using the right chia_root.")
+@click.option("-r", "--restart", is_flag=True, help="Restart running services")
+@click.option("-w", "--wallet", is_flag=True, help="Start wallet")
+@click.pass_context
+def sim_start_cmd(ctx: click.Context, restart: bool, wallet: bool) -> None:
+    from chia.cmds.start import start_cmd
+
+    group: tuple[str, ...] = ("simulator",)
+    if wallet:
+        group += ("wallet",)
+    ctx.invoke(start_cmd, restart=restart, group=group)
+
+
+@sim_cmd.command("stop", help="Stop running services while automatically using the right chia_root.")
+@click.option("-d", "--daemon", is_flag=True, help="Stop daemon")
+@click.option("-w", "--wallet", is_flag=True, help="Stop wallet")
+@click.pass_context
+def sim_stop_cmd(ctx: click.Context, daemon: bool, wallet: bool) -> None:
+    from chia.cmds.stop import stop_cmd
+
+    group: Any = ("simulator",)
+    if wallet:
+        group += ("wallet",)
+    ctx.invoke(stop_cmd, daemon=daemon, group=group)
+
+
+@sim_cmd.command("status", help="Get information about the state of the simulator.")
+@click.option("-f", "--fingerprint", type=int, help="Get detailed information on this fingerprint.")
+@click.option("--show-key/--no-show-key", help="Show detailed key information.")
+@click.option("-c", "--show-coins", is_flag=True, help="Show all unspent coins.")
+@click.option("-i", "--include-rewards", is_flag=True, help="Include reward coins when showing coins.")
+@click.option("-a", "--show-addresses", is_flag=True, help="Show the balances of all addresses.")
+@click.pass_context
+def status_cmd(
+    ctx: click.Context,
+    fingerprint: Optional[int],
+    show_key: bool,
+    show_coins: bool,
+    include_rewards: bool,
+    show_addresses: bool,
+) -> None:
+    asyncio.run(
+        print_status(
+            ctx.obj["rpc_port"],
+            ctx.obj["root_path"],
+            fingerprint,
+            show_key,
+            show_coins,
+            include_rewards,
+            show_addresses,
+        )
+    )
+
+
+@sim_cmd.command("revert", help="Reset chain to a previous block height.")
+@click.option("-b", "--blocks", type=int, default=1, help="Number of blocks to go back.")
+@click.option("-n", "--new-blocks", type=int, default=1, help="Number of new blocks to add during a reorg.")
+@click.option("-r", "--reset", is_flag=True, help="Reset the chain to the genesis block")
+@click.option(
+    "-f",
+    "--force",
+    is_flag=True,
+    help="Forcefully delete blocks, this is not a reorg but might be needed in very special circumstances."
+    "  Note: Use with caution, this will break all wallets.",
+)
+@click.option("-d", "--disable-prompt", is_flag=True, help="Disable confirmation prompt when force reverting.")
+@click.pass_context
+def revert_cmd(
+    ctx: click.Context, blocks: int, new_blocks: int, reset: bool, force: bool, disable_prompt: bool
+) -> None:
+    if force and not disable_prompt:
+        input_str = (
+            "Are you sure you want to force delete blocks? This should only ever be used in special circumstances,"
+            " and will break all wallets. \nPress 'y' to continue, or any other button to exit: "
+        )
+        if input(input_str) != "y":
+            return
+    if reset and not force:
+        print("\n The force flag (-f) is required to reset the chain to the genesis block. \n")
+        return
+    if reset and blocks != 1:
+        print("\nBlocks, '-b' must not be set if all blocks are selected by reset, '-r'. Exiting.\n")
+        return
+    asyncio.run(
+        revert_block_height(
+            ctx.obj["rpc_port"],
+            ctx.obj["root_path"],
+            blocks,
+            new_blocks,
+            reset,
+            force,
+        )
+    )
+
+
+@sim_cmd.command("farm", help="Farm blocks")
+@click.option("-b", "--blocks", type=int, default=1, help="Amount of blocks to create")
+@click.option("-n", "--non-transaction", is_flag=True, help="Allow non-transaction blocks")
+@click.option("-a", "--target-address", type=str, default="", help="Block reward address")
+@click.pass_context
+def farm_cmd(ctx: click.Context, blocks: int, non_transaction: bool, target_address: str) -> None:
+    asyncio.run(
+        farm_blocks(
+            ctx.obj["rpc_port"],
+            ctx.obj["root_path"],
+            blocks,
+            not non_transaction,
+            target_address,
+        )
+    )
+
+
+@sim_cmd.command("autofarm", help="Enable or disable auto farming on transaction submission")
+@click.argument("set-autofarm", type=click.Choice(["on", "off"]), nargs=1, required=True)
+@click.pass_context
+def autofarm_cmd(ctx: click.Context, set_autofarm: str) -> None:
+    autofarm = bool(set_autofarm == "on")
+    asyncio.run(
+        set_auto_farm(
+            ctx.obj["rpc_port"],
+            ctx.obj["root_path"],
+            autofarm,
+        )
+    )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/sim_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/sim_funcs.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,515 +1,498 @@
-from __future__ import annotations
-
-import asyncio
-import os
-import sys
-from pathlib import Path, PureWindowsPath
-from random import randint
-from typing import Any, Dict, List, Optional
-
-from aiohttp import ClientConnectorError
-from blspy import PrivateKey
-
-from chia.cmds.cmds_util import get_any_service_client
-from chia.cmds.start_funcs import async_start
-from chia.consensus.coinbase import create_puzzlehash_for_pk
-from chia.simulator.simulator_full_node_rpc_client import SimulatorFullNodeRpcClient
-from chia.types.blockchain_format.sized_bytes import bytes32
-from chia.types.coin_record import CoinRecord
-from chia.util.bech32m import decode_puzzle_hash, encode_puzzle_hash
-from chia.util.config import load_config, save_config
-from chia.util.errors import KeychainFingerprintExists
-from chia.util.ints import uint32
-from chia.util.keychain import Keychain, bytes_to_mnemonic
-from chia.wallet.derive_keys import (
-    master_sk_to_farmer_sk,
-    master_sk_to_pool_sk,
-    master_sk_to_wallet_sk,
-    master_sk_to_wallet_sk_unhardened,
-)
-
-
-def get_ph_from_fingerprint(fingerprint: int, key_id: int = 1) -> bytes32:
-    priv_key_and_entropy = Keychain().get_private_key_by_fingerprint(fingerprint)
-    if priv_key_and_entropy is None:
-        raise Exception("Fingerprint not found")
-    private_key = priv_key_and_entropy[0]
-    sk_for_wallet_id: PrivateKey = master_sk_to_wallet_sk(private_key, uint32(key_id))
-    puzzle_hash: bytes32 = create_puzzlehash_for_pk(sk_for_wallet_id.get_g1())
-    return puzzle_hash
-
-
-def create_chia_directory(
-    chia_root: Path,
-    fingerprint: int,
-    farming_address: Optional[str],
-    plot_directory: Optional[str],
-    auto_farm: Optional[bool],
-    docker_mode: bool,
-) -> Dict[str, Any]:
-    """
-    This function creates a new chia directory and returns a heavily modified config,
-    suitable for use in the simulator.
-    """
-    from chia.cmds.init_funcs import chia_init
-
-    if not chia_root.is_dir() or not Path(chia_root / "config" / "config.yaml").exists():
-        # create chia directories & load config
-        chia_init(chia_root, testnet=True, fix_ssl_permissions=True)
-        config: Dict[str, Any] = load_config(chia_root, "config.yaml")
-        # apply standard block-tools config.
-        config["full_node"]["send_uncompact_interval"] = 0
-        config["full_node"]["target_uncompact_proofs"] = 30
-        config["full_node"]["peer_connect_interval"] = 50
-        config["full_node"]["sanitize_weight_proof_only"] = False
-        config["logging"]["log_level"] = "INFO"  # extra logs for easier development
-        # make sure we don't try to connect to other nodes.
-        config["full_node"]["introducer_peer"] = None
-        config["wallet"]["introducer_peer"] = None
-        config["full_node"]["dns_servers"] = []
-        config["wallet"]["dns_servers"] = []
-        # create custom testnet (simulator0)
-        config["network_overrides"]["constants"]["simulator0"] = config["network_overrides"]["constants"][
-            "testnet0"
-        ].copy()
-        config["network_overrides"]["config"]["simulator0"] = config["network_overrides"]["config"]["testnet0"].copy()
-        sim_genesis = "eb8c4d20b322be8d9fddbf9412016bdffe9a2901d7edb0e364e94266d0e095f7"
-        config["network_overrides"]["constants"]["simulator0"]["GENESIS_CHALLENGE"] = sim_genesis
-        # tell services to use simulator0
-        config["selected_network"] = "simulator0"
-        config["wallet"]["selected_network"] = "simulator0"
-        config["full_node"]["selected_network"] = "simulator0"
-        if not docker_mode:  # We want predictable ports for our docker image.
-            # set ports and networks, we don't want to cause a port conflict.
-            port_offset = randint(1, 20000)
-            config["daemon_port"] -= port_offset
-            config["network_overrides"]["config"]["simulator0"]["default_full_node_port"] = 38444 + port_offset
-            # wallet
-            config["wallet"]["port"] += port_offset
-            config["wallet"]["rpc_port"] += port_offset
-            # full node
-            config["full_node"]["port"] -= port_offset
-            config["full_node"]["rpc_port"] += port_offset
-            # connect wallet to full node
-            config["wallet"]["full_node_peer"]["port"] = config["full_node"]["port"]
-            config["full_node"]["wallet_peer"]["port"] = config["wallet"]["port"]
-            # ui
-            config["ui"]["daemon_port"] = config["daemon_port"]
-        else:
-            config["self_hostname"] = "0.0.0.0"  # Bind to all interfaces.
-            config["logging"]["log_stdout"] = True  # Log to console.
-    else:
-        config = load_config(chia_root, "config.yaml")
-    # simulator overrides
-    config["simulator"]["key_fingerprint"] = fingerprint
-    if farming_address is None:
-        prefix = config["network_overrides"]["config"]["simulator0"]["address_prefix"]
-        farming_address = encode_puzzle_hash(get_ph_from_fingerprint(fingerprint), prefix)
-    config["simulator"]["farming_address"] = farming_address
-    if plot_directory is not None:
-        config["simulator"]["plot_directory"] = plot_directory
-    # Temporary change to fix win / linux differences.
-    config["simulator"]["plot_directory"] = str(Path(config["simulator"]["plot_directory"]))
-    if "//" in config["simulator"]["plot_directory"] and os.name != "nt":
-        # if we're on linux, we need to convert to a linux path.
-        config["simulator"]["plot_directory"] = str(PureWindowsPath(config["simulator"]["plot_directory"]).as_posix())
-    config["simulator"]["auto_farm"] = auto_farm if auto_farm is not None else True
-    farming_ph = decode_puzzle_hash(farming_address)
-    # modify genesis block to give the user the reward
-    simulator_consts = config["network_overrides"]["constants"]["simulator0"]
-    simulator_consts["GENESIS_PRE_FARM_FARMER_PUZZLE_HASH"] = farming_ph.hex()
-    simulator_consts["GENESIS_PRE_FARM_POOL_PUZZLE_HASH"] = farming_ph.hex()
-    # save config and return the config
-    save_config(chia_root, "config.yaml", config)
-    return config
-
-
-def display_key_info(fingerprint: int, prefix: str) -> None:
-    """
-    Display key info for a given fingerprint, similar to the output of `chia keys show`.
-    """
-    print(f"Using fingerprint {fingerprint}")
-    private_key_and_seed = Keychain().get_private_key_by_fingerprint(fingerprint)
-    if private_key_and_seed is None:
-        print(f"Fingerprint {fingerprint} not found")
-        return
-    sk, seed = private_key_and_seed
-    print("\nFingerprint:", sk.get_g1().get_fingerprint())
-    print("Master public key (m):", sk.get_g1())
-    print("Farmer public key (m/12381/8444/0/0):", master_sk_to_farmer_sk(sk).get_g1())
-    print("Pool public key (m/12381/8444/1/0):", master_sk_to_pool_sk(sk).get_g1())
-    first_wallet_sk: PrivateKey = master_sk_to_wallet_sk_unhardened(sk, uint32(0))
-    wallet_address: str = encode_puzzle_hash(create_puzzlehash_for_pk(first_wallet_sk.get_g1()), prefix)
-    print(f"First wallet address: {wallet_address}")
-    assert seed is not None
-    print("Master private key (m):", bytes(sk).hex())
-    print("First wallet secret key (m/12381/8444/2/0):", master_sk_to_wallet_sk(sk, uint32(0)))
-    mnemonic = bytes_to_mnemonic(seed)
-    print("  Mnemonic seed (24 secret words):")
-    print(f"{mnemonic} \n")
-
-
-def generate_and_return_fingerprint(mnemonic: Optional[str] = None) -> int:
-    """
-    Generate and add new PrivateKey and return its fingerprint.
-    """
-    from chia.util.keychain import generate_mnemonic
-
-    if mnemonic is None:
-        print("Generating private key")
-        mnemonic = generate_mnemonic()
-    try:
-        sk = Keychain().add_private_key(mnemonic, None)
-        fingerprint: int = sk.get_g1().get_fingerprint()
-    except KeychainFingerprintExists as e:
-        fingerprint = e.fingerprint
-        print(f"Fingerprint: {fingerprint} for provided private key already exists.")
-        return fingerprint
-    print(f"Added private key with public key fingerprint {fingerprint}")
-    return fingerprint
-
-
-def select_fingerprint(
-    fingerprint: Optional[int] = None, mnemonic_string: Optional[str] = None, auto_generate_key: bool = False
-) -> Optional[int]:
-    """
-    Either select an existing fingerprint or create one and return it.
-    """
-    if mnemonic_string:
-        fingerprint = generate_and_return_fingerprint(mnemonic_string)
-    fingerprints: list[int] = [pk.get_fingerprint() for pk in Keychain().get_all_public_keys()]
-    if fingerprint is not None and fingerprint in fingerprints:
-        return fingerprint
-    elif fingerprint is not None and fingerprint not in fingerprints:
-        print(f"Invalid Fingerprint. Fingerprint {fingerprint} was not found.")
-        return None
-    if auto_generate_key and len(fingerprints) == 1:
-        return fingerprints[0]
-    if len(fingerprints) == 0:
-        if not auto_generate_key:
-            if (
-                input("No keys in keychain. Press 'q' to quit, or press any other key to generate a new key.").lower()
-                == "q"
-            ):
-                return None
-        # generate private key and add to wallet
-        fingerprint = generate_and_return_fingerprint()
-    else:
-        print("Fingerprints:")
-        print(
-            "If you already used one of these keys, select that fingerprint to skip the plotting process."
-            " Otherwise, select any key below."
-        )
-        for i, fp in enumerate(fingerprints):
-            row: str = f"{i + 1}) "
-            row += f"{fp}"
-            print(row)
-        val = None
-        prompt: str = f"Choose a simulator key [1-{len(fingerprints)}] ('q' to quit, or 'g' to generate a new key): "
-        while val is None:
-            val = input(prompt)
-            if val == "q":
-                return None
-            elif val == "g":
-                fingerprint = generate_and_return_fingerprint()
-                break
-            elif not val.isdigit():
-                val = None
-            else:
-                index = int(val) - 1
-                if index < 0 or index >= len(fingerprints):
-                    print("Invalid value")
-                    val = None
-                    continue
-                else:
-                    fingerprint = fingerprints[index]
-        assert fingerprint is not None
-    return fingerprint
-
-
-async def generate_plots(config: Dict[str, Any], root_path: Path, fingerprint: int, bitfield: bool) -> None:
-    """
-    Pre-Generate plots for the new simulator instance.
-    """
-
-    from chia.simulator.block_tools import BlockTools, test_constants
-    from chia.simulator.start_simulator import PLOT_SIZE, PLOTS
-
-    farming_puzzle_hash = decode_puzzle_hash(config["simulator"]["farming_address"])
-    os.environ["CHIA_ROOT"] = str(root_path)  # change env variable, to make it match what the daemon would set it to
-
-    # create block tools and use local keychain
-    bt = BlockTools(
-        test_constants,
-        root_path,
-        automated_testing=False,
-        plot_dir=config["simulator"].get("plot_directory", "plots"),
-        keychain=Keychain(),
-    )
-    await bt.setup_keys(fingerprint=fingerprint, reward_ph=farming_puzzle_hash)
-    existing_plots = await bt.setup_plots(
-        num_og_plots=PLOTS, num_pool_plots=0, num_non_keychain_plots=0, plot_size=PLOT_SIZE, bitfield=bitfield
-    )
-    print(f"{'New plots generated.' if existing_plots else 'Using Existing Plots'}\n")
-
-
-async def get_current_height(root_path: Path) -> int:
-    async with get_any_service_client(SimulatorFullNodeRpcClient, root_path=root_path, consume_errors=False) as (
-        node_client,
-        _,
-        _,
-    ):
-        assert node_client is not None  # this cant be None, because we don't catch errors
-        num_blocks = len(await node_client.get_all_blocks())
-    return num_blocks
-
-
-async def async_config_wizard(
-    root_path: Path,
-    fingerprint: Optional[int],
-    farming_address: Optional[str],
-    plot_directory: Optional[str],
-    mnemonic_string: Optional[str],
-    auto_farm: Optional[bool],
-    docker_mode: bool,
-    bitfield: bool,
-) -> None:
-    # either return passed through fingerprint or get one
-    fingerprint = select_fingerprint(fingerprint, mnemonic_string, docker_mode)
-    if fingerprint is None:
-        # user cancelled wizard
-        return
-    # create chia directory & get config.
-    print("Creating chia directory & config...")
-    config = create_chia_directory(root_path, fingerprint, farming_address, plot_directory, auto_farm, docker_mode)
-    # Pre-generate plots by running block_tools init functions.
-    print("Please Wait, Generating plots...")
-    print("This may take up to a minute if you are on a slow machine")
-
-    await generate_plots(config, root_path, fingerprint, bitfield)
-    # final messages
-    final_farming_address = config["simulator"]["farming_address"]
-    print(f"\nFarming & Prefarm reward address: {final_farming_address}\n")
-    print("Configuration Wizard Complete.")
-    print("Starting Simulator now...\n\n")
-
-    sys.argv[0] = str(Path(sys.executable).parent / "chia")  # fix path for tests
-    await async_start(root_path, config, ("simulator",), False)
-
-    # now we make sure the simulator has a genesis block
-    print("Please wait, generating genesis block.")
-    while True:
-        try:
-            num_blocks: int = await get_current_height(root_path)
-        except ClientConnectorError:
-            await asyncio.sleep(0.25)
-        else:
-            if num_blocks == 0:
-                await farm_blocks(None, root_path, 1, True, final_farming_address)
-                print("Genesis block generated, exiting.")
-            else:
-                print("Genesis block already exists, exiting.")
-            break
-    print(f"\nMake sure your CHIA_ROOT Environment Variable is set to: {root_path}")
-
-
-def print_coin_record(
-    name: str,
-    address_prefix: str,
-    coin_record: CoinRecord,
-) -> None:
-    from datetime import datetime
-
-    coin_address = encode_puzzle_hash(coin_record.coin.puzzle_hash, address_prefix)
-    print(f"Coin 0x{coin_record.name.hex()}")
-    print(f"Wallet Address: {coin_address}")
-    print(f"Confirmed at block: {coin_record.confirmed_block_index}")
-    print(f"Spent: {f'at Block {coin_record.spent_block_index}' if coin_record.spent else 'No'}")
-    print(f"Coin Amount: {coin_record.coin.amount} {name}")
-    print(f"Parent Coin ID: 0x{coin_record.coin.parent_coin_info.hex()}")
-    print(f"Created at: {datetime.fromtimestamp(float(coin_record.timestamp)).strftime('%Y-%m-%d %H:%M:%S')}\n")
-
-
-async def print_coin_records(
-    config: Dict[str, Any],
-    node_client: SimulatorFullNodeRpcClient,
-    include_reward_coins: bool,
-    include_spent: bool = False,
-) -> None:
-    import sys
-
-    coin_records: List[CoinRecord] = await node_client.get_all_coins(include_spent)
-    coin_records = [coin_record for coin_record in coin_records if not coin_record.coinbase or include_reward_coins]
-    address_prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
-    name = "mojo"
-    paginate = False  # I might change this later.
-    if len(coin_records) != 0:
-        print("All Coins: ")
-        if paginate is True:
-            paginate = sys.stdout.isatty()
-        num_per_screen = 5 if paginate else len(coin_records)
-        # ripped from cmds/wallet_funcs.
-        for i in range(0, len(coin_records), num_per_screen):
-            for j in range(0, num_per_screen):
-                if i + j >= len(coin_records):
-                    break
-                print_coin_record(
-                    coin_record=coin_records[i + j],
-                    name=name,
-                    address_prefix=address_prefix,
-                )
-            if i + num_per_screen <= len(coin_records) and paginate:
-                print("Press q to quit, or c to continue")
-                while True:
-                    entered_key = sys.stdin.read(1)
-                    if entered_key == "q":
-                        return None
-                    elif entered_key == "c":
-                        break
-
-
-async def print_wallets(config: Dict[str, Any], node_client: SimulatorFullNodeRpcClient) -> None:
-    ph_and_amount = await node_client.get_all_puzzle_hashes()
-    address_prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
-    name = "mojo"
-    for puzzle_hash, (amount, num_tx) in ph_and_amount.items():
-        address = encode_puzzle_hash(puzzle_hash, address_prefix)
-        print(f"Address: {address} has a balance of: {amount} {name}, with a total of: {num_tx} transactions.\n")
-
-
-async def print_status(
-    rpc_port: Optional[int],
-    root_path: Path,
-    fingerprint: Optional[int],
-    show_key: bool,
-    show_coins: bool,
-    include_reward_coins: bool,
-    show_addresses: bool,
-) -> None:
-    """
-    This command allows users to easily get the status of the simulator
-    and information about the state of and the coins in the simulated blockchain.
-    """
-    from chia.cmds.show_funcs import print_blockchain_state
-    from chia.cmds.units import units
-
-    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path, fingerprint) as (
-        node_client,
-        config,
-        _,
-    ):
-        if node_client is not None:
-            # Display keychain info
-            if show_key:
-                if fingerprint is None:
-                    fingerprint = config["simulator"]["key_fingerprint"]
-                if fingerprint is not None:
-                    display_key_info(
-                        fingerprint, config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
-                    )
-                else:
-                    print(
-                        "No fingerprint in config, either rerun 'cdv sim create' "
-                        "or use --fingerprint to specify one, skipping key information."
-                    )
-            # chain status ( basically chia show -s)
-            await print_blockchain_state(node_client, config)
-            print("")
-            # farming information
-            target_ph: bytes32 = await node_client.get_farming_ph()
-            farming_coin_records = await node_client.get_coin_records_by_puzzle_hash(target_ph, False)
-            prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
-            print(
-                f"Current Farming address: {encode_puzzle_hash(target_ph, prefix)}, "
-                f"with a balance of: "
-                f"{sum(coin_records.coin.amount for coin_records in farming_coin_records) / units['chia']} TXCH."
-            )
-            if show_addresses:
-                print("All Addresses: ")
-                await print_wallets(config, node_client)
-            if show_coins:
-                await print_coin_records(config, node_client, include_reward_coins)
-
-
-async def revert_block_height(
-    rpc_port: Optional[int],
-    root_path: Path,
-    num_blocks: int,
-    num_new_blocks: int,
-    reset_chain_to_genesis: bool,
-    use_revert_blocks: bool,
-) -> None:
-    """
-    This function allows users to easily revert the chain to a previous state or perform a reorg.
-    """
-    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (
-        node_client,
-        _,
-        _,
-    ):
-        if node_client is not None:
-            if use_revert_blocks:
-                if num_new_blocks != 1:
-                    print(f"Ignoring num_new_blocks: {num_new_blocks}, because we are not performing a reorg.")
-                # in this case num_blocks is the number of blocks to delete
-                new_height: int = await node_client.revert_blocks(num_blocks, reset_chain_to_genesis)
-                print(
-                    f"All transactions in Block: {new_height + num_blocks} and above were successfully deleted, "
-                    "you should now delete & restart all wallets."
-                )
-            else:
-                # However, in this case num_blocks is the fork height.
-                new_height = await node_client.reorg_blocks(num_blocks, num_new_blocks, use_revert_blocks)
-                old_height = new_height - num_new_blocks
-                print(f"All transactions in Block: {old_height - num_blocks} and above were successfully reverted.")
-            print(f"Block Height is now: {new_height}")
-
-
-async def farm_blocks(
-    rpc_port: Optional[int],
-    root_path: Path,
-    num_blocks: int,
-    transaction_blocks: bool,
-    target_address: str,
-) -> None:
-    """
-    This function is used to generate new blocks.
-    """
-    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (
-        node_client,
-        config,
-        _,
-    ):
-        if node_client is not None:
-            if target_address == "":
-                target_address = config["simulator"]["farming_address"]
-            if target_address is None:
-                print(
-                    "No target address in config, falling back to the temporary address currently in use. "
-                    "You can use 'cdv sim create' or use --target-address to specify a different address."
-                )
-                target_ph: bytes32 = await node_client.get_farming_ph()
-            else:
-                target_ph = decode_puzzle_hash(target_address)
-            await node_client.farm_block(target_ph, num_blocks, transaction_blocks)
-            print(f"Farmed {num_blocks}{' Transaction' if transaction_blocks else ''} blocks")
-            block_height = (await node_client.get_blockchain_state())["peak"].height
-            print(f"Block Height is now: {block_height}")
-
-
-async def set_auto_farm(rpc_port: Optional[int], root_path: Path, set_autofarm: bool) -> None:
-    """
-    This function can be used to enable or disable Auto Farming.
-    """
-    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (
-        node_client,
-        _,
-        _,
-    ):
-        if node_client is not None:
-            current = await node_client.get_auto_farming()
-            if current == set_autofarm:
-                print(f"Auto farming is already {'on' if set_autofarm else 'off'}")
-                return
-            result = await node_client.set_auto_farming(set_autofarm)
-            print(f"Auto farming is now {'on' if result else 'off'}")
+from __future__ import annotations
+
+import asyncio
+import os
+import sys
+from pathlib import Path, PureWindowsPath
+from random import randint
+from typing import Any, Dict, List, Optional
+
+from aiohttp import ClientConnectorError
+from blspy import PrivateKey
+
+from chia.cmds.cmds_util import get_any_service_client
+from chia.cmds.start_funcs import async_start
+from chia.consensus.coinbase import create_puzzlehash_for_pk
+from chia.simulator.simulator_full_node_rpc_client import SimulatorFullNodeRpcClient
+from chia.types.blockchain_format.sized_bytes import bytes32
+from chia.types.coin_record import CoinRecord
+from chia.util.bech32m import decode_puzzle_hash, encode_puzzle_hash
+from chia.util.config import load_config, save_config
+from chia.util.errors import KeychainFingerprintExists
+from chia.util.ints import uint32
+from chia.util.keychain import Keychain, bytes_to_mnemonic
+from chia.wallet.derive_keys import (
+    master_sk_to_farmer_sk,
+    master_sk_to_pool_sk,
+    master_sk_to_wallet_sk,
+    master_sk_to_wallet_sk_unhardened,
+)
+
+
+def get_ph_from_fingerprint(fingerprint: int, key_id: int = 1) -> bytes32:
+    priv_key_and_entropy = Keychain().get_private_key_by_fingerprint(fingerprint)
+    if priv_key_and_entropy is None:
+        raise Exception("Fingerprint not found")
+    private_key = priv_key_and_entropy[0]
+    sk_for_wallet_id: PrivateKey = master_sk_to_wallet_sk(private_key, uint32(key_id))
+    puzzle_hash: bytes32 = create_puzzlehash_for_pk(sk_for_wallet_id.get_g1())
+    return puzzle_hash
+
+
+def create_chia_directory(
+    chia_root: Path,
+    fingerprint: int,
+    farming_address: Optional[str],
+    plot_directory: Optional[str],
+    auto_farm: Optional[bool],
+    docker_mode: bool,
+) -> Dict[str, Any]:
+    """
+    This function creates a new chia directory and returns a heavily modified config,
+    suitable for use in the simulator.
+    """
+    from chia.cmds.init_funcs import chia_init
+
+    if not chia_root.is_dir() or not Path(chia_root / "config" / "config.yaml").exists():
+        # create chia directories & load config
+        chia_init(chia_root, testnet=True, fix_ssl_permissions=True)
+        config: Dict[str, Any] = load_config(chia_root, "config.yaml")
+        # apply standard block-tools config.
+        config["full_node"]["send_uncompact_interval"] = 0
+        config["full_node"]["target_uncompact_proofs"] = 30
+        config["full_node"]["peer_connect_interval"] = 50
+        config["full_node"]["sanitize_weight_proof_only"] = False
+        config["logging"]["log_level"] = "INFO"  # extra logs for easier development
+        # make sure we don't try to connect to other nodes.
+        config["full_node"]["introducer_peer"] = None
+        config["wallet"]["introducer_peer"] = None
+        config["full_node"]["dns_servers"] = []
+        config["wallet"]["dns_servers"] = []
+        # create custom testnet (simulator0)
+        config["network_overrides"]["constants"]["simulator0"] = config["network_overrides"]["constants"][
+            "testnet0"
+        ].copy()
+        config["network_overrides"]["config"]["simulator0"] = config["network_overrides"]["config"]["testnet0"].copy()
+        sim_genesis = "eb8c4d20b322be8d9fddbf9412016bdffe9a2901d7edb0e364e94266d0e095f7"
+        config["network_overrides"]["constants"]["simulator0"]["GENESIS_CHALLENGE"] = sim_genesis
+        # tell services to use simulator0
+        config["selected_network"] = "simulator0"
+        config["wallet"]["selected_network"] = "simulator0"
+        config["full_node"]["selected_network"] = "simulator0"
+        if not docker_mode:  # We want predictable ports for our docker image.
+            # set ports and networks, we don't want to cause a port conflict.
+            port_offset = randint(1, 20000)
+            config["daemon_port"] -= port_offset
+            config["network_overrides"]["config"]["simulator0"]["default_full_node_port"] = 38444 + port_offset
+            # wallet
+            config["wallet"]["port"] += port_offset
+            config["wallet"]["rpc_port"] += port_offset
+            # full node
+            config["full_node"]["port"] -= port_offset
+            config["full_node"]["rpc_port"] += port_offset
+            # connect wallet to full node
+            config["wallet"]["full_node_peer"]["port"] = config["full_node"]["port"]
+            config["full_node"]["wallet_peer"]["port"] = config["wallet"]["port"]
+            # ui
+            config["ui"]["daemon_port"] = config["daemon_port"]
+        else:
+            config["self_hostname"] = "0.0.0.0"  # Bind to all interfaces.
+            config["logging"]["log_stdout"] = True  # Log to console.
+    else:
+        config = load_config(chia_root, "config.yaml")
+    # simulator overrides
+    config["simulator"]["key_fingerprint"] = fingerprint
+    if farming_address is None:
+        prefix = config["network_overrides"]["config"]["simulator0"]["address_prefix"]
+        farming_address = encode_puzzle_hash(get_ph_from_fingerprint(fingerprint), prefix)
+    config["simulator"]["farming_address"] = farming_address
+    if plot_directory is not None:
+        config["simulator"]["plot_directory"] = plot_directory
+    # Temporary change to fix win / linux differences.
+    config["simulator"]["plot_directory"] = str(Path(config["simulator"]["plot_directory"]))
+    if "//" in config["simulator"]["plot_directory"] and os.name != "nt":
+        # if we're on linux, we need to convert to a linux path.
+        config["simulator"]["plot_directory"] = str(PureWindowsPath(config["simulator"]["plot_directory"]).as_posix())
+    config["simulator"]["auto_farm"] = auto_farm if auto_farm is not None else True
+    farming_ph = decode_puzzle_hash(farming_address)
+    # modify genesis block to give the user the reward
+    simulator_consts = config["network_overrides"]["constants"]["simulator0"]
+    simulator_consts["GENESIS_PRE_FARM_FARMER_PUZZLE_HASH"] = farming_ph.hex()
+    simulator_consts["GENESIS_PRE_FARM_POOL_PUZZLE_HASH"] = farming_ph.hex()
+    # save config and return the config
+    save_config(chia_root, "config.yaml", config)
+    return config
+
+
+def display_key_info(fingerprint: int, prefix: str) -> None:
+    """
+    Display key info for a given fingerprint, similar to the output of `chia keys show`.
+    """
+    print(f"Using fingerprint {fingerprint}")
+    private_key_and_seed = Keychain().get_private_key_by_fingerprint(fingerprint)
+    if private_key_and_seed is None:
+        print(f"Fingerprint {fingerprint} not found")
+        return
+    sk, seed = private_key_and_seed
+    print("\nFingerprint:", sk.get_g1().get_fingerprint())
+    print("Master public key (m):", sk.get_g1())
+    print("Farmer public key (m/12381/8444/0/0):", master_sk_to_farmer_sk(sk).get_g1())
+    print("Pool public key (m/12381/8444/1/0):", master_sk_to_pool_sk(sk).get_g1())
+    first_wallet_sk: PrivateKey = master_sk_to_wallet_sk_unhardened(sk, uint32(0))
+    wallet_address: str = encode_puzzle_hash(create_puzzlehash_for_pk(first_wallet_sk.get_g1()), prefix)
+    print(f"First wallet address: {wallet_address}")
+    assert seed is not None
+    print("Master private key (m):", bytes(sk).hex())
+    print("First wallet secret key (m/12381/8444/2/0):", master_sk_to_wallet_sk(sk, uint32(0)))
+    mnemonic = bytes_to_mnemonic(seed)
+    print("  Mnemonic seed (24 secret words):")
+    print(f"{mnemonic} \n")
+
+
+def generate_and_return_fingerprint(mnemonic: Optional[str] = None) -> int:
+    """
+    Generate and add new PrivateKey and return its fingerprint.
+    """
+    from chia.util.keychain import generate_mnemonic
+
+    if mnemonic is None:
+        print("Generating private key")
+        mnemonic = generate_mnemonic()
+    try:
+        sk = Keychain().add_private_key(mnemonic, None)
+        fingerprint: int = sk.get_g1().get_fingerprint()
+    except KeychainFingerprintExists as e:
+        fingerprint = e.fingerprint
+        print(f"Fingerprint: {fingerprint} for provided private key already exists.")
+        return fingerprint
+    print(f"Added private key with public key fingerprint {fingerprint}")
+    return fingerprint
+
+
+def select_fingerprint(
+    fingerprint: Optional[int] = None, mnemonic_string: Optional[str] = None, auto_generate_key: bool = False
+) -> Optional[int]:
+    """
+    Either select an existing fingerprint or create one and return it.
+    """
+    if mnemonic_string:
+        fingerprint = generate_and_return_fingerprint(mnemonic_string)
+    fingerprints: list[int] = [pk.get_fingerprint() for pk in Keychain().get_all_public_keys()]
+    if fingerprint is not None and fingerprint in fingerprints:
+        return fingerprint
+    elif fingerprint is not None and fingerprint not in fingerprints:
+        print(f"Invalid Fingerprint. Fingerprint {fingerprint} was not found.")
+        return None
+    if auto_generate_key and len(fingerprints) == 1:
+        return fingerprints[0]
+    if len(fingerprints) == 0:
+        if not auto_generate_key:
+            if (
+                input("No keys in keychain. Press 'q' to quit, or press any other key to generate a new key.").lower()
+                == "q"
+            ):
+                return None
+        # generate private key and add to wallet
+        fingerprint = generate_and_return_fingerprint()
+    else:
+        print("Fingerprints:")
+        print(
+            "If you already used one of these keys, select that fingerprint to skip the plotting process."
+            " Otherwise, select any key below."
+        )
+        for i, fp in enumerate(fingerprints):
+            row: str = f"{i + 1}) "
+            row += f"{fp}"
+            print(row)
+        val = None
+        prompt: str = f"Choose a simulator key [1-{len(fingerprints)}] ('q' to quit, or 'g' to generate a new key): "
+        while val is None:
+            val = input(prompt)
+            if val == "q":
+                return None
+            elif val == "g":
+                fingerprint = generate_and_return_fingerprint()
+                break
+            elif not val.isdigit():
+                val = None
+            else:
+                index = int(val) - 1
+                if index < 0 or index >= len(fingerprints):
+                    print("Invalid value")
+                    val = None
+                    continue
+                else:
+                    fingerprint = fingerprints[index]
+        assert fingerprint is not None
+    return fingerprint
+
+
+async def generate_plots(config: Dict[str, Any], root_path: Path, fingerprint: int, bitfield: bool) -> None:
+    """
+    Pre-Generate plots for the new simulator instance.
+    """
+
+    from chia.simulator.block_tools import BlockTools, test_constants
+    from chia.simulator.start_simulator import PLOT_SIZE, PLOTS
+
+    farming_puzzle_hash = decode_puzzle_hash(config["simulator"]["farming_address"])
+    os.environ["CHIA_ROOT"] = str(root_path)  # change env variable, to make it match what the daemon would set it to
+
+    # create block tools and use local keychain
+    bt = BlockTools(
+        test_constants,
+        root_path,
+        automated_testing=False,
+        plot_dir=config["simulator"].get("plot_directory", "plots"),
+        keychain=Keychain(),
+    )
+    await bt.setup_keys(fingerprint=fingerprint, reward_ph=farming_puzzle_hash)
+    existing_plots = await bt.setup_plots(
+        num_og_plots=PLOTS, num_pool_plots=0, num_non_keychain_plots=0, plot_size=PLOT_SIZE, bitfield=bitfield
+    )
+    print(f"{'New plots generated.' if existing_plots else 'Using Existing Plots'}\n")
+
+
+async def get_current_height(root_path: Path) -> int:
+    async with get_any_service_client(SimulatorFullNodeRpcClient, root_path=root_path, consume_errors=False) as (
+        node_client,
+        _,
+    ):
+        assert node_client is not None  # this cant be None, because we don't catch errors
+        num_blocks = len(await node_client.get_all_blocks())
+    return num_blocks
+
+
+async def async_config_wizard(
+    root_path: Path,
+    fingerprint: Optional[int],
+    farming_address: Optional[str],
+    plot_directory: Optional[str],
+    mnemonic_string: Optional[str],
+    auto_farm: Optional[bool],
+    docker_mode: bool,
+    bitfield: bool,
+) -> None:
+    # either return passed through fingerprint or get one
+    fingerprint = select_fingerprint(fingerprint, mnemonic_string, docker_mode)
+    if fingerprint is None:
+        # user cancelled wizard
+        return
+    # create chia directory & get config.
+    print("Creating chia directory & config...")
+    config = create_chia_directory(root_path, fingerprint, farming_address, plot_directory, auto_farm, docker_mode)
+    # Pre-generate plots by running block_tools init functions.
+    print("Please Wait, Generating plots...")
+    print("This may take up to a minute if you are on a slow machine")
+
+    await generate_plots(config, root_path, fingerprint, bitfield)
+    # final messages
+    final_farming_address = config["simulator"]["farming_address"]
+    print(f"\nFarming & Prefarm reward address: {final_farming_address}\n")
+    print("Configuration Wizard Complete.")
+    print("Starting Simulator now...\n\n")
+
+    sys.argv[0] = str(Path(sys.executable).parent / "chia")  # fix path for tests
+    await async_start(root_path, config, ("simulator",), False)
+
+    # now we make sure the simulator has a genesis block
+    print("Please wait, generating genesis block.")
+    while True:
+        try:
+            num_blocks: int = await get_current_height(root_path)
+        except ClientConnectorError:
+            await asyncio.sleep(0.25)
+        else:
+            if num_blocks == 0:
+                await farm_blocks(None, root_path, 1, True, final_farming_address)
+                print("Genesis block generated, exiting.")
+            else:
+                print("Genesis block already exists, exiting.")
+            break
+    print(f"\nMake sure your CHIA_ROOT Environment Variable is set to: {root_path}")
+
+
+def print_coin_record(
+    name: str,
+    address_prefix: str,
+    coin_record: CoinRecord,
+) -> None:
+    from datetime import datetime
+
+    coin_address = encode_puzzle_hash(coin_record.coin.puzzle_hash, address_prefix)
+    print(f"Coin 0x{coin_record.name.hex()}")
+    print(f"Wallet Address: {coin_address}")
+    print(f"Confirmed at block: {coin_record.confirmed_block_index}")
+    print(f"Spent: {f'at Block {coin_record.spent_block_index}' if coin_record.spent else 'No'}")
+    print(f"Coin Amount: {coin_record.coin.amount} {name}")
+    print(f"Parent Coin ID: 0x{coin_record.coin.parent_coin_info.hex()}")
+    print(f"Created at: {datetime.fromtimestamp(float(coin_record.timestamp)).strftime('%Y-%m-%d %H:%M:%S')}\n")
+
+
+async def print_coin_records(
+    config: Dict[str, Any],
+    node_client: SimulatorFullNodeRpcClient,
+    include_reward_coins: bool,
+    include_spent: bool = False,
+) -> None:
+    import sys
+
+    coin_records: List[CoinRecord] = await node_client.get_all_coins(include_spent)
+    coin_records = [coin_record for coin_record in coin_records if not coin_record.coinbase or include_reward_coins]
+    address_prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
+    name = "mojo"
+    paginate = False  # I might change this later.
+    if len(coin_records) != 0:
+        print("All Coins: ")
+        if paginate is True:
+            paginate = sys.stdout.isatty()
+        num_per_screen = 5 if paginate else len(coin_records)
+        # ripped from cmds/wallet_funcs.
+        for i in range(0, len(coin_records), num_per_screen):
+            for j in range(0, num_per_screen):
+                if i + j >= len(coin_records):
+                    break
+                print_coin_record(
+                    coin_record=coin_records[i + j],
+                    name=name,
+                    address_prefix=address_prefix,
+                )
+            if i + num_per_screen <= len(coin_records) and paginate:
+                print("Press q to quit, or c to continue")
+                while True:
+                    entered_key = sys.stdin.read(1)
+                    if entered_key == "q":
+                        return None
+                    elif entered_key == "c":
+                        break
+
+
+async def print_wallets(config: Dict[str, Any], node_client: SimulatorFullNodeRpcClient) -> None:
+    ph_and_amount = await node_client.get_all_puzzle_hashes()
+    address_prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
+    name = "mojo"
+    for puzzle_hash, (amount, num_tx) in ph_and_amount.items():
+        address = encode_puzzle_hash(puzzle_hash, address_prefix)
+        print(f"Address: {address} has a balance of: {amount} {name}, with a total of: {num_tx} transactions.\n")
+
+
+async def print_status(
+    rpc_port: Optional[int],
+    root_path: Path,
+    fingerprint: Optional[int],
+    show_key: bool,
+    show_coins: bool,
+    include_reward_coins: bool,
+    show_addresses: bool,
+) -> None:
+    """
+    This command allows users to easily get the status of the simulator
+    and information about the state of and the coins in the simulated blockchain.
+    """
+    from chia.cmds.show_funcs import print_blockchain_state
+    from chia.cmds.units import units
+
+    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (node_client, config):
+        if node_client is not None:
+            # Display keychain info
+            if show_key:
+                if fingerprint is None:
+                    fingerprint = config["simulator"]["key_fingerprint"]
+                if fingerprint is not None:
+                    display_key_info(
+                        fingerprint, config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
+                    )
+                else:
+                    print(
+                        "No fingerprint in config, either rerun 'cdv sim create' "
+                        "or use --fingerprint to specify one, skipping key information."
+                    )
+            # chain status ( basically chia show -s)
+            await print_blockchain_state(node_client, config)
+            print("")
+            # farming information
+            target_ph: bytes32 = await node_client.get_farming_ph()
+            farming_coin_records = await node_client.get_coin_records_by_puzzle_hash(target_ph, False)
+            prefix = config["network_overrides"]["config"][config["selected_network"]]["address_prefix"]
+            print(
+                f"Current Farming address: {encode_puzzle_hash(target_ph, prefix)}, "
+                f"with a balance of: "
+                f"{sum(coin_records.coin.amount for coin_records in farming_coin_records) / units['chia']} TXCH."
+            )
+            if show_addresses:
+                print("All Addresses: ")
+                await print_wallets(config, node_client)
+            if show_coins:
+                await print_coin_records(config, node_client, include_reward_coins)
+
+
+async def revert_block_height(
+    rpc_port: Optional[int],
+    root_path: Path,
+    num_blocks: int,
+    num_new_blocks: int,
+    reset_chain_to_genesis: bool,
+    use_revert_blocks: bool,
+) -> None:
+    """
+    This function allows users to easily revert the chain to a previous state or perform a reorg.
+    """
+    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (node_client, _):
+        if node_client is not None:
+            if use_revert_blocks:
+                if num_new_blocks != 1:
+                    print(f"Ignoring num_new_blocks: {num_new_blocks}, because we are not performing a reorg.")
+                # in this case num_blocks is the number of blocks to delete
+                new_height: int = await node_client.revert_blocks(num_blocks, reset_chain_to_genesis)
+                print(
+                    f"All transactions in Block: {new_height + num_blocks} and above were successfully deleted, "
+                    "you should now delete & restart all wallets."
+                )
+            else:
+                # However, in this case num_blocks is the fork height.
+                new_height = await node_client.reorg_blocks(num_blocks, num_new_blocks, use_revert_blocks)
+                old_height = new_height - num_new_blocks
+                print(f"All transactions in Block: {old_height - num_blocks} and above were successfully reverted.")
+            print(f"Block Height is now: {new_height}")
+
+
+async def farm_blocks(
+    rpc_port: Optional[int],
+    root_path: Path,
+    num_blocks: int,
+    transaction_blocks: bool,
+    target_address: str,
+) -> None:
+    """
+    This function is used to generate new blocks.
+    """
+    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (node_client, config):
+        if node_client is not None:
+            if target_address == "":
+                target_address = config["simulator"]["farming_address"]
+            if target_address is None:
+                print(
+                    "No target address in config, falling back to the temporary address currently in use. "
+                    "You can use 'cdv sim create' or use --target-address to specify a different address."
+                )
+                target_ph: bytes32 = await node_client.get_farming_ph()
+            else:
+                target_ph = decode_puzzle_hash(target_address)
+            await node_client.farm_block(target_ph, num_blocks, transaction_blocks)
+            print(f"Farmed {num_blocks}{' Transaction' if transaction_blocks else ''} blocks")
+            block_height = (await node_client.get_blockchain_state())["peak"].height
+            print(f"Block Height is now: {block_height}")
+
+
+async def set_auto_farm(rpc_port: Optional[int], root_path: Path, set_autofarm: bool) -> None:
+    """
+    This function can be used to enable or disable Auto Farming.
+    """
+    async with get_any_service_client(SimulatorFullNodeRpcClient, rpc_port, root_path) as (node_client, _):
+        if node_client is not None:
+            current = await node_client.get_auto_farming()
+            if current == set_autofarm:
+                print(f"Auto farming is already {'on' if set_autofarm else 'off'}")
+                return
+            result = await node_client.set_auto_farming(set_autofarm)
+            print(f"Auto farming is now {'on' if result else 'off'}")
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/start.py` & `chia-blockchain-2.0.0b1/chia/cmds/start.py`

 * *Files 27% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 import click
 
 from chia.util.config import load_config
 from chia.util.service_groups import all_groups
 
 
-@click.command("start", short_help="Start service groups")
+@click.command("start", help="Start service groups")
 @click.option("-r", "--restart", is_flag=True, type=bool, help="Restart running services")
 @click.argument("group", type=click.Choice(list(all_groups())), nargs=-1, required=True)
 @click.pass_context
 def start_cmd(ctx: click.Context, restart: bool, group: tuple[str, ...]) -> None:
     import asyncio
 
     from chia.cmds.beta_funcs import warn_if_beta_enabled
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/start_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/start_funcs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/stop.py` & `chia-blockchain-2.0.0b1/chia/cmds/stop.py`

 * *Files 4% similar despite different names*

```diff
@@ -43,15 +43,15 @@
             print("Stop failed")
             return_val = 1
 
     await daemon.close()
     return return_val
 
 
-@click.command("stop", short_help="Stop services")
+@click.command("stop", help="Stop services")
 @click.option("-d", "--daemon", is_flag=True, type=bool, help="Stop daemon")
 @click.argument("group", type=click.Choice(list(all_groups())), nargs=-1, required=True)
 @click.pass_context
 def stop_cmd(ctx: click.Context, daemon: bool, group: tuple[str, ...]) -> None:
     from chia.cmds.beta_funcs import warn_if_beta_enabled
 
     root_path = ctx.obj["root_path"]
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/wallet.py` & `chia-blockchain-2.0.0b1/chia/cmds/wallet.py`

 * *Files 14% similar despite different names*

```diff
@@ -10,21 +10,21 @@
 from chia.cmds.coins import coins_cmd
 from chia.cmds.plotnft import validate_fee
 from chia.wallet.transaction_sorting import SortKey
 from chia.wallet.util.address_type import AddressType
 from chia.wallet.util.wallet_types import WalletType
 
 
-@click.group("wallet", short_help="Manage your wallet")
+@click.group("wallet", help="Manage your wallet")
 @click.pass_context
 def wallet_cmd(ctx: click.Context) -> None:
     pass
 
 
-@wallet_cmd.command("get_transaction", short_help="Get a transaction")
+@wallet_cmd.command("get_transaction", help="Get a transaction")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -37,15 +37,15 @@
     import asyncio
 
     from .wallet_funcs import get_transaction
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_transaction))
 
 
-@wallet_cmd.command("get_transactions", short_help="Get all transactions")
+@wallet_cmd.command("get_transactions", help="Get all transactions")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -128,15 +128,15 @@
     #
     # Exception ignored in: <_io.TextIOWrapper name='<stdout>' mode='w' encoding='utf-8'>
     # BrokenPipeError: [Errno 32] Broken pipe
     sys.stdout.flush()
     sys.stdout.close()
 
 
-@wallet_cmd.command("send", short_help="Send chia to another wallet")
+@wallet_cmd.command("send", help="Send chia to another wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -176,15 +176,14 @@
 @click.option(
     "--exclude-coin",
     "coins_to_exclude",
     multiple=True,
     help="Exclude this coin from being spent.",
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the change.",
     is_flag=True,
     default=False,
 )
 def send_cmd(
     wallet_rpc_port: Optional[int],
@@ -215,15 +214,15 @@
     import asyncio
 
     from .wallet_funcs import send
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, send))
 
 
-@wallet_cmd.command("show", short_help="Show wallet information")
+@wallet_cmd.command("show", help="Show wallet information")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -242,15 +241,15 @@
 
     args: Dict[str, Any] = {}
     if wallet_type is not None:
         args["type"] = WalletType[wallet_type.upper()]
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, args, print_balances))
 
 
-@wallet_cmd.command("get_address", short_help="Get a wallet receive address")
+@wallet_cmd.command("get_address", help="Get a wallet receive address")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -271,17 +270,15 @@
     import asyncio
 
     from .wallet_funcs import get_address
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_address))
 
 
-@wallet_cmd.command(
-    "delete_unconfirmed_transactions", short_help="Deletes all unconfirmed transactions for this wallet ID"
-)
+@wallet_cmd.command("delete_unconfirmed_transactions", help="Deletes all unconfirmed transactions for this wallet ID")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -292,15 +289,15 @@
     import asyncio
 
     from .wallet_funcs import delete_unconfirmed_transactions
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, delete_unconfirmed_transactions))
 
 
-@wallet_cmd.command("get_derivation_index", short_help="Get the last puzzle hash derivation path index")
+@wallet_cmd.command("get_derivation_index", help="Get the last puzzle hash derivation path index")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -310,15 +307,15 @@
     import asyncio
 
     from .wallet_funcs import get_derivation_index
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_derivation_index))
 
 
-@wallet_cmd.command("sign_message", short_help="Sign a message by a derivation address")
+@wallet_cmd.command("sign_message", help="Sign a message by a derivation address")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -331,15 +328,15 @@
 
     from .wallet_funcs import sign_message
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, sign_message))
 
 
 @wallet_cmd.command(
-    "update_derivation_index", short_help="Generate additional derived puzzle hashes starting at the provided index"
+    "update_derivation_index", help="Generate additional derived puzzle hashes starting at the provided index"
 )
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
@@ -353,15 +350,15 @@
     import asyncio
 
     from .wallet_funcs import update_derivation_index
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, update_derivation_index))
 
 
-@wallet_cmd.command("add_token", short_help="Add/Rename a CAT to the wallet by its asset ID")
+@wallet_cmd.command("add_token", help="Add/Rename a CAT to the wallet by its asset ID")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -388,15 +385,15 @@
     import asyncio
 
     from .wallet_funcs import add_token
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, add_token))
 
 
-@wallet_cmd.command("make_offer", short_help="Create an offer of XCH/CATs/NFTs for XCH/CATs/NFTs")
+@wallet_cmd.command("make_offer", help="Create an offer of XCH/CATs/NFTs for XCH/CATs/NFTs")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -416,15 +413,14 @@
     multiple=True,
 )
 @click.option("-p", "--filepath", help="The path to write the generated offer file to", required=True)
 @click.option(
     "-m", "--fee", help="A fee to add to the offer when it gets taken, in XCH", default="0", show_default=True
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the offer.",
     is_flag=True,
     default=False,
 )
 def make_offer_cmd(
     wallet_rpc_port: Optional[int],
@@ -446,15 +442,15 @@
 
     from .wallet_funcs import make_offer
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, make_offer))
 
 
 @wallet_cmd.command(
-    "get_offers", short_help="Get the status of existing offers. Displays only active/pending offers by default."
+    "get_offers", help="Get the status of existing offers. Displays only active/pending offers by default."
 )
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
@@ -492,30 +488,29 @@
     import asyncio
 
     from .wallet_funcs import get_offers
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_offers))
 
 
-@wallet_cmd.command("take_offer", short_help="Examine or take an offer")
+@wallet_cmd.command("take_offer", help="Examine or take an offer")
 @click.argument("path_or_hex", type=str, nargs=1, required=True)
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
 @click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
 @click.option("-e", "--examine-only", help="Print the summary of the offer file but do not take it", is_flag=True)
 @click.option(
     "-m", "--fee", help="The fee to use when pushing the completed offer, in XCH", default="0", show_default=True
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the offer.",
     is_flag=True,
     default=False,
 )
 def take_offer_cmd(
     path_or_hex: str,
@@ -534,15 +529,15 @@
     import asyncio
 
     from .wallet_funcs import take_offer
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, take_offer))
 
 
-@wallet_cmd.command("cancel_offer", short_help="Cancel an existing offer")
+@wallet_cmd.command("cancel_offer", help="Cancel an existing offer")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -572,20 +567,20 @@
     import asyncio
 
     from chia.cmds.check_wallet_db import scan
 
     asyncio.run(scan(ctx.obj["root_path"], db_path, verbose=verbose))
 
 
-@wallet_cmd.group("did", short_help="DID related actions")
+@wallet_cmd.group("did", help="DID related actions")
 def did_cmd():
     pass
 
 
-@did_cmd.command("create", short_help="Create DID wallet")
+@did_cmd.command("create", help="Create DID wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -615,15 +610,15 @@
 
     from .wallet_funcs import create_did_wallet
 
     extra_params = {"amount": amount, "fee": fee, "name": name}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, create_did_wallet))
 
 
-@did_cmd.command("sign_message", short_help="Sign a message by a DID")
+@did_cmd.command("sign_message", help="Sign a message by a DID")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -635,15 +630,15 @@
     import asyncio
 
     from .wallet_funcs import sign_message
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, sign_message))
 
 
-@did_cmd.command("set_name", short_help="Set DID wallet name")
+@did_cmd.command("set_name", help="Set DID wallet name")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -655,15 +650,15 @@
 
     from .wallet_funcs import did_set_wallet_name
 
     extra_params = {"wallet_id": id, "name": name}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, did_set_wallet_name))
 
 
-@did_cmd.command("get_did", short_help="Get DID from wallet")
+@did_cmd.command("get_did", help="Get DID from wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -674,20 +669,226 @@
 
     from .wallet_funcs import get_did
 
     extra_params = {"did_wallet_id": id}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_did))
 
 
-@wallet_cmd.group("nft", short_help="NFT related actions")
+@did_cmd.command("get_details", help="Get more details of any DID")
+@click.option(
+    "-wp",
+    "--wallet-rpc-port",
+    help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
+    type=int,
+    default=None,
+)
+@click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
+@click.option("-id", "--coin_id", help="Id of the DID or any coin ID of the DID", type=str, required=True)
+@click.option("-l", "--latest", help="Return latest DID information", is_flag=True, default=True)
+def did_get_details_cmd(wallet_rpc_port: Optional[int], fingerprint: int, coin_id: str, latest: bool) -> None:
+    import asyncio
+
+    from .wallet_funcs import get_did_info
+
+    extra_params = {"coin_id": coin_id, "latest": latest}
+    asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_did_info))
+
+
+@did_cmd.command("update_metadata", help="Update the metadata of a DID")
+@click.option(
+    "-wp",
+    "--wallet-rpc-port",
+    help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
+    type=int,
+    default=None,
+)
+@click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
+@click.option("-i", "--id", help="Id of the DID wallet to use", type=int, required=True)
+@click.option("-d", "--metadata", help="The new whole metadata in json format", type=str, required=True)
+@click.option(
+    "--reuse",
+    help="Reuse existing address for the change.",
+    is_flag=True,
+    default=False,
+)
+def did_update_metadata_cmd(
+    wallet_rpc_port: Optional[int], fingerprint: int, id: int, metadata: str, reuse: bool
+) -> None:
+    import asyncio
+
+    from .wallet_funcs import update_did_metadata
+
+    extra_params = {"did_wallet_id": id, "metadata": metadata, "reuse_puzhash": reuse}
+    asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, update_did_metadata))
+
+
+@did_cmd.command("find_lost", help="Find the did you should own and recovery the DID wallet")
+@click.option(
+    "-wp",
+    "--wallet-rpc-port",
+    help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
+    type=int,
+    default=None,
+)
+@click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
+@click.option("-id", "--coin_id", help="Id of the DID or any coin ID of the DID", type=str, required=True)
+@click.option("-m", "--metadata", help="The new whole metadata in json format", type=str, required=False)
+@click.option(
+    "-r",
+    "--recovery_list_hash",
+    help="Override the recovery list hash of the DID. Only set this if your last DID spend updated the recovery list",
+    type=str,
+    required=False,
+)
+@click.option(
+    "-n",
+    "--num_verification",
+    help="Override the required verification number of the DID."
+    " Only set this if your last DID spend updated the required verification number",
+    type=int,
+    required=False,
+)
+def did_find_lost_cmd(
+    wallet_rpc_port: Optional[int],
+    fingerprint: int,
+    coin_id: str,
+    metadata: Optional[str],
+    recovery_list_hash: Optional[str],
+    num_verification: Optional[int],
+) -> None:
+    import asyncio
+
+    from .wallet_funcs import find_lost_did
+
+    extra_params = {
+        "coin_id": coin_id,
+        "metadata": metadata,
+        "recovery_list_hash": recovery_list_hash,
+        "num_verification": num_verification,
+    }
+    asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, find_lost_did))
+
+
+@did_cmd.command("message_spend", help="Generate a DID spend bundle for announcements")
+@click.option(
+    "-wp",
+    "--wallet-rpc-port",
+    help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
+    type=int,
+    default=None,
+)
+@click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
+@click.option("-i", "--id", help="Id of the DID wallet to use", type=int, required=True)
+@click.option(
+    "-pa",
+    "--puzzle_announcements",
+    help="The list of puzzle announcement hex strings, split by comma (,)",
+    type=str,
+    required=False,
+)
+@click.option(
+    "-ca",
+    "--coin_announcements",
+    help="The list of coin announcement hex strings, split by comma (,)",
+    type=str,
+    required=False,
+)
+def did_message_spend_cmd(
+    wallet_rpc_port: Optional[int],
+    fingerprint: int,
+    id: int,
+    puzzle_announcements: Optional[str],
+    coin_announcements: Optional[str],
+) -> None:
+    import asyncio
+
+    from .wallet_funcs import did_message_spend
+
+    puzzle_list: List[str] = []
+    coin_list: List[str] = []
+    if puzzle_announcements is not None:
+        try:
+            puzzle_list = puzzle_announcements.split(",")
+            # validate puzzle announcements is list of hex strings
+            for announcement in puzzle_list:
+                bytes.fromhex(announcement)
+        except ValueError:
+            print("Invalid puzzle announcement format, should be a list of hex strings.")
+            return
+    if coin_announcements is not None:
+        try:
+            coin_list = coin_announcements.split(",")
+            # validate that coin announcements is a list of hex strings
+            for announcement in coin_list:
+                bytes.fromhex(announcement)
+        except ValueError:
+            print("Invalid coin announcement format, should be a list of hex strings.")
+            return
+    extra_params = {"did_wallet_id": id, "puzzle_announcements": puzzle_list, "coin_announcements": coin_list}
+    asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, did_message_spend))
+
+
+@did_cmd.command("transfer", help="Transfer a DID")
+@click.option(
+    "-wp",
+    "--wallet-rpc-port",
+    help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
+    type=int,
+    default=None,
+)
+@click.option("-f", "--fingerprint", help="Set the fingerprint to specify which key to use", type=int)
+@click.option("-i", "--id", help="Id of the DID wallet to use", type=int, required=True)
+@click.option("-ta", "--target-address", help="Target recipient wallet address", type=str, required=True)
+@click.option(
+    "-rr", "--reset_recovery", help="If you want to reset the recovery DID settings.", is_flag=True, default=False
+)
+@click.option(
+    "-m",
+    "--fee",
+    help="Set the fees per transaction, in XCH.",
+    type=str,
+    default="0",
+    show_default=True,
+    callback=validate_fee,
+)
+@click.option(
+    "--reuse",
+    help="Reuse existing address for the change.",
+    is_flag=True,
+    default=False,
+)
+def did_transfer_did(
+    wallet_rpc_port: Optional[int],
+    fingerprint: int,
+    id: int,
+    target_address: str,
+    reset_recovery: bool,
+    fee: str,
+    reuse: bool,
+) -> None:
+    import asyncio
+
+    from .wallet_funcs import transfer_did
+
+    extra_params = {
+        "did_wallet_id": id,
+        "with_recovery": reset_recovery is False,
+        "target_address": target_address,
+        "fee": fee,
+        "reuse_puzhash": True if reuse else None,
+    }
+    asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, transfer_did))
+
+
+@wallet_cmd.group("nft", help="NFT related actions")
 def nft_cmd():
     pass
 
 
-@nft_cmd.command("create", short_help="Create an NFT wallet")
+@nft_cmd.command("create", help="Create an NFT wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -701,15 +902,15 @@
 
     from .wallet_funcs import create_nft_wallet
 
     extra_params: Dict[str, Any] = {"did_id": did_id, "name": name}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, create_nft_wallet))
 
 
-@nft_cmd.command("sign_message", short_help="Sign a message by a NFT")
+@nft_cmd.command("sign_message", help="Sign a message by a NFT")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -721,15 +922,15 @@
     import asyncio
 
     from .wallet_funcs import sign_message
 
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, sign_message))
 
 
-@nft_cmd.command("mint", short_help="Mint an NFT")
+@nft_cmd.command("mint", help="Mint an NFT")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -760,15 +961,14 @@
     "--royalty-percentage-fraction",
     help="NFT royalty percentage fraction in basis points. Example: 175 would represent 1.75%",
     type=int,
     default=0,
     show_default=True,
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the change.",
     is_flag=True,
     default=False,
 )
 def nft_mint_cmd(
     wallet_rpc_port: Optional[int],
@@ -819,15 +1019,15 @@
         "fee": fee,
         "royalty_percentage": royalty_percentage_fraction,
         "reuse_puzhash": True if reuse else None,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, mint_nft))
 
 
-@nft_cmd.command("add_uri", short_help="Add an URI to an NFT")
+@nft_cmd.command("add_uri", help="Add an URI to an NFT")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -843,15 +1043,14 @@
     help="Set the fees per transaction, in XCH.",
     type=str,
     default="0",
     show_default=True,
     callback=validate_fee,
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the change.",
     is_flag=True,
     default=False,
 )
 def nft_add_uri_cmd(
     wallet_rpc_port: Optional[int],
@@ -876,15 +1075,15 @@
         "license_uri": license_uri,
         "fee": fee,
         "reuse_puzhash": True if reuse else None,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, add_uri_to_nft))
 
 
-@nft_cmd.command("transfer", short_help="Transfer an NFT")
+@nft_cmd.command("transfer", help="Transfer an NFT")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -898,15 +1097,14 @@
     help="Set the fees per transaction, in XCH.",
     type=str,
     default="0",
     show_default=True,
     callback=validate_fee,
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the change.",
     is_flag=True,
     default=False,
 )
 def nft_transfer_cmd(
     wallet_rpc_port: Optional[int],
@@ -927,15 +1125,15 @@
         "target_address": target_address,
         "fee": fee,
         "reuse_puzhash": True if reuse else None,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, transfer_nft))
 
 
-@nft_cmd.command("list", short_help="List the current NFTs")
+@nft_cmd.command("list", help="List the current NFTs")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -946,15 +1144,15 @@
 
     from .wallet_funcs import list_nfts
 
     extra_params = {"wallet_id": id}
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, list_nfts))
 
 
-@nft_cmd.command("set_did", short_help="Set a DID on an NFT")
+@nft_cmd.command("set_did", help="Set a DID on an NFT")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -968,15 +1166,14 @@
     help="Set the fees per transaction, in XCH.",
     type=str,
     default="0",
     show_default=True,
     callback=validate_fee,
 )
 @click.option(
-    "-r",
     "--reuse",
     help="Reuse existing address for the change.",
     is_flag=True,
     default=False,
 )
 def nft_set_did_cmd(
     wallet_rpc_port: Optional[int],
@@ -997,15 +1194,15 @@
         "nft_coin_id": nft_coin_id,
         "fee": fee,
         "reuse_puzhash": True if reuse else None,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, set_nft_did))
 
 
-@nft_cmd.command("get_info", short_help="Get NFT information")
+@nft_cmd.command("get_info", help="Get NFT information")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -1026,20 +1223,20 @@
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_nft_info))
 
 
 # Keep at bottom.
 wallet_cmd.add_command(coins_cmd)
 
 
-@wallet_cmd.group("notifications", short_help="Send/Manage notifications")
+@wallet_cmd.group("notifications", help="Send/Manage notifications")
 def notification_cmd():
     pass
 
 
-@notification_cmd.command("send", short_help="Send a notification to the owner of an address")
+@notification_cmd.command("send", help="Send a notification to the owner of an address")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -1075,15 +1272,15 @@
         "amount": amount,
         "message": message,
         "fee": fee,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, send_notification))
 
 
-@notification_cmd.command("get", short_help="Get notification(s) that are in your wallet")
+@notification_cmd.command("get", help="Get notification(s) that are in your wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
@@ -1108,15 +1305,15 @@
         "ids": id,
         "start": start,
         "end": end,
     }
     asyncio.run(execute_with_wallet(wallet_rpc_port, fingerprint, extra_params, get_notifications))
 
 
-@notification_cmd.command("delete", short_help="Delete notification(s) that are in your wallet")
+@notification_cmd.command("delete", help="Delete notification(s) that are in your wallet")
 @click.option(
     "-wp",
     "--wallet-rpc-port",
     help="Set the port where the Wallet is hosting the RPC interface. See the rpc_port under wallet in config.yaml",
     type=int,
     default=None,
 )
```

### Comparing `chia-blockchain-1.8.1rc2/chia/cmds/wallet_funcs.py` & `chia-blockchain-2.0.0b1/chia/cmds/wallet_funcs.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from __future__ import annotations
 
 import asyncio
+import json
 import os
 import pathlib
 import sys
 import time
 from datetime import datetime
 from decimal import Decimal
 from typing import Any, Awaitable, Callable, Dict, List, Optional, Tuple, Union
@@ -826,14 +827,88 @@
         coin_id = response["coin_id"]
         print(f"{'DID:'.ljust(23)} {my_did}")
         print(f"{'Coin ID:'.ljust(23)} {coin_id}")
     except Exception as e:
         print(f"Failed to get DID: {e}")
 
 
+async def get_did_info(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
+    coin_id: str = args["coin_id"]
+    latest: bool = args["latest"]
+    did_padding_length = 23
+    try:
+        response = await wallet_client.get_did_info(coin_id, latest)
+        print(f"{'DID:'.ljust(did_padding_length)} {response['did_id']}")
+        print(f"{'Coin ID:'.ljust(did_padding_length)} {response['latest_coin']}")
+        print(f"{'Inner P2 Address:'.ljust(did_padding_length)} {response['p2_address']}")
+        print(f"{'Public Key:'.ljust(did_padding_length)} {response['public_key']}")
+        print(f"{'Launcher ID:'.ljust(did_padding_length)} {response['launcher_id']}")
+        print(f"{'DID Metadata:'.ljust(did_padding_length)} {response['metadata']}")
+        print(f"{'Recovery List Hash:'.ljust(did_padding_length)} {response['recovery_list_hash']}")
+        print(f"{'Recovery Required Verifications:'.ljust(did_padding_length)} {response['num_verification']}")
+        print(f"{'Last Spend Puzzle:'.ljust(did_padding_length)} {response['full_puzzle']}")
+        print(f"{'Last Spend Solution:'.ljust(did_padding_length)} {response['solution']}")
+        print(f"{'Last Spend Hints:'.ljust(did_padding_length)} {response['hints']}")
+
+    except Exception as e:
+        print(f"Failed to get DID details: {e}")
+
+
+async def update_did_metadata(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
+    try:
+        response = await wallet_client.update_did_metadata(
+            args["did_wallet_id"], json.loads(args["metadata"]), args["reuse_puzhash"]
+        )
+        print(f"Successfully updated DID wallet ID: {response['wallet_id']}, Spend Bundle: {response['spend_bundle']}")
+    except Exception as e:
+        print(f"Failed to update DID metadata: {e}")
+
+
+async def did_message_spend(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
+    try:
+        response = await wallet_client.did_message_spend(
+            args["did_wallet_id"], args["puzzle_announcements"], args["coin_announcements"]
+        )
+        print(f"Message Spend Bundle: {response['spend_bundle']}")
+    except Exception as e:
+        print(f"Failed to update DID metadata: {e}")
+
+
+async def transfer_did(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
+    try:
+        response = await wallet_client.did_transfer_did(
+            args["did_wallet_id"],
+            args["target_address"],
+            args["fee"],
+            args["with_recovery"],
+            args["reuse_puzhash"],
+        )
+        print(f"Successfully transferred DID to {args['target_address']}")
+        print(f"Transaction ID: {response['transaction_id']}")
+        print(f"Transaction: {response['transaction']}")
+    except Exception as e:
+        print(f"Failed to transfer DID: {e}")
+
+
+async def find_lost_did(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
+    try:
+        response = await wallet_client.find_lost_did(
+            args["coin_id"],
+            args["recovery_list_hash"],
+            args["metadata"],
+            args["num_verification"],
+        )
+        if response["success"]:
+            print(f"Successfully found lost DID {args['coin_id']}, latest coin ID: {response['latest_coin_id']}")
+        else:
+            print(f"Cannot find lost DID {args['coin_id']}: {response['error']}")
+    except Exception as e:
+        print(f"Failed to find lost DID: {e}")
+
+
 async def create_nft_wallet(args: Dict, wallet_client: WalletRpcClient, fingerprint: int) -> None:
     did_id = args["did_id"]
     name = args["name"]
     try:
         response = await wallet_client.create_new_nft_wallet(did_id, name)
         wallet_id = response["wallet_id"]
         print(f"Successfully created an NFT wallet with id {wallet_id} on key {fingerprint}")
```

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_body_validation.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_body_validation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_creation.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_creation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_header_validation.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_header_validation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_record.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_rewards.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_rewards.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/block_root_validation.py` & `chia-blockchain-2.0.0b1/chia/consensus/block_root_validation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/blockchain.py` & `chia-blockchain-2.0.0b1/chia/consensus/blockchain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/blockchain_interface.py` & `chia-blockchain-2.0.0b1/chia/consensus/blockchain_interface.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/coinbase.py` & `chia-blockchain-2.0.0b1/chia/consensus/coinbase.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/constants.py` & `chia-blockchain-2.0.0b1/chia/consensus/constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/cost_calculator.py` & `chia-blockchain-2.0.0b1/chia/consensus/cost_calculator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/default_constants.py` & `chia-blockchain-2.0.0b1/chia/consensus/default_constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/deficit.py` & `chia-blockchain-2.0.0b1/chia/consensus/deficit.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/difficulty_adjustment.py` & `chia-blockchain-2.0.0b1/chia/consensus/difficulty_adjustment.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/find_fork_point.py` & `chia-blockchain-2.0.0b1/chia/consensus/find_fork_point.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/full_block_to_block_record.py` & `chia-blockchain-2.0.0b1/chia/consensus/full_block_to_block_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/get_block_challenge.py` & `chia-blockchain-2.0.0b1/chia/consensus/get_block_challenge.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/make_sub_epoch_summary.py` & `chia-blockchain-2.0.0b1/chia/consensus/make_sub_epoch_summary.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/multiprocess_validation.py` & `chia-blockchain-2.0.0b1/chia/consensus/multiprocess_validation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/pos_quality.py` & `chia-blockchain-2.0.0b1/chia/consensus/pos_quality.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/pot_iterations.py` & `chia-blockchain-2.0.0b1/chia/consensus/pot_iterations.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/consensus/vdf_info_computation.py` & `chia-blockchain-2.0.0b1/chia/consensus/vdf_info_computation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/daemon/client.py` & `chia-blockchain-2.0.0b1/chia/daemon/client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/daemon/keychain_proxy.py` & `chia-blockchain-2.0.0b1/chia/daemon/keychain_proxy.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/daemon/keychain_server.py` & `chia-blockchain-2.0.0b1/chia/daemon/keychain_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/daemon/server.py` & `chia-blockchain-2.0.0b1/chia/daemon/server.py`

 * *Files 1% similar despite different names*

```diff
@@ -21,16 +21,15 @@
 from chia import __version__
 from chia.cmds.init_funcs import check_keys, chia_full_version_str, chia_init
 from chia.cmds.passphrase_funcs import default_passphrase, using_default_passphrase
 from chia.daemon.keychain_server import KeychainServer, keychain_commands
 from chia.daemon.windows_signal import kill
 from chia.plotters.plotters import get_available_plotters
 from chia.plotting.util import add_plot_directory
-from chia.server.server import ssl_context_for_root, ssl_context_for_server
-from chia.ssl.create_ssl import get_mozilla_ca_crt
+from chia.server.server import ssl_context_for_server
 from chia.util.beta_metrics import BetaMetricsLogger
 from chia.util.chia_logging import initialize_service_logging
 from chia.util.config import load_config
 from chia.util.errors import KeychainCurrentPassphraseIsInvalid
 from chia.util.json_util import dict_to_json_str
 from chia.util.keychain import Keychain, passphrase_requirements, supports_os_passphrase_storage
 from chia.util.lock import Lockfile, LockfileError
@@ -38,41 +37,26 @@
 from chia.util.service_groups import validate_service
 from chia.util.setproctitle import setproctitle
 from chia.util.ws_message import WsRpcMessage, create_payload, format_response
 
 io_pool_exc = ThreadPoolExecutor()
 
 try:
-    from aiohttp import ClientSession, WSMsgType, web
+    from aiohttp import WSMsgType, web
     from aiohttp.web_ws import WebSocketResponse
 except ModuleNotFoundError:
     print("Error: Make sure to run . ./activate from the project folder before starting Chia.")
     quit()
 
 
 log = logging.getLogger(__name__)
 
 service_plotter = "chia_plotter"
 
 
-async def fetch(url: str):
-    async with ClientSession() as session:
-        try:
-            mozilla_root = get_mozilla_ca_crt()
-            ssl_context = ssl_context_for_root(mozilla_root, log=log)
-            response = await session.get(url, ssl=ssl_context)
-            if not response.ok:
-                log.warning("Response not OK.")
-                return None
-            return await response.text()
-        except Exception as e:
-            log.error(f"Exception while fetching {url}, exception: {e}")
-            return None
-
-
 class PlotState(str, Enum):
     SUBMITTED = "SUBMITTED"
     RUNNING = "RUNNING"
     REMOVING = "REMOVING"
     FINISHED = "FINISHED"
```

### Comparing `chia-blockchain-1.8.1rc2/chia/daemon/windows_signal.py` & `chia-blockchain-2.0.0b1/chia/daemon/windows_signal.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_api.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_errors.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer_errors.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_server.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_util.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer_util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_layer_wallet.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_layer_wallet.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from __future__ import annotations
 
 import dataclasses
 import logging
 import time
 from operator import attrgetter
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, cast
 
 from blspy import G1Element, G2Element
 from clvm.EvalError import EvalError
 from typing_extensions import final
 
 from chia.consensus.block_record import BlockRecord
 from chia.data_layer.data_layer_errors import OfferIntegrityError
@@ -38,24 +38,25 @@
     launch_solution_to_singleton_info,
     launcher_to_struct,
     match_dl_singleton,
 )
 from chia.wallet.derivation_record import DerivationRecord
 from chia.wallet.lineage_proof import LineageProof
 from chia.wallet.outer_puzzles import AssetType
+from chia.wallet.payment import Payment
 from chia.wallet.puzzle_drivers import PuzzleInfo, Solver
 from chia.wallet.puzzles.singleton_top_layer_v1_1 import SINGLETON_LAUNCHER_HASH
 from chia.wallet.sign_coin_spends import sign_coin_spends
 from chia.wallet.trading.offer import NotarizedPayment, Offer
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.merkle_utils import _simplify_merkle_proof
 from chia.wallet.util.transaction_type import TransactionType
 from chia.wallet.util.wallet_sync_utils import fetch_coin_spend, fetch_coin_spend_for_coin_state
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash, WalletType
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 
 if TYPE_CHECKING:
     from chia.wallet.wallet_state_manager import WalletStateManager
 
@@ -100,14 +101,19 @@
             [bytes(url, "utf8") for url in json_dict["urls"]],
             json_dict["ours"],
         )
 
 
 @final
 class DataLayerWallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("DataLayerWallet", None)
+
     wallet_state_manager: WalletStateManager
     log: logging.Logger
     wallet_info: WalletInfo
     wallet_id: uint8
     standard_wallet: Wallet
     """
     interface used by datalayer for interacting with the chain
@@ -210,35 +216,23 @@
         peer: WSChiaConnection,
         spend: Optional[CoinSpend] = None,
         height: Optional[uint32] = None,
     ) -> None:
         if await self.wallet_state_manager.dl_store.get_launcher(launcher_id) is not None:
             self.log.info(f"Spend of launcher {launcher_id} has already been processed")
             return None
-        if spend is not None and spend.coin.name() == launcher_id:  # spend.coin.name() == launcher_id is a sanity check
-            await self.new_launcher_spend(spend, peer, height)
-        else:
+        if spend is None or height is None:
             launcher_state: CoinState = await self.get_launcher_coin_state(launcher_id, peer)
-            launcher_spend = await fetch_coin_spend_for_coin_state(launcher_state, peer)
-            await self.new_launcher_spend(launcher_spend, peer)
+            spend = await fetch_coin_spend_for_coin_state(launcher_state, peer)
+            assert launcher_state.spent_height is not None
+            height = uint32(launcher_state.spent_height)
 
-    async def new_launcher_spend(
-        self,
-        launcher_spend: CoinSpend,
-        peer: WSChiaConnection,
-        height: Optional[uint32] = None,
-    ) -> None:
-        launcher_id: bytes32 = launcher_spend.coin.name()
-        if height is None:
-            coin_state = await self.get_launcher_coin_state(launcher_id, peer)
-            height = None if coin_state.spent_height is None else uint32(coin_state.spent_height)
-            assert height is not None
-        full_puzhash, amount, root, inner_puzhash = launch_solution_to_singleton_info(
-            launcher_spend.solution.to_program()
-        )
+        assert spend.coin.name() == launcher_id, "coin_id should always match the launcher_id here"
+
+        full_puzhash, amount, root, inner_puzhash = launch_solution_to_singleton_info(spend.solution.to_program())
         new_singleton = Coin(launcher_id, full_puzhash, amount)
 
         singleton_record: Optional[SingletonRecord] = await self.wallet_state_manager.dl_store.get_latest_singleton(
             launcher_id
         )
         if singleton_record is not None:
             if (  # This is an unconfirmed singleton that we know about
@@ -265,15 +259,15 @@
                         create_host_layer_puzzle(inner_puzhash, root).get_tree_hash_precalc(inner_puzhash),
                         amount,
                     ),
                     generation=uint32(0),
                 )
             )
 
-        await self.wallet_state_manager.dl_store.add_launcher(launcher_spend.coin)
+        await self.wallet_state_manager.dl_store.add_launcher(spend.coin)
         await self.wallet_state_manager.add_interested_puzzle_hashes([launcher_id], [self.id()])
         await self.wallet_state_manager.add_interested_coin_ids([new_singleton.name()])
 
         new_singleton_coin_record: Optional[
             WalletCoinRecord
         ] = await self.wallet_state_manager.coin_store.get_coin_record(new_singleton.name())
         while new_singleton_coin_record is not None and new_singleton_coin_record.spent_block_height > 0:
@@ -527,24 +521,24 @@
                     next_full_puz_hash,
                     singleton_record.lineage_proof.amount,
                 ),
                 generation=uint32(second_singleton_record.generation + 1),
             )
 
         # Create the solution
-        primaries: List[AmountWithPuzzlehash] = [
-            {
-                "puzzlehash": announce_only.get_tree_hash() if announce_new_state else new_puz_hash,
-                "amount": singleton_record.lineage_proof.amount if new_amount is None else new_amount,
-                "memos": [
+        primaries = [
+            Payment(
+                announce_only.get_tree_hash() if announce_new_state else new_puz_hash,
+                singleton_record.lineage_proof.amount if new_amount is None else new_amount,
+                [
                     launcher_id,
                     root_hash,
                     announce_only.get_tree_hash() if announce_new_state else new_puz_hash,
                 ],
-            }
+            )
         ]
         inner_sol: Program = self.standard_wallet.make_solution(
             primaries=primaries,
             coin_announcements={b"$"} if fee > 0 else None,
             coin_announcements_to_assert={a.name() for a in coin_announcements_to_consume}
             if coin_announcements_to_consume is not None
             else None,
@@ -756,17 +750,15 @@
 
         await self.standard_wallet.hack_populate_secret_key_for_puzzle_hash(parent_coin.puzzle_hash)
 
         parent_inner_puzzle: Program = self.standard_wallet.puzzle_for_pk(inner_puzzle_derivation.pubkey)
         new_puzhash: bytes32 = await self.get_new_puzzlehash()
         excess_fee: int = fee - mirror_coin.amount
         inner_sol: Program = self.standard_wallet.make_solution(
-            primaries=[{"puzzlehash": new_puzhash, "amount": uint64(mirror_coin.amount - fee), "memos": []}]
-            if excess_fee < 0
-            else [],
+            primaries=[Payment(new_puzhash, uint64(mirror_coin.amount - fee))] if excess_fee < 0 else [],
             coin_announcements={b"$"} if excess_fee > 0 else None,
         )
         mirror_spend = CoinSpend(
             mirror_coin,
             SerializedProgram.from_program(create_mirror_puzzle()),
             Program.to(
                 [
@@ -1387,13 +1379,7 @@
     taker_from_reference = {
         store.store_id: [leaf_hash(key=inclusion.key, value=inclusion.value) for inclusion in store.inclusions]
         for store in taker
     }
 
     if taker_from_offer != taker_from_reference:
         raise OfferIntegrityError("taker: reference and offer inclusions do not match")
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = DataLayerWallet()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/data_store.py` & `chia-blockchain-2.0.0b1/chia/data_layer/data_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/dl_wallet_store.py` & `chia-blockchain-2.0.0b1/chia/data_layer/dl_wallet_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/download_data.py` & `chia-blockchain-2.0.0b1/chia/data_layer/download_data.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/s3_plugin_config.yml` & `chia-blockchain-2.0.0b1/chia/data_layer/s3_plugin_config.yml`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/s3_plugin_service.py` & `chia-blockchain-2.0.0b1/chia/data_layer/s3_plugin_service.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/data_layer/util/benchmark.py` & `chia-blockchain-2.0.0b1/chia/data_layer/util/benchmark.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/farmer/farmer.py` & `chia-blockchain-2.0.0b1/chia/farmer/farmer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/farmer/farmer_api.py` & `chia-blockchain-2.0.0b1/chia/farmer/farmer_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/bitcoin_fee_estimator.py` & `chia-blockchain-2.0.0b1/chia/full_node/bitcoin_fee_estimator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/block_height_map.py` & `chia-blockchain-2.0.0b1/chia/full_node/block_height_map.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/block_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/block_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/bundle_tools.py` & `chia-blockchain-2.0.0b1/chia/full_node/bundle_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/coin_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/coin_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimate.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimate.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimate_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimate_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimation.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_constants.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_example.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_example.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_estimator_interface.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_estimator_interface.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_history.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_history.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/fee_tracker.py` & `chia-blockchain-2.0.0b1/chia/full_node/fee_tracker.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/full_node.py` & `chia-blockchain-2.0.0b1/chia/full_node/full_node.py`

 * *Files 0% similar despite different names*

```diff
@@ -2207,17 +2207,16 @@
         if self.mempool_manager.get_spendbundle(spend_name) is not None:
             self.mempool_manager.remove_seen(spend_name)
             return MempoolInclusionStatus.SUCCESS, None
         if self.mempool_manager.seen(spend_name):
             return MempoolInclusionStatus.FAILED, Err.ALREADY_INCLUDING_TRANSACTION
         self.mempool_manager.add_and_maybe_pop_seen(spend_name)
         self.log.debug(f"Processing transaction: {spend_name}")
-        # Ignore if syncing or if we have not yet received a block
-        # the mempool must have a peak to validate transactions
-        if self.sync_store.get_sync_mode() or self.mempool_manager.peak is None:
+        # Ignore if syncing
+        if self.sync_store.get_sync_mode():
             status = MempoolInclusionStatus.FAILED
             error: Optional[Err] = Err.NO_TRANSACTIONS_WHILE_SYNCING
             self.mempool_manager.remove_seen(spend_name)
         else:
             try:
                 cost_result = await self.mempool_manager.pre_validate_spendbundle(transaction, tx_bytes, spend_name)
             except ValidationError as e:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/full_node_api.py` & `chia-blockchain-2.0.0b1/chia/full_node/full_node_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/full_node_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/full_node_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/generator.py` & `chia-blockchain-2.0.0b1/chia/full_node/generator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/hint_management.py` & `chia-blockchain-2.0.0b1/chia/full_node/hint_management.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/hint_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/hint_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/lock_queue.py` & `chia-blockchain-2.0.0b1/chia/full_node/lock_queue.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/mempool.py` & `chia-blockchain-2.0.0b1/chia/full_node/mempool.py`

 * *Files 3% similar despite different names*

```diff
@@ -136,54 +136,65 @@
 
     def total_mempool_cost(self) -> CLVMCost:
         with self._db_conn:
             cursor = self._db_conn.execute("SELECT SUM(cost) FROM tx")
             val = cursor.fetchone()[0]
             return CLVMCost(uint64(0) if val is None else uint64(val))
 
-    def all_spends(self) -> Iterator[MempoolItem]:
+    def all_items(self) -> Iterator[MempoolItem]:
         with self._db_conn:
             cursor = self._db_conn.execute("SELECT * FROM tx")
             for row in cursor:
                 yield self._row_to_item(row)
 
-    def all_spend_ids(self) -> List[bytes32]:
+    def all_item_ids(self) -> List[bytes32]:
         with self._db_conn:
             cursor = self._db_conn.execute("SELECT name FROM tx")
             return [bytes32(row[0]) for row in cursor]
 
     # TODO: move "process_mempool_items()" into this class in order to do this a
     # bit more efficiently
-    def spends_by_feerate(self) -> Iterator[MempoolItem]:
+    def items_by_feerate(self) -> Iterator[MempoolItem]:
         with self._db_conn:
             cursor = self._db_conn.execute("SELECT * FROM tx ORDER BY fee_per_cost DESC, seq ASC")
             for row in cursor:
                 yield self._row_to_item(row)
 
     def size(self) -> int:
         with self._db_conn:
             cursor = self._db_conn.execute("SELECT Count(name) FROM tx")
             val = cursor.fetchone()
             return 0 if val is None else int(val[0])
 
-    def get_spend_by_id(self, spend_bundle_id: bytes32) -> Optional[MempoolItem]:
+    def get_item_by_id(self, item_id: bytes32) -> Optional[MempoolItem]:
         with self._db_conn:
-            cursor = self._db_conn.execute("SELECT * FROM tx WHERE name=?", (spend_bundle_id,))
+            cursor = self._db_conn.execute("SELECT * FROM tx WHERE name=?", (item_id,))
             row = cursor.fetchone()
             return None if row is None else self._row_to_item(row)
 
     # TODO: we need a bulk lookup function like this too
-    def get_spends_by_coin_id(self, spent_coin_id: bytes32) -> List[MempoolItem]:
+    def get_items_by_coin_id(self, spent_coin_id: bytes32) -> List[MempoolItem]:
         with self._db_conn:
             cursor = self._db_conn.execute(
                 "SELECT * FROM tx WHERE name in (SELECT tx FROM spends WHERE coin_id=?)",
                 (spent_coin_id,),
             )
             return [self._row_to_item(row) for row in cursor]
 
+    def get_items_by_coin_ids(self, spent_coin_ids: List[bytes32]) -> List[MempoolItem]:
+        items: List[MempoolItem] = []
+        for coin_ids in chunks(spent_coin_ids, SQLITE_MAX_VARIABLE_NUMBER):
+            args = ",".join(["?"] * len(coin_ids))
+            with self._db_conn:
+                cursor = self._db_conn.execute(
+                    f"SELECT * FROM tx WHERE name IN (SELECT tx FROM spends WHERE coin_id IN ({args}))", tuple(coin_ids)
+                )
+                items.extend(self._row_to_item(row) for row in cursor)
+        return items
+
     def get_min_fee_rate(self, cost: int) -> float:
         """
         Gets the minimum fpc rate that a transaction with specified cost will need in order to get included.
         """
 
         if self.at_full_capacity(cost):
             # TODO: make MempoolItem.cost be CLVMCost
@@ -378,15 +389,15 @@
         self, item_inclusion_filter: Callable[[bytes32], bool]
     ) -> Optional[Tuple[SpendBundle, List[Coin]]]:
         cost_sum = 0  # Checks that total cost does not exceed block maximum
         fee_sum = 0  # Checks that total fees don't exceed 64 bits
         spend_bundles: List[SpendBundle] = []
         additions: List[Coin] = []
         log.info(f"Starting to make block, max cost: {self.mempool_info.max_block_clvm_cost}")
-        for item in self.spends_by_feerate():
+        for item in self.items_by_feerate():
             if not item_inclusion_filter(item.name):
                 continue
             log.info("Cumulative cost: %d, fee per cost: %0.4f", cost_sum, item.fee_per_cost)
             if (
                 item.cost + cost_sum > self.mempool_info.max_block_clvm_cost
                 or item.fee + fee_sum > DEFAULT_CONSTANTS.MAX_COIN_AMOUNT
             ):
```

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/mempool_check_conditions.py` & `chia-blockchain-2.0.0b1/chia/full_node/mempool_check_conditions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/mempool_manager.py` & `chia-blockchain-2.0.0b1/chia/full_node/mempool_manager.py`

 * *Files 2% similar despite different names*

```diff
@@ -32,15 +32,14 @@
 from chia.types.spend_bundle import SpendBundle
 from chia.types.spend_bundle_conditions import SpendBundleConditions
 from chia.util import cached_bls
 from chia.util.cached_bls import LOCAL_CACHE
 from chia.util.condition_tools import pkm_pairs
 from chia.util.db_wrapper import SQLITE_INT_MAX
 from chia.util.errors import Err, ValidationError
-from chia.util.generator_tools import additions_for_npc
 from chia.util.inline_executor import InlineExecutor
 from chia.util.ints import uint32, uint64
 from chia.util.lru_cache import LRUCache
 from chia.util.setproctitle import getproctitle, setproctitle
 
 log = logging.getLogger(__name__)
 
@@ -225,15 +224,15 @@
 
             item_inclusion_filter = always
         return self.mempool.create_bundle_from_mempool_items(item_inclusion_filter)
 
     def get_filter(self) -> bytes:
         all_transactions: Set[bytes32] = set()
         byte_array_list = []
-        for key in self.mempool.all_spend_ids():
+        for key in self.mempool.all_item_ids():
             if key not in all_transactions:
                 all_transactions.add(key)
                 byte_array_list.append(bytearray(key))
 
         tx_filter: PyBIP158 = PyBIP158(byte_array_list)
         return bytes(tx_filter.GetEncoded())
 
@@ -320,15 +319,15 @@
         Returns:
             Optional[uint64]: cost of the entire transaction, None iff status is FAILED
             MempoolInclusionStatus:  SUCCESS (should add to pool), FAILED (cannot add), and PENDING (can add later)
             Optional[Err]: Err is set iff status is FAILED
         """
 
         # Skip if already added
-        existing_item = self.mempool.get_spend_by_id(spend_name)
+        existing_item = self.mempool.get_item_by_id(spend_name)
         if existing_item is not None:
             return existing_item.cost, MempoolInclusionStatus.SUCCESS, None
 
         err, item, remove_items = await self.validate_spend_bundle(
             new_spend, npc_result, spend_name, first_added_height
         )
         if err is None:
@@ -385,26 +384,28 @@
         if npc_result.error is not None:
             return Err(npc_result.error), None, []
 
         cost = npc_result.cost
         log.debug(f"Cost: {cost}")
 
         assert npc_result.conds is not None
-        # build set of removals
-        removal_names: Set[bytes32] = set(bytes32(spend.coin_id) for spend in npc_result.conds.spends)
-        if removal_names != set(s.name() for s in new_spend.removals()):
-            # If you reach here it's probably because your program reveal doesn't match the coin's puzzle hash
-            return Err.INVALID_SPEND_BUNDLE, None, []
-
-        additions: List[Coin] = additions_for_npc(npc_result)
+        removal_names: Set[bytes32] = set()
         additions_dict: Dict[bytes32, Coin] = {}
         addition_amount: int = 0
-        for add in additions:
-            additions_dict[add.name()] = add
-            addition_amount = addition_amount + add.amount
+        for spend in npc_result.conds.spends:
+            coin_id = bytes32(spend.coin_id)
+            removal_names.add(coin_id)
+            for puzzle_hash, amount, _ in spend.create_coin:
+                child_coin = Coin(coin_id, puzzle_hash, amount)
+                additions_dict[child_coin.name()] = child_coin
+                addition_amount = addition_amount + child_coin.amount
+
+        if removal_names != set(coin_spend.coin.name() for coin_spend in new_spend.coin_spends):
+            # If you reach here it's probably because your program reveal doesn't match the coin's puzzle hash
+            return Err.INVALID_SPEND_BUNDLE, None, []
 
         removal_record_dict: Dict[bytes32, CoinRecord] = {}
         removal_amount: int = 0
         for name in removal_names:
             removal_record = await self.get_coin_record(name)
             if removal_record is None and name not in additions_dict:
                 return Err.UNKNOWN_UNSPENT, None, []
@@ -511,53 +512,51 @@
             logging.DEBUG if duration < 2 else logging.WARNING,
             f"add_spendbundle {spend_name} took {duration:0.2f} seconds. "
             f"Cost: {cost} ({round(100.0 * cost/self.constants.MAX_BLOCK_COST_CLVM, 3)}% of max block cost)",
         )
 
         return None, potential, [item.name for item in conflicts]
 
-    def check_removals(self, removals: Dict[bytes32, CoinRecord]) -> Tuple[Optional[Err], Set[MempoolItem]]:
+    def check_removals(self, removals: Dict[bytes32, CoinRecord]) -> Tuple[Optional[Err], List[MempoolItem]]:
         """
         This function checks for double spends, unknown spends and conflicting transactions in mempool.
         Returns Error (if any), the set of existing MempoolItems with conflicting spends (if any).
         Note that additions are not checked for duplicates, because having duplicate additions requires also
         having duplicate removals.
         """
         assert self.peak is not None
-        conflicts: Set[MempoolItem] = set()
-
+        removals_ids = []
         for record in removals.values():
             removal = record.coin
             # 1. Checks if it's been spent already
             if record.spent:
-                return Err.DOUBLE_SPEND, set()
-            # 2. Checks if there's a mempool conflict
-            items: List[MempoolItem] = self.mempool.get_spends_by_coin_id(removal.name())
-            conflicts.update(items)
-
+                return Err.DOUBLE_SPEND, []
+            removals_ids.append(removal.name())
+        # 2. Checks if there are mempool conflicts
+        conflicts = self.mempool.get_items_by_coin_ids(removals_ids)
         if len(conflicts) > 0:
             return Err.MEMPOOL_CONFLICT, conflicts
         # 5. If coins can be spent return list of unspents as we see them in local storage
-        return None, set()
+        return None, []
 
     def get_spendbundle(self, bundle_hash: bytes32) -> Optional[SpendBundle]:
         """Returns a full SpendBundle if it's inside one the mempools"""
-        item: Optional[MempoolItem] = self.mempool.get_spend_by_id(bundle_hash)
+        item: Optional[MempoolItem] = self.mempool.get_item_by_id(bundle_hash)
         if item is not None:
             return item.spend_bundle
         return None
 
     def get_mempool_item(self, bundle_hash: bytes32, include_pending: bool = False) -> Optional[MempoolItem]:
         """
         Returns the MempoolItem in the mempool that matches the provided spend bundle hash (id)
         or None if not found.
 
         If include_pending is specified, also check the PENDING cache.
         """
-        item = self.mempool.get_spend_by_id(bundle_hash)
+        item = self.mempool.get_item_by_id(bundle_hash)
         if not item and include_pending:
             # no async lock needed since we're not mutating the pending_cache
             item = self._pending_cache.get(bundle_hash)
         if not item and include_pending:
             item = self._conflict_cache.get(bundle_hash)
 
         return item
@@ -589,25 +588,25 @@
             if last_npc_result.conds is not None:
                 # transactions in the mempool may be spending multiple coins,
                 # when looking up transactions by all coin IDs, we're likely to
                 # find the same transaction multiple times. We put them in a set
                 # to deduplicate
                 spendbundle_ids_to_remove: Set[bytes32] = set()
                 for spend in last_npc_result.conds.spends:
-                    items: List[MempoolItem] = self.mempool.get_spends_by_coin_id(bytes32(spend.coin_id))
+                    items: List[MempoolItem] = self.mempool.get_items_by_coin_id(bytes32(spend.coin_id))
                     for item in items:
                         included_items.append(MempoolItemInfo(item.cost, item.fee, item.height_added_to_mempool))
                         self.remove_seen(item.name)
                         spendbundle_ids_to_remove.add(item.name)
                 self.mempool.remove_from_pool(list(spendbundle_ids_to_remove), MempoolRemoveReason.BLOCK_INCLUSION)
         else:
             old_pool = self.mempool
             self.mempool = Mempool(old_pool.mempool_info, old_pool.fee_estimator)
             self.seen_bundle_hashes = {}
-            for item in old_pool.all_spends():
+            for item in old_pool.all_items():
                 _, result, err = await self.add_spend_bundle(
                     item.spend_bundle, item.npc_result, item.spend_bundle_name, item.height_added_to_mempool
                 )
                 # Only add to `seen` if inclusion worked, so it can be resubmitted in case of a reorg
                 if result == MempoolInclusionStatus.SUCCESS:
                     self.add_and_maybe_pop_seen(item.spend_bundle_name)
                 # If the spend bundle was confirmed or conflicting (can no longer be in mempool), it won't be
@@ -636,15 +635,15 @@
 
     def get_items_not_in_filter(self, mempool_filter: PyBIP158, limit: int = 100) -> List[SpendBundle]:
         items: List[SpendBundle] = []
 
         assert limit > 0
 
         # Send 100 with the highest fee per cost
-        for item in self.mempool.spends_by_feerate():
+        for item in self.mempool.items_by_feerate():
             if len(items) >= limit:
                 return items
             if mempool_filter.Match(bytearray(item.spend_bundle_name)):
                 continue
             items.append(item.spend_bundle)
 
         return items
@@ -658,15 +657,15 @@
 
 
 def optional_max(a: Optional[T], b: Optional[T]) -> Optional[T]:
     return max((v for v in [a, b] if v is not None), default=None)
 
 
 def can_replace(
-    conflicting_items: Set[MempoolItem],
+    conflicting_items: List[MempoolItem],
     removal_names: Set[bytes32],
     new_item: MempoolItem,
 ) -> bool:
     """
     This function implements the mempool replacement rules. Given a Mempool item
     we're attempting to insert into the mempool (new_item) and the set of existing
     mempool items that conflict with it, this function answers the question whether
```

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/pending_tx_cache.py` & `chia-blockchain-2.0.0b1/chia/full_node/pending_tx_cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/subscriptions.py` & `chia-blockchain-2.0.0b1/chia/full_node/subscriptions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/sync_store.py` & `chia-blockchain-2.0.0b1/chia/full_node/sync_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/tx_processing_queue.py` & `chia-blockchain-2.0.0b1/chia/full_node/tx_processing_queue.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/full_node/weight_proof.py` & `chia-blockchain-2.0.0b1/chia/full_node/weight_proof.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/harvester/harvester.py` & `chia-blockchain-2.0.0b1/chia/harvester/harvester.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/harvester/harvester_api.py` & `chia-blockchain-2.0.0b1/chia/harvester/harvester_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/introducer/introducer.py` & `chia-blockchain-2.0.0b1/chia/introducer/introducer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/introducer/introducer_api.py` & `chia-blockchain-2.0.0b1/chia/introducer/introducer_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plot_sync/delta.py` & `chia-blockchain-2.0.0b1/chia/plot_sync/delta.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plot_sync/exceptions.py` & `chia-blockchain-2.0.0b1/chia/plot_sync/exceptions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plot_sync/receiver.py` & `chia-blockchain-2.0.0b1/chia/plot_sync/receiver.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plot_sync/sender.py` & `chia-blockchain-2.0.0b1/chia/plot_sync/sender.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plot_sync/util.py` & `chia-blockchain-2.0.0b1/chia/plot_sync/util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotters/bladebit.py` & `chia-blockchain-2.0.0b1/chia/plotters/bladebit.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotters/chiapos.py` & `chia-blockchain-2.0.0b1/chia/plotters/chiapos.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotters/madmax.py` & `chia-blockchain-2.0.0b1/chia/plotters/madmax.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotters/plotters.py` & `chia-blockchain-2.0.0b1/chia/plotters/plotters.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotters/plotters_util.py` & `chia-blockchain-2.0.0b1/chia/plotters/plotters_util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotting/cache.py` & `chia-blockchain-2.0.0b1/chia/plotting/cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotting/check_plots.py` & `chia-blockchain-2.0.0b1/chia/plotting/check_plots.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotting/create_plots.py` & `chia-blockchain-2.0.0b1/chia/plotting/create_plots.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotting/manager.py` & `chia-blockchain-2.0.0b1/chia/plotting/manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/plotting/util.py` & `chia-blockchain-2.0.0b1/chia/plotting/util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/pools/pool_config.py` & `chia-blockchain-2.0.0b1/chia/pools/pool_config.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/pools/pool_puzzles.py` & `chia-blockchain-2.0.0b1/chia/pools/pool_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/pools/pool_wallet.py` & `chia-blockchain-2.0.0b1/chia/pools/pool_wallet.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from __future__ import annotations
 
 import dataclasses
 import logging
 import time
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple, cast
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, cast
 
 from blspy import G1Element, G2Element, PrivateKey
 from typing_extensions import final
 
 from chia.pools.pool_config import PoolWalletConfig, load_pool_config, update_pool_config
 from chia.pools.pool_puzzles import (
     SINGLETON_LAUNCHER,
@@ -55,14 +55,19 @@
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 
 
 @final
 @dataclasses.dataclass
 class PoolWallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("PoolWallet", None)
+
     MINIMUM_INITIAL_BALANCE = 1
     MINIMUM_RELATIVE_LOCK_HEIGHT = 5
     MAXIMUM_RELATIVE_LOCK_HEIGHT = 1000
     DEFAULT_MAX_CLAIM_SPENDS = 100
 
     wallet_state_manager: Any
     log: logging.Logger
@@ -984,13 +989,7 @@
         return False
 
     def puzzle_hash_for_pk(self, pubkey: G1Element) -> bytes32:
         raise RuntimeError("PoolWallet does not support puzzle_hash_for_pk")
 
     def get_name(self) -> str:
         return self.wallet_info.name
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = cast(PoolWallet, None)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/pools/pool_wallet_info.py` & `chia-blockchain-2.0.0b1/chia/pools/pool_wallet_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/farmer_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/farmer_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/full_node_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/full_node_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/harvester_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/harvester_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/introducer_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/introducer_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/pool_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/pool_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/protocol_message_types.py` & `chia-blockchain-2.0.0b1/chia/protocols/protocol_message_types.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/protocol_state_machine.py` & `chia-blockchain-2.0.0b1/chia/protocols/protocol_state_machine.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/shared_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/shared_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/timelord_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/timelord_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/protocols/wallet_protocol.py` & `chia-blockchain-2.0.0b1/chia/protocols/wallet_protocol.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from __future__ import annotations
 
 from dataclasses import dataclass
 from typing import List, Optional, Tuple
 
-from chia_rs import CoinState, RespondToPhUpdates
+import chia_rs
 
 from chia.full_node.fee_estimate import FeeEstimateGroup
 from chia.types.blockchain_format.coin import Coin
 from chia.types.blockchain_format.serialized_program import SerializedProgram
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.header_block import HeaderBlock
 from chia.types.spend_bundle import SpendBundle
@@ -16,15 +16,16 @@
 
 """
 Protocol between wallet (SPV node) and full node.
 Note: When changing this file, also change protocol_message_types.py, and the protocol version in shared_protocol.py
 """
 
 
-__all__ = ["CoinState", "RespondToPhUpdates"]
+CoinState = chia_rs.CoinState
+RespondToPhUpdates = chia_rs.RespondToPhUpdates
 
 
 @streamable
 @dataclass(frozen=True)
 class RequestPuzzleSolution(Streamable):
     coin_name: bytes32
     height: uint32
```

### Comparing `chia-blockchain-1.8.1rc2/chia/pyinstaller.spec` & `chia-blockchain-2.0.0b1/chia/pyinstaller.spec`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/crawler_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/crawler_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/data_layer_rpc_util.py` & `chia-blockchain-2.0.0b1/chia/rpc/data_layer_rpc_util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/farmer_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/farmer_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/farmer_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/farmer_rpc_client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/full_node_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/full_node_rpc_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -720,20 +720,20 @@
 
         return {
             "additions": [coin_record_dict_backwards_compat(cr.to_json_dict()) for cr in additions],
             "removals": [coin_record_dict_backwards_compat(cr.to_json_dict()) for cr in removals],
         }
 
     async def get_all_mempool_tx_ids(self, _: Dict[str, Any]) -> EndpointResult:
-        ids = list(self.service.mempool_manager.mempool.all_spend_ids())
+        ids = list(self.service.mempool_manager.mempool.all_item_ids())
         return {"tx_ids": ids}
 
     async def get_all_mempool_items(self, _: Dict[str, Any]) -> EndpointResult:
         spends = {}
-        for item in self.service.mempool_manager.mempool.all_spends():
+        for item in self.service.mempool_manager.mempool.all_items():
             spends[item.name.hex()] = item.to_json_dict()
         return {"mempool_items": spends}
 
     async def get_mempool_item_by_tx_id(self, request: Dict[str, Any]) -> EndpointResult:
         if "tx_id" not in request:
             raise ValueError("No tx_id in request")
         include_pending: bool = request.get("include_pending", False)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/full_node_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/full_node_rpc_client.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,66 +1,66 @@
 from __future__ import annotations
 
-from typing import Any, Dict, List, Optional, Tuple
+from typing import Any, Dict, List, Optional, Tuple, cast
 
 from chia.consensus.block_record import BlockRecord
 from chia.full_node.signage_point import SignagePoint
 from chia.rpc.rpc_client import RpcClient
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.coin_record import CoinRecord
 from chia.types.coin_spend import CoinSpend
 from chia.types.end_of_slot_bundle import EndOfSubSlotBundle
 from chia.types.full_block import FullBlock
 from chia.types.spend_bundle import SpendBundle
 from chia.types.unfinished_header_block import UnfinishedHeaderBlock
 from chia.util.byte_types import hexstr_to_bytes
-from chia.util.ints import uint32, uint64
+from chia.util.ints import uint32
 
 
-def coin_record_dict_backwards_compat(coin_record: Dict[str, Any]):
+def coin_record_dict_backwards_compat(coin_record: Dict[str, Any]) -> Dict[str, Any]:
     del coin_record["spent"]
     return coin_record
 
 
 class FullNodeRpcClient(RpcClient):
     """
     Client to Chia RPC, connects to a local full node. Uses HTTP/JSON, and converts back from
     JSON into native python objects before returning. All api calls use POST requests.
     Note that this is not the same as the peer protocol, or wallet protocol (which run Chia's
     protocol on top of TCP), it's a separate protocol on top of HTTP that provides easy access
     to the full node.
     """
 
-    async def get_blockchain_state(self) -> Dict:
+    async def get_blockchain_state(self) -> Dict[str, Any]:
         response = await self.fetch("get_blockchain_state", {})
         if response["blockchain_state"]["peak"] is not None:
             response["blockchain_state"]["peak"] = BlockRecord.from_json_dict(response["blockchain_state"]["peak"])
-        return response["blockchain_state"]
+        return cast(Dict[str, Any], response["blockchain_state"])
 
-    async def get_block(self, header_hash) -> Optional[FullBlock]:
+    async def get_block(self, header_hash: bytes32) -> Optional[FullBlock]:
         try:
             response = await self.fetch("get_block", {"header_hash": header_hash.hex()})
         except Exception:
             return None
         return FullBlock.from_json_dict(response["block"])
 
     async def get_blocks(self, start: int, end: int, exclude_reorged: bool = False) -> List[FullBlock]:
         response = await self.fetch(
             "get_blocks", {"start": start, "end": end, "exclude_header_hash": True, "exclude_reorged": exclude_reorged}
         )
         return [FullBlock.from_json_dict(block) for block in response["blocks"]]
 
-    async def get_block_record_by_height(self, height) -> Optional[BlockRecord]:
+    async def get_block_record_by_height(self, height: int) -> Optional[BlockRecord]:
         try:
             response = await self.fetch("get_block_record_by_height", {"height": height})
         except Exception:
             return None
         return BlockRecord.from_json_dict(response["block_record"])
 
-    async def get_block_record(self, header_hash) -> Optional[BlockRecord]:
+    async def get_block_record(self, header_hash: bytes32) -> Optional[BlockRecord]:
         try:
             response = await self.fetch("get_block_record", {"header_hash": header_hash.hex()})
             if response["block_record"] is None:
                 return None
         except Exception:
             return None
         return BlockRecord.from_json_dict(response["block_record"])
@@ -69,28 +69,24 @@
         response = await self.fetch("get_unfinished_block_headers", {})
         return [UnfinishedHeaderBlock.from_json_dict(r) for r in response["headers"]]
 
     async def get_all_block(self, start: uint32, end: uint32) -> List[FullBlock]:
         response = await self.fetch("get_blocks", {"start": start, "end": end, "exclude_header_hash": True})
         return [FullBlock.from_json_dict(r) for r in response["blocks"]]
 
-    async def get_network_space(
-        self, newer_block_header_hash: bytes32, older_block_header_hash: bytes32
-    ) -> Optional[uint64]:
-        try:
-            network_space_bytes_estimate = await self.fetch(
-                "get_network_space",
-                {
-                    "newer_block_header_hash": newer_block_header_hash.hex(),
-                    "older_block_header_hash": older_block_header_hash.hex(),
-                },
-            )
-        except Exception:
-            return None
-        return network_space_bytes_estimate["space"]
+    async def get_network_space(self, newer_block_header_hash: bytes32, older_block_header_hash: bytes32) -> int:
+        network_space_bytes_estimate = await self.fetch(
+            "get_network_space",
+            {
+                "newer_block_header_hash": newer_block_header_hash.hex(),
+                "older_block_header_hash": older_block_header_hash.hex(),
+            },
+        )
+
+        return cast(int, network_space_bytes_estimate["space"])
 
     async def get_coin_record_by_name(self, coin_id: bytes32) -> Optional[CoinRecord]:
         try:
             response = await self.fetch("get_coin_record_by_name", {"name": coin_id.hex()})
         except Exception:
             return None
 
@@ -98,15 +94,15 @@
 
     async def get_coin_records_by_names(
         self,
         names: List[bytes32],
         include_spent_coins: bool = True,
         start_height: Optional[int] = None,
         end_height: Optional[int] = None,
-    ) -> List:
+    ) -> List[CoinRecord]:
         names_hex = [name.hex() for name in names]
         d = {"names": names_hex, "include_spent_coins": include_spent_coins}
         if start_height is not None:
             d["start_height"] = start_height
         if end_height is not None:
             d["end_height"] = end_height
 
@@ -115,15 +111,15 @@
 
     async def get_coin_records_by_puzzle_hash(
         self,
         puzzle_hash: bytes32,
         include_spent_coins: bool = True,
         start_height: Optional[int] = None,
         end_height: Optional[int] = None,
-    ) -> List:
+    ) -> List[CoinRecord]:
         d = {"puzzle_hash": puzzle_hash.hex(), "include_spent_coins": include_spent_coins}
         if start_height is not None:
             d["start_height"] = start_height
         if end_height is not None:
             d["end_height"] = end_height
 
         response = await self.fetch("get_coin_records_by_puzzle_hash", d)
@@ -131,15 +127,15 @@
 
     async def get_coin_records_by_puzzle_hashes(
         self,
         puzzle_hashes: List[bytes32],
         include_spent_coins: bool = True,
         start_height: Optional[int] = None,
         end_height: Optional[int] = None,
-    ) -> List:
+    ) -> List[CoinRecord]:
         puzzle_hashes_hex = [ph.hex() for ph in puzzle_hashes]
         d = {"puzzle_hashes": puzzle_hashes_hex, "include_spent_coins": include_spent_coins}
         if start_height is not None:
             d["start_height"] = start_height
         if end_height is not None:
             d["end_height"] = end_height
 
@@ -148,15 +144,15 @@
 
     async def get_coin_records_by_parent_ids(
         self,
         parent_ids: List[bytes32],
         include_spent_coins: bool = True,
         start_height: Optional[int] = None,
         end_height: Optional[int] = None,
-    ) -> List:
+    ) -> List[CoinRecord]:
         parent_ids_hex = [pid.hex() for pid in parent_ids]
         d = {"parent_ids": parent_ids_hex, "include_spent_coins": include_spent_coins}
         if start_height is not None:
             d["start_height"] = start_height
         if end_height is not None:
             d["end_height"] = end_height
 
@@ -165,15 +161,15 @@
 
     async def get_coin_records_by_hint(
         self,
         hint: bytes32,
         include_spent_coins: bool = True,
         start_height: Optional[int] = None,
         end_height: Optional[int] = None,
-    ) -> List:
+    ) -> List[CoinRecord]:
         d = {"hint": hint.hex(), "include_spent_coins": include_spent_coins}
         if start_height is not None:
             d["start_height"] = start_height
         if end_height is not None:
             d["end_height"] = end_height
 
         response = await self.fetch("get_coin_records_by_hint", d)
@@ -188,61 +184,65 @@
         additions = []
         for coin_record in response["removals"]:
             removals.append(CoinRecord.from_json_dict(coin_record_dict_backwards_compat(coin_record)))
         for coin_record in response["additions"]:
             additions.append(CoinRecord.from_json_dict(coin_record_dict_backwards_compat(coin_record)))
         return additions, removals
 
-    async def get_block_records(self, start: int, end: int) -> List:
+    async def get_block_records(self, start: int, end: int) -> List[Dict[str, Any]]:
         try:
             response = await self.fetch("get_block_records", {"start": start, "end": end})
             if response["block_records"] is None:
                 return []
         except Exception:
             return []
         # TODO: return block records
-        return response["block_records"]
+        return cast(List[Dict[str, Any]], response["block_records"])
 
     async def get_block_spends(self, header_hash: bytes32) -> Optional[List[CoinSpend]]:
         try:
             response = await self.fetch("get_block_spends", {"header_hash": header_hash.hex()})
             block_spends = []
             for block_spend in response["block_spends"]:
                 block_spends.append(CoinSpend.from_json_dict(block_spend))
             return block_spends
         except Exception:
             return None
 
-    async def push_tx(self, spend_bundle: SpendBundle):
+    async def push_tx(self, spend_bundle: SpendBundle) -> Dict[str, Any]:
         return await self.fetch("push_tx", {"spend_bundle": spend_bundle.to_json_dict()})
 
     async def get_puzzle_and_solution(self, coin_id: bytes32, height: uint32) -> Optional[CoinSpend]:
         try:
             response = await self.fetch("get_puzzle_and_solution", {"coin_id": coin_id.hex(), "height": height})
             return CoinSpend.from_json_dict(response["coin_solution"])
         except Exception:
             return None
 
     async def get_all_mempool_tx_ids(self) -> List[bytes32]:
         response = await self.fetch("get_all_mempool_tx_ids", {})
         return [bytes32(hexstr_to_bytes(tx_id_hex)) for tx_id_hex in response["tx_ids"]]
 
-    async def get_all_mempool_items(self) -> Dict[bytes32, Dict]:
-        response: Dict = await self.fetch("get_all_mempool_items", {})
-        converted: Dict[bytes32, Dict] = {}
+    async def get_all_mempool_items(self) -> Dict[bytes32, Dict[str, Any]]:
+        response = await self.fetch("get_all_mempool_items", {})
+        converted: Dict[bytes32, Dict[str, Any]] = {}
         for tx_id_hex, item in response["mempool_items"].items():
             converted[bytes32(hexstr_to_bytes(tx_id_hex))] = item
         return converted
 
-    async def get_mempool_item_by_tx_id(self, tx_id: bytes32, include_pending: bool = False) -> Optional[Dict]:
+    async def get_mempool_item_by_tx_id(
+        self,
+        tx_id: bytes32,
+        include_pending: bool = False,
+    ) -> Optional[Dict[str, Any]]:
         try:
             response = await self.fetch(
                 "get_mempool_item_by_tx_id", {"tx_id": tx_id.hex(), "include_pending": include_pending}
             )
-            return response["mempool_item"]
+            return cast(Dict[str, Any], response["mempool_item"])
         except Exception:
             return None
 
     async def get_recent_signage_point_or_eos(
         self, sp_hash: Optional[bytes32], challenge_hash: Optional[bytes32]
     ) -> Optional[Any]:
         try:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/harvester_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/harvester_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/harvester_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/harvester_rpc_client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/rpc_client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/rpc_server.py` & `chia-blockchain-2.0.0b1/chia/rpc/rpc_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/timelord_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/timelord_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/util.py` & `chia-blockchain-2.0.0b1/chia/rpc/util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/wallet_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/rpc/wallet_rpc_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,18 +24,19 @@
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.coin_record import CoinRecord
 from chia.types.coin_spend import CoinSpend
 from chia.types.signing_mode import SigningMode
 from chia.types.spend_bundle import SpendBundle
 from chia.util.bech32m import decode_puzzle_hash, encode_puzzle_hash
 from chia.util.byte_types import hexstr_to_bytes
-from chia.util.config import load_config
+from chia.util.config import load_config, str2bool
 from chia.util.errors import KeychainIsLocked
 from chia.util.ints import uint16, uint32, uint64
 from chia.util.keychain import bytes_to_mnemonic, generate_mnemonic
+from chia.util.misc import UInt32Range
 from chia.util.path import path_from_root
 from chia.util.ws_message import WsRpcMessage, create_payload_dict
 from chia.wallet.cat_wallet.cat_constants import DEFAULT_CATS
 from chia.wallet.cat_wallet.cat_wallet import CATWallet
 from chia.wallet.derive_keys import (
     MAX_POOL_WALLETS,
     master_sk_to_farmer_sk,
@@ -55,29 +56,31 @@
 from chia.wallet.nft_wallet import nft_puzzles
 from chia.wallet.nft_wallet.nft_info import NFTCoinInfo, NFTInfo
 from chia.wallet.nft_wallet.nft_puzzles import get_metadata_and_phs
 from chia.wallet.nft_wallet.nft_wallet import NFTWallet
 from chia.wallet.nft_wallet.uncurry_nft import UncurriedNFT
 from chia.wallet.notification_store import Notification
 from chia.wallet.outer_puzzles import AssetType
+from chia.wallet.payment import Payment
 from chia.wallet.puzzle_drivers import PuzzleInfo, Solver
 from chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle import puzzle_hash_for_synthetic_public_key
 from chia.wallet.singleton import create_singleton_puzzle
 from chia.wallet.trade_record import TradeRecord
 from chia.wallet.trading.offer import Offer
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.uncurried_puzzle import uncurry_puzzle
 from chia.wallet.util.address_type import AddressType, is_valid_address
 from chia.wallet.util.compute_hints import compute_coin_hints
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.transaction_type import TransactionType
 from chia.wallet.util.wallet_sync_utils import fetch_coin_spend_for_coin_state
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash, WalletType
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import CHIP_0002_SIGN_MESSAGE_PREFIX, Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
+from chia.wallet.wallet_coin_store import HashFilter
 from chia.wallet.wallet_info import WalletInfo
 from chia.wallet.wallet_node import WalletNode
 from chia.wallet.wallet_protocol import WalletProtocol
 
 # Timeout for response from wallet/full node for sending a transaction
 TIMEOUT = 30
 MAX_DERIVATION_INDEX_DELTA = 1000
@@ -925,18 +928,18 @@
         if max_coin_amount == 0:
             max_coin_amount = uint64(self.service.wallet_state_manager.constants.MAX_COIN_AMOUNT)
         exclude_coin_amounts: Optional[List[uint64]] = request.get("exclude_coin_amounts")
         if exclude_coin_amounts is not None:
             exclude_coin_amounts = [uint64(a) for a in exclude_coin_amounts]
         exclude_coin_ids: Optional[List] = request.get("exclude_coin_ids")
         if exclude_coin_ids is not None:
-            coin_records = await self.service.wallet_state_manager.coin_store.get_coin_records(
-                [bytes32.from_hexstr(hex_id) for hex_id in exclude_coin_ids]
+            result = await self.service.wallet_state_manager.coin_store.get_coin_records(
+                coin_id_filter=HashFilter.include([bytes32.from_hexstr(hex_id) for hex_id in exclude_coin_ids])
             )
-            exclude_coins = {wr.coin for wr in coin_records.values()}
+            exclude_coins = {wr.coin for wr in result.records}
         else:
             exclude_coins = set()
 
         async with self.service.wallet_state_manager.lock:
             tx: TransactionRecord = await wallet.generate_signed_transaction(
                 amount,
                 puzzle_hash,
@@ -1098,32 +1101,36 @@
 
     async def get_coin_records_by_names(self, request) -> EndpointResult:
         if await self.service.wallet_state_manager.synced() is False:
             raise ValueError("Wallet needs to be fully synced before finding coin information")
 
         if "names" not in request:
             raise ValueError("Names not in request")
+        coin_ids = [bytes32.from_hexstr(name) for name in request["names"]]
         kwargs: Dict[str, Any] = {
-            "include_spent_coins": False,
-            "coin_names": [hexstr_to_bytes(name) for name in request["names"]],
+            "coin_id_filter": HashFilter.include(coin_ids),
         }
+
+        confirmed_range = UInt32Range()
         if "start_height" in request:
-            kwargs["start_height"] = uint32(request["start_height"])
+            confirmed_range = dataclasses.replace(confirmed_range, start=uint32(request["start_height"]))
         if "end_height" in request:
-            kwargs["end_height"] = uint32(request["end_height"])
+            confirmed_range = dataclasses.replace(confirmed_range, stop=uint32(request["end_height"]))
+        if confirmed_range != UInt32Range():
+            kwargs["confirmed_range"] = confirmed_range
 
-        if "include_spent_coins" in request:
-            kwargs["include_spent_coins"] = request["include_spent_coins"]
+        if "include_spent_coins" in request and not str2bool(request["include_spent_coins"]):
+            kwargs["spent_range"] = UInt32Range(start=uint32(uint32.MAXIMUM_EXCLUSIVE - 1))
 
         async with self.service.wallet_state_manager.lock:
             coin_records: List[CoinRecord] = await self.service.wallet_state_manager.get_coin_records_by_coin_ids(
                 **kwargs
             )
             missed_coins: List[str] = [
-                "0x" + c_id.hex() for c_id in kwargs["coin_names"] if c_id not in [cr.name for cr in coin_records]
+                "0x" + c_id.hex() for c_id in coin_ids if c_id not in [cr.name for cr in coin_records]
             ]
             if missed_coins:
                 raise ValueError(f"Coin ID's: {missed_coins} not found.")
 
         return {"coin_records": [cr.to_json_dict() for cr in coin_records]}
 
     async def get_current_derivation_index(self, request) -> Dict[str, Any]:
@@ -1417,18 +1424,18 @@
         if max_coin_amount == 0:
             max_coin_amount = uint64(self.service.wallet_state_manager.constants.MAX_COIN_AMOUNT)
         exclude_coin_amounts: Optional[List[uint64]] = request.get("exclude_coin_amounts")
         if exclude_coin_amounts is not None:
             exclude_coin_amounts = [uint64(a) for a in exclude_coin_amounts]
         exclude_coin_ids: Optional[List] = request.get("exclude_coin_ids")
         if exclude_coin_ids is not None:
-            coin_records = await self.service.wallet_state_manager.coin_store.get_coin_records(
-                [bytes32.from_hexstr(hex_id) for hex_id in exclude_coin_ids]
+            result = await self.service.wallet_state_manager.coin_store.get_coin_records(
+                coin_id_filter=HashFilter.include([bytes32.from_hexstr(hex_id) for hex_id in exclude_coin_ids])
             )
-            exclude_coins = {wr.coin for wr in coin_records.values()}
+            exclude_coins = {wr.coin for wr in result.records}
         else:
             exclude_coins = None
         cat_discrepancy_params: Tuple[Optional[int], Optional[str], Optional[str]] = (
             request.get("extra_delta", None),
             request.get("tail_reveal", None),
             request.get("tail_solution", None),
         )
@@ -1818,21 +1825,25 @@
         memos = compute_memos(SpendBundle([coin_spend], G2Element()))
         hints = []
         if coin_state.coin.name() in memos:
             for memo in memos[coin_state.coin.name()]:
                 hints.append(memo.hex())
         return {
             "success": True,
+            "did_id": encode_puzzle_hash(
+                bytes32.from_hexstr(singleton_struct.rest().first().atom.hex()),
+                AddressType.DID.hrp(self.service.config),
+            ),
             "latest_coin": coin_state.coin.name().hex(),
             "p2_address": encode_puzzle_hash(p2_puzzle.get_tree_hash(), AddressType.XCH.hrp(self.service.config)),
-            "public_key": public_key.as_python().hex(),
-            "recovery_list_hash": recovery_list_hash.as_python().hex(),
+            "public_key": public_key.atom.hex(),
+            "recovery_list_hash": recovery_list_hash.atom.hex(),
             "num_verification": num_verification.as_int(),
             "metadata": program_to_metadata(metadata),
-            "launcher_id": singleton_struct.rest().first().as_python().hex(),
+            "launcher_id": singleton_struct.rest().first().atom.hex(),
             "full_puzzle": full_puzzle,
             "solution": Program.from_bytes(bytes(coin_spend.solution)).as_python(),
             "hints": hints,
         }
 
     async def did_find_lost_did(self, request) -> EndpointResult:
         """
@@ -2863,24 +2874,24 @@
         assert amount_0 <= self.service.constants.MAX_COIN_AMOUNT
         puzzle_hash_0 = bytes32.from_hexstr(additions[0]["puzzle_hash"])
         if len(puzzle_hash_0) != 32:
             raise ValueError(f"Address must be 32 bytes. {puzzle_hash_0.hex()}")
 
         memos_0 = [] if "memos" not in additions[0] else [mem.encode("utf-8") for mem in additions[0]["memos"]]
 
-        additional_outputs: List[AmountWithPuzzlehash] = []
+        additional_outputs: List[Payment] = []
         for addition in additions[1:]:
             receiver_ph = bytes32.from_hexstr(addition["puzzle_hash"])
             if len(receiver_ph) != 32:
                 raise ValueError(f"Address must be 32 bytes. {receiver_ph.hex()}")
             amount = uint64(addition["amount"])
             if amount > self.service.constants.MAX_COIN_AMOUNT:
                 raise ValueError(f"Coin amount cannot exceed {self.service.constants.MAX_COIN_AMOUNT}")
             memos = [] if "memos" not in addition else [mem.encode("utf-8") for mem in addition["memos"]]
-            additional_outputs.append({"puzzlehash": receiver_ph, "amount": amount, "memos": memos})
+            additional_outputs.append(Payment(receiver_ph, amount, memos))
 
         fee: uint64 = uint64(request.get("fee", 0))
         min_coin_amount: uint64 = uint64(request.get("min_coin_amount", 0))
         max_coin_amount: uint64 = uint64(request.get("max_coin_amount", 0))
         if max_coin_amount == 0:
             max_coin_amount = uint64(self.service.wallet_state_manager.constants.MAX_COIN_AMOUNT)
         exclude_coin_amounts: Optional[List[uint64]] = request.get("exclude_coin_amounts")
@@ -2950,21 +2961,21 @@
 
                 return {"signed_txs": [signed_tx], "signed_tx": signed_tx}
 
             else:
                 assert isinstance(wallet, CATWallet)
 
                 txs = await wallet.generate_signed_transaction(
-                    [amount_0] + [output["amount"] for output in additional_outputs],
-                    [bytes32(puzzle_hash_0)] + [output["puzzlehash"] for output in additional_outputs],
+                    [amount_0] + [output.amount for output in additional_outputs],
+                    [bytes32(puzzle_hash_0)] + [output.puzzle_hash for output in additional_outputs],
                     fee,
                     coins=coins,
                     exclude_cat_coins=exclude_coins,
                     ignore_max_send_amount=True,
-                    memos=[memos_0] + [output["memos"] for output in additional_outputs],
+                    memos=[memos_0] + [output.memos for output in additional_outputs],
                     coin_announcements_to_consume=coin_announcements,
                     puzzle_announcements_to_consume=puzzle_announcements,
                     min_coin_amount=min_coin_amount,
                     max_coin_amount=max_coin_amount,
                     exclude_coin_amounts=exclude_coin_amounts,
                 )
                 signed_txs = [tx.to_json_dict_convenience(self.service.config) for tx in txs]
```

### Comparing `chia-blockchain-1.8.1rc2/chia/rpc/wallet_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/rpc/wallet_rpc_client.py`

 * *Files 2% similar despite different names*

```diff
@@ -417,14 +417,22 @@
     async def get_did_id(self, wallet_id: int) -> Dict:
         request: Dict[str, Any] = {
             "wallet_id": wallet_id,
         }
         response = await self.fetch("did_get_did", request)
         return response
 
+    async def get_did_info(self, coin_id: str, latest: bool) -> Dict:
+        request: Dict[str, Any] = {
+            "coin_id": coin_id,
+            "latest": latest,
+        }
+        response = await self.fetch("did_get_info", request)
+        return response
+
     async def create_did_backup_file(self, wallet_id: int, filename: str) -> Dict:
         request: Dict[str, Any] = {
             "wallet_id": wallet_id,
             "filename": filename,
         }
         response = await self.fetch("did_create_backup_file", request)
         return response
@@ -448,14 +456,25 @@
     async def get_did_recovery_list(self, wallet_id: int) -> Dict:
         request: Dict[str, Any] = {
             "wallet_id": wallet_id,
         }
         response = await self.fetch("did_get_recovery_list", request)
         return response
 
+    async def did_message_spend(
+        self, wallet_id: int, puzzle_announcements: List[str], coin_announcements: List[str]
+    ) -> Dict:
+        request: Dict[str, Any] = {
+            "wallet_id": wallet_id,
+            "coin_announcements": coin_announcements,
+            "puzzle_announcements": puzzle_announcements,
+        }
+        response = await self.fetch("did_message_spend", request)
+        return response
+
     async def update_did_metadata(
         self,
         wallet_id: int,
         metadata: Dict,
         reuse_puzhash: Optional[bool] = None,
     ) -> Dict:
         request: Dict[str, Any] = {
@@ -469,14 +488,29 @@
     async def get_did_metadata(self, wallet_id: int) -> Dict:
         request: Dict[str, Any] = {
             "wallet_id": wallet_id,
         }
         response = await self.fetch("did_get_metadata", request)
         return response
 
+    async def find_lost_did(
+        self, coin_id: str, recovery_list_hash: Optional[str], metadata: Optional[Dict], num_verification: Optional[int]
+    ) -> Dict:
+        request: Dict[str, Any] = {
+            "coin_id": coin_id,
+        }
+        if recovery_list_hash is not None:
+            request["recovery_list_hash"] = recovery_list_hash
+        if metadata is not None:
+            request["metadata"] = (metadata,)
+        if num_verification is not None:
+            request["num_verification"] = num_verification
+        response = await self.fetch("did_find_lost_did", request)
+        return response
+
     async def create_new_did_wallet_from_recovery(self, filename: str) -> Dict:
         request: Dict[str, Any] = {
             "wallet_type": "did_wallet",
             "did_type": "recovery",
             "filename": filename,
         }
         response = await self.fetch("create_new_wallet", request)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/crawl_store.py` & `chia-blockchain-2.0.0b1/chia/seeder/crawl_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/crawler.py` & `chia-blockchain-2.0.0b1/chia/seeder/crawler.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/crawler_api.py` & `chia-blockchain-2.0.0b1/chia/seeder/crawler_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/dns_server.py` & `chia-blockchain-2.0.0b1/chia/seeder/dns_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/peer_record.py` & `chia-blockchain-2.0.0b1/chia/seeder/peer_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/seeder/start_crawler.py` & `chia-blockchain-2.0.0b1/chia/seeder/start_crawler.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/address_manager.py` & `chia-blockchain-2.0.0b1/chia/server/address_manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/address_manager_sqlite_store.py` & `chia-blockchain-2.0.0b1/chia/server/address_manager_sqlite_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/address_manager_store.py` & `chia-blockchain-2.0.0b1/chia/server/address_manager_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/capabilities.py` & `chia-blockchain-2.0.0b1/chia/server/capabilities.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/chia_policy.py` & `chia-blockchain-2.0.0b1/chia/server/chia_policy.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/introducer_peers.py` & `chia-blockchain-2.0.0b1/chia/server/introducer_peers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/node_discovery.py` & `chia-blockchain-2.0.0b1/chia/server/node_discovery.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/outbound_message.py` & `chia-blockchain-2.0.0b1/chia/server/outbound_message.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/peer_store_resolver.py` & `chia-blockchain-2.0.0b1/chia/server/peer_store_resolver.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/rate_limit_numbers.py` & `chia-blockchain-2.0.0b1/chia/server/rate_limit_numbers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/rate_limits.py` & `chia-blockchain-2.0.0b1/chia/server/rate_limits.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/server.py` & `chia-blockchain-2.0.0b1/chia/server/server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/ssl_context.py` & `chia-blockchain-2.0.0b1/chia/server/ssl_context.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_data_layer.py` & `chia-blockchain-2.0.0b1/chia/server/start_data_layer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_farmer.py` & `chia-blockchain-2.0.0b1/chia/server/start_farmer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_full_node.py` & `chia-blockchain-2.0.0b1/chia/server/start_full_node.py`

 * *Files 6% similar despite different names*

```diff
@@ -70,19 +70,20 @@
 async def async_main(service_config: Dict[str, Any]) -> int:
     # TODO: refactor to avoid the double load
     config = load_config(DEFAULT_ROOT_PATH, "config.yaml")
     config[SERVICE_NAME] = service_config
     network_id = service_config["selected_network"]
     overrides = service_config["network_overrides"]["constants"][network_id]
     if network_id == "testnet10":
-        # activate softforks immediately on testnet
+        # testnet10 is 1031258 blocks behind mainnet
+        testnet10_offset = 1031258
         if "SOFT_FORK2_HEIGHT" not in overrides:
-            overrides["SOFT_FORK2_HEIGHT"] = 0
+            overrides["SOFT_FORK2_HEIGHT"] = 3886635 - testnet10_offset
         if "SOFT_FORK_HEIGHT" not in overrides:
-            overrides["SOFT_FORK_HEIGHT"] = 0
+            overrides["SOFT_FORK_HEIGHT"] = 3630000 - testnet10_offset
     updated_constants = DEFAULT_CONSTANTS.replace_str_to_bytes(**overrides)
     initialize_service_logging(service_name=SERVICE_NAME, config=config)
     service = create_full_node_service(DEFAULT_ROOT_PATH, config, updated_constants)
     await service.setup_process_global_state()
     await service.run()
 
     return 0
```

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_harvester.py` & `chia-blockchain-2.0.0b1/chia/server/start_harvester.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_introducer.py` & `chia-blockchain-2.0.0b1/chia/server/start_introducer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_service.py` & `chia-blockchain-2.0.0b1/chia/server/start_service.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_timelord.py` & `chia-blockchain-2.0.0b1/chia/server/start_timelord.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/start_wallet.py` & `chia-blockchain-2.0.0b1/chia/server/start_wallet.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/upnp.py` & `chia-blockchain-2.0.0b1/chia/server/upnp.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/server/ws_connection.py` & `chia-blockchain-2.0.0b1/chia/server/ws_connection.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/block_tools.py` & `chia-blockchain-2.0.0b1/chia/simulator/block_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/full_node_simulator.py` & `chia-blockchain-2.0.0b1/chia/simulator/full_node_simulator.py`

 * *Files 0% similar despite different names*

```diff
@@ -20,16 +20,16 @@
 from chia.types.blockchain_format.coin import Coin
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.coin_record import CoinRecord
 from chia.types.full_block import FullBlock
 from chia.types.spend_bundle import SpendBundle
 from chia.util.config import lock_and_load_config, save_config
 from chia.util.ints import uint8, uint32, uint64, uint128
+from chia.wallet.payment import Payment
 from chia.wallet.transaction_record import TransactionRecord
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash
 from chia.wallet.wallet import Wallet
 from chia.wallet.wallet_node import WalletNode
 from chia.wallet.wallet_state_manager import WalletStateManager
 
 
 class _Default:
     pass
@@ -594,42 +594,42 @@
             if len(invalid_amounts) > 0:
                 invalid_amounts_string = ", ".join(str(amount) for amount in invalid_amounts)
                 raise Exception(f"Coins must have a positive value, request included: {invalid_amounts_string}")
 
             if len(amounts) == 0:
                 return set()
 
-            outputs: List[AmountWithPuzzlehash] = []
+            outputs: List[Payment] = []
             for amount in amounts:
                 puzzle_hash = await wallet.get_new_puzzlehash()
-                outputs.append({"puzzlehash": puzzle_hash, "amount": uint64(amount), "memos": []})
+                outputs.append(Payment(puzzle_hash, amount))
 
             transaction_records: List[TransactionRecord] = []
             outputs_iterator = iter(outputs)
             while True:
                 # The outputs iterator must be second in the zip() call otherwise we lose
                 # an element when reaching the end of the range object.
                 outputs_group = [output for _, output in zip(range(per_transaction_record_group), outputs_iterator)]
 
                 if len(outputs_group) > 0:
                     async with wallet.wallet_state_manager.lock:
                         tx = await wallet.generate_signed_transaction(
-                            amount=outputs_group[0]["amount"],
-                            puzzle_hash=outputs_group[0]["puzzlehash"],
+                            amount=outputs_group[0].amount,
+                            puzzle_hash=outputs_group[0].puzzle_hash,
                             primaries=outputs_group[1:],
                         )
                     await wallet.push_transaction(tx=tx)
                     transaction_records.append(tx)
                 else:
                     break
 
             await self.process_transaction_records(records=transaction_records, timeout=None)
 
             output_coins = {coin for transaction_record in transaction_records for coin in transaction_record.additions}
-            puzzle_hashes = {output["puzzlehash"] for output in outputs}
+            puzzle_hashes = {output.puzzle_hash for output in outputs}
             change_coins = {coin for coin in output_coins if coin.puzzle_hash not in puzzle_hashes}
             coins_to_receive = output_coins - change_coins
             await wait_for_coins_in_wallet(coins=coins_to_receive, wallet=wallet)
 
             return coins_to_receive
 
     def tx_id_in_mempool(self, tx_id: bytes32) -> bool:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/keyring.py` & `chia-blockchain-2.0.0b1/chia/simulator/keyring.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/setup_nodes.py` & `chia-blockchain-2.0.0b1/chia/simulator/setup_nodes.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/setup_services.py` & `chia-blockchain-2.0.0b1/chia/simulator/setup_services.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/simulator_constants.py` & `chia-blockchain-2.0.0b1/chia/simulator/simulator_constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/simulator_full_node_rpc_api.py` & `chia-blockchain-2.0.0b1/chia/simulator/simulator_full_node_rpc_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/simulator_full_node_rpc_client.py` & `chia-blockchain-2.0.0b1/chia/simulator/simulator_full_node_rpc_client.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/simulator_protocol.py` & `chia-blockchain-2.0.0b1/chia/simulator/simulator_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/simulator_test_tools.py` & `chia-blockchain-2.0.0b1/chia/simulator/simulator_test_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/socket.py` & `chia-blockchain-2.0.0b1/chia/simulator/socket.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_1.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_1.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_10.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_10.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_2.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_2.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_3.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_3.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_4.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_4.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_5.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_5.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_6.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_6.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_7.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_7.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_8.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_8.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/ssl_certs_9.py` & `chia-blockchain-2.0.0b1/chia/simulator/ssl_certs_9.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/start_simulator.py` & `chia-blockchain-2.0.0b1/chia/simulator/start_simulator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/time_out_assert.py` & `chia-blockchain-2.0.0b1/chia/simulator/time_out_assert.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/simulator/wallet_tools.py` & `chia-blockchain-2.0.0b1/chia/simulator/wallet_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/ssl/chia_ca.crt` & `chia-blockchain-2.0.0b1/chia/ssl/chia_ca.crt`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/ssl/chia_ca.key` & `chia-blockchain-2.0.0b1/chia/ssl/chia_ca.key`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/ssl/create_ssl.py` & `chia-blockchain-2.0.0b1/chia/ssl/create_ssl.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/ssl/dst_root_ca.pem` & `chia-blockchain-2.0.0b1/chia/ssl/dst_root_ca.pem`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/timelord/iters_from_block.py` & `chia-blockchain-2.0.0b1/chia/timelord/iters_from_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/timelord/timelord.py` & `chia-blockchain-2.0.0b1/chia/timelord/timelord.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/timelord/timelord_api.py` & `chia-blockchain-2.0.0b1/chia/timelord/timelord_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/timelord/timelord_launcher.py` & `chia-blockchain-2.0.0b1/chia/timelord/timelord_launcher.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/timelord/timelord_state.py` & `chia-blockchain-2.0.0b1/chia/timelord/timelord_state.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/announcement.py` & `chia-blockchain-2.0.0b1/chia/types/announcement.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/block_protocol.py` & `chia-blockchain-2.0.0b1/chia/types/block_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/classgroup.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/classgroup.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/coin.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/coin.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/foliage.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/foliage.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/program.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/program.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/proof_of_space.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/proof_of_space.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/reward_chain_block.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/reward_chain_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/serialized_program.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/serialized_program.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/slots.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/slots.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/sub_epoch_summary.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/sub_epoch_summary.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/tree_hash.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/tree_hash.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/blockchain_format/vdf.py` & `chia-blockchain-2.0.0b1/chia/types/blockchain_format/vdf.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/coin_record.py` & `chia-blockchain-2.0.0b1/chia/types/coin_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/coin_spend.py` & `chia-blockchain-2.0.0b1/chia/types/coin_spend.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/condition_opcodes.py` & `chia-blockchain-2.0.0b1/chia/types/condition_opcodes.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/end_of_slot_bundle.py` & `chia-blockchain-2.0.0b1/chia/types/end_of_slot_bundle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/fee_rate.py` & `chia-blockchain-2.0.0b1/chia/types/fee_rate.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/full_block.py` & `chia-blockchain-2.0.0b1/chia/types/full_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/generator_types.py` & `chia-blockchain-2.0.0b1/chia/types/generator_types.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/header_block.py` & `chia-blockchain-2.0.0b1/chia/types/header_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/mempool_item.py` & `chia-blockchain-2.0.0b1/chia/types/mempool_item.py`

 * *Files 8% similar despite different names*

```diff
@@ -40,16 +40,15 @@
 
     @property
     def name(self) -> bytes32:
         return self.spend_bundle_name
 
     @property
     def cost(self) -> uint64:
-        assert self.npc_result.conds is not None
-        return uint64(self.npc_result.conds.cost)
+        return self.npc_result.cost
 
     @property
     def additions(self) -> List[Coin]:
         return additions_for_npc(self.npc_result)
 
     @property
     def removals(self) -> List[Coin]:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/types/mempool_submission_status.py` & `chia-blockchain-2.0.0b1/chia/types/mempool_submission_status.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/peer_info.py` & `chia-blockchain-2.0.0b1/chia/types/peer_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/signing_mode.py` & `chia-blockchain-2.0.0b1/chia/types/signing_mode.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/spend_bundle.py` & `chia-blockchain-2.0.0b1/chia/types/spend_bundle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/transaction_queue_entry.py` & `chia-blockchain-2.0.0b1/chia/types/transaction_queue_entry.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/unfinished_block.py` & `chia-blockchain-2.0.0b1/chia/types/unfinished_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/unfinished_header_block.py` & `chia-blockchain-2.0.0b1/chia/types/unfinished_header_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/types/weight_proof.py` & `chia-blockchain-2.0.0b1/chia/types/weight_proof.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/api_decorators.py` & `chia-blockchain-2.0.0b1/chia/util/api_decorators.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/bech32m.py` & `chia-blockchain-2.0.0b1/chia/util/bech32m.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/beta_metrics.py` & `chia-blockchain-2.0.0b1/chia/util/beta_metrics.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/block_cache.py` & `chia-blockchain-2.0.0b1/chia/util/block_cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/byte_types.py` & `chia-blockchain-2.0.0b1/chia/util/byte_types.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/cached_bls.py` & `chia-blockchain-2.0.0b1/chia/util/cached_bls.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/check_fork_next_block.py` & `chia-blockchain-2.0.0b1/chia/util/check_fork_next_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/chia_logging.py` & `chia-blockchain-2.0.0b1/chia/util/chia_logging.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/condition_tools.py` & `chia-blockchain-2.0.0b1/chia/util/condition_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/config.py` & `chia-blockchain-2.0.0b1/chia/util/config.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/create_alert_file.py` & `chia-blockchain-2.0.0b1/chia/util/create_alert_file.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/db_synchronous.py` & `chia-blockchain-2.0.0b1/chia/util/db_synchronous.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/db_version.py` & `chia-blockchain-2.0.0b1/chia/util/db_version.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/db_wrapper.py` & `chia-blockchain-2.0.0b1/chia/util/db_wrapper.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/dump_keyring.py` & `chia-blockchain-2.0.0b1/chia/util/dump_keyring.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/english.txt` & `chia-blockchain-2.0.0b1/chia/util/english.txt`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/errors.py` & `chia-blockchain-2.0.0b1/chia/util/errors.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/file_keyring.py` & `chia-blockchain-2.0.0b1/chia/util/file_keyring.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/files.py` & `chia-blockchain-2.0.0b1/chia/util/files.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/full_block_utils.py` & `chia-blockchain-2.0.0b1/chia/util/full_block_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/generator_tools.py` & `chia-blockchain-2.0.0b1/chia/util/generator_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/initial-config.yaml` & `chia-blockchain-2.0.0b1/chia/util/initial-config.yaml`

 * *Files 1% similar despite different names*

```diff
@@ -67,16 +67,16 @@
       DIFFICULTY_STARTING: 30
       EPOCH_BLOCKS: 768
       GENESIS_CHALLENGE: ae83525ba8d1dd3f09b277de18ca3e43fc0af20d20c4b3e92ef2a48bd291ccb2
       GENESIS_PRE_FARM_FARMER_PUZZLE_HASH: 3d8765d3a597ec1d99663f6c9816d915b9f68613ac94009884c4addaefcce6af
       GENESIS_PRE_FARM_POOL_PUZZLE_HASH: d23da14695a188ae5708dd152263c4db883eb27edeb936178d4d988b8f3ce5fc
       MEMPOOL_BLOCK_BUFFER: 10
       MIN_PLOT_SIZE: 18
-      SOFT_FORK_HEIGHT: 0
-      SOFT_FORK2_HEIGHT: 0
+      SOFT_FORK_HEIGHT: 2598742
+      SOFT_FORK2_HEIGHT: 2855377
   config:
     mainnet:
       address_prefix: "xch"
       default_full_node_port: 8444
     testnet0:
       address_prefix: "txch"
       default_full_node_port: 58444
```

### Comparing `chia-blockchain-1.8.1rc2/chia/util/inline_executor.py` & `chia-blockchain-2.0.0b1/chia/util/inline_executor.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/ints.py` & `chia-blockchain-2.0.0b1/chia/util/ints.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/json_util.py` & `chia-blockchain-2.0.0b1/chia/util/json_util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/keychain.py` & `chia-blockchain-2.0.0b1/chia/util/keychain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/keyring_wrapper.py` & `chia-blockchain-2.0.0b1/chia/util/keyring_wrapper.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/limited_semaphore.py` & `chia-blockchain-2.0.0b1/chia/util/limited_semaphore.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/lock.py` & `chia-blockchain-2.0.0b1/chia/util/lock.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/logging.py` & `chia-blockchain-2.0.0b1/chia/util/logging.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/lru_cache.py` & `chia-blockchain-2.0.0b1/chia/util/lru_cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/merkle_set.py` & `chia-blockchain-2.0.0b1/chia/util/merkle_set.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/misc.py` & `chia-blockchain-2.0.0b1/chia/util/misc.py`

 * *Files 8% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 import dataclasses
 import signal
 import sys
 from pathlib import Path
 from typing import Any, Dict, Sequence, Union
 
 from chia.util.errors import InvalidPathError
-from chia.util.ints import uint16
+from chia.util.ints import uint16, uint32, uint64
 from chia.util.streamable import Streamable, recurse_jsonify, streamable
 
 
 @streamable
 @dataclasses.dataclass(frozen=True)
 class VersionedBlob(Streamable):
     version: uint16
@@ -111,7 +111,21 @@
 
 if sys.platform == "win32" or sys.platform == "cygwin":
     termination_signals = [signal.SIGBREAK, signal.SIGINT, signal.SIGTERM]
     sendable_termination_signals = [signal.SIGTERM]
 else:
     termination_signals = [signal.SIGINT, signal.SIGTERM]
     sendable_termination_signals = termination_signals
+
+
+@streamable
+@dataclasses.dataclass(frozen=True)
+class UInt32Range(Streamable):
+    start: uint32 = uint32(0)
+    stop: uint32 = uint32(uint32.MAXIMUM_EXCLUSIVE - 1)
+
+
+@streamable
+@dataclasses.dataclass(frozen=True)
+class UInt64Range(Streamable):
+    start: uint64 = uint64(0)
+    stop: uint64 = uint64(uint64.MAXIMUM_EXCLUSIVE - 1)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/util/network.py` & `chia-blockchain-2.0.0b1/chia/util/network.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/paginator.py` & `chia-blockchain-2.0.0b1/chia/util/paginator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/partial_func.py` & `chia-blockchain-2.0.0b1/chia/util/partial_func.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/path.py` & `chia-blockchain-2.0.0b1/chia/util/path.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/pprint.py` & `chia-blockchain-2.0.0b1/chia/util/pprint.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/prev_transaction_block.py` & `chia-blockchain-2.0.0b1/chia/util/prev_transaction_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/profiler.py` & `chia-blockchain-2.0.0b1/chia/util/profiler.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/service_groups.py` & `chia-blockchain-2.0.0b1/chia/util/service_groups.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/significant_bits.py` & `chia-blockchain-2.0.0b1/chia/util/significant_bits.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/ssl_check.py` & `chia-blockchain-2.0.0b1/chia/util/ssl_check.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/streamable.py` & `chia-blockchain-2.0.0b1/chia/util/streamable.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/struct_stream.py` & `chia-blockchain-2.0.0b1/chia/util/struct_stream.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/task_timing.py` & `chia-blockchain-2.0.0b1/chia/util/task_timing.py`

 * *Files 1% similar despite different names*

```diff
@@ -151,14 +151,17 @@
 
 def get_file(frame: FrameType) -> str:
     code = frame.f_code
     return f"{strip_filename(code.co_filename)}:{code.co_firstlineno}"
 
 
 def trace_fun(frame: FrameType, event: str, arg: Any) -> None:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     if event in ["c_call", "c_return", "c_exception"]:
         return
 
     # we only care about instrumenting co-routines
     if (frame.f_code.co_flags & inspect.CO_COROUTINE) == 0:  # pylint: disable=no-member
         # with open("instrumentation.log", "a") as f:
         #    f.write(f"[1]    {event} {get_fun(frame)}\n")
```

### Comparing `chia-blockchain-1.8.1rc2/chia/util/validate_alert.py` & `chia-blockchain-2.0.0b1/chia/util/validate_alert.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/vdf_prover.py` & `chia-blockchain-2.0.0b1/chia/util/vdf_prover.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/util/ws_message.py` & `chia-blockchain-2.0.0b1/chia/util/ws_message.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/block_record.py` & `chia-blockchain-2.0.0b1/chia/wallet/block_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_constants.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_info.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_outer_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_utils.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/cat_wallet.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/cat_wallet.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
 import dataclasses
 import logging
 import time
 import traceback
 from secrets import token_bytes
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, cast
 
 from blspy import AugSchemeMPL, G1Element, G2Element
 
 from chia.consensus.cost_calculator import NPCResult
 from chia.full_node.bundle_tools import simple_solution_generator
 from chia.full_node.mempool_check_conditions import get_name_puzzle_conditions
 from chia.server.ws_connection import WSChiaConnection
@@ -48,15 +48,15 @@
 from chia.wallet.puzzles.tails import ALL_LIMITATIONS_PROGRAMS
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.uncurried_puzzle import uncurry_puzzle
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.curry_and_treehash import calculate_hash_of_quoted_mod_hash, curry_and_treehash
 from chia.wallet.util.transaction_type import TransactionType
 from chia.wallet.util.wallet_sync_utils import fetch_coin_spend_for_coin_state
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash, WalletType
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 
 if TYPE_CHECKING:
     from chia.wallet.wallet_state_manager import WalletStateManager
 
@@ -64,14 +64,19 @@
 
 CAT_MOD_HASH = CAT_MOD.get_tree_hash()
 CAT_MOD_HASH_HASH = Program.to(CAT_MOD_HASH).get_tree_hash()
 QUOTED_MOD_HASH = calculate_hash_of_quoted_mod_hash(CAT_MOD_HASH)
 
 
 class CATWallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("CATWallet", None)
+
     wallet_state_manager: WalletStateManager
     log: logging.Logger
     wallet_info: WalletInfo
     cat_info: CATInfo
     standard_wallet: Wallet
     cost_of_single_tx: Optional[int]
     lineage_store: CATLineageStore
@@ -681,32 +686,30 @@
         elif payment_amount < starting_amount:
             regular_chia_to_claim = payment_amount
 
         need_chia_transaction = (fee > 0 or regular_chia_to_claim > 0) and (fee - regular_chia_to_claim != 0)
 
         # Calculate standard puzzle solutions
         change = selected_cat_amount - starting_amount
-        primaries: List[AmountWithPuzzlehash] = []
-        for payment in payments:
-            primaries.append({"puzzlehash": payment.puzzle_hash, "amount": payment.amount, "memos": payment.memos})
+        primaries = payments.copy()
 
         if change > 0:
             derivation_record = await self.wallet_state_manager.puzzle_store.get_derivation_record_for_puzzle_hash(
                 list(cat_coins)[0].puzzle_hash
             )
             if derivation_record is not None and reuse_puzhash:
                 change_puzhash = self.standard_wallet.puzzle_hash_for_pk(derivation_record.pubkey)
                 for payment in payments:
                     if change_puzhash == payment.puzzle_hash and change == payment.amount:
                         # We cannot create two coins has same id, create a new puzhash for the change
                         change_puzhash = await self.get_new_inner_hash()
                         break
             else:
                 change_puzhash = await self.get_new_inner_hash()
-            primaries.append({"puzzlehash": change_puzhash, "amount": uint64(change), "memos": []})
+            primaries.append(Payment(change_puzhash, uint64(change), [change_puzhash]))
 
         # Loop through the coins we've selected and gather the information we need to spend them
         spendable_cat_list = []
         chia_tx = None
         first = True
         announcement: Announcement
         for coin in cat_coins:
@@ -923,13 +926,7 @@
         min_coin_amount: Optional[uint64] = None,
         max_coin_amount: Optional[uint64] = None,
     ) -> Set[Coin]:
         balance = await self.get_confirmed_balance()
         if balance < amount:
             raise Exception(f"insufficient funds in wallet {self.id()}")
         return await self.select_coins(amount, min_coin_amount=min_coin_amount, max_coin_amount=max_coin_amount)
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = CATWallet()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/cat_wallet/lineage_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/cat_wallet/lineage_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/chialisp.py` & `chia-blockchain-2.0.0b1/chia/wallet/chialisp.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/coin_selection.py` & `chia-blockchain-2.0.0b1/chia/wallet/coin_selection.py`

 * *Ordering differences only*

 * *Files 8% similar despite different names*

```diff
@@ -1,191 +1,191 @@
-from __future__ import annotations
-
-import logging
-import random
-from typing import Dict, List, Optional, Set
-
-from chia.types.blockchain_format.coin import Coin
-from chia.types.blockchain_format.sized_bytes import bytes32
-from chia.util.ints import uint64, uint128
-from chia.wallet.wallet_coin_record import WalletCoinRecord
-
-
-async def select_coins(
-    spendable_amount: uint128,
-    max_coin_amount: uint64,
-    spendable_coins: List[WalletCoinRecord],
-    unconfirmed_removals: Dict[bytes32, Coin],
-    log: logging.Logger,
-    amount: uint128,
-    exclude: Optional[List[Coin]] = None,
-    min_coin_amount: Optional[uint64] = None,
-    excluded_coin_amounts: Optional[List[uint64]] = None,
-) -> Set[Coin]:
-    """
-    Returns a set of coins that can be used for generating a new transaction.
-    """
-    if exclude is None:
-        exclude = []
-    if min_coin_amount is None:
-        min_coin_amount = uint64(0)
-    if excluded_coin_amounts is None:
-        excluded_coin_amounts = []
-
-    if amount > spendable_amount:
-        error_msg = (
-            f"Can't select amount higher than our spendable balance.  Amount: {amount}, spendable: {spendable_amount}"
-        )
-        log.warning(error_msg)
-        raise ValueError(error_msg)
-
-    log.debug(f"About to select coins for amount {amount}")
-
-    max_num_coins = 500
-    sum_spendable_coins = 0
-    valid_spendable_coins: List[Coin] = []
-
-    for coin_record in spendable_coins:  # remove all the unconfirmed coins, excluded coins and dust.
-        if coin_record.coin.name() in unconfirmed_removals:
-            continue
-        if coin_record.coin in exclude:
-            continue
-        if coin_record.coin.amount < min_coin_amount or coin_record.coin.amount > max_coin_amount:
-            continue
-        if coin_record.coin.amount in excluded_coin_amounts:
-            continue
-        valid_spendable_coins.append(coin_record.coin)
-        sum_spendable_coins += coin_record.coin.amount
-
-    # This happens when we couldn't use one of the coins because it's already used
-    # but unconfirmed, and we are waiting for the change. (unconfirmed_additions)
-    if sum_spendable_coins < amount:
-        raise ValueError(
-            f"Transaction for {amount} is greater than spendable balance of {sum_spendable_coins}. "
-            "There may be other transactions pending or our minimum coin amount is too high."
-        )
-    if amount == 0 and sum_spendable_coins == 0:
-        raise ValueError(
-            "No coins available to spend, you can not create a coin with an amount of 0,"
-            " without already having coins."
-        )
-
-    # Sort the coins by amount
-    valid_spendable_coins.sort(reverse=True, key=lambda r: r.amount)
-
-    # check for exact 1 to 1 coin match.
-    exact_match_coin: Optional[Coin] = check_for_exact_match(valid_spendable_coins, uint64(amount))
-    if exact_match_coin:
-        log.debug(f"selected coin with an exact match: {exact_match_coin}")
-        return {exact_match_coin}
-
-    # Check for an exact match with all of the coins smaller than the amount.
-    # If we have more, smaller coins than the amount we run the next algorithm.
-    smaller_coin_sum = 0  # coins smaller than target.
-    smaller_coins: List[Coin] = []
-    for coin in valid_spendable_coins:
-        if coin.amount < amount:
-            smaller_coin_sum += coin.amount
-            smaller_coins.append(coin)
-    if smaller_coin_sum == amount and len(smaller_coins) < max_num_coins and amount != 0:
-        log.debug(f"Selected all smaller coins because they equate to an exact match of the target.: {smaller_coins}")
-        return set(smaller_coins)
-    elif smaller_coin_sum < amount:
-        smallest_coin: Optional[Coin] = select_smallest_coin_over_target(amount, valid_spendable_coins)
-        assert smallest_coin is not None  # Since we know we have enough, there must be a larger coin
-        log.debug(f"Selected closest greater coin: {smallest_coin.name()}")
-        return {smallest_coin}
-    elif smaller_coin_sum > amount:
-        coin_set: Optional[Set[Coin]] = knapsack_coin_algorithm(smaller_coins, amount, max_coin_amount, max_num_coins)
-        log.debug(f"Selected coins from knapsack algorithm: {coin_set}")
-        if coin_set is None:
-            coin_set = sum_largest_coins(amount, smaller_coins)
-            if coin_set is None or len(coin_set) > max_num_coins:
-                greater_coin = select_smallest_coin_over_target(amount, valid_spendable_coins)
-                if greater_coin is None:
-                    raise ValueError(
-                        f"Transaction of {amount} mojo would use more than "
-                        f"{max_num_coins} coins. Try sending a smaller amount"
-                    )
-                coin_set = {greater_coin}
-        return coin_set
-    else:
-        # if smaller_coin_sum == amount and (len(smaller_coins) >= max_num_coins or amount == 0)
-        potential_large_coin: Optional[Coin] = select_smallest_coin_over_target(amount, valid_spendable_coins)
-        if potential_large_coin is None:
-            raise ValueError("Too many coins are required to make this transaction")
-        log.debug(f"Resorted to selecting smallest coin over target due to dust.: {potential_large_coin}")
-        return {potential_large_coin}
-
-
-# These algorithms were based off of the algorithms in:
-# https://murch.one/wp-content/uploads/2016/11/erhardt2016coinselection.pdf
-
-
-# we use this to check if one of the coins exactly matches the target.
-def check_for_exact_match(coin_list: List[Coin], target: uint64) -> Optional[Coin]:
-    for coin in coin_list:
-        if coin.amount == target:
-            return coin
-    return None
-
-
-# amount of coins smaller than target, followed by a list of all valid spendable coins.
-# Coins must be sorted in descending amount order.
-def select_smallest_coin_over_target(target: uint128, sorted_coin_list: List[Coin]) -> Optional[Coin]:
-    if sorted_coin_list[0].amount < target:
-        return None
-    for coin in reversed(sorted_coin_list):
-        if coin.amount >= target:
-            return coin
-    assert False  # Should never reach here
-
-
-# we use this to find the set of coins which have total value closest to the target, but at least the target.
-# IMPORTANT: The coins have to be sorted in descending order or else this function will not work.
-def knapsack_coin_algorithm(
-    smaller_coins: List[Coin], target: uint128, max_coin_amount: int, max_num_coins: int, seed: bytes = b"knapsack seed"
-) -> Optional[Set[Coin]]:
-    best_set_sum = max_coin_amount
-    best_set_of_coins: Optional[Set[Coin]] = None
-    ran: random.Random = random.Random()
-    ran.seed(seed)
-    for i in range(1000):
-        # reset these variables every loop.
-        selected_coins: Set[Coin] = set()
-        selected_coins_sum = 0
-        n_pass = 0
-        target_reached = False
-        while n_pass < 2 and not target_reached:
-            for coin in smaller_coins:
-                # run 2 passes where the first pass may select a coin 50% of the time.
-                # the second pass runs to finish the set if the first pass didn't finish the set.
-                # this makes each trial random and increases the chance of getting a perfect set.
-                if (n_pass == 0 and bool(ran.getrandbits(1))) or (n_pass == 1 and coin not in selected_coins):
-                    if len(selected_coins) > max_num_coins:
-                        break
-                    selected_coins_sum += coin.amount
-                    selected_coins.add(coin)
-                    if selected_coins_sum == target:
-                        return selected_coins
-                    if selected_coins_sum > target:
-                        target_reached = True
-                        if selected_coins_sum < best_set_sum:
-                            best_set_of_coins = selected_coins.copy()
-                            best_set_sum = selected_coins_sum
-                            selected_coins_sum -= coin.amount
-                            selected_coins.remove(coin)
-            n_pass += 1
-    return best_set_of_coins
-
-
-# Adds up the largest coins in the list, resulting in the minimum number of selected coins. A solution
-# is guaranteed if and only if the sum(coins) >= target. Coins must be sorted in descending amount order.
-def sum_largest_coins(target: uint128, sorted_coins: List[Coin]) -> Optional[Set[Coin]]:
-    total_value = 0
-    selected_coins: Set[Coin] = set()
-    for coin in sorted_coins:
-        total_value += coin.amount
-        selected_coins.add(coin)
-        if total_value >= target:
-            return selected_coins
-    return None
+from __future__ import annotations
+
+import logging
+import random
+from typing import Dict, List, Optional, Set
+
+from chia.types.blockchain_format.coin import Coin
+from chia.types.blockchain_format.sized_bytes import bytes32
+from chia.util.ints import uint64, uint128
+from chia.wallet.wallet_coin_record import WalletCoinRecord
+
+
+async def select_coins(
+    spendable_amount: uint128,
+    max_coin_amount: uint64,
+    spendable_coins: List[WalletCoinRecord],
+    unconfirmed_removals: Dict[bytes32, Coin],
+    log: logging.Logger,
+    amount: uint128,
+    exclude: Optional[List[Coin]] = None,
+    min_coin_amount: Optional[uint64] = None,
+    excluded_coin_amounts: Optional[List[uint64]] = None,
+) -> Set[Coin]:
+    """
+    Returns a set of coins that can be used for generating a new transaction.
+    """
+    if exclude is None:
+        exclude = []
+    if min_coin_amount is None:
+        min_coin_amount = uint64(0)
+    if excluded_coin_amounts is None:
+        excluded_coin_amounts = []
+
+    if amount > spendable_amount:
+        error_msg = (
+            f"Can't select amount higher than our spendable balance.  Amount: {amount}, spendable: {spendable_amount}"
+        )
+        log.warning(error_msg)
+        raise ValueError(error_msg)
+
+    log.debug(f"About to select coins for amount {amount}")
+
+    max_num_coins = 500
+    sum_spendable_coins = 0
+    valid_spendable_coins: List[Coin] = []
+
+    for coin_record in spendable_coins:  # remove all the unconfirmed coins, excluded coins and dust.
+        if coin_record.coin.name() in unconfirmed_removals:
+            continue
+        if coin_record.coin in exclude:
+            continue
+        if coin_record.coin.amount < min_coin_amount or coin_record.coin.amount > max_coin_amount:
+            continue
+        if coin_record.coin.amount in excluded_coin_amounts:
+            continue
+        valid_spendable_coins.append(coin_record.coin)
+        sum_spendable_coins += coin_record.coin.amount
+
+    # This happens when we couldn't use one of the coins because it's already used
+    # but unconfirmed, and we are waiting for the change. (unconfirmed_additions)
+    if sum_spendable_coins < amount:
+        raise ValueError(
+            f"Transaction for {amount} is greater than spendable balance of {sum_spendable_coins}. "
+            "There may be other transactions pending or our minimum coin amount is too high."
+        )
+    if amount == 0 and sum_spendable_coins == 0:
+        raise ValueError(
+            "No coins available to spend, you can not create a coin with an amount of 0,"
+            " without already having coins."
+        )
+
+    # Sort the coins by amount
+    valid_spendable_coins.sort(reverse=True, key=lambda r: r.amount)
+
+    # check for exact 1 to 1 coin match.
+    exact_match_coin: Optional[Coin] = check_for_exact_match(valid_spendable_coins, uint64(amount))
+    if exact_match_coin:
+        log.debug(f"selected coin with an exact match: {exact_match_coin}")
+        return {exact_match_coin}
+
+    # Check for an exact match with all of the coins smaller than the amount.
+    # If we have more, smaller coins than the amount we run the next algorithm.
+    smaller_coin_sum = 0  # coins smaller than target.
+    smaller_coins: List[Coin] = []
+    for coin in valid_spendable_coins:
+        if coin.amount < amount:
+            smaller_coin_sum += coin.amount
+            smaller_coins.append(coin)
+    if smaller_coin_sum == amount and len(smaller_coins) < max_num_coins and amount != 0:
+        log.debug(f"Selected all smaller coins because they equate to an exact match of the target.: {smaller_coins}")
+        return set(smaller_coins)
+    elif smaller_coin_sum < amount:
+        smallest_coin: Optional[Coin] = select_smallest_coin_over_target(amount, valid_spendable_coins)
+        assert smallest_coin is not None  # Since we know we have enough, there must be a larger coin
+        log.debug(f"Selected closest greater coin: {smallest_coin.name()}")
+        return {smallest_coin}
+    elif smaller_coin_sum > amount:
+        coin_set: Optional[Set[Coin]] = knapsack_coin_algorithm(smaller_coins, amount, max_coin_amount, max_num_coins)
+        log.debug(f"Selected coins from knapsack algorithm: {coin_set}")
+        if coin_set is None:
+            coin_set = sum_largest_coins(amount, smaller_coins)
+            if coin_set is None or len(coin_set) > max_num_coins:
+                greater_coin = select_smallest_coin_over_target(amount, valid_spendable_coins)
+                if greater_coin is None:
+                    raise ValueError(
+                        f"Transaction of {amount} mojo would use more than "
+                        f"{max_num_coins} coins. Try sending a smaller amount"
+                    )
+                coin_set = {greater_coin}
+        return coin_set
+    else:
+        # if smaller_coin_sum == amount and (len(smaller_coins) >= max_num_coins or amount == 0)
+        potential_large_coin: Optional[Coin] = select_smallest_coin_over_target(amount, valid_spendable_coins)
+        if potential_large_coin is None:
+            raise ValueError("Too many coins are required to make this transaction")
+        log.debug(f"Resorted to selecting smallest coin over target due to dust.: {potential_large_coin}")
+        return {potential_large_coin}
+
+
+# These algorithms were based off of the algorithms in:
+# https://murch.one/wp-content/uploads/2016/11/erhardt2016coinselection.pdf
+
+
+# we use this to check if one of the coins exactly matches the target.
+def check_for_exact_match(coin_list: List[Coin], target: uint64) -> Optional[Coin]:
+    for coin in coin_list:
+        if coin.amount == target:
+            return coin
+    return None
+
+
+# amount of coins smaller than target, followed by a list of all valid spendable coins.
+# Coins must be sorted in descending amount order.
+def select_smallest_coin_over_target(target: uint128, sorted_coin_list: List[Coin]) -> Optional[Coin]:
+    if sorted_coin_list[0].amount < target:
+        return None
+    for coin in reversed(sorted_coin_list):
+        if coin.amount >= target:
+            return coin
+    assert False  # Should never reach here
+
+
+# we use this to find the set of coins which have total value closest to the target, but at least the target.
+# IMPORTANT: The coins have to be sorted in descending order or else this function will not work.
+def knapsack_coin_algorithm(
+    smaller_coins: List[Coin], target: uint128, max_coin_amount: int, max_num_coins: int, seed: bytes = b"knapsack seed"
+) -> Optional[Set[Coin]]:
+    best_set_sum = max_coin_amount
+    best_set_of_coins: Optional[Set[Coin]] = None
+    ran: random.Random = random.Random()
+    ran.seed(seed)
+    for i in range(1000):
+        # reset these variables every loop.
+        selected_coins: Set[Coin] = set()
+        selected_coins_sum = 0
+        n_pass = 0
+        target_reached = False
+        while n_pass < 2 and not target_reached:
+            for coin in smaller_coins:
+                # run 2 passes where the first pass may select a coin 50% of the time.
+                # the second pass runs to finish the set if the first pass didn't finish the set.
+                # this makes each trial random and increases the chance of getting a perfect set.
+                if (n_pass == 0 and bool(ran.getrandbits(1))) or (n_pass == 1 and coin not in selected_coins):
+                    if len(selected_coins) > max_num_coins:
+                        break
+                    selected_coins_sum += coin.amount
+                    selected_coins.add(coin)
+                    if selected_coins_sum == target:
+                        return selected_coins
+                    if selected_coins_sum > target:
+                        target_reached = True
+                        if selected_coins_sum < best_set_sum:
+                            best_set_of_coins = selected_coins.copy()
+                            best_set_sum = selected_coins_sum
+                            selected_coins_sum -= coin.amount
+                            selected_coins.remove(coin)
+            n_pass += 1
+    return best_set_of_coins
+
+
+# Adds up the largest coins in the list, resulting in the minimum number of selected coins. A solution
+# is guaranteed if and only if the sum(coins) >= target. Coins must be sorted in descending amount order.
+def sum_largest_coins(target: uint128, sorted_coins: List[Coin]) -> Optional[Set[Coin]]:
+    total_value = 0
+    selected_coins: Set[Coin] = set()
+    for coin in sorted_coins:
+        total_value += coin.amount
+        selected_coins.add(coin)
+        if total_value >= target:
+            return selected_coins
+    return None
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/db_wallet/db_wallet_puzzles.py` & `chia-blockchain-2.0.0b1/chia/wallet/db_wallet/db_wallet_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/derivation_record.py` & `chia-blockchain-2.0.0b1/chia/wallet/derivation_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/derive_keys.py` & `chia-blockchain-2.0.0b1/chia/wallet/derive_keys.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_info.py` & `chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_wallet.py` & `chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_wallet.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 import dataclasses
 import json
 import logging
 import re
 import time
 from secrets import token_bytes
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, cast
 
 from blspy import AugSchemeMPL, G1Element, G2Element
 
 from chia.full_node.full_node_api import FullNodeAPI
 from chia.protocols import wallet_protocol
 from chia.protocols.wallet_protocol import CoinState
 from chia.server.ws_connection import WSChiaConnection
@@ -25,14 +25,15 @@
 from chia.wallet.coin_selection import select_coins
 from chia.wallet.derivation_record import DerivationRecord
 from chia.wallet.derive_keys import master_sk_to_wallet_sk_unhardened
 from chia.wallet.did_wallet import did_wallet_puzzles
 from chia.wallet.did_wallet.did_info import DIDInfo
 from chia.wallet.did_wallet.did_wallet_puzzles import uncurry_innerpuz
 from chia.wallet.lineage_proof import LineageProof
+from chia.wallet.payment import Payment
 from chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle import (
     DEFAULT_HIDDEN_PUZZLE_HASH,
     calculate_synthetic_secret_key,
     puzzle_for_pk,
     puzzle_hash_for_pk,
 )
 from chia.wallet.singleton import (
@@ -48,14 +49,19 @@
 from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import CHIP_0002_SIGN_MESSAGE_PREFIX, Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 
 
 class DIDWallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("DIDWallet", None)
+
     wallet_state_manager: Any
     log: logging.Logger
     wallet_info: WalletInfo
     did_info: DIDInfo
     standard_wallet: Wallet
     base_puzzle_program: Optional[bytes]
     base_inner_puzzle_hash: Optional[bytes32]
@@ -576,21 +582,15 @@
         coin = coins.pop()
         new_inner_puzzle = await self.get_new_did_innerpuz()
         uncurried = did_wallet_puzzles.uncurry_innerpuz(new_inner_puzzle)
         assert uncurried is not None
         p2_puzzle = uncurried[0]
         # innerpuz solution is (mode, p2_solution)
         p2_solution = self.standard_wallet.make_solution(
-            primaries=[
-                {
-                    "puzzlehash": new_inner_puzzle.get_tree_hash(),
-                    "amount": uint64(coin.amount),
-                    "memos": [p2_puzzle.get_tree_hash()],
-                }
-            ],
+            primaries=[Payment(new_inner_puzzle.get_tree_hash(), uint64(coin.amount), [p2_puzzle.get_tree_hash()])],
             coin_announcements={coin.name()},
         )
         innersol: Program = Program.to([1, p2_solution])
         # full solution is (corehash parent_info my_amount innerpuz_reveal solution)
         innerpuz: Program = self.did_info.current_inner
 
         full_puzzle: Program = create_singleton_puzzle(
@@ -692,21 +692,15 @@
             new_puzhash,
             backup_ids,
             backup_required,
             self.did_info.origin_coin.name(),
             did_wallet_puzzles.metadata_to_program(json.loads(self.did_info.metadata)),
         )
         p2_solution = self.standard_wallet.make_solution(
-            primaries=[
-                {
-                    "puzzlehash": new_did_puzhash,
-                    "amount": uint64(coin.amount),
-                    "memos": [new_puzhash],
-                }
-            ],
+            primaries=[Payment(new_did_puzhash, uint64(coin.amount), [new_puzhash])],
             coin_announcements={coin.name()},
         )
         # Need to include backup list reveal here, even we are don't recover
         # innerpuz solution is
         # (mode, p2_solution)
         innersol: Program = Program.to([2, p2_solution])
         if with_recovery:
@@ -781,21 +775,15 @@
         # Quote message puzzle & solution
         if new_innerpuzzle is None:
             new_innerpuzzle = innerpuz
         uncurried = did_wallet_puzzles.uncurry_innerpuz(new_innerpuzzle)
         assert uncurried is not None
         p2_puzzle = uncurried[0]
         p2_solution = self.standard_wallet.make_solution(
-            primaries=[
-                {
-                    "puzzlehash": new_innerpuzzle.get_tree_hash(),
-                    "amount": uint64(coin.amount),
-                    "memos": [p2_puzzle.get_tree_hash()],
-                }
-            ],
+            primaries=[Payment(new_innerpuzzle.get_tree_hash(), uint64(coin.amount), [p2_puzzle.get_tree_hash()])],
             puzzle_announcements=puzzle_announcements,
             coin_announcements=coin_announcements,
         )
         # innerpuz solution is (mode p2_solution)
         innersol: Program = Program.to([1, p2_solution])
 
         # full solution is (corehash parent_info my_amount innerpuz_reveal solution)
@@ -898,20 +886,16 @@
         innerpuz: Program = self.did_info.current_inner
         uncurried = did_wallet_puzzles.uncurry_innerpuz(innerpuz)
         assert uncurried is not None
         p2_puzzle = uncurried[0]
         # innerpuz solution is (mode, p2_solution)
         p2_solution = self.standard_wallet.make_solution(
             primaries=[
-                {
-                    "puzzlehash": innerpuz.get_tree_hash(),
-                    "amount": uint64(coin.amount),
-                    "memos": [p2_puzzle.get_tree_hash()],
-                },
-                {"puzzlehash": innermessage, "amount": uint64(0), "memos": []},
+                Payment(innerpuz.get_tree_hash(), uint64(coin.amount), [p2_puzzle.get_tree_hash()]),
+                Payment(innermessage, uint64(0)),
             ],
         )
         innersol = Program.to([1, p2_solution])
 
         # full solution is (corehash parent_info my_amount innerpuz_reveal solution)
         full_puzzle: Program = create_singleton_puzzle(
             innerpuz,
@@ -1321,21 +1305,15 @@
     async def generate_eve_spend(self, coin: Coin, full_puzzle: Program, innerpuz: Program):
         assert self.did_info.origin_coin is not None
         uncurried = did_wallet_puzzles.uncurry_innerpuz(innerpuz)
         assert uncurried is not None
         p2_puzzle = uncurried[0]
         # innerpuz solution is (mode p2_solution)
         p2_solution = self.standard_wallet.make_solution(
-            primaries=[
-                {
-                    "puzzlehash": innerpuz.get_tree_hash(),
-                    "amount": uint64(coin.amount),
-                    "memos": [p2_puzzle.get_tree_hash()],
-                }
-            ]
+            primaries=[Payment(innerpuz.get_tree_hash(), uint64(coin.amount), [p2_puzzle.get_tree_hash()])]
         )
         innersol = Program.to([1, p2_solution])
         # full solution is (lineage_proof my_amount inner_solution)
         fullsol = Program.to(
             [
                 [self.did_info.origin_coin.parent_coin_info, self.did_info.origin_coin.amount],
                 coin.amount,
@@ -1478,13 +1456,7 @@
             True,
             metadata,
         )
         return did_info
 
     def require_derivation_paths(self) -> bool:
         return True
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = DIDWallet()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/did_wallet/did_wallet_puzzles.py` & `chia-blockchain-2.0.0b1/chia/wallet/did_wallet/did_wallet_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/driver_protocol.py` & `chia-blockchain-2.0.0b1/chia/wallet/driver_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/key_val_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/key_val_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/lineage_proof.py` & `chia-blockchain-2.0.0b1/chia/wallet/lineage_proof.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/metadata_outer_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/metadata_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_info.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_puzzles.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/nft_wallet.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/nft_wallet.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
 import dataclasses
 import json
 import logging
 import math
 import time
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple, Type, TypeVar
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, Type, TypeVar, cast
 
 from blspy import AugSchemeMPL, G1Element, G2Element
 from clvm.casts import int_from_bytes, int_to_bytes
 
 import chia.wallet.singleton
 from chia.protocols.wallet_protocol import CoinState
 from chia.server.ws_connection import WSChiaConnection
@@ -47,24 +47,29 @@
     Offer,
 )
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.uncurried_puzzle import uncurry_puzzle
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.transaction_type import TransactionType
 from chia.wallet.util.wallet_sync_utils import fetch_coin_spend
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash, WalletType
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import CHIP_0002_SIGN_MESSAGE_PREFIX, Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 from chia.wallet.wallet_nft_store import WalletNftStore
 
 _T_NFTWallet = TypeVar("_T_NFTWallet", bound="NFTWallet")
 
 
 class NFTWallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("NFTWallet", None)
+
     wallet_state_manager: Any
     log: logging.Logger
     wallet_info: WalletInfo
     nft_wallet_info: NFTWalletInfo
     standard_wallet: Wallet
     wallet_id: int
     nft_store: WalletNftStore
@@ -715,29 +720,25 @@
             coin_announcements_bytes = None
 
         if puzzle_announcements_to_consume is not None:
             puzzle_announcements_bytes: Optional[Set[bytes32]] = {a.name() for a in puzzle_announcements_to_consume}
         else:
             puzzle_announcements_bytes = None
 
-        primaries: List[AmountWithPuzzlehash] = []
-        for payment in payments:
-            primaries.append({"puzzlehash": payment.puzzle_hash, "amount": payment.amount, "memos": payment.memos})
-
         if fee > 0:
             announcement_to_make = nft_coin.coin.name()
             chia_tx = await self.standard_wallet.create_tandem_xch_tx(
                 fee, Announcement(nft_coin.coin.name(), announcement_to_make), reuse_puzhash=reuse_puzhash
             )
         else:
             announcement_to_make = None
             chia_tx = None
 
         innersol: Program = self.standard_wallet.make_solution(
-            primaries=primaries,
+            primaries=payments,
             coin_announcements=None if announcement_to_make is None else set((announcement_to_make,)),
             coin_announcements_to_assert=coin_announcements_bytes,
             puzzle_announcements_to_assert=puzzle_announcements_bytes,
         )
 
         unft = UncurriedNFT.uncurry(*nft_coin.full_puzzle.uncurry())
         assert unft is not None
@@ -945,23 +946,15 @@
                 # First, sending all the coins to the OFFER_MOD
                 if wallet.type() == WalletType.STANDARD_WALLET:
                     payments = royalty_payments[asset] if asset in royalty_payments else []
                     payment_sum = sum(p.amount for _, p in payments)
                     tx = await wallet.generate_signed_transaction(
                         abs(amount),
                         DESIRED_OFFER_MOD_HASH,
-                        primaries=[
-                            AmountWithPuzzlehash(
-                                {
-                                    "amount": uint64(payment_sum),
-                                    "puzzlehash": DESIRED_OFFER_MOD_HASH,
-                                    "memos": [],
-                                }
-                            )
-                        ]
+                        primaries=[Payment(DESIRED_OFFER_MOD_HASH, uint64(payment_sum))]
                         if payment_sum > 0 or old
                         else [],
                         fee=fee,
                         coins=offered_coins_by_asset[asset],
                         puzzle_announcements_to_consume=announcements_to_assert,
                     )
                     txs = [tx]
@@ -1025,15 +1018,14 @@
                             inner_royalty_sol = Program.to(
                                 (
                                     None,
                                     [
                                         Payment(
                                             DESIRED_OFFER_MOD_HASH,
                                             uint64(sum(p.amount for _, p in duplicate_payments)),
-                                            [],
                                         ).as_condition_args()
                                     ],
                                 )
                             ).cons(inner_royalty_sol)
 
                         if asset is None:  # xch offer
                             offer_puzzle = DESIRED_OFFER_MOD
@@ -1303,19 +1295,15 @@
             new_innerpuzhash = innerpuz.get_tree_hash()
             uncurried_did = did_wallet_puzzles.uncurry_innerpuz(innerpuz)
             assert uncurried_did is not None
             p2_puzzle = uncurried_did[0]
             new_p2_puzhash = p2_puzzle.get_tree_hash()
         assert new_p2_puzhash is not None
         # make the primaries for the DID spend
-        primaries = [
-            AmountWithPuzzlehash(
-                {"puzzlehash": new_innerpuzhash, "amount": uint64(did_coin.amount), "memos": [bytes(new_p2_puzhash)]}
-            )
-        ]
+        primaries = [Payment(new_innerpuzhash, uint64(did_coin.amount), [bytes(new_p2_puzhash)])]
 
         # Ensure we have an xch coin of high enough amount
         assert isinstance(fee, uint64)
         total_amount = len(metadata_list) + fee
         if xch_coins is None:
             xch_coins = await self.standard_wallet.select_coins(uint64(total_amount))
         assert len(xch_coins) > 0
@@ -1344,23 +1332,15 @@
         # Loop to create each intermediate coin, launcher, eve and (optional) transfer spends
         for mint_number in range(mint_number_start, mint_number_end):
             # Create  the puzzle, solution and coin spend for the intermediate launcher
             intermediate_launcher_puz = did_wallet_puzzles.INTERMEDIATE_LAUNCHER_MOD.curry(
                 chia.wallet.singleton.SINGLETON_LAUNCHER_PUZZLE_HASH, mint_number, mint_total
             )
             intermediate_launcher_ph = intermediate_launcher_puz.get_tree_hash()
-            primaries.append(
-                AmountWithPuzzlehash(
-                    {
-                        "puzzlehash": intermediate_launcher_ph,
-                        "amount": uint64(0),
-                        "memos": [intermediate_launcher_ph],
-                    }
-                )
-            )
+            primaries.append(Payment(intermediate_launcher_ph, uint64(0), [intermediate_launcher_ph]))
             intermediate_launcher_sol = Program.to([])
             intermediate_launcher_coin = Coin(did_coin.name(), intermediate_launcher_ph, uint64(0))
             intermediate_launcher_coin_spend = CoinSpend(
                 intermediate_launcher_coin, intermediate_launcher_puz, intermediate_launcher_sol
             )
             intermediate_coin_spends.append(intermediate_launcher_coin_spend)
 
@@ -1448,35 +1428,31 @@
         # We've now created all the intermediate, launcher, eve and transfer spends.
         # Create the xch spend to fund the minting.
         spend_value = sum([coin.amount for coin in xch_coins])
         change: uint64 = uint64(spend_value - total_amount)
         xch_spends = []
         if xch_change_ph is None:
             xch_change_ph = await self.standard_wallet.get_new_puzzlehash()
-        xch_primaries = [
-            AmountWithPuzzlehash({"puzzlehash": xch_change_ph, "amount": change, "memos": [xch_change_ph]})
-        ]
+        xch_payment = Payment(xch_change_ph, change, [xch_change_ph])
 
         first = True
         for xch_coin in xch_coins:
             puzzle: Program = await self.standard_wallet.puzzle_for_puzzle_hash(xch_coin.puzzle_hash)
             if first:
                 message_list: List[bytes32] = [c.name() for c in xch_coins]
-                message_list.append(
-                    Coin(xch_coin.name(), xch_primaries[0]["puzzlehash"], xch_primaries[0]["amount"]).name()
-                )
+                message_list.append(Coin(xch_coin.name(), xch_payment.puzzle_hash, xch_payment.amount).name())
                 message: bytes32 = std_hash(b"".join(message_list))
 
                 if len(xch_coins) > 1:
                     xch_announcement: Optional[Set[bytes]] = {message}
                 else:
                     xch_announcement = None
 
                 solution: Program = self.standard_wallet.make_solution(
-                    primaries=xch_primaries,
+                    primaries=[xch_payment],
                     fee=fee,
                     coin_announcements=xch_announcement,
                     coin_announcements_to_assert={Announcement(did_coin.name(), message).name()},
                 )
                 primary_announcement_hash = Announcement(xch_coin.name(), message).name()
                 # connect this coin assertion to the DID announcement
                 did_coin_announcement = {bytes(message)}
@@ -1598,23 +1574,15 @@
         # Loop to create each intermediate coin, launcher, eve and (optional) transfer spends
         for mint_number in range(mint_number_start, mint_number_end):
             # Create  the puzzle, solution and coin spend for the intermediate launcher
             intermediate_launcher_puz = nft_puzzles.INTERMEDIATE_LAUNCHER_MOD.curry(
                 nft_puzzles.LAUNCHER_PUZZLE_HASH, mint_number, mint_total
             )
             intermediate_launcher_ph = intermediate_launcher_puz.get_tree_hash()
-            primaries.append(
-                AmountWithPuzzlehash(
-                    {
-                        "puzzlehash": intermediate_launcher_ph,
-                        "amount": uint64(1),
-                        "memos": [intermediate_launcher_ph],
-                    }
-                )
-            )
+            primaries.append(Payment(intermediate_launcher_ph, uint64(1), [intermediate_launcher_ph]))
             intermediate_launcher_sol = Program.to([])
             intermediate_launcher_coin = Coin(funding_coin.name(), intermediate_launcher_ph, uint64(1))
             intermediate_launcher_coin_spend = CoinSpend(
                 intermediate_launcher_coin, intermediate_launcher_puz, intermediate_launcher_sol
             )
             intermediate_coin_spends.append(intermediate_launcher_coin_spend)
 
@@ -1697,35 +1665,31 @@
         # We've now created all the intermediate, launcher, eve and transfer spends.
         # Create the xch spend to fund the minting.
         spend_value = sum([coin.amount for coin in xch_coins])
         change: uint64 = uint64(spend_value - total_amount)
         xch_spends = []
         if xch_change_ph is None:
             xch_change_ph = await self.standard_wallet.get_new_puzzlehash()
-        xch_primaries = [
-            AmountWithPuzzlehash({"puzzlehash": xch_change_ph, "amount": change, "memos": [xch_change_ph]})
-        ]
+        xch_payment = Payment(xch_change_ph, change, [xch_change_ph])
 
         first = True
         for xch_coin in xch_coins:
             puzzle: Program = await self.standard_wallet.puzzle_for_puzzle_hash(xch_coin.puzzle_hash)
             if first:
                 message_list: List[bytes32] = [c.name() for c in xch_coins]
-                message_list.append(
-                    Coin(xch_coin.name(), xch_primaries[0]["puzzlehash"], xch_primaries[0]["amount"]).name()
-                )
+                message_list.append(Coin(xch_coin.name(), xch_payment.puzzle_hash, xch_payment.amount).name())
                 message: bytes32 = std_hash(b"".join(message_list))
 
                 if len(xch_coins) > 1:
                     xch_announcement: Optional[Set[bytes]] = {message}
                 else:
                     xch_announcement = None
 
                 solution: Program = self.standard_wallet.make_solution(
-                    primaries=xch_primaries + primaries,
+                    primaries=[xch_payment] + primaries,
                     fee=fee,
                     coin_announcements=xch_announcement if len(xch_coins) > 1 else None,
                     coin_announcements_to_assert=coin_announcements,
                     puzzle_announcements_to_assert=puzzle_assertions,
                 )
                 primary_announcement_hash = Announcement(xch_coin.name(), message).name()
                 first = False
@@ -1759,13 +1723,7 @@
         return False
 
     def puzzle_hash_for_pk(self, pubkey: G1Element) -> bytes32:
         raise RuntimeError("NFTWallet does not support puzzle_hash_for_pk")
 
     def get_name(self) -> str:
         return self.wallet_info.name
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = NFTWallet()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/ownership_outer_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/ownership_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/singleton_outer_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/singleton_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/transfer_program_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/transfer_program_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/nft_wallet/uncurry_nft.py` & `chia-blockchain-2.0.0b1/chia/wallet/nft_wallet/uncurry_nft.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/notification_manager.py` & `chia-blockchain-2.0.0b1/chia/wallet/notification_manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/notification_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/notification_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/outer_puzzles.py` & `chia-blockchain-2.0.0b1/chia/wallet/outer_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/payment.py` & `chia-blockchain-2.0.0b1/chia/wallet/payment.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from __future__ import annotations
 
-from dataclasses import dataclass
+from dataclasses import dataclass, field
 from typing import List
 
 from chia.types.blockchain_format.program import Program
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.util.ints import uint64
 
 
 # This class is supposed to correspond to a CREATE_COIN condition
 @dataclass(frozen=True)
 class Payment:
     puzzle_hash: bytes32
     amount: uint64
-    memos: List[bytes]
+    memos: List[bytes] = field(default_factory=list)
 
     def as_condition_args(self) -> List:
         return [self.puzzle_hash, self.amount, self.memos]
 
     def as_condition(self) -> Program:
         return Program.to([51, *self.as_condition_args()])
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzle_drivers.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzle_drivers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/block_program_zero.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/block_program_zero.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_truths.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_truths.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_v2.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_v2.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/cat_v2.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/cat_v2.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/chialisp_deserialisation.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/chialisp_deserialisation.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/chialisp_deserialisation.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/chialisp_deserialisation.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/condition_codes.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/condition_codes.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/create-lock-puzzlehash.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/create-lock-puzzlehash.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/curry-and-treehash.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/curry-and-treehash.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/curry.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/curry.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/delegated_tail.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/delegated_tail.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/deployed_puzzle_hashes.json` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/deployed_puzzle_hashes.json`

 * *Files 2% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9761904761904762%*

 * *Differences: {"'rom_bootstrap_generator2'": "'fae4b90d1f0a18bf9b7e5771da787dcc288e4ab5113d526841f54d32a5777db9'"}*

```diff
@@ -28,14 +28,15 @@
     "p2_parent": "b10ce2d0b18dcf8c21ddfaf55d9b9f0adcbf1e0beb55b1a8b9cad9bbff4e5f22",
     "p2_puzzle_hash": "13e29a62b42cd2ef72a79e4bacdc59733ca6310d65af83d349360d36ec622363",
     "p2_singleton": "40f828d8dd55603f4ff9fbf6b73271e904e69406982f4fbefae2c8dcceaf9834",
     "p2_singleton_or_delayed_puzhash": "adb656e0211e2ab4f42069a4c5efc80dc907e7062be08bf1628c8e5b6d94d25b",
     "pool_member_innerpuz": "a8490702e333ddd831a3ac9c22d0fa26d2bfeaf2d33608deb22f0e0123eb0494",
     "pool_waitingroom_innerpuz": "a317541a765bf8375e1c6e7c13503d0d2cbf56cacad5182befe947e78e2c0307",
     "rom_bootstrap_generator": "161bade1f822dcd62ab712ebaf30f3922a301e48a639e4295c5685f8bece7bd9",
+    "rom_bootstrap_generator2": "fae4b90d1f0a18bf9b7e5771da787dcc288e4ab5113d526841f54d32a5777db9",
     "settlement_payments": "cfbfdeed5c4ca2de3d0bf520b9cb4bb7743a359bd2e6a188d19ce7dffc21d3e7",
     "settlement_payments_old": "bae24162efbd568f89bc7a340798a6118df0189eb9e3f8697bcea27af99f8f79",
     "sha256tree_module": "eb4ead6576048c9d730b5ced00646c7fdd390649cfdf48a00de1590cdd8ee18f",
     "singleton_launcher": "eff07522495060c066f66f32acc2a77e3a3e737aca8baea4d1a64ea4cdc13da9",
     "singleton_top_layer": "24e044101e57b3d8c908b8a38ad57848afd29d3eecc439dba45f4412df4954fd",
     "singleton_top_layer_v1_1": "7faa3253bfddd1e0decb0906b2dc6247bbc4cf608f58345d173adb63e8b47c9f",
     "test_generator_deserialize": "52add794fc76e89512e4a063c383418bda084c8a78c74055abe80179e4a7832c",
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/did_innerpuz.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/did_innerpuz.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/did_innerpuz.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/did_innerpuz.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_coin_id.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_coin_id.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/genesis_by_puzzle_hash.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/graftroot_dl_offers.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/graftroot_dl_offers.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/graftroot_dl_offers.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/graftroot_dl_offers.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/json.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/json.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/load_clvm.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/load_clvm.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/merkle_utils.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/merkle_utils.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_default.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_default.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_metadata_updater_updateable.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_layer.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_layer.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_layer.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_layer.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_ownership_transfer_program_one_way_claim_with_royalties.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_state_layer.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_state_layer.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/nft_state_layer.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/nft_state_layer.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_conditions.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_conditions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_conditions.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_conditions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_delegated_puzzle_or_hidden_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_m_of_n_delegate_direct.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_m_of_n_delegate_direct.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_puzzle_hash.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_puzzle_hash.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/p2_singleton_or_delayed_puzhash.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_member_innerpuz.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_member_innerpuz.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_member_innerpuz.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_member_innerpuz.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/make_prefarm_ph.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/make_prefarm_ph.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/prefarm/spend_prefarm.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/prefarm/spend_prefarm.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/puzzle_utils.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/puzzle_utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 from __future__ import annotations
 
-from typing import List, Optional
+from typing import List
 
 from chia.types.condition_opcodes import ConditionOpcode
 
 
-def make_create_coin_condition(puzzle_hash, amount, memos: Optional[List[bytes]]) -> List:
-    if memos is not None:
-        return [ConditionOpcode.CREATE_COIN, puzzle_hash, amount, memos]
-    return [ConditionOpcode.CREATE_COIN, puzzle_hash, amount]
+def make_create_coin_condition(puzzle_hash, amount, memos: List[bytes]) -> List:
+    condition = [ConditionOpcode.CREATE_COIN, puzzle_hash, amount]
+    if len(memos) > 0:
+        condition.append(memos)
+    return condition
 
 
 def make_assert_aggsig_condition(pubkey):
     return [ConditionOpcode.AGG_SIG_UNSAFE, pubkey]
 
 
 def make_assert_my_coin_id_condition(coin_name):
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/rom_bootstrap_generator.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/rom_bootstrap_generator.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/rom_bootstrap_generator.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments_old.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments_old.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/settlement_payments_old.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/settlement_payments_old.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp.hex` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.clsp.hex`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_top_layer_v1_1.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_top_layer_v1_1.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/singleton_truths.clib` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/singleton_truths.clib`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/tails.py` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/tails.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,14 +11,15 @@
 from chia.wallet.cat_wallet.cat_utils import (
     SpendableCAT,
     construct_cat_puzzle,
     unsigned_spend_bundle_for_spendable_cats,
 )
 from chia.wallet.cat_wallet.lineage_store import CATLineageStore
 from chia.wallet.lineage_proof import LineageProof
+from chia.wallet.payment import Payment
 from chia.wallet.puzzles.cat_loader import CAT_MOD
 from chia.wallet.puzzles.load_clvm import load_clvm_maybe_recompile
 from chia.wallet.transaction_record import TransactionRecord
 
 GENESIS_BY_ID_MOD = load_clvm_maybe_recompile("genesis_by_coin_id.clsp")
 GENESIS_BY_PUZHASH_MOD = load_clvm_maybe_recompile("genesis_by_puzzle_hash.clsp")
 EVERYTHING_WITH_SIG_MOD = load_clvm_maybe_recompile("everything_with_signature.clsp")
@@ -87,17 +88,15 @@
         tx_record: TransactionRecord = await wallet.standard_wallet.generate_signed_transaction(
             amount, minted_cat_puzzle_hash, uint64(0), origin_id, coins
         )
         assert tx_record.spend_bundle is not None
 
         inner_solution = wallet.standard_wallet.add_condition_to_solution(
             Program.to([51, 0, -113, tail, []]),
-            wallet.standard_wallet.make_solution(
-                primaries=[{"puzzlehash": cat_inner.get_tree_hash(), "amount": amount}],
-            ),
+            wallet.standard_wallet.make_solution(primaries=[Payment(cat_inner.get_tree_hash(), amount)]),
         )
         eve_spend = unsigned_spend_bundle_for_spendable_cats(
             CAT_MOD,
             [
                 SpendableCAT(
                     list(filter(lambda a: a.amount == amount, tx_record.additions))[0],
                     tail.get_tree_hash(),
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp` & `chia-blockchain-2.0.0b1/chia/wallet/puzzles/test_multiple_generator_input_arguments.clsp`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/secret_key_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/secret_key_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/sign_coin_spends.py` & `chia-blockchain-2.0.0b1/chia/wallet/sign_coin_spends.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/singleton.py` & `chia-blockchain-2.0.0b1/chia/wallet/singleton.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/trade_manager.py` & `chia-blockchain-2.0.0b1/chia/wallet/trade_manager.py`

 * *Files 2% similar despite different names*

```diff
@@ -28,14 +28,15 @@
 from chia.wallet.trading.trade_status import TradeStatus
 from chia.wallet.trading.trade_store import TradeStore
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.util.transaction_type import TransactionType
 from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet import Wallet
 from chia.wallet.wallet_coin_record import WalletCoinRecord
+from chia.wallet.wallet_coin_store import HashFilter
 
 OFFER_MOD = load_clvm_maybe_recompile("settlement_payments.clsp")
 
 
 class TradeManager:
     """
     This class is a driver for creating and accepting settlement_payments.clsp style offers.
@@ -134,16 +135,18 @@
             return
         if coin_state.spent_height is None:
             self.log.error(f"Coin: {coin_state.coin}, has not been spent so trade can remain valid")
         # Then let's filter the offer into coins that WE offered
         offer = Offer.from_bytes(trade.offer)
         primary_coin_ids = [c.name() for c in offer.removals()]
         # TODO: Add `WalletCoinStore.get_coins`.
-        our_coin_records = await self.wallet_state_manager.coin_store.get_coin_records(primary_coin_ids)
-        our_primary_coins: List[Coin] = [cr.coin for cr in our_coin_records.values()]
+        result = await self.wallet_state_manager.coin_store.get_coin_records(
+            coin_id_filter=HashFilter.include(primary_coin_ids)
+        )
+        our_primary_coins: List[Coin] = [cr.coin for cr in result.records]
         our_additions: List[Coin] = list(
             filter(lambda c: offer.get_root_removal(c) in our_primary_coins, offer.additions())
         )
         our_addition_ids: List[bytes32] = [c.name() for c in our_additions]
 
         # And get all relevant coin states
         coin_states = await self.wallet_state_manager.wallet_node.get_coin_state(
@@ -190,15 +193,19 @@
             coins_of_interest.extend([c.name() for c in trade_offer.coins_of_interest])
 
         # TODO:
         #  - No need to get the coin records here, we are only interested in the coin_id on the call site.
         #  - The cast here is required for now because TradeManager.wallet_state_manager is hinted as Any.
         return cast(
             Dict[bytes32, WalletCoinRecord],
-            await self.wallet_state_manager.coin_store.get_coin_records(coins_of_interest),
+            (
+                await self.wallet_state_manager.coin_store.get_coin_records(
+                    coin_id_filter=HashFilter.include(coins_of_interest)
+                )
+            ).coin_id_to_record,
         )
 
     async def get_all_trades(self) -> List[TradeRecord]:
         all: List[TradeRecord] = await self.trade_store.get_all_trades()
         return all
 
     async def get_trade_by_id(self, trade_id: bytes32) -> Optional[TradeRecord]:
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/trade_record.py` & `chia-blockchain-2.0.0b1/chia/wallet/trade_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/trading/offer.py` & `chia-blockchain-2.0.0b1/chia/wallet/trading/offer.py`

 * *Files 1% similar despite different names*

```diff
@@ -455,15 +455,15 @@
 
             # Because of CAT supply laws, we must specify a place for the leftovers to go
             arbitrage_amount: int = total_arbitrage_amount[asset_id]
             all_payments: List[NotarizedPayment] = payments.copy()
             if arbitrage_amount > 0:
                 assert arbitrage_amount is not None
                 assert arbitrage_ph is not None
-                all_payments.append(NotarizedPayment(arbitrage_ph, uint64(arbitrage_amount), []))
+                all_payments.append(NotarizedPayment(arbitrage_ph, uint64(arbitrage_amount)))
 
             # Some assets need to know about siblings so we need to collect all spends first to be able to use them
             coin_to_spend_dict: Dict[Coin, CoinSpend] = {}
             coin_to_solution_dict: Dict[Coin, Program] = {}
             for coin in offered_coins:
                 parent_spend: CoinSpend = list(
                     filter(lambda cs: cs.coin.name() == coin.parent_coin_info, self._bundle.coin_spends)
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/trading/trade_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/trading/trade_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/transaction_record.py` & `chia-blockchain-2.0.0b1/chia/wallet/transaction_record.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/address_type.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/address_type.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/compute_hints.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/compute_hints.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/compute_memos.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/compute_memos.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/curry_and_treehash.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/curry_and_treehash.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/debug_spend_bundle.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/debug_spend_bundle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/json_clvm_utils.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/json_clvm_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/merkle_tree.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/merkle_tree.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/merkle_utils.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/merkle_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/new_peak_queue.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/new_peak_queue.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/peer_request_cache.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/peer_request_cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/puzzle_compression.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/puzzle_compression.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/wallet_sync_utils.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/wallet_sync_utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,29 +5,32 @@
 import random
 from typing import Any, Dict, List, Optional, Tuple, Union
 
 from chia_rs import compute_merkle_set_root
 
 from chia.consensus.constants import ConsensusConstants
 from chia.full_node.full_node_api import FullNodeAPI
-from chia.protocols import wallet_protocol
 from chia.protocols.shared_protocol import Capability
 from chia.protocols.wallet_protocol import (
     CoinState,
+    RegisterForCoinUpdates,
+    RegisterForPhUpdates,
     RejectAdditionsRequest,
     RejectBlockHeaders,
     RejectHeaderBlocks,
     RejectRemovalsRequest,
     RequestAdditions,
     RequestBlockHeaders,
     RequestHeaderBlocks,
+    RequestPuzzleSolution,
     RequestRemovals,
     RespondAdditions,
     RespondBlockHeaders,
     RespondHeaderBlocks,
+    RespondPuzzleSolution,
     RespondRemovals,
     RespondToCoinUpdates,
     RespondToPhUpdates,
 )
 from chia.server.ws_connection import WSChiaConnection
 from chia.types.blockchain_format.coin import Coin, hash_coin_ids
 from chia.types.blockchain_format.sized_bytes import bytes32
@@ -67,15 +70,15 @@
     puzzle_hashes: List[bytes32],
     peer: WSChiaConnection,
     min_height: int,
 ) -> List[CoinState]:
     """
     Tells full nodes that we are interested in puzzle hashes, and returns the response.
     """
-    msg = wallet_protocol.RegisterForPhUpdates(puzzle_hashes, uint32(max(min_height, uint32(0))))
+    msg = RegisterForPhUpdates(puzzle_hashes, uint32(max(min_height, uint32(0))))
     all_coins_state: Optional[RespondToPhUpdates] = await peer.call_api(
         FullNodeAPI.register_interest_in_puzzle_hash, msg, timeout=300
     )
     if all_coins_state is None:
         raise ValueError(f"None response from peer {peer.peer_info.host} for register_interest_in_puzzle_hash")
     return all_coins_state.coin_states
 
@@ -84,15 +87,15 @@
     coin_names: List[bytes32],
     peer: WSChiaConnection,
     min_height: int,
 ) -> List[CoinState]:
     """
     Tells full nodes that we are interested in coin ids, and returns the response.
     """
-    msg = wallet_protocol.RegisterForCoinUpdates(coin_names, uint32(max(0, min_height)))
+    msg = RegisterForCoinUpdates(coin_names, uint32(max(0, min_height)))
     all_coins_state: Optional[RespondToCoinUpdates] = await peer.call_api(
         FullNodeAPI.register_interest_in_coin, msg, timeout=300
     )
 
     if all_coins_state is None:
         raise ValueError(f"None response from peer {peer.peer_info.host} for register_interest_in_coin")
     return all_coins_state.coin_states
@@ -409,17 +412,17 @@
         assert res_h_blocks is not None
         blocks.extend([bl for bl in res_h_blocks.header_blocks if bl.height >= start])
     return blocks
 
 
 async def fetch_coin_spend(height: uint32, coin: Coin, peer: WSChiaConnection) -> CoinSpend:
     solution_response = await peer.call_api(
-        FullNodeAPI.request_puzzle_solution, wallet_protocol.RequestPuzzleSolution(coin.name(), height)
+        FullNodeAPI.request_puzzle_solution, RequestPuzzleSolution(coin.name(), height)
     )
-    if solution_response is None or not isinstance(solution_response, wallet_protocol.RespondPuzzleSolution):
+    if solution_response is None or not isinstance(solution_response, RespondPuzzleSolution):
         raise PeerRequestException(f"Was not able to obtain solution {solution_response}")
     assert solution_response.response.puzzle.get_tree_hash() == coin.puzzle_hash
     assert solution_response.response.coin_name == coin.name()
 
     return CoinSpend(
         coin,
         solution_response.response.puzzle,
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/util/wallet_types.py` & `chia-blockchain-2.0.0b1/chia/wallet/util/wallet_types.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,17 +1,15 @@
 from __future__ import annotations
 
 from dataclasses import dataclass
 from enum import IntEnum
-from typing import TYPE_CHECKING, List
+from typing import TYPE_CHECKING
 
-from typing_extensions import TypedDict
-
-from chia.types.blockchain_format.sized_bytes import bytes32
-from chia.util.ints import uint32, uint64
+from chia.util.ints import uint8, uint32
+from chia.util.streamable import Streamable, streamable
 
 if TYPE_CHECKING:
     from chia.wallet.wallet_protocol import WalletProtocol
 
 
 class WalletType(IntEnum):
     # Wallet Types
@@ -25,21 +23,28 @@
     DECENTRALIZED_ID = 8
     POOLING_WALLET = 9
     NFT = 10
     DATA_LAYER = 11
     DATA_LAYER_OFFER = 12
 
 
-class AmountWithPuzzlehash(TypedDict):
-    amount: uint64
-    puzzlehash: bytes32
-    memos: List[bytes]
+class CoinType(IntEnum):
+    NORMAL = 0
+    CLAWBACK = 1
 
 
 @dataclass(frozen=True)
 class WalletIdentifier:
     id: uint32
     type: WalletType
 
     @classmethod
     def create(cls, wallet: WalletProtocol) -> WalletIdentifier:
         return cls(wallet.id(), wallet.type())
+
+
+# TODO, Can be replaced with WalletIdentifier if we have streamable enums
+@streamable
+@dataclass(frozen=True)
+class StreamableWalletIdentifier(Streamable):
+    id: uint32
+    type: uint8
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 
 import logging
 import time
-from typing import TYPE_CHECKING, Any, Dict, List, Optional, Set, Tuple
+from typing import TYPE_CHECKING, Any, ClassVar, Dict, List, Optional, Set, Tuple, cast
 
 from blspy import AugSchemeMPL, G1Element, G2Element
 
 from chia.consensus.cost_calculator import NPCResult
 from chia.full_node.bundle_tools import simple_solution_generator
 from chia.full_node.mempool_check_conditions import get_name_puzzle_conditions
 from chia.types.announcement import Announcement
@@ -17,14 +17,15 @@
 from chia.types.coin_spend import CoinSpend
 from chia.types.generator_types import BlockGenerator
 from chia.types.spend_bundle import SpendBundle
 from chia.util.hash import std_hash
 from chia.util.ints import uint32, uint64, uint128
 from chia.wallet.coin_selection import select_coins
 from chia.wallet.derivation_record import DerivationRecord
+from chia.wallet.payment import Payment
 from chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle import (
     DEFAULT_HIDDEN_PUZZLE_HASH,
     calculate_synthetic_secret_key,
     puzzle_for_pk,
     puzzle_hash_for_pk,
     solution_for_conditions,
 )
@@ -39,26 +40,31 @@
     make_reserve_fee_condition,
 )
 from chia.wallet.secret_key_store import SecretKeyStore
 from chia.wallet.sign_coin_spends import sign_coin_spends
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.transaction_type import TransactionType
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash, WalletType
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_info import WalletInfo
 
 if TYPE_CHECKING:
     from chia.server.ws_connection import WSChiaConnection
 
 # https://github.com/Chia-Network/chips/blob/80e4611fe52b174bf1a0382b9dff73805b18b8c6/CHIPs/chip-0002.md#signmessage
 CHIP_0002_SIGN_MESSAGE_PREFIX = "Chia Signed Message"
 
 
 class Wallet:
+    if TYPE_CHECKING:
+        from chia.wallet.wallet_protocol import WalletProtocol
+
+        _protocol_check: ClassVar[WalletProtocol] = cast("Wallet", None)
+
     wallet_info: WalletInfo
     wallet_state_manager: Any
     log: logging.Logger
     wallet_id: uint32
     secret_key_store: SecretKeyStore
     cost_of_single_tx: Optional[int]
 
@@ -221,34 +227,28 @@
     async def get_new_puzzlehash(self) -> bytes32:
         puzhash = (await self.wallet_state_manager.get_unused_derivation_record(self.id())).puzzle_hash
         await self.hack_populate_secret_key_for_puzzle_hash(puzhash)
         return puzhash
 
     def make_solution(
         self,
-        primaries: List[AmountWithPuzzlehash],
+        primaries: List[Payment],
         min_time=0,
         me=None,
         coin_announcements: Optional[Set[bytes]] = None,
         coin_announcements_to_assert: Optional[Set[bytes32]] = None,
         puzzle_announcements: Optional[Set[bytes]] = None,
         puzzle_announcements_to_assert: Optional[Set[bytes32]] = None,
         fee=0,
     ) -> Program:
         assert fee >= 0
         condition_list = []
         if len(primaries) > 0:
             for primary in primaries:
-                if "memos" in primary:
-                    memos: Optional[List[bytes]] = primary["memos"]
-                    if memos is not None and len(memos) == 0:
-                        memos = None
-                else:
-                    memos = None
-                condition_list.append(make_create_coin_condition(primary["puzzlehash"], primary["amount"], memos))
+                condition_list.append(make_create_coin_condition(primary.puzzle_hash, primary.amount, primary.memos))
         if min_time > 0:
             condition_list.append(make_assert_absolute_seconds_exceeds_condition(min_time))
         if me:
             condition_list.append(make_assert_my_coin_id_condition(me["id"]))
         if fee:
             condition_list.append(make_reserve_fee_condition(fee))
         if coin_announcements:
@@ -311,15 +311,15 @@
     async def _generate_unsigned_transaction(
         self,
         amount: uint64,
         newpuzzlehash: bytes32,
         fee: uint64 = uint64(0),
         origin_id: bytes32 = None,
         coins: Set[Coin] = None,
-        primaries_input: Optional[List[AmountWithPuzzlehash]] = None,
+        primaries_input: Optional[List[Payment]] = None,
         ignore_max_send_amount: bool = False,
         coin_announcements_to_consume: Set[Announcement] = None,
         puzzle_announcements_to_consume: Set[Announcement] = None,
         memos: Optional[List[bytes]] = None,
         negative_change_allowed: bool = False,
         min_coin_amount: Optional[uint64] = None,
         max_coin_amount: Optional[uint64] = None,
@@ -327,23 +327,21 @@
         exclude_coins: Optional[Set[Coin]] = None,
         reuse_puzhash: Optional[bool] = None,
     ) -> List[CoinSpend]:
         """
         Generates a unsigned transaction in form of List(Puzzle, Solutions)
         Note: this must be called under a wallet state manager lock
         """
-        if primaries_input is None:
-            primaries: Optional[List[AmountWithPuzzlehash]] = None
-            total_amount = amount + fee
-        else:
-            primaries = primaries_input.copy()
-            primaries_amount = 0
-            for prim in primaries:
-                primaries_amount += prim["amount"]
-            total_amount = amount + fee + primaries_amount
+        primaries = []
+        if (primaries_input is None and amount > 0) or primaries_input is not None:
+            primaries.append(Payment(newpuzzlehash, amount, [] if memos is None else memos))
+        if primaries_input is not None:
+            primaries.extend(primaries_input)
+
+        total_amount = sum(primary.amount for primary in primaries) + fee
         if reuse_puzhash is None:
             reuse_puzhash_config = self.wallet_state_manager.config.get("reuse_public_key_for_change", None)
             if reuse_puzhash_config is None:
                 reuse_puzhash = False
             else:
                 reuse_puzhash = reuse_puzhash_config.get(
                     str(self.wallet_state_manager.wallet_node.logged_in_fingerprint), False
@@ -391,46 +389,35 @@
         else:
             puzzle_announcements_bytes = None
 
         spends: List[CoinSpend] = []
         primary_announcement_hash: Optional[bytes32] = None
 
         # Check for duplicates
-        if primaries is not None:
-            all_primaries_list = [(p["puzzlehash"], p["amount"]) for p in primaries] + [(newpuzzlehash, amount)]
-            if len(set(all_primaries_list)) != len(all_primaries_list):
-                raise ValueError("Cannot create two identical coins")
-        if memos is None:
-            memos = []
-        assert memos is not None
+        all_primaries_list = [(p.puzzle_hash, p.amount) for p in primaries]
+        if len(set(all_primaries_list)) != len(all_primaries_list):
+            raise ValueError("Cannot create two identical coins")
         for coin in coins:
             # Only one coin creates outputs
             if origin_id in (None, coin.name()):
                 origin_id = coin.name()
-                if primaries is None:
-                    if amount > 0:
-                        primaries = [{"puzzlehash": newpuzzlehash, "amount": uint64(amount), "memos": memos}]
-                    else:
-                        primaries = []
-                else:
-                    primaries.append({"puzzlehash": newpuzzlehash, "amount": uint64(amount), "memos": memos})
                 if change > 0:
                     if reuse_puzhash:
                         change_puzzle_hash: bytes32 = coin.puzzle_hash
                         for primary in primaries:
-                            if change_puzzle_hash == primary["puzzlehash"] and change == primary["amount"]:
+                            if change_puzzle_hash == primary.puzzle_hash and change == primary.amount:
                                 # We cannot create two coins has same id, create a new puzhash for the change:
                                 change_puzzle_hash = await self.get_new_puzzlehash()
                                 break
                     else:
                         change_puzzle_hash = await self.get_new_puzzlehash()
-                    primaries.append({"puzzlehash": change_puzzle_hash, "amount": uint64(change), "memos": []})
+                    primaries.append(Payment(change_puzzle_hash, uint64(change)))
                 message_list: List[bytes32] = [c.name() for c in coins]
                 for primary in primaries:
-                    message_list.append(Coin(coin.name(), primary["puzzlehash"], primary["amount"]).name())
+                    message_list.append(Coin(coin.name(), primary.puzzle_hash, primary.amount).name())
                 message: bytes32 = std_hash(b"".join(message_list))
                 puzzle: Program = await self.puzzle_for_puzzle_hash(coin.puzzle_hash)
                 solution: Program = self.make_solution(
                     primaries=primaries,
                     fee=fee,
                     coin_announcements={message},
                     coin_announcements_to_assert=coin_announcements_bytes,
@@ -488,15 +475,15 @@
     async def generate_signed_transaction(
         self,
         amount: uint64,
         puzzle_hash: bytes32,
         fee: uint64 = uint64(0),
         origin_id: bytes32 = None,
         coins: Set[Coin] = None,
-        primaries: Optional[List[AmountWithPuzzlehash]] = None,
+        primaries: Optional[List[Payment]] = None,
         ignore_max_send_amount: bool = False,
         coin_announcements_to_consume: Set[Announcement] = None,
         puzzle_announcements_to_consume: Set[Announcement] = None,
         memos: Optional[List[bytes]] = None,
         negative_change_allowed: bool = False,
         min_coin_amount: Optional[uint64] = None,
         max_coin_amount: Optional[uint64] = None,
@@ -508,15 +495,15 @@
         Use this to generate transaction.
         Note: this must be called under a wallet state manager lock
         The first output is (amount, puzzle_hash, memos), and the rest of the outputs are in primaries.
         """
         if primaries is None:
             non_change_amount = amount
         else:
-            non_change_amount = uint64(amount + sum(p["amount"] for p in primaries))
+            non_change_amount = uint64(amount + sum(p.amount for p in primaries))
 
         self.log.debug("Generating transaction for: %s %s %s", puzzle_hash, amount, repr(coins))
         transaction = await self._generate_unsigned_transaction(
             amount,
             puzzle_hash,
             fee,
             origin_id,
@@ -622,13 +609,7 @@
     async def coin_added(
         self, coin: Coin, height: uint32, peer: WSChiaConnection
     ) -> None:  # pylint: disable=used-before-assignment
         pass
 
     def get_name(self) -> str:
         return "Standard Wallet"
-
-
-if TYPE_CHECKING:
-    from chia.wallet.wallet_protocol import WalletProtocol
-
-    _dummy: WalletProtocol = Wallet()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_action.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_action.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_blockchain.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_blockchain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_info.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_info.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_interested_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_interested_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_nft_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_nft_store.py`

 * *Files 2% similar despite different names*

```diff
@@ -268,7 +268,12 @@
             result = await conn.execute(
                 "UPDATE users_nfts SET removed_height = null WHERE removed_height>?",
                 (height,),
             )
             if result.rowcount > 0:
                 return True
             return False
+
+    async def delete_wallet(self, wallet_id: uint32) -> None:
+        async with self.db_wrapper.writer_maybe_transaction() as conn:
+            cursor = await conn.execute("DELETE FROM users_nfts WHERE wallet_id=?", (wallet_id,))
+            await cursor.close()
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_node.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_node.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,18 +15,28 @@
 from blspy import AugSchemeMPL, G1Element, G2Element, PrivateKey
 from packaging.version import Version
 
 from chia.consensus.blockchain import AddBlockResult
 from chia.consensus.constants import ConsensusConstants
 from chia.daemon.keychain_proxy import KeychainProxy, connect_to_keychain_and_validate, wrap_local_keychain
 from chia.full_node.full_node_api import FullNodeAPI
-from chia.protocols import wallet_protocol
 from chia.protocols.full_node_protocol import RequestProofOfWeight, RespondProofOfWeight
 from chia.protocols.protocol_message_types import ProtocolMessageTypes
-from chia.protocols.wallet_protocol import CoinState, RespondBlockHeader, RespondToCoinUpdates
+from chia.protocols.wallet_protocol import (
+    CoinState,
+    CoinStateUpdate,
+    NewPeakWallet,
+    RegisterForCoinUpdates,
+    RequestBlockHeader,
+    RequestChildren,
+    RespondBlockHeader,
+    RespondChildren,
+    RespondToCoinUpdates,
+    SendTransaction,
+)
 from chia.rpc.rpc_server import StateChangedProtocol, default_get_connections
 from chia.server.node_discovery import WalletPeers
 from chia.server.outbound_message import Message, NodeType, make_msg
 from chia.server.peer_store_resolver import PeerStoreResolver
 from chia.server.server import ChiaServer
 from chia.server.ws_connection import WSChiaConnection
 from chia.types.blockchain_format.coin import Coin
@@ -464,18 +474,15 @@
         records: List[TransactionRecord] = await self.wallet_state_manager.tx_store.get_not_sent(
             include_accepted_txs=retry_accepted_txs
         )
 
         for record in records:
             if record.spend_bundle is None:
                 continue
-            msg = make_msg(
-                ProtocolMessageTypes.send_transaction,
-                wallet_protocol.SendTransaction(record.spend_bundle),
-            )
+            msg = make_msg(ProtocolMessageTypes.send_transaction, SendTransaction(record.spend_bundle))
             already_sent = set()
             for peer, status, _ in record.sent_to:
                 if status == MempoolInclusionStatus.SUCCESS.value:
                     already_sent.add(bytes32.from_hexstr(peer))
             messages.append((msg, already_sent))
 
         return messages
@@ -518,43 +525,43 @@
             peer: Optional[WSChiaConnection] = None
             item: Optional[NewPeakItem] = None
             try:
                 peer, item = None, None
                 item = await self.new_peak_queue.get()
                 assert item is not None
                 if item.item_type == NewPeakQueueTypes.COIN_ID_SUBSCRIPTION:
-                    self.log.debug("Pulled from queue: %s %s", item.item_type, item.data)
+                    self.log.debug("Pulled from queue: %s %s", item.item_type.name, item.data)
                     # Subscriptions are the highest priority, because we don't want to process any more peaks or
                     # state updates until we are sure that we subscribed to everything that we need to. Otherwise,
                     # we might not be able to process some state.
                     coin_ids: List[bytes32] = item.data
                     for peer in self.server.get_connections(NodeType.FULL_NODE):
                         coin_states: List[CoinState] = await subscribe_to_coin_updates(coin_ids, peer, uint32(0))
                         if len(coin_states) > 0:
                             async with self.wallet_state_manager.lock:
                                 await self.add_states_from_peer(coin_states, peer)
                 elif item.item_type == NewPeakQueueTypes.PUZZLE_HASH_SUBSCRIPTION:
-                    self.log.debug("Pulled from queue: %s %s", item.item_type, item.data)
+                    self.log.debug("Pulled from queue: %s %s", item.item_type.name, item.data)
                     puzzle_hashes: List[bytes32] = item.data
                     for peer in self.server.get_connections(NodeType.FULL_NODE):
                         # Puzzle hash subscription
                         coin_states = await subscribe_to_phs(puzzle_hashes, peer, uint32(0))
                         if len(coin_states) > 0:
                             async with self.wallet_state_manager.lock:
                                 await self.add_states_from_peer(coin_states, peer)
                 elif item.item_type == NewPeakQueueTypes.FULL_NODE_STATE_UPDATED:
                     # Note: this can take a while when we have a lot of transactions. We want to process these
                     # before new_peaks, since new_peak_wallet requires that we first obtain the state for that peak.
-                    self.log.debug("Pulled from queue: %s %s", item.item_type, item.data[0])
+                    self.log.debug("Pulled from queue: %s %s", item.item_type.name, item.data[0])
                     coin_state_update = item.data[0]
                     peer = item.data[1]
                     assert peer is not None
                     await self.state_update_received(coin_state_update, peer)
                 elif item.item_type == NewPeakQueueTypes.NEW_PEAK_WALLET:
-                    self.log.debug("Pulled from queue: %s %s", item.item_type, item.data[0])
+                    self.log.debug("Pulled from queue: %s %s", item.item_type.name, item.data[0])
                     # This can take a VERY long time, because it might trigger a long sync. It is OK if we miss some
                     # subscriptions or state updates, since all subscriptions and state updates will be handled by
                     # long_sync (up to the target height).
                     new_peak = item.data[0]
                     peer = item.data[1]
                     assert peer is not None
                     await self.new_peak_wallet(new_peak, peer)
@@ -928,15 +935,15 @@
             (rc_height, rc_hh) for rc_height, rc_hh in self.race_cache_hashes if height - delete_threshold < rc_height
         ]
 
         if header_hash not in self.race_cache:
             self.race_cache[header_hash] = set()
         self.race_cache[header_hash].add(coin_state)
 
-    async def state_update_received(self, request: wallet_protocol.CoinStateUpdate, peer: WSChiaConnection) -> None:
+    async def state_update_received(self, request: CoinStateUpdate, peer: WSChiaConnection) -> None:
         # This gets called every time there is a new coin or puzzle hash change in the DB
         # that is of interest to this wallet. It is not guaranteed to come for every height. This message is guaranteed
         # to come before the corresponding new_peak for each height. We handle this differently for trusted and
         # untrusted peers. For trusted, we always process the state, and we process reorgs as well.
         for coin in request.items:
             self.log.info(f"request coin: {coin.coin.name().hex()}{coin}")
 
@@ -1002,27 +1009,27 @@
 
             assert last_tx_block.foliage_transaction_block is not None
             self.get_cache_for_peer(peer).add_to_blocks(last_tx_block)
             return last_tx_block.foliage_transaction_block.timestamp
 
         raise PeerRequestException("Error fetching timestamp from all peers")
 
-    async def new_peak_wallet(self, new_peak: wallet_protocol.NewPeakWallet, peer: WSChiaConnection) -> None:
+    async def new_peak_wallet(self, new_peak: NewPeakWallet, peer: WSChiaConnection) -> None:
         if self._wallet_state_manager is None:
             # When logging out of wallet
             self.log.debug("state manager is None (shutdown)")
             return
         trusted: bool = self.is_trusted(peer)
         peak_hb: Optional[HeaderBlock] = await self.wallet_state_manager.blockchain.get_peak_block()
         if peak_hb is not None and new_peak.weight < peak_hb.weight:
             # Discards old blocks, but accepts blocks that are equal in weight to peak
             self.log.debug("skip block with lower weight.")
             return
 
-        request = wallet_protocol.RequestBlockHeader(new_peak.height)
+        request = RequestBlockHeader(new_peak.height)
         response: Optional[RespondBlockHeader] = await peer.call_api(FullNodeAPI.request_block_header, request)
         if response is None:
             self.log.warning(f"Peer {peer.get_peer_info()} did not respond in time.")
             await peer.close(120)
             return
 
         new_peak_hb: HeaderBlock = response.header_block
@@ -1178,15 +1185,15 @@
         # Fetch blocks backwards until we hit the one that we have,
         # then complete them with additions / removals going forward
         fork_height = 0
         if self.wallet_state_manager.blockchain.contains_block(header_block.prev_header_hash):
             fork_height = header_block.height - 1
 
         while not self.wallet_state_manager.blockchain.contains_block(top.prev_header_hash) and top.height > 0:
-            request_prev = wallet_protocol.RequestBlockHeader(uint32(top.height - 1))
+            request_prev = RequestBlockHeader(uint32(top.height - 1))
             response_prev: Optional[RespondBlockHeader] = await peer.call_api(
                 FullNodeAPI.request_block_header, request_prev
             )
             if response_prev is None or not isinstance(response_prev, RespondBlockHeader):
                 raise RuntimeError("bad block header response from peer while syncing")
             prev_head = response_prev.header_block
             blocks.append(prev_head)
@@ -1555,17 +1562,17 @@
         for reward_chain_hash, height in blocks_to_cache:
             peer_request_cache.add_to_blocks_validated(reward_chain_hash, height)
         return True
 
     async def get_coin_state(
         self, coin_names: List[bytes32], peer: WSChiaConnection, fork_height: Optional[uint32] = None
     ) -> List[CoinState]:
-        msg = wallet_protocol.RegisterForCoinUpdates(coin_names, uint32(0))
+        msg = RegisterForCoinUpdates(coin_names, uint32(0))
         coin_state: Optional[RespondToCoinUpdates] = await peer.call_api(FullNodeAPI.register_interest_in_coin, msg)
-        if coin_state is None or not isinstance(coin_state, wallet_protocol.RespondToCoinUpdates):
+        if coin_state is None or not isinstance(coin_state, RespondToCoinUpdates):
             raise PeerRequestException(f"Was not able to get states for {coin_names}")
 
         if not self.is_trusted(peer):
             valid_list = []
             for coin in coin_state.coin_states:
                 valid = await self.validate_received_state_from_peer(
                     coin, peer, self.get_cache_for_peer(peer), fork_height
@@ -1575,36 +1582,33 @@
             return valid_list
 
         return coin_state.coin_states
 
     async def fetch_children(
         self, coin_name: bytes32, peer: WSChiaConnection, fork_height: Optional[uint32] = None
     ) -> List[CoinState]:
-        response: Optional[wallet_protocol.RespondChildren] = await peer.call_api(
-            FullNodeAPI.request_children, wallet_protocol.RequestChildren(coin_name)
+        response: Optional[RespondChildren] = await peer.call_api(
+            FullNodeAPI.request_children, RequestChildren(coin_name)
         )
-        if response is None or not isinstance(response, wallet_protocol.RespondChildren):
+        if response is None or not isinstance(response, RespondChildren):
             raise PeerRequestException(f"Was not able to obtain children {response}")
 
         if not self.is_trusted(peer):
             request_cache = self.get_cache_for_peer(peer)
             validated = []
             for state in response.coin_states:
                 valid = await self.validate_received_state_from_peer(state, peer, request_cache, fork_height)
                 if valid:
                     validated.append(state)
             return validated
         return response.coin_states
 
     # For RPC only. You should use wallet_state_manager.add_pending_transaction for normal wallet business.
     async def push_tx(self, spend_bundle: SpendBundle) -> None:
-        msg = make_msg(
-            ProtocolMessageTypes.send_transaction,
-            wallet_protocol.SendTransaction(spend_bundle),
-        )
+        msg = make_msg(ProtocolMessageTypes.send_transaction, SendTransaction(spend_bundle))
         full_nodes = self.server.get_connections(NodeType.FULL_NODE)
         for peer in full_nodes:
             await peer.send_message(msg)
 
     async def _update_balance_cache(self, wallet_id: uint32) -> None:
         assert self.wallet_state_manager.lock.locked(), "WalletStateManager.lock required"
         wallet = self.wallet_state_manager.wallets[wallet_id]
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_node_api.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_node_api.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_pool_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_pool_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_protocol.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_puzzle_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_puzzle_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_retry_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_retry_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_state_manager.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_state_manager.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,28 +4,40 @@
 import logging
 import multiprocessing.context
 import time
 import traceback
 from contextlib import asynccontextmanager
 from pathlib import Path
 from secrets import token_bytes
-from typing import Any, AsyncIterator, Callable, Dict, Iterator, List, Optional, Set, Tuple, Type, TypeVar
+from typing import (
+    TYPE_CHECKING,
+    Any,
+    AsyncIterator,
+    Callable,
+    Dict,
+    Iterator,
+    List,
+    Optional,
+    Set,
+    Tuple,
+    Type,
+    TypeVar,
+)
 
 import aiosqlite
 from blspy import G1Element, PrivateKey
 
 from chia.consensus.block_rewards import calculate_base_farmer_reward, calculate_pool_reward
 from chia.consensus.coinbase import farmer_parent_id, pool_parent_id
 from chia.consensus.constants import ConsensusConstants
 from chia.data_layer.data_layer_wallet import DataLayerWallet
 from chia.data_layer.dl_wallet_store import DataLayerStore
 from chia.pools.pool_puzzles import SINGLETON_LAUNCHER_HASH, solution_to_pool_state
 from chia.pools.pool_wallet import PoolWallet
-from chia.protocols import wallet_protocol
-from chia.protocols.wallet_protocol import CoinState
+from chia.protocols.wallet_protocol import CoinState, NewPeakWallet
 from chia.rpc.rpc_server import StateChangedProtocol
 from chia.server.outbound_message import NodeType
 from chia.server.server import ChiaServer
 from chia.server.ws_connection import WSChiaConnection
 from chia.types.blockchain_format.coin import Coin
 from chia.types.blockchain_format.program import Program
 from chia.types.blockchain_format.sized_bytes import bytes32
@@ -75,31 +87,37 @@
     fetch_coin_spend_for_coin_state,
     last_change_height_cs,
 )
 from chia.wallet.util.wallet_types import WalletIdentifier, WalletType
 from chia.wallet.wallet import Wallet
 from chia.wallet.wallet_blockchain import WalletBlockchain
 from chia.wallet.wallet_coin_record import WalletCoinRecord
-from chia.wallet.wallet_coin_store import WalletCoinStore
+from chia.wallet.wallet_coin_store import HashFilter, WalletCoinStore
 from chia.wallet.wallet_info import WalletInfo
 from chia.wallet.wallet_interested_store import WalletInterestedStore
 from chia.wallet.wallet_nft_store import WalletNftStore
 from chia.wallet.wallet_pool_store import WalletPoolStore
 from chia.wallet.wallet_protocol import WalletProtocol
 from chia.wallet.wallet_puzzle_store import WalletPuzzleStore
 from chia.wallet.wallet_retry_store import WalletRetryStore
 from chia.wallet.wallet_transaction_store import WalletTransactionStore
 from chia.wallet.wallet_user_store import WalletUserStore
 
 TWalletType = TypeVar("TWalletType", bound=WalletProtocol)
 
+if TYPE_CHECKING:
+    from chia.wallet.wallet_node import WalletNode
+
+
+PendingTxCallback = Callable[[], None]
+
 
 class WalletStateManager:
     constants: ConsensusConstants
-    config: Dict
+    config: Dict[str, Any]
     tx_store: WalletTransactionStore
     puzzle_store: WalletPuzzleStore
     user_store: WalletUserStore
     nft_store: WalletNftStore
     basic_store: KeyValStore
 
     # Makes sure only one asyncio thread is changing the blockchain state at one time
@@ -107,15 +125,15 @@
 
     log: logging.Logger
 
     # TODO Don't allow user to send tx until wallet is synced
     _sync_target: Optional[uint32]
 
     state_changed_callback: Optional[StateChangedProtocol] = None
-    pending_tx_callback: Optional[Callable]
+    pending_tx_callback: Optional[PendingTxCallback]
     db_path: Path
     db_wrapper: DBWrapper2
 
     main_wallet: Wallet
     wallets: Dict[uint32, WalletProtocol]
     private_key: PrivateKey
 
@@ -124,38 +142,37 @@
     blockchain: WalletBlockchain
     coin_store: WalletCoinStore
     interested_store: WalletInterestedStore
     retry_store: WalletRetryStore
     multiprocessing_context: multiprocessing.context.BaseContext
     server: ChiaServer
     root_path: Path
-    wallet_node: Any
+    wallet_node: WalletNode
     pool_store: WalletPoolStore
     dl_store: DataLayerStore
     default_cats: Dict[str, Any]
     asset_to_wallet_map: Dict[AssetType, Any]
     initial_num_public_keys: int
 
     @staticmethod
     async def create(
         private_key: PrivateKey,
-        config: Dict,
+        config: Dict[str, Any],
         db_path: Path,
         constants: ConsensusConstants,
         server: ChiaServer,
         root_path: Path,
-        wallet_node,
-        name: str = None,
-    ):
+        wallet_node: WalletNode,
+    ) -> WalletStateManager:
         self = WalletStateManager()
         self.config = config
         self.constants = constants
         self.server = server
         self.root_path = root_path
-        self.log = logging.getLogger(name if name else __name__)
+        self.log = logging.getLogger(__name__)
         self.lock = asyncio.Lock()
         self.log.debug(f"Starting in db path: {db_path}")
 
         sql_log_path: Optional[Path] = None
         if self.config.get("log_sqlite_cmds", False):
             sql_log_path = path_from_root(self.root_path, "log/wallet_sql.log")
             self.log.info(f"logging SQL commands to {sql_log_path}")
@@ -266,18 +283,18 @@
             )
 
         return wallet
 
     async def create_more_puzzle_hashes(
         self,
         from_zero: bool = False,
-        mark_existing_as_used=True,
+        mark_existing_as_used: bool = True,
         up_to_index: Optional[uint32] = None,
         num_additional_phs: Optional[int] = None,
-    ):
+    ) -> None:
         """
         For all wallets in the user store, generates the first few puzzle hashes so
         that we can restore the wallet from only the private keys.
         """
         targets = list(self.wallets.keys())
         self.log.debug("Target wallets to generate puzzle hashes for: %s", repr(targets))
         unused: Optional[uint32] = (
@@ -376,44 +393,44 @@
                 )
                 self.state_changed("new_derivation_index", data_object={"index": derivation_paths[-1].index})
         # By default, we'll mark previously generated unused puzzle hashes as used if we have new paths
         if mark_existing_as_used and unused > 0 and new_paths:
             self.log.info(f"Updating last used derivation index: {unused - 1}")
             await self.puzzle_store.set_used_up_to(uint32(unused - 1))
 
-    async def update_wallet_puzzle_hashes(self, wallet_id):
+    async def update_wallet_puzzle_hashes(self, wallet_id: uint32) -> None:
         derivation_paths: List[DerivationRecord] = []
         target_wallet = self.wallets[wallet_id]
         last: Optional[uint32] = await self.puzzle_store.get_last_derivation_path_for_wallet(wallet_id)
         unused: Optional[uint32] = await self.puzzle_store.get_unused_derivation_path()
         if unused is None:
             # This handles the case where the database has entries but they have all been used
             unused = await self.puzzle_store.get_last_derivation_path()
             if unused is None:
                 # This handles the case where the database is empty
                 unused = uint32(0)
         if last is not None:
             for index in range(unused, last):
                 # Since DID are not released yet we can assume they are only using unhardened keys derivation
                 pubkey: G1Element = self.get_public_key_unhardened(uint32(index))
-                puzzlehash: Optional[bytes32] = target_wallet.puzzle_hash_for_pk(pubkey)
+                puzzlehash = target_wallet.puzzle_hash_for_pk(pubkey)
                 self.log.info(f"Generating public key at index {index} puzzle hash {puzzlehash.hex()}")
                 derivation_paths.append(
                     DerivationRecord(
                         uint32(index),
                         puzzlehash,
                         pubkey,
-                        target_wallet.wallet_info.type,
+                        WalletType(target_wallet.wallet_info.type),
                         uint32(target_wallet.wallet_info.id),
                         False,
                     )
                 )
             await self.puzzle_store.add_derivation_paths(derivation_paths)
 
-    async def get_unused_derivation_record(self, wallet_id: uint32, *, hardened=False) -> DerivationRecord:
+    async def get_unused_derivation_record(self, wallet_id: uint32, *, hardened: bool = False) -> DerivationRecord:
         """
         Creates a puzzle hash for the given wallet, and then makes more puzzle hashes
         for every wallet to ensure we always have more in the database. Never reusue the
         same public key more than once (for privacy).
         """
         async with self.puzzle_store.lock:
             # If we have no unused public keys, we will create new ones
@@ -443,27 +460,29 @@
         async with self.puzzle_store.lock:
             # If we have no unused public keys, we will create new ones
             current: Optional[DerivationRecord] = await self.puzzle_store.get_current_derivation_record_for_wallet(
                 wallet_id
             )
             return current
 
-    def set_callback(self, callback: Callable):
+    def set_callback(self, callback: StateChangedProtocol) -> None:
         """
         Callback to be called when the state of the wallet changes.
         """
         self.state_changed_callback = callback
 
-    def set_pending_callback(self, callback: Callable):
+    def set_pending_callback(self, callback: PendingTxCallback) -> None:
         """
         Callback to be called when new pending transaction enters the store
         """
         self.pending_tx_callback = callback
 
-    def state_changed(self, state: str, wallet_id: Optional[int] = None, data_object: Optional[Dict[str, Any]] = None):
+    def state_changed(
+        self, state: str, wallet_id: Optional[int] = None, data_object: Optional[Dict[str, Any]] = None
+    ) -> None:
         """
         Calls the callback if it's present.
         """
         if self.state_changed_callback is None:
             return None
         change_data: Dict[str, Any] = {"state": state}
         if wallet_id is not None:
@@ -532,15 +551,17 @@
                     self.log.debug(
                         f"set_sync_mode exit - range: {start_height}-{target_height}, "
                         f"get_finished_sync_up_to: {await self.blockchain.get_finished_sync_up_to()}, "
                         f"seconds: {time.time() - start_time}"
                     )
                 self._sync_target = None
 
-    async def get_confirmed_spendable_balance_for_wallet(self, wallet_id: int, unspent_records=None) -> uint128:
+    async def get_confirmed_spendable_balance_for_wallet(
+        self, wallet_id: int, unspent_records: Optional[Set[WalletCoinRecord]] = None
+    ) -> uint128:
         """
         Returns the balance amount of all coins that are spendable.
         """
 
         spendable: Set[WalletCoinRecord] = await self.get_spendable_coins_for_wallet(wallet_id, unspent_records)
 
         spendable_amount: uint128 = uint128(0)
@@ -912,15 +933,15 @@
         ] = await self.puzzle_store.get_derivation_record_for_puzzle_hash(old_p2_puzhash)
         if new_derivation_record is None and old_derivation_record is None:
             self.log.debug(
                 "Cannot find a P2 puzzle hash for NFT:%s, this NFT belongs to others.",
                 uncurried_nft.singleton_launcher_id.hex(),
             )
             return wallet_identifier
-        for nft_wallet in self.wallets.copy().values():
+        for nft_wallet in self.wallets.values():
             if not isinstance(nft_wallet, NFTWallet):
                 continue
             if nft_wallet.nft_wallet_info.did_id == old_did_id and old_derivation_record is not None:
                 self.log.info(
                     "Removing old NFT, NFT_ID:%s, DID_ID:%s",
                     uncurried_nft.singleton_launcher_id.hex(),
                     old_did_id,
@@ -975,24 +996,24 @@
             if last_change_height < curr_h:
                 raise ValueError("Input coin_states is not sorted properly")
             curr_h = last_change_height
 
         trade_removals = await self.trade_manager.get_coins_of_interest()
         all_unconfirmed: List[TransactionRecord] = await self.tx_store.get_all_unconfirmed()
         used_up_to = -1
-        ph_to_index_cache: LRUCache = LRUCache(100)
+        ph_to_index_cache: LRUCache[bytes32, uint32] = LRUCache(100)
 
         coin_names = [coin_state.coin.name() for coin_state in coin_states]
-        local_records = await self.coin_store.get_coin_records(coin_names)
+        local_records = await self.coin_store.get_coin_records(coin_id_filter=HashFilter.include(coin_names))
 
         for coin_name, coin_state in zip(coin_names, coin_states):
             if peer.closed:
                 raise ConnectionError("Connection closed")
             self.log.debug("Add coin state: %s: %s", coin_name, coin_state)
-            local_record = local_records.get(coin_name)
+            local_record = local_records.coin_id_to_record.get(coin_name)
             rollback_wallets = None
             try:
                 async with self.db_wrapper.writer():
                     rollback_wallets = self.wallets.copy()  # Shallow copy of wallets if writer rolls back the db
                     # This only succeeds if we don't raise out of the transaction
                     await self.retry_store.remove_state(coin_state)
 
@@ -1096,15 +1117,15 @@
                             ):
                                 change = True
                             else:
                                 change = False
 
                             if not change:
                                 created_timestamp = await self.wallet_node.get_timestamp_for_height(
-                                    coin_state.created_height
+                                    uint32(coin_state.created_height)
                                 )
                                 tx_record = TransactionRecord(
                                     confirmed_at_height=uint32(coin_state.created_height),
                                     created_at_time=uint64(created_timestamp),
                                     to_puzzle_hash=(
                                         await self.convert_puzzle_hash(
                                             wallet_identifier.id, coin_state.coin.puzzle_hash
@@ -1133,23 +1154,26 @@
                                 to_puzzle_hash = None
                                 # Find coin that doesn't belong to us
                                 amount = 0
                                 for coin in additions:
                                     derivation_record = await self.puzzle_store.get_derivation_record_for_puzzle_hash(
                                         coin.puzzle_hash
                                     )
-                                    if derivation_record is None:
+                                    if derivation_record is None:  # not change
                                         to_puzzle_hash = coin.puzzle_hash
                                         amount += coin.amount
+                                    elif wallet_identifier.type == WalletType.CAT:
+                                        # We subscribe to change for CATs since they didn't hint previously
+                                        await self.add_interested_coin_ids([coin.name()])
 
                                 if to_puzzle_hash is None:
                                     to_puzzle_hash = additions[0].puzzle_hash
 
                                 spent_timestamp = await self.wallet_node.get_timestamp_for_height(
-                                    coin_state.spent_height
+                                    uint32(coin_state.spent_height)
                                 )
 
                                 # Reorg rollback adds reorged transactions so it's possible there is tx_record already
                                 # Even though we are just adding coin record to the db (after reorg)
                                 tx_records: List[TransactionRecord] = []
                                 for out_tx_record in all_unconfirmed:
                                     for rem_coin in out_tx_record.removals:
@@ -1459,52 +1483,53 @@
                 type=uint32(tx_type),
                 name=coin_name,
                 memos=[],
             )
             if tx_record.amount > 0:
                 await self.tx_store.add_transaction_record(tx_record)
 
+        # We only add normal coins here
         coin_record: WalletCoinRecord = WalletCoinRecord(
             coin, height, uint32(0), False, coinbase, wallet_type, wallet_id
         )
         await self.coin_store.add_coin_record(coin_record, coin_name)
 
         await self.wallets[wallet_id].coin_added(coin, height, peer)
 
         await self.create_more_puzzle_hashes()
 
-    async def add_pending_transaction(self, tx_record: TransactionRecord):
+    async def add_pending_transaction(self, tx_record: TransactionRecord) -> None:
         """
         Called from wallet before new transaction is sent to the full_node
         """
         # Wallet node will use this queue to retry sending this transaction until full nodes receives it
         await self.tx_store.add_transaction_record(tx_record)
         all_coins_names = []
         all_coins_names.extend([coin.name() for coin in tx_record.additions])
         all_coins_names.extend([coin.name() for coin in tx_record.removals])
 
         await self.add_interested_coin_ids(all_coins_names)
         if tx_record.spend_bundle is not None:
             self.tx_pending_changed()
         self.state_changed("pending_transaction", tx_record.wallet_id)
 
-    async def add_transaction(self, tx_record: TransactionRecord):
+    async def add_transaction(self, tx_record: TransactionRecord) -> None:
         """
         Called from wallet to add transaction that is not being set to full_node
         """
         await self.tx_store.add_transaction_record(tx_record)
         self.state_changed("pending_transaction", tx_record.wallet_id)
 
     async def remove_from_queue(
         self,
         spendbundle_id: bytes32,
         name: str,
         send_status: MempoolInclusionStatus,
         error: Optional[Err],
-    ):
+    ) -> None:
         """
         Full node received our transaction, no need to keep it in queue anymore, unless there was an error
         """
 
         updated = await self.tx_store.increment_sent(spendbundle_id, name, send_status, error)
         if updated:
             tx: Optional[TransactionRecord] = await self.get_transaction(spendbundle_id)
@@ -1564,17 +1589,17 @@
     async def get_transaction(self, tx_id: bytes32) -> Optional[TransactionRecord]:
         return await self.tx_store.get_transaction_record(tx_id)
 
     async def get_coin_record_by_wallet_record(self, wr: WalletCoinRecord) -> CoinRecord:
         timestamp: uint64 = await self.wallet_node.get_timestamp_for_height(wr.confirmed_block_height)
         return wr.to_coin_record(timestamp)
 
-    async def get_coin_records_by_coin_ids(self, **kwargs) -> List[CoinRecord]:
-        records = await self.coin_store.get_coin_records(**kwargs)
-        return [await self.get_coin_record_by_wallet_record(record) for record in records.values()]
+    async def get_coin_records_by_coin_ids(self, **kwargs: Any) -> List[CoinRecord]:
+        result = await self.coin_store.get_coin_records(**kwargs)
+        return [await self.get_coin_record_by_wallet_record(record) for record in result.records]
 
     async def get_wallet_for_coin(self, coin_id: bytes32) -> Optional[WalletProtocol]:
         coin_record = await self.coin_store.get_coin_record(coin_id)
         if coin_record is None:
             return None
         wallet_id = uint32(coin_record.wallet_id)
         wallet = self.wallets[wallet_id]
@@ -1586,15 +1611,15 @@
         is the tip, or even beyond the tip.
         """
         await self.nft_store.rollback_to_block(height)
         await self.coin_store.rollback_to_block(height)
         reorged: List[TransactionRecord] = await self.tx_store.get_transaction_above(height)
         await self.tx_store.rollback_to_block(height)
         for record in reorged:
-            if record.type in [
+            if TransactionType(record.type) in [
                 TransactionType.OUTGOING_TX,
                 TransactionType.OUTGOING_TRADE,
                 TransactionType.INCOMING_TRADE,
             ]:
                 await self.tx_store.tx_reorged(record)
 
         # Removes wallets that were created from a blockchain transaction which got reorged.
@@ -1616,15 +1641,15 @@
 
     def unlink_db(self) -> None:
         Path(self.db_path).unlink()
 
     async def get_all_wallet_info_entries(self, wallet_type: Optional[WalletType] = None) -> List[WalletInfo]:
         return await self.user_store.get_all_wallet_info_entries(wallet_type)
 
-    async def get_wallet_for_asset_id(self, asset_id: str):
+    async def get_wallet_for_asset_id(self, asset_id: str) -> Optional[WalletProtocol]:
         for wallet_id, wallet in self.wallets.items():
             if wallet.type() == WalletType.CAT:
                 assert isinstance(wallet, CATWallet)
                 if bytes(wallet.cat_info.limitations_program_hash).hex() == asset_id:
                     return wallet
             elif wallet.type() == WalletType.DATA_LAYER:
                 assert isinstance(wallet, DataLayerWallet)
@@ -1633,23 +1658,23 @@
             elif wallet.type() == WalletType.NFT:
                 assert isinstance(wallet, NFTWallet)
                 nft_coin = await self.nft_store.get_nft_by_id(bytes32.from_hexstr(asset_id), wallet_id)
                 if nft_coin:
                     return wallet
         return None
 
-    async def get_wallet_for_puzzle_info(self, puzzle_driver: PuzzleInfo):
+    async def get_wallet_for_puzzle_info(self, puzzle_driver: PuzzleInfo) -> Optional[WalletProtocol]:
         for wallet in self.wallets.values():
             match_function = getattr(wallet, "match_puzzle_info", None)
             if match_function is not None and callable(match_function):
                 if await match_function(puzzle_driver):
                     return wallet
         return None
 
-    async def create_wallet_for_puzzle_info(self, puzzle_driver: PuzzleInfo, name=None):
+    async def create_wallet_for_puzzle_info(self, puzzle_driver: PuzzleInfo, name: Optional[str] = None) -> None:
         if AssetType(puzzle_driver.type()) in self.asset_to_wallet_map:
             await self.asset_to_wallet_map[AssetType(puzzle_driver.type())].create_from_puzzle_info(
                 self,
                 self.main_wallet,
                 puzzle_driver,
                 name,
             )
@@ -1683,15 +1708,15 @@
                 continue
             if record.coin.name() in removal_dict:
                 continue
             filtered.add(record)
 
         return filtered
 
-    async def new_peak(self, peak: wallet_protocol.NewPeakWallet):
+    async def new_peak(self, peak: NewPeakWallet) -> None:
         for wallet_id, wallet in self.wallets.items():
             if wallet.type() == WalletType.POOLING_WALLET:
                 assert isinstance(wallet, PoolWallet)
                 await wallet.new_peak(uint64(peak.height))
         current_time = int(time.time())
 
         if self.wallet_node.last_wallet_tx_resend_time < current_time - self.wallet_node.wallet_tx_resend_timeout_secs:
@@ -1705,15 +1730,15 @@
 
     async def add_interested_coin_ids(self, coin_ids: List[bytes32]) -> None:
         for coin_id in coin_ids:
             await self.interested_store.add_interested_coin_id(coin_id)
         if len(coin_ids) > 0:
             await self.wallet_node.new_peak_queue.subscribe_to_coin_ids(coin_ids)
 
-    async def delete_trade_transactions(self, trade_id: bytes32):
+    async def delete_trade_transactions(self, trade_id: bytes32) -> None:
         txs: List[TransactionRecord] = await self.tx_store.get_transactions_by_trade_id(trade_id)
         for tx in txs:
             await self.tx_store.delete_transaction_record(tx.name)
 
     async def convert_puzzle_hash(self, wallet_id: uint32, puzzle_hash: bytes32) -> bytes32:
         wallet = self.wallets[wallet_id]
         # This should be general to wallets but for right now this is just for CATs so we'll add this if
```

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_transaction_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_transaction_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_user_store.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_user_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia/wallet/wallet_weight_proof_handler.py` & `chia-blockchain-2.0.0b1/chia/wallet/wallet_weight_proof_handler.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/PKG-INFO` & `chia-blockchain-2.0.0b1/chia_blockchain.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chia-blockchain
-Version: 1.8.1rc2
+Version: 2.0.0b1
 Summary: Chia blockchain full node, farmer, timelord, and wallet.
 Home-page: https://chia.net/
 Author: Mariano Sorgente
 Author-email: mariano@chia.net
 License: Apache License
 Project-URL: Source, https://github.com/Chia-Network/chia-blockchain/
 Project-URL: Changelog, https://github.com/Chia-Network/chia-blockchain/blob/main/CHANGELOG.md
```

### Comparing `chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/SOURCES.txt` & `chia-blockchain-2.0.0b1/chia_blockchain.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -612,14 +612,17 @@
 chia/wallet/puzzles/pool_member_innerpuz.clsp.hex
 chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp
 chia/wallet/puzzles/pool_waitingroom_innerpuz.clsp.hex
 chia/wallet/puzzles/puzzle_utils.py
 chia/wallet/puzzles/rom_bootstrap_generator.clsp
 chia/wallet/puzzles/rom_bootstrap_generator.clsp.hex
 chia/wallet/puzzles/rom_bootstrap_generator.py
+chia/wallet/puzzles/rom_bootstrap_generator2.clsp
+chia/wallet/puzzles/rom_bootstrap_generator2.clsp.hex
+chia/wallet/puzzles/rom_bootstrap_generator2.clsp.hex.sha256tree
 chia/wallet/puzzles/settlement_payments.clsp
 chia/wallet/puzzles/settlement_payments.clsp.hex
 chia/wallet/puzzles/settlement_payments_old.clsp
 chia/wallet/puzzles/settlement_payments_old.clsp.hex
 chia/wallet/puzzles/sha256tree.clib
 chia/wallet/puzzles/sha256tree_module.clsp
 chia/wallet/puzzles/sha256tree_module.clsp.hex
@@ -801,14 +804,15 @@
 tests/core/util/test_config.py
 tests/core/util/test_file_keyring_synchronization.py
 tests/core/util/test_files.py
 tests/core/util/test_jsonify.py
 tests/core/util/test_keychain.py
 tests/core/util/test_keyring_wrapper.py
 tests/core/util/test_lockfile.py
+tests/core/util/test_log_exceptions.py
 tests/core/util/test_lru_cache.py
 tests/core/util/test_significant_bits.py
 tests/core/util/test_streamable.py
 tests/db/__init__.py
 tests/db/test_db_wrapper.py
 tests/farmer_harvester/__init__.py
 tests/farmer_harvester/config.py
```

### Comparing `chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/entry_points.txt` & `chia-blockchain-2.0.0b1/chia_blockchain.egg-info/entry_points.txt`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/chia_blockchain.egg-info/requires.txt` & `chia-blockchain-2.0.0b1/chia_blockchain.egg-info/requires.txt`

 * *Files 6% similar despite different names*

```diff
@@ -6,37 +6,37 @@
 chiabip158==1.2
 chiapos==1.0.11
 clvm==0.9.7
 clvm_tools==0.4.6
 chia_rs==0.2.7
 clvm-tools-rs==0.1.30
 aiohttp==3.8.4
-aiosqlite==0.17.0
+aiosqlite==0.19.0
 bitstring==4.0.1
 colorama==0.4.6
 colorlog==6.7.0
-concurrent-log-handler==0.9.20
+concurrent-log-handler==0.9.23
 cryptography==39.0.1
-filelock==3.9.0
+filelock==3.12.0
 keyring==23.13.1
 PyYAML==6.0
 setproctitle==1.3.2
 sortedcontainers==2.4.0
 click==8.1.3
 dnspython==2.3.0
 watchdog==2.2.0
 dnslib==0.9.23
 typing-extensions==4.5.0
 zstd==1.5.4.0
-packaging==23.0
+packaging==23.1
 psutil==5.9.4
 
 [dev]
 build
-coverage
+coverage>=7.2.4
 diff-cover
 pre-commit
 py3createtorrent
 pylint
 pytest
 pytest-asyncio>=0.18.1
 pytest-cov
@@ -44,15 +44,15 @@
 twine
 isort
 flake8
 mypy
 black==23.3.0
 aiohttp_cors
 ipython
-pyinstaller==5.8.0
+pyinstaller==5.10.1
 types-aiofiles
 types-cryptography
 types-pkg_resources
 types-pyyaml
 types-setuptools
 
 [dev:sys_platform == "linux"]
```

### Comparing `chia-blockchain-1.8.1rc2/install-gui.sh` & `chia-blockchain-2.0.0b1/install-gui.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/install-plotter.sh` & `chia-blockchain-2.0.0b1/install-plotter.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/install-timelord.sh` & `chia-blockchain-2.0.0b1/install-timelord.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/install.sh` & `chia-blockchain-2.0.0b1/install.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/installhelper.py` & `chia-blockchain-2.0.0b1/installhelper.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/mozilla-ca/cacert.pem` & `chia-blockchain-2.0.0b1/mozilla-ca/cacert.pem`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/mypy.ini` & `chia-blockchain-2.0.0b1/mypy.ini`

 * *Files 4% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 no_implicit_optional = True
 warn_return_any = True
 no_implicit_reexport = True
 strict_equality = True
 warn_redundant_casts = True
 
 # list created by: venv/bin/mypy | sed -n 's/.py:.*//p' | sort | uniq | tr '/' '.' | tr '\n' ','
-[mypy-chia.cmds.passphrase,chia.cmds.passphrase_funcs,chia.cmds.plots,chia.cmds.plotters,chia.cmds.show,chia.cmds.start_funcs,chia.cmds.wallet,chia.cmds.wallet_funcs,chia.daemon.server,chia.farmer.farmer_api,chia.full_node.weight_proof,chia.introducer.introducer,chia.introducer.introducer_api,chia.plotters.bladebit,chia.plotters.chiapos,chia.plotters.madmax,chia.plotters.plotters,chia.plotters.plotters_util,chia.plotting.create_plots,chia.plotting.manager,chia.plotting.util,chia.pools.pool_puzzles,chia.pools.pool_wallet,chia.pools.pool_wallet_info,chia.rpc.full_node_rpc_client,chia.rpc.harvester_rpc_api,chia.rpc.harvester_rpc_client,chia.rpc.rpc_client,chia.rpc.timelord_rpc_api,chia.rpc.util,chia.rpc.wallet_rpc_api,chia.rpc.wallet_rpc_client,chia.seeder.crawler,chia.seeder.crawler_api,chia.seeder.crawl_store,chia.seeder.dns_server,chia.seeder.peer_record,chia.seeder.start_crawler,chia.simulator.full_node_simulator,chia.simulator.start_simulator,chia.ssl.create_ssl,chia.timelord.iters_from_block,chia.timelord.timelord,chia.timelord.timelord_api,chia.timelord.timelord_launcher,chia.timelord.timelord_state,chia.types.blockchain_format.program,chia.util.block_cache,chia.util.check_fork_next_block,chia.util.chia_logging,chia.util.config,chia.util.db_wrapper,chia.util.dump_keyring,chia.util.hash,chia.util.json_util,chia.util.keychain,chia.util.keyring_wrapper,chia.util.log_exceptions,chia.util.make_test_constants,chia.util.merkle_set,chia.util.network,chia.util.partial_func,chia.util.profiler,chia.util.safe_cancel_task,chia.util.service_groups,chia.util.ssl_check,chia.util.validate_alert,chia.wallet.block_record,chia.wallet.chialisp,chia.wallet.did_wallet.did_wallet,chia.wallet.did_wallet.did_wallet_puzzles,chia.wallet.key_val_store,chia.wallet.lineage_proof,chia.wallet.payment,chia.wallet.puzzles.load_clvm,chia.wallet.puzzles.p2_conditions,chia.wallet.puzzles.p2_delegated_conditions,chia.wallet.puzzles.p2_delegated_puzzle,chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle,chia.wallet.puzzles.p2_m_of_n_delegate_direct,chia.wallet.puzzles.p2_puzzle_hash,chia.wallet.puzzles.prefarm.spend_prefarm,chia.wallet.puzzles.puzzle_utils,chia.wallet.puzzles.singleton_top_layer,chia.wallet.puzzles.tails,chia.wallet.secret_key_store,chia.wallet.trade_record,chia.wallet.trading.trade_store,chia.wallet.transaction_record,chia.wallet.util.debug_spend_bundle,chia.wallet.util.new_peak_queue,chia.wallet.wallet,chia.wallet.wallet_coin_store,chia.wallet.wallet_interested_store,chia.wallet.wallet_node_api,chia.wallet.wallet_pool_store,chia.wallet.wallet_puzzle_store,chia.wallet.wallet_state_manager,chia.wallet.wallet_sync_store,chia.wallet.wallet_transaction_store,chia.wallet.wallet_user_store,installhelper,tests.blockchain.blockchain_test_utils,tests.blockchain.test_blockchain,tests.blockchain.test_blockchain_transactions,chia.simulator.block_tools,tests.build-init-files,tests.build-workflows,tests.clvm.coin_store,tests.clvm.test_chialisp_deserialization,tests.clvm.test_clvm_compilation,tests.clvm.test_program,tests.clvm.test_puzzle_compression,tests.clvm.test_puzzles,tests.clvm.test_serialized_program,tests.clvm.test_singletons,tests.clvm.test_spend_sim,tests.conftest,tests.connection_utils,tests.core.cmds.test_keys,tests.core.consensus.test_pot_iterations,tests.core.custom_types.test_coin,tests.core.custom_types.test_proof_of_space,tests.core.custom_types.test_spend_bundle,tests.core.daemon.test_daemon,tests.core.full_node.full_sync.test_full_sync,tests.core.full_node.stores.test_block_store,tests.core.full_node.stores.test_coin_store,tests.core.full_node.stores.test_full_node_store,tests.core.full_node.stores.test_hint_store,tests.core.full_node.stores.test_sync_store,tests.core.full_node.test_address_manager,tests.core.full_node.test_block_height_map,tests.core.full_node.test_conditions,tests.core.full_node.test_full_node,tests.core.mempool.test_mempool,tests.core.mempool.test_mempool_performance,tests.core.full_node.test_node_load,tests.core.full_node.test_peer_store_resolver,tests.core.full_node.test_performance,tests.core.full_node.test_transactions,tests.core.make_block_generator,tests.core.node_height,tests.core.server.test_dos,tests.core.server.test_rate_limits,tests.core.ssl.test_ssl,tests.core.test_cost_calculation,tests.core.test_crawler_rpc,tests.core.test_daemon_rpc,tests.core.test_db_conversion,tests.core.test_db_validation,tests.core.test_farmer_harvester_rpc,tests.core.test_filter,tests.core.test_full_node_rpc,tests.core.test_merkle_set,tests.core.test_setproctitle,tests.core.util.test_cached_bls,tests.core.util.test_config,tests.core.util.test_file_keyring_synchronization,tests.core.util.test_files,tests.core.util.test_keychain,tests.core.util.test_keyring_wrapper,tests.core.util.test_lru_cache,tests.core.util.test_significant_bits,tests.farmer_harvester.test_farmer_harvester,tests.generator.test_list_to_batches,tests.generator.test_scan,tests.plotting.test_plot_manager,tests.pools.test_pool_cmdline,tests.pools.test_pool_config,tests.pools.test_pool_puzzles_lifecycle,tests.pools.test_wallet_pool_store,tests.simulation.test_simulation,chia.simulator.time_out_assert,tests.tools.test_full_sync,tests.tools.test_run_block,tests.util.alert_server,tests.util.benchmark_cost,tests.util.blockchain,tests.util.build_network_protocol_files,tests.util.db_connection,tests.util.generator_tools_testing,chia.simulator.keyring,tests.util.key_tool,tests.util.test_full_block_utils,tests.util.test_lock_queue,tests.util.test_misc,tests.util.test_network,tests.util.test_network_protocol_files,tests.wallet.cat_wallet.test_cat_lifecycle,tests.wallet.cat_wallet.test_cat_wallet,tests.wallet.cat_wallet.test_offer_lifecycle,tests.wallet.cat_wallet.test_trades,tests.wallet.did_wallet.test_did,tests.wallet.did_wallet.test_did_rpc,tests.wallet.did_wallet.test_nft_rpc,tests.wallet.did_wallet.test_nft_wallet,tests.wallet.rpc.test_wallet_rpc,tests.wallet.simple_sync.test_simple_sync_protocol,tests.wallet.sync.test_wallet_sync,tests.wallet.test_bech32m,tests.wallet.test_chialisp,tests.wallet.test_puzzle_store,tests.wallet.test_singleton,tests.wallet.test_singleton_lifecycle,tests.wallet.test_singleton_lifecycle_fast,tests.wallet.test_taproot,tests.wallet.test_wallet_blockchain,tests.wallet.test_wallet_interested_store,tests.wallet.test_wallet_key_val_store,tests.wallet.test_wallet_user_store,chia.simulator.wallet_tools,tests.weight_proof.test_weight_proof,tools.analyze-chain,tools.run_block,tools.test_full_sync,tests.wallet.nft_wallet.test_nft_wallet,chia.wallet.nft_wallet.nft_puzzles,tests.wallet.nft_wallet.test_nft_puzzles]
+[mypy-chia.cmds.passphrase,chia.cmds.passphrase_funcs,chia.cmds.plots,chia.cmds.plotters,chia.cmds.show,chia.cmds.start_funcs,chia.cmds.wallet,chia.cmds.wallet_funcs,chia.daemon.server,chia.farmer.farmer_api,chia.full_node.weight_proof,chia.introducer.introducer,chia.introducer.introducer_api,chia.plotters.bladebit,chia.plotters.chiapos,chia.plotters.madmax,chia.plotters.plotters,chia.plotters.plotters_util,chia.plotting.create_plots,chia.plotting.manager,chia.plotting.util,chia.pools.pool_puzzles,chia.pools.pool_wallet,chia.pools.pool_wallet_info,chia.rpc.full_node_rpc_client,chia.rpc.harvester_rpc_api,chia.rpc.harvester_rpc_client,chia.rpc.rpc_client,chia.rpc.timelord_rpc_api,chia.rpc.util,chia.rpc.wallet_rpc_api,chia.rpc.wallet_rpc_client,chia.seeder.crawler,chia.seeder.crawler_api,chia.seeder.crawl_store,chia.seeder.dns_server,chia.seeder.peer_record,chia.seeder.start_crawler,chia.simulator.full_node_simulator,chia.simulator.start_simulator,chia.ssl.create_ssl,chia.timelord.iters_from_block,chia.timelord.timelord,chia.timelord.timelord_api,chia.timelord.timelord_launcher,chia.timelord.timelord_state,chia.types.blockchain_format.program,chia.util.block_cache,chia.util.check_fork_next_block,chia.util.chia_logging,chia.util.config,chia.util.db_wrapper,chia.util.dump_keyring,chia.util.hash,chia.util.json_util,chia.util.keychain,chia.util.keyring_wrapper,chia.util.log_exceptions,chia.util.make_test_constants,chia.util.merkle_set,chia.util.network,chia.util.partial_func,chia.util.profiler,chia.util.safe_cancel_task,chia.util.service_groups,chia.util.ssl_check,chia.util.validate_alert,chia.wallet.block_record,chia.wallet.chialisp,chia.wallet.did_wallet.did_wallet,chia.wallet.did_wallet.did_wallet_puzzles,chia.wallet.key_val_store,chia.wallet.lineage_proof,chia.wallet.payment,chia.wallet.puzzles.load_clvm,chia.wallet.puzzles.p2_conditions,chia.wallet.puzzles.p2_delegated_conditions,chia.wallet.puzzles.p2_delegated_puzzle,chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle,chia.wallet.puzzles.p2_m_of_n_delegate_direct,chia.wallet.puzzles.p2_puzzle_hash,chia.wallet.puzzles.prefarm.spend_prefarm,chia.wallet.puzzles.puzzle_utils,chia.wallet.puzzles.singleton_top_layer,chia.wallet.puzzles.tails,chia.wallet.secret_key_store,chia.wallet.trade_record,chia.wallet.trading.trade_store,chia.wallet.transaction_record,chia.wallet.util.debug_spend_bundle,chia.wallet.util.new_peak_queue,chia.wallet.wallet,chia.wallet.wallet_coin_store,chia.wallet.wallet_interested_store,chia.wallet.wallet_node_api,chia.wallet.wallet_pool_store,chia.wallet.wallet_puzzle_store,chia.wallet.wallet_sync_store,chia.wallet.wallet_transaction_store,chia.wallet.wallet_user_store,installhelper,tests.blockchain.blockchain_test_utils,tests.blockchain.test_blockchain,chia.simulator.block_tools,tests.build-init-files,tests.build-workflows,tests.clvm.coin_store,tests.clvm.test_chialisp_deserialization,tests.clvm.test_clvm_compilation,tests.clvm.test_program,tests.clvm.test_puzzle_compression,tests.clvm.test_puzzles,tests.clvm.test_serialized_program,tests.clvm.test_singletons,tests.clvm.test_spend_sim,tests.conftest,tests.connection_utils,tests.core.cmds.test_keys,tests.core.consensus.test_pot_iterations,tests.core.custom_types.test_coin,tests.core.custom_types.test_proof_of_space,tests.core.custom_types.test_spend_bundle,tests.core.daemon.test_daemon,tests.core.full_node.full_sync.test_full_sync,tests.core.full_node.stores.test_block_store,tests.core.full_node.stores.test_coin_store,tests.core.full_node.stores.test_full_node_store,tests.core.full_node.stores.test_hint_store,tests.core.full_node.stores.test_sync_store,tests.core.full_node.test_address_manager,tests.core.full_node.test_block_height_map,tests.core.full_node.test_conditions,tests.core.full_node.test_full_node,tests.core.mempool.test_mempool,tests.core.mempool.test_mempool_performance,tests.core.full_node.test_node_load,tests.core.full_node.test_peer_store_resolver,tests.core.full_node.test_performance,tests.core.full_node.test_transactions,tests.core.make_block_generator,tests.core.node_height,tests.core.server.test_dos,tests.core.server.test_rate_limits,tests.core.ssl.test_ssl,tests.core.test_cost_calculation,tests.core.test_crawler_rpc,tests.core.test_daemon_rpc,tests.core.test_db_conversion,tests.core.test_db_validation,tests.core.test_farmer_harvester_rpc,tests.core.test_filter,tests.core.test_full_node_rpc,tests.core.test_merkle_set,tests.core.test_setproctitle,tests.core.util.test_cached_bls,tests.core.util.test_config,tests.core.util.test_file_keyring_synchronization,tests.core.util.test_files,tests.core.util.test_keychain,tests.core.util.test_keyring_wrapper,tests.core.util.test_lru_cache,tests.core.util.test_significant_bits,tests.farmer_harvester.test_farmer_harvester,tests.generator.test_list_to_batches,tests.generator.test_scan,tests.plotting.test_plot_manager,tests.pools.test_pool_cmdline,tests.pools.test_pool_config,tests.pools.test_pool_puzzles_lifecycle,tests.pools.test_wallet_pool_store,tests.simulation.test_simulation,chia.simulator.time_out_assert,tests.tools.test_full_sync,tests.tools.test_run_block,tests.util.alert_server,tests.util.benchmark_cost,tests.util.build_network_protocol_files,tests.util.db_connection,tests.util.generator_tools_testing,chia.simulator.keyring,tests.util.key_tool,tests.util.test_full_block_utils,tests.util.test_lock_queue,tests.util.test_misc,tests.util.test_network,tests.util.test_network_protocol_files,tests.wallet.cat_wallet.test_cat_lifecycle,tests.wallet.cat_wallet.test_cat_wallet,tests.wallet.cat_wallet.test_offer_lifecycle,tests.wallet.cat_wallet.test_trades,tests.wallet.did_wallet.test_did,tests.wallet.did_wallet.test_did_rpc,tests.wallet.did_wallet.test_nft_rpc,tests.wallet.did_wallet.test_nft_wallet,tests.wallet.rpc.test_wallet_rpc,tests.wallet.simple_sync.test_simple_sync_protocol,tests.wallet.sync.test_wallet_sync,tests.wallet.test_bech32m,tests.wallet.test_chialisp,tests.wallet.test_puzzle_store,tests.wallet.test_singleton,tests.wallet.test_singleton_lifecycle,tests.wallet.test_singleton_lifecycle_fast,tests.wallet.test_taproot,tests.wallet.test_wallet_blockchain,tests.wallet.test_wallet_interested_store,tests.wallet.test_wallet_key_val_store,tests.wallet.test_wallet_user_store,chia.simulator.wallet_tools,tests.weight_proof.test_weight_proof,tools.analyze-chain,tools.run_block,tools.test_full_sync,tests.wallet.nft_wallet.test_nft_wallet,chia.wallet.nft_wallet.nft_puzzles,tests.wallet.nft_wallet.test_nft_puzzles]
 disable_error_code = annotation-unchecked
 disallow_any_generics = False
 disallow_subclassing_any = False
 disallow_untyped_calls = False
 disallow_untyped_defs = False
 disallow_incomplete_defs = False
 check_untyped_defs = False
```

### Comparing `chia-blockchain-1.8.1rc2/pylintrc` & `chia-blockchain-2.0.0b1/pylintrc`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/pytest.ini` & `chia-blockchain-2.0.0b1/pytest.ini`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/setup.py` & `chia-blockchain-2.0.0b1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,42 +14,43 @@
     "chiabip158==1.2",  # bip158-style wallet filters
     "chiapos==1.0.11",  # proof of space
     "clvm==0.9.7",
     "clvm_tools==0.4.6",  # Currying, Program.to, other conveniences
     "chia_rs==0.2.7",
     "clvm-tools-rs==0.1.30",  # Rust implementation of clvm_tools' compiler
     "aiohttp==3.8.4",  # HTTP server for full node rpc
-    "aiosqlite==0.17.0",  # asyncio wrapper for sqlite, to store blocks
+    "aiosqlite==0.19.0",  # asyncio wrapper for sqlite, to store blocks
     "bitstring==4.0.1",  # Binary data management library
     "colorama==0.4.6",  # Colorizes terminal output
     "colorlog==6.7.0",  # Adds color to logs
-    "concurrent-log-handler==0.9.20",  # Concurrently log and rotate logs
+    "concurrent-log-handler==0.9.23",  # Concurrently log and rotate logs
     "cryptography==39.0.1",  # Python cryptography library for TLS - keyring conflict
-    "filelock==3.9.0",  # For reading and writing config multiprocess and multithread safely  (non-reentrant locks)
+    "filelock==3.12.0",  # For reading and writing config multiprocess and multithread safely  (non-reentrant locks)
     "keyring==23.13.1",  # Store keys in MacOS Keychain, Windows Credential Locker
     "PyYAML==6.0",  # Used for config file format
     "setproctitle==1.3.2",  # Gives the chia processes readable names
     "sortedcontainers==2.4.0",  # For maintaining sorted mempools
     "click==8.1.3",  # For the CLI
     "dnspython==2.3.0",  # Query DNS seeds
     "watchdog==2.2.0",  # Filesystem event watching - watches keyring.yaml
     "dnslib==0.9.23",  # dns lib
     "typing-extensions==4.5.0",  # typing backports like Protocol and TypedDict
     "zstd==1.5.4.0",
-    "packaging==23.0",
+    "packaging==23.1",
     "psutil==5.9.4",
 ]
 
 upnp_dependencies = [
     "miniupnpc==2.2.2",  # Allows users to open ports on their router
 ]
 
 dev_dependencies = [
     "build",
-    "coverage",
+    # >=7.2.4 for https://github.com/nedbat/coveragepy/issues/1604
+    "coverage>=7.2.4",
     "diff-cover",
     "pre-commit",
     "py3createtorrent",
     "pylint",
     "pytest",
     "pytest-asyncio>=0.18.1",  # require attribute 'fixture'
     "pytest-cov",
@@ -58,15 +59,15 @@
     "twine",
     "isort",
     "flake8",
     "mypy",
     "black==23.3.0",
     "aiohttp_cors",  # For blackd
     "ipython",  # For asyncio debugging
-    "pyinstaller==5.8.0",
+    "pyinstaller==5.10.1",
     "types-aiofiles",
     "types-cryptography",
     "types-pkg_resources",
     "types-pyyaml",
     "types-setuptools",
 ]
```

### Comparing `chia-blockchain-1.8.1rc2/start-gui.sh` & `chia-blockchain-2.0.0b1/start-gui.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/README.md` & `chia-blockchain-2.0.0b1/tests/README.md`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/blockchain/blockchain_test_utils.py` & `chia-blockchain-2.0.0b1/tests/blockchain/blockchain_test_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/blockchain/test_blockchain.py` & `chia-blockchain-2.0.0b1/tests/blockchain/test_blockchain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/blockchain/test_blockchain_transactions.py` & `chia-blockchain-2.0.0b1/tests/blockchain/test_blockchain_transactions.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,57 +1,64 @@
 from __future__ import annotations
 
 import logging
+from typing import Tuple
 
 import pytest
 from clvm.casts import int_to_bytes
 
+from chia.full_node.full_node_api import FullNodeAPI
 from chia.protocols import wallet_protocol
-from chia.simulator.block_tools import test_constants
+from chia.server.server import ChiaServer
+from chia.simulator.block_tools import BlockTools, test_constants
 from chia.simulator.wallet_tools import WalletTool
 from chia.types.announcement import Announcement
+from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.condition_opcodes import ConditionOpcode
 from chia.types.condition_with_args import ConditionWithArgs
 from chia.types.spend_bundle import SpendBundle
 from chia.util.errors import ConsensusError, Err
-from chia.util.ints import uint64
+from chia.util.ints import uint32, uint64
 from tests.blockchain.blockchain_test_utils import _validate_and_add_block
 from tests.util.generator_tools_testing import run_and_get_removals_and_additions
 
-BURN_PUZZLE_HASH = b"0" * 32
+BURN_PUZZLE_HASH = bytes32(b"0" * 32)
 
 WALLET_A = WalletTool(test_constants)
 WALLET_A_PUZZLE_HASHES = [WALLET_A.get_new_puzzlehash() for _ in range(5)]
 
 log = logging.getLogger(__name__)
 
 
 class TestBlockchainTransactions:
     @pytest.mark.asyncio
-    async def test_basic_blockchain_tx(self, two_nodes):
+    async def test_basic_blockchain_tx(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block, None)
 
         spend_block = blocks[2]
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
 
-        spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_puzzlehash, spend_coin)
+        assert spend_coin is not None
+        spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_puzzlehash, spend_coin)
 
         assert spend_bundle is not None
         tx: wallet_protocol.SendTransaction = wallet_protocol.SendTransaction(spend_bundle)
 
         await full_node_api_1.send_transaction(tx)
 
         sb = full_node_1.mempool_manager.get_spendbundle(spend_bundle.name())
@@ -69,49 +76,54 @@
             transaction_data=next_spendbundle,
             guarantee_transaction_block=True,
         )
 
         next_block = new_blocks[-1]
         await full_node_1.add_block(next_block)
 
-        assert next_block.header_hash == full_node_1.blockchain.get_peak().header_hash
+        blockchain_peak = full_node_1.blockchain.get_peak()
+        assert blockchain_peak is not None
+        assert next_block.header_hash == blockchain_peak.header_hash
 
         added_coins = next_spendbundle.additions()
 
         # Two coins are added, main spend and change
         assert len(added_coins) == 2
         for coin in added_coins:
             unspent = await full_node_1.coin_store.get_coin_record(coin.name())
             assert unspent is not None
             assert not unspent.spent
             assert not unspent.coinbase
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_with_double_spend(self, two_nodes):
+    async def test_validate_blockchain_with_double_spend(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 5
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
         spend_block = blocks[2]
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
+        assert spend_coin is not None
 
-        spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_puzzlehash, spend_coin)
-        spend_bundle_double = wallet_a.generate_signed_transaction(1001, receiver_puzzlehash, spend_coin)
+        spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_puzzlehash, spend_coin)
+        spend_bundle_double = wallet_a.generate_signed_transaction(uint64(1001), receiver_puzzlehash, spend_coin)
 
         block_spendbundle = SpendBundle.aggregate([spend_bundle, spend_bundle_double])
 
         new_blocks = bt.get_consecutive_blocks(
             1,
             block_list_input=blocks,
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
@@ -119,72 +131,78 @@
             guarantee_transaction_block=True,
         )
 
         next_block = new_blocks[-1]
         await _validate_and_add_block(full_node_1.blockchain, next_block, expected_error=Err.DOUBLE_SPEND)
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_duplicate_output(self, two_nodes):
+    async def test_validate_blockchain_duplicate_output(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 3
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
         spend_block = blocks[2]
 
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
+        assert spend_coin is not None
 
         spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin, additional_outputs=[(receiver_puzzlehash, 1000)]
+            uint64(1000), receiver_puzzlehash, spend_coin, additional_outputs=[(receiver_puzzlehash, 1000)]
         )
 
         new_blocks = bt.get_consecutive_blocks(
             1,
             block_list_input=blocks,
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=spend_bundle,
             guarantee_transaction_block=True,
         )
 
         next_block = new_blocks[-1]
         await _validate_and_add_block(full_node_1.blockchain, next_block, expected_error=Err.DUPLICATE_OUTPUT)
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_with_reorg_double_spend(self, two_nodes):
+    async def test_validate_blockchain_with_reorg_double_spend(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
         spend_block = blocks[2]
 
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
+        assert spend_coin is not None
 
-        spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_puzzlehash, spend_coin)
+        spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_puzzlehash, spend_coin)
 
         blocks_spend = bt.get_consecutive_blocks(
             1,
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             guarantee_transaction_block=True,
             transaction_data=spend_bundle,
         )
@@ -262,22 +280,24 @@
             seed=b"spend at 14 is double spend",
         )
         with pytest.raises(ConsensusError):
             for block in new_blocks_reorg:
                 await full_node_api_1.full_node.add_block(block)
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_spend_reorg_coin(self, two_nodes, softfork_height):
+    async def test_validate_blockchain_spend_reorg_coin(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools], softfork_height: uint32
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_1_puzzlehash = WALLET_A_PUZZLE_HASHES[1]
         receiver_2_puzzlehash = WALLET_A_PUZZLE_HASHES[2]
         receiver_3_puzzlehash = WALLET_A_PUZZLE_HASHES[3]
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
@@ -342,20 +362,22 @@
             transaction_data=spend_bundle,
             guarantee_transaction_block=True,
         )
 
         await full_node_api_1.full_node.add_block(new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_spend_reorg_cb_coin(self, two_nodes):
+    async def test_validate_blockchain_spend_reorg_cb_coin(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 15
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_1_puzzlehash = WALLET_A_PUZZLE_HASHES[1]
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         blocks = bt.get_consecutive_blocks(num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash)
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
         # Spends a coinbase created in reorg
         new_blocks = bt.get_consecutive_blocks(
@@ -370,47 +392,51 @@
             await full_node_api_1.full_node.add_block(block)
 
         spend_block = new_blocks[-1]
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
-        spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_1_puzzlehash, spend_coin)
+        assert spend_coin is not None
+        spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_1_puzzlehash, spend_coin)
 
         new_blocks = bt.get_consecutive_blocks(
             1,
             new_blocks,
             seed=b"reorg cb coin",
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=spend_bundle,
             guarantee_transaction_block=True,
         )
 
         await full_node_api_1.full_node.add_block(new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_validate_blockchain_spend_reorg_since_genesis(self, two_nodes):
+    async def test_validate_blockchain_spend_reorg_since_genesis(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_1_puzzlehash = WALLET_A_PUZZLE_HASHES[1]
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
             await full_node_api_1.full_node.add_block(block)
 
         spend_block = blocks[-1]
         spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
-        spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_1_puzzlehash, spend_coin)
+        assert spend_coin is not None
+        spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_1_puzzlehash, spend_coin)
 
         new_blocks = bt.get_consecutive_blocks(
             1, blocks, seed=b"", farmer_reward_puzzle_hash=coinbase_puzzlehash, transaction_data=spend_bundle
         )
         await full_node_api_1.full_node.add_block(new_blocks[-1])
 
         # Spends a coin in a genesis reorg, that was already spent
@@ -432,20 +458,22 @@
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=spend_bundle,
         )
 
         await full_node_api_1.full_node.add_block(new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_my_coin_id(self, two_nodes):
+    async def test_assert_my_coin_id(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -456,25 +484,29 @@
         spend_block = blocks[2]
         bad_block = blocks[3]
         spend_coin = None
         bad_spend_coin = None
         for coin in list(spend_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin = coin
+        assert spend_coin is not None
         for coin in list(bad_block.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 bad_spend_coin = coin
+        assert bad_spend_coin is not None
         valid_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_MY_COIN_ID, [spend_coin.name()])
         valid_dic = {valid_cvp.opcode: [valid_cvp]}
         bad_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_MY_COIN_ID, [bad_spend_coin.name()])
 
         bad_dic = {bad_cvp.opcode: [bad_cvp]}
-        bad_spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_puzzlehash, spend_coin, bad_dic)
+        bad_spend_bundle = wallet_a.generate_signed_transaction(uint64(1000), receiver_puzzlehash, spend_coin, bad_dic)
 
-        valid_spend_bundle = wallet_a.generate_signed_transaction(1000, receiver_puzzlehash, spend_coin, valid_dic)
+        valid_spend_bundle = wallet_a.generate_signed_transaction(
+            uint64(1000), receiver_puzzlehash, spend_coin, valid_dic
+        )
 
         assert bad_spend_bundle is not None
         assert valid_spend_bundle is not None
 
         # Invalid block bundle
         # Create another block that includes our transaction
         invalid_new_blocks = bt.get_consecutive_blocks(
@@ -498,21 +530,22 @@
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=valid_spend_bundle,
             guarantee_transaction_block=True,
         )
         await _validate_and_add_block(full_node_1.blockchain, new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_coin_announcement_consumed(self, two_nodes):
+    async def test_assert_coin_announcement_consumed(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -523,36 +556,38 @@
         block2 = blocks[3]
 
         spend_coin_block_1 = None
         spend_coin_block_2 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
         for coin in list(block2.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_2 = coin
+        assert spend_coin_block_2 is not None
 
         # This condition requires block2 coinbase to be spent
         block1_cvp = ConditionWithArgs(
             ConditionOpcode.ASSERT_COIN_ANNOUNCEMENT,
             [Announcement(spend_coin_block_2.name(), b"test").name()],
         )
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # This condition requires block1 coinbase to be spent
         block2_cvp = ConditionWithArgs(
             ConditionOpcode.CREATE_COIN_ANNOUNCEMENT,
             [b"test"],
         )
         block2_dic = {block2_cvp.opcode: [block2_cvp]}
         block2_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_2, block2_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_2, block2_dic
         )
 
         # Invalid block bundle
         assert block1_spend_bundle is not None
         # Create another block that includes our transaction
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
@@ -579,21 +614,22 @@
             guarantee_transaction_block=True,
         )
 
         # Try to validate newly created block
         await _validate_and_add_block(full_node_1.blockchain, new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_puzzle_announcement_consumed(self, two_nodes):
+    async def test_assert_puzzle_announcement_consumed(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -604,36 +640,38 @@
         block2 = blocks[3]
 
         spend_coin_block_1 = None
         spend_coin_block_2 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
         for coin in list(block2.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_2 = coin
+        assert spend_coin_block_2 is not None
 
         # This condition requires block2 coinbase to be spent
         block1_cvp = ConditionWithArgs(
             ConditionOpcode.ASSERT_PUZZLE_ANNOUNCEMENT,
             [Announcement(spend_coin_block_2.puzzle_hash, b"test").name()],
         )
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # This condition requires block1 coinbase to be spent
         block2_cvp = ConditionWithArgs(
             ConditionOpcode.CREATE_PUZZLE_ANNOUNCEMENT,
             [b"test"],
         )
         block2_dic = {block2_cvp.opcode: [block2_cvp]}
         block2_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_2, block2_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_2, block2_dic
         )
 
         # Invalid block bundle
         assert block1_spend_bundle is not None
         # Create another block that includes our transaction
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
@@ -660,21 +698,22 @@
             guarantee_transaction_block=True,
         )
 
         # Try to validate newly created block
         await _validate_and_add_block(full_node_1.blockchain, new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_height_absolute(self, two_nodes):
+    async def test_assert_height_absolute(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -682,20 +721,21 @@
 
         # Coinbase that gets spent
         block1 = blocks[2]
         spend_coin_block_1 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
 
         # This condition requires block1 coinbase to be spent after index 10
         block1_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_HEIGHT_ABSOLUTE, [int_to_bytes(10)])
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # program that will be sent too early
         assert block1_spend_bundle is not None
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
             blocks,
@@ -724,21 +764,22 @@
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=block1_spend_bundle,
             guarantee_transaction_block=True,
         )
         await _validate_and_add_block(full_node_1.blockchain, new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_height_relative(self, two_nodes):
+    async def test_assert_height_relative(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 11
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -746,22 +787,23 @@
 
         # Coinbase that gets spent
         block1 = blocks[2]
         spend_coin_block_1 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
 
         # This condition requires block1 coinbase to be spent after index 11
         # This condition requires block1 coinbase to be spent more than 10 block after it was farmed
         # block index has to be greater than (2 + 9 = 11)
         block1_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_HEIGHT_RELATIVE, [int_to_bytes(9)])
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # program that will be sent too early
         assert block1_spend_bundle is not None
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
             blocks,
@@ -790,21 +832,22 @@
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
             transaction_data=block1_spend_bundle,
             guarantee_transaction_block=True,
         )
         await _validate_and_add_block(full_node_1.blockchain, new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_seconds_relative(self, two_nodes):
+    async def test_assert_seconds_relative(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -812,20 +855,21 @@
 
         # Coinbase that gets spent
         block1 = blocks[2]
         spend_coin_block_1 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
 
         # This condition requires block1 coinbase to be spent 300 seconds after coin creation
         block1_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_SECONDS_RELATIVE, [int_to_bytes(300)])
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # program that will be sent to early
         assert block1_spend_bundle is not None
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
             blocks,
@@ -847,21 +891,22 @@
             transaction_data=block1_spend_bundle,
             guarantee_transaction_block=True,
             time_per_block=301,
         )
         await _validate_and_add_block(full_node_1.blockchain, valid_new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_seconds_absolute(self, two_nodes):
+    async def test_assert_seconds_absolute(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -869,21 +914,23 @@
 
         # Coinbase that gets spent
         block1 = blocks[2]
         spend_coin_block_1 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
 
         # This condition requires block1 coinbase to be spent after 30 seconds from now
+        assert blocks[-1].foliage_transaction_block is not None
         current_time_plus3 = uint64(blocks[-1].foliage_transaction_block.timestamp + 30)
         block1_cvp = ConditionWithArgs(ConditionOpcode.ASSERT_SECONDS_ABSOLUTE, [int_to_bytes(current_time_plus3)])
         block1_dic = {block1_cvp.opcode: [block1_cvp]}
         block1_spend_bundle = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic
         )
 
         # program that will be sent to early
         assert block1_spend_bundle is not None
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
             blocks,
@@ -905,21 +952,22 @@
             transaction_data=block1_spend_bundle,
             guarantee_transaction_block=True,
             time_per_block=31,
         )
         await _validate_and_add_block(full_node_1.blockchain, valid_new_blocks[-1])
 
     @pytest.mark.asyncio
-    async def test_assert_fee_condition(self, two_nodes):
+    async def test_assert_fee_condition(
+        self, two_nodes: Tuple[FullNodeAPI, FullNodeAPI, ChiaServer, ChiaServer, BlockTools]
+    ) -> None:
         num_blocks = 10
         wallet_a = WALLET_A
         coinbase_puzzlehash = WALLET_A_PUZZLE_HASHES[0]
         receiver_puzzlehash = BURN_PUZZLE_HASH
-
-        full_node_api_1, full_node_api_2, server_1, server_2, bt = two_nodes
+        full_node_api_1, _, _, _, bt = two_nodes
         full_node_1 = full_node_api_1.full_node
         # Farm blocks
         blocks = bt.get_consecutive_blocks(
             num_blocks, farmer_reward_puzzle_hash=coinbase_puzzlehash, guarantee_transaction_block=True
         )
 
         for block in blocks:
@@ -927,25 +975,26 @@
 
         # Coinbase that gets spent
         block1 = blocks[2]
         spend_coin_block_1 = None
         for coin in list(block1.get_included_reward_coins()):
             if coin.puzzle_hash == coinbase_puzzlehash:
                 spend_coin_block_1 = coin
+        assert spend_coin_block_1 is not None
 
         # This condition requires fee to be 10 mojo
         cvp_fee = ConditionWithArgs(ConditionOpcode.RESERVE_FEE, [int_to_bytes(10)])
         # This spend bundle has 9 mojo as fee
         block1_dic_bad = {cvp_fee.opcode: [cvp_fee]}
         block1_dic_good = {cvp_fee.opcode: [cvp_fee]}
         block1_spend_bundle_bad = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic_bad, fee=9
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic_bad, fee=9
         )
         block1_spend_bundle_good = wallet_a.generate_signed_transaction(
-            1000, receiver_puzzlehash, spend_coin_block_1, block1_dic_good, fee=10
+            uint64(1000), receiver_puzzlehash, spend_coin_block_1, block1_dic_good, fee=10
         )
         log.warning(block1_spend_bundle_good.additions())
         log.warning(f"Spend bundle fees: {block1_spend_bundle_good.fees()}")
         invalid_new_blocks = bt.get_consecutive_blocks(
             1,
             blocks,
             farmer_reward_puzzle_hash=coinbase_puzzlehash,
```

### Comparing `chia-blockchain-1.8.1rc2/tests/build-init-files.py` & `chia-blockchain-2.0.0b1/tests/build-init-files.py`

 * *Files 11% similar despite different names*

```diff
@@ -8,30 +8,54 @@
 # See https://docs.python.org/3/tutorial/modules.html#packages.
 #
 # Note: This script is run in a `pre-commit` hook (which runs on CI) to make sure we don't miss out any folder.
 
 from __future__ import annotations
 
 import logging
-import os
 import pathlib
-import sys
+from typing import List
 
 import click
 
 log_levels = {
     0: logging.ERROR,
     1: logging.WARNING,
     2: logging.INFO,
 }
 
 
 ignores = {"__pycache__", ".pytest_cache"}
 
 
+def traverse_directory(path: pathlib.Path) -> List[pathlib.Path]:
+    of_interest: List[pathlib.Path] = []
+
+    file_found = False
+
+    for member in path.iterdir():
+        if not member.is_dir():
+            file_found = True
+            continue
+
+        if member.name in ignores:
+            continue
+
+        found = traverse_directory(path=member)
+        of_interest.extend(found)
+
+        if len(found) > 0:
+            of_interest.append(member)
+
+    if len(of_interest) > 0 or file_found:
+        of_interest.append(path)
+
+    return of_interest
+
+
 @click.command()
 @click.option(
     "-r", "--root", "root_str", type=click.Path(dir_okay=True, file_okay=False, resolve_path=True), default="."
 )
 @click.option("-v", "--verbose", count=True, help=f"Increase verbosity up to {len(log_levels) - 1} times")
 def command(verbose, root_str):
     logger = logging.getLogger()
@@ -39,37 +63,31 @@
     logger.setLevel(log_level)
     stream_handler = logging.StreamHandler()
     logger.addHandler(stream_handler)
 
     tree_roots = ["benchmarks", "build_scripts", "chia", "tests", "tools"]
     failed = False
     root = pathlib.Path(root_str).resolve()
-    directories = sorted(
-        path
-        for tree_root in tree_roots
-        for path in root.joinpath(tree_root).rglob("**/")
-        if all(part not in ignores for part in path.parts)
-    )
+    directories = [
+        directory for tree_root in tree_roots for directory in traverse_directory(path=root.joinpath(tree_root))
+    ]
 
     for path in directories:
         init_path = path.joinpath("__init__.py")
         # This has plenty of race hazards. If it messes up,
         # it will likely get caught the next time.
-        if len(os.listdir(path)) == 0:
-            logger.info(f"Skipping (empty directory)   : {init_path}")
-            continue
         if init_path.is_file() and not init_path.is_symlink():
             logger.info(f"Found   : {init_path}")
             continue
         elif not init_path.exists():
             failed = True
             init_path.touch()
             logger.warning(f"Created : {init_path}")
         else:
             failed = True
-            logger.error(f"Fail    : present but not a regular file: {init_path}", file=sys.stderr)
+            logger.error(f"Fail    : present but not a regular file: {init_path}")
 
     if failed:
         raise click.ClickException("At least one __init__.py created or not a regular file")
 
 
 command()  # pylint: disable=no-value-for-parameter
```

### Comparing `chia-blockchain-1.8.1rc2/tests/build-job-matrix.py` & `chia-blockchain-2.0.0b1/tests/build-job-matrix.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/check_pytest_monitor_output.py` & `chia-blockchain-2.0.0b1/tests/check_pytest_monitor_output.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/check_sql_statements.py` & `chia-blockchain-2.0.0b1/tests/check_sql_statements.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/chia-start-sim` & `chia-blockchain-2.0.0b1/tests/chia-start-sim`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/benchmark_costs.py` & `chia-blockchain-2.0.0b1/tests/clvm/benchmark_costs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/coin_store.py` & `chia-blockchain-2.0.0b1/tests/clvm/coin_store.py`

 * *Files 2% similar despite different names*

```diff
@@ -55,15 +55,15 @@
         return coin
 
     def validate_spend_bundle(self, spend_bundle: SpendBundle, now: CoinTimestamp, max_cost: int) -> int:
         # this should use blockchain consensus code
 
         program = simple_solution_generator(spend_bundle)
         # always use the post soft-fork2 semantics
-        result: NPCResult = get_name_puzzle_conditions(program, max_cost, mempool_mode=True, height=uint32(3886635))
+        result: NPCResult = get_name_puzzle_conditions(program, max_cost, mempool_mode=True, height=uint32(4000000))
         if result.error is not None:
             raise BadSpendBundleError(f"condition validation failure {Err(result.error)}")
 
         ephemeral_db = dict(self._db)
         assert result.conds is not None
         for spend in result.conds.spends:
             for puzzle_hash, amount, hint in spend.create_coin:
```

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_chialisp_deserialization.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_chialisp_deserialization.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_clvm_step.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_clvm_step.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_curry_and_treehash.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_curry_and_treehash.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_program.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_program.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_puzzle_compression.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_puzzle_compression.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_puzzle_drivers.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_puzzle_drivers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_puzzles.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_puzzles.py`

 * *Files 0% similar despite different names*

```diff
@@ -97,15 +97,15 @@
 ) -> Tuple[List[Tuple[bytes32, int]], Program]:
     # the coin we get from coin_db.farm_coin only has amount 1024, so we can
     # only make small payments to avoid failing with MINTING_COIN
     payments = [
         (throwaway_puzzle_hash(initial_index + 1, key_lookup), initial_index * 10),
         (throwaway_puzzle_hash(initial_index + 2, key_lookup), (initial_index + 1) * 10),
     ]
-    conditions = Program.to([make_create_coin_condition(ph, amount, None) for ph, amount in payments])
+    conditions = Program.to([make_create_coin_condition(ph, amount, []) for ph, amount in payments])
     return payments, conditions
 
 
 class TestPuzzles(TestCase):
     def test_p2_conditions(self):
         key_lookup = KeyTool()
         payments, conditions = default_payments_and_conditions(1, key_lookup)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_serialized_program.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_serialized_program.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_singletons.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_singletons.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/clvm/test_spend_sim.py` & `chia-blockchain-2.0.0b1/tests/clvm/test_spend_sim.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/cmds/test_sim.py` & `chia-blockchain-2.0.0b1/tests/cmds/test_sim.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/cmds/test_wallet_check.py` & `chia-blockchain-2.0.0b1/tests/cmds/test_wallet_check.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/conftest.py` & `chia-blockchain-2.0.0b1/tests/conftest.py`

 * *Files 0% similar despite different names*

```diff
@@ -129,15 +129,15 @@
 
 
 @pytest.fixture(scope="function", params=[1, 2])
 def db_version(request) -> int:
     return request.param
 
 
-@pytest.fixture(scope="function", params=[1000000, 3630000, 3886635])
+@pytest.fixture(scope="function", params=[1000000, 3630000, 4000000])
 def softfork_height(request) -> int:
     return request.param
 
 
 saved_blocks_version = "rc5"
```

### Comparing `chia-blockchain-1.8.1rc2/tests/connection_utils.py` & `chia-blockchain-2.0.0b1/tests/connection_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/cmds/test_beta.py` & `chia-blockchain-2.0.0b1/tests/core/cmds/test_beta.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/cmds/test_keys.py` & `chia-blockchain-2.0.0b1/tests/core/cmds/test_keys.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/cmds/test_wallet.py` & `chia-blockchain-2.0.0b1/tests/core/cmds/test_wallet.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/consensus/test_pot_iterations.py` & `chia-blockchain-2.0.0b1/tests/core/consensus/test_pot_iterations.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/custom_types/test_coin.py` & `chia-blockchain-2.0.0b1/tests/core/custom_types/test_coin.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/custom_types/test_proof_of_space.py` & `chia-blockchain-2.0.0b1/tests/core/custom_types/test_proof_of_space.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/custom_types/test_spend_bundle.py` & `chia-blockchain-2.0.0b1/tests/core/custom_types/test_spend_bundle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/daemon/test_daemon.py` & `chia-blockchain-2.0.0b1/tests/core/daemon/test_daemon.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/daemon/test_daemon_register.py` & `chia-blockchain-2.0.0b1/tests/core/daemon/test_daemon_register.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/daemon/test_keychain_proxy.py` & `chia-blockchain-2.0.0b1/tests/core/daemon/test_keychain_proxy.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/conftest.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/conftest.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_cli.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_cli.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_layer_util.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_layer_util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_rpc.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_store.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/test_data_store_schema.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/test_data_store_schema.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/data_layer/util.py` & `chia-blockchain-2.0.0b1/tests/core/data_layer/util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/conftest.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/conftest.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/full_sync/test_full_sync.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/full_sync/test_full_sync.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/ram_db.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/ram_db.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_block_store.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_block_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_coin_store.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_coin_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_full_node_store.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_full_node_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_hint_store.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_hint_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/stores/test_sync_store.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/stores/test_sync_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_address_manager.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_address_manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_block_height_map.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_block_height_map.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_conditions.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_conditions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_full_node.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_full_node.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_generator_tools.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_generator_tools.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_hint_management.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_hint_management.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_node_load.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_node_load.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_peer_store_resolver.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_peer_store_resolver.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_performance.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_performance.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_subscriptions.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_subscriptions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_transactions.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_transactions.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/full_node/test_tx_processing_queue.py` & `chia-blockchain-2.0.0b1/tests/core/full_node/test_tx_processing_queue.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/large_block.py` & `chia-blockchain-2.0.0b1/tests/core/large_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/make_block_generator.py` & `chia-blockchain-2.0.0b1/tests/core/make_block_generator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool.py` & `chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool.py`

 * *Files 1% similar despite different names*

```diff
@@ -2682,27 +2682,27 @@
                 mk_item(coins[1:2], fee=0, cost=50),
                 mk_item(coins[0:1], fee=0, cost=50),
             ],
             [coins[2], coins[1], coins[0]],
         ),
     ],
 )
-def test_spends_by_feerate(items: List[MempoolItem], expected: List[Coin]) -> None:
+def test_items_by_feerate(items: List[MempoolItem], expected: List[Coin]) -> None:
     fee_estimator = create_bitcoin_fee_estimator(uint64(11000000000))
 
     mempool_info = MempoolInfo(
         CLVMCost(uint64(11000000000 * 3)),
         FeeRate(uint64(1000000)),
         CLVMCost(uint64(11000000000)),
     )
     mempool = Mempool(mempool_info, fee_estimator)
     for i in items:
         mempool.add_to_pool(i)
 
-    ordered_items = list(mempool.spends_by_feerate())
+    ordered_items = list(mempool.items_by_feerate())
 
     assert len(ordered_items) == len(expected)
 
     last_fpc: Optional[float] = None
     for mi, expected_coin in zip(ordered_items, expected):
         assert len(mi.spend_bundle.coin_spends) == 1
         assert mi.spend_bundle.coin_spends[0].coin == expected_coin
@@ -2752,15 +2752,15 @@
     for i in items:
         mempool.add_to_pool(item_cost(i, fee_rate))
         fee_rate -= 0.1
 
     # now, add the item we're testing
     mempool.add_to_pool(item_cost(add, 3.1))
 
-    ordered_items = list(mempool.spends_by_feerate())
+    ordered_items = list(mempool.items_by_feerate())
 
     assert len(ordered_items) == len(expected)
 
     for mi, expected_cost in zip(ordered_items, expected):
         assert mi.cost == expected_cost
 
 
@@ -2814,22 +2814,59 @@
             fee_rate += 0.1
             assert ret is None
         else:
             fee_rate -= 0.1
 
     ordered_costs = [
         item.cost
-        for item in mempool.spends_by_feerate()
+        for item in mempool.items_by_feerate()
         if item.assert_before_height is not None or item.assert_before_seconds is not None
     ]
 
     assert ordered_costs == expected
 
     print("")
-    for item in mempool.spends_by_feerate():
+    for item in mempool.items_by_feerate():
         if item.assert_before_seconds is not None or item.assert_before_height is not None:
             ttl = "yes"
         else:
             ttl = "No"
         print(f"- cost: {item.cost} TTL: {ttl}")
 
     assert mempool.total_mempool_cost() > 90
+
+
+@pytest.mark.parametrize(
+    "items,coin_ids,expected",
+    [
+        # None of these spend those coins
+        (
+            [mk_item(coins[0:1]), mk_item(coins[1:2]), mk_item(coins[2:3])],
+            [coins[3].name(), coins[4].name()],
+            [],
+        ),
+        # One of these spends one of the coins
+        (
+            [mk_item(coins[0:1]), mk_item(coins[1:2]), mk_item(coins[2:3])],
+            [coins[1].name(), coins[3].name()],
+            [mk_item(coins[1:2])],
+        ),
+        # One of these spends one another spends two
+        (
+            [mk_item(coins[0:1]), mk_item(coins[1:3]), mk_item(coins[2:4]), mk_item(coins[3:4])],
+            [coins[2].name(), coins[3].name()],
+            [mk_item(coins[1:3]), mk_item(coins[2:4]), mk_item(coins[3:4])],
+        ),
+    ],
+)
+def test_get_items_by_coin_ids(items: List[MempoolItem], coin_ids: List[bytes32], expected: List[MempoolItem]) -> None:
+    fee_estimator = create_bitcoin_fee_estimator(uint64(11000000000))
+    mempool_info = MempoolInfo(
+        CLVMCost(uint64(11000000000 * 3)),
+        FeeRate(uint64(1000000)),
+        CLVMCost(uint64(11000000000)),
+    )
+    mempool = Mempool(mempool_info, fee_estimator)
+    for i in items:
+        mempool.add_to_pool(i)
+    result = mempool.get_items_by_coin_ids(coin_ids)
+    assert set(result) == set(expected)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_fee_estimator.py` & `chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_fee_estimator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_fee_protocol.py` & `chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_fee_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_manager.py` & `chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_manager.py`

 * *Files 0% similar despite different names*

```diff
@@ -774,15 +774,15 @@
             mk_item(coins[0:1], fee=10000000, assert_height=200),
             False,
         ),
     ],
 )
 def test_can_replace(existing_items: List[MempoolItem], new_item: MempoolItem, expected: bool) -> None:
     removals = set(c.name() for c in new_item.spend_bundle.removals())
-    assert can_replace(set(existing_items), removals, new_item) == expected
+    assert can_replace(existing_items, removals, new_item) == expected
 
 
 @pytest.mark.asyncio
 async def test_get_items_not_in_filter() -> None:
     mempool_manager = await instantiate_mempool_manager(get_coin_record_for_test_coins)
     conditions = [[ConditionOpcode.CREATE_COIN, IDENTITY_PUZZLE_HASH, 1]]
     sb1, sb1_name, _ = await generate_and_add_spendbundle(mempool_manager, conditions)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/core/mempool/test_mempool_performance.py` & `chia-blockchain-2.0.0b1/tests/core/mempool/test_mempool_performance.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/node_height.py` & `chia-blockchain-2.0.0b1/tests/core/node_height.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/flood.py` & `chia-blockchain-2.0.0b1/tests/core/server/flood.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/serve.py` & `chia-blockchain-2.0.0b1/tests/core/server/serve.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_capabilities.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_capabilities.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_dos.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_dos.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_event_loop.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_event_loop.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_loop.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_loop.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_rate_limits.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_rate_limits.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/server/test_server.py` & `chia-blockchain-2.0.0b1/tests/core/server/test_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/ssl/test_ssl.py` & `chia-blockchain-2.0.0b1/tests/core/ssl/test_ssl.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_coins.py` & `chia-blockchain-2.0.0b1/tests/core/test_coins.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_cost_calculation.py` & `chia-blockchain-2.0.0b1/tests/core/test_cost_calculation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_crawler_rpc.py` & `chia-blockchain-2.0.0b1/tests/core/test_crawler_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_daemon_rpc.py` & `chia-blockchain-2.0.0b1/tests/core/test_daemon_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_db_conversion.py` & `chia-blockchain-2.0.0b1/tests/core/test_db_conversion.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_db_validation.py` & `chia-blockchain-2.0.0b1/tests/core/test_db_validation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_farmer_harvester_rpc.py` & `chia-blockchain-2.0.0b1/tests/core/test_farmer_harvester_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_filter.py` & `chia-blockchain-2.0.0b1/tests/core/test_filter.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_full_node_rpc.py` & `chia-blockchain-2.0.0b1/tests/core/test_full_node_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_merkle_set.py` & `chia-blockchain-2.0.0b1/tests/core/test_merkle_set.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/test_services.py` & `chia-blockchain-2.0.0b1/tests/core/test_services.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_cached_bls.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_cached_bls.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_config.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_config.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_file_keyring_synchronization.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_file_keyring_synchronization.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_files.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_files.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_jsonify.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_jsonify.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_keychain.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_keychain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_keyring_wrapper.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_keyring_wrapper.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_lockfile.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_lockfile.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_lru_cache.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_lru_cache.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_significant_bits.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_significant_bits.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/core/util/test_streamable.py` & `chia-blockchain-2.0.0b1/tests/core/util/test_streamable.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/db/test_db_wrapper.py` & `chia-blockchain-2.0.0b1/tests/db/test_db_wrapper.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/farmer_harvester/test_farmer_harvester.py` & `chia-blockchain-2.0.0b1/tests/farmer_harvester/test_farmer_harvester.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/fee_estimation/cmdline_test.py` & `chia-blockchain-2.0.0b1/tests/fee_estimation/cmdline_test.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_integration.py` & `chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_integration.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_rpc.py` & `chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/fee_estimation/test_fee_estimation_unit_tests.py` & `chia-blockchain-2.0.0b1/tests/fee_estimation/test_fee_estimation_unit_tests.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/fee_estimation/test_mempoolitem_height_added.py` & `chia-blockchain-2.0.0b1/tests/fee_estimation/test_mempoolitem_height_added.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/generator/test_compression.py` & `chia-blockchain-2.0.0b1/tests/generator/test_compression.py`

 * *Files 0% similar despite different names*

```diff
@@ -213,28 +213,28 @@
     #    cse0 = binutils.assemble("()")
     #    cost, out = DECOMPRESS_CSE.run_with_cost(INFINITE_COST, [DESERIALIZE_MOD, DECOMPRESS_PUZZLE, b"\xff", b"\x80", cse0])
     #    print()
     #    print(out)
 
     def test_decompress_cse(self) -> None:
         """Decompress a single CSE / CoinSpendEntry"""
-        cse0 = binutils.assemble(
+        cse0 = binutils.assemble(  # type: ignore[no-untyped-call]
             "((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0) (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3 (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ())))"
-        )  # type: ignore[no-untyped-call]
+        )
         cost, out = DECOMPRESS_CSE.run_with_cost(
             INFINITE_COST, [DESERIALIZE_MOD, DECOMPRESS_PUZZLE, b"\xff", b"\x80", cse0]
         )
 
         print()
         print(out)
 
     def test_decompress_cse_with_prefix(self) -> None:
-        cse0 = binutils.assemble(
+        cse0 = binutils.assemble(  # type: ignore[no-untyped-call]
             "((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0) (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3 (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ())))"
-        )  # type: ignore[no-untyped-call]
+        )
 
         start = 2 + 44
         end = start + 238
         prefix = original_generator[start:end]
         # (deserialize decompress_puzzle puzzle_prefix cse)
         cost, out = DECOMPRESS_CSE_WITH_PREFIX.run_with_cost(
             INFINITE_COST, [DESERIALIZE_MOD, DECOMPRESS_PUZZLE, prefix, cse0]
@@ -242,32 +242,32 @@
 
         print()
         print(out)
 
     def test_block_program_zero(self) -> None:
         "Decompress a list of CSEs"
         self.maxDiff = None
-        cse1 = binutils.assemble(
+        cse1 = binutils.assemble(  # type: ignore[no-untyped-call]
             "(((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0) (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3 (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ()))))"
-        )  # type: ignore[no-untyped-call]
-        cse2 = binutils.assemble(
+        )
+        cse2 = binutils.assemble(  # type: ignore[no-untyped-call]
             """
 (
   ((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0)
    (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3
     (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ()))
   )
 
   ((0x0000000000000000000000000000000000000000000000000000000000000001 0x0186a0)
    (0xb0a6207f5173ec41491d9f2c1b8fff5579e13703077e0eaca8fe587669dcccf51e9209a6b65576845ece5f7c2f3229e7e3
    (() (q (51 0x24254a3efc3ebfac9979bbe0d615e2eda043aa329905f65b63846fa24149e2b6 0x0186a0)) ())))
 
 )
         """
-        )  # type: ignore[no-untyped-call]
+        )
 
         start = 2 + 44
         end = start + 238
 
         # (mod (decompress_puzzle decompress_coin_spend_entry start end compressed_cses deserialize generator_list reserved_arg)
         # cost, out = DECOMPRESS_BLOCK.run_with_cost(INFINITE_COST, [DECOMPRESS_PUZZLE, DECOMPRESS_CSE, start, Program.to(end), cse0, DESERIALIZE_MOD, bytes(original_generator)])
         cost, out = DECOMPRESS_BLOCK.run_with_cost(
@@ -284,32 +284,32 @@
         )
 
         print()
         print(out)
 
     def test_block_program_zero_with_curry(self) -> None:
         self.maxDiff = None
-        cse1 = binutils.assemble(
+        cse1 = binutils.assemble(  # type: ignore[no-untyped-call]
             "(((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0) (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3 (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ()))))"
-        )  # type: ignore[no-untyped-call]
-        cse2 = binutils.assemble(
+        )
+        cse2 = binutils.assemble(  # type: ignore[no-untyped-call]
             """
 (
   ((0x0000000000000000000000000000000000000000000000000000000000000000 0x0186a0)
    (0xb081963921826355dcb6c355ccf9c2637c18adf7d38ee44d803ea9ca41587e48c913d8d46896eb830aeadfc13144a8eac3
     (() (q (51 0x6b7a83babea1eec790c947db4464ab657dbe9b887fe9acc247062847b8c2a8a9 0x0186a0)) ()))
   )
 
   ((0x0000000000000000000000000000000000000000000000000000000000000001 0x0186a0)
    (0xb0a6207f5173ec41491d9f2c1b8fff5579e13703077e0eaca8fe587669dcccf51e9209a6b65576845ece5f7c2f3229e7e3
    (() (q (51 0x24254a3efc3ebfac9979bbe0d615e2eda043aa329905f65b63846fa24149e2b6 0x0186a0)) ())))
 
 )
         """
-        )  # type: ignore[no-untyped-call]
+        )
 
         start = 2 + 44
         end = start + 238
 
         # (mod (decompress_puzzle decompress_coin_spend_entry start end compressed_cses deserialize generator_list reserved_arg)
         # cost, out = DECOMPRESS_BLOCK.run_with_cost(INFINITE_COST, [DECOMPRESS_PUZZLE, DECOMPRESS_CSE, start, Program.to(end), cse0, DESERIALIZE_MOD, bytes(original_generator)])
         p = DECOMPRESS_BLOCK.curry(DECOMPRESS_PUZZLE, DECOMPRESS_CSE_WITH_PREFIX, start, Program.to(end))
```

### Comparing `chia-blockchain-1.8.1rc2/tests/generator/test_generator_types.py` & `chia-blockchain-2.0.0b1/tests/generator/test_generator_types.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/generator/test_list_to_batches.py` & `chia-blockchain-2.0.0b1/tests/generator/test_list_to_batches.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/generator/test_rom.py` & `chia-blockchain-2.0.0b1/tests/generator/test_rom.py`

 * *Files 2% similar despite different names*

```diff
@@ -45,28 +45,28 @@
     "ff06ffff04ff02ffff04ff05ffff04ff0bff808080808080ffff04ffff01ffff02ff05ff"
     "1380ff02ff05ff2b80ff018080"
 )
 
 COMPILED_GENERATOR_CODE = bytes(Program.to(compile_clvm_text(GENERATOR_CODE, [])))  # type: ignore[no-untyped-call]
 
 FIRST_GENERATOR = Program.to(
-    binutils.assemble(
+    binutils.assemble(  # type: ignore[no-untyped-call]
         '((parent_id (c 1 (q "puzzle blob")) 50000 "solution is here" extra data for coin))'
-    )  # type: ignore[no-untyped-call]
+    )
 ).as_bin()
 
 SECOND_GENERATOR = Program.to(binutils.assemble("(extra data for block)")).as_bin()  # type: ignore[no-untyped-call]
 
 
 FIRST_GENERATOR = Program.to(
-    binutils.assemble(
+    binutils.assemble(  # type: ignore[no-untyped-call]
         """
         ((0x0000000000000000000000000000000000000000000000000000000000000000 1 50000
         ((51 0x0000000000000000000000000000000000000000000000000000000000000001 500))
-        "extra" "data" "for" "coin" ))"""  # type: ignore[no-untyped-call]
+        "extra" "data" "for" "coin" ))"""
     )
 ).as_bin()
 
 SECOND_GENERATOR = Program.to(binutils.assemble("(extra data for block)")).as_bin()  # type: ignore[no-untyped-call]
 
 
 def to_sp(sexp: bytes) -> SerializedProgram:
```

### Comparing `chia-blockchain-1.8.1rc2/tests/generator/test_scan.py` & `chia-blockchain-2.0.0b1/tests/generator/test_scan.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/test_delta.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/test_delta.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/test_plot_sync.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/test_plot_sync.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/test_receiver.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/test_receiver.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/test_sender.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/test_sender.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/test_sync_simulated.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/test_sync_simulated.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plot_sync/util.py` & `chia-blockchain-2.0.0b1/tests/plot_sync/util.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/plotting/test_plot_manager.py` & `chia-blockchain-2.0.0b1/tests/plotting/test_plot_manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_pool_cmdline.py` & `chia-blockchain-2.0.0b1/tests/pools/test_pool_cmdline.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_pool_config.py` & `chia-blockchain-2.0.0b1/tests/pools/test_pool_config.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_pool_puzzles_lifecycle.py` & `chia-blockchain-2.0.0b1/tests/pools/test_pool_puzzles_lifecycle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_pool_rpc.py` & `chia-blockchain-2.0.0b1/tests/pools/test_pool_rpc.py`

 * *Files 0% similar despite different names*

```diff
@@ -60,19 +60,19 @@
     bt: BlockTools,
     p2_singleton_puzzle_hash: bytes32,
 ) -> AsyncIterator[TemporaryPoolPlot]:
     with tempfile.TemporaryDirectory() as tmpdir:
         tmp_path: Path = Path(tmpdir)
         bt.add_plot_directory(tmp_path)
         bt_plot = await bt.new_plot(p2_singleton_puzzle_hash, tmp_path, tmp_dir=tmp_path)
-        await bt.refresh_plots()
+        try:
+            await bt.refresh_plots()
 
-        plot = TemporaryPoolPlot(bt=bt, p2_singleton_puzzle_hash=p2_singleton_puzzle_hash, plot_id=bt_plot.plot_id)
+            plot = TemporaryPoolPlot(bt=bt, p2_singleton_puzzle_hash=p2_singleton_puzzle_hash, plot_id=bt_plot.plot_id)
 
-        try:
             yield plot
         finally:
             await bt.delete_plot(bt_plot.plot_id)
 
 
 PREFARMED_BLOCKS = 4
```

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_pool_wallet.py` & `chia-blockchain-2.0.0b1/tests/pools/test_pool_wallet.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/pools/test_wallet_pool_store.py` & `chia-blockchain-2.0.0b1/tests/pools/test_wallet_pool_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/simulation/test_simulation.py` & `chia-blockchain-2.0.0b1/tests/simulation/test_simulation.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/simulation/test_simulator.py` & `chia-blockchain-2.0.0b1/tests/simulation/test_simulator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/simulation/test_start_simulator.py` & `chia-blockchain-2.0.0b1/tests/simulation/test_start_simulator.py`

 * *Files 1% similar despite different names*

```diff
@@ -87,15 +87,15 @@
         old_blocks = await simulator_rpc_client.get_all_blocks()
         assert len(old_blocks) == 5
 
         # Sometimes in CI reorg_blocks takes a long time and the RPC times out
         # We can ignore this timeout as long as the subsequent tests pass
         try:
             await simulator_rpc_client.reorg_blocks(2)  # fork point 2 blocks, now height is 5
-        except asyncio.exceptions.TimeoutError:
+        except asyncio.TimeoutError:
             pass  # ignore this error and hope the reorg is going ahead
 
         # wait up to 5 mins
         await time_out_assert(300, simulator.full_node.blockchain.get_peak_height, 5)
         # now validate that the blocks don't match
         assert (await simulator.get_all_full_blocks())[0:4] != old_blocks
         # test block deletion
```

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/1315537.json` & `chia-blockchain-2.0.0b1/tests/tools/1315537.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/1315544.json` & `chia-blockchain-2.0.0b1/tests/tools/1315544.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/1315630.json` & `chia-blockchain-2.0.0b1/tests/tools/1315630.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/300000.json` & `chia-blockchain-2.0.0b1/tests/tools/300000.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/442734.json` & `chia-blockchain-2.0.0b1/tests/tools/442734.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/466212.json` & `chia-blockchain-2.0.0b1/tests/tools/466212.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/test-blockchain-db.sqlite` & `chia-blockchain-2.0.0b1/tests/tools/test-blockchain-db.sqlite`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/test_full_sync.py` & `chia-blockchain-2.0.0b1/tests/tools/test_full_sync.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/test_legacy_keyring.py` & `chia-blockchain-2.0.0b1/tests/tools/test_legacy_keyring.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/tools/test_run_block.py` & `chia-blockchain-2.0.0b1/tests/tools/test_run_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/alert_server.py` & `chia-blockchain-2.0.0b1/tests/util/alert_server.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/benchmark_cost.py` & `chia-blockchain-2.0.0b1/tests/util/benchmark_cost.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/bip39_test_vectors.json` & `chia-blockchain-2.0.0b1/tests/util/bip39_test_vectors.json`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/blockchain.py` & `chia-blockchain-2.0.0b1/tests/util/blockchain.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 from __future__ import annotations
 
 import os
 import pickle
 import tempfile
 from pathlib import Path
-from typing import List, Optional
+from typing import List, Optional, Tuple
 
 from chia.consensus.blockchain import Blockchain
 from chia.consensus.constants import ConsensusConstants
 from chia.full_node.block_store import BlockStore
 from chia.full_node.coin_store import CoinStore
 from chia.simulator.block_tools import BlockTools
 from chia.types.full_block import FullBlock
 from chia.util.db_wrapper import DBWrapper2
 from chia.util.default_root import DEFAULT_ROOT_PATH
 
 
-async def create_blockchain(constants: ConsensusConstants, db_version: int):
+async def create_blockchain(constants: ConsensusConstants, db_version: int) -> Tuple[Blockchain, DBWrapper2, Path]:
     db_path = Path(tempfile.NamedTemporaryFile().name)
 
     if db_path.exists():
         db_path.unlink()
     wrapper = await DBWrapper2.create(database=db_path, reader_count=1, db_version=db_version)
 
     coin_store = await CoinStore.create(wrapper)
@@ -31,22 +31,22 @@
 
 
 def persistent_blocks(
     num_of_blocks: int,
     db_name: str,
     bt: BlockTools,
     seed: bytes = b"",
-    empty_sub_slots=0,
+    empty_sub_slots: int = 0,
     normalized_to_identity_cc_eos: bool = False,
     normalized_to_identity_icc_eos: bool = False,
     normalized_to_identity_cc_sp: bool = False,
     normalized_to_identity_cc_ip: bool = False,
-    block_list_input: List[FullBlock] = None,
+    block_list_input: Optional[List[FullBlock]] = None,
     time_per_block: Optional[float] = None,
-):
+) -> List[FullBlock]:
     # try loading from disc, if not create new blocks.db file
     # TODO hash fixtures.py and blocktool.py, add to path, delete if the files changed
     if block_list_input is None:
         block_list_input = []
     block_path_dir = DEFAULT_ROOT_PATH.parent.joinpath("blocks")
     file_path = block_path_dir.joinpath(db_name)
 
@@ -96,15 +96,15 @@
     bt: BlockTools,
     block_list_input: List[FullBlock],
     time_per_block: Optional[float],
     normalized_to_identity_cc_eos: bool = False,  # CC_EOS,
     normalized_to_identity_icc_eos: bool = False,  # ICC_EOS
     normalized_to_identity_cc_sp: bool = False,  # CC_SP,
     normalized_to_identity_cc_ip: bool = False,  # CC_IP
-):
+) -> List[FullBlock]:
     print(f"create {path} with {num_of_blocks} blocks with ")
     blocks: List[FullBlock] = bt.get_consecutive_blocks(
         num_of_blocks,
         block_list_input=block_list_input,
         time_per_block=time_per_block,
         seed=seed,
         skip_slots=empty_sub_slots,
```

### Comparing `chia-blockchain-1.8.1rc2/tests/util/build_network_protocol_files.py` & `chia-blockchain-2.0.0b1/tests/util/build_network_protocol_files.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/db_connection.py` & `chia-blockchain-2.0.0b1/tests/util/db_connection.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/gen_ssl_certs.py` & `chia-blockchain-2.0.0b1/tests/util/gen_ssl_certs.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/generator_tools_testing.py` & `chia-blockchain-2.0.0b1/tests/util/generator_tools_testing.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/key_tool.py` & `chia-blockchain-2.0.0b1/tests/util/key_tool.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/misc.py` & `chia-blockchain-2.0.0b1/tests/util/misc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/network_protocol_data.py` & `chia-blockchain-2.0.0b1/tests/util/network_protocol_data.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/protocol_messages_bytes-v1.0` & `chia-blockchain-2.0.0b1/tests/util/protocol_messages_bytes-v1.0`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/protocol_messages_json.py` & `chia-blockchain-2.0.0b1/tests/util/protocol_messages_json.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/rpc.py` & `chia-blockchain-2.0.0b1/tests/util/rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_chunks.py` & `chia-blockchain-2.0.0b1/tests/util/test_chunks.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_full_block_utils.py` & `chia-blockchain-2.0.0b1/tests/util/test_full_block_utils.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_limited_semaphore.py` & `chia-blockchain-2.0.0b1/tests/util/test_limited_semaphore.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_lock_queue.py` & `chia-blockchain-2.0.0b1/tests/util/test_lock_queue.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_logging_filter.py` & `chia-blockchain-2.0.0b1/tests/util/test_logging_filter.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_misc.py` & `chia-blockchain-2.0.0b1/tests/util/test_misc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_network.py` & `chia-blockchain-2.0.0b1/tests/util/test_network.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_files.py` & `chia-blockchain-2.0.0b1/tests/util/test_network_protocol_files.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_json.py` & `chia-blockchain-2.0.0b1/tests/util/test_network_protocol_json.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_network_protocol_test.py` & `chia-blockchain-2.0.0b1/tests/util/test_network_protocol_test.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 # flake8: noqa
 from __future__ import annotations
 
-from typing import Any, List, Set
+import ast
+import inspect
+from typing import Any, Set, cast
 
 from chia.protocols import (
     farmer_protocol,
     full_node_protocol,
     harvester_protocol,
     introducer_protocol,
     pool_protocol,
@@ -15,24 +17,24 @@
 )
 
 # this test is to ensure the network protocol message regression test always
 # stays up to date. It's a test for the test
 
 
 def types_in_module(mod: Any) -> Set[str]:
-    ret: List[str] = []
-    mod_name = mod.__name__
-    for sym in dir(mod):
-        obj = getattr(mod, sym)
-        if hasattr(obj, "__module__") and obj.__module__ == mod_name:
-            ret.append(sym)
-
-    if hasattr(mod, "__all__"):
-        ret += getattr(mod, "__all__")
-    return set(ret)
+    parsed = ast.parse(inspect.getsource(mod))
+    types = set()
+    for line in parsed.body:
+        if isinstance(line, ast.Assign):
+            name = cast(ast.Name, line.targets[0])
+            if inspect.isclass(getattr(mod, name.id)):
+                types.add(name.id)
+        elif isinstance(line, ast.ClassDef):
+            types.add(line.name)
+    return types
 
 
 def test_missing_messages_state_machine() -> None:
     from chia.protocols.protocol_state_machine import NO_REPLY_EXPECTED, VALID_REPLY_MESSAGE_MAP
 
     # if these asserts fail, make sure to add the new network protocol messages
     # to the visitor in build_network_protocol_files.py and rerun it. Then
@@ -151,16 +153,14 @@
         "PostFarmerResponse",
         "PostPartialPayload",
         "PostPartialRequest",
         "PostPartialResponse",
         "PutFarmerPayload",
         "PutFarmerRequest",
         "PutFarmerResponse",
-        "get_current_authentication_token",
-        "validate_authentication_token",
     }
 
     timelord_msgs = {
         "NewEndOfSubSlotVDF",
         "NewInfusionPointVDF",
         "NewPeakTimelord",
         "NewSignagePointVDF",
```

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_paginator.py` & `chia-blockchain-2.0.0b1/tests/util/test_paginator.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_pprint.py` & `chia-blockchain-2.0.0b1/tests/util/test_pprint.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_struct_stream.py` & `chia-blockchain-2.0.0b1/tests/util/test_struct_stream.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/util/test_trusted_peer.py` & `chia-blockchain-2.0.0b1/tests/util/test_trusted_peer.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_lifecycle.py` & `chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_lifecycle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_outer_puzzle.py` & `chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_cat_wallet.py` & `chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_cat_wallet.py`

 * *Files 9% similar despite different names*

```diff
@@ -3,25 +3,37 @@
 import asyncio
 from typing import List
 
 import pytest
 
 from chia.consensus.block_rewards import calculate_base_farmer_reward, calculate_pool_reward
 from chia.rpc.wallet_rpc_api import WalletRpcApi
+from chia.rpc.wallet_rpc_client import WalletRpcClient
+from chia.simulator.full_node_simulator import FullNodeSimulator
+from chia.simulator.setup_nodes import SimulatorsAndWalletsServices
 from chia.simulator.simulator_protocol import FarmNewBlockProtocol, ReorgProtocol
-from chia.simulator.time_out_assert import time_out_assert
-from chia.types.blockchain_format.coin import Coin
+from chia.simulator.time_out_assert import time_out_assert, time_out_assert_not_none
+from chia.types.blockchain_format.coin import Coin, coin_as_list
+from chia.types.blockchain_format.program import Program
+from chia.types.blockchain_format.sized_bytes import bytes32
+from chia.types.coin_spend import CoinSpend
 from chia.types.peer_info import PeerInfo
+from chia.util.bech32m import encode_puzzle_hash
 from chia.util.ints import uint16, uint32, uint64
 from chia.wallet.cat_wallet.cat_constants import DEFAULT_CATS
 from chia.wallet.cat_wallet.cat_info import LegacyCATInfo
 from chia.wallet.cat_wallet.cat_utils import construct_cat_puzzle
 from chia.wallet.cat_wallet.cat_wallet import CATWallet
+from chia.wallet.derivation_record import DerivationRecord
+from chia.wallet.derive_keys import _derive_path_unhardened, master_sk_to_wallet_sk_unhardened_intermediate
+from chia.wallet.lineage_proof import LineageProof
 from chia.wallet.puzzles.cat_loader import CAT_MOD
+from chia.wallet.puzzles.p2_delegated_puzzle_or_hidden_puzzle import puzzle_hash_for_pk
 from chia.wallet.transaction_record import TransactionRecord
+from chia.wallet.util.wallet_types import WalletType
 from chia.wallet.wallet_info import WalletInfo
 
 
 class TestCATWallet:
     @pytest.mark.parametrize(
         "trusted",
         [True, False],
@@ -200,15 +212,15 @@
                 tx_id = tx_record.name.hex()
                 assert tx_record.to_puzzle_hash == cat_2_hash
 
         await time_out_assert(15, full_node_api.txs_in_mempool, True, tx_records)
 
         await time_out_assert(20, cat_wallet.get_pending_change_balance, 40)
         memos = await api_0.get_transaction_memo(dict(transaction_id=tx_id))
-        assert len(memos[tx_id]) == 1
+        assert len(memos[tx_id]) == 2  # One for tx, one for change
         assert list(memos[tx_id].values())[0][0] == cat_2_hash.hex()
 
         for i in range(1, num_blocks):
             await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(32 * b"\0"))
 
         await time_out_assert(30, wallet.get_confirmed_balance, funds - 101)
 
@@ -218,15 +230,15 @@
         await time_out_assert(30, cat_wallet_2.get_confirmed_balance, 60)
         await time_out_assert(30, cat_wallet_2.get_unconfirmed_balance, 60)
         coins = await cat_wallet_2.select_coins(uint64(60))
         assert len(coins) == 1
         coin = coins.pop()
         tx_id = coin.name().hex()
         memos = await api_1.get_transaction_memo(dict(transaction_id=tx_id))
-        assert len(memos[tx_id]) == 1
+        assert len(memos[tx_id]) == 2
         assert list(memos[tx_id].values())[0][0] == cat_2_hash.hex()
         cat_hash = await cat_wallet.get_new_inner_hash()
         tx_records = await cat_wallet_2.generate_signed_transaction([uint64(15)], [cat_hash])
         for tx_record in tx_records:
             await wallet.wallet_state_manager.add_pending_transaction(tx_record)
 
         await time_out_assert(15, full_node_api.txs_in_mempool, True, tx_records)
@@ -601,15 +613,15 @@
         for tx_record in tx_records_3:
             await wallet_1.wallet_state_manager.add_pending_transaction(tx_record)
         await time_out_assert(15, full_node_api.txs_in_mempool, True, tx_records_3)
         txs = await wallet_1.wallet_state_manager.tx_store.get_transactions_between(cat_wallet_1.id(), 0, 100000)
         for tx in txs:
             if tx.amount == 30:
                 memos = tx.get_memos()
-                assert len(memos) == 1
+                assert len(memos) == 2  # One for tx, one for change
                 assert b"Markus Walburg" in [v for v_list in memos.values() for v in v_list]
                 assert list(memos.keys())[0] in [a.name() for a in tx.spend_bundle.additions()]
 
     @pytest.mark.parametrize(
         "trusted",
         [True, False],
     )
@@ -823,7 +835,168 @@
         for tx_record in tx_records:
             await wallet.wallet_state_manager.add_pending_transaction(tx_record)
 
         await full_node_api.process_transaction_records(records=tx_records)
 
         await time_out_assert(20, cat_wallet.get_confirmed_balance, 35)
         await time_out_assert(20, cat_wallet.get_unconfirmed_balance, 35)
+
+    @pytest.mark.parametrize(
+        "trusted",
+        [True, False],
+    )
+    @pytest.mark.asyncio
+    async def test_cat_change_detection(
+        self, self_hostname: str, one_wallet_and_one_simulator_services: SimulatorsAndWalletsServices, trusted: bool
+    ) -> None:
+        num_blocks = 1
+        full_nodes, wallets, bt = one_wallet_and_one_simulator_services
+        full_node_api: FullNodeSimulator = full_nodes[0]._api
+        full_node_server = full_node_api.full_node.server
+        wallet_service_0 = wallets[0]
+        wallet_node_0 = wallet_service_0._node
+        wallet_0 = wallet_node_0.wallet_state_manager.main_wallet
+
+        assert wallet_service_0.rpc_server is not None
+
+        client_0 = await WalletRpcClient.create(
+            bt.config["self_hostname"],
+            wallet_service_0.rpc_server.listen_port,
+            wallet_service_0.root_path,
+            wallet_service_0.config,
+        )
+        wallet_node_0.config["automatically_add_unknown_cats"] = True
+
+        if trusted:
+            wallet_node_0.config["trusted_peers"] = {
+                full_node_api.full_node.server.node_id.hex(): full_node_api.full_node.server.node_id.hex()
+            }
+        else:
+            wallet_node_0.config["trusted_peers"] = {}
+
+        await wallet_node_0.server.start_client(PeerInfo(self_hostname, uint16(full_node_server._port)), None)
+        await full_node_api.farm_blocks_to_wallet(count=num_blocks, wallet=wallet_0)
+        await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node_0, timeout=20)
+
+        # Mint CAT to ourselves, immediately spend it to an unhinted puzzle hash that we have manually added to the DB
+        # We should pick up this coin as balance even though it is unhinted because it is "change"
+        intermediate_sk_un = master_sk_to_wallet_sk_unhardened_intermediate(
+            wallet_node_0.wallet_state_manager.private_key
+        )
+        pubkey_unhardened = _derive_path_unhardened(intermediate_sk_un, [100000000]).get_g1()
+        inner_puzhash = puzzle_hash_for_pk(pubkey_unhardened)
+        puzzlehash_unhardened = construct_cat_puzzle(
+            CAT_MOD,
+            Program.to(None).get_tree_hash(),
+            inner_puzhash,  # type: ignore[arg-type]
+        ).get_tree_hash_precalc(inner_puzhash)
+        change_derivation = DerivationRecord(
+            uint32(0),
+            puzzlehash_unhardened,
+            pubkey_unhardened,
+            WalletType.CAT,
+            uint32(2),
+            False,
+        )
+        # Insert the derivation record before the wallet exists so that it is not subscribed to
+        await wallet_node_0.wallet_state_manager.puzzle_store.add_derivation_paths([change_derivation])
+        our_puzzle: Program = await wallet_0.get_new_puzzle()
+        cat_puzzle: Program = construct_cat_puzzle(
+            CAT_MOD,
+            Program.to(None).get_tree_hash(),
+            Program.to(1),
+        )
+        addr = encode_puzzle_hash(cat_puzzle.get_tree_hash(), "txch")
+        cat_amount_0 = uint64(100)
+        cat_amount_1 = uint64(5)
+
+        tx = await client_0.send_transaction(1, cat_amount_0, addr)
+        spend_bundle = tx.spend_bundle
+        assert spend_bundle is not None
+
+        await time_out_assert_not_none(5, full_node_api.full_node.mempool_manager.get_spendbundle, spend_bundle.name())
+        await full_node_api.farm_blocks_to_wallet(count=num_blocks, wallet=wallet_0)
+        await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node_0, timeout=20)
+
+        # Do the eve spend back to our wallet and add the CR layer
+        cat_coin = next(c for c in spend_bundle.additions() if c.amount == cat_amount_0)
+        next_coin = Coin(
+            cat_coin.name(),
+            construct_cat_puzzle(
+                CAT_MOD,
+                Program.to(None).get_tree_hash(),
+                our_puzzle,
+            ).get_tree_hash(),
+            cat_amount_0,
+        )
+        eve_spend = await wallet_node_0.wallet_state_manager.main_wallet.sign_transaction(
+            [
+                CoinSpend(
+                    cat_coin,
+                    cat_puzzle,
+                    Program.to(
+                        [
+                            Program.to(
+                                [
+                                    [
+                                        51,
+                                        our_puzzle.get_tree_hash(),
+                                        cat_amount_0,
+                                        [our_puzzle.get_tree_hash()],
+                                    ],
+                                    [51, None, -113, None, None],
+                                ]
+                            ),
+                            None,
+                            cat_coin.name(),
+                            coin_as_list(cat_coin),
+                            [cat_coin.parent_coin_info, Program.to(1).get_tree_hash(), cat_coin.amount],
+                            0,
+                            0,
+                        ]
+                    ),
+                ),
+                CoinSpend(
+                    next_coin,
+                    construct_cat_puzzle(
+                        CAT_MOD,
+                        Program.to(None).get_tree_hash(),
+                        our_puzzle,
+                    ),
+                    Program.to(
+                        [
+                            [
+                                None,
+                                (
+                                    1,
+                                    [
+                                        [51, inner_puzhash, cat_amount_1],
+                                        [51, bytes32([0] * 32), cat_amount_0 - cat_amount_1],
+                                    ],
+                                ),
+                                None,
+                            ],
+                            LineageProof(
+                                cat_coin.parent_coin_info, Program.to(1).get_tree_hash(), cat_amount_0
+                            ).to_program(),
+                            next_coin.name(),
+                            coin_as_list(next_coin),
+                            [next_coin.parent_coin_info, our_puzzle.get_tree_hash(), next_coin.amount],
+                            0,
+                            0,
+                        ]
+                    ),
+                ),
+            ],
+        )
+        await client_0.push_tx(eve_spend)
+        await time_out_assert_not_none(5, full_node_api.full_node.mempool_manager.get_spendbundle, eve_spend.name())
+        await full_node_api.farm_blocks_to_wallet(count=num_blocks, wallet=wallet_0)
+        await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node_0, timeout=20)
+
+        async def check_wallets(node):
+            return len(node.wallet_state_manager.wallets.keys())
+
+        await time_out_assert(20, check_wallets, 2, wallet_node_0)
+        cat_wallet = wallet_node_0.wallet_state_manager.wallets[uint32(2)]
+        await time_out_assert(20, cat_wallet.get_confirmed_balance, cat_amount_1)
+        assert not full_node_api.full_node.subscriptions.has_ph_subscription(puzzlehash_unhardened)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_offer_lifecycle.py` & `chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_offer_lifecycle.py`

 * *Files 2% similar despite different names*

```diff
@@ -56,30 +56,30 @@
     payments: List[Payment] = []
     cat_bundles: List[SpendBundle] = []
     for tail_str, amounts in requested_coins.items():
         for amount in amounts:
             if tail_str:
                 tail: Program = str_to_tail(tail_str)  # Making a fake but unique TAIL
                 cat_puzzle: Program = construct_cat_puzzle(CAT_MOD, tail.get_tree_hash(), acs)
-                payments.append(Payment(cat_puzzle.get_tree_hash(), amount, []))
+                payments.append(Payment(cat_puzzle.get_tree_hash(), amount))
                 cat_bundles.append(
                     unsigned_spend_bundle_for_spendable_cats(
                         CAT_MOD,
                         [
                             SpendableCAT(
                                 Coin(parent_coin.name(), cat_puzzle.get_tree_hash(), amount),
                                 tail.get_tree_hash(),
                                 acs,
                                 Program.to([[51, acs_ph, amount], [51, 0, -113, tail, []]]),
                             )
                         ],
                     )
                 )
             else:
-                payments.append(Payment(acs_ph, amount, []))
+                payments.append(Payment(acs_ph, amount))
 
     # This bundle creates all of the initial coins
     parent_bundle = SpendBundle(
         [
             CoinSpend(
                 parent_coin,
                 acs,
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/cat_wallet/test_trades.py` & `chia-blockchain-2.0.0b1/tests/wallet/cat_wallet/test_trades.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_db_graftroot.py` & `chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_db_graftroot.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_dl_offers.py` & `chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_dl_offers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/db_wallet/test_dl_wallet.py` & `chia-blockchain-2.0.0b1/tests/wallet/db_wallet/test_dl_wallet.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/did_wallet/test_did.py` & `chia-blockchain-2.0.0b1/tests/wallet/did_wallet/test_did.py`

 * *Files 1% similar despite different names*

```diff
@@ -1013,15 +1013,15 @@
         )
         await full_node_api.process_transaction_records(records=transaction_records)
         await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node, timeout=15)
 
         assert await did_wallet_1.get_confirmed_balance() == did_amount
         assert await did_wallet_1.get_unconfirmed_balance() == did_amount
         response = await api_0.did_get_info({"coin_id": did_wallet_1.did_info.origin_coin.name().hex()})
-
+        assert response["did_id"] == encode_puzzle_hash(did_wallet_1.did_info.origin_coin.name(), AddressType.DID.value)
         assert response["launcher_id"] == did_wallet_1.did_info.origin_coin.name().hex()
         assert response["full_puzzle"] == create_singleton_puzzle(
             did_wallet_1.did_info.current_inner, did_wallet_1.did_info.origin_coin.name()
         )
         assert response["metadata"]["twitter"] == "twitter"
         assert response["latest_coin"] == (await did_wallet_1.select_coins(uint64(1))).pop().name().hex()
         assert response["num_verification"] == 0
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_1_offers.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_1_offers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_bulk_mint.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_bulk_mint.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_lifecycle.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_lifecycle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_offers.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_offers.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_puzzles.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_puzzles.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_nft_wallet.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_nft_wallet.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/nft_wallet/test_ownership_outer_puzzle.py` & `chia-blockchain-2.0.0b1/tests/wallet/nft_wallet/test_ownership_outer_puzzle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/rpc/test_dl_wallet_rpc.py` & `chia-blockchain-2.0.0b1/tests/wallet/rpc/test_dl_wallet_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/rpc/test_wallet_rpc.py` & `chia-blockchain-2.0.0b1/tests/wallet/rpc/test_wallet_rpc.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/simple_sync/test_simple_sync_protocol.py` & `chia-blockchain-2.0.0b1/tests/wallet/simple_sync/test_simple_sync_protocol.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/sync/test_wallet_sync.py` & `chia-blockchain-2.0.0b1/tests/wallet/sync/test_wallet_sync.py`

 * *Files 2% similar despite different names*

```diff
@@ -24,18 +24,18 @@
 from chia.types.blockchain_format.program import Program
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.peer_info import PeerInfo
 from chia.util.block_cache import BlockCache
 from chia.util.hash import std_hash
 from chia.util.ints import uint16, uint32, uint64
 from chia.wallet.nft_wallet.nft_wallet import NFTWallet
+from chia.wallet.payment import Payment
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.wallet_sync_utils import PeerRequestException
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash
 from chia.wallet.wallet_coin_record import WalletCoinRecord
 from chia.wallet.wallet_weight_proof_handler import get_wp_fork_point
 from tests.connection_utils import disconnect_all, disconnect_all_and_reconnect
 from tests.weight_proof.test_weight_proof import load_blocks_dont_validate
 
 
 async def wallet_height_at_least(wallet_node, h):
@@ -504,46 +504,46 @@
         await wallet_server.start_client(PeerInfo(self_hostname, uint16(full_node_api.full_node.server._port)), None)
 
         for i in range(2):
             await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
 
         await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node, timeout=20)
 
-        payees: List[AmountWithPuzzlehash] = []
+        payees: List[Payment] = []
         for i in range(10):
             payee_ph = await wallet.get_new_puzzlehash()
-            payees.append({"amount": uint64(i + 100), "puzzlehash": payee_ph, "memos": []})
-            payees.append({"amount": uint64(i + 200), "puzzlehash": payee_ph, "memos": []})
+            payees.append(Payment(payee_ph, uint64(i + 100)))
+            payees.append(Payment(payee_ph, uint64(i + 200)))
 
         tx: TransactionRecord = await wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
 
         last_block: Optional[BlockRecord] = full_node_api.full_node.blockchain.get_peak()
         assert last_block is not None
         await full_node_api.wait_for_wallet_synced(wallet_node=wallet_node, timeout=20)
 
         res2: Optional[Message] = await full_node_api.request_additions(
             RequestAdditions(
                 last_block.height,
                 None,
-                [payees[0]["puzzlehash"], payees[2]["puzzlehash"], std_hash(b"1")],
+                [payees[0].puzzle_hash, payees[2].puzzle_hash, std_hash(b"1")],
             )
         )
 
         assert res2 is not None
         response = RespondAdditions.from_bytes(res2.data)
         assert response.height == last_block.height
         assert response.header_hash == last_block.header_hash
         assert len(response.proofs) == 3
 
         # First two PHs are included
         for i in range(2):
-            assert response.proofs[i][0] in {payees[j]["puzzlehash"] for j in (0, 2)}
+            assert response.proofs[i][0] in {payees[j].puzzle_hash for j in (0, 2)}
             assert response.proofs[i][1] is not None
             assert response.proofs[i][2] is not None
 
         # Third PH is not included
         assert response.proofs[2][2] is None
 
         coin_list_dict = {p: coin_list for p, coin_list in response.coins}
@@ -714,17 +714,17 @@
         for i in range(2):
             await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
 
         # sync both nodes
         await full_node_api.wait_for_wallets_synced(wallet_nodes=[farm_wallet_node, dust_wallet_node], timeout=20)
 
         # Part 1: create a single dust coin
-        payees: List[AmountWithPuzzlehash] = []
+        payees: List[Payment] = []
         payee_ph = await dust_wallet.get_new_puzzlehash()
-        payees.append({"amount": uint64(dust_value), "puzzlehash": payee_ph, "memos": []})
+        payees.append(Payment(payee_ph, uint64(dust_value)))
 
         # construct and send tx
         tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         # advance the chain and sync both wallets
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
@@ -765,35 +765,35 @@
 
         # Verify balance and number of coins not filtered.
         assert balance == dust_coins * dust_value + large_dust_balance
         assert num_coins == dust_coins + large_dust_coins
 
         # Part 2: Create dust coins until the filter threshold has been reached.
         # Nothing should be filtered yet (unless spam_filter_after_n_txs is 0).
-        payees: List[AmountWithPuzzlehash] = []
+        payees = []
 
         # Determine how much dust to create, recalling that there already is one dust coin.
         new_dust = spam_filter_after_n_txs - 1
         dust_remaining = new_dust
 
         while dust_remaining > 0:
             payee_ph = await dust_wallet.get_new_puzzlehash()
-            payees.append({"amount": uint64(dust_value), "puzzlehash": payee_ph, "memos": []})
+            payees.append(Payment(payee_ph, uint64(dust_value)))
 
             # After every 100 (at most) coins added, push the tx and advance the chain
             # This greatly speeds up the overall process
             if dust_remaining % 100 == 0 and dust_remaining != new_dust:
                 # construct and send tx
                 tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
                 await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
                 await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
                 last_block: Optional[BlockRecord] = full_node_api.full_node.blockchain.get_peak()
                 assert last_block is not None
                 # reset payees
-                payees: List[AmountWithPuzzlehash] = []
+                payees = []
 
             dust_remaining -= 1
 
         # Only need to create tx if there was new dust to be added
         if new_dust >= 1:
             # construct and send tx
             tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
@@ -832,19 +832,19 @@
         assert balance == dust_coins * dust_value + large_dust_balance
         assert num_coins == dust_coins + large_dust_coins
 
         # Part 3: Create 10 coins that are exactly the size of the filter threshold.
         # These should not get filtered.
         large_coins = 10
 
-        payees: List[AmountWithPuzzlehash] = []
+        payees = []
 
         for i in range(large_coins):
             payee_ph = await dust_wallet.get_new_puzzlehash()
-            payees.append({"amount": uint64(xch_spam_amount), "puzzlehash": payee_ph, "memos": []})
+            payees.append(Payment(payee_ph, uint64(xch_spam_amount)))
 
         # construct and send tx
         tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         # advance the chain and sync both wallets
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
@@ -872,18 +872,18 @@
         # Make sure the number of coins matches the expected number.
         # At this point, nothing should be getting filtered unless spam_filter_after_n_txs is 0.
         assert dust_coins == spam_filter_after_n_txs
         assert balance == dust_coins * dust_value + large_coins * xch_spam_amount + large_dust_balance
         assert num_coins == dust_coins + large_coins + large_dust_coins
 
         # Part 4: Create one more dust coin to test the threshold
-        payees: List[AmountWithPuzzlehash] = []
+        payees = []
 
         payee_ph = await dust_wallet.get_new_puzzlehash()
-        payees.append({"amount": uint64(dust_value), "puzzlehash": payee_ph, "memos": []})
+        payees.append(Payment(payee_ph, uint64(dust_value)))
 
         # construct and send tx
         tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         # advance the chain and sync both wallets
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
@@ -913,31 +913,31 @@
 
         assert dust_coins == spam_filter_after_n_txs
         assert balance == dust_coins * dust_value + large_coins * xch_spam_amount + large_dust_balance
         assert num_coins == dust_coins + large_dust_coins + large_coins
 
         # Part 5: Create 5 coins below the threshold and 5 at or above.
         # Those below the threshold should get filtered, and those above should not.
-        payees: List[AmountWithPuzzlehash] = []
+        payees = []
 
         for i in range(5):
             payee_ph = await dust_wallet.get_new_puzzlehash()
 
             # Create a large coin and add on the appropriate balance.
-            payees.append({"amount": uint64(xch_spam_amount + i), "puzzlehash": payee_ph, "memos": []})
+            payees.append(Payment(payee_ph, uint64(xch_spam_amount + i)))
             large_coins += 1
             large_coin_balance += xch_spam_amount + i
 
             payee_ph = await dust_wallet.get_new_puzzlehash()
 
             # Make sure we are always creating coins with a positive value.
             if xch_spam_amount - dust_value - i > 0:
-                payees.append({"amount": uint64(xch_spam_amount - dust_value - i), "puzzlehash": payee_ph, "memos": []})
+                payees.append(Payment(payee_ph, uint64(xch_spam_amount - dust_value - i)))
             else:
-                payees.append({"amount": uint64(dust_value), "puzzlehash": payee_ph, "memos": []})
+                payees.append(Payment(payee_ph, uint64(dust_value)))
             # In cases where xch_spam_amount is sufficiently low,
             # the new dust should be considered a large coina and not be filtered.
             if xch_spam_amount <= dust_value:
                 large_dust_coins += 1
                 large_dust_balance += dust_value
 
         # construct and send tx
@@ -970,15 +970,15 @@
         assert num_coins == dust_coins + large_dust_coins + large_coins
 
         # Part 6: Clear all coins from the dust wallet.
         # Send to the dust wallet "spam_filter_after_n_txs" coins that are equal in value to "xch_spam_amount".
         # Send 1 mojo from the dust wallet. The dust wallet should receive a change coin valued at "xch_spam_amount-1".
 
         payee_ph = await farm_wallet.get_new_puzzlehash()
-        payees: List[AmountWithPuzzlehash] = [{"amount": uint64(balance), "puzzlehash": payee_ph, "memos": []}]
+        payees = [Payment(payee_ph, uint64(balance))]
 
         # construct and send tx
         tx: TransactionRecord = await dust_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         # advance the chain and sync both wallets
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
@@ -1010,27 +1010,27 @@
         else:
             # Handle the edge case to make sure the coin is at least 2 mojos
             # This is needed to receive change
             coin_value = 2
 
         while coins_remaining > 0:
             payee_ph = await dust_wallet.get_new_puzzlehash()
-            payees.append({"amount": uint64(coin_value), "puzzlehash": payee_ph, "memos": []})
+            payees.append(Payment(payee_ph, uint64(coin_value)))
 
             # After every 100 (at most) coins added, push the tx and advance the chain
             # This greatly speeds up the overall process
             if coins_remaining % 100 == 0 and coins_remaining != spam_filter_after_n_txs:
                 # construct and send tx
                 tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
                 await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
                 await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
                 last_block: Optional[BlockRecord] = full_node_api.full_node.blockchain.get_peak()
                 assert last_block is not None
                 # reset payees
-                payees: List[AmountWithPuzzlehash] = []
+                payees = []
 
             coins_remaining -= 1
 
         # construct and send tx
         tx: TransactionRecord = await farm_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
@@ -1053,15 +1053,15 @@
         else:
             # in the edge case there should be 1 coin
             assert unspent_count == 1
         assert balance == unspent_count * coin_value
 
         # Send a 1 mojo coin from the dust wallet to the farm wallet
         payee_ph = await farm_wallet.get_new_puzzlehash()
-        payees: List[AmountWithPuzzlehash] = [{"amount": uint64(1), "puzzlehash": payee_ph, "memos": []}]
+        payees = [Payment(payee_ph, uint64(1))]
 
         # construct and send tx
         tx: TransactionRecord = await dust_wallet.generate_signed_transaction(uint64(0), ph, primaries=payees)
         await full_node_api.send_transaction(SendTransaction(tx.spend_bundle))
 
         # advance the chain and sync both wallets
         await full_node_api.farm_new_transaction_block(FarmNewBlockProtocol(ph))
@@ -1365,14 +1365,17 @@
 
     def wallet_syncing() -> bool:
         return wallet_node.wallet_state_manager.sync_mode
 
     def check_sync_canceled() -> bool:
         return sync_canceled
 
+    def synced_to_trusted() -> bool:
+        return trusted_full_node_server.node_id in wallet_node.synced_peers
+
     def only_trusted_peer() -> bool:
         trusted_peers = sum([wallet_node.is_trusted(peer) for peer in wallet_server.all_connections.values()])
         untrusted_peers = sum([not wallet_node.is_trusted(peer) for peer in wallet_server.all_connections.values()])
         return trusted_peers == 1 and untrusted_peers == 0
 
     for block in default_400_blocks:
         await trusted_full_node_api.full_node.add_block(block)
@@ -1386,15 +1389,15 @@
     # Connect to the untrusted peer and wait until the long sync started
     await wallet_server.start_client(PeerInfo(self_hostname, uint16(untrusted_full_node_server._port)), None)
     await time_out_assert(30, wallet_syncing)
     with caplog.at_level(logging.INFO):
         # Connect to the trusted peer and make sure the running untrusted long sync gets interrupted via disconnect
         await wallet_server.start_client(PeerInfo(self_hostname, uint16(trusted_full_node_server._port)), None)
         await time_out_assert(600, wallet_height_at_least, True, wallet_node, len(default_400_blocks) - 1)
-        assert trusted_full_node_server.node_id in wallet_node.synced_peers
+        assert time_out_assert(10, synced_to_trusted)
         assert untrusted_full_node_server.node_id not in wallet_node.synced_peers
         assert "Connected to a a synced trusted peer, disconnecting from all untrusted nodes." in caplog.text
 
     # Make sure the sync was interrupted
     assert time_out_assert(30, check_sync_canceled)
     # And that we only have a trusted peer left
     assert time_out_assert(30, only_trusted_peer)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_address_type.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_address_type.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_bech32m.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_bech32m.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_chialisp.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_chialisp.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_coin_selection.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_coin_selection.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_nft_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_nft_store.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,21 +1,45 @@
 from __future__ import annotations
 
+from dataclasses import dataclass, field
+from secrets import token_bytes
+from typing import Dict, List
+
 import pytest
 
 from chia.types.blockchain_format.coin import Coin
 from chia.types.blockchain_format.program import Program
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.util.ints import uint32, uint64
 from chia.wallet.lineage_proof import LineageProof
 from chia.wallet.nft_wallet.nft_info import NFTCoinInfo
 from chia.wallet.wallet_nft_store import WalletNftStore
 from tests.util.db_connection import DBConnection
 
 
+def get_dummy_nft() -> NFTCoinInfo:
+    return NFTCoinInfo(
+        bytes32(token_bytes(32)),
+        Coin(bytes32(token_bytes(32)), bytes32(token_bytes(32)), uint64(1)),
+        LineageProof(bytes32(token_bytes(32)), bytes32(token_bytes(32)), uint64(1)),
+        Program.to(["A Test puzzle"]),
+        uint32(1),
+    )
+
+
+@dataclass
+class DummyNFTs:
+    nfts_per_wallet: Dict[uint32, List[NFTCoinInfo]] = field(default_factory=dict)
+
+    def generate(self, wallet_id: int, count: int) -> None:
+        nfts = self.nfts_per_wallet.setdefault(uint32(wallet_id), [])
+        for _ in range(count):
+            nfts.append(get_dummy_nft())
+
+
 class TestNftStore:
     @pytest.mark.asyncio
     async def test_nft_insert(self) -> None:
         async with DBConnection(1) as wrapper:
             db = await WalletNftStore.create(wrapper)
             a_bytes32 = bytes32.fromhex("09287c75377c63fd6a3a4d6658abed03e9a521e0436b1f83cdf4af99341ce8f1")
             b_bytes32 = bytes32.fromhex("09287c75377c63fd6a3a4d6658abed03e9a521e0436b1f83cdf4af99341ce8f2")
@@ -140,7 +164,29 @@
             assert not (await db.get_nft_by_coin_id(coin_id_2))
             assert not (await db.get_nft_by_coin_id(nft_id_1))
             assert not await db.exists(coin_id_2)
 
             await db.rollback_to_block(-1)
             assert await db.count(wallet_id=uint32(1)) == 0
             assert await db.is_empty(wallet_id=uint32(1))
+
+
+@pytest.mark.asyncio
+async def test_delete_wallet() -> None:
+    dummy_nfts = DummyNFTs()
+    for i in range(5):
+        dummy_nfts.generate(i, i * 5)
+    async with DBConnection(1) as wrapper:
+        db = await WalletNftStore.create(wrapper)
+        # Add the nfts per wallet and verify them
+        for wallet_id, nfts in dummy_nfts.nfts_per_wallet.items():
+            for nft in nfts:
+                await db.save_nft(wallet_id, None, nft)
+            assert await db.count(wallet_id) == len(nfts)
+        # Remove one wallet after the other and verify before and after each
+        for wallet_id, nfts in dummy_nfts.nfts_per_wallet.items():
+            # Assert the length again here to make sure the previous removals did not affect other wallet_ids
+            assert await db.count(wallet_id) == len(nfts)
+            await db.delete_wallet(wallet_id)
+            assert await db.count(wallet_id) == 0
+
+        assert await db.is_empty()
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_notifications.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_notifications.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_offer_parsing_performance.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_offer_parsing_performance.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from __future__ import annotations
 
 import cProfile
+import sys
 from contextlib import contextmanager
 from typing import Iterator
 
 import pytest
 
 from chia.wallet.trading.offer import Offer
 from tests.util.misc import assert_runtime
@@ -13,14 +14,17 @@
 
 # gprof2dot -f pstats offer-parsing.profile >p.dot && dot -Tpng p.dot >offer-parsing.png
 # gprof2dot -f pstats offered-coins.profile >c.dot && dot -Tpng c.dot >offered-coins.png
 
 
 @contextmanager
 def enable_profiler(name: str) -> Iterator[None]:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     if not with_profile:
         yield
         return
 
     with cProfile.Profile() as pr:
         yield
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_puzzle_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_puzzle_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_singleton.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_singleton.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_singleton_lifecycle.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_singleton_lifecycle.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_singleton_lifecycle_fast.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_singleton_lifecycle_fast.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_taproot.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_taproot.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_transaction_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_transaction_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,18 +18,18 @@
 from chia.types.blockchain_format.program import Program
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.coin_spend import compute_additions
 from chia.types.peer_info import PeerInfo
 from chia.util.bech32m import encode_puzzle_hash
 from chia.util.ints import uint16, uint32, uint64
 from chia.wallet.derive_keys import master_sk_to_wallet_sk
+from chia.wallet.payment import Payment
 from chia.wallet.transaction_record import TransactionRecord
 from chia.wallet.util.compute_memos import compute_memos
 from chia.wallet.util.transaction_type import TransactionType
-from chia.wallet.util.wallet_types import AmountWithPuzzlehash
 from chia.wallet.wallet import CHIP_0002_SIGN_MESSAGE_PREFIX
 from chia.wallet.wallet_node import WalletNode, get_wallet_db_path
 from chia.wallet.wallet_state_manager import WalletStateManager
 
 
 class TestWalletSimulator:
     @pytest.mark.parametrize(
@@ -562,18 +562,15 @@
             wallet_node_2.config["trusted_peers"] = {}
         await server_2.start_client(PeerInfo(self_hostname, uint16(full_node_1.full_node.server._port)), None)
 
         expected_confirmed_balance = await full_node_1.farm_blocks_to_wallet(count=num_blocks, wallet=wallet)
 
         await time_out_assert(20, wallet.get_confirmed_balance, expected_confirmed_balance)
 
-        primaries: List[AmountWithPuzzlehash] = []
-        for i in range(0, 60):
-            primaries.append({"puzzlehash": ph, "amount": uint64(1000000000 + i), "memos": []})
-
+        primaries = [Payment(ph, uint64(1000000000 + i)) for i in range(60)]
         tx_split_coins = await wallet.generate_signed_transaction(uint64(1), ph, uint64(0), primaries=primaries)
         assert tx_split_coins.spend_bundle is not None
 
         await wallet.push_transaction(tx_split_coins)
         await full_node_1.process_transaction_records(records=[tx_split_coins])
         await wait_for_coins_in_wallet(coins=set(tx_split_coins.additions), wallet=wallet)
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_blockchain.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_blockchain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_interested_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_interested_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_key_val_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_key_val_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_node.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_node.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_retry.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_retry.py`

 * *Files 2% similar despite different names*

```diff
@@ -32,15 +32,15 @@
 
 def assert_sb_not_in_pool(node: FullNodeAPI, sb: SpendBundle) -> None:
     assert node.full_node.mempool_manager.get_spendbundle(sb.name()) is None
     assert not node.full_node.mempool_manager.seen(sb.name())
 
 
 def evict_from_pool(node: FullNodeAPI, sb: SpendBundle) -> None:
-    mempool_item = node.full_node.mempool_manager.mempool.get_spend_by_id(sb.name())
+    mempool_item = node.full_node.mempool_manager.mempool.get_item_by_id(sb.name())
     assert mempool_item is not None
     node.full_node.mempool_manager.mempool.remove_from_pool([mempool_item.name], MempoolRemoveReason.CONFLICT)
     node.full_node.mempool_manager.remove_seen(sb.name())
 
 
 @pytest.mark.asyncio
 async def test_wallet_tx_retry(
```

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_state_manager.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_state_manager.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_trade_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_trade_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/wallet/test_wallet_user_store.py` & `chia-blockchain-2.0.0b1/tests/wallet/test_wallet_user_store.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tests/weight_proof/test_weight_proof.py` & `chia-blockchain-2.0.0b1/tests/weight_proof/test_weight_proof.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/analyze-chain.py` & `chia-blockchain-2.0.0b1/tools/analyze-chain.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/analyze_memory_profile.py` & `chia-blockchain-2.0.0b1/tools/analyze_memory_profile.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/cpu_utilization.py` & `chia-blockchain-2.0.0b1/tools/cpu_utilization.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/generate_chain.py` & `chia-blockchain-2.0.0b1/tools/generate_chain.py`

 * *Files 3% similar despite different names*

```diff
@@ -19,14 +19,17 @@
 from chia.util.chia_logging import initialize_logging
 from chia.util.ints import uint32, uint64
 from tools.test_constants import test_constants
 
 
 @contextmanager
 def enable_profiler(profile: bool, counter: int) -> Iterator[None]:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     if not profile:
         yield
         return
 
     with cProfile.Profile() as pr:
         yield
```

### Comparing `chia-blockchain-1.8.1rc2/tools/legacy_keyring.py` & `chia-blockchain-2.0.0b1/tools/legacy_keyring.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/manage_clvm.py` & `chia-blockchain-2.0.0b1/tools/manage_clvm.py`

 * *Files 0% similar despite different names*

```diff
@@ -39,15 +39,15 @@
 std_libraries = root.joinpath("chia/wallet/puzzles")
 
 
 class ManageClvmError(Exception):
     pass
 
 
-class CacheEntry(typing.TypedDict):
+class CacheEntry(typing_extensions.TypedDict):
     clsp: str
     hex: str
     hash: str
 
 
 CacheEntries = typing.Dict[str, CacheEntry]
 CacheVersion = typing.List[int]
@@ -66,15 +66,15 @@
 class WrongCacheVersionError(CacheVersionError):
     def __init__(self, found_version: object, expected_version: CacheVersion) -> None:
         self.found_version = found_version
         self.expected_version = expected_version
         super().__init__(f"Cache has wrong version, expected {expected_version!r} got: {found_version!r}")
 
 
-class Cache(typing.TypedDict):
+class Cache(typing_extensions.TypedDict):
     entries: CacheEntries
     version: CacheVersion
 
 
 def create_empty_cache() -> Cache:
     return {
         "entries": {},
```

### Comparing `chia-blockchain-1.8.1rc2/tools/plot-log.gnuplot` & `chia-blockchain-2.0.0b1/tools/plot-log.gnuplot`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/run_benchmark.sh` & `chia-blockchain-2.0.0b1/tools/run_benchmark.sh`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/run_block.py` & `chia-blockchain-2.0.0b1/tools/run_block.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/test_constants.py` & `chia-blockchain-2.0.0b1/tools/test_constants.py`

 * *Files identical despite different names*

### Comparing `chia-blockchain-1.8.1rc2/tools/test_full_sync.py` & `chia-blockchain-2.0.0b1/tools/test_full_sync.py`

 * *Files 14% similar despite different names*

```diff
@@ -3,28 +3,30 @@
 from __future__ import annotations
 
 import asyncio
 import cProfile
 import logging
 import os
 import shutil
+import sys
 import tempfile
 import time
 from contextlib import contextmanager
 from pathlib import Path
-from typing import Callable, Iterator, List, Optional
+from typing import Callable, Iterator, List, Optional, cast
 
 import aiosqlite
 import click
 import zstd
 
 from chia.cmds.init_funcs import chia_init
 from chia.consensus.default_constants import DEFAULT_CONSTANTS
 from chia.full_node.full_node import FullNode
 from chia.server.outbound_message import Message, NodeType
+from chia.server.server import ChiaServer
 from chia.server.ws_connection import WSChiaConnection
 from chia.simulator.block_tools import make_unfinished_block
 from chia.types.blockchain_format.sized_bytes import bytes32
 from chia.types.full_block import FullBlock
 from chia.types.peer_info import PeerInfo
 from chia.util.config import load_config
 from chia.util.ints import uint16
@@ -40,14 +42,17 @@
         if record.levelno != logging.ERROR:
             return
         self.exit_with_failure = True
 
 
 @contextmanager
 def enable_profiler(profile: bool, counter: int) -> Iterator[None]:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     if not profile:
         yield
         return
 
     with cProfile.Profile() as pr:
         receive_start_time = time.monotonic()
         yield
@@ -103,14 +108,17 @@
     single_thread: bool,
     test_constants: bool,
     keep_up: bool,
     db_sync: str,
     node_profiler: bool,
     start_at_checkpoint: Optional[str],
 ) -> None:
+    if sys.version_info < (3, 8):
+        raise Exception(f"Python 3.8 or higher required, running with: {sys.version}")
+
     logger = logging.getLogger()
     logger.setLevel(logging.WARNING)
     handler = logging.FileHandler("test-full-sync.log")
     handler.setFormatter(
         logging.Formatter(
             "%(levelname)-8s %(message)s",
             datefmt="%Y-%m-%dT%H:%M:%S",
@@ -140,24 +148,24 @@
         full_node = FullNode(
             config["full_node"],
             root_path=root_path,
             consensus_constants=constants,
         )
 
         try:
-            full_node.set_server(FakeServer())  # type: ignore[arg-type]
+            full_node.set_server(cast(ChiaServer, FakeServer()))
             await full_node._start()
 
             peak = full_node.blockchain.get_peak()
             if peak is not None:
                 height = int(peak.height)
             else:
                 height = 0
 
-            peer: WSChiaConnection = FakePeer()  # type: ignore[assignment]
+            peer: WSChiaConnection = cast(WSChiaConnection, FakePeer())
 
             print()
             counter = 0
             monotonic = height
             prev_hash = None
             async with aiosqlite.connect(file) as in_db:
                 await in_db.execute("pragma query_only")
@@ -234,15 +242,15 @@
 
 
 @click.group()
 def main() -> None:
     pass
 
 
-@main.command("run", short_help="run simulated full sync from an existing blockchain db")
+@main.command("run", help="run simulated full sync from an existing blockchain db")
 @click.argument("file", type=click.Path(), required=True)
 @click.option("--db-version", type=int, required=False, default=2, help="the DB version to use in simulated node")
 @click.option("--profile", is_flag=True, required=False, default=False, help="dump CPU profiles for slow batches")
 @click.option("--db-sync", type=str, required=False, default="off", help="sqlite sync mode. One of: off, normal, full")
 @click.option("--node-profiler", is_flag=True, required=False, default=False, help="enable the built-in node-profiler")
 @click.option(
     "--test-constants",
@@ -298,27 +306,27 @@
             db_sync,
             node_profiler,
             start_at_checkpoint,
         )
     )
 
 
-@main.command("analyze", short_help="generate call stacks for all profiles dumped to current directory")
+@main.command("analyze", help="generate call stacks for all profiles dumped to current directory")
 def analyze() -> None:
     from glob import glob
     from shlex import quote
     from subprocess import check_call
 
     for input_file in glob("slow-batch-*.profile"):
         output = input_file.replace(".profile", ".png")
         print(f"{input_file}")
         check_call(f"gprof2dot -f pstats {quote(input_file)} | dot -T png >{quote(output)}", shell=True)
 
 
-@main.command("create-checkpoint", short_help="sync the full node up to specified height and save its state")
+@main.command("create-checkpoint", help="sync the full node up to specified height and save its state")
 @click.argument("file", type=click.Path(), required=True)
 @click.argument("out-file", type=click.Path(), required=True)
 @click.option("--height", type=int, required=True, help="Sync node up to this height")
 def create_checkpoint(file: Path, out_file: Path, height: int) -> None:
     """
     The FILE parameter should point to an existing blockchain database file (in v2 format)
     """
```

