# DSCI 6122 Data Catalog

## Overview

This data catalog summarizes the dataset files, course topics, assignments, and practical exercises across all modules in **DSCI 6122**.

---

## Course Summary Table

| Module | Module Topic | Activity / Notebook | Datasets / Files | Notes & Description |
| --- | --- | --- | --- | --- |
| **00** | Intro | Introductory Notebook | *None* | Students complete a "Hello World" notebook. |
| **01** | R basics and intro to tidyverse | Programming Notebook | `spiderman.txt` | Small key/value text file to illustrate reading in a text file. Used in Dr. Joe's lab. |
|  |  | Data Wrangling Notebook | `collegefootballbowl.csv` | Historical records of college football bowl games. Used in Dr. Joe's lab. |
|  |  | Assignment | `gapminder-life-expectancy.csv` | Dataset from gapminder.org restructured for easier analysis. Variables: `country`, `year`, and `life expectancy`. |
| **02** | Common data structures and tidying data | Programming Notebook | `Bike-Data/`<br>`avg-tuition-multisheet.xlsx`<br>`got_chars.json`<br>`got_chars.xml` | • **Bike-Data/**: Folder containing 63 CSV files with `date` and `bike_count` across 12 Seattle bike counters (TidyTuesday).<br>• **avg-tuition-multisheet.xlsx**: Average college tuition per state over several school years (multisheet, TidyTuesday).<br>• **got_chars.json/xml**: Game of Thrones character attributes from `repurrrsive` R package. |
|  |  | Data Wrangling Notebook | `FPCPITOTLZGUSA.csv`<br>`MEPAINUSA672N.csv`<br>`MORTGAGE30US.csv`<br>`MSPUS.csv` | FRED economic data on US housing cost metrics over time:<br>• **FPCPITOTLZGUSA.csv**: CPI Inflation.<br>• **MEPAINUSA672N.csv**: Real median personal income (2023 USD).<br>• **MORTGAGE30US.csv**: 30-year fixed rate mortgage average.<br>• **MSPUS.csv**: Nominal median sales price of houses sold. |
|  |  | Assignment | `plant-cooking/`<br>`plant-refrigeration/`<br>`plant-ventilation/` | Real-world manufacturing downtime data across 3 plants. Daily CSV files separated into 3 folders. Provided by CAVS-e industry partner. |
| **03** | Acquiring and Wrangling Data from R Packages | Programming Notebook | Stock Data<br>Economic Data<br>Weather Data | • **Stock Data**: Sourced via `tidyquant` (Yahoo Finance API) for AAPL & MSFT (2000–present).<br>• **Economic Data**: Sourced via `tidyquant` for 4 FRED economic series.<br>• **Weather Data**: Pulled from `weather.gov` via `httr2` (Vicksburg lat/long default), tidied from JSON, and visualized. |
|  |  | Data Wrangling Notebook | Vehicle Recall Data<br>Vehicle MSRP Data | • **Vehicle Recall**: Sourced from NHTSA API for various makes/models.<br>• **Vehicle MSRP**: Pulled via CarAPI (`carapi.app`) to analyze MSRP vs. recall counts. |
|  |  | Assignment | `sp500-ranked-2000-2022-se.rds`<br>Stock Data | • **sp500-ranked-2000-2022-se.rds**: Return rank dataframe for S&P 500 companies (2000–2022).<br>• **Stock Data**: Students fetch raw 2023–2024 S&P 500 stock data via `tidyquant`, format, summarize, and visualize. |
| **04** | Exploring, Discovering, and Handling Missing Values in Tabular Data, Including Time-Series Data | Programming Notebook | Synthetic Data<br>`airquality` | • **Synthetic Data**: Simple in-notebook generated synthetic data.<br>• **airquality**: Built-in daily NYC air quality dataset (156 obs, 6 vars, ~24% missing Ozone values). |
|  |  | Data Wrangling Notebook | `txhousing` | Built-in `ggplot2` dataset on Texas housing market. Used to observe missing values and perform imputation on `sales` (monthly house sales). |
|  |  | Assignment | `weather-data.rds` | Subset of `weatherAUS` (~15K daily weather obs across Australia from `rattle` package). Students identify missingness and perform imputation. |
| **05** | Preparing data for statistical analysis and machine learning | Programming Notebook | Synthetic Data | Simple synthetic datasets (`toy_data_fs`, `toy_data_fsc`, `toy_data`) for feature selection, scaling, and splitting. |
|  |  | Data Wrangling Notebook | `Bike-Data/` | Seattle bike count data joined with weather and holiday indicators for linear regression modeling and 10-fold cross-validation (`rsample`). |
|  |  | Assignment | `car-data.rds` | Augmented Kaggle car dataset. Predictive modeling of car `Price` including missing value/outlier removal, feature selection, and CV performance reporting. |
| **06** | Working with text data | Programming Notebook | `austen-books.rds`<br>`stop_words` | • **austen-books.rds**: Jane Austen novel texts.<br>• **stop_words**: Built-in `tidytext` stop words for string manipulation (`stringr`) and tokenization (`unnest_tokens`). |
|  |  | Data Wrangling Notebook | `imdb-dataset.rds` | 50,000 IMDB movie reviews with binary sentiment labels. Sentiment analysis with Bing lexicon, word clouds (`wordcloud`), and LASSO classification (`textrecipes`/`tidymodels`). |
|  |  | Extra Notebook | `dataset_mnist()` | Optional tutorial demonstrating `keras3` setup and deep learning classification on MNIST digits. |
|  |  | Assignment | `enron-subset-se.rds`<br>`emails.csv` | Subset of Enron email corpus. Students extract dates and message text, tokenize, calculate Bing sentiment scores, and plot sentiment time series. |
| **07** | Working with Excel data in R | Programming Notebook | `avg-tuition-multisheet2.xlsx` | Multisheet workbook of average college tuition. Demonstrates `readxl` (sheets, ranges, header handling) and `writexl` (exporting single/multiple sheets). |
|  |  | Data Wrangling Notebook | `cheese_per_cap.xlsx` | USDA per capita cheese consumption (1970–1994 and 1995–2017 sheets). Wrangling multi-sheet structure, linear modeling, and interactive stacked area charts (`plotly`). |
|  |  | Assignment | `sales-data.zip` | Archive of 50 individual salesperson Excel files (each with multiple customer ID worksheets). Batch reading and aggregation to analyze salesperson profit, top customers, and product metrics. |
| **08** | Visual data exploration with R | Programming Notebook | `economics`<br>`presidential`<br>`mtcars`<br>`gapminder`<br>Synthetic Surface Data | Principles of Grammar of Graphics in `ggplot2` (data, mapping, layers, scales, facets, coordinates, themes) and interactive `plotly` (3D scatter/surface, animations, `ggsave()`). |
|  |  | Data Wrangling Notebook | `assets.csv`<br>`debts.csv`<br>`surface-temperature.rds`<br>`train-test.rds` | • **assets.csv/debts.csv**: Balance sheet items for interactive Treemaps (`plotly`).<br>• **surface-temperature.rds**: 3D print thermal camera & spatial surface mapping.<br>• **train-test.rds**: 3D print mechanical stress/strain testing with regression confidence/prediction intervals. |
|  |  | Assignment | `iris`<br>`mtcars`<br>`got_chars.json` | Plot recreation challenge: parallel coordinates plot (`iris`), lower-triangular correlogram (`mtcars`), and interactive network graph of GOT character book appearances (`visNetwork`). |
| **09** | Assessing and ensuring data quality | Programming Notebook | `airquality`<br>Synthetic Data | Data quality dimensions (completeness, accuracy, validity, consistency, duplicates, outliers). Programmatic rule validation using `validate` (`validator()`, `confront()`). |
|  |  | Data Wrangling Notebook | `widget-orders-synthetic.rds` | Synthetic e-commerce orders from "Widget Wonders". Comprehensive data quality audit, rule validation (`validate`), cleaning/imputation, and post-cleaning verification. |
|  |  | Assignment | `student-enrollment-data-full.rds` | Synthetic university database (`enrollment`, `student_directory`, `course_catalog`). Students enforce SME business rules and clean/correct enrollment records. |
| **10** | Wrangling, exploring, and analyzing geographical data in R | Programming Notebook | `nc.shp`<br>Synthetic Rasters | Introduction to spatial GIS formats: vector data with `sf` (reading shapefiles, CRS, spatial joins `st_join()`, buffering) and raster data with `terra` (`crop()`, `mask()`, `extract()`). |
|  |  | Data Wrangling Notebook | `census-map-data.rds` | Mississippi county ACS demographic census shapefiles (2009–2023). Spatial-temporal analysis of population density, education, and median household income choropleth maps (`geom_sf` + `plotly`). |
|  |  | Assignment | `census-map-data.rds`<br>`ms-hospitals.rds` | Healthcare accessibility analysis. Spatial joins (`st_join()`, `st_within()`) to compute hospital beds per 1,000 residents and 10-mile spatial buffer coverage maps (`st_buffer()`, `st_union()`). |
| **11** | Scraping data from the web ethically and safely with R | Programming Notebook | Web HTML<br>`robots.txt`<br>JSONPlaceholder API | Ethical scraping principles (user-agents, rate limiting, `robots.txt`), static HTML parsing with `rvest`, REST API requests with `httr2`, and overview of headless browsers (`RSelenium`). |
|  |  | Data Wrangling Notebook | Wikipedia API<br>BLS API | Fetching console sales and generation HTML tables from Wikipedia via MediaWiki API (`rvest`), adjusting launch prices for inflation using Bureau of Labor Statistics CPI API (`httr2`), and interactive visualization. |
|  |  | Assignment | `video-game-console-data.csv` | Scrapes Wikipedia infoboxes for video game consoles via MediaWiki API, extracts RAM/memory specs, converts memory units, and plots launch cost per MB of RAM over time. |
| **12** | Using R to process big data | Programming Notebook | Synthetic Benchmark Data | High-performance I/O (`data.table::fread`, `vroom`), copy-on-modify memory management (`lobstr`, `data.table`), SQLite database connections (`DBI`, `dbplyr`), and parallel processing (`parallel`, `future`, `furrr`). |
|  |  | Data Wrangling Notebook | `Taxi-Data.zip`<br>(`yellow_tripdata_2024-*.parquet`) | 2024 NYC Yellow Cab trips Parquet dataset (~12 monthly files). Lazy querying with `arrow::open_dataset()`, out-of-memory feature engineering, and parallel summary statistics with `furrr`. |
| **Midterm** | Midterm Online Practicum | Practicum Notebooks | `penguins.rds`<br>`diamonds.rds`<br>`sleep.rds`<br>`sms-spam.rds` | Hands-on practicum challenge covering Modules 1–6: penguin EDA, diamond filtering & linear modeling, financial stock retrieval (`tidyquant`), sleep missingness imputation (`visdat`/`naniar`), and SMS spam text tokenization (`tidytext`). |
| **Final** | Final Online Practicum | Practicum Notebooks | `Taxi-Data.zip`<br>`data-to-validate.rds`<br>`taxi_zones.zip` | Hands-on practicum challenge covering Modules 7–12: lazy querying on NYC Taxi Parquet data (`arrow`), data validation rule checking (`validate`), weekday vs. weekend trip/tip analysis, and Manhattan taxi zone spatial choropleth mapping (`sf`). |

---

## Detailed Module Breakdown

### Module 00: Intro

* **Notebook:** Introductory Notebook
* **Details:** Students complete a "Hello World" notebook.



---

### Module 01: R Basics and Intro to Tidyverse

1. **Programming Notebook:**
* **Dataset:** `spiderman.txt`
* **Description:** Small key/value text file to illustrate reading in a text file. Used in Dr. Joe's lab.


2. **Data Wrangling Notebook:**
* **Dataset:** `collegefootballbowl.csv`
* **Description:** Contains historical records of college football bowl games. Used in Dr. Joe's lab.


3. **Assignment:**
* **Dataset:** `gapminder-life-expectancy.csv`
* **Description:** Restructured dataset from gapminder.org for easier analysis. Variables: `country`, `year`, and `life expectancy`.

---

### Module 02: Common Data Structures and Tidying Data
1. **Programming Notebook:**
* **`Bike-Data/`**: A folder containing 63 CSV files where each file has the variables `date` and `bike_count`. Gives the daily bike count from 12 bike counters in Seattle (sourced from TidyTuesday GitHub).
* **`avg-tuition-multisheet.xlsx`**: Average college tuition cost per state across several school years. Each worksheet represents a different school year (sourced from TidyTuesday GitHub).
* **`got_chars.json` & `got_chars.xml**`: Character attributes from Game of Thrones, sourced from the `repurrrsive` R package.


2. **Data Wrangling Notebook (FRED Housing & Economic Data):**
* **`FPCPITOTLZGUSA.csv`**: Inflation as measured by Consumer Price Index (CPI) (FRED series `FPCPITOTLZGUSA`).
* **`MEPAINUSA672N.csv`**: Real median personal income in the US in 2023 USD (FRED series `MEPAINUSA672N`).
* **`MORTGAGE30US.csv`**: 30-year fixed rate mortgage average in the US (FRED series `MORTGAGE30US`).
* **`MSPUS.csv`**: Nominal median sales price of houses sold in the US (FRED series `MSPUS`).


3. **Assignment:**
* **`plant-cooking/`**, **`plant-refrigeration/`**, **`plant-ventilation/`**: Real-world dataset capturing machine downtime at three manufacturing plants. Separated into three folders with daily CSV files. Provided by CAVS-e industry partner.

---

### Module 03: Acquiring and Wrangling Data from R Packages
1. **Programming Notebook:**
* **Stock Data:** Uses `tidyquant` package (wrapping Yahoo Finance API) to fetch stock prices for AAPL and MSFT (2000–present) and generate visualizations.
* **Economic Data:** Uses `tidyquant` to pull four FRED economic series (same series as Module 02).
* **Weather Data:** Sourced via `httr2` from `weather.gov` for specific latitude/longitude coordinates (default: Vicksburg, MS). Tidies JSON payload and generates visualizations.


2. **Data Wrangling Notebook:**
* **Vehicle Recall Data:** Pulled from NHTSA API for various automotive makes and models.
* **Vehicle MSRP Data:** Sourced via CarAPI (`[https://carapi.app/](https://carapi.app/)`). Combined with recall data to generate visualizations comparing MSRP vs. recall counts.


3. **Assignment:**
* **`sp500-ranked-2000-2022-se.rds`**: Dataframe ranking return performance for S&P 500 companies (2000–2022).
* **Stock Data:** Students pull raw 2023–2024 stock data for S&P 500 companies using `tidyquant`, structure it matching the historical dataset, summarize, and visualize.

---

### Module 04: Exploring, Discovering, and Handling Missing Values in Tabular Data
1. **Programming Notebook:**
* **Synthetic Data:** Simple synthetic data generated directly in the notebook to demonstrate missing value concepts.
* **`airquality`**: Built-in dataset of daily NYC air quality measurements from May to September 1973 (156 observations, 6 variables: `Ozone`, `Solar.R`, `Wind`, `Temp`, `Month`, `Day`). ~24% missing values in `Ozone`.


2. **Data Wrangling Notebook:**
* **`txhousing`**: Built-in dataset from `ggplot2` tracking Texas housing market variables over time. Used to inspect missing values and perform imputation on `sales` (monthly house sales).


3. **Assignment:**
* **`weather-data.rds`**: Subset of `weatherAUS` dataset from the `rattle` package (~15K daily weather observations across Australia). Students identify missing values and perform imputation on the variable with the highest proportion of missing data.

---

### Module 05: Preparing Data for Statistical Analysis and Machine Learning

1. **Programming Notebook:**
* **Synthetic Data:** Simple synthetic datasets (`toy_data_fs`, `toy_data_fsc`, `toy_data`) generated directly in the notebook.
* **Description:** Concepts of feature engineering, scaling (Min-Max, Standard), categorical one-hot encoding, outlier detection (z-score, IQR, Hampel filter), feature selection methods (filter methods via correlation & Chi-squared, wrapper methods via `caret::rfe`, embedded methods via `glmnet` LASSO), and data splitting strategies (simple random, stratified sampling via `rsample::initial_split`, and cross-validation via `rsample::vfold_cv`).


2. **Data Wrangling Notebook:**
* **`Bike-Data/`**: Seattle daily bike count dataset joined with weather metrics and federal holiday indicators.
* **Description:** End-to-end dataset preparation and predictive modeling workflow. Cleans missing values, applies Hampel filter for weather outliers, transforms continuous predictors, filters correlated variables, and trains/evaluates a linear regression model using 10-fold cross-validation (`rsample`) reporting Normalized RMSE (NRMSE). Imputes missing values across the full dataset.


3. **Assignment:**
* **`car-data.rds`**: Augmented Kaggle car dataset containing missing values and outliers.
* **Description:** Predictive modeling of car prices (`Price`). Students clean missing records, detect and visualize egregious outliers, explore feature transformations, select predictors, perform 10-fold cross-validation, and report/visualize training vs. testing NRMSE and actual vs. predicted values.

---

### Module 06: Working with Text Data

1. **Programming Notebook:**
* **`austen-books.rds` & `stop_words`**: Text from Jane Austen novels alongside built-in `tidytext` stop words.
* **Description:** Text data representation in R using character vectors, string manipulation with `stringr` (concatenation, subsetting, case conversion, whitespace handling, pattern matching, regex), and tidy text principles with `tidytext` (`unnest_tokens()` for words, sentences, characters, n-grams, stop word filtering, and word frequency counting).


2. **Data Wrangling Notebook:**
* **`imdb-dataset.rds`**: 50,000 IMDB movie reviews labeled with binary sentiment (`positive`/`negative`).
* **Description:** Applied Natural Language Processing (NLP) workflow on IMDB reviews. Tokenizes review text, cleans HTML tags, calculates document sentiment scores using the Bing lexicon, generates sentiment word clouds (`wordcloud`, `comparison.cloud`), and tunes a LASSO logistic regression text classification workflow (`textrecipes`, `tidymodels`) achieving ~84% accuracy.


3. **Extra Notebook:**
* **`dataset_mnist()`**: Built-in MNIST handwritten digit dataset from `keras3`.
* **Description:** Optional tutorial on installing `keras3` with a TensorFlow backend and training a multi-layer dense neural network on MNIST digit images.


4. **Assignment:**
* **`enron-subset-se.rds` / `emails.csv`**: Subset of the Enron email dataset.
* **Description:** Students parse email headers to extract `date` and `message_text` body, convert dates to `Date` objects, tokenize message text by word using `tidytext`, score word sentiment via the Bing lexicon, calculate daily average sentiment scores, and plot sentiment time series over time.

---

### Module 07: Working with Excel Data in R

1. **Programming Notebook:**
* **`avg-tuition-multisheet2.xlsx`**: Workbook containing college tuition averages across multiple school year worksheets.
* **Description:** Foundations of reading Excel files with `readxl` (`read_excel()`, `excel_sheets()`, specifying sheets, cell ranges, column headers, handling missing values, `col_types`) and exporting single/multi-sheet Excel files with `writexl` (`write_xlsx()`).


2. **Data Wrangling Notebook:**
* **`cheese_per_cap.xlsx`**: USDA per capita cheese consumption dataset with separate worksheets for 1970–1994 and 1995–2017.
* **Description:** Wrangling multi-sheet Excel workbooks with varying column structures. Cleans and merges historical cheese consumption data, fits linear trend models, and creates interactive stacked area plots (`plotly`) analyzing Cheddar vs. Mozzarella popularity over time.


3. **Assignment:**
* **`sales-data.zip`**: Compressed archive containing 50 individual salesperson Excel files (e.g., `first_last.xlsx`), each featuring multiple customer ID sheets.
* **Description:** High-volume batch Excel processing. Students programmatically iterate over 50 workbooks and multiple sheets, calculate net pricing and profit margins, and answer key business questions regarding top salespeople, top customers, and most profitable products.

---

### Module 08: Visual Data Exploration with R

1. **Programming Notebook:**
* **`economics`, `presidential`, `mtcars`, `gapminder`, Synthetic Surface Data**: Built-in R and package datasets alongside synthetic 3D grid data.
* **Description:** In-depth coverage of the Grammar of Graphics in `ggplot2` (data, mapping, layers, scales, facets, coordinates, themes) applied to macroeconomic timelines, interactive web graphics with `plotly` (scatter plots, 3D scatter/surface plots, animated Gapminder charts), and saving figures via `ggsave()`.


2. **Data Wrangling Notebook:**
* **`assets.csv`, `debts.csv`, `surface-temperature.rds`, `train-test.rds`**: Financial balance sheets, 3D print thermal spatial coordinates, and 3D print mechanical stress/strain test data.
* **Description:** Advanced statistical and engineering visualizations: building interactive balance sheet Treemaps (`plotly`), mapping 3D thermal camera temperature measurements onto spatial surface grids (`surface-temperature.rds`), and fitting quadratic regression models with shaded 95% confidence and prediction intervals (`train-test.rds`).


3. **Assignment:**
* **`iris`, `mtcars`, `got_chars.json`**: Built-in R datasets and Game of Thrones character JSON metadata.
* **Description:** Plot recreation challenge. Students construct (1) a parallel coordinates plot on `iris` using base `ggplot2`, (2) a lower-triangular correlogram heatmap on `mtcars` using base `ggplot2`, and (3) an interactive network graph (`visNetwork` or `plotly`) mapping GOT character appearances across books from `got_chars.json`.

---

### Module 09: Assessing and Ensuring Data Quality

1. **Programming Notebook:**
* **`airquality` & Synthetic Data**: Built-in NYC air quality data and synthetic tabular datasets with intentional defects.
* **Description:** Data quality assessment dimensions (completeness, accuracy, validity, consistency, duplicates, outliers). Demonstrates missingness visualization (`visdat::vis_miss`), implicit missing date completion (`complete()`), regex pattern conformance, cross-field validation, and programmatic rule-based validation using `validate` (`validator()`, `confront()`, `summary()`, `aggregate()`).


2. **Data Wrangling Notebook:**
* **`widget-orders-synthetic.rds`**: Synthetic e-commerce order dataset from "Widget Wonders".
* **Description:** Applied end-to-end data quality audit and remediation workflow. Assesses completeness and validity on order records, defines 10 validation rules in `validate`, executes data cleaning (state imputation, price/quantity correction, deduplication, outlier capping), and performs post-cleaning verification.


3. **Assignment:**
* **`student-enrollment-data-full.rds`**: Synthetic university database containing `enrollment` records, `student_directory`, and `course_catalog`.
* **Description:** Institutional research data quality audit. Students use `validate` and `tidyverse` to enforce Subject Matter Expert (SME) business rules across student IDs, course catalog joins, semester enrollment date bounds, credit bounds (1–6), grade validity, and record uniqueness, then clean or flag non-compliant entries.

---

### Module 10: Wrangling, Exploring, and Analyzing Geographical Data in R

1. **Programming Notebook:**
* **`nc.shp` & Synthetic Rasters**: Built-in North Carolina county shapefile (`sf` package) and synthetic raster grids (`terra` package).
* **Description:** Fundamentals of GIS spatial data in R. Covers vector data with `sf` (reading shapefiles via `st_read()`, CRS inspect/transform, attribute joins, spatial joins via `st_join()`, buffering, centroids, unions) and raster data with `terra` (`crop()`, `mask()`, `resample()`, `extract()`), alongside static (`geom_sf()`) and interactive (`plotly`) spatial mapping.


2. **Data Wrangling Notebook:**
* **`census-map-data.rds`**: Mississippi county ACS demographic census shapefiles spanning multiple survey periods (2009–2023).
* **Description:** Spatial-temporal demographic analysis of Mississippi counties. Merges census survey metrics (population density, education levels, median household income) with county boundary polygons using `sf`, computes relative temporal changes, constructs choropleth maps (`geom_sf` + `plotly`), and fits spatial linear regression models.


3. **Assignment:**
* **`census-map-data.rds` & `ms-hospitals.rds`**: Mississippi county boundary shapefiles and Geospatial Management Office hospital location dataset.
* **Description:** Healthcare accessibility and coverage audit. Students plot hospital points over county polygons, execute spatial joins (`st_join()`, `st_within()`) to compute hospital beds per 1,000 residents by county, construct 10-mile spatial buffers around hospitals (`st_buffer()`, `st_union()`), map healthcare coverage, and evaluate medical deserts.

---

### Module 11: Scraping Data from the Web Ethically and Safely with R

1. **Programming Notebook:**
* **Web HTML, `robots.txt`, JSONPlaceholder API**: CRAN package web pages, website robots files, and mock REST API endpoints.
* **Description:** Principles of ethical web scraping (user-agents, rate limiting, `robots.txt`, preferring APIs). HTML parsing with `rvest` (`read_html()`, `html_elements()`, `html_text2()`, CSS selectors), REST API querying with `httr2` (`request()`, `req_url_query()`, `resp_body_json()`, API keys), and an introduction to headless browser automation (`RSelenium`).


2. **Data Wrangling Notebook:**
* **Wikipedia API & BLS API**: MediaWiki Action API for Wikipedia console pages and Bureau of Labor Statistics CPI API.
* **Description:** Real-world API web scraping and data pipeline. Interacts with the MediaWiki API to fetch rendered HTML for best-selling game console tables, parses and cleans text/tables with `rvest` and regex, queries the Bureau of Labor Statistics CPI API via `httr2` for annual inflation data, computes inflation-adjusted launch prices, and builds interactive `plotly` market trend charts.


3. **Assignment:**
* **`video-game-console-data.csv`**: Console sales dataset pre-populated with Wikipedia page links (`wiki_page`).
* **Description:** Ethical web scraping and hardware performance analysis. Students programmatically query the MediaWiki API across dozens of console pages, extract memory/RAM specs from infoboxes using `rvest`, standardize memory units (KB/MB/GB), compute inflation-adjusted launch cost per MB of RAM, and visualize historical cost-efficiency trends.

---

### Module 12: Using R to Process Big Data

1. **Programming Notebook:**
* **Synthetic Benchmark Data**: In-notebook generated large data structures, SQLite database files.
* **Description:** Strategies for handling big data in R: fast I/O (`data.table::fread`, `vroom`), copy-on-modify memory management (`lobstr`, `data.table`), SQLite database queries via `DBI` and `dbplyr` lazy evaluation, and multi-core parallel processing using `parallel`, `future`, and `furrr`.


2. **Data Wrangling Notebook:**
* **`Taxi-Data.zip` (`yellow_tripdata_2024-*.parquet`)**: 12 monthly Parquet files of NYC Yellow Cab trips from 2024 (~multi-gigabyte dataset).
* **Description:** Large-scale columnar dataset processing. Uses `arrow::open_dataset()` for out-of-memory lazy evaluation on Parquet files, performs feature engineering (trip duration, speed, tip percentage, time-of-day classification), filters outliers, and computes monthly summary statistics in parallel across CPU cores using `furrr::future_map()`.

---

### Midterm Online Practicum (Modules 1–6)

* **Notebooks:** `midterm-se.ipynb` / `midterm-te.ipynb`
* **Datasets:** `penguins.rds` (palmerpenguins), `diamonds.rds` (ggplot2), `sleep.rds` (VIM), `sms-spam.rds` (Kaggle).
* **Details:** Comprehensive hands-on practicum assessing skills from Modules 1–6:
  1. **Penguins EDA**: Inspecting structure, filtering species (`Gentoo`) and flipper length.
  2. **Diamonds Wrangling & Modeling**: Ideal cut filtering, volume calculation, carat binning, conceptual joins, linear regression price modeling, and interactive charts (`plotly`).
  3. **Financial Data Acquisition**: Fetching stock time series via `tidyquant`.
  4. **Sleep Data Imputation**: Visualizing missingness (`visdat`/`naniar`) and imputing missing non-dreaming sleep values (`NonD`).
  5. **Text Tokenization**: Tokenizing SMS spam message text and visualizing word frequencies (`tidytext`).

---

### Final Online Practicum (Modules 7–12)

* **Notebooks:** `final-se.ipynb` / `final-te.ipynb`
* **Datasets:** `Taxi-Data.zip` (2024 NYC Yellow Cab Parquet dataset), `data-to-validate.rds`, `taxi_zones.zip` (NYC taxi zone shapefile).
* **Details:** Comprehensive hands-on practicum assessing skills from Modules 7–12:
  1. **Big Data Aggregation with `arrow`**: Querying May–August 2024 NYC taxi trips, classifying pickup time of day and weekend status, and aggregating trip metrics into memory.
  2. **Data Quality Rule Validation with `validate`**: Writing validation rules for dropoff datetimes, passenger counts, and fare/tip non-negativity against `data-to-validate.rds`.
  3. **Visual & Statistical Analysis**: Comparing weekday vs. weekend pickup volume, trip duration (weighted averages), and tipping behavior across time classifications.
  4. **GIS Spatial Mapping with `sf`**: Unzipping and loading NYC taxi zone shapefiles, joining aggregated tip metrics by `LocationID`, creating faceted choropleth maps, identifying top tipping zones, and analyzing weekday vs. weekend tip differences specifically within Manhattan borough.