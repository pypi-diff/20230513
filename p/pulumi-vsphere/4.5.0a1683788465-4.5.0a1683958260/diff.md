# Comparing `tmp/pulumi_vsphere-4.5.0a1683788465.tar.gz` & `tmp/pulumi_vsphere-4.5.0a1683958260.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pulumi_vsphere-4.5.0a1683788465.tar", last modified: Thu May 11 07:08:05 2023, max compression
+gzip compressed data, was "pulumi_vsphere-4.5.0a1683958260.tar", last modified: Sat May 13 06:16:27 2023, max compression
```

## Comparing `pulumi_vsphere-4.5.0a1683788465.tar` & `pulumi_vsphere-4.5.0a1683958260.tar`

### file list

```diff
@@ -1,87 +1,87 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/
--rw-r--r--   0 runner    (1001) docker     (123)     4845 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4518 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/
--rw-r--r--   0 runner    (1001) docker     (123)     9765 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    81397 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)   231990 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)    11620 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_host_group.py
--rw-r--r--   0 runner    (1001) docker     (123)    22943 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_affinity_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)    16038 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_anti_affinity_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)    20097 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_dependency_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)    11628 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_group.py
--rw-r--r--   0 runner    (1001) docker     (123)    21803 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_host_rule.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/config/
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3210 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/config/vars.py
--rw-r--r--   0 runner    (1001) docker     (123)    15087 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/content_library.py
--rw-r--r--   0 runner    (1001) docker     (123)    15640 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/content_library_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     9031 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/custom_attribute.py
--rw-r--r--   0 runner    (1001) docker     (123)    15935 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datacenter.py
--rw-r--r--   0 runner    (1001) docker     (123)    89388 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datastore_cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)    16257 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datastore_cluster_vm_anti_affinity_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)   129818 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/distributed_port_group.py
--rw-r--r--   0 runner    (1001) docker     (123)   257355 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/distributed_virtual_switch.py
--rw-r--r--   0 runner    (1001) docker     (123)    13841 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/dpm_host_override.py
--rw-r--r--   0 runner    (1001) docker     (123)    15127 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/drs_vm_override.py
--rw-r--r--   0 runner    (1001) docker     (123)    12429 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/entity_permissions.py
--rw-r--r--   0 runner    (1001) docker     (123)    21472 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/file.py
--rw-r--r--   0 runner    (1001) docker     (123)    20105 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/folder.py
--rw-r--r--   0 runner    (1001) docker     (123)     5937 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_compute_cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)     5794 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_compute_cluster_host_group.py
--rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_content_library.py
--rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_content_library_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_custom_attribute.py
--rw-r--r--   0 runner    (1001) docker     (123)     3337 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datacenter.py
--rw-r--r--   0 runner    (1001) docker     (123)     4693 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datastore.py
--rw-r--r--   0 runner    (1001) docker     (123)     5112 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datastore_cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)     6814 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_distributed_virtual_switch.py
--rw-r--r--   0 runner    (1001) docker     (123)     6042 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_dynamic.py
--rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_folder.py
--rw-r--r--   0 runner    (1001) docker     (123)     4758 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host.py
--rw-r--r--   0 runner    (1001) docker     (123)     6430 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host_pci_device.py
--rw-r--r--   0 runner    (1001) docker     (123)     4903 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host_thumbprint.py
--rw-r--r--   0 runner    (1001) docker     (123)     5153 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_license.py
--rw-r--r--   0 runner    (1001) docker     (123)     7058 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_network.py
--rw-r--r--   0 runner    (1001) docker     (123)    31941 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_ovf_vm_template.py
--rw-r--r--   0 runner    (1001) docker     (123)     3395 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_policy.py
--rw-r--r--   0 runner    (1001) docker     (123)     6782 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_resource_pool.py
--rw-r--r--   0 runner    (1001) docker     (123)     5136 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_role.py
--rw-r--r--   0 runner    (1001) docker     (123)     4756 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_tag.py
--rw-r--r--   0 runner    (1001) docker     (123)     4959 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_tag_category.py
--rw-r--r--   0 runner    (1001) docker     (123)     4428 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_vapp_container.py
--rw-r--r--   0 runner    (1001) docker     (123)    54162 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_virtual_machine.py
--rw-r--r--   0 runner    (1001) docker     (123)     6098 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_vmfs_disks.py
--rw-r--r--   0 runner    (1001) docker     (123)    58963 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/ha_vm_override.py
--rw-r--r--   0 runner    (1001) docker     (123)    43166 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host.py
--rw-r--r--   0 runner    (1001) docker     (123)    56784 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host_port_group.py
--rw-r--r--   0 runner    (1001) docker     (123)    60596 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host_virtual_switch.py
--rw-r--r--   0 runner    (1001) docker     (123)    12752 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/license.py
--rw-r--r--   0 runner    (1001) docker     (123)    46325 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/nas_datastore.py
--rw-r--r--   0 runner    (1001) docker     (123)    81214 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/outputs.py
--rw-r--r--   0 runner    (1001) docker     (123)    20381 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/provider.py
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/pulumi-plugin.json
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    54091 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/resource_pool.py
--rw-r--r--   0 runner    (1001) docker     (123)     8528 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/role.py
--rw-r--r--   0 runner    (1001) docker     (123)    20828 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/storage_drs_vm_override.py
--rw-r--r--   0 runner    (1001) docker     (123)     9943 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/tag.py
--rw-r--r--   0 runner    (1001) docker     (123)    13982 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/tag_category.py
--rw-r--r--   0 runner    (1001) docker     (123)    48255 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vapp_container.py
--rw-r--r--   0 runner    (1001) docker     (123)    29555 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vapp_entity.py
--rw-r--r--   0 runner    (1001) docker     (123)    22447 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_disk.py
--rw-r--r--   0 runner    (1001) docker     (123)   245191 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_machine.py
--rw-r--r--   0 runner    (1001) docker     (123)    23926 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_machine_snapshot.py
--rw-r--r--   0 runner    (1001) docker     (123)    20958 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vm_storage_policy.py
--rw-r--r--   0 runner    (1001) docker     (123)    32719 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vmfs_datastore.py
--rw-r--r--   0 runner    (1001) docker     (123)    27602 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vnic.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4845 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-11 07:08:05.882517 pulumi_vsphere-4.5.0a1683788465/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2113 2023-05-11 07:08:05.000000 pulumi_vsphere-4.5.0a1683788465/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/
+-rw-r--r--   0 runner    (1001) docker     (123)     4845 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4518 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/
+-rw-r--r--   0 runner    (1001) docker     (123)     9765 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81397 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)   231990 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11620 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_host_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22943 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_affinity_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16038 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_anti_affinity_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20097 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_dependency_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11628 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21803 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_host_rule.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/config/
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3210 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/config/vars.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15087 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/content_library.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15640 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/content_library_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9031 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/custom_attribute.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15935 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datacenter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    89388 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datastore_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16257 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datastore_cluster_vm_anti_affinity_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)   129818 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/distributed_port_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)   257355 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/distributed_virtual_switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13841 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/dpm_host_override.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15127 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/drs_vm_override.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12429 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/entity_permissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21472 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20105 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/folder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5937 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_compute_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5794 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_compute_cluster_host_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_content_library.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_content_library_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4309 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_custom_attribute.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3337 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datacenter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4693 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datastore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5112 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datastore_cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6814 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_distributed_virtual_switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6042 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_dynamic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_folder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4758 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6430 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host_pci_device.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4903 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host_thumbprint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5153 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_license.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7058 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_network.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31941 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_ovf_vm_template.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3395 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_policy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6782 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_resource_pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5136 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_role.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4756 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_tag.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4959 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_tag_category.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4428 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_vapp_container.py
+-rw-r--r--   0 runner    (1001) docker     (123)    54162 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_virtual_machine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6098 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_vmfs_disks.py
+-rw-r--r--   0 runner    (1001) docker     (123)    58963 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/ha_vm_override.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43166 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host.py
+-rw-r--r--   0 runner    (1001) docker     (123)    56784 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host_port_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)    60596 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host_virtual_switch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12752 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/license.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46325 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/nas_datastore.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81214 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20381 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/pulumi-plugin.json
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    54091 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/resource_pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8528 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/role.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20828 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/storage_drs_vm_override.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9943 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/tag.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13982 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/tag_category.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48255 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vapp_container.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29555 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vapp_entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22447 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_disk.py
+-rw-r--r--   0 runner    (1001) docker     (123)   245191 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_machine.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23926 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_machine_snapshot.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20958 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vm_storage_policy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    32719 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vmfs_datastore.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27602 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vnic.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4845 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2783 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-13 06:16:27.568825 pulumi_vsphere-4.5.0a1683958260/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2113 2023-05-13 06:16:27.000000 pulumi_vsphere-4.5.0a1683958260/setup.py
```

### Comparing `pulumi_vsphere-4.5.0a1683788465/PKG-INFO` & `pulumi_vsphere-4.5.0a1683958260/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi_vsphere
-Version: 4.5.0a1683788465
+Version: 4.5.0a1683958260
 Summary: A Pulumi package for creating vsphere resources
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-vsphere
 Keywords: pulumi vsphere
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `pulumi_vsphere-4.5.0a1683788465/README.md` & `pulumi_vsphere-4.5.0a1683958260/README.md`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/__init__.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/_inputs.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/_utilities.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/_utilities.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_host_group.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_host_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_affinity_rule.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_affinity_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_anti_affinity_rule.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_anti_affinity_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_dependency_rule.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_dependency_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_group.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/compute_cluster_vm_host_rule.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/compute_cluster_vm_host_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/config/vars.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/config/vars.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/content_library.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/content_library.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/content_library_item.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/content_library_item.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/custom_attribute.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/custom_attribute.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datacenter.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datacenter.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datastore_cluster.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datastore_cluster.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/datastore_cluster_vm_anti_affinity_rule.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/datastore_cluster_vm_anti_affinity_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/distributed_port_group.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/distributed_port_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/distributed_virtual_switch.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/distributed_virtual_switch.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/dpm_host_override.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/dpm_host_override.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/drs_vm_override.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/drs_vm_override.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/entity_permissions.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/entity_permissions.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/file.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/file.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/folder.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/folder.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_compute_cluster.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_compute_cluster.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_compute_cluster_host_group.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_compute_cluster_host_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_content_library.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_content_library.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_content_library_item.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_content_library_item.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_custom_attribute.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_custom_attribute.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datacenter.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datacenter.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datastore.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datastore.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_datastore_cluster.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_datastore_cluster.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_distributed_virtual_switch.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_distributed_virtual_switch.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_dynamic.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_dynamic.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_folder.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_folder.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host_pci_device.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host_pci_device.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_host_thumbprint.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_host_thumbprint.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_license.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_license.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_network.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_network.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_ovf_vm_template.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_ovf_vm_template.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_policy.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_resource_pool.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_resource_pool.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_role.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_role.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_tag.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_tag.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_tag_category.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_tag_category.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_vapp_container.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_vapp_container.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_virtual_machine.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_virtual_machine.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/get_vmfs_disks.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/get_vmfs_disks.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/ha_vm_override.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/ha_vm_override.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host_port_group.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host_port_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/host_virtual_switch.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/host_virtual_switch.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/license.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/license.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/nas_datastore.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/nas_datastore.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/outputs.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/provider.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/provider.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/resource_pool.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/resource_pool.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/role.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/role.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/storage_drs_vm_override.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/storage_drs_vm_override.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/tag.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/tag.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/tag_category.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/tag_category.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vapp_container.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vapp_container.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vapp_entity.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vapp_entity.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_disk.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_disk.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_machine.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_machine.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/virtual_machine_snapshot.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/virtual_machine_snapshot.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vm_storage_policy.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vm_storage_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vmfs_datastore.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vmfs_datastore.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere/vnic.py` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere/vnic.py`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/PKG-INFO` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi-vsphere
-Version: 4.5.0a1683788465
+Version: 4.5.0a1683958260
 Summary: A Pulumi package for creating vsphere resources
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-vsphere
 Keywords: pulumi vsphere
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `pulumi_vsphere-4.5.0a1683788465/pulumi_vsphere.egg-info/SOURCES.txt` & `pulumi_vsphere-4.5.0a1683958260/pulumi_vsphere.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pulumi_vsphere-4.5.0a1683788465/setup.py` & `pulumi_vsphere-4.5.0a1683958260/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 
 import errno
 from setuptools import setup, find_packages
 from setuptools.command.install import install
 from subprocess import check_call
 
 
-VERSION = "4.5.0a1683788465"
-PLUGIN_VERSION = "4.5.0-alpha.1683788465+08276032"
+VERSION = "4.5.0a1683958260"
+PLUGIN_VERSION = "4.5.0-alpha.1683958260+f0e0d13f"
 
 class InstallPluginCommand(install):
     def run(self):
         install.run(self)
         try:
             check_call(['pulumi', 'plugin', 'install', 'resource', 'vsphere', PLUGIN_VERSION])
         except OSError as error:
```

