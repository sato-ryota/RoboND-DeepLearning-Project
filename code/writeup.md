## Project: Follow Me Project
---
### Writeup / README

#### 1. The write-up conveys the an understanding of the network architecture.
[//]: # (Image References)

[image1]: encoder_block.png
[image2]: decoder_block.png
[image3]: model_weights.PNG
[image4]: layers.png
Encoder Block use separable covolution layer. This block uses  smaller parameters than same size convolutions.


![alt text][image1]


Decoder block use bilinear_upsampling and concarenate the upsample and large input layers .

![alt text][image2]

My model includes 2 encoder_block and 2 decoder_block.
The model represent below.

![alt text][image3]


![alt text][image4]

#### 2. The write-up conveys the student's understanding of the parameters chosen for the the neural network.

I use the graph to decide the parameters.
train_loss and val_loss are both decreasing.
if I reduce number of epochs or increase learning rate , the model is overfit the data. training error decrease, but validation error increase.
I use batch to calculate efficient.
If batch size is big , I need to big memory.
batch_size: number of training samples/images that get propagated through the network in a single pass. now we use 128 images.
num_epochs: the number of epochs to train for. number of times the entire training dataset gets propagated through the network.
Using bigger num_epochs improve accuracy. but we need to be attention to overfit.
steps_per_epoch: the number of batches per epoch. this number decide to update the gradient.
workers: maximum number of processes to spin up. This can affect the training speed and is dependent on the hardware.



#### 3. The student has a clear understanding and is able to identify the use of various techniques and concepts in network layers indicated by the write-up.

1 by 1 convolutions use  after encoder layers. I use 1 by 1 convolutions to reduce dimension.
they're just matrix multiplies and they have relatively few parameters. this is a very inexpensive  way to make the models deeper and have more parameters.
this model is
fully connected layer use after decode block. this layer  use final part of network.

#### 4. The student has a clear understanding of image manipulation in the context of the project indicated by the write-up.

I use encoder to classify the pixel.
Encoder layers are compress the data and lost the several data. Encoder layers obtain the features. the features is more abstract the layers is deeper.

Decoder layers changes the abstract features to the pictures.
Using upsampling method gives us the higher dimensions.
to use this method lose some details.
The concatenation connection reflect the features that are lost in encoder block.

#### 5.The student is able to clearly articulate whether this model and data would work well for following another object (dog, cat, car, etc.) instead of a human and if not, what changes would be required.

this model and data doesn't work well . we need to add the data of another objects.

#### 6. future enhancement

I represent the method to improve accuracy and model.

1. adding the data
adding the data is helpful to place without any bias.
2. improve the data
for example , if object is too small, the features are not clear in the image.
Model mistake the noise  for the features.
3. changing the activation function
There are several activation function. some function can learning. this will improve the accuracy.
