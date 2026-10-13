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

*Overall machine concept and arrangement of the planting rows and greenhouse arches.*

<table>
<tr>
<td width="50%"><img src="images/jingan_white.png" alt="Rod feeding mechanism CAD design"><br><sub>Rod storage and feeding mechanism</sub></td>
<td width="50%"><img src="images/qianchazhuangzhi_white.png" alt="Arch insertion mechanism"><br><sub>Arch forming and insertion mechanism</sub></td>
</tr>
</table>

<!-- COMPONENTS_INSERTION_START -->
<details>
<summary>View components — Rod Insertion Mechanism Components</summary>

| No. | Component |
|---|---|
| 1 | Vertical Transfer Frame |
| 2 | Pneumatic Cylinder |
| 3 | Arch Forming Cavity |
| 4 | Rod Gripping End-Effector |
| 5 | Greenhouse Support Rod |

</details>
<!-- COMPONENTS_INSERTION_END -->


<!-- COMPONENTS_FEEDING_START -->
<details>
<summary>View components — Rod Feeding Mechanism Components</summary>

| No. | Component |
|---|---|
| 1 | Rod Alignment Plate |
| 2 | Support Rod |
| 3 | Gear Reducer |
| 4 | Grooved Wheel |
| 5 | Stepper Motor |

</details>
<!-- COMPONENTS_FEEDING_END -->


<!-- COMPONENTS_MACHINE_START -->
<details>
<summary>View components — Overall Machine Components</summary>

| No. | Component |
|---|---|
| 1 | Mulch Film |
| 2 | Greenhouse Support Rod |
| 3 | Crops |
| 4 | Rod Guiding Device |
| 5 | Tripod |
| 6 | RTK Positioning System |
| 7 | Rod Transfer Frame |
| 8 | Load-Carrying Platform |
| 9 | Wheel Drive Motor |
| 10 | Rod Holding End-Effector |
| 11 | Control System |
| 12 | Plastic Molding Cavity |
| 13 | Machine Frame |
| 14 | Air Pump |

</details>
<!-- COMPONENTS_MACHINE_END -->


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
