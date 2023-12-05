<table style="float: left;">
<tbody>
<tr style="height: 35px;">
<td style="height: 35px;" width="664">
<p style="text-align: center;"><strong>Instruction&nbsp;Format&nbsp;of&nbsp;: MOV&nbsp;R1,&nbsp;R7</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 149px;">
<td style="height: 149px;" width="664">
<table>
<tbody>
<tr>
<td width="125">
<p>OP Code</p>
</td>
<td width="140">
<p>Immediate</p>
</td>
<td colspan="3" width="358">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="125">
<p>4-bit</p>
</td>
<td width="140">
<p>Non-used 1-bit</p>
</td>
<td width="130">
<p>5-bits</p>
<p>(not used)</p>
</td>
<td width="124">
<p>Destination; Reg - 3 bit</p>
</td>
<td width="104">
<p>Source; Reg - 3 bit</p>
</td>
</tr>
<tr>
<td width="125">
<p>0001</p>
</td>
<td width="140">
<p>x</p>
</td>
<td width="130">
<p>xxxxx</p>
</td>
<td width="124">
<p>001</p>
</td>
<td width="104">
<p>111</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr style="text-align: center; height: 35px;">
<td style="height: 35px;" width="664">
<p><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;MOV&nbsp;R1,&nbsp;5</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 138px;">
<td style="height: 138px;" width="664">
<table>
<tbody>
<tr>
<td width="162">
<p>OP Code</p>
</td>
<td width="162">
<p>Immediate</p>
</td>
<td colspan="2" width="325">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="162">
<p>4-bit</p>
</td>
<td width="162">
<p>Non-used 1-bit</p>
</td>
<td width="162">
<p>Destination; Reg - 3 bit</p>
</td>
<td width="162">
<p>Source; Immediate value 8 bit</p>
</td>
</tr>
<tr>
<td width="162">
<p>0010</p>
</td>
<td width="162">
<p>x</p>
</td>
<td width="162">
<p>001</p>
</td>
<td width="162">
<p>0000-0101</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr style="text-align: center; height: 35px;">
<td style="height: 35px;" width="664">
<p><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;LDR&nbsp;R1,&nbsp;0x01</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 138px;">
<td style="height: 138px;" width="664">
<table>
<tbody>
<tr>
<td width="162">
<p>OP Code</p>
</td>
<td width="162">
<p>Immediate</p>
</td>
<td colspan="2" width="325">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="162">
<p>4-bit</p>
</td>
<td width="162">
<p>Non-used 1-bit</p>
</td>
<td width="162">
<p>Destination; Reg - 3 bit</p>
</td>
<td width="162">
<p>Source; Direct Address value 8 bit</p>
</td>
</tr>
<tr>
<td width="162">
<p>0001</p>
</td>
<td width="162">
<p>x</p>
</td>
<td width="162">
<p>001</p>
</td>
<td width="162">
<p>0000-0001</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr style="text-align: center; height: 35px;">
<td style="height: 35px;" width="664">
<p><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;STR&nbsp;0x01,&nbsp;R1</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 138px;">
<td style="height: 138px;" width="664">
<table>
<tbody>
<tr>
<td width="162">
<p>OP Code</p>
</td>
<td width="162">
<p>Immediate</p>
</td>
<td colspan="2" width="325">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="162">
<p>4-bit</p>
</td>
<td width="162">
<p>Non-used 1-bit</p>
</td>
<td width="162">
<p>Destination; Direct Address value 8 bit</p>
</td>
<td width="162">
<p>Source; Reg - 3 bit</p>
</td>
</tr>
<tr>
<td width="162">
<p>0001</p>
</td>
<td width="162">
<p>x</p>
</td>
<td width="162">
<p>0000-0001</p>
</td>
<td width="162">
<p>001</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr style="text-align: center; height: 35px;">
<td style="height: 35px;" width="664">
<p><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;ADD&nbsp;R1,&nbsp;R7</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 149px;">
<td style="height: 149px;" width="664">
<table>
<tbody>
<tr>
<td width="125">
<p>OP Code</p>
</td>
<td width="140">
<p>Immediate</p>
</td>
<td colspan="3" width="384">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="125">
<p>4-bit</p>
</td>
<td width="140">
<p>Non-used 1-bit</p>
</td>
<td width="130">
<p>5-bits</p>
<p>(not used)</p>
</td>
<td width="124">
<p>Destination; Reg - 3 bit</p>
</td>
<td width="130">
<p>Source; Reg - 3 bit</p>
</td>
</tr>
<tr>
<td width="125">
<p>0101</p>
</td>
<td width="140">
<p>x</p>
</td>
<td width="130">
<p>xxxxx</p>
</td>
<td width="124">
<p>001</p>
</td>
<td width="130">
<p>111</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr style="text-align: center; height: 35.6667px;">
<td style="height: 35.6667px;" width="664">
<p><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;LSR&nbsp;R1,&nbsp;R5</strong></p>
</td>
</tr>
<tr style="text-align: center; height: 190px;">
<td style="height: 190px;" width="664">
<table>
<tbody>
<tr>
<td width="125">
<p>OP Code</p>
</td>
<td width="140">
<p>Immediate</p>
</td>
<td colspan="3" width="384">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="125">
<p>4-bit</p>
</td>
<td width="140">
<p>Non-used 1-bit</p>
</td>
<td width="130">
<p>5-bits</p>
<p>(not used)</p>
</td>
<td width="124">
<p>Destination; Reg - 3 bit</p>
</td>
<td width="130">
<p>Source; Reg - 3 bit</p>
</td>
</tr>
<tr>
<td width="125">
<p>1000</p>
</td>
<td width="140">
<p>x</p>
</td>
<td width="130">
<p>xxxxx</p>
</td>
<td width="124">
<p>001</p>
</td>
<td width="130">
<p>101</p>
</td>
</tr>
<tr>
<td width="125">
<p>&nbsp;</p>
</td>
<td width="140">
<p>&nbsp;</p>
</td>
<td width="130">
<p>&nbsp;</p>
</td>
<td width="124">
<p>&nbsp;</p>
</td>
<td width="130">
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
<table style="float: left;">
<tbody>
<tr>
<td width="664">
<p style="text-align: center;"><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;BRZ&nbsp;0X01</strong></p>
</td>
</tr>
<tr>
<td width="664">
<table>
<tbody>
<tr>
<td width="125">
<p>OP Code</p>
</td>
<td width="140">
<p>Immediate</p>
</td>
<td colspan="2" width="384">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="125">
<p>4-bit</p>
</td>
<td width="140">
<p>Non-used 1-bit</p>
</td>
<td width="130">
<p>3-bits</p>
<p>(not used)</p>
</td>
<td width="253">
<p>8 bit address</p>
</td>
</tr>
<tr>
<td width="125">
<p>1010</p>
</td>
<td width="140">
<p>x</p>
</td>
<td width="130">
<p>xxx</p>
</td>
<td width="253">
<p>0000-0001</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td width="664">
<p style="text-align: center;"><strong>Instruction&nbsp;Format&nbsp;of&nbsp;&nbsp;: &nbsp;BRC&nbsp;0X01</strong></p>
</td>
</tr>
<tr>
<td width="664">
<table>
<tbody>
<tr>
<td width="125">
<p>OP Code</p>
</td>
<td width="140">
<p>Immediate</p>
</td>
<td colspan="2" width="384">
<p>Destination</p>
</td>
</tr>
<tr>
<td width="125">
<p>4-bit</p>
</td>
<td width="140">
<p>Non-used 1-bit</p>
</td>
<td width="130">
<p>3-bits</p>
<p>(not used)</p>
</td>
<td width="253">
<p>8 bit address</p>
</td>
</tr>
<tr>
<td width="125">
<p>1011</p>
</td>
<td width="140">
<p>x</p>
</td>
<td width="130">
<p>xxx</p>
</td>
<td width="253">
<p>0000-0001</p>
</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
