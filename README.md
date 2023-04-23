# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

PROGRAM 1:
module expfour(a,b,c,d,f);
input a,b,c,d;
output f;
wire f,f2,f3;
assign f1 = (~c&~b&~a);
assign f2 = (~d&~c&~a);
assign f = (c&~(~b)&~a);
assign f = f1&~f2&`f3;
endmoudule

PROGRAM 2;
module expfourtwo(a,b,c,d,f);
input f;
wire f1,f2,f3,f4;
assign f1 = c&(~b)&a;
assign f2 = d&(~c)&a;
assign f3 = c&(~b)&a;
assign f4 = ~(f1|f2|f3);
not(f,f4);
endmodule

Developed by:K.DEEPIKA
RegisterNumber:212222050009  
*/

## RTL realization
## Output:
## RTL
PROGRAM 1
![rrp1](https://user-images.githubusercontent.com/128984662/233822341-bf01ed6b-e73d-4b27-a7b6-80ada1337892.jpeg)
PROGRAM 2
![rrp2](https://user-images.githubusercontent.com/128984662/233822372-edc4aa77-5c62-4a60-bab8-7a2b09f61c89.jpeg)

##TruthTable
PROGRAM 1
![ttp1](https://user-images.githubusercontent.com/128984662/233822453-08381a31-4b87-4be1-b84b-fc5bec2b89fe.jpeg)
PROGRAM 2
![ttp2](https://user-images.githubusercontent.com/128984662/233822460-a2419e13-7861-470f-82ba-116ce1fc0e6e.jpeg)

## Timing Diagram
PROGRAM 1
![tdp1](https://user-images.githubusercontent.com/128984662/233822472-0d3f6de2-2ae1-425c-b4b5-c7431ab95f37.jpeg)
PROGRAM 2
![tdp2](https://user-images.githubusercontent.com/128984662/233822485-5acb770e-317a-4f95-b84e-c2a17e28f966.jpeg)


## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
