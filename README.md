# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:PRADEEP.M
RegisterNumber:212225220071
*/
FULLADDER
module EXP4FULLADDER(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
FULLSUBTRACTOR
module EXP4FULLSUBTRACTOR(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
**RTL Schematic**
FULL ADDER
<img width="1919" height="1079" alt="Screenshot 2026-03-11 221359" src="https://github.com/user-attachments/assets/1d6fc672-61e8-4e8a-9741-63211851d80d" />
FULLSUBTRACTOR
<img width="1919" height="1079" alt="Screenshot 2026-03-11 221823" src="https://github.com/user-attachments/assets/32871f8d-6463-45b5-8bae-2f7b5b5b9f81" />

**Output Timing Waveform**
FULLADDER
<img width="1300" height="682" alt="Screenshot 2026-03-11 221856" src="https://github.com/user-attachments/assets/d3272619-b3f5-41aa-a112-aa560802fa69" />
FULLSUBTRACTOR
<img width="1307" height="694" alt="Screenshot 2026-03-11 221927" src="https://github.com/user-attachments/assets/d6f54152-b3dd-42ad-bfcb-956641e6231e" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



