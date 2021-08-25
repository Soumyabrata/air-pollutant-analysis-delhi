# air-pollutant-analysis-delhi

# Analyzing Air Pollutant Concentrations in New Delhi, India

With the spirit of reproducible research, this repository contains all the codes required to produce the results in the manuscript:

> Alparslan, B., Jain, M., Wu, J. and Dev, S.(2021). "Analyzing Air Pollutant Concentrations in New Delhi, India." Progress in Electromagnetic Research Symposium, Hangzhou, China. 2021.

### Executive summary
Elevated air pollutants concentrations have shown to have a significant impact on human health, ecosystem as well as radio communications and increased fog levels or decreased visibility. In this work, we provide a scrapped, analyzed and pre-processed dataset from  National Air Quality Index of India (NAQII) website. The datset is scrapped for 2 stations (i.e. Anand Vihar and Punjabi Bagh) for 2017 and 2018.

### Data
Source of the data used in this work is Central Control Room for Air Quality Management - Delhi NCR ([See here](https://app.cpcbccr.com/ccr/#/caaqm-dashboard/caaqm-landing/caaqm-comparison-data)). You can reach the samples used in this work from [here](https://drive.google.com/drive/folders/1sIITvGDrgwuL7oD5GS2AbD_0d4TyzOYL?usp=sharing).

### Code
All codes are written in `python3`.
+ `automate.py`: This file is used to download the required data files from above-mentioned link automatically. One can download the csv files directly from the second link in the data section or run this python file (downloaded excel files should be saved as csv files).
+ `defns.py`: Definitions of some functions used in `automate.py`.
+ `stropns.py`: Some string operations.
+ `ljungbox.py`: Implementation of Ljung-Box test. Work is done by [Bhavesh Bhatt](github.com/bhattbhavesh91/time_series_notebooks)
+ `rand_5_data.txt`: 5 randomly selected samples used in this work.
+ `make_test.py`: Main program that runs the model and produces results in seperate text files.
+ `read_results.py` : Evaluates the results from `make_test.py` and creates the statistics of __Data Analysis__ section in the paper.
+ `data_init.ipynb`: Parses the raw dataset to remove missing values, create missing value heat maps, and generate line plots with rolling mean and standard deviation for better visualization.
