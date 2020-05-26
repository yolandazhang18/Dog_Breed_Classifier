
# DSND Capstone Project (Dog Breed Classifier)

## 1. Project overview

The main focus of project is to build a dog breed classification algorithm using Convolutional Nerual Networks to detect a dog or human in a user provided image and return the following results:

* The **predicted dog breed** if a dog is detected in the image.
* The **resembling dog breed** if a human is detected in the image.
* **Report an error** if neither is detected in the image.

## 2. Software packages

python (v3.6.3)<br>
glob<br>
random<br>
numpy (v1.12.1)<br>
pandas (v2.23.3)<br>
matplotlib (v2.1.0)<br>
sklearn (v0.19.1)<br>
keras (v2.0.9)<br>
cv2 (v3.3.1)<br>
tqdm (v4.11.2)<br>
PIL (v5.2.0)<br>

## 3. Files

The files included in this project are:

* `dog_app.ipynb`: The Jupyter notebook with all code used in this project


* `images` folder: Example images used in the dog_app.ipynb


* `new_images` folder: User provided images downloaded from the internet for model assessment


* `extract_bottleneck_features.py`: The function to extract the bottleneck features


* `haarcascades` folder: The Haar feature-based cascade classifier for face detection using OpenCV's implementation


* `bottleneck_features` folder: Bottleneck features from pre-trained model (CURRENTLY UNAVAILABLE DUE TO LARGE FILE SIZE)


* `saved_models`: All trained models generated in dog_app.ipynb


*  `README.md`

## 4. Project workflow

### **Step 0: Import Datasets:**
Import dog images and create:
* Numpy arrays containing file paths to train, validation and test images
* Numpy arrays containing onehot-encoded classification labels for training, validation and test 
* A list of string-valued dog breed names for translating labels, `dog_names`

Import human images and create: <br>
A Numpy array of human image file paths, `human_files`

### **Step 1: Detect Human**
Create and assess a human face detector to detect human faces in images using OpenCV's implementation of Haar feature-based cascade classifiers. One of these detectors have been downloaded and stored in the haarcascades directory.

### **Step 2: Detect Dogs** 
* Pre-process the dog images and use a pre-trained ResNet-50 model to detect dogs in the images. 
* Create and assess the dog detector.


### **Step 3: Create a CNN to Classify Dog Breeds (from Scratch)**
* Pre-process the dog images
* Build a multi-layer CNN model architecture
* Compile and train the built model
* Load model with best validation loss 
* Test the model accuracy (Test accuracy should be greater than 1%)

### **Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)**
* Obtain Bottleneck Features
* Build model architecture using a pre-trained ResNet-50 model
* Compile and train the transfer learning model
* Load model with best validation loss 
* Test the model accuracy (Test accuracy should be greater than 60%)

### **Step 5: Write Your Algorithm**
Combine the pre-defined face and dog detector functions with the ResNet-50 based prediction model

### **Step 6: Test Your Algorithm**
Test the algorithm with various types of user provided images and output the predicted dog breed, resembling dog breed or an error.

## 5. Medium post
There is an [article](https://medium.com/@yolanda091107/image-classifier-101-a-dog-breed-example-cd96a1038a52) about this project.
