# Business Workflow

## Header Table Data

| No | ID Sales | WO Number | Status | Sub Status | Order Type | Customer Name | Created By | Created At |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## GDN SO Walk-In Type

1. Access the **Sales Order Management > GDN**
2. Click **New Sales Order** button
3. Fill in the required fields, here are the details:

### Account Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Sales Order Type | Dropdown | Walk In | - | YES |
| Account Name | Text (Read-only) | Auto-populated from logged-in user account | - | NO |
| Customer Name | Searchable Dropdown | Select from existing customer list | - | YES |
| Order Date | Date Picker | Date of order creation | - | YES |
| Order Priority | Dropdown | Planned, Normal, Urgent | - | YES |
| Delivery Method | Dropdown | Delivery or Pickup | - | YES |
| Delivery Courier | Dropdown | Courier selection for delivery | - | NO |
| Console Shipment | Checkbox | Option to flag as console shipment | - | NO |
| Deposit | Currency Input | Deposit amount in Rp | Default: Rp 0 | NO |
| Description | Free Text | Order description or special notes | Max 500 characters | NO |

4. Click **Save** button and verify redirect to newly created sales order

#### Part Request Section

_Part Request Section_ is used for requesting and storing a part(s) from Local (service center stock itself) and Non local (CPC or other GDN SC).

1. Click **Part Request** button
2. **Part Request Popup** appear
3. Fill in the field, here are the details :

##### Part Request Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| SO Number | Text (read-only) | Auto-filled from selected Sales Order | - | YES |
| City | Text (read-only) | Auto-filled from Sales Order Service Territory | - | YES |
| Name Account | Text (read-only) | Auto-filled from selected customer | - | YES |
| Model | Dropdown | List model are shown from system inventory | Default : Model from Sales Order | YES |
| Part Number | Dropdown | List Part Number are shown based on Model selection | - | YES |
| Part Description | Text (read-only) | Auto-filled based on selected Part Number and Model | - | YES |

4. Click **Search** button
5. Verify **Request Part** table is appear, here are the header table data :

| Add | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

6. Select **Local Part** by clicking **Add** from the table
    - **Sales Order Walk-in Type** ONLY shown **Local Part**
    - Can select multiple part
7. Click **Add Part** button
8. **Selected Part Request** is appear, here are the detail header table data :

| ASC Buy | Requested Quantity | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Total Price Request | Total Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

9. Input **Requested Quantity** and Click **Request Part & Save** button
10. **Confirmation Popup** appear with **Request Part Detail** and Click **Request Part** button
11. Verify **Request Part** is appear on the **Part Request** section with status **Waiting for Submit**, also sub status is **Waiting for Submit**
    - **Available Stock** decreased and stock change to **Reserved Quantity** based on quantity inputted
    - If **Cancelled**, **Available Stock** increase and **Reserved Quantity** return to 0

### Send SO Request

1. Click **Send SO Request** button
2. Verify popup confirmation appear and select **Progress** button
3. Verify **SO** status is change to **In Progress** and sub status **Part Available** also **Part** status is change to **Buy Part for Customer**

### Generate SO Walk-In Invoice
1. Verify **Generate Invoice** button is active
2. Click **Generate Invoice** button
3. After clicking **Generate Invoice**, verify it shown a **Invoice Preview**
    - When closing **Invoice Preview**, it will shown **Confirmation** popup
    - Invoice shown based on Part Request and Charge section
4. Click **Save Invoice & Print** to save the **Invoice** and verify redirect to **Printing** preview
    - User can opt out, from **Printing** preview
5. Verify **Invoice** is appear on the **Invoice** section and digital invoice is appear on the **File & Attachment** section
6. Verify SO status is change to **Close** with Sub status **Invoice (Unpaid)** also **Part** status is change to **Invoice (Unpaid)**

### SO Invoice Payment

1. User navigate to **Invoice Detail**
2. Click **Payment** button and select **New Payment** button
3. **Create Payment** popup appear, here are the details :

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Payment/Refund Method | Dropdown | Cash, Cheque, E-Wallet, E-Payment, Credit Card, Credit Term, QRIS | - | YES |
| Transaction Amount | Text | Auto-filled from the Generated Invoice total amount | - | NO |
| Cheque No | Text | - | - | NO |
| Remark | Text | - | - | NO |

5. Click **Save** button and verify **Payment** is appear on the **Payment Transaction** section
6. Verify SO status is change to **Close** with Sub status **Invoice (Paid)**