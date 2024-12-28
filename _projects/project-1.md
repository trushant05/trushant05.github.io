---
title: "eYantra Robotics Competition 2019-20"
collection: projects
---

<p style="text-align: justify">
The <b>eYantra Robotics Competition</b> is a prestigious six-month event requiring teamwork, technical expertise, and innovative problem-solving. As part of a four-member team, our theme was <b>Survey and Rescue</b>, where we developed a <b>pre-emptive scheduling algorithm</b> for a drone to aid individuals affected by natural disasters.</p>

<p style="text-align: justify">
Our journey began with <b>Task 0</b>, setting up a simulation environment using <b>Gazebo, ROS Kinetic,</b> and <b>Ubuntu 16.04</b>, with <b>Python</b> as the primary implementation language. Subsequent tasks included:</p>

<p style="text-align: justify">
<b>Task 1.1</b> - Implementing <b>position hold</b> for the drone at a specific point [2, 2, 20] using a <b>PID control algorithm</b> in simulation.
</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/xRDrj8BBL4Y?si=0mCUtrI0Pf1qUYVv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
<b>Task 1.2</b> - Programming <b>waypoint navigation</b> for the drone to traverse a set of 3D coordinates using the PID controller. Waypoints are in the form (x, y, z).</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/p4Qnun8-WfE?si=4zsKicBg2dkS9Vfi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
After completing simulations, we transitioned to physical hardware, where we integrated an overhead camera, an RGB LED as a beacon, and a WayCon Marker for drone localization after camera calibration.</p>

<p style="text-align: justify">
In the final task, we tackled dynamic challenges involving <b>three priority-based services</b>:</p>
<ul>
 <li> <b>Red (Rescue)</b> - Highest priority, requiring the drone to return to the homing position after service. </li>
 <li> <b> Blue (Medicine)</b> - Medium priority. </li>
 <li> <b> Green (Food)</b> - Lowest priority. </li>
</ul>

<p style="text-align: justify">
To succeed, we fine-tuned the PID algorithm for the physical drone and developed a pre-emptive scheduling algorithm to manage tasks effectively.</p>

<p style="text-align: justify">
<iframe width="560" height="315" src="https://www.youtube.com/embed/91-KuGHN9CY?si=PXUnFKIFkjv-0yfb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: justify">
Despite unforeseen challenges—such as losing half of our team midway through the competition—we persevered and secured <b>6th place nationwide</b>. This project provided my first comprehensive experience with <b>ROS</b>, taught me resilience under pressure, and reinforced the value of teamwork. I remain deeply grateful to <b>eYantra</b> and <b>Prof. Kavi Arya</b> for this incredible learning opportunity.</p>
