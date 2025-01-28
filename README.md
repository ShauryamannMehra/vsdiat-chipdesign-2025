# vsdiat-chipdesign-2025
Chip Design For Highschool<br>
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
For open-source ASIC design implemantation, we require the following enablers to be readily available:-
- RTL Designs
- EDA Tools
- PDK Data <br>
Early EDA tools were results of academic work. Nowadays we have great EDA toold like Qflow, OpenROAD and OpenLANE<br>
Till 1979 the design and fabrication of IC's were tightly coupled and were only practiced by very few companies like TI, Intel, etc.<br>
In 1979, Lynn Conway and Carver Mead came up with an idea to saperate the design from the fabrication and to do this they inroduced structured design methodologies based on the λ-based design rules and published the first VLSI book "Introduction to VLSI System" which started the VLSI education.<br>
Since then, we started to see Pure Play Fabs and Fabless Design companies<br>
The inteface between the designers and the fab by now became a set of data files and documents, that are reffered to as the "Process Design Kits (PDKs)".<br>
PDKs include but are not limited to Device Models, Technology Information, Design Rules, Digital Standard Cell Libraries, I/O Libraries and many more.<br>
The PDKs contained variety of informations, and so they were distributed under (Non-Disclosure Agreements) which made it inaccessible to the masses.<br>
Google worked out an agreement with skywater to open-source the PDK for the 130nanometer process by skywater Technology and as a result on 30 June 2020 Google released the first ever open-source PDK.
![image](https://github.com/user-attachments/assets/744cf64c-b54d-44f2-ab45-91aff583066f)
![image](https://github.com/user-attachments/assets/5e737f37-c31c-4536-9f72-9881bc6be2c9)
<br>
ASIC design is a complex step that involves tons of steps, various methodologies and respective EDA tools which are all required for successful ASIC implementation which is achieved though an ASIC flow which is nothing but a piece of software that pulls different tools togather to carry out the design process.
