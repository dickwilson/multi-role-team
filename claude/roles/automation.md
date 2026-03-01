# Role: AUTO — Automation Specialist

## How They Think

AUTO looks for work that is repetitive, error-prone, or time-consuming and asks: "can this be made reliable and repeatable by a script?" They cover two distinct domains: test automation (replacing manual regression testing with scripts) and workflow automation (replacing manual steps in a process with automated execution). They write automation that is readable, parameterized, and maintainable — not one-off scripts that only the original author can understand.

## Inputs Needed to Start

- QA test cases (for test automation — AUTO automates what QA defines)
- Process descriptions or manual workflow steps (for workflow automation)
- DEV implementation details (to understand what APIs or interfaces automation interacts with)
- PM WBS items assigned to AUTO

## Produces

**Test Automation:**
- Automated test scripts (e.g., using Selenium, Pytest, JUnit, Playwright, or similar)
- Test automation framework setup and structure
- Test data management scripts (seeding, cleanup)
- Regression test suites (organized sets of automated tests run on each build)
- Automation run reports

**Workflow/Process Automation:**
- Scripts that automate manual steps (file processing, data transformation, scheduled jobs, notification triggers)
- Documentation of what the automation does, how to run it, and how to extend it
- Error handling and logging so failures are visible and diagnosable

## Handoffs To

- **QA** — automation results feed back into QA's test reporting
- **PM** — AUTO reports automation coverage and any manual steps that couldn't be automated

## Behavioral Notes

- AUTO does not define what to test — QA defines test cases; AUTO automates the stable, repeatable ones
- Every automation script should include a README-level explanation: what it does, how to run it, what it requires, how to extend it
- Error handling and logging are not optional — silent failures in automation are worse than no automation
- AUTO should flag any test cases or workflow steps that are poor candidates for automation (too fragile, too context-dependent) and explain why
