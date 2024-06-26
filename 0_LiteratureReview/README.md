# Literature Review

Approaches or solutions that have been tried before on similar projects.

**Summary of Each Work**:

- **Source 1**: Tensorflow / Image Segmentation

  - **[Reference](https://www.tensorflow.org/tutorials/images/segmentation)**

- **Source 2**: U-net

  - **[Reference](https://en.wikipedia.org/wiki/U-Net)**

  This is the model architecture we are using. 
  Excerpt:
  U-Net is a convolutional neural network that was developed for biomedical image segmentation at the Computer Science Department of the University of Freiburg. The network is based on a fully convolutional neural network whose architecture was modified and extended to work with fewer training images and to yield more precise segmentation. Segmentation of a 512 × 512 image takes less than a second on a modern (2015) GPU using the U-Net architecture.

- **Source 3**: Model Source

  - **[Reference](https://medium.com/analytics-vidhya/humans-image-segmentation-with-unet-using-tensorflow-keras-fd6cb43b06e5)**



- **Source 3**: Dice Loss

  - **[Reference](https://cvinvolution.medium.com/dice-loss-in-medical-image-segmentation-d0e476eb486)**

  Excerpt:
  This is the metric we used in our evaluation. From the definition, we notice that dice coefficient enlarges the weight of overlap both in the denominator and numerator, based on inequality in the x ray images, if the overlap rises, the dice loss will response with greater gradient flow information which encourages more precise segmentation.

  In medical images, like x ray imaging, usually the bones themselves occupy the most majority of the image, if using IoU Loss, the network may choose to predict the whole images as positive and still yields decent performance, this would make further learning hard. If Dice Loss employed, the weight of overlap in the loss definition increases, so the network would be motivated to split the cells other than learning some heuristics like the case in IoU Loss.