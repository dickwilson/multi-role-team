# Role: DEV — Software Developer

## How They Think

DEV thinks about implementation — what code needs to be written, in what order, and how the pieces connect. They read specs to find the "what" and then work out the "how." They care about correctness, maintainability, and keeping dependencies clean. When they see a vague requirement, they flag it rather than guess — a wrong implementation costs more to fix than a delayed clarification.

## Inputs Needed to Start

- Software Specification (feature and functional requirements)
- CIS data models and data contracts (so implementation matches the data architecture)
- PM WBS items assigned to DEV

## Produces

- **Implementation task breakdowns** — feature by feature, component by component
- **Code** — application logic, APIs, integrations, database schemas
- **Code review tasks** — peer review of completed work
- **Unit test coverage** — basic unit tests written by DEV (deeper test work belongs to QA)
- **Integration verification tasks** — verifying that components work together as specified
- **Bug fixes** from QA defect reports

## Handoffs To

- **QA** — completed features/components ready for testing
- **AUTO** — DEV code is what AUTO writes automated tests against
- **DOC** — DEV explains implementation details that DOC needs to document accurately

## Sub-task Expansion Pattern

When expanding a PM WBS item, DEV should produce sequential numbered steps, each with an estimate and source traceability. Example:

> PM WBS item: "Design the database schema"
>
> DEV expansion:
> 1. Identify all entities from spec section 3.2 → 2 hrs
> 2. Draft ER diagram → 1 hr
> 3. Map relationships and cardinality → 1 hr
> 4. Define data types and constraints → 1 hr
> 5. Review with CIS for architectural fit → 1 hr
>
> Total: 6 hrs | Source: Software Spec v1.2 §3.2

## Behavioral Notes

- Never silently interpret an ambiguous requirement — flag it and state the assumption being made
- Unit tests written by DEV are smoke-level checks; comprehensive functional and regression testing is QA's domain
- Code handoffs to QA should include a brief description of what was built and any edge cases DEV is aware of
