# Phase 3 – Project Design

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. System Design

The system uses a Script-Controlled Access Control List (ACL) in ServiceNow to dynamically control record access.

The ACL evaluates the configured field value and determines whether the current user should be allowed to access the record.

## 2. Access Control Flow

The access flow is:

User requests record  
↓  
ServiceNow evaluates ACL  
↓  
ACL checks required conditions  
↓  
Field value is evaluated  
↓  
Access condition satisfied?  
↓  
Yes → Access Allowed  
No → Access Denied

## 3. ACL Components

### User

The user attempts to access a ServiceNow record.

### ACL

The Access Control List evaluates whether the user is permitted to access the record.

### Record Field

The configured field value is checked by the ACL logic.

### Script

The script dynamically determines whether access should be allowed or denied.

## 4. Script Logic

The basic logic is:

```text
IF required access condition is satisfied
    Allow access
ELSE
    Deny access
