# Digikala
This repository contains e2e test for Digikala website, written in Robot Framework and Selenium library

## Project structure
tests/ – contains test suites

login.robot – verifies login functionality

cart_checkout.robot – verifies search, add-to-cart, and checkout flow

resources/ – shared resources and reusable keywords

browser.resource – handles browser setup, teardown, and common actions

keywords.resource – reusable keywords for login, add-to-cart, etc.

results/ – stores test reports and logs generated at runtime

README.md – project documentation

## How to run Tests
Some of the existing tests require a valid Digikala account in order to execute successfully.
To run these tests, you must pass your Digikala account credentials at runtime using --variable arguments.

Example:
robot \
  --variable EMAIL:you@example.com \
  --variable PASSWORD:yourSecret \
  tests/login.robot
  

Suggestion:
For better security, the test could be updated to read credentials from environment variables or CI/CD secrets, instead of entering them directly in the command. This would help ensure sensitive details like email and password aren’t exposed in terminal history, logs, or version control.



