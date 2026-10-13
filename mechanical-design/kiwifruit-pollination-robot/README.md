# Kiwifruit Pollination Robot

**Mechanical Design · Creo CAD · 3D Printing · LiDAR SLAM**  
*Undergraduate Project | Northwest A&F University*

## Project Overview

Pollination is essential for kiwifruit production, influencing fruit set and yield. However, kiwifruit flowers have a relatively short blooming period, leaving farmers with a limited window to complete pollination. Manual pollination is labor-intensive, time-consuming, and costly, especially in large orchards.

To address these challenges, our team developed a robotic pollination system for kiwifruit orchards. The system combines a UR5 robotic arm, a pollination end-effector, a tracked mobile base, and multiple sensors to support field operations.

My contributions focused on **mechanical design using Creo**, **designing and 3D-printing mounting components** for the pollination nozzle and other hardware, **LiDAR-based localization using the Livox MID-70**, and **flower image annotation** for computer vision experiments. The overall system was developed collaboratively by the project team.

## Mechanical Design and Prototyping

The mechanical design focused on integrating the robotic arm, sensors, pollination components, and supporting hardware into a mobile platform suitable for orchard environments.

![CAD model of the kiwifruit pollination robot](images/robot-cad-assembly.jpeg)

*Overall CAD model showing the robot's mechanical structure, UR5 robotic arm, sensor arrangement, and pollination system.*

![Assembled kiwifruit pollination robot](images/robot-field-prototype.jpeg)

*The assembled robot during field experiments in a kiwifruit orchard.*

I worked on component modeling and mechanical layout in Creo, as well as the design and fabrication of mounting fixtures. Several customized components, including brackets for the pollination nozzle, were produced using 3D printing and integrated into the robot.

<table>
<tr>
<td width="50%"><img src="images/pollination-nozzle.jpeg" alt="Pollination nozzle assembly"><br><sub>Pollination end-effector and mounting structure</sub></td>
<td width="50%"><img src="images/lidar-and-robot-arm.jpeg" alt="Robot arm and LiDAR integration"><br><sub>Robotic arm and sensor integration</sub></td>
</tr>
</table>

## Mechanical Workspace

The operating workspace of the robotic arm and pollination end-effector was examined to understand their reach and movement relative to the kiwifruit trellis structure.

<table>
<tr>
<td width="50%"><img src="images/cad-working-area.jpeg" alt="Robot working envelope"><br><sub>CAD analysis of the working envelope</sub></td>
<td width="50%"><img src="images/robot-arm-workspace.jpeg" alt="Robot arm operating regions"><br><sub>Robotic arm operating regions</sub></td>
</tr>
</table>

## Control System Architecture

The robot integrates a UR5 robotic arm, Livox MID-70 LiDAR, an RGB-D camera, an industrial computer, and a PLC-based control system. Together, these components support perception, motion control, and operation of the pollination mechanism.

![Robot control system architecture](images/control-system-diagram.jpeg)

*Overview of the control and sensing architecture developed by the project team.*

## LiDAR SLAM and Field Experiments

I also worked on LiDAR-based localization using the **Livox MID-70**, exploring how the robot could estimate its position while operating in kiwifruit orchards. The repetitive structure of orchard rows makes localization particularly challenging.

![Kiwifruit orchard environment](images/orchard-layout.jpg)

*The orchard environment used for field experiments, showing the trellis structure and approximate dimensions.*

[Watch the LiDAR SLAM video](videos/slam.mp4)

## Kiwifruit Flower Annotation

As part of the computer vision work, I annotated kiwifruit flowers in orchard images to support the development and evaluation of flower detection methods.

![Kiwifruit flower annotations](images/flower-detection-examples.jpeg)

*Examples of annotated kiwifruit flowers in orchard images.*

## Robot Working Demonstration

The following video shows the assembled robot operating during field experiments in a kiwifruit orchard.

[Watch the robot working video](videos/working%20video.mp4)
