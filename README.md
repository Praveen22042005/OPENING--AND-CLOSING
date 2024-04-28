# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
NAME: PRAVEEN BV
REG.No: 212222100036
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Cyber Security',(4,70), font,1,(255),5,cv2.LINE_AA)
```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/Praveen22042005/OPENING--AND-CLOSING/assets/112475766/f1375769-3432-4907-8032-ace230bba053)
### Display the result of Opening
![image](https://github.com/Praveen22042005/OPENING--AND-CLOSING/assets/112475766/ba35d849-f357-4863-9d24-b7c4d0e8442c)
### Display the result of Closing
![image](https://github.com/Praveen22042005/OPENING--AND-CLOSING/assets/112475766/01f8dd24-657b-43eb-8832-934eed10e55a)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
