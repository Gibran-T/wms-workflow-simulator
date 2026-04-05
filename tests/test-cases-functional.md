# Functional Test Cases
---

## 📊 Boundary Value Analysis — Inventory Adjustment Module

These test cases apply boundary value analysis (BVA) to the inventory quantity adjustment workflow.

### TC-INV-BVA-001 — Zero Quantity Boundary

| Field | Value |
|---|---|
| **Test Case ID** | TC-INV-BVA-001 |
| **Module** | Inventory Management |
| **Test Type** | Boundary Value Analysis |
| **Priority** | High |

**Steps:**
1. Open the inventory adjustment screen
2. Select an existing SKU with stock > 0
3. Enter quantity = `0`
4. Click Save

**Expected Result:** System accepts 0 as a valid quantity; stock is set to zero and a low-stock alert is triggered.

**Actual Result:** *(to be filled during execution)*

---

### TC-INV-BVA-002 — Minimum Valid Quantity

| Field | Value |
|---|---|
| **Test Case ID** | TC-INV-BVA-002 |
| **Module** | Inventory Management |
| **Test Type** | Boundary Value Analysis |
| **Priority** | High |

**Steps:**
1. Open the inventory adjustment screen
2. Select an existing SKU
3. Enter quantity = `1`
4. Click Save

**Expected Result:** System accepts 1 as the minimum valid quantity; no error is shown.

**Actual Result:** *(to be filled during execution)*

---

### TC-INV-BVA-003 — Maximum Capacity Boundary

| Field | Value |
|---|---|
| **Test Case ID** | TC-INV-BVA-003 |
| **Module** | Inventory Management |
| **Test Type** | Boundary Value Analysis |
| **Priority** | Medium |

**Steps:**
1. Open the inventory adjustment screen
2. Select a location with defined max capacity
3. Enter quantity = max capacity value
4. Click Save

**Expected Result:** System accepts the maximum capacity value without error.

**Actual Result:** *(to be filled during execution)*

---

### TC-INV-BVA-004 — Negative Quantity (Invalid — Must Be Blocked)

| Field | Value |
|---|---|
| **Test Case ID** | TC-INV-BVA-004 |
| **Module** | Inventory Management |
| **Test Type** | Negative / Boundary Value |
| **Priority** | Critical |

**Steps:**
1. Open the inventory adjustment screen
2. Select an existing SKU
3. Enter quantity = `-10`
4. Click Save

**Expected Result:** System blocks the entry and displays a validation error: "Quantity cannot be negative."

**Actual Result:** *(to be filled during execution)*

**Notes:** Negative inventory is a critical data integrity risk. If accepted, it creates phantom stock and corrupts financial reporting.
