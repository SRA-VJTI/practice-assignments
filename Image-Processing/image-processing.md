## Image Processing Task :computer:

The following tasks are to ensure that your basics of computer vision are clear along with all the concepts. 
The following tasks are to be performed **WITHOUT** using any of the libraries such as cv2 unless specified. 
The packages which can be used are Numpy and PIL. 

**Hint:-** Convert the image into a numpy matrix  

---
### 1. Image Rotation

Rotate an image by various angles. 
Hence write a code that will be generic for 90, 180 degrees.  
<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/rotate.png">  

### 2. Applying Kernels

Find out 5X5  filters which can do the following tasks and apply them on the given image
1. Blurring (Apply any 3 filters)
2. Sharpening  

|<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/blur.jpeg">|<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/filter.png">|
|:---:|:---:|

### 3. Edge Detection
  
Find out 3X3 filters which can do the following tasks and apply them on the given image
1. Vertical edge detection
2. Horizontal edge detection
3. Sobel edge detection (right, left, top, bottom)
4. Canny edge detection  
<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/edge-detection.png">  

### 4. Morphological Transformation  

Find out about morphological transforms (erosion , dilation) and apply them on given images    
<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/morphological.png">  

### 5. Masking

For this section your task is to detect a blue ball  
**Hint:-** Explore HSV colorspace and you can use ​`cv2.cvtColor(frame, cv.COLOR_BGR2HSV)`  
<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/mask.jpg">  

### 6. ROI

ROI (Region of interest) is obtained by Numpy indexing. Use Figure 1 to obtain Figure 2  
**Hint:-** Use bitwise operations  
<img width="640" height="450" src="https://github.com/SRA-VJTI/practice-assignments/blob/master/Image-Processing/assets/roi.jpg">  

