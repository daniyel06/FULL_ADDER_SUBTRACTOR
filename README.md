# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**DATE: 25/10/2024**

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

![image](https://github.com/user-attachments/assets/f8afc41a-66e1-4660-a7e1-4b28093ed2d5)

**Full Subtractor**

![image](https://github.com/user-attachments/assets/a51d1be3-da7b-41e3-9888-2c8bbf222b32)

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

Developed by: Daniyel Antony Raj SD

RegisterNumber: 212224220018

**Full Adder**
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
module FS(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
**RTL DIAGRAM**

**Full Adder**

![image](https://github.com/user-attachments/assets/4ae4e58f-7710-4b80-9bc5-08f4dc5afe6e)

**Full Subtractor**

![image](https://github.com/user-attachments/assets/ff68b900-1e10-4d7a-a9ed-2000f141156c)



**Timing Waveform**

**Full Adder**

![image](https://github.com/user-attachments/assets/b192938b-00f0-4357-bc42-52d0863eac77)

**Full Subtractor**

![image](https://github.com/user-attachments/assets/d392363a-6730-421f-a8f9-063246ff7bd2)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



