# MLND Project 5 - Image Classification

## Introduction

在这一项目中，你需要对 **CIFAR-10 数据集** 进行图像分类。

该数据集包含飞机，狗，猫等一共10个类型的图片，共50000张。你需要先对数据集进行预处理，然后用卷积神经网络对所有样本进行训练。你要先将图像归一化（normalize），对标签进行独热编码（one-hot encode the labels），然后建立卷积层、最大池化层和全连接层。最后，你将看到该模型对样本图像作出的预测结果。


## Performance

- **MNIST**

    | Model | Epochs   | Accuracy |
    | :---  | :------: | :-------: |
    | 传统神经网络 `FC1024`, `FC1024` | 50 | **98%**
    | 卷积神经网络 类VGG结构       | 50 | **99.5%**

- **CIFAR10**

    | Model | Epochs   | Accuracy |
    | :--- | :------: | :-------: |
    | TensorFlow `CONV16`, `CONV32`, `CONV64`, `FC128` | 100 | **70%**
    | TensorFlow `CONV16`, `CONV32`, `CONV64`, `FC128` (Xavier, BN, L2)       | 100 | **72%**
    | Keras 类VGG `(CONV / CONV / POOL) * 3`, `FC128` | 100 | **80%**
    | Keras 类VGG `(CONV / CONV / POOL) * 3`, `FC128` (With Data Augmentation) | 100 | **89%**

## Methodology

- **Preprocessing**
    - Normalize
    - One-hot Encoding
    
- **Model Construction**
    - Input Layer
    - Convolution + Maxpooling Layer
    - Flatten Layer
    - Fully Connected Layer
    - Dropout
    - Output Layer
    
- **Parameter Fine Tuning**
    - epoch
    - batch_size
    - stddev
    - conv_num_output
    - conv_size (width x height)
    - conv_stride
    - pooling_size (width x height)
    - pooling_stride
    - full_num_output
    - Activation Function (Conv Layer, Fully Connected Layer)
    - Padding Style