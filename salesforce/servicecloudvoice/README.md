# Salesforce Service Cloud Voice Connector

## Overview

This folder contains repository assets for the Webex Contact Center integration with Salesforce Service Cloud Voice. The content here supports deployments that combine Salesforce Service Cloud Voice, Webex Contact Center voice handling, and Salesforce Omni-Channel routing.

## Documentation

- Connector asset guide: this README and the two subfolder README files in this directory
- Salesforce sample routing assets: [`salesforce-examples/README.md`](./salesforce-examples/README.md)
- Webex flow template guidance: [`sample-flows/README.md`](./sample-flows/README.md)

## Included assets

| Asset | Purpose |
| --- | --- |
| [`WxCCContactCenterSCV.xml`](./WxCCContactCenterSCV.xml) | Contact center metadata definition for the Salesforce Service Cloud Voice connector |
| [`sample-flows/`](./sample-flows/README.md) | Webex Flow Designer template for Service Cloud Voice call handling and routing orchestration |
| [`salesforce-examples/`](./salesforce-examples/README.md) | Salesforce metadata package example containing a sample Omni Flow deployment artifact |

## Deployment notes

- Plan this connector for Salesforce environments that use Service Cloud Voice Partner Telephony and Omni-Channel routing.
- Prepare the required Salesforce configuration before deployment, including the Lightning Service Console app, Omni-Channel, appropriate permission sets, and any environment-specific connected app or remote site configuration used by your organization.
- Prepare the required Webex Contact Center configuration before deployment, including the tenant-level connector settings, certificates or keys used by the integration, and the flow variables needed to pass call context into Salesforce.
- Treat the contact center XML, Webex flow template, and Salesforce sample flow package as related assets: the XML defines the connector, the Webex flow template handles Webex-side voice orchestration, and the Salesforce sample assets illustrate the Omni Flow side of the routing experience.

## Configuration focus areas

Review and complete the connector-specific settings in [`WxCCContactCenterSCV.xml`](./WxCCContactCenterSCV.xml) before import or deployment, including:

- Telephony integration certificate and Webex certificate references
- Agent presence state mapping values
- Default not-ready reason and flag settings
- WebRTC domain and tenant values
- Voice call and vendor call key variable mappings
- Recording and transcription-related options, if enabled in your deployment

## Current status

This repository folder documents the deployment assets that accompany the Salesforce Service Cloud Voice connector. Environment-specific values, installed package components, and org-specific configuration remain outside version control.
