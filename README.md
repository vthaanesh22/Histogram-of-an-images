# Histogram-of-an-images
## NAME:Thaanesh.V
## REG.NO:212223230228
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
```python
# Developed By:ABINAYA S
# Register Number:212222230002
```
## Input Grayscale Image and Color Image :
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grey image.jpg")
color_image = cv2.imread("color image.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image:
```
import numpy as np
import cv2
Gray_image = cv2.imread("grey image.jpg")
Color_image = cv2.imread("color image.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
## Histogram Equalization of Grayscale Image:
```
import cv2
gray_image = cv2.imread("grey image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
## Input Grayscale Image and Color Image
![grey1](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/09b729df-2bdb-4432-81d6-1d5b8452b029)

![color 1](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/2c4740b9-e173-4f30-bbfe-a7a6d52c2f2d)


## Histogram of Grayscale Image and any channel of Color Image
![grey1 2](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/674d54e5-c151-4a34-8bce-f34a8e1e88b9)
![color 1 2](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/bcd899d6-7278-469c-8140-8b38cb008cfe)

## Histogram Equalization of Grayscale Image.
![grey 1 3](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/555fce14-db57-4128-b06e-b9fb4172e3fe)
![equali 1 3](https://github.com/abinayasangeetha/Histogram-of-an-images/assets/119393675/7267ff7b-b679-46c0-827b-167f07ec0c3e)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
