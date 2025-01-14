# Enterprise Level Website Automation Test Suite

## Overview
This project is designed to automate the testing of an enterprise-level website. It employs robust frameworks and tools to ensure high-quality, efficient, and scalable test execution. The suite is built with Selenium and Java and supports advanced reporting, cross-browser testing, and continuous integration.

---

## Features
- **Framework:** Hybrid Framework (Data-Driven + Keyword-Driven + Modular)
- **Language:** Java
- **Test Runner:** TestNG
- **Reporting:** Allure Reports
- **Browser Support:** Chrome, Firefox, Edge, and Safari
- **Integration:** CI/CD tools (e.g., Jenkins, GitHub Actions)
- **Bug Tracking:** Integration with bug-tracking tools like JIRA

---

## Prerequisites
- **Java:** JDK 8 or higher
- **Maven:** Version 3.6 or higher
- **Selenium WebDriver:** Latest version
- **IDE:** IntelliJ IDEA or Eclipse
- **Allure Commandline:** Installed and configured
- **Browser Drivers:** Appropriate drivers (e.g., chromedriver, geckodriver) available in the PATH

---

## Project Structure
```
|-- src
    |-- main
        |-- java
            |-- base
            |-- utils
    |-- test
        |-- java
            |-- testcases
            |-- data
|-- resources
    |-- config.properties
    |-- testdata.xlsx
|-- reports
    |-- allure-results
|-- pom.xml
|-- README.md
```

### Key Directories
- **base:** Contains core framework classes like BaseTest and WebDriverManager.
- **utils:** Includes utility classes for logging, reporting, and common actions.
- **testcases:** Houses the test scripts.
- **data:** Contains test data files.

---

## Installation
1. Clone the repository:
   ```
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```
   cd <project-directory>
   ```
3. Install dependencies:
   ```
   mvn clean install
   ```

---

## Configuration
1. Update the `config.properties` file in the `resources` directory with your environment-specific settings (e.g., base URL, browser).
2. Ensure that browser drivers are properly set up and accessible in the system PATH.

---

## Running Tests
1. **Run All Tests:**
   ```
   mvn test
   ```
2. **Run Specific Test Suite:**
   ```
   mvn test -DsuiteXmlFile=testng.xml
   ```
3. **Generate Allure Report:**
   ```
   allure serve allure-results
   ```

---

## CI/CD Integration
- This project includes a `Jenkinsfile`/`.github/workflows` configuration for continuous integration and automated test execution.
- Modify the configuration files as needed for your environment.

---

## Best Practices
1. **Organize Test Data:** Use external files for test data to enhance maintainability.
2. **Avoid Hardcoding:** Use `config.properties` for environment-specific configurations.
3. **Version Control:** Commit changes to the repository with clear messages.
4. **Continuous Testing:** Leverage CI/CD pipelines for frequent execution.

---

## Troubleshooting
- **WebDriver Exception:** Verify that the correct browser driver version is used.
- **Test Failure:** Review logs in the `reports` directory or check the Allure dashboard.
- **Dependency Issues:** Run `mvn dependency:resolve` to fix dependency conflicts.

---

## Contributors
--Deepak--

---

## License
This project is licensed under the [MIT License](LICENSE).
