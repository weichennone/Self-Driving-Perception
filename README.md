# Self-Driving System: Perception
Perception module of the self-driving system


## System Components & Structure
The structure is shown as below:

As we can see, our system contains a LiDAR, a RGB camera and two infrerad (IR) cameras. 

The cameras are mainly used for detecting objects on the road, e.g. vehicles, pedestrian, etc. The IR cameras can provide a good view when it's lack of clear sight (e.g. when it is foggy, rainy, snowy, or dark). The IR cameras can also provide the depth information from the stereo disparity map. 

We use SSD-MobileNet v1 (https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md) for the object detection task. 

## Results
The results are shown as below:
We can see the correct bounding box around the objects. Two SSD-MobileNet v1 models (one for each IR camera) are running on Nvidia Xavier with about 11FPS.

