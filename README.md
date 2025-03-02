# Image-Caption-Generator-using-Deep-Learning-on-Flickr8K-dataset

## Introduction
The basic working of the project is that the features are extracted from the images using pre-trained VGG16 model and then fed to the LSTM model along with the captions to train. The trained model is then capable of generating captions for any images that are fed to it.

## Dataset
The dataset used here is the **[FLICKR 8K](https://forms.illinois.edu/sec/1713398)** which consists of around 8091 images along with 5 captions for each images. 
If you have a powerful system with more than 16 GB RAM and a graphic card with more than 4 GB of memory, you can try to take **[FLICKR 30K](http://web.engr.illinois.edu/~bplumme2/Flickr30kEntities/)** which has around 30,000 images with captions.


1. Flickr8k_Dataset.zip  https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip

2. Flickr8k_text.zip https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip


## Plotting few images and their captions from the dataset

![image](https://github.com/user-attachments/assets/e0466f81-396c-4d07-83f8-aad44f430fa4)

## Plotting the top 50 words that appear in the cleaned dataset

![image](https://github.com/user-attachments/assets/6ab9f226-401b-4d9b-9fde-54535c5138a7)

## Loading VGG16 model and weights to extract features from the images
The pre-trained weights for the VGG-16 model can be downloaded from [here](https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg16_weights_tf_dim_ordering_tf_kernels.h5).

<img width="435" alt="image" src="https://github.com/user-attachments/assets/c132636a-0a87-4499-a244-d072e5bbd943" />

## Plotting similar images from the dataset
For this we have to first create a cluster and find which images belong together. Hence PCA is used to reduce the dimensions of the features which we got from VGG-16 festure extraction from **4096** to **2**

First the clusters are plotted and few examples are taken from the bunch for displaying

![image](https://github.com/user-attachments/assets/3de46148-7057-49e4-8116-c12221d94899)

## Building the LSTM model

<img width="867" alt="image" src="https://github.com/user-attachments/assets/58edd1bb-a8a1-4769-9003-7cd4618d1ce1" />

## Training the LSTM model

![image](https://github.com/user-attachments/assets/528ab851-577a-4ae9-b2b6-14d382844176)

## Generating captions on a small set of images
After the model finishes training we can test out its performance on the some of the test images to figure out if the generated captions are good enough. If the generated captions are good enough we can generate the captions for the whole test dataset.

**Output:**

![image](https://github.com/user-attachments/assets/acfccb6f-6d54-424f-8f1c-da6d09e0c156)






