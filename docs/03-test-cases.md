# Test Cases

## Feature 1: Login

### TC-LOGIN-001 — Login with valid credentials

**Related Test Condition:** Login with valid credentials.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `secret_sauce`

**Steps:**
1. Enter the valid username in the Username field.
2. Enter the valid password in the Password field.
3. Click the Login button.

**Expected Result:**
- Login succeeds.
- The user is redirected to the product inventory page.

**Priority:** High

### TC-LOGIN-002 — Login with an invalid username

**Related Test Condition:** Login with an invalid username.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `invalid_user`
- Password: `secret_sauce`

**Steps:**
1. Enter the invalid username in the Username field.
2. Enter the valid password in the Password field.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message is displayed.
- The user remains on the login page.

**Priority:** Medium

### TC-LOGIN-003 — Login with an invalid password

**Related Test Condition:** Login with an invalid password.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `abc123`

**Steps:**
1. Enter the valid username in the Username field.
2. Enter the invalid password in the Password field.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message is displayed.
- The user remains on the login page.

**Priority:** Medium

### TC-LOGIN-004 — Login with a blank username

**Related Test Condition:** Login with a blank username.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `[blank]`
- Password: `secret_sauce`

**Steps:**
1. Leave the Username field blank.
2. Enter the valid password in the Password field.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message indicating that the username is required is displayed.
- The user remains on the login page.

**Priority:** Medium

### TC-LOGIN-005 — Login with a blank password

**Related Test Condition:** Login with a blank password.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `standard_user`
- Password: `[blank]`

**Steps:**
1. Enter the valid username in the Username field.
2. Leave the Password field blank.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message indicating that the password is required is displayed.
- The user remains on the login page.

**Priority:** Medium

### TC-LOGIN-006 — Login with both username and password blank

**Related Test Condition:** Login with both username and password blank.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `[blank]`
- Password: `[blank]`

**Steps:**
1. Leave the Username field blank.
2. Leave the Password field blank.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message indicating that required login information is missing is displayed.
- The user remains on the login page.

**Priority:** Medium

### TC-LOGIN-007 — Login with a locked-out account

**Related Test Condition:** Login with a locked-out account.

**Precondition:**
- User is on the SauceDemo login page.

**Test Data:**
- Username: `locked_out_user`
- Password: `secret_sauce`

**Steps:**
1. Enter the locked-out username in the Username field.
2. Enter the valid password in the Password field.
3. Click the Login button.

**Expected Result:**
- Login is rejected.
- An appropriate error message indicating that the user is locked out is displayed.
- The user remains on the login page.

**Priority:** High
