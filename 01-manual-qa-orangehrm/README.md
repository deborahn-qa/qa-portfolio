# 01 — Manual QA Project: OrangeHRM

**Application under test:** [OrangeHRM Demo](https://opensource-demo.orangehrmlive.com/)
**Type:** Open-source Human Resource Management web application
**Scope:** Functional, exploratory, and regression testing of core HR modules

---

## 🎯 Objectives

- Demonstrate end-to-end manual QA skills within a simulated SDLC
- Design structured test cases based on business requirements
- Perform exploratory testing to uncover edge cases
- Document bugs with clear, reproducible steps
- Execute a regression checklist after bug fixes

---

## 📁 Project Structure

```
01-manual-qa-orangehrm/
├── test-plan.md                  ← Scope, strategy, entry/exit criteria
├── test-cases/
│   ├── TC-LOGIN.md               ← Login module test cases
│   ├── TC-EMPLOYEE.md            ← Employee management test cases
│   └── TC-LEAVE.md               ← Leave management test cases
├── bug-reports/
│   ├── BUG-001.md
│   ├── BUG-002.md
│   └── BUG-003.md
└── templates/
    ├── test-case-template.md
    └── bug-report-template.md
```

---

## 🔄 SDLC Approach

This project simulates a **Agile QA cycle**:

1. **Requirement Analysis** — Identified testable features from OrangeHRM modules
2. **Test Planning** — Defined scope, objectives, and exit criteria
3. **Test Design** — Created test cases using equivalence partitioning and boundary value analysis
4. **Test Execution** — Ran test cases manually and logged results
5. **Bug Reporting** — Documented defects with severity, priority, and reproduction steps
6. **Regression Testing** — Re-validated fixed areas using the regression checklist

---

## 🧪 Modules Tested

| Module | Test Cases | Bugs Found |
|---|---|---|
| Login | 8 | 1 |
| Employee Management | 10 | 1 |
| Leave Management | 8 | 1 |

---

## 📊 Test Metrics Summary

| Metric | Value |
|---|---|
| Total Test Cases | 26 |
| Passed | 22 |
| Failed | 3 |
| Blocked | 1 |
| Bugs Reported | 3 |
| Critical Bugs | 1 |

---

## 🛠️ Tools Used

- **Application:** OrangeHRM Live Demo
- **Documentation:** Markdown / GitHub
- **Bug tracking simulation:** Structured bug report format (Jira-style)
- **Test design techniques:** Equivalence Partitioning, Boundary Value Analysis, Exploratory Testing
