# User Management API Testing Portfolio

A Postman-based API testing portfolio project by **Vanessa Joy Weng** demonstrating functional and negative testing of the public [DummyJSON Users API](https://dummyjson.com/docs/users).

The project includes 12 test cases with 63 automated assertions, covering CRUD operations, pagination, search, field selection, response validation, collection variables, and simulated data persistence behavior.

## Project Scope

| Folder | Test Cases | Focus |
| --- | --- | --- |
| 01 - Get Users | TC-001–TC-005 | Retrieval, pagination, search, field selection |
| 02 - Create User | TC-006–TC-007 | Simulated creation and non-persistence |
| 03 - Update User | TC-008–TC-009 | Simulated partial update and non-persistence |
| 04 - Delete User | TC-010–TC-011 | Simulated deletion and subsequent retrieval |
| 05 - Negative Testing | TC-012 | 404 handling for nonexistent users |

## Tools and Techniques

- Postman for API request execution and automated validation
- JavaScript assertions using `pm.test` and `pm.expect`
- HTTP methods: GET, POST, PATCH, DELETE
- HTTP status code, response structure, field, and data type validation
- Pagination, search, and request/response consistency checks
- Collection variables for dynamic data handling and cross-request validation
- Positive and negative testing, including simulated CRUD non-persistence verification

## Setup and Execution

1. Import your exported Postman collection JSON into Postman.
2. Set collection variable `baseUrl` to `https://dummyjson.com`.
3. No authentication is required.
4. Run all 12 requests **in collection order**, using one iteration in Collection Runner.
5. Inspect passed, failed, and skipped requests. Record actual results before publishing execution claims.

**Dependencies:** TC-002 provides baseline names for TC-008 and TC-009. TC-006 provides `simulatedUserId` for TC-007. Run TC-010 before TC-011 using the same user ID.

**API limitation:** DummyJSON simulates create, update, and delete responses without permanently modifying its user database. The follow-up tests verify this documented behavior.

## Documentation

For detailed test case descriptions, expected results, validations, and dependencies, refer to the Overview and request descriptions in the Postman collection.

## Test Execution Results

The User Management API collection was executed using Postman Collection Runner on October 17, 2026.

| Metric | Result |
|---|---|
| Total Test Cases | 12 |
| Total Assertions | 63 |
| Passed Assertions | 63 |
| Failed Assertions | 0 |
| Execution Errors | 0 |
| Iterations | 1 |
| Execution Duration | 6.517 seconds |
| Average Response Time | 506 ms |
| Overall Result | **PASS** |

### Execution Evidence

![Postman Collection Runner Results](execution-results/collection-run-summary.png)

### Summary

All 12 API test cases completed successfully, with 63 passing assertions and zero failures.

The execution covered user retrieval, pagination, search, field selection, simulated user creation, updates, deletion, non-persistence verification, and negative testing.

**Result: PASS — No assertion failures or execution errors were reported.**

## Reference

[DummyJSON Users API](https://dummyjson.com/docs/users)
