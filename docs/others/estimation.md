# Full System Revamp: High-Level Estimation

This document outlines a high-level estimation for the system revamp initiative, organized by major workstreams spanning backend, frontend, and database layers.

---

## Workstream Breakdown & Estimation

| ID  | Title                    | Description                                                                           | Estimated Effort (Person-Days) | Notes                                                                                                                        |
| --- | ------------------------ | ------------------------------------------------------------------------------------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| 01  | UI Revamp with MUI       | Replace legacy UI with Material UI components for consistency and responsiveness      | 7–10                           | Consistent styling and responsive design. Also flow based design should be there.                                            |
| 02  | DB Schema Refactor       | Refactor and evolve database schema, normalize the tables                             | 4–7                            | Schema updates, revisit the tables and normalize                                                                             |
| 03  | Converting Python module | New spring boot service for all services written in Python                            | 10–15                          | Prefer to be done only after the DB refactor                                                                                 |
| 04  | API Endpoint Adjustments | Align API endpoints with new database changes.                                        | 5–8                            | `This estimate might require a revisit after database refactor.`                                                          |
| 05  | UI Adjutments            | Align the UI with new API endpoint adjustments.                                       | 7–10                           | `This estimate might require a revisit after estimating API endpoints changes.`                                              |
| 06  | Stepper Forms            | Convert static long forms into multi-step/tab flows with validation and draft support | 8–12                           | Complex form logic, draft-save, and validation. Use a common component if available, or create a reusable one.              |

---

## Total Estimated Effort

**Range:** `41 – 62 person-days`  
**Assumptions / Notes**

- UI/UX design changes and database refactoring should be done first.
- **Finalize and review designs with all stakeholders before starting changes.**
- After the above steps, need to revisit the estimates.

---
