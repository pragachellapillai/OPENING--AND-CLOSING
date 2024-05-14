## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: Joyce Beulah R
Register Number:212222230058
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ICE AGE', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![image](https://github.com/JoyceBeulah/OPENING--AND-CLOSING/assets/118343698/339eb79a-faa6-4905-956f-d7c71958c9f5)


#### Display the result of Opening
![image](https://github.com/JoyceBeulah/OPENING--AND-CLOSING/assets/118343698/c1d73204-2c9b-4aa2-b4a6-4e12bf820f1a)


#### Display the result of Closing
![image](https://github.com/JoyceBeulah/OPENING--AND-CLOSING/assets/118343698/c8b4e370-e437-4566-832d-b717aff204df)


### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
