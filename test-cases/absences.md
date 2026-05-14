# Absences Test Cases

## Preconditions
- The user is logged into the application.
- The user has available vacation days.
- The system operates according to HR configuration.
- The manager has permission to approve requests.

---

## TC-01: Submitting a leave request (valid data)

### Steps to Reproduce
1. Open the “Absences” module.
2. Create a new leave request.
3. Select the absence type (vacation leave).
4. Enter a valid date range.
5. Submit the request.

### Expected Result
- The request is successfully saved.
- The request appears in the absence list.
- The status is set to “Pending Approval”.


## TC-02: Submitting a request without required data

### Steps to Reproduce
1. Open the “Absences” module.
2. Create a new leave request.
3. Select the absence type (vacation leave).
4. Do not enter a date range.
5. Attempt to submit the request.

### Expected Result
- The system blocks saving the request.
- Validation messages are displayed.


## TC-03: Exceeding available vacation day limit

### Steps to Reproduce
1. Open the “Absences” module.
2. Create a new leave request.
3. Select the absence type (vacation leave).
4. Enter a date range exceeding available vacation balance.
5. Attempt to submit the request.

### Expected Result
- The system blocks the request submission.
- A message about exceeding vacation limit is displayed.
- The request is not saved.


## TC-04: Displaying absence list

### Steps to Reproduce
1. Open the “Absences” module.

### Expected Result
- The absence request list is visible.
- Types, dates, and statuses are displayed.


## TC-05: Correct request status

### Steps to Reproduce
1. Open the “Absences” module.
2. Submit a leave request.
3. Check request status.

### Expected Result
- The request status is set to “Pending”.


## TC-06: Vacation balance update

### Steps to Reproduce
1. Open the “Absences” module.
2. Check current vacation balance.
3. Submit a leave request.
4. Check balance again.

### Expected Result
- Used vacation days increase.
- Remaining vacation days decrease.
- Data is consistent.


## TC-07: Blocking past date selection

### Steps to Reproduce
1. Open the “Absences” module.
2. Start creating a leave request.
3. Attempt to select past dates.

### Expected Result
- The system blocks selection of past dates.


## TC-08: Excluding non-working days

### Steps to Reproduce
1. Open the “Absences” module.
2. Create a request including a weekend.

### Expected Result
- Non-working days are not counted according to system logic.


## TC-09: Date range across year boundary

### Steps to Reproduce
1. Open the “Absences” module.
2. Create a request covering December–January period.

### Expected Result
- The system correctly calculates number of days.
- No errors occur during year transition.


## TC-10: Editing a request before approval

### Steps to Reproduce
1. Open the “Absences” module.
2. Submit a leave request.
3. Open request details.
4. Attempt to edit the request.

### Expected Result
- The system does not allow editing approved requests.
- Fields are locked.
- The user can only cancel the request.


## TC-11: Status change after request approval

### Preconditions
- The user is logged in as an employee.
- A leave request has been submitted.
- The request has been approved by the manager.

### Steps to Reproduce
1. Open the “Absences” module.
2. Find the submitted request.
3. Check its status.

### Expected Result
- The request status changes to “Approved”.
- The status is visible to the user.


## TC-12: Vacation balance update after approval

### Preconditions
- The user is logged in as an employee.
- A leave request has been submitted and approved.

### Steps to Reproduce
1. Open the “Absences” module.
2. Check vacation balance.

### Expected Result
- Vacation balance is updated.
- Data is consistent within the system.