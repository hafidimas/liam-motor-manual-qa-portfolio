# Manual Software QA Portfolio — Liam Motor

## About This Portfolio

Welcome to my Manual Software Quality Assurance (QA) portfolio.

This repository showcases my practical knowledge of manual software testing through **Liam Motor**, a web-based workshop inventory management application. The project focuses on evaluating application functionality, validating user inputs, verifying data consistency, and identifying potential defects through structured manual testing. Through this project, I aim to demonstrate my ability to analyze application workflows, design effective test cases, execute test scenarios, document test results, and report defects clearly and systematically.

## Project Overview

| Information | Details |
|---|---|
| Project Name | Liam Motor |
| Application Type | Workshop Inventory Management Website |
| Testing Type | Manual Software Testing |
| Role | Manual QA Tester |
| Testing Approach | Functional, Positive, Negative, and Exploratory Testing |
| Project Status | In Progress |

**Application Under Test:** Liam Motor

The application is used as a testing subject to evaluate workshop inventory management workflows. The actual testing scope is based on the functionality available in the application.

## Testing Objectives

The objectives of this project are to:

- Verify that available application features function according to their expected behavior.
- Validate user inputs and business rules.
- Identify functional defects and unexpected application behavior.
- Verify inventory data consistency after supported operations.
- Evaluate error handling for invalid inputs and unsuccessful operations.
- Document test cases, execution results, and reproducible defects.
- Apply fundamental manual QA methodologies in a practical project.

## Scope of Testing

The following areas are considered for testing, subject to the features available in Liam Motor.

| Test Area | Description |
|---|---|
| Authentication | Validate login, logout, and session handling, if available. |
| Dashboard | Verify displayed information, navigation, and summary data, if available. |
| Inventory Management | Test creating, viewing, updating, and deleting inventory records, if supported. |
| Stock Validation | Verify stock quantity rules and the handling of invalid quantities. |
| Search and Filtering | Validate search results and filtering behavior, if available. |
| Input Validation | Test required fields, invalid formats, boundary values, and duplicate entries. |
| Data Integrity | Verify data consistency after supported operations. |
| Error Handling | Verify validation messages and behavior when operations cannot be completed. |
| Access Control | Verify role-based permissions, if multiple user roles are supported. |
| Reporting | Validate reports and exported data, if available. |

## Testing Methodology

### 1. Requirement Analysis
Review the available features, application behavior, and expected outcomes to identify testing requirements.

### 2. Workflow Analysis
Identify important user workflows and the relationships between application features.

### 3. Test Scenario Design
Create high-level test scenarios based on the application's functionality and business processes.

### 4. Test Case Design
Develop detailed test cases containing preconditions, test steps, test data, expected results, and execution status.

### 5. Test Execution
Execute the test cases manually and document the actual results with supporting evidence.

### 6. Defect Reporting
Report confirmed defects with clear reproduction steps, expected results, actual results, severity, priority, and screenshots when available.

### 7. Test Summary
Summarize execution progress, test results, identified defects, and outstanding testing risks.

## Test Design Techniques

The following test design techniques may be applied when relevant to the application:

- **Positive Testing:** Verify that the application processes valid inputs correctly.
- **Negative Testing:** Verify that the application handles invalid inputs and unexpected conditions appropriately.
- **Equivalence Partitioning:** Divide input data into valid and invalid classes.
- **Boundary Value Analysis:** Test values at and around defined input limits.
- **Decision Table Testing:** Verify combinations of conditions and business rules.
- **State Transition Testing:** Validate changes between application states following user actions.
- **Exploratory Testing:** Investigate unexpected behavior beyond predefined test cases.

## Test Deliverables

The repository is organized to maintain structured and traceable QA documentation.

| Folder / File | Description |
|---|---|
| `README.md` | Project overview, testing objectives, approach, and scope. |
| `test-plan/` | Test objectives, scope, strategy, assumptions, and entry/exit criteria. |
| `test-scenarios/` | High-level scenarios representing application workflows. |
| `test-cases/` | Detailed test cases, test data, steps, and expected results. |
| `bug-reports/` | Defect reports and reproduction steps. |
| `test-evidence/` | Screenshots and evidence collected during execution. |
| `test-summary/` | Test execution results, defect statistics, and outstanding risks. |

Each folder will contain the relevant documentation as the project progresses.

## Test Case Documentation

Each test case is structured to include the following information:

- Test Case ID
- Test Scenario
- Test Case Description
- Preconditions
- Test Steps
- Test Data
- Expected Result
- Actual Result
- Execution Status (Not Executed, Pass, Fail, or Blocked)
- Evidence and Remarks

## Defect Reporting

Defects confirmed during testing will be documented to support investigation and resolution.

Each defect report may include:

- Bug ID and Summary
- Environment and Preconditions
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity and Priority
- Supporting Screenshots
- Defect Status

Only issues observed during actual execution will be reported as confirmed defects. Potential issues that have not been reproduced will be documented separately.

## Tools and Technologies

- **Web Browser:** Manual application testing.
- **Microsoft Excel / Google Sheets:** Test case design and execution tracking.
- **GitHub:** QA documentation management and portfolio publication.
- **Screenshot Tools:** Capturing test evidence and defect screenshots.

Additional tools will be documented if they are used during the testing process.

## Test Environment

The test environment will be recorded during execution and may include:

- Application URL
- Browser and version
- Operating system
- Test execution date
- Test account and user role, where applicable
- Relevant environment configuration

Credentials, confidential information, and sensitive production data will not be published in this repository.

## Test Execution Status

This project is in progress. Test results, execution statistics, and defect counts will be updated as testing activities are performed.

Test cases that have not been executed will be marked **Not Executed**. Pass and Fail statuses will be assigned based on comparisons between actual and expected results.

The documented results represent the scope and evidence collected during testing and do not imply that every application feature has been exhaustively tested.

## Key Learning Outcomes

This project helps me develop practical skills in:

- Manual Software Testing
- Test Planning and Test Design
- Positive and Negative Testing
- Functional Testing and Regression Testing
- Input Validation and Data Integrity Testing
- Bug Reporting and Defect Severity Assessment
- Test Execution and Result Tracking
- Structured QA Documentation

## Disclaimer

This repository is intended for learning, practice, and professional portfolio purposes.

Testing activities are limited to authorized access and the features available in Liam Motor. The testing documentation reflects the scope, execution status, and evidence recorded during the project.

This portfolio does not claim that Liam Motor has undergone a complete security audit or that all possible defects have been identified.

---

**Author:** [Your Name]  
**Role:** Aspiring Manual Software QA Engineer  
**GitHub:** [Your GitHub Profile URL]
