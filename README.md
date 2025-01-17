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
# Developed By:R.Vijay
# Register Number:212221230121
# i) Convert BGR and RGB to HSV and GRAY
import cv2
house_color_image = cv2.imread('img5.jpg')
cv2.imshow('Original image',house_color_image)
#BGR 2 HSV
hsv_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
#RGB 2 HSV
hsv_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
# BGR 2 GRAY
gray_image = cv2.cvtColor(house_color_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
# RGB 2 GRAY
gray_image1 = cv2.cvtColor(house_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)

cv2.waitKey(0)
cv2.destroyAllWindows()




# ii)Convert HSV to RGB and BGR

import cv2
sun_color_image = cv2.imread('img5.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()






# iii)Convert RGB and BGR to YCrCb

import cv2
sun_color_image = cv2.imread('img5.jpg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()





# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('img5.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()





# v) Split and merge HSV Image

import cv2
image = cv2.imread('img5.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('H',h)
cv2.imshow('S',s)
cv2.imshow('V',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()





```
## Output:
### i) BGR and RGB to HSV and GRAY
![DIP1](https://user-images.githubusercontent.com/94381788/228289333-35097c93-fc22-489c-bdb9-1569685962e2.png)


### ii) HSV to RGB and BGR
![DIP2](https://user-images.githubusercontent.com/94381788/228289437-02a9b47b-444a-4ef7-bb89-d8710a2f9370.png)


### iii) RGB and BGR to YCrCb
![DIP3](https://user-images.githubusercontent.com/94381788/228289511-8617f726-587f-473d-94af-d50dbae66905.png)


### iv) Split and merge RGB Image
![DIP4](https://user-images.githubusercontent.com/94381788/228289592-cb626594-134d-4573-b0b3-5df234dbf13c.png)


### v) Split and merge HSV Image
![DIP5](https://user-images.githubusercontent.com/94381788/228289651-2447f713-b1d0-457b-b847-de5f22df4e76.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
