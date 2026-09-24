# PAIRWISE

## What is pairwise?

- It is a combinatorial test design technique used to ensure every possible valid pair of values across two different parameters is tested at least once

- When use pairwise when the decision tables becomes too large(where the number of combination increases)

- The three-way comparison table

| Technique       | What it tests                          |
| --------------- | -------------------------------------- |
| EP and BVA      | One condition in isolation             |
| Decision Tables | All conditions combined                |
| Pairwise        | Every pair of conditions at least once |

## Gate Question: A Tala loan application has these parameters

Device: Android, iOS
Network: 3G, 4G, WiFi
Loan amount: Small, Medium, Large
User type: New, Existing

Two questions:

How many full combinations exist?
Name three pairs you would prioritise testing and explain why each pair matters in a Kenyan fintech context.

1. Combinations = 2 _3_ 3 \* 2 = 36
2. Device + Network: An Android user on 3G may experience slow verification response causing timeouts or app abandonment, mostly fintech users are using Android with bundles as compared to WiFi.

- Device + Loan Amount: Number input fields may behave differently across Android and iOS keyboards. On certain Android devices, large amounts like KES 100,000 may be formatted with commas or spaces automatically, causing the system to reject or misread the value. This pair matters because input formatting bugs are device-specific and easy to miss when testing on only one platform.

- Loan Amount + User Type: A new user requesting a large loan should be rejected or capped by the system because no repayment history exists. An existing user with good history should be approved. The bug risk is that the system approves a large loan for a new user, exposing the company to default risk. This pair matters because loan limits tied to user history is a core business rule in Kenyan microfinance.

- PICT Tool(Pairwise Independent Combinatorial Testing): A tool that generates the minimum set of test cases needed to cover all pairs, so you don't calculate combinations manually.

- Pairwise provides testing coverage of all selected pair two-way interaction, it does not guarantee coverage of all high-order interactions or the entire application functionality.
