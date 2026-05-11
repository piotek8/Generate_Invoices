# WodyApp 💧

Desktop WPF application for automatic invoice generation in the iFirma system based on Excel file data.

![.NET](https://img.shields.io/badge/.NET-10.0-purple)
![Platform](https://img.shields.io/badge/Platform-Windows-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Description

WodyApp automates the VAT invoice generation process. The application:
- Reads customer and order data from an Excel file
- Automatically logs into the iFirma system
- Creates invoices with warehouse products and services
- Fills quantities, unit prices, and invoice items
- Supports product list pagination

## 🖼️ Screenshots

## ✨ Features

- **Excel Import** — supports `.xlsx`, `.xls`, `.xlsm` formats
- **Browser Automation** — Playwright for interaction with iFirma
- **Warehouse Products** — automatic adding from warehouse dialog
- **Services and Subscriptions** — adding from products/services list
- **Pagination** — support for multi-page product lists
- **Secure Login** — credentials stored in Windows Credential Manager

## 🛠️ Technologies

- **.NET 10** — Windows Presentation Foundation (WPF)
- **Playwright** — Chromium browser automation
- **ClosedXML** — Excel file reading
- **WPF UI** — modern user interface

## 📁 Project Structure

```text
WodyApp/
├── App.xaml              # WPF application configuration
├── MainWindow.xaml       # Main UI window
├── WebService.cs         # iFirma automation logic
├── Models.cs             # Data models (Invoice, RozliczenieHeaders)
├── ExcelReader.cs        # Excel data reading
└── README.md             # This file
```

## 🚀 Installation

### Requirements
- Windows 10 or newer
- .NET 10 Runtime
- iFirma account

### Run from source code

```bash
# Clone repository
git clone https://github.com/piotek8/WodyApp.git
cd WodyApp

# Install Playwright browsers
pwsh bin/Debug/net10.0-windows/playwright.ps1 install

# Run application
dotnet run
```

### Credentials Configuration

Run `SaveCredentials.bat` and provide:
- iFirma login
- iFirma password
- API key (Settings → API → Key)

## 📊 Excel File Format

The application expects an Excel file with a predefined column structure containing:
- Customer identification data
- Product quantities
- Unit prices

Detailed column specification is available in the internal documentation.

## 🔧 Configuration

The application automatically recognizes:
- **Warehouse products**
- **Services**

## 👤 Author

Project created for invoice process automation.
