# Architecture Prompts

## 1. Component & Data Model Sketch

```text
Given this scope: [paste v1 scope]

Propose:
1. The main components/services and how they talk to each other
   (as a short list, not a full diagram yet).
2. A first-pass data model: entities, key fields, relationships.
3. Any architectural decisions that are hard to reverse later
   (e.g. sync vs async, monolith vs services, SQL vs NoSQL) — flag these
   explicitly and give me the trade-offs, don't just pick one silently.
```

## 2. Architecture Review

```text
Here's my current architecture: [describe or paste diagram/structure].

Review it for:
- Single points of failure
- Scalability limits given expected load: [describe expected scale]
- Unnecessary complexity for the current stage
- Missing pieces (e.g. caching, queueing) that will be needed soon

Rank findings by how expensive they'd be to fix later if not addressed now.
```

## 3. Trade-off Comparison

```text
I'm deciding between [option A] and [option B] for [specific decision,
e.g. "the primary database"].

Context: [scale, team size, existing stack, constraints]

Compare them on: [e.g. operational complexity, cost, query flexibility,
scaling characteristics]. Recommend one for my specific context, and
say what would change your recommendation.
```

## 4. Mermaid Diagram Generation

```text
Generate a Mermaid flowchart/sequence diagram for this architecture:
[describe components and interactions]

Requirements:
- Use flowchart TD for structure, sequenceDiagram for request flows
- Label edges with what's being passed (not just arrows)
- Keep it to the components I listed — don't invent additional services
```

## Related

- [System Design](../../docs/09-system-design/README.md)
- [Planning](../../docs/08-planning/README.md)
- [Prompt Library home](../README.md)
