## Implementation-of-Erosion-and-Dilation-Using-OpenCV

## Aim:

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

* The program performs the following operations:

* Image Erosion
* Image Dilation
  
## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm:

## Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:

Create a blank image using NumPy.

## Step 3:

Insert text onto the image using OpenCV's text drawing function.

## Step 4:

Display the original image.

## Step 5:

Create a structuring element (kernel) of suitable size.

## Step 6: Image Erosion:

* Apply the erosion operation using the created kernel.
* Remove pixels from the boundaries of foreground objects.
* Display the eroded image.
  
## Step 7: Image Dilation:

* Apply the dilation operation using the same kernel.
* Add pixels to the boundaries of foreground objects.
* Display the dilated image.
  
## Step 8:

Compare the original, eroded, and dilated images.

## Program:

## Developed by: Syed Shamsheer Ali
## Register Number: 212225220114

## Original Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

```
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'SYED SHAMSHEER ALI B', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image with Text")
plt.axis('off')
```

## Erosion:

```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```

```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)) 
plt.title("Eroded Image")
plt.axis('off')
```

## Dilation:

```
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  
plt.title("Dilated Image")
plt.axis('off')
```

## Output:

## Original Image:

<img width="470" height="483" alt="image" src="https://github.com/user-attachments/assets/ae35a135-1ca1-46ad-ae30-755c561d6789" />

## Erosion:

<img width="472" height="485" alt="image" src="https://github.com/user-attachments/assets/4170272d-5a5b-4a01-a5df-21d5788e51db" />

## Dilation:

<img width="472" height="485" alt="image" src="https://github.com/user-attachments/assets/936b89d7-1413-4b06-a71b-f4a07e588174" />

## Result:

Thus, the morphological operations Erosion and Dilation are successfully implemented using OpenCV.
