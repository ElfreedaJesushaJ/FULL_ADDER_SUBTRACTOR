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
![Screenshot 2024-12-25 123524](https://github.com/user-attachments/assets/a080aaae-c64e-4405-b0bb-74603b359a9a)
![Screenshot 2024-12-25 123559](https://github.com/user-attachments/assets/b5e27c98-ab07-4e3e-9251-4c201d578ce4)



**Procedure**

Write the detailed procedure here

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: ELFREEDA JESUSHA J
RegisterNumber:24900146
```
```
Full Adder

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=((a^b)^cin);
assign carry=((a&b)|(cin&(a^b)));
endmodule

Full Subtractor

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference=((a^b)^bin);
assign borrow=((~a&b)|(bin&(~(a^b))));
endmodule

```

**RTL Schematic**
![fa rtl](https://github.com/user-attachments/assets/d69d4aaa-93ed-4a5c-9de9-1e12115fe324)
![fs rtl](https://github.com/user-attachments/assets/dc5b5be1-9eba-4779-ba93-9a1f5563bf0e)



**Output Timing Waveform**
![fa wf](https://github.com/user-attachments/assets/b6cb082a-213d-4b83-a884-56de5761b90f)
![fs wf](https://github.com/user-attachments/assets/b1727bde-ddc7-4fb5-b98f-cc519aa56684)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



