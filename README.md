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
![Screenshot 2024-10-24 083251](https://github.com/user-attachments/assets/59c6199a-9768-4922-9515-53ff86107db9)
![Screenshot 2024-10-24 083301](https://github.com/user-attachments/assets/f44c6742-0a52-4124-bc99-764b9148a99b)

**Procedure*
STEP-1 Open Quartus Prime software.

STEP-2 Create a new project and select the target FPGA device.

STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

STEP-4 Add the HDL file to the project and compile the design.

STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: NAKUL R
RegisterNumber:212223240102
*/
module exp04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);
//FULL SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule
**RTL Schematic**

![Screenshot 2024-10-24 083349](https://github.com/user-attachments/assets/49838c04-834b-4284-bd35-749b87003873)

**Output Timing Waveform**

![Screenshot 2024-10-24 083416](https://github.com/user-attachments/assets/a22afe8f-c235-4c85-803a-fc905bd3dc91)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



