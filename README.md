
# API Testing with Newman

This project provides automated API testing using [Newman](https://github.com/postmanlabs/newman), the command-line companion for Postman. It is designed to run tests for the API defined in the Postman collection and environment file provided in this repository.

## Prerequisites

Before running the tests, ensure the following are installed on your system:

1. [Node.js](https://nodejs.org/) 
2. [Newman](https://www.npmjs.com/package/newman)

   You can install Newman globally using npm:
   ```bash
   npm install -g newman
   ```

## Project Structure

- `Mock2Full.postman_collection.json`: The Postman collection containing the API test cases.
- `Mock2fullEnv.postman_environment.json`: The Postman environment file with variables for the API endpoints, credentials, etc.
- `newman/`: Directory where the HTML test report will be generated.

## Installation
1. Start MockServer according to this [repo](https://github.com/SharafIbra/Mock-API.git)

2. Clone this repository:
   ```bash
   git clone https://github.com/SharafIbra/Run-APIs-On-Newman.git 

## Running Tests

To execute the API tests and generate an HTML report, run the following command in your terminal:

```bash
newman run Mock2Full.postman_collection.json -e Mock2fullEnv.postman_environment.json -r html --reporter-html-export newman/report.html
```

### Command Breakdown:
- `newman run`: Executes the Newman test runner.
- `Mock2Full.postman_collection.json`: The Postman collection file to test.
- `-e Mock2fullEnv.postman_environment.json`: Specifies the environment file to use.
- `-r html`: Generates an HTML report.
- `--reporter-html-export newman/report.html`: Saves the HTML report to the `newman/` directory.

## Test Report

After running the tests, an HTML report will be generated at:

```
newman/report.html
```

You can open this file in any web browser to view the detailed test results.

---

Happy Testing! 🚀
```
