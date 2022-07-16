## Camera Calibration

Camera calibration is a necessary part of any computer vision project. It is a tool for obtaining both internal and external camera parameters, such as focal length, optical center, and 3D pose of your camera in the worl coordinate system. In this blog post, I will give basic explanation of camera calibration and show the mathematics behind the process. There are various tutorials on how to perform calibration with opencv functions. Therefore, this post is dedicated for explanation of only the theory. So let it begin..

In this post, I will explain one of the well known classical camera calibration methods, called, Zhang's method, which was proposed in around 2000s in the following paper[1]. The first thing you need to be able to calibrate your camera is a picture of known pattern imaged on a 2D plane. It is called a calibration object and people usually use chessboard pattern like the one shown below.

![chessboard](https://user-images.githubusercontent.com/18645902/179359427-ed43daed-b03d-441c-821b-40fa9ee8c5c5.png)

After getting your calibration object, let's assume that it is sticked to the center of the world frame. So every point on the chessboard pattern has the Z=0. Now, with this information at hand we will build a relationship between the points in the calibration object (which was sticked onto the world frame) and the ones on our images.  
