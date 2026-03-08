# DSCI 521-900 Term Project (EDA)

## Scope: To perform a root-cause analysis of motor vehicle-related fatalities and identify contributing factors and conditions
- A selection of 8 states will be the focus of this analysis:
  - Alaska
  - California
  - District of Columbia
  - Florida
  - Georgia
  - Rhode Island
  - Texas
  - Vermont

---

## Why this project is useful
- Provide insights that can improve roadway safety by identifying high-risk conditions pertaining to weather, road construction, signage
- Identify lag times between crash notification and EMS/EMT arrival, and EMS/EMT lag times from crash sites to medical treatment facilities

---

## Planned dataset contents
- Fatality Analysis Reports - Motor Vehicle Accidents for years 2022 and 2023

---

## Data sources
Primary sources include:
- US DOT Bureau of Transportation Statistics Fatality Analysis Reporting System 2022 and 2023

---

## Getting started: prerequisites
- Python 3.13+
- Jupyter Notebook (recommended)

Install dependencies:

---

## Quick sample pull
```python
from google.colab import drive
drive.mount('/content/drive')

import pandas as pd
import csv
FARS_2022 = pd.read_csv('/content/drive/MyDrive/NTAD_Fatality_Analysis_Reporting_System_2022_Accidents_5525296034756280586.csv')
FARS_2023 = pd.read_csv('/content/drive/MyDrive/NTAD_Fatality_Analysis_Reporting_System_2023_Accidents_-1547396067495048743.csv')

FARS_2022.head()

attribute_counts = FARS_2022.groupby('STATENAME').size() #grouping by attribute STATENAME
attributes_sorted = attribute_counts.sort_values(ascending=False) #sorting by most to least

attribute_counts2 = FARS_2023.groupby('STATENAME').size()
attributes_sorted2 = attribute_counts2.sort_values(ascending=False)
```

---

## Expected output
- Cleaned FARS tabular extract for selected years and states

---

## Reproducibility notes
- Normalize state names
- Document missing values and source-specific limitations in a data dictionary

---

## Project documentation
- Contribution guide: DSCI 521-900 CONTRIBUTION.ipynb
- Data dictionary starter: DSCI 521-900 DATA DICTIONARY.ipynb

---

## Limitations
- Missing and/or unreported data
- Data quality and transparency vary by state

---

## Where to get help
For questions about scope, preprocessing choices, or source interpretation:
- Nikita Leonard — nl578@drexel.edu
- Sharon Robinson — slr424@drexel.edu
- Alvin Boakai — asb424@drexel.edu
- Ashokkumar Jangrid — abj53@drexel.edu

---

In Git repository, use Issues for bug reports and data-quality notes

---

## Maintainers and contributors
- Nikita Leonard
- Sharon Robinson
- Alvin Boakai
- Ashokkumar Jangrid

Contributions are welcome through pull requests with clear notes on:
- Source files used
- Cleaning and standardization logic
- Any assumptions introduced during preprocessing
