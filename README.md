# Transfer_Learning_Stanford_Dog_Breed_Classifier
Classifier that takes images of dogs and classifies the breed from 120 labels.  Used Xception pre-trained CNN for transfer learning.

## Motivation
This project was completed for a Machine Learning class at the George Washington University.  I was tasked with creating an image classifier to classify dog breeds with a minimum of 85% accuracy on the Stanford Dog Breeds test dataset.  This is my first project using CNNs and transfer learning.  I used a GPU through Google Colab for training the model.

## Data Source
https://www.tensorflow.org/datasets/catalog/stanford_dogs

## The Notebook
I used this notebook to do the entire project.  Within it, I download the data via the tensorflow_datasets package.  After downloading, the data is split and preprocessed.  I removed the top layer from Xception (pre-trained on ImageNet data) and added an average pooling and a dense final layer with softmax activation.  I froze the Xception layers and trained the model using the Adam optimizer and a learning rate of .01.  I then unfroze the Xception layers and re-trained the model with a .0001 learning rate.  I achieved an accuracy of 89.64% on the test dataset.  At the bottom of the notebook, I pulled dog images from Google and the model classified the unseen images correctly.

## Other files
The images are from Google Images and are used to test the model on a few instances it did not see during training/test.  There is no dataset in the repository because it can be acquired by running the cells in the notebook.

