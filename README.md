# Dataccion-2026-analisis-de-la-violencia-de-genero-en-Veracruz-Mexico
This repository contains the code and methodology for analyzing gender-based violence in the state of Veracruz, Mexico, covering the period from 2018 to 2023. The project focuses on extracting, cleaning, and modeling open data to feed an interactive Looker Studio dashboard. 

For a comprehensive overview of the project's justification, methodology, and conclusions, please refer to the official report: `Datacción 2026_Dashboard_Identificando riesgos_ análisis de la violencia de género en Veracruz, México.pdf`.

## 👥 Team
* Eduardo Ulises López Matheis
* Victor Alfonso Contreras Apango
* Mariana Patiño de la Cruz
* Cyntia Montserrat Cruz Pérez

## 📊 Project Overview
Gender-based violence is a complex social issue. While open data exists through the National Data and Information Bank on Cases of Violence against Women (BANAVIM), it often contains inconsistencies and structural challenges that make direct analysis difficult. This project provides a practical solution by transforming raw data into an accessible, interactive dashboard to help identify geographical hotspots, violence trends, and victim/aggressor profiles.

## 🛠️ Tech Stack & Tools
* **Python 3.10**: Core language used for data extraction and intermediate-level processing.
* **Pandas**: Used for data manipulation, cleaning, and dataframe optimization.
* **Scikit-Learn**: Implemented for Machine Learning algorithms.
* **Google Looker Studio**: Used for designing the interactive reporting dashboard.
* **Google Gemini**: Utilized as a technical assistant for code optimization, debugging, and documentation.

## ⚙️ Methodology

### 1. Data Extraction
Data was extracted directly from the official BANAVIM API using Python's `requests` library. Custom functions were built to iterate API requests and bypass the standard 1,000-record manual download limit, compiling a comprehensive dataset of over 11,000 case records.

### 2. Data Cleaning & Preparation
To ensure unbiased analysis, the data underwent a strict cleaning process:
* **Geographic Normalization**: Filtering and standardizing municipality names by removing accents and fixing text formatting to match official records.
* **Text Formatting**: Standardizing text cases across categorical variables, such as weapons used, substance consumption, and the victim's relationship to the aggressor.
* **Handling Nulls**: Applying logical filtering and label normalization instead of massive deletion to preserve useful information.

### 3. Machine Learning Modeling
Two models were implemented to provide deeper strategic insights:
* **Random Forest Classifier**: Trained to predict and classify the type of violence based on contextual factors, such as the location of the event, relationship to the aggressor, and substance use.
* **K-Means Clustering**: Used to segment victim and aggressor archetypes based on their vulnerability levels.

### 4. Interactive Dashboard
The processed data was exported to Google Looker Studio. The dashboard features 6 sections equipped with geographic heatmaps and KPI cards, translating complex computational results into actionable intelligence for non-technical users and decision-makers.

## 🔗 Links
* **Interactive Dashboard**: [View on Looker Studio](https://lookerstudio.google.com/reporting/6c25ec45-7873-4123-b6b8-3ae871b04f18)