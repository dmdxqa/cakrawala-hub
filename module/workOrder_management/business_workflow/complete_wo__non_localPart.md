# Business Workflow

## GDN SC

### Completing a Work Order for Non Local Part

1. Open **Work Order Details** with status **New** and have **Assigned to Technician (service center)**
2. Change status to **In Progress** and **Save** the update
3. After changing the status, user able to add **Part Request** and **Charge**
    - For **Part Request** is optional to be inputted

#### Part Request Section

_Part Request Section_ is used for requesting and storing a part(s) from Local (service center stock itself) and Non local (CPC or other GDN SC).

1. Click **Part Request** button
2. **Part Request Popup** appear
3. Fill in the field, here are the details :

##### Part Request Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| WO Number | Text (read-only) | Auto-filled from selected Work Order | - | YES |
| Service Territory | Text (read-only) | Auto-filled from Work Order Service Territory | - | YES |
| Name Account | Text (read-only) | Auto-filled from selected customer | - | YES |
| Model | Dropdown | List model are shown from system inventory | Default : Model from Work Order | YES |
| Part Number | Dropdown | List Part Number are shown based on Model selection | - | YES |
| Part Description | Text (read-only) | Auto-filled based on selected Part Number and Model | - | YES |

4. Click **Search** button
5. Verify **Request Part** table is appear, here are the header table data :

| Add | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

6. Select **Non Local Part** by clicking **Add** from the table
    - Can select multiple part
7. Click **Add Part** button
8. **Selected Part Request** is appear, here are the detail header table data :

| ASC Buy | Requested Quantity | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Total Price Request | Total Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

9. Input **Requested Quantity** and Click **Request Part & Save** button
10. **Confirmation Popup** appear with **Request Part Detail** and Click **Request Part** button
11. Verify **Request Part** is appear on the **Part Request** section with status **Waiting for Submit**
    - an SO is auto-created for **Non Local** part being requested and it related to the WO

#### Sales Order Relation to Work Order

1. User navigate to auto-created **Sales Order** from Work Order
2. Open the **Sales Order** details
3. Verify **Part Request** is the same as on the Work Order Part Request and **Send SO Request** button is active
4. Click **Send SO Request** button
5. Verify **Part Request** status is change from **Waiting for Submit** to **Waiting for Confirmation**
    - **Part Request** status on **Work Order** also change
    - Navigate to **Sparepart Management** and open **Sparepart Request** for **Part Request** is listed
6. Verify **Receive** button is active and click **Receive** button
7. **Part Request** status is change to **Received**
    - **Reserved Quantity** is increase based total **Part Request**

---

12. User open **Request Part Detail** and navigate to **Consume** section
13. User input nominal on **Consume** field based on the total of **Quantity Requested**
    - If user **Consume** all of the part, there's **Return** part is 0
    - If user **Consume** some of the part, **Return** part is shown based on the remaining quantity and it will return to **Available Stock**
14. Click **Save** button
15. Verify **Request Part** status is change to **Consumed**

---

#### Charge Section

_Charge Section_ is used for charge for the services for the technician (ie. transport, labor, and service fee).

1. Click **New** on the **Charge** section
2. **Add Charge** popup appear
3. Fill in the field, here are the details :

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| WO Number | Text | Auto-filled from selected Work Order | - | NO |
| Charge Group | Text | Auto-filled from selected asset | - | NO |
| Product/Part Charge | Searchable Dropdown | List is appeared based on Charge Group (if Charge Group blank, it will shown all) | - | YES |
| Description | Text | Description for the charge | - | NO |

4. Click **Save** button
5. Verify **Charge** is appear on the **Charge** section

---

4. Change status to **Complete** and **Save** the update
5. Verify **Generate Invoice** is active when status is **Complete**
6. Click **Generate Invoice**
    - If both **Part Request** and **Charge** haven't inputted, it will prompt **Popup Warning**
7. After clicking **Generate Invoice**, verify it shown a **Invoice Preview**
    - When closing **Invoice Preview**, it will shown **Confirmation** popup
    - Invoice shown based on Part Request and Charge section
8. Click **Save Invoice & Print** to save the **Invoice** and verify redirect to **Printing** preview
    - User can opt out, from **Printing** preview
9. Verify **Invoice** is appear on the **Invoice** section and digital invoice is appear on the **File & Attachment** section
10. Verify WO status is change to **Close** with Sub status **Invoice (Unpaid)**
    - If WO have active Part Request, the status of that part is **Invoiced**
    - Same as SO, the status change to **Invoiced** also
11. User navigate to **Invoice Detail**
12. Click **Payment** button and select **New Payment** button
13. **Create Payment** popup appear, here are the details :

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Payment/Refund Method | Dropdown | Cash, Cheque, E-Wallet, E-Payment, Credit Card, Credit Term, QRIS | - | YES |
| Transaction Amount | Text | Auto-filled from the Generated Invoice total amount | - | NO |
| Cheque No | Text | - | - | NO |
| Remark | Text | - | - | NO |

14. Click **Save** button and verify **Payment** is appear on the **Payment Transaction** section
15. Verify WO status is change to **Close** with Sub status **Invoice (Paid)**

---

## PASS SC

### Completing a Work Order for Non Local Part

1. Open **Work Order Details** with status **New** and have **Assigned to Technician (service center)**
2. Change status to **In Progress** and **Save** the update
3. After changing the status, user able to add **Part Request** and **Charge**
    - For **Part Request** is optional to be inputted

#### Part Request Section

_Part Request Section_ is used for requesting and storing a part(s) from Local (service center stock itself) and Non local (CPC or other GDN SC).

1. Click **Part Request** button
2. **Part Request Popup** appear
3. Fill in the field, here are the details :

##### Part Request Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| WO Number | Text (read-only) | Auto-filled from selected Work Order | - | YES |
| Service Territory | Text (read-only) | Auto-filled from Work Order Service Territory | - | YES |
| Name Account | Text (read-only) | Auto-filled from selected customer | - | YES |
| Model | Dropdown | List model are shown from system inventory | Default : Model from Work Order | YES |
| Part Number | Dropdown | List Part Number are shown based on Model selection | - | YES |
| Part Description | Text (read-only) | Auto-filled based on selected Part Number and Model | - | YES |

4. Click **Search** button
5. Verify **Request Part** table is appear, here are the header table data :

| Add | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

6. Select **Local Part** by clicking **Add** from the table
    - Can select multiple part
7. Click **Add Part** button
8. **Selected Part Request** is appear, here are the detail header table data :

| ASC Buy | Requested Quantity | Service Territory | Warehouse | Source | Part Number | Description | Quantity Available | Unit Price | Tax | Unit Price with Tax | Total Price Request | Total Price with Tax | Discount |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

9. Input **Requested Quantity** and Click **Request Part & Save** button
10. **Confirmation Popup** appear with **Request Part Detail** and Click **Request Part** button
11. Verify **Request Part** is appear on the **Part Request** section with status **Waiting for Submit**
    - an SO is auto-created for **Non Local** part being requested and it related to the WO








    
12. User open **Request Part Detail** and navigate to **Consume** section
13. User input nominal on **Consume** field based on the total of **Quantity Requested**
    - If user **Consume** all of the part, there's **Return** part is 0
    - If user **Consume** some of the part, **Return** part is shown based on the remaining quantity and it will return to **Available Stock**
14. Click **Save** button
15. Verify **Request Part** status is change to **Consumed**

---

#### Charge Section

_Charge Section_ is used for charge for the services for the technician (ie. transport, labor, and service fee).

1. Click **New** on the **Charge** section
2. **Add Charge** popup appear
3. Fill in the field, here are the details :

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| WO Number | Text | Auto-filled from selected Work Order | - | NO |
| Charge Group | Text | Auto-filled from selected asset | - | NO |
| Product/Part Charge | Searchable Dropdown | List is appeared based on Charge Group (if Charge Group blank, it will shown all) | - | YES |
| Description | Text | Description for the charge | - | NO |

4. Click **Save** button
5. Verify **Charge** is appear on the **Charge** section

---

4. Change status to **Complete** and **Save** the update
5. Verify **Generate Invoice** is active when status is **Complete**
6. Click **Generate Invoice**
    - If both **Part Request** and **Charge** haven't inputted, it will prompt **Popup Warning**
7. After clicking **Generate Invoice**, verify it shown a **Invoice Preview**
    - When closing **Invoice Preview**, it will shown **Confirmation** popup
    - Invoice shown based on Part Request and Charge section
8. Click **Save Invoice & Print** to save the **Invoice** and verify redirect to **Printing** preview
    - User can opt out, from **Printing** preview
9. Verify **Invoice** is appear on the **Invoice** section and digital invoice is appear on the **File & Attachment** section
10. Verify WO status is change to **Close** with Sub status **Invoice (Unpaid)**
    - If WO have active Part Request, the status of that part is **Invoiced**
11. User navigate to **Invoice Detail**
12. Click **Payment** button and select **New Payment** button
13. **Create Payment** popup appear, here are the details :

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Payment/Refund Method | Dropdown | Cash, Cheque, E-Wallet, E-Payment, Credit Card, Credit Term, QRIS | - | YES |
| Transaction Amount | Text | Auto-filled from the Generated Invoice total amount | - | NO |
| Cheque No | Text | - | - | NO |
| Remark | Text | - | - | NO |

14. Click **Save** button and verify **Payment** is appear on the **Payment Transaction** section
15. Verify WO status is change to **Close** with Sub status **Invoice (Paid)**