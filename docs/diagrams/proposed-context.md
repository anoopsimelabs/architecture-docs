---
hide:
  - toc
---

# System Context Diagram

This diagram shows how the system interacts with users and external systems.

```mermaid
graph LR
    EMP[Employee]
    HRA[HR Admin]
    SA[Super Admin]
    PM[Project Manager]

    PAPI["PAPI <BR> (Internal Employee Portal)"]
    EXT_PMD["PM Dashboard"]

    PAPI <--> EXT_PMD

    EMP --> PAPI
    HRA --> PAPI
    SA --> PAPI
    PM --> PAPI

    PAPI <--> DB[(Internal PostgreSQL DB)]
    EXT_ZOHO[(Zoho DB)] -- employee data --> DB

    style EXT_ZOHO fill:lightgreen,stroke:white
    style EXT_PMD fill:lightgreen
```
