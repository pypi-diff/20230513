# Comparing `tmp/pulumi_github-5.9.0a1683610445.tar.gz` & `tmp/pulumi_github-5.9.0a1683752304.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pulumi_github-5.9.0a1683610445.tar", last modified: Tue May  9 05:43:07 2023, max compression
+gzip compressed data, was "pulumi_github-5.9.0a1683752304.tar", last modified: Wed May 10 21:12:33 2023, max compression
```

## Comparing `pulumi_github-5.9.0a1683610445.tar` & `pulumi_github-5.9.0a1683752304.tar`

### file list

```diff
@@ -1,126 +1,127 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/
--rw-r--r--   0 runner    (1001) docker     (123)     2908 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/pulumi_github/
--rw-r--r--   0 runner    (1001) docker     (123)    15482 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    63092 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)    19178 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_environment_secret.py
--rw-r--r--   0 runner    (1001) docker     (123)    16013 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_environment_variable.py
--rw-r--r--   0 runner    (1001) docker     (123)     9151 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_oidc_subject_claim_customization_template.py
--rw-r--r--   0 runner    (1001) docker     (123)    20745 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_permissions.py
--rw-r--r--   0 runner    (1001) docker     (123)    22394 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_secret.py
--rw-r--r--   0 runner    (1001) docker     (123)    10898 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_secret_repositories.py
--rw-r--r--   0 runner    (1001) docker     (123)    17738 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_variable.py
--rw-r--r--   0 runner    (1001) docker     (123)     9995 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_access_level.py
--rw-r--r--   0 runner    (1001) docker     (123)    14803 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_oidc_subject_claim_customization_template.py
--rw-r--r--   0 runner    (1001) docker     (123)    16292 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_permissions.py
--rw-r--r--   0 runner    (1001) docker     (123)    25998 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_runner_group.py
--rw-r--r--   0 runner    (1001) docker     (123)    15530 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_secret.py
--rw-r--r--   0 runner    (1001) docker     (123)    12596 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/actions_variable.py
--rw-r--r--   0 runner    (1001) docker     (123)    10615 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/app_installation_repositories.py
--rw-r--r--   0 runner    (1001) docker     (123)    11169 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/app_installation_repository.py
--rw-r--r--   0 runner    (1001) docker     (123)    16865 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/branch.py
--rw-r--r--   0 runner    (1001) docker     (123)    12115 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/branch_default.py
--rw-r--r--   0 runner    (1001) docker     (123)    44058 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/branch_protection.py
--rw-r--r--   0 runner    (1001) docker     (123)    31972 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/branch_protection_v3.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/pulumi_github/config/
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/config/outputs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2371 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/config/vars.py
--rw-r--r--   0 runner    (1001) docker     (123)    18662 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_organization_secret.py
--rw-r--r--   0 runner    (1001) docker     (123)     9223 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_organization_secret_repositories.py
--rw-r--r--   0 runner    (1001) docker     (123)    14359 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_secret.py
--rw-r--r--   0 runner    (1001) docker     (123)    10110 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/emu_group_mapping.py
--rw-r--r--   0 runner    (1001) docker     (123)    14476 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/enterprise_organization.py
--rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_environment_secrets.py
--rw-r--r--   0 runner    (1001) docker     (123)     5143 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_environment_variables.py
--rw-r--r--   0 runner    (1001) docker     (123)     3137 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_oidc_subject_claim_customization_template.py
--rw-r--r--   0 runner    (1001) docker     (123)     3085 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_public_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     3141 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_registration_token.py
--rw-r--r--   0 runner    (1001) docker     (123)     2549 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_secrets.py
--rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_variables.py
--rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_public_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_registration_token.py
--rw-r--r--   0 runner    (1001) docker     (123)     5164 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_repository_oidc_subject_claim_customization_template.py
--rw-r--r--   0 runner    (1001) docker     (123)     4213 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_secrets.py
--rw-r--r--   0 runner    (1001) docker     (123)     4304 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_variables.py
--rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_branch.py
--rw-r--r--   0 runner    (1001) docker     (123)     5236 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_collaborators.py
--rw-r--r--   0 runner    (1001) docker     (123)     3137 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_organization_public_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     2608 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_organization_secrets.py
--rw-r--r--   0 runner    (1001) docker     (123)     3372 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_public_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     4321 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_secrets.py
--rw-r--r--   0 runner    (1001) docker     (123)     4647 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_enterprise.py
--rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_external_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)     4071 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_github_app.py
--rw-r--r--   0 runner    (1001) docker     (123)    14508 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_ip_ranges.py
--rw-r--r--   0 runner    (1001) docker     (123)     3177 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_issue_labels.py
--rw-r--r--   0 runner    (1001) docker     (123)     5557 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_membership.py
--rw-r--r--   0 runner    (1001) docker     (123)     7246 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_organization.py
--rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_ip_allow_list.py
--rw-r--r--   0 runner    (1001) docker     (123)     2622 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_team_sync_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)     6941 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_teams.py
--rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_webhooks.py
--rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_ref.py
--rw-r--r--   0 runner    (1001) docker     (123)    13103 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_release.py
--rw-r--r--   0 runner    (1001) docker     (123)     7590 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repositories.py
--rw-r--r--   0 runner    (1001) docker     (123)    20628 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository.py
--rw-r--r--   0 runner    (1001) docker     (123)     6121 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_branches.py
--rw-r--r--   0 runner    (1001) docker     (123)     3758 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_deploy_keys.py
--rw-r--r--   0 runner    (1001) docker     (123)     8219 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_file.py
--rw-r--r--   0 runner    (1001) docker     (123)     6319 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_milestone.py
--rw-r--r--   0 runner    (1001) docker     (123)    11966 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_pull_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     9795 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_pull_requests.py
--rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_teams.py
--rw-r--r--   0 runner    (1001) docker     (123)     3647 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_webhooks.py
--rw-r--r--   0 runner    (1001) docker     (123)     2151 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_ssh_keys.py
--rw-r--r--   0 runner    (1001) docker     (123)     8735 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_team.py
--rw-r--r--   0 runner    (1001) docker     (123)     5400 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)    11971 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_user.py
--rw-r--r--   0 runner    (1001) docker     (123)     5157 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/get_users.py
--rw-r--r--   0 runner    (1001) docker     (123)    20918 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/issue.py
--rw-r--r--   0 runner    (1001) docker     (123)    13277 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/issue_label.py
--rw-r--r--   0 runner    (1001) docker     (123)     9894 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/membership.py
--rw-r--r--   0 runner    (1001) docker     (123)     6674 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/organization_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     8955 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/organization_project.py
--rw-r--r--   0 runner    (1001) docker     (123)     6958 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/organization_security_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)    79808 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/organization_settings.py
--rw-r--r--   0 runner    (1001) docker     (123)    15058 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/organization_webhook.py
--rw-r--r--   0 runner    (1001) docker     (123)   103800 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/outputs.py
--rw-r--r--   0 runner    (1001) docker     (123)    15743 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/project_card.py
--rw-r--r--   0 runner    (1001) docker     (123)     9660 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/project_column.py
--rw-r--r--   0 runner    (1001) docker     (123)    14143 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/provider.py
--rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/pulumi-plugin.json
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    28755 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/release.py
--rw-r--r--   0 runner    (1001) docker     (123)   107291 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository.py
--rw-r--r--   0 runner    (1001) docker     (123)    16391 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_autolink_reference.py
--rw-r--r--   0 runner    (1001) docker     (123)    21061 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_collaborator.py
--rw-r--r--   0 runner    (1001) docker     (123)    17395 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_collaborators.py
--rw-r--r--   0 runner    (1001) docker     (123)    13699 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_deploy_key.py
--rw-r--r--   0 runner    (1001) docker     (123)    17882 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_environment.py
--rw-r--r--   0 runner    (1001) docker     (123)    27314 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_file.py
--rw-r--r--   0 runner    (1001) docker     (123)    17109 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_milestone.py
--rw-r--r--   0 runner    (1001) docker     (123)    11063 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_project.py
--rw-r--r--   0 runner    (1001) docker     (123)    28682 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_pull_request.py
--rw-r--r--   0 runner    (1001) docker     (123)    10676 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_tag_protection.py
--rw-r--r--   0 runner    (1001) docker     (123)    17190 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/repository_webhook.py
--rw-r--r--   0 runner    (1001) docker     (123)    22137 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team.py
--rw-r--r--   0 runner    (1001) docker     (123)    11019 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team_members.py
--rw-r--r--   0 runner    (1001) docker     (123)    11623 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team_membership.py
--rw-r--r--   0 runner    (1001) docker     (123)    15177 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team_repository.py
--rw-r--r--   0 runner    (1001) docker     (123)    16613 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team_settings.py
--rw-r--r--   0 runner    (1001) docker     (123)    10810 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/team_sync_group_mapping.py
--rw-r--r--   0 runner    (1001) docker     (123)     9761 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/user_gpg_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     8960 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/user_invitation_accepter.py
--rw-r--r--   0 runner    (1001) docker     (123)     9854 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github/user_ssh_key.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2908 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4633 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-09 05:43:07.736281 pulumi_github-5.9.0a1683610445/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2155 2023-05-09 05:43:07.000000 pulumi_github-5.9.0a1683610445/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/
+-rw-r--r--   0 runner    (1001) docker     (123)     2908 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/pulumi_github/
+-rw-r--r--   0 runner    (1001) docker     (123)    15525 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    63092 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8081 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19178 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_environment_secret.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16013 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_environment_variable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9151 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_oidc_subject_claim_customization_template.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20745 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_permissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22394 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_secret.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10898 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_secret_repositories.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17738 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_variable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9995 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_access_level.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14803 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_oidc_subject_claim_customization_template.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16292 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_permissions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25998 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_runner_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15530 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_secret.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12596 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/actions_variable.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10615 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/app_installation_repositories.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11169 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/app_installation_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16865 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/branch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12115 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/branch_default.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44058 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/branch_protection.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31972 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/branch_protection_v3.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/pulumi_github/config/
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/config/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2889 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/config/vars.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18662 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_organization_secret.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9223 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_organization_secret_repositories.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14359 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_secret.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10110 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/emu_group_mapping.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14654 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/enterprise_organization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_environment_secrets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5143 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_environment_variables.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3137 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_oidc_subject_claim_customization_template.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3085 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_public_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3141 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_registration_token.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2549 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_secrets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2611 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_variables.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_public_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4374 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_registration_token.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5164 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_repository_oidc_subject_claim_customization_template.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4213 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_secrets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4304 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_variables.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4738 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_branch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3743 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_branch_protection_rules.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5236 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_collaborators.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3137 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_organization_public_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2608 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_organization_secrets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3372 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_public_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4321 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_secrets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4647 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_enterprise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_external_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4071 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_github_app.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14508 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_ip_ranges.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3177 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_issue_labels.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5557 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_membership.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7246 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_organization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_ip_allow_list.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2622 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_team_sync_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6941 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_teams.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2574 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_webhooks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_ref.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13103 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_release.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7590 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repositories.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20628 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6121 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_branches.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3758 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_deploy_keys.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8219 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6319 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_milestone.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11966 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_pull_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9795 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_pull_requests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_teams.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3647 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_webhooks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2151 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_ssh_keys.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8735 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_team.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5400 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11971 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_user.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5157 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/get_users.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20918 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/issue.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13277 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/issue_label.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9894 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/membership.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6674 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/organization_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8955 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/organization_project.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6958 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/organization_security_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)    79808 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/organization_settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15058 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/organization_webhook.py
+-rw-r--r--   0 runner    (1001) docker     (123)   104294 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15743 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/project_card.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9660 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/project_column.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16240 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/pulumi-plugin.json
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    28755 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/release.py
+-rw-r--r--   0 runner    (1001) docker     (123)   107291 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16391 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_autolink_reference.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21061 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_collaborator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17395 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_collaborators.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13699 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_deploy_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17882 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_environment.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27314 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_file.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17109 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_milestone.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11063 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_project.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28682 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_pull_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10676 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_tag_protection.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17190 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/repository_webhook.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22399 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11273 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team_members.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11921 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team_membership.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15499 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16613 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team_settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10810 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/team_sync_group_mapping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9761 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/user_gpg_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8960 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/user_invitation_accepter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9854 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github/user_ssh_key.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2908 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4678 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-10 21:12:33.662678 pulumi_github-5.9.0a1683752304/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2155 2023-05-10 21:12:33.000000 pulumi_github-5.9.0a1683752304/setup.py
```

### Comparing `pulumi_github-5.9.0a1683610445/PKG-INFO` & `pulumi_github-5.9.0a1683752304/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi_github
-Version: 5.9.0a1683610445
+Version: 5.9.0a1683752304
 Summary: A Pulumi package for creating and managing github cloud resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-github
 Keywords: pulumi github
 Platform: UNKNOWN
 Requires-Python: >=3.7
```

### Comparing `pulumi_github-5.9.0a1683610445/README.md` & `pulumi_github-5.9.0a1683752304/README.md`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/__init__.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -38,14 +38,15 @@
 from .get_actions_organization_variables import *
 from .get_actions_public_key import *
 from .get_actions_registration_token import *
 from .get_actions_repository_oidc_subject_claim_customization_template import *
 from .get_actions_secrets import *
 from .get_actions_variables import *
 from .get_branch import *
+from .get_branch_protection_rules import *
 from .get_collaborators import *
 from .get_dependabot_organization_public_key import *
 from .get_dependabot_organization_secrets import *
 from .get_dependabot_public_key import *
 from .get_dependabot_secrets import *
 from .get_enterprise import *
 from .get_external_groups import *
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/_inputs.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/_utilities.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/_utilities.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_environment_secret.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_environment_secret.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_environment_variable.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_environment_variable.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_oidc_subject_claim_customization_template.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_oidc_subject_claim_customization_template.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_permissions.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_permissions.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_secret.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_secret.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_secret_repositories.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_secret_repositories.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_organization_variable.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_organization_variable.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_access_level.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_access_level.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_oidc_subject_claim_customization_template.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_oidc_subject_claim_customization_template.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_repository_permissions.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_repository_permissions.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_runner_group.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_runner_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_secret.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_secret.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/actions_variable.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/actions_variable.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/app_installation_repositories.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/app_installation_repositories.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/app_installation_repository.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/app_installation_repository.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/branch.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/branch.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/branch_default.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/branch_default.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/branch_protection.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/branch_protection.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/branch_protection_v3.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/branch_protection_v3.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/config/outputs.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/config/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/config/vars.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/config/vars.py`

 * *Files 12% similar despite different names*

```diff
@@ -49,14 +49,23 @@
     def owner(self) -> Optional[str]:
         """
         The GitHub owner name to manage. Use this field instead of `organization` when managing individual accounts.
         """
         return __config__.get('owner')
 
     @property
+    def parallel_requests(self) -> Optional[bool]:
+        """
+        Allow the provider to make parallel API calls to GitHub. You may want to set it to true when you have a private Github
+        Enterprise without strict rate limits. Although, it is not possible to enable this setting on github.com because we
+        enforce the respect of github.com's best practices to avoid hitting abuse rate limitsDefaults to false if not set
+        """
+        return __config__.get_bool('parallelRequests')
+
+    @property
     def read_delay_ms(self) -> Optional[int]:
         """
         Amount of time in milliseconds to sleep in between non-write requests to GitHub API. Defaults to 0ms if not set.
         """
         return __config__.get_int('readDelayMs')
 
     @property
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_organization_secret.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_organization_secret.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_organization_secret_repositories.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_organization_secret_repositories.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/dependabot_secret.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/dependabot_secret.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/emu_group_mapping.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/emu_group_mapping.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/enterprise_organization.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/enterprise_organization.py`

 * *Files 2% similar despite different names*

```diff
@@ -192,14 +192,16 @@
                  admin_logins: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]] = None,
                  billing_email: Optional[pulumi.Input[str]] = None,
                  description: Optional[pulumi.Input[str]] = None,
                  enterprise_id: Optional[pulumi.Input[str]] = None,
                  name: Optional[pulumi.Input[str]] = None,
                  __props__=None):
         """
+        This resource allows you to create and manage a GitHub enterprise organization.
+
         ## Example Usage
 
         ```python
         import pulumi
         import pulumi_github as github
 
         org = github.EnterpriseOrganization("org",
@@ -224,14 +226,16 @@
         ...
     @overload
     def __init__(__self__,
                  resource_name: str,
                  args: EnterpriseOrganizationArgs,
                  opts: Optional[pulumi.ResourceOptions] = None):
         """
+        This resource allows you to create and manage a GitHub enterprise organization.
+
         ## Example Usage
 
         ```python
         import pulumi
         import pulumi_github as github
 
         org = github.EnterpriseOrganization("org",
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_environment_secrets.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_environment_secrets.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_environment_variables.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_environment_variables.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_oidc_subject_claim_customization_template.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_oidc_subject_claim_customization_template.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_public_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_public_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_registration_token.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_registration_token.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_secrets.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_secrets.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_organization_variables.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_organization_variables.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_public_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_public_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_registration_token.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_registration_token.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_repository_oidc_subject_claim_customization_template.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_repository_oidc_subject_claim_customization_template.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_secrets.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_secrets.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_actions_variables.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_actions_variables.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_branch.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_branch.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_collaborators.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_collaborators.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_organization_public_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_organization_public_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_organization_secrets.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_organization_secrets.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_public_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_public_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_dependabot_secrets.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_dependabot_secrets.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_enterprise.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_enterprise.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_external_groups.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_external_groups.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_github_app.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_github_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_ip_ranges.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_ip_ranges.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_issue_labels.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_issue_labels.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_membership.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_membership.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_organization.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_organization.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_ip_allow_list.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_ip_allow_list.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_team_sync_groups.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_team_sync_groups.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_teams.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_teams.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_organization_webhooks.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_organization_webhooks.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_ref.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_ref.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_release.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_release.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repositories.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repositories.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_branches.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_branches.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_deploy_keys.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_deploy_keys.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_file.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_file.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_milestone.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_milestone.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_pull_request.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_pull_request.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_pull_requests.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_pull_requests.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_teams.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_teams.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_repository_webhooks.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_repository_webhooks.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_ssh_keys.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_ssh_keys.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_team.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_team.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_tree.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_tree.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_user.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_user.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/get_users.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/get_users.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/issue.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/issue.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/issue_label.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/issue_label.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/membership.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/membership.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/organization_block.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/organization_block.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/organization_project.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/organization_project.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/organization_security_manager.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/organization_security_manager.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/organization_settings.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/organization_settings.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/organization_webhook.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/organization_webhook.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/outputs.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/outputs.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,14 +38,15 @@
     'TeamSyncGroupMappingGroup',
     'GetActionsEnvironmentSecretsSecretResult',
     'GetActionsEnvironmentVariablesVariableResult',
     'GetActionsOrganizationSecretsSecretResult',
     'GetActionsOrganizationVariablesVariableResult',
     'GetActionsSecretsSecretResult',
     'GetActionsVariablesVariableResult',
+    'GetBranchProtectionRulesRuleResult',
     'GetCollaboratorsCollaboratorResult',
     'GetDependabotOrganizationSecretsSecretResult',
     'GetDependabotSecretsSecretResult',
     'GetExternalGroupsExternalGroupResult',
     'GetIssueLabelsLabelResult',
     'GetOrganizationIpAllowListIpAllowListResult',
     'GetOrganizationTeamSyncGroupsGroupResult',
@@ -1683,14 +1684,32 @@
         """
         Value of the variable
         """
         return pulumi.get(self, "value")
 
 
 @pulumi.output_type
+class GetBranchProtectionRulesRuleResult(dict):
+    def __init__(__self__, *,
+                 pattern: str):
+        """
+        :param str pattern: Identifies the protection rule pattern.
+        """
+        pulumi.set(__self__, "pattern", pattern)
+
+    @property
+    @pulumi.getter
+    def pattern(self) -> str:
+        """
+        Identifies the protection rule pattern.
+        """
+        return pulumi.get(self, "pattern")
+
+
+@pulumi.output_type
 class GetCollaboratorsCollaboratorResult(dict):
     def __init__(__self__, *,
                  events_url: str,
                  followers_url: str,
                  following_url: str,
                  gists_url: str,
                  html_url: str,
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/project_card.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/project_card.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/project_column.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/project_column.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/provider.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/provider.py`

 * *Files 22% similar despite different names*

```diff
@@ -16,25 +16,29 @@
 class ProviderArgs:
     def __init__(__self__, *,
                  app_auth: Optional[pulumi.Input['ProviderAppAuthArgs']] = None,
                  base_url: Optional[pulumi.Input[str]] = None,
                  insecure: Optional[pulumi.Input[bool]] = None,
                  organization: Optional[pulumi.Input[str]] = None,
                  owner: Optional[pulumi.Input[str]] = None,
+                 parallel_requests: Optional[pulumi.Input[bool]] = None,
                  read_delay_ms: Optional[pulumi.Input[int]] = None,
                  token: Optional[pulumi.Input[str]] = None,
                  write_delay_ms: Optional[pulumi.Input[int]] = None):
         """
         The set of arguments for constructing a Provider resource.
         :param pulumi.Input['ProviderAppAuthArgs'] app_auth: The GitHub App credentials used to connect to GitHub. Conflicts with `token`. Anonymous mode is enabled if both `token`
                and `app_auth` are not set.
         :param pulumi.Input[str] base_url: The GitHub Base API URL
         :param pulumi.Input[bool] insecure: Enable `insecure` mode for testing purposes
         :param pulumi.Input[str] organization: The GitHub organization name to manage. Use this field instead of `owner` when managing organization accounts.
         :param pulumi.Input[str] owner: The GitHub owner name to manage. Use this field instead of `organization` when managing individual accounts.
+        :param pulumi.Input[bool] parallel_requests: Allow the provider to make parallel API calls to GitHub. You may want to set it to true when you have a private Github
+               Enterprise without strict rate limits. Although, it is not possible to enable this setting on github.com because we
+               enforce the respect of github.com's best practices to avoid hitting abuse rate limitsDefaults to false if not set
         :param pulumi.Input[int] read_delay_ms: Amount of time in milliseconds to sleep in between non-write requests to GitHub API. Defaults to 0ms if not set.
         :param pulumi.Input[str] token: The OAuth token used to connect to GitHub. Anonymous mode is enabled if both `token` and `app_auth` are not set.
         :param pulumi.Input[int] write_delay_ms: Amount of time in milliseconds to sleep in between writes to GitHub API. Defaults to 1000ms or 1s if not set.
         """
         if app_auth is not None:
             pulumi.set(__self__, "app_auth", app_auth)
         if base_url is None:
@@ -46,14 +50,16 @@
         if organization is not None:
             warnings.warn("""Use owner (or GITHUB_OWNER) instead of organization (or GITHUB_ORGANIZATION)""", DeprecationWarning)
             pulumi.log.warn("""organization is deprecated: Use owner (or GITHUB_OWNER) instead of organization (or GITHUB_ORGANIZATION)""")
         if organization is not None:
             pulumi.set(__self__, "organization", organization)
         if owner is not None:
             pulumi.set(__self__, "owner", owner)
+        if parallel_requests is not None:
+            pulumi.set(__self__, "parallel_requests", parallel_requests)
         if read_delay_ms is not None:
             pulumi.set(__self__, "read_delay_ms", read_delay_ms)
         if token is not None:
             pulumi.set(__self__, "token", token)
         if write_delay_ms is not None:
             pulumi.set(__self__, "write_delay_ms", write_delay_ms)
 
@@ -115,14 +121,28 @@
         return pulumi.get(self, "owner")
 
     @owner.setter
     def owner(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "owner", value)
 
     @property
+    @pulumi.getter(name="parallelRequests")
+    def parallel_requests(self) -> Optional[pulumi.Input[bool]]:
+        """
+        Allow the provider to make parallel API calls to GitHub. You may want to set it to true when you have a private Github
+        Enterprise without strict rate limits. Although, it is not possible to enable this setting on github.com because we
+        enforce the respect of github.com's best practices to avoid hitting abuse rate limitsDefaults to false if not set
+        """
+        return pulumi.get(self, "parallel_requests")
+
+    @parallel_requests.setter
+    def parallel_requests(self, value: Optional[pulumi.Input[bool]]):
+        pulumi.set(self, "parallel_requests", value)
+
+    @property
     @pulumi.getter(name="readDelayMs")
     def read_delay_ms(self) -> Optional[pulumi.Input[int]]:
         """
         Amount of time in milliseconds to sleep in between non-write requests to GitHub API. Defaults to 0ms if not set.
         """
         return pulumi.get(self, "read_delay_ms")
 
@@ -161,14 +181,15 @@
                  resource_name: str,
                  opts: Optional[pulumi.ResourceOptions] = None,
                  app_auth: Optional[pulumi.Input[pulumi.InputType['ProviderAppAuthArgs']]] = None,
                  base_url: Optional[pulumi.Input[str]] = None,
                  insecure: Optional[pulumi.Input[bool]] = None,
                  organization: Optional[pulumi.Input[str]] = None,
                  owner: Optional[pulumi.Input[str]] = None,
+                 parallel_requests: Optional[pulumi.Input[bool]] = None,
                  read_delay_ms: Optional[pulumi.Input[int]] = None,
                  token: Optional[pulumi.Input[str]] = None,
                  write_delay_ms: Optional[pulumi.Input[int]] = None,
                  __props__=None):
         """
         The provider type for the github package. By default, resources use package-wide configuration
         settings, however an explicit `Provider` instance may be created and passed during resource
@@ -179,14 +200,17 @@
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[pulumi.InputType['ProviderAppAuthArgs']] app_auth: The GitHub App credentials used to connect to GitHub. Conflicts with `token`. Anonymous mode is enabled if both `token`
                and `app_auth` are not set.
         :param pulumi.Input[str] base_url: The GitHub Base API URL
         :param pulumi.Input[bool] insecure: Enable `insecure` mode for testing purposes
         :param pulumi.Input[str] organization: The GitHub organization name to manage. Use this field instead of `owner` when managing organization accounts.
         :param pulumi.Input[str] owner: The GitHub owner name to manage. Use this field instead of `organization` when managing individual accounts.
+        :param pulumi.Input[bool] parallel_requests: Allow the provider to make parallel API calls to GitHub. You may want to set it to true when you have a private Github
+               Enterprise without strict rate limits. Although, it is not possible to enable this setting on github.com because we
+               enforce the respect of github.com's best practices to avoid hitting abuse rate limitsDefaults to false if not set
         :param pulumi.Input[int] read_delay_ms: Amount of time in milliseconds to sleep in between non-write requests to GitHub API. Defaults to 0ms if not set.
         :param pulumi.Input[str] token: The OAuth token used to connect to GitHub. Anonymous mode is enabled if both `token` and `app_auth` are not set.
         :param pulumi.Input[int] write_delay_ms: Amount of time in milliseconds to sleep in between writes to GitHub API. Defaults to 1000ms or 1s if not set.
         """
         ...
     @overload
     def __init__(__self__,
@@ -215,14 +239,15 @@
                  resource_name: str,
                  opts: Optional[pulumi.ResourceOptions] = None,
                  app_auth: Optional[pulumi.Input[pulumi.InputType['ProviderAppAuthArgs']]] = None,
                  base_url: Optional[pulumi.Input[str]] = None,
                  insecure: Optional[pulumi.Input[bool]] = None,
                  organization: Optional[pulumi.Input[str]] = None,
                  owner: Optional[pulumi.Input[str]] = None,
+                 parallel_requests: Optional[pulumi.Input[bool]] = None,
                  read_delay_ms: Optional[pulumi.Input[int]] = None,
                  token: Optional[pulumi.Input[str]] = None,
                  write_delay_ms: Optional[pulumi.Input[int]] = None,
                  __props__=None):
         opts = pulumi.ResourceOptions.merge(_utilities.get_resource_opts_defaults(), opts)
         if not isinstance(opts, pulumi.ResourceOptions):
             raise TypeError('Expected resource options to be a ResourceOptions instance')
@@ -237,14 +262,15 @@
             __props__.__dict__["base_url"] = base_url
             __props__.__dict__["insecure"] = pulumi.Output.from_input(insecure).apply(pulumi.runtime.to_json) if insecure is not None else None
             if organization is not None and not opts.urn:
                 warnings.warn("""Use owner (or GITHUB_OWNER) instead of organization (or GITHUB_ORGANIZATION)""", DeprecationWarning)
                 pulumi.log.warn("""organization is deprecated: Use owner (or GITHUB_OWNER) instead of organization (or GITHUB_ORGANIZATION)""")
             __props__.__dict__["organization"] = organization
             __props__.__dict__["owner"] = owner
+            __props__.__dict__["parallel_requests"] = pulumi.Output.from_input(parallel_requests).apply(pulumi.runtime.to_json) if parallel_requests is not None else None
             __props__.__dict__["read_delay_ms"] = pulumi.Output.from_input(read_delay_ms).apply(pulumi.runtime.to_json) if read_delay_ms is not None else None
             __props__.__dict__["token"] = token
             __props__.__dict__["write_delay_ms"] = pulumi.Output.from_input(write_delay_ms).apply(pulumi.runtime.to_json) if write_delay_ms is not None else None
         super(Provider, __self__).__init__(
             'github',
             resource_name,
             __props__,
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/release.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/release.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_autolink_reference.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_autolink_reference.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_collaborator.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_collaborator.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_collaborators.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_collaborators.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_deploy_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_deploy_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_environment.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_environment.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_file.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_file.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_milestone.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_milestone.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_project.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_project.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_pull_request.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_pull_request.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_tag_protection.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_tag_protection.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/repository_webhook.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/repository_webhook.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,23 +14,23 @@
 @pulumi.input_type
 class TeamArgs:
     def __init__(__self__, *,
                  create_default_maintainer: Optional[pulumi.Input[bool]] = None,
                  description: Optional[pulumi.Input[str]] = None,
                  ldap_dn: Optional[pulumi.Input[str]] = None,
                  name: Optional[pulumi.Input[str]] = None,
-                 parent_team_id: Optional[pulumi.Input[int]] = None,
+                 parent_team_id: Optional[pulumi.Input[str]] = None,
                  privacy: Optional[pulumi.Input[str]] = None):
         """
         The set of arguments for constructing a Team resource.
         :param pulumi.Input[bool] create_default_maintainer: Adds a default maintainer to the team. Defaults to `false` and adds the creating user to the team when `true`.
         :param pulumi.Input[str] description: A description of the team.
         :param pulumi.Input[str] ldap_dn: The LDAP Distinguished Name of the group where membership will be synchronized. Only available in GitHub Enterprise Server.
         :param pulumi.Input[str] name: The name of the team.
-        :param pulumi.Input[int] parent_team_id: The ID of the parent team, if this is a nested team.
+        :param pulumi.Input[str] parent_team_id: The ID or slug of the parent team, if this is a nested team.
         :param pulumi.Input[str] privacy: The level of privacy for the team. Must be one of `secret` or `closed`.
                Defaults to `secret`.
         """
         if create_default_maintainer is not None:
             pulumi.set(__self__, "create_default_maintainer", create_default_maintainer)
         if description is not None:
             pulumi.set(__self__, "description", description)
@@ -89,22 +89,22 @@
 
     @name.setter
     def name(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "name", value)
 
     @property
     @pulumi.getter(name="parentTeamId")
-    def parent_team_id(self) -> Optional[pulumi.Input[int]]:
+    def parent_team_id(self) -> Optional[pulumi.Input[str]]:
         """
-        The ID of the parent team, if this is a nested team.
+        The ID or slug of the parent team, if this is a nested team.
         """
         return pulumi.get(self, "parent_team_id")
 
     @parent_team_id.setter
-    def parent_team_id(self, value: Optional[pulumi.Input[int]]):
+    def parent_team_id(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "parent_team_id", value)
 
     @property
     @pulumi.getter
     def privacy(self) -> Optional[pulumi.Input[str]]:
         """
         The level of privacy for the team. Must be one of `secret` or `closed`.
@@ -123,25 +123,25 @@
                  create_default_maintainer: Optional[pulumi.Input[bool]] = None,
                  description: Optional[pulumi.Input[str]] = None,
                  etag: Optional[pulumi.Input[str]] = None,
                  ldap_dn: Optional[pulumi.Input[str]] = None,
                  members_count: Optional[pulumi.Input[int]] = None,
                  name: Optional[pulumi.Input[str]] = None,
                  node_id: Optional[pulumi.Input[str]] = None,
-                 parent_team_id: Optional[pulumi.Input[int]] = None,
+                 parent_team_id: Optional[pulumi.Input[str]] = None,
                  privacy: Optional[pulumi.Input[str]] = None,
                  slug: Optional[pulumi.Input[str]] = None):
         """
         Input properties used for looking up and filtering Team resources.
         :param pulumi.Input[bool] create_default_maintainer: Adds a default maintainer to the team. Defaults to `false` and adds the creating user to the team when `true`.
         :param pulumi.Input[str] description: A description of the team.
         :param pulumi.Input[str] ldap_dn: The LDAP Distinguished Name of the group where membership will be synchronized. Only available in GitHub Enterprise Server.
         :param pulumi.Input[str] name: The name of the team.
         :param pulumi.Input[str] node_id: The Node ID of the created team.
-        :param pulumi.Input[int] parent_team_id: The ID of the parent team, if this is a nested team.
+        :param pulumi.Input[str] parent_team_id: The ID or slug of the parent team, if this is a nested team.
         :param pulumi.Input[str] privacy: The level of privacy for the team. Must be one of `secret` or `closed`.
                Defaults to `secret`.
         :param pulumi.Input[str] slug: The slug of the created team, which may or may not differ from `name`,
                depending on whether `name` contains "URL-unsafe" characters.
                Useful when referencing the team in [`BranchProtection`](https://www.terraform.io/docs/providers/github/r/branch_protection.html).
         """
         if create_default_maintainer is not None:
@@ -241,22 +241,22 @@
 
     @node_id.setter
     def node_id(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "node_id", value)
 
     @property
     @pulumi.getter(name="parentTeamId")
-    def parent_team_id(self) -> Optional[pulumi.Input[int]]:
+    def parent_team_id(self) -> Optional[pulumi.Input[str]]:
         """
-        The ID of the parent team, if this is a nested team.
+        The ID or slug of the parent team, if this is a nested team.
         """
         return pulumi.get(self, "parent_team_id")
 
     @parent_team_id.setter
-    def parent_team_id(self, value: Optional[pulumi.Input[int]]):
+    def parent_team_id(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "parent_team_id", value)
 
     @property
     @pulumi.getter
     def privacy(self) -> Optional[pulumi.Input[str]]:
         """
         The level of privacy for the team. Must be one of `secret` or `closed`.
@@ -288,15 +288,15 @@
     def __init__(__self__,
                  resource_name: str,
                  opts: Optional[pulumi.ResourceOptions] = None,
                  create_default_maintainer: Optional[pulumi.Input[bool]] = None,
                  description: Optional[pulumi.Input[str]] = None,
                  ldap_dn: Optional[pulumi.Input[str]] = None,
                  name: Optional[pulumi.Input[str]] = None,
-                 parent_team_id: Optional[pulumi.Input[int]] = None,
+                 parent_team_id: Optional[pulumi.Input[str]] = None,
                  privacy: Optional[pulumi.Input[str]] = None,
                  __props__=None):
         """
         Provides a GitHub team resource.
 
         This resource allows you to add/remove teams from your organization. When applied,
         a new team will be created. When destroyed, that team will be removed.
@@ -311,27 +311,31 @@
         some_team = github.Team("someTeam",
             description="Some cool team",
             privacy="closed")
         ```
 
         ## Import
 
-        GitHub Teams can be imported using the GitHub team ID e.g.
+        GitHub Teams can be imported using the GitHub team ID or name e.g.
 
         ```sh
          $ pulumi import github:index/team:Team core 1234567
         ```
 
+        ```sh
+         $ pulumi import github:index/team:Team core Administrators
+        ```
+
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] create_default_maintainer: Adds a default maintainer to the team. Defaults to `false` and adds the creating user to the team when `true`.
         :param pulumi.Input[str] description: A description of the team.
         :param pulumi.Input[str] ldap_dn: The LDAP Distinguished Name of the group where membership will be synchronized. Only available in GitHub Enterprise Server.
         :param pulumi.Input[str] name: The name of the team.
-        :param pulumi.Input[int] parent_team_id: The ID of the parent team, if this is a nested team.
+        :param pulumi.Input[str] parent_team_id: The ID or slug of the parent team, if this is a nested team.
         :param pulumi.Input[str] privacy: The level of privacy for the team. Must be one of `secret` or `closed`.
                Defaults to `secret`.
         """
         ...
     @overload
     def __init__(__self__,
                  resource_name: str,
@@ -353,20 +357,24 @@
         some_team = github.Team("someTeam",
             description="Some cool team",
             privacy="closed")
         ```
 
         ## Import
 
-        GitHub Teams can be imported using the GitHub team ID e.g.
+        GitHub Teams can be imported using the GitHub team ID or name e.g.
 
         ```sh
          $ pulumi import github:index/team:Team core 1234567
         ```
 
+        ```sh
+         $ pulumi import github:index/team:Team core Administrators
+        ```
+
         :param str resource_name: The name of the resource.
         :param TeamArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
     def __init__(__self__, resource_name: str, *args, **kwargs):
         resource_args, opts = _utilities.get_resource_args_opts(TeamArgs, pulumi.ResourceOptions, *args, **kwargs)
@@ -378,15 +386,15 @@
     def _internal_init(__self__,
                  resource_name: str,
                  opts: Optional[pulumi.ResourceOptions] = None,
                  create_default_maintainer: Optional[pulumi.Input[bool]] = None,
                  description: Optional[pulumi.Input[str]] = None,
                  ldap_dn: Optional[pulumi.Input[str]] = None,
                  name: Optional[pulumi.Input[str]] = None,
-                 parent_team_id: Optional[pulumi.Input[int]] = None,
+                 parent_team_id: Optional[pulumi.Input[str]] = None,
                  privacy: Optional[pulumi.Input[str]] = None,
                  __props__=None):
         opts = pulumi.ResourceOptions.merge(_utilities.get_resource_opts_defaults(), opts)
         if not isinstance(opts, pulumi.ResourceOptions):
             raise TypeError('Expected resource options to be a ResourceOptions instance')
         if opts.id is None:
             if __props__ is not None:
@@ -416,30 +424,30 @@
             create_default_maintainer: Optional[pulumi.Input[bool]] = None,
             description: Optional[pulumi.Input[str]] = None,
             etag: Optional[pulumi.Input[str]] = None,
             ldap_dn: Optional[pulumi.Input[str]] = None,
             members_count: Optional[pulumi.Input[int]] = None,
             name: Optional[pulumi.Input[str]] = None,
             node_id: Optional[pulumi.Input[str]] = None,
-            parent_team_id: Optional[pulumi.Input[int]] = None,
+            parent_team_id: Optional[pulumi.Input[str]] = None,
             privacy: Optional[pulumi.Input[str]] = None,
             slug: Optional[pulumi.Input[str]] = None) -> 'Team':
         """
         Get an existing Team resource's state with the given name, id, and optional extra
         properties used to qualify the lookup.
 
         :param str resource_name: The unique name of the resulting resource.
         :param pulumi.Input[str] id: The unique provider ID of the resource to lookup.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] create_default_maintainer: Adds a default maintainer to the team. Defaults to `false` and adds the creating user to the team when `true`.
         :param pulumi.Input[str] description: A description of the team.
         :param pulumi.Input[str] ldap_dn: The LDAP Distinguished Name of the group where membership will be synchronized. Only available in GitHub Enterprise Server.
         :param pulumi.Input[str] name: The name of the team.
         :param pulumi.Input[str] node_id: The Node ID of the created team.
-        :param pulumi.Input[int] parent_team_id: The ID of the parent team, if this is a nested team.
+        :param pulumi.Input[str] parent_team_id: The ID or slug of the parent team, if this is a nested team.
         :param pulumi.Input[str] privacy: The level of privacy for the team. Must be one of `secret` or `closed`.
                Defaults to `secret`.
         :param pulumi.Input[str] slug: The slug of the created team, which may or may not differ from `name`,
                depending on whether `name` contains "URL-unsafe" characters.
                Useful when referencing the team in [`BranchProtection`](https://www.terraform.io/docs/providers/github/r/branch_protection.html).
         """
         opts = pulumi.ResourceOptions.merge(opts, pulumi.ResourceOptions(id=id))
@@ -506,17 +514,17 @@
         """
         The Node ID of the created team.
         """
         return pulumi.get(self, "node_id")
 
     @property
     @pulumi.getter(name="parentTeamId")
-    def parent_team_id(self) -> pulumi.Output[Optional[int]]:
+    def parent_team_id(self) -> pulumi.Output[Optional[str]]:
         """
-        The ID of the parent team, if this is a nested team.
+        The ID or slug of the parent team, if this is a nested team.
         """
         return pulumi.get(self, "parent_team_id")
 
     @property
     @pulumi.getter
     def privacy(self) -> pulumi.Output[Optional[str]]:
         """
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team_members.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team_members.py`

 * *Files 2% similar despite different names*

```diff
@@ -138,20 +138,24 @@
                     role="member",
                 ),
             ])
         ```
 
         ## Import
 
-        GitHub Team Membership can be imported using the team ID `teamid`, e.g.
+        GitHub Team Membership can be imported using the team ID `teamid` or team name, e.g.
 
         ```sh
          $ pulumi import github:index/teamMembers:TeamMembers some_team 1234567
         ```
 
+        ```sh
+         $ pulumi import github:index/teamMembers:TeamMembers some_team Administrators
+        ```
+
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['TeamMembersMemberArgs']]]] members: List of team members. See Members below for details.
         :param pulumi.Input[str] team_id: The GitHub team id or the GitHub team slug
         """
         ...
     @overload
@@ -186,20 +190,24 @@
                     role="member",
                 ),
             ])
         ```
 
         ## Import
 
-        GitHub Team Membership can be imported using the team ID `teamid`, e.g.
+        GitHub Team Membership can be imported using the team ID `teamid` or team name, e.g.
 
         ```sh
          $ pulumi import github:index/teamMembers:TeamMembers some_team 1234567
         ```
 
+        ```sh
+         $ pulumi import github:index/teamMembers:TeamMembers some_team Administrators
+        ```
+
         :param str resource_name: The name of the resource.
         :param TeamMembersArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
     def __init__(__self__, resource_name: str, *args, **kwargs):
         resource_args, opts = _utilities.get_resource_args_opts(TeamMembersArgs, pulumi.ResourceOptions, *args, **kwargs)
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team_membership.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team_membership.py`

 * *Files 4% similar despite different names*

```diff
@@ -162,20 +162,24 @@
             team_id=some_team.id,
             username="SomeUser",
             role="member")
         ```
 
         ## Import
 
-        GitHub Team Membership can be imported using an ID made up of `teamid:username`, e.g.
+        GitHub Team Membership can be imported using an ID made up of `teamid:username` or `teamname:username`, e.g.
 
         ```sh
          $ pulumi import github:index/teamMembership:TeamMembership member 1234567:someuser
         ```
 
+        ```sh
+         $ pulumi import github:index/teamMembership:TeamMembership member Administrators:someuser
+        ```
+
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] role: The role of the user within the team.
                Must be one of `member` or `maintainer`. Defaults to `member`.
         :param pulumi.Input[str] team_id: The GitHub team id or the GitHub team slug
         :param pulumi.Input[str] username: The user to add to the team.
         """
@@ -201,20 +205,24 @@
             team_id=some_team.id,
             username="SomeUser",
             role="member")
         ```
 
         ## Import
 
-        GitHub Team Membership can be imported using an ID made up of `teamid:username`, e.g.
+        GitHub Team Membership can be imported using an ID made up of `teamid:username` or `teamname:username`, e.g.
 
         ```sh
          $ pulumi import github:index/teamMembership:TeamMembership member 1234567:someuser
         ```
 
+        ```sh
+         $ pulumi import github:index/teamMembership:TeamMembership member Administrators:someuser
+        ```
+
         :param str resource_name: The name of the resource.
         :param TeamMembershipArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
     def __init__(__self__, resource_name: str, *args, **kwargs):
         resource_args, opts = _utilities.get_resource_args_opts(TeamMembershipArgs, pulumi.ResourceOptions, *args, **kwargs)
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team_repository.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team_repository.py`

 * *Files 2% similar despite different names*

```diff
@@ -176,20 +176,24 @@
             team_id=some_team.id,
             repository=some_repo.name,
             permission="pull")
         ```
 
         ## Import
 
-        GitHub Team Repository can be imported using an ID made up of `team_id:repository`, e.g.
+        GitHub Team Repository can be imported using an ID made up of `team_id:repository` or `team_name:repository`, e.g.
 
         ```sh
          $ pulumi import github:index/teamRepository:TeamRepository terraform_repo 1234567:terraform
         ```
 
+        ```sh
+         $ pulumi import github:index/teamRepository:TeamRepository terraform_repo Administrators:terraform
+        ```
+
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] permission: The permissions of team members regarding the repository.
                Must be one of `pull`, `triage`, `push`, `maintain`, `admin` or the name of an existing [custom repository role](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-peoples-access-to-your-organization-with-roles/managing-custom-repository-roles-for-an-organization) within the organisation. Defaults to `pull`.
         :param pulumi.Input[str] repository: The repository to add to the team.
         :param pulumi.Input[str] team_id: The GitHub team id or the GitHub team slug
         """
@@ -229,20 +233,24 @@
             team_id=some_team.id,
             repository=some_repo.name,
             permission="pull")
         ```
 
         ## Import
 
-        GitHub Team Repository can be imported using an ID made up of `team_id:repository`, e.g.
+        GitHub Team Repository can be imported using an ID made up of `team_id:repository` or `team_name:repository`, e.g.
 
         ```sh
          $ pulumi import github:index/teamRepository:TeamRepository terraform_repo 1234567:terraform
         ```
 
+        ```sh
+         $ pulumi import github:index/teamRepository:TeamRepository terraform_repo Administrators:terraform
+        ```
+
         :param str resource_name: The name of the resource.
         :param TeamRepositoryArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
     def __init__(__self__, resource_name: str, *args, **kwargs):
         resource_args, opts = _utilities.get_resource_args_opts(TeamRepositoryArgs, pulumi.ResourceOptions, *args, **kwargs)
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team_settings.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team_settings.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/team_sync_group_mapping.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/team_sync_group_mapping.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/user_gpg_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/user_gpg_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/user_invitation_accepter.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/user_invitation_accepter.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github/user_ssh_key.py` & `pulumi_github-5.9.0a1683752304/pulumi_github/user_ssh_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/PKG-INFO` & `pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi-github
-Version: 5.9.0a1683610445
+Version: 5.9.0a1683752304
 Summary: A Pulumi package for creating and managing github cloud resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-github
 Keywords: pulumi github
 Platform: UNKNOWN
 Requires-Python: >=3.7
```

### Comparing `pulumi_github-5.9.0a1683610445/pulumi_github.egg-info/SOURCES.txt` & `pulumi_github-5.9.0a1683752304/pulumi_github.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -36,14 +36,15 @@
 pulumi_github/get_actions_organization_variables.py
 pulumi_github/get_actions_public_key.py
 pulumi_github/get_actions_registration_token.py
 pulumi_github/get_actions_repository_oidc_subject_claim_customization_template.py
 pulumi_github/get_actions_secrets.py
 pulumi_github/get_actions_variables.py
 pulumi_github/get_branch.py
+pulumi_github/get_branch_protection_rules.py
 pulumi_github/get_collaborators.py
 pulumi_github/get_dependabot_organization_public_key.py
 pulumi_github/get_dependabot_organization_secrets.py
 pulumi_github/get_dependabot_public_key.py
 pulumi_github/get_dependabot_secrets.py
 pulumi_github/get_enterprise.py
 pulumi_github/get_external_groups.py
```

