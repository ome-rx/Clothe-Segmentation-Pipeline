# Clothing Segmentation Project

## Overview

This project implements a clothing segmentation solution using a U-Net model. It processes images to segment and extract clothing items, providing visualizations of the original image, segmentation mask, masked image, and extracted clothing.

## Features

- Clothing segmentation using a pre-trained U-Net model
- Image preprocessing and postprocessing
- Segmentation refinement using edge detection and morphological operations
- Visualization of results (original, mask, masked, and extracted clothing)
- Batch processing of multiple images

## Output Images

The script generates four types of output images for each input:

1. `original_{i}.png`: The original input image
2. `mask_{i}.png`: The segmentation mask
3. `masked_{i}.png`: The original image with the segmentation mask overlay
4. `extracted_{i}.png`: The extracted clothing item on a white background

Where `{i}` is the index of the processed image.

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/clothing-segmentation-project.git
   cd clothing-segmentation-project
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Place your input images in the `Images` folder.

2. Update the `image_paths` list in the script with the paths to your input images.

3. Set the `output_dir` variable to your desired output directory.

4. Run the script:
   ```
   python clothing_segmentation.py
   ```

5. The script will process each image and save the results in the specified output directory. It will also display the results using matplotlib.

## Assumptions and Decisions

1. The script assumes that the U-Net model file is available and can be loaded using the `create_model` function.
2. Input images are resized to 320x320 pixels for processing.
3. A simple binary threshold (>0.5) is used to create the segmentation mask.
4. Edge detection and morphological operations are used to refine the segmentation results.
5. The script uses a white background for extracted clothing items.
6. The visualization uses a 70% opacity for the original image and 30% for the mask in the masked image.

## Future Improvements

- Implement multi-class segmentation for different clothing categories
- Add support for different input image sizes
- Optimize the processing pipeline for better performance
- Implement a user interface for easier interaction with the script

