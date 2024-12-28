---
title: "Botlab"
collection: research
---

<p style="text-align: justify">
The BotLab project was part of the ROB 550 curriculum in Fall 2023, focusing on the autonomy of a differential-drive ground robot, the MBot. The project encompassed fundamental robotics concepts such as motion control, perception, localization, mapping, and planning. By integrating these modules, I developed a fully autonomous robot capable of navigating and interacting with its environment.</p>

<h2>Project Objectives</h2>
* <b>Acting</b>: Implemented motion control strategies, including PID controllers and trajectory-following algorithms for precise navigation.
* <b>Sensing</b>: Utilized sensors like quadrature encoders, a 2D LiDAR, an IMU, and a camera for environment perception and robot localization.
* <b>Reasoning</b>: Developed algorithms for Monte Carlo Localization (MCL), simultaneous localization and mapping (SLAM), and path planning.

<h2>Implementation Methodology</h2>
<ol>
<h3><li>Motion Control Odometry: </li></h3>
    <ul>
    <li>Designed and tuned a PID controller for precise wheel speed control and body velocity adjustments.</li>
    <li>Implemented an odometry module using encoder and IMU data to estimate the robot's position and orientation through dead reckoning.</li>
    <li>Developed a motion controller to execute paths between waypoints, ensuring smooth transitions and maintaining trajectory accuracy.</li>
    </ul>

<p style="text-align:center">
<img src='/images/projects/botlab/run.png'></p>

<h3><li>Vision and Camera Integration</li></h3>
    <ul>
    <li>Calibrated the camera for intrinsic and extrinsic parameters, enabling accurate mapping between image and world coordinates.</li>
    <li>Utilized AprilTags for obstacle detection, distance estimation, and visual servoing to align the robot with targets.</li>
    </ul>

<h3><li>Simultaneous Localization and Mapping (SLAM)</li></h3>
    <ul>
    <li>Implemented an occupancy grid mapping algorithm using LiDAR data and ground-truth poses.</li>
    <li>Developed a Monte Carlo Localization (MCL) module to estimate the robot’s pose within a known map using a particle filter.</li>
    <li>Combined localization and mapping into a robust SLAM system, enabling real-time environment mapping and navigation.</li>
    </ul>

<p style="text-align:center">
<img src='/images/projects/botlab/map.png'></p>

<h3><li>Path Planning</li></h3>
    <ul>
    <li>Built an A* path planner to compute optimal paths through a mapped environment.</li>
    <li>Implemented obstacle avoidance strategies and ensured smooth execution of planned paths using a motion controller.</li>
    <li>Designed an exploration algorithm to autonomously navigate and map unknown environments by identifying unexplored frontiers.</li>
    </ul>

<h3><li>Lifting Mechanism Design</li></h3>
    <ul>
    <li>Designed and prototyped a gripper mechanism to lift and place targets.</li>
    <li>Integrated gripper control with the MBot's motion system to complete pick-and-place tasks.</li>
    </ul>
</ol>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/YL5bH4rEbHw?si=1NFtHVwvR5SVt99D" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<h3>Results and Challenges</h3>
* <b> Maze Eploration </b>: Successfully mapped a maze, returned to the starting pose, and achieved high accuracy in map quality.
* <b> Warehouse Task </b>: Completed the pick-and-place challenge by retrieving and placing multiple targets within time constraints.