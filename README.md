# img-classify
Image Classification for Ants and Bees

## Overview
This package utilises neural network models to classify Ants and Bees from a given training and validation datasets. Two models are used for comparison use. 
1. Simple Neural Network
2. Computational Neural Network based on VGG16

## Installation
Once cloned (via git) or downloaded to the local drive, python scripts schould run directly from the folder.

### Required Packages
Package was developed for use on Windows 10 x64 machine. Should run on other platforms if the required packages and dependencies are already configured.

- Python 3.6
- OpenCV 4.1.0
- tensorflow==1.10.0
- keras

### Dependencies
- protobuf==3.6.0
- imutils
- scikit-learn
- matplotlib

If running on a Windows 10 machine, then also install opencv-python with pip.

## Examples
To setup model based on training data:
```
python train_vgg.py --dataset data\train --model output\smallvggnet.model --label-bin output\smallvggnet_lb.pickle --plot output\smallvggnet.png
```

To setup model based on training and validation data:
```
python train2_vgg.py --dataset data\train --valdataset data\val --model output\smallvggnet.model --label-bin output\smallvggnet_lb.pickle --plot output\smallvggnet.png
```

To predict on new data:
```
python predict.py --image images\test1.jpg --model output\smallvggnet.model --label-bin output\smallvggnet_lb.pickle --width 64 --height 64
```
