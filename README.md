# Document image classification

The article can be found [here](DocumentImageClassification.md)


# A breaf article on on-going work and it's progress.



We choose a sample dataset from rvl-cdip with 10K trainig and 2k testing

|approach|accuracy|accuracy with finetuning|Finetune with [res2net](#res2net) layer|
|--|--|--|--|
VGG 19 (FC)|61%|87%|?|
VGG 19 (FV)|74%|75%|?|
VGG 19 (FV+FC)|74%|87\%|?|
Resnet 152 (FC)|67\%|69\%|?|
Resnet 152 (FV)|68%|72\%|?|
densenet161 (FV)|68\%|?|?|
[DFL](https://arxiv.org/pdf/1611.09932.pdf)|92.6%|.|?|
