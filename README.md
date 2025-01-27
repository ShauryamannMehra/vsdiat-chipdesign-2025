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
