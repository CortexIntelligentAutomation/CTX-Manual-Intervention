<a href="https://www.cortex-ia.co.uk/" target="_blank"><img src="https://github.com/CortexIATest/CTXImages/blob/master/Cortex-350-120.png" alt="Welcome to Cortex!" width="350" height="120" border="0"></a>

# CTX-Manual-Intervention Cortex Module
The Manual Intervention module allows Cortex flows and processes to be run separately from any User Interactions. 
This allows a user to view and launch any pending UIs from a dashboard flow.
By using this module, processes can be run with a Case Management style interaction.

This functionality is achieved by using the Cortex-Logging module.
This module can also support Access Control, restricting different processes to certain Active Directory groups.

The module allows users to perform the following functionality:
* Pause a flow and wait for a User Interactions
* View all processes and if required, launch the UI for that process in a new tab
* Resume a flow from an opened UI flow
* Assign an AD Group to a Process execution

The following features are planned for v1.1:
* Email a link to the Dashboard flow to a user or group of users once the UI is pending.
* Send / Receive an email in place of a UI for a paused process
* Allow intergration with 3rd party UI

## Table of Contents
1) [Dependencies](#dependencies)
    * [Cortex Version](#cortex-version)
    * [OCIs](#ocis)
    * [Files](#files)
    * [Other](#other)
2) [Installation](#installation)
3) [How to use](#how-to-use)
4) [How you can contribute](#how-you-can-contribute)
5) [Versioning](#versioning)
6) [Licensing](#licensing)


## Dependencies
### Cortex Version
This version of the CTX-Manual-Intervention module was developed in Cortex version 7.1. Some functionality may not be available on different versions of Cortex.

### OCIs
The  module requires the following Cortex OCIs:
* Database
* HTTP
* PowerShell (optional for Access Control extensions)

### Files
The CTX-Manual-Intervention module requires the following files:
* [CTX-Manual-Intervention.studiopkg](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/1.0/CTX-Manual-Intervention.studiopkg)
* [CTX-Manual-Intervention-Components.zip](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/1.0/CTX-Manual-Intervention-Components.zip)

### Other
The CTX-Manual-Intervention module has the following additional requirements which are explained in detail in the [Installation section](#Installation):
* Cortex-Logging Solution
* Manual Intervention Config File

## Installation
Details of the installation can be found in the [CTX-Manual-Intervention Deployment Plan](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/blob/master/CTX-Manual-Intervention%20-%20Deployment%20Plan.pdf).
This document covers the deployment of all the module requirements, including the additional LivePortal components and the Manual Intervention Config File.
For the Cortex-Logging solution, see [Cortex-Logging Github Module](https://github.com/CortexIntelligentAutomation/CTX-Logging)

## How to use
A detailed User Guide has been provided with instructions on how to use the flows/subtasks, available [here](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/blob/master/CTX-Manual-Intervention%20-%20User%20Guide.pdf). Configuration of subtask inputs and outputs are detailed in notes on the subtask workspace.

## How you can contribute
Unfortunately, we cannot offer pull requests at this time or accept any improvements.

## Versioning
CTX-Manual-Intervention has the following versions, starting with the most recent: v1.0
Version | Release | Functionality | Notes
------------ | ------------- | ----------- | -----------
v1.0 | 18/10/2021 | Manual Intervention - first full release | Created

## Licensing
All functionality within this module is licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).

Copyright 2021 Cortex Limited

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


