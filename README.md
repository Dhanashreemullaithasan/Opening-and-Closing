# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:

Import the necessary packages.

#### Step 2: 

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

``` Python
Developed by : DHANASHREE M
Register Number : 212221230018

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
text_image = np.zeros((100,540),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"DHANASHREE M",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')


# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')



```
## Output:

### Display the input Image

![d1](https://github.com/Dhanashreemullaithasan/Opening-and-Closing/assets/94165415/df78f5a1-a7f1-4063-a00d-c36b63931f7d)

### Display the result of Opening

![d2](https://github.com/Dhanashreemullaithasan/Opening-and-Closing/assets/94165415/a432bffd-44da-4938-ab5d-d5725045b923)

### Display the result of Closing

![d3](https://github.com/Dhanashreemullaithasan/Opening-and-Closing/assets/94165415/20ecbc34-4c28-4f6e-b995-47741ecf4457)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
