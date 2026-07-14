# Asset Management Workflow

## Overview

Tracks physical assets belonging to customers or the service center — including model, serial number, purchase date, and service history. Assets are linked to work orders and warranty records.

## Header Table Data

| No | ID Asset | Serial Number | Model | Status | In Warranty | Last Updated By | Last Updated At | Action |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

## Create New Asset

1. Navigate to **Warranty & Asset Management** menu
2. Open **Asset Management** sub menu
3. Click **New** button
4. Fill in the field, here are the details :

### New Asset

#### Base Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Account Name | Searchable Dropdown | List all of the existing customer | - | YES |
| Mobile Phone | Text | Auto filled from selecting account name | - | NO |
| Email | Text | Auto filled from selecting account name | - | NO |

##### Asset Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Serial Number | Text | Product serial number | Unique | YES |
| Serial Number Type | Text | Auto filled from product | - | YES |
| Status | Dropdown | Active or Nonactive | - | YES |
| Description | Free Text | Product description | - | NO |
| Foreign Model | Text | - | - | NO |
| Product | Dropdown | List of existing product on database | - | YES |
| Compressor No. | Text | - | - | NO |
| Purchase Date | Date | - |  | NO |

#### Asset Hierarchy

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Parent Asset | Searchable Dropdown | - | - | NO |
| Asset Level | Text | - | - | NO |

5. Click **Save** button
6. Verify confirmation popup appear and click **Save** button
7. After saving the **Asset** it open the **Detail Asset**
8. Verify new Asset have been listed on the table
    - **In Warranty** status is set to **Inactive**

### Edit Asset

1. Access to **Warranty & Asset Management**
2. Navigate to **Asset Management**
3. Navigate to **Action**
    - Or navigate to **Details** and click **Edit** button from the detail page
4. Click **Edit** button
5. Verify **Edit Asset** is open
6. Update any field
7. Click **Save** button
8. Verify the changes

### Remove Asset _(Only performed by Superadmin)_

1. Access to **Warranty & Asset Management**
2. Navigate to **Asset Management**
3. Navigate to **Action**
4. Click **Remove** button
5. Verify confirmation popup appear and click **Delete** button
    - Asset can be removed if the asset itself don't have active Work Order
6. Verify the asset is removed from the table list