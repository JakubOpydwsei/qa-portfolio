# Login Page - Test Cases

## TC-001: Empty Email Input Shows Required Message
**Preconditions:** Login page is open.
**Steps:**
1. Leave the email input empty.
2. Click on the password input or try to submit the form.

**Expected result:**
- Required field message appears near the email input or as a prompt alert.

**Actual result:**
- After clicking submit, a prompt alert appeared at the top-right corner of the window stating "Warning: No match for E-Mail Address and/or Password.". No errors in the console.

**Status:** Pass
**Notes:** Behavior consistent with expectations, generic message.

---

## TC-002: Invalid Email Format Shows Error Message
**Preconditions:** Login page is open.
**Steps:**
1. Enter an invalid email format (e.g., "userexample.com" without '@').
2. Enter any password (valid or invalid).
3. Click the login button.

**Expected result:**
- Error message "Invalid email or password" is displayed.

**Actual result:**
- After submitting alert appeared at the top-right corner of the window stating "Invalid email or password".

**Status:** Pass with deviation
**Notes:** Generic message.

---

## TC-003: Empty Password Input Shows Required Message
**Preconditions:** Login page is open.
**Steps:**
1. Enter a valid email.
2. Leave the password input empty.
3. Try to submit the form.

**Expected result:**
- Required field message appears near the password input or as a prompt alert.

**Actual result:**
- After submitting alert appeared at the top-right corner of the window stating "Invalid email or password".

**Status:** Pass with deviation
**Notes:** Generic message.

---

## TC-004: Login Button Enabled/Disabled Behavior
**Preconditions:** Login page is open.
**Steps:**
1. Leave email and password inputs empty.
2. Observe the state of the login button.
3. Enter invalid email and/or password and observe the button.
4. Enter valid email and password and observe the button.

**Expected result:**
- Button is disabled when inputs are empty or invalid (expected behavior).
- Button is enabled only when both email and password have valid formats (expected).
- *Note: In tested app, button is always enabled (report as bug).*

**Actual result:**
- Button is always enabled

**Status:** Fail
**Notes:** Unexpected behavior

---

## TC-005: Successful Login Redirect
**Preconditions:** User has valid credentials. Login page is open.
**Steps:**
1. Enter valid email and password.
2. Click login button.

**Expected result:**
- User is redirected to the dashboard or profile page.
- No error message is shown.

**Actual result:**
- User was redirected to profile page without any error or warning message on window and console.

**Status:** Pass
**Notes:**

---

## TC-006: Unsuccessful Login Shows Error
**Preconditions:** Login page is open.
**Steps:**
1. Enter valid email but incorrect password (or vice versa).
2. Click login button.

**Expected result:**
- Error message "Invalid email or password" is displayed.
- User remains on the login page.

**Actual result:**
- After submitting alert appeared at the top-right corner of the window stating "Invalid email or password".

**Status:** Pass
**Notes:**

---

## TC-007: Password Masking
**Preconditions:** Login page is open.
**Steps:**
1. Enter any password into the password field.

**Expected result:**
- Password characters are masked (e.g., shown as ****).
- No plain text password visible on screen.

**Actual result:**
- Password characters are properly masked as '*'

**Status:** Pass
**Notes:**

---