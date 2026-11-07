# Employee Lifecycle Management – Phase 1

## Overview

Phase 1 focuses on building the foundation of the Employee Lifecycle Management application in ServiceNow. This includes scoped application creation, custom table configuration, form design, data lookup rules, and dot-walking.

---

## 1. ServiceNow Studio – Application Creation

### Objective
To create a dedicated scoped application for managing employee lifecycle requests.

### Implementation
- Opened ServiceNow Studio.
- Created a new scoped application named **Employee Lifecycle Management**.
- Configured the application scope and basic application details.

### Outcome
Successfully created a dedicated application to organize employee onboarding and offboarding functionality.

### Screenshot
![ServiceNow Studio Application](servicenow%20studio%20application.png)

---

## 2. Custom Table Creation

### Objective
To create a custom table for storing employee lifecycle request information.

### Implementation
- Created a custom table named **Employee Lifecycle**.
- Configured the required fields to capture employee-related information.
- Enabled automatic number generation to assign unique request numbers to records.

### Outcome
Successfully created the Employee Lifecycle table to store and manage employee lifecycle records with automatically generated request numbers.

### Screenshot
![Custom Table Configuration](custom-table.png)

---

## 3. Custom Form Configuration

### Objective
To design a structured form for managing employee lifecycle requests.

### Implementation
- Configured the Employee Lifecycle form.
- Added and arranged the required fields.
- Organized employee and request-related information.
- Implemented the **Process Flow Formatter** to visually represent the different stages of the employee lifecycle process.

### Outcome
Created a structured form with an improved user interface and a visual representation of the request lifecycle.

### Screenshot
![Employee Lifecycle Form](employee-form.png)

---

## 4. Data Lookup Rule – Automatic Assignment Group Population

### Objective
To automatically populate the Assignment Group based on the selected Department.

### Implementation
- Configured a Data Lookup Rule.
- Defined the Department as the lookup condition.
- Mapped the corresponding Assignment Group.
- When a user selects a Department, the corresponding Assignment Group is automatically populated.

### Outcome
Reduced manual assignment and ensured that requests are directed to the appropriate assignment group based on the selected department.

### Screenshot
![Data Lookup Rule](data-lookup-rule.png)

---

## 5. Dot-Walking – Automatic Email Retrieval

### Objective
To retrieve related email information using reference fields and dot-walking.

### Implementation
- Configured the required reference field.
- Used dot-walking to access the related email field from the referenced record.
- When the Department is selected, the corresponding email information is automatically retrieved and displayed.

### Outcome
Demonstrated how dot-walking can access related record information without creating unnecessary duplicate fields.

### Screenshot
Add the dot-walking configuration screenshot here.

---

## Phase 1 – Learning Outcomes

- Created a scoped application using ServiceNow Studio.
- Created custom tables and configured fields.
- Designed forms and configured Formatters.
- Implemented automatic field population using Data Lookup Rules.
- Understood and implemented dot-walking with reference fields.

## Project Status

**Phase 1 – Administrative Configuration: In Progress / Implementation documented**
