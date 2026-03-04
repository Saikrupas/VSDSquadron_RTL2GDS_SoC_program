# 🖥️ VSDSquadron RTL2GDS SoC program 
--- 
&copy; saikrupas 

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)](https://riscv.org/)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://vsdiat.vlsisystemdesign.com/)

</div>

## Table of Contents
---
 - [Week-1 - Digital VLSI SoC Design and Planning (Openlane sky130 workshop)](#week-1-Digital-VLSI-SoC-Design-and-Planning-(Openlane-sky130-workshop))        
   - [Phase 1: OpenLANE Flow Familiarity (RTL → Synthesis literacy)](#phase-1-OpenLANE-Flow-Familiarity (RTL → Synthesis literacy))
   - [Phase 2: Floorplan Fundamentals (macro awareness for Caravel blocks)](#Phase-2-Floorplan-Fundamentals (macro awareness for Caravel blocks))
   - [Phase 3: Timing Literacy with Ideal Clocks (OpenSTA + ECO mindset)](#Phase-3-Timing-Literacy-with-Ideal-Clocks (OpenSTA + ECO mindset))
   - [Phase 4: CTS and Timing with Real Clocks (bridges directly to Week 4–6)](#Phase-4-CTS-and-Timing-with-Real-Clocks (bridges directly to Week 4–6))
   - [Phase 5: PDN Awareness (required vocabulary for ORFS and signoff thinking)](#Phase-5-PDN-Awareness (required vocabulary for ORFS and signoff thinking))
     
 - [Week-2](#week-2)
   - [Phase 1: ORFS Execution in GitHub Codespaces](#Phase-1-ORFS-Execution-in-GitHub-Codespaces)
   - [Phase 2: Toolchain Understanding (Devcontainer Deep Dive)](#Phase-2-Toolchain-Understanding (Devcontainer Deep Dive))
   - [Phase 3: Local Installation (Self-Owned Environment)](#Phase-3-Local-Installation (Self-Owned Environment))
   - [Phase 4: Re-Run RTL-to-GDS Locally](#Phase-4-Re-Run-RTL-to-GDS-Locally)
   - [Phase 5: Debugging and Unix Literacy](#Phase-5-Debugging-and-Unix-Literacy)
     
 - [Week-2](#week-2)
 - [Week-2](#week-2)
 - [Week-2](#week-2)
 - [Week-2](#week-2)

-----
   
 
## 📃 Week-1- Digital-VLSI-SoC-Design-and-Planning-(Openlane-sky130-workshop)

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
   <b>Phase-1-ORFS Execution in GitHub Codespaces</b>
  </summary>

  - [Link used for codespace for OpenLANE flow - VSD - Repository](https://github.com/vsdip/vsd-scl180-orfs)

## Task 1.1 — Repository Setup

 - Fork this repository [vsd-scl180-orfs](https://github.com/vsdip/vsd-scl180-orfs) </br>

   Click code ----> Codespaces ----> Create Codespace </br>
   
 <p align="center">
    <img width="1907" height="926" alt="image" src="https://github.com/user-attachments/assets/f488ba27-6747-44bc-ba85-c2b6b7e59e4a" />
 </p>
  <p align="center">
    <img width="1915" height="952" alt="image" src="https://github.com/user-attachments/assets/a5c10e83-4787-4b89-b5ad-e89a5d526b66" />
  </p>

## Task 1.2 — Run Sky130 Testcase in Cloud

- Open noVnc in the codespace </br>
  
```` bash
## Go to the following directory
  cd workspaces/vsd-scl180-orfs/orfs/flow

## open Makefile using gedit command
   gedit Makefile
## comment line no. 44 and uncomment line no. 48 in Makefile (by doing this we are connecting the foundry(sky130nm) with the design(riscv32i))
````

 <p align="center">
   <img width="1601" height="822" alt="image" src="https://github.com/user-attachments/assets/0a46a608-3c87-4374-921e-5335a71e2a46" />
   <img width="1608" height="717" alt="image" src="https://github.com/user-attachments/assets/62df3634-6f72-4683-b68d-83d3844cd3c9" />
   <img width="1455" height="872" alt="image" src="https://github.com/user-attachments/assets/e12f054b-d062-43ec-882e-b5c73aa85b6c" />
 </p>


```bash
## To run the logic synthesis for design riscv32i using sky130nm pdk using Makefile commands 
  make synth

## To see the synthesis results go to base directory
 cd results/sky130hd/riscv32i/base

## To see the synthesized netlist 
gedit results/sky130hd/riscv32i/base/1_2_yosys.v
```

snapshots for synthesis run proof 

```bash
## To run floorplanning
 cd workspaces/vsd-scl180-orfs/orfs/flow
  make floorplan

## To visualize the floorplan in gui mode
make gui_floorplan
```

 snapshots for floorplan run proof 

```bash
## To run placement
cd workspaces/vsd-scl180-orfs/orfs/flow
make place

## To visualize the placement in gui mode to zoom in (z) zoom out (shift + z)
make gui_place 
```

snapshots for placement run proof

```bash
## To run CTS
cd workspaces/vsd-scl180-orfs/orfs/flow
make cts

## To visualize the placement in gui mode 
make gui_cts
```

snapshots for cts

```bash
## To run routing
cd workspaces/vsd-scl180-orfs/orfs/flow
make route

## To visualize the routing in gui mode 
make gui_route
```


```bash
## To run GDS
cd workspaces/vsd-scl180-orfs/orfs/flow
make DESIGN_NAME=riscv32i PLATFORM=sky130hd

## To check final gui layout
make gui_final
```


-  Refrence </br>
 [sky130-testcase-run-cloud](https://www.youtube.com/live/XLeMNjgrlK0) </br>
</details>

<details>
  <summary>
    Phase-2-Toolchain Understanding (Devcontainer Deep Dive)   
  </summary>
  
## Task 2.1 — Toolchain Mapping

## Task 2.2 — Flow Architecture Explanation
</details>

<details>
  <summary>
    Phase-3-Local Installation (Self-Owned Environment)
    
  </summary>

  </details>


<details>
  <summary>
    Phase-4-Re-Run RTL-to-GDS Locally
    
  </summary>

  </details>

  <details>
  <summary>
    Phase-5-Debugging and Unix Literacy
    
  </summary>

  </details>
