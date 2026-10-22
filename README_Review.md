# v168 Consolidated Staging Review

This package combines the latest user-tested staging candidates without modifying their HTML. It is NOT certified as browser-tested or production-ready.

## File selection

- `index.html` ← `LAHD_v162_Index_Isolation/index.html` (158,631 bytes)
- `borrower-portal.html` ← `LAHD_v166_1_Role_Handoff_Candidate/borrower-portal.html` (178,394 bytes)
- `staff-dashboard.html` ← `LAHD_v164_1_Staff_Dashboard_Style_Recovery/staff-dashboard.html` (12,618 bytes)
- `loan-portfolio-transaction-form.html` ← `LAHD_v165_3_Transaction_Only_Candidate/loan-portfolio-transaction-form.html` (182,196 bytes)
- `reserve-withdrawal-form.html` ← `LAHD_v166_Reserve_Form_Candidate/reserve-withdrawal-form.html` (155,598 bytes)
- `lp-transaction-detail.html` ← `LAHD_v167_Staff_Detail_Isolation_Candidates/lp-transaction-detail.html` (318,945 bytes)
- `reserve-withdrawal-detail.html` ← `LAHD_v167_Staff_Detail_Isolation_Candidates/reserve-withdrawal-detail.html` (327,896 bytes)

## Static audit

- **index.html**: 2 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **borrower-portal.html**: 15 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **staff-dashboard.html**: 1 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **loan-portfolio-transaction-form.html**: 8 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **reserve-withdrawal-form.html**: 4 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **lp-transaction-detail.html**: 39 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.
- **reserve-withdrawal-detail.html**: 40 inline scripts; 0 JavaScript syntax errors; 0 unresolved local references; 0 duplicate ID names.

## Known limitations
- User role switching after returning to the dashboard can retain the prior user role. Start a fresh sign-in session when testing a different role.
- Staff editing of submitted fields was not present in v160 and remains out of scope.
- Final end-to-end interaction, visual, browser storage, and GitHub Pages navigation tests must be performed in staging before production deployment.

## Suggested regression walkthrough
1. Sign in separately as Primary, Affiliated, Basic; check role-specific loan association in both forms.
2. Open Loan Portfolio Transaction, select types, review conditional ownership sections and document uploads; navigate back.
3. Open Reserve Withdrawal, test fund, invoice/bid entries, document controls, and draft/navigation.
4. Open Staff Dashboard and both detail pages; test review steps, Documents, Activity Log, Action Menu, and return navigation.
5. Repeat after a fresh browser session; verify GitHub Pages URL case and relative links.
6. Keep production v160 unchanged until checks pass.
