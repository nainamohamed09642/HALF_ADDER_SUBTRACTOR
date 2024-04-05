FULL_ADDER_SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit

AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

Full Adder and Full Subtractor

Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin

Carry = AB + ACin + BCin

image

Figure -1 FULL ADDER

Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

image

Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

Truthtable
FULL ADDER image

FULL SUBTRACTOR image

Procedure

Write the detailed procedure here

Program:

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```

module exp04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);
//FUKK SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule
```

Developed by:Yuvaraj V RegisterNumber:212223230252*/

RTL Schematic  
![image](https://github.com/YuvarajVB/HALF_ADDER_SUBTRACTOR/assets/151488375/91e1e930-8ed9-4d87-aabb-e4464cb4b009)


Output Timing Waveform 
![image](https://github.com/YuvarajVB/HALF_ADDER_SUBTRACTOR/assets/151488375/e9aaefb1-d12e-45e4-ad2f-eec8f10f5f3d)


Result: Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
