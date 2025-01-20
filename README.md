# EnergieOpwek
Datachallenge made by Marjolein van der Eerden and Esther Wolfs.

---

## Table of contents
[Idea](#idea)
[Approach](#approach)
[Results](#results)
[Folder Structure](#folder-structure)

---
## Idea
Motivation, problem statement, goal of the project

---
## Approach
Methodology used to solve the problem. Key steps, tools, frameworks

---

## Results
Outcomes with metrics, visualisations

---

## Folder Structure
The project is divided into the following folders. The data used in the project can be found in the data folder, this contains both the raw and cleaned data. The dataprep 
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
    └── README.md
```