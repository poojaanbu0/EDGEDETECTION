# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.

### Step2:
Read the image and convert the rgb image to gray scale image.

### Step3:
Use filters for smoothing the image to reduce the noise.

### Step4:
Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
Display the filtered image using plot and imshow.

## Program:
```
Developed by: Pooja A
Register no: 212222240072
```

### Import the packages and load image
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("wome.jpg")
gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.title("Original")
plt.imshow(gray,cmap='gray')
plt.axis('off')
plt.show()
```

## SOBEL EDGE DETECTOR
### SOBEL X AXIS :
```python
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X")
plt.axis("off")
plt.show()
```

### SOBEL Y AXIS :
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y")
plt.axis("off")
plt.show()
```

### SOBEL XY AXIS :
```python
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY")
plt.axis("off")
plt.show()
```

### LAPLACIAN EDGE DETECTOR
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian")
plt.axis("off")
plt.show()
```

### CANNY EDGE DETECTOR
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny")
plt.axis("off")
plt.show()
```

## Output:
### Original:
![WhatsApp Image 2023-11-13 at 23 28 20_ddd3ff47](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/2f3dddd5-e443-4e99-be8d-8a3625ac46a6)

### SOBEL EDGE DETECTOR
### Sobel X:
![WhatsApp Image 2023-11-14 at 00 21 20_4bb5ef22](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/70fd586e-095f-484d-977e-6fafec166cac)

### Sobel Y:
![WhatsApp Image 2023-11-14 at 00 22 02_66cb81c0](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/8b0cf368-02f4-429b-a2e5-f7ee28a78c2d)

### Sobel XY:
![WhatsApp Image 2023-11-14 at 00 22 28_d5d46b36](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/af1dbcb9-f8a3-4175-b076-dccfc3a57cdf)

### LACIAN EDGE DETECTOR
![WhatsApp Image 2023-11-13 at 23 36 44_636dbe59](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/44f7a016-c19a-4cfc-9ac6-71febada1dfc)

### CANNY EDGE DETECTOR
![WhatsApp Image 2023-11-14 at 00 23 02_493dff9b](https://github.com/poojaanbu0/EDGEDETECTION/assets/119390329/b5ce00d3-40fe-48d0-9211-d1fe0925f891)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
