# Test Cases: User Authentication

| Test Case ID | Scenario | Pre-Conditions | Test Steps | Expected Result | Status | Bug ID |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-AUTH-01** | Login with valid credentials | User is on login page | 1. Enter `standard_user`<br>2. Enter `secret_sauce`<br>3. Click Login | Redirected to `/inventory.html` and product grid is displayed | **PASS** | N/A |
| **TC-AUTH-02** | Login with invalid password | User is on login page | 1. Enter `standard_user`<br>2. Enter `wrong_password`<br>3. Click Login | Red error banner appears: "Username and password do not match..." | **PASS** | N/A |
| **TC-AUTH-03** | Login with locked out user | User is on login page | 1. Enter `locked_out_user`<br>2. Enter `secret_sauce`<br>3. Click Login | Red error banner appears: "Sorry, this user has been locked out." | **PASS** | N/A |
| **TC-AUTH-04** | Login with blank fields | User is on login page | 1. Leave fields empty<br>2. Click Login | Red error banner appears: "Username is required" | **FAIL** | #1 |
