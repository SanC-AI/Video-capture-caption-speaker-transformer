# Video-capture-caption-speaker-transformer
This project is for RPi based Video capture with Object detection and captioning it with transformer and play the caption on speaker


I have already developed the light weight OpenCV based Object detection logic based on RPi Camera.
Now with this project I have taken it 2 step next level.

Here I have used the transformer based image captioning model to caption the captured video frame.
And also used the "flite" library to convert the captioned text to Audio output, so user can hear out the caption instead of looking into screen for caption.
Basically I have developed this for Automobile use case. Where driver can get the captioned audio based on image captured by its camera module.


As I have mentioned earlier OpenCV is using 40% cpu for object detection, where as audio conversion is not consuming any extra cpu load.
But as soon as I used the transformer library for captioning the image CPU load is increased to 300% while it is doing the captioning.
And this transformer based model is consuming the 30% of memory, in my RPi I have 4GB of RAM.

Also it is consuming the 300% CPU while initializing/loading the transformer model for captioning.
