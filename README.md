# Opening and Closing

### Aim:
To implement Opening and Closing using Python and OpenCV.

### Software Required:
Anaconda - Python 3.7
OpenCV
### Algorithm:
### Step 1:
Import the necessary packages

### Step 2:
Read the image

### Step 3:
Create the structuring element

### Step 4:
Use Opening operation

### Step 5:
Use Closing Operation

### Step 6:
Display all the output images

### Program:
```
Developed By : Silambarasan K

Register Number: 212221230101
```
```py
#Import the necessary packages
import cv2
import matplotlib.pyplot as plt
```
```py
#Plot Function
def plot(img):
    plt.imshow(img)
    plt.axis('off')
 ```
 ```py
#Create the text using cv2.putText
image = np.zeros((200,1150),dtype='uint8')
font=cv2.FONT_HERSHEY_SCRIPT_COMPLEX
cv2.putText(image,'Shafeeq Ahamed',(20,140),font,5,(255),3,cv2.LINE_AA)
plot(image)
```

```py
#Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
```
```py
#Use Opening operation
img1=cv2.morphologyEx(image,cv2.MORPH_OPEN,kernel)
plot(img1)
```
```py
#Use Closing Operation
img2 = cv2.morphologyEx(image,cv2.MORPH_CLOSE,kernel)
plot(img2)
```

### Output:
### Display the input Image
![Screenshot 2023-05-11 185924](https://github.com/simbu07/Opening-and-Closing/assets/94525786/e74a1239-63cc-438f-8026-efb92c2fa9ed)

### Display the result of Opening
![Screenshot 2023-05-11 185935](https://github.com/simbu07/Opening-and-Closing/assets/94525786/4658ca6e-cdb9-461d-9964-b1113730f7ab)

### Display the result of Closing
![Screenshot 2023-05-11 185944](https://github.com/simbu07/Opening-and-Closing/assets/94525786/49a4b9cb-f690-49df-990a-b0a86b9c867a)

### Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
