# Phase 2 – Requirement Analysis

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. Introduction

This phase identifies the functional and non-functional requirements for implementing a Script-Controlled ACL in ServiceNow.

The system will restrict or allow access to records based on the value of a selected field.

## 2. Problem Statement

Role-based access alone may not satisfy situations where access must depend on the data stored in a record.

The project therefore requires a dynamic access control mechanism that evaluates a field value before granting access.

## 3. Proposed System

A scripted Access Control List (ACL) will be configured in ServiceNow.

The ACL script will evaluate:

- The record's field value
- The current user's context
- The required access condition

Based on these conditions, access will either be granted or denied.

## 4. Functional Requirements

### FR1 – Record Access
The system shall control access to records using an ACL.

### FR2 – Field Value Validation
The ACL shall evaluate the value of the configured field.

### FR3 – Access Permission
The system shall allow access when the defined condition is satisfied.

### FR4 – Access Restriction
The system shall deny access when the defined condition is not satisfied.

### FR5 – User Validation
The ACL shall consider the current user's authorization where required.

### FR6 – Dynamic Evaluation
The access decision shall be evaluated dynamically when the record is accessed.

## 5. Non-Functional Requirements

### Security
Unauthorized users should not be able to access restricted records.

### Reliability
The ACL should consistently apply the defined access condition.

### Performance
The ACL script should execute efficiently without unnecessary processing.

### Maintainability
The ACL logic should be clear and easy to maintain.

### Usability
Authorized users should be able to access permitted records normally.

## 6. Actors

### Administrator
- Configure ACL
- Maintain access rules
- Test security behavior

### Authorized User
- Access records that satisfy the access condition

### Unauthorized User
- Should be prevented from accessing restricted records

## 7. Inputs

The ACL may evaluate:

- Selected record field value
- Current user
- User role
- Other required access conditions

## 8. Outputs

The ACL produces an access decision:

- Access Allowed
- Access Denied

## 9. Security Requirements

- Access must be controlled at the ACL level.
- Unauthorized access must be prevented.
- ACL configuration should follow the principle of least privilege.
- Access behavior should be tested using different user scenarios.

## 10. Expected Result

The system should dynamically restrict record access according to the configured field value and access conditions.

## 11. Conclusion

The requirement analysis defines the security, functional, and technical requirements needed to implement the Script-Controlled ACL solution in ServiceNow.
