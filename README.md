# Transfer-Learning-for-NLP-with-TensorFlow-Hub

Text Classification with Pre-trained Embeddings

This repository explores text classification using various pre-trained sentence encoders from TensorFlow Hub. The code trains and evaluates models on a binary classification task.

Getting Started

# Clone the repository:

git clone https://github.com/furkansepetci/Transfer-Learning-for-NLP-with-TensorFlow-Hub.git

# Run the script:

python train_and_evaluate.py


This script loads the data, trains models with different pre-trained embeddings, and visualizes the results.

# Pre-trained Models Used:

gnews-swivel-20dim/1: https://tfhub.dev/google/tf2-preview/gnews-swivel-20dim/1: A 20-dimensional embedding model trained on Google News.
nnlm-en-dim50/1: https://tfhub.dev/google/tf2-preview/nnlm-en-dim50/1 & nnlm-en-dim128/1: https://tfhub.dev/google/tf2-preview/nnlm-en-dim128/1: Neural net language models trained on English text with 50 and 128 dimensions, respectively.
universal-sentence-encoder/4: https://tfhub.dev/google/universal-sentence-encoder/4 & universal-sentence-encoder-large/5: https://tfhub.dev/google/universal-sentence-encoder-large/5: Contextual sentence encoders from Google with 512 and varying dimensions.

# Experiment Details:

The script trains two versions of the gnews-swivel model: one with the embedding layer frozen (trainable=False) and one fine-tuned (trainable=True).
All models use a simple architecture with a Dense layer for classification.
The script plots the accuracy and loss curves for each model during training.
TensorBoard logs are saved for visualization using tensorboard --logdir {logdir}.
