# Requirements Gathering

`Requirements Gathering` is the foundation upon which a successful system is built.

<br />

## Functional Requirements (The "What")

These describe the specific `behaviors` and `functionalities` the system must perform. This tells us about what we can do with this system.

- `User Stories/Use Cases`: Describe how different actors (users, systems) will interact with the system. (e.g., "As a customer, I want to add items to a shopping cart so that I can purchase them later.")
- `Features & Capabilities`: A detailed list of system features.
- `System Inputs & Outputs`: What data goes in, what results/forms/reports come out?
- `Workflows & Business Logic`: The step-by-step processes and rules the system must enforce (e.g., "An order must pass a credit check before fulfillment").
- `Data Handling`: What data needs to be created, read, updated, deleted (CRUD)?

<br />

## Non-Functional Requirements (The "How Well")

These define the `quality attributes` and `constraints` of the system. They are often the difference between a usable system and a failed one. This tells us about how out system can perform under diffrent factors and diffrent scenarios.

- `Performance`: Response time (latency), throughput (transactions/second), resource usage (CPU, memory).
- `Scalability`: Ability to handle increased load (more users, more data). Consider vertical (bigger machine) vs. horizontal (more machines) scaling.
- `Availability & Reliability`: Uptime requirements (e.g., 99.9%), mean time between failures (MTBF), fault tolerance.
- `Security`: Authentication, authorization, data encryption, audit logging, compliance (GDPR, HIPAA, PCI-DSS), vulnerability management.
- `Usability`: Target user proficiency, accessibility standards, learning curve.
- `Maintainability`: Ease of fixing bugs, adding features, and updating technology.
- `Portability`: Does it need to run on different OSes, browsers, or cloud platforms?

<br />
<br />
<br />
<hr />

## Constraints (The "Limits")
- `Technical Constraints`: Mandated technology stacks (programming languages, databases, cloud providers), compatibility with legacy systems.
- `Business Constraints`: Budget, deadlines (time-to-market), resource availability (team skills).
- `Regulatory & Compliance Constraints`: Legal requirements specific to the industry (e.g., financial reporting, data residency laws).

<br />

## Stakeholder and User Considerations
- `Identify All Stakeholders`: Not just end-users, but also business owners, managers, admins, support staff, and external systems.
- `User Personas & Characteristics`: Who are the users? What is their technical skill level? What are their primary goals?
- `Context of Use`: Where and how will the system be used? (e.g., on a mobile device in the field, on a desktop in an office).

<br />

## Domain and System Context
- `Domain Knowledge`: Deeply understand the business problem. Misunderstanding the domain is a leading cause of failure.
- `System Landscape`: How will the new system interact with existing systems (APIs, data feeds, imports/exports)? Define system boundaries clearly.
- `External Dependencies`: Third-party services, APIs, or data sources the system will rely on.

<br />

## Future-Proofing and Evolution
- `Expected Changes`: What features are likely to be added in the next 1-3 years? (e.g., "We plan to enter the European market next year.")
- `Extensibility`: Designing the system to accommodate foreseeable changes without major rewrites.
- `Deprecation & Sunset`: Are you replacing an old system? What is the migration and coexistence plan?

<br />
<br />
<br />
<hr />

## Key Principles & Best Practices for the Gathering Process:
- `Ask "Why" Continuously`: Uncover the root business problem, not just the stated solution. A stakeholder might ask for a button; you need to understand the job they need done.
- `Prioritize Ruthlessly`: Use frameworks like MoSCoW (Must have, Should have, Could have, Won't have) to manage scope and focus on value.
- `Quantify Wherever Possible`: Turn "must be fast" into "the search page must load in < 2 seconds for 95% of users under standard load."
- `Use Multiple Techniques`: Don't rely on just one method. Combine:
    - Interviews (for depth),
    - Workshops/JAD sessions (for alignment and brainstorming),
    - Surveys (for breadth),
    - Observation (to see actual workflows),
    - Document Analysis (of existing systems/processes),
    - Prototyping (to validate and clarify requirements visually).
- `Traceability`: Ensure each requirement can be traced back to a business objective and forward to a design component and test case.
- `Assumptions & Risks`: Explicitly document all assumptions made. Identify and document risks associated with requirements (e.g., "This requires a third-party API that is currently in beta").
- `Validation and Verification`: Continuously validate requirements with stakeholders to ensure they are correct ("Are we building the right thing?"). Plan to verify the system later against them ("Are we building the thing right?").

<br />
<br />
<br />
<hr />

## Common Pitfalls to Avoid
- `Focusing Only on Functional Requirements`: Ignoring non-functional needs like scalability leads to system failure under load.
- `Ambiguity`: Vague statements like "user-friendly" are a source of conflict later. Be precise.
- `Gold-Plating`: Adding features nobody really asked for or needs.
- `Silent Stakeholders`: Failing to identify a key stakeholder (e.g., the legal department) who surfaces critical constraints late in the process.
- `Analysis Paralysis`: Trying to gather 100% of requirements before any design or building. Embrace an iterative approach (Agile/Scrum) where requirements are refined continuously.

<br />
<br />
<br />
<hr />

## Output / Deliverables

While not always formal documents, the gathered knowledge should be captured in:

- Software Requirements Specification (SRS) or a Product Requirements Document (PRD)
- User Story Map and prioritized Product Backlog
- Use Case Diagrams and detailed Use Case Descriptions
- Glossary of Key Domain Terms
- List of Accepted Constraints and Assumptions
- UI/UX Wireframes and Prototypes

<br />
<br />
<br />
<br />

In essence, the goal of requirements gathering is to develop a shared, unambiguous, and actionable understanding of what needs to be built and why, considering not just the desired features but the environment, users, and future. A well-gathered set of requirements acts as the guiding star for all subsequent design and development decisions.