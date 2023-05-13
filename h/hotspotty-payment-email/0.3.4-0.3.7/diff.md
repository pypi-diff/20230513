# Comparing `tmp/hotspotty_payment_email-0.3.4.tar.gz` & `tmp/hotspotty_payment_email-0.3.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hotspotty_payment_email-0.3.4.tar", max compression
+gzip compressed data, was "hotspotty_payment_email-0.3.7.tar", max compression
```

## Comparing `hotspotty_payment_email-0.3.4.tar` & `hotspotty_payment_email-0.3.7.tar`

### file list

```diff
@@ -1,7 +1,6 @@
--rw-r--r--   0        0        0     4063 2023-05-13 15:04:19.641156 hotspotty_payment_email-0.3.4/README.md
--rw-r--r--   0        0        0        0 2023-05-10 02:24:31.545585 hotspotty_payment_email-0.3.4/hotspotty_payment_email/__init__.py
--rw-r--r--   0        0        0       58 2023-05-13 14:50:06.721967 hotspotty_payment_email-0.3.4/hotspotty_payment_email/__main__.py
--rw-r--r--   0        0        0     5218 2023-05-13 15:13:25.368214 hotspotty_payment_email-0.3.4/hotspotty_payment_email/cli.py
--rw-r--r--   0        0        0      880 2023-05-13 15:14:03.627681 hotspotty_payment_email-0.3.4/pyproject.toml
--rw-r--r--   0        0        0     5422 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.4/setup.py
--rw-r--r--   0        0        0     5077 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.4/PKG-INFO
+-rw-r--r--   0        0        0     4063 2023-05-13 16:10:21.289678 hotspotty_payment_email-0.3.7/README.md
+-rw-r--r--   0        0        0        0 2023-05-13 16:10:21.293679 hotspotty_payment_email-0.3.7/hotspotty_payment_email/__init__.py
+-rw-r--r--   0        0        0       58 2023-05-13 16:10:21.293679 hotspotty_payment_email-0.3.7/hotspotty_payment_email/__main__.py
+-rw-r--r--   0        0        0     5218 2023-05-13 16:10:21.293679 hotspotty_payment_email-0.3.7/hotspotty_payment_email/cli.py
+-rw-r--r--   0        0        0      880 2023-05-13 16:10:21.293679 hotspotty_payment_email-0.3.7/pyproject.toml
+-rw-r--r--   0        0        0     5077 1970-01-01 00:00:00.000000 hotspotty_payment_email-0.3.7/PKG-INFO
```

### Comparing `hotspotty_payment_email-0.3.4/README.md` & `hotspotty_payment_email-0.3.7/README.md`

 * *Files identical despite different names*

### Comparing `hotspotty_payment_email-0.3.4/hotspotty_payment_email/cli.py` & `hotspotty_payment_email-0.3.7/hotspotty_payment_email/cli.py`

 * *Files identical despite different names*

### Comparing `hotspotty_payment_email-0.3.4/pyproject.toml` & `hotspotty_payment_email-0.3.7/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hotspotty-payment-email"
-version = "0.3.4"
+version = "0.3.7"
 description = "A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive."
 authors = ["Andrea Del Corto <andrea.delcorto@gmail.com>"]
 readme = "README.md"
 packages = [
     { include = "hotspotty_payment_email" }
 ]
```

### Comparing `hotspotty_payment_email-0.3.4/setup.py` & `hotspotty_payment_email-0.3.7/PKG-INFO`

 * *Files 19% similar despite different names*

```diff
@@ -1,39 +1,121 @@
-# -*- coding: utf-8 -*-
-from setuptools import setup
-
-packages = \
-['hotspotty_payment_email']
+Metadata-Version: 2.1
+Name: hotspotty-payment-email
+Version: 0.3.7
+Summary: A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive.
+Author: Andrea Del Corto
+Author-email: andrea.delcorto@gmail.com
+Requires-Python: >=3.8,<4.0
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: click (>=8.1.3,<9.0.0)
+Requires-Dist: google-api-python-client (>=2.86.0,<3.0.0)
+Requires-Dist: google-auth-oauthlib (>=1.0.0,<2.0.0)
+Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
+Requires-Dist: pandas (>=2.0.1,<3.0.0)
+Description-Content-Type: text/markdown
+
+# Hotspotty Payment Email
+
+The goal of this project is about developing a command line tool that take as input a list of commission reports in csv
+format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of
+Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the
+rewards they'll receive.
+
+## Setup your Google account and get the file credentials.json
+
+1. Set up a [Google Cloud Platform](https://cloud.google.com/) project, click on the hamburger menu, and select view all
+   products. Under the management
+   section, select [APIs and services](https://console.cloud.google.com/apis/dashboard)
+2. Next, select [Library](https://console.cloud.google.com/apis/library) and type “Gmail API” in the search bar, and
+   click on the Gmail API card.
+3. Finally, select the enable
+   the [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com?project=geocaching-366015) button.
+4. Now, you’ll need to download the client secrets file for your project. Start by selecting create credentials. In this
+   section, select the Gmail API as your preferred API and user data as the type of data you will be accessing.
+5. To get the OAuth client ID, select your application type as a Desktop App, set the application name, and select
+   create. Next, download and store the credentials in your local file system.
+
+After downloading the secret file, you should have a file in this format:
+
+```json
+{
+  "installed": {
+    "client_id": "463225603869-un1ijjk75iguesbh4nhclm74edprhj5p.apps.googleusercontent.com",
+    "project_id": "geocaching-366015",
+    "auth_uri": "https://accounts.google.com/o/oauth2/auth",
+    "token_uri": "https://oauth2.googleapis.com/token",
+    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
+    "client_secret": "TOCSXX-wXkVvnUSGrqC_OcH722jmnFPZHIE",
+    "redirect_uris": [
+      "http://localhost"
+    ]
+  }
+}
+```
 
-package_data = \
-{'': ['*']}
+## How to use the script
 
-install_requires = \
-['click>=8.1.3,<9.0.0',
- 'google-api-python-client>=2.86.0,<3.0.0',
- 'google-auth-oauthlib>=1.0.0,<2.0.0',
- 'jinja2>=3.1.2,<4.0.0',
- 'pandas>=2.0.1,<3.0.0']
-
-entry_points = \
-{'console_scripts': ['hotspotty-payment-email = '
-                     'hotspotty_payment_email.cli:cli']}
-
-setup_kwargs = {
-    'name': 'hotspotty-payment-email',
-    'version': '0.3.4',
-    'description': "A command line tool that takes as input a list of commission reports in csv format exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the rewards they'll receive.",
-    'long_description': '# Hotspotty Payment Email\n\nThe goal of this project is about developing a command line tool that take as input a list of commission reports in csv\nformat exported from the [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of\nHotspotty platform and send a gmail e-mail to each user inside the input reports to inform them about the\nrewards they\'ll receive.\n\n## Setup your Google account and get the file credentials.json\n\n1. Set up a [Google Cloud Platform](https://cloud.google.com/) project, click on the hamburger menu, and select view all\n   products. Under the management\n   section, select [APIs and services](https://console.cloud.google.com/apis/dashboard)\n2. Next, select [Library](https://console.cloud.google.com/apis/library) and type “Gmail API” in the search bar, and\n   click on the Gmail API card.\n3. Finally, select the enable\n   the [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com?project=geocaching-366015) button.\n4. Now, you’ll need to download the client secrets file for your project. Start by selecting create credentials. In this\n   section, select the Gmail API as your preferred API and user data as the type of data you will be accessing.\n5. To get the OAuth client ID, select your application type as a Desktop App, set the application name, and select\n   create. Next, download and store the credentials in your local file system.\n\nAfter downloading the secret file, you should have a file in this format:\n\n```json\n{\n  "installed": {\n    "client_id": "463225603869-un1ijjk75iguesbh4nhclm74edprhj5p.apps.googleusercontent.com",\n    "project_id": "geocaching-366015",\n    "auth_uri": "https://accounts.google.com/o/oauth2/auth",\n    "token_uri": "https://oauth2.googleapis.com/token",\n    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",\n    "client_secret": "TOCSXX-wXkVvnUSGrqC_OcH722jmnFPZHIE",\n    "redirect_uris": [\n      "http://localhost"\n    ]\n  }\n}\n```\n\n## How to use the script\n\n1. Export a one or more contact commissions as show below in the\n   [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty:\n   ![export_contact_commissions.png](docs/img/export_contact_commissions.png)\n\n2. See script help to get more details about how to use the script. \n   \n   ```bash\n      hotspotty-payment-email --help\n   ```\n3. Here below a concrete example which assumes that:\n   - You have followed stesps described in [Setup you googl account](#setup-you-googl-account) section and you have a \n     credentials.json file in the local folder.\n   - You have 2 contact commissions files exported from hotspotty in the local folder called commission-report-1.csv\n     and commission-report-2.csv and these files have \',\' as delimiter.\n   - You have a jinja emial template called mail_template.html in the local folder.\n\n   ```bash\n    hotspotty-payment-email \\\n     --draft True \\\n     --subject "Hotspot report from 2023/04/01 to 2023/05/01" \\\n     --start 2023-04-01 \\\n     --end 2023-05-01 \\\n     --template "mail_template.html" \\\n     --credentials "credentials.json" \\\n     --delimiter "," \\\n     --report "commission-report-1.csv" --report "commission-report-2.csv"\n   ```\n\n## Sample template e-mail\nHere below a sample template e-mail that you can use as a starting point to create your own template e-mail:\n\n```html\n<!DOCTYPE html>\n<html>\n<head>\n    <meta charset="UTF-8">\n</head>\n<body>\n\t<p>\n      Hi {{name}},<br>\n      Below the tokens accrued by your hotspot in the following\n      period: {{start_date}} - {{end_date}}. Payments will be made to your wallet:\n      <a href="https://explorer.solana.com/address/{{wallet_address}}">{{wallet_address}}</a> and in total you will receive:\n      <ul>\n         {% if amount_hnt > 0 %}\n             <li>{{amount_hnt}} HNT.</li>\n         {% endif %}\n         {% if amount_iot > 0 %}\n             <li>{{amount_iot}} IOT.</li>\n         {% endif %}\n      </ul>\n\t</p>\n    <p>\n      Thanks,<br>\n      Bye bye\n    </p>\n</body>\n</html>\n```\n\n',
-    'author': 'Andrea Del Corto',
-    'author_email': 'andrea.delcorto@gmail.com',
-    'maintainer': 'None',
-    'maintainer_email': 'None',
-    'url': 'None',
-    'packages': packages,
-    'package_data': package_data,
-    'install_requires': install_requires,
-    'entry_points': entry_points,
-    'python_requires': '>=3.8,<4.0',
-}
+1. Export a one or more contact commissions as show below in the
+   [Commission report](https://app.hotspotty.net/workspace/helium/commission-reports) section of Hotspotty:
+   ![export_contact_commissions.png](docs/img/export_contact_commissions.png)
+
+2. See script help to get more details about how to use the script. 
+   
+   ```bash
+      hotspotty-payment-email --help
+   ```
+3. Here below a concrete example which assumes that:
+   - You have followed stesps described in [Setup you googl account](#setup-you-googl-account) section and you have a 
+     credentials.json file in the local folder.
+   - You have 2 contact commissions files exported from hotspotty in the local folder called commission-report-1.csv
+     and commission-report-2.csv and these files have ',' as delimiter.
+   - You have a jinja emial template called mail_template.html in the local folder.
+
+   ```bash
+    hotspotty-payment-email \
+     --draft True \
+     --subject "Hotspot report from 2023/04/01 to 2023/05/01" \
+     --start 2023-04-01 \
+     --end 2023-05-01 \
+     --template "mail_template.html" \
+     --credentials "credentials.json" \
+     --delimiter "," \
+     --report "commission-report-1.csv" --report "commission-report-2.csv"
+   ```
+
+## Sample template e-mail
+Here below a sample template e-mail that you can use as a starting point to create your own template e-mail:
+
+```html
+<!DOCTYPE html>
+<html>
+<head>
+    <meta charset="UTF-8">
+</head>
+<body>
+	<p>
+      Hi {{name}},<br>
+      Below the tokens accrued by your hotspot in the following
+      period: {{start_date}} - {{end_date}}. Payments will be made to your wallet:
+      <a href="https://explorer.solana.com/address/{{wallet_address}}">{{wallet_address}}</a> and in total you will receive:
+      <ul>
+         {% if amount_hnt > 0 %}
+             <li>{{amount_hnt}} HNT.</li>
+         {% endif %}
+         {% if amount_iot > 0 %}
+             <li>{{amount_iot}} IOT.</li>
+         {% endif %}
+      </ul>
+	</p>
+    <p>
+      Thanks,<br>
+      Bye bye
+    </p>
+</body>
+</html>
+```
 
 
-setup(**setup_kwargs)
```

