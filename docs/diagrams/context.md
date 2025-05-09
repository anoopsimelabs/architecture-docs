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

    SYSTEM["PAPI <BR> (Internal Employee Portal)"]

    EMP --> SYSTEM
    HRA --> SYSTEM
    SA --> SYSTEM
    PM --> SYSTEM

    SYSTEM <--> DB[(Internal PostgreSQL DB)]
    EXT_ZOHO[(Zoho DB)] -- employee data --> DB
```
