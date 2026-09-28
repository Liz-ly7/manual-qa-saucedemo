# Test Summary

## Overview

Manual black-box testing was performed on SauceDemo (Swag Labs), covering the main shopping workflow and selected exploratory testing scenarios.

The test scope included:

- Login
- Product inventory
- Product details
- Shopping cart
- Checkout
- Side menu and navigation
- Exploratory testing with special test users

---

## Scripted Test Execution Summary

A total of **38 test cases** were executed.

| Result | Count |
|---|---:|
| Pass | 36 |
| Failed / Requires clarification | 1 |
| Pending requirement clarification | 1 |
| Total | 38 |

Most scripted test cases behaved as expected.

Two cases could not be fully resolved because the expected behavior was not clearly defined:

- `TC-CHK-OVR-004` — The Cancel button returned the user to the shopping cart instead of the inventory page defined in the test case. The intended destination requires clarification.
- `TC-NAV-004` — The expected behavior of Reset App State was not defined, so the result could not be classified as Pass or Fail.

---

## Exploratory Testing Summary

Additional exploratory testing was performed using the special SauceDemo accounts:

- `problem_user`
- `error_user`
- `visual_user`
- `performance_glitch_user`

Exploratory testing identified **11 confirmed functional and visual defects**.

Examples included:

- Incorrect product images.
- Cart controls not functioning correctly.
- Products not being added from product details pages.
- Checkout input fields behaving incorrectly.
- Required checkout information not being validated correctly.
- Missing product information.
- Misaligned interface elements.

Detailed defect reports are documented in `06-defect-reports.md`.

---

## Additional Findings

Four findings require further clarification or defined acceptance criteria:

- Intended destination of the Checkout Cancel button.
- Expected behavior of Reset App State.
- ZIP / Postal Code validation rules.
- Acceptable application response-time thresholds.

These findings are documented in `05-test-findings.md`.

---

## Overall Result

The primary shopping workflow worked successfully when tested with `standard_user`.

However, exploratory testing with special test users revealed multiple reproducible functional and visual defects.

The testing also identified several areas where clearer requirements would be necessary before behavior could be confidently classified as correct or defective.

Further testing would be recommended after requirement clarification and after confirmed defects are fixed.
