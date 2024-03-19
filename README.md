# Histogram-of-an-images
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

# Developed By: B.NARENDRAN
# Register Number: 21222224069
### Input Grayscale Image and Color Image
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
### Histogram of Grayscale Image and any channel of Color Image
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


### Histogram Equalization of Grayscale Image.

```
import cv2
gray_image = cv2.imread("grey image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT
### Input Grayscale Image and Color Image
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/6fc700dd-62e2-48c0-b672-122df3d6e8a9)
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/40f0ea66-92ac-484a-b8c2-896044ef958e)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/121fc4e4-6f5c-44ae-824f-306e30a5409e)
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/0764721c-e0ff-497f-86cb-ed42752c0a8f)
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/7d00b73c-ce03-4f6e-a176-182edabe4b0a)
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/a075177e-6648-4de9-aa16-2cc3e91621d4)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/c405afc3-55ef-493e-bfec-758e852b1480)

![image](https://github.com/naren2704/Histogram-of-an-images/assets/118706984/8e5b940e-a470-4b07-b29f-2d7e474b1c94)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
