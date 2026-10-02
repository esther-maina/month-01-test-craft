# EXPLORATORY TESTING

## What is Exploratory Testing?

- It is an unscripted testing approach where learning software, designing test cases, and executing them all happens at the same time.

- Charter: It is an unscripted short document created before a session; it defines:

1. What are you exploring?
2. Your goal (what you are looking for)
3. Time

Example: Using the Cellipay loan application app

Charter 1: Exploring the login form of Cellipay
Goal: Investigate how the login form handles invalid
and missing inputs
Time: 10 minutes

Charter 2: Examining the loan application form
Goal: Explore how the form handles invalid credentials
and how number input fields display on
iPhone and Android
Time: 25 minutes

Charter 3: Exploring business-critical areas
Goal: Evaluate how the app handles duplicate transactions
Time: 10 minutes

- Sessions: These are notes of everything the tester recorded during and after the session.

Example: Using Charter 1 in the Cellipay loan application app
During Session (Login Form)
I tested the login form with the correct credentials, and it passed; there were no bugs and no error messages.
I tested the login form using the wrong password, and the app showed a clear error explaining what caused it to block the process.
In the email input field, I left it empty and proceeded to click the login button; then the form silently processed to the loan application page.
I used an invalid phone format, and the app crashed immediately when I pressed the login button.

After Session
Bug 1: The system silently processed the invalid/empty email field. This is a high-severity, high-priority issue because the system creates a way for unauthorised individuals to attempt login, and the cost is too expensive for the business to cover.
Bug 2: The app crashed when I entered an invalid phone format. Based on the requirement, the app should be able to handle this scenario by alerting the user with a red banner that contains a clear message they can understand. App crashes are never acceptable behaviour.

Areas not covered: Multiple failed login attempts lockout behaviour. Recommended for a follow-up charter.

- Difference between charter and test case: In contrast to test cases, where testers are given guidelines to follow before testing, a charter gives testers a goal and focus and also freedom to test and investigate what they find.
