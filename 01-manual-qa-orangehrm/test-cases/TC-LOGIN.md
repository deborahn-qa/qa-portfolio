# Test Cases — Login Module

**Module:** Authentication / Login
**Tester:** Deborah Nuñez Valencia
**Environment:** OrangeHRM Demo — https://opensource-demo.orangehrmlive.com/
**Techniques:** Equivalence Partitioning, Boundary Value Analysis, Negative Testing

---

## Test Cases

| TC ID | Title | Preconditions | Steps | Test Data | Expected Result | Status |
|---|---|---|---|---|---|---|
| TC-LOG-001 | Successful login with valid credentials | App is accessible | 1. Navigate to login page 2. Enter username 3. Enter password 4. Click Login | User: Admin / Pass: admin123 | User is redirected to Dashboard | ✅ Pass |
| TC-LOG-002 | Login with invalid username | App is accessible | 1. Enter incorrect username 2. Enter valid password 3. Click Login | User: wronguser / Pass: admin123 | Error message displayed: "Invalid credentials" | ✅ Pass |
| TC-LOG-003 | Login with invalid password | App is accessible | 1. Enter valid username 2. Enter incorrect password 3. Click Login | User: Admin / Pass: wrongpass | Error message displayed: "Invalid credentials" | ✅ Pass |
| TC-LOG-004 | Login with empty username field | App is accessible | 1. Leave username empty 2. Enter valid password 3. Click Login | User: (empty) / Pass: admin123 | Validation message: "Required" | ✅ Pass |
| TC-LOG-005 | Login with empty password field | App is accessible | 1. Enter valid username 2. Leave password empty 3. Click Login | User: Admin / Pass: (empty) | Validation message: "Required" | ✅ Pass |
| TC-LOG-006 | Login with both fields empty | App is accessible | 1. Leave both fields empty 2. Click Login | User: (empty) / Pass: (empty) | Both fields show "Required" validation | ✅ Pass |
| TC-LOG-007 | Password field masks characters | App is accessible | 1. Enter any value in password field 2. Observe character display | Pass: admin123 | Characters are masked (shown as dots) | ✅ Pass |
| TC-LOG-008 | Successful logout | User is logged in | 1. Click user avatar (top right) 2. Click Logout | — | User is redirected to login page, session ends | ⚠️ Bug → BUG-001 |

---

## Notes

- TC-LOG-008 revealed an intermittent session persistence issue — see BUG-001
- No CAPTCHA or lockout policy was observed after multiple failed attempts (potential security gap, logged as observation)
