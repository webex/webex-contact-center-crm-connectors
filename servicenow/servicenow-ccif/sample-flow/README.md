# ServiceNow CCIF Sample Flow

## Overview

This folder contains the Webex Contact Center sample flow for the ServiceNow CCIF connector track.

## Included asset

| File | Description |
| --- | --- |
| [`ServiceNow_CCIF_Template.json`](./ServiceNow_CCIF_Template.json) | Webex Contact Center Flow Designer template named `ServiceNow_CCIF_Template` |

## What the template illustrates

- Passing ServiceNow interaction context from Webex Contact Center.
- Using shared variables such as `sharedRecordId`, `sn_queue_sysid`, and `time_zone`.
- Providing a starting point for the voice orchestration flow that works with the ServiceNow CCIF deployment.

## Import guidance

1. In Webex Contact Center, open **Flow Designer**.
2. Choose the option to import a flow JSON template.
3. Upload [`ServiceNow_CCIF_Template.json`](./ServiceNow_CCIF_Template.json).
4. Save the imported flow as a draft and review all connector bindings, queue identifiers, and environment-specific variables.
5. Test the flow in a non-production tenant before publishing.

## Usage notes

- This JSON is a sample flow template, not a production-ready drop-in configuration.
- Replace any tenant-specific values, connector references, queue mappings, and naming conventions before using it in a live deployment.
- Use this template together with the ServiceNow update set in [`../update-set/`](../update-set/README.md) when preparing the full ServiceNow CCIF integration.
