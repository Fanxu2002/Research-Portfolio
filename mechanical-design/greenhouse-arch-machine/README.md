# Intelligent Greenhouse Arch Support Insertion Machine

**Mechanical Design · Material Testing · ANSYS Simulation · Field Prototype**  
*Undergraduate Engineering Project | Northwest A&F University*  
*25th China Robot and Artificial Intelligence Competition*

## Project Overview

Building small greenhouse tunnels requires repeated placement, bending, and insertion of flexible support rods. Doing this manually can be time-consuming and physically demanding, especially when many arches must be installed at consistent spacing and depth.

Our team developed a mobile machine designed to automate rod feeding, arch forming, and support-rod insertion. This page presents the **mechanical design**, **material characterization**, **wind-resistance analysis**, and **prototype demonstrations** from the project.

## 1. Mechanical Design and Operating Principle

The machine integrates a mobile frame, rod storage and feeding components, an arch-forming mechanism, and an insertion device. Its operating sequence moves a support rod from storage, advances it into position, and inserts the formed arch into the soil.

<p align="center"><img src="images/jigou_white.png" alt="Overall machine CAD" width="85%"></p>

<!-- COMPONENTS_MACHINE_START -->
<details>
<summary>View components — Overall Machine Components</summary>
<table>
<tr><th>No.</th><th>Component</th></tr>
<tr><td>1</td><td>Mulch Film</td></tr>
<tr><td>2</td><td>Greenhouse Support Rod</td></tr>
<tr><td>3</td><td>Crops</td></tr>
<tr><td>4</td><td>Rod Guiding Device</td></tr>
<tr><td>5</td><td>Tripod</td></tr>
<tr><td>6</td><td>RTK Positioning System</td></tr>
<tr><td>7</td><td>Rod Transfer Frame</td></tr>
<tr><td>8</td><td>Load-Carrying Platform</td></tr>
<tr><td>9</td><td>Wheel Drive Motor</td></tr>
<tr><td>10</td><td>Rod Holding End-Effector</td></tr>
<tr><td>11</td><td>Control System</td></tr>
<tr><td>12</td><td>Plastic Molding Cavity</td></tr>
<tr><td>13</td><td>Machine Frame</td></tr>
<tr><td>14</td><td>Air Pump</td></tr>
</table>
</details>
<!-- COMPONENTS_MACHINE_END -->


*Overall machine concept and arrangement of the planting rows and greenhouse arches.*

<table>
<tr>
<td width="50%" valign="top">

<img src="images/jingan_white.png" alt="Rod feeding mechanism CAD design">

<sub>Rod storage and feeding mechanism</sub>

<!-- COMPONENTS_FEEDING_START -->
<details>
<summary>View components — Rod Feeding Mechanism Components</summary>
<table>
<tr><th>No.</th><th>Component</th></tr>
<tr><td>1</td><td>Rod Alignment Plate</td></tr>
<tr><td>2</td><td>Support Rod</td></tr>
<tr><td>3</td><td>Gear Reducer</td></tr>
<tr><td>4</td><td>Grooved Wheel</td></tr>
<tr><td>5</td><td>Stepper Motor</td></tr>
</table>
</details>
<!-- COMPONENTS_FEEDING_END -->

</td>
<td width="50%" valign="top">

<img src="images/qianchazhuangzhi_white.png" alt="Arch insertion mechanism">

<sub>Arch forming and insertion mechanism</sub>

<!-- COMPONENTS_INSERTION_START -->
<details>
<summary>View components — Rod Insertion Mechanism Components</summary>
<table>
<tr><th>No.</th><th>Component</th></tr>
<tr><td>1</td><td>Vertical Transfer Frame</td></tr>
<tr><td>2</td><td>Pneumatic Cylinder</td></tr>
<tr><td>3</td><td>Arch Forming Cavity</td></tr>
<tr><td>4</td><td>Rod Gripping End-Effector</td></tr>
<tr><td>5</td><td>Greenhouse Support Rod</td></tr>
</table>
</details>
<!-- COMPONENTS_INSERTION_END -->

</td>
</tr>
</table>










### Mechanism Demonstrations

<table>
<tr>
<td width="50%"><img src="images/jingan.gif" alt="Rod feeding demonstration"><br><sub>Rod feeding mechanism</sub></td>
<td width="50%"><img src="images/qiancha.gif" alt="Arch insertion demonstration"><br><sub>Arch insertion operation</sub></td>
</tr>
</table>

## 2. Support Rod Material Testing

The project compared **fiberglass** and **polytetrafluoroethylene (PTFE)** support rods through shear, axial compression, and bending tests. Three experimental runs were conducted for each plotted test condition. The force–displacement curves show the response of the specimens as load was applied.

### Experimental Setup

![Shear test setup and specimen](images/jianqieshiyan.png)

*Shear testing: specimen setup and condition after failure.*

![Axial compression test setup and specimen](images/yasuoshiyan.png)

*Axial compression testing: specimen setup and condition after failure.*

![Bending test setup and specimen](images/wanqushiyan.png)

*Bending testing: specimen setup and condition after failure.*

### Force–Displacement Curves

| Fiberglass | PTFE |
|:--:|:--:|
| ![Shear test: fiberglass](images/a.png) | ![Shear test: PTFE](images/b.png) |
| **Shear** | **Shear** |
| ![Axial compression test: fiberglass](images/c.png) | ![Axial compression test: PTFE](images/d.png) |
| **Axial compression** | **Axial compression** |
| ![Bending test: fiberglass](images/e.png) | ![Bending test: PTFE](images/f.png) |
| **Bending** | **Bending** |

*The black dotted, red solid, and blue dashed curves represent the first, second, and third experimental runs, respectively.*

### Material Comparison

| Property | Fiberglass | PTFE |
|:--|--:|--:|
| Shear strength | 151.27 MPa | 57.54 MPa |
| Bending strength | 952.94 MPa | 25.40 MPa |
| Compressive strength | 294.06 MPa | 161.69 MPa |

*Average values reported in the project materials.* Fiberglass showed higher measured strength in all three tests and was selected as the support-rod material for the studied greenhouse design.

![Material strength comparison](images/cailiaoduibijieguo.png)

## 3. Wind Resistance and Insertion Depth

The mechanical properties of the selected fiberglass rods were used in an **ANSYS structural analysis** to examine how wind loading affects the greenhouse arch. The analysis considered how different insertion depths influence the structure's stress and deformation.

![Greenhouse arch under lateral wind loading](images/gongpengcemianchuizhi%20feng_white.png)

*Simplified greenhouse arch geometry and lateral wind-loading direction.*

![ANSYS structural simulation results](images/anasy.png)

*Finite-element model and representative stress/deformation results.*

![Comparison of insertion depths](images/13cmxuanze.png)

*Comparison of equivalent elastic strain and equivalent stress across the studied insertion depths.*

For the geometry and loading assumptions considered in the project, a support-rod insertion depth of approximately **13 cm (130 mm)** was selected. This is a project-specific design parameter, rather than a universal value for all soils or wind conditions.

## 4. Prototype and Field Demonstration

After mechanical design and analysis, the team assembled a working prototype and tested it in the field. The photographs and demonstrations below show the machine and its operation.

<table>
<tr>
<td width="50%"><img src="images/yangji.png" alt="Greenhouse arch machine prototype"><br><sub>Assembled prototype</sub></td>
<td width="50%"><img src="images/yangji%20tianjian.png" alt="Machine in agricultural field"><br><sub>Field prototype and installed greenhouse arches</sub></td>
</tr>
</table>

### Field Demonstration

![Field operation demonstration](images/image83.gif)

*Demonstration of the prototype in operation.*

---

*Figures, test results, and simulation results are from the project materials. The machine was developed as a team project.*
