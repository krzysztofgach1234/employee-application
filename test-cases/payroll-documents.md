# Payroll Documents Test Cases

## Preconditions
- The user is logged into the application.

---

## TC-01: Displaying payroll documents list

### Steps to Reproduce
1. Navigate to “Payroll Documents”.

### Expected Result
- A list of documents is displayed.
- Each document contains correct data (date, type).
- Documents are assigned to the logged-in user.
- No UI errors are present.


## TC-02: Filtering documents by date range

### Steps to Reproduce
1. Navigate to “Payroll Documents”.
2. Open the date filter.
3. Set a date range (from–to).
4. Apply the filter.

### Expected Result
- Only documents within the selected date range are displayed.
- The list is refreshed after applying the filter.
- Results correctly match the selected range.


## TC-03: Default date range

### Steps to Reproduce
1. Navigate to “Payroll Documents”.
2. Open the date filter.

### Expected Result
- A valid default date range is set.
- The end date does not exceed the current date.


## TC-04: Validation of future dates

### Steps to Reproduce
1. Navigate to “Payroll Documents”.
2. Open the date filter.
3. Attempt to select a future date.

### Expected Result
- Future dates are disabled (greyed out).
- They cannot be selected.
- The system does not allow using them in filters.


## TC-05: Restriction to employment period

### Steps to Reproduce
1. Navigate to “Payroll Documents”.
2. Open the date filter.
3. Set a date earlier than employment start date.

### Expected Result
- Out-of-range dates are disabled (greyed out).
- The user cannot select them.
- The system prevents applying invalid ranges.


## TC-06: Filter persistence after document preview

### Steps to Reproduce
1. Navigate to “Payroll Documents”.
2. Open the date filter.
3. Set a custom date range.
4. Apply the filter.
5. Open any payroll document.
6. Return to the documents list.

### Expected Result
- Previously selected filter values are preserved.
- The document list remains filtered.
- The user does not need to reconfigure the filter.