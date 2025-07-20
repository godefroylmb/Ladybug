# Ladybug classification

This project was a course project from ISEP. The goal was to classify ladybugs using a dataset of images. We had access to RGB image and segmented images. Ladybugs had to be classified into 2 species, the principal difficulty was to run our own features extraction to be able to fully explain/control the process. Once features were extracted, we used an explainable model to classify the ladybugs.

## Dataset
The dataset used to train the model is the [ladybug folder](/ladybug/). It contains both RGB images and segmented images.
The test dataset is available in the [test folder](/test/), it was used to test the model.

## Features extraction
The features extraction was done using a custom script that extracts various features from the images. Full details of the features extraction process and reasoning can be found in the [features extraction notebook](/feature_extraction.ipynb).

## Classification
The [classification notebook](/classification.ipynb) contains the code used to train classification models and evaluate their performance. We first trained and validated the model using the training dataset, and then tested it on the test dataset. The classification was done using an explainable model to ensure that we could interpret the results.

## Files
- `training_labels.md`: is the base dataset given with the training images, it contains the labels for each image.
- `training_labels_completed.csv`: is the training dataset completed with the extracted features.
- `test_labels.md`: is the base dataset given with the test images, it contains the labels for each image, the labels is only used to evaluate the model and never used in the training process.
- `test_labels_completed.csv`: is the test dataset completed with the extracted features