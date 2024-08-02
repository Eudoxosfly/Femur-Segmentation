# Dataset Characteristics

The dataset consists of images in the nifti format, which is commonly used in the medical community for x-ray and MRI images.
To make working with them easier, they were converted to .png while preserving the full color depth (8-bit) and resolution using the notebook **[conversion](conversion.ipynb)
Afterwards, the success of the conversion was checked by comparison with the orginals. Furthermore, characteristics of the dataset, like the size of the images, the number of labels in the mask and histograms of the x-ray images were [examined](explorativeAnalysis.ipynb).
To finish up, a tf.data.Dataset was [created](createDataset.ipynb) to seamlessly load image and mask for training the model.
