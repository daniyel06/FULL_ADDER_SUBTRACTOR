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

**Procedure**

Full Adder: 

1.Open Quartus II and create a new project. 

2.Use schematic design entry to draw the full adder circuit. 

3.The circuit consists of XOR, AND, and OR gates. 

4.Compile the design, verify its functionality through simulation. 5.Implement the design on the target device and program it.

Full Subtractor: 

1.Follow the same steps as for the full adder. 

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction. 

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: DANIYEL ANTONY RAJ SD

RegisterNumber: 24002985

**Fullull Adder**
```
module fa(a, b, cin, sum, carry);
  input a, b, cin;
  output sum, carry;
  
  assign sum = (a ^ b ^ cin);
  assign carry = (a & b) | (cin & (a ^ b));
endmodule
```
**Full Subtractor**
```
module fs(a,b,Bin,Borrow,Difference);
input a,b,Bin;
output Borrow,Difference;
assign Difference = a ^ b ^ Bin;
  assign Borrow = (a & b) | ((a ^ b) & Bin);
endmodule

```
**RTL Schematic**

**Full Adder**

![image](https://github.com/user-attachments/assets/4ae4e58f-7710-4b80-9bc5-08f4dc5afe6e)

**Full Subtractor**

![image](https://github.com/user-attachments/assets/de00131b-5923-415b-8bc4-0f6de01404bc)


**Output/Timing Waveform**

**Full Adder**

![image](https://github.com/user-attachments/assets/b192938b-00f0-4357-bc42-52d0863eac77)

**Full Subtractor**

![image](https://github.com/user-attachments/assets/c104147c-a6bd-4774-ad79-872074dd10a4)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



