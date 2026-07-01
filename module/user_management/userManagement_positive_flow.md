# User Management Workflow

## Overview

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
| Role | Dropdown | Existing Role from system | - | YES |
| Salutation | Dropdown | None, Mr, Ms, Mrs, Dr, Prof | - | YES |
| Name | Text | - | - | YES |
| Email | Text | - | Must follow email format | YES |
| Password | Text | - | Auto-generated from system | YES |
| Mobile Phone | Number | - | Must start from +62/08/62 | YES |
| Business Phone | Number | - | Must start from +62/08/62 | NO |
| Suffix | Text | - | - | NO |
| Tax Payer ID | Number | - | Numeric input only | NO |
| Gender | Dropdown | Male or Female | - | NO |
| Status | Dropdown | Active or Inactive | - | YES |
| Remark | Free Text | - | - | NO |

**Billing Address Information**

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Country | Searchable Dropdown | - | Default: Indonesia, but can be changed | NO |
| Province | Dropdown | - | - | NO |
| City | Dropdown | - | Depends on Province selection | NO |
| Sub District | Dropdown | - | Depends on City selection | NO |
| Village | Dropdown | - | Depends on Sub District selection | NO |
| Street | Free Text | - | - | NO |
| Postal Code | Text (read-only) | Auto-generated from Village selection | - | NO |

**Mailing Address Information**

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