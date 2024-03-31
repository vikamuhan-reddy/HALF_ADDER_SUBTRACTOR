# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

## AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:

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

![WhatsApp Image 2024-03-31 at 19 17 33_4801cee5](https://github.com/vikamuhan-reddy/HALF_ADDER_SUBTRACTOR/assets/144928933/0cc91e1f-2e4e-43e7-b1d3-38796c9274d7)

## Procedure :

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


## Program:

'''Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:Vikamuhan reddy.N
RegisterNumber:212223240181'''

module half(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
xor(sum,a,b);//TYPE HERE THE COMMAND FOR SUM GENERATION IN GATE LEVEL MODELLING
and(carry,a,b);//TYPE HERE THE COMMAND FOR CARRY GENERATION IN GATE LEVEL MODELLING
wire abar;
not(abar,a);
xor(D,a,b);
and(Bo,abar,b);//Type logic for half subtractor difference D,Borrow Bo using gate level modelling
endmodule

## RTL Schematic:
![WhatsApp Image 2024-03-31 at 19 07 18_227c61b6](https://github.com/vikamuhan-reddy/HALF_ADDER_SUBTRACTOR/assets/144928933/06abe3f2-fae5-4b12-8769-33364292c9cb)


## Output/TIMING Waveform:
![WhatsApp Image 2024-03-31 at 19 00 46_42eff1fa](https://github.com/vikamuhan-reddy/HALF_ADDER_SUBTRACTOR/assets/144928933/b2582c6f-4d9d-4197-8a32-500ff6092d87)

## Result:
Thus the program is executed successfully.
