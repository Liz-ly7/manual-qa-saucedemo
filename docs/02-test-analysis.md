# Test Analysis

## Feature 1: Login

### Test Conditions

- Login with valid credentials.
- Login with an invalid username.
- Login with an invalid password.
- Login with both username and password invalid.
- Login with a blank username.
- Login with a blank password.
- Login with both username and password blank.
- Login with a locked-out account.

## Feature 2: Product Inventory

### Test Conditions

- Product images correspond to the correct products.
- Product information is displayed correctly and matches the corresponding products.
- Products can be added to the cart correctly.
- Products can be removed from the cart correctly.
- Product links navigate to the correct product details.
- Products are sorted correctly according to the selected sorting option.

## Feature 3: Product Details

### Test Conditions

- The correct product details page opens for the selected product.
- Product information is consistent between the inventory page and the product details page.
- Products can be added to the cart from the product details page.
- Products can be removed from the cart from the product details page.
- The user can navigate back to the inventory page correctly.

## Feature 4: Shopping Cart

### Test Conditions

- The cart displays the correct products that were added.
- The cart displays the correct number of added products.
- Products can be removed from the cart correctly.
- Continue Shopping navigates back to the inventory page correctly.
- Checkout proceeds to the checkout information page correctly.

## Feature 5: Checkout

### Checkout Information

#### Test Conditions

- Required checkout information must be provided before continuing.
- Checkout information fields accept user input correctly.
- ZIP / Postal Code input is validated according to the expected format.
- Entered checkout information can be edited correctly.
- Missing required information is handled with an appropriate error message.
- Continue proceeds to the checkout overview when valid required information is provided.


### Check Overview

#### Test Conditions

- Products in the shopping cart are carried over correctly to the checkout overview.
- The quantity of each product is displayed correctly.
- Payment information is displayed correctly and clearly.
- Shipping information is displayed correctly and clearly.
- The total is calculated correctly from the item total and tax.
- Finish proceeds to the checkout completion page correctly.
- Cancel navigates to the intended destination correctly.

### Checkout Complete

#### Test Conditions

- A clear order completion message is displayed.
- The cart is cleared after the order is completed.
- Back Home returns the user to the inventory page correctly.

## Feature 6: Side Menu / Navigation

### Test Conditions

- The side menu can be opened and closed correctly.
- Menu navigation links lead to the correct destinations.
- Logout ends the user session correctly.
- The user remains logged out after refreshing the page.
- Reset App State resets the application state as intended.

## Requirement Clarifications

- What validation rules should apply to the ZIP / Postal Code field?
- What application state is expected to be reset by Reset App State?
