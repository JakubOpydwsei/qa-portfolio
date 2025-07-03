# Test Summary Report – Login Page

## Overview
Manual testing was conducted on the login page of the demo application (https://demo.opencart.com/) to verify the correctness of UI components, input validation, button behavior, and the basic authentication flow.

Testing was performed in the Chrome browser on Windows 10.

## Scope
The scope of testing included:
- UI component visibility and layout
- Input field validation for email and password
- Login button state handling
- Authentication flow (successful and failed login)
- Basic security (password masking, console errors)
- Responsiveness on various screen sizes

## Results Summary
A total of **7 test cases** were executed. The outcomes were:

- Passed: 4
- Passed with deviation: 2
- Failed: 1

### Test Case Results

| ID | Tesc Case Description |Status |
| --- | --- | --- |
| TC-001 | Empty email input | Pass |
| TC-002 | Invalid email format | Pass (deviation) |
| TC-003 | Empty password input | Pass (deviation) |
| TC-004 | Login button logic | Fail |
| TC-005 | Successful login | Pass |
| TC-006 | Unsuccessful login | Pass |
| TC-007 | Password masking | Pass |

## Issues Identified
- **BUG-001:** The login button remains active regardless of input values. This allows form submission even with empty fields, which could lead to confusion or security concerns. Reported in `bug-login-button.md`.

- Missing field-specific validation:
   - Invalid email format is not caught explicitly.
   - Error messages are too generic ("Invalid email or password").

## Conclusion
Most core functionality of the login page works as expected. However, there are several UX and validation issues that should be addressed:

- Add proper field-level validation for email and password.
- Fix button logic to prevent unnecessary form submissions.
- Improve clarity of error messages for better user feedback.

The login feature is **functionally usable**, but needs improvements before it can be considered **fully polished** or production-ready.
