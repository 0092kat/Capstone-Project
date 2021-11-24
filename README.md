# Performing Brain Tumor classification and Segmentation

## Brief Description

This project was designed by Katlego Reuben KGOSI, and Mishi MAKADE, as our end year Bachelors degree in Data Science Capstone Project. The project classifies brain tumor MRI images, and segments the images. This project was motivated by seeing that EfficientNetB7 is one the best common pre-trained transfer learning models, but it hasnt been implemented in brain tumor classification. so we decided to compare it with state of the art most common best pre-trained transfer learning model VGG16. In this project we compare VGG16 and EfficientNetB7 in relation to accuracy and complexity and time of training and prediction. And implement the Best model in a web application.

###### _Keywords_
> `EfficientNetB7`, `VGG16`, `classification`,  `segmentation`, `transfer learning`, `pre-trained model`

## Overview

| **Table of Content**              | 
| --------------------------------- | 
| _Specifications and requirements_ | 
| _Content of project with results_ | 
| _Acknowledgements_                | 
| _Web Application_                 | 

## Specifications and requirements

Machine Specifications

| **Table of Content**   |   **Description**                                   |
| ---------------------- |  -------------------------------------------------- |
| `Operating system`     | Windows 10 & Windows 11 64-bit operating system     |
| `RAM`                  | 8GB & 16GB                                          |
| `Graphics`             | Intel(R) Core(TM) i5-8265U CPU @ 1.60GHz   1.80 GHz |
| `Editors`              | Jupyter Notebbok, Spyder, Google Colab              |

Requirements

1. Python
2. Tensorflow
3. Keras
4. matplotlib
5. Streamlit

## Content of project with results

**1. Data Collection & Pre-Processing**

The data was downloaded from kaggle, Read the [README file](Documents/README.md) to get the link for the dataset.

_A Glimpse of the data_

[Picure of the DATASET]

_Pre-Processing of the data_

The images where transformed inthr following manner

| **Transformation**               |   **OutPut**                                  |
| -------------------------------- |  -------------------------------------------- |
| horizontal flipping              |   OutPut                                      |
| vertical flipping                |   OutPut                                      |
| zooming at 0.2                   |   OutPut                                      |
| rotation at 20 degrees           |   OutPut                                      |
| featurewise_std_normalization    |   OutPut                                      |
| shear-range of 0.2               |   OutPut                                      |
| brightening at the range 0.2-1.5 |   OutPut                                      |
| width shift range of 0.1         |   OutPut                                      |
| height shift range of 0.1        |   OutPut                                      |


**2. Model Development and Fine-tuning**

The Efficientnet model development and fine tuning

in this notebook we will load and add our layers to the base model of the pre-trained EfficientnetB7 model, and fine tune the following parameters of the model:

    Optimizers - We will use only 5 optimizers to see which one works best, namely; 1. SGD,2. RMSprop,3. Adam,4. Adagrad,5. Adadelta. the best optimizer will be used in the New model
    Number of epochs - We will also use only 4 epochs to choose the best performer namely; 1, 2, 5, 10.
    Batch size - we will also use these batch sizes to choose the optimum batch size, namely; 8, 16.
    Dropout - we will optimise the dropout of the model, values 0.5, 0.6, 0.7, 0.8, 0.9

    Section one: we will create common function and also create our base model, with the following initial parameters: Batch size 8, Optimizer Adam, Number of epochs 4, dropout value 0.5

**3. Final Model Implementation and Results**


## Acknowledgements

## Web Application
