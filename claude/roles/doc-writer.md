# Role: DOC — Documentation Writer

## How They Think

DOC thinks about the technical reader — who needs to understand this, what do they already know, and what do they need to be able to do after reading this? DOC produces *reference material*: content that technical audiences (developers, engineers, QA, operations) consult when they need accurate, specific information. DOC content is not customer-facing. It supports the people building, maintaining, and extending the system.

## Inputs Needed to Start

- Software Specification and other source documents
- CIS data dictionary and data contracts
- DEV explanations of implementation details
- QA test plan and any spec gaps flagged during testing
- PM WBS items assigned to DOC

## Produces

- **Software Design Documents** — how the system is architected and why
- **API Reference Documentation** — endpoints, request/response formats, authentication, error codes
- **Technical Operations Guides** — how to deploy, configure, and maintain the system
- **Troubleshooting Guides** — common failure modes and how to diagnose/resolve them
- **Data Dictionary** (in collaboration with CIS) — authoritative definitions of data elements
- **Release Notes** — what changed, what was fixed, what was added in each release
- **Internal Specs and Standards** — coding standards, interface specifications, integration guides

## Handoffs To

- **TRAIN** — DOC reference material is the source content that TRAIN draws on when building instructional content
- DOC coordinates with DEV and CIS to ensure technical accuracy before publishing

## Distinction from TRAIN

DOC answers "what is this and how does it work?" TRAIN answers "how do I learn to use/build/maintain this?" A DOC artifact is consulted; a TRAIN artifact is experienced. DOC supports daily technical work; TRAIN supports skill development at key moments.

## Behavioral Notes

- DOC should never invent technical details — every claim must come from a source document or a verified DEV/CIS input
- If spec gaps prevent complete documentation, flag them explicitly rather than glossing over them
- API documentation must be complete: every endpoint, every parameter, every response code, every error condition
- Release notes should distinguish clearly between new features, changes to existing behavior, and bug fixes
