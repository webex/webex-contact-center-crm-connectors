# ServiceNow CCIF Subflow

## Overview

This folder contains the ServiceNow-native subflow update set for the ServiceNow CCIF connector track.

## Included asset

| File | Description |
| --- | --- |
| [`EA-Subflow-UpdateSet.xml`](./EA-Subflow-UpdateSet.xml) | ServiceNow update set XML that imports the published subflow `Cisco_CCIF_Subflow_Sample` |

## What this asset contains

- A ServiceNow subflow record named `Cisco_CCIF_Subflow_Sample`
- Internal name `cisco_ccif_subflow_sample`
- Published subflow metadata for the ServiceNow side of the CCIF workflow
- Input fields including `cisco_phone_number`, `servicenow_interaction_sysid`, `cisco_collected_digits`, and `action_type`

## Import guidance

1. In ServiceNow, open **Retrieved Update Sets**.
2. Choose **Import Update Set from XML**.
3. Upload [`EA-Subflow-UpdateSet.xml`](./EA-Subflow-UpdateSet.xml).
4. Preview the update set and review any warnings or conflicts.
5. Commit the update set after validation is complete.

## Verify the subflow in ServiceNow

1. Open **Flow Designer** in ServiceNow.
2. Go to the **Subflows** page or open the subflow list from Flow Designer.
3. Search for `Cisco_CCIF_Subflow_Sample`.
4. Confirm the record appears in the list and is shown as a subflow.
5. Confirm the record status is `Published`.
6. Open the subflow and verify that the expected inputs and outputs are visible.

## If you do not see it

- Confirm the update set was successfully committed.
- Refresh the browser or reopen Flow Designer.
- Search again using both `Cisco_CCIF_Subflow_Sample` and `cisco_ccif_subflow_sample`.
- Recheck preview or commit errors if the subflow still does not appear.

## Usage notes

- Treat this asset as part of the same ServiceNow CCIF implementation set as the update set in [`../update-set/`](../update-set/README.md) and the Webex sample flow in [`../sample-flow/`](../sample-flow/README.md).
- Import and validate this subflow in a non-production instance before production rollout.
