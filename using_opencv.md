# 使用OpenCV
OpenCV的全称是：Open Source Computer Vision Library。OpenCV是一个基于BSD许可（开源）发行的跨平台计算机视觉库，可以运行在Linux、Windows和Mac OS操作系统上。它轻量级而且高效——由一系列 C 函数和少量 C++ 类构成，同时提供了Python、Ruby、MATLAB等语言的接口，实现了图像处理和计算机视觉方面的很多通用算法。

OpenCV在人机互动、物体识别、图像分割、人脸识别、动作识别、运动跟踪、运动分析、机器视觉、结构分析、汽车安全驾驶等领域有广泛应用。

OpenCV-Python 在线教程：http://opencv-python-tutroals.readthedocs.org/en/latest/py_tutorials/py_tutorials.html
###安装OpenCV
```
sudo apt-get install python-opencv
```
###显示图像
```
import cv2   

img = cv2.imread("picture.jpg")   
cv2.namedWindow("Image")   
cv2.imshow("Image", img)   
cv2.waitKey (0)  
cv2.destroyAllWindows()  
```
###获取像素信息
```
import cv2   

img = cv2.imread("picture.jpg")   
x = 100
y = 120
print img[x,y,0],img[x,y,1],img[x,y,2]
#Blue, Green, Red 
```
###调用摄像头

###人脸识别

###视频直播
