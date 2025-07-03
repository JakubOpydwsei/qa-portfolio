# QA Portfolio – Manual & Automated Testing

## About This Repository

This repository showcases my practical QA skills through **manual testing artifacts** (checklists, test cases, bug reports) and supports my knowledge of **automated end-to-end testing** using **Playwright** (available in [ManagMe project](https://github.com/JakubOpydwsei/ManagMe)).

---

## Structure

<pre>
qa-portfolio/
├── login-checklist.md      # Manual checklist for login functionality
├── login-test-cases.md     # Manual test cases
├── bug-login-button.md     # Example bug report
└── README.md               # This file
</pre>

---

## Manual Testing Scope

All tests are based on the login flow of a demo application.

- **Checklist**: Verifies UI elements, validation, error handling, and security practices.
- **Test Cases**: Seven test cases (TC-001 to TC-007) covering login behavior (positive & negative).
- **Bug Report**: Describes a UI logic bug (login button always enabled).

Each document was written in Markdown using a clear and structured format.

---

## Automated Testing (External)

Automated tests written in **Playwright** are available in my other repository: [ManagMe](https://github.com/JakubOpydwsei/ManagMe)

This includes:
- Login flow verification
- Full CRUD testing for Projects, Stories, and Tasks
- Tests connected to a working local backend and database

---

## CI/CD (Coming Soon)

Plans:
- Integrate GitHub Actions for running Playwright tests automatically on push/PR
- Display test results via badge or status

---

## Technologies Used

| Area | Tool / Language |
|---|---|
| Manual Testing | Markdown (`.md`) |
| Automated Testing | Playwright + TypeScript |
| Test Management | GitHub Projects / Issues |
| CI/CD (planned) | GitHub Actions |

---

## How to Use This Repository

Feel free to:
- Explore the Markdown files to see my test design process.
- Clone or fork for inspiration in your own QA projects.
- Use it as a reference for bug report and test case formatting.

---

## Status

This project is **work in progress**. More features (CI/CD, exploratory tests, responsive testing) coming soon.