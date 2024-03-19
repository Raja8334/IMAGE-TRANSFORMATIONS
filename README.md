# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: RAJA R
Register Number: 212222100041
i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "Sky.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("timesquare.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```

iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("sphere.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```


iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("statue.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  

```



v)Image Rotation
```python

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("photograph.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 

```
vi)Image Cropping
```python

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("beach.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()

```

## Output:

#### Original Image :
![Screenshot 2024-03-19 114416](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/61d39f87-cb3c-4aaf-9dc7-a6fd1da99e99)
### i)Image Translation :
![Screenshot 2024-03-19 114426](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/1977bd12-0508-481d-9860-6de8f6b3a378)


### ii) Image Scaling
![Screenshot 2024-03-19 114503](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/74a0acfa-3e60-48aa-ab61-f3b2f8f8d05a)



### iii)Image shearing
![Screenshot 2024-03-19 114539](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/fc1fbf21-57de-492a-98ec-85c6a35fa4bd)

![Screenshot 2024-03-19 114549](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/e940ddea-9991-49f3-b971-9db981fb25f5)


### iv)Image Reflection
![Screenshot 2024-03-19 114638](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/2ccdc6e1-ce09-45d7-9f60-f7e03d402238)

![Screenshot 2024-03-19 114649](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/e6f68b9d-6c0a-4cb8-9a6c-41ab3273ca96)


### v)Image Rotation
![Screenshot 2024-03-19 114721](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/04ddb875-b5b5-47f9-b167-916adc206050)




### vi)Image Cropping
![Screenshot 2024-03-19 114746](https://github.com/Raja8334/IMAGE-TRANSFORMATIONS/assets/120719634/21771095-291e-41c6-9cd4-167cf1acd33f)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
