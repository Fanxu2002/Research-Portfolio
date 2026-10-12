# Kiwifruit Pollination Robot

**Mechanical Design · Creo CAD · Prototype Integration · LiDAR Localization**  
*Undergraduate project | Northwest A&F University*

This project explored a tracked robotic platform for precision pollination in kiwifruit orchards. The system combined a UR5 robotic arm, a pollination end-effector, onboard sensing, and a mobile base for field operation.

My main contributions were **mechanical design with Creo**, the design and **3D printing of mounting components** for the nozzle and other hardware, **real-time robot localization work using Livox MID-70 LiDAR**, and **annotation of kiwifruit flowers** for computer-vision experiments. The overall robot and control architecture were developed as part of a team project.

## Prototype and Mechanical Design

![CAD view of the robotic pollination platform](images/robot-cad-assembly.jpeg)

*Robot system CAD overview, showing the integrated arm, sensors, and tracked platform.*

![Field prototype of the robot](images/robot-field-prototype.jpeg)

*Assembled robot during orchard experiments.*

I worked on Creo-based component modeling, mechanical layout, mounting solutions, and prototype integration. Several fixtures, including nozzle-related mounts, were fabricated using 3D printing.

<table>
<tr>
<td width="50%"><img src="images/pollination-nozzle.jpeg" alt="Pollination nozzle and actuator assembly"><br><sub>Pollination end-effector detail</sub></td>
<td width="50%"><img src="images/lidar-and-robot-arm.jpeg" alt="LiDAR and robot arm integration"><br><sub>Robot arm and sensor integration</sub></td>
</tr>
</table>

## Mechanical Workspace

<table>
<tr>
<td width="50%"><img src="images/cad-working-area.jpeg" alt="Mechanical operating envelope"><br><sub>CAD workspace analysis</sub></td>
<td width="50%"><img src="images/robot-arm-workspace.jpeg" alt="Arm movement quadrants"><br><sub>Arm operating regions</sub></td>
</tr>
</table>

## LiDAR Localization and Field Experiments

I explored real-time localization of the mobile robot using **Livox MID-70 LiDAR**, in support of operation in the repetitive structure of kiwifruit orchards.

![Kiwifruit orchard field site](images/orchard-layout.jpg)

*Representative orchard environment and row geometry.*

## Kiwifruit Flower Annotation

I also annotated kiwifruit flowers in orchard imagery for visual detection experiments.

![Annotated flowers](images/flower-detection-examples.jpeg)

*Example images showing flower detection annotations; this figure is not presented as a stand-alone model performance evaluation.*

## Additional Materials

![Robot System and Control Architecture](images/control-system-diagram.jpeg)

<!-- SLAM_DEMO_START -->
## LiDAR Localization Demo

Real-time LiDAR localization using the Livox MID-70 sensor.

<video src="videos/slam.mp4" controls width="100%"></video>

[Watch the demonstration](videos/slam.mp4)
<!-- SLAM_DEMO_END -->
