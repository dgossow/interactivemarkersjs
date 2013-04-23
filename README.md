## Deprecated

The Interactive Marker functionality has moved to
[ros3djs](https://github.com/robotwebtools/ros3djs). Ros3djs includes
interactive markers plus scene management, Collada loading, and more.

## Original Description

InteractiveMarkers.js provides an implementation of [Interactive Markers](http://www.ros.org/wiki/interactive_markers) 
for the web based on [ros.js](https://github.com/RobotWebTools/rosjs), 
[actionlib.js](https://github.com/RobotWebTools/actionlibjs) and 
[three.js](https://github.com/mrdoob/three.js/).

In order to reduce data traffic, it requires you to run a 
[proxy node](https://github.com/dgossow/interactive_marker_proxy) on the topic that you are subscribing to
and a [tf republisher](https://github.com/RobotWebTools/tf2_web_republisher).

Please also use the most recent source version of interative_markers and 
[visualization_tutorials](https://github.com/ros-visualization/visualization_tutorials), as some changes are not released yet 
(on ROS Fuerte, use [this branch](https://github.com/ros-interactive-manipulation/interactive_markers/tree/fuerte-devel)).

The library is designed to be modular, lightweight and to follow the UMD convention. 

Modules
=======
 * markersthree.js: Visualizes Marker messages in three.js
 * threeinteraction.js: Mouse Interaction library for three.js
 * improxy.js: Client to an Interactive Marker proxy server via ros.js
 * imthree.js: View Interactive Markers using the above libraries
 * tfclient.js: tf implementation via actionlib.js

Usage
=====

For example WebGL apps, see the examples directory.

To run the basic_controls example, go to the examples directory and run (in two terminals):

`./simple_webserver.py`

`roslaunch basic_controls.launch`

Then, go to [http://localhost:8000/examples/basic_controls.html](http://localhost:8000/examples/basic_controls.html).
