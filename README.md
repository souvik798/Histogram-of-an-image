# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
# Developed By: SOUVIK KUNDU
# Register Number: 212221230105


# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('download.jfif')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
Color_image=cv2.imread('2.jfif')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
import cv2
gray_image = cv2.imread("2.jfif",0)
cv2.imshow('grey scale image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows






```
## Output:
### Input Grayscale Image and Color Image
![1](https://user-images.githubusercontent.com/94752764/165466837-1cf40040-21fe-45a9-b0ae-d5ed5b306575.png)

<br>


### Histogram of Grayscale Image and any channel of Color Image
![2](https://user-images.githubusercontent.com/94752764/165466999-4b1d0d30-124c-4473-b2fd-7d34bf296272.png)


<br>

### Histogram Equalization of Grayscale Image
![Equalized Image](https://user-images.githubusercontent.com/94752764/165467128-c174209b-a579-440d-a2b3-806eb183c51e.png)

![grey scale image](https://user-images.githubusercontent.com/94752764/165467199-53c031ff-8030-4d07-aff8-cdfb1fd93bda.png)


<br>


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
