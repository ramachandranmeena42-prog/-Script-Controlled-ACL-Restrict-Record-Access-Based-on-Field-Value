# Phase 1 – Brainstorming & Ideation

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. Problem Identification

In ServiceNow, users may have access to records based on roles and permissions. However, in some situations, record access must also depend on the value of a particular field.

For example, certain records may contain sensitive information and should only be accessible when a specific field value satisfies an access condition.

## 2. Proposed Idea

The proposed project uses a Script-Controlled Access Control List (ACL) in ServiceNow to dynamically control record access based on a field value.

A server-side ACL script will evaluate the field value and determine whether the current user should be allowed to access the record.

## 3. Project Objective

The main objective is to implement a dynamic record-level access control mechanism using a scripted ACL.

The system should:

- Check a specific field value.
- Evaluate the current user's access.
- Allow authorized access.
- Restrict unauthorized access.
- Provide dynamic security at record level.

## 4. Motivation

Traditional role-based access may not be sufficient for every business requirement.

A scripted ACL provides additional control by allowing access decisions to depend on record data and user context.

## 5. Proposed Solution

A ServiceNow ACL will be configured for the selected table and operation.

The ACL script will evaluate the required field value and determine whether access should be granted.

### Basic Logic

User requests record
        ↓
ACL is evaluated
        ↓
Field value is checked
        ↓
Access condition satisfied?
      /       \
    Yes        No
     ↓          ↓
Access      Access
Allowed     Denied

## 6. Expected Benefits

- Improved record-level security
- Dynamic access control
- Reduced unauthorized access
- Flexible security rules
- Better control over sensitive records

## 7. Expected Outcome

The project will demonstrate how a Script-Controlled ACL can restrict access to ServiceNow records based on a field value.

## 8. Conclusion

The brainstorming phase establishes the need for dynamic record-level access control and proposes a scripted ACL solution to address the requirement.
