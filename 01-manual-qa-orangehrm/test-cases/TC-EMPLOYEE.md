# Test Cases — Employee Management Module

**Module:** PIM (Personnel Information Management) — Employee Management
**Tester:** Deborah Nuñez Valencia
**Environment:** OrangeHRM Demo
**Techniques:** Functional Testing, Boundary Value Analysis, Exploratory Testing

---

## Test Cases

| TC ID | Title | Preconditions | Steps | Test Data | Expected Result | Status |
|---|---|---|---|---|---|---|
| TC-EMP-001 | Add new employee with required fields only | Logged in as Admin | 1. Go to PIM > Add Employee 2. Enter First Name, Last Name 3. Click Save | First: Jane / Last: Doe | Employee record is created and visible in employee list | ✅ Pass |
| TC-EMP-002 | Add new employee with all fields | Logged in as Admin | 1. Go to PIM > Add Employee 2. Fill all available fields 3. Click Save | Full profile data | All data is saved and displayed correctly on employee profile | ✅ Pass |
| TC-EMP-003 | Add employee with duplicate Employee ID | Logged in as Admin | 1. Go to PIM > Add Employee 2. Enter an existing Employee ID 3. Click Save | Existing ID: 0001 | Error message: "Employee Id already exists" | ✅ Pass |
| TC-EMP-004 | Add employee with empty First Name | Logged in as Admin | 1. Go to PIM > Add Employee 2. Leave First Name empty 3. Click Save | First: (empty) | Validation message: "Required" | ✅ Pass |
| TC-EMP-005 | Search employee by name | Employee records exist | 1. Go to PIM > Employee List 2. Enter name in search field 3. Click Search | Name: Jane Doe | Matching employee record(s) displayed | ✅ Pass |
| TC-EMP-006 | Search employee with no matching results | Employee list loaded | 1. Enter a non-existent name in search 2. Click Search | Name: XXXXXX | Message: "No Records Found" | ✅ Pass |
| TC-EMP-007 | Edit employee personal information | Employee record exists | 1. Open employee profile 2. Edit personal info fields 3. Click Save | Updated name/email | Changes are saved and reflected on the profile | ✅ Pass |
| TC-EMP-008 | Delete an employee record | Employee record exists | 1. Go to Employee List 2. Select employee checkbox 3. Click Delete 4. Confirm deletion | Any employee | Employee is removed from the list | ✅ Pass |
| TC-EMP-009 | First Name field max character boundary | Logged in as Admin | 1. Enter 100 characters in First Name field 2. Click Save | 100-char string | System accepts or shows max-length validation | ✅ Pass |
| TC-EMP-010 | Upload profile photo with invalid format | Employee profile open | 1. Click profile photo 2. Upload a .pdf file | File: document.pdf | Error: "File type not allowed" or similar | ⚠️ Bug → BUG-002 |

---

## Notes

- TC-EMP-010: System accepted a .pdf file upload without displaying an error, which is unintended behavior — see BUG-002
- Employee ID auto-generates correctly when left blank
