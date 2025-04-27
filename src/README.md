# TrxToHtml

A tool to convert `.trx` test results files into clean HTML reports.

> **Note:** This project is a fork of [SamhammerAG/TrxToHtml](https://github.com/SamhammerAG/TrxToHtml), updated for .NET 9 compatibility.

## Version 1.0.8 Update

### Changes
- Upgraded to **.NET 9.0** to ensure compatibility with GitHub Actions runners
- Updated NuGet packages to their latest versions:
  - Scriban **6.2.1**
  - CommandLineParser **2.9.1**
  - Microsoft.Extensions.FileProviders.Embedded **9.0.4**

### Bug Fixes
- Resolved template parsing issues introduced by the newer Scriban version

### Note
The core functionality remains unchanged.  
This update focuses on framework and package upgrades to maintain compatibility with the latest .NET version and GitHub Actions runners.

## Installation

```bash
dotnet tool install -g Samhammer.net9.TrxToHtml
```

## Usage

```bash
trx-to-html-net9 [options]
```

### Options
- `-s, --searchPattern` — Search pattern to scan for `.trx` files (default: `"*.trx"`)
- `-n, --outputFileName` — Name of the output HTML file (default: `"TestResults.html"`)
- `-o, --outputDirectory` — Target directory for the output HTML file (default: `"."`)
- `-w, --workingDirectory` — Directory to recursively scan for `.trx` files (default: `"."`)
- `-t, --templateFile` — Path to a custom template file used for generating the HTML
- `-a, --all` — Process all matching `.trx` files; if omitted, only the latest `.trx` file per folder is processed

## License

[MIT](LICENSE)
