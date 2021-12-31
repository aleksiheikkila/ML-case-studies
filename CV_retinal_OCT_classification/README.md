# Retinal_OCT_Image_Classification
Classifying Retinal optical coherence tomography (OCT) images. The implementation that is referred to is in the accompanying Colab notebook. 

However, it does not seem to always render on github. Check it with e.g. nbviewer at https://nbviewer.jupyter.org/github/aleksiheikkila/Retinal_OCT_Image_Classification/blob/master/Retinal_OCT_image_classification.ipynb


## Background

Retinal optical coherence tomography (OCT) is an imaging technique used to capture high-resolution cross sections of the retinas of living patients. Approximately 30 million OCT scans are performed each year, and the analysis and interpretation of these images takes up a significant amount of time (Swanson and Fujimoto, 2017).

Here are examples of the four classes/labels we have images of:

![Image of the different classes](https://i.imgur.com/fSTeZMd.png)

(A) (Far left) choroidal neovascularization (CNV) with neovascular membrane (white arrowheads) and associated subretinal fluid (arrows). (Middle left) Diabetic macular edema (DME) with retinal-thickening-associated intraretinal fluid (arrows). (Middle right) Multiple drusen (arrowheads) present in early AMD. (Far right) Normal retina with preserved foveal contour and absence of any retinal fluid/edema.

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (NORMAL,CNV,DME,DRUSEN). There are 84,495 X-Ray images (JPEG) and 4 categories (NORMAL,CNV,DME,DRUSEN).

### Citation:
![Citation](https://i.imgur.com/8AUJkin.png)


## Setup

Run on Google Colab. The beginning of the notebook contains some Colab specific setup stuff such as integrating with Google Drive (primarily to persistenty store the trained models)

Data was sourced from Kaggle: https://www.kaggle.com/paultimothymooney/kermany2018. This was done thru the Kaggle Api (API credentials needed). The compressed size of the data is something around 5.5 GB.

For the deep learning I used fastai v1 CNN with pretrained (imagenet) resnet50 architecture.
