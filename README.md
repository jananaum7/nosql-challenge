# nosql-challenge

# Eat Safe, Love

A MongoDB data project for exploring UK food establishments and analyzing food safety standards based on hygiene ratings and location data.

## Table of Contents
- [Overview](#overview)
- [Setup](#setup)
- [Data Import Instructions](#data-import)
- [Usage](#usage)
- [Key Insights](#key-insights)
- [Contributors](#contributors)

## Overview
This project utilizes MongoDB to examine the food safety standards of establishments across the UK. The two primary notebooks include:
- **NoSQL_setup_starter.ipynb**: Guides through MongoDB setup and data import.
- **NoSQL_analysis_starter.ipynb**: Provides queries and data analysis to derive insights from food hygiene scores and ratings.

## Setup
### Requirements
- **MongoDB** (default port `27017`)
- **Python 3.12.4** with packages:
  ```bash
  pip install pymongo pandas
  ```
   - Start Jupyter Notebook:
     ```bash
     jupyter notebook
     ```

## Data Import Instructions
Data for this project is imported from a JSON file (e.g., `establishments.json`). To import the data into MongoDB, use the following command:

```bash
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
```
## Usage
Database Setup: Follow NoSQL_setup_starter.ipynb to confirm MongoDB connection and data import.
Data Analysis: Use NoSQL_analysis_starter.ipynb to perform various queries, analyze ratings, and extract insights on food establishments.

## Key Insights
1. Establishments with High Hygiene Issues: Identified establishments with a hygiene score of 20.
   - Count: Displays total results and the first 10 entries, highlighting those with the highest hygiene risk.
2. High-Rated Establishments in London: Queried establishments in London with a RatingValue of 4 or above.
   - Count: The query returns establishments with high ratings within the capital, detailing top-rated establishments.
3. Nearby Establishments to Penang Flavours:
   - Extracted data for establishments near "Penang Flavours" with a RatingValue of 5, sorted by the lowest hygiene scores for quality comparisons.
4. Local Authority Hygiene Overview: Aggregated establishments with a hygiene score of 0, grouped by Local Authority.
   - Top Authorities: Displays the authorities with the highest number of establishments with zero hygiene scores, revealing areas for potential health interventions.

## Contributers
J. Naum

