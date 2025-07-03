# Login Page Test Checklist

## Test Scope / Purpose
Test the functionality and UI of the login page to ensure it works correctly and provides a smooth user experience.

## Test Environment
- Browser: Chrome (latest version)
- Device: Desktop (Windows)
- Network: Stable internet connection

## Test Checklist

### UI Elements
- [x] Login page loads correctly without errors – Page loaded without errors, no console warnings.
- [x] Logo is visible and correctly displayed – Logo visible also on mobile devices (tested via DevTools).
- [x] Email input field is visible and labeled properly.
- [x] Password input field is visible and labeled properly.
- [ ] Login button is visible and initially disabled if inputs are empty – Button is visible but **not disabled** when inputs are empty (unexpected behavior).
- [x] "Forgot password?" link is visible – Located at the bottom of the login form.

### Input Validation
- [x] Email field validation:
  - [x] Empty input shows required field message – Prompt alert at top-right corner of window.
  - [ ] Invalid email format shows error message – No specific validation for invalid format; treated as generic login failure.
- [x] Password field validation:
  - [x] Empty input shows required field message – Prompt alert at top-right corner of window.
  - [x] Invalid password shows error message – Generic alert: "Invalid email or password".
- [x] Valid email and password show no error message and trigger login flow.

### Login Button Behavior
- [ ] Login button is disabled when email or password is invalid or empty – Currently always enabled (unexpected).
- [ ] Login button is enabled only when both email and password are valid – Button is always enabled, regardless of input (unexpected behavior).

### Authentication Flow
- [x] Successful login with valid credentials redirects to the correct page/dashboard.
- [x] Unsuccessful login with invalid credentials shows clear error message – Generic message: "Invalid email or password".
- [x] No sensitive information (e.g. password) is exposed in URL or page source.

### Security & Privacy
- [x] Password input masks the characters (e.g., ****).
- [x] No console errors or warnings during login attempt.

### Responsiveness
- [x] Login page displays correctly on desktop screens.
- [x] Login page displays correctly on various mobile devices and screen sizes – Simulated using Chrome DevTools.

---

## Notes
- Bugs: Missing email format validation; login button always enabled.
- No screenshots were attached due to the absence of visual bugs.