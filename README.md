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
