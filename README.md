# Eureka_Website_Automation_Testing_Case_4

## Overview

This repository contains the Case_4 automation script. It is developed using Python and Selenium to automate **Access_Typed_Open book and book chapter search and download actions** on the Eureka Website. The script was developed in **PyCharm IDE**.

## Test Case Summary

This positive test case verifies that a user can successfully access and download assigned **Access_Typed_Open books or Access_Typed_Open book chapters** from the Eureka Website.

The user logs in with valid credentials and searches for the required book or book chapter by entering its title, chapter name, or keyword in the **Search** field. After clicking the **Search** button, the system displays the relevant book or chapter.

The test case verifies the following download scenarios:

* Search and download **Chapter #1 of Book 1 – 4D Fetal Echocardiography**.
* Search and download a **different chapter of Book 1 – 4D Fetal Echocardiography**.
* Search and download the **complete Book 2 – An Ecological Perspective on Health Promotion Systems, Settings and Social Processes**.
* Search for a chapter of **Book 3 – Consanguinity - Its Impact, Consequences and Management** using right-click functionality.
* Verify that the selected chapter opens successfully in a **new tab/window**.
* Download the selected chapter from the newly opened page.

The test case confirms that assigned Access_Typed_Open content can be searched and downloaded successfully by an authenticated user.

## Folder Structure

[image](https://private-user-images.githubusercontent.com/84409898/655534168-72a262d5-c372-4012-bbbd-0675cd09b7b6.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODk5NjgxMjAsIm5iZiI6MTc4OTk2NzgyMCwicGF0aCI6Ii84NDQwOTg5OC82NTU1MzQxNjgtNzJhMjYyZDUtYzM3Mi00MDEyLWJiYmQtMDY3NWNkMDliN2I2LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA5MjElMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwOTIxVDA1MTcwMFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.DWTrI8RAHUZanvOsZzLqlf2Vjjvqpsg1yktDtjJzweY)

## .env File

### Purpose:

To securely store login credentials and the base URL.

### Install dotenv library:

```bash
pip install python-dotenv
```

### Python Code to Load .env File:

```python
import os
from dotenv import load_dotenv

# Load .env file
load_dotenv(".env")

# Variables
EMAIL = os.getenv("EMAIL")
PASSWORD = os.getenv("PASSWORD")
BASE_URL = os.getenv("BASE_URL")
```

### .env File Content:

**LOGIN CREDENTIALS**

```text
EMAIL=(Your Email)
PASSWORD=(Your Password)
```

**SITE URL**

```text
BASE_URL=https://www.eurekaselect.com/
```

## Creating Executable (.exe) File

### Install PyInstaller:

```bash
pip install pyinstaller
```

### Command to Create Executable:

```bash
pyinstaller --onefile --collect-all selenium Case_4.py
```
