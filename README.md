# Distracted-Driver
Kaggle State Farm Distracted Driver Detection

I found that image processing was very important in 
Kaggle State Farm Distracted Driver Detection

The Kaggle State Farm Distracted Driver dataset was obtained from here: https://www.kaggle.com/c/state-farm-distracted-driver-detection

The dataset was split into 17939 test samples and 4485 validation samples corresponding to a 80:20 split.  The data set predicts 10 classes of a distracted driver:

c0: safe driving
c1: texting - right
c2: talking on the phone - right
c3: texting - left
c4: talking on the phone - left
c5: operating the radio
c6: drinking
c7: reaching behind
c8: hair and makeup
c9: talking to passenger

First, a CNN was built consisting of 2 convolutional layers with a filter size of 3x3, followed by a max-pooling layer with pool size of 2x2, and 2 fully-connected dense layers. This CNN model was used to compare image processing methods of Laplacian transformation, canny, random rotation, image resizing. The best image processing on the CNN was the Canny function shown in file Simple_CNN

Next using the Canny image processing function was used to compare the previous CNN model to a functional API model. the functional API model is in file Functional_API.

Memory constraints and running costs kept the CNN and functional API model shallow.  More computing power would allow for deeper models and a better classifier.
