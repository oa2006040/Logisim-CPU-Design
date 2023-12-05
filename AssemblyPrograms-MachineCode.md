<table>
<tbody>
<tr>
<td colspan="4" width="664">
<p><strong>Code 1: R0 <strong>&larr;</strong> 5 + 8 - 3</strong></p>
</td>
</tr>
<tr>
<th>The Assembly code</th>
<th>Code description</th>
<th>Machine code</th>
<th>Hex code</th>
</tr>
<!-- Step 1 -->
<tr>
<td>MOV R0, 5</td>
<td>Load the immediate value 5 into register R0.</td>
<td>0010 0000 0000 0101</td>
<td>2005</td>
</tr>
<!-- Step 2 -->
<tr>
<td>MOV R1, 8</td>
<td>Load the immediate value 8 into register R1.</td>
<td>0010 0001 0000 1000</td>
<td>2108</td>
</tr>
<!-- Step 3 -->
<tr>
<td>ADD R0, R1</td>
<td>Add R1 to R0 and store it in R0.</td>
<td>0101 0000 0000 0001</td>
<td>5001</td>
</tr>
<!-- Step 4 -->
<tr>
<td>MOV R1, 3</td>
<td>Load the immediate value 3 into register R1.</td>
<td>0010 0001 0000 0011</td>
<td>2103</td>
</tr>
<!-- Step 5 -->
<tr>
<td>SUB R0, R1</td>
<td>Subtract R1 from R0 and store it in R0.</td>
<td>0110 0000 0000 0001</td>
<td>6001</td>
</tr>
<!-- Step 6 -->
<tr>
<td>HLT</td>
<td>Halt.</td>
<td>0000 0000 0000 0000</td>
<td>0000</td>
</tr>
</tbody>
</table>
<p>R0 = 5+8-3 = ox0a</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/4adc0d54-59f8-4878-b8f0-712358f57401)
<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td colspan="4">
<p><strong>Code 2: R0 &larr; A + B (let A=0xaa, let B=0xbb)</strong></p>
</td>
</tr>
<tr>
<th>The Assembly code</th>
<th>Code description</th>
<th>Machine code</th>
<th>Hex code</th>
</tr>
<!-- Step 1 -->
<tr>
<td>LDR R0, [A]</td>
<td>Load memory location A data into R0.</td>
<td>0011 0000 1010 1010</td>
<td>30AA</td>
</tr>
<!-- Step 2 -->
<tr>
<td>LDR R1, [B]</td>
<td>Load memory location B data into R1.</td>
<td>0011 0001 1011 1011</td>
<td>31BB</td>
</tr>
<!-- Step 3 -->
<tr>
<td>ADD R0, R1</td>
<td>Add R1 to R0 and store it in R0.</td>
<td>0101 0000 0000 0001</td>
<td>5001</td>
</tr>
<!-- Step 4 -->
<tr>
<td>HLT</td>
<td>Halt.</td>
<td>0000 0000 0000 0000</td>
<td>0000</td>
</tr>
</tbody>
</table>
<p>[0xaa] = 5</p>
<p>[0xbb] = 6</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/fa7301ca-c8bf-4e49-9a91-8eaf0f19ea01)
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/f69c5664-d567-4a39-b7c7-879834c03042)

<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td colspan="3">
<p><strong>Code 3: R0 &larr; 5 x A (let A=0xaa)</strong></p>
</td>
</tr>
<tr>
<th>The Assembly code</th>
<th>Code description</th>
<th>Machine code</th>
<th>Hex code</th>
</tr>
<!-- Step 1 -->
<tr>
<td>LDR R0, [A]</td>
<td>Load memory location A data into R0.</td>
<td>0011 0000 1010 1010</td>
<td>30AA</td>
</tr>
<!-- Step 2 -->
<tr>
<td>MOV R1, R0</td>
<td>Copy R0 data to R1.</td>
<td>0001 0000 0000 1000</td>
<td>1008</td>
</tr>
<!-- Step 3 -->
<tr>
<td>LSL R0, R0</td>
<td>Shift left R0 and store it in R0.</td>
<td>1001 0000 0000 0000</td>
<td>9000</td>
</tr>
<!-- Step 4 -->
<tr>
<td>LSL R0, R0</td>
<td>Shift left R0 and store it in R0.</td>
<td>1001 0000 0000 0000</td>
<td>9000</td>
</tr>
<!-- Step 5 -->
<tr>
<td>ADD R0, R1</td>
<td>Add R1 to R0 and store it in R0.</td>
<td>0101 0000 0000 0001</td>
<td>5001</td>
</tr>
<!-- Step 6 -->
<tr>
<td>HLT</td>
<td>Halt.</td>
<td>0000 0000 0000 0000</td>
<td>0000</td>
</tr>
</tbody>
</table>
<p>[0xaa] = 5</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/dffa3da3-ca68-46e0-8b03-6ef1c3193175)
<p>&nbsp;</p>
<p>5*0xaa = 0x19</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/7298c1ec-8d00-44d2-8adb-5d293d11905c)
<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td colspan="3">
<p><strong>Code 4: Find if A is even or odd (R2=0:even, R2=1:odd) (let A=0xaa)</strong></p>
<p>(Program Origin is 0x00 so to branch sixth code we branch 0x06)</p>
</td>
</tr>
<tr>
<th>Code description</th>
<th>Machine code</th>
<th>Hex code</th>
</tr>
<!-- Step 1 -->
<tr>
<td>Load memory location A data into R0.</td>
<td>0011 0000 1010 1010</td>
<td>30AA</td>
</tr>
<!-- Step 2 -->
<tr>
<td>Load immediate value 1 to R1 which is the mask.</td>
<td>0010 0001 0000 0001</td>
<td>2101</td>
</tr>
<!-- Step 3 -->
<tr>
<td>Use AND operation on R0 and R1 and store it in R0.</td>
<td>0111 0000 0000 0001</td>
<td>7001</td>
</tr>
<!-- Step 4 -->
<tr>
<td>Initially store 0 in R2 for even values.</td>
<td>0010 0010 0000 0000</td>
<td>2200</td>
</tr>
<!-- Step 5 -->
<tr>
<td>Branch if the mask result gave 0 meaning even.</td>
<td>1010 0000 0000 0110</td>
<td>A006</td>
</tr>
<!-- Step 6 -->
<tr>
<td>If the branch failed, change R2 value to 1 meaning odd.</td>
<td>0010 0010 0000 0001</td>
<td>2201</td>
</tr>
<!-- Step 7 -->
<tr>
<td>Halt.</td>
<td>0000 0000 0000 0000</td>
<td>0000</td>
</tr>
</tbody>
</table>
<p>If [0xaa] = 1</p>
<p>Meaning odd</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/3a105b7f-f531-49eb-b04e-8394aa9c63c2)

<p>If [0xaa] = 8</p>
<p>meaning even</p>
![image](https://github.com/oa2006040/logisim-CPU-design/assets/152556993/aa29d431-1f52-42cf-ad43-ddcfe8661e11)

<p>&nbsp;</p>
<table>
<tbody>
<tr>
<td colspan="3">
<p><strong>Code 5: Carry test (loop subtract from R0 until carry)</strong></p>
<p>(We don&rsquo;t have JMP instructions so we will force jump using BRZ by making ZF=0)</p>
</td>
</tr>
<tr>
<th>Code description</th>
<th>Machine code</th>
<th>Hex code</th>
</tr>
<!-- Step 1 -->
<tr>
<td>Initialize R0 with 2.</td>
<td>0010 0000 0000 0010</td>
<td>2002</td>
</tr>
<!-- Step 2 -->
<tr>
<td>Initialize R1 with 1.</td>
<td>0010 0001 0000 0001</td>
<td>2101</td>
</tr>
<!-- Step 3 -->
<tr>
<td>Initialize R2 with 0.</td>
<td>0010 0010 0000 0000</td>
<td>2200</td>
</tr>
<!-- Step 4 -->
<tr>
<td>Subtract 1 from R0.</td>
<td>0110 0000 0000 0001</td>
<td>6001</td>
</tr>
<!-- Step 5 -->
<tr>
<td>If carry, branch to Halt.</td>
<td>1011 0000 0000 0111</td>
<td>b007</td>
</tr>
<!-- Step 6 -->
<tr>
<td>Force ZF=0 by adding 0 to 0.</td>
<td>0101 0000 0001 0010</td>
<td>5012</td>
</tr>
<!-- Step 7 -->
<tr>
<td>Loop back to subtracting.</td>
<td>1010 0000 0000 0011</td>
<td>a003</td>
</tr>
<!-- Step 8 -->
<tr>
<td>Halt.</td>
<td>0000 0000 0000 0000</td>
<td>0000</td>
</tr>
</tbody>
</table>
