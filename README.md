# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step 2:
Create the Text using cv2.putText.

### Step 3:
Create the structuring element.

### Step 4:
Use Opening operation.

### Step 5:
Use Closing Operation.

### Step 6:
Print the output and end the program.

 
## Program:
```
Developed by: Harini.B
Register number: 212221230035
```

``` 
# Import the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Harini Bas",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("ORIGINAL IMAGE")
plt.imshow(text_image)
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
open_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("OPENING")
plt.imshow(open_image)
plt.axis('off')

# Use Closing Operation
close_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("CLOSING")
plt.imshow(close_image)
plt.axis('off')
```

## Output:

### Display the input Image
![pic1](https://github.com/HariniBaskar/Opening-and-Closing/assets/93427253/d976f85b-d3c6-411f-9d82-a4381bce8836)


### Display the result of Opening
![pic2](https://github.com/HariniBaskar/Opening-and-Closing/assets/93427253/b6bb9f46-3b1f-4cba-a751-ae63e402334a)


### Display the result of Closing
![pic3](https://github.com/HariniBaskar/Opening-and-Closing/assets/93427253/15c6d210-e893-4f91-acb8-efdc4ecf318d)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
