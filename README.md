# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** YASWANTH.V
- **Register Number:** 212225220125

  ### Ex. No. 01

### **Step 1: Read and Display Image**
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('vr46.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```
### **Step 2: Draw a Line**
```python
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

### **Step 3: Draw a Circle**
```python
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

### **Step 4: Draw a Rectangle**
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

### **Step 5:Image with Text**
```python
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

### **Step 6: Convert RGB to HSV**
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
### **Step 7: Convert RGB to Gray**
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
### **Step 8: Convert RGB to YCrCb**
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

### **Step 9: Convert HSV back to RGB**
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

### **Step 10: Modify Pixel Block**
```python
image[200:500, 200:500] = [255, 255, 255]
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

### **Step 11: Resize Image**
```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

### **Step 12: Crop ROI**
```python
roi = image[50:350, 50:350]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

### **Step 13: Flip Horizontally**
```python
image = cv2.imread('vr46.png')
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

### **Step 14: Flip Vertically**
```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

### **Step 15: Save Final Image**
```python
cv2.imwrite(
"final_output.jpg",
flipped_horizontally
)**
```
### **Step16: IMAGE WITH TEXT
```
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
##**

## Output:
### Original Image
<img width="913" height="470" alt="image" src="https://github.com/user-attachments/assets/3144ba8d-c89d-4275-be92-060b2a5f80c0" />



### Image with Line
<img width="900" height="437" alt="image" src="https://github.com/user-attachments/assets/1c8ac886-1910-41b6-9676-4c259fbf884a" />


### Image with Circle

<img width="842" height="447" alt="image" src="https://github.com/user-attachments/assets/2eecb0a0-322c-4483-b8f9-15b5b32cb527" />


### Image with Rectangle

<img width="872" height="457" alt="image" src="https://github.com/user-attachments/assets/a5ab5b27-2a6a-405a-b34d-c29616afbaaf" />

### Image with Text
<img width="781" height="445" alt="image" src="https://github.com/user-attachments/assets/21c2b2fa-8b20-43ec-8d12-0f64e5a27c6a" />

### HSV, Gray and YCrCb Images
<img width="887" height="431" alt="image" src="https://github.com/user-attachments/assets/d7e6f135-798f-4cf3-aeed-2c7a06e27f5c" />
<img width="882" height="430" alt="image" src="https://github.com/user-attachments/assets/536455df-cdd0-4798-a95f-f6499211fe09" />
<img width="817" height="427" alt="image" src="https://github.com/user-attachments/assets/f4f34e1e-4303-4a0d-9511-61b90afe1dbd" />

### Resized Image
<img width="805" height="523" alt="image" src="https://github.com/user-attachments/assets/13337b63-0917-42cf-95bc-dc2efa9c6064" />


### Cropped ROI

<img width="650" height="516" alt="image" src="https://github.com/user-attachments/assets/705bd4f7-edd3-41da-b4d8-f37beb126a76" />

### Flipped Images

<img width="803" height="457" alt="image" src="https://github.com/user-attachments/assets/68333826-cb4c-4210-94f9-5e7189eb5f36" />

<img width="806" height="437" alt="image" src="https://github.com/user-attachments/assets/aaad8b5c-e743-44bf-850d-b78b6e8ab519" />


## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

