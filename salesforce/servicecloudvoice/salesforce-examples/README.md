# Salesforce Service Cloud Voice Omni Flow Example

## Overview

This folder contains a packaged Salesforce metadata example for a Service Cloud Voice Omni Flow. The ZIP file is intended as a deployment example for administrators who want a starting point for Salesforce-side routing behavior that complements the Webex Contact Center Service Cloud Voice connector.

## Included assets

| File | Description |
| --- | --- |
| [`Sample_Salesforce_OmniFlow.zip`](./Sample_Salesforce_OmniFlow.zip) | Metadata deployment package containing a sample Salesforce routing flow |
| [`LICENSE.md`](./LICENSE.md) | License information for the sample content |

The ZIP package contains a sample flow named `WxCC_Routing_Flow` and a `package.xml` manifest suitable for Salesforce metadata deployment.

## What the sample flow does

The packaged flow demonstrates a basic Service Cloud Voice routing pattern that:

- reads a `VoiceCall` record
- looks up a Salesforce contact by phone number
- adds a screen pop entry for the matched record
- routes the work item through Salesforce Omni-Channel

Treat the packaged flow as a reference example. Queue identifiers, labels, matching logic, and routing behavior should be adjusted for the target Salesforce org.

## Deployment notes

Before deployment, make sure you have:

- access to a Salesforce org with the required Service Cloud Voice capabilities
- permissions to deploy metadata
- the related Webex Contact Center Service Cloud Voice connector configuration prepared

To deploy the ZIP package:

1. Sign in to [Salesforce Workbench](https://workbench.developerforce.com) or use your preferred metadata deployment process.
2. Open the metadata deployment function and upload [`Sample_Salesforce_OmniFlow.zip`](./Sample_Salesforce_OmniFlow.zip).
3. Review deployment settings, then submit the package.
4. After deployment, open Salesforce Setup and confirm that the sample flow is available.
5. Update queue IDs, labels, routing logic, and any related record-lookup behavior to match your environment before activation.

## Usage notes

- This example is designed to complement the assets documented in the parent folder README: [`../README.md`](../README.md).
- Use the sibling Webex flow template in [`../sample-flows/`](../sample-flows/README.md) when you need a matching Webex-side reference flow.
- Validate the flow in a sandbox before promoting it to a production environment.

## Current status

This folder provides a deployable Salesforce example package only. It does not replace environment-specific routing design, testing, or governance practices.
