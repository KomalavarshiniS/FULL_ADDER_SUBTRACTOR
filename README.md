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

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

**Figure -1 FULL ADDER**

![image](https://github.com/user-attachments/assets/b679565b-d09f-4a71-9faf-6da470c66f6f)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Figure -1 FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/24e39e96-e9c8-44e9-9794-b7db17dce970)

**Truthtable**

FULL ADDER

![image](https://github.com/user-attachments/assets/8d7f56d6-2e80-4a9b-a9e3-e273db395494)

FULL SUBTACTOR

![image](https://github.com/user-attachments/assets/b2cc9fb4-3318-405f-bccd-5789b6329337)

**Procedure**

Write the detailed procedure here
 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire s1,c1,c2;

//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```
```
FULL SUBTRACTOR

module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule
```
```
Developed by:KOMALAVARSHINI.S
RegisterNumber:24900909
```

**RTL Schematic**

FULL ADDER
![exp4](https://github.com/user-attachments/assets/dc4041c9-3a28-44b6-833d-b39b145d01e4)
FULL SUBTRACTOR
![exp4a](https://github.com/user-attachments/assets/a9fccf24-3614-4c0c-91c5-250b2f2b6698)

**Output Timing Waveform**

FULL ADDER
![exp4 (2)](https://github.com/user-attachments/assets/0cbd8c54-3b43-426b-8eda-f7c34767b2c7)
FULL SUBTRACTOR
![exp4a (2)](https://github.com/user-attachments/assets/93ad6e80-d7ac-4959-adfb-9357bc71291b)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



