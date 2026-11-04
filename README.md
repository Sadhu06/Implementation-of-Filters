## Implementation-of-Filters

## NAME : SADHANA S

## REGISTER NUMBER : 212224230234

## Aim

To implement filters for smoothing and sharpening images in the spatial domain.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import the required libraries.

### Step 2
Read the image and convert it from BGR to RGB.

### Step 3
Apply the required smoothing and sharpening filters to the image separately.

### Step 4
Plot and display the original and filtered images using `matplotlib.pyplot`.

### Step 5
End the program.

## Program

**Developed By:** SADHANA S

**Register Number:** 212224230234

## 1. Smoothing Filters

### i) Using Averaging Filter

```
import cv2
import matplotlib.pyplot as plt
import numpy as np

image1=cv2.imread(r"C:\Users\admin\Downloads\mypic.jpeg")
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

### ii) Using Weighted Averaging Filter

```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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

### iii) Using Gaussian Filter

```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
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

### iv) Using Median Filter

```
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

## 2. Sharpening Filters

### i) Using Laplacian Linear Kernel

```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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

### ii) Using Laplacian Operator

```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
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

## Output

### 1. Smoothing Filters

#### i) Using Averaging Filter

<img width="1073" height="782" alt="image" src="https://github.com/user-attachments/assets/345a5cb9-6943-452b-a417-fb93804a5ced" />



#### ii) Using Weighted Averaging Filter


<img width="732" height="540" alt="image" src="https://github.com/user-attachments/assets/ee5f0be9-552e-463a-b089-2e973605d7dd" />



#### iii) Using Gaussian Filter


<img width="740" height="533" alt="image" src="https://github.com/user-attachments/assets/dca1439c-b28d-480e-ac8e-58b7bc93d2f8" />



#### iv) Using Median Filter


<img width="1002" height="769" alt="image" src="https://github.com/user-attachments/assets/5ac21c6f-ccc6-4564-8ab0-74ec03e8c2d1" />



### 2. Sharpening Filters

#### i) Using Laplacian Kernel


<img width="680" height="531" alt="image" src="https://github.com/user-attachments/assets/80e5964a-66a5-4854-a33b-073b3f6809b2" />



#### ii) Using Laplacian Operator

<img width="717" height="539" alt="image" src="https://github.com/user-attachments/assets/f392c399-3235-46af-8dae-8a46eff916dd" />



## Result

Thus, filters were implemented for smoothing and sharpening images in the spatial domain using OpenCV and Python.
