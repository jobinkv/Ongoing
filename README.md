### Deep feature experiments and results


## Existing results

The result reported in respective papers for Caltech dataset 

| Approach |Caltech-101 |caltech 256|
|--|--|--|
|[FVCNN](https://www.robots.ox.ac.uk/~vedaldi/assets/pubs/cimpoi15deep.pdf)  | ? |?
[Deep-Ten](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhang_Deep_TEN_Texture_CVPR_2017_paper.pdf)|85.3|?
[E2E-SCN-SPP](https://link.springer.com/content/pdf/10.1007%2Fs11063-018-9967-5.pdf)|94.3|86.5
[ProCRC](http://azadproject.ir/wp-content/uploads/2014/07/2015-A-Probabilistic-Collaborative-Representation-based-Approach-for-Pattern-Classification.pdf)|94.8|86.1


### Result of FV-CNN reported in various paper


Paper|Caltech-101 |caltech 256|
|--|--|--|
[Deep-Ten](http://openaccess.thecvf.com/content_cvpr_2017/papers/Zhang_Deep_TEN_Texture_CVPR_2017_paper.pdf)|83.0|?|
[E2E-SCN-SPP](https://link.springer.com/content/pdf/10.1007%2Fs11063-018-9967-5.pdf)|90.3|81.2|

## Experiment 1
### General experimental setup
Input image size set to 224&times;224 for all experiment except FV-CNN and FV+FC-CNN.
The convolutional network for feature extraction are not trainable.

|Exp params|Value|
|--|--|
|Learning rate| 0.005
| train_batch_size | 16 |
|input_size|224&times;224|
|weight decay|0.0001|
|lr decay|0|
|momentum|0.9|


Experiment setup|Caltech-101|Caltech-256|
|--|--|--|
FV-CNN on VGG_VD|86.69|214673|
FV+FC-CNN on VGG_VD|92.34|?|
VGG-VD fineturn|[75.13](http://10.2.16.142/r1/ijdar/215776.html)|[65.27](http://10.2.16.142/r1/ijdar/216041.html)|
VGG-VD +[PPM](#ppm)|[81.02](http://10.2.16.142/r1/ijdar/216766.html)|[64.62](http://10.2.16.142/r1/ijdar/216686.html)|
VGG-VD<sup>*</sup> +[PPM](#ppm)|?|[60.19](http://10.2.16.142/r1/ijdar/216648.html)|
VGG-VD +[SPP](#spp) |?|?|
VGG-VD +[PPM](#ppm)+[SPP](#spp)|?|?|
VGG-VD +[SCN](#scn)+[SPP](#spp)|?|?|
VGG-VD +[PPM](#ppm)+[SCN](#scn)+[SPP](#spp)|?|?|
Resnet 152 finetune|[86.5](http://10.2.16.142/r1/ijdar/215833.html)|[80.91](http://10.2.16.142/r1/ijdar/215918.html)|
Resnet 152 +[PPM](#ppm)|[88.32](http://10.2.16.142/r1/ijdar/217200.html)|[77.69](http://10.2.16.142/r1/ijdar/217251.html)|
Resnet 152 +[SPP](#spp)|[89.88](http://10.2.16.142/r1/ijdar/217174.html)|?|
Resnet 152 +[PPM](#ppm)+[SPP](#spp)|[90.85](http://10.2.16.142/r1/ijdar/217263.html)|?|
Resnet 152 +[SCN](#scn)+[SPP](#spp)|?|?|
Resnet 152 +[PPM](#ppm)+[SCN](#scn)+[SPP](#spp)|?|?|


<sup>*</sup> learnable convolution layer --> slow converge
___
#### SPP
![SPP](pic1.png)


*A network structure with a spatial pyramid
pooling layer (SPP). Here 512 for VGG and 2048 or resnet is the filter number of the last convolutional layer.* [Kaiming He 2015](https://arxiv.org/pdf/1406.4729.pdf)
___
#### PPM
![SPP](pic2.png)


*A pyramid parsing module (PPM) is applied to harvest different sub-region representations, followed by upsampling and concatenation layers to form the final feature representation, which carries both local and global context information* [Hengshuang Zhao 2017](https://arxiv.org/pdf/1612.01105.pdf)


___
#### SCN
![SPP](pic3.png)


*A sparse coding network (SCN) is applied to encode the deep convolutional features* [Boheng Chen 19](https://link.springer.com/content/pdf/10.1007%2Fs11063-018-9967-5.pdf)
