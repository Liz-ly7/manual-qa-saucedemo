# Test Findings

## Summary

During scripted test case execution, two cases required further investigation because the observed behavior could not be confidently classified as a product defect without clearer requirements.

No confirmed defects were identified during the scripted test case execution.

Additional exploratory testing with special test users identified 11 confirmed functional and visual defects. Detailed defect reports are documented separately in `06-defect-reports.md`.

Additional observations involving ZIP / Postal Code validation and application response time also require clearer requirements before they can be classified as defects.

---

## Exploratory Testing Summary

### problem_user

Exploratory testing with `problem_user` identified several reproducible functional defects:

- Incorrect product images are displayed on the inventory page.
- Products cannot be removed from the cart from the inventory page.
- Products cannot be added to the cart from the product details page.
- Entering a Last Name modifies the First Name value instead.

Detailed defect reports are documented separately in `06-defect-reports.md`.

### error_user

Exploratory testing with `error_user` identified several reproducible functional issues:

- Products cannot be removed from the cart from the inventory page.
- The product description is missing from the product details page.
- The Last Name field does not accept input during checkout.
- Checkout can proceed even when the Last Name field is blank.

Alphabetic input was also accepted in the ZIP / Postal Code field. Because the expected validation rules are not defined, this observation is documented separately as `F-003`.

Detailed confirmed defect reports are documented separately in `06-defect-reports.md`.

### visual_user

Exploratory testing with `visual_user` identified several reproducible visual defects:

- The image displayed for `Sauce Labs Backpack` does not correspond to the product.
- The Checkout button is visually misaligned.
- The shopping cart button is visually misaligned.
- The hamburger menu button is visually misaligned.

Detailed defect reports are documented separately in `06-defect-reports.md`.

### performance_glitch_user

Exploratory testing with `performance_glitch_user` showed noticeable response delays during several actions:

- Login took approximately 5 seconds.
- Opening a product details page showed no noticeable delay.
- Returning to the inventory page took approximately 5 seconds.
- Returning after completing checkout took approximately 3 seconds.

Because no response-time requirement or acceptable performance threshold is defined, these observations are documented as `F-004` rather than as a confirmed defect.

---

## F-001 — Cancel button destination differs from test expectation

**Related Test Case:** `TC-CHK-OVR-004`

**Area:** Checkout Overview

**Expected Result:**
- Clicking Cancel should return the user to the inventory page.

**Actual Result:**
- Clicking Cancel returned the user to the shopping cart page.

**Finding Type:** Requirement clarification / Test expectation mismatch

**Status:** Open — clarification required

**Analysis:**
- The observed behavior differs from the expected result defined in the test case.
- However, the original test condition only states that Cancel should navigate to the intended destination.
- The intended destination is not explicitly defined.
- Therefore, it cannot currently be determined whether the application behavior is defective or the test case expectation is incorrect.

**Next Action:**
- Confirm the intended destination of the Cancel button.
- Update the test case or raise a defect depending on the clarified requirement.

---

## F-002 — Reset App State behavior is unclear

**Related Test Case:** `TC-NAV-004`

**Area:** Side Menu / Navigation

**Expected Result:**
- Not defined. Requirement clarification was already pending.

**Actual Result:**
- No visible change was observed after clicking Reset App State.

**Finding Type:** Requirement clarification

**Status:** Open — clarification required

**Analysis:**
- The expected scope of Reset App State is not defined.
- It is unclear which application state should be reset.
- Because no expected behavior is available, the observed result cannot be classified as Pass or Fail.

**Next Action:**
- Clarify which application data or state Reset App State is expected to reset.
- Define the expected result and execute the test again.

---

## F-003 — ZIP / Postal Code accepts alphabetic input

**Related Area:** Checkout Information

**Account:** `error_user`

**Actual Result:**
- Alphabetic input was accepted in the ZIP / Postal Code field.
- No validation error was displayed.

**Finding Type:** Requirement clarification

**Status:** Open — clarification required

**Analysis:**
- The expected format and validation rules for ZIP / Postal Code are not defined.
- Therefore, accepting alphabetic input cannot currently be classified as a defect.

**Next Action:**
- Confirm the required ZIP / Postal Code format and validation rules.
- Define the expected result and retest.

---

## F-004 — Noticeable response delays for performance_glitch_user

**Account:** `performance_glitch_user`

**Finding Type:** Performance observation / Requirement clarification

**Status:** Open — performance requirement not defined

**Observed Behavior:**
- Login took approximately 5 seconds.
- Opening a product details page showed no noticeable delay.
- Returning to the inventory page took approximately 5 seconds.
- Returning after completing checkout took approximately 3 seconds.

**Analysis:**
- The account responds noticeably more slowly during several navigation actions.
- No response-time requirement or acceptable performance threshold is defined.
- Therefore, the observed delays cannot currently be classified as a confirmed performance defect.

**Next Action:**
- Define acceptable response-time criteria.
- Repeat the performance checks against the defined threshold.
