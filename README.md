# Infosec_Process_Automation

## 6way Analysis

Organization-wide process improvement for Information Security Department was conducted. These processes that were done manually every week were first understood then replicated 
in code to streamline and automate for ease of use.

      - 6way_analysis.ipynb

This code performs reconciliation and analysis across 6 data sources:

- Deferred onboarding data 
- Infosec employee data
- Contractor data
- US employee database
- Gmail data
- MDM data
- India AD data
- Biometric data

## Overview

The main steps are:

1. Read in and preprocess each data source into a standard format
2. Merge data sources into an employee master dataset
3. Reconcile employee master against Gmail, MDM, AD, Biometric to identify mismatches
4. Analyze for active employees missing in Gmail, AD  
5. Analyze for inactive employees still present in Gmail, MDM, AD, Biometric
6. Additional analysis on Gmail, MDM, AD, Biometric

## Running the Code 

- Import required libraries (pandas, numpy, openpyxl, xlrd)
- Update file paths to point to latest data source files
- Call `saving()` function to execute full analysis 
- Results output to Excel file `6way_Final.xlsx` with separate sheets for each data source, reconciliation, and analysis

## Configuration

- Set `decide` variable to 'yes' or 'no' to control whether to vlookup employee id for AD analysis
- Update `file_paths` at the top to point to latest data files

## Outputs

- `Reconciliation` sheet shows employee master merged against all systems
- Individual sheets for each system's raw data
- `Analysis A+I` shows inactive users still active in systems
- `Raw Analysis` shows additional ad hoc analysis for each system
- `Gmail Analysis` shows Gmail accounts not tied to employee

## Documentation 

A document was also created for knowledge transfer.

      - 6way_Documentation.pdf
