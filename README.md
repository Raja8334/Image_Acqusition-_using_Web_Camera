# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:

Use cv2.VideoCapture(0) to access web camera
<br>
### Step 2:

Use cv2.imread to read the video or image
<br>
### Step 3:

Use cv2.imwrite to save the image
<br>
### Step 4:

Use cv2.imshow to show the video
<br>
### Step 5:

End the program and close the output video window by pressing 'q'.
<br>

## Program:
``` Python
### Developed By:
### Register No:

## i) Write the frame as JPG file

import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("raja.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()


## ii) Display the video

import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('bird',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


## iii) Display the video by resizing the window


import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222100041',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()


## iv) Rotate and display the video

import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222100041',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()







```
## Output

### i) Write the frame as JPG image

![Screenshot 2024-02-27 102652](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/4eaafd18-98a3-4d8e-a548-970bf29e0644)


### ii) Display the video

![2](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/dfaf4b00-4326-49e2-aa52-c6f441374c5c)

### iii) Display the video by resizing the window


![3](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/dada9502-f3cd-4c05-bfcf-79b3814ee4a6)



### iv) Rotate and display the video


![4](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/e3492c19-e820-45c5-a4e1-be6687e58aa8)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
