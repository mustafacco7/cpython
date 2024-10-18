# Supported Platforms and Build Types

This project now supports building on multiple platforms and with various build types. The supported platforms and build types are as follows:

## Platforms
- Ubuntu
- Windows
- macOS

## Build Types
- Release
- Debug
- RelWithDebInfo

# Running Tests and Generating Reports

After building the project, you can run the tests and generate reports using the following instructions:

## Running Unit Tests
1. Navigate to the build output directory.
2. Run the following command to execute the unit tests:
   ```
   ctest --build-config <build_type>
   ```

## Running Integration Tests
1. Navigate to the build output directory.
2. Run the following command to execute the integration tests:
   ```
   ctest --build-config <build_type> --tests-regex <integration_test_pattern>
   ```

## Generating Test Coverage Reports
1. Ensure that the project is built with coverage instrumentation.
2. Run the following command to generate the coverage report:
   ```
   gcovr -r . --html --html-details -o coverage.html
   ```

## Notifications for Build or Test Failures
The workflow is configured to send notifications to the team when a build or test fails. Ensure that the notification settings are properly configured in the workflow file.
