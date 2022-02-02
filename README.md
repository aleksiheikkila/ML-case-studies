### Machine learning case studies

#### Repo structure

Each case study / experiment / project in separate folder. Case studies:

 - [**Human activity recognition (HAR)**](human_activity_recognition)
 
    Using smartphone accelerometer and gyroscope time series data to classify what activity was being performed. LSTM-based solution with minimal feature engineering.

 - [**Computer vision image classification to separate elephants from rhinos**](CV_classify_elephants_vs_rhinos)
 - A toy example of [**market basket analysis**](market_basket_analysis)
 - [**RNN language model for Finnish**](finnish_lang_model)

    Downloaded 44 Juhani Aho books from Project Gutenberg and trained a character-level RNN model to predict the next character (one character at a time) from the input sequences. Used to generate some Juhani Aho-esque texts.

 - [**Retinal OCT image classification**](CV_retinal_OCT_classification)
 - [**Colorectal histology image classification**](CV_colorectal_histology_classification)
 - [**Dogs vs. cats image classification**](CV_dogs_vs_cats_redux).

    Used pretrained EfficientNet-b7 model to extract features from the images, then applied simple LogisticRegression to classify them. PyTorch.
