# Identifying the Viral spread of COVID-19 using Deep learning

## Introduction
COVID-19 has had a negative impact on the health and wellbeing of the general public. 
The current gold standard for testing suspicious patients of SARSCoV-2(COVID-19) is through
 nasopharyngeal swabs and obtaining results for this test can often take 72 hours or more. 
 In a global pandemic, having a streamline screening and diagnosing system in place plays a 
 vital role of saving the lives of patients.  X-ray technology offer a non-invasive tool that 
 can be used to monitor the progression of the COVID-19 disease. In this project I propose COVID-Detect, 
 a classification model that uses Convolutional neural network to detect COVID-19 using X-RAY images. 
 The binary models were able to classify COVID-19 images with 99% accuracy, as well as use explainable 
 artificial intelligence technique for humans to better understand how the model achieved its results.  

 
## COVID-19  
COVID-19 comes from a large family of infectious viruses that causes illness varying from the common cold to more severe diseases such as 
Severe Acute Respiratory Syndrome (SARS-CoV). The main symptoms of COVID-19 are high body temperature, a new continuous cough and a loss or 
change to smell or taste. Most patients that are infected with the virus experience mild to moderate respiratory illness, and often recover 
without requiring special treatment. 

  
## Data Source
The dataset that we used to build COVID-Detect contained 2 folders train & test. 
Each folder contained 3 subfolders of (COVID19, PNEUMONIA, NORMAL) image. The dataset contained a total of 6432 x-ray images. 
70% of the total was used for training, 10% for validation and 20% for testing.  
The Data source can be found using the following link: https://tinyurl.com/y55wwznt 

## Convolutional Neural Network
Convolutional Neural Networks (CNN) are a very popular group of neural networks that belong to a wider set of techniques
 known as deep learning. CNN uses one or more Convolution layer and a many filtering layers to process complex pictures 
 compare to regular neural networks.  These are some of the reason that make them great for processing and classifying 
 medical chest images generated by Computer tomography (CT) and X-rays. In this project four different CNN architectures 
 were used to build over 8 different binary and categorical classification models. 
 
## Machine Learning (ML) - Steps taken
The following 6 steps were sued to build COVID-Detect. Using these following steps allows us to build models, 
ensure that our data is bias free, well-trained, finely tuned and thoroughly evaluated. Following this systematic 
process means that our models can be recreated by myself or other data scientific alike, using these 6 steps. 

1.	Identifying the problem
2.	Getting the Data
3.	Discovering and Visualizing the data
4.	Prepare the data for the CNN models
5.	Training models (with Parameter tuning)
6.	Results Evaluation 

## The CNN Layers & Pre-trained Models
All of our CNN model architectures, such as ResNet (2), DenseNet (3) used the pretrained weights of the Imagenet (4) dataset. 
Looking at the list on the right, you can see the final step that were taken to train the network. Freezing the initial weights 
of each chosen CNN architecture (step 2) meant that each model did not need to be retrained from scratch (this saves computational 
power and process such as RAM and GPU as well as time). Step 3 to 8 list the final additional steps and layers that were added on 
top of the frozen layers. Through research (5) we discovered that setting the dropout to 0.4 (40%) compared to the traditional 0.5 (50%),
was one of the main factors that contributed towards the high accuracy for the binary classification model. 

1.	Input
2.	Frozen CNN layers (Pre-trained)
3.	Average Pooling 2D
4.	Flatten
5.	Dense layer (128)
6.	Dropout (40%)
7.	Dense layer (64)
8.	Dropout (40%)
9.	Model output SoftMax

## Explainable AI using Grad-CAM Class Activation
![GitHub Logo](Masters_Disseration/images/image_1.png)




