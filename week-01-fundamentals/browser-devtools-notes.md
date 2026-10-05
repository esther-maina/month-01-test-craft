# BROWSER-DEVTOOL

## What is browser devtool

- It is a panel (Inspect) on the browser that enables both developers and testers to find bugs where they occurred and also to test responsiveness and how the system handles the process when the network is slow, fast, or drops while the user is still in action.

- Three-step decision tree for frontend and backend bugs.
  1. The user visits the website and fills in the credentials to log in.
  2. Check the console: If there is a red error, then the bug is frontend.
- If there is no error or nothing in the console, we proceed to the network tab. 3. In the network tab, we ask two questions:
- Did the request appear? If no, then that's a frontend bug. This means the code never reached the network call.
- If yes, then we proceed to the next step, where we check the request status code. 4. Check the request status code:
  - 4XX: The request sent was wrong. Most likely a frontend bug.
  - 5XX: Server failed. Backend server.
  - 200: This means the request was sent successfully; now you will check the response data to see if there are any errors. That's a backend bug.

As a good QA, you should also check the application to make sure it is secure. HttpOnly, Secure, and SameSite should all be registered with ticks or static values such as `None`. This communicates that the app is safe from attackers exploiting it easily.

- Also check device emulation to understand how the app is responsive on different devices. Also, throttling will enable the tester to know how the app responds to slow and fast networks, and how the system handles the data when the network drops abruptly while still in action.

- A table for the status code.

| Status code | Meaning               | Common cause                          |
| ----------- | --------------------- | ------------------------------------- |
| 200         | OK                    | Request was successful                |
| 201         | Created               | New resource was created              |
| 304         | Not Modified          | Cached version was used               |
| 401         | Unauthorized          | Invalid or missing credentials        |
| 403         | Forbidden             | Authenticated but no permission       |
| 404         | Not Found             | The requested resource does not exist |
| 500         | Internal Server Error | Backend crashed or failed             |
| 503         | Service Unavailable   | Server is overloaded or down          |

- What are cookies: These are small pieces of data that websites save in the browser to help remember the user's information. For example, instead of the website constantly asking the user to log in, once the user logs in, the website creates a cookie session.

- We have significant security flags to check in the cookie section of the Application tab.

1. HttpOnly: This means JavaScript cannot read the cookie. If so, an attacker can inject malicious JavaScript to steal the cookie directly, which would result in a security breach and the user's session may be compromised.
2. Secure cookies: The cookies should only be sent over HTTPS, not HTTP, because they can be intercepted on unsecured networks.
3. SameSite: The browser should only send a cookie if the request comes from the same website, not from another website. If it is third-party, it must be verified first before anything else occurs.

- Throttling matters because it enables both the tester and developer to observe how the system handles requests and processes over different network conditions, and also if the network drops suddenly while the user is still in action, what happens. Does the system save the process, or does it fetch again when the network returns?

## A SIMPLE BUG REPORT: SWAGLAB.COM SESSION COOKIES HAD EMPTY HTTPONLY, SECURE, AND SAMESITE VALUES

1. Title: Security Vulnerability: Missing cookie security flags on swaglab.com

2. Summary: While exploring the app in the browser developer tools, in the Application tab, I found that the session cookies are missing the HttpOnly, Secure, and SameSite attributes.

3. Preconditions: You should have an internet connection.

4. Steps to reproduce:
5. Open the site in the browser.
6. Log in to <www.saucedemo.com> using the username: standard_user and password: secret_sauce.
7. Right-click the page and select Inspect, or press F12 to open Developer Tools.
8. Navigate to Application tab > Cookies.
9. Inspect the session cookies.
10. Observe that HttpOnly, Secure, and SameSite are empty.

11. Expected Result: The site should configure all session cookies with proper security attributes to protect user sessions.

12. Actual Result: The cookies are missing the HttpOnly, Secure, and SameSite attributes.

13. Severity: High

14. Impact: This may expose the site to session hijacking, cross-site request forgery (CSRF), and cookie theft through malicious JavaScript injection.
