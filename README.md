# CTX-Manual-Intervention Cortex Module
The Manual Intervention module for Cortex allows a user to interact with a process execution (via UI or email) without the process having to be initiated by a user. This means that a user can log in to the dashboard flow and see everything which needs their attention.

This is done by pausing the process flow, and only triggering the relevant UI flow when the user requests it. The data is passed back to the main process flow which is then continued.


## Table of Contents
1) [Dependencies](#dependencies)
    * [Cortex Version](#cortex-version)
    * [OCIs](#ocis)
    * [Files](#files)
    * [Other](#other)
1) [Support and Warranty](#support-and-warranty)
2) [Installation](#installation)
3) [How to use](#how-to-use)
4) [How you can contribute](#how-you-can-contribute)
5) [Versioning](#versioning)
6) [Licensing](#licensing)


## Dependencies
### Cortex Version
This version of the CTX-Manual-Intervention module was developed in Cortex version 6.4. Some functionality may not be available on different verions of Cortex.

### OCIs
The  module requires the following Cortex OCIs:
* Database
* HTTP

### Files
The CTX-Manual-Intervention module requires the following files:
* [CTX-Manual-Intervention.studiopkg](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/CTX-Manual-Intervention.studiopkg)
* [Additional LivePortal Files](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/LivePortal.Components.zip)
* [SQL Upgrade Scripts](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/Upgrade.SQL.Scripts.zip)


### Other
The CTX-Manual-Intervention module has the following additional requirements which are explained in detail in the [Installation section](#Installation):
* Cortex Audit Logging Solution
* Cortex Config Store Solution

## Support and Warranty 
This module is supplied as a template that you can amend and extend to fit your requirements, as such it is not supported as part of the Cortex Product suite under the Cortex product support agreement.

## Installation
Details of the installation can be found in the [CTX-Manual-Intervention Deployment Plan](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/blob/master/CTX-Manual-Intervention%20-%20Deployment%20Plan.pdf).

The steps to upgrade differ depending on whether the Logging Database was installed as a Partitioned or Non-Partitioned database. These are details in the Deployment Plan and the relefvant files for each can be found below:

### Partitioned Logging Solution
For upgrading the Logging Database to support Manual Intervention, the Stored Procedure must be updated with the [Stored Procedure Upgrade Script](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/CommitLog.sql).

If the Logging Database was installed as a partitioned solution, you will also need to upgrade another stored procedure by running the [ProcessLog Stored Procedure Upgrade Script](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/usp_PART_ProcessLog.sql).

### Non-Partitioned Logging Solution
For upgrading the Logging Database to support Manual Intervention, the Stored Procedure must be updated with the [Stored Procedure Upgrade Script](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/CommitLog.sql).

If the Logging Database was installed as a non-partitioned solution, you can modify the table directly with the [ProcessLog Upgrade Script](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/releases/download/v1.0/ProcessLog.Recreate.sql).

## How to use
A detailed User Guide has been provided with instructions on how to use the flows/subtasks, available [here](https://github.com/CortexIntelligentAutomation/CTX-Manual-Intervention/blob/master/CTX-Manual-Intervention%20-%20User%20Guide.pdf). Configuration of subtask inputs and outputs are detailed in notes on the subtask workspace.

## How you can contribute
Unfortunately, we cannot offer pull requests at this time or accept any improvements.

## Versioning
CTX-Manual-Intervention has the following versions, starting with the most recent: v1.0

## Licensing
All functionality within this module is licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).

Copyright 2018 Cortex Limited

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


