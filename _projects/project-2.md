---
title: "ROS Rover"
collection: projects
---

<p style="text-align: justify">
During my sophomore year, I participated in <b>Robofest</b>, an annual project competition organized by <b>GUJCOST</b>, where I proposed and developed a <b>ROS-based Rover</b> under the guidance of <b>Dr. Avani R. Vasant</b> from BITs EDU Campus. This competition involved three phases:</p>

1. **Phase-1**: Develop a Proof of Concept (PoC)
2. **Phase-2**: Develop a Minimum Viable Product (MVP)
3. **Phase-3**: Develop a Full-Fledged System

<p style="text-align: justify">
In terms of software, I opted for the Robot Operating System (ROS) due to my prior experience with it. ROS proved to be an ideal choice for both rapid prototyping and the creation of industry-grade software.</p>

<p style="text-align: justify">
To tackle this complex task, I broke down the entire system into smaller, manageable subsystems as follow:</p>

<p style="text-align:center">
<img src='/images/projects/ros_rover/sf.png'></p>

1. <p style="text-align: justify">
<b>Drive System</b>: This system allowed manual control of the rover by a human operator and could override autonomous control in emergencies. I considered using a joystick package from ROS to send velocity commands to the rover.</p>

2. <p style="text-align: justify">
<b>Visual Feedback System</b>: This system was all about seeing what the rover sees. Here, the RViz package from ROS came to the rescue. The BL170 camera provided a real-time stream over RTSP, ensuring low-latency transmission.</p>

3. <p style="text-align: justify">
<b>GPS System</b>: Although part of the Autonomous System, it was worth explaining separately. GPS data was used for monitoring long-distance tasks and providing visualization feedback on MapViz. Additionally, it enabled us to set goals on the map, which the rover could then execute.</p>

4. <p style="text-align: justify">
<b>Autonomous System</b>: The heart of the project, this system guided the rover to reach and execute goals. The rover featured a depth camera to avoid obstacles in its path, LiDAR for mapping and navigation, and a tracking camera for recalibrating LiDAR in case of false localization. The IMU played a crucial role in keeping the rover's motion in check.</p>

5. <p style="text-align: justify">
<b>Odometry System</b>: This system received feedback from the motors when velocity commands were issued by either the Autonomous System or the Drive System. Using tick odometry, the motors were controlled more efficiently.</p>

6. <p style="text-align: justify">
<b>Navigation Stack</b>: When a specific task was assigned to the rover, it would map the environment on the fly if the map wasn't already available. The Cost Map included an obstacle layer for dynamic obstacles and a static layer for objects expected to remain stationary. The Global planner generated the overall path, while the local planner was continually adapted for shorter durations.</p>

<p style="text-align: justify">
For hardware, I explored two distinct flow diagrams, differing primarily in actuator power, sensor configurations, and the choice of single-board computers, tailored to meet the project's requirements.</p>

<p style="text-align:center">
<img src='/images/projects/ros_rover/hw.jpg'></p>

<p style="text-align: justify">
Although I did not advance to the next round, the experience provided invaluable insights into designing system and software architectures for robotics systems, particularly Rovers.</p>
