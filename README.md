<<<<<<< HEAD
# Opensource term project _ team27

## Team 27 Information
|Major|ID|name|
|------|---|---|
|Software|201937913|박예진|
|Software|201735857|이동건|
|Design|20|임수연|

## _Realtime detect object project using cvlib_
There are a total of three simple cvlib-related opencv projects. At this time, [cvlib](https://www.cvlib.net/) is an easy-to-use library for face and object recognition in Python. Since you are using opencv and tensorflow, you must install two of the following to use this library.

Tensorflow 
 ```sh
pip3 install tensorflow
```
opencv-python 
 ```sh
pip3 install opencv-python
```
✨cvlib✨
 ```sh
pip3 install cvlib
```

## Version
Pip list and version used in the project
- python version 3.8
- Tensorflow version 2.11
- Opencv-pyyhon version 4.6.0.66
- cvlib version 0.2.7

## Project
- Face detection function
- Real-time object detection in webcam images function
- Real-time face detection and mosaic in webcam images function

---

## 1. Face detection function
> 이동건 developed

We're going to use Gangnam to create a program to censor faces after detecting faces are detected.

### Function 
The functions used in the project are as follows
-faces, confidences = cv.detect_face(im)
 ```sh
-cv.detect : detect faces
```

### How to execute
To execute a function, you can do it as follows
-It's a program that automatically recognizes and blurs the face when you bring an image.

### Result 


---

## 2. Real-time object detection in webcam images function
> 임수연 developed

프로젝트 설명 서술

### Function 
The functions used in the project are as follows
-cv2.VideoCapture(0)
 ```sh
cv2.VideoCapture(0) : open webcam of capture faced
```

-cv.detect_face(frame)
 ```sh
cv.detect_face(frame) : detect face
```

-사용된 함수1
 ```sh
함수 : 설명
```

### How to execute
To execute a function, you can do it as follows
- 실행방법 서술해주세요

### Result 
사진이나 동영상 첨부 해주세요 

---

## 3. Real-time face detection and mosaic in webcam images function
> 박예진 developed

Today, I'm going to add a mosaic effect to the faces detected in the webcam video. We will put a mosaic effect on the faces through the following procedure. 

1. First, the face detection model of the cvlib library (based on deep learning) is used to detect the faces in each frame of the image. 

2. Cut off the face part, reduce the size, and enlarge it back to its original size

3. Paste the mosaic effect back into the frame. 

 ***The resolution of the face part is greatly reduced and then magnified again, making it look blurred.***

### Function 
The functions used in the project are as follows
-cv2.resize(face_region, (N, M), interpolation=cv2.INTER_AREA)
 ```sh
cv2.resize : Cut off the face part, reduce the size, and enlarge it back to its original size
```

-frame[startY:endY, startX:endX] = face_region
 ```sh
frame[startY:endY, startX:endX] : reduced and then magnified again, making it look blurred.
```
### How to execute
To execute a function, you can do it as follows
- Prepare a webcam.
- Take a picture or video of your face through a webcam
- Project automatically mosaic

### Result 
사진이나 동영상 첨부

---

## Team project operation
Group 27 was operated by implementing one function for each, creating and modifying its own branch, and then proceeding with a pull request and merging it merged.
> one function per person
> one branch per person
> a total of one register

**3 people in total implement 3 functions**

## License

MIT
**Free Software!**

## Reference
https://bskyvision.com/934
https://bskyvision.com/675
https://bskyvision.com/681
=======
# opensource   
import cv2   
import maplotlib.pyplot as plt   
import cvlib as cv   
   
image_path = 'v1.jpg'              //open the image      
im cv2.imread(image_path)          //read the image   
plt.imshow(im)   
plt.show()   
   
faces, confidences = cv.detect_face(im)      //detect faces   
   
for face in faces:                 //loop through detected faces and bounding box   
(startX, startY) = face[0], face[1]   
(endX,endY) = face[2],face[3]   
cv2.rectangle(im, (startX,startY), (endX,endY), (0,255,0), 2)   
   
plt.imshow(im)                     //display output   
plt.show()   
cv2.imwrite('result,jpg',im)       //result output   
>>>>>>> 7f1b2207b03066d08f80f2d97ce6f814bb6c9c67
