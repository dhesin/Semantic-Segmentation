## Semantic Segmentation Project Reflections

In this project, road scene image pixels are classified as road or non-road. At the onset of deep learning, applications are developed mostly for classification problems to answer the question of whether an object exists in the image or not and if it exists what is the object type. To answer this question, deep network consisted of several convolutional layers followed by fully connected layer which outputs the probabilities of each type of object. But there is also a localization problem for most of the computer vision applications where we want to know what is in the scene and where it is. In the last couple of year, localization problem has been addressed too with state of the art results.

To answer detection and localization problem, fully convolutional networks (FCN) are developed. YOLO, Faster R-CNN, R-FCN, Single Shot Detectors (SSD) are recent state of the art object detection and localization models. FCNs implement 1x1 convolutions and reverse convolution to obtain high resolution feature maps. There is also a skip connection approach where lower layer activations are served as input not only to one next layer but also other higher layers. Experiments showed that skip connections improve network performance by enabling lower layer high resolution features to low resolution upper layers. 

Semantic Segmantation project implements FCNs on top of VGG network and incepts layers from VGG to some of the FCN layers to improve road pixel classification. Although this project implements FCNs to classify each pixel, it does not do localization where bounding box of the detected objects are also predicted. Localization usually requires another network to propose/predict bounding box location by using pixel classifications. For road segmentation, bounding box information wouldn't be very useful since IoU measure would be small due to non-compact shape of road.

You can find the links to related papers below;

 - [YOLO9000: Better, Faster, Stronger](https://arxiv.org/pdf/1612.08242.pdf)
 - [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](https://arxiv.org/pdf/1506.01497.pdf)
 - [R-FCN: Object Detection via Region-based Fully Convolutional Networks](https://arxiv.org/pdf/1605.06409.pdf)
 - [SSD: Single Shot MultiBox Detector](https://arxiv.org/pdf/1512.02325v5.pdf)
 - [MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications](https://arxiv.org/pdf/1704.04861.pdf)
