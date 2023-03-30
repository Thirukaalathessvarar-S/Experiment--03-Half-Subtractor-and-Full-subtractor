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
### 1.Use module projname(input,output) to start the Verilog programmming.
### 2.Assign inputs and outputs using the word input and output respectively.
### 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
### 4.Use each output to represnt onre for differnce and the other for borrow.
### 5.End the verilog program using keyword endmodule.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Thirukaalathessvarar S
RegisterNumber:  212222230161
```
### Half Adder
```
module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule
```
### Full Adder
```
FULL SUBTRACTOR:
module fullsub(a,b,c,diff,borrow);
input a,b,c;
output borrow,diff;
wire an,q,r,s,t,cn,u;
not(an,a);
not(cn,c);
xor(q,a,b);
xor(diff,q,c);
and(s,a,b);
and(t,q,cn);
or(borrow,s,t);
endmodule
```

## OUTPUT :

## Truthtable :
### Full subractor
![full sub truth](https://user-images.githubusercontent.com/121166390/228721264-16f580ea-c0d8-4da7-876a-a56a6247c6be.png)
### Half subtractor
![half sub truth](https://user-images.githubusercontent.com/121166390/228721352-fcb8e055-2d0f-4e22-94e5-ba9059701af9.png)

##  RTL realization :
### Full subtractor
![full sub rtl](https://user-images.githubusercontent.com/121166390/228721397-c0ff358d-e2c5-4466-8bde-919625bec4cb.png)
### Half subtractor
![half sub rtl](https://user-images.githubusercontent.com/121166390/228721457-24d00ee8-03b0-459f-b70f-9f78e2dcb753.png)

## Timing diagram :
### Full subtractor
![full sub tim](https://user-images.githubusercontent.com/121166390/228721661-285fca6f-dcc9-416a-a6bc-1751a2895517.png)
### Half subtractor
![half sub tim](https://user-images.githubusercontent.com/121166390/228721704-fbe2a7aa-04e5-42b6-bb89-4117fd122a90.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
