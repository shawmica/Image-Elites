# Image Segmentation Phase

This repository outlines the image segmentation process we followed for our analysis. Below are the detailed steps:

## 1. Dilation for Preprocessed Image
We chose dilation for the preprocessed image to connect nearby components of patches. This step won't affect our goal analysis because we performed dilation for all the samples equally.

![image](https://github.com/user-attachments/assets/a767f6fa-6217-4df2-880d-f1531599a6ce)           ![image](https://github.com/user-attachments/assets/3eca9911-93ad-45ce-8c6d-26f2d4d4095a)



## 2. Otsu Thresholding
We attempted Otsu thresholding to extract the foreground and background. To do that, we checked the histogram for each image to see if it was bimodal. Unfortunately, the histograms were not bimodal.

![WhatsApp Image 2024-08-07 at 18 03 40_a31ab06c](https://github.com/user-attachments/assets/33f1de66-3d19-4514-a40d-b88221be8d7f)


## 3. Adaptive Thresholding
Given the lack of bimodal histograms, we opted for adaptive thresholding because it can calculate the threshold for each pixel based on its local neighborhood. Instead of analyzing all the black patches in the sample, we selected three patches to ensure the accuracy of our outcome.

![image](https://github.com/user-attachments/assets/63cb89a5-cccb-4b40-990e-530d62b41c99)




## 4. Floodfill for Patch Extraction
To extract each patch, we used floodfill manually on each sample.Here You might be curious why we chose floodfill over contour detection. It is because floodfill offers simple region filling, handling irregular shapes easily.

<img width="287" alt="image" src="https://github.com/user-attachments/assets/bab25f6c-07ec-4c8a-a974-0cd88dd0e839">


## Conclusion

The image segmentation phase involved several steps to accurately isolate and analyze patches within the samples. We began by performing dilation to connect nearby components. Due to the lack of bimodal histograms, we applied adaptive thresholding for better foreground and background extraction. Finally, we used floodfill for patch extraction, favoring it over contour detection due to its effectiveness in handling irregular shapes.

These steps ensured a robust segmentation process, providing reliable data for further analysis.

