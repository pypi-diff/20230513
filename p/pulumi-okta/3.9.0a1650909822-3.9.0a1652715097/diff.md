# Comparing `tmp/pulumi_okta-3.9.0a1650909822.tar.gz` & `tmp/pulumi_okta-3.9.0a1652715097.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/pulumi_okta-3.9.0a1650909822.tar", last modified: Thu May  5 20:03:40 2022, max compression
+gzip compressed data, was "dist/pulumi_okta-3.9.0a1652715097.tar", last modified: Mon May 16 15:35:00 2022, max compression
```

## Comparing `pulumi_okta-3.9.0a1650909822.tar` & `pulumi_okta-3.9.0a1652715097.tar`

### file list

```diff
@@ -1,207 +1,218 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/
--rw-r--r--   0 runner    (1001) docker     (121)     3760 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2916 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/
--rw-r--r--   0 runner    (1001) docker     (121)    22454 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    22685 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)     7667 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (121)    15141 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/admin_role_custom.py
--rw-r--r--   0 runner    (1001) docker     (121)    11780 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/admin_role_custom_assignments.py
--rw-r--r--   0 runner    (1001) docker     (121)    14786 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/admin_role_targets.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/
--rw-r--r--   0 runner    (1001) docker     (121)      813 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    24325 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    78431 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/auto_login.py
--rw-r--r--   0 runner    (1001) docker     (121)    50928 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/basic_auth.py
--rw-r--r--   0 runner    (1001) docker     (121)    51053 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/bookmark.py
--rw-r--r--   0 runner    (1001) docker     (121)    10126 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_app.py
--rw-r--r--   0 runner    (1001) docker     (121)     7067 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_metadata_saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    18419 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_oauth.py
--rw-r--r--   0 runner    (1001) docker     (121)    31215 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    14684 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/group_assignment.py
--rw-r--r--   0 runner    (1001) docker     (121)   136888 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth.py
--rw-r--r--   0 runner    (1001) docker     (121)     9360 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth_post_logout_redirect_uri.py
--rw-r--r--   0 runner    (1001) docker     (121)     8778 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth_redirect_uri.py
--rw-r--r--   0 runner    (1001) docker     (121)    20066 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)   143102 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    87663 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/secure_password_store.py
--rw-r--r--   0 runner    (1001) docker     (121)    73882 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/swa.py
--rw-r--r--   0 runner    (1001) docker     (121)    81676 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/three_field.py
--rw-r--r--   0 runner    (1001) docker     (121)    17853 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user.py
--rw-r--r--   0 runner    (1001) docker     (121)    23187 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user_base_schema.py
--rw-r--r--   0 runner    (1001) docker     (121)    49339 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user_schema.py
--rw-r--r--   0 runner    (1001) docker     (121)    11289 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_group_assignments.py
--rw-r--r--   0 runner    (1001) docker     (121)    10999 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_oauth_api_scope.py
--rw-r--r--   0 runner    (1001) docker     (121)    10082 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_saml_app_settings.py
--rw-r--r--   0 runner    (1001) docker     (121)    80981 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_shared_credentials.py
--rw-r--r--   0 runner    (1001) docker     (121)    78383 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_signon_policy_rule.py
--rw-r--r--   0 runner    (1001) docker     (121)    23454 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_user_base_schema_property.py
--rw-r--r--   0 runner    (1001) docker     (121)    50464 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/app_user_schema_property.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/
--rw-r--r--   0 runner    (1001) docker     (121)      559 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     7565 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server.py
--rw-r--r--   0 runner    (1001) docker     (121)     5347 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)     3652 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server_scopes.py
--rw-r--r--   0 runner    (1001) docker     (121)     3167 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    23462 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server.py
--rw-r--r--   0 runner    (1001) docker     (121)    24601 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_claim.py
--rw-r--r--   0 runner    (1001) docker     (121)    20413 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)    46586 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy_claim.py
--rw-r--r--   0 runner    (1001) docker     (121)    46333 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy_rule.py
--rw-r--r--   0 runner    (1001) docker     (121)    19785 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_scope.py
--rw-r--r--   0 runner    (1001) docker     (121)    19971 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth_server_claim_default.py
--rw-r--r--   0 runner    (1001) docker     (121)    23137 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/auth_server_default.py
--rw-r--r--   0 runner    (1001) docker     (121)    30385 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/authenticator.py
--rw-r--r--   0 runner    (1001) docker     (121)    24059 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/behaviour.py
--rw-r--r--   0 runner    (1001) docker     (121)    12672 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/captcha.py
--rw-r--r--   0 runner    (1001) docker     (121)    11209 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/captcha_org_wide_settings.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/config/
--rw-r--r--   0 runner    (1001) docker     (121)      285 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     3629 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/config/vars.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/
--rw-r--r--   0 runner    (1001) docker     (121)      882 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    22615 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    68555 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/auth_login_app.py
--rw-r--r--   0 runner    (1001) docker     (121)    45893 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/bookmark_app.py
--rw-r--r--   0 runner    (1001) docker     (121)     3062 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/get_default_policies.py
--rw-r--r--   0 runner    (1001) docker     (121)    61856 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/idp.py
--rw-r--r--   0 runner    (1001) docker     (121)    50409 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/mfa_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)    32071 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/mfa_policy_rule.py
--rw-r--r--   0 runner    (1001) docker     (121)   121587 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/oauth_app.py
--rw-r--r--   0 runner    (1001) docker     (121)     7475 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/oauth_app_redirect_uri.py
--rw-r--r--   0 runner    (1001) docker     (121)    17387 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    77607 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/password_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)    31492 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/password_policy_rule.py
--rw-r--r--   0 runner    (1001) docker     (121)   124749 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_app.py
--rw-r--r--   0 runner    (1001) docker     (121)    58334 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_idp.py
--rw-r--r--   0 runner    (1001) docker     (121)    10556 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_idp_signing_key.py
--rw-r--r--   0 runner    (1001) docker     (121)    79343 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/secure_password_store_app.py
--rw-r--r--   0 runner    (1001) docker     (121)    14495 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/signon_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)    57068 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/signon_policy_rule.py
--rw-r--r--   0 runner    (1001) docker     (121)    63490 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/social_idp.py
--rw-r--r--   0 runner    (1001) docker     (121)    67025 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/swa_app.py
--rw-r--r--   0 runner    (1001) docker     (121)    74706 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/three_field_app.py
--rw-r--r--   0 runner    (1001) docker     (121)    15340 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/domain.py
--rw-r--r--   0 runner    (1001) docker     (121)    22145 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/domain_certificate.py
--rw-r--r--   0 runner    (1001) docker     (121)     6822 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/domain_verification.py
--rw-r--r--   0 runner    (1001) docker     (121)    12784 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/email_sender.py
--rw-r--r--   0 runner    (1001) docker     (121)     6904 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/email_sender_verification.py
--rw-r--r--   0 runner    (1001) docker     (121)    18007 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/event_hook.py
--rw-r--r--   0 runner    (1001) docker     (121)     7935 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/event_hook_verification.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/factor/
--rw-r--r--   0 runner    (1001) docker     (121)      291 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/factor/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     9833 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/factor/factor.py
--rw-r--r--   0 runner    (1001) docker     (121)    19482 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/factor_totp.py
--rw-r--r--   0 runner    (1001) docker     (121)     3283 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_group_assignments.py
--rw-r--r--   0 runner    (1001) docker     (121)     3577 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_signon_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)     3245 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_user_assignments.py
--rw-r--r--   0 runner    (1001) docker     (121)     7133 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_auth_server_claim.py
--rw-r--r--   0 runner    (1001) docker     (121)     3743 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_auth_server_claims.py
--rw-r--r--   0 runner    (1001) docker     (121)     8133 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_authenticator.py
--rw-r--r--   0 runner    (1001) docker     (121)     4496 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_behaviour.py
--rw-r--r--   0 runner    (1001) docker     (121)     3281 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_behaviours.py
--rw-r--r--   0 runner    (1001) docker     (121)     5355 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_groups.py
--rw-r--r--   0 runner    (1001) docker     (121)     6541 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_network_zone.py
--rw-r--r--   0 runner    (1001) docker     (121)     5436 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_role_subscription.py
--rw-r--r--   0 runner    (1001) docker     (121)     3851 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_trusted_origins.py
--rw-r--r--   0 runner    (1001) docker     (121)     4157 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/get_user_security_questions.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/
--rw-r--r--   0 runner    (1001) docker     (121)      436 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     3807 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/get_everyone_group.py
--rw-r--r--   0 runner    (1001) docker     (121)     5640 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/get_group.py
--rw-r--r--   0 runner    (1001) docker     (121)    18577 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/group.py
--rw-r--r--   0 runner    (1001) docker     (121)     7647 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/membership.py
--rw-r--r--   0 runner    (1001) docker     (121)    22094 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/role.py
--rw-r--r--   0 runner    (1001) docker     (121)    10660 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/roles.py
--rw-r--r--   0 runner    (1001) docker     (121)    20797 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group/rule.py
--rw-r--r--   0 runner    (1001) docker     (121)     9939 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group_memberships.py
--rw-r--r--   0 runner    (1001) docker     (121)    47527 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/group_schema_property.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/
--rw-r--r--   0 runner    (1001) docker     (121)      462 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     7649 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_metadata_saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    11480 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_oidc.py
--rw-r--r--   0 runner    (1001) docker     (121)     9008 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    17437 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_social.py
--rw-r--r--   0 runner    (1001) docker     (121)    88769 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/oidc.py
--rw-r--r--   0 runner    (1001) docker     (121)    84468 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/saml.py
--rw-r--r--   0 runner    (1001) docker     (121)    11841 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/saml_key.py
--rw-r--r--   0 runner    (1001) docker     (121)    89175 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/social.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/
--rw-r--r--   0 runner    (1001) docker     (121)      334 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1578 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    18725 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/hook.py
--rw-r--r--   0 runner    (1001) docker     (121)     1265 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    18828 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/link_definition.py
--rw-r--r--   0 runner    (1001) docker     (121)    14692 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/link_value.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/network/
--rw-r--r--   0 runner    (1001) docker     (121)      289 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/network/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    24362 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/network/zone.py
--rw-r--r--   0 runner    (1001) docker     (121)    35438 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/org_configuration.py
--rw-r--r--   0 runner    (1001) docker     (121)     8703 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/org_support.py
--rw-r--r--   0 runner    (1001) docker     (121)    26892 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/outputs.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/
--rw-r--r--   0 runner    (1001) docker     (121)      553 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    15404 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)     3682 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/get_default_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)     4300 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/get_policy.py
--rw-r--r--   0 runner    (1001) docker     (121)    68145 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/mfa.py
--rw-r--r--   0 runner    (1001) docker     (121)    14476 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    76206 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/password.py
--rw-r--r--   0 runner    (1001) docker     (121)    50598 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_idp_discovery.py
--rw-r--r--   0 runner    (1001) docker     (121)    42192 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_mfa.py
--rw-r--r--   0 runner    (1001) docker     (121)    32461 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_password.py
--rw-r--r--   0 runner    (1001) docker     (121)    68608 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_signon.py
--rw-r--r--   0 runner    (1001) docker     (121)    13726 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/signon.py
--rw-r--r--   0 runner    (1001) docker     (121)    64334 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_mfa_default.py
--rw-r--r--   0 runner    (1001) docker     (121)    71452 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_password_default.py
--rw-r--r--   0 runner    (1001) docker     (121)     8222 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_profile_enrollment.py
--rw-r--r--   0 runner    (1001) docker     (121)    11807 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_profile_enrollment_apps.py
--rw-r--r--   0 runner    (1001) docker     (121)    26953 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_rule_profile_enrollment.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/
--rw-r--r--   0 runner    (1001) docker     (121)      337 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     2154 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    21547 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/mapping.py
--rw-r--r--   0 runner    (1001) docker     (121)     2234 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    20247 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/provider.py
--rw-r--r--   0 runner    (1001) docker     (121)       41 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/pulumi-plugin.json
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/py.typed
--rw-r--r--   0 runner    (1001) docker     (121)    13521 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/rate_limiting.py
--rw-r--r--   0 runner    (1001) docker     (121)    11782 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/resource_set.py
--rw-r--r--   0 runner    (1001) docker     (121)    12625 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/role_subscription.py
--rw-r--r--   0 runner    (1001) docker     (121)    21459 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/security_notification_emails.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template/
--rw-r--r--   0 runner    (1001) docker     (121)      335 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1858 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    12079 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template/email.py
--rw-r--r--   0 runner    (1001) docker     (121)     1386 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    11557 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/template_sms.py
--rw-r--r--   0 runner    (1001) docker     (121)    14278 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/threat_insight_settings.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/trustedorigin/
--rw-r--r--   0 runner    (1001) docker     (121)      291 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/trustedorigin/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    12543 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/trustedorigin/origin.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/
--rw-r--r--   0 runner    (1001) docker     (121)      533 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    10707 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/_inputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    21467 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/base_schema.py
--rw-r--r--   0 runner    (1001) docker     (121)    22470 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user.py
--rw-r--r--   0 runner    (1001) docker     (121)     2890 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user_profile_mapping_source.py
--rw-r--r--   0 runner    (1001) docker     (121)     3806 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user_type.py
--rw-r--r--   0 runner    (1001) docker     (121)     3858 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_users.py
--rw-r--r--   0 runner    (1001) docker     (121)    21017 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/outputs.py
--rw-r--r--   0 runner    (1001) docker     (121)    50926 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/schema.py
--rw-r--r--   0 runner    (1001) docker     (121)    96316 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/user.py
--rw-r--r--   0 runner    (1001) docker     (121)     9948 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user/user_type.py
--rw-r--r--   0 runner    (1001) docker     (121)    13484 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user_admin_roles.py
--rw-r--r--   0 runner    (1001) docker     (121)    22928 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user_base_schema_property.py
--rw-r--r--   0 runner    (1001) docker     (121)    13931 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user_factor_question.py
--rw-r--r--   0 runner    (1001) docker     (121)     9023 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user_group_memberships.py
--rw-r--r--   0 runner    (1001) docker     (121)    51953 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta/user_schema_property.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3760 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     6215 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (121)       49 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-05-05 20:03:40.000000 pulumi_okta-3.9.0a1650909822/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     2100 2022-05-05 20:03:39.000000 pulumi_okta-3.9.0a1650909822/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/
+-rw-r--r--   0 runner    (1001) docker     (121)     3760 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2916 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/
+-rw-r--r--   0 runner    (1001) docker     (121)    23205 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22685 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7667 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (121)    19952 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/admin_role_custom.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11812 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/admin_role_custom_assignments.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14818 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/admin_role_targets.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/
+-rw-r--r--   0 runner    (1001) docker     (121)      813 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    24381 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    78495 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/auto_login.py
+-rw-r--r--   0 runner    (1001) docker     (121)    50992 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/basic_auth.py
+-rw-r--r--   0 runner    (1001) docker     (121)    51117 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/bookmark.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10126 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7067 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_metadata_saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18419 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_oauth.py
+-rw-r--r--   0 runner    (1001) docker     (121)    31215 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14716 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/group_assignment.py
+-rw-r--r--   0 runner    (1001) docker     (121)   137148 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9392 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth_post_logout_redirect_uri.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8810 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth_redirect_uri.py
+-rw-r--r--   0 runner    (1001) docker     (121)    20122 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)   146225 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    87727 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/secure_password_store.py
+-rw-r--r--   0 runner    (1001) docker     (121)    73946 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/swa.py
+-rw-r--r--   0 runner    (1001) docker     (121)    81740 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/three_field.py
+-rw-r--r--   0 runner    (1001) docker     (121)    17885 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23219 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user_base_schema.py
+-rw-r--r--   0 runner    (1001) docker     (121)    49371 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user_schema.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11305 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_group_assignments.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11015 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_oauth_api_scope.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10098 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_saml_app_settings.py
+-rw-r--r--   0 runner    (1001) docker     (121)    81045 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_shared_credentials.py
+-rw-r--r--   0 runner    (1001) docker     (121)    78415 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_signon_policy_rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23486 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_user_base_schema_property.py
+-rw-r--r--   0 runner    (1001) docker     (121)    50496 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/app_user_schema_property.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/
+-rw-r--r--   0 runner    (1001) docker     (121)      559 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7565 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5347 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3652 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server_scopes.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3167 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23478 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server.py
+-rw-r--r--   0 runner    (1001) docker     (121)    24633 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_claim.py
+-rw-r--r--   0 runner    (1001) docker     (121)    20445 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)    46634 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy_claim.py
+-rw-r--r--   0 runner    (1001) docker     (121)    46381 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy_rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)    19817 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_scope.py
+-rw-r--r--   0 runner    (1001) docker     (121)    20035 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth_server_claim_default.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23153 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/auth_server_default.py
+-rw-r--r--   0 runner    (1001) docker     (121)    30205 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/authenticator.py
+-rw-r--r--   0 runner    (1001) docker     (121)    24075 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/behaviour.py
+-rw-r--r--   0 runner    (1001) docker     (121)    16723 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/brand.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12688 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/captcha.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11209 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/captcha_org_wide_settings.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/config/
+-rw-r--r--   0 runner    (1001) docker     (121)      285 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3629 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/config/vars.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/
+-rw-r--r--   0 runner    (1001) docker     (121)      882 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22615 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    68555 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/auth_login_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)    45893 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/bookmark_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3062 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/get_default_policies.py
+-rw-r--r--   0 runner    (1001) docker     (121)    61856 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/idp.py
+-rw-r--r--   0 runner    (1001) docker     (121)    50409 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/mfa_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)    32071 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/mfa_policy_rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)   121587 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/oauth_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7475 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/oauth_app_redirect_uri.py
+-rw-r--r--   0 runner    (1001) docker     (121)    17387 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    77607 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/password_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)    31492 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/password_policy_rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)   124749 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)    58334 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_idp.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10556 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_idp_signing_key.py
+-rw-r--r--   0 runner    (1001) docker     (121)    79343 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/secure_password_store_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14495 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/signon_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)    57068 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/signon_policy_rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)    63490 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/social_idp.py
+-rw-r--r--   0 runner    (1001) docker     (121)    67025 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/swa_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)    74706 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/three_field_app.py
+-rw-r--r--   0 runner    (1001) docker     (121)    15356 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/domain.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22145 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/domain_certificate.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6822 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/domain_verification.py
+-rw-r--r--   0 runner    (1001) docker     (121)    17183 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/email_customization.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12800 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/email_sender.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6904 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/email_sender_verification.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18023 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/event_hook.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7935 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/event_hook_verification.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/factor/
+-rw-r--r--   0 runner    (1001) docker     (121)      291 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/factor/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9833 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/factor/factor.py
+-rw-r--r--   0 runner    (1001) docker     (121)    19482 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/factor_totp.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3283 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_group_assignments.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3577 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_signon_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3245 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_user_assignments.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7133 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_auth_server_claim.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3743 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_auth_server_claims.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8133 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_authenticator.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4496 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_behaviour.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3281 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_behaviours.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4394 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_brand.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2256 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_brands.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6763 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_email_customization.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4581 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_email_customizations.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5355 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_groups.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6541 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_network_zone.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5436 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_role_subscription.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3764 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_template.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3402 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_templates.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11160 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_theme.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3186 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_themes.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3851 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_trusted_origins.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4157 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/get_user_security_questions.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/
+-rw-r--r--   0 runner    (1001) docker     (121)      436 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3807 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/get_everyone_group.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5640 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/get_group.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18609 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/group.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7647 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/membership.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22126 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/role.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10676 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/roles.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21072 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group/rule.py
+-rw-r--r--   0 runner    (1001) docker     (121)    10371 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group_memberships.py
+-rw-r--r--   0 runner    (1001) docker     (121)    47543 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/group_schema_property.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/
+-rw-r--r--   0 runner    (1001) docker     (121)      462 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7649 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_metadata_saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11480 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_oidc.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9008 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    17437 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_social.py
+-rw-r--r--   0 runner    (1001) docker     (121)    88785 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/oidc.py
+-rw-r--r--   0 runner    (1001) docker     (121)    84484 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/saml.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11857 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/saml_key.py
+-rw-r--r--   0 runner    (1001) docker     (121)    89191 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/social.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/
+-rw-r--r--   0 runner    (1001) docker     (121)      334 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1578 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18741 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/hook.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1265 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    18844 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/link_definition.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14724 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/link_value.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/network/
+-rw-r--r--   0 runner    (1001) docker     (121)      289 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/network/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    24378 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/network/zone.py
+-rw-r--r--   0 runner    (1001) docker     (121)    35438 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/org_configuration.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8703 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/org_support.py
+-rw-r--r--   0 runner    (1001) docker     (121)    34071 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/outputs.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/
+-rw-r--r--   0 runner    (1001) docker     (121)      553 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    15404 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3682 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/get_default_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4300 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/get_policy.py
+-rw-r--r--   0 runner    (1001) docker     (121)    68161 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/mfa.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14476 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    76222 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/password.py
+-rw-r--r--   0 runner    (1001) docker     (121)    50630 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_idp_discovery.py
+-rw-r--r--   0 runner    (1001) docker     (121)    42224 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_mfa.py
+-rw-r--r--   0 runner    (1001) docker     (121)    32493 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_password.py
+-rw-r--r--   0 runner    (1001) docker     (121)    68640 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_signon.py
+-rw-r--r--   0 runner    (1001) docker     (121)    13742 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/signon.py
+-rw-r--r--   0 runner    (1001) docker     (121)    64334 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_mfa_default.py
+-rw-r--r--   0 runner    (1001) docker     (121)    71452 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_password_default.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8238 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_profile_enrollment.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11823 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_profile_enrollment_apps.py
+-rw-r--r--   0 runner    (1001) docker     (121)    26985 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_rule_profile_enrollment.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/
+-rw-r--r--   0 runner    (1001) docker     (121)      337 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2154 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21547 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/mapping.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2234 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    20247 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/provider.py
+-rw-r--r--   0 runner    (1001) docker     (121)       41 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/pulumi-plugin.json
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/py.typed
+-rw-r--r--   0 runner    (1001) docker     (121)    13521 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/rate_limiting.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11798 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/resource_set.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12678 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/role_subscription.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21459 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/security_notification_emails.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template/
+-rw-r--r--   0 runner    (1001) docker     (121)      335 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1858 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12273 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template/email.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1386 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11573 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/template_sms.py
+-rw-r--r--   0 runner    (1001) docker     (121)    43378 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/theme.py
+-rw-r--r--   0 runner    (1001) docker     (121)    14278 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/threat_insight_settings.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/trustedorigin/
+-rw-r--r--   0 runner    (1001) docker     (121)      291 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/trustedorigin/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12559 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/trustedorigin/origin.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/
+-rw-r--r--   0 runner    (1001) docker     (121)      533 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    12791 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    21515 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/base_schema.py
+-rw-r--r--   0 runner    (1001) docker     (121)    23325 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2890 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user_profile_mapping_source.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3806 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user_type.py
+-rw-r--r--   0 runner    (1001) docker     (121)     7388 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_users.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22825 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/outputs.py
+-rw-r--r--   0 runner    (1001) docker     (121)    50974 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/schema.py
+-rw-r--r--   0 runner    (1001) docker     (121)    96794 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/user.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9964 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user/user_type.py
+-rw-r--r--   0 runner    (1001) docker     (121)    13500 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user_admin_roles.py
+-rw-r--r--   0 runner    (1001) docker     (121)    22976 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user_base_schema_property.py
+-rw-r--r--   0 runner    (1001) docker     (121)    13963 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user_factor_question.py
+-rw-r--r--   0 runner    (1001) docker     (121)     9023 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user_group_memberships.py
+-rw-r--r--   0 runner    (1001) docker     (121)    52001 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta/user_schema_property.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     3760 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     6530 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (121)       49 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       12 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-05-16 15:35:00.000000 pulumi_okta-3.9.0a1652715097/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     2100 2022-05-16 15:34:59.000000 pulumi_okta-3.9.0a1652715097/setup.py
```

### Comparing `pulumi_okta-3.9.0a1650909822/PKG-INFO` & `pulumi_okta-3.9.0a1652715097/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi_okta
-Version: 3.9.0a1650909822
+Version: 3.9.0a1652715097
 Summary: A Pulumi package for creating and managing okta resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-okta
 Description: r[![Actions Status](https://github.com/pulumi/pulumi-okta/workflows/master/badge.svg)](https://github.com/pulumi/pulumi-okta/actions)
         [![Slack](http://www.pulumi.com/images/docs/badges/slack.svg)](https://slack.pulumi.com)
         [![NPM version](https://badge.fury.io/js/%40pulumi%2Fokta.svg)](https://www.npmjs.com/package/@pulumi/okta)
```

### Comparing `pulumi_okta-3.9.0a1650909822/README.md` & `pulumi_okta-3.9.0a1652715097/README.md`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,35 +15,45 @@
 from .app_signon_policy_rule import *
 from .app_user_base_schema_property import *
 from .app_user_schema_property import *
 from .auth_server_claim_default import *
 from .auth_server_default import *
 from .authenticator import *
 from .behaviour import *
+from .brand import *
 from .captcha import *
 from .captcha_org_wide_settings import *
 from .domain import *
 from .domain_certificate import *
 from .domain_verification import *
+from .email_customization import *
 from .email_sender import *
 from .email_sender_verification import *
 from .event_hook import *
 from .event_hook_verification import *
 from .factor_totp import *
 from .get_app_group_assignments import *
 from .get_app_signon_policy import *
 from .get_app_user_assignments import *
 from .get_auth_server_claim import *
 from .get_auth_server_claims import *
 from .get_authenticator import *
 from .get_behaviour import *
 from .get_behaviours import *
+from .get_brand import *
+from .get_brands import *
+from .get_email_customization import *
+from .get_email_customizations import *
 from .get_groups import *
 from .get_network_zone import *
 from .get_role_subscription import *
+from .get_template import *
+from .get_templates import *
+from .get_theme import *
+from .get_themes import *
 from .get_trusted_origins import *
 from .get_user_security_questions import *
 from .group_memberships import *
 from .group_schema_property import *
 from .link_definition import *
 from .link_value import *
 from .org_configuration import *
@@ -55,14 +65,15 @@
 from .policy_rule_profile_enrollment import *
 from .provider import *
 from .rate_limiting import *
 from .resource_set import *
 from .role_subscription import *
 from .security_notification_emails import *
 from .template_sms import *
+from .theme import *
 from .threat_insight_settings import *
 from .user_admin_roles import *
 from .user_base_schema_property import *
 from .user_factor_question import *
 from .user_group_memberships import *
 from .user_schema_property import *
 from ._inputs import *
@@ -611,14 +622,22 @@
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/behaviour:Behaviour": "Behaviour"
   }
  },
  {
   "pkg": "okta",
+  "mod": "index/brand",
+  "fqn": "pulumi_okta",
+  "classes": {
+   "okta:index/brand:Brand": "Brand"
+  }
+ },
+ {
+  "pkg": "okta",
   "mod": "index/captcha",
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/captcha:Captcha": "Captcha"
   }
  },
  {
@@ -651,14 +670,22 @@
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/domainVerification:DomainVerification": "DomainVerification"
   }
  },
  {
   "pkg": "okta",
+  "mod": "index/emailCustomization",
+  "fqn": "pulumi_okta",
+  "classes": {
+   "okta:index/emailCustomization:EmailCustomization": "EmailCustomization"
+  }
+ },
+ {
+  "pkg": "okta",
   "mod": "index/emailSender",
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/emailSender:EmailSender": "EmailSender"
   }
  },
  {
@@ -819,14 +846,22 @@
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/templateSms:TemplateSms": "TemplateSms"
   }
  },
  {
   "pkg": "okta",
+  "mod": "index/theme",
+  "fqn": "pulumi_okta",
+  "classes": {
+   "okta:index/theme:Theme": "Theme"
+  }
+ },
+ {
+  "pkg": "okta",
   "mod": "index/threatInsightSettings",
   "fqn": "pulumi_okta",
   "classes": {
    "okta:index/threatInsightSettings:ThreatInsightSettings": "ThreatInsightSettings"
   }
  },
  {
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/_utilities.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/_utilities.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/admin_role_custom_assignments.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/admin_role_custom_assignments.py`

 * *Files 1% similar despite different names*

```diff
@@ -141,15 +141,15 @@
         > **NOTE:** This an `Early Access` feature.
 
         ## Import
 
         Okta Custom Admin Role Assignments can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/adminRoleCustomAssignments:AdminRoleCustomAssignments example <resource_set_id>/<custom_role_id>
+         $ pulumi import okta:index/adminRoleCustomAssignments:AdminRoleCustomAssignments example &#60;resource_set_id&#62;/&#60;custom_role_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] custom_role_id: ID of the Custom Role.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] members: The hrefs that point to User(s) and/or Group(s) that receive the Role. At least one
                permission must be specified when creating custom role.
@@ -169,15 +169,15 @@
         > **NOTE:** This an `Early Access` feature.
 
         ## Import
 
         Okta Custom Admin Role Assignments can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/adminRoleCustomAssignments:AdminRoleCustomAssignments example <resource_set_id>/<custom_role_id>
+         $ pulumi import okta:index/adminRoleCustomAssignments:AdminRoleCustomAssignments example &#60;resource_set_id&#62;/&#60;custom_role_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AdminRoleCustomAssignmentsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/admin_role_targets.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/admin_role_targets.py`

 * *Files 1% similar despite different names*

```diff
@@ -200,15 +200,15 @@
         ```
 
         ## Import
 
         Okta Admin Role Targets can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/adminRoleTargets:AdminRoleTargets example <user id>/<role type>
+         $ pulumi import okta:index/adminRoleTargets:AdminRoleTargets example &#60;user id&#62;/&#60;role type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] apps: List of app names (name represents set of app instances) or a combination of app name and app instance ID (like 'salesforce' or 'facebook.0oapsqQ6dv19pqyEo0g3').
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups: List of group IDs. Conflicts with `apps`.
         :param pulumi.Input[str] role_type: Name of the role associated with the user.
@@ -242,15 +242,15 @@
         ```
 
         ## Import
 
         Okta Admin Role Targets can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/adminRoleTargets:AdminRoleTargets example <user id>/<role type>
+         $ pulumi import okta:index/adminRoleTargets:AdminRoleTargets example &#60;user id&#62;/&#60;role type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AdminRoleTargetsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/_inputs.py`

 * *Files 1% similar despite different names*

```diff
@@ -200,15 +200,15 @@
     def __init__(__self__, *,
                  name: pulumi.Input[str],
                  type: pulumi.Input[str],
                  value: pulumi.Input[str],
                  filter_type: Optional[pulumi.Input[str]] = None):
         """
         :param pulumi.Input[str] name: Name of the claim that will be used in the token.
-        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param pulumi.Input[str] value: Value of the claim. Can be an Okta Expression Language statement that evaluates at the time the token is minted.
         :param pulumi.Input[str] filter_type: Groups claim filter. Can only be set if type is `"FILTER"`. Valid values: `"EQUALS"`, `"STARTS_WITH"`, `"CONTAINS"`, `"REGEX"`.
         """
         pulumi.set(__self__, "name", name)
         pulumi.set(__self__, "type", type)
         pulumi.set(__self__, "value", value)
         if filter_type is not None:
@@ -226,15 +226,15 @@
     def name(self, value: pulumi.Input[str]):
         pulumi.set(self, "name", value)
 
     @property
     @pulumi.getter
     def type(self) -> pulumi.Input[str]:
         """
-        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         """
         return pulumi.get(self, "type")
 
     @type.setter
     def type(self, value: pulumi.Input[str]):
         pulumi.set(self, "type", value)
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/auto_login.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/auto_login.py`

 * *Files 0% similar despite different names*

```diff
@@ -1059,29 +1059,29 @@
         ```
 
         ## Import
 
         Okta Auto Login App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_users
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_groups
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1153,29 +1153,29 @@
         ```
 
         ## Import
 
         Okta Auto Login App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_users
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/autoLogin:AutoLogin example <app id>/skip_groups
+         $ pulumi import okta:app/autoLogin:AutoLogin example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param AutoLoginArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/basic_auth.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/basic_auth.py`

 * *Files 0% similar despite different names*

```diff
@@ -709,29 +709,29 @@
         ```
 
         ## Import
 
         A Basic Auth App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_users
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_groups
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -775,29 +775,29 @@
         ```
 
         ## Import
 
         A Basic Auth App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_users
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/basicAuth:BasicAuth example <app id>/skip_groups
+         $ pulumi import okta:app/basicAuth:BasicAuth example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param BasicAuthArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/bookmark.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/bookmark.py`

 * *Files 1% similar despite different names*

```diff
@@ -709,29 +709,29 @@
         ```
 
         ## Import
 
         A Bookmark App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_users
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_groups
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -774,29 +774,29 @@
         ```
 
         ## Import
 
         A Bookmark App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_users
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/bookmark:Bookmark example <app id>/skip_groups
+         $ pulumi import okta:app/bookmark:Bookmark example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param BookmarkArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_metadata_saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_metadata_saml.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_oauth.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_oauth.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/get_saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/get_saml.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/group_assignment.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/group_assignment.py`

 * *Files 1% similar despite different names*

```diff
@@ -197,15 +197,15 @@
                  __props__=None):
         """
         ## Import
 
         An application group assignment can be imported via the `app_id` and the `group_id`.
 
         ```sh
-         $ pulumi import okta:app/groupAssignment:GroupAssignment example <app_id>/<group_id>
+         $ pulumi import okta:app/groupAssignment:GroupAssignment example &#60;app_id&#62;/&#60;group_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The ID of the application to assign a group to.
         :param pulumi.Input[str] group_id: The ID of the group to assign the app to.
         :param pulumi.Input[int] priority: Priority of group assignment.
@@ -220,15 +220,15 @@
                  opts: Optional[pulumi.ResourceOptions] = None):
         """
         ## Import
 
         An application group assignment can be imported via the `app_id` and the `group_id`.
 
         ```sh
-         $ pulumi import okta:app/groupAssignment:GroupAssignment example <app_id>/<group_id>
+         $ pulumi import okta:app/groupAssignment:GroupAssignment example &#60;app_id&#62;/&#60;group_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param GroupAssignmentArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth.py`

 * *Files 0% similar despite different names*

```diff
@@ -62,15 +62,15 @@
                  user_name_template_suffix: Optional[pulumi.Input[str]] = None,
                  user_name_template_type: Optional[pulumi.Input[str]] = None,
                  users: Optional[pulumi.Input[Sequence[pulumi.Input['OAuthUserArgs']]]] = None,
                  wildcard_redirect: Optional[pulumi.Input[str]] = None):
         """
         The set of arguments for constructing a OAuth resource.
         :param pulumi.Input[str] label: The Application's display name.
-        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
         :param pulumi.Input[str] admin_note: Application notes for admins.
         :param pulumi.Input[str] app_links_json: Displays specific appLinks for the app. The value for each application link should be boolean.
         :param pulumi.Input[str] app_settings_json: Application settings in JSON format.
         :param pulumi.Input[bool] auto_key_rotation: Requested key rotation mode.
@@ -237,15 +237,15 @@
     def label(self, value: pulumi.Input[str]):
         pulumi.set(self, "label", value)
 
     @property
     @pulumi.getter
     def type(self) -> pulumi.Input[str]:
         """
-        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         """
         return pulumi.get(self, "type")
 
     @type.setter
     def type(self, value: pulumi.Input[str]):
         pulumi.set(self, "type", value)
 
@@ -913,15 +913,15 @@
         :param pulumi.Input[Sequence[pulumi.Input[str]]] response_types: List of OAuth 2.0 response type strings.
         :param pulumi.Input[str] sign_on_mode: Sign-on mode of application.
         :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[str] status: The status of the application, by default, it is `"ACTIVE"`.
         :param pulumi.Input[str] token_endpoint_auth_method: Requested authentication method for the token endpoint. It can be set to `"none"`, `"client_secret_post"`, `"client_secret_basic"`, `"client_secret_jwt"`, `"private_key_jwt"`. To enable PKCE, set this to `"none"`.
         :param pulumi.Input[str] tos_uri: URI to web page providing client tos (terms of service).
-        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
         :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input['OAuthUserArgs']]] users: The users assigned to the application. It is recommended not to use this and instead use `app.User`.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         :param pulumi.Input[str] wildcard_redirect: *Early Access Property*. Indicates if the client is allowed to use wildcard matching of `redirect_uris`. Valid values: `"DISABLED"`, `"SUBDOMAIN"`. Default value is `"DISABLED"`.
@@ -1586,15 +1586,15 @@
     def tos_uri(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "tos_uri", value)
 
     @property
     @pulumi.getter
     def type(self) -> Optional[pulumi.Input[str]]:
         """
-        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         """
         return pulumi.get(self, "type")
 
     @type.setter
     def type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "type", value)
 
@@ -1762,29 +1762,29 @@
         ```
 
         ## Import
 
         An OIDC Application can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_users
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_groups
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1828,15 +1828,15 @@
         :param pulumi.Input[str] refresh_token_rotation: Refresh token rotation behavior. Valid values: `"STATIC"` or `"ROTATE"`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] response_types: List of OAuth 2.0 response type strings.
         :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[str] status: The status of the application, by default, it is `"ACTIVE"`.
         :param pulumi.Input[str] token_endpoint_auth_method: Requested authentication method for the token endpoint. It can be set to `"none"`, `"client_secret_post"`, `"client_secret_basic"`, `"client_secret_jwt"`, `"private_key_jwt"`. To enable PKCE, set this to `"none"`.
         :param pulumi.Input[str] tos_uri: URI to web page providing client tos (terms of service).
-        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
         :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['OAuthUserArgs']]]] users: The users assigned to the application. It is recommended not to use this and instead use `app.User`.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         :param pulumi.Input[str] wildcard_redirect: *Early Access Property*. Indicates if the client is allowed to use wildcard matching of `redirect_uris`. Valid values: `"DISABLED"`, `"SUBDOMAIN"`. Default value is `"DISABLED"`.
@@ -1883,29 +1883,29 @@
         ```
 
         ## Import
 
         An OIDC Application can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_users
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/oAuth:OAuth example <app id>/skip_groups
+         $ pulumi import okta:app/oAuth:OAuth example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param OAuthArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -2160,15 +2160,15 @@
         :param pulumi.Input[Sequence[pulumi.Input[str]]] response_types: List of OAuth 2.0 response type strings.
         :param pulumi.Input[str] sign_on_mode: Sign-on mode of application.
         :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
         :param pulumi.Input[str] status: The status of the application, by default, it is `"ACTIVE"`.
         :param pulumi.Input[str] token_endpoint_auth_method: Requested authentication method for the token endpoint. It can be set to `"none"`, `"client_secret_post"`, `"client_secret_basic"`, `"client_secret_jwt"`, `"private_key_jwt"`. To enable PKCE, set this to `"none"`.
         :param pulumi.Input[str] tos_uri: URI to web page providing client tos (terms of service).
-        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param pulumi.Input[str] type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
         :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['OAuthUserArgs']]]] users: The users assigned to the application. It is recommended not to use this and instead use `app.User`.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         :param pulumi.Input[str] wildcard_redirect: *Early Access Property*. Indicates if the client is allowed to use wildcard matching of `redirect_uris`. Valid values: `"DISABLED"`, `"SUBDOMAIN"`. Default value is `"DISABLED"`.
@@ -2597,15 +2597,15 @@
         """
         return pulumi.get(self, "tos_uri")
 
     @property
     @pulumi.getter
     def type(self) -> pulumi.Output[str]:
         """
-        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         """
         return pulumi.get(self, "type")
 
     @property
     @pulumi.getter(name="userNameTemplate")
     def user_name_template(self) -> pulumi.Output[Optional[str]]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth_post_logout_redirect_uri.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth_post_logout_redirect_uri.py`

 * *Files 2% similar despite different names*

```diff
@@ -118,15 +118,15 @@
         ```
 
         ## Import
 
         A post logout redirect URI can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuthPostLogoutRedirectUri:OAuthPostLogoutRedirectUri example <app id>/<uri>
+         $ pulumi import okta:app/oAuthPostLogoutRedirectUri:OAuthPostLogoutRedirectUri example &#60;app id&#62;/&#60;uri&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: OAuth application ID.
         :param pulumi.Input[str] uri: Post Logout Redirect URI to append to Okta OIDC application.
         """
@@ -158,15 +158,15 @@
         ```
 
         ## Import
 
         A post logout redirect URI can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuthPostLogoutRedirectUri:OAuthPostLogoutRedirectUri example <app id>/<uri>
+         $ pulumi import okta:app/oAuthPostLogoutRedirectUri:OAuthPostLogoutRedirectUri example &#60;app id&#62;/&#60;uri&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param OAuthPostLogoutRedirectUriArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/o_auth_redirect_uri.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/o_auth_redirect_uri.py`

 * *Files 2% similar despite different names*

```diff
@@ -117,15 +117,15 @@
         ```
 
         ## Import
 
         A redirect URI can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuthRedirectUri:OAuthRedirectUri example <app id>/<uri>
+         $ pulumi import okta:app/oAuthRedirectUri:OAuthRedirectUri example &#60;app id&#62;/&#60;uri&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: OAuth application ID.
         :param pulumi.Input[str] uri: Redirect URI to append to Okta OIDC application.
         """
@@ -156,15 +156,15 @@
         ```
 
         ## Import
 
         A redirect URI can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/oAuthRedirectUri:OAuthRedirectUri example <app id>/<uri>
+         $ pulumi import okta:app/oAuthRedirectUri:OAuthRedirectUri example &#60;app id&#62;/&#60;uri&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param OAuthRedirectUriArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/outputs.py`

 * *Files 1% similar despite different names*

```diff
@@ -170,15 +170,15 @@
     def __init__(__self__, *,
                  name: str,
                  type: str,
                  value: str,
                  filter_type: Optional[str] = None):
         """
         :param str name: Name of the claim that will be used in the token.
-        :param str type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        :param str type: The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         :param str value: Value of the claim. Can be an Okta Expression Language statement that evaluates at the time the token is minted.
         :param str filter_type: Groups claim filter. Can only be set if type is `"FILTER"`. Valid values: `"EQUALS"`, `"STARTS_WITH"`, `"CONTAINS"`, `"REGEX"`.
         """
         pulumi.set(__self__, "name", name)
         pulumi.set(__self__, "type", type)
         pulumi.set(__self__, "value", value)
         if filter_type is not None:
@@ -192,15 +192,15 @@
         """
         return pulumi.get(self, "name")
 
     @property
     @pulumi.getter
     def type(self) -> str:
         """
-        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`.
+        The type of OAuth application. Valid values: `"web"`, `"native"`, `"browser"`, `"service"`. For SPA apps use `browser`.
         """
         return pulumi.get(self, "type")
 
     @property
     @pulumi.getter
     def value(self) -> str:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/saml.py`

 * *Files 3% similar despite different names*

```diff
@@ -65,61 +65,71 @@
                  user_name_template_type: Optional[pulumi.Input[str]] = None,
                  users: Optional[pulumi.Input[Sequence[pulumi.Input['SamlUserArgs']]]] = None):
         """
         The set of arguments for constructing a Saml resource.
         :param pulumi.Input[str] label: label of application.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
-        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
+        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. Default is: `false`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] acs_endpoints: An array of ACS endpoints. You can configure a maximum of 100 endpoints.
         :param pulumi.Input[str] admin_note: Application notes for admins.
         :param pulumi.Input[str] app_links_json: Displays specific appLinks for the app. The value for each application link should be boolean.
         :param pulumi.Input[str] app_settings_json: Application settings in JSON format.
         :param pulumi.Input[bool] assertion_signed: Determines whether the SAML assertion is digitally signed.
         :param pulumi.Input[Sequence[pulumi.Input['SamlAttributeStatementArgs']]] attribute_statements: List of SAML Attribute statements.
         :param pulumi.Input[str] audience: Audience restriction.
         :param pulumi.Input[str] authn_context_class_ref: Identifies the SAML authentication context class for the assertion’s authentication statement.
-        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar.
+        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar. Default is: `false`
         :param pulumi.Input[str] default_relay_state: Identifies a specific application resource in an IDP initiated SSO scenario.
         :param pulumi.Input[str] destination: Identifies the location where the SAML response is intended to be sent inside the SAML assertion.
         :param pulumi.Input[str] digest_algorithm: Determines the digest algorithm used to digitally sign the SAML assertion and response.
         :param pulumi.Input[str] enduser_note: Application notes for end users.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] features: features enabled. Notice: you can't currently configure provisioning features via the API.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups: Groups associated with the application.
                - `DEPRECATED`: Please replace usage with the `AppGroupAssignments` (or `app.GroupAssignment`) resource.
-        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app.
-        :param pulumi.Input[bool] hide_web: Do not display application icon to users
-        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it.
+        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app. Default is: `false`
+        :param pulumi.Input[bool] hide_web: Do not display application icon to users. Default is: `false`
+        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it. Default is: `false`
         :param pulumi.Input[str] idp_issuer: SAML issuer ID.
         :param pulumi.Input[bool] implicit_assignment: *Early Access Property*. Enables Federation Broker Mode. When this mode is enabled, `users` and `groups` arguments are ignored.
         :param pulumi.Input[str] inline_hook_id: Saml Inline Hook associated with the application.
         :param pulumi.Input[str] key_name: Certificate name. This modulates the rotation of keys. New name == new key. Required to be set with `key_years_valid`.
         :param pulumi.Input[int] key_years_valid: Number of years the certificate is valid (2 - 10 years).
         :param pulumi.Input[str] logo: Local file path to the logo. The file must be in PNG, JPG, or GIF format, and less than 1 MB in size.
-        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.
+        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.  
+               If not provided the following arguments are required:
+               - `sso_url`
+               - `recipient`
+               - `destination`
+               - `audience`
+               - `subject_name_id_template`
+               - `subject_name_id_format`
+               - `signature_algorithm`
+               - `digest_algorithm`
+               - `authn_context_class_ref`
         :param pulumi.Input[str] recipient: The location where the app may present the SAML assertion.
         :param pulumi.Input[bool] request_compressed: Denotes whether the request is compressed or not.
         :param pulumi.Input[bool] response_signed: Determines whether the SAML auth response message is digitally signed.
         :param pulumi.Input[str] saml_version: SAML version for the app's sign-on mode. Valid values are: `"2.0"` or `"1.1"`. Default is `"2.0"`.
         :param pulumi.Input[str] signature_algorithm: Signature algorithm used ot digitally sign the assertion and response.
         :param pulumi.Input[str] single_logout_certificate: x509 encoded certificate that the Service Provider uses to sign Single Logout requests.
                Note: should be provided without `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`, see [official documentation](https://developer.okta.com/docs/reference/api/apps/#service-provider-certificate).
         :param pulumi.Input[str] single_logout_issuer: The issuer of the Service Provider that generates the Single Logout request.
         :param pulumi.Input[str] single_logout_url: The location where the logout response is sent.
-        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
-        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         :param pulumi.Input[str] sp_issuer: SAML service provider issuer.
         :param pulumi.Input[str] sso_url: Single Sign-on Url.
         :param pulumi.Input[str] status: status of application.
         :param pulumi.Input[str] subject_name_id_format: Identifies the SAML processing rules.
         :param pulumi.Input[str] subject_name_id_template: Template for app user's username when a user is assigned to the app.
-        :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
+        :param pulumi.Input[str] user_name_template: Username template. Default is: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
-        :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
+        :param pulumi.Input[str] user_name_template_type: Username template type. Default is: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input['SamlUserArgs']]] users: Users associated with the application.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         """
         pulumi.set(__self__, "label", label)
         if accessibility_error_redirect_url is not None:
             pulumi.set(__self__, "accessibility_error_redirect_url", accessibility_error_redirect_url)
         if accessibility_login_redirect_url is not None:
@@ -259,15 +269,15 @@
     def accessibility_login_redirect_url(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "accessibility_login_redirect_url", value)
 
     @property
     @pulumi.getter(name="accessibilitySelfService")
     def accessibility_self_service(self) -> Optional[pulumi.Input[bool]]:
         """
-        Enable self-service. By default, it is `false`.
+        Enable self-service. Default is: `false`.
         """
         return pulumi.get(self, "accessibility_self_service")
 
     @accessibility_self_service.setter
     def accessibility_self_service(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "accessibility_self_service", value)
 
@@ -367,15 +377,15 @@
     def authn_context_class_ref(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "authn_context_class_ref", value)
 
     @property
     @pulumi.getter(name="autoSubmitToolbar")
     def auto_submit_toolbar(self) -> Optional[pulumi.Input[bool]]:
         """
-        Display auto submit toolbar.
+        Display auto submit toolbar. Default is: `false`
         """
         return pulumi.get(self, "auto_submit_toolbar")
 
     @auto_submit_toolbar.setter
     def auto_submit_toolbar(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "auto_submit_toolbar", value)
 
@@ -452,39 +462,39 @@
     def groups(self, value: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]]):
         pulumi.set(self, "groups", value)
 
     @property
     @pulumi.getter(name="hideIos")
     def hide_ios(self) -> Optional[pulumi.Input[bool]]:
         """
-        Do not display application icon on mobile app.
+        Do not display application icon on mobile app. Default is: `false`
         """
         return pulumi.get(self, "hide_ios")
 
     @hide_ios.setter
     def hide_ios(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "hide_ios", value)
 
     @property
     @pulumi.getter(name="hideWeb")
     def hide_web(self) -> Optional[pulumi.Input[bool]]:
         """
-        Do not display application icon to users
+        Do not display application icon to users. Default is: `false`
         """
         return pulumi.get(self, "hide_web")
 
     @hide_web.setter
     def hide_web(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "hide_web", value)
 
     @property
     @pulumi.getter(name="honorForceAuthn")
     def honor_force_authn(self) -> Optional[pulumi.Input[bool]]:
         """
-        Prompt user to re-authenticate if SP asks for it.
+        Prompt user to re-authenticate if SP asks for it. Default is: `false`
         """
         return pulumi.get(self, "honor_force_authn")
 
     @honor_force_authn.setter
     def honor_force_authn(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "honor_force_authn", value)
 
@@ -560,15 +570,25 @@
     def logo(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "logo", value)
 
     @property
     @pulumi.getter(name="preconfiguredApp")
     def preconfigured_app(self) -> Optional[pulumi.Input[str]]:
         """
-        name of application from the Okta Integration Network, if not included a custom app will be created.
+        name of application from the Okta Integration Network, if not included a custom app will be created.  
+        If not provided the following arguments are required:
+        - `sso_url`
+        - `recipient`
+        - `destination`
+        - `audience`
+        - `subject_name_id_template`
+        - `subject_name_id_format`
+        - `signature_algorithm`
+        - `digest_algorithm`
+        - `authn_context_class_ref`
         """
         return pulumi.get(self, "preconfigured_app")
 
     @preconfigured_app.setter
     def preconfigured_app(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "preconfigured_app", value)
 
@@ -669,27 +689,27 @@
     def single_logout_url(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "single_logout_url", value)
 
     @property
     @pulumi.getter(name="skipGroups")
     def skip_groups(self) -> Optional[pulumi.Input[bool]]:
         """
-        Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_groups")
 
     @skip_groups.setter
     def skip_groups(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "skip_groups", value)
 
     @property
     @pulumi.getter(name="skipUsers")
     def skip_users(self) -> Optional[pulumi.Input[bool]]:
         """
-        Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_users")
 
     @skip_users.setter
     def skip_users(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "skip_users", value)
 
@@ -753,15 +773,15 @@
     def subject_name_id_template(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "subject_name_id_template", value)
 
     @property
     @pulumi.getter(name="userNameTemplate")
     def user_name_template(self) -> Optional[pulumi.Input[str]]:
         """
-        Username template. Default: `"${source.login}"`
+        Username template. Default is: `"${source.login}"`
         """
         return pulumi.get(self, "user_name_template")
 
     @user_name_template.setter
     def user_name_template(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template", value)
 
@@ -789,15 +809,15 @@
     def user_name_template_suffix(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template_suffix", value)
 
     @property
     @pulumi.getter(name="userNameTemplateType")
     def user_name_template_type(self) -> Optional[pulumi.Input[str]]:
         """
-        Username template type. Default: `"BUILT_IN"`.
+        Username template type. Default is: `"BUILT_IN"`.
         """
         return pulumi.get(self, "user_name_template_type")
 
     @user_name_template_type.setter
     def user_name_template_type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template_type", value)
 
@@ -878,73 +898,83 @@
                  user_name_template_suffix: Optional[pulumi.Input[str]] = None,
                  user_name_template_type: Optional[pulumi.Input[str]] = None,
                  users: Optional[pulumi.Input[Sequence[pulumi.Input['SamlUserArgs']]]] = None):
         """
         Input properties used for looking up and filtering Saml resources.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
-        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
+        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. Default is: `false`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] acs_endpoints: An array of ACS endpoints. You can configure a maximum of 100 endpoints.
         :param pulumi.Input[str] admin_note: Application notes for admins.
         :param pulumi.Input[str] app_links_json: Displays specific appLinks for the app. The value for each application link should be boolean.
         :param pulumi.Input[str] app_settings_json: Application settings in JSON format.
         :param pulumi.Input[bool] assertion_signed: Determines whether the SAML assertion is digitally signed.
         :param pulumi.Input[Sequence[pulumi.Input['SamlAttributeStatementArgs']]] attribute_statements: List of SAML Attribute statements.
         :param pulumi.Input[str] audience: Audience restriction.
         :param pulumi.Input[str] authn_context_class_ref: Identifies the SAML authentication context class for the assertion’s authentication statement.
-        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar.
+        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar. Default is: `false`
         :param pulumi.Input[str] certificate: The raw signing certificate.
         :param pulumi.Input[str] default_relay_state: Identifies a specific application resource in an IDP initiated SSO scenario.
         :param pulumi.Input[str] destination: Identifies the location where the SAML response is intended to be sent inside the SAML assertion.
         :param pulumi.Input[str] digest_algorithm: Determines the digest algorithm used to digitally sign the SAML assertion and response.
         :param pulumi.Input[str] enduser_note: Application notes for end users.
         :param pulumi.Input[str] entity_key: Entity ID, the ID portion of the `entity_url`.
         :param pulumi.Input[str] entity_url: Entity URL for instance [http://www.okta.com/exk1fcia6d6EMsf331d8](http://www.okta.com/exk1fcia6d6EMsf331d8).
         :param pulumi.Input[Sequence[pulumi.Input[str]]] features: features enabled. Notice: you can't currently configure provisioning features via the API.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups: Groups associated with the application.
                - `DEPRECATED`: Please replace usage with the `AppGroupAssignments` (or `app.GroupAssignment`) resource.
-        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app.
-        :param pulumi.Input[bool] hide_web: Do not display application icon to users
-        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it.
+        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app. Default is: `false`
+        :param pulumi.Input[bool] hide_web: Do not display application icon to users. Default is: `false`
+        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it. Default is: `false`
         :param pulumi.Input[str] http_post_binding: `urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Post` location from the SAML metadata.
         :param pulumi.Input[str] http_redirect_binding: `urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect` location from the SAML metadata.
         :param pulumi.Input[str] idp_issuer: SAML issuer ID.
         :param pulumi.Input[bool] implicit_assignment: *Early Access Property*. Enables Federation Broker Mode. When this mode is enabled, `users` and `groups` arguments are ignored.
         :param pulumi.Input[str] inline_hook_id: Saml Inline Hook associated with the application.
         :param pulumi.Input[str] key_id: Certificate key ID.
         :param pulumi.Input[str] key_name: Certificate name. This modulates the rotation of keys. New name == new key. Required to be set with `key_years_valid`.
         :param pulumi.Input[int] key_years_valid: Number of years the certificate is valid (2 - 10 years).
         :param pulumi.Input[str] label: label of application.
         :param pulumi.Input[str] logo: Local file path to the logo. The file must be in PNG, JPG, or GIF format, and less than 1 MB in size.
         :param pulumi.Input[str] logo_url: Direct link of application logo.
         :param pulumi.Input[str] metadata: The raw SAML metadata in XML.
         :param pulumi.Input[str] metadata_url: SAML xml metadata URL.
         :param pulumi.Input[str] name: The name of the attribute statement.
-        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.
+        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.  
+               If not provided the following arguments are required:
+               - `sso_url`
+               - `recipient`
+               - `destination`
+               - `audience`
+               - `subject_name_id_template`
+               - `subject_name_id_format`
+               - `signature_algorithm`
+               - `digest_algorithm`
+               - `authn_context_class_ref`
         :param pulumi.Input[str] recipient: The location where the app may present the SAML assertion.
         :param pulumi.Input[bool] request_compressed: Denotes whether the request is compressed or not.
         :param pulumi.Input[bool] response_signed: Determines whether the SAML auth response message is digitally signed.
         :param pulumi.Input[str] saml_version: SAML version for the app's sign-on mode. Valid values are: `"2.0"` or `"1.1"`. Default is `"2.0"`.
         :param pulumi.Input[str] sign_on_mode: Sign-on mode of application.
         :param pulumi.Input[str] signature_algorithm: Signature algorithm used ot digitally sign the assertion and response.
         :param pulumi.Input[str] single_logout_certificate: x509 encoded certificate that the Service Provider uses to sign Single Logout requests.
                Note: should be provided without `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`, see [official documentation](https://developer.okta.com/docs/reference/api/apps/#service-provider-certificate).
         :param pulumi.Input[str] single_logout_issuer: The issuer of the Service Provider that generates the Single Logout request.
         :param pulumi.Input[str] single_logout_url: The location where the logout response is sent.
-        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
-        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         :param pulumi.Input[str] sp_issuer: SAML service provider issuer.
         :param pulumi.Input[str] sso_url: Single Sign-on Url.
         :param pulumi.Input[str] status: status of application.
         :param pulumi.Input[str] subject_name_id_format: Identifies the SAML processing rules.
         :param pulumi.Input[str] subject_name_id_template: Template for app user's username when a user is assigned to the app.
-        :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
+        :param pulumi.Input[str] user_name_template: Username template. Default is: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
-        :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
+        :param pulumi.Input[str] user_name_template_type: Username template type. Default is: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input['SamlUserArgs']]] users: Users associated with the application.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         """
         if accessibility_error_redirect_url is not None:
             pulumi.set(__self__, "accessibility_error_redirect_url", accessibility_error_redirect_url)
         if accessibility_login_redirect_url is not None:
             pulumi.set(__self__, "accessibility_login_redirect_url", accessibility_login_redirect_url)
@@ -1095,15 +1125,15 @@
     def accessibility_login_redirect_url(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "accessibility_login_redirect_url", value)
 
     @property
     @pulumi.getter(name="accessibilitySelfService")
     def accessibility_self_service(self) -> Optional[pulumi.Input[bool]]:
         """
-        Enable self-service. By default, it is `false`.
+        Enable self-service. Default is: `false`.
         """
         return pulumi.get(self, "accessibility_self_service")
 
     @accessibility_self_service.setter
     def accessibility_self_service(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "accessibility_self_service", value)
 
@@ -1203,15 +1233,15 @@
     def authn_context_class_ref(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "authn_context_class_ref", value)
 
     @property
     @pulumi.getter(name="autoSubmitToolbar")
     def auto_submit_toolbar(self) -> Optional[pulumi.Input[bool]]:
         """
-        Display auto submit toolbar.
+        Display auto submit toolbar. Default is: `false`
         """
         return pulumi.get(self, "auto_submit_toolbar")
 
     @auto_submit_toolbar.setter
     def auto_submit_toolbar(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "auto_submit_toolbar", value)
 
@@ -1324,39 +1354,39 @@
     def groups(self, value: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]]):
         pulumi.set(self, "groups", value)
 
     @property
     @pulumi.getter(name="hideIos")
     def hide_ios(self) -> Optional[pulumi.Input[bool]]:
         """
-        Do not display application icon on mobile app.
+        Do not display application icon on mobile app. Default is: `false`
         """
         return pulumi.get(self, "hide_ios")
 
     @hide_ios.setter
     def hide_ios(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "hide_ios", value)
 
     @property
     @pulumi.getter(name="hideWeb")
     def hide_web(self) -> Optional[pulumi.Input[bool]]:
         """
-        Do not display application icon to users
+        Do not display application icon to users. Default is: `false`
         """
         return pulumi.get(self, "hide_web")
 
     @hide_web.setter
     def hide_web(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "hide_web", value)
 
     @property
     @pulumi.getter(name="honorForceAuthn")
     def honor_force_authn(self) -> Optional[pulumi.Input[bool]]:
         """
-        Prompt user to re-authenticate if SP asks for it.
+        Prompt user to re-authenticate if SP asks for it. Default is: `false`
         """
         return pulumi.get(self, "honor_force_authn")
 
     @honor_force_authn.setter
     def honor_force_authn(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "honor_force_authn", value)
 
@@ -1528,15 +1558,25 @@
     def name(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "name", value)
 
     @property
     @pulumi.getter(name="preconfiguredApp")
     def preconfigured_app(self) -> Optional[pulumi.Input[str]]:
         """
-        name of application from the Okta Integration Network, if not included a custom app will be created.
+        name of application from the Okta Integration Network, if not included a custom app will be created.  
+        If not provided the following arguments are required:
+        - `sso_url`
+        - `recipient`
+        - `destination`
+        - `audience`
+        - `subject_name_id_template`
+        - `subject_name_id_format`
+        - `signature_algorithm`
+        - `digest_algorithm`
+        - `authn_context_class_ref`
         """
         return pulumi.get(self, "preconfigured_app")
 
     @preconfigured_app.setter
     def preconfigured_app(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "preconfigured_app", value)
 
@@ -1649,27 +1689,27 @@
     def single_logout_url(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "single_logout_url", value)
 
     @property
     @pulumi.getter(name="skipGroups")
     def skip_groups(self) -> Optional[pulumi.Input[bool]]:
         """
-        Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_groups")
 
     @skip_groups.setter
     def skip_groups(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "skip_groups", value)
 
     @property
     @pulumi.getter(name="skipUsers")
     def skip_users(self) -> Optional[pulumi.Input[bool]]:
         """
-        Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_users")
 
     @skip_users.setter
     def skip_users(self, value: Optional[pulumi.Input[bool]]):
         pulumi.set(self, "skip_users", value)
 
@@ -1733,15 +1773,15 @@
     def subject_name_id_template(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "subject_name_id_template", value)
 
     @property
     @pulumi.getter(name="userNameTemplate")
     def user_name_template(self) -> Optional[pulumi.Input[str]]:
         """
-        Username template. Default: `"${source.login}"`
+        Username template. Default is: `"${source.login}"`
         """
         return pulumi.get(self, "user_name_template")
 
     @user_name_template.setter
     def user_name_template(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template", value)
 
@@ -1769,15 +1809,15 @@
     def user_name_template_suffix(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template_suffix", value)
 
     @property
     @pulumi.getter(name="userNameTemplateType")
     def user_name_template_type(self) -> Optional[pulumi.Input[str]]:
         """
-        Username template type. Default: `"BUILT_IN"`.
+        Username template type. Default is: `"BUILT_IN"`.
         """
         return pulumi.get(self, "user_name_template_type")
 
     @user_name_template_type.setter
     def user_name_template_type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "user_name_template_type", value)
 
@@ -1990,83 +2030,93 @@
         ```
 
         ## Import
 
         A SAML App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_users
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_groups
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
-        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
+        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. Default is: `false`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] acs_endpoints: An array of ACS endpoints. You can configure a maximum of 100 endpoints.
         :param pulumi.Input[str] admin_note: Application notes for admins.
         :param pulumi.Input[str] app_links_json: Displays specific appLinks for the app. The value for each application link should be boolean.
         :param pulumi.Input[str] app_settings_json: Application settings in JSON format.
         :param pulumi.Input[bool] assertion_signed: Determines whether the SAML assertion is digitally signed.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['SamlAttributeStatementArgs']]]] attribute_statements: List of SAML Attribute statements.
         :param pulumi.Input[str] audience: Audience restriction.
         :param pulumi.Input[str] authn_context_class_ref: Identifies the SAML authentication context class for the assertion’s authentication statement.
-        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar.
+        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar. Default is: `false`
         :param pulumi.Input[str] default_relay_state: Identifies a specific application resource in an IDP initiated SSO scenario.
         :param pulumi.Input[str] destination: Identifies the location where the SAML response is intended to be sent inside the SAML assertion.
         :param pulumi.Input[str] digest_algorithm: Determines the digest algorithm used to digitally sign the SAML assertion and response.
         :param pulumi.Input[str] enduser_note: Application notes for end users.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] features: features enabled. Notice: you can't currently configure provisioning features via the API.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups: Groups associated with the application.
                - `DEPRECATED`: Please replace usage with the `AppGroupAssignments` (or `app.GroupAssignment`) resource.
-        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app.
-        :param pulumi.Input[bool] hide_web: Do not display application icon to users
-        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it.
+        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app. Default is: `false`
+        :param pulumi.Input[bool] hide_web: Do not display application icon to users. Default is: `false`
+        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it. Default is: `false`
         :param pulumi.Input[str] idp_issuer: SAML issuer ID.
         :param pulumi.Input[bool] implicit_assignment: *Early Access Property*. Enables Federation Broker Mode. When this mode is enabled, `users` and `groups` arguments are ignored.
         :param pulumi.Input[str] inline_hook_id: Saml Inline Hook associated with the application.
         :param pulumi.Input[str] key_name: Certificate name. This modulates the rotation of keys. New name == new key. Required to be set with `key_years_valid`.
         :param pulumi.Input[int] key_years_valid: Number of years the certificate is valid (2 - 10 years).
         :param pulumi.Input[str] label: label of application.
         :param pulumi.Input[str] logo: Local file path to the logo. The file must be in PNG, JPG, or GIF format, and less than 1 MB in size.
-        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.
+        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.  
+               If not provided the following arguments are required:
+               - `sso_url`
+               - `recipient`
+               - `destination`
+               - `audience`
+               - `subject_name_id_template`
+               - `subject_name_id_format`
+               - `signature_algorithm`
+               - `digest_algorithm`
+               - `authn_context_class_ref`
         :param pulumi.Input[str] recipient: The location where the app may present the SAML assertion.
         :param pulumi.Input[bool] request_compressed: Denotes whether the request is compressed or not.
         :param pulumi.Input[bool] response_signed: Determines whether the SAML auth response message is digitally signed.
         :param pulumi.Input[str] saml_version: SAML version for the app's sign-on mode. Valid values are: `"2.0"` or `"1.1"`. Default is `"2.0"`.
         :param pulumi.Input[str] signature_algorithm: Signature algorithm used ot digitally sign the assertion and response.
         :param pulumi.Input[str] single_logout_certificate: x509 encoded certificate that the Service Provider uses to sign Single Logout requests.
                Note: should be provided without `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`, see [official documentation](https://developer.okta.com/docs/reference/api/apps/#service-provider-certificate).
         :param pulumi.Input[str] single_logout_issuer: The issuer of the Service Provider that generates the Single Logout request.
         :param pulumi.Input[str] single_logout_url: The location where the logout response is sent.
-        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
-        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         :param pulumi.Input[str] sp_issuer: SAML service provider issuer.
         :param pulumi.Input[str] sso_url: Single Sign-on Url.
         :param pulumi.Input[str] status: status of application.
         :param pulumi.Input[str] subject_name_id_format: Identifies the SAML processing rules.
         :param pulumi.Input[str] subject_name_id_template: Template for app user's username when a user is assigned to the app.
-        :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
+        :param pulumi.Input[str] user_name_template: Username template. Default is: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
-        :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
+        :param pulumi.Input[str] user_name_template_type: Username template type. Default is: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['SamlUserArgs']]]] users: Users associated with the application.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         """
         ...
     @overload
     def __init__(__self__,
                  resource_name: str,
@@ -2212,29 +2262,29 @@
         ```
 
         ## Import
 
         A SAML App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_users
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/saml:Saml example <app id>/skip_groups
+         $ pulumi import okta:app/saml:Saml example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param SamlArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -2452,73 +2502,83 @@
         properties used to qualify the lookup.
 
         :param str resource_name: The unique name of the resulting resource.
         :param pulumi.Input[str] id: The unique provider ID of the resource to lookup.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
-        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
+        :param pulumi.Input[bool] accessibility_self_service: Enable self-service. Default is: `false`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] acs_endpoints: An array of ACS endpoints. You can configure a maximum of 100 endpoints.
         :param pulumi.Input[str] admin_note: Application notes for admins.
         :param pulumi.Input[str] app_links_json: Displays specific appLinks for the app. The value for each application link should be boolean.
         :param pulumi.Input[str] app_settings_json: Application settings in JSON format.
         :param pulumi.Input[bool] assertion_signed: Determines whether the SAML assertion is digitally signed.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['SamlAttributeStatementArgs']]]] attribute_statements: List of SAML Attribute statements.
         :param pulumi.Input[str] audience: Audience restriction.
         :param pulumi.Input[str] authn_context_class_ref: Identifies the SAML authentication context class for the assertion’s authentication statement.
-        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar.
+        :param pulumi.Input[bool] auto_submit_toolbar: Display auto submit toolbar. Default is: `false`
         :param pulumi.Input[str] certificate: The raw signing certificate.
         :param pulumi.Input[str] default_relay_state: Identifies a specific application resource in an IDP initiated SSO scenario.
         :param pulumi.Input[str] destination: Identifies the location where the SAML response is intended to be sent inside the SAML assertion.
         :param pulumi.Input[str] digest_algorithm: Determines the digest algorithm used to digitally sign the SAML assertion and response.
         :param pulumi.Input[str] enduser_note: Application notes for end users.
         :param pulumi.Input[str] entity_key: Entity ID, the ID portion of the `entity_url`.
         :param pulumi.Input[str] entity_url: Entity URL for instance [http://www.okta.com/exk1fcia6d6EMsf331d8](http://www.okta.com/exk1fcia6d6EMsf331d8).
         :param pulumi.Input[Sequence[pulumi.Input[str]]] features: features enabled. Notice: you can't currently configure provisioning features via the API.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups: Groups associated with the application.
                - `DEPRECATED`: Please replace usage with the `AppGroupAssignments` (or `app.GroupAssignment`) resource.
-        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app.
-        :param pulumi.Input[bool] hide_web: Do not display application icon to users
-        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it.
+        :param pulumi.Input[bool] hide_ios: Do not display application icon on mobile app. Default is: `false`
+        :param pulumi.Input[bool] hide_web: Do not display application icon to users. Default is: `false`
+        :param pulumi.Input[bool] honor_force_authn: Prompt user to re-authenticate if SP asks for it. Default is: `false`
         :param pulumi.Input[str] http_post_binding: `urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Post` location from the SAML metadata.
         :param pulumi.Input[str] http_redirect_binding: `urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect` location from the SAML metadata.
         :param pulumi.Input[str] idp_issuer: SAML issuer ID.
         :param pulumi.Input[bool] implicit_assignment: *Early Access Property*. Enables Federation Broker Mode. When this mode is enabled, `users` and `groups` arguments are ignored.
         :param pulumi.Input[str] inline_hook_id: Saml Inline Hook associated with the application.
         :param pulumi.Input[str] key_id: Certificate key ID.
         :param pulumi.Input[str] key_name: Certificate name. This modulates the rotation of keys. New name == new key. Required to be set with `key_years_valid`.
         :param pulumi.Input[int] key_years_valid: Number of years the certificate is valid (2 - 10 years).
         :param pulumi.Input[str] label: label of application.
         :param pulumi.Input[str] logo: Local file path to the logo. The file must be in PNG, JPG, or GIF format, and less than 1 MB in size.
         :param pulumi.Input[str] logo_url: Direct link of application logo.
         :param pulumi.Input[str] metadata: The raw SAML metadata in XML.
         :param pulumi.Input[str] metadata_url: SAML xml metadata URL.
         :param pulumi.Input[str] name: The name of the attribute statement.
-        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.
+        :param pulumi.Input[str] preconfigured_app: name of application from the Okta Integration Network, if not included a custom app will be created.  
+               If not provided the following arguments are required:
+               - `sso_url`
+               - `recipient`
+               - `destination`
+               - `audience`
+               - `subject_name_id_template`
+               - `subject_name_id_format`
+               - `signature_algorithm`
+               - `digest_algorithm`
+               - `authn_context_class_ref`
         :param pulumi.Input[str] recipient: The location where the app may present the SAML assertion.
         :param pulumi.Input[bool] request_compressed: Denotes whether the request is compressed or not.
         :param pulumi.Input[bool] response_signed: Determines whether the SAML auth response message is digitally signed.
         :param pulumi.Input[str] saml_version: SAML version for the app's sign-on mode. Valid values are: `"2.0"` or `"1.1"`. Default is `"2.0"`.
         :param pulumi.Input[str] sign_on_mode: Sign-on mode of application.
         :param pulumi.Input[str] signature_algorithm: Signature algorithm used ot digitally sign the assertion and response.
         :param pulumi.Input[str] single_logout_certificate: x509 encoded certificate that the Service Provider uses to sign Single Logout requests.
                Note: should be provided without `-----BEGIN CERTIFICATE-----` and `-----END CERTIFICATE-----`, see [official documentation](https://developer.okta.com/docs/reference/api/apps/#service-provider-certificate).
         :param pulumi.Input[str] single_logout_issuer: The issuer of the Service Provider that generates the Single Logout request.
         :param pulumi.Input[str] single_logout_url: The location where the logout response is sent.
-        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
-        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_groups: Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
+        :param pulumi.Input[bool] skip_users: Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         :param pulumi.Input[str] sp_issuer: SAML service provider issuer.
         :param pulumi.Input[str] sso_url: Single Sign-on Url.
         :param pulumi.Input[str] status: status of application.
         :param pulumi.Input[str] subject_name_id_format: Identifies the SAML processing rules.
         :param pulumi.Input[str] subject_name_id_template: Template for app user's username when a user is assigned to the app.
-        :param pulumi.Input[str] user_name_template: Username template. Default: `"${source.login}"`
+        :param pulumi.Input[str] user_name_template: Username template. Default is: `"${source.login}"`
         :param pulumi.Input[str] user_name_template_push_status: Push username on update. Valid values: `"PUSH"` and `"DONT_PUSH"`.
         :param pulumi.Input[str] user_name_template_suffix: Username template suffix.
-        :param pulumi.Input[str] user_name_template_type: Username template type. Default: `"BUILT_IN"`.
+        :param pulumi.Input[str] user_name_template_type: Username template type. Default is: `"BUILT_IN"`.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['SamlUserArgs']]]] users: Users associated with the application.
                - `DEPRECATED`: Please replace usage with the `app.User` resource.
         """
         opts = pulumi.ResourceOptions.merge(opts, pulumi.ResourceOptions(id=id))
 
         __props__ = _SamlState.__new__(_SamlState)
 
@@ -2600,15 +2660,15 @@
         """
         return pulumi.get(self, "accessibility_login_redirect_url")
 
     @property
     @pulumi.getter(name="accessibilitySelfService")
     def accessibility_self_service(self) -> pulumi.Output[Optional[bool]]:
         """
-        Enable self-service. By default, it is `false`.
+        Enable self-service. Default is: `false`.
         """
         return pulumi.get(self, "accessibility_self_service")
 
     @property
     @pulumi.getter(name="acsEndpoints")
     def acs_endpoints(self) -> pulumi.Output[Optional[Sequence[str]]]:
         """
@@ -2672,15 +2732,15 @@
         """
         return pulumi.get(self, "authn_context_class_ref")
 
     @property
     @pulumi.getter(name="autoSubmitToolbar")
     def auto_submit_toolbar(self) -> pulumi.Output[Optional[bool]]:
         """
-        Display auto submit toolbar.
+        Display auto submit toolbar. Default is: `false`
         """
         return pulumi.get(self, "auto_submit_toolbar")
 
     @property
     @pulumi.getter
     def certificate(self) -> pulumi.Output[str]:
         """
@@ -2753,31 +2813,31 @@
         """
         return pulumi.get(self, "groups")
 
     @property
     @pulumi.getter(name="hideIos")
     def hide_ios(self) -> pulumi.Output[Optional[bool]]:
         """
-        Do not display application icon on mobile app.
+        Do not display application icon on mobile app. Default is: `false`
         """
         return pulumi.get(self, "hide_ios")
 
     @property
     @pulumi.getter(name="hideWeb")
     def hide_web(self) -> pulumi.Output[Optional[bool]]:
         """
-        Do not display application icon to users
+        Do not display application icon to users. Default is: `false`
         """
         return pulumi.get(self, "hide_web")
 
     @property
     @pulumi.getter(name="honorForceAuthn")
     def honor_force_authn(self) -> pulumi.Output[Optional[bool]]:
         """
-        Prompt user to re-authenticate if SP asks for it.
+        Prompt user to re-authenticate if SP asks for it. Default is: `false`
         """
         return pulumi.get(self, "honor_force_authn")
 
     @property
     @pulumi.getter(name="httpPostBinding")
     def http_post_binding(self) -> pulumi.Output[str]:
         """
@@ -2889,15 +2949,25 @@
         """
         return pulumi.get(self, "name")
 
     @property
     @pulumi.getter(name="preconfiguredApp")
     def preconfigured_app(self) -> pulumi.Output[Optional[str]]:
         """
-        name of application from the Okta Integration Network, if not included a custom app will be created.
+        name of application from the Okta Integration Network, if not included a custom app will be created.  
+        If not provided the following arguments are required:
+        - `sso_url`
+        - `recipient`
+        - `destination`
+        - `audience`
+        - `subject_name_id_template`
+        - `subject_name_id_format`
+        - `signature_algorithm`
+        - `digest_algorithm`
+        - `authn_context_class_ref`
         """
         return pulumi.get(self, "preconfigured_app")
 
     @property
     @pulumi.getter
     def recipient(self) -> pulumi.Output[Optional[str]]:
         """
@@ -2970,23 +3040,23 @@
         """
         return pulumi.get(self, "single_logout_url")
 
     @property
     @pulumi.getter(name="skipGroups")
     def skip_groups(self) -> pulumi.Output[Optional[bool]]:
         """
-        Indicator that allows the app to skip `groups` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `groups` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_groups")
 
     @property
     @pulumi.getter(name="skipUsers")
     def skip_users(self) -> pulumi.Output[Optional[bool]]:
         """
-        Indicator that allows the app to skip `users` sync (it's also can be provided during import). Default is `false`.
+        Indicator that allows the app to skip `users` sync (it can also be provided during import). Default is `false`.
         """
         return pulumi.get(self, "skip_users")
 
     @property
     @pulumi.getter(name="spIssuer")
     def sp_issuer(self) -> pulumi.Output[Optional[str]]:
         """
@@ -3026,15 +3096,15 @@
         """
         return pulumi.get(self, "subject_name_id_template")
 
     @property
     @pulumi.getter(name="userNameTemplate")
     def user_name_template(self) -> pulumi.Output[Optional[str]]:
         """
-        Username template. Default: `"${source.login}"`
+        Username template. Default is: `"${source.login}"`
         """
         return pulumi.get(self, "user_name_template")
 
     @property
     @pulumi.getter(name="userNameTemplatePushStatus")
     def user_name_template_push_status(self) -> pulumi.Output[Optional[str]]:
         """
@@ -3050,15 +3120,15 @@
         """
         return pulumi.get(self, "user_name_template_suffix")
 
     @property
     @pulumi.getter(name="userNameTemplateType")
     def user_name_template_type(self) -> pulumi.Output[Optional[str]]:
         """
-        Username template type. Default: `"BUILT_IN"`.
+        Username template type. Default is: `"BUILT_IN"`.
         """
         return pulumi.get(self, "user_name_template_type")
 
     @property
     @pulumi.getter
     def users(self) -> pulumi.Output[Optional[Sequence['outputs.SamlUser']]]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/secure_password_store.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/secure_password_store.py`

 * *Files 0% similar despite different names*

```diff
@@ -1205,29 +1205,29 @@
         ```
 
         ## Import
 
         Secure Password Store Application can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_users
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_groups
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1288,29 +1288,29 @@
         ```
 
         ## Import
 
         Secure Password Store Application can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_users
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example <app id>/skip_groups
+         $ pulumi import okta:app/securePasswordStore:SecurePasswordStore example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param SecurePasswordStoreArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/swa.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/swa.py`

 * *Files 0% similar despite different names*

```diff
@@ -1043,29 +1043,29 @@
         ```
 
         ## Import
 
         Okta SWA App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_users
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_groups
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1121,29 +1121,29 @@
         ```
 
         ## Import
 
         Okta SWA App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_users
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/swa:Swa example <app id>/skip_groups
+         $ pulumi import okta:app/swa:Swa example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param SwaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/three_field.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/three_field.py`

 * *Files 0% similar despite different names*

```diff
@@ -1122,29 +1122,29 @@
         This resource allows you to create and configure a Three Field Application.
 
         ## Import
 
         A Three Field App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_users
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_groups
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1189,29 +1189,29 @@
         This resource allows you to create and configure a Three Field Application.
 
         ## Import
 
         A Three Field App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_users
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_users/skip_groups
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:app/threeField:ThreeField example <app id>/skip_groups
+         $ pulumi import okta:app/threeField:ThreeField example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param ThreeFieldArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user.py`

 * *Files 1% similar despite different names*

```diff
@@ -258,15 +258,15 @@
         ```
 
         ## Import
 
         An Application User can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/user:User example <app id>/<user id>
+         $ pulumi import okta:app/user:User example &#60;app id&#62;/&#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: App to associate user with.
         :param pulumi.Input[str] password: The password to use.
         :param pulumi.Input[str] profile: The JSON profile of the App User.
@@ -295,15 +295,15 @@
         ```
 
         ## Import
 
         An Application User can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:app/user:User example <app id>/<user id>
+         $ pulumi import okta:app/user:User example &#60;app id&#62;/&#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user_base_schema.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user_base_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -345,15 +345,15 @@
         ```
 
         ## Import
 
         App user base schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:app/userBaseSchema:UserBaseSchema example <app id>/<property name>
+         $ pulumi import okta:app/userBaseSchema:UserBaseSchema example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The Application's ID the user schema property should be assigned to.
         :param pulumi.Input[str] index: The property name.
         :param pulumi.Input[str] master: Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
@@ -390,15 +390,15 @@
         ```
 
         ## Import
 
         App user base schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:app/userBaseSchema:UserBaseSchema example <app id>/<property name>
+         $ pulumi import okta:app/userBaseSchema:UserBaseSchema example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserBaseSchemaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app/user_schema.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app/user_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -741,15 +741,15 @@
         ```
 
         ## Import
 
         App user schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:app/userSchema:UserSchema example <app id>/<property name>
+         $ pulumi import okta:app/userSchema:UserSchema example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The Application's ID the user custom schema property should be assigned to.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] array_enums: Array of values that an array property's items can be set to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['UserSchemaArrayOneOfArgs']]]] array_one_ofs: Display name and value an enum array can be set to.
@@ -796,15 +796,15 @@
         ```
 
         ## Import
 
         App user schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:app/userSchema:UserSchema example <app id>/<property name>
+         $ pulumi import okta:app/userSchema:UserSchema example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserSchemaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_group_assignments.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_group_assignments.py`

 * *Files 2% similar despite different names*

```diff
@@ -139,15 +139,15 @@
         > **IMPORTANT:** When using `AppGroupAssignments` it is expected to manage ALL group assignments for the target application.
 
         ## Import
 
         An application's group assignments can be imported via `app_id`.
 
         ```sh
-         $ pulumi import okta:index/appGroupAssignments:AppGroupAssignments example <app_id>
+         $ pulumi import okta:index/appGroupAssignments:AppGroupAssignments example &#60;app_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The ID of the application to assign a group to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['AppGroupAssignmentsGroupArgs']]]] groups: A group to assign the app to.
         """
@@ -198,15 +198,15 @@
         > **IMPORTANT:** When using `AppGroupAssignments` it is expected to manage ALL group assignments for the target application.
 
         ## Import
 
         An application's group assignments can be imported via `app_id`.
 
         ```sh
-         $ pulumi import okta:index/appGroupAssignments:AppGroupAssignments example <app_id>
+         $ pulumi import okta:index/appGroupAssignments:AppGroupAssignments example &#60;app_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppGroupAssignmentsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_oauth_api_scope.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_oauth_api_scope.py`

 * *Files 1% similar despite different names*

```diff
@@ -153,15 +153,15 @@
         ```
 
         ## Import
 
         OAuth API scopes can be imported via the Okta Application ID.
 
         ```sh
-         $ pulumi import okta:index/appOauthApiScope:AppOauthApiScope example <app id>
+         $ pulumi import okta:index/appOauthApiScope:AppOauthApiScope example &#60;app id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: ID of the application.
         :param pulumi.Input[str] issuer: The issuer of your Org Authorization Server, your Org URL.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] scopes: List of scopes for which consent is granted.
@@ -197,15 +197,15 @@
         ```
 
         ## Import
 
         OAuth API scopes can be imported via the Okta Application ID.
 
         ```sh
-         $ pulumi import okta:index/appOauthApiScope:AppOauthApiScope example <app id>
+         $ pulumi import okta:index/appOauthApiScope:AppOauthApiScope example &#60;app id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppOauthApiScopeArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_saml_app_settings.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_saml_app_settings.py`

 * *Files 1% similar despite different names*

```diff
@@ -126,15 +126,15 @@
         ```
 
         ## Import
 
         A settings for the SAML App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSamlAppSettings:AppSamlAppSettings example <app id>
+         $ pulumi import okta:index/appSamlAppSettings:AppSamlAppSettings example &#60;app id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: ID of the application.
         :param pulumi.Input[str] settings: Application settings in JSON format.
         """
@@ -174,15 +174,15 @@
         ```
 
         ## Import
 
         A settings for the SAML App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSamlAppSettings:AppSamlAppSettings example <app id>
+         $ pulumi import okta:index/appSamlAppSettings:AppSamlAppSettings example &#60;app id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppSamlAppSettingsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_shared_credentials.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_shared_credentials.py`

 * *Files 1% similar despite different names*

```diff
@@ -1122,29 +1122,29 @@
         ```
 
         ## Import
 
         Okta SWA Shared Credentials App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_users
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_users/skip_groups
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_groups
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] accessibility_error_redirect_url: Custom error page URL.
         :param pulumi.Input[str] accessibility_login_redirect_url: Custom login page for this application.
         :param pulumi.Input[bool] accessibility_self_service: Enable self-service. By default, it is `false`.
@@ -1215,29 +1215,29 @@
         ```
 
         ## Import
 
         Okta SWA Shared Credentials App can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;
         ```
 
          It's also possible to import app without groups or/and users. In this case ID may look like this
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_users
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_users
         ```
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_users/skip_groups
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_users/skip_groups
         ```
 
         ```sh
-         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example <app id>/skip_groups
+         $ pulumi import okta:index/appSharedCredentials:AppSharedCredentials example &#60;app id&#62;/skip_groups
         ```
 
         :param str resource_name: The name of the resource.
         :param AppSharedCredentialsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_signon_policy_rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_signon_policy_rule.py`

 * *Files 1% similar despite different names*

```diff
@@ -989,15 +989,15 @@
         ```
 
         ## Import
 
         Okta app sign-on policy rule can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSignonPolicyRule:AppSignonPolicyRule example <policy_id>/<rule_id>
+         $ pulumi import okta:index/appSignonPolicyRule:AppSignonPolicyRule example &#60;policy_id&#62;/&#60;rule_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] access: Allow or deny access based on the rule conditions. It can be set to `"ALLOW"` or `"DENY"`. Default is `"ALLOW"`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] constraints: - An array that contains nested Authenticator Constraint objects that are organized by the Authenticator class. Each element should be in JSON format.
         :param pulumi.Input[str] custom_expression: This is an advanced optional setting. If the expression is formatted incorrectly or conflicts with conditions set above, the rule may not match any users.
@@ -1251,15 +1251,15 @@
         ```
 
         ## Import
 
         Okta app sign-on policy rule can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/appSignonPolicyRule:AppSignonPolicyRule example <policy_id>/<rule_id>
+         $ pulumi import okta:index/appSignonPolicyRule:AppSignonPolicyRule example &#60;policy_id&#62;/&#60;rule_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppSignonPolicyRuleArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_user_base_schema_property.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_user_base_schema_property.py`

 * *Files 1% similar despite different names*

```diff
@@ -345,15 +345,15 @@
         ```
 
         ## Import
 
         App user base schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:index/appUserBaseSchemaProperty:AppUserBaseSchemaProperty example <app id>/<property name>
+         $ pulumi import okta:index/appUserBaseSchemaProperty:AppUserBaseSchemaProperty example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The Application's ID the user schema property should be assigned to.
         :param pulumi.Input[str] index: The property name.
         :param pulumi.Input[str] master: Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
@@ -390,15 +390,15 @@
         ```
 
         ## Import
 
         App user base schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:index/appUserBaseSchemaProperty:AppUserBaseSchemaProperty example <app id>/<property name>
+         $ pulumi import okta:index/appUserBaseSchemaProperty:AppUserBaseSchemaProperty example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppUserBaseSchemaPropertyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/app_user_schema_property.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/app_user_schema_property.py`

 * *Files 0% similar despite different names*

```diff
@@ -744,15 +744,15 @@
         ```
 
         ## Import
 
         App user schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:index/appUserSchemaProperty:AppUserSchemaProperty example <app id>/<property name>
+         $ pulumi import okta:index/appUserSchemaProperty:AppUserSchemaProperty example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] app_id: The Application's ID the user custom schema property should be assigned to.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] array_enums: Array of values that an array property's items can be set to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['AppUserSchemaPropertyArrayOneOfArgs']]]] array_one_ofs: Display name and value an enum array can be set to.
@@ -802,15 +802,15 @@
         ```
 
         ## Import
 
         App user schema property can be imported via the property index and app id.
 
         ```sh
-         $ pulumi import okta:index/appUserSchemaProperty:AppUserSchemaProperty example <app id>/<property name>
+         $ pulumi import okta:index/appUserSchemaProperty:AppUserSchemaProperty example &#60;app id&#62;/&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AppUserSchemaPropertyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/get_server_scopes.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/get_server_scopes.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server.py`

 * *Files 1% similar despite different names*

```diff
@@ -312,15 +312,15 @@
         ```
 
         ## Import
 
         Authorization Server can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:auth/server:Server example <auth server id>
+         $ pulumi import okta:auth/server:Server example &#60;auth server id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] audiences: The recipients that the tokens are intended for. This becomes the `aud` claim in an access token.
         :param pulumi.Input[str] credentials_rotation_mode: The key rotation mode for the authorization server. Can be `"AUTO"` or `"MANUAL"`.
         :param pulumi.Input[str] description: The description of the authorization server.
@@ -353,15 +353,15 @@
         ```
 
         ## Import
 
         Authorization Server can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:auth/server:Server example <auth server id>
+         $ pulumi import okta:auth/server:Server example &#60;auth server id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_claim.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_claim.py`

 * *Files 1% similar despite different names*

```diff
@@ -345,15 +345,15 @@
         ```
 
         ## Import
 
         Authorization Server Claim can be imported via the Auth Server ID and Claim ID.
 
         ```sh
-         $ pulumi import okta:auth/serverClaim:ServerClaim example <auth server id>/<claim id>
+         $ pulumi import okta:auth/serverClaim:ServerClaim example &#60;auth server id&#62;/&#60;claim id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] always_include_in_token: Specifies whether to include claims in token, by default it is set to `true`.
         :param pulumi.Input[str] auth_server_id: ID of the authorization server.
         :param pulumi.Input[str] claim_type: Specifies whether the claim is for an access token `"RESOURCE"` or ID token `"IDENTITY"`.
@@ -389,15 +389,15 @@
         ```
 
         ## Import
 
         Authorization Server Claim can be imported via the Auth Server ID and Claim ID.
 
         ```sh
-         $ pulumi import okta:auth/serverClaim:ServerClaim example <auth server id>/<claim id>
+         $ pulumi import okta:auth/serverClaim:ServerClaim example &#60;auth server id&#62;/&#60;claim id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerClaimArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy.py`

 * *Files 0% similar despite different names*

```diff
@@ -285,15 +285,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy can be imported via the Auth Server ID and Policy ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicy:ServerPolicy example <auth server id>/<policy id>
+         $ pulumi import okta:auth/serverPolicy:ServerPolicy example &#60;auth server id&#62;/&#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] auth_server_id: The ID of the Auth Server.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] client_whitelists: The clients to whitelist the policy for. `["ALL_CLIENTS"]` is a special value that can be used to whitelist all clients, otherwise it is a list of client ids.
         :param pulumi.Input[str] description: The description of the Auth Server Policy.
@@ -328,15 +328,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy can be imported via the Auth Server ID and Policy ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicy:ServerPolicy example <auth server id>/<policy id>
+         $ pulumi import okta:auth/serverPolicy:ServerPolicy example &#60;auth server id&#62;/&#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerPolicyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy_claim.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy_claim.py`

 * *Files 0% similar despite different names*

```diff
@@ -594,15 +594,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy Rule can be imported via the Auth Server ID, Policy ID, and Policy Rule ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicyClaim:ServerPolicyClaim example <auth server id>/<policy id>/<policy rule id>
+         $ pulumi import okta:auth/serverPolicyClaim:ServerPolicyClaim example &#60;auth server id&#62;/&#60;policy id&#62;/&#60;policy rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[int] access_token_lifetime_minutes: Lifetime of access token. Can be set to a value between 5 and 1440 minutes.
         :param pulumi.Input[str] auth_server_id: Auth Server ID.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] grant_type_whitelists: Accepted grant type values, `"authorization_code"`, `"implicit"`, `"password"`, `"client_credentials"`, 
@@ -650,15 +650,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy Rule can be imported via the Auth Server ID, Policy ID, and Policy Rule ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicyClaim:ServerPolicyClaim example <auth server id>/<policy id>/<policy rule id>
+         $ pulumi import okta:auth/serverPolicyClaim:ServerPolicyClaim example &#60;auth server id&#62;/&#60;policy id&#62;/&#60;policy rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerPolicyClaimArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_policy_rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_policy_rule.py`

 * *Files 1% similar despite different names*

```diff
@@ -589,15 +589,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy Rule can be imported via the Auth Server ID, Policy ID, and Policy Rule ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicyRule:ServerPolicyRule example <auth server id>/<policy id>/<policy rule id>
+         $ pulumi import okta:auth/serverPolicyRule:ServerPolicyRule example &#60;auth server id&#62;/&#60;policy id&#62;/&#60;policy rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[int] access_token_lifetime_minutes: Lifetime of access token. Can be set to a value between 5 and 1440 minutes.
         :param pulumi.Input[str] auth_server_id: Auth Server ID.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] grant_type_whitelists: Accepted grant type values, `"authorization_code"`, `"implicit"`, `"password"`, `"client_credentials"`, 
@@ -645,15 +645,15 @@
         ```
 
         ## Import
 
         Authorization Server Policy Rule can be imported via the Auth Server ID, Policy ID, and Policy Rule ID.
 
         ```sh
-         $ pulumi import okta:auth/serverPolicyRule:ServerPolicyRule example <auth server id>/<policy id>/<policy rule id>
+         $ pulumi import okta:auth/serverPolicyRule:ServerPolicyRule example &#60;auth server id&#62;/&#60;policy id&#62;/&#60;policy rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerPolicyRuleArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth/server_scope.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth/server_scope.py`

 * *Files 1% similar despite different names*

```diff
@@ -280,15 +280,15 @@
         ```
 
         ## Import
 
         Okta Auth Server Scope can be imported via the Auth Server ID and Scope ID.
 
         ```sh
-         $ pulumi import okta:auth/serverScope:ServerScope example <auth server id>/<scope id>
+         $ pulumi import okta:auth/serverScope:ServerScope example &#60;auth server id&#62;/&#60;scope id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] auth_server_id: Auth Server ID.
         :param pulumi.Input[str] consent: Indicates whether a consent dialog is needed for the scope. It can be set to `"REQUIRED"` or `"IMPLICIT"`.
         :param pulumi.Input[bool] default: A default scope will be returned in an access token when the client omits the scope parameter in a token request, provided this scope is allowed as part of the access policy rule.
@@ -321,15 +321,15 @@
         ```
 
         ## Import
 
         Okta Auth Server Scope can be imported via the Auth Server ID and Scope ID.
 
         ```sh
-         $ pulumi import okta:auth/serverScope:ServerScope example <auth server id>/<scope id>
+         $ pulumi import okta:auth/serverScope:ServerScope example &#60;auth server id&#62;/&#60;scope id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ServerScopeArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth_server_claim_default.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth_server_claim_default.py`

 * *Files 2% similar despite different names*

```diff
@@ -252,21 +252,21 @@
         ```
 
         ## Import
 
         Authorization Server Claim can be imported via the Auth Server ID and Claim ID or Claim Name.
 
         ```sh
-         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example <auth server id>/<claim id>
+         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example &#60;auth server id&#62;/&#60;claim id&#62;
         ```
 
          or
 
         ```sh
-         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example <auth server id>/<claim name>
+         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example &#60;auth server id&#62;/&#60;claim name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] always_include_in_token: Specifies whether to include claims in token.
         :param pulumi.Input[str] auth_server_id: ID of the authorization server.
         :param pulumi.Input[str] name: The name of the claim. Can be set to `"sub"`, `"address"`, `"birthdate"`, `"email"`,
@@ -297,21 +297,21 @@
         ```
 
         ## Import
 
         Authorization Server Claim can be imported via the Auth Server ID and Claim ID or Claim Name.
 
         ```sh
-         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example <auth server id>/<claim id>
+         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example &#60;auth server id&#62;/&#60;claim id&#62;
         ```
 
          or
 
         ```sh
-         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example <auth server id>/<claim name>
+         $ pulumi import okta:index/authServerClaimDefault:AuthServerClaimDefault example &#60;auth server id&#62;/&#60;claim name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AuthServerClaimDefaultArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/auth_server_default.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/auth_server_default.py`

 * *Files 1% similar despite different names*

```diff
@@ -309,15 +309,15 @@
         ```
 
         ## Import
 
         Authorization Server can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/authServerDefault:AuthServerDefault example <auth server name>
+         $ pulumi import okta:index/authServerDefault:AuthServerDefault example &#60;auth server name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] audiences: The recipients that the tokens are intended for. This becomes the `aud` claim in an access token.
         :param pulumi.Input[str] credentials_rotation_mode: The key rotation mode for the authorization server. Can be `"AUTO"` or `"MANUAL"`.
         :param pulumi.Input[str] description: The description of the authorization server.
@@ -346,15 +346,15 @@
         ```
 
         ## Import
 
         Authorization Server can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/authServerDefault:AuthServerDefault example <auth server name>
+         $ pulumi import okta:index/authServerDefault:AuthServerDefault example &#60;auth server name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AuthServerDefaultArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/authenticator.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/authenticator.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,15 +19,15 @@
                  provider_hostname: Optional[pulumi.Input[str]] = None,
                  provider_shared_secret: Optional[pulumi.Input[str]] = None,
                  provider_user_name_template: Optional[pulumi.Input[str]] = None,
                  settings: Optional[pulumi.Input[str]] = None,
                  status: Optional[pulumi.Input[str]] = None):
         """
         The set of arguments for constructing a Authenticator resource.
-        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         :param pulumi.Input[str] name: Name of the authenticator.
         :param pulumi.Input[int] provider_auth_port: The RADIUS server port (for example 1812). This is defined when the On-Prem RADIUS server is configured. Default is `9000`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_hostname: Server host name or IP address. Default is `"localhost"`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_shared_secret: An authentication key that must be defined when the RADIUS server is configured, and must be the same on both the RADIUS client and server. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_user_name_template: Username template expected by the provider. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] settings: Settings for the authenticator. Settings object contains values based on Authenticator key. It is not used for authenticators with type `"security_key"`.
         :param pulumi.Input[str] status: Status of the authenticator. Default is `ACTIVE`.
@@ -48,15 +48,15 @@
         if status is not None:
             pulumi.set(__self__, "status", status)
 
     @property
     @pulumi.getter
     def key(self) -> pulumi.Input[str]:
         """
-        A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         """
         return pulumi.get(self, "key")
 
     @key.setter
     def key(self, value: pulumi.Input[str]):
         pulumi.set(self, "key", value)
 
@@ -157,15 +157,15 @@
                  provider_type: Optional[pulumi.Input[str]] = None,
                  provider_user_name_template: Optional[pulumi.Input[str]] = None,
                  settings: Optional[pulumi.Input[str]] = None,
                  status: Optional[pulumi.Input[str]] = None,
                  type: Optional[pulumi.Input[str]] = None):
         """
         Input properties used for looking up and filtering Authenticator resources.
-        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         :param pulumi.Input[str] name: Name of the authenticator.
         :param pulumi.Input[int] provider_auth_port: The RADIUS server port (for example 1812). This is defined when the On-Prem RADIUS server is configured. Default is `9000`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_hostname: Server host name or IP address. Default is `"localhost"`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_instance_id: App Instance ID.
         :param pulumi.Input[str] provider_shared_secret: An authentication key that must be defined when the RADIUS server is configured, and must be the same on both the RADIUS client and server. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_type: The type of Authenticator. Values include: `"password"`, `"security_question"`, `"phone"`, `"email"`, `"app"`, `"federated"`, and `"security_key"`.
         :param pulumi.Input[str] provider_user_name_template: Username template expected by the provider. Used only for authenticators with type `"security_key"`.
@@ -196,15 +196,15 @@
         if type is not None:
             pulumi.set(__self__, "type", type)
 
     @property
     @pulumi.getter
     def key(self) -> Optional[pulumi.Input[str]]:
         """
-        A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         """
         return pulumi.get(self, "key")
 
     @key.setter
     def key(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "key", value)
 
@@ -365,20 +365,20 @@
         ```
 
         ## Import
 
         Okta authenticator can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/authenticator:Authenticator example <authenticator_id>
+         $ pulumi import okta:index/authenticator:Authenticator example &#60;authenticator_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
-        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         :param pulumi.Input[str] name: Name of the authenticator.
         :param pulumi.Input[int] provider_auth_port: The RADIUS server port (for example 1812). This is defined when the On-Prem RADIUS server is configured. Default is `9000`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_hostname: Server host name or IP address. Default is `"localhost"`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_shared_secret: An authentication key that must be defined when the RADIUS server is configured, and must be the same on both the RADIUS client and server. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_user_name_template: Username template expected by the provider. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] settings: Settings for the authenticator. Settings object contains values based on Authenticator key. It is not used for authenticators with type `"security_key"`.
         :param pulumi.Input[str] status: Status of the authenticator. Default is `ACTIVE`.
@@ -411,15 +411,15 @@
         ```
 
         ## Import
 
         Okta authenticator can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/authenticator:Authenticator example <authenticator_id>
+         $ pulumi import okta:index/authenticator:Authenticator example &#60;authenticator_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param AuthenticatorArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -490,15 +490,15 @@
         """
         Get an existing Authenticator resource's state with the given name, id, and optional extra
         properties used to qualify the lookup.
 
         :param str resource_name: The unique name of the resulting resource.
         :param pulumi.Input[str] id: The unique provider ID of the resource to lookup.
         :param pulumi.ResourceOptions opts: Options for the resource.
-        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        :param pulumi.Input[str] key: A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         :param pulumi.Input[str] name: Name of the authenticator.
         :param pulumi.Input[int] provider_auth_port: The RADIUS server port (for example 1812). This is defined when the On-Prem RADIUS server is configured. Default is `9000`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_hostname: Server host name or IP address. Default is `"localhost"`. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_instance_id: App Instance ID.
         :param pulumi.Input[str] provider_shared_secret: An authentication key that must be defined when the RADIUS server is configured, and must be the same on both the RADIUS client and server. Used only for authenticators with type `"security_key"`.
         :param pulumi.Input[str] provider_type: The type of Authenticator. Values include: `"password"`, `"security_question"`, `"phone"`, `"email"`, `"app"`, `"federated"`, and `"security_key"`.
         :param pulumi.Input[str] provider_user_name_template: Username template expected by the provider. Used only for authenticators with type `"security_key"`.
@@ -523,15 +523,15 @@
         __props__.__dict__["type"] = type
         return Authenticator(resource_name, opts=opts, __props__=__props__)
 
     @property
     @pulumi.getter
     def key(self) -> pulumi.Output[str]:
         """
-        A human-readable string that identifies the authenticator. Possible values inclue: `"duo"`, `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, `"webauthn"`, and `"yubikey_token"`.
+        A human-readable string that identifies the authenticator. Possible values inclue: `"external_idp"`, `"google_otp"`, `"okta_email"`, `"okta_password"`, `"okta_verify"`, `"onprem_mfa"`, `"phone_number"`, `"rsa_token"`, `"security_question"`, and `"webauthn"`.
         """
         return pulumi.get(self, "key")
 
     @property
     @pulumi.getter
     def name(self) -> pulumi.Output[str]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/behaviour.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/behaviour.py`

 * *Files identical despite different names*

```diff
@@ -316,15 +316,15 @@
         ```
 
         ## Import
 
         Behavior can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/behaviour:Behaviour example <behavior id>
+         $ pulumi import okta:index/behaviour:Behaviour example &#60;behavior id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] location_granularity_type: Determines the method and level of detail used to evaluate the behavior.
                Required for `"ANOMALOUS_LOCATION"` behavior type. Can be set to `"LAT_LONG"`, `"CITY"`, `"COUNTRY"`
                or `"SUBDIVISION"`.
@@ -375,15 +375,15 @@
         ```
 
         ## Import
 
         Behavior can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/behaviour:Behaviour example <behavior id>
+         $ pulumi import okta:index/behaviour:Behaviour example &#60;behavior id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param BehaviourArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/captcha.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/captcha.py`

 * *Files 1% similar despite different names*

```diff
@@ -179,15 +179,15 @@
         ```
 
         ## Import
 
         Behavior can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/captcha:Captcha example <captcha id>
+         $ pulumi import okta:index/captcha:Captcha example &#60;captcha id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] name: Name of the captcha.
         :param pulumi.Input[str] secret_key: Secret key issued from the CAPTCHA vendor to perform server-side validation for a CAPTCHA token.
         :param pulumi.Input[str] site_key: Site key issued from the CAPTCHA vendor to render a CAPTCHA on a page.
@@ -217,15 +217,15 @@
         ```
 
         ## Import
 
         Behavior can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/captcha:Captcha example <captcha id>
+         $ pulumi import okta:index/captcha:Captcha example &#60;captcha id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param CaptchaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/captcha_org_wide_settings.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/captcha_org_wide_settings.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/config/vars.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/config/vars.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/auth_login_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/auth_login_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/bookmark_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/bookmark_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/get_default_policies.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/get_default_policies.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/idp.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/idp.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/mfa_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/mfa_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/mfa_policy_rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/mfa_policy_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/oauth_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/oauth_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/oauth_app_redirect_uri.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/oauth_app_redirect_uri.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/password_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/password_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/password_policy_rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/password_policy_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_idp.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_idp.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/saml_idp_signing_key.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/saml_idp_signing_key.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/secure_password_store_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/secure_password_store_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/signon_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/signon_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/signon_policy_rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/signon_policy_rule.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/social_idp.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/social_idp.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/swa_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/swa_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/deprecated/three_field_app.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/deprecated/three_field_app.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/domain.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/domain.py`

 * *Files 0% similar despite different names*

```diff
@@ -188,15 +188,15 @@
         ```
 
         ## Import
 
         Okta Admin Role Targets can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/domain:Domain example <domain_id>
+         $ pulumi import okta:index/domain:Domain example &#60;domain_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] certificate_source_type: Certificate source type that indicates whether the certificate is provided by the user or Okta. Accepted values: `MANUAL`, `OKTA_MANAGED`. Default value = `MANUAL`
         :param pulumi.Input[str] name: Custom Domain name.
         :param pulumi.Input[bool] verify: Indicates whether the domain should be verified.
@@ -221,15 +221,15 @@
         ```
 
         ## Import
 
         Okta Admin Role Targets can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/domain:Domain example <domain_id>
+         $ pulumi import okta:index/domain:Domain example &#60;domain_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param DomainArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/domain_certificate.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/domain_certificate.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/domain_verification.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/domain_verification.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/email_sender.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/email_sender.py`

 * *Files 2% similar despite different names*

```diff
@@ -178,15 +178,15 @@
         ```
 
         ## Import
 
         Custom email sender can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/emailSender:EmailSender example <sender id>
+         $ pulumi import okta:index/emailSender:EmailSender example &#60;sender id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] from_address: Email address to send from.
         :param pulumi.Input[str] from_name: Name of sender.
         :param pulumi.Input[str] subdomain: Mail domain to send from.
@@ -213,15 +213,15 @@
         ```
 
         ## Import
 
         Custom email sender can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/emailSender:EmailSender example <sender id>
+         $ pulumi import okta:index/emailSender:EmailSender example &#60;sender id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param EmailSenderArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/email_sender_verification.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/email_sender_verification.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/event_hook.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/event_hook.py`

 * *Files 1% similar despite different names*

```diff
@@ -251,15 +251,15 @@
         ```
 
         ## Import
 
         An event hook can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/eventHook:EventHook example <hook id>
+         $ pulumi import okta:index/eventHook:EventHook example &#60;hook id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] auth: Authentication required for event hook request.
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] channel: Details of the endpoint the event hook will hit.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] events: The events that will be delivered to this hook. [See here for a list of supported events](https://developer.okta.com/docs/reference/api/event-types/?q=event-hook-eligible).
@@ -301,15 +301,15 @@
         ```
 
         ## Import
 
         An event hook can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/eventHook:EventHook example <hook id>
+         $ pulumi import okta:index/eventHook:EventHook example &#60;hook id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param EventHookArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/event_hook_verification.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/event_hook_verification.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/factor/factor.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/factor/factor.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/factor_totp.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/factor_totp.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_group_assignments.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_group_assignments.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_signon_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_signon_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_app_user_assignments.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_app_user_assignments.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_auth_server_claim.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_auth_server_claim.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_auth_server_claims.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_auth_server_claims.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_authenticator.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_authenticator.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_behaviour.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_behaviour.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_behaviours.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_behaviours.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_groups.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_groups.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_network_zone.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_network_zone.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_role_subscription.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_role_subscription.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_trusted_origins.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_trusted_origins.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/get_user_security_questions.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/get_user_security_questions.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/get_everyone_group.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/get_everyone_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/get_group.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/get_group.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/group.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/group.py`

 * *Files 1% similar despite different names*

```diff
@@ -247,21 +247,21 @@
         ```
 
         ## Import
 
         An Okta Group can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:group/group:Group example <group id>
+         $ pulumi import okta:group/group:Group example &#60;group id&#62;
         ```
 
          It's also possible to import group without users. In this case ID will look like this
 
         ```sh
-         $ pulumi import okta:group/group:Group example <group id>/skip_users
+         $ pulumi import okta:group/group:Group example &#60;group id&#62;/skip_users
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] custom_profile_attributes: raw JSON containing all custom profile attributes.
         :param pulumi.Input[str] description: The description of the Okta Group.
         :param pulumi.Input[str] name: The name of the Okta Group.
@@ -315,21 +315,21 @@
         ```
 
         ## Import
 
         An Okta Group can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:group/group:Group example <group id>
+         $ pulumi import okta:group/group:Group example &#60;group id&#62;
         ```
 
          It's also possible to import group without users. In this case ID will look like this
 
         ```sh
-         $ pulumi import okta:group/group:Group example <group id>/skip_users
+         $ pulumi import okta:group/group:Group example &#60;group id&#62;/skip_users
         ```
 
         :param str resource_name: The name of the resource.
         :param GroupArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/membership.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/membership.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/role.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/role.py`

 * *Files 1% similar despite different names*

```diff
@@ -241,15 +241,15 @@
         ```
 
         ## Import
 
         Individual admin role assignment can be imported by passing the group and role assignment IDs as follows
 
         ```sh
-         $ pulumi import okta:group/role:Role example <group id>/<role id>
+         $ pulumi import okta:group/role:Role example &#60;group id&#62;/&#60;role id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] disable_notifications: When this setting is enabled, the admins won't receive any of the default Okta
                administrator emails. These admins also won't have access to contact Okta Support and open support cases on behalf of your org.
         :param pulumi.Input[str] group_id: The ID of group to attach admin roles to.
@@ -287,15 +287,15 @@
         ```
 
         ## Import
 
         Individual admin role assignment can be imported by passing the group and role assignment IDs as follows
 
         ```sh
-         $ pulumi import okta:group/role:Role example <group id>/<role id>
+         $ pulumi import okta:group/role:Role example &#60;group id&#62;/&#60;role id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RoleArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/roles.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/roles.py`

 * *Files 1% similar despite different names*

```diff
@@ -114,15 +114,15 @@
         ```
 
         ## Import
 
         Group Role Assignment can be imported via the Okta Group ID.
 
         ```sh
-         $ pulumi import okta:group/roles:Roles example <group id>
+         $ pulumi import okta:group/roles:Roles example &#60;group id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] admin_roles: Admin roles associated with the group. It can be any of the following values `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"APP_ADMIN"`, `"USER_ADMIN"`, `"HELP_DESK_ADMIN"`, `"READ_ONLY_ADMIN"`, `"MOBILE_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`, `"REPORT_ADMIN"`, `"GROUP_MEMBERSHIP_ADMIN"`.
         :param pulumi.Input[str] group_id: The ID of group to attach admin roles to.
         """
@@ -149,15 +149,15 @@
         ```
 
         ## Import
 
         Group Role Assignment can be imported via the Okta Group ID.
 
         ```sh
-         $ pulumi import okta:group/roles:Roles example <group id>
+         $ pulumi import okta:group/roles:Roles example &#60;group id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RolesArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group/rule.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group/rule.py`

 * *Files 5% similar despite different names*

```diff
@@ -22,15 +22,15 @@
                  users_excludeds: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]] = None):
         """
         The set of arguments for constructing a Rule resource.
         :param pulumi.Input[str] expression_value: The expression value.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] group_assignments: The list of group ids to assign the users to.
         :param pulumi.Input[str] expression_type: The expression type to use to invoke the rule. The default
                is `"urn:okta:expression:1.0"`.
-        :param pulumi.Input[str] name: The name of the Group Rule.
+        :param pulumi.Input[str] name: The name of the Group Rule (min character 1; max characters 50).
         :param pulumi.Input[bool] remove_assigned_users: This tells the provider to remove users added by this rule from the assigned
                group after destroying this resource. Default is `false`.
         :param pulumi.Input[str] status: The status of the group rule.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] users_excludeds: The list of user IDs that would be excluded when rules are processed.
         """
         pulumi.set(__self__, "expression_value", expression_value)
         pulumi.set(__self__, "group_assignments", group_assignments)
@@ -82,15 +82,15 @@
     def expression_type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "expression_type", value)
 
     @property
     @pulumi.getter
     def name(self) -> Optional[pulumi.Input[str]]:
         """
-        The name of the Group Rule.
+        The name of the Group Rule (min character 1; max characters 50).
         """
         return pulumi.get(self, "name")
 
     @name.setter
     def name(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "name", value)
 
@@ -144,15 +144,15 @@
                  users_excludeds: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]] = None):
         """
         Input properties used for looking up and filtering Rule resources.
         :param pulumi.Input[str] expression_type: The expression type to use to invoke the rule. The default
                is `"urn:okta:expression:1.0"`.
         :param pulumi.Input[str] expression_value: The expression value.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] group_assignments: The list of group ids to assign the users to.
-        :param pulumi.Input[str] name: The name of the Group Rule.
+        :param pulumi.Input[str] name: The name of the Group Rule (min character 1; max characters 50).
         :param pulumi.Input[bool] remove_assigned_users: This tells the provider to remove users added by this rule from the assigned
                group after destroying this resource. Default is `false`.
         :param pulumi.Input[str] status: The status of the group rule.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] users_excludeds: The list of user IDs that would be excluded when rules are processed.
         """
         if expression_type is not None:
             pulumi.set(__self__, "expression_type", expression_type)
@@ -206,15 +206,15 @@
     def group_assignments(self, value: Optional[pulumi.Input[Sequence[pulumi.Input[str]]]]):
         pulumi.set(self, "group_assignments", value)
 
     @property
     @pulumi.getter
     def name(self) -> Optional[pulumi.Input[str]]:
         """
-        The name of the Group Rule.
+        The name of the Group Rule (min character 1; max characters 50).
         """
         return pulumi.get(self, "name")
 
     @name.setter
     def name(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "name", value)
 
@@ -288,24 +288,24 @@
         ```
 
         ## Import
 
         An Okta Group Rule can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:group/rule:Rule example <group rule id>
+         $ pulumi import okta:group/rule:Rule example &#60;group rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] expression_type: The expression type to use to invoke the rule. The default
                is `"urn:okta:expression:1.0"`.
         :param pulumi.Input[str] expression_value: The expression value.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] group_assignments: The list of group ids to assign the users to.
-        :param pulumi.Input[str] name: The name of the Group Rule.
+        :param pulumi.Input[str] name: The name of the Group Rule (min character 1; max characters 50).
         :param pulumi.Input[bool] remove_assigned_users: This tells the provider to remove users added by this rule from the assigned
                group after destroying this resource. Default is `false`.
         :param pulumi.Input[str] status: The status of the group rule.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] users_excludeds: The list of user IDs that would be excluded when rules are processed.
         """
         ...
     @overload
@@ -332,15 +332,15 @@
         ```
 
         ## Import
 
         An Okta Group Rule can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:group/rule:Rule example <group rule id>
+         $ pulumi import okta:group/rule:Rule example &#60;group rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RuleArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -408,15 +408,15 @@
         :param str resource_name: The unique name of the resulting resource.
         :param pulumi.Input[str] id: The unique provider ID of the resource to lookup.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] expression_type: The expression type to use to invoke the rule. The default
                is `"urn:okta:expression:1.0"`.
         :param pulumi.Input[str] expression_value: The expression value.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] group_assignments: The list of group ids to assign the users to.
-        :param pulumi.Input[str] name: The name of the Group Rule.
+        :param pulumi.Input[str] name: The name of the Group Rule (min character 1; max characters 50).
         :param pulumi.Input[bool] remove_assigned_users: This tells the provider to remove users added by this rule from the assigned
                group after destroying this resource. Default is `false`.
         :param pulumi.Input[str] status: The status of the group rule.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] users_excludeds: The list of user IDs that would be excluded when rules are processed.
         """
         opts = pulumi.ResourceOptions.merge(opts, pulumi.ResourceOptions(id=id))
 
@@ -456,15 +456,15 @@
         """
         return pulumi.get(self, "group_assignments")
 
     @property
     @pulumi.getter
     def name(self) -> pulumi.Output[str]:
         """
-        The name of the Group Rule.
+        The name of the Group Rule (min character 1; max characters 50).
         """
         return pulumi.get(self, "name")
 
     @property
     @pulumi.getter(name="removeAssignedUsers")
     def remove_assigned_users(self) -> pulumi.Output[Optional[bool]]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group_memberships.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group_memberships.py`

 * *Files 3% similar despite different names*

```diff
@@ -114,14 +114,22 @@
             group_id=test_group.id,
             users=[
                 okta_user["test1"]["id"],
                 okta_user["test2"]["id"],
             ])
         ```
 
+        ## Import
+
+        an Okta Group's memberships can be imported via the Okta group ID.
+
+        ```sh
+         $ pulumi import okta:index/groupMemberships:GroupMemberships test &#60;group id&#62;
+        ```
+
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] group_id: Okta group ID.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] users: The list of Okta user IDs which the group should have membership managed for.
         """
         ...
     @overload
@@ -147,14 +155,22 @@
             group_id=test_group.id,
             users=[
                 okta_user["test1"]["id"],
                 okta_user["test2"]["id"],
             ])
         ```
 
+        ## Import
+
+        an Okta Group's memberships can be imported via the Okta group ID.
+
+        ```sh
+         $ pulumi import okta:index/groupMemberships:GroupMemberships test &#60;group id&#62;
+        ```
+
         :param str resource_name: The name of the resource.
         :param GroupMembershipsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
     def __init__(__self__, resource_name: str, *args, **kwargs):
         resource_args, opts = _utilities.get_resource_args_opts(GroupMembershipsArgs, pulumi.ResourceOptions, *args, **kwargs)
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/group_schema_property.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/group_schema_property.py`

 * *Files 0% similar despite different names*

```diff
@@ -679,15 +679,15 @@
         ```
 
         ## Import
 
         Group schema property can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/groupSchemaProperty:GroupSchemaProperty example <index>
+         $ pulumi import okta:index/groupSchemaProperty:GroupSchemaProperty example &#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] array_enums: Array of values that an array property's items can be set to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['GroupSchemaPropertyArrayOneOfArgs']]]] array_one_ofs: Display name and value an enum array can be set to.
         :param pulumi.Input[str] array_type: The type of the array elements if `type` is set to `"array"`.
@@ -735,15 +735,15 @@
         ```
 
         ## Import
 
         Group schema property can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/groupSchemaProperty:GroupSchemaProperty example <index>
+         $ pulumi import okta:index/groupSchemaProperty:GroupSchemaProperty example &#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param GroupSchemaPropertyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_metadata_saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_metadata_saml.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_oidc.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_oidc.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_saml.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/get_social.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/get_social.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/oidc.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/oidc.py`

 * *Files 0% similar despite different names*

```diff
@@ -1196,15 +1196,15 @@
         ```
 
         ## Import
 
         An OIDC IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/oidc:Oidc example <idp id>
+         $ pulumi import okta:idp/oidc:Oidc example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] account_link_action: Specifies the account linking action for an IdP user.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] account_link_group_includes: Group memberships to determine link candidates.
         :param pulumi.Input[str] authorization_binding: The method of making an authorization request. It can be set to `"HTTP-POST"` or `"HTTP-REDIRECT"`.
@@ -1273,15 +1273,15 @@
         ```
 
         ## Import
 
         An OIDC IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/oidc:Oidc example <idp id>
+         $ pulumi import okta:idp/oidc:Oidc example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param OidcArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/saml.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/saml.py`

 * *Files 0% similar despite different names*

```diff
@@ -1122,15 +1122,15 @@
         ```
 
         ## Import
 
         An SAML IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/saml:Saml example <idp id>
+         $ pulumi import okta:idp/saml:Saml example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] account_link_action: Specifies the account linking action for an IdP user.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] account_link_group_includes: Group memberships to determine link candidates.
         :param pulumi.Input[str] acs_type: The type of ACS. It can be `"INSTANCE"` or `"ORG"`.
@@ -1192,15 +1192,15 @@
         ```
 
         ## Import
 
         An SAML IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/saml:Saml example <idp id>
+         $ pulumi import okta:idp/saml:Saml example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param SamlArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/saml_key.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/saml_key.py`

 * *Files 0% similar despite different names*

```diff
@@ -162,15 +162,15 @@
                  __props__=None):
         """
         ## Import
 
         A SAML IdP Signing Key can be imported via the key id.
 
         ```sh
-         $ pulumi import okta:idp/samlKey:SamlKey example <key id>
+         $ pulumi import okta:idp/samlKey:SamlKey example &#60;key id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] x5cs: base64-encoded X.509 certificate chain with DER encoding.
         """
         ...
@@ -181,15 +181,15 @@
                  opts: Optional[pulumi.ResourceOptions] = None):
         """
         ## Import
 
         A SAML IdP Signing Key can be imported via the key id.
 
         ```sh
-         $ pulumi import okta:idp/samlKey:SamlKey example <key id>
+         $ pulumi import okta:idp/samlKey:SamlKey example &#60;key id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param SamlKeyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/idp/social.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/idp/social.py`

 * *Files 0% similar despite different names*

```diff
@@ -1147,15 +1147,15 @@
         ```
 
         ## Import
 
         A Social IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/social:Social example <idp id>
+         $ pulumi import okta:idp/social:Social example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] account_link_action: Specifies the account linking action for an IdP user.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] account_link_group_includes: Group memberships to determine link candidates.
         :param pulumi.Input[str] apple_kid: The Key ID that you obtained from Apple when you created the private key for the client.
@@ -1220,15 +1220,15 @@
         ```
 
         ## Import
 
         A Social IdP can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:idp/social:Social example <idp id>
+         $ pulumi import okta:idp/social:Social example &#60;idp id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param SocialArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/hook.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/hook.py`

 * *Files 2% similar despite different names*

```diff
@@ -281,15 +281,15 @@
         ```
 
         ## Import
 
         An inline hook can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:inline/hook:Hook example <hook id>
+         $ pulumi import okta:inline/hook:Hook example &#60;hook id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] auth: Authentication required for inline hook request.
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] channel: Details of the endpoint the inline hook will hit.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['HookHeaderArgs']]]] headers: Map of headers to send along in inline hook request.
@@ -330,15 +330,15 @@
         ```
 
         ## Import
 
         An inline hook can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:inline/hook:Hook example <hook id>
+         $ pulumi import okta:inline/hook:Hook example &#60;hook id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param HookArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/inline/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/inline/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/link_definition.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/link_definition.py`

 * *Files 0% similar despite different names*

```diff
@@ -246,15 +246,15 @@
         ```
 
         ## Import
 
         Okta Link Definition can be imported via the Okta Primary Link Name.
 
         ```sh
-         $ pulumi import okta:index/linkDefinition:LinkDefinition example <primary_name>
+         $ pulumi import okta:index/linkDefinition:LinkDefinition example &#60;primary_name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] associated_description: Description of the associated relationship.
         :param pulumi.Input[str] associated_name: API name of the associated link.
         :param pulumi.Input[str] associated_title: Display name of the associated link.
@@ -290,15 +290,15 @@
         ```
 
         ## Import
 
         Okta Link Definition can be imported via the Okta Primary Link Name.
 
         ```sh
-         $ pulumi import okta:index/linkDefinition:LinkDefinition example <primary_name>
+         $ pulumi import okta:index/linkDefinition:LinkDefinition example &#60;primary_name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param LinkDefinitionArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/link_value.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/link_value.py`

 * *Files 1% similar despite different names*

```diff
@@ -170,15 +170,15 @@
         ```
 
         ## Import
 
         Okta Link Value can be imported via Primary Name and Primary User ID.
 
         ```sh
-         $ pulumi import okta:index/linkValue:LinkValue example <primary_name>/<primary_user_id>
+         $ pulumi import okta:index/linkValue:LinkValue example &#60;primary_name&#62;/&#60;primary_user_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] associated_user_ids: Set of User IDs or login values of the users to be assigned the 'associated' relationship.
         :param pulumi.Input[str] primary_name: Name of the `primary` relationship being assigned.
         :param pulumi.Input[str] primary_user_id: User ID to be assigned to `primary` for the `associated` user in the specified relationship.
@@ -230,15 +230,15 @@
         ```
 
         ## Import
 
         Okta Link Value can be imported via Primary Name and Primary User ID.
 
         ```sh
-         $ pulumi import okta:index/linkValue:LinkValue example <primary_name>/<primary_user_id>
+         $ pulumi import okta:index/linkValue:LinkValue example &#60;primary_name&#62;/&#60;primary_user_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param LinkValueArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/network/zone.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/network/zone.py`

 * *Files 1% similar despite different names*

```diff
@@ -334,15 +334,15 @@
         ```
 
         ## Import
 
         Okta Network Zone can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:network/zone:Zone example <zone id>
+         $ pulumi import okta:network/zone:Zone example &#60;zone id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] asns: Array of Autonomous System Numbers (each element is a string representation of an ASN numeric value).
         :param pulumi.Input[Sequence[pulumi.Input[str]]] dynamic_locations: Array of locations [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
                and [ISO-3166-2](https://en.wikipedia.org/wiki/ISO_3166-2). Format code: countryCode OR countryCode-regionCode.
@@ -394,15 +394,15 @@
         ```
 
         ## Import
 
         Okta Network Zone can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:network/zone:Zone example <zone id>
+         $ pulumi import okta:network/zone:Zone example &#60;zone id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ZoneArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/org_configuration.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/org_configuration.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/org_support.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/org_support.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/outputs.py`

 * *Files 16% similar despite different names*

```diff
@@ -23,15 +23,19 @@
     'PolicyRuleProfileEnrollmentProfileAttribute',
     'TemplateSmsTranslation',
     'UserSchemaPropertyArrayOneOf',
     'UserSchemaPropertyMasterOverridePriority',
     'UserSchemaPropertyOneOf',
     'GetAuthServerClaimsClaimResult',
     'GetBehavioursBehaviorResult',
+    'GetBrandsBrandResult',
+    'GetEmailCustomizationsEmailCustomizationResult',
     'GetGroupsGroupResult',
+    'GetTemplatesEmailTemplateResult',
+    'GetThemesThemeResult',
     'GetTrustedOriginsTrustedOriginResult',
     'GetUserSecurityQuestionsQuestionResult',
 ]
 
 @pulumi.output_type
 class AppGroupAssignmentsGroup(dict):
     def __init__(__self__, *,
@@ -799,33 +803,124 @@
         """
         Behavior type.
         """
         return pulumi.get(self, "type")
 
 
 @pulumi.output_type
+class GetBrandsBrandResult(dict):
+    def __init__(__self__, *,
+                 custom_privacy_policy_url: str,
+                 id: str,
+                 links: str,
+                 remove_powered_by_okta: bool):
+        pulumi.set(__self__, "custom_privacy_policy_url", custom_privacy_policy_url)
+        pulumi.set(__self__, "id", id)
+        pulumi.set(__self__, "links", links)
+        pulumi.set(__self__, "remove_powered_by_okta", remove_powered_by_okta)
+
+    @property
+    @pulumi.getter(name="customPrivacyPolicyUrl")
+    def custom_privacy_policy_url(self) -> str:
+        return pulumi.get(self, "custom_privacy_policy_url")
+
+    @property
+    @pulumi.getter
+    def id(self) -> str:
+        return pulumi.get(self, "id")
+
+    @property
+    @pulumi.getter
+    def links(self) -> str:
+        return pulumi.get(self, "links")
+
+    @property
+    @pulumi.getter(name="removePoweredByOkta")
+    def remove_powered_by_okta(self) -> bool:
+        return pulumi.get(self, "remove_powered_by_okta")
+
+
+@pulumi.output_type
+class GetEmailCustomizationsEmailCustomizationResult(dict):
+    def __init__(__self__, *,
+                 body: str,
+                 id: str,
+                 is_default: bool,
+                 language: str,
+                 links: str,
+                 subject: str):
+        pulumi.set(__self__, "body", body)
+        pulumi.set(__self__, "id", id)
+        pulumi.set(__self__, "is_default", is_default)
+        pulumi.set(__self__, "language", language)
+        pulumi.set(__self__, "links", links)
+        pulumi.set(__self__, "subject", subject)
+
+    @property
+    @pulumi.getter
+    def body(self) -> str:
+        return pulumi.get(self, "body")
+
+    @property
+    @pulumi.getter
+    def id(self) -> str:
+        return pulumi.get(self, "id")
+
+    @property
+    @pulumi.getter(name="isDefault")
+    def is_default(self) -> bool:
+        return pulumi.get(self, "is_default")
+
+    @property
+    @pulumi.getter
+    def language(self) -> str:
+        return pulumi.get(self, "language")
+
+    @property
+    @pulumi.getter
+    def links(self) -> str:
+        return pulumi.get(self, "links")
+
+    @property
+    @pulumi.getter
+    def subject(self) -> str:
+        return pulumi.get(self, "subject")
+
+
+@pulumi.output_type
 class GetGroupsGroupResult(dict):
     def __init__(__self__, *,
+                 custom_profile_attributes: str,
                  description: str,
                  id: str,
                  name: str,
                  type: str):
         """
+        :param str custom_profile_attributes: raw JSON containing all custom profile attributes. Likely only useful on groups of type `APP_GROUP`.
         :param str description: Group description.
         :param str id: Group ID.
         :param str name: Group name.
         :param str type: type of the group to retrieve. Can only be one of `OKTA_GROUP` (Native Okta Groups), `APP_GROUP`
                (Imported App Groups), or `BUILT_IN` (Okta System Groups).
         """
+        pulumi.set(__self__, "custom_profile_attributes", custom_profile_attributes)
         pulumi.set(__self__, "description", description)
         pulumi.set(__self__, "id", id)
         pulumi.set(__self__, "name", name)
         pulumi.set(__self__, "type", type)
 
     @property
+    @pulumi.getter(name="customProfileAttributes")
+    def custom_profile_attributes(self) -> str:
+        """
+        raw JSON containing all custom profile attributes. Likely only useful on groups of type `APP_GROUP`.
+        """
+        return pulumi.get(self, "custom_profile_attributes")
+
+    @property
     @pulumi.getter
     def description(self) -> str:
         """
         Group description.
         """
         return pulumi.get(self, "description")
 
@@ -852,14 +947,129 @@
         type of the group to retrieve. Can only be one of `OKTA_GROUP` (Native Okta Groups), `APP_GROUP`
         (Imported App Groups), or `BUILT_IN` (Okta System Groups).
         """
         return pulumi.get(self, "type")
 
 
 @pulumi.output_type
+class GetTemplatesEmailTemplateResult(dict):
+    def __init__(__self__, *,
+                 links: str,
+                 name: str):
+        pulumi.set(__self__, "links", links)
+        pulumi.set(__self__, "name", name)
+
+    @property
+    @pulumi.getter
+    def links(self) -> str:
+        return pulumi.get(self, "links")
+
+    @property
+    @pulumi.getter
+    def name(self) -> str:
+        return pulumi.get(self, "name")
+
+
+@pulumi.output_type
+class GetThemesThemeResult(dict):
+    def __init__(__self__, *,
+                 background_image_url: str,
+                 email_template_touch_point_variant: str,
+                 end_user_dashboard_touch_point_variant: str,
+                 error_page_touch_point_variant: str,
+                 favicon_url: str,
+                 id: str,
+                 links: str,
+                 logo_url: str,
+                 primary_color_contrast_hex: str,
+                 primary_color_hex: str,
+                 secondary_color_contrast_hex: str,
+                 secondary_color_hex: str,
+                 sign_in_page_touch_point_variant: str):
+        pulumi.set(__self__, "background_image_url", background_image_url)
+        pulumi.set(__self__, "email_template_touch_point_variant", email_template_touch_point_variant)
+        pulumi.set(__self__, "end_user_dashboard_touch_point_variant", end_user_dashboard_touch_point_variant)
+        pulumi.set(__self__, "error_page_touch_point_variant", error_page_touch_point_variant)
+        pulumi.set(__self__, "favicon_url", favicon_url)
+        pulumi.set(__self__, "id", id)
+        pulumi.set(__self__, "links", links)
+        pulumi.set(__self__, "logo_url", logo_url)
+        pulumi.set(__self__, "primary_color_contrast_hex", primary_color_contrast_hex)
+        pulumi.set(__self__, "primary_color_hex", primary_color_hex)
+        pulumi.set(__self__, "secondary_color_contrast_hex", secondary_color_contrast_hex)
+        pulumi.set(__self__, "secondary_color_hex", secondary_color_hex)
+        pulumi.set(__self__, "sign_in_page_touch_point_variant", sign_in_page_touch_point_variant)
+
+    @property
+    @pulumi.getter(name="backgroundImageUrl")
+    def background_image_url(self) -> str:
+        return pulumi.get(self, "background_image_url")
+
+    @property
+    @pulumi.getter(name="emailTemplateTouchPointVariant")
+    def email_template_touch_point_variant(self) -> str:
+        return pulumi.get(self, "email_template_touch_point_variant")
+
+    @property
+    @pulumi.getter(name="endUserDashboardTouchPointVariant")
+    def end_user_dashboard_touch_point_variant(self) -> str:
+        return pulumi.get(self, "end_user_dashboard_touch_point_variant")
+
+    @property
+    @pulumi.getter(name="errorPageTouchPointVariant")
+    def error_page_touch_point_variant(self) -> str:
+        return pulumi.get(self, "error_page_touch_point_variant")
+
+    @property
+    @pulumi.getter(name="faviconUrl")
+    def favicon_url(self) -> str:
+        return pulumi.get(self, "favicon_url")
+
+    @property
+    @pulumi.getter
+    def id(self) -> str:
+        return pulumi.get(self, "id")
+
+    @property
+    @pulumi.getter
+    def links(self) -> str:
+        return pulumi.get(self, "links")
+
+    @property
+    @pulumi.getter(name="logoUrl")
+    def logo_url(self) -> str:
+        return pulumi.get(self, "logo_url")
+
+    @property
+    @pulumi.getter(name="primaryColorContrastHex")
+    def primary_color_contrast_hex(self) -> str:
+        return pulumi.get(self, "primary_color_contrast_hex")
+
+    @property
+    @pulumi.getter(name="primaryColorHex")
+    def primary_color_hex(self) -> str:
+        return pulumi.get(self, "primary_color_hex")
+
+    @property
+    @pulumi.getter(name="secondaryColorContrastHex")
+    def secondary_color_contrast_hex(self) -> str:
+        return pulumi.get(self, "secondary_color_contrast_hex")
+
+    @property
+    @pulumi.getter(name="secondaryColorHex")
+    def secondary_color_hex(self) -> str:
+        return pulumi.get(self, "secondary_color_hex")
+
+    @property
+    @pulumi.getter(name="signInPageTouchPointVariant")
+    def sign_in_page_touch_point_variant(self) -> str:
+        return pulumi.get(self, "sign_in_page_touch_point_variant")
+
+
+@pulumi.output_type
 class GetTrustedOriginsTrustedOriginResult(dict):
     def __init__(__self__, *,
                  active: bool,
                  id: str,
                  name: str,
                  origin: str,
                  scopes: Sequence[str]):
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/get_default_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/get_default_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/get_policy.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/get_policy.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/mfa.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/mfa.py`

 * *Files 0% similar despite different names*

```diff
@@ -957,15 +957,15 @@
         ```
 
         ## Import
 
         An MFA Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/mfa:Mfa example <policy id>
+         $ pulumi import okta:policy/mfa:Mfa example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] description: Policy Description.
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] duo: DUO MFA policy settings (✓ Classic, ✓ OIE).
         :param pulumi.Input[Mapping[str, pulumi.Input[str]]] external_idp: External IDP MFA policy settings (✓ OIE).
@@ -1031,15 +1031,15 @@
         ```
 
         ## Import
 
         An MFA Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/mfa:Mfa example <policy id>
+         $ pulumi import okta:policy/mfa:Mfa example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param MfaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/password.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/password.py`

 * *Files 0% similar despite different names*

```diff
@@ -1041,15 +1041,15 @@
         ```
 
         ## Import
 
         A Password Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/password:Password example <policy id>
+         $ pulumi import okta:policy/password:Password example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] auth_provider: Authentication Provider: `"OKTA"`, `"ACTIVE_DIRECTORY"` or `"LDAP"`. Default is `"OKTA"`.
         :param pulumi.Input[str] call_recovery: Enable or disable voice call password recovery: ACTIVE or INACTIVE.
         :param pulumi.Input[str] description: Policy Description.
@@ -1106,15 +1106,15 @@
         ```
 
         ## Import
 
         A Password Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/password:Password example <policy id>
+         $ pulumi import okta:policy/password:Password example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param PasswordArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_idp_discovery.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_idp_discovery.py`

 * *Files 1% similar despite different names*

```diff
@@ -611,15 +611,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleIdpDiscovery:RuleIdpDiscovery example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleIdpDiscovery:RuleIdpDiscovery example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['RuleIdpDiscoveryAppExcludeArgs']]]] app_excludes: Applications to exclude in discovery. See `app_include` for details.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['RuleIdpDiscoveryAppIncludeArgs']]]] app_includes: Applications to include in discovery rule.
         :param pulumi.Input[str] idp_id: The identifier for the Idp the rule should route to if all conditions are met.
@@ -693,15 +693,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleIdpDiscovery:RuleIdpDiscovery example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleIdpDiscovery:RuleIdpDiscovery example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RuleIdpDiscoveryArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_mfa.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_mfa.py`

 * *Files 0% similar despite different names*

```diff
@@ -550,15 +550,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleMfa:RuleMfa example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleMfa:RuleMfa example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['RuleMfaAppExcludeArgs']]]] app_excludes: Applications to exclude
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['RuleMfaAppIncludeArgs']]]] app_includes: Applications to include in discovery rule. **IMPORTANT**: this field is only available in Classic Organizations.
         :param pulumi.Input[str] enroll: When a user should be prompted for MFA. It can be `"CHALLENGE"`, `"LOGIN"`, or `"NEVER"`.
@@ -692,15 +692,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleMfa:RuleMfa example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleMfa:RuleMfa example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RuleMfaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_password.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_password.py`

 * *Files 0% similar despite different names*

```diff
@@ -440,15 +440,15 @@
         This resource allows you to create and configure a Password Policy Rule.
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/rulePassword:RulePassword example <policy id>/<rule id>
+         $ pulumi import okta:policy/rulePassword:RulePassword example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] name: Policy Rule Name.
         :param pulumi.Input[str] network_connection: Network selection mode: `"ANYWHERE"`, `"ZONE"`, `"ON_NETWORK"`, or `"OFF_NETWORK"`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] network_excludes: The network zones to exclude. Conflicts with `network_includes`.
@@ -474,15 +474,15 @@
         This resource allows you to create and configure a Password Policy Rule.
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/rulePassword:RulePassword example <policy id>/<rule id>
+         $ pulumi import okta:policy/rulePassword:RulePassword example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RulePasswordArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/rule_signon.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/rule_signon.py`

 * *Files 1% similar despite different names*

```diff
@@ -921,15 +921,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleSignon:RuleSignon example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleSignon:RuleSignon example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] access: Allow or deny access based on the rule conditions: `"ALLOW"`, `"DENY"` or `"CHALLENGE"`. The default is `"ALLOW"`.
         :param pulumi.Input[str] authtype: Authentication entrypoint: `"ANY"`, `"LDAP_INTERFACE"` or `"RADIUS"`.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] behaviors: List of behavior IDs.
@@ -1044,15 +1044,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:policy/ruleSignon:RuleSignon example <policy id>/<rule id>
+         $ pulumi import okta:policy/ruleSignon:RuleSignon example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RuleSignonArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy/signon.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy/signon.py`

 * *Files 2% similar despite different names*

```diff
@@ -215,15 +215,15 @@
         ```
 
         ## Import
 
         A Sign On Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/signon:Signon example <policy id>
+         $ pulumi import okta:policy/signon:Signon example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] description: Policy Description.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] groups_includeds: List of Group IDs to Include.
         :param pulumi.Input[str] name: Policy Name.
@@ -254,15 +254,15 @@
         ```
 
         ## Import
 
         A Sign On Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:policy/signon:Signon example <policy id>
+         $ pulumi import okta:policy/signon:Signon example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param SignonArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_mfa_default.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_mfa_default.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_password_default.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_password_default.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_profile_enrollment.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_profile_enrollment.py`

 * *Files 0% similar despite different names*

```diff
@@ -113,15 +113,15 @@
         ```
 
         ## Import
 
         A Profile Enrollment Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/policyProfileEnrollment:PolicyProfileEnrollment example <policy id>
+         $ pulumi import okta:index/policyProfileEnrollment:PolicyProfileEnrollment example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] name: Policy Name.
         :param pulumi.Input[str] status: Status of the policy.
         """
@@ -146,15 +146,15 @@
         ```
 
         ## Import
 
         A Profile Enrollment Policy can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/policyProfileEnrollment:PolicyProfileEnrollment example <policy id>
+         $ pulumi import okta:index/policyProfileEnrollment:PolicyProfileEnrollment example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param PolicyProfileEnrollmentArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_profile_enrollment_apps.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_profile_enrollment_apps.py`

 * *Files 2% similar despite different names*

```diff
@@ -138,15 +138,15 @@
         ```
 
         ## Import
 
         A Profile Enrollment Policy Apps can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/policyProfileEnrollmentApps:PolicyProfileEnrollmentApps example <policy id>
+         $ pulumi import okta:index/policyProfileEnrollmentApps:PolicyProfileEnrollmentApps example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] apps: List of app IDs to be added to this policy.
         :param pulumi.Input[str] policy_id: ID of the enrollment policy.
         """
@@ -181,15 +181,15 @@
         ```
 
         ## Import
 
         A Profile Enrollment Policy Apps can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/policyProfileEnrollmentApps:PolicyProfileEnrollmentApps example <policy id>
+         $ pulumi import okta:index/policyProfileEnrollmentApps:PolicyProfileEnrollmentApps example &#60;policy id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param PolicyProfileEnrollmentAppsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/policy_rule_profile_enrollment.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/policy_rule_profile_enrollment.py`

 * *Files 1% similar despite different names*

```diff
@@ -345,15 +345,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:index/policyRuleProfileEnrollment:PolicyRuleProfileEnrollment example <policy id>/<rule id>
+         $ pulumi import okta:index/policyRuleProfileEnrollment:PolicyRuleProfileEnrollment example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] access: Allow or deny access based on the rule conditions. Valid values are: `"ALLOW"`, `"DENY"`. Default is `"ALLOW"`.
         :param pulumi.Input[bool] email_verification: Indicates whether email verification should occur before access is granted. Default is `true`.
         :param pulumi.Input[str] inline_hook_id: ID of a Registration Inline Hook.
@@ -418,15 +418,15 @@
         ```
 
         ## Import
 
         A Policy Rule can be imported via the Policy and Rule ID.
 
         ```sh
-         $ pulumi import okta:index/policyRuleProfileEnrollment:PolicyRuleProfileEnrollment example <policy id>/<rule id>
+         $ pulumi import okta:index/policyRuleProfileEnrollment:PolicyRuleProfileEnrollment example &#60;policy id&#62;/&#60;rule id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param PolicyRuleProfileEnrollmentArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/mapping.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/mapping.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/profile/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/profile/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/provider.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/provider.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/rate_limiting.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/rate_limiting.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/resource_set.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/resource_set.py`

 * *Files 2% similar despite different names*

```diff
@@ -148,15 +148,15 @@
         > **NOTE:** This an `Early Access` feature.
 
         ## Import
 
         Okta Resource Set can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/resourceSet:ResourceSet example <resource_set_id>
+         $ pulumi import okta:index/resourceSet:ResourceSet example &#60;resource_set_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] description: A description of the Resource Set.
         :param pulumi.Input[str] label: Unique name given to the Resource Set.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] resources: The endpoints that reference the resources to be included in the new Resource Set. At least one
@@ -183,15 +183,15 @@
         > **NOTE:** This an `Early Access` feature.
 
         ## Import
 
         Okta Resource Set can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/resourceSet:ResourceSet example <resource_set_id>
+         $ pulumi import okta:index/resourceSet:ResourceSet example &#60;resource_set_id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param ResourceSetArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/role_subscription.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/role_subscription.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,16 +15,16 @@
     def __init__(__self__, *,
                  notification_type: pulumi.Input[str],
                  role_type: pulumi.Input[str],
                  status: Optional[pulumi.Input[str]] = None):
         """
         The set of arguments for constructing a RoleSubscription resource.
         :param pulumi.Input[str] notification_type: Type of the notification. Valid values:
-        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-               "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+               `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         :param pulumi.Input[str] status: Subscription status. Valid values: `"subscribed"`, `"unsubscribed"`.
         """
         pulumi.set(__self__, "notification_type", notification_type)
         pulumi.set(__self__, "role_type", role_type)
         if status is not None:
             pulumi.set(__self__, "status", status)
 
@@ -40,16 +40,16 @@
     def notification_type(self, value: pulumi.Input[str]):
         pulumi.set(self, "notification_type", value)
 
     @property
     @pulumi.getter(name="roleType")
     def role_type(self) -> pulumi.Input[str]:
         """
-        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-        "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+        `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         """
         return pulumi.get(self, "role_type")
 
     @role_type.setter
     def role_type(self, value: pulumi.Input[str]):
         pulumi.set(self, "role_type", value)
 
@@ -71,16 +71,16 @@
     def __init__(__self__, *,
                  notification_type: Optional[pulumi.Input[str]] = None,
                  role_type: Optional[pulumi.Input[str]] = None,
                  status: Optional[pulumi.Input[str]] = None):
         """
         Input properties used for looking up and filtering RoleSubscription resources.
         :param pulumi.Input[str] notification_type: Type of the notification. Valid values:
-        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-               "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+               `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         :param pulumi.Input[str] status: Subscription status. Valid values: `"subscribed"`, `"unsubscribed"`.
         """
         if notification_type is not None:
             pulumi.set(__self__, "notification_type", notification_type)
         if role_type is not None:
             pulumi.set(__self__, "role_type", role_type)
         if status is not None:
@@ -98,16 +98,16 @@
     def notification_type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "notification_type", value)
 
     @property
     @pulumi.getter(name="roleType")
     def role_type(self) -> Optional[pulumi.Input[str]]:
         """
-        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-        "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+        `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         """
         return pulumi.get(self, "role_type")
 
     @role_type.setter
     def role_type(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "role_type", value)
 
@@ -151,22 +151,22 @@
         ```
 
         ## Import
 
         A role subscription can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/roleSubscription:RoleSubscription example <role_type>/<notification_type>
+         $ pulumi import okta:index/roleSubscription:RoleSubscription example &#60;role_type&#62;/&#60;notification_type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] notification_type: Type of the notification. Valid values:
-        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-               "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+               `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         :param pulumi.Input[str] status: Subscription status. Valid values: `"subscribed"`, `"unsubscribed"`.
         """
         ...
     @overload
     def __init__(__self__,
                  resource_name: str,
                  args: RoleSubscriptionArgs,
@@ -189,15 +189,15 @@
         ```
 
         ## Import
 
         A role subscription can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:index/roleSubscription:RoleSubscription example <role_type>/<notification_type>
+         $ pulumi import okta:index/roleSubscription:RoleSubscription example &#60;role_type&#62;/&#60;notification_type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param RoleSubscriptionArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -250,16 +250,16 @@
         Get an existing RoleSubscription resource's state with the given name, id, and optional extra
         properties used to qualify the lookup.
 
         :param str resource_name: The unique name of the resulting resource.
         :param pulumi.Input[str] id: The unique provider ID of the resource to lookup.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] notification_type: Type of the notification. Valid values:
-        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-               "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        :param pulumi.Input[str] role_type: Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+               `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         :param pulumi.Input[str] status: Subscription status. Valid values: `"subscribed"`, `"unsubscribed"`.
         """
         opts = pulumi.ResourceOptions.merge(opts, pulumi.ResourceOptions(id=id))
 
         __props__ = _RoleSubscriptionState.__new__(_RoleSubscriptionState)
 
         __props__.__dict__["notification_type"] = notification_type
@@ -275,16 +275,16 @@
         """
         return pulumi.get(self, "notification_type")
 
     @property
     @pulumi.getter(name="roleType")
     def role_type(self) -> pulumi.Output[str]:
         """
-        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN",
-        "APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN".
+        Type of the role. Valid values: `"SUPER_ADMIN"`, `"ORG_ADMIN"`, `"API_ACCESS_MANAGEMENT_ADMIN"`,
+        `"APP_ADMIN"`, `"USER_ADMIN"`, `"MOBILE_ADMIN"`, `"READ_ONLY_ADMIN"`, `"HELP_DESK_ADMIN"`, `"API_ADMIN"`.
         """
         return pulumi.get(self, "role_type")
 
     @property
     @pulumi.getter
     def status(self) -> pulumi.Output[Optional[str]]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/security_notification_emails.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/security_notification_emails.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/template/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/template/_inputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/template/email.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/template/email.py`

 * *Files 1% similar despite different names*

```diff
@@ -128,14 +128,16 @@
                  resource_name: str,
                  opts: Optional[pulumi.ResourceOptions] = None,
                  default_language: Optional[pulumi.Input[str]] = None,
                  translations: Optional[pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['EmailTranslationArgs']]]]] = None,
                  type: Optional[pulumi.Input[str]] = None,
                  __props__=None):
         """
+        ** This resource is deprecated. Swith over to the email_customization resource.
+
         Creates an Okta Email Template.
 
         This resource allows you to create and configure an Okta Email Template.
 
         ## Example Usage
 
         ```python
@@ -159,15 +161,15 @@
         ```
 
         ## Import
 
         An Okta Email Template can be imported via the template type.
 
         ```sh
-         $ pulumi import okta:template/email:Email example <template type>
+         $ pulumi import okta:template/email:Email example &#60;template type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] default_language: The default language, by default is set to `"en"`.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['EmailTranslationArgs']]]] translations: Set of translations for a particular template.
         :param pulumi.Input[str] type: Email template type
@@ -175,14 +177,16 @@
         ...
     @overload
     def __init__(__self__,
                  resource_name: str,
                  args: EmailArgs,
                  opts: Optional[pulumi.ResourceOptions] = None):
         """
+        ** This resource is deprecated. Swith over to the email_customization resource.
+
         Creates an Okta Email Template.
 
         This resource allows you to create and configure an Okta Email Template.
 
         ## Example Usage
 
         ```python
@@ -206,15 +210,15 @@
         ```
 
         ## Import
 
         An Okta Email Template can be imported via the template type.
 
         ```sh
-         $ pulumi import okta:template/email:Email example <template type>
+         $ pulumi import okta:template/email:Email example &#60;template type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param EmailArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/template/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/template/outputs.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/template_sms.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/template_sms.py`

 * *Files 2% similar despite different names*

```diff
@@ -158,15 +158,15 @@
         ```
 
         ## Import
 
         An Okta SMS Template can be imported via the template type.
 
         ```sh
-         $ pulumi import okta:index/templateSms:TemplateSms example <template type>
+         $ pulumi import okta:index/templateSms:TemplateSms example &#60;template type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] template: The SMS message.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['TemplateSmsTranslationArgs']]]] translations: Set of translations for a particular template.
         :param pulumi.Input[str] type: SMS template type
@@ -204,15 +204,15 @@
         ```
 
         ## Import
 
         An Okta SMS Template can be imported via the template type.
 
         ```sh
-         $ pulumi import okta:index/templateSms:TemplateSms example <template type>
+         $ pulumi import okta:index/templateSms:TemplateSms example &#60;template type&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param TemplateSmsArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/threat_insight_settings.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/threat_insight_settings.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/trustedorigin/origin.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/trustedorigin/origin.py`

 * *Files 1% similar despite different names*

```diff
@@ -179,15 +179,15 @@
         ```
 
         ## Import
 
         A Trusted Origin can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:trustedorigin/origin:Origin example <trusted origin id>
+         $ pulumi import okta:trustedorigin/origin:Origin example &#60;trusted origin id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[bool] active: Whether the Trusted Origin is active or not - can only be issued post-creation. By default, it is 'true'.
         :param pulumi.Input[str] name: Unique name for this trusted origin.
         :param pulumi.Input[str] origin: Unique origin URL for this trusted origin.
@@ -216,15 +216,15 @@
         ```
 
         ## Import
 
         A Trusted Origin can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:trustedorigin/origin:Origin example <trusted origin id>
+         $ pulumi import okta:trustedorigin/origin:Origin example &#60;trusted origin id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param OriginArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/__init__.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/__init__.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/_inputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/_inputs.py`

 * *Files 20% similar despite different names*

```diff
@@ -217,110 +217,146 @@
     def work_factor(self, value: Optional[pulumi.Input[int]]):
         pulumi.set(self, "work_factor", value)
 
 
 @pulumi.input_type
 class GetUserSearchArgs:
     def __init__(__self__, *,
-                 name: str,
-                 value: str,
-                 comparison: Optional[str] = None):
+                 comparison: Optional[str] = None,
+                 expression: Optional[str] = None,
+                 name: Optional[str] = None,
+                 value: Optional[str] = None):
         """
+        :param str comparison: Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
+        :param str expression: A raw search expression string. If present it will override name/comparison/value.
         :param str name: Name of property to search against.
         :param str value: Value to compare with.
-        :param str comparison: Comparison to use.
         """
-        pulumi.set(__self__, "name", name)
-        pulumi.set(__self__, "value", value)
         if comparison is not None:
             pulumi.set(__self__, "comparison", comparison)
+        if expression is not None:
+            pulumi.set(__self__, "expression", expression)
+        if name is not None:
+            pulumi.set(__self__, "name", name)
+        if value is not None:
+            pulumi.set(__self__, "value", value)
 
     @property
     @pulumi.getter
-    def name(self) -> str:
+    def comparison(self) -> Optional[str]:
+        """
+        Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
+        """
+        return pulumi.get(self, "comparison")
+
+    @comparison.setter
+    def comparison(self, value: Optional[str]):
+        pulumi.set(self, "comparison", value)
+
+    @property
+    @pulumi.getter
+    def expression(self) -> Optional[str]:
+        """
+        A raw search expression string. If present it will override name/comparison/value.
+        """
+        return pulumi.get(self, "expression")
+
+    @expression.setter
+    def expression(self, value: Optional[str]):
+        pulumi.set(self, "expression", value)
+
+    @property
+    @pulumi.getter
+    def name(self) -> Optional[str]:
         """
         Name of property to search against.
         """
         return pulumi.get(self, "name")
 
     @name.setter
-    def name(self, value: str):
+    def name(self, value: Optional[str]):
         pulumi.set(self, "name", value)
 
     @property
     @pulumi.getter
-    def value(self) -> str:
+    def value(self) -> Optional[str]:
         """
         Value to compare with.
         """
         return pulumi.get(self, "value")
 
     @value.setter
-    def value(self, value: str):
+    def value(self, value: Optional[str]):
         pulumi.set(self, "value", value)
 
+
+@pulumi.input_type
+class GetUsersSearchArgs:
+    def __init__(__self__, *,
+                 comparison: Optional[str] = None,
+                 expression: Optional[str] = None,
+                 name: Optional[str] = None,
+                 value: Optional[str] = None):
+        """
+        :param str comparison: Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
+        :param str expression: A raw search expression string. If present it will override name/comparison/value.
+        :param str name: Name of property to search against.
+        :param str value: Value to compare with.
+        """
+        if comparison is not None:
+            pulumi.set(__self__, "comparison", comparison)
+        if expression is not None:
+            pulumi.set(__self__, "expression", expression)
+        if name is not None:
+            pulumi.set(__self__, "name", name)
+        if value is not None:
+            pulumi.set(__self__, "value", value)
+
     @property
     @pulumi.getter
     def comparison(self) -> Optional[str]:
         """
-        Comparison to use.
+        Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
         """
         return pulumi.get(self, "comparison")
 
     @comparison.setter
     def comparison(self, value: Optional[str]):
         pulumi.set(self, "comparison", value)
 
-
-@pulumi.input_type
-class GetUsersSearchArgs:
-    def __init__(__self__, *,
-                 name: str,
-                 value: str,
-                 comparison: Optional[str] = None):
+    @property
+    @pulumi.getter
+    def expression(self) -> Optional[str]:
         """
-        :param str name: Name of property to search against.
-        :param str value: Value to compare with.
-        :param str comparison: Comparison to use.
+        A raw search expression string. If present it will override name/comparison/value.
         """
-        pulumi.set(__self__, "name", name)
-        pulumi.set(__self__, "value", value)
-        if comparison is not None:
-            pulumi.set(__self__, "comparison", comparison)
+        return pulumi.get(self, "expression")
+
+    @expression.setter
+    def expression(self, value: Optional[str]):
+        pulumi.set(self, "expression", value)
 
     @property
     @pulumi.getter
-    def name(self) -> str:
+    def name(self) -> Optional[str]:
         """
         Name of property to search against.
         """
         return pulumi.get(self, "name")
 
     @name.setter
-    def name(self, value: str):
+    def name(self, value: Optional[str]):
         pulumi.set(self, "name", value)
 
     @property
     @pulumi.getter
-    def value(self) -> str:
+    def value(self) -> Optional[str]:
         """
         Value to compare with.
         """
         return pulumi.get(self, "value")
 
     @value.setter
-    def value(self, value: str):
+    def value(self, value: Optional[str]):
         pulumi.set(self, "value", value)
 
-    @property
-    @pulumi.getter
-    def comparison(self) -> Optional[str]:
-        """
-        Comparison to use.
-        """
-        return pulumi.get(self, "comparison")
-
-    @comparison.setter
-    def comparison(self, value: Optional[str]):
-        pulumi.set(self, "comparison", value)
-
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/base_schema.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/base_schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -313,21 +313,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:user/baseSchema:BaseSchema example <property name>
+         $ pulumi import okta:user/baseSchema:BaseSchema example &#60;property name&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:user/baseSchema:BaseSchema example <user type id>.<property name>
+         $ pulumi import okta:user/baseSchema:BaseSchema example &#60;user type id&#62;.&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] index: The property name.
         :param pulumi.Input[str] master: Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
         :param pulumi.Input[str] pattern: The validation pattern to use for the subschema, only available for `login` property. Must be in form of `.+`, or `[<pattern>]+`.
@@ -363,21 +363,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:user/baseSchema:BaseSchema example <property name>
+         $ pulumi import okta:user/baseSchema:BaseSchema example &#60;property name&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:user/baseSchema:BaseSchema example <user type id>.<property name>
+         $ pulumi import okta:user/baseSchema:BaseSchema example &#60;user type id&#62;.&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param BaseSchemaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user.py`

 * *Files 4% similar despite different names*

```diff
@@ -18,21 +18,24 @@
 ]
 
 @pulumi.output_type
 class GetUserResult:
     """
     A collection of values returned by getUser.
     """
-    def __init__(__self__, admin_roles=None, city=None, cost_center=None, country_code=None, custom_profile_attributes=None, department=None, display_name=None, division=None, email=None, employee_number=None, first_name=None, group_memberships=None, honorific_prefix=None, honorific_suffix=None, id=None, last_name=None, locale=None, login=None, manager=None, manager_id=None, middle_name=None, mobile_phone=None, nick_name=None, organization=None, postal_address=None, preferred_language=None, primary_phone=None, profile_url=None, searches=None, second_email=None, skip_groups=None, skip_roles=None, state=None, status=None, street_address=None, timezone=None, title=None, user_id=None, user_type=None, zip_code=None):
+    def __init__(__self__, admin_roles=None, city=None, compound_search_operator=None, cost_center=None, country_code=None, custom_profile_attributes=None, department=None, display_name=None, division=None, email=None, employee_number=None, first_name=None, group_memberships=None, honorific_prefix=None, honorific_suffix=None, id=None, last_name=None, locale=None, login=None, manager=None, manager_id=None, middle_name=None, mobile_phone=None, nick_name=None, organization=None, postal_address=None, preferred_language=None, primary_phone=None, profile_url=None, searches=None, second_email=None, skip_groups=None, skip_roles=None, state=None, status=None, street_address=None, timezone=None, title=None, user_id=None, user_type=None, zip_code=None):
         if admin_roles and not isinstance(admin_roles, list):
             raise TypeError("Expected argument 'admin_roles' to be a list")
         pulumi.set(__self__, "admin_roles", admin_roles)
         if city and not isinstance(city, str):
             raise TypeError("Expected argument 'city' to be a str")
         pulumi.set(__self__, "city", city)
+        if compound_search_operator and not isinstance(compound_search_operator, str):
+            raise TypeError("Expected argument 'compound_search_operator' to be a str")
+        pulumi.set(__self__, "compound_search_operator", compound_search_operator)
         if cost_center and not isinstance(cost_center, str):
             raise TypeError("Expected argument 'cost_center' to be a str")
         pulumi.set(__self__, "cost_center", cost_center)
         if country_code and not isinstance(country_code, str):
             raise TypeError("Expected argument 'country_code' to be a str")
         pulumi.set(__self__, "country_code", country_code)
         if custom_profile_attributes and not isinstance(custom_profile_attributes, str):
@@ -157,14 +160,19 @@
     def city(self) -> str:
         """
         user profile property.
         """
         return pulumi.get(self, "city")
 
     @property
+    @pulumi.getter(name="compoundSearchOperator")
+    def compound_search_operator(self) -> Optional[str]:
+        return pulumi.get(self, "compound_search_operator")
+
+    @property
     @pulumi.getter(name="costCenter")
     def cost_center(self) -> str:
         """
         user profile property.
         """
         return pulumi.get(self, "cost_center")
 
@@ -457,14 +465,15 @@
     # pylint: disable=using-constant-test
     def __await__(self):
         if False:
             yield self
         return GetUserResult(
             admin_roles=self.admin_roles,
             city=self.city,
+            compound_search_operator=self.compound_search_operator,
             cost_center=self.cost_center,
             country_code=self.country_code,
             custom_profile_attributes=self.custom_profile_attributes,
             department=self.department,
             display_name=self.display_name,
             division=self.division,
             email=self.email,
@@ -497,60 +506,57 @@
             timezone=self.timezone,
             title=self.title,
             user_id=self.user_id,
             user_type=self.user_type,
             zip_code=self.zip_code)
 
 
-def get_user(searches: Optional[Sequence[pulumi.InputType['GetUserSearchArgs']]] = None,
+def get_user(compound_search_operator: Optional[str] = None,
+             searches: Optional[Sequence[pulumi.InputType['GetUserSearchArgs']]] = None,
              skip_groups: Optional[bool] = None,
              skip_roles: Optional[bool] = None,
              user_id: Optional[str] = None,
              opts: Optional[pulumi.InvokeOptions] = None) -> AwaitableGetUserResult:
     """
     Use this data source to retrieve a users from Okta.
 
     ## Example Usage
 
     ```python
     import pulumi
     import pulumi_okta as okta
 
-    example = okta.user.get_user(searches=[
-        okta.user.GetUserSearchArgs(
-            name="profile.firstName",
-            value="John",
-        ),
-        okta.user.GetUserSearchArgs(
-            name="profile.lastName",
-            value="Doe",
-        ),
-    ])
+    example = okta.user.get_user(searches=[okta.user.GetUserSearchArgs(
+        expression="profile.firstName eq \"John\"",
+    )])
     ```
 
 
+    :param str compound_search_operator: Given multiple search elements they will be compounded together with the op. Default is `and`, `or` is also valid.
     :param Sequence[pulumi.InputType['GetUserSearchArgs']] searches: Map of search criteria. It supports the following properties.
     :param bool skip_groups: Additional API call to collect user's groups will not be made.
     :param bool skip_roles: Additional API call to collect user's roles will not be made.
     :param str user_id: String representing a specific user's id value
     """
     __args__ = dict()
+    __args__['compoundSearchOperator'] = compound_search_operator
     __args__['searches'] = searches
     __args__['skipGroups'] = skip_groups
     __args__['skipRoles'] = skip_roles
     __args__['userId'] = user_id
     if opts is None:
         opts = pulumi.InvokeOptions()
     if opts.version is None:
         opts.version = _utilities.get_version()
     __ret__ = pulumi.runtime.invoke('okta:user/getUser:getUser', __args__, opts=opts, typ=GetUserResult).value
 
     return AwaitableGetUserResult(
         admin_roles=__ret__.admin_roles,
         city=__ret__.city,
+        compound_search_operator=__ret__.compound_search_operator,
         cost_center=__ret__.cost_center,
         country_code=__ret__.country_code,
         custom_profile_attributes=__ret__.custom_profile_attributes,
         department=__ret__.department,
         display_name=__ret__.display_name,
         division=__ret__.division,
         email=__ret__.email,
@@ -584,40 +590,35 @@
         title=__ret__.title,
         user_id=__ret__.user_id,
         user_type=__ret__.user_type,
         zip_code=__ret__.zip_code)
 
 
 @_utilities.lift_output_func(get_user)
-def get_user_output(searches: Optional[pulumi.Input[Optional[Sequence[pulumi.InputType['GetUserSearchArgs']]]]] = None,
+def get_user_output(compound_search_operator: Optional[pulumi.Input[Optional[str]]] = None,
+                    searches: Optional[pulumi.Input[Optional[Sequence[pulumi.InputType['GetUserSearchArgs']]]]] = None,
                     skip_groups: Optional[pulumi.Input[Optional[bool]]] = None,
                     skip_roles: Optional[pulumi.Input[Optional[bool]]] = None,
                     user_id: Optional[pulumi.Input[Optional[str]]] = None,
                     opts: Optional[pulumi.InvokeOptions] = None) -> pulumi.Output[GetUserResult]:
     """
     Use this data source to retrieve a users from Okta.
 
     ## Example Usage
 
     ```python
     import pulumi
     import pulumi_okta as okta
 
-    example = okta.user.get_user(searches=[
-        okta.user.GetUserSearchArgs(
-            name="profile.firstName",
-            value="John",
-        ),
-        okta.user.GetUserSearchArgs(
-            name="profile.lastName",
-            value="Doe",
-        ),
-    ])
+    example = okta.user.get_user(searches=[okta.user.GetUserSearchArgs(
+        expression="profile.firstName eq \"John\"",
+    )])
     ```
 
 
+    :param str compound_search_operator: Given multiple search elements they will be compounded together with the op. Default is `and`, `or` is also valid.
     :param Sequence[pulumi.InputType['GetUserSearchArgs']] searches: Map of search criteria. It supports the following properties.
     :param bool skip_groups: Additional API call to collect user's groups will not be made.
     :param bool skip_roles: Additional API call to collect user's roles will not be made.
     :param str user_id: String representing a specific user's id value
     """
     ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user_profile_mapping_source.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user_profile_mapping_source.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/get_user_type.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/get_user_type.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/outputs.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/outputs.py`

 * *Files 14% similar despite different names*

```diff
@@ -193,91 +193,119 @@
         """
         return pulumi.get(self, "work_factor")
 
 
 @pulumi.output_type
 class GetUserSearchResult(dict):
     def __init__(__self__, *,
-                 name: str,
-                 value: str,
-                 comparison: Optional[str] = None):
+                 comparison: Optional[str] = None,
+                 expression: Optional[str] = None,
+                 name: Optional[str] = None,
+                 value: Optional[str] = None):
         """
+        :param str comparison: Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
+        :param str expression: A raw search expression string. If present it will override name/comparison/value.
         :param str name: Name of property to search against.
         :param str value: Value to compare with.
-        :param str comparison: Comparison to use.
         """
-        pulumi.set(__self__, "name", name)
-        pulumi.set(__self__, "value", value)
         if comparison is not None:
             pulumi.set(__self__, "comparison", comparison)
+        if expression is not None:
+            pulumi.set(__self__, "expression", expression)
+        if name is not None:
+            pulumi.set(__self__, "name", name)
+        if value is not None:
+            pulumi.set(__self__, "value", value)
 
     @property
     @pulumi.getter
-    def name(self) -> str:
+    def comparison(self) -> Optional[str]:
         """
-        Name of property to search against.
+        Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
         """
-        return pulumi.get(self, "name")
+        return pulumi.get(self, "comparison")
 
     @property
     @pulumi.getter
-    def value(self) -> str:
+    def expression(self) -> Optional[str]:
         """
-        Value to compare with.
+        A raw search expression string. If present it will override name/comparison/value.
         """
-        return pulumi.get(self, "value")
+        return pulumi.get(self, "expression")
 
     @property
     @pulumi.getter
-    def comparison(self) -> Optional[str]:
+    def name(self) -> Optional[str]:
         """
-        Comparison to use.
+        Name of property to search against.
         """
-        return pulumi.get(self, "comparison")
+        return pulumi.get(self, "name")
+
+    @property
+    @pulumi.getter
+    def value(self) -> Optional[str]:
+        """
+        Value to compare with.
+        """
+        return pulumi.get(self, "value")
 
 
 @pulumi.output_type
 class GetUsersSearchResult(dict):
     def __init__(__self__, *,
-                 name: str,
-                 value: str,
-                 comparison: Optional[str] = None):
+                 comparison: Optional[str] = None,
+                 expression: Optional[str] = None,
+                 name: Optional[str] = None,
+                 value: Optional[str] = None):
         """
+        :param str comparison: Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
+        :param str expression: A raw search expression string. If present it will override name/comparison/value.
         :param str name: Name of property to search against.
         :param str value: Value to compare with.
-        :param str comparison: Comparison to use.
         """
-        pulumi.set(__self__, "name", name)
-        pulumi.set(__self__, "value", value)
         if comparison is not None:
             pulumi.set(__self__, "comparison", comparison)
+        if expression is not None:
+            pulumi.set(__self__, "expression", expression)
+        if name is not None:
+            pulumi.set(__self__, "name", name)
+        if value is not None:
+            pulumi.set(__self__, "value", value)
 
     @property
     @pulumi.getter
-    def name(self) -> str:
+    def comparison(self) -> Optional[str]:
         """
-        Name of property to search against.
+        Comparison to use. Comparitors for strings: [`eq`, `ge`, `gt`, `le`, `lt`, `ne`, `pr`, `sw`](https://developer.okta.com/docs/reference/core-okta-api/#operators).
         """
-        return pulumi.get(self, "name")
+        return pulumi.get(self, "comparison")
 
     @property
     @pulumi.getter
-    def value(self) -> str:
+    def expression(self) -> Optional[str]:
         """
-        Value to compare with.
+        A raw search expression string. If present it will override name/comparison/value.
         """
-        return pulumi.get(self, "value")
+        return pulumi.get(self, "expression")
 
     @property
     @pulumi.getter
-    def comparison(self) -> Optional[str]:
+    def name(self) -> Optional[str]:
         """
-        Comparison to use.
+        Name of property to search against.
         """
-        return pulumi.get(self, "comparison")
+        return pulumi.get(self, "name")
+
+    @property
+    @pulumi.getter
+    def value(self) -> Optional[str]:
+        """
+        Value to compare with.
+        """
+        return pulumi.get(self, "value")
 
 
 @pulumi.output_type
 class GetUsersUserResult(dict):
     def __init__(__self__, *,
                  admin_roles: Sequence[str],
                  city: str,
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/schema.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/schema.py`

 * *Files 1% similar despite different names*

```diff
@@ -742,21 +742,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:user/schema:Schema example <index>
+         $ pulumi import okta:user/schema:Schema example &#60;index&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:user/schema:Schema example <user type id>.<index>
+         $ pulumi import okta:user/schema:Schema example &#60;user type id&#62;.&#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] array_enums: Array of values that an array property's items can be set to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['SchemaArrayOneOfArgs']]]] array_one_ofs: Display name and value an enum array can be set to.
         :param pulumi.Input[str] array_type: The type of the array elements if `type` is set to `"array"`.
@@ -803,21 +803,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:user/schema:Schema example <index>
+         $ pulumi import okta:user/schema:Schema example &#60;index&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:user/schema:Schema example <user type id>.<index>
+         $ pulumi import okta:user/schema:Schema example &#60;user type id&#62;.&#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param SchemaArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/user.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/user.py`

 * *Files 1% similar despite different names*

```diff
@@ -98,15 +98,15 @@
         :param pulumi.Input[str] preferred_language: User profile property.
         :param pulumi.Input[str] primary_phone: User profile property.
         :param pulumi.Input[str] profile_url: User profile property.
         :param pulumi.Input[str] recovery_answer: User password recovery answer.
         :param pulumi.Input[str] recovery_question: User password recovery question.
         :param pulumi.Input[str] second_email: User profile property.
         :param pulumi.Input[str] state: User profile property.
-        :param pulumi.Input[str] status: User profile property.
+        :param pulumi.Input[str] status: User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         :param pulumi.Input[str] street_address: User profile property.
         :param pulumi.Input[str] timezone: User profile property.
         :param pulumi.Input[str] title: User profile property.
         :param pulumi.Input[str] user_type: User profile property.
         :param pulumi.Input[str] zip_code: User profile property.
         """
         pulumi.set(__self__, "email", email)
@@ -635,15 +635,15 @@
     def state(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "state", value)
 
     @property
     @pulumi.getter
     def status(self) -> Optional[pulumi.Input[str]]:
         """
-        User profile property.
+        User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         """
         return pulumi.get(self, "status")
 
     @status.setter
     def status(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "status", value)
 
@@ -796,15 +796,15 @@
         :param pulumi.Input[str] primary_phone: User profile property.
         :param pulumi.Input[str] profile_url: User profile property.
         :param pulumi.Input[str] raw_status: The raw status of the User in Okta - (status is mapped)
         :param pulumi.Input[str] recovery_answer: User password recovery answer.
         :param pulumi.Input[str] recovery_question: User password recovery question.
         :param pulumi.Input[str] second_email: User profile property.
         :param pulumi.Input[str] state: User profile property.
-        :param pulumi.Input[str] status: User profile property.
+        :param pulumi.Input[str] status: User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         :param pulumi.Input[str] street_address: User profile property.
         :param pulumi.Input[str] timezone: User profile property.
         :param pulumi.Input[str] title: User profile property.
         :param pulumi.Input[str] user_type: User profile property.
         :param pulumi.Input[str] zip_code: User profile property.
         """
         if admin_roles is not None:
@@ -1351,15 +1351,15 @@
     def state(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "state", value)
 
     @property
     @pulumi.getter
     def status(self) -> Optional[pulumi.Input[str]]:
         """
-        User profile property.
+        User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         """
         return pulumi.get(self, "status")
 
     @status.setter
     def status(self, value: Optional[pulumi.Input[str]]):
         pulumi.set(self, "status", value)
 
@@ -1534,15 +1534,15 @@
         ```
 
         ## Import
 
         An Okta User can be imported via the ID.
 
         ```sh
-         $ pulumi import okta:user/user:User example <user id>
+         $ pulumi import okta:user/user:User example &#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] admin_roles: Administrator roles assigned to User.
                - `DEPRECATED`: Please replace usage with the `UserAdminRoles` resource.
         :param pulumi.Input[str] city: User profile property.
@@ -1582,15 +1582,15 @@
         :param pulumi.Input[str] preferred_language: User profile property.
         :param pulumi.Input[str] primary_phone: User profile property.
         :param pulumi.Input[str] profile_url: User profile property.
         :param pulumi.Input[str] recovery_answer: User password recovery answer.
         :param pulumi.Input[str] recovery_question: User password recovery question.
         :param pulumi.Input[str] second_email: User profile property.
         :param pulumi.Input[str] state: User profile property.
-        :param pulumi.Input[str] status: User profile property.
+        :param pulumi.Input[str] status: User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         :param pulumi.Input[str] street_address: User profile property.
         :param pulumi.Input[str] timezone: User profile property.
         :param pulumi.Input[str] title: User profile property.
         :param pulumi.Input[str] user_type: User profile property.
         :param pulumi.Input[str] zip_code: User profile property.
         """
         ...
@@ -1661,15 +1661,15 @@
         ```
 
         ## Import
 
         An Okta User can be imported via the ID.
 
         ```sh
-         $ pulumi import okta:user/user:User example <user id>
+         $ pulumi import okta:user/user:User example &#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
@@ -1894,15 +1894,15 @@
         :param pulumi.Input[str] primary_phone: User profile property.
         :param pulumi.Input[str] profile_url: User profile property.
         :param pulumi.Input[str] raw_status: The raw status of the User in Okta - (status is mapped)
         :param pulumi.Input[str] recovery_answer: User password recovery answer.
         :param pulumi.Input[str] recovery_question: User password recovery question.
         :param pulumi.Input[str] second_email: User profile property.
         :param pulumi.Input[str] state: User profile property.
-        :param pulumi.Input[str] status: User profile property.
+        :param pulumi.Input[str] status: User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         :param pulumi.Input[str] street_address: User profile property.
         :param pulumi.Input[str] timezone: User profile property.
         :param pulumi.Input[str] title: User profile property.
         :param pulumi.Input[str] user_type: User profile property.
         :param pulumi.Input[str] zip_code: User profile property.
         """
         opts = pulumi.ResourceOptions.merge(opts, pulumi.ResourceOptions(id=id))
@@ -2257,15 +2257,15 @@
         """
         return pulumi.get(self, "state")
 
     @property
     @pulumi.getter
     def status(self) -> pulumi.Output[Optional[str]]:
         """
-        User profile property.
+        User profile property. Valid values are "ACTIVE", "DEPROVISIONED", "STAGED", "SUSPENDED"
         """
         return pulumi.get(self, "status")
 
     @property
     @pulumi.getter(name="streetAddress")
     def street_address(self) -> pulumi.Output[Optional[str]]:
         """
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user/user_type.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user/user_type.py`

 * *Files 1% similar despite different names*

```diff
@@ -146,15 +146,15 @@
         ```
 
         ## Import
 
         A User Type can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:user/userType:UserType example <user type id>
+         $ pulumi import okta:user/userType:UserType example &#60;user type id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] description: Description of the User Type.
         :param pulumi.Input[str] display_name: Display Name of the User Type.
         :param pulumi.Input[str] name: Name of the User Type.
@@ -182,15 +182,15 @@
         ```
 
         ## Import
 
         A User Type can be imported via the Okta ID.
 
         ```sh
-         $ pulumi import okta:user/userType:UserType example <user type id>
+         $ pulumi import okta:user/userType:UserType example &#60;user type id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserTypeArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user_admin_roles.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user_admin_roles.py`

 * *Files 2% similar despite different names*

```diff
@@ -158,15 +158,15 @@
         ```
 
         ## Import
 
         Existing user admin roles can be imported via the Okta User ID.
 
         ```sh
-         $ pulumi import okta:index/userAdminRoles:UserAdminRoles example <user id>
+         $ pulumi import okta:index/userAdminRoles:UserAdminRoles example &#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] admin_roles: The list of Okta user admin roles, e.g. `["APP_ADMIN", "USER_ADMIN"]`
         :param pulumi.Input[bool] disable_notifications: When this setting is enabled, the admins won't receive any of the default Okta 
                administrator emails. These admins also won't have access to contact Okta Support and open support cases on behalf of your org.
@@ -203,15 +203,15 @@
         ```
 
         ## Import
 
         Existing user admin roles can be imported via the Okta User ID.
 
         ```sh
-         $ pulumi import okta:index/userAdminRoles:UserAdminRoles example <user id>
+         $ pulumi import okta:index/userAdminRoles:UserAdminRoles example &#60;user id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserAdminRolesArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user_base_schema_property.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user_base_schema_property.py`

 * *Files 2% similar despite different names*

```diff
@@ -322,21 +322,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example <property name>
+         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example &#60;property name&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example <user type id>.<property name>
+         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example &#60;user type id&#62;.&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] index: The property name.
         :param pulumi.Input[str] master: Master priority for the user schema property. It can be set to `"PROFILE_MASTER"` or `"OKTA"`.
         :param pulumi.Input[str] pattern: The validation pattern to use for the subschema, only available for `login` property. Must be in form of `.+`, or `[<pattern>]+`.
@@ -381,21 +381,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example <property name>
+         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example &#60;property name&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example <user type id>.<property name>
+         $ pulumi import okta:index/userBaseSchemaProperty:UserBaseSchemaProperty example &#60;user type id&#62;.&#60;property name&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserBaseSchemaPropertyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user_factor_question.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user_factor_question.py`

 * *Files 0% similar despite different names*

```diff
@@ -188,15 +188,15 @@
         ```
 
         ## Import
 
         Security question factor for a user can be imported via the `user_id` and the `factor_id`.
 
         ```sh
-         $ pulumi import okta:index/userFactorQuestion:UserFactorQuestion example <user id>/<question factor id>
+         $ pulumi import okta:index/userFactorQuestion:UserFactorQuestion example &#60;user id&#62;/&#60;question factor id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[str] answer: Security question answer. Note here that answer won't be set during the resource import.
         :param pulumi.Input[str] key: Security question unique key.
         :param pulumi.Input[str] user_id: ID of the user. Resource will be recreated when `user_id` changes.
@@ -235,15 +235,15 @@
         ```
 
         ## Import
 
         Security question factor for a user can be imported via the `user_id` and the `factor_id`.
 
         ```sh
-         $ pulumi import okta:index/userFactorQuestion:UserFactorQuestion example <user id>/<question factor id>
+         $ pulumi import okta:index/userFactorQuestion:UserFactorQuestion example &#60;user id&#62;/&#60;question factor id&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserFactorQuestionArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user_group_memberships.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user_group_memberships.py`

 * *Files identical despite different names*

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta/user_schema_property.py` & `pulumi_okta-3.9.0a1652715097/pulumi_okta/user_schema_property.py`

 * *Files 2% similar despite different names*

```diff
@@ -746,21 +746,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example <index>
+         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example &#60;index&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example <user type id>.<index>
+         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example &#60;user type id&#62;.&#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param pulumi.ResourceOptions opts: Options for the resource.
         :param pulumi.Input[Sequence[pulumi.Input[str]]] array_enums: Array of values that an array property's items can be set to.
         :param pulumi.Input[Sequence[pulumi.Input[pulumi.InputType['UserSchemaPropertyArrayOneOfArgs']]]] array_one_ofs: Display name and value an enum array can be set to.
         :param pulumi.Input[str] array_type: The type of the array elements if `type` is set to `"array"`.
@@ -811,21 +811,21 @@
         ```
 
         ## Import
 
         User schema property of default user type can be imported via the property index.
 
         ```sh
-         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example <index>
+         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example &#60;index&#62;
         ```
 
          User schema property of custom user type can be imported via user type id and property index
 
         ```sh
-         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example <user type id>.<index>
+         $ pulumi import okta:index/userSchemaProperty:UserSchemaProperty example &#60;user type id&#62;.&#60;index&#62;
         ```
 
         :param str resource_name: The name of the resource.
         :param UserSchemaPropertyArgs args: The arguments to use to populate this resource's properties.
         :param pulumi.ResourceOptions opts: Options for the resource.
         """
         ...
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/PKG-INFO` & `pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pulumi-okta
-Version: 3.9.0a1650909822
+Version: 3.9.0a1652715097
 Summary: A Pulumi package for creating and managing okta resources.
 Home-page: https://pulumi.io
 License: Apache-2.0
 Project-URL: Repository, https://github.com/pulumi/pulumi-okta
 Description: r[![Actions Status](https://github.com/pulumi/pulumi-okta/workflows/master/badge.svg)](https://github.com/pulumi/pulumi-okta/actions)
         [![Slack](http://www.pulumi.com/images/docs/badges/slack.svg)](https://slack.pulumi.com)
         [![NPM version](https://badge.fury.io/js/%40pulumi%2Fokta.svg)](https://www.npmjs.com/package/@pulumi/okta)
```

### Comparing `pulumi_okta-3.9.0a1650909822/pulumi_okta.egg-info/SOURCES.txt` & `pulumi_okta-3.9.0a1652715097/pulumi_okta.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -13,35 +13,45 @@
 pulumi_okta/app_signon_policy_rule.py
 pulumi_okta/app_user_base_schema_property.py
 pulumi_okta/app_user_schema_property.py
 pulumi_okta/auth_server_claim_default.py
 pulumi_okta/auth_server_default.py
 pulumi_okta/authenticator.py
 pulumi_okta/behaviour.py
+pulumi_okta/brand.py
 pulumi_okta/captcha.py
 pulumi_okta/captcha_org_wide_settings.py
 pulumi_okta/domain.py
 pulumi_okta/domain_certificate.py
 pulumi_okta/domain_verification.py
+pulumi_okta/email_customization.py
 pulumi_okta/email_sender.py
 pulumi_okta/email_sender_verification.py
 pulumi_okta/event_hook.py
 pulumi_okta/event_hook_verification.py
 pulumi_okta/factor_totp.py
 pulumi_okta/get_app_group_assignments.py
 pulumi_okta/get_app_signon_policy.py
 pulumi_okta/get_app_user_assignments.py
 pulumi_okta/get_auth_server_claim.py
 pulumi_okta/get_auth_server_claims.py
 pulumi_okta/get_authenticator.py
 pulumi_okta/get_behaviour.py
 pulumi_okta/get_behaviours.py
+pulumi_okta/get_brand.py
+pulumi_okta/get_brands.py
+pulumi_okta/get_email_customization.py
+pulumi_okta/get_email_customizations.py
 pulumi_okta/get_groups.py
 pulumi_okta/get_network_zone.py
 pulumi_okta/get_role_subscription.py
+pulumi_okta/get_template.py
+pulumi_okta/get_templates.py
+pulumi_okta/get_theme.py
+pulumi_okta/get_themes.py
 pulumi_okta/get_trusted_origins.py
 pulumi_okta/get_user_security_questions.py
 pulumi_okta/group_memberships.py
 pulumi_okta/group_schema_property.py
 pulumi_okta/link_definition.py
 pulumi_okta/link_value.py
 pulumi_okta/org_configuration.py
@@ -56,14 +66,15 @@
 pulumi_okta/pulumi-plugin.json
 pulumi_okta/py.typed
 pulumi_okta/rate_limiting.py
 pulumi_okta/resource_set.py
 pulumi_okta/role_subscription.py
 pulumi_okta/security_notification_emails.py
 pulumi_okta/template_sms.py
+pulumi_okta/theme.py
 pulumi_okta/threat_insight_settings.py
 pulumi_okta/user_admin_roles.py
 pulumi_okta/user_base_schema_property.py
 pulumi_okta/user_factor_question.py
 pulumi_okta/user_group_memberships.py
 pulumi_okta/user_schema_property.py
 pulumi_okta.egg-info/PKG-INFO
```

### Comparing `pulumi_okta-3.9.0a1650909822/setup.py` & `pulumi_okta-3.9.0a1652715097/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 
 import errno
 from setuptools import setup, find_packages
 from setuptools.command.install import install
 from subprocess import check_call
 
 
-VERSION = "3.9.0a1650909822"
-PLUGIN_VERSION = "3.9.0-alpha.1650909822+56a310b5"
+VERSION = "3.9.0a1652715097"
+PLUGIN_VERSION = "3.9.0-alpha.1652715097+705a5aa3"
 
 class InstallPluginCommand(install):
     def run(self):
         install.run(self)
         try:
             check_call(['pulumi', 'plugin', 'install', 'resource', 'okta', PLUGIN_VERSION])
         except OSError as error:
```

