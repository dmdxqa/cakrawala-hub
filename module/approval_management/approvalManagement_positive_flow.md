# Approval Management Workflow

## Overview

The Approval Management module enables tracking and processing of approval requests across multiple business processes. It provides a centralized hub for reviewing, approving, or rejecting submissions from various modules (Warranty, Work Order Claims, Sales Orders, Manual Inventory Requisitions, and Quotations). Approvers can view pending approvals, filter by status, and manage approval workflows based on their assigned roles and approval authorities.

---

## Header Table Data

### Warranty

| No | ID Warranty | Customer Name | Status | Verification Note | Approved By | Submitted At | Action |
| --- | --- | --- | --- | --- | --- | --- | --- |

---

### Work Order Claim

| No | WO Number | Submitted By | Customer Name | Remarks | Status | Action |
| --- | --- | --- | --- | --- | --- | --- |

---

### Sales Order

| No | ID Sales Order | Sales Order Number | Submitted By | Status | Verification Note | Approved By | Submitted At | Action |
| --- | --- | --- | --- | --- | --- | --- | --- |

---

### Manual Inventory

| No | MIR Number | Submitted By | Status | Verification Note | Approved By | Submitted At | Action |
| --- | --- | --- | --- | --- | --- | --- |

---

### Quotation

| No | Quotation Number | Submitted By | Customer Name | Status | Verification Note | Approved By | Submitted At | Action |
| --- | --- | --- | --- | --- | --- | --- | --- |

---

## Approval Status Reference

| Status | Description | Approver Role | Next Action |
| --- | --- | --- | --- |
| Waiting For GDN SC Approval | Awaiting approval from GDN Service Center | GDN SC | Approve/Reject |
| Waiting For GDN HO Approval | Awaiting approval from GDN Head Office | GDN HO | Approve/Reject |
| Waiting For PGI Approval | Awaiting approval from PGI (Parts and Service Provider) | PGI | Approve/Reject |
| Waiting For Approval | Generic pending approval status | Assigned Approver | Approve/Reject |
| Approved By GDN SC | Approved by GDN Service Center | - | View/Close |
| Approved By GDN HO | Approved by GDN Head Office | - | View/Close |
| Approved By PGI | Approved by PGI (Parts and Service Provider) | - | View/Close |

---

## Workflow

### Access Approval Management

1. Navigate to **Approval Management** menu from the sidebar
2. Verify the module opens with 5 main tabs: **Warranty**, **Work Order Claim**, **Sales Order**, **Manual Inventory**, and **Quotation**
3. System displays default tab based on user's recent access or permission level
4. Verify **Search** and **Filter** buttons are available for filtering approval requests

---

### View Pending Approvals

#### Warranty Approvals

1. Navigate to **Approval Management** → **Warranty** tab
2. Verify the list displays all warranty approval requests with the following columns:
   - **ID Warranty** — Unique warranty identifier
   - **Customer Name** — Customer submitting the warranty claim
   - **Status** — Current approval status (e.g., "Waiting For GDN SC Approval")
   - **Verification Note** — Any notes or remarks from verification process
   - **Approved By** — Name of approver (if already approved)
   - **Submitted At** — Date and time warranty was submitted
   - **Action** — Click button to view/manage approval
3. Verify pagination controls show total number of records (e.g., "354 pages")
4. Default page size is 10 records per page

#### Work Order Claim Approvals

1. Navigate to **Approval Management** → **Work Order Claim** tab
2. Verify the list displays all work order claim approval requests with the following columns:
   - **WO Number** — Work order number linked to claim
   - **Submitted By** — Employee/department that submitted the claim
   - **Customer Name** — Associated customer name
   - **Remarks** — Additional remarks or notes for approval
   - **Status** — Current approval status (e.g., "Waiting For GDN SC Approval" or "Waiting For PGI Approval")
   - **Action** — Click button to view/manage approval
3. Verify pagination shows total records (e.g., "772 pages")

#### Sales Order Approvals _(PASS - Buy Part Workflow)_

1. Navigate to **Approval Management** → **Sales Order** tab
2. Verify the list displays all sales order approval requests from the **PASS (Procurement/Purchase Approval Sales Order)** workflow
3. Note: These approvals originate from **Sales Order Management > PASS** module when a Buy Part sales order is submitted
4. Verify the list displays the following columns:
   - **ID Sales Order** — Auto-generated sales order ID
   - **Sales Order Number** — Sales order reference number (e.g., "PGI-SO-2607343997")
   - **Submitted By** — Sales department or submitting entity
   - **Status** — Current approval status (typically "Waiting For GDN SC Approval")
   - **Verification Note** — Verification notes or comments
   - **Approved By** — Approver name (if already approved; shows "-" if pending)
   - **Submitted At** — Date and time order was submitted
   - **Action** — Click button to view/manage approval
5. Verify pagination shows total records (e.g., "491 pages")

#### Manual Inventory Requisition (MIR) Approvals

1. Navigate to **Approval Management** → **Manual Inventory** tab
2. Verify the list displays all MIR approval requests with the following columns:
   - **MIR Number** — Manual Inventory Requisition unique identifier
   - **Submitted By** — Employee/department submitting the requisition
   - **Status** — Current approval status (e.g., "Waiting For Approval" or "Approved By GDN HO")
   - **Verification Note** — Verification notes or comments
   - **Approved By** — Approver name (e.g., "Yeni Susanty"; shows "-" if pending)
   - **Submitted At** — Date and time requisition was submitted
   - **Action** — Click button to view/manage approval
3. Verify pagination shows total records (e.g., "54 pages")
4. Verify status colors: Yellow badge for "Waiting For Approval", Green badge for "Approved By GDN HO"

---

### Filter and Search Approvals

1. Navigate to **Approval Management** → Any approval type tab
2. Click **Search** icon (magnifying glass) to open search bar
3. Enter search term to filter by:
   - ID/Number (Warranty ID, WO Number, Sales Order Number, MIR Number)
   - Customer Name
   - Submitted By (submitting user/department)
4. Click **Filter** icon (funnel) to filter by specific criteria:
   - **Status** — Filter by approval status (e.g., "Waiting For GDN SC Approval")
   - **Approver Role** — Filter by approval authority (GDN SC, GDN HO, PGI)
   - **Date Range** — Filter by submission date
5. Verify filtered results update in real-time
6. Click **Reset** or clear filters to show all records

---

### View Approval Details

1. Navigate to **Approval Management** → Relevant approval type tab
2. Locate the approval request to review
3. Click **Action** button (icon) at the end of the row
4. Verify an **Approval Detail** modal/panel opens displaying:
   - **Item Information** — Summary details of the approval request (ID, Customer Name, Submitted By, Status, etc.)
   - **Verification Note** field — For adding approver comments or observations
   - **Approve** button — To approve the request
   - **Reject** button — To reject the request
   - **Detail** button — To view full item details in the related module
5. Verify the modal contains action buttons to manage the approval

### Open Full Item Details in Related Module

1. From the **Approval Detail** modal (opened via Action button)
2. Click **Detail** button to open the full item details
3. Verify the system navigates to the related item's detail page in the corresponding module:
   - **Warranty approval** → Navigates to Warranty detail page in **Warranty & Asset Management**
   - **Work Order Claim approval** → Navigates to Work Order detail page in **Work Order Management**
   - **Sales Order approval** → Navigates to Sales Order detail page in **Sales Order Management > PASS**
   - **Manual Inventory approval** → Navigates to MIR detail page in **Sparepart Management** or relevant inventory module
   - **Quotation approval** → Navigates to Quotation detail page in respective quotation module
4. Verify full item information is displayed in the related module
5. Verify **Back** button or navigation path returns to **Approval Management** list

---

### Approve an Approval Request

#### Approve Warranty



#### Approve Work Order Claim



#### Approve Sales Order (PASS - Buy Part)



#### Approve Manual Inventory Requisition (MIR)



---

### Reject an Approval Request



---

### Add Verification Notes During Approval

1. Navigate to **Approval Management** → Any approval type tab
2. Locate the approval request
3. Click **Action** button to open **Approval Detail** modal
4. Locate the **Verification Note** field in the modal
5. Click in the field to enable editing
6. Enter verification observations:
   - Compliance check results
   - Data validation findings
   - Special conditions or requirements
   - Follow-up actions needed
   - Questions or clarifications needed
7. Notes can be added before clicking **Approve** or **Reject**
8. _(Optional)_ Notes are automatically saved when approval/rejection is submitted
9. Verify notes appear with the approval action in the audit trail
10. Notes are preserved with the approval record for future reference

---

## Approval Authority Matrix

| Approval Type | Source | Approver Role | Permission Level | Status Label |
| --- | --- | --- | --- | --- |
| Warranty | Warranty & Asset Management | GDN SC | Service Center Level | Waiting For GDN SC Approval |
| Work Order Claim | Work Order Management | PGI / GDN SC | Both authorities can approve | Waiting For PGI Appro / Waiting For GDN SC App |
| Sales Order (Buy Part) | Sales Order Management > PASS | GDN SC | Service Center Level | Waiting For GDN SC Approval |
| Manual Inventory (MIR) | Sparepart Management | GDN HO / General Approver | Head Office Level | Waiting For Approval / Waiting For GDN HO Approval |
| Quotation | Quotation Module | TBD | In Development | - |

---

## Key Business Rules

1. **Single Approval Workflow** — Each approval request requires approval from the designated authority before proceeding
2. **Approval Status Tracking** — System tracks and displays approval status in real-time
3. **Approver Identification** — Approved By field identifies the specific user who approved the request
4. **Timestamp Recording** — All approval actions are timestamped for audit purposes
5. **Verification Notes** — Approvers can add notes/remarks to justify approval or rejection decisions
6. **Pending List** — Approvers see only pending items matching their approval authority
7. **No Approval Override** — Approvals cannot be modified once completed (typically)
8. **Rejection Workflow** — Rejected requests may be resubmitted after addressing feedback

---

## Notes

- Approval permissions are role-based; users only see approvals within their authority
- Rejected approvals can typically be resubmitted after corrections
- All approval actions are logged for audit trail purposes
- Status badge colors help quickly identify approval state: Yellow = Pending, Green = Approved, Red = Rejected
