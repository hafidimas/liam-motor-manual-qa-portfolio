# Test Plan — Liam Motor Workshop Inventory Management System

## 1. Document Information

| Field | Details |
|---|---|
| Project | Liam Motor — Workshop Inventory Management System |
| Document | Manual QA Test Plan |
| Version | 1.0 |
| Prepared by | Manual QA Tester |
| Date | 28 October 2026 |
| Test approach | Manual, risk-based testing |
| Current test status | Planning — execution has not started |

## 2. Project Overview

Liam Motor is presented on its public entry page as **“Bengkel Liam Motor”** with the description **“Sistem Manajemen Stok Barang Bengkel”** (workshop inventory management system). This project documents a manual testing approach for the available application workflows.

The purpose of this test plan is to define the testing objectives, scope, approach, environment, entry and exit criteria, deliverables, risks, and reporting method before test execution begins.

### Application under test

- **Application name:** Liam Motor
- **Current test URL:** <https://curdle-crust-prayer.ngrok-free.dev/william-motor/public/>
- **Access note:** The URL is served through an ngrok tunnel. It may stop working or change when the tunnel is stopped or restarted. Confirm the current URL before testing.
- **Observed public pages:** Login, account registration, and password reset.
- **Inventory/dashboard pages:** Require authenticated access and must be inspected before their exact workflows and coverage can be finalized.

## 3. Initial Inspection Baseline

The following items were visible during an initial inspection of the public pages. Their presence does not mean the forms have been fully tested.

| Page | UI elements observed | Testing status |
|---|---|---|
| Login | Username, password, **Masuk** button, **Lupa Password?** link, **Daftar Akun** link | UI observed; behavior not yet executed |
| Account registration | Full name, username described as unique, password with a minimum of 8 characters, password confirmation, **Daftar Sekarang** button | UI observed; behavior not yet executed |
| Password reset | Username, current password, new password with a minimum of 8 characters, new-password confirmation, **Simpan Password Baru** button | UI observed; behavior not yet executed |
| Dashboard and inventory modules | Not visible without authentication during the public-page inspection | Pending inspection |
| User roles and permissions | Not verified | Pending inspection |

**Important:** Inventory CRUD operations, stock movements, search, reports, dashboard widgets, and role names are candidate areas to investigate, not confirmed features. Keep or remove those areas from the final test scope after inspecting the authenticated application.

## 4. Testing Objectives

The objectives are to:

1. Verify that available application features behave according to their defined requirements and observed expected behavior.
2. Validate authentication, account registration, and password-reset workflows.
3. Verify input validation for required fields, password rules, mismatched confirmation values, and duplicate usernames where applicable.
4. Check that errors are presented clearly and that failed operations do not create unintended changes.
5. Inspect and test the actual inventory-management workflows available after login.
6. Verify data consistency after supported create, view, update, and delete operations, where those operations exist.
7. Check access restrictions and role-based permissions if the application has multiple roles.
8. Record reproducible defects with evidence and communicate their impact clearly.

## 5. Scope of Testing

### 5.1 In scope

Testing will cover the following areas when the feature is available in the application:

- **Public navigation:** Login, registration, password reset, and navigation between these pages.
- **Authentication:** Valid and invalid credentials, empty fields, successful/unsuccessful login, logout, session expiration, and direct access to protected pages.
- **Account registration:** Required fields, username uniqueness, password length, password confirmation, and duplicate-account handling.
- **Password reset:** Correct and incorrect current password, new-password length, confirmation mismatch, and login behavior after a successful reset.
- **Inventory management:** View, create, edit, and delete inventory records, if supported.
- **Stock rules:** Valid quantities, zero and negative quantities, upper/lower boundaries, and stock consistency, according to actual business rules.
- **Search and filtering:** Matching results, no-result states, and filter behavior, if available.
- **Dashboard and reports:** Displayed values and report/export accuracy, if available.
- **Access control:** Access to pages and actions according to verified user roles, if applicable.
- **Error handling and data integrity:** Validation messages, failed-operation handling, duplicate submissions, and persistence of saved data.
- **Basic usability and compatibility:** Layout, readability, and primary workflows in the agreed browser and viewport.

### 5.2 Out of scope

Unless separately agreed, this project does not include:

- Full penetration testing or a formal security audit.
- Load, stress, endurance, or large-scale performance testing.
- Automated UI/API test implementation.
- Source-code review or infrastructure review.
- Testing third-party integrations that are not present or accessible in the observed workflows.
- Testing with real customer data, production credentials, or other sensitive information.

Basic, non-invasive security checks related to authentication and access restrictions may be performed using authorized test accounts. Findings must be documented responsibly.

## 6. Test Approach and Methodology

Testing will be performed manually and prioritized by business impact and risk.

1. **Application walkthrough:** Log in with an authorized test account and record every visible menu, user role, and key workflow.
2. **Requirement and workflow analysis:** Define expected behavior from available requirements, labels, validation messages, and confirmed product behavior. Record unanswered questions as assumptions.
3. **Test scenario design:** Create high-level scenarios for each confirmed workflow.
4. **Test case design:** Specify preconditions, test data, steps, expected results, actual results, status, and evidence reference.
5. **Smoke testing:** Verify that the application opens and critical navigation and login functions are available.
6. **Functional testing:** Validate valid user flows and expected business behavior.
7. **Negative testing:** Try invalid, missing, duplicate, and out-of-range values to check rejection and error handling.
8. **Boundary Value Analysis and Equivalence Partitioning:** Use these techniques for fields with defined minimum, maximum, or accepted-value rules.
9. **State Transition Testing:** Check changes in authentication state and any inventory/status workflow that exists.
10. **Regression testing:** Re-run relevant tests after a defect is fixed or the application changes.
11. **Defect retesting:** Reproduce the original steps and verify that the reported issue is resolved without introducing obvious regressions.

Do not invent expected behavior when requirements are unclear. Record the uncertainty and confirm the expected rule with the application owner before marking a result as Pass or Fail.

## 7. Candidate Test Areas

This table is a working checklist. Areas marked **Pending inspection** must be confirmed against the actual application before they are treated as in-scope features.

| ID | Test area | Priority | Status |
|---|---|---|---|
| TA-01 | Public page loads and navigation | High | UI observed; behavior pending |
| TA-02 | Login validation and authentication | High | UI observed; execution pending |
| TA-03 | Account registration validation | High | UI observed; execution pending |
| TA-04 | Password reset validation | High | UI observed; execution pending |
| TA-05 | Logout and session behavior | High | Pending inspection |
| TA-06 | Protected-page access and authorization | High | Pending login and role inspection |
| TA-07 | Dashboard content and navigation | Medium | Pending inspection |
| TA-08 | Inventory record management | High | Pending inspection |
| TA-09 | Stock quantity/business rules | High | Pending inspection |
| TA-10 | Search and filtering | Medium | Pending inspection |
| TA-11 | Reports and exports | Medium | Pending inspection |
| TA-12 | Responsive layout and basic usability | Medium | Pending execution |
| TA-13 | Error handling and data consistency | High | Pending execution |

Priorities are initial planning estimates and may change after business impact and actual features are confirmed.

## 8. Test Environment

Record the actual environment at execution time.

| Item | Planned value / instruction |
|---|---|
| Application | Liam Motor |
| URL | Current ngrok URL supplied by the application owner |
| Browser | Chrome or another agreed supported browser; record exact version |
| Operating system | Record the operating system and version used for testing |
| Viewport | Record the viewport or screen resolution used |
| Test accounts | Owner-provided or safely created test accounts only |
| Test data | Synthetic/dummy workshop and inventory data only |
| Database access | Not required for normal black-box manual testing unless explicitly authorized |
| Network/tunnel | Confirm ngrok tunnel is running and URL is current before execution |

The ngrok URL may be publicly reachable. Use dummy data, do not expose credentials or production information, and stop the tunnel when it is no longer needed.

## 9. Test Data Guidelines

Prepare data that covers valid, invalid, and boundary conditions without using sensitive real-world data.

- Valid and invalid usernames.
- Passwords below, at, and above the stated minimum length of 8 characters.
- Matching and mismatching password-confirmation values.
- A duplicate username, where duplicate handling can be tested safely.
- Inventory items with valid descriptions or codes, if those fields exist.
- Valid quantities, zero, negative quantities, and boundary values where the business rules define limits.
- Search terms that match a record, partially match a record, and return no results.

Use unique test identifiers so records created during testing can be recognized and removed safely, if deletion is supported and authorized. Do not delete pre-existing user data.

## 10. Entry Criteria

Testing may begin when:

- The application owner has provided authorization to test the environment.
- The application is reachable and the current URL is confirmed.
- Required test accounts and access permissions are available.
- The initial application walkthrough has identified the available modules and roles.
- Test scenarios and test cases have been reviewed sufficiently for execution.
- Safe test data is prepared.

## 11. Exit Criteria

The planned test cycle may be considered complete when:

- All agreed high-priority test cases have an execution status.
- Actual results and evidence are recorded for executed cases.
- All critical/high-severity defects are documented and communicated.
- Failed and blocked cases have clear explanations and follow-up actions.
- Relevant retests and regression checks are completed for fixes made during the cycle.
- A test summary reports coverage, results, known issues, and remaining risks.

Completion of this test cycle does not mean the application is defect-free; it means the agreed scope has been executed and reported.

## 12. Test Case Status Definitions

| Status | Definition |
|---|---|
| Not Executed | The test case has been designed but has not been run. |
| Pass | Actual behavior matches the expected result. |
| Fail | Actual behavior differs from the expected result and the discrepancy is reproducible or sufficiently evidenced. |
| Blocked | Execution cannot proceed because of an environment, access, dependency, or prerequisite issue. |
| Not Applicable | The feature or scenario is confirmed not to apply to the current application scope. |

A test case must not be marked Pass based only on the existence of a page or control.

## 13. Defect Management and Severity

Every confirmed defect should include a unique ID, concise summary, environment, preconditions, steps to reproduce, expected result, actual result, severity, priority (when agreed), evidence, and status.

| Severity | Guideline |
|---|---|
| Critical | The application or a critical workflow is unusable, major data loss occurs, or a serious security/access-control failure is confirmed. |
| High | A major function is broken and there is no reasonable workaround. |
| Medium | A function is partially broken or produces incorrect behavior, but a workaround exists. |
| Low | A minor visual, wording, or usability issue with limited functional impact. |

Severity describes impact. Priority describes how urgently the issue should be addressed and should be agreed with the project owner/team. Do not report a suspected issue as a confirmed defect until it has been observed or reproduced.

## 14. Deliverables

The QA portfolio is expected to contain the following artifacts as the project progresses:

- `README.md` — Portfolio and project overview.
- `test-plan/test-plan.md` — This test plan.
- `test-scenarios/test-scenarios.md` — Confirmed workflows and high-level scenarios.
- `test-cases/test-cases.xlsx` or `.csv` — Detailed test cases and execution results.
- `bug-reports/` — Reproducible defect reports with evidence.
- `test-evidence/` — Screenshots or recordings captured during authorized testing.
- `test-summary/test-summary.md` — Execution summary and residual risks.

Only files and evidence that have actually been created should be listed as completed deliverables in the final portfolio.

## 15. Risks, Assumptions, and Dependencies

| Item | Impact | Mitigation |
|---|---|---|
| The ngrok tunnel may be unavailable or its URL may change. | Testing cannot access the application. | Confirm the active URL immediately before testing and record environment issues. |
| Internal pages are not visible before login. | Inventory scope and role coverage may be incomplete. | Perform an authenticated walkthrough with owner-provided test credentials. |
| Requirements or business rules may be undocumented. | Expected results may be ambiguous. | Record assumptions and request confirmation before judging a case Pass/Fail. |
| Roles and permissions are not yet verified. | Access-control coverage may be inaccurate. | Inspect account/role management and test each confirmed role with authorized accounts. |
| Test data may affect shared records. | Existing data could be changed or deleted. | Use dummy data and agree on cleanup rules before execution. |
| A public tunnel exposes a local application to the internet. | Unauthorized access or exposure of data may occur. | Use synthetic data and test accounts, avoid secrets, restrict access where possible, and stop the tunnel after testing. |

## 16. Reporting and Metrics

The test summary should report:

- Total test cases designed.
- Number of cases executed.
- Pass, Fail, Blocked, and Not Executed counts.
- Execution rate: `Executed test cases / Total planned test cases × 100%`.
- Pass rate: `Passed test cases / Executed test cases × 100%`.
- Number of confirmed defects by severity and status.
- Outstanding risks, unresolved questions, and recommended next steps.

Report metrics only from the actual test execution records. Do not use planned test cases as if they were executed results.

## 17. Current Limitations and Next Steps

At the time of this plan, the public login, registration, and password-reset pages have been observed, but their behaviors have not yet been fully executed. The authenticated dashboard, inventory workflows, and actual role/permission model remain to be inspected.

Next steps:

1. Log in with an authorized test account and capture the available dashboard and navigation menus.
2. Record every confirmed role and the menus/actions each role can access.
3. Confirm inventory workflows and business rules with the application owner or through observed behavior.
4. Update the scope and candidate test areas, then write linked test scenarios and detailed test cases.
5. Execute tests and record actual results and evidence.

## 18. Document History

| Version | Date | Changes |
|---|---|---|
| 1.0 | 28 October 2026 | Initial test plan based on the public pages available during the first inspection. |
