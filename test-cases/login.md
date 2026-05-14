# Login Test Cases

## TC-01: Successful login

### Steps to Reproduce
1. Open the login screen.
2. Enter a valid email address, password, and server address.
3. Click the “Login” button.

### Expected Result
1. The user is successfully logged in.
2. The application redirects the user to the main screen.


## TC-02: Login with incorrect password

### Steps to Reproduce
1. Open the login screen.
2. Enter a valid email address and server address.
3. Enter an incorrect password.
4. Click the “Login” button.

### Expected Result
1. The login attempt is rejected.
2. An error message about invalid login credentials is displayed.
3. The user remains on the login screen.


## TC-03: Empty login fields

### Steps to Reproduce
1. Open the login screen.
2. Leave the email, password, and server address fields empty.
3. Click the “Login” button.

### Expected Result
1. The system blocks the login attempt.
2. An error message about invalid login credentials is displayed.
3. The user remains on the login screen.


## TC-04: Password masking

### Steps to Reproduce
1. Open the login screen.
2. Enter a password in the “Password” field.

### Expected Result
1. The password is masked (••••••).
2. The password is not visible in plain text.


## TC-05: User logout

### Preconditions
- The user is logged in.

### Steps to Reproduce
1. Click the “Logout” button.

### Expected Result
1. The user is successfully logged out.
2. The application returns to the login screen.


## TC-06: Remember user settings

### Steps to Reproduce
1. Open the login screen.
2. Enter valid login credentials: email, password, and server address.
3. Select the “Remember settings” option.
4. Click the “Login” button.
5. Log out and reopen the application.

### Expected Result
1. The previously saved login data is automatically filled in after reopening the application, if the “Remember settings” option was selected.


## TC-07: Automatic logout after inactivity

### Steps to Reproduce
1. Open the login screen.
2. Log in using valid credentials.
3. Remain inactive for 6 minutes without any actions.

### Expected Result
1. The user is automatically logged out after the inactivity timeout period.
2. The application redirects the user to the login screen.
3. The session is terminated.