# Test Plan for COBOL Application

This test plan outlines the test cases for validating the business logic and implementation of the current COBOL application. Each test case includes details such as pre-conditions, test steps, expected results, and space for recording actual results and status.

---

## Test Cases

| Test Case ID | Test Case Description                          | Pre-conditions                                                                 | Test Steps                                                                                                     | Expected Result                                                                 | Actual Result | Status (Pass/Fail) | Comments |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------|--------------------|----------|
| TC-001       | Validate menu options                         | Application is compiled and running                                           | 1. Launch the application<br>2. Observe the menu options displayed                                              | Menu displays options: 1. View Balance, 2. Credit Account, 3. Debit Account, 4. Exit |               |                    |          |
| TC-002       | View current balance                          | Application is running<br>Default balance is 1000.00                         | 1. Select option 1 (View Balance)<br>2. Observe the displayed balance                                           | Displays "Current balance: 1000.00"                                         |               |                    |          |
| TC-003       | Credit account with valid amount              | Application is running<br>Default balance is 1000.00                         | 1. Select option 2 (Credit Account)<br>2. Enter 500.00<br>3. Observe the updated balance                        | Displays "Amount credited. New balance: 1500.00"                           |               |                    |          |
| TC-004       | Debit account with sufficient funds           | Application is running<br>Default balance is 1000.00                         | 1. Select option 3 (Debit Account)<br>2. Enter 500.00<br>3. Observe the updated balance                        | Displays "Amount debited. New balance: 500.00"                             |               |                    |          |
| TC-005       | Debit account with insufficient funds         | Application is running<br>Default balance is 1000.00                         | 1. Select option 3 (Debit Account)<br>2. Enter 1500.00<br>3. Observe the error message                         | Displays "Insufficient funds for this debit."                              |               |                    |          |
| TC-006       | Exit the application                          | Application is running                                                       | 1. Select option 4 (Exit)<br>2. Observe the application termination message                                     | Displays "Exiting the program. Goodbye!"                                   |               |                    |          |
| TC-007       | Handle invalid menu input                     | Application is running                                                       | 1. Enter an invalid menu option (e.g., 5)<br>2. Observe the error message                                      | Displays "Invalid choice, please select 1-4."                              |               |                    |          |
| TC-008       | Validate balance persistence (in-memory only) | Application is running<br>Default balance is 1000.00                         | 1. Credit account with 500.00<br>2. Restart the application<br>3. View balance                                 | Displays "Current balance: 1000.00" (balance resets on restart)            |               |                    |          |

---

## Notes

- This test plan is designed to validate the current COBOL application's business logic and implementation.
- The "Actual Result" and "Status" columns should be filled during testing.
- Any deviations from the expected results should be documented in the "Comments" column.