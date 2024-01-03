---
title: "ROS Rover"
excerpt: "Proposal for ROS Based Rover for Robofest 2.0 <br/><img src='/images/projects/ros_rover/sa_pv.jpg'>"
collection: projects
---

<p style="text-align: justify">
Robofest, an annual project competition organized by GUJCOST, provided me with an exciting opportunity during my sophomore year. I embarked on a journey to create a captivating project proposal for a ROS based Rover.</p>

The competition had a three-phase structure:
1. **Phase-1**: Develop a Proof of Concept (PoC)
2. **Phase-2**: Develop a Minimum Viable Product (MVP)
3. **Phase-3**: Develop a Full-Fledged System

<p style="text-align: justify">
I chose to focus on the development of a ROS-based Rover for my project, with guidance from Dr. Avani R. Vasant, the Head of the Department of Computer Science and Engineering at BITs EDU Campus. Since this was my first time, our initial step was to submit the proposal and then assemble the team upon selection.</p>

<p style="text-align: justify">
In terms of software, I opted for the Robot Operating System (ROS) due to my prior experience with it. ROS proved to be an ideal choice for both rapid prototyping and the creation of industry-grade software.</p>

<p style="text-align: justify">
The project wasn't just about simulation; it also involved building two physical rovers. To tackle this complex task, I broke down the entire system into smaller, manageable subsystems as follow:</p>

<p style="text-align:center">
<img src='/images/projects/ros_rover/sf.png'></p>

<p style="text-align: justify">
1. <b>Drive System</b>: This system allowed manual control of the rover by a human operator and could override autonomous control in emergencies. I considered using a joystick package from ROS to send velocity commands to the rover.</p>

<p style="text-align: justify">
2. <b>Visual Feedback System</b>: This system was all about seeing what the rover sees. Here, the RViz package from ROS came to the rescue. The BL170 camera provided a real-time stream over RTSP, ensuring low-latency transmission.</p>

<p style="text-align: justify">
3. <b>GPS System</b>: Although part of the Autonomous System, it was worth explaining separately. GPS data was used for monitoring long-distance tasks and providing visualization feedback on MapViz. Additionally, it enabled us to set goals on the map, which the rover could then execute.</p>

<p style="text-align: justify">
4. <b>Autonomous System</b>: The heart of the project, this system guided the rover to reach and execute goals. The rover featured a depth camera to avoid obstacles in its path, LiDAR for mapping and navigation, and a tracking camera for recalibrating LiDAR in case of false localization. The IMU played a crucial role in keeping the rover's motion in check.</p>

<p style="text-align: justify">
5. <b>Odometry System</b>: This system received feedback from the motors when velocity commands were issued by either the Autonomous System or the Drive System. Using tick odometry, the motors were controlled more efficiently.</p>

<p style="text-align: justify">
6. <b>Navigation Stack</b>: When a specific task was assigned to the rover, it would map the environment on the fly if the map wasn't already available. The Cost Map included an obstacle layer for dynamic obstacles and a static layer for objects expected to remain stationary. The Global planner generated the overall path, while the local planner was continually adapted for shorter durations.</p>

<p style="text-align: justify">
Regarding hardware, we considered two flow diagrams. The major differences revolved around the power of actuators, the number of sensors, and the single-board computer in use.</p>

<p style="text-align:center">
<img src='/images/projects/ros_rover/hw.jpg'></p>

<p style="text-align: justify">
Though I didn't qualify for the next round, I learnt how to design system and software architecture for robotics systems - Rovers.</p>
