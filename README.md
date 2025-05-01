# Crowdfunding to Support Education Needs: Predicting Unfunded Education Projects on DonorsChoose
### DonorsChoose ML Project List of Files and Instructions for Running Notebooks and Downloading .csv Datasets
### By Arthur Spirou, Akin Joseph, & Nikki Chen
This repo contains Notebooks associated with predicting projects that are unlikely to be funded in order to prioritize expert resources for DonorsChoose.
Note: The main source data utilized for this project was provided by Kaggle https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data

In order to run the notebooks provided in this repo, one must have downloaded the following .csv data files and saved them in the same directory where you are executing the notebooks:
  - TIDY_unclean_1.csv (a merged and partially cleaned dataframe consisting of the various relational datasets proivided by Kaggle)
      - https://drive.google.com/file/d/1WihsvXdqblYZmjeb7BU2wGsyFOU172tP/view?usp=sharing
  - SASUMMARY__ALL_AREAS_1998_2024.csv (a file containing annual state GDP data to be used as prior's year's GDP for a predictive feature)
      - https://drive.google.com/file/d/10SzlX0w5IQ9zj_Nx9jSx8OWj1vkOKT6I/view?usp=sharing

It contains an EDA Notebook, a Simple Seed Baseline Model Notebook, a Classification Task Model Notebook, and a Regression Task Model Notebook\
  - DonorsChoose_EDA.ipynb ---> Explores the merged data in TIDY_unclean_1.csv, and provides an in-depth detailed review of feature-selection
  - InitialFeatureEngineering.ipynb ---> Takes bare minimum information from TIDY_unclean_1.csv and creates a seed baseline model, predicting using a basic decision tree on only the row ID's and labels
  - ClassificationModels_DonorsChoose.ipynb ---> using TIDY_unclean_1.csv and SASUMMARY__ALL_AREAS_1998_2024.csv - creates, trains, tests, cross-validates, tunes hyperparameters, and assesses metrics 
    for classification task models
  - RegressionModels_DonorsChoose.ipynb ---> Using TIDY_unclean_1 and SASUMMARY__ALL_AREAS_1998_2024.csv - creates, trains, tests, cross-validates, tunes hyperparameters, and assesses metrics for 
    regression task models
   
Note: TIDY_unclean1.csv allows the notebooks to be run from a semi-clean merged dataframe state, where additional features can easily be cleaned and added to the pipeline
  - In order to reproduce this from the original Kaggle datasets, the data needs to be merged on 'projectid'. We have already done that and exported to a .csv for further use in early-stage scratch   
    work for this project.
  - At that same time, we also used the yahoo finance library to calculate past 30-day moving averages and standard deviations for the S&P 500 for every calendar date, and included those as selectable 
    features
