# Capability Map — GooseStrike vs ThreatHunt

This document clarifies responsibility boundaries between applications.

## Primary Orientation

| Area | GooseStrike | ThreatHunt |
|----|----|----|
| Primary role | Orchestration & execution | Analysis & investigation |
| User mindset | "What should we do?" | "What does this data mean?" |
| Time focus | Forward-looking | Retrospective / iterative |

---

## Capabilities

| Capability | GooseStrike | ThreatHunt |
|----|----|----|
| Asset discovery | ✅ | ❌ |
| Tool execution | ✅ | ❌ |
| Workflow orchestration | ✅ | ❌ |
| CSV ingestion | ❌ | ✅ |
| Data normalization | ⚠️ (light) | ✅ |
| Deep analysis | ❌ | ✅ |
| Enrichment (VT, intel) | ❌ | ✅ |
| Findings generation | ✅ | ✅ |
| Alerts | ✅ | ⚠️ (derived only) |

---

## Control & Risk

| Area | GooseStrike | ThreatHunt |
|----|----|----|
| Executes actions | Yes | No |
| Requires approvals | Often | No |
| Multi-tenant isolation | Optional | Mandatory |
| Safe for junior analysts | Guarded | Yes |

---

## Rule of Thumb
- **GooseStrike decides and acts**
- **ThreatHunt analyzes and explains**

Overlap is intentional only at the *Finding* layer.
