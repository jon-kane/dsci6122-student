# DSCI 6122: R Lab for Applied Data Science — Student Resource Repository

Welcome to the student resource repository for **DSCI 6122: R Lab for Applied Data Science** at Mississippi State University. 

This repository contains all official datasets, supplementary cheatsheets, and reference materials required for your laboratory notebooks, weekly assignments, midterm practicum, and final practicum.

---

## 📂 Repository Structure

- **`data/`**: Module-specific datasets used across programming notebooks, data wrangling exercises, lab assignments, and practicums. See `data/data-catalog.md` for a detailed description of all datasets.
- **`extra-materials/`**: Reference cheatsheets (PDF format) for core R packages and data science workflows.

---

## 📊 Datasets Directory Summary (`data/`)

Datasets are organized into subdirectories by module and practicum:

| Folder | Topic / Activity | Key Datasets & Files |
| --- | --- | --- |
| `module-01/` | R Basics & Intro to Tidyverse | `spiderman.txt`, `collegefootballbowl.csv`, `gapminder-life-expectancy.csv` |
| `module-02/` | Common Data Structures & Tidying Data | `Bike-Data/`, `avg-tuition-multisheet.xlsx`, `got_chars.json`, `got_chars.xml`, `FPCPITOTLZGUSA.csv`, `MEPAINUSA672N.csv`, `MORTGAGE30US.csv`, `MSPUS.csv`, `plant-cooking/`, `plant-refrigeration/`, `plant-ventilation/` |
| `module-03/` | Acquiring & Wrangling Data from R Packages | `recall-msrp-data.rds`, `sp500-ranked-2000-2022.rds`, `sp500-ranked-2000-2022-se.rds` |
| `module-04/` | Handling Missing Values | `weather-data.rds` |
| `module-05/` | ML Data Prep & Feature Selection | `car-data.rds` |
| `module-06/` | Text Data & NLP | `austen-books.rds`, `imdb-dataset.rds`, `enron-subset-se.rds` |
| `module-07/` | Working with Excel Data | `avg-tuition-multisheet2.xlsx`, `cheese_per_cap.xlsx`, `sales-data/` |
| `module-08/` | Visual Data Exploration | `assets.csv`, `debts.csv`, `surface-temperature.rds`, `train-test.rds` |
| `module-09/` | Assessing & Ensuring Data Quality | `widget-orders-synthetic.rds`, `student-enrollment-data-full.rds` |
| `module-10/` | GIS & Geographical Data | `census-map-data.rds`, `ms-hospitals.rds` |
| `module-11/` | Ethical Web Scraping & APIs | `video-game-console-data.csv` |
| `midterm/` | Midterm Online Practicum | `penguins.rds`, `diamonds.rds`, `sleep.rds`, `sms-spam.rds` |
| `final/` | Final Online Practicum | `data-to-validate.rds`, `taxi_zones.zip` |

> **Note on Large Datasets:** Datasets exceeding 30 MB—including the Enron email dataset (`emails.csv` / `enron-subset-*.rds`) in Module 06 and the 2024 NYC Yellow Cab Parquet dataset (`yellow_tripdata_2024-*.parquet`) in Module 12—are provided separately through Canvas / cloud storage.

---

## 📑 Extra Materials Directory (`extra-materials/`)

Supplementary cheatsheets to assist you with R packages throughout the course:
- **`data-import.pdf`**: Reading files into R using `readr`, `readxl`, and `DBI`.
- **`data-tidying.pdf`**: Reshaping and tidying data with `tidyr`.
- **`data-transformation.pdf`**: Data manipulation verbs with `dplyr`.
- **`data-visualization.pdf`**: Visual customization and aesthetics with `ggplot2`.
- **`lubridate.pdf`**: Working with dates and time-series data in R.
- **`facets of R.pdf`**: High-level reference of R language features and data structures.

---

## 🚀 Getting Started

All data is available through Canvas, but if you want to get it all at once:

1. **Clone the repository** to your local environment:
   ```bash
   git clone https://github.com/jon-kane/dsci6122-student.git
   ```

2. **Loading datasets**: Reference dataset file paths relative to your working directory or point directly into `data/module-XX/` (e.g., `readRDS("data/module-05/car-data.rds")`).
