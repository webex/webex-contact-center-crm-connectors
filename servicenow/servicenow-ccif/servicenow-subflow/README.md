# ServiceNow CCIF Subflow

## Overview

This folder contains the ServiceNow-native subflow update set variants for the ServiceNow CCIF connector track. Use these XML files when your ServiceNow deployment needs a published Flow Designer subflow that can be invoked from the Webex Contact Center integration.

## Included assets

| File | Description |
| --- | --- |
| [`EA_Advanced_ServiceNow_Subflow.xml`](./EA_Advanced_ServiceNow_Subflow.xml) | Advanced ServiceNow subflow template that publishes `EA_Advanced_ServiceNow_Subflow` |
| [`EA_Simple_ServiceNow_Subflow.xml`](./EA_Simple_ServiceNow_Subflow.xml) | Simplified ServiceNow subflow template that publishes `EA_Simple_ServiceNow_Subflow` |

## Which file to use

- Use [`EA_Advanced_ServiceNow_Subflow.xml`](./EA_Advanced_ServiceNow_Subflow.xml) when you want the broader ServiceNow-side subflow pattern with the richer input model already present in the original CCIF sample.
- Use [`EA_Simple_ServiceNow_Subflow.xml`](./EA_Simple_ServiceNow_Subflow.xml) when you want the lightweight pattern that looks up the interaction, identifies the caller by phone, and is the default companion for the with-subflow Webex flow template in [`../sample-flow/`](../sample-flow/README.md).
- Treat both files as reference templates. Review names, integration bindings, and any customer-specific logic before promoting them beyond a test environment.

## What the variants contain

- `EA_Advanced_ServiceNow_Subflow.xml`
  - Published subflow name `EA_Advanced_ServiceNow_Subflow`
  - Internal name `ea_advanced_servicenow_subflow`
  - ServiceNow-side CCIF workflow suited for the advanced template path
- `EA_Simple_ServiceNow_Subflow.xml`
  - Published subflow name `EA_Simple_ServiceNow_Subflow`
  - Internal name `ea_simple_servicenow_subflow`
  - Lightweight CCIF workflow used to resolve the interaction and caller context
- Both variants remain ServiceNow Flow Designer subflow update set XML files that should be previewed and committed through the normal ServiceNow update set import process.

## Import guidance

1. In ServiceNow, open **Retrieved Update Sets**.
2. Choose **Import Update Set from XML**.
3. Upload the XML file that matches the variant you want to test.
4. Preview the update set and review any warnings or conflicts.
5. Commit the update set after validation is complete.

## Verify the subflow in ServiceNow

1. Open **Flow Designer** in ServiceNow.
2. Go to the **Subflows** page or open the subflow list from Flow Designer.
3. Search for the published subflow name that matches the imported file:
   - `EA_Advanced_ServiceNow_Subflow`
   - `EA_Simple_ServiceNow_Subflow`
4. Confirm the record appears in the list and is shown as a subflow.
5. Confirm the record status is `Published`.
6. Open the subflow and verify that the expected inputs and outputs are visible.

## If you do not see it

- Confirm the update set was successfully committed.
- Refresh the browser or reopen Flow Designer.
- Search again using both the published name and the internal name for the selected variant.
- Recheck preview or commit errors if the subflow still does not appear.

## Usage notes

- Treat these assets as part of the same ServiceNow CCIF implementation set as the update set in [`../update-set/`](../update-set/README.md) and the Webex flow templates in [`../sample-flow/`](../sample-flow/README.md).
- The with-subflow Webex flow template is configured to call `EA_Simple_ServiceNow_Subflow` by name.
- Import and validate the selected subflow in a non-production instance before production rollout.
