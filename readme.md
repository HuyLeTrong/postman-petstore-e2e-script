### Petstore E2E Testing - Postman Collection

This is a complete end-to-end API test suit for the Swagger Petstore API, covering authentication, negative testing, and session log out using Postman.

## Prerequisites

Postman installed
Collection file Petstore_E2E_Testing_postman_collection.json downloaded

## Environment Setup

Before running the collection, create a Postman Environment with the following variables:

| Variable | Value | Description |
-----------------------------------------------------------------------------------------------------
| baseUrl | https://petstore.swagger.io/v2 | Base url for the Petstore API |
| api_key | special-key | API key for authenticated endpoints |


## How to Set Up the Environment in Postman
1. Click **Environments** in the left sidebar
2. Click **+** to create a new environment
3. Name it `Pet Store`
4. Add the variables from the table above
5. Click **Save**
6. Select `Pet Store` as the active environment from the top-right dropdown

## How to Import and Run the Collection

1. Click Import in Postman
2. Select Petstore_E2E_Testing_postman_collection.json
3. In the left sidebar, right-click the Petstore E2E Testing collection
4. Select Run Collection
5. Confirm the Pet Store environment is selected
6. Click Run Petstore E2E Testing

## Test Scenarios Covered

| Step | Request | Method | Endpoint |
|---|---|---|---|
| 1 | User Login | GET | `/user/login` |
| 2 | Add New Pet | POST | `/pet` |
| 3 | Verify Pet Exists | GET | `/pet/{petId}` |
| 4 | Update Pet Status | PUT | `/pet` |
| 5 | Verify Pet Updated | GET | `/pet/{petId}` |
| 6 | Delete Pet | DELETE | `/pet/{petId}` |
| 7 | Verify Pet Deleted | GET | `/pet/{petId}` |
| 8 | User Logout | GET | `/user/logout` |

## Expected Results
All 20 tests should pass with 0 failures when the environment is configured correctly.

## Test Results

### Steps 1-3
![Steps 1-3](screenshots/run-results-1.png)

### Steps 4-5
![Steps 4-5](screenshots/run-results-2.png)

### Steps 6-8
![Steps 6-8](screenshots/run-results-3.png)
