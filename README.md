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
full adder:

![full adder tt](https://github.com/user-attachments/assets/bc37d0e7-65ce-435b-8077-a0ab6dd2ea32)


full subtractor:

![full-subtractor-truth-table](https://github.com/user-attachments/assets/d74bdc3b-3f39-41ec-be0a-21e35d8dcc6d)



**Procedure**

1. Type the program in quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for the input and output to generate the timing diagram.
5. For different input combination generate the timing diagram.


**Program:**
full adder:
```
module exp_4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor(sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,cl);
endmodule
```

full subtractor:
```
module exp_4_1(df,bo,a,b,bin);
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
Developed by: KIRTHICK SHA R RegisterNumber: 24900676
*/

**RTL Schematic**

full adder:

![Screenshot 2024-11-12 111942](https://github.com/user-attachments/assets/6b49db3c-76e4-416c-bf56-bad4b91927e2)

full subtractor :

![Screenshot 2024-11-19 112233](https://github.com/user-attachments/assets/822384cb-eb5f-409c-8731-70ca219825f8)




**Output Timing Waveform**
full adder :

![Screenshot 2024-11-12 112243](https://github.com/user-attachments/assets/c32ca58d-6ab7-4a7c-9af0-e6e3a1554c3f)

full subtractor:

![Screenshot 2024-11-19 113900](https://github.com/user-attachments/assets/cd79bfac-4414-4fc8-ba99-066e61f65794)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



