# Image Acqusition using Web Camera
## Aim
 
#### To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
##### i) Write the frame as JPG 
##### ii) Display the video 
##### iii) Display the video by resizing the window
##### iv) Rotate and display the video

## Software 

### Anaconda - Python 3.7

## Algorithm

### Step 1:

#### Use cv2.VideoCapture(0) to access web camera

### Step 2:

#### Use cv2.imread to read the video or image

### Step 3:

#### Use cv2.imwrite to save the image

### Step 4:

#### Use cv2.imshow to show the video

### Step 5:

End the program and close the output video window by pressing 'q'.

## Program:

### Developed By: DINESH KUMAR R
### Register No: 212222110010

#### i) Write the frame as JPG file
```py
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("dinesh.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
#### ii) Display the video
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('Hibiscus',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

#### iii) Display the video by resizing the window
```py
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
    cv2.imshow('212222110010-Dineshkumar R',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
#### iv) Rotate and display the video

```py
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
    cv2.imshow('212222110010_Dineshkumar R',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>

![dip1](https://github.com/DINESH18032004/Image_Acqusition-_using_Web_Camera/assets/119477784/7a81a36e-88ee-42df-afd9-ff0bd5a8bb7f)

</br>


### ii) Display the video
</br>

![dip 2](https://github.com/DINESH18032004/Image_Acqusition-_using_Web_Camera/assets/119477784/fb4cf477-8352-4dfd-87a1-49afb0428c66)


</br>


### iii) Display the video by resizing the window
</br>

![dip3](https://github.com/DINESH18032004/Image_Acqusition-_using_Web_Camera/assets/119477784/e3a9c92a-8bd9-4ccf-be4e-9b4fb97d3e27)


</br>



### iv) Rotate and display the video
</br>



![dip4](https://github.com/DINESH18032004/Image_Acqusition-_using_Web_Camera/assets/119477784/595bc6a3-4740-425c-af3d-c358d5301602)




## Result:
### Thus the image is accessed from webcamera and displayed using openCV.
