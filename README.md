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

**Truthtable**

Half adder

![image](https://github.com/kishore-2506/HALF_ADDER_SUBTRACTOR/assets/165657398/5bb48c21-4c30-4412-9bfb-d4c013a0ce51)

Half subtractor

![image](https://github.com/kishore-2506/HALF_ADDER_SUBTRACTOR/assets/165657398/0ffde23f-0a9c-4fda-b8c2-e7843518fb06)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:KISHORE M.

RegisterNumber:212223040100
```
module HALF_ADDSUB(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo;
//HALF ADDER
xor(sum,a,b);
and(carry,a,b);


//HALF SUBTRACTOR
wire abar;
not(abar,a);
xor(D,a,b);
and(Bo,abar,b);
endmodule
```

**RTL Schematic**

![image](https://github.com/kishore-2506/HALF_ADDER_SUBTRACTOR/assets/165657398/3c3740ff-8cf0-49fc-8c81-9bc2e5769ec0)

**Output/TIMING Waveform**

## Half adder

![image](https://github.com/kishore-2506/HALF_ADDER_SUBTRACTOR/assets/165657398/242d6e1f-bdef-4af0-a756-4f5080bb1edf)
## Halfsub

![image](https://github.com/kishore-2506/HALF_ADDER_SUBTRACTOR/assets/165657398/242b94cb-12e2-423a-bf34-e69725ea26ea)


**Result:**

Thus Implementation-of-Half-Adder-and-Half Subtractor-circuit is running successfully
