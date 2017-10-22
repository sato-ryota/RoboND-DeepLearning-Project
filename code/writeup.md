## Project: Follow Me Project
---
### Writeup / README

#### 1. The write-up conveys the an understanding of the network architecture.

Encoder Block use separable covolution layer. This block uses  smaller parameters than same size convolutions.

Decoder block use bilinear_upsampling and concarenate the upsample and large input layers .

#### 2. The write-up conveys the student's understanding of the parameters chosen for the the neural network.

I use the graph to decide the parameters.
train_loss and val_loss are both decreasing.

#### 3. The student has a clear understanding and is able to identify the use of various techniques and concepts in network layers indicated by the write-up.

1 by 1 convolutions use  after encoder layers.

fully connected layer use after decode block. this layer  use final part of network.

#### 4. The student has a clear understanding of image manipulation in the context of the project indicated by the write-up.

I use encoder to classify the pixel. and I use decoder layer to
Encoder layers are compress the data and lost the several data.
Decoder layers chage the abstract features to the pictures.

#### 5.The student displays a solid understanding of the limitations to the neural network with the given data chosen for various follow-me scenarios which are conveyed in the write-up.

this model and data doesn't work well . we need to add the data of another objects.
