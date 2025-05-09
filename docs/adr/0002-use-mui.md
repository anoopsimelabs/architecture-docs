# ADR-002: Standardize Frontend with MUI Design System

## Status

Proposed - 13/05/2025

## Context

React frontend uses a mix of styled components and lacks modular design. As per current implementation, we use MUI and to match with the design, there is lot of unnecessary work done. Also so much of redundant and unused compoentns are in the system.

## Decision

- Adopt MUI Figma UI kit for consistent design.
- Modularize components using a clean folder structure.
- Usage of dialog boxes will reduce the scrolling the page from user perspective.
- Identify common components and reuse it.

## Consequences

- Consistent UI/UX and devleoper experience.

## Related

[ADR-003](./0003-convert-long-forms.md)
