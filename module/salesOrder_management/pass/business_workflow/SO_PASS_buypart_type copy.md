# Business Workflow

## Header Table Data

| No | ID Sales | WO Number | Status | Sub Status | Order Type | Customer Name | Created By | Created At |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## PASS SO Buy Part Type

1. Access the **Sales Order Management > PASS**
2. Click **New Sales Order** button
3. Fill in the required fields, here are the details:

### Account Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Sales Order Type | Dropdown | Buy Part | - | YES |
| Account Name | Text (Read-only) | Auto-populated from logged-in user account | - | NO |
| Order Date | Date Picker | Date of order creation | - | YES |
| Order Priority | Dropdown | Planned, Normal, Urgent | - | YES |
| Delivery Method | Dropdown | Delivery or Pickup | - | YES |
| Delivery Courier | Dropdown | Courier selection for delivery | - | NO |
| Console Shipment | Checkbox | Option to flag as console shipment | - | NO |
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
| Name Account | Text (read-only) | Auto-filled from selected Service Territory | - | YES |
| Model | Dropdown | List model are shown from system inventory | Default : Model from Sales Order | YES |
| Part Number | Dropdown | List Part Number are shown based on Model selection | - | YES |
| Part Description | Text (read-only) | Auto-filled based on selected Part Number and Model | - | YES |

4. Click **Search** button
5. Verify **Request Part** table is appear, here are the header table data :

| Add | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

6. Select **Non Local Part** by clicking **Add** from the table
    - **Sales Order Buy Part Type** ONLY shown **Non Local Part** from **GDN Only**
    - Can select multiple part
7. Click **Add Part** button
8. **Selected Part Request** is appear, here are the detail header table data :

| ASC Buy | Requested Quantity | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Total Price Request | Total Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

9. Input **Requested Quantity** and Click **Request Part & Save** button
10. **Confirmation Popup** appear with **Request Part Detail** and Click **Request Part** button
11. Verify **Request Part** is appear on the **Part Request** section with status **Waiting for Submit**, also sub status is **Waiting for Submit**

### Send SO Request

1. Click **Send SO Request** button
2. Verify popup confirmation appear and select **Progress** button
3. Verify **SO** status is change to **In Progress** and sub status **Part Not Available** also **Part** status is change to **Waiting Confirmation**
    - Request Part from **Non Local** appear on **Sparepart Management - Sparepart Request > Tab Sales Order**

### Receive Part from GDN

1. User GDN navigate to **Approval Management > Sales Order** section
2. Verify **Part Request** from **Non Local** appear on the list
3. Click **Action** button and select **Approved**
4. Verify Popup Confirmation appear and select **Approve** button
    - **Part** status change to **Approved by GDN**
    - Button **Request CPC** and **Process Order** is active
5. Select **Process Order**
    - **Available Stock** decreased and stock change to **Reserved Quantity** based on quantity inputted
    - If **Cancelled**, **Available Stock** increase and **Reserved Quantity** return to 0

#### Process Order by GDN

1. User GDN navigate to **Sales Order > GDN** and open tab **Processing Part**
2. Verify the **Process Order** from **Approval Management** appear on the list
3. Click **Action** 

### Generate SO Buy Part Invoice

1. Only CPC can **Generate Invoice** by their system (Invoice is outside from the system)

### SO Invoice Payment

1. Invoice payment is outside from the system at the moment