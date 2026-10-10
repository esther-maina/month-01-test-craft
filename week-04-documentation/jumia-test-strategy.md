# Test Strategy - Jumia Kenya (jumia.co.ke)

**Product:** Jumia Kenya E-commerce Platform
**Prepared by:** Esther Maina
**Date:** October 2026
**Version:** 1.0

## 1.Scope

### In Scope

- Add to cart functionality button
- User registration and login Authentication
- Product search and filtering
- Responsive design on both desktop and phone browser.
- Order confirmation
- Payment methods

### Out of Scope

- Third party payment integration system
- Jumia logistic Dashboard
- Jumia Admin Dashboard
- The performance and loading of the web app
- Email notification delivery system
- Responsive design of the web app on iOS - not available for testing

## 2.Test Approach

- The following test types and test designs will be used to the  Jumia Kenya checkout flow:

- **Regression Testing:** Check to ensure that the existing features are not broken after any changes.
- **Sanity:** Check that specific feature work as expected after some changes done.
- **Functional Testing:** check every built-in feature works according to expected behaviour.
- **Responsive Testing:** Verify every layout on both mobile phone and desktop.
- **Exploratory Testing:** Check system unexpected behaviour.
- **State Transition Testing Design:** Observe how the system behave when in state and also when it transition between state.
- **Boundary-Value Testing Design:** Test the how the system handles the edge cases on the number input, in the M-Pesa section.

## 3.Tools

- **Browser:** Google Chrome and Firefox
- **DevTools:** Chrome DevTools - Application/Cookies, Network Tab, Console Tab, Throttling, Device emulation
- **Playwright Automation Tool:**(Month 3)
- **API Testing**(month 2)
- **Test Documentation:** Github and markdown
- **Jira:** For bug tracking
- **Evidence:** Mobile screen recorder and screenshots

## 4. Risks and Mitigations

| Risk | Mitigation |
| --- | --- |
| Delayed responses from the PM | Maintain clear and timely communication channels; align on expectations and decision-making promptly. |
| Electricity shortage | Ensure laptops are fully charged before testing sessions and keep mobile data as a backup connection. |
| Network drop | Test during stable network periods and save progress frequently to avoid losing work. |
| Deployment of updates during testing | Coordinate release windows and communicate change updates clearly before and during testing. |
| Test data limitation | Use guest checkout where possible and document payment steps with screenshots and network logs without completing a real purchase. |

## 5. Entry and Exist Criteria

### 1.Entry Criteria

- checkout flow is accessible and login/registration at checkout is functional.
- Test environment is stable and accessible
- Test cases have been written and reviewed
- Test devices and browsers are available and configured
- Chrome DevTools is available for network and console monitoring

### 2.Exit Criteria

- We have fixed and verified by QA, all the high severity bugs their status on JIRA is closed.
- We have tested 47 test cases out of 50 test cases that 96% of test cases have passed.
