Eureka_Website_Automation_Testing_Case_4OverviewThis repository contains the Case_4 automation script. It is developed using Python and Selenium to automate Access_Typed_Open book and book chapter search and download actions on the Eureka website. The script was developed in PyCharm IDE.Test Case Summary:This positive test case verifies that a user can successfully access and download assigned Access_Typed_Open books or Access_Typed_Open book chapters from the Eureka Website. The user logs in with valid credentials and searches for the required Access Book or Book Chapter by entering its title or keyword in the Search field. After clicking the Search button, the system displays the relevant book or chapter. If the selected content is assigned by the admin, the user is able to download the permitted content, either specific chapters or the complete book. The test case also verifies a chapter download using the right-click functionality, where the chapter link opens in a new tab/window and the user downloads the chapter from the newly opened page.   Folder StructurePlaintextEureka_Website_Automation_Testing_Case_4/
│
├── Case#4/
│   │
│   ├── case_4/
│   │   ├── .env                       # Environment variables file (credentials & URL)
│   │   └── Case_4.exe                 # Executable file generated from .py script
│   │
│   ├── build/
│   │   └── Case_4/                    # PyInstaller auto-generated files
│   │
│   ├── Case_4.py                      # Main Python automation script
│   ├── Case_4.spec                    # PyInstaller spec file
│   ├── Case_4.xlsx                    # Excel file containing test case details
│   └── README.md



Purpose:

To securely store login credentials and the base URL.

Install dotenv library:

pip install python-dotenv

Python Code to Load .env File:

import os from dotenv import load_dotenv

Load .env file
load_dotenv(".env")

Variables
EMAIL = os.getenv("EMAIL") PASSWORD = os.getenv("PASSWORD") BASE_URL = os.getenv("BASE_URL")

.env File Content:

LOGIN CREDENTIALS

EMAIL=(Your Email) PASSWORD=(Your Password)

SITE URL

BASE_URL=https://www.eurekaselect.com/

Creating Executable (.exe) File

Install PyInstaller:

pip install pyinstaller

Command to Create Executable:

pyinstaller --onefile --collect-all selenium Case_2.py
