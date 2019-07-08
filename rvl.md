# Journal work on deep features


We have done the following experiment and the result and observation are given below.

## Problem
Document figure classification
Classify the document figure into its coresponding classes using deep features.

## Dataset
We chose the dataset of RVL CDIP. This dataset contains 400K images in wich 320K, 40K,40K for training validaton and testing. Inorder to run the experiment we choose a small data from the set. 10K,2K,2K or training validaton and testing.

# Result
The result are given in the below table.
* FC - indicate the feature extracted from the fully connected layer
* FV - indicate the feature extracted from the convolutional layer with Fisher vector pooling.

|approach|accuracy|accuracy with finetuning|
|--|--|--|
VGG 19 (FC)|61%|87%|
VGG 19 (FV)|74%|75%|
VGG 19 (FV+FC)|74%|87\%|
Resnet 152 (FC)|67\%|69\%|
Resnet 152 (FV)|68%|72\%|
densenet161 (FV)|68\%|?|


# Related links
[Deep feature experiments and results on caltech dataset](deepFeatureEXP.md)
