# Tor-Network-Website-Accessibility-Checker
The Tor Network Website Accessibility Checker is a Python-based script designed to run on Google Colab or Jupyter Notebook. It tests the accessibility of specified websites using different Tor exit nodes from various countries. This script helps to test if certain websites are accessible from different geographical locations from residential ips.

# Google Colab Link
https://colab.research.google.com/drive/1kueqAO7kf1zz6sr8dTUUsC8zuHocV9KF?usp=sharing

# Basic Usage Guide for Tor Exit Node Testing Script
Introduction
This script checks the accessibility of two websites, google.com and hanseyachts.com, from various countries using Tor exit nodes. If google.com is not accessible, it retries with a new endpoint from the same country. It also handles timeout errors by retrying with a new endpoint.

Requirements
Google Colab or Local Environment: The script can be run on Google Colab or a local machine.
Ngrok API Key: Required to expose the Tor control port via Ngrok for remote access.
Installation and Setup
Install Necessary Packages:

Tor
Stem (Python library for interacting with Tor)
Requests (for making HTTP requests)
Pyngrok (for creating secure tunnels to localhost)
Ngrok API Key:

Sign up for an Ngrok account at ngrok.com.
Obtain your API key from the Ngrok dashboard.
Use the API key to authenticate Ngrok in the script.
Script Settings
Ngrok API Key: Replace the placeholder with your actual Ngrok API key.

python
Copy code
ngrok_authtoken = "YOUR_NGROK_API_KEY"
Tor Hashed Password: Set your desired password for Tor authentication.

python
Copy code
password = 'my_password'
List of Country Codes: Modify the list to include the country codes you want to test.

python
Copy code
country_codes = ['US', 'CA', 'DE', 'FR', 'NL', 'GB', 'AU', 'JP', 'KR', 'RU', 'IN', 'BR', 'ES', 'IT', 'CH', 'SE', 'FI', 'NO', 'DK', 'BE', 'AT', 'PL', 'CZ', 'RO', 'UA', 'HU', 'GR', 'BG', 'TR', 'IL', 'ZA', 'SG', 'HK', 'MY', 'ID', 'PH', 'VN', 'TH']
Max Retries Per Country: Set the maximum number of retries per country if google.com is not accessible or a timeout error occurs.

python
Copy code
max_retries_per_country = 3

# License
Creative Commons Attribution-NonCommercial 4.0 International Public License

By exercising the Licensed Rights (defined below), You accept and agree to be bound by the terms and conditions of this Creative Commons Attribution-NonCommercial 4.0 International Public License ("Public License"). To the extent this Public License may be interpreted as a contract, You are granted the Licensed Rights in consideration of Your acceptance of these terms and conditions, and the Licensor grants You such rights in consideration of benefits the Licensor receives from making the Licensed Material available under these terms and conditions.

...

You are free to:
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material

The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:
- Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- NonCommercial — You may not use the material for commercial purposes.

...

Full License Text: https://creativecommons.org/licenses/by-nc/4.0/legalcode
