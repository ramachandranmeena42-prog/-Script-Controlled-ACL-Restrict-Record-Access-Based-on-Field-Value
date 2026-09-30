# Phase 7 – Project Documentation

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. Project Overview

This project implements a Script-Controlled Access Control List (ACL) in ServiceNow.

The ACL dynamically controls record access by evaluating a configured field value and applying the defined access condition.

## 2. Problem Statement

Traditional role-based access may not be sufficient when access to a record depends on the data stored within that record.

This project addresses this requirement by using a scripted ACL to evaluate the record field value before granting access.

## 3. Proposed Solution

A Script-Controlled ACL is configured in ServiceNow.

The ACL evaluates:

- Record field value
- Current user
- Required access condition

Based on the evaluation, access is either allowed or denied.

## 4. System Workflow

```text
User requests record
        ↓
ACL is evaluated
        ↓
Field value is checked
        ↓
Access condition evaluated
        ↓
   Condition satisfied?
       /        \
     Yes         No
      ↓           ↓
Access Allowed  Access Denied
