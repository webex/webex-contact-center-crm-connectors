# ServiceNow CCIF Sample Flow

## Overview

This folder contains Webex Contact Center sample flow variants for the ServiceNow CCIF connector track. The templates illustrate two deployment patterns: one that creates the ServiceNow interaction directly from the Webex flow, and one that also invokes a ServiceNow subflow after the interaction is created.

## Included assets

| File | Description |
| --- | --- |
| [`ServiceNow_CCIF_Template.json`](./ServiceNow_CCIF_Template.json) | Webex Contact Center Flow Designer template named `ServiceNow_CCIF_Template` for deployments that do not call a ServiceNow subflow |
| [`ServiceNow_CCIF_with_SNOW_Subflow_Template.json`](./ServiceNow_CCIF_with_SNOW_Subflow_Template.json) | Webex Contact Center Flow Designer template named `ServiceNow_CCIF_with_SNOW_Subflow_Template` for deployments that call a ServiceNow subflow |

## Which file to use

- Use [`ServiceNow_CCIF_Template.json`](./ServiceNow_CCIF_Template.json) when you want the simpler flow pattern that creates the ServiceNow interaction directly and then continues queue handling in Webex Contact Center.
- Use [`ServiceNow_CCIF_with_SNOW_Subflow_Template.json`](./ServiceNow_CCIF_with_SNOW_Subflow_Template.json) when you want the Webex flow to create the interaction and then invoke a ServiceNow Flow Designer subflow as part of the call handling sequence.

## What the templates illustrate

- Passing ServiceNow interaction context from Webex Contact Center.
- Using shared variables such as `sharedRecordId`, `sn_queue_sysid`, and `time_zone`.
- Providing one flow template without a ServiceNow subflow dependency and one template with a ServiceNow subflow dependency.
- Showing where tenant-specific connector bindings, queue identifiers, and ServiceNow-specific values need to be reviewed before publication.

## Import guidance

1. In Webex Contact Center, open **Flow Designer**.
2. Choose the option to import a flow JSON template.
3. Upload the JSON file that matches your deployment pattern.
4. Save the imported flow as a draft and review all connector bindings, queue identifiers, and environment-specific variables.
5. Test the flow in a non-production tenant before publishing.

## Usage notes

- These JSON files are sample flow templates, not production-ready drop-in configurations.
- Replace any tenant-specific values, connector references, queue mappings, queue sys_ids, and naming conventions before using them in a live deployment.
- `ServiceNow_CCIF_with_SNOW_Subflow_Template.json` is configured to call the ServiceNow subflow `EA_Simple_ServiceNow_Subflow`, so import that subflow from [`../servicenow-subflow/`](../servicenow-subflow/README.md) before end-to-end testing.
- Use either template together with the ServiceNow update set in [`../update-set/`](../update-set/README.md) when preparing the full ServiceNow CCIF integration.
