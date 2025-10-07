# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
module booleanexpression (
    input A, B, C, D,
    output F
);

    wire nB, nD, term1, term2, term3;

    // NOT gates
    not (nB, B);
    not (nD, D);

    // AND terms
    and (term1, nB, nD);   // B'D'
    and (term2, A, C);     // AC
    and (term3, B, D);     // BD

    // OR the terms
    or  (F, term1, term2, term3);

endmodule

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:s.vishvabala
RegisterNumber:25006451


**RTL realization**
<img width="702" height="400" alt="{9C0E35B2-DB1C-4593-A8A2-F22A6539B6B1}" src="https://github.com/user-attachments/assets/37e57fbe-8795-4c7f-8346-a990f654d30f" />


**Output:**

**RTL**
<img width="1276" height="861" alt="{A00291A6-2F32-4DEA-B37E-CC41661CF99C}" src="https://github.com/user-attachments/assets/4a3c84f2-ec3e-418a-a734-f77e448ad594" />


**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.



Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

