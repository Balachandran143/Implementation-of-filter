# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.
### Step5
End the program.

## Program:
```
 Developed By:BALACHANDRAN S
 Register Number:212222100008
```
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('chameleon.jpg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Orignal')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```
## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter
![Screenshot 2024-03-21 092405](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/31881b46-768a-49dc-aa4e-d16d1b4d0acd)

ii) Using Weighted Averaging Filter
![Screenshot 2024-03-21 092552](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/719efc3e-5acf-44bf-8e31-d491a19d3117)

iii) Using Gaussian Filter
![Screenshot 2024-03-21 092627](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/9947f75d-f273-4aa1-b3aa-239085c9ad7f)

iv) Using Median Filter
![Screenshot 2024-03-21 092705](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/3f32f3d6-bed4-40b5-84ab-158ae9be8e30)

### 2. Sharpening Filters
i) Using Laplacian Kernal
![Screenshot 2024-03-21 092753](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/7b4e1577-81bc-4c47-a5d7-263cd2ee5b40)

ii) Using Laplacian Operator
![Screenshot 2024-03-21 092817](https://github.com/Balachandran143/Implementation-of-filter/assets/118886489/cfda20df-1f27-4762-afc8-3cf64f0f4645)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
