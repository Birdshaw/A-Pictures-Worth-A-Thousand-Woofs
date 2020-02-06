# A Pictures Worth a Thousand Woofs

> By: Haydin Bradshaw



## Description:

This project's goal is to build a machine learning model for canine facial expression classification. Have you ever wanted that perfect picture of your furry best friend but were too slow to capture it or your dog was too distracted to hold the pose for you? That is the inspiration behind this project. The endpoint of this project is to have a working classifier that can be implemented into either native mobile phone camera apps or Instagram. While the app's camera is running, the classifier will be working in the background continuously to focus on the canine subject, determine when it makes the expression you choose, and take photos automatically so you never miss that perfect moment. In the initial stage of this project I will be focusing on classifying when a dog is "smiling" i.e. when it is looking at the camera, mouth open and tongue out. 


## Dataset:

The datasets used in the project were the Stanford Dogs dataset and pictures taken from sites such as unsplash.com and freepik.com. The Standford Dogs dataset contains 20,580 images of 120 different breeds separated accordingly. Out of these I utilized 8 different breeds that had similar facial types. The breeds in question were Siberian Husky, Burmese Mountain Dog, Golden Retriever, Labrador Retriever, Brittany Spaniel, German Shepherd, Border Collie and Vizsla. From unsplash.com and freepik I choose dogs of the same breed that fit the "smiling" criteria. 

## EDA:

Exploratory data analysis for this project, though tedious, came down to viewing photos of dogs from the breeds listed and determining which were of best fit to the criteria mentioned above. Along with that they needed to be relatively centered and close up in the photograph. Opposing images were of various different forms of and iterations of dogs not "smiling". 

"Smiling" Dog Example      |  Non "smiling" Dog Example
:-------------------------:|:-------------------------:
![](/Data/retriever1.png)  |  ![](/Data/n02106662_10858.jpg)

## Pipeline:

Image files were of .jpg type. All were vectorized, turned to grayscal, and resized to be of uniform pixel density. Afterwards, multiple classifiers such as Random Forests, Stochastic Gadient Descent, Support Vector Machines, and Logistic Regression were used on the dataset to build a best model. 

## Models: 



