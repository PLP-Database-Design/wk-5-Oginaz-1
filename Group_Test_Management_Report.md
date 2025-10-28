# 🧪 Group Test Management Report — Word Puzzle Game Plus

**Level:** QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

---

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Okai Nyarko Isaac | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Sammy Shoka | Risk identification, prioritization, test design linkage |
| Test Executor | Joel Githara | Execution, evidence capture, defect logging |

---

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Test Focus |
|---------|-------------|------------|
| Reset Game | Resets score and progress instantly | State management, data integrity |
| Leaderboard | Stores top 3 scores in `localStorage` | Persistence, boundary values |
| Bonus Round | Every 3 puzzles → score × 2 | Logic, arithmetic, event sequencing |

---

## 1. Test Plan

### 1.1 Test Objectives

The primary objectives of this test plan are to:

- **Functionality Verification:** Ensure all core game features (Reset Game, Leaderboard, Bonus Round) operate as specified
- **Data Integrity:** Validate correct score calculation, leaderboard persistence, and state management
- **Risk Mitigation:** Identify and test high-risk areas including localStorage operations, bonus round logic, and edge cases
- **Quality Assurance:** Maintain game stability, user experience, and data consistency across all interactions
- **Team Collaboration:** Demonstrate effective test management through proper planning, execution, and monitoring

### 1.2 Scope

#### In Scope
- **Functional Testing:**
  - Reset Game functionality and state management
  - Leaderboard storage and retrieval from localStorage
  - Bonus Round calculation and trigger logic
  - Score calculation with hints and without hints
  - Puzzle scrambling and validation
  - Hint display and cost deduction
  
- **Non-Functional Testing:**
  - Usability and accessibility testing
  - Browser compatibility (Chrome desktop focus)
  - User interface responsiveness
  - Error handling and edge cases

#### Out of Scope
- Cross-browser testing beyond Chrome desktop
- Performance testing under load
- Security testing of localStorage
- Mobile device testing
- Network connectivity scenarios
- Backend server integration

### 1.3 Resources

#### Team Structure (3 Members)

| Role | Responsibilities | Deliverables |
|------|------------------|--------------|
| **Test Manager** | • Draft comprehensive test plan<br>• Schedule test activities and milestones<br>• Track test metrics and progress<br>• Coordinate team communication<br>• Manage test artifacts | • Test Plan Document<br>• Test Schedule<br>• Test Metrics Dashboard<br>• Progress Reports |
| **Risk Analyst** | • Identify functional and non-functional risks<br>• Assess risk likelihood and impact<br>• Prioritize risks and create mitigation strategies<br>• Design high-risk test cases<br>• Create risk-coverage analysis | • Risk Assessment Matrix<br>• Risk Mitigation Plans<br>• High-Priority Test Cases<br>• Risk Coverage Chart |
| **Test Executor** | • Execute designed test cases<br>• Document test results and evidence<br>• Log defects in GitHub Issues<br>• Capture screenshots and logs<br>• Validate defect fixes<br>• Maintain test execution log | • Test Execution Results<br>• Defect Reports (GitHub Issues)<br>• Test Evidence (Screenshots)<br>• Test Summary Report |

#### Tools & Technologies

- **Test Environment:** Chrome Browser (Desktop) - Recommended Version: Latest stable
- **Repository Management:** GitHub (for version control and issue tracking)
- **Defect Management:** GitHub Issues
- **Documentation:** Markdown files
- **Communication:** Team collaboration through GitHub and WhatsApp
- **Test Data:** Word bank included in application

### 1.4 Schedule (Phase Timeline)

| Phase | Activities | Planned Duration | Actual Duration | Status |
|-------|-----------|------------------|-----------------|--------|
| **Planning** | • Test plan creation<br>• Risk analysis<br>• Test case design | 2 days | [TBD] | [TBD] |
| **Design** | • Finalize test cases<br>• Prepare test data<br>• Setup test environment | 1 day | [TBD] | [TBD] |
| **Execution** | • Execute test cases<br>• Log defects<br>• Track metrics | 3 days | [TBD] | [TBD] |
| **Reporting** | • Compile results<br>• Create final report<br>• Team reflection | 1 day | [TBD] | [TBD] |

**Total Estimated Duration:** 7 days

### 1.5 Entry and Exit Criteria

#### Entry Criteria (Pre-Requisites for Test Execution)

- ✅ Test plan approved by all team members
- ✅ Test environment setup completed (Chrome browser installed)
- ✅ Application accessible and functional
- ✅ GitHub repository configured for issue tracking
- ✅ Test cases documented and reviewed
- ✅ Risk analysis completed
- ✅ Team roles assigned and understood

#### Exit Criteria (Conditions to Stop Testing)

- ✅ All planned test cases executed
- ✅ Minimum 8 test cases completed (≥5 risk-based)
- ✅ Minimum 2 negative test cases executed
- ✅ Minimum 1 usability test executed
- ✅ Minimum 3 defects logged in GitHub Issues
- ✅ All critical and high-severity defects either fixed or documented
- ✅ Risk coverage ≥ 80%
- ✅ Test metrics calculated and recorded
- ✅ Final test report completed
- ✅ All team members approved the report

### 1.6 Test Environment

- **Primary Browser:** Chrome (Desktop) - Recommended version
- **Operating System:** Windows 10 (or macOS/Linux as available)
- **Screen Resolution:** Minimum 1366x768
- **Storage:** Application uses browser localStorage (no external dependencies)
- **Network:** Not required (fully offline capable)
- **Prerequisites:** 
  - Chrome browser installed
  - Application file (`index.html`) accessible locally
  - GitHub account for issue tracking


---

## 2. Risk Analysis
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

- Tested Risks Percent: 86% (6 out 7 risks tested)
- Untested Risks Percent: 14% (1 out 7 risk untested -UI)

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
|TC-01 |Reset Button |Verify reset clears all game variables |Score, solved count, and hint reset to zero |Works correctly |Pass |R01 |
|TC-02 |Leader Board |Validate score sorting and top 3 display |Scores sorted in descending order and top 3 retained after refreshing |Works correctly |Pass |R02 |
|TC-03 |Leader Board |Confirm new lower score doesn’t overwrite higher ones |Scores below top 3 should be ignored i.e leaderboard remains unchanged |Works correctly |Pass |R02 |
|TC-04 |Bonus Round |Verify score doubles only every 3rd correct solve |Score doubles after every 3 correct guesses |Works correctly |Pass |R03 |
|TC-05 |Hint Bonus |Verify 2-point deduction occurs correctly on hint use |Score decreases by 2 after hint |Hint deductions occurs when score > 0 only |Fail |R04 |
|TC-06 |Hint Bonus |Verify that 2-point deduction occurs only once per puzzle |Only one hint per puzzle |Works correctly |Pass |R04 |
|TC-07 |Input Validation |Warning shown when submitting empty input |Error message displayed |Works correctly |Pass |R05 |
|TC-08 |Submit Button |Prevent multiple score increments from rapid clicks |Only one score increment allowed per correct guess |Rapid clicks increment the score |Fail |R07 |
|TC-09 |Submit Button |Ensure buttons re-enable after new puzzle loads |Submit button active  |Works correctly |Pass |R07 |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
|D -01 |Reset game message not clearing |Low |R01 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/2#issue-3560892924 |
|D -02 |Double scoring exploit during post-solve delay |Major |R07 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/3#issue-3560894117 |
|D -03 |Hint Button not deducting points when score is Zero |Major |R04 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/6#issue-3561000641 |
|D -04 |Reset button does not automatically start a new puzzle |Medium |R01 |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/7#issue-3561037593 |
|D -05 |Reset leaves message and allows Hint without a new puzzle |Medium |R01 and R04  |Open |https://github.com/PLP-Database-Design/wk-5-Oginaz-1/issues/8#issue-3561083307 |

## Metrics

- Test Case Pass Percent: 78% (7/9 * 100)
- Defect Density: 0.56 (5/9)
- Risk Coverage Percent: 86%

### Defect Summary

- Total Defects Logged: 5
- Critical High: Major -2, Medium -2, Low -1

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

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| Okai Nyarko Isaac | Test Manager | O.N.I | 2025-10-28 |
| Sammy Shoka| Risk Analyst | S.S | 2025-10-28 |
|Joel Githara | Test Executor | J.G|2025-10-28 |
