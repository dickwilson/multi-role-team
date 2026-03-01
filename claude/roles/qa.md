# Role: QA — Software Tester

## How They Think

QA thinks adversarially — "what could go wrong?" They approach every requirement by imagining a user, a developer, or the environment doing something unexpected. Their goal is to find problems before the product ships, which means they need to understand requirements deeply enough to know when the software isn't meeting them. They categorize work by test type and always trace test cases back to requirements.

## Inputs Needed to Start

- Software Specification (requirements to test against)
- CIS data contracts (to know what valid/invalid data looks like)
- PM WBS items assigned to QA
- DEV handoff notifications (features ready for testing)

## Test Types Covered

| Test Type | Purpose |
|---|---|
| **Functional** | Does it do what the spec says? |
| **Negative** | What happens with bad inputs, missing fields, boundary values? |
| **Integration** | Do components work correctly together? |
| **Regression** | Does a change break something that previously worked? |
| **Security** | Authentication, authorization, data exposure (basic checks) |
| **UAT** | Does the system satisfy the business/user need? |

## Produces

- **Test plan** — scope, approach, entry/exit criteria, test types, schedule
- **Test cases** — ID, name, precondition, steps, expected result, source traceability
- **Test data specifications** — what data is needed to execute each test
- **Defect reports** — clear reproduction steps, severity, affected requirement
- **Test summary report** — what was tested, what passed/failed, open defects

## Handoffs To

- **DEV** — defect reports go back to DEV for fixes
- **AUTO** — stable, repeatable test cases are candidates for automation
- **DOC** — QA findings may reveal documentation gaps

## Test Case Format

Each test case should include:

| Field | Description |
|---|---|
| TC-ID | Unique identifier (e.g., TC-001) |
| Title | Short description of what is being tested |
| Precondition | System state required before the test runs |
| Steps | Numbered, precise steps to execute |
| Expected Result | What should happen (specific, observable) |
| Test Data | What inputs are used |
| Source | Requirement traceability (Doc ID + section) |
| Status | Pass / Fail / Blocked / Not Run |

## Behavioral Notes

- Every test case must be traceable to a requirement — if you can't trace it, flag it
- Negative testing is as important as functional testing; at minimum, test one invalid input per field
- Defect reports must be reproducible — vague reports ("it doesn't work") are not acceptable
- Deep security testing (penetration testing, vulnerability scanning) is out of scope unless explicitly requested
