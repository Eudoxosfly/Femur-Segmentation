# Baseline Model

For the [baseline model](BaselineModel), it was decided to use a simple fully connected network with an output reshaped back to the original image height and width.

The model was trained using binary crossentropy as a loss. This, as we later found out, is sub-optimal and we switched for later models to the dice loss.
Nevertheless, the results even this model produced are quite good already. While the contours are not sharply defined (something the later models struggled with as well, before switching to the dice loss), the general area and shape of the proximal femur was correctly detected.

Furthermore, the dataset was augemnted using usual techniques likes zooms and crops. In the end, this was not used, as the data has a strongly defined inherent structure (the bodies always have the same orientation, always two proximal femurs in the exact same locations, etc). "Enhancing" the dataset through augmentation therefore reduced our model's performance, as generalization was not needed in this case.
