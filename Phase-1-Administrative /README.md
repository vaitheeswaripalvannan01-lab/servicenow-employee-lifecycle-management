
# Employee Lifecycle Management – Phase 1

## Overview

Employee Lifecycle Management is a custom ServiceNow application designed to manage employee onboarding and offboarding requests.

Phase 1 focuses on application creation, table configuration, form design, data lookup rules, dot-walking, and other administrative configurations.

---

## 1. ServiceNow Studio

**Objective**

To create a dedicated scoped application for managing employee lifecycle requests.

**Implementation**
- Opened ServiceNow Studio.
- Created a new scoped application named Employee Lifecycle Management.
- Configured the application details and scope.

**Outcome**

Successfully created a dedicated scoped application to manage employee onboarding and offboarding processes.

<img width="1501" height="655" alt="servicenow studio application" src="https://github.com/user-attachments/assets/79f6b11f-1bf6-41cc-8b35-24b403bcb82f" />


---

## 2. Custom Table Creation

**Objective**

To create a custom table for storing employee lifecycle request information.

**Implementation**
- Created a custom table named Employee Lifecycle.
- Configured the required employee-related fields.
- Enabled automatic number generation for the table.
- Configured unique request numbers for each record.

**Outcome**

Successfully created the Employee Lifecycle table to store and manage employee lifecycle records.

<img width="1502" height="813" alt="custom-table" src="https://github.com/user-attachments/assets/ebeecdcc-b2b6-46b8-a4b0-d77e53fe9eae" />


---

## 3. Custom Form Configuration

**Objective**

To design a structured form for managing employee lifecycle requests.

**Implementation**
- Created and configured the Employee Lifecycle form.
- Added the required employee and request-related fields.
- Arranged the fields in an organized layout.
- Added the Process Flow Formatter to visually represent the different stages of the employee lifecycle process.

**Outcome**

Successfully designed an organized employee lifecycle form with a visual representation of the request process.

<img width="1502" height="813" alt="custom-table" src="https://github.com/user-attachments/assets/1b22528e-46f1-4f30-a1ed-35e56c7340c1" />


---

## 4. Data Lookup Rule

**Objective**

To automatically populate the Assignment Group based on the selected Department.

**Implementation**
- Created a Data Lookup Rule.
- Configured Department as the lookup condition.
- Mapped the corresponding Assignment Group.
- When a Department is selected, the matching Assignment Group is automatically populated.

**Outcome**

Successfully automated assignment group population based on the selected department, reducing manual assignment.

**Screenshot**

![Data Lookup Rule](./data-lookup-rule.png)

---

## 5. Dot-Walking

**Objective**

To retrieve related email information using reference fields and dot-walking.

**Implementation**
- Configured the required reference field.
- Used dot-walking to access the email field from the referenced Department record.
- When a Department is selected, the related email information is automatically retrieved.

**Outcome**

Successfully implemented dot-walking to access related record information without creating unnecessary duplicate fields.

**Screenshot**

Dot-walking screenshot will be added here.

---

## 6. Knowledge Article Integration

**Objective**

To display relevant Knowledge Articles based on the Short Description.

**Implementation**
- Configured the Short Description field.
- Set up the condition to identify the value "New Hire".
- Configured the relevant Knowledge Article to open when the condition is met.

**Outcome**

Successfully integrated Knowledge Articles with the employee lifecycle request process to provide relevant information to users.

**Screenshot**

![Knowledge Article](./knowledge-article.png)

---

## 7. UI Actions – Onboarding and Offboarding

**Objective**

To display different options based on the selected employee request type.

**Implementation**
- Configured UI Actions for Onboarding and Offboarding.
- Implemented the Onboarding action to display onboarding-related requirements and date information.
- Implemented the Offboarding action to display offboarding-related options.

**Outcome**

Successfully implemented separate actions for handling employee onboarding and offboarding requests.

**Screenshot**

![UI Actions](./Ui-%20actions.png)

---

## 8. UI Action – Pending Approval

**Objective**

To display the Pending Reason field when a request enters the Pending Approval state.

**Implementation**
- Configured the UI Action for the Pending Approval state.
- Implemented the condition to display the Pending Reason field.
- Tested the functionality by changing the request state.

**Outcome**

Successfully implemented the Pending Reason functionality for requests in the Pending Approval state.

**Screenshot**

![Pending Approval UI Action](./Ui-%20actions.png)

---

## 9. Data Policy

**Objective**

To enforce data validation when records are updated through different interfaces, including the list view.

**Implementation**
- Identified a validation issue when updating records through the list view.
- Converted the relevant UI Policy validation into a Data Policy.
- Configured the required validation rules.
- Tested the validation by attempting to update records through the list view.

**Outcome**

Successfully implemented Data Policy validation to prevent invalid record updates through supported interfaces.

**Screenshot**

![Data Policy](./data-policy.png)

---

## 10. ServiceNow Formatters

**Objective**

To improve the employee lifecycle form by displaying process information, activity history, and contextual information.

**Implementation**
- Configured the Process Flow Formatter to display the stages of the employee lifecycle process.
- Added the Activity Formatter to display comments and field changes.
- Configured the Contextual Formatter to display relevant contextual information within the form.

**Outcome**

Successfully implemented three types of formatters to improve form usability and provide better visibility into employee lifecycle records.

**Screenshot**

Process Flow, Activity, and Contextual Formatter screenshots will be added here.

---

## Project Status

**Phase 1 – Administrative Configuration: Completed**

**Next Phase:** Advanced Development and Automation.
