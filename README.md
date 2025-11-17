# Camping Project — Data Science Analysis of

# European Campsites

This repository contains the full workflow of a data science project that scrapes, analyses, and models
campsite information from camping.info. It was created as a final project for a data‑science course and
demonstrates how to collect data from the web, clean and explore it, and build predictive models using
Python.

## Overview

The project aims to understand factors that influence campsite characteristics (such as price and rating) and
to build simple models that can estimate these values. To do this, we scraped thousands of campground
listings across Europe from camping.info and assembled a dataset with the following fields:

```
country – the country where the campground is located
price – average nightly price in euros (may be missing)
rating – average user rating (stars)
size_of_site – total area of the campground in hectares
total_pitches – number of pitches (camping spots)
caravans – indicator of caravan accommodation
sea , lake, river – indicators of nearby water bodies
mountain – indicator of mountainous terrain
Height – altitude above sea level (metres)
next_city – distance to the nearest city (km or descriptive text)
transport – public transport availability or travel time
```
Missing values are common because information on camping.info is inconsistent. The notebook includes
cleaning steps such as dropping columns with too many missing values and imputing numeric data.

## Repository structure

```
Camping.Info - Project/
├── NOTEBOOKS/
│ └── Final project - Camping.Info.ipynb # main Jupyter notebook with
scraping, EDA and modelling
├── data1.csv, data2.csv, ... # CSV files containing the scraped
data
├── lst_links1.csv, lst_links2.csv, lst_links3.csv # search page URL lists used
for scraping
├── <hebrew_name>.py # Python script with scraping helper
functions
```
### • • • • • • • • • • •


```
├── chromedriver.exe # ChromeDriver binary used by
Selenium
├── LICENSE.chromedriver # licences for ChromeDriver and
third‑party components
└── README.md # project description (this file)
```
## Getting started

```
Clone the repository
```
```
gitclone https://github.com/yourusername/Camping-Project.git
cd Camping-Project/Camping.Info\ -\ Project
```
```
Install Python dependencies
```
The project uses Python 3.8+. Install required packages with pip:

```
pipinstall -r requirements.txt
```
If there is no requirements.txt, install the main packages manually:

```
pipinstall pandasnumpy beautifulsoup4seleniumrequests scikit-learn
matplotlibseaborn
```
```
Set up ChromeDriver
```
The scraper uses Selenium with ChromeDriver. If you are on Windows, chromedriver.exe is included.
On Linux/Mac, download the appropriate version from https://chromedriver.chromium.org/downloads and
place it in the project directory or ensure it is in your system PATH.

```
Run the notebook
```
Open the notebook with Jupyter:

```
jupyternotebook "NOTEBOOKS/Final project - Camping.Info.ipynb"
```
The notebook is divided into sections:

```
Scraping links – uses lists of search‑result URLs to collect individual campsite links.
Scraping campground data – visits each campsite and extracts the features listed above.
Data cleaning – handles missing values, converts strings to numeric types and encodes categorical
variables.
```
### 1.

### 1.

### 1.

### 1.

### 1.

### 2.

### 3.


```
Exploratory analysis – visualises distributions, correlations and geographic trends using matplotlib
and seaborn.
```
```
Modelling – builds regression models (decision tree and linear regression) to predict price and a
Gaussian Naive Bayes classifier for rating categories.
```
```
Explore the dataset
```
The scraped data are stored in data1.csv, data2.csv, ... You can load them in Python using
pandas.read_csv() for further analysis or to extend the model.

## Results and discussion

The exploratory analysis reveals that campsite ratings cluster between ~3.5 and 4.5 stars and that prices
vary widely across countries. There is a weak positive correlation between price and site size or amenities.
The regression models capture some patterns but are limited by missing data and heterogeneity; the
decision‑tree model outperforms linear regression but still has moderate accuracy. The classification model
categorises campsites into rating tiers with modest success. Improving the models would require more
complete data or additional features, such as textual reviews.

## Contributing

Contributions are welcome! Feel free to open issues or pull requests if you spot bugs, have suggestions or
want to add new analyses.

## License

The repository contains **chromedriver.exe** and a combined licence file (LICENSE.chromedriver) which
covers ChromeDriver and various third‑party components. Please review that file for details on usage rights.
The rest of the project’s code is provided for educational purposes; you may modify and reuse it at your
discretion.

### 4.

### 5.

### 6.
