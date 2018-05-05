# Classify-Image-Using-Keras-And-CNN
In this model we use smallervggnet model and 3 category from images. The Images are Ballpoint, Eraser, and Ruler images. 
We get the data using crawling image in google image search using python, you can see in my blog [how to crawling image](https://thinkstudioo.blogspot.co.id/2018/03/crawling-images-in-google-images.html).
After we have the data, we cleaning the data and choosing image with just object in image.  
we have 179 ballpoint images, 132 ruler images, and 142 eraser images with resolution 100x100.

structure :

* Clasify images
  * classify.py
  * train.py
  * alattulis3.model
  * lb3.pickle
  * Model
    * smallervggnet.py
  * examples
    * images for testing
  * dataset
    * ballpoint
    * eraser
    * ruler

### There are 3 directories:
* dataset : Contains the three classes, each class is its own respective subdirectory to make parsing class labels easy.
* examples : Contains images we’ll be using to test our CNN.
* The model  module: Contains our SmallerVGGNet  model class.

### And 5 files in the root:
* plot.png : Our training/testing accuracy and loss plot which is generated after the training script is ran.
* lb3.pickle : Our LabelBinarizer  serialized object file — this contains a class index to class name lookup mechamisn.
* alattulis3.model : This is our serialized Keras Convolutional Neural Network model file (i.e., the “weights file”).
* train.py : We will use this script to train our Keras CNN, plot the accuracy/loss, and then serialize the CNN and label binarizer to disk.
* classify.py : Our testing script.

### Dependencies
* Keras
* Imutils
* cv2
* Numpy
                  
### How to Run
* python train.py --dataset dataset --model alattulis3.model --labelbin lb3.pickle

* python classify.py --model alattulis3.model --labelbin lb3.pickle --image examples/ballpoint.jpg
