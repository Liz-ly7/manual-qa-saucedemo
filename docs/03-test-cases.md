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

### TC-INV-001 — Verify product images on the inventory page

**Related Test Condition:** Product images correspond to the correct products.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.

**Test Data:**
- Account: `standard_user`
- Products: All six products displayed on the inventory page

**Steps:**
1. Review the image displayed for each product on the inventory page.
2. Verify that each image corresponds to the correct product.

**Expected Result:**
- Each product displays an image that corresponds to the correct product.

**Priority:** Medium

### TC-INV-002 — Verify product information on the inventory page

**Related Test Condition:** Product information is displayed correctly and matches the corresponding products.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.

**Test Data:**
- Account: `standard_user`
- Products: All six products displayed on the inventory page

**Steps:**
1. Review each product displayed on the inventory page.
2. Verify that each product displays a product name.
3. Verify that each product displays a description.
4. Verify that each product displays a price.

**Expected Result:**
- All six products display a name, description, and price.
- Product information is clearly associated with the corresponding product.

**Priority:** Medium

### TC-INV-003 — Add a product to the cart

**Related Test Condition:** Products can be added to the cart correctly.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.
- The shopping cart is empty.

**Test Data:**
- Account: `standard_user`
- Product: `Sauce Labs Backpack`

**Steps:**
1. Locate `Sauce Labs Backpack` on the inventory page.
2. Click the Add to cart button for the product.
3. Open the shopping cart.

**Expected Result:**
- The Add to cart button changes to Remove after the product is added.
- The cart badge shows `1`.
- `Sauce Labs Backpack` is displayed in the shopping cart.

**Priority:** High

### TC-INV-004 — Remove a product from the cart from the inventory page

**Related Test Condition:** Products can be removed from the cart correctly.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.
- `Sauce Labs Backpack` has been added to the shopping cart.

**Test Data:**
- Account: `standard_user`
- Product: `Sauce Labs Backpack`

**Steps:**
1. Locate `Sauce Labs Backpack` on the inventory page.
2. Click the Remove button for the product.
3. Open the shopping cart.

**Expected Result:**
- The Remove button changes back to Add to cart.
- The cart badge is updated correctly.
- `Sauce Labs Backpack` is no longer displayed in the shopping cart.

**Priority:** High

### TC-INV-005 — Product links navigate to the correct product details

**Related Test Condition:** Product links navigate to the correct product details.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.

**Test Data:**
- Account: `standard_user`
- Product: `Sauce Labs Backpack`

**Steps:**
1. Click the `Sauce Labs Backpack` product link.
2. Review the product details page.

**Expected Result:**
- The product details page for `Sauce Labs Backpack` opens.
- The displayed product name corresponds to the selected product.

**Priority:** Medium

### TC-INV-006 — Verify product sorting

**Related Test Condition:** Products are sorted correctly according to the selected sorting option.

**Precondition:**
- User is logged in as `standard_user`.
- User is on the SauceDemo inventory page.

**Test Data:**
- Account: `standard_user`
- Products: All six products displayed on the inventory page
- Sorting options:
  - Name (A to Z)
  - Name (Z to A)
  - Price (low to high)
  - Price (high to low)

**Steps:**
1. Locate the sorting dropdown on the inventory page.
2. Select `Name (A to Z)` and review the product order.
3. Select `Name (Z to A)` and review the product order.
4. Select `Price (low to high)` and review the product order.
5. Select `Price (high to low)` and review the product order.

**Expected Result:**
- `Name (A to Z)` sorts products alphabetically from A to Z.
- `Name (Z to A)` sorts products alphabetically from Z to A.
- `Price (low to high)` sorts products from the lowest price to the highest price.
- `Price (high to low)` sorts products from the highest price to the lowest price.

**Priority:** Medium
