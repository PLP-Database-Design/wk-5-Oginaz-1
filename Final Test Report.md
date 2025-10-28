# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Okai Nyarko Isaac| Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Sammy Shoka | Risk identification, prioritization, test design linkage |
| Test Executor | Joel Githara| Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | High — State integrity & control flow |
| Leaderboard | Stores top 3 scores in localStorage | Medium — Data persistence & sorting |
| Bonus Round | Every 3 puzzles → doubles score | Medium — Logic correctness & sequencing |

## Test Plan

### Objectives

- Functionality Verification: Ensure Reset, Leaderboard, and Bonus Round work as specified.
- Data Integrity: Validate score calculation, leaderboard persistence, and state management.
- Risk Mitigation: Focus tests on high-risk areas (localStorage, bonus logic, edge cases).
- Quality Assurance: Maintain stability, UX quality, and data consistency across flows.
- Team Collaboration: Demonstrate effective planning, execution, and monitoring.

### Scope

**In Scope:**
- Functional Testing:
  - Reset Game state management
  - Leaderboard storage/retrieval from localStorage
  - Bonus Round calculation and trigger logic
  - Score calculation with and without hints
  - Puzzle scrambling and validation
  - Hint display and cost deduction
- Non-Functional Testing:
  - Usability and accessibility
  - Browser compatibility (Chrome desktop)
  - UI responsiveness
  - Error handling and edge cases

**Out of Scope:**
- Cross-browser testing beyond Chrome desktop
- Performance testing under load
- Security testing of localStorage
- Mobile device testing
- Network connectivity scenarios
- Backend server integration

### Tools & Resources

- Test Environment: Chrome Browser (Desktop) — latest stable
- Repository Management: GitHub
- Defect Management: GitHub Issues
- Documentation: Markdown files
- Communication: GitHub and WhatsApp
- Test Data: Built-in word bank

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| Planning | 2 days | [TBD] | [TBD] |
| Design | 1 day | [TBD] | [TBD] |
| Execution | 3 days | [TBD] | [TBD] |
| Reporting | 1 day | [TBD] | [TBD] |

## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
|R01 |Reset Button |Game state may not reset all variables |Medium |High |High |Validate all state variables and UI values reset correctly |
|R02 |Leader Board |Incorrect Score sorting or overwriting of scores |Medium |Medium |Critical |Test boundary values and local storage persistence |
|R03 |Bonus Round |Logic error could double at wrong time |Medium |Medium |Medium |Test with cumulative solves and verify arithmetic logic |
|R04 |Hint Bonus |Hint points may not be deducted when score is zero |Medium |Medium |High |Validate deduction logic and arithmetic |
|R05 |Input Validation |Empty input   |low |Medium |Low |Add validation message and error messages |
|R06 |UI |Screen readers may not get updates |Low |Medium |Low |Verify Accessibility tags in Browser |
|R07 |Submit Button |Clicking submit rapidly multiple times before next puzzle loads causing repeated score increments and false bonus triggers. |High |High |High |Disable Submit and Hint buttons immediately after a correct guess, and re-enable them only once new puzzle loads |


### Risk Coverage

- Tested Risks Percent: 
- Untested Risks Percent: 

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
| | | | | | | |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
|D -01 |Reset game message not clearing |Low |R01 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/2#issue-3560892924 |
|D -02 |Double scoring exploit during post-solve delay |Major |R07 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/3#issue-3560894117 |
|D -03 |Hint Button not deducting points when score is Zero |Major |R04 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/6#issue-3561000641 |
|D -04 |Reset button does not automatically start a new puzzle |Medium |R01 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/7#issue-3561037593 |
|D -05 |Reset leaves message and allows Hint without a new puzzle |Medium |R01 and R04  |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/8#issue-3561083307 |


## Metrics

- Test Case Pass Percent: 
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 

### Defect Summary

- Total Defects Logged: 5
- Critical High: Major -2, Medium -2, Low -1
- Fix Rate: 

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
|Planning |Test Plan |Completed |0 |Isaac Okai |
|Risk Analysis |Risk Table |Completed |0 |Sammy Shoka |
|Test Design & Execution |Test Cases and Results |Completed |0 |Joel Githara |
|Defect Reporting |Defects Table |Completed |0 |Sammy Shoka |
|Test Monitoring & Metrics |Metrics results |Completed |0 |Isaac Okai |

**Progress Tracking Method:**  Github issues and Manual checklist

**Change Control Notes:** Risk table updated after Submit button defect discovery

## Lessons Learned

- Most Defect Prone Feature: Hint System
- Risk Analysis Impact: Did focus on bonus system,submit and hint button
- Team Communication Effectiveness: Cross-channel updates (GitHub + WhatsApp) reduced blockers and sped decisions.
- Improvements for Next Cycle: Automate regression (smoke tests) and tighten control on post-solve state.

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Okai Nyarko Isaac | Test Manager | O.N.I | 2025-10-28 |
| | Risk Analyst | | |
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
