# BUG REPORT ANATOMY

## Bug Anatomy

- It is a well structured report bug document that a QA present it to the team, after catching and evaluating the bug, This help the team especially developer to understand the bug, its impact.

## A sample of bug report that includes every detail

- QUESTION: You are a QA engineer at Cellipay and you did a test on the loan application on SamSung Galaxy A32 android 11,where the submit button on the appliacation form is unresponsive. No alerts, No notification. Just a silent bug. But testing the same process on iOS(iphone 13) the submit button works perfectly. Write a sample of bug Report.

- TITLE: Loan application submit button unresponsive on SamSung Galaxy A32(android 11),but on iphone it works.

- Enviroment: Device Type: SamSung Galaxy A32
            App Version: Cellipay app version 2.3.1
            Netwrok: Safaricom 4G data bundles

- Precondtions: User not yet logged in
               App already installed with the latest version.
               Device connected to the internet.

 Steps to Reproduce:

1. Click the Cellipay app on the homescreen to open.
2. Click Login and enter credentials:
   - Phone Number: 0756876543
   - Password: @test.com
   - Click Login button
3. On loan application form fill in each field:
   - First Name: John
   - Middle Name: Doe
   - Surname: Mally
   - Phone Number: 0756687543
   - National ID: 2543456
   - Amount to borrow: 10,000
   - Bank to receive money: Equity
4. Click Submit button.

Expected Result: When submit button is clicked, the app
should immediately process the loan application for approval.

Actual Result: Submit button is unresponsive. No action,
no alerts, no notifications displayed.

Evidence:

- Screenshot: [attached — cellipay_submit_bug.png]
- Logcat logs: [attached — logcat_2026_11_29.txt]

Severity: High — submit button is the final step of the
loan application flow. No Android user can complete
a loan application.

Impact:

- User: Cannot complete loan application, leading to
  frustration and app abandonment.
- Business: Revenue loss as users seek competitor apps.
  Potential CBK compliance violations if bug was
  knowingly shipped.
