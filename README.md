# SauceDemo Manual QA Project

## Project Overview

This project is a manual QA testing project for **SauceDemo (Swag Labs)**.

The application was tested using a **manual black-box testing** approach, covering the main e-commerce workflow as well as exploratory testing with special test accounts.

The project includes test analysis, test case design, test execution, exploratory testing, defect reporting, and a final test summary.

---

## Test Scope

The following areas were tested:

- Login
- Product inventory
- Product details
- Shopping cart
- Checkout
- Side menu and navigation

Additional exploratory testing was performed using special SauceDemo accounts to investigate unusual functional, visual, and performance behavior.

---

## Test Approach

### Scripted Testing

Test conditions were identified for the main application features and converted into detailed test cases.

A total of **38 test cases** were executed.

| Result | Count |
|---|---:|
| Pass | 36 |
| Failed / Requires clarification | 1 |
| Pending requirement clarification | 1 |
| Total | 38 |

### Exploratory Testing

Exploratory testing was performed using:

- `problem_user`
- `error_user`
- `visual_user`
- `performance_glitch_user`

This testing identified **11 confirmed functional and visual defects**.

Additional observations involving unclear requirements or undefined acceptance criteria were documented separately as test findings.

---

## Key Findings

Examples of confirmed defects include:

- Incorrect product images.
- Products that cannot be removed from the cart from the inventory page.
- Products that cannot be added from a product details page.
- Checkout fields behaving incorrectly.
- Checkout proceeding when required information is missing.
- Missing product information.
- Misaligned interface elements.

The project also identified areas where clearer requirements are needed, including:

- Checkout Cancel button destination.
- Reset App State behavior.
- ZIP / Postal Code validation rules.
- Acceptable application response-time thresholds.

---

## Test Environment

- **Operating System:** Windows 10
- **Browser:** Google Chrome
- **Testing Type:** Manual Black-box Testing

---

## Project Structure

```text
manual-qa-saucedemo/
│
├── 01-product-overview.md
├── 02-test-analysis.md
├── 03-test-cases.md
├── 04-test-execution.md
├── 05-test-findings.md
├── 06-defect-reports.md
├── 07-test-summary.md
└── README.md
```

### Documentation

**01-product-overview.md**  
Initial application exploration, test environment, application areas, test users, risks, and requirement questions.

**02-test-analysis.md**  
Test conditions identified for each major feature.

**03-test-cases.md**  
Detailed manual test cases including preconditions, test data, steps, expected results, and priorities.

**04-test-execution.md**  
Actual execution results and Pass / Fail / Pending statuses.

**05-test-findings.md**  
Requirement gaps, exploratory testing observations, and findings requiring further clarification.

**06-defect-reports.md**  
Detailed reports for confirmed defects, including reproduction steps, expected and actual results, severity, and status.

**07-test-summary.md**  
Overall testing results, defect summary, unresolved findings, and final testing conclusions.

---

## Skills Demonstrated

This project demonstrates practical experience with:

- Manual black-box testing
- Test analysis
- Test condition identification
- Test case design
- Test execution
- Expected vs. actual result comparison
- Exploratory testing
- Defect identification
- Defect reporting
- Severity classification
- Requirement gap identification
- Test documentation
- Test summary reporting

---

## Notes

Some observed behaviors could not be classified as defects because the expected behavior or acceptance criteria were not clearly defined.

Rather than assuming the intended behavior, these cases were documented as requirement clarification items for further investigation.

This distinction was maintained throughout the project between:

- Confirmed product defects
- Test expectation mismatches
- Undefined requirements
- Performance observations without defined thresholds
