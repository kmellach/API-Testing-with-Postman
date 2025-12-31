# API Automation Projects – Postman | Newman | Jenkins

This repository contains API automation frameworks built using Postman, with CLI execution via Newman and CI/CD integration using Jenkins.
The projects demonstrate real-world API testing practices including token-based authorization, multi-environment execution, data-driven testing, and automated reporting.

## Project 1: Dummy E-Commerce API Automation
### Overview
End-to-end API automation for a dummy E-Commerce application validating product and order workflows using Postman.

### Features Covered
1. Create Product
2. Create Order
3. Get Order Details
4. Delete Order
5. Delete Product

### Authorization
1. Token-based authentication
2. Tokens passed dynamically via headers

### Parameterization
1. Collection & environment variables
2. Reusable and environment-agnostic design

### Execution
1. Manual execution via Postman
2. CLI execution via Newman
3. Automated execution using Jenkins (SCM-triggered & manual)

## Project 2: Library Management API Automation
### Overview
API automation framework for a Library Management system with multi-environment support, global variables, and data-driven execution.

### Features Covered
1. Add Book
2. Get Book Details
3. Delete Book

### Multi-Environment Support
* Dev / QA environments
* Environment switching without code changes

### Data-Driven Testing
1. External data files for multiple test scenarios
2. Scalable execution using Newman

### Common Tools & Technologies
1. Postman – API design & automation
2. Newman – CLI execution
3. Jenkins – CI/CD pipeline
4. JavaScript – Test scripting
5. REST APIs – Backend testing

### Running Tests Using Newman
1. E-Commerce Project: 
newman run E2E ECommerce Application.postman_collection.json -r htmlextra

2. Library Project: 
newman run Library.postman_collection.json
-e  QA.postman_environment.json
-g workspace.postman_globals.json
-d Books_Data.csv
-r htmlextra

### CI/CD Integration with Jenkins
1. Jenkins jobs configured on local Jenkins server
2. Builds triggered via:
 a. Poll SCM (every 5 minutes)
 b. Manual build
3. Jobs support:
 a. Parameterized execution
 b. Environment selection

HTML reports generated and archived per build

### Reporting
Newman HTML reports generated after each execution
Reports stored in Jenkins workspace
Accessible via Jenkins build history

## Highlights
1. Multiple projects in a single repository
2. Real-world API automation scenarios
3. CI/CD-ready framework
4. Parameterized and reusable test design

## Future Enhancements
1. Allure report integration
2. Negative and edge-case validations
3. Dockerized execution
4. GitHub Actions integration
