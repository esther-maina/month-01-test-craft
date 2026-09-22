# State Transition Testing

## What is State Transition Testing?

- It is a testing technique that testers use to test each state that the system is in and every possible transition in each state.

## Three things that state transition testing checks

- Valid transition: Does the system move correctly between states?
- Invalid transition: Does the system block any transition that is not supposed to happen?
- State behaviour: How does the system behave while in a state?

## The Tala Loan state diagram and valid transitions and invalid transitions

- SUBMITTED → APPROVED → DISBURSED → ACTIVE → CLOSED
  ↓
  REJECTED

ACTIVE → OVERDUE → DEFAULTED

1. VALID: submitted -> approved: The system either rejects or accepts the credentials provided and then notifies the user.
2. VALID: Approved -> Disbursed: If the credentials are successfully verified, the user should receive the loan amount in either a bank account or M-Pesa, depending on the method they chose to receive the money.
3. VALID: Active -> CLOSED: The user completes the loan, the system updates its status, and notifies both the user and the company.

4. INVALID: REJECTED -> DISBURSED: The system fails to verify the user credentials but still moves to the disbursed state. It should reject the request, notify the user what happened, and block the user from acquiring the loan.
5. INVALID: OVERDUE -> NEW LOAN APPLICATION: The system allows the user to acquire a new loan even though the user has not yet completed paying the previous loan.
6. INVALID: ACTIVE -> CLOSED: The system marks the loan as complete when the user has only almost paid it; for example, if the loan was 5,000 and the user has paid 4,900.

- A state transition bug can cause financial loss if the system does not respond correctly to a state. For example, if it allows a user to acquire a loan even when verification failed, a hacker could empty the company's funds.
