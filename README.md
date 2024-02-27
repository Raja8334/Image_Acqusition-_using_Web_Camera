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
<br>
Use cv2.VideoCapture(0) to access web camera
### Step 2:
<br>
Use cv2.imread to read the video or image
### Step 3:
<br>
Use cv2.imwrite to save the image
### Step 4:
<br>
Use cv2.imshow to show the video
### Step 5:
<br>
End the program and close the output video window by pressing 'q'.

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
</br>
![Screenshot 2024-02-27 102652](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/7a2db0ee-db6c-4b60-8533-c488f9944a78)

</br>


### ii) Display the video
</br>
![2](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/42101342-d937-4e5e-81d8-30261961dc54)

</br>


### iii) Display the video by resizing the window
</br>
![3](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/3fc09282-2293-4d64-841c-76381a7b7834)

</br>



### iv) Rotate and display the video
</br>
![4](https://github.com/Raja8334/Image_Acqusition-_using_Web_Camera/assets/120719634/d6d9feae-c951-4288-b36f-06833e56cfdb)

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
