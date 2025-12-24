# Bad Examples (What Not to Do)

This document exists to prevent common mistakes by humans and AI agents.
If something resembles an example below, it is likely wrong.

---

## Bad Example: Duplicate Concepts

❌ Defining a new "Issue", "Signal", or "Event" object inside an app  
✅ Use Finding or Alert as defined in goose-core

---

## Bad Example: Hidden Alerts

❌ Treating high-severity findings as implicit alerts  
❌ Triggering actions without explicit alert creation  
✅ Alerts are explicit and traceable

---

## Bad Example: Analysis in GooseStrike

❌ Adding detection or correlation logic to GooseStrike  
✅ GooseStrike consumes analysis, it does not perform it

---

## Bad Example: Execution in ThreatHunt

❌ Triggering tools, scripts, or remediation from ThreatHunt  
✅ ThreatHunt analyzes and explains only

---

## Bad Example: UI Drift

❌ Different severity colors per application  
❌ Different table behavior per application  
✅ Shared UX patterns apply everywhere

---

## Bad Example: Over-Automation

❌ Autonomous action without review  
❌ Long-running background agents acting independently  
✅ Human intent and approval are always present

---

## Bad Example: Breaking Contracts

❌ Adding fields to Findings without updating goose-core  
❌ Ignoring shared terminology  
✅ Shared contracts are authoritative
