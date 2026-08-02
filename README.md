# Histogram Equalization Using OpenCV (Grayscale & Color Images)

---

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  

---

## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the image `parrot.jpg` in grayscale format.

### Step 3:
Display the grayscale image and plot its histogram.

### Step 4:
Apply histogram equalization using `cv2.equalizeHist()` to enhance contrast.

### Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

### Step 6:
Read the same image in color format.

### Step 7:
Split the image into B, G, R channels and plot their histograms.

### Step 8:
Convert the image from BGR to HSV color space.

### Step 9:
Apply histogram equalization on the V (Value) channel.

### Step 10:
Merge the channels and convert the image back to BGR format.

### Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

---

## Program

### Developed By:
**Name:** KAVIDHARSHINI RAMESH

### Register No: 2122225240069

## STEP - 1
```
import cv2
from matplotlib import pyplot as plt
```
## STEp - 2
```
# Load the color image
image = cv2.imread('parrot.jpg')
```
## STEP - 3
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
## STEP - 4
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## STEP - 5
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
## STEP - 6
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## STEP - 7
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
## STEP - 8
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
## STEP - 9
```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
## STEP - 10
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
---

##  Output

### Grayscale Histogram Equalization

- Original grayscale image is displayed

<img width="735" height="580" alt="image" src="https://github.com/user-attachments/assets/175bfe83-5903-4e14-ae1a-ee309f05292c" />

- Histogram of original grayscale image is plotted

<img width="750" height="615" alt="image" src="https://github.com/user-attachments/assets/b4fac03b-42d3-40c0-80db-20b6b6a84fae" />


- Enhanced image after histogram equalization is displayed

<img width="767" height="581" alt="image" src="https://github.com/user-attachments/assets/fc4cd154-07ef-490d-a852-0e9a28857b29" />



- Histogram of enhanced grayscale image shows improved contrast  

<img width="740" height="615" alt="image" src="https://github.com/user-attachments/assets/650a9a84-3dcb-4462-bd85-e00fd32fe4a6" />




---

## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
