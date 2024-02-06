---
title: Configuration
nav_order: 3
---

# Configuring Sticky Selectron

## Data Sources
Sticky Selectron supports a single object, standard or custom. Selection of the object is defined during configuration.

## Sample Flow
Sticky Selectron comes with a Sample flow called Sticky Selectron Example Account Flow. This flow is deactivated and intended to demonstrate how to use Sticky Selectron. See the [Example Flows](https://sfdo-community-sprints.github.io/SSSFDG/docs/example-flows/) page for more information.

## Adding Sticky Selectron to a Screen Flow

In the components pane select 'Sticky Selectron' and drag it onto the screen.
_add screenshot here_

## Create Collections
The flow will need to reference a set of collections in the configuration so first build the collections. Below are sample collection names from the Sample Account flow provided with the installation. We recommend you name collections with more meaningful names to reflect your use-case.

| Sample Name |Description | Type |
| --- | --- | --- |
| **API Name** | List all *new or modified* files | Display_Sticky_Selectron_Accounts |
| **Input sObject Type** | Show file differences that **haven't been** staged | Show file differences that **haven't been** staged |
| **Input (Left) Table's Field Names** | List all *new or modified* files | List all *new or modified* files |
| **Input sObject collection**| Show file differences that **haven't been** staged | Show file differences that **haven't been** staged |
| **Selected (Right) Table's Field Names** | List all *new or modified* files | List all *new or modified* files |
| **Selected sObjects collection** | Show file differences that **haven't been** staged | Show file differences that **haven't been** staged |
| `git status` | List all *new or modified* files | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged | Show file differences that **haven't been** staged |


## Configuration Options
Below is a list of the settings that need to be configured.

| Setting Name |Description | Sample Value |
| --- | --- | --- |
| **API Name** | List all *new or modified* files | Display_Sticky_Selectron_Accounts |
| **Input sObject Type** | This is the Object used by Sticky Selectron  | Account |
| **Input (Left) Table's Field Names** | List all *new or modified* files | inputTableFieldNames |
| **Input sObject collection**| Show file differences that **haven't been** staged | InputAccountList |
| **Selected (Right) Table's Field Names** | List all *new or modified* files | selectedTableFieldNames |
| **Selected sObjects collection** | Show file differences that **haven't been** staged | SelectedAccountList |
| **Table Header** | List all *new or modified* files | Accounts |
| **Output the count of inputSObjectsList records** | Show file differences that **haven't been** staged | ListCount |
| **Output the count of selectedSObjectsList records** | Show file differences that **haven't been** staged | SelectedListCount |

**Advanced Settings**
Under Advanced Settings select the checkbox called **Manually assign variables**. There are three output configuration fields that need to be configured in Advanced Settings. Populate these with the same values used in the Standard settings.

| Setting Name |Description | Sample Value |
| --- | --- | --- |
| **Input sObject collection** | List all *new or modified* files | InputAccountList |
| **Output the count of selectedSObjectsList records** | Show file differences that **haven't been** staged | SelectedListCount |
| **Selected sObjects collection** | Show file differences that **haven't been** staged | SelectedAccountList |

Next review the [Example Flows](https://sfdo-community-sprints.github.io/SSSFDG/docs/example-flows/) page to see how to build the flow.
