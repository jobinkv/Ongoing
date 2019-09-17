# A breaf article on on-going work and it's progress.


## Experiment 1
Aim: Compare with state of the art approaches.
### Experimental setup: 
Dataset: rvlcdip <br />
Main parameters:<br />
Network: resnext101 trained on rvlcdip dataset (91.18%).<br />
Input image size: 224*224<br />
batch size: 32<br />
momentum: 0.9<br />
learning rate: 0.005<br />
learning rate update: cosine decay [ref](https://scholar.googleusercontent.com/scholar.bib?q=info:rxYcO-LPyYMJ:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlN2ws8:AAGBfm0AAAAAXYBz2s8jn5zP6cRsjA6kfPmVZIR7CY-b&scisig=AAGBfm0AAAAAXYBz2gr2xbnG5boA2rp2KQFtq2fFYpOy&scisf=4&ct=citation&cd=-1&hl=en)<br />
loss: cross entropy loss <br />
Maximum number of iterations: 10 <br />
optimizer : Stochastic gradient decent. <br />

|approach|accuracy|
|--|--|
|[Resnext](https://scholar.googleusercontent.com/scholar.bib?q=info:7cOWMQ1bebQJ:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlOFcMw:AAGBfm0AAAAAXYCAaMwPIWK0PeR6k5nh8iSFzVORNUHD&scisig=AAGBfm0AAAAAXYCAaKs4c_6xOdBTA-exDfhVc79ulLis&scisf=4&ct=citation&cd=-1&hl=en)|91.18%|
|[DFL](https://scholar.googleusercontent.com/scholar.bib?q=info:NMEU4q_QWJ4J:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlNymcI:AAGBfm0AAAAAXYB3gcJeNkJb4Uq_qX8VTk3HgSErjBw6&scisig=AAGBfm0AAAAAXYB3gcqSiLvSqEUVQM62LdniOwcxFM4N&scisf=4&ct=citation&cd=-1&hl=en)|91.73%|
|[TEN](https://scholar.googleusercontent.com/scholar.bib?q=info:gRUOCuIJ_ZAJ:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlN9Wcc:AAGBfm0AAAAAXYB4QcdfG4aNs2C2hzVNXuVcvvtfRsHS&scisig=AAGBfm0AAAAAXYB4QQVQonrJ05r0prM986tNqnWYTet9&scisf=4&ct=citation&cd=-1&hl=en)|?%|
|[DFL](https://scholar.googleusercontent.com/scholar.bib?q=info:NMEU4q_QWJ4J:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlNymcI:AAGBfm0AAAAAXYB3gcJeNkJb4Uq_qX8VTk3HgSErjBw6&scisig=AAGBfm0AAAAAXYB3gcqSiLvSqEUVQM62LdniOwcxFM4N&scisf=4&ct=citation&cd=-1&hl=en)+[TEN](https://scholar.googleusercontent.com/scholar.bib?q=info:gRUOCuIJ_ZAJ:scholar.google.com/&output=citation&scisdr=CgWP9T8GEJ-utlN9Wcc:AAGBfm0AAAAAXYB4QcdfG4aNs2C2hzVNXuVcvvtfRsHS&scisig=AAGBfm0AAAAAXYB4QQVQonrJ05r0prM986tNqnWYTet9&scisf=4&ct=citation&cd=-1&hl=en)|91.85%|



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
