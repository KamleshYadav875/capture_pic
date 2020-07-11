# Capture pics 

import cv2    #import cv2
import sys    #import sys

cpt = 0       #counter for pic name

vidStream = cv2.VideoCapture(0)

while True:
    ret, frame = vidStream.read()
    cv2.imshow("Capture photo", frame)

    cv2.imwrite(r"D:\Capture_Photo\images\img%04i.jpg" %cpt, frame) #save pic to specific folder
    cpt +=1

    if cv2.waitKey(10) == ord('q'): #when q is press from keybord to stop taking pic
        break
