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

## PROGRAM :
### Developed By : K MADHAVAREDDY
### Register Number : 212223240064

### Importing packages,load and convert to gray image
```python
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('orangeflower.jpg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### Sobel Edge Detector

### Sobel X  
```python
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y
```python
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```python
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### Laplacian Edge Detector
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

### Canny Edge Detector
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## OUTPUT:
### Gray Image
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/80c5a6f1-c02a-458d-8cc8-d371c485a1e2)

### SOBEL EDGE DETECTOR
### Sobel X
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/b4fe1077-fbcb-4b0a-8f18-27aeddf70150)
### Sobel Y
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/495994b7-0e52-4e80-ac78-843a624acfe4)
### Sobel XY
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/125a0797-282e-4a0a-be45-0a9d8caf2ade)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/3a1ff6c8-a6fb-49eb-a72a-80774cebff67)



### CANNY EDGE DETECTOR
![image](https://github.com/Madhavareddy09/EDGE-DETECTION/assets/145742470/b94d75d3-8ffb-47f6-9dbc-27bdff9dd8f1)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
