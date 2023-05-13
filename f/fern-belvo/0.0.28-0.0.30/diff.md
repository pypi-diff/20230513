# Comparing `tmp/fern_belvo-0.0.28.tar.gz` & `tmp/fern_belvo-0.0.30.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fern_belvo-0.0.28.tar", max compression
+gzip compressed data, was "fern_belvo-0.0.30.tar", max compression
```

## Comparing `fern_belvo-0.0.28.tar` & `fern_belvo-0.0.30.tar`

### file list

```diff
@@ -1,469 +1,469 @@
--rw-r--r--   0        0        0     2460 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/README.md
--rw-r--r--   0        0        0      433 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/pyproject.toml
--rw-r--r--   0        0        0    27716 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/__init__.py
--rw-r--r--   0        0        0    16332 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/client.py
--rw-r--r--   0        0        0      348 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/core/__init__.py
--rw-r--r--   0        0        0      426 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/core/api_error.py
--rw-r--r--   0        0        0     1047 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/core/datetime_utils.py
--rw-r--r--   0        0        0     3710 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/core/jsonable_encoder.py
--rw-r--r--   0        0        0      385 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/core/remove_none_from_headers.py
--rw-r--r--   0        0        0      247 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/environment.py
--rw-r--r--   0        0        0      594 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/__init__.py
--rw-r--r--   0        0        0      346 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/bad_request_error.py
--rw-r--r--   0        0        0      341 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/forbidden_error.py
--rw-r--r--   0        0        0      323 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/internal_server_error.py
--rw-r--r--   0        0        0      325 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/not_found_error.py
--rw-r--r--   0        0        0      340 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/precondition_error.py
--rw-r--r--   0        0        0      349 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/request_timeout_error.py
--rw-r--r--   0        0        0      340 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/errors/unauthorized_error.py
--rw-r--r--   0        0        0        0 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/py.typed
--rw-r--r--   0        0        0     1252 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/__init__.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/accounts/__init__.py
--rw-r--r--   0        0        0    24969 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/accounts/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/balances/__init__.py
--rw-r--r--   0        0        0    23438 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/balances/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/bank_accounts/__init__.py
--rw-r--r--   0        0        0    12881 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/bank_accounts/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/categorization/__init__.py
--rw-r--r--   0        0        0     5136 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/categorization/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/customers/__init__.py
--rw-r--r--   0        0        0    11285 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/customers/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/employment_records/__init__.py
--rw-r--r--   0        0        0    14543 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/employment_records/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/income_verification/__init__.py
--rw-r--r--   0        0        0     7011 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/income_verification/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/incomes/__init__.py
--rw-r--r--   0        0        0    20690 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/incomes/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/institutions/__init__.py
--rw-r--r--   0        0        0     8765 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/institutions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/investment_portfolios/__init__.py
--rw-r--r--   0        0        0    18632 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/investment_portfolios/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/invoices/__init__.py
--rw-r--r--   0        0        0    24516 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/invoices/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/links/__init__.py
--rw-r--r--   0        0        0    33898 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/links/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/owners/__init__.py
--rw-r--r--   0        0        0    19773 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/owners/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_institutions/__init__.py
--rw-r--r--   0        0        0     7761 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_institutions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_intents/__init__.py
--rw-r--r--   0        0        0    16753 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_intents/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_links/__init__.py
--rw-r--r--   0        0        0    12471 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_links/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_transactions/__init__.py
--rw-r--r--   0        0        0    10337 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_transactions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_webhooks/__init__.py
--rw-r--r--   0        0        0    12737 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/payment_webhooks/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/receivable_transactions/__init__.py
--rw-r--r--   0        0        0    17393 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/receivable_transactions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/recurring_expenses/__init__.py
--rw-r--r--   0        0        0    20402 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/recurring_expenses/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.144124 fern_belvo-0.0.28/src/belvo/resources/risk_insights/__init__.py
--rw-r--r--   0        0        0    18655 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/risk_insights/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/secret_keys/__init__.py
--rw-r--r--   0        0        0     5974 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/secret_keys/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_compliance_status/__init__.py
--rw-r--r--   0        0        0    15905 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_compliance_status/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_declarations/__init__.py
--rw-r--r--   0        0        0    17236 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_declarations/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_retentions/__init__.py
--rw-r--r--   0        0        0    15901 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_retentions/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_returns/__init__.py
--rw-r--r--   0        0        0    16912 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_returns/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_status/__init__.py
--rw-r--r--   0        0        0    15773 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/tax_status/client.py
--rw-r--r--   0        0        0       65 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/transactions/__init__.py
--rw-r--r--   0        0        0    34291 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/resources/transactions/client.py
--rw-r--r--   0        0        0    41108 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/__init__.py
--rw-r--r--   0        0        0     1908 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/access_to_resource_denied.py
--rw-r--r--   0        0        0     4506 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/account.py
--rw-r--r--   0        0        0     2443 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_balance.py
--rw-r--r--   0        0        0     2241 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_credit_data.py
--rw-r--r--   0        0        0     1594 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_funds_data.py
--rw-r--r--   0        0        0      958 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_funds_data_public_identifications.py
--rw-r--r--   0        0        0     4780 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_loan_data.py
--rw-r--r--   0        0        0      935 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_loan_data_fees.py
--rw-r--r--   0        0        0     1191 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_loan_data_interest_rate.py
--rw-r--r--   0        0        0     1674 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_paginated_response.py
--rw-r--r--   0        0        0     1349 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/accounts_receivables_data.py
--rw-r--r--   0        0        0     1588 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/annual_costs_and_deductions_statement_business.py
--rw-r--r--   0        0        0     1883 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/annual_income_statement_business.py
--rw-r--r--   0        0        0     1282 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/annual_income_statement_individual.py
--rw-r--r--   0        0        0     1514 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/annual_totals_individual.py
--rw-r--r--   0        0        0      992 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/asynchronous_accepted_202.py
--rw-r--r--   0        0        0     1014 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bad_request_error_body_item.py
--rw-r--r--   0        0        0     1827 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/balance.py
--rw-r--r--   0        0        0     1671 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/balances_paginated_response.py
--rw-r--r--   0        0        0     2531 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_business_pse.py
--rw-r--r--   0        0        0     1189 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_details_ofpi.py
--rw-r--r--   0        0        0      930 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_details_ofpi_pix.py
--rw-r--r--   0        0        0     1196 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_details_open_finance.py
--rw-r--r--   0        0        0      937 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_details_open_finance_pix.py
--rw-r--r--   0        0        0     1094 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_holder_request_ofpi.py
--rw-r--r--   0        0        0      356 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_holder_request_ofpi_information.py
--rw-r--r--   0        0        0      966 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_information_content_pse.py
--rw-r--r--   0        0        0     1077 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_information_pse.py
--rw-r--r--   0        0        0     1852 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_ofpi_response.py
--rw-r--r--   0        0        0      309 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_ofpi_response_details.py
--rw-r--r--   0        0        0     1801 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_paginated_response.py
--rw-r--r--   0        0        0      311 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_paginated_response_results_item.py
--rw-r--r--   0        0        0      176 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/bank_account_pse_response.py
--rw-r--r--   0        0        0     1439 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/beneficiary_bank_account_ofpi.py
--rw-r--r--   0        0        0      356 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/beneficiary_bank_account_ofpi_details.py
--rw-r--r--   0        0        0     1242 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/beneficiary_bank_account_pse.py
--rw-r--r--   0        0        0      945 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/categorization.py
--rw-r--r--   0        0        0     3020 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/categorization_body.py
--rw-r--r--   0        0        0     2488 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/categorization_body_request.py
--rw-r--r--   0        0        0     1052 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/categorization_merchant_data.py
--rw-r--r--   0        0        0     3723 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge.py
--rw-r--r--   0        0        0      342 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details.py
--rw-r--r--   0        0        0      972 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_ofpi.py
--rw-r--r--   0        0        0     1135 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_ofpi_content.py
--rw-r--r--   0        0        0      959 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_pse.py
--rw-r--r--   0        0        0     1127 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_pse_content.py
--rw-r--r--   0        0        0      703 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/charge_status.py
--rw-r--r--   0        0        0     1304 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_bank_account_ofpi.py
--rw-r--r--   0        0        0      307 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_bank_account_ofpi_details.py
--rw-r--r--   0        0        0     1863 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_bank_account_pse.py
--rw-r--r--   0        0        0      284 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_bank_account_request.py
--rw-r--r--   0        0        0      297 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_bank_account_response.py
--rw-r--r--   0        0        0     1521 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_customer_ofpi.py
--rw-r--r--   0        0        0     1517 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_customer_pse.py
--rw-r--r--   0        0        0      261 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_customer_request.py
--rw-r--r--   0        0        0      224 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_customer_response.py
--rw-r--r--   0        0        0     2638 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_intent_pse.py
--rw-r--r--   0        0        0      134 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_intent_pse_amount.py
--rw-r--r--   0        0        0     2894 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_link_ofpi.py
--rw-r--r--   0        0        0      135 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_link_ofpi_amount.py
--rw-r--r--   0        0        0     2835 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_link_pse.py
--rw-r--r--   0        0        0      132 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_payment_link_pse_amount.py
--rw-r--r--   0        0        0      284 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_paymentlink_request.py
--rw-r--r--   0        0        0      247 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/create_paymentlink_response.py
--rw-r--r--   0        0        0     1855 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/customer_ofpi.py
--rw-r--r--   0        0        0     1784 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/customer_paginated_response.py
--rw-r--r--   0        0        0      238 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/customer_paginated_response_results_item.py
--rw-r--r--   0        0        0     2229 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/customer_pse.py
--rw-r--r--   0        0        0      297 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_bank_account_response.py
--rw-r--r--   0        0        0      253 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_create_paymentlink_response.py
--rw-r--r--   0        0        0      224 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_customer_response.py
--rw-r--r--   0        0        0      237 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_invoice_response.py
--rw-r--r--   0        0        0      301 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_tax_declaration_response.py
--rw-r--r--   0        0        0      450 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_tax_return_response.py
--rw-r--r--   0        0        0      233 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/detail_tax_status_response.py
--rw-r--r--   0        0        0      972 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_confirmation_required_content_pse.py
--rw-r--r--   0        0        0     1301 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_confirmation_required_ofpi.py
--rw-r--r--   0        0        0     1001 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_credentials_required_content_pse.py
--rw-r--r--   0        0        0     1279 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_customer_bank_accounts_content_pse.py
--rw-r--r--   0        0        0      913 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_payment_failed.py
--rw-r--r--   0        0        0     1055 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_payment_method_information_content_ofpi.py
--rw-r--r--   0        0        0     1489 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_payment_method_information_content_pse.py
--rw-r--r--   0        0        0      917 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_payment_processing.py
--rw-r--r--   0        0        0      916 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_payment_succeeded.py
--rw-r--r--   0        0        0      861 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/display_token_required_content_pse.py
--rw-r--r--   0        0        0     1005 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/document_id_business.py
--rw-r--r--   0        0        0     1007 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/document_id_individual.py
--rw-r--r--   0        0        0     1277 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/document_information_business.py
--rw-r--r--   0        0        0     1275 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/document_information_individual.py
--rw-r--r--   0        0        0     2557 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/employment_record.py
--rw-r--r--   0        0        0     2769 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/employment_record_detail.py
--rw-r--r--   0        0        0     1086 2023-05-12 23:30:30.148126 fern_belvo-0.0.28/src/belvo/types/employment_record_document_id.py
--rw-r--r--   0        0        0     1317 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_record_employment_status_updates.py
--rw-r--r--   0        0        0     1584 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_record_entitlement.py
--rw-r--r--   0        0        0     1034 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_record_file.py
--rw-r--r--   0        0        0     1843 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_record_personal_data.py
--rw-r--r--   0        0        0     1495 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_record_social_security_summary.py
--rw-r--r--   0        0        0     1732 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/employment_records_paginated_response.py
--rw-r--r--   0        0        0      123 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_account_category.py
--rw-r--r--   0        0        0      630 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_bank_account_holder_type_ofpi.py
--rw-r--r--   0        0        0      506 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_bank_account_holder_type_pse.py
--rw-r--r--   0        0        0      850 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py
--rw-r--r--   0        0        0     1179 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_categorization_account_category.py
--rw-r--r--   0        0        0      668 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_categorization_account_holder_type.py
--rw-r--r--   0        0        0      141 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_categorization_transaction_category.py
--rw-r--r--   0        0        0      144 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_categorization_transaction_subcategory.py
--rw-r--r--   0        0        0      702 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_categorization_transaction_type.py
--rw-r--r--   0        0        0      592 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_customer_identifier_type_ofpi.py
--rw-r--r--   0        0        0     1031 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_customer_identifier_type_pse.py
--rw-r--r--   0        0        0      699 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_customer_type.py
--rw-r--r--   0        0        0      495 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_employment_record_document_type.py
--rw-r--r--   0        0        0      532 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_employment_record_status.py
--rw-r--r--   0        0        0     1719 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_employment_record_status_update_events.py
--rw-r--r--   0        0        0      911 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_minimum_confidence_level_request.py
--rw-r--r--   0        0        0      475 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_source_type.py
--rw-r--r--   0        0        0      824 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_stream_confidence.py
--rw-r--r--   0        0        0     1495 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_stream_frequency.py
--rw-r--r--   0        0        0     2123 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_stream_type.py
--rw-r--r--   0        0        0      758 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_verification_account_category.py
--rw-r--r--   0        0        0      484 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_verification_account_holder_type.py
--rw-r--r--   0        0        0      359 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_income_verification_type.py
--rw-r--r--   0        0        0      862 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_institution_integration_type.py
--rw-r--r--   0        0        0      630 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_institution_status.py
--rw-r--r--   0        0        0      805 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_institution_type.py
--rw-r--r--   0        0        0     1687 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_investment_portfolio_instrument_type.py
--rw-r--r--   0        0        0     1084 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_investment_portfolio_type.py
--rw-r--r--   0        0        0     2329 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_allowed_income_types_request.py
--rw-r--r--   0        0        0      470 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_dian_invoice_type.py
--rw-r--r--   0        0        0      132 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_dian_payment_method.py
--rw-r--r--   0        0        0      986 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_sat_invoice_type.py
--rw-r--r--   0        0        0      131 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_sat_payment_method.py
--rw-r--r--   0        0        0      119 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_invoice_type.py
--rw-r--r--   0        0        0      923 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_link_access_mode_request.py
--rw-r--r--   0        0        0      130 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_link_access_mode_response.py
--rw-r--r--   0        0        0      123 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_link_refresh_rate.py
--rw-r--r--   0        0        0     1144 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_link_status.py
--rw-r--r--   0        0        0      869 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_loan_data_fee_type.py
--rw-r--r--   0        0        0      513 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_loan_data_interest_rate_type.py
--rw-r--r--   0        0        0      636 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_intent_holder_type_pse.py
--rw-r--r--   0        0        0     1196 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_intent_status.py
--rw-r--r--   0        0        0      728 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_link_allowed_payment_method.py
--rw-r--r--   0        0        0      711 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_link_provider.py
--rw-r--r--   0        0        0      981 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_links_status.py
--rw-r--r--   0        0        0      682 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payment_transaction_type.py
--rw-r--r--   0        0        0      571 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payments_country.py
--rw-r--r--   0        0        0      586 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_payments_currency.py
--rw-r--r--   0        0        0      416 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_receivable_transaction_fee_type.py
--rw-r--r--   0        0        0      930 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_receivable_transaction_status.py
--rw-r--r--   0        0        0      133 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_receivable_transaction_type.py
--rw-r--r--   0        0        0     2023 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_category.py
--rw-r--r--   0        0        0      513 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_frequency.py
--rw-r--r--   0        0        0      552 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_payment_type.py
--rw-r--r--   0        0        0      760 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_tax_compliance_status_outcome.py
--rw-r--r--   0        0        0      526 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_payment_status.py
--rw-r--r--   0        0        0      544 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_receiver_nationality.py
--rw-r--r--   0        0        0      735 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_type.py
--rw-r--r--   0        0        0      129 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_transaction_bill_status.py
--rw-r--r--   0        0        0      127 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_transaction_category.py
--rw-r--r--   0        0        0      125 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_transaction_status.py
--rw-r--r--   0        0        0      130 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_transaction_subcategory.py
--rw-r--r--   0        0        0      123 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/enum_transaction_type.py
--rw-r--r--   0        0        0     2117 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/equity_statement_business.py
--rw-r--r--   0        0        0     1137 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/equity_statement_individual.py
--rw-r--r--   0        0        0     2410 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/eyod_income_verification_body_request.py
--rw-r--r--   0        0        0     1525 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/gross_income_individual.py
--rw-r--r--   0        0        0     1067 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_bank_account_information_pse.py
--rw-r--r--   0        0        0     1089 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_bank_account_pse.py
--rw-r--r--   0        0        0     1045 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_business_pse.py
--rw-r--r--   0        0        0     1179 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_business_response_pse.py
--rw-r--r--   0        0        0     1189 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_business_ofpi.py
--rw-r--r--   0        0        0     1073 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_business_ofpi_response.py
--rw-r--r--   0        0        0      935 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_business_pse.py
--rw-r--r--   0        0        0      993 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_business_pse_response.py
--rw-r--r--   0        0        0     1290 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_individual_ofpi.py
--rw-r--r--   0        0        0     1174 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_information_individual_ofpi_response.py
--rw-r--r--   0        0        0     1043 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_response_ofpi.py
--rw-r--r--   0        0        0      402 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/holder_response_ofpi_information.py
--rw-r--r--   0        0        0     4077 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/income.py
--rw-r--r--   0        0        0     4769 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/income_streams_body.py
--rw-r--r--   0        0        0     1666 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/incomes_paginated_response.py
--rw-r--r--   0        0        0     3939 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution.py
--rw-r--r--   0        0        0     1205 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution_account.py
--rw-r--r--   0        0        0     1989 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution_down_error.py
--rw-r--r--   0        0        0     2062 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution_form_field.py
--rw-r--r--   0        0        0     1894 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution_inactive_error.py
--rw-r--r--   0        0        0     2011 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institution_unavailable_error.py
--rw-r--r--   0        0        0      937 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institutions_feature.py
--rw-r--r--   0        0        0     1937 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institutions_form_field.py
--rw-r--r--   0        0        0     1513 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institutions_form_field_values.py
--rw-r--r--   0        0        0     1691 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/institutions_paginated_response.py
--rw-r--r--   0        0        0     2002 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invalid_access_mode.py
--rw-r--r--   0        0        0     1936 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invalid_link_error.py
--rw-r--r--   0        0        0     1967 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invalid_period_error.py
--rw-r--r--   0        0        0     2666 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio.py
--rw-r--r--   0        0        0     4088 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument.py
--rw-r--r--   0        0        0     1056 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_fees.py
--rw-r--r--   0        0        0     1465 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_interest_rate.py
--rw-r--r--   0        0        0     1008 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_public_id.py
--rw-r--r--   0        0        0      952 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py
--rw-r--r--   0        0        0     1751 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/investments_portfolios_paginated_response.py
--rw-r--r--   0        0        0     2518 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_detail_dian.py
--rw-r--r--   0        0        0     1418 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_detail_retained_tax_sat.py
--rw-r--r--   0        0        0     3178 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_detail_sat.py
--rw-r--r--   0        0        0     7893 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_dian.py
--rw-r--r--   0        0        0     2326 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_sender_details_dian.py
--rw-r--r--   0        0        0     1066 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_warnings_dian.py
--rw-r--r--   0        0        0      925 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_warnings_sat.py
--rw-r--r--   0        0        0     9760 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoice_with_id_sat.py
--rw-r--r--   0        0        0     2919 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payments_dian.py
--rw-r--r--   0        0        0     2063 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payments_related_documents_dian.py
--rw-r--r--   0        0        0     2024 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payments_related_documents_sat.py
--rw-r--r--   0        0        0     3037 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payments_sat.py
--rw-r--r--   0        0        0     2066 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payroll_dian.py
--rw-r--r--   0        0        0     1782 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_payroll_sat.py
--rw-r--r--   0        0        0     2343 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_receiver_details_dian.py
--rw-r--r--   0        0        0     1809 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_response_paginated_response.py
--rw-r--r--   0        0        0      260 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/invoices_response_paginated_response_results_item.py
--rw-r--r--   0        0        0     1249 2023-05-12 23:30:30.152128 fern_belvo-0.0.28/src/belvo/types/last_error_invalid_credentials.py
--rw-r--r--   0        0        0     1227 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/last_error_invalid_token.py
--rw-r--r--   0        0        0     1257 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/last_error_login_error.py
--rw-r--r--   0        0        0     1243 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/last_error_payment_error.py
--rw-r--r--   0        0        0     1289 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/last_error_session_expired.py
--rw-r--r--   0        0        0     1261 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/last_error_two_factor.py
--rw-r--r--   0        0        0     2833 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/link.py
--rw-r--r--   0        0        0      554 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/list_payment_links_request_ordering.py
--rw-r--r--   0        0        0      521 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/list_payment_links_request_status.py
--rw-r--r--   0        0        0      356 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/list_tax_declarations_response.py
--rw-r--r--   0        0        0      586 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/list_tax_returns_response.py
--rw-r--r--   0        0        0     2699 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/login_error.py
--rw-r--r--   0        0        0      913 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/needs_redirect_content.py
--rw-r--r--   0        0        0      923 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/needs_redirect_content_pse.py
--rw-r--r--   0        0        0     1588 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/net_income_individual.py
--rw-r--r--   0        0        0     1660 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_ofpi.py
--rw-r--r--   0        0        0     2256 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py
--rw-r--r--   0        0        0     1673 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_pse.py
--rw-r--r--   0        0        0     2850 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_pse_type.py
--rw-r--r--   0        0        0     1665 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_credentials_required_pse.py
--rw-r--r--   0        0        0     2840 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_credentials_required_pse_type.py
--rw-r--r--   0        0        0     1676 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_customer_bank_accounts_pse.py
--rw-r--r--   0        0        0     2850 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py
--rw-r--r--   0        0        0     1595 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_needs_redirect_pse.py
--rw-r--r--   0        0        0     2780 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_needs_redirect_pse_type.py
--rw-r--r--   0        0        0     1573 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_failed.py
--rw-r--r--   0        0        0     2179 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_failed_type.py
--rw-r--r--   0        0        0     1700 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information.py
--rw-r--r--   0        0        0     1874 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_pse.py
--rw-r--r--   0        0        0     2890 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_pse_type.py
--rw-r--r--   0        0        0     2256 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_type.py
--rw-r--r--   0        0        0     1606 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_processing.py
--rw-r--r--   0        0        0     2207 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_processing_type.py
--rw-r--r--   0        0        0     1598 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_succeeded.py
--rw-r--r--   0        0        0     2200 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_succeeded_type.py
--rw-r--r--   0        0        0     2128 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_token_required_pse.py
--rw-r--r--   0        0        0     2780 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_display_token_required_pse_type.py
--rw-r--r--   0        0        0     1545 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_needs_redirect.py
--rw-r--r--   0        0        0     2130 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/next_step_needs_redirect_type.py
--rw-r--r--   0        0        0     1531 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/non_taxable_income_individual.py
--rw-r--r--   0        0        0     1703 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/not_found_error_body.py
--rw-r--r--   0        0        0     2545 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/owner.py
--rw-r--r--   0        0        0     1584 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/owner_document_id.py
--rw-r--r--   0        0        0     1661 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/owners_paginated_response.py
--rw-r--r--   0        0        0     1596 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/paginated_response_link.py
--rw-r--r--   0        0        0     1798 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/patch_body.py
--rw-r--r--   0        0        0     1479 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/patch_body_without_save_data.py
--rw-r--r--   0        0        0      241 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/patch_invoices_response_item.py
--rw-r--r--   0        0        0      876 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/patch_payment_intents_body_pse.py
--rw-r--r--   0        0        0     2677 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/patch_payment_method_details_pse.py
--rw-r--r--   0        0        0     2302 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_institution.py
--rw-r--r--   0        0        0     4025 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_ofpi.py
--rw-r--r--   0        0        0      846 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_ofpi_next_step.py
--rw-r--r--   0        0        0      462 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_ofpi_payment_method_details.py
--rw-r--r--   0        0        0     1733 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_paginated_response.py
--rw-r--r--   0        0        0     1549 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py
--rw-r--r--   0        0        0     1551 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py
--rw-r--r--   0        0        0     2222 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_pse.py
--rw-r--r--   0        0        0     1013 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py
--rw-r--r--   0        0        0     1030 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py
--rw-r--r--   0        0        0      983 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_pse.py
--rw-r--r--   0        0        0     4050 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_pse.py
--rw-r--r--   0        0        0      656 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_pse_last_error.py
--rw-r--r--   0        0        0      933 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intent_pse_next_step.py
--rw-r--r--   0        0        0     1644 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intents_payment_method_details_body_pse.py
--rw-r--r--   0        0        0      995 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_intents_payment_method_details_pse.py
--rw-r--r--   0        0        0     1499 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_callback_urls.py
--rw-r--r--   0        0        0     1408 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_callback_urls_response.py
--rw-r--r--   0        0        0     2547 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_list_ofpi.py
--rw-r--r--   0        0        0     2546 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_list_pse.py
--rw-r--r--   0        0        0     2331 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_ofpi.py
--rw-r--r--   0        0        0     1801 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_paginated_response.py
--rw-r--r--   0        0        0      287 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_paginated_response_results_item.py
--rw-r--r--   0        0        0     2326 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_link_pse.py
--rw-r--r--   0        0        0     1244 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_links_payment_method_details_body_ofpi.py
--rw-r--r--   0        0        0     1646 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_links_payment_method_details_body_pse.py
--rw-r--r--   0        0        0     1021 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_details_ofpi.py
--rw-r--r--   0        0        0      980 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_details_pse.py
--rw-r--r--   0        0        0     1530 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py
--rw-r--r--   0        0        0     1256 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_information_body_ofpi.py
--rw-r--r--   0        0        0     1390 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_information_body_pse.py
--rw-r--r--   0        0        0     1013 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_information_details_pse.py
--rw-r--r--   0        0        0      967 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_information_ofpi.py
--rw-r--r--   0        0        0     1043 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_method_information_pse.py
--rw-r--r--   0        0        0     2247 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_transaction.py
--rw-r--r--   0        0        0      313 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_transaction_payer.py
--rw-r--r--   0        0        0     1527 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payment_webhook.py
--rw-r--r--   0        0        0     1742 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payments_institutions_paginated_response.py
--rw-r--r--   0        0        0     1742 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payments_transactions_paginated_response.py
--rw-r--r--   0        0        0     1471 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payments_way.py
--rw-r--r--   0        0        0     1708 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/payments_webhooks_paginated_response.py
--rw-r--r--   0        0        0     1072 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/pension_income_statement_individual.py
--rw-r--r--   0        0        0      817 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/providers_pse.py
--rw-r--r--   0        0        0     2957 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/receivables_transaction.py
--rw-r--r--   0        0        0     1042 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/receivables_transaction_account.py
--rw-r--r--   0        0        0     1065 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/receivables_transaction_number_of_installments.py
--rw-r--r--   0        0        0     1750 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/receivables_transactions_paginated_response.py
--rw-r--r--   0        0        0     1026 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/recevables_transaction_fees.py
--rw-r--r--   0        0        0     1242 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/recurring_expense_source_transaction.py
--rw-r--r--   0        0        0     2895 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/recurring_expenses.py
--rw-r--r--   0        0        0     1735 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/recurring_expenses_paginated_response.py
--rw-r--r--   0        0        0     1120 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/reporting_id.py
--rw-r--r--   0        0        0     2051 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/request_timeout_error_body.py
--rw-r--r--   0        0        0     1454 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retention_breakdown.py
--rw-r--r--   0        0        0      244 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retrieve_invoices_response_item.py
--rw-r--r--   0        0        0      308 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retrieve_tax_declarations_response_item.py
--rw-r--r--   0        0        0      307 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retrieve_tax_returns_request_body.py
--rw-r--r--   0        0        0      457 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retrieve_tax_returns_response_item.py
--rw-r--r--   0        0        0      235 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/retrieve_tax_status_response.py
--rw-r--r--   0        0        0     1980 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights.py
--rw-r--r--   0        0        0     3951 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_balance_metrics.py
--rw-r--r--   0        0        0     3942 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_cashflow_metrics.py
--rw-r--r--   0        0        0     1093 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_credit_card_metrics.py
--rw-r--r--   0        0        0     1369 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_loans_metrics.py
--rw-r--r--   0        0        0     1711 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_paginated_response.py
--rw-r--r--   0        0        0     9169 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/risk_insights_transaction_metrics.py
--rw-r--r--   0        0        0     1176 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/secret_keys.py
--rw-r--r--   0        0        0     1694 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/secret_keys_paginated_response.py
--rw-r--r--   0        0        0     2013 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/session_expired_error.py
--rw-r--r--   0        0        0     1276 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/standard_request.py
--rw-r--r--   0        0        0     2491 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_assessment_business.py
--rw-r--r--   0        0        0     2771 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_assessment_individual.py
--rw-r--r--   0        0        0     1788 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_compliance_status.py
--rw-r--r--   0        0        0     1748 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_compliance_status_paginated_response.py
--rw-r--r--   0        0        0     2291 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_declaration_business.py
--rw-r--r--   0        0        0     1755 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_declaration_business_paginated.py
--rw-r--r--   0        0        0     2281 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_declaration_individual.py
--rw-r--r--   0        0        0     1765 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_declaration_individual_paginated.py
--rw-r--r--   0        0        0     1666 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_payer_information_business.py
--rw-r--r--   0        0        0     1489 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_payer_information_individual.py
--rw-r--r--   0        0        0     3880 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_retentions.py
--rw-r--r--   0        0        0     1716 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_retentions_paginated_response.py
--rw-r--r--   0        0        0      129 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_return_business.py
--rw-r--r--   0        0        0      136 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_return_business_monthly.py
--rw-r--r--   0        0        0      129 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_return_personal.py
--rw-r--r--   0        0        0      136 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_return_personal_monthly.py
--rw-r--r--   0        0        0      146 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_returns_business_monthly_paginated.py
--rw-r--r--   0        0        0      139 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_returns_business_paginated.py
--rw-r--r--   0        0        0     2175 2023-05-12 23:30:30.156130 fern_belvo-0.0.28/src/belvo/types/tax_returns_monthly_request.py
--rw-r--r--   0        0        0      146 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_returns_personal_monthly_paginated.py
--rw-r--r--   0        0        0      139 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_returns_personal_paginated.py
--rw-r--r--   0        0        0     1967 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_returns_yearly_request.py
--rw-r--r--   0        0        0     1089 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_address_between_street_dian.py
--rw-r--r--   0        0        0     1029 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_address_between_street_sat.py
--rw-r--r--   0        0        0     2076 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_address_dian.py
--rw-r--r--   0        0        0     1919 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_address_sat.py
--rw-r--r--   0        0        0     3269 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_dian.py
--rw-r--r--   0        0        0     1728 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_economic_activity_dian.py
--rw-r--r--   0        0        0     1328 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_economic_activity_sat.py
--rw-r--r--   0        0        0     1550 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_obligations_dian.py
--rw-r--r--   0        0        0     1357 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_obligations_sat.py
--rw-r--r--   0        0        0     1784 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_paginated_response.py
--rw-r--r--   0        0        0      247 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_paginated_response_results_item.py
--rw-r--r--   0        0        0     1179 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_regimens_dian.py
--rw-r--r--   0        0        0     1048 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_regimens_sat.py
--rw-r--r--   0        0        0     3194 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_sat.py
--rw-r--r--   0        0        0     2648 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_tax_payer_information_dian.py
--rw-r--r--   0        0        0     2672 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/tax_status_tax_payer_information_sat.py
--rw-r--r--   0        0        0     2428 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/token_required_response.py
--rw-r--r--   0        0        0     1605 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/token_required_response_token_generation_data.py
--rw-r--r--   0        0        0     2133 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/too_many_sessions_error.py
--rw-r--r--   0        0        0     3391 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction.py
--rw-r--r--   0        0        0     1052 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction_bank_account_body_pse.py
--rw-r--r--   0        0        0      138 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction_bank_account_ofpi.py
--rw-r--r--   0        0        0      325 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction_bank_account_pse.py
--rw-r--r--   0        0        0     1689 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction_credit_card_data.py
--rw-r--r--   0        0        0     1049 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transaction_merchant_data.py
--rw-r--r--   0        0        0     1691 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transactions_paginated_response.py
--rw-r--r--   0        0        0     2001 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/transactions_request.py
--rw-r--r--   0        0        0     1945 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/unauthorized_error_body.py
--rw-r--r--   0        0        0     2077 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/unconfirmed_link_error.py
--rw-r--r--   0        0        0     2013 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/unexpected_error.py
--rw-r--r--   0        0        0     2032 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/unsupported_operation_error.py
--rw-r--r--   0        0        0     2657 2023-05-12 23:30:30.160132 fern_belvo-0.0.28/src/belvo/types/validation_error.py
--rw-r--r--   0        0        0     3060 1970-01-01 00:00:00.000000 fern_belvo-0.0.28/PKG-INFO
+-rw-r--r--   0        0        0     2460 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/README.md
+-rw-r--r--   0        0        0      371 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/pyproject.toml
+-rw-r--r--   0        0        0    27716 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/__init__.py
+-rw-r--r--   0        0        0    12781 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/client.py
+-rw-r--r--   0        0        0      348 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/core/__init__.py
+-rw-r--r--   0        0        0      426 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/core/api_error.py
+-rw-r--r--   0        0        0     1047 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/core/datetime_utils.py
+-rw-r--r--   0        0        0     3710 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/core/jsonable_encoder.py
+-rw-r--r--   0        0        0      385 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/core/remove_none_from_headers.py
+-rw-r--r--   0        0        0      247 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/environment.py
+-rw-r--r--   0        0        0      594 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/__init__.py
+-rw-r--r--   0        0        0      346 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/bad_request_error.py
+-rw-r--r--   0        0        0      341 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/forbidden_error.py
+-rw-r--r--   0        0        0      323 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/internal_server_error.py
+-rw-r--r--   0        0        0      325 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/not_found_error.py
+-rw-r--r--   0        0        0      340 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/precondition_error.py
+-rw-r--r--   0        0        0      349 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/request_timeout_error.py
+-rw-r--r--   0        0        0      340 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/errors/unauthorized_error.py
+-rw-r--r--   0        0        0        0 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/py.typed
+-rw-r--r--   0        0        0     1252 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/__init__.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/accounts/__init__.py
+-rw-r--r--   0        0        0    24969 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/accounts/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/balances/__init__.py
+-rw-r--r--   0        0        0    23438 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/balances/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/bank_accounts/__init__.py
+-rw-r--r--   0        0        0    12881 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/bank_accounts/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/categorization/__init__.py
+-rw-r--r--   0        0        0     5136 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/categorization/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/customers/__init__.py
+-rw-r--r--   0        0        0    11285 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/customers/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/employment_records/__init__.py
+-rw-r--r--   0        0        0    14543 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/employment_records/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/income_verification/__init__.py
+-rw-r--r--   0        0        0     7011 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/income_verification/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/incomes/__init__.py
+-rw-r--r--   0        0        0    20690 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/incomes/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/institutions/__init__.py
+-rw-r--r--   0        0        0     8765 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/institutions/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/investment_portfolios/__init__.py
+-rw-r--r--   0        0        0    18632 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/investment_portfolios/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/invoices/__init__.py
+-rw-r--r--   0        0        0    24516 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/invoices/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/links/__init__.py
+-rw-r--r--   0        0        0    33898 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/links/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/owners/__init__.py
+-rw-r--r--   0        0        0    19773 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/owners/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_institutions/__init__.py
+-rw-r--r--   0        0        0     7761 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_institutions/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_intents/__init__.py
+-rw-r--r--   0        0        0    16753 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_intents/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_links/__init__.py
+-rw-r--r--   0        0        0    12471 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_links/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_transactions/__init__.py
+-rw-r--r--   0        0        0    10337 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_transactions/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_webhooks/__init__.py
+-rw-r--r--   0        0        0    12737 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/payment_webhooks/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/receivable_transactions/__init__.py
+-rw-r--r--   0        0        0    17393 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/receivable_transactions/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/recurring_expenses/__init__.py
+-rw-r--r--   0        0        0    20402 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/recurring_expenses/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/risk_insights/__init__.py
+-rw-r--r--   0        0        0    18655 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/risk_insights/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/secret_keys/__init__.py
+-rw-r--r--   0        0        0     5974 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/secret_keys/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.035003 fern_belvo-0.0.30/src/belvo/resources/tax_compliance_status/__init__.py
+-rw-r--r--   0        0        0    15905 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_compliance_status/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_declarations/__init__.py
+-rw-r--r--   0        0        0    17236 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_declarations/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_retentions/__init__.py
+-rw-r--r--   0        0        0    15901 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_retentions/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_returns/__init__.py
+-rw-r--r--   0        0        0    16912 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_returns/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_status/__init__.py
+-rw-r--r--   0        0        0    15773 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/tax_status/client.py
+-rw-r--r--   0        0        0       65 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/transactions/__init__.py
+-rw-r--r--   0        0        0    34291 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/resources/transactions/client.py
+-rw-r--r--   0        0        0    41108 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/__init__.py
+-rw-r--r--   0        0        0     1908 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/access_to_resource_denied.py
+-rw-r--r--   0        0        0     4506 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/account.py
+-rw-r--r--   0        0        0     2443 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_balance.py
+-rw-r--r--   0        0        0     2241 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_credit_data.py
+-rw-r--r--   0        0        0     1594 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_funds_data.py
+-rw-r--r--   0        0        0      958 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_funds_data_public_identifications.py
+-rw-r--r--   0        0        0     4780 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_loan_data.py
+-rw-r--r--   0        0        0      935 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_loan_data_fees.py
+-rw-r--r--   0        0        0     1191 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_loan_data_interest_rate.py
+-rw-r--r--   0        0        0     1674 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_paginated_response.py
+-rw-r--r--   0        0        0     1349 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/accounts_receivables_data.py
+-rw-r--r--   0        0        0     1588 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/annual_costs_and_deductions_statement_business.py
+-rw-r--r--   0        0        0     1883 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/annual_income_statement_business.py
+-rw-r--r--   0        0        0     1282 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/annual_income_statement_individual.py
+-rw-r--r--   0        0        0     1514 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/annual_totals_individual.py
+-rw-r--r--   0        0        0      992 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/asynchronous_accepted_202.py
+-rw-r--r--   0        0        0     1014 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bad_request_error_body_item.py
+-rw-r--r--   0        0        0     1827 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/balance.py
+-rw-r--r--   0        0        0     1671 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/balances_paginated_response.py
+-rw-r--r--   0        0        0     2531 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_business_pse.py
+-rw-r--r--   0        0        0     1189 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_details_ofpi.py
+-rw-r--r--   0        0        0      930 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_details_ofpi_pix.py
+-rw-r--r--   0        0        0     1196 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_details_open_finance.py
+-rw-r--r--   0        0        0      937 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_details_open_finance_pix.py
+-rw-r--r--   0        0        0     1094 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_holder_request_ofpi.py
+-rw-r--r--   0        0        0      356 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_holder_request_ofpi_information.py
+-rw-r--r--   0        0        0      966 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_information_content_pse.py
+-rw-r--r--   0        0        0     1077 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_information_pse.py
+-rw-r--r--   0        0        0     1852 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_ofpi_response.py
+-rw-r--r--   0        0        0      309 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_ofpi_response_details.py
+-rw-r--r--   0        0        0     1801 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_paginated_response.py
+-rw-r--r--   0        0        0      311 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_paginated_response_results_item.py
+-rw-r--r--   0        0        0      176 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/bank_account_pse_response.py
+-rw-r--r--   0        0        0     1439 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/beneficiary_bank_account_ofpi.py
+-rw-r--r--   0        0        0      356 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/beneficiary_bank_account_ofpi_details.py
+-rw-r--r--   0        0        0     1242 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/beneficiary_bank_account_pse.py
+-rw-r--r--   0        0        0      945 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/categorization.py
+-rw-r--r--   0        0        0     3020 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/categorization_body.py
+-rw-r--r--   0        0        0     2488 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/categorization_body_request.py
+-rw-r--r--   0        0        0     1052 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/categorization_merchant_data.py
+-rw-r--r--   0        0        0     3723 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge.py
+-rw-r--r--   0        0        0      342 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details.py
+-rw-r--r--   0        0        0      972 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_ofpi.py
+-rw-r--r--   0        0        0     1135 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_ofpi_content.py
+-rw-r--r--   0        0        0      959 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_pse.py
+-rw-r--r--   0        0        0     1127 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_pse_content.py
+-rw-r--r--   0        0        0      703 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/charge_status.py
+-rw-r--r--   0        0        0     1304 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_bank_account_ofpi.py
+-rw-r--r--   0        0        0      307 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_bank_account_ofpi_details.py
+-rw-r--r--   0        0        0     1863 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_bank_account_pse.py
+-rw-r--r--   0        0        0      284 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_bank_account_request.py
+-rw-r--r--   0        0        0      297 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_bank_account_response.py
+-rw-r--r--   0        0        0     1521 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_customer_ofpi.py
+-rw-r--r--   0        0        0     1517 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_customer_pse.py
+-rw-r--r--   0        0        0      261 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_customer_request.py
+-rw-r--r--   0        0        0      224 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_customer_response.py
+-rw-r--r--   0        0        0     2638 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_intent_pse.py
+-rw-r--r--   0        0        0      134 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_intent_pse_amount.py
+-rw-r--r--   0        0        0     2894 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_link_ofpi.py
+-rw-r--r--   0        0        0      135 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_link_ofpi_amount.py
+-rw-r--r--   0        0        0     2835 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_link_pse.py
+-rw-r--r--   0        0        0      132 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_payment_link_pse_amount.py
+-rw-r--r--   0        0        0      284 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_paymentlink_request.py
+-rw-r--r--   0        0        0      247 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/create_paymentlink_response.py
+-rw-r--r--   0        0        0     1855 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/customer_ofpi.py
+-rw-r--r--   0        0        0     1784 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/customer_paginated_response.py
+-rw-r--r--   0        0        0      238 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/customer_paginated_response_results_item.py
+-rw-r--r--   0        0        0     2229 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/customer_pse.py
+-rw-r--r--   0        0        0      297 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_bank_account_response.py
+-rw-r--r--   0        0        0      253 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_create_paymentlink_response.py
+-rw-r--r--   0        0        0      224 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_customer_response.py
+-rw-r--r--   0        0        0      237 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_invoice_response.py
+-rw-r--r--   0        0        0      301 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_tax_declaration_response.py
+-rw-r--r--   0        0        0      450 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_tax_return_response.py
+-rw-r--r--   0        0        0      233 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/detail_tax_status_response.py
+-rw-r--r--   0        0        0      972 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_confirmation_required_content_pse.py
+-rw-r--r--   0        0        0     1301 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_confirmation_required_ofpi.py
+-rw-r--r--   0        0        0     1001 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_credentials_required_content_pse.py
+-rw-r--r--   0        0        0     1279 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_customer_bank_accounts_content_pse.py
+-rw-r--r--   0        0        0      913 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_payment_failed.py
+-rw-r--r--   0        0        0     1055 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_payment_method_information_content_ofpi.py
+-rw-r--r--   0        0        0     1489 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_payment_method_information_content_pse.py
+-rw-r--r--   0        0        0      917 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_payment_processing.py
+-rw-r--r--   0        0        0      916 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_payment_succeeded.py
+-rw-r--r--   0        0        0      861 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/display_token_required_content_pse.py
+-rw-r--r--   0        0        0     1005 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/document_id_business.py
+-rw-r--r--   0        0        0     1007 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/document_id_individual.py
+-rw-r--r--   0        0        0     1277 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/document_information_business.py
+-rw-r--r--   0        0        0     1275 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/document_information_individual.py
+-rw-r--r--   0        0        0     2557 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record.py
+-rw-r--r--   0        0        0     2769 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_detail.py
+-rw-r--r--   0        0        0     1086 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_document_id.py
+-rw-r--r--   0        0        0     1317 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_employment_status_updates.py
+-rw-r--r--   0        0        0     1584 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_entitlement.py
+-rw-r--r--   0        0        0     1034 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_file.py
+-rw-r--r--   0        0        0     1843 2023-05-13 21:07:25.039003 fern_belvo-0.0.30/src/belvo/types/employment_record_personal_data.py
+-rw-r--r--   0        0        0     1495 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/employment_record_social_security_summary.py
+-rw-r--r--   0        0        0     1732 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/employment_records_paginated_response.py
+-rw-r--r--   0        0        0      123 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_account_category.py
+-rw-r--r--   0        0        0      630 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_bank_account_holder_type_ofpi.py
+-rw-r--r--   0        0        0      506 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_bank_account_holder_type_pse.py
+-rw-r--r--   0        0        0      850 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py
+-rw-r--r--   0        0        0     1179 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_categorization_account_category.py
+-rw-r--r--   0        0        0      668 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_categorization_account_holder_type.py
+-rw-r--r--   0        0        0      141 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_categorization_transaction_category.py
+-rw-r--r--   0        0        0      144 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_categorization_transaction_subcategory.py
+-rw-r--r--   0        0        0      702 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_categorization_transaction_type.py
+-rw-r--r--   0        0        0      592 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_customer_identifier_type_ofpi.py
+-rw-r--r--   0        0        0     1031 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_customer_identifier_type_pse.py
+-rw-r--r--   0        0        0      699 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_customer_type.py
+-rw-r--r--   0        0        0      495 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_employment_record_document_type.py
+-rw-r--r--   0        0        0      532 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_employment_record_status.py
+-rw-r--r--   0        0        0     1719 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_employment_record_status_update_events.py
+-rw-r--r--   0        0        0      911 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_minimum_confidence_level_request.py
+-rw-r--r--   0        0        0      475 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_source_type.py
+-rw-r--r--   0        0        0      824 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_stream_confidence.py
+-rw-r--r--   0        0        0     1495 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_stream_frequency.py
+-rw-r--r--   0        0        0     2123 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_stream_type.py
+-rw-r--r--   0        0        0      758 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_verification_account_category.py
+-rw-r--r--   0        0        0      484 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_verification_account_holder_type.py
+-rw-r--r--   0        0        0      359 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_income_verification_type.py
+-rw-r--r--   0        0        0      862 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_institution_integration_type.py
+-rw-r--r--   0        0        0      630 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_institution_status.py
+-rw-r--r--   0        0        0      805 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_institution_type.py
+-rw-r--r--   0        0        0     1687 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_investment_portfolio_instrument_type.py
+-rw-r--r--   0        0        0     1084 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_investment_portfolio_type.py
+-rw-r--r--   0        0        0     2329 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_allowed_income_types_request.py
+-rw-r--r--   0        0        0      470 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_dian_invoice_type.py
+-rw-r--r--   0        0        0      132 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_dian_payment_method.py
+-rw-r--r--   0        0        0      986 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_sat_invoice_type.py
+-rw-r--r--   0        0        0      131 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_sat_payment_method.py
+-rw-r--r--   0        0        0      119 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_invoice_type.py
+-rw-r--r--   0        0        0      923 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_link_access_mode_request.py
+-rw-r--r--   0        0        0      130 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_link_access_mode_response.py
+-rw-r--r--   0        0        0      123 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_link_refresh_rate.py
+-rw-r--r--   0        0        0     1144 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_link_status.py
+-rw-r--r--   0        0        0      869 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_loan_data_fee_type.py
+-rw-r--r--   0        0        0      513 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_loan_data_interest_rate_type.py
+-rw-r--r--   0        0        0      636 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_intent_holder_type_pse.py
+-rw-r--r--   0        0        0     1196 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_intent_status.py
+-rw-r--r--   0        0        0      728 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_link_allowed_payment_method.py
+-rw-r--r--   0        0        0      711 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_link_provider.py
+-rw-r--r--   0        0        0      981 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_links_status.py
+-rw-r--r--   0        0        0      682 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payment_transaction_type.py
+-rw-r--r--   0        0        0      571 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payments_country.py
+-rw-r--r--   0        0        0      586 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_payments_currency.py
+-rw-r--r--   0        0        0      416 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_receivable_transaction_fee_type.py
+-rw-r--r--   0        0        0      930 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_receivable_transaction_status.py
+-rw-r--r--   0        0        0      133 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_receivable_transaction_type.py
+-rw-r--r--   0        0        0     2023 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_category.py
+-rw-r--r--   0        0        0      513 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_frequency.py
+-rw-r--r--   0        0        0      552 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_payment_type.py
+-rw-r--r--   0        0        0      760 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_tax_compliance_status_outcome.py
+-rw-r--r--   0        0        0      526 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_payment_status.py
+-rw-r--r--   0        0        0      544 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_receiver_nationality.py
+-rw-r--r--   0        0        0      735 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_type.py
+-rw-r--r--   0        0        0      129 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_transaction_bill_status.py
+-rw-r--r--   0        0        0      127 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_transaction_category.py
+-rw-r--r--   0        0        0      125 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_transaction_status.py
+-rw-r--r--   0        0        0      130 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_transaction_subcategory.py
+-rw-r--r--   0        0        0      123 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/enum_transaction_type.py
+-rw-r--r--   0        0        0     2117 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/equity_statement_business.py
+-rw-r--r--   0        0        0     1137 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/equity_statement_individual.py
+-rw-r--r--   0        0        0     2410 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/eyod_income_verification_body_request.py
+-rw-r--r--   0        0        0     1525 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/gross_income_individual.py
+-rw-r--r--   0        0        0     1067 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_bank_account_information_pse.py
+-rw-r--r--   0        0        0     1089 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_bank_account_pse.py
+-rw-r--r--   0        0        0     1045 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_business_pse.py
+-rw-r--r--   0        0        0     1179 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_business_response_pse.py
+-rw-r--r--   0        0        0     1189 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_business_ofpi.py
+-rw-r--r--   0        0        0     1073 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_business_ofpi_response.py
+-rw-r--r--   0        0        0      935 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_business_pse.py
+-rw-r--r--   0        0        0      993 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_business_pse_response.py
+-rw-r--r--   0        0        0     1290 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_individual_ofpi.py
+-rw-r--r--   0        0        0     1174 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_information_individual_ofpi_response.py
+-rw-r--r--   0        0        0     1043 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_response_ofpi.py
+-rw-r--r--   0        0        0      402 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/holder_response_ofpi_information.py
+-rw-r--r--   0        0        0     4077 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/income.py
+-rw-r--r--   0        0        0     4769 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/income_streams_body.py
+-rw-r--r--   0        0        0     1666 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/incomes_paginated_response.py
+-rw-r--r--   0        0        0     3939 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution.py
+-rw-r--r--   0        0        0     1205 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution_account.py
+-rw-r--r--   0        0        0     1989 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution_down_error.py
+-rw-r--r--   0        0        0     2062 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution_form_field.py
+-rw-r--r--   0        0        0     1894 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution_inactive_error.py
+-rw-r--r--   0        0        0     2011 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institution_unavailable_error.py
+-rw-r--r--   0        0        0      937 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institutions_feature.py
+-rw-r--r--   0        0        0     1937 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institutions_form_field.py
+-rw-r--r--   0        0        0     1513 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institutions_form_field_values.py
+-rw-r--r--   0        0        0     1691 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/institutions_paginated_response.py
+-rw-r--r--   0        0        0     2002 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invalid_access_mode.py
+-rw-r--r--   0        0        0     1936 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invalid_link_error.py
+-rw-r--r--   0        0        0     1967 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invalid_period_error.py
+-rw-r--r--   0        0        0     2666 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio.py
+-rw-r--r--   0        0        0     4088 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument.py
+-rw-r--r--   0        0        0     1056 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_fees.py
+-rw-r--r--   0        0        0     1465 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_interest_rate.py
+-rw-r--r--   0        0        0     1008 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_public_id.py
+-rw-r--r--   0        0        0      952 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py
+-rw-r--r--   0        0        0     1751 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/investments_portfolios_paginated_response.py
+-rw-r--r--   0        0        0     2518 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_detail_dian.py
+-rw-r--r--   0        0        0     1418 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_detail_retained_tax_sat.py
+-rw-r--r--   0        0        0     3178 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_detail_sat.py
+-rw-r--r--   0        0        0     7893 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_dian.py
+-rw-r--r--   0        0        0     2326 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_sender_details_dian.py
+-rw-r--r--   0        0        0     1066 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_warnings_dian.py
+-rw-r--r--   0        0        0      925 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_warnings_sat.py
+-rw-r--r--   0        0        0     9760 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoice_with_id_sat.py
+-rw-r--r--   0        0        0     2919 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payments_dian.py
+-rw-r--r--   0        0        0     2063 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payments_related_documents_dian.py
+-rw-r--r--   0        0        0     2024 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payments_related_documents_sat.py
+-rw-r--r--   0        0        0     3037 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payments_sat.py
+-rw-r--r--   0        0        0     2066 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payroll_dian.py
+-rw-r--r--   0        0        0     1782 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_payroll_sat.py
+-rw-r--r--   0        0        0     2343 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_receiver_details_dian.py
+-rw-r--r--   0        0        0     1809 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_response_paginated_response.py
+-rw-r--r--   0        0        0      260 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/invoices_response_paginated_response_results_item.py
+-rw-r--r--   0        0        0     1249 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/last_error_invalid_credentials.py
+-rw-r--r--   0        0        0     1227 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/last_error_invalid_token.py
+-rw-r--r--   0        0        0     1257 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/last_error_login_error.py
+-rw-r--r--   0        0        0     1243 2023-05-13 21:07:25.043003 fern_belvo-0.0.30/src/belvo/types/last_error_payment_error.py
+-rw-r--r--   0        0        0     1289 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/last_error_session_expired.py
+-rw-r--r--   0        0        0     1261 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/last_error_two_factor.py
+-rw-r--r--   0        0        0     2833 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/link.py
+-rw-r--r--   0        0        0      554 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/list_payment_links_request_ordering.py
+-rw-r--r--   0        0        0      521 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/list_payment_links_request_status.py
+-rw-r--r--   0        0        0      356 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/list_tax_declarations_response.py
+-rw-r--r--   0        0        0      586 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/list_tax_returns_response.py
+-rw-r--r--   0        0        0     2699 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/login_error.py
+-rw-r--r--   0        0        0      913 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/needs_redirect_content.py
+-rw-r--r--   0        0        0      923 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/needs_redirect_content_pse.py
+-rw-r--r--   0        0        0     1588 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/net_income_individual.py
+-rw-r--r--   0        0        0     1660 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_ofpi.py
+-rw-r--r--   0        0        0     2256 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py
+-rw-r--r--   0        0        0     1673 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_pse.py
+-rw-r--r--   0        0        0     2850 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_pse_type.py
+-rw-r--r--   0        0        0     1665 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_credentials_required_pse.py
+-rw-r--r--   0        0        0     2840 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_credentials_required_pse_type.py
+-rw-r--r--   0        0        0     1676 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_customer_bank_accounts_pse.py
+-rw-r--r--   0        0        0     2850 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py
+-rw-r--r--   0        0        0     1595 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_needs_redirect_pse.py
+-rw-r--r--   0        0        0     2780 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_needs_redirect_pse_type.py
+-rw-r--r--   0        0        0     1573 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_failed.py
+-rw-r--r--   0        0        0     2179 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_failed_type.py
+-rw-r--r--   0        0        0     1700 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information.py
+-rw-r--r--   0        0        0     1874 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_pse.py
+-rw-r--r--   0        0        0     2890 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_pse_type.py
+-rw-r--r--   0        0        0     2256 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_type.py
+-rw-r--r--   0        0        0     1606 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_processing.py
+-rw-r--r--   0        0        0     2207 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_processing_type.py
+-rw-r--r--   0        0        0     1598 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_succeeded.py
+-rw-r--r--   0        0        0     2200 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_succeeded_type.py
+-rw-r--r--   0        0        0     2128 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_token_required_pse.py
+-rw-r--r--   0        0        0     2780 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_display_token_required_pse_type.py
+-rw-r--r--   0        0        0     1545 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_needs_redirect.py
+-rw-r--r--   0        0        0     2130 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/next_step_needs_redirect_type.py
+-rw-r--r--   0        0        0     1531 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/non_taxable_income_individual.py
+-rw-r--r--   0        0        0     1703 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/not_found_error_body.py
+-rw-r--r--   0        0        0     2545 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/owner.py
+-rw-r--r--   0        0        0     1584 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/owner_document_id.py
+-rw-r--r--   0        0        0     1661 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/owners_paginated_response.py
+-rw-r--r--   0        0        0     1596 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/paginated_response_link.py
+-rw-r--r--   0        0        0     1798 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/patch_body.py
+-rw-r--r--   0        0        0     1479 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/patch_body_without_save_data.py
+-rw-r--r--   0        0        0      241 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/patch_invoices_response_item.py
+-rw-r--r--   0        0        0      876 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/patch_payment_intents_body_pse.py
+-rw-r--r--   0        0        0     2677 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/patch_payment_method_details_pse.py
+-rw-r--r--   0        0        0     2302 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_institution.py
+-rw-r--r--   0        0        0     4025 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_ofpi.py
+-rw-r--r--   0        0        0      846 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_ofpi_next_step.py
+-rw-r--r--   0        0        0      462 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_ofpi_payment_method_details.py
+-rw-r--r--   0        0        0     1733 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_paginated_response.py
+-rw-r--r--   0        0        0     1549 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py
+-rw-r--r--   0        0        0     1551 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py
+-rw-r--r--   0        0        0     2222 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0     1013 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py
+-rw-r--r--   0        0        0     1030 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py
+-rw-r--r--   0        0        0      983 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_pse.py
+-rw-r--r--   0        0        0     4050 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_pse.py
+-rw-r--r--   0        0        0      656 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_pse_last_error.py
+-rw-r--r--   0        0        0      933 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intent_pse_next_step.py
+-rw-r--r--   0        0        0     1644 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intents_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0      995 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_intents_payment_method_details_pse.py
+-rw-r--r--   0        0        0     1499 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_callback_urls.py
+-rw-r--r--   0        0        0     1408 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_callback_urls_response.py
+-rw-r--r--   0        0        0     2547 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_list_ofpi.py
+-rw-r--r--   0        0        0     2546 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_list_pse.py
+-rw-r--r--   0        0        0     2331 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_ofpi.py
+-rw-r--r--   0        0        0     1801 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_paginated_response.py
+-rw-r--r--   0        0        0      287 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_paginated_response_results_item.py
+-rw-r--r--   0        0        0     2326 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_link_pse.py
+-rw-r--r--   0        0        0     1244 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_links_payment_method_details_body_ofpi.py
+-rw-r--r--   0        0        0     1646 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_links_payment_method_details_body_pse.py
+-rw-r--r--   0        0        0     1021 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_details_ofpi.py
+-rw-r--r--   0        0        0      980 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_details_pse.py
+-rw-r--r--   0        0        0     1530 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py
+-rw-r--r--   0        0        0     1256 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_information_body_ofpi.py
+-rw-r--r--   0        0        0     1390 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_information_body_pse.py
+-rw-r--r--   0        0        0     1013 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_information_details_pse.py
+-rw-r--r--   0        0        0      967 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_information_ofpi.py
+-rw-r--r--   0        0        0     1043 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_method_information_pse.py
+-rw-r--r--   0        0        0     2247 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_transaction.py
+-rw-r--r--   0        0        0      313 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_transaction_payer.py
+-rw-r--r--   0        0        0     1527 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payment_webhook.py
+-rw-r--r--   0        0        0     1742 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payments_institutions_paginated_response.py
+-rw-r--r--   0        0        0     1742 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payments_transactions_paginated_response.py
+-rw-r--r--   0        0        0     1471 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payments_way.py
+-rw-r--r--   0        0        0     1708 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/payments_webhooks_paginated_response.py
+-rw-r--r--   0        0        0     1072 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/pension_income_statement_individual.py
+-rw-r--r--   0        0        0      817 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/providers_pse.py
+-rw-r--r--   0        0        0     2957 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/receivables_transaction.py
+-rw-r--r--   0        0        0     1042 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/receivables_transaction_account.py
+-rw-r--r--   0        0        0     1065 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/receivables_transaction_number_of_installments.py
+-rw-r--r--   0        0        0     1750 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/receivables_transactions_paginated_response.py
+-rw-r--r--   0        0        0     1026 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/recevables_transaction_fees.py
+-rw-r--r--   0        0        0     1242 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/recurring_expense_source_transaction.py
+-rw-r--r--   0        0        0     2895 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/recurring_expenses.py
+-rw-r--r--   0        0        0     1735 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/recurring_expenses_paginated_response.py
+-rw-r--r--   0        0        0     1120 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/reporting_id.py
+-rw-r--r--   0        0        0     2051 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/request_timeout_error_body.py
+-rw-r--r--   0        0        0     1454 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retention_breakdown.py
+-rw-r--r--   0        0        0      244 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retrieve_invoices_response_item.py
+-rw-r--r--   0        0        0      308 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retrieve_tax_declarations_response_item.py
+-rw-r--r--   0        0        0      307 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retrieve_tax_returns_request_body.py
+-rw-r--r--   0        0        0      457 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retrieve_tax_returns_response_item.py
+-rw-r--r--   0        0        0      235 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/retrieve_tax_status_response.py
+-rw-r--r--   0        0        0     1980 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights.py
+-rw-r--r--   0        0        0     3951 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_balance_metrics.py
+-rw-r--r--   0        0        0     3942 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_cashflow_metrics.py
+-rw-r--r--   0        0        0     1093 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_credit_card_metrics.py
+-rw-r--r--   0        0        0     1369 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_loans_metrics.py
+-rw-r--r--   0        0        0     1711 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_paginated_response.py
+-rw-r--r--   0        0        0     9169 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/risk_insights_transaction_metrics.py
+-rw-r--r--   0        0        0     1176 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/secret_keys.py
+-rw-r--r--   0        0        0     1694 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/secret_keys_paginated_response.py
+-rw-r--r--   0        0        0     2013 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/session_expired_error.py
+-rw-r--r--   0        0        0     1276 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/standard_request.py
+-rw-r--r--   0        0        0     2491 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_assessment_business.py
+-rw-r--r--   0        0        0     2771 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_assessment_individual.py
+-rw-r--r--   0        0        0     1788 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_compliance_status.py
+-rw-r--r--   0        0        0     1748 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_compliance_status_paginated_response.py
+-rw-r--r--   0        0        0     2291 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_declaration_business.py
+-rw-r--r--   0        0        0     1755 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_declaration_business_paginated.py
+-rw-r--r--   0        0        0     2281 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_declaration_individual.py
+-rw-r--r--   0        0        0     1765 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_declaration_individual_paginated.py
+-rw-r--r--   0        0        0     1666 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_payer_information_business.py
+-rw-r--r--   0        0        0     1489 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_payer_information_individual.py
+-rw-r--r--   0        0        0     3880 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_retentions.py
+-rw-r--r--   0        0        0     1716 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_retentions_paginated_response.py
+-rw-r--r--   0        0        0      129 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_return_business.py
+-rw-r--r--   0        0        0      136 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_return_business_monthly.py
+-rw-r--r--   0        0        0      129 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_return_personal.py
+-rw-r--r--   0        0        0      136 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_return_personal_monthly.py
+-rw-r--r--   0        0        0      146 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_business_monthly_paginated.py
+-rw-r--r--   0        0        0      139 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_business_paginated.py
+-rw-r--r--   0        0        0     2175 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_monthly_request.py
+-rw-r--r--   0        0        0      146 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_personal_monthly_paginated.py
+-rw-r--r--   0        0        0      139 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_personal_paginated.py
+-rw-r--r--   0        0        0     1967 2023-05-13 21:07:25.047003 fern_belvo-0.0.30/src/belvo/types/tax_returns_yearly_request.py
+-rw-r--r--   0        0        0     1089 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_address_between_street_dian.py
+-rw-r--r--   0        0        0     1029 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_address_between_street_sat.py
+-rw-r--r--   0        0        0     2076 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_address_dian.py
+-rw-r--r--   0        0        0     1919 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_address_sat.py
+-rw-r--r--   0        0        0     3269 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_dian.py
+-rw-r--r--   0        0        0     1728 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_economic_activity_dian.py
+-rw-r--r--   0        0        0     1328 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_economic_activity_sat.py
+-rw-r--r--   0        0        0     1550 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_obligations_dian.py
+-rw-r--r--   0        0        0     1357 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_obligations_sat.py
+-rw-r--r--   0        0        0     1784 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_paginated_response.py
+-rw-r--r--   0        0        0      247 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_paginated_response_results_item.py
+-rw-r--r--   0        0        0     1179 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_regimens_dian.py
+-rw-r--r--   0        0        0     1048 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_regimens_sat.py
+-rw-r--r--   0        0        0     3194 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_sat.py
+-rw-r--r--   0        0        0     2648 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_tax_payer_information_dian.py
+-rw-r--r--   0        0        0     2672 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/tax_status_tax_payer_information_sat.py
+-rw-r--r--   0        0        0     2428 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/token_required_response.py
+-rw-r--r--   0        0        0     1605 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/token_required_response_token_generation_data.py
+-rw-r--r--   0        0        0     2133 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/too_many_sessions_error.py
+-rw-r--r--   0        0        0     3391 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction.py
+-rw-r--r--   0        0        0     1052 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction_bank_account_body_pse.py
+-rw-r--r--   0        0        0      138 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction_bank_account_ofpi.py
+-rw-r--r--   0        0        0      325 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction_bank_account_pse.py
+-rw-r--r--   0        0        0     1689 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction_credit_card_data.py
+-rw-r--r--   0        0        0     1049 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transaction_merchant_data.py
+-rw-r--r--   0        0        0     1691 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transactions_paginated_response.py
+-rw-r--r--   0        0        0     2001 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/transactions_request.py
+-rw-r--r--   0        0        0     1945 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/unauthorized_error_body.py
+-rw-r--r--   0        0        0     2077 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/unconfirmed_link_error.py
+-rw-r--r--   0        0        0     2013 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/unexpected_error.py
+-rw-r--r--   0        0        0     2032 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/unsupported_operation_error.py
+-rw-r--r--   0        0        0     2657 2023-05-13 21:07:25.051003 fern_belvo-0.0.30/src/belvo/types/validation_error.py
+-rw-r--r--   0        0        0     2968 1970-01-01 00:00:00.000000 fern_belvo-0.0.30/PKG-INFO
```

### Comparing `fern_belvo-0.0.28/README.md` & `fern_belvo-0.0.30/README.md`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/__init__.py` & `fern_belvo-0.0.30/src/belvo/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/core/datetime_utils.py` & `fern_belvo-0.0.30/src/belvo/core/datetime_utils.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/core/jsonable_encoder.py` & `fern_belvo-0.0.30/src/belvo/core/jsonable_encoder.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/errors/__init__.py` & `fern_belvo-0.0.30/src/belvo/errors/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/__init__.py` & `fern_belvo-0.0.30/src/belvo/resources/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/accounts/client.py` & `fern_belvo-0.0.30/src/belvo/resources/accounts/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/balances/client.py` & `fern_belvo-0.0.30/src/belvo/resources/balances/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/bank_accounts/client.py` & `fern_belvo-0.0.30/src/belvo/resources/bank_accounts/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/categorization/client.py` & `fern_belvo-0.0.30/src/belvo/resources/categorization/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/customers/client.py` & `fern_belvo-0.0.30/src/belvo/resources/customers/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/employment_records/client.py` & `fern_belvo-0.0.30/src/belvo/resources/employment_records/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/income_verification/client.py` & `fern_belvo-0.0.30/src/belvo/resources/income_verification/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/incomes/client.py` & `fern_belvo-0.0.30/src/belvo/resources/incomes/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/institutions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/institutions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/investment_portfolios/client.py` & `fern_belvo-0.0.30/src/belvo/resources/investment_portfolios/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/invoices/client.py` & `fern_belvo-0.0.30/src/belvo/resources/invoices/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/links/client.py` & `fern_belvo-0.0.30/src/belvo/resources/links/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/owners/client.py` & `fern_belvo-0.0.30/src/belvo/resources/owners/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/payment_institutions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/payment_institutions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/payment_intents/client.py` & `fern_belvo-0.0.30/src/belvo/resources/payment_intents/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/payment_links/client.py` & `fern_belvo-0.0.30/src/belvo/resources/payment_links/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/payment_transactions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/payment_transactions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/payment_webhooks/client.py` & `fern_belvo-0.0.30/src/belvo/resources/payment_webhooks/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/receivable_transactions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/receivable_transactions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/recurring_expenses/client.py` & `fern_belvo-0.0.30/src/belvo/resources/recurring_expenses/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/risk_insights/client.py` & `fern_belvo-0.0.30/src/belvo/resources/risk_insights/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/secret_keys/client.py` & `fern_belvo-0.0.30/src/belvo/resources/secret_keys/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/tax_compliance_status/client.py` & `fern_belvo-0.0.30/src/belvo/resources/tax_compliance_status/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/tax_declarations/client.py` & `fern_belvo-0.0.30/src/belvo/resources/tax_declarations/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/tax_retentions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/tax_retentions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/tax_returns/client.py` & `fern_belvo-0.0.30/src/belvo/resources/tax_returns/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/tax_status/client.py` & `fern_belvo-0.0.30/src/belvo/resources/tax_status/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/resources/transactions/client.py` & `fern_belvo-0.0.30/src/belvo/resources/transactions/client.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/__init__.py` & `fern_belvo-0.0.30/src/belvo/types/__init__.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/access_to_resource_denied.py` & `fern_belvo-0.0.30/src/belvo/types/access_to_resource_denied.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/account.py` & `fern_belvo-0.0.30/src/belvo/types/account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_balance.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_balance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_credit_data.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_credit_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_funds_data.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_funds_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_funds_data_public_identifications.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_funds_data_public_identifications.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_loan_data.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_loan_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_loan_data_fees.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_loan_data_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_loan_data_interest_rate.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_loan_data_interest_rate.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/accounts_receivables_data.py` & `fern_belvo-0.0.30/src/belvo/types/accounts_receivables_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/annual_costs_and_deductions_statement_business.py` & `fern_belvo-0.0.30/src/belvo/types/annual_costs_and_deductions_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/annual_income_statement_business.py` & `fern_belvo-0.0.30/src/belvo/types/annual_income_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/annual_income_statement_individual.py` & `fern_belvo-0.0.30/src/belvo/types/annual_income_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/annual_totals_individual.py` & `fern_belvo-0.0.30/src/belvo/types/annual_totals_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/asynchronous_accepted_202.py` & `fern_belvo-0.0.30/src/belvo/types/asynchronous_accepted_202.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bad_request_error_body_item.py` & `fern_belvo-0.0.30/src/belvo/types/bad_request_error_body_item.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/balance.py` & `fern_belvo-0.0.30/src/belvo/types/balance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/balances_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/balances_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_business_pse.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_details_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_details_ofpi_pix.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_details_ofpi_pix.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_details_open_finance.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_details_open_finance.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_details_open_finance_pix.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_details_open_finance_pix.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_holder_request_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_holder_request_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_information_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_information_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_information_pse.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_ofpi_response.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/bank_account_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/bank_account_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/beneficiary_bank_account_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/beneficiary_bank_account_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/beneficiary_bank_account_pse.py` & `fern_belvo-0.0.30/src/belvo/types/beneficiary_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/categorization.py` & `fern_belvo-0.0.30/src/belvo/types/categorization.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/categorization_body.py` & `fern_belvo-0.0.30/src/belvo/types/categorization_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/categorization_body_request.py` & `fern_belvo-0.0.30/src/belvo/types/categorization_body_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/categorization_merchant_data.py` & `fern_belvo-0.0.30/src/belvo/types/categorization_merchant_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge.py` & `fern_belvo-0.0.30/src/belvo/types/charge.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_ofpi_content.py` & `fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_ofpi_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge_payment_method_details_pse_content.py` & `fern_belvo-0.0.30/src/belvo/types/charge_payment_method_details_pse_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/charge_status.py` & `fern_belvo-0.0.30/src/belvo/types/charge_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_bank_account_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/create_bank_account_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_bank_account_pse.py` & `fern_belvo-0.0.30/src/belvo/types/create_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_customer_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/create_customer_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_customer_pse.py` & `fern_belvo-0.0.30/src/belvo/types/create_customer_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_payment_intent_pse.py` & `fern_belvo-0.0.30/src/belvo/types/create_payment_intent_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_payment_link_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/create_payment_link_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/create_payment_link_pse.py` & `fern_belvo-0.0.30/src/belvo/types/create_payment_link_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/customer_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/customer_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/customer_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/customer_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/customer_pse.py` & `fern_belvo-0.0.30/src/belvo/types/customer_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_confirmation_required_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/display_confirmation_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_confirmation_required_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/display_confirmation_required_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_credentials_required_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/display_credentials_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_customer_bank_accounts_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/display_customer_bank_accounts_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_payment_failed.py` & `fern_belvo-0.0.30/src/belvo/types/display_payment_failed.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_payment_method_information_content_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/display_payment_method_information_content_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_payment_method_information_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/display_payment_method_information_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_payment_processing.py` & `fern_belvo-0.0.30/src/belvo/types/display_payment_processing.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_payment_succeeded.py` & `fern_belvo-0.0.30/src/belvo/types/display_payment_succeeded.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/display_token_required_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/display_token_required_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/document_id_business.py` & `fern_belvo-0.0.30/src/belvo/types/document_id_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/document_id_individual.py` & `fern_belvo-0.0.30/src/belvo/types/document_id_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/document_information_business.py` & `fern_belvo-0.0.30/src/belvo/types/document_information_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/document_information_individual.py` & `fern_belvo-0.0.30/src/belvo/types/document_information_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_detail.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_detail.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_document_id.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_document_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_employment_status_updates.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_employment_status_updates.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_entitlement.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_entitlement.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_file.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_file.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_personal_data.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_personal_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_record_social_security_summary.py` & `fern_belvo-0.0.30/src/belvo/types/employment_record_social_security_summary.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/employment_records_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/employment_records_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_bank_account_holder_type_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/enum_bank_account_holder_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/enum_bank_account_pix_account_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_categorization_account_category.py` & `fern_belvo-0.0.30/src/belvo/types/enum_categorization_account_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_categorization_account_holder_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_categorization_account_holder_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_categorization_transaction_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_categorization_transaction_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_customer_identifier_type_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/enum_customer_identifier_type_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_customer_identifier_type_pse.py` & `fern_belvo-0.0.30/src/belvo/types/enum_customer_identifier_type_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_customer_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_customer_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_employment_record_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_employment_record_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_employment_record_status_update_events.py` & `fern_belvo-0.0.30/src/belvo/types/enum_employment_record_status_update_events.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_income_minimum_confidence_level_request.py` & `fern_belvo-0.0.30/src/belvo/types/enum_income_minimum_confidence_level_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_income_stream_confidence.py` & `fern_belvo-0.0.30/src/belvo/types/enum_income_stream_confidence.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_income_stream_frequency.py` & `fern_belvo-0.0.30/src/belvo/types/enum_income_stream_frequency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_income_stream_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_income_stream_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_income_verification_account_category.py` & `fern_belvo-0.0.30/src/belvo/types/enum_income_verification_account_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_institution_integration_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_institution_integration_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_institution_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_institution_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_institution_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_institution_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_investment_portfolio_instrument_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_investment_portfolio_instrument_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_investment_portfolio_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_investment_portfolio_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_invoice_allowed_income_types_request.py` & `fern_belvo-0.0.30/src/belvo/types/enum_invoice_allowed_income_types_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_invoice_sat_invoice_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_invoice_sat_invoice_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_link_access_mode_request.py` & `fern_belvo-0.0.30/src/belvo/types/enum_link_access_mode_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_link_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_link_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_loan_data_fee_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_loan_data_fee_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_loan_data_interest_rate_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_loan_data_interest_rate_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_intent_holder_type_pse.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_intent_holder_type_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_intent_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_intent_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_link_allowed_payment_method.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_link_allowed_payment_method.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_link_provider.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_link_provider.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_links_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_links_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payment_transaction_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payment_transaction_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payments_country.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payments_country.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_payments_currency.py` & `fern_belvo-0.0.30/src/belvo/types/enum_payments_currency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_receivable_transaction_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_receivable_transaction_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_category.py` & `fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_category.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_frequency.py` & `fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_frequency.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_recurring_expense_payment_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_recurring_expense_payment_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_tax_compliance_status_outcome.py` & `fern_belvo-0.0.30/src/belvo/types/enum_tax_compliance_status_outcome.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_payment_status.py` & `fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_payment_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_receiver_nationality.py` & `fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_receiver_nationality.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/enum_tax_retention_type.py` & `fern_belvo-0.0.30/src/belvo/types/enum_tax_retention_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/equity_statement_business.py` & `fern_belvo-0.0.30/src/belvo/types/equity_statement_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/equity_statement_individual.py` & `fern_belvo-0.0.30/src/belvo/types/equity_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/eyod_income_verification_body_request.py` & `fern_belvo-0.0.30/src/belvo/types/eyod_income_verification_body_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/gross_income_individual.py` & `fern_belvo-0.0.30/src/belvo/types/gross_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_bank_account_information_pse.py` & `fern_belvo-0.0.30/src/belvo/types/holder_bank_account_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_bank_account_pse.py` & `fern_belvo-0.0.30/src/belvo/types/holder_bank_account_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_business_pse.py` & `fern_belvo-0.0.30/src/belvo/types/holder_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_business_response_pse.py` & `fern_belvo-0.0.30/src/belvo/types/holder_business_response_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_business_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_business_ofpi_response.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_business_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_business_pse.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_business_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_business_pse_response.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_business_pse_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_individual_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_information_individual_ofpi_response.py` & `fern_belvo-0.0.30/src/belvo/types/holder_information_individual_ofpi_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/holder_response_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/holder_response_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/income.py` & `fern_belvo-0.0.30/src/belvo/types/income.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/income_streams_body.py` & `fern_belvo-0.0.30/src/belvo/types/income_streams_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/incomes_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/incomes_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution.py` & `fern_belvo-0.0.30/src/belvo/types/institution.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution_account.py` & `fern_belvo-0.0.30/src/belvo/types/institution_account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution_down_error.py` & `fern_belvo-0.0.30/src/belvo/types/institution_down_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution_form_field.py` & `fern_belvo-0.0.30/src/belvo/types/institution_form_field.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution_inactive_error.py` & `fern_belvo-0.0.30/src/belvo/types/institution_inactive_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institution_unavailable_error.py` & `fern_belvo-0.0.30/src/belvo/types/institution_unavailable_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institutions_feature.py` & `fern_belvo-0.0.30/src/belvo/types/institutions_feature.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institutions_form_field.py` & `fern_belvo-0.0.30/src/belvo/types/institutions_form_field.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institutions_form_field_values.py` & `fern_belvo-0.0.30/src/belvo/types/institutions_form_field_values.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/institutions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/institutions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invalid_access_mode.py` & `fern_belvo-0.0.30/src/belvo/types/invalid_access_mode.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invalid_link_error.py` & `fern_belvo-0.0.30/src/belvo/types/invalid_link_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invalid_period_error.py` & `fern_belvo-0.0.30/src/belvo/types/invalid_period_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_fees.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_interest_rate.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_interest_rate.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_public_id.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_public_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolio_instrument_redemption_conditions.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/investments_portfolios_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/investments_portfolios_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_detail_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_detail_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_detail_retained_tax_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_detail_retained_tax_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_detail_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_detail_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_sender_details_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_sender_details_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_warnings_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_warnings_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_warnings_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_warnings_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoice_with_id_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoice_with_id_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payments_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payments_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payments_related_documents_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payments_related_documents_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payments_related_documents_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payments_related_documents_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payments_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payments_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payroll_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payroll_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_payroll_sat.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_payroll_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_receiver_details_dian.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_receiver_details_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/invoices_response_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/invoices_response_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_invalid_credentials.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_invalid_credentials.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_invalid_token.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_invalid_token.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_login_error.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_login_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_payment_error.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_payment_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_session_expired.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_session_expired.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/last_error_two_factor.py` & `fern_belvo-0.0.30/src/belvo/types/last_error_two_factor.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/link.py` & `fern_belvo-0.0.30/src/belvo/types/link.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/list_payment_links_request_ordering.py` & `fern_belvo-0.0.30/src/belvo/types/list_payment_links_request_ordering.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/list_payment_links_request_status.py` & `fern_belvo-0.0.30/src/belvo/types/list_payment_links_request_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/list_tax_returns_response.py` & `fern_belvo-0.0.30/src/belvo/types/list_tax_returns_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/login_error.py` & `fern_belvo-0.0.30/src/belvo/types/login_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/needs_redirect_content.py` & `fern_belvo-0.0.30/src/belvo/types/needs_redirect_content.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/needs_redirect_content_pse.py` & `fern_belvo-0.0.30/src/belvo/types/needs_redirect_content_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/net_income_individual.py` & `fern_belvo-0.0.30/src/belvo/types/net_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_ofpi_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_confirmation_required_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_confirmation_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_credentials_required_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_credentials_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_credentials_required_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_credentials_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_customer_bank_accounts_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_customer_bank_accounts_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_customer_bank_accounts_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_needs_redirect_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_needs_redirect_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_needs_redirect_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_needs_redirect_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_failed.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_failed.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_failed_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_failed_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_method_information_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_method_information_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_processing.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_processing.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_processing_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_processing_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_succeeded.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_succeeded.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_payment_succeeded_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_payment_succeeded_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_token_required_pse.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_token_required_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_display_token_required_pse_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_display_token_required_pse_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_needs_redirect.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_needs_redirect.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/next_step_needs_redirect_type.py` & `fern_belvo-0.0.30/src/belvo/types/next_step_needs_redirect_type.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/non_taxable_income_individual.py` & `fern_belvo-0.0.30/src/belvo/types/non_taxable_income_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/not_found_error_body.py` & `fern_belvo-0.0.30/src/belvo/types/not_found_error_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/owner.py` & `fern_belvo-0.0.30/src/belvo/types/owner.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/owner_document_id.py` & `fern_belvo-0.0.30/src/belvo/types/owner_document_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/owners_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/owners_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/paginated_response_link.py` & `fern_belvo-0.0.30/src/belvo/types/paginated_response_link.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/patch_body.py` & `fern_belvo-0.0.30/src/belvo/types/patch_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/patch_body_without_save_data.py` & `fern_belvo-0.0.30/src/belvo/types/patch_body_without_save_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/patch_payment_intents_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/patch_payment_intents_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/patch_payment_method_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/patch_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_institution.py` & `fern_belvo-0.0.30/src/belvo/types/payment_institution.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_ofpi_next_step.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_ofpi_next_step.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_business_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_individual_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_payment_method_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_pse_last_error.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_pse_last_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intent_pse_next_step.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intent_pse_next_step.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intents_payment_method_details_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intents_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_intents_payment_method_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_intents_payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_callback_urls.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_callback_urls.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_callback_urls_response.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_callback_urls_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_list_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_list_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_list_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_list_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_link_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_link_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_links_payment_method_details_body_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_links_payment_method_details_body_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_links_payment_method_details_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_links_payment_method_details_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_details_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_details_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_info_customer_bank_accounts_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_information_body_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_information_body_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_information_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_information_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_information_details_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_information_details_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_information_ofpi.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_information_ofpi.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_method_information_pse.py` & `fern_belvo-0.0.30/src/belvo/types/payment_method_information_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_transaction.py` & `fern_belvo-0.0.30/src/belvo/types/payment_transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payment_webhook.py` & `fern_belvo-0.0.30/src/belvo/types/payment_webhook.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payments_institutions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/payments_institutions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payments_transactions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/payments_transactions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payments_way.py` & `fern_belvo-0.0.30/src/belvo/types/payments_way.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/payments_webhooks_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/payments_webhooks_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/pension_income_statement_individual.py` & `fern_belvo-0.0.30/src/belvo/types/pension_income_statement_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/providers_pse.py` & `fern_belvo-0.0.30/src/belvo/types/providers_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/receivables_transaction.py` & `fern_belvo-0.0.30/src/belvo/types/receivables_transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/receivables_transaction_account.py` & `fern_belvo-0.0.30/src/belvo/types/receivables_transaction_account.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/receivables_transaction_number_of_installments.py` & `fern_belvo-0.0.30/src/belvo/types/receivables_transaction_number_of_installments.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/receivables_transactions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/receivables_transactions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/recevables_transaction_fees.py` & `fern_belvo-0.0.30/src/belvo/types/recevables_transaction_fees.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/recurring_expense_source_transaction.py` & `fern_belvo-0.0.30/src/belvo/types/recurring_expense_source_transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/recurring_expenses.py` & `fern_belvo-0.0.30/src/belvo/types/recurring_expenses.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/recurring_expenses_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/recurring_expenses_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/reporting_id.py` & `fern_belvo-0.0.30/src/belvo/types/reporting_id.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/request_timeout_error_body.py` & `fern_belvo-0.0.30/src/belvo/types/request_timeout_error_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/retention_breakdown.py` & `fern_belvo-0.0.30/src/belvo/types/retention_breakdown.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_balance_metrics.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_balance_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_cashflow_metrics.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_cashflow_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_credit_card_metrics.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_credit_card_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_loans_metrics.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_loans_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/risk_insights_transaction_metrics.py` & `fern_belvo-0.0.30/src/belvo/types/risk_insights_transaction_metrics.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/secret_keys.py` & `fern_belvo-0.0.30/src/belvo/types/secret_keys.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/secret_keys_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/secret_keys_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/session_expired_error.py` & `fern_belvo-0.0.30/src/belvo/types/session_expired_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/standard_request.py` & `fern_belvo-0.0.30/src/belvo/types/standard_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_assessment_business.py` & `fern_belvo-0.0.30/src/belvo/types/tax_assessment_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_assessment_individual.py` & `fern_belvo-0.0.30/src/belvo/types/tax_assessment_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_compliance_status.py` & `fern_belvo-0.0.30/src/belvo/types/tax_compliance_status.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_compliance_status_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/tax_compliance_status_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_declaration_business.py` & `fern_belvo-0.0.30/src/belvo/types/tax_declaration_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_declaration_business_paginated.py` & `fern_belvo-0.0.30/src/belvo/types/tax_declaration_business_paginated.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_declaration_individual.py` & `fern_belvo-0.0.30/src/belvo/types/tax_declaration_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_declaration_individual_paginated.py` & `fern_belvo-0.0.30/src/belvo/types/tax_declaration_individual_paginated.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_payer_information_business.py` & `fern_belvo-0.0.30/src/belvo/types/tax_payer_information_business.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_payer_information_individual.py` & `fern_belvo-0.0.30/src/belvo/types/tax_payer_information_individual.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_retentions.py` & `fern_belvo-0.0.30/src/belvo/types/tax_retentions.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_retentions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/tax_retentions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_returns_monthly_request.py` & `fern_belvo-0.0.30/src/belvo/types/tax_returns_monthly_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_returns_yearly_request.py` & `fern_belvo-0.0.30/src/belvo/types/tax_returns_yearly_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_address_between_street_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_address_between_street_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_address_between_street_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_address_between_street_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_address_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_address_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_address_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_address_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_economic_activity_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_economic_activity_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_economic_activity_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_economic_activity_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_obligations_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_obligations_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_obligations_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_obligations_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_regimens_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_regimens_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_regimens_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_regimens_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_tax_payer_information_dian.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_tax_payer_information_dian.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/tax_status_tax_payer_information_sat.py` & `fern_belvo-0.0.30/src/belvo/types/tax_status_tax_payer_information_sat.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/token_required_response.py` & `fern_belvo-0.0.30/src/belvo/types/token_required_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/token_required_response_token_generation_data.py` & `fern_belvo-0.0.30/src/belvo/types/token_required_response_token_generation_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/too_many_sessions_error.py` & `fern_belvo-0.0.30/src/belvo/types/too_many_sessions_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transaction.py` & `fern_belvo-0.0.30/src/belvo/types/transaction.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transaction_bank_account_body_pse.py` & `fern_belvo-0.0.30/src/belvo/types/transaction_bank_account_body_pse.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transaction_credit_card_data.py` & `fern_belvo-0.0.30/src/belvo/types/transaction_credit_card_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transaction_merchant_data.py` & `fern_belvo-0.0.30/src/belvo/types/transaction_merchant_data.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transactions_paginated_response.py` & `fern_belvo-0.0.30/src/belvo/types/transactions_paginated_response.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/transactions_request.py` & `fern_belvo-0.0.30/src/belvo/types/transactions_request.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/unauthorized_error_body.py` & `fern_belvo-0.0.30/src/belvo/types/unauthorized_error_body.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/unconfirmed_link_error.py` & `fern_belvo-0.0.30/src/belvo/types/unconfirmed_link_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/unexpected_error.py` & `fern_belvo-0.0.30/src/belvo/types/unexpected_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/unsupported_operation_error.py` & `fern_belvo-0.0.30/src/belvo/types/unsupported_operation_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/src/belvo/types/validation_error.py` & `fern_belvo-0.0.30/src/belvo/types/validation_error.py`

 * *Files identical despite different names*

### Comparing `fern_belvo-0.0.28/PKG-INFO` & `fern_belvo-0.0.30/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,22 +1,20 @@
 Metadata-Version: 2.1
 Name: fern-belvo
-Version: 0.0.28
+Version: 0.0.30
 Summary: 
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: backports-cached_property (==1.0.2)
 Requires-Dist: httpx (==0.23.3)
 Requires-Dist: pydantic (>=1.9.2,<2.0.0)
-Requires-Dist: types-backports (==0.1.3)
 Description-Content-Type: text/markdown
 
 
 # Belvo Python Library
 
 [![pypi](https://img.shields.io/pypi/v/fern-belvo.svg)](https://pypi.python.org/pypi/fern-belvo)
 [![fern shield](https://img.shields.io/badge/%F0%9F%8C%BF-SDK%20generated%20by%20Fern-brightgreen)](https://github.com/fern-api/fern)
```

