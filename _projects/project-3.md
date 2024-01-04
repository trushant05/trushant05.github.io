---
title: "Jetson Mate Cluster"
excerpt: "Homogeneous Cluster Computer. <br/> <img src='/images/projects/jetson_mate/jm_pv.jpg'>"
collection: projects
---

<p style="text-align: justify">
Jetson Mate, designed by Seeed Studio, is a versatile cluster computer capable of accommodating up to four Jetson Modules. Whether it is a Jetson Nano 2GB, 4GB, or the powerful Jetson NX, this device is gateway to exploring the world of parallel computing.</p>

<p style="text-align:center">
<img src='/images/projects/jetson_mate/IMG_20230117_163425.jpg'></p>

<h2>A Quest for Jetson Modules</h2>
<p style="text-align: justify">
I embarked on this adventure with two Jetson Modules in hand, eager to find two more. My quest coincided with a critical moment - Nvidia had just discontinued the Jetson Nano SD series. But fortune smiled upon me when the ROS Developer Summit, organized by Rigbetel Lab in Pune, came to my rescue. Thanks to my good friend Pranshu Tople, I was able to secure the missing pieces – two additional Jetson Nano modules.</p>

<h2>Getting Started</h2>
<p style="text-align: justify">
My first task was to bring all four Jetson Nano Boards to the same page. I installed the same JetPack version (4.6) on each module and assigned them distinct names in a simple, iterative fashion. I also configured incremental IP addresses for easy identification.</p>

<p style="text-align:center">
<img src='/images/projects/jetson_mate/jetson_stat.png'></p>

<h2>Testing the Waters</h2>
<p style="text-align: justify">
Next, it was time to put them to the test. Jetson Mate provided a convenient solution with one USB 3.0 port per board, allowing me to establish serial communication and interact seamlessly. I even crafted a handy configuration script to set up a Kubernetes cluster, setting the stage for future load balancing experiments.</p>

<h2>Setting Up the Clusters</h2>
<p style="text-align: justify">
I ensured smooth communication between nodes by configuring each one with an SSH key. Here's the hardware setup I used:</p>

- Master Node: Jetson Nano 4GB
- Node 1: Jetson Nano 4GB
- Node 2: Jetson Nano 2GB
- Node 3: Jetson Nano 2GB

<p style="text-align: justify">
This setup allowed me to log into each node effortlessly. For a comprehensive view, I relied on the master node to perform benchmarking tests.</p>

<h2>The Countdown Begins</h2>
<p style="text-align: justify">
With a ticking clock and just four hours before my train departure, I had to wrap things up. But my journey with Jetson Mate was far from over. In my next phase, I planned to attach a camera to the master node. This camera would capture image frames or stream via GStreamer, distributing the feed to all three nodes. These nodes would then work their magic, executing dedicated vision algorithms like color detection, object detection, and overlapping inference to provide a synchronized output.</p>

Stay tuned as I continue to explore the world of parallel computing with Jetson Mate!
