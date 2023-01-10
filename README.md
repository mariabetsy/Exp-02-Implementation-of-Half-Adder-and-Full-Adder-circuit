# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:

```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Maria Betsy 

RegisterNumber:  22008543

HALF ADDER 

module halfadder(A,B,Sum,Carry);
input A,B;
output Sum,Carry;
xor(Sum,A,B);
and(Carry,A,B);
endmodule

FULL ADDER

module fulladder(A,B,C,Sum,Carry);
input A,B,C;
output Sum,Carry;
assign Sum = ((A^B)^C);
assign Carry = ((A&B)|(B&C)|(C&A));
endmodule

```

### Output:
### Logic symbol & Truthtable
### TRUTH TABLE 
TRUTH TABLE FOR HALF ADDER

![TT EXP2](https://user-images.githubusercontent.com/122356434/211524520-cc938f20-84fa-4d28-b152-6d35eba3fb4d.jpeg)


TRUTH TABLE FOR FULL ADDER

![ttexp2](https://user-images.githubusercontent.com/122356434/211524741-32788442-afb0-48f5-85db-2bc5d1bc05d0.jpeg)


### RTL realization

RTL REALIZATION FOR HALF ADDER

![RTL HALF ADDER](https://user-images.githubusercontent.com/122356434/211525432-7f5e3409-837e-47cc-a474-c8819ca98d03.jpeg)


RTL REALIZATION FOR FULL ADDER

![RTL FULL ADDER](https://user-images.githubusercontent.com/122356434/211526074-ec609530-bbf3-455d-908a-b6c31420f2b1.jpeg)


### TIMING DIAGRAM

TIMING DIAGRAM FOR HALF ADDER:

![TIMING DIAGRAM (HALF ADDER)](https://user-images.githubusercontent.com/122356434/211526869-0a7fcf4a-0b69-466a-aabd-0f5ecb4f1a63.jpeg)

TIMING DIAGRAM FOR FULL ADDER:

![TIMING DIAGRAM (FULL ADDER)](https://user-images.githubusercontent.com/122356434/211527300-718da595-f825-4fef-82b8-62da613905f0.jpeg)


### Result:

Thus the Half adder and Full adder circuit was succesfully implemented.
