# data_scientist_dog_breed_classifier

## Blog 
[Dog Breed Identification](https://moonlight43.home.blog/dog-breed-identification/)

## Table of Contents

  1. [Project Overview](##Project Overview)
  2. [Installation](##Installation)
  3. [File Descriptions](##File Descriptuons)
  4. [Conclusions](##Conclusions)

## Project Overview
This is a Udacity Data Scientist Nanodegree project. In this project, we will select the existed classifier to detect human and dog images. Based on that we will build and train a Convolutional Neural Network (CNN) to identify the dog breed of the uploaded images (if the updated image has been detected as a dog, we will give the dog breed as the response; if it has been detected as a human, the response would be a resembling bog breed.) Finally, we will use transfer learning to improve the model accuracy.

## Installation

Beyond the Anaconda distribution of Python, the following packages need to be installed:

  * opencv-python==3.2.0.6
  * h5py==2.6.0
  * matplotlib==2.0.0
  * numpy==1.12.0
  * scipy==0.18.1
  * tqdm==4.11.2
  * scikit-learn==0.18.1
  * keras==2.0.2
  * tensorflow==1.0.0

## File Descriptuons
  1. bottleneck_features
    * Pre-trained features for VGG-16 and VGG-19, since the size is very big, we ignored here.
  2. haarcascades
    * A pre-trained human face detector which is provided by OpenCV.
  3. images
    * All the test images.
  4. saved_models
    * saved model for different CNNs with the best validation loss.
  5. dog_app.html
    * The html format for the notebook to build and train the dog app project.
  6. dog_app.ipynb
    * The notebook to build and train the dog app project.

## Conclusions
By using the transfer learning, we could take advantage of the already trained model and make improvements based on that. It saves the future developer a lot of model research and training time.

Overall, the result is better than I expected. The categories (dog, human, and others) classification are all correct. For the animal fox, even it looks like a dog, the model still made a correct prediction. In the human_spaniel photo, there is a dog logo in the human’s cotta, but the model still got the right answer. For the breed prediction, all the dogs are correct. For human breed, I am also satisfied with the result since the we don’t have the absolutely correct answer.

For the categories classification and dog breed prediction, we could train the model offline periodically by using new data from different data sources. For the human breed prediction, we could show the several top resembling breeds (n)to users and users to give some feedback, by using the feedback, we could keep training the model.
