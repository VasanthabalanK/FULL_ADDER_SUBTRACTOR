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
**Full Adder**
![full adder](https://github.com/user-attachments/assets/4ef4e26c-4520-43cf-8626-320b85d6f10c)
**Full Subtractor**
![full sub](https://github.com/user-attachments/assets/17ab9a1d-3fdb-47ce-b433-fed4d765ed9d)

**Procedure**

Write the detailed procedure here

**Program:**
**Full Adder**
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;

xor (sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,cl);

endmodule
```
**Full Subtractor**
```
module exp4a (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Vasanthabalan K 
RegisterNumber:24900992
*/

**RTL Schematic**
**Full Adder**
![exp4](https://github.com/user-attachments/assets/33a5e1b7-5a7a-4bbf-b9eb-57bfab79c4e7)

**Full Subtractor**
![exp4a](https://github.com/user-attachments/assets/223dc3b0-a311-4a4b-a127-1efc312cd989)

**Output Timing Waveform**
**Full Adder**
![Screenshot 2024-12-16 132039](https://github.com/user-attachments/assets/83689bbd-73da-471f-9c0a-21e119c0f8aa)

**Full Subtractor**
![Screenshot 2024-12-16 133032](https://github.com/user-attachments/assets/bfefcc48-1924-4ee4-98c0-3e3e21d17552)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



