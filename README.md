# Urban Grocers — API Testing

API testing project for the Urban Grocers backend, focused on validating new functionality for kit management and delivery services.

## Project Overview

The objective of this project was to analyze backend requirements and API documentation, design test scenarios, execute API tests in Postman, and document defects found during testing.

The project focused on two API endpoints:

- `POST /api/v1/kits/{id}/products`
- `POST /order-and-go/v1/delivery`

## Features Tested

### Adding Products to Kits

Endpoint:

`POST /api/v1/kits/{id}/products`

Tests covered the behavior of adding products to an existing kit, including:

- Valid product IDs
- Invalid and non-existent product IDs
- Invalid data types
- Product quantity validation
- Boundary values
- Empty values
- Kit capacity limits
- Validation of the 30-product limit

### Delivery Service

Endpoint:

`POST /order-and-go/v1/delivery`

Tests covered delivery availability and cost calculation based on:

- Delivery time
- Number of products
- Product weight
- Host delivery cost
- Client delivery cost
- Boundary values
- Invalid input data

## Testing Approach

The test suite included:

- Positive testing
- Negative testing
- Boundary Value Analysis
- Input validation
- HTTP status code validation
- Response data validation
- Requirements-based testing

## Tools Used

- Postman
- Jira
- API documentation
- HTTP
- JSON
- Google Sheets

## Test Results

A total of **51 test cases** were executed.

| Feature | Test Cases | Passed | Failed |
|---|---:|---:|---:|
| Add products to kits | 21 | 9 | 12 |
| Delivery service | 30 | 23 | 7 |
| **Total** | **51** | **32** | **19** |

During testing, **19 defects were identified and documented in Jira**.

Examples of issues found included:

- Invalid product IDs returning `200 OK` or `500 Internal Server Error` instead of the expected `400 Bad Request`
- Invalid product quantities being accepted
- Incorrect validation of kit product limits
- Incorrect delivery cost calculations
- Requests with boundary values returning unexpected responses

## My Responsibilities

- Analyzed backend requirements and API documentation
- Designed test cases based on requirements
- Applied positive, negative, and boundary value testing techniques
- Executed requests using Postman
- Validated HTTP status codes and API responses
- Compared actual results against expected results
- Identified backend defects
- Created bug reports in Jira

## Repository Contents

- Test checklist with executed test cases
- Expected and actual results
- Test status
- Bug references
- API request examples

## Skills Demonstrated

- API Testing
- Postman
- Test Case Design
- Requirements Analysis
- Boundary Value Analysis
- Negative Testing
- HTTP
- JSON
- Bug Reporting
- Jira
