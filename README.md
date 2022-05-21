# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step1:
Import the necessary packages.

Step2:
Create the Text using cv2.putText.

Step3:
Create the structuring element.

Step4:
Erode and Dilate the image.

Step5:
End Program.

 
## Program:

``` 
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image= np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,'THARUN',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Name",image)

# Create the structuring element
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Erode Image",erodeImage)

# Dilate the image
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)



cv2.waitKey(0)
cv2.DestroyAllWindows




```
## Output:

### Display the input Image
![1](https://user-images.githubusercontent.com/93427201/169656734-612e0cc0-186c-4059-9afe-b41d59424e2d.jpeg)


### Display the Eroded Image
![2](https://user-images.githubusercontent.com/93427201/169656741-21d4f68b-7343-4968-aa5b-f1b28154fdeb.jpeg)


### Display the Dilated Image
![3](https://user-images.githubusercontent.com/93427201/169656752-5e974f8e-db2c-4f18-93a2-c22456a447eb.jpeg)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
