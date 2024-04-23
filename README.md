# Implementation of Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1 :
Load the necessary packages requiured for the implemtation of erosion and dilation on an image.

### Step 2 :
Create the text image for the implemtation of erosion and dilation using cv2.putText function.

### Step 3 :
Create the structuring image for the implemtation of erosion and dilation on the text image.

### Step 4 :
Apply the erosion and dilation to the text image using cv2.erode and cv2.dilate.

### Step 5 :
Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6 :
End the program.
 
## Program:
## Developed by : Yogabharathi S
## Register Number: 212222230179
### Program to implement Erosion and Dilation using Python and OpenCV.
## Import the necessary packages :
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create the Text using cv2.putText :
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'YOGABHARATHI',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
## Create the structuring element :
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
## Dilate the image :
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output :
## Display the input Image :

![image](https://github.com/Yogabharathi3/erosion--dilation/assets/118899387/630e7aa1-8853-4926-afb9-c1f809faac68)

## Display the Eroded Image :
![image](https://github.com/Yogabharathi3/erosion--dilation/assets/118899387/b52129d0-c8f5-4a35-8ccf-271672451a50)


## Display the Dilated Image :
![image](https://github.com/Yogabharathi3/erosion--dilation/assets/118899387/478ed09a-ffc6-48e5-8ae4-82a35a1cf0c9)

## Result :
Thus the generated text image is eroded and dilated using python and OpenCV.
