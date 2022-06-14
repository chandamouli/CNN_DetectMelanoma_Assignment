# CNN based model to detect melanoma
> To build a CNN based model which can accurately detect melanoma.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

- The data set contains the following diseases:

    Actinic keratosis
    Basal cell carcinoma
    Dermatofibroma
    Melanoma
    Nevus
    Pigmented benign keratosis
    Seborrheic keratosis
    Squamous cell carcinoma
    Vascular lesion

The following models are created in this project
   1. Create a base CNN model 
   2. Create a second model and use data augmentation to resolve the overfitting issues in base model
        - RandomFlip
        - RandomRotation
        - RandomZoom
   3. Create a third model post class re-balance using augmentor library to add 500 images for each class
<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- From base model or model 1
    * The model is overfitting because the training accuracy is around 70% but validation accuracy is around 51% 
    * also after epoch 7, there is a huge deviation in the loss between validation and training.
- From model 1 post data augmentation
    * The overfitting issue from model1 is resolved due to data augmentation
    * However the training accuracy dropped from 70% to 40%
    * Number of epocs can be increased or more layers added and/or tune the hyper parameters to increase accuracy
- From model 2 post class re-balance
    * Accuracy on training data has increased by class rebalance using Augmentor library
    * Model is still overfitting
    * Overfitting can be resolved by adding more layers, neurons and dropout layers
    * Accuracy can be further improved by tuning the hyperparameters

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- numpy
- pandas
- tensorflow - Keras, pre-processing,callbacks
- google colab


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- This project was inspired by CNN based model to detect melonam assignment from upgrad
- Stackoverflow for certain code snippets and to understand the usage of augmentation
- tensorflow official documentation to understand various api's used in this project


## Contact
Created by [@chandamouli] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->