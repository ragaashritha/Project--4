#  Architectural Basics
**1.How many layers:**
	- Number of layers is based on the size of the object. 
	- We keep adding layers until receptive field equals size of the object 

**2. Max Pooling:**
	- MaxPooling is a technique where the maximum pixel value in the block is choosen because max pixel value has more information about the image
	- Max pooling is done after a convolution block i.e., after finding edges/gradients and textures/patterns and parts of object
	- Receptive field doubles after each maxpooling layer
 
**3. 1x1 Convolutions:**
	- 1x1 convolution summarises the pixel values of all the channels
	- Used to reduce number of channels 

**4. 3x3 Convolutions:**
	- 3x3 convolution calculates the weighted average of the 3x3 pixels of the image
 
** 5.Receptive Field:**
	- Receptive field is the number of pixels each kernel is looking at
	- Towards the end of the convolution layers, we are expected to look at the entire image i.e., our receptive field has to be equal to size of the object

** 6.SoftMax:**
    - Softmax is the activation function which is used in classification models to give percentage attribution to each class in between 0 and 1

**7.Learning Rate:**
    - Learning rate is the rate at which the weights descent in the optimization function 
    - Optimal learning rate is expected to be high in the beginning and slowly decrease in value as we reach minima of the optimization function

** 8.Kernels and how do we decide the number of kernels:**
	- Kernels are the blocks which move over the image and calculate the weighted average of the image pixels.
	- We decide number of kernels based on the number of features of th image we are looking to extract

**9.Batch Normalization:**
	- Batch normalization is normalizing the values of entire batch size which is considered i.e, subtracting the pixels of the bacth with batch mean and dividing by its standard deviation
	- We do batch normalization in order to put the pixel values in between -1 aand 1 thus minimising the variance

**10.Image Normalization:**
    - Image normalization is normalizing the pixel values of the image i.e, subtracting the pixels of the image with image mean and dividing by its standard deviation
	- We do image normalization in order to put the pixel values in between -1 aand 1 thus minimising the variance

**11. Position of MaxPooling:**
    - In general Max pooling is done as a trasition block after a convolution block where the features like edges/gradients,textures, patterns, parts of objects are identified and needs to be summarized 

**12. Concept of Transition Layers:**
    - Transition layers summarise the pixel information/ reduce number of channels
    - They are put after each convolution block once the concolution block identifies each of the following;
    		1. Edges and gradients
    		2. Textures
    		3. Patterns
    		4. Parts of objects
    - Maxpooling, 1x1 convolutions come under transition layer	
**13. Position of Transition Layer:**
	- Transition layer is put after each convolution block once the concolution block identifies each of the following:
    		1. Edges and gradients
    		2. Textures
    		3. Patterns
    		4. Parts of objects
**14.Number of Epochs and when to increase them:**
    - Epoch is when loss function sees the entire training data
    - Epochs are increased when the loss can decrease further and not stagnated at a point 

**15.DropOut:**
	- Dropout is making neurons dead in order to not let model overfit by learning too intricate features 

**16.When do we introduce DropOut, or when do we know we have some overfitting:**
    - We intoduce dropout when we get to know that our model is overfitting
    - We can say that model is overfitting when there is huge difference between train and test accuracies

**17.The distance of MaxPooling from Prediction:**
    - Maxpooling has to be atleast two layers before the prediction layer

**18. The distance of Batch Normalization from Prediction:*
    - Batch Normalization has to be atleast two layers before the prediction layer

**19. When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered):**
    - 
How do we know our network is not going well, comparatively, very early
Batch Size, and effects of batch size
When to add validation checks
LR schedule and concept behind it
Adam vs SGD
