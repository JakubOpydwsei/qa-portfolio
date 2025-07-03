# BUG-001: Login button is always enabled regardless of input validity

**Related Test Case:** TC-004

**Environment:**
- Browser: Chrome (latest version)
- OS: Windows 10
- URL: https://demo.opencart.com/ (Login page)

**Description:**
The login button on the login page remains enabled at all times, even when email and/or password inputs are empty or invalid. According to best practices and expected behavior, the button should be disabled until both fields have valid inputs.

**Steps to Reproduce:**
1. Open the login page.
2. Leave both email and password inputs empty.
3. Observe the state of the login button (it is enabled).
4. Enter invalid email and/or password.
5. Observe the login button remains enabled.
6. Enter valid email and password.
7. Login button remains enabled.

**Expected Result:**
- Login button is disabled when email or password inputs are empty or invalid.
- Login button is enabled only when both email and password inputs are valid.

**Actual Result:**
- Login button is always enabled regardless of input validity.

**Severity:** Medium
**Priority:** Medium

**Impact:**
- Users may attempt to login with invalid credentials leading to frustration.
- Increased load on backend due to unnecessary login requests.
- Poor user experience and possible decrease in conversion rates.

**Additional Notes:**
This behavior deviates from expected standards and can confuse users, potentially leading to failed login attempts without proper input validation feedback.