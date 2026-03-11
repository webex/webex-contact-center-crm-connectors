# Salesforce Service Cloud Voice Sample Webex Flows

## Overview

This folder contains a Webex Flow Designer template that can be used as a reference for Salesforce Service Cloud Voice integrations. The template shows how Webex Contact Center can create and manage Salesforce voice-call context while passing routing data between Webex and Salesforce.

## Included assets

| File | Description |
| --- | --- |
| [`ServiceCloudVoice_Template.json`](./ServiceCloudVoice_Template.json) | Webex Flow Designer template for Service Cloud Voice integration scenarios |
| [`LICENSE.md`](./LICENSE.md) | License information for the sample content |

## What the template illustrates

- Creating a VoiceCall context for Salesforce from a Webex Contact Center flow
- Passing vendor call identifiers and related call metadata
- Persisting flow variables used by the Salesforce integration
- Supporting downstream routing and lifecycle updates for Service Cloud Voice scenarios

## Key variables in the template

The template includes integration-oriented variables such as:

- `SCV_VoiceCallRecordId`
- `SCV_CallStartTime`
- `SCV_OmniFlowQueue`
- `SCV_OmniFlowAgent`
- `SCV_VendorCallKey`
- `SCV_VoiceCallReference`

Review the JSON file directly for the full variable list and the exact HTTP request payloads used in the sample flow.

## Usage notes

- Import or adapt this JSON as a starting point, not as a drop-in production flow.
- Replace sample identifiers, connector references, certificate names, and environment-specific values before use.
- Validate the flow variable names against the values expected by your Salesforce Service Cloud Voice connector configuration.
- Use this folder together with the contact center XML in the parent folder and the Salesforce sample Omni Flow package in [`../salesforce-examples/`](../salesforce-examples/README.md).

## Current status

This is a reference template intended to accelerate design and validation work for Service Cloud Voice integrations. Production deployments should be reviewed and adjusted to match customer-specific routing, security, and naming conventions.
