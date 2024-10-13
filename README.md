# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim:
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries.

### Step2:
Use cv2.calcHist(images, channels, mask, histSize, ranges[, hist[, accumulate]]) to find the histogram of the image.

### Step3:
Plot the image and its stem plots using the plt.show() and plt.stem() functions.


### Step4:
Equalize the grayscale image (cv2.equalizeHist().)


### Step5:
Print and end the program.


## Program:
#### Developed By: Nithishkumar P
#### Register Number: 212221230070
```py
## grayscale image and color image channels.
```python
import cv2
import matplotlib.pyplot as plt
gray_image =cv2.imread('cat.jpg',0)
cv2.imshow('gray_image',gray_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

hist = cv2.calcHist([gray_image],[0],None,[256],[0,255])

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
# Equalizing the image
```python

#equalizing the image
equ_g = cv2.equalizeHist (gray_image)
cv2.imshow('EQUALIZED IMAGE',equ_g)
cv2.waitKey(0)
cv2.destroyAllWindows()
equal_hist = cv2.calcHist([equ_g],[0],None,[256],[0,255])

plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(equal_hist)
plt.show()
```
## color image
```python
import cv2
import matplotlib.pyplot as plt
color_image =cv2.imread('cat.jpg',-1)
cv2.imshow('color_img',color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()


# code to calculate the histogram of different channels of color image
hist0 = cv2.calcHist([color_image],[0],None,[256],[0,255]) #channel 0 - blue
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,255]) #channel 1 - green
hist2 = cv2.calcHist([color_image],[2],None,[256],[0,255]) #channel 2 - red


# Display the histogram graph of different channels of color image
#channel 0 - blue
plt.figure()
plt.title("Histogram")
plt.xlabel('blue value')
plt.ylabel('pixel count')
plt.stem(hist0)
plt.show()


#channel 1 - green
plt.figure()
plt.title("Histogram")
plt.xlabel('green value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()


#channel 2 - red
plt.figure()
plt.title("Histogram")
plt.xlabel('red value')
plt.ylabel('pixel count')
plt.stem(hist2)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image

![exp4gray](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/a6c441b8-8360-4fd4-a111-35fe50b86721)
![exp4equalized](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/28e2c18e-d600-469c-9374-1692cb016188)
![color](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/41f72147-3f26-4006-971b-9a0ce838bd4a)



### Histogram of Grayscale Image and any channel of Color Image
![grayhisto](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/f5ffb0e0-90c7-4216-b5ed-55505c9e31ba)

![equali](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/97b804ba-26e3-4da9-b3fc-cf1ae7a25ce0)


### Histogram Equalization of Grayscale Image
![blue](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/a91c8e69-ba81-4615-b5ac-bdfa23cd43c8)
![red](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/8b83e736-ca45-44a1-acc0-131f416f02ca)
![green](https://github.com/JEEVAABI/HISTOGRAM/assets/93427098/2ad42de9-e92c-42e9-88ee-ef1a49cf0431)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
