# Visual-words-in-google-celebrity-dataset
Visual words in google celebrity dataset


## Overview

1. **Establish Dictionary**: In this step, we compute SIFT descriptors for a set of training images and cluster them using K-Means to create a visual dictionary.

2. **Convert New Image to Visual Words**: We use the visual dictionary to convert a new image into a histogram of visual word occurrences.

3. **Histogram Representation**: We compute a histogram representation of the visual words in the new image.

4. **Histogram Matching**: We can then use histogram matching to compare the histogram of the new image with histograms of other images in the dataset for classification purposes.

## Usage

1. Set the `training_path` variable to the path containing the training images.
2. Set the `new_image_path` variable to the path of the new image you want to classify.
3. Define the number of clusters `K` for K-Means clustering.
4. Run the script.


