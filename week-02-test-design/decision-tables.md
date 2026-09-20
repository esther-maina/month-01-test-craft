# DECISION TABLES

- It is a design test techniques where tester use to test multiple conditions combined to produce possibles outcomes.

## When to use Decision Tables instead of EP and BVA

- We use EP and BVA when we have to test each inputs at a time, but when we have multiple conditions combined to produce possible outcomes we use decision tables.

## The formula

- Total combination = number of conditions _2, so if you have three condition we say: 2_ 2 \* 2 = 8, this means that you have 8 possible outcomes.

## QUESTION 1

- M-Pesa has a feature: "A user can send money only if they have sufficient balance AND their account is verified AND the recipient number is valid. Write a complete decision table showing the results.
  Balance | Verified | Recipient | Result
  Y | Y | Y | ACCEPT
  Y | Y | N | REJECT
  Y | N | Y | REJECT
  Y | N | N | REJECT
  N | Y | Y | REJECT
  N | Y | N | REJECT
  N | N | Y | REJECT
  N | N | N | REJECT

## QUESTION 2

- A user can withdraw cash only if their account is active AND they have completed PIN verification AND their daily withdrawal limit has not been exceeded.
  Account | PIN | Limit OK | Result
  Y | Y | Y | ACCEPT
  Y | Y | N | REJECT
  Y | N | Y | REJECT
  Y | N | N | REJECT
  N | Y | Y | REJECT
  N | Y | N | REJECT
  N | N | Y | REJECT
  N | N | N | REJECT

## RULE

- Always start with 'Y' combinations for the first condition, then flip systematically

## QUESTION

- Which of the combinations would you prioritise.

The only ACCEPT combination

- All conditions that pass, ACCEPT, if this breaks the feature is completely dead. Nothing works; always test this first.

The highest business risk

Account: Y | PIN: N | Limit: Y, REJECT

- Why? Because a valid account with a wrong PIN attempting a withdrawal is a fraud signal. If this combination incorrectly accepts, a hacker who stole someone's phone can drain their account. That is a catastrophic security failure worth millions.

The silent failure combination

- Because this is the combination that is most likely to frustrate a real user. Everything looks correct - active account, correct PIN - but the transaction fails because the limit is exceeded.
