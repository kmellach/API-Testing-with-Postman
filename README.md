# Postman API Automation – Dummy E-Commerce Application
File in Repo:  E2E ECommerce Application.postman_collection.json

## Project Overview

This project is an end-to-end API automation framework built using Postman for a dummy E-Commerce application.
The framework validates core business flows such as product management and order processing, with complete parameterization, token-based authorization, and CI/CD execution using Jenkins.

The project is designed to validate core backend functionalities and ensure API reliability using Postman’s scripting and collection features.


## Scope of Testing

The following E-Commerce functionalities are covered:

* ✅ Create Product
* ✅ Add Product
* ✅ Create Order
* ✅ Get Order Details
* ✅ Delete Order

Each API is validated with **test scripts** for:

* Status code verification
* Response body validation
* Data consistency
* Authorization handling


## Authorization Handling

* Authentication is implemented using **token-based authorization**
* Tokens are passed dynamically through **request headers**
* Authorization is reusable and configurable across environments

## Parameterization

All dynamic data is parameterized using:
Collection variables
Environment variables

Common parameters include:
Product IDs
Order IDs
User data
Authentication tokens

Enables seamless execution across multiple environments

## Test Automation Features

* Postman **Pre-request scripts** for data setup
* **Test scripts** for assertions and validations
* Reusable variables for scalability
* Modular request design for maintainability
* Supports both manual execution and automated runs

## Tools & Technologies Used

1. **Postman** – API design and automation
2. **Newman** – CLI execution of Postman collections
3. **Jenkins** – CI/CD pipeline automation
4. **JavaScript** – Test scripting
5. **REST APIs** – Backend testing

## How to Run the Collection

1. Import the **Postman Collection** into Postman
2. Import the **Environment file**
3. Set the required variables:

   * `baseUrl`
   * `authToken`
4. Run individual requests or execute the entire collection using **Collection Runner**

## Running Tests Using Newman

Execute the collection from command line:
newman run E2E ECommerce Application.postman_collection.json -g 'global variables config (if any)'

## CI/CD Integration with Jenkins

Automated execution configured using Jenkins job
1. Collection runs triggered via SCM -- checks for every 5 mins and SCM initiates a run for the commmits
2. Manual build
3. Test results generated as HTML reports
4. Job configured to support parameterized runs

## Project Highlights

1. End-to-end API automation coverage
2. Token-based secure authorization
3. Fully parameterized and reusable design
4. CLI execution using Newman
5. CI/CD integration with Jenkins
6. Production-ready testing approach

## Future Enhancements
* Negative and edge-case test coverage
* Extended Email Notifications from Jenkins
