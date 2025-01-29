# vsdiat-chipdesign-2025
## Chip Design For Highschool<br> 
### THEORY
<details>
  <summary>
Expand or Collapse
  </summary>
  
### D1_Sk1_L1<br>
#### PACKAGE: In any embedded board we come across, the chip that we refer to is actually only the PACKAGE of the chip. 
- Examples are QFN-48 and Quad Flat No Leads. It is like an outer covering of the actual chip.
- There are pins around the boundary of the chip in a package and they are connected to the chip via WIRE BOUND method.
![image](https://github.com/user-attachments/assets/2528d024-0ced-46ad-81ae-f62a01c54dc2)
![image](https://github.com/user-attachments/assets/7a141f16-0606-43b7-ab58-4b6e99b46e05)
![image](https://github.com/user-attachments/assets/dcf44ac0-beb2-45a0-ac79-488512088877)<br>
#### CHIP: Inside the chip, there are many components. One of them is PADS
- Pads are used to send signals inside the chip.
- The area surrounded by the pads is called CORE; it is where all the digital logic of the chip is placed.
-  The PADS and CORE together make up the DIE, which is manufactured on a silicon paper. 
![image](https://github.com/user-attachments/assets/de24e5a3-01db-42b7-b46f-032e9b1a0ae4)<br>
#### FOUNDRY: A FOUNDRY is similar to a factory where chips are manufactured. FOUNDRY IP's are Intellectual Properties that require a specific level of intelligence to be produced. MACROS are just repeated digital logic blocks
![image](https://github.com/user-attachments/assets/923d9525-6854-45a3-9e07-be173bc37b80)<br>
### D1_Sk1_L2
#### ISA (Intruction Set Architecture):
- A C program that is to be run on a specific hardware layout which is the interior of a chip in your laptop, there is particular flow to be followed.
- This particular C program is compiled in it's assembly language program which is translated into machine language,i.e. the binary language program.
- we have to implement this RISC-V specification using some RTL (a Hardware Description Language).
![image](https://github.com/user-attachments/assets/faf7c246-b991-4072-bdce-60f15b8b3839)<br>
### D1_Sk1_L3
#### Application Software to Hardware
- apps enters into a block called system software and it converts the application program to binary language.
- major layers or components in system software are OS (Operating System), Compiler and Assembler.
- OS outputs are small function in C, C++ or Java language which are taken by the compiler and converted into instructions.
- These syntax will be dependent on the HARDWARE
- The job of the assembler is to take these instructions and convert them into binary numbers which is basically called as a machine language program.
![image](https://github.com/user-attachments/assets/d94a9937-c4a1-4e41-935a-7e5b04b9dda3)<br>
#### Example of STOPWATCH <br>
- if we take a stopwatch app on RISC-V core, the output of the Operating System could be a function which enters into the compiler and we get RISC-V instructions as output. The output of the assembler will be the binary code which will enter into the chip layout. <br>
![image](https://github.com/user-attachments/assets/368caebf-6c32-4822-b438-508754579d9a) <br>
- INSTRUCTION SET ARCHITECTURE or the architecure is the abstract interface between the C language and the Hardware.
- Hardware understands only 1s and 0s thus there is a need for hardware description language.
- we need some RTL (a Hardware Description Language) which understands and implements the particular instructions.
- RTL is then synthesised into a netlist in form of operation gates which is put into the chip through physical design implementation.
![image](https://github.com/user-attachments/assets/9950cc7b-4f36-4994-b6d5-ef91720b61ba)<br>
### D1_Sk2_L1<br>
For open-source ASIC design implemantation, we require the following enablers to be readily available:- <br>
 RTL Designs <br>
EDA Tools <br>
PDK Data <br>
- Early EDA tools were results of academic work. Nowadays we have great EDA toold like Qflow, OpenROAD and OpenLANE
- Till 1979 the design and fabrication of IC's were tightly coupled and were only practiced by very few companies like TI, Intel, etc.<br>
- In 1979, Lynn Conway and Carver Mead came up with an idea to saperate the design from the fabrication and to do this they inroduced structured design methodologies based on the λ-based design rules and published the first VLSI book "Introduction to VLSI System" which started the VLSI education.<br>
- Since then, we started to see Pure Play Fabs and Fabless Design companies<br>
- The inteface between the designers and the fab by now became a set of data files and documents, that are reffered to as the "Process Design Kits (PDKs)".<br>
- PDKs include but are not limited to Device Models, Technology Information, Design Rules, Digital Standard Cell Libraries, I/O Libraries and many more.<br>
- The PDKs contained variety of informations, and so they were distributed under Non-Disclosure Agreements which made it inaccessible to the masses.<br>
- Google worked out an agreement with skywater to open-source the PDK for the 130nanometer process by skywater Technology and as a result on 30 June 2020 Google released the first ever open-source PDK. <br>
![image](https://github.com/user-attachments/assets/744cf64c-b54d-44f2-ab45-91aff583066f)
![image](https://github.com/user-attachments/assets/5e737f37-c31c-4536-9f72-9881bc6be2c9)
<br>
- ASIC design is a complex and involves tons of steps, various methodologies and EDA tools, which are required for successful ASIC implementation which is achieved though an ASIC flow, which is nothing but a piece of software that pulls different tools together to carry out the design process.<br>
![image](https://github.com/user-attachments/assets/9da5f2fa-35d4-4bde-ab7f-7254d46bfcef)<br>
### D1_Sk2_L2<br>
The main objective of the ASIC Design Flow is to take the design from the RTL (Register Transfer Level) all the way to the GDSII, which is the format used for the final fabrication layout. <br>
![image](https://github.com/user-attachments/assets/b761647b-b06b-4433-81b5-1ec442a30a25)<br>
- Gate-Level Netlist is functionally equivalent to the RTL.<br>
![image](https://github.com/user-attachments/assets/06cb2ad2-00c5-467a-aa87-63c68aea8c32)<br>
- The fundemental building blocks which are the standard cells have regular layouts.
- Each cell has different views/models which are utilised by different EDA tools like liberty view with electrical models of the cells, HDL behavioral models, SPICE or CDL views of the cells, Layout view which include GDSII view which is the detailed view and LEF view which is the abstract view.<br>
![image](https://github.com/user-attachments/assets/56e8763e-7158-4f07-8491-ff2436c9d4c2)<br>
- Power Planning typically uses upper metal layers for power distribution since thay are thicker than lower metal layers and so have lower resistance and PP is done to avoid electron migration and IR drops.
![image](https://github.com/user-attachments/assets/036d0181-3fdb-4d3a-ad0d-ccf28604bb29)<br>
![image](https://github.com/user-attachments/assets/016a440f-8ce7-4af2-9138-a4fd41c1450b)<br>
![image](https://github.com/user-attachments/assets/e37ba4dc-4f64-498f-a3d0-ed302f4dd6a3)<br>
![image](https://github.com/user-attachments/assets/ac25ef24-1867-405e-8e7e-bb0fe2514192)
- Global placement provide approximate locations for all cells based on connectivity but in this stage the cells may be overlapped on each other and in detailed placement the positions obtained from global placements are minimally altered to make it legal (non-overlapping and in site-rows)<br>
![image](https://github.com/user-attachments/assets/0ef78032-d1aa-4f10-b6cc-6acf9ab1e988)<br>
![image](https://github.com/user-attachments/assets/39e753c6-dc3a-455f-a252-243bfb92bc8a)
- Clock skew is the time difference in arrival of clock at different components.<br>
![image](https://github.com/user-attachments/assets/ae964d65-800c-48c3-91bb-e5f6d8892e3c)<br>
- skywater PDK has 6 routing layers in which the lowest layer is called the local interconnect layer which is a Titanium Nitride layer the following 5 layers are all Aluminium layers.<br>
![image](https://github.com/user-attachments/assets/fcbd4686-d8d2-43af-aed6-659e66103a38)<br>
![image](https://github.com/user-attachments/assets/ce7c9cef-d69a-4a6e-bbb4-07dfd744c60d)
- Once done with the routing the final layout can be generated which undergoes various Sign-Off checks.
- Design Rules Checking (DRC) which verifies that the final layout honours all design fabrication rules.
- Layout Vs Schematic (LVS) which verifies that the final layout functionality matches the gate-level netlist that we started with.
- Static Timing Analysis (STA) to verify that the design runs at the designated clock frequency
![image](https://github.com/user-attachments/assets/97239f7b-0364-451a-bb10-93a5e5fa5f2f)<br>
