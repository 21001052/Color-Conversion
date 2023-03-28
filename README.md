# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
import opencv.

### Step2:
Read the original Image.

### Step3:
Store the required conversion of the image in a variable.

### Step4:
Show the image stored in the given variable.

### Step5:
Destroy all the windows and end the program.

## Program:
```python
# Developed By: G Venkata Pavan Kumar
# Register Number: 212221240013
# i) Convert BGR and RGB to HSV and GRAY
  import cv2
house_color_image= cv2.imread('car.jpg')
cv2.imshow ('Original image', house_color_image)
hsv_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_image)
hsv_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_image1)
gray_image= cv2.cvtColor (house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_image)
gray_image1 = cv2.cvtColor (house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)

# ii)Convert HSV to RGB and BGR
import cv2
house_HSV_image= cv2.imread('car.jpg')
cv2.imshow('Original HSV image',house_HSV_image)
RGB_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',RGB_image )
BGR_image = cv2.cvtColor(house_HSV_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',BGR_image)
cv2.waitKey(0)
cv2.destroyAllwindows()


# iii)Convert RGB and BGR to YCrCb

import cv2
houseImage = cv2.imread('bike.jpg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
import cv2
image = cv2.imread('car.jpg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()


# v) Split and merge HSV Image
import cv2
image = cv2.imread('car.jpg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![DPIIMG1](https://user-images.githubusercontent.com/94827772/162903299-264076fb-559a-4fca-ad80-a8ee67e3f89d.png)


### ii) HSV to RGB and BGR
![DPIIMG2](https://user-images.githubusercontent.com/94827772/162903327-901ffc36-06a9-40db-8ce1-e595ccadba22.png)


### iii) RGB and BGR to YCrCb
![DPIIM3](https://user-images.githubusercontent.com/94827772/162903462-b3f71b05-bf6d-4768-99c7-14982c975ae4.png)


### iv) Split and merge RGB Image
![DPIIMG3](https://user-images.githubusercontent.com/94827772/162903688-536b17ef-2a1b-4030-bc0e-2516c3c10830.png)


### v) Split and merge HSV Image
![DPIIMG4](https://user-images.githubusercontent.com/94827772/162903724-c760d9bf-6c6d-4a1d-822d-7e5e6470cfff.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
