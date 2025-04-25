# TrxToHtml

A tool to convert TRX (Visual Studio Test Results) files to HTML reports.

## Version 1.0.7 Update

### Changes
- Upgraded to .NET 9.0 to ensure compatibility with GitHub Actions runners
- Updated NuGet packages to their latest versions:
  - Scriban 6.2.1
  - CommandLineParser 2.9.1
  - Microsoft.Extensions.FileProviders.Embedded 9.0.4

### Bug Fixes
  - Resolved template parsing issues with newer Scriban version

### Note
The core functionality remains unchanged. This update primarily focuses on framework and package upgrades to ensure compatibility with the latest .NET version and GitHub Actions runners.

## Installation

```bash
dotnet tool install -g Samhammer.net9.TrxToHtml
```

## Usage

```bash
trx-to-html-net9 [options]
```

### Options
- `-s, --searchPattern`: Search pattern to scan for trx files (default: "*.trx")
- `-n, --outputFileName`: Name for the html file (default: "TestResults.html")
- `-o, --outputDirectory`: Target directory for the html file (default: ".")
- `-w, --workingDirectory`: Directory to scan recursive for trx files (default: ".")
- `-t, --templateFile`: Path of template file used to create the html file
- `-a, --all`: Process all matched trx files, otherwise only latest trx file per folder

## License

MIT 
