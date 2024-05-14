## EXP 10 OPENING--AND-CLOSING
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
Developed by: Pragaharshitha NC
Register Number:212222110033
```
#### Display the input Image
```
import cv2
import numpy as np
```
```
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Ice broken', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
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
![Screenshot 2024-05-05 144113](https://github.com/Thirisha-s/OPENING--AND-CLOSING/assets/120380280/7580d1e8-7277-42be-8d93-db8083858e6c)

#### Display the result of Opening
![Screenshot 2024-05-05 144125](https://github.com/Thirisha-s/OPENING--AND-CLOSING/assets/120380280/7e0e69e0-e301-4d15-91a4-ed39253a04b5)

#### Display the result of Closing
![Screenshot 2024-05-05 144155](https://github.com/Thirisha-s/OPENING--AND-CLOSING/assets/120380280/b1394bb5-b49d-49d4-b3ee-63242f1ab1e3)

### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
