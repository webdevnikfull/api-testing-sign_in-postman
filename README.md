# 🧪 QA Automation Portfolio: Sign In API Testing & Authentication Validation

> About this repository: This project demonstrates automated API testing and negative validation testing using Postman and JavaScript test scripts (Chai assertions) for user authentication endpoints (Conduit API). It covers authentication error handling, validation messages, and HTTP status code verification (e.g., 422 Unprocessable Entity)[cite: 21]. It also highlights a modern "Shift-Left" QA approach and Continuous Integration (CI/CD) readiness via Newman.

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Newman](https://img.shields.io/badge/Newman-026E42?style=for-the-badge&logo=postman&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

## 🎯 Project Overview

This collection provides automated API test scripts targeting user login endpoints (`https://conduit.mate.academy/api/users/login`)[cite: 21]. It focuses heavily on negative test scenarios, input validation, and proper server error-response formatting.

As a QA Automation / API Testing Engineer, my focus in this repository is to validate authentication error handling, verify strict API contract compliance under incorrect inputs, and write precise Chai assertions for JSON error structures.

## 🛠️ QA Tech Stack & Tools

* **API Testing Tool:** Postman
* **CLI Runner / CI Execution:** Newman
* **Test Assertions & Scripting:** JavaScript (Chai Assertion Library built into Postman)
* **CI/CD Pipeline Support:** GitHub Actions
* **Target Environment:** Conduit Mate Academy API[cite: 21]

## 📊 Test Strategy & Coverage

### 1. Automated Negative API Testing & Assertions
The Postman collection includes structured test suites (`pm.test`) validating:
* **Authentication Error Handling (`Successful Sign In` / Negative Scenario):** Verifies correct handling of incorrect login credentials, expecting an HTTP 422 Unprocessable Entity status, checking error properties for 'email or password', and ensuring unauthorized user payloads are undefined[cite: 21].
* **Non-Existing Email Validation (`Sign In with non-existing email`):** Validates API responses when attempting authentication with an unregistered email, expecting an HTTP 422 status and a precise validation message (`'is invalid'`)[cite: 21].

## 🚀 How to Run the Tests Locally

To run and evaluate this Postman collection locally using Node.js and Newman, follow these steps:

### 1. Prerequisites
Ensure you have Node.js installed, then install Newman globally (if not already installed):
```bash
npm install -g newman
