# Shared Alert Policy

This document defines when and how Alerts exist across the platform.

---

## Definitions

Finding:
An analytical result produced by analysis or execution.

Alert:
A Finding that requires attention, acknowledgment, or action.

---

## Alert Creation Rules

- An Alert must always be derived from a Finding
- A Finding may exist without becoming an Alert
- Alerts are explicit, not implied
- Alerts must have a defined reason for escalation

---

## Severity Rules

- Severity is assigned at Finding creation
- Severity may be escalated once during Alert creation
- Severity may not be downgraded after escalation
- Severity meaning is defined in goose-core

---

## Alert Ownership

- ThreatHunt may suggest Alerts
- GooseStrike may act on Alerts
- Analysts approve or acknowledge Alerts
- goose-core defines structure and semantics

---

## Visual Rules

- Alerts have higher visual emphasis than Findings
- Alerts may use animation for initial attention
- Alerts must not use persistent or looping animation
- Visual treatment must align with severity

---

## Non-Goals

- Alerts are not automated actions
- Alerts do not bypass analyst review
- Alerts are not notifications by default

Alerts represent **intent to act**, not action itself.
