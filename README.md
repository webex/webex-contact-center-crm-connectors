# Webex Contact Center CRM Connectors

![Salesforce](https://img.shields.io/badge/Platform-Salesforce-00A1E0?logo=salesforce&logoColor=white)
![ServiceNow](https://img.shields.io/badge/Platform-ServiceNow-81B441?logo=servicenow&logoColor=white)
![Connectors](https://img.shields.io/badge/Connectors-CTI%20%7C%20Service%20Cloud%20Voice%20%7C%20ServiceNow%20CCIF-005073)
![Documentation](https://img.shields.io/badge/Docs-Public%20Guides%20%2B%20Repo%20READMEs-1D63ED)

This repository contains connector assets, metadata, and deployment examples for Webex Contact Center integrations with Salesforce and ServiceNow. Use the folder-level README files to identify the correct connector type, locate the packaged assets, and follow the applicable deployment guidance.

## Repository layout

| Platform | Folder | Connector types covered |
| --- | --- | --- |
| Salesforce | [`salesforce/`](./salesforce/README.md) | CTI, Service Cloud Voice |
| ServiceNow | [`servicenow/`](./servicenow/README.md) | CTI, ServiceNow CCIF (next-gen) |

## Connector matrix

| Platform | Connector | Repository guide | Product documentation |
| --- | --- | --- | --- |
| Salesforce | CTI | [`salesforce/cti`](./salesforce/cti/README.md) | [Webex Help: Integrate Webex Contact Center with Salesforce (Version 2-New)](https://help.webex.com/en-us/article/dyidod/Integrate-Webex-Contact-Center-with-Salesforce-(Version-2-New)) |
| Salesforce | Service Cloud Voice | [`salesforce/servicecloudvoice`](./salesforce/servicecloudvoice/README.md) | Repository guidance in this repo |
| ServiceNow | CTI | [`servicenow/cti`](./servicenow/cti/README.md) | [Webex Help: Integrate Webex Contact Center with ServiceNow (Version 2-New)](https://help.webex.com/en-us/article/ny83tx0/Integrate-Webex-Contact-Center-with-ServiceNow-(Version-2-New)#reference-template_0b9dece3-d6e9-47c2-ae59-3b0c7ac71882) |
| ServiceNow | ServiceNow CCIF | [`servicenow/servicenow-ccif`](./servicenow/servicenow-ccif/README.md) | Repository guidance in this folder |

## What is included

- Salesforce CTI call center metadata used to configure the Open CTI connector.
- Salesforce Service Cloud Voice contact center metadata, sample Salesforce routing flow assets, and a Webex Flow Designer template.
- ServiceNow CTI update set assets for the current connector.
- A reserved folder for the next-generation ServiceNow CCIF connector documentation.

## How to use this repository

1. Start from the platform landing page under `salesforce/` or `servicenow/`.
2. Open the connector-specific README for deployment notes and asset descriptions.
3. Use the public Webex Help documentation for platform setup and product configuration.
4. Use the files in this repository as deployment assets, templates, or examples for the relevant connector.

## Notes

- This repository is focused on connector assets and deployment references, not full product documentation.
- Folder contents may differ by connector type; always use the README in the target folder before importing or deploying any asset.
