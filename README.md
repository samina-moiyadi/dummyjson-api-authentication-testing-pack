# DummyJSON API Authentication Testing Pack

A Postman API testing collection focused on authentication scenarios for QA practice and portfolio use.

**Version:** v1.0 – Authentication Testing Pack

---

## Collection Overview

This collection validates **authentication-related** API behavior using the DummyJSON API.

It includes:

- Login with valid credentials
- Login failures with invalid or missing data
- Method validation and payload validation
- Edge cases such as extra parameters and incorrect request formats
- SQL Injection attempt in login credentials

Each request contains:

- Correct HTTP method usage
- Automated tests for status code validation
- Assertions for response body and error handling
- Clear separation of positive and negative scenarios

---

## Folder Structure
```text
DummyJSON Auth – Executed Core Scenarios
└── Authentication
   ├── AUTH_001 - Login - Valid Credentials
   ├── AUTH_002 - Login - Invalid Password
   ├── AUTH_003 - Login - Invalid Username
   ├── AUTH_004 - Login - Missing Password
   ├── AUTH_005 - Login - Missing Username
   ├── AUTH_006 - Login - Empty Payload
   ├── AUTH_007 - Login with Extra Parameters
   ├── AUTH_008 - Login - Wrong HTTP Method
   ├── AUTH_009 - Login with Malformed JSON
   └── AUTH_010 - Login - SQL Injection Attempt
```
---

## Environment Variables

**Environment Name:** `DummyJSON_Env`

| Variable   | Value                  | Description                 |
|-----------|-----------------------|----------------------------|
| base_url  | https://dummyjson.com  | Base URL for API requests   |

Using environment variables allows requests to be reused easily across environments and collections.

---

## Authentication Details

- **Endpoint**: /auth/login
- **Method**: POST
- **Authentication Type**: Token-based (JWT returned on successful login)

Valid credentials are sourced from the official DummyJSON documentation and are used strictly for testing/demo purposes.

---

## How to Use

1. Import the collection into Postman Web: [https://web.postman.co](https://web.postman.co)  
2. Create or import the environment `DummyJSON_Env` and set `base_url`.  
3. Select the collection → select a request → click **Send**.  
4. Observe the response and validation results in the **Tests** tab.  

---

## Positive & Negative Testing Coverage

**Positive Scenario**

- **Login - Valid Credentials**
  - Status Code: 200 OK
  - JWT token present in response
  - User details returned

**Negative & Validation Scenarios**

- Invalid username or password → 400
- Missing mandatory fields → 400
- Empty payload or malformed JSON → 400
- Incorrect HTTP method → 404 / 405
- SQL Injection attempt → 400

These scenarios demonstrate how APIs handle incorrect input, validation gaps, and unexpected client behavior.

Assertions validate response behavior without relying on exact error messages, ensuring resilience against backend message changes.

---

## Purpose of This Pack

This collection is designed to showcase:
- Practical API testing skills
- Understanding of authentication flows
- Clear separation of positive vs negative testing
- Real-world QA validation mindset

This is the initial stable version (v1.0) of the authentication testing pack.
It is suitable for **QA portfolios, interview discussions, and freelance proof-of-work and reusable starter packs for API testing projects**.

## Author

**Samina Moiyadi** – ISTQB Advanced-certified QA professional building portfolio-ready API and automation testing assets.
