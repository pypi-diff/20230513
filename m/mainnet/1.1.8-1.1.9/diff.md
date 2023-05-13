# Comparing `tmp/mainnet-1.1.8.tar.gz` & `tmp/mainnet-1.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/mainnet-1.1.8.tar", last modified: Fri Apr 28 15:28:21 2023, max compression
+gzip compressed data, was "dist/mainnet-1.1.9.tar", last modified: Thu May  4 10:40:19 2023, max compression
```

## Comparing `mainnet-1.1.8.tar` & `mainnet-1.1.9.tar`

### file list

```diff
@@ -1,332 +1,332 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/
--rw-r--r--   0 runner    (1001) docker     (123)      415 2023-04-28 15:28:21.000000 mainnet-1.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    26887 2023-04-28 15:28:16.000000 mainnet-1.1.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet/
--rw-r--r--   0 runner    (1001) docker     (123)    11667 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet/api/
--rw-r--r--   0 runner    (1001) docker     (123)      823 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    25442 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/contract_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    25428 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/contract_escrow_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    31417 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/faucet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     6238 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/mine_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    33290 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/smartbch_contract_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    59168 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/smartbch_sep20_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    55917 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/smartbch_wallet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    18227 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/util_api.py
--rw-r--r--   0 runner    (1001) docker     (123)   154240 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/wallet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    43177 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/wallet_bcmr_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    12272 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/wallet_signed_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    86667 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/wallet_slp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    13613 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/wallet_util_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     8401 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api/webhook_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    27387 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/api_client.py
--rw-r--r--   0 runner    (1001) docker     (123)    16450 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/configuration.py
--rw-r--r--   0 runner    (1001) docker     (123)     4488 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/exceptions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet/models/
--rw-r--r--   0 runner    (1001) docker     (123)    10495 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5246 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/auth_chain_element.py
--rw-r--r--   0 runner    (1001) docker     (123)     6071 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3998 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/cashscript_receipt.py
--rw-r--r--   0 runner    (1001) docker     (123)     3711 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract.py
--rw-r--r--   0 runner    (1001) docker     (123)    16948 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_fn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_fn_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3638 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6743 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4714 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4386 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/contract_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     6046 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/convert_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4240 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/create_signed_message_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3514 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)    10983 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/electrum_raw_transaction.py
--rw-r--r--   0 runner    (1001) docker     (123)     6376 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/electrum_raw_transaction_script_pub_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     4118 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/electrum_raw_transaction_script_sig.py
--rw-r--r--   0 runner    (1001) docker     (123)     7247 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/electrum_raw_transaction_vin.py
--rw-r--r--   0 runner    (1001) docker     (123)     5009 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/electrum_raw_transaction_vout.py
--rw-r--r--   0 runner    (1001) docker     (123)     5969 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/encode_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3961 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/encode_transaction_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3917 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/error.py
--rw-r--r--   0 runner    (1001) docker     (123)     3926 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_contract.py
--rw-r--r--   0 runner    (1001) docker     (123)     9020 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_fn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)    10302 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     6209 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4536 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/escrow_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7021 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_addresses_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4796 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_addrs_by_xpub_key_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3582 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_bch_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_bch_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3601 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_sbch_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3586 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_sbch_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4745 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_sep20_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_sep20_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4781 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_slp_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_testnet_slp_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_xpub_key_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6695 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/get_xpub_key_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7344 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/history_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3617 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/history_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/inline_object.py
--rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/inline_object1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/inline_object2.py
--rw-r--r--   0 runner    (1001) docker     (123)     3735 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/inline_object3.py
--rw-r--r--   0 runner    (1001) docker     (123)     3735 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/inline_object4.py
--rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/max_amount_to_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4154 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/mine_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4633 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/network_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)     2768 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/op_return_data.py
--rw-r--r--   0 runner    (1001) docker     (123)     5193 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/scalable_vector_graphic.py
--rw-r--r--   0 runner    (1001) docker     (123)     5259 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_max_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4966 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2780 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4452 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_request_item_any_of.py
--rw-r--r--   0 runner    (1001) docker     (123)    13440 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     5734 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/send_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/serialized_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/signed_message_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     5584 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/signed_message_response_details.py
--rw-r--r--   0 runner    (1001) docker     (123)     5713 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/signed_message_response_raw.py
--rw-r--r--   0 runner    (1001) docker     (123)     4642 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6680 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3517 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)    14019 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4315 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_genesis_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     8437 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4172 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_mint_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3537 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_outpoints_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     6363 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4546 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5463 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     3523 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     5087 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_send_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4884 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_token_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     9297 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_token_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     9275 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_utxo.py
--rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/slp_utxo_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     6605 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_deploy_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6075 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_deploy_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7680 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_estimate_gas_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3555 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_estimate_gas_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7560 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_fn_call_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6108 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_fn_call_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     7215 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4774 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4420 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_contract_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3557 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_max_amount_to_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     8916 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_overrides.py
--rw-r--r--   0 runner    (1001) docker     (123)     6158 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6126 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2812 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4526 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_request_item_any_of.py
--rw-r--r--   0 runner    (1001) docker     (123)     5693 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     5222 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_send_response_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4575 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_all_balances_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4812 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5986 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)    11666 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4465 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_genesis_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7465 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4342 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_mint_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     5674 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5399 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5565 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4836 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_token_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6920 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_sep20_token_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)    18358 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/smart_bch_transaction_receipt.py
--rw-r--r--   0 runner    (1001) docker     (123)     6255 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/submit_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/submit_transaction_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     9587 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/token_burn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     9714 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/token_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6700 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/token_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6835 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/token_mint_request_requests.py
--rw-r--r--   0 runner    (1001) docker     (123)     8624 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/token_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)    10549 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/transaction_history_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     4214 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/unit_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     5205 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/util_decode_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5599 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/utxo.py
--rw-r--r--   0 runner    (1001) docker     (123)     6552 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/utxo_token.py
--rw-r--r--   0 runner    (1001) docker     (123)     6388 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/verify_signed_message_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/verify_signed_message_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     7258 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/verify_signed_message_response_details.py
--rw-r--r--   0 runner    (1001) docker     (123)    11603 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     4545 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_mnemonic.py
--rw-r--r--   0 runner    (1001) docker     (123)     4930 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_named_exists_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5826 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_replace_named_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     4806 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     6003 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4456 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wallet_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     9131 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/watch_address_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3482 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/watch_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3385 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/wif.py
--rw-r--r--   0 runner    (1001) docker     (123)     3935 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/x_pub_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/x_pub_key_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3488 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/x_pub_key_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     4867 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/models/zero_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)    12400 2023-04-28 15:28:16.000000 mainnet-1.1.8/mainnet/rest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      415 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    12123 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-28 15:28:21.000000 mainnet-1.1.8/mainnet.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       69 2023-04-28 15:28:21.000000 mainnet-1.1.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1269 2023-04-28 15:28:20.000000 mainnet-1.1.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 15:28:21.000000 mainnet-1.1.8/test/
--rw-r--r--   0 runner    (1001) docker     (123)     1565 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_auth_chain_element.py
--rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1584 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_cashscript_receipt.py
--rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract.py
--rw-r--r--   0 runner    (1001) docker     (123)     1431 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1471 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_escrow_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2224 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_fn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2432 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_fn_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1537 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2224 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2477 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3596 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_contract_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1623 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_convert_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1753 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_create_signed_message_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     3044 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_electrum_raw_transaction.py
--rw-r--r--   0 runner    (1001) docker     (123)     1870 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_electrum_raw_transaction_script_pub_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_electrum_raw_transaction_script_sig.py
--rw-r--r--   0 runner    (1001) docker     (123)     1909 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_electrum_raw_transaction_vin.py
--rw-r--r--   0 runner    (1001) docker     (123)     1994 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_electrum_raw_transaction_vout.py
--rw-r--r--   0 runner    (1001) docker     (123)     2341 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_encode_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_encode_transaction_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1406 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_error.py
--rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_contract.py
--rw-r--r--   0 runner    (1001) docker     (123)     2066 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_fn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1522 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     5421 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_escrow_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1996 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_faucet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1680 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_addresses_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_addrs_by_xpub_key_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1547 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_bch_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_bch_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1557 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_sbch_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1569 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_sbch_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_sep20_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1580 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_sep20_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_slp_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_testnet_slp_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_xpub_key_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1705 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_get_xpub_key_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_history_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_history_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1648 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_inline_object.py
--rw-r--r--   0 runner    (1001) docker     (123)     1691 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_inline_object1.py
--rw-r--r--   0 runner    (1001) docker     (123)     1691 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_inline_object2.py
--rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_inline_object3.py
--rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_inline_object4.py
--rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_max_amount_to_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)      917 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_mine_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_mine_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1449 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_network_enum.py
--rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_op_return_data.py
--rw-r--r--   0 runner    (1001) docker     (123)     1726 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_scalable_vector_graphic.py
--rw-r--r--   0 runner    (1001) docker     (123)     2422 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1727 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_max_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1459 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_request_item_any_of.py
--rw-r--r--   0 runner    (1001) docker     (123)     1985 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_send_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_serialized_wallet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_signed_message_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_signed_message_response_details.py
--rw-r--r--   0 runner    (1001) docker     (123)     1648 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_signed_message_response_raw.py
--rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1720 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1650 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2487 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_genesis_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2127 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_mint_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_outpoints_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2282 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2350 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1903 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1677 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_send_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_token_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1941 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_token_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_utxo.py
--rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_slp_utxo_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2802 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_deploy_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_deploy_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2406 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_estimate_gas_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_estimate_gas_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_fn_call_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2623 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_fn_call_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2089 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_contract_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_deposit_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1859 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_max_amount_to_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1767 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_overrides.py
--rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2398 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1551 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_request_item_any_of.py
--rw-r--r--   0 runner    (1001) docker     (123)     1678 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_request_options.py
--rw-r--r--   0 runner    (1001) docker     (123)     1977 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_send_response_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_all_balances_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1969 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_balance_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_balance_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2732 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1982 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_genesis_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2491 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1970 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_mint_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2116 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_send_max_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1957 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_send_request_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_token_info_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_sep20_token_info_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smart_bch_transaction_receipt.py
--rw-r--r--   0 runner    (1001) docker     (123)     1815 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smartbch_contract_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2643 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smartbch_sep20_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2413 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_smartbch_wallet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_submit_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1660 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_submit_transaction_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_token_burn_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_token_genesis_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_token_mint_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_token_mint_request_requests.py
--rw-r--r--   0 runner    (1001) docker     (123)     1736 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_token_send_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1876 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_transaction_history_item.py
--rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_unit_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1306 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_util_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1740 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_util_decode_transaction_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1861 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_utxo.py
--rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_utxo_token.py
--rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_verify_signed_message_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_verify_signed_message_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1834 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_verify_signed_message_response_details.py
--rw-r--r--   0 runner    (1001) docker     (123)     5001 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_bcmr_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1826 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     1513 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_mnemonic.py
--rw-r--r--   0 runner    (1001) docker     (123)     1628 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_named_exists_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1736 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_replace_named_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1502 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1741 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_signed_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_slp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1217 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wallet_util_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1971 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_watch_address_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1537 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_watch_address_response.py
--rw-r--r--   0 runner    (1001) docker     (123)      976 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_webhook_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     1400 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_wif.py
--rw-r--r--   0 runner    (1001) docker     (123)     1430 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_x_pub_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     1797 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_x_pub_key_request.py
--rw-r--r--   0 runner    (1001) docker     (123)     1644 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_x_pub_key_response.py
--rw-r--r--   0 runner    (1001) docker     (123)     1579 2023-04-28 15:28:16.000000 mainnet-1.1.8/test/test_zero_balance_response.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-04 10:40:19.000000 mainnet-1.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    26887 2023-05-04 10:40:16.000000 mainnet-1.1.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/mainnet/
+-rw-r--r--   0 runner    (1001) docker     (123)    11667 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/mainnet/api/
+-rw-r--r--   0 runner    (1001) docker     (123)      823 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25442 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/contract_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25428 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/contract_escrow_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31417 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/faucet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6238 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/mine_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33290 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/smartbch_contract_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    59168 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/smartbch_sep20_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    55917 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/smartbch_wallet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18227 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/util_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)   154240 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/wallet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43177 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/wallet_bcmr_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12272 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/wallet_signed_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    86667 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/wallet_slp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13613 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/wallet_util_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8401 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api/webhook_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27387 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/api_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16450 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4488 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/mainnet/models/
+-rw-r--r--   0 runner    (1001) docker     (123)    10495 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5246 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/auth_chain_element.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6071 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3998 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/cashscript_receipt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3711 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16948 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_fn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_fn_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3638 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6743 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4714 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4386 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/contract_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6046 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/convert_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4240 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/create_signed_message_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3514 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10983 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/electrum_raw_transaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6376 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/electrum_raw_transaction_script_pub_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4118 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/electrum_raw_transaction_script_sig.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7247 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/electrum_raw_transaction_vin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5009 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/electrum_raw_transaction_vout.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5969 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/encode_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3961 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/encode_transaction_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3917 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/error.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3926 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9020 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_fn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10302 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6209 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4536 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/escrow_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7021 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_addresses_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4796 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_addrs_by_xpub_key_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3582 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_bch_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_bch_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3601 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_sbch_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3586 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_sbch_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4745 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_sep20_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_sep20_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4781 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_slp_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3516 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_testnet_slp_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_xpub_key_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6695 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/get_xpub_key_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7344 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/history_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3617 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/history_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/inline_object.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/inline_object1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4660 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/inline_object2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3735 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/inline_object3.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3735 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/inline_object4.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5659 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/max_amount_to_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4154 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/mine_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4633 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/network_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2768 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/op_return_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5193 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/scalable_vector_graphic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5259 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4195 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_max_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4966 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2780 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4452 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_request_item_any_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13440 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5734 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/send_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4163 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/serialized_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/signed_message_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5584 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/signed_message_response_details.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5713 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/signed_message_response_raw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4642 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6680 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3517 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14019 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4315 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_genesis_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8437 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4172 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_mint_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3537 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_outpoints_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6363 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4546 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5463 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3523 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5087 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_send_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4884 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_token_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9297 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_token_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9275 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_utxo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/slp_utxo_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6605 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_deploy_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6075 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_deploy_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7680 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_estimate_gas_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3555 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_estimate_gas_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7560 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_fn_call_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6108 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_fn_call_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3700 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7215 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4774 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4420 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_contract_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3557 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_max_amount_to_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8916 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_overrides.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6158 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6126 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2812 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4526 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_request_item_any_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5693 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5222 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_send_response_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4575 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_all_balances_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4812 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5986 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11666 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4465 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_genesis_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7465 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4342 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_mint_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5674 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5399 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5565 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4836 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_token_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6920 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_sep20_token_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18358 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/smart_bch_transaction_receipt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6255 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/submit_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3570 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/submit_transaction_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9587 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/token_burn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9714 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/token_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6700 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/token_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6835 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/token_mint_request_requests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8624 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/token_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10549 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/transaction_history_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4214 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/unit_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5205 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/util_decode_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5599 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/utxo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6552 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/utxo_token.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6388 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/verify_signed_message_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/verify_signed_message_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7258 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/verify_signed_message_response_details.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11603 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4545 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_mnemonic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4930 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_named_exists_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5826 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_replace_named_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4806 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6003 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4456 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wallet_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9131 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/watch_address_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3482 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/watch_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3385 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/wif.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3935 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/x_pub_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4358 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/x_pub_key_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3488 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/x_pub_key_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4867 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/models/zero_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12400 2023-05-04 10:40:16.000000 mainnet-1.1.9/mainnet/rest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/mainnet.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      415 2023-05-04 10:40:18.000000 mainnet-1.1.9/mainnet.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    12123 2023-05-04 10:40:18.000000 mainnet-1.1.9/mainnet.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-04 10:40:18.000000 mainnet-1.1.9/mainnet.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-05-04 10:40:18.000000 mainnet-1.1.9/mainnet.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-05-04 10:40:18.000000 mainnet-1.1.9/mainnet.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       69 2023-05-04 10:40:19.000000 mainnet-1.1.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1269 2023-05-04 10:40:18.000000 mainnet-1.1.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-04 10:40:19.000000 mainnet-1.1.9/test/
+-rw-r--r--   0 runner    (1001) docker     (123)     1565 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_auth_chain_element.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1584 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_cashscript_receipt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1447 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1431 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1471 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_escrow_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2224 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_fn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2432 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_fn_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1537 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2224 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2477 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3596 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_contract_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1623 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_convert_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1753 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_create_signed_message_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1616 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3044 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_electrum_raw_transaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1870 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_electrum_raw_transaction_script_pub_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1693 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_electrum_raw_transaction_script_sig.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1909 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_electrum_raw_transaction_vin.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1994 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_electrum_raw_transaction_vout.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2341 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_encode_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_encode_transaction_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1406 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_error.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1529 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_contract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2066 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_fn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1522 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5421 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3890 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_escrow_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1996 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_faucet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1680 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_addresses_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_addrs_by_xpub_key_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1547 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_bch_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_bch_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1557 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_sbch_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1569 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_sbch_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_sep20_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1580 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_sep20_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1642 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_slp_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_testnet_slp_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1559 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_xpub_key_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1705 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_get_xpub_key_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1773 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_history_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2018 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_history_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1648 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_inline_object.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1691 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_inline_object1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1691 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_inline_object2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_inline_object3.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_inline_object4.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_max_amount_to_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)      917 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_mine_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1523 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_mine_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1449 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_network_enum.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1426 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_op_return_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1726 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_scalable_vector_graphic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2422 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1727 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_max_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2156 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1459 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_request_item_any_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1985 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_send_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_serialized_wallet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_signed_message_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_signed_message_response_details.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1648 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_signed_message_response_raw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1720 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1650 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2487 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_genesis_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2127 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_mint_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_outpoints_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2282 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2350 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1903 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1677 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_send_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_token_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1941 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_token_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_utxo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_slp_utxo_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2802 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_deploy_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_deploy_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2406 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_estimate_gas_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_estimate_gas_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2351 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_fn_call_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2623 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_fn_call_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1629 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2089 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_contract_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_deposit_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1859 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_max_amount_to_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1767 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_overrides.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2398 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1551 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_request_item_any_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1678 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_request_options.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1977 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_send_response_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1901 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_all_balances_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1969 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_balance_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_balance_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2732 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1982 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_genesis_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2491 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1970 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_mint_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2116 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_send_max_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2888 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1957 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_send_request_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_token_info_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_sep20_token_info_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smart_bch_transaction_receipt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1815 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smartbch_contract_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2643 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smartbch_sep20_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2413 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_smartbch_wallet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_submit_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1660 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_submit_transaction_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_token_burn_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_token_genesis_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1959 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_token_mint_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_token_mint_request_requests.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1736 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_token_send_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1876 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_transaction_history_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_unit_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1306 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_util_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1740 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_util_decode_transaction_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1861 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_utxo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_utxo_token.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_verify_signed_message_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_verify_signed_message_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1834 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_verify_signed_message_response_details.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5001 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_bcmr_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1826 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1513 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_mnemonic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1628 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_named_exists_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1736 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_replace_named_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1502 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1741 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_signed_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3209 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_slp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1217 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wallet_util_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1971 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_watch_address_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1537 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_watch_address_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)      976 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_webhook_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1400 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_wif.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1430 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_x_pub_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1797 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_x_pub_key_request.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1644 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_x_pub_key_response.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1579 2023-05-04 10:40:16.000000 mainnet-1.1.9/test/test_zero_balance_response.py
```

### Comparing `mainnet-1.1.8/README.md` & `mainnet-1.1.9/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 This API is currently in *active* development, breaking changes may
 be made prior to official release of version 1.0.0.
 
 
 This Python package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:
 
-- API version: 1.1.7
+- API version: 1.1.8
 - Package version: 1.0.0
 - Build package: org.openapitools.codegen.languages.PythonClientCodegen
 
 ## Requirements.
 
 Python 2.7 and 3.4+
```

### Comparing `mainnet-1.1.8/mainnet/__init__.py` & `mainnet-1.1.9/mainnet/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 # flake8: noqa
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/__init__.py` & `mainnet-1.1.9/mainnet/api/__init__.py`

 * *Files identical despite different names*

### Comparing `mainnet-1.1.8/mainnet/api/contract_api.py` & `mainnet-1.1.9/mainnet/api/contract_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/contract_escrow_api.py` & `mainnet-1.1.9/mainnet/api/contract_escrow_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/faucet_api.py` & `mainnet-1.1.9/mainnet/api/faucet_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/mine_api.py` & `mainnet-1.1.9/mainnet/api/mine_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/smartbch_contract_api.py` & `mainnet-1.1.9/mainnet/api/smartbch_contract_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/smartbch_sep20_api.py` & `mainnet-1.1.9/mainnet/api/smartbch_sep20_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/smartbch_wallet_api.py` & `mainnet-1.1.9/mainnet/api/smartbch_wallet_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/util_api.py` & `mainnet-1.1.9/mainnet/api/util_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/wallet_api.py` & `mainnet-1.1.9/mainnet/api/wallet_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/wallet_bcmr_api.py` & `mainnet-1.1.9/mainnet/api/wallet_bcmr_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/wallet_signed_api.py` & `mainnet-1.1.9/mainnet/api/wallet_signed_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/wallet_slp_api.py` & `mainnet-1.1.9/mainnet/api/wallet_slp_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/wallet_util_api.py` & `mainnet-1.1.9/mainnet/api/wallet_util_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api/webhook_api.py` & `mainnet-1.1.9/mainnet/api/webhook_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/api_client.py` & `mainnet-1.1.9/mainnet/api_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # coding: utf-8
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 from __future__ import absolute_import
 
 import atexit
```

### Comparing `mainnet-1.1.8/mainnet/configuration.py` & `mainnet-1.1.9/mainnet/configuration.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
@@ -378,15 +378,15 @@
         """Gets the essential information for debugging.
 
         :return: The report for debugging.
         """
         return "Python SDK Debug Report:\n"\
                "OS: {env}\n"\
                "Python Version: {pyversion}\n"\
-               "Version of the API: 1.1.7\n"\
+               "Version of the API: 1.1.8\n"\
                "SDK Package Version: 1.0.0".\
                format(env=sys.platform, pyversion=sys.version)
 
     def get_host_settings(self):
         """Gets an array of host settings
 
         :return: An array of host settings
```

### Comparing `mainnet-1.1.8/mainnet/exceptions.py` & `mainnet-1.1.9/mainnet/exceptions.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import six
```

### Comparing `mainnet-1.1.8/mainnet/models/__init__.py` & `mainnet-1.1.9/mainnet/models/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 # flake8: noqa
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet/models/auth_chain_element.py` & `mainnet-1.1.9/mainnet/models/auth_chain_element.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/balance_request.py` & `mainnet-1.1.9/mainnet/models/balance_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/balance_response.py` & `mainnet-1.1.9/mainnet/models/balance_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/cashscript_receipt.py` & `mainnet-1.1.9/mainnet/models/cashscript_receipt.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract.py` & `mainnet-1.1.9/mainnet/models/contract.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_fn_request.py` & `mainnet-1.1.9/mainnet/models/contract_fn_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_fn_response.py` & `mainnet-1.1.9/mainnet/models/contract_fn_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_info_request.py` & `mainnet-1.1.9/mainnet/models/contract_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_info_response.py` & `mainnet-1.1.9/mainnet/models/contract_info_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_request.py` & `mainnet-1.1.9/mainnet/models/contract_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/contract_response.py` & `mainnet-1.1.9/mainnet/models/contract_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/convert_request.py` & `mainnet-1.1.9/mainnet/models/convert_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/create_signed_message_request.py` & `mainnet-1.1.9/mainnet/models/create_signed_message_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/deposit_address_response.py` & `mainnet-1.1.9/mainnet/models/deposit_address_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/electrum_raw_transaction.py` & `mainnet-1.1.9/mainnet/models/electrum_raw_transaction.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/electrum_raw_transaction_script_pub_key.py` & `mainnet-1.1.9/mainnet/models/electrum_raw_transaction_script_pub_key.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/electrum_raw_transaction_script_sig.py` & `mainnet-1.1.9/mainnet/models/electrum_raw_transaction_script_sig.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/electrum_raw_transaction_vin.py` & `mainnet-1.1.9/mainnet/models/electrum_raw_transaction_vin.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/electrum_raw_transaction_vout.py` & `mainnet-1.1.9/mainnet/models/electrum_raw_transaction_vout.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/encode_transaction_request.py` & `mainnet-1.1.9/mainnet/models/encode_transaction_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/encode_transaction_response.py` & `mainnet-1.1.9/mainnet/models/encode_transaction_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/error.py` & `mainnet-1.1.9/mainnet/models/error.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_contract.py` & `mainnet-1.1.9/mainnet/models/escrow_contract.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_fn_request.py` & `mainnet-1.1.9/mainnet/models/escrow_fn_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_info_request.py` & `mainnet-1.1.9/mainnet/models/escrow_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_info_response.py` & `mainnet-1.1.9/mainnet/models/escrow_info_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_request.py` & `mainnet-1.1.9/mainnet/models/escrow_request.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/escrow_response.py` & `mainnet-1.1.9/mainnet/models/escrow_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_addresses_response.py` & `mainnet-1.1.9/mainnet/models/get_addresses_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_addrs_by_xpub_key_request.py` & `mainnet-1.1.9/mainnet/models/get_addrs_by_xpub_key_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_bch_request.py` & `mainnet-1.1.9/mainnet/models/get_testnet_bch_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_bch_response.py` & `mainnet-1.1.9/mainnet/models/get_testnet_bch_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_sbch_request.py` & `mainnet-1.1.9/mainnet/models/get_testnet_sbch_request.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_sbch_response.py` & `mainnet-1.1.9/mainnet/models/get_testnet_sbch_response.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_sep20_request.py` & `mainnet-1.1.9/mainnet/models/get_testnet_sep20_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_sep20_response.py` & `mainnet-1.1.9/mainnet/models/get_testnet_sep20_response.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_slp_request.py` & `mainnet-1.1.9/mainnet/models/get_testnet_slp_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_testnet_slp_response.py` & `mainnet-1.1.9/mainnet/models/get_testnet_slp_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_xpub_key_info_request.py` & `mainnet-1.1.9/mainnet/models/get_xpub_key_info_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/get_xpub_key_info_response.py` & `mainnet-1.1.9/mainnet/models/get_xpub_key_info_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/history_request.py` & `mainnet-1.1.9/mainnet/models/history_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/history_response.py` & `mainnet-1.1.9/mainnet/models/history_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/inline_object.py` & `mainnet-1.1.9/mainnet/models/inline_object.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/inline_object1.py` & `mainnet-1.1.9/mainnet/models/inline_object1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/inline_object2.py` & `mainnet-1.1.9/mainnet/models/inline_object2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/inline_object3.py` & `mainnet-1.1.9/mainnet/models/inline_object3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/inline_object4.py` & `mainnet-1.1.9/mainnet/models/inline_object4.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/max_amount_to_send_request.py` & `mainnet-1.1.9/mainnet/models/max_amount_to_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/mine_request.py` & `mainnet-1.1.9/mainnet/models/mine_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/network_enum.py` & `mainnet-1.1.9/mainnet/models/network_enum.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/op_return_data.py` & `mainnet-1.1.9/mainnet/models/op_return_data.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/scalable_vector_graphic.py` & `mainnet-1.1.9/mainnet/models/scalable_vector_graphic.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_max_request.py` & `mainnet-1.1.9/mainnet/models/send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_max_response.py` & `mainnet-1.1.9/mainnet/models/send_max_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_request.py` & `mainnet-1.1.9/mainnet/models/send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_request_item.py` & `mainnet-1.1.9/mainnet/models/send_request_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_request_item_any_of.py` & `mainnet-1.1.9/mainnet/models/send_request_item_any_of.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_request_options.py` & `mainnet-1.1.9/mainnet/models/send_request_options.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/send_response.py` & `mainnet-1.1.9/mainnet/models/send_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/serialized_wallet.py` & `mainnet-1.1.9/mainnet/models/serialized_wallet.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/signed_message_response.py` & `mainnet-1.1.9/mainnet/models/signed_message_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/signed_message_response_details.py` & `mainnet-1.1.9/mainnet/models/signed_message_response_details.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/signed_message_response_raw.py` & `mainnet-1.1.9/mainnet/models/signed_message_response_raw.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_balance_request.py` & `mainnet-1.1.9/mainnet/models/slp_balance_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_balance_response.py` & `mainnet-1.1.9/mainnet/models/slp_balance_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_deposit_address_response.py` & `mainnet-1.1.9/mainnet/models/slp_deposit_address_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_genesis_request.py` & `mainnet-1.1.9/mainnet/models/slp_genesis_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_genesis_response.py` & `mainnet-1.1.9/mainnet/models/slp_genesis_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_mint_request.py` & `mainnet-1.1.9/mainnet/models/slp_mint_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_mint_response.py` & `mainnet-1.1.9/mainnet/models/slp_mint_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_outpoints_response.py` & `mainnet-1.1.9/mainnet/models/slp_outpoints_response.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_send_max_request.py` & `mainnet-1.1.9/mainnet/models/slp_send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_send_request.py` & `mainnet-1.1.9/mainnet/models/slp_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_send_request_item.py` & `mainnet-1.1.9/mainnet/models/slp_send_request_item.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_send_request_options.py` & `mainnet-1.1.9/mainnet/models/slp_send_request_options.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_send_response.py` & `mainnet-1.1.9/mainnet/models/slp_send_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_token_info_request.py` & `mainnet-1.1.9/mainnet/models/slp_token_info_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_token_info_response.py` & `mainnet-1.1.9/mainnet/models/slp_token_info_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_utxo.py` & `mainnet-1.1.9/mainnet/models/slp_utxo.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/slp_utxo_response.py` & `mainnet-1.1.9/mainnet/models/slp_utxo_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_deploy_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_deploy_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_deploy_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_deploy_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_estimate_gas_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_estimate_gas_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_estimate_gas_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_estimate_gas_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_fn_call_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_fn_call_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_fn_call_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_fn_call_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_info_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_info_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_info_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_contract_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_contract_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_deposit_address_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_deposit_address_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_max_amount_to_send_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_max_amount_to_send_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_overrides.py` & `mainnet-1.1.9/mainnet/models/smart_bch_overrides.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_max_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_request_item.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_request_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_request_item_any_of.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_request_item_any_of.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_request_options.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_request_options.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_send_response_item.py` & `mainnet-1.1.9/mainnet/models/smart_bch_send_response_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_all_balances_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_all_balances_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_balance_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_balance_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_balance_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_balance_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_genesis_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_genesis_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_genesis_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_genesis_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_mint_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_mint_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_mint_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_mint_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_max_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_send_request_item.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_send_request_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_token_info_request.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_token_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_sep20_token_info_response.py` & `mainnet-1.1.9/mainnet/models/smart_bch_sep20_token_info_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/smart_bch_transaction_receipt.py` & `mainnet-1.1.9/mainnet/models/smart_bch_transaction_receipt.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/submit_transaction_request.py` & `mainnet-1.1.9/mainnet/models/submit_transaction_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/submit_transaction_response.py` & `mainnet-1.1.9/mainnet/models/submit_transaction_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/token_burn_request.py` & `mainnet-1.1.9/mainnet/models/token_burn_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/token_genesis_request.py` & `mainnet-1.1.9/mainnet/models/token_genesis_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/token_mint_request.py` & `mainnet-1.1.9/mainnet/models/token_mint_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/token_mint_request_requests.py` & `mainnet-1.1.9/mainnet/models/token_mint_request_requests.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/token_send_request.py` & `mainnet-1.1.9/mainnet/models/token_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/transaction_history_item.py` & `mainnet-1.1.9/mainnet/models/transaction_history_item.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/unit_type.py` & `mainnet-1.1.9/mainnet/models/unit_type.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/util_decode_transaction_request.py` & `mainnet-1.1.9/mainnet/models/util_decode_transaction_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/utxo.py` & `mainnet-1.1.9/mainnet/models/utxo.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/utxo_token.py` & `mainnet-1.1.9/mainnet/models/utxo_token.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/verify_signed_message_request.py` & `mainnet-1.1.9/mainnet/models/verify_signed_message_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/verify_signed_message_response.py` & `mainnet-1.1.9/mainnet/models/verify_signed_message_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/verify_signed_message_response_details.py` & `mainnet-1.1.9/mainnet/models/verify_signed_message_response_details.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_info.py` & `mainnet-1.1.9/mainnet/models/wallet_info.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_mnemonic.py` & `mainnet-1.1.9/mainnet/models/wallet_mnemonic.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_named_exists_request.py` & `mainnet-1.1.9/mainnet/models/wallet_named_exists_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_replace_named_request.py` & `mainnet-1.1.9/mainnet/models/wallet_replace_named_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_request.py` & `mainnet-1.1.9/mainnet/models/wallet_request.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_response.py` & `mainnet-1.1.9/mainnet/models/wallet_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wallet_type.py` & `mainnet-1.1.9/mainnet/models/wallet_type.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/watch_address_request.py` & `mainnet-1.1.9/mainnet/models/watch_address_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/watch_address_response.py` & `mainnet-1.1.9/mainnet/models/watch_address_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/wif.py` & `mainnet-1.1.9/mainnet/models/wif.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/x_pub_key.py` & `mainnet-1.1.9/mainnet/models/x_pub_key.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/x_pub_key_request.py` & `mainnet-1.1.9/mainnet/models/x_pub_key_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/x_pub_key_response.py` & `mainnet-1.1.9/mainnet/models/x_pub_key_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/models/zero_balance_response.py` & `mainnet-1.1.9/mainnet/models/zero_balance_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 import pprint
 import re  # noqa: F401
```

### Comparing `mainnet-1.1.8/mainnet/rest.py` & `mainnet-1.1.9/mainnet/rest.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/mainnet.egg-info/SOURCES.txt` & `mainnet-1.1.9/mainnet.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mainnet-1.1.8/setup.py` & `mainnet-1.1.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
-    A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.1.8.   # noqa: E501
+    A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.1.9.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from setuptools import setup, find_packages  # noqa: H301
 
 NAME = "mainnet"
-VERSION = "1.1.8"
+VERSION = "1.1.9"
 # To install the library, run the following
 #
 # python setup.py install
 #
 # prerequisite: setuptools
 # http://pypi.python.org/pypi/setuptools
 
@@ -33,10 +33,10 @@
     url="",
     keywords=["OpenAPI", "OpenAPI-Generator", "Mainnet Cash"],
     install_requires=REQUIRES,
     packages=find_packages(exclude=["test", "tests"]),
     include_package_data=True,
     license="MIT Licence",
     long_description="""\
-    A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.1.8.   # noqa: E501
+    A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.1.9.   # noqa: E501
     """
 )
```

### Comparing `mainnet-1.1.8/test/test_auth_chain_element.py` & `mainnet-1.1.9/test/test_auth_chain_element.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_balance_request.py` & `mainnet-1.1.9/test/test_balance_request.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_balance_response.py` & `mainnet-1.1.9/test/test_balance_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_cashscript_receipt.py` & `mainnet-1.1.9/test/test_cashscript_receipt.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract.py` & `mainnet-1.1.9/test/test_contract.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_api.py` & `mainnet-1.1.9/test/test_contract_api.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_escrow_api.py` & `mainnet-1.1.9/test/test_contract_escrow_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_fn_request.py` & `mainnet-1.1.9/test/test_contract_fn_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_fn_response.py` & `mainnet-1.1.9/test/test_contract_fn_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_info_request.py` & `mainnet-1.1.9/test/test_contract_info_request.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_info_response.py` & `mainnet-1.1.9/test/test_contract_info_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_request.py` & `mainnet-1.1.9/test/test_contract_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_contract_response.py` & `mainnet-1.1.9/test/test_contract_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_convert_request.py` & `mainnet-1.1.9/test/test_convert_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_create_signed_message_request.py` & `mainnet-1.1.9/test/test_create_signed_message_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_deposit_address_response.py` & `mainnet-1.1.9/test/test_deposit_address_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_electrum_raw_transaction.py` & `mainnet-1.1.9/test/test_electrum_raw_transaction.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_electrum_raw_transaction_script_pub_key.py` & `mainnet-1.1.9/test/test_electrum_raw_transaction_script_pub_key.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_electrum_raw_transaction_script_sig.py` & `mainnet-1.1.9/test/test_electrum_raw_transaction_script_sig.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_electrum_raw_transaction_vin.py` & `mainnet-1.1.9/test/test_electrum_raw_transaction_vin.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_electrum_raw_transaction_vout.py` & `mainnet-1.1.9/test/test_electrum_raw_transaction_vout.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_encode_transaction_request.py` & `mainnet-1.1.9/test/test_encode_transaction_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_encode_transaction_response.py` & `mainnet-1.1.9/test/test_encode_transaction_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_error.py` & `mainnet-1.1.9/test/test_error.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_contract.py` & `mainnet-1.1.9/test/test_escrow_contract.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_fn_request.py` & `mainnet-1.1.9/test/test_escrow_fn_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_info_request.py` & `mainnet-1.1.9/test/test_escrow_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_info_response.py` & `mainnet-1.1.9/test/test_escrow_info_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_request.py` & `mainnet-1.1.9/test/test_escrow_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_escrow_response.py` & `mainnet-1.1.9/test/test_escrow_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_faucet_api.py` & `mainnet-1.1.9/test/test_faucet_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_addresses_response.py` & `mainnet-1.1.9/test/test_get_addresses_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_addrs_by_xpub_key_request.py` & `mainnet-1.1.9/test/test_get_addrs_by_xpub_key_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_bch_request.py` & `mainnet-1.1.9/test/test_get_testnet_bch_request.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_bch_response.py` & `mainnet-1.1.9/test/test_get_testnet_bch_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_sbch_request.py` & `mainnet-1.1.9/test/test_get_testnet_sbch_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_sbch_response.py` & `mainnet-1.1.9/test/test_get_testnet_sbch_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_sep20_request.py` & `mainnet-1.1.9/test/test_get_testnet_sep20_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_sep20_response.py` & `mainnet-1.1.9/test/test_get_testnet_sep20_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_slp_request.py` & `mainnet-1.1.9/test/test_get_testnet_slp_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_testnet_slp_response.py` & `mainnet-1.1.9/test/test_get_testnet_slp_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_xpub_key_info_request.py` & `mainnet-1.1.9/test/test_get_xpub_key_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_get_xpub_key_info_response.py` & `mainnet-1.1.9/test/test_get_xpub_key_info_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_history_request.py` & `mainnet-1.1.9/test/test_history_request.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_history_response.py` & `mainnet-1.1.9/test/test_history_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_inline_object.py` & `mainnet-1.1.9/test/test_inline_object.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_inline_object1.py` & `mainnet-1.1.9/test/test_inline_object2.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,56 +1,56 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
 import unittest
 import datetime
 
 import mainnet
-from mainnet.models.inline_object1 import InlineObject1  # noqa: E501
+from mainnet.models.inline_object2 import InlineObject2  # noqa: E501
 from mainnet.rest import ApiException
 
-class TestInlineObject1(unittest.TestCase):
-    """InlineObject1 unit test stubs"""
+class TestInlineObject2(unittest.TestCase):
+    """InlineObject2 unit test stubs"""
 
     def setUp(self):
         pass
 
     def tearDown(self):
         pass
 
     def make_instance(self, include_optional):
-        """Test InlineObject1
+        """Test InlineObject2
             include_option is a boolean, when False only required
             params are included, when True both required and
             optional params are included """
-        # model = mainnet.models.inline_object1.InlineObject1()  # noqa: E501
+        # model = mainnet.models.inline_object2.InlineObject2()  # noqa: E501
         if include_optional :
-            return InlineObject1(
+            return InlineObject2(
                 wallet_id = 'wif:testnet:cNfsPtqN2bMRS7vH5qd8tR8GMvgXyL5BjnGAKgZ8DYEiCrCCQcP6', 
                 token_id = '0'
             )
         else :
-            return InlineObject1(
+            return InlineObject2(
                 wallet_id = 'wif:testnet:cNfsPtqN2bMRS7vH5qd8tR8GMvgXyL5BjnGAKgZ8DYEiCrCCQcP6',
                 token_id = '0',
         )
 
-    def testInlineObject1(self):
-        """Test InlineObject1"""
+    def testInlineObject2(self):
+        """Test InlineObject2"""
         inst_req_only = self.make_instance(include_optional=False)
         inst_req_and_optional = self.make_instance(include_optional=True)
 
 
 if __name__ == '__main__':
     unittest.main()
```

### Comparing `mainnet-1.1.8/test/test_inline_object2.py` & `mainnet-1.1.9/test/test_inline_object1.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,56 +1,56 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
 
 import unittest
 import datetime
 
 import mainnet
-from mainnet.models.inline_object2 import InlineObject2  # noqa: E501
+from mainnet.models.inline_object1 import InlineObject1  # noqa: E501
 from mainnet.rest import ApiException
 
-class TestInlineObject2(unittest.TestCase):
-    """InlineObject2 unit test stubs"""
+class TestInlineObject1(unittest.TestCase):
+    """InlineObject1 unit test stubs"""
 
     def setUp(self):
         pass
 
     def tearDown(self):
         pass
 
     def make_instance(self, include_optional):
-        """Test InlineObject2
+        """Test InlineObject1
             include_option is a boolean, when False only required
             params are included, when True both required and
             optional params are included """
-        # model = mainnet.models.inline_object2.InlineObject2()  # noqa: E501
+        # model = mainnet.models.inline_object1.InlineObject1()  # noqa: E501
         if include_optional :
-            return InlineObject2(
+            return InlineObject1(
                 wallet_id = 'wif:testnet:cNfsPtqN2bMRS7vH5qd8tR8GMvgXyL5BjnGAKgZ8DYEiCrCCQcP6', 
                 token_id = '0'
             )
         else :
-            return InlineObject2(
+            return InlineObject1(
                 wallet_id = 'wif:testnet:cNfsPtqN2bMRS7vH5qd8tR8GMvgXyL5BjnGAKgZ8DYEiCrCCQcP6',
                 token_id = '0',
         )
 
-    def testInlineObject2(self):
-        """Test InlineObject2"""
+    def testInlineObject1(self):
+        """Test InlineObject1"""
         inst_req_only = self.make_instance(include_optional=False)
         inst_req_and_optional = self.make_instance(include_optional=True)
 
 
 if __name__ == '__main__':
     unittest.main()
```

### Comparing `mainnet-1.1.8/test/test_inline_object3.py` & `mainnet-1.1.9/test/test_inline_object3.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_inline_object4.py` & `mainnet-1.1.9/test/test_inline_object4.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_max_amount_to_send_request.py` & `mainnet-1.1.9/test/test_max_amount_to_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_mine_api.py` & `mainnet-1.1.9/test/test_mine_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_mine_request.py` & `mainnet-1.1.9/test/test_mine_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_network_enum.py` & `mainnet-1.1.9/test/test_network_enum.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_op_return_data.py` & `mainnet-1.1.9/test/test_op_return_data.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_scalable_vector_graphic.py` & `mainnet-1.1.9/test/test_scalable_vector_graphic.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_max_request.py` & `mainnet-1.1.9/test/test_send_max_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_max_response.py` & `mainnet-1.1.9/test/test_send_max_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_request.py` & `mainnet-1.1.9/test/test_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_request_item.py` & `mainnet-1.1.9/test/test_send_request_item.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_request_item_any_of.py` & `mainnet-1.1.9/test/test_send_request_item_any_of.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_request_options.py` & `mainnet-1.1.9/test/test_send_request_options.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_send_response.py` & `mainnet-1.1.9/test/test_send_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_serialized_wallet.py` & `mainnet-1.1.9/test/test_serialized_wallet.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_signed_message_response.py` & `mainnet-1.1.9/test/test_signed_message_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_signed_message_response_details.py` & `mainnet-1.1.9/test/test_signed_message_response_details.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_signed_message_response_raw.py` & `mainnet-1.1.9/test/test_signed_message_response_raw.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_balance_request.py` & `mainnet-1.1.9/test/test_slp_balance_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_balance_response.py` & `mainnet-1.1.9/test/test_slp_balance_response.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_deposit_address_response.py` & `mainnet-1.1.9/test/test_slp_deposit_address_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_genesis_request.py` & `mainnet-1.1.9/test/test_slp_genesis_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_genesis_response.py` & `mainnet-1.1.9/test/test_slp_genesis_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_mint_request.py` & `mainnet-1.1.9/test/test_slp_mint_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_mint_response.py` & `mainnet-1.1.9/test/test_slp_mint_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_outpoints_response.py` & `mainnet-1.1.9/test/test_slp_outpoints_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_send_max_request.py` & `mainnet-1.1.9/test/test_slp_send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_send_request.py` & `mainnet-1.1.9/test/test_slp_send_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_send_request_item.py` & `mainnet-1.1.9/test/test_slp_send_request_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_send_request_options.py` & `mainnet-1.1.9/test/test_slp_send_request_options.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_send_response.py` & `mainnet-1.1.9/test/test_slp_send_response.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_token_info_request.py` & `mainnet-1.1.9/test/test_slp_token_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_token_info_response.py` & `mainnet-1.1.9/test/test_slp_token_info_response.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_utxo.py` & `mainnet-1.1.9/test/test_slp_utxo.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_slp_utxo_response.py` & `mainnet-1.1.9/test/test_slp_utxo_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_deploy_request.py` & `mainnet-1.1.9/test/test_smart_bch_contract_deploy_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_deploy_response.py` & `mainnet-1.1.9/test/test_smart_bch_contract_deploy_response.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_estimate_gas_request.py` & `mainnet-1.1.9/test/test_smart_bch_contract_estimate_gas_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_estimate_gas_response.py` & `mainnet-1.1.9/test/test_smart_bch_contract_estimate_gas_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_fn_call_request.py` & `mainnet-1.1.9/test/test_smart_bch_contract_fn_call_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_fn_call_response.py` & `mainnet-1.1.9/test/test_smart_bch_contract_fn_call_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_info_request.py` & `mainnet-1.1.9/test/test_smart_bch_contract_info_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_info_response.py` & `mainnet-1.1.9/test/test_smart_bch_contract_info_response.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_request.py` & `mainnet-1.1.9/test/test_smart_bch_contract_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_contract_response.py` & `mainnet-1.1.9/test/test_smart_bch_contract_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_deposit_address_response.py` & `mainnet-1.1.9/test/test_smart_bch_deposit_address_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_max_amount_to_send_request.py` & `mainnet-1.1.9/test/test_smart_bch_max_amount_to_send_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_overrides.py` & `mainnet-1.1.9/test/test_smart_bch_overrides.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_max_request.py` & `mainnet-1.1.9/test/test_smart_bch_send_max_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_request.py` & `mainnet-1.1.9/test/test_smart_bch_send_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_request_item.py` & `mainnet-1.1.9/test/test_smart_bch_send_request_item.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_request_item_any_of.py` & `mainnet-1.1.9/test/test_smart_bch_send_request_item_any_of.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_request_options.py` & `mainnet-1.1.9/test/test_smart_bch_send_request_options.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_send_response_item.py` & `mainnet-1.1.9/test/test_smart_bch_send_response_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_all_balances_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_all_balances_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_balance_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_balance_request.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_balance_response.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_balance_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_genesis_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_genesis_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_genesis_response.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_genesis_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_mint_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_mint_request.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_mint_response.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_mint_response.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_send_max_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_send_max_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_send_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_send_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_send_request_item.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_send_request_item.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_token_info_request.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_token_info_request.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_sep20_token_info_response.py` & `mainnet-1.1.9/test/test_smart_bch_sep20_token_info_response.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smart_bch_transaction_receipt.py` & `mainnet-1.1.9/test/test_smart_bch_transaction_receipt.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smartbch_contract_api.py` & `mainnet-1.1.9/test/test_smartbch_contract_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smartbch_sep20_api.py` & `mainnet-1.1.9/test/test_smartbch_sep20_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_smartbch_wallet_api.py` & `mainnet-1.1.9/test/test_smartbch_wallet_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_submit_transaction_request.py` & `mainnet-1.1.9/test/test_submit_transaction_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_submit_transaction_response.py` & `mainnet-1.1.9/test/test_submit_transaction_response.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_token_burn_request.py` & `mainnet-1.1.9/test/test_token_burn_request.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_token_genesis_request.py` & `mainnet-1.1.9/test/test_token_genesis_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_token_mint_request.py` & `mainnet-1.1.9/test/test_token_mint_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_token_mint_request_requests.py` & `mainnet-1.1.9/test/test_token_mint_request_requests.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_token_send_request.py` & `mainnet-1.1.9/test/test_token_send_request.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_transaction_history_item.py` & `mainnet-1.1.9/test/test_transaction_history_item.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_unit_type.py` & `mainnet-1.1.9/test/test_unit_type.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_util_api.py` & `mainnet-1.1.9/test/test_util_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_util_decode_transaction_request.py` & `mainnet-1.1.9/test/test_util_decode_transaction_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_utxo.py` & `mainnet-1.1.9/test/test_utxo.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_utxo_token.py` & `mainnet-1.1.9/test/test_utxo_token.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_verify_signed_message_request.py` & `mainnet-1.1.9/test/test_verify_signed_message_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_verify_signed_message_response.py` & `mainnet-1.1.9/test/test_verify_signed_message_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_verify_signed_message_response_details.py` & `mainnet-1.1.9/test/test_verify_signed_message_response_details.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_api.py` & `mainnet-1.1.9/test/test_wallet_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_bcmr_api.py` & `mainnet-1.1.9/test/test_wallet_bcmr_api.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_info.py` & `mainnet-1.1.9/test/test_wallet_info.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_mnemonic.py` & `mainnet-1.1.9/test/test_wallet_mnemonic.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_named_exists_request.py` & `mainnet-1.1.9/test/test_wallet_named_exists_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_replace_named_request.py` & `mainnet-1.1.9/test/test_wallet_replace_named_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_request.py` & `mainnet-1.1.9/test/test_wallet_request.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_response.py` & `mainnet-1.1.9/test/test_wallet_response.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_signed_api.py` & `mainnet-1.1.9/test/test_wallet_signed_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_slp_api.py` & `mainnet-1.1.9/test/test_wallet_slp_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_type.py` & `mainnet-1.1.9/test/test_wallet_type.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wallet_util_api.py` & `mainnet-1.1.9/test/test_wallet_util_api.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_watch_address_request.py` & `mainnet-1.1.9/test/test_watch_address_request.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_watch_address_response.py` & `mainnet-1.1.9/test/test_watch_address_response.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_webhook_api.py` & `mainnet-1.1.9/test/test_webhook_api.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_wif.py` & `mainnet-1.1.9/test/test_wif.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_x_pub_key.py` & `mainnet-1.1.9/test/test_x_pub_key.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_x_pub_key_request.py` & `mainnet-1.1.9/test/test_x_pub_key_request.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_x_pub_key_response.py` & `mainnet-1.1.9/test/test_x_pub_key_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

### Comparing `mainnet-1.1.8/test/test_zero_balance_response.py` & `mainnet-1.1.9/test/test_zero_balance_response.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # coding: utf-8
 
 """
     Mainnet Cash
 
     A developer friendly bitcoin cash wallet api  This API is currently in *active* development, breaking changes may be made prior to official release of version 1.0.0.   # noqa: E501
 
-    The version of the OpenAPI document: 1.1.7
+    The version of the OpenAPI document: 1.1.8
     Contact: hello@mainnet.cash
     Generated by: https://openapi-generator.tech
 """
 
 
 from __future__ import absolute_import
```

