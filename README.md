# Playwright To-Do Application Automation

## Project Overview

This is a beginner-level end-to-end test automation project developed using **Playwright and JavaScript**.

The project automates and validates the functionality of a To-Do application, including adding tasks, marking tasks as completed, and filtering completed tasks.

## Technologies Used

- Playwright
- JavaScript
- Node.js
- Git
- GitHub

## Test Scenario

The automated test performs the following actions:

1. Opens the To-Do application.
2. Adds multiple tasks.
3. Verifies that the tasks are displayed.
4. Marks tasks as completed.
5. Verifies the completed tasks.
6. Filters the tasks using the **Completed** filter.
7. Validates the expected number of completed tasks.

## Test Reports

This project includes both failed and successful Playwright HTML test reports.

### Failed Test Report

The initial test execution failed because the expected number of completed tasks was incorrect.

**Initial Assertion:**

```javascript
await expect(page.locator('.todo-list li')).toHaveCount(3);
```

**Actual Result:**

```text
Expected: 3
Received: 2
```

### Issue Analysis

After applying the **Completed** filter, only two completed tasks were displayed. Therefore, the assertion expecting three tasks was incorrect.

### Fix Applied

The assertion was updated to expect two completed tasks:

```javascript
await expect(page.locator('.todo-list li')).toHaveCount(2);
```

### Successful Test Execution

After correcting the assertion, the test was executed again successfully.

```text
1 passed
```

## Project Structure

```text
playwright-mini-project/
│
├── reports/
│   ├── failed-test-report/
│   └── passed-test-report/
│
├── tests/
│   └── todo-demo1.spec.js
│
├── .gitignore
├── package.json
├── package-lock.json
├── playwright.config.js
└── README.md
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Adithyakr18/playwright-mini-project.git
```

### 2. Navigate to the project folder

```bash
cd playwright-mini-project
```

### 3. Install dependencies

```bash
npm install
```

### 4. Install Playwright browsers

```bash
npx playwright install
```

### 5. Run the tests

```bash
npx playwright test
```

### 6. View the HTML report

```bash
npx playwright show-report
```

## Key Learnings

- Writing automated test scripts using Playwright.
- Using locators and assertions.
- Automating user interactions.
- Validating expected results.
- Analyzing test failures.
- Correcting test assertions based on actual application behavior.
- Generating Playwright HTML reports.
- Using Git and GitHub for version control.

## Author

**Adithya**

Aspiring Software Test Engineer | Manual Testing | API Testing | SQL | Playwright Automation
