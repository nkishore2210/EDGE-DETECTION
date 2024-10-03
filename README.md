## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### Name: KISHORE N
### Reg No. 212222240049

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('mikey kun dorake kun.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
```
```python
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()
```
### OUTPUT:
![Screenshot 2024-10-03 155935](https://github.com/user-attachments/assets/0794b7bb-5c49-41cb-a745-922b7dd40af4)

```python
# Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```
### OUTPUT:
![Screenshot 2024-10-03 160031](https://github.com/user-attachments/assets/495c0be1-9a21-4a58-9a9f-5457672381fc)

```python
# Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
```
### OUTPUT:
![Screenshot 2024-10-03 160120](https://github.com/user-attachments/assets/f0f6763e-fe2e-49dc-9cdf-7ee174d10a18)

```python
# Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
### OUTPUT:
![Screenshot 2024-10-03 160158](https://github.com/user-attachments/assets/65c59005-e57a-487e-ae31-9a463f57f00d)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
