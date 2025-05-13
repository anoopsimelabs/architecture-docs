---
hide:
  - toc
---

### Auth & Permissions

```mermaid
erDiagram
    auth_group ||--o{ auth_group_permissions : has
    auth_group_permissions }o--|| auth_permission : uses
    auth_permission ||--o{ django_content_type : typed_as
    peoples_user ||--o{ peoples_user_groups : belongs_to
    peoples_user ||--o{ peoples_user_user_permissions : granted
```

### Core People Management

```mermaid
erDiagram
    direction LR
    peoples_user ||--o{ peoples_userrole : has
    peoples_user ||--o{ peoples_documents : has
    peoples_user ||--o{ peoples_educationalqualification : qualified_by
    peoples_user ||--o{ peoples_professionalcertificate : certified
    peoples_user ||--o{ peoples_workexperience : experienced_in
    peoples_user ||--o{ peoples_useridentitydocument : identified_by
    peoples_user ||--o{ peoples_bankdetails : paid_via
    peoples_user ||--o{ peoples_emergencycontact : contacts
    peoples_user ||--o{ peoples_insurancedependent : insures
    peoples_user ||--o{ peoples_gratuitynominee : nominates
    peoples_user ||--o{ peoples_pfnominee : pfnominates
```

### Leave Management

```mermaid
erDiagram
    peoples_user ||--o{ peoples_leaverequest : requests
    peoples_leaverequest ||--o{ peoples_leaverequestdetail : contains
    peoples_leaverequest ||--o{ peoples_leaveapproval : approved_by
    peoples_leaverequest ||--o{ peoples_leaverequestproject : for_project
    peoples_user ||--o{ peoples_leavebalance : has_balance
    peoples_user ||--o{ peoples_compensatoryrequest : comp_request
    peoples_compensatoryrequest ||--o{ peoples_compensatoryrequestapproval : approved
    peoples_user ||--o{ peoples_entitlement : entitled_to
    peoples_user ||--o{ peoples_firstmonthrule : first_month_rule
```

### Organization Structure

```mermaid
erDiagram
    peoples_user ||--o{ peoples_department : works_in
    peoples_user ||--o{ peoples_designation : holds
    peoples_user ||--o{ peoples_location : located_at
    peoples_user ||--o{ peoples_workmode : works_as
    peoples_user ||--o{ peoples_contractuserprofile : has_contract
```

### Roles, Menus & Permissions

```mermaid
erDiagram
    peoples_role ||--o{ peoples_userrole : assigned
    peoples_menu ||--o{ peoples_menu_roles : linked
    peoples_menu ||--o{ peoples_menupermission : secured_by
    peoples_role ||--o{ peoples_rolemenumapping : maps_to
    peoples_rolemenumapping ||--o{ peoples_rolemenumapping_button_permission : has_button
```

### Skills & Projects

```mermaid
erDiagram
    peoples_user ||--o{ peoples_userskill : skilled
    peoples_userskill ||--|| peoples_skill : describes
    peoples_skill ||--|| peoples_skillcategory : categorized_in
    peoples_user ||--o{ peoples_userproject : involved_in
    peoples_project ||--o{ peoples_userproject : worked_on
    peoples_user ||--o{ peoples_projectallocationl1 : allocated
```

### Project Managment

```mermaid
erDiagram
    project ||--o{ project_allocation : allocates
    project ||--|| project_type : classified_as
    project ||--|| project_status : status
    project ||--o{ project_technology_stack : uses
    technology_stack ||--o{ project_technology_stack : part_of
```

### Billing, Domain, Currency

```mermaid
erDiagram
    billing_type ||--|| project : project_type
    business_unit ||--|| project : under_unit
    domain ||--|| project : belongs_to
    currency ||--|| project : uses_currency
```
