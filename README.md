# Histogram-of-an-images->
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: Pradeepraj P
# Register Number: 212222240073

import cv2
import matplotlib.pyplot as plt
import numpy as np
gray_image = cv2.imread('gray.jpg')
color_image = cv2.imread('color.jpg')
cv2.imshow("gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_image=cv2.imread('gray.jpg')
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure(figsize=(10,6))
plt.subplot(1,2,1)
plt.imshow(gray_image)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('color.jpg')
color_img=cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB)
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_img,[0],None,[255],[0,255])
plt.figure(figsize=(8,4))
plt.subplot(1,2,1)
plt.imshow(color_img)
plt.subplot(1,2,2)
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-09-29 171404](https://github.com/user-attachments/assets/b9307723-a504-435e-91e0-d2f33c69cdea)

### Histogram of Grayscale Image
![Screenshot 2024-09-29 171453](https://github.com/user-attachments/assets/d8e9f305-3f23-4132-ba93-df4ad383fd04)

### Histogram of Color Image
![Screenshot 2024-09-29 171513](https://github.com/user-attachments/assets/b739a717-0691-45b3-902e-eb12ed39f788)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-09-29 171753](https://github.com/user-attachments/assets/1e2aacd9-338c-4cab-91d1-28e5c8747e2d)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
