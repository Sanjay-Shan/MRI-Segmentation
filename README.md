# MRI-Segmentation
Simple Image segmentation using Fully connected neural network and Conv Net. 

The hierarchy of this project goes as follows
1. Preparation of the dataset using tensorflow records
2. Building the tensorflow keras network using various built-in network components
3. Setting the parameters for training
4. Training the model for set number of epochs
5. Evaluation of the trained network

This project was accomplished as a part of Nvidia's DLI course on Image Segmentation. This project was initially a part of Kaggle's competition where in the actual task was to predict the volume of left ventricle of the heart during the systole and distole. But here we will be focusing majorly on the image segmentation part.

# Dataset
As a part of the DLI course , the data was handed over to me in the form of the TFRecord , where in the DICOM format MRI scans were processed and were finally stored as TFRecords.
Training Images:234
Validation Images:26

I definetly have plans to cover the data prepartion part as it forms a import part of the machine learning pipeline. And maybe if time permits I'll extend the image segmentation to the ventricle volume prediction task.

Images after processing looks something like this:  
<kbd>![Sample image1](Data/example1.png)</kbd>
<kbd>![Sample image2](Data/example2.png)</kbd>

# Networks
As mentioned in the initial part , I have 2 networks namely a simple neural network and a Convolutional network which resembles the same as shown below  
<kbd>![NeuralNet](Data/NeuralNet.png)</kbd>
<kbd>![ConvNet](Data/ConvNet.png)</kbd>

# Results
The validation process in the code implementation provided shows the results obtained after inferencing the model on the validation data  

# Dice metric loss
As shown in the training dataset , there is a huge imbalance in the classes. Hence the normal accuracy of matching correct pixels in the prediction to ground truth does'nt really give us a proper estimate of the model hence another metric namely Dice metric is introduced which is very similar to that of the IOU used in Non max suppression.

# Future works
I'll soon be adding another implementation of CNN i.e. a popular segmentation architecture namely U-Net along with the data preparation part.Untill then stay tuned...    
