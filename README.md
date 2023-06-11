# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

Write the detailed procedure here 

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Athmaj Venugopal
RegisterNumber: 212222240014
*/
### Half Subractor:
```
module halfsub(A,B,Diff,Borrow);
input A,B; 
output Diff,borrow;
asssign Diff = (A ^ B);
assign Borrow = (~A & B);
endmodule

```
### Full Subractor:
```
module fullsub(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
assign Diff = (A^B^C);
assign borrow = (~a&(b^c)|(b&c));
endmodule
```
## Output:
### HALF SUBTRACTOR:
### GATES:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/311a1e36-e019-420a-8ce9-0e9f701f0ab8)

### RTL realization:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/7a5929a9-6862-4e4b-9ece-1b72d809b485)

### Truthtable:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/7170f6cd-66f2-4c98-9b38-9581551b36d6)


### Timing diagram :
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/d80f14f7-a87e-4ac0-af75-9782b6a0d006)


## FULL SUBTRACTOR:
### GATES:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/a1654bf9-b079-4e1e-8975-caa4ecd1bb93)

### RTL realization:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/e66b4175-2cd2-4d23-8715-664437616abe)


### Truthtable:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/502b31b2-c103-4cdb-961b-3acb5de39b90)


### Timing diagram:
![image](https://github.com/ATHMAJ03/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118753139/d6b544a1-b65e-4175-a132-d677c038d475)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
