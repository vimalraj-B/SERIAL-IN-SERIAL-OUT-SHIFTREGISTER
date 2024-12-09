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

```
 1).Type the program in Quartus software.
 2).Compile and run the program.
 3).Generate the RTL schematic and save the logic diagram.
 4).Create nodes for inputs and outputs to generate the timing diagram.
 5).For different input combinations generate the timing diagram.
```


**PROGRAM**

```
module exp10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
```
![EXP 10](https://github.com/user-attachments/assets/d75af337-8e65-4f4d-a3f2-9960e90cc84d)


```

Developed by:B.VIMALRAJ
RegisterNumber:24900283.

```



**RTL LOGIC FOR SISO Shift Register**


![EXP 10 (2)](https://github.com/user-attachments/assets/63327504-e7f6-49de-ac41-aa952f81c8c8)



**TIMING DIGRAMS FOR SISO Shift Register**


![EXP 10 (3)](https://github.com/user-attachments/assets/7a8e176e-272b-40d1-bf6b-84095960927a)



**RESULTS**

```
Thus the Serial in and Serial out shift Register expression is verified using Quartus software.
```
