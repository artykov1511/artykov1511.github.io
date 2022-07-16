## Camera Calibration

Camera calibration is a necessary part of any computer vision project. It is a tool for obtaining both internal and external camera parameters, such as focal length, optical center, and 3D pose of your camera in the worl coordinate system. In this blog post, I will give basic explanation of camera calibration and show the mathematics behind the process. There are various tutorials on how to perform calibration with opencv functions. Therefore, this post is dedicated for explanation of only the theory. So let it begin..

In this post, I will explain one of the well known classical camera calibration methods, called, Zhang's method, which was proposed in around 2000s in the following paper[1]. The first thing you need to be able to calibrate your camera is a picture of known pattern imaged on a 2D plane. It is called a calibration object and people usually use chessboard pattern as shown below.

