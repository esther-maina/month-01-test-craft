# BOUNDARY VALUE ANALYSIS (BVA)

- It is a test design technique where we test the exact boundary values and their values just outside them, because that is where developers make the most mistakes.

## Example: Requirement: Only 18 and 40 inclusive allowed

- In BVA we have six test cases. where we have lower boundary and upper boundary.

 1. Lower Boundary
 Value below the boundary(17)---> Reject
 Boundary itself(18)---> accept
 value above the boundary(19)---> accept(since it is falls within the requirement between 18 and 40)

 2. Upper Boundary
  Value below the boundary(39)---> Accept(since it falls between the boundary(18 and 40))
  Boundry itself(40)---> Accept
  Value above the boundary(41)---> reject.

## How EP and BVA work together in one sentence

- EP: It tells which groups are being tested, while BVA tells where inside this partition will be tested, since that is where bugs usually occur.

## QUESTION: Given this Tala requirement, for transaction to happen the amount should be between KES 500 - 50,000. Generate or write the EP and BVA tables

- EP
Partition                        Example        Expected Behaviour
invalid: amount < 500            450            Reject
valid: 500<= amount <= 50,000   35,000          Accept
invalid: amount > 50,000        55,000          Reject

- BVA
Lower Boundary
499---> just lower value ---> REJECT
500---> boundary ---> ACCEPT
501---> above value---> ACCEPT

Upper Boundary
49999---lower value ---> ACCEPT
50000---boundary---> ACCEPT
50001---Above value ---> REJECT
