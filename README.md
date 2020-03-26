# covid19-detection
The Project aims to scan patients to predict COVID-19 from chest X-Ray/CT using Deep Learning. The model currently has 98% accuracy. The python notebook document(ipynb) contains the code for training and testing.

# Goal
The tasks are as follows using chest X-ray or CT (preference for X-ray) as input to predict these tasks:
1- Healthy vs Pneumonia (prototype already implemented Chester with ~74% AUC, validation study here)
2- Bacterial vs Viral vs COVID-19 Pneumonia
3- Survival of patient

# Dataset
Currently this git repo is maintaining the COVID-19 Xray dataset:
https://github.com/ieee8023/covid-chestxray-dataset


# Model Statistics and Accuracy
VGG16 model was utilized as base model, the layers were freezed and on top of it some more layers were added. The model was trained on 370 samples of data and tested on 36 samples. The testing accuracy currently reported is 95%.

![ROC curve of model](https://github.com/hananshafi/covid19-detection/blob/master/covid-roc.png)
![Confusion matrix](https://github.com/hananshafi/covid19-detection/blob/master/cmatrix.JPG)

Confusion Matrix (accuracy 98%, sensitiviy 93% and specificity 100%)

Correct Healthy Patient Detection (True Negatives): 13
Incorrect Covid-19 Detection (False Positives): 1
Incorrect Healthy Patient Detection (False Negatives): 0
Correct Covid-19 Detection (True Positives): 28
Total Patietns Diagnosed with Covid-19: 28


# Here is the the result of model on one of the samples:
![Initial Result](https://github.com/hananshafi/covid19-detection/blob/master/covid-xray-umap.png)
![X-Ray of COVID-19 Positive patient](https://github.com/hananshafi/covid19-detection/blob/master/covid-19.JPG)
