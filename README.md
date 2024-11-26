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
![image](https://github.com/user-attachments/assets/8ba98b07-8a67-436b-908c-1e518282521e)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
**Figure -1 FULL SUBTRACTOR**

![image](https://github.com/user-attachments/assets/25ce2fba-c302-4ddc-8575-901d7bf1d490)


**Truthtable**
Full adder
![image](https://github.com/user-attachments/assets/3a12627b-3348-46f2-a210-b9d420b0268e)
Full subractor
![image](https://github.com/user-attachments/assets/6484d089-fb58-485d-81a9-b316131df9a1)

**Procedure**

Write the detailed procedure here
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
Full adder

//full adder
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire s1,c1,c2;


//instantiate logic gate primitives
xor (s1,a,b);
and (c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);


endmodule

Full subtractor

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
assign df=^bin;
assign bo=w2|w3;
endmodule
```
Name: Priyanka P
Developed by: RegisterNumber:24900671

**RTL Schematic**
Full adder
![image](https://github.com/user-attachments/assets/5b6576a2-dd11-4271-b43c-d34e6f2575eb)
Full subtractor
![Screenshot 2024-11-26 103407](https://github.com/user-attachments/assets/2a819c6a-950f-4d1d-a82d-e19d45be116e)


**Output Timing Waveform**
Full adder
![image](https://github.com/user-attachments/assets/f8128b65-7858-481f-8eeb-97cb62508301)
Full subractor
![image](https://github.com/user-attachments/assets/dce8f1c4-d9cb-4694-a80f-b8ca28a17c9d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



