# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import All The Necessary Modules.
<br>

### Step 2:
Using Averaging Filter Smoothen the given image.
<br>

### Step 3:
Using the Weighted Averaging Filter Smoothen the given Image.
<br>

### Step 4:
Using the Gaussian Filter Smoothen the given Image.
<br>

### Step 5:
Using the Median Filter Smoothen the given Image.
<br>

### Step 6:
Using the Laplacian Kernel Filter Sharpen the given Image.
<br>

### Step 7:
Using the Laplacian Operator Filter Sharpen the given Image.


## Program:
### Developed By   : Jeswanth S
### Register Number: 212221230042
</br>

### 1. Smoothing Filters
i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

### 2. Sharpening Filters
i) Using Laplacian Kernel
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1, kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('amaze.jgp')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
new_image = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
<img width="740" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/e05f425e-b757-459e-9c0f-a9e72133ff04">
</br>

ii) Using Weighted Averaging Filter
</br>
<img width="745" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/8d76dbea-c319-4d44-8114-6fab8a69000c">
</br>

iii) Using Gaussian Filter
</br>
<img width="706" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/d627b05c-2f1e-4de4-934c-9d6805b70021">

</br>

iv) Using Median Filter
</br>
<img width="706" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/09743811-ad0c-4299-b293-07eb0cdc5e58">

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernel
</br>
<img width="758" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/966dbd34-5b6e-4bab-99fc-93b1d15b3b08">

</br>

ii) Using Laplacian Operator
</br>
<img width="725" alt="image" src="https://github.com/Jeswanth21001768/IMPLEMENTATION-OF-FILTERSS/assets/94155480/07fb0c17-0d54-4be7-9cb5-52691611a733">

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
