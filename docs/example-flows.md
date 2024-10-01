---
title: Example Flows
nav_order: 4
has_children: true
---

# Example Flows

Here are some examples of how you might use the Sticky Selectron component from within a screen flow.

## Sticky Selectron Example Account Flow

When installing Sticky Selectron through MetaDEPLOY, you can optionally install this sample flow.
This flow is deactivated and intended to demonstrate how to use Sticky Selectron. 

Below is a breakdown explaining the flow.

**Overview**

<img alt="Sample Account Flow Overview Screenshot" src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Overview.png" width="50%" >

**Resources & Elements**

The resources are described in the [configuration](/sticky-selectron-documentation/docs/configuration/) document. 

<img alt="Sample Account Flow Resources and Elements"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Resources.png" width="35%" >

**Explanation**

1. Assign the left (Unselected) columns by adding the field API name to the Input_Table_Field_Names variable. This variable stores the column field names and defineds which columns will be displayed. Assign up to five columns. If using a custom field use the field's API name (with __c at the end). Sticky Selectron left-to-right column display corresponds to top to bottom field assignment. 
![Sticky Selectron Set Input Table Field Names Screenshot](Assets/Set_Input_Table_Field_Names.png)
2. Assign the right (Selected) columns by adding the field API name to the Selected_Table_Field_Names variable. This variable stores the column field names and defineds which columns will be displayed. Assign up to two columns. If using a custom field use the field's API name (with __c at the end). Sticky Selectron left-to-right column display corresponds to top to bottom field assignment.
![Sticky Selectron Set Selected Table Field Names Screenshot](Assets/SampleAccountFlow_Set_Selected_Columns.png)
3. The Get Records element retrieves Account records and assigns them to the input_Account_List record variable. This is the collection of unselected records. Assignment to the variable is achieved in the section 'How to Store Record Data' set to: 'Choose fields and assign variables (advanced)', and the input_Account_List is populated in the Record Collection Field. This configuration also requires the selection of which fields to store. 
- _The column header fields MUST be selected and available in order to display those columns and related data in Sticky Selectron._
- <img alt="Sample Account Flow Get Variable Assignment"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_VarAssignment.png" width="50%" >
4. This is a screen component using Sticky Selectron. When clicking on Sticky Selectron you can see the configuration settings. Be sure to check the advanced settings as well as three fields need to be populated. 
- <img alt="Sample Account Flow Sticky Selectron Configuration 1"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Configuration1.png" width="80%" >
- <img alt="Sample Account Flow Sticky Selectron Configuration 2"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Configuration2.png" width="80%" >
- <img alt="Sample Account Flow Sticky Selectron Configuration 3"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Configuration3.png" width="80%" >

