# Introduction

# Related works

# Proposed Approach

# Experiments
The proposed approach was evaluated on the document image classification task with RVL-CDIP dataset.
The RVL-CDIP dataset consists of scanned grayscale images of documents
from lawsuits against American Tobacco companies and is
segregated into 16 categories or classes. The dataset is subdivided into
training, validation and test sets each containing 320000,
40000 and 40000 images respectively.<br />
As a preprocessing similar to [[1](#tensmeyer2017analysis)], the images are resize to 384 \* 384 and single image channel was duplicated to 3 channels for the network compatibility.  

## Experiment 1

Aim: Compare with state of the art approaches.
### Experimental setup: 
Dataset: rvlcdip <br />
Main parameters:<br />
Network: resnext101 trained on rvlcdip dataset.<br />
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
|[TEN](#ten)|91.2%|
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
## Experimental Results
<table>
<th> Performance Comparison with State-of-the-art Approaches</th>
<tr><td>

Method | Accuracy(%) | Comments
--- | --- | ---
Harley et al. [1]  | 89.90 | Document region based DCNN models with transfer learning
Tensmeyer et al. [2] | 89.31 | Spatial pyramidal pooling based AlexNet without transfer learning
Tensmeyer et al. [2] | 90.94 | Same model as above with increased image dimension (384X384) keeping aspect ratio same
Csurka et al. [3]  | 90.70 | GoogleNet with weights transferred from ImageNet
Afzal et al. [4] | 90.97 | VGG-16 with weights transferred from ImageNet
Kölsch et al. [5] | 90.05 | Weights transferred from ImageNet to VGG-16 and adding ELM in place of MLP
Das et al. | 91.11 | VGG-16 model trained on holistic samples with weights transferred from ImageNet
Das et al. | 92.21 | Inter and intra domain transfer learning on region based DCNNs and MLNN based stacking


</td></tr> </table>
# Conclusions

# References

[1] A. W. Harley, A. Ufkes, and K. G. Derpanis, “Evaluation of deep convolutional nets for document image classification and retrieval,” in _Document Analysis and Recognition (ICDAR), 2015 13th International Conference on_. IEEE, 2015, pp. 991–995.<Enter>
  
[2] C. Tensmeyer and T. Martinez, “Analysis of convolutional neural networks for document image classification,” _arXiv preprint arXiv:1708.03273_, 2017.<Enter>

[3] G. Csurka, D. Larlus, A. Gordo, and J. Almazan, “What is the right way to represent document images?” _arXiv preprint arXiv:1603.01076_, 2016.<Enter>

[4] M. Z. Afzal, A. K¨olsch, S. Ahmed, and M. Liwicki, “Cutting the error by half: Investigation of very deep cnn and advanced training strategies for document image classification,” _arXiv preprint arXiv:1704.03557_, 2017.<Enter>

[5] Andreas Kölsch, Muhammad Zeshan Afzal, Markus Ebbecke, Marcus Liwicki, "Cutting the Error by Half: Investigation of Very Deep CNN and Advanced Training Strategies for Document Image Classification", _arXiv preprint arXiv:1704.03557_, 2017.
[6] Das, Arindam, et al. "Document Image Classification with Intra-Domain Transfer Learning and Stacked Generalization of Deep Convolutional Neural Networks." 2018 24th International Conference on Pattern Recognition (ICPR). IEEE, 2018.
<Enter>

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
##### tensmeyer2017analysis
```
@inproceedings{tensmeyer2017analysis,
  title={Analysis of convolutional neural networks for document image classification},
  author={Tensmeyer, Chris and Martinez, Tony},
  booktitle={2017 14th IAPR International Conference on Document Analysis and Recognition (ICDAR)},
  volume={1},
  pages={388--393},
  year={2017},
  organization={IEEE}
}
```
