# 🧪 Group Test Management Report — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

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
| Test Executor | joel githara | Execution, evidence capture, defect logging |

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
- **Communication:** Team collaboration through GitHub Projects/Issues
- **Test Data:** Word bank included in application (10 words)

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