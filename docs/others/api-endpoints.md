# PAPI Api Endpoints

## Python Backend

### Peoples - Core Employee Operations

| Method | Path                      | Description                              | Decision |
| ------ | ------------------------- | ---------------------------------------- | -------- |
| GET    | /peoples/                 | Get employee details from Zoho peoples   |          |
| GET    | /peoples/list/            | Get all employee list, search and filter |          |
| GET    | /peoples/{id}/            | Retrieve employee details                |          |
| PUT    | /peoples/deactivate/{id}/ | Deactivate a user                        |          |
| PATCH  | /peoples/deactivate/{id}/ | Deactivate a user (partial)              |          |

---

### Peoples - Regular Employees

| Method | Path                  | Description                     | Decision |
| ------ | --------------------- | ------------------------------- | -------- |
| POST   | /peoples/regular/     | Create regular employee         |          |
| PUT    | /peoples/regular/{id} | Update regular employee         |          |
| PATCH  | /peoples/regular/{id} | Partial update regular employee |          |

---

### Peoples - Contractors

| Method | Path                      | Description                      | Decision |
| ------ | ------------------------- | -------------------------------- | -------- |
| POST   | /peoples/contractor/      | Add contract employee            |          |
| GET    | /peoples/contractor/{id}/ | Retrieve contract user           |          |
| PUT    | /peoples/contractor/{id}/ | Update contract user             |          |
| PATCH  | /peoples/contractor/{id}/ | Partial update for contract user |          |

---

### Peoples - Identifiers and Login

| Method | Path                           | Description                       | Decision |
| ------ | ------------------------------ | --------------------------------- | -------- |
| GET    | /peoples/generate-contract-id/ | Retrieve new contract employee ID |          |
| GET    | /peoples/generate-employee-id/ | Retrieve new regular employee ID  |          |
| POST   | /peoples/login/                | User login                        |          |
| POST   | /peoples/login/google/         | Handle Google OAuth2 callback     |          |
| POST   | /peoples/logout/               | Logout the current user           |          |
| POST   | /peoples/refreshtoken/         | Refresh JWT token                 |          |
| POST   | /peoples/token/verify/         | Verify JWT token                  |          |
| POST   | /peoples/set-password/         | Set password                      |          |

---

### Peoples - Skills & Proficiency

| Method | Path                             | Description                    | Decision |
| ------ | -------------------------------- | ------------------------------ | -------- |
| GET    | /peoples/skill-master/           | List skills (active only)      |          |
| GET    | /peoples/skill/                  | List skills (active only)      |          |
| POST   | /peoples/skill/                  | Create skills                  |          |
| GET    | /peoples/skill/{id}/             | Retrieve skill                 |          |
| PUT    | /peoples/skill/{id}/             | Update skill                   |          |
| PATCH  | /peoples/skill/{id}/             | Partial update skill           |          |
| DELETE | /peoples/skill/{id}/             | Delete skill                   |          |
| GET    | /peoples/skill/categories/       | List & search skill categories |          |
| POST   | /peoples/skills-categories/      | Create skill category          |          |
| GET    | /peoples/skills-categories/{id}/ | Retrieve skill category        |          |
| PUT    | /peoples/skills-categories/{id}/ | Update skill category          |          |
| PATCH  | /peoples/skills-categories/{id}/ | Partial update skill category  |          |
| DELETE | /peoples/skills-categories/{id}/ | Delete skill category          |          |
| GET    | /peoples/proficiency/            | List proficiencies             |          |
| PUT    | /peoples/proficiency/{id}/       | Update proficiency             |          |
| PATCH  | /peoples/proficiency/{id}/       | Partial update for proficiency |          |
| POST   | /peoples/user/skill/             | Add user skill                 |          |
| PUT    | /peoples/user/skill/{id}/        | Update user skill              |          |
| PATCH  | /peoples/user/skill/{id}/        | Partial update user skill      |          |
| DELETE | /peoples/user/skill/{id}/        | Delete user skill              |          |
| GET    | /peoples/{id}/user-skills/       | Get employee skills            |          |

---

### Peoples - Education, Certificates, Experience

| Method | Path                                     | Description                      | Decision |
| ------ | ---------------------------------------- | -------------------------------- | -------- |
| DELETE | /peoples/educational-qualification/{id}/ | Remove educational qualification |          |
| POST   | /peoples/professional-certificates/      | Add professional certificate     |          |
| GET    | /peoples/{id}/certificates/              | Get employee certificates        |          |
| GET    | /peoples/{id}/work-experience/           | Get employee work experiences    |          |

---

### Peoples - Metadata (Departments, Designations, Locations, Managers)

| Method | Path                         | Description               | Decision |
| ------ | ---------------------------- | ------------------------- | -------- |
| GET    | /peoples/departments/        | List & search department  |          |
| GET    | /peoples/designations/       | List & search designation |          |
| GET    | /peoples/locations/          | List & search locations   |          |
| GET    | /peoples/reporting-managers/ | List reporting managers   |          |

---

### Peoples - User & Project Overview

| Method | Path                         | Description           | Decision |
| ------ | ---------------------------- | --------------------- | -------- |
| GET    | /peoples/users/              | Get all user list     |          |
| GET    | /peoples/{id}/user-projects/ | Get employee projects |          |
