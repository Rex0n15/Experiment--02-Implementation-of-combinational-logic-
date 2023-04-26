# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime


## Theory

+ A combinational logic circuit implement logical functions where its outputs depend only on its current combination of input values. On the other hand sequential circuits, unlike combinational logic, have state or memory.
+ Some logic operations may require more than one logic gate. Different combinations of gates are designed for different operations. The behaviour of the combined logic gates can be determined by constructing a truth table of the combined gates.

## Procedure
1. Create a project with required entities.
2. Create a module along with respective file name.
3. Run the respective programs for the given boolean equations.
4. Run the module and get the respective RTL outputs.
5. Create university program(VWF) for getting timing diagram.
6. Give the respective inputs for timing diagram and obtain the results
## Program:
```
Program For F1

module combilogic(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire G1,G2,G3,G4,G5;
assign G1=((~A)&(~B)&(~C)&(~D));
assign G2=((A)&(~C)&(~D));
assign G3=((~B)&(C)&(~D));
assign G4=((~A)&(B)&(C)&(D));
assign G5=((B)&(~C)&(D));
assign F1=G1|G2|G3|G4|G5;
endmodule
```
```
Program For F2

module combilogic(W,X,Y,Z,F);
input W,X,Y,Z;
output F;
wire G6,G7,G8,G9,G10;
assign G6=((X)&(~Y)&(Z));
assign G7=((~X)&(~Y)&(Z));
assign G8=((~W)&(X)&(Y));
assign G9=((W)&(~X)&(Y)); 
assign G10=((W)&(X)&(Y));
assign F=G6|G7|G8|G9|G10;
endmodule
```
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Rexon JP
RegisterNumber: 212222050048 
```
## Output:
### Output For F1
## RTL
![rtl f1](https://user-images.githubusercontent.com/130550796/234521044-a0aba03e-a89d-419f-9295-5dcf02cd4918.png)

## Timing Diagram
![time f1](https://user-images.githubusercontent.com/130550796/234521066-25d75381-13f2-4d97-906f-803ed3114717.png)

### Output for F2
## RTL
![rtl f2](https://user-images.githubusercontent.com/130550796/234521085-f38b8394-1386-4ed9-a07b-08535e3c7cf7.png)

## Timing Diagram
![time f2](https://user-images.githubusercontent.com/130550796/234521101-b1e9ec6a-6f42-4d90-999f-dc29f5a36264.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
