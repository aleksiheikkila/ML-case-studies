### RNN language model for Finnish

This experiment consists of the following steps:
 - Collect moderately-sized (at least some tens of books worth of) Finnish text corpus from Project Gutenberg. I ended up using 44 books from Juhani Aho (all that were available except plays and audiobooks), a total of roughly 16.5 million characters and something like ~16 MB of text data.
 - Train a RNN-based architecture on that data, on character level (using sequence of chars to predict the next char)
 - Use the trained model to generate some Finnish text, given a context / cue string.

This was done on Google Colab, where the model has been trained on multiple separate sessions (maybe for several hours in total in GPU-accelerated runtime, for maybe 20 epochs or so). The model checkpoints were stored in Google Drive and restored from there.

Check the notebook for further details.

At this points, the model has figured out the structure and spelling quite okay, but it has still some work to do for capturing something meaningful a bit more consistently :)
