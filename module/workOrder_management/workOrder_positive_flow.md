# Work Order Workflow

## Overview

The Work Order Management module is the core operational module of Cakrawala Hub. It allows staff to create, assign, and track Work Orders (WO) for maintenance and repair jobs. Each WO captures the customer, asset, job description, assigned technician, status, and associated costs — supporting the full WO lifecycle from creation through completion and closure.

## Header Table Data

| No | WO Number | Assigned By | Status | Sub Status | WO Type | In Warranty | Created By | Created At | Current Territory | Customer User | Customer Mobile Phone | Customer Business Phone | Aging |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

## Create New Work Order

1. Access to **Work Order Management**
2. Click **New Work Order** button
3. Fill in the field, here are the details :

### Work Order Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| ID Case | Text | Auto-generated from system | - | NO |
| Work Type | Dropdown | Repair, Dealer Support, Installation, PCB Refurb, Maintenance, Testing & Commission, Project | Default : Repair | YES |
| Job Type | Dropdown | Walk-In or Onsite | - | YES |
| Status | Dropdown | New, In Progress, Completed, Close, Cancelled | Default : New | YES |
| Sub Status | Dropdown | List based on status being selected | Default : Draft | YES |
| Priority | Dropdown | None, Low, Medium, High | Default : Medium | YES |
| Job Reason | Dropdown | List based on status being selected | - | NO |
| Creation Date | Date | Auto-filled: current date & time | - | YES |
| Creation Name | Text (read-only) | Auto-filled: logged-in user | - | YES |
| Subject | Text | - | - | NO |
| Deposit | Currency | - | Default: Rp 0 | NO |
| Description | Free Text | - | - | NO |

#### Customer Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Name | Dropdown + Add | - | Select existing or add new customer | YES |
| Phone Number | Text (read-only) | Auto-filled from selected customer | - | NO |
| Business Phone | Text (read-only) | Auto-filled from selected customer | - | NO |
| Region | Text (read-only) | Auto-filled from selected customer | - | NO |
| Province | Text (read-only) | Auto-filled from selected customer | - | NO |
| Sub District | Text (read-only) | Auto-filled from selected customer | - | NO |
| City | Text (read-only) | Auto-filled from selected customer | - | NO |
| Village | Text (read-only) | Auto-filled from selected customer | - | NO |
| Street | Text (read-only) | Auto-filled from selected customer | - | NO |
| Postal Code | Text (read-only) | Auto-filled from selected customer | - | NO |

#### Service Territory

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Name Service Territory | Text (read-only) | Auto-filled: logged-in user's territory | - | NO |
| Account | Text | - | - | NO |
| Country | Text (read-only) | Auto-filled from service territory | - | NO |
| Province | Text (read-only) | Auto-filled from service territory | - | NO |
| City | Text (read-only) | Auto-filled from service territory | - | NO |
| Sub District | Text (read-only) | Auto-filled from service territory | - | NO |
| Village | Text (read-only) | Auto-filled from service territory | - | NO |
| Postal Code | Text (read-only) | Auto-filled from service territory | - | NO |
| Street | Text (read-only) | Auto-filled from service territory | - | NO |

#### Product Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Asset Name | Dropdown + Add | - | Select existing or add new asset from Customer Data | YES |
| In Warranty | Checkbox (read-only) | Auto-filled based on selected asset | - | NO |
| Model Code | Text (read-only) | Auto-filled from selected asset | - | YES |
| Category Name | Text (read-only) | Auto-filled from selected asset | - | YES |

#### IRIS Information — Pre-Service

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Condition Code | Dropdown | - | - | YES |
| Condition Detail | Free Text | - | - | NO |
| Symptom Group | Dropdown | - | - | YES |
| Symptom Group 2 | Dropdown | - | - | YES |
| Symptom Details | Free Text | - | - | NO |
| Accessories Received | Free Text | - | - | NO |
| ARC Code | Dropdown | - | - | NO |
| MQC Code | Dropdown | - | - | NO |

#### IRIS Information — Post-Service (Active when Status is In Progress)

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Defect Code | Dropdown | - | - | NO |
| Defect Details | Text | - | - | NO |
| Repair Code | Dropdown | - | - | NO |
| Repair Detail | Text | - | - | NO |
| Technical Remarks | Text | - | - | NO |
| Product Condition | Text | - | - | NO |
| Special Instructions to Part Admin | Text | - | - | NO |

#### Technician Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Technician Name 1 | Dropdown | Existing Technician under Service Center (GDN or PASS) | - | YES |
| Service Territory Name | Text (read-only) | Auto-filled from selected technician | - | YES |


### Service Appointment _(Visible only when Job Type is **Onsite**)_

#### Service Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Status | Dropdown | Scheduled, Draft, Dispatched, In Progress, Cannot Complete, Complete, Close, Cancel, On The Way, - | Default: Scheduled | YES |
| Appointment Type | Dropdown | Service or Logistic | Default: Service | YES |
| Description | Free Text | - | - | NO |
| Subject | Text | - | - | NO |
| Service Note | Free Text | - | - | NO |

#### Address Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Country | Text (read-only) | Auto-filled from selected customer | - | NO |
| Province | Text (read-only) | Auto-filled from selected customer | - | NO |
| City | Text (read-only) | Auto-filled from selected customer | - | NO |
| Sub District | Text (read-only) | Auto-filled from selected customer | - | NO |
| Village | Text (read-only) | Auto-filled from selected customer | - | NO |
| Postal Code | Text (read-only) | Auto-filled from selected customer | - | NO |
| Street | Text (read-only) | Auto-filled from selected customer | - | NO |

#### Scheduled Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Schedule Start Date | Date | - | Default: current date | NO |
| Schedule Start Time | Time | - | Format: HH:mm | NO |
| Schedule End Date | Date | - | Default: current date | NO |
| Schedule End Time | Time | - | Format: HH:mm | NO |
| Duration Type | Dropdown | - | - | NO |
| Duration | Text (read-only) | Auto-calculated from start & end time | - | NO |

#### Actual Information _(Active only when Status is **In Progress**)_

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Actual Start Date | Date | - | - | NO |
| Actual Start Time | Time | - | Format: HH:mm | NO |
| Actual End Date | Date | - | - | NO |
| Actual End Time | Time | - | Format: HH:mm | NO |
| Duration Type | Dropdown | - | - | NO |
| Duration | Text (read-only) | Auto-calculated from actual start & end time | - | NO |

4. Click **Save** button
5. After saving the **Work Order** it open the **Detail Work Order**
6. Verify new Work Order have been listed on the table

### Work Order Detail

1. Access to **Work Order Management**
2. Navigate to **Action** section
3. Click **Details** button
4. Verify **Work Order Details** is open

### Edit Work Order

1. Access to **Work Order Management**
2. Navigate to **Action**
    - Or navigate to **Details** and click **Edit** button from the detail page
3. Click **Edit** button
4. Verify **Edit Work Order** is open
5. Update any field
6. Click **Save** button
7. Verify the changes

### Filter Function
Filter can be performed with **Status**, **Sub Status**, **Service Territory**, **Created By**, and **Created Date**

### Search Function
Search function can be performed with searching **WO Number**, **Status**, **Sub Status**, **Created By**

### Pagination
Pagination is increment by 10, 25, 50 and 100

---