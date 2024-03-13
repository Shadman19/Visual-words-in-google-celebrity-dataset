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

## Example

```python
# Set the paths and parameters
training_path = "../ECE884/archive (3)/img_align_celeba/img_align_celeba"
new_image_path = "../ECE884/IMG_0543.jpg"
K = 10000  # Number of clusters

# Step 1: Establish Dictionary
dictionary = establish_dictionary(training_path, K)

# Step 2: Convert New Image to Visual Words
visual_words = compute_visual_words(new_image_path, dictionary)

# Step 3: Histogram Representation
histogram = histogram_representation(visual_words, K)

# Plot Histogram
plt.figure(figsize=(10, 6))
plt.bar(range(K), histogram, color='blue', alpha=0.7)
plt.title('Histogram of Visual Words')
plt.xlabel('Visual Word Index')
plt.ylabel('Frequency')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
