# ServiceNow CCIF Connector

## Overview

This folder contains repository assets for the next-generation Webex Contact Center integration with ServiceNow based on the ServiceNow Contact Center Integration Framework (CCIF). The current contents provide the ServiceNow-side update set, the Webex Contact Center sample flow, and the ServiceNow subflow update set used to stand up and validate the integration.

## Included assets

| Asset | Purpose |
| --- | --- |
| [`update-set/`](./update-set/README.md) | ServiceNow update set used to load the ServiceNow CCIF application artifacts |
| [`sample-flow/`](./sample-flow/README.md) | Webex Contact Center sample flow template used to orchestrate the ServiceNow CCIF voice workflow |
| [`servicenow-subflow/`](./servicenow-subflow/README.md) | ServiceNow subflow update set used to load the ServiceNow-side CCIF subflow into Flow Designer |

## Deployment notes

- Treat the update set, the sample flow, and the ServiceNow subflow as companion assets for the same connector track.
- Import the ServiceNow update set into a non-production ServiceNow instance first, then validate the installed records and cross-scope behavior before moving forward.
- Import the sample flow into Webex Contact Center Flow Designer as a starting point and replace tenant-specific values before publishing.
- Import the ServiceNow subflow update set into ServiceNow and verify that the published subflow is visible in Flow Designer before end-to-end testing.
- Review queue identifiers, connector bindings, authentication references, and any environment-specific variables before production use.

## Usage notes

- Use the section README files in this folder for import guidance:
  - [`update-set/README.md`](./update-set/README.md)
  - [`sample-flow/README.md`](./sample-flow/README.md)
  - [`servicenow-subflow/README.md`](./servicenow-subflow/README.md)
- These assets are intended to accelerate implementation and validation work, not to replace customer-specific configuration and testing.
