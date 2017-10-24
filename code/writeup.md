## Project: Follow Me Project
---
### Writeup / README

#### 1. The write-up conveys the an understanding of the network architecture.
[//]: # (Image References)

[image1]: encoder_block.png
[image2]: decoder_block.png

Encoder Block use separable covolution layer. This block uses  smaller parameters than same size convolutions.

![alt text][image1]


Decoder block use bilinear_upsampling and concarenate the upsample and large input layers .

![alt text][image2]

My model includes 2 encoder_block and 2 decoder_block.

#### 2. The write-up conveys the student's understanding of the parameters chosen for the the neural network.

I use the graph to decide the parameters.
train_loss and val_loss are both decreasing.
if I reduce number of epochs or increase learning rate , learing is delay and accuracy is bad.
I use batch to calculate efficient.
If batch size is big , I need to big memory.

#### 3. The student has a clear understanding and is able to identify the use of various techniques and concepts in network layers indicated by the write-up.

1 by 1 convolutions use  after encoder layers. I use 1 by 1 convolutions to reduce dimension

fully connected layer use after decode block. this layer  use final part of network.

#### 4. The student has a clear understanding of image manipulation in the context of the project indicated by the write-up.

I use encoder to classify the pixel. and I use decoder layer to
Encoder layers are compress the data and lost the several data.
Decoder layers chage the abstract features to the pictures.

#### 5.The student is able to clearly articulate whether this model and data would work well for following another object (dog, cat, car, etc.) instead of a human and if not, what changes would be required.

this model and data doesn't work well . we need to add the data of another objects.

#### 6. future enhancement

I represent the method to improve accuracy and model.

1. adding the data
2. improve the data
3. changing the activation function
