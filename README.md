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

The data was downloaded from kaggle, Read the [README file](DataSet/README.md) to get the link for the dataset.

_A Glimpse of the data_

![DataSet](/README-images/DataSet.png)

_Pre-Processing of the data_

The images where transformed in the following manner

| **Transformation**               |   **OutPut**                                     |
| -------------------------------- |  ----------------------------------------------- |
| Original Image                   | ![Transformation](/README-images/original.png)   |
| horizontal flipping              | ![Transformation](/README-images/horizontal.png) |
| vertical flipping                | ![Transformation](/README-images/vertical.png)   |
| zooming at 0.2                   | ![Transformation](/README-images/zoom.png)       |
| rotation at 20 degrees           | ![Transformation](/README-images/rotation.png)   |
| featurewise_std_normalization    | ![Transformation](/README-images/featurewise.png)|
| shear-range of 0.2               | ![Transformation](/README-images/shear.png)      |
| brightening at the range 0.2-1.5 | ![Transformation](/README-images/brightness.png) |
| width shift range of 0.1         | ![Transformation](/README-images/width.png)      |
| height shift range of 0.1        | ![Transformation](/README-images/height.png)     |


**2. Model Development and Fine-tuning**

The following parameters namely: Batch size, Epochs, Dropout and Optimizer, of the model where fined, and the visualisation of the results are below

The following values and parameters where chosen:

- **_Optimizers_** - We will use only 5 optimizers to see which one works best, namely; `1. SGD,2. RMSprop,3. Adam,4. Adagrad,5. Adadelta.` the best optimizer will be used in the New model

- **_Number of epochs_** - We will also use only 4 epochs to choose the best performer namely; `1, 2, 5, 10.`

- **_Batch size_** - we will also use these batch sizes to choose the optimum batch size, namely; `8, 16.`

- **_Dropout_** - we will optimise the dropout of the model, values `0.5, 0.6, 0.7, 0.8, 0.9`

#### EfficientNetB7 - Batch size and Epochs

![FineTuning](/README-images/efn_bNe.png)       


#### VGG16 - Batch size and Epochs

![FineTuning](/README-images/vgg_bNe.png)


#### EfficientNetB7 - Dropout

![FineTuning](/README-images/efn_drop.png)


#### VGG16 - Dropout

![FineTuning](/README-images/vgg_drop.png)


#### EfficientNetB7 - Optimizer

![FineTuning](/README-images/efn_opt.png)


#### VGG16 - Optimizer

![FineTuning](/README-images/vgg_opt.png)



**3. Final Model Implementation and Results**

This is the structure of the EfficientNetB7 model we implemented with optimum parameters, similarly with the VGG16 model.

![Model](/README-images/ModelEFN.png)

## Acknowledgements

I appreciate and acknowledge the supervision of the project by Mr Kudakwashe MADZIMA, my Capstone-Project Lecture at Sol Plaatje University in 2021, and also my collaborater Miss Mishi MAKADE, as we designed and implemented the project together.

## Web Application

will add the section of the Web App soon...

Thank you.
