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
module boolean_function_4var (
    input  wire A,
    input  wire B,
    input  wire C,
    input  wire D,
    output wire F
);

assign F = (~A & B) | (C & D) | (A & ~D);

endmodule

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:SANTHOSH SIVAKUMAR RegisterNumber:25013000

//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd //f2=xy'z+x'y'z+w'xy+wx'y+wxy // simplify the logic using Boolean minimization/k map //compute f2 and write verilog code for f2 as like f1

module EX_02(a,b,c,d,w,x,y,z,f1,f2); input a,b,c,d,w,x,y,z; output f1,f2; wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u; not(adash,a); not(bdash,b); not(cdash,c); not(ddash,d); not(ydash,y); and(p,bdash,ddash); and(q,adash,b,d); and(r,a,b,cdash); or(f1,p,q,r);

**RTL realization**
<img width="935" height="642" alt="652041684-4984a946-9a14-4990-9e0a-98d7b3a7197f" src="https://github.com/user-attachments/assets/82d28b12-d552-4be2-a39d-fc4364849811" />


**Output:**
<img width="935" height="582" alt="652042194-6e404397-45ae-4e0f-876d-755e23be44bd" src="https://github.com/user-attachments/assets/7d3dd5f8-a412-4280-a926-86c1ca0617a8" />


**Result:**
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

