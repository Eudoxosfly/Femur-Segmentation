# Model Definition and Evaluation

Although we decided to not use augmentation and binary crossentropy for our base model, we thought it worth a try to use both for our UNet model. Using binary crossentropy resulted in the [second model](SecondModel.ipynb). After this proved inferior, we switched to dice loss and dice metric in the [third model](ThirdModel.ipynb). Some augementation was [tested](ThirdModelAugmentedDataset.ipynb), but yielded equivalent results to our baseline model, the model perfomance was decreased. 

After deciding on the final model with dice loss and metric, without augmentation and with Adam optimizer, only hyperparameter tuning was left. On the one hand, we tuned [manually](ThirdModelHypterParameterTuning.ipynb) by iterating over different parameter combinations. The problem was the high computational expense, where the one run took over ten hours.
To tackle this problem, we tried using the [Hyperband tuner](hyperparameter_tuning.ipynb) to decrease the amount of resources needed. This works by letting different hyperparameter combinations compete in a bracket style competition, where gradually more computational resources are provided as fewer candidates are still in the contest. This yielded only a slight increase in dice metric, which shows that hyperparameter optimization can help a model improve performance, but it is not guaranteed and even if it works, it may only be a small improvement.

Overall, our model performed very well on the test dataset, giving segmentation masks that differed only in the smallest margins from the ground truth.
