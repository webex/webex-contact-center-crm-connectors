# ServiceNow CTI Connector

## Overview

This folder contains the current ServiceNow CTI assets for Webex Contact Center. The files here are intended for ServiceNow administrators who are deploying or updating the existing ServiceNow CTI integration and need the repository-hosted update set artifacts.

## Documentation

- Public setup guide: [Integrate Webex Contact Center with ServiceNow (Version 2-New)](https://help.webex.com/en-us/article/ny83tx0/Integrate-Webex-Contact-Center-with-ServiceNow-(Version-2-New)#reference-template_0b9dece3-d6e9-47c2-ae59-3b0c7ac71882)


## Included assets

| File | Description |
| --- | --- |
| [`updateSet.xml`](./updateSet.xml) | Main ServiceNow update set for the Webex Contact Center ServiceNow CTI integration |
| [`Global_WxCC_ClickToDial_UIMacro_UpdateSet_1.0.xml`](./Global_WxCC_ClickToDial_UIMacro_UpdateSet_1.0.xml) | Optional click-to-dial UI macro update set used to surface dialing actions in supported ServiceNow forms |


## Usage notes

- Import the main update set as part of the current ServiceNow CTI connector deployment.
- Use the click-to-dial macro update set when your deployment requires click-to-call actions from supported phone fields or reference records.
- Review ServiceNow platform prerequisites, required plugins, roles, and OpenFrame-related configuration in the public Webex Help guide before importing the assets.
- Validate the imported artifacts in a non-production instance and confirm agent desktop behavior, click-to-dial behavior, and integration settings before production rollout.

## Current status

This folder contains the currently published ServiceNow CTI repository assets only. Customer-specific instance configuration, credentials, and environment policies remain outside version control.
