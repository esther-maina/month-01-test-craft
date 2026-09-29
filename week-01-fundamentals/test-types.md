# TEST TYPES

## What are Test Types

- These are actions performed by the testers on the new build feature and existing codebases to ensure the entire system works according to the requirements and also meets real users' expectations.

Smoke Test: It is a quick, high-level check of the new build software to verify its critical core feature is stable enough to be tested.

- WHEN IT RUNS: At the beginning of every test cycle.
- WHAT TRIGGERS IT: When a new build arrives from the developers.
- EXAMPLE: In the Cellipay app, developers implement a new feature of monthly repayment.
- It matters to do a quick test before investing more time in deep testing, and it helps us to find bugs fast. For example, when testing the entire application, we find that the new application's user repayment history dashboard is not displaying.

Functional Test: Carried out on a new build feature or new system to ensure it meets the requirement needs.

- WHEN IT RUNS: When a QA is testing a new feature or a newly built system (application).
- WHAT  TRIGGERS IT: When a new build feature or newly built application is ready.
- EXAMPLE: When developers present the new repayment feature of paying monthly, we test it to ensure it works or functions according to the requirement.
- WHY IT MATTERS: It helps testers confirm that the new build feature is working according to the requirement.

Regression Test: Confirms that the existing codebase is still working as expected when changes happen.

- WHEN IT RUNS: When anything is changed in the codebase.
- WHAT TRIGGERS IT: Developers make a change or update anything in the existing codebase.
- EXAMPLE: In Cellipay, developers change the daily repayment to monthly repayment, and we check if the existing dependencies were affected by the changes.
- WHY IT MATTERS: Enables testers to catch silent bugs in hidden dependencies.

Sanity Test: Testers focus on the specific area or feature that was updated or fixed and test it to confirm the fix works.

- WHEN IT RUNS: When the specific feature is debugged or updated.
- WHAT TRIGGERS IT: When developers present an updated feature of the application.
- EXAMPLE: A developer at Cellipay debugs the 'send' money button. As a tester I'll carry out testing of that specific fixed feature.
- WHY IT MATTERS: It ensures that the specific updated feature works.

UAT (User Acceptance Testing): A group of controlled real users and operations officers test the entire application to ensure it meets the user's expectations and the business vision.

- WHEN IT RUNS: When the tester gives a green light, then the users and operations officers test.
- WHAT TRIGGERS IT: QA presents the application to the operations officers and controlled users.
- WHY IT MATTERS: To ensure that the application meets the business vision and users' needs before shipping to production.
