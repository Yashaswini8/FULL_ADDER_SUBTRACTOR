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

FULL ADDER
![Screenshot 2024-12-21 170507](https://github.com/user-attachments/assets/6c4fad1a-1868-4a4b-8c31-b2f32b5e218b)



FULL SUBRACTOR

![Screenshot 2024-12-21 170559](https://github.com/user-attachments/assets/06b1a831-b5b5-4fa3-a193-34a35a7cf493)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
```
NAME:YASHASWINI S
REGISTER NUMBER:24900807
 
```
FULL ADDER
module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

```
FULL SUBRACTOR
```
module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule
``` 

**RTL Schematic**

FULL ADDER

![Screenshot 2024-12-21 170610](https://github.com/user-attachments/assets/54111a5d-17dd-49e1-b938-9bcf1bdb975e)


FULL SUBRACTOR

![Screenshot 2024-12-21 170617](https://github.com/user-attachments/assets/51c3db04-d8c4-427f-a4ff-96dd51295170)




**Output Timing Waveform**

FULL ADDER

![Screenshot 2024-12-21 170623](https://github.com/user-attachments/assets/077ccbb3-0a2a-4e80-a1d3-47ff266862a4)


FULL SUBRACTOR


![Screenshot 2024-12-21 170630](https://github.com/user-attachments/assets/7c9d240a-41fc-4ff1-8240-9a3bc0b5fdd5)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



