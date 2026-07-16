# Sales Order GDN Workflow

## Overview

Outlines the positive flow for Sales Order GDN (Goods Delivery Note) creation, editing, and cancellation. This document serves as the primary reference for validating the order creation process, verifying order modifications while in Draft status, and testing order cancellation before deployment.

---

## Header Table Data

| No | ID Sales | WO Number | Status | Sub Status | Order Type | Customer Name | Created By | Created At |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

---

## Workflow

### Create New Sales Order

1. Access the **Sales Order Management > GDN**
2. Click **New Sales Order** button
3. Fill in the required fields, here are the details:

#### Account Information

| Field | Input Field | Detail | Rules | Required |
| --- | --- | --- | --- | --- |
| Sales Order Type | Dropdown | Walk In or Buy Part | - | YES |
| Account Name | Text (Read-only) | Auto-populated from logged-in user account | - | NO |
| Customer Name | Searchable Dropdown | Select from existing customer list | - | YES |
| Order Date | Date Picker | Date of order creation | - | YES |
| Order Priority | Dropdown | Planned, Normal, Urgent | - | YES |
| Delivery Method | Dropdown | Delivery or Pickup | - | YES |
| Delivery Courier | Dropdown | Courier selection for delivery | - | NO |
| Console Shipment | Checkbox | Option to flag as console shipment | - | NO |
| Parent SO Number | Searchable Dropdown | Link to parent Sales Order if applicable | - | NO |
| Billing Address | Text (Read-only) | Auto-populated from customer data | - | NO |
| Deposit | Currency Input | Deposit amount in Rp | Default: Rp 0 | NO |
| Description | Free Text | Order description or special notes | Max 500 characters | NO |

4. Click **Save** button and verify redirect to newly created sales order
5. Go back to **Sales Order Management > GDN** and Verify new Sales Order is created with **Draft** status and is listed in the Sales Order table

---

### View Sales Order Details

1. Access the **Sales Order Management > GDN**
2. Navigate to **Action** section
3. Click **Details** button (eye icon)
4. Verify **Sales Order Details** is displayed with all information

---

### Edit Sales Order

1. Access the **Sales Order Management > GDN**
2. Verify the Sales Order has **Draft** status
3. Navigate to **Action** section
4. Click **Edit** button (pencil icon)
5. Verify **Update Sales Order** form is opened
6. Make changes to any fields (e.g., Customer Name, Order Date, Delivery Method, Deposit amount, Description)
7. Click **Save** button
8. Verify the updated Sales Order is saved and reflected in the list

---

### Cancel Sales Order

1. Access the **Sales Order Management > GDN**
2. Verify the Sales Order has **Draft** status (Cancel button is only available in Draft status)
3. Navigate to **Action** section
4. Click **Cancel** button (cancel icon)
5. Verify the Sales Order status changes from **Draft** to **Close** or **Cancelled**
6. Verify the Sales Order is updated in the list with the new status

---

## Notes

- **Cancel Availability**: The Cancel action is only available when the Sales Order status is **Draft**
- **Status Flow**: Draft → (Edit possible) → (Cancel possible) OR → Other statuses (Approved, Close, Cancelled, etc.)
- **Sub Status Options**: The Sub Status field shows values like "Waiting For Submit", "Part Received", "Invoice Paid", "Part Available", etc. depending on the order progression
- **Role Access**: Refer to the **handover.md** file for role-based visibility rules for GDN and PASS orders
