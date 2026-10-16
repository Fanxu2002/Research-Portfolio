# Intelligent Greenhouse Arch Support Insertion Machine

**Mechanical Design · Automated Rod Feeding · Material Testing · ANSYS Simulation**  
*Undergraduate team project | Northwest A&F University | Robotic competition project*

## Project Overview

Small plastic tunnels are widely used in agriculture to protect crops, improve growing conditions, and extend the growing season. Their frames are commonly formed by bending flexible support rods into arches and inserting both ends into the soil.

Installing these arches manually involves repeatedly picking up rods, bending them, positioning them along planting rows, and pushing them into the ground. The process can be physically demanding and time-consuming, especially over large planting areas where consistent spacing and insertion depth are important.

To address these challenges, our team developed an **intelligent greenhouse arch support insertion machine** that integrates rod storage, sequential feeding, arch forming, and soil insertion on a mobile platform. In addition to mechanical design and prototype fabrication, the project investigated the strength of candidate support-rod materials and the structural response of greenhouse arches to lateral wind loads.

The project aimed to **reduce repetitive manual work, improve the consistency of arch installation, and provide an engineering basis for material selection and insertion-depth design**.

## My Contributions

My main responsibilities in this undergraduate team project were **mechanical structure design, prototype fabrication and assembly, material mechanical testing and analysis, and finite element analysis (FEA) of greenhouse arches under lateral wind loading**.

- **Mechanical design:** Developed the mechanical structure and worked on the rod feeding, arch-forming, and insertion mechanisms.
- **Prototype fabrication:** Worked on manufacturing, assembling, and integrating the machine's mechanical components.
- **Material testing and analysis:** Evaluated fiberglass and PTFE rods using shear, axial compression, and bending tests, and analyzed the experimental results to support material selection.
- **Finite element analysis:** Used ANSYS to study the wind resistance of the arch structure and assess the effect of support-rod insertion depth.

The **control system and autonomous driving/navigation functions** were handled by other team members. The complete machine was developed collaboratively.

## 1. Mechanical Structure and Working Principle

### 1.1 Overall Mechanical Design

The machine integrates a mobile chassis, a rod storage and feeding unit, a rod transfer and gripping assembly, an arch-forming guide, and a vertical insertion mechanism. Its main operating sequence is **rod feeding → pickup and gripping → arch forming → transfer → insertion into soil**. This arrangement supports repeated installation of small-tunnel arches along a planting row.

<table align="center">
<tr>
<td align="center" valign="middle">
<img src="images/jigou_white.png" alt="Overall mechanical design" width="420"><br>
<sub>Overall CAD assembly showing the machine, planting rows, and greenhouse arches.</sub>
</td>
<td align="center" valign="middle">
<img src="images/working.gif" alt="Working process demonstration" width="320"><br>
<sub>Working process demonstration.</sub>
</td>
</tr>
</table>

<details>
<summary>View components — Overall machine (1–14)</summary>

| No. | Component | No. | Component |
|---:|---|---:|---|
| 1 | Mulch film | 8 | Load-carrying platform |
| 2 | Greenhouse support rod | 9 | Wheel hub motor |
| 3 | Crops | 10 | Rod-gripping end effector |
| 4 | Rod guide device | 11 | Control system |
| 5 | Tripod | 12 | Plastic forming cavity |
| 6 | RTK positioning system | 13 | Machine frame |
| 7 | Rod transfer gantry | 14 | Air pump |

</details>

### 1.2 Key Mechanisms

<table>
<tr>
<td width="50%" valign="top">

<strong>Rod Feeding Mechanism</strong>

<p>The inclined guide plate directs stored rods toward a grooved wheel. A stepper motor and reducer rotate the wheel to advance the rods sequentially toward the pickup position.</p>

<img src="images/jingan_white.png" alt="Rod storage and grooved-wheel feeding mechanism" width="100%">

<details>
<summary>View feeding components (1–5)</summary>
<table>
<tr><th>No.</th><th>Component</th></tr>
<tr><td>1</td><td>Rod alignment plate</td></tr>
<tr><td>2</td><td>Support rod</td></tr>
<tr><td>3</td><td>Gear reducer</td></tr>
<tr><td>4</td><td>Grooved wheel</td></tr>
<tr><td>5</td><td>Stepper motor</td></tr>
</table>
</details>

</td>
<td width="50%" valign="top">

<strong>Arch Forming and Insertion Mechanism</strong>

<p>After pickup, the rod is gripped and shaped around a forming guide. The transfer and vertical-motion assemblies bring the formed arch to its insertion position and press its ends into the soil.</p>

<img src="images/qianchazhuangzhi_white.png" alt="Arch forming and soil-insertion mechanism" width="100%">

<details>
<summary>View insertion components (1–5)</summary>
<table>
<tr><th>No.</th><th>Component</th></tr>
<tr><td>1</td><td>Vertical transfer frame</td></tr>
<tr><td>2</td><td>Pneumatic cylinder</td></tr>
<tr><td>3</td><td>Arch-forming cavity</td></tr>
<tr><td>4</td><td>Rod-gripping end effector</td></tr>
<tr><td>5</td><td>Greenhouse support rod</td></tr>
</table>
</details>

</td>
</tr>
</table>

### 1.3 Mechanism Demonstrations

<table>
<tr>
<td width="50%" valign="top"><img src="images/jingan.gif" alt="Rod feeding mechanism operating" width="100%"><br><sub>Rod feeding and positioning.</sub></td>
<td width="50%" valign="top"><img src="images/qiancha.gif" alt="Arch support gripping and insertion mechanism operating" width="100%"><br><sub>Gripping and insertion mechanism.</sub></td>
</tr>
</table>

## 2. Support Rod Material Testing

Fiberglass and polytetrafluoroethylene (**PTFE**) rods were evaluated as candidate greenhouse support materials. The project used **shear, axial compression, and bending tests**, with three repetitions per condition, to compare load-bearing behavior and mechanical strength.

### 2.1 Experimental Setup

<table>
<tr>
<td width="33%"><img src="images/jianqieshiyan.png" width="100%" alt="Shear testing setup"><br><sub>Shear test</sub></td>
<td width="33%"><img src="images/yasuoshiyan.png" width="100%" alt="Axial compression testing setup"><br><sub>Axial compression test</sub></td>
<td width="33%"><img src="images/wanqushiyan.png" width="100%" alt="Bending testing setup"><br><sub>Bending test</sub></td>
</tr>
</table>

### 2.2 Load–Displacement Results

Each curve compares **three repeated tests** (rather than three materials). The two columns below correspond to the two candidate rod materials. The images retain the original (a)–(f) labels from the project figures.

| Test | Fiberglass | PTFE |
|---|---|---|
| **Shear** | <img src="images/a.png" width="100%" alt="Fiberglass shear load-displacement curves"> | <img src="images/b.png" width="100%" alt="PTFE shear load-displacement curves"> |
| **Axial compression** | <img src="images/c.png" width="100%" alt="Fiberglass compression load-displacement curves"> | <img src="images/d.png" width="100%" alt="PTFE compression load-displacement curves"> |
| **Bending** | <img src="images/e.png" width="100%" alt="Fiberglass bending load-displacement curves"> | <img src="images/f.png" width="100%" alt="PTFE bending load-displacement curves"> |

### 2.3 Material Comparison

| Average strength | Fiberglass | PTFE |
|---|---:|---:|
| Shear strength | 151.27 MPa | 57.54 MPa |
| Bending strength | 952.94 MPa | 25.40 MPa |
| Compressive strength | 294.06 MPa | 161.69 MPa |

Fiberglass exhibited higher measured strength across all three tests and was selected for subsequent greenhouse support-rod structural analysis. The results inform **material selection under the tested conditions**, rather than establishing the performance of every possible fiberglass or PTFE product.

## 3. Wind Resistance and Insertion Depth Analysis

The selected fiberglass support rods were evaluated using **ANSYS finite element analysis**. The study examined the response of a greenhouse arch under lateral wind loading and investigated the influence of the rod insertion depth on its equivalent stress and elastic strain.

### 3.1 Finite Element Model

The analysis used material parameters reported for the fiberglass rods, including an elastic modulus of **14.864 GPa**, Poisson's ratio **0.22**, and shear modulus **6.091 GPa**. The reported design wind pressure was **252 N/m²**.

<p align="center"><img src="images/anasy.png" alt="ANSYS finite element meshing, stress, and deformation results" width="94%"></p>
<p align="center"><sub>Finite element model and selected ANSYS analysis results.</sub></p>

### 3.2 Selecting the Insertion Depth

The study compared rod insertion depths from **8 to 20 cm**. As the insertion depth increased, the simulated equivalent stress and elastic strain generally decreased. The improvement became less pronounced beyond approximately **13 cm**, which was selected as the target insertion depth for the studied geometry and loading conditions.

<p align="center"><img src="images/13cmxuanze.png" alt="Relationship between rod insertion depth, equivalent stress, and elastic strain" width="90%"></p>
<p align="center"><sub>Effect of insertion depth on the simulated structural response.</sub></p>

**Design outcome: 13 cm target soil insertion depth**, under the assumptions of the reported simulation. This is a project-specific design decision, not a universal installation depth for all soils or wind conditions.

## 4. Prototype and Field Demonstration

A physical prototype was assembled and used in field trials to examine machine operation and greenhouse arch installation. The photographs and demonstrations below show the relationship between the proposed mechanism and the realized machine.

<table>
<tr>
<td width="50%"><img src="images/yangji.png" alt="Assembled greenhouse arch insertion machine" width="100%"><br><sub>Prototype assembly.</sub></td>
<td width="50%"><img src="images/yangji%20tianjian.png" alt="Greenhouse arch insertion machine in the field" width="100%"><br><sub>Field prototype and installed arches.</sub></td>
</tr>
</table>

<p align="center"><img src="images/image83.gif" alt="Prototype moving in a field demonstration" width="48%"></p>
<p align="center"><sub>Field mobility demonstration.</sub></p>

---

*Project documentation: Figures and numerical results are based on the team’s project materials and associated mechanical design and experimental study. Control and autonomous driving were developed by other team members.*
