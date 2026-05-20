# ServiceNow CCIF Update Set

## Overview

This folder contains the ServiceNow update set for the ServiceNow CCIF connector track.

## Included asset

| File | Description |
| --- | --- |
| [`WebexCC_CCIF_GA_UpdateSet_1_0_0.xml`](./WebexCC_CCIF_GA_UpdateSet_1_0_0.xml) | May 2026 GA ServiceNow update set XML for the Cisco Webex Contact Center application scope `x_caci_crm_wxcc_vx`, version `1.0.0` |

## What this asset does

- Loads the ServiceNow-side application artifacts associated with the ServiceNow CCIF integration.
- Carries the remote update set named `Cisco Webex Contact Center`.
- Provides the packaged ServiceNow records for the GA CCIF implementation path, including the May 2026 AWA tab prioritization update.

## Import guidance

1. In ServiceNow, open **System Update Sets > Retrieved Update Sets**.
2. Choose **Import Update Set from XML**.
3. Upload [`WebexCC_CCIF_GA_UpdateSet_1_0_0.xml`](./WebexCC_CCIF_GA_UpdateSet_1_0_0.xml).
4. Preview the update set and review any collisions, skipped items, or cross-scope warnings.
5. Commit the update set only after validation is complete in the target instance.

## Usage notes

- Import this asset in a non-production instance first.
- Treat the update set as environment-sensitive and verify that installed records, privileges, and dependencies match the target tenant.
- Use this asset together with the Webex Contact Center flow in [`../sample-flow/`](../sample-flow/README.md) when preparing a full ServiceNow CCIF deployment.
