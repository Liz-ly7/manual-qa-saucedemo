# Defect Reports

## BUG-001 — Incorrect product images displayed on inventory page

**Account:** `problem_user`

**Area:** Product Inventory

**Steps to Reproduce:**
1. Log in as `problem_user`.
2. Open the product inventory page.
3. Review the image displayed for each product.
4. Open a product details page and compare the image.

**Expected Result:**
- Each product should display the image corresponding to that product on the inventory page.

**Actual Result:**
- All products display images that do not correspond to the respective products on the inventory page.
- The correct product image is displayed after opening the product details page.

**Severity:** Medium

**Status:** Confirmed

---

## BUG-002 — Products cannot be removed from cart on inventory page

**Affected Accounts:** `problem_user`, `error_user`

**Area:** Product Inventory / Shopping Cart

**Steps to Reproduce:**
1. Log in using an affected account.
2. Add a product to the cart from the inventory page.
3. Click the Remove button on the inventory page.

**Expected Result:**
- The selected product should be removed from the shopping cart.
- The cart state and badge should update accordingly.

**Actual Result:**
- The product can be added to the cart.
- The product cannot be removed using the Remove button on the inventory page.
- The product can still be removed after opening the shopping cart.

**Severity:** Medium

**Status:** Confirmed

---

## BUG-003 — Product cannot be added to cart from product details page

**Account:** `problem_user`

**Area:** Product Details

**Steps to Reproduce:**
1. Log in as `problem_user`.
2. Open a product details page.
3. Click the Add to cart button.

**Expected Result:**
- The product should be added to the shopping cart.
- The cart badge should update accordingly.

**Actual Result:**
- The product is not added to the shopping cart from the product details page.

**Severity:** Medium

**Status:** Confirmed

---

## BUG-004 — Entering Last Name modifies First Name value

**Account:** `problem_user`

**Area:** Checkout Information

**Steps to Reproduce:**
1. Log in as `problem_user`.
2. Add a product to the shopping cart.
3. Proceed to the checkout information page.
4. Enter a value in the First Name field.
5. Attempt to enter a value in the Last Name field.

**Expected Result:**
- The Last Name field should accept the entered value.
- The First Name field should remain unchanged.

**Actual Result:**
- The Last Name field does not accept the input correctly.
- Typing in the Last Name field modifies the value in the First Name field instead.

**Severity:** High

**Status:** Confirmed

---

## BUG-005 — Product description is missing from product details page

**Account:** `error_user`

**Area:** Product Details

**Steps to Reproduce:**
1. Log in as `error_user`.
2. Open a product from the inventory page.
3. Review the information displayed on the product details page.

**Expected Result:**
- The product details page should display the product name, description, price, and image.

**Actual Result:**
- The product description is not displayed on the product details page.

**Severity:** Medium

**Status:** Confirmed

---

## BUG-006 — Last Name field does not accept input during checkout

**Account:** `error_user`

**Area:** Checkout Information

**Steps to Reproduce:**
1. Log in as `error_user`.
2. Add a product to the shopping cart.
3. Proceed to the checkout information page.
4. Attempt to enter a value in the Last Name field.

**Expected Result:**
- The Last Name field should accept the entered value.

**Actual Result:**
- The Last Name field does not accept input.

**Severity:** High

**Status:** Confirmed

---

## BUG-007 — Checkout proceeds when Last Name is blank

**Account:** `error_user`

**Area:** Checkout Information

**Steps to Reproduce:**
1. Log in as `error_user`.
2. Add a product to the shopping cart.
3. Proceed to the checkout information page.
4. Enter a valid First Name and ZIP / Postal Code.
5. Leave the Last Name field blank.
6. Click Continue.

**Expected Result:**
- Checkout should not proceed.
- An error message should indicate that Last Name is required.

**Actual Result:**
- Checkout proceeds to the checkout overview page even though the Last Name field is blank.

**Severity:** High

**Status:** Confirmed

---

## BUG-008 — Incorrect image displayed for Sauce Labs Backpack

**Account:** `visual_user`

**Area:** Product Inventory

**Steps to Reproduce:**
1. Log in as `visual_user`.
2. Locate `Sauce Labs Backpack` on the inventory page.
3. Review the displayed product image.

**Expected Result:**
- The displayed image should correspond to `Sauce Labs Backpack`.

**Actual Result:**
- The image displayed for `Sauce Labs Backpack` does not correspond to the product.

**Severity:** Medium

**Status:** Confirmed

---

## BUG-009 — Checkout button is visually misaligned

**Account:** `visual_user`

**Area:** Shopping Cart

**Steps to Reproduce:**
1. Log in as `visual_user`.
2. Open the shopping cart.
3. Review the position of the Checkout button.

**Expected Result:**
- The Checkout button should be positioned correctly according to the page layout.

**Actual Result:**
- The Checkout button is visibly positioned away from its expected location.

**Severity:** Low

**Status:** Confirmed

---

## BUG-010 — Shopping cart button is visually misaligned

**Account:** `visual_user`

**Area:** Navigation / Header

**Steps to Reproduce:**
1. Log in as `visual_user`.
2. Review the shopping cart button position.

**Expected Result:**
- The shopping cart button should be aligned correctly within the page header.

**Actual Result:**
- The shopping cart button is visibly misaligned.

**Severity:** Low

**Status:** Confirmed

---

## BUG-011 — Menu button is visually misaligned

**Account:** `visual_user`

**Area:** Navigation / Header

**Steps to Reproduce:**
1. Log in as `visual_user`.
2. Review the hamburger menu button.

**Expected Result:**
- The menu button should be correctly aligned within the page header.

**Actual Result:**
- The hamburger menu icon is visibly misaligned.

**Severity:** Low

**Status:** Confirmed
