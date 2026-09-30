# Phase 5 – Project Development

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. Development Objective

The objective of this phase is to implement a Script-Controlled Access Control List (ACL) in ServiceNow.

The ACL will evaluate a selected record field value and determine whether the current user should be allowed to access the record.

## 2. Development Environment

The project is developed using:

- ServiceNow Developer Instance
- Access Control List (ACL)
- ServiceNow Script Editor
- Test Users
- Test Records

## 3. ACL Configuration

The ACL is configured to control access to the selected ServiceNow record.

The ACL contains:

- Target table
- Access operation
- Required conditions
- Scripted access logic

## 4. Access Control Logic

The ACL follows this logic:

```text
User requests record
        ↓
ServiceNow evaluates ACL
        ↓
Configured field value is checked
        ↓
Is the access condition satisfied?
        ↓
   Yes          No
    ↓            ↓
Access Allowed  Access Denied
