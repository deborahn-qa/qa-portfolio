# Test Cases — Leave Management Module

**Module:** Leave Management
**Tester:** Deborah Nuñez Valencia
**Environment:** OrangeHRM Demo
**Techniques:** Functional Testing, Negative Testing, Exploratory Testing

---

## Test Cases

| TC ID | Title | Preconditions | Steps | Test Data | Expected Result | Status |
|---|---|---|---|---|---|---|
| TC-LVE-001 | Apply for leave with valid data | Logged in as employee | 1. Go to Leave > Apply 2. Select leave type 3. Select valid date range 4. Click Apply | Type: Annual / Dates: future range | Leave request submitted successfully, status shows "Pending Approval" | ✅ Pass |
| TC-LVE-002 | Apply for leave with past date | Logged in as employee | 1. Go to Leave > Apply 2. Select a past date as From date 3. Click Apply | From Date: yesterday | Validation error: past dates not allowed | ✅ Pass |
| TC-LVE-003 | Apply for leave with end date before start date | Logged in as employee | 1. Select To date earlier than From date 2. Click Apply | From: 2025-12-10 / To: 2025-12-05 | Error: "To date must be after From date" | ✅ Pass |
| TC-LVE-004 | Apply for leave with no leave type selected | Logged in as employee | 1. Leave Leave Type field empty 2. Fill dates 3. Click Apply | Type: (none) | Validation message: "Required" | ✅ Pass |
| TC-LVE-005 | Admin approves a pending leave request | Leave request is pending, logged in as Admin | 1. Go to Leave > Leave List 2. Find pending request 3. Click Approve | — | Leave status changes to "Approved" | ✅ Pass |
| TC-LVE-006 | Admin rejects a pending leave request | Leave request is pending, logged in as Admin | 1. Go to Leave > Leave List 2. Find pending request 3. Click Reject | — | Leave status changes to "Rejected" | ✅ Pass |
| TC-LVE-007 | View leave balance | Logged in as employee | 1. Go to Leave > My Leave Usage | — | Leave balances displayed per leave type | ✅ Pass |
| TC-LVE-008 | Apply for leave exceeding available balance | Logged in, leave balance is low | 1. Apply for more days than available balance | Days: balance + 5 | Warning or error indicating insufficient leave balance | ⚠️ Bug → BUG-003 |

---

## Notes

- TC-LVE-008: System allowed leave application exceeding balance without any warning — see BUG-003
- Leave module correctly reflects weekend days as non-working by default
