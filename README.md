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
|[Resnext](#resnext)|91.18%|
|[DFL](#dfl)|91.73%|
|[TEN](#ten)|?%|
|[DFL](#dfl)+[TEN](#ten)|91.85%|


##### DFL
```
@inproceedings{wang2018learning,
  title={Learning a discriminative filter bank within a CNN for fine-grained recognition},
  author={Wang, Yaming and Morariu, Vlad I and Davis, Larry S},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  pages={4148--4157},
  year={2018}
}
```
##### TEN
```
@inproceedings{zhang2017deep,
  title={Deep ten: Texture encoding network},
  author={Zhang, Hang and Xue, Jia and Dana, Kristin},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={708--717},
  year={2017}
}
```

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
