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

### TC-PD-001 — Verify product details and information consistency

**Related Test Condition:**
- The correct product details page opens for the selected product.
- Product information is consistent between the inventory page and the product details page.

**Test Data:**
- Product: `Sauce Labs Backpack`

**Steps:**
1. Click `Sauce Labs Backpack` on the inventory page.
2. Review the product details page.
3. Compare the displayed product information with the information on the inventory page.

**Expected Result:**
- The product details page for `Sauce Labs Backpack` opens.
- The product name, description, price, and image are consistent with the inventory page.

**Priority:** Medium

### TC-PD-002 — Add a product to the cart from the product details page

**Related Test Condition:**
- Products can be added to the cart from the product details page.

**Test Data:**
- Product: `Sauce Labs Backpack`

**Steps:**
1. Click `Sauce Labs Backpack` on the inventory page.
2. Click the Add to cart button on the product details page.

**Expected Result:**
- The product details page for `Sauce Labs Backpack` opens.
- The Add to cart button changes to Remove.
- The cart badge is updated correctly to show that the product has been added.

**Priority:** High

### TC-PD-003 — Remove a product from the cart from the product details page

**Related Test Condition:**
- Products can be removed from the cart from the product details page.

**Additional Precondition:**
- `Sauce Labs Backpack` has been added to the shopping cart.

**Test Data:**
- Product: `Sauce Labs Backpack`

**Steps:**
1. Open the product details page for `Sauce Labs Backpack`.
2. Click the Remove button.

**Expected Result:**
- The Remove button changes to Add to cart.
- The cart badge is updated correctly to show that the product has been removed.

**Priority:** High

### TC-PD-004 — Navigate back to the inventory page

**Related Test Condition:**
- The user can navigate back to the inventory page correctly.

**Test Data:**
- Product: `Sauce Labs Backpack`

**Steps:**
1. Click `Sauce Labs Backpack` on the inventory page to open the product details page.
2. Click the Back to products button.

**Expected Result:**
- The user is returned to the inventory page.
- The inventory page is displayed correctly.

**Priority:** Medium

## Feature 4: Shopping Cart

### Common Preconditions

- User is logged in as `standard_user`.

### TC-CART-001 — Verify products and product count in the shopping cart

**Related Test Conditions:**
- The cart displays the correct products that were added.
- The cart displays the correct number of added products.

**Additional Precondition:**
- The shopping cart is empty.

**Test Data:**
- Product 1: `Sauce Labs Backpack`
- Product 2: `Sauce Labs Bike Light`

**Steps:**
1. Add `Sauce Labs Backpack` to the cart.
2. Add `Sauce Labs Bike Light` to the cart.
3. Check the cart badge.
4. Open the shopping cart.

**Expected Result:**
- The cart badge displays `2`.
- The shopping cart contains exactly two products.
- `Sauce Labs Backpack` and `Sauce Labs Bike Light` are both displayed in the shopping cart.

**Priority:** High

### TC-CART-002 — Remove products from the shopping cart

**Related Test Condition:**
- Products can be removed from the cart correctly.

**Additional Precondition:**
- The shopping cart contains `Sauce Labs Backpack` and `Sauce Labs Bike Light`.

**Test Data:**
- Product 1: `Sauce Labs Backpack`
- Product 2: `Sauce Labs Bike Light`

**Steps:**
1. Open the shopping cart.
2. Remove `Sauce Labs Backpack`.
3. Check the cart contents and cart badge.
4. Remove `Sauce Labs Bike Light`.
5. Check the cart contents and cart badge again.

**Expected Result:**
- After `Sauce Labs Backpack` is removed, only `Sauce Labs Bike Light` remains in the cart.
- The cart badge displays `1`.
- After `Sauce Labs Bike Light` is removed, the shopping cart is empty.
- The cart badge is no longer displayed.

**Priority:** High

### TC-CART-003 — Continue shopping from the shopping cart

**Related Test Condition:**
- Continue Shopping navigates back to the inventory page correctly.

**Additional Precondition:**
- User is on the shopping cart page.

**Test Data:**
- N/A

**Steps:**
1. Click the Continue Shopping button.

**Expected Result:**
- The inventory page is displayed.

**Priority:** Medium

### TC-CART-004 — Proceed to checkout from the shopping cart

**Related Test Condition:**
- Checkout proceeds to the checkout information page correctly.

**Additional Precondition:**
- User is on the shopping cart page.

**Test Data:**
- N/A

**Steps:**
1. Click the Checkout button.

**Expected Result:**
- The checkout information page is displayed.

**Priority:** High

## Feature 5: Checkout

### Checkout Information

#### Common Preconditions

- User is logged in as `standard_user`.
- User has at least one product in the shopping cart.
- User is on the checkout information page.

### TC-CHK-INFO-001 — Continue checkout with valid required information

**Related Test Conditions:**
- Required checkout information must be provided before continuing.
- Checkout information fields accept user input correctly.
- Continue proceeds to the checkout overview when valid required information is provided.

**Test Data:**
- First Name: `Test`
- Last Name: `User`
- Postal Code: `10001`

**Steps:**
1. Enter the first name in the First Name field.
2. Enter the last name in the Last Name field.
3. Enter the postal code in the ZIP / Postal Code field.
4. Click the Continue button.

**Expected Result:**
- All three fields accept the entered data.
- The checkout overview page is displayed.

**Priority:** High

### TC-CHK-INFO-002 — Continue checkout with a blank first name

**Related Test Conditions:**
- Required checkout information must be provided before continuing.
- Missing required information is handled with an appropriate error message.

**Test Data:**
- First Name: `[blank]`
- Last Name: `User`
- Postal Code: `10001`

**Steps:**
1. Leave the First Name field blank.
2. Enter the last name in the Last Name field.
3. Enter the postal code in the ZIP / Postal Code field.
4. Click the Continue button.

**Expected Result:**
- Checkout does not proceed to the checkout overview page.
- An appropriate error message indicating that the first name is required is displayed.
- The user remains on the checkout information page.

**Priority:** Medium

### TC-CHK-INFO-003 — Continue checkout with a blank last name

**Related Test Conditions:**
- Required checkout information must be provided before continuing.
- Missing required information is handled with an appropriate error message.

**Test Data:**
- First Name: `Test`
- Last Name: `[blank]`
- Postal Code: `10001`

**Steps:**
1. Enter the first name in the First Name field.
2. Leave the Last Name field blank.
3. Enter the postal code in the ZIP / Postal Code field.
4. Click the Continue button.

**Expected Result:**
- Checkout does not proceed to the checkout overview page.
- An appropriate error message indicating that the last name is required is displayed.
- The user remains on the checkout information page.

**Priority:** Medium

### TC-CHK-INFO-004 — Continue checkout with a blank postal code

**Related Test Conditions:**
- Required checkout information must be provided before continuing.
- Missing required information is handled with an appropriate error message.

**Test Data:**
- First Name: `Test`
- Last Name: `User`
- Postal Code: `[blank]`

**Steps:**
1. Enter the first name in the First Name field.
2. Enter the last name in the Last Name field.
3. Leave the ZIP / Postal Code field blank.
4. Click the Continue button.

**Expected Result:**
- Checkout does not proceed to the checkout overview page.
- An appropriate error message indicating that the postal code is required is displayed.
- The user remains on the checkout information page.

**Priority:** Medium

### TC-CHK-INFO-005 — Continue checkout with all required fields blank

**Related Test Conditions:**
- Required checkout information must be provided before continuing.
- Missing required information is handled with an appropriate error message.

**Test Data:**
- First Name: `[blank]`
- Last Name: `[blank]`
- Postal Code: `[blank]`

**Steps:**
1. Leave the First Name field blank.
2. Leave the Last Name field blank.
3. Leave the ZIP / Postal Code field blank.
4. Click the Continue button.

**Expected Result:**
- Checkout does not proceed to the checkout overview page.
- An appropriate error message indicating that required checkout information is missing is displayed.
- The user remains on the checkout information page.

**Priority:** Medium

### TC-CHK-INFO-006 — Edit entered checkout information

**Related Test Condition:**
- Entered checkout information can be edited correctly.

**Test Data:**
- Initial First Name: `Test`
- Updated First Name: `Edited`
- Initial Last Name: `User`
- Updated Last Name: `Tester`
- Initial Postal Code: `10001`
- Updated Postal Code: `20002`

**Steps:**
1. Enter the initial first name, last name, and postal code.
2. Replace the First Name value with `Edited`.
3. Replace the Last Name value with `Tester`.
4. Replace the ZIP / Postal Code value with `20002`.
5. Check the values displayed in all three fields.
6. Click the Continue button.

**Expected Result:**
- Each field accepts the updated value.
- The updated values remain displayed correctly before continuing.
- The checkout overview page is displayed after clicking Continue.

**Priority:** Medium

### Checkout Overview

#### Common Preconditions

- User is logged in as `standard_user`.
- `Sauce Labs Backpack` and `Sauce Labs Bike Light` are in the shopping cart.
- User has entered valid required checkout information.
- User is on the checkout overview page.

### TC-CHK-OVR-001 — Verify order information and cart items

**Related Test Conditions:**
- Products in the shopping cart are carried over correctly to the checkout overview.
- The quantity of each product is displayed correctly.
- Payment information is displayed correctly and clearly.
- Shipping information is displayed correctly and clearly.

**Test Data:**
- N/A

**Steps:**
1. Review the products and quantities displayed on the checkout overview page.
2. Review the Payment Information section.
3. Review the Shipping Information section.

**Expected Result:**
- `Sauce Labs Backpack` and `Sauce Labs Bike Light` are displayed on the checkout overview page.
- The quantity of each product is displayed correctly.
- Payment information is displayed clearly.
- Shipping information is displayed clearly.

**Priority:** High

### TC-CHK-OVR-002 — Verify item total, tax, and total calculation

**Related Test Condition:**
- The total is calculated correctly from the item total and tax.

**Test Data:**
- N/A

**Steps:**
1. Review the prices of the products on the checkout overview page.
2. Calculate the sum of the product prices.
3. Compare the calculated sum with the displayed Item total.
4. Review the displayed Tax.
5. Calculate the Item total plus Tax.
6. Compare the calculated amount with the displayed Total.

**Expected Result:**
- The Item total equals the sum of the product prices.
- The Total equals the Item total plus Tax.

**Priority:** High

### TC-CHK-OVR-003 — Complete checkout using the Finish button

**Related Test Condition:**
- Finish proceeds to the checkout completion page correctly.

**Test Data:**
- N/A

**Steps:**
1. Click the Finish button.

**Expected Result:**
- The checkout completion page is displayed.

**Priority:** High

### TC-CHK-OVR-004 — Cancel checkout from the overview page

**Related Test Condition:**
- Cancel navigates to the intended destination correctly.

**Test Data:**
- N/A

**Steps:**
1. Click the Cancel button.

**Expected Result:**
- The inventory page is displayed.

**Priority:** Medium

### TC-CHK-CMP-001 — Verify checkout completion and cart state

**Related Test Conditions:**
- A clear order completion message is displayed.
- The cart is cleared after the order is completed.

**Additional Precondition:**
- The order has been successfully completed.
- User is on the checkout completion page.

**Test Data:**
- N/A

**Steps:**
1. Review the order completion message.
2. Check the shopping cart badge.
3. Open the shopping cart and review its contents.

**Expected Result:**
- A clear order completion message is displayed.
- The cart badge is not displayed.
- The shopping cart contains no products.

**Priority:** Medium

### TC-CHK-CMP-002 — Return to inventory using Back Home

**Related Test Condition:**
- Back Home returns the user to the inventory page correctly.

**Additional Precondition:**
- User is on the checkout completion page.

**Test Data:**
- N/A

**Steps:**
1. Click the Back Home button.

**Expected Result:**
- The inventory page is displayed.

**Priority:** Medium

### TC-NAV-001 — Open and close the side menu

**Related Test Condition:**
- The side menu can be opened and closed correctly.

**Test Data:**
- N/A

**Steps:**
1. Click the hamburger menu icon.
2. Click the Close menu button.

**Expected Result:**
- The side menu opens after clicking the hamburger menu icon.
- The side menu closes after clicking the Close menu button.

**Priority:** Medium

### TC-NAV-002 — Verify menu navigation links

**Related Test Condition:**
- Menu navigation links lead to the correct destinations.

**Test Data:**
- N/A

**Steps:**
1. Open the side menu.
2. Click All Items.
3. Review the displayed page.
4. Open the side menu again.
5. Click About.

**Expected Result:**
- All Items navigates to the inventory page.
- About navigates to the intended Sauce Labs page.

**Priority:** Medium

### TC-NAV-003 — Logout and verify session state after refresh

**Related Test Conditions:**
- Logout ends the user session correctly.
- The user remains logged out after refreshing the page.

**Test Data:**
- N/A

**Steps:**
1. Open the side menu.
2. Click Logout.
3. Refresh the page.

**Expected Result:**
- The user is returned to the login page after logging out.
- After the page is refreshed, the user remains logged out.
- The login page remains displayed.

**Priority:** High

### TC-NAV-004 — Reset application state

**Related Test Condition:**
- Reset App State resets the application state as intended.

**Test Data:**
- N/A

**Additional Precondition:**
- The application has a modified state, such as products added to the shopping cart.

**Steps:**
1. Open the side menu.
2. Click Reset App State.
3. Review the application state after the reset.

**Expected Result:**
- TBD — Expected reset behavior requires requirement clarification.

**Priority:** Medium

**Status:** Pending requirement clarification
