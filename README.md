# Gray Scale Morphology
## PROGRAM
```
Developed By : J.JENISHA
Reg. No. : 212222230056
```
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
frac=cv2.imread('bone.jpg')

# Define the structuring element for erosion
kernel = np.ones((11,11),np.uint8)

# Apply erosion morphological operation
eroded_image = cv2.erode(frac, kernel, iterations=1)

plt.subplot(1, 2, 1)
plt.imshow(frac, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

plt.show()

import cv2
import matplotlib.pyplot as plt
import numpy as np
frac=cv2.imread('bone.jpg')

# Define the structuring element for erosion
kernel = np.ones((11,11),np.uint8)

# Apply erosion morphological operation
eroded_image = cv2.erode(frac, kernel, iterations=1)

# Subtract eroded image from original to get fractures
fractures = cv2.absdiff(frac,eroded_image)

plt.subplot(1, 2, 1)
plt.imshow(frac, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image (flat)')
plt.axis('off')

plt.show()
```
## OUTPUT
![Screenshot 2024-05-20 195622](https://github.com/Jenishajustin/Gray_Scale_Morphology/assets/119405070/9b68de4e-751a-4306-b51b-cda4c20b6ee6)
![Screenshot 2024-05-20 195644](https://github.com/Jenishajustin/Gray_Scale_Morphology/assets/119405070/843b1b73-d51d-47bd-ba43-cf6642dc2a57)
