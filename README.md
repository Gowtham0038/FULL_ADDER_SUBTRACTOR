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
![391812197-26765e12-1448-4442-8b42-e173735db3e5](https://github.com/user-attachments/assets/78138294-03a0-4dea-9850-882bae535beb)

**Procedure**

Write the detailed procedure here
~~~
**Program:**
module full(A,B,Cin,Bin,Sum,Carry,Diff,Borrow);
input A,B,Cin,Bin;
output Sum,Carry,Diff,Borrow;
assign Sum=A^(B^Cin);
assign Carry=(A&B)|(A&Cin)|(B&Cin);
assign Diff=A^(B^Bin);
assign Borrow=(~A&Bin)|(~A&B)|(B&Bin);
endmodule

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule
 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 Developed by: Gowtham C
 RegisterNumber: 24002349
*/
~~~
**RTL Schematic**
![391811939-bf2c0e59-2c59-4196-b095-2c9927831b8b](https://github.com/user-attachments/assets/c8170c9a-17e3-4f0e-bcb3-0bbd496eebc4)
![391812005-f0422017-40df-4f51-8b2b-18ebbb9d47ea](https://github.com/user-attachments/assets/553bf8c9-5ee9-4577-931b-30b2a27488bc) 
**Waveform**
![391812099-d5d06393-4aaa-4ce0-a983-ce784ddbf165](https://github.com/user-attachments/assets/3a8473b9-f273-4ab1-8e0c-908f3717bda7)
![391812145-9ab6111e-6845-4b51-9ecb-47c04441d845](https://github.com/user-attachments/assets/8c6e24b2-2cec-4735-be09-1ecc077704ea)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



