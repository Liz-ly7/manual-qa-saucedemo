# Test Findings

## Summary

During test execution, two cases required further investigation because the observed behavior could not be confidently classified as a product defect without clearer requirements.

No confirmed defects were identified during the executed test cases.

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

## Exploratory Testing — problem_user

Exploratory testing with `problem_user` identified four reproducible functional defects:

- Incorrect product images are displayed on the inventory page.
- Products cannot be removed from the cart from the inventory page.
- Products cannot be added to the cart from the product details page.
- Entering a Last Name modifies the First Name value instead.

Detailed defect reports are documented separately in `06-defect-reports.md`.
- The expected scope of Reset App State is not defined.
- It is unclear which application state should be reset.
- Because no expected behavior is available, the observed result cannot be classified as Pass or Fail.

**Next Action:**
- Clarify which application data or state Reset App State is expected to reset.
- Define the expected result and execute the test again.

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
