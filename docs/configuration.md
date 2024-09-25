---
title: Configuration
nav_order: 3
---

# Configuring Sticky Selectron

## Data Sources
Sticky Selectron supports the selection of records from a single object, standard or custom. Selection of the object is defined during configuration.

## Sample Flow
Sticky Selectron comes with a Sample flow called Sticky Selectron Example Account Flow. This flow is deactivated and intended to demonstrate how to use Sticky Selectron. The example flow is optional to install when using MetaDEPLOY to install Sticky Selectron. See the [Example Flows](https://sfdo-community-sprints.github.io/SSSFDG/docs/example-flows/) page for more information. This sample flow is referenced as example information in the configuration settings below.

## Known Field Display Limitations
Join us in making Sticky Selectron even better! These are the currently identified limitations for field display (and are part of our planned feature list). 

- Date/Time display are displayed as system values
- Relationship fields display the ID of the related record

## Configure Resources
The flow will need to reference a set of variables (Collection Variables, Record collection Variables and Variables) that you will need to build in order for the Sticky Selectron to reference them in configuration. 
We recommend that you create these resources before configuring Sticky Selectron. 
Below is a list of the Resources that you will need to create and how they are used/populated. The sample collection names are from the sample flow (Sticky Selectron Example Account Flow) provided in the package. We recommend you name collections with more meaningful names to reflect your use-case.

| Description | Type | Assignment/Use | Sample Name from flow |
| --- | --- | --- | --- |
| **Collection Variable:** Used to configure which columns should display on the left _selectable_ side | Variable, Data Type: Text, Allow Multiple values (collection): True, Available for input: True| Populated with an assignment element in the flow. See Assigning Table Columns| inputTableFieldNames |
| **Collection Variable:** Used to configure which columns should display on the right _selectable_ side | Variable, Data Type: Text, Allow Multiple values (collection): True, Available for input: True | Populated with an assignment element in the flow. See Assigning Table Columns | selectedTableFieldNames |
| **Record Collection Variable:** Record collection used to store the records that should be displayed on the left _selectable_ side  | Record Collection Variable, Data Type: Record, Object: The object you are selecting from, Allow Multiple values (collection): True, Available for input: True _Available for output: True IS THIS THE CASE?_ | Populated from within the flow with a *Get Records* Element or passed to the flow from another process | inputAccountList |
| **Record Collection Variable:** Record collection used to store the records that should be displayed on the right _seleced_ side  | Record Collection Variable, Data Type: Record, Object: The object you are selecting from, Allow Multiple values (collection): True, Available for input: True _Available for output: True IS THIS THE CASE?_  | Populated by Sticky Selectron when users select records from within the screen flow. NOTE: If you want to pre-populate this collection make sure the same records are also populated in the selectable Record Collection Variable _TEST THIS_  | selectedAccountList |
| **Variable:** Count of records in the SELECTABLE Record Collection Variable | Variable, Data Type: Number, Allow Multiple values (collection): False, Decimal Places: 0, Default Value: NULL | Populated by Sticky Selectron. You can reference this variable elsewhere in your flow | listCount |
| **Variable:** Count of records in the SELECTED Record Collection Variable | Variable, Data Type: Number, Allow Multiple values (collection): False, Decimal Places: 0, Default Value: NULL | Populated by Sticky Selectron. You can reference this variable elsewhere in your flow  | selectedListCount |

## Assign Column Display Collection Variables

Using an Assignment Element - Assign the columns you wish to display to the two collection variables you created to store the information. In the Sticky Selectron Example Account Flow this is demonstrated with two assignment elements - but it is possible to assign both collection variables in the same assignment element. Please note that you use the 'Add' Operator and the API name of the fields you wish to display for the Object Sticky Selectron will display. 

![Sticky Selectron Set Input Table Field Names Screenshot](Assets/Set_Input_Table_Field_Names.png)

## Adding and Configuring Sticky Selectron
Sticky Selectron is available from a Screen Element in Edit mode. Select Sticky Selectron from the Components tab and drag it into the screen. Once Sticky Selectron is on the screen elemenent, click on it so that you can configure it. Please follow the next section (Configuration Options) for information on how to configure each setting. 

![Sticky Selectron LWC Selection Screenshot](Assets/Sticky_LWC_Selection.png)

## Configuration Options
Below is a list of the settings that need to be configured.

| Setting Name |Description | Sample Value |
| --- | --- | --- |
| **API Name** | Whatever API Name you want to give the component | Display_Sticky_Selectron_Accounts |
| **Input sObject Type** | This is the Object used by Sticky Selectron, once you select an object and save this field will not be editable   | Account |
| **Input (Left) Table's Field Names** | This is the Collection Variable that is used to configure which columns should display on the left _selectable_ side  | inputTableFieldNames |
| **Input sObject collection**| This is the Record Collection Variable created to store the records that will be selectable | inputAccountList |
| **Selected (Right) Table's Field Names** | This is the Collection Variable that is used to configure which columns should display on the right _selected_ side | selectedTableFieldNames |
| **Selected sObjects collection** | This is the Record Collection Variable created to store the records that have been selected | selectedAccountList |
| **Table Header** | _HOW HAS THIS CHANGED?_ This is the header you want to display above the record selection UI | Accounts |
| **Output the count of inputSObjectsList records** | This is the Variable created that stores the count of records in the SELECTABLE Record Collection Variable | listCount |
| **Output the count of selectedSObjectsList records** | This is the Variable created that stores the count of records in the SELECTED Record Collection Variable | selectedListCount |

**Advanced Settings**
Under Advanced Settings select the checkbox called **Manually assign variables**. There are three output configuration fields that need to be configured in Advanced Settings. Populate these with the same values used in the Standard settings.

| Setting Name |Description | Sample Value |
| --- | --- | --- |
| **Input sObject collection** | This is the Record Collection Variable created to store the records that will be selectable | inputAccountList |
| **Output the count of selectedSObjectsList records** | This is the Variable created that stores the count of records in the SELECTED Record Collection Variable | selectedListCount |
| **Selected sObjects collection** | This is the Record Collection Variable created to store the records that have been selected | selectedAccountList |

Next review the [Example Flows](https://sfdo-community-sprints.github.io/SSSFDG/docs/example-flows/) page to see how to build the flow.
