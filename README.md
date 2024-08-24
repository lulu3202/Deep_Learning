# Deep_Learning

## General Notes on Deep Learning 
Numbers works well for ML, images work best for DL. DL is supervised learning. 
There are 3 types of images
	○  Black and white - B is 0 and white is 1
	○ (CV) Grey scale - 0 (black) to 255 (white) - PURE NUMBER CONVERSION  between 0 and 255
	○ (DL) Color image - R (0 is darkest red to 255 lightest red) +  G (0 to 255) + Blue(0 to 255)  

# Introduction of Face Mask Detection Project 
 This is a model to detect whether or not people are wearing masks. We will leverage Keras and Computer Vision algorithm. We will also use transfer learning from Facenet and MobileVnet V2. 

## Dataset
- Data collection is of 2 types: manual labelling  and folder dataset (where you have only the object of interest). We will be using folder dataset. 

##Application flow:
Camera -> takes photo (with background) -> create pretrained model that will crop out only the face (similar to how brain will process it) -> only cropped face image  is  fed It to model -> model predicts whether there is mask or not -> respective CTA 

## Model Creation/Learning
- Data Collection (masked pics and unmasked pics)
- Data Preprocessing (cropping only the face using pretrained model called facenet)
-Split input and output (convert image into numbers and matrix format leveraging mobileVnetv2)
-Train model
-Test model
-Save the best model as .h5 file


