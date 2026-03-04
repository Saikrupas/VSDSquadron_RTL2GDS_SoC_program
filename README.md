# 🖥️ Digital VLSI SoC Design and Planning Course Work (Openlane Sky130 workshop)
--- 
&copy; saikrupas 

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)](https://riscv.org/)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://vsdiat.vlsisystemdesign.com/)

</div>

  

## Table of Contents
---
 - [Week-1](#week-1)        
   - [Phase 1:OpenLANE Flow Familiarity (RTL → Synthesis literacy)](#phase-1-OpenLANE-Flow-Familiarity (RTL → Synthesis literacy))
   - [Phase 2:Floorplan Fundamentals (macro awareness for Caravel blocks)](#Phase-2-Floorplan-Fundamentals (macro awareness for Caravel blocks))
   - [Phase 3:Timing Literacy with Ideal Clocks (OpenSTA + ECO mindset)](#Phase-3-Timing-Literacy-with-Ideal-Clocks (OpenSTA + ECO mindset))
   - [Phase 4:CTS and Timing with Real Clocks (bridges directly to Week 4–6)](#Phase-4-CTS-and-Timing-with-Real-Clocks (bridges directly to Week 4–6))
   - [Phase 5:PDN Awareness (required vocabulary for ORFS and signoff thinking)](#Phase-5-PDN-Awareness (required vocabulary for ORFS and signoff thinking))
 - [Week-2](#week-2)
   - [Phase 1:OpenLANE Flow Familiarity (RTL → Synthesis literacy)](#phase-1-OpenLANE-Flow-Familiarity (RTL → Synthesis literacy))
   - [Phase 2:Floorplan Fundamentals (macro awareness for Caravel blocks)](#Phase-2-Floorplan-Fundamentals (macro awareness for Caravel blocks))
   - [Phase 3:Timing Literacy with Ideal Clocks (OpenSTA + ECO mindset)](#Phase-3-Timing-Literacy-with-Ideal-Clocks (OpenSTA + ECO mindset))
   - [Phase 4:CTS and Timing with Real Clocks (bridges directly to Week 4–6)](#Phase-4-CTS-and-Timing-with-Real-Clocks (bridges directly to Week 4–6))
 - [Week-2](#week-2)
 - [Week-2](#week-2)
 - [Week-2](#week-2)
 - [Week-2](#week-2)

-----
   
 
## 📃 Week-1 

  <details>
  <summary>
 Phase-1-OpenLANE Flow Familiarity (RTL → Synthesis literacy)
   </summary>
    
### Phase 1: Synthesis + characterization evidence 

 - [Link used for codespace for OpenLANE flow - VSD](https://github.com/vsdip/vsd-openlane)
   
#### Soc design and OpenLANE 

-----

#### Get familiar to open-source EDA tools 



**Steps to envoke OpenLANE flow and to preform synthesis of picorv32a inside noVNC :-**</br>  

 - once noVNC window is open in codespace,</br>
   > right click ----> go to terminal ----> cd OpenLANE (change directory to OpenLANE) </br>
 - Then type  "make mount" to invoke OpenLANE flow. </br>
 - type <mark> ./flow.tcl -interactive </mark> (to open OpenLANE flow in interactive mode, the flow is step-by-step ) </br>
 
   ![OpenLANE run directory](https://github.com/Saikrupas/VSDSquadron_RTL2GDS_SoC_program/blob/main/Lab_results_OpenLANE_workshop/Lab-1_results%20(1).png?raw=true)</br>

  - type <mark> package require openlane 1.0.2 </mark> to get the required packages. </br>
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
 - [Directory Structure of OpenLANE run directory](directory_structure_run.md) </br>
 



  **Synthesis run proof + synthesis report snippet :-**
  
<img width="1667" height="888" alt="image" src="https://github.com/user-attachments/assets/8b3d0fd5-f95a-4bb3-805e-f299d234f8a5" /></br>  
<img width="1707" height="881" alt="image" src="https://github.com/user-attachments/assets/aaa28e96-5eb7-4e5a-9941-0bf66c24651b" /></br>  
<img width="1670" height="876" alt="image" src="https://github.com/user-attachments/assets/d20dd1a8-af05-4aa7-a50a-2c8c65fa464a" /></br>   
<img width="1753" height="781" alt="image" src="https://github.com/user-attachments/assets/9d40512a-d206-4ef7-a109-5a257ba571e0" /></br>  

**Characterization output (area, cell count, worst slack):-**  
- Area </br>  
<img width="1753" height="781" alt="image" src="https://github.com/user-attachments/assets/1182ff63-aaa9-418f-8a3d-6e82d498024a" /></br>

- No. of cells </br>  
<img width="1670" height="876" alt="image" src="https://github.com/user-attachments/assets/033003dd-bc6d-4153-8c4e-125e10d73817" /> </br>

<p align="center"> Flop Ratio (No. of FF) = Number of D Flip Flops / Total number of cells   =  1613 / 18508 = 0.08715 </p> </br>

<p align="center"> percentage of D-FF's = 0.08715 * 100 = 8.715 </p></br>  

- Worst slack </br>

<img width="1366" height="206" alt="image" src="https://github.com/user-attachments/assets/248c1ed9-e385-43df-90d5-c71bf7779528" /> </br>


-  Refrence</br>
 [OpenLANE Resource-1](https://github.com/efabless/openlane2) </br>
 [OpenLANE Resource-2](https://github.com/efabless/openlane)  </br>
 [Youtube link1](https://www.youtube.com/watch?v=EczW2IWdnOM)  </br>
 [Youtube link2](https://www.youtube.com/watch?v=Vhyv0eq_mLU)  </br>
</details>


<details>
  <summary>
    Phase-2-Floorplan Fundamentals (macro awareness for Caravel blocks)
  </summary>

  ## Phase 2: Floorplan + macro/pre-placed cell understanding evidence
</details>


<details>
  <summary>
   Phase-3-Timing Literacy with Ideal Clocks (OpenSTA + ECO mindset)
</summary>
  
  ## Phase 3: OpenSTA run + optimization + ECO evidence
</details>

<details>
  <summary>
    Phase-4-CTS and Timing with Real Clocks (bridges directly to Week 4–6)
  </summary>
  
  ## Phase 4: CTS run + real-clock timing evidence

</details>


<details>
  <summary>
   Phase-5-PDN Awareness (required vocabulary for ORFS and signoff thinking)
  </summary>
  
  ## Phase 5: PDN evidence
 

</details>


------

## 📃 Week-2

<details>
  <summary>
   Phase-1-ORFS Execution in GitHub Codespaces
  </summary>

  - [Link used for codespace for OpenLANE flow - VSD - Repository](https://github.com/vsdip/vsd-scl180-orfs)

## Task 1.1 — Repository Setup




## Task 1.2 — Run Sky130 Testcase in Cloud


</details>

