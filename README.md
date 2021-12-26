# Crop-Yield-Prediction
This repository contains my work on Study Oriented Project, Time Series Analysis at BITS Pilani

### Problem Statement
Accurate and timely estimation of crop yield at a small scale is of great significance to food security and harvest management. Recent studies have proven remote sensing is an efficient method for yield estimation and machine learning, especially deep learning, can infer a good prediction by integrating multi-source datasets like satellite data, climate data, soil data, and so on. However, there are some bottleneck challenges to improve accuracy. First, the popular remote sensing data used for yield prediction fall into two major groups, time-series data, and constant data. Surprisingly little attention has been devoted to deep learning networks that can integrate the two kinds of data effectively; second, both temporal and spatial features play a role in affecting the yields. This paper proposed a novel multi-level deep learning (MLDL) model coupling RNN and CNN to extract both spatial and temporal features. The inputs include both time-series remote sensing data and soil property data and the model outputs yield.

For detailed explanation here is the link to [paper](https://www.researchgate.net/publication/343865804_Multilevel_Deep_Learning_Network_for_County-Level_Corn_Yield_Estimation_in_the_US_Corn_Belt)

<hr>

### Structure

There are 4 functionalities:

1. Data Export : Taken care by Export.ipynb file. This file basically exports data export MODIS data from Google Earth Engine to Google Drive as per requirements.
2. Data Cleaning: Taken care by DataCleaner.ipynb file. It performs the following functions:
- split the image collections into years
- merge the temperature and reflection images
- apply the mask, so only the farmland pixels are considered 
3. Data Engineering: Taken care by Engineer.ipynb file. Takes the preprocessed data from the Data Cleaner and turn the images into matrices which can be input into the machine learning models. These matrices are histograms, which describe the distributions of pixels on each band, and contain 32 bins. This turns the band of an image from dim=(width*height) to dim=32.
4. Data training and testing: Taken care by Model.ipynb file. Train and test on keras model. Further, generates an svg of the counties, coloured by their prediction error.

<hr>

### Approach
The architecture of the MLDL-Net: ![image description](https://github.com/lakshya0904/Crop-Yield-Prediction/blob/main/MLDL-Net_arch.png)

<hr>


### Group Members
- Lakshya Agarwal, 2017B5A70904P
- Aditya Vishwakarma, 2017B5A70954P
- Arshveer Kaur

