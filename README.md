IATA Traacs Automation

A robust .NET-based automation tool built with Selenium WebDriver to streamline workflows within the IATA Traacs ecosystem. This repository provides the compiled executable version of the automation suite, released under the MIT License.

🚀 Overview

This project automates repetitive tasks and data entry processes within IATA Traacs, significantly reducing manual effort and minimizing human error. It is designed to handle complex web interactions, including multi-factor authentication (TOTP) and dynamic web elements.

Key Features

Headless & Windowed Execution: Supports various browser modes for debugging or background processing.

TOTP Integration: Handles time-based one-time passwords for secure automated logins.

Excel/Data Processing: Integrated with ClosedXML and EPPlus for efficient data handling.

Advanced Logging: Powered by Serilog for detailed execution tracking and troubleshooting.

🛠️ Project Structure (Build)

The published build includes:

IATATraacsAutomation.exe: The primary executable.

WebDriver.dll: Selenium core for browser control.

appsettings.json: Application configurations (Templated).

totp_secrets.json: Security configuration for MFA (Templated).

Supporting .NET Core libraries and Serilog extensions.

⚙️ Setup & Usage

To maintain security and integrity, all sensitive credentials have been removed from the configuration files in this build. To run the automation, follow these steps:

1. Prerequisites

Google Chrome: Ensure you have the latest version installed.

.NET Runtime: Ensure you have the .NET 6.0 (or higher) runtime installed on your machine.

2. Configuration

Locate the following JSON files in the root directory and populate them with your specific environment details:

appsettings.json

Update this file with your environment URLs, timeout settings, and log paths.

{
  "TargetUrl": "[https://your-traacs-url.com](https://your-traacs-url.com)",
  "BrowserType": "Chrome",
  "Logging": {
    "LogLevel": "Information"
  }
}


totp_secrets.json

Add your TOTP secret keys here to enable automated multi-factor authentication.

{
  "UserSecret": "YOUR_TOTP_SECRET_KEY_HERE"
}


3. Execution

Simply run the IATATraacsAutomation.exe. The logs will be generated in the logs/ folder for review.

⚖️ License

This project is licensed under the MIT License. You are free to use, modify, and distribute this software, provided that the original copyright notice and permission notice are included.

🤝 Contributing

Contributions to improve the automation logic or add new features are welcome. Please feel free to open an issue or submit a pull request.

Disclaimer: This tool is intended for professional use within authorized environments. Ensure you comply with IATA and your organization's security policies when using automation scripts.
