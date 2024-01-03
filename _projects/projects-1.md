---
title: "eYantra Robotics Competition"
excerpt: "Pre-emptive scheduling algorithm for task allocation which could be used in drones at the time of survey and rescue in disaster afflicted areas.<br/><img src='/images/projects/eyrc/eyrc_pv.jpg'>"
collection: projects
---

<p style="text-align: justify">
e-Yantra Robotics Competition is a six month long competition which need to be accomplished in a team of 4. Our theme was Survey and Rescue in which we have to develop a pre-emptive scheduling algorithm for a drone which will aid individuals afflicted by natural disaster.</p>

<p style="text-align: justify">
<b>Task 0</b> was setting up the system with Gazebo simulator. Other software we used was ROS (Robot Operating System) Kinetic and underlying operating system was Ubuntu 16.04. Primary language of implementation was Python. After setup was done, we received Task 1 which was as follow:</p>

<p style="text-align: justify">
<b>Task 1.1</b> - Position hold of the drone in a simulation
	   The drone should hold its position in the given simulation scene at the given point [2, 2, 20] using the PID control algorithm.
</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/xRDrj8BBL4Y?si=0mCUtrI0Pf1qUYVv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
<b>Task 1.2</b> - Waypoint navigation of the drone in a simulation
	   The drone should visit the given waypoint coordinates in the simulation using the PID control algorithm. Waypoints are in the form (x, y, z).
	   [(0.2, 0, 23), (3.5, -3.3, 23), (-4.4, -4.6, 20.7), (-6.0, 6.3, 18.3), (5.0, 5.3, 16.3)]
</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/p4Qnun8-WfE?si=4zsKicBg2dkS9Vfi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
Once the simluation was complete, we were given physical hardware to implement. Alongwith that we were provided with an overhead camera, RGB LED as beacon and we used WayCon Marker to locate drone through the camera after its calibration.</p>

<p style="text-align: justify">
In the final task a random sequence was given for three colors, each indicating a specific service with a priority level. There were three colors:</p>
- Red - Rescue
- Green - Food
- Blue - Medicine


<p style="text-align: justify">
Highest priority was given to Rescue (Red) but to accomplish that the drone has to visit homing position after the service. Second priority was given to Medicine (Blue) and last one to Food (Green). I alongside my team first tuned the PID algorithm for the physical drone and later on developed a pre-emptive schedluing algorithm. Overall it was a rewarding experience filled with sleepless nights and managing exams with task submission deadlines. One hardship I faced was that the team constituted of four individuals but half way through we were just two remaining.</p>



<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/91-KuGHN9CY?si=PXUnFKIFkjv-0yfb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
This was my first thorough experience working with ROS. Even with the challenges our team managed to rank 6th nationwide. I am grateful to eYantra for providing me this opportunity and especially to Prof. Kavi Arya, the man behind the initiative.</p>
