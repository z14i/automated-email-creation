Automated Email Account Creation Script
=======================================

This Python script automates the process of creating email accounts on a cPanel interface using Selenium WebDriver.

Features
--------

*   **Automated Browser Interaction**: Automatically logs into a specified cPanel URL, creates email accounts using names from an Excel file, and saves generated credentials to another Excel file.
    
*   **Excel Integration**: Utilizes pandas and openpyxl to read names from names.xlsx and save generated email addresses and passwords to generated\_emails.xlsx.
    
*   **Chrome WebDriver**: Configured to run Chrome headlessly with customizable options.
    
*   **Timeout Handling**: Uses WebDriverWait to ensure elements are loaded before interaction.
    

Prerequisites
-------------

*   Python 3.x
    
*   Chrome WebDriver (chromedriver) installed and added to your system PATH.
    
*   Dependencies: pandas, selenium, openpyxl.
    

Installation
------------

1.  git clone [https://github.com/z14i/automated-email-creation.git](https://github.com/z14i/automated-email-creation.git)
    
2.  pip install -r requirements.txt
    
3.  Download chromedriver:
    
    *   Visit [ChromeDriver Downloads](https://developer.chrome.com/docs/chromedriver/downloads#current_releases).
        
    *   Download the appropriate chromedriver version based on your Chrome browser version and operating system (e.g., Windows, macOS, Linux).
        
    *   Extract the chromedriver executable and place it in a directory included in your system's PATH.
        

Usage
-----

1.  Prepare your Excel file (names.xlsx) with a list of names to be used for email account creation.
    
2.  Update url in the script (main.py) to replace 'yourdomain.com:2083' with your domain.
    
3.  Update email formatting in the script (main.py) to match your domain ({formatted\_name}@yourdomain.com).
    
4.  Update input\_field\_user and input\_field\_pass with your cPanel login credentials.
    
5.  Update webdriver\_path in the script (main.py) to match your system's chromedriver executable path.
    
6.  python main.py This will start the automated process. The browser will open, log into the cPanel, create email accounts, and save credentials to generated\_emails.xlsx.
    

Notes
-----

*   Adjust timeouts (WebDriverWait durations) in main.py based on your system and page load speeds.
    
*   Customize Chrome options (chrome\_options) in main.py as needed for your environment.
