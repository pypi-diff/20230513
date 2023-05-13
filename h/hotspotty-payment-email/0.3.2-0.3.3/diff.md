# Comparing `tmp/hotspotty_payment_email-0.3.2.tar.gz` & `tmp/hotspotty_payment_email-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hotspotty_payment_email-0.3.2.tar", max compression
+gzip compressed data, was "hotspotty_payment_email-0.3.3.tar", max compression
```

## Comparing `hotspotty_payment_email-0.3.2.tar` & `hotspotty_payment_email-0.3.3.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     4055 2023-05-12 15:07:11.864812 hotspotty_payment_email-0.3.2/README.md
--rw-r--r--   0        0        0        0 2023-05-10 02:24:31.545585 hotspotty_payment_email-0.3.2/hotspotty_payment_email/__init__.py
--rw-r--r--   0        0        0       58 2023-05-13 14:50:06.721967 hotspotty_payment_email-0.3.2/hotspotty_payment_email/__main__.py
--rw-r--r--   0        0        0     4901 2023-05-13 14:47:26.866638 hotspotty_payment_email-0.3.2/hotspotty_payment_email/cli.py
--rw-r--r--   0        0        0      880 2023-05-13 14:55:47.163480 hotspotty_payment_email-0.3.2/pyproject.toml
--rw-r--r--   0        0        0     5414 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.2/setup.py
--rw-r--r--   0        0        0     5069 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.2/PKG-INFO
+-rw-r--r--   0        0        0     4062 2023-05-13 14:58:18.213351 hotspotty_payment_email-0.3.3/README.md
+-rw-r--r--   0        0        0        0 2023-05-10 02:24:31.545585 hotspotty_payment_email-0.3.3/hotspotty_payment_email/__init__.py
+-rw-r--r--   0        0        0       58 2023-05-13 14:50:06.721967 hotspotty_payment_email-0.3.3/hotspotty_payment_email/__main__.py
+-rw-r--r--   0        0        0     4925 2023-05-13 15:01:42.459449 hotspotty_payment_email-0.3.3/hotspotty_payment_email/cli.py
+-rw-r--r--   0        0        0      880 2023-05-13 15:02:08.862473 hotspotty_payment_email-0.3.3/pyproject.toml
+-rw-r--r--   0        0        0     5421 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.3/setup.py
+-rw-r--r--   0        0        0     5076 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.3/PKG-INFO
```

### Comparing `hotspotty_payment_email-0.3.2/README.md` & `hotspotty_payment_email-0.3.3/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -60,15 +60,15 @@
      --draft True \
      --subject "Hotspot report from 2023/04/01 to 2023/05/01" \
      --start 2023-04-01 \
      --end 2023-05-01 \
      --template "mail_template.html" \
      --credentials "credentials.json" \
      --delimiter "," \
-     --reports "commission-report-1.csv" "commission-report-2.csv"
+     --report "commission-report-1.csv" -report "commission-report-2.csv"
    ```
 
 ## Sample template e-mail
 Here below a sample template e-mail that you can use as a starting point to create your own template e-mail:
 
 ```html
 <!DOCTYPE html>
```

#### html2text {}

```diff
@@ -34,17 +34,17 @@
 (#setup-you-googl-account) section and you have a credentials.json file in the
 local folder. - You have 2 contact commissions files exported from hotspotty in
 the local folder called commission-report-1.csv and commission-report-2.csv and
 these files have ',' as delimiter. - You have a jinja emial template called
 mail_template.html in the local folder. ```bash hotspotty-payment-email \ --
 draft True \ --subject "Hotspot report from 2023/04/01 to 2023/05/01" \ --start
 2023-04-01 \ --end 2023-05-01 \ --template "mail_template.html" \ --credentials
-"credentials.json" \ --delimiter "," \ --reports "commission-report-1.csv"
-"commission-report-2.csv" ``` ## Sample template e-mail Here below a sample
-template e-mail that you can use as a starting point to create your own
+"credentials.json" \ --delimiter "," \ --report "commission-report-1.csv" -
+report "commission-report-2.csv" ``` ## Sample template e-mail Here below a
+sample template e-mail that you can use as a starting point to create your own
 template e-mail: ```html
 Hi {{name}},
 Below the tokens accrued by your hotspot in the following period: {
 {start_date}} - {{end_date}}. Payments will be made to your wallet: {
 {wallet_address}} and in total you will receive:
     * {% if amount_hnt > 0 %}
     * {{amount_hnt}} HNT.
```

### Comparing `hotspotty_payment_email-0.3.2/hotspotty_payment_email/cli.py` & `hotspotty_payment_email-0.3.3/hotspotty_payment_email/cli.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from datetime import date
 from email.message import EmailMessage
+from typing import List
 
 import click
 import base64
 from google_auth_oauthlib.flow import InstalledAppFlow
 from googleapiclient.discovery import build, Resource
 from jinja2 import Template
 from pandas import DataFrame, read_csv, concat
@@ -45,15 +46,15 @@
             message = service.users().messages().send(userId="me", body=create_message).execute()
     except HTTPError as error:
         logger.error(F'The following error occurred whe trying to send email to {recipient_email}: {error}')
         message = None
     return message
 
 
-def process_reports(reports: list[str], delimiter: str) -> DataFrame:
+def process_reports(reports: List[str], delimiter: str) -> DataFrame:
     data = DataFrame()
     for report in reports:
         data = concat([data, read_csv(report, delimiter=delimiter)])
 
     result = DataFrame(columns=['email', 'name', 'wallet', 'amount_hnt', 'amount_iot'])
 
     emails = set(data['email'].tolist())
@@ -84,15 +85,15 @@
 @click.option('--subject', type=str, help='Subject of the emails to send.')
 @click.option('--start', type=date.fromisoformat,
               help='Specify a start date for the report in ISO format (YYYY-MM-DD)')
 @click.option('--end', type=date.fromisoformat,
               help='Specify a end date for the report in ISO format (YYYY-MM-DD)')
 @click.option('--delimiter', type=str, default=',', help='Delimiter used in the reports files.')
 @click.option('--draft', type=bool, default=True, help='If true, the email will be created as a draft.')
-def cli(credentials: str, report: list[str], subject: str, template: str, start: date, end: date, delimiter: str,
+def cli(credentials: str, report: List[str], subject: str, template: str, start: date, end: date, delimiter: str,
         draft: bool):
 
     result = process_reports(report, delimiter)
 
     SCOPES = ['https://www.googleapis.com/auth/gmail.compose']
     flow = InstalledAppFlow.from_client_secrets_file(credentials, SCOPES)
     creds = flow.run_local_server(port=0)
```

### Comparing `hotspotty_payment_email-0.3.2/pyproject.toml` & `hotspotty_payment_email-0.3.3/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hotspotty-payment-email"
-version = "0.3.2"
+version = "0.3.3"
 description = "A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive."
 authors = ["Andrea Del Corto <andrea.delcorto@gmail.com>"]
 readme = "README.md"
 packages = [
     { include = "hotspotty_payment_email" }
 ]
```

### Comparing `hotspotty_payment_email-0.3.2/setup.py` & `hotspotty_payment_email-0.3.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -16,17 +16,17 @@
 
 entry_points = \
 {'console_scripts': ['hotspotty-payment-email = '
                      'hotspotty_payment_email.cli:cli']}
 
 setup_kwargs = {
     'name': 'hotspotty-payment-email',
-    'version': '0.3.2',
+    'version': '0.3.3',
     'description': "A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive.",
-    'long_description': '# Hotspotty Payment Email\n\nThe goal of this project is about developing a command line tool that take as input a list of commission reports in csv\nformat exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of\nHotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the\nrewards they\'ll receive.\n\n## Setup your Google account and get the file credentials.json\n\n1. Set up a [Google Cloud Platform](https://cloud.google.com/) project, click on the hamburger menu, and select view all\n   products. Under the management\n   section, select [APIs and services](https://console.cloud.google.com/apis/dashboard)\n2. Next, select [Library](https://console.cloud.google.com/apis/library) and type “Gmail API” in the search bar, and\n   click on the Gmail API card.\n3. Finally, select the enable\n   the [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com?project=geocaching-366015) button.\n4. Now, you’ll need to download the client secrets file for your project. Start by selecting create credentials. In this\n   section, select the Gmail API as your preferred API and user data as the type of data you will be accessing.\n5. To get the OAuth client ID, select your application type as a Desktop App, set the application name, and select\n   create. Next, download and store the credentials in your local file system.\n\nAfter downloading the secret file, you should have a file in this format:\n\n```json\n{\n  "installed": {\n    "client_id": "463225603869-un1ijjk75iguesbh4nhclm74edprhj5p.apps.googleusercontent.com",\n    "project_id": "geocaching-366015",\n    "auth_uri": "https://accounts.google.com/o/oauth2/auth",\n    "token_uri": "https://oauth2.googleapis.com/token",\n    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",\n    "client_secret": "TOCSXX-wXkVvnUSGrqC_OcH722jmnFPZHIE",\n    "redirect_uris": [\n      "http://localhost"\n    ]\n  }\n}\n```\n\n## How to use the script\n\n1. Export a one or more contact commissions as show below in the\n   [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty:\n   ![export_contact_commissions.png](docs/img/export_contact_commissions.png)\n\n2. See script help to get more details about how to use the script. \n   \n   ```bash\n      hotspotty-payment-email --help\n   ```\n3. Here below a concrete example which assumes that:\n   - You have followed stesps described in [Setup you googl account](#setup-you-googl-account) section and you have a \n     credentials.json file in the local folder.\n   - You have 2 contact commissions files exported from hotspotty in the local folder called commission-report-1.csv\n     and commission-report-2.csv and these files have \',\' as delimiter.\n   - You have a jinja emial template called mail_template.html in the local folder.\n\n   ```bash\n    hotspotty-payment-email \\\n     --draft True \\\n     --subject "Hotspot report from 2023/04/01 to 2023/05/01" \\\n     --start 2023-04-01 \\\n     --end 2023-05-01 \\\n     --template "mail_template.html" \\\n     --credentials "credentials.json" \\\n     --delimiter "," \\\n     --reports "commission-report-1.csv" "commission-report-2.csv"\n   ```\n\n## Sample template e-mail\nHere below a sample template e-mail that you can use as a starting point to create your own template e-mail:\n\n```html\n<!DOCTYPE html>\n<html>\n<head>\n    <meta charset="UTF-8">\n</head>\n<body>\n\t<p>\n      Hi {{name}},<br>\n      Below the tokens accrued by your hotspot in the following\n      period: {{start_date}} - {{end_date}}. Payments will be made to your wallet:\n      <a href="https://explorer.solana.com/address/{{wallet_address}}">{{wallet_address}}</a> and in total you will receive:\n      <ul>\n         {% if amount_hnt > 0 %}\n             <li>{{amount_hnt}} HNT.</li>\n         {% endif %}\n         {% if amount_iot > 0 %}\n             <li>{{amount_iot}} IOT.</li>\n         {% endif %}\n      </ul>\n\t</p>\n    <p>\n      Thanks,<br>\n      Bye bye\n    </p>\n</body>\n</html>\n```\n\n',
+    'long_description': '# Hotspotty Payment Email\n\nThe goal of this project is about developing a command line tool that take as input a list of commission reports in csv\nformat exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of\nHotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the\nrewards they\'ll receive.\n\n## Setup your Google account and get the file credentials.json\n\n1. Set up a [Google Cloud Platform](https://cloud.google.com/) project, click on the hamburger menu, and select view all\n   products. Under the management\n   section, select [APIs and services](https://console.cloud.google.com/apis/dashboard)\n2. Next, select [Library](https://console.cloud.google.com/apis/library) and type “Gmail API” in the search bar, and\n   click on the Gmail API card.\n3. Finally, select the enable\n   the [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com?project=geocaching-366015) button.\n4. Now, you’ll need to download the client secrets file for your project. Start by selecting create credentials. In this\n   section, select the Gmail API as your preferred API and user data as the type of data you will be accessing.\n5. To get the OAuth client ID, select your application type as a Desktop App, set the application name, and select\n   create. Next, download and store the credentials in your local file system.\n\nAfter downloading the secret file, you should have a file in this format:\n\n```json\n{\n  "installed": {\n    "client_id": "463225603869-un1ijjk75iguesbh4nhclm74edprhj5p.apps.googleusercontent.com",\n    "project_id": "geocaching-366015",\n    "auth_uri": "https://accounts.google.com/o/oauth2/auth",\n    "token_uri": "https://oauth2.googleapis.com/token",\n    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",\n    "client_secret": "TOCSXX-wXkVvnUSGrqC_OcH722jmnFPZHIE",\n    "redirect_uris": [\n      "http://localhost"\n    ]\n  }\n}\n```\n\n## How to use the script\n\n1. Export a one or more contact commissions as show below in the\n   [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty:\n   ![export_contact_commissions.png](docs/img/export_contact_commissions.png)\n\n2. See script help to get more details about how to use the script. \n   \n   ```bash\n      hotspotty-payment-email --help\n   ```\n3. Here below a concrete example which assumes that:\n   - You have followed stesps described in [Setup you googl account](#setup-you-googl-account) section and you have a \n     credentials.json file in the local folder.\n   - You have 2 contact commissions files exported from hotspotty in the local folder called commission-report-1.csv\n     and commission-report-2.csv and these files have \',\' as delimiter.\n   - You have a jinja emial template called mail_template.html in the local folder.\n\n   ```bash\n    hotspotty-payment-email \\\n     --draft True \\\n     --subject "Hotspot report from 2023/04/01 to 2023/05/01" \\\n     --start 2023-04-01 \\\n     --end 2023-05-01 \\\n     --template "mail_template.html" \\\n     --credentials "credentials.json" \\\n     --delimiter "," \\\n     --report "commission-report-1.csv" -report "commission-report-2.csv"\n   ```\n\n## Sample template e-mail\nHere below a sample template e-mail that you can use as a starting point to create your own template e-mail:\n\n```html\n<!DOCTYPE html>\n<html>\n<head>\n    <meta charset="UTF-8">\n</head>\n<body>\n\t<p>\n      Hi {{name}},<br>\n      Below the tokens accrued by your hotspot in the following\n      period: {{start_date}} - {{end_date}}. Payments will be made to your wallet:\n      <a href="https://explorer.solana.com/address/{{wallet_address}}">{{wallet_address}}</a> and in total you will receive:\n      <ul>\n         {% if amount_hnt > 0 %}\n             <li>{{amount_hnt}} HNT.</li>\n         {% endif %}\n         {% if amount_iot > 0 %}\n             <li>{{amount_iot}} IOT.</li>\n         {% endif %}\n      </ul>\n\t</p>\n    <p>\n      Thanks,<br>\n      Bye bye\n    </p>\n</body>\n</html>\n```\n\n',
     'author': 'Andrea Del Corto',
     'author_email': 'andrea.delcorto@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
     'packages': packages,
     'package_data': package_data,
```

### Comparing `hotspotty_payment_email-0.3.2/PKG-INFO` & `hotspotty_payment_email-0.3.3/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hotspotty-payment-email
-Version: 0.3.2
+Version: 0.3.3
 Summary: A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive.
 Author: Andrea Del Corto
 Author-email: andrea.delcorto@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -79,15 +79,15 @@
      --draft True \
      --subject "Hotspot report from 2023/04/01 to 2023/05/01" \
      --start 2023-04-01 \
      --end 2023-05-01 \
      --template "mail_template.html" \
      --credentials "credentials.json" \
      --delimiter "," \
-     --reports "commission-report-1.csv" "commission-report-2.csv"
+     --report "commission-report-1.csv" -report "commission-report-2.csv"
    ```
 
 ## Sample template e-mail
 Here below a sample template e-mail that you can use as a starting point to create your own template e-mail:
 
 ```html
 <!DOCTYPE html>
```

