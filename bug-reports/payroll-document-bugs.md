# Payroll Documents Bug Reports

## BUG-DOC-01

### Title
Default date range in payroll documents filter includes a future end date

### Description
The date filter allows selecting future dates even though payroll documents should only cover historical periods.

### Environment
- Employee application
- Device: Realme 9
- OS: Android 14

### Preconditions
- User is logged into the application.

### Steps to Reproduce
1. Go to the “Payroll Documents” tab.
2. Open the date filter.
3. Check the default date range.

### Expected Result
- The date range should include only historical data.
- The end date should not exceed the current date.
- The system should not allow selection of future dates.

### Actual Result
- The end date is set in the future (last day of the month).
- The system allows filtering using future date ranges.

### Severity
Medium


## BUG-DOC-02

### Title
Ability to select dates earlier than employment start date

### Description
The date filter does not enforce restrictions based on the user’s employment period. The system allows selecting dates outside the valid range.

### Environment
- Employee application
- Device: Realme 9
- OS: Android 14

### Preconditions
- User has a defined employment start date.
- User is logged into the application.

### Steps to Reproduce
1. Go to the “Payroll Documents” tab.
2. Open the date filter.
3. Set a start date earlier than the employment start date.
4. Apply the filter.

### Expected Result
- The system restricts date selection to the user’s employment period.

### Actual Result
- The system allows selecting dates earlier than the employment start date.
- The filter accepts out-of-range values.

### Severity
Medium


## BUG-DOC-03

### Title
Date filter resets after returning from document preview

### Description
The application does not preserve filter state after navigating to a document detail view and returning to the list, negatively affecting user experience.

### Environment
- Employee application
- Device: Realme 9
- OS: Android 14

### Preconditions
- User is logged into the application.

### Steps to Reproduce
1. Go to the “Payroll Documents” tab.
2. Set a custom date range in the filter.
3. Apply the filter.
4. Open any payroll document.
5. Return to the document list.

### Expected Result
- The previously set filter values remain unchanged.
- The list stays filtered accordingly.
- The user does not need to reapply the filter.

### Actual Result
- The date filter resets to default values.
- The document list returns to default state.
- The user must reconfigure the filter.

### Severity
Medium