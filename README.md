# oak-d_raspberry-pi
Repository containing what I learned about the use of oak-d depth camera with raspberry pi

I downloaded custom linux operating system image to my sd card. The image was dowloaded from https://docs.luxonis.com/projects/hardware/en/latest/pages/guides/raspberrypi.html. I downloaded the OAK_CM4_POE_V9, it was the recommended image for installation. I used raspberry pi imager to write the image to the sd card and enabled ssh for easy use of the raspberry pi.

!Important:
When connecting through ssh to the raspberry pi, it is important to add the flag -X when connecting, for example: 'ssh raspdor@raspdor.local -X'.
THis step is crucial because the flag enables X11 forwarding, so opencv could forward the imshow images to the main computer through ssh.

After you successfuly connected you can run the command: 'python depthai-python/examples/MobileNet/rgb_mobilenet.py', which will run a python script that will show live fedd from the camera with the addition of fps count.

!important: I would suggest checking that the raspberry pi is cooled and not getting too hot, it may affect performance and even cause crashes as a rasult of overheating.
