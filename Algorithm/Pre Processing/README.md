# Image Pre-Processing Phase

## Overview

In this phase, we process images to prepare them for further analysis. This involves several steps including loading images, cropping, noise reduction, and image sharpening.

## Steps

### 1. Loading Sample Images

We load sample images from a 14-day dataset. Below is an example of the 20th image from a Pixel device used throughout this process.

![image](https://github.com/user-attachments/assets/cee1de9c-91d3-4d9b-bac8-a8d3d676d4d9)



### 2. Cropping the White Background

To avoid unnecessary influence in our calculations, we crop out the white background from the images.

![Cropped Image](https://github.com/user-attachments/assets/b6289d4d-054c-494d-bf84-4c93b44b5869)

### 3. Applying Gaussian Blur

To make the process efficient and to simplify the cropped samples, we reduce the 3 color channels into 1. Gaussian blur is applied to reduce random noise produced during dataset preparation. We chose Gaussian blur because it allows for effective noise reduction, which is essential for the subsequent sharpening step.


![image](https://github.com/user-attachments/assets/38af120a-febc-4272-b5bf-cd3b95ef52c3)


### 4. Sharpening the Images

#### Step 4.1: Applying the Laplacian Filter

We apply the Laplacian filter to the blurred images. This filter detects edges in all directions simultaneously, which is useful for identifying fungal growth that lacks a definite shape.

![image](https://github.com/user-attachments/assets/401b9c9d-50ed-4a45-8606-9e4da03a5c99)


#### Step 4.2: Subtracting the Laplacian Output

After applying the Laplacian filter, we subtract its output from the previous image to obtain sharpened images.


![image](https://github.com/user-attachments/assets/308646cc-c6bd-4652-901a-415ab9ebb481)


## Conclusion

These steps summarize the pre-processing phase of our algorithm. Below is the simplified overview of the process:

1. Load sample images.
2. Crop the white background.
3. Apply Gaussian blur to reduce noise.
4. Sharpen images using the Laplacian filter.

This concludes the pre-processing phase of our image processing algorithm.
