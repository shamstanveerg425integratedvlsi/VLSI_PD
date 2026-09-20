<div align="center">

<img
  src="https://github.com/user-attachments/assets/88fa5098-24b1-4ece-87df-95eb920ea721"
  alt="SURE ProEd Logo"
  width="180"
/>

<h1>SURE ProEd</h1>

<h3>Skill Upgradation for Rural youth Empowerment Trust</h3>

<p><i>Formerly SURE Trust</i></p>

</div>

---

# Student Details

| Details | Information |
|---|---|
| **Name** | Shams Tanveer |
| **Email ID** | shamstanveer.g4.25.integratedvlsi@gmail.com |
| **College** | Narula Institute of Technology |
| **Branch / Specialization** | Electronics and Instrumentation / VLSI Physical Design |
| **College ID** | NIT/2022/1667 |

---

# Course Details

| Details | Information |
|---|---|
| **Course** | Physical Design (VLSI) |
| **Batch** | G4-25-VLSI |
| **Duration** | 6 Months |

---

# Mentor Details

| Details | Information |
|---|---|
| **Mentor** | Veeramani R |
| **Email** | veeramani_r@outlook.com |
| **Designation** | Staff Engineer - Synopsys Inc. |
| **Education** | MTech in VLSI - NITG \| MTech in AI - IISc |

---

# Table of Contents

- [Overall Learning](#overall-learning)
- [Projects Completed](#projects-completed)
- [Project 1](#project-1)
- [Project 2](#project-2)
- [Project 3](#project-3)
- [Technologies Used](#technologies-used)
- [Roles and Responsibilities](#roles-and-responsibilities)
- [Project Report](#project-report)
- [Learnings from LST and SST](#learnings-from-lst-and-sst)
- [Community Services](#community-services)
- [Certificate](#certificate)
- [Acknowledgments](#acknowledgments)
- [References](#references)

---

# Overall Learning

During this course, I gained practical knowledge of **VLSI Physical Design** and learned how an RTL design is taken through different stages of the **RTL-to-GDSII flow**.

I developed hands-on experience with:

- OpenLane
- OpenROAD
- SKY130 technology
- Linux commands
- TCL scripting
- Static Timing Analysis (STA)
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Routing
- Power analysis
- Area analysis
- IR-drop analysis

The course started with basic Linux and tool-environment learning and gradually progressed to physical-design implementation and analysis.

I worked on a **4-bit up/down counter** and later worked on a **32-bit RISC-V PicoRV32** design.

The assignments helped me understand how design constraints such as clock period, clock uncertainty, timing derate, utilization and floorplan parameters affect physical implementation.

Along with technical knowledge, the LST and SST sessions helped me improve my communication, confidence, teamwork, time management and professional skills.

---

# Projects Completed

| Project | Title |
|---|---|
| **Project 1** | OpenLane Environment, Linux Commands and TCL-Based Design Analysis |
| **Project 2** | 4-bit Up/Down Counter Physical Design |
| **Project 3** | 32-bit RISC-V PicoRV32 Physical Design |

---

# Project 1

## OpenLane Environment, Linux Commands and TCL-Based Design Analysis

### Project Introduction

The first assignment focused on understanding the OpenLane environment, Linux commands, VI editor, file permissions, text-processing commands and TCL scripting.

The objective was to become familiar with the environment required for VLSI Physical Design and to understand how reports and design data can be analyzed using command-line tools and TCL.

---

## Linux Commands

The following Linux commands were practiced:

| Command | Purpose |
|---|---|
| `pwd` | Display current directory |
| `ls` | List files and directories |
| `cd` | Change directory |
| `mkdir` | Create a directory |
| `rm` | Remove files |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `chmod` | Modify file permissions |
| `grep` | Search patterns in files |
| `awk` | Process and analyze structured text |

---

## VI Editor

The VI editor was used to edit configuration files and scripts.

Important commands practiced included:

- `i` – Insert mode
- `:w` – Save
- `:q` – Exit
- `:wq` – Save and exit
- `:q!` – Force quit

---

## TCL-Based Wire Length Analysis

Wire-length analysis was performed using available reports and OpenROAD.

| Parameter | Value |
|---|---:|
| Total Wire Length | 6716.82 |
| Clock Wire Length | 784.48 |
| Data Wire Length | 5932.34 |

This activity helped me understand the relationship between clock routing, data routing and total wire length.

---

## IR-Drop Analysis

IR-drop analysis was performed using signoff power reports.

The analysis used the SKY130 nominal supply voltage of **1.8 V**.

### Recorded Results

- Minimum voltage = **1.79972 V**
- Nominal VDD = **1.8 V**
- Worst IR Drop = **0.00028 V**
- Percentage degradation ≈ **0.0156%**

This helped me understand how voltage variation across the power distribution network is analyzed.

---

## Levels of Logic Analysis

TCL scripting was used to process timing reports and extract:

- Startpoint
- Endpoint
- Slack
- Levels of Logic (LoL)

### Example Results

| Path | Startpoint | Endpoint | Slack | LoL |
|---|---|---|---:|---:|
| 1 | `rst` | `__445__` | 7.78 ns | 6 |
| 2 | `__444__` | `p` | 6.86 ns | 3 |

This activity helped me understand how timing paths can be automatically analyzed using TCL scripts.

---

# Project 2

## 4-bit Up/Down Counter Physical Design

### Project Introduction

The second assignment involved implementing and analyzing a **4-bit up/down counter** using the OpenLane physical-design flow.

The design was taken through major stages including:

- Synthesis
- Floorplanning
- Placement
- Clock Tree Synthesis
- Routing
- Signoff analysis

---

## Maximum Operating Frequency

Different clock periods were tested to determine the maximum operating frequency.

| Clock Period | Timing Status | Observation |
|---:|---|---|
| 4 ns | PASS | Large positive slack |
| 3 ns | PASS | Timing closure achieved |
| 2 ns | FAIL | Negative slack |

The highest passing frequency was obtained at a **3 ns clock period**.

Using:

```text
f = 1/T
```

Therefore:

```text
f = 1 / (3 × 10⁻⁹)
```

### Maximum Operating Frequency: 333.33 MHz

The design failed timing closure at a 2 ns clock period because negative slack was observed.

---

## Timing Parameters

| Parameter | Value |
|---|---:|
| Clock Uncertainty | 0.25 ns |
| Early Timing Derate | 0.95 |
| Late Timing Derate | 1.05 |

---

## Power Analysis

Power was analyzed at different stages of the physical-design flow.

| Stage | Total Power |
|---|---:|
| Synthesis | 1.58 × 10⁻⁴ W |
| Placement | 1.63 × 10⁻⁴ W |
| CTS | 3.62 × 10⁻⁴ W |
| Global Routing | 3.56 × 10⁻⁴ W |
| Routing Timing | 3.71 × 10⁻⁴ W |
| Signoff RCX_MAX | 4.31 × 10⁻⁴ W |

### Maximum Reported Signoff Power

**4.31 × 10⁻⁴ W**

---

## Area and Utilization

| Parameter | Value |
|---|---:|
| Synthesis Chip Area | 257.7472 µm² |
| Placement Area | 1268.7168 µm² |
| Routing Area | 1268.7168 µm² |
| Final Die Area | 0.0027065604 mm² |
| Core Area | 1268.7168 µm² |
| Utilization | 22.37% |
| Cell Density | 59115.62 |
| Cell Count/mm² | 11823.12 |

---

## Floorplan Analysis

The core dimensions were measured using OpenROAD TCL commands.

| Parameter | Value |
|---|---:|
| Core LLX | 5520 DBU |
| Core LLY | 10880 DBU |
| Core URX | 41400 DBU |
| Core URY | 46240 DBU |
| Core Width | 35880 DBU |
| Core Height | 35360 DBU |

### Die Dimensions

| Parameter | Value |
|---|---:|
| Die Width | 46940 DBU |
| Die Height | 57660 DBU |

---

## Physical-Only Cells

The following physical-only cells were identified:

- `sky130_fd_sc_hd__decap_3`
- `sky130_fd_sc_hd__tapvpwrvgnd_1`

Decap cells help improve power-supply stability, while tap cells provide substrate and well connections.

---

## Placement Analysis

Buffers, inverters, flip-flops, site rows and standard-cell dimensions were analyzed during placement.

### Placement Site

| Parameter | Value |
|---|---:|
| Site Name | `unithd` |
| Site Width | 460 DBU |
| Site Height | 2720 DBU |

### Example Library Cells

| Library Cell | Width (DBU) | Height (DBU) |
|---|---:|---:|
| `sky130_fd_sc_hd__xor2_1` | 3220 | 2720 |
| `sky130_fd_sc_hd__xnor2_1` | 3220 | 2720 |
| `sky130_fd_sc_hd__or2b_1` | 2760 | 2720 |
| `sky130_fd_sc_hd__and2b_1` | 2760 | 2720 |
| `sky130_fd_sc_hd__dfrtp_1` | 9200 | 2720 |

---

## CTS Analysis

Clock Tree Synthesis inserted clock buffers to distribute the clock signal.

The report identified three CTS buffers:

- `clkbuf_0_clk`
- `clkbuf_1_0__f_clk`
- `clkbuf_1_1__f_clk`

The cell type was:

```text
sky130_fd_sc_hd__clkbuf_16
```

No additional inverter cells were inserted during CTS.

---

## Routing Analysis

The routing stage was analyzed to understand signal routing and physical implementation after CTS.

The OpenLane flow was successfully taken through routing and signoff analysis.

---

# Project 3

## 32-bit RISC-V PicoRV32 Physical Design

### Project Introduction

The third assignment focused on implementing and analyzing a **32-bit RISC-V PicoRV32 design** using the OpenLane/OpenROAD physical-design flow.

This project extended the concepts learned from the smaller 4-bit counter design to a considerably larger processor-oriented RTL design.

---

## Design Details

| Parameter | Value |
|---|---|
| Design | PicoRV32 |
| Architecture | 32-bit RISC-V |
| Technology | SKY130 |
| Clock Period | 6 ns |
| Synthesis Clock Uncertainty | 0.9 ns |
| CTS Clock Uncertainty | 0.3 ns |
| Timing Derate | 3% |
| Input Delay | 3 ns |
| Output Delay | 3 ns |
| Floorplan Utilization | 60% |
| Floorplan Ratio | 0.7 |

---

## Clock Period and Uncertainty

The PicoRV32 design used a **6 ns clock period**.

The synthesis clock uncertainty was configured as 15% of the clock period:

```text
15% × 6 ns = 0.9 ns
```

For CTS, the target skew/uncertainty requirement was based on 5% of the clock period:

```text
5% × 6 ns = 0.3 ns
```

---

## Timing Derate

A **3% timing derate** was applied to the design.

The timing derate was configured and verified during the physical-design flow.

---

## Input and Output Delays

The input and output delays were configured to 50% of the clock period.

For a 6 ns clock:

- Input Delay = **3 ns**
- Output Delay = **3 ns**

---

## Floorplan Utilization

The floorplan utilization was configured to:

```text
60%
```

This configuration was used to control the amount of core area occupied by standard cells.

---

## Floorplan Ratio

The floorplan ratio was configured to:

```text
0.7
```

This parameter was verified through the OpenLane configuration.

---

## Manual Port Placement

Manual port placement was performed using a `pin_order.cfg` file.

The configuration included signals such as:

- Clock
- Reset
- Memory interface signals
- IRQ signals
- PCPI signals
- Memory data signals
- Other PicoRV32 input/output signals

The objective was to organize the ports systematically and control their physical placement.

---

## Library Cell Analysis

The OpenROAD report for the PicoRV32 design recorded:

| Parameter | Value |
|---|---:|
| Technology Layers | 14 |
| Technology Vias | 25 |
| Library Cells | 441 |
| Pins | 411 |
| Components | 12005 |
| Nets | 9508 |

This demonstrated the considerably larger physical complexity of the PicoRV32 design compared with the 4-bit counter.

---

## CTS Target Skew

For a 6 ns clock:

```text
5% × 6 ns = 0.3 ns
```

### Target CTS Skew

**0.3 ns**

The CTS stage was analyzed using the OpenLane/OpenROAD flow and the achieved clock behavior was verified from the generated reports.

---

## Post-CTS Clock Network Delay

After CTS, the clock network was configured as a propagated clock.

The ideal clock network was disabled.

| Parameter | Result |
|---|---|
| Clock Network Delay | INSERTED |
| Clock Type | PROPAGATED CLOCK |
| Ideal Clock Network | DISABLED |

This ensures that post-CTS timing analysis considers the implemented clock network rather than an ideal clock.

---

# Technologies Used

The following technologies, tools and concepts were used during the course:

- OpenLane
- OpenROAD
- SKY130 HD PDK
- TCL
- Linux
- VI Editor
- Verilog / RTL
- Static Timing Analysis (STA)
- RTL-to-GDSII Flow
- Synthesis
- Floorplanning
- Placement
- Clock Tree Synthesis (CTS)
- Routing
- Signoff Analysis
- IR-Drop Analysis
- Power Analysis
- Area Analysis
- Utilization Analysis
- Wire Length Analysis
- PicoRV32
- 32-bit RISC-V

---

# Roles and Responsibilities

During the course, I was responsible for:

- Learning the OpenLane physical-design environment.
- Practicing Linux commands required for the VLSI flow.
- Using VI editor for configuration and script editing.
- Learning TCL scripting for automation and report analysis.
- Running OpenLane physical-design stages.
- Performing synthesis and floorplan analysis.
- Performing placement analysis.
- Performing Clock Tree Synthesis analysis.
- Performing routing analysis.
- Analyzing timing slack.
- Determining maximum operating frequency.
- Analyzing power consumption.
- Analyzing area and utilization.
- Performing IR-drop analysis.
- Analyzing physical-only cells.
- Identifying buffers, inverters and flip-flops.
- Measuring standard-cell dimensions.
- Analyzing clock routing.
- Working with a 32-bit RISC-V PicoRV32 design.
- Configuring timing constraints.
- Configuring floorplan parameters.
- Performing post-CTS clock-network verification.
- Preparing technical documentation and reports.

---

# Project Report

The complete technical report contains the detailed project analysis, methodology, results and learning outcomes from the course.

### 📄 Complete Technical Report

**[View / Download Final Project Report](https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/blob/main/Final%20Project.pdf)**

Repository:

**https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/blob/main/Final%20Project.pdf**

---

# Assignment Summary

## Assignment 1

### Main Areas Covered

- Linux command practice
- VI editor
- `chmod`
- `grep`
- `awk`
- OpenLane directory structure
- TCL scripting
- Wire-length analysis
- IR-drop analysis
- Levels of Logic analysis

The first assignment established the basic command-line, scripting and physical-design analysis skills required for the later assignments.

---

## Assignment 2

### 4-bit Up/Down Counter

The 4-bit up/down counter was implemented using the OpenLane flow.

### Main Results

| Parameter | Result |
|---|---|
| Maximum Passing Clock Period | 3 ns |
| Maximum Operating Frequency | 333.33 MHz |
| 2 ns Clock Period | Timing Failure |
| Clock Uncertainty | 0.25 ns |
| Early Derate | 0.95 |
| Late Derate | 1.05 |
| Placement Utilization | 22.37% |
| Signoff RCX_MAX Power | 4.31 × 10⁻⁴ W |

### GUI-Based Physical-Design Exploration

**Floorplan**

- Core width and height
- Die width and height
- Physical-only cells

**Placement**

- Buffers
- Inverters
- Flip-flops
- Site rows
- Standard-cell dimensions

**CTS**

- CTS buffers/inverters
- Clock tree
- Clock routing

**Routing**

- Signal routing
- Routed design
- Routing-stage analysis

---

## Assignment 3

### 32-bit RISC-V PicoRV32

The third assignment involved taking the PicoRV32 RTL through the OpenLane/OpenROAD physical-design flow.

### Major Topics

- Clock period configuration
- Clock uncertainty
- Timing derate
- Input/output delays
- Floorplan utilization
- Floorplan ratio
- Manual port placement
- CTS target skew
- Clock network delay
- Propagated clock analysis
- Physical implementation of a larger RISC-V design

---

# Learnings from LST and SST

## LST – Life Skills Training

The LST sessions helped me understand the importance of personal development along with technical knowledge.

### Key Learnings

- Time management
- Goal setting
- Self-discipline
- Decision-making
- Problem-solving
- Self-confidence
- Handling challenges and failures
- Maintaining a positive attitude
- Developing a growth mindset
- Taking responsibility for my actions

These sessions helped me understand how good life skills can improve both personal and professional development.

---

## SST – Soft Skills Training

The SST sessions helped me improve my communication and professional behavior.

### Key Learnings

- Effective communication
- Active listening
- Teamwork
- Leadership
- Presentation skills
- Professional communication
- Interview skills
- Workplace etiquette
- Confidence while interacting with others
- Coordination and collaboration

Overall, the LST and SST sessions helped me become more confident, disciplined and better prepared for a professional working environment.

---

# Community Services

During the internship/course period, I participated in community-oriented activities and learned the importance of social responsibility and helping others.

## Community Service Activities

The community-service activities completed as part of the course are documented through the photographs below.

> The exact activity descriptions are intentionally not fabricated here. Add the specific activity names if required by your course documentation.

## Community Service Photos

<div align="center">

<img
  src="https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/raw/main/WhatsApp%20Image%202026-09-19%20at%2011.02.12%20PM.jpeg"
  alt="Community Service Activity 1"
  width="45%"
/>

<br><br>

<img
  src="https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/raw/main/WhatsApp%20Image%202026-09-19%20at%2011.02.12%20PM%20(1).jpeg"
  alt="Community Service Activity 2"
  width="45%"
/>

</div>

### Community Service Contribution

The community-service activities helped me understand the importance of social responsibility, teamwork, communication and contributing positively to society.

---

# Certificate

The internship/course certificate serves as official recognition of my participation and successful completion of the required training and activities.

> **Certificate image will be added once the certificate file is available.**

---

# Acknowledgments

I would like to sincerely thank **Prof. Radhakumari Challa**, Executive Director and Founder - SURE Trust, for providing me with the opportunity to participate in this course and gain valuable technical and professional knowledge.

I would also like to express my sincere gratitude to my mentor, **Veeramani R**, Staff Engineer at Synopsys Inc., for his guidance, support and valuable insights throughout the Physical Design (VLSI) course.

His guidance during the assignments helped me understand practical aspects of VLSI Physical Design, including the OpenLane/OpenROAD flow, timing analysis, floorplanning, placement, Clock Tree Synthesis, routing and signoff analysis.

I am grateful to SURE Trust and all the instructors and trainers for their continuous support and encouragement throughout my learning journey.

The practical assignments and LST/SST sessions helped me improve both my technical knowledge and professional skills.

I sincerely appreciate the time and effort invested in helping students develop the technical and professional skills required for their future careers.

---

# References

1. [OpenLane](https://github.com/The-OpenROAD-Project/OpenLane)
2. [OpenROAD](https://github.com/The-OpenROAD-Project/OpenROAD)
3. [SKY130 PDK](https://github.com/google/skywater-pdk)
4. [PicoRV32 RISC-V RTL](https://github.com/YosysHQ/picorv32)
5. OpenLane/OpenROAD generated reports
6. Course assignments and technical documentation

---

# Repository

### GitHub Repository

**[VLSI Physical Design - OpenLane](https://github.com/shamstanveerg425integratedvlsi/VLSI_PD)**

### Project Files

- [Community Service Photo 1](https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/blob/main/Plantation_collage.jpg)
- [Community Service Photo 2](https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/blob/main/Food_Service-collage.jpg)
- [`Final Project.pdf`](https://github.com/shamstanveerg425integratedvlsi/VLSI_PD/blob/main/Final%20Project.pdf) — Complete Technical Report

---

<div align="center">

### VLSI Physical Design using OpenLane & OpenROAD

**SKY130 • RTL-to-GDSII • Physical Design • RISC-V**

</div>
