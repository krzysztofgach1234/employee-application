# Absences Bug Reports

## BUG-ABS-01

### Title
Missing consideration of weekends and holidays when planning leave for the next year before January 1st

### Description
The system does not provide full calendar data (weekends and public holidays) for the new year when planning leave before January 1st. This may lead to incorrect calculation of vacation days during the transition period.

### Environment
- Employee application
- Device: Realme 9
- OS: Android 14

### Preconditions
- The user is logged into the application.

### Steps to Reproduce
1. Navigate to the “Absences” module.
2. Create a leave request.
3. In December, set a date range that includes January of the following year.
4. Submit the request.

### Expected Result
- The system includes weekends and public holidays for the next year.
- The calendar of non-working days is available for the entire selected date range.
- Vacation day calculation is consistent regardless of the month in which the request is created.

### Actual Result
- The system does not include weekends and public holidays for the new year when the request is created in December.
- Full calendar logic becomes available only after January 1st.
- The user must manually avoid non-working days.

### Severity
Critical