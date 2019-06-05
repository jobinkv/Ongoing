# A breaf article on on-going work and it's progress.



We choose a sample dataset from rvl-cdip with 10K trainig and 2k testing

|approach|accuracy|accuracy with finetuning|Finetune with [res2net](#res2net) layer|
|--|--|--|--|
VGG 19 (FC)|61%|87%|?|
VGG 19 (FV)|74%|75%|
VGG 19 (FV+FC)|74%|89\% at C=0.01|?|
Resnet 152 (FC)|?|69\%|?|
Resnet 152 (FV)|68%|72\%|?|
Densenet|?|?|?|

# Res2Net
The [paper](https://arxiv.org/pdf/1904.01169.pdf) propose an hierarchical residual-like
connections within one single residual block
![Res2net](pic1.png)


# Related links
[Deep feature experiments and results on caltech dataset](deepFeatureEXP.md)
