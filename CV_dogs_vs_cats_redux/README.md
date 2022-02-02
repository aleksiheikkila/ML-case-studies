## Dogs vs. Cats classification

This was just to check how good results one can get these days by simply getting a large pretrained modern network, generating features with it and then using these as input for a simple classifier.

I used large EfficientNet-b7 pretrained model, extracted features and used logistic regression on these for the binary classification. This resulted in top-10 score without too many tricks (obviously the competition is an old one, and the leaderboard is from that time, so to some extent this was to be expected and the comparison is a bit silly... the point is just how much the DNN methodology has advanced during the past several years)

### Data

The train folder contains 25,000 images of dogs and cats. Each image in this folder has the label as part of the filename. The test folder contains 12,500 images, named according to a numeric id. For each image in the test set, you should predict a probability that the image is a dog (1 = dog, 0 = cat).

### Evaluation

Submissions are scored on the log loss.

So, if a model is very confident but wrong, it will get penalized a lot. So maybe better not be extremely confident with preds (clip the probabilities?)

### Outline

Create Datasets and DataLoaders. Use pretrained EfficientNet-b7 model to extract features (vector of length 2560, kind of embedding for the image) from the penultimate layer of the pretrained EffNet model.

Train a simple classifier using these embeddings as input.

Perhaps finetune the pretrained model a bit.