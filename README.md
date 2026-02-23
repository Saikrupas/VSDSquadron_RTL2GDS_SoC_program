# 🖥️ Digital VLSI SoC Design and Planning Course Work (Openlane Sky130 workshop)
--- 
&copy; saikrupas 

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)](https://riscv.org/)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://vsdiat.vlsisystemdesign.com/)

</div>

Link used to run codespace for OpenLANE flow - https://github.com/vsdip/vsd-openlane 

## Table of Contents
---
   - [Phase 1:OpenLANE Flow Familiarity (RTL → Synthesis literacy)](#phase-1-OpenLANE-Flow-Familiarity (RTL → Synthesis literacy))                                                      
   - [Phase 2:Floorplan Fundamentals (macro awareness for Caravel blocks)](#Phase-2-Floorplan-Fundamentals (macro awareness for Caravel blocks))

   
  
 ## Phase-1-OpenLANE Flow Familiarity (RTL → Synthesis literacy)
<details>
  <summary>
     Phase 1: Synthesis + characterization evidence 
</summary>
   
### <u>Soc design and OpenLANE</u></br>

-----
### Get familiar to open-source EDA tools 


#### **Steps to envoke OpenLANE flow and to preform synthesis of picorv32a inside noVNC** 
 - once noVNC window is open in codespace,</br>
   > right click ----> go to terminal ----> cd OpenLANE (change directory to OpenLANE)

   ![OpenLANE run directory](images/1.jpg)
 - Then type  "make mount" to invoke OpenLANE flow.

 - type <mark> ./flow.tcl -interactive </mark> (to open OpenLANE flow in interactive mode)

 - type <mark> prep -design picorv32a </mark>

 - <mark> run_synthesis </mark>, to sythesize the RTL cose of the desired design for us now its picorv32a)

 - To exit out of OpenLANE type exit.
 - results of synthesis  run can be found under,
   > Desktop --> openLANE --> designs --> picorv32a ---> runs ---> latest run folder ---> reports and results.
#### Screenshot of OpenLANE run directory showing the structure

![OpenLANE run directory](images/1.jpg)

  



## Phase-2-Floorplan Fundamentals (macro awareness for Caravel blocks)
