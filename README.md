# A breaf article on on-going work and it's progress.


## Experiment 1
Aim: Compare with state of the art approaches.
### Experimental setup: 
Dataset: rvlcdip
Main parameters:
Network: resnext101 trained on rvlcdip dataset (91.18\%).
Input image size: 224*224
batch size: 32
momentum: 0.9
learning rate: 0.005
learning rate update: [ref](https://scholar.googleusercontent.com/scholar.bib?q=info:rxYcO-LPyYMJ:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlN2ws8:AAGBfm0AAAAAXYBz2s8jn5zP6cRsjA6kfPmVZIR7CY-b&scisig=AAGBfm0AAAAAXYBz2gr2xbnG5boA2rp2KQFtq2fFYpOy&scisf=4&ct=citation&cd=-1&hl=en)
loss: cross entropy loss
Maximum number o iterations: 10
optimizer : Stochastic gradient decent.



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
