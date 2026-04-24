# Salesforce CTI Connector

## Overview

This folder contains the Salesforce call center metadata used with the Webex Contact Center CTI connector for Salesforce. The asset in this folder is intended for Salesforce administrators who need to import and maintain the call center definition that points Salesforce to the Webex Contact Center CTI adapter.

## Documentation

- Public setup guide: [Integrate Webex Contact Center with Salesforce (Version 2-New)](https://help.webex.com/en-us/article/dyidod/Integrate-Webex-Contact-Center-with-Salesforce-(Version-2-New))

## Included assets

| File | Description |
| --- | --- |
| [`OpenCTI.callCenter-meta.xml`](./OpenCTI.callCenter-meta.xml) | Salesforce call center definition with Webex Contact Center CTI settings, adapter URL, layout dimensions, and optional behavior flags |

## Configurable call center elements

| Section | Element | Label | Default value |
| --- | --- | --- | --- |
| Call Activity Record Creation | `subjectDateFormat` | Date Format In Subject | MM-DD-YYYY hh:mm a |
| Call Activity Record Creation | `subjectTemplate` | Subject Template | {direction} Call {activityDatetime} |
| Call Activity Record Creation | `recordCallLiveNotes` | Record Call Live Notes | true |
| Call Activity Record Creation | `recordCallLiveSubject` | Record Call Live Subject | true |
| Call Activity Record Creation | `liveCallNotesFieldMapping` | Live Call Notes Field Mapping | Description |
| Call Activity Record Creation | `changeActivityRecordOwnership` | Change Activity Record Ownership For Transferred Calls | false |
| Call Activity Record Creation | `cadVarNameWithActivityId` | CAD Variable Name That Holds Activity Id | (blank) |
| Call Activity Record Creation | `objectFieldMapping` | Object Field Mappings | (blank) |
| Call Activity Record Creation | `agentSharedRecord` | Variable for Record Sharing | (blank) |
| Call Activity Record Creation | `assignActivityToSharedRecord` | Use Activity as Shared Record by default | true |
| Call Activity Record Creation | `disableActivityRecord` | Disable Activity Record Creation | false |
| Call Activity Record Creation | `openCtiEnableActivityScreenPopConnected` | Enable Activity Screen Pop on Connected | false |
| Call Activity Record Creation | `openCtiEnableActivityScreenPopWrapup` | Enable Activity Screen Pop on Wrapup | false |
| Outdial Configuration | `outdialRemovePrefix` | Remove Phone Number Prefix Strings | (blank) |
| Outdial Configuration | `openCtiEnableCrmSearch` | Search For CRM records | false |
| Advanced Screen Pop Search Configuration | `openCtiEnableAdvancedScreenPop` | Advanced Screen Pop Enabled | false |
| Advanced Screen Pop Search Configuration | `openCtiCadSearchVariable` | CAD Variable Name | (blank) |
| Advanced Screen Pop Search Configuration | `openCtiRemoveANIPrefix` | Remove ANI Prefix Strings | (blank) |
| Advanced Screen Pop Search Configuration | `openCtiFallbackToAni` | Fallback to ANI | false |
| Case Management | `createObjectIncoming` | Auto Case Creation For Inbound Calls | false |
| Case Management | `createObjectOutgoing` | Auto Case Creation For Outbound calls | false |
| Case Management | `openInEditMode` | Open Case Object In Edit Mode | false |
| Case Management | `objectFieldMapping` | Object Field Mappings | (blank) |
| Screen Pop Settings For No Record Match | `noRecordMatchObjectFieldMappings` | Object Field Mappings | (blank) |
| Omni-Channel State Sync Configuration | `enableOmniChannelSync` | Enable Omni-Channel Sync | false |
| Omni-Channel State Sync Configuration | `omniChannelNotReadyReason` | Omni-Channel Not Ready Reason | (blank) |
| Omni-Channel State Sync Configuration | `wxCCIdleReasonCode` | WxCC Idle Reason Code | (blank) |
| Widget Settings | `sendBrowserNotifications` | Send Browser Notifications | false |

## Usage notes

- Import the call center definition into Salesforce as part of the CTI connector setup.
- Review the values in the metadata before deployment, especially region, WebRTC domain, adapter URL, activity logging settings, screen pop options, and Omni-Channel synchronization settings.
- Align the imported settings with your Webex Contact Center tenant and Salesforce configuration before assigning users to the call center.
- Use the public Webex Help guide for the end-to-end platform configuration steps; this folder provides the connector asset referenced during that setup.

## Current status

This folder currently contains the Salesforce CTI call center metadata only. Managed package components and org-specific configuration remain outside this repository.
