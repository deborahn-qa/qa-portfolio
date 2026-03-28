# Test Plan — OrangeHRM Manual QA Project

**Version:** 1.0
**Author:** Deborah Nuñez Valencia
**Date:** 2025
**Status:** Active

---

## 1. Introduction

This test plan covers the manual QA testing of the OrangeHRM demo application, focusing on three core HR modules: Login, Employee Management, and Leave Management. The goal is to validate functional behavior against expected requirements and uncover defects before a hypothetical production release.

**Application URL:** https://opensource-demo.orangehrmlive.com/

---

## 2. Scope

### In Scope
- Login / Authentication module
- Employee Management (Add, Edit, Search, Delete)
- Leave Management (Apply, Approve, Reject)
- UI validation and error message accuracy
- Cross-browser testing: Chrome, Firefox

### Out of Scope
- Performance testing
- Security / penetration testing
- Mobile native app
- Admin configuration modules

---

## 3. Test Objectives

- Verify that all in-scope features work according to expected behavior
- Identify functional defects, UI inconsistencies, and usability issues
- Ensure critical user workflows complete without errors
- Validate input field boundaries and error handling

---

## 4. Test Strategy

| Test Type | Description |
|---|---|
| Functional Testing | Verify each feature works as expected |
| Exploratory Testing | Uncover edge cases without scripted steps |
| Negative Testing | Test invalid inputs, empty fields, boundary conditions |
| Regression Testing | Re-test after reported bugs are resolved |

**Test design techniques used:**
- Equivalence Partitioning
- Boundary Value Analysis
- Error Guessing

---

## 5. Entry Criteria

- Test environment is accessible (OrangeHRM demo is live)
- Test cases are reviewed and approved
- Test data is prepared (valid/invalid credentials, employee records)

---

## 6. Exit Criteria

- All planned test cases have been executed
- No open Critical or High severity bugs
- Test summary report is complete

---

## 7. Test Environment

| Item | Details |
|---|---|
| Application | OrangeHRM Demo (web) |
| URL | https://opensource-demo.orangehrmlive.com/ |
| Browser | Chrome 120+, Firefox 121+ |
| OS | Windows 10 / macOS |
| Test Data | Demo credentials: Admin / admin123 |

---

## 8. Roles & Responsibilities

| Role | Name |
|---|---|
| QA Tester | Deborah Nuñez Valencia |
| Test Design | Deborah Nuñez Valencia |
| Bug Reporting | Deborah Nuñez Valencia |

---

## 9. Risk & Mitigation

| Risk | Mitigation |
|---|---|
| Demo app data resets periodically | Re-create test data before each session |
| Demo app may have known bugs | Document and flag as pre-existing if applicable |
| Limited access to source code | Focus on black-box testing only |

---

## 10. Deliverables

- [ ] Test Plan (this document)
- [ ] Test Cases (per module)
- [ ] Bug Reports
- [ ] Regression Checklist
- [ ] Test Summary (metrics in README)
