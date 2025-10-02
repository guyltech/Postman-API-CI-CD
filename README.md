# Postman-API-CI-CD
API testing and CI/CD practice with Postman and GitHub Actions.  

This project demonstrates how to automate payment API tests (createPaymentProcess) using Postman’s CLI tool Newman, integrated into a CI/CD pipeline.

## 📦 Installation & Setup:

npm install -g newman

newman run tests/Meshulam_Payments.postman_collection.json -e tests/env.json

## ✅ Test Coverage for Critical Features:

The Postman tests cover the main payment flow and critical validations:

Create Valid Payment – valid request returns 200 OK with confirmation.

Create Payment – Missing required field – returns the correct error message.

Create Payment – Sum equals 0 – returns an error and no payment is created.

These three cases ensure coverage of the critical features: successful payment creation, mandatory field validation, and protection against invalid amounts.

## 📊 Future Improvements:

TestRail → I will use this tool because it is very convenient to build a clear tests-tree, and also to see line by line if each test passed or failed.

In addition, it creates a visual pie chart to quickly understand the results. 

Allure Reports → For advanced visual test reports.

## 📝 Explanation of api-tests.yml:

The api-tests.yml file defines a simple GitHub Actions workflow that runs API tests automatically using Postman’s CLI tool Newman.

runs-on: ubuntu-latest → The workflow runs on a temporary Ubuntu server provided by GitHub.

actions/checkout@v2 → Checks out the repository code so the workflow can access files (e.g., the exported Postman collection).

actions/setup-node@v2 → Installs Node.js on the server, required to run Newman.

npm install -g newman → Installs Newman globally on the server.

newman run tests/Meshulam Payments.postman_collection.json → Executes the exported Postman collection, running all defined requests and test scripts.


## Built with ❤️ by Guy Levy
