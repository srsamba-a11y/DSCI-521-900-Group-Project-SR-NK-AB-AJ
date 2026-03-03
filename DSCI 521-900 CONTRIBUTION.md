# Contributing  

Thanks for your interest in contributing to this project.  

## Scope  

This repository focuses on building a reproducible, multi-state dataset from Bureau of Transportation (BTS) Fatality Analysis Reports (FARS) for the years 2022 and 2023.  That datasets were pulled from kaggle.com, which are subsets of the original BTS FARS datasets. The following 8 states are included in this analysis:    

* Alaska  
* California
* District of Columbia  
* Florida  
* Georgia  
* Rhode Island
* Texas
* Vermont  

## How to Contribute  

1. Fork the repository and create a feature branch.  
2. Make focused changes (one logical update per pull request).  
3. Include a short summary of what changed and why.  
4. Open a pull request with evidence that your changes run correctly.  

## Contribution Checklist  

Before opening a pull request:  

- Confirm source URLs are public and stable  
- Document variables added/changed in the data dictionary  
- Describe all cleaning and standardization steps  
- Note assumptions (date or time conversions, missing value logic)  
- Verify outputs are reproducible from notebook/script steps  

## Data Standards  

Use these standards for all new or changed data:  

- Retain one row per state-year for core tables  
- Use consistent state names; if using state abbreviations adhere to the ISO
  3166-2 codes for US states   
- Standardize column names  
- Preserve units in column definitions  
- Do not overwrite raw source files; develop transformed outputs separately  

## Pull Request Format  

Please include:  

- Problem statement  
- Data source(s) used  
- Processing steps performed  
- Output files produced  
- Limitations or caveats  

## Code and Notebook Expectations  

- Notebooks and scripts should be readable and modular  
- Avoid hard-coded local machine paths  
- Prefer deterministic transformations  
- Add brief markdown notes before complex processing blocks  

## Reporting of Issues  

When filing an issue, include:  

- Expected behavior  
- Actual behavior  
- Steps to reproduce  
- File names and sample rows (if relevant)  

## Team Roles & Attribution  
**Nikita Lenard:  EDA Lead**: Authored project scope; executed data extractions from kaggle.com BTS FARS .csv files; developed Google Collab Python notebook, including project scope, implementation and Power Point shells; conducted Accident Patterns by Time of Day analysis  
**Sharon Robinson:  Documentation Lead & EDA Team Member**: Authored project README.md, DATA DICTIONARY.md, and CONTRIBUTIONS.md documents; creation and management of GitHub repository and version synchronization; conducted Notification of MVA Crash to EMT Arrival lag-time and EMT Transport to Medical Treatment Facility lag-time analyses  
**Alvin Boakai:  EDA Team Member**: Conducted Construction Zone Crashes per State analyses  
**Ashokkumar Jangid:  EDA Team Member**: Conducted Multiple Fatalities by State analyses  

## Team Contacts  

- Nikita Lenard — nl578@drexel.edu  
- Sharon Robinson — slr424@drexel.edu  
- Ashokkumar Jangid - abj53@drexel.edu  
- Alvin Boakai - asb424@drexel.edu
