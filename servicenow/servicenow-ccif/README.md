# ServiceNow CCIF Connector

## Overview

This folder contains repository assets for the next-generation Webex Contact Center integration with ServiceNow based on the ServiceNow Contact Center Integration Framework (CCIF). The current contents provide the ServiceNow-side update set, two Webex Contact Center sample flow variants, and two ServiceNow subflow variants used to stand up and validate different ServiceNow CCIF deployment patterns.

## Included assets

| Asset | Purpose |
| --- | --- |
| [`update-set/`](./update-set/README.md) | ServiceNow update set used to load the ServiceNow CCIF application artifacts |
| [`sample-flow/`](./sample-flow/README.md) | Webex Contact Center sample flow templates for deployments with and without a ServiceNow subflow |
| [`servicenow-subflow/`](./servicenow-subflow/README.md) | ServiceNow subflow update set variants used to load either the advanced or simple ServiceNow-side CCIF subflow into Flow Designer |

## Deployment notes

- Treat the update set, the sample flow templates, and the ServiceNow subflow variants as companion assets for the same connector track.
- Import the ServiceNow update set into a non-production ServiceNow instance first, then validate the installed records and cross-scope behavior before moving forward.
- Import the sample flow variant that matches your deployment model and replace tenant-specific values before publishing.
- Import a ServiceNow subflow only when your Webex flow design is intended to call a ServiceNow subflow during the interaction lifecycle.
- Review queue identifiers, connector bindings, authentication references, and any environment-specific variables before production use.

## Usage notes

- Use the section README files in this folder for import guidance:
  - [`update-set/README.md`](./update-set/README.md)
  - [`sample-flow/README.md`](./sample-flow/README.md)
  - [`servicenow-subflow/README.md`](./servicenow-subflow/README.md)
- The `sample-flow/` folder contains:
  - `ServiceNow_CCIF_Template.json` for the direct ServiceNow CCIF pattern without a ServiceNow subflow
  - `ServiceNow_CCIF_with_SNOW_Subflow_Template.json` for the variant that calls a ServiceNow subflow after creating the interaction
- The `servicenow-subflow/` folder contains:
  - `EA_Advanced_ServiceNow_Subflow.xml` for the richer ServiceNow subflow pattern
  - `EA_Simple_ServiceNow_Subflow.xml` for the lightweight ServiceNow subflow pattern used by the sample flow template
- These assets are intended to accelerate implementation and validation work, not to replace customer-specific configuration and testing.
