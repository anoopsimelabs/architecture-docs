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

## Spring Boot Services

---

### People Module - User Roles

| Method | Path                                     | Description                                                                | Decision |
| ------ | ---------------------------------------- | -------------------------------------------------------------------------- | -------- |
| GET    | /peoplemodule/userRole                   | List user roles with optional pagination and filtering by username         |          |
| GET    | /peoplemodule/userRole/{id}              | Fetch role details of a user by ID                                         |          |
| POST   | /peoplemodule/userRole                   | Assign role(s) to a user                                                   |          |
| PUT    | /peoplemodule/userRole/{userId}          | Update roles of a user                                                     |          |
| DELETE | /peoplemodule/userRole?userId=1?roleId=1 | Remove a specific role from a user using userId and roleId as query params |          |

---

### People Module - User Info

| Method | Path                         | Description                                       | Decision |
| ------ | ---------------------------- | ------------------------------------------------- | -------- |
| GET    | /peoplemodule/peopleUserList | Get users with optional filtering by employeeId   |          |
| GET    | /peoplemodule/user-details   | Fetch details of the currently authenticated user |          |

---

### Role Permission Management

| Method | Path                                   | Description                                            | Decision |
| ------ | -------------------------------------- | ------------------------------------------------------ | -------- |
| GET    | /peoplemodule/rolePermissions          | List all roles with filtering, pagination, and sorting |          |
| GET    | /peoplemodule/rolePermissions/{id}     | Get role details by ID                                 |          |
| GET    | /peoplemodule/selectedPermissions/{id} | Get selected permissions for a role                    |          |
| GET    | /peoplemodule/userList/{id}            | List users assigned to a specific role by roleId       |          |
| POST   | /peoplemodule/rolePermissions          | Create a new role with permissions                     |          |
| PUT    | /peoplemodule/rolePermissions/{id}     | Update a role’s permissions by ID                      |          |
| DELETE | /peoplemodule/rolePermissions?roleId=1 | Delete a role by roleId query param                    |          |

---

### Menu Management

| Method | Path                          | Description                           | Decision |
| ------ | ----------------------------- | ------------------------------------- | -------- |
| GET    | /peoplemodule/menuMaster      | Get a menu by id and parentId         |          |
| GET    | /peoplemodule/menuMaster/list | Fetch all menu items                  |          |
| GET    | /peoplemodule/menuList        | Fetch dropdown-friendly list of menus |          |
| POST   | /peoplemodule/menuMaster      | Create a new menu                     |          |
| DELETE | /peoplemodule/menuMaster/{id} | Delete a menu by ID                   |          |

---

### Leave Management (Spring Boot Services)

#### Leave Types and Status

| Method | Path                                 | Description                  | Decision |
| ------ | ------------------------------------ | ---------------------------- | -------- |
| PUT    | /leave/updateLeaveType/{id}          | Update leave type by ID      |          |
| POST   | /leave/saveLeaveType                 | Add leave type               |          |
| DELETE | /leave/deleteLeaveType/{leaveTypeId} | Delete leave type            |          |
| GET    | /leave/leaveType                     | Get all leave types          |          |
| GET    | /leave/getLeaveTypeById/{id}         | Get leave type by ID         |          |
| GET    | /leave/getAllLeaveTypeAndYear        | Get all leave types and year |          |
| PATCH  | /leave/updateStatus/{id}             | Update status                |          |

#### Leave Requests & Actions

| Method | Path                                       | Description                                 | Decision |
| ------ | ------------------------------------------ | ------------------------------------------- | -------- |
| POST   | /leave/leaveRequest                        | Apply leave                                 |          |
| GET    | /leave/leaveRequest/{id}                   | Get leave request by ID                     |          |
| PUT    | /leave/leaveRequest/{id}                   | Update leave request when status is pending |          |
| PUT    | /leave/cancel/{id}                         | Cancel leave request                        |          |
| PUT    | /leave/leaveApprove                        | Approve leave                               |          |
| PUT    | /leave/rejectLeave                         | Reject leave request                        |          |
| POST   | /leave/requestForMoreInfo/{leaveRequestId} | Request more information                    |          |
| GET    | /leave/getAllLeaveRequestOfUser            | Get all leave requests with employee ID     |          |
| GET    | /leave/getAllLeaveRequestByApproverId      | Get leave requests by approver ID           |          |
| GET    | /leave/allLeaveRequest                     | Get all leave requests                      |          |
| DELETE | /leave/getAllLeaveRequestOfUser/{id}       | Delete leave request by date                |          |

#### TOIL Requests

| Method | Path                     | Description          | Decision |
| ------ | ------------------------ | -------------------- | -------- |
| PUT    | /leave/toilReject        | Reject TOIL request  |          |
| PUT    | /leave/toilCancel/{id}   | Cancel TOIL request  |          |
| PUT    | /leave/toilApprove       | Approve TOIL request |          |
| POST   | /leave/toilApprovalEntry | Create TOIL approval |          |

#### Holidays

| Method | Path                              | Description                          | Decision |
| ------ | --------------------------------- | ------------------------------------ | -------- |
| POST   | /leave/addHoliday                 | Add holiday                          |          |
| PUT    | /leave/updateHoliday/{holidayId}  | Update holiday                       |          |
| GET    | /leave/holiday                    | Get holidays                         |          |
| GET    | /leave/getHolidaysByLocation      | Get holidays by location and year    |          |
| GET    | /leave/getHolidaysByEmployeeId    | Get holidays by employee ID and year |          |
| GET    | /leave/getHolidayById/{holidayId} | Get holiday by ID                    |          |
| DELETE | /leave/deleteHoliday/{holidayId}  | Delete holiday                       |          |
| GET    | /leave/sendHolidayReminders       | Send holiday reminders               |          |

#### Metadata & Configuration

| Method | Path                                              | Description                       | Decision |
| ------ | ------------------------------------------------- | --------------------------------- | -------- |
| GET    | /leave/getAllUnit                                 | Get all units                     |          |
| GET    | /leave/getAllDesignations                         | Get all designations              |          |
| GET    | /leave/getAllDepartments                          | Get all departments               |          |
| GET    | /leave/getAllTimelineByRequestId/{leaveRequestId} | Get reminders by leave request ID |          |
| GET    | /leave/getAllRole                                 | Get all roles                     |          |
| GET    | /leave/getAllResetType                            | Get all reset types               |          |
| GET    | /leave/getAllResetMonth                           | Get all reset months              |          |
| GET    | /leave/getAllReminderDays                         | Get all reminder days             |          |
| GET    | /leave/getAllPercentage                           | Get all percentage                |          |
| GET    | /leave/getAllLocations                            | Get all locations                 |          |
| GET    | /leave/getAllGender                               | Get all genders                   |          |
| GET    | /leave/getAllHolidayTypes                         | Get all holiday types             |          |
| GET    | /leave/getAllEffectiveTypes                       | Get all effective types           |          |
| GET    | /leave/getAllEffectiveMonth                       | Get all effective months          |          |
| GET    | /leave/updateAllocateToL1/getAllEffectiveDate     | Get all effective dates           |          |
| GET    | /leave/getAllCarryForwardStatus                   | Get all carry forward status      |          |
| GET    | /leave/getAllBalanceBasedOn                       | Get all balance based on          |          |
| GET    | /leave/getAllAccuralType                          | Get all accrual types             |          |
| GET    | /leave/getAllAccuralStatus                        | Get all accrual status            |          |
| GET    | /leave/getAllAccuralMonth                         | Get all accrual months            |          |
| GET    | /leave/getAllAccuralDate                          | Get all accrual dates             |          |
| GET    | /leave/health                                     | Health check endpoint             |          |

---

### Project Module - Master Data & Allocations

#### Technology Stack

| Method | Path                           | Description                      | Decision |
| ------ | ------------------------------ | -------------------------------- | -------- |
| GET    | /project/technologyStack       | Retrieve all technology stacks   |          |
| GET    | /project/technologyStack/{id}  | Find technology stack by ID      |          |
| GET    | /project/technologyStackSearch | Search technology stacks by name |          |
| POST   | /project/technologyStack       | Create a new technology stack    |          |
| PUT    | /project/technologyStack       | Update a technology stack        |          |
| DELETE | /project/technologyStack/{id}  | Delete a technology stack        |          |

#### Project CRUD

| Method | Path             | Description                                     | Decision |
| ------ | ---------------- | ----------------------------------------------- | -------- |
| GET    | /project/project | Find a project by ID (query parameter required) |          |
| POST   | /project/project | Add master data for project module              |          |
| PUT    | /project/project | Update master data for the project module       |          |

#### Project Types

| Method | Path                      | Description               | Decision |
| ------ | ------------------------- | ------------------------- | -------- |
| GET    | /project/projectType      | Find all project types    |          |
| GET    | /project/projectType/{id} | Find a project type by ID |          |
| POST   | /project/projectType      | Create a project type     |          |
| PUT    | /project/projectType      | Update a project type     |          |
| DELETE | /project/projectType/{id} | Delete a project type     |          |

#### Project Statuses

| Method | Path                        | Description                   | Decision |
| ------ | --------------------------- | ----------------------------- | -------- |
| GET    | /project/projectStatus      | Find all project statuses     |          |
| GET    | /project/projectStatus/{id} | Find a project status by ID   |          |
| POST   | /project/projectStatus      | Create a project status       |          |
| PUT    | /project/projectStatus      | Update a project status       |          |
| DELETE | /project/projectStatus/{id} | Delete a project status by ID |          |

#### Domains

| Method | Path                 | Description           | Decision |
| ------ | -------------------- | --------------------- | -------- |
| GET    | /project/domain      | Find all domains      |          |
| GET    | /project/domain/{id} | Find a domain by ID   |          |
| POST   | /project/domain      | Create a domain       |          |
| PUT    | /project/domain      | Update a domain       |          |
| DELETE | /project/domain/{id} | Delete a domain by ID |          |

#### Currency

| Method | Path                   | Description             | Decision |
| ------ | ---------------------- | ----------------------- | -------- |
| GET    | /project/currency      | Find all currencies     |          |
| GET    | /project/currency/{id} | Find a currency by ID   |          |
| POST   | /project/currency      | Create a currency       |          |
| PUT    | /project/currency      | Update a currency       |          |
| DELETE | /project/currency/{id} | Delete a currency by ID |          |

#### Business Units

| Method | Path                       | Description                  | Decision |
| ------ | -------------------------- | ---------------------------- | -------- |
| GET    | /project/businessUnit      | Get all business units       |          |
| GET    | /project/businessUnit/{id} | Find a business unit by ID   |          |
| POST   | /project/businessUnit      | Create a business unit       |          |
| PUT    | /project/businessUnit      | Update a business unit       |          |
| DELETE | /project/businessUnit/{id} | Delete a business unit by ID |          |

#### Billing Types

| Method | Path                      | Description               | Decision |
| ------ | ------------------------- | ------------------------- | -------- |
| GET    | /project/billingType      | Get all billing types     |          |
| GET    | /project/billingType/{id} | Find a billing type by ID |          |
| POST   | /project/billingType      | Create a billing type     |          |
| PUT    | /project/billingType      | Update a billing type     |          |
| DELETE | /project/billingType/{id} | Delete a billing type     |          |

#### Project Allocations & Users

| Method | Path                        | Description                                 | Decision |
| ------ | --------------------------- | ------------------------------------------- | -------- |
| PUT    | /project/unassign/{id}      | Unassign (delete allocation) from a project |          |
| POST   | /project/peopleUserList     | Update project managers from people users   |          |
| GET    | /project/projectMaster      | Get all master data for project module      |          |
| GET    | /project/projectDetails     | Find a project by ID                        |          |
| GET    | /project/projectAllocate    | Get project by ID                           |          |
| GET    | /project/project-allocation | Find project allocation by project ID       |          |
| GET    | /project/findProjectBySmlId | Find projects by SML ID                     |          |
| GET    | /project/doc                | Download doc for project module             |          |
| GET    | /project/allProject         | Fetches a paginated list of all projects    |          |
