# Product Overview

## Test Object

Application: Swag Labs (SauceDemo)

Testing Type: Manual Black-box Testing

## Test Environment

OS:Windows 10
Browser: Google Chrome
Browser: Version 151.0.7922.138

## First-pass Observations

## Test Users

| User | Observed Behavior |
|---|---|
| standard_user | Basic shopping flow appears to work normally. |
| locked_out_user | Login is blocked with a message indicating that the user has been locked out. |
| problem_user | Product images are incorrect on the inventory page. Some products cannot be added to the cart. The Last Name field on the checkout page does not accept input. |
| performance_glitch_user | The application responds noticeably more slowly than with the standard user. |
| error_user | Similar functional issues to problem_user were observed. |
| visual_user | Multiple visual/layout issues were observed, including misaligned interface elements and an incorrect product image. |

### What can I do in this application?

- Log in using the provided credentials.
- Browse rpoducts.
- Add products to the shopping cart.
- Remove products from the shopping cart.
- Proceed through the checkout process.

### Main areas/pages I found

- Login page
- Product inventory page
- Product details page
- Shopping cart
- Checkout information page
- Checkout overview page
- Checkout completion page
- Side menu

### Questions / things I am not sure about

- Is each product intentionally limited to one unit per order?
- Is checkout intentionally designed without a full shipping address?
- What validation rules should apply to the ZIP / Postal Code field?
- Are the different test users intentionally designed to demonstrate different application behaviors?

### Things that look interesting or risky to test later

- Cart quantity and item handling.
- Checkout input validation.
- ZIP / postal code boundary and invalid inputs.
