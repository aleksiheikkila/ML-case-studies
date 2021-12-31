# Colorectal Histology Image Classification

Using deep learning to classify colorectal histology images.

Multiclass image classification problem using colorectal histology images.

## Data
Sourced from Kaggle: https://www.kaggle.com/kmader/colorectal-histology-mnist

This data set represents a collection of textures in histological images of human colorectal cancer. It contains two files:

* "Kather_texture_2016_image_tiles_5000.zip": a zipped folder containing 5000 histological images of 150 * 150 px each (74 * 74 µm). Each image belongs to exactly one of eight tissue categories (specified by the folder name).
* "Kather_texture_2016_larger_images_10.zip": a zipped folder containing 10 larger histological images of 5000 x 5000 px each. These images contain more than one tissue type.

All images are RGB, 0.495 µm per pixel, digitized with an Aperio ScanScope (Aperio/Leica biosystems), magnification 20x.


## Setup

Run on Google Colab. The beginning of the notebook contains some Colab specific setup stuff such as integrating with Google Drive (primarily to persistenty store the trained models)

Data was sourced from Kaggle: https://www.kaggle.com/kmader/colorectal-histology-mnist. This was done thru the Kaggle Api (API credentials needed). The compressed size of the data is something around 1 GB.

For the deep learning I used fastai v1 CNN with pretrained (imagenet) resnet50 architecture.
