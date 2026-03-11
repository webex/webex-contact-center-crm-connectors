# Salesforce Connector Assets

## Overview

This folder contains Webex Contact Center assets for the Salesforce connector portfolio. The current repository structure separates Salesforce CTI assets from Salesforce Service Cloud Voice assets so administrators can work with the correct deployment package for their environment.

## Connector folders

| Connector | Folder | Purpose |
| --- | --- | --- |
| CTI | [`cti/`](./cti/README.md) | Open CTI call center metadata for the Salesforce CTI connector |
| Service Cloud Voice | [`servicecloudvoice/`](./servicecloudvoice/README.md) | Contact center metadata, sample Salesforce routing assets, and a Webex flow template for Service Cloud Voice |

## Documentation

- Salesforce CTI public guide: [Integrate Webex Contact Center with Salesforce (Version 2-New)](https://help.webex.com/en-us/article/dyidod/Integrate-Webex-Contact-Center-with-Salesforce-(Version-2-New))
- Service Cloud Voice deployment notes: start with the README files in [`servicecloudvoice/`](./servicecloudvoice/README.md)

## Usage notes

- Use the CTI folder when your deployment uses the Open CTI desktop integration pattern.
- Use the Service Cloud Voice folder when your deployment uses Salesforce Service Cloud Voice and Omni-Channel routing.
- Review the folder-level README before importing metadata so that required Salesforce settings, permission sets, and Webex-side configuration are aligned with the selected connector.
