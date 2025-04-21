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

Write the detailed procedure here
Open Quartus Prime Software

Create a New Project

Create Verilog HDL File

Compile the Project

Open Simulation Tool

Run the Simulation and view results in the waveform viewer or console

Verify Truth Table

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: RegisterNumber: 212223110058
*/
```
**4.1**
module exp_4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```
```
**4.2**
exp_4b
module exp_4b(df, bo, a, b, bin);
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
**RTL Schematic**

# Full Adder
![435601997-3c8e210a-cc11-40f1-ae95-5fb22e493041](https://github.com/user-attachments/assets/27abfa74-14ed-4bc1-9dad-e637b62f6f69)

# # Full Subtractor
![435606091-9e01900a-1e16-4d12-b3ee-fd4a07e5c81c](https://github.com/user-attachments/assets/4d0e3883-d548-45eb-b01b-1f0e3c0b457c)

**Output Timing Waveform**

# Full Adder
![435602192-318827b4-5059-4a4b-8c5b-acc0dcb89c18](https://github.com/user-attachments/assets/0289dc5c-b06b-49ac-a0b3-dbafdd0d7e92)

# # Full Subtractor
![435606165-901b1df3-e77f-43e1-b735-7ddacc6c3bf3](https://github.com/user-attachments/assets/2daa607f-44e0-47f0-a4c1-c076dcbc71b7)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



