# Canny_edge_detection
## NAME : Pooja P
## REG NO : 212224230195
## Aim:
To implement the Canny Edge Detection algorithm in Python using OpenCV, and visualize each step of the process — from grayscale conversion to Gaussian blur and final edge detection — on a sample image.

## Overview:
This project demonstrates how to apply Canny Edge Detection, a multi-stage algorithm used to detect edges in an image while minimizing noise. It involves:

-Converting the image to grayscale

-Applying Gaussian Blur to remove noise

-Detecting edges using Canny algorithm with two threshold values

-Displaying all intermediate stages using Matplotlib

## Steps Performed:
1.Read the input image using OpenCV.

2.Resize the image for uniform processing.

3.Convert the image to grayscale.

4.Apply Gaussian Blur to reduce noise and smooth the image.

5.Perform Canny Edge Detection using two threshold values.

6.Display all stages — original, grayscale, blurred, and edge-detected — using Matplotlib.

## Tech Used:
~ Python 3.x

~ OpenCV (cv2)

~ Matplotlib

## Program:
```py
import cv2
import matplotlib.pyplot as plt
# Read the image
img = cv2.imread('photo1.jpg',cv2.IMREAD_GRAYSCALE)
# Apply Gaussian blur to reduce noise
blurred =cv2.GaussianBlur(img, (5,5),0)
# Detect edges using Canny
edges = cv2.Canny(blurred, 50, 150) #Adjust threshold values as needed
# Plot the original image and the detected edges
plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```
Output:

<img width="737" height="440" alt="image" src="https://github.com/user-attachments/assets/f2326672-5d3a-40e1-a411-30b41a229a2b" />


## Result:
The Canny algorithm successfully detects clear, continuous edges while suppressing noise.Gaussian Blur improves the quality of detected edges by smoothing small variations. Final output displays - Original Image,Grayscale Image,Blurred Image,Canny Edge Detected Image.

