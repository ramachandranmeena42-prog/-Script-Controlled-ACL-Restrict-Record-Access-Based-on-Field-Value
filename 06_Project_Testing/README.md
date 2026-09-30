# Phase 6 – Project Testing

## Project Title

Script-Controlled ACL – Restrict Record Access Based on Field Value

## 1. Testing Objective

The objective of this phase is to verify that the Script-Controlled ACL correctly allows or denies record access based on the configured field value.

## 2. Testing Environment

Testing is performed using:

- ServiceNow Developer Instance
- Configured ACL
- Test Records
- Authorized User
- Unauthorized User

## 3. Test Scenarios

### Test Case 1 – Access Allowed

**Condition:** The record field value satisfies the configured access condition.

**Expected Result:**  
The user should be allowed to access the record.

**Status:** Pass

---

### Test Case 2 – Access Denied

**Condition:** The record field value does not satisfy the configured access condition.

**Expected Result:**  
The user should be denied access to the record.

**Status:** Pass

---

### Test Case 3 – Authorized User

**Condition:** An authorized user attempts to access a permitted record.

**Expected Result:**  
The user should be able to access the record.

**Status:** Pass

---

### Test Case 4 – Unauthorized User

**Condition:** An unauthorized user attempts to access a restricted record.

**Expected Result:**  
The user should not be able to access the restricted record.

**Status:** Pass

---

### Test Case 5 – Different Field Values

**Condition:** Records containing different field values are accessed.

**Expected Result:**  
The ACL should evaluate each record according to the configured field-based condition.

**Status:** Pass

## 4. Test Case Summary

| Test Case | Scenario | Expected Result | Status |
|---|---|---|---|
| TC01 | Allowed field value | Access Allowed | Pass |
| TC02 | Restricted field value | Access Denied | Pass |
| TC03 | Authorized user | Access Allowed | Pass |
| TC04 | Unauthorized user | Access Denied | Pass |
| TC05 | Different field values | Dynamic access decision | Pass |

## 5. Validation

The ACL configuration is validated by testing different users and record values.

The test verifies that:

- The ACL is active.
- The configured field is evaluated.
- Valid access conditions allow access.
- Invalid access conditions restrict access.
- Access behavior is applied dynamically.

## 6. Security Testing

Security testing verifies that unauthorized users cannot access records that do not satisfy the configured access condition.

The ACL is also checked to ensure that authorized users can access permitted records.

## 7. Expected Testing Result

The ACL should consistently provide the correct access decision based on the configured field value and access conditions.

## 8. Conclusion

The Project Testing phase verifies the functionality and security of the Script-Controlled ACL.

Successful testing confirms that the ACL can dynamically restrict or allow record access based on the configured field value.
