==# CaseKaro Mobile Cover Search Automation

This project implements automated testing for **mobile cover search functionality** on the [CaseKaro](https://casekaro.com) website using **Java, Playwright, and Cucumber BDD framework**.  

The main file is `CasekaroTest.java`, located in the `Playwright1` package.  

---

## 📂 Project Structure
src/
├── test/
│ ├── java/
│ │ ├── runners/
│ │ │ └── TestRunner.java # Cucumber test runner
│ │ ├── stepDefinitions/
│ │ │ └── MobileCoverSteps.java # Step definitions for BDD scenarios
│ │ └── Playwrights1/
│ │ └── Myassignament1.java # Original non-BDD test
│ └── resources/
│ └── features/
│ └── mobile_cover_search.feature # BDD feature file

markdown
Copy code

---

## ✅ Test Steps Covered
- Navigate to CaseKaro website  
- Click on **Mobile Covers**  
- Search for **"Apple"** and validate only Apple brand results  
- Click on **Apple brand**  
- Search for **"iPhone 16 Pro"** model  
- Apply **"In Stock"** filter  
- Extract product details from 2 pages including:
  - Discounted price  
  - Actual price  
  - Item description  
  - Image link  
- Store and print data in **ascending order of discounted price**  

---

## 🛠️ Technologies Used
- **Java 11** – Programming language  
- **Playwright** – Web automation framework  
- **Cucumber** – BDD framework  
- **JUnit 5** – Testing framework  
- **Maven** – Build tool  

### 📦 Dependencies
- `playwright: 1.40.0`  
- `cucumber-java: 7.15.0`  
- `cucumber-junit-platform-engine: 7.15.0`  
- `junit-jupiter: 5.10.0`  
- `junit-platform-suite: 1.10.0`  

---

## ▶️ Running Tests

### Prerequisites
- Java 11 or higher  
- Maven 3.6 or higher  
- Internet connection (for downloading browser binaries)  

### Run BDD Tests
```bash
mvn test
Run Specific Test Runner
bash
Copy code
mvn test -Dtest=TestRunner
Run Original Non-BDD Test
bash
Copy code
mvn test -Dtest=Myassignament1
📊 Test Reports
Console output shows detailed step execution

Results available in target/surefire-reports/

Browser trace files saved as trace.zip

📝 BDD Feature File
The feature file mobile_cover_search.feature contains:

Feature: Mobile Cover Search and Data Extraction

Background: Common setup steps

Scenario: Complete search and data extraction workflow

🖊️ Step Definitions
The step definitions in MobileCoverSteps.java include:

Browser setup and teardown using @Before and @After hooks

Page object interactions via Playwright

Data extraction and validation logic

Assertions for test validation

🌟 Key Features
No try-catch blocks (as per requirement)

Comprehensive assertions at each step

Clean, modular code structure

BDD approach with human-readable scenarios

Browser tracing enabled for debugging

Non-headless mode execution for visibility

Automatic browser binary downloads handled by Playwright

Product sorting by discounted price implemented

Negative validation for non-Apple brands included

Multi-page product data extraction supported

⚠️ Troubleshooting
Browser not found:

bash
Copy code
mvn exec:java -e -Dexec.mainClass="com.microsoft.playwright.CLI" -Dexec.args="install"
Test failures: Check browser compatibility and internet connection

Missing dependencies: Run

bash
Copy code
mvn clean install
📌 Notes
Tests run in non-headless mode for visibility.

Contributions and improvements are welcome!
