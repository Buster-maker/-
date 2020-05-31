# 基于卷积神经网络的农作物病虫害识别程序设计
本项目以神经网络VGG16和AlexNet为基础实现对农作物病虫害的识别任务，在识别任务中加载网络在ImageNet上的训练得到的权重文件，固定了网络的卷积层进行微调，从而达到较好的识别效果。
### 环境配置
+ macOS 10.15.3
+ Python3.7
+ Pytorch1.1.0、
+ pycharm
### AtrainDataset & Atestdataset
数据集来源于PlantVillage,将数据集分成80%的为训练集AtrainDataset，20%的为测试集Atestdataset。
### 权重
Alex.pth和VGG16.pth分别是在Alex和VGG16上训练得到的权重。
### 代码介绍
+ Alexnet.py  Alexnet模型搭建代码。
+ model.py  VGG16模型搭建代码。
+ Classify.py 训练代码，分别可以使用AlexNet和VGG16对数据集进行训练。
+ detect.py 对VGG16进行模型的测试，获得VGG16在测试集上的准确率。
+ detectAlexnet.py  对AlexNet进行模型的测试，获得AlexNet在测试集上的准确率。
### 训练 
> python Classify.py
### 测试
> python detect.py &  python deteceAlexNet.py
### Headmap
+ headmap.py headmp的生成程序
+ VGG16.py VGG16网络模型
+ pca_project.py 对feature进行主成分分析
#### 生成headmap
```
python headmap.py
```
Headmap
(![Alt text](https://github.com/tsfw/-/blob/master/picture1.png)
(![Alt text](https://github.com/tsfw/-/blob/master/picture2.png)
### 结果
|模型  | AlexNet|  VGG16|
|--|--|--|
|  准确率| 96.82% |97.40%|
