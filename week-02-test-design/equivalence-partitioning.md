# EQUIVALENCE PARTITIONING (EP)

- What is Equivalence Partitioning? It is a test design technique that is used to group inputs into partition where values are expected to produce same behaviour according to requirements.

- What problem does equivalence partitioning solve?
  1. It reduces the number of test cases by selecting representative inputs from groups that should behave the same while maintaining meaningful behavioural coverage.

- Why do we group inputs according to expected behaviour rather than simply grouping values that look similar?
  1. We group inputs according to expected behaviour because numerical similarity does not determine how the system should respond. For example, if an amount must be at least KES 5,000, then KES 4,900 and KES 5,001 are numerically close but belong to different partitions because one should be rejected and the other accepted. Meanwhile, KES 5,001 and KES 15,000 may be far apart but belong to the same valid partition because both should be accepted.

## APPLY THE TECHNIQUE

QUESTION: A fintech accepts withdrawal amounts between KES 500 and KES 50,000 inclusive.
Identify: - All equivalence partitions - One representative value for each partition - The expected behaviour of each representative - Explain why your chosen values belong to their respective partitions

Answers:

1. Partition Example Expected Behaviour
   invalid: amount < 500 400 reject
   valid: 500 <= amount <= 50,000 30,000 accept
   invalid: amount > 50,000 55,000 reject

2. Representative Values: 400, 30,000, 55,000
3. Expected Behaviour: Less than 500, the system will reject; greater than or equal to 500 and less than or equal to 50,000, the system will accept; greater than 50,000, the system will reject.
4. Each representative belongs to its partition and is expected to produce the behavior defined by the requirement. For example, 30,000 belongs to the valid range because it is between 500 and 50,000 inclusive.

## UNDERSTANDING REPRESENTATIVES

- What is a representative value? is one selected input from an equivalence partition used to test that category instead of testing every value in the partition.
- Question: If you choose KES 10,000 to represent the valid withdrawal partition, does that mean amounts below KES 10,000 are invalid? Explain your reasoning.
- Answer: No. KES 10,000 is only one representatives selected from the valid partition. It does not mean that KES 10,000 is the minimum valid amount

## LIMITATIONS AND PRODUCTION THINKING

A developer says: "We tested one valid amount, so all valid amounts are proven to work." Do you agree? Explain what EP can achieve, what it cannot guarantee, and why additional testing designs are necessary.

- EP can achieve the ability to test values that behave the same according to the requirement.
- EP cannot guarantee that all valid values are good to go, since a bug in implementation can cause two valid values to behave differently, violating the expected behaviour.
- We need additional testing design to ensure that all valid values do not violate expected behaviour.

## REQUIREMENT AND REAL-WORLD APPLICATION

A PIN must contain exactly 4 numeric digits, with no letters or special characters. Design equivalence partitions and explain how you would handle an ambiguous requirement where the specification only says "exactly 4 characters" without clarifying whether letters are allowed.

- Answer

Partition Example Expected Behaviour
invalid: PIN < 4 123 reject
valid: PIN = 4 4567 accept
invalid: PIN > 4 56789 reject.

- I would report the ambiguity in the specification for clarification to understand what they meant. It is a mixture of numbers and special characters, and the requirement should clearly state whether letters are allowed or if it is numeric only.
