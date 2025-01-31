---
layout: default
title: Robotics Course Report
---

# Robotics Course Report

Welcome to my robotics course report! Below, you'll find images and videos documenting the progress and functionality of my robot, along with explanations for each.

---

## Image of Camera and Motor Signals from Dashboard

![Camera and Motor Signals](assets/images/camera-motor-signals.jpg)

**Explanation**: This image shows the signals captured from the dashboard, showing both the motor signals and the camera signals. In the chart at the top, it shows the speed of the left and right motor. We can see that there is a slight difference between the speed of the two motors. I think this is because before wheel calibration, the two wheels should have the same speed, but after doing wheel calibration we tweeked the speed of the two wheels to make it able to move in a straight line. Below it shows the image of the camera signal, showing us what the robot is looking at, which seems fairly good to me.

---

## Screenshot of Duckiebot Saying "Hello from MY_ROBOT"

![Duckiebot Screenshot](assets/images/duckiebot-hello.jpg)

**Explanation**: This screenshot demonstrates the Duckiebot's interface displaying the message "Hello from csc22916", as we can see in the picture, I have successfully built the image using docker, so as using the template in github to build the python program and environments. Lastly, I successfully ran the very simple hello world program on my duckiebot, though struggling at first as you can see, there were many error messages previously :) (RH2 Unit B-2.3).

---

## Screenshots of Camera Calibration .yaml Files

### Intrinsics Calibration
![Intrinsics Calibration](assets/images/intrinsics-calibration.jpg)

### Extrinsics Calibration
![Extrinsics Calibration](assets/images/extrinsics-calibration.jpg)

**Explanation**: These screenshots show the `.yaml` files for camera calibration, including intrinsics and extrinsics parameters. The intrinsic parameters describe the internal characteristics of the camera, such as its optical center, focal length, and lens distortion as we can see in the screenshot. These parameters are specific to the camera itself and do not depend on its position or orientation in the world. On the other hand, the extrinsic parameters describe the camera's position and orientation relative to a world coordinate system, as we can see in the screenshot, it consists of a homography matrix, which includes the camera position and orientation informations. These parameters define how the camera is positioned in 3D space. Accurate intrinsic and extrinsic parameters are necessary for performing tasks like lane following.

---

## Screenshot of Kinematics .yaml File

![Kinematics .yaml File](assets/images/kinematics-yaml.jpg)

**Explanation**: This screenshot displays the kinematics configuration file, which defines the robot's motion parameters. These parameters where likely modified as we do the wheel calibration, these paramters are crucial for us to control the robot's motion.

---

## Video of 2m Straight Driving

<iframe width="560" height="315" src="https://youtube.com/embed/7d23Su7wlAY?feature=share" frameborder="0" allowfullscreen></iframe>

**Explanation**: This video demonstrates the robot driving straight for 2 meters, showcasing its motion control capabilities. We can see that it is drifting off a bit to the left, but that is OK for our duckiebot, the small drift is acceptable since it is hard for it to go perfectly straight, there are to many external factors that are impacting its performance, I do think that the smoothness of the mattress is something that makes it not working as properly as expected.

---

## Video of Lane Following Demo

<iframe width="560" height="315" src="https://youtube.com/embed/yuF5YfN6ei0?si=yS2v0GK7UkI1nUGq" frameborder="0" allowfullscreen></iframe>

**Explanation**: This video shows the robot successfully following a lane, highlighting its navigation and control systems. The duckiebot is moving slower than when we use keyboard control, I think it is because the duckiebot is viewing and computing in order to follow the line, and hence resulting in less speed. But anyways, the result seems more than acceptable, the duckiebot is indeed following the lane for a whole lap.

---

## Conclusion

During this lab exercise, I gained hands on experience with the duckiebot for the first time, I followed the guide to do all those calibrations, and it was indeed quite fun. I got the chance to learn the functions of the different components that made up duckiebot, and also the dts terminal basic commands. I also got a chance to implement a small Python program, not to exclude the experience with Docker, which I know is very popular in industries.

At the start of this lab, I first tried to do wheel calibration. This is to assure that the robot can move in a fairly straight line. Before calibrating, I noticed that the robot is drifting right, so I adjusted the trim parameters little by little and achieved quite a good result, but the second time I test it with the exact same parameters, the robot drifts off again. I do think that the uneven surface of the mattress is causing the problems, but I also think that not placing the robot accurately in the center is also a small issue. Robots could detect a drift by the camera, as we have lane markers on the mattress, and it will detect drift if markers does not align with what it should be like when driving in a straight line.

Then I did camera calibration, this is important because it is crucial for tasks like lane following, as it uses camera to detect lanes and follow them. Making the robot recognize a recognized image is how we do both the intrinsics and extrinsics camera calibrations.

When doing the lane following demo, I do notice that the robot seems to be failing while it path is a turn. I think this might be due to the fact that the robot might have failed to accurately detect the lane markings during the turn, and hence causing it to lose track of the path. The robot is following the lane through computer vision, it detects the lane markings to recognize the path.

The key takeaway in this lab is that I realized that robots are always not behaving as expected, sometimes, instead of tuning parameters, just simply give the robot a few more tries.
