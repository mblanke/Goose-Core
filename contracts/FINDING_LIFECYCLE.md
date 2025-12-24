# Finding Lifecycle (Shared)

This defines how findings move across systems.

## Lifecycle Stages

1. **Generated**
   - Created by ThreatHunt analysis
   - Created by GooseStrike execution results

2. **Normalized**
   - Must conform to shared Finding contract
   - Terminology and severity aligned

3. **Reviewed**
   - Analyst inspects finding
   - Confidence assessed
   - Context added

4. **Escalated (Optional)**
   - Finding becomes an Alert
   - Requires action or acknowledgment

5. **Consumed**
   - Used by GooseStrike for planning
   - Used by analysts for reporting

---

## Hard Rules
- A Finding must exist before an Alert
- Severity is immutable once escalated
- All actions must trace back to a Finding
- Findings are never deleted, only closed

---

## Ownership
- ThreatHunt owns analytical correctness
- GooseStrike owns action traceability
- goose-core owns structure and meaning
