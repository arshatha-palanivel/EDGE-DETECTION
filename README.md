# EDGE-DETECTION
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
## PROGRAM:
```
DEVELOPED BY: ARSHATHA.P
REGISTER NO.:212222230012
```
```python
Convert image to grayscale and remove noise:
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("rose.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
#### SOBEL X AXIS :
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
#### SOBEL Y AXIS :
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
#### SOBEL XY AXIS :
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```py
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```


## Output:
### SOBEL EDGE DETECTOR:
#### SOBEL X AXIS:
![image](https://github.com/arshatha-palanivel/EDGE-DETECTION/assets/118682484/3a4bd2b0-bdb3-45da-9c2d-ba1512803407)

#### SOBEL Y AXIS:
![image](https://github.com/arshatha-palanivel/EDGE-DETECTION/assets/118682484/a9491c2a-da62-4dd3-a9f9-fda2761416fe)

#### SOBEL XY AXIS:
![image](https://github.com/arshatha-palanivel/EDGE-DETECTION/assets/118682484/befd8e44-fb39-4e82-b384-e2f307d83cc3)

### LAPLACIAN EDGE DETECTOR:
![image](https://github.com/arshatha-palanivel/EDGE-DETECTION/assets/118682484/76766c20-3a72-4207-a40e-f0e96fb2dc03)

### CANNY EDGE DETECTOR:
![image](https://github.com/arshatha-palanivel/EDGE-DETECTION/assets/118682484/2e9c01c4-735c-4ecb-a61e-d53f0e342b10)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
