
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


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: VARSHINI S A
RegisterNumber:  22009118
```
HALF SUBTRACTOR  

module HS(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=(~a&b);
endmodule  

FULL SUBTRACTOR  
module FS(a,b,c,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b^c);
assign borr=(~a&(b^c)|(b&c));
endmodule  
```


## Output:

## Truthtable
HALF SUBTRACTOR  
![210802334-f7ee77a0-38db-4917-986a-e0c154cd17a8](https://user-images.githubusercontent.com/119401150/211158630-236c4741-5a89-4130-ad26-d62e00cc57a4.jpg)


FULL SUBTRACTOR  
![210806829-e8faa983-2648-444c-8290-2b1082744d52](https://user-images.githubusercontent.com/119401150/211158632-285c8914-abbd-4705-9539-feb2b7855cdd.jpg)




##  RTL realization

HALF SUBTRACTOR  

![WhatsApp Image 2023-01-07 at 17 54 47](https://user-images.githubusercontent.com/119401150/211158685-885abedd-0230-4745-8c9a-3cafefaa5e11.jpg)


FULL SUBTRACTOR  
![WhatsApp Image 2023-01-07 at 19 20 10](https://user-images.githubusercontent.com/119401150/211158674-919eb04f-6256-46af-9ce4-2f9e72df6299.jpg)



## Timing diagram 
HALF SUBTRACTOR  

![210794248-a1ec9343-5e1a-4f43-94f7-21aec0586c7c](https://user-images.githubusercontent.com/119401150/211158648-a9ca8b11-d93d-4b3a-aeca-7cc5a733b12f.png)


FULL SUBTRACTOR  

![210802008-99d86d7b-c012-460e-8ef5-fbcbb8c5f60b](https://user-images.githubusercontent.com/119401150/211158651-9b4bbe02-7566-4136-b689-e7e583ae3f8a.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
