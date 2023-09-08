# Exp-02 Implementation of Half Adder and Full Adder circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by:Sri Sai Priya.S 
RegisterNumber: 212222240103 
*/
HALF ADDER:
module exp3 (a,b,sum,carry);
input a,b;
output sum,carry;
assign sum = (a^b);
assign carry = (a&b);
endmodule

FULL ADDER:
module exp3b(a,b,Cin,s,c);
input a,b,Cin;
output s,c;
assign s= (a^b^Cin);
assign c = (a&b)|((a^b)&Cin);
endmodule
```

### Output:
### RTL
HALF ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/285c870a-a369-4f6e-9e51-ef0d1692de9b)

FULL ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/b889054b-1959-4375-901f-ec8a39bd6e81)

### TIMING DIAGRAM
HALF ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/c0395a4d-378d-4662-b6fd-873521fe0141)

FULL ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/1c405e50-6373-4b4b-a9af-eb0aa3c9ded8)

### TRUTH TABLE 
HALF ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/371a8bbd-c0ec-41d2-b886-1bfc39c55ea4)

FULL ADDER:
![image](https://github.com/SriSaiPriyaSenthilvel/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119475702/d668f73e-c15d-4016-9942-848832d3b74d)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
