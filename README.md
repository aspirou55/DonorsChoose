# Crowdfunding to Support Education Needs: Predicting Unfunded Education Projects on DonorsChoose
### DonorsChoose ML Project List of Files and Instructions for Running Notebooks and Downloading .csv Datasets
### By Arthur Spirou (aspirou), Akin Joseph (ababujos), & Nikki Chen (yiqichen)
This repo contains Notebooks associated with predicting projects that are unlikely to be funded in order to prioritize expert resources for DonorsChoose.
Note: The main source data utilized for this project was provided by Kaggle https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data

In order to run the notebooks provided in this repo, one must have downloaded the following .csv data files and saved them in the same directory where you are executing the notebooks:
  - TIDY.csv (a merged and partially cleaned dataframe consisting of the various relational datasets proivided by Kaggle)
      - https://drive.google.com/file/d/1WihsvXdqblYZmjeb7BU2wGsyFOU172tP/view?usp=sharing
  - Likewise, flagged_projects_top10_xgboost.csv can also be found here:
      - https://drive.google.com/file/d/1tMbXAbRrRegQ4DvEjCXhlnIep_moVXV2/view?usp=sharing

It contains an EDA Notebook, a Bias Audit Notebook, a Classification Task Model Notebook, and a Regression Task Model Notebook\
  - DonorsChoose_EDA_Final.ipynb ---> Explores the merged data in TIDY.csv, and provides an in-depth detailed review of feature-selection
  - BiasReport.ipynb ---> Takes the project information from the test set for projects flagged at top 10% precision for further bias review
  - ClassificationModels_DonorsChoose.ipynb ---> using TIDY.csv, creates, trains, tests, cross-validates, tunes hyperparameters, and assesses metrics 
    for classification task models
  - RatioModels_DonorsChoose.ipynb ---> Using TIDY.csv creates, trains, tests, cross-validates, tunes hyperparameters, and assesses metrics for 
    regression task models (alternative approach to solving the task by making % funded the label)
   
Note: TIDY.csv allows the notebooks to be run from a semi-clean merged dataframe state, where additional features can easily be cleaned and added to the pipeline
  - In order to reproduce this from the original Kaggle datasets, the data needs to be merged on 'projectid'. We have already done that and exported      to a .csv for further use during the early-stage scratch work for this project.
  - At that same time, we also used the yahoo finance library to calculate past 30-day moving averages and standard deviations for the S&P 500 for          every calendar date, and included those as selectable features though they did not prove to be particularly meaningful in the end.
    
**** SEE THE INCLUDED Github_Repo_Instructions.pdf FILE FOR FURTHER INFORMATION ON RUNNING THE NOTEBOOKS AND INSTALLING REQUIRED PACKAGES ****
