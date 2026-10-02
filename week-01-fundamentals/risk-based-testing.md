# RISK-BASED TESTING

## What is risk-based testing?

- Risk-based Testing: It is a practice that testers uses to priorities high likelihood/high impact of failures that could hurt most.

- Two question I should ask about every feature:
1.How likely is this to break?
2.The impact that could be caused when this breaks?

Example: Four category using watu credit:

| | High Impact | Low Impact |
| --- | --- | --- |
| **High Likelihood** | Test first. Automate. | Test manually. Monitor. |
| **Low Likelihood** | Test thoroughly. | Test last or skip. |

- In this Table it suggest that: If the test case are high likelihood and have high impact then you prioritise it to test it first. if many automate.
- If high likelihood but have low impact, you can manually test and monitor.
- If it is low likelihood but have high impact, you test it thoroughly
- If it is low likelihood and have low impact, you can either just skip it or test it later.

- Automation belongs to high likelihood/high impact to speed up the testing of the test cases, and also it is efficient, as compared to manual regression where due to exhaustively testing this can make the testers burn out and some of the bugs may be ignored or not captured which is expensive if discovered at production.
