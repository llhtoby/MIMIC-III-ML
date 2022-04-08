# Imputation strategies for risk prediction models based on Electronic Health Records

# About

This repo contains code used in the L4 Honours Project. It has been divided into the following folders:
* data: contain all resouces files, ethics form, and raw data. Since the raw data files in this project is too large, these file is not uploaded to github. However, these files can be recreated by running the notebooks in this project.
* Dissertation: contains the latex and figures used for dissertation
* Meetings: Contains all powerpoint files that is used for weekly meeting with the project supervisor.
* Presentation: Contains final presentation resources
* src: The source folder contains all the source code for this project, which are all python notebooks file in .ipynb format. 
* status_report: Contains the mid-term status report

# Installation
This project used standard python libraries like pandas, numpy, sklearn, matplotlib, seaborn, tensorflow etc. If these you see libaries not installed when trying to run the code, simply do pip install for the missing libary. Other than standard libaries, this project also used some libaries like mice_forest and MIDASpy for some imputation strategies. However, all these libaries can also be installed simply by using pip install in your python environment.

# Abstract
he digitisation of health records in recent years created large amount of healthcare data that are now publicly available for researchers. Along side recent advancements in machine learning and artificial intelligence, accurate and robust clinical decision support systems using machine learning is made possible. However, Electronic Health Records (EHR) are complex and irregularly sampled, which introduces the problem of missing data. Previous researches often exclude patients with missing data in their dataset, which makes the population sample not representative and could introduce biases.
    
Uni-variate imputation strategies like mean imputation is often used to solve this problem, but was proven to be ineffective and introduces bias to the clinical decision machine learning models in this research. 
    
To conduct in-depth analysis on imputation strategies with electronic health records, the publicly available clinical database MIMIC-III is used. This dissertation includes detailed extraction pipeline to extract events and patient data, along side pre-processing steps so that it is ready for imputation and machine learning. Mean, most-frequent and knn imputation are common approaches for it's effectiveness and ease of implementation. This research dives deeper to apply advanced multiple imputation techniques featuring chained equations and denoising auto-encoders.After implementation, the imputed datasets are evaluated using leave one out cross validation (LOOCV) simulation and statistical performances of risk prediction model created to predict in-hospital mortality.
    
 It was found that Multiple imputation by chained equations (MICE) is the all-rounded winner by small margins over other imputation strategies both in terms of it's ability to impute data similar of the original, and evaluation metrics performances for the in-hospital mortality classifier. 
