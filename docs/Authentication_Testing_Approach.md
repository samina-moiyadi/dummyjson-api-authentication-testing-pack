# Authentication Testing Approach

This document outlines the testing strategy followed for validating authentication-related APIs using Postman.

## Scope
The authentication testing pack focuses on validating:
- Successful login flows
- Token generation and presence
- Error handling for invalid credentials
- Wrong HTTP Method
- Malformed request payloads
- Basic security-related negative scenarios (e.g., SQL injection attempts)

## Test Design
- Test cases were first designed in Excel to ensure clear coverage and traceability.
- Scenarios include both positive and negative cases.
- Edge cases were intentionally included to validate API resilience.

## Automation & Validation
- Postman collections were created based on the designed test cases.
- Assertions validate response behavior without relying on exact error messages, ensuring resilience against backend message changes.
- Environment variables are used where applicable to improve reusability.

## Outcome
This pack demonstrates practical backend QA skills relevant to Manual QA and API Testing roles, with emphasis on real-world authentication scenarios.
