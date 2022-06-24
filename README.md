### EX NO : 11
### DATE  : 03.06.2022
# <p align="center">Opening-and-Closing</p>


## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
1. Step1:
Import the necessary packages

2. Step 2:
Create the Text using cv2.putText

3. Step 3:
Create the structuring element

4. Step 4:
Use Opening operation

5. Step 5:
Use Closing Operation

6. Step 6:
end the program.
 
## Program:

``` Python
# Developed By:J Vincent isaac jeyaraj
# Register Number: 212220230060

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,300),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'VINCENT',(5,65),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)
```
## Output:

### Display the input Image
![Capture64](https://user-images.githubusercontent.com/75234588/172544834-603f3bba-be97-4b1d-a561-317cd64a042c.PNG)

### Display the result of Opening
![Capture65](https://user-images.githubusercontent.com/75234588/172544883-3a6fdb49-3b69-4a26-ae0b-59c45a4cf384.PNG)

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
![Capture66](https://user-images.githubusercontent.com/75234588/172544900-25d62899-4a6d-4688-bc8d-35ae3272d35b.PNG)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
