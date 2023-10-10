# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step2:
Translate the image.
### Step3:
Scale the image
### Step4:
Shear the image in both the the axes.
### Step5:
Find the reflection of the image.
### Step6:
Rotate the image.
### STEP7:
Crop the image.Display all the transformed images.
## Program:
```python
Developed By: SARGURU.K
Register Number:212222230134
```
```PYTHON
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
translated_image = cv2.warpPerspective(org_image,M,(cols,rows))
plt.imshow(translated_image)
plt.show()

ii) Image Scaling

import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()


iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("e.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1,0,0],[0,1.5,0],[0,0,1.5]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()


iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("e.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("e.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()



vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("e.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:450,120:600]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/46d79f55-d770-4098-809a-b2276f5a2627)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/0dd2a129-1da1-49b6-bceb-2d65589bd56e)
### ii) Image Scaling
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/017cfd29-1eff-4501-8805-ee647fdbcedd)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/b8ec94db-9215-4b34-9e44-d9334ba9f18a)
### iii)Image shearing
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/b38f1108-5a92-4648-8f82-3f855288d4ca)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/cb72aae4-ddc1-4836-8861-860dd8b8ee0e)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/ced78ebc-b5fb-4dda-a29b-4cd86ea9189e)
### iv)Image Reflection
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/4b7cbe49-0436-4719-84eb-3707f00ac0e6)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/d50cee28-818e-4139-89bf-0f61a136d370)
### v)Image Rotation
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/fd620a2b-6865-4a6f-bd75-d4fadcc2a66c)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/4de2f144-ab4a-435f-b88e-3c377866a1aa)
### vi)Image Cropping
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/fd2158c4-55b5-47ec-ab26-a4b62bfd6276)
![download](https://github.com/BaskaranV15/IMAGETRANSFORMATION/assets/118703522/914be236-3bd1-408f-ad96-3aac695d0c73)
## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
