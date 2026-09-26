# Test Levels

## What is test level and why is it important?

- Test Levels: Are structural stages where a system/application is involved from the isolated code block to the entire application. It is significant because it enables the team to find and catch bugs early, which is less costly compared to finding bugs in production.

Unit Test Level:

- It is a stage where developers write and test each unit in isolation.
- Developers own this level; QA's just review tests.
- M-Pesa application has hundreds of rules and decisions, and each one is a unit, so developers test the unit according to the requirement.
- Skipping these levels would cause bugs that would later be found in production, which could be costly for the company.

Integration Test Level: QA's and developers test units integrated together to make sure they communicate seamlessly and no bugs are present.

- Both QA's and developers own this level.
- When an API communicates with the database to confirm the user's existing account.
- Skipping this stage would place the company in catastrophic consequences. Example: we have double transactions at the same time in a loan application, money leaving twice. Recovery is painful, costly, and sometimes impossible.

System Test Level: QA's run the tests from the user's perspective against the requirement document.

- QA owns this level.
- Find out how the system is verifying the user's credentials (speed, and if rejected does it block the user from getting approved and communicate clearly to the user what happened).
- This is important to identify and catch silent bugs. Example: if the system silently fails to verify the user credentials and approves the user in acquiring the loan, that is a financial risk for the company.

Acceptance Test Level: Stakeholders (Directors, Product Managers, Customers, Operations Officers) test the system to ensure it meets the business vision and the user's requirements.

- The stakeholders (Directors, Product Managers, Users) are involved in this phase.
- Customer: Real users in a controlled environment before the application is shipped are given access to experience the application, e.g., the loan application process and repayment clarity.
- It is important to make sure that the system meets the business vision and the real user requirements before it is shipped to production.
