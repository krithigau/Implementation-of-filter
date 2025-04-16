# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.

## Program:
### Developed By   :KRITHIGA U
### Register Number:212223240076
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("kholi.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()

```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:

![Screenshot 2025-04-16 070612](https://github.com/user-attachments/assets/052621d5-c70e-4704-a922-f6a5c86b4a58)

### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![Screenshot 2025-04-16 070622](https://github.com/user-attachments/assets/fa885143-6cad-41f0-81f0-40c7cc0995fb)


ii)Using Weighted Averaging Filter

![Screenshot 2025-04-16 070632](https://github.com/user-attachments/assets/9baaa5f9-f22e-48ec-89ac-1d9d05e109b4)


iii)Using Gaussian Filter

![Screenshot 2025-04-16 070648](https://github.com/user-attachments/assets/5b2ae99c-f076-4786-849f-de5fda46a3fe)


iv) Using Median Filter

![Screenshot 2025-04-16 070659](https://github.com/user-attachments/assets/36435bb7-7c61-4423-ace8-2997d7baab43)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![Screenshot 2025-04-16 070707](https://github.com/user-attachments/assets/1ca1f566-a587-4626-8f03-69ed8c8f6a5d)

ii) Using Laplacian Operator

![Screenshot 2025-04-16 070714](https://github.com/user-attachments/assets/088e7fe1-8f11-4645-97c4-36cd9585d0b1)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
