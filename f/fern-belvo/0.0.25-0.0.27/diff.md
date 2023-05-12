# Comparing `tmp/fern_belvo-0.0.25.tar.gz` & `tmp/fern_belvo-0.0.27.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fern_belvo-0.0.25.tar", max compression
+gzip compressed data, was "fern_belvo-0.0.27.tar", max compression
```

## Comparing `fern_belvo-0.0.25.tar` & `fern_belvo-0.0.27.tar`

### file list

```diff
@@ -1,482 +1,469 @@
--rw-r--r--   0        0        0     2581 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/README.md
--rw-r--r--   0        0        0      433 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/pyproject.toml
--rw-r--r--   0        0        0    28390 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/__init__.py
--rw-r--r--   0        0        0    16332 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/client.py
--rw-r--r--   0        0        0      348 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/core/__init__.py
--rw-r--r--   0        0        0      426 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/core/api_error.py
--rw-r--r--   0        0        0     1047 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/core/datetime_utils.py
--rw-r--r--   0        0        0     3710 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/core/jsonable_encoder.py
--rw-r--r--   0        0        0      385 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/core/remove_none_from_headers.py
--rw-r--r--   0        0        0      247 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/environment.py
--rw-r--r--   0        0        0      594 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/__init__.py
--rw-r--r--   0        0        0      346 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/bad_request_error.py
--rw-r--r--   0        0        0      341 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/forbidden_error.py
--rw-r--r--   0        0        0      323 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/internal_server_error.py
--rw-r--r--   0        0        0      325 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/not_found_error.py
--rw-r--r--   0        0        0      340 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/precondition_error.py
--rw-r--r--   0        0        0      349 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/request_timeout_error.py
--rw-r--r--   0        0        0      340 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/errors/unauthorized_error.py
--rw-r--r--   0        0        0        0 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/py.typed
--rw-r--r--   0        0        0     1252 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/resources/__init__.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.402869 fern_belvo-0.0.25/src/belvo/resources/accounts/__init__.py
--rw-r--r--   0        0        0    24969 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/accounts/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/balances/__init__.py
--rw-r--r--   0        0        0    22327 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/balances/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/bank_accounts/__init__.py
--rw-r--r--   0        0        0    12881 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/bank_accounts/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/categorization/__init__.py
--rw-r--r--   0        0        0     5136 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/categorization/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/customers/__init__.py
--rw-r--r--   0        0        0    11285 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/customers/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/employment_records/__init__.py
--rw-r--r--   0        0        0    13909 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/employment_records/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/income_verification/__init__.py
--rw-r--r--   0        0        0     7011 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/income_verification/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/incomes/__init__.py
--rw-r--r--   0        0        0    18409 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/incomes/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/institutions/__init__.py
--rw-r--r--   0        0        0     8765 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/institutions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/investment_portfolios/__init__.py
--rw-r--r--   0        0        0    18632 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/investment_portfolios/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/invoices/__init__.py
--rw-r--r--   0        0        0    23340 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/invoices/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/links/__init__.py
--rw-r--r--   0        0        0    28742 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/links/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/owners/__init__.py
--rw-r--r--   0        0        0    19773 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/owners/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_institutions/__init__.py
--rw-r--r--   0        0        0     7761 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_institutions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_intents/__init__.py
--rw-r--r--   0        0        0    16753 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_intents/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_links/__init__.py
--rw-r--r--   0        0        0    12471 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_links/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_transactions/__init__.py
--rw-r--r--   0        0        0    10337 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_transactions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_webhooks/__init__.py
--rw-r--r--   0        0        0    12737 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/payment_webhooks/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/receivable_transactions/__init__.py
--rw-r--r--   0        0        0    16641 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/receivable_transactions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/recurring_expenses/__init__.py
--rw-r--r--   0        0        0    19318 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/recurring_expenses/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/risk_insights/__init__.py
--rw-r--r--   0        0        0    18655 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/risk_insights/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/secret_keys/__init__.py
--rw-r--r--   0        0        0     5974 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/secret_keys/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_compliance_status/__init__.py
--rw-r--r--   0        0        0    15284 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_compliance_status/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_declarations/__init__.py
--rw-r--r--   0        0        0    16352 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_declarations/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_retentions/__init__.py
--rw-r--r--   0        0        0    14725 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_retentions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_returns/__init__.py
--rw-r--r--   0        0        0    16912 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_returns/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_status/__init__.py
--rw-r--r--   0        0        0    15045 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/tax_status/client.py
--rw-r--r--   0        0        0       65 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/transactions/__init__.py
--rw-r--r--   0        0        0    34291 2023-05-12 20:31:50.406869 fern_belvo-0.0.25/src/belvo/resources/transactions/client.py
--rw-r--r--   0        0        0    42168 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/__init__.py
--rw-r--r--   0        0        0     1908 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/access_to_resource_denied.py
--rw-r--r--   0        0        0     4506 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/account.py
--rw-r--r--   0        0        0     2443 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_balance.py
--rw-r--r--   0        0        0     2241 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_credit_data.py
--rw-r--r--   0        0        0     1594 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_funds_data.py
--rw-r--r--   0        0        0      958 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_funds_data_public_identifications.py
--rw-r--r--   0        0        0     4780 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_loan_data.py
--rw-r--r--   0        0        0      935 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_loan_data_fees.py
--rw-r--r--   0        0        0     1191 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_loan_data_interest_rate.py
--rw-r--r--   0        0        0     1674 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_paginated_response.py
--rw-r--r--   0        0        0     1349 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/accounts_receivables_data.py
--rw-r--r--   0        0        0     1588 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/annual_costs_and_deductions_statement_business.py
--rw-r--r--   0        0        0     1883 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/annual_income_statement_business.py
--rw-r--r--   0        0        0     1282 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/annual_income_statement_individual.py
--rw-r--r--   0        0        0     1514 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/annual_totals_individual.py
--rw-r--r--   0        0        0      992 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/asynchronous_accepted_202.py
--rw-r--r--   0        0        0     1014 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bad_request_error_body_item.py
--rw-r--r--   0        0        0     1827 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/balance.py
--rw-r--r--   0        0        0     1671 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/balances_paginated_response.py
--rw-r--r--   0        0        0     1990 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/balances_request.py
--rw-r--r--   0        0        0     2531 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_business_pse.py
--rw-r--r--   0        0        0     1189 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_details_ofpi.py
--rw-r--r--   0        0        0      930 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_details_ofpi_pix.py
--rw-r--r--   0        0        0     1196 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_details_open_finance.py
--rw-r--r--   0        0        0      937 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_details_open_finance_pix.py
--rw-r--r--   0        0        0     1094 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_holder_request_ofpi.py
--rw-r--r--   0        0        0      356 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_holder_request_ofpi_information.py
--rw-r--r--   0        0        0      966 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_information_content_pse.py
--rw-r--r--   0        0        0     1077 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_information_pse.py
--rw-r--r--   0        0        0     1852 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_ofpi_response.py
--rw-r--r--   0        0        0      309 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_ofpi_response_details.py
--rw-r--r--   0        0        0     1801 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_paginated_response.py
--rw-r--r--   0        0        0      311 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_paginated_response_results_item.py
--rw-r--r--   0        0        0      176 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/bank_account_pse_response.py
--rw-r--r--   0        0        0     1439 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/beneficiary_bank_account_ofpi.py
--rw-r--r--   0        0        0      356 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/beneficiary_bank_account_ofpi_details.py
--rw-r--r--   0        0        0     1242 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/beneficiary_bank_account_pse.py
--rw-r--r--   0        0        0      945 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/categorization.py
--rw-r--r--   0        0        0     3020 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/categorization_body.py
--rw-r--r--   0        0        0     2488 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/categorization_body_request.py
--rw-r--r--   0        0        0     1052 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/categorization_merchant_data.py
--rw-r--r--   0        0        0      848 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/change_access_mode.py
--rw-r--r--   0        0        0     3723 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge.py
--rw-r--r--   0        0        0      342 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details.py
--rw-r--r--   0        0        0      972 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_ofpi.py
--rw-r--r--   0        0        0     1135 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_ofpi_content.py
--rw-r--r--   0        0        0      959 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_pse.py
--rw-r--r--   0        0        0     1127 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_pse_content.py
--rw-r--r--   0        0        0      703 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/charge_status.py
--rw-r--r--   0        0        0     1304 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_bank_account_ofpi.py
--rw-r--r--   0        0        0      307 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_bank_account_ofpi_details.py
--rw-r--r--   0        0        0     1863 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_bank_account_pse.py
--rw-r--r--   0        0        0      284 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_bank_account_request.py
--rw-r--r--   0        0        0      297 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_bank_account_response.py
--rw-r--r--   0        0        0     1521 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_customer_ofpi.py
--rw-r--r--   0        0        0     1517 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_customer_pse.py
--rw-r--r--   0        0        0      261 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_customer_request.py
--rw-r--r--   0        0        0      224 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_customer_response.py
--rw-r--r--   0        0        0     2638 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_intent_pse.py
--rw-r--r--   0        0        0      134 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_intent_pse_amount.py
--rw-r--r--   0        0        0     2894 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_link_ofpi.py
--rw-r--r--   0        0        0      135 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_link_ofpi_amount.py
--rw-r--r--   0        0        0     2835 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_link_pse.py
--rw-r--r--   0        0        0      132 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_payment_link_pse_amount.py
--rw-r--r--   0        0        0      284 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_paymentlink_request.py
--rw-r--r--   0        0        0      247 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/create_paymentlink_response.py
--rw-r--r--   0        0        0     1855 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/customer_ofpi.py
--rw-r--r--   0        0        0     1784 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/customer_paginated_response.py
--rw-r--r--   0        0        0      238 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/customer_paginated_response_results_item.py
--rw-r--r--   0        0        0     2229 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/customer_pse.py
--rw-r--r--   0        0        0      297 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_bank_account_response.py
--rw-r--r--   0        0        0      253 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_create_paymentlink_response.py
--rw-r--r--   0        0        0      224 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_customer_response.py
--rw-r--r--   0        0        0      237 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_invoice_response.py
--rw-r--r--   0        0        0      301 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_tax_declaration_response.py
--rw-r--r--   0        0        0      450 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_tax_return_response.py
--rw-r--r--   0        0        0      233 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/detail_tax_status_response.py
--rw-r--r--   0        0        0      972 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_confirmation_required_content_pse.py
--rw-r--r--   0        0        0     1301 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_confirmation_required_ofpi.py
--rw-r--r--   0        0        0     1001 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_credentials_required_content_pse.py
--rw-r--r--   0        0        0     1279 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_customer_bank_accounts_content_pse.py
--rw-r--r--   0        0        0      913 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_payment_failed.py
--rw-r--r--   0        0        0     1055 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_payment_method_information_content_ofpi.py
--rw-r--r--   0        0        0     1489 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_payment_method_information_content_pse.py
--rw-r--r--   0        0        0      917 2023-05-12 20:31:50.410869 fern_belvo-0.0.25/src/belvo/types/display_payment_processing.py
--rw-r--r--   0        0        0      916 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/display_payment_succeeded.py
--rw-r--r--   0        0        0      861 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/display_token_required_content_pse.py
--rw-r--r--   0        0        0     1005 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/document_id_business.py
--rw-r--r--   0        0        0     1007 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/document_id_individual.py
--rw-r--r--   0        0        0     1277 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/document_information_business.py
--rw-r--r--   0        0        0     1275 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/document_information_individual.py
--rw-r--r--   0        0        0     2557 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record.py
--rw-r--r--   0        0        0     2769 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_detail.py
--rw-r--r--   0        0        0     1086 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_document_id.py
--rw-r--r--   0        0        0     1317 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_employment_status_updates.py
--rw-r--r--   0        0        0     1584 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_entitlement.py
--rw-r--r--   0        0        0     1034 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_file.py
--rw-r--r--   0        0        0     1843 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_personal_data.py
--rw-r--r--   0        0        0     1353 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_request.py
--rw-r--r--   0        0        0     1495 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_record_social_security_summary.py
--rw-r--r--   0        0        0     1732 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/employment_records_paginated_response.py
--rw-r--r--   0        0        0      123 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_account_category.py
--rw-r--r--   0        0        0      630 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_bank_account_holder_type_ofpi.py
--rw-r--r--   0        0        0      506 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_bank_account_holder_type_pse.py
--rw-r--r--   0        0        0      850 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py
--rw-r--r--   0        0        0     1179 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_categorization_account_category.py
--rw-r--r--   0        0        0      668 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_categorization_account_holder_type.py
--rw-r--r--   0        0        0      141 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_categorization_transaction_category.py
--rw-r--r--   0        0        0      144 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_categorization_transaction_subcategory.py
--rw-r--r--   0        0        0      702 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_categorization_transaction_type.py
--rw-r--r--   0        0        0      592 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_customer_identifier_type_ofpi.py
--rw-r--r--   0        0        0     1031 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_customer_identifier_type_pse.py
--rw-r--r--   0        0        0      699 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_customer_type.py
--rw-r--r--   0        0        0      495 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_employment_record_document_type.py
--rw-r--r--   0        0        0      532 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_employment_record_status.py
--rw-r--r--   0        0        0     1719 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_employment_record_status_update_events.py
--rw-r--r--   0        0        0      911 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_minimum_confidence_level_request.py
--rw-r--r--   0        0        0      475 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_source_type.py
--rw-r--r--   0        0        0      824 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_stream_confidence.py
--rw-r--r--   0        0        0     1495 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_stream_frequency.py
--rw-r--r--   0        0        0     2123 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_stream_type.py
--rw-r--r--   0        0        0      758 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_verification_account_category.py
--rw-r--r--   0        0        0      484 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_verification_account_holder_type.py
--rw-r--r--   0        0        0      359 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_income_verification_type.py
--rw-r--r--   0        0        0      862 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_institution_integration_type.py
--rw-r--r--   0        0        0      630 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_institution_status.py
--rw-r--r--   0        0        0      805 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_institution_type.py
--rw-r--r--   0        0        0     1687 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_investment_portfolio_instrument_type.py
--rw-r--r--   0        0        0     1084 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_investment_portfolio_type.py
--rw-r--r--   0        0        0     2329 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_allowed_income_types_request.py
--rw-r--r--   0        0        0      470 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_dian_invoice_type.py
--rw-r--r--   0        0        0      132 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_dian_payment_method.py
--rw-r--r--   0        0        0      986 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_sat_invoice_type.py
--rw-r--r--   0        0        0      131 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_sat_payment_method.py
--rw-r--r--   0        0        0      119 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_invoice_type.py
--rw-r--r--   0        0        0      923 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_link_access_mode_request.py
--rw-r--r--   0        0        0      130 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_link_access_mode_response.py
--rw-r--r--   0        0        0      123 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_link_refresh_rate.py
--rw-r--r--   0        0        0     1144 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_link_status.py
--rw-r--r--   0        0        0      869 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_loan_data_fee_type.py
--rw-r--r--   0        0        0      513 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_loan_data_interest_rate_type.py
--rw-r--r--   0        0        0      636 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_intent_holder_type_pse.py
--rw-r--r--   0        0        0     1196 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_intent_status.py
--rw-r--r--   0        0        0      728 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_link_allowed_payment_method.py
--rw-r--r--   0        0        0      711 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_link_provider.py
--rw-r--r--   0        0        0      981 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_links_status.py
--rw-r--r--   0        0        0      682 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payment_transaction_type.py
--rw-r--r--   0        0        0      571 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payments_country.py
--rw-r--r--   0        0        0      586 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_payments_currency.py
--rw-r--r--   0        0        0      416 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_receivable_transaction_fee_type.py
--rw-r--r--   0        0        0      930 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_receivable_transaction_status.py
--rw-r--r--   0        0        0      133 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_receivable_transaction_type.py
--rw-r--r--   0        0        0     2023 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_category.py
--rw-r--r--   0        0        0      513 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_frequency.py
--rw-r--r--   0        0        0      552 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_payment_type.py
--rw-r--r--   0        0        0      760 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_tax_compliance_status_outcome.py
--rw-r--r--   0        0        0      526 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_payment_status.py
--rw-r--r--   0        0        0      544 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_receiver_nationality.py
--rw-r--r--   0        0        0      735 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_type.py
--rw-r--r--   0        0        0      129 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_transaction_bill_status.py
--rw-r--r--   0        0        0      127 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_transaction_category.py
--rw-r--r--   0        0        0      125 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_transaction_status.py
--rw-r--r--   0        0        0      130 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_transaction_subcategory.py
--rw-r--r--   0        0        0      123 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/enum_transaction_type.py
--rw-r--r--   0        0        0     2117 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/equity_statement_business.py
--rw-r--r--   0        0        0     1137 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/equity_statement_individual.py
--rw-r--r--   0        0        0     2410 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/eyod_income_verification_body_request.py
--rw-r--r--   0        0        0     1525 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/gross_income_individual.py
--rw-r--r--   0        0        0     1067 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_bank_account_information_pse.py
--rw-r--r--   0        0        0     1089 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_bank_account_pse.py
--rw-r--r--   0        0        0     1045 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_business_pse.py
--rw-r--r--   0        0        0     1179 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_business_response_pse.py
--rw-r--r--   0        0        0     1189 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_information_business_ofpi.py
--rw-r--r--   0        0        0     1073 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_information_business_ofpi_response.py
--rw-r--r--   0        0        0      935 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_information_business_pse.py
--rw-r--r--   0        0        0      993 2023-05-12 20:31:50.414869 fern_belvo-0.0.25/src/belvo/types/holder_information_business_pse_response.py
--rw-r--r--   0        0        0     1290 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/holder_information_individual_ofpi.py
--rw-r--r--   0        0        0     1174 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/holder_information_individual_ofpi_response.py
--rw-r--r--   0        0        0     1043 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/holder_response_ofpi.py
--rw-r--r--   0        0        0      402 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/holder_response_ofpi_information.py
--rw-r--r--   0        0        0     4077 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/income.py
--rw-r--r--   0        0        0     4769 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/income_streams_body.py
--rw-r--r--   0        0        0     1666 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/incomes_paginated_response.py
--rw-r--r--   0        0        0     2630 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/incomes_request.py
--rw-r--r--   0        0        0     3939 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution.py
--rw-r--r--   0        0        0     1205 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution_account.py
--rw-r--r--   0        0        0     1989 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution_down_error.py
--rw-r--r--   0        0        0     2062 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution_form_field.py
--rw-r--r--   0        0        0     1894 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution_inactive_error.py
--rw-r--r--   0        0        0     2011 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institution_unavailable_error.py
--rw-r--r--   0        0        0      937 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institutions_feature.py
--rw-r--r--   0        0        0     1937 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institutions_form_field.py
--rw-r--r--   0        0        0     1513 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institutions_form_field_values.py
--rw-r--r--   0        0        0     1691 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/institutions_paginated_response.py
--rw-r--r--   0        0        0     2002 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invalid_access_mode.py
--rw-r--r--   0        0        0     1936 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invalid_link_error.py
--rw-r--r--   0        0        0     1967 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invalid_period_error.py
--rw-r--r--   0        0        0     2666 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio.py
--rw-r--r--   0        0        0     4088 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument.py
--rw-r--r--   0        0        0     1056 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_fees.py
--rw-r--r--   0        0        0     1465 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_interest_rate.py
--rw-r--r--   0        0        0     1008 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_public_id.py
--rw-r--r--   0        0        0      952 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py
--rw-r--r--   0        0        0     1751 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/investments_portfolios_paginated_response.py
--rw-r--r--   0        0        0     2518 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_detail_dian.py
--rw-r--r--   0        0        0     1418 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_detail_retained_tax_sat.py
--rw-r--r--   0        0        0     3178 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_detail_sat.py
--rw-r--r--   0        0        0     7893 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_dian.py
--rw-r--r--   0        0        0     2326 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_sender_details_dian.py
--rw-r--r--   0        0        0     1066 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_warnings_dian.py
--rw-r--r--   0        0        0      925 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_warnings_sat.py
--rw-r--r--   0        0        0     9760 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoice_with_id_sat.py
--rw-r--r--   0        0        0     2919 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payments_dian.py
--rw-r--r--   0        0        0     2063 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payments_related_documents_dian.py
--rw-r--r--   0        0        0     2024 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payments_related_documents_sat.py
--rw-r--r--   0        0        0     3037 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payments_sat.py
--rw-r--r--   0        0        0     2066 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payroll_dian.py
--rw-r--r--   0        0        0     1782 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_payroll_sat.py
--rw-r--r--   0        0        0     2343 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_receiver_details_dian.py
--rw-r--r--   0        0        0     2061 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_request.py
--rw-r--r--   0        0        0     1809 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_response_paginated_response.py
--rw-r--r--   0        0        0      260 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/invoices_response_paginated_response_results_item.py
--rw-r--r--   0        0        0     1249 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_invalid_credentials.py
--rw-r--r--   0        0        0     1227 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_invalid_token.py
--rw-r--r--   0        0        0     1257 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_login_error.py
--rw-r--r--   0        0        0     1243 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_payment_error.py
--rw-r--r--   0        0        0     1289 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_session_expired.py
--rw-r--r--   0        0        0     1261 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/last_error_two_factor.py
--rw-r--r--   0        0        0     2833 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/link.py
--rw-r--r--   0        0        0     4669 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/links_put_request.py
--rw-r--r--   0        0        0     7955 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/links_request.py
--rw-r--r--   0        0        0      554 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/list_payment_links_request_ordering.py
--rw-r--r--   0        0        0      521 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/list_payment_links_request_status.py
--rw-r--r--   0        0        0      356 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/list_tax_declarations_response.py
--rw-r--r--   0        0        0      586 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/list_tax_returns_response.py
--rw-r--r--   0        0        0     2699 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/login_error.py
--rw-r--r--   0        0        0      913 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/needs_redirect_content.py
--rw-r--r--   0        0        0      923 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/needs_redirect_content_pse.py
--rw-r--r--   0        0        0     1588 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/net_income_individual.py
--rw-r--r--   0        0        0     1660 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_ofpi.py
--rw-r--r--   0        0        0     2256 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py
--rw-r--r--   0        0        0     1673 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_pse.py
--rw-r--r--   0        0        0     2850 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_pse_type.py
--rw-r--r--   0        0        0     1665 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_credentials_required_pse.py
--rw-r--r--   0        0        0     2840 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_credentials_required_pse_type.py
--rw-r--r--   0        0        0     1676 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_customer_bank_accounts_pse.py
--rw-r--r--   0        0        0     2850 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py
--rw-r--r--   0        0        0     1595 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_needs_redirect_pse.py
--rw-r--r--   0        0        0     2780 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_needs_redirect_pse_type.py
--rw-r--r--   0        0        0     1573 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_failed.py
--rw-r--r--   0        0        0     2179 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_failed_type.py
--rw-r--r--   0        0        0     1700 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information.py
--rw-r--r--   0        0        0     1874 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_pse.py
--rw-r--r--   0        0        0     2890 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_pse_type.py
--rw-r--r--   0        0        0     2256 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_type.py
--rw-r--r--   0        0        0     1606 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_processing.py
--rw-r--r--   0        0        0     2207 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_processing_type.py
--rw-r--r--   0        0        0     1598 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_succeeded.py
--rw-r--r--   0        0        0     2200 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_succeeded_type.py
--rw-r--r--   0        0        0     2128 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_token_required_pse.py
--rw-r--r--   0        0        0     2780 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_display_token_required_pse_type.py
--rw-r--r--   0        0        0     1545 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_needs_redirect.py
--rw-r--r--   0        0        0     2130 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/next_step_needs_redirect_type.py
--rw-r--r--   0        0        0     1531 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/non_taxable_income_individual.py
--rw-r--r--   0        0        0     1703 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/not_found_error_body.py
--rw-r--r--   0        0        0     2545 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/owner.py
--rw-r--r--   0        0        0     1584 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/owner_document_id.py
--rw-r--r--   0        0        0     1661 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/owners_paginated_response.py
--rw-r--r--   0        0        0     1596 2023-05-12 20:31:50.418869 fern_belvo-0.0.25/src/belvo/types/paginated_response_link.py
--rw-r--r--   0        0        0     1798 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/patch_body.py
--rw-r--r--   0        0        0     1479 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/patch_body_without_save_data.py
--rw-r--r--   0        0        0      241 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/patch_invoices_response_item.py
--rw-r--r--   0        0        0      876 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/patch_payment_intents_body_pse.py
--rw-r--r--   0        0        0     2677 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/patch_payment_method_details_pse.py
--rw-r--r--   0        0        0     2302 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_institution.py
--rw-r--r--   0        0        0     4025 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_ofpi.py
--rw-r--r--   0        0        0      846 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_ofpi_next_step.py
--rw-r--r--   0        0        0      462 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_ofpi_payment_method_details.py
--rw-r--r--   0        0        0     1733 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_paginated_response.py
--rw-r--r--   0        0        0     1549 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py
--rw-r--r--   0        0        0     1551 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py
--rw-r--r--   0        0        0     2222 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_pse.py
--rw-r--r--   0        0        0     1013 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py
--rw-r--r--   0        0        0     1030 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py
--rw-r--r--   0        0        0      983 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_pse.py
--rw-r--r--   0        0        0     4050 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_pse.py
--rw-r--r--   0        0        0      656 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_pse_last_error.py
--rw-r--r--   0        0        0      933 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intent_pse_next_step.py
--rw-r--r--   0        0        0     1644 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intents_payment_method_details_body_pse.py
--rw-r--r--   0        0        0      995 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_intents_payment_method_details_pse.py
--rw-r--r--   0        0        0     1499 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_callback_urls.py
--rw-r--r--   0        0        0     1408 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_callback_urls_response.py
--rw-r--r--   0        0        0     2547 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_list_ofpi.py
--rw-r--r--   0        0        0     2546 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_list_pse.py
--rw-r--r--   0        0        0     2331 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_ofpi.py
--rw-r--r--   0        0        0     1801 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_paginated_response.py
--rw-r--r--   0        0        0      287 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_paginated_response_results_item.py
--rw-r--r--   0        0        0     2326 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_link_pse.py
--rw-r--r--   0        0        0     1244 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_links_payment_method_details_body_ofpi.py
--rw-r--r--   0        0        0     1646 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_links_payment_method_details_body_pse.py
--rw-r--r--   0        0        0     1021 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_details_ofpi.py
--rw-r--r--   0        0        0      980 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_details_pse.py
--rw-r--r--   0        0        0     1530 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py
--rw-r--r--   0        0        0     1256 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_information_body_ofpi.py
--rw-r--r--   0        0        0     1390 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_information_body_pse.py
--rw-r--r--   0        0        0     1013 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_information_details_pse.py
--rw-r--r--   0        0        0      967 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_information_ofpi.py
--rw-r--r--   0        0        0     1043 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_method_information_pse.py
--rw-r--r--   0        0        0     2247 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_transaction.py
--rw-r--r--   0        0        0      313 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_transaction_payer.py
--rw-r--r--   0        0        0     1527 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payment_webhook.py
--rw-r--r--   0        0        0     1742 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payments_institutions_paginated_response.py
--rw-r--r--   0        0        0     1742 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payments_transactions_paginated_response.py
--rw-r--r--   0        0        0     1471 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payments_way.py
--rw-r--r--   0        0        0     1708 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/payments_webhooks_paginated_response.py
--rw-r--r--   0        0        0     1072 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/pension_income_statement_individual.py
--rw-r--r--   0        0        0      817 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/providers_pse.py
--rw-r--r--   0        0        0     1866 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/receivable_transaction_request.py
--rw-r--r--   0        0        0     2957 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/receivables_transaction.py
--rw-r--r--   0        0        0     1042 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/receivables_transaction_account.py
--rw-r--r--   0        0        0     1065 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/receivables_transaction_number_of_installments.py
--rw-r--r--   0        0        0     1750 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/receivables_transactions_paginated_response.py
--rw-r--r--   0        0        0     1026 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/recevables_transaction_fees.py
--rw-r--r--   0        0        0     1242 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/recurring_expense_source_transaction.py
--rw-r--r--   0        0        0     2895 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/recurring_expenses.py
--rw-r--r--   0        0        0     1735 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/recurring_expenses_paginated_response.py
--rw-r--r--   0        0        0     2148 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/recurring_expenses_request.py
--rw-r--r--   0        0        0     1120 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/reporting_id.py
--rw-r--r--   0        0        0     2051 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/request_timeout_error_body.py
--rw-r--r--   0        0        0     1454 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retention_breakdown.py
--rw-r--r--   0        0        0      244 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retrieve_invoices_response_item.py
--rw-r--r--   0        0        0      308 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retrieve_tax_declarations_response_item.py
--rw-r--r--   0        0        0      307 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retrieve_tax_returns_request_body.py
--rw-r--r--   0        0        0      457 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retrieve_tax_returns_response_item.py
--rw-r--r--   0        0        0      235 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/retrieve_tax_status_response.py
--rw-r--r--   0        0        0     1980 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights.py
--rw-r--r--   0        0        0     3951 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_balance_metrics.py
--rw-r--r--   0        0        0     3942 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_cashflow_metrics.py
--rw-r--r--   0        0        0     1093 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_credit_card_metrics.py
--rw-r--r--   0        0        0     1369 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_loans_metrics.py
--rw-r--r--   0        0        0     1711 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_paginated_response.py
--rw-r--r--   0        0        0     9169 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/risk_insights_transaction_metrics.py
--rw-r--r--   0        0        0     1176 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/secret_keys.py
--rw-r--r--   0        0        0     1694 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/secret_keys_paginated_response.py
--rw-r--r--   0        0        0     2013 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/session_expired_error.py
--rw-r--r--   0        0        0     1276 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/standard_request.py
--rw-r--r--   0        0        0     2491 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_assessment_business.py
--rw-r--r--   0        0        0     2771 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_assessment_individual.py
--rw-r--r--   0        0        0     1788 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_compliance_status.py
--rw-r--r--   0        0        0     1748 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_compliance_status_paginated_response.py
--rw-r--r--   0        0        0     1326 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_compliance_status_request.py
--rw-r--r--   0        0        0     2291 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_declaration_business.py
--rw-r--r--   0        0        0     1755 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_declaration_business_paginated.py
--rw-r--r--   0        0        0     2281 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_declaration_individual.py
--rw-r--r--   0        0        0     1765 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_declaration_individual_paginated.py
--rw-r--r--   0        0        0     1727 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_declarations_request.py
--rw-r--r--   0        0        0     1666 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_payer_information_business.py
--rw-r--r--   0        0        0     1489 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_payer_information_individual.py
--rw-r--r--   0        0        0     3880 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_retentions.py
--rw-r--r--   0        0        0     1716 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_retentions_paginated_response.py
--rw-r--r--   0        0        0     1989 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_retentions_request.py
--rw-r--r--   0        0        0      129 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_return_business.py
--rw-r--r--   0        0        0      136 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_return_business_monthly.py
--rw-r--r--   0        0        0      129 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_return_personal.py
--rw-r--r--   0        0        0      136 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_return_personal_monthly.py
--rw-r--r--   0        0        0      146 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_returns_business_monthly_paginated.py
--rw-r--r--   0        0        0      139 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_returns_business_paginated.py
--rw-r--r--   0        0        0     2175 2023-05-12 20:31:50.422869 fern_belvo-0.0.25/src/belvo/types/tax_returns_monthly_request.py
--rw-r--r--   0        0        0      146 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_returns_personal_monthly_paginated.py
--rw-r--r--   0        0        0      139 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_returns_personal_paginated.py
--rw-r--r--   0        0        0     1967 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_returns_yearly_request.py
--rw-r--r--   0        0        0     1089 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_address_between_street_dian.py
--rw-r--r--   0        0        0     1029 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_address_between_street_sat.py
--rw-r--r--   0        0        0     2076 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_address_dian.py
--rw-r--r--   0        0        0     1919 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_address_sat.py
--rw-r--r--   0        0        0     3269 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_dian.py
--rw-r--r--   0        0        0     1728 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_economic_activity_dian.py
--rw-r--r--   0        0        0     1328 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_economic_activity_sat.py
--rw-r--r--   0        0        0     1550 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_obligations_dian.py
--rw-r--r--   0        0        0     1357 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_obligations_sat.py
--rw-r--r--   0        0        0     1784 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_paginated_response.py
--rw-r--r--   0        0        0      247 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_paginated_response_results_item.py
--rw-r--r--   0        0        0     1179 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_regimens_dian.py
--rw-r--r--   0        0        0     1048 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_regimens_sat.py
--rw-r--r--   0        0        0     1316 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_request.py
--rw-r--r--   0        0        0     3194 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_sat.py
--rw-r--r--   0        0        0     2648 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_tax_payer_information_dian.py
--rw-r--r--   0        0        0     2672 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/tax_status_tax_payer_information_sat.py
--rw-r--r--   0        0        0     2428 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/token_required_response.py
--rw-r--r--   0        0        0     1605 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/token_required_response_token_generation_data.py
--rw-r--r--   0        0        0     2133 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/too_many_sessions_error.py
--rw-r--r--   0        0        0     3391 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction.py
--rw-r--r--   0        0        0     1052 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction_bank_account_body_pse.py
--rw-r--r--   0        0        0      138 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction_bank_account_ofpi.py
--rw-r--r--   0        0        0      325 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction_bank_account_pse.py
--rw-r--r--   0        0        0     1689 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction_credit_card_data.py
--rw-r--r--   0        0        0     1049 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transaction_merchant_data.py
--rw-r--r--   0        0        0     1691 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transactions_paginated_response.py
--rw-r--r--   0        0        0     2001 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/transactions_request.py
--rw-r--r--   0        0        0     1945 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/unauthorized_error_body.py
--rw-r--r--   0        0        0     2077 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/unconfirmed_link_error.py
--rw-r--r--   0        0        0     2013 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/unexpected_error.py
--rw-r--r--   0        0        0     2032 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/unsupported_operation_error.py
--rw-r--r--   0        0        0     2657 2023-05-12 20:31:50.426869 fern_belvo-0.0.25/src/belvo/types/validation_error.py
--rw-r--r--   0        0        0     3181 1970-01-01 00:00:00.000000 fern_belvo-0.0.25/PKG-INFO
+-rw-r--r--   0        0        0     2460 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/README.md
+-rw-r--r--   0        0        0      433 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/pyproject.toml
+-rw-r--r--   0        0        0    27716 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/__init__.py
+-rw-r--r--   0        0        0    16332 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/client.py
+-rw-r--r--   0        0        0      348 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/core/__init__.py
+-rw-r--r--   0        0        0      426 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/core/api_error.py
+-rw-r--r--   0        0        0     1047 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/core/datetime_utils.py
+-rw-r--r--   0        0        0     3710 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/core/jsonable_encoder.py
+-rw-r--r--   0        0        0      385 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/core/remove_none_from_headers.py
+-rw-r--r--   0        0        0      247 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/environment.py
+-rw-r--r--   0        0        0      594 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/__init__.py
+-rw-r--r--   0        0        0      346 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/bad_request_error.py
+-rw-r--r--   0        0        0      341 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/forbidden_error.py
+-rw-r--r--   0        0        0      323 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/internal_server_error.py
+-rw-r--r--   0        0        0      325 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/not_found_error.py
+-rw-r--r--   0        0        0      340 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/precondition_error.py
+-rw-r--r--   0        0        0      349 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/request_timeout_error.py
+-rw-r--r--   0        0        0      340 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/errors/unauthorized_error.py
+-rw-r--r--   0        0        0        0 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/py.typed
+-rw-r--r--   0        0        0     1252 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/__init__.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/accounts/__init__.py
+-rw-r--r--   0        0        0    24969 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/accounts/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/balances/__init__.py
+-rw-r--r--   0        0        0    23438 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/balances/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/bank_accounts/__init__.py
+-rw-r--r--   0        0        0    12881 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/bank_accounts/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/categorization/__init__.py
+-rw-r--r--   0        0        0     5136 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/categorization/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/customers/__init__.py
+-rw-r--r--   0        0        0    11285 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/customers/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/employment_records/__init__.py
+-rw-r--r--   0        0        0    14543 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/employment_records/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/income_verification/__init__.py
+-rw-r--r--   0        0        0     7011 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/income_verification/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/incomes/__init__.py
+-rw-r--r--   0        0        0    20690 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/incomes/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/institutions/__init__.py
+-rw-r--r--   0        0        0     8765 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/institutions/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/investment_portfolios/__init__.py
+-rw-r--r--   0        0        0    18632 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/investment_portfolios/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/invoices/__init__.py
+-rw-r--r--   0        0        0    24516 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/invoices/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/links/__init__.py
+-rw-r--r--   0        0        0    33898 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/links/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/owners/__init__.py
+-rw-r--r--   0        0        0    19773 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/owners/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_institutions/__init__.py
+-rw-r--r--   0        0        0     7761 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_institutions/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_intents/__init__.py
+-rw-r--r--   0        0        0    16753 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_intents/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_links/__init__.py
+-rw-r--r--   0        0        0    12471 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_links/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_transactions/__init__.py
+-rw-r--r--   0        0        0    10337 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_transactions/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_webhooks/__init__.py
+-rw-r--r--   0        0        0    12737 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/payment_webhooks/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/receivable_transactions/__init__.py
+-rw-r--r--   0        0        0    17393 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/receivable_transactions/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/recurring_expenses/__init__.py
+-rw-r--r--   0        0        0    20402 2023-05-12 23:08:15.674100 fern_belvo-0.0.27/src/belvo/resources/recurring_expenses/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/risk_insights/__init__.py
+-rw-r--r--   0        0        0    18655 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/risk_insights/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/secret_keys/__init__.py
+-rw-r--r--   0        0        0     5974 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/secret_keys/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_compliance_status/__init__.py
+-rw-r--r--   0        0        0    15905 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_compliance_status/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_declarations/__init__.py
+-rw-r--r--   0        0        0    17236 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_declarations/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_retentions/__init__.py
+-rw-r--r--   0        0        0    15901 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_retentions/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_returns/__init__.py
+-rw-r--r--   0        0        0    16912 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_returns/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_status/__init__.py
+-rw-r--r--   0        0        0    15773 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/tax_status/client.py
+-rw-r--r--   0        0        0       65 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/transactions/__init__.py
+-rw-r--r--   0        0        0    34291 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/resources/transactions/client.py
+-rw-r--r--   0        0        0    41108 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/__init__.py
+-rw-r--r--   0        0        0     1908 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/access_to_resource_denied.py
+-rw-r--r--   0        0        0     4506 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/account.py
+-rw-r--r--   0        0        0     2443 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_balance.py
+-rw-r--r--   0        0        0     2241 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_credit_data.py
+-rw-r--r--   0        0        0     1594 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_funds_data.py
+-rw-r--r--   0        0        0      958 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_funds_data_public_identifications.py
+-rw-r--r--   0        0        0     4780 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_loan_data.py
+-rw-r--r--   0        0        0      935 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_loan_data_fees.py
+-rw-r--r--   0        0        0     1191 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_loan_data_interest_rate.py
+-rw-r--r--   0        0        0     1674 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_paginated_response.py
+-rw-r--r--   0        0        0     1349 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/accounts_receivables_data.py
+-rw-r--r--   0        0        0     1588 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/annual_costs_and_deductions_statement_business.py
+-rw-r--r--   0        0        0     1883 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/annual_income_statement_business.py
+-rw-r--r--   0        0        0     1282 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/annual_income_statement_individual.py
+-rw-r--r--   0        0        0     1514 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/annual_totals_individual.py
+-rw-r--r--   0        0        0      992 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/asynchronous_accepted_202.py
+-rw-r--r--   0        0        0     1014 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bad_request_error_body_item.py
+-rw-r--r--   0        0        0     1827 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/balance.py
+-rw-r--r--   0        0        0     1671 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/balances_paginated_response.py
+-rw-r--r--   0        0        0     2531 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_business_pse.py
+-rw-r--r--   0        0        0     1189 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_details_ofpi.py
+-rw-r--r--   0        0        0      930 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_details_ofpi_pix.py
+-rw-r--r--   0        0        0     1196 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_details_open_finance.py
+-rw-r--r--   0        0        0      937 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_details_open_finance_pix.py
+-rw-r--r--   0        0        0     1094 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_holder_request_ofpi.py
+-rw-r--r--   0        0        0      356 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_holder_request_ofpi_information.py
+-rw-r--r--   0        0        0      966 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_information_content_pse.py
+-rw-r--r--   0        0        0     1077 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_information_pse.py
+-rw-r--r--   0        0        0     1852 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_ofpi_response.py
+-rw-r--r--   0        0        0      309 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_ofpi_response_details.py
+-rw-r--r--   0        0        0     1801 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_paginated_response.py
+-rw-r--r--   0        0        0      311 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_paginated_response_results_item.py
+-rw-r--r--   0        0        0      176 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/bank_account_pse_response.py
+-rw-r--r--   0        0        0     1439 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/beneficiary_bank_account_ofpi.py
+-rw-r--r--   0        0        0      356 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/beneficiary_bank_account_ofpi_details.py
+-rw-r--r--   0        0        0     1242 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/beneficiary_bank_account_pse.py
+-rw-r--r--   0        0        0      945 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/categorization.py
+-rw-r--r--   0        0        0     3020 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/categorization_body.py
+-rw-r--r--   0        0        0     2488 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/categorization_body_request.py
+-rw-r--r--   0        0        0     1052 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/categorization_merchant_data.py
+-rw-r--r--   0        0        0     3723 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge.py
+-rw-r--r--   0        0        0      342 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details.py
+-rw-r--r--   0        0        0      972 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_ofpi.py
+-rw-r--r--   0        0        0     1135 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_ofpi_content.py
+-rw-r--r--   0        0        0      959 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_pse.py
+-rw-r--r--   0        0        0     1127 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_pse_content.py
+-rw-r--r--   0        0        0      703 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/charge_status.py
+-rw-r--r--   0        0        0     1304 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_bank_account_ofpi.py
+-rw-r--r--   0        0        0      307 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_bank_account_ofpi_details.py
+-rw-r--r--   0        0        0     1863 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_bank_account_pse.py
+-rw-r--r--   0        0        0      284 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_bank_account_request.py
+-rw-r--r--   0        0        0      297 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_bank_account_response.py
+-rw-r--r--   0        0        0     1521 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_customer_ofpi.py
+-rw-r--r--   0        0        0     1517 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_customer_pse.py
+-rw-r--r--   0        0        0      261 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_customer_request.py
+-rw-r--r--   0        0        0      224 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_customer_response.py
+-rw-r--r--   0        0        0     2638 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_intent_pse.py
+-rw-r--r--   0        0        0      134 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_intent_pse_amount.py
+-rw-r--r--   0        0        0     2894 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_link_ofpi.py
+-rw-r--r--   0        0        0      135 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_link_ofpi_amount.py
+-rw-r--r--   0        0        0     2835 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_link_pse.py
+-rw-r--r--   0        0        0      132 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_payment_link_pse_amount.py
+-rw-r--r--   0        0        0      284 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_paymentlink_request.py
+-rw-r--r--   0        0        0      247 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/create_paymentlink_response.py
+-rw-r--r--   0        0        0     1855 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/customer_ofpi.py
+-rw-r--r--   0        0        0     1784 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/customer_paginated_response.py
+-rw-r--r--   0        0        0      238 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/customer_paginated_response_results_item.py
+-rw-r--r--   0        0        0     2229 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/customer_pse.py
+-rw-r--r--   0        0        0      297 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_bank_account_response.py
+-rw-r--r--   0        0        0      253 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_create_paymentlink_response.py
+-rw-r--r--   0        0        0      224 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_customer_response.py
+-rw-r--r--   0        0        0      237 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_invoice_response.py
+-rw-r--r--   0        0        0      301 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_tax_declaration_response.py
+-rw-r--r--   0        0        0      450 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_tax_return_response.py
+-rw-r--r--   0        0        0      233 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/detail_tax_status_response.py
+-rw-r--r--   0        0        0      972 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_confirmation_required_content_pse.py
+-rw-r--r--   0        0        0     1301 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_confirmation_required_ofpi.py
+-rw-r--r--   0        0        0     1001 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_credentials_required_content_pse.py
+-rw-r--r--   0        0        0     1279 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_customer_bank_accounts_content_pse.py
+-rw-r--r--   0        0        0      913 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_payment_failed.py
+-rw-r--r--   0        0        0     1055 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_payment_method_information_content_ofpi.py
+-rw-r--r--   0        0        0     1489 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_payment_method_information_content_pse.py
+-rw-r--r--   0        0        0      917 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_payment_processing.py
+-rw-r--r--   0        0        0      916 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_payment_succeeded.py
+-rw-r--r--   0        0        0      861 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/display_token_required_content_pse.py
+-rw-r--r--   0        0        0     1005 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/document_id_business.py
+-rw-r--r--   0        0        0     1007 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/document_id_individual.py
+-rw-r--r--   0        0        0     1277 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/document_information_business.py
+-rw-r--r--   0        0        0     1275 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/document_information_individual.py
+-rw-r--r--   0        0        0     2557 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/employment_record.py
+-rw-r--r--   0        0        0     2769 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/employment_record_detail.py
+-rw-r--r--   0        0        0     1086 2023-05-12 23:08:15.678100 fern_belvo-0.0.27/src/belvo/types/employment_record_document_id.py
+-rw-r--r--   0        0        0     1317 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_record_employment_status_updates.py
+-rw-r--r--   0        0        0     1584 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_record_entitlement.py
+-rw-r--r--   0        0        0     1034 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_record_file.py
+-rw-r--r--   0        0        0     1843 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_record_personal_data.py
+-rw-r--r--   0        0        0     1495 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_record_social_security_summary.py
+-rw-r--r--   0        0        0     1732 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/employment_records_paginated_response.py
+-rw-r--r--   0        0        0      123 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_account_category.py
+-rw-r--r--   0        0        0      630 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_bank_account_holder_type_ofpi.py
+-rw-r--r--   0        0        0      506 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_bank_account_holder_type_pse.py
+-rw-r--r--   0        0        0      850 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py
+-rw-r--r--   0        0        0     1179 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_categorization_account_category.py
+-rw-r--r--   0        0        0      668 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_categorization_account_holder_type.py
+-rw-r--r--   0        0        0      141 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_categorization_transaction_category.py
+-rw-r--r--   0        0        0      144 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_categorization_transaction_subcategory.py
+-rw-r--r--   0        0        0      702 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_categorization_transaction_type.py
+-rw-r--r--   0        0        0      592 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_customer_identifier_type_ofpi.py
+-rw-r--r--   0        0        0     1031 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_customer_identifier_type_pse.py
+-rw-r--r--   0        0        0      699 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_customer_type.py
+-rw-r--r--   0        0        0      495 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_employment_record_document_type.py
+-rw-r--r--   0        0        0      532 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_employment_record_status.py
+-rw-r--r--   0        0        0     1719 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_employment_record_status_update_events.py
+-rw-r--r--   0        0        0      911 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_minimum_confidence_level_request.py
+-rw-r--r--   0        0        0      475 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_source_type.py
+-rw-r--r--   0        0        0      824 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_stream_confidence.py
+-rw-r--r--   0        0        0     1495 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_stream_frequency.py
+-rw-r--r--   0        0        0     2123 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_stream_type.py
+-rw-r--r--   0        0        0      758 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_verification_account_category.py
+-rw-r--r--   0        0        0      484 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_verification_account_holder_type.py
+-rw-r--r--   0        0        0      359 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_income_verification_type.py
+-rw-r--r--   0        0        0      862 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_institution_integration_type.py
+-rw-r--r--   0        0        0      630 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_institution_status.py
+-rw-r--r--   0        0        0      805 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_institution_type.py
+-rw-r--r--   0        0        0     1687 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_investment_portfolio_instrument_type.py
+-rw-r--r--   0        0        0     1084 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_investment_portfolio_type.py
+-rw-r--r--   0        0        0     2329 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_allowed_income_types_request.py
+-rw-r--r--   0        0        0      470 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_dian_invoice_type.py
+-rw-r--r--   0        0        0      132 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_dian_payment_method.py
+-rw-r--r--   0        0        0      986 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_sat_invoice_type.py
+-rw-r--r--   0        0        0      131 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_sat_payment_method.py
+-rw-r--r--   0        0        0      119 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_invoice_type.py
+-rw-r--r--   0        0        0      923 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_link_access_mode_request.py
+-rw-r--r--   0        0        0      130 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_link_access_mode_response.py
+-rw-r--r--   0        0        0      123 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_link_refresh_rate.py
+-rw-r--r--   0        0        0     1144 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_link_status.py
+-rw-r--r--   0        0        0      869 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_loan_data_fee_type.py
+-rw-r--r--   0        0        0      513 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_loan_data_interest_rate_type.py
+-rw-r--r--   0        0        0      636 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_intent_holder_type_pse.py
+-rw-r--r--   0        0        0     1196 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_intent_status.py
+-rw-r--r--   0        0        0      728 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_link_allowed_payment_method.py
+-rw-r--r--   0        0        0      711 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_link_provider.py
+-rw-r--r--   0        0        0      981 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_links_status.py
+-rw-r--r--   0        0        0      682 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payment_transaction_type.py
+-rw-r--r--   0        0        0      571 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payments_country.py
+-rw-r--r--   0        0        0      586 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_payments_currency.py
+-rw-r--r--   0        0        0      416 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_receivable_transaction_fee_type.py
+-rw-r--r--   0        0        0      930 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_receivable_transaction_status.py
+-rw-r--r--   0        0        0      133 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_receivable_transaction_type.py
+-rw-r--r--   0        0        0     2023 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_category.py
+-rw-r--r--   0        0        0      513 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_frequency.py
+-rw-r--r--   0        0        0      552 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_payment_type.py
+-rw-r--r--   0        0        0      760 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_tax_compliance_status_outcome.py
+-rw-r--r--   0        0        0      526 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_payment_status.py
+-rw-r--r--   0        0        0      544 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_receiver_nationality.py
+-rw-r--r--   0        0        0      735 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_type.py
+-rw-r--r--   0        0        0      129 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_transaction_bill_status.py
+-rw-r--r--   0        0        0      127 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_transaction_category.py
+-rw-r--r--   0        0        0      125 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_transaction_status.py
+-rw-r--r--   0        0        0      130 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_transaction_subcategory.py
+-rw-r--r--   0        0        0      123 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/enum_transaction_type.py
+-rw-r--r--   0        0        0     2117 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/equity_statement_business.py
+-rw-r--r--   0        0        0     1137 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/equity_statement_individual.py
+-rw-r--r--   0        0        0     2410 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/eyod_income_verification_body_request.py
+-rw-r--r--   0        0        0     1525 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/gross_income_individual.py
+-rw-r--r--   0        0        0     1067 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_bank_account_information_pse.py
+-rw-r--r--   0        0        0     1089 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_bank_account_pse.py
+-rw-r--r--   0        0        0     1045 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_business_pse.py
+-rw-r--r--   0        0        0     1179 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_business_response_pse.py
+-rw-r--r--   0        0        0     1189 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_business_ofpi.py
+-rw-r--r--   0        0        0     1073 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_business_ofpi_response.py
+-rw-r--r--   0        0        0      935 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_business_pse.py
+-rw-r--r--   0        0        0      993 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_business_pse_response.py
+-rw-r--r--   0        0        0     1290 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_individual_ofpi.py
+-rw-r--r--   0        0        0     1174 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_information_individual_ofpi_response.py
+-rw-r--r--   0        0        0     1043 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_response_ofpi.py
+-rw-r--r--   0        0        0      402 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/holder_response_ofpi_information.py
+-rw-r--r--   0        0        0     4077 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/income.py
+-rw-r--r--   0        0        0     4769 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/income_streams_body.py
+-rw-r--r--   0        0        0     1666 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/incomes_paginated_response.py
+-rw-r--r--   0        0        0     3939 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution.py
+-rw-r--r--   0        0        0     1205 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution_account.py
+-rw-r--r--   0        0        0     1989 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution_down_error.py
+-rw-r--r--   0        0        0     2062 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution_form_field.py
+-rw-r--r--   0        0        0     1894 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution_inactive_error.py
+-rw-r--r--   0        0        0     2011 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institution_unavailable_error.py
+-rw-r--r--   0        0        0      937 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institutions_feature.py
+-rw-r--r--   0        0        0     1937 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institutions_form_field.py
+-rw-r--r--   0        0        0     1513 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institutions_form_field_values.py
+-rw-r--r--   0        0        0     1691 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/institutions_paginated_response.py
+-rw-r--r--   0        0        0     2002 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invalid_access_mode.py
+-rw-r--r--   0        0        0     1936 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invalid_link_error.py
+-rw-r--r--   0        0        0     1967 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invalid_period_error.py
+-rw-r--r--   0        0        0     2666 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio.py
+-rw-r--r--   0        0        0     4088 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument.py
+-rw-r--r--   0        0        0     1056 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_fees.py
+-rw-r--r--   0        0        0     1465 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_interest_rate.py
+-rw-r--r--   0        0        0     1008 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_public_id.py
+-rw-r--r--   0        0        0      952 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py
+-rw-r--r--   0        0        0     1751 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/investments_portfolios_paginated_response.py
+-rw-r--r--   0        0        0     2518 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_detail_dian.py
+-rw-r--r--   0        0        0     1418 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_detail_retained_tax_sat.py
+-rw-r--r--   0        0        0     3178 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_detail_sat.py
+-rw-r--r--   0        0        0     7893 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_dian.py
+-rw-r--r--   0        0        0     2326 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_sender_details_dian.py
+-rw-r--r--   0        0        0     1066 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_warnings_dian.py
+-rw-r--r--   0        0        0      925 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_warnings_sat.py
+-rw-r--r--   0        0        0     9760 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoice_with_id_sat.py
+-rw-r--r--   0        0        0     2919 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payments_dian.py
+-rw-r--r--   0        0        0     2063 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payments_related_documents_dian.py
+-rw-r--r--   0        0        0     2024 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payments_related_documents_sat.py
+-rw-r--r--   0        0        0     3037 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payments_sat.py
+-rw-r--r--   0        0        0     2066 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payroll_dian.py
+-rw-r--r--   0        0        0     1782 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_payroll_sat.py
+-rw-r--r--   0        0        0     2343 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_receiver_details_dian.py
+-rw-r--r--   0        0        0     1809 2023-05-12 23:08:15.682101 fern_belvo-0.0.27/src/belvo/types/invoices_response_paginated_response.py
+-rw-r--r--   0        0        0      260 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/invoices_response_paginated_response_results_item.py
+-rw-r--r--   0        0        0     1249 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_invalid_credentials.py
+-rw-r--r--   0        0        0     1227 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_invalid_token.py
+-rw-r--r--   0        0        0     1257 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_login_error.py
+-rw-r--r--   0        0        0     1243 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_payment_error.py
+-rw-r--r--   0        0        0     1289 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_session_expired.py
+-rw-r--r--   0        0        0     1261 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/last_error_two_factor.py
+-rw-r--r--   0        0        0     2833 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/link.py
+-rw-r--r--   0        0        0      554 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/list_payment_links_request_ordering.py
+-rw-r--r--   0        0        0      521 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/list_payment_links_request_status.py
+-rw-r--r--   0        0        0      356 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/list_tax_declarations_response.py
+-rw-r--r--   0        0        0      586 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/list_tax_returns_response.py
+-rw-r--r--   0        0        0     2699 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/login_error.py
+-rw-r--r--   0        0        0      913 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/needs_redirect_content.py
+-rw-r--r--   0        0        0      923 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/needs_redirect_content_pse.py
+-rw-r--r--   0        0        0     1588 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/net_income_individual.py
+-rw-r--r--   0        0        0     1660 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_ofpi.py
+-rw-r--r--   0        0        0     2256 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py
+-rw-r--r--   0        0        0     1673 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_pse.py
+-rw-r--r--   0        0        0     2850 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_pse_type.py
+-rw-r--r--   0        0        0     1665 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_credentials_required_pse.py
+-rw-r--r--   0        0        0     2840 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_credentials_required_pse_type.py
+-rw-r--r--   0        0        0     1676 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_customer_bank_accounts_pse.py
+-rw-r--r--   0        0        0     2850 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py
+-rw-r--r--   0        0        0     1595 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_needs_redirect_pse.py
+-rw-r--r--   0        0        0     2780 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_needs_redirect_pse_type.py
+-rw-r--r--   0        0        0     1573 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_failed.py
+-rw-r--r--   0        0        0     2179 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_failed_type.py
+-rw-r--r--   0        0        0     1700 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information.py
+-rw-r--r--   0        0        0     1874 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_pse.py
+-rw-r--r--   0        0        0     2890 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_pse_type.py
+-rw-r--r--   0        0        0     2256 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_type.py
+-rw-r--r--   0        0        0     1606 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_processing.py
+-rw-r--r--   0        0        0     2207 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_processing_type.py
+-rw-r--r--   0        0        0     1598 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_succeeded.py
+-rw-r--r--   0        0        0     2200 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_succeeded_type.py
+-rw-r--r--   0        0        0     2128 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_token_required_pse.py
+-rw-r--r--   0        0        0     2780 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_display_token_required_pse_type.py
+-rw-r--r--   0        0        0     1545 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_needs_redirect.py
+-rw-r--r--   0        0        0     2130 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/next_step_needs_redirect_type.py
+-rw-r--r--   0        0        0     1531 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/non_taxable_income_individual.py
+-rw-r--r--   0        0        0     1703 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/not_found_error_body.py
+-rw-r--r--   0        0        0     2545 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/owner.py
+-rw-r--r--   0        0        0     1584 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/owner_document_id.py
+-rw-r--r--   0        0        0     1661 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/owners_paginated_response.py
+-rw-r--r--   0        0        0     1596 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/paginated_response_link.py
+-rw-r--r--   0        0        0     1798 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/patch_body.py
+-rw-r--r--   0        0        0     1479 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/patch_body_without_save_data.py
+-rw-r--r--   0        0        0      241 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/patch_invoices_response_item.py
+-rw-r--r--   0        0        0      876 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/patch_payment_intents_body_pse.py
+-rw-r--r--   0        0        0     2677 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/patch_payment_method_details_pse.py
+-rw-r--r--   0        0        0     2302 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_institution.py
+-rw-r--r--   0        0        0     4025 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_ofpi.py
+-rw-r--r--   0        0        0      846 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_ofpi_next_step.py
+-rw-r--r--   0        0        0      462 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_ofpi_payment_method_details.py
+-rw-r--r--   0        0        0     1733 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_paginated_response.py
+-rw-r--r--   0        0        0     1549 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py
+-rw-r--r--   0        0        0     1551 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py
+-rw-r--r--   0        0        0     2222 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0     1013 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py
+-rw-r--r--   0        0        0     1030 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py
+-rw-r--r--   0        0        0      983 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_pse.py
+-rw-r--r--   0        0        0     4050 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_pse.py
+-rw-r--r--   0        0        0      656 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_pse_last_error.py
+-rw-r--r--   0        0        0      933 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intent_pse_next_step.py
+-rw-r--r--   0        0        0     1644 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intents_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0      995 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_intents_payment_method_details_pse.py
+-rw-r--r--   0        0        0     1499 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_callback_urls.py
+-rw-r--r--   0        0        0     1408 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_callback_urls_response.py
+-rw-r--r--   0        0        0     2547 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_list_ofpi.py
+-rw-r--r--   0        0        0     2546 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_list_pse.py
+-rw-r--r--   0        0        0     2331 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_ofpi.py
+-rw-r--r--   0        0        0     1801 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_paginated_response.py
+-rw-r--r--   0        0        0      287 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_paginated_response_results_item.py
+-rw-r--r--   0        0        0     2326 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_link_pse.py
+-rw-r--r--   0        0        0     1244 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_links_payment_method_details_body_ofpi.py
+-rw-r--r--   0        0        0     1646 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_links_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0     1021 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_details_ofpi.py
+-rw-r--r--   0        0        0      980 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_details_pse.py
+-rw-r--r--   0        0        0     1530 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py
+-rw-r--r--   0        0        0     1256 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_information_body_ofpi.py
+-rw-r--r--   0        0        0     1390 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_information_body_pse.py
+-rw-r--r--   0        0        0     1013 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_information_details_pse.py
+-rw-r--r--   0        0        0      967 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_information_ofpi.py
+-rw-r--r--   0        0        0     1043 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_method_information_pse.py
+-rw-r--r--   0        0        0     2247 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_transaction.py
+-rw-r--r--   0        0        0      313 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_transaction_payer.py
+-rw-r--r--   0        0        0     1527 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payment_webhook.py
+-rw-r--r--   0        0        0     1742 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payments_institutions_paginated_response.py
+-rw-r--r--   0        0        0     1742 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payments_transactions_paginated_response.py
+-rw-r--r--   0        0        0     1471 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payments_way.py
+-rw-r--r--   0        0        0     1708 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/payments_webhooks_paginated_response.py
+-rw-r--r--   0        0        0     1072 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/pension_income_statement_individual.py
+-rw-r--r--   0        0        0      817 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/providers_pse.py
+-rw-r--r--   0        0        0     2957 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/receivables_transaction.py
+-rw-r--r--   0        0        0     1042 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/receivables_transaction_account.py
+-rw-r--r--   0        0        0     1065 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/receivables_transaction_number_of_installments.py
+-rw-r--r--   0        0        0     1750 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/receivables_transactions_paginated_response.py
+-rw-r--r--   0        0        0     1026 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/recevables_transaction_fees.py
+-rw-r--r--   0        0        0     1242 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/recurring_expense_source_transaction.py
+-rw-r--r--   0        0        0     2895 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/recurring_expenses.py
+-rw-r--r--   0        0        0     1735 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/recurring_expenses_paginated_response.py
+-rw-r--r--   0        0        0     1120 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/reporting_id.py
+-rw-r--r--   0        0        0     2051 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/request_timeout_error_body.py
+-rw-r--r--   0        0        0     1454 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retention_breakdown.py
+-rw-r--r--   0        0        0      244 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retrieve_invoices_response_item.py
+-rw-r--r--   0        0        0      308 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retrieve_tax_declarations_response_item.py
+-rw-r--r--   0        0        0      307 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retrieve_tax_returns_request_body.py
+-rw-r--r--   0        0        0      457 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retrieve_tax_returns_response_item.py
+-rw-r--r--   0        0        0      235 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/retrieve_tax_status_response.py
+-rw-r--r--   0        0        0     1980 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights.py
+-rw-r--r--   0        0        0     3951 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_balance_metrics.py
+-rw-r--r--   0        0        0     3942 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_cashflow_metrics.py
+-rw-r--r--   0        0        0     1093 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_credit_card_metrics.py
+-rw-r--r--   0        0        0     1369 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_loans_metrics.py
+-rw-r--r--   0        0        0     1711 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_paginated_response.py
+-rw-r--r--   0        0        0     9169 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/risk_insights_transaction_metrics.py
+-rw-r--r--   0        0        0     1176 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/secret_keys.py
+-rw-r--r--   0        0        0     1694 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/secret_keys_paginated_response.py
+-rw-r--r--   0        0        0     2013 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/session_expired_error.py
+-rw-r--r--   0        0        0     1276 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/standard_request.py
+-rw-r--r--   0        0        0     2491 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_assessment_business.py
+-rw-r--r--   0        0        0     2771 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_assessment_individual.py
+-rw-r--r--   0        0        0     1788 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_compliance_status.py
+-rw-r--r--   0        0        0     1748 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_compliance_status_paginated_response.py
+-rw-r--r--   0        0        0     2291 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_declaration_business.py
+-rw-r--r--   0        0        0     1755 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_declaration_business_paginated.py
+-rw-r--r--   0        0        0     2281 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_declaration_individual.py
+-rw-r--r--   0        0        0     1765 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_declaration_individual_paginated.py
+-rw-r--r--   0        0        0     1666 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_payer_information_business.py
+-rw-r--r--   0        0        0     1489 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_payer_information_individual.py
+-rw-r--r--   0        0        0     3880 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_retentions.py
+-rw-r--r--   0        0        0     1716 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_retentions_paginated_response.py
+-rw-r--r--   0        0        0      129 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_return_business.py
+-rw-r--r--   0        0        0      136 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_return_business_monthly.py
+-rw-r--r--   0        0        0      129 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_return_personal.py
+-rw-r--r--   0        0        0      136 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_return_personal_monthly.py
+-rw-r--r--   0        0        0      146 2023-05-12 23:08:15.686101 fern_belvo-0.0.27/src/belvo/types/tax_returns_business_monthly_paginated.py
+-rw-r--r--   0        0        0      139 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_returns_business_paginated.py
+-rw-r--r--   0        0        0     2175 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_returns_monthly_request.py
+-rw-r--r--   0        0        0      146 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_returns_personal_monthly_paginated.py
+-rw-r--r--   0        0        0      139 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_returns_personal_paginated.py
+-rw-r--r--   0        0        0     1967 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_returns_yearly_request.py
+-rw-r--r--   0        0        0     1089 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_address_between_street_dian.py
+-rw-r--r--   0        0        0     1029 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_address_between_street_sat.py
+-rw-r--r--   0        0        0     2076 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_address_dian.py
+-rw-r--r--   0        0        0     1919 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_address_sat.py
+-rw-r--r--   0        0        0     3269 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_dian.py
+-rw-r--r--   0        0        0     1728 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_economic_activity_dian.py
+-rw-r--r--   0        0        0     1328 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_economic_activity_sat.py
+-rw-r--r--   0        0        0     1550 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_obligations_dian.py
+-rw-r--r--   0        0        0     1357 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_obligations_sat.py
+-rw-r--r--   0        0        0     1784 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_paginated_response.py
+-rw-r--r--   0        0        0      247 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_paginated_response_results_item.py
+-rw-r--r--   0        0        0     1179 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_regimens_dian.py
+-rw-r--r--   0        0        0     1048 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_regimens_sat.py
+-rw-r--r--   0        0        0     3194 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_sat.py
+-rw-r--r--   0        0        0     2648 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_tax_payer_information_dian.py
+-rw-r--r--   0        0        0     2672 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/tax_status_tax_payer_information_sat.py
+-rw-r--r--   0        0        0     2428 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/token_required_response.py
+-rw-r--r--   0        0        0     1605 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/token_required_response_token_generation_data.py
+-rw-r--r--   0        0        0     2133 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/too_many_sessions_error.py
+-rw-r--r--   0        0        0     3391 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction.py
+-rw-r--r--   0        0        0     1052 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction_bank_account_body_pse.py
+-rw-r--r--   0        0        0      138 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction_bank_account_ofpi.py
+-rw-r--r--   0        0        0      325 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction_bank_account_pse.py
+-rw-r--r--   0        0        0     1689 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction_credit_card_data.py
+-rw-r--r--   0        0        0     1049 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transaction_merchant_data.py
+-rw-r--r--   0        0        0     1691 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transactions_paginated_response.py
+-rw-r--r--   0        0        0     2001 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/transactions_request.py
+-rw-r--r--   0        0        0     1945 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/unauthorized_error_body.py
+-rw-r--r--   0        0        0     2077 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/unconfirmed_link_error.py
+-rw-r--r--   0        0        0     2013 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/unexpected_error.py
+-rw-r--r--   0        0        0     2032 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/unsupported_operation_error.py
+-rw-r--r--   0        0        0     2657 2023-05-12 23:08:15.690101 fern_belvo-0.0.27/src/belvo/types/validation_error.py
+-rw-r--r--   0        0        0     3060 1970-01-01 00:00:00.000000 fern_belvo-0.0.27/PKG-INFO
```

### Comparing `fern_belvo-0.0.25/README.md` & `fern_belvo-0.0.27/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -24,21 +24,19 @@
 
 belvo_client = Belvo(
     secret_id="YOUR_SECRET_ID",
     secret_password="YOUR_SECRET_PASSWORD",
 )
 
 link = belvo_client.links.register_link(
-    request=belvo.LinksRequest(
-        institution="banamex_mx_retail",
-        username="username",
-        password="password",
-        accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
-        credentialsStorage="30d",
-    )
+    institution="banamex_mx_retail",
+    username="username",
+    password="password",
+    accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
+    credentialsStorage="30d",
 )
 
 print(link)
 ```
 
 ## Async client
 
@@ -51,21 +49,19 @@
 belvo_client = AsyncBelvo(
     secret_id="YOUR_SECRET_ID",
     secret_password="YOUR_SECRET_PASSWORD",
 )
 
 async def get_link() -> None:
     link = await belvo_client.links.register_link({
-        body=belvo.LinksRequest(
-            institution="banamex_mx_retail",
-            username="username",
-            password="password",
-            accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
-            credentialsStorage="30d,
-        )
+        institution="banamex_mx_retail",
+        username="username",
+        password="password",
+        accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
+        credentialsStorage="30d,
     })
 
     print(link)
 
 asyncio.run(get_link())
 ```
```

### Comparing `fern_belvo-0.0.25/src/belvo/__init__.py` & `fern_belvo-0.0.27/src/belvo/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -56,15 +56,14 @@
     AnnualIncomeStatementBusiness,
     AnnualIncomeStatementIndividual,
     AnnualTotalsIndividual,
     AsynchronousAccepted202,
     BadRequestErrorBodyItem,
     Balance,
     BalancesPaginatedResponse,
-    BalancesRequest,
     BankAccountBusinessPse,
     BankAccountDetailsOfpi,
     BankAccountDetailsOfpiPix,
     BankAccountDetailsOpenFinance,
     BankAccountDetailsOpenFinancePix,
     BankAccountHolderRequestOfpi,
     BankAccountHolderRequestOfpiInformation,
@@ -78,15 +77,14 @@
     BeneficiaryBankAccountOfpi,
     BeneficiaryBankAccountOfpiDetails,
     BeneficiaryBankAccountPse,
     Categorization,
     CategorizationBody,
     CategorizationBodyRequest,
     CategorizationMerchantData,
-    ChangeAccessMode,
     Charge,
     ChargePaymentMethodDetails,
     ChargePaymentMethodDetailsOfpi,
     ChargePaymentMethodDetailsOfpiContent,
     ChargePaymentMethodDetailsPse,
     ChargePaymentMethodDetailsPseContent,
     ChargeStatus,
@@ -135,15 +133,14 @@
     EmploymentRecord,
     EmploymentRecordDetail,
     EmploymentRecordDocumentId,
     EmploymentRecordEmploymentStatusUpdates,
     EmploymentRecordEntitlement,
     EmploymentRecordFile,
     EmploymentRecordPersonalData,
-    EmploymentRecordRequest,
     EmploymentRecordSocialSecuritySummary,
     EmploymentRecordsPaginatedResponse,
     EnumAccountCategory,
     EnumBankAccountHolderTypeOfpi,
     EnumBankAccountHolderTypePse,
     EnumBankAccountPixAccountTypeOfpi,
     EnumCategorizationAccountCategory,
@@ -219,15 +216,14 @@
     HolderInformationBusinessPseResponse,
     HolderInformationIndividualOfpi,
     HolderInformationIndividualOfpiResponse,
     HolderResponseOfpi,
     HolderResponseOfpiInformation,
     Income,
     IncomesPaginatedResponse,
-    IncomesRequest,
     IncomeStreamsBody,
     Institution,
     InstitutionAccount,
     InstitutionDownError,
     InstitutionFormField,
     InstitutionInactiveError,
     InstitutionsFeature,
@@ -253,29 +249,26 @@
     InvoicesPaymentsDian,
     InvoicesPaymentsRelatedDocumentsDian,
     InvoicesPaymentsRelatedDocumentsSat,
     InvoicesPaymentsSat,
     InvoicesPayrollDian,
     InvoicesPayrollSat,
     InvoicesReceiverDetailsDian,
-    InvoicesRequest,
     InvoicesResponsePaginatedResponse,
     InvoicesResponsePaginatedResponseResultsItem,
     InvoiceWarningsDian,
     InvoiceWarningsSat,
     InvoiceWithIdSat,
     LastErrorInvalidCredentials,
     LastErrorInvalidToken,
     LastErrorLoginError,
     LastErrorPaymentError,
     LastErrorSessionExpired,
     LastErrorTwoFactor,
     Link,
-    LinksPutRequest,
-    LinksRequest,
     ListPaymentLinksRequestOrdering,
     ListPaymentLinksRequestStatus,
     ListTaxDeclarationsResponse,
     ListTaxReturnsResponse,
     LoginError,
     NeedsRedirectContent,
     NeedsRedirectContentPse,
@@ -358,20 +351,18 @@
     PaymentWebhook,
     PensionIncomeStatementIndividual,
     ProvidersPse,
     ReceivablesTransaction,
     ReceivablesTransactionAccount,
     ReceivablesTransactionNumberOfInstallments,
     ReceivablesTransactionsPaginatedResponse,
-    ReceivableTransactionRequest,
     RecevablesTransactionFees,
     RecurringExpenses,
     RecurringExpenseSourceTransaction,
     RecurringExpensesPaginatedResponse,
-    RecurringExpensesRequest,
     ReportingId,
     RequestTimeoutErrorBody,
     RetentionBreakdown,
     RetrieveInvoicesResponseItem,
     RetrieveTaxDeclarationsResponseItem,
     RetrieveTaxReturnsRequestBody,
     RetrieveTaxReturnsResponseItem,
@@ -387,25 +378,22 @@
     SecretKeysPaginatedResponse,
     SessionExpiredError,
     StandardRequest,
     TaxAssessmentBusiness,
     TaxAssessmentIndividual,
     TaxComplianceStatus,
     TaxComplianceStatusPaginatedResponse,
-    TaxComplianceStatusRequest,
     TaxDeclarationBusiness,
     TaxDeclarationBusinessPaginated,
     TaxDeclarationIndividual,
     TaxDeclarationIndividualPaginated,
-    TaxDeclarationsRequest,
     TaxPayerInformationBusiness,
     TaxPayerInformationIndividual,
     TaxRetentions,
     TaxRetentionsPaginatedResponse,
-    TaxRetentionsRequest,
     TaxReturnBusiness,
     TaxReturnBusinessMonthly,
     TaxReturnPersonal,
     TaxReturnPersonalMonthly,
     TaxReturnsBusinessMonthlyPaginated,
     TaxReturnsBusinessPaginated,
     TaxReturnsMonthlyRequest,
@@ -421,15 +409,14 @@
     TaxStatusEconomicActivitySat,
     TaxStatusObligationsDian,
     TaxStatusObligationsSat,
     TaxStatusPaginatedResponse,
     TaxStatusPaginatedResponseResultsItem,
     TaxStatusRegimensDian,
     TaxStatusRegimensSat,
-    TaxStatusRequest,
     TaxStatusSat,
     TaxStatusTaxPayerInformationDian,
     TaxStatusTaxPayerInformationSat,
     TokenRequiredResponse,
     TokenRequiredResponseTokenGenerationData,
     TooManySessionsError,
     Transaction,
@@ -464,15 +451,14 @@
     "AnnualIncomeStatementIndividual",
     "AnnualTotalsIndividual",
     "AsynchronousAccepted202",
     "BadRequestError",
     "BadRequestErrorBodyItem",
     "Balance",
     "BalancesPaginatedResponse",
-    "BalancesRequest",
     "BankAccountBusinessPse",
     "BankAccountDetailsOfpi",
     "BankAccountDetailsOfpiPix",
     "BankAccountDetailsOpenFinance",
     "BankAccountDetailsOpenFinancePix",
     "BankAccountHolderRequestOfpi",
     "BankAccountHolderRequestOfpiInformation",
@@ -487,15 +473,14 @@
     "BeneficiaryBankAccountOfpi",
     "BeneficiaryBankAccountOfpiDetails",
     "BeneficiaryBankAccountPse",
     "Categorization",
     "CategorizationBody",
     "CategorizationBodyRequest",
     "CategorizationMerchantData",
-    "ChangeAccessMode",
     "Charge",
     "ChargePaymentMethodDetails",
     "ChargePaymentMethodDetailsOfpi",
     "ChargePaymentMethodDetailsOfpiContent",
     "ChargePaymentMethodDetailsPse",
     "ChargePaymentMethodDetailsPseContent",
     "ChargeStatus",
@@ -544,15 +529,14 @@
     "EmploymentRecord",
     "EmploymentRecordDetail",
     "EmploymentRecordDocumentId",
     "EmploymentRecordEmploymentStatusUpdates",
     "EmploymentRecordEntitlement",
     "EmploymentRecordFile",
     "EmploymentRecordPersonalData",
-    "EmploymentRecordRequest",
     "EmploymentRecordSocialSecuritySummary",
     "EmploymentRecordsPaginatedResponse",
     "EnumAccountCategory",
     "EnumBankAccountHolderTypeOfpi",
     "EnumBankAccountHolderTypePse",
     "EnumBankAccountPixAccountTypeOfpi",
     "EnumCategorizationAccountCategory",
@@ -630,15 +614,14 @@
     "HolderInformationIndividualOfpi",
     "HolderInformationIndividualOfpiResponse",
     "HolderResponseOfpi",
     "HolderResponseOfpiInformation",
     "Income",
     "IncomeStreamsBody",
     "IncomesPaginatedResponse",
-    "IncomesRequest",
     "Institution",
     "InstitutionAccount",
     "InstitutionDownError",
     "InstitutionFormField",
     "InstitutionInactiveError",
     "InstitutionUnavailableError",
     "InstitutionsFeature",
@@ -667,26 +650,23 @@
     "InvoicesPaymentsDian",
     "InvoicesPaymentsRelatedDocumentsDian",
     "InvoicesPaymentsRelatedDocumentsSat",
     "InvoicesPaymentsSat",
     "InvoicesPayrollDian",
     "InvoicesPayrollSat",
     "InvoicesReceiverDetailsDian",
-    "InvoicesRequest",
     "InvoicesResponsePaginatedResponse",
     "InvoicesResponsePaginatedResponseResultsItem",
     "LastErrorInvalidCredentials",
     "LastErrorInvalidToken",
     "LastErrorLoginError",
     "LastErrorPaymentError",
     "LastErrorSessionExpired",
     "LastErrorTwoFactor",
     "Link",
-    "LinksPutRequest",
-    "LinksRequest",
     "ListPaymentLinksRequestOrdering",
     "ListPaymentLinksRequestStatus",
     "ListTaxDeclarationsResponse",
     "ListTaxReturnsResponse",
     "LoginError",
     "NeedsRedirectContent",
     "NeedsRedirectContentPse",
@@ -767,24 +747,22 @@
     "PaymentsInstitutionsPaginatedResponse",
     "PaymentsTransactionsPaginatedResponse",
     "PaymentsWay",
     "PaymentsWebhooksPaginatedResponse",
     "PensionIncomeStatementIndividual",
     "PreconditionError",
     "ProvidersPse",
-    "ReceivableTransactionRequest",
     "ReceivablesTransaction",
     "ReceivablesTransactionAccount",
     "ReceivablesTransactionNumberOfInstallments",
     "ReceivablesTransactionsPaginatedResponse",
     "RecevablesTransactionFees",
     "RecurringExpenseSourceTransaction",
     "RecurringExpenses",
     "RecurringExpensesPaginatedResponse",
-    "RecurringExpensesRequest",
     "ReportingId",
     "RequestTimeoutError",
     "RequestTimeoutErrorBody",
     "RetentionBreakdown",
     "RetrieveInvoicesResponseItem",
     "RetrieveTaxDeclarationsResponseItem",
     "RetrieveTaxReturnsRequestBody",
@@ -801,25 +779,22 @@
     "SecretKeysPaginatedResponse",
     "SessionExpiredError",
     "StandardRequest",
     "TaxAssessmentBusiness",
     "TaxAssessmentIndividual",
     "TaxComplianceStatus",
     "TaxComplianceStatusPaginatedResponse",
-    "TaxComplianceStatusRequest",
     "TaxDeclarationBusiness",
     "TaxDeclarationBusinessPaginated",
     "TaxDeclarationIndividual",
     "TaxDeclarationIndividualPaginated",
-    "TaxDeclarationsRequest",
     "TaxPayerInformationBusiness",
     "TaxPayerInformationIndividual",
     "TaxRetentions",
     "TaxRetentionsPaginatedResponse",
-    "TaxRetentionsRequest",
     "TaxReturnBusiness",
     "TaxReturnBusinessMonthly",
     "TaxReturnPersonal",
     "TaxReturnPersonalMonthly",
     "TaxReturnsBusinessMonthlyPaginated",
     "TaxReturnsBusinessPaginated",
     "TaxReturnsMonthlyRequest",
@@ -835,15 +810,14 @@
     "TaxStatusEconomicActivitySat",
     "TaxStatusObligationsDian",
     "TaxStatusObligationsSat",
     "TaxStatusPaginatedResponse",
     "TaxStatusPaginatedResponseResultsItem",
     "TaxStatusRegimensDian",
     "TaxStatusRegimensSat",
-    "TaxStatusRequest",
     "TaxStatusSat",
     "TaxStatusTaxPayerInformationDian",
     "TaxStatusTaxPayerInformationSat",
     "TokenRequiredResponse",
     "TokenRequiredResponseTokenGenerationData",
     "TooManySessionsError",
     "Transaction",
```

### Comparing `fern_belvo-0.0.25/src/belvo/client.py` & `fern_belvo-0.0.27/src/belvo/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/core/datetime_utils.py` & `fern_belvo-0.0.27/src/belvo/core/datetime_utils.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/core/jsonable_encoder.py` & `fern_belvo-0.0.27/src/belvo/core/jsonable_encoder.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/errors/__init__.py` & `fern_belvo-0.0.27/src/belvo/errors/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/__init__.py` & `fern_belvo-0.0.27/src/belvo/resources/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/accounts/client.py` & `fern_belvo-0.0.27/src/belvo/resources/accounts/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/balances/client.py` & `fern_belvo-0.0.27/src/belvo/resources/balances/client.py`

 * *Files 3% similar despite different names*

```diff
@@ -15,22 +15,24 @@
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.balance import Balance
 from ...types.balances_paginated_response import BalancesPaginatedResponse
-from ...types.balances_request import BalancesRequest
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.patch_body import PatchBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class BalancesClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -115,21 +117,37 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_balances(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: BalancesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        account: typing.Optional[str] = OMIT,
+        date_from: str,
+        date_to: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[Balance]:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "date_from": date_from, "date_to": date_to}
+        if account is not OMIT:
+            _request["account"] = account
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/balances"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[Balance], _response.json())  # type: ignore
@@ -338,22 +356,38 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_balances(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: BalancesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        account: typing.Optional[str] = OMIT,
+        date_from: str,
+        date_to: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[Balance]:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "date_from": date_from, "date_to": date_to}
+        if account is not OMIT:
+            _request["account"] = account
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/balances"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[Balance], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/bank_accounts/client.py` & `fern_belvo-0.0.27/src/belvo/resources/bank_accounts/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/categorization/client.py` & `fern_belvo-0.0.27/src/belvo/resources/categorization/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/customers/client.py` & `fern_belvo-0.0.27/src/belvo/resources/customers/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/employment_records/client.py` & `fern_belvo-0.0.27/src/belvo/resources/employment_records/client.py`

 * *Files 3% similar despite different names*

```diff
@@ -14,22 +14,24 @@
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.employment_record import EmploymentRecord
-from ...types.employment_record_request import EmploymentRecordRequest
 from ...types.employment_records_paginated_response import EmploymentRecordsPaginatedResponse
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class EmploymentRecordsClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -65,21 +67,28 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_employment_record_details(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: EmploymentRecordRequest,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[EmploymentRecord]:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/employment-records"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[EmploymentRecord], _response.json())  # type: ignore
@@ -198,22 +207,29 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_employment_record_details(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: EmploymentRecordRequest,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[EmploymentRecord]:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/employment-records"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[EmploymentRecord], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/income_verification/client.py` & `fern_belvo-0.0.27/src/belvo/resources/income_verification/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/incomes/client.py` & `fern_belvo-0.0.27/src/belvo/resources/incomes/client.py`

 * *Files 8% similar despite different names*

```diff
@@ -13,24 +13,28 @@
 from ...errors.bad_request_error import BadRequestError
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
+from ...types.enum_income_minimum_confidence_level_request import EnumIncomeMinimumConfidenceLevelRequest
+from ...types.enum_invoice_allowed_income_types_request import EnumInvoiceAllowedIncomeTypesRequest
 from ...types.income import Income
 from ...types.incomes_paginated_response import IncomesPaginatedResponse
-from ...types.incomes_request import IncomesRequest
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.patch_body import PatchBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class IncomesClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -75,21 +79,44 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_income(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: IncomesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        allowed_income_types: typing.Optional[typing.List[EnumInvoiceAllowedIncomeTypesRequest]] = OMIT,
+        minimum_confidence_level: typing.Optional[EnumIncomeMinimumConfidenceLevelRequest] = OMIT,
+        date_from: typing.Optional[str] = OMIT,
+        date_to: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> Income:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if allowed_income_types is not OMIT:
+            _request["allowed_income_types"] = allowed_income_types
+        if minimum_confidence_level is not OMIT:
+            _request["minimum_confidence_level"] = minimum_confidence_level
+        if date_from is not OMIT:
+            _request["date_from"] = date_from
+        if date_to is not OMIT:
+            _request["date_to"] = date_to
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/incomes"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Income, _response.json())  # type: ignore
@@ -258,22 +285,45 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_income(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: IncomesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        allowed_income_types: typing.Optional[typing.List[EnumInvoiceAllowedIncomeTypesRequest]] = OMIT,
+        minimum_confidence_level: typing.Optional[EnumIncomeMinimumConfidenceLevelRequest] = OMIT,
+        date_from: typing.Optional[str] = OMIT,
+        date_to: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> Income:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if allowed_income_types is not OMIT:
+            _request["allowed_income_types"] = allowed_income_types
+        if minimum_confidence_level is not OMIT:
+            _request["minimum_confidence_level"] = minimum_confidence_level
+        if date_from is not OMIT:
+            _request["date_from"] = date_from
+        if date_to is not OMIT:
+            _request["date_to"] = date_to
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/incomes"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Income, _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/institutions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/institutions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/investment_portfolios/client.py` & `fern_belvo-0.0.27/src/belvo/resources/investment_portfolios/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/invoices/client.py` & `fern_belvo-0.0.27/src/belvo/resources/invoices/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,25 +14,28 @@
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.detail_invoice_response import DetailInvoiceResponse
-from ...types.invoices_request import InvoicesRequest
+from ...types.enum_invoice_type import EnumInvoiceType
 from ...types.invoices_response_paginated_response import InvoicesResponsePaginatedResponse
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.patch_body import PatchBody
 from ...types.patch_invoices_response_item import PatchInvoicesResponseItem
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.retrieve_invoices_response_item import RetrieveInvoicesResponseItem
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class InvoicesClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -123,21 +126,40 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_invoices(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: InvoicesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        date_from: str,
+        date_to: str,
+        type: EnumInvoiceType,
+        attach_xml: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[RetrieveInvoicesResponseItem]:
+        _request: typing.Dict[str, typing.Any] = {
+            "link": link,
+            "date_from": date_from,
+            "date_to": date_to,
+            "type": type,
+        }
+        if attach_xml is not OMIT:
+            _request["attach_xml"] = attach_xml
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/invoices"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RetrieveInvoicesResponseItem], _response.json())  # type: ignore
@@ -348,22 +370,41 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_invoices(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: InvoicesRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        date_from: str,
+        date_to: str,
+        type: EnumInvoiceType,
+        attach_xml: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[RetrieveInvoicesResponseItem]:
+        _request: typing.Dict[str, typing.Any] = {
+            "link": link,
+            "date_from": date_from,
+            "date_to": date_to,
+            "type": type,
+        }
+        if attach_xml is not OMIT:
+            _request["attach_xml"] = attach_xml
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/invoices"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RetrieveInvoicesResponseItem], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/links/client.py` & `fern_belvo-0.0.27/src/belvo/resources/links/client.py`

 * *Files 14% similar despite different names*

```diff
@@ -12,25 +12,26 @@
 from ...environment import BelvoEnvironment
 from ...errors.bad_request_error import BadRequestError
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
-from ...types.change_access_mode import ChangeAccessMode
+from ...types.enum_link_access_mode_request import EnumLinkAccessModeRequest
 from ...types.link import Link
-from ...types.links_put_request import LinksPutRequest
-from ...types.links_request import LinksRequest
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.paginated_response_link import PaginatedResponseLink
 from ...types.patch_body_without_save_data import PatchBodyWithoutSaveData
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class LinksClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -105,21 +106,63 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def register_link(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: LinksRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        institution: str,
+        username: str,
+        password: typing.Optional[str] = OMIT,
+        external_id: typing.Optional[str] = OMIT,
+        username_2: typing.Optional[str] = OMIT,
+        username_3: typing.Optional[str] = OMIT,
+        password_2: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        access_mode: typing.Optional[EnumLinkAccessModeRequest] = OMIT,
+        fetch_historical: typing.Optional[bool] = OMIT,
+        credentials_storage: typing.Optional[str] = OMIT,
+        username_type: typing.Optional[str] = OMIT,
+        certificate: typing.Optional[str] = OMIT,
+        private_key: typing.Optional[str] = OMIT,
     ) -> Link:
+        _request: typing.Dict[str, typing.Any] = {"institution": institution, "username": username}
+        if password is not OMIT:
+            _request["password"] = password
+        if external_id is not OMIT:
+            _request["external_id"] = external_id
+        if username_2 is not OMIT:
+            _request["username2"] = username_2
+        if username_3 is not OMIT:
+            _request["username3"] = username_3
+        if password_2 is not OMIT:
+            _request["password2"] = password_2
+        if token is not OMIT:
+            _request["token"] = token
+        if access_mode is not OMIT:
+            _request["access_mode"] = access_mode
+        if fetch_historical is not OMIT:
+            _request["fetch_historical"] = fetch_historical
+        if credentials_storage is not OMIT:
+            _request["credentials_storage"] = credentials_storage
+        if username_type is not OMIT:
+            _request["username_type"] = username_type
+        if certificate is not OMIT:
+            _request["certificate"] = certificate
+        if private_key is not OMIT:
+            _request["private_key"] = private_key
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/links"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
@@ -212,21 +255,37 @@
 
     def update_link(
         self,
         id: str,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: LinksPutRequest,
+        password: str,
+        password_2: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        username_type: typing.Optional[str] = OMIT,
+        certificate: typing.Optional[str] = OMIT,
+        private_key: typing.Optional[str] = OMIT,
     ) -> Link:
+        _request: typing.Dict[str, typing.Any] = {"password": password}
+        if password_2 is not OMIT:
+            _request["password2"] = password_2
+        if token is not OMIT:
+            _request["token"] = token
+        if username_type is not OMIT:
+            _request["username_type"] = username_type
+        if certificate is not OMIT:
+            _request["certificate"] = certificate
+        if private_key is not OMIT:
+            _request["private_key"] = private_key
         _response = httpx.request(
             "PUT",
             urllib.parse.urljoin(f"{self._environment.value}/", f"api/links/{id}"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
@@ -256,21 +315,21 @@
 
     def change_link_access_mode(
         self,
         id: str,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: ChangeAccessMode,
+        access_mode: EnumLinkAccessModeRequest,
     ) -> Link:
         _response = httpx.request(
             "PATCH",
             urllib.parse.urljoin(f"{self._environment.value}/", f"api/links/{id}"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder({"access_mode": access_mode}),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
@@ -400,22 +459,64 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def register_link(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: LinksRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        institution: str,
+        username: str,
+        password: typing.Optional[str] = OMIT,
+        external_id: typing.Optional[str] = OMIT,
+        username_2: typing.Optional[str] = OMIT,
+        username_3: typing.Optional[str] = OMIT,
+        password_2: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        access_mode: typing.Optional[EnumLinkAccessModeRequest] = OMIT,
+        fetch_historical: typing.Optional[bool] = OMIT,
+        credentials_storage: typing.Optional[str] = OMIT,
+        username_type: typing.Optional[str] = OMIT,
+        certificate: typing.Optional[str] = OMIT,
+        private_key: typing.Optional[str] = OMIT,
     ) -> Link:
+        _request: typing.Dict[str, typing.Any] = {"institution": institution, "username": username}
+        if password is not OMIT:
+            _request["password"] = password
+        if external_id is not OMIT:
+            _request["external_id"] = external_id
+        if username_2 is not OMIT:
+            _request["username2"] = username_2
+        if username_3 is not OMIT:
+            _request["username3"] = username_3
+        if password_2 is not OMIT:
+            _request["password2"] = password_2
+        if token is not OMIT:
+            _request["token"] = token
+        if access_mode is not OMIT:
+            _request["access_mode"] = access_mode
+        if fetch_historical is not OMIT:
+            _request["fetch_historical"] = fetch_historical
+        if credentials_storage is not OMIT:
+            _request["credentials_storage"] = credentials_storage
+        if username_type is not OMIT:
+            _request["username_type"] = username_type
+        if certificate is not OMIT:
+            _request["certificate"] = certificate
+        if private_key is not OMIT:
+            _request["private_key"] = private_key
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/links"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
@@ -512,22 +613,38 @@
 
     async def update_link(
         self,
         id: str,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: LinksPutRequest,
+        password: str,
+        password_2: typing.Optional[str] = OMIT,
+        token: typing.Optional[str] = OMIT,
+        username_type: typing.Optional[str] = OMIT,
+        certificate: typing.Optional[str] = OMIT,
+        private_key: typing.Optional[str] = OMIT,
     ) -> Link:
+        _request: typing.Dict[str, typing.Any] = {"password": password}
+        if password_2 is not OMIT:
+            _request["password2"] = password_2
+        if token is not OMIT:
+            _request["token"] = token
+        if username_type is not OMIT:
+            _request["username_type"] = username_type
+        if certificate is not OMIT:
+            _request["certificate"] = certificate
+        if private_key is not OMIT:
+            _request["private_key"] = private_key
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "PUT",
                 urllib.parse.urljoin(f"{self._environment.value}/", f"api/links/{id}"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
@@ -557,22 +674,22 @@
 
     async def change_link_access_mode(
         self,
         id: str,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: ChangeAccessMode,
+        access_mode: EnumLinkAccessModeRequest,
     ) -> Link:
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "PATCH",
                 urllib.parse.urljoin(f"{self._environment.value}/", f"api/links/{id}"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder({"access_mode": access_mode}),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(Link, _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/owners/client.py` & `fern_belvo-0.0.27/src/belvo/resources/owners/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/payment_institutions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/payment_institutions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/payment_intents/client.py` & `fern_belvo-0.0.27/src/belvo/resources/payment_intents/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/payment_links/client.py` & `fern_belvo-0.0.27/src/belvo/resources/payment_links/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/payment_transactions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/payment_transactions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/payment_webhooks/client.py` & `fern_belvo-0.0.27/src/belvo/resources/payment_webhooks/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/receivable_transactions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/receivable_transactions/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -13,21 +13,23 @@
 from ...errors.bad_request_error import BadRequestError
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.precondition_error import PreconditionError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.not_found_error_body import NotFoundErrorBody
-from ...types.receivable_transaction_request import ReceivableTransactionRequest
 from ...types.receivables_transaction import ReceivablesTransaction
 from ...types.receivables_transactions_paginated_response import ReceivablesTransactionsPaginatedResponse
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class ReceivableTransactionsClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -98,21 +100,30 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_receivable_transactions(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: ReceivableTransactionRequest,
+        link: str,
+        date_from: str,
+        date_to: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> ReceivablesTransaction:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "date_from": date_from, "date_to": date_to}
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "receivables/transactions"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(ReceivablesTransaction, _response.json())  # type: ignore
@@ -262,22 +273,31 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_receivable_transactions(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: ReceivableTransactionRequest,
+        link: str,
+        date_from: str,
+        date_to: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> ReceivablesTransaction:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "date_from": date_from, "date_to": date_to}
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "receivables/transactions"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(ReceivablesTransaction, _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/recurring_expenses/client.py` & `fern_belvo-0.0.27/src/belvo/resources/recurring_expenses/client.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,20 +17,22 @@
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.patch_body import PatchBody
 from ...types.recurring_expenses import RecurringExpenses
 from ...types.recurring_expenses_paginated_response import RecurringExpensesPaginatedResponse
-from ...types.recurring_expenses_request import RecurringExpensesRequest
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.token_required_response import TokenRequiredResponse
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class RecurringExpensesClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -83,21 +85,34 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_recurring_expenses(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: RecurringExpensesRequest,
+        link: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
+        date_from: typing.Optional[str] = OMIT,
+        date_to: typing.Optional[str] = OMIT,
     ) -> typing.List[RecurringExpenses]:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
+        if date_from is not OMIT:
+            _request["date_from"] = date_from
+        if date_to is not OMIT:
+            _request["date_to"] = date_to
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/recurring-expenses"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RecurringExpenses], _response.json())  # type: ignore
@@ -274,22 +289,35 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_recurring_expenses(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: RecurringExpensesRequest,
+        link: str,
+        token: typing.Optional[str] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
+        date_from: typing.Optional[str] = OMIT,
+        date_to: typing.Optional[str] = OMIT,
     ) -> typing.List[RecurringExpenses]:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if token is not OMIT:
+            _request["token"] = token
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
+        if date_from is not OMIT:
+            _request["date_from"] = date_from
+        if date_to is not OMIT:
+            _request["date_to"] = date_to
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/recurring-expenses"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RecurringExpenses], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/risk_insights/client.py` & `fern_belvo-0.0.27/src/belvo/resources/risk_insights/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/secret_keys/client.py` & `fern_belvo-0.0.27/src/belvo/resources/secret_keys/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/tax_compliance_status/client.py` & `fern_belvo-0.0.27/src/belvo/resources/tax_compliance_status/client.py`

 * *Files 3% similar despite different names*

```diff
@@ -16,18 +16,20 @@
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.tax_compliance_status import TaxComplianceStatus
 from ...types.tax_compliance_status_paginated_response import TaxComplianceStatusPaginatedResponse
-from ...types.tax_compliance_status_request import TaxComplianceStatusRequest
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class TaxComplianceStatusClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -86,21 +88,28 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_tax_compliance_status(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: TaxComplianceStatusRequest,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> TaxComplianceStatus:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-compliance-status"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(TaxComplianceStatus, _response.json())  # type: ignore
@@ -238,22 +247,29 @@
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_tax_compliance_status(
         self,
         *,
         omit: typing.Optional[str] = None,
         fields: typing.Optional[str] = None,
-        request: TaxComplianceStatusRequest,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> TaxComplianceStatus:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-compliance-status"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(TaxComplianceStatus, _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/tax_declarations/client.py` & `fern_belvo-0.0.27/src/belvo/resources/tax_declarations/client.py`

 * *Files 6% similar despite different names*

```diff
@@ -17,18 +17,20 @@
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.detail_tax_declaration_response import DetailTaxDeclarationResponse
 from ...types.list_tax_declarations_response import ListTaxDeclarationsResponse
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.retrieve_tax_declarations_response_item import RetrieveTaxDeclarationsResponseItem
-from ...types.tax_declarations_request import TaxDeclarationsRequest
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class TaxDeclarationsClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -95,21 +97,34 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_tax_declarations(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxDeclarationsRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        year_from: str,
+        year_to: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[RetrieveTaxDeclarationsResponseItem]:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "year_from": year_from, "year_to": year_to}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-declarations"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RetrieveTaxDeclarationsResponseItem], _response.json())  # type: ignore
@@ -255,22 +270,35 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_tax_declarations(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxDeclarationsRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        year_from: str,
+        year_to: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[RetrieveTaxDeclarationsResponseItem]:
+        _request: typing.Dict[str, typing.Any] = {"link": link, "year_from": year_from, "year_to": year_to}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-declarations"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[RetrieveTaxDeclarationsResponseItem], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/tax_retentions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/tax_retentions/client.py`

 * *Files 6% similar despite different names*

```diff
@@ -12,22 +12,25 @@
 from ...environment import BelvoEnvironment
 from ...errors.bad_request_error import BadRequestError
 from ...errors.internal_server_error import InternalServerError
 from ...errors.not_found_error import NotFoundError
 from ...errors.request_timeout_error import RequestTimeoutError
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
+from ...types.enum_tax_retention_type import EnumTaxRetentionType
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.tax_retentions import TaxRetentions
 from ...types.tax_retentions_paginated_response import TaxRetentionsPaginatedResponse
-from ...types.tax_retentions_request import TaxRetentionsRequest
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class TaxRetentionsClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -78,21 +81,40 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_tax_retentions(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxRetentionsRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        date_from: str,
+        date_to: str,
+        type: EnumTaxRetentionType,
+        attach_xml: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[TaxRetentions]:
+        _request: typing.Dict[str, typing.Any] = {
+            "link": link,
+            "date_from": date_from,
+            "date_to": date_to,
+            "type": type,
+        }
+        if attach_xml is not OMIT:
+            _request["attach_xml"] = attach_xml
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-retentions"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[TaxRetentions], _response.json())  # type: ignore
@@ -222,22 +244,41 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_tax_retentions(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxRetentionsRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        date_from: str,
+        date_to: str,
+        type: EnumTaxRetentionType,
+        attach_xml: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> typing.List[TaxRetentions]:
+        _request: typing.Dict[str, typing.Any] = {
+            "link": link,
+            "date_from": date_from,
+            "date_to": date_to,
+            "type": type,
+        }
+        if attach_xml is not OMIT:
+            _request["attach_xml"] = attach_xml
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-retentions"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(typing.List[TaxRetentions], _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/tax_returns/client.py` & `fern_belvo-0.0.27/src/belvo/resources/tax_returns/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/resources/tax_status/client.py` & `fern_belvo-0.0.27/src/belvo/resources/tax_status/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,18 +17,20 @@
 from ...errors.unauthorized_error import UnauthorizedError
 from ...types.bad_request_error_body_item import BadRequestErrorBodyItem
 from ...types.detail_tax_status_response import DetailTaxStatusResponse
 from ...types.not_found_error_body import NotFoundErrorBody
 from ...types.request_timeout_error_body import RequestTimeoutErrorBody
 from ...types.retrieve_tax_status_response import RetrieveTaxStatusResponse
 from ...types.tax_status_paginated_response import TaxStatusPaginatedResponse
-from ...types.tax_status_request import TaxStatusRequest
 from ...types.unauthorized_error_body import UnauthorizedErrorBody
 from ...types.unexpected_error import UnexpectedError
 
+# this is used as the default value for optional parameters
+OMIT = typing.cast(typing.Any, ...)
+
 
 class TaxStatusClient:
     def __init__(
         self, *, environment: BelvoEnvironment = BelvoEnvironment.PRODUCTION, secret_id: str, secret_password: str
     ):
         self._environment = environment
         self._secret_id = secret_id
@@ -83,21 +85,32 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     def retrieve_tax_status(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxStatusRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> RetrieveTaxStatusResponse:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         _response = httpx.request(
             "POST",
             urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-status"),
             params={"omit": omit, "fields": fields},
-            json=jsonable_encoder(request),
+            json=jsonable_encoder(_request),
             auth=(self._secret_id, self._secret_password)
             if self._secret_id is not None and self._secret_password is not None
             else None,
             timeout=60,
         )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(RetrieveTaxStatusResponse, _response.json())  # type: ignore
@@ -231,22 +244,33 @@
         try:
             _response_json = _response.json()
         except JSONDecodeError:
             raise ApiError(status_code=_response.status_code, body=_response.text)
         raise ApiError(status_code=_response.status_code, body=_response_json)
 
     async def retrieve_tax_status(
-        self, *, omit: typing.Optional[str] = None, fields: typing.Optional[str] = None, request: TaxStatusRequest
+        self,
+        *,
+        omit: typing.Optional[str] = None,
+        fields: typing.Optional[str] = None,
+        link: str,
+        attach_pdf: typing.Optional[bool] = OMIT,
+        save_data: typing.Optional[bool] = OMIT,
     ) -> RetrieveTaxStatusResponse:
+        _request: typing.Dict[str, typing.Any] = {"link": link}
+        if attach_pdf is not OMIT:
+            _request["attach_pdf"] = attach_pdf
+        if save_data is not OMIT:
+            _request["save_data"] = save_data
         async with httpx.AsyncClient() as _client:
             _response = await _client.request(
                 "POST",
                 urllib.parse.urljoin(f"{self._environment.value}/", "api/tax-status"),
                 params={"omit": omit, "fields": fields},
-                json=jsonable_encoder(request),
+                json=jsonable_encoder(_request),
                 auth=(self._secret_id, self._secret_password)
                 if self._secret_id is not None and self._secret_password is not None
                 else None,
                 timeout=60,
             )
         if 200 <= _response.status_code < 300:
             return pydantic.parse_obj_as(RetrieveTaxStatusResponse, _response.json())  # type: ignore
```

### Comparing `fern_belvo-0.0.25/src/belvo/resources/transactions/client.py` & `fern_belvo-0.0.27/src/belvo/resources/transactions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/__init__.py` & `fern_belvo-0.0.27/src/belvo/types/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,15 +15,14 @@
 from .annual_income_statement_business import AnnualIncomeStatementBusiness
 from .annual_income_statement_individual import AnnualIncomeStatementIndividual
 from .annual_totals_individual import AnnualTotalsIndividual
 from .asynchronous_accepted_202 import AsynchronousAccepted202
 from .bad_request_error_body_item import BadRequestErrorBodyItem
 from .balance import Balance
 from .balances_paginated_response import BalancesPaginatedResponse
-from .balances_request import BalancesRequest
 from .bank_account_business_pse import BankAccountBusinessPse
 from .bank_account_details_ofpi import BankAccountDetailsOfpi
 from .bank_account_details_ofpi_pix import BankAccountDetailsOfpiPix
 from .bank_account_details_open_finance import BankAccountDetailsOpenFinance
 from .bank_account_details_open_finance_pix import BankAccountDetailsOpenFinancePix
 from .bank_account_holder_request_ofpi import BankAccountHolderRequestOfpi
 from .bank_account_holder_request_ofpi_information import BankAccountHolderRequestOfpiInformation
@@ -37,15 +36,14 @@
 from .beneficiary_bank_account_ofpi import BeneficiaryBankAccountOfpi
 from .beneficiary_bank_account_ofpi_details import BeneficiaryBankAccountOfpiDetails
 from .beneficiary_bank_account_pse import BeneficiaryBankAccountPse
 from .categorization import Categorization
 from .categorization_body import CategorizationBody
 from .categorization_body_request import CategorizationBodyRequest
 from .categorization_merchant_data import CategorizationMerchantData
-from .change_access_mode import ChangeAccessMode
 from .charge import Charge
 from .charge_payment_method_details import ChargePaymentMethodDetails
 from .charge_payment_method_details_ofpi import ChargePaymentMethodDetailsOfpi
 from .charge_payment_method_details_ofpi_content import ChargePaymentMethodDetailsOfpiContent
 from .charge_payment_method_details_pse import ChargePaymentMethodDetailsPse
 from .charge_payment_method_details_pse_content import ChargePaymentMethodDetailsPseContent
 from .charge_status import ChargeStatus
@@ -94,15 +92,14 @@
 from .employment_record import EmploymentRecord
 from .employment_record_detail import EmploymentRecordDetail
 from .employment_record_document_id import EmploymentRecordDocumentId
 from .employment_record_employment_status_updates import EmploymentRecordEmploymentStatusUpdates
 from .employment_record_entitlement import EmploymentRecordEntitlement
 from .employment_record_file import EmploymentRecordFile
 from .employment_record_personal_data import EmploymentRecordPersonalData
-from .employment_record_request import EmploymentRecordRequest
 from .employment_record_social_security_summary import EmploymentRecordSocialSecuritySummary
 from .employment_records_paginated_response import EmploymentRecordsPaginatedResponse
 from .enum_account_category import EnumAccountCategory
 from .enum_bank_account_holder_type_ofpi import EnumBankAccountHolderTypeOfpi
 from .enum_bank_account_holder_type_pse import EnumBankAccountHolderTypePse
 from .enum_bank_account_pix_account_type_ofpi import EnumBankAccountPixAccountTypeOfpi
 from .enum_categorization_account_category import EnumCategorizationAccountCategory
@@ -179,15 +176,14 @@
 from .holder_information_individual_ofpi import HolderInformationIndividualOfpi
 from .holder_information_individual_ofpi_response import HolderInformationIndividualOfpiResponse
 from .holder_response_ofpi import HolderResponseOfpi
 from .holder_response_ofpi_information import HolderResponseOfpiInformation
 from .income import Income
 from .income_streams_body import IncomeStreamsBody
 from .incomes_paginated_response import IncomesPaginatedResponse
-from .incomes_request import IncomesRequest
 from .institution import Institution
 from .institution_account import InstitutionAccount
 from .institution_down_error import InstitutionDownError
 from .institution_form_field import InstitutionFormField
 from .institution_inactive_error import InstitutionInactiveError
 from .institution_unavailable_error import InstitutionUnavailableError
 from .institutions_feature import InstitutionsFeature
@@ -215,26 +211,23 @@
 from .invoices_payments_dian import InvoicesPaymentsDian
 from .invoices_payments_related_documents_dian import InvoicesPaymentsRelatedDocumentsDian
 from .invoices_payments_related_documents_sat import InvoicesPaymentsRelatedDocumentsSat
 from .invoices_payments_sat import InvoicesPaymentsSat
 from .invoices_payroll_dian import InvoicesPayrollDian
 from .invoices_payroll_sat import InvoicesPayrollSat
 from .invoices_receiver_details_dian import InvoicesReceiverDetailsDian
-from .invoices_request import InvoicesRequest
 from .invoices_response_paginated_response import InvoicesResponsePaginatedResponse
 from .invoices_response_paginated_response_results_item import InvoicesResponsePaginatedResponseResultsItem
 from .last_error_invalid_credentials import LastErrorInvalidCredentials
 from .last_error_invalid_token import LastErrorInvalidToken
 from .last_error_login_error import LastErrorLoginError
 from .last_error_payment_error import LastErrorPaymentError
 from .last_error_session_expired import LastErrorSessionExpired
 from .last_error_two_factor import LastErrorTwoFactor
 from .link import Link
-from .links_put_request import LinksPutRequest
-from .links_request import LinksRequest
 from .list_payment_links_request_ordering import ListPaymentLinksRequestOrdering
 from .list_payment_links_request_status import ListPaymentLinksRequestStatus
 from .list_tax_declarations_response import ListTaxDeclarationsResponse
 from .list_tax_returns_response import ListTaxReturnsResponse
 from .login_error import LoginError
 from .needs_redirect_content import NeedsRedirectContent
 from .needs_redirect_content_pse import NeedsRedirectContentPse
@@ -315,24 +308,22 @@
 from .payment_webhook import PaymentWebhook
 from .payments_institutions_paginated_response import PaymentsInstitutionsPaginatedResponse
 from .payments_transactions_paginated_response import PaymentsTransactionsPaginatedResponse
 from .payments_way import PaymentsWay
 from .payments_webhooks_paginated_response import PaymentsWebhooksPaginatedResponse
 from .pension_income_statement_individual import PensionIncomeStatementIndividual
 from .providers_pse import ProvidersPse
-from .receivable_transaction_request import ReceivableTransactionRequest
 from .receivables_transaction import ReceivablesTransaction
 from .receivables_transaction_account import ReceivablesTransactionAccount
 from .receivables_transaction_number_of_installments import ReceivablesTransactionNumberOfInstallments
 from .receivables_transactions_paginated_response import ReceivablesTransactionsPaginatedResponse
 from .recevables_transaction_fees import RecevablesTransactionFees
 from .recurring_expense_source_transaction import RecurringExpenseSourceTransaction
 from .recurring_expenses import RecurringExpenses
 from .recurring_expenses_paginated_response import RecurringExpensesPaginatedResponse
-from .recurring_expenses_request import RecurringExpensesRequest
 from .reporting_id import ReportingId
 from .request_timeout_error_body import RequestTimeoutErrorBody
 from .retention_breakdown import RetentionBreakdown
 from .retrieve_invoices_response_item import RetrieveInvoicesResponseItem
 from .retrieve_tax_declarations_response_item import RetrieveTaxDeclarationsResponseItem
 from .retrieve_tax_returns_request_body import RetrieveTaxReturnsRequestBody
 from .retrieve_tax_returns_response_item import RetrieveTaxReturnsResponseItem
@@ -348,25 +339,22 @@
 from .secret_keys_paginated_response import SecretKeysPaginatedResponse
 from .session_expired_error import SessionExpiredError
 from .standard_request import StandardRequest
 from .tax_assessment_business import TaxAssessmentBusiness
 from .tax_assessment_individual import TaxAssessmentIndividual
 from .tax_compliance_status import TaxComplianceStatus
 from .tax_compliance_status_paginated_response import TaxComplianceStatusPaginatedResponse
-from .tax_compliance_status_request import TaxComplianceStatusRequest
 from .tax_declaration_business import TaxDeclarationBusiness
 from .tax_declaration_business_paginated import TaxDeclarationBusinessPaginated
 from .tax_declaration_individual import TaxDeclarationIndividual
 from .tax_declaration_individual_paginated import TaxDeclarationIndividualPaginated
-from .tax_declarations_request import TaxDeclarationsRequest
 from .tax_payer_information_business import TaxPayerInformationBusiness
 from .tax_payer_information_individual import TaxPayerInformationIndividual
 from .tax_retentions import TaxRetentions
 from .tax_retentions_paginated_response import TaxRetentionsPaginatedResponse
-from .tax_retentions_request import TaxRetentionsRequest
 from .tax_return_business import TaxReturnBusiness
 from .tax_return_business_monthly import TaxReturnBusinessMonthly
 from .tax_return_personal import TaxReturnPersonal
 from .tax_return_personal_monthly import TaxReturnPersonalMonthly
 from .tax_returns_business_monthly_paginated import TaxReturnsBusinessMonthlyPaginated
 from .tax_returns_business_paginated import TaxReturnsBusinessPaginated
 from .tax_returns_monthly_request import TaxReturnsMonthlyRequest
@@ -382,15 +370,14 @@
 from .tax_status_economic_activity_sat import TaxStatusEconomicActivitySat
 from .tax_status_obligations_dian import TaxStatusObligationsDian
 from .tax_status_obligations_sat import TaxStatusObligationsSat
 from .tax_status_paginated_response import TaxStatusPaginatedResponse
 from .tax_status_paginated_response_results_item import TaxStatusPaginatedResponseResultsItem
 from .tax_status_regimens_dian import TaxStatusRegimensDian
 from .tax_status_regimens_sat import TaxStatusRegimensSat
-from .tax_status_request import TaxStatusRequest
 from .tax_status_sat import TaxStatusSat
 from .tax_status_tax_payer_information_dian import TaxStatusTaxPayerInformationDian
 from .tax_status_tax_payer_information_sat import TaxStatusTaxPayerInformationSat
 from .token_required_response import TokenRequiredResponse
 from .token_required_response_token_generation_data import TokenRequiredResponseTokenGenerationData
 from .too_many_sessions_error import TooManySessionsError
 from .transaction import Transaction
@@ -423,15 +410,14 @@
     "AnnualIncomeStatementBusiness",
     "AnnualIncomeStatementIndividual",
     "AnnualTotalsIndividual",
     "AsynchronousAccepted202",
     "BadRequestErrorBodyItem",
     "Balance",
     "BalancesPaginatedResponse",
-    "BalancesRequest",
     "BankAccountBusinessPse",
     "BankAccountDetailsOfpi",
     "BankAccountDetailsOfpiPix",
     "BankAccountDetailsOpenFinance",
     "BankAccountDetailsOpenFinancePix",
     "BankAccountHolderRequestOfpi",
     "BankAccountHolderRequestOfpiInformation",
@@ -445,15 +431,14 @@
     "BeneficiaryBankAccountOfpi",
     "BeneficiaryBankAccountOfpiDetails",
     "BeneficiaryBankAccountPse",
     "Categorization",
     "CategorizationBody",
     "CategorizationBodyRequest",
     "CategorizationMerchantData",
-    "ChangeAccessMode",
     "Charge",
     "ChargePaymentMethodDetails",
     "ChargePaymentMethodDetailsOfpi",
     "ChargePaymentMethodDetailsOfpiContent",
     "ChargePaymentMethodDetailsPse",
     "ChargePaymentMethodDetailsPseContent",
     "ChargeStatus",
@@ -502,15 +487,14 @@
     "EmploymentRecord",
     "EmploymentRecordDetail",
     "EmploymentRecordDocumentId",
     "EmploymentRecordEmploymentStatusUpdates",
     "EmploymentRecordEntitlement",
     "EmploymentRecordFile",
     "EmploymentRecordPersonalData",
-    "EmploymentRecordRequest",
     "EmploymentRecordSocialSecuritySummary",
     "EmploymentRecordsPaginatedResponse",
     "EnumAccountCategory",
     "EnumBankAccountHolderTypeOfpi",
     "EnumBankAccountHolderTypePse",
     "EnumBankAccountPixAccountTypeOfpi",
     "EnumCategorizationAccountCategory",
@@ -587,15 +571,14 @@
     "HolderInformationIndividualOfpi",
     "HolderInformationIndividualOfpiResponse",
     "HolderResponseOfpi",
     "HolderResponseOfpiInformation",
     "Income",
     "IncomeStreamsBody",
     "IncomesPaginatedResponse",
-    "IncomesRequest",
     "Institution",
     "InstitutionAccount",
     "InstitutionDownError",
     "InstitutionFormField",
     "InstitutionInactiveError",
     "InstitutionUnavailableError",
     "InstitutionsFeature",
@@ -623,26 +606,23 @@
     "InvoicesPaymentsDian",
     "InvoicesPaymentsRelatedDocumentsDian",
     "InvoicesPaymentsRelatedDocumentsSat",
     "InvoicesPaymentsSat",
     "InvoicesPayrollDian",
     "InvoicesPayrollSat",
     "InvoicesReceiverDetailsDian",
-    "InvoicesRequest",
     "InvoicesResponsePaginatedResponse",
     "InvoicesResponsePaginatedResponseResultsItem",
     "LastErrorInvalidCredentials",
     "LastErrorInvalidToken",
     "LastErrorLoginError",
     "LastErrorPaymentError",
     "LastErrorSessionExpired",
     "LastErrorTwoFactor",
     "Link",
-    "LinksPutRequest",
-    "LinksRequest",
     "ListPaymentLinksRequestOrdering",
     "ListPaymentLinksRequestStatus",
     "ListTaxDeclarationsResponse",
     "ListTaxReturnsResponse",
     "LoginError",
     "NeedsRedirectContent",
     "NeedsRedirectContentPse",
@@ -721,24 +701,22 @@
     "PaymentWebhook",
     "PaymentsInstitutionsPaginatedResponse",
     "PaymentsTransactionsPaginatedResponse",
     "PaymentsWay",
     "PaymentsWebhooksPaginatedResponse",
     "PensionIncomeStatementIndividual",
     "ProvidersPse",
-    "ReceivableTransactionRequest",
     "ReceivablesTransaction",
     "ReceivablesTransactionAccount",
     "ReceivablesTransactionNumberOfInstallments",
     "ReceivablesTransactionsPaginatedResponse",
     "RecevablesTransactionFees",
     "RecurringExpenseSourceTransaction",
     "RecurringExpenses",
     "RecurringExpensesPaginatedResponse",
-    "RecurringExpensesRequest",
     "ReportingId",
     "RequestTimeoutErrorBody",
     "RetentionBreakdown",
     "RetrieveInvoicesResponseItem",
     "RetrieveTaxDeclarationsResponseItem",
     "RetrieveTaxReturnsRequestBody",
     "RetrieveTaxReturnsResponseItem",
@@ -754,25 +732,22 @@
     "SecretKeysPaginatedResponse",
     "SessionExpiredError",
     "StandardRequest",
     "TaxAssessmentBusiness",
     "TaxAssessmentIndividual",
     "TaxComplianceStatus",
     "TaxComplianceStatusPaginatedResponse",
-    "TaxComplianceStatusRequest",
     "TaxDeclarationBusiness",
     "TaxDeclarationBusinessPaginated",
     "TaxDeclarationIndividual",
     "TaxDeclarationIndividualPaginated",
-    "TaxDeclarationsRequest",
     "TaxPayerInformationBusiness",
     "TaxPayerInformationIndividual",
     "TaxRetentions",
     "TaxRetentionsPaginatedResponse",
-    "TaxRetentionsRequest",
     "TaxReturnBusiness",
     "TaxReturnBusinessMonthly",
     "TaxReturnPersonal",
     "TaxReturnPersonalMonthly",
     "TaxReturnsBusinessMonthlyPaginated",
     "TaxReturnsBusinessPaginated",
     "TaxReturnsMonthlyRequest",
@@ -788,15 +763,14 @@
     "TaxStatusEconomicActivitySat",
     "TaxStatusObligationsDian",
     "TaxStatusObligationsSat",
     "TaxStatusPaginatedResponse",
     "TaxStatusPaginatedResponseResultsItem",
     "TaxStatusRegimensDian",
     "TaxStatusRegimensSat",
-    "TaxStatusRequest",
     "TaxStatusSat",
     "TaxStatusTaxPayerInformationDian",
     "TaxStatusTaxPayerInformationSat",
     "TokenRequiredResponse",
     "TokenRequiredResponseTokenGenerationData",
     "TooManySessionsError",
     "Transaction",
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/access_to_resource_denied.py` & `fern_belvo-0.0.27/src/belvo/types/access_to_resource_denied.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/account.py` & `fern_belvo-0.0.27/src/belvo/types/account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_balance.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_balance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_credit_data.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_credit_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_funds_data.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_funds_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_funds_data_public_identifications.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_funds_data_public_identifications.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_loan_data.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_loan_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_loan_data_fees.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_loan_data_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_loan_data_interest_rate.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_loan_data_interest_rate.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/accounts_receivables_data.py` & `fern_belvo-0.0.27/src/belvo/types/accounts_receivables_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/annual_costs_and_deductions_statement_business.py` & `fern_belvo-0.0.27/src/belvo/types/annual_costs_and_deductions_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/annual_income_statement_business.py` & `fern_belvo-0.0.27/src/belvo/types/annual_income_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/annual_income_statement_individual.py` & `fern_belvo-0.0.27/src/belvo/types/annual_income_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/annual_totals_individual.py` & `fern_belvo-0.0.27/src/belvo/types/annual_totals_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/asynchronous_accepted_202.py` & `fern_belvo-0.0.27/src/belvo/types/asynchronous_accepted_202.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bad_request_error_body_item.py` & `fern_belvo-0.0.27/src/belvo/types/bad_request_error_body_item.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/balance.py` & `fern_belvo-0.0.27/src/belvo/types/balance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/balances_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/balances_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/balances_request.py` & `fern_belvo-0.0.27/src/belvo/types/tax_returns_monthly_request.py`

 * *Files 18% similar despite different names*

```diff
@@ -4,40 +4,48 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class BalancesRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The `link.id` that you want to get information for.\n"))
-    account: typing.Optional[str] = pydantic.Field(
-        description=("If provided, only balances matching this `account.id` are returned.\n")
+class TaxReturnsMonthlyRequest(pydantic.BaseModel):
+    """
+    Request body for monthly tax returns
+    """
+
+    link: str = pydantic.Field(description=("The fiscal `link.id` you want specific tax return information for.\n"))
+    attach_pdf: typing.Optional[bool] = pydantic.Field(
+        description=("When this is set to `true`, you will receive the PDF as a binary string in the response.\n")
+    )
+    save_data: typing.Optional[bool] = pydantic.Field(
+        description=(
+            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
+            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+        )
+    )
+    type: str = pydantic.Field(
+        description=(
+            "The type of tax return to return. For monthly tax returns, this field must be set to `monthly`.\n"
+        )
     )
     date_from: str = pydantic.Field(
         description=(
-            "Date from which you want to start receiving balances, in `YYYY-MM-DD` format.\n"
+            "The starting date you want to get tax returns for, in `YYYY-MM-DD` format.\n"
             "\n"
             "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
         )
     )
     date_to: str = pydantic.Field(
         description=(
-            "Date that you want to stop receiving balances, in `YYYY-MM-DD` format.\n"
+            "The date you want to stop getting tax returns for, in `YYYY-MM-DD` format.\n"
             "\n"
             "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
         )
     )
-    token: typing.Optional[str] = pydantic.Field(description=("The OTP token generated by the bank.\n"))
-    save_data: typing.Optional[bool] = pydantic.Field(
-        description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
-        )
-    )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_business_pse.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_details_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_details_ofpi_pix.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_details_ofpi_pix.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_details_open_finance.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_details_open_finance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_details_open_finance_pix.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_details_open_finance_pix.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_holder_request_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_holder_request_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_information_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_information_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_information_pse.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_ofpi_response.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/bank_account_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/bank_account_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/beneficiary_bank_account_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/beneficiary_bank_account_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/beneficiary_bank_account_pse.py` & `fern_belvo-0.0.27/src/belvo/types/beneficiary_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/categorization.py` & `fern_belvo-0.0.27/src/belvo/types/categorization.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/categorization_body.py` & `fern_belvo-0.0.27/src/belvo/types/categorization_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/categorization_body_request.py` & `fern_belvo-0.0.27/src/belvo/types/categorization_body_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/categorization_merchant_data.py` & `fern_belvo-0.0.27/src/belvo/types/categorization_merchant_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/change_access_mode.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py`

 * *Files 14% similar despite different names*

```diff
@@ -2,19 +2,19 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
-from .enum_link_access_mode_request import EnumLinkAccessModeRequest
 
 
-class ChangeAccessMode(pydantic.BaseModel):
-    access_mode: EnumLinkAccessModeRequest
+class InvestmentsPortfolioInstrumentRedemptionConditions(pydantic.BaseModel):
+    type: str = pydantic.Field(description=("The name of the redemption condition.\n"))
+    value: str = pydantic.Field(description=("The value of `redemption_conditions.type`.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge.py` & `fern_belvo-0.0.27/src/belvo/types/charge.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_ofpi_content.py` & `fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_ofpi_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge_payment_method_details_pse_content.py` & `fern_belvo-0.0.27/src/belvo/types/charge_payment_method_details_pse_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/charge_status.py` & `fern_belvo-0.0.27/src/belvo/types/charge_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_bank_account_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/create_bank_account_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_bank_account_pse.py` & `fern_belvo-0.0.27/src/belvo/types/create_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_customer_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/create_customer_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_customer_pse.py` & `fern_belvo-0.0.27/src/belvo/types/create_customer_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_payment_intent_pse.py` & `fern_belvo-0.0.27/src/belvo/types/create_payment_intent_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_payment_link_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/create_payment_link_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/create_payment_link_pse.py` & `fern_belvo-0.0.27/src/belvo/types/create_payment_link_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/customer_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/customer_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/customer_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/customer_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/customer_pse.py` & `fern_belvo-0.0.27/src/belvo/types/customer_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_confirmation_required_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/display_confirmation_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_confirmation_required_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/display_confirmation_required_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_credentials_required_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/display_credentials_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_customer_bank_accounts_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/display_customer_bank_accounts_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_payment_failed.py` & `fern_belvo-0.0.27/src/belvo/types/display_payment_failed.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_payment_method_information_content_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/display_payment_method_information_content_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_payment_method_information_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/display_payment_method_information_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_payment_processing.py` & `fern_belvo-0.0.27/src/belvo/types/display_payment_processing.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_payment_succeeded.py` & `fern_belvo-0.0.27/src/belvo/types/display_payment_succeeded.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/display_token_required_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/display_token_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/document_id_business.py` & `fern_belvo-0.0.27/src/belvo/types/document_id_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/document_id_individual.py` & `fern_belvo-0.0.27/src/belvo/types/document_id_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/document_information_business.py` & `fern_belvo-0.0.27/src/belvo/types/document_information_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/document_information_individual.py` & `fern_belvo-0.0.27/src/belvo/types/document_information_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_detail.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_detail.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_document_id.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_document_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_employment_status_updates.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_employment_status_updates.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_entitlement.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_entitlement.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_file.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_file.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_personal_data.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_personal_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_request.py` & `fern_belvo-0.0.27/src/belvo/types/recurring_expense_source_transaction.py`

 * *Files 12% similar despite different names*

```diff
@@ -4,25 +4,22 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class EmploymentRecordRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The `link.id` you want to retrieve employment records for.\n"))
-    attach_pdf: typing.Optional[bool] = pydantic.Field(
-        description=("When set to `true`, you will receive the PDF in binary format in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
+class RecurringExpenseSourceTransaction(pydantic.BaseModel):
+    amount: float = pydantic.Field(description=("The transaction amount.\n"))
+    description: typing.Optional[str] = pydantic.Field(
         description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+            "The description of the transaction provided by the institution. Usually, this is the text that the end user would see in the bank statement. The description can be an empty string.\n"
         )
     )
+    value_date: str = pydantic.Field(description=("The date when the transaction occurred, in `YYYY-MM-DD` format.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_record_social_security_summary.py` & `fern_belvo-0.0.27/src/belvo/types/employment_record_social_security_summary.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/employment_records_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/employment_records_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_bank_account_holder_type_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/enum_bank_account_holder_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_categorization_account_category.py` & `fern_belvo-0.0.27/src/belvo/types/enum_categorization_account_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_categorization_account_holder_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_categorization_account_holder_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_categorization_transaction_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_categorization_transaction_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_customer_identifier_type_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/enum_customer_identifier_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_customer_identifier_type_pse.py` & `fern_belvo-0.0.27/src/belvo/types/enum_customer_identifier_type_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_customer_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_customer_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_employment_record_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_employment_record_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_employment_record_status_update_events.py` & `fern_belvo-0.0.27/src/belvo/types/enum_employment_record_status_update_events.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_income_minimum_confidence_level_request.py` & `fern_belvo-0.0.27/src/belvo/types/enum_income_minimum_confidence_level_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_income_stream_confidence.py` & `fern_belvo-0.0.27/src/belvo/types/enum_income_stream_confidence.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_income_stream_frequency.py` & `fern_belvo-0.0.27/src/belvo/types/enum_income_stream_frequency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_income_stream_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_income_stream_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_income_verification_account_category.py` & `fern_belvo-0.0.27/src/belvo/types/enum_income_verification_account_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_institution_integration_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_institution_integration_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_institution_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_institution_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_institution_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_institution_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_investment_portfolio_instrument_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_investment_portfolio_instrument_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_investment_portfolio_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_investment_portfolio_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_invoice_allowed_income_types_request.py` & `fern_belvo-0.0.27/src/belvo/types/enum_invoice_allowed_income_types_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_invoice_sat_invoice_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_invoice_sat_invoice_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_link_access_mode_request.py` & `fern_belvo-0.0.27/src/belvo/types/enum_link_access_mode_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_link_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_link_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_loan_data_fee_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_loan_data_fee_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_loan_data_interest_rate_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_loan_data_interest_rate_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_intent_holder_type_pse.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_intent_holder_type_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_intent_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_intent_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_link_allowed_payment_method.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_link_allowed_payment_method.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_link_provider.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_link_provider.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_links_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_links_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payment_transaction_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payment_transaction_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payments_country.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payments_country.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_payments_currency.py` & `fern_belvo-0.0.27/src/belvo/types/enum_payments_currency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_receivable_transaction_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_receivable_transaction_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_category.py` & `fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_frequency.py` & `fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_frequency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_recurring_expense_payment_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_recurring_expense_payment_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_tax_compliance_status_outcome.py` & `fern_belvo-0.0.27/src/belvo/types/enum_tax_compliance_status_outcome.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_payment_status.py` & `fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_payment_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_receiver_nationality.py` & `fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_receiver_nationality.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/enum_tax_retention_type.py` & `fern_belvo-0.0.27/src/belvo/types/enum_tax_retention_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/equity_statement_business.py` & `fern_belvo-0.0.27/src/belvo/types/equity_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/equity_statement_individual.py` & `fern_belvo-0.0.27/src/belvo/types/equity_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/eyod_income_verification_body_request.py` & `fern_belvo-0.0.27/src/belvo/types/eyod_income_verification_body_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/gross_income_individual.py` & `fern_belvo-0.0.27/src/belvo/types/gross_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_bank_account_information_pse.py` & `fern_belvo-0.0.27/src/belvo/types/holder_bank_account_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_bank_account_pse.py` & `fern_belvo-0.0.27/src/belvo/types/holder_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_business_pse.py` & `fern_belvo-0.0.27/src/belvo/types/holder_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_business_response_pse.py` & `fern_belvo-0.0.27/src/belvo/types/holder_business_response_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_business_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_business_ofpi_response.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_business_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_business_pse.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_business_pse_response.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_business_pse_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_individual_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_information_individual_ofpi_response.py` & `fern_belvo-0.0.27/src/belvo/types/holder_information_individual_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/holder_response_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/holder_response_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/income.py` & `fern_belvo-0.0.27/src/belvo/types/income.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/income_streams_body.py` & `fern_belvo-0.0.27/src/belvo/types/income_streams_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/incomes_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/incomes_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/incomes_request.py` & `fern_belvo-0.0.27/src/belvo/types/transactions_request.py`

 * *Files 25% similar despite different names*

```diff
@@ -2,36 +2,31 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
-from .enum_income_minimum_confidence_level_request import EnumIncomeMinimumConfidenceLevelRequest
-from .enum_invoice_allowed_income_types_request import EnumInvoiceAllowedIncomeTypesRequest
 
 
-class IncomesRequest(pydantic.BaseModel):
+class TransactionsRequest(pydantic.BaseModel):
     link: str = pydantic.Field(description=("The `link.id` that you want to get information for.\n"))
-    allowed_income_types: typing.Optional[typing.List[EnumInvoiceAllowedIncomeTypesRequest]]
-    minimum_confidence_level: typing.Optional[EnumIncomeMinimumConfidenceLevelRequest]
-    date_from: typing.Optional[str] = pydantic.Field(
+    account: typing.Optional[str] = pydantic.Field(
+        description=("If provided, we return transactions only from this account.\n")
+    )
+    date_from: str = pydantic.Field(
         description=(
-            "The date from which you want to start getting incomes for, in `YYYY-MM-DD` format, within the last 365 days. When you use this parameter, you must also send `date_to`.\n"
-            "\n"
-            "⚠️ You must have at least 90 days between `date_from` and `date_to`.\n"
+            "The date from which you want to start getting transactions for, in `YYYY-MM-DD` format.\n"
             "\n"
             "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
         )
     )
-    date_to: typing.Optional[str] = pydantic.Field(
+    date_to: str = pydantic.Field(
         description=(
-            "The date you want to stop getting incomes for, in `YYYY-MM-DD` format, within the last 365 days. When you use this parameter, you must also send `date_from`.\n"
-            "\n"
-            "⚠️ You must have at least 90 days between `date_from` and `date_to`.\n"
+            "The date you want to stop getting transactions for, in `YYYY-MM-DD` format.\n"
             "\n"
             "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
         )
     )
     token: typing.Optional[str] = pydantic.Field(description=("The OTP token generated by the bank.\n"))
     save_data: typing.Optional[bool] = pydantic.Field(
         description=(
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution.py` & `fern_belvo-0.0.27/src/belvo/types/institution.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution_account.py` & `fern_belvo-0.0.27/src/belvo/types/institution_account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution_down_error.py` & `fern_belvo-0.0.27/src/belvo/types/institution_down_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution_form_field.py` & `fern_belvo-0.0.27/src/belvo/types/institution_form_field.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution_inactive_error.py` & `fern_belvo-0.0.27/src/belvo/types/institution_inactive_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institution_unavailable_error.py` & `fern_belvo-0.0.27/src/belvo/types/institution_unavailable_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institutions_feature.py` & `fern_belvo-0.0.27/src/belvo/types/institutions_feature.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institutions_form_field.py` & `fern_belvo-0.0.27/src/belvo/types/institutions_form_field.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institutions_form_field_values.py` & `fern_belvo-0.0.27/src/belvo/types/institutions_form_field_values.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/institutions_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/institutions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invalid_access_mode.py` & `fern_belvo-0.0.27/src/belvo/types/invalid_access_mode.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invalid_link_error.py` & `fern_belvo-0.0.27/src/belvo/types/invalid_link_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invalid_period_error.py` & `fern_belvo-0.0.27/src/belvo/types/invalid_period_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_fees.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_interest_rate.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_interest_rate.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_public_id.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolio_instrument_public_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_warnings_sat.py`

 * *Files 12% similar despite different names*

```diff
@@ -4,17 +4,17 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class InvestmentsPortfolioInstrumentRedemptionConditions(pydantic.BaseModel):
-    type: str = pydantic.Field(description=("The name of the redemption condition.\n"))
-    value: str = pydantic.Field(description=("The value of `redemption_conditions.type`.\n"))
+class InvoiceWarningsSat(pydantic.BaseModel):
+    code: typing.Optional[str] = pydantic.Field(description=("The warning code.\n"))
+    message: typing.Optional[str] = pydantic.Field(description=("The description of the warning.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/investments_portfolios_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/investments_portfolios_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_detail_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_detail_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_detail_retained_tax_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_detail_retained_tax_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_detail_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_detail_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_sender_details_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_sender_details_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_warnings_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_warnings_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_warnings_sat.py` & `fern_belvo-0.0.27/src/belvo/types/transaction_merchant_data.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,17 +4,18 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class InvoiceWarningsSat(pydantic.BaseModel):
-    code: typing.Optional[str] = pydantic.Field(description=("The warning code.\n"))
-    message: typing.Optional[str] = pydantic.Field(description=("The description of the warning.\n"))
+class TransactionMerchantData(pydantic.BaseModel):
+    logo: typing.Optional[str] = pydantic.Field(description=("The URL to the merchant's logo.\n"))
+    website: typing.Optional[str] = pydantic.Field(description=("The URL to the merchant's website.\n"))
+    merchant_name: typing.Optional[str] = pydantic.Field(description=("The name of the merchant.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoice_with_id_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoice_with_id_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payments_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payments_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payments_related_documents_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payments_related_documents_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payments_related_documents_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payments_related_documents_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payments_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payments_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payroll_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payroll_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_payroll_sat.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_payroll_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_receiver_details_dian.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_receiver_details_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_request.py` & `fern_belvo-0.0.27/src/belvo/types/too_many_sessions_error.py`

 * *Files 22% similar despite different names*

```diff
@@ -2,43 +2,43 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
-from .enum_invoice_type import EnumInvoiceType
 
 
-class InvoicesRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The fiscal `link.id` to use.\n"))
-    date_from: str = pydantic.Field(
+class TooManySessionsError(pydantic.BaseModel):
+    """
+    This error occurs when:
+
+      - a user is attempting to log in to their institution via Belvo while also already being logged in to their institution on a web browser or mobile app.
+      - you make a request for information while Belvo is scraping data from the institution for that user.
+    """
+
+    code: typing.Optional[str] = pydantic.Field(
         description=(
-            "The date from which you want to start getting invoices for, in `YYYY-MM-DD` format.\n"
+            "A unique error code (`too_many_sessions`) that allows you to classify and handle the error programmatically.\n"
             "\n"
-            "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
+            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#400-too_many_sessions" target="_blank">400 too_many_sessions errors</a>.\n'
         )
     )
-    date_to: str = pydantic.Field(
+    message: typing.Optional[str] = pydantic.Field(
         description=(
-            "The date you want to stop getting invoices for, in `YYYY-MM-DD` format.\n"
+            "A short description of the error.\n"
             "\n"
-            "⚠️ The number of days between `date_from` and `date_to` cannot be over 365.\n"
+            "For `too_many_sessions` errors, the description is:\n"
             "\n"
-            "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
+            "  - `Impossible to login, a session is already opened with the institution for these credentials`.\n"
         )
     )
-    type: EnumInvoiceType
-    attach_xml: typing.Optional[bool] = pydantic.Field(
-        description=("When set to `true`, you will receive the XML invoice in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
+    request_id: typing.Optional[str] = pydantic.Field(
         description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+            "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
         )
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/invoices_response_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/invoices_response_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_invalid_credentials.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_invalid_credentials.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_invalid_token.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_invalid_token.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_login_error.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_login_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_payment_error.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_payment_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_session_expired.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_session_expired.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/last_error_two_factor.py` & `fern_belvo-0.0.27/src/belvo/types/last_error_two_factor.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/link.py` & `fern_belvo-0.0.27/src/belvo/types/link.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/list_payment_links_request_ordering.py` & `fern_belvo-0.0.27/src/belvo/types/list_payment_links_request_ordering.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/list_payment_links_request_status.py` & `fern_belvo-0.0.27/src/belvo/types/list_payment_links_request_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/list_tax_returns_response.py` & `fern_belvo-0.0.27/src/belvo/types/list_tax_returns_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/login_error.py` & `fern_belvo-0.0.27/src/belvo/types/login_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/needs_redirect_content.py` & `fern_belvo-0.0.27/src/belvo/types/needs_redirect_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/needs_redirect_content_pse.py` & `fern_belvo-0.0.27/src/belvo/types/needs_redirect_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/net_income_individual.py` & `fern_belvo-0.0.27/src/belvo/types/net_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_confirmation_required_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_confirmation_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_credentials_required_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_credentials_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_credentials_required_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_credentials_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_customer_bank_accounts_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_customer_bank_accounts_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_needs_redirect_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_needs_redirect_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_needs_redirect_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_needs_redirect_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_failed.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_failed.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_failed_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_failed_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_method_information_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_method_information_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_processing.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_processing.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_processing_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_processing_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_succeeded.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_succeeded.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_payment_succeeded_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_payment_succeeded_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_token_required_pse.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_token_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_display_token_required_pse_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_display_token_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_needs_redirect.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_needs_redirect.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/next_step_needs_redirect_type.py` & `fern_belvo-0.0.27/src/belvo/types/next_step_needs_redirect_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/non_taxable_income_individual.py` & `fern_belvo-0.0.27/src/belvo/types/non_taxable_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/not_found_error_body.py` & `fern_belvo-0.0.27/src/belvo/types/not_found_error_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/owner.py` & `fern_belvo-0.0.27/src/belvo/types/owner.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/owner_document_id.py` & `fern_belvo-0.0.27/src/belvo/types/owner_document_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/owners_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/owners_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/paginated_response_link.py` & `fern_belvo-0.0.27/src/belvo/types/paginated_response_link.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/patch_body.py` & `fern_belvo-0.0.27/src/belvo/types/patch_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/patch_body_without_save_data.py` & `fern_belvo-0.0.27/src/belvo/types/patch_body_without_save_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/patch_payment_intents_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/patch_payment_intents_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/patch_payment_method_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/patch_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_institution.py` & `fern_belvo-0.0.27/src/belvo/types/payment_institution.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_ofpi_next_step.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_ofpi_next_step.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_payment_method_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_pse_last_error.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_pse_last_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intent_pse_next_step.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intent_pse_next_step.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intents_payment_method_details_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intents_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_intents_payment_method_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_intents_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_callback_urls.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_callback_urls.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_callback_urls_response.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_callback_urls_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_list_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_list_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_list_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_list_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_link_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_link_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_links_payment_method_details_body_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_links_payment_method_details_body_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_links_payment_method_details_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_links_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_details_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_information_body_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_information_body_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_information_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_information_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_information_details_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_information_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_information_ofpi.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_information_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_method_information_pse.py` & `fern_belvo-0.0.27/src/belvo/types/payment_method_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_transaction.py` & `fern_belvo-0.0.27/src/belvo/types/payment_transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payment_webhook.py` & `fern_belvo-0.0.27/src/belvo/types/payment_webhook.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payments_institutions_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/payments_institutions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payments_transactions_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/payments_transactions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payments_way.py` & `fern_belvo-0.0.27/src/belvo/types/payments_way.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/payments_webhooks_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/payments_webhooks_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/pension_income_statement_individual.py` & `fern_belvo-0.0.27/src/belvo/types/pension_income_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/providers_pse.py` & `fern_belvo-0.0.27/src/belvo/types/providers_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/receivable_transaction_request.py` & `fern_belvo-0.0.27/src/belvo/types/tax_returns_yearly_request.py`

 * *Files 16% similar despite different names*

```diff
@@ -4,36 +4,41 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class ReceivableTransactionRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The `link.id` that you want to get information for.\n"))
-    date_from: str = pydantic.Field(
+class TaxReturnsYearlyRequest(pydantic.BaseModel):
+    """
+    Request body for yearly tax returns
+    """
+
+    link: str = pydantic.Field(description=("The fiscal `link.id` you want specific tax return information for.\n"))
+    attach_pdf: typing.Optional[bool] = pydantic.Field(
+        description=("When this is set to `true`, you will receive the PDF as a binary string in the response.\n")
+    )
+    save_data: typing.Optional[bool] = pydantic.Field(
         description=(
-            "The date from which you want to start getting transactions for, in `YYYY-MM-DD` format.\n"
-            "\n"
-            "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
+            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
+            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
         )
     )
-    date_to: str = pydantic.Field(
+    type: str = pydantic.Field(
         description=(
-            "The date you want to stop getting transactions for, in `YYYY-MM-DD` format.\n"
+            "The type of tax return to return. For yearly tax returns this must be set to `yearly`.\n"
             "\n"
-            "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
+            "By default, Belvo returns the yearly (annual) tax returns.\n"
         )
     )
-    token: typing.Optional[str] = pydantic.Field(description=("The OTP token generated by the bank.\n"))
-    save_data: typing.Optional[bool] = pydantic.Field(
-        description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
-        )
+    year_from: str = pydantic.Field(
+        description=("The starting year you want to get tax returns for, in `YYYY` format.\n")
+    )
+    year_to: str = pydantic.Field(
+        description=("The year you want to stop getting tax returns for, in `YYYY` format.\n")
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/receivables_transaction.py` & `fern_belvo-0.0.27/src/belvo/types/receivables_transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/receivables_transaction_account.py` & `fern_belvo-0.0.27/src/belvo/types/receivables_transaction_account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/receivables_transaction_number_of_installments.py` & `fern_belvo-0.0.27/src/belvo/types/receivables_transaction_number_of_installments.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/receivables_transactions_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/receivables_transactions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/recevables_transaction_fees.py` & `fern_belvo-0.0.27/src/belvo/types/recevables_transaction_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/recurring_expense_source_transaction.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_address_between_street_sat.py`

 * *Files 13% similar despite different names*

```diff
@@ -4,22 +4,21 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class RecurringExpenseSourceTransaction(pydantic.BaseModel):
-    amount: float = pydantic.Field(description=("The transaction amount.\n"))
-    description: typing.Optional[str] = pydantic.Field(
-        description=(
-            "The description of the transaction provided by the institution. Usually, this is the text that the end user would see in the bank statement. The description can be an empty string.\n"
-        )
+class TaxStatusAddressBetweenStreetSat(pydantic.BaseModel):
+    street_one: typing.Optional[str] = pydantic.Field(
+        description=("The first street that `street` is located between.\n")
+    )
+    street_two: typing.Optional[str] = pydantic.Field(
+        description=("The second street that `street` is located between.\n")
     )
-    value_date: str = pydantic.Field(description=("The date when the transaction occurred, in `YYYY-MM-DD` format.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/recurring_expenses.py` & `fern_belvo-0.0.27/src/belvo/types/recurring_expenses.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/recurring_expenses_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/recurring_expenses_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/recurring_expenses_request.py` & `fern_belvo-0.0.27/src/belvo/types/unauthorized_error_body.py`

 * *Files 21% similar despite different names*

```diff
@@ -4,39 +4,38 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class RecurringExpensesRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The `link.id` that you want to get information for.\n"))
-    token: typing.Optional[str] = pydantic.Field(description=("The OTP token generated by the bank.\n"))
-    save_data: typing.Optional[bool] = pydantic.Field(
+class UnauthorizedErrorBody(pydantic.BaseModel):
+    """
+    This error occurs when you try to make an API call using incorrect Belvo API credentials (either your secret key or secret password, or both, are incorrect).
+    """
+
+    code: typing.Optional[str] = pydantic.Field(
         description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+            "A unique error code (`authentication_failed`) that allows you to classify and handle the error programmatically.\n"
+            "\n"
+            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#401-authentication_failed" target="_blank">401 authentication_failed errors</a>.\n'
         )
     )
-    date_from: typing.Optional[str] = pydantic.Field(
+    message: typing.Optional[str] = pydantic.Field(
         description=(
-            "The date from which you want to start getting recurring expenses for, in `YYYY-MM-DD` format, within the last 365 days. When you use this parameter, you must also send `date_to`.\n"
-            "\n"
+            "A short description of the error.\n"
             "\n"
+            "For `authentication_failed` errors, the description is:\n"
             "\n"
-            "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
+            "  - `Invalid Secret Keys`.\n"
         )
     )
-    date_to: typing.Optional[str] = pydantic.Field(
+    request_id: typing.Optional[str] = pydantic.Field(
         description=(
-            "The date you want to stop getting recurring expenses for, in `YYYY-MM-DD` format, within the last 365 days. When you use this parameter, you must also send `date_from`.\n"
-            "\n"
-            "\n"
-            "\n"
-            "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
+            "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
         )
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/reporting_id.py` & `fern_belvo-0.0.27/src/belvo/types/reporting_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/request_timeout_error_body.py` & `fern_belvo-0.0.27/src/belvo/types/request_timeout_error_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/retention_breakdown.py` & `fern_belvo-0.0.27/src/belvo/types/retention_breakdown.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_balance_metrics.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_balance_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_cashflow_metrics.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_cashflow_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_credit_card_metrics.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_credit_card_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_loans_metrics.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_loans_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/risk_insights_transaction_metrics.py` & `fern_belvo-0.0.27/src/belvo/types/risk_insights_transaction_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/secret_keys.py` & `fern_belvo-0.0.27/src/belvo/types/secret_keys.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/secret_keys_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/secret_keys_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/session_expired_error.py` & `fern_belvo-0.0.27/src/belvo/types/session_expired_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/standard_request.py` & `fern_belvo-0.0.27/src/belvo/types/standard_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_assessment_business.py` & `fern_belvo-0.0.27/src/belvo/types/tax_assessment_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_assessment_individual.py` & `fern_belvo-0.0.27/src/belvo/types/tax_assessment_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_compliance_status.py` & `fern_belvo-0.0.27/src/belvo/types/tax_compliance_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_compliance_status_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/tax_compliance_status_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_compliance_status_request.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_regimens_sat.py`

 * *Files 12% similar despite different names*

```diff
@@ -4,25 +4,18 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TaxComplianceStatusRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The fiscal `link.id` to use.\n"))
-    attach_pdf: typing.Optional[bool] = pydantic.Field(
-        description=("When set to `true`, you will receive the PDF in binary format in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
-        description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
-        )
-    )
+class TaxStatusRegimensSat(pydantic.BaseModel):
+    end_date: typing.Optional[str] = pydantic.Field(description=("The end date of the regimen.\n"))
+    initial_date: typing.Optional[str] = pydantic.Field(description=("The start date of the regimen.\n"))
+    regimen: typing.Optional[str] = pydantic.Field(description=("The description of the regimen.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_declaration_business.py` & `fern_belvo-0.0.27/src/belvo/types/tax_declaration_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_declaration_business_paginated.py` & `fern_belvo-0.0.27/src/belvo/types/tax_declaration_business_paginated.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_declaration_individual.py` & `fern_belvo-0.0.27/src/belvo/types/tax_declaration_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_declaration_individual_paginated.py` & `fern_belvo-0.0.27/src/belvo/types/tax_declaration_individual_paginated.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_declarations_request.py` & `fern_belvo-0.0.27/src/belvo/types/token_required_response_token_generation_data.py`

 * *Files 16% similar despite different names*

```diff
@@ -4,35 +4,30 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TaxDeclarationsRequest(pydantic.BaseModel):
+class TokenRequiredResponseTokenGenerationData(pydantic.BaseModel):
     """
-    Request body for tax declrarations
+    Details on how to generate the token.
     """
 
-    link: str = pydantic.Field(
-        description=("The fiscal `link.id` you want specific tax declaration information for.\n")
+    instructions: typing.Optional[str] = pydantic.Field(description=("Instructions for token generation.\n"))
+    type: typing.Optional[str] = pydantic.Field(
+        description=("Type of the data to generate the token (QR code, numeric challenge).\n")
     )
-    year_from: str = pydantic.Field(
-        description=("The starting year you want to get tax declaration for, in `YYYY` format.\n")
-    )
-    year_to: str = pydantic.Field(
-        description=("The year you want to stop getting tax declaration for, in `YYYY` format.\n")
-    )
-    attach_pdf: typing.Optional[bool] = pydantic.Field(
-        description=("When this is set to `true`, you will receive the PDF as a binary string in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
+    value: typing.Optional[str] = pydantic.Field(description=("Value to use to generate the token.\n"))
+    expects_user_input: typing.Optional[bool] = pydantic.Field(
         description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+            "Indicates whether the user needs to provide input in order to complete the authentication.\n"
+            "When set to `false`, your user may need to:\n"
+            "- confirm the login on another device - scan a QR code\n"
+            "You will still need to make a PATCH call to complete the request.\n"
         )
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_payer_information_business.py` & `fern_belvo-0.0.27/src/belvo/types/tax_payer_information_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_payer_information_individual.py` & `fern_belvo-0.0.27/src/belvo/types/tax_payer_information_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_retentions.py` & `fern_belvo-0.0.27/src/belvo/types/tax_retentions.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_retentions_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/tax_retentions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_retentions_request.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_economic_activity_dian.py`

 * *Files 26% similar despite different names*

```diff
@@ -2,42 +2,31 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
-from .enum_tax_retention_type import EnumTaxRetentionType
 
 
-class TaxRetentionsRequest(pydantic.BaseModel):
-    link: str = pydantic.Field(description=("The `link.id` that you want to get information for.\n"))
-    date_from: str = pydantic.Field(
+class TaxStatusEconomicActivityDian(pydantic.BaseModel):
+    economic_activity: typing.Optional[str] = pydantic.Field(
         description=(
-            "The date from which you want to start getting tax retentions for, in `YYYY-MM-DD` format.\n"
+            "The economic activity code, according to the fiscal institution.\n"
             "\n"
-            "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
+            "For detailed information regarding DIAN's economic activities, please see their [official PDF](https://www.dian.gov.co/impuestos/factura-electronica/Documents/Anexo_tecnico_factura_electronica_vr_1_7_2020.pdf).\n"
         )
     )
-    date_to: str = pydantic.Field(
-        description=(
-            "The date you want to stop getting tax retentions for, in `YYYY-MM-DD` format.\n"
-            "\n"
-            "⚠️ The number of days between `date_from` and `date_to` cannot be over 365.\n"
-        )
+    initial_date: typing.Optional[str] = pydantic.Field(description=("The start date of the economic activity.\n"))
+    end_date: typing.Optional[str] = pydantic.Field(
+        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
     )
-    type: EnumTaxRetentionType
-    attach_xml: typing.Optional[bool] = pydantic.Field(
-        description=("When set to `true`, you will receive the XML tax retention in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
-        description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
-        )
+    order: typing.Optional[str] = pydantic.Field(description=("The order of the economic activity.\n"))
+    percentage: typing.Optional[str] = pydantic.Field(
+        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_returns_monthly_request.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_paginated_response.py`

 * *Files 22% similar despite different names*

```diff
@@ -2,49 +2,31 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
+from .tax_status_paginated_response_results_item import TaxStatusPaginatedResponseResultsItem
 
 
-class TaxReturnsMonthlyRequest(pydantic.BaseModel):
-    """
-    Request body for monthly tax returns
-    """
-
-    link: str = pydantic.Field(description=("The fiscal `link.id` you want specific tax return information for.\n"))
-    attach_pdf: typing.Optional[bool] = pydantic.Field(
-        description=("When this is set to `true`, you will receive the PDF as a binary string in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
-        description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
-        )
-    )
-    type: str = pydantic.Field(
+class TaxStatusPaginatedResponse(pydantic.BaseModel):
+    count: typing.Optional[int] = pydantic.Field(description=("The total number of results in your Belvo account.\n"))
+    next: typing.Optional[str] = pydantic.Field(
         description=(
-            "The type of tax return to return. For monthly tax returns, this field must be set to `monthly`.\n"
-        )
-    )
-    date_from: str = pydantic.Field(
-        description=(
-            "The starting date you want to get tax returns for, in `YYYY-MM-DD` format.\n"
+            "The URL to next page of results. Each page consists of up to 100 items. If there are not enough results for an additional page, the value is `null`.\n"
             "\n"
-            "⚠️ The value of `date_from` cannot be greater than `date_to`.\n"
+            "In our documentation example, we use `{endpoint}` as a placeholder value. In production, this value will be replaced by the actual endpoint you are currently using (for example, `accounts` or `owners`).\n"
         )
     )
-    date_to: str = pydantic.Field(
-        description=(
-            "The date you want to stop getting tax returns for, in `YYYY-MM-DD` format.\n"
-            "\n"
-            "⚠️ The value of `date_to` cannot be greater than today's date (in other words, no future dates).\n"
-        )
+    previous: typing.Optional[str] = pydantic.Field(
+        description=("The URL to the previous page of results. If there is no previous page, the value is `null`.\n")
+    )
+    results: typing.Optional[typing.List[TaxStatusPaginatedResponseResultsItem]] = pydantic.Field(
+        description=("Array of tax status objects.\n")
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_returns_yearly_request.py` & `fern_belvo-0.0.27/src/belvo/types/unconfirmed_link_error.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,41 +4,40 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TaxReturnsYearlyRequest(pydantic.BaseModel):
+class UnconfirmedLinkError(pydantic.BaseModel):
     """
-    Request body for yearly tax returns
+    This error occurs when you try to access a link that was paused previously (and as such is not active now).
+    A Link's status is set to `unconfirmed_link` when your user has not completed the Link creation process successfully (for example, they might not provide a valid MFA token).
     """
 
-    link: str = pydantic.Field(description=("The fiscal `link.id` you want specific tax return information for.\n"))
-    attach_pdf: typing.Optional[bool] = pydantic.Field(
-        description=("When this is set to `true`, you will receive the PDF as a binary string in the response.\n")
-    )
-    save_data: typing.Optional[bool] = pydantic.Field(
+    code: typing.Optional[str] = pydantic.Field(
         description=(
-            "Indicates whether or not to persist the data in Belvo. By default, this is set to `true` and we return a 201 Created response.\n"
-            "When set to `false`, the data won't be persisted and we return a 200 OK response.\n"
+            "A unique error code (`unconfirmed_link`) that allows you to classify and handle the error programmatically.\n"
+            "\n"
+            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#400-unconfirmed_link" target="_blank">400 unconfirmed_link errors</a>.\n'
         )
     )
-    type: str = pydantic.Field(
+    message: typing.Optional[str] = pydantic.Field(
         description=(
-            "The type of tax return to return. For yearly tax returns this must be set to `yearly`.\n"
+            "A short description of the error.\n"
+            "\n"
+            "For `unconfirmed_link` errors, the description is:\n"
             "\n"
-            "By default, Belvo returns the yearly (annual) tax returns.\n"
+            "  - `The link creation has not been completed yet`.\n"
         )
     )
-    year_from: str = pydantic.Field(
-        description=("The starting year you want to get tax returns for, in `YYYY` format.\n")
-    )
-    year_to: str = pydantic.Field(
-        description=("The year you want to stop getting tax returns for, in `YYYY` format.\n")
+    request_id: typing.Optional[str] = pydantic.Field(
+        description=(
+            "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
+        )
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_address_between_street_dian.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_address_between_street_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_address_between_street_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_regimens_dian.py`

 * *Files 15% similar despite different names*

```diff
@@ -4,21 +4,22 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TaxStatusAddressBetweenStreetSat(pydantic.BaseModel):
-    street_one: typing.Optional[str] = pydantic.Field(
-        description=("The first street that `street` is located between.\n")
+class TaxStatusRegimensDian(pydantic.BaseModel):
+    end_date: typing.Optional[str] = pydantic.Field(
+        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
     )
-    street_two: typing.Optional[str] = pydantic.Field(
-        description=("The second street that `street` is located between.\n")
+    initial_date: typing.Optional[str] = pydantic.Field(
+        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
     )
+    regimen: typing.Optional[str] = pydantic.Field(description=("The description of the regimen.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_address_dian.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_address_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_address_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_address_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_dian.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_economic_activity_dian.py` & `fern_belvo-0.0.27/src/belvo/types/unexpected_error.py`

 * *Files 20% similar despite different names*

```diff
@@ -4,29 +4,39 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TaxStatusEconomicActivityDian(pydantic.BaseModel):
-    economic_activity: typing.Optional[str] = pydantic.Field(
+class UnexpectedError(pydantic.BaseModel):
+    """
+    This error occurs when we (Belvo) have encountered an internal system error (sorry about that) or due to an unsupported response from the institution.
+    """
+
+    code: typing.Optional[str] = pydantic.Field(
         description=(
-            "The economic activity code, according to the fiscal institution.\n"
+            "A unique error code (`unexpected_error`) that allows you to classify and handle the error programmatically.\n"
             "\n"
-            "For detailed information regarding DIAN's economic activities, please see their [official PDF](https://www.dian.gov.co/impuestos/factura-electronica/Documents/Anexo_tecnico_factura_electronica_vr_1_7_2020.pdf).\n"
+            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#500-unexpected_error" target="_blank">500 unexpected_error errors</a>.\n'
         )
     )
-    initial_date: typing.Optional[str] = pydantic.Field(description=("The start date of the economic activity.\n"))
-    end_date: typing.Optional[str] = pydantic.Field(
-        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
+    message: typing.Optional[str] = pydantic.Field(
+        description=(
+            "A short description of the error.\n"
+            "\n"
+            "For `unexpected_error` errors, the description is:\n"
+            "\n"
+            "  - `Belvo is unable to process the request due to an internal system issue or to an unsupported response from an institution`.\n"
+        )
     )
-    order: typing.Optional[str] = pydantic.Field(description=("The order of the economic activity.\n"))
-    percentage: typing.Optional[str] = pydantic.Field(
-        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
+    request_id: typing.Optional[str] = pydantic.Field(
+        description=(
+            "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
+        )
     )
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_economic_activity_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_economic_activity_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_obligations_dian.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_obligations_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_obligations_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_obligations_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_paginated_response.py` & `fern_belvo-0.0.27/src/belvo/types/transactions_paginated_response.py`

 * *Files 7% similar despite different names*

```diff
@@ -2,32 +2,30 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
-from .tax_status_paginated_response_results_item import TaxStatusPaginatedResponseResultsItem
+from .transaction import Transaction
 
 
-class TaxStatusPaginatedResponse(pydantic.BaseModel):
+class TransactionsPaginatedResponse(pydantic.BaseModel):
     count: typing.Optional[int] = pydantic.Field(description=("The total number of results in your Belvo account.\n"))
     next: typing.Optional[str] = pydantic.Field(
         description=(
             "The URL to next page of results. Each page consists of up to 100 items. If there are not enough results for an additional page, the value is `null`.\n"
             "\n"
             "In our documentation example, we use `{endpoint}` as a placeholder value. In production, this value will be replaced by the actual endpoint you are currently using (for example, `accounts` or `owners`).\n"
         )
     )
     previous: typing.Optional[str] = pydantic.Field(
         description=("The URL to the previous page of results. If there is no previous page, the value is `null`.\n")
     )
-    results: typing.Optional[typing.List[TaxStatusPaginatedResponseResultsItem]] = pydantic.Field(
-        description=("Array of tax status objects.\n")
-    )
+    results: typing.Optional[typing.List[Transaction]] = pydantic.Field(description=("Array of transaction objects.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_regimens_dian.py` & `fern_belvo-0.0.27/src/belvo/types/transaction_credit_card_data.py`

 * *Files 17% similar despite different names*

```diff
@@ -2,24 +2,37 @@
 
 import datetime as dt
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
+from .enum_transaction_bill_status import EnumTransactionBillStatus
 
 
-class TaxStatusRegimensDian(pydantic.BaseModel):
-    end_date: typing.Optional[str] = pydantic.Field(
-        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
+class TransactionCreditCardData(pydantic.BaseModel):
+    collected_at: typing.Optional[str] = pydantic.Field(
+        description=("The ISO-8601 timestamp when the data point was collected.\n")
     )
-    initial_date: typing.Optional[str] = pydantic.Field(
-        description=("**Note**: This field is not applicable for DIAN Colombia and will return `null`.\n")
+    bill_name: typing.Optional[str] = pydantic.Field(
+        description=(
+            "The title of the monthly credit card bill the transaction belongs to. The format of the returned value is institution specific, however, some common examples are:\n"
+            "\n"
+            "- diciembre-2021\n"
+            "- dec-2021\n"
+            "- dec-21\n"
+        )
+    )
+    bill_status: typing.Optional[EnumTransactionBillStatus]
+    bill_amount: typing.Optional[float] = pydantic.Field(
+        description=("The aggregate bill amount, as of `collected_at`.\n")
+    )
+    previous_bill_total: typing.Optional[str] = pydantic.Field(
+        description=("The total amount of the previous month's bill, if available.\n")
     )
-    regimen: typing.Optional[str] = pydantic.Field(description=("The description of the regimen.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_tax_payer_information_dian.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_tax_payer_information_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/tax_status_tax_payer_information_sat.py` & `fern_belvo-0.0.27/src/belvo/types/tax_status_tax_payer_information_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/token_required_response.py` & `fern_belvo-0.0.27/src/belvo/types/token_required_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/too_many_sessions_error.py` & `fern_belvo-0.0.27/src/belvo/types/unsupported_operation_error.py`

 * *Files 13% similar despite different names*

```diff
@@ -4,36 +4,33 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class TooManySessionsError(pydantic.BaseModel):
+class UnsupportedOperationError(pydantic.BaseModel):
     """
-    This error occurs when:
-
-      - a user is attempting to log in to their institution via Belvo while also already being logged in to their institution on a web browser or mobile app.
-      - you make a request for information while Belvo is scraping data from the institution for that user.
+    This error occurs when you try to access some data operation that Belvo does not support for an institution. For example, trying to access the Balances resource for fiscal institutions.
     """
 
     code: typing.Optional[str] = pydantic.Field(
         description=(
-            "A unique error code (`too_many_sessions`) that allows you to classify and handle the error programmatically.\n"
+            "A unique error code (`unsupported_operation`) that allows you to classify and handle the error programmatically.\n"
             "\n"
-            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#400-too_many_sessions" target="_blank">400 too_many_sessions errors</a>.\n'
+            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#400-unsupported_operation" target="_blank">400 unsupported_operation errors</a>.\n'
         )
     )
     message: typing.Optional[str] = pydantic.Field(
         description=(
             "A short description of the error.\n"
             "\n"
-            "For `too_many_sessions` errors, the description is:\n"
+            "For `unsupported_operation` errors, the description is:\n"
             "\n"
-            "  - `Impossible to login, a session is already opened with the institution for these credentials`.\n"
+            "  - `The resource you are trying to access is not supported by this institution`.\n"
         )
     )
     request_id: typing.Optional[str] = pydantic.Field(
         description=(
             "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
         )
     )
```

### Comparing `fern_belvo-0.0.25/src/belvo/types/transaction.py` & `fern_belvo-0.0.27/src/belvo/types/transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/transaction_bank_account_body_pse.py` & `fern_belvo-0.0.27/src/belvo/types/transaction_bank_account_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.25/src/belvo/types/unauthorized_error_body.py` & `fern_belvo-0.0.27/src/belvo/types/validation_error.py`

 * *Files 25% similar despite different names*

```diff
@@ -4,40 +4,48 @@
 import typing
 
 import pydantic
 
 from ..core.datetime_utils import serialize_datetime
 
 
-class UnauthorizedErrorBody(pydantic.BaseModel):
+class ValidationError(pydantic.BaseModel):
     """
-    This error occurs when you try to make an API call using incorrect Belvo API credentials (either your secret key or secret password, or both, are incorrect).
+    This error occurs when you try to resume a request session that has already expired. This is usually because the user took too long to provide their authentication token.
     """
 
     code: typing.Optional[str] = pydantic.Field(
         description=(
-            "A unique error code (`authentication_failed`) that allows you to classify and handle the error programmatically.\n"
+            "A unique error code (`null`, `does_not_exist`, `required`) that allows you to classify and handle the error programmatically.\n"
             "\n"
-            'ℹ️ Check our DevPortal for more information on how to handle <a href="https://developers.belvo.com/docs/belvo-api-errors#401-authentication_failed" target="_blank">401 authentication_failed errors</a>.\n'
+            "ℹ️ Check our DevPortal for more information on how to handle:\n"
+            '  - <a href="https://developers.belvo.com/docs/belvo-api-errors#400-blank" target="_blank">400 blank errors</a>\n'
+            '  - <a href="https://developers.belvo.com/docs/belvo-api-errors#400-null" target="_blank">400 null errors</a>\n'
+            '  - <a href="https://developers.belvo.com/docs/belvo-api-errors#400-does_not_exist" target="_blank">400 does_not_exist errors</a>\n'
+            '  - <a href="https://developers.belvo.com/docs/belvo-api-errors#400-required" target="_blank">400 required errors</a>\n'
         )
     )
     message: typing.Optional[str] = pydantic.Field(
         description=(
             "A short description of the error.\n"
             "\n"
-            "For `authentication_failed` errors, the description is:\n"
+            "For `session_expired` errors, the description can be (among others):\n"
             "\n"
-            "  - `Invalid Secret Keys`.\n"
+            "  - `This field is required.`\n"
+            "  - `Object with name=narnia does not exist.`\n"
+            "  - `This field may not be null.`\n"
+            "  - `This field may not be blank.`\n"
         )
     )
     request_id: typing.Optional[str] = pydantic.Field(
         description=(
             "A 32-character unique ID of the request (matching a regex pattern of: `[a-f0-9]{32}`). Provide this ID when contacting the Belvo support team to accelerate investigations.\n"
         )
     )
+    field: typing.Optional[str] = pydantic.Field(description=("Name of the field where the error was encountered.\n"))
 
     def json(self, **kwargs: typing.Any) -> str:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
         return super().json(**kwargs_with_defaults)
 
     def dict(self, **kwargs: typing.Any) -> typing.Dict[str, typing.Any]:
         kwargs_with_defaults: typing.Any = {"by_alias": True, "exclude_unset": True, **kwargs}
```

### Comparing `fern_belvo-0.0.25/PKG-INFO` & `fern_belvo-0.0.27/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fern-belvo
-Version: 0.0.25
+Version: 0.0.27
 Summary: 
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
@@ -41,21 +41,19 @@
 
 belvo_client = Belvo(
     secret_id="YOUR_SECRET_ID",
     secret_password="YOUR_SECRET_PASSWORD",
 )
 
 link = belvo_client.links.register_link(
-    request=belvo.LinksRequest(
-        institution="banamex_mx_retail",
-        username="username",
-        password="password",
-        accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
-        credentialsStorage="30d",
-    )
+    institution="banamex_mx_retail",
+    username="username",
+    password="password",
+    accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
+    credentialsStorage="30d",
 )
 
 print(link)
 ```
 
 ## Async client
 
@@ -68,21 +66,19 @@
 belvo_client = AsyncBelvo(
     secret_id="YOUR_SECRET_ID",
     secret_password="YOUR_SECRET_PASSWORD",
 )
 
 async def get_link() -> None:
     link = await belvo_client.links.register_link({
-        body=belvo.LinksRequest(
-            institution="banamex_mx_retail",
-            username="username",
-            password="password",
-            accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
-            credentialsStorage="30d,
-        )
+        institution="banamex_mx_retail",
+        username="username",
+        password="password",
+        accessMode=belvo.EnumLinkAccessModeRequest.SINGLE,
+        credentialsStorage="30d,
     })
 
     print(link)
 
 asyncio.run(get_link())
 ```
```

