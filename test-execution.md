# Test Execution Report – Employee Application

## General Information
- Environment: Android 14 (Realme 9)
- Test types: functional, negative, non-functional
- Scope: login, absences, payroll documents

---

## Test Results

### Module: Login

| TC ID | Description | Result | Related Bug |
|------|------|------|--------------|
| TC-01 | Successful login | PASS | - |
| TC-02 | Login with invalid password | PASS | - |
| TC-03 | Empty login fields | FAIL | BUG-LOG-01, BUG-LOG-02, BUG-LOG-03 |
| TC-04 | Password masking | PASS | - |
| TC-05 | User logout | PASS | - |
| TC-06 | Remember user settings | PASS | - |
| TC-07 | Automatic logout after inactivity | PASS | - |

---

### Module: Absences

| TC ID | Description | Result | Related Bug |
|------|------|------|--------------|
| TC-01 | Submit absence request (valid data) | PASS | - |
| TC-02 | Submitting a request without required data | PASS | - |
| TC-03 | Exceeding available vacation day limit | PASS | - |
| TC-04 | Displaying absence list | PASS | - |
| TC-05 | Correct request status | PASS | - |
| TC-06 | Vacation balance update | PASS | - |
| TC-07 | Blocking past date selection | PASS | - |
| TC-08 | Excluding non-working days | PASS | - |
| TC-09 | Date range across year boundary | FAIL | BUG-ABS-01 |
| TC-10 | Editing request before approval | PASS | - |
| TC-11 | Status change after request approval | PASS | - |
| TC-12 | Vacation balance update after approval | PASS | - |

---

### Module: Payroll Documents

| TC ID | Description | Result | Related Bug |
|------|------|------|--------------|
| TC-01 | Displaying payroll documents list | PASS | - |
| TC-02 | Filtering documents by date range | PASS | - |
| TC-03 | Default date range | FAIL | BUG-DOC-01 |
| TC-04 | Validation of future dates | FAIL | BUG-DOC-01 |
| TC-05 | Restriction to employment period | FAIL | BUG-DOC-02 |
| TC-06 | Filter persistence after document preview | FAIL | BUG-DOC-03 |

---

## Summary

- PASS: Most functional tests passed successfully
- FAIL: Issues mainly related to date filtering logic and input validation
- Critical issues: None
- Highest risk area: Payroll Documents module (date filtering and validation inconsistencies)