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


**Steps to envoke OpenLANE flow and to preform synthesis of picorv32a inside noVNC :-**

 - once noVNC window is open in codespace,</br>
   > right click ----> go to terminal ----> cd OpenLANE (change directory to OpenLANE) </br>
 - Then type  "make mount" to invoke OpenLANE flow. </br>
 - type <mark> ./flow.tcl -interactive </mark> (to open OpenLANE flow in interactive mode) </br>
 
   ![OpenLANE run directory](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(1).png?raw=true)</br>
   
  - type <mark> prep -design picorv32a </mark> </br>  
  - <mark> run_synthesis </mark>, to sythesize the RTL cose of the desired design for us now its picorv32a)</br>  
   ![OpenLANE synthesis](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(2).png?raw=true)</br>
  - To exit out of OpenLANE type exit.</br>  
   ![OpenLANE exit](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(3).png?raw=true)</br>  
   
  - results of synthesis  run can be found under,</br>
   > Desktop --> openLANE --> designs --> picorv32a ---> runs ---> latest run folder ---> reports and results.</br>  
   ![OpenLANE synthesis results](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(4).png?raw=true)</br>  
   ![OpenLANE synthesis results](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(5).png?raw=true)</br>  
   <img width="1665" height="876" alt="image" src="https://github.com/user-attachments/assets/90e877ad-e9f3-482a-a361-ee5508d0f642"/></br>

   
 **Screenshot of OpenLANE run directory showing the structure :-**

<img width="1665" height="876" alt="image" src="https://github.com/user-attachments/assets/96c8212d-e629-4547-8803-f1aa10df85f5" /> </br>  


  **Synthesis run proof + synthesis report snippet :-**
  
<img width="1667" height="888" alt="image" src="https://github.com/user-attachments/assets/8b3d0fd5-f95a-4bb3-805e-f299d234f8a5" /></br>  
<img width="1707" height="881" alt="image" src="https://github.com/user-attachments/assets/aaa28e96-5eb7-4e5a-9941-0bf66c24651b" /></br>  
<img width="1670" height="876" alt="image" src="https://github.com/user-attachments/assets/d20dd1a8-af05-4aa7-a50a-2c8c65fa464a" /></br>  
<img width="1747" height="895" alt="image" src="https://github.com/user-attachments/assets/2c765e5f-87c0-4581-9f6d-fa5decd930fb" /></br>  









## Phase-2-Floorplan Fundamentals (macro awareness for Caravel blocks)
