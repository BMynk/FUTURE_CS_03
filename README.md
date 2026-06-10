# FUTURE_CS_03 – API Security Risk Analysis

**CIN:** FIT/MAY26/CS8295  
**Intern:** Mishael Kwaku Yeboah  
**Date:** June 2026  
**APIs tested:** JSONPlaceholder, Fake Store API, DummyJSON

## Summary
This repository contains my Task 3 submission for the Cyber Security Internship at Future Interns.

## Findings
| # | Finding | Severity |
|---|---------|----------|
| 1 | Missing Authentication – No API keys or tokens required | Critical |
| 2 | Excessive Data Exposure – Email, phone, address exposed | High |
| 3 | IDOR – Access any user by changing ID in URL | Critical |
| 4 | Lack of Rate Limiting – No 429 error after rapid requests | Medium |
| 5 | Weak Input Validation – Empty parameter returns user 1 instead of 404 | Low |

## Files in this repository
- `Mishael_Yeboah_Task3_API_Security_Report.pdf` – Final report
- `postman_user1_response.png` – Screenshot of user 1 data
- `postman_user2_response.png` – Screenshot of user 2 data
- `postman_user3_response.png` – Screenshot of user 3 data
- `excessive_data_exposure.png` – Highlighted sensitive fields
- `rate_limiting_test.png` – Evidence of no rate limiting
- `input_validation_empty.png` – Empty parameter test
- `input_validation_long_id.png` – Long ID test (404)
- `input_validation_xss.png` – XSS test (404)

## Recommendations
- Implement API keys or OAuth2 tokens
- Add object-level access control to prevent IDOR
- Filter sensitive fields (email, phone, address)
- Add rate limiting with 429 responses
- Validate all inputs; reject invalid parameters
