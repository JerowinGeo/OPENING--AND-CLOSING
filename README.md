# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Load the input image using cv2.imread().

### Step2:
Define a structuring element (e.g., 5x5 rectangular) using cv2.getStructuringElement().

### Step3:
Perform erosion followed by dilation using cv2.morphologyEx() with the cv2.MORPH_OPEN operation.

### Step4:
Perform dilation followed by erosion using cv2.morphologyEx() with the cv2.MORPH_CLOSE operation.

### Step5:
Use plt.subplot() to show the original, opening, and closing images side by side.
 
## Program:

``` 
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((300, 600, 3), dtype="uint8")

# Create the Text using cv2.putText
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'JEROWIN GEO', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
plt.figure(figsize=(10, 5))
plt.imshow(img, cmap='gray')
plt.axis("off")
plt.show()
![image](https://github.com/user-attachments/assets/4e59d59f-0d19-47e5-aaf2-3112db07bfad)



# Create the structuring element
kernel = np.ones((11, 11), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS, (11, 11))


# Use Opening operation
image1 = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel)
plt.figure(figsize=(10, 5))
plt.imshow(image1, cmap='gray')
plt.axis("off")
plt.show()



# Use Closing Operation
image2 = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel)
plt.figure(figsize=(10, 5))
plt.imshow(image2, cmap='gray')
plt.axis("off")
plt.show()


```
## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/a79ef044-79a3-437d-a1f4-9acf30a39963)



### Display the result of Opening
![image](https://github.com/user-attachments/assets/1f69aa76-4be7-42ed-a32c-751fec619b52)


### Display the result of Closing
![image](https://github.com/user-attachments/assets/7026c804-1433-4b07-ae9e-fb33564da828)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
