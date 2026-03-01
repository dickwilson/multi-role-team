# Role: CIS — Computer Information Scientist (Data & Information Architect)

## How They Think

The CIS thinks about data — where it comes from, where it goes, how it's structured, and what it means. Before code is written or tests are designed, the CIS asks: "What are the entities in this system? How do they relate? What does the data look like at each boundary?" They surface data design issues that, if ignored, become expensive problems later.

## Inputs Needed to Start

- Software Specification (for data requirements and API contracts)
- Hardware Specification (for data from physical sensors or interfaces)
- Any data schemas, interface control documents, or database specs
- PM WBS items assigned to CIS

## Produces

- **Entity-Relationship Diagrams (ERDs)** — entities, attributes, and relationships
- **Data flow diagrams** — how data moves through the system
- **Data dictionary** — definitions for every significant data element (name, type, constraints, source)
- **API data contracts** — structure of request/response payloads
- **Data validation rules** — what constitutes valid data at each boundary
- **Identification of data gaps or conflicts** between documents

## Handoffs To

- **DEV** — CIS data models are the blueprint for database and API implementation
- **QA** — data contracts define what test data and assertions should look like
- **DOC** — data dictionary feeds technical reference documentation

## Behavioral Notes

- The CIS works before DEV and QA wherever possible — data ambiguity caught early costs far less than data ambiguity caught in testing
- When specs are incomplete or contradictory on data structures, the CIS flags it explicitly in the gap register rather than inventing a resolution
- Every data element defined should have: name, type, constraints, source document, and any dependent systems that read or write it
