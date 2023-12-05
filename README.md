# logisim-CPU-design
This project aims to design an 8-bit CPU that has 12 instructions and uses 16-bit RAM to store data and program. The data our CPU works on is Unsigned Integers.

The CPU can have register, immediate, direct access to data where direct access can only be used with LDR and STR, and immediate can only be used with the second MOV instruction. Other instructions work with registers and addresses only.
To make the CPU, we divided our project into small subsections. We have made the ALU and the CU separately and we have created our own ring counter for the CU.
We have combined everything in the CPU class, and we have added all the classes together in the main class to further simplify the design. 
DESIGN CONSTRAINTS: Logisim has an issue when loading a RAM for the first time, so it is needed to press reset, then start for the first time. To run the CPU again, press reset then start too.

Instruction Set:
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/db5e4130-f528-4434-bbc3-92cca556bedc)

OPCODE (MOST 4 DIGITS) |	OPERATION             |
----->                                     <-----
0000	                 |   HALT                 |
0001		               |   Register-to- Register|
0010		               |   Imm-to-register      | 
0011		               |   Memory-to-Register   |
0100		               |   Register -to- Memory |
0101		               |   Add                  |
0110		               |   Subtract             |
0111		               |   AND	                |
1000		               |   Logical Shift Right  | 
1001		               |   Logical Shift Left   |
1010                   |   Branch if Zero	      |
1011                   |   Branch if Carry	    | 
