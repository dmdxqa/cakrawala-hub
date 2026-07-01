# Cakrawala Hub

## Overview

Service Center Hub is a centralized operational utility engineered to optimize asset management workflows for service centers. It enables seamless creation of Maintenance/Repair Work Orders and Procurement Sales Orders while providing real-time stock tracking for comprehensive quality reporting.

The system serves as a single platform for service center staff, technicians, warehouse teams, and managers — covering the full lifecycle of a service request: from customer intake and work order assignment, through spare part procurement and stock management, to invoicing and reporting.

---

## What It Does

### Core Business Flow

```
Customer → Work Order → Technician Assignment → Spare Part Request
       → Stock Check → Sales Order (GDN/PASS) → Completion → Invoice/Report
```

1. A **customer** is registered and a **work order** is created for a maintenance or repair job.
2. The work order is **assigned to a tevchnician** via the schedule management module.
3. The technician may request **spare parts**, which triggers a stock check and procurement flow.
4. **Sales orders** are generated (GDN for goods delivery, PASS for procurement approvals) to fulfill the spare part need.
5. Upon completion, the work order feeds into **reporting** — including warranty invoice registers and raw data exports.

---

## Features

| Module | Description |
|---|---|
| Dashboard | Operational overview and key metrics at a glance |
| User Access Management | User and role-based access control |
| Work Order Management | Create and track maintenance/repair jobs |
| Customer Management | Customer records and history |
| Content Management | Manage informational or operational content |
| Claim Management | Handle warranty and service claims |
| Warranty & Asset Management | Track assets and their warranty status |
| Approval Management | Multi-step approval workflows |
| Sales Order Management | GDN and PASS order processing |
| Quotation Management | Generate and manage cost quotations |
| Sparepart Management | Stock checking, requests, and warehouse ops |
| Schedule Management | Calendar-based scheduling for technicians |
| Reporting | Invoice registers and raw data exports |

---

## Feature Details

### Dashboard
Provides a high-level operational snapshot — pending work orders, open claims, stock alerts, and technician availability — giving managers and staff an at-a-glance view of service center status.

---

### User Access Management

#### User Management
Manages user creation and access control, enabling administrators to onboard new users and assign appropriate roles for the Service Center Hub.

#### Roles Management
Manages role creation for access control, enabling new roles to be set up with granular permissions across modules.

---

### Work Order Management
The core operational module. Allows staff to create, assign, and track Work Orders (WO) for maintenance and repair jobs. Each WO captures the customer, asset, job description, assigned technician, status, and associated costs. Supports the full WO lifecycle from creation through completion and closure.

---

### Customer Management
Maintains a registry of customers including contact details, service history, and associated assets. Enables quick lookup during work order creation and claim processing.

---

### Content Management
Manages operational or informational content within the platform — such as announcements, service bulletins, or reference documents accessible to staff.

---

### Claim Management
Handles warranty and service claims submitted by customers. Tracks claim status, links claims to relevant work orders and assets, and routes them through the appropriate approval or resolution flow.

---

### Warranty & Asset Management

#### Asset Management
Tracks physical assets belonging to customers or the service center — including model, serial number, purchase date, and service history. Assets are linked to work orders and warranty records.

#### Warranty Management
Manages warranty records tied to assets. Tracks warranty coverage periods, claim eligibility, and expiry — feeding into the Invoice Register Warranty report.

---

### Approval Management
Provides a configurable multi-step approval workflow for work orders, quotations, sales orders, and procurement requests. Ensures the right stakeholders sign off before actions are executed.

---

### Sales Order Management

#### GDN (Goods Delivery Note)
Manages outbound goods delivery orders tied to spare part fulfillment for work orders. Tracks item quantities, delivery status, and links back to the originating work order or spare part request.

#### PASS (Procurement/Purchase Approval Sales Order)
Handles the procurement approval side — raising purchase requests for spare parts that are not in stock and routing them through the approval chain before fulfillment.

---

### Quotation Management
Enables staff to generate cost quotations for customers before work begins. Quotations capture labor, parts, and overhead costs and can be approved by the customer or internally before a work order is confirmed.

---

### Sparepart Management

#### Check Stock GDN
Real-time stock lookup for parts needed in GDN-based sales orders, ensuring delivery commitments are backed by available inventory.

#### Check Stock PASS
Stock availability check for PASS-based procurement flows — identifying shortfalls that require purchase orders.

#### Sparepart Request
Allows technicians or service staff to formally request spare parts for an active work order, initiating the stock check and procurement chain.

#### Warehouse
Manages the physical warehouse — item receipts, stock levels, bin locations, and movements. The source of truth for all stock-related queries across the platform.

---

### Schedule Management

#### Calendar List
A calendar view of all scheduled work orders, technician assignments, and service appointments, giving operations teams visibility over capacity and workload.

#### WO for Technician
Displays work orders assigned to each technician, filtered by date or status, to support daily task planning.

#### Technician Job List
A technician-facing view of their assigned jobs, including job details, priority, and required parts — used directly on the service floor.

---

### Reporting

#### Invoice Register Warranty
Generates structured invoice reports for warranty-covered jobs, used for reconciliation with warranty providers and internal accounting.

#### Raw Reporting Export
Exports raw operational data (work orders, sales orders, stock movements, claims) in bulk for analysis, compliance, or integration with external reporting tools.

### General Field Rule

#### Free Text/Text

- Maximum character is 500 characters