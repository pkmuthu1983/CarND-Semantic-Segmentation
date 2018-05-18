# Semantic Segmentation

##### Run
The model is implemented in main.py and the following command is used to run the project:
python main.py

[//]: # (Image References)
[image1]: ./sample1.png
[image2]: ./sample2.png
[image3]: ./sample3.png
[image4]: ./sample4.png
[image5]: ./sample5.png

### Discussion:
1. Layers module:
The model utilizes the layers 3, 4, and 7 from VGG and decodes/upsamples to match input dimensions.
The 1x1 convolutional layers and upsampling layers are initialized with random 
normal weights with zero mean and very low standard deviations. This resulted in low training loss
and faster learning. Furthermore, regularization is also done to prevent overfitting.  The output is 
layers.

2) Optimize module:
Adam optimizer is used to minimize the cross entropy between ground truth data and the features. 

3) Tain NN module:
Training was done in batches of size of 5 for about 50 epochs. Other choices like 10/50 also
produced similar results. However 2/50, did not provide good training loss.

4) Results:
The model passed all the unit tests. The training loss decreased on an average with each epoch.
The images below shows sample images from the run with batch size of 5 and 50 epochs.
As we can see, the model labels most of the pixels on the road correctly.

![Labeled image 1][image1]
![Labeled image 3][image3]
![Labeled image 5][image5]
