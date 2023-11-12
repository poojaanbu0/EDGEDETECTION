# EDGEDETECTION

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
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## Program:
```
NAME : KAVYA K
REG NO : 212222230065
```


# Import the packages
```
import cv2
import numpy as np
```


# Load the image, Convert to grayscale and remove noise
```
image = cv2.imread('image.jpg', cv2.IMREAD_GRAYSCALE)
```


# SOBEL EDGE DETECTOR
```
# Apply Sobel edge detection
sobel_x = cv2.Sobel(image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(image, cv2.CV_64F, 0, 1, ksize=5)
sobel = np.sqrt(sobel_x**2 + sobel_y**2)

cv2.imshow('Sobel Edge Detection', sobel)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


# LAPLACIAN EDGE DETECTOR
```
# Apply Laplacian edge detection
laplacian = cv2.Laplacian(image, cv2.CV_64F)

cv2.imshow('Laplacian Edge Detection', laplacian)
cv2.waitKey(0)
cv2.destroyAllWindows()

```


# CANNY EDGE DETECTOR
```

# Apply Canny edge detection
canny = cv2.Canny(image, 100, 200)  # You can adjust the threshold values as needed

cv2.imshow('Canny Edge Detection', canny)
cv2.waitKey(0)
cv2.destroyAllWindows()
```




## Output:
### SOBEL EDGE DETECTOR

![Sobel Edge Detection_screenshot_11 10 2023](https://github.com/Jayakrishnan22003251/EDGEDETECTION/assets/120232371/22b908aa-2283-4cdb-8c83-0d5e8d104108)


### LAPLACIAN EDGE DETECTOR

![laplacian](https://github.com/Jayakrishnan22003251/EDGEDETECTION/assets/120232371/cfcbea38-aea7-46cc-b6de-7c9383e91a26)



### CANNY EDGE DETECTOR
![canny](https://github.com/Jayakrishnan22003251/EDGEDETECTION/assets/120232371/e155bd31-83f7-4f35-960d-5c15ace8e0b0)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
