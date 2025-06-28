# Cucumber TypeScript Example

This project demonstrates BDD testing using Cucumber.js with TypeScript.

## Project Structure

- `features/` - Contains feature files and step definitions
  - `books.feature` - Example feature for books and authors
  - `support/books.steps.ts` - Step definitions for the feature
- `report.js` - Script to generate HTML reports from Cucumber JSON output
- `cucumber.json` - Cucumber configuration file
- `package.json` - Project dependencies and scripts

## Prerequisites

- Node.js (v14 or above recommended)
- npm

## Setup

1. Install dependencies:
   ```sh
   npm install
   ```

## Running Tests

To execute the Cucumber tests:
```sh
npm test
```

## Generating HTML Report

After running the tests, generate the HTML report:
```sh
npm run report
```
The report will be available at `reports/cucumber_report.html`.

## Example Feature

See `features/books.feature` for a sample scenario of searching books by author.

## Notes
- Step definitions are written in TypeScript and use `ts-node` for execution.
- Reports are generated using `cucumber-html-reporter`.
