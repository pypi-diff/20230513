# Comparing `tmp/nebari_workflow_controller-2023.5.4.tar.gz` & `tmp/nebari_workflow_controller-2023.5.5.tar.gz`

## Comparing `nebari_workflow_controller-2023.5.4.tar` & `nebari_workflow_controller-2023.5.5.tar`

### file list

```diff
@@ -1,194 +1,195 @@
--rw-r--r--   0        0        0     2786 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/.pre-commit-config.yaml
--rw-r--r--   0        0        0      269 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nwc.py
--rw-r--r--   0        0        0     1988 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/.github/workflows/release.yaml
--rw-r--r--   0        0        0      905 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/__init__.py
--rw-r--r--   0        0        0     1107 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/__main__.py
--rw-r--r--   0        0        0      166 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/_version.py
--rw-r--r--   0        0        0     6600 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/app.py
--rw-r--r--   0        0        0      159 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/exceptions.py
--rw-r--r--   0        0        0      234 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/models.py
--rw-r--r--   0        0        0    11587 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/nebari_workflow_controller/utils.py
--rw-r--r--   0        0        0     2733 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/conftest.py
--rw-r--r--   0        0        0     3153 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_app.py
--rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/README.md
--rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/convert_workflows.py
--rw-r--r--   0        0        0    43422 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/jupyterlab_pod_spec.pkl
--rw-r--r--   0        0        0     8976 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_disallowed_conda_mount.yaml
--rw-r--r--   0        0        0     8812 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_disallowed_file_mount.yaml
--rw-r--r--   0        0        0     8760 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_empty_subPath.yaml
--rw-r--r--   0        0        0     8943 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/disallowed_volume.yaml
--rw-r--r--   0        0        0     8826 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_disallowed_conda_mount.yaml
--rw-r--r--   0        0        0     8812 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_disallowed_file_mount.yaml
--rw-r--r--   0        0        0     8773 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_empty_subPath.yaml
--rw-r--r--   0        0        0     1837 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/volumes-existing.yaml
--rw-r--r--   0        0        0     1153 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/archive-location.yaml
--rw-r--r--   0        0        0     2948 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/argo_cli_hello_world.yaml
--rw-r--r--   0        0        0     1442 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-artifacts.yaml
--rw-r--r--   0        0        0     1823 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-parameters-from-configmap.yaml
--rw-r--r--   0        0        0     1278 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-parameters.yaml
--rw-r--r--   0        0        0     2616 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-disable-archive.yaml
--rw-r--r--   0        0        0     1606 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-gc-workflow.yaml
--rw-r--r--   0        0        0     2452 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-passing-subpath.yaml
--rw-r--r--   0        0        0     1875 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-passing.yaml
--rw-r--r--   0        0        0     2030 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-path-placeholders.yaml
--rw-r--r--   0        0        0     1303 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-repository-ref.yaml
--rw-r--r--   0        0        0     2526 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifactory-artifact.yaml
--rw-r--r--   0        0        0     2932 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/browser_hello_world.yaml
--rw-r--r--   0        0        0     2846 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/ci-output-artifact.yaml
--rw-r--r--   0        0        0     2920 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/ci.yaml
--rw-r--r--   0        0        0     1697 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/coinflip-recursive.yaml
--rw-r--r--   0        0        0     2109 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/coinflip.yaml
--rw-r--r--   0        0        0     1633 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/colored-logs.yaml
--rw-r--r--   0        0        0     2924 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditional-artifacts.yaml
--rw-r--r--   0        0        0     2621 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditional-parameters.yaml
--rw-r--r--   0        0        0     2753 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditionals-complex.yaml
--rw-r--r--   0        0        0     1750 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditionals.yaml
--rw-r--r--   0        0        0     1627 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/continue-on-fail.yaml
--rw-r--r--   0        0        0     3211 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/custom-metrics.yaml
--rw-r--r--   0        0        0     1889 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemon-nginx.yaml
--rw-r--r--   0        0        0     3131 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemon-step.yaml
--rw-r--r--   0        0        0     3316 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemoned-stateful-set-with-service.yaml
--rw-r--r--   0        0        0     2257 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-coinflip.yaml
--rw-r--r--   0        0        0     2994 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-conditional-artifacts.yaml
--rw-r--r--   0        0        0     2696 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-conditional-parameters.yaml
--rw-r--r--   0        0        0     1875 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-continue-on-fail.yaml
--rw-r--r--   0        0        0     3485 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-custom-metrics.yaml
--rw-r--r--   0        0        0     3343 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-daemon-task.yaml
--rw-r--r--   0        0        0     2276 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-diamond-steps.yaml
--rw-r--r--   0        0        0     1874 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-diamond.yaml
--rw-r--r--   0        0        0     2061 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-disable-failFast.yaml
--rw-r--r--   0        0        0     1869 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-enhanced-depends.yaml
--rw-r--r--   0        0        0     1343 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-inline-workflow.yaml
--rw-r--r--   0        0        0     1857 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-multiroot.yaml
--rw-r--r--   0        0        0     2838 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-nested.yaml
--rw-r--r--   0        0        0     2183 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-targets.yaml
--rw-r--r--   0        0        0     1734 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-task-level-timeout.yaml
--rw-r--r--   0        0        0     2398 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/data-transformations.yaml
--rw-r--r--   0        0        0     1194 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/default-pdb-support.yaml
--rw-r--r--   0        0        0     1300 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dns-config.yaml
--rw-r--r--   0        0        0     1798 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-code-output-variable.yaml
--rw-r--r--   0        0        0     2152 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-dag-level.yaml
--rw-r--r--   0        0        0     1545 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-slack.yaml
--rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-step-level.yaml
--rw-r--r--   0        0        0     2108 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-with-artifacts.yaml
--rw-r--r--   0        0        0     2140 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-with-param.yaml
--rw-r--r--   0        0        0     2079 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handlers.yaml
--rw-r--r--   0        0        0     1797 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-destructure-json.yaml
--rw-r--r--   0        0        0     2145 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-reusing-verbose-snippets.yaml
--rw-r--r--   0        0        0     1788 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-tag-template-workflow.yaml
--rw-r--r--   0        0        0     4868 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/fibonacci-seq-conditional-param.yaml
--rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/forever.yaml
--rw-r--r--   0        0        0     4167 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/fun-with-gifs.yaml
--rw-r--r--   0        0        0     1206 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/gc-ttl.yaml
--rw-r--r--   0        0        0     2579 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-outputs.yaml
--rw-r--r--   0        0        0     1845 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters-from-configmap-referenced-as-local-variable.yaml
--rw-r--r--   0        0        0     1731 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters-from-configmap.yaml
--rw-r--r--   0        0        0     1215 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters.yaml
--rw-r--r--   0        0        0     2221 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/handle-large-output-results.yaml
--rw-r--r--   0        0        0     2459 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hdfs-artifact.yaml
--rw-r--r--   0        0        0     1594 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-hybrid.yaml
--rw-r--r--   0        0        0     1223 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-windows.yaml
--rw-r--r--   0        0        0     1380 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-world.yaml
--rw-r--r--   0        0        0     1901 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/http-hello-world.yaml
--rw-r--r--   0        0        0     2284 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/http-success-condition.yaml
--rw-r--r--   0        0        0     1156 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/image-pull-secrets.yaml
--rw-r--r--   0        0        0     7924 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/influxdb-ci.yaml
--rw-r--r--   0        0        0     1385 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/init-container.yaml
--rw-r--r--   0        0        0     1519 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-azure.yaml
--rw-r--r--   0        0        0     1447 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-gcs.yaml
--rw-r--r--   0        0        0     1356 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-git.yaml
--rw-r--r--   0        0        0     1374 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-http.yaml
--rw-r--r--   0        0        0     1603 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-oss.yaml
--rw-r--r--   0        0        0     1325 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-raw.yaml
--rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-s3.yaml
--rw-r--r--   0        0        0     1092 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/jupyterflow-override-example.yaml
--rw-r--r--   0        0        0     8814 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/jupyterlab_pod.yaml
--rw-r--r--   0        0        0     1694 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-jobs.yaml
--rw-r--r--   0        0        0     1330 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-json-patch-workflow.yaml
--rw-r--r--   0        0        0     3023 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-orchestration.yaml
--rw-r--r--   0        0        0     1762 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-owner-reference.yaml
--rw-r--r--   0        0        0     1334 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-patch-basic.yaml
--rw-r--r--   0        0        0     1371 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-patch.yaml
--rw-r--r--   0        0        0     2772 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-resource-log-selector.yaml
--rw-r--r--   0        0        0     1207 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-set-owner-reference.yaml
--rw-r--r--   0        0        0     2110 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-wait-wf.yaml
--rw-r--r--   0        0        0     1678 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/key-only-artifact.yaml
--rw-r--r--   0        0        0     4818 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/kubectl_malicious.yaml
--rw-r--r--   0        0        0     1574 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/label-value-from-workflow.yaml
--rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/life-cycle-hooks-tmpl-level.yaml
--rw-r--r--   0        0        0     1526 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/life-cycle-hooks-wf-level.yaml
--rw-r--r--   0        0        0     2320 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-arbitrary-sequential-steps.yaml
--rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-dag.yaml
--rw-r--r--   0        0        0     1756 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-maps.yaml
--rw-r--r--   0        0        0     1963 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-param-argument.yaml
--rw-r--r--   0        0        0     1893 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-param-result.yaml
--rw-r--r--   0        0        0     2521 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-sequence.yaml
--rw-r--r--   0        0        0     1472 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops.yaml
--rw-r--r--   0        0        0     4627 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/map-reduce.yaml
--rw-r--r--   0        0        0     1391 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/memoize-simple.yaml
--rw-r--r--   0        0        0     3630 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/nested-workflow.yaml
--rw-r--r--   0        0        0     1328 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/node-selector.yaml
--rw-r--r--   0        0        0     1536 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-azure.yaml
--rw-r--r--   0        0        0     1457 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-gcs.yaml
--rw-r--r--   0        0        0     1613 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-s3.yaml
--rw-r--r--   0        0        0     1921 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-parameter.yaml
--rw-r--r--   0        0        0     1431 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-limit.yaml
--rw-r--r--   0        0        0     2793 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested-dag.yaml
--rw-r--r--   0        0        0     1960 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested-workflow.yaml
--rw-r--r--   0        0        0     2415 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested.yaml
--rw-r--r--   0        0        0     1460 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-template-limit.yaml
--rw-r--r--   0        0        0     3480 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation-dag.yaml
--rw-r--r--   0        0        0     2172 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation-script.yaml
--rw-r--r--   0        0        0     3356 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation.yaml
--rw-r--r--   0        0        0     2080 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-gc-strategy-with-label-selector.yaml
--rw-r--r--   0        0        0     1444 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-gc-strategy.yaml
--rw-r--r--   0        0        0     1531 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-metadata-wf-field.yaml
--rw-r--r--   0        0        0     1540 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-metadata.yaml
--rw-r--r--   0        0        0     2164 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-from-previous-step.yaml
--rw-r--r--   0        0        0     1518 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-patch-wf-tmpl.yaml
--rw-r--r--   0        0        0     1320 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-patch.yaml
--rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-yaml-patch.yaml
--rw-r--r--   0        0        0     2143 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/recursive-for-loop.yaml
--rw-r--r--   0        0        0     1733 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resource-delete-with-flags.yaml
--rw-r--r--   0        0        0     1856 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resource-flags.yaml
--rw-r--r--   0        0        0     1995 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resubmit.yaml
--rw-r--r--   0        0        0     1331 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-backoff.yaml
--rw-r--r--   0        0        0     1901 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-conditional.yaml
--rw-r--r--   0        0        0     1225 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-container-to-completion.yaml
--rw-r--r--   0        0        0     1240 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-container.yaml
--rw-r--r--   0        0        0     1260 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-on-error.yaml
--rw-r--r--   0        0        0     1227 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-script.yaml
--rw-r--r--   0        0        0     1510 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-with-steps.yaml
--rw-r--r--   0        0        0     1776 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-bash.yaml
--rw-r--r--   0        0        0     1768 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-javascript.yaml
--rw-r--r--   0        0        0     1759 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-python.yaml
--rw-r--r--   0        0        0     1558 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/secrets.yaml
--rw-r--r--   0        0        0     1566 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar-dind.yaml
--rw-r--r--   0        0        0     1368 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar-nginx.yaml
--rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar.yaml
--rw-r--r--   0        0        0     1889 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/status-reference.yaml
--rw-r--r--   0        0        0     1696 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/step-level-timeout.yaml
--rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/steps-inline-workflow.yaml
--rw-r--r--   0        0        0     1721 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/steps.yaml
--rw-r--r--   0        0        0     1630 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/suspend-template-outputs.yaml
--rw-r--r--   0        0        0     1453 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/suspend-template.yaml
--rw-r--r--   0        0        0     2046 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-mutex-tmpl-level.yaml
--rw-r--r--   0        0        0     1167 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-mutex-wf-level.yaml
--rw-r--r--   0        0        0     1598 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-tmpl-level.yaml
--rw-r--r--   0        0        0     1231 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-wf-level.yaml
--rw-r--r--   0        0        0     1898 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/template-defaults.yaml
--rw-r--r--   0        0        0     1480 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/template-on-exit.yaml
--rw-r--r--   0        0        0     1142 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/timeouts-step.yaml
--rw-r--r--   0        0        0     1567 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/timeouts-workflow.yaml
--rw-r--r--   0        0        0     1410 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/volumes-emptydir.yaml
--rw-r--r--   0        0        0     1957 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/volumes-pvc.yaml
--rw-r--r--   0        0        0    18252 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/web-ui-resubmit.yaml
--rw-r--r--   0        0        0     2600 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/webhdfs-input-output-artifacts.yaml
--rw-r--r--   0        0        0     3475 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/work-avoidance.yaml
--rw-r--r--   0        0        0     2692 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/workflow-of-workflows.yaml
--rw-r--r--   0        0        0     4495 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/workflow_from_cronWorkflow.yaml
--rw-r--r--   0        0        0     1830 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/.gitignore
--rw-r--r--   0        0        0     1536 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/LICENSE
--rw-r--r--   0        0        0      340 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/README.md
--rw-r--r--   0        0        0     1913 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/pyproject.toml
--rw-r--r--   0        0        0     1800 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.4/PKG-INFO
+-rw-r--r--   0        0        0     2786 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      269 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nwc.py
+-rw-r--r--   0        0        0     1988 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/.github/workflows/release.yaml
+-rw-r--r--   0        0        0      905 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/__init__.py
+-rw-r--r--   0        0        0     1107 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/__main__.py
+-rw-r--r--   0        0        0      166 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/_version.py
+-rw-r--r--   0        0        0     6443 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/app.py
+-rw-r--r--   0        0        0      159 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/exceptions.py
+-rw-r--r--   0        0        0      234 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/models.py
+-rw-r--r--   0        0        0      269 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/nwc.py
+-rw-r--r--   0        0        0    10844 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/nebari_workflow_controller/utils.py
+-rw-r--r--   0        0        0     2733 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/conftest.py
+-rw-r--r--   0        0        0     3144 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_app.py
+-rw-r--r--   0        0        0      138 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/README.md
+-rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/convert_workflows.py
+-rw-r--r--   0        0        0    43422 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/jupyterlab_pod_spec.pkl
+-rw-r--r--   0        0        0     8976 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_disallowed_conda_mount.yaml
+-rw-r--r--   0        0        0     8812 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_disallowed_file_mount.yaml
+-rw-r--r--   0        0        0     8760 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_empty_subPath.yaml
+-rw-r--r--   0        0        0     8943 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/disallowed_volume.yaml
+-rw-r--r--   0        0        0     8826 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_disallowed_conda_mount.yaml
+-rw-r--r--   0        0        0     8812 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_disallowed_file_mount.yaml
+-rw-r--r--   0        0        0     8773 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_empty_subPath.yaml
+-rw-r--r--   0        0        0     1837 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/volumes-existing.yaml
+-rw-r--r--   0        0        0     1153 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/archive-location.yaml
+-rw-r--r--   0        0        0     2948 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/argo_cli_hello_world.yaml
+-rw-r--r--   0        0        0     1442 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-artifacts.yaml
+-rw-r--r--   0        0        0     1823 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-parameters-from-configmap.yaml
+-rw-r--r--   0        0        0     1278 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-parameters.yaml
+-rw-r--r--   0        0        0     2616 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-disable-archive.yaml
+-rw-r--r--   0        0        0     1606 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-gc-workflow.yaml
+-rw-r--r--   0        0        0     2452 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-passing-subpath.yaml
+-rw-r--r--   0        0        0     1875 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-passing.yaml
+-rw-r--r--   0        0        0     2030 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-path-placeholders.yaml
+-rw-r--r--   0        0        0     1303 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-repository-ref.yaml
+-rw-r--r--   0        0        0     2526 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifactory-artifact.yaml
+-rw-r--r--   0        0        0     2932 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/browser_hello_world.yaml
+-rw-r--r--   0        0        0     2846 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/ci-output-artifact.yaml
+-rw-r--r--   0        0        0     2920 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/ci.yaml
+-rw-r--r--   0        0        0     1697 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/coinflip-recursive.yaml
+-rw-r--r--   0        0        0     2109 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/coinflip.yaml
+-rw-r--r--   0        0        0     1633 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/colored-logs.yaml
+-rw-r--r--   0        0        0     2924 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditional-artifacts.yaml
+-rw-r--r--   0        0        0     2621 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditional-parameters.yaml
+-rw-r--r--   0        0        0     2753 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditionals-complex.yaml
+-rw-r--r--   0        0        0     1750 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditionals.yaml
+-rw-r--r--   0        0        0     1627 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/continue-on-fail.yaml
+-rw-r--r--   0        0        0     3211 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/custom-metrics.yaml
+-rw-r--r--   0        0        0     1889 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemon-nginx.yaml
+-rw-r--r--   0        0        0     3131 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemon-step.yaml
+-rw-r--r--   0        0        0     3316 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemoned-stateful-set-with-service.yaml
+-rw-r--r--   0        0        0     2257 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-coinflip.yaml
+-rw-r--r--   0        0        0     2994 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-conditional-artifacts.yaml
+-rw-r--r--   0        0        0     2696 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-conditional-parameters.yaml
+-rw-r--r--   0        0        0     1875 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-continue-on-fail.yaml
+-rw-r--r--   0        0        0     3485 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-custom-metrics.yaml
+-rw-r--r--   0        0        0     3343 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-daemon-task.yaml
+-rw-r--r--   0        0        0     2276 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-diamond-steps.yaml
+-rw-r--r--   0        0        0     1874 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-diamond.yaml
+-rw-r--r--   0        0        0     2061 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-disable-failFast.yaml
+-rw-r--r--   0        0        0     1869 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-enhanced-depends.yaml
+-rw-r--r--   0        0        0     1343 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-inline-workflow.yaml
+-rw-r--r--   0        0        0     1857 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-multiroot.yaml
+-rw-r--r--   0        0        0     2838 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-nested.yaml
+-rw-r--r--   0        0        0     2183 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-targets.yaml
+-rw-r--r--   0        0        0     1734 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-task-level-timeout.yaml
+-rw-r--r--   0        0        0     2398 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/data-transformations.yaml
+-rw-r--r--   0        0        0     1194 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/default-pdb-support.yaml
+-rw-r--r--   0        0        0     1300 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dns-config.yaml
+-rw-r--r--   0        0        0     1798 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-code-output-variable.yaml
+-rw-r--r--   0        0        0     2152 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-dag-level.yaml
+-rw-r--r--   0        0        0     1545 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-slack.yaml
+-rw-r--r--   0        0        0     1938 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-step-level.yaml
+-rw-r--r--   0        0        0     2108 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-with-artifacts.yaml
+-rw-r--r--   0        0        0     2140 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-with-param.yaml
+-rw-r--r--   0        0        0     2079 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handlers.yaml
+-rw-r--r--   0        0        0     1797 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-destructure-json.yaml
+-rw-r--r--   0        0        0     2145 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-reusing-verbose-snippets.yaml
+-rw-r--r--   0        0        0     1788 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-tag-template-workflow.yaml
+-rw-r--r--   0        0        0     4868 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/fibonacci-seq-conditional-param.yaml
+-rw-r--r--   0        0        0     1118 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/forever.yaml
+-rw-r--r--   0        0        0     4167 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/fun-with-gifs.yaml
+-rw-r--r--   0        0        0     1206 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/gc-ttl.yaml
+-rw-r--r--   0        0        0     2579 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-outputs.yaml
+-rw-r--r--   0        0        0     1845 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters-from-configmap-referenced-as-local-variable.yaml
+-rw-r--r--   0        0        0     1731 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters-from-configmap.yaml
+-rw-r--r--   0        0        0     1215 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters.yaml
+-rw-r--r--   0        0        0     2221 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/handle-large-output-results.yaml
+-rw-r--r--   0        0        0     2459 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hdfs-artifact.yaml
+-rw-r--r--   0        0        0     1594 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-hybrid.yaml
+-rw-r--r--   0        0        0     1223 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-windows.yaml
+-rw-r--r--   0        0        0     1380 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-world.yaml
+-rw-r--r--   0        0        0     1901 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/http-hello-world.yaml
+-rw-r--r--   0        0        0     2284 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/http-success-condition.yaml
+-rw-r--r--   0        0        0     1156 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/image-pull-secrets.yaml
+-rw-r--r--   0        0        0     7924 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/influxdb-ci.yaml
+-rw-r--r--   0        0        0     1385 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/init-container.yaml
+-rw-r--r--   0        0        0     1519 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-azure.yaml
+-rw-r--r--   0        0        0     1447 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-gcs.yaml
+-rw-r--r--   0        0        0     1356 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-git.yaml
+-rw-r--r--   0        0        0     1374 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-http.yaml
+-rw-r--r--   0        0        0     1603 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-oss.yaml
+-rw-r--r--   0        0        0     1325 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-raw.yaml
+-rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-s3.yaml
+-rw-r--r--   0        0        0     1086 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/jupyterflow-override-example.yaml
+-rw-r--r--   0        0        0     8814 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/jupyterlab_pod.yaml
+-rw-r--r--   0        0        0     1694 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-jobs.yaml
+-rw-r--r--   0        0        0     1330 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-json-patch-workflow.yaml
+-rw-r--r--   0        0        0     3023 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-orchestration.yaml
+-rw-r--r--   0        0        0     1762 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-owner-reference.yaml
+-rw-r--r--   0        0        0     1334 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-patch-basic.yaml
+-rw-r--r--   0        0        0     1371 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-patch.yaml
+-rw-r--r--   0        0        0     2772 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-resource-log-selector.yaml
+-rw-r--r--   0        0        0     1207 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-set-owner-reference.yaml
+-rw-r--r--   0        0        0     2110 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-wait-wf.yaml
+-rw-r--r--   0        0        0     1678 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/key-only-artifact.yaml
+-rw-r--r--   0        0        0     4818 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/kubectl_malicious.yaml
+-rw-r--r--   0        0        0     1574 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/label-value-from-workflow.yaml
+-rw-r--r--   0        0        0     1942 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/life-cycle-hooks-tmpl-level.yaml
+-rw-r--r--   0        0        0     1526 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/life-cycle-hooks-wf-level.yaml
+-rw-r--r--   0        0        0     2320 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-arbitrary-sequential-steps.yaml
+-rw-r--r--   0        0        0     1829 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-dag.yaml
+-rw-r--r--   0        0        0     1756 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-maps.yaml
+-rw-r--r--   0        0        0     1963 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-param-argument.yaml
+-rw-r--r--   0        0        0     1893 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-param-result.yaml
+-rw-r--r--   0        0        0     2521 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-sequence.yaml
+-rw-r--r--   0        0        0     1472 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops.yaml
+-rw-r--r--   0        0        0     4627 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/map-reduce.yaml
+-rw-r--r--   0        0        0     1391 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/memoize-simple.yaml
+-rw-r--r--   0        0        0     3630 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/nested-workflow.yaml
+-rw-r--r--   0        0        0     1328 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/node-selector.yaml
+-rw-r--r--   0        0        0     1536 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-azure.yaml
+-rw-r--r--   0        0        0     1457 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-gcs.yaml
+-rw-r--r--   0        0        0     1613 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-s3.yaml
+-rw-r--r--   0        0        0     1921 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-parameter.yaml
+-rw-r--r--   0        0        0     1431 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-limit.yaml
+-rw-r--r--   0        0        0     2793 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested-dag.yaml
+-rw-r--r--   0        0        0     1960 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested-workflow.yaml
+-rw-r--r--   0        0        0     2415 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested.yaml
+-rw-r--r--   0        0        0     1460 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-template-limit.yaml
+-rw-r--r--   0        0        0     3480 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation-dag.yaml
+-rw-r--r--   0        0        0     2172 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation-script.yaml
+-rw-r--r--   0        0        0     3356 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation.yaml
+-rw-r--r--   0        0        0     2080 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-gc-strategy-with-label-selector.yaml
+-rw-r--r--   0        0        0     1444 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-gc-strategy.yaml
+-rw-r--r--   0        0        0     1531 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-metadata-wf-field.yaml
+-rw-r--r--   0        0        0     1540 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-metadata.yaml
+-rw-r--r--   0        0        0     2164 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-from-previous-step.yaml
+-rw-r--r--   0        0        0     1518 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-patch-wf-tmpl.yaml
+-rw-r--r--   0        0        0     1320 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-patch.yaml
+-rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-yaml-patch.yaml
+-rw-r--r--   0        0        0     2143 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/recursive-for-loop.yaml
+-rw-r--r--   0        0        0     1733 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resource-delete-with-flags.yaml
+-rw-r--r--   0        0        0     1856 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resource-flags.yaml
+-rw-r--r--   0        0        0     1995 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resubmit.yaml
+-rw-r--r--   0        0        0     1331 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-backoff.yaml
+-rw-r--r--   0        0        0     1901 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-conditional.yaml
+-rw-r--r--   0        0        0     1225 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-container-to-completion.yaml
+-rw-r--r--   0        0        0     1240 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-container.yaml
+-rw-r--r--   0        0        0     1260 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-on-error.yaml
+-rw-r--r--   0        0        0     1227 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-script.yaml
+-rw-r--r--   0        0        0     1510 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-with-steps.yaml
+-rw-r--r--   0        0        0     1776 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-bash.yaml
+-rw-r--r--   0        0        0     1768 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-javascript.yaml
+-rw-r--r--   0        0        0     1759 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-python.yaml
+-rw-r--r--   0        0        0     1558 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/secrets.yaml
+-rw-r--r--   0        0        0     1566 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar-dind.yaml
+-rw-r--r--   0        0        0     1368 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar-nginx.yaml
+-rw-r--r--   0        0        0     1534 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar.yaml
+-rw-r--r--   0        0        0     1889 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/status-reference.yaml
+-rw-r--r--   0        0        0     1696 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/step-level-timeout.yaml
+-rw-r--r--   0        0        0     1333 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/steps-inline-workflow.yaml
+-rw-r--r--   0        0        0     1721 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/steps.yaml
+-rw-r--r--   0        0        0     1630 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/suspend-template-outputs.yaml
+-rw-r--r--   0        0        0     1453 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/suspend-template.yaml
+-rw-r--r--   0        0        0     2046 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-mutex-tmpl-level.yaml
+-rw-r--r--   0        0        0     1167 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-mutex-wf-level.yaml
+-rw-r--r--   0        0        0     1598 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-tmpl-level.yaml
+-rw-r--r--   0        0        0     1231 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-wf-level.yaml
+-rw-r--r--   0        0        0     1898 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/template-defaults.yaml
+-rw-r--r--   0        0        0     1480 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/template-on-exit.yaml
+-rw-r--r--   0        0        0     1142 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/timeouts-step.yaml
+-rw-r--r--   0        0        0     1567 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/timeouts-workflow.yaml
+-rw-r--r--   0        0        0     1410 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/volumes-emptydir.yaml
+-rw-r--r--   0        0        0     1957 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/volumes-pvc.yaml
+-rw-r--r--   0        0        0    18252 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/web-ui-resubmit.yaml
+-rw-r--r--   0        0        0     2600 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/webhdfs-input-output-artifacts.yaml
+-rw-r--r--   0        0        0     3475 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/work-avoidance.yaml
+-rw-r--r--   0        0        0     2692 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/workflow-of-workflows.yaml
+-rw-r--r--   0        0        0     4495 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/workflow_from_cronWorkflow.yaml
+-rw-r--r--   0        0        0     1830 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/.gitignore
+-rw-r--r--   0        0        0     1536 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/LICENSE
+-rw-r--r--   0        0        0      340 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/README.md
+-rw-r--r--   0        0        0     1913 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/pyproject.toml
+-rw-r--r--   0        0        0     1800 2020-02-02 00:00:00.000000 nebari_workflow_controller-2023.5.5/PKG-INFO
```

### Comparing `nebari_workflow_controller-2023.5.4/.pre-commit-config.yaml` & `nebari_workflow_controller-2023.5.5/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/.github/workflows/release.yaml` & `nebari_workflow_controller-2023.5.5/.github/workflows/release.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/nebari_workflow_controller/__init__.py` & `nebari_workflow_controller-2023.5.5/nebari_workflow_controller/__init__.py`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/nebari_workflow_controller/__main__.py` & `nebari_workflow_controller-2023.5.5/nebari_workflow_controller/__main__.py`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/nebari_workflow_controller/app.py` & `nebari_workflow_controller-2023.5.5/nebari_workflow_controller/app.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,15 +15,14 @@
 )
 from nebari_workflow_controller.utils import (
     base_return_response,
     find_invalid_volume_mount,
     get_container_keep_portions,
     get_keycloak_user,
     get_spec_keep_portions,
-    get_spec_to_container_portions,
     get_user_pod_spec,
     mutate_template,
     process_unhandled_exception,
 )
 
 logger = logging.getLogger(__name__)
 
@@ -140,31 +139,28 @@
             except NWFCException as e:
                 return return_response(False, message=str(e))
 
             api = client.ApiClient()
 
             container_keep_portions = get_container_keep_portions(user_pod_spec, api)
             spec_keep_portions = get_spec_keep_portions(user_pod_spec, api)
-            spec_to_container_portions = get_spec_to_container_portions(
-                user_pod_spec, api
-            )
 
             if spec["kind"] == "Workflow":
                 templates = modified_spec["spec"]["templates"]
             elif spec["kind"] == "CronWorkflow":
                 templates = modified_spec["spec"]["workflowSpec"]["templates"]
             else:
                 raise Exception("Only expecting Workflow or CronWorkflow")
 
             for template in templates:
                 mutate_template(
                     container_keep_portions,
                     spec_keep_portions,
                     template,
-                    spec_to_container_portions,
+                    # spec_to_template_portions,
                 )
 
             patch = jsonpatch.JsonPatch.from_diff(spec, modified_spec)
             return return_response(
                 allowed=True,
                 patch=patch,
                 patchType="JSONPatch",
```

### Comparing `nebari_workflow_controller-2023.5.4/nebari_workflow_controller/utils.py` & `nebari_workflow_controller-2023.5.5/nebari_workflow_controller/utils.py`

 * *Files 8% similar despite different names*

```diff
@@ -179,23 +179,14 @@
             f"A user pod instance for Jupyterhub user {keycloak_user.username} must be running when workflow starts. No pod found for user {keycloak_user.username}."
         )
 
     jupyter_pod_spec = jupyter_pod_list[0]
     return jupyter_pod_spec
 
 
-def get_spec_to_container_portions(user_pod_spec, api):
-    return [
-        (
-            api.sanitize_for_serialization(user_pod_spec.spec.node_selector),
-            "nodeSelector",
-        )
-    ]
-
-
 def get_spec_keep_portions(user_pod_spec, api):
     return [
         (
             [
                 api.sanitize_for_serialization(iC)
                 for iC in user_pod_spec.spec.init_containers
             ],
@@ -213,14 +204,18 @@
             [
                 api.sanitize_for_serialization(v)
                 for v in user_pod_spec.spec.volumes
                 if not v.name.startswith("kupe-api-access-")
             ],
             "volumes",
         ),
+        (
+            api.sanitize_for_serialization(user_pod_spec.spec.node_selector),
+            "nodeSelector",
+        ),
     ]
 
 
 def recursive_dict_merge(greater_dict, lesser_dict, path=None):
     "merges lesser_dict into greater_dict and assigns to greater_dict, greater_dict value takes precedence in case of conflict between greater and lesser dict"
     if path is None:
         path = []
@@ -274,15 +269,14 @@
     ]
 
 
 def mutate_template(
     container_keep_portions,
     spec_keep_portions,
     template,
-    spec_to_container_portions=None,
 ):
     for value, key in container_keep_portions:
         if "container" not in template:
             continue
 
         if isinstance(value, dict):
             if key in template["container"]:
@@ -306,22 +300,7 @@
         elif isinstance(value, list):
             if key in template:
                 template[key].append(value)
             else:
                 template[key] = value
         else:
             template[key] = value
-
-    if spec_to_container_portions:
-        for value, key in spec_to_container_portions:
-            if isinstance(value, dict):
-                if key in template["container"]:
-                    recursive_dict_merge(template["container"][key], value)
-                else:
-                    template["container"][key] = value
-            elif isinstance(value, list):
-                if key in template["container"]:
-                    template["container"][key].append(value)
-                else:
-                    template["container"][key] = value
-            else:
-                template["container"][key] = value
```

### Comparing `nebari_workflow_controller-2023.5.4/tests/conftest.py` & `nebari_workflow_controller-2023.5.5/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_app.py` & `nebari_workflow_controller-2023.5.5/tests/test_app.py`

 * *Files 2% similar despite different names*

```diff
@@ -76,16 +76,16 @@
         {
             "configMap": {"defaultMode": 420, "name": "jupyterlab-settings"},
             "name": "jupyterlab-settings",
         },
     ]:
         assert volume in mutated_spec["spec"]["templates"][0]["volumes"]
 
-    assert mutated_spec["spec"]["templates"][0]["container"]["nodeSelector"] == {
+    assert mutated_spec["spec"]["templates"][0]["nodeSelector"] == {
         "mylabel": "myValue",
         "cloud.google.com/gke-nodepool": "user",
     }
 
     assert mutated_spec["spec"]["templates"][0]["container"]["resources"] == {
-        "requests": {"cpu": "3000m", "memory": "5368709120"},
-        "limits": {"cpu": "2", "memory": "8589934592"},
+        "requests": {"cpu": "1500m", "memory": "5368709120"},
+        "limits": {"cpu": "3000m", "memory": "8589934592"},
     }
```

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/convert_workflows.py` & `nebari_workflow_controller-2023.5.5/tests/test_data/convert_workflows.py`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/jupyterlab_pod_spec.pkl` & `nebari_workflow_controller-2023.5.5/tests/test_data/jupyterlab_pod_spec.pkl`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_disallowed_conda_mount.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_disallowed_conda_mount.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_disallowed_file_mount.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_disallowed_file_mount.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/container_empty_subPath.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/container_empty_subPath.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/disallowed_volume.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/disallowed_volume.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_disallowed_conda_mount.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_disallowed_conda_mount.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_disallowed_file_mount.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_disallowed_file_mount.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/initContainer_empty_subPath.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/initContainer_empty_subPath.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/invalid/volumes-existing.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/invalid/volumes-existing.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/archive-location.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/archive-location.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/argo_cli_hello_world.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/argo_cli_hello_world.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-artifacts.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-artifacts.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-parameters-from-configmap.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-parameters-from-configmap.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/arguments-parameters.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/arguments-parameters.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-disable-archive.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-disable-archive.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-gc-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-gc-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-passing-subpath.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-passing-subpath.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-passing.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-passing.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-path-placeholders.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-path-placeholders.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifact-repository-ref.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifact-repository-ref.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/artifactory-artifact.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/artifactory-artifact.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/browser_hello_world.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/browser_hello_world.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/ci-output-artifact.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/ci-output-artifact.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/ci.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/ci.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/coinflip-recursive.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/coinflip-recursive.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/coinflip.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/coinflip.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/colored-logs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/colored-logs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditional-artifacts.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditional-artifacts.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditional-parameters.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditional-parameters.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditionals-complex.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditionals-complex.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/conditionals.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/conditionals.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/continue-on-fail.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/continue-on-fail.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/custom-metrics.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/custom-metrics.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemon-nginx.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemon-nginx.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemon-step.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemon-step.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/daemoned-stateful-set-with-service.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/daemoned-stateful-set-with-service.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-coinflip.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-coinflip.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-conditional-artifacts.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-conditional-artifacts.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-conditional-parameters.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-conditional-parameters.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-continue-on-fail.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-continue-on-fail.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-custom-metrics.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-custom-metrics.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-daemon-task.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-daemon-task.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-diamond-steps.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-diamond-steps.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-diamond.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-diamond.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-disable-failFast.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-disable-failFast.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-enhanced-depends.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-enhanced-depends.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-inline-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-inline-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-multiroot.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-multiroot.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-nested.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-nested.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-targets.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-targets.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dag-task-level-timeout.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dag-task-level-timeout.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/data-transformations.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/data-transformations.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/default-pdb-support.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/default-pdb-support.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/dns-config.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/dns-config.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-code-output-variable.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-code-output-variable.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-dag-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-dag-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-slack.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-slack.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-step-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-step-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-with-artifacts.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-with-artifacts.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handler-with-param.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handler-with-param.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/exit-handlers.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/exit-handlers.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-destructure-json.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-destructure-json.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-reusing-verbose-snippets.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-reusing-verbose-snippets.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/expression-tag-template-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/expression-tag-template-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/fibonacci-seq-conditional-param.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/fibonacci-seq-conditional-param.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/forever.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/forever.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/fun-with-gifs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/fun-with-gifs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/gc-ttl.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/gc-ttl.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-outputs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-outputs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters-from-configmap-referenced-as-local-variable.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters-from-configmap-referenced-as-local-variable.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters-from-configmap.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters-from-configmap.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/global-parameters.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/global-parameters.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/handle-large-output-results.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/handle-large-output-results.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hdfs-artifact.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hdfs-artifact.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-hybrid.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-hybrid.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-windows.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-windows.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/hello-world.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/hello-world.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/http-hello-world.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/http-hello-world.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/http-success-condition.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/http-success-condition.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/image-pull-secrets.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/image-pull-secrets.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/influxdb-ci.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/influxdb-ci.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/init-container.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/init-container.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-azure.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-azure.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-gcs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-gcs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-git.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-git.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-http.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-http.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-oss.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-oss.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-raw.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-raw.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/input-artifact-s3.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/input-artifact-s3.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/jupyterflow-override-example.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/jupyterflow-override-example.yaml`

 * *Files 2% similar despite different names*

```diff
@@ -25,18 +25,18 @@
             image: quay.io/nebari/nebari-jupyterlab:2023.1.1
             command:
             - sh
             - '-c'
             args:
             - conda run -n nebari-git-dask python script.py
             resources:
-              requests:
+              limits:
                 cpu: '3000m'
-            nodeSelector:
-              mylabel: myValue
+          nodeSelector:
+            mylabel: myValue
       entrypoint: argosay
   uid: c1bba5c6-2189-41ff-9487-be504c04487b
   userInfo:
     groups:
     - system:serviceaccounts
     - system:serviceaccounts:dev
     - system:authenticated
```

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/jupyterlab_pod.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/jupyterlab_pod.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-jobs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-jobs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-json-patch-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-json-patch-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-orchestration.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-orchestration.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-owner-reference.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-owner-reference.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-patch-basic.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-patch-basic.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-patch.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-patch.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-resource-log-selector.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-resource-log-selector.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-set-owner-reference.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-set-owner-reference.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/k8s-wait-wf.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/k8s-wait-wf.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/key-only-artifact.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/key-only-artifact.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/kubectl_malicious.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/kubectl_malicious.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/label-value-from-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/label-value-from-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/life-cycle-hooks-tmpl-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/life-cycle-hooks-tmpl-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/life-cycle-hooks-wf-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/life-cycle-hooks-wf-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-arbitrary-sequential-steps.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-arbitrary-sequential-steps.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-dag.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-dag.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-maps.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-maps.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-param-argument.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-param-argument.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-param-result.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-param-result.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops-sequence.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops-sequence.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/loops.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/loops.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/map-reduce.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/map-reduce.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/memoize-simple.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/memoize-simple.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/nested-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/nested-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/node-selector.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/node-selector.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-azure.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-azure.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-gcs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-gcs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-artifact-s3.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-artifact-s3.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/output-parameter.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/output-parameter.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-limit.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-limit.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested-dag.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested-dag.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-nested.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-nested.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parallelism-template-limit.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parallelism-template-limit.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation-dag.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation-dag.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation-script.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation-script.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/parameter-aggregation.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/parameter-aggregation.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-gc-strategy-with-label-selector.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-gc-strategy-with-label-selector.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-gc-strategy.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-gc-strategy.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-metadata-wf-field.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-metadata-wf-field.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-metadata.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-metadata.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-from-previous-step.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-from-previous-step.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-patch-wf-tmpl.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-patch-wf-tmpl.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-patch.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-patch.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/pod-spec-yaml-patch.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/pod-spec-yaml-patch.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/recursive-for-loop.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/recursive-for-loop.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resource-delete-with-flags.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resource-delete-with-flags.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resource-flags.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resource-flags.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/resubmit.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/resubmit.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-backoff.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-backoff.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-conditional.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-conditional.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-container-to-completion.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-container-to-completion.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-container.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-container.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-on-error.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-on-error.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-script.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-script.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/retry-with-steps.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/retry-with-steps.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-bash.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-bash.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-javascript.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-javascript.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/scripts-python.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/scripts-python.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/secrets.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/secrets.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar-dind.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar-dind.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar-nginx.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar-nginx.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/sidecar.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/sidecar.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/status-reference.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/status-reference.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/step-level-timeout.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/step-level-timeout.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/steps-inline-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/steps-inline-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/steps.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/steps.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/suspend-template-outputs.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/suspend-template-outputs.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/suspend-template.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/suspend-template.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-mutex-tmpl-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-mutex-tmpl-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-mutex-wf-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-mutex-wf-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-tmpl-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-tmpl-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/synchronization-wf-level.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/synchronization-wf-level.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/template-defaults.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/template-defaults.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/template-on-exit.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/template-on-exit.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/timeouts-step.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/timeouts-step.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/timeouts-workflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/timeouts-workflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/volumes-emptydir.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/volumes-emptydir.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/volumes-pvc.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/volumes-pvc.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/web-ui-resubmit.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/web-ui-resubmit.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/webhdfs-input-output-artifacts.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/webhdfs-input-output-artifacts.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/work-avoidance.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/work-avoidance.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/workflow-of-workflows.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/workflow-of-workflows.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/tests/test_data/requests/valid/workflow_from_cronWorkflow.yaml` & `nebari_workflow_controller-2023.5.5/tests/test_data/requests/valid/workflow_from_cronWorkflow.yaml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/.gitignore` & `nebari_workflow_controller-2023.5.5/.gitignore`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/LICENSE` & `nebari_workflow_controller-2023.5.5/LICENSE`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/pyproject.toml` & `nebari_workflow_controller-2023.5.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `nebari_workflow_controller-2023.5.4/PKG-INFO` & `nebari_workflow_controller-2023.5.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nebari-workflow-controller
-Version: 2023.5.4
+Version: 2023.5.5
 Summary: An admission controller for argo workflows in Nebari
 Project-URL: Documentation, https://github.com/nebari-dev/nebari-workflow-controller
 Project-URL: Source, https://github.com/nebari-dev/nebari-workflow-controller
 Author-email: Nebari development team <internal-it@quansight.com>
 License-Expression: BSD-3-Clause
 License-File: LICENSE
 Keywords: admission-controller,argo-workflows,fastapi,kubernetes,nebari
```

