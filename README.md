## 🏃 Building an AI Running Assistant using OpenCV, YOLOv2, and OpenWeatherMap

This project aims to develop an AI Running Assistant that provides recommendations for optimum walking/running conditions. The solution includes three main steps: counting the number of people on the walking trail using OpenCV and YOLOv2, retrieving weather data using OpenWeatherMap, and deciding whether or not to go out for a walk/run based on the gathered data.

![](https://github.com/tolgakurtuluss/running-assistant-opencv-yolo/raw/main/output.png)

[![Open in colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/tolgakurtuluss/c20fa444ed04099d43f6dec0260df31a/bahcelievlerpark.ipynb)

To solve the problem of whether or not to go out for a walk/run, the project uses a pre-trained "lightweight" model known for its speed and relative accuracy, YOLOv2 in Darkflow (the Tensorflow implementation of YOLO in Darknet), to count the number of people on the walking trail per minute. The model is used in conjunction with OpenCV to analyze the streaming video source of Bahcelievler Belediyesi Kuleli live webcam, which is accessible to everyone.

To gather weather data for the exact location of the park with the walking trail, OpenWeatherMap's one-time call API is used.

The final decision on whether or not to go for a walk/run is based on two main factors: the number of people per minute and the "live feeling" weather. If the people per minute is greater than 15 and the live feeling weather is less than 5°C, it is not recommended to walk/run.

> Credits;
  * (Faster video file FPS with cv2.VideoCapture and OpenCV) - https://www.pyimagesearch.com/2017/02/06/faster-video-file-fps-with-cv2-videocapture-and-opencv/
  * (Computer Vision with EOL v3 Images) - https://github.com/aubricot/computer_vision_with_eol_images
