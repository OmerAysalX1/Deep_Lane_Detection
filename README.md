# Deep_Lane_Detection

This project is a documentation study examining the performance of different deep learning architectures in the lane detection task. The behavior, outputs, and architectural visuals of each model are described under separate headings.

## 🚗 Veri Setim

This study was conducted using the TuSimple Lane Detection Dataset.

Dataset link:
--> [https://github.com/TuSimple/tusimple-benchmark](https://www.kaggle.com/datasets/manideep1108/tusimple). [1]

The dataset size is large and has not been added to this repo.

## 🚀 How to Run?

A requirements.txt file has been shared for this project.
This environment is used in my own CNN projects, so it also includes many additional libraries.
However, for this project, only the following libraries are required to run it:

-TensorFlow
-NumPy
-Pandas
-Matplotlib
-Seaborn
-OpenCV
-tqdm
-Scikit-learn
-TensorFlow Keras components (applications, layers, Model)
-Warnings module
-Python standard libraries such as OS, shutil, and random

These libraries are sufficient to run the VGG19, ResNet50, MobileNet, DenseNet121, and EfficientNet-B0 models.


## 🧩Installation Steps
1. Install the dependencies
pip install -r requirements.txt

2. Download the dataset

Download the TuSimple dataset from the link above and place it in your own folder.

3. Run the project

python3 lane_seg.ipynb

📂 Models Examined

VGG19

ResNet50

MobileNet

DenseNet121

EfficientNet-B0

For each model:

Architectural image

Brief description




## VGG19
Architecture:

<img width="600" height="344" alt="image" src="https://github.com/user-attachments/assets/279b02fc-7bfb-41fb-9228-1dd6c8f46bdb" />

                                                  [2]

Observations:

This model is a specialized VGG19-Seg architecture for pixel-based segmentation, incorporating the convolutional encoder structure of VGG19, removing the FC layers, and adding a U-Net-type skip-connection and decoder.

## RenNet50

Architecture:

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/aa30d49b-174f-447f-928f-44fa72de8b59" />

                                                  [3]

Observations:

This model is a ResNet50-Seg architecture that takes the convolutional backbone of ResNet50, removes FC layers, and adds U-Net-style decoder and upsampling layers. It is designed for pixel-based segmentation without using skip-connection.

## MobileNet

Architecture:

<img width="850" height="471" alt="image" src="https://github.com/user-attachments/assets/d7dd09f1-6168-4102-b6cf-e273963b9bd5" />

                                                  [4]

Observations:

This model is a specialized MobileNet-Seg architecture for pixel-based segmentation, taking the convolutional backbone of MobileNet, removing FC layers, and adding U-Net-style decoder and upsampling layers.

## EfficentNet

Architecture:

<img width="1364" height="669" alt="image" src="https://github.com/user-attachments/assets/907feea7-7a4e-44ce-831a-6bf0d35fc0ce" />

                                                  [5]

Observations:

This model is a specialized EfficientNet-Seg architecture for pixel-based segmentation, based on the convolutional backbone of EfficientNetB0, with FC layers removed and U-Net-type decoder and upsampling layers added.

## DenseNet

Architecture:

<img width="850" height="253" alt="image" src="https://github.com/user-attachments/assets/a0d73af4-6dbf-479a-9191-d3bf7e109835" />

                                                  [6]

Observations:

This model is a specialized DenseNet-Seg architecture for pixel-based segmentation, based on the convolutional backbone of DenseNet121, with FC layers removed and U-Net-type decoder and upsampling layers added.

## 📊 Results

In this project, lane detection was performed using VGG19, ResNet50, MobileNet, EfficientNet, and DenseNet models.
The predictions made by each model on the test dataset represent the pixel-based segmentation results.
These outputs can be visualized and compared with IoU/accuracy scores going forward.

## 📚 References
1.https://www.kaggle.com/datasets/manideep1108/tusimple

2.https://www.kaggle.com/discussions/getting-started/518971

3.https://wisdomml.in/understanding-resnet-50-in-depth-architecture-skip-connections-and-advantages-over-other-networks/

4.https://www.researchgate.net/figure/MobileNet-V1-architecture_fig3_376752661

5.https://www.ultralytics.com/blog/what-is-efficientnet-a-quick-overview

6.https://www.researchgate.net/figure/A-schematic-illustration-of-the-DenseNet-121-architecture-82_fig5_334170752
