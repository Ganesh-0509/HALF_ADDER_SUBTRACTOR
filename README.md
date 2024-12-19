# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
![388817761-49ca9b44-6131-4cf9-8eb4-ce1698f1aa56](https://github.com/user-attachments/assets/2182becc-628d-48c2-ba1a-8878a3611509)
![388817781-a0948617-084f-4cc4-89c1-d9299fcd1346](https://github.com/user-attachments/assets/cf61d910-6aee-424f-9925-dff14424c1ee)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.



**Program:**
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
~~~
*Half_adder*
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule

*Half_subtractor*
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule

~~~


**RTL Schematic**
![DE E-3 RTL](https://github.com/04Varsha/HALF_ADDER_SUBTRACTOR/assets/149035374/4146d7c9-565b-4389-b8a2-54118b2c261e)

**Output/TIMING Waveform**

HALF ADDER:

![DE E-3 adder](https://github.com/04Varsha/HALF_ADDER_SUBTRACTOR/assets/149035374/8efe7503-fea8-4272-bf8b-0e334e95cdb1)

HALF SUTRACTOR:

![DE E-3 subtractor](https://github.com/04Varsha/HALF_ADDER_SUBTRACTOR/assets/149035374/5bd0588f-6b33-4352-bfb0-2e33f3f77f13)

**Result:** Thus the Half and Full Subtractors are studied and the truth tables are verified.
