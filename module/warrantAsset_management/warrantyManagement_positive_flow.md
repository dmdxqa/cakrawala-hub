# Warranty Management Workflow

## Overview

Manages warranty records tied to assets. Tracks warranty coverage periods, claim eligibility, and expiry — feeding into the Invoice Register Warranty report.

## Header Table Data

| No | ID | Register As | Warranty Registration Name | Serial Number | Purchase Date | Activation | Purchase From | Purchase Invoice No | Price | Installation Date | Status | Registration Date | Created At | Updated By | Updated At | Action |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

## Create New Warranty

1. Navigate to **Warranty & Asset Management** menu
2. Open **Warranty Management** sub menu
3. Click **New** button
4. Fill in the field, here are the details :

### New Warranty

#### Base Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Registering as | Dropdown | Customer or Dealer | - | YES |
| Name | Searchable Dropdown | List all of the existing customer | - | YES |
| Email | Text | Auto filled from selecting account name | - | YES |
| Mobile Phone | Text | Auto filled from selecting account name | - | YES |

#### Warranty Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Asset | Searchable Dropdown | List of existing asset on database | - | YES |
| Name Category | Text | Product category name | - | YES |
| Model Number | Text | Product model number | - | YES |
| Purchase Date | Date | Date of product purchase | - | YES |
| Purchase From | Text | Seller or vendor name | - | NO |
| Purchase Invoice Number | Text | Invoice reference number | - | NO |
| Price | Text | Purchase price | - | NO |
| Source of Registration | Text | Where warranty was registered | - | NO |
| Installation Date | Date | Date of product installation | - | NO |
| Status | Dropdown | Verified or Unverified | - | YES |
| Registration Date | Date | Auto filled - warranty registration date | - | YES |
| Warranty Expiry Date | Text | End date of warranty coverage | - | YES |
| Country of Origin | Text | Country where product was manufactured | - | NO |

#### System Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Warranty Registration Name | Text | Auto generated - unique warranty reference | - | NO |
| Created At | Text | Auto filled - record creation timestamp | - | NO |
| Updated By | Text | Auto filled - user who last modified the record | - | NO |
| Updated At | Text | Auto filled - last modification timestamp | - | NO |

5. Click **Save** button
6. Verify confirmation popup appear and click **Save** button
7. After saving the **Warranty** it open the **Detail Warranty**
8. Verify new Warranty have been listed on the table

### Edit Warranty

1. Access to **Warranty & Asset Management**
2. Navigate to **Warranty Management**
3. Navigate to **Action**
    - Or navigate to **Details** and click **Edit** button from the detail page
4. Click **Edit** button
5. Verify **Edit Warranty** is open
6. Update any field
7. Click **Save** button
8. Verify the changes

### Remove Warranty _(Only performed by Superadmin)_

1. Access to **Warranty & Asset Management**
2. Navigate to **Warranty Management**
3. Navigate to **Action**
4. Click **Remove** button
5. Verify confirmation popup appear and click **Delete** button
    - Warranty can be removed if the asset itself don't have active Work Order
6. Verify the warranty is removed from the table list