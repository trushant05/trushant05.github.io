---
title: "Jetson Mate Cluster"
collection: projects
---

<p style="text-align: justify">
The Jetson Mate, designed by Seeed Studio, is a cluster computer capable of hosting up to four Jetson modules. Whether you're working with the Jetson Nano 2GB, the 4GB version, or the powerful Jetson NX, the Jetson Mate provides a versatile platform for delving into parallel computing.</p>

<p style="text-align:center">
<img src='/images/projects/jetson_mate/IMG_20230117_163425.jpg'></p>

<h2>The Hunt for Jetson Modules</h2>
<p style="text-align: justify">
My journey with the Jetson Mate began with two Jetson modules in hand and a mission to find two more. The timing was challenging, as Nvidia had recently discontinued the Jetson Nano SD series. However, serendipity struck at the ROS Developer Summit in Pune, organized by Rigbetel Lab. With the help of my friend Pranshu Tople, I secured two additional Jetson Nano modules, completing my cluster setup.</p>

<h2>Preparing the Jetson Cluster</h2>
<p style="text-align: justify">
The first step was synchronizing all four Jetson Nano boards by installing the same JetPack version (4.6) and giving each module a unique name and incremental IP address for easy identification.</p>

<p style="text-align:center">
<img src='/images/projects/jetson_mate/jetson_stat.png'></p>

<h2>Testing and Configuration</h2>
<p style="text-align: justify">
With the hardware ready, I tested each module using the Jetson Mate's convenient USB 3.0 ports for serial communication. To streamline the setup, I created a configuration script for setting up a Kubernetes cluster, laying the groundwork for future load balancing experiments.</p>

<h2>Building the Clusters</h2>
<p style="text-align: justify">
To enable seamless communication, I configured each module with an SSH key. Here’s how the cluster was organized:</p>

* <b>Master Node</b>: Jetson Nano 4GB
* <b>Node 1</b>: Jetson Nano 4GB
* <b>Node 2</b>: Jetson Nano 2GB
* <b>Node 3</b>: Jetson Nano 2GB

<p style="text-align: justify">
This setup allowed me to log into each node effortlessly. Using the master node as the command center, I conducted benchmarking tests and monitored the system.</p>

<h2>Racing Against Time</h2>
<p style="text-align: justify">
With only four hours before my train departure, I had to conclude the initial phase of my exploration. But this was just the beginning. In the next phase, I plan to attach a camera to the master node to capture image frames or stream video via GStreamer. This feed will be distributed across the three nodes, where each will run dedicated vision algorithms such as color detection, object detection, and overlapping inference. The goal is to achieve a synchronized output, showcasing the true potential of parallel computing.</p>

<h2>Stay Tuned!</h2>
<p style="text-align: justify">
The Jetson Mate has opened the door to exciting possibilities in parallel computing. As I continue this journey, I’ll share updates and insights on leveraging this powerful cluster computer for real-world applications. Stay tuned for the next chapter! </p>