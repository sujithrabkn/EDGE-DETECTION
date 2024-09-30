# EX-6 EDGE-DETECTION
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
DEVELOPED BY:SUJITHRA B K N
REGISTER NUMBER: 212222230153
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:

![pspk-1](https://github.com/user-attachments/assets/97cdebbd-35c2-43ed-a9c9-3cd3de5fc948)

### SOBEL EDGE DETECTOR:

![Screenshot 2024-09-30 193642](https://github.com/user-attachments/assets/33261c58-a801-4de1-9724-b846ec0dfd97)

![Screenshot 2024-09-30 193652](https://github.com/user-attachments/assets/baf85d4a-f5a9-4a8c-85de-ac06ce247eb0)

![Screenshot 2024-09-30 193703](https://github.com/user-attachments/assets/b8a1aa77-7416-427a-8f66-5b1b8c240286)


### LAPLACIAN EDGE DETECTOR

![Screenshot 2024-09-30 193714](https://github.com/user-attachments/assets/19f28f6d-7f8b-437e-a01b-0d62ae109c54)

### CANNY EDGE DETECTOR

![Screenshot 2024-09-30 193725](https://github.com/user-attachments/assets/d6252c8c-2030-485e-91a6-eba3aeca698f)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
