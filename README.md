# A breaf article on on-going work and it's progress.



We choose a sample dataset from rvl-cdip with 10K trainig and 2k testing

|approach|accuracy(matlab)|accuracy(pytorch)|accuracy with finetuning|Finetune with [res2net](#res2net) layer|
|--|--|--|--|--|
FC VGG 19 | 60.28\%|61\%(vgg19,clf = svm.LinearSVC(C=1)),net.classifier = nn.Sequential(*list(net.classifier.children())[:-2]) minimum value:  0.0 Maximum value: 0.2161|?|?|
FV+FC VGG 19|74.10\%|50\%|?|?|
Resnet 152|?|?|?|?|
Densenet|?|?|?|?|

# Res2Net
The [paper](https://arxiv.org/pdf/1904.01169.pdf) propose an hierarchical residual-like
connections within one single residual block
![Res2net](pic1.png)


# Related links
[Deep feature experiments and results on caltech dataset](deepFeatureEXP.md)
