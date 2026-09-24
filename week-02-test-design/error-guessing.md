# ERROR GUESSING TESTING

## What is Error Guessing Testing?

- It is a testing technique that testers use their knowledge, intuition, and experience to catch bugs that structured techniques would have missed.

## Why does the Error Guessing Technique Exist?

- To enable testers to catch bugs in the system where structured techniques such as EP and BVA would have missed.

- STRENGTH OF ERROR GUESSING: It catches bugs that structured techniques would have missed.
- WEAKNESS OF ERROR GUESSING: It requires experience and more iterations of how systems break.

## M-Pesa Send Money - Error Guessing Examples

What if the user sends KES 0?
What if the user copies and pastes the recipient number and it has a hidden space at the end?
What if the user makes two transactions at the same time?
What if the user enters an amount that is insufficient?
What if the network drops at midnight while the user is doing the transaction?
What if the user misses one number of the recipient's phone number intended to be sent the money?
What if the user enters the wrong PIN, and he has forgotten the PIN number?
What if the user enters the wrong amount, maybe he is in a hurry?

- How does experience build the error guessing technique? Being exposed to handling several real-world systems makes QA make deadly error guesses since he understands and knows the patterns of how systems break.
