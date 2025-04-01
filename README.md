# LinqtestingLucyrayala
# Linq Application Testing Documentation

This document contains testing information for the Linq application, including exploratory testing notes, test cases for adding a contact, and Postman API testing notes.

## Table of Contents

1.  [Exploratory Testing: Onboarding Page](#exploratory-testing-onboarding-page)
2.  [Test Cases: Adding a Contact](#test-cases-adding-a-contact)
3.  [API Testing: Contacts API](#api-testing-contacts-api)

## 1. Exploratory Testing: Onboarding Page

Exploratory testing was conducted on the Linq onboarding page to identify potential usability issues, bugs, and areas for improvement. [cite: 1, 2, 3, 4]

###   Areas of Focus

The testing focused on the following areas:

* Content Clarity and Relevance [cite: 3]
* Navigation and Flow [cite: 4]
* Visual Design and Layout [cite: 4]
* Functionality [cite: 5]

###   Testing Notes

The following observations, questions, test ideas, and potential issues were noted:

* **"Hi, Lucy" Greeting:** The page greets the user by name, suggesting personalization. [cite: 5, 6] It is unclear if the name is dynamically populated. [cite: 6, 7, 8]
* **"Take Control" Section:** This section outlines steps with a progress bar. [cite: 9, 10] The specific steps and their clarity were questioned. [cite: 9, 10, 11, 12]
* **"How will your team use Linq primarily?" Section:** This section presents five options for selecting the primary use of Linq. [cite: 13, 14, 15, 16] The selection mechanism's clarity was questioned. [cite: 13, 14, 15, 16]
* **LinqOne Welcome Image:** A large image is displayed, and its relevance to onboarding was questioned. [cite: 17, 18, 19, 20]
* **"Live Training" Button:** The destination and content of the training were questioned. [cite: 21, 22, 23, 24]
* **Lucy Rayala (User Profile):** The relevance of the admin status during onboarding was questioned. [cite: 25, 26, 27, 28]
* **Navigation Menu:** The relevance of the navigation options to the onboarding process was questioned. [cite: 29, 30, 31, 32]
* **Overall Flow:** The logical flow and completeness of the onboarding steps were questioned. [cite: 32, 33, 34, 35]

###   Potential Bugs and Issues

The following potential issues were identified:

* Unclear step descriptions in the "Take Control" section [cite: 35, 36]
* Ambiguous selection mechanism in the "How will your team use Linq primarily?" section [cite: 36, 37]
* Irrelevant or distracting welcome image [cite: 36, 37]
* Potentially non-functional "Live Training" button [cite: 37]
* Overwhelming navigation menu during onboarding [cite: 37, 38, 39]

###   Further Testing

Further testing was recommended, including:

* Interacting with page elements [cite: 38, 39]
* Testing on different browsers and devices [cite: 38, 39]
* Considering accessibility for users with different technical abilities [cite: 38, 39]
* Documenting bugs and issues [cite: 38, 39]

## 2. Test Cases: Adding a Contact

This section details test cases for adding a contact in the Linq application. [cite: 40, 41, 42, 43, 44, 45, 46, 47, 48, 49]

###   Test Case 1: Basic Contact Creation (Successful Path)

* **Test ID:** TC\_Contact\_001 [cite: 40, 41, 42, 43, 44, 45, 46, 47, 48, 49]
* **Test Title:** Create a new contact with valid details. [cite: 40, 41, 42, 43, 44, 45, 46, 47, 48, 49]
* **Preconditions:** User is logged in, and on the "Contacts" page. No contact named "Sriram" exists. [cite: 41, 42, 43, 44, 45, 46, 47, 48, 49]
* **Test Steps:** Navigate to "Contacts," click "Add Contact," enter "Sriram" in the name field, enter other details, and click "Save." [cite: 43, 44, 45, 46, 47, 48, 49]
* **Expected Result:** Contact is created, appears in the contact list, details page is displayed, and a success message appears. [cite: 47, 48, 49]
* **Pass/Fail:** Pass if all results are met, fail otherwise. [cite: 49]

###   Test Case 2: Contact Creation with Missing Name

* **Test ID:** TC\_Contact\_002 [cite: 50, 51, 52, 53, 54, 55]
* **Test Title:** Attempt to create a contact without entering a name. [cite: 50, 51, 52, 53, 54, 55]
* **Preconditions:** User is logged in and on the "Contacts" page. [cite: 51, 52, 53, 54, 55]
* **Test Steps:** Navigate to "Contacts", click "Add Contact", leave the name field blank, enter other details, and click "Save". [cite: 51, 52, 53, 54, 55]
* **Expected Result:** An error message is displayed, and the contact is not created. [cite: 53, 54, 55]
* **Pass/Fail:** Pass if the error message is displayed and the contact is not created, fail otherwise. [cite: 55]

###   Test Case 3: Contact Creation with Duplicate Name

* **Test ID:** TC\_Contact\_003 [cite: 56, 57, 58, 59, 60, 61, 62]
* **Test Title:** Attempt to create a contact with a name that already exists. [cite: 56, 57, 58, 59, 60, 61, 62]
* **Preconditions:** User is logged in and on the "Contacts" page. A contact named "Sriram" already exists. [cite: 57, 58, 59, 60, 61, 62]
* **Test Steps:** Navigate to "Contacts," click "Add Contact," enter the existing name, enter other details, and click "Save." [cite: 58, 59, 60, 61, 62]
* **Expected Result:** An error message is displayed, and the contact is not created. [cite: 60, 61, 62]
* **Pass/Fail:** Pass if the error message is displayed and the contact is not created, fail otherwise. [cite: 62]

###   Test Case 4: Contact Creation with Special Characters

* **Test ID:** TC\_Contact\_004 [cite: 63, 64, 65, 66, 67, 68, 69]
* **Test Title:** Create a contact with special characters in the name. [cite: 63, 64, 65, 66, 67, 68, 69]
* **Preconditions:** User is logged in and on the "Contacts" page. [cite: 64, 65, 66, 67, 68, 69]
* **Test Steps:** Navigate to "Contacts," click "Add Contact," enter a name with special characters, enter other details, and click "Save." [cite: 64, 65, 66, 67, 68, 69]
* **Expected Result:** Contact is created (or an error message is displayed), and special characters are displayed correctly. [cite: 67, 68, 69]
* **Pass/Fail:** Pass if the contact is created or an appropriate error message is shown, fail otherwise. [cite: 69]

###   Test Case 5: Contact Creation with Long Name

* **Test ID:** TC\_Contact\_005 [cite: 70, 71, 72, 73, 74, 75, 76]
* **Test Title:** Create a contact with a very long name. [cite: 70, 71, 72, 73, 74, 75, 76]
* **Preconditions:** User is logged in and on the "Contacts" page. [cite: 71, 72, 73, 74, 75, 76]
* **Test Steps:** Navigate to "Contacts," click "Add Contact," enter a very long name, enter other details, and click "Save." [cite: 71, 72, 73, 74, 75, 76]
* **Expected Result:** Contact is created with the name truncated, or an error message is displayed. [cite: 74, 75, 76]
* **Pass/Fail:** Pass if the long name is handled correctly, fail otherwise. [cite: 76]

## 3. API Testing: Contacts API

This section details Postman tests for the Linq Contacts API. [cite: 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]

###   GET Contacts API

* **Endpoint URL:** `https://linqapp.com/admin/22407/contacts` [cite: 77, 78, 79, 80, 81, 82, 83, 84, 85]
* **Method:** GET [cite: 77, 78, 79, 80, 81, 82, 83, 84, 85]
* **Headers:** `Content-Type: application/json`, `Authorization: Bearer <your_access_token>` [cite: 77, 78, 79, 80, 81, 82, 83, 84, 85]
* **Post-Response Tests:** Tests for property existence and schema validation. [cite: 77, 78, 79, 80, 81, 82, 83, 84, 85]
* **Test Results:** The API returned HTML instead of JSON. [cite: 79, 80, 81, 82, 83, 84, 85]
* **Issue Identified:** HTML response instead of JSON, possibly due to an incorrect URL, missing authorization, or a server-side issue. [cite: 79, 80, 81, 82, 83, 84, 85]
* **Resolution Steps:** Verify URL, authorization, inspect response body, use `pm.response.text()`, and test in a browser. [cite: 81, 82, 83, 84, 85]

###   POST Contacts API

* **Endpoint URL:** `https://linqapp.com/admin/22407/contacts` [cite: 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Method:** POST [cite: 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Headers:** `Content-Type: application/json`, `Authorization: Bearer <your_access_token>` [cite: 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Request Body (Example):** JSON object with contact details. [cite: 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Post-Response Tests:** Tests for status code, content type, and response time. [cite: 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Test Results:** The API returned a 404 Not Found error and an HTML response. [cite: 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Issue Identified:** 404 error, indicating an incorrect URL or non-existent resource, and an HTML response instead of JSON. [cite: 89, 90, 91, 92, 93, 94, 95, 96, 97]
* **Resolution Steps:** Verify URL, authorization, inspect response body, confirm API permissions, and test in a browser. [cite: 93, 94, 95, 96, 97]
