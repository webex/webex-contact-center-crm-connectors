# Salesforce CTI Connector

## Overview

This folder contains the Salesforce call center metadata used with the Webex Contact Center CTI connector for Salesforce. The asset in this folder is intended for Salesforce administrators who need to import and maintain the call center definition that points Salesforce to the Webex Contact Center CTI adapter.

## Documentation

- Public setup guide: [Integrate Webex Contact Center with Salesforce (Version 2-New)](https://help.webex.com/en-us/article/dyidod/Integrate-Webex-Contact-Center-with-Salesforce-(Version-2-New))

## Included assets

| File | Description |
| --- | --- |
| [`OpenCTI.callCenter-meta.xml`](./OpenCTI.callCenter-meta.xml) | Salesforce call center definition with Webex Contact Center CTI settings, adapter URL, layout dimensions, and optional behavior flags |

## Usage notes

- Import the call center definition into Salesforce as part of the CTI connector setup.
- Review the values in the metadata before deployment, especially region, WebRTC domain, adapter URL, activity logging settings, screen pop options, and Omni-Channel synchronization settings.
- Align the imported settings with your Webex Contact Center tenant and Salesforce configuration before assigning users to the call center.
- Use the public Webex Help guide for the end-to-end platform configuration steps; this folder provides the connector asset referenced during that setup.

## Current status

This folder currently contains the Salesforce CTI call center metadata only. Managed package components and org-specific configuration remain outside this repository.
