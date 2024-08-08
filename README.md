# Selenium Hybrid Framework

## Overview

This repository contains a Selenium Hybrid Framework using Java. The framework employs Page Object Model (POM) design, Extent Reports for detailed reporting, Log4j for logging, and TestNG for running the tests. The project is built using Maven for dependency management.

## Prerequisites

- Java JDK 1.8 or higher
- Maven
- IDE (Eclipse/IntelliJ IDEA/VS Code)
- ChromeDriver/GeckoDriver (based on your browser)

## Project Structure

seleniumFramework/
├── .settings/
├── driver/
├── excelFiles/
├── logs/
├── reports/
│   └── report<timestamp>.html
├── Screenshots/
├── src/
│   ├── main/
│   │   └── java/
│   │       ├── pageObject/
│   │       ├── reusable/
│   │       └── utilities/
│   └── resources/
│       ├── log4j2.xml
│       └── siteData.properties
├── test/
│   └── java/
│       └── package2/
│           └── AppTest.java
├── target/
├── test-output/
├── .classpath
├── .project
├── extent-config.xml
├── pom.xml
└── testng.xml


## Getting Started

### Clone the Repository

```bash
git clone https://github.com/abhinav18e/SeleniumHybrid.git
cd seleniumHybrid
```

### Install Dependencies

Run the following command to install the required dependencies:

```bash
mvn clean install
```

### Configuration

1. **Driver Configuration:** Place your WebDriver (ChromeDriver/GeckoDriver) executables in the `driver` directory or configure the path in the `reusable` package.
2. **Log4j Configuration:** Configure the `log4j2.xml` file located in the `resources` folder.
3. **Extent Report Configuration:** Configure the `extent-config.xml` file located in the root directory.

### Running Tests

You can run the tests using TestNG:

```bash
mvn test
```

Or you can run specific test suites using the TestNG XML:

```bash
mvn test -DsuiteXmlFile=testng.xml
```

## Framework Components

### 1. Page Object Model (POM)

The POM design pattern is implemented to create an object repository for web UI elements. It reduces code duplication and improves test maintenance.

### 2. Logging

Log4j is used for logging purposes. Logs are stored in the `logs` directory.

### 3. Reporting

Extent Reports are used to generate detailed test execution reports. Reports are stored in the `reports` directory.

### 4. Test Runner

TestNG is used to run the test cases. The test suite is configured in the `testng.xml` file.

## Adding New Tests

1. **Create Page Classes:** Add new page classes in the `pageObject` package.
2. **Create Test Classes:** Add test classes in the `package2` package.
3. **Add Test Methods:** Write test methods in the test classes using TestNG annotations.


## Contact

If you have any questions or feedback, feel free to reach out at abhinavnagpure4@gmail.com.
