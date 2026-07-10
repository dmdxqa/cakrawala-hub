# Customer Management Workflow

## Overview

Outlines the standard lifecycle for onboarding and managing customer data within the ecosystem. This workflow governs customer profile creation, asset linking, and account association to ensure all subsequent Work Orders and Sales Orders map accurately to the correct customer records.

## Header Table Data

| No | ID Customer | Name | Unified ID | Primary Email | Email | Mobile Phone | Business Phone | Status | Updated By | Updated At |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

### Create New Customer

1. Access the **Customer Management**
2. Click **New Customer** button
3. Fill in the field, here are the details :

#### Account Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Type | Dropdown | Customer or Dealer | - | YES |
| Name | Text | - | - | YES |
| Tax Payer ID | Number | - | Numeric input only | YES |
| Salutation | Dropdown | None, Mr, Ms, Mrs, Dr, Prof | - | NO |
| Email | Text | - | Must follow email format | NO |
| Mobile Phone | Number | - | Must start from +62/08/62 | YES |
| Business Phone | Number | - | Must start from +62/08/62 | NO |
| Suffix | Text | - | - | NO |
| Gender | Dropdown | Male or Female | - | NO |
| Status | Dropdown | Active or Inactive | - | YES |
| Remark | Free Text | - | - | NO |
| Membership Type | Dropdown | None, Standard, Silver, Gold, Platinum, Diamond | - | NO |

#### Billing Address Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Country | Searchable Dropdown | - | Default: Indonesia, but can be changed | NO |
| Province | Dropdown | - | - | NO |
| City | Dropdown | - | Depends on Province selection | NO |
| Sub District | Dropdown | - | Depends on City selection | NO |
| Village | Dropdown | - | Depends on Sub District selection | NO |
| Street | Free Text | - | - | NO |
| Postal Code | Text (read-only) | Auto-generated from Village selection | - | NO |

#### Mailing Address Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Country | Searchable Dropdown | - | Default: Indonesia, but can be changed | NO |
| Province | Dropdown | - | - | NO |
| City | Dropdown | - | Depends on Province selection | NO |
| Sub District | Dropdown | - | Depends on City selection | NO |
| Village | Dropdown | - | Depends on Sub District selection | NO |
| Street | Free Text | - | - | NO |
| Postal Code | Text (read-only) | Auto-generated from Village selection | - | NO |

4. Click **Save** button
    - Additionally, if click **Save & New** it will save the current customer and open a new customer field
5. Verify new User have been listed on the table
6. Verify **Source Created**, if the Customer created via **Partner Portal** or **Customer Portal**

### Customer Detail

1. Access the **Customer Management**
2. Navigate to **Action** section
3. Click **Details** button
4. Verify **Customer Details** is open

### Edit Customer

1. Access the **Customer Management**
2. Navigate to **Action** section
3. Click **Details** button
4. Verify **Customer Details** is open and can **Edit** the user
5. Made any changes from the field
6. Click **Save** button
7. Verify the updated details

### Filter Function
Filter can be perform with **Status** and **Member Type**

### Status Toggle
Status can be updated through a **Toggle**

### Search Field
Search field are used to find **Customer**

### Pagination
Pagination is increment by 10, 25, 50 and 100