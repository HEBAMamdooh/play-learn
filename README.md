# play-learn - Playwright with JavaScript Learning Project

## Overview
This project is designed for learning and practicing **Playwright** with **JavaScript** and **TypeScript**. Playwright is an end-to-end testing framework that enables reliable automation for web applications across multiple browsers.

## Prerequisites
Before starting, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (LTS version recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## Setup
1. Clone this repository:
   ```sh
   git https://github.com/HEBAMamdooh/play-learn.git
   cd play-learn
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Install Playwright browsers:
   ```sh
   npx playwright install
   ```

## Project Structure
```
📂 play-learn
 ├── 📂 tests                # Test scripts
 ├── 📜 playwright.config.ts # Playwright configuration
 ├── 📜 package.json         # Project metadata and dependencies
 ├── 📜 README.md            # Project documentation
```

## Running Tests
To execute tests, use the following command:

Runs the end-to-end tests.
```sh
npx playwright test
```

Starts the interactive UI mode.
```sh
npx playwright test --ui
```

To open last HTML report run:
```sh
npx playwright show-report
```

To run tests in a specific browser (e.g., Chrome):
```sh
npx playwright test --project=chromium
```
Or:
```sh
npx playwright test --browser=chromium
```

Runs the tests in a specific file.
```sh
npx playwright test example
```

Runs the tests in debug mode.
```sh
npx playwright test --debug
```

Auto generate tests with Codegen.
```sh
npx playwright codegen
```

To run tests in headed mode:
```sh
npx playwright test --headed
```

## Writing Tests
Create a new test file inside the `tests` folder and write Playwright test scripts using the syntax:
```js
const { test, expect } = require('@playwright/test');

test('Example test', async ({ page }) => {
  await page.goto('https://example.com');
  await expect(page).toHaveTitle(/Example Domain/);
});
```

## Debugging Tests
Use the following command to debug tests:
```sh
npx playwright test --debug
```
You can also trace a test run for debugging:
```sh
npx playwright test --trace on
```

## License
This project is for learning purposes. Feel free to use and modify it.

---
Happy Testing! 🚀
