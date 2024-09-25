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

<img alt="Sample Account Flow Overview Screenshot" src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Overview.png" width=50% >

**Resources & Elements**

The resources are described in the [configuration](/sticky-selectron-documentation/docs/configuration/) document. 

<img alt="Sample Account Flow Resources and Elements"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_Resources.png" width=50% >

**Explanation**

1. Assign the left (Unselected) columns. Up to five columns. If using a custom field use the field's API name (with __c at the end).
![Sticky Selectron Set Input Table Field Names Screenshot](Assets/Set_Input_Table_Field_Names.png)
2. Assign the right (Selected). Up to two Columns.
3. The Get Records element is where the collection of unselected records is populated. This collection doesn't have to be populated directly from a Get elements as demonstrated, but it does have to be populated. It could, for example, also be populated with an assignment element. In this case the configuration for How to Store Record Data is 'Choose fields and assign variables (advanced), and the input_Account_List was populated in the Record Collection Field.
_If Choosing Fields, the Column header fields MUST be selected in order to display those columns in Sticky Selectron._
<img alt="Sample Account Flow Get Variable Assignment"  src="/sticky-selectron-documentation/docs/Assets/SampleAccountFlow_VarAssignment.png" width=25% >
4. This is a screen component using Sticky Selectron. When clicking on Sticky Selectron you can see the configuration settings. Be sure to check the advanced settings as well as three fields need to be populated. 



