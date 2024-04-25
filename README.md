https://queue.qa/cmps405/labs/06-process-management/
# logisim-CPU-design
This project aims to design an 8-bit CPU that has 12 instructions and uses 16-bit RAM to store data and program. The data our CPU works on is Unsigned Integers.

The CPU can have register, immediate, direct access to data where direct access can only be used with LDR and STR, and immediate can only be used with the second MOV instruction. Other instructions work with registers and addresses only.
To make the CPU, we divided our project into small subsections. We have made the ALU and the CU separately and we have created our own ring counter for the CU.
We have combined everything in the CPU class, and we have added all the classes together in the main class to further simplify the design. 
DESIGN CONSTRAINTS: Logisim has an issue when loading a RAM for the first time, so it is needed to press reset, then start for the first time. To run the CPU again, press reset then start too.

Instruction Set:
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/db5e4130-f528-4434-bbc3-92cca556bedc)

<table style="width: 678px;">
<tbody>
<tr style="height: 48px;">
<td style="height: 48px; width: 363px;">
<p><span style="color: #0000ff;"><strong><span style="color: #000080;">OPCODE (MOST 4 DIGITS)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
</td>
<td style="height: 48px; width: 301px;">
<p><span style="color: #000080;"><strong>OPERATION</strong></span></p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0000</p>
</td>
<td style="height: 35px; width: 301px;">
<p>HALT</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0001</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Register-to- Register</p>
</td>
</tr>
<tr style="height: 35.6667px;">
<td style="height: 35.6667px; width: 363px;">
<p>0010</p>
</td>
<td style="height: 35.6667px; width: 301px;">
<p>Imm-to-register</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0011</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Memory-to-Register</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0100</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Register -to- Memory</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0101</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Add</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0110</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Subtract</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>0111</p>
</td>
<td style="height: 35px; width: 301px;">
<p>AND&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>1000</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Logical Shift Right</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>1001</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Logical Shift Left</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>1010</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Branch if Zero&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
</td>
</tr>
<tr style="height: 35px;">
<td style="height: 35px; width: 363px;">
<p>1011</p>
</td>
<td style="height: 35px; width: 301px;">
<p>Branch if Carry&nbsp;&nbsp;&nbsp;&nbsp;</p>
</td>
</tr>
</tbody>
</table>
