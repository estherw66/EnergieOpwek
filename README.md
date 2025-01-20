# Energie Opwek
This repository contains all the notebooks for the Data Driven Innovation Challenge. For this challenge we decided to predict renewable energy production in the Netherlands. This data challenge is made by Marjolein van der Eerden and Esther Wolfs.

---

## Table of contents
[Idea](#idea)
[Approach](#approach)
[Results](#results)
[Folder Structure](#folder-structure)

---
## Idea
The original idea was to create a predictive tool for forecasting energy congestion in power grids or other energy networks. For would involve analysing real-time and historical energy data, to detect bottlenecks in the energy flow and provide actionable insights for grid operators to prevent or mitigate congestion issues. However, due to the necessary energy consumption data not being publicly available, this idea is not feasible. Instead, the focus shifted to predicting renewable energy production, specifically solar and wind energy. 

---
## Approach
To predict renewable energy we took the following steps:

#### 1. Data Requirements

**Essential Data**:
- **Energy production** data for the Netherlands, preferably hourly but at least daily
- **Energy consumption** data for the Netherlands, preferably hourly but at least daily
- **Weather data** for the Netherlands, preferably hourly but at least daily

**Nice-to-Have Data**:
- Number of solar panels in the Netherlands
- Total number of windmills in the Netherlands
- Total number of electric vehicles in the Netherlands

These datasets could help improve predictions, since all of these influence the total energy production and consumption. 

#### 2. Data Collection
The main dataset we used is the energy production dataset from <https://ned.nl>. This contains the total energy production per hour in the Netherlands for multiple different energy sources. Unfortunately, they only have energy production data and the energy consumption data is not yet available on their data portal. We tried looking for other sources of energy consumption data for the Netherlands, but we only found a cbs dataset that contained monthly (calculated) energy consumption data. For this reason we mainly focused on the energy production data. 

For the nice-to-have data we found some datasets that contained the total number of solar panels and windmills in the Netherlands at the end of each year, we used these datasets for some analysis. We did not find a useful source for the total amount of electric vehicles, but also decided to not include this anyway, since we also don't have the right energy consumption data.

#### 4. Data Preparation
We started with combining these datasets and then cleaning them, so they could be used for data analysis. This also includes handling the missing values.

#### 5. Modelling
After doing the analysis we started on modelling. We decided to focus on two different energy sources, solar energy production and wind energy production. After doing some research we found a few models we could try. These models include:

- **Solar Energy Production**:
    - LSTM
    - BiLSTM
    - CNN
    - SARIMA (statistical model)

- **Wind Energy Production**:
    - LSTM
    - RNN
    - GRU

All of these models are also evaluated and compared, to find the best performing model.

---

## Results
Outcomes with metrics, visualisations

---

## Folder Structure
The project is divided into the following folders. The data used in the project can be found in the data folder, this contains both the raw and cleaned data. The data_prep folder contains all the notebooks we created for cleaning the data, the eda folder contains all the notebooks where we did the EDA and finally the models folder contains the notebooks used for creating and evaluating the models.
```
.
└── root/
    ├── data/
    │   ├── ConsumptionData # energy consumption data
    │   ├── Model # data used for modelling
    │   ├── Other # other data
    │   ├── ProductionData # energy production data
    │   └── Weather # weather data
    ├── data_prep/
    │   ├── ConsumptionDataCleaning.ipynb # Esther
    │   ├── JoiningProductionData.ipynb # Marjolein
    │   ├── ProductionDataCleaning.ipynb # Marjolein
    │   ├── SolarPanels.ipynb # Esther
    │   ├── WeatherDataCleaning.ipynb # Marjolein
    │   └── WindmillsDataCleaning.ipynb # Marjolein
    ├── eda/
    │   ├── ConsumptionData.ipynb # Esther
    │   ├── ProductionEDA.ipynb # Marjolein
    │   ├── SolarProduction.ipynb # Esther
    │   └── WindvsWindmillsEDA.ipynb # Marjolein
    ├── models/
    │   └── SolarEnergyPrediction.ipynb # Esther
    │   └── WindEnergyPrediction.ipynb # Marjolein
    └── README.md
```

## References