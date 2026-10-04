# E-commerce Manual QA Project

Manual black-box functional testing of https://automationexercise.com.
No requirements were published, so I explored the application, wrote requirements,
designed and executed test cases, and reported defects with screenshots.

## Summary

| Item | Count |
|---|---|
| Requirements written | [28 or 30] |
| Test cases executed | 62 |
| Passed | 53 |
| Failed | 9 |
| Bugs logged | 7 |

## Coverage

| Module | Requirements | Test cases | Pass | Fail |
|---|---|---|---|---|
| Login / Logout | REQ-06 to REQ-09 | 26 | 25 | 1 |
| Registration | REQ-01 to REQ-05, REQ-25, REQ-26 | 24 | 18 | 6 |
| Products and Search | REQ-11, REQ-12, REQ-15 | 3 | 3 | 0 |
| Reviews | REQ-16, REQ-27, REQ-28 | 3 | 1 | 2 |
| Cart | REQ-17 to REQ-20 | 3 | 3 | 0 |
| Checkout | REQ-21, REQ-22, REQ-24 | 3 | 3 | 0 |

**Not covered:** brand and category filters, order comment, API testing,
performance and security testing.

## Key defects found

| Bug ID | Title | Severity |
|---|---|---|
| BUG-001 | Login fails when email is entered in uppercase | Minor |
| BUG-002 | Name with only spaces accepted at first signup step | Trivial |
| BUG-003 | Duplicate account created with an existing email in uppercase | Major |
| BUG-004 | Mobile number field accepts letters | Minor |
| BUG-005 | Registration accepts passwords of any length and complexity | Major |
| BUG-006 | Guest user can submit a product review | Minor |
| BUG-007 | Submitted review is not displayed and no approval message is shown | Major |

Full details with steps and screenshots: [Bug report](04_Bug_Reports/bug_report.md)

## Approach

- Black-box functional testing with positive, negative and boundary cases
- Techniques: boundary value analysis, equivalence partitioning, error guessing
- Every test case is linked to a requirement ID
- Every failed test case is linked to a bug ID
- Environment: Windows, Firefox , Dummy data only.

## Assumptions

- No official requirements existed, so they were derived from the application
  and standard practice (for example password rules and case-insensitive email).

## Repository contents

| Folder | Contents |
|---|---|
| [01_Requirements](01_Requirements/requirements.md) | Requirements list |
| [02_Test_Plan](02_Test_Plan/test_plan.md) | Short test plan |
| [03_Test_Cases](03_Test_Cases/) | Test cases (Excel and PDF) |
| [04_Bug_Reports](04_Bug_Reports/bug_report.md) | Bug reports |
| [Test report folder name] | Test summary report |
| [Test Screenshots folder] |


## Tools

Google Sheets, GitHub, Chrome DevTools

## What I would do next

Automate the regression suite with Selenium or Playwright, and add API testing with Postman.
