# VSD-VLSI-Internship
# Task 1 as of 20th April 
## Installation of Yosys 

![Screenshot 2024-04-29 143424](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/7fe24e87-bb1f-4430-a081-882a03f18119)

## Installation of Gtkwave

![Screenshot 2024-04-29 144319](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/e2eef5c1-d49b-4587-888e-1e928c97c981)

## Installation of iverilog 

![Screenshot 2024-04-29 144405](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/ab983b6d-1871-4f18-b912-18c65dd9d056)

## Git Cloning 


![Screenshot 2024-04-29 144611](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/b0f6549f-efa0-403d-b6f7-83761987c44e)

# Task 2 as of 23rd April
## Identifying the Instruction Type 

### Identify instruction type and exact 32-bit instruction code in the instruction type format. Upload the 32-bit pattern on Github.

### INSTRUCTIONS FORMAT IN RISC-V
### 1)R-type:

The R-format instruction in MIPS assembly language is used for arithmetic and logical operations between registers. It typically consists of an opcode, three register operands (source register 1, source register 2, and destination register), a shift amount, and a function code.

For the "add" instruction "add r6, r2, r1", the opcode is 000000, the function code for addition is 100000, and the registers involved are r2, r1, and r6.

Using this information, we can construct the 32-bit instruction code:
Opcode (6 bits): 000000 
Source Register 1 (rs, 5 bits):r2 (register 2) 
Source Register 2 (rt, 5 bits): r1(register 1) Destination Register (rd, 5 bits): r6 (register 6) 
Shift Amount (shamt, 5 bits): 00000 Function Code (6 bits): 100000

Concatenating all the fields gives the 32-bit instruction code:000000 00010 00001 00110 00000 100000



### 2) I-Type :

For an I-type instruction in MIPS assembly language, the format typically consists of:

6 bits for the opcode
5 bits for the source register (rs)
5 bits for the destination register (rt)
16 bits for the immediate value (immediate)

Let's construct a 32-bit instruction code for an example "addi" instruction:
Opcode (6 bits): 001000 (for "addi") Source Register (rs, 5 bits): r2 (register 2) Destination Register (rt, 5 bits): r6 (register 6) 
Immediate Value (16 bits): 1001 (for example, decimal value 9)


Concatenating all the fields gives the 32-bit instruction code:001000 00010 00110 0000000000001001

### 3)S-Type :
  
For an S-type instruction in MIPS assembly language, the format typically consists of:
6 bits for the opcode
5 bits for the source register (rs)
5 bits for the destination register (rt)
16 bits for the offset (or immediate value)
Let's construct a 32-bit instruction code for an example "sw" (store word) instruction:
Opcode (6 bits): 101011 (for "sw") 
Source Register (rs, 5 bits): r2 (register 2) Destination Register (rt, 5 bits): r6 (register 6) 
Offset (16 bits): 1001001100110011 (example offset value)
  
Concatenating all the fields gives the 32-bit instruction code:101011 00010 00110 1001001100110011


### 4)B-type:

For a B-type (branch) instruction in MIPS assembly language, the format typically consists of:
6 bits for the opcode
5 bits for the source register (rs)
5 bits for the destination register (rt)
16 bits for the branch offset (or immediate value)
Let's construct a 32-bit instruction code for an example "beq" (branch if equal) instruction:
Opcode (6 bits): 000100 (for "beq") 
Source Register (rs, 5 bits): r2(register 2) Destination Register (rt, 5 bits): r6 (register 6)
 Branch Offset (16 bits): 1111111111111111 (example offset value)

Concatenating all the fields gives the 32-bit instruction code:000100 00010 00110 1111111111111111


### 5)J type:
For a J-type (jump) instruction in MIPS assembly language, the format typically consists of:
6 bits for the opcode
26 bits for the jump target address
Let's construct a 32-bit instruction code for an example "j" (jump) instruction:
Opcode (6 bits): 000010 (for "j") 
Jump Target Address (26 bits): 00111111111111111111111111 (example target address)

Concatenating all the fields gives the 32-bit instruction code:000010 00111111111111111111111111

### 6)U Type
For a U-type (upper immediate) instruction in MIPS assembly language, the format typically consists of:
6 bits for the opcode
5 bits for the destination register (rd)
21 bits for the immediate value (immediate)
Let's construct a 32-bit instruction code for an example "lui" (load upper immediate) instruction:
Opcode (6 bits): 001111 (for "lui") Destination Register (rd, 5 bits): r6 (register 6) 
Immediate Value (21 bits): 1100110011001100111 (example immediate value)

Concatenating all the fields gives the 32-bit instruction code:001111 00110 1100110011001100111

# Task 3 as of 27th April 
## Compiled C Code 

![Screenshot 2024-04-30 160017](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/be88b9d1-91e4-4be6-acb5-647a47a67be7)

### Output 

![Screenshot 2024-04-30 155519](https://github.com/Karthiknayakk/VSD-VLSI-Internship/assets/167952131/280d97d7-76ab-4a5f-8a51-4dd823f47631)


