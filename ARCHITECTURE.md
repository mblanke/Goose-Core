# Platform Architecture (Conceptual)

This document describes how GooseStrike, ThreatHunt, and goose-core relate at a high level.
It is conceptual by design and avoids implementation detail.

---

## High-Level Components

### goose-core (Shared)
- Defines shared terminology, contracts, and UX patterns
- Owns meaning, not behavior
- Changes infrequently

### ThreatHunt (Analysis Engine)
- Ingests exported data (CSV artifacts)
- Normalizes and enriches data
- Produces analytical Findings
- Never executes actions

### GooseStrike (Orchestration Engine)
- Accepts analyst intent
- Plans and coordinates actions
- Executes tools and workflows
- Consumes Findings as input

---

## Data Flow (Primary)

1. Data is collected externally (e.g., Velociraptor)
2. Data is exported and uploaded into ThreatHunt
3. ThreatHunt analyzes data and produces Findings
4. Findings conform to shared contracts (goose-core)
5. Findings may be consumed by GooseStrike
6. GooseStrike plans and executes actions
7. Execution produces additional Findings

---

## Control Flow (Primary)

- ThreatHunt is analyst-driven and exploratory
- GooseStrike is intent-driven and controlled
- goose-core enforces shared meaning across both

---

## Key Boundaries

- No direct database sharing between applications
- No direct execution from ThreatHunt
- No analysis logic inside GooseStrike
- Shared concepts are defined once in goose-core

---

## Design Intent

- Loose coupling
- Clear ownership
- Shared analyst experience
- Independent evolution of capabilities
