# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
# Step1:
Import the necessary packages.

# Step2:
Create the Text using cv2.putText.

# Step3:
Create the structuring element.

# Step4:
Erode and Dilate the image.

# Step5:
End the Program.

 
## Program:

``` Python

Developed by: Gayathri A
Reg.no : 212221230028
# Import the necessary packages
import cv2
import  numpy as np
import matplotlib.pyplot as  plt


# Create the Text using cv2.putText

img=np.zeros((100,450),dtype='uint8')
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img1,'Gayathri Raj',(0,70),font,2,(219,112,147),5,cv2.LINE_AA)
cv2.imshow('MyName',img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

img_erode1=cv2.erode(img1,kernel1)
cv2.imshow('MyName',img_erode1)
cv2.waitKey(0)
cv2.destroyAllWindows()


# Dilate the image

img_dilate1=cv2.dilate(img1,kernel1)
cv2.imshow('MyName',img_dilate1)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:

### Display the input Image

![d10 1](https://github.com/Gayathriraj18/Implementation-of-Erosion-and-Dilation/assets/94154854/53cc4fb3-6a63-4344-a2a4-1de053e811e6)


### Display the Eroded Image

![d10 2](https://github.com/Gayathriraj18/Implementation-of-Erosion-and-Dilation/assets/94154854/ee94ef28-8862-45f7-9a1c-fefbbed1ac0b)


### Display the Dilated Image

![d10 3](https://github.com/Gayathriraj18/Implementation-of-Erosion-and-Dilation/assets/94154854/629ef6da-a083-48b2-bbfa-cc874dfa2a5f)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
