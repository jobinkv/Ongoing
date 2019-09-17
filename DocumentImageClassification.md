# Introduction

# Related works

# Proposed Approach

# Experiments
The proposed approach was evaluated on the document image classification task with RVL-CDIP dataset.
The RVL-CDIP dataset consists of scanned grayscale images of documents
from lawsuits against American Tobacco companies and is
segregated into 16 categories or classes. The dataset is subdivided into
Training, Validation and Test Sets each containing 320000,
40000 and 40000 images respectively.<br />


## Experiment 1

Aim: Compare with state of the art approaches.
### Experimental setup: 
Dataset: rvlcdip <br />
Main parameters:<br />
Network: resnext101 trained on rvlcdip dataset (91.18%).<br />
Input image size: **224*224**<br />
batch size: 32<br />
momentum: 0.9<br />
learning rate: 0.005<br />
learning rate update: cosine decay [ref](#cosine-decay)<br />
loss: cross entropy loss <br />
Maximum number of iterations: 10 <br />
optimizer : Stochastic gradient decent. <br />

|approach|accuracy|
|--|--|
|[Resnext](#resnext)|91.11%|
|[DFL](#dfl)|91.73%|
|[TEN](#ten)|?%|
|[DFL](#dfl)+[TEN](#ten)|91.85%|

## Experiment 2
Aim: Compare with state of the art approaches.
### Experimental setup: 
Dataset: rvlcdip <br />
Main parameters:<br />
Network: resnext101 trained on rvlcdip dataset (91.18%).<br />
Input image size: **384*384**<br />
batch size: 32<br />
momentum: 0.9<br />
learning rate: 0.005<br />
learning rate update: cosine decay [ref](#cosine-decay)<br />
loss: cross entropy loss <br />
Maximum number of iterations: 10 <br />
optimizer : Stochastic gradient decent. <br />

|approach|accuracy|
|--|--|
|[Resnext](#resnext)|91.18%|
|[DFL](#dfl)|?%|
|[TEN](#ten)|?%|
|[DFL](#dfl)+[TEN](#ten)|?%|





# Results

# Conclusions

# References
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
##### ResNext
```
@inproceedings{xie2017aggregated,
  title={Aggregated residual transformations for deep neural networks},
  author={Xie, Saining and Girshick, Ross and Doll{\'a}r, Piotr and Tu, Zhuowen and He, Kaiming},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={1492--1500},
  year={2017}
}
```
##### Cosine decay
```
@article{loshchilov2016sgdr,
  title={Sgdr: Stochastic gradient descent with warm restarts},
  author={Loshchilov, Ilya and Hutter, Frank},
  journal={arXiv preprint arXiv:1608.03983},
  year={2016}
}
```
