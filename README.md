# Postman-API-CI-CD
API testing and CI/CD practice with Postman and GitHub Actions.  

Explanation of api-tests.yml:

The api-tests.yml file defines a simple GitHub Actions workflow that runs API tests automatically using Postman’s CLI tool Newman.

runs-on: ubuntu-latest → The workflow runs on a temporary Ubuntu server provided by GitHub.

actions/checkout@v2 → Checks out the repository code so the workflow can access files (e.g., the exported Postman collection).

actions/setup-node@v2 → Installs Node.js on the server, required to run Newman.

npm install -g newman → Installs Newman globally on the server.

newman run tests/Meshulam Payments.postman_collection.json → Executes the exported Postman collection, running all defined requests and test scripts.

This workflow demonstrates a basic CI/CD integration where API tests are automatically executed whenever new code is pushed to the repository.
