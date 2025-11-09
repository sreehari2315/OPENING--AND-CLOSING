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
cv2.putText(image, 'RAKSHAN', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
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
<img width="509" height="515" alt="image" src="https://github.com/user-attachments/assets/994937fd-0d54-4251-9c09-67bb9dd08af6" />

### Display the result of Opening
<img width="504" height="513" alt="image" src="https://github.com/user-attachments/assets/4d5c752f-aeaa-4b3c-8013-a2043c44e508" />

### Display the result of Closing
<img width="495" height="487" alt="image" src="https://github.com/user-attachments/assets/460294a5-a5a5-4d34-a9ad-9f44f708023e" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
