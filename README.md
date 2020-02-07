# A Pictures Worth a Thousand Woofs
<p align="center">
  <img src=Data/4349564710_ee40075f95_o.jpg>
</p>

> By: Haydin Bradshaw



## Description:

This project's goal is to build a machine learning model for canine facial expression classification. Have you ever wanted that perfect picture of your furry best friend but were too slow to capture it or your dog was too distracted to hold the pose for you? That is the inspiration behind this project. The endpoint of this project is to have a working classifier that can be implemented into either native mobile phone camera apps or Instagram. While the app's camera is running, the classifier will be working in the background continuously to focus on the canine subject, determine when it makes the expression you choose, and take photos automatically so you never miss that perfect moment. In the initial stage of this project I will be focusing on classifying when a dog is "smiling" i.e. when it is looking at the camera, mouth open and tongue out. 


## Dataset:

The datasets used in the project were the Stanford Dogs dataset and pictures taken from sites such as unsplash.com and freepik.com. The Standford Dogs dataset contains 20,580 images of 120 different breeds separated accordingly. Out of these I utilized 8 different breeds that had similar facial types. The breeds in question were Siberian Husky, Burmese Mountain Dog, Golden Retriever, Labrador Retriever, Brittany Spaniel, German Shepherd, Border Collie and Vizsla. From unsplash.com and freepik I choose dogs of the same breed that fit the "smiling" criteria. 

## EDA:

Exploratory data analysis for this project, though tedious, came down to viewing photos of dogs from the breeds listed and determining which were of best fit to the criteria mentioned above. Along with that they needed to be relatively centered and close up in the photograph. Opposing images were of various different forms of and iterations of dogs not "smiling". 


"Smiling" & Facing Camera      |  Not "smiling" nor Facing Camera
:-------------------------:|:-------------------------:
![](/Data/zachary-casler-XLZxKsjhdPU-unsplash.jpg)  |  ![](/Data/christopher-stark-ilYiCxBf-m0-unsplash.jpg)

## Pipeline:

Image files were of .jpg type. All were vectorized, turned to grayscal, and resized to be of uniform pixel density. Afterwards, multiple classifiers such as Random Forests, Stochastic Gradient Descent, Support Vector Machines, and Logistic Regression were used on the dataset to build a best model. 

## Models: 

As mentioned before the models used were **Random Forests**, **Stochastic Gradient Descent**, **Support Vector Machines**, **Logistic Regression**, and a **Convolutional Neural Network**.

---

Comparing all but CNN, Random Forest Classifier performed the best as can be seen by the ROC curve below:

<p align="center">
  <img width='700' height='700' src=Data/roc_curve.png>
</p>

We can also look deeper into their individual metrics through their confustion matrices, accuracy, precision and recall values:

Metric | Random Forest | Stochastic Gradient Descent | Support Vector Machine | Linear Regression
:----------------:|:------------:|:------------:|:-----------:|:------------------:
Confustion Matrix |![](/Data/rf_mat.png)  |  ![](/Data/sgd_mat.png) | ![](/Data/svm_mat.png) | ![](/Data/lr_mat.png)
Accuracy          | 0.64         |   0.56       |   0.52      |   0.54
Recall            | 0.84         |   0.65       |   0.66      |   0.70 
Precision         | 0.58         |   0.59       |   0.64      |   0.64

<p align="center">
  <img width='700' height='700' src=Data/prec_rec.png>
</p>

---

PCA was utilized and optimal number of components were found, however all attempts to model using PCA transformed data were inferior to above metrics.

<p align="center">
  <img width='700' height='700' src=Data/better_pca.png>
</p>

<p align="center">
  <img width='700' height='700' src=Data/dog_face_comp.png>
</p>

---

Lastly, a Convolutional Neural Network was trained on the built dog dataset. Ending results were superior to all other models, though they had yet to level out. With additional epochs or data a leveled accuracy might be found.

<p align="center">
  <img width='700' height='700' src=Data/cnn_acc.png>
</p>

---

## Conclusion:

As we could have guess, convolutional neural networks have the possibility to perform the best. For classical classifiers random forests provide us with the best accuracy and recall which is what is most desired for this application. For future works I will continue work implemting a neural network for classification, expand the dataset of smiling dogs for improved classification, and expand the facial expressions this model can classify.  
