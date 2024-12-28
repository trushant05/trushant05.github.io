---
title: "Armlab"
collection: research
---

<p style="text-align: justify">
The Armlab project, part of the ROB 550 curriculum in Fall 2023, was a comprehensive exploration into the autonomy of a 5-DOF robotic arm. The project involved implementing advanced computer vision, kinematics, and path-planning techniques. It culminated in a series of challenges where the robotic arm autonomously manipulated objects in its workspace. The project was not only a demonstration of robotics theory but also a practical test of implementation methodologies.</p>

<h2>Project Objectives</h2>
* <b>Acting</b>: Develop forward and inverse kinematics models for precise robotic arm movement and object manipulation.
* <b>Sensing</b>: Perform 3D camera calibration, object detection, and workspace mapping using depth sensors and computer vision algorithms.
* <b>Reasoning</b>: Design and implement state machines for automated task execution, integrating sensor data, and kinematics.

<h2>Implementation Methodology</h2>
<ol>
<li><h2>Forward and Inverse Kinematics (IK/FK): </h2></li>

<p style="text-align: justify">
<b>Forward Kinematics</b>:  Utilized the Denavit-Hartenberg (DH) parameterization to calculate the end-effector’s position and orientation. This involved defining the RX200 robotic arm’s geometry and solving transformation matrices to map joint angles to global coordinates.</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/hAnHlFvRkM4?si=iIb7y0iOv3Wy8oos" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<p style="text-align: justify">
<b>Inverse Kinematics</b>: Developed algorithms to compute joint angles from a desired end-effector position and orientation. The implementation included error handling for unreachable configurations and degenerate poses. </p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/ideIQyKmkjk?si=31MZQyy3GmKgdrmy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<li><h2>Automatic Camera Calibration with AprilTags</h2></li>

    <ul>
    <li>Leveraged AprilTags for camera extrinsic calibration. By detecting known AprilTag positions in the workspace, the system calculated the transformation matrix between the camera and the robot’s base frame.</li>

    <li>Applied projective transformations to rectify the workspace view, ensuring accurate mapping between image and world coordinates.</li>
    </ul>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/V8SBXsi8USc?si=8zo1kFTeT1C0KX1u" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<li><h2>Object Detection</h2></li>

    <ul>
    <li>Implemented a block detection algorithm using OpenCV. The algorithm identified block positions, shapes, and colors (red, green, blue, and more) using a combination of depth imaging and RGB image analysis.</li>

    <li>Enhanced robustness by filtering false positives and calibrating thresholds for color and depth consistency.</li>
    </ul>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/3wkHn5D2LIs?si=l2AEPqZb5J3BsQ9-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

<li><h2>Pick-and-Place Task</h2></li>

    <ul>
    <li>Designed a state machine to automate the pick-and-place process. The system integrated IK, FK, and camera data to:</li>
        <ul>
        <li>Detect blocks in the workspace.</li>
        <li>Plan and execute an approach trajectory.</li>
        <li>Grasp blocks using the gripper and move them to specified locations.</li>
        </ul>

    <li>Added functionality for "click-to-grab" and "click-to-drop," allowing users to interact with the system via GUI.</li>
    </ul>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/zv9TkZM83cg?si=n53WkRFMRgThxpqW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>

</ol>

<h2>Results and Challenges</h2>
* <b> Competitions </b>: Successfully participated in challenges such as sorting, stacking, and arranging blocks, achieving high accuracy and efficiency under time constraints.
* <b> Accuracy </b>: Verified FK/IK outputs using controlled test cases and calibrated camera data. Errors were minimized through iterative adjustments and robust algorithm design.
* <b> Future Improvements </b>: While the implementation was successful, enhancements in gripper design and motion smoothing could improve performance further.