# 使用摄像头
准备一个USB摄像头，将摄像头插在树莓派的USB口上
 
###捕捉图像

###显示图像
```
import os
import pygame, sys
import pygame.camera

width = 640
height = 480

#initialise pygame   
pygame.init()
pygame.camera.init()
cam = pygame.camera.Camera("/dev/video0",(width,height))
cam.start()

#setup window
windowSurfaceObj = pygame.display.set_mode((width,height),1,16)
pygame.display.set_caption('Camera')
while True:
    #take a picture
    image = cam.get_image()

    #display the picture
    catSurfaceObj = image
    windowSurfaceObj.blit(catSurfaceObj,(0,0))
    pygame.display.update()
```