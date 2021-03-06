# Testing

 > Unit, functional and end-to-end (e2e) tests

## Unit Testing

 > Test isolated functions/files, focusing on api input vs output rather than implementation.

`yarn test:unit`

You can find all the `*.spec.js` test file sitting next to the file they test.
This way it is very quick and simple to see documentation on how to use a function.
It is also very easy to see if any files are _missing_ tests

## Functional Testing

 > Testing a whole route, Simulating clicks, Mock api calls and test the page is rendered correctly,
   focusing on how interactions affect multiple components.

`yarn test:func`

These tests should _not_ contribute to code-coverage as they load and check multiple functions across files (not lines of code).

## e2e Testing

 > Make sure the whole app run on multiple _real_ browsers,
   focusing on potentially problematic functionality.

 * `yarn test:e2e` (headless browser for local testing)
 * `yarn test:e2e-xb` (multiple browsers for remote testing)

## Smoke Testing

 > A subset of e2e tests that have been chosen to prove the app has been deployed correctly.

 * `yarn test:smoke -- --TARGET_PATH=preprod.domain.com`
