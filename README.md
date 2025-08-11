# Digikala
This repository contains e2e test for Digikala website, written in Robot Framework and Selenium library

## Project structure
Digikala/
├── tests/
│ ├── login.robot
│ └── cart_checkout.robot
├── resources/
│ ├── browser.resource # open/close browser, common setup
│ └── keywords.resource # reusable keywords (login, add to cart, etc.)
├── results/ # reports output (created at runtime)
└── README.md

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



