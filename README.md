# IMPLEMENTATION OF EROSION AND DILATION
## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

## PROGRAM:
```
/*
Developed by   : B.Kavya
Register Number: 212220230007
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(image,'Kavya',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(image)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(image,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(image,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```
## OUTPUT:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235813/169954859-a04004c3-102c-4284-94fa-e16f86f95f42.png)


### Display the Eroded Image
![image](https://user-images.githubusercontent.com/75235813/169954925-710f76bd-f606-4d76-8697-745f9afda452.png)


### Display the Dilated Image
![image](https://user-images.githubusercontent.com/75235813/169954965-640eed4a-a20e-4ced-b622-7cc83fbc8210.png)


## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
