# Interview 
This project contains some exercises.
The time for these exercises is **one hour**.

## 1. ATM Workflow

Prepare the optimal (effective and efficient) set of test cases required to test this workflow.

The workflow of an ATM is defined by the following rules:

* The ATM goes into the **WORKING** state with the TURN ON action.
* When in the **WORKING** state, the ATM can:
    * ACCEPT CARD which switches it to the **CARD ACCEPTED** state.
    * Start the AUTOMATIC TESTING action which switches it to the **SELF TESTING** state.
* Within **CARD ACCEPTED** the ATM can:
    * CALL POLICE which switches it to the **WAITING POLICE** state.
    * PROCESS TRANSACTION which switches it to the **TRANSACTION PROCESSED** state.
* From the **TRANSACTION PROCESSED** state the ATM goes into the **SELF TESTING** state with the PULL CARD action.
* When in the **SELF TESTING** state, the ATM can either:
    * PASS, which switches it to the **WORKING** state.
    * FAIL, which switches it to the **WAITING SERVICE** state.
* From the **WAITING SERVICE** state, the ATM can either:
    * Be SERVICED, which puts the ATM into the **WORKING** state.
    * Be RETESTED, which returns the ATM to the **SELF TESTING** state.


## 2. Auriga Flight Comparison
This is a sample flight price comparison service. Analyze the [API specifications](flight-comparison-openapi.json) and design a test suite for this endpoint.
```
GET http://localhost/flights/from/{departureCode}/to/{arrivalCode}
```
Finally, implements the test suite using an automation tool. You should use [Postman](https://www.postman.com/) to test and mock the service.

# How to contribute
* Create a branch with your name 
* Solve the exercises
* Commit
* Push
