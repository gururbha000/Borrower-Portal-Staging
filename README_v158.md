# v158 — canonical page navigation and form display corrections

Upload ONLY `index.html`, `loan-portfolio-transaction-form.html`, and `reserve-withdrawal-form.html` to the TEST repository. Other pages remain untouched.

- index.html retains the existing onboarding/sign-in scripts, but combined request/dashboard areas are hidden when the home route is active. This is display isolation, not removal of all legacy code.
- LP and Reserve radio switches navigate to the corresponding standalone URL.
- Both standalone forms expose Borrower Submission / Staff Review demo switch. Staff Review links to existing example staff detail pages.
- LP disclaimer and action footer move after ownership-specific Document Upload when that section is shown.

Important: Browser behavior has NOT been validated. Do not deploy to production until testing. Existing form demo state is not preserved when navigating between pages.
