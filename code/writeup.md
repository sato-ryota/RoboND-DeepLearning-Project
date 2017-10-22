## Project: Perception Pick & Place
### Writeup Template: You can use this file as a template for your writeup if you want to submit it as a markdown file, but feel free to use some other method and submit a pdf if you prefer.

---
### Writeup / README

#### 1. Provide a Writeup / README that includes all the rubric points and how you addressed each one.  You can submit your writeup as markdown or pdf.
You're reading it!

### Exercise 1, 2 and 3 pipeline implemented
#### 1. Complete Exercise 1 steps. Pipeline for filtering and RANSAC plane fitting implemented.


[//]: # (Image References)

[image1]: ./misc_images/objects.png
[image2]: ./misc_images/segmentation.png
[image3]: ./misc_images/train_svm.png
[image4]: ./misc_images/object_recognition.png
[image5]: ./misc_images/test1.png
[image6]: ./misc_images/test2.png
[image7]: ./misc_images/test3.png


I modify RANSAC.py.
I attach the file.

![alt text][image1]


#### 2. Complete Exercise 2 steps: Pipeline including clustering for segmentation implemented.  

I copy template.py. and I call new fie segmentation.py.
I segmentate the 6 objects.

![alt text][image2]

#### 2. Complete Exercise 3 Steps.  Features extracted and SVM trained.  Object recognition implemented.

To get better features, open up the featrues.py

I change the 3 point.

1. histogram: I use color and normal.
2. orientation: I use 5 orientation to train the object.
3. color:I use HSV.

I inprove the accuracy .(0.3 to 0.9 )
![alt text][image3]

![alt text][image4]


### Pick and Place Setup

#### 1. For all three tabletop setups (`test*.world`), perform object recognition, then read in respective pick list (`pick_list_*.yaml`). Next construct the messages that would comprise a valid `PickPlace` request output them to `.yaml` format.

test1.world
![alt text][image5]

test2.world
![alt text][image6]

test3.world
![alt text][image7]




Spend some time at the end to discuss your code, what techniques you used, what worked and why, where the implementation might fail and how you might improve it if you were going to pursue this project further.  

I train the objects more times and need to fit the features.
