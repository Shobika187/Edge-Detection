# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.


### Step2:
Read the image and convert the bgr image to gray scale image.

### Step3:
Use any filters for smoothing the image to reduse the noise.

### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector

### Step5:
Display the filtered image using plot and imshow.

 
## Program:
```
Devloped by: Shobika P
Register No: 212221230096
```

# Import the packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Load the image, Convert to grayscale and remove noise

```
img=cv2.imread ('img.jpg')
img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.title('Original_image')
plt.imshow(img1)

gray_img = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
plt.title('GRAY_IMAGE')
plt.imshow(gray_img,cmap = 'gray')
```

# SOBEL EDGE DETECTOR

```
img = cv2.GaussianBlur(gray_img,(3,3),0)
sobelx = cv2.Sobel(gray_img,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_img,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_img,cv2.CV_64F,1,1,ksize=5)

plt.figure(1)
plt.subplot(1,1,1)
plt.imshow(gray_img,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])

```
### SOBELx
```
plt.subplot(1,1,1)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])

```
### SOBELx
```
plt.subplot(1,1,1)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])
```
### SOBELxy
```
plt.subplot(1,1,1)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
```

# LAPLACIAN EDGE DETECTOR

```
laplacian = cv2.Laplacian(gray_img,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()
```

# CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_img, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```




## Output:

## GRAY IMAGE
![s1](https://user-images.githubusercontent.com/94508142/232531691-09d0d397-d0ba-47d5-aba4-8372cc158f87.png)

## SOBEL EDGE DETECTOR
### SOBELX
![s2](https://user-images.githubusercontent.com/94508142/232531910-bd75ee0d-e80b-423c-ad7e-f57a207c5a91.png))
### SOBELY
![s3](https://user-images.githubusercontent.com/94508142/232532033-a6ad2673-f281-4530-a4ca-76c7b74fc3d0.png)
### SOBELXY
![s4](https://user-images.githubusercontent.com/94508142/232532114-8e78a20e-d7e4-445e-bcf3-89201a913ede.png)



### LAPLACIAN EDGE DETECTOR
![s5](https://user-images.githubusercontent.com/94508142/232532241-a6335e99-9553-4b1c-811a-7d7b35f078c4.png)


### CANNY EDGE DETECTOR
![s6](https://user-images.githubusercontent.com/94508142/232532340-57029b26-f615-4a7d-9e11-3b3b8672b25c.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
