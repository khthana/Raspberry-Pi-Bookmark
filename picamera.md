https://www.raspberrypi.org/learning/getting-started-with-picamera/worksheet/

from picamera import PiCamera
from time import sleep

camera = PiCamera()

camera.start_preview()
sleep(10)
camera.stop_preview()

camera.rotation = 180
camera.start_preview()
sleep(10)
camera.stop_preview()

camera.start_preview()
sleep(5)
camera.capture('/home/pi/Desktop/image.jpg')
camera.stop_preview()
