<div align="center">
  <h1>🚀 Demo Webshop Automation</h1>
  <p><i>Automated Playwright test scripts for User Registration and Login</i></p>
</div>

---

## 📖 Overview
This project contains automated, data-driven Playwright test scripts that validate the user registration and login workflows on the [Demo Webshop](https://demowebshop.tricentis.com/) website. It reads user credentials dynamically from an Excel file, executes tests in an automated browser instance, and logs detailed results (Pass/Fail/Exceptions).

## ✨ Features
- **Data-Driven Testing:** Reads accounts and passwords from `accounts_playwright_unique_passwords.xlsx`.
- **Headless & UI Mode:** Easily toggleable to see the browser running in real-time.
- **Robust Error Handling:** Checks for strict locators, explicitly captures validation errors, and gracefully handles network timeouts.
- **Detailed Logs:** Generates persistent log files in the `logs/` directory for every test run.

---

## 🛠️ Setup & Installation

**1. Install Required Packages**
Install Playwright and the library to read Excel files:
```bash
pip install playwright openpyxl pytest
```

**2. Install Browsers**
Download the necessary browser binaries for Playwright to work:
```bash
playwright install chromium
```

---

## 💻 How to Run

### 1. Register Users
First, you need to register the accounts present in your Excel file on the platform.
```bash
python register.py
```
> **Note:** Successful and failed registrations will be recorded inside `logs/register_results.txt`.

### 2. Test Logins
Once accounts are registered, you can run the login test script. It verifies both valid logins and gracefully catches any invalid login errors.
```bash
python login.py
```
> **Note:** Login outcomes and any captured validation errors are recorded inside `logs/login_results.txt`.

---

## 📁 Project Structure
```text
📦 automation_test_demo
 ┣ 📂 logs/                                      # Test execution log files
 ┃  ┣ 📜 login_results.txt
 ┃  ┗ 📜 register_results.txt
 ┣ 📜 accounts_playwright_unique_passwords.xlsx  # Excel sheet with test data
 ┣ 📜 register.py                                # Registration automation script
 ┗ 📜 login.py                                   # Login automation script
```
=======
# PlayWright_Login_Test

