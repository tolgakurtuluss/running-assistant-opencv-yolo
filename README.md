# 🏃 running-assistant-opencv-yolo
**🏃 Building an AI Running Assistant to get Recommendations for optimum walking/running conditions using OpenCV, YOLOv2 and OpenWeatherMap**

![](https://github.com/tolgakurtuluss/running-assistant-opencv-yolo/raw/main/output.png)

[![Open in colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/tolgakurtuluss/c20fa444ed04099d43f6dec0260df31a/bahcelievlerpark.ipynb)


> Main problem;

*   Problem here is to decide to go out for walking either my favourite walking trail is crowded by others and weather is optimal or not.
*   I used open-sourced streaming video source of Bahcelievler Belediyesi Kuleli live webcamera where it's accessible by everyone.
(Source: Bahçelievler Belediyesi Video Platformu - https://video.bahcelievler.bel.tr/)


> Step-by-step solutions;

*   I used **OpenCV** and a pre-trained "lightweight" model known for its speed that's still relatively accurate, **YOLOv2 in Darkflow** (the Tensorflow implementation of YOLO in Darknet) to count how many people are using the walking trail **per minute**.
*   Using OpenWeatherMap's one time call api, gathered **weather data** for exact location of park with walking trail.
*   Final decision is based on if **people per minute** is greater than **15 people** and **live feeling weather** is less than **5 °C**, it is not recommended to walk/run.



> Credits;

* (Faster video file FPS with cv2.VideoCapture and OpenCV) - https://www.pyimagesearch.com/2017/02/06/faster-video-file-fps-with-cv2-videocapture-and-opencv/
* (Computer Vision with EOL v3 Images) - https://github.com/aubricot/computer_vision_with_eol_images
