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

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:  G.Hindhu
RegisterNumber:212223230079

//full adder
module fulladd(sum,cout,a,b,cin);
   output sum;
	output cout;
	input a;
   input b;
   input cin;
  
        //Internal nets
 wire sl,cl,c2;

  //Instantiate logic gate primitives
 xor(sl,a,b);
 and(cl,a,b);
 xor(sum,sl,cin);
 and(c2,sl,cin);
 or(cout,c2,cl);
 endmodule 
```
![Screenshot 2024-04-04 103519](https://github.com/hindhujanaki/FULL_ADDER_SUBTRACTOR/assets/148514666/c26494b3-10d0-47db-93a5-024d1cae9685)
**RTL Schematic**
![Screenshot 2024-04-04 095313](https://github.com/hindhujanaki/FULL_ADDER_SUBTRACTOR/assets/148514666/47fe189c-93d9-4455-b608-1d351f1e2455)


**Output Timing Waveform**
![image](https://github.com/hindhujanaki/FULL_ADDER_SUBTRACTOR/assets/148514666/85fc7b07-295d-49f0-8282-3d0267b043ab)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



