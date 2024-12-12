# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**


Step1: Define the specifications and initialize the design. 

Step2: Declare the name of the entity and architecture by using VHDL source code. 

Step3: Write the source code in VERILOG. 

Step4: Check the syntax and debug the errors if found, obtain the synthesis report. 

Step5: Verify the output by simulating the source code. 

Step6: Write all possible combinations of input using the test bench. 

Step7: Obtain the place and route report.  

**PROGRAM**

 Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: HARINI S

RegisterNumber:24900110

module shift_registers(din, clk, rst, dout); 

  input din; 
  
  input clk; 
  
  input rst; 
  
  output dout; 
  
  reg dout; 

  reg [7:0]x; 
  
  always @ (posedge(clk) or posedge(rst)) begin 
  
  if (rst==1'b1) 
  
  begin 
  
  dout=8'hzz; 
  
  end 
  
  else 
  
  begin 
  
  x={x[6:0],din}; 
  
  dout=x[7]; 
  
  end 
  
  end 
  
  endmodule 



**RTL LOGIC FOR SISO Shift Register**

![Screenshot (45)](https://github.com/user-attachments/assets/390b1284-f2a7-44b6-9dc1-d60db370d82a)


**TIMING DIGRAMS FOR SISO Shift Register**

![Screenshot (44)](https://github.com/user-attachments/assets/862d63b3-3920-4c26-ac35-d5af5cfe2cf5)

**RESULTS**

Thus the OUTPUT’s of 8-bit shift register are verified by synthesizing and simulating the 
VERILOG code.
