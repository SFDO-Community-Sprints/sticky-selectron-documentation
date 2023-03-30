# Speedy Sticky Salesforce Data Grid Lightning Web Component

---

## Summary

Speedy Sticky Salesforce Data Grid (S3DG) is a Lightning Web Component (LWC) that enables easy Contact selection in a Salesforce Screen Flow.

## Use Case

Multiple services to the same group of contacts.

## Key Requirements for the Custom LWC

1. LWC within a Screen Flow. Can read flow-defined collection
2. Multi-Screen Display, Support for persisting revisions
3. Selected records stored in distinct collection
4. Handle 2K records without huge slow-down
5. Customizable column display and table header
6. Sorting and searching with persistent selection
7. Easy to select, de-select and see what is selected
8. Familiar UI to simplify user experience
9. Collaborate & Give Back to the Community!

## Installation

- Make sure that you have logged out of all Salesforce Orgs.
- Click on the following link, then log in to the Org that the LWC component will be installed on. The Package ID is **04t5c0000014WigAAE**.

  [https://login.salesforce.com/packaging/installPackage.apexp?p0=04t5c0000014WigAAE](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t5c0000014WigAAE)

- Choose an install option: Install for Admins Only, Install for All Users, or Install for Specific Profiles...

  ![My Image](images/readme-install-s3dg-package.png)

- Click on the Install button.

- When the "Installation Complete!" message is displayed, click on the Done button.

## Flow Component Setup

- Launch the Screen Flow.

- Create two record collection variables:

  1. **collectionContactList** which is the main contact list containing all the fields that will be displayed.

     ![My Image](images/readme-new-variable-collectioncontactlist.png)

  2. **collectionSelectedContactList** which is the list of s`elected contacts.

- Create count and table header variables:

  1. listCount (Data Type: Number; Decimal Places: 0; Default Value: 0)
  2. selectedListCount (Data Type: Number; Decimal Places: 0; Default Value: 0)
  3. tableHeader (Data Type: Text; Default Value: Contacts)

- Add Screen Element to your Flow.

  ![My Image](images/readme-add-variables-and-screen-element.png)

- Find the component in the Custom section and drag it onto the canvas.

  ![My Image](images/readme-find-component-and-drag-to-canvas-for-screen-element.png)

- Assign variables, field names, and field labels.

  ![My Image](images/readme-assign-variables-field-names-and-field-variables.png)

- Edit Table Header text.

  ![My Image](images/readme-edit-table-header-text.png)

- Make sure that your Record Collection variable for the Contact List is storing all the Contact Fields to display in the data tables.

  ![My Image](images/readme-store-contact-fields-in-record-collection-variable.png)

- In the Advanced section, make sure to assign the Record Collection, Count, and Table Header variables.

  ![My Image](images/readme-store-output-values-to-select-variables.png)

## LWC in Action

- Initial listing showing message to please select at least one person.

  ![My Image](images/readme-sample-listing.png)

- Click on the Select header to sort all selected items at the top of the list.

  ![My Image](images/readme-sample-sort-by-selected-items.png)

## Acknowledgements

- [Bigger Boat Consulting](https://biggerboatconsulting.com/)

  ![Bigger Boat Consulting logo](images/bigger-boat-consulting-logo.png)

- [Purple Maiʻa Foundation](https://purplemaia.org/)

  ![Purple Maiʻa Foundation logo](images/purple-maia-logo.jpg)

## Contributors &amp; Maintainers

- [David Pickett / pickettd](https://github.com/pickettd)
- [Karen Sabog / kalena](https://github.com/kalena)
- [Bhanudas Tanaka / bhanudas](https://github.com/bhanudas)

**Current Version:** 0.1
