# User Management Work Flow

Outlines the authorization and account management flows designed to maintain system security. This document serves as the primary reference for validating permission boundaries, verifying data isolation during user creation, and testing account lifecycle states before deployment.

## Header Table Data

| No | ID | Name | Email | Phone | Email | Role | Status | Last Login Date | Last Update By | Last Update By |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

### Create New User

1. Access the **User Access Management**
2. Click **New User** button
3. Fill in the field, here are the details :

**Account Information**

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Role | Dropdown | Existing Role from @handover.md | - | YES |
| Salutation | Dropdown | None, Mr, Ms, Mrs, Dr, Prof | - | YES |
| Name | Text | Name for the user | - | YES |
| Email | Text | User email | Email Parameters Rules | YES |
| Password | Text | Auto-generated from system | - | YES |
| Mobile Phone | Number | User phone number | Need to start from +62/08/62 | YES |
| Business Phone | Number | User business phone number | Same rule as Mobile Phone | NO |
| Suffix | Text | Honorification | - | NO |
| Tax Payer ID | Number | Tax ID for user | Only input number | NO |
| Gender | Dropdown | Male or Female | - | NO |
| Status | Dropdown | Active or In Active | - | YES |
| Remark | Free Text | Note for user | - | No |

**Billing Address Information**

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Country | Searchable Dropdown | Indonesia (but can change from user input) | - | NO |
| Province | Dropdown | Indonesia Province | - | NO |
| City | Dropdown | City from selected Province | Need to select the Province field | NO |
| Sub District | Dropdown | City Sub District | Need to select the City | NO |
| Village | Dropdown | Village inside the Sub Disrict | Need to select the Sub District | NO |
| Street | Free Text | Street Address | - | NO |
| Postal Code | Text | Postal Code address is auto-generated from Village selection | - | NO |

**Mailing Address Information**

Same field as **Billing Address Information**

4. Click **Save** button
5. Verify new User have been listed on the table

### User Detail

1. Access the **User Access Management**
2. Navigate to **Action** section
3. Click **Details** button
4. Verify **User Details** is open

### Edit User

1. Access the **User Access Management**
2. Navigate to **Action** section
3. Click **Details** button
4. Verify **User Details** is open and can **Edit** the user
5. Made any changes from the field
6. Click **Save** button
7. Verify the updated details

### Filter Function
Filter can be perform with **Status** and **Role Name**

### Status Toggle
Status can be updated through a **Toggle**

### Export Button
As of creating the flow, **Export** function is not available yet