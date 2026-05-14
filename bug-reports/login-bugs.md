# Login Bug Reports

---

## BUG-LOG-01

### Title
Missing email field validation in login form

### Description
The system does not display a validation message when the email field is empty.

### Environment
- Employee application
- Device: Realme 9
- OS: Android 14

### Steps to Reproduce
1. Open the login screen.
2. Fill in the server address field.
3. Leave the email field empty.
4. Leave the password field empty.
5. Click “Login”.

### Expected Result
- Login is blocked.
- Validation messages appear for email and password fields.

### Actual Result
- Only password validation message is shown.
- No validation message for email field.

### Impact
Major

---

## BUG-LOG-02

### Title
Missing validation for empty login fields – server error returned

### Description
When all login fields are empty, the system returns a server error instead of validating inputs.

### Steps to Reproduce
1. Open the login screen.
2. Leave all fields empty (email, password, server address).
3. Click “Login”.

### Expected Result
- Login is blocked before request is sent.
- Validation messages appear for all fields.

### Actual Result
- “Server connection error” is displayed.
- No validation is shown.

### Impact
Major

---

## BUG-LOG-03

### Title
Login form always returns “server connection error” instead of validation

### Description
The system does not distinguish between validation errors and real connection issues.

### Steps to Reproduce

#### Scenario 1
1. Open login screen.
2. Leave email and server empty.
3. Enter password.
4. Click “Login”.

#### Scenario 2
1. Open login screen.
2. Enter email.
3. Leave password and server empty.
4. Click “Login”.

### Expected Result
- Validation errors are shown before request.

### Actual Result
- Same error appears every time: “server connection error”.

### Impact
Major