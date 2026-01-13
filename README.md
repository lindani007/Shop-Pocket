# Shop Pocket 

## By Lindani Dev 

 
<img width="1024" height="1024" alt="myicon" src="https://github.com/user-attachments/assets/ba8e3ec5-9793-4716-a3d8-76d180e586c2" />

 

 

 

 

# Shop Pocket 

Shop Pocket is a cross-platform self-service supermarket management and point-of-sale helper built with .NET MAUI. It provides quick price lookups, inventory management, simple transactions (card/cash), and basic reporting tools intended for small retailers and attendants. 

 

# About The Project 

Shop Pocket helps store staff perform quick, local tasks without needing full POS hardware: 

Search product prices and availability 

Add incoming stock batches and update available quantities 

Record simple card and cash transactions and fees 

Generate basic profit and transaction summaries 

Provide a simple staff/employee flow for restricted actions 

The project stores data in JSON files (local storage) and is designed for small shops that need an on-device, lightweight inventory and sales helper. 

 

# Built With 

.NET 10 and .NET MAUI (cross-platform UI) 

C# 14 

CommunityToolkit.Mvvm 

Microcharts.Maui (for charts) 

BCrypt.Net-Next (for password hashing) 

JSON-based local persistence (custom Json helper classes) 

 

# Getting Started 

Clone the repository: 

Restore packages and build: 

Open the project in Visual Studio (recommended) or use the .NET CLI. For Visual Studio: 

Open SuperMarket.sln or the SuperMarket folder. 

Ensure the .NET MAUI workload is installed. 

 

# Prerequisites 

.NET 10 SDK (matching your target frameworks) 

.NET MAUI workload (installed via Visual Studio or dotnet workload) 

Visual Studio 2022/2026 or Visual Studio for Mac with MAUI support (Visual Studio 2026 recommended) 

Platform SDKs: 

Android SDK (Android 21+ as in csproj) 

Xcode (for iOS/Mac Catalyst builds) on macOS 

(Optional) Windows 10 SDK if packaging for Windows 

Git (for source control) 

 

# Installation 

Ensure prerequisites are installed. 

Clone the repository: https://github.com/lindani007/Shop-Pocket.git

Copy or add your app icon and splash images under Resources/Images/: 

Recommended names used in csproj: myicon.svg, myicon_foreground.svg, myicon_background.png, logo.svg 

If files do not exist, update SuperMarket.csproj to reference existing images. 

Restore and build: 

Run on a platform: 

Android emulator or device:dotnet build -f net10.0-android 
or run from Visual Studio with an Android target. 

iOS / Mac Catalyst: build on macOS with Xcode installed. 

Windows: set the Windows target and run (if supported on your machine). 

 

 # Usage 

App flow highlights: 

Login page: This is the first page the app starts on. choose user type (Employer or Employee) and authenticate.  

Username Entry 

     You can enter your username or name here, both are allowed. 

Password Entry 

Your password you set when registering 

 

NOTE:  As an EMPLOYER you can login as employer and employee with the same credentials 
![login](https://github.com/user-attachments/assets/dc97c259-f498-4839-a217-a9586d3834e1)

 

Employee Page: self-service features such as Check Price, Card Fees, and Quick Withdraw. Click a button to navigate to the self-service you want to do. 
![emplyee](https://github.com/user-attachments/assets/365dabe2-899d-43ed-8943-5776bc8e99ad)

 

Stock page: add incoming stock, set cost/pack cost, stage additions, and commit with Done. 

 ![stock](https://github.com/user-attachments/assets/7ea81434-536d-47cb-b554-2916d821a9fb)


Store page: selling workflow for attendants to ring up purchases. 

Profit pages: view transaction summaries, income, cost, and profit for selected products. 

Settings & Security: change product info, password recovery pages, and basic user verification. 

Important notes: 

The app uses local JSON files for persistence (stock.json, availableStock.json, transactions files). 

Adding stock is a two-step flow: input/batch staging, then Done will persist the staged list to the file(s). 

Some operations update multiple files (e.g., adding stock updates both incoming-stock file and available-stock file). 

Use the built-in UI elements to search and select items; the CollectionView lists product names. 

 

# Roadmap 

##Planned improvements: 

Replace JSON file storage with a lightweight embedded database (SQLite) for concurrency and reliability 

Add unit and integration tests for core flows (stock, transactions, pricing) 

Improve UI responsiveness and add progress indicators on long-running operations 

Add localization and currency formatting settings 

Add export/import (CSV) for inventory and transactions 

Implement role-based access controls and audit logs 

 

# Contributing 

Contributionsare welcome. Please follow these steps: 

Fork the repository. 

Create a feature branch: 

Commit your changes with clear messages and follow project code style. 

Run tests (if added) and ensure build succeeds. 

Open a pull request describing the change and rationale. 

Please follow this repo's CONTRIBUTING.md and .editorconfig for style and commit guidance. 

 

# License 

This project is provided under the MIT License. See LICENSE  file for details. 

 

# Contact 

Project maintainer: Lindani  

Email : lindanidev@outlook.com 

Repository:  https://github.com/lindani007/Shop-Pocket.git

 

# Acknowledgments 

## Third-party libraries and resources used: 

.NET MAUI templates and docs 

CommunityToolkit.Mvvm 

Microcharts.Maui 

BCrypt.Net-Next 

Iconsor starter assets (update attribution as needed if you add third-party artwork) 

 

# File & Component Map (brief) 

SuperMarket.csproj — project file and platform settings (application title, icons, splash config). 

Resources/Images/ —icons and splash images used by the project. 

Pages/ — XAML pages and code-behind: 

Login.xaml(.cs) — authentication UI and logic. 

EmployeePage.xaml(.cs) — employee self-service UI. 

Stock.xaml(.cs) — stock management and add-stock staging. 

Store.xaml(.cs) — selling workflow. 

Profit*.xaml(.cs) — reporting/profit pages. 

Models/ — data models (e.g., Products, helper classes). 

JsonData/ — JSON persistence helpers (read/write/update JSON files). 

Transactions/ — transaction and profit calculation helpers. 

Security/ — login/verification helpers and password hashing. 

Resources/Fonts — custom fonts. 

Resources/Raw/ — raw assets (where applicable). 

 

# Line-by-line explanation 

Below is a concise explanation for each key line or block in this README to clarify intent. 

Shop Pocket Project title shown at the top of README. 

Short project summary one-line description of what the app does. 

 visual separator for sections. 4–9. About The Project section — explains purpose, primary features, and intended users. 10–14. BuiltWith — lists core frameworks and libraries used by the app. 15–24. Getting Started — clone and build quick steps to get the repo locally. 25–30. Prerequisites — software and SDKs required before building. 31–43. Installation — explicit clone/restore/build instructions plus asset notes for icons and splash. 44–61. Usage — describes major pages and behavior, and important notes about JSON persistence and workflows. 62–69. Roadmap — planned future improvements and higher priority items. 70–78. Contributing — how to contribute (fork, branch, PR) and reference to repo contributing rules. 79–82. License — licensing statement (MIT) and pointer to LICENSE file. 83–86. Contact — placeholder contact info and repo link; should be updated. 87–92. Acknowledgments — credits third-party libraries and resources used. 93–110. File & Component Map — maps repository directories and major responsibilities to help new contributors navigate the codebase. 

 

 

 

 


 


