# OPENING--AND-CLOSING
## Name: Sree Hari K
## Reg.No: 212223230212
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
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HARI', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Create the structuring element
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Use Opening operation
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image)
plt.axis("off")
```
## Output:

### Display the input Image
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/82f08a7e-e9f9-4f6a-a970-42170f717892" />

### Display the result of Opening
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/e1547f21-9224-4b6a-978d-9bccf6e06753" />


### Display the result of Closing
<img width="389" height="389" alt="image" src="https://github.com/user-attachments/assets/af4cfe60-b5a1-4ec8-ada5-dcd76414878a" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
