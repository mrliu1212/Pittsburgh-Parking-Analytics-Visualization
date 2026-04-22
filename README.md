# Pittsburgh Parking Analytics — Data Cleaning & Visualization

## Overview
This project focuses on heavy data cleaning and visualization using public parking data from Pittsburgh. The goal is to transform messy, independently collected datasets into analysis-ready data and uncover insights about parking demand, pricing, and utilization.

Using 2M+ transaction records along with meter and space data, this project builds an end-to-end data pipeline and uses visualization to explore spatial-temporal patterns and system inefficiencies.

---

## Datasets
This project uses publicly available datasets from the Western Pennsylvania Regional Data Center (WPRDC):

- [Parking Meter Information](https://data.wprdc.org/dataset/parking-meters-pittsburgh-parking-authority/resource/72fff5c4-5ef2-4437-9e40-e2d999d455ed)  
- [Payment Transactions across Meters](https://data.wprdc.org/dataset/parking-transactions/resource/1ad5394f-d158-46c1-9af7-90a9ef4e0ce1)  
- [Space Counts and Rates](https://data.wprdc.org/tl/dataset/zone-and-lot-attributes/resource/4d4a0668-7905-4db6-985e-f7575a9e3160)  

These datasets were collected independently and required extensive cleaning, standardization, and key normalization before integration.

---

## Key Features
- End-to-end data cleaning and integration pipeline  
- Standardization and normalization of heterogeneous datasets  
- Multi-source dataset merging with consistent join keys  
- Interactive visualizations using Altair  
- Analysis of spatial-temporal demand and pricing patterns  

---

## Results
- Identified strong variation in parking demand across locations and time  
- Discovered pricing-demand mismatches  
- Found up to **6× revenue-efficiency gaps**  
- Built a simple parking recommendation approach based on demand and utilization  

Start here: `main_notebook.ipynb` for final results and visualizations  

---

## Data Pipeline

### 1. Data Cleaning
- Handle missing values and inconsistencies  
- Standardize formats and column names  
- Reshape datasets into tidy format  

### 2. Data Integration
- Normalize join keys across datasets  
- Merge meter, transaction, and space datasets  
- Produce final analysis-ready tables  

### 3. Visualization & Analysis
- Explore spatial patterns (by location/zone)  
- Analyze temporal trends (hourly, daily usage)  
- Compare pricing vs. utilization  

---

## Project Structure

```
.
├── main_notebook.ipynb        # Final analysis and visualizations
├── cleaning/
│   ├── dataset_cleaning/
│   │   ├── raw/               # Raw datasets from WPRDC
│   │   └── *.ipynb            # Cleaning & EDA per dataset
│   └── datasets_join.ipynb    # Key normalization & merging
└── final_datasets/            # Cleaned and merged datasets
```
---

## Notes
- Cleaning workflow follows **Tidy Data principles (Hadley Wickham)**  
- Each notebook documents cleaning decisions and transformations  
- Focus is on **data quality + visualization**, not heavy modeling  

---

## Future Work
- Demand prediction models  
- Pricing optimization  
- Interactive dashboard (Streamlit or similar)


## Data Availability

Due to GitHub file size limitations, the raw datasets are not included in this repository.

To reproduce this project:
1. Download the datasets from the links in the **Datasets** section above  
2. Place the files into the following directory:

```
cleaning/dataset_cleaning/raw/
```

Make sure the folder structure matches the project layout so the notebooks can load the data correctly.

After placing the data, you can run the cleaning and analysis notebooks as provided.
