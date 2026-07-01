# Customer Management Work Flow

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

**Account Information**

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Type | Dropdown | Customer or Dealer | - | YES |
| Name | Text | Name for the user | - | YES |
| Tax Payer ID | Number | Tax ID for user | Only input number | YES |
| Salutation | Dropdown | None, Mr, Ms, Mrs, Dr, Prof | - | NO |
| Email | Text | User email | Email Parameters Rules | NO |
| Mobile Phone | Number | User phone number | Need to start from +62/08/62 | YES |
| Business Phone | Number | User business phone number | Same rule as Mobile Phone | NO |
| Suffix | Text | Honorification | - | NO |
| Gender | Dropdown | Male or Female | - | NO |
| Status | Dropdown | Active or In Active | - | YES |
| Remark | Free Text | Note for user | - | No |
| Membership Type | Dropdown | None, Standard, Silver, Gold, Platinum, Diamond | - | No |

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