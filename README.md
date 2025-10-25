# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

``` Python
#NAME:SOMALARAJU ROHINI
#REG.NO: 212224240156

# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "ROHINI", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

cv2_imshow(img2)

# ii) Create structuring elements
kernel1 = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))
kernel2 = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# iii) Use Opening operation (Erosion followed by Dilation)
img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)

# iv) Use Closing operation (Dilation followed by Erosion)
img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)

```
## Output:

### Display the input Image
<img width="721" height="375" alt="image" src="https://github.com/user-attachments/assets/a273b663-04e9-42d8-8c1a-e99e258c0d2f" />


### Display the result of Opening
<img width="690" height="366" alt="image" src="https://github.com/user-attachments/assets/93c459a5-e9de-4ba6-a856-c2045636562c" />


### Display the result of Closing
<img width="699" height="372" alt="image" src="https://github.com/user-attachments/assets/c4415ee6-fe46-4828-bddf-8597e1c2e01e" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
