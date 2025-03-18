---
title: Scan tool
description: Check out how you can dump and inspect the currently available strands of a Ballerina program.
keywords: ballerina runtime, troubleshoot, scan, thread dump
permalink: /learn/scan-tool/
active: scan-tool
---

The Ballerina scan tool is a static code analysis tool performs analysis on Ballerina projects and identifies potential code smells, bugs, and vulnerabilities without executing them.

>**Note:** Ballerina Scan is an experimental feature, which supports only a limited set of rules.


## Install the tool

Execute the command below to pull the scan tool from [Ballerina Central](https://central.ballerina.io/ballerina/wsdl/latest).

```sh
bal tool pull scan
```

## Usage Guide for Ballerina Scan Tool

The Ballerina Scan tool helps you analyze your Ballerina project for potential issues, enforce coding standards, and generate detailed reports. Below are various ways you can use the tool to fit your development workflow.

### Scan a Ballerina project

To run a full analysis across all Ballerina files in your project, use the following command:

```bash
bal scan --scan-report
```

This will produce the HTML report and scan results inside `target/report` directory

### List All Available Analysis Rules

If you’d like to explore the full set of rules the tool can apply, run:

```bash
bal scan --list-rules
```

This will display a comprehensive list of available rules for your project, which you can include or exclude in future scans.

### Run Analysis for Specific Rules

If you want to apply a specific set of rules, list them as a comma-separated string by specifying the rule ID:

```bash
bal scan --include-rules="ballerina:1, ballerina/io:2"
```

To ignore a specific set of rules during the analysis, use the following command:

```bash
bal scan --exclude-rules="ballerina:1, ballerina/io:2"
```
