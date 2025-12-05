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
FULL ADDER 

![ttfulladder](https://github.com/user-attachments/assets/10b30295-3ca3-45aa-9873-591218b2ac77)

FULL SUBTRACTOR 

![ttfullsubtractor](https://github.com/user-attachments/assets/2aa09fda-f13f-41bd-b674-611d7c910a97)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:NITESH BHANDARI K 
RegisterNumber: 25009039
*/
FULL ADDER

module fa(a, b, cin, sum, carry);

input a, b, cin;

output sum, carry;

assign sum = (a ^ b) ^ cin;

assign carry = (a & b) | (cin & (a ^ b));

endmodule

FULL SUBRACTOR

module fs(a, b, bin, difference, borrow);

input a, b, bin;

output difference, borrow;

assign difference = (a ^ b) ^ bin;

assign borrow = (a & b) | (bin & ((a ^ b)));

**RTL Schematic**
FULL ADDER 

<img width="1902" height="768" alt="fulladder" src="https://github.com/user-attachments/assets/b25b5a29-6854-4ecb-8163-9983ed7fd2aa" />

FULL SUBTRACTOR 

<img width="1905" height="765" alt="fullsubtractor" src="https://github.com/user-attachments/assets/11722f5f-bbf6-4bd5-8b61-57b8fc4a0c65" />


**Output Timing Waveform**

FULL ADDER WAVEFORM 

<img width="1906" height="373" alt="fulladderwave" src="https://github.com/user-attachments/assets/1f9f788b-03cc-407e-a48d-e14698fba662" />

 FULL SUBTRACTOR 

 <img width="1910" height="426" alt="fullsubtractorwave" src="https://github.com/user-attachments/assets/5bd767b0-0e01-4046-a7eb-f7284d3e443e" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



