# Classify-Image-Using-Keras-And-CNN
In this model we use smallervggnet model and 3 category from image. The Images are Ballpoint, Eraser, and Ruler images. 

### There are 3 directories:
dataset : Contains the three classes, each class is its own respective subdirectory to make parsing class labels easy.
examples : Contains images we’ll be using to test our CNN.
The model  module: Contains our SmallerVGGNet  model class.

### And 5 files in the root:
plot.png : Our training/testing accuracy and loss plot which is generated after the training script is ran.
lb3.pickle : Our LabelBinarizer  serialized object file — this contains a class index to class name lookup mechamisn.
alattulis3.model : This is our serialized Keras Convolutional Neural Network model file (i.e., the “weights file”).
train.py : We will use this script to train our Keras CNN, plot the accuracy/loss, and then serialize the CNN and label binarizer to disk.
classify.py : Our testing script.

### Dependencies
* Keras
* Imutils
* cv2
* Numpy
                  
### How to Run
* Training
python train.py --dataset dataset --model alattulis3.model --labelbin lb3.pickle

* Classify
python classify.py --model alattulis3.model --labelbin lb3.pickle --image examples/ballpoint.jpg
