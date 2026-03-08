# Data Dictionary

## Dataset Metadata
- Dataset names: 1) NTAD_Fatality_Analysis_Reporting_System_2022_Accidents_5525296034756280586.csv; 2) NTAD_Fatality_Analysis_Reporting_System_2023_Accidents_-1547396067495048743.csv  
- Created on: April 17, 2025  
- Created from: US DOT Bureau of Transportation Statistics  
- Primary source(s): Fatality Analysis Reporting System (FARS) 2022 - Accidents, Fatality Analysis Reporting System (FARS) 2023 - Accidents  
- Geographic scope: ALASKA, CALIFORNIA, DISTRICT OF COLUMBIA, FLORIDA, GEORGIA, RHODE ISLAND, TEXAS, VERMONT  
- Time coverage: YEARS 2022 and 2023  
- License / usage constraints:  
  These NTAD datasets are works of the United States government as defined in 17 U.S.C. § 101 and as such are not protected by any U.S. copyrights. This work is available for unrestricted public use.  

## File Names and Attribute Descriptions
**File name: NTAD_Fatality_Analysis_Reporting_System_2022_Accidents_5525296034756280586.csv**  
- **Layout**: .csv format  
- **Number of rows**: 39,681  
- **Number of columns**: 80  

**File name: NTAD_Fatality_Analysis_Reporting_System_2023_Accidents_-1547396067495048743.csv**  
- **Layout**: .csv format  
- **Number of rows**: 37,951  
- **Number of columns**: 80  
- **Column (Attributes) - 2022 and 2023 Datasets**:  
```
STATE:  Long integer  
STATENAME:  Character string  
ST_CASE:  Long integer  
PEDS:  Long integer  
PERNOTMVIT:  Long integer  
VE_TOTAL:  Long integer  
VE_FORMS:  Long integer  
PVH_INVL:  Long integer  
PERSONS:  Long integer  
PEMVIT:  Long integer  
COUNTY:  Long integer  
COUNTYNAME:  Character string  
CITY:  Long integer  
CITYNAME:  Character string  
MONTH:  Long integer  
MONTHNAME:  Character string  
DAY:  Long integer  
DAYNAME:  Character string  
DAY_WEEK:  Long integer  
DAY_WEEKNAME:  Character string  
YEAR:  Long integer  
HOUR:  Long integer  
HOURNAME:  Character string  
MINUTE:  Long integer; value: 0 - 59
MINUTENAME:  Character string  
TWAY_ID:  Character string  
TWAY_ID2:  Character string  
ROUTE:  Long integer  
ROUTENAME:  Character string  
RUR_URB:  Long integer  
RUR_URBNAME:  Character string  
FUNC_SYS:  Long integer  
FUNC_SYSNAME:  Character string  
RD_OWNER:  Long integer  
RD_OWNERNAME:  Character string  
NHS:  Long integer  
NHSNAME:  Character string  
SP_JUR:  Long integer  
SP_JURNAME:  Character string  
MILEPT:  Long integer  
MILEPTNAME:  Character string  
LATITUDE:  Long integer  
LATITUDENAME:  Character string  
LONGITUD:  Long integer  
LONGITUDNAME:  Character string  
HARM_EV:  Long integer  
HARM_EVNAME:  Character string  
MAN_COLL:  Long integer  
MAN_COLLNAME:  Character string 
RELJCT1:  Long integer  
RELJCT1NAME:  Character string  
RELJCT2:  Long integer  
RELJCT2NAME:  Character string  
TYP_INT:  Long integer  
TYP_INTNAME:  Character string  
REL_ROAD:  Long integer  
REL_ROADNAME:  Character string  
WRK_ZONE:  Long integer  
WRK_ZONENAME:  Character string  
LGT_COND:  Long integer  
LGT_CONDNAME:  Character string  
WEATHER:  Long integer  
WEATHERNAME:  Character string  
SCH_BUS:  Long integer  
SCH_BUSNAME:  Character string  
RAIL:  Long integer  
RAILNAME:  Character string  
NOT_HOUR:  Long integer  
NOT_HOURNAME:  Character string  
NOT_MIN:  Long integer  
NOT_MINNAME:  Character string  
ARR_HOUR:  Long integer  
ARR_HOURNAME:  Character string  
ARR_MIN:  Long integer  
ARR_MINNAME:  Character string  
HOSP_HR:  Long integer
HOSP_HRNAME:  Character string  
HOSP_MN:  Long integer  
HOSP_MNNAME:  Character string  
FATALS:  Long integer  
```

## Standardization Rules
- State names normalized to a single format  
- Coding added to accommodate rollover to midnight hour  
- Hour values range from 0 - 23  
- Minute values range from 0 - 59  
- Additional hour/minute values:  
  - 88 – Not Applicable or Not Notified  
  - 98 - Unknown if notified/if arrived  
  - 99 – Unknown MIN/HR, Officially Cancelled, Unknown if transported, or Unknown if arrived  

## Assumptions and Limitations
- In the FARS dataset, EMT arrival times coded as 97–99 do not indicate clinical outcomes. These administrative codes represent missing, unknown, or not reported values rather than meaningful clinical information. Therefore, no inference can be made regarding whether the victim had expired prior to EMT arrival.
- The state of Florida had missing/unknown/unreported values for majority of the attributes listed in the datasets.  As a result, the data is skewed.  Unable to ascertain whether the omitted values are a result of state policy or other unmentioned factors.
- The Fatality Analysis Reporting System (FARS) 2022 Final Release - Fatal Motor Vehicle Accidents datasets were compiled from January 1, 2022/2023 to December 31, 2022/2023 by the National Highway Traffic Safety Administration (NHTSA) and are part of the U.S. Department of Transportation (USDOT)/Bureau of Transportation Statistics (BTS) National Transportation Atlas Database (NTAD). These geospatial datasets are the accident files from the FARS 2022/2023 Final Release Data. The Final Release Data is published 12-15 months, after the initial release of FARS, and could contain additional fatal accidents due to the delay in police reporting, toxicology reports, etc., along with changes to attribute information for previously reported fatal accidents. This data files contain information about crash characteristics and environmental conditions at the time of the crash. There is one record per crash.
- The FARS Fatal MVS datasets utilized for this EDA are subsets of the NTAD, resulting in an elimination of greater than 50 attributes thus limiting the scope of the analyses.  A sample of attributes removed for are:
    - P8/NM10 Injury Severity – describes the severity of injury to the person in the crash using a KABCO scale.  E.g. 4 = Fatal Injury,  6 = Died Prior to Crash; P21/NM23 Died at Scene/En Route – if person died at scene of crash or enroute to medical facility; P23A/NM23A Hour of Death – hour of person’s death; P25A/NM25B Minute of Death – minutes after hour of person’s death; P100A Lag Hours – hours between time of crash and person’s time of death were eliminated from the datsets.  

---

## Provenance
- Raw file/API endpoints: https://geodata.bts.gov/datasets/usdot::fatality-analysis-reporting-system-fars-2022-accidents/explore?location=44.631047%2C-112.477350%2C3&showTable=true  
  https://geodata.bts.gov/datasets/usdot::fatality-analysis-reporting-system-fars-2023-accidents/explore?location=44.631047%2C-112.477350%2C3&showTable=true  
---
- Extraction date: 2026-01-25  
- Transformation notebook/script: DSCI_521_Project_Scope.ipynb  
- Output analyses:   
** MVA Crash by Time of Day - 2022 and 2023  
** MVA Crash Construction Zone Impact - 2022 and 2023  
** Notification of MVA Crash / EMT Arrival Lag-time - 2022 and 2023, Rural vs Urban  
** EMT Transit Time from Crash Site to Hospital Facility - 2022 and 2023, Rural vs Urban  
** Type of Harm - 2022 and 2023 

## Change Log
| Date | Version | Author | Change summary |
| :--- | :--- | :--- | :--- |
| 2026-03-04 | v0.0 | Sharon Robinson | Initial draft |
| 2026-03-07 | v1.0 | Sharon Robinson | 1st amendment |